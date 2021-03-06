
## 이진탐색
: 배열 내부 데이터가 정렬되어 있어야만 사용할 수 있는 알고리즘. 탐색 범위를 절반씩 좁혀가며 데이터를 탐색하는 특징이 있다. </br>
이진 탐색은 위치를 나타내는 변수 3개(시작점, 끝점, 중간점)를 사용한다. </br>
찾으려는 데이터와 중간점 위치에 있는 데이터를 반복적으로 비교해서 원하는 데이터를 찾는다.
중간점이 실수일때는 소수점 이하를 버린다.

<img src= "https://user-images.githubusercontent.com/105165279/170898590-f415a990-b75e-47f7-9bab-6aee835dfc16.png" width=300px>

전체 데이터 개수는 9개지만, 이진 탐색을 통해 3번만에 찾을 수 있었다.
이를 알고리즘 맥락에 맞춰 이야기하자만 로그는 어떤 수를 2로 나눠서 1에 도달하기까지의 횟수, 또는 2를 거듭제곱해서 그 수까지 도달하기까지의 횟수이다.
알고리즘에서 로그는 항상 밑수 2인 로그를 의미한다. 때문에 시간복잡도는 O(logN)이다.

### 이름 데이터가 1000개에서 2000개가 된다면?
: 알파벳 순으로 정렬된 이름 데이터가 1000개일때는 이름 10번을 확인하면 된다. (2의 10제곱 1024)
이름 데이터가 2000개로, 1000개가 늘어난 상황에서도 이름 11번을 확인하면 찾을 수 있다. (2의 11제곱 2048)
찾고자하는 이름이 최전방에 있는 경우를 제외하고는 순차(선형) 탐색보다 빠르다. 




## 선택정렬 vs 퀵정렬
: 이진 탐색을 하기 위해서는 알파벳순, 숫자순 처럼 정렬이 선행되어야한다. 정렬은 선택정렬, 삽입정렬, 퀵정렬, 계수정렬 등 다양하다.

### 선택정렬
: 가장 작은 데이터를 선택해 맨 앞에 있는 데이터와 바꾸고, 그 다음 작은 데이터를 선택해 앞에서 두 번째 데이터와 바꾸는 과정을 반복한다.

### 파이썬의 정렬은?
파이썬은 기본 정렬 라이브러리인 sorted() 함수를 제공한다.
sorted()는 퀵 정렬과 동작 방식이 비슷한 병합 정렬 + 삽입 정렬을 기반으로 한 하이브리드 방식으로 만들어졌는데,
병합 정렬은 일반적으로 퀵 정렬보다 느리지만 최악의 경우에도 시간 복잡도 O(NlogN)을 보장한다는 특징이 있다.
sorted() 는 다른 리스트를 이용하여 정렬된 리스트를 반환하는데, sort() 를 이용하면 내부 원소를 바로 정렬할 수 있다.
