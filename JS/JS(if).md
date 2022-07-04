# 조건문

## 조건문이란 주어진 조건의 참/거짓 여부에따라 프로그램의 흐름을 결정할 수 있는 구문을 뜻한다.

# if문
## 키워드 if를 이용해 만드는 구문 'if문'은 가장 일반적인 형태의 조건문이다.

### 예시 :
    if (조건){

    // 조건이 True일 때 실행될 실행문
    }

### if사용해보기:
    let number =10
    if (number > 8) {
    console.log("비교 연산을 이용해")
    console.log("조건식을 만들었어요")
    }
    !해석 변수number의 값이 8보다크면 콘솔에 2개의 구문을 출력해라
# else문 추가하기
## if문 조건이 참일때 할일을 만들고 else로 거짓일때 할일을 만든다.
    if (조건){
        // 조건이 true일 때 실행할 코드
        print("True Case")
    }
    else {
        //조건이 false일 때 실행할 코드
        print("False Case")
    }
### if-else 사용 예시

    let number = 5
    if(number==3){
        console.log("It it true")
    }else{
        console.log("It is false")
    }
### 조건문을 사용할 때 주의할점
    조건문은 '주어진 조건에 따라 선택적으로 구문을 실행한다'는 특징을
    가진 하나의 구문일 뿐이다. 조건문이 실행을 마치고 나면 코드 진행 흐름은 이어지는 다음 구문으로 자연스럽게 이동한다.
