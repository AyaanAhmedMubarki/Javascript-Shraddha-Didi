---


---

<h1 id="javascript-–-shraddha-didi"><strong>JAVASCRIPT – Shraddha Didi</strong></h1>
<h2 id="lecture-6-dom-document-object-model"><strong>Lecture 6: DOM (Document Object Model)</strong></h2>
<hr>
<h2 id="window-object"><strong>1) Window Object</strong></h2>
<p>✅ <strong>Window</strong> represents the browser window/tab.</p>
<ul>
<li>It is <strong>created by the browser automatically</strong> (not by JavaScript).</li>
<li>It is a <strong>global object</strong>, so you can access many properties/methods through it.</li>
</ul>
<h3 id="example"><strong>Example</strong></h3>
<p>console.log(“Hello”);</p>
<p>window.console.log(“Hello”);</p>
<p>✅ Both produce the same output, so we usually <strong>don’t write <code>window</code></strong>.</p>
<hr>
<h2 id="what-is-dom"><strong>2) What is DOM?</strong></h2>
<p>👉 When a webpage loads, the browser converts HTML into a <strong>tree-like structure</strong> called the <strong>DOM</strong>.<br>
JavaScript uses this DOM to <strong>read/change HTML &amp; CSS dynamically</strong>.</p>
<h3 id="✅-dom-tree-simple-diagram">✅ DOM Tree (Simple Diagram)</h3>
<pre><code>window
 └── document
      └── html
           ├── head
           │    ├── meta
           │    ├── title
           │    └── link
           └── body
                ├── div
                ├── img
                ├── h1
                ├── p
                ├── div
                └── script

</code></pre>
<hr>
<h3 id="console.log-vs-console.dir"><strong>console.log vs console.dir</strong></h3>
<ul>
<li><code>console.log(document)</code> → prints document in normal readable format</li>
<li><code>console.dir(document)</code> → prints as an <strong>object with properties</strong></li>
</ul>
<p>✅ <code>console.dir()</code> is very useful while exploring DOM nodes.</p>
<hr>
<h2 id="dom-manipulation-selecting-elements"><strong>3) DOM Manipulation (Selecting Elements)</strong></h2>
<h3 id="a-select-by-id"><strong>A) Select by ID</strong></h3>
<p><code>document.getElementById("myId");</code></p>
<h3 id="b-select-by-class"><strong>B) Select by Class</strong></h3>
<p><code>document.getElementsByClassName("myClass");</code></p>
<p>⚠️ Returns an <strong>HTMLCollection</strong> (looks like array but not exactly array)</p>
<h3 id="c-select-by-tag"><strong>C) Select by Tag</strong></h3>
<p><code>document.getElementsByTagName("p");</code></p>
<hr>
<h2 id="query-selector-most-used-✅"><strong>4) Query Selector (Most Used ✅)</strong></h2>
<h3 id="a-queryselector"><strong>A) querySelector()</strong></h3>
<ul>
<li>Returns the <strong>first matching element</strong></li>
</ul>
<p><code>document.querySelector("p");</code> // first p tag</p>
<p><code>document.querySelector(".myClass");</code> // class</p>
<p><code>document.querySelector("#myId");</code>// id</p>
<h3 id="b-queryselectorall"><strong>B) querySelectorAll()</strong></h3>
<ul>
<li>Returns <strong>all matching elements</strong> as a <strong>NodeList</strong></li>
</ul>
<p>document.querySelectorAll(“p”); // all </p><p></p>
<h3 id="examples"><strong>Examples</strong></h3>
<p>let firstP = document.querySelector(“p”);</p>
<p>console.dir(firstP);</p>
<p>let allP = document.querySelectorAll(“p”);</p>
<p>console.dir(allP);</p>
<p>let classEle = document.querySelector(".myClass");</p>
<p>console.dir(classEle);</p>
<p>let idEle = document.querySelector("#myId");</p>
<p>console.dir(idEle);</p>
<hr>
<h2 id="dom-tree-node-types"><strong>5) DOM Tree Node Types</strong></h2>
<p>DOM consists of different node types:</p>
<ol>
<li><strong>Element nodes</strong> → tags like <code>&lt;div&gt;</code>, <code>&lt;p&gt;</code></li>
<li><strong>Text nodes</strong> → text inside tags</li>
<li><strong>Comment nodes</strong> → <code>&lt;!-- comment --&gt;</code></li>
</ol>
<hr>
<h2 id="important-dom-properties-very-important-⭐"><strong>6) Important DOM Properties (Very Important ⭐)</strong></h2>
<h3 id="✅-1-tagname">✅ (1) <code>tagName</code></h3>
<ul>
<li>Returns the tag name <strong>for element nodes</strong> in uppercase.</li>
</ul>
<p><code>&lt;p id="para"&gt;Hello&lt;/p&gt;</code></p>
<p>let el = document.querySelector("#para");</p>
<p>console.log(el.tagName);</p>
<p>✅ Output:</p>
<pre><code>P

