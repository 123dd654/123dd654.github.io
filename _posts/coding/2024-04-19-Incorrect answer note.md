---
layout: post
title: 자바스크립트 오답노트 
date: 2024-04-19 14:54 +0900
description: 자바스크립트
image: https://github.com/123dd654/123dd654.github.io/assets/161431124/25a51da0-a28a-4a5e-a9b9-9127cd53349c
category: 오답노트
tags: 자바스크립트 오답노트
published: true
sitemap: true
---


## 자바스크립트 문제 및 문제풀이

### 01. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    (function(){
        console.log("함수가 실행되었습니다.");
    })();
}   
````

이 코드는 JavaScript에서 Immediately Invoked Function Expression (IIFE)을 사용하여 함수를 정의하고 즉시 실행하는 방법을 보여줍니다.
이 코드는 함수를 선언하고 그 즉시 실행되는 형태로 작성되어 있습니다.

이 코드는 다음과 같은 일을 합니다:

함수를 선언합니다.
이 함수를 즉시 실행합니다.
실행 시 함수 내부에 있는 내용을 콘솔에 출력합니다.
여기서 (function(){ ... })(); 부분이 IIFE를 나타내며, 이는 함수를 선언하고 즉시 실행하는 구문입니다.
이 구문 안에 있는 함수는 즉시 실행되므로 별도의 호출 없이 실행됩니다.

이 코드를 실행하면 콘솔에 "함수가 실행되었습니다."라는 메시지가 출력될 것입니다. 이 코드를 어떻게 활용하고자 하는지에 따라서 다양한 용도로 활용할 수 있습니다.


### 02. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    function func(str = "함수가 실행되었습니다."){
        document.write(str);
    }
    func();
}   
````

이 코드는 JavaScript에서 함수를 정의하고 호출하는 예제입니다.
함수의 이름은 func이며, 하나의 매개변수 str을 가지고 있습니다.
이 함수는 기본값으로 "함수가 실행되었습니다." 문자열을 가지고 있습니다.

그리고 함수 내부에서는 document.write()를 사용하여 매개변수 str에 해당하는 내용을 문서에 출력합니다.
여기서 함수를 호출할 때 인자를 전달하지 않았으므로, 기본값 "함수가 실행되었습니다."가 출력됩니다.

간단한 풀이는 다음과 같습니다:

함수 func를 정의하고 매개변수 str에 기본값을 설정합니다.
함수 내에서는 document.write()를 사용하여 str을 문서에 출력합니다.
함수를 호출하면서 아무런 인자를 전달하지 않았으므로, 기본값인 "함수가 실행되었습니다."가 출력됩니다.

### 03. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    let sum = 0;
    for(var i=1; i<=10; i++) {
        sum += i;
    };
    document.write(sum);
}
````

이 코드는 JavaScript로 작성된 조각입니다. 여기서는 변수 sum을 초기화하고,
1부터 10까지의 숫자를 더하는 루프를 실행합니다. 그런 다음 결과를 문서에 출력합니다.
변수 sum은 초기값 0으로 설정되며, for 루프를 통해 변수 i를 1부터 10까지 증가시키면서 sum에 더해집니다.

따라서 sum에는 1부터 10까지의 모든 숫자를 더한 값이 저장되고, 이 값은 문서에 출력됩니다.
1부터 10까지의 숫자를 모두 더한 55가 나옵니다.


### 04. 다음의 결괏값을 보고 빈칸을 작성하시오.

````javascript
{
    const obj = {
        a: 100,
        b: 200,
        c: "javascript"
    }
    const { a, b, c } = _______;

    document.write(a);
    document.write(b);
    document.write(c);

    //100
    //200
    //javascript
}
````

주어진 코드에서는 객체 디스트럭처링을 사용하여 객체 obj의 속성을 추출하려고 합니다.
빈칸에는 디스트럭처링할 대상 객체를 넣어주어야 합니다.
따라서, 빈칸에는 obj를 넣어야 합니다. 
위 코드에서는 obj 객체의 속성들을 a, b, c라는 변수에 디스트럭처링하여 할당한 후, 각 변수를 document.write()를 사용하여 출력하고 있습니다.


