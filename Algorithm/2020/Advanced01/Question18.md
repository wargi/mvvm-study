# 다리 건너갔다 돌아오기

## 1. 문제
```
1. 아래의 1차원 배열(1x11)을 하드코딩 해주세요.
-1 3 1 2 1 3 2 1 2 1 -1

2. 처음 점프 할 n값(index)을 입력받습니다. (1 <= n <= 9)
만약, index n을 1로 입력받으면 1칸을 점프합니다.
만약, n을 3으로 입력받았다면 2칸을 점프합니다.

3. 점프를 해서 다음 인덱스로 가서 그 안에 값만큼 점프를 계속해서 마지막에 도착지점에 도달하면,
다시 시작지점으로 돌아갑니다.

4. 위의 시작부터 도착하여 다시 시작까지의 과정을 출력해주세요.
만약, n을 2를 입력받았다면,
시작 1 2 3 2 도착 2 3 2 1 시작 <- 출력
```

## 2. 입력
- 시작할 위치 n을 입력받으세요. (1 <= n <= 9)

## 3. 출력
- 위의 예제처럼 출력해주세요.

## 4. 예제 입력
```
4
```

## 5. 예제 출력
```
시작 1 3 2 도착 2 3 1 시작
```

## 6. 코드
```c++
#include <iostream>
using namespace std;

int vect[11] = { 0, 3, 1, 2, 1, 3, 2, 1, 2, 1, 0 };

void run(int idx) {
	if (idx >= 10) {
		cout << "도착 ";
		return;
	}

	cout << vect[idx] << " ";
	run(idx + vect[idx]);
	cout << vect[idx] << " ";
}

int main() {
	int n;
	cin >> n;

	cout << "시작 ";
	run(n);
	cout << "시작";

	return 0;
}
```
