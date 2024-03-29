
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
<summary>Context Switch</summary>
  <br>
<div markdown="1">
  
  현재 CPU 를 사용중인 프로세스의 CPU 제어권이 다른 프로세스로 이양되는 과정이다.  
  Context Switch 에 사용되는 메모리, 시간을 오버헤드라 한다.  
    
  스레드가 프로세스보다 빠른 이유는 컨텍스트 스위칭 때문이다.  
  멀티스레드 환경에서는 컨텍스트 스위칭이 드물게 일어난다.  
  스레드는 공유하는 데이터(code, data, heap) 가 있기 때문에 PCB 의 stack 영역만 스위칭을 하기 때문에 비용이 적게 든다.  
  
 
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
  <summary>CPU 스케줄링</summary>  
  <br>
  <div markdown="1">
    
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
                                                          
  **SJF 비선점형 스케줄링** :  
  도착 순서에 상관 없이 CPU 버스트가 짧은 프로세스에게 CPU 를 할당한다.  
  (비선점형 이기에 이미 할당된 CPU 를 뺏지는 않는다.)   
    
  **우선순위 스케줄링**  
  우선순위가 높은 프로세스에게 CPU 를 할당하는 방식이다.  
  비선점형과 선점형 두 가지로 구현 가능하다.  
  선점형의 경우 더 높은 우선순위의 프로세스가 도착하는 경우 실행중인 프로세스를 멈추고 CPU 를 선점한다.  
  비선점형의 경우 더 높은 우선순위의 프로세스가 도착하는 경우 Ready Queue 에 Head 에 프로세스를 넣는다.  
  기아현상, 무기한봉쇄 발생 -> aging 으로 해결(대기 시간이 길어지는 경우 우선순위를 조금씩 높여주는 방법)  
    
  **Round Robin 스케줄링**  
  선점형 방식이다.  
  시분할 시스템의 성질을 잘 황용한 가장 현대적인 CPU 방식이다.  
  각 프로세스가 CPU 를 연속적으로 사용할 수 있는 시간을 제한하여 이 시간이 경과하면 CPU 를 회수하여 다른 프로세스에게 할당한다.  
  CPU 를 연속적으로 사용할 수 있는 최대 시간을 할당 시간(Quantum Time) 이라 한다.  
  할당 시간이 지나면 프로세스는 CPU 를 빼앗기고 Ready Queue 의 맨 뒤로 돌아간다.  
  할당 시간이 너무 길면 FCFS 와 같게되며 너무 짧은 경우 잦은 Context Switch 로 인해 오버헤드가 발생한다.  
  CPU 버스트 시간이 짧은 프로세스가 CPU 를 빨리 할당받게 하는 동시에 CPU 버스트 시간이 긴 프로세스가 불이익을 당하지 않도록 하는 것이다.  
  프로세스의 대기 시간이 자신의 CPU 버스트 시간에 비례해 증가하므로 공정한 스케줄링이라 할 수 있다.
  
</div>
</details>
<details>
<summary>Sync vs Async</summary>
  <br>
<div markdown="1">

  **Sync(동기)**  
  메스드의 실행과 동시에 반환 값이 기대되는 경우이다.  
  메소드 실행 시 값이 반환되기 전까지 blocking 되어 있다.  
    
  **Async(비동기)**  
  메소드의 실행과 동시에 반환 값이 기대되지 않는 경우이다.  
  메소드 실행 시 blocking 되지 않고 이벤트 큐에 넣거아 백그라운드 스레드에게 해당 task 를 위임하고 바로 다음 코드를 실행하기 때문에 기대되는 값이 바로 반환되지 않는다.  
  
</div>
</details>
<details>
<summary>인터럽트</summary>
  <br>
