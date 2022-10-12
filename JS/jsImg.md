# 자바스크립트 이미지 업로드 방법

자바 스크립트로 이미지파일을 불러오고 hmtl화면에 띄우는 방법이다.

- input
- button
- img
  태그를 이용

# 해보기

    <input type="file" id="inputImage">
    <button id="sendButton">보내기</button>
    <img src="" class="uploadImage">

    보내기를 클릭하면 file 주소를 가져오는 방법은 다음과 같다.

    <script>
    document.querySelector("#sendButton).addEventListener("click",()=>{
      let selectFile = doccument.querySelector("#inputImage").files[0];
      const file = URL.createObjectURL(selectFile);
      doccument.querySelector(".uploadImage").src = file;
    })
    <script/>
