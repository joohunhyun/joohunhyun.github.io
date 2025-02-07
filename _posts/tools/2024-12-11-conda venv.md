---
layout: distill
title: (KOR) 아나콘다 venv 설정
date: 2024-12-7
description:
tags: tools
categories: study
featured: false
---

## 1. 가상환경 관련

가상환경 만들기
```
conda create -n venv이름 python=3.8.11
conda create -n venv이름 python=3.11
```

가상환경 활성화
```
conda activate venv이름
```

가상환경 비활성화
```
conda deactivate venv이름
```

가상환경 리스트 조회
```
conda env list
```

가상환경 삭제
```
conda env remove -n venv이름
```

파이썬 버전 변경
```
conda install python=3.11
```

파이썬 버전 확인
```
python --version
```

<br>

## 2. 디버깅 관련

### 2.1 ModuleNotFound Error

가끔 pip이나 conda를 사용하여 패키지를 설치했음에도 불구하고 'Module not found' 오류가 발생하는 경우가 있다. 이 경우, PATH 설정에 문제가 있을 확률이 높다. 가상환경의 PATH를 올바르게 설정하면 이 문제를 해결할 수 있다.

현재 PATH 확인하는 방법 (만약 가상환경이 아닌 기본 PATH 설정이 나타난다면, 아래 명령어를 실행한다)
```
which python
```

PATH 설정 (여기서 $PATH에는 가상환경의 실제 경로를 입력해야 한다)
```
export PATH=~/anaconda3/bin:$PATH
```