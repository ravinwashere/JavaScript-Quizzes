# JavaScript-Quizzes

Quiz 1: What's the output? 

```JavaScript
const val = [10, 20, 30, 40, 50];
val.push(val.shift());

console.log(val);
``` 
<details>
<summary>Answer</summary>
Let's break it 

<code style="white-space:nowrap;">shift()</code> removes the first element and returns the removed element.

<code style="white-space:nowrap;">push()</code> adds the elements at the end of the array and returns the new length of the array 

<code style="white-space:nowrap;">val.shift()</code> -> removes 10
<code style="white-space:nowrap;">val.push(10)</code> -> 10 back to array's end

Output: [20, 30, 40, 10]

Answer Credit - [Shan Shah](https://twitter.com/codewithshan)

</details>

Quiz 2: What's the output? 

```JavaScript
function test() {
    const cat = dog = 123;
}
test()

console.log(typeof cat);
console.log(typeof dog);
``` 

<details>
<summary>Answer</summary>
The code start execution from invoked <code style="white-space:nowrap;">"test"</code> function. so in <code style="white-space:nowrap;">"test"</code> function, first <code style="white-space:nowrap;">123</code> assigned to <code style="white-space:nowrap;">dog</code> varibale and then the new value of <code style="white-space:nowrap;">dog</code> is assigned to <code style="white-space:nowrap;">cat</code> both value are <code style="white-space:nowrap;">123</code>.
<br/>
<br/>
Now if we <code style="white-space:nowrap;">console.log(typeof cat);</code> it should be <code style="white-space:nowrap;">undefined.</code> because cat is explicity declred with 'const' keyword which makes it local variable and if the execution of function end the local memory vanished.
<br/>
<br/>
<code style="white-space:nowrap;">console.log(typeof dog);</code> → In this line of code should print a <code style="white-space:nowrap;">number</code> because <code style="white-space:nowrap;">dog</code> variable is not explicity declared in the test function. So this becomes a global variable. And global variable can access anywhere. So the output should be <code style="white-space:nowrap;">undefined and number</code>

Answer Credit - [Haroon Hayat](https://twitter.com/hanohayat)

</details>

Quiz 3: What's the output? 

```JavaScript
let x = 1, y = 2, z = 3;
[x, y, z] = [y, z];

console.log(x, y, z);
``` 

<details>
<summary>Answer</summary>
<code style="white-space:nowrap;">let x = 1, y = 2, z = 3;</code> → This line store x = 1, y = 2 and z = 3 in memory. 
<br/>
<code style="white-space:nowrap;">[x, y, z] = [y, z];</code> → In this like if JavaSScript look square brackets on the lift side of assignment operator "=". Then it will inderstand that it is not array but it it destracturing. 

1. So the value of y which is 2 is assign to x. 
2. Then the value of z which is 3 is assign to y.
3. And there is nothing which is assign to z. So the value of z is undefined. 

<code style="white-space:nowrap;">console.log(x, y, z);</code> → So answer is 2, 3, undefined

Answer Credit - [Haroon Hayat](https://twitter.com/hanohayat)
</details>

Quiz 4: What's the output? 

```JavaScript
const val = 3 && 2 && 1 && 0 && false;

console.log(val);
```
<details>
<summary>Answer</summary>
3 && 2 ==> goes to 2 because 3 is truthy  <br>
2 && 1 ==> goes to 1 because 2 is truthy  <br>
1 && 0 ==> goes to 0 because 1 is truthy  <br>
0 && false ==> stays at 0 because it's falsy (&& stops when left side is falsy)  <br>
<br>
therefore val = 0  <br>

Answer Credit - [Savvas Stephanides](https://twitter.com/SavvasStephnds)
</details>