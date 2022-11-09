---
layout: post
title: "[CodeUp] 1675, 1294 : 시저의 암호 1, 2"
date: 2022-11-09
excerpt: "#소수 #반복문(for문) #함수"
comments: true
---

## 1675 : 시저의 암호 1 <br>

```C
#include<stdio.h>

int main() 
{
    char s;
    
    while (scanf("%c", &s) != EOF) {
        if (s >= 97 && s <= 122) {
            if (s - 3 < 97) 
                printf("%c", s + 23);
            else if (s - 3 >= 97)
                printf("%c", s - 3);
        }

        if (s == ' ')
            printf(" ");
    }

    return 0;
}
```
<br>
<br>

## 1294 : 시저의 암호 2 <br>

```C
#include<stdio.h>

int main() 
{
    char s;
    
    while (scanf("%c", &s) != EOF) {
        if (s >= 97 && s <= 122) {
            if (s + 3 >= 123) 
                printf("%c", s - 23);
            else if (s + 3 <= 122)
                printf("%c", s + 3);
        }

        if (s == ' ')
            printf(" ");
    }

    return 0;
}
```

### 느낀점 <br>
* 시저 암호는 알파벳을 3글자씩 밀려서 암호화를 하는 방법이다. (예) d -> a로 표현 / a -> x로 표현
* 그래서 알파벳 소문자 아스키코드에 -3을 한 값이 암호화한 값이다.
* 하지만, a b c 경우는 x y z로 치환해주어야한다. 이는 아스키코드에 23을 더한 값으로 표현할 수 있다.
* 공백의 경우 그냥 출력해주면 된다.
* 시저의 암호 2번 문제의 경우 이를 반대로 생각해서 풀이하면 된다.


