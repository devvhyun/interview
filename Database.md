## Database
<details>
  <summary>무결성(Integrity)</summary>
  <br>
  <div markdown="1">
  
  **데이터의 무결성**  
      
데이터의 정확성, 일관성, 유효성이 유지되는 것을 말한다. 데이터의 무결성을 유지하는 것은 데이터베이스 관리시스템의 
    중요한 기능이며 4가지 종류의 무결성이 있다.  
      
  **1.개체 무결성**  
      
  모든 테이블이 기본키를 가져야 한다.  
      
  **2.참조 무결성**  
      
  참조 관계에 있는 두 테이블의 데이터가 항상 일관된 값을 갖도록 유지되는 것을 말한다.  
      
  **3.도메인 무결성**  
      
  테이블에 존재하는 필드의 무결성을 보장하기 위한 것으로 조건을 정의하고 입력 데이터의 유효성을 검사한다.  
   주민등록번호 필드에 알파벳이 입력되는 경우 도메인 무결성이 깨지는 경우라 볼 수 있다.  
      
  **4.무결성 규칙**  
      
  데이터의 무결성을 지키기 위한 모든 제약사항을 맒한다. 데이터베이스 전체에 공통적으로 적용되는 규칙이다.  
    
  </div>
</details>


<details>
  <summary>Key</summary>
  <br>
  <div markdown="1">
  
  **Key 의 역할**  
    1. 테이블 내의 튜플(레코드)를 식별해주는 역할  
    2. 테이블 간의 관계를 설정하고 식별하게 해주는 역할  
      
  **후보키(Candidate Key)**  
      
    테이블에서 튜플을 고유하게 식별하는 속성의 집합이다.  
    기본키가 될 수 있는 키들이다.
    PK 는 후보키 중에서 선택된다.  
    (Null 값을 포함할 수 없음)  
      
  **기본키(Primary Key)**  
      
    테이블의 모든 튜플을 고유하게 식별하는 속성 혹은 속성의 집합이다.  
    중복될 수 없다.  
    테이블에는 기본키가 하나여야 한다.  
    (Null 값을 포함할 수 없음)  
      
  **대체키(Alternate Key, 보조키)**  
      
    후보키 중 기본키로 선정되지 않는 키들을 대체키라 한다.  
      
  **외래키(Foreign Key)**  
      
    두 테이블 사이의 관계를 만드는 키이다.  
    다른 테이블의 기본키를 참조할 때 두 테이블 간의 상호 참조 역할을 한다.  
    (Null 값이 허용됨)  
      
    (참조 무결성을 보장하기 위한 기능)
    RESTRICTED: 레코드를 변경 또는 삭제하고자 할 때 해당 레코드를 참조하고 있는 개체가 있다면, 변경 또는 삭제 연산을 취소한다.  
    CASCADE: 레코드를 변경 또는 삭제하면, 해당 레코드를 참조하고 있는 개체도 변경 또는 삭제된다.  
    SET NULL: 레코드를 변경 또는 삭제하면, 해당 레코드를 참조하고 있는 개체의 값을 NULL로 설정한다.  
      
  **복합키(Compound Key, Composite Key)**  
      
    특정 레코드를 고유하게 식별할 수 있는 속성이 두 개 이상 있을수 있다.  
    다른 속성과 결합 시 복합 키의 조합이 고유해진다.  
      
  **대리키(Surrogate Key)**  
      
    기본키를 인공적으로 만든 키이다.  
    대리키는 보통 정수이며 아무 의미를 갖지 않는다. (ex 시퀀스)  
    pk로 설정할 속성이 없거나 너무 복잡한 경우 사용한다.  
    
    
  </div>
</details>


<details>
  <summary>DBMS(Database Management System)</summary>
  <br>
  <div markdown="1">
  
   데이터베이스 관리시스템을 말한다.  
    사용자가 데이터에 관한 정보를 효율적이고 편리하게 구성, 복원 및 검색을 할 수 있도록 하는 
    응용프로그램의 모음을 말한다.  
    MySql, Oracle 등이 있다.
  </div>
</details>

<details>
  <summary>DBMS 장점</summary>
  <br>
  <div markdown="1">
  
 1. 데이터가 구조적으로 저장되며 중복이 제거 된다.  
  2. 입력한 데이터의 유효성을 검사하고 데이터베이스에 대한 무단 액세스를 방지한다.  
  3. 데이터의 백업 및 복구를 제공한다.  
  4. 사용자 인터페이스를 제공한다.
  </div>
</details>

