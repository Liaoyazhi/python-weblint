# Rule

## HTML

### E01001. DOCTYPE must be decalred first (文档类型必须首先声明)

Right(正确)：

```html
<!DOCTYPE html>
<html lang="zh-Hans">
  <head>
    <title>文档的标题</title>
  </head>

  <body>
    文档的内容......
  </body>

</html>
```

Wrong(错误)：

```html
<!-- <!DOCTYPE html> -->
<html lang="zh-Hans">
  <head>
    <title>文档的标题</title>
  </head>

  <body>
    文档的内容......
  </body>

</html>
```

### E01002. DOCTYPE for HTML5 should be "&lt;DOCTYPE html&gt;" (HTML5的文档类型必须是"&lt;DOCTYPE html&gt;")

Right(正确)：

```html
<!DOCTYPE html>
<html lang="zh-Hans">
  <head>
    <title>文档的标题</title>
  </head>

  <body>
    文档的内容......
  </body>

</html>
```

Wrong(错误)：

```html
<!DOCTYPE html6>
<html lang="zh-Hans">
  <head>
    <title>文档的标题</title>
  </head>

  <body>
    文档的内容......
  </body>

</html>
```

### E01003. invalid tag (不可使用非法标签)

Right(正确)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <p>AAA</p>
  </body>
</html>
```

Wrong(错误)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <invalidtag>AAA</invalidtag>
  </body>
</html>
```

### E01004. deprecated tag (不可使用废弃标签)

Deprecated tags include (废弃标签包括):

```html
<center>, <font>, <s>, <strike>, <b>, <i>, <tt>, <small>, <frame>, <acronym>, <big>, <u>, <isindex>, <basefont>, <dir>, <applet>, <style>
```

Right(正确)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <p>something</p>
  </body>
</html>
```

Wrong(错误)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <font>something</font>
  </body>
</html>
```

### E01005. non-selfclosed tag must be paired (双标签必须成对)

Paired Tags(成对标签)：

```html
<html>, <body>, <title>, <p>, <div>, <h1>~<h6>, <abbr>, <address>, <bdi>, <bdo>, <blockquote>, <cite>, <del>, <dfn>, <em>, <ins>, <kbd>, <meter>, <progress>, <rb>, <rtc>, <rp>, <rt>, <ruby>, <time>, <datalist>, <canvas>, <figcaption>, <figure>, <audio>, <source>, <video>, <nav>, <header>, <footer>, <section>, <article>, <aside>, <details>, <dialog>, <pre>, <q>, <samp>, <strong>, <sup>, <sub>, <var>, <form>, <textarea>, <button>, <select>, <option>, <optgroup>, <label>, <fieldset>, <legend>, <frameset>, <noframes>, <map>, <a>, <ul>, <ol>, <li>, <dl>, <dt>, <dd>, <menu>, <menuitem>, <span>, <head>, <script>, <noscript>, <object>, <table>, <th>, <td>, <tr>, <tbody>, <thead>, <tfoot>, <caption>, <col>, <colgroup>, <main>, <picture>, <template>, <data>, <code>
```

Selfclosed tags(自闭合标签)：

```html
<wbr>, <keygen>, <output>, <track>, <embed>, <input>, <iframe>, <img>, <area>, <link>, <meta>, <base>, <param>
```

Right(正确)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <p>段落</p><br>
  </body>
</html>
```

Wrong(错误)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <p>段落
  </body>
</html>
```

### E01006. invalid attribute (不可使用非法属性)

Right(正确)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
  </body>
</html>
```

Wrong(错误)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title invalidattribute="oh">Page Title</title>
  </head>
  <body>
  </body>
</html>
```

### E01007. deprecated attribute (不能使用废弃的属性)

Deprecated attributes (废弃属性包括):

| Attribute (属性) | Element (所属的元素) |
| ---- | ---- |
| manifest | html |
| xmlns | html,title |
| align | caption, iframe, img, input, object, legend, table, hr, div, h1, h2, h3, h4, h5, h6, p, col, colgroup, tbody, td, tfoot, th, thead and tr |
| alink | body |
| link | body |
| vlink | body |
| text | body |
| background | body |
| bgcolor | table, tr, td, th and body |
| border | table and object, img|
| char | col, colgroup, tbody, td, tfoot, th, thead and tr |
| charoff | col, colgroup, tbody, td, tfoot, th, thead and tr |
| compact | dl , ol and ul |
| frame | table |
| frameborder | iframe |
| hspace | img and object |
| nowrap | td and th|
| rules | table |
| type | li, ol and ul |
| value | li |
| valign | col, colgroup, tbody, td, tfoot, th, thead and tr |
| width | hr, table, td, th, col, colgroup and pre |
| accept | form |
| vspace | img |
| charset | a, link |
| coords | a |
| name | a |
| rev | a, link |
| shape |
| target | link |
| height | th, td |

Right(正确)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
  </body>
</html>
```

Wrong(错误)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title style="font-size: 1rem">Page Title</title>
  </head>
  <body>
  </body>
</html>
```

