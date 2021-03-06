---
layout: chapter
title: CSS
permalink: /css/
next: /templating/
---

[CSS][css] is a markup language for describing the visuals of web pages. It contains numerous [properties][css-properties] for changing how the HTML elements look like; colors, fonts, layouts etc.


## Prettier defaults

At first let's make the default text look a bit nicer by using the [Pure](http://purecss.io/) CSS library. See its web site for the correct `<link rel="stylesheet">` code and add it inside your HTML page's `<head>`.

![Pure](/screenshots/css-pure.png)

TODO: link to solution


## Custom styles

To have a place where to add our own CSS, create a file `style.css` with the following content and add into your `<head>` a stylesheet link which points to it.

```css
h1 {
    font-size: 30px;
    color: #E0330C;
}

.profile-picture {
    float: right;
    border: 1px solid #E0330C;
}
```

This CSS defines what `<h1>` elements and any elements with the attribute `class="profile-picture"` should look like. Add the `profile-picture` class to your image and it will be positioned on the right side of elements that follow it (move it above your heading and paragraphs).

![Pure](/screenshots/css-basics.png)

TODO: link to solution


## Prepare for layout fiddling

Most web sites contain a navigation menu for moving between pages. Let's create a navigation menu that will be on the left side of the page content and also limit the width of the page content to look nicer on wide screen.

Add the following elements to your page's `<body>` and put the page content you wrote earlier inside the content section.

```html
<nav class="navigation">
    navigation will be here
</nav>

<section class="content">
    page content goes here
</section>
```

To get ready for fiddling with CSS layouts, let's make the edges of the `.navigation` and `.content` elements visible:

```css
.content {
    border: 1px solid Green;
}

.navigation {
    border: 1px solid Blue;
}
```

![Layout elements highlighted](/screenshots/css-layout-blocks-before.png)

TODO: link to solution


## Get the layout right

Now experiment with the CSS properties [position][css-position], [left][css-left], [right][css-right], [top][css-top], [bottom][css-bottom], [width][css-width] and [height][css-height] to get the boxes to look like shown below. Also try to make the page look good whether the page has very little or lots of content; the CSS property [min-height][css-min-height] can be handy.

![Layout elements where we want them](/screenshots/css-layout-blocks-after.png)

[View solution](https://github.com/orfjackal/web-intro-project/commit/a87bf9eb64be3a6b840251f2431400d5bd1fff12)


## Make it pretty

After the boxes are where you want them to be, remove those placeholder borders and move on to styling the layout elements properly. You can change their [background][css-background], add some [margin][css-margin] between the edges and the page content and create nicer [borders][css-border].

For the navigation menu, create an *unordered list* (`<ul>`) which contains *list items* (`<li>`) which contains links (`<a>` as in *anchor*) to the various pages that we will be creating.

```html
<nav class="navigation">
    <ul>
        <li><a href="my-page.html">Ruby</a></li>
        <li><a href="pictures.html">Pictures</a></li>
    </ul>
</nav>
```

Google for "css vertical navigation bar" to find out how to make it look nicer; you'll probably want to remove those black bullet in front of every `<li>`.

![Finished layout styling](/screenshots/css-layout-done.png)

[View solution](https://github.com/orfjackal/web-intro-project/commit/42e94566c051ec08df4ed6e633993b44f57af07d)


[css]: https://developer.mozilla.org/en-US/docs/Web/CSS
[css-properties]: https://developer.mozilla.org/en-US/docs/Web/CSS/Reference
[css-position]: https://developer.mozilla.org/en-US/docs/Web/CSS/position
[css-left]: https://developer.mozilla.org/en-US/docs/Web/CSS/left
[css-right]: https://developer.mozilla.org/en-US/docs/Web/CSS/right
[css-top]: https://developer.mozilla.org/en-US/docs/Web/CSS/top
[css-bottom]: https://developer.mozilla.org/en-US/docs/Web/CSS/bottom
[css-width]: https://developer.mozilla.org/en-US/docs/Web/CSS/width
[css-height]: https://developer.mozilla.org/en-US/docs/Web/CSS/height
[css-min-height]: https://developer.mozilla.org/en-US/docs/Web/CSS/min-height
[css-background]: https://developer.mozilla.org/en-US/docs/Web/CSS/background
[css-margin]: https://developer.mozilla.org/en-US/docs/Web/CSS/margin
[css-border]: https://developer.mozilla.org/en-US/docs/Web/CSS/border
[html-ul]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul
[html-li]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul
[css-navigation-bar]: http://www.w3schools.com/css/css_navbar.asp
