---


---

<h1 id="javascript-–-shraddha-didi"><strong>JAVASCRIPT – Shraddha Didi</strong></h1>
<h2 id="lecture-7-events">Lecture 7: Events</h2>
<hr>
<h2 id="what-are-events-in-javascript"><strong>1) What are Events in JavaScript?</strong></h2>
<p>👉 An <strong>Event</strong> is a change in the state of an object (or something that happens on the webpage).<br>
Events are fired to notify the code about “interesting changes” that may affect execution.</p>
<h3 id="common-types-of-events"><strong>Common Types of Events</strong></h3>
<ul>
<li><strong>Mouse Events:</strong> <code>click</code>, <code>dblclick</code>, <code>mouseover</code>, <code>mouseout</code>, etc.</li>
<li><strong>Keyboard Events:</strong> <code>keypress</code>, <code>keyup</code>, <code>keydown</code></li>
<li><strong>Form Events:</strong> <code>submit</code>, <code>change</code>, <code>focus</code>, <code>blur</code></li>
<li><strong>Other:</strong> <code>load</code>, <code>scroll</code>, <code>resize</code>, <code>print</code>, etc.</li>
</ul>
<hr>
<h2 id="ways-to-handle-events-in-javascript"><strong>2) Ways to Handle Events in JavaScript</strong></h2>
<p>There are 3 classic approaches:</p>
<ol>
<li><strong>Inline Event Handlers (HTML)</strong></li>
<li><strong>DOM Level 0 Event Handlers (<code>element.onclick = ...</code>)</strong></li>
<li><strong>Event Listeners (DOM Level 2) – Best ✅</strong></li>
</ol>
<hr>
<h1 id="✅-1.-inline-event-handlers-not-preferred">✅ 1. Inline Event Handlers (Not Preferred)</h1>
<h3 id="example-in-html"><strong>Example (in HTML)</strong></h3>
<p><code>&lt;button onclick="alert('Clicked!')"&gt;Click Me&lt;/button&gt;</code></p>
<h3 id="✅-more-examples">✅ More examples</h3>
<p><code>&lt;button onclick="console.log('Button was clicked')"&gt;Click Me&lt;/button&gt;</code></p>
<p><code>&lt;button ondblclick="console.log('Clicked 2x')"&gt;Click Me 2 Times&lt;/button&gt;</code></p>
<p><code>&lt;div onmouseover="console.log('You are inside div')"&gt;This is a div&lt;/div&gt;</code></p>
<h3 id="drawbacks-of-inline-events"><strong>Drawbacks of Inline Events</strong></h3>
<ul>
<li>❌ Mixes HTML + JavaScript (bad separation of concerns)</li>
<li>❌ Hard to maintain and debug (especially large code)</li>
<li>❌ Usually runs in global scope → naming conflicts</li>
<li>❌ Not easy to remove/modify dynamically</li>
<li>❌ Not scalable for real projects</li>
</ul>
<hr>
<h1 id="✅-2.-event-handlers-dom-level-0">✅ 2. Event Handlers (DOM Level 0)</h1>
<p>This is when you assign a handler directly using JS property like <code>onclick</code>, <code>onmouseover</code>, etc.</p>
<h3 id="syntax"><strong>Syntax</strong></h3>
<p>node.event = () =&gt; {</p>
<p>// handle here</p>
<p>};</p>
<h3 id="example"><strong>Example</strong></h3>
<p><strong>index.html</strong></p>
<pre><code>&lt;button id="btn1"&gt;Click Me&lt;/button&gt;`

&lt;div id="box"&gt;This is a div&lt;/div&gt;
  
`&lt;script src="script.js"&gt;&lt;/script&gt;
</code></pre>
<p><strong>script.js</strong></p>
<pre><code>let btn1 = document.querySelector("#btn1");

btn1.onclick = () =&gt; {

console.log("Button was clicked");

};

let box = document.querySelector("#box");

box.onmouseover = () =&gt; {

console.log("You are inside div");

};
</code></pre>
<hr>
<h2 id="⭐-important-notes-dom-level-0">⭐ Important Notes (DOM Level 0)</h2>
<h3 id="✅-a-js-handler-has-higher-priority-than-inline">✅ (A) JS handler has higher priority than inline</h3>
<p>If both exist, the JS handler typically overrides.</p>
<h3 id="✅-b-multiple-handlers-not-possible-for-same-event-property">✅ (B) Multiple handlers NOT possible for same event property</h3>
<p>Because reassigning overwrites the previous one.</p>
<p>btn1.onclick = () =&gt; console.log(“Handler 1”);</p>
<p>btn1.onclick = () =&gt; console.log(“Handler 2”);</p>
<p>``</p>
<p>✅ Output:</p>
<pre><code>Handler 2

