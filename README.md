# xblog: A minimal, tiny and modest Hugo theme.

![screenshot1](https://i.imgur.com/i4AvR1v.png)

![screenshot2](https://i.imgur.com/SyFrZ3E.png)

## Features

- Responsive Layout
- Very small/easy-to-understand codebase
- Basic Hugo builtin features
  - OGP
  - Twitter/Facebook Card
  - Google Analytics
  - Disqus
- Customization based on CSS variables
  - Accent color
  - Fonts

## Customization

Some customizations can be done by overriding the CSS variables. For example, putting the below code at /layouts/partials/head.html:

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Lato&display=swap&{{ querify "text" (print .Site.Copyright .Site.Title "0123456789-") | safeURL }}" /><!-- This line is copied from the original head.html -->

<style>
:root {
  --accent-color: #dda0dd;
  --article-header-font: "Times New Roman", "YuMincho", "Hiragino Mincho ProN", "Yu Mincho", "MS PMincho", serif;
  --article-body-font: "Times New Roman", "YuMincho", "Hiragino Mincho ProN", "Yu Mincho", "MS PMincho", serif;
}
</style>
```

This customization changes the accent color and fonts, like:

![screenshot3](https://i.imgur.com/2Kql1Xl.png)

The list of available variables is [here](https://github.com/acomagu/xblog/blob/main/layouts/_default/baseof.html#L18).

If you need more advanced customization, you can do it by overriding the [partial templates](./layouts/partials).
