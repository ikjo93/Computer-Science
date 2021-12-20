### 1. TCP(Transmission Control Protocol, 전송 제어 프로토콜) : IP의 문제점 개선
- 출발지 PORT, 목적지 PORT, 전송제어, 순서, 검증 정보 등을 포함
- 연결 지향 : TCP 3 way handshake(가상 연결, 실제 연결 X)
  - 클라이언트 -> 서버 : SYN(접속 요청)
  - 서버 -> 클라이언트 : SYN(접속 요청) + ACK(요청 수락)
  - 클라이언트 -> 서버 : ACK(요청 수락)
  - 위 3개의 과정을 통해 서로의 연결 상태를 확인한 이후에 데이터를 주고받음
  - 최근에는 ACK 과정에서 데이터를 전송 가능할 수 있게 되었다.
- 데이터 전달 보증
- 순서 보장
- 신뢰할 수 있는 프로토콜
- 현재 인터넷은 대부분 TCP/IP 기반의 네트워크를 사용하나 최근에는 UDP가 새롭게 부상하는 중이다.
  - UDP는 TCP에서 제공하는 연결지향, 데이터 전달 보증, 순서 보장 기능이 없지만 **단순하고(IP와 거의 같다. 포트 PORT와 체크섬 checksum 추가) 빠른 장점**이 있으며 TCP는 있는 그대로 사용할 수밖에 없지만 UDP는 **애플리케이션에 따라 추가 작업을 통해 최적화할 수 있는 장점**이 있다.

<br/>

### 2. TCP/IP 스택(Stack)의 4 계층(Layer)
- `애플리케이션 계층` -> `전송 계층` -> `인터넷 계층` -> `네트워크 인터페이스(접근) 계층` 순으로 데이터 전송이 이루어진다.
- 애플리케이션 계층
  - 프로토콜: HTTP, FTP, SMTP, SOCKET, etc...
- 전송 계층
  - 프로토콜: TCP, UDP
- 인터넷 계층
  - 프로토콜: IP
- 네트워크 인터페이스 계층
  - 프로토콜: MAC Address, LAN DRIVER, LAN Card, Ethernet cable, wire, etc...
- 예시
  - 애플리케이션이 Hello, world! 메시지 데이터를 생성하고 이를 SOCKET 라이브러리를 통해 데이터를 전송한다.
  - TCP 정보를 생성하고 이를 포함하여 데이터를 전송한다.
  - IP 패킷을 생성하고 이를 포함하여 데이터를 전송한다.
  - LAN Card를 통해 인터넷으로 데이터를 전송한다. 이때 이더넷 프레임(Ethernet frame)을 포함시킨다.
```
※ 참고 : SOCKET
- 웹 브라우저, 게임, 채팅 프로그램 등의 프로세스들은 소켓(SOCKET) 라이브러리를 창구로 사용하여 데이터를 주고 받는다.
- 소켓은 IP 주소와 포트(PORT) 번호로 정의되며 TCP(Transmission Control Protocol) 또는 UDP(User Datagram Protocol)를 사용할 수 있다.
- HTTP : 클라이언트의 요청이 있을 때만 서버가 응답하여 해당 정보를 전송하고 곧바로 연결을 종료
- SOCKET : 클라이언트와 서버가 특정 포트를 통해 실시간 및 양방향으로 통신
```