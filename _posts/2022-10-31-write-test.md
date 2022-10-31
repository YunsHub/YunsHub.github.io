---
title: 마크다운(Markdown)
date: 2022-10-31 01:27:11 +0900
categories: [git, markdown]
tags: [markdown] # TAG names should always be lowercase
---
>블로그 포스팅을 위한 마크다운 문법 익히기

## 마크다운(Markdown)이란?
## 마크다운(Markdown) 장단점
## 마크다운(Markdown) 문법
---
### **줄바꿈**
1. 문장 뒤에 스페이스바 2번 + Enter
   ```markdown
   안녕하세요.  
   줄바꿈 테스트 중입니다.
   ```
   안녕하세요.  
   줄바꿈 테스트 중입니다.

2. HTML 태그인 ```<br>``` 태그 사용
   ```markdown
   안녕하세요. <br> 줄바꿈 테스트 중입니다.
   ```
   안녕하세요. <br> 줄바꿈 테스트 중입니다.

### **문단 나누기**
한 줄의 공백을 두고 작성
```markdown
안녕하세요.

문단 나누기 테스트 중입니다.
```
안녕하세요.

문단 나누기 테스트 중입니다.

### **중첩된 구조**
중첩된 구조를 만드려면 스페이스바 2번 띄워준 후 작성
세 번 중첩된 구조는 스페스바 4번 띄워준 후 작성
```markdown
- 중첩
  - 중첩
    - 중첩
```
- 중첩
  - 중첩
    - 중첩

### **마크다운 문법 바로 보여주기**
마크다운 문법 앞에 ```\```를 붙여준다.  
```markdown
\<u>마크다운</u>  
```
\<u>마크다운</u>  
<u>마크다운</u>

### **Header**
글의 제목으로 # 개수에 따라 h1 ~ h6로 나타낸다.
```markdown
# 제목 1단계
## 제목 2단계
### 제목 3단계
#### 제목 4단계
##### 제목 5단계
###### 제목 6단계
```
# 제목 1단계
## 제목 2단계
### 제목 3단계
#### 제목 4단계
##### 제목 5단계
###### 제목 6단계  
<br>

### **텍스트**
```markdown
*기울어진 텍스트*
**굵은 텍스트**
***굵고 기울어진 텍스트***
```
*기울어진 텍스트*  
**굵은 텍스트**  
***굵고 기울어진 텍스트***
```markdown
~~취소선 텍스트~~
```
~~취소선 텍스트~~
```markdown
<u>밑줄 있는 텍스트</u>
```
<u>밑줄 있는 텍스트</u>
```markdown
<span style="color:red">빨간색 텍스트</span>
```
<span style="color:red">빨간색 텍스트</span>

### **inline 코드 블록**
\`\`\`  언어 이름(소문자)  
코드 내용  
\`\`\`

```markdown
inline 코드 블록
```

### **링크**
1. 설명 없는 링크 주소
   ```markdown
   <http://www.google.com>
   ```
   <http://www.google.com>
2. 설명 있는 링크 주소
   ```markdown
   [구글](http://www.google.com)
   ```
   [구글](http://www.google.com)

### **인용문**
```>```로 표현.  
```>>```는 중첩 인용문
```markdown
>인용문
>>중첩 인용문
```
>인용문
>>중첩 인용문  

```<cite>```태그와 ```{: .small}```을 사용하여 인용문 출처 남기기
```markdown
<cite>JungYun</cite> --- YunsHub Android Developer, 2022
{: .small}
```
<cite>JungYun</cite> --- YunsHub Android Developer, 2022
{: .small}

### **리스트**
1. unordered list
   ```markdown
   - 순서
     * 없는
       + 리스트
     * unorder
   - list
   ```
   - 순서
     * 없는
       + 리스트
     * unorder
   - list
2. ordered list
   ```markdown
   1. 순서
   2. 리스트
     1. 하나
       - 1
       - 2
     2. 둘
       - 1
       - 2
   3. ordered list
   ```
   1. 순서
   2. 리스트
      1. 하나
         - 1
         - 2
       2. 둘
          - 1
          - 2
   3. ordered list
3. check list
   ```markdown
   - [ ] 체크X
   - [x] 체크
   ```
   - [ ] 체크X
   - [x] 체크

### **구분선**
```***```와 ```---```로 표현
```markdown
***
---
```
***
---

### **테이블**
```|```와 ```-```의 조합으로 테이블을 표현
- 정렬
    -  왼쪽 : |:---|
    -  오른쪽 : |---:|
    -  가운데 : |:---:|
```markdown
|**공부**|점수|후기|
|:---:|---:|---|
|Android Studio|⭐⭐⭐⭐⭐|어려움|
|Kotlin|⭐⭐⭐⭐⭐|보통|
|Algorithm|⭐⭐⭐⭐⭐|어려움|
```
|**공부**|점수|후기|
|:---:|---:|---|
|Android Studio|⭐⭐⭐⭐⭐|어려움|
|Kotlin|⭐⭐⭐⭐⭐|보통|
|Algorithm|⭐⭐⭐⭐⭐|어려움|