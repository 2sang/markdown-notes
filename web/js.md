Things worth knowing - Javascript(ES6)
--------------------------------------

#### * Caution - 'async, await'
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

<br></br>
#### * How to handle pause, play feature using ES6 async, await syntax & infinity loop only
```javascript
let pause = false;

/* This function is called with await, and it won't be returned 
   until pause value is changed. It polls every 50 miliseconds 
   to see if the variable changes.
*/
async function resumeCheck() {
    while (true) {
        let promise = new Promise(resolve => {
            setTimeout(() => {
                if (!pause) {
                    resolve(true);
                } else {
                    resolve(false);
                }
            }, 50);
        });
        resolved = await promise;
        if (resolved) break;
    }
}

// we want this function runs forever, unless the pause is activated.
async function infLoopEverySecond(func) {
    while (true) {
        let promise = new Promise(resolve => {
            setTimeout(() => {
                func();
                resolve();
            }, 1000);
        });
        let result = await promise;
        await resumeCheck();
    }
}

// Keep yelling every second.
async function yelling() {
    console.log("yell!");
}
infLoopEverySecond(yelling);


// Let's see what the output shows.
// we'll hit pause in 1.4 seconds after the program starts.
setTimeout(() => {
    pause = true;
}, 1400);

// After that, we'll resume the program in another 1.3 seconds.
setTimeout(() => {
    pause = false;
}, 2700);
```
Can you believe that I've put my whole day for this damn play/pause script? lol


