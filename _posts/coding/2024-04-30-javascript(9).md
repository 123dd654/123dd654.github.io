---
layout: post
title: 리턴값 함수 매개+리턴값 함수 화살표 함수이란?
date: 2024-04-30 20:29 +0900
description: 자바스크립트 데이터 실행하기(3)
image: https://github.com/123dd654/123dd654.github.io/assets/161431124/d7558034-68be-4384-8bad-fe06ba8cd109
category: coding
tags: 리턴값 함수 매개+리턴값 함수 화살표함수
published: true
sitemap: true
---


## 프로그램 실행하기<br />

### 01. 리턴값 함수란?               
함수가 리턴값을 가질 때, 해당 함수는 호출자에게 결과를 반환합니다.
이 결과는 함수가 계산하거나 처리한 값입니다. 리턴값을 가진 함수는 주어진 입력에 대한 결과를 계산하고, 이
결과를 호출자에게 반환하게 됩니다.

프로그래밍에서 함수의 리턴값은 보통 함수의 실행 결과를 나타냅니다.
이것은 다른 함수나 변수에 할당하거나 조건문에서 사용되거나 출력되는 등 다양한 방식으로 활용될 수 있습니다.

✤ 리턴값 함수 예시문 ✤

````javascript 
{
    // 선언적 함수
    function func() {
        return "04. 함수 : 리턴값 함수";
    };
    console.log(func());

    //익명함수
    const func1 = function () {
        return "04. 함수 : 리턴값 함수";
    };
    console.log(func1());
}
````

<div class="result">
<details>
   <summary>결과 확인하기</summary>
   <div>
         <b> 04. 함수 : 리턴값 함수 </b>
         <b> 04. 함수 : 리턴값 함수 </b>
   </div>
</details>
</div>


### 02. 매개변수 + 리턴값 함수란?               
매개변수와 리턴값을 함께 사용하는 함수는 주로 입력을 받아 처리한 후 그 결과를 반환하는데 사용됩니다.
이렇게 함으로써 함수는 외부의 값을 받아들이고, 그 값을 기반으로 계산 또는 처리를 수행한 후 그 결과를 반환합니다.

✤ 매개변수 + 리턴값 함수 예시문 ✤

````javascript 
{
    //선언적 함수
    function func(str) {
        return str;
    };
    console.log(func("05. 함수 : 매개변수 + 리턴값 함수"));

    //익명함수
    const func1 = function (str) {
        return str;
    };
    console.log(func1("05. 함수 : 매개변수 + 리턴값 함수"));
}
````

<div class="result">
<details>
   <summary>결과 확인하기</summary>
   <div>
         <b> 05. 함수 : 매개변수 + 리턴값 함수 </b>
         <b> 05. 함수 : 매개변수 + 리턴값 함수 </b>
   </div>
</details>
</div>



### 03. 화살표 함수란?               
화살표 함수(arrow function)는 ES6(ECMAScript 2015)에서 도입된 새로운 함수 표현식입니다.
기존의 함수 표현식보다 간결하고 가독성이 높으며, 함수를 좀 더 간결하게 정의할 수 있습니다.


화살표 함수의 기본 구문은 다음과 같습니다:

````javascript 
    const functionName = (parameters) => {
    // 함수 본문
    };
````
여기서 parameters는 함수의 매개변수이고, => 기호 뒤에는 함수의 본문이 위치합니다.
만약 매개변수가 하나뿐이라면 괄호 ()를 생략할 수 있습니다.
또한, 함수의 본문이 단일 표현식인 경우 중괄호 {}와 return 키워드도 생략할 수 있습니다.

예를 들어, 기존의 함수 표현식과 비교해보겠습니다:

````javascript 
// 기존의 함수 표현식
    function sayHello(name) {
    return "Hello, " + name + "!";
    }

// 화살표 함수
    const sayHello = (name) => {
    return "Hello, " + name + "!";
    };

// 화살표 함수 (더 간결한 형태)
    const sayHello = (name) => "Hello, " + name + "!";
````

위의 예시에서 보듯이, 화살표 함수는 함수를 간결하게 작성할 수 있습니다.\
또한, this의 바인딩 동작이 일반 함수와 다르게 동작하기 때문에, 객체 메서드의 콜백 함수나 이벤트 핸들러 등에서 유용하게 사용됩니다.

화살표 함수의 특징을 요약하면 다음과 같습니다:

함수의 정의가 간결하고 가독성이 높습니다.
function 키워드 대신 => 기호를 사용합니다.
몸체가 한 줄인 경우 return 문과 중괄호 {}를 생략할 수 있습니다.
this가 자신을 감싼 정적 스코프를 가리킵니다.

화살표 함수는 일반적인 함수 표현식보다 코드를 간결하게 만들어주고, 특히 콜백 함수나 간단한 함수를 정의할 때 효과적입니다.


여기까지 리턴값 함수 ,매개+리턴값 함수 ,화살표함수에 대해 알아봤습니다.
도움이 되셨길 바라며 이만 마치겠습니다.
고생하셨습니다.🫶😊