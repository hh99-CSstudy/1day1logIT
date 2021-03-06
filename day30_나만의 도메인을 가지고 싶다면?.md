# IETF (Internet Engineering Task Force)
> 국제 인터넷 표준화 기구는 인터넷의 운영, 관리, 개발에 대해 협의하고 프로토콜과 구조적인 사안들을 분석하는 인터넷 표준화 작업 기구 이다. 

# RFC (Request for Comments)
> 인터넷 기술에 적용 가능한 새로운 연구, 혁신, 기법 등을 아우르는 문서를 나타낸다. 인터넷 협회에서 기술자 및 컴퓨터 과학자들은 RFC 메모의 형태로 생각을 출판하게 되었다. IETF는 일부 RFC를 인터넷 표준으로 받아들이기도 한다.

# ICANN (Internet Coporation for Assigned Names and Numbers)
> 국제 인터넷 주소 관리 기구는 도메인 네임, IP 주소, 일부 프로토콜 정보처럼 인터넷이 제대로 작동하려면 고유하게 유지돼야 하는 이름과 번호를 할당한다. 도메인 네임 등록 대행 업체에 권한을 승인하고, 등록 대행 업체는 개인이나 단체에 도메인 네임을 할당한다. 

# 도메인 네임 시스템(DNS)
> * 웹사이트에 접속 할 때 우리는 외우기 어려운 IP 주소 대신 도메인 이름을 사용한다.
* 도메인 이름을 사용했을 때 입력한 도메인을 실제 네트워크상에서 사용하는 IP 주소로 바꾸고 해당 IP 주소로 접속하는 과정이 필요하다.
* 이러한 과정, 전체 시스템을 DNS(도메인 네임 시스템)라고 한다.
* 이러한 시스템은 전세계적으로 약속된 규칙을 공유한다.
* 상위 기관에서 인증된 기관에게 도메인을 생성하거나 IP 주소로 변경할 수 있는 ‘권한’을 부여한다.
* DNS는 이처럼 상위 기관과 하위 기관과 같은 ‘계층 구조’를 가지는 분산 데이터베이스 구조를 가진다.

# IP주소
![](https://velog.velcdn.com/images/mocakosan/post/41c9c301-b9de-4908-bd14-b24346c35f2f/image.png)
> 컴퓨터 네트워크에서 장치들이 서로를 인식하고 통신을 하기 위해서 사용하는 특수한 번호이다. 
 - 각 네트워크와 연결된 각각의 호스트 컴퓨터는 다른 개체와 통신 할 수 있도록 IP주소가 있어야 한다.
- IPv4 주소의 최대 개수는 2^32개 43억 개에 불과 하다. 통신 서비스 사용이 증가하는 속도를 고려하면 언젠가는 다 소진될 것이다.
- 여러 개의 호스트를 단일 IP 주소에 편승하게 하는 기법을 사용하면 여유가 생긴다. 일반적으로 가정용 무선 공유기는 일반적으로 네트워크 주소 변환(Network Address Translation) , 즉 NAT 기술을 사용한다.
- 이 기술은 단일 외부 IP 주소로 여러 개의 내부 IP 주소에 서비스를 제공할 수 있도록 한다.
- 전 세계적으로 128비트 주소를 사용하는 IPv6로 전환하여 점점 널리 사용되는 추세이다

# 루트 서버
> DNS가 제공하는 매우 중요한 서비스는 도메인 네임을 IP 주소로 변환하는 것이다.
- 최상위 도메인은 모든 최상위 도메인의 IP 주소를 알고 있는 일련의 루트 네임 서버에 의해 처리된다.
- 실제로는 네임 서버가 최근에 조회되어 자신을 거쳐 간 이름과 주소에 대해 캐시를 유지하고 있어서, 새로운 요청이 왔을 때 멀리서 찾을 필요 없이 로컬 정보로 응답한다.
- 루트 서버 대부분은 서로 멀리 떨어져 있는 여러 대의 컴퓨터로 구성되어 있다.
- 이 컴퓨터들은 단일 컴퓨터처럼 작동하지만 루트 서버를 구성하는 컴퓨터 중 가까이 있는 컴퓨터에 요청을 라우팅하는 프로토콜을 사용한다.


