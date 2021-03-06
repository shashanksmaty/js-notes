# Converting Object to Array

### Object.keys()

The **Object.keys()** method returns an array of a given object's own property name, in the same order of the normal loop.

For example:-

```javascript
const object1 = {
  a: "foo",
  b: "bar"
};
console.log(Object.keys(object1));
// output: Array ["a", "b"]
```

### Object.values()

The **Object.values()** method returns an array of a given object's own property value.

For example:-

```javascript
const object1 = {
  a: "foo",
  b: "bar"
};
console.log(Object.values(object1));
// output: Array ["foo", "bar"]
```

**Convert Object to Array**

To convert object to array, we will use Object.keys() method.

```javascript
const object1 = {
  a: "foo",
  b: "bar"
};
const objToArr = Object.keys(object1).map(key => {
  return {
    [key]: object1[key]
  }
});
console.log(objToArr);
/* output
Array [{a: "foo"}, {b: "bar"}] */
```