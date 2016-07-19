---
layout: post
title:  "Jekyll 시작하기"
description: "jekyll를 이용한 블로깅 시작하기"
category: blog
tags: [ jekyll, github ]
---

#### 오늘은 jekyll을 살짝 이해한 역사적인 날이다.
분명 여러가지를 까먹을 것이기에 몇가지 정리를 해놓도록하자

**- jekyll 관련 Url**

- [영문 페이지 - http://jekyllrb.com/](http://jekyllrb.com/)
- [한글 페이지 - http://jekyllrb-ko.github.io/](http://jekyllrb-ko.github.io/)
- [가장 도움이 많이된 블로그 - https://nolboo.github.io/blog/2013/10/15/free-blog-with-github-jekyll/](https://nolboo.github.io/blog/2013/10/15/free-blog-with-github-jekyll/)


**- 내 생각에 중요한 명령들111**

- 설치하기
`$ gem install jekyll` // jekyll 인스톨 ( 필요할경우 sudo 이용)

- 생성하기
`$ mkdir 폴더명` // 깃허브 저상소이면 더 좋음
`$ jekyll new 폴더명`

- 서버실행하기
`$ jekyll serve —watch`  // 해당폴더 내에서 실행하면 서버가 실행되며 --watch 명려으로 실시간 변경 내용반영됨 ( loclahost:4000 )으로 확인가능하다

- 빌드하기
`$ jekyll build` // 빌드를 하게 되면 site라는 폴더에 Html로 완전히 빌드가 되게되어 깃허브가 아니라도 어디든 업로드가 가능함


..
