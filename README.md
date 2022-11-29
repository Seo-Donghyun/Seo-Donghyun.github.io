<!-- # Lanyon

Lanyon is an unassuming [Jekyll](http://jekyllrb.com) theme that places content first by tucking away navigation in a hidden drawer. It's based on [Poole](http://getpoole.com), the Jekyll butler.

![Lanyon](https://f.cloud.github.com/assets/98681/1825266/be03f014-71b0-11e3-9539-876e61530e24.png)
![Lanyon with open sidebar](https://f.cloud.github.com/assets/98681/1825267/be04a914-71b0-11e3-966f-8afe9894c729.png)


## Contents

- [Usage](#usage)
- [Options](#options)
  - [Sidebar menu](#sidebar-menu)
  - [Themes](#themes)
  - [Reverse layout](#reverse-layout)
- [Development](#development)
- [Author](#author)
- [License](#license)


## Usage

Lanyon is a theme built on top of [Poole](https://github.com/poole/poole), which provides a fully furnished Jekyll setup—just download and start the Jekyll server. See [the Poole usage guidelines](https://github.com/poole/poole#usage) for how to install and use Jekyll.


## Options

Lanyon includes some customizable options, typically applied via classes on the `<body>` element.


### Sidebar menu

Create a list of nav links in the sidebar by assigning each Jekyll page the correct layout in the page's [front-matter](http://jekyllrb.com/docs/frontmatter/).

```
---
layout: page
title: About
---
```

**Why require a specific layout?** Jekyll will return *all* pages, including the `atom.xml`, and with an alphabetical sort order. To ensure the first link is *Home*, we exclude the `index.html` page from this list by specifying the `page` layout.


### Themes

Lanyon ships with eight optional themes based on the [base16 color scheme](https://github.com/chriskempson/base16). Apply a theme to change the color scheme (mostly applies to sidebar and links).

![Lanyon with red theme](https://f.cloud.github.com/assets/98681/1825270/be065110-71b0-11e3-9ed8-9b8de753a4af.png)
![Lanyon with red theme and open sidebar](https://f.cloud.github.com/assets/98681/1825269/be05ec20-71b0-11e3-91ea-a9138ef07186.png)

There are eight themes available at this time.

![Available theme classes](https://f.cloud.github.com/assets/98681/1817044/e5b0ec06-6f68-11e3-83d7-acd1942797a1.png)

To use a theme, add any one of the available theme classes to the `<body>` element in the `default.html` layout, like so:

```html
<body class="theme-base-08">
  ...
</body>
```

To create your own theme, look to the Themes section of [included CSS file](https://github.com/poole/lanyon/blob/master/public/css/lanyon.css). Copy any existing theme (they're only a few lines of CSS), rename it, and change the provided colors.


### Reverse layout

![Lanyon with reverse layout](https://f.cloud.github.com/assets/98681/1825265/be03f2e4-71b0-11e3-89f1-360705524495.png)
![Lanyon with reverse layout and open sidebar](https://f.cloud.github.com/assets/98681/1825268/be056174-71b0-11e3-88c8-5055bca4307f.png)

Reverse the page orientation with a single class.

```html
<body class="layout-reverse">
  ...
</body>
```


### Sidebar overlay instead of push

Make the sidebar overlap the viewport content with a single class:

```html
<body class="sidebar-overlay">
  ...
</body>
```

This will keep the content stationary and slide in the sidebar over the side content. It also adds a `box-shadow` based outline to the toggle for contrast against backgrounds, as well as a `box-shadow` on the sidebar for depth.

It's also available for a reversed layout when you add both classes:

```html
<body class="layout-reverse sidebar-overlay">
  ...
</body>
```

### Sidebar open on page load

Show an open sidebar on page load by modifying the `<input>` tag within the `sidebar.html` layout to add the `checked` boolean attribute:

```html
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox" checked>
```

Using Liquid you can also conditionally show the sidebar open on a per-page basis. For example, here's how you could have it open on the homepage only:

```html
<input type="checkbox" class="sidebar-checkbox" id="sidebar-checkbox" {% if page.title =="Home" %}checked{% endif %}>
```

## Development

Lanyon has two branches, but only one is used for active development.

- `master` for development.  **All pull requests should be to submitted against `master`.**
- `gh-pages` for our hosted site, which includes our analytics tracking code. **Please avoid using this branch.**


## Author

**Mark Otto**
- <https://github.com/mdo>
- <https://twitter.com/mdo>


## License

Open sourced under the [MIT license](LICENSE.md).

<3 -->

## 20223091 서동현 git 블로그 build 과정

이 글은 20223091 서동현의 git 블로그 build 과정을 적은 글입니다.

## 목차

- [Repository 생성](#repository-생성)
- [로컬 저장소와 연동](#로컬-저장소와-연동)
- [jekyll](#jekyll)
  - [컴퓨터에 설치](#컴퓨터에-설치)
- [테마 가져오기](#테마-가져오기)
- [git에 연동](#git에-연동)
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

저 같은 경우에는 아무 post를 적지 않은 상태에서 테마를 가져오기 위해, 제가 원한 테마인 [lanyon](https://github.com/poole/lanyon)의 zip파일을 다운 받아서 로컬 저장소에 저장했습니다. 
![예시](/assets/images/readme.md%20%EC%82%AC%EC%A7%841.png "예시")

## git에 연동

우선 git에 연동하고 싶은 파일들을 git에서 추적하기 위해 `git add <파일 이름>`을  통해 staged 시킵니다. 물론 `git add *`을 통해 현재 디렉토리의 모든 파일을 한 번에 staged 시킬 수 있습니다. 다음으로 `git commit -m "남기고 싶은 말"`을 통해 staged 시킨 파일들에 대해 메모할 말을 적습니다. 마지막으로 `git push origin main`을 통해서 git에 연동 시킵니다.
![예시](/assets/images/readme.md%20%EC%82%AC%EC%A7%842.png "예시")

## 완료

위의 과정을 따라오면 다음과 같은 저의 블로그가 완성됩니다.
![예시](/assets/images/readme.md%20%EC%82%AC%EC%A7%843.png "예시")
