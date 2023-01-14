---
title: "Spring공부 01 Spring입문 개발환경 세팅"
excerpt: "Spring 개발환경 세팅"

categories:
 - Spring
tags:
 - [Spring, Web, Backend, Github]

toc: true
toc_sticky: true

date: 2023-01-14
last_modified_at: 2023-01-14
---

# 스프링 개발 환경 세팅

스프링 개발 환경은 보통 자바를 이용하기 때문에 이클립스 아니면 인텔리제이를 쓴다.  

본인은 자바 공부 시에도 인텔리제이를 썼기 때문에 인텔리제이를 쓸 예정이다.  

start.spring.io 사이트에 접속해서 스프링 부트 기반 프로젝트를 만들어 압축파일을 받고 압축을 풀어준다.    

다음으론 인텔리제이에서 해당 폴더를 열어준다.  

HelloSpringApplication.java 를 실행시키면  

![image](https://user-images.githubusercontent.com/50610894/212460124-b245c21d-16fb-4016-9a61-175100fd266a.png)  

이런 화면이 뜨는데  
이제 웹 브라우저에서 localhost:8080 을 접속했을때 

![image](https://user-images.githubusercontent.com/50610894/212460166-cd986db9-4529-4dbe-94c3-32b64f1363a3.png)  
이러한 오류 화면이 뜬다면 성공이다.

```java
여기서 오류 화면 뜨는 것이 성공인 이유는 
아직 아무것도 작성한것이 없기 때문에  
오류 화면이 뜨는것이 당연한 것이라고 한다. 
```

따라서 여기까지 하면 스프링 개발 환경설정이 끝난다.

_**처음엔 인텔리제이로 스프링 프로젝트를 열었을 때 오류가 나서 당황했지만**_  
_**구글링을 통해서 임시방편 느낌으로 해결했으므로**_  
_**제발 추후 같은 오류가 생기지 않았으면 좋겠다..**_