## 20223091 서동현 git 블로그 build 과정

이 글은 20223091 서동현의 git 블로그 build 과정을 적은 글입니다.

## 목차

- [Repository 생성](#repository-생성)
- [로컬 저장소와 연동](#로컬-저장소와-연동)
- [jekyll](#jekyll)
  - [컴퓨터에 설치](#컴퓨터에-설치)
- [테마 가져오기](#테마-가져오기)
- [git에 연동](#git에-연동)
- [disqus로 댓글 구현](#댓글-구현)
- [완료](#완료)

## repository 생성

우선 github에서 제 이름을 적은 Seo-Donghyun.github.io 라는 repository를 생성했습니다.

## 로컬 저장소와 연동

repository를 생성한 다음 로컬 저장소에 연동할 repository를 생성하고,
git repository 주소를 복사해서 로컬 저장소에 `git clone <주소>`를 적어서
연동해줍니다.

## jekyll

jekyll은 **Ruby 기반 정적 웹사이트 생성기**입니다.
그래서 이번에 이를 통해 git 블로그를 만들었습니다.

### 컴퓨터에 설치

jekyll은 [jekyll 사이트](https://jekyllrb-ko.github.io/)에서 설치합니다.
여기에서 ruby와 jekyll을 같이 설치하고나서 로컬 저장소에 `jekyll new . --force`를 입력해서 jekyll을 설치할 수 있습니다. 이를 통해 간단한 페이지를 만들 수 있습니다.

## 테마 가져오기

저 같은 경우에는 아무 post를 적지 않은 상태에서 테마를 가져오기 위해, 제가 원한 테마인 [lanyon](https://github.com/poole/lanyon)의 파일들을 로컬 저장소에 덮어씌웠습니다. 
![테마](/assets/images/readme.md%20%EC%82%AC%EC%A7%841.png "테마")

## git에 연동

우선 git에 연동하고 싶은 파일들을 git에서 추적하기 위해 `git add <파일 이름>`을  통해 staged 시킵니다. 물론 `git add *`을 통해 현재 디렉토리의 모든 파일을 한 번에 staged 시킬 수 있습니다. 다음으로 `git commit -m "남기고 싶은 말"`을 통해 staged 시킨 파일들에 대해 메모할 말을 적습니다. 마지막으로 `git push origin main`을 통해서 git에 연동 시킵니다.
![예시](/assets/images/readme.md%20%EC%82%AC%EC%A7%842.png "예시")

## 댓글 구현

댓글을 구현하기 위해 disqus를 사용했습니다. 먼저 disqus에 회원가입을 하고, 웹사이트 주소를 입력합니다. 그러고 나서 `_config.yml`에 ![예시](/assets/images/readme.md%20%EC%82%AC%EC%A7%844.png "예시") 이런 key-value를 적어줍니다. 다음으로 disqus에 universal code를 복사해서 `_layouts/post.html`에 붙여넣습니다. 마지막으로 댓글을 허용하고 싶은 post에 ![댓글](/assets/images/readme.md%20%EC%82%AC%EC%A7%845.png "댓글") 다음과 같이 `comments: true`를 적어주면 구현됩니다. ![댓글](/assets/images/readme.md%20%EC%82%AC%EC%A7%846.png "댓글")

## 완료

위의 과정을 따라오면 다음과 같은 저의 블로그가 완성됩니다.
![블로그](/assets/images/readme.md%20%EC%82%AC%EC%A7%843.png "블로그")
