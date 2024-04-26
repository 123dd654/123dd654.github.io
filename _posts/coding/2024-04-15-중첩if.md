---
layout: post
title: 중첩 if문,삼항연산자
date: 2024-04-15 20:29 +0900
description: 자바스크립트 데이터 제어하기(2)
image: ../assets/img/blog.jpg
category: 자바스크립트
tags: 중첩if문 if문생략 삼항연산자
published: true
sitemap: true
---

[링크](https://github.com/123dd654/123dd654.github.io)


## 프로그램의 흐름을 제어하기<br />

### 01. 중첩 if문이란?               
중첩 if문은 if문 내부에 다시 if문을 포함시켜 여러 단계의 조건을 체크하는 방법입니다.<br />
중첩 if문을 사용하면 더 복잡한 조건을 다룰 수 있습니다.<br />
중첩 if문은 if문의 조건 블록 안에 또 다른 if문을 넣는 형태로 구성됩니다.

✤ 중첩 if문 예시문 ✤
````javascript 
{
    const num = 100;

    if (num == 100) {
        console.log("실행되었습니다.1")
        if (num == 100) {
            console.log("실행되었습니다.2")
            if (num == 100) {
                console.log("실행되었습니다.3")
            }
        }

    } else {
        console.log("실행되었습니다.4")
    }
}
````

<div class="result">
<details>
   <summary>결과 확인하기</summary>
   <div>
         <b> 실행되었습니다.1 </b><br>
         <b> 실행되었습니다.2 </b><br>
         <b> 실행되었습니다.3 </b>
   </div>
</details>
</div>

<br />

### 02. if문 생략 & 삼항연산자이란?               
자바스크립트에서 조건에 따라 다른 동작을 수행해야 할 때,<br />
if문 외에도 삼항 연산자(?:)를 사용하여 간결하게 코드를 작성할 수 있습니다.<br />
삼항 연산자는 if문을 간단하게 표현하는 방법 중 하나입니다.<br />
<br />
삼항 연산자의 기본 구조는 다음과 같습니다:<br />
조건 ? 참인 경우 실행할 코드 : 거짓인 경우 실행할 코드<br />
<br />
삼항 연산자를 사용하면 코드가 더 간결해지고 가독성이 향상됩니다.<br />
그러나 너무 복잡한 조건이나 다양한 경우를 다룰 때에는 if문이 더 나은 선택일 수 있습니다.

✤ 다중 if문 예시문 ✤
````javascript 
{
    const num = 100;

    if (num == 100) {
        console.log("true")
    }

    if (num == 100) console.log("true")     //위에 내용을 이렇게 생략가능

    if (num == 100) {
        console.log("true")
    } else {
        console.log("false")
    }

    //삼항 연산자(조건식 연산자)
    num == 100 ? console.log("true") : console.log("false");
}
````

<div class="result">
<details>
   <summary>결과 확인하기</summary>
   <div>
         <b> true </b><br>
         <b> true </b><br>
         <b> true </b><br>
         <b> true </b>
   </div>
</details>
</div>


여기까지 중첩if문,if문생략,삼항연산자에 대해 알아봤습니다.
도움이 되셨길 바라며 이만 마치겠습니다.
고생하셨습니다.🫶😊




                