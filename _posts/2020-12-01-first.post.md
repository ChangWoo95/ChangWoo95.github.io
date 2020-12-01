---
title:  "[boiler-plate #3] browser에 보여질 page 구현"
date: 2020-12-01 17:31:00
categories:
    - boiler-plate
tags:
    - Node.js
    - Express.js
    - React
    - MongoDB
    - TIL
    - 실습
toc: true
toc_sticky: true
toc_label: "[boiler-plate #3] browser에 보여질 page 구현"
---
## github Link
<https://github.com/qaqa313a/boiler-plate-ko>  
오늘 사이트 입장 시 보여질 첫 페이지와 로그인 쪽 페이지를 구현하면서 알게된 정보들을 정리하겠다.

## 정리
1. CSS framework 중 Ant design
   - 장점: style이 깔끔하고 쓰기 편하다.
   - 단점: 이용 시 size가 크다. (들어가 있는 것들이 많아서)

2. redux: state를 관리해주는 **TOOL**

3. props VS state
   1. props:
      - property의 줄임말
      - component간 주고 받을 때 이용
      - 소통방식: 부모 -> 자식으로만 가능
      - 자식에서는 부모가 준 값을 **변경못함(immutable)**
   2. state:
      - 어떤 component안의 data를 전달 및 변경
      - mutable(값 변경 가능)
      - state가 변하게 되면 re-rendering 진행
4. redux 동작방식
   ![Image Alt 텍스트](/assets/images/2020-12-01_image1.png){: width="300" height="300"}

4. redux-promise, redux-thunk
    - redux Store는 object를 받아 수행하게 되는게 promise 또는 Functions 형태로 올 때가 있음  
    -> 이를 어떻게 해결해줄지를 제시해줌 

## 후기
  - 오늘 react의 동작방식과 어떻게 진행되는지에 많이 알 수 있는 시간이었다.  
  props와 state에 대해 애매하게 알고 있었는데 이번 기회에 좀 더 명확하게 입력될 수 있는 계기가 되었다.  
  빨리 여러 component를 만들어보고 다뤄보고 싶다.
