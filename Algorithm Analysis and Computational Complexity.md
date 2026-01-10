###### Lecture Notes on Algorithm Analysis and Computational Complexity (Fourth Edition)

 Ian Parberry[1]
 Department of Computer Sciences University of North Texas

 December 2001

1Author’s address: Department of Computer Sciences, University of North Texas, P.O. Box 311366, Denton, TX
76203–1366, U.S.A. Electronic mail: ian@cs.unt.edu.


-----

##### g

###### This work is copyright Ian Parberry. All rights reserved. The author offers this work, retail value US$20, free of charge under the following conditions:

G  No part of this work may be made available on a public forum (including, but not limited to a web

###### page, ftp site, bulletin board, or internet news group) without the written permission of the author.


G  No part of this work may be rented, leased, or offered for sale commercially in any form or by any

###### means, either print, electronic, or otherwise, without written permission of the author.

G  If you wish to provide access to this work in either print or electronic form, you may do so by

###### providing a link to, and/or listing the URL for the online version of this license agreement: http://hercule.csci.unt.edu/ian/books/free/license.html. You may not link directly to the PDF file.


G  All printed versions of any or all parts of this work must include this license agreement. Receipt of

###### a printed copy of this work implies acceptance of the terms of this license agreement. If you have received a printed copy of this work and do not accept the terms of this license agreement, please destroy your copy by having it recycled in the most appropriate manner available to you.

G  You may download a single copy of this work. You may make as many copies as you wish for

###### your own personal use. You may not give a copy to any other person unless that person has read, understood, and agreed to the terms of this license agreement.


G  You undertake to donate a reasonable amount of your time or money to the charity of your choice

###### as soon as your personal circumstances allow you to do so. The author requests that you make a cash donation to The National Multiple Sclerosis Society in the following amount for each work that you receive:
H  $5 if you are a student,
H  $10 if you are a faculty member of a college, university, or school,
H  $20 if you are employed full-time in the computer industry.
###### Faculty, if you wish to use this work in your classroom, you are requested to:
H  encourage your students to make individual donations, or
H  make a lump-sum donation on behalf of your class.
###### If you have a credit card, you may place your donation online at https://www.nationalmssociety.org/donate/donate.asp. Otherwise, donations may be sent to:

 National Multiple Sclerosis Society - Lone Star Chapter 8111 North Stadium Drive Houston, Texas 77054

 If you restrict your donation to the National MS Society's targeted research campaign, 100% of your money will be directed to fund the latest research to find a cure for MS.

 For the story of Ian Parberry's experience with Multiple Sclerosis, see http://www.thirdhemisphere.com/ms.


-----

###### Preface

These lecture notes are almost exact copies of the overhead projector transparencies that I use in my CSCI
4450 course (Algorithm Analysis and Complexity Theory) at the University of North Texas. The material
comes from

textbooks on algorithm design and analysis,

_•_
textbooks on other subjects,

_•_
research monographs,

_•_
papers in research journals and conferences, and

_•_
my own knowledge and experience.

_•_

Be forewarned, this is not a textbook, and is not designed to be read like a textbook. To get the best use
out of it you must attend my lectures.

Students entering this course are expected to be able to program in some procedural programming language
such as C or C++, and to be able to deal with discrete mathematics. Some familiarity with basic data
structures and algorithm analysis techniques is also assumed. For those students who are a little rusty, I
have included some basic material on discrete mathematics and data structures, mainly at the start of the
course, partially scattered throughout.

Why did I take the time to prepare these lecture notes? I have been teaching this course (or courses very
much like it) at the undergraduate and graduate level since 1985. Every time I teach it I take the time to
improve my notes and add new material. In Spring Semester 1992 I decided that it was time to start doing
this electronically rather than, as I had done up until then, using handwritten and xerox copied notes that
I transcribed onto the chalkboard during class.

This allows me to teach using slides, which have many advantages:

They are readable, unlike my handwriting.

_•_
I can spend more class time talking than writing.

_•_
I can demonstrate more complicated examples.

_•_
I can use more sophisticated graphics (there are 219 figures).

_•_

Students normally hate slides because they can never write down everything that is on them. I decided to
avoid this problem by preparing these lecture notes directly from the same source files as the slides. That
way you don’t have to write as much as you would have if I had used the chalkboard, and so you can spend
more time thinking and asking questions. You can also look over the material ahead of time.

To get the most out of this course, I recommend that you:

Spend half an hour to an hour looking over the notes before each class.

_•_


-----

**iv** **PREFACE**

Attend class. If you think you understand the material without attending class, you are probably kidding

_•_
yourself. Yes, I do expect you to understand the details, not just the principles.
Spend an hour or two after each class reading the notes, the textbook, and any supplementary texts

_•_
you can find.
Attempt the ungraded exercises.

_•_
Consult me or my teaching assistant if there is anything you don’t understand.

_•_

The textbook is usually chosen by consensus of the faculty who are in the running to teach this course. Thus,
it does not necessarily meet with my complete approval. Even if I were able to choose the text myself, there
does not exist a single text that meets the needs of all students. I don’t believe in following a text section
by section since some texts do better jobs in certain areas than others. The text should therefore be viewed
as being supplementary to the lecture notes, rather than vice-versa.


-----

**Summary**


###### Algorithms Course Notes Introduction

 Ian Parberry[∗]

 Fall 2001

Therefore he asked for 3.7 10[12] bushels.
_×_


What is “algorithm analysis”?

_•_
What is “complexity theory”?

_•_
What use are they?

_•_

**The Game of Chess**

According to legend, when Grand Vizier Sissa Ben
Dahir invented chess, King Shirham of India was so
taken with the game that he asked him to name his
reward.

The vizier asked for

One grain of wheat on the first square of the

_•_
chessboard
Two grains of wheat on the second square

_•_
Four grains on the third square

_•_
Eight grains on the fourth square

_•_
etc.

_•_

How large was his reward?

How many grains of wheat?

63
�

2[i] = 2[64] 1 = 1.8 10[19].
_−_ _×_
_i=0_

A bushel of wheat contains 5 10[6] grains.
_×_

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


The price of wheat futures is around $2.50 per
bushel.

Therefore, he asked for $9.25 10[12] = $92 trillion
_×_
at current prices.

**The Time Travelling Investor**

A time traveller invests $1000 at 8% interest compounded annually. How much money does he/she
have if he/she travels 100 years into the future? 200
years? 1000 years?

_Years_ _Amount_

100 $2.9 10[6]
_×_

200 $4.8 10[9]
_×_

300 $1.1 10[13]
_×_

400 $2.3 10[16]
_×_

500 $5.1 10[19]
_×_

1000 $2.6 10[36]
_×_

**The Chinese Room**

Searle (1980): Cognition cannot be the result of a
formal program.

Searle’s argument: a computer can compute something without really understanding it.

Scenario: Chinese room = person + look-up table

The Chinese room passes the Turing test, yet it has
no “understanding” of Chinese.

Searle’s conclusion: A symbol-processing program
cannot truly understand.

**Analysis of the Chinese Room**

|Years|Amount|
|---|---|
|100 200 300 400 500 1000|$2.9 106 × $4.8 109 × $1.1 1013 × $2.3 1016 × $5.1 1019 × $2.6 1036 ×|


1


-----

How much space would a look-up table for Chinese
take?

A typical person can remember seven objects simultaneously (Miller, 1956). Any look-up table must
contain queries of the form:

“Which is the largest, a `<noun>1,` a
```
  <noun>2, a <noun>3, a <noun>4, a <noun>5,

```
a <noun>6, or a <noun>7?”,

There are at least 100 commonly used nouns. Therefore there are at least 100 99 98 97 96 95 94 =
_·_ _·_ _·_ _·_ _·_ _·_
8 10[13] queries.
_×_

**100 Common Nouns**

aardvark duck lizard sardine
ant eagle llama scorpion
antelope eel lobster sea lion
bear ferret marmoset seahorse
beaver finch monkey seal
bee fly mosquito shark
beetle fox moth sheep
buffalo frog mouse shrimp
butterfly gerbil newt skunk
cat gibbon octopus slug
caterpillar giraffe orang-utang snail
centipede gnat ostrich snake
chicken goat otter spider
chimpanzee goose owl squirrel
chipmunk gorilla panda starfish
cicada guinea pig panther swan
cockroach hamster penguin tiger
cow horse pig toad
coyote hummingbird possum tortoise
cricket hyena puma turtle
crocodile jaguar rabbit wasp
deer jellyfish racoon weasel
dog kangaroo rat whale
dolphin koala rhinocerous wolf
donkey lion salamander zebra

**Size of the Look-up Table**

The Science Citation Index:

215 characters per line

_•_
275 lines per page

_•_
1000 pages per inch

_•_

Our look-up table would require 1.45 10[8] inches
_×_
= 2, 300 miles of paper = a cube 200 feet on a side.


**The Look-up Table and the Great Pyramid**

**Computerizing the Look-up Table**

Use a large array of small disks. Each drive:

Capacity 100 10[9] characters

_•_ _×_
Volume 100 cubic inches

_•_
Cost $100

_•_

Therefore, 8 10[13] queries at 100 characters per
_×_
query:

8,000TB = 80, 000 disk drives

_•_
cost $8M at $1 per GB

_•_
volume over 55K cubic feet (a cube 38 feet on

_•_
a side)

**Extrapolating the Figures**

Our queries are very simple. Suppose we use 1400
nouns (the number of concrete nouns in the Unix
spell-checking dictionary), and 9 nouns per query
(matches the highest human ability). The look-up
table would require

1400[9] = 2 10[28] queries, 2 10[30] bytes

_•_ _×_ _×_
a stack of paper 10[10] light years high [N.B. the

_•_
nearest spiral galaxy (Andromeda) is 2.1 10[6]
_×_

light years away, and the Universe is at most
1.5 10[10] light years across.]
_×_
2 10[19] hard drives (a cube 198 miles on a side)

_•_ _×_
if each bit could be stored on a single hydrogen

_•_
atom, 10[31] use almost seventeen tons of hydrogen

**Summary**

We have seen three examples where cost increases
exponentially:


2


-----

Chess: cost for an n _n chessboard grows pro-_

_•_ _×_
portionally to 2[n][2].
Investor: return for n years of time travel is

_•_
proportional to 1000 1.08[n] (for n centuries,
_×_
1000 2200[n]).
_×_
Look-up table: cost for an n-term query is pro
_•_
portional to 1400[n].

**Algorithm Analysis and Complexity Theory**

Computational complexity theory = the study of the
cost of solving interesting problems. Measure the
amount of resources needed.

time

_•_
space

_•_

Two aspects:

Upper bounds: give a fast algorithm

_•_
Lower bounds: no algorithm is faster

_•_

Algorithm analysis = analysis of resource usage of
given algorithms

Exponential resource use is bad. It is best to

Make resource usage a polynomial

_•_
Make that polynomial as small as possible

_•_


Y x 10[3]

Linear

5.00 Quadratic

Cubic

4.50 Exponential

Factorial

4.00

3.50

3.00

2.50

2.00

1.50

1.00

0.50

0.00
X

50.00 100.00 150.00

**Motivation**

Why study this subject?

Efficient algorithms lead to efficient programs.

_•_
Efficient programs sell better.

_•_
Efficient programs make better use of hardware.

_•_
Programmers who write efficient programs are

_•_
more marketable than those who don’t!

**Efficient Programs**

Factors influencing program efficiency

Problem being solved

_•_
Programming language

_•_
Compiler

_•_
Computer hardware

_•_
Programmer ability

_•_
Programmer effectiveness

_•_
Algorithm

_•_

**Objectives**

What will you get from this course?

Methods for analyzing algorithmic efficiency

_•_
A toolbox of standard algorithmic techniques

_•_
A toolbox of standard algorithms

_•_

|Col1|Linear|
|---|---|
||Quadratic|
||Cubic|
||Exponential|
||Factorial X|
|||

|Polynomial Good Exponential Bad|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Col10|Col11|Col12|Col13|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
||||||||||||||
||||||||||||||
||||||||||||||
||||||||||||||
||||||||||||||


3


-----

###### Just when YOUJ thought it was safe to take CS courses...

 Discrete Mathematics

 What’s this class like?

 Welcome To CSCI 4450

**Assigned Reading**

CLR, Section 1.1


POA, Preface and Chapter 1.
```
http://hercule.csci.unt.edu/csci4450

```

4


-----

###### Algorithms Course Notes Mathematical Induction

 Ian Parberry[∗]


**Summary**

Mathematical induction:


###### Fall 2001

Fact: Pick any person in the line. If they are Nigerian, then the next person is Nigerian too.


versatile proof technique

_•_
various forms

_•_
application to many types of problem

_•_

**Induction with People**


Question: Are they all Nigerian?

Scenario 4:


Fact 1: The first person is Indonesian.

Fact 2: Pick any person in the line. If all the people
up to that point are Indonesian, then the next person
is Indonesian too.


Question: Are they all Indonesian?

**Mathematical Induction**


Scenario 1:

Fact 1: The first person is Greek.


Fact 2: Pick any person in the line. If they are
Greek, then the next person is Greek too.

Question: Are they all Greek?


###### 1[23456][789]

To prove that a property holds for all IN, prove:


Fact 1: The property holds for 1.

Fact 2: For all n 1, if the property holds for n,
_≥_
then it holds for n + 1.


Scenario 2:

Fact: The first person is Ukranian.


Question: Are they all Ukranian?


Scenario 3:

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


**Alternatives**

There are many alternative ways of doing this:


1


-----

1. The property holds for 1.
2. For all n 2, if the property holds for n 1,
_≥_ _−_
then it holds for n.

There may have to be more base cases:

1. The property holds for 1, 2, 3.
2. For all n 3, if the property holds for n, then
_≥_
it holds for n + 1.

Strong induction:

1. The property holds for 1.
2. For all n 1, if the property holds for all 1
_≥_ _≤_
_m_ _n, then it holds for n + 1._
_≤_

**Example of Induction**

An identity due to Gauss (1796, aged 9):

Claim: For all n IN,
_∈_

1 + 2 + + n = n(n + 1)/2.
_· · ·_

First: Prove the property holds for n = 1.

1 = 1(1 + 1)/2

Second: Prove that if the property holds for n, then
the property holds for n + 1.

Let S(n) denote 1 + 2 + + n.
_· · ·_

Assume: S(n) = n(n + 1)/2 (the induction hypothesis).
Required to Prove:

_S(n + 1) = (n + 1)(n + 2)/2._

_S(n + 1)_
= _S(n) + (n + 1)_
= _n(n + 1)/2 + (n + 1)_ (by ind. hyp.)
= _n[2]/2 + n/2 + n + 1_
= (n[2] + 3n + 2)/2
= (n + 1)(n + 2)/2


This can be solved analytically, but it illustrates the
technique.

Guess: S(n) = an[2] + bn + c for some a, b, c IR.
_∈_

Base: S(1) = 8, hence guess is true provided a + b +
_c = 8._

Inductive Step: Assume: S(n) = an[2] + bn + c.
Required to prove: S(n+1) = a(n+1)[2] +b(n+1)+c.

Now,

_S(n + 1)_ = _S(n) + 5(n + 1) + 3_


**Second Example**

Claim: For all n IN, if 1 + x > 0, then
_∈_

(1 + x)[n] 1 + nx
_≥_

First: Prove the property holds for n = 1.
Both sides of the equation are equal to 1 + x.

Second: Prove that if the property holds for n, then
the property holds for n + 1.

Assume: (1 + x)[n] 1 + nx.
_≥_
Required to Prove:

(1 + x)[n][+1] 1 + (n + 1)x.
_≥_

(1 + x)[n][+1]

= (1 + x)(1 + x)[n]

(1 + x)(1 + nx) (by ind. hyp.)
_≥_
= 1 + (n + 1)x + nx[2]

1 + (n + 1)x (since nx[2] 0)
_≥_ _≥_

**More Complicated Example**


Solve


_S(n) =_


_n_
�(5i + 3)

_i=1_


2


-----

We want


= (an[2] + bn + c) + 5(n + 1) + 3

= _an[2]_ + (b + 5)n + c + 8

_an[2]_ + (b + 5)n + c + 8
= _a(n + 1)[2]_ + b(n + 1) + c
= _an[2]_ + (2a + b)n + (a + b + c)


Each pair of coefficients has to be the same.

_an + (b+5)n + (c+8) = an + (2a+b)n + (a+b+c)2_ _2_

The first coefficient tells us nothing.

The second coefficient tells us b+5 = 2a+b, therefore
_a = 2.5._

We know a + b + c = 8 (from the Base), so therefore
(looking at the third coefficient), c = 0.

Since we now know a = 2.5, c = 0, and a + _b_ + _c = 8,_
we can deduce that b = 5.5.

Therefore S(n) = 2.5n[2] + 5.5n = n(5n + 11)/2.

**Complete Binary Trees**

Claim: A complete binary tree with k levels has exactly 2[k] 1 nodes.
_−_

Proof: Proof by induction on number of levels. The
claim is true for k = 1, since a complete binary tree
with one level consists of a single node.

Suppose a complete binary tree with k levels has 2[k]
_−_
1 nodes. We are required to prove that a complete
binary tree with k + 1 levels has 2[k][+1] 1 nodes.
_−_

A complete binary tree with k +1 levels consists of a
root plus two trees with k levels. Therefore, by the
induction hypothesis the total number of nodes is

1 + 2(2[k] 1) = 2[k][+1] 1
_−_ _−_


as required.

###### Tree with k Tree with k levels levels

**Another Example**

Prove that for all n 1,
_≥_

_n_
� 1/2[i] _< 1._

_i=1_

The claim is clearly true for n = 1. Now assume
that the claim is true for n.

|Col1|Col2|Col3|
|---|---|---|
||||


_n+1_
� 1/2[i]

_i=1_

1 1
=
2 [+ 1]4 [+ 1]8 [+][ · · ·][ +] 2[n][+1]

1 � 1
=
2 [+ 1]2 2 [+ 1]4 [+ 1]8 [+][ · · ·][ + 1]2[n]


�


1
=
2 [+ 1]2


_n_
� 1/2[i]

_i=1_


1
_<_ (by ind. hyp.)
2 [+ 1]2

_[·][ 1]_

= 1

**A Geometric Example**

Prove that any set of regions defined by n lines in the
plane can be coloured with only 2 colours so that no
two regions that share an edge have the same colour.


3


-----

|Col1|L|
|---|---|


Proof by induction on n. True for n = 1 (colour one
side light, the other side dark). Now suppose that
the hypothesis is true for n lines.

Suppose we are given n + 1 lines in the plane. Remove one of the lines, and colour the remaining
_L_
regions with 2 colours (which can be done, by the induction hypothesis). Replace . Reverse all of the
_L_
colours on one side of the line.

Consider two regions that have a line in common. If
that line is not, then by the induction hypothe_L_
sis, the two regions have different colours (either the
same as before or reversed). If that line is, then
_L_
the two regions formed a single region before was
_L_
replaced. Since we reversed colours on one side of
_L_
only, they now have different colours.

**A Puzzle Example**

A triomino is an L-shaped figure formed by the juxtaposition of three unit squares.

An arrangement of triominoes is a tiling of a shape
if it covers the shape exactly without overlap. Prove
by induction on n 1 that any 2[n] 2[n] grid that
_≥_ _×_
is missing one square can be tiled with triominoes,
regardless of where the missing square is.


Proof by induction on n. True for n = 1:

Now suppose that the hypothesis is true for n. Suppose we have a 2[n][+1] 2[n][+1] grid with one square
_×_
missing.

###### NW NE

 SW SE

Divide the grid into four 2[n] 2[n] subgrids. Suppose
_×_
the missing square is in the NE subgrid. Remove
the squares closest to the center of the grid from the
other three subgrids. By the induction hypothesis,
all four subgrids can be tiled. The three removed
squares in the NW, SW, SE subgrids can be tiled
with a single triomino.

**A Combinatorial Example**

A Gray code is a sequence of 2[n] _n-bit binary num-_
bers where each adjacent pair of numbers differs in
exactly one bit.

|NW|Col2|NE|
|---|---|---|
||||
|SW|||


4


-----

###### 0 00 0 0 00 1 0 01 1 0 01 0 0 11 0 0 11 1 0 10 1 0 10 0 1 10 0 1 10 1 1 11 1 1 11 0 1 01 0 1 01 1 1 00 1 1 00 0

|n = 1|n = 2|n = 3|n = 4|
|---|---|---|---|
|0 1|00 01 11 10|000 001 011 010 110 111 101 100|0000 0001 0011 0010 0110 0111 0101 0100 1100 1101 1111 1110 1010 1011 1001 1000|


# 0 1


Claim: the binary reflected Gray code on n bits is a
Gray code.

Proof by induction on n. The claim is trivially true
for n = 1. Suppose the claim is true for n bits.
Suppose we construct the n + 1 bit binary reflected
Gray code as above from 2 copies of the n bit code.
Now take a pair of adjacent numbers. If they are in
the same half, then by the induction hypothesis they
differ in exactly one bit (since they both start with
the same bit). If one is in the top half and one is
in the bottom half, then they only differ in the first
bit.

**Assigned Reading**


Re-read the section in your discrete math textbook
or class notes that deals with induction. Alternatively, look in the library for one of the many books
on discrete mathematics.

POA, Chapter 2.


5


-----

**Summary**


###### Algorithms Course Notes Algorithm Correctness

 Ian Parberry[∗]

 Fall 2001

**Correctness of Recursive Algorithms**


Confidence in algorithms from testing and cor
_•_
rectness proof.
Correctness of recursive algorithms proved di
_•_
rectly by induction.
Correctness of iterative algorithms proved using

_•_
loop invariants and induction.
Examples: Fibonacci numbers, maximum, mul
_•_
tiplication

**Correctness**

How do we know that an algorithm works?

Modes of rhetoric (from ancient Greeks)

Ethos

_•_
Pathos

_•_
Logos

_•_

Logical methods of checking correctness

Testing

_•_
Correctness proof

_•_

**Testing vs. Correctness Proofs**

Testing: try the algorithm on sample inputs

Correctness Proof: prove mathematically

Testing may not find obscure bugs.

Using tests alone can be dangerous.

Correctness proofs can also contain bugs: use a combination of testing and correctness proofs.

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


To prove correctness of a recursive algorithm:

Prove it by induction on the “size” of the prob
_•_
lem being solved (e.g. size of array chunk, number of bits in an integer, etc.)
Base of recursion is base of induction.

_•_
Need to prove that recursive calls are given sub
_•_
problems, that is, no infinite recursion (often
trivial).
Inductive step: assume that the recursive calls

_•_
work correctly, and use this assumption to prove
that the current call works correctly.

**Recursive Fibonacci Numbers**

Fibonacci numbers: F0 = 0, F1 = 1, and for all
_n ≥_ 2, Fn = Fn−2 + Fn−1.

**function fib(n)**
**comment return Fn**
1. **if n** 1 then return(n)
_≤_
2. **else return(fib(n** 1)+fib(n 2))
_−_ _−_

Claim: For all n ≥ 0, fib(n) returns Fn.

Base: for n = 0, fib(n) returns 0 as claimed. For
_n = 1, fib(n) returns 1 as claimed._

Induction: Suppose that n 2 and for all 0 _m <_
_≥_ _≤_
_n, fib(m) returns Fm._

RTP fib(n) returns Fn.

What does fib(n) return?

fib(n 1) + fib(n 2)
_−_ _−_


1


-----

= _Fn−1 + Fn−2_ (by ind. hyp.)

= _Fn._

**Recursive Maximum**

**function maximum(n)**
**comment Return max of A[1..n].**
1. **if n** 1 then return(A[1]) else
_≤_
2. return(max(maximum(n 1),A[n]))
_−_

Claim: For all n 1, maximum(n) returns
_≥_
max _A[1], A[2], . . ., A[n]_ . Proof by induction on
_{_ _}_
_n_ 1.
_≥_

Base: for n = 1, maximum(n) returns A[1] as
claimed.

Induction: Suppose that n 1 and maximum(n)
_≥_
returns max _A[1], A[2], . . ., A[n]_ .
_{_ _}_

RTP maximum(n + 1) returns

max _A[1], A[2], . . ., A[n + 1]_ _._
_{_ _}_

What does maximum(n + 1) return?

max(maximum(n), A[n + 1])
= max(max _A[1], A[2], . . ., A[n]_ _, A[n + 1])_
_{_ _}_
(by ind. hyp.)
= max _A[1], A[2], . . ., A[n + 1]_ _._
_{_ _}_

**Recursive Multiplication**

Notation: For x IR, _x_ is the largest integer not
_∈_ _⌊_ _⌋_
exceeding x.

**function multiply(y, z)**
**comment return the product yz**
1. **if z = 0 then return(0) else**
2. **if z is odd**
3. **then return(multiply(2y,** _z/2_ )+y)
_⌊_ _⌋_
4. **else return(multiply(2y,** _z/2_ ))
_⌊_ _⌋_

Claim: For all y, z 0, multiply(y, z) returns yz.
_≥_
Proof by induction on z 0.
_≥_


Base: for z = 0, multiply(y, z) returns 0 as claimed.

Induction: Suppose that for z 0, and for all 0
_≥_ _≤_
_q_ _z, multiply(y, q) returns yq._
_≤_

RTP multiply(y, z + 1) returns y(z + 1).

What does multiply(y, z + 1) return?

There are two cases, depending on whether z + 1 is
odd or even.

If z + 1 is odd, then multiply(y, z + 1) returns

multiply(2y, (z + 1)/2 ) + y
_⌊_ _⌋_
= 2y (z + 1)/2 + y (by ind. hyp.)
_⌊_ _⌋_
= 2y(z/2) + y (since z is even)
= _y(z + 1)._

If z + 1 is even, then multiply(y, z + 1) returns

multiply(2y, (z + 1)/2 )
_⌊_ _⌋_
= 2y (z + 1)/2 (by ind. hyp.)
_⌊_ _⌋_
= 2y(z + 1)/2 (since z is odd)
= _y(z + 1)._

**Correctness of Nonrecursive Algorithms**

To prove correctness of an iterative algorithm:

Analyse the algorithm one loop at a time, start
_•_
ing at the inner loop in case of nested loops.
For each loop devise a loop invariant that re
_•_
mains true each time through the loop, and captures the “progress” made by the loop.
Prove that the loop invariants hold.

_•_
Use the loop invariants to prove that the algo
_•_
rithm terminates.
Use the loop invariants to prove that the algo
_•_
rithm computes the correct result.

**Notation**

We will concentrate on one-loop algorithms.

The value in identifier x immediately after the ith
iteration of the loop is denoted xi (i = 0 means
immediately before entering for the first time).


2


-----

For example, x6 denotes the value of identifier x after
the 6th time around the loop.

**Iterative Fibonacci Numbers**

**function fib(n)**
1. **comment Return Fn**
2. **if n = 0 then return(0) else**
3. _a := 0; b := 1; i := 2_
4. **while i** _n do_
_≤_
5. _c := a + b; a := b; b := c; i := i + 1_
6. **return(b)**

Claim: fib(n) returns Fn.

**Facts About the Algorithm**

_i0_ = 2
_ij+1_ = _ij + 1_

_a0_ = 0
_aj+1_ = _bj_

_b0_ = 1
_bj+1_ = _cj+1_

_cj+1_ = _aj + bj_

**The Loop Invariant**

For all natural numbers j ≥ 0, ij = j + 2, aj = Fj,
and bj = Fj+1.

The proof is by induction on j. The base, j = 0, is
trivial, since i0 = 2, a0 = 0 = F0, and b0 = 1 = F1.

Now suppose that j ≥ 0, ij = j + 2, aj = Fj and
_bj = Fj+1._

RTP ij+1 = j + 3, aj+1 = Fj+1 and bj+1 = Fj+2.

_ij+1_ = _ij + 1_


= (j + 2) + 1 (by ind. hyp.)

= _j + 3_

_aj+1_ = _bj_
= _Fj+1_ (by ind. hyp.)

_bj+1_ = _cj+1_
= _aj + bj_
= _Fj + Fj+1_ (by ind. hyp.)
= _Fj+2._

**Correctness Proof**

Claim: The algorithm terminates with b containing
_Fn._

The claim is certainly true if n = 0. If n > 0, then
we enter the while-loop.

Termination: Since ij+1 = ij + 1, eventually i will
equal n + 1 and the loop will terminate. Suppose
this happens after t iterations. Since it = n + 1 and
_it = t + 2, we can conclude that t = n −_ 1.

Results: By the loop invariant, bt = Ft+1 = Fn.

**Iterative Maximum**

**function maximum(A, n)**
**comment Return max of A[1..n]**
1. _m := A[1]; i := 2_
2. **while i** _n do_
_≤_
3. **if A[i] > m then m := A[i]**
4. _i := i + 1_
4. **return(m)**

Claim: maximum(A, n) returns

max _A[1], A[2], . . ., A[n]_ _._
_{_ _}_


3


-----

**Facts About the Algorithm**

_m0_ = _A[1]_
_mj+1_ = max{mj, A[ij]}

_i0_ = 2
_ij+1_ = _ij + 1_

**The Loop Invariant**

Claim: For all natural numbers j 0,
_≥_

_mj_ = max{A[1], A[2], . . ., A[j + 1]}
_ij_ = _j + 2_

The proof is by induction on j. The base, j = 0, is
trivial, since m0 = A[1] and i0 = 2.

Now suppose that j ≥ 0, ij = j + 2 and

_mj = max{A[1], A[2], . . ., A[j + 1]},_

RTP ij+1 = j + 3 and

_mj+1 = max{A[1], A[2], . . ., A[j + 2]}_

_ij+1_ = _ij + 1_
= (j + 2) + 1 (by ind. hyp.)
= _j + 3_

_mj+1_
= max{mj, A[ij]}
= max{mj, A[j + 2]} (by ind. hyp.)
= max max _A[1], . . ., A[j + 1]_ _, A[j + 2]_
_{_ _{_ _}_ _}_
(by ind. hyp.)
= max _A[1], A[2], . . ., A[j + 2]_ _._
_{_ _}_


**Correctness Proof**

Claim: The algorithm terminates with m containing
the maximum value in A[1..n].

Termination: Since ij+1 = ij + 1, eventually i will
equal n+1 and the loop will terminate. Suppose this
happens after t iterations. Since it = t+2, t = n−1.

Results: By the loop invariant,

_mt_ = max{A[1], A[2], . . ., A[t + 1]}
= max _A[1], A[2], . . ., A[n]_ _._
_{_ _}_

**Iterative Multiplication**

**function multiply(y, z)**
**comment Return yz, where y, z** IN
_∈_
1. _x := 0;_
2. **while z > 0 do**
3. **if z is odd then x := x + y;**
4. _y := 2y; z :=_ _z/2_ ;
_⌊_ _⌋_
5. **return(x)**

Claim: if y, z IN, then multiply(y, z) returns the
_∈_
value yz. That is, when line 5 is executed, x = yz.

**A Preliminary Result**

Claim: For all n IN,
_∈_

2 _n/2_ + (n mod 2) = n.
_⌊_ _⌋_

Case 1. n is even. Then _n/2_ = n/2, n mod 2 = 0,
_⌊_ _⌋_
and the result follows.

Case 2. n is odd. Then _n/2_ = (n 1)/2, n mod
_⌊_ _⌋_ _−_
2 = 1, and the result follows.

**Facts About the Algorithm**

Write the changes using arithmetic instead of logic.

From line 4 of the algorithm,

_yj+1_ = 2yj
_zj+1_ = _⌊zj/2⌋_


4


-----

From lines 1,3 of the algorithm,

_x0_ = 0
_xj+1_ = _xj + yj(zj mod 2)_

**The Loop Invariant**

Loop invariant: a statement about the variables that
remains true every time through the loop.

Claim: For all natural numbers j 0,
_≥_

_yjzj + xj = y0z0._

The proof is by induction on j. The base, j = 0, is
trivial, since then

_yjzj + xj_ = _y0z0 + x0_
= _y0z0_

Suppose that j 0 and
_≥_

_yjzj + xj = y0z0._

We are required to prove that

_yj+1zj+1 + xj+1 = y0z0._

By the Facts About the Algorithm

_yj+1zj+1 + xj+1_
= 2yj⌊zj/2⌋ + xj + yj(zj mod 2)
= _yj(2⌊zj/2⌋_ + (zj mod 2)) + xj
= _yjzj + xj_ (by prelim. result)
= _y0z0_ (by ind. hyp.)

**Correctness Proof**

Claim: The algorithm terminates with x containing
the product of y and z.

Termination: on every iteration of the loop, the
value of z is halved (rounding down if it is odd).
Therefore there will be some time t at which zt = 0.
At this point the while-loop terminates.


Results: Suppose the loop terminates after t iterations, for some t 0. By the loop invariant,
_≥_

_ytzt + xt = y0z0._

Since zt = 0, we see that xt = y0z0. Therefore, the
algorithm terminates with x containing the product
of the initial values of y and z.

**Assigned Reading**

_Problems on Algorithms: Chapter 5._


5


-----

**Summary**


###### Algorithms Course Notes Algorithm Analysis 1

 Ian Parberry[∗]

 Fall 2001

Recall: measure resource usage as a function of input
size.


_O, Ω, Θ_

_•_
Sum and product rule for O

_•_
Analysis of nonrecursive algorithms

_•_

**Implementing Algorithms**


**Algorithm**


_Programmer_

**Program**

_Compiler_

**Executable**

_Computer_

**Constant Multiples**

Analyze the resource usage of an algorithm to within
a constant multiple.

Why? Because other constant multiples creep in
when translating from an algorithm to executable
code:

Programmer ability

_•_
Programmer effectiveness

_•_
Programming language

_•_
Compiler

_•_
Computer hardware

_•_

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


**Big Oh**

We need a notation for “within a constant multiple”.
Actually, we have several of them.

Informal definition: f (n) is O(g(n)) if f grows at
most as fast as g.

Formal definition: f (n) = O(g(n)) if there exists
_c, n0 ∈_ IR[+] such that for all n ≥ _n0, f_ (n) ≤ _c · g(n)._

###### cg(n)

 f(n)

_time_

|Col1|Col2|
|---|---|
|Programmer||
|||
|Program||
|||
|Compiler||
|||
|Executable||
|||
|Computer||


Claim: for all n 1, log n _n. The proof is by_
_≥_ _≤_
induction on n. The claim is trivially true for n = 1,
since 0 < 1. Now suppose n 1 and log n _n._
_≥_ _≤_
Then,

log(n + 1)
log 2n
_≤_
= log n + 1
_n + 1_ (by ind. hyp.)
_≤_


###### n 0

**Example**

Most big-Os can be proved by induction.

Example: log n = O(n).


_n_


1


-----

**Second Example**

2[n][+1] = O(3[n]/n).

Claim: for all n 7, 2[n][+1] 3[n]/n. The proof is
_≥_ _≤_
by induction on n. The claim is true for n = 7,
since 2[n][+1] = 2[8] = 256, and 3[n]/n = 3[7]/7 > 312.
Now suppose n 7 and 2[n][+1] 3[n]/n. RTP 2[n][+2]
_≥_ _≤_ _≤_
3[n][+1]/(n + 1).

2[n][+2]

= 2 2[n][+1]
_·_

2 3[n]/n (by ind. hyp.)
_≤_ _·_

3n

(see below)

_≤_

_n + 1_ _n_

_[·][ 3][n]_

= 3[n][+1]/(n + 1).

(Note that we need

3n/(n + 1) 2
_≥_
3n 2n + 2
_⇔_ _≥_
_n_ 2.)
_⇔_ _≥_

**Big Omega**

Informal definition: f (n) is Ω(g(n)) if f grows at
least as fast as g.

Formal definition: f (n) = Ω(g(n)) if there exists
_c > 0 such that there are infinitely many n_ IN
_∈_
such that f (n) _c_ _g(n)._
_≥_ _·_

###### f(n)

 cg(n)


**Alternative Big Omega**

Some texts define Ωdifferently: f (n) = Ω[′](g(n)) if
there exists c, n0 ∈ IR[+] such that for all n ≥ _n0,_
_f_ (n) _c_ _g(n)._
_≥_ _·_

###### f(n)

 cg(n)

**Is There a Difference?**

If f (n) = Ω[′](g(n)), then f (n) = Ω(g(n)), but the
converse is not true. Here is an example where
_f_ (n) = Ω(n[2]), but f (n) = Ω[′](n[2]).
_̸_


###### f(n)

Does this come up often in practice? No.

**Big Theta**

Informal definition: f (n) is Θ(g(n)) if f is essentially
the same as g, to within a constant multiple.

Formal definition: _f_ (n) = Θ(g(n)) if f (n) =
_O(g(n)) and f_ (n) = Ω(g(n)).


###### 0.6 n [2]


2


-----

###### f(n)

 dg(n)


###### n 0

**Multiple Guess**

True or false?

3n[5] 16n + 2 = O(n[5])?

_•_ _−_
3n[5] 16n + 2 = O(n)?

_•_ _−_
3n[5] 16n + 2 = O(n[17])?

_•_ _−_
3n[5] 16n + 2 = Ω(n[5])?

_•_ _−_
3n[5] 16n + 2 = Ω(n)?

_•_ _−_
3n[5] 16n + 2 = Ω(n[17])?

_•_ _−_
3n[5] 16n + 2 = Θ(n[5])?

_•_ _−_
3n[5] 16n + 2 = Θ(n)?

_•_ _−_
3n[5] 16n + 2 = Θ(n[17])?

_•_ _−_

**Adding Big Ohs**

Claim. If f1(n) = O(g1(n)) and f2(n) = O(g2(n)),
then f1(n) + f2(n) = O(g1(n) + g2(n)).

Proof: Suppose for all n ≥ _n1, f1(n) ≤_ _c1 ·_ _g1(n) and_
for all n ≥ _n2, f2(n) ≤_ _c2 · g2(n)._

Let n0 = max{n1, n2} and c0 = max{c1, c2}. Then
for all n ≥ _n0,_

_f1(n) + f2(n)_ _≤_ _c1 · g1(n) + c2 · g2(n)_
_≤_ _c0(g1(n) + g2(n))._

Claim. If f1(n) = O(g1(n)) and f2(n) = O(g2(n)),
then f1(n) + f2(n) = O(max{g1(n), g2(n)}).

Proof: Suppose for all n ≥ _n1, f1(n) ≤_ _c1 ·_ _g1(n) and_
for all n ≥ _n2, f2(n) ≤_ _c2 · g2(n)._

Let n0 = max{n1, n2} and c0 = c1 + _c2. Then for all_
_n ≥_ _n0,_

_f1(n) + f2(n)_ _≤_ _c1 · g1(n) + c2 · g2(n)_
_≤_ (c1 + c2)(max{g1(n), g2(n)})
= _c0(max{g1(n), g2(n)})._


**Multiplying Big Ohs**

Claim. If f1(n) = O(g1(n)) and f2(n) = O(g2(n)),
then f1(n) · f2(n) = O(g1(n) · g2(n)).

Proof: Suppose for all n ≥ _n1, f1(n) ≤_ _c1 ·_ _g1(n) and_
for all n ≥ _n2, f2(n) ≤_ _c2 · g2(n)._

Let n0 = max{n1, n2} and c0 = c1 · c2. Then for all
_n ≥_ _n0,_

_f1(n) · f2(n)_ _≤_ _c1 · g1(n) · c2 · g2(n)_
= _c0 · g1(n) · g2(n)._

**Types of Analysis**

Worst case: time taken if the worst possible thing
happens. T (n) is the maximum time taken over all
inputs of size n.

Average Case: The expected running time, given
some probability distribution on the inputs (usually
uniform). T (n) is the average time taken over all
inputs of size n.

Probabilistic: The expected running time for a random input. (Express the running time and the probability of getting it.)

Amortized: The running time for a series of executions, divided by the number of executions.

**Example**

Consider an algorithm that for all inputs of n bits
takes time 2n, and for one input of size n takes time
_n[n]._

Worst case: Θ(n[n])

Average Case:

Θ( _[n][n][ + (2][n][ −]_ [1)][n] ) = Θ( _[n][n]_

2[n] 2[n][ )]


Probabilistic: O(n) with probability 1 1/2[n]
_−_


3


-----

Amortized: A sequence of m executions on different
inputs takes amortized time

_O(_ _[n][n][ + (]m[m][ −]_ [1)][n] ) = O( _[n]m[n]_ [)][.]


**Time Complexity**

We’ll do mostly worst-case analysis. How much time
does it take to execute an algorithm in the worst
case?

assignment _O(1)_
procedure entry _O(1)_
procedure exit _O(1)_
if statement time for test plus
_O(max of two branches)_
loop sum over all iterations of
the time for each iteration

Put these together using sum rule and product rule.
Exception — recursive algorithms.

**Multiplication**

**function multiply(y, z)**
**comment Return yz, where y, z** IN
_∈_
1. _x := 0;_
2. **while z > 0 do**
3. **if z is odd then x := x + y;**
4. _y := 2y; z :=_ _z/2_ ;
_⌊_ _⌋_
5. **return(x)**

Suppose y and z have n bits.

Procedure entry and exit cost O(1) time

_•_
Lines 3,4 cost O(1) time each

_•_
The while-loop on lines 2–4 costs O(n) time (it

_•_
is executed at most n times).
Line 1 costs O(1) time

_•_

Therefore, multiplication takes O(n) time (by the
sum and product rules).


Therefore, bubblesort takes time O(n[2]) in the worst
case. Can show similarly that it takes time Ω(n[2]),
hence Θ(n[2]).

**Analysis Trick**

Rather than go through the step-by-step method of
analyzing algorithms,

Identify the fundamental operation used in the

_•_
algorithm, and observe that the running time
is a constant multiple of the number of fundamental operations used. (Advantage: no need
to grunge through line-by-line analysis.)
Analyze the number of operations exactly. (Ad
_•_
vantage: work with numbers instead of symbols.)

This often helps you stay focussed, and work faster.

**Example**

In the bubblesort example, the fundamental operation is the comparison done in line 4. The running
time will be big-O of the number of comparisons.

Line 4 uses 1 comparison

_•_
The for-loop on lines 3–5 uses n _i comparisons_

_•_ _−_


**Bubblesort**

1. **procedure bubblesort(A[1..n])**
2. **for i := 1 to n** 1 do
_−_
3. **for j := 1 to n** _i do_
_−_
4. **if A[j] > A[j + 1] then**
5. Swap A[j] with A[j + 1]

Procedure entry and exit costs O(1) time

_•_
Line 5 costs O(1) time

_•_
The if-statement on lines 4–5 costs O(1) time

_•_
The for-loop on lines 3–5 costs O(n _i) time_

_•_ _−_

_• The for-loop on lines 2–5 costs O([�][n]i=1[−][1][(][n][ −]_ _[i][))]_
time.


_n�−1_

_i) = O(n[2])_

