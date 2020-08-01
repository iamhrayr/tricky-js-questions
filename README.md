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

----

5.  
```javascript
const func = async () => {
    return true;
};

// what is the result?
console.log(typeof func());
```

----

6.  
```javascript
// what is the result?
console.log(019 - 016);
```

----

7.
```javascript
const a = a => a;

// what is the result?
console.log(a(10));
```

----

8.
```javascript
// what is the result?
console.log(Math.max() > Math.min());
```

----

9.
```javascript
var count = 0;
for (var i = 0.1; i % 0.1 === 0; i += 0.1) {
    count++;
}

// what is the result?
console.log(count);
```

----

10.
```javascript
console.log(x == 1 && x == 2 && x == 3) // true

// what is the value of x?
```

----

11. What's the order of the logged messages
```javascript
const asyncFn = () => {
    return new Promise((resolve) => {
        console.log('I am in promise')
        resolve()
    })
}

asyncFn()
console.log('I am outside')
```

----

12. 
```javascript
console.log(a == !a) // true
// what is the value of a?
```

----

13. 
```javascript
(function() {
  console.log(typeof this);
}).call(10)
```

----

14. 
```javascript
console.log(value !== value) // true
// what is the value?
// NaN
```

----

15. 
`{} + '1'` and `'1' + {}` return different results, explain why
```
