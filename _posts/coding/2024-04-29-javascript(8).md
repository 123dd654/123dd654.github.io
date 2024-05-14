---
layout: post
title: break문 continue문이란?
date: 2024-04-29 20:29 +0900
description: 자바스크립트 데이터 제어하기(4)
image: https://github.com/123dd654/123dd654.github.io/assets/161431124/281e55ed-b9ca-40bb-b34f-3bd487895aeb
category: coding
tags: break문 continue문
published: true
sitemap: true
---


## 프로그램의 흐름을 제어하기<br />

### 01. break문이란?               
JavaScript에서의 break문은 반복문(for, while, do...while)이나 switch문을 빠져나오는 데 사용됩니다.
break문을 만나면 가장 가까운 반복문이나 switch문을 즉시 종료하고 해당 반복문이나 switch문을 빠져나옵니다.
break문은 주로 반복문 내에서 특정 조건을 만족했을 때 반복을 중지하고 루프를 탈출하는 데 사용됩니다.

switch문 내에서 break문을 사용하여 각 case문이 실행된 후에 switch문을 빠져나올 수 있습니다.
이를 통해 해당 case문을 실행한 후 다음 case문들을 실행하지 않고 switch문을 종료할 수 있습니다.

✤ break문 예시문 ✤

````javascript 
{
    for (let i = 1; i < 10; i++) {
        if (i == 5) {
            break;
        }
        console.log(i);
    }
}
````

<div class="result">
<details>
   <summary>결과 확인하기</summary>
   <div>
         <b> 1~4 </b>
   </div>
</details>
</div>


### 02. continue문이란?               
JavaScript에서의 continue문은 반복문(for, while, do...while)에서
특정 조건이 충족될 때 현재 반복을 중지하고 다음 반복으로 넘어가는 데 사용됩니다.

continue문을 만나면 반복문의 현재 반복을 종료하고 다음 반복으로 넘어갑니다.
따라서 반복문의 나머지 부분은 실행되지 않고 바로 다음 반복이 실행됩니다.

continue문은 주로 특정 조건을 만족하는 경우에 해당 반복을 건너뛰고자 할 때 사용됩니다.
예를 들어, 특정 조건을 만족하는 경우에만 특정 작업을 수행하고자 할 때 유용합니다.

✤ continue문 예시문 ✤

````javascript 
{
    console.log("11. continue문")
    for (let i = 1; i < 10; i++) {
        if (i == 5) {
            continue;
        }
        console.log(i);
    }
}
````

<div class="result">
<details>
   <summary>결과 확인하기</summary>
   <div>
         <b> 1 2 3 4 6 7 8 9 </b>
   </div>
</details>
</div>

<br />
<br />
<br />

## ✔️break문, continue문 문제 예제

* 다음 코드를 실행했을 때 화면에 어떤 숫자들이 출력될까요?

````javascript 
{
    for (let i = 1; i <= 10; i++) {
    if (i % 2 === 0) {
        continue;
    }
    console.log(i);
    }
}
````

<div class="result">
<details>
   <summary>결과 및 설명 확인하기</summary>
   <div>
         <b> 1 3 5 7 9 </b>
         <p>✨ 이 코드는 1부터 10까지의 숫자를 반복하면서, 각 숫자가 홀수인 경우에만 출력합니다. continue 문은 짝수일 경우 해당 숫자를 건너뛰도록 합니다.</p>
   </div>
</details>
</div>


* 다음 배열을 반복하면서 첫 번째로 5를 만날 때의 숫자 출력 결과는 무엇일까요?

````javascript 
{
    const arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
    for (let num of arr) {
        if (num === 5) {
            console.log("5를 발견했습니다.");
            break;
        }
        console.log(num);
    }
}
````

<div class="result">
<details>
   <summary>결과 및 설명 확인하기</summary>
   <div>
         <b> 1, 2, 3, 4, "5를 발견했습니다." </b>
         <p>✨ 이 코드는 주어진 배열에서 숫자를 반복하면서, 5를 만나면 "5를 발견했습니다."를 출력하고 반복을 종료합니다.</p>
   </div>
</details>
</div>


* 다음 코드를 실행했을 때 화면에 어떤 숫자들이 출력될까요?

````javascript 
{
    for (let i = 1; i <= 100; i++) {
        if (i === 30) {
            console.log("30을 발견했습니다.");
            break;
        }
        if (i % 3 !== 0) {
            continue;
        }
        console.log(i);
    }
}
````

<div class="result">
<details>
   <summary>결과 및 설명 확인하기</summary>
   <div>
         <b> 3, 6, 9, 12, ..., 27, "30을 발견했습니다." </b>
         <p>✨ 이 코드는 1부터 100까지의 숫자를 반복하면서, 3의 배수일 때 해당 숫자를 출력합니다. 그러나 숫자가 30일 때 반복이 종료됩니다.</p>
   </div>
</details>
</div>


* 다음 코드를 실행했을 때 화면에 어떤 숫자들이 출력될까요?

````javascript 
{
    for (let i = 1; i <= 20; i++) {
        if (i === 10) {
            console.log("10을 발견했습니다.");
            break;
        }
        if (i % 2 !== 0) {
            continue;
        }
        console.log(i);
    }
}
````

<div class="result">
<details>
   <summary>결과 및 설명 확인하기</summary>
   <div>
         <b> 2, 4, 6, 8, "10을 발견했습니다." </b>
         <p>✨ 이 코드는 1부터 20까지의 숫자를 반복하면서, 짝수일 때만 해당 숫자를 출력합니다. 그리고 숫자가 10일 때 반복이 종료됩니다.</p>
   </div>
</details>
</div>

* 다음 배열을 반복하면서 첫 번째로 0보다 큰 숫자를 만날 때의 숫자 출력 결과는 무엇일까요?

````javascript 
{
    const arr = [-3, 5, -2, 0, 10, -7];
    for (let num of arr) {
        if (num > 0) {
            console.log(num);
            break;
        }
    }
}
````

<div class="result">
<details>
   <summary>결과 및 설명 확인하기</summary>
   <div>
         <b> 5 </b>
         <p>✨ 이 코드는 주어진 배열에서 숫자를 반복하면서, 첫 번째로 0보다 큰 숫자를 만나면 해당 숫자를 출력하고 반복을 종료합니다.</p>
   </div>
</details>
</div>


* 다음 코드를 실행했을 때 화면에 어떤 숫자들이 출력될까요?

````javascript 
{
    for (let i = 1; i <= 10; i++) {
        if (i === 5) {
            continue;
        }
        if (i > 5) {
            console.log(i);
        }
    }
}
````

<div class="result">
<details>
   <summary>결과 및 설명 확인하기</summary>
   <div>
         <b> 6, 7, 8, 9, 10 </b>
         <p>✨ 이 코드는 1부터 10까지의 숫자를 반복하면서, 숫자가 5일 때는 건너뜁니다. 그리고 5보다 큰 숫자만을 출력합니다.</p>
   </div>
</details>
</div>


<br />
<br />
<br />

여기까지 break문, continue문에 대해 알아봤습니다.
도움이 되셨길 바라며 이만 마치겠습니다.
고생하셨습니다.🫶😊




                