_i=1_


_O(_


_n�−1_

(n _i)) = O(n(n_ 1)
_−_ _−_ _−_
_i=1_


4


-----

_• The for-loop on lines 2–5 uses_ [�][n]i=1[−][1][(][n][−][i][) com-]
parisons, and


_n�−1_

(n _i)_ = _n(n_ 1)
_−_ _−_ _−_
_i=1_


_n�−1_

_i_

_i=1_


= _n(n_ 1) _n(n_ 1)/2
_−_ _−_ _−_
= _n(n_ 1)/2.
_−_

**Lies, Damn Lies, and Big-Os**

(Apologies to Mark Twain.)

The multiplication algorithm takes time O(n).

What does this mean? Watch out for

Hidden assumptions: word model vs. bit model

_•_
(addition takes time O(1))
Artistic lying: the multiplication algorithm

_•_
takes time O(n[2]) is also true. (Robert Heinlein: There are 2 artistic ways of lying. One is
to tell the truth, but not all of it.)
The constant multiple: it may make the algo
_•_
rithm impractical.

**Algorithms and Problems**

Big-Os mean different things when applied to algorithms and problems.

“Bubblesort runs in time O(n[2]).” _But is it_

_•_
_tight?_ _Maybe I was too lazy to figure it out,_
_or maybe it’s unknown._
“Bubblesort runs in time Θ(n[2]).” This is tight.

_•_
“The sorting problem takes time O(n log n).”

_•_
_There exists an algorithm that sorts in time_
_O(n log n), but I don’t know if there is a faster_
_one._
“The sorting problem takes time Θ(n log n).”

_•_
_There exists an algorithm that sorts in time_
_O(n log n), and no algorithm can do any better._

**Assigned Reading**

CLR, Chapter 1.2, 2.

POA, Chapter 3.


5


-----

**Summary**


###### Algorithms Course Notes Algorithm Analysis 2

 Ian Parberry[∗]

 Fall 2001

2. Structure. The value in each parent is the
_≤_
values in its children.


Analysis of iterative (nonrecursive) algorithms.

The heap: an implementation of the priority queue

Insertion in time O(log n)

_•_
Deletion of minimum in time O(log n)

_•_

Heapsort

Build a heap in time O(n log n).

_•_
Dismantle a heap in time O(n log n).

_•_
Worst case analysis — O(n log n).

_•_
How to build a heap in time O(n).

_•_

**The Heap**

A priority queue is a set with the operations

Insert an element

_•_
Delete and return the smallest element

_•_

A popular implementation: the heap. A heap is a
binary tree with the data stored in the nodes. It has
two important properties:

1. Balance. It is as much like a complete binary tree
as possible. “Missing leaves”, if any, are on the last
level at the far right.

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


Note this implies that the value in each parent is
_≤_
the values in its descendants (nb. includes self).

**To Delete the Minimum**

1. Remove the root and return the value in it.

###### 33

 ?

 9 5

 11 20 10 24

 21 15 30 40 12

But what we have is no longer a tree!

2. Replace root with last leaf.


1


-----

But we’ve violated the structure condition!

3. Repeatedly swap the new element with its smallest child until it reaches a place where it is no larger
than its children.


**Why Does it Work?**

Why does swapping the new node with its smallest
child work?

###### a a
 or
 b c c b

Suppose b _c and a is not in the correct place. That_
_≤_
is, either a > b or a > c. In either case, since b _c,_
_≤_
we know that a > b.

###### a a
 or
 b c c b

Then we get

###### b b
 or
 a c c a

respectively.

Is b smaller than its children? Yes, since b < a and
_b_ _c._
_≤_


###### c


###### b


###### c


###### b


###### c


###### a


2


###### a


###### b


###### b


-----

Is c smaller than its children? Yes, since it was before.

Is a smaller than its children? Not necessarily.
That’s why we continue to swap further down the
tree.

Does the subtree of c still have the structure condition? Yes, since it is unchanged.

**To Insert a New Element**

###### 4 ?
 3

 9 5

 11 20 10 24

 21 15 30 40 12

1. Put the new element in the next leaf. This preserves the balance.

###### 3

 9 5

 11 20 10 24

 21 15 30 40 12 4

But we’ve violated the structure condition!

2. Repeatedly swap the new element with its parent
until it reaches a place where it is no smaller than
its parent.

|4|Col2|
|---|---|
||? 3 9 5 11 20 10 24 21 15 30 40 12|


**Why Does it Work?**

Why does swapping the new node with its parent
work?

###### a

 b c

 d e

Suppose c < a. Then we swap to get


###### b


###### d


3


###### e


-----

|1. Remove root 2. Replace root 3. Swaps|O(1) O(1) O(ℓ(n))|
|---|---|


###### b


###### d


Is a larger than its parent? Yes, since a > c.

Is b larger than its parent? Yes, since b > a > c.

Is c larger than its parent? Not necessarily. That’s
why we continue to swap

Is d larger than its parent? Yes, since d was a descendant of a in the original tree, d > a.

Is e larger than its parent? Yes, since e was a descendant of a in the original tree, e > a.

Do the subtrees of b, d, e still have the structure condition? Yes, since they are unchanged.

**Implementing a Heap**

An n node heap uses an array A[1..n].

The root is stored in A[1]

_•_
The left child of a node in A[i] is stored in node

_•_
_A[2i]._
The right child of a node in A[i] is stored in

_•_
node A[2i + 1].

###### A


where ℓ(n) is the number of levels in an n-node heap.

Insert:

1. Put in leaf _O(1)_

2. Swaps _O(ℓ(n))_

**Analysis of ℓ(n)**

A complete binary tree with k levels has exactly 2[k]
_−_
1 nodes (can prove by induction). Therefore, a heap
with k levels has no fewer than 2[k][−][1] nodes and no
more than 2[k] 1 nodes.
_−_

_k-1_

###### 2   -1k-1 k nodes 2 -1k
 nodes

Therefore, in a heap with n nodes and k levels:

2[k][−][1] _n_ 2[k] 1
_≤_ _≤_ _−_
_k_ 1 log n _< k_
_−_ _≤_
_k_ 1 log n _k_
_−_ _≤_ _⌊_ _⌋_ _≤_
_k_ 1 log n _k_ 1
_−_ _≤_ _⌊_ _⌋_ _≤_ _−_
log n = k 1
_⌊_ _⌋_ _−_
_k_ = log n + 1
_⌊_ _⌋_

Hence, number of levels is ℓ(n) = log n + 1.
_⌊_ _⌋_

Examples:

|1. Put in leaf 2. Swaps|O(1) O(ℓ(n))|
|---|---|


_k_

###### 2 -1 nodes


###### e


###### 3
 9
 5
 11
 20
 10
 24
 21 15 30 40 12


###### 2   -1k-1 nodes


_1_


_1_
_2_
_3_
_4_
_5_
_6_
_7_
_8_
_9_
_10_
_11_
_12_


**Analysis of Priority Queue Operations**

Delete the Minimum:


4


-----

Left side: 8 nodes, log 8 +1 = 4 levels. Right side:
_⌊_ _⌋_
15 nodes, log 15 + 1 = 4 levels.
_⌊_ _⌋_

So, insertion and deleting the minimum from an nnode heap requires time O(log n).

**Heapsort**

Algorithm:

To sort n numbers.
1. Insert n numbers into an empty heap.
2. Delete the minimum n times.
The numbers come out in ascending order.

Analysis:

Each insertion costs time O(log n). Therefore cost
of line 1 is O(n log n).

Each deletion costs time O(log n). Therefore cost of
line 2 is O(n log n).

Therefore heapsort takes time O(n log n) in the
worst case.

**Building a Heap Top Down**

Cost of building a heap proportional to number of
comparisons. The above method builds from the top
down.

**. . .**

Cost of an insertion depends on the height of the
heap. There are lots of expensive nodes.


_k_
�

_j2[j]_ = (k 1)2[k][+1] + 2
_−_
_j=1_

= Θ(k2[k])

**Building a Heap Bottom Up**

Cost of an insertion depends on the height of the
heap. But now there are few expensive nodes.


number of
comparisons


###### 0


###### 3 3 3 3 3 3 3 3

Number of comparisons (assuming a full heap):

_ℓ(n)−1_
�

_j2[j]_ = Θ(ℓ(n)2[ℓ][(][n][)]) = Θ(n log n).

_j=0_

How do we know this? Can prove by induction that:


5


-----

number of
comparisons


CLR Chapter 7.

POA Section 11.1


###### 0


###### 0 0 0 0 0 0 0


Number of comparisons is (assuming a full heap):


_ℓ(n)_
�

(i 1)
_−_
_i=1_ ����
cost


_ℓ(n)_
�

_i/2[i])._

_i=1_


2[ℓ][(][n][)][−][i]

_·_
����
copies


_ℓ(n)_
�
_< 2[ℓ][(][n][)]_ _i/2[i]_ = O(n

_·_
_i=1_


What is [�][ℓ]i=1[(][n][)] _[i/][2][i][? It is easy to see that it is][ O][(1):]_


_k_

1

�

_i/2[i]_ =

2[k]

_i=1_

1
=

2[k]


_k_
�

_i2[k][−][i]_

_i=1_

_k−1_
�

(k _i)2[i]_
_−_
_i=0_


_k_ _k�−1_ _k�−1_
= 2[i] _i2[i]_

_−_ [1]

2[k] 2[k]

_i=0_ _i=0_

= _k(2[k]_ 1)/2[k] ((k 2)2[k] + 2)/2[k]
_−_ _−_ _−_

= _k_ _k/2[k]_ _k + 2_ 1/2[k][−][1]
_−_ _−_ _−_

= 2
_−_ _[k][ + 2]_

2[k]
2 for all k 1
_≤_ _≥_

Therefore building the heap takes time O(n). Heapsort is still O(n log n).

**Questions**

Can a node be deleted in time O(log n)?

Can a value be deleted in time O(log n)?

**Assigned Reading**


6


-----

**Summary**

Analysis of recursive algorithms:

recurrence relations

_•_
how to derive them

_•_
how to solve them

_•_


###### Algorithms Course Notes Algorithm Analysis 3

 Ian Parberry[∗]

 Fall 2001

Running time for base

###### T(n) =


Number of times
recursive call is
made


Base of recursion


###### a.T(f(n)) + g(n) otherwise

All other processing
not counting recursive
calls


**Deriving Recurrence Relations**

To derive a recurrence relation for the running time
of an algorithm:

Figure out what “n”, the problem size, is.

_•_
See what value of n is used as the base of the

_•_
recursion. It will usually be a single value (e.g.
_n = 1), but may be multiple values. Suppose it_
is n0.

_• Figure out what T_ (n0) is. You can usually
use “some constant c”, but sometimes a specific
number will be needed.
The general T (n) is usually a sum of various

_•_
choices of T (m) (for the recursive calls), plus
the sum of the other work done. Usually the
recursive calls will be solving a subproblems of
the same size f (n), giving a term “a _T_ (f (n))”
_·_
in the recurrence relation.

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


Size of problem solved
by recursive call

**Examples**

**procedure bugs(n)**
**if n = 1 then do something**
**else**
bugs(n 1);
_−_
bugs(n 2);
_−_
**for i := 1 to n do**
something


_T_ (n) =








1


-----

**procedure daffy(n)**
**if n = 1 or n = 2 then do something**
**else**
daffy(n 1);
_−_
**for i := 1 to n do**
do something new
daffy(n 1);
_−_


_T_ (n) =








**procedure elmer(n)**
**if n = 1 then do something**
**else if n = 2 then do something else**
**else**
**for i := 1 to n do**
elmer(n 1);
_−_
do something different


_T_ (n) =








**procedure yosemite(n)**
**if n = 1 then do something**
**else**
**for i := 1 to n** 1 do
_−_
yosemite(i);
do something completely different


**function multiply(y, z)**
**comment return the product yz**
1. **if z = 0 then return(0) else**
2. **if z is odd**
3. **then return(multiply(2y,** _z/2_ )+y)
_⌊_ _⌋_
4. **else return(multiply(2y,** _z/2_ ))
_⌊_ _⌋_

Let T (n) be the running time of multiply(y, z),
where z is an n-bit natural number.

Then for some c, d IR,
_∈_

� _c_ if n = 1
_T_ (n) =
_T_ (n 1) + d otherwise
_−_

**Solving Recurrence Relations**

Use repeated substitution.

Given a recurrence relation T (n).

Substitute a few times until you see a pattern

_•_
Write a formula in terms of n and the number

_•_
of substitutions i.
Choose i so that all references to T () become

_•_
references to the base case.
Solve the resulting summation

_•_

This will not always work, but works most of the
time in practice.

**The Multiplication Example**

We know that for all n > 1,

_T_ (n) = T (n 1) + d.
_−_

Therefore, for large enough n,

_T_ (n) = _T_ (n 1) + d
_−_
_T_ (n 1) = _T_ (n 2) + d
_−_ _−_

_T_ (n 2) = _T_ (n 3) + d
_−_ _−_
...

_T_ (2) = _T_ (1) + d
_T_ (1) = _c_

**Repeated Substitution**


_T_ (n) =








**Analysis of Multiplication**


2


-----

_T_ (n) = _T_ (n 1) + d
_−_
= (T (n 2) + d) + d
_−_
= _T_ (n 2) + 2d
_−_
= (T (n 3) + d) + 2d
_−_
= _T_ (n 3) + 3d
_−_

There is a pattern developing. It looks like after i
substitutions,

_T_ (n) = T (n _i) + id._
_−_

Now choose i = n 1. Then
_−_

_T_ (n) = _T_ (1) + d(n 1)
_−_

= _dn + c_ _d._
_−_

**Warning**

This is not a proof. There is a gap in the logic.
Where did

_T_ (n) = T (n _i) + id_
_−_

come from? Hand-waving!

What would make it a proof? Either

Prove that statement by induction on i, or

_•_
Prove the result by induction on n.

_•_

**Reality Check**

We claim that

_T_ (n) = dn + c _d._
_−_

Proof by induction on n. The hypothesis is true for
_n = 1, since d + c_ _d = c._
_−_

Now suppose that the hypothesis is true for n. We
are required to prove that

_T_ (n + 1) = dn + c.


Now,

_T_ (n + 1) = _T_ (n) + d
= (dn + c _d) + d_ (by ind. hyp.)
_−_
= _dn + c._

**Merge Sorting**

**function mergesort(L, n)**
**comment sorts a list L of n numbers,**
when n is a power of 2
**if n** 1 then return(L) else
_≤_
break L into 2 lists L1, L2 of equal size
return(merge(mergesort(L1, n/2),
mergesort(L2, n/2)))

Here we assume a procedure merge which can merge
two sorted lists of n elements into a single sorted list
in time O(n).

Correctness: easy to prove by induction on n.

Analysis: Let _T_ (n) be the running time of
mergesort(L, n). Then for some c, d IR,
_∈_

� _c_ if n 1
_T_ (n) = _≤_
2T (n/2) + dn otherwise

|1|3|8|10|
|---|---|---|---|

|3|8|10|
|---|---|---|

|8|10|
|---|---|

|5|6|9|11|
|---|---|---|---|

|5|6|9|11|
|---|---|---|---|

|5|6|9|11|
|---|---|---|---|

|1|3|
|---|---|

|8|10|
|---|---|

|8|10|
|---|---|

|6|9|11|
|---|---|---|

|9|11|
|---|---|

|9|11|
|---|---|

|1|3|5|
|---|---|---|

|1|3|5|6|
|---|---|---|---|

|1|3|5|6|8|
|---|---|---|---|---|

|1|3|5|6|8|9|
|---|---|---|---|---|---|

|1|3|5|6|8|9|10|
|---|---|---|---|---|---|---|

|1|3|5|6|8|9|10|11|
|---|---|---|---|---|---|---|---|

|1 3 8 10 5 6 9 11|3 8 10 5 6 9 11 1|Col3|8 10 5 6 9 11 1 3|
|---|---|---|---|
|8 10 6 9 11 1 3 5|8 10 9 11 1 3 5 6||10 9 11 1 3 5 6 8|
|10 11 1 3 5 6 8 9||11 1 3 5 6 8 9 10||
|1 3 5 6 8 9 1011||||


3


-----

_T_ (n) = 2T (n/2) + dn

= 2(2T (n/4) + dn/2) + dn
= 4T (n/4) + dn + dn
= 4(2T (n/8) + dn/4) + dn + dn
= 8T (n/8) + dn + dn + dn

Therefore,

_T_ (n) = 2[i]T (n/2[i]) + i _dn_
_·_

Taking i = log n,

_T_ (n) = 2[log][ n]T (n/2[log][ n]) + dn log n
= _dn log n + cn_

Therefore T (n) = O(n log n).

Mergesort is better than bubblesort (in the worst
case, for large enough n).

**A General Theorem**

Theorem: If n is a power of c, the solution to the
recurrence

� _d_ if n 1
_T_ (n) = _≤_
_aT_ (n/c) + bn otherwise


The sum is the hard part. There are three cases to
consider, depending on which of a and c is biggest.

But first, we need some results on geometric progressions.

**Geometric Progressions**

Finite Sums: Define Sn = [�]i[n]=0 _[α][i][. If][ α >][ 1, then]_


= _a[3]_ _T_ (n/c[3]) + a[2]bn/c[2] + abn/c + bn

_·_
...


= _a[i]T_ (n/c[i]) + bn


_i−1_
�(a/c)[j]

_j=0_


= _a[log][c][ n]T_ (1) + bn


logc n−1
� (a/c)[j]

_j=0_


= _da[log][c][ n]_ + bn


logc n−1
� (a/c)[j]

_j=0_


Now,

_a[log][c][ n]_ = (c[log][c][ a])[log][c][ n] = (c[log][c][ n])[log][c][ a] = n[log][c][ a].

Therefore,


_T_ (n) = d _n[log][c][ a]_ + bn
_·_


logc n−1
� (a/c)[j]

_j=0_


is

_T_ (n) =

Examples:








_O(n)_ if a < c
_O(n log n)_ if a = c
_O(n[log][c][ a])_ if a > c


_α · Sn −_ _Sn_ =


_n_
� _α[i]_

_i=0_


_n_
� _α[i][+1]_

_−_
_i=0_


If T (n) = 2T (n/3) + dn, then T (n) = O(n)

_•_
If T (n) = 2T (n/2)+dn, then T (n) = O(n log n)

_•_
(mergesort)
If T (n) = 4T (n/2) + dn, then T (n) = O(n[2])

_•_

**Proof Sketch**

If n is a power of c, then

_T_ (n) = _a_ _T_ (n/c) + bn
_·_
= _a(a_ _T_ (n/c[2]) + bn/c) + bn
_·_
= _a[2]_ _T_ (n/c[2]) + abn/c + bn

_·_
= _a[2](a_ _T_ (n/c[3]) + bn/c[2]) + abn/c + bn
_·_


= _α[n][+1]_ 1
_−_

Therefore Sn = (α[n][+1] _−_ 1)/(α − 1).

Infinite Sums: Suppose 0 < α < 1 and let S =
�∞i=0 _[α][i][. Then,][ αS][ =][ �]i[∞]=1_ _[α][i][, and so][ S][ −]_ _[αS][ = 1.]_
That is, S = 1/(1 _α)._
_−_

**Back to the Proof**

Case 1: a < c.


logc n−1
� (a/c)[j] _<_

_j=0_


_∞_
�(a/c)[j] = c/(c _a)._

_−_
_j=0_


4


-----

Therefore,

_T_ (n) < d _n[log][c][ a]_ + bcn/(c _a) = O(n)._
_·_ _−_

(Note that since a < c, the first term is insignificant.)

Case 2: a = c. Then


_T_ (n) = d _n + bn_
_·_


logc n−1
� 1[j] = O(n log n).

_j=0_


Case 3: a > c. Then _j=0_ (a/c)[j] is a geometric

[�][log][c][ n][−][1]
progression.

Hence,

logc n−1 (a/c)[log][c][ n] 1
� (a/c)[j] = _−_

(a/c) 1

_j=0_ _−_


_n[log][c][ a][−][1]_ 1
_−_
=

(a/c) 1
_−_

= _O(n[log][c][ a][−][1])_

Therefore, T (n) = O(n[log][c][ a]).

**Messy Details**

What about when n is not a power of c?

Example: in our mergesort example, n may not be a
power of 2. We can modify the algorithm easily: cut
the list L into two halves of size _n/2_ and _n/2_ .
_⌊_ _⌋_ _⌈_ _⌉_
The recurrence relation becomes T _[′](n) = c if n ≤_ 1,
and

_T_ _[′](n) = T_ _[′](⌊n/2⌋) + T_ _[′](⌈n/2⌉) + dn_

otherwise.

This is much harder to analyze, but gives the same
result: T _[′](n) = O(n log n)._ To see why, think of
padding the input with extra numbers up to the
next power of 2. You at most double the number
of inputs, so the running time is

_T_ (2n) = O(2n log(2n)) = O(n log n).

This is true most of the time in practice.


**Examples**

If T (1) = 1, solve the following to within a constant
multiple:

_T_ (n) = 2T (n/2) + 6n

_•_
_T_ (n) = 3T (n/3) + 6n 9

_•_ _−_
_T_ (n) = 2T (n/3) + 5n

_•_
_T_ (n) = 2T (n/3) + 12n + 16

_•_
_T_ (n) = 4T (n/2) + n

_•_
_T_ (n) = 3T (n/2) + 9n

_•_

**Assigned Reading**

CLR Chapter 4.

POA Chapter 4.

Re-read the section in your discrete math textbook
or class notes that deals with recurrence relations.
Alternatively, look in the library for one of the many
books on discrete mathematics.


5


-----

###### Algorithms Course Notes Divide and Conquer 1

 Ian Parberry[∗]

 Fall 2001


**Summary**

Divide and conquer and its application to

Finding the maximum and minimum of a se
_•_
quence of numbers
Integer multiplication

_•_
Matrix multiplication

_•_

**Divide and Conquer**

To solve a problem

Divide it into smaller problems

_•_
Solve the smaller problems

_•_
Combine their solutions into a solution for the

_•_
big problem

Example: merge sorting

Divide the numbers into two halves

_•_
Sort each half separately

_•_
Merge the two sorted halves

_•_

**Finding Max and Min**

Problem. Find the maximum and minimum elements in an array S[1..n]. How many comparisons
between elements of S are needed?

To find the max:

max:=S[1];
**for i := 2 to n do**
**if S[i] > max then max := S[i]**

(The min can be found similarly).

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


max of n ?
min of n 1 ?
_−_

TOTAL ?

**Divide and Conquer Approach**

Divide the array in half. Find the maximum and
minimum in each half recursively. Return the maximum of the two maxima and the minimum of the
two minima.

**function maxmin(x, y)**
**comment return max and min in S[x..y]**
**if y** _x_ 1 then
_−_ _≤_
**return(max(S[x], S[y]),min(S[x], S[y]))**
**else**
(max1,min1):=maxmin(x, (x + y)/2 )
_⌊_ _⌋_
(max2,min2):=maxmin( (x + y)/2 + 1, y)
_⌊_ _⌋_
**return(max(max1,max2),min(min1,min2))**

**Correctness**

The size of the problem is the number of entries in
the array, y _x + 1._
_−_

We will prove by induction on n = y _x + 1 that_
_−_
maxmin(x, y) will return the maximum and minimum values in S[x..y]. The algorithm is clearly correct when n 2. Now suppose n > 2, and that
_≤_
maxmin(x, y) will return the maximum and minimum values in S[x..y] whenever y _x + 1 < n._
_−_

In order to apply the induction hypothesis to the
first recursive call, we must prove that (x + _y)/2_
_⌊_ _⌋−_
_x + 1 < n. There are two cases to consider, depend-_
ing on whether y _x + 1 is even or odd._
_−_

Case 1. y _x + 1 is even. Then, y_ _x is odd, and_
_−_ _−_


1


-----

hence y + x is odd. Therefore,

_x + 1_

_⌊_ _[x][ +][ y]_ _⌋−_

2

_x + y_ 1
_−_
= _x + 1_

_−_
2

= (y _x + 1)/2_
_−_

= _n/2_
_<_ _n._

Case 2. y _x + 1 is odd. Then y_ _x is even, and_
_−_ _−_
hence y + x is even. Therefore,

_x + 1_

_⌊_ _[x][ +][ y]_ _⌋−_

2

_x + y_
= _x + 1_

_−_
2

= (y _x + 2)/2_
_−_
= (n + 1)/2
_<_ _n_ (see below).

(The last inequality holds since

(n + 1)/2 < n _n > 1.)_
_⇔_

To apply the ind. hyp. to the second recursive call,
must prove that y ( (x + y)/2 + 1) + 1 < n. Two
_−_ _⌊_ _⌋_
cases again:

Case 1. y _x + 1 is even._
_−_


= _[y][ −]_ _[x][ + 1]_ = n/2.

2

So when n is a power of 2, procedure maxmin on
an array chunk of size n calls itself twice on array
chunks of size n/2. If n is a power of 2, then so is
_n/2. Therefore,_

� 1 if n = 2
_T_ (n) =
2T (n/2) + 2 otherwise

_T_ (n) = 2T (n/2) + 2
= 2(2T (n/4) + 2) + 2
= 4T (n/4) + 4 + 2
= 8T (n/8) + 8 + 4 + 2


Procedure maxmin divides the array into 2 parts.
By the induction hypothesis, the recursive calls correctly find the maxima and minima in these parts.
Therefore, since the procedure returns the maximum
of the two maxima and the minimum of the two minima, it returns the correct values.

**Analysis**

Let T (n) be the number of comparisons made by
maxmin(x, y) when n = y _x + 1. Suppose n is a_
_−_
power of 2.

What is the size of the subproblems? The first subproblem has size (x + y)/2 _x + 1. If y_ _x + 1 is_
_⌊_ _⌋−_ _−_
a power of 2, then y _x is odd, and hence x + y is_
_−_
odd. Therefore,

_x + 1 =_ _[x][ +][ y][ −]_ [1] _x + 1_

_⌊_ _[x][ +][ y]_ _⌋−_ _−_

2 2


= _[y][ −]_ _[x][ + 1]_ = n/2.

2

The second subproblem has size y ( (x + y)/2 +
_−_ _⌊_ _⌋_
1) + 1. Similarly,


_y_ ( + 1) + 1 = y
_−_ _⌊_ _[x][ +][ y]_ _⌋_ _−_ _[x][ +][ y][ −]_ [1]

2 2


_y_ ( + 1) + 1
_−_ _⌊_ _[x][ +][ y]_ _⌋_

2

= _y_
_−_ _[x][ +][ y][ −]_ [1]

2
= (y _x + 1)/2_
_−_
= _n/2_
_<_ _n._

Case 2. y _x + 1 is odd._
_−_

_y_ ( + 1) + 1
_−_ _⌊_ _[x][ +][ y]_ _⌋_

2

= _y_
_−_ _[x][ +][ y]_

2
= (y _x + 1)/2_ 1/2
_−_ _−_
= _n/2_ 1/2
_−_
_<_ _n._


= 2[log][ n][−][1]T (2) +


= 2[i]T (n/2[i]) +


_i_
� 2[j]

_j=1_


log n−1
� 2[j]

_j=1_


2


-----

= _n/2 + (2[log][ n]_ 2)
_−_

= 1.5n 2
_−_

Therefore function maxmin uses only 75% as many
comparisons as the naive algorithm.

**Multiplication**

Given positive integers y, z, compute x = yz. The
naive multiplication algorithm:

_x := 0;_
**while z > 0 do**
**if z mod 2 = 1 then x := x + y;**
_y := 2y; z :=_ _z/2_ ;
_⌊_ _⌋_

This can be proved correct by induction using the
loop invariant yjzj + xj = y0z0.

Addition takes O(n) bit operations, where n is the
number of bits in y and z. The naive multiplication
algorithm takes O(n) n-bit additions. Therefore, the
naive multiplication algorithm takes O(n[2]) bit operations.

Can we multiply using fewer bit operations?

**Divide and Conquer Approach**

Suppose n is a power of 2. Divide y and z into two
halves, each with n/2 bits.

_y_ _a_ _b_

_z_ _c_ _d_

Then

_y_ = _a2[n/][2]_ + b
_z_ = _c2[n/][2]_ + d

and so

_yz_ = (a2[n/][2] + b)(c2[n/][2] + d)

= _ac2[n]_ + (ad + bc)2[n/][2] + bd

This computes yz with 4 multiplications of n/2 bit
numbers, and some additions and shifts. Running


time given by T (1) = c, T (n) = 4T (n/2)+dn, which
has solution O(n[2]) by the General Theorem. No gain
over naive algorithm!

But x = yz can also be computed as follows:

1. _u := (a + b)(c + d)_
2. _v := ac_
3. _w := bd_
4. _x := v2[n]_ + (u _v_ _w)2[n/][2]_ + w
_−_ _−_

Lines 2 and 3 involve a multiplication of n/2 bit
numbers. Line 4 involves some additions and shifts.
What about line 1? It has some additions and a
multiplication of (n/2 + 1) bit numbers. Treat the
leading bits of a + b and c + d separately.

_a + b_ _a1_ _b1_

_c + d_ _c1_ _d1_

Then

_a + b_ = _a12[n/][2]_ + b1
_c + d_ = _c12[n/][2]_ + d1.

Therefore, the product (a + _b)(c_ + _d) in line 1 can be_
written as

|a 1|b 1|
|---|---|
|c 1|d 1|


_a1c12[n]_ + (a1d1 + b1c1)2[n/][2]
� �� �
additions and shifts


+b1d1


Thus to multiply n bit numbers we need

3 multiplications of n/2 bit numbers

_•_
a constant number of additions and shifts

_•_

Therefore,

� _c_ if n = 1
_T_ (n) =
3T (n/2) + dn otherwise

where c, d are constants.

Therefore, by our general theorem, the divide and
conquer multiplication algorithm uses

_T_ (n) = O(n[log 3]) = O(n[1][.][59])

bit operations.

|a|b|
|---|---|
|c|d|


3


-----

**Matrix Multiplication**

The naive matrix multiplication algorithm:

**procedure matmultiply(X, Y, Z, n);**
**comment multiplies n** _n matrices X := Y Z_
_×_
**for i := 1 to n do**
**for j := 1 to n do**
_X[i, j] := 0;_
**for k := 1 to n do**
_X[i, j] := X[i, j] + Y [i, k]_ _Z[k, j];_
_∗_

Assume that all integer operations take O(1) time.
The naive matrix multiplication algorithm then
takes time O(n[3]). Can we do better?

**Divide and Conquer Approach**

Divide X, Y, Z each into four (n/2) (n/2) matrices.
_×_


Compute

Then,


= 8[3]T (n/8) + 4dn[2] + 2dn[2] + dn[2]


_i−1_
= 8[i]T (n/2[i]) + dn[2] � 2[j]

_j=0_

log n−1
= 8[log][ n]T (1) + dn[2] � 2[j]

_j=0_

= _cn[3]_ + dn[2](n 1)
_−_
= _O(n[3])_

**Strassen’s Algorithm**

_M1_ := (A + C)(E + F )
_M2_ := (B + D)(G + H)
_M3_ := (A − _D)(E + H)_
_M4_ := _A(F −_ _H)_
_M5_ := (C + D)E
_M6_ := (A + B)H
_M7_ := _D(G −_ _E)_

_I_ := _M2 + M3_ _M6_ _M7_
_−_ _−_
_J_ := _M4 + M6_
_K_ := _M5 + M7_
_L_ := _M1 −_ _M3 −_ _M4 −_ _M5_

**Will This Work?**


� _I_ _J_
_X_ =
_K_ _L_

� _A_ _B_
_Y_ =
_C_ _D_

� _E_ _F_
_Z_ =
_G_ _H_


�

�

�


Then

_I_ = _AE + BG_
_J_ = _AF + BH_
_K_ = _CE + DG_
_L_ = _CF + DH_

Let T (n) be the time to multiply two n _n matrices._
_×_
The approach gains us nothing:

� _c_ if n = 1
_T_ (n) =
8T (n/2) + dn[2] otherwise

where c, d are constants.

Therefore,

_T_ (n) = 8T (n/2) + dn[2]

= 8(8T (n/4) + d(n/2)[2]) + dn[2]

= 8[2]T (n/4) + 2dn[2] + dn[2]


_I_ := _M2 + M3_ _M6_ _M7_
_−_ _−_
= (B + D)(G + H) + (A _D)(E + H)_
_−_
(A + B)H _D(G_ _E)_
_−_ _−_ _−_
= (BG + BH + DG + DH)
+ (AE + AH _DE_ _DH)_
_−_ _−_
+ ( _AH_ _BH) + (_ _DG + DE)_
_−_ _−_ _−_
= _BG + AE_

_J_ := _M4 + M6_


4


-----

= _A(F_ _H) + (A + B)H_
_−_

= _AF_ _AH + AH + BH_
_−_
= _AF + BH_

_K_ := _M5 + M7_
= (C + D)E + D(G _E)_
_−_
= _CE + DE + DG_ _DE_
_−_
= _CE + DG_

_L_ := _M1 −_ _M3 −_ _M4 −_ _M5_
= (A + C)(E + F ) (A _D)(E + H)_
_−_ _−_
_A(F_ _H)_ (C + D)E
_−_ _−_ _−_
= _AE + AF + CE + CF_ _AE_ _AH_
_−_ _−_
+ DE + DH _AF + AH_ _CE_ _DE_
_−_ _−_ _−_
= _CF + DH_

**Analysis of Strassen’s Algorithm**

� _c_ if n = 1
_T_ (n) =
7T (n/2) + dn[2] otherwise

where c, d are constants.

_T_ (n) = 7T (n/2) + dn[2]

= 7(7T (n/4) + d(n/2)[2]) + dn[2]

= 7[2]T (n/4) + 7dn[2]/4 + dn[2]

= 7[3]T (n/8) + 7[2]dn[2]/4[2] + 7dn[2]/4 + dn[2]

_i−1_
= 7[i]T (n/2[i]) + dn[2] �(7/4)[j]

_j=0_


**State of the Art**

Integer multiplication: O(n log n log log n).

Sch¨onhage and Strassen, “Schnelle multiplikation
grosser zahlen”, Computing, Vol. 7, pp. 281–292,
1971.

Matrix multiplication: O(n[2][.][376]).

Coppersmith and Winograd, “Matrix multiplication
via arithmetic progressions”, Journal of Symbolic
_Computation, Vol. 9, pp. 251–280, 1990._

**Assigned Reading**

CLR Chapter 10.1, 31.2.

POA Sections 7.1–7.3


log n−1
= 7[log][ n]T (1) + dn[2] � (7/4)[j]

_j=0_

= _cn[log 7]_ + dn[2][ (7][/][4)][log][ n][ −] [1]

7/4 1
_−_

= _cn[log 7]_ + [4] 1)

