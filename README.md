# 인터뷰
<details>
<summary>객체지향이란?</summary>
<br>
<div markdown="1">

객체지향이란 현실 세계를 프로그래밍으로 옮겨와 현실의 사물이나 개념에서 필요한 정보를 추출하여 상태와 행위를 가진 객체를 만들고, 객체들 간의 상호작용을 통해 로직을 구성하는 프로그래밍 방법입니다.
</div>
</details>

<details>
<summary>객체지향의 특징</summary>
<br>
<div markown="1">

객체지향의 대표적인 특징으로는 캡슐화, 추상화, 상속, 다형성이 있습니다.  
캡슐화는 코드의 재사용과 정보 은닉을 위한 특징으로 속성과 기능들을 클래스라는 캡슐에 넣는 것이라고 볼 수 있습니다. 이후에는 접근제어자를 통해 외부에서의 접근을 통제합니다.  
추상화는 객체의 공통된 속성들 중 필요한 부분을 하나의 집합으로 만들어 내는 것입니다. 현실의 객체들은 매우 복잡하기 때문에 추상화를 통해 복잡도를 낮추고 필요한 속성들만 추출합니다.  
상속은 자식 클래스가 부모 클래스의 속성과 기능을 물려 받는 것입니다.  
다형성은 한 타입의 참조 변수로 여러 타입의 객체를 참조할 수 있도록 하는 것입니다. 부모 클래스 타입의 참조 변수로 자식 클래스의 인스턴스를 참조할 수 있는 것입니다. 오버로딩과 오버라이딩을 통해 구현할 수 있습니다.
</div>
</details>

<details>
<summary>객체지향 설계 원칙</summary>
<br>
<div markdown="1">
	
객체지향 설계 원칙에는 5가지 대표적인 원칙이 있습니다.  
단일책임원칙(SRP) : 객체는 단 하나의 책임만 가져야 한다. -> 응집도는 높게, 결합도는 낮게  
개방폐쇄원칙(OCP) : 확장에는 열려있고, 변경에는 닫혀 있어야 한다. -> 기존의 코드는 수정이 일어나지 말아야 하며, 쉽게 확장이 가능해야 한다.  
리스코프치환원칙(LSP) : 부모 클래스의 인스턴스 대신 자식 클래스의 인스턴스를 사용해도 프로그램은 정상 작동해야 한다.  
인터페이스분리원칙(ISP) : 사용하지 않는 인터페이스에 대해 영향을 받지 않아야 한다. -> 각각의 기능들은 독립된 인터페이스로 구현하며, 서로 영향을 주지 않도록 설계해야 한다.  
의존역전원칙(DIP) : 변화하기 쉬운 것보다 어려운 것에 의존해야 한다. -> 변화가 쉬운 것은 구체화된 클래스, 어려운 것은 인터페이스나 추상 클래스를 의미한다.   
</div>
</details>

<details>
<summary>객체지향 장점</summary>
<br>
<div markdown="1">

코드의 재사용성이 높습니다. 객체를 부품처럼 바꿔 사용할 수 있기 때문입니다. 또 객체 단위로 나눠 개발을 한 뒤에 나중에 객체들간의 관계만 설정 해주면 되기 때문에 대규모 프로젝트에 적합합니다. 그리고 절차지향에 비해 코드 수정이 편리하기 때문에 유지보수가 용이합니다.
</div>
</details>

<details>
<summary>객체지향 단점</summary>
<br>
<div markdown="1">

절차지향보다 속도면에서 좀 더 느리고 설계 단계에서 많은 시간이 들게 되는 것입니다.
</div>
</details>

<details>
<summary>클래스란?</summary>
<br>
<div markdown="1">

추상화를 거쳐 공통적인 속성과 행위를 변수와 메소드로 정의한 것 입니다. 객체를 만들기 위한 틀이라고 볼 수 있습니다.
</div>
</details>

<details>
<summary>인스턴스란?</summary>
<br>
<div markdown="1">

클래스에서 정의한 것을 토대로 실제 메모리에 할당된 것입니다. 
</div>
</details>

