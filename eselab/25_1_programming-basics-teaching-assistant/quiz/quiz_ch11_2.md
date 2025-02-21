# Quiz\_ch11\_2

다음의 물음에 답하시오.

* 명령어줄(Command line)에 "command.exe red green blue"의 명령이 주어질 때, argv의 첫 번째 값은 무엇인가?
* 명령어 인수를 받기 위한 main 함수의 두 개의 파라미터 argc, argv는 각각 어떤 자료형인가?\
  int main(argc, argv) -> int main(\_\_\_\_\_\_\_\_\_\_, \_\_\_\_\_\_\_\_\_)

***

아래 프로그래밍의 수행결과를 출력해보자.

```c
int i;
char *lang[] = {"C", "Java", "CPP"};
char langArr[][5] = {"C", "Java", "CPP"};

printf("%d %d\n", strlen(lang[0]), strlen(langArr[0]));
printf("%d %d\n", strlen(lang[1]), strlen(langArr[1]));
printf("%d %d\n", strlen(lang[2]), strlen(langArr[2]));
```

***

다음 프로그램을 수행하면서 키보드로 "abcdq"를 입력할 때 화면에 표시되는 입출력 값을 그대로 적으시오.

```c
#include <stdio.h>
#include <conio.h>
char ch;
printf("문자를 누를 때마다 2번 출력 >>\n");
while((ch  = getche()) != 'q')
    putchar(ch);
```

***

아래 프로그램의 수행 결과는 원하는 결과가 나오지 않는다.\
제대로 출력되도록 수정해보자.

```c
int i, len;
char des1[6], dst2[20];
char *src = "abcdef";
len = strlen(src);
for(i = 0; i < len; i++) {
    dst1[i] = src[i];
    dst2[i] = src[i];
}
printf("%s %s\n", dst1, dst2);
```

***

아래 프로그램은 문자열을 공백과 콤마로 분할하는 프로그램을 보여준다.\
빈 곳에 적당한 코드를 추가해보자.

```c
char *delimiter = " ,";
char str1[] = "C, C++ language are best!";
ptoken = strtok(str1, delimiter);
while(ptoken != NULL) {
    printf("%s \n", ptoken);
    ptoken = (____________);
}
```
