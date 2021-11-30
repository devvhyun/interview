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
https://gyoogle.dev/blog/computer-language/Java/Java%20Virtual%20Machine.html  
https://gyoogle.dev/blog/computer-language/Java/Garbage%20Collection.html
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

기본형 타입은 논리형, 문자형, 정수형, 실수형이 있습니다. 또한 비객체이기에 null 을 값으로 가질 수 없고 제네릭타입으로 쓰일 수 없습니다. 기본형을 객체로 사용하려면 래퍼 클래스를 사용해야 합니다.  
자바에서 기본형을 제외한 나머지는 모두 참조형입니다. Object 클래스를 상속하는 모든 클래스를 의미합니다. 클래스 타입, 인터페이스 타입, 배열 타입, 열거 타입이 있습니다.
</div>
</details>

<details>
<summary>== 와 eqauls()</summary>
<br>
<div markdown="1">

동등연산자는 참조하는 주소 값을 비교합니다. 값이 같더라도 주소 값이 다르면 false 를 반환합니다.  
equals() 는 단순히 값을 비교합니다.  
리터럴로 생성한 문자열의 경우는 String pool에 저장되기 때문에 같은 값을 가진 문자열의 경우 같은 주소를 가지게 됩니다. 그래서 동등연산자로 비교가 가능합니다. 하지만 new 연산자를 통해 생성한 문자열은 값이 같더라도 다른 주소를 가지게 됩니다.
</div>
</details>

<details>
<summary>오토박싱 / 언박싱</summary>
<br>
<div markdown="1">

기본형 데이터를 래퍼 클래스로 객체로 만드는 동작을 박싱이라 합니다.  
언박싱은 반대로 래퍼 클래스를 기본형으로 변환하는 동작입니다.  
jDK 1.5 부터는 자바 컴파일러가 박싱과 언박싱이 필요한 상황에 박싱과 언박싱을 자동으로 처리해줍니다.  
이를 오토박싱, 언박싱이라 합니다.
</div>
</details>

<details>
<summary>직렬화란?</summary>
<br>
<div markdown="1">

자바 시스템 내부에서 사용되는 객체 또는 데이터를 외부의 자바 시스템에서도 사용할 수 있도록 바이트 형태로 변환하는 기술입니다.  
운영체제마다 서로 다른 가상 메모리 주소 공간을 갖기 때문에 레퍼런스 타입의 데이터들은 인스턴스를 전달 할 수 없습니다. 이를 해결하기 위해 직렬화를 거치게 됩니다. 직렬화된 데이터들은 모두 기본형이 되고, 이는 파일 저장이나 네트워크 전송 시 파싱이 가능한 유의미한 데이터가 됩니다. 이러한 과정을 직렬화라고 합니다.  
</div>
</details>

<details>
<summary>String, StringBuffer, StringBuilder</summary>
<br>
<div markdown="1">

String은 불변적입니다. 문자열 연산을 하는 경우 새로 객체를 만들어야 하기 때문에 연산이 적고 조회가 많은 경우 효율적입니다.  
StringBuffer 와 StringBuilder 모두 가변적입니다. 문자열 연산의 경우 새로 객체를 만들지 않고도 수정이 가능합니다. 하지만 StringBuidler 는 Thread-safe 하지 않기 때문에 문자열 연산이 많고 멀티 쓰레드인 경우는 StringBuffer, 싱글 쓰레드인 경우는 StringBuidler 를 사용하는 것이 좋습니다. 
</div>
</details>

<details>
<summary>캐스팅이란?</summary>
<br>
<div markdown="1">

형변환입니다. 형변환은 묵시적 형변환과 명시적 형변환이 있는데 이 중 묵시적 형변환은 업캐스팅, 명시적 형변환은 다운캐스팅입니다. 자식은 부모의 모든 속성을 가지고 있기 때문에 업스팅의 경우 캐스팅을 명시해주지 않아도 자등으로 캐스팅이 됩니다. 이를 묵시적 형변환이라 합니다. 
</div>
</details>

<details>
<summary>프로세스란?</summary>
<br>
<div markdown="1">

운영체제에서 실행중인 하나의 프로그램입니다. 프로세스는 하나 이상의 쓰레드를 포함합니다.
</div>
</details>

<details>
<summary>쓰레드란?</summary>
<br>
<div markdown="1">

프로세스 내에서 동시에 실행되는 독립적인 실행 단위를 말합니다. 하나의 작업 단위라고 생각할 수 있습니다.  
https://gyoogle.dev/blog/computer-language/Java/Thread.html
</div>
</details>
<details>
<summary>멀티쓰레딩이란?</summary>
<br>
<div markdown="1">

