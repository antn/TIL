# Module level dunder names
#### Module level dunder 의 이름

> Module level dunder: 앞 뒤로 두개씩의 언더바로 감싸져 있는 이름

`__all__`, `__author__`, `__version__` 과 같은 Module level dunder는 반드시 모듈의 docstring 후에 위치해야 합니다.

동시에 `from __future__ imports` 를 제외한 모든 임포트 구분 전에 위치해야 합니다.
<br><br>
파이썬은 `__future__` 모듈을 docstring을 제외한 모든 코드들보다 전에 위치하도록 규정하고 있습니다.
<br><br>
```python
"""This is the example module.


This module does stuff.
"""


from __future__ import barry_as_FLUFL

__all__ = ['a', 'b', 'c']
__version__ = '0.1'
__author__ = 'Cardinal Biggles'

import os
import sys

```
<br><br>
___
# String Quotes
#### 스트링 따옴표

파이썬에서는 작은 따옴표로 감싸진 스트링과 큰 따옴표로 감싸진 스트링을 같게 취급합니다. 
이 PEP에서도 이것에 관련된 추천사항은 없습니다. 룰을 선택해서 준수하기만 하면 됩니다.
<br><br>
그러나 스트링 값이 작은 따옴표 또는 큰 따옴표 문자 자체를 포함하는 경우에는 `백슬래시(\)`를 사용하는 것을
피하기 위해 작은 따옴표를 썼다면 큰 따옴표를 그 반대 경우에도 동일하게 사용하는 것이 바람직 합니다.
이를 통해 가독성을 향상시킬 수 있습니다.
<br><br>
```python
a = 'he"eeee"llo'
b = "he'eeee'llo"
```
<br><br>
세 개의 따옴표로 감싸진 스트링을 나타낼 때는 [docstring 규칙](https://www.python.org/dev/peps/pep-0257/)과의 일관성을 유지하기 위해, 항상 큰 따옴표를 사용해야 합니다.
<br><br>




