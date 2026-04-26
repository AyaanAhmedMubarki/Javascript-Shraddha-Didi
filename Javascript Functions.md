---


---

<h1 id="javascript-–-shraddha-didi"><strong>JAVASCRIPT – Shraddha Didi</strong></h1>
<h2 id="lecture-5-functions-and-methods"><strong>Lecture 5: Functions and Methods</strong></h2>
<hr>
<h2 id="functions-in-javascript"><strong>1. Functions in JavaScript</strong></h2>
<p>👉 A <strong>Function</strong> is a block of code that performs a <strong>specific task</strong>.<br>
Functions help to <strong>avoid repetition</strong> and improve <strong>code reusability</strong>.</p>
<h3 id="examples-of-built‑in-functions"><strong>Examples of Built‑in Functions</strong></h3>
<p>console.log(“hello”);</p>
<p>“abc”.toUpperCase();</p>
<p>[1, 2, 3].push(4);</p>
<p>✅ Each function performs its own specific task.</p>
<hr>
<h2 id="creating-user‑defined-functions"><strong>2. Creating User‑Defined Functions</strong></h2>
<h3 id="step-1-function-definition"><strong>Step 1: Function Definition</strong></h3>
<p>function functionName() {</p>
<p>// do some task</p>
<p>}</p>
<p>With parameters:</p>
<p>function functionName(param1, param2) {</p>
<p>// do some task</p>
<p>}</p>
<hr>
<h3 id="step-2-function-call"><strong>Step 2: Function Call</strong></h3>
<p>functionName();</p>
<p>functionName(arg1, arg2);</p>
<hr>
<h2 id="return-statement--scope"><strong>3. return Statement &amp; Scope</strong></h2>
<h3 id="important-notes"><strong>Important Notes</strong></h3>
<p>function Add(x, y) {</p>
<p>let s = x + y;</p>
<p>console.log(s);</p>
<p>return;</p>
<p>console.log(“After return”); // unreachable code</p>
<p>}</p>
<p>➡️ Code written <strong>after <code>return</code> is not executed</strong>.</p>
<hr>
<h3 id="local-scope-example"><strong>Local Scope Example</strong></h3>
<p>function sum(x, y) {</p>
<p>let s = x + y; // local variable</p>
<p>console.log(s);</p>
<p>return s;</p>
<p>}</p>
<p>let val = sum(3, 4);</p>
<p>❌ Not allowed:</p>
<p>console.log(s); // Error: s is local to function</p>
<p>✅ Allowed:</p>
<p>console.log(val);</p>
<hr>
<h2 id="arrow-functions"><strong>4. Arrow Functions</strong></h2>
<p>👉 A <strong>shorter and cleaner way</strong> to write functions.</p>
<h3 id="syntax"><strong>Syntax</strong></h3>
<p>const funcName = (param1, param2) =&gt; {</p>
<p>// do some task</p>
<p>};</p>
<h3 id="example"><strong>Example</strong></h3>
<p>const sum = (x, y) =&gt; {</p>
<p>return x + y;</p>
<p>};</p>
<p>sum(3, 4);</p>
<p>✅ Output:</p>
<pre><code>7

