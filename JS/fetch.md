# fetch()함수

fetch()함수는 첫번쨰 인자로 URL, 두번쨰 인자로 옵션 객체를 받고, Promise 타입의 객체를 반환합니다.
반환된 객체는, API 호출이 성공했을 경우에는 응답(response) 객체를 resolve하고, 실패했을 경우에는 예외(error) 객체를 reject합니다.
<br/>
<br/>
fetch(url, options)  
.then((response) => console.log("response:",response))  
.catch((error) => console.log("error:",error))
