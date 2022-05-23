# 연속과 불연속
> 이진 숫자, 줄여서 bit는 존 투키가 제안한 단어이다 - 클로드 새넌

### 컴퓨터의 정보 표현
<img src="https://images.velog.io/images/hshs0409/post/6346fdee-9f2a-4532-a114-3a2f2018ea5d/image.png" width="700px">
<ol>
<li>컴퓨터는 디지털 처리장치로 불연속적(이산적)인 값을 사용한다</li> 
<li>컴퓨터는 정보를 비트로 표현한다</li>
<li>비트는 모여서 더 큰 정보를 표현한다</li>
</ol>



### 아날로그와 디지털
<ul>
	<img src="https://simage.mujikorea.net/goods/31/05/12/88/4547315915224_N_N_400.jpg" width="250px">
	<img src="http://image.mujikorea.net/goods/31/04/73/97/4547315831982_N_N_400.jpg" width="250px">
    <li> 컴퓨터는 디지털 데이터를 다룬다</li>
    <li> 현실의 데이터는 입력단에서 최대한 일찍 디지털 형태로 변환되고 출력단에서 최대한 늦게 아날로그로 변환된다</li>
</ul>


# 아날로그 정보를 디지털로 바꾸기
### 이미지 디지털화
<ul>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f8/Photodiode-closeup.jpg/540px-Photodiode-closeup.jpg" width="250px">
    <li>광 검출 소자 </li>
    <ul>
        <li>빛의 강도를 전기 신호로 변환, 검출하는 장치</li>
        <li>RGB(적색, 녹색, 청색) 필터를 통과한 빛을 전기신호로 변환한다 </li>
        <li>광검출 소자나 검출하는 광신호의 종류에 따라 다이오드형 광검출소자, 광전도체형 광검출소자등이 있다.</li>
    </ul>
    <li> 사진 데이터는 이렇게 변환된 값의 배열이다</li>
</ul>


### 음향 디지털화
<ul>
<img src="https://t1.daumcdn.net/cfile/tistory/214ABC4458725BA232" width="500px">
    <li> 소리란 </li>
    <ul>
        <li> 진동이 발생해서 공기의 압력 변화를 일으켜 파동의 형태로 고막을 진동시키는 것</li>
        <li> 이런 공기의 압력 변화를 변환하면 녹음, 재생이 가능해진다  </li>
    </ul>
    <li> 파형의 측정값을 모아서 곡선의 값에 가까운 값을 얻을 수 있다</li>
</ul>


### 영화 디지털화
<ul>
    <li> 영상은 사진을 빠르게 이어서 보여주는 것으로 인간의 눈은 이것을 연속적인 움직임으로 인지한다 </li>
    <li> 영화는 초당 24프레임, 비디오 게임은 일반적으로 초당 60프레임을 사용한다</li>
</ul>

### 텍스트 디지털화
<ul>
    <img src="https://patentimages.storage.googleapis.com/c1/0a/19/3e7be16e5dc0bf/pat00002.png" width="500px">
    <li>ASCII(아스키 코드), Unicode등 문자에 고유한 숫자 값을 지정해서 bit를 문자로 변환한다</li>
</ul>