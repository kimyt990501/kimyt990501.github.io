---
title: "Spring공부 02 Spring웹개발 기초"
excerpt: "Spring웹개발 기초"

categories:
 - Spring
tags:
 - [Spring, Web, Backend, Github]

toc: true
toc_sticky: true

date: 2023-01-21
last_modified_at: 2023-01-21
---

# 1. 정적 컨텐츠

__서버에서 뭐 하는거 없이 파일을 웹브라우저에 그냥 내리는 것을 의미함__  

예: 전 포스트에서 말했던 Welcome page 처럼 `index.html` 파일을 웹브라우저에서 바로 표시하는 것.

## 1.1 정적 컨텐츠 동작 확인
`resources/static` 에 `hello-static.html` 파일을 작성해서 집어 넣는다. 코드는 아래와 같다.
```html
<!DOCTYPE HTML>
<html>
<head>
    <title>static content</title>
    <meta http-equiv="Content-Type" content="text/html"; charset="UTF-8" />
</head>
<body>
정적 컨텐츠입니다.
</body>
</html>
```
다음은 컴파일 후 `localhost:8080/hello-static.html`으로 접속하여 확인 한다.  
![image](https://user-images.githubusercontent.com/50610894/213844438-ee722fdc-d8b2-474a-9664-6289d5bf3204.png)
이러한 화면이 뜬다면 성공이다.  

대신 여기에는 코드 그대로 반환이 되기 때문에 어떠한 프로그래밍을 할 수는 없다.

## 1.2 정적컨텐츠 작동 원리 정리
1. 웹브라우저에서 `localhost:8080/hello-static.html`을 요청한다.
2. 내장 톰캣 서버가 이 요청을 받고 `hello-static.html`을 받았다는 메시지를 스프링에 넘긴다.
3. 스프링은 `hello-static`관련 컨트롤러가 있는지 찾는다. (컨트롤러가 우선순위를 가짐) 
4. 없다면 내부에서 `resources/static/hello-static.html` 을 찾아내서 웹브라우저로 반환해준다.

# 2. MVC 와 템플릿 엔진

__템플릿 엔진 : `html` 파일을 그냥 내려주는게 아니라 서버에서 프로그래밍해서 동적으로 바꿔서 내려주는 장치__
예: 전 포스트에서 말했던 Thymeleaf  

__MVC : Model View Controller 라고 해서 템플릿 엔진이 작동하기 위한 장치들__

_**현재 이 패턴으로 많이 개발함**_  
