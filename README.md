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
