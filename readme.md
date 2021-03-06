<h1 align="center">
  <img src="https://x.icyphox.sh/iYsTY.png" width="280">
</h1>

> publish your markdown to Medium, from the CLI

**Update: Looks like you can get an integration token by [emailing customer support](https://github.com/icyphox/mdium/issues/2)?**

[Medium](https://medium.com/@icyphox/mdium-publish-your-markdown-to-medium-from-the-cli-79906ef6b16b) post I wrote on a whim.

## Installation

```console
$ pip install mdium
```


## Usage

### Initializing

First off, set up `mdium` with your Medium integration token. You’ll have to generate one from the [settings](https://medium.com/me/settings) page.
```console
$ mdium init <integration-token>
```

This will create a file at `~/.mdium`, containing your integration token and author ID.

### Publishing

For publishing, your markdown doc must have the following frontmatter:

```yaml
---
title: My Awesome Post
tags: ['some', 'tags', 'here']
status: draft
---

## markdown here
...
```

Note that the `status` field can be either `draft` or `public`. I recommend that you publish them as drafts and fine tune using Medium’s editor.

If your post contains images, host them somewhere public and then include them in your document like so:

```markdown
![cat](https://catpics.com/some_cat.png)
```
Medium will then CDN it and you can delete it from there if you want to.

When you’re ready to publish, run
```console
$ mdium publish path/to/markdown.md
Done! Your post has been published at https://medium.com/@gaben/76272e9d241c
```

It’s that simple.

## License

MIT © [Anirudh Oppiliappan](https://icyphox.sh)
