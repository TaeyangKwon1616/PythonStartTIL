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
