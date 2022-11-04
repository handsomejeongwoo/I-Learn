# spread란?

`반복가능한 객체 = 배열,문자열,개게 등등`

`스프레드 연산자 = 반복가능한 객체를 개별요소로 만들어 주는 기능`

# 예시

    let arr1 = [1, 2, 3];
    let arr2 = [4, 5, 6];

    let arr = [...arr1, ...arr2];

    let arrr = [0, arrr1, 2, arr2];

    console.log(arrr);
    //[0, 1, 2, 3, 2, 4, 5, 6]

    console.log(arr);
    //[1, 2, 3, 4, 5, 6]
