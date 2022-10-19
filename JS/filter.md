# Array filter

filter는 해석 그대로 걸러주는 역할을 하는 함수입니다. 주로 특정 조건을 만족하는 새로운 배열을 필요로 할 때 사용하는 편입니다.

# 사용법

    const numbers = [1, 2, 3, 4, 5];
    const result = numbers.filter(number => number > 3);

    console.log(numbers);
    // [1, 2, 3, 4, 5];

    console.log(result);
    // [4, 5]
