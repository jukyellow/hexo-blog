---
title: Hexo blog 스킨 적용 및 github 배포
catalog: true
date: 2021-01-30 07:00:45
subtitle: Hexo 블로그 테마 다운로드, 설치, Github 배포까지!
header-img: "tag-bg.png"
tags: ["hexo", "hexo blog", "hexo install"]
categories:
- Blog, PT
- Hexo
---

## 1. git/npm windows 설치
> git과 npm이 사전에 설치되어 있어야한다.  


## 2. hexo (기본 가이드 한글로 번역됨)  
- https://hexo.io/ko/docs/   
```
npm install hexo-cli -g --save
npm install hexo-server --save
npm install hexo-deployer-git --save
```


## 3. 테마 repo clone
- 테마 원본: https://github.com/YenYuHsuan/hexo-theme-beantech  
- 테마 튜닝: https://github.com/jukyellow/hexo-blog
```
git clone https://github.com/jukyellow/hexo-blog
```


## 4. 경로진입
> cd hexo-beantech  


## 5. node 패키지 설치
```
npm install
```


## 6. 실행
- hexo serve  
- localhost:4000 확인  


## 7. category 기능 활성화:
- _config.yml > widgets 부분 category 주석풀기 + post에 작성시 category 추가  


## 8. 기초세팅
- _config.yml 설정(https://github.com/YenYuHsuan/hexo-theme-beantech 따라하기)  


## 9. post작성 및 배포
```
hexo new post "<post name>" # you can change post to another layout if you want
hexo clean && hexo generate # generate the static file
hexo server # run hexo in local environment
hexo deploy # hexo will push the static files automatically into the specific branch(gh-pages) of your repo!
```


## 10. 버그 패치
1) hexo beantech 테마 적용후, deploy 단계에서 파일 0 bytes 오류 발생  
2) hexo 3.9버전이 버전이여서 문제인가 싶어, hexo init으로 새 폴더 생성(hexo 5.3.0버전)+ theme 복제  
3) forEach문 오류발생(sidebar widgets 목록을 찾을수 없음)  
4) theme/beantech/_config.yml에 widgets목록을 직접 기입해서 해결됨, deploy도 성공  


## 11. tag/category 입력
```
tags:
- Hexo
- Blog
# or tags: ["A", "B"]
catagories:
- Hexo
```


## 12. 무료 이미지 다운로드
> https://www.freepik.com
> https://pixabay.com/
> https://unsplash.com/
<br>
