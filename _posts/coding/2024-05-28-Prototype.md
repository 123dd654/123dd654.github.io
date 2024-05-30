---
layout: post
title: Prototype
date: 2024-05-28 10:29 +0900
description: Prototype
image: https://github.com/123dd654/123dd654.github.io/assets/161431124/797022c7-af81-4acd-aa89-4a8e05b9196d
category: coding
tags: Prototype
published: true
sitemap: true
---

안녕하세요!
오늘은 프로토타입에 대해 말씀드리겠습니다 🍞

### 프로토타입이란?
* 프로토타입은 자바스크립트에서 클래스 대신 존재하는 개념입니다.
자바스크립트는 클래스 기반 언어가 아닌 프로토타입 기반 언어로,객체 지향 프로그래밍을 위해 프로토타입을 사용합니다.
이는 객체가 다른 객체를 상속하여 속성과 메서드를 공유할 수 있도록 합니다.

### 프로토타입의 개념 
자바스크립트에서 모든 객체는 프로토타입을 가지며,
이 프로토타입은 다른 객체의 속성과 메서드를 상속할 수 있게 해줍니다.
객체는 자신의 프로토타입 객체를 참조하여 속성이나 메서드를 찾습니다.
이때 프로토타입 체인을 통해 상속된 속성과 메서드에 접근할 수 있습니다.

✨프로토타입 사용 예시✨
다음 예시를 통해 프로토타입의 개념을 더 쉽게 이해할 수 있습니다.

* 객체 생성 및 프로토타입 상속

> 아래 예시에서 Person 생성자 함수는 새로운 객체를 생성할 때 사용됩니다.
Person.prototype 객체에 greet 메서드를 추가하여, 생성된 모든 객체가 이 메서드를 상속받아 사용할 수 있게 합니다.

````javascript
// 생성자 함수
function Person(name, age) {
    this.name = name;
    this.age = age;
}

// 프로토타입에 메서드 추가
Person.prototype.greet = function() {
    console.log("Hello, my name is " + this.name);
};

// 새로운 객체 생성
let person1 = new Person("Alice", 30);
let person2 = new Person("Bob", 25);

// 프로토타입 메서드 호출
person1.greet(); // "Hello, my name is Alice"
person2.greet(); // "Hello, my name is Bob"
````

* 프로토타입 체인
자바스크립트 객체는 프로토타입 체인을 통해 다른 객체의 속성과 메서드를 상속받습니다.
객체가 특정 속성이나 메서드를 찾지 못하면, 프로토타입 체인을 따라 상위 객체에서 이를 찾습니다.

````javascript
let animal = {
    eats: true
};

let rabbit = {
    jumps: true
};

// rabbit의 프로토타입을 animal로 설정
rabbit.__proto__ = animal;

console.log(rabbit.eats); // true (animal로부터 상속됨)
console.log(rabbit.jumps); // true (rabbit 자신의 속성)
````

* 클래스 문법과 프로토타입
ES6부터 자바스크립트는 클래스 문법을 도입하여 프로토타입 기반 상속을 더 쉽게 사용할 수 있게 했습니다.
그러나 클래스 문법 역시 내부적으로는 프로토타입을 기반으로 동작합니다.
아래 예시에서 클래스 문법을 사용했지만, 내부적으로는 프로토타입을 기반으로 greet 메서드를 상속하고 있습니다.


````javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    greet() {
        console.log("Hello, my name is " + this.name);
    }
}

let person1 = new Person("Alice", 30);
person1.greet(); // "Hello, my name is Alice"
````
-----------------------------------------------------

<br />
<br />

프로토타입은 자바스크립트에서 클래스 대신 객체 지향 프로그래밍을 가능하게 하는 중요한 개념입니다.
객체는 프로토타입을 통해 다른 객체의 속성과 메서드를 상속받아 사용할 수 있습니다.
이를 통해 코드의 재사용성을 높이고, 객체 간의 관계를 명확하게 정의할 수 있습니다.

오늘은 프로토타입에 대해 알아보았습니다 유익한 시간 되셨길 바라며 이만 마치겠습니다 🤓