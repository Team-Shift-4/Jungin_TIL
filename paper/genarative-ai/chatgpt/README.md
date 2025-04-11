# 기획중 - 소프트웨어테스팅 기법을 활용하여 ChatGPT의 신뢰도를 올리는 방법

&#x20;글을 참고하여 GPT가 인간보다 약세, 강세, 비슷한 경향을 보이는 문제 유형을 선정하였다.\
-> 해당 페이지 아래에 Problem에 기입

문제는 ChatGPT가 정확히 인식하여 입력과 출력을 양식을 맞출 수 있는 문제로만 진행한다.\
-> GPT-4로 진행한다.

문제 양식을 제출하기 위해 HTML 문서로 문제 페이지를 변환하여 GPT에게 기입한다.\
-> GPT가 백준 문제임을 인식하고 문제를 해결하는 것으로 보여서 문제의 내용만 기입한 후 다시 진행한다.

Prompt template은 "해당하는 HTML 문서의 프로그래밍 문제를 C언어로 작성해줘." 로 진행한다.\
-> HTML로 제출 시 해당 문제가 백준 문제임을 인식하고 검색하여 해결하는 것으로 보여 문제 내용을 복사하여 제출하고 GPT 프로젝트 지침으로 "해당하는 문제를 해결하는 C언어 코드를 출력해줘."로 진행한다.\
-> 이미지 힌트도 얻을 수 있고 일관적인 문제 해결 능력과 백준 문제임을 인식하지 못하게 하기 위해 Markdown으로 작성한 문제를 제출하고 GPT 프로젝트 지침으로 "제출하는 마크다운 파일을 읽고 해당하는 문제를 해결하는 C언어 코드를 출력해줘."로 진행한다.

<figure><img src="../../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>



'25.04.04: Greedy Aproach Test

'25.04.08: All case test done; Detail hit-rate test

공정한 독립 시행을 위해 프롬프트는 단 한번만 활용하고 제거한다.\
프로젝트를 생성하여 문제 파일을 마크다운으로 제공한 뒤 최대한 변수를 제거하기 위해 전체 테스트 했을 때의 지침을 활용하여 행동하도록 유도한다.\
아래는 프롬프트 내용이다.

```
프로젝트 파일 4.md를 지침에 따라 행동해줘
```

***

질문 수 제한이 너무 낮아 방법을 바꿔 AI의 신뢰도를 높이는 것을 바탕으로 동작시킬 것이기 때문에 gpt-4o-mini 모델을 활용하여 Hit rate가 8할, 5할, 2할에 준하는 케이스들을 찾을 예정이다.

발견한 케이스는 총 네개, 80%, 60%, 20%, 0%이다.\
각 케이스는 아래와 같다.

* [https://www.acmicpc.net/problem/10974](https://www.acmicpc.net/problem/10974) 80%/81%
* [https://www.acmicpc.net/problem/24389](https://www.acmicpc.net/problem/24389) 60%/67%
* [https://www.acmicpc.net/problem/2417](https://www.acmicpc.net/problem/2417) 40%/20%
* 0%/8%

&#x20;

<table><thead><tr><th width="109">Problem</th><th width="180.3333740234375">Link</th><th>Pass rate per 10 times</th><th>Pass rate per 50 times</th><th>Wrong reason : Number of times</th></tr></thead><tbody><tr><td>10974</td><td><a href="https://boj.kr/10974">https://boj.kr/10974</a></td><td>80%</td><td>81%(9)</td><td>Wrong: 9</td></tr><tr><td>24389</td><td><a href="https://boj.kr/24389">https://boj.kr/24389</a></td><td>60%</td><td>68%(16)</td><td>Time out: 8<br>Wrong: 8</td></tr><tr><td>2417</td><td><a href="https://boj.kr/2417">https://boj.kr/2417</a></td><td>40%</td><td>20%(40)</td><td>Time out: 20<br>Wrong: 20</td></tr><tr><td>5568</td><td><a href="https://boj.kr/5568">https://boj.kr/5568</a></td><td>0%</td><td>8%(46)</td><td>Compile error: 4<br>Out of bounds: 10<br>Buffer overflow: 1<br>Wrong: 31</td></tr></tbody></table>

