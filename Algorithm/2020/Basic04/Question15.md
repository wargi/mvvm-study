# 포인터 익혀보기 #

## 1. 문제

```
포인트를 선언 해보십다.
포인트 변수 t, p, Q, K,
int 변수 G가 있습니다.

t -> p 를 가르키고,
Q -> K 를 가르키고,
p -> G 를 가르키고,
K -> G 를 가르킵니다.
```

- **t, *K의 값을 출력해주세요.

## 2. 입력
- 정수 G의 값을 입력 받아주세요.

## 3. 출력
- **t, *K의 값을 출력해주세요.

## 4. 예제 입력
```
5
```

## 5. 예제 출력
```
5 5
```

## 6. 코드
```c++
#include <iostream>
using namespace std;

int main()
{
    int G;
    int* p = &G, *K = &G;
    int** t = &p, **Q = &K;

    cin >> G;

    cout << **t << " " << *K;
}
```