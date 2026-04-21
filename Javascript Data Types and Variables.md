---


---

<h1 id="javascript-–-shraddha-didi"><strong>JAVASCRIPT – Shraddha Didi</strong></h1>
<h2 id="lecture-1-variables-and-data-types"><strong>Lecture 1: Variables and Data Types</strong></h2>
<hr>
<h2 id="vs-code-shortcut-for-html-boilerplate"><strong>1. VS Code Shortcut for HTML Boilerplate</strong></h2>
<p>To generate the full standard HTML structure quickly:</p>
<p><strong>Shortcut:</strong></p>
<pre><code>Shift + !

</code></pre>
<p>✅ Automatically creates the complete HTML boilerplate code.</p>
<hr>
<h2 id="javascript-in-console"><strong>2. JavaScript in Console</strong></h2>
<h3 id="alert"><strong>alert()</strong></h3>
<p>alert(‘Hello JS’);</p>
<ul>
<li>Displays a popup alert message in the browser.</li>
</ul>
<h3 id="console.log"><strong>console.log()</strong></h3>
<p>console.log(‘Hello Javascript’);</p>
<ul>
<li>Used to print (log) messages to the browser console.</li>
<li>Mainly used for debugging and checking output.</li>
</ul>
<hr>
<h2 id="variables-in-javascript"><strong>3. Variables in JavaScript</strong></h2>
<p>👉 <strong>Variables</strong> are containers used to store data.</p>
<hr>
<h3 id="rules-for-naming-variables"><strong>Rules for Naming Variables</strong></h3>
<ul>
<li>Variable names are <strong>case‑sensitive</strong><br>
✅ <code>a</code> and <code>A</code> are different</li>
<li>Allowed characters:
<ul>
<li>Letters (a–z, A–Z)</li>
<li>Digits (0–9)</li>
<li>Underscore <code>_</code></li>
<li>Dollar sign <code>$</code></li>
</ul>
</li>
<li><strong>First character</strong> must be:
<ul>
<li>Letter, <code>_</code>, or <code>$</code></li>
</ul>
</li>
<li><strong>Spaces are not allowed</strong></li>
<li><strong>Reserved words</strong> cannot be used</li>
<li><strong>Camel Case</strong> naming convention is used<br>
✅ Example: <code>avgSalary</code>, <code>totalMarks</code></li>
</ul>
<hr>
<h3 id="dynamic-typing-in-javascript"><strong>Dynamic Typing in JavaScript</strong></h3>
<p>JavaScript is <strong>dynamically typed</strong>, meaning the data type of a variable can change during execution.</p>
<p>name = ‘Ayaan’;</p>
<p>name = 25;</p>
<p>console.log(name);</p>
<p>✅ Output:</p>
<pre><code>25

</code></pre>
<p>(The string value is replaced by a number.)</p>
<hr>
<h3 id="examples"><strong>Examples</strong></h3>
<h4 id="example-1"><strong>Example 1</strong></h4>
<p>name = ‘Ayaan’;</p>
<p>console.log(name + " from script file");</p>
<p>✅ Output:</p>
<pre><code>Ayaan from script file

</code></pre>
<hr>
<h4 id="example-2"><strong>Example 2</strong></h4>
<p>x = null;</p>
<p>y = undefined;</p>
<p>console.log(x + " " + y);</p>
<p>✅ Output:</p>
<pre><code>null undefined

</code></pre>
<hr>
<h4 id="example-3"><strong>Example 3</strong></h4>
<p>isPalin = true;</p>
<p>console.log(isPalin);</p>
<p>✅ Output:</p>
<pre><code>true

