---


---

<h1 id="javascript-–-shraddha-didi"><strong>JAVASCRIPT – Shraddha Didi</strong></h1>
<h2 id="lecture-2-operators-and-conditionals"><strong>Lecture 2: Operators and Conditionals</strong></h2>
<hr>
<h2 id="comments-in-javascript"><strong>1. Comments in JavaScript</strong></h2>
<p>👉 <strong>Comments</strong> are parts of code that are <strong>not executed</strong> by JavaScript.<br>
They are used to explain code and make it more readable.</p>
<h3 id="types-of-comments"><strong>Types of Comments</strong></h3>
<h3 id="single‑line-comment"><strong>Single‑line Comment</strong></h3>
<p>// This is a single line comment</p>
<h3 id="multi‑line-comment"><strong>Multi‑line Comment</strong></h3>
<p>/* This is a multi-line</p>
<p>comment */</p>
<p>✅ Comments do not affect program execution.</p>
<hr>
<h2 id="operators-in-javascript"><strong>2. Operators in JavaScript</strong></h2>
<p>👉 <strong>Operators</strong> are used to perform operations on data (operands).</p>
<hr>
<h3 id="a-arithmetic-operators"><strong>A) Arithmetic Operators</strong></h3>
<p>Operators</p>
<p>Addition <code>+</code></p>
<p>Subtraction <code>-</code></p>
<p>Multiplication <code>*</code></p>
<p>Division <code>/</code></p>
<p>Modulus (Remainder) <code>%</code></p>
<p>Exponentiation (Power) <code>**</code></p>
<h4 id="example"><strong>Example</strong></h4>
<p>let a = 2 ** 3;</p>
<p>console.log(a);</p>
<p>✅ Output:</p>
<pre><code>8

</code></pre>
<hr>
<h3 id="increment-and-decrement-operators"><strong>Increment and Decrement Operators</strong></h3>
<h4 id="increment-"><strong>Increment (<code>++</code>)</strong></h4>
<ul>
<li><strong>Pre‑increment:</strong> <code>++a</code> → increase first, then use</li>
<li><strong>Post‑increment:</strong> <code>a++</code> → use first, then increase</li>
</ul>
<h4 id="decrement---"><strong>Decrement (<code>--</code>)</strong></h4>
<ul>
<li><strong>Pre‑decrement:</strong> <code>--a</code></li>
<li><strong>Post‑decrement:</strong> <code>a--</code></li>
</ul>
<hr>
<h2 id="b-assignment-operators"><strong>B) Assignment Operators</strong></h2>
<p>Used to assign values to variables.</p>
<p>Operator</p>
<p>Assignment <code>=</code></p>
<p>Add and assign <code>+=</code></p>
<p>Subtract and assign <code>-=</code></p>
<p>Multiply and assign <code>*=</code></p>
<p>Modulus and assign <code>%=</code></p>
<p>Power and assign <code>**=</code></p>
<h4 id="example-1"><strong>Example</strong></h4>
<p>let a = 10;</p>
<p>a += 5; // a = a + 5</p>
<p>✅ Output:</p>
<pre><code>15