멀티쓰레딩이란 하나의 프로세스 안에 여러개의 쓰레드가 동시에 작업을 수행하는 것을 말합니다.
</div>
</details>

<details>
<summary>에러와 익셉션의 차이</summary>
<br>
<div markdown="1">

https://gyoogle.dev/blog/computer-language/Java/Error%20&%20Exception.html
</div>
</details>
# 인터뷰

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
	- Garbage Collection(GC)이란?  
	시스템에서 더 이상 사용하지 않는 동적 할당된 메모리 블록이나 객체를 찾아 자동적으로 다시 사용 가능한 자원으로 회수하는 것입니다. JVM이 메모리가 부족해지면 운영체제에 추가적인 메모리를 요청할 때 Garbage Collection이 실행됩니다. GC 를 수행하는 부분을 Garbage Collector 라 부릅니다.
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
	OOP는 프로그래밍 패러다임 중 하나로, 프로그래밍에서 필요한 데이터를 추상화시켜 상태와 행위를 가진 객체를 만들고 그 객체들 간의 유기적인 상호작용을 통해 로직을 구성하는 프로그래밍 방법이다.
- #### 클래스와 인스턴스
	- ##### 클래스
		어떤 문제를 해결하기 위한 데이터를 만들기 위해 추상화를 거쳐 집단에 속하는 속성과 행위를 변수와 메소드로 정의한 것입니다. 객체를 만들기 위한 틀 이라고 볼 수 있습니다.
	- ##### 인스턴스
		클래스에서 정의한 것을 토대로 실제 메모리에 할당된 것입니다. 
- #### OOP에서 시스템은 상호작용하는 자율적인 객체들의 공동체이며, 자율적인 객체랑 상태와 행위를 함께 지니며 스스로 자기 자신을 책임지는 객체를 의미합니다.
- #### OOP의 특징
	- #####  추상화(모델링)  
		OOP는 현실 세계의 객체를 프로그래밍으로 옮겨오는 과정에서 복잡성을 극복하기 위해 추상화를 거칩니다. 추상화란 어떤 양상, 세부 사항, 구조 등의 객체의 특성을 필요에 따라 의도적으로 생략하거나 감춤으로 복잡도를 낮추는 방법입니다. (객체의 공통된 속성들 중 필요한 부분을 포착해서 클래스로 정의하는 설계 기법)
	- #####  캡슐화(정보은닉)  
		기능과 특성의 모음을 클래스라는 캡슐에 분류해서 넣은 것을 캡슐화라고 볼 수 있습니다. 캡슐화의 목적은 코드를 재수정 없이 재활용하는 것과 접근 제어자를 통한 정보 은닉에 있습니다. 관련된 기능과 특성을 한데 모음으로써 객체 재활용이 원활해졌고 접근 제어자를 통해 접근을 제한함으로써 코드 변경 시 영향 범위를 예측하기 수월해졌습니다. 
	- ##### 상속 
		부모 클래스의 속성과 기능을 물려받아 사용할 수 있게 하고, 기능의 일부를 변경해야 할 경우 자식클래스에서 해당 기능을 재정의하여 사용할 수 있게 하는 것입니다. 코드의 재사용성을 높이고 유지보수를 용이하게 해주는 특성입니다. 자바에서의 특징으로는 다중 상속을 허용하지 않는 것입니다. 
	- ##### 다형성 
		하나의 객체가 여러가지 타입을 가질 수 있는 것을 의미합니다. 자바에서는 한 레퍼런스 변수가 다른 형태의 객체를 참조할 수 있음을 말합니다. 오버로딩, 오버라이딩, 업캐스팅, 다운캐스팅 등의 방법으로 자바에서 다형성을 구현할 수 있습니다. ( 자식 클래스에서 메소드를 오버라이딩하고 자식 클래스 객체를 부모 타입으로 업캐스팅한다. 업캐스팅 된 부모 타입의 객체에서 자식 클래스의 멤버를 참조하여 다형성을 구현한다.)  
		하나의 변수명, 함수명 등이 상황에 따라 다른 의미로 해석될 수 있는 것입니다. 
	
	
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
## 인터페이스
- #### 인터페이스란?
	일종의 추상클래스입니다. 자바는 다중 상속을 지원하지 않는데 이를 보완하기 위해 인터페이스로 다중 상속을 구현합니다. 인터페이스는 오로지 추상메소드와 상수만을 포함할 수 있습니다. 인터페이스는 클래스가 아니기 때문에 인스턴스를 생성할 수 없습니다.
