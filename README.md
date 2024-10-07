##  Constructors and Destructors in C++

### Overview
<p>
In C++, <strong>constructors</strong> and <strong>destructors</strong> are special member functions that play a crucial role in object-oriented programming. They manage the initialization and cleanup of objects in a class, ensuring that resources are allocated and released properly.
</p>

### Constructors
<p>
A <strong>constructor</strong> is a special member function that is automatically called when an object of a class is created. Its primary purpose is to initialize the object's data members.
</p>

#### Syntax:
<pre><code>class ClassName {
public:
    ClassName() {
        // Constructor code
    }
};
</code></pre>

#### Types of Constructors:

1. Default Constructor:
   <p>A constructor that does not take any arguments.</p>
   <pre><code>ClassName() {
       // Default constructor code
   }
   </code></pre>
   <br>

2. Parameterized Constructor:
   <p>A constructor that takes parameters to initialize the object's data members with specific values.</p>
   <pre><code>ClassName(int x, int y) {
       // Parameterized constructor code
   }
   </code></pre>
   <br>

3. Copy Constructor:
   <p>A constructor that creates a new object as a copy of an existing object.</p>
   <pre><code>ClassName(const ClassName &obj) {
       // Copy constructor code
   }
   </code></pre>
   <br>

### Destructors
<p>
A <strong>destructor</strong> is a special member function that is automatically called when an object goes out of scope or is explicitly deleted. Its main purpose is to release resources allocated by the constructor or during the object's lifetime.
</p>

#### Syntax:
<pre><code>class ClassName {
public:
    ~ClassName() {
        // Destructor code
    }
};
</code></pre>

#### Key Points:
<ul>
<li>The destructor has the same name as the class, but it is preceded by a tilde (~).</li>
<li>Unlike constructors, a class can only have one destructor.</li>
<li>Destructors cannot be overloaded, take arguments, or return values.</li>
</ul>
<br>
<h2 style="text-align: center;">Exp 12 A</h2>

## Aim
<p> To create a C++ program that defines a <code>Date</code> class, which is used to store and display the current date (day, month, and year) entered by the user. </p>

### Algorithm
<p> This algorithm describes the steps involved in the execution of the C++ program that creates a <code>Date</code> class to store and display the current date. </p>
Steps:
<ol> <li> <p><strong>Start</strong></p> </li> <li> <p><strong>Declare variables:</strong><br> <code>day</code>, <code>month</code>, and <code>year</code> as integers to store the day, month, and year respectively.</p> </li> <li> <p><strong>Create a class:</strong> Define a class named <code>Date</code> with the following components:</p> <ul> <li> <p><strong>Private Data Members:</strong><br> <code>day</code>, <code>month</code>, and <code>year</code> to store the date information.</p> </li> <li> <p><strong>Public Constructor:</strong><br> A constructor <code>Date(int d, int m, int y)</code> that initializes the <code>day</code>, <code>month</code>, and <code>year</code> with the values passed as arguments.</p> </li> <li> <p><strong>Public Method:</strong><br> A method <code>displayDate()</code> to display the date in the format "day/month/year".</p> </li> </ul> </li> <li> <p><strong>In the <code>main()</code> function:</strong></p> <ul> <li> <p>Prompt the user to enter today's date in the format <code>(day month year)</code>.</p> </li> <li> <p>Read the values for <code>day</code>, <code>month</code>, and <code>year</code> from the user input.</p> </li> <li> <p>Create an object <code>today</code> of the class <code>Date</code>, passing the user-input values as arguments to the constructor.</p> </li> <li> <p>Call the method <code>displayDate()</code> on the <code>today</code> object to display the entered date.</p> </li> </ul> </li> <li> <p><strong>Stop</strong></p> </li> </ol>

### ** Output **

