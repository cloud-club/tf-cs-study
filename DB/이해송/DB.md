<details>
<summary>Q. 데이터베이스의 특징에 대해 설명해주세요.</summary>
<div markdown="1">

_**(DataBase)**_ :  특정 조직의 여러 사용자가 '공유'하여 사용할 수 있도록 '통합'해서 '저장'한 '운영' 데이터의 집합


- 실시간 접근성 : 수시적이고 비정형적 질의에 대해 실시간 처리에 의한 응답이 가능해야 합니다. 
- 계속적인 변화 : 데이터베이스의 상태는 동적이기에 새 데이터의 삽입, 삭제, 갱신으로 항상 최신의 데이터를 유지합니다. 
- 동시공용 : 다수의 사용자가 동시에 같은 내용의 데이터를 이용할 수 있어야 합니다. 
- 내용에 의한 참조 : 데이터 내용으로 데이터를 찾습니다.
- **데이터 공유** : 많은 사람들이 데이터를 공유할 수 있습니다.   
- **중복의 제거** : 데이터를 한 곳에 모으면서 중복되는 데이터를 제거할 수 있습니다.  
- **데이터 통합** : 흩어져 있는 데이터를 한 곳에 모을 수 있습니다.  
- **보안성** : 권한이 있는 관리자만이 데이터를 관리한다면 데이터의 보안을 지킬 수 있습니다.



</div>
</details>

<details>
<summary>Q. 데이터베이스 언어(DDL,DML,DCL) 에 대해 설명하라</summary>
<div markdown="1">

- DDL (Data Definition Language) : 객체의 생성, 변경, 삭제 명령어 create, alter, drop, rename 등 
- DML (Data Manipulation Language) : 제어 명령어, select , insert,update,delete 등 이 있다.
- DCL ( Data Control Language) : 객체 권한 부 등의 제어어, commit, rollback, grant, revoke 

</div>
</details>

<details>
<summary>Q.DBMS란?</summary>
<div markdown="1">

DB를 ‘데이터의 집합’이라고 정의한다면,   
이런 DB를 관리하고 운영하는 소프트웨어를 DBMS(Database Management System)라고 합니다.   
또한 응용프로그램들이 DB에 접근할 수 있는 인터페이스를 제공하고 복구기능과 보안성 기능을 제공합니다.


</div>
</details>


<details>
<summary>Q. DBMS 의 기능?</summary>
<div markdown="1">

**1) 정의(Definition) 기능**

: 모든 응용 프로그램들이 요구하는 데이터 구조를 지원하기 위해 데이터베이스에 저장될 데이터의 형(Type)과 구조에 대한 정의, 이용 방식, 제약 조건 등을 명시하는 기능입니다.

**2) 조작(Manipulation) 기능**

: 데이터 검색, 갱신, 삽입, 삭제 등을 체계적으로 처리하기 위해 사용자와 데이터베이스 사이의 인터페이스 수단을 제공하는 기능입니다.

**3) 제어(Control) 기능**

: 데이터베이스를 접근하는 갱신, 삽입, 삭제 작업이 정확하게 수행되어 데이터의 무결성이 유지되도록 제어해야 합니다. 정당한 사용자가 허가된 데이터에 접근할 수 있도록 보안을 유지하고 권한을 검사할 수 있어야 합니다.


</div>
</details>


<details>
<summary>Q. UML이란?</summary>
<div markdown="1">

- **Unified Modeling Language의 약자로 ‘객체 모델링 언어’ 또는 ‘통합 모델링 언어’를 뜻한다.**
- 시스템 설계, 요구분석, 시스템 구현 등의 과정에서 사용되는 모델링 언어로 표기법의 표준화를 목적으로 한다.
- 시스템에 대해 동일한 의미를 공유할 수 있게 하여 언어를 가시화 시킬 수 있고 시스템 구조와 모든 상세 내역에 대해 문서화하여 모델링하는 기능들을 제공하며, 다양한 모델링 도구로서의 다이어그램들로 이루어져 있다.


</div>
</details>


<details>
<summary>Q. 정규화란?</summary>
<div markdown="1">

정규화란 이상현상이 있는 릴레이션을 분해하여 이상현상을 없애는 과정이다. 이상현상이 존재하는 릴레이션을 분해하여 여러 개의 릴레이션을 생성하게 된다. 이를 구분하여 정규형이 높아질수록 이상현상은 줄어들게 된다.

즉, 쉽게말하면<span style="background:#affad1"> 테이블 간에 중복된 데이터를 허용하지 않는다는 것</span>이다. 중복된 데이터를 허용하지 않음으로써 무결성(Integrity)를 유지할 수 있으며, DB의 저장 용량 역시 줄일 수 있다. 이러한 테이블을 분해하는 정규화 단계가 정의 되어 있다.




</div>
</details>


<details>
<summary>Q. 정규화의 장단점?</summary>
<div markdown="1">

