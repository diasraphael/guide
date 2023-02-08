## CSS (Cascading Style Sheets)

is the code that styles web content.

CSS is not a programming language. It's not a markup language either. CSS is a style sheet language. CSS is what you use to selectively style HTML elements.

#### Element

3 parts  
opening tag  
content  
closing tag

#### Semantic elements

b to strong  
i to em  
you can wrap nav and h1 tag under header tag(to be semantic tags)

### Rule or ruleset

The whole structure is called a ruleset. (The term ruleset is often referred to as just rule.)

![image info](images/ruleset.png)

### Style inherit

Since html is the parent element of the whole page, all elements inside it inherit the same font-size and font-family.

```
html {
  font-size: 10px; /* px means "pixels": the base font size is now 10 pixels high */
  font-family: "Open Sans", sans-serif; /* this should be the rest of the output you got from Google Fonts */
}
```

### Notes:

1. Good practise to have one h1 in a page
2. we need to mention lang attribute to en to html

```
<html lang="en">
```

3. jonas.io (resources links)
4. line-height: 1.5(without giving px it will be 1.5 times of the font-size of the element)
5. article header p {} will make the structure not maintainable should avoid this
6. a:link selects all the anchor tag with href attribute
7. order of adding style to a tag is link, visited, hover, active
8. final width of the element = left border + left padding + content + right padding + right border
9. to provide spaces between elements always prefer margins, and to provide vertical space choose margin bottom.
10. only width or height is enough to automatically scale the image.(dont want to mention both, avoid mentioning in html along with image inline style)
11. centering our page trick

```
    .container{
    width: 700px;
    margin: 0 auto;
    }
```
