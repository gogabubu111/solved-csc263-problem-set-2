Download Link: https://assignmentchef.com/product/solved-csc263-problem-set-2
<br>
<h1></h1>

Answer each question completely, always justifying your claims and reasoning. Your solution will be graded not only on correctness, but also on clarity. Answers that are technically correct that are hard to understand will not receive full marks. Mark values for each question are contained in the [square brackets].

<strong>You may work in groups of up to THREE to complete these questions.</strong>

<ol>

 <li><strong>[10] </strong>Suppose that we want to generate a BST by inserting the keys 1 through <em>n </em>into an initially empty BST (assume <em>n &gt; </em>1). Assume that the insert sequence is a random permutation of [1<em>,</em>2<em>,</em>3<em>,…,n</em>] and each permutation is equally likely to occur. Answer the following questions.

  <ul>

   <li>What is the maximum possible height of the generated BST? Describe <strong>three </strong>different insert sequences that would result in a BST with the maximum height.</li>

   <li>By picking a random permutation of [1<em>,</em>2<em>,</em>3<em>,…,n</em>] as the insert sequence, what is the probability that the resulting BST has the maximum height? Show detailed steps of your calculation with clear justification.</li>

  </ul></li>

 <li><strong>[10] </strong>A PowerStack consists of a potentially infinite series of stacks <em>S</em><sub>0</sub><em>,S</em><sub>1</sub><em>,S</em><sub>2</sub><em>,…</em>, where the <em>i</em>-th stack <em>S<sub>i </sub></em>can hold up to 2<em><sup>i </sup></em> In this question, we study the following PowerPush operation for an PowerStack.</li>

</ol>

The main working mechanism of a PowerPush is the following: whenever there is an attempt to Push an element onto any <strong>full </strong>stack <em>S<sub>i</sub></em>, we first Pop <strong>all </strong>the elements off <em>S<sub>i </sub></em>and Push them onto stack <em>S<sub>i</sub></em><sub>+1 </sub>to make room. If <em>S<sub>i</sub></em><sub>+1 </sub>is already full, we first recursively move all its members to <em>S<sub>i</sub></em><sub>+2</sub>, etc. Each PowerPush operation starts by attempting to Push to <em>S</em><sub>0</sub>. Assume that each elementary Push and Pop operation takes 1 unit of time, and the cost of any other operation (e.g., checking if a stack is full) is ignored.

<ul>

 <li>In the worst case, how many units of time does it take to PowerPush one new element onto a PowerStack containing <em>n </em>elements? Your answer should be in exact form (i.e., not in asymptotic notation) and justified.</li>

 <li>Consider performing a sequence of <em>n </em>PowerPush operations onto a PowerStack that is initially empty. Show that the amortized runtime per operation is O(log<em>n</em>).</li>

</ul>

<strong>Hint</strong>: You can first try to analyze it using the aggregate method, which is doable but quite complicated; then you should try the accounting method and realize that it becomes much simpler.

<ol start="3">

 <li><strong>[10] </strong>In this problem, you will design the data structure for implementing an ADT called SHOPPING-SET. Below is the description of the ADT.</li>

</ol>

<strong>Objects: </strong>A collection of items objects for sale. Each item object obj has the following attributes:

<ul>

 <li>name: a string which is the name of the item. Each item has a unique name, i.e., no two items have the same name.</li>

 <li>price: a decimal value such as 12<em>.</em>99. For simplicity, assume that the each item’s price is unique, i.e., no two items have the same price.</li>

 <li>rating: a decimal value between 0<em>.</em>0 and 5<em>.</em>0, e.g., 0<em>.</em>012, 3<em>.</em>1415926. For simplicity, assume that each item’s rating value is unique, i.e., no two items have the same rating value.</li>

</ul>

<strong>Operations:</strong>

<ul>

 <li>GET-ITEM(S, name): returns the item object with name name if it exists in the SHOPPING-SET S; returns NIL if the item does not exist in S.</li>

 <li>ADD-ITEM(S, obj): Add an item object obj to the SHOPPING-SET S. You may assume that obj has a unique name, a unique price and a unique rating.</li>

 <li>TOP-RATED-UNDER-PRICE(S, p): returns the top-rated item object (item with the maximum rating value) whose price is less than or equal to p.</li>

