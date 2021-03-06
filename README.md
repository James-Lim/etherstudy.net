# 이더리움 연구회 기술 블로그

[![Current Branch](https://img.shields.io/badge/dynamic/yaml.svg?label=current%20branch&url=https%3A%2F%2Fraw.githubusercontent.com%2Fetherstudy%2Ftech.etherstudy.net%2Fmaster%2F.travis.yml&query=%24.default_branch)](https://github.com/etherstudy/tech.etherstudy.net) [![Build Status](https://travis-ci.org/etherstudy/tech.etherstudy.net.svg?)](https://travis-ci.org/etherstudy/tech.etherstudy.net) [![GitHub issues](https://img.shields.io/github/issues/etherstudy/tech.etherstudy.net.svg)](https://github.com/etherstudy/tech.etherstudy.net) [![GitHub contributors](https://img.shields.io/github/contributors/etherstudy/tech.etherstudy.net.svg)](https://github.com/etherstudy/tech.etherstudy.net/graphs/contributors/)



이 블로그는 이더리움 연구회에서 운영하는 기술 블로그입니다.

# Hosting

본 블로그는 Github pages를 통해 호스팅됩니다. 호스팅되는 브랜치는 `gh-pages` 브랜치이며, 실제로는 `master` 브랜치의 [`.travis.yml`](https://github.com/etherstudy/tech.etherstudy.net/blob/master/.travis.yml) 파일의 `default_branch` 항목이 가리키는 브랜치[![Current Branch](https://img.shields.io/badge/dynamic/yaml.svg?label=current%20branch&url=https%3A%2F%2Fraw.githubusercontent.com%2Fetherstudy%2Ftech.etherstudy.net%2Fmaster%2F.travis.yml&query=%24.default_branch)](https://github.com/etherstudy/tech.etherstudy.net) 에 변경사항이 발생하면, [Travis CI](https://travis-ci)에 의해 변경사항이 `gh-pages` 브랜치로 Force Push 되는 방식으로 업데이트 됩니다. 따라서 새로운 테마를 적용하는 등의 개편을 진행할 때에는 새로운 브랜치를 생성하여 작업한 뒤 `master`의 [`.travis.yml`](https://github.com/etherstudy/tech.etherstudy.net/blob/master/.travis.yml)의 `default_branch` 항목을 해당 브랜치로 변경하면 됩니다.

# Local test

```
bundle install
bundle exec jekyll serve
```

# 새로운 포스트 작성하는 방법

1. Fork하기

     레포지토리를 본인 깃허브 계정으로 포크해주세요.  [![Github Fork](https://img.shields.io/github/forks/etherstudy/tech.etherstudy.net.svg?style=social&label=Fork)](https://github.com/etherstudy/tech.etherstudy.net/fork)

2. 포스팅용 브랜치 시작

     ```bash
     git clone https://github.com/$YOUR_GITHUB_ID/tech.etherstudy.net
     ```
     을 통해 클론하신 다음, 게시물 이름으로 새로운 브랜치를 시작해주세요.

     ```bash
     git checkout -b $BRANCH_NAME_WITH_POST_TITLE
     ```

3. 게시물 작성

     `_posts` 폴더에 `yyyy-mm-dd-title.markdown`의 형식으로 파일을 만들어주세요.

     게시물 작성을 완료하였으면 해당 게시물을 Stage에 올린 뒤 Commit합니다.
     ```bash
     git add ./_posts/$YOUR_POSTING_FILE
     git commit -m "$PUT_COMMIT_MESSAGE_HERE"
     ```

     자세한 내용은 [여기](/_posts/2018-06-24-welcome-to-jekyll.markdown)를 참조해주세요.

4. 푸쉬

     본인의 깃허브 계정에 게시물 작성을 위해 만든 브랜치를 푸쉬해주세요.
     ```bash
     git push $YOUR_REPOSITORY_URL $BRANCH_NAME_WITH_POST_TITLE
     ```

5. 풀리퀘스트

     Base branch를 [![Current Branch](https://img.shields.io/badge/dynamic/yaml.svg?label=current%20branch&url=https%3A%2F%2Fraw.githubusercontent.com%2Fetherstudy%2Ftech.etherstudy.net%2Fmaster%2F.travis.yml&query=%24.default_branch)](https://github.com/etherstudy/tech.etherstudy.net)으로 해서 [Pull Request를 만들어주세요](https://github.com/etherstudy/tech.etherstudy.net/compare).

6. Pull Request가 승인되면 게시물이 자동으로 업데이트 됩니다.



# 웹브라우저를 통해 빠르게 포스트 작성하기

깃허브에서 제공하는 기능을 활용해서 포스트를 빠르게 작성할 수 있습니다.

1. 레포지토리로 이동 후 [Create new file 버튼](https://github.com/etherstudy/tech.etherstudy.net/new/ui-180622)클릭

2. File 이름으로 `_posts/yyyy-mm-dd-title.markdown` 입력 (yyyy, mm, dd, title은 직접 변경하세요)

3. 포스트의 정보를 `---` 사이에 YAML형태로 간단하게 적어주세요. 다음을 참조하면 됩니다. 그리고 그 아래에 포스트를 작성해주세요.

   ````markdown
   ---
   layout: post # 바꾸지 마세요.
   title:  "여기에 새로운 제목을 입력하세요".
   date:   2018-06-24 19:57:40 +0900 # 작성 날짜를 입력해주세요.
   author:  저자 이름 <your-email@address.com>
   ---
   # H1
   ## H2
   여기에 포스트를 작성해주세요
   ````

4. 기본적으로 Pull request 형식을 따르고, 굳이 리뷰가 필요하지 않을 경우에는 직접 Commit해주세요.



# Built with Jekyll

This is the base Jekyll theme. You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at [jekyllrb.com](https://jekyllrb.com/)

You can find the source code for Minima at GitHub:
[jekyll][jekyll-organization] /
[minima](https://github.com/jekyll/minima)

You can find the source code for Jekyll at GitHub:
[jekyll][jekyll-organization] /
[jekyll](https://github.com/jekyll/jekyll)


[jekyll-organization]: https://github.com/jekyll



# LICENSE
[MIT](/LICENSE)
