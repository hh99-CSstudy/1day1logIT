## 라이브러리
: 파이썬의 print() 와 같은 함수 모음.
프로그램 개발자가 사용자를 위해 미리 만들어 놓은 함수들.

 
## 애플리케이션 프로그래밍 인터페이스 (Application Programming Interface) 
: 관련 없는 두 애플리케이션이 서로 통신할 수 있도록 하는 소프트웨어 중개자. 
한 프로그램에서 요청이나 메시지를 받은 다음 다른 프로그램으로 전달하고 API가 수행하도록 프로그래밍된 작업을 기반으로 메시지를 번역하고 프로토콜을 수행하는 브리지 역할. 
API는 플러그인, 디지털 인터페이스 및 소프트웨어 통신과 같은 현대 디지털 생활의 거의 모든 측면에 존재. API는 모든 것을 함께 연결하고 소프트웨어 시스템이 조화롭게 작동하도록 합니다.

<img src = "https://user-images.githubusercontent.com/105165279/171988086-14e7b59a-2440-45d1-a6ff-1910bff74d1d.png" width =500px>

- 함수의 용도, 사용법, 요구되는 입력 데이터, 출력되는 값 등을 나열
- 시스템 내부에서 주고받는 구조 기술

<img src = "https://user-images.githubusercontent.com/105165279/171988148-3c2283bd-c958-4db8-b3e1-841a2e4b0a1c.png" width =500px>

- <b>REST API</b> : HTTP통신에서 어떤 자원에 대한 CRUD요청을 Resource와 Method로 표현하여 특정한 형태로 전달하는 방식.
  REST (REpresentational State Transfer)는 어떤 자원에 대해 CRUD(Create, Read, Update, Delete)연산을 수행하기 위해 UR(Resource)로 요청을 보내는 것으로
  Get, Post 등의 방식(Method)을 사용하여 요청을 보내며, 요청을 위한 자원은 특정한 형태(Representation of Resource)으로 표현된다.
  그리고 이러한 REST 기반의 API를 웹으로 구현한 것이 RESTful API 인데 예를 들어, 우리는 게시글을 작성하기 위해 “http://localhost:8080/board” 라는
  URI에 POST방식을 사용하여 JSON형태의 데이터를 전달할 수 있다.
 

## 소프트웨어 개발 키트 (Software Development Kit)
: 대규모 시스템은 프로그래머들이 복잡한 소프트웨어 라이브러리를 잘 다룰 수 있도록 SDK 제공
ex) IOS 개발환경, 지원도구

 
## 버그
: 1947년 호퍼와 동료들은 기계식 컴퓨터에서 죽은 나방을 발견했고, 호퍼는 동료들이 컴퓨터를 디버깅(debugging) 하고 있다고 말함.
 하지만 1889년 에디슨이 축음기에서 버그를 찾았다는 옥스퍼드 영어 사전에 따르면 유래가 더 오래된 것으로 보임.
 버그는 시스템을 공격에 취약하게 만든다. 버그 때문에 공격자가 메모리에 악성코드를 심어 놓기 쉽기 때문이다. 때문에 소프트웨어 업데이트를 해야하며,
 사용자들은 소프트웨어를 최신 상태로 유지해야한다. 그리고 새로운 하드웨어가 개발되면 새로운 소프트웨어가 필요하다.
 끊임없는 변화에 뒤처지지 않는 소프트웨어 유지보수는 중요하며, 그렇지 않으면 '비트 부식'을 겪게된다.
 <b>비트부식</b>은 재컴파일 불가, 라이브러리 변동으로 작동불가, 업데이트 불가 상태를 야기한다.
