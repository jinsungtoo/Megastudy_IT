# 예외(에러)가 발생하는 경우

### 나눗셈 함수 정의
    def div_ten(x):
      return 10/x

### 함수 실행 -> 호출
    result = div_ten(2)
    print(result)

### 정상적으로 작동하는 코드
    print("프로그램 종료")

-----------

# 예외 처리를 하지않는 경우
    for i in range(0,10):
      print(10/i)

-----------
# 예외 처리를 하는 경우
    for i in range(0,10):
      try:
        print(10/i)
      except:
        print("0으로 나눌 수 없습니다.")

-----------

# 포괄적 에러 처리의 문제점

    list_data = [10,20,30]
    
    try:
      output = list_data[10]
      print(output)
    except:
      print("0으로 나눌 수 없습니다")

------

from IPython.core import oinspect
# 현명한 포괄적 에러 처리

### 상황1
    for number in range(0,10):
      try:
        print(10/number)
      except Exception as e:
        print(f'프로그램 실행 중 예측하지 못한 오류가 발생했습니다')
        print(f'오류 유형: {type(e).__name__}')
    
print('-'*80)

### 상황2
    list_data = [10,20,30]
    try:
      ### 리스트 데이터에 대한 인덱싱
      output= list_data[10]
      print(output)
    except Exception as e:
      print(f'프로그램 실행 중 예측하지 못한 오류가 발생했습니다.')
      print(f'오류 유형:{type(e).__name__}')
