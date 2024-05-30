---
layout: post
title: 불변성을 유지하는법
date: 2024-05-27 10:29 +0900
description: 불변성을 유지하는법
image: https://github.com/123dd654/123dd654.github.io/assets/161431124/fa366153-db94-46d5-9f5e-f72a8e40378c
category: coding
tags: Immutability
published: true
sitemap: true
---

안녕하세요!
오늘은 불변성을 유지하는법에 대해 말씀드리겠습니다 🍞

## 불변성이란? (Immutability)
불변성은 프로그래밍에서 데이터의 원본이 훼손되지 않도록 보호하는 개념을 의미합니다.
불변한 데이터를 사용하면 코드의 예측 가능성과 안정성을 높일 수 있습니다.
데이터가 변경되지 않도록 하면, 특히 상태 관리와 관련된 버그를 줄이는 데 도움이 됩니다.


### ✔️ 불변성을 유지하는 방법

#### 01. 변수 이름 불변하게 하기

- var 대신 const를 사용하여 변수를 선언합니다.
const로 선언된 변수는 재할당이 불가능하므로, 변수의 이름을 불변하게 유지할 수 있습니다.

````javascript
const myName = "Alice";
// myName = "Bob"; // 오류 발생: const 변수는 재할당할 수 없음
````
--------------------------------------

#### 02. 값을 불변하게 하기

* 원시형 타입(Primitive Types):
숫자, 문자열, 불리언, null, undefined, symbol, BigInt와 같은 원시형 타입은 그 값 자체가 불변합니다.

````javascript
let age = 30;
age = 31; // 변수는 변경되지만, 원래 값 30은 불변
````

* 객체(Object Types): 객체는 속성 값을 변경할 수 있어 가변성을 가집니다.
객체를 불변하게 만드는 방법은 여러 가지가 있습니다.

<br />

> Object.assign: 새로운 객체를 생성하여 기존 객체의 속성을 복사하는 방법입니다.

````javascript
const original = { name: "Alice", age: 30 };
const copy = Object.assign({}, original);
copy.age = 31;

console.log(original.age); // 30 (원본 객체는 변경되지 않음)
````

<br />

> Object.freeze: 객체를 동결하여 객체의 속성을 변경할 수 없도록 만듭니다.

````javascript
const original = { name: "Alice", age: 30 };
Object.freeze(original);

// original.age = 31; // 오류 발생: 동결된 객체는 속성을 변경할 수 없음
````

<br />

> Nested Object: 객체가 중첩된 구조를 가질 경우, 깊은 복사를 통해 불변성을 유지할 수 있습니다.
이를 위해 라이브러리(예: Lodash)를 사용하거나 수동으로 구현할 수 있습니다.

````javascript
const original = { name: "Alice", address: { city: "Wonderland" } };
const copy = JSON.parse(JSON.stringify(original));
copy.address.city = "New Wonderland";

console.log(original.address.city); // "Wonderland" (원본 객체는 변경되지 않음)
````

<br />

> 불변 함수: 상태를 변경하지 않는 함수입니다. 새로운 값을 반환하는 방식으로 상태를 관리합니다.

````javascript
const original = [1, 2, 3];
const copy = original.concat(4);

console.log(original); // [1, 2, 3] (원본 배열은 변경되지 않음)
console.log(copy); // [1, 2, 3, 4] (새로운 배열 생성)
````
<br />
<br />
불변성은 데이터의 원본을 보호하여 코드의 안정성과 예측 가능성을 높이는 중요한 개념입니다.
<br /><br />
이를 유지하기 위해 변수 선언 시 const를 사용하고,
객체를 다룰 때는 Object.assign, Object.freeze, 깊은 복사, 불변 함수를 활용합니다.
이러한 방법을 통해 불변성을 유지하면 더 안전하고 유지 보수하기 쉬운 코드를 작성할 수 있습니다.
<br /><br />
오늘은 불변성을 유지하는법에 대해 알아보았습니다 유익한 시간 되셨길 바라며 이만 마치겠습니다 🤓