<details>
<summary>자바의 특징</summary>
<br>
<div markdown="1">

자바는 대표적인 객체지향 언어이며 JVM 위에서 실행하기 때문에 운영체제에 독립적입니다. 또 GC를 통해 자동으로 메모리 관리가 됩니다. 그리고 운영체제 지원 없이 멀티 쓰레드를 자체적으로 지원합니다. 또 동적 로딩을 지원합니다. 
</div>
</details>

<details>
<summary>운영체제 독립적이라는 말이 무슨 뜻인가요?</summary>
<br>
<div markdown="1">

운영체제에 독립적이라는 것은 개발 환경과 배포 환경이 다를 경우 프로그램을 재컴파일 할 필요 없이 실행 가능함을 뜻합니다.
</div>
</details>

<details>
<summary>동적 로딩이란?</summary>
<br>
<div markdown="1">

자바는 애플리케이션 실행 시 모든 객체가 생성되지 않고, 객체가 필요한 시점에 클래스를 동적 로딩하여 생성합니다. 이러한 동적 로딩은 일부 클래스 변경 시 전체를 다시 컴파일 하지 않아도 된다는 장점이 있지만 정적 로딩에 비해 속도가 느릴 수 있습니다. 이 부분에 대해서 자바는 static 키워드를 지원하여 보완합니다.
</div>
</details>

<details>
<summary>JVM이란?</summary>
<br>
<div markdown="1">

JVM은 운영체제 위에서 동작하는 프로세스로 자바 바이트 코드를 해당 운영체제가 이해할 수 있는 기계어로 바꿔 실행하는 역할을 하는 자바 가상 머신입니다. 또한 Garbage Collection 을 수행하는 주체입니다. 자바는 JVM 으로 인해 운영체제에 종속되지 않고 메모리 관리 또한 자동으로 됩니다. 
</div>
</details>

<details>
<summary>JVM 동작 흐름</summary>
<br>
<div markdown="1">

프로그램이 실행되면 JVM 은 운영체제로 부터 필요한 메모리를 할당 받습니다. JVM은 이 메모리를 용도에 따라 여러 영역으로 나누어 관리합니다.  
자바 컴파일러가 자바 코드를 바이트코드로 변환시킵니다. 변환된 class 파일들을 클래스 로더를 통해 JVM 메모리 영역으로 로딩합니다.  
로딩된 class 파일들은 실행 엔진을 통해 해석됩니다.  
해석된 바이트 코드는 메모리 영역에 배치되어 실질적인 수행이 이루어집니다.
</div>
</details>

<details>
<summary>JVM 구성요소</summary>
<br>
<div markdown="1">

Class Loader : JVM 내로 클래스를 로드하고 링크를 통해 배치하는 작업을 수행하는 모듈입니다.  
Execution Engine : 런타임 데이터 영역에 배치된 바이트 코드를 실행시키는 역할을 합니다.  
Garbage Collectior : Garbage Collection 을 수행합니다.  
Runtime Data Areas : JVM이 운영체제에게서 할당 받은 메모리 영역입니다. 
</div>
</details>

<details>
<summary>자바의 메모리 영역은?</summary>
<br>
<div markdown="1">

메소드 영역, 스택 영역, 힙 영역, 상수 풀 등이 있습니다. 
</div>
</details>

<details>
<summary>메소드 영역이란?</summary>
<br>
<div markdown="1">

JVM 이 읽어들인 클래스와 인터페이스에 대한 런타임 상수 풀, 멤버 변수, 클래스 변수, 생성자와 메소드를 저장하는 영역입니다.
</div>
</details>

<details>
<summary>Runtime Constant Pool</summary>
<br>
<div markdown="1">

JVM 은 런타인 상수 풀을 통해 해당 메소드나 필드의 실제 메모리 상 주소를 찾아 참조한다.
</div>
</details>

<details>
<summary>스택 영역</summary>
<br>
<div markdown="1">

지역변수, 함수 등이 올라가는 LIFO 방식의 메모리 영역입니다. 기본 타입 변수는 스택 영역에 값을 저장하지만 참조 타입 변수는 주소를 저장합니다.
</div>
</details>

