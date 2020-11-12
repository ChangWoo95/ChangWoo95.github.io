---
title:  "[리액트를 사용할 고급 웹앱 클라이언트 제작#1] 기본적인 구조"
date: 2020-11-12 13:12:00
categories:
    - Toy project
tags:
    - react
    - 실습
toc: true
toc_sticky: true
toc_label: "[리액트를 사용할 고급 웹앱 클라이언트 제작#1] 기본적인 구조"
---

## 현재까지 작성한 코드(app.js)
```xml
import React, { Component } from 'react';

export default class App extends Component {

  constructor(props) {
    super(props);
    this.state = {
      userName: "qaqa313a"
    }
  }

  changeStateData = () => { //화살표 함수로 이용
    this.setState({
      userName: this.state.userName === "qaqa313a" ? "me" : "qaqa313a"
    })
  }

  render = () =>
      <div>
        <h4 className="bg-primary text-white text-center p-2">
          {this.state.userName}'s To Do List
        </h4>
        <button className="btn btn-primary m-2" onClick={ this.changeStateData }>
         Change
        </button>
      </div>
}
```

## 알게 된 점
- React에서는 컴포넌트가 정희한 프로퍼티나 메소드를 호출할 때는 항상 this키워드를 이용해야 한다!!
- 화살표 함수의 경우, return 키워드와 함수내용을 둘러싸는 중괄호도 생략가능하다.