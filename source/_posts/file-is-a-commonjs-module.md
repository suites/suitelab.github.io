---
sitemap-priority: 1
sitemap-changefreq: daily
layout: post
date: '2018-12-04 19:00 +0900'
published: true
comments: true
insearch: true
title: vs code에서 File is a CommonJS module; 메시지 발생할 때.
published_on: '2018-12-04'
categories:
  - Web
  - Node.js
tags:
  - Node.js
  - editor
  - vs code
---

오늘은 미세먼지급 팁을 가져왔다. vs code로 node.js 개발을 하고있는데  
`[js] File is a CommonJS module; it may be converted to an ES6 module.` 라는 메시지가 나를 꽤나 성가시게 하였다.

`const http = require('http');` require등을 사용할 때 발생하고 덕분에 require가 자동완성도 되지않는다.

<div align="middle">
    <img src="/images/20181204/message.png" width="400px">
</div>

## 해결방법

> File > Preferences > Settings

또는
> Ctrl + ,

입력 후 아래 사진과 같이 `suggestion Actions`을 검색하고  
`Javascript > Suggestion Actions: Enabled` 의 체크를 해제한다.

<div align="middle">
    <img src="/images/20181204/message1.png" width="400px">
</div>

이후 더이상의 경고는 발생하지 않았다!

<div align="middle">
    <img src="/images/20181204/message2.png" width="400px">
</div>

필자의 경우에는 성가심 해결이 먼저여서 우선 조치를 취했지만, 이 메세지에 관해서 자세히 알고 싶은 사람은 다음 vscode의 Issue를 들여다 보면 도움이 될 것 같다.  

[[js] File is a CommonJS module; it may be converted to an ES6 module. #47299](https://github.com/Microsoft/vscode/issues/47299)

# 🛴
