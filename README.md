## Description

Works in a IS590 WFO, Web development using app framework





### Django templates

`|linebreaksbr` is piping the posts' text through a filter to convert line-breaks into paragraphs.





### CSS – make it pretty!

**Static files** are all your CSS and images. Their content doesn't depend on the request context and will be the same for every user.

```css
h1 a, h2 a {
    color: #C25100;
}
```

`h1 a` is a CSS Selector. This means we're applying our styles to any `a` element inside of an `h1`element; the `h2 a` selector does the same thing for `h2` elements. 



#### Ways to determine styles for elements in the HTML file

*  identify elements is with the element name. You might remember these as tags from the HTML section. Things like `a`, `h1`, and `body` are all examples of element names.
* identify elements by the attribute `class` or the attribute `id`. Class and id are names you give the element by yourself. Classes define groups of elements, and ids point to specific elements.



#### Tell our HTML template that we added some CSS.

Open the .html file in the code editor and add this line at the very beginning of it(We're just loading static files here.):

```html
{% load static %}
```

Between the `` and `` tags, after the links to the Bootstrap CSS files, add this line:

```html
<link rel="stylesheet" href="{% static 'css/blog.css' %}">
```

