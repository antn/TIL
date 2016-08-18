# Whitespace in Expressions and Statements
#### 표현들과 구문들에 있어서의 공백

### Pet Peeves
#### 불쾌한 것들, 질색인 것들, 정말 싫어하는 것들

아래와 같은 경우에 관련없는 공백은 피하세요.

* 소괄호, 중괄호, 대괄호를 열고 닫을 때, 곧바로 있는 공백들

```python
Yes: 
spam(ham[1], {eggs: 2})

No:
spam( ham[ 1 ], { eggs: 2 } )

```
<br>
* 콤마, 세미콜론, 콜론 바로 전에 있는 공백들

```python
Yes:
if x == 4: print x, y; x, y = y, x

No:
if x == 4 : print x , y ; x , y = y , x 

```
<br>
* 하지만, 슬라이스에서의 콜론은 마치 이항 연산자처럼 작동합니다. 이 경우에는 콜론 양쪽을 같은 만큼 공백을 넣어줍니다.
(이 콜론은 마치 가장 낮은 우선순위를 가진 연산자처럼 간주합니다.)
확장된 형태의 슬라이스에서는, 두 콜론 모두 같은 만큼의 공백을 가져야만 합니다.
> 예외: 만약 슬라이스의 인자가 생략된다면, 공백 또한 생략됩니다.

<br>
```python
Yes:
ham[1:9], ham[1:9:3], ham[:9:3], ham[1::3], ham[1:9:]
ham[lower:upper], ham[lower:upper:], ham[lower::step]
ham[lower+offset : upper+offset]
ham[: upper_fn(x) : step_fn(x)], ham[:: step_fn(x)]
ham[lower + offset : upper + offset]

No:
ham[lower + offset:upper + offset]
ham[1: 9], ham[1 :9], ham[1:9 :3]
ham[lower : : upper]
ham[ : upper]

```
<br>
* 함수의 호출을 위해 인자 리스트들을 대입하기 위한 괄호 바로 전에 공백이 있는 경우

<br>
```python
Yes: spam(1)
No: spam (1)

```
<br>
* 슬라이스나 인덱싱이 시작하는 부분의 괄호 바로 전에 공백이 있을 경우

<br>
```python
Yes: dct['key'] = lst[index]
No: dct ['key'] = lst [index]

```
<br>
* 연산자 앞뒤로 하나 이상의 공백이 존재할 경우

<br>
```python
Yes:
x = 1
y = 2
long_variable = 3

No:
x             = 1
y             = 2
long_variable = 3

```
















