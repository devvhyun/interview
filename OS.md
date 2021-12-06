
## 운영체제
<details>
<summary>운영체제란?</summary>
<div markdown="1">

시스템의 자원과 동작을 관리하는 소프트웨어이다.  
프로세스 관리, 저장장치 관리, 네트워킹 등의 기능을 수행한다.  

</div>
</details>

<details>
<summary>프로세스(Process)</summary>
  <br>
<div markdown="1">

  프로세스는 실행중인 프로그램이다.  
  하나 이상의 스레드를 포함한다.  
  운영체제로부터 주소 공간, 메모리 등을 할당 받으며 각각의 프로세스는 고유의 공간과 자원을 할당 받는다.   
  
</div>
</details>
<details>
<summary>프로세스 제어 블록(PCB, Process Control Block)</summary>
  <br>
<div markdown="1">

   PCB 는 특정 프로세스에 대한 중요한 정보를 저장하고 있는 운영체제의 자료구조이다.  
  운영체제는 프로세스의 생성과 동시애 고유한 PCB 를 생성한다.  
  프로세스 전환이 발생하면 기존 작업 내용을 PCB 에 저장하고 다시 PCB 에서 작업 내용을 불러와 다시 작업을 수행한다.  
  프로세스 식별자(PID), 프로세스상태, 프로그램 카운터 등이 저장된다. 
</div>
</details>
<details>
<summary>스레드(Thread)</summary>
  <br>
<div markdown="1">
  
  스레드는 프로세스 안에서 실행되는 작업의 단위 이다.  
  동일 프로세스 내의 스레드 끼리는 서로 전역변수나 힙 영역을 공유할 수 있다.  
  스레드마다 독립된 스택이 할당된다.
</div>
</details>
<details>
<summary>멀티스레딩의 장점</summary>
  <br>
<div markdown="1">
  
  멀티프로세스에 비해서 메모리 공간과 자원의 소모가 줄어들게 된다.  
  스레드 간의 통신을 위해 별도의 자원을 이용하지 않아도 전역 변수 공간이나 힙 영역을 통해 데이터 공유가 가능하다.  
  캐시 메모리를 비울 필요가 없기 때문에 Context Switch 가 빠르다.  
  
</div>
</details>
<details>
<summary>멀티스레딩의 문제점</summary>
  <br>
<div markdown="1">
  
  멀티프로세스의 경우는 자원에 대한 동시접근 문제를 신경쓰지 않아도 되지만 멀티스레딩의 경우는 다르다.  
  스레드 간의 데이터를 공유하기 때문에 동기화 작업이 필요하다.  
  동기화 작업으로 인해 병목 현상이 일어날 수 있으며 성능 저하가 발생할 수 있다.
</div>
</details>
<details>
<summary>멀티스레드 vs 멀티프로세스</summary>
  <br>
<div markdown="1">
  
  멀티스레드는 멀티프로세스에 비해 메모리 소모가 적고 Context Switch 가 빠르다는 장점이 있다.  
  하지만 오류로 인해 하나의 스레드가 종료되면 전체 스레드가 종료될 수 있다는 점과 동기화 문제를 가지고 있다.  
  멀티프로세스는 하나의 프로세스가 종료되더라도 다른 프로세스에 영향을 주지 않지만 자원의 소모가 많다는 단점이 있다.  
  대상 시스템의 특징에 따라 적합한 동작 방식을 선택해야 한다.
</div>
</details>
<details>
<summary>스케줄러</summary>
  <br>
<div markdown="1">
  
  CPU 를 효율적으로 사용하기 위해 어떤 프로세스에게 자원을 할당할지를 결정하는 운영체제 커널의 모듈이다.  
  현재 시스템 내에 모든 있는 모든 프로세스의 집합인 Job Queue  
  현재 메모리 내에 있으면서 실행을 대기하는 프로세스의 집합인 Ready Queue  
  I/O 작업을 대기하고 있는 프로세스의 집합인 Device Queue  
  세 가지  종류의 Queue 가 존재한다.
</div>
</details>
<details>
<summary>장기스케줄러(Long-term scheduler or job scheduler)</summary>
  <br>
