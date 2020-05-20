# README

## セットアップ

サイト作成

```shell
hugo new site hugo-liva
```

レポジトリ初期化

```shell
cd hugo-liva
git init
echo '*.bak' >> .gitignore
echo '*~' >> .gitignore
echo '*.orig' >> .gitignore
echo 'public' >> .gitignore
```

テーマ設定

```shell
cd themes 
git submodule add https://github.com/themefisher/liva-hugo.git
```

サイト設定

```shell
cd hugo-liva
cp -pr ./themes/liva-hugo/exampleSite/{config.toml,static,content} .
```

config.toml

```toml
baseURL = "https://higebobo.github.io/hugo-liva/"
languageCode = "ja"
title = "Hugo Liva"
theme = "liva-hugo"
publishDir = "docs"
```

> github pagesやnetlifyで使う場合はbaseURLのプロトコルはhttpsにすること

Githubレポジトリ作成後

```shell
git remote add origin git@github.com:higebobo/hugo-liva.git
hugo
git add -A
git commit -m 'init'
git push -u origin master
```

Github>Settings>Gighub Pages>Source>master branch/docs folder

## 既存のレポジトリからクローンする場合

```shell
git clone git@github.com:higebobo/hugo-liva.git higebobo-liva
cd higebobo-liva
git submodule update --init --recursive
```

## 使い方

### 投稿

新規ポートフォリオ

```shell
hugo new blog/hello.md
content/blog/hello.md created
```

編集

```shell
vi content/blog/hello.md
```

公開(githubにプッシュ)

```shell
make deploy
```

## Link

* [Liva Hugo \| Hugo Themes](https://themes.gohugo.io/liva-hugo/)
