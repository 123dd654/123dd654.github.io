---
layout: post
title: if문,다중if문
date: 2024-04-14 17:29 +0900
description: 자바스크립트 데이터 제어하기
image: https://github.com/123dd654/123dd654.github.io/assets/161431124/4ea8e722-f46c-4118-bccf-76f8e82f8c4b
category: 자바스크립트
tags: if문 다중if문
published: true
sitemap: true
---



## 프로그램의 흐름을 제어하기<br />

### 01. if문이란?               
if문은 프로그래밍에서 조건을 검사하고 그에 따라 코드를 실행하는 데 사용되는 제어 구조입니다.<br />
일반적으로 조건이 참(True)일 때 코드 블록이 실행되며, 조건이 거짓(False)이면 실행되지 않습니다.<br />
이는 프로그램이 특정 조건에 따라 다른 동작을 할 수 있도록 하는 데 매우 유용합니다.<br />
조건은 참(True) 또는 거짓(False)이 될 수 있는 표현식이며, 조건을 만족하는 경우에만 코드 블록이 실행됩니다.<br />
코드 블록은 일반적으로 들여쓰기로 구분됩니다.<br />
<br />
if문은 추가적인 옵션으로 else문을 사용하여 조건이 거짓일 때 실행할 코드를 지정할 수 있습니다.

✤ if문 예시문 ✤
````javascript 
{
  //true, "문자열", 1, 2, "1", "2", [], {}
  //false, ""(빈문자열), 0, null, undefined
    
    if (0) {
        console.log("실행되었습니다.(true)");
    } else {
        console.log("실행되었습니다.(false)");
    }
}
````

<div class="result">
<details>
   <summary>결과 확인하기</summary>
   <div>
         <b> 실행되었습니다.(true) </b><br>
         <b> 실행되었습니다.(false) </b>
   </div>
</details>
</div>

<br />

### 02. 다중 if문이란?               
다중 if문은 조건에 따라 여러 가지 경우를 처리할 때 사용되는 제어 구조입니다.<br />
자바스크립트에서 if문은 조건이 참(true)일 때 특정 코드 블록을 실행합니다.<br />
다중 if문은 하나 이상의 if문을 조합하여 여러 가지 조건을 처리할 때 사용됩니다.<br />
첫 번째 조건부터 순서대로 확인하며, 조건이 참이면 해당 코드 블록이 실행됩니다.<br />
조건이 거짓이면 다음 조건으로 넘어가게 됩니다.<br />
만약 모든 조건이 거짓이라면 felse 블록이 실행됩니다.

✤ 다중 if문 예시문 ✤
````javascript 
{
    const num = 100;

    if (num == 90) {
        console.log("실행되었습니다.(90)")
    } else if (num == 100) {
        console.log("실행되었습니다.(100)")
    } else if (num == 110) {
        console.log("실행되었습니다.(110)")
    } else if (num == 120) {
        console.log("실행되었습니다.(120)")
    } else if (num == 130) {
        console.log("실행되었습니다.(130)")
    } else {
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


여기까지 if문. 다중if문에 대해 알아봤습니다.
도움이 되셨길 바라며 이만 마치겠습니다.
고생하셨습니다.🫶😊

                