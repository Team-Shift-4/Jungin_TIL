# Quiz\_ch4\_5

## 4. Input & Basic operator



다음의 프로그램에서 틀린 부분을 알맞게 고치시오.(2개) (각 2점, 총 4점)

```c
#include <stdio.h>
#define PHI(3.14)
int main() {
    int input;
    double circumference;
    printf("반지름을 입력하시오(정수): ");
    scanf("%d", &input);
    circumference = 2 * PHI * input;
    printf("원의 둘레는 %s입니다.\n", &circumference);
    return 0;
}
```

***

(각 2점, 총 4점)   키워드 (          )은 이미 정해진 자료 유형의 이름을 다른 이름으로 재정의 하는 데 쓰인다. 그리고 전처리기 지시자인 (          )은 프로그램 소스에서 지정된 기호 상수를 정의된 치환 문자열로 대체하는 역할을 수행한다.

***

다음의 빈칸에 들어갈 출력 값과 변수 $$x$$의 값을 적으시오. 단 $$x$$의 값은 누적된다. (쌍 당 1점, 총 4점)

| Example code         | Output | Value of variable x |
| -------------------- | ------ | ------------------- |
| int x = 5;           | NaN    | 5                   |
| x++;                 | NaN    | 6                   |
| x--;                 | NaN    | 5                   |
| printf("%d\n", x--); |        |                     |
| printf("%d\n", ++x); |        |                     |
| printf("%d\n", --x); |        |                     |
| printf("%d\n", x++); |        |                     |

***

다음의 프로그램을 수행한 후 화면에 출력되는 값을 그대로 적으시오. (4점)

```c
#include <stdio.h>
#define TRIPLE(x) (x*x*x)
void main() {
    int a = 5;
    printf("%d의 세제곱은 %d입니다.\n", a, TRIPLE(a+a));
}
```

***

다음 프로그램의 빈칸을 알맞게 채워 프로그램을 완성하시오. (빈칸 당 2점, 총 4점)

```c
void main() {
    int sec;
    printf("초를 입력하시오: ");
    scanf("%d", &sec);
    printf("입력하신 %d초를 시간으로 나타내면 %d시 %d분 %d초입니다.\n",
            sec, ______, ______, sec%60);
}
```



