---
layout: post
title: (KOR) 연구실 안전교육 배속하는 방법
date: 2024-12-16
description: 
tags: tools
categories: study
featured: false
---

24'12월 기준, 이 방법이 제일 편한 듯. 다른 방법들은 다 막힌 듯 하다.

참고 :
- 중간중간에 퀴즈도 있으니 유의해야한다.
- 배속은 16배까지만 가능하다.
 
**크롬** 환경에서 연구실 안전교육 동영상 재생 후 개발자모드 콘솔 `F12`에 해당 코드 붙여넣기:

```
document.querySelector('video').playbackRate = 16;
```