_−_

3 _[dn][2][(]_ _[n]n[log 7][2]_

= _O(n[log 7])_
_O(n[2][.][8])_
_≈_


5


-----

###### Algorithms Course Notes Divide and Conquer 2

 Ian Parberry[∗]

 Fall 2001


**Summary**

Quicksort

The algorithm

_•_
Average case analysis — O(n log n)

_•_
Worst case analysis — O(n[2]).

_•_

Every sorting algorithm based on comparisons and
swaps must make Ω(n log n) comparisons in the
worst case.

**Quicksort**

Let S be a list of n distinct numbers.

**function quicksort(S)**
1. **if** _S_ 1
_|_ _| ≤_
2. **then return(S)**
3. **else**
4. Choose an element a from S
5. Let S1, S2, S3 be the elements of S
which are respectively <, =, > a
6. **return(quicksort(S1),S2,quicksort(S3))**

Terminology: a is called the pivot value. The operation in line 5 is called pivoting on a.

**Average Case Analysis**

Let T (n) be the average number of comparisons
used by quicksort when sorting n distinct numbers.
Clearly T (0) = T (1) = 0.

Suppose a is the ith smallest element of S. Then

_|S1|_ = _i −_ 1

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


_|S2|_ = 1
_|S3|_ = _n −_ _i_

The recursive calls need average time T (i 1) and
_−_
_T_ (n _i), and i can have any value from 1 to n with_
_−_
equal probability. Splitting S into S1, S2, S3 takes
_n_ 1 comparisons (compare a to n 1 other values).
_−_ _−_

Therefore, for n 2,
_≥_


_T_ (n)
_≤_ [1]

_n_

Now,


_n_
� (T (i 1) + T (n _i)) + n_ 1

_−_ _−_ _−_
_i=1_


_n_
� (T (i 1) + T (n _i))_

_−_ _−_
_i=1_

_n_ _n_

= � _T_ (i 1) + � _T_ (n _i)_

_−_ _−_
_i=1_ _i=1_

_n−1_ _n−1_

= � _T_ (i) + � _T_ (i)

_i=0_ _i=0_


= 2


_n−1_
� _T_ (i)

_i=2_


Therefore, for n 2,
_≥_

_T_ (n)
_≤_ [2]

_n_


_n−1_
� _T_ (i) + n 1

_−_
_i=2_


How can we solve this? Not by repeated substitution!

Multiply both sides of the recurrence for T (n) by n.
Then, for n 2,
_≥_


_nT_ (n) = 2


_n−1_
� _T_ (i) + n[2] _n._

_−_
_i=2_


1


-----

Hence, substituting n 1 for n, for n 3,
_−_ _≥_


(n 1)T (n 1) = 2
_−_ _−_


_n−2_
� _T_ (i) + n[2] 3n + 2.

_−_
_i=2_


Subtracting the latter from the former,

_nT_ (n) (n 1)T (n 1) = 2T (n 1) + 2(n 1),
_−_ _−_ _−_ _−_ _−_

for all n 3. Hence, for all n 3,
_≥_ _≥_

_nT_ (n) = (n + 1)T (n 1) + 2(n 1).
_−_ _−_

Therefore, dividing both sides by n(n + 1),

_T_ (n)/(n + 1) = T (n 1)/n + 2(n 1)/n(n + 1).
_−_ _−_

Define S(n) = T (n)/(n + 1). Then, by definition,
_S(0) = S(1) = 0, and by the above, for all n_ 3,
_≥_
_S(n) = S(n_ 1)+2(n 1)/n(n+1). This is true even
_−_ _−_
for n = 2, since S(2) = T (2)/3 = 1/3. Therefore,

� 0 if n 1
_S(n)_ _≤_
_≤_ _S(n_ 1) + 2/n otherwise.
_−_

Solve by repeated substitution:

_S(n)_ _S(n_ 1) + 2/n
_≤_ _−_

_S(n_ 2) + 2/(n 1) + 2/n
_≤_ _−_ _−_
_S(n_ 3) + 2/(n 2) + 2/(n 1) + 2/n
_≤_ _−_ _−_ _−_

_n_

1

_S(n_ _i) + 2_ �
_≤_ _−_

_j [.]_

_j=n−i+1_

Therefore, taking i = n 1,
_−_


_n_
�

_j=2_


1 � _n_
_j_ _[≤]_ [2] 1


1
_x_ [d][x][ = ln][ n.]


Thus quicksort uses O(n log n) comparisons on average. Quicksort is faster than mergesort by a small
constant multiple in the average case, but much
worse in the worst case.

How about the worst case? In the worst case, i = 1
and

� 0 if n 1
_T_ (n) = _≤_
_T_ (n 1) + n 1 otherwise
_−_ _−_

It is easy to show that this is Θ(n[2]).

**Best Case Analysis**

How about the best case? In the best case, i = n/2
and

� 0 if n 1
_T_ (n) = _≤_
2T (n/2) + n 1 otherwise
_−_

for some constants c, d.

It is easy to show that this is n log n + O(n). Hence,
the average case number of comparisons used by
quicksort is only 39% more than the best case.

**A Program**

The algorithm can be implemented as a program
that runs in time O(n log n). To sort an array
_S[1..n], call quicksort(1, n):_

1. **procedure quicksort(ℓ, r)**
2. **comment sort S[ℓ..r]**
3. _i := ℓ; j := r;_
_a := some element from S[ℓ..r];_
4. **repeat**
5. **while S[i] < a do i := i + 1;**
6. **while S[j] > a do j := j** 1;
_−_
7. **if i** _j then_
_≤_
8. swap S[i] and S[j];
9. _i := i + 1; j := j_ 1;
_−_
10. **until i > j;**
11. **if ℓ< j then quicksort(ℓ, j);**
12. **if i < r then quicksort(i, r);**

**Correctness Proof**

Consider the loop on line 5.


_S(n)_ _S(1)+2_
_≤_

Therefore,


_n_
�

_j=2_


1
_j_ [= 2]


_T_ (n) = (n + 1)S(n)
_<_ 2(n + 1) ln n
= 2(n + 1) log n/ log e
1.386(n + 1) log n.
_≈_

**Worst Case Analysis**


2


-----

5. **while S[i] < a do i := i + 1;**


Loop invariant: For k ≥ 0, ik = i0 + k and S[v] < a
for all i0 ≤ _v < ik._

###### all < a


4. **repeat**
5. **while S[i] < a do i := i + 1;**
6. **while S[j] > a do j := j** 1;
_−_
7. **if i** _j then_
_≤_
8. swap S[i] and S[j];
9. _i := i + 1; j := j_ 1;
_−_
10. **until i > j;**

Loop invariant: after each iteration, either i _j and_
_≤_


###### . . .


###### . . .


###### . . .

|. . .|Col2|Col3|Col4|Col5|. . .|Col7|. . .|
|---|---|---|---|---|---|---|---|


_i0_ _ik_

Proof by induction on k. The invariant is vacuously
true for k = 0.

Now suppose k > 0. By the induction hypothesis,
_ik−1 = i0 + k −_ 1, and S[v] < a for all i0 ≤ _v < ik−1._
Since we enter the while-loop on the kth iteration,
it must be the case that S[ik−1] < a. Therefore,
_S[v] < a for all i0 ≤_ _v ≤_ _ik−1. Furthermore, i is_
incremented in the body of the loop, so ik = ik−1 +
1 = (i0 + k − 1) + 1 = i0 + k. This makes both parts
of the hypothesis true.

Conclusion: upon exiting the loop on line 5, S[i] _a_
_≥_
and S[v] < a for all i0 ≤ _v < i._

|all <= a ?|Col2|Col3|Col4|Col5|Col6|all >= a ?|Col8|Col9|Col10|Col11|Col12|
|---|---|---|---|---|---|---|---|---|---|---|---|
|||||||||||||
||||. . .|||||. . .||||


###### ?


_S[v]_ _a for all ℓ_ _v_ _i, and_

_•_ _≤_ _≤_ _≤_
_S[v]_ _a for all j_ _v_ _r._

_•_ _≥_ _≤_ _≤_

###### all <= a ?


_l_

or i > j and


_i_ _j_


_r_


_S[v]_ _a for all ℓ_ _v < i, and_

_•_ _≤_ _≤_
_S[v]_ _a for all j < v_ _r._

_•_ _≥_ _≤_


###### all >= a

 . . .

_i_ _r_


Consider the loop on line 6.

6. **while S[j] > a do j := j** 1;
_−_


###### all <= a

_j_

|Col1|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Col10|
|---|---|---|---|---|---|---|---|---|---|
|||. . .|||||. . .|||


Loop invariant: For k ≥ 0, jk = j0 − _k and S[v] > a_
for all jk < v ≤ _j0._

###### all > a


_l_

After lines 5,6


_S[v]_ _a for all ℓ_ _v < i, and_

_•_ _≤_ _≤_
_S[i]_ _a_

_•_ _≥_
_S[v]_ _a for all j < v_ _r._

_•_ _≥_ _≤_
_S[j]_ _a_

_•_ _≤_

|. . .|Col2|. . .|Col4|Col5|Col6|Col7|. . .|
|---|---|---|---|---|---|---|---|
|j j k 0||||||||


Proof is similar to the above.

Conclusion: upon exiting the loop on line 6, S[j] _a_
_≤_
and S[v] > a for all j < v ≤ _j0._


If i > j, then the loop invariant holds. Otherwise,
line 8 makes it hold:

_S[v]_ _a for all ℓ_ _v_ _i, and_

_•_ _≤_ _≤_ _≤_
_S[v]_ _a for all j_ _v_ _r._

_•_ _≥_ _≤_ _≤_


The loop terminates since i is incremented and j is
decremented each time around the loop as long as
_i_ _j._
_≤_

Hence we exit the repeat-loop with small values to
the left, and big values to the right.


The loops on lines 5,6 will always halt.

Question: Why?


Consider the repeat-loop on lines 4–10.


3


-----

|Col1|Col2|Col3|. . .|Col5|Col6|Col7|. . .|Col9|
|---|---|---|---|---|---|---|---|---|


###### all >= a


###### all >= a


After it makes one comparison, it can be in one of
two possible worlds, depending on the result of that
comparison.

After it makes 2 comparisons, each of these worlds
can give rise to at most 2 more possible worlds.

**Decision Tree**


_l_


###### all <= a

 all <= a


_j_


###### . . .

_i_ _r_

|Col1|Col2|. . .|Col4|Col5|Col6|. . .|Col8|
|---|---|---|---|---|---|---|---|


_l_


_j_


###### . . .

_i_ _r_


(How can each of these scenarios happen?)

Correctness proof is by induction on the size of the
chunk of the array, r _ℓ_ +1. It works for an array of
_−_
size 1 (trace through the algorithm). In each of the
two scenarios above, the two halves of the array are
smaller than the original (since i and j must cross).
Hence, by the induction hypothesis, the recursive
call sorts each half, which in both scenarios means
that the array is sorted.


What should we use for a? Candidates:

_S[ℓ], S[r] (vanilla)_

_•_
_S[_ (ℓ + r)/2 ] (fast on “nearly sorted” data)

_•_ _⌊_ _⌋_
_S[m] where m is a pseudorandom value, ℓ_

_•_ _≤_
_m_ _r (good for repeated use on similar data)_
_≤_


**A Lower Bound**

Claim: Any sorting algorithm based on comparisons
and swaps must make Ω(n log n) comparisons in the
worst case.

Mergesort makes O(n log n) comparisons. So, there
is no comparison-based sorting algorithm that is
faster than mergesort by more than a constant multiple.


After i comparisons, the algorithm gives rise to at
most 2[i] possible worlds.

But if the algorithm sorts, then it must eventually
give rise to at least n! possible worlds.

Therefore, if it sorts in at most T (n) comparisons in
the worst case, then

2[T][ (][n][)] _n!,_
_≥_


_T_ (n) log n!.
_≥_

**How Big is n!?**


That is,


**Proof of Lower Bound**

A sorting algorithm permutes its inputs into sorted
order.


It must perform one of n! possible permutations.

It doesn’t know which until it compares its inputs.


Consider a “many worlds” view of the algorithm.
Initially, it knows nothing about the input.


_n![2]_ = (1 2 _n)(n_ 2 1)
_·_ _· · ·_ _· · ·_ _·_

_n_

= � _k(n + 1_ _k)_

_−_
_k=1_

_k(n + 1_ _k) has its minimum when k = 1 or k = n,_
_−_
and its maximum when k = (n + 1)/2.


4


-----

2
_(n+1) /4_

_n_

Therefore,


_k(n+1-k)_

_1_ _(n+1)/2_ _n_


_k_


_n_
� _n_ _n![2]_

_≤_ _≤_
_k=1_


_n_
�

_k=1_


(n + 1)[2]

4


That is,
_n[n/][2]_ _n!_ (n + 1)[n]/2[n]
_≤_ _≤_

Hence
log n! = Θ(n log n).

More precisely (Stirling’s approximation),


_√_ � _n_ �n
_n!_ 2πn _._
_∼_

_e_


Hence,
log n! _n log n + Θ(n)._
_∼_

**Conclusion**

_T_ (n) = Ω(n log n), and hence any sorting algorithm based on comparisons and swaps must make
Ω(n log n) comparisons in the worst case.

This is called the decision tree lower bound.

Mergesort meets this lower bound. Quicksort
doesn’t.

It can also be shown that any sorting algorithm based on comparisons and swaps must make
Ω(n log n) comparisons on average. Both quicksort
and mergesort meet this bound.

**Assigned Reading**

CLR Chapter 8.

POA 7.5


5


-----

**Summary**


###### Algorithms Course Notes Divide and Conquer 3

 Ian Parberry[∗]

 Fall 2001

The average time for the recursive calls is thus at
most:


More examples of divide and conquer.

selection in average time O(n)

_•_
binary search in time O(log n)

_•_
the towers of Hanoi and the end of the Universe

_•_

**Selection**

Let S be an array of n distinct numbers. Find the
_kth smallest number in S._

**function select(S, k)**
**if** _S_ = 1 then return(S[1]) else
_|_ _|_
Choose an element a from S
Let S1, S2 be the elements of S
which are respectively <, > a
Suppose |S1| = j (a is the (j + 1)st item)
**if k = j + 1 then return(a)**
**else if k ≤** _j then return(select(S1, k))_
**else return(select(S2,k −** _j −_ 1))

Let T (n) be the worst case for all k of the average
number of comparisons used by procedure select on
an array of n numbers. Clearly T (1) = 0.

**Analysis**

Now,

_|S1|_ = _j_
_|S2|_ = _n −_ _j −_ 1

Hence the recursive call needs an average time of
either T (j) or T (n _j_ 1), and j can have any value
_−_ _−_
from 0 to n 1 with equal probability.
_−_

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


1

_n_


_n−1_
�(either T (j) or T (n _j_ 1))

_−_ _−_
_j=0_


When is it T (j) and when is it T (n _j_ 1)?
_−_ _−_

_• k ≤_ _j: recurse on S1, time T_ (j)
_k = j + 1: finished_

_•_

_• k > j + 1: recurse on S2, time T_ (n − _j −_ 1)

The average time for the recursive calls is thus at
most:
1 _k−2_ _n−1_

� _T_ (n _j_ 1) + � _T_ (j))

_−_ _−_

_n_ [(]

_j=0_ _j=k_


Splitting S into S1, S2 takes n − 1 comparisons (as
in quicksort).

Therefore, for n 2,
_≥_


_n−1_
� _T_ (j)) + n 1

_−_
_j=k_


