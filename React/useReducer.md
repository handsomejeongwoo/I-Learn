# useReducer 훅이란?

- useState를 대체할 수 있는 함수.

# useReducer 사용해보기

```
import React, { useReducer } from "react";
const [state, dispatch] = useReducer(reducer, initialState);
```

## state

- 컴포넌트에서 사용할 상태

## reducer 함수

- 컴포넌트에서 state를 업데이트 하는 함수이다.
- 현재state, action 객체를 인자로 받아, 기존의 state를 대체하여 새로운 state를 반환하는 함수

## initialState

- 초기 state

## dispatch 함수

- 첫번째 인자인 reducer함수를 실행시킨다.

- 컴포넌트 내에서 state 업데이트를 일으키기 위해 사용함.

- reducer 함수를 실행 시킨다.

- action 객체를 인자로 받으며 action 객체는 어떤 행동인지를 나타내는 type 속성과 해당 행동과 관련된 데이터(payload)를 담고 있다.

- action을 이용하여 컴포넌트 내에서 state의 업데이트를 일으킨다.

# example

```
function reducer(state, action) { // 함수의 인자로 state와 action을 받는다.
  switch (action.type) { // 인자 action의 타입의 따라서 switch문으로 state를 업데이트한다.
    case "INCREMENT":
      return { count: state.count + 1 };
    case "DECREMENT":
      return { count: state.count - 1 };
    default:
      throw new Error("unsupported action type: ", action.type);
  }
}
```
