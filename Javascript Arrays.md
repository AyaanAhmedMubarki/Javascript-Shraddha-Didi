---


---

<h1 id="javascript-–-shraddha-didi"><strong>JAVASCRIPT – Shraddha Didi</strong></h1>
<h2 id="lecture-3-arrays"><strong>Lecture 3: Arrays</strong></h2>
<hr>
<h2 id="arrays-in-javascript"><strong>1. Arrays in JavaScript</strong></h2>
<p>👉 <strong>Arrays</strong> are a <strong>collection of items</strong> stored in a single variable.</p>
<hr>
<h2 id="creating-an-array"><strong>Creating an Array</strong></h2>
<h3 id="syntax"><strong>Syntax</strong></h3>
<p>let arr = [item1, item2, item3];</p>
<h3 id="example"><strong>Example</strong></h3>
<p>let marks = [97, 82, 75, 64, 32];</p>
<p>✅ In JavaScript, arrays can store <strong>mixed data types</strong>, but it is <strong>not preferred</strong>.</p>
<p>let info = [“1002”, “Ravi”, 25000]; // Allowed but not recommended</p>
<hr>
<h2 id="length-of-an-array"><strong>Length of an Array</strong></h2>
<p>arr.length;</p>
<h3 id="example-1"><strong>Example</strong></h3>
<p>let marks = [97, 82, 75];</p>
<p>console.log(marks.length);</p>
<p>✅ Output:</p>
<pre><code>3

</code></pre>
<hr>
<h2 id="important-note"><strong>Important Note</strong></h2>
<p>let arr = [1, 2, 3];</p>
<p>console.log(typeof arr);</p>
<p>✅ Output:</p>
<pre><code>object

</code></pre>
<p>➡️ Arrays are a <strong>special type of object</strong> in JavaScript.</p>
<hr>
<h2 id="array-indices"><strong>Array Indices</strong></h2>
<ul>
<li>Indexing starts from <strong>0</strong></li>
</ul>
<p>arr[0], arr[1], arr[2] … arr[n]</p>
<hr>
<h2 id="looping-over-an-array"><strong>2. Looping Over an Array</strong></h2>
<hr>
<h3 id="a-using-for-loop"><strong>A) Using for Loop</strong></h3>
<p>for (let i = 0; i &lt; arr.length; i++) {</p>
<p>console.log(arr[i]);</p>
<p>}</p>
<p>✅ Best when index is required.</p>
<hr>
<h3 id="b-using-for‑of-loop"><strong>B) Using for‑of Loop</strong></h3>
<p>for (let val of arr)<br>
{<br>
console.log(val);</p>
<p>}</p>
<p>✅ Best for directly accessing values.</p>
<hr>
<h2 id="practice-questions"><strong>3. Practice Questions</strong></h2>
<hr>
<h3 id="q1-calculate-average-marks"><strong>Q1: Calculate Average Marks</strong></h3>
<p><strong>Given:</strong></p>
<p>[85, 97, 44, 100, 80]</p>
<h3 id="solution"><strong>Solution</strong></h3>
<p>let marks = [85, 97, 44, 100, 80];</p>
<p>let sum = 0;</p>
<p>for (let i of marks) {</p>
<p>sum += i;</p>
<p>}</p>
<p>let avg = sum / marks.length;</p>
<p>console.log(<code>Avg marks : ${avg}</code>);</p>
<hr>
<h3 id="q2-apply-10-discount-on-prices"><strong>Q2: Apply 10% Discount on Prices</strong></h3>
<p><strong>Given:</strong></p>
<p>[250, 645, 300, 900, 500]</p>
<hr>
<h3 id="approach-1-for‑of-loop"><strong>Approach 1: for‑of loop</strong></h3>
<p>let prices = [250, 645, 300, 900, 500];</p>
<p>let idx = 0;</p>
<p>for (let val of prices) {</p>
<p>prices[idx] = prices[idx] - 0.1 * prices[idx];</p>
<p>idx++;</p>
<p>}</p>
<p>console.log(prices);</p>
<hr>
<h3 id="better-approach-for-loop-recommended"><strong>Better Approach: for loop (Recommended)</strong></h3>
<p>let prices = [250, 645, 300, 900, 500];</p>
<p>for (let i = 0; i &lt; prices.length; i++) {</p>
<p>prices[i] = prices[i] - 0.1 * prices[i];</p>
<p>}</p>
<p>console.log(prices);</p>
<hr>
<h2 id="array-methods-in-javascript"><strong>4. Array Methods in JavaScript</strong></h2>
<p>👉 Built‑in functions used to manipulate arrays.</p>
<hr>
<h3 id="push-–-add-element-at-the-end"><strong>push() – Add element at the end</strong></h3>
<p>arr = [1, 2, 3];</p>
<p>arr.push(4);</p>
<p>console.log(arr);</p>
<p>✅ Output:</p>
<pre><code>[1, 2, 3, 4]

</code></pre>
<hr>
<h3 id="pop-–-remove-element-from-the-end"><strong>pop() – Remove element from the end</strong></h3>
<p>let arr = [1, 2, 3];</p>
<p>arr.pop();</p>
<p>console.log(arr);</p>
<p>✅ Output:</p>
<pre><code>[1, 2]

