DOM related notes
=================
#### javascript node
javascript nodes are unique. It cannot be copied dynamically by assigning multiple times.
#### cloneNode()
Painted nodes(such as 'canvas'), and inner texts are not cloned. 
If you need deep copy of the element, give "true" to first parameter.
#### removeChild(), replaceChilde()
Think about this, the console says 2, 3, something's wrong.
```javascript

```
#### Remove all children of a dom element
[StackOverflow question](https://stackoverflow.com/questions/3955229/remove-all-child-elements-of-a-dom-node-in-javascript)
```javascript
//Option 1
const myNode = document.getElementById("foo");
myNode.innerHTML = '';
//OPtion 2 - much faster
const myNode = document.getElementById("foo");
while (myNode.firstChild) {
    myNode.removeChild(myNode.firstChild);
}
```

#### How to pass arguments to addEventListener function? - [StackOverflow](https://stackoverflow.com/questions/256754/how-to-pass-arguments-to-addeventlistener-listener-function)
```javascript
let someInput = document.querySelector('input');
someInput.addEventListener('click', myFunc, false);
someInput.myParam = 'This is my parameter';
function myFunc(evt)
{
  window.alert( evt.target.myParam );
}
```



