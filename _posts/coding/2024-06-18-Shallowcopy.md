---
layout: post
title: 자바스크립트 얕은 복사와 깊은 복사 이해하기
date: 2024-06-18 10:29 +0900
description: 자바스크립트 얕은 복사와 깊은 복사 이해하기
image: https://github.com/123dd654/123dd654.github.io/assets/161431124/be6ff23b-f5fd-4450-8a96-bc7d203324b4
category: coding
tags: JavaScript, Shallow Copy, Deep Copy
published: true
sitemap: true
---

## 자바스크립트 얕은 복사와 깊은 복사 이해하기

자바스크립트에서 객체를 복사할 때, 얕은 복사(Shallow Copy)와 깊은 복사(Deep Copy)의 개념을 이해하는 것이 중요합니다. 이 두 가지 개념은 객체의 중첩 구조를 어떻게 복사하는지에 따라 크게 다릅니다. 이번 글에서는 얕은 복사와 깊은 복사의 차이점과 이를 구현하는 방법에 대해 자세히 알아보겠습니다.

### 얕은 복사란?

얕은 복사는 객체의 1단계 깊이만 복사하는 방법입니다. 즉, 객체 안에 또 다른 객체가 있을 경우, 내부 객체는 원본 객체의 참조를 유지합니다.

#### 얕은 복사의 예시

```javascript
const original = {
  name: "John",
  address: {
    city: "New York",
    zip: "10001",
  },
};

const shallowCopy = { ...original };

console.log(shallowCopy.address === original.address); // true
```

위 예시에서 `shallowCopy` 객체는 `original` 객체와 동일한 `address` 객체를 참조하고 있습니다. 따라서 `address` 객체를 수정하면 `original`과 `shallowCopy` 모두에 영향을 미칩니다.

### 깊은 복사란?

깊은 복사는 객체의 모든 중첩 구조를 새롭게 복사하는 방법입니다. 즉, 객체 안에 또 다른 객체가 있을 경우, 내부 객체도 새로운 객체로 복사됩니다.

#### 깊은 복사의 예시

깊은 복사를 구현하는 방법은 여러 가지가 있습니다. 대표적으로 재귀적 복사, JSON 메서드 사용, 그리고 라이브러리를 이용한 방법이 있습니다.

##### 1. JSON 메서드를 이용한 깊은 복사

```javascript
const original = {
  name: "John",
  address: {
    city: "New York",
    zip: "10001",
  },
};

const deepCopy = JSON.parse(JSON.stringify(original));

console.log(deepCopy.address === original.address); // false
```

JSON 메서드를 이용한 깊은 복사는 간단하지만, 함수나 `undefined` 같은 특수한 값들은 복사되지 않는다는 단점이 있습니다.

##### 2. 재귀적 복사를 이용한 깊은 복사

```javascript
function deepClone(obj) {
  if (obj === null || typeof obj !== "object") {
    return obj;
  }

  if (Array.isArray(obj)) {
    const arrCopy = [];
    obj.forEach((item, index) => {
      arrCopy[index] = deepClone(item);
    });
    return arrCopy;
  }

  const objCopy = {};
  Object.keys(obj).forEach((key) => {
    objCopy[key] = deepClone(obj[key]);
  });
  return objCopy;
}

const original = {
  name: "John",
  address: {
    city: "New York",
    zip: "10001",
  },
};

const deepCopy = deepClone(original);

console.log(deepCopy.address === original.address); // false
```

재귀적 복사는 모든 중첩 객체를 순회하며 복사하는 방법으로, 함수와 같은 특수한 값들도 복사할 수 있습니다.

##### 3. 라이브러리를 이용한 깊은 복사

Lodash와 같은 라이브러리를 사용하면 깊은 복사를 간편하게 구현할 수 있습니다.

```javascript
const _ = require("lodash");

const original = {
  name: "John",
  address: {
    city: "New York",
    zip: "10001",
  },
};

const deepCopy = _.cloneDeep(original);

console.log(deepCopy.address === original.address); // false
```

Lodash의 `_.cloneDeep` 메서드는 복잡한 객체도 쉽게 깊은 복사할 수 있는 편리한 방법을 제공합니다.

### 얕은 복사와 깊은 복사의 차이점 요약

- 얕은 복사: 객체의 1단계 깊이만 복사. 내부 객체는 원본 객체와 참조를 공유.
- 깊은 복사: 객체의 모든 중첩 구조를 새롭게 복사. 내부 객체도 새로운 객체로 복사.

### 언제 얕은 복사와 깊은 복사를 사용해야 할까?

- 얕은 복사:

  - 객체가 단순하고 중첩되지 않은 경우.
  - 성능이 중요한 경우(깊은 복사는 더 많은 메모리와 시간이 소요됨).

- 깊은 복사:
  - 객체가 중첩된 구조를 가지고 있으며, 내부 객체를 독립적으로 조작해야 하는 경우.
  - 원본 객체와 복사된 객체가 완전히 독립적으로 동작해야 하는 경우.

### 성능 고려 사항

깊은 복사는 더 많은 메모리와 CPU 시간을 소모하기 때문에 성능에 영향을 줄 수 있습니다. 따라서 객체의 크기와 중첩 수준을 고려하여 적절한 복사 방법을 선택해야 합니다.

### 결론

얕은 복사와 깊은 복사는 자바스크립트에서 객체를 복사할 때 자주 사용되는 개념입니다. 이 두 가지 복사 방법의 차이점을 이해하고, 상황에 맞게 적절한 복사 방법을 선택하는 것이 중요합니다. 이번 글에서는 얕은 복사와 깊은 복사의 개념, 구현 방법, 그리고 사용 시의 고려 사항에 대해 살펴보았습니다.
