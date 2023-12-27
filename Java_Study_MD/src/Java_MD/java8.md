12월 2일 일

# 08강 타입의 변환

#### doulbe형 타입은 정수값이 잘 대입됨
- 다음은 가능함
- 이를 '묵시적 타입 변환'(자동 타입 변환, implicit conversion)이라고 함
- double d1 = 50;
  doulbe d2 = 500L;
- int형 리터럴 50, long형 리터럴 500L이 모두 d1,d2에 저장됨

#### int형 타입에 실수를 대입하면 오류가 발생함
- 실수는 정수를 포함하지만, 정수는 실수를 포함할 수 없기 때문에 아래의 코드는 컴파일 오류가 발생함
- int i1 = 50.0;
  int i2 = 25.4f; 

#### 실수 값을 정수에 저장하려면 형 변환을 해야함
- 실수 값을 정수타입의 변수에 저장하려면 정수타입으로 형 변환 해야 함. 변환 하고하 자는 값 앞에 ex -> (int) 를 붙임
- 주의 해야 할 점은 소수점 이하 부분은 잘림
- 이를 '명시적 타입 변환'(강제 타입 변환, explicit conversion) 이라고 함
- int i1 = (int)50.0;
  int i2 = (int)25.6f;

#### 크기가 큰 타입은 작은 타입을 저장할 수 있음
- long 타입의 변수는 byte, short, int 타입의 값을 저장할 수 있음
- int 타입의 변수는 byte, short 타입의 값을 저장할 수 있음
- short 타입의 변수는 byte 타입의 값을 저장할 수 있음
- short s = 5;
  int i = s;
  long x = i;

  System.out.println(i);
  System.out.println(x);
- 요류가 발생하지 않고 

#### 형 변환시 주의할 점
- 크기가 큰 타입을 작은 타입에 저장할 때는 오버플로우를 조심해야 함      

public class PrimitiveCastExam4Main {
    public static void main(String[] args){
        long x2 = 50;
        int i2 = (int)x2;
        System.out.println(x2);
        System.out.println(i2);

        System.out.println("---------------------------------");

        long x3 = Long.MAX_VALUE;
        int i3 = (int)x3;   <--- 이러면 오버플로우 됨(큰 타입을 작은 타입에 담았기 때문에, 그래서 출력하면 음수로 나옴)
        System.out.println(x3);
        System.out.println(i3);
    }
}