</code></pre>
<hr>
<h3 id="unshift-–-add-element-at-the-start"><strong>unshift() – Add element at the start</strong></h3>
<p>arr = [2, 3];</p>
<p>arr.unshift(1);</p>
<p>console.log(arr);</p>
<p>✅ Output:</p>
<pre><code>[1, 2, 3]

</code></pre>
<hr>
<h3 id="shift-–-remove-element-from-the-start"><strong>shift() – Remove element from the start</strong></h3>
<p>let arr = [1, 2, 3];</p>
<p>arr.shift();</p>
<p>console.log(arr);</p>
<p>✅ Output:</p>
<pre><code>[2, 3]

</code></pre>
<hr>
<h3 id="summary"><strong>Summary</strong></h3>
<p>Method</p>
<p><code>push()</code> : Add at end</p>
<p><code>pop()</code> : Remove from end</p>
<p><code>unshift()</code> : Add at start</p>
<p><code>shift()</code> : Remove from start</p>
<hr>
<h2 id="concat-–-join-multiple-arrays"><strong>concat() – Join multiple arrays</strong></h2>
<p>let arr1 = [1, 2];</p>
<p>let arr2 = [3, 4];</p>
<p>let arr3 = arr1.concat(arr2);</p>
<p>console.log(arr3);</p>
<p>✅ Output:</p>
<pre><code>[1, 2, 3, 4]

</code></pre>
<hr>
<h2 id="tostring-–-convert-array-to-string"><strong>toString() – Convert array to string</strong></h2>
<p>let arr = [1, 2, 3];</p>
<p>console.log(arr.toString());</p>
<p>✅ Output:</p>
<pre><code>1,2,3

</code></pre>
<hr>
<h2 id="slice-–-extract-part-of-array-does-not-change-original"><strong>slice() – Extract part of array (does NOT change original)</strong></h2>
<p>let arr = [1, 2, 3, 4, 5];</p>
<p>console.log(arr.slice(1, 4));</p>
<p>✅ Output:</p>
<pre><code>[2, 3, 4]

</code></pre>
<hr>
<h2 id="splice-–-add--remove--replace-elements-changes-original-array"><strong>splice() – Add / Remove / Replace elements (changes original array)</strong></h2>
<h3 id="syntax-1"><strong>Syntax</strong></h3>
<p>arr.splice(startIndex, deleteCount, newElement1, newElement2, …);</p>
<hr>
<h3 id="️⃣-add-and-remove-elements"><strong>1️⃣ Add and Remove Elements</strong></h3>
<p>let arr = [1, 2, 3, 4, 5, 6, 7];</p>
<p>arr.splice(2, 2, 101, 102);</p>
<p>console.log(arr);</p>
<p>✅ Output:</p>
<pre><code>[1, 2, 101, 102, 5, 6, 7]

</code></pre>
<hr>
<h3 id="️⃣-only-add-element"><strong>2️⃣ Only Add Element</strong></h3>
<p>let arr = [1, 2, 3, 4];</p>
<p>arr.splice(2, 0, 101);</p>
<p>console.log(arr);</p>
<p>✅ Output:</p>
<pre><code>[1, 2, 101, 3, 4]

</code></pre>
<hr>
<h3 id="️⃣-only-remove-element"><strong>3️⃣ Only Remove Element</strong></h3>
<p>let arr = [1, 2, 3, 4, 5, 6, 7];</p>
<p>arr.splice(3, 1);</p>
<p>console.log(arr);</p>
<p>✅ Output:</p>
<pre><code>[1, 2, 3, 5, 6, 7]

</code></pre>
<hr>
<h3 id="️⃣-replace-an-element"><strong>4️⃣ Replace an Element</strong></h3>
<p>let arr = [1, 2, 3, 4, 5];</p>
<p>arr.splice(3, 1, 101);</p>
<p>console.log(arr);</p>
<p>✅ Output:</p>
<pre><code>[1, 2, 3, 101, 5]

</code></pre>
<hr>
<h3 id="️⃣-remove-all-elements-after-index"><strong>5️⃣ Remove All Elements After Index</strong></h3>
<p>let arr = [1, 2, 3, 101, 5, 6, 7];</p>
<p>arr.splice(4);</p>
<p>console.log(arr);</p>
<p>✅ Output:</p>
<pre><code>[1, 2, 3, 101]

</code></pre>
<hr>
<h2 id="practice-question"><strong>5. Practice Question</strong></h2>
<h3 id="question"><strong>Question</strong></h3>
<p>Create an array of companies:<br>
<code>A, B, C, D, E, F</code></p>
<ol>
<li>Remove the <strong>first company</strong></li>
<li>Remove <strong>C</strong> and add <strong>G</strong> in its place</li>
<li>Add <strong>Y</strong> at the end</li>
</ol>
<hr>
<h3 id="solution-1"><strong>Solution</strong></h3>
<p>let arr = [“A”, “B”, “C”, “D”, “E”, “F”];</p>
<p>arr.shift(); // Remove first</p>
<p>arr.splice(2, 1, “G”); // Replace C with G</p>
<p>arr.push(“Y”); // Add Y at end</p>
<p>console.log(arr);</p>
<p>✅ Final Output:</p>
<pre><code>["B", "G", "D", "E", "F", "Y"]

</code></pre>
<hr>

