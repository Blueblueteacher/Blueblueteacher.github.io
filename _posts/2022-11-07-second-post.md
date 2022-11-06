---
layout: post
title: "[CodeUp] 1269 : 수열의 값 구하기"
date: 2022-11-07
excerpt: "#수열 #반복문(for문)"
comments: true
---

```C
#include<stdio.h>

int main() 
{
    int a, b, c, n; // 시작 값 : a, 곱할 값 : b. 더할 값 : c. 항 : n
    int answer; // 값을 저장할 변수
    scanf("%d %d %d %d", &a, &b, &c, &n); 
    answer = a; // 첫번째 항 저장
    for (int i = 0; i < n-1; i++) { // 두번째 항부터 ~ n까지
        answer = answer * b + c;
    }
    printf("%d", answer);

    return 0;
}
```

### 느낀점 <br>
* 수열의 원리와 첫번째 항을 먼저 answer에 저장하고 시작하면 쉽게 접근할 수 있던 문제였다. <br>
* 첫번째 항을 먼저 answer에 저장했으면 반복문의 범위가 하나 줄어 n-1번 반복한다는 점을 인지해야한다. <br>


