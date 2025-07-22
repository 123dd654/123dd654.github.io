---
layout: post
title: 자바스크립트 데이터 타입
date: 2024-05-25 10:29 +0900
description: 자바스크립트 데이터 타입
image: https://github.com/123dd654/123dd654.github.io/assets/161431124/c7c13c03-7de9-4993-8f52-509c71093cb6
category: 2024년도 공부내용
tags: number string boolean null undefined symbol object array function BigInt
published: true
sitemap: true
---

안녕하세요!
오늘은 자바스크립트 데이터 타입에 대해 말씀드리겠습니다 🍞

## 데이터 타입이란?

데이터 타입은 프로그래밍 언어에서 사용할 수 있는 값의 종류를 정의하는 개념입니다.
각 값은 특정 타입을 가지며, 이는 그 값이 어떤 종류의 데이터인지, 그리고 어떻게 다뤄질 수 있는지를 결정합니다.
자바스크립트를 비롯한 대부분의 프로그래밍 언어에서 데이터 타입은 코드의 안정성과 예측 가능성을 높이는 데 중요한 역할을 합니다.

✨왜 데이터 타입이 중요한가?

- 정확한 연산: 데이터 타입을 알면 특정 값이 어떤 연산에 적합한지 알 수 있습니다.
  예를 들어, 숫자끼리 더할 수 있지만, 문자열을 숫자처럼 더하는 것은 의미가 없습니다.
- 메모리 관리: 각 데이터 타입은 메모리를 사용하는 방식이 다릅니다.
  이를 통해 프로그램의 효율성을 높일 수 있습니다.
- 코드의 가독성: 데이터 타입을 명시하면 코드의 가독성이 높아집니다.
  다른 개발자들이 코드를 읽고 이해하기 쉬워집니다.
- 오류 방지: 잘못된 데이터 타입의 사용을 방지하여 런타임 오류를 줄일 수 있습니다.
  예를 들어, 숫자가 필요한 곳에 문자열이 들어가면 에러가 발생할 수 있습니다.

## 자바스크립트에서의 데이터 타입

- 자바스크립트에서는 다양한 데이터 타입을 지원하며, 이를 크게 원시 타입과 객체 타입으로 구분합니다.
  원시 타입은 실제 값을 가지고, 객체 타입은 값의 주소를 참조합니다.

아래에서 종류 및 예시코드를 보며 설명드리겠습니다.😉

### 원시 타입 (Primitive Types)

원시 타입은 단순한 데이터로, 실제 값을 그대로 가집니다.
원시 타입에는 다음과 같은 종류가 있습니다:

1.  number: 숫자를 나타내는 데이터 타입으로, 정수와 실수를 모두 포함합니다.

```javascript
let age = 25;
let temperature = 36.5;
```

2.  string: 문자열을 나타내는 데이터 타입으로, 따옴표로 감싼 텍스트입니다.

```javascript
let greeting = "Hello, world!";
let name = "Alice";
```

3.  boolean: 논리 값을 나타내는 데이터 타입으로, true 또는 false 값을 가집니다.

```javascript
let isActive = true;
let isCompleted = false;
```

4.  null: 값이 없음을 나타내는 데이터 타입으로, 의도적으로 비어 있음을 명시합니다.

```javascript
let emptyValue = null;
```

5.  undefined: 값이 정의되지 않았음을 나타내는 데이터 타입으로,
    변수가 선언되었지만 아직 값이 할당되지 않은 경우입니다.

```javascript
let notAssigned;
console.log(notAssigned); // undefined
```

6.  symbol: 고유한 식별자를 나타내는 데이터 타입으로, ES6(ECMAScript 2015)에서 추가되었습니다.
    주로 객체의 속성 키로 사용됩니다.

```javascript
let symbol1 = Symbol("description");
let symbol2 = Symbol("description");
console.log(symbol1 === symbol2); // false
```

✤✤ 추가적인 데이터 타입 ✤✤

- ES6 이후 자바스크립트에는 새로운 데이터 타입과 기능들이 추가되었습니다.
  여기에는 BigInt 타입이 포함되며, 이는 매우 큰 정수를 다루기 위한 데이터 타입입니다.

7.  BigInt: 안전한 정수 범위를 넘어서는 큰 정수를 표현할 수 있는 데이터 타입입니다.

```javascript
let bigNumber = BigInt(9007199254740991) + BigInt(1);
console.log(bigNumber); // 9007199254740992n
```

---

### 객체 타입 (Object Types)

객체 타입은 실제 값이 아니라 값의 주소를 참조합니다.
자바스크립트에서 객체는 복합적인 데이터 구조로, 여러 값을 키-값 쌍으로 저장할 수 있습니다.
객체 타입에는 다음과 같은 종류가 있습니다:

1.  object: 키-값 쌍의 모음으로, 여러 속성을 가질 수 있습니다.

```javascript
let person = {
  name: "John",
  age: 30,
  isEmployed: true,
};
console.log(person.name); // John
```

2.  array: 순서가 있는 값의 모음으로, 여러 값을 하나의 변수에 저장할 수 있습니다.

```javascript
let numbers = [1, 2, 3, 4, 5];
console.log(numbers[0]); // 1
```

3.  function: 실행 가능한 코드 블록으로, 특정 작업을 수행하는 데 사용됩니다.

```javascript
function greet(name) {
  return "Hello, " + name;
}
console.log(greet("Alice")); // Hello, Alice
```

---

🩵데이터 타입 확인🩵

- 자바스크립트에서 변수의 데이터 타입을 확인하기 위해 typeof 연산자를 사용할 수 있습니다.

```javascript
console.log(typeof 42); // "number"
console.log(typeof "hello"); // "string"
console.log(typeof true); // "boolean"
console.log(typeof undefined); // "undefined"
console.log(typeof null); // "object" (자바스크립트의 오래된 버그)
console.log(typeof Symbol("symbol")); // "symbol"
console.log(typeof { name: "Alice" }); // "object"
console.log(typeof [1, 2, 3]); // "object" (배열도 객체로 취급됨)
console.log(typeof function () {}); // "function"
console.log(typeof BigInt(123456789012345678901234567890)); // "bigint"
```

- 자바스크립트의 데이터 타입을 잘 이해하면 더 안정적이고 예측 가능한 코드를 작성할 수 있습니다.
  원시 타입과 객체 타입의 차이를 알고 이를 적절히 활용하는 것이 중요합니다.

---

<br />
<br />
<br />

자바스크립트의 데이터 타입은 원시 타입과 객체 타입으로 나뉘며, 각각의 특성을 이해하는 것이 중요합니다.

원시 타입은 실제 값을 가지며 단순한 데이터를 표현하고, 객체 타입은 값의 주소를 참조하여 복합적인 데이터를 다룰 수 있습니다.이러한 데이터 타입의 이해는 자바스크립트로 효율적이고 안정적인 코드를 작성하는 데 필수적입니다.

오늘은 자바스크립트 데이터 타입에 대해 알아보았습니다 유익한 시간 되셨길 바라며 이만 마치겠습니다 🤓