</code></pre>
<hr>
<h2 id="var-let-and-const"><strong>4. var, let, and const</strong></h2>
<h3 id="var"><strong>var</strong></h3>
<ul>
<li>Can be <strong>re‑declared</strong> and <strong>updated</strong></li>
<li>Has <strong>global scope</strong></li>
<li>Older keyword (used before 2015)</li>
</ul>
<p>var a = 15;</p>
<p>var a = 25; // No error</p>
<hr>
<h3 id="let"><strong>let</strong></h3>
<ul>
<li>❌ Cannot be re‑declared</li>
<li>✅ Can be updated</li>
<li>Has <strong>block scope</strong></li>
</ul>
<p>let a = 5;</p>
<p>let a = 10; // Error</p>
<p>``</p>
<p>✅ Correct way:</p>
<p>let a = 5;</p>
<p>a = 10; // No error</p>
<p><strong>Special case:</strong></p>
<p>let a;</p>
<p>console.log(a);</p>
<p>✅ Output:</p>
<pre><code>undefined

</code></pre>
<hr>
<h3 id="const"><strong>const</strong></h3>
<ul>
<li>❌ Cannot be re‑declared</li>
<li>❌ Cannot be updated</li>
<li>Has <strong>block scope</strong></li>
<li>Must be initialized at declaration</li>
</ul>
<p>const PI = 3.14;</p>
<p>❌ Invalid:</p>
<p>const PI;</p>
<p>console.log(PI);</p>
<p>✅ Output:</p>
<pre><code>Error

</code></pre>
<hr>
<h2 id="data-types-in-javascript"><strong>5. Data Types in JavaScript</strong></h2>
<h3 id="a-primitive-data-types-7"><strong>A) Primitive Data Types (7)</strong></h3>
<ol>
<li>number</li>
<li>string</li>
<li>boolean</li>
<li>undefined</li>
<li>null</li>
<li>BigInt</li>
<li>symbol</li>
</ol>
<hr>
<h3 id="primitive-type-examples"><strong>Primitive Type Examples</strong></h3>
<p>let a = ‘Ayaan’;</p>
<p>console.log(typeof a);</p>
<p>✅ Output:</p>
<pre><code>string

</code></pre>
<p>let x = BigInt(“123”);</p>
<p>console.log(typeof x);</p>
<p>✅ Output:</p>
<pre><code>bigint

</code></pre>
<p>let s = Symbol(“Hello!”);</p>
<p>console.log(typeof s);</p>
<p>✅ Output:</p>
<pre><code>symbol

</code></pre>
<hr>
<h3 id="b-non‑primitive-data-type"><strong>B) Non‑Primitive Data Type</strong></h3>
<h4 id="object"><strong>Object</strong></h4>
<ul>
<li>A collection of values stored as <strong>key : value</strong> pairs.</li>
</ul>
<hr>
<h3 id="example-student-object"><strong>Example: Student Object</strong></h3>
<p>const student = {</p>
<p>name: “Reza Khan”,</p>
<p>age: 20,</p>
<p>marks: 80</p>
<p>};</p>
<hr>
<h3 id="accessing-object-properties"><strong>Accessing Object Properties</strong></h3>
<p>console.log(student[“name”]);</p>
<p>OR</p>
<p>console.log(<a href="http://student.name">student.name</a>);</p>
<p>✅ Output:</p>
<pre><code>Reza Khan

</code></pre>
<hr>
<h3 id="updating-object-values"><strong>Updating Object Values</strong></h3>
<p>student[“name”] = “Rahul Sharma”;</p>
<p>console.log(student[“name”]);</p>
<p>✅ Output:</p>
<pre><code>Rahul Sharma

</code></pre>
<hr>
<h3 id="important-note-very-important-for-exams--interviews"><strong>Important Note (Very Important for Exams &amp; Interviews)</strong></h3>
<ul>
<li>✅ <code>let</code> variables <strong>can be updated</strong></li>
<li>❌ <code>const</code> variables <strong>cannot be updated</strong></li>
<li>✅ BUT: <strong>Objects declared with <code>const</code> CAN be updated</strong></li>
</ul>
<p>✅ Reason:<br>
The <strong>reference</strong> to the object is constant, but the <strong>properties inside the object</strong> can change.</p>
<hr>
<p>console.log(typeof student);</p>
<p>✅ Output:</p>
<pre><code>object

</code></pre>
<hr>

