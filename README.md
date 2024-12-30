# 👏Python👏
# 📆Day1
### 파이썬 기본문법 요약(1)
|항목|요소|정의|설명|예시|
|:---:|:---:|:---:|:---:|:---:|
|변수||데이터를 저장하는 메모리 공간|숫자, 문자|x = 5<br/>x = "사과"|
|자료형|정수형<br/>(int)|소수점이 없는 숫자|산술 연산 가능|x = 5|
|자료형|실수형<br/>(float)|소수점이 있는 숫자|근사값 처리|x = 3.14|
|자료형|문자열<br/>(str)|문자들의 집합|큰 따옴표 또는 작은 따옴표|s = "사과" 또는 s = '사과'|
|자료형|볼린<br/>(bool)|참/거짓 값|True/False 만 가능|b = True|
|자료형|리스트<br/>(list)|순서가 있는 집합|수정 가능, 중복 허용|lst = [1,2,3]|
|자료형|튜플<br/>(tuple)|순서가 있는 집합|수정 불가, 중복 허용|tup = (1,2,3)|
|자료형|딕서너리<br/>(dict)|키-값 쌍의 집합|키는 중복 불가|d = {"a" : 1}
### 기본문법 요약(2)
<table>
    <tr>
        <th>항목</th>
        <th>요소</th>
        <th>정의</th>
        <th>설명</th>
        <th>예시</th>
    </tr>
    <tr>
        <td rowspan="3">조건문</td>
        <td>if</td>
        <td>조건에 따른 실행</td>
        <td>조건이 참일 때 실행</td>
        <td>if x > 0</td>
    </tr>
    <tr>
        <td>elif</td>
        <td>다중 조건 실행</td>
        <td>이전 조건이 거짓일 때 확인</td>
        <td>elif x == 0</td>
    </tr>
    <tr>
        <td>else</td>
        <td>기본 실행</td>
        <td>모든 조건이 거짓일 때 실행</td>
        <td>else:</td>
    </tr>
    <tr>
        <td rowspan="3">반복문</td>
        <td>for</td>
        <td>정해진 횟수 반복</td>
        <td>시퀀스 객체 순회</td>
        <td>for i in range(3):</td>
    </tr>
    <tr>
        <td>while</td>
        <td>조건부 반복</td>
        <td>조건이 참인 동안 반복</td>
        <td>while x > 0:</td>
    </tr>
    <tr>
        <td>제어문</td>
        <td>반복 제어</td>
        <td>break, continue 사용</td>
        <td>break</td>
    </tr>
    <tr>
        <td rowspan="3">함수</td>
        <td>기본함수</td>
        <td>코드의 재사용 단위</td>
        <td>def로 정의, 반환값 설정</td>
        <td>def add(a,b)</td>
    </tr>
    <tr>
        <td>람다함수</td>
        <td>익명 함수</td>
        <td>단일 표현식 함수</td>
        <td>lambda x : x * 2</td>
    </tr>
    <tr>
        <td>내장함수</td>
        <td>파이썬 기본 제공</td>
        <td>print(), len() 등</td>
        <td>print("Hello")</td>
    </tr>
    <tr>
        <td rowspan="2">메소드</td>
        <td>리스트 메소드</td>
        <td>리스트 조작 함수</td>
        <td>append, remove, sort 등</td>
        <td>lst.append(4)</td>
    </tr>
    <tr>
        <td>문자열 메소드</td>
        <td>문자열 처리 함수</td>
        <td>upper, lower, split 등</td>
        <td>s.upper()</td>
    </tr>
    <tr>
        <td rowspan="3">예외처리</td>
        <td>try</td>
        <td>예외 발생 가능 코드</td>
        <td>오류 검사 블록</td>
        <td>try:</td>
    </tr>
    <tr>
        <td>except</td>
        <td>예외 처리 코드</td>
        <td>오류 방생시 실행</td>
        <td>except:</td>
    </tr>
    <tr>
        <td>finally</td>
        <td>항상 실행 코드</td>
        <td>예외 발생 여부와 무관</td>
        <td>finally:</td>
    </tr>
</table>

# 리스트(List)
* 여러 개의 값을 하나의 변수에 담을 수 있는 순서가 있는 데이터 자료형으로 대괄호[] 안에 콤마(,)로 구분하여 정의.
* 수정 가능하고 중복이 허용되며, 다양한 데이터 유형을 한 리스트에 담을 수 있음.

### 리스트 생성과 초기화

[빈 리스트 생성]
```python
    empty_list = []
```
[초기값 설정]
```python
    numbers = [1,2,3,4,5]
    fruits = ["apple", "banana", "cherry"]
```

### 리스트 생성과 초기화

