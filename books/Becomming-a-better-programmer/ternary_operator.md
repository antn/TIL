# 장황한 내용

코드를 풀어쓴다고 생각하고 쓰다보면, 장황하고 의도를 파악하기 어렵게 되는 경우가 많다.

이런 경우, 삼항 연산자를 사용하는 것이 가능한 경우, 쓰는 것이 바람직하다.


```Java
public String getPath(URL url){
    if(url==null){
        return null;
    }
    else{
        return url.getPath();
    }
}
```
<br>
위와 같은 식은 다음과 같이 삼항연산자로 간단히 나타낼 수 있다.
<br><br>

```Java
public String getPath(URL url){
    return url == null ? null : url.getPath();
}
```

