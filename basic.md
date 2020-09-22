
Python Basic from DjangoGirls Tutorial
======================================

#### 파이썬 실행하기 (터미널)
```
$ python3
Python 3.8.5 (v3.8.5:580fbb018f, Jul 20 2020, 12:11:27)
>>>
```

#### 파이썬 사칙연산
```
>>> 2 + 3
5
```

#### 파이썬 문자열
```
>>> "Hi there"
'Hi there'

>>> "Hi there " + "0la"
'Hi there 0la'

>>> "0la" * 2
'0la0la'

>>> 'Runnin\' down the hill'
'Runnin' down the hill'

>>> "01a".upper()
'0LA'

>>> len("01a")
3

>>> len(304023)   # 문자열이 아닌 int 형으로 오류발생
TypeError ~~~~~

>>> len(str(304023))
6
```

+ str() 함수 : 대상을 문자열로 변환
+ int() 함수 : 대상을 정수로 변환 / 텍스트에서 숫자로 변환은 불가


#### 파이썬 변수
```
>>> name = "0la"
>>> name
'ola'

>>> name = "Sonja"
>>> name
'Sonja'

>>> len(name)
5

>>> a = 4
>>> b = 6
>>> a * b
24

>>> city = "Tokyo"
>>> ctiy
~~ NameError: name 'ctiy' is not defined
# NameError 오류가 보일 경우 오타가 있는지 살펴보기
```

#### 출력함수 (print)
```
>>> name = "Mini"
>>> name
'Mini'
>>> print(name)  
Mini
```

#### List
```
>>> []
[]

>>> lottery = [3, 42, 12, 19, 30, 59]
>>> len(lottery)   # List 안의 객체의 수를 알려줌
6

>>> lottery.sort()
>>> print(lottery)
[3, 12, 19, 30, 42, 59]  # 오름차순 정렬

>>> lottery.reverse()
>>> print(lottery)
[59, 42, 30, 19, 12, 3]  # 내림차순 정렬

>>> lottery.append(199)
>>> print(lottery)
[59, 42, 30, 19, 12, 3, 199]   # List에 새로운 값 추가

>>> print(lottery[1])
42
>>> print(lottery[0])
59    # index 를 통한 값 조회
>>> lottery.pop(0)   # List 내의 아이템을 삭제할 때  
59
>>> print(lottery)
[42, 30, 19, 12, 3, 199]
>>> lottery.pop()   # index 를 지정해주지않으면 제일 뒤 부터 제거
```


#### Dictionary
**Dictionary는 List와 유사하지만, 인덱스가 아닌 키로 값을 찾음**
```
>>> {}   # 비어있는 Dictionary 생성
{}
```

```
>>> participant = {'name': 'ola', 'country': 'Poland', 'favorite_numbers': [7,42,92]}
```
+ 이 변수 안에는 3개의 Key-Vaule 쌍이 들어있음

```
>>> print(participant['name'])
ola
>>> participant['house']
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 'house'     # 존재하지 않는 key 로 조회하면 KeyError 발생
```

- 리스트(List) : 아이템 정렬이 필요할 때 사용
- 딕셔너리(Dictionary) : Key-Vaule 서로 연관되어 있거나, Key 를 이용하여 어떤 값을 찾을 때

```
>>> participant['favorite_language'] = 'Python'   # Key-Vaule 쌍 추가 가능
>>> participant
{'name': 'ola', 'country': 'Poland', 'favorite_numbers': [7, 42, 92], 'favorite_language': 'Python'}

>>> len(participant)
4

>>> participant
{'name': 'ola', 'country': 'Poland', 'favorite_numbers': [7, 42, 92], 'favorite_language': 'Python'}
>>> participant.pop('favorite_numbers')   # 값 제거
[7, 42, 92]
>>> participant
{'name': 'ola', 'country': 'Poland', 'favorite_language': 'Python'}

>>> participant['country'] = 'NewZealand'   # 기존 값을 변경 (Poland > NewZealand)
>>> participant
{'name': 'ola', 'country': 'NewZealand', 'favorite_language': 'Python'}

```
