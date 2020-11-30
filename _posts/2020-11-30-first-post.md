---
title:  "[boiler-plate #2] server part 구현 및 client part 구현"
date: 2020-11-30 19:27:00
categories:
    - boiler-plate
tags:
    - Node.js
    - Express.js
    - React
    - MongoDB
    - 실습
toc: true
toc_sticky: true
toc_label: "[boiler-plate #2] server part 구현 및 client part 구현"
---
## github Link
<https://github.com/qaqa313a/boiler-plate-ko>

오늘 인증 기능 및 로그아웃 기능을 구현했고, client에서 component만 나누었다.<br>
배웠던 내용들을 정리해보려고 한다.

1. logout <br>
   login시 등록된 token을 해제시킨다.
2. React <br>
   - No framework -> Library
   - Components(모듈의 일종)을 이용하며 재사용성이 높음
   - Real DOM과 Virtual DOM의 차이: Real DOM은 하나의 리스트를 수정해도 전체를 reload해야하지만,<br>
     Virtual DOM은 바뀐 부분만 탐지하고 update -> 이를 **diffing**이라 부름
3. Virtual DOM의 동작방식:
   1. JSX를 렌더링 -> Virtual DOM이 업데이트됨
   2. 현재의 Virtual DOM과 이전에 Virtual DOM에서 찍은 snap-shot과 비교하여 바뀐 부분을 탐지
   3. 바뀐 부분만 Real DOM에 적용

## 후기
  - server 파트와 client의 port가 다를 때, 단순히 URL을 입력해준다고 연결되지 않는다는 것을 처음 알았다..<br>
    **CORS(Cross-Origin Resource Sharing)**정책으로 인해 되지 않는다고 하는데 이 정책은 추후에 다시 정리하겠다.
  - 그리고 이를 이어줄 수 있는 방법 중 하나가 proxy인데, 3학년 때 봤었던 proxy를 여기서 다시 봐서 당황스럽기도 하고, <br>
    이런 방식으로 이용된다는 것이 조금 놀라웠다.
  - 이제 client에서 react component를 실습할 예정인데 OOP의 클래스 개념처럼 나누어 진행하는 것이 재미가 있는 것 같다.
