---
layout: post
title: 데이터 형 변환
date: 2024-05-26 10:29 +0900
description: 데이터 형 변환
image: https://github.com/123dd654/123dd654.github.io/assets/161431124/8e0a10ec-a2d8-448b-88a8-cef26ea64819
category: coding
tags: TypeConversion
published: true
sitemap: true
---

안녕하세요!
오늘은 데이터형 변환에 대해 말씀드리겠습니다 🍞

### 데이터 형 변환 (Type Conversion)
데이터 형 변환이란, 하나의 데이터 타입을 다른 데이터 타입으로 변경하는 과정을 의미합니다.
<span style="background-color:#fff5b1">자바스크립트에서는 함수와 연산자에 전달되는 값이 대부분 적절한 자료형으로 자동 변환됩니다.</span>
데이터 형 변환에는 암시적 형 변환과 명시적 형 변환이 있습니다.

1. 암시적 형 변환 (Implicit Type Conversion)
자바스크립트는 상황에 따라 자동으로 데이터 타입을 변환합니다. 이를 암시적 형 변환이라고 하며, 개발자가 명시적으로 변환을 지시하지 않아도 자동으로 이루어집니다.

````javascript
// 문자열과 숫자의 덧셈
let result = "5" + 2;
console.log(result); // "52" (숫자 2가 문자열 "2"로 변환되어 결합됨)

// 문자열과 숫자의 곱셈
let result2 = "5" * 2;
console.log(result2); // 10 (문자열 "5"가 숫자 5로 변환되어 곱셈 수행)
````

✤ 암시적 형 변환 예시

````javascript
// 숫자와 문자열의 덧셈
let example1 = "The answer is " + 42; 
console.log(example1); // "The answer is 42"

// 숫자와 불리언의 덧셈
let example2 = 1 + true; 
console.log(example2); // 2 (true는 1로 변환됨)
````

-------------------------------------------------------

2. 명시적 형 변환 (Explicit Type Conversion)
개발자가 의도적으로 데이터 타입을 변환하는 것을 명시적 형 변환이라고 합니다.
이를 위해 자바스크립트는 여러 가지 변환 함수를 제공합니다.

- 숫자로 변환: Number() 함수 또는 parseInt(), parseFloat() 함수를 사용합니다.

````javascript
let str = "123";
let num = Number(str);
console.log(num); // 123

let str2 = "123.45";
let floatNum = parseFloat(str2);
console.log(floatNum); // 123.45
````

- 문자열로 변환: String() 함수나 toString() 메서드를 사용합니다.

````javascript
let num = 123;
let str = String(num);
console.log(str); // "123"

let bool = true;
let boolStr = bool.toString();
console.log(boolStr); // "true"
````

- 불리언으로 변환: Boolean() 함수를 사용합니다.

````javascript
let num = 0;
let bool = Boolean(num);
console.log(bool); // false (0은 false로 변환)

let str = "Hello";
let boolStr = Boolean(str);
console.log(boolStr); // true (빈 문자열이 아닌 경우 true로 변환)
````

✤ 명시적 형 변환 예시
````javascript
// 명시적으로 문자열을 숫자로 변환
let stringNum = "123";
let number = Number(stringNum);
console.log(number); // 123

// 명시적으로 숫자를 문자열로 변환
let num = 456;
let str = String(num);
console.log(str); // "456"

// 명시적으로 불리언을 숫자로 변환
let boolValue = true;
let numValue = Number(boolValue);
console.log(numValue); // 1
````

-------------------------------------------------------

<br />
<br />
<br />

데이터형 변환은 자바스크립트에서 함수와 연산자에 전달되는 값을 적절한 자료형으로 변경하는 과정입니다.

암시적 형 변환은 자바스크립트가 자동으로 수행하며, 명시적 형 변환은 개발자가 의도적으로 수행합니다.
이를 잘 이해하면 데이터 타입 간의 변환을 예측하고 원하는 결과를 얻을 수 있습니다.

오늘은 데이터형 변환에 대해 알아보았습니다 유익한 시간 되셨길 바라며 이만 마치겠습니다 🤓



