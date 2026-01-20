#  Nodejsm Error-Handling

## Description
Error handling is a way to find bugs and solve the as quicly as possible.
Errors in Node can either be **Operational** or **Programmer** error.

## How to deliver Node.js Errors
1. Exceptions
2. Error-first callback
3. Promise Rejection
4. Event Emitters


## Real-Life Use Cases
- Token invalidation
- Batch DB updates
- Reducing round-trip network cost

## Code Example
``` javascript 

// 2. ERROR-FIRST CALLBACK
function square(num: number, callback: Function) {
  if (typeof callback !== "function") {
    throw new TypeError(`Expected a function callback but got: ${typeof num}`);
  }

  setTimeout(() => {
    if (typeof num !== "number") {
      callback(new TypeError(`Expected number but got: ${typeof num}`));
      return;
    }

    const result = num * num;

    callback(null, result);
  }, 1000);
}

square(9, (err: TypeError, data: number) => {
  if (err) {
    return console.log(err);
  }

  console.log(data);
});
```

## What I Learned
Proper error handling is important to keep your apps running and prevent unwanted or premature crashes from your app, hence error handling.
