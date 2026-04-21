---


---

<h1 id="javascript-–-shraddha-didi"><strong>JAVASCRIPT – Shraddha Didi</strong></h1>
<h2 id="lecture-3-loops-and-strings"><strong>Lecture 3: Loops and Strings</strong></h2>
<hr>
<h2 id="loops-in-javascript"><strong>1. Loops in JavaScript</strong></h2>
<p>👉 <strong>Loops</strong> are used to execute a block of code <strong>again and again</strong> until a condition is satisfied.</p>
<hr>
<h2 id="a-for-loop"><strong>A) for Loop</strong></h2>
<p>Used when the number of iterations is known.</p>
<h3 id="syntax"><strong>Syntax</strong></h3>
<p>for (initialization; condition; updation) {</p>
<p>// some task</p>
<p>}</p>
<h3 id="example"><strong>Example</strong></h3>
<p>for (let i = 1; i &lt;= 5; i++) {</p>
<p>console.log(“Apna College”);</p>
<p>}</p>
<p>✅ Prints <code>"Apna College"</code> 5 times.</p>
<hr>
<h2 id="b-while-loop"><strong>B) while Loop</strong></h2>
<p>Used when the condition is checked <strong>before</strong> executing the code block.</p>
<h3 id="syntax-1"><strong>Syntax</strong></h3>
<p>while (condition) {</p>
<p>// some task</p>
<p>}</p>
<hr>
<h2 id="c-do‑while-loop"><strong>C) do‑while Loop</strong></h2>
<ul>
<li>Executes the code <strong>at least once</strong></li>
<li>Condition is checked <strong>after</strong> execution</li>
</ul>
<h3 id="syntax-2"><strong>Syntax</strong></h3>
<p>do {</p>
<p>// some task</p>
<p>} while (condition);</p>
<hr>
<h2 id="d-for‑of-loop"><strong>D) for‑of Loop</strong></h2>
<p>👉 Used to iterate over <strong>strings and arrays</strong>.</p>
<h3 id="syntax-3"><strong>Syntax</strong></h3>
<p>for (let i of str) {</p>
<p>// some task</p>
<p>}</p>
<h3 id="example-1"><strong>Example</strong></h3>
<p>let str = “ApnaCollege”;</p>
<p>for (let i of str) {</p>
<p>console.log(i);</p>
<p>}</p>
<p>✅ Prints each character of the string.</p>
<hr>
<h2 id="e-for‑in-loop"><strong>E) for‑in Loop</strong></h2>
<p>👉 Used to iterate over <strong>objects and arrays</strong> (keys/indexes).</p>
<h3 id="syntax-4"><strong>Syntax</strong></h3>
<p>for (let key in obj) {</p>
<p>// some task</p>
<p>}</p>
<p>``</p>
<h3 id="example-2"><strong>Example</strong></h3>
<p>let student = {</p>
<p>name: “Rahul Sharma”,</p>
<p>age: 20,</p>
<p>isPass: true</p>
<p>};</p>
<p>for (let key in student) {</p>
<p>console.log(“key:”, key, “value:”, student[key]);</p>
<p>}</p>
<p>✅ Outputs all keys and their corresponding values.</p>
<hr>
<h2 id="practice-questions-loops"><strong>2. Practice Questions (Loops)</strong></h2>
<h3 id="q1-print-all-even-numbers-from-0-to-100"><strong>Q1: Print all even numbers from 0 to 100</strong></h3>
<p>for (let i = 0; i &lt;= 100; i++) {</p>
<p>if (i % 2 == 0)</p>
<p>console.log(i);</p>
<p>}</p>
<hr>
<h3 id="q2-guess-the-game-number"><strong>Q2: Guess the Game Number</strong></h3>
<p>👉 Keep asking the user to guess the number until the correct value is entered.</p>
<p>let gameNum = 5;</p>
<p>let userNum =) {let userNum = prompt("Guess the game number: ");</p>
<p>userNum = prompt(“You entered the wrong number. Guess the number again:”);</p>
<p>}</p>
<p>console.log(“Congrats! You entered the right number”);</p>
<hr>
<h2 id="strings-in-javascript"><strong>3. Strings in JavaScript</strong></h2>
<p>👉 A <strong>String</strong> is a sequence of characters used to represent text.</p>
<hr>
<h3 id="creating-a-string"><strong>Creating a String</strong></h3>
<p>let str = “Apna College”;</p>
<hr>
<h3 id="string-length"><strong>String Length</strong></h3>
<p>str.length;</p>
<hr>
<h3 id="string-indices"><strong>String Indices</strong></h3>
<p>str[0];</p>
<p>str[2];</p>
<p>✅ Indexing starts from <strong>0</strong>.</p>
<hr>
<h2 id="template-literals"><strong>4. Template Literals</strong></h2>
<p>👉 Template literals allow <strong>embedded expressions</strong> inside strings.</p>
<ul>
<li>Written using backticks <code>`</code></li>
</ul>
<p><code>This is a template literal</code></p>
<hr>
<h3 id="string-interpolation"><strong>String Interpolation</strong></h3>
<p>Used to insert variables or expressions using <code>${}</code>.</p>
<p>let obj {</p>
<p>item: “pen”,</p>
<p>price: 10</p>
<p>};</p>
<p>console.log(<code>The cost of ${obj.item} is ${obj.price} rupees</code>);</p>
<p>✅ Output:</p>
<pre><code>The cost of pen is 10 rupees

</code></pre>
<hr>
<h3 id="template-literal-evaluation"><strong>Template Literal Evaluation</strong></h3>
<p>let numberString = <code>This is a template literal having value ${1 + 2 + 3}</code>;</p>
<p>console.log(numberString);</p>
<p>console.log(typeof numberString);</p>
<p>✅ Output:</p>
<pre><code>This is a template literal having value 6
string

</code></pre>
<hr>
<h2 id="escape-characters"><strong>5. Escape Characters</strong></h2>
<p>Escape Character</p>
<p>Meaning</p>
<p>New line : <code>\n</code></p>
<p>Tab space : <code>\t</code></p>
<h3 id="example-3"><strong>Example</strong></h3>
<p>let str = “Apna\tCollege”;</p>
<p>console.log(str);</p>
<p>console.log(str.length);</p>
<p>✅ Output:</p>
<pre><code>Apna    College
12

</code></pre>
<p>✅ Escape characters count as <strong>one character</strong>.</p>
<hr>
<h2 id="string-methods-in-javascript"><strong>6. String Methods in JavaScript</strong></h2>
<p>👉 Built‑in methods to manipulate strings.</p>
<p>Method</p>
<p><code>toUpperCase()</code> : Converts to uppercase</p>
<p><code>toLowerCase()</code> : Converts to lowercase</p>
<p><code>trim()</code> : Removes extra spaces</p>
<p><code>slice(start, end)</code> : Extracts part of string</p>
<p><code>concat()</code> : Joins strings</p>
<p><code>replace()</code> : Replaces values</p>
<p><code>charAt()</code> : Gets character at index</p>
<hr>
<h3 id="examples"><strong>Examples</strong></h3>
<p>let str = “Apna College”;</p>
<p>console.log(str.toUpperCase());</p>
<p>console.log(str);</p>
<p>✅ Output:</p>
<pre><code>APNA COLLEGE
Apna College

</code></pre>
<p>⚠️ <strong>Note:</strong><br>
Strings are <strong>immutable</strong> in JavaScript – methods return a <strong>new string</strong>, original remains unchanged.</p>
<hr>
<p>let str = “Apna College”;</p>
<p>console.log(str.slice(1, 3));</p>
<p>✅ Output:</p>
<pre><code>pn

</code></pre>
<hr>
<p>let str = “hello”;</p>
<p>console.log(str.replace(“he”, “yo”));</p>
<p>✅ Output:</p>
<pre><code>yollo

</code></pre>
<hr>
<h2 id="practice-question-strings"><strong>7. Practice Question (Strings)</strong></h2>
<h3 id="question"><strong>Question</strong></h3>
<p>Prompt the user to enter their full name and generate a username:</p>
<ul>
<li>Start with <code>@</code></li>
<li>Followed by full name</li>
<li>End with name length</li>
</ul>
<p><strong>Example:</strong><br>
<code>shraddhakhapra → @shraddhakhapra13</code></p>
<hr>
<h3 id="solution"><strong>Solution</strong></h3>
<p>let str = prompt(“Enter your name:”);</p>
<p>let username = “@” + str + str.length;</p>
<p>console.log(username);</p>
<hr>

