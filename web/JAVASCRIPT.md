# Javascript

## null과 undefined

> - undefined은 변수가 선언되었지만 값이 할당 되지 않은 상태 <br>
> - null은 명시적으로 값이 비어있음을 알려줌 <br>
> - 일치연산자(===)를 이용하여 둘을 비교할 수 있다.

## 원시 값과 객체

> - 원시 값에는 String, Number, Boolean, Symbol, null, undefined가 있으며, 원시 값은 값 자체를 전달 <br>
> - 객체는 객체가 참조하고 있는 주소를 전달

## 동등연산자(==)와 일치연산자(===)의 차이

> - 동등연산자(==) : 타입 변환을 한 후에 비교
> - 일치연산자(===) : 타입 변환을 하지 않고 비교

```
let a = "13";
let b = 13;

console.log(a == b, a === b);  //true, false
```

## javascript의 this

## 호이스팅 (Hoisting)

## 이터레이터 (Iterator)

## 제너레이터 (Generator)

## 클로저 (Closure)

## 프로토타임 (Prototype)

## 이벤트 버블링과 캡처링

> - 캡처링은 가장 부모태그인 body태그에서 부터 이벤트가 일어난 요소까지 거슬러 내려가는 것, <br>
> - 버블링은 이벤트가 일어난 요소부터 가장 부모태그인 body태그까지 거슬러 올러가는 것

## delete 연산자

> - 객체의 속성을 제거하는 연산자

## 메소드 체이닝 패턴

## Call, Apply, Bind

> ### Call
>
> - call(thisArg, arg1, arg2, ...)

```
const john = { name: "John" };
const lisa = { name: "Lisa", age: 28 };

function greet() {
  return `Hello, ${this.name}!`;
}
function update(age) {
  this.age = age;
}

greet.call(john); // Hello, John!
update.call(lisa, 31); // {name: "Lisa", age: 31}
```

> ### Apply
>
> - apply(thisArg, [argsArray])
> - call과 같지만 배열형태로 인자를 넘긴다는 차이가 있음

```
const lisa = { name: "Lisa", age: 28, gender: "female" };
const numbers = [31, -3, 10, 1, 5, 7, 13];
const newLisaData = [29, "Programmer"];

function greet() {
  retrun`Hello, ${this.name}!`;
}

function update(age, job) {
  this.age = age;
  this.job = job;
}

update.apply(lisa, [31, "Professor"]); // {name: "Lisa", age: 31, gender: "female", job: "Professor"}
update.apply(lisa, ...newLisaData); // {name: "Lisa", age: 29, gender: "female", job: "Programmer"}
Math.min.apply(null, numbers); // -3
```

> ### Bind
>
> - bind(thisArg[, arg1[, arg2[, ...]]])
> - bind는 함수의 this 값을 영구히 변경할 수 있음
> - bind한 함수는 apply, call로 thisArg를 다른 객체로 명시해도 bind시 thisArg로 넘긴 객체로 실행됨

```
const john = { name: "john" };
const lisa = { name: "lisa" };

function update(birthYear, job) {
this.birthYear = birthYear;
this.job = job;
}

var updateLisa = update.bind(john);

updateLisa.call(john, 1904, "Doctor"); // {name: "john", birthYear: 1904, job: "Doctor"} {name: "lisa"}
updateLisa.call(lisa, 1274, "Programmer"); // {name: "john", birthYear: 1274, occupation: "Programmer"} {name: "lisa"}
```

## map, filter, reduce
