# AJAX비동기처리+CORS

## locallhost8070 -> localhost8080
- 이렇게 접속하면 CORS 에러가 발생한다
- 왜? 외부에서, 내가 가지고 있는 리소스는 8080인데, 8070에서 접근하는 요청을 받아들인다면,
- 치명적인 보안 위협으로 다가올 수 있기 때문이다. (ex: 가짜 웹 사이트가, 실제 웹사이트 흉내)
- 따라서 몇가지 조건을 붙여서 허가 해 준다. (get, 이라던가 특정 요청에 한해)
<img width="1280" alt="image" src="https://github.com/user-attachments/assets/bc5c47dc-ce4f-435e-86ed-0f8cb2ad6962">
<img width="1280" alt="image" src="https://github.com/user-attachments/assets/947e5241-4758-4f39-91d4-ecaacea59c25">

## AJAX 비동기처리를 위한 라이브러리
- Ajax + Axios , Ajax + fetch(내장라이브러리)
- 위에서 진행한 방법은 후자 (AJAX + fetch)
- 
