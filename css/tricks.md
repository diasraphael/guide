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
```

```
<div class='center-box'>
  <div>
    <div>Outdoors<div>
    <div>is where the life starts</div>
  </div>
</div>
```

## spacing between the letters

```
letter-spacing: 35px;
```
