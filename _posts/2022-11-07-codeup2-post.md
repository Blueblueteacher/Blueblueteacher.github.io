---
layout: post
title: "[CodeUp] 1273 : 약수 구하기"
date: 2022-11-07
excerpt: "#약수 #반복문(for문)"
comments: true
---

```C
#include<stdio.h>

int main() 
{
    int n; // 입력받은 수
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) { // 1부터 n까지 나눠보기
        if (n % i == 0)
            printf("%d ", i);
    }

    return 0;
}
```

### 느낀점 <br>
* 약수는 어떤 수를 나누어떨어지게 하는 수를 말한다.
* 따라서, for문을 사용해서 1부터 n(입력받은 수)까지 다 나누고 나머지가 0일 때의 값을 출력해주면 된다.


