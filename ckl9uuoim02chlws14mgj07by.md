## Difference between CSS position property - absolute versus relative

Position property assists in placing an element at a specific spot on the web page. By default, the position takes a static value. What this means is, the element will appear as per the natural flow of the web page. If you intend to move it around from its natural flow, then the static value must be replaced with either absolute or relative. The below sample code snippets will highlight some of CSS position absolute versus relative values.

![first.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1613628036497/dA2eb45qb.png)
*A container div element contains box1, box2 and box3 divs. Box1 div contains box4 and box5 divs.*

All Divs displayed as per their static position.</figcaption></figure></div>The below HTML and CSS code is used to display 5 div boxes within a container div. You will notice, box4 and box5 are within box1, and box1, box2, and box3 are within the container.

```
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Exploring Different Position layouts</title>
    <link type="text/css" rel="stylesheet" href="./Resources/css/index.css">
  </head>
  <body>
    <div id="container">
      Container
      <div id="box1">
        Box1
        <div id="box4">Box4</div>
        <div id="box5">Box5</div>
      </div>
      <div id="box2">Box2</div>
      <div id="box3">Box3</div>
    </div>
  </body>
</html>
```

```
body {
  background-color: black;
  color: white;
  text-transform: uppercase;
  text-align: center;
}

div {
  border: 2px white solid;
}

#container{
  max-width: 100%
  height: auto;
}

#box2,#box3,#box4,#box5 {
  width: 100px;
  height: 100px;
  background-color: green;
}

#box1 {
  width: 250px;
  height: 250px;
  background-color: red;
}
```

Absolute and Relative Positioning
---------------------------------

When an element position is set to relative, it will move the element relative to its current position. Box3 is placed 104px relative to its original positioning. On the other hand, absolute value will move the element relative to its parent ancestor. If it can’t find a relative parent item, the browser will drill up to the next parent and finally will default to the body. This can also be clearly noticed in the next picture, where Box5 can be seen a few inches close to Box4 when compared to Box2 and Box3. Even though both positions are moved equally left to 104px. (Border value is also added to the width).


![second.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1613628133699/Bx5uSYTJs.png)
*Box5 is positioned left using absolute and box3 is moved right using relative.*

CSS code added to make the above change is as follows:

```
#box5 {
  position: absolute;
  left: 104px;
}

#box3 {
  position: relative;
  left: 104px;
}
```

Now let’s move Box4 245px left, relative to the body tag, and Box2 bottom by 104px relative to its original position.

```
#box4 {
  position: absolute;
  left: 254px;
}

#box2 {
  position: relative;
  top: 104px;
}
```

![third.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1613628216296/QVGEn3qnZ.png)
*Box4 and Box2 moved from their original positions.*

One key point to note with both absolute and relative positioning is the offset properties used to move an element. If you intend to move the element right, you should add offset to its left and if you want to move the element left, you should use the right offset property.

Extra Space
-----------

![four.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1613628271332/pQKco9cOF.png)
Move Box2 and Box3 relative to their original positioning.

You will notice by moving Box3 down relative to its original position, the extra space where it is originally supposed to stay is still there. And, this highlights the CSS position absolute versus relative. Change Box3 position value to absolute and the empty space will be removed. This explains how the absolute position removes the element from its normal flow and how the other elements ignore it. In this case, the container div ignores it even though the HTML says Box3 div is within it.

![five.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1613628310380/gUKchgyl7.png)
*Box3 is positioned absolute to its original position.*

CSS used for this change is:

```
#box3 {
  position: absolute;
  bottom: 104px;
}
```

Git link to the HTML and CSS can be found at  [here](https://github.com/narmada-nannaka/Position-Examples)

Hope this post helps with clarifying the differences between absolute and relative position values. Have you observed any other differences, if so leave a comment below?