## 인터페이스와 추상클래스
- #### 차이점
	추상클래스는 is a (~이다), 인터페이스는 has a(~을 할수 있는) 입니다. 추상클래스의 목적은 상속을 받아서 기능을 확장시키는 것이고 인터페이스의 목적은 구현하는 클래스들에 대해 특정한 메소드가 반드시 존재하도록 강제하여 구현 객체들의 같은 동작을 보장하는 것입니다. 또한 추상클래스는 일반 메소드를 가질 수 있지만, 인터페이스는 추상메소드와 상수만 가질 수 있다.
- #### 공통점
	new 연산자로 인스턴스 생성이 불가합니다. 추상클래스는 미완성된 클래스, 인터페이스는 클래스가 아니기 때문입니다. 둘 다 추상메소드를 갖고 있습니다. 해당 추상메소드를 사용하기 위해서는 하위 클래스에서 확장 또는 구현을 해야 합니다.
## 오버로딩과 오버라이딩
- #### 오버로딩
	같은 이름의 메소드를 여러 개 정의 하는 것입니다.  
	매개변수의 타입이나 개수가 달라야 하며, 리턴 타입은 오버로딩에 영향을 주지 않습니다.
- #### 오버라이딩
	부모 클래스의 메소드를 자식 클래스에서 재정의 하는 것을 말합니다.
## Call By Value / Call By Reference
- #### Call By Value
	인자로 받은 값을 복사하여 처리하는 방식입니다.  메소드 내의 처리 결과는 메소드 밖의 변수에 영향을 주지 않습니다. 복사하는 방식이기 때문에 메모리 사용이 증가한다는 단점이 있습니다. 
- #### Call By Reference
	인자로 받은 값의 주소를 참조하여 직접 값에 영향을 주는 방식입니다. 값을 복사하지 않고 직접 참조하기 때문에 속도가 빠릅니다.
- #### 자바는?
	자바는 Call By Value 입니다. 매개변수로 넘어가는 기본 타입은 값을, 참조 타입은 주소 값을 복사합니다. 
## 원시형과 참조형
- #### 원시형(Primitive type)
	변수에 값 자체를 저장합니다.(정수형, 실수형, 문자형, 논리형) 래퍼 클래스를 통해 객체로 변환할 수 있습니다. 제네릭 타입 사용 불가
- #### 참조형(Reference type)
	객체의 주소를 저장합니다.
##  Thread
- #### Process
	운영체제에서 실행중인 하나의 프로그램입니다. 하나 이상의 쓰레드를 포함합니다.
- #### Thread
	프로세스 내에서 동시에 실행되는 독립적인 실행 단위를 말합니다. 자원을 많이 사용하지 않고 구현이 쉬우며 범용성이 높습니다. 
	- ##### 장점
		빠른 프로세스 생성  
		적은 메모리 사용  
		쉬운 정보 공유
	- ##### 단점
		교착상태에 빠질 수 있습니다.
	- ##### Dead Lock (교착상태)
		다중 프로그래밍 체제에서 하나 또는 그 이상의 프로세스가 수행할 수 없는 어떤 특정 시간을 기다리고 있는 상태입니다. 
## 싱글톤
- #### 싱글톤 패턴이란?
	애플리케이션이 시작될 때 최초 한번만 메모리를 할당하고, 그 메모리에 인스턴스를 만들어서 사용하는 디자인패턴입니다. 생성자가 여러번 호출되더라도 실제로 생성되는 하나이고, 최초 생성 이후에 호출된 생성자는 기존의 생성된 객체를 반환합니다. (자바에서는 생성자를 private 선언하고 getInstance() 메소드를 선언하는 방식을 주로 사용한다.) 즉 싱글톤 패턴이란 단 하나의 인스턴스를 생성해 전역적으로 공유하여 사용하는 디자인 패턴입니다.
## Parameter / Argument
- #### Parameter
	함수를 선언할 때 사용된 변수
- #### Argument
	함수가 호출되었을 때 함수의 파라미터로 전달된 실제 값
## 컬렉션 프레임워크
- #### 컬렉션 프레임워크란?
	다수의 데이터를 쉽고 효과적으로 처리할 수 있는 표준화된 방법을 제공하는 클래스의 집합을 의미합니다. 즉 데이터를 저장하는 자료 구조와 데이터를 처리하는 알고리즘을 구조화하여 클래스로 구현해 놓은 것입니다.