<div markdown="1">
  
  프로그램을 실행하는 도중에 예기치 않은 상황이 발생할 경우 현재 실행 중인 작업을 즉시 중단하고, 발생된 상황에 대한 우선 처리가 필요함을 CPU 에게 알리는 것이다.  
  해당 상황을 처리한 뒤 다시 기존의 일을 진행한다.  
  CPU 의 하드웨어 신호에 의해 발생하는 외부/내부(Trap) 인터럽트  
  명령어의 수행에 의해 발생하는 소프트웨어 인터럽트  
    
  폴링 방식 : 사용자가 명령어를 사용해 핀의 값을 계속 읽어 변화를 알아내는 방식  
  인터럽트 방식 : MCU 자체가 하드웨어적으로 변화를 체크하여 변화 시에만 일정한 동작을 하는 방식  
    
  인터럽트 방식은 하드웨어의 지원을 받아야 하지만, 폴링 방식에 비해 신속한 대응이 가능하다. 따라서 실시간 대응이 필요한 경우 필수적이다.  
</div>
</details>
<details>
<summary>프로세스 동기화</summary>
  <br>
<div markdown="1">
  
  임계영역(Critical Section) : 동일한 자원에 동시에 접근하는 작업을 실행하는 영역을 임계영역이라 한다.  
  한번에 하나의 프로세스만 이용하게끔 보장해줘야 하는 영역이다.  
    
  
  **임계영역 문제 해결 조건**  
  1. 상호 배제(Mutual Exclution)  
    하나의 프로세스가 임계영역에서 실행 중이라면, 다른 프로세스는 임계영역에 들어올 수 없다.    
  2. 진행(Progress)  
    임계영역에서 실행중인 프로세스가 없는 경우 별도의 동작이 없는 프로세스들만 임계영역에 진입 후보로서 참여할 수 있다.  
  3. 한정 대기(Bounded Wating)  
    다른 프로세스의 기아(Starvation) 을 방지하기 위해, 한번 임계영역에 들어갔던 프로세스는 이후 진입 횟수에 제한이 있어야 한다.  
    
  **해결방법**  
  **1. Lock**  
    하나의 스레드나 프로세스가 자원을 사용하고 이는 동안에는 다른 스레드나 프로세스가 접근하지 못하도록 하는 방식이다.  
  무한루프문을 통해 구현한다.(Lock 해제를 기다리는 스레드나 프로세스는 이 무한루프에 갇혀있다.)  
    
  특정한 상황에서는 제대로 작동하지 않는다.  
  무한루프를 돌게끔 변수의 값을 변경하기 전 인터럽트가 걸려 값을 변경하지 못하고 다른 스레드가 Lock 함수에 들어오게 된다면 두 개의 스레드가 임계영역에 동시접근을 하는 상황이 발생한다.  
    
  **2.Semaphores**  
    Binary Semaphores : Mutex 라 불리며 0과 1 사이의 값만 사용하며, 다중 프로세스들 사이의 임계영역 문제를 해결하기 위해 사용한다.  
    Counting Semaphores : 가용한 개수를 가진 자원에 대한 접근 제어용으로 사용되며, Semaphores 는 그 가용한 자원의 개수로 초기화 된다.  
    
  **Mutex 와 Lock 의 차이점  
    Lock 과 Mutext 는 임계영역의 락이 풀릴 때까지 기다려야 한다는 공통점이 있다.  
  하지만 Lock 은 락이 걸려 있는 경유 CPU 를 양보하지 않는다.  
  Mutex 는 락이 풀리기를 기다리면서 Context Switch 를 실행한다. 병렬 처리가 가능하지만 Context Switch 에서 발생하는 오버헤드 문제가 있다.  
    
  
 **3. Monitor**  
    하나의 프로세스 내에 다른 스레드 사이의 임계영역 문제를 해결한다.  
  Semaphores 와 비슷하지만 사용이 더 간단하다. (락 획득 및 해제와 관련된 모든 부분을 다 처리해준다.)
  
</div>
</details>
<details>
<summary>메모리 관리 전략</summary>
  <br>
