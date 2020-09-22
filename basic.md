
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
ctiy
~~ NameError: name 'ctiy' is not defined
```
`NameError` 오류가 보일 경우 오타가 있는지 살펴보기