1
_T_ (n)
_≤_
_n_ [(]

1
=
_n_ [(]


_k−2_
� _T_ (n _j_ 1) +

_−_ _−_
_j=0_


_n−1_
� _T_ (j) +

_j=n−k+1_


_n−1_
� _T_ (j)) + n 1

_−_
_j=k_


What value of k maximizes

_n−1_
� _T_ (j) +

_j=n−k+1_


_n−1_
� _T_ (j)?

_j=k_


Decrementing the value of k deletes a term from the
left sum, and inserts a term into the right sum. Since
_T is the running time of an algorithm, it must be_
monotone nondecreasing.


1


-----

Hence we must choose k = n _k + 1. Assume n_
_−_
is odd (the case where n is even is similar). This
means we choose k = (n + 1)/2.

###### Write m=(n+1)/2 (shorthand for this diagram only.)

 k=m

_T(n-m+1)_ _T(m)_
_T(n-m+2)_ _T(m+1)_

_T(n-2)_ _T(n-2)_
_T(n-1)_ _T(n-1)_

###### k=m-1

_T(m-1)_

_T(m)_

_T(n-m+2)_ _T(m+1)_

_T(n-2)_ _T(n-2)_
_T(n-1)_ _T(n-1)_

Therefore,


�


8
=
_n_


� (n 1)(n 2)
_−_ _−_

_−_ [(][n][ −] [3)(][n][ −] [1)]
2 8

|Col1|T(n-m+1)|Col3|
|---|---|---|
|T(n-m+2)|||

|Col1|T(m)|Col3|
|---|---|---|
|T(m+1)|||

|Col1|. . . T(n-m+2) T(n-m+1)|Col3|
|---|---|---|
||T(n-2)||
|T(n-1)|||

|Col1|. . . T(m+1) T(m)|Col3|
|---|---|---|
||T(n-2)||
|T(n-1)|||

|Col1|. . . T(n-m+2)|Col3|
|---|---|---|
||T(n-2)||
|T(n-1)|||

|Col1|. . . T(m+1) T(m) T(m-1)|Col3|
|---|---|---|
||T(n-2)||
|T(n-1)|||


_T_ (n)
_≤_ [2]

_n_


_n−1_
� _T_ (j) + n 1.

_−_
_j=(n+1)/2_


Claim that T (n) 4(n 1). Proof by induction on
_≤_ _−_
_n. The claim is true for n = 1. Now suppose that_
_T_ (j) 4(j 1) for all j < n. Then,
_≤_ _−_

_T_ (n)


+ n 1
_−_

1
=
_n_ [(4][n][2][ −] [12][n][ + 8][ −] _[n][2][ + 4][n][ −]_ [3) +][ n][ −] [1]

= 3n 8 + [5]
_−_

_n_ [+][ n][ −] [1]

4n 4
_≤_ _−_

Hence the selection algorithm runs in average time
_O(n)._

Worst case O(n[2]) (just like the quicksort analysis).

**Comments**

There is an O(n) worst-case time algorithm

_•_
that uses divide and conquer (it makes a smart
choice of a). The analysis is more difficult.
How should we pick a? It could be S[1] (average

_•_
case significant in the long run) or a random
element of S (the worst case doesn’t happen
with particular inputs).

**Binary Search**

Find the index of x in a sorted array A.

**function search(A, x, ℓ, r)**
**comment find x in A[ℓ..r]**
**if ℓ** = r then return(ℓ) else
_m :=_ (ℓ + r)/2
_⌊_ _⌋_
**if x** _A[m]_
_≤_
**then return(search(A, x, ℓ, m))**
**else return(search(A, x, m + 1, r))**

Suppose n is a power of 2. Let T (n) be the worst case
number of comparisons used by procedure search on
an array of n numbers.

� 0 if n = 1
_T_ (n) =
_T_ (n/2) + 1 otherwise

(As in the maxmin algorithm, we must argue that
the array is cut in half.)

Hence,

_T_ (n) = _T_ (n/2) + 1




+ n 1
 _−_




2
_≤_

_n_

8
_≤_

_n_


 _n−1_

� _T_ (j)


_j=(n+1)/2_


 _n−1_

� (j 1)
 _−_

_j=(n+1)/2_


+ n 1
 _−_


8
=

_n_

8
=

_n_


 _n−2_

�

_j_



_j=(n−1)/2_


n−2

�

_j_

 _−_

_j=1_




+ n 1
 _−_


(n−3)/2 
� _j_ + n 1

 _−_

_j=1_


2


-----

= (T (n/4) + 1) + 1

= _T_ (n/4) + 2
= (T (n/8) + 1) + 2
= _T_ (n/8) + 3
= _T_ (n/2[i]) + i
= _T_ (1) + log n
= log n

Therefore, binary search on an array of size n takes
time O(log n).

**The Towers of Hanoi**

###### 1 2 3

Move all the disks from peg 1 to peg 3 using peg 2 as
workspace without ever placing a disk on a smaller
disk.

To move n disks from peg i to peg j using peg k as
workspace

Move n 1 disks from peg i to peg k using peg

_•_ _−_
_j as workspace._
Move remaining disk from peg i to peg j.

_•_
Move n 1 disks from peg k to peg j using peg

_•_ _−_
_i as workspace._

**How Many Moves?**

Let T (n) be the number of moves it takes to move
_n disks from peg i to peg j._

Clearly,

� 1 if n = 1
_T_ (n) =
2T (n 1) + 1 otherwise
_−_

Hence,

_T_ (n) = 2T (n 1) + 1
_−_
= 2(2T (n 2) + 1) + 1
_−_


= 4T (n 2) + 2 + 1
_−_

= 4(2T (n 3) + 1) + 2 + 1
_−_
= 8T (n 3) + 4 + 2 + 1
_−_

_i−1_

= 2[i]T (n _i) +_ � 2[j]
_−_

_j=0_


= 2[n][−][1]T (1) +

= 2[n] 1
_−_


_n−2_
� 2[j]

_j=0_


**The End of the Universe**

According to legend, there is a set of 64 gold disks
on 3 diamond needles, called the Tower of Brahma.
Legend reports that the Universe will end when the
task is completed. (Edouard Lucas,[´] _R´ecr´eations_
_Math´ematiques, Vol. 3, pp 55–59, Gauthier-Villars,_
Paris, 1893.)

How many moves will it need? If done correctly,
_T_ (64) = 2[64] 1 = 1.84 10[19] moves. At one move
_−_ _×_
per second, that’s

1.84 10[19] seconds
_×_
= 3.07 10[17] minutes
_×_
= 5.12 10[15] hours
_×_
= 2.14 10[14] days
_×_
= 5.85 10[11] years
_×_

Current age of Universe is 10[10] years.
_≈_


3


-----

**The Answer to Life, the Universe, and**
**Everything**

## 42
 2[64]-1

###### = 18,446,744,073,709,552,936

**A Sneaky Algorithm**

What if the monks are not good at recursion?

Imagine that the pegs are arranged in a circle. Instead of numbering the pegs, think of moving the
disks one place clockwise or anticlockwise.

_Clockwise_

###### 2

 3 1

**Impress Your Friends and Family**

If there are an odd number of disks:

Start by moving the smallest disk in an anti
_•_
clockwise direction.
Alternate between doing this and the only other

_•_
legal move.


If there are an even number of disks, replace “anticlockwise” by “clockwise”.

How do you remember whether to start clockwise or
anticlockwise? Think of what happens with n = 1
and n = 2.

###### Odd

1 2 3 1 2 3

###### Even

1 2 3 1 2 3

1 2 3 1 2 3

What happens if you use the wrong direction?

**A Formal Algorithm**

Let D be a direction, either clockwise or anticlock_wise. Let D be the opposite direction._

To move n disks in direction D, alternate between
the following two moves:

If n is odd, move the smallest disk in direction

_•_
_D. If n is even, move the smallest disk in direc-_
tion D.
Make the only other legal move.

_•_

This is exactly what the recursive algorithm does!
Or is it?

**Formal Claim**

When the recursive algorithm is used to move n disks
in direction D, it alternates between the following
two moves:


4


-----

If n is odd, move the smallest disk in direction

_•_
_D. If n is even, move the smallest disk in direc-_
tion D.
Make the only other legal move.

_•_

**The Proof**

Proof by induction on n. The claim is true when
_n = 1. Now suppose that the claim is true for n_
disks. Suppose we use the recursive algorithm to
move n+1 disks in direction D. It does the following:

Move n disks in direction D.

_•_
Move one disk in direction D.

_•_
Move n disks in direction D.

_•_

Let

“D” denote moving the smallest disk in direc
_•_
tion D,
“D” denote moving the smallest disk in direc
_•_
tion D
“O” denote making the only other legal move.

_•_

Case 1. n + 1 is odd. Then n is even, and so by the
induction hypothesis, moving n disks in direction D
uses
_DODO_ _OD_
_· · ·_

(NB. The number of moves is odd, so it ends with
_D, not O.)_

Hence, moving n + 1 disks in direction D uses


**Assigned Reading**

CLR Chapter 10.2.

POA 7.5,7.6.


_DODO_ _OD_
_· · ·_
� �� �
_n disks_

as required.


_O DODO_ _OD,_
_· · ·_
� �� �
_n disks_


Case 2. n + 1 is even. Then n is odd, and so by the
induction hypothesis, moving n disks in direction D
uses

_DODO_ _OD_
_· · ·_

(NB. The number of moves is odd, so it ends with
_D, not O.)_

Hence, moving n + 1 disks in direction D uses


_DODO_ _OD_
_· · ·_
� �� �
_n disks_

as required.


_O DODO_ _OD,_
_· · ·_
� �� �
_n disks_


Hence by induction the claim holds for any number
of disks.


5


-----

**Summary**


###### Algorithms Course Notes Dynamic Programming 1

 Ian Parberry[∗]

 Fall 2001

Correctness Proof: A simple induction on n.


Dynamic programming: divide and conquer with a
table.

Application to:

Computing combinations

_•_
Knapsack problem

_•_

**Counting Combinations**

To choose r things out of n, either

Choose the first item. Then we must choose the

_•_
remaining r 1 items from the other n 1 items.
_−_ _−_
Or
Don’t choose the first item. Then we must

_•_
choose the r items from the other n 1 items.
_−_


Analysis: Let T (n) be the worst case running time
of choose(n, r) over all possible values of r.

Then,

� _c_ if n = 1
_T_ (n) =
2T (n 1) + d otherwise
_−_

for some constants c, d.

Hence,

_T_ (n) = 2T (n 1) + d
_−_
= 2(2T (n 2) + d) + d
_−_
= 4T (n 2) + 2d + d
_−_
= 4(2T (n 3) + d) + 2 + d
_−_
= 8T (n 3) + 4d + 2d + d
_−_

_i−1_

= 2[i]T (n _i) + d_ � 2[j]
_−_

_j=0_


Therefore,

� _n_
_r_


� � _n_ 1
= _−_
_r_ 1
_−_


�


= 2[n][−][1]T (1) + d


� � _n_ 1
+ _−_
_r_


_n−2_
� 2[j]

_j=0_


**Divide and Conquer**

This gives a simple divide and conquer algorithm
for finding the number of combinations of n things
chosen r at a time.

**function choose(n, r)**
**if r = 0 or n = r then return(1) else**
**return(choose(n** 1, r 1) +
_−_ _−_
choose(n 1, r))
_−_

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


= (c + d)2[n][−][1] _d_
_−_

Hence, T (n) = Θ(2[n]).

**Example**

The problem is, the algorithm solves the same subproblems over and over again!


1


-----

1
1


T


**Initialization**

0 _r_
0

_n-r_

_n_

**General Rule**


1
0


1
1


1
0


1
1


6
4

1
0


**Repeated Computation**

6
4

5 5
3 4

4 4 4
2 3 3

3 3 3 3 3 3
1 2 2 3 2 3

2 2 2 2 2 2
1 2 1 2 1 2

1 1 1 1 1 1
0 1 0 1 0 1

**A Better Algorithm**

Pascal’s Triangle. Use a table T[0..n, 0..r].


Required answer

|Col1|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Required|
|---|---|---|---|---|---|---|---|---|---|
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||


3
2

2 2
1 2

1 1
0 1


3
2

2 2
1 2

1 1
0 1


� _i_
T[i, j] holds
_j_


3
2

2 2 2
2 1 2

1 1
0 1


�
_._


1
2 13
3 14 25
4 15 26
5 16 27
6 17 28
7 18 29
8 19 30


**function choose(n, r)**
**for i := 0 to n** _r do T[i, 0]:=1;_
_−_
**for i := 0 to r do T[i, i]:=1;**
**for j := 1 to r do**
**for i := j + 1 to n** _r + j do_
_−_
T[i, j]:=T[i 1, j 1] + T[i 1, j]
_−_ _−_ _−_
**return(T[n, r])**


To fill in T[i, j], we need T[i 1, j 1] and T[i 1, j]
_−_ _−_ _−_
to be already filled in.

_j-1_ _j_

_i-1_

_i_ +

**Filling in the Table**

Fill in the columns from left to right. Fill in each of
the columns from top to bottom.

0 _r_
0

1
2 13
3 14 25
4 15 26
5 16 27
6 17 28
7 18 29 Numbers show the
8 19 30 order in which the
9 20 31 entries are filled in
10 21 32

_n-r_ 11 22 33

12 23 34
24 35
36

_n_

|0|Col2|Col3|Col4|Col5|Col6|Col7|r|
|---|---|---|---|---|---|---|---|
|||||||||
|||||||||
||1|||||||
||2|13||||||
||3|14|25|||||
||4|15|26|||||
||5|16|27|||||
||6|17|28|||||
||7|18|29|||||
||8|19|30|||||
||9|20|31|||||
||10|21|32|||||
||11|22|33|||||
||12|23|34|||||
|||24|35|||||
||||36|||||
|||||||||
|||||||||
|||||||||
|||||||||
|||||||||
|||||||||


###### +


2


-----

**Example**

0 _r_
0 1

1 1
1 2 1
1 3 3 1
1 4 6 1
1 5 1 6+4=10
1 6 1
1 7 1
1 8 1
1 9 1
1 10
1 11

_n-r_ 1 12

13

_n_

**Analysis**

How many table entries are filled in?

(n _r + 1)(r + 1) = nr + n_ _r[2]_ + 1 _n(r + 1) + 1_
_−_ _−_ _≤_

Each entry takes time O(1), so total time required
is O(n[2]).

This is much better than O(2[n]).

Space: naive, O(nr). Smart, O(r).

**Dynamic Programming**

When divide and conquer generates a large number
of identical subproblems, recursion is too expensive.

Instead, store solutions to subproblems in a table.

This technique is called dynamic programming.

**Dynamic Programming Technique**

To design a dynamic programming algorithm:

Identification:

devise divide-and-conquer algorithm

_•_
analyze — running time is exponential

_•_
same subproblems solved many times

_•_

Construction:


take part of divide-and-conquer algorithm that

_•_
does the “conquer” part and replace recursive
calls with table lookups
instead of returning a value, record it in a table

_•_
entry
use base of divide-and-conquer to fill in start of

_•_
table
devise “look-up template”

_•_
devise for-loops that fill the table using “look
_•_
up template”

###### Divide and Conquer

function choose(n,r)
if r=0 or r=n then return(1) else

return(choose(n-1,r-1)+choose(n-1,r))

###### Dynamic Programming

function choose(n,r)

for i:=0 to n-r do T[i,0]:=1
for i:=0 to r do T[i,i]:=1

for j:=1 to r do
for i:=j+1 to n-r+j do

T[i,j]:=T[i-1,j-1]+T[i-1,j]

return(T[n,r])

**The Knapsack Problem**

Given n items of length s1, s2, . . ., sn, is there a subset of these items with total length exactly S?

###### s1 s2 s3 s4 s5 s6 s7

 S

 s1 s3 s6

 s2 s4 s5 s7

 S

|0|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|r|Col11|
|---|---|---|---|---|---|---|---|---|---|---|
|1||||||||||6+4=10|
|1|1||||||||||
|1|2|1|||||||||
|1|3|3|1||||||||
|1|4|6||1|||||||
|1|5||||||||||
||||||1||||||
|1|6|||||1|||||
|1|7||||||1||||
|1|8|||||||1|||
|1|9||||||||1||
|1|10||||||||||
|1|11||||||||||
|1|12||||||||||
||13||||||||||
||||||||||||
||||||||||||
||||||||||||
||||||||||||
||||||||||||
||||||||||||
||||||||||||
||||||||||||

|Col1|Col2|Col3|Col4|
|---|---|---|---|


1

2 1

3 3 1

4 6 1
5 1
6 1
7 1
8 1


3


13


-----

**Divide and Conquer**

Want knapsack(i, j) to return true if there is a subset of the first i items that has total length exactly
_j._

###### s1 s2 s3 s4 si-1 si
 . . .

 j

When can knapsack(i, j) return true? Either the
_ith item is used, or it is not._

If the ith item is not used, and knapsack(i 1, j)

_•_ _−_
returns true.

###### s1 s2 s3 s4 si-1 . . .


###### j



_• If the ith item is used, and knapsack(i−1, j−si)_
returns true.

###### s1 s2 s3 s4 si-1 . . .
 j- si si

 j

**The Code**

Call knapsack(n, S).

**function knapsack(i, j)**
**comment returns true if s1, . . ., si can fill j**
**if i = 0 then return(j=0)**
**else if knapsack(i** 1, j) then return(true)
_−_
**else if si ≤** _j then_
**return(knapsack(i −** 1, j − _si))_

Let T (n) be the running time of knapsack(n, S).

� _c_ if n = 1
_T_ (n) =
2T (n 1) + d otherwise
_−_

Hence, by standard techniques, T (n) = Θ(2[n]).


**Dynamic Programming**

Store knapsack(i, j) in table t[i, j].

_t[i, j] is set to true iff either:_

_t[i_ 1, j] is true, or

_•_ _−_

_• t[i −_ 1, j − _si] makes sense and is true._

This is done with the following code:

_t[i, j] := t[i_ 1, j]
_−_
**if j −** _si ≥_ 0 then
_t[i, j] := t[i, j] or t[i −_ 1, j − _si]_

_j-s i_ _j_

_i-1_

_i_

**Filling in the Table**

###### 0 S
 0 t f f f f f f f

 n

**The Algorithm**

**function knapsack(s1, s2, . . ., sn, S)**
1. _t[0, 0] :=true_
2. **for j := 1 to S do t[0, j] :=false**
3. **for i := 1 to n do**
4. **for j := 0 to S do**
5. _t[i, j] := t[i_ 1, j]
_−_
6. **if j −** _si ≥_ 0 then
7. _t[i, j] := t[i, j] or t[i −_ 1, j − _si]_
8. **return(t[n, S])**

Analysis:

Lines 1 and 8 cost O(1).

_•_

|Col1|Col2|
|---|---|

|0|Col2|Col3|Col4|Col5|Col6|Col7|S|
|---|---|---|---|---|---|---|---|
|t|f|f|f|f|f|f|f|
|||||||||
|||||||||
|||||||||
|||||||||
|||||||||
|||||||||
|||||||||


4


-----

The for-loop on line 2 costs O(S).

_•_
Lines 5–7 cost O(1).

_•_
The for-loop on lines 4–7 costs O(S).

_•_
The for-loop on lines 3–7 costs O(nS).

_•_

Therefore, the algorithm runs in time O(nS). This
is usable if S is small.

**Example**

_s1 = 1, s2 = 2 s3 = 2, s4 = 4, s5 = 5, s6 = 2, s7 = 4,_
_S = 15._

_t[i, j]_ := _t[i −_ 1, j] or t[i − 1, j − _si]_
_t[3, 3]_ := _t[2, 3] or t[2, 3 −_ _s3]_
_t[3, 3]_ := _t[2, 3] or t[2, 1]_

0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15
0 t f `f f f f f f f f f f f f f f`

1 `t` `t f f f f f f f f f f f f f f`
2 `t` `t` `t` `t` `f f f f f f f f f f f f`
3 `t` `t` `t` `t`
4
5
6
7

_t[i, j]_ := _t[i −_ 1, j] or t[i − 1, j − _si]_
_t[3, 4]_ := _t[2, 4] or t[2, 4 −_ _s3]_
_t[3, 4]_ := _t[2, 4] or t[2, 2]_


0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15
0 t f `f f f f f f f f f f f f f f`

1 `t` `t f f f f f f f f f f f f f f`
2 `t` `t` `t` `t` `f f f f f f f f f f f f`
3 `t` `t` `t` `t` `t t` `f f f f f f f f f f`
4 `t` `t` `t` `t` `t t` `t t t t` `f f f f f f`
5 `t` `t` `t` `t` `t t` `t t t t` `t t t t t f`
6 `t` `t` `t` `t` `t t` `t t t t` `t t` `t t t t`
7 `t` `t` `t` `t` `t t` `t t t t` `t t` `t t t t`

Question: Can we get by with 2 rows?

Question: Can we get by with 1 row?

**Assigned Reading**

CLR Section 16.2.

POA Section 8.2.

|t|f|f|f|f|f|f|f|f|f|f|f|f|f|f|f|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|t|t|f|f|f|f|f|f|f|f|f|f|f|f|f|f|
|t|t|t|t|f|f|f|f|f|f|f|f|f|f|f|f|
|t|t|t|t|t|t|f|f|f|f|f|f|f|f|f|f|
|t|t|t|t|t|t|t|t|t|t|f|f|f|f|f|f|
|t|t|t|t|t|t|t|t|t|t|t|t|t|t|t|f|
|t|t|t|t|t|t|t|t|t|t|t|t|t|t|t|t|
|t|t|t|t|t|t|t|t|t|t|t|t|t|t|t|t|

|t|f|f|f|f|f|f|f|f|f|f|f|f|f|f|f|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|t|t|f|f|f|f|f|f|f|f|f|f|f|f|f|f|
|t|t|t|t|f|f|f|f|f|f|f|f|f|f|f|f|
|t|t|t|t|||||||||||||
|||||||||||||||||
|||||||||||||||||
|||||||||||||||||
|||||||||||||||||


0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15
0 t f `f f f f f f f f f f f f f f`

1 `t` `t f f f f f f f f f f f f f f`
2 `t` `t` `t` `t` `f` `f f f f f f f f f f f`
3 `t` `t` `t` `t` `t`
4
5
6
7

|t|f|f|f|f|f|f|f|f|f|f|f|f|f|f|f|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|t|t|f|f|f|f|f|f|f|f|f|f|f|f|f|f|
|t|t|t|t|f|f|f|f|f|f|f|f|f|f|f|f|
|t|t|t|t|t||||||||||||
|||||||||||||||||
|||||||||||||||||
|||||||||||||||||
|||||||||||||||||


5


-----

###### Algorithms Course Notes Dynamic Programming 2

 Ian Parberry[∗]

 Fall 2001


**Summary**

Dynamic programming applied to

Matrix products problem

_•_

**Matrix Product**

Consider the problem of multiplying together n rectangular matrices.

_M = M1 · M2 · · · Mn_

where each Mi has ri−1 rows and ri columns.

Suppose we use the naive matrix multiplication algorithm. Then a multiplication of a p _q matrix by_
_×_
a q _r matrix takes pqr operations._
_×_

Matrix multiplication is associative, so we can evaluate the product in any order. However, some orders
are cheaper than others. Find the cost of the cheapest one.

N.B. Matrix multiplication is not commutative.

**Example**

If we multiply from right to left:

_M = M1 · (M2 · (M3 · M4))_

_∗Copyright c⃝_ Ian Parberry, 1992–2001.

|50 x 1|1 x 100|
|---|---|


###### 10 x 100


_Cost = 5000_

_Cost = 100,000_

_Cost = 20,000_


Total cost is 5, 000 + 100, 000 + 20, 000 = 125, 000.

However, if we begin in the middle:

_M = (M1 · (M2 · M3)) · M4_

###### 10 x 20 20 x 50 50 x 1 1 x 100

|10 x 20|20 x 50|50 x 1|
|---|---|---|


###### 10 x 1


###### 20 x 1

 10 x 100


_Cost = 1000_

_Cost = 200_

_Cost = 1000_


Total cost is 1000 + 200 + 1000 = 2200.

**The Naive Algorithm**

One way is to try all possible ways of parenthesizing
the n matrices. However, this will take exponential time since there are exponentially many ways of
parenthesizing them.

Let X(n) be the number of ways of parenthesizing
the n matrices. It is easy to see that X(1) = X(2) =


1


-----

1 and for n > 2,

_X(n) =_


_n−1_
� _X(k)_ _X(n_ _k)_

_·_ _−_
_k=1_


(just consider breaking the product into two pieces):


(M1 · M2 · · · Mk)
� �� �
_X(k) ways_

Therefore,



_· (Mk+1 · · · Mn)_
� �� �
_X(n_ _k) ways_
_−_


_X(3)_ =


2
� _X(k)_ _X(3_ _k)_

_·_ _−_
_k=1_


= _X(1)_ _X(2) + X(2)_ _X(1)_
_·_ _·_
= 2

This is easy to verify: x(xx), (xx)x.

_X(4)_


=


3
� _X(k)_ _X(4_ _k)_

_·_ _−_
_k=1_


= _X(1)_ _X(3) + X(2)_ _X(2) + X(3)_ _X(1)_
_·_ _·_ _·_
= 5

This is easy to verify: x((xx)x), x(x(xx)), (xx)(xx),
((xx)x)x, (x(xx))x.

Claim: X(n) 2[n][−][2]. Proof by induction on n. The
_≥_
claim is certainly true for n 4. Now suppose n 5.
_≤_ _≥_
Then


**Divide and Conquer**

Let cost(i, j) be the minimum cost of computing

_Mi · Mi+1 · · · Mj._

What is the cost of breaking the product at Mk?

(Mi · Mi+1 · · · Mk) · (Mk+1 · · · Mj).

It is cost(i, k) plus cost(k + 1, j) plus the cost of
multiplying an ri−1 _×rk matrix by an rk_ _×rj matrix._

Therefore, the cost of breaking the product at Mk is

cost(i, k) + cost(k + 1, j) + ri−1rkrj.

**A Divide and Conquer Algorithm**

This gives a simple divide and conquer algorithm.
Simply call cost(1, n).

**function cost(i, j)**
**if i = j then return(0) else**
**return(mini≤k<j(cost(i, k) + cost(k + 1, j)**
+ ri−1rkrj))

Correctness Proof: A simple induction.

Analysis: Let T (n) be the worst case running time
of cost(i, j) when j _i + 1 = n._
_−_

Then, T (0) = c and for n > 0,


_n−1_
� (T (m) + T (n _m)) + dn_

_−_
_m=1_


_X(n)_ =

_≥_

=


_n−1_
� _X(k)_ _X(n_ _k)_

_·_ _−_
_k=1_

_n−1_
� 2[k][−][2]2[n][−][k][−][2] (by ind. hyp.)

_k=1_


_n−1_
� 2[n][−][4]

_k=1_


_T_ (n) =


_T_ (n) = 2


for some constants c, d.

Hence, for n > 0,


_n−1_
� _T_ (m) + dn.

_m=1_


= (n 1)2[n][−][4]
_−_

2[n][−][2] (since n 5)
_≥_ _≥_

Actually, it can be shown that


�
_._


Therefore,

_T_ (n) _T_ (n 1)
_−_ _−_

_n−1_

= (2 � _T_ (m) + dn) (2

_−_
_m=1_

= 2T (n 1) + d
_−_


_n−2_
� _T_ (m) + d(n 1))

_−_
_m=1_


_X(n) = [1]_

_n_


� 2(n 1)
_−_
_n_ 1
_−_


2


-----

That is,
_T_ (n) = 3T (n 1) + d
_−_

And so,

_T_ (n) = 3T (n 1) + d
_−_
= 3(3T (n 2) + d) + d
_−_
= 9T (n 2) + 3d + d
_−_
= 9(3T (n 3) + d) + 3d + d
_−_
= 27T (n 3) + 9d + 3d + d
_−_

_m−1_

= 3[m]T (n _m) + d_ � 3[ℓ]
_−_

_ℓ=0_

_n−1_

= 3[n]T (0) + d � 3[ℓ]

_ℓ=0_

= _c3[n]_ + d [3][n][ −] [1]

2
= (c + d/2)3[n] _d/2_
_−_


Hence, T (n) = Θ(3[n]).

**Example**

The problem is, the algorithm solves the same subproblems over and over again!

cost(1,4)

1,1 1,2 1,3 2,4 3,4 4,4

1,1 2,2 1,1 1,2 2,3 3,3 2,2 2,3 3,4 4,4 3,3 4,4

1,1 2,2 2,2 3,3 2,2 3,3 3,3 4,4

**Dynamic Programming**

This is a job for . . .

#### D

Dynamic programming!


Faster than a speeding divide and conquer!

Able to leap tall recursions in a single bound!

**Details**

Store cost(i, j) in m[i, j]. Therefore, m[i, j] = 0 if
_i = j, and_

min
_i≤k<j[(][m][[][i, k][] +][ m][[][k][ + 1][, j][] +][ r][i][−][1][r][k][r][j][)]_

otherwise.

When we fill in the table, we had better make sure
that m[i, k] and m[k + 1, j] are filled in before we
compute m[i, j]. Compute entries of m[] in increasing order of difference between parameters.

_j_
_i_

_i_

_j_

**Example**

_r0 = 10, r1 = 20, r2 = 50, r3 = 1, r4 = 100._

_m[1, 2]_ = min
1≤k<2[(][m][[1][, k][] +][ m][[][k][ + 1][,][ 2] +][ r][0][r][k][r][2][)]

= _r0r1r2 = 10000_
_m[2, 3]_ = _r1r2r3 = 1000_
_m[3, 4]_ = _r2r3r4 = 5000_

|Col1|Col2|Col3|
|---|---|---|

|Col1|Col2|Col3|
|---|---|---|


#### D


3


-----

|0|10K|Col3|Col4|
|---|---|---|---|
||0|1K||
|||0|5K|
||||0|


_m[1, 3]_
= min
1≤k<3[(][m][[1][, k][] +][ m][[][k][ + 1][,][ 3] +][ r][0][r][k][r][3][)]

= min(m[1, 1] + m[2, 3] + r0r1r3,
_m[1, 2] + m[3, 3] + r0r2r3)_
= min(0 + 1000 + 200, 10000 + 0 + 500)
= 1200

###### 0 10K 1.2K

 0 1K

 0 5K

 0

_m[2, 4]_

= min
2≤k<4[(][m][[2][, k][] +][ m][[][k][ + 1][,][ 4] +][ r][1][r][k][r][4][)]

= min(m[2, 2] + m[3, 4] + r1r2r4,
_m[2, 3] + m[4, 4] + r1r3r4)_
= min(0 + 5000 + 100000, 1000 + 0 + 2000)
= 3000

###### 0 10K 1.2K

 0 1K 3K

 0 5K

 0

_m[1, 4]_
= min
1≤k<4[(][m][[1][, k][] +][ m][[][k][ + 1][,][ 4] +][ r][0][r][k][r][4][)]


= min(m[1, 1] + m[2, 4] + r0r1r4,

_m[1, 2] + m[3, 4] + r0r2r4,_
_m[1, 3] + m[4, 4] + r0r3r4)_
= min(0 + 3000 + 20000,
10000 + 5000 + 50000,
1200 + 0 + 1000)
= 2200

###### 0 10K 1.2K2.2K

 0 1K 3K

 0 5K

 0

**Filling in the Diagonal**

**for i := 1 to n do m[i, i] := 0**

###### 1 n

 1

 n

**Filling in the First Superdiagonal**

**for i := 1 to n** 1 do
_−_
_j := i + 1_
_m[i, j] :=_
_· · ·_

|0|10K|1.2K|2.2K|
|---|---|---|---|
||0|1K|3K|
|||0|5K|
||||0|

|0|10K|1.2K|Col4|
|---|---|---|---|
||0|1K||
|||0|5K|
||||0|

|0|10K|1.2K|Col4|
|---|---|---|---|
||0|1K|3K|
|||0|5K|
||||0|


4


-----

###### 1 n

 1

 n

**Filling in the Second Superdiagonal**

**for i := 1 to n** 2 do
_−_
_j := i + 2_
_m[i, j] :=_
_· · ·_

###### 1 n

 1

 n

**Filling in the dth Superdiagonal**

**for i := 1 to n** _d do_
_−_
_j := i + d_
_m[i, j] :=_
_· · ·_


###### 1

 n


###### 1 d+1 n

**The Algorithm**


###### n-d


**function matrix(n)**
1. for i := 1 to n do m[i, i] := 0
2. for d := 1 to n 1 do
_−_
3 **for i := 1 to n** _d do_
_−_
4. _j := i + d_
5. _m[i, j] := mini≤k<j(m[i, k] + m[k + 1, j]_
+ri−1rkrj)
6. return(m[1, n])

Analysis:

Line 1 costs O(n).

_•_
Line 5 costs O(n) (can be done with a single

_•_
for-loop).
Lines 4 and 6 costs O(1).

_•_
The for-loop on lines 3–5 costs O(n[2]).

_•_
The for-loop on lines 2–5 costs O(n[3]).

_•_

Therefore the algorithm runs in time O(n[3]). This
is a characteristic of many dynamic programming
algorithms.


5


-----

**Other Orders**

###### 1 8 14 19 23 26 28 1 13 14 22 23 26 28 2 9 15 20 24 27 2 12 15 21 24 27 3 10 16 21 25 3 11 16 20 25 4 11 17 22 4 10 17 19 5 12 18 5 9 18 6 13 6 8 7 7

 1 3 6 10 15 21 28 22 23 24 25 26 27 28 2 5 9 14 20 27 16 17 18 19 20 21
 4 8 13 19 26 11 12 13 14 15
 7 12 18 25 7 8 9 10
 11 17 24 4 5 6
 16 23 2 3
 22 1

**Assigned Reading**

CLR Section 16.1, 16.2.

POA Section 8.1.

|1|8|14|19|23|26|28|
|---|---|---|---|---|---|---|
||2|9|15|20|24|27|
|||3|10|16|21|25|
||||4|11|17|22|
|||||5|12|18|
||||||6|13|
|||||||7|

|1|13|14|22|23|26|28|
|---|---|---|---|---|---|---|
||2|12|15|21|24|27|
|||3|11|16|20|25|
||||4|10|17|19|
|||||5|9|18|
||||||6|8|
|||||||7|

|1|3|6|10|15|21|28|
|---|---|---|---|---|---|---|
||2|5|9|14|20|27|
|||4|8|13|19|26|
||||7|12|18|25|
|||||11|17|24|
||||||16|23|
|||||||22|

|22|23|24|25|26|27|28|
|---|---|---|---|---|---|---|
||16|17|18|19|20|21|
|||11|12|13|14|15|
||||7|8|9|10|
|||||4|5|6|
||||||2|3|
|||||||1|


6


-----

###### Algorithms Course Notes Dynamic Programming 3

 Ian Parberry[∗]

 Fall 2001

**Summary** 1. search(x, S) return true iff x _S._

_∈_

2. min(S) return the smallest value in S.

Binary search trees

3. delete(x, S) delete x from S.

Their care and feeding

_•_

4. insert(x, S) insert x into S.

Yet another dynamic programming example –

_•_
optimal binary search trees

**The Search Operation**

**Binary Search Trees**

**procedure search(x, v)**
**comment is x in BST with root v?**

A binary search tree (BST) is a binary tree with the

**if x = ℓ(v) then return(true) else**

data stored in the nodes.

**if x < ℓ(v) then**
**if v has a left child w**

1. The value in a node is larger than the values in

**then return(search(x, w))**

its left subtree.

**else return(false)**

2. The value in a node is smaller than the values **else if v has a right child w**
in its right subtree. **then return(search(x, w))**

**else return(false)**

Note that this implies that the values must be distinct. Let ℓ(v) denote the value stored at node v. Correctness: An easy induction on the number of

layers in the tree.

**Examples** Analysis: Let T (d) be the runtime on a BST of d

layers. Then T (0) = 0 and for d > 0, T (d) _T_ (d
_≤_ _−_
1) + O(1). Therefore, T (d) = O(d).

###### 10 15

 5 15
 5 The Min Operation

 2 7 12 2 10

**procedure min(v);**
**comment return smallest in BST with root v**

###### 7 12

**if v has a left child w**
**then return(min(w))**
**else return(ℓ(v)))**

**Application**

Correctness: An easy induction on the number of

Binary search trees are useful for storing a set S of layers in the tree.
ordered elements, with operations:

_∗Copyright c⃝_ Ian Parberry, 1992–2001. Analysis: Once again O(d).

1


-----

**The Delete Operation**

To delete x from the BST:

Procedure search can be modified to return the node
_v that has value x (instead of a Boolean value). Once_
this has been found, there are four cases.

1. v is a leaf.

Then just remove v from the tree.

2. v has exactly one child w, and v is not the root.

Then make the parent of v the parent of w.

###### v x w

 w

3. v has exactly one child w, and v is the root.

Then make w the new root.

###### v x w

 w

4. v has 2 children.

This is the interesting case. First, find the smallest
element s in the right subtree of v (using procedure
min). Delete s (note that this uses case 1 or 2 above).
Replace the value in node v with s.


Note: could have used largest in left subtree for s.

Correctness: Obvious for cases 1, 2, 3. In case 4,
_s is larger than all of the values in the left subtree_
of v, and smaller than the other values in the right
subtree of v. Therefore s can replace the value in v.

Analysis: Running time O(d) — dominated by
search for node v.

**The Insert Operation**

**procedure insert(x, v);**
**comment insert x in BST with root v**
**if v is the empty tree**
**then create a root node v with ℓ(v) = x**
**else**
**if x < ℓ(v) then**
**if v has a left child w**
**then insert(x, w)**
**else**
create a new left child w of v
_ℓ(w) := x_
**else if x > ℓ(v) then**
**if v has a right child w**
**then insert(x, w)**
**else**
create a new right child w of v
_ℓ(w) := x_

Correctness: Once again, an easy induction.

Analysis: Once again O(d).

**Analysis**

All operations run in time O(d).

But how big is d?

The worst case for an n node BST is O(n) and
Ω(log n).


2


-----

_n_
�

= _n_ 1 + [1] _T_ (j 1) +
_−_ _−_

_n_ [(]

_j=1_


_n_
�

_T_ (n _j))_
_−_
_j=1_


= _n_ 1 + [2]
_−_

_n_


_n−1_
�

_T_ (j)

_j=0_


The average case is O(log n).

**Average Case Analysis**

What is the average case running time for n insertions into an empty BST? Suppose we insert
_x1, . . ., xn, where x1 < x2 < · · · < xn (not neces-_
sarily inserted in that order). Then

Run time is proportional to number of compar
_•_
isons.
Measure number of comparisons, T (n).

_•_

_• The root is equally likely to be xj for 1 ≤_ _j ≤_ _n_
(whichever is inserted first).

Suppose the root is xj. List the values to be inserted
in ascending order.

_• x1, . . ., xj−1: these go to the left of the root;_
needs j 1 comparisons to root, T (j 1) com_−_ _−_
parisons to each other.

