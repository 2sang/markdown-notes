Things worth knowing - Javascript(ES6)
--------------------------------------


Recently I wasted three hours of my time because of my stupid understanding.  
And it was, 
```javascript
async function timeConsumingFunction(param) {
    await anotherPromiseFunction(param)
}

resultObject = timeConsumingFunction(myParam);
resultObject.itsMethod(10);
```
As you might noticed the pitfall of this code, resultObject should have blocked the code 
Until it gets proper return object. I completely forgot, and obviously the console in browser  
repeatedly says "theres no such a function 'isMethod' in resultObject, idiot".
I've never thought this was async problem. Oh boy. 

