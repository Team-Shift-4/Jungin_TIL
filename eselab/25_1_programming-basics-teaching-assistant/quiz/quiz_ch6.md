# Quiz\_ch6

빈칸을 알맞게 채우시오.

* 원하는 특정 비트를 반대로 하려면 해당 비트만을 (         )로 하는 마스크를 이용하여 (          )연산을 수행한다.
* 어떤 값에서 특정 비트의 값을 1로 변경하려면 해당 비트만을 (          )로 하는 마스크를 이용하여 (          )연산을 수행한다.

***

다음 프로그램을 실행한 후 변수 result의 결과값을 적으시오.

```c
int x = 4, y = 16;
double result;
result = (double)x / y;
```

```c
int x = 3.5, result;
double y = 5.9;
result x + y;
```

***

논리 오류를 포함한 다음 프로그램을 실행한 후 출력되는 count의 값은 얼마인가?

```c
int num = 2, count = 0;
switch(num) {
    case 3:
        count = 6;
        break;
    case 2:
        count = 7;
    case 6:
        count = 8;
        break;
    case 9:
        count = 5;
}
printf("%d", count);
```

***

int 형 변수 x의 초기값이 75일 때, 다음 각 프로그램을 실행 후 출력되는 값을 적으시오.

* `printf("%d >> 1의 결과는 %d입니다.\n", x, x>>1);`
* `printf("%d << 2의 결과는 %d입니다.\n", x, x<<2);`

***

다음의 프로그램에서 빈칸을 알맞게 채우시오.

```c
#include <stdio.h>
void main() {
    int num = 0;
    scanf("%d", &num);
    printf("%d의 최하위 비트부터 6번째 비트는 %d이다.\n", num, ______ ? 1 : 0);
```