### 05. 다음을 보고 결괏값을 작성하시오!

````javascript
{       
    for(var i=1; i<=1; i++){
        document.write(i);
        for(var j=1; j<=5; j++){
            document.write(j);
        }
    }                
}
````

주어진 코드는 중첩된 for 루프를 사용하여 숫자를 출력하는 것으로 보입니다.
첫 번째 for 루프에서는 변수 i를 1부터 1까지 반복하고, 두 번째 for 루프에서는 변수 j를 1부터 5까지 반복합니다.

내부 for 루프가 완료되기 전까지는 외부 for 루프가 반복되지 않습니다. 따라서 외부 for 루프는 한 번만 반복됩니다.
외부 루프에서 i가 1일 때 내부 루프가 실행되며, 내부 루프에서는 1부터 5까지의 숫자가 출력됩니다. 그 결과로 112345가 출력됩니다.


### 06. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    const num = [100, 200, 300, 400, 500];

    for(let i=0; i<num.length; i++){
        document.write(_______);
    }

    //100 200 300 400 500
}
````

주어진 코드에서는 배열 num에 있는 요소들을 반복하여 출력하려고 합니다. 
빈칸에는 배열의 각 요소를 가리키는 변수를 넣어주어야 합니다.

따라서, 빈칸에는 배열의 각 요소를 가리키는 변수 num[i]를 넣어주어야 합니다. 

위 코드에서는 num 배열의 각 요소를 반복하여 document.write() 함수를 사용하여 출력하고 있습니다.
출력 결과는 100 200 300 400 500가 됩니다.


### 07. 다음을 보고 리턴값을 생략하여 한줄로 표현하시오!

````javascript
{
    const func = str => {
            return str;
    }  
}
````

주어진 코드에서 함수 func는 매개변수 str을 받아서 그대로 반환하는 기능을 가지고 있습니다.
이러한 경우에는 함수 바디 내의 리턴 구문을 생략하고 한 줄로 간단히 표현할 수 있습니다.

const func = str => str;

여기서 화살표 함수를 사용하여 매개변수 str을 받고 그대로 반환하고 있습니다. 이렇게 간단한 경우에는 중괄호와 리턴 구문을 생략할 수 있습니다.


### 08. 다음의 결괏값을 보고 빈 칸을 채우시오.

````javascript
{
    const num = [100, 200, 300, 400, 500];

    for(let index of _____ ){
        document.write(index);
    }

    //결과값
    //100 200 300 400 500
}
````

주어진 코드에서는 배열 num의 각 요소를 반복하여 출력하려고 합니다.
이때는 배열의 인덱스를 사용하는 것이 아니라, 배열의 각 요소를 직접 사용해야 합니다.

따라서, 빈칸에는 배열 num을 넣어주어야 합니다. 

위 코드에서는 num 배열의 각 요소를 반복하여 document.write() 함수를 사용하여 출력하고 있습니다.
출력 결과는 100 200 300 400 500가 됩니다.


### 09. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    function func(){
            let i = 5, j = 4, k = 1, l, m;
            l = i > 5 || j != 0;   // true 또는 false
            m = j <= 4 && k < 1;   // true 또는 false

            document.write(l);     // 변수 l의 값 출력
            document.write(m);     // 변수 m의 값 출력
    }
    func();                        // 함수 호출
}
````

주어진 코드에서는 함수 func()가 정의되어 있습니다.
이 함수는 세 개의 변수 i, j, k를 초기화하고, 그 값을 사용하여 두 개의 변수 l과 m을 초기화합니다.
그런 다음에는 이 변수들을 사용하여 document.write()를 호출하여 결과를 출력합니다.

