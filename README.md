# AJAX비동기처리+CORS

## locallhost8070 -> localhost8080
- 이렇게 접속하면 CORS 에러가 발생한다
- 왜? 외부에서, 내가 가지고 있는 리소스는 8080인데, 8070에서 접근하는 요청을 받아들인다면,
- 치명적인 보안 위협으로 다가올 수 있기 때문이다. (ex: 가짜 웹 사이트가, 실제 웹사이트 흉내)
- 따라서 몇가지 조건을 붙여서 허가 해 준다. (get, 이라던가 특정 요청에 한해)

<img width="700" alt="image" src="https://github.com/user-attachments/assets/bc5c47dc-ce4f-435e-86ed-0f8cb2ad6962">

- bootjar 를 통해 "스냅 샷 jar" 파일 생성
- cmd 를 통해, 파일 경로에 접근하여 jar 파일을 실행
- 아래와 같이 cmd 환경에서 jar 파일이 돌아간다
    * 배포를 진행하고, 외부 환경에서 실행한 것과 마찬가지 (다른 컴퓨터에서 서버를 구동 시킨 것)
    * 이와 동일하게 인텔리제이 내부에서 서버를 두개 동시에 돌리는 것도 가능하다 (포트번호 다르게, 얼티메이트 기준)
 
<img width="700" alt="image" src="https://github.com/user-attachments/assets/947e5241-4758-4f39-91d4-ecaacea59c25">
<img width="700" alt="image" src="https://github.com/user-attachments/assets/0db4acd4-99c9-4517-9647-44cd9c53cc53">

- 2024-08-28T20:55:51.714+09:00 : Tomcat started on port 8070 (http) with context path '/'
- apiService.sendToken({ url: 'http://localhost:8080/api/v1/sample/hellos',
- 위와 같이, 서버는 8070에서 돌아가는데, 8080으로 요청을 보내면 CORS 로 인해 접근이 불가능하다.
  
<img width="700" alt="image" src="https://github.com/user-attachments/assets/604ad145-2819-4478-a114-38cbf0995512">
<img width="700" alt="image" src="https://github.com/user-attachments/assets/a13bfef2-89c7-4747-a1d1-ace8f3c034c4">
<img width="700" alt="image" src="https://github.com/user-attachments/assets/ac70a5fc-e5dd-401a-9718-f098d3663f7d">
<img width="700" alt="image" src="https://github.com/user-attachments/assets/881325ed-8fcd-4c9e-807e-f82d6e47468f">



## AJAX 비동기처리를 위한 라이브러리
- Ajax + Axios , Ajax + fetch(내장라이브러리)

<img width="700" alt="image" src="https://github.com/user-attachments/assets/b4e371ee-a572-4bcf-9bf9-3107fe2d7eeb">

- 위에서 진행한 방법은 후자 (AJAX + fetch)
