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

Note:

1. Good practise to have one h1 in a page
2. we need to mention lang attribute to en to html
<html lang="en">

3. jonas.io (resources links)