변수 l은 i > 5 또는 j != 0 라는 조건을 가지는 논리 연산자 ||를 사용하여 초기화됩니다.
변수 m은 j <= 4와 k < 1 라는 조건을 가지는 논리 연산자 &&를 사용하여 초기화됩니다.

따라서, l과 m에는 각각 true 또는 false가 할당될 것입니다.
그리고 이 값을 document.write()를 사용하여 출력합니다.

결과는 변수 l과 m의 값에 따라 다를 것입니다.
결과가 true이면 1이 출력되고, false이면 0이 출력될 것입니다.


### 10. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    const arr = [100, 200, 300, 400, 500];
    const text = arr.push(600);

    document.write(arr);      
}
````

주어진 코드에서는 배열 arr에 새로운 요소 600을 추가하고,
이 작업을 수행한 후의 배열의 길이를 반환합니다. 그리고 이 반환된 값을 text 변수에 할당하고 있습니다.
그러나 arr.push(600) 메서드는 배열에 요소를 추가할 뿐만 아니라 배열의 길이를 반환하기 때문에,
text 변수에는 배열의 길이가 할당됩니다. 따라서 text 변수에는 6이 할당됩니다.

그리고 마지막으로 document.write(arr)를 호출하여 배열 arr의 내용을 출력하고 있습니다.
결과는 배열 arr의 내용이 출력될 것입니다. 즉, [100, 200, 300, 400, 500, 600]가 출력될 것입니다.


### 11. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    const obj = {
        a: 100, 
        b: 200
    };

    for(let key in obj) { 
        console.log(key);
    } 
}
````

주어진 코드는 객체 obj에 대한 for...in 루프를 사용하여 객체의 속성을 반복적으로 순회하고 있습니다.
이 코드는 객체의 각 속성에 대해 키(key)를 출력하는 것입니다.

따라서 코드의 실행 결과는 객체 obj의 각 속성 이름인 'a'와 'b'가 각각 콘솔에 출력될 것입니다.


### 12. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    let num = 0;

    while(false){
        num++;
        if( num == 3 ){
            continue;
        }
        if( num > 6 ){
            break;
        }
    }
    console.log(num);
}
````

주어진 코드는 while 루프가 false 조건으로 시작하므로 루프가 실행되지 않습니다.
따라서 루프 내부의 코드는 실행되지 않고 console.log(num)이 실행될 때 num의 값은 변하지 않습니다.
루프 내부의 continue문은 실행되지 않고, break문 역시 실행되지 않으므로 num은 초기값인 0으로 유지됩니다.

결과적으로 console.log(num)에서는 num의 초기값인 0이 출력됩니다.


### 13. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    let data = [70, 80, 75, 60, 90];
    let best = 0;
    let score = 50;

    for(let i=0; i<data.length; i++){
        if(data[i]>80) {
            best++;
        }
        if(score > data[i]) {
            score = data[i];
        }
    }

    console.log(best, score);      
}
````


주어진 코드는 배열 data의 각 요소를 반복하면서 두 가지를 수행합니다:

1. 배열 data의 각 요소가 80보다 큰지 확인하여 그렇다면 best 변수를 증가시킵니다.
2. 배열 data의 요소와 변수 score의 값을 비교하여 작은 값을 score 변수에 할당합니다.
이렇게 반복을 마친 후에는 best 변수에는 80보다 큰 요소의 수가 저장되고, score 변수에는 data 배열의 요소 중 가장 작은 값이 저장됩니다.
위 코드를 실행하면 콘솔에 best 변수의 값과 score 변수의 값이 출력됩니다. 이 값은 각각 80보다 큰 요소의 개수와 배열 data에서 가장 작은 값입니다.


### 14. 다음의 보기를 보고 조건 값에 따른 결과값이 false가 나오는 경우를 작성하시오.

````javascript
{
    function func(num1, num2){
        if(num1 > num2) return num1
        else return num2
    }
    console.log(func(10, 23) + func(40, 50))
}
````