</code></pre>
<hr>
<h3 id="✅-2-innertext">✅ (2) <code>innerText</code></h3>
<ul>
<li>Returns/sets the <strong>visible text</strong> inside the element and its children.</li>
</ul>
<h1>Welcome <span>Hidden</span></h1>
<p>let h1 = document.querySelector(“h1”);</p>
<p>console.log(h1.innerText);</p>
<p>✅ Output:</p>
<pre><code>Welcome

</code></pre>
<p>(Does NOT include hidden text)</p>
<hr>
<h3 id="✅-3-innerhtml">✅ (3) <code>innerHTML</code></h3>
<ul>
<li>Returns/sets the <strong>HTML content</strong> inside the element.</li>
</ul>
<p><code>&lt;div id="box"&gt;&lt;b&gt;Hello&lt;/b&gt; World&lt;/div&gt;</code></p>
<p>let box = document.querySelector("#box");</p>
<p>console.log(box.innerHTML);</p>
<p>✅ Output:</p>
<pre><code>&lt;b&gt;Hello&lt;/b&gt; World

</code></pre>
<p>You can also set HTML:</p>
<p>box.innerHTML = “<i>New Text</i>”;</p>
<hr>
<h3 id="✅-4-textcontent">✅ (4) <code>textContent</code></h3>
<ul>
<li>Returns/sets <strong>all text</strong>, including hidden text.</li>
</ul>
<p>Using the earlier example:</p>
<p>console.log(h1.textContent);</p>
<p>✅ Output:</p>
<pre><code>Welcome Hidden

</code></pre>
<hr>
<h3 id="quick-summary">Quick Summary</h3>
<ul>
<li><strong>tagName</strong> → tag name</li>
<li><strong>innerText</strong> → visible text only</li>
<li><strong>innerHTML</strong> → HTML inside element</li>
<li><strong>textContent</strong> → all text (even hidden)</li>
</ul>
<hr>
<h1 id="✅-practice-questions-part-1">✅ Practice Questions (Part 1)</h1>
<hr>
<h2 id="q1-append-text-to-an-h2"><strong>Q1) Append text to an <code>&lt;h2&gt;</code></strong></h2>
<h3 id="html"><strong>HTML</strong></h3>
<p><code>&lt;h2&gt;Hello JavaScript&lt;/h2&gt;</code></p>
<h3 id="js"><strong>JS</strong></h3>
<pre><code>let h2 = document.querySelector("h2");

h2.innerText = h2.innerText + " from Apna College students"; 
</code></pre>
<hr>
<h2 id="q2-3-divs-with-class-“box”-and-add-unique-text"><strong>Q2) 3 divs with class “box” and add unique text</strong></h2>
<h3 id="html-fixed"><strong>HTML (Fixed)</strong></h3>
<p><code>&lt;div class="box"&gt;First Div&lt;/div&gt;</code></p>
<p><code>&lt;div class="box"&gt;Second Div&lt;/div&gt;</code></p>
<p><code>&lt;div class="box"&gt;Third Div&lt;/div&gt;</code></p>
<h3 id="js-correct-way-✅"><strong>JS (Correct Way ✅)</strong></h3>
<pre class=" language-let"><code class="prism  language-let">

let idx = 1;

