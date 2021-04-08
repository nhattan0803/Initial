# Initial
Initial Repository
**Hoisting**
	Hoisting is a Javascript mechanism where variables and function declarations are moved to top of their scope before code execution, same with the function.
	
	```js
	 function hoisting (){
	 	console.log(a);
	 	var a = "Hello world!"
	 }
	 ///Result: undefined
	```
	
	*Because The variable declaration is hoist in the top of function, but the initialise is not change*

**Scope and Closure**
	- Scope: When we declare a variable in a function, we can only access it in the function. These variable are call to be scoped to the function. There are 2 types of scopes in javascript: Global scope(block scope) and local scope(function scope)
	- Closure: If we define any inner function within another function, this inner function is called a closure. It retains access to the variables created in the outer function.
	*Example:*
	```js
	var countNumbmer = (()=> {
		var counter = 0;
		return function() {
			counter += 1;
			return counter;
		}
	});
	```
**Object, Prototype & Inheritance**
	- Object is collection of properties(an association between a name and a value)
	- Propotype: All objects inherit properties and methods from a prototype
	*Example*
	```js
		function obj(x, y, z){
			this.x = x;
			this.y = y;
			this.z = z;
		}
		newObj = new obj(1, 2, 3);
	```
	- Inheritance: It refers to an object's ability to access methods and other properties from another object. Objects can inherit things from other objects.
	*Example*
	```js
		class Game{
			constructor(name){
				this.gameName = name;
			}
			get gname(){
				return this.gameName;
			}
			set gname(x){
				this.gameName = x;
			}
		}
		let newGame = new game("LOL");
	```
**Condition statement** 
	- Use if to specify a block of code to be executed, if a specified condition is true.
	```js
	if(condition){
		...
	}
	else if{
		...
	}
	else{
		...
	}
	```
	- Else to specify a block of code to be executed, if the same condition is false.
	- Else if to specify a new condition to test, if the first condition is false
	- Switch to specify manny alternative blocks of code to be executed
**Data type**
	|Data Types|Description|Example|
	|---|---|---|
	|String	|textual data|'Hello world!'|
	|Number|An interger or a floating-point number|3; 3.14;...|
	|BigInt|An interger with arbitrary precision|1n,...|
