# display 속성

## 개요

- display 속성은 요소를 어떻게 보여줄지를 결정합니다.  
  주로 4가지 속성값이 쓰이는데, 태그마다 기본값이 다릅니다.
- none:보이지 않음
- block:블록박스
- inline: 인라인박스
- inline-block : block과 inline의 중간 형태

# none

## 요소를 렌더링하지 않도록 설정합니다. visibility 속성을 hidden으로 설정한 것과 달리, 영역도 차지하지 않습니다.

<br/>

# 예제

    <style>
    .display-none{ display: none }
    .invisible{ visibility: hidden }
    </style>

    <div class="display-none">1</div>
    <div>2</div>

    <div class="invisible">3</div>
    <div>4</div>

# 출력

    2  //display none은 공간도 안차지하지만

    4 //visibility 속성을 hidden으로 설정한 것은 공간을 차지한다.

<br/>

# block 태그

## div 태그, p 태그, h 태그#, li 태그 등이 이에 해당됩니다.

    width, height 속성을 지정 할 수 있으며, block 요소 뒤에 등장하는 태그가 그 이전 block 요소에 오른쪽에 배치될 수 있어도 항상 다음 줄에 렌더링됩니다.

<br/>

# inline태그

## span 태그, b 태그, i 태그, a 태그 등이 이에 해당됩니다.

    block 과 달리 줄 바꿈이 되지 않고, width와 height를 지정 할 수 없습니다.

<br/>

# inline-block태그

## block과 inline의 중간 형태라고 볼 수 있는데, 줄 바꿈이 되지 않지만 크기를 지정 할 수 있습니다.
