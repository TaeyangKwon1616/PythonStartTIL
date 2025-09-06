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
