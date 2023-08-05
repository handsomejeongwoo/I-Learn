# JavaScript Scope에 대해

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbnSku3%2Fbtq65Tns5FT%2FSAJfSEM822vJM9YLwK6h7K%2Fimg.jpg)

# Scope란

JavaScript 에서 Scope란 변수에 접근할 수 있는 범위를 말한다.  
식별자를(변수)를 찾기위한 규칙이라고도 한다.

```js
let name = "홍길동";

const sayName = () => {
  let name = "홍길똥";
  console.log(name);
};

sayName(); // ?
console.log(name); //?
```

위 코드를 보면 name이 2번 선언되었는데, 각각 콘솔에 어떠한 값이 나올까?

위 코드에서 전역에 선언된 변수 name는 어디에든 참조할 수 있다. 하지만 함수 foo 내에서 선어도니 변수 name는 함수 foo 내부에서만 참조할 수 있고, 외부에서는 참조할 수 없다.
이러한 규칙을 스코프 라고 한다.

# JavaScript Scope의 특징

- 블록레벨 스코프
- 함수레벨 스코프
- 렉시컬 스코프
- 동적 스코프

! 자바스크립트는 함수레벨 스코프를 따른다. !

# 블록레벨 스코프

코드블록 ({}) 내에서만 참조 가능한 범위를 말한다.

```js
const test = () => {
  if (1) {
    let i = 9;
    console.log(i); //9
  }
  console.log(i); // Uncaught ReferenceError: i is not defined
};
```

위 코드처럼 if문 안에서 선언한 i는 if문 코드 블록 내에서만 참조 가능하다.  
참고로 var를 쓰면 if문 코드 블록 밖에서도 참조가 가능하다.

# 함수레벨 스코프

함수 코드 블록 내에서만 참조 가능한 범위를 말한다.

```js
let y = 0;
{
  let y = 1;
  console.log(y); // 1
}
console.log(y); // 0
```

# 렉시컬 스코프

Scope의 또다른 특징으로, 상위 스코프를 결정하는 방법이 있다.

- 동적 스코프

  - Dynamic Scope
  - 함수를 어디서 호출 하였는지에 따라 상위 스코프를 결정

- 렉시컬 스코프
  - Lexical/Static scope
  - 함수를 어디서 선언 하였는지에 따라 상위 스코프 결정
  - JavaScript 및 대부분의 프로그래밍 언어에서 사용하는 방법

자바스크립트는 렉시컬 스코프를 따르므로 함수를 선언한 시점에서 상위 스코프가 결정된다.
함수를 어디에서 호출하였는지는 스코프 결정에 아무런 의미를 주지 않는다.

```js
let x = 1;

function one() {
  let x = 10;
  two();
}

function two() {
  console.log(x);
}

foo(); // ?
```

위 예제의 함수 two는 전역에 선언되었다.  
따라서 함수 one을 실행하면 1이 출력된다.

# 스코프 종류

- 전역 스코프

  - Global scope
  - 코드 어디에서든지 참조가능

- 지역 스코프
  - Local scope / Function-level scope
  - 함수 코드 블록이 만든, 변수 관점에서 스코프를 구분하여 다음과 같이 나눌수 있다.

# 전역 스코프

전역에 변수를 선언하면 이 변수는 어디서든지 참조할 수 있는 전역 스코프를 갖는 변수가 된다.

```js
var global = "global";

function foo() {
  var local = "local";
  console.log(global);
  console.log(local);
}
foo();

console.log(global);
console.log(local); // Uncaught ReferenceError: local is not defined
```

# 지역 스코프 지역 스코프

Local Scope.
함수 레벨 스코프(Function-level Scope) 라고 할 수 있다.

함수 내에서 선언된 매개변수와 변수는 함수 외부에서는 유효하지 않다.

```js
let a = 10; // 전역변수

(function () {
  let b = 20; // 지역변수
})();

console.log(a); // 10
console.log(b); // "b" is not defined. b는 지역 변수이다.
```