for (let div of divs) {

div.innerText = `New Unique Value ${idx}`;

idx++;

}
</code></pre>
<p>⚠️ Your earlier code had an issue: <code>divs[i]</code> is wrong inside <code>for-of</code>.<br>
In <code>for-of</code>, <code>div</code> itself is the element.</p>
<hr>
<hr>
<h1 id="section">------------------------------</h1>
<h1 id="part-2-more-dom-manipulation"><strong>Part 2: More DOM Manipulation</strong></h1>
<h1 id="section-1">------------------------------</h1>
<h2 id="attributes"><strong>7) Attributes</strong></h2>
<h3 id="✅-getattributeattr">✅ getAttribute(attr)</h3>
<p>Gets attribute value:</p>
<p>let div = document.querySelector(“div”);</p>
<p>console.log(div.getAttribute(“id”));</p>
<p>console.log(div.getAttribute(“name”));</p>
<h3 id="✅-setattributeattr-val">✅ setAttribute(attr, val)</h3>
<p>Sets/updates attribute value:</p>
<p>let para = document.querySelector(“p”);</p>
<p>para.setAttribute(“class”, “newClass”);</p>
<p>``</p>
<p>⚠️ Note: <code>setAttribute("class","newClass")</code> <strong>overwrites the old class</strong>.</p>
<hr>
<h2 id="styling-using-javascript"><strong>8) Styling using JavaScript</strong></h2>
<h3 id="node.style"><strong>node.style</strong></h3>
<p>let div = document.querySelector("#box");</p>
<p>div.style.backgroundColor = “green”;</p>
<p>div.style.visibility = “hidden”;</p>
<p>div.style.fontSize = “26px”;</p>
<p>div.innerText = “hello”;</p>
<p>✅ CSS property naming rule in JS:</p>
<ul>
<li><code>background-color</code> → <code>backgroundColor</code></li>
<li><code>font-size</code> → <code>fontSize</code></li>
</ul>
<hr>
<h2 id="creating--inserting-elements"><strong>9) Creating &amp; Inserting Elements</strong></h2>
<h3 id="✅-create-element">✅ Create Element</h3>
<p>let el = document.createElement(“div”);</p>
<h3 id="✅-insert-elements">✅ Insert Elements</h3>
<p>Method : Where it inserts</p>
<p><code>node.append(el)</code>: inside node (end)</p>
<p><code>node.prepend(el)</code>: inside node (start)</p>
<p><code>node.before(el)</code>: before node (outside)</p>
<p><code>node.after(el)</code>: after node (outside)</p>
<h3 id="✅-remove-element">✅ Remove Element</h3>
<p><code>node.remove();</code></p>
<hr>
<h3 id="example-create-a-button-and-append">Example: Create a Button and Append</h3>
<p>let newBtn = document.createElement(“button”);</p>
<p>newBtn.innerText = “Click Me”;</p>
<p>let div = document.querySelector(“div”);</p>
<p>div.append(newBtn);</p>
<h3 id="example-insert-paragraph-after-div">Example: Insert paragraph after div</h3>
<p>If you want the paragraph <strong>after</strong> the div:</p>
<p>let div = document.querySelector(“div”);</p>
<p>let para = document.querySelector(“p”);</p>
<p>div.after(para);</p>
<hr>
<h3 id="example-create-a-heading--insert-at-start-of-body">Example: Create a heading &amp; insert at start of body</h3>
<p>let newHeading = document.createElement(“h1”);</p>
<p>newHeading.innerHTML = “<i>This is heading created through DOM feature</i>”;</p>
<p>document.querySelector(“body”).prepend(newHeading);</p>
<hr>
<h3 id="example-remove-paragraph">Example: Remove paragraph</h3>
<p>let para1 = document.querySelector(“p”);</p>
<p>para1.remove();</p>
<hr>
<h1 id="✅-practice-questions-part-2">✅ Practice Questions (Part 2)</h1>
<hr>
<h2 id="create-a-new-button-element.-give-it-a-text-click-me-background-color-of-red-and-text-color-of-white.-insert-the-button-as-the-first-element-inside-the-body-tag">1) Create a new button element. Give it a text “Click Me”, background color of red and text color of white. Insert the button as the first element inside the body tag</h2>
<p>let newBtn = document.createElement(“button”);</p>
<p>newBtn.innerText = “Click Me”;</p>
<p>newBtn.style.backgroundColor = “red”;</p>
<p>newBtn.style.color = “white”;</p>
<p>document.querySelector(“body”).prepend(newBtn);</p>
<hr>
<h2 id="create-a-p-tag-in-html-and-give-it-a-class-and-some-style.-now-create-a-new-class-in-css-and-try-to-append-this-class-to-the-p-element.--did-you-notice-how-you-overwrite-the-class-name-when-you-add-a-new-class.-solve-this-problem-using-classlist.">*2)Create a <p> tag in html and give it a class and some style. Now create a new class in CSS and try to append this class to the </p><p> element.  Did you notice how you overwrite the class name when you add a new class. Solve this problem using classList.</p></h2>
<h3 id="html-1"><strong>HTML</strong></h3>
<p><code>&lt;p class="oldClass"&gt;This is a paragraph in DOM Practice Question&lt;/p&gt;</code></p>
<h3 id="css"><strong>CSS</strong></h3>
<p>.oldClass<br>
{<br>
color: red;<br>
}</p>
<p>.newClass<br>
{<br>
background-color: green;<br>
}</p>
<h3 id="js-1">JS</h3>
<p>let para = document.querySelector(“p”);</p>
<p>para.classList.add(“newClass”);</p>
<p>✅ Now paragraph has both classes:</p>
<ul>
<li><code>oldClass</code></li>
<li><code>newClass</code></li>
</ul>
<h3 id="remove-class">Remove class:</h3>
<p>para.classList.remove(“newClass”);</p>
<h3 id="toggle-class-add-if-absent-remove-if-present">Toggle class (add if absent, remove if present):</h3>
<p>para.classList.toggle(“newClass”);</p>
<hr>

