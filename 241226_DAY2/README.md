# 📆Day2
# 💡조건문 & 반복문
# if문
* 조건에 따라 코드 블록을 실행할 지 결정하는 제어문으로서 조건식이 True 일 경우에만 특정 코드를 실행.,
* 조건식의 결과는 True 또는 False로 나타나야 하고, 코드 블록은 들여쓰기로 구분되고, 콜론(:)기호로 조건식의 끝을 표시.

  
## 단순 if문
* 조건이 참일 때만 실행되는 단일 블록.
* 형식
```python
    if 조건식 : 
      실행문
```
[예시]
```python
   score = 85
   if score > 80:
       print("테스트에 합격하셨습니다.")
   # 결과 : 테스트에 합격하셨습니다.
```

## if-else문
* 조건이 참일 때와 거짓일 때 각각 다른 코드로 실행
* 형식
```python
    if 조건식 : 
        실행문1
    else:
        실행문2
```
[예시]
```python
    number = 5
    if number % 2 == 0:     # %는 나머지를 구하는 연산자
        print("짝수입니다.")
    else:
        print("홀수입니다.")
    # 결과 : 홀수입니다.
```

## if-elif-else
* 여러 조건 중 하나만 선택하여 실행
* 형식
```python
    if 조건식:
        실행문1
    elif 조건식2:
        실행문2
    else:
        실행문3
```
[예시]
```python
    score = 85
        if score >= 90:
            print("A학점")
        elif score >= 80:
            print("B학점")
        else:
            print("C학점")
        # 걸과 : B 학점
```

## if문 활용 팁
* 조건식 간단화 : 복잡한 조건은 논리 연산자(and, or, not)를 사용.
* 중첩 피하기 : 여러 조건은 elif 로 나누어 가독성 향상.
* 디버깅 편리 : print()문으로 조건 결과 확인.
[예시]
```python
    x, y = 10, 20
        if x > 5 and y < 30:
            print("조건을 만족합니다")
        # 결과 : 조건을 만족합니다.
```


# for문
* 반복 가능한 객체(리스트, 튜플, 문자열 등)의 각 요소를 순회하며 코드를 실행하는 반복문.
* 특정 작업을 반복적으로 수행할 때 사용하고,반복 횟수를 명확히 제어 가능.
### 기본 for문
* 반복 대상의 요소를 하나씩 순회하며 실행.
* 형식
```python
  for 변수 in 반복가능 객체:
            실행문
```
[예시]
```python
  numbers = [1,2,3,4,5]
  for num in numbers:
      print(num * 2)
  # 결과 : 2,4,6,8,10
```
### range()와 함께 사용시
* range()함수로 반복 횟수를 지정.
* range(시작값, 종료값, 증가값)
* 형식
```python
    for 변수 in range():
        실행문
```
[예시]
```python
    for i in range(1,6):
        print(f"{현재 값 : {i}}")
 # 결과 : 현재값 1, 현재값 2 ~ 현재값 5
```
### 중첩 for문
* 반복문 안에 또 다른 반복문 포함.
* 안쪽에 있는 for문이 완전히 실행된 후에 바깥쪽 for문이 실행되면서 반복되는 구조.
* 형식
```python
    for 변수1 in 반복객체1:
        for 변수2 in 반복객체2:
              실행문
```

[예시]
```python
    for i in range(1,4):
        for j in range(1,3):
            print(f"i:{i}, j:{j}")
    # i:1, j:1
    # i:1, j:2
    # i:2, j:1
    # i:2, j:2
    # i:3, j:1
    # i:3, j:2
```

### enumerate() 함께 사용 시
* enumerate() 함수는 시퀀스(리스트, 튜플, 문자열 등)를 순회하면서 각 요소의 인덱스와 값을 튜플 형태로 함께 반환하는 내장 함수입니다.
* 반복문을 돌면서 현재 어떤 인덱스의 값을 처리하고 있는지 알고 싶을 때 용이.


* 형식
```python
    for 인덱스, 값 in enumerate():
        실행문
```

[예시]
```python
    items = ["A", "B", "C"]
    for idx, item in enumerate(items):
        print(f"인덱스{idx} : {item}")
    # 인덱스0 : A
    # 인덱스1 : B
    # 인덱스2 : C
```


# while문
* 조건이 참(True)인 동안 특정 코드를 반복 실행하는 반복문으로 반복 횟수를 사전에 알 수 없을때 주로 사용합니다.
* 조건식의 값이 변하지 않으면 무한 루프가 발생할 수 있음.



### 기본 for문
* 종료 조건을 명시적으로 설정해야 안전.
* 조건식이 False가 되면 반복 종료.


* 형식
```python
    while 조건식 : 
        실행문
```

[예시]
```python
    count = 0
    while count < 5:
        print(f"Count : {count}")
        count += 1
    # Count : 0
    # Count : 1
    # Count : 2
    # Count : 3
    # Count : 4
```


### 무한 루프
* 종료 조건 없이 True를 조건식으로 설정.
* 반드시 break문으로 종료 조건 설정.
* 형식
```python
   while True:
        실행문
```

[예시]
```python
  while True:
      user_input = input("종료하려면 'exit'입력 : ")
      if user_input == "exit":
            break
```
### 조건과 else 사용
* 조건이 False로 바뀌면 else 블록 실행.
* 형식
```python 
   while 조건식:
        실행문
   else:
        실행문
```
[예시]
```python
    x = 5
    while x > 0:
        print(x)
        x -= 1
    else:
        print("반복 종료")
```

### break & continue 사용
* continue : continue 아래의 코드는 실행되지 않고, 반복문의 조건 검사로 다시 돌아감.
* break : break를 만나면 반복문을 벗어나게 되고 반복문 종료.
[예시]
```python
    n = 0
    while n < 10:
          n += 1
          if n % 2 == 0:
              continue   # 짝수는 출력 건너뜀
          print(n)
          if n == 7:
              break    # 7에서 반복 종료.
```





