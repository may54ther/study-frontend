# 비동기 프로그래밍

## AJAX

> - 페이지를 새로고침하지 않고 일부 화면의 내용을 갱신하기 위해 비동기로 XMLHttpRequest 객체를 이용해 XML이나 JSON 형식으로 서버와 통신하는 방식

## Promise

> - 자바스크립트 비동기 처리에 사용되는 객체, 콜백지옥을 해결할 수 있음
> - 상태(Stsate)
>   - Pending (대기) : 비동기 처리 로직이 아직 완료되지 않은 상태

```
new Promise(function (resolve, reject) { // … });
```

> - Fulfilled (이행) : 비동기 처리가 완료되어 프로미스가 결과 값을 반환해준 상태

```
new Promise(function (resolve, reject) { resolve() });
```

> - Rejected (실패) : 비동기 처리가 실패하거나 오류가 발생한 상태

```
new Promise(function (resolve, reject) { reject() });
```

## Promise vs Callback

## Async, Await