</code></pre>
<hr>
<h2 id="practice-question-–-vowel-counter"><strong>5. Practice Question – Vowel Counter</strong></h2>
<h3 id="q1-count-vowels-using-function-keyword"><strong>Q1: Count Vowels using Function Keyword</strong></h3>
<p>function countVowels(s) {</p>
<p>let count = 0;</p>
<p>s = s.toLowerCase();</p>
<p>for (let i = 0; i &lt; s.length; i++)<br>
{</p>
<p>if (</p>
<p>s.charAt(i) === ‘a’ ||</p>
<p>s.charAt(i) === ‘e’ ||</p>
<p>s.charAt(i) === ‘i’ ||</p>
<p>s.charAt(i) === ‘o’ ||</p>
<p>s.charAt(i) === ‘u’</p>
<p>)<br>
{</p>
<p>count++;</p>
<p>}</p>
<p>}</p>
<p>return count;</p>
<p>}</p>
<hr>
<h3 id="same-logic-using-for‑of-loop"><strong>Same Logic using for‑of Loop</strong></h3>
<p>function countVowels(s) {</p>
<p>let count = 0;</p>
<p>s = s.toLowerCase();</p>
<p>for (let char of s) {</p>
<p>if (</p>
<p>char === ‘a’ ||</p>
<p>char === ‘e’ ||</p>
<p>char === ‘i’ ||</p>
<p>char === ‘o’ ||</p>
<p>char === ‘u’</p>
<p>)<br>
{</p>
<p>count++;</p>
<p>}</p>
<p>}</p>
<p>return count;</p>
<p>}</p>
<hr>
<h3 id="q2-count-vowels-using-arrow-function"><strong>Q2: Count Vowels using Arrow Function</strong></h3>
<p>const countVow = (s) =&gt; {</p>
<p>let count = 0;</p>
<p>s = s.toLowerCase();</p>
<p>for (let char of s) {</p>
<p>if (</p>
<p>char === ‘a’ ||</p>
<p>char === ‘e’ ||</p>
<p>char === ‘i’ ||</p>
<p>char === ‘o’ ||</p>
<p>char === ‘u’</p>
<p>)<br>
{</p>
<p>count++;</p>
<p>}</p>
<p>}</p>
<p>return count;</p>
<p>};</p>
<hr>
<h2 id="foreach-loop-in-arrays"><strong>6. forEach Loop in Arrays</strong></h2>
<p>👉 Executes a function once for <strong>each element of array</strong>.</p>
<h3 id="syntax-1"><strong>Syntax</strong></h3>
<p>arr.forEach(callbackFunction);</p>
<p>👉 <strong>Callback Function</strong><br>
A function passed as an <strong>argument</strong> to another function.</p>
<p>✅ JavaScript allows passing functions as parameters.</p>
<hr>
<h3 id="callback-parameters"><strong>Callback Parameters</strong></h3>
<p>arr.forEach((value, index, array) =&gt; {</p>
<p>// task</p>
<p>});</p>
<hr>
<h3 id="examples"><strong>Examples</strong></h3>
<h4 id="example-1">Example 1</h4>
<p>let arr = [1, 2, 3, 4, 5];</p>
<p>arr.forEach(function printVal(val) {</p>
<p>console.log(val);</p>
<p>});</p>
<hr>
<h4 id="example-2">Example 2</h4>
<p>let cities = [“pune”, “Kolkata”, “Chennai”];</p>
<p>cities.forEach((val) =&gt; {</p>
<p>console.log(val.toUpperCase());</p>
<p>});</p>
<hr>
<h4 id="example-3">Example 3</h4>
<p>cities.forEach((val, idx, arr) =&gt; {</p>
<p>console.log(val.toUpperCase());</p>
<p>});</p>
<hr>
<h2 id="higher-order-functions"><strong>7. Higher Order Functions</strong></h2>
<p>👉 <strong>Higher Order Functions</strong> are functions that:</p>
<ul>
<li>Take another function as parameter <strong>OR</strong></li>
<li>Return a function</li>
</ul>
<p>✅ Example:</p>
<p>forEach()</p>
<p>map()</p>
<p>filter()</p>
<p>reduce()</p>
<hr>
<h2 id="practice-question-–-foreach"><strong>8. Practice Question – forEach</strong></h2>
<h3 id="print-square-of-each-number"><strong>Print Square of Each Number</strong></h3>
<h4 id="method-1">Method 1</h4>
<p>let nums = [1, 2, 3, 4, 5];</p>
<p>nums.forEachnum) =&gt; {</p>
<p>console.log(num * num);</p>
<p>});</p>
<h4 id="method-2">Method 2</h4>
<p>let nums = [1, 2, 3, 4, 5];</p>
<p>let calcSquare = (num) =&gt; {</p>
<p>console.log(num * num);</p>
<p>};</p>
<p>nums.forEach(calcSquare);</p>
<hr>
<h2 id="more-array-methods"><strong>9. More Array Methods</strong></h2>
<hr>
<h2 id="map"><strong>map()</strong></h2>
<p>👉 Creates a <strong>new array</strong> by applying operations on each element.</p>
<p>let arr = [1, 2, 3];</p>
<p>let newArr = arr.map((val) =&gt; {</p>
<p>return val * val;</p>
<p>});</p>
<p>✅ Output:</p>
<pre><code>[1, 4, 9]

</code></pre>
<hr>
<h2 id="filter"><strong>filter()</strong></h2>
<p>👉 Returns a <strong>new array</strong> with elements that satisfy a condition.</p>
<h3 id="example-filter-even-numbers"><strong>Example: Filter Even Numbers</strong></h3>
<p>let arr = [1,2,3,4,5,6,7,8,9];</p>
<p>let newArr = arr.filter((val) =&gt; {</p>
<p>return val % 2 === 0;</p>
<p>});</p>
<p>✅ Output:</p>
<pre><code>[2, 4, 6, 8]

</code></pre>
<hr>
<h2 id="reduce"><strong>reduce()</strong></h2>
<p>👉 Reduces array to a <strong>single value</strong>.</p>
<h3 id="example-1-sum-of-elements"><strong>Example 1: Sum of Elements</strong></h3>
<p>const arr = [1, 2, 3, 4];</p>
<p>const output = arr.reduce((result, curr) =&gt; {</p>
<p>return result + curr;</p>
<p>});</p>
<p>console.log(output);</p>
<p>✅ Output:</p>
<pre><code>10

</code></pre>
<hr>
<h3 id="example-2-largest-number"><strong>Example 2: Largest Number</strong></h3>
<p>const arr = [1, 2, 3, 4];</p>
<p>const largest = arr.reduce((prev, curr) =&gt; {</p>
<p>return prev &gt; curr ? prev : curr;</p>
<p>});</p>
<p>console.log(largest);</p>
<p>✅ Output:</p>
<pre><code>4

</code></pre>
<hr>
<h2 id="practice-questions"><strong>10. Practice Questions</strong></h2>
<hr>
<h3 id="q1-filter-marks--90"><strong>Q1: Filter Marks &gt; 90</strong></h3>
<p>let marks = [80, 79, 92, 99, 100, 77, 65];let marks = [80, 79, 92, 99, 100, 90;</p>
<p>});</p>
<p>console.log(newArr);</p>
<p>let newArr = marks.filter((val) =&gt; {</p>
<p>✅ Output:</p>
<pre><code>[92, 99, 100]

</code></pre>
<hr>
<h3 id="q2-sum--product-using-reduce"><strong>Q2: Sum &amp; Product using reduce()</strong></h3>
<p>let n = prompt(“Enter a number:”);</p>
<p>let arr = [];</p>
<p>for (let i = 0; i n; i++) {</p>
<p>arr[i] = i + 1;</p>
<p>}</p>
<p>let sum = arr.reduce((res, curr) =&gt; {</p>
<p>return res + curr;</p>
<p>});</p>
<p>console.log(“Sum:”, sum);</p>
<p>let product = arr.reduce((res, curr) =&gt; {</p>
<p>return res * curr;</p>
<p>});</p>
<p>console.log(“Product:”, product);</p>
<hr>

