## C
C는 1973년에 벨 연구소의 데니스 리치(Dennis Ritchie)가 개발했고,   
아직도 폭넓게 사용되며 가장 인기있는 언어 중 하나이다.   
```c
#include <stdio.h>
int main() {
  int num, sum;
  sum = 0;
  while (scanf("%d", &num) != EOF && num != 0)
    sum = sum + num;
  printf("%d\n", sum);
  return 0;
}
```
<br/>

## C++
1980년대에 들어서는 규모가 매우 큰 프로그램의 복잡성 관리를 도울 의도로 설계된 언어들이 개발되었고, C++가 대표적이다.   
C++는 벨 연구소의 비야네 스트롭스트룹(Bjarne Stroustrup)이 개발했다.   
C프로그램은 대부분 C++프로그램에서도 유효하지만, 그 반대는 그렇지 않다.   
```c++
#include <iostream>
using namespace std;
int main() {
  int num, sum;
  sum = 0;
  while (cin >> num && num != 0)
    sum = sum + num;
  cout << sum << endl;
  return 0;
}
```
<br/>

## JAVA
1990년대에는 인터넷과 월드 와이드 웹의 성장에 대응하여 더 많은 언어가 개발됐다.   
프로그래밍을 빠르고 편하게 하는 것이 컴퓨터가 효율적으로 돌아가도록 하는 것보다 더 중요해졌다.   
자바는 1990년대 썬 마이크로시스템즈의 제임스 고슬링(James Gosling)이 개발했다.   
자바는 원래 유연성이 중요한 가전 제품과 전자 기기 같은 작은 임베디드 시스템에 사용했으나 현재에는 웹 서버에 널리 사용되고 있다.   
자바는 안드로이드 앱을 작성하는 주요 언어이기도 하며 C++보다 단순하지만 C보다는 더 복잡하다 또한 C보다 더 안전하기도 해서   
프로그래밍 수업에서 처음 배우는 언어로 인기가 높다.   
```java
import java.util.*;

class Addup {
  public static void main (String[] args) {
    Scanner keyboard = new Scanner(System.in);
    int num, sum;
    sum = 0;
    num = keyboard.nextInt();
    
    while (num != 0) {
      sum = sum + num;
      num = keyboard.nextInt();
    }
    
    System.out.println(sum);
  }
}
```
<br/>

## Javascript
자바스크립트는 1995년 넷스케이프에서 근무하던 브렌던 아이크(Brendan Eich)가 만들었다.   
자바스크립트는 처음부터 웹페이지의 동적인 효과를 구현하기 위해 브라우저 내부에서 사용할 목적으로 설계되었고, 오늘날 거의 모든 웹페이지는 자바스크립트 코드를 어느정도 포함하고 있다.   
```javascript
var num, sum;
sum = 0;
num = prompt("Enter new value, or 0 to end");

while (num != '0') {
  sum = sum + parseInt(num);
  num = prompt("Enter new value, or 0 to end");
}

alert(sum);
```
<br/>

## Python
파이썬은 네덜란드 암스테르담의 CWI에서 일하던 귀도 반 로섬(Guido van Rossum)이 개발해서 1991년에 처음 발표되었다.   
파이썬은 문장을 그룹화하는 데 중괄호 대신 들여쓰기를 사용한다는 특징이 있다.   
파이썬은 가독성에 초점을 두고 설계되었고, 배우기 쉽고, 라이브러리를 풍부하게 제공하기 때문에 가장 널리 사용되는 언어 중하나로 자리 잡았다.   
```python
sum = 0
num = input()

while num != '0':
  sum = sum + int(num)
  num = input()

print(sum)
```
<br/>
<br/>

특정 작업을 하는 프로그램을 작성하는 데는 항상 많은 방법이 있다. 이러한 의미에서 프로그래밍은 작문과 비슷하다.   
현재 널리 사용되는 언어는 100개 미만이지만, 지금까지 수천 개의 프로그래밍 언어가 발명되었다.   
각 언어는 효율성, 표현력, 안전성, 복잡성 같은 문제 간 트레이드오프를 고려해서 만들어진 결과물이다.
