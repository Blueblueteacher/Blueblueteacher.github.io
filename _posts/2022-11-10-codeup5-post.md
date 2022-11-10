---
layout: post
title: "[CodeUp] 1353, 1354 : 삼각형 출력하기 1, 2"
date: 2022-11-10
excerpt: "#삼각형찍기 #다중반복문(for문)"
comments: true
---

## 1353 : 삼각형 출력하기 1 <br>
0 <br>
00 <br>
000 <br>
0000 <br>
00000 <br>

```C
#include<stdio.h>

int main() 
{
	int n;
	scanf("%d", &n);
	
	for (int i = 0; i < n; i++) { // 줄
		for (int j = 0; j <= i; j++) { // 별
			printf("*");
			if (i == j) // 별의 개수와 줄의 개수가 동일할 때 \n
				printf("\n");
		}
	}
}
```
<br>
<br>

## 1354 : 삼각형 출력하기 2 <br>
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
	
	for (int i = n; i > 0; i--) {  // 줄 
		for (int j = 0; j < i; j++) { // 칸 (이때 반복문의 범위를 0부터 i까찌로 설정해서 별 찍기)
			printf("*");
		}
		printf("\n");
	}
}
```

### 느낀점 <br>
* 별찍기는 이중 반복문의 기초 문제인데 할 때마다 헷갈려서 이번에 확실히 정리하려고 풀었다.
* 별찍기를 쉽게 풀기 위해서는 처음 for문이 줄이라고 생각하고 그 다음 for문이 칸이라고 생각하면 된다.
* 또는, 내가 출력하려는 모양을 좌표라고 생각해서 값을 설정하고 규칙을 찾아내서 for문을 구상해도 된다.
* 두 가지의 방법이 있지만 첫번째 방법이 훨씬 더 쉽게 별찍기 문제를 푸는 방법이라고 생각한다 😄

