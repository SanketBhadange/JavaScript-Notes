Difference between let var const
# Scope	

var: Accessible within entire function or globally (if outside functions).	
```Javascript 
function func() { 
var x = 10; 
if (true) { var y = 20; }
console.log(x); // Accessible (10) 
console.log(y); // Accessible (20) }
func();
console.log(x); // Also accessible globally (10, if not redefined elsewhere)
```
let and const: 
Accessible only within the block they are declared in.	
```Javascript 
function func() {
let x = 10; 
if (true) { 
const y = 20; } 
console.log(x); // Accessible (10)
console.log(y); // Accessible (20) //
Error: ReferenceError: y is not defined (outside its block) } 
func();
```
# Reassignment	

var: 
Can be re-declared and updated within its scope.	
```Javascript 
var x = 10; 
x = 20; 
console.log(x); // 20 (updated value)
```
let:
Can be updated within its scope, but cannot be re-declared.	
```Javascript  
let x = 10;
x = 20; 
console.log(x); // 20 (updated value) 
let x = 30; // Error: Identifier 'x' has already been declared
```
const:
Must be assigned a value at declaration, then cannot be changed.	
```Javascript  
const x = 10;
x = 20; // Error: Assignment to constant variable
```
# Hoisting

var: Variables are hoisted to the top of their scope (can be accessed before declaration, but value is undefined).	
```Javascript  
console.log(x); // undefined (var is hoisted but not initialized)
var x = 10;
console.log(x); // 10
```
let and const:
Not hoisted, cannot be accessed before declaration.	
```Javascript  
console.log(x); // ReferenceError: Cannot access 'x' before initialization (not hoisted) 
let x = 10;
```
Best Practice in ES6+	const by default for variables that don't need to be reassigned (makes code predictable).	

```Javascript  
const PI = 3.14159; // Constant value
let message = "Hello"; // Can be reassigned if needed
```
