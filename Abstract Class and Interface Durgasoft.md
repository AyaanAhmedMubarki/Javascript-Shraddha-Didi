---


---

<h1 id="durgasoft-notes">Durgasoft Notes</h1>
<h2 id="interface-and-abstract-class">Interface and Abstract Class</h2>
<hr>
<h2 id="new-operator-vs-constructor">1) new Operator vs Constructor</h2>
<p>The main purpose of ‘new’ operator is to CREATE AN OBJECT<br>
The main purpose of Constructor is to INITIALISE AN OBJECT.</p>
<p>First object will be created by using new operator and then initialization will be performed by Constructor</p>
<p>Example:</p>
<pre><code>class Student
{
	String name;
	int rollno;

	Student(String name,int rollno)
		{
			this.name = name;	
			this.rollno = rollno;
		}
}
  

Student ob = new Student("Durga",101);
</code></pre>
<p>Explanation:</p>
<p>new --&gt; responsible to create Object<br>
Student(“Durga”,101) --&gt; to initialise object</p>
<hr>
<h2 id="parent-constructor-execution-during-child-object-creation">2) Parent Constructor Execution During Child Object Creation</h2>
<p>Whenever a <strong>child class object</strong> is created:</p>
<ul>
<li>The <strong>parent class constructor</strong> executes automatically.</li>
<li>This is done to initialize the <strong>inherited instance variables</strong>.</li>
</ul>
<p>Example:</p>
<pre><code>class Person
{
	String name;
	int age;

	Person(String name,int age)
	{
		this.name = name;
		this.age = age;
	}
}

  
class Student extends Person
{
	int rollno;
	int marks;
		
	Student(String name, int age, int rollno, int marks)
	{
		super(name,age);
		this.rollno = rollno;
		this.marks = marks;
	}
}

Student ob = new Student("Durga",48,101,90);
</code></pre>
<h3 id="initialization-breakdown">Initialization Breakdown</h3>
<ul>
<li><code>name</code>, <code>age</code> → initialized by <strong>parent constructor</strong></li>
<li><code>rollno</code>, <code>marks</code> → initialized by <strong>child constructor</strong></li>
</ul>
<p><strong>Note:</strong><br>
In the above program, both <strong>Parent and Child Constructor</strong> executed for <strong>Child Object initialisation</strong> only</p>
<hr>
<h2 id="parent-constructor-executes-but-parent-object-is-not-created">3) Parent Constructor Executes But Parent Object is NOT Created</h2>
<p>Whenever we are creating Child Class object, Parent Constructor will be executed BUT Parent Object won’t be created.</p>
<p>Example:</p>
<pre><code>class P 
{
	P() 
	{
		System.out.println(this.hashCode());
	}
}

class C extends P 
{
	C() 
	{
		System.out.println(this.hashCode());
		}
}


class Test 
{
	public static void main(String[] args) 
	{
		C ob = new C();
		System.out.println(ob.hashCode());
	}
}
</code></pre>
<p>Output:</p>
<p>5442986<br>
5442986<br>
5442986</p>
<p>In the above example, we just created ONLY Child Class object, but both Parent and Child Constructor executed for that Child Class Object</p>
<hr>
<h2 id="constructor-in-abstract-class">4) Constructor in Abstract Class</h2>
<h3 id="important-rules">Important Rules</h3>
<ul>
<li>We <strong>cannot create objects</strong> for an abstract class (directly or indirectly).</li>
<li>Abstract classes <strong>CAN have constructors</strong>.</li>
</ul>
<p>Need for Constructor in Abstract Class(even though object can’t be created):</p>
<h3 id="why-abstract-classes-need-constructors">Why Abstract Classes Need Constructors</h3>
<ul>
<li>Abstract classes can have <strong>instance variables</strong>.</li>
<li>Constructors are used to <strong>initialize those instance variables</strong>.</li>
<li>This improves <strong>code reusability</strong>.</li>
</ul>
<hr>
<h3 id="without-constructor-in-abstract-class-bad-design">Without Constructor in Abstract Class (Bad Design):</h3>
<pre><code>abstract class Person
{
	String name;
	int age;
}

  

class Student extends Person

{
	int rollno;
	int marks;
	Student(String name, int age, int rollno, int marks)
	{
	this.name = name;
	this.age = age;
	this.rollno = rollno;
	this.marks = marks;
	}
}
</code></pre>
<p>Problem:</p>
<ul>
<li>Same initialization code repeated in every child class.</li>
</ul>
<hr>
<h3 id="with-constructor-in-abstract-class">With Constructor in Abstract Class:</h3>
<pre><code>abstract class Person  
{  
	String name;  
	int age;
	Person(String name, int age)  
	{  
	    this.name = name;  
	    this.age = age;  
	}  
}