![image](https://github.com/user-attachments/assets/a42429c5-3fd2-4d90-b83e-a1e4b021a028)

<h2 style="text-align: center;">Exp 12 B</h2>
## Aim

<p> To create a C++ program that defines a <code>Date</code> class, with the constructor defined outside the class, and uses it to store and display the current date (day, month, and year) entered by the user. </p>

## Algorithm

<ol> <li><p>Start.</p></li>
<li><p>Declare a class <code>Date</code> with private data members:</p>
    <ul>
        <li><code>day</code> of type <code>int</code>.</li>
        <li><code>month</code> of type <code>int</code>.</li>
        <li><code>year</code> of type <code>int</code>.</li>
    </ul>
</li>

<li><p>Declare a public constructor <code>Date(int d, int m, int y)</code> to initialize the data members with the values provided by the user.</p></li>

<li><p>Define the constructor <code>Date(int d, int m, int y)</code> outside the class, where:</p>
    <ul>
        <li><code>day = d</code></li>
        <li><code>month = m</code></li>
        <li><code>year = y</code></li>
    </ul>
</li>

<li><p>Declare a public member function <code>displayDate()</code> to display the date in the format <code>day/month/year</code>.</p></li>

<li><p>In the <code>main()</code> function:</p>
    <ul>
        <li><p>Declare variables <code>day</code>, <code>month</code>, and <code>year</code> of type <code>int</code>.</p></li>
        <li><p>Prompt the user to enter the date (day, month, year) and store the input values in the respective variables.</p></li>
        <li><p>Create an object <code>today</code> of the <code>Date</code> class, passing the input values <code>day</code>, <code>month</code>, and <code>year</code> to the constructor.</p></li>
        <li><p>Call the <code>displayDate()</code> function using the <code>today</code> object to display the date.</p></li>
    </ul>
</li>

<li><p>Stop.</p></li>
</ol>

### Output 

![image](https://github.com/user-attachments/assets/c253c2e0-9888-48cf-81e4-83de2148e76b)

<h2 style="text-align: center;">Exp 12 C</h2>

## Aim

<p> To create a C++ program that demonstrates the use of a copy constructor in the <code>Rectangle</code> class, which initializes an object using another object of the same class. The program will also calculate and display the area of the rectangle for both the original and copied objects. </p>

## Algorithm

<ol> <li><p>Start.</p></li>
<li><p>Declare a class <code>Rectangle</code> with the following public data members:</p>
    <ul>
        <li><code>length</code> of type <code>int</code>.</li>
        <li><code>width</code> of type <code>int</code>.</li>
    </ul>
</li>

<li><p>Define a parameterized constructor <code>Rectangle(int l, int w)</code> to initialize the <code>length</code> and <code>width</code> with the values provided by the user.</p></li>

<li><p>Define a copy constructor <code>Rectangle(Rectangle &rect)</code> that initializes a new object using the <code>length</code> and <code>width</code> of another <code>Rectangle</code> object <code>rect</code>.</p></li>

<li><p>Declare a member function <code>calculateArea()</code> that calculates and returns the area of the rectangle by multiplying <code>length</code> and <code>width</code>.</p></li>

<li><p>Declare a member function <code>display()</code> to display the <code>length</code>, <code>width</code>, and area of the rectangle using the <code>calculateArea()</code> function.</p></li>

<li><p>In the <code>main()</code> function:</p>
    <ul>
        <li><p>Declare variables <code>l</code> and <code>w</code> of type <code>int</code> to store the length and width of the rectangle.</p></li>
        <li><p>Prompt the user to enter the length and width, and store the input values in <code>l</code> and <code>w</code>.</p></li>
        <li><p>Create an object <code>rect1</code> of the <code>Rectangle</code> class, passing <code>l</code> and <code>w</code> to the parameterized constructor.</p></li>
        <li><p>Create a new object <code>rect2</code> using the copy constructor, initializing it with <code>rect1</code>.</p></li>
        <li><p>Display the properties and area of the original rectangle <code>rect1</code> using the <code>display()</code> function.</p></li>
        <li><p>Display the properties and area of the copied rectangle <code>rect2</code> using the <code>display()</code> function.</p></li>
    </ul>
</li>

<li><p>Stop.</p></li>
</ol>

### Output

![image](https://github.com/user-attachments/assets/d910d0cd-04ff-4db7-b1c4-725ea0372faf)

<h2 style="text-align: center;">Exp 12 D</h2>

## Aim

<p> To create a C++ program that demonstrates the use of a parameterized constructor in the <code>Numbers</code> class to initialize two integer data members and display their values. </p>

## Algorithm

<ol> <li><p>Start.</p></li>
<li><p>Declare a class <code>Numbers</code> with two public data members:</p>
    <ul>
        <li><code>num1</code> of type <code>int</code>.</li>
        <li><code>num2</code> of type <code>int</code>.</li>
    </ul>
</li>

<li><p>Define a parameterized constructor <code>Numbers(int n1, int n2)</code> to initialize <code>num1</code> and <code>num2</code> with the values provided by the user.</p></li>

<li><p>Declare a member function <code>displayNumbers()</code> to display the values of <code>num1</code> and <code>num2</code>.</p></li>

<li><p>In the <code>main()</code> function:</p>
    <ul>
        <li><p>Declare variables <code>a</code> and <code>b</code> of type <code>int</code> to store the user input values.</p></li>
        <li><p>Prompt the user to enter two numbers and store the input values in <code>a</code> and <code>b</code>.</p></li>
        <li><p>Create an object <code>numbers</code> of the <code>Numbers</code> class, passing <code>a</code> and <code>b</code> to the parameterized constructor.</p></li>
        <li><p>Call the <code>displayNumbers()</code> function to display the values of <code>num1</code> and <code>num2</code>.</p></li>
    </ul>
</li>

<li><p>Stop.</p></li>
</ol>

## Output

![image](https://github.com/user-attachments/assets/5c52d452-28ea-4073-8136-fe80d831e2d6)

<h2 style="text-align: center;">Exp 12 E</h2>

## Aim

<p> To create a C++ program that demonstrates the use of a default constructor to initialize the data members of a class and a destructor to clean up resources when the object is destroyed. </p>

## Algorithm

<ol> <li><p>Start.</p></li>
<li><p>Declare a class <code>Numbers</code> with two public data members:</p>
    <ul>
        <li><code>num1</code> of type <code>int</code>.</li>
        <li><code>num2</code> of type <code>int</code>.</li>
    </ul>
</li>

<li><p>Define a default constructor <code>Numbers()</code> to prompt the user for two integer values and initialize <code>num1</code> and <code>num2</code> with those values.</p></li>

<li><p>Define a destructor <code>~Numbers()</code> to display a message when the object is destroyed.</p></li>

<li><p>Declare a member function <code>displayNumbers()</code> to display the values of <code>num1</code> and <code>num2</code>.</p></li>

<li><p>In the <code>main()</code> function:</p>
    <ul>
        <li><p>Create an object <code>numbers</code> of the <code>Numbers</code> class, which automatically calls the default constructor to initialize the object.</p></li>
        <li><p>Call the <code>displayNumbers()</code> function to display the values of <code>num1</code> and <code>num2</code>.</p></li>
    </ul>
</li>

<li><p>The destructor is automatically called when the object goes out of scope, displaying a message.</p></li>

<li><p>Stop.</p></li>
</ol>

## Output


![image](https://github.com/user-attachments/assets/6915fbeb-4898-42cb-9647-03c2231822e7)
