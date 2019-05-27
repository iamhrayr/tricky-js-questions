1. understanding `this` in JavaScript
```javascript
function foo() {
    console.log('my name is ' + this.name);
}
var name = 'Samuel';
var obj = { name: 'Sam' };

// what is the result?
(obj.foo = foo)();
```

----

2. object keys in JavaScript 
```javascript
const arrayLikeObj = {
    0: 'zero',
    1: 'one',
};

// what is the result?
console.log(Object.keys(arrayLikeObj)[0] === 0);
```

```javascript
const myObject = {};
myObject[{}] = 15;

// what is the result?
console.log(myObject[myObject]);
```
----

3. reasigning object value 
```javascript
const obj = {};
Object.defineProperty(obj, "a", {
    writeable: false,
    value: 25,
});
const obj2 = Object.create(obj);
obj2.a = 16;

// what is the result?
console.log(obj2.a);
```

----

4.  
```javascript
const obj1 = {
    a: 10,
};
const obj2 = Object.create(obj1);
obj2.a++;

// what is the result?
console.log(obj2.a);
console.log(obj1.a);
```
