# ES6

## ES6 지원에 대한 해결방법

> - es6코드를 es5코드로 트랜스 컴파일하는 babel 사용<br>
> - HTML5나 CSS3코드를 지원하지 않는 브라우저를 위해 polyfills를 사용<br>

## Babel의 기능

> - 아직 ES6 코드를 지원하지 않는 브라우저를 위해서 ES5코드로 트랜스컴파일

## var vs let, const

> - var (function-scoped)
>   - 함수안에서 선언한 변수는 함수 밖에서 사용불가
>   - 블럭안에서 선언한 변수는 블록 밖에서 사용가능
>   - 동일한 이름의 변수를 재선언/할당 할 수 있음

> - let, const (block-scoped)
>   - 함수안에서 선언한 변수는 함수 밖에서 사용불가
>   - 블록안에서 선언한 변수는 블록 밖에서 사용불가
>   - 동일한 이름의 변수를 재선언/할당 할 수 없음(같은 영역내에서)
>   - const는 상수로 선언과 동시에 할당이 이루어지며 값의 재할당은 불가능

```
var a = "initialize-var";
let b = "initialize-let";

console.log("[초기화]", a, b);

function test() {
 var a = "function-var";
 let b = "function-let";
 console.log("[함수 안]", a, b);
}
test();

console.log("[함수 종료]", a, b);

{
 var a = "block-var";
 let b = "block-let";
 console.log("[블럭 안]", a, b);
}

console.log("[블럭 밖]", a, b);

```

```
[초기화] initialize-var initialize-let
[함수 안] function-var function-let
[함수 종료] initialize-var initialize-let
[블럭 안] block-var block-let
[블럭 밖] block-var initialize-let
```

## Class란?

## function의 스펙으로 Class를 구현할 수 있는가?
