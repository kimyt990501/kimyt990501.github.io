---
title: "JAVA공부 03 <Java의 정석> ch.05 배열(array)"
excerpt: "JAVA 배열"

categories:
 - Java
tags:
 - [Blog, jekyll, Github, Git]

toc: true
toc_sticky: true

date: 2023-01-08
last_modified_at: 2023-01-08
---

# 1. 배열

__"배열은 같은 타입의 여러 변수를 하나의 묶음으로 다루는 것"__

## 1.1 배열의 선언과 생성

```java
타입[] 변수이름;            // 배열을 선언
변수이름 = new 타입[길이];   // 배열을 생성
```
예:
```java
int[] score;
score = new int[5];
```

```java
int[] score = new int[5];
```

_해당 부분은 C, C++ 문법과 조금 다르다._

## 1.2 배열의 복사

배열 num 의 요소를 배열 newNum 으로 복사

```java
for(int i = 0; i < num.length; i++) {
    newNum[i] = num[i];
}
```
보통은 위와 같이 하지만 arraycopy를 쓰면 더 간단하다.

```java
System.arraycopy(num, 0, newNum, 0, num.length);
//num[0]에서 newNum[0]으로 num.length개의 데이터를 복사
```