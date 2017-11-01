1. Callback Functions: Function can be passed around just like anything else. A callback function is a function that is passed to another function as a parameter. When that function is called, the callback function can be called inside that function. 

2. Closure: This is a hard one. It is a function(let's call it innerFunction) returned from another function (let's call it outerFunction). The innerFunction knows and has access to everything inside the outerFunction when it is created. 

3. Arguments: Arguments are several values that are passed to a function in the form of an array-like object. In the object, the frist entry's index starting at 0. For example, we can say arguments[0], or arguments[1]... we can also determine the number of passed vaules by asking arguments.length.

4. Recursion: Recursion is a self referring process. A recursive function is a function that calls itself inside the function body. You will always need a control statment that allows the function to exit the recursive loop, for example, an "if" statement.

5. Prototype: Any object in javascript has a private link to another object which is called the prototype of the object. The properties of the prototype will be available for this object. 

6. Constructors: Constructors are functions that can be used to creat a new object using the operator "new".

For 5 and 6, I tried this example.

function C() {
	this.name = "name";
}                             //If I ask what C.prototype is, I will get {}. It is an empty object.

var x = new C(); 
C.prototype.sayHi = function() {
	console.log ("hi");
}                           //when I do this, if I ask what C.prototype is, I got "C {sayHi: [function]}". It is not empty anymore


x.sayHi();        //If I do this, I got "hi" printed.
