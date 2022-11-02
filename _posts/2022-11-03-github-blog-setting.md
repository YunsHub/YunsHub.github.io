---
title: 깃허브 블로그 기본 설정
pin: true
date: 2022-11-03 02:18:11 +0900
categories: [Github.io, Github Blog]
tags: [github.io, blog, jekyll, ruby] # TAG names should always be lowercase
---
>깃허브(Github) 블로그 설정

## 깃허브(Github) 블로그 설정
---
깃허브 페이지 테마를 적용하였으면 기본 설정 몇가지를 추가로 해주겠습니다.  

### **_config.yml 파일 확인**  
자신의 local repository를 확인하면 ```_config.yml```파일이 있습니다.  
해당 파일 설정은 테마 별로 다르기 때문에 설정하는 법은 제작자의```README.md```을 참고해야 합니다.  
여기서는 jekyll-theme-chirpy테마 기준으로 설명드리겠습니다.
```yml
# 테마 이름 
theme: jekyll-theme-chirpy

# 사용자 페이지를 만들었을 경우 빈 칸, 프로젝트 페이지를 만들 경우 프로젝트 명 적기
baseurl: ""

# 사용하는 언어 설정 (한국어 : #ko-KR)
lang: en 

# 타임존 설정
timezone: Asia/Seoul

# 블로그 이름 (첫 페이지 좌측 확인 가능)
title: YunsHub 

# 서브 타이틀 (첫 페이지 좌측 확인 가능)
tagline: Android Developer 

description: >- # 별도 설정 X
  A minimal, responsive, and powerful Jekyll theme for presenting professional writing.

# 'https://username.github.io'과 같이 설정
url: "https://yunshub.github.io/"

github:
  username: YunsHub # 본인의 github username

#twitter:
#username: twitter_username            # twitter username 없으면 주석

social:
  # social 관련 내용으로 이름, 이메일, 링크 등 작성 안쓰면 주석
  # Change to your full name.
  name: YunsHub
  email: wkdrns3918@gmail.com # change to your email address
  links:
    # The first element serves as the copyright owner's link
    #- https://twitter.com/username      # change to your twitter homepage
    - https://github.com/YunsHub # change to your github homepage
    # Uncomment below to add more social links
    # - https://www.facebook.com/username
    # - https://www.linkedin.com/in/username

google_site_verification: # googole search console 관련 내용

# ↑ --------------------------
# The end of `jekyll-seo-tag` settings

google_analytics:
  id: "" # Google Analytics 관련 내용
  # Google Analytics pageviews report settings
  pv:
    proxy_endpoint: # fill in the Google Analytics superProxy endpoint of Google App Engine
    cache_path: # the local PV cache data, friendly to visitors from GFW region

# Prefer color scheme setting.
#
# Note: Keep empty will follow the system prefer color by default,
# and there will be a toggle to switch the theme between dark and light
# on the bottom left of the sidebar.
#
# Available options:
#
#     light  - Use the light color scheme
#     dark   - Use the dark color scheme
#

# chirpy는 light|dark 테마 지원
theme_mode: # [light|dark]

# The CDN endpoint for images.
# Notice that once it is assigned, the CDN url
# will be added to all image (site avatar & posts' images) paths starting with '/'
#
# e.g. 'https://cdn.com'
img_cdn: #"https://raw.githubusercontent.com/cotes2020/chirpy-images/main"

# 프로필 이미지
avatar: "/assets/img/profile.jpg"

# toc 사용 여부
toc: true

# 댓글 사용 여부
comments:
  active: # The global switch for posts comments, e.g., 'disqus'.  Keep it empty means disable
  # The active options are as follows:
  disqus:
    shortname: # fill with the Disqus shortname. › https://help.disqus.com/en/articles/1717111-what-s-a-shortname
  # utterances settings › https://utteranc.es/
  utterances:
    repo: # <gh-username>/<repo>
    issue_term: # < url | pathname | title | ...>
  # Giscus options › https://giscus.app
  giscus:
    repo: # <gh-username>/<repo>
    repo_id:
    category:
    category_id:
    mapping: # optional, default to 'pathname'
    input_position: # optional, default to 'bottom'
    lang: # optional, default to the value of `site.lang`
    reactions_enabled: # optional, default to the value of `1`

# -------- 아래는 별도 수정 생략 --------

```

### **파일 삭제 및 추가작업**
1. ```.travis.yml```파일 삭제
2. ```_post```안의 파일 모두 삭제 -> 게시물 업로드 하는 폴더 (포스팅 참고 후 삭제)
3. ```.github```폴더 안에서 ```workflows```폴더를 제외한 모든 폴더 및 파일 삭제
4. ```docs``` 폴더 삭제 -> 없으면 무시
5. ```.github > workflows```폴더에서 ```ci.yml```파일, ```pr-interceptor.yml```파일 삭제
6. ```.github > workflows > pages-deploy.yml.hook```파일에서 ```.hook```을 지우고 ```pages-deploy.yml.hook```파일로 변환 후 상단 branches를 자신의 Repository default branch로 변경 (대부분 ```main```)