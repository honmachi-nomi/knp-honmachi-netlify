# knp-honmachi-netlify

[Hugo](https://gohugo.io/), [Netlify](https://www.netlify.com/), [GitHub](https://github.com/)

## ブランチについて

- `master`: 公開ブランチ
- `develop`: Theme, サイト設定
- `記事 post`: 記事投稿

## Getting Started

```bash
$ brew update && brew install hugo
```

```bash
$ git clone git@github.com:honmachi-nomi/knp-honmachi-netlify.git
```

```bash
$ cd knp-honmachi-netlify
```

### Add content

ステータス: 下書き（ `draft = true` ）の記事が `content/post/hoge.md` に作成されます。  
**`draft = true` のまま公開ブランチに push しても公開されません。**

```bash
$ hugo new post/hoge.md
```

#### Make posts public

記事が作成できたら、 `draft = false` にします。

```bash
$ hugo undraft content/post/hoge.md
```

### Serve content

現在使用中の Theme 名 [robust](https://github.com/dim0627/hugo_theme_robust) を引数でわたします。

```bash
$ hugo server --theme=hugo_theme_robust
```

config.toml に以下を書けば、省略することができます。

```config.toml
theme = "hugo_theme_robust"
```

```bash
$ hugo server
```

<http://localhost:1313/>

また下書き状態の記事を表示する際は以下のオプションも必要です。

```bash
$ hugo server --buildDrafts --theme=hugo_theme_robust
```
