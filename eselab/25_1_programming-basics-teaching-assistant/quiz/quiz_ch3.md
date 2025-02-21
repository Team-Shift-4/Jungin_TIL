# Quiz\_ch3

자료형 unsigned int와 signed long의 저장 공간에서 표현할 수 있는 정수 값의 범위는 얼마인가?\
(각 1점, 총 2점)

* unsigned int :                    \~
* signed long :                     \~

***

아래 코드의 수행 결과를 출력해보자.

```c
unsigned short umax;
short max = pow(2, 15) - 1;
umax = max + 1;
printf("%d\n", umax);
max = max + 1;
printf("%d\n", max);
```

***

다음 자료형으로 양의 정수를 표현할 때, 표현할 수 있는 최대값이 작은 것부터 나열하시오.

* signed short, unsigned int, unsigned char, int, double, float

***

다음의 프로그램 수행 후 예상되는 출력 값을 적으시오.

```c
#include <stdio.h>
void main() {
    unsigned char a = 30;
    int b = 7;
    printf("%d\n", sizeof(short)-sizeof(a));
    printf("%d\n", sizeof(b)-sizeof(short));
    printf("%d\n", sizeof(float)-sizeof(b));
    printf("%d\n", sizeof(int)-sizeof(a));
}
```

***

다음 실행 화면이 나오도록 프로그램을 작성하려 한다.\
아래 소스 코드에엇 틀린 부분을 찾아서 수정하시오.

```
대문자 J의 출력값은 F 이고 ASCII값은 %d 이다.
```

```c
#include <stdio.h>
int main(void) {
    unsigned char ch = 'F';
    printf("hello students ^^.\n");
    printf("대문자 J의 출력값은 %d 이고 ASCII값은 %d 이다.\n", ch, ch);
    return 0;
}
```
