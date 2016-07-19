---
layout: post
title:  "맥 초기화시 개발환경 구축"
description: "맥을 초기화 후 나만의 기본적인 개발환경 초기 세팅법"
category: dev
tags: [xcode, mac, homebrew, zsh, git, sass, jekyll]
---



### 맥 초기화시 개발환경 세팅

#### -기준 엘캐피탄

1. Xcode 설치
1. homebrew 설치
  1. [OS X 10.11 엘 캐피탄에 '홈브류(Homebrew)'를 설치하는 방법](http://macnews.tistory.com/3728)
<pre class="terminal small">
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
</pre>
1. 터미널 설정
  1. CMD+, 눌러 테마 홈브류, 테스트 크기등 설정
1. Oh My ZSH! 설치
  1. [터미널 초보의 필수품인 Oh My ZSH!를 사용하자](http://nolboo.github.io/blog/2015/08/21/oh-my-zsh)
  1. zsh 설치!!
      1. `$ zsh --version` 로 설치 확인
      1. `$ brew update` 로 최신 업뎃 or `$ brew install zsh` 로 설치
      1. `$ which zsh`로 zsh 경로 확인 `$ chsh -s /bin/zsh`로 쉘 경로 변경
      1. `$ echo $SHELL`로 쉘경로 변경확인
  1. Oh My Zsh 설치!!
<pre class="terminal small">
$ curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh
</pre>
1. 터미널(zsh)에서 ll 동작 할 수 있도록 설정
  1. alias ll='ls -lhp' 추가
  1. bash 에서 ll사용
      1. `vi .bash_profile` bash프로필 수정
      1. `alias ll='ls -nhp'`추가
      1. `:wq` 저장하고 나오기
  1. zsh에서 ll사용
      1. `vi ~/.zshrc` zsh설정 들어가서
      1. 젤 마지막쪽에 `alias ll='ls -nhp'` 추가
      1. `:wq` 저장하고 나오기
1. Git 설치
  1. [맥 GIT 설치](https://git-scm.com/book/ko/v1/%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0-Git-%EC%84%A4%EC%B9%98)
      1. <del> `$ sudo port install git-core +svn +doc +bash_completion +gitweb`</del>
      1. `$ git version` 깃 버전 확인
      1. `$ git config --global user.name "이름"` 이름설정
      1. `$ git config --global user.email linu4u@example.com` 메일 설정
1. Git 세팅 > github ssh키값 설정
  1. [Generating SSH keys - 깃허브](https://help.github.com/articles/generating-ssh-keys)
      1. SSH키를 새로 생성 > `$ ssh-keygen -t rsa -b 4096 -C "메일주소"`
      1. `Enter a file in which to save the key (/Users/you/.ssh/id_rsa):` 나오면 엔터!
      1. `Enter passphrase (empty for no passphrase):` 라고 나오면 암호 입력!(짧으면 에러남)
      1. `Enter same passphrase again:` 라고 나오면 한번더 엔터
      1. `$ eval "$(ssh-agent -s)"` 라고 입력!
      1. `$ ssh-add ~/.ssh/id_rsa` 라고 입력!
      1. 키값 복사하기 > `$ pbcopy < ~/.ssh/id_rsa.pub` 라고 입력!
      1. [깃허브 SSH and GPG keys 세팅](https://github.com/settings/keys) 에 `New SSH key`를 클릭하여 닉네임 지정후 붙여넣기 !
1. [sass 설치 및 적용](https://opentutorials.org/course/470/2489)
      1. 맥과 리눅스에는 ruby가설치 되어 있기 때문에 `$ gem install sass`를 입력해서 sass 컴파일러를 설치한다.
      1. CSS 폴더에가서 `$ sass --watch style.scss:style.css --style expanded --sourcemap=none` 으로 실행
1. 작업폴더 바로가기 만들기
    1. ln -s 소스폴더 별명폴더
    1. ex) `$ ln -s /Users/linu4u/Dropbox/1.lates/0.HTML/1.GIT/linu4u 2.git`
1. D2Coding 설치
    1. [네이버 개발자센터 - D2 Coding 글꼴](http://dev.naver.com/projects/d2coding/)
1. [스크린샷 저장 폴더 위치 변경](http://macnews.tistory.com/3188)
    1. `$ defaults write com.apple.screencapture location 저장할폴더위치 `
        1. `$ defaults write com.apple.screencapture location ` 한다음 폴더 드래서 해서 지정하기도 가능
    1.  `$ killall SystemUIServer` 실행해서 바로 적용
1. jekyll 서비스 설치
  1. [지킬로 깃허브에 무료 블로그 만들기](https://nolboo.github.io/blog/2013/10/15/free-blog-with-github-jekyll/)
  2. [Jekyll 시작하기 - 리누깃헙](http://linu4u.github.io/jekyll/2015/08/25/jekyll-start)