<details>
  <summary>RDBMS (관계형 데이터베이스 시스템)</summary>
  <br>
  <div markdown="1">
  
 현재 가장 많이 사용되고 있는 데이터베이스의 한 종류이다.  
    행과 열로 이루어진 각각의 테이블을 고유키로 참조하여 서로 종속되는 관계를 
    표현하는 데이터베이스 구조를 관계형 데이터베이스라 한다.
  </div>
</details>

<details>
  <summary>관계형 데이터베이스의 특징</summary>
  <br>
  <div markdown="1">
  
 1. 데이터의 분류, 정렬, 탐색 속도가 빠르다.  
  2. 오랫동안 사용된 만큼 신뢰성이 높고 어떤 상황에서도 데이터의 무결성을 보장한다.  
  3. 기존의 작성된 스키마를 수정하기 어렵다.
  </div>
</details>

<details>
  <summary>SQL</summary>
  <br>
  <div markdown="1">
  
   데이터베이스와 통신하기 위한 언어로 DDL, DML, DCL 크게 세 가지로 나뉜다.  
      
  **DDL**  
    데이터 정의어로 데이터 구조를 정의하는데 사용되는 명령어들이다.  
    create, alter, drop, rename, truncate 등이 있다.  
      
  **DML**  
    데이터 조작어로 데이터를 조회하거나 조작할 때 사용되는 명령어들이다.  
    select, update, insert, delete 등이 있다.  
      
  **DCL**  
    액세스 권한 부여, 취소 등 데이터의 가시성을 제어하는데 사용되는 명령어들이다.  
    grant, revoke 등이 있다.
  </div> 
</details>

<details>
  <summary>정규화(Nomalization)</summary>
  <br>
  <div markdown="1">
  
   자료의 손실이나 불필요한 정보의 추가 없이 데이터의 일관성 확보 및 데이터의 중복을 회소화하고 
    데이터의 안정성 확보를 위해 테이블을 분할하는 작업이다.  
      
  **1정규화**  
    테이블의 컬럼이 원자값을 갖도록 테이블을 분리시킨다.  
      
  **2정규화**  
    테이블의 모든 컬럼이 완전 함수적 종속을 만족시키도록 테이블을 분리시킨다.  
    (기본키의 부분집합 키가 결정자가 되어서는 안된다는 의미이다.)  
      
  **3정규화**  
   2정규화가 진행된 테이블에서 이행적 종속관계를 없애기 위해 테이블을 분리 시킨다.  
    **이행적 종속** : a->b , b->c, a->c 인 관계 ( b->c 를 별도의 테이블로 분리)
  </div>
</details>

<details>
  <summary>정규화의 목적</summary>
  <br>
  <div markdown="1">
  
 1.저장 공간 최소화  
  2. 데이터 무결성 유지  
  3. 이상 현상 제거
  </div>
</details>

<details>
  <summary>정규화의 문제점</summary>
  <br>
  <div markdown="1">
  
   릴레이션 분해로 인해 릴레이션 간의 join 연산이 많아진다.  
    이로 인해 응답 시간이 느려질 수 있다.
  </div>
</details>

<details>
  <summary>이상현상(Anormaly)</summary>
  <br>
  <div markdown="1">
  
   **1. 삽입이상**  
      
    불필요한 데이터를 추가해야만 삽입이 가능한 상황  
      
  **2. 갱신이상**  
      
    중복된 데이터 중 일부만 수정되어 데이터 모순이 일어나는 상황  
      
  **3. 삭제이상**  
      
    어떤 데이터를 삭제할 때 다른 필요한 데이터까지 삭제되는 상황
  </div>
</details>

<details>
  <summary>인덱스</summary>
  <br>
  <div markdown="1">
  
   인덱스는 데이터베이스 테이블에 대한 검색 성능을 높여주는 자료구조이다.  
    특정 컬럼에 인덱스를 생성하면 해당 컬럼의 데이터들을 정렬하여 별도의 메모리 공간에 
    데이터의 물리적 주소와 함께 저장된다.  
    이를 통해 인덱스에 저장된 물리적 주소로가서 데이터를 가져오는 방식으로 검색 속도를 향상시킨다.
  </div>
</details>

