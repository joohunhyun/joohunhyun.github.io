---
layout: post
title: (KOR) 연구실 안전교육 배속하는 방법
date: 2024-12-15
description: 
tags: tools
categories: study
featured: false
---

202412월 기준, 해당 방법이 가장 편하다. 다른 방법들은 모두 막혔다. 중간에 "깜짝 퀴즈"도 있으니 유의해야한다.

**크롬**에서 연구실 안전교육 동영상 재생 후 개발자모드 콘솔 `F12`에 해당 코드 붙여넣기:

```
document.querySelector('video').playbackRate = 15;
```