<div markdown="1">
  
  **Swapping**  
  메모리의 관리를 위해 사용되는 기법이다.  
  Round Robin 과 같은 스케줄링의 다중 프로그래밍 환경에서 CPU 할당 시간이 끝난 프로세스의 메모리를 보조 기억장치(e.g. hdd) 로 내보내고 다른 프로세스의 메모리를 불러 들인다.  
    
  
    swap-in : ->주기억장치(RAM)  
    swap-out : ->보조기억장치  
    
  **단편화(Fragmentation)**  
  사용 가능한 메모리가 존재하지만 할당이 불가능한 상태를 메모리 단편화라 한다.  
  프로세스들이 차지하는 메모리 틈 사이에 사용하지 못할 만큼의 작은 자유 공간들이 생기는데, 이것이 단편화이다.  
    
  **내부 단편화**  
  프로세스가 필요한 메모리 크기보다 더 많은 크기를 할당받아 사용하는 메모리 공간을 제외하고 낭비되는 공간이 생기면 이를 내부 단편화라 한다.  
  ->**Segmentation 기법**  
  가상메모리를 논리적인 단위인 세그먼트로 분할하여 메모리를 할당한다.  
  프로세스가 필요한 크기게 맞게 할당해주어 내부 단편화를 막는다.  
  각 세그먼트는 적재될 빈 공간을 찾아 할당되며 연속적인 공간에 저장된다.  
  세그먼트 테이블이 필요하다.(세그먼트 시작주소와 길이정보를 가진 테이블)  
    
  **외부 단편화**  
  메모리의 할당과 해제가 반복되면서 할당된 메모리 사이의 빈 공간이 생기게 되고, 총 메모리 공간은 충분하지만 할당이 될 수 없는 것을 외부 단편화라 한다.  
    
  ->**Paging 기법**  
  가상메모리를 같은 크기의 페이지로 미리 나누고 프로세스에게 할당해준다.  
  프로세스가 필요한 만큼 할당하는게 아닌 같은 크기의 페이지로 나눈 것을 할당하기 때문에 꽉 채워 쓰지 않는 경우가 있어 내부 단편화가 발생할 수 있다.  
  연속적이지 않은 공간도 활용할 수 있기 때문에 외부 단편화를 해결할 수 있다.  
  
  
    외부단편화 : 메모리 공간 중 사용하지 못하게 되는 일부분이다.  
    내부단편화 : 프로세스가 사용하는 메모리 공간에 포함된 남는 부분이다.  
      
  압축 : 외부 단편화를 해소하기 위해 프로세스가 사용하는 공강들을 한쪽으로 몰아 자유공간을 확보하는 방법이다. (효율이 낮음)  
    
  **Paging**  
  하나의 프로세스가 사용하는 메모리 공간이 연속적이어야 한다는 제약을 없애는 메모리 관리 방법이다.  
  외부단편화와 압축 작업의 문제를 해소하기 위해 생긴 방법론이다.  
  물리 메모리는 Frame 이라는 고정 크기로 분리되어 있고, 논리 메모리(프로세스가 점유하는 메모리) 는 페이지라 불리는 고정 크기의 블록으로 분리된다.  
  논리 메모리는 물리 메모리에 저장될 때, 연속적일 필요가 없고 물리 메모리의 남는 프레임에 적절히 배치됨으로 외부 단편화를 해결할 수 있다.  
  하지만 내부단편와 문제의 비중이 늘어나게 된다.  
    
  **Segmentation**  
  논리 메모리와 물리 메모리를 같은 크기의 블록이 아닌, 서로 다른 크기의 논리적 단위인 세그먼트로 분할한다.  
  세그먼트 테이블에는 각 세그먼트의 기준과 한계를 저장한다.  
    
  서로 다른 크기의 세그먼트들이 메모리에 적재되고 제거되는 일이 반복되다 보면, 자유 공간들이 많은 수의 작은 조각들로 나누어져 못 쓰게 될 수도 있다.(외부단편화)
</div>
</details>
<details>
<summary>가상 메모리</summary>
  <br>
