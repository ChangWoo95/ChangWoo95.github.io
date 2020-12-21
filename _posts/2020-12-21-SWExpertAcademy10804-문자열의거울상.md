---
title:  "[SWExpertAcademy10804 문자열의거울상]"
date: 2020-12-21 20:32:00
categories:
- PS
  tags:
- Python
- SW Expert Academy
- Algorithm
  toc: true
  toc_sticky: true
  toc_label: "[SWExpertAcademy10804 문자열의거울상]"
---
## 문제
<https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AXTC0x16D8EDFASe&categoryId=AXTC0x16D8EDFASe&categoryType=CODE>

## 접근 방식
1. 입력받은 문자열을 반전(reverse)시킨다.
2. 반복문을 돌면서 해당 문자의 미러링된 문자를 dictionary에서 찾아 정답에 넣는다.

## 풀이

```python
t = int(input())

reverseDict = {'b': 'd', 'd': 'b', 'p': 'q', 'q': 'p'}  # 반대되는 문자를 미러링하기 위함

for x in range(1, t+1):
    word = list(input())
    word.reverse()  # 입력받은 문자열을 반전 시킴
    answer = ""
    for i in range(len(word)):
        answer += reverseDict[word[i]]  # 해당 문자의 미러링 된 버전을 정답에 넣음
    print('#{0} {1}'.format(x, answer))
```

## 후기
코딩테스트를 준비할 때, 문자열 문제들에 조금 취약한 기분을 받아서 우선적으로 문자열 관련 문제들을 풀고 있다.  
이번 문제는 문제 자체가 일상생활(거울)과 관련된 문제여서 그런지 친근하면서도 감 잡기가 편했다.
