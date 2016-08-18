# import
#### 들여오기(임포트)

* 임포트들은 서로 줄을 나눠서 작성합니다.

```python
Yes:
import os
import sys

No:
import sys, os

```
하지만 다음과 같은 것은 허용됩니다.
<br>
```python
from subprocess import Popen, PIPE

```
<br>
* 임포트는 항상 파일의 가장 위에 작성합니다. 이는 모듈에 대한 주석이나 docstring 후, 그리고 모듈의 전역변수들 전의 위치를 의미합니다.
<br><br>
또한, 임포트는 다음의 순서로 그룹화 되어야 합니다.
<br>
    1. 기본 라이브러리 임포트
    2. 연관된 써드파티 임포트
    3. 로컬 어플리케이션/라이브러리 전용 임포트
<br>   
* 절대적 임포트가 더 가독성이 좋고, 더 작동을 잘 하는 경우가 있기 때문에 명시적 임포트가 권장됩니다. 
    * 임포트 시스템이 비정상적으로 설정되었을 경우, 절대적 임포트가 더 명확한 에러 메세지를 출력합니다.

<br>
```python
import mypkg.sibling
from mypkg import sibling
from mypkg.sibling import example

```
<br>
그러나 절대적 임포트의 대안으로 상대적이지만 명시적으로 임포트를 하는 방식도 적용가능 합니다.
특히, 복잡한 패키지 구조를 다룰때, 절대적 임포트를 사용한다면 불필요하게 장황한 코드를 만들어 낼 수도 있습니다.
<br><br>
```python
from . import sibling
from .sibling import example

```
<br>
기본 라이브러리는 복잡한 패키지 구조를 피해야 하고, 항상 절대적 임포트를 사용해야 합니다.
<br><br>
암묵적이고, 상대적 임포트는 절대 사용하지 말아야하고, `python 3`에서는 불가능하게 되었습니다.
<br><br>

* 클래스를 포함하고 있는 모듈로부터 클래스를 임포트 하는 경우에 다음과 같이 이름을 붙이는 것도 괜찮습니다.
<br>
```python
from myclass import MyClass
from foo.bar.yourclass import YourClass
```
<br>
만약, 이런 방식이 지역 변수의 이름과 충돌한다면 다음과 같은 방법을 택하세요.
<br>
```python
import myclass
import foo.bar.yourclass
```
<br>
그리고 `myclass.MyClass` 와 `foo.bar.yourclass.YourClass`와 같은 방식으로 사용하세요.
<br>

* 와일드 카드 `from <module> import *`를 쓰는 것은 피해야 합니다. 이는 명칭 공간에 존재하는 이름을 불분명하게 만들어서
코드를 읽는 사람이나, 자동화 툴이 혼란에 빠지게 합니다. 다만, 와일드 카드를 사용하는 것이 허용되는 경우가 한가지 있는데,
그것은 바로 공개 API의 일부로써 내부 인터페이스를 재선언 하는 경우입니다.

<br>
예를 들어, 인터페이스의 순수 파이썬 구변부를 추가적인 엑셀레이터 모듈로부터 온 정의로 재정의 하는 경우와 
명확하게 어떤 정의가 재정의 되었는지 미리 알 수 없는 경우가 있습니다.
<br><br>
이름을 재정의 하는 경우에, 다음 장에 나오는 공개 그리고 내부 인터페이스에 관한 가이드라인은 여전히 적용해야 합니다.








