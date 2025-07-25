---
layout: post
title: 익명함수,매개변수함수란?
date: 2024-04-13 17:29 +0900
description: 자바스크립트 데이터 실행하기
image: https://github.com/123dd654/123dd654.github.io/assets/161431124/f8ccbc25-b73f-45b8-b9f0-8f724ebf1127
category: 2024년도 공부내용
tags: 익명함수 매개변수함수
published: true
sitemap: true
---

## 프로그램 실행하기<br />

### 01. 익명 함수란?

익명 함수는 이름이 없는 함수를 가리킵니다.<br>
일반적으로 함수를 정의할 때 함수의 이름을 지정하는데, 익명 함수는 이름을 가지지 않기 때문에 익명 함수라고 부릅니다.<br>
익명 함수는 코드를 보다 간결하게 만들고, 필요한 곳에 간편하게 사용할 수 있는 장점이 있습니다
<br />

✤ 익명 함수 예시문 ✤

```javascript
{
  const func = function () {
    console.log("02. 함수가 실행되었습니다.");
  };
  func();
}
```

<div class="result">
<details>
   <summary>결과 확인하기</summary>
   <div>
         <b> 02. 함수가 실행되었습니다. </b>
   </div>
</details>
</div>

<br />

### 02. 매개변수 함수란?

매개변수(parameter)는 컴퓨터 프로그래밍 및 수학에서 사용되는 중요한 개념입니다.<br>
매개변수는 함수나 프로시저에 입력으로 전달되는 값을 나타냅니다.<br>
이러한 값은 함수나 프로시저가 실행되는 동안에만 유효합니다.<br>
<br>
프로그래밍에서 매개변수는 함수에 전달되는 값들을 가리키며, 함수를 호출할 때 해당 값들을 함수 내부로 전달합니다.<br>
매개변수는 함수의 정의에 포함되어야 하며, 함수를 호출할 때 실제로 전달되는 값과 매핑됩니다.<br>

✤ 매개변수 함수 예시문 ✤

```javascript
{
  // 선언적 함수
  function func(str) {
    console.log(str);
  }
  func("03. 함수가 실행되었습니다.");

  // 익명 함수
  const func1 = function (str) {
    console.log(str);
  };
  func1("03. 함수가 실행되었습니다.");
}
```

<div class="result">
<details>
   <summary>결과 확인하기</summary>
   <div>
         <b> 03. 함수가 실행되었습니다. </b><br>
         <b> 03. 함수가 실행되었습니다. </b>
   </div>
</details>
</div>

여기까지 익명함수, 매개변수함수에 대해 알아봤습니다.
도움이 되셨길 바라며 이만 마치겠습니다.
고생하셨습니다.🫶😊