_• xj: this is the root; needs no comparisons_

_• xj+1, . . ., xn: these go to the right of the root;_
needs n _j comparisons to root, T_ (n _j) com-_
_−_ _−_
parisons to each other.

Therefore, when the root is xj the total number of
comparisons is

_T_ (j 1) + T (n _j) + n_ 1
_−_ _−_ _−_

Therefore, T (0) = 0, and for n > 0,


This is just like the quicksort analysis! It can be
shown similarly that T (n) _kn log n where k =_
_≤_
loge 4 ≈ 1.39.

Therefore, each insert operation takes O(log n) time
on average.

**Optimal Binary Search Trees**

Given:

_• S = {x1, . . . xn}, xi < xi+1 for 1 ≤_ _i < n._

_• For all 1 ≤_ _i ≤_ _n, the probability pi that we_
will be asked search(xi, S).

_• For all 0 ≤_ _i ≤_ _n, the probability qi that we will_
be asked search(x, S) for some xi < x < xi+1
(where x0 = −∞, xn+1 = ∞).

The problem: construct a BST that has the minimum number of expected comparisons.

**Fictitious Nodes**

Add fictitious nodes labelled 0, 1, . . ., n to the BST.
Node i is where we would fall off the tree on a query
search(x, S) where xi < x < xi+1.

Example:

###### p5 x 5

 p3 x 3 x 8 p8
 p2 x 2 p4 x 4 p6 x 6 x 10 p10

 p1 x 1 2 q2 q3 3 4 5 x 7 p7 p9 x 9 10
 q4 q5 q10


###### 10


###### 2


###### 4


###### q0


###### 3


###### q1


###### 5


###### q6 q7 q8 q9

**Depth of a Node**


###### 9


###### 1


###### 7


1
_T_ (n) =
_n_


###### 0


###### 8


_n_
�

(n 1 + T (j 1) + T (n _j))_
_−_ _−_ _−_
_j=1_


###### 6


Definition: The depth of a node v is


3


-----

0 if v is the root

_•_
_d + 1 if v’s parent has depth d_

_•_

###### 0 15

 1 5

 2 2 10

 3 7 12

**Cost of a Node**

Let depth(xi) be the depth of the node v with ℓ(v) =
_xi._

Number of comparisons for search(xi, S) is

depth(xi) + 1.

This happens with probability pi.

Number of comparisons for search(x, S) for some
_xi < x < xi+1 is_
depth(i).

This happens with probability qi.

**Cost of a BST**

The expected number of comparisons is therefore


Let


_j_
�

_qh._

_h=i_


_wi,j =_


_j_
�

_ph +_
_h=i+1_


What is wi,j? Call it the weight of Ti,j. Increasing
the depths by 1 by making Ti,j the child of some
node increases the cost of Ti,j by wi,j.


_j_
�

_qhdepth(h)._
_h=i_


_ci,j =_


_j_
�

_ph(depth(xh) + 1) +_
_h=i+1_

|Col1|15|Col3|
|---|---|---|
|1|5||
|2|2 10||
||7 12||


_n_
�

_ph(depth(xh) + 1)_

_h=1_

� �� �
real


+


_n_
�

_qhdepth(h)_

_h=0_

� �� �
fictitious


_._


Given the probabilities, we want to find the BST
that minimizes this value.

Call it the cost of the BST.

**Weight of a BST**

Let Ti,j be the min cost BST for xi+1, . . ., xj, which
has fictitious nodes i, . . ., j. We are interested in
_T0,n._

Let ci,j be the cost of Ti,j.


###### Ti,j nodes x ,...,xi+1 j

 i j

**Constructing Ti,j**

To find the best tree Ti,j:

Choose a root xk. Construct Ti,k−1 and Tk,j.

###### xk

 Ti,k-1 Tk,j

**Computing ci,j**

_ci,j_ = (ci,k−1 + wi,k−1) + (ck,j + wk,j) + pk
= _ci,k−1 + ck,j + (wi,k−1 + wk,j + pk)_


= _ci,k−1 + ck,j +_


_k−1_ _k−1_
� �

_ph +_ _qh +_
_h=i+1_ _h=i_


4


-----

_j_
�

_ph +_
_h=k+1_


_j_
�

_qh + pk_
_h=k_


_j_ _j_
� �

= _ci,k−1 + ck,j +_ _ph +_ _qh_

_h=i+1_ _h=i_

= _ci,k−1 + ck,j + wi,j_

Which xk do we choose to be the root?

Pick k in the range i + 1 _k_ _j such that_
_≤_ _≤_

_ci,j = ci,k−1 + ck,j + wi,j_

is smallest.

Loose ends:

if k = i + 1, there is no left subtree

_•_
if k = j, there is no right subtree

_•_

_• Ti,i is the empty tree, with wi,i = qi, and ci,i =_
0.

**Dynamic Programming**

To compute the cost of the minimum cost BST, store
_ci,j in a table c[i, j], and store wi,j in a table w[i, j]._

**for i := 0 to n do**
_w[i, i] := qi_
_c[i, i] := 0_
**for ℓ** := 1 to n do
**for i := 0 to n** _ℓ_ **do**
_−_
_j := i + ℓ_
_w[i, j] := w[i, j −_ 1] + pj + qj
_c[i, j] := mini<k≤j(c[i, k −_ 1] + c[k, j] + w[i, j])

Correctness: Similar to earlier examples.

Analysis: O(n[3]).

**Assigned Reading**

CLR, Chapter 13.

POA Section 8.3.


5


-----

**Summary**


###### Algorithms Course Notes Dynamic Programming 4

 Ian Parberry[∗]

 Fall 2001

**Directed Graphs**


Dynamic programming applied to

All pairs shortest path problem (Floyd’s Algo
_•_
rithm)
Transitive closure (Warshall’s Algorithm)

_•_

Constructing solutions using dynamic programming

All pairs shortest path problem

_•_
Matrix product

_•_

**Graphs**

A graph is an ordered pair G = (V, E) where

_V is a finite set of vertices_
_E_ _V_ _V is a set of edges_
_⊆_ _×_

For example,

_V_ = 1, 2, 3, 4, 5
_{_ _}_
_E_ = (1, 2), (1, 4), (1, 5), (2, 3),
_{_
(3, 4), (3, 5), (4, 5)
_}_

###### 1

 2 5

 3 4

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


A directed graph is a graph with directions on the
edges.

For example,

_V_ = 1, 2, 3, 4, 5
_{_ _}_
_E_ = (1, 2), (1, 4), (1, 5), (2, 3),
_{_
(4, 3), (3, 5), (4, 5)
_}_

###### 1

 2 5

 3 4

**Labelled, Directed Graphs**

A labelled directed graph is a directed graph with
positive costs on the edges.

###### 1

10 100

###### 2 30 5

50 10
60

###### 3 4

20

Applications: cities and distances by road.

**Conventions**

_n is the number of vertices_
_e is the number of edges_


1


-----

Questions:

What is the maximum number of
edges in an undirected graph of n
vertices?

What is the maximum number of
edges in a directed graph of n
vertices?

**Paths in Graphs**

A path in a graph G = (V, E) is a sequence of edges

(v1, v2), (v2, v3), . . ., (vn, vn+1) ∈ _E_

The length of a path is the number of edges.

_•_
The cost of a path is the sum of the costs of the

_•_
edges.

For example, (1, 2), (2, 3), (3, 5). Length 3. Cost 70.

###### 1

10 100

###### 2 30 5

50 10
60

###### 3 4

20

**All Pairs Shortest Paths**

Given a labelled, directed graph G = (V, E), find for
each pair of vertices v, w _V the cost of the shortest_
_∈_
(i.e. least cost) path from v to w.

Define Ak to be an n × n matrix with Ak[i, j] the
cost of the shortest path from i to j with internal
vertices numbered _k._
_≤_

_A0[i, j] equals_

If i = j and (i, j) _E, then the cost of the edge_

_•_ _̸_ _∈_
from i to j.
If i = j and (i, j) _E, then_ .

_•_ _̸_ _̸∈_ _∞_
If i = j, then 0.

_•_

**Computing Ak**

Consider the shortest path from i to j with internal
vertices 1..k. Either:


It does not go through k, in which place it costs

_•_
_Ak−1[i, j]._
It goes through k, in which case it goes through

_•_
_k only once, so it costs Ak−1[i, k] + Ak−1[k, j]._
(Only true for positive costs.)

Vertices numbered at most
_k-1_

###### i j

 k

Hence,

_Ak[i, j] = min{Ak−1[i, j], Ak−1[i, k] + Ak−1[k, j]}_

###### A k-1 j k A k j

 i i

 k

All entries in Ak depend upon row k and column k
of Ak−1.

The entries in row k and column k of Ak are the
same as those in Ak−1.

Row k:

_Ak[k, j]_ = min{Ak−1[k, j],
_Ak−1[k, k] + Ak−1[k, j]}_
= min{Ak−1[k, j], 0 + Ak−1[k, j]}
= _Ak−1[k, j]_

Column k:

_Ak[i, k]_ = min{Ak−1[i, k],
_Ak−1[i, k] + Ak−1[k, k]}_

= min{Ak−1[i, k], Ak−1[i, k] + 0}
= _Ak−1[i, k]_

Therefore, we can use the same array.

|A k|Col2|j|
|---|---|---|
|i|||
||||


2


-----

**Floyd’s Algorithm**

**for i := 1 to n do**
**for j := 1 to n do**
**if (i, j)** _E_
_∈_
**then A[i, j] := cost of (i, j)**
**else A[i, j] :=**
_∞_
_A[i, i] := 0_
**for k := 1 to n do**
**for i := 1 to n do**
**for j := 1 to n do**
**if A[i, k] + A[k, j] < A[i, j] then**
_A[i, j] := A[i, k] + A[k, j]_

Running time: O(n[3]).

0 10 00 30 100 0 10 00 30 100

00 0 50 00 00 00 0 50 00 00

###### A 0 00 00 0 00 10 00 00 0 00 10

00 00 20 0 60 00 00 20 0 60

00 00 00 00 0 00 00 00 00 0

0 10 60 30 70 0 10 60 30 100

00 0 50 00 60 00 0 50 00 00

###### A 3 00 00 0 00 10 00 00 0 00 10

00 00 20 0 30 00 00 20 0 60

00 00 00 00 0 00 00 00 00 0

0 10 50 30 60 0 10 50 30 60

00 0 50 00 60 00 0 50 00 60

###### A 4 00 00 0 00 10 00 00 0 00 10


###### A 1

 A 2

 A 5


**Storing the Shortest Path**

**for i := 1 to n do**
**for j := 1 to n do**

_P_ [i, j] := 0

**if (i, j)** _E_
_∈_
**then A[i, j] := cost of (i, j)**
**else A[i, j] :=**
_∞_
_A[i, i] := 0_
**for k := 1 to n do**
**for i := 1 to n do**
**for j := 1 to n do**
**if A[i, k] + A[k, j] < A[i, j] then**
_A[i, j] := A[i, k] + A[k, j]_

_P_ [i, j] := k

Running time: Still O(n[3]).

Note: On termination, P [i, j] contains a vertex on
the shortest path from i to j.

**Computing the Shortest Path**

**for i := 1 to n do**
**for j := 1 to n do**
**if A[i, j] <** **then**
_∞_
print(i); shortest(i, j); print(j)

**procedure shortest(i, j)**
_k := P_ [i, j]
**if k > 0 then**
shortest(i, k); print(k); shortest(k, j)

Claim: Calling procedure shortest(i, j) prints the internal nodes on the shortest path from i to j.

Proof: A simple induction on the length of the path.

**Warshall’s Algorithm**

Transitive closure: Given a directed graph G =
(V, E), find for each pair of vertices v, w _V whether_
_∈_
there is a path from v to w.

Solution: make the cost of all edges 1, and run
Floyd’s algorithm. If on termination A[i, j] =,
_̸_ _∞_
then there is a path from i to j.

A cleaner solution: use Boolean values instead.

|0|10|00|30|100|Col6|
|---|---|---|---|---|---|
|00|0|50|00|00||
|00|00|0|00|10||
|00|00|20|0|60||
|00|00|00|00|0||

|0|10|00|30|100|
|---|---|---|---|---|
|00|0|50|00|00|
|00|00|0|00|10|
|00|00|20|0|60|
|00|00|00|00|0|

|0|10|60|30|70|
|---|---|---|---|---|
|00|0|50|00|60|
|00|00|0|00|10|
|00|00|20|0|30|
|00|00|00|00|0|

|0|10|60|30|100|
|---|---|---|---|---|
|00|0|50|00|00|
|00|00|0|00|10|
|00|00|20|0|60|
|00|00|00|00|0|

|0|10|50|30|60|
|---|---|---|---|---|
|00|0|50|00|60|
|00|00|0|00|10|
|00|00|20|0|30|
|00|00|00|00|0|

|0|10|50|30|60|
|---|---|---|---|---|
|00|0|50|00|60|
|00|00|0|00|10|
|00|00|20|0|30|
|00|00|00|00|0|


3


-----

**for i := 1 to n do**
**for j := 1 to n do**
_A[i, j] := (i, j)_ _E_
_∈_
_A[i, i] := true_
**for k := 1 to n do**
**for i := 1 to n do**
**for j := 1 to n do**
_A[i, j] := A[i, j] or (A[i, k] and A[k, j])_

**Finding Solutions Using Dynamic**
**Programming**

We have seen some examples of finding the cost of
the “best” solution to some interesting problems:

cheapest order of multiplying n rectangular ma
_•_
trices
min cost binary search tree

_•_
all pairs shortest path

_•_

We have also seen some examples of finding whether
solutions exist to some interesting problems:

the knapsack problem

_•_
transitive closure

_•_

What about actually finding the solutions?

We saw how to do it with the all pairs shortest path
problem.

The principle is the same every time:

In the inner loop there is some kind of “deci
_•_
sion” taken.
Record the result of this decision in another ta
_•_
ble.
Write a divide-and-conquer algorithm to con
_•_
struct the solution from the information in the
table.

**Matrix Product**

As another example, consider the matrix product
algorithm.

**for i := 1 to n do m[i, i] := 0**
**for d := 1 to n** 1 do
_−_
**for i := 1 to n** _d do_
_−_
_j := i + d_
_m[i, j] := mini≤k<j(m[i, k] + m[k + 1, j]_
+ri−1rkrj)


In more detail:

**for i := 1 to n do m[i, i] := 0**
**for d := 1 to n** 1 do
_−_
**for i := 1 to n** _d do_
_−_
_j := i + d_
_m[i, j] := m[i, i] + m[i + 1, j] + ri−1rirj_
**for k := i + 1 to j** 1 do
_−_
**if m[i, k] + m[k + 1, j] + ri−1rkrj < m[i, j]**
**then**
_m[i, j] := m[i, k] + m[k + 1, j] + ri−1rkrj_

Add the extra lines:

**for i := 1 to n do m[i, i] := 0**
**for d := 1 to n** 1 do
_−_
**for i := 1 to n** _d do_
_−_
_j := i + d_
_m[i, j] := m[i, i] + m[i + 1, j] + ri−1rirj_

_P_ [i, j] := i

**for k := i + 1 to j** 1 do
_−_
**if m[i, k] + m[k + 1, j] + ri−1rkrj < m[i, j]**
**then**
_m[i, j] := m[i, k] + m[k + 1, j] + ri−1rkrj_

_P_ [i, j] := k

**Example**

_r0 = 10, r1 = 20, r2 = 50, r3 = 1, r4 = 100._

_m[1, 2]_ = min
1≤k<2[(][m][[1][, k][] +][ m][[][k][ + 1][,][ 2] +][ r][0][r][k][r][2][)]

= _r0r1r2 = 10000_
_m[2, 3]_ = _r1r2r3 = 1000_
_m[3, 4]_ = _r2r3r4 = 5000_

###### 0 10K 0 1

 0 1K 0 2

 0 5K 0 3

 m 0 P 0

_m[1, 3]_

|0|10K|Col3|Col4|
|---|---|---|---|
||0|1K||
|||0|5K|
|m|||0|

|0|1|Col3|Col4|
|---|---|---|---|
||0|2||
|||0|3|
|P|||0|


4


-----

= min
1≤k<3[(][m][[1][, k][] +][ m][[][k][ + 1][,][ 3] +][ r][0][r][k][r][3][)]

= min(m[1, 1] + m[2, 3] + r0r1r3,
_m[1, 2] + m[3, 3] + r0r2r3)_
= min(0 + 1000 + 200, 10000 + 0 + 500)
= 1200

###### 0 10K 1.2K 0 1 1

 0 1K 0 2

 0 5K 0 3

 m 0 P 0

_m[2, 4]_
= min
2≤k<4[(][m][[2][, k][] +][ m][[][k][ + 1][,][ 4] +][ r][1][r][k][r][4][)]

= min(m[2, 2] + m[3, 4] + r1r2r4,

_m[2, 3] + m[4, 4] + r1r3r4)_
= min(0 + 5000 + 100000, 1000 + 0 + 2000)
= 3000

###### 0 10K 1.2K 0 1 1

 0 1K 3K 0 2 3

 0 5K 0 3

 m 0 P 0

_m[1, 4]_
= min
1≤k<4[(][m][[1][, k][] +][ m][[][k][ + 1][,][ 4] +][ r][0][r][k][r][4][)]

= min(m[1, 1] + m[2, 4] + r0r1r4,
_m[1, 2] + m[3, 4] + r0r2r4,_
_m[1, 3] + m[4, 4] + r0r3r4)_
= min(0 + 3000 + 20000,
1000 + 5000 + 50000,
1200 + 0 + 1000)
= 2200


###### 0 10K 1.2K2.2K 0 1 1 3

 0 1K 3K 0 2 3

 0 5K 0 3

 m 0 P 0

**Performing the Product**

Suppose we have a function matmultiply that multiplies two rectangular matrices and returns the result.

**function product(i, j)**
**comment returns Mi · Mi+1 · · · Mj**
**if i = j then return(Mi) else**
_k := P_ [i, j]
**return(matmultiply(product(i, k),**
product(k + 1, j)))

Main body: product(1, n).

**Parenthesizing the Product**

Suppose we want to output the parenthesization instead of performing it. Use arrays L, R:

_L[i] stores the number of left parentheses in_

_•_
front of matrix Mi
_R[i] stores the number of right parentheses be-_

_•_
hind matrix Mi.

**for i := 1 to n do**
_L[i] := 0; R[i] := 0_
product(1, n)
**for i := 1 to n do**
**for j := 1 to L[i] do print(“(”)**
print(“Mi”)
**for j := 1 to R[i] do print(“)”)**

**procedure product(i, j)**
**if i < j** 1 then
_−_
_k := P_ [i, j]
**if k > i then**
increment L[i] and R[k]
**if k + 1 < j then**
increment L[k + 1] and R[j]
product(i,k)
product(k+1,j)

|0|10K|1.2K|2.2K|
|---|---|---|---|
||0|1K|3K|
|||0|5K|
|m|||0|

|0|1|1|3|
|---|---|---|---|
||0|2|3|
|||0|3|
|P|||0|

|0|10K|1.2K|Col4|
|---|---|---|---|
||0|1K||
|||0|5K|
|m|||0|

|0|1|1|Col4|
|---|---|---|---|
||0|2||
|||0|3|
|P|||0|

|0|10K|1.2K|Col4|
|---|---|---|---|
||0|1K|3K|
|||0|5K|
|m|||0|

|0|1|1|Col4|
|---|---|---|---|
||0|2|3|
|||0|3|
|P|||0|


5


-----

**Example**

|0|0|0|0|
|---|---|---|---|


product(1,4) 1 2 3 4

R 0 0 0 0

k:=P[1,4]=3

Increment L[1], R[3] 1 2 3 4

product(1,3) L 1 0 0 0

1 2 3 4

k:=P[1,3]=1

R 0 0 1 0

Increment L[2], R[3]

product(1,1)

1 2 3 4

L 1 1 0 0

product(2,3)

1 2 3 4

R 0 0 2 0

product(4,4)

###### (M1 M( 2 M3)) M4

**Assigned Reading**

CLR Section 16.1, 26.2.

POA Section 8.4, 8.6.

|0|0|0|0|
|---|---|---|---|

|1|0|0|0|
|---|---|---|---|

|0|0|1|0|
|---|---|---|---|

|1|1|0|0|
|---|---|---|---|

|0|0|2|0|
|---|---|---|---|

|1 2 3 4 L 0 0 0 0 product(1,4) 1 2 3 4 R 0 0 0 0 k:=P[1,4]=3 Increment L[1], R[3] 1 2 3 4 product(1,3) L 1 0 0 0 1 2 3 4 k:=P[1,3]=1 R 0 0 1 0 Increment L[2], R[3] product(1,1) 1 2 3 4 L 1 1 0 0 product(2,3) 1 2 3 4 R 0 0 2 0 product(4,4) (M (M M 3)) M 1 2 4|1 2 3 4 L 0 0 0 0 1 2 3 4 R 0 0 0 0|
|---|---|
|k:=P[1,4]=3 Increment L[1], R[3] product(1,3) k:=P[1,3]=1 Increment L[2], R[3] product(1,1) product(2,3) product(4,4)||
||1 2 3 4 L 1 0 0 0 1 2 3 4 R 0 0 1 0|
||1 2 3 4 L 1 1 0 0 1 2 3 4 R 0 0 2 0|


6


-----

**Summary**

Greedy algorithms for


###### Algorithms Course Notes Greedy Algorithms 1

 Ian Parberry[∗]

 Fall 2001

There are 3! = 6 possible orders.


Optimal tape storage

_•_
Continuous knapsack problem

_•_

**Greedy Algorithms**

Start with a solution to a small subproblem

_•_
Build up to a solution to the whole problem

_•_
Make choices that look good in the short term

_•_

Disadvantage: Greedy algorithms don’t always
work. (Short term solutions can be disastrous in
the long term.) Hard to prove correct.

Advantage: Greedy algorithms work fast when they
work. Simple algorithms, easy to implement.

**Optimal Tape Storage**

Given n files of length

_m1, m2, . . ., mn_

find which order is the best to store them on a tape,
assuming

Each retrieval starts with the tape rewound.

_•_
Each retrieval takes time equal to the length of

_•_
the preceding files in the tape plus the length of
the retrieved file.
All files are to be retrieved.

_•_

**Example**

_n = 3; m1 = 5, m2 = 10, m3 = 3._

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


1,2,3: (5+10+3)+(5+10)+5 =38
1,3,2: (5+3+10)+(5+3) +5 =31
2,1,3: (10+5+3)+(10+5)+10=43
2,3,1: (10+3+5)+(10+3)+10=41
3,1,2: (3+5+10)+(3+5) +3 =29
3,2,1: (3+10+5)+(3+10)+3 =34

The best order is 3, 1, 2.

**The Greedy Solution**

make tape empty
**for i := 1 to n do**
grab the next shortest file
put it next on tape

The algorithm takes the best short term choice without checking to see whether it is the best long term
decision.

Is this wise?

**Correctness**

Suppose we have files f1, f2, . . ., fn, of lengths
_m1, m2, . . ., mn respectively. Let i1, i2, . . ., in be a_
permutation of 1, 2, . . ., n.

Suppose we store the files in order

_fi1_ _, fi2, . . ., fin_ _._

What does this cost us?

To retrieve the kth file on the tape, fik, costs

_k_
� _mij_

_j=1_


1


-----

The cost of permutation Π[′] is


Therefore, the cost of retrieving them all is


_C(Π[′]) =_


_j−1_
�(n − _k + 1)mik_ +

_k=1_


_n_
�

_k=1_

To see this:


_k_
� _mij =_

_j=1_


_n_
�(n − _k + 1)mik_

_k=1_


_fi1:_ _mi1_
_fi2:_ _mi1+mi2_
_fi3:_ _mi1+mi2+mi3_
...
_fin−1:_ _mi1+mi2+mi3+. . . +min−1_
_fin_ : _mi1+mi2+mi3+. . . +min−1+min_

Total is

_nmi1 + (n −_ 1)mi2 + (n − 2)mi3 + . . .

_n_

+ 2min−1 + min = �(n − _k + 1)mik_

_k=1_


The greedy algorithm picks files fi in nondecreasing
order of their size mi. It remains to prove that this
is the minimum cost permutation.

Claim: Any permutation in nondecreasing order of
_mi’s has minimum cost._

Proof: Let Π = (i1, i2, . . ., in) be a permutation of
1, 2, . . ., n that is not in nondecreasing order of mi’s.
We will prove that it cannot have minimum cost.

Since mi1, mi2, . . ., min is not in nondecreasing order, there must exist 1 ≤ _j < n such that mij >_
_mij+1._

Let Π[′] be permutation Π with ij and ij+1 swapped.

The cost of permutation Π is


(n − _j + 1)mij+1 + (n −_ _j)mij +_

_n_
� (n − _k + 1)mik_

_k=j+2_

Hence,

_C(Π) −_ _C(Π[′])_ = (n − _j + 1)(mij −_ _mij+1)_
+ (n − _j)(mij+1 −_ _mij_ )
= _mij_ _mij+1_
_−_
_>_ 0 (by definition of j)

Therefore, C(Π[′]) < C(Π), and so Π cannot be a
permutation of minimum cost. This is true of any Π
that is not in nondecreasing order of mi’s.

Therefore the minimum cost permutation must be
in nondecreasing order of mi’s.

**Analysis**

_O(n log n) for sorting_

_O(n) for the rest_

**The Continuous Knapsack Problem**

This is similar to the knapsack problem met earlier.

_• given n objects A1, A2, . . ., An_
given a knapsack of length S

_•_

_• Ai has length si_

_• Ai has weight wi_

_• an xi-fraction of Ai, where 0 ≤_ _xi ≤_ 1 has
length xisi and weight xiwi

Fill the knapsack as full as possible using fractional
parts of the objects, so that the weight is minimized.

**Example**

_S = 20._


_C(Π) =_


_n_
�(n − _k + 1)mik_

_k=1_


=


_j−1_
�(n − _k + 1)mik +_

_k=1_

(n − _j + 1)mij + (n −_ _j)mij+1 +_

_n_
� (n − _k + 1)mik_

_k=j+2_


2


-----

_s1 = 18, s2 = 10, s3 = 15._

_w1 = 25, w2 = 15, w3 = 24._

(x1, x2, x3) �3i=1 _[x][i][s][i]_ �3i=1 _[x][i][w][i]_
(1,1/5,0) 20 28
(1,0,2/15) 20 28.2
(0,1,2/3) 20 31
(0,1/2,1) 20 31.5
...

The first one is the best so far. But is it the best
overall?

**The Greedy Solution**

Define the density of object Ai to be wi/si. Use
as much of low density objects as possible. That
is, process each in increasing order of density. If
the whole thing fits, use all of it. If not, fill the
remaining space with a fraction of the current object,
and discard the rest.

First, sort the objects in nondecreasing density, so
that wi/si ≤ _wi+1/si+1 for 1 ≤_ _i < n._

Then, do the following:

_s := S; i := 1_
**while si ≤** _s do_
_xi := 1_
_s := s −_ _si_
_i := i + 1_
_xi := s/si_
**for j := i + 1 to n do**
_xj := 0_

|Col1|Col2|
|---|---|
|10 5 0|15 20 25 30|

|Col1|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Col10|Col11|Col12|Col13|Col14|Col15|Col16|Col17|Col18|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|||||||||||||||||||

|1 10|5 20|
|---|---|
|5 25 0 30||

|Col1|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Col10|Col11|Col12|Col13|Col14|Col15|Col16|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|15 10 20 5 25 0 30||||||||||||||||

|1 10 5|5 20 25|
|---|---|
|0 30||

|Col1|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Col10|Col11|Col12|Col13|Col14|Col15|Col16|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|15 10 20 5 25 0 30||||||||||||||||

|1 10|5 20|
|---|---|
|5 25 0 30||


Claim: The greedy algorithm gives a solution of minimal weight.

(Note: a solution of minimal weight. There may be
many solutions of minimal weight.)

Proof: Let X = (x1, x2, . . ., xn) be the solution generated by the greedy algorithm.

If all the xi are 1, then the solution is clearly optimal
(it is the only solution).

Otherwise, let j be the smallest number such that


###### A 1

 A 2

 A 3

 A 1 A 2 A 3

 A 2 A 3

 A 2 A 3


**Example**

density = 25/18=1.4

[15 ]20
25
30

density =15/10=1.5

[15 ]20
25
30

density =24/15=1.6

[15 ]20
25
30

10 [15 ]20
5 25
0 30

10 [15 ]20
5 25
0 30

10 [15 ]20
5 25
0 30

**Correctness**


3


-----

_n_
� _yisi_

_i=k+1_


_xj ̸= 1. From the algorithm,_

_xi = 1_ for 1 ≤ _i < j_
0 ≤ _xj < 1_
_xi = 0_ for _j < i ≤_ _n_

Therefore,
_j_
� _xisi = S._

_i=1_

Let Y = (y1, y2, . . ., yn) be a solution of minimal
weight. We will prove that X must have the same
weight as Y, and hence has minimal weight.

If X = Y, we are done. Otherwise, let k be the least
number such that xk ̸= yk.

**Proof Stategy**

Transform Y into X, maintaining weight.

We will see how to transform Y into Z, which looks
“more like” X.


_S_ =

=

=


=

=

=


_j_
� _xisi + (yk_ _xk)sk +_

_−_
_i=1_


_k−1_
� _xisi + yksk +_

_i=1_


_k_
� _xisi + (yk_ _xk)sk +_

_−_
_i=1_


_n_
� _yisi_

_i=k+1_


_n_
� _yisi_

_i=k+1_


= _S + (yk_ _xk)sk +_
_−_

_>_ _S_


_n_
� _yisi_

_i=k+1_


which contradicts the fact that Y is a solution.
Therefore, yk < xk.

Case 3: k > j. Then xk = 0 and yk > 0, and so


_n_
� _yisi_

_i=j+1_

_n_
� _yisi_

_i=j+1_


_n_
� _yisi_

_i=1_

_j_
� _yisi +_

_i=1_

_j_
� _xisi +_

_i=1_


###### Y=

 Z=

 X=


###### ... ...
 x 1 x 2 x k-1 y k y k+1 y n

 ... ...
 x 1 x 2 x k-1 x k z k+1 z n


###### x 1 x 2 ... x k-1 x k x k+1 ... x n

**Digression**


_n_
� _yisi_

_i=j+1_


= _S +_

_>_ _S_


It must be the case that yk < xk. To see this, consider the three possible cases:

Case 1: k < j. Then xk = 1. Therefore, since
_xk_ = yk, yk must be smaller than xk.
_̸_

Case 2: k = j. By the definition of k, xk ̸= yk. If
_yk > xk,_


This is not possible, hence Case 3 can never happen.

In the other 2 cases, yk < xk as claimed.

**Back to the Proof**

Now suppose we increase yk to xk, and decrease as
many of yk+1, . . ., yn as necessary to make the total
length remain at S. Call this new solution Z =
(z1, z2, . . ., zn).

Therefore,

1. (zk _yk)sk > 0_
_−_

2. [�]i[n]=k+1[(][z][i][ −] _[y][i][)][s][i][ <][ 0]_


_n_
� _yisi_

_i=k+1_


_S_ =

=


_n_
� _yisi_

_i=1_

_k−1_
� _yisi + yksk +_

_i=1_


4


-----

3. (zk − _yk)sk +_ [�]i[n]=k+1[(][z][i][ −] _[y][i][)][s][i][ = 0]_

Then,

_n_
� _ziwi_

_i=1_


_n_
� _ziwi_

_i=k+1_

_n_
� _ziwi_

_i=k+1_

_n_
� _yiwi +_

_i=k+1_


=

=

=

=

=

_≤_

=

=


_k−1_
� _ziwi + zkwk +_

_i=1_

_k−1_
� _yiwi + zkwk +_

_i=1_

_n_
� _yiwi −_ _ykwk −_

_i=1_


_n_
� _yiwi (by (3))_

_i=1_


_n_

_zkwk +_ � _ziwi_

_i=k+1_


_n_
� _yiwi + (zk_ _yk)wk +_

_−_
_i=1_


_n_
� (zi − _yi)wi_

_i=k+1_


“more like” X — the first k entries of Z are the same
as X.

Repeating this procedure transforms Y into X and
maintains the same weight. Therefore X has minimal weight.

**Analysis**

_O(n log n) for sorting_

_O(n) for the rest_

**Assigned Reading**

CLR Section 17.2.

POA Section 9.1.


_n_
� _yiwi + (zk_ _yk)skwk/sk +_

_−_
_i=1_

_n_
� (zi − _yi)siwi/si_

_i=k+1_


_n_
� _yiwi + (zk_ _yk)skwk/sk +_

_−_
_i=1_

_n_
� (zi _yi)siwk/sk (by (2) & density)_

_−_
_i=k+1_

_n_
� _yiwi +_

_i=1_


�


(zk _yk)sk +_
_−_


_wk/sk_


_n_
� (zi − _yi)si_

_i=k+1_


�


Now, since Y is a minimal weight solution,


_n_
� _ziwi ̸<_

