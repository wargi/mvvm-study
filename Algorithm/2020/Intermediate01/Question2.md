# 범위 사이의 숫자 바꾸기

## 1. 문제
```
아래의 2차원 배열(4x3)을 하드코딩 해주세요.
1 5 3
4 5 5
3 3 5
4 6 2
```

- 숫자 두 개를 입력 받고, 두 숫자 사이에 있는 숫자를 모두 '#'으로 바꿔 출력해주세요.

## 2. 입력
- 숫자 두 개를 입력 받습니다.

## 3. 출력
- 입력 받은 두 숫자 사이에 있는 숫자를 모두 '#'으로 바꿔 출력해주세요.

## 4. 예제 입력
```
1 4
```

## 5. 예제 출력
```
# 5 #
# 5 5
# # 5
# 6 #
```

## 6. 코드
```c++
#include <iostream>
using namespace std;

int main()
{
    int map[4][3] = {
        1, 5, 3,
        4, 5, 5,
        3, 3, 5,
        4, 6, 2
    };

    int n, m;
    cin >> n >> m;

    int mask[4][3] = { 0 };

    for (int i = 0; i < 4; i++) {
        for (int j = 0; j < 3; j++) {
            if (map[i][j] >= n && map[i][j] <= m) mask[i][j] = 1;
        }
    }

    for (int i = 0; i < 4; i++) {
        for (int j = 0; j < 3; j++) {
            if (mask[i][j] == 1) cout << "# ";
            else cout << map[i][j] << " ";
        }
        cout << "\n";
    }
}
```