**정규화의 장점**

- 데이터베이스 변경 시 이상 현상(Anomaly)을 제거할 수 있다.
- 정규화된 데이터베이스 구조에서는 새로운 데이터 형의 추가로 인한 확장 시, 그 구조를 변경하지 않아도 되거나 일부만 변경해도 된다.
- 데이터베이스와 연동된 응용 프로그램에 최소한의 영향만을 미치게 되어 응용프로그램의 생명을 연장시킨다.

**정규화의 단점**

- 릴레이션의 분해로 인해 릴레이션 간의 JOIN연산이 많아진다.
- 질의에 대한 응답 시간이 느려질 **수도** 있다. 데이터의 중복 속성을 제거하고 결정자에 의해 동일한 의미의 일반 속성이 하나의 테이블로 집약되므로 한 테이블의 데이터 용량이 최소화되는 효과가 있다. 
- 따라서 데이터를 처리할 때 속도가 빨라질 수도 있고 느려질 수도 있다.
- 만약 조인이 많이 발생하여 성능 저하가 나타나면 **반정규화(De-normalization)**를 적용할 수도 있다.


</div>
</details>


<details>
<summary>Q.DB에서 View는 무엇인가? 가상 테이블이란?</summary>
<div markdown="1">

**1.** 뷰는 사용자에게 접근이 허용된 자료만을 제한적으로 보여주기 위해 하나 이상의 기본 테이블로부터 유도된, 이름을 가지는 가상 테이블이다.

**2.** 뷰는 저장장치 내에 물리적으로 존재하지 않지만 사용자에게 있는 것처럼 간주된다.

**3.** 뷰는 데이터 보정작업, 처리과정 시험 등 임시적인 작업을 위한 용도로 활용된다.

**4.** 뷰는 조인문의 사용 최소화로 사용상의 편의성을 최대화 한다.


</div>
</details>


<details>
<summary>Q.이상현상이란?</summary>
<div markdown="1">

이상 현상은 테이블을 설계할 때 잘못 설계하여 데이터를 삽입, 삭제, 수정할 때 논리적으로 생기는 오류를 말합니다.


> ###  이상현상(Anomaly)이란? 

> **이상현상(Anomaly)의 종류**  
> **삭제 이상 :** 데이터 삭제 시 의도와는 상관없이 다른 정보까지 연쇄적으로 삭제되는 현상  
> **삽입 이상 :** 데이터 삽입 시 의도와는 상관없이 원하지 않는 값들도 함께 삽입되는 현상  
> **수정 이상 :** 데이터 수정 시 의도와는 상관없이 데이터의 일부만 수정되어 일어나는 데이터 불일치 현상


</div>
</details>


<details>
<summary>Q.역정규화를 하는 이유?</summary>
<div markdown="1">

Join이 너무 많아지는 DB 설계와 쿼리는 요청을 처리하는 시간을 증가시키는 문제가 있기 때문에 모든 주요 Entity를 분리하는 것이 좋은 것이 아니라 DB의 전반적인 성능을 향상시킬 수 있는 구조화 과정을 거치는 것이 필요하다.

역정규화는  중복을 허용하며 Entity를 다시 통합하거나 분할하여 정규화 과정을 통해 도출된 DB 구조를 재조정하는 과정이다.


</div>
</details>


<details>
<summary>Q.데이터베이스를 설계할 때 가장 중요한 것이 무엇이라고 생각하나요?</summary>
<div markdown="1">

요구사항에 맞는 설계 ? ..

**DB 설계 시에는 유의해야 할 고려사항**이 존재한다.

1. 무결성 : 삽입, 삭제, 갱신 등의 연산 후에도 데이터베이스에 저장된 데이터가 정해진 제약조건을 항상 만족해야 함

2. 일관성 : DB에 저장된 데이터들 사이나, 특정 질의에 대한 응답이 처음부터 끝까지 변함없이 일정해야 함

3. 회복 : 시스템에 장애가 발생했을 때 장애 발생 직전의 상태로 복구할 수 있어야 함

4. 보안 : 불법적인 데이터의 노출 또는 변경이나 손실로부터 보호할 수 있어야 함

5. 효율성 : 응답 시간의 단축, 시스템의 생산성, 저장 공간의 최적화 등이 가능해야 함

6. DB확장 : 데이터베이스 운영에 영향을 주지 않으면서 지속적으로 데이터를 추가할 수 있어야 함


</div>
</details>

<details>
<summary>Q.데이터베이스 무결성이란?</summary>
<div markdown="1">


 무결성 : 삽입, 삭제, 갱신 등의 연산 후에도 데이터베이스에 저장된 데이터가 정해진 제약조건을 항상 만족해야 함

</div>
</details>

<details>
<summary>Q.트리거란?</summary>
<div markdown="1">