<div markdown="1">
  
  작업 스케줄러라고도 불린다.  
  어떤 프로세스를 Ready Queue 에 삽입할지 결정하는 역할을 한다.  
  현대의 시분할 시스템에서는 일반적으로 장기 스케줄러를 사용하지 않는 경우가 대부분이다.  
  new -> ready 
</div>
</details>
<details>
<summary>단기스케줄러(Short-term scheduler or CPU scheduler)</summary>
  <br>
<div markdown="1">
  
  Ready Queue 에 존재하는 프로세스 중 어떤 프로세스를 running 시킬 지(CPU 할당) 결정하는 역할이다.  
  일반적으로 스케줄러라 함은 단기 스케줄러를 의미하며 단기 스케줄러는 미리 정해진 스케줄링 알고리즘에 따라 CPU 를 할당할 프로세스를 선택한다.  
  ready -> running -> wating -> ready
</div>
</details>
<details>
<summary>중기스케줄러(medium-term scheduler or swapper)</summary>
  <br>
<div markdown="1">
</div>
  
  메모리의 적재된 프로세스의 수를 동적으로 조절하기 위한 스케줄러이다.  
  메모리가 부족한 경우 여유 공간을 얻기 위해 프로세스를 통째로 메모리에서 디스크로 이동 시키는 스왑 아웃을 수행한다.  
  suspended
</details>
<details>
<summary>CPU 스케줄링</sum 
  
  비선점형 방식과 선점형 방식이 존재한다.  
  비선점형은 CPU 를 획등한 프로세스가 스스로 CPU 를 반납하기 전까지 CPU 를 뺏기지 않는 방법이다.  
  선점형 방식은 프로세스가 CPU 를 계속 사용하기를 원하더라도 강제로 CPU 를 회수 할 수 있는 방법이다.                                  
    
  
  **FCFS(First Come Fisrt Served)**  
  Ready Queue 에 들어온 순서대로 CPU 를 할당하는 비선점형 방식이다.  
  CPU 버스트가 짧은 프로세스가 먼저 Ready Queue 에  
  **SJF(Shortest - Job - First)**  
  CPU 버스트가 가장 짧은 프로세스에게 CPU 를 먼저 할당하는 방식이다.  
  평균 대기시간을 가장 짧게 하는 알고리즘으로 알려져 있다.  
  SJF 는 비선점형과 선점형 두 가지 방식으로 구현된다.  
                                                          
  SJF 비선점형 스케줄링 :  
  도착 순서에 상관 없이 CPU 버스트가 짧은 프로세스에게 CPU 를 할당한다.  
  (비선점형 이기에 이미 할당된 CPU 를 뺏지는 않는다.)   
    
  **우선순위 스케줄링**  
  우선순위가 높은 프로세스에게 CPU 를 할당하는 방식이다.  
  비선점형과 선점형 두 가지로 구현 가능하다.  
  선점형의 경우 더 높은 우선순위의 프로세스가 도착하는 경우 실행중인 프로세스를 멈추고 CPU 를 선점한다.  
  비선점형의 경우 더 높은 우선순위의 프로세스가 도착하는 경우 Ready Queue 에 Head 에 프로세스를 넣는다.  
  기아현상, 무기한봉쇄 발생 -> aging 으로 해결(대기 시간이 길어지는 경우 우선순위를 조금씩 높여주는 방법)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       
</div>
</details>
<details>
<summary></summary>
  <br>
<div markdown="1">
</div>
</details>
<details>
<summary></summary>
  <br>
<div markdown="1">
</div>
</details>
<details>
<summary></summary>
  <br>
<div markdown="1">
</div>
</details>
<details>
<summary></summary>
  <br>
<div markdown="1">
</div>
</details>
<details>
<summary></summary>
  <br>
<div markdown="1">
</div>
</details>
<details>
<summary></summary>
  <br>
<div markdown="1">
</div>
</details>
<details>
<summary></summary>
  <br>
<div markdown="1">
</div>
</details>
<details>
<summary></summary>
  <br>
<div markdown="1">
</div>
</details>
<details>
<summary></summary>
  <br>
<div markdown="1">
</div>
</details>
<details>
<summary></summary>
  <br>
<div markdown="1">
</div>
</details>
<details>
<summary></summary>
  <br>
<div markdown="1">
</div>
</details>
