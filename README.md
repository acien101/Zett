# Zett

Hugo theme for creating a digital garden based on Zettelkästen. Original work by [Crisrojas](https://github.com/crisrojas) from [Zettels](https://github.com/crisrojas/zettels). Checkout [gumroad](https://gumroad.com/l/zettelkasten) for supporting the original author.

## Demo

<https://acien101.gitlab.io/>

## Minimum Hugo version

You will need Hugo *extended* version in order to support Sass/SCSS.

Hugo version 0.60.1 or higher is required. View the [Hugo releases](https://github.com/gohugoio/hugo/releases) and download the binary for your OS.

## Installation

From the root of your site:

```
git submodule add https://github.com/acien101/Zett themes/Zett
```

## Updating

From the root of your site:

```
git submodule update --remote --merge
```

## Run example site

From the root of `themes/Zett/exampleSite`:

```
hugo server --themesDir ../..
```

## Configuration

Copy `config.yaml` from the [`exampleSite`](https://github.com/acien101/Zett/blob/master/exampleSite/config.yaml), then edit as desired.

## Favicons

Upload your image to [RealFaviconGenerator](https://realfavicongenerator.net/) then copy-paste the generated favicon files under `assets`.

### Linking notes

This theme includes [[wikilinks]] support.

If you want to link a note, just put it's file name inside two brackets.

That means that for the note:

```
biology.md
```

You would link it like this

```
[[biology]]
```

Output:

```html
<a href="biology.html">biology</a>
```

Make sure your filenames contain not spaces as this isn't supported by the regex yet.

**DO**

```
biologia-celular.md ✅
[[biologia-celular]] ✅
```

**DON'T**

```
biología celular.md ⛔️
[[biología celular]] ⛔️
```

**Your markdown notes go inside the `content` folder and need to comply with a valid yaml syntax if you're using metadata**

### Backlinks

Backlinks are supported right out the box. To use them properly you would want to give a title to each of your notes in the yaml header,  like so:

```
---
title: My awesome note
---

Hi! This is the content of my awesome note.
```

This way the note can be referenced in the backlinks section since the backlink function will look for the `title` key.

### MathJax

You can write math equations using **latex syntax**.

```
For multi-line equations:

$$
\sqrt{\frac{\lambda}{\ro}}
$$

For inline equations you can use \\(\Omega_{124}\\)
```
