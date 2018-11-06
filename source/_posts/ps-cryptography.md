---
sitemap-priority: 1
sitemap-changefreq: daily
layout: post
date: '2018-11-05 22:00 +0900'
published: true
comments: true
insearch: true
title: 탑코더 알고리즘 정복 - 3. 암호
published_on: '2018-11-05'
categories:
  - Algorithm
  - Top Coder
tags:
  - Algorithm
  - 전체 탐색
  - Python
---

## 문제
TopCoder Security Agency(TSA, 오늘 설립되었어요!)는 새로운 암호화 시스템을 개발했습니다.  
이 시스템은 암호화하려고 숫자 리스트를 입력받습니다.

여러분은 TSA의 비밀 정보 수사원입니다. 암호화 과정에서 중요한 부분을 구현하는 것이 여러분의 일입니다.  
여러분은 입력 리스트에서 1개의 값을 선택하고 값을 1 증가시킵니다. 이때 리스트 내부의 모든 숫자 곱이  
가장 커져야 합니다.

int[] numbers 형태로 숫자 배열이 주어질 때 곱의 최댓값을 리턴하세요. 리턴값이 $2^62$를 넘는 문제는 나오지 않을 것을 보장합니다.

## 정의
```py
class Cryptography:
	def encrypt(self, numbers):
```

## 입력
first : 1~50개의 요소가 있는 배열.
second : 1~50개의 요소가 있는 배열.
first, second 공통 : 각 요소는 1~15개 문자이며, 각 문자는 영어 소문자입니다.
i번째 요소 first[i]와 second[i]의 내용은 다릅니다.


## 출력
정수를 담고있는 변수

## IO Example
```py
# Case# 0
```

## 구현

### 1차 코드

## 마무리
- **마무리1**
