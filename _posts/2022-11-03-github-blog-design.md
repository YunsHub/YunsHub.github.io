---
title: 깃허브 블로그 테마 적용
date: 2022-11-03 02:18:15 +0900
categories: [Github.io, Github Blog]
tags: [github.io, blog, jekyll, ruby] # TAG names should always be lowercase
---
>깃허브(Github) 블로그 테마 적용

![이미지](/assets/img/Github%20Blog/Github_Blog_1.jpg)

## 깃허브(Github) 블로그 테마 적용
---
깃허브 페이지를 성공적으로 생성하였으면 이번에는 블로그를 어떻게 꾸미는지 알아봅시다.
Github Blog는 Github Page, Jekyll, Ruby가 필수입니다.  
>Jekyll은 홈페이지를 자동으로 생성해줍니다.  
>Ruby는 프로그래밍 언어 명으로 Jekyll이 Ruby로 만들어져 있습니다.  

이 글에서는 [Jekyll-theme-chirpy](https://github.com/cotes2020/jekyll-theme-chirpy/)테마를 선택하여 진행하겠습니다.
- Jekyll테마
  - <http://jekyllthemes.org/>
  - <https://jekyllthemes.io/free>
  - <http://themes.jekyllrc.org/>
  - <https://github.com/topics/jekyll-theme>

## Jekyll, Ruby 설치
---
### **Ruby 설치**  
[Ruby](https://rubyinstaller.org/downloads/)에 접속하여 ```Ruby+Devkit(x64)```를 설치합니다. -> **윈도우 전용**  
별도의 수정없이 설치  
![이미지](/assets/img/Github%20Blog/Github_Blog_5.PNG)

Ruby 첫 실행화면에서 ```1 + enter``` ```2 + enter``` ```3 + enter```해서 설치  
![이미지](/assets/img/Github%20Blog/Github_Blog_6.jpg)

>루비 설치 확인 : ```ruby -v```  
>실행 결과 : "ruby 2.6.10p210 (2022-04-12 revision 67958) [x64-mingw32]"  

>인코딩 확인 : ```chcp 65001```  
>실행 결과 : "Active code page: 65001"  

### **Jekyll 설치**
**Ruby에서 자신의 repository를 설치한 경로로 이동한 후 (ex-C:\Users\82103\Desktop\YunsHub.github.io)**  
아래의 명령어를 차례대로 입력해줍니다.  
```gem install jekyll bundler```  
```gem install webrick```  
설치가 완료되면 ```jekyll new ./```을 실행하여 Jekyll을 생성합니다.  

**만약 오류가 뜬다면 repository 폴더 안에 있는 index.html을 삭제 후 실행합니다.**  

Jekyll생성이 완료되면 아래 명령어들을 실행하여 Jekyll서버를 동작시킵니다.  
```bundle install```  
```bundle exec jekyll serve```  
에러가 없이 정상적으로 실행되었다면 웹 주소창에 <http://127.0.0.1:4000/> 또는 <http://localhost:4000/>으로 접속하면 ```index.html``` 내용이 홈페이지에 보입니다.

### **Jekyll 테마 적용**  
위에서 테마를 선택했다면 테마에서 "Download" 또는 "Github"링크로 이동하여 해당 Repository 소스를 다운로드 합니다.  
chirpy 테마의 경우 [Jekyll-theme-chirpy](https://github.com/cotes2020/jekyll-theme-chirpy/)로 이동하여 소스파일을 다운 후 압축을 풀고 자신의 repository에 모든 내용을 덮어쓰기를 합니다.  
![이미지](/assets/img/Github%20Blog/Github_Blog_7.jpg)
![이미지](/assets/img/Github%20Blog/Github_Blog_8.jpg)

다시 아래의 명령어를 차례대로 입력해줍니다.  
```bundle install```  
```bundle exec jekyll serve```  
웹 주소창에 <http://127.0.0.1:4000/> 또는 <http://localhost:4000/>으로 접속하면 다운로드 받은 테마의 Demo화면과 동일하게 보입니다.  
이제 이 내용들을 commit->push를 해주시면 "```username```.github.io"에도 적용된 것을 확인하실 수 있습니다.  
![이미지](/assets/img/Github%20Blog/Github_Blog_9.jpg)