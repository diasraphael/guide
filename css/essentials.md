## css reset

```
*{
  margin:0;
  height: 0;
  box-sizing: border-box;  // to change the box-model to set borders and paddings are not added to the elements
}
```

## set background image with linear gradient

```
*{
 background-image: linear-gradient(to right bottom, #72d56f, #28b485), url(../img/hero.jpg);  
 background-size:cover;
 background-position: top; // can have center, bottom try it
}
```

rgba red blue green opacity
can change the opacity by clicking on the color in vscode and pull the opacity level to .8 in color picker.


## clip path feature in css to clip the image

```
clip-path: polygon(0 0, 100% 0, 100% 75%, 0 100%);
```

for different clip types go to
bennettfeely.com/clippy