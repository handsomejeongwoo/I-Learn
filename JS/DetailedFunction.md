# 함수

유사한 동작을 하는 코드를 중복없이 여러번 호출할수있게끔 작성하는 코드

## 함수 선언

매개변수가 없는경우

    function hiFunction() {
      alert('안녕하세요!');
    }

매개변수가 있는경우

    function plus(parameter1,parameter2){
      return parameter1 + parameter2 //ex
    }

새롭게 정의한 함수는 이름 옆에 괄호() 를 붙여서 호출
hiFunction();
plus(2,3); //5

## 지역변수

함수내에서 선언한 지역변수는 함수 안에서만 사용가능하다.

    function showAlert() {
      let message = '안녕하세요!'

      alert(message);
    }

    showAlert(); //안녕하세요!
    alert(message); //error

## 외부변수

함수 내부에서 함수 외부애있는 변수에 접근과 수정이 가능하다.  
함수 내부에 외부 변수와 동일한 이름을 가진 변수가 선언된다면, 내부변수는 외부변수를 가립니다.

    let name = '홍길동';
    let age = 39;
    let country = 'korea'

    function showAlert() {
      age = 20;
      let country = 'japan';

      alert(`Hello ${name} I'm ${age} years old I'm from ${country}`);

    }

    showAlert(); // Hello 홍길동 I'm 20 years old I'm from japan
    alert(country); // 함수는 외부변수에 접근하지 않아서 korea가 출력됩니다.

# 매개변수

매개변수를 이용하면 함수안에 임의의 데이터를 전송할수있다. 매개변수는 파라미터(parameter)라고도 불린다.

    function plus(parameter1, parameter2) {
      return parameter1 + parameter2;
    }

    plus(3, 10) //13
    plus(100, 1000) //1100

함수의 매개변수에 전달된 값을 인수(argument) 라고 부릅니다.

- 매개변수는 함수 선언 방식 괄호 사이에 있는 변수입니다.
- 인수는 함수를 호출할 때 매개변수에 전달되는 값입니다.

# 기본값

함수 호출 시 매개변수에 인수를 전달하지 않으면 그 값은 undefined가 됩니다.

showUser(name,age)라는 함수는 매개변수가 2개지만, 아래와 같이 인수를 하나만 넣어서 호출할 수 있습니다.

    function showUser(name, age) {

      alert(name + age + "세");

    }

    showUser('이정우'); // 이정우 undefined세

두 번째 매개변수는 값을 전달하지않아 undefined를 할당했기에 에러는 일어나지 않는다.

    function showUser(name, age = '18') {

      alert(name + age + "세");

    }

    showUser('이정우'); // 이정우 18세

이젠 age가 값을 전달받지 못해도 undefined가아닌 18이 age에 할당됩니다.

## 매개변 기본값을 설정할 수 있는 또다른 방법

if문이나 , 연산자(||,??)을 사용한다.

     function showUser(name) {
      //ex 1
      if (name === undefined) {
        name = "빈문자열";
        alert(name);
      }

     //ex 2
     name = name || '빈 문자열';
     alert(name);

     //ex 3
     alert(name ?? '빈문자열');

    }

## 반환값

함수를 호출했을 때 함수를 호출한 그곳에 특정 값을 반환하게 할 수 있습니다. 이때 이 특정 값을 반환 값(return value)이라고 부릅니다.

    function sum(a, b) {
      return a + b;
    }

    let result = sum(1, 2);
    alert( result ); // 3

지시자 return은 함수 내 어디서든 사용할 수 있습니다. 실행 흐름이 지시자 return을 만나면 함수 실행은 즉시 중단되고 함수를 호출한 곳에 값을 반환합니다.

- return만 명시하는 것도 가능합니다. 이런 경우는 함수가 즉시 종료됩니다.

## 함수 이름짓기

함수이름은 내 마음대로 짓는게 아닌 내 코드를 읽는사람이 함수 이름만 봐도 어떤기능을 하는 함수인지 알수있게끔 지어야 한다.

예를들어 "show"로 시작하는 함수는 대개 무언가를 보여주는 함수입니다.

## 함수는 동작 하나만 담당하게 하자!

예를들어 이름만 얻어오는 함수는 그 동작만 수행해야 한다. 얻어온 이름을 출력하는건 다른 함수가 수행하는게 더 좋다!