주어진 코드에서는 func라는 함수를 정의하고 있습니다.
이 함수는 두 개의 매개변수 num1과 num2를 받아서, 둘 중 큰 값을 반환합니다. 그런 다음 console.log()를 사용하여 두 번의 func 호출의 결과를 출력합니다.
이 코드에서 func 함수의 조건은 num1 > num2입니다. 따라서 조건 값이 false가 되는 경우를 찾아보겠습니다.

예를 들어, func(10, 23)을 호출할 때 num1은 10이고 num2는 23입니다.
이때는 num1 > num2가 false가 되므로 두 번째 return문이 실행되어 23이 반환됩니다.
또한, func(40, 50)을 호출할 때는 num1이 40이고 num2가 50입니다. 마찬가지로 조건은 false가 되므로 두 번째 return문이 실행되어 50이 반환됩니다.

따라서 console.log(func(10, 23) + func(40, 50))의 결과는 23 + 50 = 73이 됩니다.


### 15. 다음의 결괏값을 보고 빈칸을 채우시오.

````javascript
{
    function func(){
        document.write("함수2가 실행되었습니다.");
    }
    function callback(str){
        document.write("함수1가 실행되었습니다.");
        _______();
    }
    callback(func);

    //함수1가 실행되었습니다.
    //함수2가 실행되었습니다.
}
````

주어진 코드에서는 두 개의 함수 func()와 callback(str)가 정의되어 있습니다.
callback 함수는 매개변수로 문자열을 받으며, 이 문자열을 출력하고, 그 후에는 콜백 함수를 실행하는 기능을 가지고 있습니다.

callback 함수를 호출할 때 func 함수를 인자로 전달했습니다.
이 때 func 함수는 콜백 함수의 인자로 전달됩니다. 그러면 빈칸에는 콜백 함수의 인자인 str을 호출하는 코드가 들어가야 합니다.

따라서, 빈칸에는 str()를 넣어주어야 합니다.
callback(func)의 결과로 "함수1가 실행되었습니다."가 출력되고, 그 후 func()이 실행되어 "함수2가 실행되었습니다."가 출력됩니다.


### 16. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    function func(num, name, word){
        this.num = num;
        this.name = name;
        this.word = word;
    }
    
    func.prototype = {
        result1 : function(){
            console.log(this.num + ". " + this.name + "가 "+ this.word + "되었습니다.");
        },
        result2 : function(){
            console.log(this.num + ". " + this.name + "가 "+ this.word + "되었습니다.");
        },
        result3 : function(){
            console.log(this.num + ". " + this.name + "가 "+ this.word + "되었습니다.");
        }
    }
    
    const info1 = new func("1", "함수", "실행");
    const info2 = new func("2", "자바스크립트", "실행");
    const info3 = new func("3", "제이쿼리", "실행");
    
    info1.result1();
    info2.result2();
}
````

주어진 코드는 생성자 함수 func를 사용하여 객체를 생성하고,
이를 프로토타입을 통해 메서드를 공유하는 방식으로 객체의 동작을 정의하고 있습니다.
여기서 생성자 함수 func는 세 개의 매개변수 num, name, word를 받아서 객체의 속성으로 할당합니다.
그리고 func의 프로토타입에는 세 개의 메서드 result1, result2, result3이 정의되어 있습니다.
이들은 객체의 속성을 사용하여 결과를 콘솔에 출력합니다.
마지막으로 info1, info2, info3라는 세 개의 객체를 생성하고, 각 객체의 메서드를 호출하여 실행합니다.


### 17. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    function func(num, name, word){
        this.num = num;
        this.name = name;
        this.word = word;
    }

    func.prototype.result = function(){
        console.log(this.num + ". " + this.name + "가 "+ this.word + "되었습니다.");
    }

    const info1 = new func("1", "함수", "실행");
    const info2 = new func("2", "자바스크립트", "실행");
    const info3 = new func("3", "제이쿼리", "실행");

    info1.result();
}
````

