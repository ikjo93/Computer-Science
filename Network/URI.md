### URI(Uniform Resource Identifier)
+ Uniform: 리소스 식별하는 통일된 방식
+ Resource: 자원, URI로 식별할 수 있는 모든 것(제한 없음)
+ Identifier: 다른 항목과 구분하는데 필요한 정보
+ URI = URL(Uniform Resource Locator) + URN(Uniform Resource Name)
  + Locator: 리소스가 있는 위치를 지정 -> 위치는 변할 수 있다.
  + Name: 리소스에 이름을 부여 -> 이름은 변하지 않는다.
  + 이름만으로 실제 리소스를 찾을 수 있는 방법은 보편화 되지 않아 URN은 거의 사용되지 않는다. -> **우리가 주로 사용하는 것은 URL!!**
+ URI와 URN 차이 비교
```
  URI -> foo://example.com:8042/over/there?name=ferret#nose
         \_/   \______________/\_________/ \_________/ \__/
          |           |            |            |        |
       scheme     authority       path        query   fragment
          |   _____________________|__
         / \ /                        \
  URN ->     example:animal:ferret:nose
  
출처 : `https://www.ietf.org/rfc/rfc3986.txt` - 1.1.3. URI, URL, and URN
```

### URL(Uniform Resource Locator)의 개념
+ URL은 **인터넷 상의 자원의 위치** 또는 **특정 웹 서버의 특정 파일에 접근하기 위한 경로 혹은 주소**이다.
  + 물리적인 서버를 찾기 위해서 반드시 필요한 것은 **IP 주소(or 도메인 이름)** 또는 **포트**이다.

### URL 분석
> 
> #### URL 전체 문법 : `scheme://[userinfo@]host[:port][/path][?query][#fragment]`
> + URL 예시 : `https://www.google.com:443/search?q=hello&hl=ko`
>   + 프로토콜 : https
>   + 호스트명(도메인명) : `(www.google.com)`
>   + 포트번호 : 443
>   + 패스 : /search
>   + 쿼리 파라미터 : q=hello&hi=ko
> 
> #### scheme
> + 주로 프로토콜을 사용함
> + 프로토콜 : 어떤 방식으로 자원에 접근할 것인가 하는 약속 규칙
>   + http, https, ftp 등
>   + https는 http에 보안 추가 (HTTP Secure)
>   
> #### userinfo
> + 사용자 정보를 포함해서 인증 but 거의 사용하지 않음
> 
> #### host
> + 호스트명 or 도메인명 or IP 주소
> 
> #### PORT
> + 일반적으로 생략, 생략 시 http는 80, https는 443
>
> #### path
> + 리소스 경로(path), 계층적 구조
>
> #### query
> + key=value 형태
> + ?로 시작, &로 추가 가능 ?keyA=valueA&keyB=valueB
> + query parameter, query string 등으로 불림, 웹서버에 제공하는 파라미터, 문자 형태
> 
> #### fragment
> + html 내부 북마크 등에 사용
> + 서버에 전송하는 정보 아님
> ```
> ※ 참고 : fragment도 URL에 포함되는가?
> fragment는 일반적으로 URL에 포함시켜 사용되어져 왔으나,
> URL scheme은 RFC 1738에서 http://<host>:<port>/<path>?<searchpart>로 정의되어 있으며,
> RFC 1808, 2.1. URL Syntactic Components 에서는 #fragment 부분이 URL이 아니라고 명시되어있다.
> "Note that the fragment identifier(and the "#" that precedes it) is not considered part of the URL."
> ```

<br/>

### 참고자료
+ 인프런 모든 개발자를 위한 HTTP 웹 기본 지식
