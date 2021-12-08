## 네트워크
<details>
  <summary>OSI 7 계층</summary>
  <br>
  <div markdown="1">
    
  **데이터 송수신 시, 컴퓨터 내에서 이뤄지는 작업들을 7개 계층으로 분리한 것이다.  
    각 계층은 서로 독립적이므로 데이터가 전달되는 동안 다른 계층의 영향을 받지 않는다.**  
      
    **캡슐화**  
    7 계층 -> 1 계층의 과정, 데이터가 전송되는 과정 동안 데이터에 각 계층의 헤더가 붙는 과정이다.
    
  **1 계층 : 물리 계층**  
      
  전송되는 데이터를 전기신호로 변환하는 계층이다.  
    (랜카드, 리피터, 허브)  
      
  **2 계층 : 데이터 링크 계층**  
      
  네트워크 장비 간에 신호를 주고 받는 규칙을 정하는 계층이다.  
    프레임 생성 : 데이터 + 이더넷 헤더 + 트레일러
      
  **3 계층 : 네트워크 계층**  
      
  네트워크 간의 통신을 가능하게 하는 계층이다.  
    라우팅을 통해 데이터를 목적지까지 빠르고 안전하게 전송한다.
    데이터 + IP 헤더  
      
  **4 계층 : 전송 계층**  
      
  통신을 활성화하기 위한 계층이다.  
    보통 TCP 프로토콜을 이용하며, 포트를 열어서 응용프로그램들이 전송을 할 수 있게 한다.  
      
  **5 계층 : 세션 계층**  
      
  데이터가 통신하기 위한 논리적 연결을 담당한다. TCP/IP 세션을 만들고 없애는 책임을 지는 계층이다.  
      
  **6 계층 : 표현 계층**  
      
  데이터의 형식을 정의하는 계층이다. 서로 다른 환경의 컴퓨터와 애플리케이션들이
    데이터를 서로 이해할 수 있도록 도와주는 계층이다. (변환, 압축, 암호화)  
      
  **7 계층 : 응용 계층**  
      
  사용자가 직접 눈으로 보고 작업을 하는 계층이다. HTTP, FTP, SMTP 등 사용자와 직접적으로 상호작용 하는 모든 응용 프로그램들이 속한다.  
      
  
  </div>
</details>

<details>
  <summary>TCP/IP 4 계층</summary>
  <br>
  <div markdown="1">
    
  네트워크 전송 시 데이터 표준을 정리 한 것이 OSI 7 계층이다.  
  이 이론을 실제 사용하는 인터넷 표준이 TCP/IP 4 계층이다.  
      
  **1 계층 : 네트워크 계층**  
      
  OSI 7 계층에서 물리 계층(1계층) 과 데이터 링크 계층(2계층) 에 해당된다.  
    실제 데이터인 프레임을 송수신하는 계층이다.  
    또한 하드웨어적인 요소와 관련되는 모든 것을 지원하며 물리적인 주소로 MAC 주소를 사용한다.  
      
  **2 계층 : 인터넷 계층**  
      
  OSI 7 계층에서 네트워크 계층에 해당된다.  
    데이터에 IP 헤더를 붙여 IP 패킷을 만들고 이를 전송하는 역할을 한다.  
      
  **3 계층 : 전송 계층**  
      
  OSI 7 계층에서 전송 계층에 해당된다.  
    통신 노드간의 연결을 제어하고, 자료의 송수신을 담당하는 역할을 한다.  
    TCP 나 UDP 를 사용한다.  
      
  **4 계층 : 응용 계층**  
      
  OSI 7 계층에서 세션, 표현, 응용 계층에 해당된다.  
    응용 프로그램들에게 표준적인 인터페이스를 제공하는 역할을 한다.  
    FTP, DNS, SMTP 등을 사용한다.
      
    
  </div>
</details>

<details>
  <summary>HTTP / HTTPS</summary>
  <div markdown="1">
    
  **HTTP** : 클라이언트와 서버 사이에 자원을 주고 받을 때 사용하는 통신 규약이다.  
    요청 및 응답 구조 이며 80번 port 를 사용한다.  
      
    
  **HTTPS** : HTTP에 SSL을 추가함으로써 보안을 강화한 프로토콜이다.  
    HTTP 는 원래 TCP 와 직접 통신하였지만, HTTPS 에서는 SSL 과 통신하고 SSL 이 TCP 와 통신한다.  
    SSL 을 사용하여 암호화와 증명서를 이용할 수 있게 된다.
      
  **HTTP 의 문제점**  
    단순 텍스트를 주고 받기 때문에 누군가 네트워크에서 신호를 가로챈다면 데이터가 노출될 수 있다.  
      
  **SSL**  
    하이브리드 암호 시스템 : 대칭키 방식 + 공개키 방식  
    대칭키를 주고 받을 때는 공개키를 사용하고, 이후 부터는 대칭키 방식을 사용한다.
      
  대칭키 방식 : 1개의 키로 암호화 복호화 모두에 사용한다.  
    공개키 방식 : 2개의 개인키와 공개키를 사용한다. 개인키로 암호화한 것은 공개키로 복호화 가능하다. 반대의 경우도 가능하다.  
    
  </div>