<details>
<summary>힙 영역</summary>
<br>
<div markdown="1">

new 연산자를 통해 동적 할당된 객체들이 저장되는 메모리 영역입니다. GC에 의해 메모리가 관리 되는 영역이기도 합니다. 참조가 없는 객체는 의미 없는 객체로 판단되어 GC의 대상이 됩니다.
</div>
</details>

<details>
<summary>자바 컴파일</summary>
<br>
<div markdown="1">

자바 소스를 자바 컴파일러를 통해 컴파일합니다. 컴파일 결과로 자바 바이트 코드 .class 파일이 생성됩니다. 해당 class 파일은 클래스 로더를 통해 JVM 런타임 데이터 영역에 저장됩니다. 그 다음 실행 엔진을 통해 명령어 단위로 실행됩니다.
</div>
</details>

<details>
<summary>컴파일 / 인터프리터 설명해주세요</summary>
<br>
<div markdown="1">

컴파일러는 작성된 코드를 한 번에 기계어로 번역합니다. 최초 번역 이후에는 실행 파일이 생성되어 다음 실행에서는 속도가 빠릅니다. 반면에 인터프리터는 한 줄 단위로 번역을 하기 때문에 번역 속도는 컴파일러보다 빠르지만 실행 속도는 상대적으로 느립니다.  
또한 컴파일러는 플랫폼에 종속적이지만, 인터프리터는 그렇지 않습니다.  
</div>
</details>

<details>
<summary>JIT 컴파일러란?</summary>
<br>
<div markdown="1">

인터프리터 방식의 단점을 보완하기 위해 도입된 방식입니다. 실행 시점에 인터프리터 방식으로 번역하면서 해당 코드를 캐싱하여 동일한 부분이 호출되는 경우 캐싱해둔 코드를 불러다 사용하는 방식입니다. 중복되는 코드마저 매번 번역하는 인터프리터 방식의 단점을 보완하여 기존 인터프리터 방식보다 빠르게 동작합니다. 자바는 예전에는 인터프리터 방식을 사용하였지만 현재는 인터프리터 방식과 JIT 방식을 함께 사용한다고 알고 있습니다.
</div>
</details>

<details>
<summary>Call by Value / Call by Reference</summary>
<br>
<div markdown="1">

Call by Value 는 인자의 값을 복사하여 처리하는 방식입니다. 메소드 내의 처리 결과는 메소드 밖의 변수에 영향을 주지 않습니다. 인자를 복사하여 사용하기 때문에 메모리 사용량이 증가합니다.  
Call by Reference 는 인자의 주소를 참조하여 직접 값에 영향을 주는 방식입니다. 복사를 하지 않고 직접 참조하기 때문에 속도가 빠르고 메모리를 적게 사용하지만 원본이 변경될 수 있다는 위험이 있습니다.  
자바는 항상 Call by Value 로 값을 넘깁니다. 레퍼런스 타입을 인자로 넘기는 경우에는 주소 값을 복사하여 사용합니다. 따라서 원본 객체의 프로퍼티에는 접근 가능하나 원본 객체 자체를 변경하는 것은 불가능합니다.
</div>
</details>

<details>
<summary>Primitive type / Reference type</summary>
<br>
<div markdown="1">

기본형 타입은 선언과 동시에 초기화 되어야 합니다. 또한 비객체이기에 null 을 값으로 가질 수 없고 제네릭타입으로 쓰일 수 없습니다. 
</div>
</details>

<details>
<summary>자바 컴파일</summary>
<br>
<div markdown="1">


</div>
</details>

<details>
<summary>자바 컴파일</summary>
<br>
<div markdown="1">


</div>
</details>

<details>
<summary>자바 컴파일</summary>
<br>
<div markdown="1">


</div>
</details>

<details>
<summary>자바 컴파일</summary>
<br>
<div markdown="1">


</div>
</details>

<details>
<summary>자바 컴파일</summary>
<br>
<div markdown="1">


</div>
</details>

