### HTTP의 개념
+ 모든 웹 브라우저(클라이언트 프로그램)와 웹 서버(서버 프로그램)는 웹 상에서 일종의 규약을 지키면서 서로 요청과 응답을 주고 받는데 이 규약을 HTTP라고 한다.
+ 즉, HTTP는 HyperText Transfer Protocol(번역: 초 본문 전송 규약)의 약자로 웹 상에서 웹 브라우저와 웹 서버간 리소스(HTML 문서, 이미지, 동영상 등)를 주고받을 수 있는 일종의 규약이다.
+ HTTP를 통해 데이터를 주고 받을 때는 HTTP 요청(또는 응답) 메시지를 생성하여 이를 주고 받게 된다.
  + HTML, TEXT, IMAGE, 음성, 영상, 파일, JSON(API), XML(API) 등 거의 모든 형태의 데이터를 전송할 수 있으며 서버간에 데이터를 주고 받을 때도 대부분 HTTP를 사용한다.
+ HTTPS(HyperText Transfer Protocol over Secure Socket Layer)는 보안이 강화된 웹 통신 프로토콜로 통신의 인증과 암호화를 위해 Netscape Communications가 개발했으며, 전자 상거래에서 널리 쓰인다.

<br/>

### HTTP의 역사
+ HTTP/0.9 1991년: GET 메서드만 지원, HTTP 헤더X
+ HTTP/1.0 1996년: 메서드, 헤더 추가
+ HTTP/1.1 1997년: 가장 많이 사용, 우리에게 가장 중요한 버전
  + RFC2068 (1997) -> RFC2616 (1999) -> RFC7230~7235 (2014)
+ HTTP/2 2015년: 성능 개선
+ HTTP/3 진행중: TCP 대신에 UDP 사용, 성능 개선

<br/>

### (TCP or UDP) 기반 프로토콜
+ TCP: HTTP/1.1, HTTP/2
+ UDP: HTTP/3
+ 현재 HTTP/1.1 주로 사용
  + HTTP/2, HTTP/3 도 점점 증가

<br/>

### HTTP 특징
> #### 클라이언트-서버 구조
> 

<br/>

### 참고자료
+ 인프런 모든 개발자를 위한 HTTP 웹 기본 지식
