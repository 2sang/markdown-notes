CSS tips
==========

### Positioned Layout - [Link](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning)
Most tricky part of CSS.

#### 'float' property - [Link](https://developer.mozilla.org/en-US/docs/Web/CSS/float)
Specifies that an element should be placed along the **left or right side** of its container,
allowing text and inline elements to wrap around it.
```css
float: none;
float: left;
float: right;
```

#### 'position' property - [Link](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
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