[인덱스로 접근]
```python
    fruits = ["apple", "banana", "cherry"]
    print(fruits[0])  # apple
```

[슬라이싱]
```python
    fruits = ["apple", "banana", "cherry"]
    print(fruits[0:2])   # ['apple', 'banana']
```

### 리스트 활용예제
```python
    numbers = [3,1,4,1,5]
```


1. 요소 추가(append)
```python
    numbers.append(9)
    print(numbers)     # [3,1,4,1,5,9]
```


2. 요소 정렬(sort)
```python
    umbers.sort()
    print(numbers)  #[1,1,3,4,5,9]
```


3. 요소 제거(remove)
```python
    numbers.remove(1)  # 첫 번째로 발결되는 1을 제거.
    print(numbers)   # [1, 3, 4, 5, 9]
```


4. 특정 위치의 요소 추출 및 삭제(pop)
```python
    removed_item = numbers.pop(2)  # 인덱스 2의 요소를 추출하고 삭제.
    print(numbers)     # [1, 3, 5, 9]
    print(removed_item)  # 4
```


5. 리스트 뒤집기(reverse)
```python
    numbers.reverse()
    print(numbers)    # [9, 5, 3, 1]
```


6. 리스트속 특정 요소의 개수 세기(count)
```python
    count = numbers.count(5)
    print(count)  # 1
```


7.  리스트 복사(copy)
```python
    new_numbers = numbers.copy()
    print(new_numbers)   # [9, 5, 3, 1]
```


8. 리스트 확장(extend)
```python
    numbers.extend([6,7,8])
    print(numbers)   # [9, 5, 3, 1, 6, 7, 8]
```


9. 리스트 합치기(concatenate)
```python
    another_list = [10, 11, 12]
    combined_list = numbers + another_list
    print(combined_list)  # [9, 5, 3, 1, 6, 7, 8, 10, 11, 12]
```


# 튜플(tuple)
* 여러 개의 값을 하나의 변수에 담을 수 있는 순서가 있는 데이터 자료형.
* 리스트와는 달리 수정할 수 없고 중복은 허용되며, 튜플은 소괄호() 안에 값을 콤마(,)로 구분하여 정의함.


### 리스트 생성과 초기화

[빈 튜플 생성]
```python
  empty_tuple = ()
```
[한 개의 요소를 가진 튜플 : 단일 요소일 때는 콤마가 필요]
```python
  single_element = (5,)
```

### 튜플 요소 접근 및 슬라이싱

[인덱스로 접근]
```python
  colors = ("red", "green", "blue")
  print(colors[1])   # green
```

[슬라이싱]
```python
  colors = ("red", "green", "blue")
  print(colors[0:2])  # ("red", "green")
```

### 튜플 활용예제
```python
  특정 값의 개수 세기(count)
  numbers = (1,2,3,2,4)
  print(numbers.count(2))    # 2 (2가 두 번 등장)
```

* 특정 값의 인덱스 찾기(index)
```python
  print(numbers.index(3))    # 2 (3의 인덱스)
```

[예제]
```python
  point = (3,4)
  print("x좌표 : ", point[0])
  print("y좌표 : ", point[1]) # 결과 : x좌표 : 3,  y좌표 : 4
```

# 딕셔너리
* 키(key)-값(value)쌍으로 데이터를 저장하는 매핑 타입의 자료형.
* 요소 추가, 수정, 삭제가 가능하며, 표기는 중괄호{}안에 key : value 형태로 값을 저장함.

  
### 리스트 생성과 초기화

[빈 딕셔너리 생성]
```python
  empty_tuple = {}
```
[초기값 설정]
```python
  person = {"name" : "Bob", "age" : 30, "city" : "New York"}
```

### 딕셔너리 요소 접근 및 슬라이싱

[키를 통해 값 접근]
```python
person = {"name" : "Bob", "age" : 30, "city" : "New York"}
print(person["name"])  # Bob
```

[값 수정]
```python
  person["age"] = 31
  print(person["age"])  # 31
```

### 딕셔너리 활용예제

1. 키에 대응하는 값 반환 (get)
```python
  info = {"name" : "Charlie", "age" : 22}
  print(info.get("name"))   # Charlie
```
2. 모든 키를 반환 (keys)
```python
  print(info.keys())    #dict_keys(['name', 'age'])
```

3. 모든 값을 반환 (values)
```python
  print(info.values()) # dict_values(['Charlie', 22])
```

4. 키-값 쌍을 튜플 형태로 반환(items)
```python
  print(info.items())  # dict_items([('name', 'Charlie'), ('age', 22)])
```

# 📆Day2
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
       print(\"테스트에 합격하셨습니다.\")
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






