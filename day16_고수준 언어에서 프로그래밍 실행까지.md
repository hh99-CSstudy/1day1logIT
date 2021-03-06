# 어셈블리와 고수준 언어

## 어셈블리 언어
기계에 특화된 언어로 대개 프로세서의 명령어와 일대일로 연결되고, 명령어가 이진수로 인코딩 되는 등 특정한 방식과 메모리에 정보가 배치되는 방식을 알고있다.  어셈블리 언어로 인해 프로그래머들은 명령어에 의미있는 단어를 붙이는 등 소프트웨어에서 가장 중요한 발전을 이루는데 핵심적인 기여를 했다.

## 고수준 프로그래밍 언어

우리가 아는 C,C++,Java,Javascript,Python 등..의 프로그래밍 언어
고수준 언어는 사람이 표현하는 방식에 가까운 용어로 계산 과정을 작성할 수 있다.
고수준 언어로 작성된 코드는 컴파일러에 의해 프로세서의 어셈블리 언어로 된 명령어로 변환되고, 어셈블러에 의해 비트로 변환되어 메모리에 로드되고 실행된다.

## 컴파일러의 컴파일 과정
어셈블러는 각자의 어셈블리 언어 명령어를 실제 명령어의 비트 패턴으로 변환하는 일 뿐만 아니라 저장할 메모리 위치를 확보하는 일을 담당한다. 기계와 1:1로 대응되는 특징을 갖고있기 때문에 같은 고수준 언어의 입력 표현은 아래와 같이 서로 다른 명령어와 비트 패턴으로 컴파일된다

>                              Z = X + Y
			     	     		ㅣ
            ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ
            ㅣ                                       ㅣ
	     컴파일러#1                               컴파일러#2
    [LOAD X, ADD Y, STORE Z]               [COPY X,Z / ADD Y,Z]
            ㅣ                                       ㅣ
         어셈블러#1	    						어셈블러 #2
     [100101001010....]                     [001001110101...]



실제로는 위에서 독립적인 여러개의 컴파일러를 이용하는 것 보단 실제로는 아래와 같이 나뉠 수 있다.

프런트엔드 : 프로그램 코드의 유효성을 검사하고 고수준 프로그래밍 언어로 작성된 프로그램을 ** 어떤 중간 형태로 만듬**
백엔드 : 공통된 중간 표현을 아키텍처에 맞는 어셈블리 언어로 변환

>   intermediate representation(중간 표현)
어떤 중간 표현은 하이레벨 언어와 매우 유사한 형태를 가지며 어떤 중간 표현은 중간 표현이 어셈블리 코드와 유사한 경우도 있다.
중요한 것은 컴파일러는 동시에 여러 가지 형태의 중간 표현을 가지지 않는 것이다.

### 컴파일러의 최적화기
여기서 컴파일러는 코드의 효율성을 높이기 위해 최적화기(optimizer)를 이용한다.
코드 성능을 최고로 향상시키고 프로그램 바이너리의 크기를 줄이기 위함.
- 코드 구조 최적화
  최적화기는 코드의 의미를 그대로 유지하면서 동시에 효율성을 높이기 위해 코드의 구조를 변경시키곤 한다. 예를 들어 반복문은 부분적으로나 전체적으로 해제되기도 한다. 반복문의 해제는 점프 명령을 이용해서 같은 코드 부분은 반복 실행하는 대신 단순히 반복할 코드를 복제해서 연속적으로 수행하는 것을 의미한다. 이렇게 하면 바이너리의 크기는 커지지만 카운터를 관리할 필요가 없어지고 조건에 따라서 실행을 분기시킬 필요가 없다. 또한 반복문은 부분적으로 해제해서 반복 실행을 감소시킬 수도 있다.

- 잉여 제거 최적화(redundancy elimination)
  잉여 제거는 코드 최적화 분야에서 상당히 중요한 요소다. 프로그래머는 똑같은 계산을 한 번 이상 반복하거나 전혀 사용하지 않는 변수에 값을 할당하는 일과 같은 쓸데 없는 코드를 만들어 내곤 한다. 최적화기는 이런 제거 가능한 코드를 찾아내서 그것을 실제로 제거하기 위한 알고리즘을 가지고 있다.

가독성에 직접 영향을 미치는 최적화 작업은 최적화기에 의해서 수행되는 것이 아니라 백엔드에서 수행되는 프로세서 관련 최적화 작업에 의해서 이뤄진다.

## 고수준 언어의 이점

- 사람이 생각하는 방식에 더 가까워 배우고 사용하기 쉽다.
- 특정 아키텍처에 종속되지 않는다. 한번만 작성하면 다양한 컴퓨터에서 실행 가능
- 컴파일 단계에서 에러들을 미리 점검하게 해준다. 어셈블리 언어는 논리적인 흐름이나 전후 관계를 파악하지 못하여 구문 오류 이외의 에러는 검출하기 어렵다.

## 초기의 고수준 언어들

### 포트란(FORTRAN)
수식 변환'Formula Translation'에서 이름이 유래됨. 과학과 공학 분야에서 계산을 표현하는 데 성공적으로 사용됨. 오늘날 아직도 건재한 언어
### 코볼 (CO-BOL, Common Business Oriented Language)
사무 데이터 처리 목적으로 사용되어 자료구조와 계산을 쉽게 표현할 수 있는 언어적 특징이 있다. 오래전 개발되어 사용되는 코볼 프로그램은 많지만 프로그래머는 많지 않다.
### 베이직(BASIC, Beginner's All-purpose Symbolic Instruction Code)
이름처럼 프로그래밍 교육을 위한 쉬운 언어로 만들어졌다. 특히 간단하면서 컴퓨팅 자원을 적게 필요로 하여 개인용 컴퓨터에서 사용할 수 있는 첫 번째 고수준 언어였다. 마이크로소프트 창업자인 빌 게이츠와 폴 앨런이 마이크로컴퓨터용 베이직 컴파일러를 만들면서 사업을 시작함. 이 변종이 바로 비주얼 베이직(Visual Basic)

초창기 컴퓨터는 비싸고, 느리고, 성능의 한계로 인해 고수준 언어가 비효율적이라고 했으나 지금은 컴퓨터의 발전과 컴파일러 개발자들의 노력으로 인해 프로그래머가 개별 명령어 수준의 효율성 까지 걱정하는 경우는 드물다.

출처 - 리버싱: 리버스 엔지니어링 비밀을 파헤치다 / 1일 1로그 100일 완성 IT 지식
