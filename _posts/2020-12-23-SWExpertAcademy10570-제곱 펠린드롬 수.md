---
title:  "[SWExpertAcademy10570 제곱펠린드롬 수]"
date: 2020-12-23 19:54:00
categories:
- PS
tags:
- Python
- SW Expert Academy
- Algorithm
toc: true
toc_sticky: true
toc_label: "[SWExpertAcademy10570 제곱펠린드롬 수]"
---
## 문제
<https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AXO72aaqPrcDFAXS&categoryId=AXO72aaqPrcDFAXS&categoryType=CODE>

## 접근 방식
1. 먼저 해당 수가 완전제곱수인지 판별한다.
2. 완전 제곱수가 맞다면 두 수(원래 수, 제곱근)가 모두 회문인지 판별한다.

## 풀이

```python
def isPalindrome(i, j):  # 원래 수와 거듭제곱근이 회문인지 확인
    num1 = str(i)
    num2 = str(j)

    if num1 == ''.join(reversed(num1)) and num2 == ''.join(reversed(num2)):
        return True
    else:
        return False

t = int(input())

for x in range(1, t+1):
    a, b = map(int, input().split())
    answer = 0
    for i in range(a, b+1):
        if int(i ** 0.5) ** 2 != i:  # 해당 수가 완전제곱수가 아니라면
            continue  # 넘김
        else:  # 완전제곱수인 경우
            if isPalindrome(i, int(i ** 0.5)):
                answer += 1

    print('#{0} {1}'.format(x, answer))
```

## 후기
이번에도 문자열 문제다. 완전제곱수인지 먼저 판별한 후에 isPalindrome함수를 통해 두 수 모두 회문인지 확인해주었다.  
완전제곱수를 찾는 과정에서 sqrt 등 여러가지 방법을 사용해보려 했는데 역시 현재 진행한 방법이 나한테는 좀 더 편했던 것 같다.
