---
title: "Theme Headers & Footers"
---

CTFd allows for admins to set Cascading Style Sheets (CSS) rules and JavaScript (JS) code that applies to the user facing portion of the site. This allows admins to make simple style changes without having to create entirely new custom themes.

<div class="alert rounded-0 alert-primary">
  The configured theme must have been programed to use this behavior.
</div>

## Theme Header

In the admin panel, under Config > Appearances, you can edit the CSS & JS used for your CTFd instance as part of the theme header.

The theme header is loaded as part of the ``<head>`` element before the ``<body>`` tag of the page. Here you can add whatever HTML, CSS, or JS you would like such as changing the fonts or scripts used for your theme.

![](/images/config/css-header.png)

## Theme Footer

You can also edit the CSS & JS loaded through the Theme footer as well. The theme footer is loaded at the end of the page, just before the closing ``</body>`` tag.

![](/images/config/css-footer.png)

### Example

Setting the theme header as such will change the font to a different family. While this example only demonstrates CSS, you can also add in custom JS files or modify other aspects of the page using HTML.

```html
<link href="https://fonts.googleapis.com/css?family=Oswald&display=swap" rel="stylesheet">
<style>
:not(i) {
    font-family: 'Oswald', sans-serif !important;
}
</style>
```

![](/images/config/css-header-filled.png)

![](/images/config/css-header-effect.png)