<div markdown="1">
  
  **가상 메모리**  
    
   프로세스 전체가 메모리 내에 올라오지 않더라도 실행이 가능하도록 하는 기법이다.  
    각 프로그램에 실제 메모리 주소가 아닌 가상의 메모리 주소를 주는 방식이다.  
    프로그램이 물리 메모리보다 커도 된다는 장점이 있다.  
    
  ex) 하나의 프로그램이 실행의 필요한 논리 메모리가 100mb, 하지만 실제로 실행에 필요한 메모리 공간은 40mb 라면 실제 물리 메모리에는 40mb 만 올리고, 나머지 60mb 은 필요시에 물리 메모리에 요구한다.  
    
  **Demanding Paging(요구페이징)**  
      
   프로그램 실행 시에 프로그램 전체를 물리 메모리에 적재하는 대신, 초기에 필요한 것들만 적재하는 전략을 요구페이징이라 한다.  
    가상 메모리 시스템에서 많이 사용된다.  
    가상 메모리는 일반적으로 페이지로 관리된다.  
    한 번도 접근되지 않은 페이지는 물리 메모리에 적재되지 않는다.

</div>
</details>
<details>
<summary>페이지 교체 알고리즘</summary>
  <br>
<div markdown="1">
  
  **Page Fault** : 프로그램이 자신의 주소 공간에는 존재하지만 시스템의 RAM 에는 현재 없는 데이터나 코드에 접근을 시도할 경우 발생하는 현상 (페이지 부재)  
    
  페이지 부재 발생 -> 새로운 페이지 할당 해야함 -> 현재 할당된 페이지 중 어떤 것을 교체할 지 결정하는 방법  
    
  가상 메모리는 요구 페이지 기법을 통해 필요한 페이지만 메모리에 적재한다. 하지만 결국엔 메모리가 가득 차게 된다. 이 때 추가로 페이지를 가져오기 위해 기존의 페이지를 out 해야 한다. 어떤 페이지를 out 할지 결정하는 방법이다.  
    
  **FIFO(First-In First-Out) 알고리즘**  
    Victim Page : 메모리에 먼저 올라온 페이지  
    초기화 코드에 적용하기 좋다.  
    
  **OPT(Optimal Page Replacement) 알고리즘**  
    Victim Page : 앞으로 가장 사용하지 않을 페이지  
    FIFO에 비해 페이지 부재의 횟수를 많이 감소 시킬 수 있다.  
    하지만 실질적으로 앞으로 잘 사용되지 않을 것이라는 보장이 없기 때문에 수행하기 어려운 알고리즘이다.  
    
  **LRU(Least-Recently-Used) 알고리즘**  
    Victim Page : 최근에 사용하지 않은 페이지  
    실질적으로 사용이 가능한 알고리즘  
    OPT 보다 덜 효율적일 수 있으나 실제로 사용 가능한 알고리즘 중 최선이다.  
    
  **교체 방식**  
    Global 교체 : 메모리 상의 모든 프로세스 페이지에 대해 교체하는 방식  
    Local 교체 : 메모리 상의 자기 프로세스 페이지에서만 교체하는 방식  
    (Victim page 선정 기준 차이)
</div>
</details>
<details>
<summary>캐시메모리</summary>
  <br>
<div markdown="1">
  
  주기억장치에 저장된 내용의 일부를 임시로 저장해두는 기억장치이다.  
  CPU와 주기억장치의 속도 차이로 인한 성능 저하를 방지하기 위한 방법이다.  
  CPU 가 이미 봤던 거에 대해 재접근할 때, 메모리 참조 및 인출 과정에 대한 비용을 줄이기 위해 캐시에 저장해둔 데이터를 활용한다.  
    
  **Hit** : 캐시 기억장치에 명령이 존재  
  **Miss** : 캐시 기억장치에 명령이 존재하지 않음  
    
  적중율(Hit Rate) 을 극대화 시키기 위해 데이터 지역성의 원리를 사용한다.  
    
  **지역성** : 기억 장치 내의 정보를 균일하게 액세스 하는 것이 아니라 한 순간에 특정 부분을 집중적으로 참조하는 특성  
    
  **시간지역성** : 최근에 참조된 주소의 내용은 곧 다음에도 참조되는 특성  
  **공간지역성** : 실제 프로그램이 참조된 주소와 인접한 주소의 내용이 다시 참조되는 특성  
    
  **캐싱라인**  
  캐시에서 목적 데이터에 바로 접근할 수 있도록 캐시에 데이터를 저장할 때 특정 자료구조를 사용하여 묶음으로 저장하게 되는데 이를 캐싱라인이라 한다.  
  캐시에 저장하는 데이터와 데이터의 메모리 주소를 함께 저장하여 빠르게 원하는 정보를 찾을 수 있다. (set 이나 map 등 활용)
  
