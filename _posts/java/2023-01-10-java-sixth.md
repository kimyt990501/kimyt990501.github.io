---
title: "JAVA공부 05 <Java의 정석> ch.06 객체지향 프로그래밍 2"
excerpt: "JAVA 객체지향 프로그래밍 2"

categories:
 - Java
tags:
 - [Java, Github]

toc: true
toc_sticky: true

date: 2023-01-10
last_modified_at: 2023-01-10
---

# 3. 변수와 메서드

## 3.1 선언위치에 따른 변수의 종류
|변수의 종류    |선언위치       |생성시기       |
|:----------:|:-----------:|:------------|
|클래스 변수    |클래스 영역    |클래스가 메모리로 올라갈 때|
|인스턴스 변수  ||인스턴스가 생성되었을 때|
|지역변수       |클래스 영역 이외의 영역|변수 선언문이 수행되었을 때|

## 3.2 클래스 변수와 인스턴스 변수
__객체의 속성 중에 개별적인것은 인스턴스 변수, 공통적으로 유지되어야하는 것은 클래스 변수.__
_iv = instance variable
cv = class variable_
예:
```java
class Card {
    String kind; // 무늬 iv
    int number; // 숫자 iv

    static int width = 120; // 폭 cv
    static int height = 250; // 높이 cv
}

class CardTest {
    public static void main(String args[]) {
        //객체 생성
        Card c = new Card();

        //객체 사용
        c.kind = "HEART"; //iv인 경우는 앞에 객체 이름을 쓴다
        c.number = 5;

        Card.width = 200; //cv인 경우는 앞에 클래스 이름을 쓴다
        Card.height = 300;
    }
}
```
_**인스턴스 변수는 개별적으로 객체마다 만들어지지만 클래스 변수는 다른 공간에 하나만 만들어진다**_

## 3.3 메서드란 ?
__문장들을 묶어놓은 것__


# 4. 클래스 작성하기
__1. 클래스이름과 파일명은 일치해야한다.
2. 파일 안에 클래스가 하나 이상이라면 public 클래스명과 일치시킨다.
3. public 클래스가 없다면 어느 클래스 이름이든 가능하다.
4. 하나의 소스파일에는 public 클래스가 한 개만 있어야 한다. 
5.대소문자를 잘 입력해야 한다.__
