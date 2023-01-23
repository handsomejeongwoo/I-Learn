# interface란?

같은 형식의 타입들을 naming하는 역할이다.

# interface 예시

    interface User {
    age: number,
    name: string
    }

# 내가 써본 interface

    interface Person1 {

    name: string;
    age: number;
    }

    function hello1(person: Person1): void {
      console.log(`안녕하세요! ${person.name} 입니다.`);
    }

    const p1: Person1 = {
      name: "mark",
      age: 39,
    };

    hello1(p1); // 안녕하세요 mark 입니다.
