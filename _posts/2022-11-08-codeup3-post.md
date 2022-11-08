---
layout: post
title: "[CodeUp] 1284 : 암호 해독"
date: 2022-11-08
excerpt: "#소수 #반복문(for문) #함수"
comments: true
---

```C
#include<stdio.h>

int prime(x) { // 소수인지 판단하는 함수
    int count = 0;
    for (int i = 1; i <= x; i++) {  // 1부터 자기 자신까지 나누어보기
        if (x % i == 0) {  
            count++;
        }
    }

    if (count == 2) // 나누어 떨어지는 수의 개수가 2개이면 소수
        return 1;
    return 0;
}

int main() 
{
    int n; // 어떤 수
    scanf("%d", &n);
    
    for (int i = 1; i <= n / 2; i++) { 
        if (n % i == 0) { 
            if (prime(i) && prime(n / i)) {  // 나누어 떨어지는 수가 소수인지 판단
                printf("%d %d", i, n / i);
                return 0;
            }
        }
    }

    printf("wrong number");

    return 0;
}
```

### 느낀점 <br>
* 소수는 1과 자기 자신만을 약수로 가지는 수이다.
* 문제에서는 어떤 수 n을 두 소수의 곱으로 나타내야하므로 다음과 같은 순서로 표현할 수 있다. <br>
1) 어떤 수(n)을 자기자신까지 나눠서 나누어 떨어지는 수 찾기 => 자기자신까지 나누면 중복된 내용이 나올 수 있으므로, n/2만큼 반복해서 중복을 방지<br> 
2) 나누어떨어지는 수가 소수인지 판단 <br>
3) 소수이면 오름차순으로 정리해서 출력 <br>
* printf() 다음에 return을 하지 않으면 중복된 값이 계속 나온다.


