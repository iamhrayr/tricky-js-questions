1. understanding `this` in JavaScript
```javascript
function foo() {
    console.log('my name is ' + this.name);
}
var name = 'Samuel';
var obj = { name: 'Sam' };
(obj.foo = foo)();
```


2. object keys are always string 
```javascript
const arrayLikeObj = {
    0: 'zero',
    1: 'one',
};

console.log(Object.keys(arrayLikeObj)[0] === 0);
```

```javascript
const myObject = {};
myObject[{}] = 15;

console.log(myObject[myObject]);
```
