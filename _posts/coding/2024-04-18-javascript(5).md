---
layout: post
title: switch, while문이란?
date: 2024-04-18 20:29 +0900
description: 자바스크립트 데이터 제어하기(2)
image: ../assets/img/blog.jpg
category: 자바스크립트
tags: switch문 while문
published: true
sitemap: true
---

[링크](https://github.com/123dd654/123dd654.github.io)


## 프로그램의 흐름을 제어하기<br />

### 01. switch문이란?               
JavaScript에서 switch문은 다양한 조건에 따라 다른 동작을 수행할 때 사용되는 제어 구조입니다.<br />
switch문은 if-else문과 유사하지만, 조건이 여러 가지 값을 가질 때 더 간결하게 코드를 작성할 수 있습니다.<br />
<br />
switch문의 기본 구조는 다음과 같습니다:

✤ switch문 예시문 ✤
````javascript 
{
const num = 100;

console.log("05. switch문")
switch (num) {
    case 90:
        console.log("실행되었습니다.(90)")
        break;
    case 95:
        console.log("실행되었습니다.(95)")
        break;
    case 100:
        console.log("실행되었습니다.(100)")
        break;
    case 105:
        console.log("실행되었습니다.(105)")
        break;
    default:
        console.log("실행되었습니다.")
    }
}
````

<div class="result">
<details>
   <summary>결과 확인하기</summary>
   <div>
         <b> 실행되었습니다.(100) </b>
   </div>
</details>
</div>

switch문은 먼저 표현식의 값을 평가하고,<br />
각 case문의 값과 비교하여 일치하는 경우 해당 case문의 코드 블록을 실행합니다.<br />
break문을 사용하여 해당 case문의 실행을 종료하고 switch문을 빠져나옵니다.<br />
만약 break문이 없다면, 일치하는 case문 이후의 모든 코드가 실행됩니다.<br />
마지막에 default문을 사용하여 표현식의 값이 어떤 case와도 일치하지 않을 때 실행될 코드를 정의할 수 있습니다.

<br />

### 02. while문이란?               
JavaScript에서 while문은 조건이 참인 동안 특정 코드 블록을 반복적으로 실행하는 제어 구조입니다.
while문은 반복 횟수가 불확실한 상황에서 사용됩니다.

while문은 먼저 조건을 평가하고, 조건이 참일 경우에만 코드 블록을 실행합니다.
코드 블록을 실행한 후 다시 조건을 평가하고, 조건이 여전히 참이면 코드 블록을 다시 실행합니다.<
이 과정을 조건이 거짓이 될 때까지 반복합니다.

while문의 기본 구조는 다음과 같습니다:<br />
while (조건) {// 조건이 참일 때 실행될 코드}

✤ 다중 if문 예시문 ✤
````javascript 
{
    let num = 1;            //초깃값;

    console.log("06. while문")
    while (num &lt;= 10) {     //조건식;
        console.log(num);   //실행문
        num++;              //증감값;
    }
}
````

<div class="result">
<details>
   <summary>결과 확인하기</summary>
   <div>
         <b> 1~10 </b>
   </div>
</details>
</div>




여기까지 switch문,while문에 대해 알아봤습니다.
도움이 되셨길 바라며 이만 마치겠습니다.
고생하셨습니다.🫶😊




                