CSS tips
==========

### Basic Selector - [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors)

### Positioned Layout - [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning)
Most tricky part of CSS.

#### 'float' property - [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/float)
Specifies that an element should be placed along the **left or right side** of its container,
allowing text and inline elements to wrap around it.
```css
float: none;
float: left;
float: right;
```

#### 'position' property - [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
default: static
```css
position: static;
position: relative;
position: absolute;
```

### Others
#### Calculating size of elements - "box-sizing"
box-sizing: How browser calculates the total width and height.
```css
box-sizing: content-box; /*default*/
```
#### Display Property
```css 
display: inline-block;
```
Initial value of property display is 'inline'. It gives its child elements 
#### horizontal scrolling
```css 
.horizontal-scroll-wrapper {
    width: 100px;
    height: 300px;
    overflow-y: auto;
    overflow-x: hidden;
}
```
Another solution is, rotate the whole container to counter, or clockwise.
check out this [Link](http://css-tricks.com/pure-css-horizontal-scrolling)

#### Make innerText vertically centered? - [StackOverflow](https://stackoverflow.com/questions/9249359/is-it-possible-to-vertically-align-text-within-a-div)
```css 
#column-content {
  display: inline-block;
}
img {
  vertical-align: middle;
}
span {
  display: inline-block;
  vertical-align: middle;
}

/* for visual purposes */
#column-content {
  border: 1px solid red;
  position: relative;
}
```

#### Make two divs are placed next to each other - [StackOverflow](https://stackoverflow.com/questions/5803023/how-to-place-two-divs-next-to-each-other)
```css
#wrapper {
    width: 500px;
    border: 1px solid black;
    overflow: hidden; /* will contain if #first is longer than #second */
}
#first {
    width: 300px;
    float:left; /* add this */
    border: 1px solid red;
}
#second {
    border: 1px solid green;
    overflow: hidden; /* if you don't want #second to wrap below #first */
}

/* or */ 

#wrapper {
    width: 500px;
    border: 1px solid black;
    overflow: hidden; /* add this to contain floated children */
}
#first {
    width: 300px;
    float:left; /* add this */
    border: 1px solid red;
}
#second {
    border: 1px solid green;
    float: left; /* add this */
}
```

#### Use '&&, ||' operator - [StackOverflow](https://stackoverflow.com/questions/2797091/css-and-and-or),
```css
<div class="class1 class2"></div>

/*This works as AND */
div.class1.class2
{
  /* foo */
}

<div class="class1"></div>
<div class="class2"></div>

/*And this works as OR */
div.class1,
div.class2
{
  /* foo */
}
```

#### Blur effect - [Codepen](https://codepen.io/anthonyadamski/pen/yJBpd)





