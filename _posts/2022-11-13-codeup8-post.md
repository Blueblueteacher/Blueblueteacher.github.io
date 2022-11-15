---
layout: post
title: "[CodeUp] 1405 : 숫자 로테이션"
date: 2022-11-13
excerpt: "#배열 #로테이션"
comments: true
---

## 1405 : 숫자 로테이션 <br>

```C
#include<stdio.h>

int main() 
{
	int n, temp;
	scanf("%d", &n);
	int arr[1000] = {0, }; // 문제에서 1000칸까지 요구했으므로 1000칸 선언
    
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]); // 배열에 값 입력받기
    }

    for (int i = 0; i < n; i++) { 
       for (int j = 0; j < n; j++) { // 배열 값 출력
           printf("%d ", arr[j]);
       } 
       temp = arr[0]; // 배열의 첫번째 요소를 temp에 저장
       for (int j = 0; j < n - 1; j++) {
           arr[j] = arr[j+1]; // 배열의 요소들을 한 칸씩 옮기기
       }
       arr[n-1] = temp; // 배열의 마지막 요소에 temp 값 넣기

       printf("\n");
    }
    return 0;
}
```
<br>
<br>


### 느낀점 <br>
* 배열의 요소들과 temp 변수를 적절하게 사용해야 풀리는 문제였다. 
