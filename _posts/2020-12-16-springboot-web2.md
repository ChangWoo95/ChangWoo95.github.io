---
title:  "[스프링 부트로 배우는 Java web 개발#2] 정리"
date: 2020-12-16 01:04:00
categories:
- Spring
tags:
- Spring boot
- Java
- TIL
- study
toc: true
toc_sticky: true
toc_label: "[스프링 부트로 배우는 Java web 개발#2] 정리"
---
원래 어제 올리려고 했으나, 실습하다가 뭐가 잘 안돌아가서 한참 부여잡다가 지금 쓰게 되었다.

## 정리
- @import annotation  
  configuration 클래스를 묶을 수 있음 -> 이로 인해 설정 정보 추적에 용이  
  register 및 refresh를 통해 할수도 있지만, 파라미터 제공으로도 대체 가능  
  
- @post construct  
  bean이 초기화될 때, 호출된다.  
  별도의 매핑없이 사용가능  
  
- 스프링 MVC
  Front controller 패턴에 spring의 의존성 주입(DI)을 이용해,  
  컴포넌트의 생명주기를 관리할 수 있는 컨트롤러 중심의 웹 MVC framework  
  구성요소:
  1. dispatcher servlet
  2. view resolver
  3. Interceptor
  4. Handler
  5. view 등  
  
- 자바에서의 결과 파일 포맷은 2개인데 (로컬) jar과 (웹 애플리케이션 컨테이너) war가 있다.  
  
- 스프링 부트는 기본적으로 runnable jar로 실행  
  
- 웹 리소스 폴더: ex) resources, static, public  
  webMVCConfigureAdapter: static, public 이외에 다른 폴더 지정 및 캐시 설정 변경 등  
  => spring5이상부터 webMVCConfigurer

## 후기
슬슬 여러 어노테이션들이 나오기 시작했다..... 어노테이션을 이용하면 xml 및 bean설정을 줄이면서  
간략하게 진행할 수 있는 장점이 있지만, 아직 완벽히 잘 모르는 나에게 있어서는 조금 버거운 부분들인 것 같다.  
아마 다음장은 rest api 서버 쪽을 다룰 것 같은데 실습을 진행하는 것도 중요하지만 제대로 이해하면서 넘어가는 것이 중요할 것 같다!!