</code></pre>
<hr>
<h1 id="✅-event-object-e-–-very-important-⭐">✅ Event Object (<code>e</code>) – Very Important ⭐</h1>
<p>👉 When an event occurs, JavaScript automatically creates a special object called the <strong>Event Object</strong> that contains event details.</p>
<h3 id="syntax-1"><strong>Syntax</strong></h3>
<p>node.event = (e) =&gt; {</p>
<p>// handle here</p>
<p>};</p>
<h3 id="useful-properties"><strong>Useful Properties</strong></h3>
<ul>
<li><code>e.type</code> → event type (<code>click</code>, <code>mouseover</code>, etc.)</li>
<li><code>e.target</code> → element on which event happened</li>
<li><code>e.clientX</code>, <code>e.clientY</code> → mouse position (viewport)</li>
</ul>
<h3 id="example-1"><strong>Example</strong></h3>
<pre><code>let btn1 = document.querySelector("#btn1");

 
btn1.onclick = (e) =&gt; {

console.log(e);

console.log("Type:", e.type);

console.log("Target:", e.target);

console.log("Mouse:", e.clientX, e.clientY);

};
</code></pre>
<hr>
<h1 id="✅-3.-event-listeners-dom-level-2-—-best-approach-✅✅">✅ 3. Event Listeners (DOM Level 2) — Best Approach ✅✅</h1>
<h3 id="syntax-2"><strong>Syntax</strong></h3>
<p>node.addEventListener(“eventName”, callback);</p>
<p>node.removeEventListener(“eventName”, callback);</p>
<p>``</p>
<h3 id="why-event-listeners-are-better"><strong>Why Event Listeners are Better?</strong></h3>
<ul>
<li>✅ Multiple listeners allowed (no overwriting)</li>
<li>✅ Cleaner HTML (separation of concerns)</li>
<li>✅ Easy to remove dynamically</li>
<li>✅ Better control and structure</li>
</ul>
<hr>
<h2 id="example-multiple-event-listeners"><strong>Example: Multiple event listeners</strong></h2>
<pre><code>let btn = document.querySelector("#btn1");

btn.addEventListener("click", () =&gt; {

console.log("Button was clicked - handler 1");

});

  

btn.addEventListener("click", () =&gt; {

console.log("Button was clicked - handler 2");

});
</code></pre>
<p>✅ Both handlers run.</p>
<hr>
<h2 id="✅-removing-an-event-listener-important-rule-⭐">✅ Removing an Event Listener (Important Rule ⭐)</h2>
<p>⚠️ To remove a listener, the callback <strong>must be the same function reference</strong> (same memory reference).</p>
<h3 id="✅-example">✅ Example</h3>
<pre><code>let btn = document.querySelector("#btn1");

  
const handler3 = () =&gt; {

console.log("Button was clicked - handler 3");

};

  

btn.addEventListener("click", () =&gt; console.log("handler 1"));

btn.addEventListener("click", () =&gt; console.log("handler 2"));

btn.addEventListener("click", handler3);

btn.addEventListener("click", () =&gt; console.log("handler 4"));

 
btn.removeEventListener("click", handler3);
</code></pre>
<p>✅ Now handler3 will not run.</p>
<p>⚠️ Common mistake:</p>
<p>btn.removeEventListener(“click”, () =&gt; console.log(“handler 3”));</p>
<p>❌ This won’t work because it’s a new function, not the same reference.</p>
<hr>
<h1 id="✅-practice-question-darklight-mode-toggle-button-🌙☀️">✅ Practice Question: Dark/Light Mode Toggle Button 🌙☀️</h1>
<h2 id="✅-goal">✅ Goal</h2>
<p>Create a toggle button:</p>
<ul>
<li>On click → switch to <strong>dark mode</strong></li>
<li>On next click → switch back to <strong>light mode</strong></li>
</ul>
<hr>
<h2 id="✅-method-1-direct-style-change">✅ Method 1 (Direct style change)</h2>
<p><strong>index.html</strong></p>
<pre><code>&lt;button id="mode"&gt;Toggle Mode&lt;/button&gt;

&lt;script src="script.js"&gt;&lt;/script&gt;

</code></pre>
<p><strong>script.js (Corrected ✅)</strong></p>
<pre><code>let modeBtn = document.querySelector("#mode");

let currMode = "light";

let body = document.querySelector("body");

  

modeBtn.addEventListener("click", () =&gt; {

if (currMode === "light") {

currMode = "dark";

body.style.backgroundColor = "black";

body.style.color = "white";

} else {

currMode = "light";

body.style.backgroundColor = "white";

body.style.color = "black";

}

});
</code></pre>
<p>✅ Note: Background color must be set using <strong><code>body.style.backgroundColor</code></strong>, not <code>body.backgroundColor</code>.</p>
<hr>
<h2 id="✅-method-2-best-using-css-classes--classlist-⭐">✅ Method 2 (Best): Using CSS classes + classList ⭐</h2>
<p><strong>style.css</strong></p>
<pre><code>.dark {

background-color: black;

color: white;

}

  

.light {

background-color: white;

color: black;

}
</code></pre>
<p><strong>index.html</strong></p>
<pre><code>&lt;button id="mode"&gt;Toggle Mode&lt;/button&gt;

&lt;script src="script.js"&gt;&lt;/script&gt;
</code></pre>
<p><strong>script.js</strong></p>
<pre><code>let modeBtn = document.querySelector("#mode");

let currMode = "light";

let body = document.querySelector("body");

  

body.classList.add("light");

  

modeBtn.addEventListener("click", () =&gt; {

if (currMode === "light") {

currMode = "dark";

body.classList.add("dark");

body.classList.remove("light");

} else {

currMode = "light";

body.classList.add("light");

body.classList.remove("dark");

}

});

</code></pre>
<p>✅ This is cleaner and more scalable than direct style changes.</p>
<hr>

