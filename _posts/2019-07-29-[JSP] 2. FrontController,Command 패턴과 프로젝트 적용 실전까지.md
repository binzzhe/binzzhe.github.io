---
title: "[JSP] 2. FrontController,Command 패턴과 프로젝트 적용 실전까지 "
date: 2019-07-30 12:49:39 -0400
categories: JSP
---


2019-07-29-[JSP] 2. FrontController,Command 패턴과 프로젝트 적용 실전까지.md


# [JSP] FrontController/Command 패턴과 프로젝트 적용까지

## FrontController 패턴이란?
쉽게 말해서 클라이언트의 다양한 요청을 한 곳으로 집중시켜, 개발 및 유지보수에 효율성을 극대화하는 구조이다.

즉, 요청 a,b,c에 각각의 요청 'a서블릿, b서블릿 ,c서블릿'을 두는 것이 아닌 ** '모든 요청을 처리하는 통합 서블릿' **하나를 두는 구조이다.

하지만, Front Controller에서 모든 요청에 대한 처리를 하면, 소스가 길어지고 유지보수 관리에 힘이 든다. 이에 대한 대처가 다시 다른 Servelet으로 보내서 분산해서 관리해준다. 이것이 Command 패턴이다.


## Command 패턴이란
클라이언트로부터 받은 요청들에 대해, 서블릿이 작업을 직접 처리하지 않고, 해당 클래스가 처리하도록 하는 것이다.
