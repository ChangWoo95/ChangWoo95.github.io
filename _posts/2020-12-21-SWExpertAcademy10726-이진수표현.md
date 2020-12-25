---
title:  "[SWExpertAcademy10726 이진수 표현]"
date: 2020-12-21 20:21:00
categories:
    - PS 
tags:
    - Python
    - SW Expert Academy
    - Algorithm
toc: true
toc_sticky: true
toc_label: "[SWExpertAcademy10726 이진수 표현]"
---
## 문제
<!--break-->
<https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AXRSXf_a9qsDFAXS&categoryId=AXRSXf_a9qsDFAXS&categoryType=CODE>

## 접근 방식
특정 숫자를 이진수로 나타내어주는 bin을 이용하여 진행

## 풀이

```python
def isOne(m):  # 원하는 부분의 비트가 모두 1인지 확인하기 위한 함수
    for i in range(n):  # 0~ n-1까지 반복
        if m[i] == '1':  # 해당 비트가 1이면 계속
            continue
        else:  # 그렇지 않으면 False return
            return False
    return True

t = int(input())

for x in range(1, t+1):
    n, m = map(int, input().split())
    m = list(bin(m))  # 이진화된 문자열리스트를 얻기 위함
    m.reverse()  # bin사용 시, 0b~~~로 시작하고 또한 문제에서 마지막 n자리까지 요구하므로 뒤부터 찾기 위해 reverse 진행
    if isOne(m):  # 원하는 부분의 비트가 모두 1로 켜져있다면
        print('#{0} {1}'.format(x, "ON"))
    else:  # 그렇지 않다면 
        print('#{0} {1}'.format(x, "OFF"))
```

## 후기
C++의 bitSet같은 문법이 있는지 알아보던 중, bin이라는 문법을 알게 되었다.  
해당 문법을 이용하면 0b~~~형식의 이진수형태의 문자열을 얻을 수 있다.  
문제에서의 조건이 마지막 n개의 bit의 상황을 물어보는 것이기에 reverse로 뒤집은 후, n만큼 반복문을 돌려서 모두 1이면 ON을,  
그렇지 않으면 OFF를 출력해주게 했다. 쉬워서 그런건지는 모르겠는데 풀 때 빠르게 풀어내는 것 같아서 기분이 좋았다.
