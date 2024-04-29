---
layout: post
title: do while문, for문, 중첩 for문
date: 2024-04-25 20:29 +0900
description: 자바스크립트 데이터 제어하기(3)
image: ../assets/img/blog.jpg
category: 자바스크립트
tags: dowhile문 for문 중첩for문
published: true
sitemap: true
---


## 프로그램의 흐름을 제어하기<br />

### 01. do while문이란?               
JavaScript의 do...while문은 while문과 유사하지만,
코드 블록을 먼저 실행하고 조건을 검사하는 차이점이 있습니다.
do...while문은 코드 블록을 먼저 실행하고 나서 조건을 평가하므로, 코드 블록이 최소 한 번은 실행됩니다.
do...while문은 먼저 코드 블록을 실행한 후에 조건을 평가합니다.
조건이 참이면 코드 블록을 다시 실행하고, 조건이 거짓이면 반복을 종료합니다.

do...while문은 코드 블록이 최소 한 번은 실행되어야 하는 상황에서 사용됩니다.
예를 들어, 사용자의 입력이 유효한지 검사하고자 할 때나 반복적인 작업을 수행한 후에 조건을 검사하고자 할 때 유용합니다.

do...while문의 기본 구조는 다음과 같습니다:
do {// 실행될 코드} while (조건);

✤ do while문 예시문 ✤

````javascript 
{
    let num = 1;            //초깃값;

    console.log("06. while문")
    while (num <= 10) {     //조건식;
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


### 02. for문이란?               
아래의 코드는 1부터 10까지의 숫자를 출력하는 for문입니다.
먼저 변수 i를 1로 초기화하고, i가 10보다 작거나 같은 동안에만 반복합니다.
반복할 때마다 i를 1씩 증가시키면서 각 숫자를 출력합니다.

따라서 주어진 코드는 정상적으로 동작하며, 실행하면 콘솔에 1부터 10까지의 숫자가 출력됩니다.

✤ for문 예시문 ✤

````javascript 
{
    for (let i = 1; i <= 10; i++) {     //초깃값; 조건식; 증감값;
        console.log(i);                    //실행문
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



### 03. 중첩 for문이란?               
중첩 for문은 하나의 for문 안에 다시 다른 for문이 들어가는 형태입니다.
이를 사용하여 다차원 배열이나 이차원 데이터 구조를 탐색하거나 처리할 때 유용합니다.
중첩 for문은 각각의 for문이 반복되는 동안 다른 for문을 포함하여 일정한 패턴을 반복적으로 실행합니다.

외부 for문과 내부 for문 각각에 대해 초기식, 조건식, 증감식이 있습니다.
외부 for문이 한 번 실행될 때마다 내부 for문이 전체 반복됩니다.
내부 for문의 반복이 완료되면 외부 for문의 증감식이 실행되고,
조건을 다시 평가하여 반복 여부를 결정합니다.

중첩 for문의 기본 구조는 다음과 같습니다:
````javascript
{
    for (초기식1; 조건1; 증감식1) {
    // 외부 for문의 실행 내용
    for (초기식2; 조건2; 증감식2) {
        // 내부 for문의 실행 내용
        }
    }
}
````

✤ 중첩 for문 예시문 ✤

````javascript 
{
    for (let i = 1; i <= 10; i++) {
        for (let j = 1; j <= 10; j++) {
            console.log(i, j)
        }
    }
}
````

<div class="result">
<details>
   <summary>결과 확인하기</summary>
   <div>
         <b> 1 2,1 3,1 4...10 9,10 10 </b>
   </div>
</details>
</div>


<br />
<br />
<br />


여기까지 do while문, for문, 중첩 for문에 대해 알아봤습니다.
도움이 되셨길 바라며 이만 마치겠습니다.
고생하셨습니다.🫶😊




                