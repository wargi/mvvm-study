# 배열 변경하기 #

## 1. 문제
```
1. 아래에 2차원 배열(3x4)을 하드코딩 해주세요.
3 5 4 1
1 1 2 3
6 7 1 2

2. 각기 다른 숫자를 총 4개를 입력 받고, 배열에 입력받은 숫자가 있다면 아래 처럼 바꿔주세요.

예를 들어 1, 2, 3, 4를 입력받았다면,
배열의 값이 1인 곳은 2로, 2인 곳은 3으로,
3인 곳은 4로, 4인 곳은 1로 바꿔주세요.

3. 위의 조건대로 변경하고 최종결과를 출력해주세요.

1, 2, 3, 4를 입력받았다면,
최종결과)
4 5 5 2
2 2 3 4
6 7 2 3
```

## 2. 입력
- 각기 다른 숫자를 총 4개를 입력 받아주세요.

## 3. 출력
- 위의 조건대로 변경하고 최종결과를 출력해주세요.

## 4. 예제 입력
```
1 2 3 4
```

## 5. 예제 출력
```
4 5 5 2
2 2 3 4
6 7 2 3
```

## 6. 예제 입력

```
1 3 5 6
```

## 7. 예제 출력

```
7 5 4 3
3 3 2 7
1 6 3 2
```

## 8. 코드

```c++
#include<iostream>
using namespace std;

int map[3][4] = {
	3, 5, 4, 1,
	1, 1, 2, 3,
	6, 7, 1, 2
};
int direct[4];
int vect[10];
int main() {
	for (int i = 0; i < 4; i++) {
		cin >> direct[i];
	}

	int x = direct[0];
	for (int i = 0; i < 3; i++) {
		vect[direct[i]] = direct[i + 1];
	}
	vect[direct[3]] = x;

	for (int i = 0; i < 3; i++) {
		for (int j = 0; j < 4; j++) {
			if (vect[map[i][j]] != 0) {
				map[i][j] = vect[map[i][j]];
			}
		}
	}

	for (int i = 0; i < 3; i++) {
		for (int j = 0; j < 4; j++) {
			cout << map[i][j] << " ";
		}
		cout << "\n";
	}

	return 0;
}
```