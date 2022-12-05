# book: introduction to mathmatical statistics
- Hogg, McKean, Craig
- 수리통계학 개론
- http://www.kocw.net/home/cview.do?cid=7c789810ade43386: 부산대 김충락 교수님 강의
- crkim.pusan.ac.kr
    + lecture: lecture notes
    + KOCW:
        * 수리통계학 mathematical statistics(1, 2), 
        * 회귀분석 regression analysis(1, 2), 
        * 수리통계학 math.stat(3), 
        * 생존분석 survival analysis, 
    + KMOOC: R을 활용한 통계학 개론

## 1. Probability and Distributions

### 1.1 Introduction

- Statistical(random) experiment: the outcome cannot be predicted with certainty prior to the performance of the experiment.
- Sample space: collection of every possible outcome from the random experiment, and denoted by $\mathscr{C}$ .
- Event: subset of sample, and denoted by A, B, C.
- Example 1.1.1. Consider tossing a coin, then $\mathscr{C}$ = {H, T}.
- Example 1.1.2. Consider tossing two die (one red, the other white), then $\mathscr{C}$ = {(1,1), ··· , (1,6), (2,1), ··· , (6,6)}.
- Example 1.1.3. Let C denote an event of sum seven when tossing two die, then $\mathscr{C}$ = {(1,6), (2,5), ··· , (6,1)}.
- Remark 1.1.1. Two types of probability 
    + (i) Relative frequancy approach.
    + (ii) Personal or subjective approach.

![](./img/2022-08-03-02.jpg)

### 1.2 Set Theory

- Definition 1.2.1. If each element of set $C_1$ is also an element of set $C_2$, then $C_1$ is called subset of $C_2$, and denoted by $C_1 \subset C_2$ .
- Definition 1.2.2. If a set C has no elements, C is called the null(empty) set, and denoted by C = $\phi$ .
- Definition 1.2.3. The set of all elements that belong to at least one of $C_1$ and $C_2$ is called the union of $C_1$ and $C_2$, and denoted by $C_1 \cup C_2$ and it can be generalized to any number of sets. For example, $C_1 \cup C_2 \cup \cdots \cup C_n = \cup_{k=1}^{\infty}C_k$ .

![](./img/2022-08-03-03.jpg)

![](./img/2022-08-03-04.jpg)

![](./img/2022-08-04-02.jpg)

![](./img/2022-08-04-03.jpg)

![](./img/2022-08-05-02.jpg)

## 1.3 The Probability Set Funciton

#### 1.3.1 셈규칙

![](./img/2022-08-05-03.jpg)

![](./img/2022-08-05-04.jpg)

#### 1.3.2 확률의 추가적 특성

![](./img/2022-08-05-05.jpg)

![](./img/2022-08-08-17.jpg)

### 1.4 조건부 확률과 독립성

![](./img/2022-08-08-18.jpg)

![](./img/2022-08-09-17.jpg)

![](./img/2022-08-09-18.jpg)

![](./img/2022-08-09-19.jpg)

![](./img/2022-08-11-07.jpg)

![](./img/2022-08-12-03.jpg)

#### 1.4.1 독립성

![](./img/2022-08-13-00.jpg)

![](./img/2022-08-13-04.jpg)

![](./img/2022-08-13-05.jpg)

#### 1.4.2 시뮬레이션

![](./img/2022-08-13-06.jpg)

### 1.5 확률 변수

![](./img/2022-08-13-07.jpg)

![](./img/2022-08-13-08.jpg)

![](./img/2022-08-15-00.jpg)

![](./img/2022-08-15-01.jpg)

![](./img/2022-08-15-02.jpg)

![](./img/2022-08-15-03.jpg)

![](./img/2022-08-15-04.jpg)

![](./img/2022-08-15-05.jpg)

![](./img/2022-08-15-06.jpg)

![](./img/2022-08-15-07.jpg)

![](./img/2022-08-15-08.jpg)

### 1.6 이산형 확률 변수

![](./img/2022-08-15-09.jpg)

![](./img/2022-08-15-10.jpg)

![](./img/2022-08-15-11.jpg)

#### 1.6.1 변환

![](./img/2022-08-16-07.jpg)

![](./img/2022-08-16-08.jpg)

### 1.7 연속형 확률 변수

![](./img/2022-08-17-03.jpg)

![](./img/2022-08-22-14.jpg)

![](./img/2022-08-29-00.jpg)

#### 1.7.1 분위수

![](./img/2022-08-29-01.jpg)

![](./img/2022-08-29-02.jpg)

![](./img/2022-08-29-03.jpg)

#### 1.7.2 변환

![](./img/2022-08-30-21.jpg)