<details>
  <summary>인덱스 장점</summary>
  <br>
  <div markdown="1">
  
   인덱스의 가장 큰 특징은 데이터들이 정렬되어 있다는 것이다.  
    이를 통해 조건 검색 영역에서 강점이 나타난다.  
      
  **1.조건 검색 where 절의 효율성**  
    -> 이미 정렬되어 있기 때문에 풀스캔을 하지 않고 해당 조건을 빠르게 검색 가능하다.  
      
  **2. 정렬 order by 절의 효율성**  
    -> 이미 정렬되어 있기 때문에 order by 에 의한 sort 과정을 생략할 수 있다.  
      
  **3. MIN, MAX 의 효율적인 처리**  
    -> 풀스캔을 하지 않고 양 끝 데이터만 가져오면 최대, 최소 값을 구할 수 있다.
  </div>
</details>

<details>
  <summary>인덱스 단점</summary>
  <br>
  <div markdown="1">
  
 가장 큰 문제점은 정렬을 계속 유지해야 한다는 것이다.  
      
  insert, update, delete 시 테이블 내에 있는 데이터들을 재정렬해야 한다.  
  인덱스 테이블, 원본 테이블 두 테이블을 모두 수정해야한다.  
      
  인덱스 사용을 위해서는 10% 정도의 추가적인 저장공간이 필요하다.
  </div>
</details>

<details>
  <summary>인덱스를 사용하면 좋은 경우</summary>
  <br>
  <div markdown="1">
  
  1. 전체 데이터 중 10~15% 이하의 데이터를 처리하는 경우  
  2. where 절에서 자주 사용되는 column  
  3. 외래키가 사용되는 column  
  4. join에 자주 사용되는 column
  </div>
</details>

<details>
  <summary>인덱스 사용을 피해야 하는 경우</summary>
  <br>
  <div markdown="1">
  
  1. data 중복도가 높은 column  
  2. DML 이 자주 일어나는 column  
    ->insert : 블로킹 발생, delete : 삭제가 아닌 사용안됨 표시 (인덱스 테이블과 원본 테이블의 불일치)
  </div>
</details>

<details>
  <summary>인덱스 자료구조</summary>
  <br>
  <div markdown="1">
  
  **B*Tree**  
      
    일반적으로 사용되는 인덱스 알고리즘은 B-Tree 알고리즘이다.  
    컬럼의 값을 변경하지 않고 원래의 값을 이용해 인덱싱하는 방식이다.  
      
  **Hash**  
      
    컬럼의 값으로 해시 값을 계산해서 인덱싱하는 방식이다.  
    O(1) 의 검색속도를 가지지만 기존의 값을 변경해서 인덱싱하기 때문에 문자열의 전방일치 같이 
    값의 일부분으로 검색하는 것이 불가능하다.  
      
  **B Tree vs Hash**  
      
    단순히 데이터에 대한 접근 속도는 Hash 가 빠르지만 select 쿼리의 연산에는 부등호 연산도 포함된다.  
    Hash 의 경우 등호 연산에 특화되어 있기 때문에 데이터베이스의 자료구조로는 적합하지 않다.  
    
  </div>
</details>

<details>
  <summary>데이터베이스 뷰</summary>
  <br>
  <div markdown="1">
  
  허용된 데이터를 제한적으로 보여주기 위해 하나 이상의 테이블에서 유도한 가상 테이블이다.  
      
  **장점**  
    1. 뷰의 데이터가 저장되는 물리적 위치가 없으므로 리소스를 낭비하지 않고 테이블 출력이 가능하다.  
    2. 삽입, 수정, 삭제 같은 명령어를 허용하지 않기 때문에 데이터 엑세스가 자동으로 제한된다.  
      
  **단점**  
    1. 해당 뷰와 관련된 테이블을 삭제할 경우 뷰도 영향을 받는다.  
    2. 큰 테이블에 대해 뷰를 만들 때 더 많은 메모리가 사용된다.  
    
  </div>
</details>

<details>
  <summary>ER Model</summary>
  <br>
  <div markdown="1">
  
  개념적 데이터 모델의 가장 대표적인 모델이다.  
    개체, 속성 이들간의 관계를 통해 개념 세계의 정보 구조를 표현한다.  
      
    **1. 개체(Entity)**  
      
    개체는 현실 세계에 존재하는 실체를 의미하며 하나 이상의 속성으로 구성된다.  
      
    **2. 개체 타입(Entity Type)**  
      
    같은 특성을 갖고있는 개체들의 집합이다.  
      
    **3. 개체 집합(Entity Set)**  
      
    특정 유형을 갖는 개체들의 집합이다.  
      
    **4. 관계**  
      
    여러 개체들간의 연관성이다.  
      
    **5. 관계 타입**  
      
    같은 관계들의 집합, 개체 타입들간의 연관성이다.  
      
    **6. 차수 **  
      
    관계에 참여하는 개체 타입들의 개수이다. N항 관계라 표현한다.  
      
    **7. 카디널리티**  
      
    관계에 참여하는 개체의 개수이다.  
      
    **8. 속성**  
      
    개체 또는 관계에 대한 특성이나 상태를 기술하는 데이터 항목이다.  
    
  </div>
