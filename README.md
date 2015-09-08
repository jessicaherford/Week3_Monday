# Outline for Monday, September 28th
- Operators
- Loops
- If..else statements
- Switches

##Decision making
There are often several places in a script where decisions are made to determine which lines of code should be run next. There are two components to a decision:
<br>
<br>
1: An expression is evaluated, which returns a value.
<br>
<br>
2: A conditional statement says what to do in a given situation.
<br>
<br>
'Comparison operators' and `logical operators` are used to determine the next path of your code.

##Evaluation of a Condition

##Comparison Operators
In any condition, there is usually one operator and two operands. The operands are placed on either side of the operator, and can be `values` or `variables`. Brackets are used to enclose the expression.
<br>
<br>
- >
- '>='
- <
- <=
- ==
- !=
- ===
- !==

Operands do not have to be a single `value` or `variable` name. An operand can also be an `expression` (each expression evaluates to a single value).
- Code here

##Logical Operators
Comparison operators usually return single values of `true` or `false`. Logical operators allow you to compare the results of multiple comparison operators.
<br>
<br>
- &&
- ||
- !

##Conditional Statements

The `if` statement evaluates a condition. If the condition is `true`, any statements in the subsequent block of code will be executed.
```javascript
var score = 75;

if (score >= 50) {
  var message = 'Congrats! You passed!';
}

console.log(message);
```
So...what if your score was below 50?
```javascript
var score = 45;

var congratulate = function(){
  console.log('You passed!');
};

var encourage = function(){
  console.log('Not quite..practice makes perfect.')
};

if (score >= 50) {
  congratulate();
}

else {
  encourage();
}
//If the score is below 50, the encourage function will be called.
```
Often times, there are more than one outcome when evaluating a condition. The `if..else` statement provides an alternate path if the condition isn't met. If it resolves to 'true', the first block of code will be executed. If the condition resolves to false, the second block of code is run instead.

##Switch Statements
`Switch` statements are used to execute code when a variable matches a particular value. A `switch` statement starts with a variable called the `switch value`. Each `case` indicates a possible value and the code that should be run if the the 'switch value' matches the `case value`.
<br>
<br>
If the 'switch value' does not match the value of any `case`, the `default` case will be executed. At the end of every `case` is a `break` keyword. This tells the JavaScript interpreter that the `switch` statement is complete, and to proceed with any subsequent code.
```javascript
var level = 2;

switch(level) {
  case 1:
    var message = 'You have arrived on floor 1';
    break;
  case 2:
    var message = 'You have arrived on floor 2';
    break;
  case 3:
    var message = 'You have arrived on floor 3';
    break;
  default:
    var message = 'That floor does not exist!';
    break;
}

console.log(message);
```
Switches are useful if you're looking for a particular value. Though you could use multiple if statements, they will all be evaluated even if a match is found, making your code slower than if you had used a `switch` instead.

##Loops
Loops also check for conditions. If a `loop` returns `true`, the block of code will run. The condition will then be checked again and if it still returns `true`, the block of code will run again. The `loop` will repeat itself until the condition returns `false`.

###For Loops
The 'for' loop is the most common loop you'll see in JavaScript, and is used if you need the code to run a specific amount of times. The condition is usually a `counter` that specifies how many times the loop should run.

```javascript
for(i=0;i<10,i++) {
  console.log(i);
}
//What will the output be to the console??
```
Counting is great, but the `for` loop is most often used to iterate through the items of an array.
```javascript
var animals = ['duck', 'cow', 'goat', 'pig']; //array of animals
var animalCount = animals.length; //total number of items in array
for(i=0;i<animalCount;i++) { //the first position in an array is 0 so we set i equal to it
  var animal = animals[i];//finds the animal at position i
  console.log(animal);//logs the animal to the console
}
//What will the output be to the console??
```

###While Loops

###Do While Loops
