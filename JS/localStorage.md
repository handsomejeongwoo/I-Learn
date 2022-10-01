# 로컬스토리지란

` 로컬스토리지를 사용하면 브라우저에 key-value값을 Storage에 저장할 수 있다. 저장한 데이터는 세션간에 공유가 가능`

- setItem() - key, value추가
- getITem() - value 읽어 오기
- removeItem() - item 삭제

# 사용법 (console)

    localStorage.setItem("username","dlwjddn")
    //key = username, value = dlwjddn 로 데이터가 저장됨.

    localStorage.getItem("username") //username의 value인 dlwjddn출력

    localStorage.removeItem("username") //key와 value삭제
