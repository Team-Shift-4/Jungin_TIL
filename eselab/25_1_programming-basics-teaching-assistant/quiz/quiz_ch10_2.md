# Quiz\_ch10\_2

다음의 설명에 적합한 코드를 작성하시오.

* 10x10 크기의 2차원 배열 2개를 함수 인자로 받고 반환값이 없으며 이름이 reverse인 함수를 선언한다.
* 크기가 4x4x4인 행렬 1개를 함수 인자로 받고 정수를 반환하며 이름이 cube인 함수를 선언한다.

***

다음 문장의 참/거짓을 밝히시오.

* 2x2 크기의 정수형 배열 ary에서 ary\[0]\[1]과 ary\[1]\[0]은 연속적으로 배치되어 저장된다.
* int의 크기가 4바이트일 때, int test\[10]\[20]\[8]의 크기는 1600바이트이다.

***

다음 프로그램을 실행한 후 프로그램의 출력값을 적으시오.

```c
#include <stdio.h>
int com(char ary[], char ary2[], int size) {
    int i;
    for(i = 0; i < size && (ary[i] == ary2[i]); ++i);
    return i == size;
}
void main() {
    char x[100] = "abc";
    char y[100] = "def";
    printf("%s", com(x, y, 3) ? "same" : "not same");
}
```

***

다음의 프로그램을 실행한 후 화면에 출력되는 값을 그대로 적으시오.

```c
#include <stdio.h>
void main() {
    int threeDimension[3][3][3], x, y, z;
    for(z = 0; z < 3; z++) 
        for(y = 0; y < 3; y++) 
            for (x = 0; x < 3; x++) 
                threeDimension[z][y][x] = x + y*3 + z*9;
    for(z = 0; z < 3; z++) {
        for(y = 0; y < 3; y++) {
            for(x = 0; x < 3; x++) {
                printf("%3d ", threeDemension[z][y][x]);
            }
            printf("\n");
        }
        printf("\n");
    }
}
```