- #### 주요 인터페이스
	- ##### List 인터페이스
		순서가 있는 데이터의 집합, 데이터의 중복을 허용합니다.  
		ArrayList, LinkedList, Stack, Vector 등이 있습니다.
	- ##### Set 인터페이스
		순서를 유지하지 않는 데이터의 집합, 데이터의 중복을 허용하지 않습니다.  
		HashSet, TreeSet 등이 있습니다.
	- ##### Map 인터페이스
		키와 값의 쌍으로 이루어진 데이터의 집합입니다.  
		순서는 유지되지 않으며, 키는 중복을 허용하지 않지만 값은 중복을 허용합니다.
	List 와 Set 인터페이스는 모두 Collection 인터페이스를 상속받지만, 구조상의 차이로 인해 Map 인터페이스는 별도로 정의됩니다. 
## 디자인 패턴
TODO
## String, StringBuilder, StringBuffer
- #### String
	불변입니다. 한번 생성이 되면 변경이 불가능 합니다. 그렇기 때문에 문자열의 변경이 잦은 경우 String 사용은 비효율적일 수 있습니다. 힙 메모리에 임시 가비지가 생성되어 힙 메모리가 부족할 수 도 있기 때문입니다.
- #### StringBuffer
	가변입니다. StringBuffer 는 동기화 키워드를 지원하여 멀티쓰레드 환경에서 안전합니다.
- #### StringBuilder
	가변입니다. StringBuilder 는 동기화를 지원하지 않기 때문에 멀티쓰레드 환경에서 사용하는 것은 적합하지 않지만, 그 만큼 단일쓰레드에서의 성능은 StringBuffer 보다 뛰어납니다.
## 프레임워크와 라이브러리
- #### 프레임워크
	프레임워크는 뼈대나 기반 구조를 뜻하는데 제어의 역전 개념이 적용된 대표적인 기술입니다. 애플리케이션 개발 시 필수적인 코드, 알고리즘, 데이터베이스 연동 등과 같은 기능들을 위해 어느 정도 뼈대를 제공해주는 것입니다. 개발자는 이 뼈대 위에서 코드를 작성하여 애플리케이션을 완성합니다. 객체 지향 개발을 하면서 겪을 수 있는 통합성, 일관성 부족의 문제를 해결하는 방법 중 하나입니다.  
	(소프트웨어의 특정 문제를 해결하기 위해서 상호 협력하는 클래스와 인터페이스의 집합)
- #### 라이브러리
	라이브러리는 특정 기능에 대한 도구나 함수들을 모아 놓은 집합입니다. 즉 개발자가 개발하는데 필요한 것들을 모아둔 것이라 할 수 있습니다.  
	(단순 활용이 가능한 도구들의 집합)
- #### 프레임워크 vs 라이브러리
	둘의 가장 큰 차이는 흐름에 대한 제어 권한이 어디에 있느냐 입니다. 프레임워크는 전체적인 흐름을 자체적으로 가지고 있으며, 개발자가 그 흐름 안에서 코드를 작성하는 반면에 라이브러리는 개발자가 흐름에 대한 제어를 하며 필요한 상황에 가져다 쓰는 것입니다. 한마디로 프레임워크에는 제어의 역전이 적용되어 있습니다.
- #### 제어의 역전(IOC)
	어떠한 일을 하도록 만들어진 프레임워크에 제어의 권한을 넘김으로써 클라이언트 코드가 신경써야 할 것을 줄이는 전략입니다. 일반적으로 개발자가 Main 함수를 정의하고 애플리케이션의 시작 지점을 정합니다. 이렇게 프로그램의 흐름을 개발자가 제어하는 것이 일반적인 흐름입니다.  
	하지만 프레임워크는 이와 반대로 실행의 흐름을 프레임워크가 가지고 있습니다. 개발자는 프레임워크에 맞춰 개발을 진행합니다. 이런식으로 제어의 권한을 프레임워크에게 넘기기 때문에 이를 제어의 역전이라고 합니다.
## AJAX
- #### AJAX란?
	자바스크립트를 사용한 비동기 통신, 클라이언트와 서버간에 xml 데이터를 주고받는 기술입니다. 자바스크립트를 통해서 서버에 데이터를 요청하고 응답 받는 방식입니다.
## 에러와 예외
- #### Error
	메모리 부족, 스택오버플로우와 같이 발생하게 되면 복구할 수 없는 심각한 오류입니다.