<details>
<summary>자바 컴파일</summary>
<br>
<div markdown="1">


</div>
</details>

<details>
<summary>자바 컴파일</summary>
<br>
<div markdown="1">


</div>
</details>

<details>
<summary>자바 컴파일</summary>
<br>
<div markdown="1">


</div>
</details>







## 자바의 특징
#### 1. 객체지향 언어
객체지향 개념의 특징인 상속, 캡슐화, 다형성, 추상화가 잘 적용된 언어이다.
#### 2. 운영체제에 독립적
자바는 JVM 위에서 실행되기 때문에 운영체제에 독립적입니다. 운영체제에 독립적이라는 것은 개발 환경과 배포 환경이 다를 경우, 프로그램을 다시 컴파일 할 필요 없이 실행 가능함을 뜻합니다.
#### 3. 자동 메모리 관리
자바에서는 JVM이 지속적으로 메모리를 감시하면서 더 이상 사용되지 않는 메모리를 해지시켜 줍니다.
#### 4. 멀티쓰레드 지원
자바는 하나의 프로그램에서 여러 개의 쓰레드가 동시에 실행할 수 있는 환경을 지원합니다. C/C++ 는 운영체제의 도움을 받아 멀티 쓰레드를 수행하지만, 자바는 운영체제에 지원 없이 멀티쓰레드 프로그래밍이 가능합니다.

#### 5. 동적 로딩을 지원
자바는 애플리케이션 실행 시 모든 객체가 생성되지 않고, 객체가 필요한 시점에 클래스를 동적 로딩하여 생성합니다. 동적 로딩은 클래스 일부를 변경 시 클래스 전체를 다시 컴파일 하지 않아도 된다는 장점이 있습니다. 하지만 정적 로딩에 비해 속도가 느릴 수 있고 이를 해결하기 위해 자바에서는 static 키워드를 지원합니다.
## 자바의 장점
- #### 운영체제에 독립적입니다.
	JVM위에서 동작하기 때문에, 특정 운영체제에 종속되지 않습니다.
- #### 대표적인 객체지향언어입니다.
	캡슐화, 상속, 추상화, 다형성 등을 지원해주기 때문입니다.
- #### 자동으로 메모리 관리를 해준다.
	JVM에서 Garbage Collector라고 불리는 Demon Thread에 의해 GC(Garbage Collection)가 일어납니다. GC로 인해 별도의 메모리 관리가 필요 없으며, 비즈니스 로직에 집중할 수 있습니다.
## JVM
- #### JVM이란?  
	자바를 운영체제에 독립적일 수 있게 해주는 자바 가상머신 입니다. JVM은 운영체제 위에서 동작하는 프로세스로 자바 코드를 컴파일한 바이트 코드를 해당 운영체제가 이해할 수 있는 기계어로 바꿔 실행하는 역할을 합니다. 또한 Garbage Collection을 수행합니다.
	- Garbage Collection이란?  
	시스템에서 더 이상 사용하지 않는 동적 할당된 메모리 블록이나 객체를 찾아 자동적으로 다시 사용 가능한 자원으로 회수하는 것입니다. JVM이 메모리가 부족해지면 운영체제에 추가적인 메모리를 요청할 때 Garbage Collection이 실행됩니다. 
- #### JVM 동작 흐름
	1. 실행될 클래스 파일을 메모리에 로드 후 초기화 작업을 수행합니다.
	2. 메소드와 멤버 변수들을 해당 메모리 영역에 배치합니다.
	3. 클래스 로드가 끝난 후 JVM 은 main 메소드를 찾아 변수들을 스택에 쌓습니다.
	4. 함수 호출, 객체 할당 등 상황에 맞는 작업을 수행합니다.
- #### JVM 구성요소
	- ##### Class Loader
		JVM 내로 클래스를 로드하고 링크를 통해 배치하는 작업을 수행하는 모듈입니다. 런타임 시에 동적으로 클래스를 로드합니다.
	- ##### Execution Engine
		Class Loader를 통해 JVM 내의 런타임 데이터 영역에 배치된 바이트 코드를 실행시킵니다. 이 때 자바 바이트 코드를 명령어 단위로 읽어 실행합니다. 
	- ##### Garbage Collector
		Garbage Collection 을 수행한다.
	- ##### Runtime Data Areas
		JVM이 운영체제 위에서 실행되면서 할당 받는 메모리 영역입니다. Class Loader에서 준비한 데이터들을 보관합니다.