</ul>

<strong>Requirements: </strong>Let <em>n </em>be the size of <em>S</em>,

<ul>

 <li>GET-ITEM(S, name) must have average-case runtime O(1).</li>

 <li>ADD-ITEM(S, obj) must have worst-case runtime O(log<em>n</em>).</li>

 <li>TOP-RATED-UNDER-PRICE(S, p) must have worst-case runtime O(log<em>n</em>).</li>

</ul>

Give a <em>detailed </em>description of the design of your data structure by answering the following questions.

<ul>

 <li>Which data structure(s) do you use in your design? What is the key of each data structure? What attributes does each node in your data structure(s) keep?</li>

 <li>Explain concisely in English how your GET-ITEM operation works, and justify its runtime.</li>

 <li>Explain concisely in English how your ADD-ITEM operation works, and justify its runtime. In particular, explain why all the attributes kept in each node can be maintained efficiently upon the addition of the new node.</li>

 <li>Explain how your TOP-RATED-UNDER-PRICE works and <strong>write the pseudocode </strong>of this operation, then justify its runtime.</li>

</ul>

<strong>Note</strong>: As usual, please do <strong>not </strong>repeat algorithm details or runtime analyses from class or the textbook — just directly refer to known results as needed.

<h1>Programming Question</h1>

The best way to learn a data structure or an algorithm is to code it up. In each problem set, we will have a programming exercise for which you will be asked to write some code and submit it. You may also be asked to include a write-up about your code in the PDF/TEXfile that you submit. Make sure to <strong>maintain your academic integrity </strong>carefully, and protect your own work. The code you submit will be checked for plagiarism. It is much better to take the hit on a lower mark than risking much worse consequences by committing an academic offence.

<ol start="4">

 <li><strong>[10] </strong>In this problem, your task is to solve the following equation.</li>

</ol>

where <em>x</em><sub>1</sub><em>,x</em><sub>2</sub><em>,…,x</em><sub>5 </sub>are unknowns, and <em>A,B,C,D,E,S </em>are given constants. All these constants are integers and can be positive, negative, or zero.

You will write a Python program that, given the values of <em>A</em>, <em>B</em>, <em>C</em>, <em>D</em>, <em>E</em>, and <em>S</em>, finds <strong>the number of unique integer solutions </strong>to the above equation, each of which satisfies the following condition:

−50 ≤ <em>x<sub>i </sub></em>≤ 50 ∀<em>i </em>∈{1<em>,</em>2<em>,</em>3<em>,</em>4<em>,</em>5}

The header of your function is as follows. The test cases in the docstring can be used to verify the correctness of your program.

<ul>

 <li>def solve(A, B, C, D, E, S):</li>

 <li>’’’</li>

 <li>Return the number of unique integer solutions</li>

 <li>where each integer is in the range [-50, 50]</li>

</ul>

5

6                                                   Precondition: A, B, C, D, E, S are integers in the range [-1000, 1000]

7

<ul>

 <li>&gt;&gt;&gt; solve(12, 34, 56, 78, 9, 10)</li>

 <li>159</li>

 <li>&gt;&gt;&gt; solve(148, -42, 21, 77, -2, -263)</li>

 <li>112</li>

 <li>&gt;&gt;&gt; solve(0, 0, 0, 0, 0, 0)</li>

 <li>10510100501</li>

 <li>’’’</li>

</ul>

<strong>Requirements:</strong>

<ul>

 <li>Your solve() function must be able to return the correct answer <strong>within 5 seconds </strong>(measured when running on the utm.utoronto.ca server). It’s not hard to think of a na¨ıve algorithm which enumerates and checks all possible 5-tuples of the unknowns, but this algorithm will obviously be too slow.</li>

 <li>You are <strong>not </strong>allowed to use the built-in Python set or dict in your code, and you are <strong>not </strong>allowed to use any import statement in your code.</li>

 <li>Your code must be written in Python 3, and filename must be py as required my MarkUs.</li>

</ul>