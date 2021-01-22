---
title:  "[Java] 프로그래밍 입문 #0"
date: 2020-12-10 22:09:00
categories:
- Java
tags:
- Java
- TIL
- study
toc: true
toc_sticky: true
toc_label: "[Java] 프로그래밍 입문 #0"
---
하반기 취업일정이 거의 끝나가면서 Java 프로그래밍과 Spring에 대한 학습이 더 필요하다고 느껴 시작하게 되었다.  
spring에 대한 정리도 추후 올리도록 하겠다.

## 정리
- JVM(자바 가상 머신): 자바 프로그램 실행환경을 만들어주는 software  
    1. 자바코드를 컴파일하여 .class 바이트 코드로 만들어준다.
    2. 해당 코드가 자바 가상머신 환경에서 실행된다.
- GC(가비지 컬렉터): 더이상 사용되지 않는 메모리를 주기적으로 수거  
    자바의 경우, C와는 다르게 메모리를 직접 해제해주지 않고 GC가 자동으로 해제해줌으로서 관리하게 된다.
- JDK(Java Development Kit)
    1. SE: standard editon, 기본 자바 개발환경
    2. EE: enterprise edition, 서버기반 프로그램의 개발환경(servlet, jsp 개발)
    3. ME: micro edition, 모바일 및 임베디드 프로그래밍에 이용
- 상수의 경우, final 예약어를 이용하여 선언
- 묵시적 형 변환: 작은 바이트에서 큰 바이트의 자료형으로 변환하는 경우 자동 형 변환이 가능함  
- 명시적(강제) 형 변환: 큰 바이트에서 작은 바이트의 자료형으로 변환하는 경우 ex. (int) 변수 처럼 강제로 진행해주어야함  

- 객체: 소프트웨어 상의 구현할 대상, 클래스의 **'인스턴스'**라고도 함, 모든 인스턴스를 포함하는 포괄적 의미

- 클래스: 객체를 설계하기 위한 설계도
- 인스턴스: 객체를 메모리 할당하여 실체화하면 이를 인스턴스라 부름
    1. 클래스 VS 객체  
    클래스를 설계도라 하면, 객체는 설계도로 구현한 모든 대상
    2. 객체 VS 인스턴스  
    클래스 타입으로 선언되었을땐? => **객체**  
    그 객체가 메모리에 할당되어 실제 사용될 때? => **인스턴스**
- 컨벤션:  
    1. 클래스 선언 시, 첫 글자는 **대문자**로 함
    2. 변수, 함수 선언 시, **카멜 표기법**으로 진행 
    3. 패키지 이름은 **소문자**로 함

- 함수 호출 시 stack memory 이용:  
   ![Image Alt 텍스트](/assets/images/2020-12-10_image1.PNG){: width="300" height="300"}

- 인스턴스와 heap memory:  
    힙 메모리란?:  
        프로그램에서 사용하는 동적 메모리 공간  
    ex. studentX = new student();  
    
   ![Image Alt 텍스트](/assets/images/2020-12-10_image2.PNG){: width="300" height="300"}  
   studentX변수는 스택 메모리에 저장되고,  
   student 클래스의 멤버변수들을 힙 메모리에 저장된다.  

## 후기
  자바 프로그래밍은 늘 완벽하게 학습하지 않아서 부족한 지식들이 많았었는데 이번 기회로 많이 늘려나가야겠다.  
  특히 클래스, 객체, 인스턴스 같은 용어들 및 기초 지식들을  
  다시 쌓아간다는 마인드로 진행하겠다.