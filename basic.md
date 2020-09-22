
Python Basic from DjangoGirls Tutorial
======================================

## 파이썬 실행 및 종료 (터미널)
```
$ python3
Python 3.8.5 (v3.8.5:580fbb018f, Jul 20 2020, 12:11:27)
>>>

>>> exit()
$
```

## 파이썬 사칙연산
```
>>> 2 + 3
5
```

## 파이썬 문자열
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


## 파이썬 변수
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

## 출력함수 (print)
```
>>> name = "Mini"
>>> name
'Mini'
>>> print(name)  
Mini
```

## List
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


## Dictionary
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


## 비교 (Comparison)
```
>>> 5 > 2
True
>>> 4 == 3
False
>>> 4 != 3
True
>>> 1 == 1
True

>>> 5 > 2 * 2
True
>>> 3 < 1
False
>>> 6 >= 12 / 2
True
>>> 3 <= 2
False

# and , or 연산자의 사용
>>> 6 > 2 and 2 < 3
True
>>> 3 > 2 and 2 < 1
False
>>> 3 > 2 or 2 < 1
True

# 숫자와 문자열을 비교할 때
>>> 1 > 'django'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: '>' not supported between instances of 'int' and 'str'
# TypeError 발생으로 두 타입이 서로 비교대상이 아니라는 것 알랴줌
```


## Boolean (불리언)
+ True (참) , False (거짓)
- 대소문자를 구분한다 !!! (true, tRue 다 틀린표현)
```
>>> a = True
>>> a
True

>>> a = 2 > 5   # 요렇게도 지정 가능
>>> a
False
```


## 파이썬 파일(.py)로 실행하기
예제파일(python_intro.py)을 생성하고 나서 터미널에서 실행
```
$ python3 python_intro.py
Hello, Django girls!
```

## 파이썬 조건문 (if, elif, else)
```
if 3 > 2 :
    print('It works!')
```
**조건에 만족할 경우 반드시 코드에 들여쓰기 적용해야 함**
**탭 한번은 띄어쓰기 4칸과 동일하다**

```
# python_intro.py
if 5 > 2 :
    print('5 is indeed greater than 2')
else :
    print('5 is not greater than 2')

# 실행
$ python3 python_intro.py
5 is indeed greater than 2



# python_intro.py
volume = 57

if volume < 20 :
    print ("It's kinda quiet")
elif 20 <= volume < 40 :     # and 연산자 없이도 가능하군!
    print ("2040")
elif 40 <= volume < 60 :
    print ("4060")
else:
    print ("Too High")

# 실행
$ python3 python_intro.py
4060

```


## 나만의 함수 만들기
**파이썬의 각 함수는 `def`로 시작**
**파이썬은 위에서 아래로 읽어내리는 언어**  
```
def hi():   # 인자값이 없는 hi 함수
    print ("Hi there! ")
    print ('How are you!')

hi()


def hi (name):   # name 인자값이 있는 hi 함수
    if name == "ola" :
        print("Hi ola")
    elif name == "Sonja" :
        print("Hi Sonja")
    else :
        print("Nothing")

hi('Sonja')

```


## 반복문
```
# python_intro.py
def hi(name) :
    print('Hi ' + name + '!')

girls = ['Rachel', 'Monica', 'Phoebe', 'Ola', 'You']

for name in girls :
    hi(name)
    print('Next Girl')


# 실행 결과
$ python3 python_intro.py
Hi Rachel!
Next Girl
Hi Monica!
Next Girl
Hi Phoebe!
Next Girl
Hi Ola!
Next Girl
Hi You!
Next Girl


# range 함수로 범위 지정
for i in range(1,6) :
    print(i)
# 실행 결과
$ python3 python_intro.py
1
2
3
4
5
```
**range(1,6) 함수는 1부터 5까지만 출력한다. 마지막 숫자는 리스트에 포함되지 않음!**

끝
--
