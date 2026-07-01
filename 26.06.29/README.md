# 라이브러리, 패키지, 모듈의 관계

<img width="463" height="375" alt="image" src="https://github.com/user-attachments/assets/94a9686e-64e5-4ee8-a091-1abba1d46dcb" />

    # 폴더를 묶어놓은게 패키지
    # 보통 크롤링할 때 urllib.request 안에 있는 내용을 긁어온다.
    # 도서관으로 예를 들면 책들이 (module) -> 책들이 모여 경제,지식들이 되는게 (패키지) -> 이런 것들이 모여 도서관(라이브러리)

--------------------


# 1. python 내장 모듈 - random 모듈을 이용한 로또 번호 추출

### 필요한 모듈 임포트(하드 디스크 -> 메모리 RAM)
    import random

### 1부터 45까지 정수 범위 설정(start=1, stop=46)
    numbers = range(1,46)

### 중복 없이 6개의 숫자를 선택
    #lottery = random.sample(population=numbers, k=6)
    lottery = random.sample(population=range(1,46), k=6)

### 선택된 숫자 출력
    print(lottery)

---------------

# 2. python 내장 모듈 - for문 + random 모듈을 이용한 로또 번호 추출

### 로또 번호 5세트 저장할 빈 리스트 생성
    lotteries = []

### 5번 연속 추출 -> for문 작성
    for number in range(1,6):
      lottery = random.sample(population=numbers, k = 6)
      lotteries.append(lottery)

### 결과 확인
    print("--- 이번주 로또 번호 ---")
    print(lotteries)

-------------

# 클래스(class): 세상에 없던 ‘나만의 자료형(커스텀 자료형)’만들기
    - 우리가 이미 써온 자료형들 : 파이썬이 기본 제공하는 내장 자료형(Built-in Type): int, float, str, bool, list, tuple, dict
    - 클래스 (커스텀 자료형) : 기본 자료형만으로는 표현하기 어려운 현실 세계의 데이터를 표현하기 위해 기존에 없던 새로운 종류의 데이터 타입(Custom Data Type)을 직접 정의하는 것
    클래스와 데이터의 관계를 붕어빵 틀과 붕어빵의 관계라고 생각하면 쉽다.
