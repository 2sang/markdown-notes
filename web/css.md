CSS tips
==========
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
#### javascript node
javascript nodes are unique. It cannot be copied dynamically by assigning multiple times.
#### cloneNode()
Painted nodes(such as 'canvas'), and inner texts are not cloned. 
If you need deep copy of the element, give "true" to first parameter.
#### Vim replace


