---
layout: post
title: "[CodeUp] 1410 : 올바른 괄호 1 (괄호 개수 세기)"
date: 2022-11-14
excerpt: "#배열 #strlen #문자열 비교""
comments: true
---

## 1410 : 올바른 괄호 1 (괄호 개수 세기) <br>

```C
#include<stdio.h>
#include<string.h>

int main() 
{
	char st[100001];
	int open = 0, close = 0; // open = '(' /  close : ')'
	scanf("%s", &st); 
	
	for (int i = 0; i < strlen(st); i++) { // strlen(문자열) : 문자열의 길이를 세줌
		if (st[i] == '(') // " "안에 작성하면 오류 ' '로 작성해야함 (" "은 여러 문자열, ' '은 하나의 문자열을 나타냄)
			open++;
		else if (st[i] == ')')
			close++;
	}
	
	printf("%d %d", open, close);

    return 0;
}
```
<br>
<br>


### 느낀점 <br>
* C언어 문제를 풀며 문자열 라이브러리를 처음 사용해보았다. 파이썬의 len함수처럼 strlen함수가 문자열의 길이를 알려주어서 편리한 것 같다.
* 따옴표의 차이가 없을 것으로 생각해서 " "을 사용했었는데 " "을 사용할 때에는 오류가 났다. 그 이유를 찾아보니 " "은 여러 문자열일 때 사용하고 ' '은 하나의 문자열을 표현할 때 사용한다고 한다.
* 이번 문제로 문자열에 대해 학습하게 되어서 좋았다.
