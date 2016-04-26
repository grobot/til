# `async` `await` you know, for prettiness

Promises are catching on. They don't seem like a cureall. A proposal for
a way of handling async code is out there. So enter `async` / `await`

### `async`

A keyword added before function declartions to indciate some async shit
is going to happen here.

### `await`

This seems where shit gets powerful, you are able to write async code
that looks like sync code. Take for example the following promiseified
code:

```
var db = new datorbase('mydb');
db.post({}).then(function (result) { // post a new doc
  return db.get(result.id);          // fetch the doc
}).then(function (doc) {
  console.log(doc);                  // log the doc
}).catch(function (err) {
  console.log(err);                  // log any errors
});
```

followed by the async/await-ified code

```
let db = new datorbase('mydb');
try {
  let result = await db.post({});
  let doc = await db.get(result.id);
  console.log(doc);
} catch (err) {
  console.log(err);
}
```

It takes a minute to get used to. I've developed coping mechanisms for
the state of async code in js and ES5, namely the async module in npm.
It is damn fucking handy and make shit readable as hell. This feels like
a move in the right diection.

Overall a good writeup can be found
[here](https://pouchdb.com/2015/03/05/taming-the-async-beast-with-es7.html).
