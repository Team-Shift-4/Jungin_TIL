# Quiz\_ch11\_1

다음의 물음에 답하시오.

* `char c[]="Clanguage";`라고 문자열을 선언했을 때 배열 c의 크기는 얼마인가?
* 문자열의 마지막에 꼭 들어가야 할 문자는 무엇인가?

***

isupper(int c)는 문자 c가 알파벳 대문자인지를 검사하여 대문자이면 0이 아닌 수, 대문자가 아니면 0을 리턴하는 함수이다.\
이 함수를 이용해 문자열에 포함된 알파벳 대문자를 알파벳 소문자로 변환하려는 기능을 구현하려 한다.\
대문자를 소문자로 변환할 때 알파벳의 ASCII 코드 값을 이용하는 방법이 있다.\
다음 빈 칸에 들어갈 코드를 간단하게 적으시오.

```c
for(i = 0; i < strlen(str); ++i) {
    if(isupper(str[i])) {
        str[i] = str[i] + ___________;
    }
}
```

***

다음 간단한 프로그램 코드의 출력값을 적으시오.

```c
if(strcmp("abcD", "abcd") == 0) {
    printf("yes");
}
else
    printf("no");
```

***

입력값을 "Class C Languague"로 주었을 때 다음 프로그램 종료 후의 결과값을 적으시오.

```c
int i;
char line[80], line2[80];
scanf("%s", line);
for(i = 0; i < strlen(line); i++)
    printf("%c", tolower(line[i]));
gets(line2);
for(i = 0; i < strlen(line2); i++)
    printf("%c", toupper(line2[i]));
```

***

회문(Palindrome)이란 Level, Rotator와 같이 앞에서부터 읽든 뒤에서부터 읽든 같은 단어가 되는 단어이다.\
다음은 한 단어를 입력받아 그 단어가 회문인지 검사하는 프로그램이다.\
잘못된 부분을 수정하시오.(2개)

```c
int i, n, count = 0;
char *line;
printf("Enter a string : ");
gets(line);
n = strlen(line);
for (i = 0; i < n / 2; i++) {
    if(line[i] != line[n-i-1]) {
        count++;
        break;
    }
}
if(count == n / 2)
    printf("yes\n");
else
    printf("no\n");
```
