# JavaScript-Quizzes

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

Answer Credit - [Shan Shah](https://twitter.com/codewithshan)

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

Answer Credit - [Haroon Hayat](https://twitter.com/hanohayat)

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

Answer Credit - [Savvas Stephanides](https://twitter.com/SavvasStephnds)

</p>
</details>

---