### E01008. required element missing (必须包含特定标签)

- `<html>`必须包含`<head>`，`<body>`
- `<select>`只能且必须包含`<option>`
- `<ul>`只能且必须包含`<li>`
- `<ol>`只能且必须包含`<li>`
- `<dl>`只能且必须包含`<dt>`、`<dd>`
- `<details>`必须包含`<summary>`
- `<video>`必须包含属性`controls`和`<source>`，且`<source>`必须包含`src`属性
- `<audio>`必须包含属性`controls`和`<source>`，且`<source>`必须包含`src`属性

Right(正确)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
  </body>
</html>
```

Wrong(错误)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
  </head>
  <body>
  </body>
</html>
```

### E01009. required attribute missing (必须包含特定属性)

- `<html>`必须包含属性`lang`
- `<link>`元素必须属性是`src`、`rel`
- `<a>`必须包含属性`href`
- `<img>`必须包含属性`src`、`alt`
- `<input>`必须包含属性`type`
- `<iframe>`必须包含属性`src`
- `<embed>`必须包含属性`src`
- `<video>`必须包含属性`controls`和`<source>`，且`<source>`必须包含`src`属性
- `<audio>`必须包含属性`controls`和`<source>`，且`<source>`必须包含`src`属性
- `<input>`的`type`的属性值为`radio`的时候必须包含`name`属性
- `<input>`的`type`的属性值为`img`的时候必须包含`src`、`alt`属性
- `<output>`必须包含属性`name`、`for`
- `<meter>`必须包含属性`value`
- `<progress>`必须包含属性`value`

Right(正确)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
  </body>
</html>
```

Wrong(错误)：

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
  </body>
</html>
```

### E01010. duplicated attribute (同一标签不可使用重复的属性)

Right(正确)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
  </body>
</html>
```

Wrong(错误)：

```html
<!DOCTYPE html>
<html lang="en" lang="zh-Hans">
  <head>
    <title>Page Title</title>
  </head>
  <body>
  </body>
</html>
```

### E01011. tag name must be in lowercase (标签名必须小写)

Right(正确)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
  </body>
</html>
```

Wrong(错误)：

```html
<!DOCTYPE html>
<HTML lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
  </body>
</html>
```

### E01012. attribute name must be in lowercase (属性名必须小写)

Right(正确)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
  </body>
</html>
```

Wrong(错误)：

```html
<!DOCTYPE html>
<html LANG="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
  </body>
</html>
```

### E01013. "title" element must not be empty (title标签不可为空)

- `<p>`内容不能为空

Right(正确)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
  </head>
  <body>
  </body>
</html>
```

Wrong(错误)：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title></title>
  </head>
  <body>
  </body>
</html>
```

### E01014. (必须包含`charset`属性的`<meta>`元素)

示例如下：

```html
<meta charset="utf-8">
```

### E01015. (`id`只能是唯一)

正确：

```html
<body>
  <p id="index">文档内容</p>
  <p id="home">文档内容</p>
</body>
```

错误：

```html
<body>
  <p id="index">文档内容</p>
  <p id="index">文档内容</p>
</body>
```

### E01016. (`<h1>`只能出现一次)

正确：

```html
<body>
  <h1>标题1</h1>
  <h2>标题2</h2>
</body>
```

错误：

```html
<body>
  <h1>标题1</h1>
  <h1>标题1</h1>
</body>
```

### E01017. (不能包含特定标签)

- `<aside>`不能包含`<main>`
- `<nav>`不能包含`<main>`、`<header>`、`<footer>`
- `<header>`不能包含`<main>`、`<footer>`、`<aside>`
- `<footer>`不能包含`<main>`、`<header>`、`<aside>`

正确：

```html
<html lang="zh-Hans">
  <head>
    <meta charset="utf-8">
    <title>文档标题</title>
  </head>
  <body>
    <aside>侧边栏内容</aside>
    <main>主体内容</main>
  </body>
</html>
```

错误：

```html
<html lang="zh-Hans">
  <head>
    <meta charset="utf-8">
    <title>文档标题</title>
  </head>
  <body>
    <aside>
      侧边栏内容
      <main>主体内容</main>
    </aside>
  </body>
</html>
```

### E01018. (`<main>`不带`hidden`只能出现一次)

正确：

```html
<body>
  <main>主体内容</main>
  <main hidden>主体内容</main>
</body>
```

或

```html
<body>
  <main>主体内容</main>
</body>
```

错误：

```html
<body>
  <main>主体内容</main>
  <main>主体内容</main>
</body>
```

### E01019. (`<script>`不能有`type="text/javascript"`属性)

正确：

```html
<script src="js/js.js"></script>
```

错误：

```html
<script src="js/js.js" type="text/javascript"></script>
```

### E01020. (`<link>`不能有`type="text/css"`属性)

正确：

```html
<link src="css/style.css" rel="stylesheet">
```

错误：

```html
<link src="css/style.css" rel="stylesheet" type="text/css">
```
