---
title: 깃허브 블로그 만들기
date: 2022-11-03 01:18:11 +0900
categories: [Github.io, Github Blog]
tags: [github blog, blog] # TAG names should always be lowercase
---
>깃허브(Github) 블로그 만들기

## 깃허브(Github) 블로그란?
---
분산 버전 관리 툴인 깃허브(Github)에서 ```Github Pages```서비스를 이용하여 자신의 깃허브 저장소에 블로그를 생성할 수 있습니다.  
```Github page```는 ```Jekyll```과 같은 정적 웹사이트 생성기와 결합하여 ```HTML```, ```Markdown``` 등의 언어들로 사용자가 편리하게 웹을 만들 수 있는 기능들을 제공합니다.
>요약하면 깃허브 블로그는 깃허브에서 제공하는 웹 호스팅 서비스로 자신만의 블로그를 운영할 수 있는 서비스입니다.

## 깃허브 블로그 장단점
---
### **깃허브 블로그 장점**
- Github와 호환이 된다.
- 이용료가 무료이며 계정 용량에 제한이 없다.
- 트래픽과 사용량에 크게 신경쓰지 않아도 된다.
- 높은 자유도로 직접 블로그 페이지를 설계하고 개발할 수 있다.

### **깃허브 블로그 단점**
- 초반 진입장벽이 높다.
- 자유도가 높은 만큼 코드를 활용할 줄 알아야 자신이 원하는 페이지를 만들 수 있다.
- 글을 작성할 때 ```Markdown```언어를 사용해야 한다.
- 웹소스가 모두 공개되어 자신의 블로그 페이지 소스가 공개된다.

## 깃허브 블로그 생성
---
Github Blog를 만들기 전에 Github계정이 필요합니다.  
계정이 없으신 분들은 [Github](https://github.com/)로 접속하여 계정을 먼저 생성하고 진행합니다.
### **Github Page 생성**
계정을 생성하였으면 본인의 Github계정으로 접속 후 Repositoris로 이동 후 new 버튼을 클릭하여 새로운 repository를 생성합니다.  
![이미지](/assets/img/Github%20Blog/Github_Blog_1.jpg)

Owner는 변경하지 않고 Repository name은 "```username```.github.io"로 입력합니다.  
그 후, ```public```으로 설정하고 ```Add a README file```만 체크하고 repository를 생성합니다.  
![이미지](/assets/img/Github%20Blog/Github_Blog_2.jpg)

생성한 repository에서 Settings > Pages로 가시면 자신의 Github Pages가 보일겁니다.    
이제 ```https://username.github.io/```가 자신의 깃허브 블로그 주소가 됩니다.  

**만약 위와 같은 주소 형식이 아니라면 생성할 때 repository와 사용자 이름이 달라서 그렇습니다.**
![이미지](/assets/img/Github%20Blog/Github_Blog_3.jpg)

이제 Sourcetree, Github Desktop나 commend line을 활용하여 원격지의 repository를 자신의 로컬에 Clone을 해야합니다.  
저는 Github Desktop을 활용해 Clone을 하였습니다.  
Github Desktop에 자신의 Github 계정으로 로그인하면 "```username```.github.io" repository를 선택 후 Clone 버튼을 클릭하면 자신의 로컬에 Clone이 됩니다.    

**선택을 못했거나 Clone이 안되었으면 File->Clone a repository->Github.com에서 repository를 선택하여 <br>Clone하시면 됩니다.**  

테스트로 홈페이지 하나를 작성해보겠습니다. 저는 Visual Studio Code를 활용하여 Clone된 폴더를 열고 index.html 파일을 생성하여 아래와 같이 작성하였습니다.
```html
<html>
	<body>
		Hello Github Blog!
	</body>
</html>
```
좌측 Changes에 index.html 변경 내용 확인 후 commit->push 해주시면 완료입니다.  
![이미지](/assets/img/Github%20Blog/Github_Blog_4.jpg)

Github홈페이지에서 "```username```.github.io" repository를 확인하면 README.md 파일과 index.html파일이 보이면 Push가 성공적으로 된 걸 확인할 수 있습니다.  
이제 웹 주소창에 "http://```username```.github.io"로 접속하시면 상단에 "Hello Github Blog"가 보이면 완료입니다.