# 안전한 배치 판변 #

## 1. 문제
```
1. 3개의 위치를 2차원 배열(3x4) 입력받습니다.
예)
0 0
0 4
2 1

# _ _ #
_ _ _ _
_ # _ _

2. 이제 안전한지 판별합니다. 판별은 입력받은 좌표의 직선거리(가로/세로)에 다른 좌표가 있다면 "위험"을 출력하고, 없다면 "안전"을 출력합니다.
예) 위의 예제로 받은 좌표는 (0,1), (0,3) 같은 직선거리 선상에 존재하기 때문에 "위험"을 출력합니다.
```

## 2. 입력
- 3개의 위치 좌표를 입력 받습니다.

## 3. 출력
- 입력받은 좌표의 직선거리(가로/세로)에 다른 좌표가 있다면 "위험"을 출력하고, 없다면 "안전"을 출력합니다.

## 4. 예제 입력
```
0 0
1 2
2 1
```

## 5. 예제 출력
```
안전
```

## 6. 코드
```c++
#include<iostream>
using namespace std;

int main() {
	int ay, ax;
	int by, bx;
	int cy, cx;

	cin >> ay >> ax;
	cin >> by >> bx;
	cin >> cy >> cx;

	if (ay == by || ay == cy || by == cy || ax == bx || ax == cx || cx == bx) cout << "위험";
	else cout << "안전";


	return 0;
}
```