주어진 코드에서는 생성자 함수 func를 사용하여 객체를 생성하고,
이를 프로토타입을 통해 메서드를 공유하는 방식으로 객체의 동작을 정의하고 있습니다.
여기서 생성자 함수 func는 세 개의 매개변수 num, name, word를 받아서 객체의 속성으로 할당합니다.
그리고 func의 프로토타입에는 result 메서드가 정의되어 있습니다.이 메서드는 객체의 속성을 사용하여 결과를 콘솔에 출력합니다.
마지막으로 info1, info2, info3라는 세 개의 객체를 생성하고, 각 객체의 result 메서드를 호출하여 실행합니다.


### 18. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    function func(index){
        console.log("함수가 실행되었습니다." + index);
    }
    function callback(num){
        for( let i=1; i<=1; i++){
            num(i);
        }
    }
    callback(func);
}
````

주어진 코드에서는 func 함수와 callback 함수가 정의되어 있습니다.

func(index) 함수는 매개변수 index를 받아서 "함수가 실행되었습니다."와 index를 출력하는 기능을 가지고 있습니다.
callback(num) 함수는 매개변수 num으로 함수를 받습니다. 이 함수는 1부터 1까지의 숫자를 반복하면서 매개변수로 받은 함수를 호출합니다.
마지막으로 callback(func)를 호출하여 callback 함수에 func 함수를 전달합니다.

따라서 코드의 실행 결과는 func 함수가 callback 함수 내에서 한 번 호출되는 것입니다. 이때 매개변수 index는 1이 됩니다.


### 19. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    let num = 1;

    while(num<=10){
            document.write(num);
            num++;
    }
}
````

주어진 코드는 while 루프를 사용하여 변수 num이 1부터 10까지의 값을 출력하는 것입니다.
루프는 변수 num이 10 이하일 때까지 실행됩니다.
각 반복에서는 document.write()를 사용하여 num 값을 출력하고, 그 다음에는 num을 1씩 증가시킵니다.

따라서 코드의 실행 결과는 1부터 10까지의 숫자가 차례대로 출력됩니다.


### 20. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    function func(){
        let i = 10, j = 10, k = 30;
        i /= j;
        j -= i;
        k %= j;

        console.log(i);
        console.log(j);
        console.log(k);
    }
    func();
}
````

주어진 함수 func()는 세 개의 변수 i, j, k를 선언하고 있습니다.
이후에는 각 변수에 대한 연산을 수행하고 그 결과를 콘솔에 출력합니다.
변수 i는 초기값인 10을 변수 j로 나눈 값을 할당하고, 변수 j에서 i 값을 뺀 값을 다시 변수 j에 할당합니다. 
마지막으로 변수 k는 변수 k를 변수 j로 나눈 나머지 값을 할당합니다.

따라서 각 변수의 값은 다음과 같습니다:

변수 i: 10을 10으로 나눈 값이므로 1이 됩니다.
변수 j: 초기값인 10에서 변수 i의 값인 1을 뺀 값이므로 9가 됩니다.
변수 k: 초기값인 30에서 변수 j의 값인 9로 나눈 나머지 값이므로 3이 됩니다.

따라서 1,9,3이 출력됩니다.


### 21. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    for( let i=1; i<=10; i+=2 ){
            document.write(i);
    }
}
````

주어진 코드는 for 루프를 사용하여 변수 i가 1부터 10까지 2씩 증가하면서 반복됩니다.
각 반복에서는 document.write()를 사용하여 i의 값을 출력합니다.

즉, i가 1에서 시작하여 2씩 증가하면서 10까지 반복됩니다. 따라서 출력 결과는 1, 3, 5, 7, 9가 됩니다.


### 22. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    for(let i=1; i<10; i++){
            if( i == 5 ){
                    break;
            }
            document.write(i);
    }
}
````