## 자바의 메모리 영역
- #### 메소드 영역  
	JVM이 읽어들인 클래스와 인터페이스에 대한 런타임 상수 풀, 멤버 변수(필드), 클래스 변수(static 변수), 생성자와 메소드를 저장하는 영역입니다.
- #### Runtime Constant pool
	JVM은 런타임 상수 풀을 통해 해당 메소드나 필드의 실제 메모리 상 주소를 찾아 참조한다.
- #### 메소드 영역/런타임 상수 풀의 사용기간 및 쓰레드 공유 범위
	- JVM 시작 부터 프로그램 종료 혹은 명시적 null 선언 시 까지 유효합니다.
	- 모든 쓰레드에서 공유합니다.
- #### 스택 영역  
	지역변수, 함수 등이 올라가는 LIFO 방식의 메모리 영역입니다.
	기본 타입 변수는 스택 영역에 값을 저장하지만 참조 타입 변수는 객체의 주소를 저장합니다.
- #### 힙 영역  
	new 연산자를 통해 동적 할당된 객체들이 저장되는 메모리 영역입니다. GC에 의해 메모리가 관리 됩니다. 힙 영역에 생성된 객체나 배열은 스택 영역의 변수나 다른 객체의 필드에서 참조합니다. 참조가 없다면 의미 없는 객체가 되어 GC의 대상이 됩니다.
## 자바에서의 바이트 코드
- 자바에서 코드를 컴파일하면 바이트 코드(.class) 형태로 출력됩니다. 컴파일 된 바이트 코드는 JVM에 의해 런타임 시 운영체제가 이해 가능한 기계어로 변경되어 실행됩니다.
- 이 과정 때문에 다른 컴파일 언어보다 속도가 느리다는 단점이 있습니다.
## 객체지향 프로그래밍 (OOP, Oriented Object Programming)
- #### 객체지향이란?  
	객체지향이란 현실 세계를 프로그래밍으로 옮겨와 현실 세계의 사물이나 개념들을 객체로 보고, 그 객체로부터 개발하고자 하는 특징과 기능을 추출하여 프로그래밍하는 기법입니다.
- #### OOP 설계 5 원칙(SOLID)  
	- ##### SRP(Single Responsibility Principle, 단일 책임 원칙)  
		클래스는 단 하나의 목적을 가져야 하며, 클래스를 변경 하는 이유 또한 하나의 이유여야 한다는 원칙입니다.  
		-> 객체는 단 하나의 책임만 가져야 한다.
	- ##### OCP(Open-Closed Principle, 개방-폐쇠 원칙)  
		클래스는 확장에는 열려있고 변경에는 닫혀 있어야 한다는 원칙입니다.  
		-> 기존의 코드를 변경하지 않고 기능을 추가할 수 있도록 설계해야 한다.
	- ##### LSP(Liskov Subtitution Principle, 리스코프 치환 원칙)  
		상위 타입의 객체를 하위 타입의 객체로 바꾸어도 프로그램은 일관되게 동작해야 한다는 원칙입니다.  
		-> 자식 클래스는 최소한 자신의 부모 클래스의 기능을 수행할 수 있어야 한다.
	- ##### ISP(Interface Segregation Principle, 인터페이스 분리 원칙)  
		클라이언트는 사용하지 않는 메소드에 의존하지 않도록 인터페이스를 분리해야 한다는 원칙입니다.  
		-> 인터페이스를 클라이언트에 특화되도록 분리시켜야 한다.
	- ##### DIP(Dependency Inversion Principle, 의존 역전 법칙)  
		클라이언트는 추상화에 의존해야 하며, 구체화에 의존하면 안된다는 원칙입니다. 여기서 말하는 추상화는 인터페이스, 구체화는 구현된 클래스라고 볼 수 있습니다.  
		-> 고수준 모듈은 저수준 모듈의구현에 의존해서는 안된다. 변화하기 어려운 것에 의존하라.
