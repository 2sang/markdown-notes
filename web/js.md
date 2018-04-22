Things worth knowing - Javascript(ES6)
--------------------------------------

#### Caution - 'async, await'
Recently I wasted four hours of my time because of my poor understanding of ES6 async syntax.  
Feel free to guess my mistake, And the code was:
```javascript
async function timeConsumingFunction(param) {
    await anotherPromiseFunction(param)
}

const resultObject = timeConsumingFunction(myParam);
resultObject.itsMethod(10);
```
Did you notice?

As you might notice the pitfall when I try to assign resultObject as the return of timeConsumingFunction(),  
**I should have blocked the code before I call itsMethod(), since the function returns object is expected to be time consuming.**  
I completely forgot, and naturally the console in browser repeatedly said "theres no such function 'itsMethod()' in resultObject, idiot". Yes, apparently resultObject tried to call the method  
which doesn't even exist yet. And I've never thought this was async problem. Oh boy. 

