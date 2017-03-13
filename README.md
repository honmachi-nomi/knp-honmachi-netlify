# knp-honmachi-netlify

[Hugo](https://gohugo.io/), [Netlify](https://www.netlify.com/), [GitHub](https://github.com/)

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
** `draft = true` のまま公開ブランチに push しても公開されません。**

```bash
$ hugo new post/hoge.md
```

#### Make posts public

記事が作成できたら、 `draft = false` にします。

```bash
$ hugo undraft content/post/hoge.md
```

### Serve content

```bash
$ hugo server --theme=hugo_theme_robust
```

<http://localhost:1313/>

記事が下書き状態の時は以下のオプションが必要です。

```bash
$ hugo server --buildDrafts --theme=hugo_theme_robust
```
