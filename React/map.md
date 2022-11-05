# map() 함수란?

- 반복되는 컴포넌트를 렌더링하기 위한 자바스크립트 배열의 내장 함수이다.
- 파라미터로 전달된 함수를 사용하여 배열 내 각 요소를 원하는 규칙에 따라 변환환 후 새로운 배열을 생성한다.

# 문법

- arr. map(callbackFunction,[thisArg])
- arr.map(callbackFunction(currenValue,index,array),thisArg)

1. callbackFunction: 새로운 배열의 요소를 생성하는 함수로서 다음 세가지 인수를 갖는다.

   - currenValue: 현재 배열 내의 값들을 의미
   - index: 현재 배열 내 값의 인덱스를 의미
   - array: 현재배열

2. thisArg(선택항목): callback 함수 내부에서 사용할 this레퍼런스를 설정한다.
