## Evernote 에 Markdown 문서를 작성하는 방법

Mac 에서 Evernote 클라이언트에서 마크다운 프리뷰를 제공하지 않는다.
하지만 이쁜 문서로 남기고 싶은 욕심은 누구에게나 있다.

최근 회사 동료분중에 한분도 그런 방법이 없는지 구글링을 해봤지만 적절한 방법을 찾지 못하고 있다고 했다.
물론 나도 무료 마크다운 편집기인 [Mou](http://mouapp.com/) 를 사용하고 있다.

하지만 [Mou](http://mouapp.com/) 는 편집 기능만 제공하고 클라우드 환경을 별도로 제공하지 않는다.  그래서 Mou 로 작성된 마크다운을 스타일을 적용해 에버노트로 게시할 수 없을까 고민하다.

적절한 해결책을 찾았다.

### 준비물
준비물은 맥, 에버노트, Mou 이렇게 3가지와 [마크다운](http://daringfireball.net/projects/markdown/)을 즐겨 쓰는 마음 가짐만 있으면 된다.

[Mac](http://www.apple.com/mac/), [Evernote](http://evernote.com/intl/ko/), [Mou](http://mouapp.com)


## 설치

### Fancy Install
```
$ curl https://raw.github.com/rhiokim/Mou2Evernote/master/bin/install.sh | sh
```

### Source Install
```
$ git clone git@github.com:rhiokim/Mou2Evernote.git
$ cd Mou2Evernote
$ make
```


## 실행 방법

### AppleScript 활성화
AppleScript 메뉴는 맥에서 기본적으로 활성화 되어있지 않다.  
먼저 AppleScript 를 실행하고 환경설정 > 일반 탭 에서 "메뉴 막대에서 스크립트 메뉴 보기" 를 체크하면 된다.

![](https://github.com/rhiokim/Mou2Evernote/raw/master/screenshots/applescript-preference.png) 

위의 설정을 체크하면 상단 메뉴바에 AppleScript 가 생기고 다양한 AppleScript 를 활용할 수 있다.  만약 위의 Mou2Evernote 를 실행했다면 가장 하단에 `mou2evernote.scpt` 항목이 추가되어 있는 것을 볼 수 있다.

### Alfred 를 이용하기
Alfred 는 맥에서 빠른 애플리케이션 런쳐로 맥에서 기본적으로 제공하는 'spotlight' 기능보다 더 많은 고급 기능을 제공하고 있다. 
물론 AppleScript 도 바로 실행이 가능하기 때문에 Mou2Evernote Script 도 Alfred 에 추가하면 간편하게 이용할 수 있다.

![](https://github.com/rhiokim/Mou2Evernote/raw/master/screenshots/alfred-preference.png)

Alfred 의 환경설정(Preference)에서 위의 사진에서 처럼 `/Users/사용자계정/Library/Scripts` 를 추가하면 Alfred 에서도 바로 수행할 수 있게 된다.

[http://www.alfredapp.com/](http://www.alfredapp.com/)

## 소스에 대하여
이 소스는 [sandai](http://github.com/sandai) 씨가 작성한 AppleScript 를 fork 받아 일부만 한글화를 하였고 설치에 용이하도록 쉘 스크립트를 작성하였다.