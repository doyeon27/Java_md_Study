12월 6일 수

# 36강 패키지, 부제 : 1반 영희와 2반 영희

#### 패키지
- 클래스는 패키지를 이용하여 관련된 클래스 들을 관리 함
- 자바에서 패키지는 폴더와 같은 기능을 제공한다고 보면 됨

#### 패키지 이름 규칙
- 패키지 이름은 보통 도메인 이름을 거꾸로 적은 후에 프로젝트 이름 등을 붙여서 만들게 됨

#### 패키지 선언방법
- package 패키지명;
- 주석문이나 빈줄을 제외하고 가장 윗 줄에 위와 같은 형식으로 선언

#### 패키지를 사용할 땐 import 문장을 사용함
- import 패키지명.클래스명;

#### 패키지가 정의된 클래스 컴파일 하기
- javac -d 경로명 *.java
- -d 옵션을 사용함

#### 패키지 연습하기
- com.exapmle.util 이란 package 에  Calculator 클래스를 작성
- 해당 클래스는 int plus(int, int), int minus(int, int)메소드를 가짐
- com.exapmle.main 이란 package 에 CalculatorTest 클래스를 작성
- 해당 클래스는 Calculator 클래스 인스턴스를 생성한 후 plus, minus 메소드를 호출한 결과를 출력함