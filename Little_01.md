<!-- Heading -->
#  첫번째 미니 도토리

<!-- Quote -->
> ## 백준 풀이
>
>### automata님의 문제집 C++ 배우기 (51 ~ 100)

<br>
안녕하세요 코드 지식이 모자라 다람쥐가 도토리 모으듯이 여기저기서 긁어 모아 사용하다가

숨겨 놓은 도토리 까먹듯이 맨날 자료 못찾아서 뒤적거리는 다람쥐코더 입니다

제가 심어놓은 도토리들이 나무가 되길 바라며 글을 적어봅니다

<br>

벌써 오늘로 5일차라 업로드 해보려고 합니다

아직까진 별찍기 정도지만 남의 코드가 아니라 내가 작성을 해본다는것은 실력 향상에 큰 도움이 되는것 같습니다

<br>

## 별찍기1

문 : 첫째 줄에는 별 1개, 둘째 줄에는 별 2개, N번째 줄에는 별 N개를 찍는 문제

입력 : 첫째 줄에 N(1 ≤ N ≤ 100)이 주어진다.

예제 입력 5

```c++
#define _CRT_SECURE_NO_WARNINGS
#include <iostream>

int main()
{
    // int형 변수 n을 선언합니다
	int n;
	// scanf로 입력받아 d형으로 변수 n을 출력합니다
	scanf("%d", &n);
    
    // int i를 0부터 시작하여 n보다 작은동안 ++를 반복합니다
	for (int i = 0; i < n; i++)
	{
	    // 첫번째 i = 0 두번째 i = 1 .. 2.. 3.. 문제는 5를 입력하므로 4까지 5번 반복됩니다
	    
	    // int j 를 0부터 시작하여 i와 같거나 작은동안 ++를 반복합니다
		for (int j = 0; j <= i; j++)
		{
		    // 첫번째 j 는 0부터 두번째 i = 1.. 2.. 3.. j는 입력한 i 처음값 0.. 1.. 2.. 3.. 4.. 까지 반복합니다
		    
			printf("*");
		}
		printf("\n");
	}
}
```

최종 출력 값
```c++
*
**
***
****
*****
```

대학교때 하던 별찍기를 다시하니 기분이 오묘했습니다 근데 오랫만에 하니 좀 헷깔렸네요ㅋㅋㅋ

## 별찍기2

문 : 첫째 줄에는 별 N개, 둘째 줄에는 별 N-1개, ..., N번째 줄에는 별 1개를 찍는 문제

하지만, 오른쪽을 기준으로 정렬한 별(예제 참고)을 출력하시오.

입력 : 첫째 줄에 N(1 ≤ N ≤ 100)이 주어진다.

입력 예제 : 5

```c++
#define _CRT_SECURE_NO_WARNINGS
#include <iostream>

int main()
{
	int n;

	scanf("%d", &n);

	for (int i = 1; i <= n; i++)
	{
		for (int k = 1; k <= n-i; k++)
		{
			printf(" ");
		}
		for (int j = 1; j <= i; j++)
		{
			printf("*");
		}
		printf("\n");
	}
}
```
최종출력
```c++
    *
   **
  ***
 ****
*****
```
### 다풀고난후

3중 for문이라 헷깔렸지만 결국 해냈습니다~

## 별찍기3

문 : 첫째 줄에는 별 N개, 둘째 줄에는 별 N-1개, ..., N번째 줄에는 별 1개를 찍는 문제

하지만, 오른쪽을 기준으로 정렬한 별(예제 참고)을 출력하시오.

입력 : 첫째 줄에 N(1 ≤ N ≤ 100)이 주어진다.

입력 예제 : 5

```c++
#define _CRT_SECURE_NO_WARNINGS
#include <iostream>

int main()
{
	int n;

	scanf("%d", &n);

	// i를 입력받은 값부터 (5) 1이 될때까지 반복, 하나씩 줄인다
	for (int i = n; i >= 1; i--)
	{
		// k를 i값부터 1이 될때까지 반복, 하나씩 줄인다
		for (int k = i; k >= 1; k--)
		{
			printf("*");
		}
		printf("\n");
	}
}
```
최종출력
```c++
*****
****
***
**
*
```
### 다풀고난후

쪼~금 헷깔렸지만 ~~(3번틀림)~~ 빨리 풀었습니다~

## 별찍기4

문 : 첫째 줄에는 별 N개, 둘째 줄에는 별 N-1개, ..., N번째 줄에는 별 1개를 찍는 문제

하지만, 오른쪽을 기준으로 정렬한 별(예제 참고)을 출력하시오.

입력 : 첫째 줄에 N(1 ≤ N ≤ 100)이 주어진다.

입력 예제 : 5

```c++
#define _CRT_SECURE_NO_WARNINGS
#include <iostream>

int main()
{
	int n;

	scanf("%d", &n);
    
    // i를 0부터 n-1(4) 까지 (5)번 반복
	for (int i = 0; i <= n-1; i++)
	{
	    // k를 0부터 i(0.. 1.. 4) 까지 (0.. 1.. 4..번 반복)
		for (int k = 0; k < i; k++)
		{
			printf(" ");
		}
		// j를 1부터 n-1(5.. 4.. 1..) 까지 (5.. 4.. 1번 반복)
		for (int j = 1; j <= n - i; j++)
		{
			printf("*");
		}
		printf("\n");
	}
}
```
최종출력
```c++
*****
 ****
  ***
   **
    *
```
### 다풀고난후

으 제머리로는 진짜 어려웠습니다 for문을 아직 잘모르나봐요

## 별찍기5

첫째 줄에는 별 1개, 둘째 줄에는 별 3개, ..., N번째 줄에는 별 2×N-1개를 찍는 문제

별은 가운데를 기준으로 대칭이어야 한다.

입력 : 첫째 줄에 N(1 ≤ N ≤ 100)이 주어진다.

입력 예제 : 5

```c++
#define _CRT_SECURE_NO_WARNINGS
#include <iostream>

int main()
{
	int n;

	scanf("%d", &n);
    
    // i를 1부터 입력받은값(5) 까지 총 5번 반복 (5줄 출력)
	for (int i = 1; i <= n; i++)
	{
	    // k를 1부터 n - i (4.. 3.. 0)번 출력 
		for (int k = 1; k <= n - i; k++)
		{
			printf(" ");
		}
		// j를 1부터 2*i - 1 (1.. 3.. 5.. 7)번 출력
		for (int j = 1; j <= (2 * i) - 1; j++)
		{
			printf("*");
		}
		printf("\n");
	}
}
```
최종출력
```c++
    *
   ***
  *****
 *******
*********
```
### 다풀고난후

좀 야매긴한데 지금까지 풀었던거 써먹고 1.. 3.. 7.. 계산하는건 검색찬스를 썼습니다ㅠ

그런데 어느부분에 넣어야 동작을 하는지 그런 개념은 제가 생각한거니 합법입니다!
