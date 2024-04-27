## 운영체제

<details>
<summary>Q. 운영체제란?.</summary>
<div markdown="1">


<span style="background:rgba(74, 82, 199, 0.2)">운영체제란 컴퓨터 사용자와 컴퓨터 HW 간의 인터페이스로서 동작하는 시스템 SW의 일종으로, 다른 응용프로그램이 유용한 작업을 할 수 있도록 환경을 제공해줍니다.</span>

![](https://i.imgur.com/IO8Ei9b.png)

운영체제의 코어(핵심) 부분을 **커널(Kernel)**이라고 하는데, 일반적으로는 커널에 여러가지 기능(라이브러리, 시스템 프로그램 등등)이 추가된 상태를 통칭해서 운영체제(OS)라고 한다.

### 운영체제의 주요 목적은?

CPU, 입출력 장치, 프로세스 등 컴퓨터 시스템의 자원을 관리하여 컴퓨터 시스템이 제대로 작동하도록 합니다. 이외에도 처리능력 향상, 반환 시간 단축, 신뢰도 향상 등이 있습니다.

- 처리능력: 일정 시간 내에 시스템이 처리하는 일의 양
- 신뢰도: 시스템이 주어진 문제를 정확하게 해결하는 정도
- 반환 시간: 일정 시간 내에 시스템이 처리하는 일의 양


</div>
</details>

<details>
<summary>Q.프로세스와 스레드의 차이?</summary>
<div markdown="1">

> - 프로세스: 운영체제로부터 자원을 할당받은 작업의 단위.  
> - 스레드: 프로세스가 할당받은 자원을 이용하는 실행 흐름의 단위.

### 프로세스 
- 프로세스는 각각 독립된 메모리 영역(Code, Data, Stack, Heap의 구조)을 할당받는다.
- 각 프로세스는 별도의 주소 공간에서 실행되며, 한 프로세스는 다른 프로세스의 변수나 자료구조에 접근할 수 없다.
- 한 프로세스가 다른 프로세스의 자원에 접근하려면 프로세스 간의 통신(IPC, inter-process communication)을 사용해야 한다.

  ![](https://i.imgur.com/TkHdAJQ.png)



### 스레드 
스레드는 프로세스 내에서 각각 Stack만 따로 할당받고 Code, Data, Heap 영역은 공유한다.
- 스레드는 한 프로세스 내에서 동작되는 여러 실행의 흐름으로, 프로세스 내의 주소 공간이나 자원들(힙 공간 등)을 같은 프로세스 내에 스레드끼리 공유하면서 실행된다.
- 같은 프로세스 안에 있는 여러 스레드들은 같은 힙 공간을 공유한다. 반면에 프로세스는 다른 프로세스의 메모리에 직접 접근할 수 없다.
- 각각의 스레드는 별도의 레지스터와 스택을 갖고 있지만, 힙 메모리는 서로 읽고 쓸 수 있다.
- 한 스레드가 프로세스 자원을 변경하면, 다른 이웃 스레드(sibling thread)도 그 변경 결과를 즉시 볼 수 있다.

  ![](https://i.imgur.com/iBkvhWc.png)


**<font color="#00b050">한마디로 요약:</font>**
프로세스는 각각 독립된 메모리 영역을 할당받는 반면에, 스레드는 stack 만 따로 할당 받고 code,data,heap 을 공유한다는 차이점이 있습니다. 



[이해하기 좋은 글](https://inpa.tistory.com/entry/%F0%9F%91%A9%E2%80%8D%F0%9F%92%BB-%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4-%E2%9A%94%EF%B8%8F-%EC%93%B0%EB%A0%88%EB%93%9C-%EC%B0%A8%EC%9D%B4)

</div>
</details>

<details>
<summary>Q.멀티 스레드와 멀티 프로세스의 차이</summary>
<div markdown="1">



![](https://i.imgur.com/tzoRBQU.png)

### 멀티 프로세스
**멀티 프로세싱이란**

하나의 프로그램을 여러 개의 프로세스로 구성하여 각 프로세스가 하나의 작업(태스크)을 처리하도록 하는 것이다.

**<font color="#00b050">장점</font>**
여러 개의 자식 프로세스 중 하나에 문제가 발생하면 그 자식 프로세스만 죽는 것 이상으로 다른 영향이 확산되지 않는다.

<font color="#ff0000">**단점**</font>
**Context Switching에서의 오버헤드**
Context Switching 과정에서 캐쉬 메모리 초기화 등 무거운 작업이 진행되고 많은 시간이 소모되는 등의 오버헤드가 발생하게 된다.

프로세스는 각각의 독립된 메모리 영역을 할당받았기 때문에 프로세스 사이에서 공유하는 메모리가 없어, Context Switching가 발생하면 캐쉬에 있는 모든 데이터를 모두 리셋하고 <u>다시 캐쉬 정보를 불러와야 한다.</u>

**프로세스 사이의 어렵고 복잡한 통신 기법(IPC)**
프로세스는 각각의 독립된 메모리 영역을 할당받았기 때문에 하나의 프로그램에 속하는 프로세스들 사이의 변수를 공유할 수 없다.



### 멀티 스레드
**멀티 스레딩이란**
하나의 응용프로그램을 여러 개의 스레드로 구성하고 각 스레드로 하여금 하나의 작업을 처리하도록 하는 것이다.


<font color="#00b050">**장점**</font>

**시스템 자원 소모 감소 (자원의 효율성 증대)**

프로세스를 생성하여 자원을 할당하는 시스템 콜이 줄어들어 자원을 효율적으로 관리할 수 있다.

**시스템 처리량 증가 (처리 비용 감소)**

스레드 간 데이터를 주고 받는 것이 간단해지고 시스템 자원 소모가 줄어들게 된다.
스레드 사이의 작업량이 작아 Context Switching이 빠르다.
간단한 통신 방법으로 인한 프로그램 응답 시간 단축

스레드는 프로세스 내의 Stack 영역을 제외한 모든 메모리를 공유하기 때문에 <u>통신의 부담이 적다.</u>

**<font color="#ff0000">단점</font>**
- 주의 깊은 설계가 필요하다.
- 디버깅이 까다롭다.
- 단일 프로세스 시스템의 경우 효과를 기대하기 어렵다.
- 다른 프로세스에서 스레드를 제어할 수 없다. (즉, 프로세스 밖에서 스레드 각각을 제어할 수 없다.)
- 멀티 스레드의 경우 자원 공유의 문제가 발생한다. (동기화 문제)
- 하나의 스레드에 문제가 발생하면 전체 프로세스가 영향을 받는다.

> **요약**
> 멀티 프로세스는 하나의 프로그램을 여러개의 프로세스로 구성하여 하나의 작업을 처리여 프로세스가 갑자기 종료되더라도 다른 프세스는 영향을 받지 않습니다만, 
> 
> 독립된 메모리 영역이기에 컨텍스트 스위치 비용이 발생합니다. 
> 
> 반면 멀티 스레드는 프로그램을 여러개의 쓰레드로 구성하여 작업을 처리합니다. 스레드간 데이터 공유가 쉽지만, 하나의 스레에 문제가 발생하면 다른 스레드가 영향을 받아 전체 프로세스가 영향을 받습니다.




</div>
</details>

<details>
<summary>Q. 멀티 프로세스로 처리 가능한 걸 굳이 멀티 스레드로 하는 이유는?</summary>
<div markdown="1">


![](https://i.imgur.com/pZ85MS5.png)

**자원의 효율성 증대**
멀티 프로세스로 실행되는 작업을 멀티 스레드로 실행할 경우, 프로세스를 생성하여 자원을 할당하는 시스템 콜이 줄어들어 자원을 효율적으로 관리할 수 있다.
–> 프로세스 간의 Context Switching시 단순히 CPU 레지스터 교체 뿐만 아니라 RAM과 CPU 사이의 캐쉬 메모리에 대한 데이터까지 초기화되므로 오버헤드가 크기 때문
스레드는 프로세스 내의 메모리를 공유하기 때문에 독립적인 프로세스와 달리 스레드 간 데이터를 주고 받는 것이 간단해지고 시스템 자원 소모가 줄어들게 된다.

**처리 비용 감소 및 응답 시간 단축**
또한 프로세스 간의 통신(IPC)보다 스레드 간의 통신의 비용이 적으므로 작업들 간의 통신의 부담이 줄어든다.
–> 스레드는 Stack 영역을 제외한 모든 메모리를 공유하기 때문
프로세스 간의 전환 속도보다 스레드 간의 전환 속도가 빠르다.
–> Context Switching시 스레드는 Stack 영역만 처리하기 때문

<span style="background:#fff88f">주의할 점!</span>

**동기화 문제**
스레드 간의 자원 공유는 전역 변수(데이터 세그먼트)를 이용하므로 함께 상용할 때 충돌이 발생할 수 있다.



</div>
</details>

<details>
<summary>Q.Context Swiching이란 무엇인가요?</summary>
<div markdown="1">

<span style="background:#fff88f">** Context Switching란?**</span>
CPU에서 여러 프로세스를 돌아가면서 작업을 처리하는 데 이 과정을 Context Switching라 한다. 
구체적으로, 동작 중인 프로세스가 대기를 하면서 해당 프로세스의 상태(Context)를 보관하고, 대기하고 있던 다음 순서의 프로세스가 동작하면서 이전에 보관했던 프로세스의 상태를 복구하는 작업을 말한다.

![](https://i.imgur.com/jqyMIXP.png)


</div>
</details>


<details>
<summary>Q.교착상태(DeadLock)가 무엇이며, 4가지 조건은?</summary>
<div markdown="1">

![](https://i.imgur.com/khT3h2T.png)

### 교착상태란 
교착상태(Dead Lock)은 둘 이상의 프로세스들이 자원을 점유한 상태에서 서로 다른 프로세스가 점유하고 있는 자원을 요구하며 무한정 기다리는 현상을 의미한다.

#### 교착상태 발생 조건

주로 멀티 프로그래밍 환경에서 한정된 자원을 얻기 위해 서로 경쟁하는 상황에서 발생한다.

교착상태가 발생하기 위해서는 다음의 네가지 조건이 충족되어야 하는데, 이 네가지 조건 중 하나라도 충족되지 않으면 교착상태가 발생하지 않는다.

#####  1. 상호배제(Mutual Exclusion)

<span style="background:#fff88f">자원은 한 번에 한 프로세스만이 사용할 수 있어야 한다</span>. 상호 배제 기법에는 뮤텍스, 세마포어 등이 있다.

##### 2. 점유와 대기(Hold and Wait)

최소한 하나의 자원을 점유하고 있으면서 다른 프로세스에 할당되어 사용하고 있는 자원을 추가로 점유하기 위해<u> 대기하는 프로세스가 있어야 한다</u>.

##### 3. 비선점(Non-preemption)

다른 프로세스에 할당된 자원은 사용이 끝날 때까지 <u>강제로 빼앗을 수 없어야 한다</u>.

##### 4. 환경 대기(Circular Wait)

서로 다른 공유 자원을 사용하기 위해 **대기하는 프로세스들이 원형으로 구성(순환형태)**되어 있어 자신에게 할당된 자원을 점유하면서<u> 앞이나 뒤에 있는 프로세스의 자원을 요구</u>한다.


####  **🚀 데드락 예방(Prevention)**

**데드락의 발생조건 4가지 중 하나라도 발생하지 않게 하는 것**이 데드락을 예방하는 방법입니다. 즉, 각각의 조건을 방지(부정)하여 데드락 발생 가능성을 차단합니다.

- **자원의 상호 배제 조건** 방지 : 한 번에 여러 프로세스가 공유 자원을 사용할 수 있게 합니다.
    - 그러나 추후 동기화 관련 문제가 발생할 수 있습니다.
- **점유 대기 조건 방지** : 프로세스 실행에 필요한 모든 자원을 한꺼번에 요구하고 허용할 때까지 작업을 보류해서, 나중에 또다른 자원을 점유하기 위한 대기 조건을 성립하지 않도록 합니다.
    
- **비선점 조건 방지** : 이미 다른 프로세스에게 할당된 자원이 선점권이 없다고 가정할 때, 높은 우선순위의 프로세스가 해당 자원을 선점할 수 있도록 합니다.

- **순환 대기 조건 방지** : 자원을 순환 형태로 대기하지 않도록 <u>일정한 한 쪽 방향</u>으로만 자원을 요구할 수 있도록 합니다.



</div>
</details>

<details>
<summary>Q.뮤텍스, 세마포어가 뭔지, 차이점은?</summary>
<div markdown="1">

여러 프로세스가 동시에 공유 데이터에 접근할 때 접근 순서에 따라 실행 결과가 달라지는 상황에 놓인 프로세스들을 경쟁상태(reace condition)에 있다고 한다. 이러한 경쟁상태를 예방하려면, 병행 프로세스들을 동기화 해야 하는데, 이는 임계 영역을 이용한 상호 배제로 구현할 수 있다. 

> **임계영역** 
> 여러 프로세스가 데이터를 공유하며 수행될 때, 각 프로세스에서 공유데이터를 접근하는 프로그램 코드 부문 

여기서 뮤텍스와 세마포어가 바로 상호 배제의 방법들 중 하나이다. 

###  뮤텍스(mutex)

뮤텍스는 Key 에 해당하는 어떤 오브젝트가 있으며 이 오브젝트를 소유한 (쓰레드,프로세스) 것 만이 공유자원에 접근할 수 있다.

![](https://i.imgur.com/8nwyKeN.png)

다중 프로세스들의 공유 리소스에 대한 접근을 조율하기 위해 locking 과 unlocking 을 사용한다. 즉, 쉽게 말하면 뮤텍스 객체를 두 스레드가 동시에 사용할 수 없다는 의미이다.

- lock : 현재 임계 구역에 들어갈 권한을 얻어옴( 만약 다른 프로세스/스레드가 임계 구역 수ㅇ중이면, 종료할 때까지 대기)
- unlock : 현재 입계 구역을 모두 사용했음을 알림. (대기중인 다른 프로세스/스레드가 임ㅖ구역에 진입할 수 있음.)

##### 과정

- 1번 프로세스가 자원을 접근하기 위해 Key를 점유한다.
    
- 1번 프로세스는 키를 점유했기 때문에 공유 자원을 사용한다.
    
- 2번 프로세스가 공유 자원을 사용하기를 원한다.
    
- 2번 프로세스는 키를 점유하기 위해 대기한다.
    
- 3번 프로세스 또한 공유 자원을 사용하기 위해 2번 프로세스 다음 순번으로 대기한다.
    
- 1번 프로세스가 공유 자원을 다 사용하고 Key를 반환한다.
    
- 2번 프로세스는 대기하고 있다가 반환된 Key를 점유하고 공유 자원을 사용한다.


**(예시)**

![](https://i.imgur.com/6q9ueph.png)
프로세스는 자원에 접근하기 위해 열쇠(lock)를 얻고 화장실(자원)을 쓴다.
다 쓰고 키(unlock)을 반납한다. 

뮤텍스에서는 3가지 알고리즘을 사용한다고 한다.
1. 데커알고리즘
2. 피터슨 알고리즘
3. 제과점 알고리즘 



### 세마포어란?
공유 자원에 대한 접속을 제어하기 위해 최대 허용치만큼 접근 요청을 가능하게 하여 카운트를 세서 카운트가 0이되면 대기하도록 하여 상호 배제를 달성하는 기법입니다.

![](https://i.imgur.com/w88Hkst.png)

앞선 방법들과의 차이점을 제시하자면,
앞선 방법은 프로세스가 임계 영역에 진입할 수 없을 때 진입 조건이 true 가 될 때까지 반복적으로 조사하고 바쁜 대기를 하기 때문에 프로세스를 낭비한다. 따라서, 진입 조건을 반복 조사하지 않고 true일때 프로세스 상태를 확인한다면, 프로세서 사이클을 낭비하지 않을 것입니다.

##### 과정

- 공유 자원에 대한 최대 허용치를 정의한다. 우선, 3으로 해보겠다.
    
- 1번 프로세스가 공유 자원에 접근한다. 허용치는 2로 감소하였다.
    
- 2번 프로세스가 공유 자원에 접근한다. 허용치는 1로 감소하였다.
    
- 3번 프로세스가 공유 자원에 접근한다. 허용치는 0로 감소하였다.
    
- 4번 프로세스가 공유 자원에 접근한다. 허용치가 0이므로 대기한다.
    
- 2번 프로세스가 공유 자원을 다 사용하였다. 허용치는 1로 증가하였다.
    
- 4번 프로세스는 대기 하다 허용치가 1로 증가되어 공유 자원에 접근한다. 허용치는 다시 0으로 감소하였다.



이또한 예시를 통해 알아봅시다.

![](https://i.imgur.com/o4BH3M6.png)
위 그림은 카운팅 세마포어를 쉽게 이해할 수 있는 예시입니다. 즉, 유한한 개수를 가진 자원에 대한 접근을 제어하는데에 사용할 수 있습니다. 

그리고 다른 방법은 이진 세마포어가 있습니다. 세마포어의 초기 값이 0 또는 1만 가질 수 있는 세마포어 입니다. (뮤텍스가 이진 세마포어와 비슷한 것이라 생각하면 됩니다.)


### 뮤텍스와 세마포어의 차이

- 세마포어는 뮤텍스가 될 수 있지만, 뮤텍스는 세마포어가 될 수 없다.
    
- 세마포어는 소유할 수 없으며, 뮤텍스는 소유할 수 있고 소유주가 그에 대한 책임을 가진다.
    
- 세마포어는 동기화 대상이 여러개 일 때 사용하고, 뮤텍스는 동기화 대상이 오로지 하나 일 때 사용된다.



</div>
</details>

<details>
<summary>Q.PCB란 무엇이고, 왜 필요한지?</summary>
<div markdown="1">

#### **PCB (Process Control Block)**

PCB(프로세스 제어 블록)는 운영체제에서 프로세스를 관리하기 위해 해당 프로세스의 상태 정보를 담고 있는 자료구조를 말한다.

프로세스를 컨텍스트 스위칭 할때 기존 프로세스의 상태를 어딘가에 저장해 둬야 다음에 똑같은 작업을 이어서 할 수 있을 것이고, 새로 해야 할 작업의 상태 또한 알아야 어디서부터 다시 작업을 시작할지 결정할 수 있을 것이다. 즉, PCB는 프로세스 스케줄링을 위해 프로세스에 관한 모든 정보 저장하는 **임시 저장소**인 것이다. 

![](https://i.imgur.com/5LZ83z1.png)

따라서 운영체제는 PCB에 담긴 프로세스 고유 정보를 통해 프로세스를 관리하며, 프로세스의 실행 상태를 파악하고, 우선순위를 조정하며, 스케줄링을 수행하고, 다른 프로세스와의 동기화를 제어한다. 

운영체제에 따라 PCB에 포함되는 항목이 다를 수 있지만 일반적으로 PCB내 에는 다음과 같은 정보가 포함되어 있다.

![](https://i.imgur.com/vh9Kho9.png)


##### context switching 과정 
![](https://i.imgur.com/sJMt2zS.png)



</div>
</details>


<details>
<summary>Q. 스택, 데이터, 코드에 대해 설명해주세요.</summary>
<div markdown="1">

   ![](https://i.imgur.com/MIUCWIZ.png)

- **코드 영역(Code / Text)** : 프로그래머가 작성한 프로그램 함수들의 코드가 CPU가 해석 가능한 기계어 형태로 저장되어 있다.
- **데이터 영역(Data)** : 코드가 실행되면서 사용하는 전역 변수나 각종 데이터들이 모여있다. 데이터영역은 .data ,.rodata, .bss 영역으로 세분화 된다.
    - .data : 전역 변수 또는 static 변수 등 프로그램이 사용하는 데이터를 저장
    - .BSS : 초기값 없는 전역 변수, static 변수가 저장
    - .rodata : const같은 상수 키워드 선언 된 변수나 문자열 상수가 저장
- **스택 영역(Stack)** : 지역 변수와 같은 호출한 함수가 종료되면 되돌아올 임시적인 자료를 저장하는 독립적인 공간이다. Stack은 함수의 호출과 함께 할당되며, 함수의 호출이 완료되면 소멸한다. 만일 stack 영역을 초과하면 stack overflow 에러가 발생한다.
- **힙 영역(Heap)** : 생성자, 인스턴스와 같은 동적으로 할당되는 데이터들을 위해 존재하는 공간이다. 사용자에 의해 메모리 공간이 동적으로 할당되고 해제된다.


</div>
</details>

(오늘은 여기까지)

---

<details>
<summary>Q.사용자 수준 스레드 vs 커널 수준 스레드 차이는?</summary>
<div markdown="1">


</div>
</details>

<details>
<summary>Q.4 CPU 환경에서 4개의 쓰레드가 실행된다고 가정해보자. 어떤 문제가 발생할 수 있겠는가?</summary>
<div markdown="1">


</div>
</details>


<details>
<summary>Q.동기와 비동기의 차이?</summary>
<div markdown="1">


</div>
</details>


<details>
<summary>Q.가상 메모리란?</summary>
<div markdown="1">


</div>
</details>

<details>
<summary>Q.외부 단편화와 내부 단편화란?</summary>
<div markdown="1">


</div>
</details>

<details>
<summary>Q.페이징과 세그먼테이션이란?</summary>
<div markdown="1">


</div>
</details>

<details>
<summary>Q.비선점형(Non-preemptive) 스케줄링</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q.선점형(Non-preemptive) 스케줄링</summary>
<div markdown="1">


</div>
</details>

<details>
<summary>Q.인터럽트란 무엇인가요?</summary>
<div markdown="1">


</div>
</details>

<details>
<summary>Q.운영체제한테 CPU가 넘어가는 경우는 언제인가?.</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q.인터럽트 처리중에 또다른 인터럽트가 발생하는 경우는 어떻게 되는가?</summary>
<div markdown="1">


</div>
</details>


### 리눅스 



<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>

<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>


<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>

<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>

<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>
<details>
<summary>Q..</summary>
<div markdown="1">


</div>
</details>


---

### <u>Reference.</u>
- [기똥찬 프로세스/스레드 설명글](https://inpa.tistory.com/entry/%F0%9F%91%A9%E2%80%8D%F0%9F%92%BB-%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4-%E2%9A%94%EF%B8%8F-%EC%93%B0%EB%A0%88%EB%93%9C-%EC%B0%A8%EC%9D%B4)
- [이것도 좋아요 프로세스/스레드](https://gmlwjd9405.github.io/2018/09/14/process-vs-thread.html)
- [뮤텍스와 세마포어](https://incheol-jung.gitbook.io/docs/q-and-a/computer-science/undefined-1)