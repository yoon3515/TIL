## 22.12.29(목)
> 주요학습 : 클레스에 대하여

## 1. 관련 용어

- class : 멤버와 메서드를 가지는 객체
- class object : 클레스와 같은 의미
- class instance : 클레스를 호출하여 생성된 객체 (=클레스 인스턴스 객체, 객체)
- 멤버 : 클레스/클레스 인스턴스 공간에 정의된 변수 
- 메서드(method) : 클레스 공간에 def로 정의된 함수 
- 속성(Attribute) : 멤버와 메서드 전체를 지칭
- 상속 : 상위클레스의 속성과 행동을 그대로 받아들이고 필요한 기능을 추가해 쓸 수 있음

## 2. 클레스 생성

```bash 
class simple : 
    pass 

print(Simple)
# <class '__main__.Simple'> 출력됨 
```
- `__main__` : 최상위 코드가 실행되는 환경의 이름
- **최상위 코드**란, 프로그램 실행시 첫 번째로 실행되는 모듈을 뜻함. 프로그램 구동에 필요한 다른 모듈들을 import하기 때문에 '최상위'라고 함.  
  
```bash
s1= Simple() # 인스턴스 생성
print(s1)
# <__main__.Simple object at 0x000001D466942670> 출력됨

s2 = Simple()
print(s2)
# <__main__.Simple object at 0x000001D466942EB0> 출력됨
# 같은 클레스더라도 인스턴스마다 id가 다른걸 알 수 있음
``` 
- 인스턴스는 파이썬 종료시 자동으로 소멸됨

## 3. Self
- self : 현재 오브젝트(클레스)를 지칭하는 연산자
- self가 있으면 특정 클레스의 메소드 라는 의미
- 메소드의 매게인자 -> 메소드의 첫 인자는 클레스의 주소를 가진다는 의미 
- self가 없으면 첫 인자를 자동으로 self로 인식하게됨 
```bash
Class U_class :
    def Hap(self, a, b, /) #a, b = 지역변수
    return a + b

r = U_class()
print(r)
#인자가 없으니 self로 인해 U_class의 주소를 16진수로 출력
```
### 1)
```bash
Class U_class2 :
    a = 0  # 멤버변수 (= 전역변수)
    b = 0
    def Hap(self, a, b, /) :
        self.a = a #입력된 지역변수를 전역변수에 대입
        self.b = b
        return self.a + self.b #멤버끼리 합산

r = U_class2()
print(r.Hap(100, 200)) # U_class2의 메서드 사용
```

### 2) 객체를 생성할 때 값을 전달하는 생성자 이용 (`__init__`)
```bash
class U_class3 :
    def __init__(self, su) :
        print(su)

r = U_class3(100)
```
- `__init__` : 초기화를 위한 메소드
    - 인스턴스화를 실시할 때 반드시 처음에 호출되는 특수한 함수 
    - 반드시 첫 인자로 self를 가져야 함
    - 컨스트럭터(constructor) 이라고도 함

```bash
r = 100
print(r)
>>> 100
```
- 기본자료형은 값을 대입해도 알아서 값을 생성(`__init__`)해줌 
- `r = int(100)` 과 동일
- 기본 자료형 외에는 클레스를 객체(인스턴스)로 생성해서 생성자 값 만들어냄 