</div>
</details>
<details>
<summary>데드락(교착상태)</summary>
  <br>
<div markdown="1">
    
  **둘 이상의 프로세스들이 자원을 점유한 상태에서 서로에게 자원을 요구하며 무한정 대기하는 현상**  
    
  
  프로세스가 자원을 얻지 못해서 다음 처리를 하지 못하는 상태이다.  
  시스템에서 한정된 자원을 여러 곳에서 사용하려고 할 때 발생한다.  
    
  멀티 프로그래밍 환경에서 한정된 자원을 얻기 위해 서로 경쟁하는 상황이 발생  
  한 프로세스가 자원을 요청했을 때, 동시에 그 자원을 사용할 수 없는 상황이 발생할 수 있음  
  이 때 프로세스는 대기 상태로 들어감  
  대기 상태로 들어간 프로세스들이 실행 상태로 변경될 수 없을 때 교착상태 발생  
    
  **발생조건**  
    
  
  **4가지 모두 성립해야 데드락 발생**  
  
    **1. 상호 배제(Mutual Extension)**    
    자원은 한번에 한 프로세스만 사용할 수 있다.  
    **2. 점유 대기(Hold and Wait)**  
    최소한 하나의 자원을 점유하고 있으면서 다른 프로세스에 할당되어 사용하고 있는 자원을 추가로 점유하기 위해 대기하는 프로세스가 존재해야 함  
    **3. 비선점(No Preemption)**  
    다른 프로세스에 할당된 자원은 사용이 끝날 때까지 강제로 뺏을 수 없음  
    **4. 순환 대기(Circular Wait)**  
    프로세스의 집합에서 순환 형태로 자원을 대기하고 있어야 함  
    
  **데드락 처리**  
    
    **1.예방(Prevention)**  
    교착 상태 발생 조건 중 하나를 제거하여 해결한다.  
    **2.회피(Avoidance)**  
    교착상태가 발생할 가능성을 배제하지 않고 교착상태 발생 시 적절히 피해 가는 방법    
    은행원 알고리즘  
      
    **3.탐지(Detection)**  
    시스템에 교착상태가 발생했는지 점검하여 교착상태에 있는 프로세스와 자원을 발견하는 것이다.  
    교착상태 발견 알고리즘와 자원 할당 그래프를 통해 탐지 과정에서 오버헤드 발생  
  
    **4.회복(Recovery)**  
    교착 상태를 일으킨 프로세스를 종료하거나, 할당된 자원을 해제시켜 회복시키는 방법  
    
  
    교착 상태의 프로세스를 모두 중지하거나, 교착 상태가 제거될 때가지 하나씩 프로세스 중지  
    교착상태에 있는 프로세스가 점유하고 있는 자원을 선점하여 일시정지 시키고 다른 프로세스에게 자원을 할당  
  
    
  
  
</div>
</details>
<details>
<summary>은행원 알고리즘</summary>
  <br>
<div markdown="1">
  
  프로세스가 자원을 요청하면 시스템이 안전상태에 머무르게 되는지 판단하고 안전하다면 자원을 할당한다.  
    
  안전상태 : 시스템이 교착상태를 일으키지 않으면서 각 프로세스가 요구한 최대 요구량만큼 자원을 할당해 줄 수 있는 상태로 안전 순서열이 존재하는 상태
</div>
</details>
<details>
<summary>기아상태</summary>
  <br>
<div markdown="1">
  
  특정 프로세스가 우선 순위가 낮아 잦원을 계속 할당받지 못하는 상태이다. 
  
</div>
</details>
<details>
<summary>식사하는 철학자 문제</summary>
  <br>
<div markdown="1">
  
  데드락 상태를 설명하기 위한 문제이다.  
  모든 철학자가 동시에 자신의 왼쪽 포크를 잡는다면, 모든 철학자들이 자기 오른쪽 포크가 사용 가능할 때까지 기다려야 한다.  
  모든 철학자들은 영원히 오른쪽 포크를 기다린다.  
  
</div>
</details>