_i=1_


_n_
� _yiwi._

_i=1_


Hence Y and Z have the same weight. But Z looks


5


-----

###### Algorithms Course Notes Greedy Algorithms 2

 Ian Parberry[∗]

 Fall 2001

**Summary** If w _S, then D[w] is the cost of the shortest_

_•_ _̸∈_
internal path to w.
If w _S, then D[w] is the cost of the shortest_

A greedy algorithm for _•_ _∈_

path from s to w, δ(s, w).

The single source shortest path problem (Dijk
_•_
stra’s algorithm)

**The Frontier**

**Single Source Shortest Paths**

A vertex w is on the frontier if w _S, and there is_
_̸∈_
a vertex u _S such that (u, w)_ _E._
_∈_ _∈_

Given a labelled, directed graph G = (V, E) and
a distinguished vertex s _V, find for each vertex_
_∈_
_w_ _V a shortest (i.e. least cost) path from s to w._
_∈_

###### Frontier

More precisely, construct a data structure that allows us to compute the vertices on a shortest path
from s to w for any w _V in time linear in the_
_∈_
length of that path.

###### s

Vertex s is called the source.

###### S

Let δ(v, w) denote the cost of the shortest path from _G_
_v to w._

Let C[v, w] be the cost of the edge from v to w (
_∞_
if it doesn’t exist, 0 if v = w).

**Dijkstra’s Algorithm: Overview** All internal paths end at vertices in S or the fron
tier.

Maintain a set S of vertices whose minimum distance
from the source is known. **Adding a Vertex to S**

Initially, S = _s_ .

_•_ _{_ _}_

Which vertex do we add to S? The vertex w _V_ _S_

Keep adding vertices to S. _∈_ _−_

_•_ with smallest D value. Since the D value of vertices
Eventually, S = V .

_•_ not on the frontier or in S is infinite, w will be on

the frontier.

A internal path is a path from s with all internal
vertices in S. Claim: D[w] = δ(s, w).

Maintain an array D with: That is, we are claiming that the shortest internal

_∗Copyright c⃝_ Ian Parberry, 1992–2001. path from s to w is a shortest path from s to w.

1


-----

Consider the shortest path from s to w. Let x be
the first frontier vertex it meets.

###### w

 s x

 S

Then

_δ(s, w)_ = _δ(s, x) + δ(x, w)_
= _D[x] + δ(x, w)_
_D[w] + δ(x, w) (By defn. of w)_
_≥_
_D[w]_
_≥_

But by the definition of δ, δ(s, w) _D[w]._
_≤_

Hence, D[w] = δ(s, w) as claimed.

**Observation**

Claim: If u is placed into S before v, then δ(s, u)
_≤_
_δ(s, v)._

Proof: Proof by induction on the number of vertices already in S when v is put in. The hypothesis
is certainly true when _S_ = 1. Now suppose it is
_|_ _|_
true when _S_ _< n, and consider what happens when_
_|_ _|_
_S_ = n.
_|_ _|_

Consider what happens at the time that v is put into
_S. Let x be the last internal vertex on the shortest_
path to v.

###### v
 x

 s
 u
 S

Case 1: x was put into S before u.

Go back to the time that u was put into S.


Since x was already in S, v was on the frontier. But
since u was chosen to be put into S before v, it
must have been the case that D[u] _D[v]. Since_
_≤_
_u was chosen to be put into S, D[u] = δ(s, u). By_
the definition of x, and because x was put into S
before u, D[v] = δ(s, v). Therefore, δ(s, u) = D[u]
_≤_
_D[v] = δ(s, v)._

Case 2: x was put into S after u.

Since x was put into S before v, at the time x was
put into S, _S_ _< n._ Therefore, by the induction
_|_ _|_
hypothesis, δ(s, u) _δ(s, x). Therefore, by the defi-_
_≤_
nition of x, δ(s, u) _δ(s, x)_ _δ(s, v)._
_≤_ _≤_

**Updating the Cost Array**

The D value of frontier vertices may change, since
there may be new internal paths containing w.

There are 2 ways that this can happen. Either,

_w is the last internal vertex on a new internal_

_•_
path, or
_w is some other internal vertex on a new internal_

_•_
path

If w is the last internal vertex:


2


-----

###### Old internal path of cost


###### D[x]


###### New internal path of cost


###### D[w]+C[w,x]


If w is not the last internal vertex:

###### Was a non-internal path

 w

 s
 x
 y
 S

 Becomes an internal path

 w

 s
 x
 y
 S

This cannot be shorter than any other path from s
to x.

Vertex y was put into S before w. Therefore, by the
earlier Observation, δ(s, y) _δ(s, w)._
_≤_

That is, it is cheaper to go from s to y directly than
it is to go through w. So, this type of path can be
ignored.


The D value of vertices outside the frontier may
change

###### w y

 s

 D[y]=OO

 w y

 s

 D[y]=D[w]+C[w,y]

The D value of vertices in S do not change (they are
already the shortest).

Therefore, for every vertex v _V, when w is moved_
_∈_
from the frontier to S,

_D[v] := min_ _D[v], D[w] + C[w, v]_
_{_ _}_

**Dijkstra’s Algorithm**

1. _S :=_ _s_
_{_ _}_
2. **for each v** _V do_
_∈_
3. _D[v] := C[s, v]_
4. **for i := 1 to n** 1 do
_−_
5. choose w _V_ _S with smallest D[w]_
_∈_ _−_
6. _S := S_ _w_
_∪{_ _}_
7. **for each vertex v** _V do_
_∈_
8. _D[v] := min_ _D[v], D[w] + C[w, v]_
_{_ _}_

**First Implementation**

Store S as a bit vector.

Line 1: initialize the bit vector, O(n) time.

_•_
Lines 2–3: n iterations of O(1) time per itera
_•_
tion, total of O(n) time
Line 4: n 1 iterations

_•_ _−_
Line 5: a linear search, O(n) time.

_•_
Line 6: O(1) time

_•_


3


-----

Lines 7–8: n iterations of O(1) time per itera
_•_
tion, total of O(n) time
Lines 4–8: n 1 iterations, O(n) time per iter
_•_ _−_
ation

Total time O(n[2]).

**Second Implementation**

Instead of storing S, store S[′] = V _S. Implement_
_−_
_S[′]_ as a heap, indexed on D value.

Line 8 only needs to be done for those v such that
(w, v) _E. Provide a list for each w_ _V of those_
_∈_ _∈_
vertices v such that (w, v) _E (an adjacency list)._
_∈_

1–3. makenull(S[′])
**for each v** _V except s do_
_∈_
_D[v] := C[s, v]_
insert(v, S[′])
4. **for i := 1 to n** 1 do
_−_
5–6. _w := deletemin(S[′])_
7. **for each v such that (w, v)** _E do_
_∈_
8. _D[v] := min_ _D[v], D[w] + C[w, v]_
_{_ _}_
move v up the heap

**Analysis**

Line 8: O(log n) to adjust the heap

_•_
Lines 7–8: O(n log n)

_•_
Lines 5–6: O(log n)

_•_
Lines 4–8: O(n[2] log n)

_•_
Lines 1–3: O(n log n)

_•_

Total: O(n[2] log n)

But, line 8 is executed exactly once for each edge:
each edge (u, v) _E is used once when u is placed_
_∈_
in S. Therefore, the true complexity is O(e log n):

Lines 1–3: O(n log n)

_•_
Lines 4–6: O(n log n)

_•_
Lines 4,8: O(e log n)

_•_

**Dense and Sparse Graphs**

Which is best? They match when e log n = Θ(n[2]),
that is, e = Θ(n[2]/ log n).


use first implementation on dense graphs (e

_•_
is larger than n[2]/ log n, technically, _e_ =
_ω(n[2]/ log n))_
use second implementation on sparse graphs

_•_
(e is smaller than n[2]/ log n, technically, e =
_o(n[2]/ log n))_

The second implementation can be improved by implementing the priority queue using Fibonacci heaps.
Run time is O(n log n + e).

**Computing the Shortest Paths**

We have only computed the costs of the shortest
paths. What about constructing them?

Keep an array P, with P [v] the predecessor of v in
the shortest internal path.

Every time D[v] is modified in line 8, set P [v] to w.

1. _S :=_ _s_
_{_ _}_
2. **for each v** _V do_
_∈_
3. _D[v] := C[s, v]_

**if (s, v)** _E then P_ [v] := s else P [v] := 0
_∈_

4. **for i := 1 to n** 1 do
_−_
5. choose w _V_ _S with smallest D[w]_
_∈_ _−_
6. _S := S_ _w_
_∪{_ _}_
7. **for each vertex v** _V_ _S do_
_∈_ _−_
8. **if D[w] + C[w, v] < D[v] then**
_D[v] := D[w] + C[w, v]_

_P_ [v] := w

**Reconstructing the Shortest Paths**

For each vertex v, we know that P [v] is its predecessor on the shortest path from s to v. Therefore, the
shortest path from s to v is:

The shortest path from s to P [v], and

_•_
the edge (P [v], v).

_•_

To print the list of vertices on the shortest path from
_s to v, use divide-and-conquer:_

**procedure path(s, v)**
**if v** = s then path(s, P [v])
_̸_
print(v)

To use, do the following:


4


-----

**if P** [v] = 0 then path(s, v)
_̸_

Correctness: Proof by induction.

Analysis: linear in the length of the path; proof by
induction.

**Example**

###### 1

10 100

###### 2 30 5 Dark shading: S

Light shading: frontier

50 10
60

###### 3 4

20

Source is vertex 1.

2 3 4 5


2 3 4 5

_D_ 10 50 30 90

_P_ 1 4 1 4

###### 1

10 100

###### 2 30 5

50 10
60

###### 3 4

20

2 3 4 5

_D_ 10 50 30 60

_P_ 1 4 1 3

###### 1

10 100

###### 2 30 5

50 10
60

###### 3 4

20

2 3 4 5

_D_ 10 50 30 60

_P_ 1 4 1 3

To reconstruct the shortest paths from the P array:

_P_ [2] _P_ [3] _P_ [4] _P_ [5]

1 4 1 3

Vertex Path Cost

2: 1 2 10
3: 1 4 3 20 + 30 = 50
4: 1 4 30
5: 1 4 3 5 10 + 20 + 30 = 60

The costs agree with the D array.

The same example was used for the all pairs shortest
path problem.

|10|50|30|90|
|---|---|---|---|

|1|4|1|4|
|---|---|---|---|

|10|50|30|60|
|---|---|---|---|

|1|4|1|3|
|---|---|---|---|


Dark shading: S
Light shading: entries
that have changed

###### 1

100

30 5

10

60

###### 4

20

2 3 4 5


_D_


10 00 30 100

|10|00|30|10|
|---|---|---|---|


_P_ 1 0 1 1

###### 2

50

_D_

|1|0|1|1|
|---|---|---|---|

|10|50|30|60|
|---|---|---|---|

|1|4|1|3|
|---|---|---|---|

|10|60|30|100|
|---|---|---|---|


_P_ 1 2 1 1

|1|2|1|1|
|---|---|---|---|


5


-----

**Assigned Reading**

CLR Section 25.1, 25.2.


6


-----

**Summary**

Greedy algorithms for


###### Algorithms Course Notes Greedy Algorithms 3

 Ian Parberry[∗]

 Fall 2001

Set 2 is {2}


Set 11 is {9,10,11,12}


The union-find problem

_•_
Min cost spanning trees (Prim’s algorithm and

_•_
Kruskal’s algorithm)

**The Union-Find Problem**

Given a set 1, 2, . . ., n initially partitioned into n
_{_ _}_
disjoint subsets, one member per subset, we want to
perform the following operations:

find(x): return the name of the subset that x is

_•_
in
union(x, y): combine the two subsets that x and

_•_
_y are in_

What do we use for the “name” of a subset? Use
one of its members.

**A Data Structure for Union-Find**

Use a tree:

implement with pointers and records

_•_
the set elements are stored in the nodes

_•_
each child has a pointer to its parent

_•_
there is an array P [1..n] with P [i] pointing to

_•_
the node containing i

_∗Copyright c⃝_ Ian Parberry, 1992–2001.

|9|Col2|
|---|---|

|2|Col2|
|---|---|

|1|Col2|
|---|---|

|11 et 2 is {2} 9 10 2 7 1 12 4 3 8 6 5|Col2|Col3|
|---|---|---|
||||
||||
|3|||

|8|Col2|
|---|---|


Set 7 is {4,5,7}
Set 1 is {1,3,6,8}

###### 11

 9 10
 2 7
 1 12
 4

 3 8 6 5

 P
 1 2 3 4 5 6 7 8 9 10 11 12

**Implementing the Operations**

find(x): Follow the chain of pointers starting at

_•_
_P_ [x] to the root of the tree containing x. Return
the set element stored there.
union(x, y): Follow the chains of pointers start
_•_
ing at P [x] and P [y] to the roots of the trees
containing x and y, respectively. Make the root
of one tree point to the root of the other.

|9|Col2|
|---|---|

|2|Col2|
|---|---|

|1|Col2|
|---|---|

|3|Col2|
|---|---|

|8|Col2|
|---|---|

|11 9 10 2 7 1 12 4 3 8 6 5 P|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Col10|Col11|
|---|---|---|---|---|---|---|---|---|---|---|
||||||||||||


1


-----

**Example**

union(4,12): 11

###### 9 10
 2
 7
 1 12
 4

 3 8 6 5

 P 1 2 3 4 5 6 7 8 9 10 11 12

**Analysis**

Running time proportional to number of layers in
the tree. But this may be Ω(n) for an n-node tree.

After After After
Initially
union(1,2) union(1,3) union(1,n)

###### 1 1 1 1

 2 2 2 2

 3 3 3 3

 n n n n

**Improvement**

Make the root of the smaller tree point to the root
of the bigger tree.

|1|Col2|
|---|---|

|1|Col2|
|---|---|

|1|Col2|
|---|---|

|1|Col2|
|---|---|

|1|Col2|
|---|---|

|11|Col2|
|---|---|

|2|Col2|
|---|---|

|2|Col2|
|---|---|

|2|Col2|
|---|---|

|2|Col2|
|---|---|

|2|Col2|
|---|---|

|9|Col2|
|---|---|

|10|Col2|
|---|---|

|3|Col2|
|---|---|

|3|Col2|
|---|---|

|3|Col2|
|---|---|

|3|Col2|
|---|---|

|3|Col2|
|---|---|

|2|Col2|
|---|---|

|4|Col2|
|---|---|

|4|Col2|
|---|---|

|4|Col2|
|---|---|

|4|Col2|
|---|---|

|4|Col2|
|---|---|

|1|Col2|
|---|---|

|4|Col2|
|---|---|

|5|Col2|
|---|---|

|5|Col2|
|---|---|

|5|Col2|
|---|---|

|5|Col2|
|---|---|

|5|Col2|
|---|---|

|Initially|After union(1,2)|After union(1,3)|After union(4,5)|After union(2,5)|
|---|---|---|---|---|
|1 2 3 4 5|1 2 3 4 5|1 2 3 4 5|1 2 3 4 5|1 2 3 4 5|


5 nodes, 3 layers

**More Analysis**

Claim: If this algorithm is used, every tree with n
nodes has at most log n + 1 layers.
_⌊_ _⌋_

Proof: Proof by induction on n, the number of nodes
in the tree. The claim is clearly true for a tree with
1 node. Now suppose the claim is true for trees
with less than n nodes, and consider a tree T with
_n nodes._

_T was made by unioning together two trees with less_
than n nodes each.

Suppose the two trees have m and n _m nodes each,_
_−_
where m _n/2._
_≤_

_T_ _T_
1 2

_m_ _m_ _n-m_
_n-m_

Then, by the induction hypothesis, T has

max{depth(T1) + 1, depth(T2)}
= max log m + 2, log(n _m)_ + 1
_{⌊_ _⌋_ _⌊_ _−_ _⌋_ _}_
max log n/2 + 2, log n + 1
_≤_ _{⌊_ _⌋_ _⌊_ _⌋_ _}_
= log n + 1
_⌊_ _⌋_

layers.

Implementation detail: store count of nodes in root
of each tree. Update during union in O(1) extra
time.

Conclusion: union and find operations take time
_O(log n)._

|3|Col2|
|---|---|

|8|Col2|
|---|---|

|6|Col2|
|---|---|

|5|Col2|
|---|---|

|union(4,12): 11 9 10 2 7 1 12 4 3 8 6 5|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Col10|Col11|Col12|Col13|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
||||||||||||||

|1|Col2|
|---|---|

|1|Col2|
|---|---|

|1|Col2|
|---|---|

|1|Col2|
|---|---|

|2|Col2|
|---|---|

|2|Col2|
|---|---|

|2|Col2|
|---|---|

|2|Col2|
|---|---|

|3|Col2|
|---|---|

|3|Col2|
|---|---|

|3|Col2|
|---|---|

|3|Col2|
|---|---|

|n|Col2|
|---|---|

|n|Col2|
|---|---|

|n|Col2|
|---|---|

|n|Col2|
|---|---|

|Initially|After union(1,2)|After union(1,3)|After union(1,n)|
|---|---|---|---|
|1 2 3 n|1 2 3 n|1 2 3 n|1 2 3 n|


2


-----

It is possible to do better using path compression.
When traversing a path from leaf to root, make all
nodes point to root. Gives better amortized performance.

_O(log n) is good enough for our purposes._

**Spanning Trees**

A graph S = (V, T ) is a spanning tree of an undirected graph G = (V, E) if:

_S is a tree, that is, S is connected and has no_

_•_
cycles
_T_ _E_

_•_ _⊆_

###### 1 2 1 2

 4 7 3 4 7 3

 6 5 6 5

 1 2 1 2

 4 7 3 4 7 3

 6 5 6 5

**Spanning Forests**

A graph S = (V, T ) is a spanning forest of an undirected graph G = (V, E) if:

_S is a forest, that is, S has no cycles_

_•_
_T_ _E_

_•_ _⊆_


**The Muddy City Problem**

The residents of Muddy City are too cheap to pave
their streets. (After all, who likes to pay taxes?)
However, after several years of record rainfall they
are tired of getting muddy feet. They are still too
miserly to pave all of the streets, so they want to
pave only enough streets to ensure that they can
travel from every intersection to every other intersection on a paved route, and they want to spend as
little money as possible doing it. (The residents of
Muddy City don’t mind walking a long way to save
money.)

Solution: Create a graph with a node for each intersection, and an edge for each street. Each edge
is labelled with the cost of paving the corresponding
street. The cheapest solution is a min-cost spanning
tree for the graph.

**An Observation About Trees**

Claim: Let S = (V, T ) be a tree. Then:

1. For every u, v _V, the path between u and v_
_∈_
in S is unique.
2. If any edge (u, v) _T is added to S, then a_
_̸∈_
unique cycle results.

Proof:

1. If there were more than one path between u
and v, then there would be a cycle, which contradicts the definition of a tree.


**Min Cost Spanning Trees**

Given a labelled, undirected, connected graph G,
find a spanning tree for G of minimum cost.

_20_ _20_


_17_


_17_

Cost = 23+1+4+9+3+17=57


3


-----

2. Consider adding an edge (u, v) _T to T_ . There
_̸∈_
must already be a path from u to v (since a tree
is connected). Therefore, adding an edge from
_u to v creates a cycle._

###### u v u v

This cycle must be unique, since if adding (u, v) creates two cycles, then there must have been a cycle
before, which contradicts the definition of a tree.

###### u v

 u v

 u v

**Key Fact**

Here is the principle behind MCST algorithms:

Claim: Let G = (V, E) be a labelled, undirected
graph, and S = (V, T ) a spanning forest for G.

Suppose S is comprised of trees

(V1, T1), (V2, T2), . . ., (Vk, Tk)

for some k _n._
_≤_

Let 1 _i_ _k. Suppose e = (u, v) is the cheapest_
_≤_ _≤_
edge leaving Vi (that is, an edge of lowest cost in
_E −_ _T such that u ∈_ _Vi and v ̸∈_ _Vi)._

Consider all of the spanning trees that contain T .
There is a spanning tree that includes T _e_ that
_∪{_ _}_
is as cheap as any of them.

**Decision Tree**


_Choose e_ _Choose edges_
_other than e_

_For every spanning tree here_
_there is one at least as cheap there_

Proof: Suppose there is a spanning tree that includes
_T but does not include e. Adding e to this spanning_
tree introduces a cycle.

_e_ _e_

###### v v u u

 w
 Vi Vi d x

Therefore, there must be an edge d = (w, x) such
that w ∈ _Vi and x ̸∈_ _Vi._

Let c(e) denote the cost of e and c(d) the cost of d.
By hypothesis, c(e) _c(d)._
_≤_

There is a spanning tree that includes T _e_ that
_∪{_ _}_
is at least as cheap as this tree. Simply add edge e
and delete edge d.

Is the new spanning tree really a spanning tree?

_•_
Yes, because adding e introduces a unique new
cycle, and deleting d removes it.
Is it more expensive? No, because c(e) _c(d)._

_•_ _≤_

**Corollary**

Claim: Let G = (V, E) be a labelled, undirected
graph, and S = (V, T ) a spanning forest for G.

Suppose S is comprised of trees

(V1, T1), (V2, T2), . . ., (Vk, Tk)


4


-----

for some k _n._
_≤_

Let 1 _i_ _k. Suppose e = (u, v) is an edge of_
_≤_ _≤_
lowest cost in E − _T such that u ∈_ _Vi and v ̸∈_ _Vi._

If S can be expanded to a min cost spanning tree,
then so can S[′] = (V, T _e_ ).
_∪{_ _}_

Proof: Suppose S can be expanded to a min cost
spanning tree M . By the previous result, S[′] =
(V, T _e_ ) can be expanded to a spanning tree that
_∪{_ _}_
is at least as cheap as M, that is, a min cost spanning
tree.

**General Algorithm**

1. _F := set of single-vertex trees_
2. **while there is > 1 tree in F do**
3. Pick an arbitrary tree Si = (Vi, Ti) from F
4. _e := min cost edge leaving Vi_
5. Join two trees with e

1. _F :=_
_∅_
**for j := 1 to n do**
_Vj := {j}_
_F := F ∪{(Vj, ∅)}_
2. **while there is > 1 tree in F do**
3. Pick an arbitrary tree Si = (Vi, Ti) from F
4. Let e = (u, v) be a min cost edge,
where u ∈ _Vi, v ∈_ _Vj, j ̸= i_
5. _Vi := Vi ∪_ _Vj; Ti := Ti ∪_ _Tj ∪{e}_
Remove tree (Vj, Tj) from forest F

Many ways of implementing this.

Prim’s algorithm

_•_
Kruskal’s algorithm

_•_

**Prim’s Algorithm: Overview**

Take i = 1 in every iteration of the algorithm.

We need to keep track of:

_• the set of edges in the spanning forest, T1_

_• the set of vertices V1_

_• the edges that lead out of the tree (V1, T1), in_
a data structure that enables us to choose the
one of smallest cost


_Q is a priority queue of edges, ordered on cost._

1. _T1 := ∅; V1 := {1}; Q := empty_
2. **for each w** _V such that (1, w)_ _E do_
_∈_ _∈_
3 insert(Q, (1, w))
4. **while |V1| < n do**
5. _e :=deletemin(Q)_
6. Suppose e = (u, v), where u ∈ _V1_
7. **if v ̸∈** _V1 then_
8. _T1 := T1 ∪{e}_
9. _V1 := V1 ∪{v}_
10. **for each w** _V such that (v, w)_ _E do_
_∈_ _∈_
11. insert(Q, (v, w))

**Data Structures**

For

_E: adjacency list_

_•_

_• V1: linked list_

_• T1: linked list_
_Q: heap_

_•_

**Analysis**

Line 1: O(1)

_•_
Line 3: O(log e)

_•_


_17_


**Example**

_20_

1 2

_15_ _23_ _1_ _15_

_4_

3 4 _36_ 7 3

_9_

_25_

_28_ _16_ _3_

6 5

_17_

1 _20_ 2

_15_ _23_ _1_ _15_

_4_

3 4 _36_ 7 3

_9_

_25_

_28_ _16_ _3_

6 5

_17_

_15_

3

**Prim’s Algorithm**


5


-----

Lines 2–3: O(n log e)

_•_
Line 5: O(log e)

_•_
Line 6: O(1)

_•_
Line 7: O(1)

_•_
Line 8: O(1)

_•_
Line 9: O(1)

_•_
Lines 4–9: O(e log e)

_•_
Line 11: O(log e)

_•_
Lines 4,10–11: O(e log e)

_•_

Total: O(e log e) = O(e log n)

**Kruskal’s Algorithm: Overview**

At every iteration of the algorithm, take e = (u, v)
to be the unused edge of smallest cost, and Vi and
_Vj to be the vertex sets of the forest such that u ∈_ _Vi_
and v ∈ _Vj._

We need to keep track of

the vertices of spanning forest

_•_

_F = {V1, V2, . . ., Vk}_

(note: F is a partition of V )
the set of edges in the spanning forest, T

_•_
the unused edges, in a data structure that en
_•_
ables us to choose the one of smallest cost

**Example**

_20_ _20_ _20_

1 2 1 2 1 2

_23_ _1_ _15_ _23_ _1_ _15_ _23_ _1_ _15_

_4_ _4_ _4_

4 _36_ 7 3 4 _36_ 7 3 4 _36_ 7 3

_9_ _9_ _9_

_25_ _25_ _25_

_28_ _16_ _3_ _28_ _16_ _3_ _28_ _16_ _3_

6 5 6 5 6 5

_17_ _17_ _17_

1 _20_ 2 1 _20_ 2 1 _20_ 2

_23_ _1_ _15_ _23_ _1_ _15_ _23_ _1_ _15_

_4_ _4_ _4_

4 _36_ 7 _9_ 3 4 _36_ 7 _9_ 3 4 _36_ 7 _9_ 3

_25_ _25_ _25_

_28_ _16_ _3_ _28_ _16_ _3_ _28_ _16_ _3_

6 5 6 5 6 5

_17_ _17_ _17_

1 _20_ 2

_23_ _1_ _15_

_4_

4 _36_ 7 3

_9_

_25_

_28_ _16_ _3_

6 5

_17_


**Kruskal’s Algorithm**

_T is the set of edges in the forest._

_F is the set of vertex-sets in the forest._

1. _T :=_ ; F :=
_∅_ _∅_
2. **for each vertex v** _V do F := F_ _v_
_∈_ _∪{{_ _}}_
3. Sort edges in E in ascending order of cost
4. **while** _F_ _> 1 do_
_|_ _|_
5. (u, v) := the next edge in sorted order
6. **if find(u)** = find(v) then
_̸_
7. union(u, v)
8. _T := T_ (u, v)
_∪{_ _}_

Lines 6 and 7 use union-find on F .

On termination, T contains the edges in the min cost
spanning tree for G = (V, E).

**Data Structures**

For

_E: adjacency list_

_•_
_F_ : union-find data structure

_•_
_T_ : linked list

_•_

**Analysis**

Line 1: O(1)

_•_
Line 2: O(n)

_•_
Line 3: O(e log e) = O(e log n)

_•_
Line 5: O(1)

_•_
Line 6: O(log n)

_•_
Line 7: O(log n)

_•_
Line 8: O(1)

_•_
Lines 4–8: O(e log n)

_•_

Total: O(e log n)

**Questions**

Would Prim’s algorithm do this?


6


-----

3

3

5

2 4

2 12 2 12

1 4 5 1

6 10

1 8 2 1 8
9

7 7

6 7 6

3

**Assigned Reading**

CLR Chapter 24.


3


6 10

1 8 11
9

7

6 7

3

3

5

2 4

2 12

1 4 5

6 10

1 8 11
9

7

6 7

3


3

|3 5 2 4 2 12 1 4 5 6 10 1 8 11 9 7 6 7|3 5 2 4 2 12 1 4 5 6 10 1 8 1 9 7 6 7 3 3 5 2 4 2 12 1 4 5 6 10 1 8 1 9 7 6 7|
|---|---|


Would Kruskal’s algorithm do this?

3 3

5 5

2 4 2 4

2 12 2 12

1 4 5 1 4 5

6 10 6 10

1 8 9 11 1 8 9 11

7 7

6 7 6 7

3 3

3 3

5 5

2 4 2 4

2 12 2 12

1 4 5 1 4 5

6 10 6 10

1 8 11 1 8 11
9 9


3


3

|3 5 2 4 2 12 1 4 5 6 10 1 8 11 9 7 6 7|3 5 2 4 2 12 1 4 5 6 10 1 8 1 9 7 6 7 3 3 5 2 4 2 12 1 4 5 6 10 1 8 1 9 7 6 7|
|---|---|


Could a min-cost spanning tree algorithm do this?


7


-----

###### Algorithms Course Notes Backtracking 1

 Ian Parberry[∗]

 Fall 2001


**Summary**

Backtracking: exhaustive search using divide-andconquer.

General principles:

backtracking with binary strings

_•_
backtracking with k-ary strings

_•_
pruning

_•_
how to write a backtracking algorithm

_•_

Application to

the knapsack problem

_•_
the Hamiltonian cycle problem

_•_
the travelling salesperson problem

_•_

**Exhaustive Search**

Sometimes the best algorithm for a problem is to try
all possibilities.

This is always slow, but there are standard tools that
we can use to help: algorithms for generating basic
objects such as

2[n] binary strings of length n

_•_
_k[n]_ _k-ary strings of length n_

_•_
_n! permutations_

_•_
_n!/r!(n_ _r)! combinations of n things chosen r_

_•_ _−_
at a time

Backtracking speeds the exhaustive search by pruning.

**Bit Strings**

Problem: Generate all the strings of n bits.

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


Solution: Use divide-and-conquer. Keep current
binary string in an array A[1..n]. Aim is to call
process(A) once with A[1..n] containing each binary
string. Call procedure binary(n):

**procedure binary(m)**
**comment process all binary strings of length m**
**if m = 0 then process(A) else**
_A[m] := 0; binary(m_ 1)
_−_
_A[m] := 1; binary(m_ 1)
_−_

**Correctness Proof**

Claim: For all m 1, binary(m) calls process(A)
_≥_
once with A[1..m] containing every string of m bits.

Proof: The proof is by induction on m. The claim
is certainly true for m = 0.

Now suppose that binary(m 1) calls process(A)
_−_
once with A[1..m 1] containing every string of m 1
_−_ _−_
bits.

First, binary(m)

sets A[m] to 0, and

_•_
calls binary(m 1).

_•_ _−_

By the induction hypothesis, this calls process(A)
once with A[1..m] containing every string of m bits
ending in 0.

Then, binary(m)

sets A[m] to 1, and

_•_
calls binary(m 1).

_•_ _−_

By the induction hypothesis, this calls process(A)
once with A[1..m] containing every string of m bits
ending in 1.


1


-----

Hence, binary(m) calls process(A) once with A[1..m]
containing every string of m bits.

**Analysis**

Let T (n) be the running time of binary(n). Assume
procedure process takes time O(1). Then,

� _c_ if n = 1
_T_ (n) =
2T (n 1) + d otherwise
_−_

Therefore, using repeated substitution,

_T_ (n) = (c + d)2[n][−][1] _d._
_−_

Hence, T (n) = O(2[n]), which means that the algorithm for generating bit-strings is optimal.

_k-ary Strings_

Problem: Generate all the strings of n numbers
drawn from 0..k 1.
_−_

Solution: Keep current k-ary string in an array A[1..n]. Aim is to call process(A) once with
_A[1..n] containing each k-ary string. Call procedure_
string(n):

**procedure string(m)**
**comment process all k-ary strings of length m**
**if m = 0 then process(A) else**
**for j := 0 to k** 1 do
_−_
_A[m] := j; string(m_ 1)
_−_

Correctness proof: similar to binary case.

Analysis: similar to binary case, algorithm optimal.

**Backtracking Principles**

Backtracking imposes a tree structure on the solution space. e.g. binary strings of length 3:


Backtracking does a preorder traversal on this tree,
processing the leaves.

Save time by pruning: skip over internal nodes that
have no useful leaves.

_k-ary strings with Pruning_

Procedure string fills the array A from right to left,
string(m, k) can prune away choices for A[m] that
are incompatible with A[m + 1..n].

**procedure string(m)**
**comment process all k-ary strings of length m**
**if m = 0 then process(A) else**
**for j := 0 to k** 1 do
_−_
**if j is a valid choice for A[m] then**
_A[m] := j; string(m_ 1)
_−_

**Devising a Backtracking Algorithm**

Steps in devising a backtracker:

Choose basic object, e.g. strings, permutations,

_•_
combinations. (In this lecture it will always be
strings.)
Start with the divide-and-conquer code for gen
_•_
erating the basic objects.
Place code to test for desired property at the

_•_
base of recursion.
Place code for pruning before each recursive

_•_
call.

General form of generation algorithm:

**procedure generate(m)**
**if m = 0 then process(A) else**
**for each of a bunch of numbers j do**
_A[m] := j; generate(m_ 1)
_−_

General form of backtracking algorithm:

