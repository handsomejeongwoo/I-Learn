# CSS 적용 우선순위 정하기

- 나중에 작성된 스타일이 먼저 작성된 스타일보다 우선순위가 높다.

- !important -> inline style -> id -> class 순으로 우선순위가 높다.

# !important란

!important는 강제로 우선순위를 부여한다.

# 사용예시

```css
.box {
  background-color: red;
}

.box {
  background-color: pink !important;
} // 이게 적용됨
```