</details>

<details>
  <summary>DNS</summary>
  <div markdown="1">
    
  Domain Name Service, URL 을 IP 주소로 변환하는 서비스이다.  
    기본적으로 UDP 를 사용한다.  
    (TCP 에서는 3-way handshake 와 같은 오버헤드가 발생하기 때문)
      
    1. url 입력  
    2. 웹 브라우저가 url 을 분석한다.  
    3. DNS 서버에 해당하는 도메인의 IP 주소 요청  
    (요청 전에 브라우저에 해당 도메인이 캐시되어 있는지 먼저 확인한다.  
    로컬에 저장되어 있는 hosts 파일에서 참조할 수 있는 도메인이 있는지 확인한다.)  
    4. Root DNS 서버에 요청한다.
    5. .com DNS 서버에 요청한다.  
    6. naver.com 네임 서버에 요청한다. ->naver.com 의 IP 주소를 반환  
    7. 로컬메모리에 캐싱된다.  
    
  </div>
</details>

<details>
  <summary>TCP / UDP</summary>
  <div markdown="1">
    
  **TCP 프로토콜**  
      
  데이터 통신을 위한 프로토콜의 일종으로 연결지향 프로토콜이다.  
    3-way handshake 를 통한 가상 회선을 제공하며 흐름제어, 혼잡제어를 제공한다.  
    이를 통해 높은 신뢰성을 보장한다.  
    서버와 클라이언트는 1대1 로 연결된다.
      
  **흐름제어** : 전송 속도를 조절하여 버퍼 오버플로우를 방지하는 것이다.  
    **혼잡제어** : 네트워크 내에 패킷의 수가 과도하게 증가하는 현상을 방지하는 것이다.  
      
  **UDP 프로토콜**  
      
  데이터 통신을 위한 프로토콜의 일종으로 비연결성이며 데이터그램 방식을 제공하는 프로토콜이다.  
    별도의 연결이나 해제, 신뢰성을 보장하는 과정이 없기 때문에 속도가 빠르나 신뢰성이 낮다.  
    멀티캐스팅이 가능하다.  
    스트리밍 서비스에 적합하다.
    
  </div>
</details>

<details>
  <summary>HTTP Method</summary>
  <div markdown="1">
    
  GET : 서버에 존재하는 데이터를 요청하는 것입니다. CRUD 중 R 에 해당합니다.  
  POST : 서버에 데이터 생성을 요청하는 것입니다. CRUD 중 C 에 해당합니다.  
  PUT : 서버에 존재하는 데이터를 수정하거나 존재하지 않으면 생성하는 요청입니다. CRUD 중 C 와 U 입니다.  
  DELETE : 서버에 데이터 제거를 요청합니다. CRUD 중 D 에 해당합니다.  
  PATCH : 서버에 존재하는 데이터를 일부 수정합니다. CRUD 중 U 입니다.  
  OPTIONS : 서버가 허용하는 메소드를 확인할 때 사용합니다.  
  HEAD : GET 과 마찬가지로 데이터를 요청하지만 header 만 가져오는 요청입니다.  
    
  </div>
</details>

<details>
  <summary>TCP 3, 4 way handshake</summary>
  <div markdown="1">
    
    TCP 3way handshake 는 가상회선을 수립하는 단계입니다.  
    클라이언트는 서버에 요청을 전송할 수 있는지,  
    서버는 클라이언트에게 응답을 전송할 수 있는지 확인하는 과정입니다.  
    SYN, ACK 패킷을 주고 받으며, 임의의 난수로 SYN 플래그를 전송하고 ACK 플래그에는 1을 더한 값을 전송합니다.  
    SYN(n) -> ACK(n+1), SYN(m) -> CK(m+1) 순으로 일어납니다. 임의의 난수를 지정하는 이유는 기존 요청과 구분하기 위해서 입니다.  
      
    TCP 4way handshake 는 TCP 연결을 해제하는 단계입니다.  
    클라이언트는 서버에게 연결 해제를 통지하고,  
    서버는 이를 확인했음을 전송하고, 데이터를 모두 전송한 뒤 연결 종료를 클라이언트에게 전송합니다.  
    클라이언트는 종료 확인을 서버에게 전송합니다.  
    클라이언트는 소켓이 닫힌 후에도 일정시간 대기하는데, 혹시 패킷이 나중에 도착할 수 있기 때문입니다.  
      
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

<details>
  <summary></summary>
  <div markdown="1">
    
    
  </div>
</details>