**procedure generate(m)**
**if m = 0 then process(A) else**
**for each of a bunch of numbers j do**
**if j consistent with A[m + 1..n]**
**then A[m] := j; generate(m** 1)
_−_

|??? ??0 ??1 ?00 ?10 ?01 ?11 000 100 010 110 001 101 011 111|Col2|
|---|---|
|000|111|


2


-----

**The Knapsack Problem**

To solve the knapsack problem: given n rods, use
a bit array A[1..n]. Set A[i] to 1 if rod i is to be
used. Exhaustively search through all binary strings
_A[1..n] testing for a fit._

_n = 3, s1 = 4, s2 = 5, s3 = 2, L = 6._

_Length used_

??? 0

??0 _0_ ??1 _2_

?00 _0_ ?10 _5_ ?01 _2_ ?11 _7_

000 100 010 110 001 101 011 111

_0_ _4_ _5_ _9_ _2_ _6_

Gray means pruned

**The Algorithm**

Use the binary string algorithm. Pruning: let ℓ be
length remaining,

_A[m] = 0 is always legal_

_•_

_• A[m] = 1 is illegal if sm > ℓ; prune here_

To print all solutions to knapsack problem with n
rods of length s1, . . ., sn, and knapsack of length L,
call knapsack(n, L).

**procedure knapsack(m, ℓ)**
**comment solve knapsack problem with m**
rods, knapsack size ℓ
**if m = 0 then**
**if ℓ** = 0 then print(A)
**else**
_A[m] := 0; knapsack(m_ 1, ℓ)
_−_
**if sm ≤** _ℓ_ **then**
_A[m] := 1; knapsack(m −_ 1, ℓ _−_ _sm)_

Analysis: time O(2[n]).

**Generalized Strings**

Note that k can be different for each digit of the
string, e.g. keep an array D[1..n] with A[m] taking
on values 0..D[m] 1.
_−_


**procedure string(m)**
**comment process all strings of length m**
**if m = 0 then process(A) else**
**for j := 0 to D[m]** 1 do
_−_
_A[m] := j; string(m_ 1)
_−_

Application: in a graph with n nodes, D[m] could
be the degree of node m.

**Hamiltonian Cycles**

A Hamiltonian cycle in a directed graph is a cycle
that passes through every vertex exactly once.

3

2

4 5

1

6 7

Problem: Given a directed graph G = (V, E), find a
Hamiltonian cycle.

Store the graph as an adjacency list (for each vertex
_v_ 1, 2, . . ., n, store a list of the vertices w such
_∈{_ _}_
that (v, w) _E)._
_∈_

Store a Hamiltonian cycle as A[1..n], where the cycle
is

_A[n]_ _A[n_ 1] _A[2]_ _A[1]_ _A[n]_
_→_ _−_ _→· · · →_ _→_ _→_

Adjacency list:

|Length used|Col2|
|---|---|
|??? 0 ??0 0 ??1 2 ?00 0 ?10 5 ?01 2 ?11 7 000 100 010 110 001 101 011 111||
|000|111|


_N_ 1 2 3

1 2

2 3 4 6

3 4

4 1 7

5 3

6 1 4 7

7 5

Hamiltonian cycle:


_D_

1 1

2 3

3 1

4 2

5 1

6 3

7 1

|1|2|3|
|---|---|---|
|2|||
|3|4|6|
|4|||
|1|7||
|3|||
|1|4|7|
|5|||


1 2 3 4 5 6 7

_A_ 6 2 1 4 3 5 7

|6|2|1|4|3|5|7|
|---|---|---|---|---|---|---|


3


-----

**The Algorithm**

Use the generalized string algorithm. Pruning: Keep
a Boolean array U [1..n], where U [m] is true iff vertex m is unused. On entering m,

_U_ [m] = true is legal

_•_
_U_ [m] = false is illegal; prune here

_•_

To solve the Hamiltonian cycle problem, set up arrays N (neighbours) and D (degree) for the input graph, and execute the following. Assume that
_n > 1._

1. **for i := 1 to n** 1 do U [i] := true
_−_
2. _U_ [n] := false; A[n] := n
3. hamilton(n 1)
_−_

**procedure hamilton(m)**
**comment complete Hamiltonian cycle**
from A[m + 1] with m unused nodes
4. **if m = 0 then process(A) else**
5. **for j := 1 to D[A[m + 1]] do**
6. _w := N_ [A[m + 1], j]
7. **if U** [w] then
8. _U_ [w]:=false
9. _A[m] := w; hamilton(m_ 1)
_−_
10. _U_ [w]:=true

**procedure process(A)**
**comment check that the cycle is closed**
11. ok:=false
12. **for j := 1 to D[A[1]] do**
13. **if N** [A[1], j] = A[n] then ok:=true
14. **if ok then print(A)**

Notes on the algorithm:

From line 2, A[n] = n.

_•_
Procedure process(A) closes the cycle. At the

_•_
point where process(A) is called, A[1..n] contains a Hamiltonian path from vertex A[n] to
vertex A[1]. It remains to verify the edge from
vertex A[1] to vertex A[n], and print A if successful.
Line 7 does the pruning, based on whether the

_•_
new node has been used (marked in line 8).
Line 10 marks a node as unused when we return

_•_
from visiting it.


**Analysis**

How long does it take procedure hamilton to find one
Hamiltonian cycle? Assume that there are none.

Let T (n) be the running time of hamilton(v, n).
Suppose the graph has maximum out-degree d.
Then, for some b, c IN,
_∈_

� _bd_ if n = 0
_T_ (n)
_≤_ _dT_ (n 1) + c otherwise
_−_

Hence (by repeated substitution), T (n) = O(d[n]).

Therefore, the total running time on an n-vertex
graph is O(d[n]) if there are no Hamiltonian cycles.
The running time will be O(d[n] + d) = O(d[n]) if one
is found.

**Travelling Salesperson**

Optimization problem (TSP): Given a directed labelled graph G = (V, E), find a Hamiltonian cycle
of minimum cost (cost is sum of labels on edges).

Bounded optimization problem (BTSP): Given a directed labelled graph G = (V, E) and B IN, find a
_∈_
Hamiltonian cycle of cost _B._
_≤_

It is enough to solve the bounded problem. Then
the full problem can be solved using binary search.

Suppose we have a procedure BTSP(x) that returns
a Hamiltonian cycle of length at most x if one exists.
To solve the optimization problem, call TSP(1, B),
where B is the sum of all the edge costs (the cheapest
Hamiltonian cycle costs less that this, if one exists).

**function TSP(ℓ, r)**
**comment return min cost Ham. cycle**
of cost _r and_ _ℓ_
_≤_ _≥_
**if ℓ** = r then return (BTSP(ℓ)) else
_m :=_ (ℓ + r)/2
_⌊_ _⌋_
**if BTSP(m) succeeds**
**then return(TSP(ℓ, m))**
**else return(TSP(m + 1, r))**

(NB. should first call BTSP(B) to make sure a
Hamiltonian cycle exists.)

Procedure TSP is called O(log B) times (analysis
similar to that of binary search). Suppose


4


-----

the graph has n edges

_•_
the graph has labels at most b (so B _bn)_

_•_ _≤_
procedure BTSP runs in time O(T (n)).

_•_

Then, procedure TSP runs in time

(log n + log b)T (n).

**Backtracking for BTSP**

Let C[v, w] be cost of edge (v, w) _E, C[v, w] =_
_∈_ _∞_
if (v, w) _E._
_̸∈_

1. **for i := 1 to n** 1 do U [i] := true
_−_
2. _U_ [n] := false; A[n] := n
3. hamilton(n 1, B)
_−_

**procedure hamilton(m, b)**
**comment complete Hamiltonian cycle from**
_A[m + 1] with m unused nodes, cost_ _b_
_≤_
4. **if m = 0 then process(A, b) else**
5. **for j := 1 to D[A[m + 1]] do**
6. _w := N_ [A[m + 1], j]
7. **if U** [w] and C[A[m + 1], w] _b then_
_≤_
8. _U_ [w]:=false
9. _A[m] := w_
hamilton(m 1, b _C[v, w])_
_−_ _−_
10. _U_ [w]:=true

**procedure process(A, b)**
**comment check that the cycle is closed**
11. **if C[A[1], n]** _b then print(A)_
_≤_

Notes on the algorithm:

Extra pruning of expensive tours is done in

_•_
line 7.
Procedure process (line 11) is made easier using

_•_
adjacency matrix.

Analysis: time O(d[n]), as for Hamiltonian cycles.


5


-----

###### Algorithms Course Notes Backtracking 2

 Ian Parberry[∗]

 Fall 2001


**Summary**

Backtracking with permutations.

Application to

the Hamiltonian cycle problem

_•_
the peaceful queens problem

_•_

**Permutations**

Problem: Generate all permutations of n distinct
numbers.

Solution:

Backtrack through all n-ary strings of length n,

_•_
pruning out non-permutations.
Keep a Boolean array U [1..n], where U [m] is

_•_
```
  true iff m is unused.

```
Keep current permutation in an array A[1..n].

_•_
Aim is to call process(A) once with A[1..n] con
_•_
taining each permutation.

Call procedure permute(n):

**procedure permute(m)**
**comment process all perms of length m**
1. **if m = 0 then process(A) else**
2. **for j := 1 to n do**
3. **if U** [j] then
4. _U_ [j]:=false
5. _A[m] := j; permute(m_ 1)
_−_
6. _U_ [j]:=true

Note: this is what we did in the Hamiltonian cycle
algorithm. A Hamiltonian cycle is a permutation of
the nodes of the graph.

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


**Analysis**

Clearly, the algorithm runs in time O(n[n]). But this
analysis is not tight: it does not take into account
pruning.

How many times is line 3 executed? Running time
will be big-O of this.

What is the situation when line 3 is executed? The
algorithm has, for some 0 _i < n,_
_≤_

filled in i places at the top of A with part of a

_•_
permutation, and
tries n candidates for the next place in line 2.

_•_

What do the top i places in a permutation look like?

_i things chosen from n without duplicates_

_•_
permuted in some way

_•_

_permutation of i_
_things chosen from n_

_try n_
_things_

How many ways are there of filling in part of a permutation?
� _n_ �

_i!_

_i_

Therefore, number of times line 3 is executed is


�
_i!_


_n_


_n−1_
�

_i=0_


� _n_
_i_


1


-----

###### All permutations with 4 in the last place

 All permutations with 3 in the last place

 All permutations with 2 in the last place

 All permutations with 1 in the last place


= _n_


_n−1_
�

_i=0_


_n!_

(n _i)!_
_−_


###### 1 2 3 4


= _n_ _n!_
_·_


_n_
�

_i=1_


1

_i!_


(n + 1)!(e 1)
_≤_ _−_
1.718(n + 1)!
_≤_

**Analysis of Permutation Algorithm**

Therefore, procedure permute runs in time O((n +
1)!).

This is an improvement over O(n[n]). Recall that

|1|2|3|4|
|---|---|---|---|
|||||
||||4|
|?||||
||||3|
|||||
||||3|
|?||||
||||2|
|||||
||||2|
|?||||
||||1|
|||||
||||1|


_√_ � _n_
_n!_ 2πn
_∼_

_e_


_n_
�
_._


**Faster Permutations**

The permutation generation algorithm is not optimal: off by a factor of n

generates n! permutations

_•_
takes time O((n + 1)!).

_•_

A better algorithm: use divide and conquer to devise
a faster backtracking algorithm that generates only
permutations.

Initially set A[i] = i for all 1 _i_ _n._

_•_ _≤_ _≤_
Instead of setting A[n] to 1..n in turn, swap

_•_
values from A[1..n 1] into it.
_−_


**procedure permute(m)**
**comment process all perms in A[1..m]**
1. **if m = 1 then process(A) else**
2. permute(m 1)
_−_
3. **for i := 1 to m** 1 do
_−_
4. swap A[m] with A[j] for some 1 _j < m_
_≤_
5. permute(m 1)
_−_

Problem: How to make sure that the values swapped
into A[m] in line 4 are distinct?

Solution: Make sure that A is reset after every recursive call, and swap A[m] with A[i].

**procedure permute(m)**
1. **if m = 1 then process else**
2. permute(m 1)
_−_
3. **for i := m** 1 downto 1 do
_−_
4. swap A[m] with A[i]
5. permute(m 1)
_−_
6. swap A[m] with A[i]


2


-----

_n=2_

###### 1 2


_n=4_

|1|2|
|---|---|
|2|1|
|1|2|


_n=3_

###### 1 2 3 2 1 3
 1 2 3
 1 3 2 3 1 2
 1 3 2
 1 2 3
 3 2 1 2 3 1
 3 2 1
 1 2 3

_unprocessed at_
_n=2_
_n=3_
_n=4_

|1|2|3|
|---|---|---|
|2|1|3|
|1|2|3|
|1|3|2|
|3|1|2|
|1|3|2|
|1|2|3|
|3|2|1|
|2|3|1|
|3|2|1|
|1|2|3|

|1|2|3|n 4|
|---|---|---|---|
|1|2|3|4|
|2|1|3|4|
|1|2|3|4|
|1|3|2|4|
|3|1|2|4|
|1|3|2|4|
|1|2|3|4|
|3|2|1|4|
|2|3|1|4|
|3|2|1|4|
|1|2|3|4|
|1|2|4|3|
|2|1|4|3|
|1|2|4|3|
|1|4|2|3|
|4|1|2|3|
|1|4|2|3|
|1|2|4|3|
|4|2|1|3|
|2|4|1|3|
|4|2|1|3|
|1|2|4|3|
|1|2|3|4|

|4 1|4|3|2|
|---|---|---|---|
|1|4|3|2|
|4|1|3|2|
|1|4|3|2|
|1|3|4|2|
|3|1|4|2|
|1|3|4|2|
|1|4|3|2|
|3|4|1|2|
|4|3|1|2|
|3|4|1|2|
|1|4|3|2|
|1|2|3|4|
|4|2|3|1|
|2|4|3|1|
|4|2|3|1|
|4|3|2|1|
|3|4|2|1|
|4|3|2|1|
|4|2|3|1|
|3|2|4|1|
|2|3|4|1|
|3|2|4|1|
|4|2|3|1|
|1|2|3|4|


**Analysis**

Let _T_ (n) be the number of swaps made by
permute(n). Then T (1) = 0, and for n > 2,
_T_ (n) = nT (n 1) + 2(n 1).
_−_ _−_

Claim: For all n 1, T (n) 2n! 2.
_≥_ _≤_ _−_

Proof: Proof by induction on n. The claim is certainly true for n = 1. Now suppose the hypothesis
is true for n. Then,

_T_ (n + 1) = (n + 1)T (n) + 2n
(n + 1)(2n! 2) + 2n
_≤_ _−_
= 2(n + 1)! 2.
_−_

Hence, procedure permute runs in time O(n!), which
is optimal.

**Hamiltonian Cycles on Dense Graphs**

Use adjacency matrix: M [i, j] true iff (i, j) _E._
_∈_


1. **for i := 1 to n do**
2. _A[i] := i_
3. hamilton(n 1)
_−_

**procedure hamilton(m)**
**comment find Hamiltonian cycle from A[m]**
with m unused nodes
4. **if m = 0 then process(A) else**
5. **for j := m downto 1 do**
6. **if M** [A[m + 1], A[j]] then
7. swap A[m] with A[j]
8. hamilton(m 1)
_−_
9. swap A[m] with A[j]

**procedure process(A)**
**comment check that the cycle is closed**
10. **if M** [A[1], n] then print(A)

**Analysis**

Therefore, the Hamiltonian circuit algorithms run in
time

_O(d[n]) (using generalized strings)_

_•_
_O((n_ 1)!) (using permutations).

_•_ _−_

Which is the smaller of the two bounds? It depends
on d. The string algorithm is better if d _n/e_
_≤_
(e = 2.7183 . . .).

Notes on algorithm:

Note upper limit in for-loop on line 5 is m, not

_•_
_m_ 1: why?
_−_
Can also be applied to travelling salesperson.

_•_

**The Peaceful Queens Problem**

How many ways are there to place n queens on an
_n_ _n chessboard so that no queen threatens any_
_×_
other.


3


-----

Number the rows and columns 1..n. Use an array
_A[1..n], with A[i] containing the row number of the_
queen in column i.

1 2 3 4 5 6 7 8

1
2
3
4
5
6
7
8

###### A 4 2 7 3 6 8 5 1

This is a permutation!

**An Algorithm**

**procedure queen(m)**
1. **if m = 0 then process else**
2. **for i := m downto 1 do**
3. **if OK to put queen in (A[i], m) then**
4. swap A[m] with A[i]
5. queen(m 1)
_−_
6. swap A[m] with A[i]

How do we determine if it is OK to put a queen in
position (i, j)? It is OK if there is no queen in the
same diagonal or backdiagonal.

Consider the following array: entry (i, j) contains
_i + j._

1 2 3 4 5 6 7 8

1 2 3 4 5 6 7 8 9
2 3 4 5 6 7 8 9 10
3 4 5 6 7 8 9 10 11
4 5 6 7 8 9 1011 12
5 6 7 8 9 10 1112 13
6 7 8 9 1011 1213 14
7 8 9 10 1112 1314 15
8 9 1011 1213 1415 16

Note that:

Entries in the same back-diagonal are identical.

_•_


Entries are in the range 2..2n.

_•_

Consider the following array: entry (i, j) contains
_i_ _j._
_−_


1
2
3
4
5
6
7
8


1 2 3 4 5 6 7 8
0 -1 -2 -3 -4 -5 -6 -7
1 0 -1 -2 -3 -4 -5 -6
2 1 0 -1 -2 -3 -4 -5
3 2 1 0 -1 -2 -3 -4
4 3 2 1 0 -1 -2 -3
5 4 3 2 1 0 -1 -2
6 5 4 3 2 1 0 -1
7 6 5 4 3 2 1 0

|1|2|3|4|5|6|7|8|
|---|---|---|---|---|---|---|---|
|0|-1|-2|-3|-4|-5|-6|-7|
|1|0|-1|-2|-3|-4|-5|-6|
|2|1|0|-1|-2|-3|-4|-5|
|3|2|1|0|-1|-2|-3|-4|
|4|3|2|1|0|-1|-2|-3|
|5|4|3|2|1|0|-1|-2|
|6|5|4|3|2|1|0|-1|
|7|6|5|4|3|2|1|0|


Note that:

Entries in the same diagonal are identical.

_•_
Entries are in the range _n + 1..n_ 1.

_•_ _−_ _−_

Keep arrays b[2..2n] and d[ _n +1..n_ 1] (initialized
_−_ _−_
to true) such that:

_b[i] is false if back-diagonal i is occupied by a_

_•_
queen, 2 _i_ 2n.
_≤_ _≤_
_d[i] is false if diagonal i is occupied by a queen,_

_•_
_n + 1_ _i_ _n_ 1.
_−_ _≤_ _≤_ _−_

**procedure queen(m)**
1. **if m = 0 then process else**
2. **for i := m downto 1 do**
3. **if b[A[i] + m] and d[A[i]** _m] then_
_−_
4. swap A[m] with A[i]
5. _b[A[m] + m] := false_
6. _d[A[m]_ _m] := false_
_−_
7. queen(m 1)
_−_
8. _b[A[m] + m] := true_
9. _d[A[m]_ _m] := true_
_−_
10. swap A[m] with A[i]

**Experimental Results**

How well does the algorithm work in practice?

theoretical running time: O(n!)

_•_
implemented in Berkeley Unix Pascal on Sun

_•_
Sparc 2
practical for n 18

_•_ _≤_
possible to reduce run-time by factor of 2 (not

_•_
implemented)

|4|2|7|3|6|8|5|1|
|---|---|---|---|---|---|---|---|

|2|3|4|5|6|7|8|9|
|---|---|---|---|---|---|---|---|
|3|4|5|6|7|8|9|10|
|4|5|6|7|8|9|10|11|
|5|6|7|8|9|1|011|12|
|6|7|8|9|10|1|112|13|
|7|8|9|10|11|1|213|14|
|8|9|10|11|12|1|314|15|
|9|1|011|12|13|1|415|16|


4


-----

improvement over naive backtracking (theoreti
_•_
cally O(n _n!)) observed to be more than a con-_

_·_
stant multiple

_n_ **count** **time**

6 4 _< 0.001 seconds_

7 40 _< 0.001 seconds_

8 92 _< 0.001 seconds_

9 352 0.034 seconds

10 724 0.133 seconds

11 2,680 0.6 seconds

12 14,200 3.3 seconds

13 73,712 18.0 seconds

14 365,596 1.8 minutes

15 2,279,184 11.6 minutes

16 14,772,512 1.3 hours

17 95,815,104 9.1 hours

18 666,090,624 2.8 days

**Comparison of Running Times**

time (secs)

1e+06 perm

vanilla

1e+05

1e+04

1e+03

1e+02

1e+01

1e+00

1e-01

1e-02

1e-03
n

10.00 15.00

**Ratio of Running Times**

ratio

2.00

1.95

1.90

1.85

1.80

1.75

1.70

1.65

1.60

1.55

1.50

|n|count|time|
|---|---|---|
|6 7 8 9 10 11 12 13|4 40 92 352 724 2,680 14,200 73,712|< 0.001 seconds < 0.001 seconds < 0.001 seconds 0.034 seconds 0.133 seconds 0.6 seconds 3.3 seconds 18.0 seconds|
|14 15|365,596 2,279,184|1.8 minutes 11.6 minutes|
|16 17|14,772,512 95,815,104|1.3 hours 9.1 hours|
|18|666,090,624|2.8 days|

|)|Col2|Col3|perm|
|---|---|---|---|
||||perm|
||||vanilla|
|||||
|||||
|||||
|||||
|||||
|||||
|||||
|||||
|||||


1.45 n

10.00 15.00

|Col1|Col2|Col3|
|---|---|---|
||||
||||
||||
||||
||||
||||
||||
||||
||||
||||
||||


5


-----

**Summary**

Backtracking with combinations.

principles

_•_
analysis

_•_

**Combinations**


###### Algorithms Course Notes Backtracking 3

 Ian Parberry[∗]

 Fall 2001

Now suppose that r > 0 and for all i _r_ 1, in
_≥_ _−_
combinations processed by choose(i, r 1), A[1..r
_−_ _−_
1] contains a combination of r 1 things chosen from
_−_
1..i.

Now, choose(n, r) calls choose(i 1, r 1) with i
_−_ _−_
running from r to n. Therefore, by the induction
hypothesis and since A[r] is set to i, in combinations
processed by choose(n, r), A[1..r] contains a combination of r 1 things chosen from 1..i 1, followed
_−_ _−_
by the value i.


Problem: Generate all the combinations of n things
chosen r at a time.

Solution: Keep the current combination in an array
_A[1..r]. Call procedure choose(n, r)._

**procedure choose(m, q)**
**comment choose q elements out of 1..m**
**if q = 0 then process(A)**
**else for i := q to m do**
_A[q] := i_
choose(i 1, q 1)
_−_ _−_

**Correctness**

Proved in three parts:

1. Only combinations are processed.
2. The right number of combinations are processed.
3. No combination is processed twice.

Claim 1. If 0 _r_ _n, then in combinations pro-_
_≤_ _≤_
cessed by choose(n, r), A[1..r] contains a combination of r things chosen from 1..n.

Proof: Proof by induction on r. The hypothesis is
vacuously true for r = 0.

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


That is, A[1..r] contains a combination of r things
chosen from 1..n.

Claim 2. A call to choose(n, r) processes exactly

� _n_ �
_r_

combinations.

Proof: Proof by induction on r. The hypothesis is
certainly true for r = 0.

Now suppose that r > 0 and a call to choose(i,r 1)
_−_
generates exactly

� _i_ �
_r_ 1
_−_

combinations, for all r 1 _i_ _n._
_−_ _≤_ _≤_

Now, choose(n, r) calls choose(i 1, r 1) with i
_−_ _−_
running from r to n. Therefore, by the induction
hypothesis, the number of combinations generated
is


_n_
�

_i=r_


� _i_
_r_ 1
_−_

�
_._


� _i_ 1
_−_
_r_ 1
_−_


�
=


_n−1_
�

_i=r−1_


�


� _n_
=
_r_


The first step follows by re-indexing, and the second
step follows by Identity 2:


1


-----

**Identity 1**


� � _n + 1_
+
_r_

� � _n + 1_
+
_r_


�

�


=


_n_
�

_i=r_


� _i_
_r_


Claim:

� _n_
_r_


� � _n_
+
_r_ 1
_−_


� � _n + 1_
=
_r_


�


Proof:

� _n_ � � _n_ �

+

_r_ _r_ 1

_−_

_n!_ _n!_
=

_r!(n_ _r)! [+]_ (r 1)!(n _r + 1)!_
_−_ _−_ _−_


� _n + 1_
=
_r + 1_

� _n + 2_
=
_r + 1_


�
(By Identity 1).


(n + 1 _r)n! + rn!_
_−_
=

_r!(n + 1_ _r)!_
_−_

(n + 1)n!
=

_r!(n + 1_ _r)!_
_−_


� _n + 1_
=
_r_


�
_._


**Identity 2**

Claim: For all n 0 and 1 _r_ _n,_
_≥_ _≤_ _≤_


_n_

� _i_

�

_r_

_i=r_


� � _n + 1_
=
_r + 1_


�
_._


Proof: Proof by induction on n. Suppose r 1. The
_≥_
hypothesis is certainly true for n = r, in which case
both sides of the equation are equal to 1.

Now suppose n > r and that


**Back to the Correctness Proof**

Claim 3. A call to choose(n, r) processes combinations of r things chosen from 1..n without repeating
a combination.

Proof: The proof is by induction on r, and is similar
to the above.

Now we can complete the correctness proof: By
Claim 1, a call to procedure choose(n, r) generates
combinations of r things from 1..n (since r things at
a time are processed from the array A. By Claim
3, it never duplicates a combination. By Claim 2, it
generates exactly the right number of combinations.
Therefore, it generates exactly the combinations of
_r things chosen from 1..n._

**Analysis**

Let T (n, r) be the number of assignments to A made
in choose(n, r).

Claim: For all n 1 and 0 _r_ _n,_
_≥_ _≤_ _≤_


_n_

� _i_

�

_r_

_i=r_


� � _n + 1_
=
_r + 1_


Proof: A call to choose(n, r) makes the following
recursive calls:

**for i := r to n do**
_A[r] := i_
choose(i 1, r 1)
_−_ _−_

The costs are the following:


� _n_
_T_ (n, r) _r_
_≤_ _r_


�
_._


We are required to prove that


_n+1_

� _i_

�

_r_

_i=r_


� � _n + 2_
=
_r + 1_


�
_._

�
_._


Now, by the induction hypothesis,


_n+1_
�

_i=r_


� _i_
_r_


�


2


-----

_Call_ _Cost_
choose(r 1,r 1) _T_ (r 1, r 1) + 1
_−_ _−_ _−_ _−_
choose(r,r 1) _T_ (r, r 1) + 1
_−_ _−_
...
choose(n 1,r 1) _T_ (n 1, r 1) + 1
_−_ _−_ _−_ _−_

Therefore, summing these costs:


_T_ (n, r) =


_n−1_
� _T_ (i, r 1) + (n _r + 1)_

_−_ _−_
_i=r−1_


We will prove by induction on r that


� _n_
_T_ (n, r) _r_
_≤_ _r_


�
_._


The claim is certainly true for r = 0. Now suppose
that r > 0 and for all i < n,


� _i_
_T_ (i, r 1) (r 1)
_−_ _≤_ _−_ _r_ 1
_−_


�
_._


Then by the induction hypothesis and Identity 2,

_T_ (n, r)


=

_≤_


_n−1_
� _T_ (i, r 1) + (n _r + 1)_

_−_ _−_
_i=r−1_


_n−1_ � _i_
� ((r 1)

_−_ _r_ 1
_i=r−1_ _−_


�
) + (n _r + 1)_
_−_

�
+ (n _r + 1)_
_−_


= (r 1)
_−_


_n−1_
�

_i=r−1_


� _i_
_r_ 1
_−_


� _n_
= (r 1)
_−_ _r_


�
+ (n _r + 1)_
_−_


� _n_
_r_
_≤_ _r_


�


This last step follows since, for 1 _r_ _n,_
_≤_ _≤_

� _n_ �

_n_ _r + 1_

_r_ _≥_ _−_

This can be proved by induction on r. It is certainly
true for r = 1, since both sides of the inequality are
equal to n in this case.


Now suppose that r > 1.

� _n_ � _n!_

=

_r_ _r!(n_ _r)!_

_−_

_n(n_ 1)!
_−_
=

_r(r_ 1)!((n 1) (r 1))!
_−_ _−_ _−_ _−_

_n_ (n 1)!

_−_

=

_r_ (r 1)!((n 1) (r 1))!

_−_ _−_ _−_ _−_

_n_ � _n_ 1 �
= _−_

_r_ _r −_ 1

_n_
_≥_

_r_ [((][n][ −] [1)][ −] [(][r][ −] [1) + 1) (by hyp.)]

_n_ _r + 1 (since r_ _n)_
_≥_ _−_ _≤_

**Optimality**

Therefore, the combination generation algorithm

� _n_ �
runs in time O(r ) (since the amount of extra
_r_

computation done for each assignment is a constant).

Therefore, the combination generation algorithm
seems to have running time that is not optimal to

� _n_ �
within a constant multiple (since there are
_r_

combinations).

Unfortunately, it often seems to require this much
time. In the following table, A denotes the number
of assignments to array A, C denotes the number of
combinations, and Ratio denotes A/C.

**Experiments**


3


-----

_n_ _r_ _A_ _C_ _Ratio_

20 1 20 20 1.00

20 2 209 190 1.10

20 3 1329 1140 1.17

20 4 5984 4845 1.24

20 5 20348 15504 1.31

20 6 54263 38760 1.40

20 7 116279 77520 1.50

20 8 203489 125970 1.62

20 9 293929 167960 1.75

20 10 352715 184756 1.91

20 11 352715 167960 2.10

20 12 293929 125970 2.33

20 13 203489 77520 2.62

20 14 116279 38760 3.00

20 15 54263 15504 3.50

20 16 20348 4845 4.20

20 17 5984 1140 5.25

20 18 1329 190 6.99

20 19 209 20 10.45

20 20 20 1 20.00

**Optimality for r** _n/2_
_≤_

� _n_ �
It looks like T (n) < 2 provided r _n/2. But_
_r_ _≤_

is this true, or is it just something that happens with
small numbers?

Claim: If 1 _r_ _n/2, then_
_≤_ _≤_


we require that

(n + 2)(n 1)/2 _n(n_ 1) 2
_−_ _≤_ _−_ _−_
2n(n 1) (n + 2)(n 1) 4
_⇔_ _−_ _−_ _−_ _≥_
(n 2)(n 1) 4
_⇔_ _−_ _−_ _≥_
_n[2]_ 3n 2 0.
_⇔_ _−_ _−_ _≥_

This is true since n 4 (recall, r _n/2), since the_
_≥_ _≤_
_√_
largest root of n[2] 3n 2 0 is (3+ 17)/2 < 3.562.
_−_ _−_ _≥_

**The Case 3** _r_ _n/2_
_≤_ _≤_

Claim: If 3 _r_ _n/2, then_
_≤_ _≤_


**The Case r = 2**


Since

and


� _n_
2
2


_T_ (n, 2) =

=


_n−1_
� _T_ (i, 1) + (n 1)

_−_
_i=1_

_n−1_
� _i + (n_ 1)

_−_
_i=1_


= _n(n_ 1)/2 + (n 1)
_−_ _−_
= (n + 2)(n 1)/2,
_−_

�
2 = n(n 1) 2,
_−_ _−_ _−_


� _n_
_T_ (n, r) 2
_≤_ _r_


�
_r._
_−_


�
_r._
_−_


Observation: With induction, you often have to
prove something stronger than you want.

Proof: First, we will prove the claim for r = 1, 2.
Then we will prove it for 3 _r_ _n/2 by induction_
_≤_ _≤_
on n.

**The Case r = 1**

_T_ (n, 1) = n (by observation), and


Proof by induction on n. The base case is n = 6.
The only choice for r is 3. Experiments show that
the algorithm uses 34 assignments to produce 20
combinations. Since 2 20 2 = 38 > 34, the hy_·_ _−_
pothesis holds for the base case.

Now suppose n 6, which implies that r 3. By
_≥_ _≥_
the induction hypothesis and the case r = 1, 2,

_T_ (n, r)


� _n_
_T_ (n, r) 2
_≤_ _r_


� _n_
2
1


�
1 = 2n 1 _n._
_−_ _−_ _≥_


_n−1_
� _T_ (i, r 1) + (n _r + 1)_

_−_ _−_
_i=r−1_


_n−1_
�

_i=r−1_


� � _i_
2
_r_ 1
_−_


Hence,

as required.


� _n_
_T_ (n, 1) 2
_≤_ 1


�
1,
_−_


=

_≤_


� �
(r 1) + (n _r + 1)_
_−_ _−_ _−_


4


-----

�
(n _r + 1)(r_ 2)
_−_ _−_ _−_


= 2


_n−1_
�

_i=r−1_


� _i_
_r_ 1
_−_


� _n_
= 2
_r_

� _n_
2
_≤_ _r_

� _n_
_<_ 2
_r_


�
(n _r + 1)(r_ 2)
_−_ _−_ _−_

�
(n
_−_ _−_ _[n]_

2 [+ 1)(3][ −] [2)]

�
_r._
_−_

**Optimality Revisited**


Hence, our algorithm is optimal for r _n/2._
_≤_

Sometimes this is just as useful: if r > n/2, generate
the items not chosen, instead of the items chosen.


5


-----

###### Algorithms Course Notes Backtracking 4

 Ian Parberry[∗]

 Fall 2001


**Summary**

More on backtracking with combinations. Application to:

the clique problem

_•_
the independent set problem

_•_
Ramsey numbers

_•_

**Complete Graphs**

The complete graph on n vertices is Kn = (V, E)
where V = 1, 2, . . ., n, E = V _V ._
_{_ _}_ _×_

###### K2 K4
 1 2 1 2

 1 2
 4 3
 K3
 3

 K5 1 K6 1 2

 5 2
 4 3

 4 3 6 5

**Subgraphs**

A subgraph of a graph G = (V, E) is a graph B =
(U, F ) such that U _V and F_ _E._
_⊆_ _⊆_

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


###### 4 3 4 3

 6 5 6 5

**Induced Subgraphs**

An induced subgraph of a graph G = (V, E) is a
graph B = (U, F ) such that U _V and F = (U_
_⊆_ _×_
_U_ ) _E._
_∩_

###### 1 2 1 2

 4 3 4 3

 6 5 6 5

**The Clique Problem**

A clique is an induced subgraph that is complete.
The size of a clique is the number of vertices.

The clique problem:

Input: A graph G = (V, E), and an integer r.

Output: A clique of size r in G, if it exists.

Assumption: given u, v _V, we can check whether_
_∈_
(u, v) _E in O(1) time (use adjacency matrix)._
_∈_

**Example**

Does this graph have a clique of size 6?


1


-----

**procedure clique(m, q)**
1. **if q = 0 then print(A) else**
2. **for i := q to m do**
3. **if (A[q], A[j])** _E for all q < j_ _r_
_∈_ _≤_
**then**
4. _A[q] := i_
5. clique(i 1, q 1)
_−_ _−_

**Analysis**

Line 3 takes time O(r). Therefore, the algorithm
takes time


�
) if r _n/2, and_
_≤_

