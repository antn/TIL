#Code lay-out
#####코드 구성

###Indentation(들여쓰기)



들여쓰기를 할때 4번의 스페이스를 사용하세요.
<br><br>
이어지는 줄은 수직적으로 parentheses(괄호 *()* ), brackets(대괄호 *[]* ), braces(중괄호 *{}* ) 안에 있는 파이썬의 암묵적인 줄이음을 사용하거나
또는 내어쓰기를 사용하여 구성요소들을 감싸도록 배치되어야 한다.<br>

내어쓰기를 사용할 때는 다음을 고려해야 한다.
<br>
첫 줄에는 인자들(arguments)이 존재해서는 안되며, 이어지는 줄이라는 것을 명확하게 구분할 수 있도록 추가적인 들여쓰기가 사용되어야만 한다.
<br>

>좋은 예

```python
# Aligned with opening delimiter.
# 시작하는 구분 문자에 따라 배열하세요.
foo = long_function_name(var_one, var_two,
                        var_three, var_four)

# More indentation included to distinguish this from the rest.
# 추가적인 들여쓰기는 나머지들로부터 구분하고자하는 것을 더 잘 구분하기 위해 포함될 수 있습니다.
def long_function_name(
        var_one, var_two, var_three,
        var_four):
    print(var_one)
    
# Hanging indents should add a level
# 내어쓰기는 한 단계의 수준을 더해준다. (들여쓰기를 한 수준 낮춘다.)
foo = long_function_name(
    var_one, var_two,
    var_three, var_four)
```
<br>
>나쁜 예

```python
# Arguments on first line forbidden when not using vertical alignment.
# 수직적 배열을 사용하지 않을 경우에는 인자들을 첫 번째 줄에 쓰는 것이 금지됩니다.
foo = long_function_name(var_one, var_two,
    var_three, var_four)
    
# Further indentation required as indentation is not distinguishable.
# 들여쓰기가 코드를 구분하는데 적절하지 않게 작성되어 있다면, 추가적인 들여쓰기가 필요합니다.
def long_function_name(
    var_one, var_two, var_three,
    var_four):
    print(var_one)

```
<br>
이어지는 줄들에는 4개의 스페이스 룰은 선택적으로(예외적으로) 적용가능 합니다.

>예외 경우

```python
# Hanging indents *may* be indented to other than 4 spaces.
# 내어쓰기가 4개의 스페이스 룰 대신 적용 가능 할 수도 있습니다.
foo = long_function_name(
  var_one, var_two,
  var_three, var_four)
```
<br>
if 조건문이 길어서, 여러 줄에 걸쳐 작성되어야 할 경우에는 if 뒤에 한칸을 띄고 괄호를 연 다음 이어지는 줄들에는 
4개의 스페이스 들여쓰기를 적용하는 것이 바람직합니다.

이러한 방식은 if 조건절 안에 들여쓰기 되어 있는 코드들과의 시각적 충돌을 일으킬 수도 있습니다.

PEP에서 이에 대한 명확한 위치를 지정하고 있지는 않습니다. 대신, 상황에 따라 적절한 옵션들을 포함하고 있습니다. 하지만, 제약이
가해지는 것은 아닙니다.

```python
# No extra indentation
# 추가적인 들여쓰기가 없을 경우
if (this_is_one_thing and
    that_is_another_thing):
    do_something()
    
# Add a comment, which will provide some distinction in editors supporting syntax highlighting
# 주석을 추가하세요. 그럼으로 해서 구문 강조기능을 에디터에서 코드를 구분하는 역할을 할 수 있습니다.
if (this_is_one_thing and
    that_is_another_thing):
    # Since both conditions are true, we can frobnicate
    # 두 조건이 모두 참이므로, 의미가 없습니다.
    do_something()
    
# Add some extra indentation on the conditional continuation line.
# 조건문의 이어지는 줄들에 추가적인 들여쓰기를 사용하세요.
if (this_is_one_thing
        and that_is antoher_thing):
    do_something()
```
<br>
여러 줄에 이어지는 함수나, 리스트에서 닫는 괄호, 중괄호, 대괄호는 마지막 줄의 첫번째 문자 아래에 닫아주는 방법이 있습니다.

```python
my_list = [
    1, 2, 3,
    4, 5, 6,
    ]
    
result = some_function_that_takes_arguments(
    'a', 'b', 'c',
    'd', 'e', 'f',
    )
```
<br>
또는, 맨 첫 번째 문자에 맞추는 방법도 존재합니다.
```python
my_list = [
    1, 2, 3,
    4, 5, 6,
]

result = some_function_that_takes_arguments(
    'a', 'b', 'c',
    'd', 'e', 'f',
)

```