</code></pre>
<hr>
<h2 id="c-comparison-operators"><strong>C) Comparison Operators</strong></h2>
<p>Used to compare two values and return <code>true</code> or <code>false</code>.</p>
<p>Operator</p>
<p>Equal to (loose comparison) <code>==</code></p>
<p>Equal value &amp; type (strict – recommended)<br>
<code>===</code></p>
<p>Not equal (loose) <code>!=</code></p>
<p>Not equal value or type (strict) <code>!==</code></p>
<p>Greater than <code>&gt;</code></p>
<p>Less than <code>&lt;</code></p>
<p>Greater than or equal to <code>&gt;=</code></p>
<p>Less than or equal to <code>&lt;=</code></p>
<hr>
<h3 id="important-examples"><strong>Important Examples</strong></h3>
<p>5 == “5” // true</p>
<p>5 === “5” // false</p>
<p>5 != “5” // false</p>
<p>5 !== “5” // true</p>
<p>✅ <strong>Best Practice:</strong><br>
Always use <code>===</code> (strict equality).</p>
<hr>
<h2 id="d-logical-operators"><strong>D) Logical Operators</strong></h2>
<p>Used to combine multiple conditions.</p>
<p>Operator</p>
<p>AND (all conditions must be true) <code>&amp;&amp;</code></p>
<p>OR (any one condition true) <code>||</code></p>
<p>NOT (reverses result) <code>!</code></p>
<h4 id="examples"><strong>Examples</strong></h4>
<p>true &amp;&amp; false // false</p>
<p>true || false // true</p>
<p>!true // false</p>
<hr>
<h2 id="conditional-statements"><strong>3. Conditional Statements</strong></h2>
<p>Used to execute code <strong>based on conditions</strong>.</p>
<hr>
<h3 id="a-if--else--else-if-statements"><strong>A) if / else / else if Statements</strong></h3>
<p>let color;</p>
<p>if (mode === “dark-mode”)<br>
{<br>
color = “black”;<br>
}<br>
else<br>
{<br>
color = “white”;<br>
}</p>
<p>✅ Executes code based on the condition result.</p>
<hr>
<h3 id="b-ternary-operator"><strong>B) Ternary Operator</strong></h3>
<p>A <strong>short form of if‑else</strong>.</p>
<p><strong>Syntax:</strong></p>
<p>condition ? trueExpression : falseExpression;</p>
<h4 id="example-2"><strong>Example</strong></h4>
<p>age &gt;= 18 ? “Adult” : “Minor”;</p>
<hr>
<h3 id="c-switch-statement"><strong>C) switch Statement</strong></h3>
<p>Used when multiple conditions are based on <strong>one value</strong>.</p>
<p>switch (x)<br>
{<br>
case 1:<br>
break;</p>
<p>default:</p>
<p>}</p>
<p>✅ More readable than multiple <code>if‑else</code> conditions.</p>
<hr>
<h2 id="user-interaction-methods"><strong>4. User Interaction Methods</strong></h2>
<p>Used to interact with the user through popups.</p>
<h3 id="alert"><strong>alert()</strong></h3>
<p>alert(“Hello”);</p>
<ul>
<li>Displays a message popup.</li>
</ul>
<hr>
<h3 id="prompt"><strong>prompt()</strong></h3>
<p>prompt(“Enter name”);</p>
<ul>
<li>Takes input from the user (returns a <strong>string</strong>).</li>
</ul>
<hr>
<h3 id="confirm"><strong>confirm()</strong></h3>
<p>confirm(“Are you sure?”);</p>
<ul>
<li>Returns <code>true</code> or <code>false</code>.</li>
</ul>
<hr>
<h2 id="javascript-documentation"><strong>5. JavaScript Documentation</strong></h2>
<p>📘 <strong>MDN Web Docs</strong></p>
<ul>
<li>Official documentation for <strong>HTML, CSS, and JavaScript</strong></li>
<li>Most trusted resource for JavaScript learning</li>
</ul>
<p>✅ Website: <a href="https://developer.mozilla.org/">https://developer.mozilla.org</a></p>
<hr>
<h2 id="practice-question"><strong>6. Practice Question</strong></h2>
<h3 id="question"><strong>Question</strong></h3>
<p>Prompt the user to enter a number and check if it is a multiple of 5.</p>
<h3 id="solution"><strong>Solution</strong></h3>
<p>let n = Number(prompt(“Enter a number”));</p>
<p>if (n % 5 === 0)</p>
<p>alert(<code>${n} is a multiple of 5</code>);</p>
<p>else</p>
<p>alert(<code>${n} is not a multiple of 5</code>);</p>
<hr>

