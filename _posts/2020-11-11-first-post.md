---
title:  "[이것이 취업을 위한 코딩 테스트다] 미로탈출"
date: 2020-10-22 23:43:00
categories:
    - PS
tags:
    - Python
    - 이것이 취업을 위한 코딩 테스트다
    - BFS/DFS
    - Algorithm
toc: true
toc_sticky: true
toc_label: "[이것이 취업을 위한 코딩 테스트다] 미로탈출"
---

## 풀이

기본적인 BFS문제이다.
탈출을 위한 함수의 원리는 다음과 같다.  

1. deque 안에 시작점을 추가
2. 큐가 빌 때까지 반복하는데 상, 하, 좌, 우의 좌표를 확인
3. 좌표가 지정된 맵보다 초과하거나 더 작다면 continue
4. 처음 방문하는 곳이고 이동할 수 있는 곳이면 방문정보 갱신 및 큐에 추가

```python
from sys import stdin
from collections import deque
input = stdin.readline

#bfs 접근방식
def find_exit(x, y):
    q = deque() #deque 선언
    q.append((x, y)) #시작점 추가
    visited[x][y] = 1
    while q:
        cx, cy = q.popleft()
        for i in range(4):
            nx, ny = cx+dx[i], cy + dy[i]
            if nx < 0 or nx >= N or ny < 0 or ny >= M: continue #미로의 크기보다 작거나 큰 경우, 넘어감
            if not visited[nx][ny] and miro[nx][ny] == 1: #방문하지 않았고, 해당 칸이 이동할 수 있는 곳이면
                visited[nx][ny] = visited[cx][cy] + 1
                q.append((nx, ny))
    return visited[N-1][M-1]

N, M = map(int,input().strip().split()) #행, 열 입력
miro = list() #미로의 입력값을 받기위한 리스트
visited = [[0]*M for _ in range(N)] #방문여부를 알려주는 2차원 리스트
#상,하,좌,우로 이동할 때 쓰이는 리스트
dx = [1, -1, 0, 0]
dy = [0, 0, 1, -1]

for _ in range(N):
    miro.append(list(map(int,input().strip())))

print(find_exit(0,0))
```

## 후기

기본적인 유형이라서 금세 풀었던 것 같다.
앞으로 한 문제에 대해 BFS와 DFS를 둘 다 만들어서 연습해봐야겠다. 