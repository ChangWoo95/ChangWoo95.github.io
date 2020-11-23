---
title:  "[백준14503: 로봇 청소기]"
date: 2020-11-23 22:20:00
categories:
    - PS
tags:
    - Python
    - Baekjoon
    - Simulation
    - Algorithm
toc: true
toc_sticky: true
toc_label: "로봇 청소기"
---
## 문제 
<https://www.acmicpc.net/problem/14503>


## 풀이
입력 받아야 할 정보들을 입력받음<br>
deque를 이용하여 로봇 청소기의 현 위치와 방향을 저장<br>
1. 현 위치가 청소할 수 있는 공간이면 청소
2. 현 방향 기준 왼쪽으로 90도씩 회전하면서 청소할 수 있는 공간이 있는지 확인하고 있다면 deque에 저장하고 탈출
3. 4방향 모두 갈 곳이 없다면 현재 방향 기준 뒤로 한 칸 후진
4. 후진도 할 수 없는 경우, 종료

## 내 풀이
```python
from collections import deque

R, C = map(int, input().split())  # 행과 열 입력
area = []  # 청소할 map
# 앞에부터 순서대로 북, 동, 남, 서
dx = [-1, 0, 1, 0]
dy = [0, 1, 0, -1]
q = deque()

robot = list(map(int, input().split()))  # 로봇의 현위치 및 방향 입력
q.append([robot[0], robot[1], robot[2]])  # deque에 삽입

for _ in range(R):
    area.append(list(map(int, input().split())))

def FindCleaningArea(q):
    cnt = 0  # 청소한 공간의 갯수
    while q:  # q가 비어있지 않을 동안
        cx, cy, direction = q.popleft()

        if area[cx][cy] == 0:  # 아직 청소하지 않은 공간이라면
            area[cx][cy] = 2  # 여기서 2는 청소를 했다는 의미
            cnt += 1
        i = direction
        for _ in range(4):
            i += 3  # 원래 배열의 순서는 북, 동, 남, 서이지만 회전의 경우, 왼쪽방향으로 90도 회전이기 때문에 + 3을 더함
            i %= 4  # 4로 나눈 나머지로 설정한 이유: 배열의 범위를 초과하지 않는 선에서 4방향을 확인하기 위함
            nx, ny = cx + dx[i], cy + dy[i]  # 다음 갈 곳의 좌표
            if nx < 0 or nx >=R or ny < 0 or ny >= C: continue  # map의 크기를 초과하면 continue
            if area[nx][ny] == 0:  # 아직 청소하지 않는 공간이라면
                q.append([nx, ny, i])  # q에 삽입
                break
        if len(q) == 0:  # 4방향으로 다 확인했는데도 갈 곳이 없는 경우(뒤로 후진)
            nx, ny = cx - dx[direction], cy - dy[direction]
            if area[nx][ny] != 1:  # 뒤로 후진할 수 있다면
                q.append([nx, ny, direction])
    return cnt

print(FindCleaningArea(q))
```
## 후기
- 솔직히 구현 문제이기도 하고 단순하게 생각해서 접근을 했었다. 
- 정해놓은 시간(30분) 안에 풀지 못하고 문제점을 찾아봤는데, 방향을 정하기 위한 배열은 북, 동, 남 ,서 순으로 **시계 방향**인데, 청소하는 공간찾기의 경우 **시계반대방향**으로 접근하는 것을 놓쳤었다...
- 빠른 정답풀이보다는 **정확한** 코딩을 할 수 있도록 접근을 해야겠다. 