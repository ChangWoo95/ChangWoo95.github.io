---
title:  "[백준1407 국회의원 선거]"
date: 2020-11-28 16:16:00
categories:
    - PS
tags:
    - Python
    - Baekjoon
    - Algorithm
toc: true
toc_sticky: true
toc_label: "[백준1407 국회의원 선거]"
---
## 문제 
<https://www.acmicpc.net/problem/1417>
## 풀이

```python
import heapq

N = int(input())
votes = []
for _ in range(N):
    votes.append(int(input()))
result = votes[0]
if N == 1:
    print(0)
else:
    q = []
    for i in range(1, len(votes)):
        heapq.heappush(q, (-votes[i], votes[i]))
    while(result <= q[0][1]):
        ord, tmp = heapq.heappop(q)
        tmp -= 1
        result += 1
        heapq.heappush(q, (-tmp, tmp))
    print(result - votes[0])

```

## 후기
오늘 N회사의 코딩테스트를 봤었는데, 비슷한 유형의 문제가 있다고 해서 풀어보았다.
코딩테스트 당시 결국 이 문제에서 점수를 받지 못했다.. 지금 풀면서 다시 생각해보니, while문에서의 조건을 잘못잡아서 테케에서 걸린게 아닌가 싶다..
스스로에게 조금, 아니 너무 아쉬웠던 코딩테스트였던 것 같다. 코딩대회처럼 풀이시간 및 제출횟수로 차등 점수가 발생하는 시스템이었는데 그것때문인지는 몰라도 푸는 내내 조급함을 가지고 해서 해결하지 못했던 것 같다.
앞으로 그러지 않기 위해 좀 더 침착하게 대응하는 습관을 길들여야겠다.