�
) otherwise.


Yes!

**A Backtracking Algorithm**

Use backtracking on a combination A of r vertices
chosen from V . Assume a procedure process(A) that
checks to see whether the vertices listed in A form a
clique. A represents a set of vertices in a potential
clique. Call clique(n, r).

Backtracking without pruning:

**procedure clique(m, q)**
**if q = 0 then process(A) else**
**for i := q to m do**
_A[q] := i_
clique(i 1, q 1)
_−_ _−_

Backtracking with pruning (line 3):


**The Independent Set Problem**

An independent set is an induced subgraph that has
no edges. The size of an independent set is the number of vertices.

The independent set problem:

Input: A graph G = (V, E), and an integer r.

Output: Does G have an independent set of size r?

Assumption: given u, v _V, we can check whether_
_∈_
(u, v) _E in O(1) time (use adjacency matrix)._
_∈_

**Complement Graphs**

The complement of a graph G = (V, E) is a graph
_G = (V, E), where E = (V_ _V )_ _E._
_×_ _−_

###### G G
 1 2 1 2

 4 3 4 3

 6 5 6 5

**Cliques and Independent Sets**

A clique in G is an independent set in G.


� _n_
_O(r_

_•_ _r_

� _n_
_O(r[2]_

_•_ _r_


2


-----

Backtrack through all binary strings A representing
the upper triangle of the incidence matrix of G.


###### G


###### G


Therefore, the independent set problem can be
solved with the clique algorithm, in the same running time: Change the if statement in line 3 from
“if (A[q], A[j]) _E” to “if (A[i], A[j])_ _E”._
_∈_ _̸∈_

**Ramsey Numbers**


###### 1 2 3

 n


_n-1 entries_
_n-2 entries_

_2 entries_
_1 entry_

|1|2 3 n . . .|Col3|Col4|Col5|Col6|Col7|Col8|
|---|---|---|---|---|---|---|---|
|||||||||
|. . .||||||||
|||||||||
|||||||||
|||||||||
|||||||||
|||||||||
|||||||||


Ramsey’s Theorem: For all i, j IN, there exists
_∈_
a value R(i, j) IN such that every graph G with
_∈_
_R(i, j) vertices either has a clique of size i or an_
independent set of size j.

So, R(i, j) is the smallest number n such that every
graph on n vertices has either a clique of size i or an
independent set of size j.

_i_ _j_ _R(i, j)_

3 3 6

3 4 9

3 5 14

3 6 18

3 7 23

3 8 28?

3 9 36

4 4 18


How many entries does A have?

_n−1_
� _i = n(n_ 1)/2

_−_
_i=1_


_1,2_ _. . ._ _1,n_ _2,3_ _. . ._ _2,n_ _. . ._ _i,i+1_ _..._ _i,j_


To test if (i, j) _E, where i < j, we need to consult_
_∈_
the (i, j) entry of the incidence matrix. This is stored
in

_A[n(i_ 1) _i(i + 1)/2 + j]._
_−_ _−_

|i|j|R(i, j)|
|---|---|---|
|3 3 3 3 3 3 3 4|3 4 5 6 7 8 9 4|6 9 14 18 23 28? 36 18|

|1,2|. . .|1,n|2,3|. . .|2,n|
|---|---|---|---|---|---|

|i,i+1|...|i,j|
|---|---|---|


_R(3, 8) is either 28 or 29, rumored to be 28._

**Finding Ramsey Numbers**


_(n-1) + (n-2) +...+(n-(i-1))_ _j-i_


_i−1_
�(n _k) + (j_ _i)_

_−_ _−_
_k=1_


If the following prints anything, then R(i, j) > n.
Run it for n = 1, 2, 3, . . . until the first time it doesn’t
print anything. That value of n will be R(i, j).

**for each graph G with n vertices do**
**if (G doesn’t have a clique of size i) and**
(G doesn’t have an indept. set of size j)
**then print(G)**


Address is:

=


= _n(i_ 1) _i(i_ 1)/2 + j _i_
_−_ _−_ _−_ _−_
= _n(i_ 1) _i(i + 1)/2 + j._
_−_ _−_


How do we implement the for-loop?


3


-----

###### G


**Example**

1 2 3 4 5 6
1 0 1 1 1 0 1
2 1 0 1 1 1 0
3 1 1 0 0 1 1

###### 3

4 1 1 0 0 1 1
5 0 1 1 1 0 1
6 1 0 1 1 1 0

|0 1|1 2|1 3|1 4|0  5|1 6|
|---|---|---|---|---|---|
|0|1|1|1|0|1|
|1|0|1|1|1|0|
|1|1|0|0|1|1|
|1|1|0|0|1|1|
|0|1|1|1|0|1|
|1|0|1|1|1|0|


1 2 3 4 5 6
###### 1 1 1 0 1 1
 1 1 1 0 2
 0 1 1 3
 1 1 4
 1 5

6


###### 1 1 1 0 1
 1 1 1 0
 0 1 1
 1 1
 1

|1|1|1|0|1|
|---|---|---|---|---|

|1|1|1|0|
|---|---|---|---|

|0|1|1|
|---|---|---|

|1|1|
|---|---|

|1 2|1 3|1 4|5 0|1 6|
|---|---|---|---|---|
|1|1|1|0|1|
|1 1 1 0 1 1|1|1|1|0|
|||0|1|1|
||||1|1|
|||||1|


###### 1 1 1 0 1 1 1 1 0 0 1 1 1 1 1

1 2 3 4 5 6 7 8 9 10 11 12 13 14 15

###### 1 1 1 0 1 1 1 1 0 0 1 1 1 1 1

**Further Reading**

R. L. Graham and J. H. Spencer, “Ramsey Theory”,
_Scientific American, Vol. 263, No. 1, July 1990._

R. L. Graham, B. L. Rothschild, and J. H. Spencer,
_Ramsey Theory, John Wiley & Sons, 1990._

|1|1|1|0|1|Col6|1|1|1|0|Col11|0|1|1|Col15|1|1|Col18|1|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|

|1|1|1|0|1|1|1|1|0|0|1|1|1|1|1|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|


4


-----

**Summary**


###### Algorithms Course Notes NP Completeness 1

 Ian Parberry[∗]

 Fall 2001

10110


An introduction to the theory of NP completeness:

Polynomial time computation

_•_
Standard encoding schemes

_•_
The classes P and NP.

_•_
Polynomial time reductions

_•_
_NP completeness_

_•_
The satisfiability problem

_•_
Proving new NP completeness results

_•_

**Polynomial Time**

Encode all inputs in binary. Measure running time
as a function of n, the number of bits in the input.

Assume

Each instruction takes O(1) time

_•_
The word size is fixed

_•_
There is as much memory as we need

_•_

A program runs in polynomial time if there are constants c, d IN such that on every input of size n,
_∈_
the program halts within time d _n[c]._
_·_

Polynomial time is not well-defined. Padding the
input to 2[n] bits (with extra zeros) makes an exponential time algorithm run in linear time.

But this doesn’t tell us how to compute faster.

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


Program Time 2[n]

Output

1011000000000000000000000000000000000

Program Time 2log _n_ _= n_

Output

**Standard Encoding Scheme**

We must insist that inputs are encoded in binary as
tersely as possible.

Padding by a polynomial amount is acceptable (since
a polynomial of a polynomial is a polynomial), but
padding by an exponential amount is not acceptable.

Insist that encoding be no worse than a polynomial
amount larger than the standard encoding scheme.
The standard encoding scheme contains a list each
mathematical object and a terse way of encoding it:

Integers: Store in binary using two’s comple
_•_
ment.

154 010011010
-97 10011111

Lists: Duplicate each bit of each list element,

_•_
and separate them using 01.

|Prog|ram|
|---|---|

|Pro|gram|
|---|---|


1


-----

4,8,16,22

100,1000,10000,10110

110000,11000000,1100000000,1100111100

1100000111000000011100000000011100111100

Sets: Store as a list of set elements.

_•_
Graphs: Number the vertices consecutively, and

_•_
store as an adjacency matrix.

**Standard Measures of Input Size**

There are some shorthand sizes that we can easily
remember. These are no worse than a polynomial of
the size of the standard encoding.

_• Integers: log2 of the absolute value of the inte-_
ger.
Lists: number of items in the list times size of

_•_
each item. If it is a list of n integers, and each
integer has less than n bits, then n will suffice.
Sets: size of the list of elements.

_•_
Graphs: Number of vertices or number of edges.

_•_

**Recognizing Valid Encodings**

Not all bit strings of size n encode an object. Some
are simply nonsense. For example, all lists use an
even number of bits. An algorithm for a problem
whose input is a list must deal with the fact that
some of the bit strings that it gets as inputs do not
encode lists.

For an encoding scheme to be valid, there must be a
polynomial time algorithm that can decide whether
a given inputs string is a valid encoding of the type
of object we are interested in.

**Examples**

Polynomial time algorithms

Sorting

_•_
Matrix multiplication

_•_
Optimal binary search trees

_•_
All pairs shortest paths

_•_
Transitive closure

_•_
Single source shortest paths

_•_
Min cost spanning trees

_•_


**Exponential Time**

A program runs in exponential time if there are constants c, d IN such that on every input of size n,
_∈_
the program halts within time d 2[n][c] .
_·_

Once again we insist on using the standard encoding
scheme.

Example: n! _n[n]_ = 2[n][ log][ n] is counted as exponen_≤_
tial time

Exponential time algorithms:

The knapsack problem

_•_
The clique problem

_•_
The independent set problem

_•_
Ramsey numbers

_•_
The Hamiltonian cycle problem

_•_

How do we know there are not polynomial time algorithms for these problems?

###### Polynomial Good Exponential Bad

**Complexity Theory**

We will focus on decision problems, that is, problems
that have a Boolean answer (such as the knapsack,
clique and independent set problems).

Define P to be the set of decision problems that can
be solved in polynomial time.

If x is a bit string, let _x_ denote the number of bits
_|_ _|_
in x.

Define NP to be the set of decision problems of the
following form, where R _P, c_ IN:
_∈_ _∈_

“Given x, does there exist y with _y_ _x_ such that
_|_ _| ≤|_ _|[c]_
(x, y) _R.”_
_∈_

|Polynomial Good Exponential Bad|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Col10|
|---|---|---|---|---|---|---|---|---|---|
|||||||||||
|||||||||||
|||||||||||
|||||||||||
|||||||||||


###### Polynomial Good


2


###### Polynomial Good


-----

That is, NP is the set of existential questions that
can be verified in polynomial time.

**Problems and Languages**

The language corresponding to a problem is the set
of input strings for which the answer to the problem
is affirmative.

For example, the language corresponding to the
clique problem is the set of inputs strings that encode a graph G and an integer r such that G has a
clique of size r.

We will use capital letters such as A or CLIQUE to
denote the language corresponding to a problem.

For example, x _CLIQUE means that x encodes a_
_∈_
graph G and an integer r such that G has a clique
of size r.

**Example**

The clique problem:

_x is a pair consisting of a graph G and an integer_

_•_
_r,_
_y is a subset of the vertices in G; note y has size_

_•_
smaller than x,
_R is the set of (x, y) such that y forms a clique_

_•_
in G of size r. This can easily be checked in
polynomial time.

Therefore the clique problem is a member of NP.
The knapsack problem and the independent set
problem are members of NP too. The problem of
finding Ramsey numbers doesn’t seem to be in NP.

_P versus NP_

Clearly P _NP._
_⊆_

To see this, suppose that A _P. Then A can be_
_∈_
rewritten as “Given x, does there exist y with size
zero such that x _A.”_
_∈_


It is not known whether P = NP.

But it is known that there are problems in NP with
the property that if they are members of P then
_P = NP. That is, if anything in NP is outside of_
_P, then they are too. They are called NP complete_
problems.

###### P NP

_NP complete problems_

Every problem in NP can be solved in exponential
time. Simply use exhaustive search to try all of the
bit strings y.

Also known:

If P = NP then there are problems in NP that

_•_ _̸_
are neither in P nor NP complete.
Hundreds of NP complete problems.

_•_

**Reductions**

A problem A is reducible to B if an algorithm for B
can be used to solve A. More specifically, if there is
an algorithm that maps every instance x of A into
an instance f (x) of B such that x _A iff f_ (x) _B._
_∈_ _∈_


###### P NP


_Min cost_
_spanning_
_trees_

_INDEPENDENT SET_


_KNAPSACK_

_CLIQUE_


3


-----

What we want: a program that we can ask questions
about A.

_Is x in A?_

**Yes!**

_Program_
_for A_

Instead, all we have is a program for B.

_Is x in A?_

**Say what?**

_Program_
_for B_

This is not much use for answering questions about
_A._

_Program_
_for B_

But, if A is reducible to B, we can use f to translate
the question about A into a question about B that
has the same answer.

_Is x in A?_

_Is f(x) in B?_

_Program_
_for f_

**Yes!**

_Program_
_for B_

**Polynomial Time Reductions**

A problem A is polynomial time reducible to B, written A ≤p B if there is a polynomial time algorithm


that maps every instance x of A into an instance
_f_ (x) of B such that x _A iff f_ (x) _B. Note that_
_∈_ _∈_
the size of f (x) can be no greater than a polynomial
of the size if x.

**Observation 1.**

Claim: If A ≤p B and B ∈ _P, then A ∈_ _P._

Proof: Suppose there is a function f that can be
computed in time O(n[c]) such that x _A iff f_ (x)
_∈_ _∈_
_B. Suppose also that B can be recognized in time_
_O(n[d])._

Given x such that _x_ = n, first compute f (x) using
_|_ _|_
this program. Clearly, _f_ (x) = O(n[c]). Then run
_|_ _|_
the polynomial time algorithm for B on input f (x).
The compete process recognizes A and takes time

_O(_ _f_ (x) ) = O((n[c])[d]) = O(n[cd]).
_|_ _|[d]_

Therefore, A _P._
_∈_

**Proving NP Completeness**

Polynomial time reductions are used for proving NP
completeness results.

Claim: If B ∈ _NP and for all A ∈_ _NP, A ≤p B, then_
_B is NP complete._

Proof: It is enough to prove that if B _P then_
_∈_
_P = NP._

Suppose B _P. Let A_ _NP. Then, since by hy-_
_∈_ _∈_
pothesis A ≤p B, by Observation 1 A ∈ _P. There-_
fore P = NP.

**The Satisfiability Problem**

A variable is a member of {x1, x2, . . .}.

A literal is either a variable xi or its complement xi.

A clause is a disjunction of literals

_C = xi1_ _xi2_ _xik_ _._
_∨_ _∨· · · ∨_

A Boolean formula is a conjunction of clauses

_C1 ∧_ _C2 ∧· · · ∧_ _Cm._


4


-----

**Satisfiability (SAT)**
Instance: A Boolean formula F .
Question: Is there a truth assignment to
the variables of F that makes F true?

**Example**

(x1 ∨ _x2 ∨_ _x3) ∧_ (x1 ∨ _x2 ∨_ _x3) ∧_
(x1 ∨ _x2) ∧_ (x1 ∨ _x2)_

This formula is satisfiable: simply take x1 = 1, x2 =
0, x3 = 0.

(1 0 1) (0 1 1)
_∨_ _∨_ _∧_ _∨_ _∨_ _∧_
(1 1) (0 1)
_∨_ _∧_ _∨_
= 1 1 1 1
_∧_ _∧_ _∧_
= 1

But the following is not satisfiable (try all 8 truth
assignments)

(x1 ∨ _x2) ∧_ (x1 ∨ _x3) ∧_ (x2 ∨ _x3) ∧_
(x1 ∨ _x2) ∧_ (x1 ∨ _x3) ∧_ (x2 ∨ _x3)_

**Cook’s Theorem**

SAT is NP complete.

This was published in 1971. It is proved by showing that every problem in NP is polynomial time reducible to SAT. The proof is long and tedious. The
key technique is the construction of a Boolean formula that simulates a polynomial time algorithm.
Given a problem in NP with polynomial time verification problem A, a Boolean formula F is constructed in polynomial time such that

_F simulates the action of a polynomial time al-_

_•_
gorithm for A
_y is encoded in any assignment to F_

_•_
the formula is satisfiable iff (x, y) _A._

_•_ _∈_


**Observation 2**

Claim: If A ≤p B and B ≤p C, then A ≤p C (transitivity).

Proof: Almost identical to the Observation 1.

Claim: If B ≤p C, C ∈ _NP, and B is NP complete,_
then C is NP complete.

Proof: Suppose B is NP complete. Then for every
problem A ∈ _NP, A ≤p B. Therefore, by transi-_
tivity, for every problem A ∈ _NP, A ≤p C. Since_
_C_ _NP, this shows that C is NP complete._
_∈_

**New NP Complete Problems from Old**

Therefore, to prove that a new problem C is NP
complete:

1. Show that C _NP._
_∈_

2. Find an NP complete problem B and prove that
_B ≤p C._

(a) Describe the transformation f .
(b) Show that f can be computed in polynomial time.
(c) Show that x _B iff f_ (x) _C._
_∈_ _∈_
i. Show that if x _B, then f_ (x) _C._
_∈_ _∈_
ii. Show that if f (x) _C, then x_ _B, or_
_∈_ _∈_
equivalently, if x _B, then f_ (x) _C._
_̸∈_ _̸∈_

This technique was used by Karp in 1972 to prove
many NP completeness results. Since then, hundreds more have been proved.

In the Soviet Union at about the same time, there
was a Russian Cook (although the proof of the NP
completeness of SAT left much to be desired), but
no Russian Karp.

The standard text on NP completeness:
M. R. Garey and D. S. Johnson, Computers and
_Intractability:_ _A Guide to the Theory of NP-_
_Completeness, W. H. Freeman, 1979._

**What Does it All Mean?**

Scientists have been working since the early 1970’s
to either prove or disprove P = NP. The consensus
_̸_
of opinion is that P = NP.
_̸_


5


-----

This open problem is rapidly gaining popularity as
one of the leading mathematical open problems today (ranking with Fermat’s last theorem and the
Reimann hypothesis). There are several incorrect
proofs published by crackpots every year.

It has been proved that CLIQUE, INDEPENDENT
_SET, and KNAPSACK are NP complete. Therefore,_
it is not worthwhile wasting your employer’s time
looking for a polynomial time algorithm for any of
them.

**Assigned Reading**

CLR, Section 36.1–36.3


6


-----

**Summary**


###### Algorithms Course Notes NP Completeness 2

 Ian Parberry[∗]

 Fall 2001

No:


The following problems are NP complete:

_3SAT_

_•_
_CLIQUE_

_•_
_INDEPENDENT SET_

_•_
_VERTEX COVER_

_•_

**Reductions**

###### SAT

 3SAT

 CLIQUE

 INDEPENDENT    SET

 VERTEX COVER

**3SAT**

_3SAT is the satisfiability problem with at most 3_
literals per clause. For example,

(x1 ∨ _x2 ∨_ _x3) ∧_ (x1 ∨ _x2 ∨_ _x3) ∧_
(x1 ∨ _x2) ∧_ (x1 ∨ _x2)_

_3SAT is a subproblem of SAT. Does that mean that_
_3SAT is automatically NP complete?_

_∗Copyright c⃝_ Ian Parberry, 1992–2001.


Some subproblems of NP complete problems are

_•_
_NP complete._
Some subproblems of NP complete problems are

_•_
in P.

Claim: 3SAT is NP complete.

Proof: Clearly 3SAT is in NP: given a Boolean formula with n operations, it can be evaluated on a
truth assignment in O(n) time using standard expression evaluation techniques.

It is sufficient to show that SAT ≤p 3SAT. Transform an instance of SAT to an instance of 3SAT as
follows. Replace every clause

(ℓ1 ∨ _ℓ2 ∨· · · ∨_ _ℓk)_

where k > 3, with clauses

_• (ℓ1 ∨_ _ℓ2 ∨_ _y1)_

_• (ℓi+1 ∨_ _yi−1 ∨_ _yi) for 2 ≤_ _i ≤_ _k −_ 3

_• (ℓk−1 ∨_ _ℓk ∨_ _yk−3)_

for some new variables y1, y2, . . ., yk−3 different for
each clause.

**Example**

Instance of SAT:

(x1 ∨ _x2 ∨_ _x3 ∨_ _x4 ∨_ _x5 ∨_ _x6) ∧_
(x1 ∨ _x2 ∨_ _x3 ∨_ _x5) ∧_
(x1 ∨ _x2 ∨_ _x6) ∧_ (x1 ∨ _x5)_

Corresponding instance of 3SAT:

(x1 ∨ _x2 ∨_ _y1) ∧_ (x3 ∨ _y1 ∨_ _y2) ∧_

|3S|AT|
|---|---|

|Col1|SAT 3SAT|Col3|Col4|
|---|---|---|---|
||CLI|QUE||
|||||
|IN|DEPE SET|NDE|NT|
|||||
||VERTEX COVER|||


1


-----

(x4 ∨ _y2 ∨_ _y3) ∧_ (x5 ∨ _x6 ∨_ _y3) ∧_

(x1 ∨ _x2 ∨_ _z1) ∧_ (x3 ∨ _x5 ∨_ _z1) ∧_
(x1 ∨ _x2 ∨_ _x6) ∧_ (x1 ∨ _x5)_

_Is_ ( _x_ 1 _x_ 2 _x_ 3 x 4 _x_ 5 _x_ 6 ) . . .

_in SAT?_

_Is_ ( _x_ 1 _x_ 2 _y_ 1 )

( _x_ 3 _y_ 1 _y_ 2 )
. . .

_in 3SAT?_

_Program_
_for f_

**Yes!**

_Program_
_for 3SAT_

**Back to the Proof**

Clearly, this transformation can be computed in
polynomial time.

Does this reduction preserve satisfiability?

Suppose the original Boolean formula is satisfiable.
Then there is a truth assignment that satisfies all of
the clauses. Therefore, for each clause

(ℓ1 ∨ _ℓ2 ∨· · · ∨_ _ℓk)_

there will be some ℓi with 1 ≤ _i ≤_ _k that is assigned_
truth value 1. Then in the new instance of 3SAT,
set each

_• ℓj for 1 ≤_ _j ≤_ _k to the same truth value_

_• yj = 1 for 1 ≤_ _j ≤_ _i −_ 2

_• yj = 0 for i −_ 2 < j ≤ _k −_ 3.

Every clause in the new Boolean formula is satisfied.

_Clause_ _Made true by_

(ℓ1 ∨ _ℓ2 ∨_ _y1)∧_ _y1_

(ℓ3 ∨ _y1 ∨_ _y2)∧_ _y2_

...

(ℓi−1 ∨ _yi−3 ∨_ _yi−2)∧_ _yi−2_

(ℓi ∨ _yi−2 ∨_ _yi−1)∧_ _ℓi_

(ℓi+1 ∨ _yi−1 ∨_ _yi)∧_ _yi−1_

...

(ℓk−2 ∨ _yk−4 ∨_ _yk−3)∧_ _yk−4_

(ℓk−1 ∨ _ℓk ∨_ _yk−3)_ _yk−3_


Therefore, if the original Boolean formula is satisfiable, then the new Boolean formula is satisfiable.

Conversely, suppose the new Boolean formula is satisfiable.

If y1 = 0, then since there is a clause

(ℓ1 ∨ _ℓ2 ∨_ _y1)_

in the new formula, and the new formula is satisfiable, it must be the case that one of ℓ1, ℓ2 = 1.
Hence, the original clause is satisfied.

If yk−3 = 1, then since there is a clause

(ℓk−1 ∨ _ℓk ∨_ _yk−3)_

in the new formula, and the new formula is satisfiable, it must be the case that one of ℓk−1, ℓk = 1.
Hence, the original clause is satisfied.

Otherwise, y1 = 1 and yk−3 = 0, which means there
must be some i with 1 ≤ _i ≤_ _k −_ 4 such that yi = 1
and yi+1 = 0. Therefore, since there is a clause

(ℓi+2 ∨ _yi ∨_ _yi+1)_

in the new formula, and the new formula is satisfiable, it must be the case that ℓi+2 = 1. Hence, the
original clause is satisfied.

This is true for all of the original clauses. Therefore,
if the new Boolean formula is satisfiable, then the
old Boolean formula is satisfiable.

This completes the proof that 3SAT is NP complete.

**Clique**

Recall the CLIQUE problem again:

**CLIQUE**
Instance: A graph G = (V, E), and an
integer r.
Question: Does G have a clique of size r?

Claim: CLIQUE is NP complete.

Proof: Clearly CLIQUE is in NP: given a graph G,
an integer r, and a set V _[′]_ of at least r vertices, it
is easy to see whether V _[′]_ _⊆_ _V forms a clique in G_
using O(n[2]) edge-queries.

|Clause|Made true by|
|---|---|
|(ℓ ℓ y ) 1 ∨ 2 ∨ 1 ∧ (ℓ y y ) 3 ∨ 1 ∨ 2 ∧ . . . (ℓ y y ) i−1 ∨ i−3 ∨ i−2 ∧|y 1 y 2 y i−2|
|(ℓ y y ) i ∨ i−2 ∨ i−1 ∧|ℓ i|
|(ℓ y y ) i+1 ∨ i−1 ∨ i ∧ . . . (ℓ y y ) k−2 ∨ k−4 ∨ k−3 ∧ (ℓ ℓ y ) k−1 ∨ k ∨ k−3|y i−1 y k−4 y k−3|


2


-----

It is sufficient to show that 3SAT ≤p CLIQUE.
Transform an instance of 3SAT into an instance of
_CLIQUE as follows._ Suppose we have a Boolean
formula F consisting of r clauses:

_F = C1 ∧_ _C2 ∧· · · ∧_ _Cr_

where each

_Ci = (ℓi,1_ _ℓi,2_ _ℓi,3)_
_∨_ _∨_

Construct a graph G = (V, E) as follows.

_V =_ (i, 1), (i, 2), (i, 3) such that 1 _i_ _r_ _._
_{_ _≤_ _≤_ _}_

The set of edges E is constructed as follows:
((g, h), (i, j)) _E iff g_ = i and either:
_∈_ _̸_

_• ℓg,h = ℓi,j, or_

_• ℓg,h and ℓi,j are literals of different variables._

Clearly, this transformation can be carried out in
polynomial time.

**Example**

(x1 ∨ _x2 ∨_ _x3) ∧_ (x1 ∨ _x2 ∨_ _x3) ∧_
(x1 ∨ _x2) ∧_ (x1 ∨ _x2)_

Clause 1

Clause 4 (x1,1) (x2,1)

(x2,4) (x3,1)

(x1,4)

( _x1_,2)

( _x2,3)_

(x2,2)

(x1,3) (x3,2)

Clause 2
Clause 3

Exactly the same literal in different clauses
Literals of different variables in different clauses


**Back to the Proof**

Observation: there is an edge between (g, h) and
(i, j) iff literals ℓg,h and ℓi,j are in different clauses
and can be set to the same truth value.

Claim that F is satisfiable iff G has a clique of size
_r._

Suppose that F is satisfiable. Then there exists an
assignment that satisfies every clause. Suppose that
for all 1 ≤ _i ≤_ _r, the true literal in Ci is ℓi,ji_, for some
1 ≤ _ji ≤_ 3. Since these r literals are assigned the
same truth value, by the above observation, vertices
(i, ji) must form a clique of size r.

Conversely, suppose that G has a clique of size r.
Each vertex in the clique must correspond to a literal
in a different clause (since no edges go between vertices representing literals in different clauses). Since
there are r of them, each clause must have exactly
one literal in the clique. By the observation, all of
these literals can be assigned the same truth value.
Setting the variables to make these literals true will
satisfy all clauses, and hence satisfy the formula F .

Therefore, G has a clique of size r iff F is satisfiable.

This completes the proof that CLIQUE is NP complete.

**Example**

(x1 ∨ _x2 ∨_ _x3) ∧_ (x1 ∨ _x2 ∨_ _x3) ∧_
(x1 ∨ _x2) ∧_ (x1 ∨ _x2)_


3


-----

Clause 1

Clause 4 (x1,1) (x2,1)

(x2,4) (x3,1)

(x1,4)

( _x1_,2)

( _x2,3)_

(x2,2)

(x1,3) (x3,2)

Clause 2
Clause 3

**Independent Set**

Recall the INDEPENDENT SET problem again:

**INDEPENDENT SET**

Instance: A graph G = (V, E), and an
integer r.

Question: Does G have an independent
set of size r?

Claim: INDEPENDENT SET is NP complete.

Proof: Clearly INDEPENDENT SET is in NP:
given a graph G, an integer r, and a set V _[′]_ of at least
_r vertices, it is easy to see whether V_ _[′]_ _⊆_ _V forms an_
independent set in G using O(n[2]) edge-queries.

It is sufficient to show that CLIQUE ≤p INDEPEN_DENT SET._

Suppose we are given a graph G = (V, E). Since
_G has a clique of size r iff G has an independent_
set of size r, and the complement graph G can be
constructed in polynomial time, it is obvious that
_INDEPENDENT SET is NP complete._


**Vertex Cover**

A vertex cover for a graph G = (V, E) is a set V _[′]_ _⊆_ _V_
such that for all edges (u, v) ∈ _E, either u ∈_ _V_ _[′]_ or
_v ∈_ _V_ _[′]._

Example:

###### 1 2

 4 3

 6 5

**VERTEX COVER**

Instance: A graph G = (V, E), and an
integer r.

Question: Does G have a vertex cover of
size r?

Claim: VERTEX COVER is NP complete.

Proof: Clearly VERTEX COVER is in NP: it is
easy to see whether V _[′]_ _⊆_ _V forms a vertex cover in_
_G using O(n[2]) edge-queries._

It is sufficient to show that INDEPENDENT SET
_≤p VERTEX COVER. Claim that V_ _[′]_ is an independent set iff V − _V_ _[′]_ is a vertex cover.


4


-----

Suppose V _[′]_ is an independent set in G. Then, there
is no edge between vertices in V _[′]. That is, every edge_
in G has at least one endpoint in V − _V_ _[′]. Therefore,_
_V −_ _V_ _[′]_ is a vertex cover.

Conversely, suppose V − _V_ _[′]_ is a vertex cover in G.
Then, every edge in G has at least one endpoint in
_V −_ _V_ _[′]. That is, there is no edge between vertices_
in V _[′]. Therefore, V_ _[′]_ is a vertex cover.

_Is (_, 3)

_in INDEPENDENT_ _Is (_, 4)
_SET?_

_in VERTEX_
_COVER?_

_Program_
_for f_

**Yes!**

_Program for_
_VERTEX_
_COVER_

**Assigned Reading**

CLR, Sections 36.4–36.5


5


-----

