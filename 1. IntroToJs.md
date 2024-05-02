## 1.Numbers

``` JavaScript
console.log(5 / 2); // Output: 2.5
```

## 2.Strings
``` JavaScript
let age = 25;
let str1 = 'I am ' + age + " years old ";
console.log(str1); // Output: I am 25 years old


let templateString = `I am ${age} years old`;
console.log(templateString); // Output: I am 25 years old
```

## 3.Null and Undefined:
``` JavaScript
let myNull = null;
let myUndefined;

console.log(myNull); // Output: null
console.log(myUndefined); // Output: undefined
```

## 4.typeof Operator:

``` JavaScript
var a = 10;
console.log(typeof a); // Output: number
a = "string";
console.log(typeof a); // Output: string
a = { "name": "Jasbir" };
console.log(typeof a); // Output: object
```

## 5.typeof null and Array Check:
``` JavaScript
console.log(typeof null); // Output: object

let arr = [1, 2, 3, 4];
console.log(Array.isArray(arr)); // Output: true
```

## Function Definition
``` JavaScript
function fn(param1) {
    console.log("Hello world!", param1);
    return "Returned value";
}

// Function Call
let rVal = fn();

console.log("Return value:", rVal);
```


## Object Definition
``` JavaScript
let cap = {
    name: "Steve",
    age: 34,
    isAvenger: true,
    key: "hello"
}

// Loop through Object Properties
for (let key in cap) {
    console.log(key, " ", cap[key], " ", cap.key);
}
```

## Arrays
``` JavaScript
let arr = [1, 'Scaler', true, undefined, null, [1, 2, 3]]
console.log(arr)
// access an element with index from an array
console.log(arr[4]) // print null

let d=arr[5]
console.log(d) // print [1, 2, 3]
console.log(d[0]) // print 1

//Changing an array element
let arr = [1, 'Scaler', true, undefined, null, [1, 2, 3]]
console.log(arr) // print [1, 'Scaler', true, undefined, null, [1, 2, 3]]

// change an array element to a different value
arr[3] = 'Mrinal'
arr[4] = 700
console.log(arr) //print [1, 'Scaler', true, 'Mrinal', 700, [1, 2, 3]]

//Length of an array
let arr = [1, 'Scaler', true, undefined, null, [1, 2, 3]]
console.log(arr.length) // print 6 as there are a total of 6 elements in an array.
```