- #### OOP에서 시스템은 상호작용하는 자율적인 객체들의 공동체이며, 자율적인 객체랑 상태와 행위를 함께 지니며 스스로 자기 자신을 책임지는 객체를 의미합니다.
- #### OOP의 특징
	- #####  추상화(모델링)  
		OOP는 현실 세계의 객체를 프로그래밍으로 옮겨오는 과정에서 복잡성을 극복하기 위해 추상화를 거칩니다. 추상화란 어떤 양상, 세부 사항, 구조 등의 객체의 특성을 필요에 따라 의도적으로 생략하거나 감춤으로 복잡도를 낮추는 방법입니다. (객체의 공통된 속성들 중 필요한 부분을 포착해서 클래스로 정의하는 설계 기법)
	- #####  캡슐화(정보은닉)  
		외부에 노출할 필요가 없는 정보들을 은닉하는 것을 의미합니다. 외부 객체는 내부 객체가 제공하는 정보와 기능 외에는 접근할 수 없게 함으로써 내부 객체의 손상을 방지합니다. 자바에서는 접근 제한자를 통해 캡슐화된 멤버에 대한 노출 여부를 정의합니다.  
	- ##### 상속 
		자식 클래스가 부모 클래스의 속성을 물려 받는 것을 의미합니다. 코드의 재사용성을 높이고 유지보수를 용이하게 해주는 특성입니다. 자바에서의 특징으로는 다중 상속을 허용하지 않는 것입니다. 
	- ##### 다형성 
		하나의 객체가 여러가지 타입을 가질 수 있는 것을 의미합니다. 자바에서는 한 레퍼런스 변수가 다른 형태의 객체를 참조할 수 있음을 말합니다. 오버로딩, 오버라이딩, 업캐스팅, 다운캐스팅 등의 방법으로 자바에서 다형성을 구현할 수 있습니다. ( 자식 클래스에서 메소드를 오버라이딩하고 자식 클래스 객체를 부모 타입으로 업캐스팅한다. 업캐스팅 된 부모 타입의 객체에서 자식 클래스의 멤버를 참조하여 다형성을 구현한다.)
	
	
- #### OOP의 장점
	- 코드 재사용이 용이합니다.  
	클래스를 재사용하거나 상속을 통해 확장해서 사용이 가능하기 때문에 재사용성이 높아집니다.
	- 유지보수가 용이합니다.  
	클래스나 메소드 단위의 수정을 통해 코드의 변경이 용이하기 때문입니다.
	- 대형 프로젝트에 적합합니다.  
	클래스 단위의 모듈로 개발을 할 수 있어 업무 분담이 용이하기 때문입니다.
	- 신뢰성 높은 프로그래밍이 가능합니다.  
	접근 제어자를 통해 데이터를 보호하고, 메소드를 통해 코드의 중복을 제거하여 코드의 불일치로 인한 오작동을 방지할 수 있기 때문입니다.
- #### OOP의 단점
	- 처리속도가 상대적으로 느립니다.
	- 설계 단계에서 많은 시간이 소모됩니다.
## 인터프리터와 컴파일러
- #### 컴파일러(번역기)
	컴파일러는 사람이 작성한 고급 언어를 한번에 기계어로 번역합니다. 한 줄 단위로 번역하는 인터프리터 방식보다 번역 시간을 오래 걸리지만, 한 번 번역을 하면 실행 파일이 생성되어 다음에 실행할 때 기존에 생성된 실행 파일을 사용하기 때문에 인터프리터에 비해 실행 시간이 빠른 편입니다.
- #### 인터프리터(실행기)
	인터프리터는 한 줄 단위로 번역을 하기 때문에 번역 속도는 컴파일러보다 빠릅니다. 하지만 매번 실행할 때마다 번역을 하기 때문에 컴파일러를 사용하는 언어보다 실행 속도가 느린  편 입니다.
