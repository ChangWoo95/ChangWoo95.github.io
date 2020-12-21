---
title:  "[SWExpertAcademy10912 외로운문자]"
date: 2020-12-21 20:21:00
categories:
- PS
  tags:
- Python
- SW Expert Academy
- Algorithm
  toc: true
  toc_sticky: true
  toc_label: "[SWExpertAcademy10912 외로운문자]"
---
## 문제
<https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AXVJuEvqLAADFASe&categoryId=AXVJuEvqLAADFASe&categoryType=CODE>

## 접근 방식
같은 알파벳 쌍을 찾는 것이기 때문에 counter를 이용해서 2로 나눈 나머지를 answer에 넣어주는 방식으로 진행했다.

## 풀이

```python
from collections import Counter

t = int(input())

for x in range(1, t+1):
    answer = ""
    word = list(input())  # 입력받은 단어를 리스트형식으로 받음
    word.sort()  # 사전순으로 정렬함
    cntList = Counter(word)  # Counter를 이용해 알파벳 별로 수를 찾음

    for key, value in cntList.items():
        for i in range(value % 2):  # 만약 해당 알파벳을 2로 나누어도 남는 알파벳이 존재한다면
            answer += key  # answer에 해당 알파벳을 더해줌
    if answer == "":  # 해당 단어에서 알파벳이 쌍으로만 있었다면
        print('#{0} {1}'.format(x, "Good"))  # 출력
    else:
        print('#{0} {1}'.format(x, answer))

```

## 후기
처음에는 선형적인 방식으로 접근해서 반복문을 돌리려고 했었다.  
하지만 그 방식으로 진행하는 것이 약간 바보 같아서 방향성을 바꾸게 되었다.  
해당 문제에서는 단순히 **쌍을 이루는 알파벳**을 찾는 것이기 때문에 counter를 이용하는 방식으로 바꾸었다.  
어렵지 않은 문제였던 것 같은데 바로 방식을 생각해내지 못해 조금 아쉬웠던 것 같다.  
다른 공부도 좋지만 알고리즘 학습을 계속 꾸준히 이어가야겠다.