- #### 예외
	덜 심각한 오류라고 말할 수 있습니다. 발생하더라도 프로그램이 무조건 종료되지 않으며 예외처리를 통해 프로그램 종료를 막고 개발자가 처리할 수 있습니다. 
## Getter / Setter
	getter와 setter 메소드를 통해 접근하기 때문에 메소드 안에서 매개변수 같이 올바르지 않은 입력이나 접근에 대해 사전에 제한하거나 처리 할 수 있습니다.
## 서블릿
- #### 서블릿이란?
	클라이언트의 요청을 처리하고, 그 결과를 반환하는 Servlet 클래스의 구현 규칙을 지킨 자바 웹 프로그래밍 기술입니다. 
- #### 서블릿 특징
	- 클라이언트의 요청에 대해 동적으로 작동하는 웹 어플리케이션 컴포넌트
	- html 을 사용하여 요청에 응답한다.
	- 자바 Thread를 이용하여 동작한다.
	- MVC 패턴에서 Controller로 이용된다.
	- http 프로토콜 서비스를 지원하는 javax.servlet.http.HttpServlet 클래스를 상속받는다.
	- UDP 보다 처리 속도가 느리다.
	- html 변경시 재컴파일해야 한다.
- #### 동작 방식
	1. 클라이언트가 url 을 입력하면 http request 가 servelt container 로 전송한다.
	2. 요청을 전송받은 servlet container는 HttpServletRequest, HttpServletResponse 객체를 생성한다.
	3. web.xml 을 기반으로 사용자가 요청한 url 이 어느 서블릿에 대한 요청인지 찾는다.
	4. 해당 서블릿에서 service 메소드를 호출한 후 클라이언트의 GET,POST 여부에 따라 doGet() 또는 doPost()를 호출한다.
	5. 응답이 끝나면 HttpServletRequest, HttpServletResponse 두 객체를 소멸시킨다.
- #### 서블릿 컨테이너
	서블릿을 관리해주는 역할을 담당합니다. 서블릿 컨테이너는 클라이언트의 요청을 받아주고 응답할 수 있도록 웹서버와 소켓으로 통신합니다. 대표적으로 톰캣이 있습니다. 톰캣은 실제로 웹 서버와 통신하여 jsp와 servlet이 작동하는 한경을 제공해줍니다.
- #### JSP
	자바 코드가 들어가 있는 html 코드를 말합니다. 서블릿은 자바 코드 속에 html 코드가 들어가는 형태인데 이와 반대로 JSP 는 html 속에 자바 코드가 들어간 구조입니다. 
## GET / POST 차이
	http는 웹에서 클라이언트와 서버간의 요청과 응답을 데이터로 주고 받을 수 있는 프로토콜입니다. 클라이언트가 http 프로토콜을 통해 서버에게 요청을 보내면 서버는 요청에 맞는 응답을 클라이언트에게 전송을 하게 됩니다. http 요청에 포함되는 http 메소드는 서버가 요청을 수행하기 위해 해야할 행동을 표시하는 용도로 사용됩니다.
- #### GET
	서버로부터 정보를 조회하기 위해 설계된 메소드입니다. GET 방식으로 요청을 하는 경우 데이터를 쿼리스트링을 통해 전달합니다. 전달되는 데이터는 url에 노출됩니다. 그래서 페이지 정보 등의 민감하지 않은 정보를 전달할 때 주로 사용합니다.
- #### POST
	리소스를 변경하거나 생성하기 위한 메소드입니다. GET 방식과 달리 전송해야할 데이터를 http 메시지의 body 에 담아 전송합니다. 요청 헤더 타입을 명시해야 합니다. body 는 데이터 길이의 제한이 없고 url 에 노출되지 않습니다. GET 방식보다 많은 양의 데이터를 좀 더 안전하게 전송할 수 있습니다. 하지만 POST 요청 또한 개발자도구 같은 툴로 데이터를 확인할 수 있기 때문에 민감한 데이터의 경우는 별도의 암호화를 하는 것이 적절합니다.  
## == / equals 차이
- #### ==
	주소값을 비교합니다. 같은 값이더라도 참조하고 있는 주소 값이 다르면 false
- #### equals
	단순히 값을 비교합니다.
리터럴 "" 으로 생성한 문자열은 String pool 에 저장됩니다. 그래서 이미 같은 문자열로 생성된 값이 있다면 같은 값을 참조하게 됩니다. 따라서 같은 문자열이라면 == 비교시 true를 반환합니다.  
new 연산자를 통해 생성된 문자열은 풀이 아닌 힙 영역에 저장됩니다.
