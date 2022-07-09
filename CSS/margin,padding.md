# margin,padding 속성

    margin과 padding 속성은 각각 바깥쪽 여백, 안쪽 여백을 의미한다.
    width,height 속성과 마찬가지로 숫지뒤에 단위를 표시하여 적습니다.

# 방향

## 방향마다 여백을 다르게 설정할수 있습니다.

- margin: 20px 같은 표현은 상하좌우 모두 20px을 의미합니다
- margin: 30px 10px은 상하 30px, 좌우 10px을 의미합니다.
- margin: 30px 10px 20px 50px은 위 30px, 오른쪽 10px, 아래 20px, 왼쪽 50px을 의미합니다.
- margin: 30px 10px 40px은 위 30px, 좌우 10px, 아래 40px을 의미합니다.

# 사용법

    #id{margin:10px;padding:20px}

# margin

- 테두리 바깥쪽 여백을 표현

- 요소와 요소사이의 여백을 표현

- 마진은 top, right, bottom, left 네방향을 설정

# padding

- 테두리와 콘텐츠 사이의 여백을 표현

- 패딩은 top, right, bottom, left 네방향을 설정

# vertical-align

## 인라인 요소 수직 정렬

- inline이나 inline-block요소에만 적용됨
  div태그 쓰면 적용 안됨
- 요소 자체만을 정렬하고, 내용에는 영향 X

- vertical-align 은 정렬하려는 요소를 다른 인라인 요소에 상대적으로
  정렬함

# 인라인 요소 속성 값

    baseline | sub | super | text-top | text-bottom | middle |top | bottom| 길이값| %

- 대부분 부모 요소에 상대적으로 정렬합니다.
