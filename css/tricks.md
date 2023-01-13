## to set the logo in the header

```
.header{
  position: relative;
}
.logobox{
  position: absolute;  // container should have relative to make context to it
  top:40px;
  left: 40px;
}
.logo{
  height: 35px;  // can set only the height and width will be automatically figured out and vice versa
}
```

```
<header class="header">
  <div class="logo-box">
    <img class="logo">
  </div>
</header>
```

## to center anything with transform, top, left properties

```
.center-box{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.wrapper{
  backface-visibility: hidden;   // when we use the animation, there is a shake , to avoid this we have added this on the parent element
}
.header{
  animation-name: moveInLeft;
  animation-duration: 5s;
  animation-timing-function: ease-out;
  // animation-delay: 3s;
}
.sub-header{
animation: moveInRight  1s ease-out;
}
```

```
<div class='center-box'>
  <div class="wrapper">
    <div class="header">Outdoors<div>
    <div class="sub-header">is where the life starts</div>
  </div>
</div>
```

## spacing between the letters

```
letter-spacing: 35px;
```

## create animations using keyframes and animation property

@keyframes moveInLeft {
0%{
opacity: 0;
transform:translateX(-100px)
}
80%{
transform:translateX(10px)
}
100%{
opacity: 1;
transform:translateX(0)
}
}

@keyframes moveInRight {

0%{
opacity: 0;
transform:translateX(100px)
}

80%{
transform:translateX(-10px)
}

100%{
opacity: 1;
transform:translateX(0)
}

}
