# 자바스크립트 비교 연산자

```
자바스크립트는 주어진 두 항을 비교할 수 있는 '비교연산자 제공

+ 대소비교

+ 등가비교
```

# 대소비교

|    의미     | 연산자 | 사용 형태 |
| :---------: | :----: | :-------: |
|    크다     |   >    |   A > B   |
|    작다     |   <    |   A < B   |
| 크거나 같다 |   >=   |   A >=B   |
| 작거나 같다 |   <=   |   A<=B    |

# 등가비교

|       의미       | 연산자 | 사용 형태 |
| :--------------: | :----: | :-------: |
|       같다       |   ==   |   A==B    |
|    같지 않다     |   !=   |   A!=B    |
|   완전히 같다    |  ===   |   A===B   |
| 완전히 같지 않다 |  !==   |   A!==B   |

# EX

    console.log('1'==1) //true
    console.log('1'===1) //false

    let num1=3;
    let nume2=4;

    console.log(num1>num2) //False
    console.log(num1<num2) //True

    let num3 ='2';
    let num4 = 2;

    console.log(num3==num4) //true

    console.log(num3===num4) //False

    console.log(num3!=num4) //False

    console.log(num3!==num4) //true
