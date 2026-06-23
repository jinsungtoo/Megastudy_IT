# 문자열 연결

## 짧은 문자열 생성
string1= 'Good'
string2= 'Morning'

## 연결
string = string1 + " " + string2 # 공백 넣기
print(string)

# 문자열 전용 함수

## split 함수 : 보통은 변수.함수(값) <<< 이지만 (기준값)join(변수)
기본 설정은 빈칸(공백)을 기준으로 문자열을 분리한다

### 쉼표 기준으로 문자열 분리
변수.split(sep=",") <<< sep은 생략 가능

## join 함수
공백 기준으로 join : ' '.join(변수)

# 블리언 자료형
긍정 또는 부정 표시(True or False)

# for 반복문
기본 문법 : for 변수 in (리스트, 문자열 등등):
               print(변수)
