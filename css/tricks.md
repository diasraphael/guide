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
  text-align: center;
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

```
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

@keyframes moveInBottom {

0%{
opacity: 0;
transform:translateY(30px)
}


100%{
opacity: 1;
transform:translateY(0)
}

}
```

## what are pseudo elements and pseudo classes

\ why to use pseudo element

\ how to create hover animation effect using transition property

```
.btn:link,
.btn:visited{
  text-decoration: none;
  padding: 15px 40px;
  display: inline-block;
  border-radius: 100px;
  transition: all .2s;
}
.btn:hover{
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0,0,0,.2);
}
.btn:active{
  transform: translateY(-1px);
   box-shadow: 0 5px 10px rgba(0,0,0,.2);
}
.btn::after{
  content: '';
  display: inline-block;
  height: 100%;
  width: 100%;
  border-radius: 100px;
  position: absolute;
  top:0;
  left:0;
  z-index: -1;
  transition: all .4s;
}
.btn-white::after{
  background-color: #fff;
}
.btn:hover::after{
  transform:scaleX(1.4) scaleY(1.6);
  opacity: 0;
}
.btn-animated{
  animation: moveInBottom .5s ease-out .75s;
  animation-fill-mode: backwards;
}
```
