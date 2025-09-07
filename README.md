# 웹/파이선 TIL

## 메소드
### 문자열 메소드
#### str.upper() / str.lower() / str.isupper() / str.islower()
#### str.strip("ae") / str.replace("a", "b")
#### str.split()
#### str.index(x) / str.count(x) / str.find(x)

### 포메팅

#### 포멧 연산자 %
```py
name = "OOO"
age 00
s = "My name is %s and I am %d years old. %(name, age)
print(s)
```

#### 포멧함수
```py
name = input()
age = input()
s = "My name is {} and I am {} years old" .format(name, age) #.format의 위치 잘봐라
print(s)
s = "My name is {0} and I am {1} years old" .format(name, age)
s = "My name is {1} and I am {0} years old" .format(name, age)
print(s)
```
#### 문자열 포멧팅
```py
name = "OOO"
age = 00
s = f"My name is {name} and I am {age} years old."
```
#### ***Q.format함수 또는 문자열 포매팅을 사용해 !!!python!!! 문자열을 출력해보자.
```py
py = "python"
a = "{0:!^12}".format(py) #주의해라 0~12까지 범위를 확실히 정하자.
print(a)
```
다른 정답
```py
print(f'{"python":!^12}')
```
## 리스트 자료형
```py
odd =[1,2,3,4,5]
del odd[0]
```
#### ***Q.a=[1,2,3,4,5] 리스트에서 슬라이싱 기법을 사용하여 리스트 [2,3]을 만들어보자.
```py
a =[1,2,3,4,5]
b=a[1:3]
b=a[-4:-2]
print(b)
```
리스트 더하기 곱하기는 문자열 더하기 곱하기랑 비슷
#### 리스트 길이 구하기
```py
a = [1,2,3]
print(len(a))
>>> 3
```
## 리스트 관련함수

#### ___.append(x)
___ 리스트에 x값을 더하겠다.
#### list.sort() / list.reverse()
#### list.index(x) / list.insert(a,b)
list.index(x)는 리스트 안에 x라는 값을 가진 것의 위칫값을 묻는다. / list.insert(a,b)는 리스트 a번째 위치에 b를 삽입한다.
#### list.remove(x) / list.pop(x)
list.remove(x)는 첫번째로 나오는 x라는 값을 삭제 / list.pop(x)는 x라는 요소를 끄집어낸다.
#### list.count(x) / list.extend([4,5])

## 튜플 자료형
튜플은 리스트처럼 요솟값을 바꿀 수 없다.
```py
t1 = ()
t2 = (1,)
t3 = (1,2,3)
t4 = 1,2,3
t5 = (('a','b'),('ab','cd')) #문자니까 '' 해야함
```
t2처럼 단지 1개의 요소만을 가질 때에는 요소 뒤에 쉽표를 반드시 붙여야 한다.
t4처럼 소괄호를 생략해도 된다.
#### del 함수로 지우고 싶어도 못지우고, t1[0] = c처럼 특정 인덱스를 집어서 바꾸는 것도 불가
#### 인덱싱하기
t1 = (1,2,'a','b')
#### print(t1[0])처럼 인덱싱하는 건 가능
#### 슬라이싱하기
```py
t1 = (1,2,'a','b')
print((t1[0:]))
```
#### 튜플 더하기
```py
t1 = (1,2,'a','b')
t2 = (3,4)
t3 = t1 +t2
print(t3)
```
바꿀수는 없지만 새로운 튜플을 만들어서 더할 수는 있다. 튜플 곱하기도 마찬가지, (3,4,3,3,4,3,4) 이렇게 됨.
#### 튜플 길이 구하기 len(t1)
## 딕셔너리 자료형
키와 벨류로 구성 한쌍이 세트. 키는 변하지 않는 값이 와야하므로, 리스트는 올 수 없지만 튜플을 올 수 있다.

#### 딕셔너리 쌍 추가, 삭제
```py
a = {1: 'b'}
a[2] = 'c'
a['name']='dog'
```
#### 딕셔너리 요소 삭제하는 법은 리스트 요소를 삭제하는 방법과 유사하다
```py
del a[2]
```
이러면 2의 위치에 있는 한쌍의 키와 벨류{key:value}가 모두 삭제된다.

### 딕서너리 활용법
#### 딕셔너리에서 key를 사용해 value 얻기 // value가 나온다
```py
grade = {'pey':10, 'julliet': 99}
grade['pey']
>>10
grade['julliet']
>>99
```
```py
a = {1:'pey', 99:'julliet'}
a[1]
>>'pey
```
여기에서 a[1]이 의미하는 것은 리스트나 튜플의 a1이랑은 전혀 다르다. 딕셔너리와 리스트, 튜플의 차이점. 또한, 딕셔너리는 리스트나 튜플에 있는 인덱싱 방법을 적용할 수 없다. 따라서 a[1]은 key가 1인것의 value인 'pey'를 리턴한다. 정리하면, 딕셔너리 변수 무엇은 Key로 Key에 해당하는 Value를 얻는다.

#### 딕셔너리 만들 때 주의사항
딕셔너리에서 Key는 고유한 값이므로 중복되는 Key 값을 설정해 놓으면 하나를 제외한 나머지 것들이 모두 무시된다는 점에 주의해야한다.
```py
a = {1:'a',1:'b'} # 중복된 key에 대한 value 값의 한쌍이 하나 이외 모두 일제히 무시. 
print(a)
>> {1:'b'}
```
## 딕셔너리 관련 함수

### Key리스트 만들기 - keys
```py
a = {'name':'pey', 'phone' :'010-9999-1234','birth':'1118'}
print(a.keys())
>> dict_keys(['name', 'phone', 'birth'])
```
#### dict_keys 객체는 다음과 같이 사용할 수 있다. 리스트를 사용하는 것과 별 차이는 없지만, 리스트 고유의 append, insert, pop,remove, sort 함수는 수행할 수 없다.
```py
for k in a.keys():
    print(k)
>> name
>> phone
>> birth
```

### Value 리스트 만들기
```py
a.values()
```
### Key Value 쌍 얻기
```py
print(a.items())
>> dict_items([('name', 'pey'), ('phone', '010-9999-1234'), ('birth', '1118')])
```
items 함수는 key와 value의 쌍을 튜플로 묶은 값을 dict_items 객체로 리턴한다.

### Key: Value 쌍 모두 지우기
```py
a.clear()
```

### Key로 Value 값 얻기 - get
```py
a.get('name')
>> 'pey'
```
get('name')은 a['name']을 사용했을 때와 동일한 값을 리턴한다. 단 차이점은 'nokey'에서 오류와 'none'

## if
```py
money = 2000
card = True
if money > 3000 or card:
    print("택시를 타고 가라")
```
