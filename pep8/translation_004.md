# Should a line break before or after a binary operator?
#### 이항 연산자 전에 개행해야하나요? 아니면 이향 연산자 후에 개행해야 하나요?

수십 년 동안 추천되었던 스타일은 이항 연산자 이후에 개행하는 형식입니다. 그러나 이것은 다음과 같은 방식으로 가독성을 해칠 수 있습니다.
<br><br>
* 연산자가 스크린의 이곳 저곳에 흩어져 있는 경우
* 각각의 연산자가 그 전의 라인에 있는 피연산자와 멀리 떨어져 버리는 경우
<br><br>
이런 경우들에 있어서, 우리의 눈은 더하거나 뺄 요소들을 찾기위해 추가적인 일을 해야합니다.

```python
# No: operators sit far away from their operands
# 금지 : 연산자가 자신의 피연산자로부터 멀리 떨어져 있음.
income = (gross_wages +
          taxable_interest +
          (dividends - qualified_dividends) -
          ira_deduction -
          student_loan_interest)
        
```
<br>
이 가독성 문제를 해결하기 위해서 수학자들과 출판사들은 정반대의 관습을 따랐습니다. `Donald Knuth`는 그의 저서 *Computers and 
Typesetting* 시리즈에서 전통적인 방식에 대해 언급했습니다.
>[비록 문단 안의 공식들은 항상 이항 연산자들과 어떤 관계들 뒤에서 나눠지지만, 보여주기 위한 공식들은 항상 이항연한자 전에 나눕니다.](https://www.python.org/dev/peps/pep-0008/#id10)

<br>
아래의 수학으로부터 비롯된 전통은 코드를 더 읽기 쉽게 만들어 줍니다.

```python
# Yes : easy to match operators with operands
# 올바른 방법 : 쉽게 연산자와 피연산자를 연관지을 수 있다.
income = (gross_wages
          + taxable_interest
          + (dividends - qualified_dividends)
          - ira_deduction
          - student_loan_interest)
```

파이썬 코드에서 지역적으로 그 관습이 일관성이 있다면, 두가지 나누는 방식 모두 허용됩니다. 하지만, 만약 새로운 코드를 위해서라면, `Knuth`의 
스타일을 추천합니다.