데이터베이스 트리거는 테이블에 대한 이벤트에 반응해 자동으로 실행되는 작업을 의미한다. 트리거는 INSERT, DELETE, UPDATE 같은 DML(데이터 조작 언어)의 데이터 상태 관리를 자동화하는데 사용된다.



</div>
</details>


<details>
<summary>Q. SELECT 쿼리의 수행 순서를 알려주세요.
</summary>
<div markdown="1">

![](https://i.imgur.com/xrjJsm9.png)

SQL 실행 순서를 이해하면 **쿼리의 성능이 낭비되는 지점이 잘 보이고 튜닝을 할 수 있게 된다.**


</div>
</details>

<details>
<summary>Q.데이터 베이스에서 인덱스(색인)이란 무엇인가요, 장단점은?</summary>
<div markdown="1">

인덱스란 추가적인 쓰기 작업과 저장 공간을 활용하여 데이터베이스 테이블의 검색 속도를 향상시키기 위한 자료구조이다.

- 장점
    
    - 테이블을 조회하는 속도와 그에 따른 성능을 향상시킬 수 있다.
    - 전반적인 시스템의 부하를 줄일 수 있다.
    
- 단점
    
    - 인덱스를 관리하기 위해 DB의 약 10%에 해당하는 저장공간이 필요하다.
    - 인덱스를 관리하기 위해 추가 작업이 필요하다.
    - 인덱스를 잘못 사용할 경우 오히려 성능이 저하되는 역효과가 발생할 수 있다.
    


</div>
</details>

<details>
<summary>Q.RDBMS와 NoSQL의 차이에 대해 설명해주세요.</summary>
<div markdown="1">

 RDBMS는 일관성과 신뢰도를 보장하기 위해 데이터 유형에 제약을 두고, NoSQL은 이러한 제약을 없애 속도, 유연성 및 확장성을 선사하는 것이라고 볼 수 있습니다.


</div>
</details>

<details>
<summary>Q.트랜잭션이란 무엇인지 설명해주세요.</summary>
<div markdown="1">

트랜잭션(Transaction) 이란, **데이터베이스의 상태를 변경시키기 위해 수행하는 작업 단위**이다.



# 트랜잭션의 상태
![](https://i.imgur.com/Wx98nfc.png)


트랜잭션은 논리적으로 5가지의 상태에 있을 수 있다.

- Active
    - 트랜잭션이 현재 실행 중인 상태
- Failed
    - 트랜잭이 실행되다 오류가 발생해서 중단된 상태
- Aborted
    - 브랜잭션이 비정상 종료되어 Rollback 이 수행된 상태
- Partially Committed
    - 트랜잭션의 연산이 마지막까지 실행되고 Commit이 되기 직전 상태
- Committed
    - 트랜잭션이 성공적으로 종료되어 Commit 연산을 실행한 후의 상태

</div>
</details>


<details>
<summary>Q.트랜잭션의 특성(ACID)에 대해 설명해주세요.</summary>
<div markdown="1">

### 원자성

원자성은 트랜잭션이 **DB에 모두 반영되거나, 전혀 반영되지 않거나**를 뜻한다.  
**All** or **Nothing**을 생각하면 된다.

### 일관성

일관성은 트랜잭션 **작업 처리의 결과가 항상 일관되어야 한다**를 뜻한다.  
즉, 데이터 타입이 반환 후와 전이 항상 동일해야 한다.

### 독립성

독립성은 **하나의 트랜잭션은 다른 트랜잭션에 끼어들 수 없고 마찬가지로 독립적임**을 의미한다.  
즉, 각각의 트랜잭션은 독립적이라 서로 간섭이 불가능하다.

### 지속성

지속성은 **트랜잭션이 성공적으로 완료되면 영구적으로 결과에 반영되어야 함**을 뜻한다.  
보통 commit 이 된다면 지속성은 만족할 수 있다.


</div>
</details>

<details>
<summary>Q. commit 과 rollback 이란? </summary>
<div markdown="1">

### Commit

하나의 트랜잭션이 **성공적으로 끝나서 데이터베이스가 일관성있는 상태에 있음**을 의미한다.
- 완전 저장
- COMMIT이란 모든 작업들을 정상적으로 처리하겠다고 확정하는 명령어로 처리과정을 **DB에 영구 저장**하는 것이다.
- COMMIT을 수행하면 하나의 트랜잭션 과정을 종료하는 것이다.
- COMMIT을 수행하면 이전 데이터가 완전히 UPDATE 된다.
![](https://i.imgur.com/DO7HHQJ.png)

### Rollback

트랜잭션의 원자성이 깨질 때, 즉 **하나의 트랜잭션 처리가 비정상적으로 종료** 되었을 때의 상태를 뜻한다.  
Rollback 이 이뤄진다면 트랜잭션을 다시 실행하거나 부분적으로 변경된 결과를 취소할 수 있다.

- 트랜잭션이 시작되기 이전의 상태로 되돌린다.  
- 즉, 마지막 COMMIT을 완료한 시점으로 다시 돌아간다.  
- COMMIT하여 저장한 것만 복구한다.

![](https://i.imgur.com/hSdqNJ2.png)
- 위 그림에서 ROLLBACK 명령은 마지막으로 수행한 COMMIT 명령까지만 청상처리(1,2)된 상태로 유지한다.
- 그 이후에 수행했던 모든 DML 명령어 작업(3,4,5)들을 취소시켜 이전 상태로 원상 복귀 시킨다.
- 트랜잭션은 이렇든 ALL-OR-Nothing 방식으로 DML 명령어들을 처리한다.
- ALL-OR-Nothing이란 '모든것을 수행하던지 아무것도 하지말던지'라는 의미이다.

</div>
</details>

<details>
<summary>Q. 트랜잭션을 사용할 때 주의해야 할 점은 무엇인가요?</summary>
<div markdown="1">

광범위한 트랜잭션은 성능 저하를 일으킬 수 있기 때문에, 꼭 필요한 최소의 코드에만 적용하는 것이 좋다. 일반 데이터 베이스 커넥션은 개수가 제한적인데, 각 단위 프로그램이 커넥션을 소유하는 시간이 길어진다면 사용가능한 여유 커넥션의 개수가 줄어들기 때문이다. 


</div>
</details>


<details>
<summary>Q. DB 에서 Inode 란 무엇인지 아나요?</summary>
<div markdown="1">

ㅇㅇ

</div>
</details>




<details>
<summary>Q.트랜잭션을 병행으로 처리(동시성 제어)하려고 할 때 발생할 수 있는 문제를 설명해보시오.</summary>
<div markdown="1">

## **[ 동시성제어란? ]**

- 다중 사용자 환경에서 둘 이상의 트랜잭션이 동시에 수행될 때, 일관성을 해치지 않도록 트랜잭션의 데이터 접근 제어

**병행 제어(Concurrency Control)**는 이렇게 **트랜잭션이 병행 수행될 때 트랜잭션이 데이터베이스의 일관성을 파괴하지 않고, 다른 트랜잭션에 영향을 주지 않도록 트랜잭션 간의 상호작용을 제어하는 것**을 말한다. 

병행 제어의 목적은 다음과 같다. 

- **데이터베이스의 일관성 유지**
- **데이터베이스 공유 최대화**
- **시스템 활용도 최대화**
- **사용자 응답 시간 최소화**
- **단위 시간당 트랜잭션 처리 건수 최대화**

2개 이상의 트랜잭션이 하나의 값에 접근하는 경우에는 어떻게 될까요? 2개의 트랜잭션이 모두 읽는 경우에는 문제가 발생하지 않지만, 
1개의 트랜잭션은 쓰고 1개의 트랜잭션은 읽는 경우에 상황에 따라 <span style="background:#affad1">오손 읽기, 반복불가능 읽기, 유령데이터 읽기 문제가 발생할 수 있으며, 2개의 트랜잭션이 모두 쓰기(Write) 시 무제어 병행 수행을 하는 경우에 갱신 손실, 모순성, 연쇄 복귀 등의 문제가 발생</span>할 수 있다.



##### - **트랜잭션을 병행으로 처리할 때 위와 같은 문제를 방지하기 위한 방법을 설명하시오.**


**1. 로킹 (Locking)**

로킹은 **트랜잭션이 접근하려는 데이터를 다른 트랜잭션이 접근하지 못하도록 잠그는(lock) 병행 제어 기법**이다.

이를 통해 **상호 배제(Mutual Exclusive) 기능**을 제공하며, 잠금을 설정한 트랜잭션이 해제(unlock)할 때까지 데이터를 **독점적**으로 사용할 수 있다. 



##### - **그렇다면 이 로킹 단위를 크게했을 때와 작게 했을 때의 차이점을 설명하시오.**

한 번에 로킹 할 수 있는 데이터의 크기를 **로킹 단위**라고 하며 필드(Field), 레코드(Record), 테이블(Table), 파일(File), 데이터베이스(Database) 모두 로킹 단위가 될 수 있다. 

로킹 단위의 크기에 따라 성능의 차이가 발생한다.

**로킹 단위가 클수록 병행 제어가 단순해지고 관리하기가 편하지만 병행성 수준이 낮아진다.** 

**반면 로킹 단위가 작을수록 병행 제어가 복잡해지고 오버헤드가 증가하지만, 병행성 수준이 높아지고 데이터베이스 공유도가 높아진다.** 

[출처](https://rebro.kr/163)


##### - **로킹 제어가 일으킬 수 있는 문제점은 무엇인가?**

로킹 기법은 **교착 상태(Dead lock)**가 발생할 수 있다는 한계가 있다. 

**교착 상태란, 여러 트랜잭션이 특정 데이터에 lock을 한 채 다른 트랜잭션이 lock을 수행한 데이터에 접근하려고 할 때 실행을 하지 못하고 서로 무한정 기다리는 상태**를 말한다. 

![](https://i.imgur.com/nHk8yn8.png)


</div>
</details>


<details>
<summary>Q.격리 수준 중 SERIALIZABLE에 대해 설명해주세요.</summary>
<div markdown="1">

트랜잭션의 격리 수준(Isolation Level)이란 여러 트랜잭션이 동시에 처리될 때, 
특정 트랜잭션이 다른 트랜잭션에서 변경하거나 조회하는 데이터를 볼 수 있게 허용할지 여부를 결정하는 것이다. 트랜잭션의 격리 수준은 격리(고립) 수준이 높은 순서대로 SERIALIZABLE, REPEATABLE READ, READ COMMITTED, READ UNCOMMITED가 존재한다. 


SERIALIZABLE은 가장 엄격한 격리 수준으로, 이름 그대로 트랜잭션을 순차적으로 진행시킨다. SERIALIZABLE에서 여러 트랜잭션이 동일한 레코드에 동시 접근할 수 없으므로, 어떠한 데이터 부정합 문제도 발생하지 않는다. 하지만 트랜잭션이 순차적으로 처리되어야 하므로 동시 처리 성능이 매우 떨어진다.

[참고](https://mangkyu.tistory.com/299#:~:text=%5B%20SERIALIZABLE%20%5D,%EB%AC%B8%EC%A0%9C%EB%8F%84%20%EB%B0%9C%EC%83%9D%ED%95%98%EC%A7%80%20%EC%95%8A%EB%8A%94%EB%8B%A4.)


</div>
</details>


<details>
<summary>Q.그럼 데드락을 안 생기게 하는 방법을 설명해보시오</summary>
<div markdown="1">

DB(데이버베이스)에서 교착상태(Dead Lock)을 해결하기 위한 방법은 아래와 같다.

- 예방 기법 : 
대표적인 예방 기법은 아래와 같다.

	- 각 트랜잭션이 실행되기 전에 필요한 모든 자원을 Lock(잠금)한다.
	    - 필요한 모든 데이터를 Lock(잠금)해야 하므로 병행성이 떨어진다.
	- SET LOCK_TIMEOUT문을 통해 일정 시간이 지나면 쿼리를 취소한다.
	    - 기존의 교착상태인 데이터가 있다면, 그 데이터에 접근하는 쿼리만 취소한다.
	    - 즉, 근본적인 해결책이 될 수 없다.
- 회피 기법 : **회피 기법은 자원을 할당할 때 시간 스탬프(Time Stamp)를 활용해서 교착상태가 일어나지 않도록 회피하는 방법**이다. 예방 기법의 단점 때문에 실제로는 회피 기법이 많이 사용된다.

회피 기법의 종류는 크게 2가지가 있다.

- Wait-Die 방식
	    - 트랜잭션 A가 트랜잭션 B에 의해 잠금된 데이터를 요청할 때 트랜잭션 A이 먼저 들어온 트랜잭션이라면 대기(Wait)한다.
	    - 트랜잭션 A가 나중에 들어온 트랜잭션이라면, 포기(Die)하고 나중에 다시 요청한다.
- Wound-Wait 방식
	    - 트랜잭션 A가 트랜잭션 B보다 먼저 들어온 트랜잭션이라면, 데이터를 선점(Wound)한다.
	    - 반면, 트랜잭션A가 트랜잭션 B보다 나중에 들어온 트랜잭션이라면 대기(Wait)한다.
- 낙관적 병행 제어 기법 : 낙관적 병행 제어 기법은 트랜잭션이 실행되는 동안에는 검사를 수행하지 않고, 트랜잭션이 커밋된 후에 데이터에 문제가 있다면 롤백(Rollback)하는 방법이다.

	즉, 낙관적 병행 제어 기법은 **판독->확인->기록** 단계를 따른다. **확인 단계**를 성공적으로 거친 트랜잭션만  **기록 단계**를 수행할 수 있다.


- 빈도 줄이기 기법 : 교착상태의 빈도를 낮추는 방법은 아래와 같다.

	- 트랜잭션을 자주 커밋한다.
	
	- 정해진 순서로 테이블에 접근한다. (위에서는 트랜잭션 1은 B->A 순, 트랜잭션 2는 A->B순으로 접근했다.)
	
	- 읽기 잠금 (SELECT ~ FOR UPDATE)의 사용을 피한다.
	
	- 테이블 단위의 Lock(잠금)을 획득해 갱신을 직렬화한다. (테이블의 복수행을 복수의 연결에서 순서 없이 갱신하면 교착상태가 자주 발생하기 때문)
	
	- Index 설계 (Update시 Index를 타지 않으면 테이블 전체에 Lock이 걸릴 수 있다.)
	
	- Isolation level(고립 수준)을 낮춘다. (서비스 검토 필요)


</div>
</details>


<details>
<summary>Q.JDBC와 ODBC의 차이는?</summary>
<div markdown="1">


|   |   |   |
|---|---|---|
||**ODBC**|**JDBC**|
사용목적|응용프로그램에서 데이터에 접근할 때|Java에서 DataBase와 연결하여 작업하기 위해서|
DBMS  <br>종류에 따라|접속처의 데이터베이스가 어떠한 DBMS에 의해  <br>관리되고 있는지 의식할 필요가 **없다**.|Java와 연동되는 DBMS에 따라  <br>**그에 맞는 JDBC를 설치할 필요가 있다.**|



</div>
</details>


<details>
<summary>Q.커넥션 풀을 사용하는 이유와 장점 그리고 주의점</summary>
<div markdown="1">

웹 컨테이너(WAS)가 실행되면서 일정량의 Connection 객체를 미리 만들어서 Pool에 저장한다.

클라이언트 요청이 오면 Connection 객체를 빌려주고 해당 객체 임무가 완료되면 다시 Connection 객체를 반납해 Pool에 저장한다.


1. DB 접속 설정 객체를 미리 만들어 연결해 메모리 상에 등록하기 때문에 불필요한 작업이 사라진다.(커넥션 생성, 삭제)

→ 클라이언트가 DB에 빠르게 접근 가능하다.

1. DB Connection 수를 제한할 수 있어서 과도한 접속으로 인한 서버 자원 고갈을 예방할 수 있다.
2. DB 서버 환경이 바뀔 경우 쉬운 유지 보수가 가능하다.
3. 연결이 끝난 Connection을 재사용함으로써 새로 객체를 생성하는 비용을 절약할 수 있다.

커넥션 풀을 크게 설정하면 메모리 소모가 크다. 하지만 많은 사용자가 대기 시간이 줄어든다.

커넥션 풀을 작게 설정하면 그 만큼 대기시간이 늘어난다. 하지만 적은 메모리를 사용한다.

Connection의 주체는 Thread이기 때문에 Thread와 함께 고려해야한다.

- Thread Pool 크기 < Connection Pool 크기
    - Thread Pool에서 트랜잭션을 처리하는 Thread가 사용하는 Connection 외에 남는 Connection은 실질적으로 메모리 공간만 차지한다.
- Thread Pool 크기와 Connection Pool 모두 크기 증가
    - Thread 증가로 인해 더 많은 Context Switching이 발생한다.


</div>
</details>


<details>
<summary>Q.CAP 이론</summary>
<div markdown="1">

CAP 이론(또는 Brewer`s theorem)이란 Network로 연결된 분산된 **데이터베이스 시스템은 일관성(Consistency), 가용성(Availability), and 분할 내구성(Partition Tolerance)의 3가지 특성중 2가지 특성만을 충족 할수 있고 3가지 모두 충족할 수 없다는 이론**입니다.

[출처](https://sabarada.tistory.com/91)

</div>
</details>

<details>
<summary>Q.OLTP, OLAP</summary>
<div markdown="1">

*** OLTP (Online Transaction Processing)**

 OLTP 란 온라인 트랜잭션 처리를 말하며, 네트워크 상의 온라인 사용자들의 Database 에 대한 일괄 트랜잭션 처리를 의미한다. 

흔히 말하는 "트랜잭션(Transaction) 처리" 를 OLTP 라 부른다. 트랜잭션이라 부르는 용어의 의미 자체가 OLTP 의 의미를 포함하고 있다고 할 수 있겠다. 



*** OLAP (Online Analytical Processing)**

 OLAP 란 Database 자체적으로 운용되는 시스템이라기 보다는 데이터 웨어하우스 등의 시스템과 연관되어 Data 를 분석하고 의미있는 정보로 치환하거나, 복잡한 모델링을 가능하게끔 하는 분석 방법을 말한다.

기능 자체에 중심을 두는 OLTP 와는 다르게 사용하는 목적과 주제에 보다 중점을 둔다.

그렇기 때문에 주로 대용량의 데이터에 대해 처리하고 보다 복잡한 Data processing 으로 의미를 추출하는데 중점을 둔다.

대부분의 경우 OLAP 연산을 수행한다 라고 하면 적재된 데이터에 대한 분석 또는 SELECT Query 를 통한 데이터 스캔 Operation 이 주가 된다. 이는 OLTP 가 Transaction 의 과정에서 INSERT/UPDATE 를 중점적으로 수행하는 것과 대조되게 된다.

(하지만 언급했듯이, 쿼리의 읽기냐 쓰기냐 에 따라 구분되는 개념이라고 보기는 애매하다!)


</div>
</details>

<details>
<summary>Q.ETL</summary>
<div markdown="1">

추출, 전환, 적재(_ETL_)는 다양한 소스의 데이터를 데이터 웨어하우스라고 부르는 대형 중앙 집중식 리포지토리에 결합하는 과정


</div>
</details>

---

### 알고리즘 

<details>
<summary>Q. BigO 란 무엇인가</summary>
<div markdown="1">

BigO 표기법은 알고리즘의 시간 복잡도나 공간 복잡도를 나타내는 데 사용되는 표기법입니다. 알고리즘의 최악의 성능을 나타내며, 입력 데이터의 크기에 따라 알고리즘의 실행 시간이나 필요한 메모리 공간이 어떻게 증가하는지를 설명합니다.'

(원리까지 말해야해요? ..)
[참고](https://cocococo.tistory.com/entry/%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98-BigO%EC%8B%9C%EA%B0%84-%EB%B3%B5%EC%9E%A1%EB%8F%84-%EA%B3%B5%EA%B0%84-%EB%B3%B5%EC%9E%A1%EB%8F%84-%EA%B0%9C%EB%85%90-%EB%B0%8F-%EC%98%88%EC%A0%9C#:~:text=%EB%B9%85%EC%98%A4%EB%9E%80%3F,%EC%8B%9C%EA%B0%84%EC%9D%98%20%EA%B4%80%EA%B3%84%EB%A5%BC%20%EB%A7%90%ED%95%9C%EB%8B%A4.)

</div>
</details>

<details>
<summary>Q DFS와 BFS의 차이</summary>
<div markdown="1">

- DFS는 가능한 한 깊게 노드를 탐색한 후, 더 이상 탐색할 노드가 없을 때 이전 분기점으로 돌아가 다른 경로를 탐색합니다. 재귀 또는 스택을 사용하여 구현할 수 있습니다.
- BFS는 가까운 노드부터 차례대로 탐색하는 방법으로, 큐를 사용하여 구현합니다. 같은 레벨의 노드를 모두 탐색한 후 다음 레벨의 노드를 탐색합니다.


</div>
</details>

<details>
<summary>Q. Fibonacci에서의 세 가지(Recursion, Dynamic Programming, 반복) 방식에 대한 시간복잡도와 공간복잡도 차이</summary>
<div markdown="1">

1. **재귀(Recursion)**: 시간 복잡도는 O(2^n)이며, 공간 복잡도는 O(n)입니다. 매우 비효율적인 방식입니다.
2. **동적 계획법(Dynamic Programming)**: 시간 복잡도는 O(n), 공간 복잡도도 O(n)입니다. 이전에 계산한 값을 저장해두고 재사용함으로써 효율을 높입니다.
3. **반복(Iterative)**: 시간 복잡도는 O(n), 공간 복잡도는 O(1)입니다. 두 변수만을 이용해 이전 두 수를 기억하며 반복하여 계산합니다.


</div>
</details>



<details>
<summary>Q.정렬 알고리즘의 종류와 개념</summary>
<div markdown="1">

- **버블 정렬(Bubble Sort)**: 인접한 두 원소를 비교하여 정렬하는 방식. 매우 비효율적.
- **선택 정렬(Selection Sort)**: 가장 작은(또는 큰) 원소를 선택해 맨 앞(또는 뒤)로 이동시키는 방식.
- **삽입 정렬(Insertion Sort)**: 각 원소를 이미 정렬된 배열의 적절한 위치에 삽입하는 방식.
- **퀵 정렬(Quick Sort)**: 피벗을 기준으로 배열을 두 부분으로 나누어 각 부분을 재귀적으로 정렬하는 방식.
- **병합 정렬(Merge Sort)**: 분할 정복 알고리즘을 이용하여 배열을 절반으로 나눈 뒤 각각을 정렬하고 마지막에 병합.


</div>
</details>

<details>
<summary>Q. Greedy 알고리즘</summary>
<div markdown="1">

은 매 순간 최적의 선택을 함으로써 최종적인 해답에 도달하는 방식입니다. 지역적 최적해가 전체적으로도 최적해가 되는 상황에 적합합니다.


</div>
</details>

<details>
<summary>Q.최소 신장 트리(MST, Minimum Spanning Tree)란</summary>
<div markdown="1">

그래프의 모든 정점을 최소한의 비용으로 연결하는 부분 그래프입니다. 간선의 가중치 합이 최소가 되어야 합니다.


</div>
</details>


<details>
<summary>Q. Kruskal MST 알고리즘</summary>
<div markdown="1">

 가장 가벼운 간선부터 선택하여 사이클을 형성하지 않는 한도 내에서 MST를 구성합니다. 분리 집합을 사용해 효율적으로 구현합니다.


</div>
</details>

<details>
<summary>Q. Prim MST 알고리즘</summary>
<div markdown="1">

특정 정점에서 시작하여 접근 가능한 간선 중 가장 가벼운 간선을 선택해 MST를 확장해 나갑니다. 우선순위 큐를 사용하여 효율적으로 구현할 수 있습니다.


</div>
</details>

<details>
<summary>Q. 본인이 사용하는 언어의 sort 함수 내부 작동 알고리즘에 대해서 설명하세요</summary>
<div markdown="1">

- Python의 경우, 내부 sort 함수는 Timsort 알고리즘을 사용합니다. Timsort는 병합 정렬과 삽입 정렬의 장점을 결합한 알고리즘입니다.


</div>
</details>

<details>
<summary>Q.Trie 알고리즘</summary>
<div markdown="1">


문자열 검색을 위한 트리 기반 자료구조로, 각 노드가 문자를 표현하며 문자열을 효율적으로 검색할 수 있습니다

</div>
</details>

<details>
<summary>Q.스택과 큐에 대해 설명하세요</summary>
<div markdown="1">

- 스택은 LIFO(후입선출) 방식, 큐는 FIFO(선입선출) 방식으로 데이터를 관리합니다.


</div>
</details>

<details>
<summary>Q. 그래프와 트리 각각의 개념과 차이에 대해 설명해주세요</summary>
<div markdown="1">

- 그래프는 노드들이 간선으로 연결된 구조, 트리는 사이클이 없는 하나의 연결된 그래프입니다.


</div>
</details>

<details>
<summary>Q. RAID 란?</summary>
<div markdown="1">

- RAID는 여러 디스크를 결합해 데이터의 신뢰성과 I/O 성능을 높이는 기술로, 다양한 레벨이 있습니다.


</div>
</details>

<details>
<summary>Q. Stack과 Queue, Tree와 Heap의 구조에 대해 설명해주세요.</summary>
<div markdown="1">

- 스택은 배열이나 연결 리스트로 구현할 수 있으며 LIFO 구조입니다. 큐는 배열이나 연결 리스트로 구현할 수 있으며 FIFO 구조입니다. 
- 트리는 계층적 구조를 가진 노드의 집합이며, 힙은 최대값이나 최소값을 빠르게 찾기 위한 트리 기반의 자료구조입니다.


</div>
</details>

<details>
<summary>Q.Stack과 Queue의 실사용 예를 들어 간단히 설명해주세요.</summary>
<div markdown="1">

- 스택의 실사용 예로는 웹 브라우저의 뒤로 가기 기능이 있으며, 큐의 예로는 프린터의 인쇄 대기열이 있습니다.


</div>
</details>

<details>
<summary>Q. Priority Queue(우선순위 큐)에 대해 설명해주세요.</summary>
<div markdown="1">

우선순위 큐는 각 요소가 우선순위를 가지고, 우선순위가 높은 순서대로 처리되는 큐입니다.


</div>
</details>

### 저번에 못한 것 (못한것을 못함 쪼금밖에...)

<details>
<summary>Q. vpn 이란 </summary>
<div markdown="1">

VPN은 가설사설망(Virtual Private Network)을 의미하며, ISP에 정보를 넘기지 않고 익명성을 유지하여 인터넷에 접속하는 방법을 묻는 질문입니다. VPN은 공중망 연결을 통해 전용선처럼 연결을 사용할 수 있는 효과를 누릴 수 있습니다


</div>
</details>

<details>
<summary>Q. 컴퓨터 부팅후 인터넷 접속까지의 과정을 설명 </summary>
<div markdown="1">

- Booting은 Bootstrapping의 간략화된 표현으로, 원래는 Bootstrapping이 정확한 표현
- BIOS가 시스템의 하드웨어 이상유무 점검
- 전원 공급 후 부트로더를 통해 Bootstrap Program 메모리 적재
- Bootstrap Program이 커널을 적재하고 실행
- 커널에 의해 init 프로세스 생성, OS 초기화 작업 수행


대기열, 캐싱, DNS, 라우팅, ARP, 초기연결을 거쳐 컨텐츠를 다운받게 되고 이 후 브라우저렌더링 과정을 거쳐 네이버라는 화면이 나타나게 됩니다. 또한 이러한 과정이 캡슐화, 비캡슐화과정을 거쳐서 이뤄지게 됩니다.


[참고1](https://blog.naver.com/jhc9639/222700552159)
[참고2](https://ddb8036631.github.io/question/%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C-3/)
[참고3](https://cryptosalamander.tistory.com/120#google_vignette)

</div>
</details>

<details>
<summary>Q. 리눅스 부팅 과정 </summary>
<div markdown="1">

## **리눅스 시스템 부팅 프로세스**

> **리눅스 시스템의 부팅 프로세스를 아래 4단계의 순서로 자세하게 살펴보자  
>   
> **1단계: 하드웨어 단계  
> 2단계: 부트로더 단계  
> 3단계: 커널로드 단계  
> 4단계: INIT 단계(SysV / Systemd)


조금 더 공부해올게요 
[참고](https://yonlog.tistory.com/59)

</div>
</details>

