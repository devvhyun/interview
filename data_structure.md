## 자료구조
<details>
  <summary>선형자료구조</summary>
  <div markdown="1">
    
  하나의 자료 뒤에 하나의 자료가 존재하는 것이다.  
  자료들 간의 앞 뒤 관계가 1:1의 선형관계  
  배열, 리스트, 스택, 큐 등
  </div>
</details>
<details>
  <summary>비선형자료구조</summary>
  <div markdown="1">
    
  하나의 자료 뒤에 여러개의 자료가 존재할 수 있는 것이다.  
  자료들 간의 앞 뒤관계가 1:n 또는 n:n 이다.  
  트리, 그래프 등 계층적 구조를 나타내기에 적합하다.  
  </div>
</details>
<details>
  <summary>Array</summary>
  <div markdown="1">
  
  Array는 연속된 공간에 데이터를 저장하는 선형자료구조이다.  
  인덱스를 통한 데이터 접근이 가능하다.  
  데이터 접근 시에는 O(1), 검색 시에는 O(N) 이다.   
  추가, 삭제 시에는 shift 가 발생하기 때문에 O(N)  
  **길이가 고정적이다.**  
  기본형과 참조형 모두 저장 가능하지만 하나의 배열에 한 가지 타입만 저장가능하다.  
  자바의 경우 length 를 통해 길이를 알 수 있다. O(1)    
  데이터의 변경이 적고 조회가 많은 경우에 효율적이다.
  </div>
 </details>
<details>
  <summary>ArrayList</summary>
  <div markdown="1">
  
  ArrayList는 배열과 마찬가지로 데이터를 연속된 공간에 저장하는 선형자료구조이다.  
  인덱스를 통한 접근이 가능하다.  
  데이터 접근 시에는 O(1), 검색 시에는 O(N) 이다.  
  추가, 삭제 시에는 shift 가 발생하기 때문에 O(N) 이다. (맨 뒤에 add() 인 경우 O(1))    
  **길이가 가변적이다.**  
  초기 크기를 지정하여 생성할 수 있으면 디폴트는 10 이다.  
  ArrayList 내부는 배열로 구현되어 있는데 capacity 라는 변수를 통해 자동으로 리사이징해준다.  
  데이터 삽입 시 배열의 크기가 capacity와 같아지면 기존 capacity *1.5 크기의 배열을 만들어 기존 배열을 복사한다.  
  참조형 타입의 데이터만 저장가능하며 여러 타입의 데이터를 저장할 수 있다.  
  (기본형 데이터를 저장할 수 있는 것은 오토박싱 때문이다.)  
  제네릭으로 타입을 지정할 수 있다.  
  데이터의 변경이 적고 조회가 많은 경우에 효율적이다.  
  (크기를 변경하지 않는다면 배열이 더 효율적이다.)
  </div>
 </details>
<details>
  <summary>Array vs ArrayList</summary>
  <div markdown="1">
  
  Array 와 ArrayList 모두 연속된 공간에 데이터를 저장하는 선형자료구조이다.  
  ArrayList 도 내부적으로는 배열로 구현되어 있다.  
  둘 다 인덱스를 사용할 수 있다.  
  접근 시에는 O(1), 검색 시에는 O(N), 추가, 삭제 시에는 O(N) 이 걸린다.  
  데이터의 변경이 적고 조회가 많은 경우 효율적인 자료구조이다.  
    
  가장 큰 차이점은 길이가 가변적인지 고정적인지이다.  
  Array 의 경우 길이가 고정적이고 ArrayList 는 가변적이다.  
  Array 는 다차원이 가능하지만 ArrayList 는 단일차원만 가능하다.  
  Array 는 기본형과 참조형 모두 저장 가능하지만, ArrayList 는 참조형만 저장 가능하다.  
  ArrayList 는 제네릭을 사용할 수 있다.  
  Array 는 length 프로퍼티를 통해 길이를 알 수 있고 ArrayList 는 size() 메소드를 통해 알 수 있다.
  </div>
 </details>
<details>
  <summary>LinkedList</summary>
  <div markdown="1">
  
  LinkedList 는 요소들간의 연결을 통해 리스트를 구현한 선형자료구조이다.  
  노드라 불리는 각 요소들은 데이터와 다음 노드의 주소를 가진 포인터로 이루어져 있다.  
  데이터에 대한 접근, 검색 시에는 순차 탐색이 이뤄지기 때문에 O(N)  
  추가, 삭제 시에는 연결된 노드만 수정하면 되기 때문에 O(1)    
  데이터의 변경이 잦은 경우 사용하면 효율적이다.
  </div>
 </details>
<details>
  <summary>Array vs LinkedList</summary>
  <div markdown="1">
  
  Array 는 임의 접근을 지원한다.  
  인덱스를 통해 요소들에 접근하며 O(1) 이다.  
  LinkedList 는 순차 탐색을 통해 요소에 접근하며 O(N) 이다. 
    
  Array 는 삽입, 삭제 시 shift 가 발생하여 O(N) 이다.  
  LinkedList 는 연결된 노드의 포인터만 수정하면 되기 때문에 O(1) 이다.  
  
  Array 는 컴파일 시 메모리에 할당이 되는 정적 메모리 할당이다.  
  LinkedList 는 요소가 추가, 삭제되는 런타임에 메모리에 할당되는 동적 메모리 할당이다.  
    
  Array 는 스택 영역에 메모리가 할당되며, LinkedList 는 힙 영역에 메모리가 할당된다.
    
  데이터의 변경이 적고 조회가 많은 경우 Array, 변경이 많고 조회가 적은 경우는 LinkedList 를 사용하는 것이 효율적이다.  
  LinkedList 는 데이터와 포인터를 저장하기 때문에 포인터라는 오버헤드가 발생한다.  
  </div>
 </details>
<details>
  <summary>ArrayList vs LinkedList</summary>
  <div markdown="1">
  
  ArrayList 는 길이가 가변적이나 내부적으로는 배열로 구현되어 있기 때문에 길이 변경 시 배열의 복사가 이뤄진다.  
  LinkedLisst 는 한 개의 노드에 다른 노드에 대한 참조만 가지고 있기 때문에 공간적 제약을 받지 않는다.  
    
  요소에 대한 접근 시에는 ArrayList 는 O(1), LinkedList 는 O(N) 이다.  
  추가 시에는 ArrayList 는 여유 공간이 있는 경우 O(1) 이지만 여유 공간이 없는 경우 O(N) 이다.  
  삽입, 삭제 시에는 ArrayList 는 shift 가 발생한다. LinkedList 는 연결된 노드의 포인터만 변경하면 된다. 
    
  LinkedList 는 데이터와 포인터를 저장하기 때문에 포인터라는 오버헤드가 발생한다.  
  
  </div>
 </details>