- #### 컴파일러는 플랫폼에 종속적이지만, 인터프리터는 모든 플랫폼에 종속되지 않습니다.
	컴파일러는 실행 파일을 만들 때 해당 환경에 맞게 변환을 하기 때문에 기존 환경과 호환되는 환경에서만 작동되기 때문입니다. 
## JIT 컴파일러
- #### JIT 컴파일러란?
	컴파일 방식과 인터프리터 방식을 혼합한 방식이라 볼 수 있습니다. 실행 시점에서 인터프리터 방식으로 기계어 코드를 생성하면서 해당 코드를 캐싱하여 동일 함수가 여러 번 불릴 때 매번 기계어 코드를 생성하는 것을 방지합니다. 반복되는 코드들을 컴파일 하는 방식이라 생각할 수 있습니다. 자바는 플랫폼에 대한 유연성을 위해 이러한 방식을 택한 것 같습니다.
## 접근제어자
- #### public
	어떤 클래스에서든 접근이 가능합니다.
- #### private
	동일 클래스 내에서만 접근이 가능합니다.
- #### protected
	동일 패키지나 상속 관계에 있는 하위 클래스에서만 접근 가능합니다.
- #### package
	동일 패키지 내에서만 접근이 가능합니다.
## Wrapper Class
- #### Wrapper Class란?
	기본 타입의 데이터를 객체로 취급해야 하는 경우 기본 타입을 객체로 변환해주는 클래스입니다.
- #### Boxing / UnBoxing
	Boxing : 기본형 -> 객체  
	UnBoxing : 객체 -> 기본형  
	JDK1.5 부터는 자바 컴파일러가 박싱/언박싱을 자동으로 처리 해줍니다.
## 추상클래스와 추상메소드
- #### 추상메소드
	추상메소드란 선언부만 존재하고 구현부가 작성되어 있지 않은 메소드입니다. 자식 클래스에서 반드시 오버라이딩해야 사용할 수 있습니다. 
- #### 추상클래스
	하나 이상의 추상메소드를 포함하는 클래스를 추상클래스라고 합니다. 추상클래스를 상속하는 자식클래스는 추상메소드를 오버라이딩 해야 하며 추상클래스는 인스턴스를 생성할 수 없습니다. 추상클래스는 추상메소드의 포함을 제외하면 일반 클래스와 모든 점이 같습니다.
## Interface
- #### Interface란?
	일종의 추상클래스입니다. 자바는 다중 상속을 지원하지 않는데 이를 보완하기 위해 인터페이스로 다중 상속을 구현합니다. 인터페이스는 오로지 추상메소드와 상수만을 포함할 수 있습니다. 인터페이스는 클래스가 아니기 때문에 인스턴스를 생성할 수 없습니다. 동일한 동작을 위해 구현을 강제화 시키는 기능을 합니다. 
## 오버로딩과 오버라이딩
- #### 오버로딩
	같은 이름의 메소드를 여러 개 정의 하는 것입니다.  
	매개변수의 타입이나 개수가 달라야 하며, 리턴 타입은 오버로딩에 영향을 주지 않습니다.
- #### 오버라이딩
	부모 클래스의 메소드를 자식 클래스에서 재정의 하는 것을 말합니다.
## Call By Value / Call By Reference
- #### Call By Value
	인자로 받은 값을 복사하여 처리하는 방식입니다. 넘어온 값을 변경해도 기존의 값은 변경되지 않습니다. 메모리 사용량이 늘어난다는 단점이 있습니다.
- #### Call By Reference
	인자로 받은 값의 주소를 참조하여 직접 값에 영향을 주는 방식입니다. 값을 복사하지 않고 직접 참조하기 때문에 속도가 빠릅니다.
- #### 자바는?
	자바는 Call By Value 입니다. 매개변수로 넘어가는 기본 타입은 값을, 참조 타입은 주소 값을 복사합니다. 
## Parameter / Argument
- #### Parameter
	함수를 선언할 때 사용된 변수
- #### Argument
	함수가 호출되었을 때 함수의 파라미터로 전달된 실제 값
