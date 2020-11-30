---
title:  "[boiler-plate #1] 로그인"
date: 2020-11-29 17:45:00
categories:
    - boiler-plate
tags:
    - Node.js
    - Express.js
    - MongoDB
    - 실습
toc: true
toc_sticky: true
toc_label: "[boiler-plate #1] 로그인"
---
## github Link
<https://github.com/qaqa313a/boiler-plate-ko>

## 정리
로그인 기능을 만들면서 배웠던 지식을 정리하려고 한다.

1. pre() <br>
   MongoDB에서 제공하는 기능으로써 현재 사용했던 경우는 DB에 저장하기 전에 구현한 함수를 진행시켜 비밀번호 변경유무에 따른 조건을 걸었다.
2. findOne() <br>
   MongoDB에서 제공하는 기능으로써 요청된 E-mail이 DB에 있는지 확인하는 기능을 담당함

## 후기
- 로그인 기능을 구현하면서 MongoDB의 스키마를 짰었는데 확실히 관계형 DB보다 구현하는데 있어 편리함이 있는 것 같다.
- 또한 로그인 시, 토큰을 만들고 나서 토큰을 저장하기 위한 여러가지(session, cookie)를 알게 되었다. 교내에서 진행한 프로젝트에서는 항상 session을 사용했었는데 이번 기회에 cookie로 진행하게 되었다. 아직 초반부이지만 지속해서 실습을 진행하겠다.
