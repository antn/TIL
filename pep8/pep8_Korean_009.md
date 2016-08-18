# Other Recommendations
#### 다른 추천 사항들

* 공백이 길게 이어지는 것을 피하세요. 공백은 눈에 보이지 않기 때문에 혼란을 야기할 수 있습니다.
(예를 들어, 스페이스 뒤에 오는 `백슬래시(\)`와 뉴라인 문자는 라인을 잇는 문자로 간주되지 않습니다. 
몇몇 에디터들은 그것들을 보존하지 않고, 많은 프로젝트들(CPython 과 같은)은 그것들을 제거하는 `pre-commit hook`을 가지고 있습니다.

<br>
* 항상 `이항연산자`를 한칸의 공백으로 감싸세요. 
(할당(=), 증강 할당(+=, -= etc), 비교(==, <, >, !=, <>, <=, >=, in, not in, is, is not), 논리(and, or, not))

<br>
* 만약 서로 다른 우선순위를 가진 연산자들이 함께 쓰인다면, 낮은 우선순위를 가진 연산자들을 공백으로 감싸는 것을 고려해 볼만 합니다.
이것은 당신의 판단에 달렸지만, 하나 이상의 공백은 절대 사용해서는 안됩니다. 또한, 이항연산자 양쪽에는 항상 같은 양의 공백을 줘야합니다.

<br>
```python
Yes:
i = i + 1
submitted += 1
x = x*2 - 1
hypot2 = x*x + y*y
c = (a+b) * (a-b)

No:
i=i+1
submitted +=1
x = x * 2 - 1
hypot2 = x * x + y * y
c = (a + b) * (a - b)

```
<br>
* `=` 문자를 키워드 인자를 나타내거나 기본 매개변수를 나타내는 곳에 쓰일 경우 공백을 쓰지 않아야 합니다.

<br>
```python
Yes:
def complex(real, imag=0.0):
    return magic(r=real, i=imag)
    
No:
def complex(real, imag = 0.0):
    return magic(r = real, i = imag)
    
```
<br>
* Function annotation은 반드시 보통의 콜론을 위한 규칙을 적용해야 합니다. 또한, `->` 가 존재하는 경우 공백으로 감싸주어야 합니다.

<br>
```python
Yes:
def munge(input: AnyStr): ...
def munge() -> AnyStr: ...

No:
def munge(input:AnyStr): ...
def munge()->PosInt: ...

```
<br>
* Argument annotation 이 기본값과 같이 제시될 경우, `=` 문자를 공백으로 감싸줍니다. 
(하지만, 오직 인자들이 모두 annotation을 가지고 있거나 기본값일 경우에만 해당됩니다.)

<br>
```python
Yes:
def munge(sep: AnyStr = None): ...
def munge(input: AnyStr, sep: AnyStr = None, limit=1000): ...

No:
def munge(sep: AnyStr=None): ...
def munge(input: AnyStr, limit = 1000): ...

```
<br>
* Compound statements(여러 개의 구문이 하나의 라인에 있는 것) 은 일반적으로 지양됩니다.

<br>
```python
Yes:
if foo == 'blah':
    do_blah_thing()
do_one()
do_two()
do_three()

Rather not(지양해야할 것):
if foo == 'blah': do_blah_thing()
do_one(); do_two(); do_three()

```
<br>
때때로, `if/for/while` 구문이 짧을 경우 같은 라인에 쓰는 것이 허용되기도 하지만, 다중 구문들은 절대 해서는 안됩니다.
또한, 긴 라인이 다음 라인으로 접히는 것도 피하세요.
<br><br>
```python
Rather not(지양해야할 것):
if foo == 'blah': do_blah_thing()
for x in lst: total += x
while t < 10: t = delay()

Definitely not(분명히 안되는 것):
if foo == 'blah': do_blah_thing()
else: do_non_blah_thing()

try: something()
finally: cleanup()

do_one(); do_two(); do_three(long, argument,
                             list, like, this)
                             
if foo == 'blah': one(); two(); three()

```