</details>

<details>
  <summary>트랜잭션(Transcation)</summary>
  <br>
  <div markdown="1">
  
  데이터베이스의 상태를 변화시키기 위해 수행하는 작업의 단위이다.  
      
    ex)  
    a가 b에게 만원을 송금하는 경우,  
    a 계좌에서 만원을 차감, b 계좌에서 만원을 증가시키는 두 개의 update 쿼리가 실행된다.  
    두 작업 모두 완료되어야 송금이라는 작업이 성공적으로 완료된 것이다.  
    두 개의 update 쿼리를 하나의 트랜잭션으로 관리한다.  
      
  **트랜잭션의 상태**  
      
  **1.Active** : 트랜잭션이 실행중인 상태  
  **2.Faild** : 트랜잭션이 실패한 상태  
    **3.Partially Committed** : Commit 명령이 도착한 상태  
    **4.Comitted** : Commit 이 완료된 상태  
    **5.Aborted** : 트랜잭션 취소 후, 이전 상태로 돌아간 상태  
      
  **트랜잭션의 특징 ACID**  
      
    **1.원자성(Atomicity)  
      
    트랜잭션 연산이 데이터베이스에 모두 반영되거나, 모두 반영되지 않아야한다.  
      
    **2.일관성(Consistency)**  
      
    트랜잭션의 처리 결과는 항상 데이터베이스의 일관성을 보장해야 한다.  
      
    **3.독립성(Isolation)**  
      
    트랜잭션이 수행되고 있을 때, 다른 트랜잭션의 연산 작업이 기존 트랜잭션의 작업에 영향을 주지 못해야 한다.  
      
    **4.지속성(Durability)**  
      
    트랜잭션이 성공적으로 완료되면, 그 결과는 영구적으로 데이터베이스에 반영되어야 한다.
  </div>
</details>

<details>
  <summary>트랜잭션 격리 수준(Isolation Level)</summary>
  <br>
  <div markdown="1">
  
  Lock 을 통해 트랜잭션의 독립성을 보장하는데 무조건적인 Lock 은 데이터베이스의 성능을 저하시킬 수 있다.  
    그렇기 때문에 Lock 의 범위를 조절해야 하는데 이 때의 범위를 격리 수준이라 한다.  
      
  **1. level 0 (Read Uncommitted)**  
      
  select 쿼리가 수행되는 동안 해당 데이터에 **shared lock 이 걸리지 않는다.**  
    트랜잭션이 처리 중이거나, 아직 커밋되지 않은 데이터를 다른 트랜잭션이 읽는 것을 허용한다.  
    -> 일관성 유지가 불가능하다. Dirty Read 발생  
      
  **2. level 1 (Read Committed)**  
      
  select 쿼리가 수행되는 동안 해당 데이터에 **shared lock 이 걸린다.**  
    트랜잭션이 수행되는 동안 다른 트랜잭션이 접근할 수 없어 대기하게 된다.  
    커밋이 이루어진 트랜잭션만 조회가 가능하다.  
    Oracle, Sql server 의 default isolation level  
    -> Non-Repeatable Read 발생
      
  **3. level 2 (Repeatable Read)**  
      
  트랜잭션이 완료될 때까지 select 쿼리가 사용하는 **모든 데이터에 shared lock 이 걸린다.**  
    트랜잭션이 범위 내에서 조회한 데이터가 항상 동일함을 보장한다.  
    다른 사용자는 트랜잭션 영역에 해당되는 데이터에 대한 **수정**이 불가능하다.  
    Mysql 의 default  
    -> Phantom Read 발생  
      
  **4. level 3 (Serializable)**  
      
  트랜잭션이 완료될 때까지 select 쿼리가 사용하는 **모든 데이터에 shared lock 이 걸린다.**  
    완벽한 읽기 일관성 모드를 제공한다.  
    다른 사용자는 트랜잭션 영역에 해당되는 데이터에 대한 **수정 및 입력**이 불가능하다.
      
      
  ** 낮은 단계의 격리 수준을 적용할 때 발생하는 현상**  
      
  **Dirty Read**  
      
  완료되지 않은 트랜잭션에 의한 변경사항을 보게되는 경우  
      
  **Non-Repeatable Read**  
      
  한 트랜잭션 내에서 동일한 두 쿼리의 결과가 다르게 나타나는 경우  
      
  **Phantom Read**  
      
  한 트랜잭션 안에서 일정 범위의 레코드를 두 번 이상 읽었을때, 없던 레코드가 나타나는 현상
  </div>
