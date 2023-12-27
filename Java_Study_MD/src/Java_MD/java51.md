12월 16일 토

# 51강 익명클래스와 처음 만나는 람다

#### 익명클래스 - 이름 없는 클래스(Anonymous Class)
- new 생성자(){...}
- 생성자 뒤에 중괄호가 나오고 코드를 오버라이딩 하여 보통 구현함

Car car = new Car();{
    public void run(){
        System.out.println("Car를 상속받는 이름없는 객체가 run 메소드를 오버라이딩 함");
    }
}