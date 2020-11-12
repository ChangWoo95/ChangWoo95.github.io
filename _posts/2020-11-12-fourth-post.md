---
title:  "[이것이 취업을 위한 코딩 테스트다] 실전: 문자열 재정렬"
date: 2020-11-12 19:26:00
categories:
    - PS
tags:
    - Python
    - 이것이 취업을 위한 코딩 테스트다
    - Simulation
    - Algorithm
toc: true
toc_sticky: true
toc_label: "문자열 재정렬"
---

## 풀이

우선 숫자와 문자에 대해 구별할 필요성을 느꼈다.
그래서 입력받은 문자열에 대해 for문을 돌리면서 alpha리스트로 문자들을 담았고, 숫자들은 정수형으로 변환하여 더해주었다.

## 내 풀이
```python
word = input() # 문자열을 입력받음
alpha = [] # 처음 알파벳을 받기 위한 리스트
num = 0 # 숫자들을 합해주기 위한 변수

for i in word:
    if i.isalpha(): # 알파벳이라면
        alpha.append(i) # 리스트에 추가
    else:
        num += int(i) # 숫자면 정수형으로 변환하여 더함
alpha.sort() # 문자들을 오름차순으로 정렬
alpha.append(str(num)) # 끝에 더해진 숫자를 추가

print(''.join(alpha)) # 이어붙여 출력
```
## 후기

풀고 나서 책의 풀이와 비교했을 때, 거의 똑같이 생각해서 조금 기뻤다.
앞으로 효율적인 코딩을 위해 한 단계 더 파고드는 사고를 할 수 있도록 정진하겠다.