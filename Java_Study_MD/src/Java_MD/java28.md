12월 4일 월

# 28강 객체지향문법 = 인스턴스 필드 & NullPointException은 왜 발생할까?

#### 클래스 메소드 vs 인스턴스 메소드
- 인스턴스 별로 다르게 동작해야 한다면 인스턴스 메소드
- static 메소드는 객체 생성이나 유틸리티 관련에서 사용될 때가 있음
- 되도록 인스턴스 메소드를 사용함

- static이 붙은 메소드는 '클래스 메소드'
- static이 붙지 않은 메소드는 '인스턴스 메소드'


#### 필드(field)
- 클래스가 가지는 속성을 자바 언어 에서는 필드라고 말함
- 다른 언어에서는 멤버변수 라고 말하는 경우도 있음
- 필드는 어떤 키워드와 함께 사용하느냐에 따라서 사용방법이 달라짐
- static 이라는 키워드가 함께 사용되는 필드는 클래스 필드, 함께 사용되지 않는 필드는 인스턴스 필드라고 함

- 필드 선언방법
  [접근제한자] [static] [final] 타입 필드명 [=초기값];  [] <- 는 생략이 가능하다
- 접근제한자는 public, protected, 아무것도 없는 경우(default), private이 올수 있음
- 필드명은 식별자 규칙을 따름. 다만 필드는 첫번째 글자는 소문자로 시작하는것이 관례
- 타입(type)은 기본형(boolean, btye, char, short, int, long, float, double)과 참조타입(class, 인터페이스, 배열)등 이 나올 수 있음
- 초기값이 없을 경우에는 참조형일 경우 null로 boolean형 일 경우는 false로 나머지 기본형은 모두 0 으로 초기화 됨

- 필드 선언 예제
  String name;
  String address = "경기도 고양시";
  public int age = 50;
  protected boolean flag;


☕Java: 클래스(필드, 메소드, 생성자) 개념 정리
https://velog.io/@yoondgu/Java-%ED%81%B4%EB%9E%98%EC%8A%A4%ED%95%84%EB%93%9C-%EB%A9%94%EC%86%8C%EB%93%9C-%EC%83%9D%EC%84%B1%EC%9E%90-%EA%B0%9C%EB%85%90-%EC%A0%95%EB%A6%AC