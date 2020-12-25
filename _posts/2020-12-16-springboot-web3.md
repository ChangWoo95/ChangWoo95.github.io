---
title:  "[스프링 부트로 배우는 Java web 개발#3] 정리"
date: 2020-12-17 20:47:00
categories:
    - Spring
tags:
    - Spring boot
    - Java
    - TIL
    - study
toc: true
toc_sticky: true
toc_label: "[스프링 부트로 배우는 Java web 개발#3] 정리"
---
API 작성 및 database 관련 실습 진행한 것을 정리해보겠다.

## 정리
- REST 특성
  1. server, client는 독립적으로 구분
  2. server, client간 통신 시 상태가 없어야함  

- API: 데이터와 기능의 집합  

- Rest Controller: 기존 컨트롤러 annotation + ResponseBody  

- ResponseBody: 실행결과 처리를 위한 어노테이션  

- ResponseEntity: 응답헤더에 대한 구현체  

- swagger: API정보를 Json으로 매핑해서 문서를 생성 -> swagger VI  

- SQl mapper(iBatis), ORM(JPA) : 복잡해지는 쿼리문 등을 해결하기 위해 등장  
  -> 그중에서 spring data jpa와 querydsl이 자주 사용됨  

- ORM(Object Relational Mapping)이란?  
  object와 relation간의 불일치 문제를 해결하기 위한 도구  
  => 사용이유: 반복되는 코드를 줄이고 객체 중심의 설계를 위함  

- JDBC(Java Database Connectivity): 자바로 데이터베이스 프로그래밍을 하기 위한  API  

- hsqldb: 데이터 저장소, JDBC를 지원  

- Entity 클래스: 데이터베이스 스키마의 내용을 자바클래스로 표현(@Entity로 인식시킴)  

- Id annotation: 데이터베이스에서 제공하는 시퀀스 값 또는 주 키 매핑


## 후기
API실습까지는 기존의 해왔던 경험들이 있어서 그런지 이해하는데 있어서 많이 어렵지는 않았다. 그러나 JPA 및 QueryDSL을 할 때는  
버전 상의 변경된 표현들이 몇몇 있어서 그런건지 모르겠는데 gradle 잡는것부터 해서 한참 걸린 것 같다.....  
하지만 나의 경우만 해도 이전에 해온 웹 프로젝트들에서 반복되는 sql문 대입으로 인해 불편한 점들이 여럿 있었는데,  
그런 것들을 해소해줄수도 있고 객체지향적 문법 및 표현식을 알 수 있었던 좋은 계기였다.
