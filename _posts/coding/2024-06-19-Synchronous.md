---
layout: post
title: 동기와 비동기 프로그래밍 이해하기
date: 2024-06-19 10:29 +0900
description: 동기와 비동기 프로그래밍 이해하기
image: https://github.com/123dd654/123dd654.github.io/assets/161431124/be6ff23b-f5fd-4450-8a96-bc7d203324b4
category: 2024년도 공부내용
tags: Programming, Synchronous, Asynchronous
published: true
sitemap: true
---

## 동기와 비동기 프로그래밍 이해하기

프로그래밍에서 동기(Synchronous)와 비동기(Asynchronous)의 개념은 매우 중요합니다. 이 두 가지 개념은 코드가 실행되는 방식과 작업이 처리되는 순서를 결정짓는 중요한 요소입니다. 이번 글에서는 동기와 비동기 프로그래밍의 차이점과 각각의 장단점에 대해 자세히 알아보겠습니다.

### 동기 프로그래밍이란?

동기 프로그래밍은 요청과 결과가 동시에 일어난다는 약속을 기반으로 합니다. 즉, 하나의 작업이 완료된 후에야 다음 작업을 수행할 수 있습니다.

#### 동기 프로그래밍의 예시

```javascript
function fetchData() {
  const result = requestDataFromServer(); // 서버에서 데이터 요청
  console.log(result); // 요청한 데이터 출력
}

fetchData();
```

위 예시에서 `requestDataFromServer` 함수가 데이터를 반환하기 전까지 `fetchData` 함수는 다음 줄로 넘어가지 않습니다.

### 동기 프로그래밍의 장단점

#### 장점

1. 설계가 간단하고 직관적: 코드가 순차적으로 실행되기 때문에 이해하고 디버깅하기 쉽습니다.
2. 예측 가능한 실행 흐름: 코드가 작성된 순서대로 실행되므로, 실행 흐름을 예측하기 쉽습니다.

#### 단점

1. 대기 시간: 하나의 작업이 완료될 때까지 다음 작업을 수행하지 않기 때문에 대기 시간이 발생할 수 있습니다.
2. 비효율적인 자원 사용: CPU와 같은 시스템 자원이 비효율적으로 사용될 수 있습니다. 예를 들어, 네트워크 요청 대기 시간 동안 CPU는 유휴 상태가 됩니다.

### 비동기 프로그래밍이란?

비동기 프로그래밍은 요청과 결과가 동시에 일어나지 않을 거라는 약속을 기반으로 합니다. 즉, 하나의 작업이 시작된 후에도 다음 작업을 바로 수행할 수 있습니다.

#### 비동기 프로그래밍의 예시

```javascript
function fetchData() {
  requestDataFromServerAsync((result) => {
    // 서버에서 비동기적으로 데이터 요청
    console.log(result); // 요청한 데이터 출력
  });
  console.log("Next task"); // 다음 작업 수행
}

fetchData();
```

위 예시에서 `requestDataFromServerAsync` 함수는 비동기적으로 데이터를 요청하고, 콜백 함수를 통해 데이터를 반환합니다. 따라서 `console.log('Next task')`는 데이터 요청이 완료되기 전에 실행됩니다.

### 비동기 프로그래밍의 장단점

#### 장점

1. 효율적인 자원 사용: 작업이 완료될 때까지 대기하지 않고 다음 작업을 수행할 수 있어 시스템 자원을 효율적으로 사용할 수 있습니다.
2. 반응성 향상: 사용자 인터페이스가 더 반응성 있게 동작합니다. 예를 들어, 네트워크 요청 중에도 사용자 입력을 처리할 수 있습니다.

#### 단점

1. 복잡한 설계: 비동기 코드는 동기 코드보다 복잡합니다. 콜백 지옥(Callback Hell)이나 복잡한 상태 관리를 유발할 수 있습니다.
2. 디버깅 어려움: 비동기 코드의 실행 흐름을 예측하기 어려워 디버깅이 어렵습니다.

### 동기와 비동기의 활용 사례

#### 동기 프로그래밍 활용 사례

- 파일 읽기/쓰기: 간단한 파일 읽기/쓰기 작업에서는 동기 프로그래밍이 적합합니다. 코드가 순차적으로 실행되기 때문에 파일을 읽은 후 바로 처리가 가능합니다.

```javascript
const fs = require("fs");
const data = fs.readFileSync("/path/to/file");
console.log(data);
```

- 단순한 계산 작업: 복잡한 비동기 처리 없이 순차적으로 실행되는 계산 작업에서도 동기 프로그래밍이 유용합니다.

#### 비동기 프로그래밍 활용 사례

- 네트워크 요청: 네트워크 요청은 응답 시간이 불확실하기 때문에 비동기 프로그래밍이 적합합니다. 네트워크 요청 중에도 다른 작업을 수행할 수 있습니다.

```javascript
fetch("/api/data")
  .then((response) => response.json())
  .then((data) => console.log(data));
```

- 타이머: 일정 시간이 지난 후에 실행되어야 하는 작업에서는 비동기 프로그래밍이 필요합니다.

```javascript
setTimeout(() => {
  console.log("Time out!");
}, 1000);
```

### 동기와 비동기의 혼합 사용

현실적인 애플리케이션에서는 동기와 비동기를 혼합하여 사용하는 경우가 많습니다. 예를 들어, 비동기적으로 데이터를 가져온 후 동기적으로 데이터를 처리하는 경우가 있습니다.

```javascript
function processData() {
  fetchDataFromServer((data) => {
    // 비동기 데이터 요청
    const processedData = processDataSync(data); // 동기 데이터 처리
    console.log(processedData);
  });
}
```

### 결론

동기와 비동기 프로그래밍은 각각의 장단점을 가지고 있으며, 상황에 맞게 적절히 사용해야 합니다. 동기 프로그래밍은 설계가 간단하고 직관적이지만, 대기 시간이 발생할 수 있습니다. 반면, 비동기 프로그래밍은 자원을 효율적으로 사용할 수 있지만, 설계가 복잡하고 디버깅이 어렵습니다.

이번 글에서는 동기와 비동기 프로그래밍의 개념, 장단점, 활용 사례에 대해 살펴보았습니다. 앞으로의 개발에서 이 두 가지 개념을 잘 이해하고 적절히 활용하여 효율적이고 반응성이 뛰어난 애플리케이션을 개발해 보세요!
