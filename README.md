<div align="center">
  <img height="80" src="https://img.icons8.com/color/480/000000/javascript--v1.png">
  <h1>JavaScript Quizzes</h1>

---
<span>I post everyday JavaScript quiz on my [Twitter](https://twitter.com/ravinwashere) which I'll also post here! Last updated: <a href=#20200612><b>March 11th</b></a> 
</div>

###### 1. What's the output? 

```JavaScript
const val = [10, 20, 30, 40, 50];
val.push(val.shift());

console.log(val);
``` 
<details>
<summary><b>Answer</b></summary>
<p>
Let's break it 

`shift()` → removes the first element and returns the removed element.

`push()` → adds the elements at the end of the array and returns the new length of the array 

`val.shift()` → removes 10
`val.push(10)` → 10 back to array's end

Output: [20, 30, 40, 10]

Credit - [Shan Shah](https://twitter.com/codewithshan)

</p>

</details>

---
###### 2. What's the output? 

```JavaScript
function test() {
    const cat = dog = 123;
}
test()

console.log(typeof cat);
console.log(typeof dog);
``` 

<details>
<summary><b>Answer</b></summary>
<p>

The code start execution from invoked `test` function. so in `test` function, first `123` assigned to `dog` varibale and then the new value of `dog` is assigned to `cat` both value are `123`.

Now if we `console.log(typeof cat)` it should be `undefined` because cat is explicity declred with 'const' keyword which makes it local variable and if the execution of function end the local memory vanished.

`console.log(typeof dog);` → In this line of code should print a `number` because `dog` variable is not explicity declared in the test function. So this becomes a global variable. And global variable can access anywhere. So the output should be `undefined and number`

Answer Credit - [Haroon Hayat](https://twitter.com/hanohayat)

</p>

</details>

---

###### 3. What's the output? 

```JavaScript
let x = 1, y = 2, z = 3;
[x, y, z] = [y, z];

console.log(x, y, z);
``` 

<details>
<summary><b>Answer</b></summary>
<p>

`let x = 1, y = 2, z = 3;` → This line store x = 1, y = 2 and z = 3 in memory. 

`[x, y, z] = [y, z];` → In this like if JavaSScript look square brackets on the lift side of assignment operator "=". Then it will inderstand that it is not array but it it destracturing. 

1. So the value of y which is 2 is assign to x. 
2. Then the value of z which is 3 is assign to y.
3. And there is nothing which is assign to z. So the value of z is undefined. 

`console.log(x, y, z);` → So answer is 2, 3, undefined

Credit - [Haroon Hayat](https://twitter.com/hanohayat)

</p>

</details>

---
###### 4. What's the output? 

```JavaScript
const val = 3 && 2 && 1 && 0 && false;

console.log(val);
```
<details>
<summary><b>Answer</b></summary>
<p>

3 && 2 ==> goes to 2 because 3 is truthy
2 && 1 ==> goes to 1 because 2 is truthy 
1 && 0 ==> goes to 0 because 1 is truthy 
0 && false ==> stays at 0 because it's falsy (&& stops when left side is falsy) 

therefore val = 0 

Credit - [Savvas Stephanides](https://twitter.com/SavvasStephnds)

</p>
</details>

---

###### 5. What's the output? 

```JavaScript
let a = 1 + "1";
let b = 1 + 1;
let c = "1" + "1";

if(a === 2) {
console.log(b);
} else {
  console.log(c);
}
```
<details>

<summary><b>Answer</b></summary>
<p>

`let a - 1 + "1";` → The addition 1 wwith string "1" will convert to "11" string. 

`let b = 1 + 1;` → The addition of two number will be number 2.

`let c = "1" + "1";` → The addition of two string also be string "11".

`if ( a === 2){console.log(b); }else {console.log(c);}` → The condition is checked `(a === 2)` which is wrong because of `a = "11"` so the else block will be execute and print "11" on console screen. 

Credit - [Haroon Hayat](https://twitter.com/hanohayat)
</p>
</details>

###### 6. What's the output? 

```JavaScript
console.log( 'A'  >  'a' )
```

<details>

<summary><b>Answer</b></summary>
<p>

`False` Because the ascii code for ‘A’ is 65 while for ‘a’ it’s 97. 

So basically the code is doing 65>97 which results into a false.

</p>
</details>

###### 7. What's the output? 

```JavaScript
let nums = [5, 10, 20];
let sum = nums[1] + nums.sort()[1];

console.log(sum);
```
<details>

<summary><b>Answer</b></summary>
<p>

Answer is `30`
Dry run:
sum 
→ (1st index from [5,10,20]) + (1st index from [10,20,5])
→ 10 + 20
→ 30

Explanation:

`sort()` without a callback function considers numbers as strings and hence comparing first character based on their ASCII values, gives sorted result as 1,2,5

Credit - [Shubham Sagar Singh](https://twitter.com/shubhamsagarsin)

</p>
</details>

###### 8. What's the output? 

```JavaScript
let a = 4;
let b = 8;

console.log(1%0 + a + b);
```
<details>

<summary><b>Answer</b></summary>
<p>

Answer is `NaN` 

Because, `1%0` will be `NaN`. If one operand of the operation is 'NaN' then, the result will also be `NaN`.

</p>
</details>

###### 8. What's the output? 

```JavaScript
let a1 = ["2", "1", "4", "6"];
let a2 = ["1", "2", "5", "3"];

let val = a1.filter( e => !a2.includes(e) );

console.log(val);
```
<details>

<summary><b>Answer</b></summary>
<p>

Outpit is `["4", "6"]`
Because that line can be seen as the Maths Set operation a1 - a2. Remove all elements from a1 that are also there in a2

</p>
</details>

###### 9. What's the output? 

```JavaScript
function myFunc( ){
  console.log(this.name);
}

myFunc.name = "Ravin";

console.log(myFunc( ));
```
<details>

<summary><b>Answer</b></summary>
<p>

Output is `undefined`

4 ways to bind `this`:

1. The `new` keyword (doesn't apply)
2. Explicit binding (doesn't apply)
3. Default binding (applies here)✅
4. Implicit binding (calling from obj prop)

When default binding, `this` references the global scope. 

In this case, `name` is a property of `myFunc`, not the global object.

`global.name` === undefined
`this.name` === `global.name`

Also, `Function.name` is a read-only property, so even if this worked, the answer would not be 'Ravin'
</p>
</details>

###### 10. What's the output? 

```JavaScript
const websites = ['youtube', 'udemy'];

websites.length = 0;

console.log(websites[0]);
```
<details>

<summary><b>Answer</b></summary>
<p>

`Undefined`

Setting the length of an array is the same as making it empty so when you try to access the first element it'll be undefined cause it's []

</p>
</details>

###### 11. What's the output? 

```JavaScript
const string = "Hello developers";

console.log(string.substring(16, 6));
```
<details>

<summary><b>Answer</b></summary>
<p>

substring() method in JavaScript extract characters, between two indies.
(Note: last index is exclusive.)

If start index is greate than end, arguments are swapped.
E.g:: (16, 6) == (6, 16)
So, 
Starting from 6 index to 16 and it will print
`developers`

Credit - [Haroon Hayat](https://twitter.com/hanohayat)

</p>
</details>

###### 11. What's the output? 

```JavaScript
const arr1 = ['x', 'y', 'z'];
const arr2 = ['y', 'z', 'x'];

console.log(
  arr1.sort() === arr1, 
  arr2.sort() === arr2,
  arr1.sort() === arr2.sort()
);
```
<details>

<summary><b>Answer</b></summary>
<p>

`const arr1 = ['x', 'y', 'z'];` → arr1 is independent Object.
`const arr2 = ['y', 'z', 'x'];` → arr2 is also independent Object.

The comparison between two object will return `TRUE`, if both of object point to the same memory location otherwise they will return `FALSE`.

`console.log(`

  `arr.sort() === arr1` → `TRUE`, because both object are refernce to the memory location(both are arr1).

  `arr2.sort() == arr2` → `TRUE`, again because both object are reference to same memory.

  `arr1.sort() === arr2.sort()` → `FALSE`, because both object are differnt, and object comparison done through memory location. (arr1 !== arr2).

`);`

Credit - [Haroon Hayat](https://twitter.com/hanohayat)

</p>
</details>

###### 11. What's the output? 

```JavaScript
const a = null;
const b = (a ?? ('1' == 1));

console.log(b);
```
<details>

<summary><b>Answer</b></summary>
<p>



Credit - [Haroon Hayat](https://twitter.com/hanohayat)

</p>
</details>

<br>

