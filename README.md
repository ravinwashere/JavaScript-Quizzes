# JavaScript-Quizzes

Quiz 1: What's the output? 

```JavaScript
const val = [10, 20, 30, 40, 50];
style="white-space:nowrap;"val.push(val.shift());

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
