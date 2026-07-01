## Class 커스텀 함수에서 등록하는 문법

    def __init__(self, )

## 'Customer(고객)'라는 이름의 커스텀 자료형 '틀(설계도)' 만들기
    
    class Customer:
    # 이 자료형이 만들어질 때 가질 세부 데이터(속성)를 정합니다.
    def __init__(self, name, age, gender):
        self.name = name        # 고객 이름 데이터
        self.age = age          # 고객 나이 데이터
        self.gender = gender    # 고객 성별 데이터


    # 이 자료형만 사용할 수 있는 전용 기능(메서드)을 정합니다.
    def purchase(self, price, product_name):
        print(f"{self.name} 고객님이 {price}원 상당의 {product_name}를 구매하셨습니다.")

## 'Customer' 클래스를 이용해서 구체적인 데이터 생성하기
    client1 = Customer(name ="철수", age = 24, gender = "남성")
    client2 = Customer("김혜수", 55, "여성")

# 데이터 꺼내기

## 첫 번쨰 고객님의 이름 추출
    print(f'첫 번쨰 고객님의 이름은 {client1.name} 입니다')

    print("-"*80)

## 두 번째 고객님의 이름 추출
    print(f'두 번째 고객님의 나이는 {client2.age} 입니다')

## 전용 함수(메소드) 실행하기
    client1.purchase(price = 900000, product_name = "아이패드")
