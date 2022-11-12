---
layout: post
title: "[CodeUp] 1355, 1357 : 삼각형 출력하기 3, 4"
date: 2022-11-11
excerpt: "#삼각형찍기 #다중반복문(for문)"
comments: true
---

## 1355 : 삼각형 출력하기 3 <br>
00000 <br>
 0000 <br>
  000 <br>
   00 <br>
    0 <br>

```C
#include<stdio.h>

int main() 
{
	int n;
	scanf("%d", &n);
	
	for (int i = 0; i < n; i++) { // 줄
		for (int j = 0; j < i; j++) // 공백을 먼저 찍고 있으므로 공백 for문이 먼저온다.
			printf(" ");

        for (int j = i; j < n; j++) // 별에 관한 for문 (이때 공백 개수는 0번째 줄일 때 0개 / 1번째 줄일 때 1개 이런식이므로 j의 값을 i(줄)로 설정)
            printf("*");
            
        printf("\n");
	}
}
```
<br>
<br>

## 1357 : 삼각형 출력하기 4 <br>
0 <br>
00 <br>
000 <br>
0000 <br>
000 <br>
00 <br>
0 <br>

```C
#include<stdio.h>

int main() 
{
	int n;
	scanf("%d", &n);
	
	for (int i = 0; i < n; i++) {
		for (int j = 0; j < i; j++) {
			printf("*");
			if (i-1 == j)
				printf("\n");
		}
	}
	
	for (int i = n; i > 0; i--) {  // 줄 
		for (int j = 0; j < i; j++) { // 칸 (이때 반복문의 범위를 0부터 i까지로 설정해서 별 찍기)
			printf("*");
		}
		printf("\n");
	}
}
```

### 느낀점 <br>
* 저번에 이어 별찍기 문제를 풀어보았다. 이번 문제는 저번에 풀었던 문제를 응용해서 풀면 되는 것이어서 복습하는 느낌이 들었다.
* 별찍기 문제는 별과 공백과의 관계 파악이 먼저라고 생각했던 문제들이었다. 

