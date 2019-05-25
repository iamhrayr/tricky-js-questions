
```javascript
// question 1 (understanding about this)

function foo() {
    console.log('my name is ' + this.name);
}
var name = 'Samuel';
var obj = { name: 'Sam' };
(obj.foo = foo)();
```