주어진 코드는 for 루프를 사용하여 변수 i가 1부터 9까지 반복됩니다.
각 반복에서는 i가 5일 때 break문을 통해 루프를 중단하고, 그 외에는 document.write()를 사용하여 i의 값을 출력합니다.

즉, i가 1부터 시작하여 5가 될 때까지 반복되고, 그 후에는 break문을 만나서 루프가 중단됩니다.
따라서 출력 결과는 1부터 4까지의 숫자입니다.


### 23. 다음을 보고 결괏값을 작성하시오!

````javascript
{
    for(let i=1; i<10; i++){
            if( i == 5 ){
                    continue;
            }
            document.write(i);
    }
}
````

주어진 코드는 for 루프를 사용하여 변수 i가 1부터 9까지 반복됩니다.
각 반복에서는 i가 5일 때 continue문을 만나서 해당 반복을 건너뛰고,
그 외에는 document.write()를 사용하여 i의 값을 출력합니다.

즉, i가 1부터 시작하여 5가 될 때까지 출력되고,
continue문에 의해 5는 건너뛰어지므로 출력 결과는 1부터 4까지의 숫자와 6부터 9까지의 숫자입니다.


### 24. 다음의 결과를 보고 빈칸을 작성하시오!

````javascript
{
    const obj = {
            a: 100,
            b: 200,
            c:"javascript"
    }
    
    console.log(_______________________);       // true
    console.log(_______________________);       // true
    console.log(_______________________);       // true
}
````

주어진 코드에서는 객체 obj에 대한 조건을 확인하고 있습니다. 객체의 속성에 대한 유무를 확인하는 방법은 다양합니다.
주어진 문제에서는 객체의 속성 존재 여부를 확인하는 hasOwnProperty 메서드를 사용하여 해결할 수 있습니다.
이 메서드는 객체가 지정된 속성을 포함하고 있는지 여부를 나타내는 부울 값을 반환합니다.

따라서, 빈칸에는 다음과 같이 hasOwnProperty 메서드를 사용하여 각 속성에 대한 존재 여부를 확인할 수 있습니다:

````javascript
console.log(obj.hasOwnProperty('a')); // true
console.log(obj.hasOwnProperty('b')); // true
console.log(obj.hasOwnProperty('c')); // true
````

위 코드는 각각 속성 'a', 'b', 'c'가 객체 obj에 존재하므로 모두 true를 출력합니다.


### 25. 다음의 결과를 보고 빈칸을 작성하시오!

````javascript
{
    function solution(a, b, c){
        let answer="YES", max;
        let tot = a + b + c;

        if(a > b) max = a;
        else max = b;
        if(c > max) max = c;
        if(tot-max <= max) answer = "NO"; 
        
        return answer;
    }

    console.log(solution(13, 33, 17));
}
````

주어진 코드는 세 개의 숫자를 매개변수로 받아들여서 어떤 조건을 만족하는지 확인하고 "YES" 또는 "NO"를 반환하는 solution 함수를 정의하고 있습니다.

함수 내부에서는 먼저 "YES"를 담는 변수 answer와 총합을 저장하는 변수 tot을 선언합니다.
그리고 세 숫자 중 가장 큰 수를 찾아내기 위해 조건문을 사용하여 max 변수에 할당합니다.
이후에는 세 숫자를 합한 값에서 가장 큰 수를 뺀 값이 가장 큰 수와 같거나 작다면 "NO"를 answer에 할당합니다.
마지막으로 answer를 반환합니다.
주어진 입력이 (13, 33, 17)인 경우에는 다음과 같이 실행됩니다:

tot은 13 + 33 + 17 = 63이 됩니다.
가장 큰 수는 33입니다.
따라서 tot - max는 63 - 33 = 30이며, max는 33입니다.
조건 tot - max <= max는 30 <= 33를 의미합니다. 이 조건은 참이므로 answer에 "NO"가 할당됩니다.
"NO"가 반환됩니다.
따라서 solution(13, 33, 17)의 결과는 "NO"가 됩니다.







                