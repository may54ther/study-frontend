# Web

## HTTP와 HTTPS

> - HTTP : 인터넷에서 데이터를 주고 받을 수 있는 프로토콜
> - HTTPS : 제 3자가 네트워크 정보를 볼 수 없도록 HTTP를 암호화 한 것. 복호화 필요
> - HTTPS는 HTTP보다 느리고 트래픽이 많이 발생함

## 쿠키(Cookie), 로컬스토리지(LocalStorage)와 세션(Session)

> - Session
>   - 인증된 클라이언트의 정보를 서버에서 내부적으로 저장, 관리
>   - 클라이언트의 중요한 정보가 아닌 세션 ID만 넘겨주므로 쿠키보다 안전함
>   - 많은 수의 세션은 서버에 부하가 올 수 있음
>   - 세션 종료(브라우저 종료)시 자동으로 세션이 끊김
> - Cookie
>   - Size Limit : 4KB
>   - 요청 때마다 쿠키 정보를 클라이언트의 특정 경로에 파일로 전달/저장하는 방식
>   - 클라이언트의 저장장치에 파일로 저장되고, 자바스크립트로 접근 가능하므로 제 3자가 데이터를 쉽게 탈취할 수 있음
> - LocalStorage
>   - Size Limit : 5~10MB
>   - 오직 로컬에만 저장되고 서버에 전달하지 않음
>   - 사용자가 삭제하기 전까지 데이터가 소멸되지 않음

## Rest API란?

> 웹에 존재하는 모든 자원에 고유한 URI를 부여해 활용하는 것
>
> - 특정 언어나 기술에 종속되지 않고 모든 플랫폼에 사용 가능
> - API 서버는 들어오는 요청만 단순 처리
> - 동사(Method) + 명사(URI) 형태로 메시지만 보고도 행위의 이해가 쉬움
>
> ### 1. 자원(Resource) - URI
>
> - 명사를 사용해 정보의 자원을 표현
> - 소문자 사용
> - 하이픈(-, hyphen) 사용
> - 파일 확장자 사용X
> - insert, delete, update 등의 행위는 HTTP Method로 대신함
>
> ### 2. 행위(Verb) - HTTP Method
>
> - GET (리소스 조회)
> - POST (리소스 생성)
> - PUT (리소스 갱신)
> - DELETE (리소스 삭제)
>
> ##### Error
>
> - 20x : 성공
> - 30x : 리다이렉션
> - 40x : 클라이언트 에러
> - 50x : 서버
>
> ### 3. 표현(Representations)

## 자바스크립트 구동 원리

> [참고] https://joshua1988.github.io/web-development/translation/javascript/how-js-works-inside-engine/

## 서버 사이드 렌더링 (SSR, Server Side Rendering)

> 서버측에서 HTML, View를 생성하여 응답하는 방법
>
> - 초기 구동이 빠름
> - View 변경시 서버에 계속 요청(서버의 부담)

## 클라이언트 사이드 렌더링 (CSR, Client Side Rendering)

> 서버측에서 HTML을 생성하여 제공하고, View는 Javascript로 클라이언트에서 생성함
>
> - 초기 구동이 느림, 구동 후에는 서버 요청 필요X
> - SEO(Search Engine Optimization) 즉, 검색 엔진 최적화 문제가 있음
>   - Google은 자바스크립트를 해석해서 크롤링
> - ex) SPA (Single Page Application)
