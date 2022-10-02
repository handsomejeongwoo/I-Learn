# 자바스크립트 반올림(round), 올림(ceil), 내림(floor)

## 올림(Math.ceil())

    자바스크리브에서 숫자를 올림 처리할 때는 주로 Math.ceil()함수 사용

    ex) ceil(1) : 1 / ceil(1.2) : 1 / ceil(1.998) : 1

        ceil(0) : 0 / ceil(null) : 0

        ceil(-1) : -1 / ceil(-1.56) : 1

## 내림(Math.floor())

    자바스크립트에서 숫자를 내림 처리할 때는 주로 Math.floor()함수 사용
    입력받은 숫자보다 작거나 같은 정수 중 가장 큰 정수를 리턴합니다.

    ex) floor(1) : 1 / floor(1.32) : 1 / floor(1.892) : 1

        floor(0) : 0 / floor(null) : 0

        floor(-1) : -1 / floor(-1.111) : -2

## 반올림(Math.round())

    자바스크립트에서 숫자를 반올림 처리할 때는 주로 Math.round()함수를 사용합니다.

    ex) round(1) : 1 / round(1.2) : 1 / round(1.7) : 2

        round(null) : 0 / round(0) : 0

        round(-1) : -1 / round(-1.5) : -1 / round(1.777) : -2
