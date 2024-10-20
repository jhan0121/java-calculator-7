# 프리코스 1주차 미션 - 문자열 덧셈 계산기

***
<div align="center">
  <img src="./img/logo.webp" alt="우아한테크코스">
</div>

***

![Static badge](https://img.shields.io/badge/precourse-week1-14CC80.svg)
![Static badge](https://img.shields.io/badge/test-0_passed-1E96EB.svg)


> 우아한테크코스 7기 1주차 프리코스 미션을 구현한 프로젝트

***

# 목차

- [시작](#시작)
- [기능 목록](#기능-목록)
    - [입력 기능](#입력-기능)
    - [구분자 판정 기능](#구분자-판정-기능)
    - [문자열 분리 기능](#문자열-분리-기능)
    - [덧셈 연산 기능](#덧셈-연산-기능)
    - [출력 기능](#출력-기능)
- [제약 조건](#제약-조건)

***

## 시작

1. repository를 clone한 뒤, IDE에서 open하여 Application.java 파일을 실행한다.

```git
    git clone https://github.com/jhan0121/java-calculator-7.git
```

## 기능 목록

***

구현해야 할 기능들을 정리한다.

### 입력 기능

+ 문자열 덧셈 대상 문자열을 입력받아야 한다.
+ 입력을 받기 전에 `덧셈할 문자열을 입력해 주세요.`를 먼저 출력한 뒤, 개행하여 입력을 받아야 한다.
+ 사용자가 입력하는 값의 처리는 `camp.nextstep.edu.missionutils.Console`의 `readLine()`을 활용한다.
+ 사용자가 프로그램에서 요구하는 사항이 아닌, 잘못된 값을 입력할 경우 `IllegalArgumentException`을 발생시킨 후 애플리케이션은 종료되어야 한다.

### 구분자 판정 기능

+ 기본 구분자(콤마, 세미콜론)외에 커스컴 구분자(`"//"`와 `"\n"` 사이에 위치하는 문자)의 사용 여부를 확인해야 한다.
+ 구분자 문자열을 return 한다.

### 문자열 분리 기능

+ 구분자를 이용하여 입력받은 문자열에서 숫자를 분리한다.
+ 정수 또는 실수를 요소로 가지는 List를 return한다.

### 자료형 판정 기능

+ 일관된 연산을 진행하기 위해 자료형을 판정한다.
+ 정수 또는 실수 여부를 판정하여 자료형에 맞는 요소를 제공한다.

### 덧셈 연산 기능

+ input은 정수 또는 실수를 요소로 가지는 List로 한정한다.
+ List의 요소를 모두 더한 값을 return 한다.

### 출력 기능

+ 덧셈 연산 기능에서 return한 값을 출력한다.
+ 출력 형태는 `결과 : <덧셈 연산 기능 return 값>`로 해야 한다.

### 종합 실행 기능

+ 위에서 구성한 기능들을 종합하여 실행한다.

***

## 제약 조건

구현할 때 모호하거나 유의해야 할 사항을 어떻게 처리할지 정의한다.

+ 숫자의 범위는 java에서 처리할 수 있는 양수의 최대 범위로 설정한다.   
  (숫자의 범위를 가장 넓게 지원하는 java의 자료형 또는 기본 라이브러리를 사용한다.)
+ "잘못된 값"은 아래의 형태 중 하나 이상 만족할 경우로 정의한다.
    * 판정된 구분자 또는 숫자가 아닌 다른 문자가 존재하는 경우 **(ex: `"//!\n1!2/3!4"`, `"1;2;3;a"`)**
    * 커스텀 구분자를 판정하는 문자의 형태가 잘못된 경우 **(ex: `"/?\b1?2?3?4"`)**
    * 빈 문자열일 경우
+ 결과 출력에 성공하였을 때, 애플리케이션은 종료되도록 한다.