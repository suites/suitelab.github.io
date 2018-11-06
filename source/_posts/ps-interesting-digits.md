---
sitemap-priority: 1
sitemap-changefreq: daily
layout: post
date: '2018-11-06 22:00 +0900'
published: true
comments: true
insearch: true
title: 탑코더 알고리즘 정복 - 4. 재미있는 수학
published_on: '2018-11-06'
categories:
  - Algorithm
  - Top Coder
tags:
  - Algorithm
  - 전체 탐색
  - Python
---

## 문제
숫자 3과 9는 재미있는 성질이 있습니다. 3의 배수의 각 자릿수의 합은 다른 3의 배수가 됩니다.  
예를 들어 $118x3=358$이고 $3+5+4=12$는 3의 배수입니다. 마찬가지로 9의 배수의 각 자릿수의 합은  
다른 9의 배수가 됩니다. 예를 들어 $75x9=675$이고 $6+7+5=18$은 9의 배수입니다.
base 진법이 주어졌을 때 이러한 성질을 가진 수를 오름차순으로 모두 리턴하세요(0과 1은 제외)  
어떤 수가 이러한 성질을 가지는지 알고자 모든 숫자의 곱을 고려할 필요는 없습니다.  
만약 4자리 미만의 곱으로 성립되면 더 큰 자리에서도 성립된다 할 수 있습니다. 예를 들어 10진수 에서는  
999보다 큰 숫자를 고려하지 않아도 됩니다.

## 정의
```py
class InterestingDigits:
	def digits(self, base):
```

## 입력
base : 3~30의 정수

## 출력
정수를 담고있는 배열

## IO Example
```py
# Case# 0
base = 10
returns = [3, 9]

# Case# 1
base = 3
returns = [2]

# Case# 2
base = 9
returns = [2, 4, 8]

# Case# 3
base = 26
returns = [5, 25]

# Case# 4
base = 30
returns = [29]
```

## 구현

### 1차 코드
```py
class InterestingDigits:
    def digits(self, base):
        ans = []

        for n in range(2, base):
            ok = True
            for k1 in range(base):
                for k2 in range(base):
                    for k3 in range(base):
                        if (k1 + k2 * base + k3 * base * base) % n == 0 and (k1 + k2 + k3) % n != 0:
                            # n의 배수 숫자로 각 숫자의 합이 n의 배수가 아니면
                            # n을 제외합니다.
                            ok = False
                            break
                    if not ok:
                        break
                if not ok:
                    break
            if ok:
                ans.append(n)

        return ans
```
### 2차 코드
```py

```

## 마무리
- **마무리1**
