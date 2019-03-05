# Functional JavaScript


## 클로저(closure)
```javascript
function splat (func) {
  return function (array) {
    func.apply(null, array);
  };
}

var addArrayElements = splat(function (x, y) { return x + y });

addArrayElements([1, 2]);
// => 3
```