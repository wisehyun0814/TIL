# MardDown - TOC기능 만들기 (Table Of Contents)

깃허브에 올라온 md파일을 읽다보면 목차가 생성되어있는 것을 볼수가 있다. 이걸 자동으로 만들어주는 라이브러리가 있지만.. 
보통은 그냥 작성한다. 그렇게 어렵지않다.


## 띄어쓰기 없는 타이틀을 사용할 때
일단 우리가 보통 마크다운문서를 작성할 때는 `#`의 갯수에 따라 타이틀1, 타이틀2, 타이틀3 을 구분하여 사용할 수 있다.
이게 타이틀 역할도 하지만 이게 앵커 역할도 한다. 

아래를 보면 ### 섹션 이라고 작성되어있는 부분이 있다. 이걸 상단에서 `[섹션1](#섹션1)`의 형태로 불러올 수가 있다. 
`[]()`이건 하이퍼링크를 달때 사용하는 표현인데 오른쪽엔 링크 왼쪽엔 보여질 텍스트가 들어가는 것이다. 이때 오른쪽 링크의 값을 가지고 앵커를 찾아간다.  
```
## 목차

- [섹션1](#섹션1)
- [섹션2](#섹션2)

### 섹션1

이곳은 섹션1입니다.

### 섹션2

이곳은 섹션2입니다.
```
위 부분 처럼 타이틀이  띄어쓰기도없이 나타나는 경우는 위와 동일하게 앵커를 따로 만들필요가 없다. ### 섹션1 자체가 앵커역할을 할 수 있기 때문이다.  


## 띄어쓰기 있는 타이틀을 사용할 때


하지만 아래 처럼 띄어쓰기가 있는 경우는 달라진다. 
타이틀이 ## Section 1 에는 띄어쓰기가 있다. 이 앵커를 찾아가려면 위에있는 URL에 공백에 `-`를 표시해준다. 

```
## Table of Contents

- [Section 1](#section-1)
  - [Subsection 1.1](#subsection-1-1)
  - [Subsection 1.2](#subsection-1-2)
- [Section 2](#section-2)
  - [Subsection 2.1](#subsection-2-1)
  - [Subsection 2.2](#subsection-2-2)

## Section 1

### Subsection 1.1

### Subsection 1.2

## Section 2

### Subsection 2.1

### Subsection 2.2
```

## 주의할 점
링크가 들어가는 부분에는 띄어쓰기가 들어갈 수 없다. 또한 인덱스의 `[]()`에서 []안에는 `:`도 들어가서는 안된다. 
그럴경우 인덱스를 눌렀을 때 해당 부분으로 이동을 할 수가 없다. 



## 예시

**Index**
- [클로저란](#클로저란)
    - [표현식](#표현식)
    - [사용하기](#사용하기)
    - [1급객체](#1급객체)
    - [실행하기](#실행하기)
- [후행 클로저 - Trailing Closure](#후행-클로저---Trailing-Closure)
- [경량화 문법 - Lightweight Closure Syntax](#경량화-문법---lightweight-closure-syntax)
- [iOS에서 흔하게 사용하는 클로저](#iOS에서흔하게-사용하는-클로저)
    - [탈출 클로저 - Escaping Closure](#탈출-클로저---Escaping-Closure)
    - [오토 클로저 - Auto Closure](#오토-클로저---Auto-Closure)

## 클로저란
123
### 표현식
123
## 사용하기
123
### 함수의 사용법
123
## 1급객체
123
## 실행하기
123

## [경량화 문법 - Lightweight Closure Syntax](#경량화-문법---lightweight-closure-syntax)
123
## [오토 클로저 - Auto Closure](#오토-클로저---Auto-Closure)
123
## [iOS에서 흔하게 사용하는 클로저](#iOS에서-흔하게-사용하는-클로저)
123