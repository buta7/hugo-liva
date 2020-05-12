# README

## セットアップ

サイト作成

```shell
hugo new site hugo-syna
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

## 使い方

総合的なウェブサイトなので詳細はcontent参照のこと

## Github連携

config.tomlに以下の設定があることを確認

```toml
baseURL = "https://higebobo.github.com/hugo-liva/"
publishDir = "docs"
```

公開(githubにプッシュ)

```shell
make deploy
```

## Link

* [Liva Hugo \| Hugo Themes](https://themes.gohugo.io/liva-hugo/)
