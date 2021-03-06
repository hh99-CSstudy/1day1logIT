# 데이터 압축
: 데이터를 압축하면 가용 메모리와 대역폭을 더 효율적으로 활용할 수 있다. 
압축의 기본 아이디어는 수신자가 재현하거나 유추 가능한 정보는 압축에서 제외하는 것이다. 
이렇게 하면 같은 파일을 더 적은 비트로 인코딩이 가능하다.
 ex) 미국 아스크코드에서 8번째 비트(가장 왼쪽 비트)는 항상 0이므로 아무 정보도 전달하지 않는데, 
 이런 비트는 인코딩에서 제외하여 7비트만 사용한다.


## 압축 종류
: 무손실 압축(압축해도 정보가 소실되지 않으므로 압축을 풀면 원본 소스가 정확하게 복원)과 
손실 압축(사람의 감각으로는 알아차리기 어려운 일부 미세한 세부 정보는 버려서 원본과 비슷하게 복원)이 있다.

 

### 이미지
  - GIF : 무손실 압축.  256색 지원
  - PNG : 무손실 압축. 1천 600백 색 지원
  -  JPEG : 손실 압축. 원본 이미지를 1/10로 압축


### 영상
  - MPEG : 손실 압축. 한 프레임에서 다음 프레임으로 갈 때 크게 변하지 않는 일련의 블록을 압축.


### 오디오
  - MP3, AAC : 손실 압축. 지각 부호화 알고리즘. 시끄러운 소리가 조용한 소리를 가리고, 사람의 청각 보다 높은 주파수는 삭제. 표준 오디오를 1/10로 압축.

 
 </br>
  </br>
 
# 오류 검출, 수정 알고리즘
: 오류 검출를 검출하고 수정까지 할 수 있게 하는, 신중하게 제어된 여분의 정보를 추가하는 과정.


### 체크섬 알고리즘
: 카드 번호 등에 사용. 가장 오른쪽 숫자에서 시작하여 왼쪽으로 가면서 각 숫자에 1과 2를 번갈아 곱한다.
곱해서 나온 값이 9보다 크면 9를 뺀 뒤, 각 자리 숫자들을 더했을 때 10으로 나누어 떨어져야한다.

### 페리티 코드
: 각 비트 그룹에 붙어서 그룹 내에서 값이 1인 비트의 총 개수가 짝수가 되도록 만든다. 
이후 단일 비트 오류가 발생하면 수신자는 1인 비트 개수가 홀수인 것을 보고 무엇인가 손상되었음을 알게된다.
물론 어느 비트에 오류가 있는지는 식별할 수 없으며, 짝수 개의 오류가 발생하면 검출할 수 없다.


## 활용 범위
주기억 장치는 패리티 비트를 사용하여 임의 위치에서 발생하는 단일 비트 오류를 검출한다.
CD와 DVD에서는 연속적으로 손상된 비트를 수정하는 코드로 사용하고, 휴대전화는 짧게 집중적으로 발생하는 노이즈 신호에 대처한다.
