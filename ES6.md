<h2 id="es6">ES6</h2>
<ul>
<li>ES6 also known as esnext or es2015</li>
</ul>
<h3 id="tooling">Tooling</h3>
<ul>
<li>To work with ES6 we need a javascript <strong>transpiler</strong>,i.e. code in newer version of javascript(i.e. es6) and transpile into older version (es5) of javascript because some of the does not support es6.</li>
<li>Use <em><strong>babel</strong></em> to transpile es6 into es5 for static build</li>
</ul>
<h3 id="destructuring">Destructuring</h3>
<p>To unpack values from arrays, or properties from objects, into distinct variables</p>
<pre><code>let arr =  ["John",  "Smith"]
// destructuring assignment 
// sets firstName = arr[0] 
// and surname = arr[1] 
let [firstName, surname] = arr;
console.log(firstName,lastname); //John,Smith
</code></pre>
<p>we can also write as this…</p>
<pre><code>let  [firstName, surname]  =  "John Smith".split(' ');
alert(firstName);  // John  
alert(surname);  // Smith
</code></pre>
<ul>
<li>Ignore element by , (commas)<br>
<code>let [firstName, , title] = ["Julius", "Caesar", "Consul", "of the Roman Republic"];</code></li>
<li>We can use any “assignables” at the left side.**</li>
</ul>
<pre><code>let user =  {};  
[user.name, user.surname]="John Smith".split(' ');
alert(user.name);  // John  
alert(user.surname);  // Smith
</code></pre>
<ul>
<li>
<h5 id="object-destructure">Object Destructure</h5>
</li>
</ul>
<pre><code>const user = {
    id: 42,
    is_verified: true
};
const {id, is_verified} = user;
</code></pre>
<ul>
<li>
<h5 id="rest-destructuring">Rest Destructuring</h5>
</li>
</ul>
<pre><code>let {a, b, ...rest} = {a: 10, b: 20, c: 30, d: 40}
console.log(a,b) //10,20
console.log(rest) // {c:30,d:40}
</code></pre>
<ul>
<li>
<h5 id="swap-trick">Swap Trick</h5>
</li>
</ul>
<pre><code>let guest = "Jane";  
let admin ="Pete";  
// Let's swap the values:make guest=Pete, admin=Jane
[guest, admin] = [admin, guest];
console.log(guest,admin)
</code></pre>
<h3 id="spread-operator-...--rest-parameter...">Spread Operator … &amp; Rest Parameter…</h3>
<p>Spread operator unpacks elements of iterable objects such as arrays, sets, and maps into a list.<br>
e.g.<br>
<code>var variablename1 = [...value];</code></p>
<pre><code>Math.max(1,3,5) // 5
Math.max([1,3,5]) // NaN
console.log(...[1,3,4]) // 1,3,4
Math.max(...[1,3,5]) // 5
</code></pre>
<p>Spread e.g.</p>
<pre><code>let s1=[4,5,6];
let s2=[6,7,8];
let m=[...a,...b];
console.log(m)  //[4,5,6,6,7,8]
</code></pre>
<pre><code>let str =  "Hello";  
alert(  [...str]  );  // H,e,l,l,o
</code></pre>
<p>The spread syntax internally uses iterators to gather elements, the same way as <code>for..of</code> does.<br>
So, for a string, <code>for..of</code> returns characters and <code>...str</code> becomes <code>"H","e","l","l","o"</code>.<br>
For this particular task we could also use <code>Array.from</code>, because it converts an iterable (like a string) into an array:</p>
<p><em><strong>Key Note</strong></em></p>
<ul>
<li>By using the spread operator we made sure that the original array is not affected whenever we alter the new array.</li>
</ul>
<pre><code>
</code></pre>
<p><strong>Rest parameter</strong> is also denoted by three dots (…). However, it packs remaining arguments of a function into an array.</p>
<p>Many JavaScript built-in functions support an arbitrary number of arguments.</p>
<ul>
<li>The rest parameters must be at the end <code>function sum(a,b,..rest){..}</code></li>
<li>There is also a special array-like object named <code>arguments</code> that contains all arguments by their index.</li>
</ul>
<pre><code>function showName(){
 console.log(arguments[0]);
 console.log(arguments[1]);
 console.log(arguments[2]);
}
showName('Hello','Name','Mobile2'); // 

// https://jstools-tripathi-4zrtcs.stackblitz.io
</code></pre>
<h3 id="this">this</h3>
<p>The JavaScript <code>this</code> keyword refers to the object it belongs to.</p>