</details>

<details>
  <summary>join</summary>
  <br>
  <div markdown="1">
  
  2개 이상의 테이블에서 조건에 맞는 데이터를 추출하기 위해 사용하는 명령어이다.  
    **Inner Join** : 2개 이상의 테이블에서 교집합만 추출  
    **Left Join** : 2개 이상의 테이블에서 from 에 해당하는 부분을 추출  
    **Right Join** : 2개 이상의 테이블에서 from 과 join 하는 테이블에 해당하는 부분을 추출  
    **Outer Join** : Full Join 이라고도 불린다. 2개 이상의 테이블에서 합집합을 추출  
      
  Inner) SELECT user.name, course.name FROM user INNER JOIN course ON user.course=course.id;  
  Left) SELECT user.name, course.name FROM user LEFT JOIN course ON user.course=course.id;  
  Right) SELECT user.name, course.name FROM user RIGHT JOIN course ON user.course=course.id;  
  Outer) SELECT user.name, course.name FROM user OUTER JOIN course ON user.course=course.id;  
  </div>
</details>

<details>
  <summary>NoSql</summary>
  <br>
  <div markdown="1">
  
  관계형 데이터 모델을 지양하며 대량의 분산된 데이터를 저장하고 조회하는데 특화되었으며 스키마 없이 사용 가능하거나 
    느슨한 스키마를 제공하는 저장소를 말한다.  
    분산형 구조를 통해 여러 대의 서버에 분산 저장이 가능하다.  
      
  **특징**  
      
  1. 스키마가 없다.  
  2. join 이 불가능하다.  
  3. 트랜잭션을 지원하지 않는다.  
  4. 분산처리(수평적 확장)의 기능을 쉽게 제공한다.  
      
  **저장 방식에 따른 NoSql 분류**  
      
  **1.key-value model**  
      
  ex) Redis  
    가장 기본적인 형태의 NoSql 이며 키 하나로 데이터 하나를 저장하고 조회할 수 있는 단일 키-값 구조를 가지고 있다.  
    단순한 저장구조로 인해 복잡한 조회 연산을 지원하지 않으며 고속 읽기와 쓰기에 최적화된 경우가 많다.  
      
  **2.document model**  
      
  ex)MongoDB  
    key-value 모델을 개념적으로 확장한 구조이며 하나의 키에 하나의 구조화된 문서를 저장하고 조회한다.  
    저장된 문서를 컬렉션으로 관리하며 문서 ID 에 대한 인덱스를 사용하여 O(1) 시간 안에 문서를 조회할 수 있다.  
    읽기와 쓰기의 비율이 7:3 정도일 때 최고의 성능을 보인다.  
      
  **3.column model**  
      
  ex) 구글의 빅테이블  
    하나의 키에 여러 개의 컬럼 이름과 컬럼 값의 쌍으로 이루어진 데이터를 저장하고 조회한다.  
    모든 컬럼은 항상 타임스탬프 값과 함께 저장된다.  
    대부분 쓰기에 더 특화되어 있다.
  </div>
</details>

<details>
  <summary>교착상태</summary>
  <br>
  <div markdown="1">
  
 두 개 이상의 트랜잭션이 특정 자원의 락을 획득한 채 다른 트랜잭션이 소유하고 있는 락을 요구하는 경우의 발생한다.  
    아무리 기다려도 상태가 변경되지 않는 경우를 교착상태라 한다.  
      
  **교착 상태를 줄이는 방법**  
      
  **1. 트랜잭션을 자주 커밋한다.**  
  **2. 정해진 순서로 테이블에 접근한다. **  
  **3. 읽기 잠금 획득의 사용을 피한다. **
  </div>
</details>

<details>
  <summary>Statement vs PreparedStatement</summary>
  <br>
  <div markdown="1">
  
   속도면에서 PreparedStatement 가 더 빠르다. 쿼리를 수행하기 전에 이미 쿼리가 컴파일 되어 있으며, 반복 수행의 경우 
    프리 컴파일된 쿼리를 사용하기 때문이다.  
      
  Statement 는 보통 정적 쿼리에 사용되고 PreparedStatement 는 동적 쿼리에 사용된다.  
    PreparedStatement 가 파싱 타임을 줄여주지만 동적 쿼리를 사용하는데 따르는 성능 저하는 있다.
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