class Student extends Person  
{  
	int rollno;  
	int marks;
	Student(String name, int age, int rollno, int marks)  
	{  
	    super(name, age);  
	    this.rollno = rollno;  
	    this.marks = marks;  
	}  
}
</code></pre>
<p>Benefit:</p>
<ul>
<li>Parent variables initialized in one place</li>
<li>Cleaner and reusable code</li>
</ul>
<hr>
<h2 id="constructor-in-abstract-class-vs-interface">5) Constructor in Abstract Class vs Interface</h2>
<h3 id="common-point">Common Point</h3>
<ul>
<li>We <strong>cannot create objects</strong> of both abstract class and interface.</li>
</ul>
<h3 id="key-differences">Key Differences:</h3>
<pre><code>		Abstract Class						Interface

Can have instance variables			All variables are public static final

Can have constructors				Cannot have constructors

Constructor initializes instance 	No instance variables, so no constructor
variables		
</code></pre>
<p>Example:</p>
<pre><code>abstract class Person
{
	String name;
	int age;
	Person(String name,int age)
	{
		this.name = name;
		this.age = age;
	}
}
----------------------------------------------------------
interface Demo
{
	int x=10;
}
</code></pre>
<hr>
<h2 id="can-we-replace-interface-with-abstract-class">6) Can We Replace Interface with Abstract Class?</h2>
<p>If everything is Abstract, it is highly recommended to go with Interface but not Abstract Class.</p>
<p>We can replace Interface with Abstract Class, but it is not a good programming practice.<br>
Eg: Hiring IAS officer for sweeping purpose</p>
<hr>
<h3 id="interface-vs-abstract-class-comparison">Interface vs Abstract Class Comparison</h3>
<pre><code>Interface:								     Abstract Class:
-----------------------------------------------------------------------------------------
interface X									abstract class X
{											{

}											}


1.  While implementing Interface, 			    While extending Abstract class,
    we can extend any other class,				we cant extend any other class, 
    and hence we won't miss Inheritance 		and hence we are missing Inheritance
    benefit										benefit

class Test extends A implements X   			class Test extends X,A
{												{

}												}
VALID											INVALID

----------

2.  In this case, object creation              In this case, object creation
    is not costly							   is costly

class Test implements X						   class Test extends X 
{											   {
	Test t = new Test();      						Test t = new Test();
}											   }

(2 mins)									   (20 mins)

 










</code></pre>
<hr>
<h2 id="objective-questions-">Objective Questions :</h2>
<p>Which of the following are valid?</p>
<ol>
<li>
<p>The purpose of constructor is to create an object. – Invalid<br>
Explanation:<br>
Object creation is done by the new keyword, not by the constructor.<br>
Constructor is executed only after the object is created.</p>
</li>
<li>
<p>The purpose of constructor is to initialize an object but not to create object. – Valid<br>
Explanation:<br>
Constructor assigns initial values to instance variables.<br>
Object creation happens first, then constructor runs.</p>
</li>
<li>
<p>Once constructor completes then only object creation completes. – Invalid<br>
Explanation:<br>
Object creation completes before constructor execution begins.</p>
</li>
<li>
<p>First object will be created and then constructor will be executed. – Valid<br>
Explanation:<br>
Memory allocation happens first, then constructor initializes the object.</p>
</li>
<li>
<p>The purpose of new keyword is to create object and the purpose of constructor is to initialize that object. – Valid<br>
Explanation:<br>
The new keyword creates the object, and the constructor initializes it.</p>
</li>
<li>
<p>We can’t create object for abstract class directly but indirectly we can create. – Invalid<br>
Explanation:<br>
We cannot create an object for an abstract class either directly or indirectly.<br>
Only the abstract class constructor executes when a concrete subclass object is created.</p>
</li>
<li>
<p>Whenever we are creating child class object automatically parent class object will be created internally. – Invalid<br>
Explanation:<br>
Parent class constructor executes, but parent object is not created separately.</p>
</li>
<li>
<p>Whenever we are creating child class object automatically abstract class constructor will be executed. – Valid<br>
Explanation:<br>
If the parent is an abstract class, its constructor executes during child object creation.</p>
</li>
<li>
<p>Whenever we are creating child class object automatically parent object will be created. – Invalid<br>
Explanation:<br>
Only the child object is created. Parent part exists inside the child object.</p>
</li>
<li>
<p>Whenever we are creating child class object automatically parent constructor will be executed but parent object won’t be created. – Valid<br>
Explanation:<br>
When a child class object is created, the parent class constructor executes automatically.<br>
However, no separate parent object is created; only the child object exists.</p>
</li>
<li>
<p>Either directly or indirectly we can’t create object for abstract class and hence constructor concept is not applicable for abstract class. – Invalid<br>
Explanation:<br>
Although we cannot create an object for an abstract class, abstract classes can have constructors.<br>
These constructors are executed during child class object creation.</p>
</li>
<li>
<p>Interface can contain constructor. – Invalid<br>
Explanation:<br>
Interfaces cannot have constructors because interfaces cannot be instantiated.</p>
</li>
</ol>

