---
title:  "[스프링 부트로 배우는 Java web 개발#1] 정리"
date: 2020-12-13 18:07:00
categories:
    - Spring
tags:
    - Spring boot
    - Java
    - TIL
    - study
toc: true
toc_sticky: true
toc_label: "[스프링 부트로 배우는 Java web 개발#1] 정리"
---
Servlet, Jsp까지의 실습을 모두 마쳤고, 스프링 웹 초기 진행중에 있다.  
오늘 한 내용들을 정리해보려고 한다.

## 정리
  - Servlet과 Jsp  
    1. **Servlet:**  
        - 웹 기반의 요청에 대한 동적인 처리가 가능한 server side에서 돌아가는 JAVA program(하나의 클래스)  
        - java코드 안에 HTML코드가 들어감  
    2. **Jsp(java server pages):**
        - 자바 언어를 기반으로 하는 server side 스크립트 언어  
        - HTML코드 안에 JAVA코드가 들어감  
        - 백그라운드에서 servlet으로 자동 변환  
    3. 차이:  
    - servlet의 경우 controller에서 이용하기 좋고 수정하게 되면, 전체 코드 업데이트 후에 다시 컴파일해서 재배포해야해서 생산성이 저하된다.
    - JSP의 경우 view에서 이용하기 좋고 수정하게 되면 WAS가 알아서 처리해준다.(쉬운 배포)

  - HTTP 프로토콜은 비상태(stateless) 프로토콜이다.  
    1. 쿠키: 사용자가 사이트 방문 시, 컴퓨터에 저장되는 정보
    2. 세션: 서버와 클라이언트의 유효한 커넥션을 식별하기 위한 정보

  - SPRING  
    1. IOC(Inversion of control) 제어의 역전:  
        프로그램의 생명주기에 대한 주도권이 웹 애플리케이션 컨테이너에 존재
    2. DI(의존성 주입):  
        객체 간 결합도를 줄이기 위함

  - extends와 implements  
    1. extends: 상속의 대표적 형태, 부모의 메소드 그대로 사용가능하며 오버라이딩이 굳이 필요 없다.
    2. implements: 부모의 메소드를 반드시 오버라이딩(재정의)해야함
   ![Image Alt 텍스트](/assets/images/2020-12-13-image1.PNG){: width="300" height="300"}    


## 후기
확실히 조급하게 하는것보다 천천히 하면서 알아가는 것이 머릿속에도 이해가 잘되고 안까먹게 되는 것 같다. 서블릿과 JSP를 완벽히 아는 것은 아니지만 공부하고 실습하면서 늘려나가도록 하겠다.  
그리고.... 자바 프로그래밍 공부하면서 알고리즘 공부도 해줘야겠다.
