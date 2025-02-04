---
layout: distill
title: (KOR) Github al-folio 설치부터 블로그 테마 변경까지
date: 2024-2-4
description: 
tags: tools
categories: study
featured: false
toc:  
  sidebar: left
---

## 서론

테크 블로그를 운영하기 위한 사람들에게

순서대로 작성해뒀으면,


## 설치 방법

1. [Al-Folio Github Page](https://github.com/alshedivat/al-folio)에서 forking을 통해 레포를 복제한다. 
   - **중요!** 사이트 URL을 `<your-github-username>.github.io`형식으로 배포하려면 레포 이름을 URL과 동일하게 설정해야 한다.
   - 편의상 <your-github-username>.github.io로 레포 이름을 설정하는 것을 권장한다.
  
2. GitHub Actions 설정 변경  
   - 레포에서 `Settings -> Actions -> General`로 이동해 `Workflow permissions`을 `Read and write`로 변경한다.  

3. `_config.yml` 파일 수정  
   - `_config.yml` 파일에서 `url`을 `https://<your-github-username>.github.io`로 설정한다.
   - `baseurl`은 비워두되 삭제하지 않는다.  

4. **GitHub Pages 배포 설정**  
   - `Actions` 탭에서 `Deploy site` 작업이 완료될 때까지 기다린다 (~4분 소요).  
   - `Settings -> Pages -> Build and deployment`에서 `Source`를 `Deploy from a branch`로 설정하고 `gh-pages`를 선택한다.  
   - `pages-build-deployment` 작업이 완료될 때까지 기다린다 (~45초 소요).  

5. **사이트 확인 및 로컬 복사**  
   - 브라우저에서 `https://<your-github-username>.github.io`에 접속하여 정상 작동하는지 확인한다.  
   - 이후 레포를 로컬에 클론하여 커스터마이징을 시작한다.

```sh
   git clone git@github.com:<your-username>/<your-repo-name>.git
```

## navbar 페이지 제거

필자는 웹사이트에서 렌더링하고 싶지 않은 페이지들은 `root/_pages`에 해당하는 마크다운 페이지를 삭제하거나, 추후 사용 가능성이 있다면 별도로 저장해두는 것을 권장한다. 현재 필자는 학부생으로서 about, blog, cv, project 네비게이션 bar 항목만 남겨두었다.



## 블로그 관련

### 블로그 포스팅 방법

블로그 글은 `root/_posts`에 .md 형식으로 추가하면 된다. 파일명 형식은 다음과 같고, 날짜 정보 뒤에 오는 블로그 제목이 블로그 URL로 사용된다. 만약 블로그의 노출을 고려한다면, 해당 부분을 성의있게 작성해야 한다.

```
YEAR-MM-DD-블로그 제목(공백과 한국어를 지원한다)
```

### 블로그 지원 언어

al-folio는 기본적으로 마크다운을 지원하며, mermaid diagram, tex 문법, 등도 지원한다. 템플릿이 지원하는 형식과 관련해서 더 알고 싶다면 다음 링크를 참고하길 바랍니다. -> [distill-style 블로그](https://github.com/alshedivat/al-folio/blob/main/_posts/2018-12-22-distill.md?plain=1).

### 마크다운 문법
마크다운 문법은 다음 포스트를 참고 -> [마크다운 문법 총정리](https://joohunhyun.github.io/blog/2024/markdown-syntax/)

### 코드 관련

마크다운 코드 태그로 코드를 감싸게 되면, 코드 블럭 우측에 마우스를 올려두면 복붙도 가능해지고 코드 하이라이팅도 언어에 따라서 자동으로 해줘서 매우 편리하다.

````markdown
```python
여기에 코드를 작성하시면 됩니다.
```
````
이런 식으로 렌더링이 된다.
```python
def get_arxiv_abstract(arxiv_id):
    """
    arxvix.org에서 arxiv_id에 해당하는 논문의 초록을 가져오는 함수
    """
    url = f"http://export.arxiv.org/api/query?id_list={arxiv_id}"
    response = requests.get(url)
    if response.status_code == 200:
        root = ET.fromstring(response.text)
        ns = {'arxiv': 'http://www.w3.org/2005/Atom'}
        abstract = root.find(".//arxiv:summary", ns).text
        return abstract.strip()
    else:
        return fallback_extraction(url)
```

## CV 관련

필자는 al-folio 기본 CV 페이지의 수정 과정이 다소 번거롭다고 느껴질 수 있다고 생각한다. CV 페이지의 각 항목을 LaTeX가 아닌 Markdown으로 수정해야 하는 점과 블로그용 CV와 업무용 CV를 따로 관리해야 하는 불편함이 있다. 이러한 이유로 필자는 PDF 형식의 CV를 화면 전체에 렌더링하도록 CV페이지를 수정하였다.

**PDF형식의 CV만 렌더링하는 방법**

`root/_pages/cv.md`에서 상단의 tag 정보를 제외한 나머지 부분을 주석처리한다.

```
---
layout: cv
permalink: /cv/
title: cv
nav: true
nav_order: 3
cv_pdf:
---
<!-- ---
코드 주석 처리
--- -->
```
`root/assets/pdf` 디렉토리에 나의 CV를 추가한다.

`root/_layouts/cv.liquid`에서도 상단의 tag 정보를 제외한 나머지 부분을 주석처리하고, 다음 코드를 입력한다. 이때, `MY_CV.pdf` 부분은 이전 단계에서 추가한 PDF 형식의 CV 파일 이름과 일치해야 한다. 이를 통해 CV 페이지가 올바르게 렌더링될 수 있도록 할 수 있다.


```
---
layout: default
---
<div class="post">

<object data="../assets/pdf/MY_CV.pdf#pagemode=none" width="750" height="1000" type='application/pdf'></object>

</div>
```
