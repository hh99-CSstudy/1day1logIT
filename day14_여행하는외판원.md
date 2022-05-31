## NP-P

<img src="https://upload.wikimedia.org/wikipedia/commons/4/4a/Complexity_classes.png" width="500">
<img src="https://blog.chulgil.me/content/images/2019/02/Screen-Shot-2019-02-07-at-2.31.54-PM-1.png" width="500"><br>

- P(Polynomial, 다항)
    - 쉬운 문제는 복잡도 면에서 다항시간 내에 해결할 수 있고 이러한 문제를 P이라고 부른다

- NP(Nondeterministic Polynomial, 비결정적 다항)
    - 지수 알고리즘(2^n)이 필요한 문제는 일반적인 다항 알고리즘으로 풀수 없고 이를 NP이라고 한다
  - 적절한 알고리즘으로 풀이한다면 다항 시간내에 해결될 수 있지만 이론적인 개념일 뿐이다
- NP-완전(NP-complete, NP-C, NPC)은 NP 집합에 속하는 결정 문제 중에서 가장 어려운 문제의 부분집합


## NP : 여행하는 외판원 문제
<img src="https://seongjaemoon.github.io/assets/uploads/algorithm/tsp.png" width="500"><br>
- 외판원은 자신이 사는 도시에서 출발, 어떤 순서든 다른 도시를 모두 방문하고 돌아와야 하는데 반복없이 정확히 한번씩만 방문하면서 최단거리를 만드는 문제이다
- 풀이법
    - *최근접 이웃 휴리스틱* : 아직 방문하지 않은 도시중 가장 가까운 도시로 이동하는 방식으로 최단거리를 보장할 수 없다
    - *브루트 포스(완전탐색)* : 외판원 문제는 오랫동안 연구됬지만 여전히 모든 경우의 수를 완전 탐색해서 찾는 방법밖에 없다
      - 10개의 도시를 방문한다면 실행 가능하겠지만 100개나 1000개의 도시는 실행할수 없다

- 이런 문제들은 완전 탐색하는 것 밖에 방법이 없다 
  - 스티븐 쿡은 이런 문제들이 비슷해서 한 문제라도 다항 시간 알고리즘을 찾을 수 있다면 모든 문제에 대한 다항 시간 알고리즘을 찾아낼 수 있다고 말했다