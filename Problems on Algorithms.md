# Problems on Algorithms
##### Second Edition

 Ian Parberry and William Gasarch

###### July 2002

 Consisting of

 Problems on Algorithms, First Edition, by Ian Parberry, formerly published in 1994 by Prentice- Hall, Inc.

 Errata to the First Edition, published in 1998.

 Supplementary Problems, by William Gasarch.

 © Ian Parberry and William Gasarch, 2002.


-----

## License Agreement

###### This work is copyright Ian Parberry and William Gasarch. All rights reserved. The authors offer this work, retail value US$20, free of charge under the following conditions:
 • No part of this work may be made available on a public forum (including, but not limited to a web page, ftp site, bulletin board, or internet news group) without the written permission of the authors.
 • No part of this work may be rented, leased, or offered for sale commercially in any form or by any means, either print, electronic, or otherwise, without written permission of the authors.
 • If you wish to provide access to this work in either print or electronic form, you may do so by providing a link to, and/or listing the URL for the online version of this license agreement:

 http://hercule.csci.unt.edu/ian/books/free/license.html.

 You may not link directly to the PDF file.
 • All printed versions of any or all parts of this work must include this license agreement. Receipt of a printed copy of this work implies acceptance of the terms of this license agreement. If you have received a printed copy of this work and do not accept the terms of this license agreement, please destroy your copy by having it recycled in the most appropriate manner available to you.
 • You may download a single copy of this work. You may make as many copies as you wish for your own personal use. You may not give a copy to any other person unless that person has read, understood, and agreed to the terms of this license agreement.
 • You undertake to donate a reasonable amount of your time or money to the charity of your choice as soon as your personal circumstances allow you to do so. The author requests that you make a cash donation to The National Multiple Sclerosis Society in the following amount for each work that you receive:
 • $5 if you are a student,
 • $10 if you are a faculty member of a college, university, or school,
 • $20 if you are employed full-time in the computer industry.

 Faculty, if you wish to use this work in your classroom, you are requested to:
 • encourage your students to make individual donations, or
 • make a lump-sum donation on behalf of your class.

 If you have a credit card, you may place your donation online at:

 https://www.nationalmssociety.org/donate/donate.asp.

 Otherwise, donations may be sent to:

 National Multiple Sclerosis Society - Lone Star Chapter 8111 North Stadium Drive Houston, Texas 77054

 If you restrict your donation to the National MS Society's targeted research campaign, 100% of your money will be directed to fund the latest research to find a cure for MS. For the story of Ian Parberry's experience with Multiple Sclerosis, see http:// multiplesclerosissucks.com.


-----

### Problems on Algorithms

###### by

 Ian Parberry (ian@ponder.csci.unt.edu)

 Dept. of Computer Science University of North Texas Denton, TX 76203

 August, 1994


-----

### Contents

**Preface** **ix**

**1** **Introduction** **1**
1.1 How to Use This Book 1
1.2 Overview of Chapters 1
1.3 Pseudocode 3
1.4 Useful Texts 4

**2** **Mathematical Induction** **8**
2.1 Summations 8
2.2 Inequalities 10
2.3 Floors and Ceilings 10
2.4 Divisibility 11
2.5 Postage Stamps 11
2.6 Chessboard Problems 12
2.7 Fibonacci Numbers 14
2.8 Binomial Coefficients 14
2.9 What is Wrong? 15
2.10 Graphs 16
2.11 Trees 17
2.12 Geometry 18
2.13 Miscellaneous 19
2.14 Hints 20
2.15 Solutions 21
2.16 Comments 23

**iii**


-----

**iv** Contents

**3** **Big-O and Big-Ω** **28**
3.1 Rank the Functions 28
3.2 True or False? 30
3.3 Proving Big-O 31
3.4 Manipulating Big-O 32
3.5 Alternative Definitions 33
3.6 Find the Functions 34
3.7 Hints 35
3.8 Solutions 35
3.9 Comments 36

**4** **Recurrence Relations** **37**
4.1 Simple Recurrences 37
4.2 More Difficult Recurrences 38
4.3 General Formulae 39
4.4 Recurrences with Full History 39
4.5 Recurrences with Floors and Ceilings 40
4.6 Hints 41
4.7 Solutions 41
4.8 Comments 44

**5** **Correctness Proofs** **46**
5.1 Iterative Algorithms 46
5.1.1 Straight-Line Programs 47
5.1.2 Arithmetic 47
5.1.3 Arrays 49
5.1.4 Fibonacci Numbers 51
5.2 Recursive Algorithms 51
5.2.1 Arithmetic 52
5.2.2 Arrays 53
5.2.3 Fibonacci Numbers 54
5.3 Combined Iteration and Recursion 54
5.4 Hints 55
5.5 Solutions 56
5.6 Comments 58

**6** **Algorithm Analysis** **59**
6.1 Iterative Algorithms 59


-----

Contents **v**

6.1.1 What is Returned? 59
6.1.2 Arithmetic 61
6.1.3 Arrays 61
6.1.4 Fibonacci Numbers 62
6.2 Recursive Algorithms 62
6.2.1 Arithmetic 63
6.2.2 Arrays 63
6.2.3 Fibonacci Numbers 64
6.3 Combined Iteration and Recursion 64
6.4 Hints 64
6.5 Solutions 65
6.6 Comments 66

**7** **Divide-and-Conquer** **67**
7.1 Maximum and Minimum 67
7.2 Integer Multiplication 68
7.3 Strassen’s Algorithm 73
7.4 Binary Search 74
7.5 Quicksort 75
7.6 Towers of Hanoi 77
7.7 Depth-First Search 78
7.8 Applications 79
7.9 Hints 81
7.10 Solutions 83
7.11 Comments 85

**8** **Dynamic Programming** **87**
8.1 Iterated Matrix Product 87
8.2 The Knapsack Problem 89
8.3 Optimal Binary Search Trees 90
8.4 Floyd’s Algorithm 91
8.5 Applications 92
8.6 Finding the Solutions 97
8.7 Hints 99
8.8 Solutions 99
8.9 Comments 100


-----

**vi** Contents

**9** **Greedy Algorithms** **101**
9.1 Continuous Knapsack 101
9.2 Dijkstra’s Algorithm 102
9.3 Min-Cost Spanning Trees 103
9.4 Traveling Salesperson 109
9.5 Applications 109
9.6 Hints 111
9.7 Solutions 111
9.8 Comments 115

**10 Exhaustive Search** **116**
10.1 Strings 116
10.2 Permutations 118
10.3 Combinations 120
10.4 Other Elementary Algorithms 121
10.5 Backtracking 122
10.6 Applications 123
10.7 Hints 130
10.8 Solutions 131
10.9 Comments 133

**11 Data Structures** **135**
11.1 Heaps 135
11.2 AVL Trees 138
11.3 2–3 Trees 141
11.4 The Union-Find Problem 142
11.5 Applications 142
11.6 Hints 145
11.7 Solutions 145
11.8 Comments 146

**12** **-completeness** **147**
_NP_
12.1 General 147
12.2 Cook Reductions 148
12.3 What is Wrong? 150
12.4 Circuits 152
12.5 One-in-Three 3SAT 153
12.6 Factorization 154


-----

Contents **vii**

12.7 Hints 154
12.8 Solutions 155
12.9 Comments 155

**13 Miscellaneous** **156**
13.1 Sorting and Order Statistics 156
13.2 Lower Bounds 157
13.3 Graph Algorithms 158
13.4 Maximum Flow 160
13.5 Matrix Reductions 161
13.6 General 162
13.7 Hints 164
13.8 Solutions 166
13.9 Comments 166

**Bibliography** **168**

**Index** **174**


-----

**viii** Contents


-----

### Preface

The ability to devise effective and efficient algorithms in new situations is a skill
that separates the master programmer from the merely adequate coder. The best
way to develop that skill is to solve problems. To be effective problem solvers,
master-programmers-in-training must do more than memorize a collection of standard techniques and applications — they must in addition be able to internalize and
integrate what they have learned and apply it in new circumstances. This book is a
collection of problems on the design, analysis, and verification of algorithms for use
by practicing programmers who wish to hone and expand their skills, as a supplementary text for students enrolled in an undergraduate or beginning graduate class
on algorithms, and as a self-study text for graduate students who are preparing for
the qualifying (often called “breadth” or “comprehensive”) examination on algorithms for a Ph.D. program in Computer Science or Computer Engineering. It is
intended to augment the problem sets found in any standard algorithms textbook.
Recognizing that a supplementary text must be cost-effective if it is to be useful,
I have made two important and perhaps controversial decisions in order to keep its
length within reasonable bounds. The first is to cover only what I consider to be
the most important areas of algorithm design and analysis. Although most instructors throw in a “fun” advanced topic such as amortized analysis, computational
geometry, approximation algorithms, number-theoretic algorithms, randomized algorithms, or parallel algorithms, I have chosen not to cover these areas. The second
decision is not to search for the origin of the problems that I have used. A lengthy
discussion of the provenance of each problem would help make this book more scholarly, but would not make it more attractive for its intended audience — students
and practicing programmers.
To make this book suitable for self-instruction, I have provided at the end of
each chapter a small collection of hints, solutions, and comments. The solutions are
necessarily few for reasons of brevity, and also to avoid hindering instructors in their
selection of homework problems. I have included various preambles that summarize
the background knowledge needed to solve the problems so that students who are
familiar with the notation and style of their textbook and instructor can become
more familiar with mine.

**ix**


-----

**x** Preface

The organization of this book is a little unusual and requires a few words of
explanation. After a chapter of introduction, it begins with five chapters on background material that most algorithms instructors would like their students to have
mastered before setting foot in an algorithms class. This will be the case at some
universities, but even then most students would profit from brushing up on this
material by attempting a few of the problems. The introductory chapters include
mathematical induction, big-O notation, recurrence relations, correctness proofs,
and basic algorithm analysis methods. The correctness proof chapter goes beyond
what is normally taught, but I believe that students profit from it once they overcome their initial aversion to mathematical formalism.
The next four chapters are organized by algorithm design technique: divide-andconquer, dynamic programming, greedy algorithms, and exhaustive search. This
organization is somewhat nonstandard, but I believe that the pedagogical benefits
outweigh the drawbacks (the most significant of which seems to be the scattering of
problems on graph algorithms over several chapters, mainly in Sections 2.10, 2.11,
7.7, 8.4, 9.2, 9.3, 9.4, 13.3, and 13.4). Standard textbooks usually devote little time
to exhaustive search because it usually requires exponential time, which is a pity
when it contains many rich and interesting opportunities to practice the application
of algorithm design, analysis, and verification methods. The manuscript is rounded
out with chapters on advanced data structures and -completeness. The final
_NP_
chapter contains miscellaneous problems that do not necessarily fit into the earlier
chapters, and those for which part of the problem is to determine the algorithmic
technique or techniques to be used.
The algorithms in this book are expressed in a Pascal-like pseudocode. Two
problems (Problems 326 and 327) require the reader to examine some code written
in Pascal, but the details of the programming language are not a major factor in
the solutions. In any case, I believe that students of Computer Science should be
literate in many different programming languages.
For those who are interested in technical details, this manuscript was produced
from camera-ready copy provided by the author using L[A]TEX version 2.09 (which
used TEX C Version 3.14t3), using the Prentice Hall macros phstyle.sty written by J. Kenneth Shultis, and the twoside, epsf, and makeidx style files. The
Bibliography was created by BibTEX. The index was produced using the program
```
makeindex. The figures were prepared in encapsulated Postscript form using idraw,

```
and the graphs using xgraph. The dvi file produced by L[A]TEX was translated into
Postscript using dvips.
A list of errata for this book is available by anonymous ftp from ftp.unt.edu
(IP address 129.120.1.1), in the directory ian/poa. I will be grateful to receive
feedback, suggestions, errata, and in particular any new and interesting problems
(including those from areas not presently covered), which can be sent by electronic
mail to ian@ponder.csci.unt.edu.


-----

###### Chapter 1

### Introduction

_Problems on Algorithms contains 668 problems on the design, verification, and_
analysis of algorithms. This chapter is the only background that you will get before
we start listing problems. It is divided into four sections. The first section describes
the philosophy of this book and how to get the best out of it. The second section
contains an overview of the remaining chapters. The third section briefly touches
on the pseudocode used to describe algorithms. The fourth section gives a quick
review of some of the textbooks available on algorithms and related subjects.

###### 1.1 HOW TO USE THIS BOOK

Most chapters have sections with hints for, solutions to, and comments on selected
problems. It is recommended that readers first attempt the problems on their own.
The hints should be consulted only when encountering serious difficulty in getting
started. The solutions can be used as examples of the type of answers that are
expected. Only a limited number of solutions are given so that students are not
tempted to peek, and to ensure that there remains a large number of problems that
instructors can assign as homework.
Each problem is labeled with a sequence of icons. The more mortarboards

a problem has, the more difficult it is. Problems with one or two mortarboards are
suitable for a senior-level undergraduate class on algorithms. Problems with two or
three mortarboards are suitable for a graduate class on algorithms. The remaining
icons indicate the existence of additional material: The lightbulb indicates that
there is a hint, the scroll and feather indicates that there is a solution, and the
smiley face indicates that there is a comment. This is summarized for the
reader’s convenience in Table 1.1.

###### 1.2 OVERVIEW OF CHAPTERS

Chapters 2–4 contain problems on some background material on discrete mathematics that students should already have met before entering an undergraduate
algorithms course; respectively mathematical induction, big-O notation, and recurrence relations. If you are a student in an algorithms class, I strongly recommend

**1**


-----

**2** Chap. 1. Introduction

**Symbol** **Meaning**

easy
medium
difficult
hint
solution
comment

**Table 1.1. Problem symbols and their meaning.**

that you review this material and attempt some of the problems from Chapters 2–4
before attending the first class. Some kind instructors may spend a few lectures
“reminding” you of this material, but not all of them can afford the time to do so.
In any case, you will be ahead of the game if you devote some time to look over
the material again. If you ignored the material on mathematical induction in your
discrete mathematics class, thinking that it is useless to a programmer, then think
again. If you can master induction, you have mastered recursion — they are two
sides of the same coin.
You may also meet the material from Chapters 5 and 6 in other classes. Chapter 5 contains problems on correctness proofs. Not all instructors will emphasize
correctness proofs in their algorithms class, but mastering them will teach you important skills in formalization, expression, and design. The approach to correctness
proofs taken in Chapter 5 is closer to that taken by working researchers than the
formal-logic approach expounded by others such as Dijkstra [21]. Chapter 6 contains some problems involving the analysis of some naive algorithms. You should
have met this material in earlier classes, but you probably don’t have the depth of
knowledge and facility that you can get from working the problems in this chapter.
Chapters 7–10 consist of problems on various algorithm design techniques: respectively, divide-and-conquer, dynamic programming, greedy algorithms, and exhaustive search. The problems address some of the standard applications of these
techniques, and ask you to demonstrate your knowledge by applying the techniques
to new problems. Divide-and-conquer has already been foreshadowed in earlier
chapters, but the problems in Chapter 7 will test your knowledge further. The
treatment of exhaustive search in Chapter 10 goes beyond what is normally covered
in algorithms courses. The excuse for skimming over exhaustive search is usually a
natural distate for exponential time algorithms. However, extensive problems are
provided here because exhaustive search contains many rich and interesting opportunities to practice the application of algorithm design, analysis, and verification
methods.
Chapter 11 contains problems on advanced data structures, and Chapter 12

|Symbol|Meaning|
|---|---|
||easy medium difficult hint solution comment|


-----

Sec. 1.3. Pseudocode **3**

contains problems on -completeness, Finally, Chapter 13 contains miscellaneous
_NP_
problems, defined to be those that do not necessarily fit into the earlier chapters,
and those for which part of the problem is to determine the algorithmic technique
to be used.

###### 1.3 PSEUDOCODE

The algorithms in this text are described in a Pascal-like pseudocode. Here is a
quick overview of the conventions used:

**Data Types: Most variables are either integers or one- or two-dimensional arrays**
of integers. The notation P [i..j] is shorthand for an array P, whose elements
are P [i], P [i + 1], . . ., P [j]. Occasionally, variables will be other mathematical
objects such as sets or lists.

**Block-Structuring: Indentation is used to indicate block-structuring, in an at-**
tempt to save space.

**Assignment Statements: The “:=” symbol is the assignment operator.**

**Sequencing: A sequence of commands will be on separate lines or separated by**
semicolons.

**Selection: The selection command uses Pascal’s if-then-else syntax, which has**
the form

**if condition**
**then S1**
**else S2**

If the condition is true at time of execution, then S1 is executed; otherwise
_S2 is executed. The else clause will be omitted if it is empty._

**Indefinite Iteration: Indefinite iteration uses Pascal’s pre-tested while loop or**
post-tested repeat loop. The while loop has the form

**while condition do**
_S_

If the condition is true, then S is executed. The condition is then re-evaluated.
If it is false, the loop terminates. Otherwise S is executed again. The process
repeats until the condition is false. The repeat loop has the form

**repeat**
_S_
**until condition**


-----

**4** Chap. 1. Introduction

and is equivalent to

_S_
**while not condition do**
_S_

**Definite Iteration: Definite (count-controlled) iteration is achieved using Pascal’s**
**for loop.** Some loops count up (using the keyword to), and some count
down (using the keyword downto). An upward-counting for-loop will be
done zero times if the start value is larger than the finish value (analogously
for downward-counting for-loops). The syntax is as follows, with the upwardcounting loop on the left, and the downward-counting loop on the right:

**for i := s to f do** **for i := s downto f do**
_S_ _S_

which are equivalent to, respectively,

_i := s_ _i := s_
**while i** _f do_ **while i** _f do_
_≤_ _≥_
_S_ _S_
_i := i + 1_ _i := i_ 1
_−_

**Subroutines and Parameters: Subroutines are expressed using Pascal-style pro-**
**cedures and functions. Functions return a value, which unlike Pascal may**
be a complicated object. I have chosen to follow the lead of Aho, Hopcroft,
and Ullman [2] in using a C-like return statement to describe the value returned by a function. Procedures return values through their parameters.
Most parameters are value parameters, though some are variable parameters.
You’ll be able to tell the difference by context — those that return values are
obviously variable parameters! Comments in the algorithms should give you
an extra hint.

###### 1.4 USEFUL TEXTS

There are many good algorithms texts available, and more get published every
year. Here is a quick thumbnail sketch of some of them, and some related texts
that you might find useful. I recommend that the conscientious student examine
as many texts as possible in the library and choose one that suits their individual
taste. Remember, though, that different texts have differing areas of strength, and
appeal to different types of reader. I also strongly recommend that the practicing
programmer include in their library a copy of Bentley [9, 10]; Cormen, Leiserson,
and Rivest [19]; Garey and Johnson [28]; Graham, Knuth, and Patashnik [30]; and
Knuth [45, 46, 47].


-----

Sec. 1.4. Useful Texts **5**

**Aho, Hopcroft, and Ullman [1] This was the standard graduate text on algo-**
rithms and data structures for many years. It is written quite tersely, with
some sentences requiring a paragraph of explanation for some students. If you
want the plain facts with no singing or dancing, this is the book for you. It is
a little dated in presentation and material, but not particularly so.

**Aho, Hopcroft, and Ullman [2] This is the undergraduate version of the pre-**
vious book, with more emphasis on programming. It is full of minor errors.
A large number of the Pascal program fragments don’t work, even when you
correctly implement their C-like return statement.

**Aho and Ullman [3] This textbook is redefining the undergraduate computer sci-**
ence curriculum at many leading institutions. It is a good place to go to brush
up on your discrete mathematics, data structures, and problem solving skills.

**Baase [7] A good algorithms text at the upper-division undergraduate level.**

**Bentley [9, 10] This delightful pair of books are a collection of Jon Bentley’s Pro-**
gramming Pearls column from Communications of the ACM. They should be
recommended reading for all undergraduate computer science majors. Bentley explores the problems and pitfalls of algorithm design and analysis, and
pays careful attention to implementation and experimentation. The subjects
chosen are too idiosyncratic and anecdotal to be a textbook, but nonetheless
a useful pair of books.

**Brassard and Bratley [14] This is another good algorithms text with a strong**
emphasis on design techniques. The title comes from the French word algo_rithmique, which is what they (perhaps more aptly) call Computer Science._

**Cormen, Leiserson, and Rivest [19] This is an excellent text for those who can**
handle it. In the spirit of Aho, Hopcroft, and Ullman [1], it does not mess
around. A massive tome, it contains enough material for both a graduate and
undergraduate course in algorithms. It is the definitive text for those who
want to get right down to business, but it is not for the faint of heart.

**Even [26] This is the canonical book on graph algorithms covering most of the**
graph algorithm material taught in the typical algorithms course, plus more.
It is a little dated, but still very useful.

**Garey and Johnson [28] This is the canonical book on** -completeness. It is
_NP_
particularly useful for its large list of -complete problems. It is showing
_NP_
its age a little, but David Johnson has expressed an intention to work on a
Second Edition. More modern subjects are covered by David Johnson in “The
NP-Completeness Column: An On-Going Guide” published on a semiregular
basis in Journal of Algorithms (the latest was in September 1992, but David
Johnson recently assured me that more are planned).


-----

**6** Chap. 1. Introduction

**Gibbons [29] A more modern and carefully presented text on graph algorithms,**
superior in many ways to Even [26].

**Graham, Knuth, and Patashnik [30] An excellent book on discrete mathemat-**
ics for computer science. However, many students find it quite difficult going.
It is noted for its marginal (and often obscure) graffiti.

**Greene and Knuth [33] A highly mathematical text for an advanced course on**
algorithm analysis at Stanford. Recommended for the serious graduate student.

**Harel [34] This is another good text along the lines of Brassard and Bratley. It**
contains excellent high-level descriptions of subjects that tend to confuse the
beginning student if they are presented in all their detailed glory. It is noted
for its biblical quotes.

**Horowitz and Sahni [37] This is a reasonable text for many of the topics found**
in the typical algorithms class, but it is weak on analysis and but its approach
to backtracking is somewhat idiosyncratic and hard to follow.

**Kingston [44] A strong textbook for the elementary undergraduate algorithms**
course, but the coverage is a little shallow for advanced undergraduates. The
chapter on correctness proofs is an unusual but welcome addition. Divideand-conquer and dynamic programming are covered very sketchily, and the
approach to greedy algorithms is idiosyncratic but likely to strike a chord with
some students.

**Knuth [45, 46, 47] The Knuth three-volume series is the standard reference text**
for researchers and students. The material in it has aged well, except for
Knuth’s penchant for an obscure fictitious assembly-level code instead of the
more popular and easy to understand pseudocode.

**Kozen [50] A text for graduate students containing 40 lectures on algorithms. The**
terse presentation is not for everybody. It contains enough material for a single
graduate course, as opposed to the normal text that allows the instructor
to pick and choose the material to be covered. The choice of material is
strong but not to everybody’s taste. The homework problems (all of which
have solutions) and miscellaneous exercises (some of which have solutions) are
particularly useful.

**Lewis and Denenberg [52] A strong data structures text that also covers some**
of the material in the typical algorithms course.

**Manber [56] Some students find the approach taken in this book, which is algo-**
rithm design by successive refinement of intuitive but flawed version of the
algorithm, very helpful. Others, who do not think this way, hate it. It is
certainly more realistic in its approach to algorithm design than more formal


-----

Sec. 1.4. Useful Texts **7**

texts, but perhaps it encourages the wrong habits. Some important topics are
not covered in very great detail.

**Moret and Shapiro [58] This is planned as the first volume of a two-volume set.**
This volume covers tractable problems, and the second volume (unsighted
as yet) will cover intractable problems. It has a definite combinatorial optimization flavor. Dynamic programming is a notable omission from the first
volume.

**Papadimitriou and Steiglitz [59] A reasonable text for an algorithms course,**
but one which is very heavy with the jargon and mind-set of the combinatorial
optimization and numerical analysis community, which makes it a difficult
book to just dip into at random for the parts of it that are useful.

**Purdom and Brown [64] A mathematically rigorous text that focuses on anal-**
ysis almost to the exclusion of design principles.

**Rawlins [67] An entertaining text that nonetheless is technically rigorous and**
detailed.

**Sedgewick [72] This book studies a large array of standard algorithms, but it is**
largely descriptive in nature and does not spend much time on verification,
analysis, or design techniques. It is excellent for the elementary undergraduate
algorithms curriculum, but not sufficiently rigorous for upper-division courses.

**Smith [74] This is another strong algorithms text with an awesome collection of**
problems.

**Solow [75] This is a good text for the student who has trouble with mathematical**
formalism. The chapter on induction may be particularly useful for those who
have trouble getting started.

**Weiss [82] A strong data structures text that also covers quite a bit of the material**
in the typical algorithms course.

**Wilf [83] A book that does a good job on analysis, but does not cover algorithm**
design techniques. The selection of topics is limited to chapters on mathematical preliminaries, recursion, network flow, number-theoretic algorithms,
and -completeness.
_NP_


-----

###### Chapter 2

### Mathematical Induction

At first sight, this chapter may seem out of place because it doesn’t seem to be
about algorithms at all. Although the problems in this chapter are mainly mathematical in nature and have very little to do with algorithms, they are good practice
in a technique that is fundamental to algorithm design, verification, and analysis.
Unfortunately, many students come to my algorithms class poorly versed in the use
of induction. Either it was badly taught or they discarded it as useless information
(or both). If you are one of these students, you should start by attempting at least
some of the following problems. In addition to mastering the technique of mathematical induction, you should pay particular attention to the results in Sections 2.1,
2.2, 2.3, 2.7, 2.8, 2.10, and 2.11. Some of them are quite useful in algorithm design
and analysis, as we shall see later.

###### 2.1 SUMMATIONS

1. Prove by induction on n ≥ 0 that _i=1_ _[i][ =][ n][(][n][ + 1)][/][2.]_

[�][n]

2. Prove by induction on n ≥ 0 that _i=1_ _[i][2][ =][ n][(][n][ + 1)(2][n][ + 1)][/][6.]_

[�][n]

3. Prove by induction on n ≥ 0 that _i=1_ _[i][3][ =][ n][2][(][n][ + 1)][2][/][4.]_

[�][n]

4. Prove by induction on n 0 that
_≥_


_n_
�(2i + 1)[2] = (n + 1)(2n + 1)(2n + 3)/3.

_i=0_

5. Prove by induction on n ≥ 0 that _i=1_ _[i][(][i]_ [+1) =][ n][(][n] [+1)(][n] [+2)][/][3.]

[�][n]

6. Prove by induction on n 0 that
_≥_

_n_
� _i(i + 1)(i + 2) = n(n + 1)(n + 2)(n + 3)/4._

_i=1_


**8**


-----

Sec. 2.1. Summations **9**

7. Prove by induction on n ≥ 0 that _i=1_ _[i][ ·][ i][! = (][n][ + 1)!][ −]_ [1.]

[�][n]

8. Prove by induction on n ≥ 1 that _i=1_ [1][/][2][i][ = 1][ −] [1][/][2][n][.]

[�][n]

9. Prove by induction on n 1 that for every a = 1,
_≥_ _̸_

_n_
� _a[i]_ = _[a][n][+1][ −]_ [1] _._

_a_ 1

_i=0_ _−_


10. Prove by induction on n 0 that for every a = 1, and all 0 _j_ _n,_
_≥_ _̸_ _≤_ _≤_

_n_
� _a[i]_ = _[a][n][+1][ −]_ _[a][j]_ _._

_a_ 1

_i=j_ _−_


11. Prove by induction on n ≥ 0 that _i=0_ [2][i][ = 2][n][+1][ −] [1.]

[�][n]

12. Prove by induction on n 1 that
_≥_


_n_
�

_i=1_


1 _n_

_i(i + 1) [=]_ _n + 1_ _[.]_


13. Prove by induction on n ≥ 0 that _i=1_ _[i][2][i][ = (][n][ −]_ [1)2][n][+1][ + 2.]

[�][n]

14. Prove by induction on n 0 that for every a = 1,
_≥_ _̸_

_n_
� _ia[i]_ = _[na][n][+2][ −]_ [(][n][ + 1)][a][n][+1][ +][ a] _._

(a 1)[2]

_i=1_ _−_


15. Prove by induction on n 0 that
_≥_

_n_
� _i[2]2[i]_ = n[2]2[n][+1] _n2[n][+2]_ + 3 2[n][+1] 6.

_−_ _·_ _−_
_i=1_

16. Prove by induction on n 0 that
_≥_

_n_
� _i[2]2[n][−][i]_ = 2[n][+3] 2[n][+1] _n[2]_ 4n 6.

_−_ _−_ _−_ _−_
_i=1_

17. Prove by induction on n 0 that
_≥_


_n_
�

_i=1_


1

_n + i_ [=]


_n_
�

_i=1_


� 1

2i 1 2i
_−_ _[−]_ [1]


�
_._


-----

**10** Chap. 2. Mathematical Induction

###### 2.2 INEQUALITIES

18. Prove by induction on n 1 that if x > 1, then (1 + x)[n] 1 + nx.
_≥_ _−_ _≥_

19. Prove by induction on n 7 that 3[n] _< n!._
_≥_

20. Prove by induction on n 5 that 2[n] _> n[2]._
_≥_

21. Prove by induction on k ≥ 1 that _i=1_ _[i][k][ ≤]_ _[n][k][(][n][ + 1)][/][2.]_

[�][n]

22. Prove by induction on n 0 that
_≥_


_n_
�

_i=1_


1

_i[2][ <][ 2][ −]_ _n[1]_ _[.]_


23. Prove by induction that if n 4 is even, and 2 _i_ _n/2, then_
_≥_ _≤_ _≤_


_i_
�

_k=1_


_k_
�(n 2j + 1) 2

_−_ _≤_
_j=1_


_i_
�(n 2j + 1).

_−_
_j=1_


###### 2.3 FLOORS AND CEILINGS

Suppose x IR[+]. The floor of x, denoted _x_, is defined to be the largest integer
_∈_ _⌊_ _⌋_
that is no larger than x. The ceiling of x, denoted _x_, is defined to be the smallest
_⌈_ _⌉_
integer that is no smaller than x.

24. Prove by induction on n 0 that
_≥_


� _n_

2


� � _n/2_ if n is even
=
(n 1)/2 if n is odd.
_−_


25. Prove by induction on n 0 that
_≥_


� _n_

2


� � _n/2_ if n is even
=
(n + 1)/2 if n is odd.


26. Prove by induction on n 1 that for all m IR[+],
_≥_ _∈_


� _n_ � � _n + m −_ 1

=

_m_ _m_


�
_._


-----

Sec. 2.4. Divisibility **11**

###### 2.4 DIVISIBILITY

27. Prove by induction on n 0 that n[3] + 2n is divisible by 3.
_≥_

28. Prove by induction on n 0 that n[5] _n is divisible by 5._
_≥_ _−_

29. Prove by induction on n 0 that 5[n][+1] + 2 3[n] + 1 is divisible by 8.
_≥_ _·_

30. Prove by induction on n 0 that 8[n][+2] + 9[2][n][+1] is divisible by 73.
_≥_

31. Prove by induction that for all n 0, 11[n][+2] +12[2][n][+1] is divisible by 133.
_≥_

32. Define S IN IN as follows. (0, 0) _S._ If (m, n) _S, then_
_⊆_ _×_ _∈_ _∈_
(m +2, n +3) _S. Prove by induction on n_ 0 that for all (m, n) _S, m_ + _n_
_∈_ _≥_ _∈_
is divisible by 5.

33. Prove by induction that a decimal number is divisible by 3 iff the sum
of its digits is divisible by 3.

34. Prove by induction that a decimal number is divisible by 9 iff the sum
of its digits is divisible by 9.

35. Prove by induction that the sum of the cubes of three successive natural
numbers is divisible by 9.

36. Let Sn = {1, 2, . . ., 2n} be the set of integers from 1 to 2n. Let
_T ⊂_ _Sn be any subset containing exactly n + 1 elements of Sn. Prove by_
induction on n that there exists x, y _T_, x = y, such that x divides evenly
_∈_ _̸_
into y with no remainder.

###### 2.5 POSTAGE STAMPS

37. Show that any integer postage greater than 7 cents can be formed
by using only 3-cent and 5-cent stamps.

38. Show that any integer postage greater than 34 cents can be formed by
using only 5-cent and 9-cent stamps.

39. Show that any integer postage greater than 5 cents can be formed by
using only 2-cent and 7-cent stamps.

40. Show that any integer postage greater than 59 cents can be formed by
using only 7-cent and 11-cent stamps.

41. What is the smallest value of k such that any integer postage greater
than k cents can be formed by using only 4-cent and 9-cent stamps? Prove
your answer correct.


-----

**12** Chap. 2. Mathematical Induction

42. What is the smallest value of k such that any integer postage greater
than k cents can be formed by using only 6-cent and 11-cent stamps? Prove
your answer correct.

43. Show that for all n 1, any positive integer amount of postage that
_≥_
is at least n(n 1) cents can be formed by using only n-cent and (n + 1)-cent
_−_
stamps.

44. Show that for all m, n 1 such that gcd(m, n) = 1, there exists k IN
_≥_ _∈_
such that any positive integer amount of postage that is at least k cents can
be formed by using only m-cent and n-cent stamps.

###### 2.6 CHESSBOARD PROBLEMS

45. Prove by induction that for all n IN and all even m IN, an n _m_
_∈_ _∈_ _×_
chessboard has exactly the same number of black squares and white squares.

46. Prove by induction that for all odd n, m IN, an n _m chessboard has_
_∈_ _×_
all four corner squares colored the same.

47. Prove by induction that for all odd n, m IN, an n _m chessboard_
_∈_ _×_
with the corner squares colored white has one more white square than black
square.

48. Recall that a knight can make one of eight legal moves depicted in Figure 2.1. Figure 2.2 shows a closed knight’s tour on an 8 8
_×_
chessboard, that is, a circular tour of knight’s moves that visits every square
of the chessboard exactly once before returning to the first square. Prove by
induction that a closed knight’s tour exists for any 2[k] 2[k] chessboard for all
_×_
_k_ 3.
_≥_

A triomino is an “L”-shaped tile formed by three adjacent squares of a chessboard,
shown in Figure 2.3. An arrangement of triominoes is a tiling of a chessboard if
it covers it exactly without overlap, except for one square which is missed. For
example, Figure 2.4 shows a chessboard with a missing square filled in black on the
left, and a tiling with triominos that covers every square of the board except this
one on the right.

49. Prove by induction on n 1 that any 2[n] 2[n] chessboard that
_≥_ _×_
is missing one square can be tiled with triominoes, regardless of where the
missing square is.

50. Prove or disprove that all chessboards of the following dimensions
can be tiled by triominoes: (a) 3 2[n], (b) 6 2[n], (c) 3[n] 3[n], (d) 6[n] 6[n].
_×_ _×_ _×_ _×_


-----

Sec. 2.6. Chessboard Problems **13**

2 3

1 4

8 5

7 6

**Figure 2.1.** The eight legal moves that a knight on the
center square can make.

**Figure 2.2. A closed knight’s tour on an 8** 8 chessboard.
_×_

**Figure 2.3. A triomino.**

**Figure 2.4. A chessboard with a missing square filled in**
black (left), and a tiling with triominos that covers every
square of the board except the missing one (right).

|Col1|2|Col3|3|Col5|
|---|---|---|---|---|
|1||||4|
||||||
|8||||5|
||7||6||


-----

**14** Chap. 2. Mathematical Induction

51. Prove that any 2[n] 2[n] chessboards with one square missing
_×_
can be tiled by triominoes of only three colors so that no pair of triominoes
that share an edge have the same color.

###### 2.7 FIBONACCI NUMBERS

The Fibonacci numbers Fn for (n ≥ 0) are defined recursively as follows: F0 = 0,
_F1 = 1, and for n ≥_ 2, Fn = Fn−1 + Fn−2.

52. Prove by induction on n that [�]i[n]=0 _[F][i][ =][ F][n][+2][ −]_ [1.]

53. Prove by induction that Fn+k = FkFn+1 + Fk−1Fn.

54. Prove by induction on n ≥ 1 that _i=1_ _[F][ 2]i_ [=][ F][n][F][n][+1][.]

[�][n]

55. Prove by induction on n ≥ 1 that Fn+1Fn+2 = FnFn+3 + (−1)[n].

56. Prove by induction on n ≥ 2 that Fn−1Fn+1 = Fn[2] [+ (][−][1)][n][.]

###### 2.8 BINOMIAL COEFFICIENTS


The binomial coefficient
� _n_
_r_


�
_,_


for n, r IN, r _n, is defined to be the number of ways of choosing r things from_
_∈_ _≤_
_n without replacement, that is,_

� _n_ � _n!_

=

_r_ _r!(n_ _r)!_ _[.]_

_−_

57. Prove by induction on n that


_n_
�

_m=0_


� _n_
_m_


�
= 2[n].


58. Prove by induction on n 1 that for all 1 _m_ _n,_
_≥_ _≤_ _≤_

� _n_ �

_n[m]._

_m_ _≤_


-----

Sec. 2.9. What is Wrong? **15**

59. Prove by induction on n that


�
_a[m]b[n][−][m]._


(a + b)[n] =


_n_
�

_m=0_


� _n_
_m_


60. Prove by induction on n that for all even n, if k = n/2, then
_̸_
� _n_ � � _n_ �

_>_ _._

_n/2_ _k_

61. Prove by induction on n that for all even n,

� _n_ �

= Ω(2[n]/n).

_n/2_

62. Prove by induction that for all n IN,
_∈_


_n_ � _n_
�

_i_
_·_ _i_
_i=0_


�
= n2[n][−][1].


63. Prove by induction that for all n IN,
_∈_


_n_ � _n_
� 2[−][i]

_·_ _i_
_i=0_

###### 2.9 WHAT IS WRONG?


�
= (3/2)[n].


64. What, if anything is wrong with the following reasoning? All horses
are the same color. The proof is by induction on the number of horses. The
base of the induction is easy: If there is one horse, then it is trivially the same
color as itself. Now suppose that there are n horses, numbered 1 through n.
By the induction hypothesis, horses 1 through n 1 have the same color (let’s
_−_
say black). In particular, horse 2 is black. Also by the induction hypothesis,
horses 2 through n have the same color. Since horse 2 is black, this means
that horses 2 through n must be black. Therefore, all of the horses have the
same color.

65. What is wrong with the following proof? We claim that 6n = 0 for all
_n_ IN. The proof is by induction on n 0. Clearly, if n = 0, then 6n = 0.
_∈_ _≥_
Now, suppose that n > 0. Let n = a + _b. By the induction hypothesis, 6a = 0_
and 6b = 0. Therefore,

6n = 6(a + b) = 6a + 6b = 0 + 0 = 0.


-----

**16** Chap. 2. Mathematical Induction

66. What is wrong with the following reasoning? We show that for every
_n ≥_ 3, Fn is even. The base of the induction is trivial, since F3 = 2. Now
suppose that n ≥ 4 and that Fm is even for all m < n. Then Fn = Fn−1+Fn−2,
and by the induction hypothesis Fn−1 and Fn−2 are even. Thus, Fn is the
sum of two even numbers, and must therefore be even.

###### 2.10 GRAPHS

A graph is an ordered pair G = (V, E), where V is a finite set and E _V_ _V . The_
_⊆_ _×_
elements of V are called nodes or vertices, and the elements of E are called edges.
We will follow the normal conventions of using n for the number of nodes and e for
the number of edges. Where convenient we will take V = {v2, v2, . . ., vn}.

67. Prove by induction that a graph with n vertices can have at most
_n(n_ 1)/2 edges.
_−_

68. A tournament is a directed graph formed by taking the complete
undirected graph and assigning arbitrary directions on the edges. That is,
it is a graph G = (V, E) such that for all u, v _V, either exactly one of_
_∈_
(u, v), (v, u) _E. Show that every tournament has a Hamiltonian path, that_
_∈_
is, a path that visits every vertex exactly once.

69. An Eulerian cycle in a connected graph is a cycle in which
every edge appears exactly once. Prove by induction that every graph in
which each vertex has even degree (that is, each vertex has an even number
of edges incident with it) has an Eulerian cycle.

The hypercube of dimension n is a graph defined as follows. A hypercube of dimension 0 is a single vertex. To build a hypercube of dimension n, start with a
hypercube of dimension n 1. Take a second, exact copy of this hypercube. Draw
_−_
an edge from each vertex in the first copy to the corresponding vertex of the second
copy. For example, Figure 2.5 shows the hypercubes of dimensions 0, 1, 2, 3, and 4.

70. Prove by induction that a hypercube of dimension n has 2[n] vertices.

71. Prove by induction that a hypercube of dimension n has n2[n][−][1] edges.

72. Prove by induction that every hypercube has a Hamiltonian cycle, that
is, a cycle that visits every vertex exactly once.

73. Prove by induction that the vertices of a hypercube can be colored using
two colors so that no pair of adjacent vertices have the same color.


-----

Sec. 2.11. Trees **17**

Dimension 0 Dimension 1 Dimension 2

Dimension 3 Dimension 4

**Figure 2.5. Some hypercubes of various dimensions.**

74. Prove by induction that the edges of an n-dimensional hypercube can be
colored using n colors so that no pair of edges that share a common vertex
have the same color.

75. Prove by induction that an n-dimensional hypercube has exactly

� _n_ �

2[n][−][k]

_k_

different subcubes of dimension k.

###### 2.11 TREES

A tree is a special kind of graph defined as follows[1]. A single vertex v is a tree
with root v. Suppose Ti = (Vi, Ei) are disjoint trees with roots ri respectively, for
1 ≤ _i ≤_ _k. Suppose r ̸∈_ _V1, V2, . . ., Vk. Then, T = (V, E) is a tree, where_

_V_ = _V1 ∪_ _V2 ∪· · · ∪_ _Vk ∪{r},_
_E_ = _E1 ∪_ _E2 ∪· · · ∪_ _Ek ∪{(r, r1), (r, r2), . . ., (r, rk)}._

1Technically, this is actually called a rooted tree, but the distinction is not of prime importance
here.


-----

**18** Chap. 2. Mathematical Induction

The root of a tree is said to be at level 1. For all i 1, a child of a level i node
_≥_
is said to be at level i +1. The number of levels in a tree is the largest level number
of any node in the tree. A binary tree is a tree in which all nodes have at most two
children. A complete binary tree is a binary tree in which all leaves are at the same
level.

76. Prove by induction that a tree with n vertices has exactly n 1 edges.
_−_

77. Prove by induction that a complete binary tree with n levels has 2[n] 1
_−_
vertices.

78. Prove by induction that if there exists an n-node tree in which all the
nonleaf nodes have k children, then n mod k = 1.

79. Prove by induction that for every n such that n mod k = 1, there exists
an n-node tree in which all of the nonleaf nodes have k children.

80. Prove by induction that between any pair of vertices in a tree there is a
unique path.

81. A cycle in a graph G = (V, E) is a sequence of distinct vertices
_v1, v2, . . ., vk such that (vk, v1) ∈_ _E, and for all 1 ≤_ _i < k, (vi, vi+1) ∈_ _E._
Prove by induction that a tree is a connected graph that has no cycles.

82. Prove by induction that a connected graph that has no cycles is a
tree.

83. A spanning tree of a graph G = (V, E) is a tree T = (V, F ), where F _E._
_⊆_
Prove by induction that an n-node graph can have as many as (n 1)! spanning
_−_
trees.

###### 2.12 GEOMETRY

84. Prove that any set of regions defined by n lines in the plane can be
colored with two colors so that no two regions that share an edge have the
same color.

85. Prove by induction that n circles divide the plane into n[2] _n + 2_
_−_
regions if every pair of circles intersect in exactly two points, and no three
circles intersect in a common point. Does this hold for closed shapes other
than circles?

86. A polygon is convex if every pair of points in the polygon can be
joined by a straight line that lies in the polygon. Prove by induction on n 3
_≥_
that the sum of the angles of an n-vertex convex polygon is 180(n 2) degrees.
_−_


-----

Sec. 2.13. Miscellaneous **19**

87. Consider any arrangement of n 3 lines in general position in the plane
_≥_
(that is, no pair of lines is parallel, and no three lines can have a common
point). Prove that at least one of the minimal connected regions that they
form is a triangle.

88. Consider any arrangement of n 3 lines in general position in the
_≥_
plane. Prove that at least n 2 of the minimal connected regions in any such
_−_
arrangement are triangles. Is this bound tight?

89. Prove that n straight lines in the plane, all passing through a single
point, divide the plane into 2n regions.

90. Prove that n planes in space, all passing through a single point, no
three of which meet in a straight line, divide space into n(n 2) + 2 regions.
_−_

###### 2.13 MISCELLANEOUS

91. Suppose Mi is an ri−1 × ri matrix, for 1 ≤ _i ≤_ _n. Prove by induction on_
_n ≥_ 1 that the matrix product M1 · M2 · · · Mn is an r0 × rn matrix.

92. Prove by induction on n 1 that the binary representation of n has
_≥_
log n + 1 bits.
_⌊_ _⌋_

93. If x, y `true, false`, let x _y denote the exclusive-or of x and y,_
_∈{_ _}_ _⊕_
which is defined to be true iff exactly one of x and y is true. Note that
the exclusive-or operation is associative, that is, a (b _c) = (a_ _b)_ _c._
_⊕_ _⊕_ _⊕_ _⊕_
Prove by induction on n that x1 _x2_ _xn is true iff an odd number of_
_⊕_ _⊕· · · ⊕_
_x1, x2, . . ., xn are true._

94. (The Pigeonhole Principle) Suppose n pigeons roost in m holes.
Prove by induction on n that there must be at least one hole containing at
least _n/m_ pigeons.
_⌈_ _⌉_

95. Suppose An = {a1, a2, . . ., an} is a set of distinct coin types,
where each ai ∈ IN, for 1 ≤ _i ≤_ _n. Suppose also that a1 ≤_ _a2 ≤· · · ≤_ _an. The_
coin-changing problem is defined as follows. Given C IN, find the smallest
_∈_
number of coins from An that add up to C, given that an unlimited number of
coins of each type are available. Show that for all n ≥ 2, if a1 = 1, then there
is always a solution to the coin-changing problem, and that solution uses less
than a2 coins of type a1. What happens when a1 = 1?
_̸_

A Gray code is a list of the 2[n] _n-bit strings in which each string differs from the_
previous one in exactly one bit. Consider the following algorithm for listing the


-----

**20** Chap. 2. Mathematical Induction

_n-bit strings. If n = 1, the list is 0, 1. If n > 1, first take the list of (n_ 1)-bit
_−_
strings, and place a 0 in front of each string. Then, take a second copy of the list of
(n 1)-bit strings, place a 1 in front of each string, reverse the order of the strings,
_−_
and place it after the first list. So, for example, for n = 2 the list is 00, 01, 11, 10,
and for n = 3 the list is 000, 001, 011, 010, 110, 111, 101, 100.

96. Show that every n-bit string appears exactly once in the list generated
by the algorithm.

97. Show that the list has the Gray code property, that is, that each string
differs from the previous one in exactly one bit.

###### 2.14 HINTS

37. You will need to use strong induction. And your base case may not be what
you expect at first,

48. Try combining four n/2 _n/2 tours into one. Your induction hypothesis must_
_×_
be stronger than what you really need to prove — the tours you build must
have some extra structure to allow them to be joined at the corners.

49. Look carefully at the example given before the problem. It illustrates the
technique that you will need. Also, consider the hint to Problem 48.

53. You will need to use strong induction here.


57. You will need to use the identity

� _n_ � � _n_ 1

= _−_

_r_ _r_


� � _n_ 1
+ _−_
_r_ 1
_−_


�
_._


(Can you prove this identity?) Be careful how you apply this identity (it
doesn’t always hold), and take special care with the upper and lower limits
of the summation.

69. First, prove that any graph in which all vertices have even degree must have a
cycle C (try constructing one). Delete C, leaving a smaller graph in which all
vertices have even degree. Apply the induction hypothesis (careful: there is
something I am not telling you). Put together C and the results of applying
the induction hypothesis to give the Eulerian cycle.

85. The circles are a red herring.

86. The hardest part of this is the base case, proving that the sum of the three
angles of a triangle is 180 degrees. It can be proved as follows. First, prove


-----

Sec. 2.15. Solutions **21**

it for a right-angled triangle (using symmetry). This can be extended to any
triangle by judicious choice of diagonal. Once you have mastered the base
case, the inductive step should be obvious.

92. You’ll need to make two cases in your inductive step, according to whether n
is a power of 2 (or something like that) or not.

###### 2.15 SOLUTIONS

1. We are required to prove that for all n ≥ 0, _i=1_ _[i][ =][ n][(][n][ + 1)][/][2. The claim]_

[�][n]
is certainly true for n = 0, in which case both sides of the equation are zero.
Suppose that n ≥ 0 and _i=1_ _[i][ =][ n][(][n][ + 1)][/][2. We are required to prove that]_
�n+1 [�][n]
_i=1_ _[i][ = (][n][ + 1)(][n][ + 2)][/][2. Now,]_


_n+1_
� _i_ =

_i=1_


_n_
� _i + (n + 1)_

_i=1_


= _n(n + 1)/2 + (n + 1)_ (by the induction hypothesis)
= (n + 1)(n + 2)/2,

as required.

8. We are required to prove that for all n ≥ 1, _i=1_ [1][/][2][i][ = 1][ −] [1][/][2][n][. The claim]

[�][n]
is true for n = 1, since in this case both sides of the equation are equal to
1/2. Now suppose that n ≥ 1, and _i=1_ [1][/][2][i][ = 1] _[−]_ [1][/][2][n][. It remains to prove]

[�][n]
that [�][n]i=1[+1] [1][/][2][i][ = 1][ −] [1][/][2][n][+1][.]


_n+1_

1 1

� 1/2[i] =

2 [+ 1]4 [+ 1]8 [+][ · · ·][ +] 2[n][+1]
_i=1_


�


1
=
2 [+ 1]2


� 1

2 [+ 1]4 [+ 1]8 [+][ · · ·][ + 1]2[n]


_n_

1 1
= �
2 [+ 1]2 2[i]

_i=1_

1

(by the induction hypothesis)

_−_
2 [+ 1]2 2[n][ )]

_[·][ (1][ −]_ [1]

= 1 1/2[n][+1],
_−_

as required.

11. We are required to prove that for all n ≥ 0, _i=0_ [2][i][ = 2][n][+1][ −] [1.] The

[�][n]
claim is certainly true for n = 0, in which case [�]i[0]=0 [2][i][ = 1 = 2][1][ −] [1.]
Suppose that n ≥ 0 and _i=0_ [2][i][ = 2][n][+1][ −] [1. We are required to prove that]

[�][n]


-----

**22** Chap. 2. Mathematical Induction

�n+1
_i=0_ [2][i][ = 2][n][+2][ −] [1. Now,]


_n+1_
� 2[i] =

_i=0_


_n_
� 2[i] + 2[n][+1]

_i=0_


= (2[n][+1] 1) + 2[n][+1] (by the induction hypothesis)
_−_
= 2[n][+2] 1,
_−_

as required.

27. We are required to prove by induction on n 0 that n[3] + 2n is divisible by
_≥_
3. The claim is true for n = 0, since then n[3] + 2n = 0, which is certainly
divisible by 3. Suppose that n 0, and n[3] + 2n is divisible by 3. We are
_≥_
required to prove that (n + 1)[3] + 2(n + 1) is divisible by 3. Now,

(n + 1)[3] + 2(n + 1) = (n[3] + 3n[2] + 3n + 1) + (2n + 2)
= _n[3]_ + 3n[2] + 5n + 3
= (n[3] + 2n) + (3n[2] + 3n + 3).

Since the first term is divisible by 3 (by the induction hypothesis) and the
second term is obviously divisible by 3, it follows that (n + 1)[3] + 2(n + 1) is
divisible by 3, as required.

37. We are required to show that any amount of postage that is a positive integer
number of cents n > 7 can be formed by using only 3-cent and 5-cent stamps.
The claim is certainly true for n = 8 (one 3-cent and one 5-cent stamp), n = 9
(three 3-cent stamps), and n = 10 (two 5-cent stamps). Now suppose that
_n_ 11 and all values up to n 1 cents can be made with 3-cent and 5-cent
_≥_ _−_
stamps. Since n 11, n 3 8, and hence by hypothesis, n 3 cents can
_≥_ _−_ _≥_ _−_
be made with 3-cent and 5-cent stamps. Simply add a 3-cent stamp to this
to make n cents. Notice that we can prove something stronger with just a
little more work. The required postage can always be made using at most
two 5-cent stamps. Can you prove this?

52. We are required to prove that for all n ≥ 0, _i=0_ _[F][i][ =][ F][n][+2][ −]_ [1. The claim]

[�][n]
is certainly true for n = 0, since the left-hand side of the equation is F0 = 0,
and the right-hand side is F2 − 1 = 1 − 1 = 0. Now suppose that n ≥ 1, and
that [�][n]i=0[−][1] _[F][i][ =][ F][n][+1][ −]_ [1. Then,]


_n_
� _Fi_ =

_i=0_


_n−1_
�

_Fi + Fn_
_i=0_


= (Fn+1 − 1) + Fn (by the induction hypothesis)
= _Fn+2 −_ 1,


as required.


-----

Sec. 2.16. Comments **23**

_L_

**Figure 2.6. Shading the regions formed by all lines except**
_L (top), and the new shading obtained by flipping the colors_
on one side of L (bottom).

84. We are required to prove that any set of regions defined by n lines in the
plane can be colored with only two colors so that no two regions that share
an edge have the same color. The hypothesis is true for n = 1 (color one side
light, the other side dark). Now suppose that the hypothesis is true for n
lines. Suppose we are given n + 1 lines in the plane. Remove one of the lines
_L, and color the remaining regions with two colors (which can be done, by_
the induction hypothesis). Replace L. Reverse all of the colors on one side
of the line. Consider two regions that have a line in common. If that line is
not L, then by the induction hypothesis, the two regions have different colors
(either the same as before or reversed). If that line is L, then the two regions
formed a single region before L was replaced. Since we reversed colors on one
side of L only, they now have different colors.

###### 2.16 COMMENTS

1. This identity was apparently discovered by Gauss at age 9 in 1786. There is
an apocryphal story attached to this discovery. Gauss’ teacher set the class
to add the numbers 1 + 2 + + 100. One account I have heard said that the
_· · ·_
teacher was lazy, and wanted to occupy the students for a long time so that
he could read a book. Another said that it was punishment for the class being
unruly and disruptive. Gauss came to the teacher within a few minutes with
an answer of 5050. The teacher was dismayed, and started to add. Some time
later, after some fretting and fuming, he came up with the wrong answer. He
refused to believe that he was wrong until Gauss explained:

|Col1|L|
|---|---|


-----

**24** Chap. 2. Mathematical Induction

1 + 2 + + 50

_· · ·_
+ 100 + 99 + + 51

_· · ·_

101 + 101 + + 101 = 50 101 = 5050.

_· · ·_ _×_
Can you prove this result without using induction? The case for even n can
easily be inferred from Gauss’ example. The case for odd n is similar.


3. I could go on asking for more identities like this. I can never remember the
exact form of the solution. Fortunately, there is not much need to. In general,
if you are asked to solve
_n_
�

_i[k]_

_i=1_

for some k 1, just remember that the solution is a polynomial in n with
_≥_
largest exponent k + 1 (see Problem 21). Simply hypothesize that the sum is

_ak+1n[k][+1]_ + akn[k] + · · · + a1n + a0

for some choice of ai ∈ IR, 0 ≤ _i ≤_ _k + 1, and try to prove it by induction._
The right values for the constants will drop right out of the proof. It gets a
bit tricky as k becomes larger, though. If you want to practice this technique,
start with k = 2. If you want a challenge to your ability to do arithmetic, try
_k = 4._

4. Yes, I realize that you can solve this without induction by applying some
elementary algebra and the identities of Problems 1 and 2. What I want you
to do is practice your induction by proving this identity from first principles.

5. See the comment to Problem 4.

6. See the comment to Problem 4.

9. There is an elegant noninductive proof of this that you should have met in
high school. Let S = [�]i[n]=0 _[a][i][. Then,]_

_n+1_ _n_

_aS_ _S =_ � _a[i]_ � _a[i]_ = a[n][+1] 1.
_−_ _−_ _−_

_i=1_ _i=0_

Hence, S = (a[n][+1] 1)/(a 1), as required.
_−_ _−_

10. This can also be solved by applying the identity of Problem 9 twice.

11. This is a special case of the identity in Problem 9. There is an easy noninductive proof of this fact that appeals more to computer science students than
math students. The binary representation of [�]i[n]=0 [2][i][ is a string of][ n] [+1 ones,]
that is,
11 1 _._
_· · ·_
����n+1


-----

Sec. 2.16. Comments **25**

2[n-1] 2[n-1]

_n-1_

_n_

2[n]

**Figure 2.7.** Using the method of areas to show that
�n
_i=1_ _[i][2][i][ = (2][n][ −]_ [1)2][n][ −] [�]i[n]=1[−][1] [2][i][.]

If you add 1 to this, you get, in binary,

1 00 0,
_· · ·_
����n+1

that is, 2[n][+1]. Therefore, _i=0_ [2][i][ + 1 = 2][n][+1][ or, equivalently,][ �]i[n]=0 [2][i][ =]

[�][n]
2[n][+1] 1.
_−_

13. There is an elegant noninductive proof of this using the method of areas. This
technique works well for sums of products: Simply make a rectangle with area
equal to each term of the sum, fit them together to “nearly” make a rectangle,
and analyze the missing area.

_n_ _n−1_
� _i2[i]_ = (2n 1)2[n] � 2[i] (see Figure 2.7)

_−_ _−_
_i=1_ _i=1_

= (2n 1)2[n] (2[n] 2) (by Problem 1)
_−_ _−_ _−_
= (n 1)2[n][+1] + 2.
_−_

15. This can also be solved using the method of areas sketched in the comment
to Problem 13.

16. This can also be solved using algebra and the identity from Problem 15.

19. And, therefore, 3[n] = O(n!). But we’re getting ahead of ourselves here. See
Chapter 3.

20. And, therefore, 2[n] = Ω(n[2]). But we’re getting ahead of ourselves here. See
Chapter 3.

48. There are actually closed knight’s tours on n _n chessboards for all even_
_×_
_n_ 6 (see Problem 369). Note that Problem 47 implies that there can be no
_≥_
such tour for odd n. The formal study of the knight’s tour problem is said


-----

**26** Chap. 2. Mathematical Induction

to have begun with Euler [25] in 1759, who considered the standard 8 8
_×_
chessboard. Rouse Ball and Coxeter [8] give an interesting bibliography of
the history of the problem from this point.

51. This problem was suggested to the author by Nainan Kovoor in 1990.

60. Don’t cheat by using Stirling’s approximation. You’re supposed to be practicing your induction!

61. See the comment for Problem 60.

62. There is an elegant noninductive proof of the identity


_n_ � _n_
�

_i_
_·_ _i_
_i=0_


�
= n2[n][−][1].


� _n_ �
Write down every string of n bits. Since there are _i_ strings with exactly
_i ones, you must have written exactly_


_n_ � _n_
�

_i_
_·_ _i_
_i=0_


�


ones. But since you have written exactly as many ones as zeros, and you have
written n2[n] bits in all, there must be n2[n][−][1] ones.

64. Of course it is obvious that the proof is wrong, since all horses are not of the
same color. What I want you to do is point out where in the proof is there a
false statement made?

67. This can be proved using Problem 1, but what I’m looking for is a straightforward inductive proof.

69. An Eulerian cycle is not possible if the graph has at least one vertex of odd
degree. (Can you prove this?) Therefore, we conclude that a graph has a
Eulerian cycle iff it is connected and all vertices have even degree. The Swiss
mathematician Leonhard Euler first proved this in 1736 [24].

81. This problem together with Problem 82 show that “a connected graph with
no cycles” is an alternate definition of a tree. You’ll see this in the literature as often as you’ll see the recursive definition given at the beginning of
Section 2.11.

82. See the comment for Problem 81.


-----

Sec. 2.16. Comments **27**

94. Yes, this is a little contrived. It’s easier to prove by contradiction. But it’s
good practice in using induction.

95. See also Problems 415 and 471.


-----

###### Chapter 3

### Big-O and Big-Ω

Big-O notation is useful for the analysis of algorithms since it captures the asymptotic growth pattern of functions and ignores the constant multiple (which is out
of our control anyway when algorithms are translated into programs). We will use
the following definitions (although alternatives exist; see Section 3.5). Suppose that
_f, g_ : IN IN.
_→_

_• f_ (n) is O(g(n)) if there exists c, n0 ∈ IR[+] such that for all n ≥ _n0, f_ (n) ≤
_c_ _g(n)._
_·_

_• f_ (n) is Ω(g(n)) if there exists c, n0 ∈ IR[+] such that for all n ≥ _n0, f_ (n) ≥
_c_ _g(n)._
_·_
_f_ (n) is Θ(g(n)) if f (n) is O(g(n)) and f (n) is Ω(g(n)).

_•_

_• f_ (n) is o(g(n)) if limn→∞ _f_ (n)/g(n) = 0.

_• f_ (n) is ω(g(n)) if limn→∞ _g(n)/f_ (n) = 0.

_• f_ (n) ∼ _g(n) if limn→∞_ _f_ (n)/g(n) = 1.

We will follow the normal convention of writing, for example, “f (n) = O(g(n))”
instead of “f (n) is O(g(n))”, even though the equality sign does not indicate true
equality. The proper definition of “O(g(n))” is as a set:

_O(g(n)) = {f_ (n) | there exists c, n0 ∈ IR[+] such that for all n ≥ _n0, f_ (n) ≤ _c · g(n)}._

Then, “f (n) = O(g(n))” can be interpreted as meaning “f (n) _O(g(n)).”_
_∈_

###### 3.1 RANK THE FUNCTIONS

98. Consider the following eighteen functions:


_√_
_n_ _n_ 2[n]

_n log n_ _n_ _n[3]_ + 7n[5] _n[2]_ + log n
_−_
_n[2]_ _n[3]_ log n
_n[1][/][3]_ + log n (log n)[2] _n!_
ln n _n/ log n_ log log n
(1/3)[n] (3/2)[n] 6


**28**


-----

Sec. 3.1. Rank the Functions **29**

Group these functions so that f (n) and g(n) are in the same group if and
only if f (n) = O(g(n)) and g(n) = O(f (n)), and list the groups in increasing
order.

99. Draw a line from each of the five functions in the center to the best
big-Ωvalue on the left, and the best big-O value on the right.

Ω(1/n) _O(1/n)_
Ω(1) _O(1)_
Ω(log log n) _O(log log n)_
Ω(log n) _O(log n)_
Ω(log[2] _n)_ _O(log[2]_ _n)_
Ω([√][3] _n)_ _O([√][3]_ _n)_
Ω(n/ log n) 1/(log n) _O(n/ log n)_
Ω(n) 7n[5] 3n + 2 _O(n)_
_−_
Ω(n[1][.][00001]) (n[2] + n)/(log[2] _n + log n)_ _O(n[1][.][00001])_
Ω(n[2]/ log[2] _n)_ 2[log][2][ n] _O(n[2]/ log[2]_ _n)_
Ω(n[2]/ log n) 3[n] _O(n[2]/ log n)_
Ω(n[2]) _O(n[2])_
Ω(n[3][/][2]) _O(n[3][/][2])_
Ω(2[n]) _O(2[n])_
Ω(5[n]) _O(5[n])_
Ω(n[n]) _O(n[n])_
Ω(n[n][2]) _O(n[n][2])_

For each of the following pairs of functions f (n) and g(n), either f (n) = O(g(n))
or g(n) = O(f (n)), but not both. Determine which is the case.

100. _f_ (n) = (n[2] _n)/2, g(n) = 6n._
_−_

101. _f_ (n) = n + 2[√]n, g(n) = n[2].

102. _f_ (n) = n + log n, g(n) = n[√]n.

103. _f_ (n) = n[2] + 3n + 4, g(n) = n[3].

104. _f_ (n) = n log n, g(n) = n[√]n/2.

105. _f_ (n) = n + log n, g(n) = _n._

_[√]_

106. _f_ (n) = 2(log n)[2], g(n) = log n + 1.

107. _f_ (n) = 4n log n + n, g(n) = (n[2] _n)/2._
_−_


-----

**30** Chap. 3. Big-O and Big-Ω

###### 3.2 TRUE OR FALSE?

108. _n[2]_ = O(n[3]).

109. _n[3]_ = O(n[2]).

110. 2n[2] + 1 = O(n[2]).

111. _n log n = O(n[√]n)._

_√_
112. _n = O(log n)._

113. log n = O([√]n).

114. _n[3]_ = O(n[2](1 + n[2])).

115. _n[2](1 +_ _[√]n) = O(n[2])._

116. _n[2](1 +_ _n) = O(n[2]_ log n).

_[√]_

117. 3n[2] + _[√]n = O(n[2])._

118. 3n[2] + _n = O(n + n[√]n +_ _n)._

_[√]_ _[√]_

119. log n + _n = O(n)._

_[√]_

_√_
120. _n log n = O(n)._

121. 1/n = O(log n).

122. log n = O(1/n).

123. log n = O(n[−][1][/][2]).

124. _n +_ _n = O([√]n log n)._

_[√]_

125. If f (n) _g(n), then f_ (n) = Θ(g(n)).
_∼_

126. If f (n) = Θ(g(n)), then g(n) = Θ(f (n)).

For each of the following pairs of functions f (n) and g(n), state whether f (n) =
_O(g(n)), f_ (n) = Ω(g(n)), f (n) = Θ(g(n)), or none of the above.

127. _f_ (n) = n[2] + 3n + 4, g(n) = 6n + 7.

128. _f_ (n) = _n, g(n) = log(n + 3)._

_[√]_

129. _f_ (n) = n[√]n, g(n) = n[2] _n._
_−_

130. _f_ (n) = n + n[√]n, g(n) = 4n log(n[2] + 1).

131. _f_ (n) = (n[2] + 2)/(1 + 2[−][n]), g(n) = n + 3.

132. _f_ (n) = 2[n] _n[2], g(n) = n[4]_ + n[2].
_−_


-----

Sec. 3.3. Proving Big-O **31**

###### 3.3 PROVING BIG-O

133. Prove that (n + 1)[2] = O(n[2]).

134. Prove that 3n[2] 8n + 9 = O(n[2]).
_−_

135. Prove that for all k ≥ 1 and all ak, ak−1, . . ., a1, a0 ∈ IR,

_akn[k]_ + ak−1n[k][−][1] + · · · + a1n + a0 = O(n[k]).

136. Prove that log n = O(n).
_⌈_ _⌉_

137. Prove that 3n log n = O(n[2]).
_⌊_ _⌋_

138. Prove that n[2] 3n 18 = Ω(n).
_−_ _−_

139. Prove that n[3] 3n[2] _n + 1 = Θ(n[3])._
_−_ _−_

140. Prove that n = O(2[n]).

141. Prove that 2n + 1 = O(2[n]).

142. Prove that 9999n + 635 = O(2[n]).

143. Prove that cn + d = O(2[n]) for all c, d IR[+].
_∈_

144. Prove that n[2] = O(2[n]).

145. Prove that cn[2] + d = O(2[n]) for all c, d IR[+].
_∈_

146. Prove that cn[k] + d = O(2[n]) for all c, d, k IR[+].
_∈_

147. Prove that 2[n] = O(n!).

148. Prove that n! = Ω(2[n]).

149. Does n[log][ n] = O((log n)[n])? Prove your answer.

150. Does n[log][ n] = Ω((log n)[n])? Prove your answer.

151. Does n[log log log][ n] = O((log n)!)? Prove your answer.

152. Does n[log log log][ n] = Ω((log n)!)? Prove your answer.

153. Does (n!)! = O(((n 1)!)!(n 1)![n][!])? Prove your answer.
_−_ _−_

154. Does (n!)! = Ω(((n 1)!)!(n 1)![n][!])? Prove your answer.
_−_ _−_

155. Prove or disprove:


= O( _n_ ).
_⌊[√]_ _⌋_


_O_


�� _n[2]_

log log n


1/2[�]
�


-----

**32** Chap. 3. Big-O and Big-Ω

156. Prove or disprove: 2[(1+][O][(1][/n][))][2] = 2 + O(1/n).

Compare the following pairs of functions f, g. In each case, say whether f = o(g),
_f = ω(g), or f = Θ(g), and prove your claim._

157. _f_ (n) = 100n + log n, g(n) = n + (log n)[2].

158. _f_ (n) = log n, g(n) = log log(n[2]).

159. _f_ (n) = n[2]/log n, g(n) = n(log n)[2].

160. _f_ (n) = (log n)[10][6], g(n) = n[10][−][6].

161. _f_ (n) = n log n, g(n) = (log n)[log][ n].

162. _f_ (n) = n2[n], g(n) = 3[n].

For each of the following pairs of functions f (n) and g(n), find c IR[+] such that
_∈_
_f_ (n) _c_ _g(n) for all n > 1._
_≤_ _·_

163. _f_ (n) = n[2] + n, g(n) = n[2].

164. _f_ (n) = 2[√]n + 1, g(n) = n + n[2].

165. _f_ (n) = n[2] + n + 1, g(n) = 2n[3].

166. _f_ (n) = n[√]n + n[2], g(n) = n[2].

167. _f_ (n) = 12n + 3, g(n) = 2n 1.
_−_

168. _f_ (n) = n[2] _n + 1, g(n) = n[2]/2._
_−_

169. _f_ (n) = 5n + 1, g(n) = (n[2] 6n)/2.
_−_

170. _f_ (n) = 5 _n_ 1, g(n) = n _n_ .
_⌊[√]_ _⌋−_ _−⌈[√]_ _⌉_

###### 3.4 MANIPULATING BIG-O

171. Prove that if f1(n) = O(g1(n)) and f2(n) = O(g2(n)), then
_f1(n) + f2(n) = O(g1(n) + g2(n))._

172. Prove that if f1(n) = Ω(g1(n)) and f2(n) = Ω(g2(n)), then f1(n) +
_f2(n) = Ω(g1(n) + g2(n))._

173. Prove that if f1(n) = O(g1(n)) and f2(n) = O(g2(n)), then f1(n)+
_f2(n) = O(max{g1(n), g2(n)})._


-----

Sec. 3.5. Alternative Definitions **33**

174. Prove that if f1(n) = Ω(g1(n)) and f2(n) = Ω(g2(n)), then f1(n) +
_f2(n) = Ω(min{g1(n), g2(n)})._

175. Suppose that f1(n) = Θ(g1(n)) and f2(n) = Θ(g2(n)). Is it true
that f1(n) + f2(n) = Θ(g1(n) + g2(n))? Is it true that f1(n) + f2(n) =
Θ(max{g1(n), g2(n)})? Is it true that f1(n) + f2(n) = Θ(min{g1(n), g2(n)})?
Justify your answer.

176. Prove that if f1(n) = O(g1(n)) and f2(n) = O(g2(n)), then f1(n) ·
_f2(n) = O(g1(n) · g2(n))._

177. Prove that if f1(n) = Ω(g1(n)) and f2(n) = Ω(g2(n)), then f1(n)·f2(n) =
Ω(g1(n) · g2(n)).

178. Prove or disprove: For all functions f (n) and g(n), either f (n) =
_O(g(n)) or g(n) = O(f_ (n)).

179. Prove or disprove: If f (n) > 0 and g(n) > 0 for all n, then O(f (n) +
_g(n)) = f_ (n) + O(g(n)).

180. Prove or disprove: O(f (n)[α]) = O(f (n))[α] for all α IR[+].
_∈_

181. Prove or disprove: O(x + y)[2] = O(x[2]) + O(y[2]).

182. Multiply log n + 6 + O(1/n) by n + O([√]n) and simplify your answer as
much as possible.

183. Show that big-O is transitive. That is, if f (n) = O(g(n)) and g(n) =
_O(h(n)), then f_ (n) = O(h(n)).

184. Prove that if f (n) = O(g(n)), then f (n)[k] = O(g(n)[k]).

185. Prove or disprove: If f (n) = O(g(n)), then 2[f] [(][n][)] = O(2[g][(][n][)]).

186. Prove or disprove: If f (n) = O(g(n)), then log f (n) = O(log g(n)).

187. Suppose f (n) = Θ(g(n)). Prove that h(n) = O(f (n)) iff h(n) = O(g(n)).

188. Prove or disprove: If f (n) = O(g(n)), then f (n)/h(n) = O(g(n)/h(n)).

###### 3.5 ALTERNATIVE DEFINITIONS

Here is an alternative definition of O.

_• f_ (n) is O1(g(n)) if there exists c ∈ IR such that limn→∞ _f_ (n)/g(n) = c.

189. Prove that if f (n) = O(g(n)), then f (n) = O1(g(n)), or find a counterexample to this claim.


-----

**34** Chap. 3. Big-O and Big-Ω

190. Prove that if f (n) = O1(g(n)), then f (n) = O(g(n)), or find a counterexample to this claim.

Here are two alternative definitions of Ω.

_• f_ (n) is Ω1(g(n)) if there exists c ∈ IR[+] such that for infinitely many n, f (n) ≥
_c_ _g(n)._
_·_

_• f_ (n) is Ω2(g(n)) if there exists c ∈ IR[+] such that for all n0 ∈ IN, there exists
_n ≥_ _n0 such that f_ (n) ≥ _c · g(n)._

191. Prove that if f (n) = Ω(g(n)), then f (n) = Ω2(g(n)), or find a counterexample to this claim.

192. Prove that if f (n) = Ω2(g(n)), then f (n) = Ω(g(n)), or find a counterexample to this claim.

193. Prove that if f (n) = Ω1(g(n)), then f (n) = Ω2(g(n)), or find a counterexample to this claim.

194. Prove that if f (n) = Ω2(g(n)), then f (n) = Ω1(g(n)), or find a counterexample to this claim.

195. Prove or disprove: If f (n) = O(g(n)), then f (n) = Ω(g(n)). If
_̸_
_f_ (n) ̸= O(g(n)), then f (n) = Ω2(g(n)).

196. Define the relation by f (n) _g(n) iff f_ (n) = Ω(g(n)) and g(n) =
_≡_ _≡_
Ω(f (n)). Similarly, define the relation ≡2 by f (n) ≡ _g(n) iff f_ (n) = Ω2(g(n))
and g(n) = Ω2(f (n)). Show that ≡ is an equivalence relation, but ≡2 is not
an equivalence relation.

###### 3.6 FIND THE FUNCTIONS

Find two functions f (n) and g(n) that satisfy the following relationships. If no such
_f and g exist, write “None.”_

197. _f_ (n) = o(g(n)) and f (n) = Θ(g(n)).
_̸_

198. _f_ (n) = Θ(g(n)) and f (n) = o(g(n)).

199. _f_ (n) = Θ(g(n)) and f (n) = O(g(n)).
_̸_

200. _f_ (n) = Ω(g(n)) and f (n) = O(g(n)).
_̸_

201. _f_ (n) = Ω(g(n)) and f (n) = o(g(n)).
_̸_


-----

Sec. 3.7. Hints **35**

###### 3.7 HINTS

98. There are a lot of groups.

99. Be careful with (n[2] + n)/(log[2] _n + log n)._

136. When solving problems that require you to prove that f (n) = O(g(n)), it is a
good idea to try induction first. That is, pick a c and an n0, and try to prove
that for all n ≥ _n0, f_ (n) ≤ _c · g(n). Try starting with n0 = 1. A good way_
of guessing a value for c is to look at f (n) and g(n) for n = n0, · · ·, n0 + 10.
If the first function seems to grow faster than the second, it means that you
must adjust your n0 higher — eventually (unless the thing you are trying to
prove is false), the first function will grow more slowly than the second. The
ratio of f (n0)/g(n0) gives you your first cut for c. Don’t be afraid to make c
higher than this initial guess to help you make it easier to prove the inductive
step. This happens quite often. You might even have to go back and adjust
_n0 higher to make things work out correctly._

171. Start by writing down the definitions for f1(n) = O(g1(n)) and f2(n) =
_O(g2(n))._

###### 3.8 SOLUTIONS

133. We are required to prove that (n + 1)[2] = O(n[2]). We need to find a constant
_c such that (n + 1)[2]_ _cn[2]. That is, n[2]_ + 2n + 1 _cn[2]_ or, equivalently,
_≤_ _≤_
(c 1)n[2] 2n 1 0. Is this possible? It is if c > 1. Take c = 4. The roots
_−_ _−_ _−_ _≥_
of 3n[2] 2n 1 are (2 4 + 12)/2 = 1/3, 1 . The second root gives us
_−_ _−_ _± [√]_ _{−_ _}_
the correct value for n0. Therefore, for all n ≥ 1, (n + 1)[2] _≤_ 4n[2], and so by
definition, (n + 1)[2] = O(n[2]).

136. We are required to prove that log n = O(n). By looking at log n for
_⌈_ _⌉_ _⌈_ _⌉_
small values of n, it appears that for all n 1, log n _n. The proof is_
_≥_ _⌈_ _⌉≤_
by induction on n. The claim is certainly true for n = 1. Now suppose that
_n > 1, and_ log(n 1) _n_ 1. Then,
_⌈_ _−_ _⌉≤_ _−_

log n log(n 1) + 1
_⌈_ _⌉_ _≤_ _⌈_ _−_ _⌉_
(n 1) + 1 (by the induction hypothesis)
_≤_ _−_
= _n._

Hence, we can take c = 1 and n0 = 1.

137. We are required to prove that 3n log n = O(n[2]). By looking at 3n log n for
_⌊_ _⌋_ _⌊_ _⌋_
small values of n, it appears that for all n 1, 3n log n 3n[2]. The proof is
_≥_ _⌊_ _⌋≤_
by induction on n. The claim is certainly true for n = 1. Now suppose that


-----

**36** Chap. 3. Big-O and Big-Ω

_n > 1, and 3(n_ 1) log(n 1) 3(n 1)[2]. Then,
_−_ _⌊_ _−_ _⌋≤_ _−_

3n log n
_⌊_ _⌋_
3n( log(n 1) + 1)
_≤_ _⌊_ _−_ _⌋_
= 3(n 1)( log(n 1) + 1) + 3( log(n 1) + 1)
_−_ _⌊_ _−_ _⌋_ _⌊_ _−_ _⌋_
= 3(n 1) log(n 1) + 3(n 1) + 3( log(n 1) + 1)
_−_ _⌊_ _−_ _⌋_ _−_ _⌊_ _−_ _⌋_
3(n 1)[2] + 3(n 1) + 3( log(n 1) + 1)
_≤_ _−_ _−_ _⌊_ _−_ _⌋_
(by the induction hypothesis)
3(n 1)[2] + 3(n 1) + 3n (see the solution to Problem 136)
_≤_ _−_ _−_
= 3n[2] 6n + 3 + 3n 3 + 3n
_−_ _−_
= 3n[2].

Hence, we can take c = 3 and n0 = 1.

171. We are required to prove that if f1(n) = O(g1(n)) and f2(n) = O(g2(n)), then
_f1(n)+f2(n) = O(g1(n)+g2(n)). Suppose for all n ≥_ _n1, f1(n) ≤_ _c1·g1(n) and_
for all n ≥ _n2, f2(n) ≤_ _c2_ _·g2(n). Let n0 = max{n1, n2} and c0 = max{c1, c2}._
Then for all n ≥ _n0, f1(n)+_ _f2(n) ≤_ _c1 ·_ _g1(n)+_ _c2 ·_ _g2(n) ≤_ _c0(g1(n)+_ _g2(n))._

###### 3.9 COMMENTS

173. This is often called the sum rule for big-Os.

176. This is often called the product rule for big-Os.


-----

###### Chapter 4

### Recurrence Relations

Recurrence relations are a useful tool for the analysis of recursive algorithms, as we
will see later in Section 6.2. The problems in this chapter are intended to develop
skill in solving recurrence relations.

###### 4.1 SIMPLE RECURRENCES

Solve the following recurrences exactly.

202. _T_ (1) = 1, and for all n 2, T (n) = 3T (n 1) + 2.
_≥_ _−_

203. _T_ (1) = 8, and for all n 2, T (n) = 3T (n 1) 15.
_≥_ _−_ _−_

204. _T_ (1) = 2, and for all n 2, T (n) = T (n 1) + n 1.
_≥_ _−_ _−_

205. _T_ (1) = 3, and for all n 2, T (n) = T (n 1) + 2n 3.
_≥_ _−_ _−_

206. _T_ (1) = 1, and for all n 2, T (n) = 2T (n 1) + n 1.
_≥_ _−_ _−_

207. _T_ (1) = 5, and for all n 2, T (n) = 2T (n 1) + 3n + 1.
_≥_ _−_

208. _T_ (1) = 1, and for all n 2 a power of 2, T (n) = 2T (n/2) + 6n 1.
_≥_ _−_

209. _T_ (1) = 4, and for all n 2 a power of 2, T (n) = 2T (n/2) + 3n + 2.
_≥_

210. _T_ (1) = 1, and for all n 2 a power of 6, T (n) = 6T (n/6) + 2n + 3.
_≥_

211. _T_ (1) = 3, and for all n 2 a power of 6, T (n) = 6T (n/6) + 3n 1.
_≥_ _−_

212. _T_ (1) = 3, and for all n 2 a power of 3, T (n) = 4T (n/3) + 2n 1.
_≥_ _−_

213. _T_ (1) = 2, and for all n 2 a power of 3, T (n) = 4T (n/3) + 3n 5.
_≥_ _−_

214. _T_ (1) = 1, and for all n 2 a power of 2, T (n) = 3T (n/2) + n[2] _n._
_≥_ _−_

215. _T_ (1) = 4, and for all n 2 a power of 2, T (n) = 3T (n/2) + n[2] 2n + 1.
_≥_ _−_

216. _T_ (1) = 1, and for all n 2 a power of 2, T (n) = 3T (n/2) + n 2.
_≥_ _−_

**37**


-----

**38** Chap. 4. Recurrence Relations

217. _T_ (1) = 1, and for all n 2 a power of 2, T (n) = 3T (n/2) + 5n 7.
_≥_ _−_

218. _T_ (1) = 1, and for all n 2 a power of 3, T (n) = 4T (n/3) + n[2].
_≥_

219. _T_ (1) = 1, and for all n 2 a power of 3, T (n) = 4T (n/3) + n[2] 7n + 5.
_≥_ _−_

220. _T_ (1) = 1, and for n 4 a power of 4, T (n) = T (n/4) + _n + 1._
_≥_ _[√]_

###### 4.2 MORE DIFFICULT RECURRENCES

221. Suppose 0 < α, β < 1, where α + β = 1. Let T (1) = 1, and for all
_n_ 1, T (n) = T (αn) + T (βn) + cn, for some c IN. Prove that T (n) =
_≥_ _∈_
_O(n log n). You may make any necessary assumptions about n._

222. The Fibonacci numbers Fn for n ≥ 0 are defined recursively as
follows: F0 = 0, F1 = 1, and for n ≥ 2, Fn = Fn−1 +Fn−2. Prove by induction
_√_ _√_ _√_
on n that Fn = (φ[n] _−_ _φ[ˆ][n])/_ 5, where φ = (1 + 5)/2, and φ[ˆ] = (1 − 5)/2.

Let X(n) be the number of different ways of parenthesizing the product of n values.
For example, X(1) = X(2) = 1, X(3) = 2 (they are (xx)x and x(xx)), and X(4) = 5
(they are x((xx)x), x(x(xx)), (xx)(xx), ((xx)x)x, and (x(xx))x).

223. Prove that if n 2, then X(n) = 1; and otherwise
_≤_


_X(n) =_


_n−1_
� _X(k)_ _X(n_ _k)_

_·_ _−_
_k=1_


224. Show that for all n 1, X(n) 2[n][−][2].
_≥_ _≥_

225. Show that


�
_._


_X(n) = [1]_

_n_


� 2n 2
_−_
_n_ 1
_−_


Solve the following recurrences exactly.

226. _T_ (1) = 1, T (2) = 6, and for all n 3, T (n) = T (n 2)+3n+4.
_≥_ _−_

227. _T_ (0) = c, T (1) = d, and for n > 1, T (n) = T (n 2) + n.
_−_

228. _T_ (1) = 1, T (2) = 6, T (3) = 13, and for all n 4,
_≥_

_T_ (n) = T (n 3) + 5n 9.
_−_ _−_

229. _T_ (1) = 1, and for all n 2, T (n) = 2T (n 1) + n[2] 2n + 1.
_≥_ _−_ _−_

230. _T_ (1) = 1, and for all n 2, T (n) = n _T_ (n 1) + n.
_≥_ _·_ _−_


-----

Sec. 4.3. General Formulae **39**

###### 4.3 GENERAL FORMULAE

It is normal to teach the general solution to recurrences of the form T (n) =
_aT_ (n/c) + bn (see, for example, Aho, Hopcroft, and Ullman [1, Theorem 1.1]).
The following are interesting variants of this recurrence.

231. State and prove a general formula for recurrences of the form

� _d_ if n 1
_T_ (n) = _≤_
_aT_ (n/c) + b otherwise.

232. State and prove a general formula for recurrences of the form

� _d_ if n 1
_T_ (n) = _≤_
_aT_ (n/c) + bn[2] otherwise.

233. State and prove a general formula for recurrences of the form

� _d_ if n 1
_T_ (n) = _≤_
_aT_ (n/c) + bn[k] otherwise.

234. Prove that the asymptotic solution of the recurrence relation

� 0 if 0 _n < c_
_T_ (n) = _≤_
2T (n _c) + k_ otherwise.
_−_

where c, k IN, is T (n) = Θ(d[n]) for some constant d.
_∈_

###### 4.4 RECURRENCES WITH FULL HISTORY

Solve the following recurrences exactly.

235. _T_ (1) = 1, and for all n 2,
_≥_


_T_ (n) =

236. _T_ (1) = 1, and for all n 2,
_≥_

_T_ (n) =


_n−1_
� _T_ (i) + 1.

_i=1_

_n−1_
� _T_ (i) + 7.

_i=1_


-----

**40** Chap. 4. Recurrence Relations

237. _T_ (1) = 1, and for all n 2,
_≥_


_T_ (n) =

238. _T_ (1) = 1, and for all n 2,
_≥_


_n−1_
� _T_ (i) + n[2].

_i=1_


_T_ (n) = 2

239. _T_ (1) = 1, and for all n 2,
_≥_


_n−1_
� _T_ (i) + 1.

_i=1_


_T_ (n) =


_n−1_
� _T_ (n _i) + 1._

_−_
_i=1_


240. _T_ (1) = 1, and for all n 2,
_≥_


_T_ (n) =


_n−1_
�(T (i) + T (n _i)) + 1._

_−_
_i=1_


###### 4.5 RECURRENCES WITH FLOORS AND CEILINGS

241. Suppose T (1) = 1, and for all n 2, T (n) = T ( _n/2_ ) + n 1. Show
_≥_ _⌊_ _⌋_ _−_
that 2n log n 1 _T_ (n) 2n log n _/2_ 1.
_−⌊_ _⌋−_ _≤_ _≤_ _−⌊_ _⌋_ _−_

242. Suppose T (1) = 1, and for all n 2, T (n) = T ( _n/2_ ) +
_≥_ _⌊_ _⌋_
_T_ ( _n/2_ ) + n 1. Find an exact solution for T (n).
_⌊_ _⌋_ _−_

243. Solve the following recurrence relation exactly. T (1) = 1 and for
all n 2, T (n) = T ( _n/2_ ) + 1.
_≥_ _⌊_ _⌋_

244. Solve the following recurrence relation exactly. T (1) = 1 and for all
_n_ 2, T (n) = T ( _n/2_ ) + 1.
_≥_ _⌈_ _⌉_

245. Solve the following recurrence relation exactly. T (1) = 1, and for
_n_ 2, T (n) = 2T ( _n/2_ ) + 6n 1.
_≥_ _⌊_ _⌋_ _−_

246. Solve the following recurrence relation exactly. T (1) = 2, and for all
_n_ 2, T (n) = 4T ( _n/3_ ) + 3n 5.
_≥_ _⌈_ _⌉_ _−_

247. Solve the following recurrence: T (1) = 1, and for all n 2, T (n) =
_≥_
_T_ ( _n_ ) + 1.
_⌊[√]_ _⌋_

248. Solve the following recurrence: T (1) = T (2) = 1, and for all
_n_ 3, T (n) = T ( _n/ log n_ ) + 1.
_≥_ _⌊_ _⌋_


-----

Sec. 4.6. Hints **41**

###### 4.6 HINTS

202. Try repeated substitution (see the comment to Problem 202 for a definition
of this term).

224. Use induction on n. The base case will be n 4.
_≤_

226. If you think about it, this is really two independent recurrence relations, one
for odd n and one for even n. Therefore, you will need to make a special case
for even n and one for odd n. Once you realize this, the recurrences in this
group of problems are fairly easy.

242. The solution is T (n) = n log n 2[⌈][log][ n][⌉]+1. This can be proved by induction.
_⌈_ _⌉−_
Can you derive this answer from first principles?

243. This problem is difficult to solve directly, but it becomes easy when you
use the following fact from Graham, Knuth, and and Patashnik [30, Section 6.6]. Suppose f : IR IR is continuous and monotonically increasing, and
_→_
has the property that if f (x) ZZ, then x ZZ. Then, _f_ ( _x_ ) = _f_ (x) and
_∈_ _∈_ _⌊_ _⌊_ _⌋_ _⌋_ _⌊_ _⌋_
_f_ ( _x_ ) = _f_ (x) .
_⌈_ _⌈_ _⌉_ _⌉_ _⌈_ _⌉_

248. The answer is that for n 3, T (n) 1.76 log n/ log log n, but this may not
_≥_ _≤_
help you much.

###### 4.7 SOLUTIONS

202. Suppose T (1) = 1, and for all n 2, T (n) = 3T (n 1) + 2. If n is large
_≥_ _−_
enough, then by repeated substitution,

_T_ (n) = 3T (n 1) + 2 (after one substitution)
_−_
= 3(3T (n 2) + 2) + 2
_−_
= 9T (n 2) + 2 3 + 2 (after two substitutions)
_−_ _·_
= 9(3T (n 3) + 2) + 2 3 + 2
_−_ _·_
= 27T (n 3) + 2 9 + 2 3 + 2 (after three substitutions).
_−_ _·_ _·_

It looks like there’s a pattern developing. After i substitutions,


_T_ (n) = 3[i]T (n _i) + 2_
_−_


_i−1_
� 3[j]. (4.1)

_j=0_


-----

**42** Chap. 4. Recurrence Relations

We can prove that identity (4.1) is true by induction on i. It is trivially true
for i = 1. Now suppose that i > 1 and that


_i−2_

_T_ (n) = 3[i][−][1]T (n _i + 1) + 2_ � 3[j].
_−_

_j=0_


Then,


_i−2_

_T_ (n) = 3[i][−][1]T (n _i + 1) + 2_ � 3[j]
_−_

_j=0_


= 3[i][−][1](3T (n _i) + 2) + 2_
_−_


_i−2_
� 3[j]

_j=0_


= 3[i]T (n _i) + 2_
_−_


_i−1_
� 3[j],

_j=0_


as required. Now that we’ve established identity (4.1), we can continue with
solving the recurrence. Suppose we take i = n 1. Then, by identity (4.1),
_−_

_n−2_

_T_ (n) = 3[n][−][1]T (1) + 2 � 3[j]

_j=0_

= 3[n][−][1] + 3[n][−][1] 1 (by Problem 9)
_−_
= 2 3[n][−][1] 1.
_·_ _−_

208. Suppose T (1) = 1, and for all n 2 a power of 2, T (n) = 2T (n/2) + 6n 1.
_≥_ _−_
If n is large enough, then by repeated substitution,

_T_ (n) = 2T (n/2) + 6n 1 (after one substitution)
_−_
= 2(2T (n/4) + 6n/2 1) + 6n 1
_−_ _−_
= 4T (n/4) + (6n 2) + (6n 1) (after two substitutions)
_−_ _−_
= 4(2T (n/8) + 6n/4 1) + (6n 2) + (6n 1)
_−_ _−_ _−_
= 8T (n/8) + (6n 4) + (6n 2) + (6n 1)
_−_ _−_ _−_
(after three substitutions).

Therefore, after i substitutions,


_T_ (n) = 2[i]T (n/2[i]) + 6in
_−_


_i−1_
� 2[j].

_j=0_


-----

Sec. 4.7. Solutions **43**

This can be verified easily by induction. Hence, taking i = log n,


_T_ (n) = _nT_ (1) + 6n log n
_−_


log n−1
� 2[j]

_j=0_


= _n + 6n log n_ (2[log][ n] 1) (by Problem 11)
_−_ _−_
= 6n log n + 1.

214. Suppose T (1) = 1, and for all n 2 a power of 2, T (n) = 3T (n/2) + n[2] _n._
_≥_ _−_
If n is large enough, then by repeated substitution,

_T_ (n) = 3T (n/2) + n[2] _n_ (after one substitution)
_−_
= 3(3T (n/4) + n[2]/4 _n/2) + n[2]_ _n_
_−_ _−_
= 9T (n/4) + 3(n[2]/4 _n/2) + (n[2]_ _n)_ (after two substitutions)
_−_ _−_
= 9(3T (n/8) + n[2]/16 _n/4) + 3(n[2]/4_ _n/2) + (n[2]_ _n)_
_−_ _−_ _−_
= 27T (n/8) + 9(n[2]/16 _n/4) + 3(n[2]/4_ _n/2) + (n[2]_ _n)_
_−_ _−_ _−_
(after three substitutions).

Therefore, after i substitutions,

_i−1_ _i−1_
_T_ (n) = 3[i]T (n/2[i]) + n[2] �(3/4)[j] _n_ �(3/2)[j]

_−_
_j=0_ _j=0_

= 3[i]T (n/2[i]) 4n[2](3/4)[i] + 4n[2] 2n(3/2)[i] + 2n (by Problem 11).
_−_ _−_

This can be verified easily by induction. Hence, taking i = log n,

_T_ (n) = 3[log][ n] 4n[2](3/4)[log][ n] + 4n[2] 2n(3/2)[log][ n] + 2n
_−_ _−_
= _n[log 3]_ 4n[log 3] + 4n[2] 2n[log 3] + 2n
_−_ _−_
= 4n[2] 5n[log 3] + 2n.
_−_

226. Suppose T (1) = 1, T (2) = 6, and for all n 3, T (n) = T (n 2) + 3n + 4. If
_≥_ _−_
_n is large enough, then by repeated substitution,_

_T_ (n) = _T_ (n 2) + 3n + 4
_−_
= _T_ (n 4) + (3(n 2) + 4) + (3n + 4)
_−_ _−_
= _T_ (n 6) + (3(n 4) + 4) + (3(n 2) + 4) + (3n + 4).
_−_ _−_ _−_

Therefore, after i substitutions,


_T_ (n) = _T_ (n 2i) + 3
_−_


_i−1_
�(n 2j) + 4i

_−_
_j=0_


-----

**44** Chap. 4. Recurrence Relations


= _T_ (n 2i) + 3in 6
_−_ _−_


_i−1_
� _j + 4i_

_j=0_


= _T_ (n 2i) + 3in 3i(i 1) + 4i (by Problem 1)
_−_ _−_ _−_
= _T_ (n 2i) + 3in 3i[2] + 7i.
_−_ _−_

This can be verified easily by induction. Now, suppose that n is even. Take
_i = n/2_ 1. Then,
_−_


_T_ (n) = _T_ (n 2i) + 3in 3i[2] + 7i
_−_ _−_

= _T_ (2) + 3(n/2 1)n 3(n/2 1)[2] + 7(n/2 1)
_−_ _−_ _−_ _−_
= 6 + 3n[2]/2 3n 3n[2]/4 + 3n 3 + 7n/2 7
_−_ _−_ _−_ _−_
= 3n[2]/4 + 7n/2 4.
_−_

Now, suppose that n is odd. Take i = (n 1)/2. Then,
_−_

_i−1_

_T_ (n) = _T_ (n 2i) + 3 �(n 2j) + 4i
_−_ _−_

_j=0_

= _T_ (1) + 3n(n 1)/2 3((n 1)/2)[2] + 7(n 1)/2
_−_ _−_ _−_ _−_
= 1 + 3n[2]/2 3n/2 3n[2]/4 + 3n/2 3/4 + 7n/2 7/2
_−_ _−_ _−_ _−_
= 3n[2]/4 + 7n/2 13/4.
_−_

Therefore, when n is even, T (n) = (3n[2] + 14n 16)/4, and when n is odd,
_−_
_T_ (n) = (3n[2] + 14n 13)/4. Or, more succinctly, T (n) = (3n[2] + 14n 16 +
_−_ _−_
3(n mod 2))/4.

235. Suppose that T (1) = 1, and for all n ≥ 2, T (n) = _i=1_ _[T]_ [(][i][) + 1.]

[�][n][−][1]


_n−2_
� _T_ (i) + 1)

_i=1_


_T_ (n) _T_ (n 1) = (
_−_ _−_


_n−1_
� _T_ (i) + 1) (

_−_
_i=1_


= _T_ (n 1).
_−_

Therefore, T (n) = 2T (n 1). Thus, we have reduced a recurrence with full
_−_
history to a simple recurrence that can be solved by repeated substitution
(I’ll leave that to you) to give the solution T (n) = 2[n][−][1].

###### 4.8 COMMENTS

202. The technique used to solve this problem in the previous section is called
_repeated substitution. It works as follows. Repeatedly substitute until you_
see a pattern developing. Write down a formula for T (n) in terms of n and
the number of substitutions (which you can call i). To be completely formal,


-----

Sec. 4.8. Comments **45**

verify this pattern by induction on i. (You should do this if you are asked to
prove that your answer is correct or if you want to be sure that the pattern
is right, but you can skip it is you are short of time.) Then choose i to be
whatever value it takes to make all of the T ( )s in the pattern turn into the

_·_
base case for the recurrence. You are usually left with some algebra to do,
such as a summation or two. Once you have used repeated substitution to
get an answer, it is prudent to check your answer by using induction. (It
is not normally necessary to hand in this extra work when you are asked to
solve the recurrence on a homework or an exam, but it’s a good idea to do it
for your own peace of mind.) Let’s do it for this problem. We are required
to prove that the solution to the recurrence T (1) = 1, and for all n 2,
_≥_
_T_ (n) = 3T (n 1) + 2, is T (n) = 2 3[n][−][1] 1. The proof is by induction
_−_ _·_ _−_
on n. The claim is certainly true for n = 1. Now suppose that n > 1 and
_T_ (n 1) = 2 3[n][−][2] 1. Then,
_−_ _·_ _−_

_T_ (n) = 3T (n 1) + 2
_−_
= 3(2 3[n][−][2] 1) + 2 (by the induction hypothesis)
_·_ _−_
= 2 3[n][−][1] 1,
_·_ _−_

as required.

222. Hence, Fn = O(1.62[n]). For more information on the constant multiple in the
big-O bound, see Graham, Knuth, and Patashnik [30].


-----

###### Chapter 5

### Correctness Proofs

How do we know that a given algorithm works? The best method is to prove it
correct. Purely recursive algorithms can be proved correct directly by induction.
Purely iterative algorithms can be proved correct by devising a loop invariant for
every loop, proving them correct by induction, and using them to establish that the
algorithm terminates with the correct result. Here are some simple algorithms to
practice on. The algorithms use a simple pseudocode as described in Section 1.3.

###### 5.1 ITERATIVE ALGORITHMS

To prove correctness of an iterative algorithm, you need to do the following:

Write down a specification for the output to be produced by the algorithm as

_•_
a function of its inputs (this will be easy for the simple algorithms considered
in this chapter).
Verify the algorithm one loop at a time, starting at the inner loop in case of

_•_
nested loops.
For each loop, devise a loop invariant that remains true each time through

_•_
the loop and captures the “progress” made by the loop.
Prove that the loop invariants hold. This is usually done by induction on the

_•_
number of iterations. Start by listing the new values of the variables in terms
of the old values. Use this for your inductive step.
Use the loop invariants to prove that the algorithm terminates.

_•_
Use the loop invariants and the termination conditions to prove that the

_•_
algorithm computes the correct result (according to the specification).

The loop invariants discussed in this section use the following convention: If
_v is a variable used in a loop, then vj denotes the value stored in v immediately_
after the jth iteration of the loop, for j ≥ 0. The value v0 means the contents of v
immediately before the loop is entered.

**46**


-----

Sec. 5.1. Iterative Algorithms **47**

###### 5.1.1 Straight-Line Programs

249. Prove that the following algorithm for swapping two numbers is correct.

**procedure swap(x, y)**
**comment Swap x and y.**
1. _x := x + y_
2. _y := x_ _y_
_−_
3. _x := x_ _y_
_−_

###### 5.1.2 Arithmetic

250. Prove that the following algorithm for the addition of natural
numbers is correct.

**function add(y, z)**
**comment Return y + z, where y, z** IN
_∈_
1. _x := 0; c := 0; d := 1;_
2. **while (y > 0)** (z > 0) (c > 0) do
_∨_ _∨_
3. _a := y mod 2;_
_b := z mod 2;_
4. **if a** _b_ _c then x := x + d;_
_⊕_ _⊕_
5. _c := (a_ _b)_ (b _c)_ (a _c);_
_∧_ _∨_ _∧_ _∨_ _∧_
6. _d := 2d; y :=_ _y/2_ ;
_⌊_ _⌋_
_z :=_ _z/2_ ;
_⌊_ _⌋_
7. **return(x)**

251. Prove that the following algorithm for incrementing a natural number is
correct.

**function increment(y)**
**comment Return y + 1, where y** IN
_∈_
1. _x := 0; c := 1; d := 1;_
2. **while (y > 0)** (c > 0) do
_∨_
3. _a := y mod 2;_
4. **if a** _c then x := x + d;_
_⊕_
5. _c := a_ _c;_
_∧_
6. _d := 2d; y :=_ _y/2_ ;
_⌊_ _⌋_
7. **return(x)**

252. Prove that the following algorithm for the multiplication of natural
numbers is correct.


-----

**48** Chap. 5. Correctness Proofs

**function multiply(y, z)**
**comment Return yz, where y, z** IN
_∈_
1. _x := 0;_
2. **while z > 0 do**
3. **if z mod 2 = 1 then x := x + y;**
4. _y := 2y; z :=_ _z/2_ ;
_⌊_ _⌋_
5. **return(x)**

253. Prove that the following algorithm for the multiplication of
natural numbers is correct.

**function multiply(y, z)**
**comment Return yz, where y, z** IN
_∈_
1. _x := 0;_
2. **while z > 0 do**
3. _x := x + y_ (z mod 2);
_·_
4. _y := 2y; z :=_ _z/2_ ;
_⌊_ _⌋_
5. **return(x)**

254. Prove that the following algorithm for the multiplication of natural
numbers is correct, for all integer constants c 2.
_≥_

**function multiply(y, z)**
**comment Return yz, where y, z** IN
_∈_
1. _x := 0;_
2. **while z > 0 do**
3. _x := x + y_ (z mod c);
_·_
4. _y := c_ _y; z :=_ _z/c_ ;
_·_ _⌊_ _⌋_
5. **return(x)**

255. Prove that the following algorithm for division and remaindering of
natural numbers is correct.

**function divide(y, z)**
**comment Return q, r** IN such that y = qz + r
_∈_
and r < z, where y, z IN
_∈_
1. _r := y; q := 0; w := z;_
2. **while w** _y do w := 2w;_
_≤_
3. **while w > z do**
4. _q := 2q; w :=_ _w/2_ ;
_⌊_ _⌋_
5. **if w** _r then_
_≤_
6. _r := r_ _w; q := q + 1_
_−_
7. **return(q, r)**


-----

Sec. 5.1. Iterative Algorithms **49**

256. Prove that the following algorithm for exponentiation is correct.

**function power(y, z)**
**comment Return y[z], where y** IR, z IN
_∈_ _∈_
1. _x := 1;_
2. **while z > 0 do**
3. _x := x_ _y_
_·_
4. _z := z_ 1
_−_
5. **return(x)**

257. Prove that the following algorithm for exponentiation is correct.

**function power(y, z)**
**comment Return y[z], where y** IR, z IN
_∈_ _∈_
1. _x := 1;_
2. **while z > 0 do**
3. **if z is odd then x := x** _y_
_·_
4. _z :=_ _z/2_
_⌊_ _⌋_
5. _y := y[2]_

6. **return(x)**

258. Prove that the following algorithm for computing factorials is correct.

**function factorial(y)**
**comment Return y!, where y** IN
_∈_
1. _x := 1_
2. **while y > 1 do**
3. _x := x_ _y; y := y_ 1
_·_ _−_
4. **return(x)**

###### 5.1.3 Arrays

259. Prove that the following algorithm that adds the values in an array
_A[1..n] is correct._

**function sum(A)**
**comment Return** [�]i[n]=1 _[A][[][i][]]_
1. _s := 0;_
2. **for i := 1 to n do**
3. _s := s + A[i]_
4. **return(s)**


-----

**50** Chap. 5. Correctness Proofs

260. Prove that the following algorithm for computing the maximum value
in an array A[1..n] is correct.

**function max(A)**
**comment Return max A[1], . . ., A[n]**
1. _m := A[1]_
2. **for i := 2 to n do**
3. **if A[i] > m then m := A[i]**
4. **return(m)**

261. Prove the correctness of the following bubblesort algorithm. The
values to be sorted are in an array A[1..n].

**procedure bubblesort(A[1..n])**
**comment Sort A[1], A[2], . . ., A[n] into nondecreasing order**
1. **for i := 1 to n** 1 do
_−_
2. **for j := 1 to n** _i do_
_−_
3. **if A[j] > A[j + 1] then**
4. Swap A[j] with A[j + 1]

262. Prove the correctness of the following pattern-matching algorithm.
The input consists of a string S[1..n], and a pattern P [0..m 1], where 1
_−_ _≤_
_m_ _n. The algorithm locates the first contiguous occurrence of the pattern_
_≤_
_P in the string S, that is, ℓ_ = p if S[p..p + m 1] = P, and ℓ = n _m + 1 if_
_−_ _−_
the pattern P does not occur at all in the string S.

**function match(P, S, n, m)**
**comment Find the pattern P** [0..m 1] in string S[1..n]
_−_
1. _ℓ_ := 0; matched := false
2. **while (ℓ** _n_ _m)_ matched do
_≤_ _−_ _∧¬_
3. _ℓ_ := ℓ + 1 ;
4. _r := 0; matched := true_
5. **while (r < m)** matched do
_∧_
6. matched := matched (P [r] = S[ℓ + r])
_∧_
7. _r := r + 1_
8. **return(ℓ)**

263. Prove that the following matrix multiplication algorithm is correct.


-----

Sec. 5.2. Recursive Algorithms **51**

**procedure matmultiply(Y, Z, n);**
**comment multiplies n** _n matrices Y Z_
_×_
1. **for i := 1 to n do**
2. **for j := 1 to n do**
3. _X[i, j] := 0;_
4. **for k := 1 to n do**
5. _X[i, j] := X[i, j] + Y [i, k]_ _Z[k, j];_
_·_
6. **return(X)**

264. Prove that the following algorithm for evaluating the polynomial
_anx[n]_ + an−1x[n][−][1] + · · · + a1x + a0 is correct, where the coefficients are stored
in an array A[0..n], with A[i] = ai for all 0 ≤ _i ≤_ _n. The algorithm is named_
after its inventor, William G. Horner, and is often called Horner’s rule.

**function Horner(A, n)**
**comment Return** [�]i[n]=0 _[A][[][i][]][ ·][ x][i]_

1. _v := 0_
2. **for i := n downto 0 do**
3. _v := A[i] + v_ _x_
_·_
4. **return(v)**

###### 5.1.4 Fibonacci Numbers

265. Prove that the following algorithm for computing Fibonacci
numbers is correct.

**function fib(n)**
1. **comment Return Fn, the nth Fibonacci number**
2. **if n = 0 then return(0) else**
3. last:=0; current:=1
4. **for i := 2 to n do**
5. temp:=last+current; last:=current; current:=temp
6. **return(current)**

###### 5.2 RECURSIVE ALGORITHMS

To prove correctness of a recursive algorithm, you need to do the following:

You will prove correctness by induction on the “size” of the problem being

_•_
solved (for example, the size of array chunk, number of bits in an integer,
etc.). Your first task is to identify what is to be used as the “size.”


-----

**52** Chap. 5. Correctness Proofs

Then, you prove the base of the induction, which will usually involve only the

_•_
base of the recursion.
Next, you need to prove that recursive calls are given subproblems to solve

_•_
(that is, there is no infinite recursion). This is often trivial, but it can be
difficult to prove and so should not be overlooked.
Finally, you prove the inductive step: Assume that the recursive calls work

_•_
correctly, and use this assumption to prove that the current call works correctly.

###### 5.2.1 Arithmetic

266. Prove that the following recursive algorithm computes 3[n] 2[n] for all
_−_
_n_ 0.
_≥_

**function g(n)**
1. **if n** 1 then return(n)
_≤_
2. **else return(5** _g(n_ 1) 6 _g(n_ 2))
_·_ _−_ _−_ _·_ _−_

267. Prove that the following recursive algorithm for incrementing a natural
number is correct.

**function increment(y)**
**comment Return y + 1.**
1. **if y = 0 then return(1) else**
2. **if y mod 2 = 1 then**
3. return(2 increment( _y/2_ ))
_·_ _⌊_ _⌋_
4. **else return(y + 1)**

268. Prove that the following recursive algorithm for the addition of natural
numbers is correct.

**function add(y, z, c)**
**comment Return the sum y + z + c, where c** 0, 1 .
_∈{_ _}_
1. **if y = z = 0 then return(c) else**
2. _a := y mod 2; b := z mod 2;_
3. return(2 add( _y/2_ _,_ _z/2_ _,_ (a + b + c)/2 ) + (a _b_ _c))_
_·_ _⌊_ _⌋_ _⌊_ _⌋_ _⌊_ _⌋_ _⊕_ _⊕_

269. Prove that the following recursive algorithm for the multiplication
of natural numbers is correct.

**function multiply(y, z)**
**comment Return the product yz.**
1. **if z = 0 then return(0) else**
2. **if z is odd then return(multiply(2y,** _z/2_ )+y)
_⌊_ _⌋_
3. **else return(multiply(2y,** _z/2_ ))
_⌊_ _⌋_


-----

Sec. 5.2. Recursive Algorithms **53**

270. Prove that the following recursive algorithm for the multiplication of
natural numbers is correct.

**function multiply(y, z)**
**comment Return the product yz.**
1. **if z = 0 then return(0) else**
2. return(multiply(2y, _z/2_ ) + y (z mod 2))
_⌊_ _⌋_ _·_

271. Prove that the following recursive algorithm for the multiplication of
natural numbers is correct, for all integers constants c 2.
_≥_

**function multiply(y, z)**
**comment Return the product yz.**
1. **if z = 0 then return(0) else**
2. return(multiply(cy, _z/c_ ) + y (z mod c))
_⌊_ _⌋_ _·_

272. Prove that the following recursive algorithm for exponentiation is correct.

**function power(y, z)**
**comment Return y[z], where y** IR, z IN.
_∈_ _∈_
1. **if z = 0 then return(1)**
2. **if z is odd then return(power(y[2],** _z/2_ ) _y)_
_⌊_ _⌋_ _·_
3. **else return(power(y[2],** _z/2_ ))
_⌊_ _⌋_

273. Prove that the following recursive algorithm for computing factorials is
correct.

**function factorial(n)**
**comment Return n!.**
1. **if n** 1 then return(1)
_≤_
2. **else return(n** factorial(n 1))
_·_ _−_

###### 5.2.2 Arrays

274. Prove that the following recursive algorithm for computing the maximum
value in an array A[1..n] is correct.

**function maximum(n)**
**comment Return max of A[1..n].**
1. **if n** 1 then return(A[1])
_≤_
2. **else return(max(maximum(n** 1),A[n]))
_−_

**function max(x, y)**
**comment Return largest of x and y.**
3. **if x** _y then return(x) else return(y)_
_≥_


-----

**54** Chap. 5. Correctness Proofs

275. Prove that the following recursive algorithm that adds the values in an
array A[1..n] is correct.

**function sum(n)**
**comment Return sum of A[1..n].**
1. **if n** 1 then return(A[1])
_≤_
2. **else return(sum(n** 1) + A[n])
_−_

###### 5.2.3 Fibonacci Numbers

276. Prove that the following algorithm for computing Fibonacci numbers is correct.

**function fib(n)**
**comment Return Fn, the nth Fibonacci number.**
1. **if n** 1 then return(n)
_≤_
2. **else return(fib(n** 1)+fib(n 2))
_−_ _−_

277. Prove that the following algorithm for computing Fibonacci
numbers is correct.

**function fib(n)**
**comment Return (Fn−1, Fn)**
1. **if n is odd then**
2. (a, b) := even(n 1)
_−_
3. **return(b, a + b)**
4. **else return(even(n))**

**function even(n)**
**comment Return (Fn−1, Fn) when n is even**
1. **if n = 0 then return(1, 0)**
2. **else if n = 2 then return(1, 1)**
3. **else if n = 4 then return(2, 3)**
4. (a, b) := fib(n/2 1)
_−_
5. _c := a + b; d := b + c_
6. **return(b** _d + a_ _c, c_ (d + b))
_·_ _·_ _·_

###### 5.3 COMBINED ITERATION AND RECURSION

The following questions ask you to prove correct some recursive algorithms that
have loops in them. Naturally enough, you can solve them by applying both of the
techniques you have used in this chapter.


-----

Sec. 5.4. Hints **55**

278. Prove that the following recursive bubblesort algorithm is correct. The
values to be sorted are in an array A[1..n].

**procedure bubblesort(n)**
**comment Sort A[1..n].**
1. **if n > 1 then**
2. **for j := 1 to n** 1 do
_−_
3. **if A[j] > A[j + 1] then**
4. Swap A[j] with A[j + 1]
5. bubblesort(n 1)
_−_

279. Prove that the following variant of quicksort is correct. The values
to be sorted are in an array A[1..n].

1. **procedure quicksort(ℓ, r)**
2. **comment sort S[ℓ..r]**
3. _i := ℓ; j := r_
_a := some element from S[ℓ..r]_
4. **repeat**
5. **while S[i] < a do i := i + 1**
6. **while S[j] > a do j := j** 1
_−_
7. **if i** _j then_
_≤_
8. swap S[i] and S[j]
9. _i := i + 1; j := j_ 1
_−_
10. **until i > j**
11. **if ℓ< j then quicksort(ℓ, j)**
12. **if i < r then quicksort(i, r)**

###### 5.4 HINTS

In each of the following hints, if the algorithm uses a variable v, then vi denotes the
contents of v immediately after the ith iteration of the single loop in the algorithm
(v0 denotes the contents of v immediately before the loop is entered for the first
time).

250. The loop invariant is the following: (yj + zj + cj)dj + xj = y0 + z0.

252. The loop invariant is the following: yjzj + xj = y0z0.

255. The loop invariant is the following: qjwj + rj = y0 and rj < wj.

256. The loop invariant is the following: xjyj _[z][j]_ = y0[z][0] [.]


-----

**56** Chap. 5. Correctness Proofs

257. The loop invariant is the following: xjyj _[z][j]_ = y0[z][0] [.]

258. The loop invariant is the following: mj = [�]k[n]=n−j+1 _[k][.]_

259. The loop invariant is the following: sj = [�]i[j]=1 _[A][[][i][].]_

260. The loop invariant is the following: mj is the maximum of A[1], . . ., A[j + 1].

261. The loop invariant for the inner loop is the following: after the jth iteration,
for all 1 _i < j, A[i]_ _A[j]. The loop invariant for the outer loop is the_
_≤_ _≤_
following: after the jth iteration, for all n _j + 1_ _i_ _n, for all k < i,_
_−_ _≤_ _≤_
_A[k]_ _A[i]._
_≤_

277. The identity from Problem 53 might help.

###### 5.5 SOLUTIONS

250. This correctness proof will make use of the fact that for all n IN,
_∈_

2 _n/2_ + (n mod 2) = n. (5.1)
_⌊_ _⌋_

(Can you prove this?) We claim that if y, z IN, then add(y, z) returns the
_∈_
value y + z. That is, when line 8 is executed, x = y + z. For each of the
identifiers, use a subscript i to denote the value of the identifier after the ith
iteration of the while-loop on lines 3–7, for i 0, with i = 0 meaning the
_≥_
time immediately before the while loop is entered and immediately after the
statement on line 2 is executed. By inspection,

_aj+1_ = _yj mod 2_
_bj+1_ = _zj mod 2_
_yj+1_ = _⌊yj/2⌋_
_zj+1_ = _⌊zj/2⌋_
_dj+1_ = 2dj.

From line 6 of the algorithm, cj+1 is 1 iff at least two of aj+1, bj+1, and cj
are 1 (see Problem 93). Therefore,

_cj+1 = ⌊(aj+1 + bj+1 + cj)/2⌋._

Note that d is added into x in line 5 of the algorithm only when an odd
number of a, b, and c are 1. Therefore,

_xj+1 = xj + dj((aj+1 + bj+1 + cj) mod 2)._

We will now prove the following loop invariant: For all natural numbers j 0,
_≥_

(yj + zj + cj)dj + xj = y0 + z0.


-----

Sec. 5.5. Solutions **57**

The proof is by induction on j. The base j = 0 is trivial, since c0 = 0, d0 = 1,
and x0 = 0. Now, suppose that

(yj + zj + cj)dj + xj = y0 + z0.

We are required to prove that

(yj+1 + zj+1 + cj+1)dj+1 + xj+1 = y0 + z0.

By the preceding,

(yj+1 + zj+1 + cj+1)dj+1 + xj+1
= (⌊yj/2⌋ + ⌊zj/2⌋ + ⌊(yj mod 2 + zj mod 2 + cj)/2⌋)2dj
+ xj + dj((yj mod 2 + zj mod 2 + cj) mod 2)

= (⌊yj/2⌋ + ⌊zj/2⌋)2dj + xj + dj(yj mod 2 + zj mod 2 + cj)
(by Equation 5.1)
= (yj + zj + cj)dj + xj (by Equation 5.1 twice).

Therefore, by the induction hypothesis,

(yj+1 + zj+1 + cj+1)dj+1 + xj+1 = y0 + z0.

This ends the proof of the loop invariant. It remains to use it to prove that
the algorithm is correct. We need to prove that the algorithm terminates
with x containing the sum of y and z. First, we will prove that it terminates.
By inspection, the values of y and z are halved (rounding down if they are
odd) on every iteration of the loop. Therefore, they will eventually both have
value zero, and stay that way. At the first point at which y = z = 0, either
_c will equal zero or c will be assigned zero on the next iteration of the loop._
Therefore, eventually y = z = c = 0, at which point the loop terminates.
Now we will prove that x has the correct value on termination. Suppose the
loop terminates after t iterations, for some t 0. By the loop invariant,
_≥_

(yt + zt + ct)dt + xt = y0 + z0.

Since yt = zt = ct = 0, we see that xt = y0 + z0. Therefore, the algorithm
terminates with x containing the sum of the initial values of y and z, as
required.

269. The correctness proof is by induction on z. We claim that multiply(y, z)
returns the product yz. The hypothesis is true for z = 0, since multiply(y, 0)
returns 0. Now, suppose that for z 0, multiply(y, z) returns yz. We now
_≥_
must prove that multiply(y, z + 1) returns y(z + 1). There are two cases to
be considered, depending on whether z + 1 is odd or even. By inspection, if


-----

**58** Chap. 5. Correctness Proofs

_z + 1 is odd, then multiply(y, z + 1) returns_

multiply(2y, (z + 1)/2 ) + y
_⌊_ _⌋_
= 2y (z + 1)/2 + y (by the induction hypothesis)
_⌊_ _⌋_
= 2y(z/2) + y (since z is even)
= _y(z + 1)._

By inspection, if z + 1 is even, then multiply(y, z + 1) returns

multiply(2y, (z + 1)/2 )
_⌊_ _⌋_
= 2y (z + 1)/2 (by the induction hypothesis)
_⌊_ _⌋_
= 2y(z + 1)/2 (since z is odd)
= _y(z + 1)._

###### 5.6 COMMENTS

253. The hard part about this problem (and other similar problems in this section)
is that you will need to find your own loop invariant.

265. See Section 2.7 for the definition of Fibonacci numbers. This is the obvious
iterative algorithm.

276. See Section 2.7 for the definition of Fibonacci numbers. This is the obvious
recursive algorithm.

277. See Section 2.7 for the definition of Fibonacci numbers. This is a sneaky
recursive algorithm.


-----

###### Chapter 6

### Algorithm Analysis

Algorithm analysis usually means “give a big-O figure for the running time of an
algorithm.” (Of course, a big-Θ bound would be even better.) This can be done by
getting a big-O figure for parts of the algorithm and then combining these figures
using the sum and product rules for big-O (see Problems 173 and 176). As we will
see, recursive algorithms are more difficult to analyze than nonrecursive ones.
Another useful technique is to pick an elementary operation, such as additions,
multiplications, or comparisons, and observe that the running time of the algorithm
is big-O of the number of elementary operations. (To find the elementary operation,
just ignore the “book keeping” code and look for the point in the algorithm where
the real work is done.) Then, you can analyze the exact number of elementary
operations as a function of n in the worst case. This is often easier to deal with
because it is an exact function of n and you don’t have the messy big-O symbols to
carry through your analysis.

###### 6.1 ITERATIVE ALGORITHMS

The analysis of iterative algorithms is fairly easy. Simply charge O(1) for code
without loops (assuming that your pseudocode isn’t hiding something that takes
longer), and use the sum and product rules for big-O (see Problems 173 and 176).
If you get tired of carrying around big-Os, use the “elementary operation” technique
described earlier.

###### 6.1.1 What is Returned?

280. What is the value returned by the following function? Express your
answer as a function of n. Give, using big-O notation, the worst-case running
time.

**59**


-----

**60** Chap. 6. Algorithm Analysis

**function mystery(n)**
1. _r := 0;_
2. **for i := 1 to n** 1 do
_−_
3. **for j := i + 1 to n do**
4. **for k := 1 to j do**
5. _r := r + 1_
6. return(r)

281. What is the value returned by the following function? Express your
answer as a function of n. Give, using big-O notation, the worst-case running
time.

**function pesky(n)**
1. _r := 0;_
2. **for i := 1 to n do**
3. **for j := 1 to i do**
4. **for k := j to i + j do**
5. _r := r + 1_
6. return(r)

282. What is the value returned by the following function? Express your
answer as a function of n. Give, using big-O notation, the worst-case running
time.

**function pestiferous(n)**
1. _r := 0;_
2. **for i := 1 to n do**
3. **for j := 1 to i do**
4. **for k := j to i + j do**
5. **for ℓ** := 1 to i + j _k do_
_−_
6. _r := r + 1_
7. return(r)

283. What is the value returned by the following function? Express
your answer as a function of n. Give, using big-O notation, the worst-case
running time.

**function conundrum(n)**
1. _r := 0;_
2. **for i := 1 to n do**
3. **for j := i + 1 to n do**
4. **for k := i + j** 1 to n do
_−_
5. _r := r + 1_
6. return(r)


-----

Sec. 6.1. Iterative Algorithms **61**

###### 6.1.2 Arithmetic

284. Analyze the algorithm for the addition of natural numbers in Problem 250. How many additions does it use (that is, how many times is line 4
executed) in the worst case?

285. Analyze the algorithm for incrementing a natural number in Problem 251.
How many additions does it use (that is, how many times is line 4 executed)
in the worst case?

286. Analyze the algorithm for the multiplication of natural numbers in Problem 252. How many additions does it use (that is, how many times is line 3
executed) in the worst case?

287. Analyze the algorithm for the multiplication of natural numbers in Problem 253. How many additions does it use (that is, how many times is line 3
executed) in the worst case?

288. Analyze the algorithm for the multiplication of natural numbers in Problem 254. How many additions does it use (that is, how many times is line 3
executed) in the worst case? You may assume that c 2 is an integer.
_≥_

289. Analyze the algorithm for division and remaindering of natural numbers
in Problem 255. How many subtractions does it use (that is, how many times
is line 6 executed) in the worst case?

290. Analyze the algorithm for exponentiation in Problem 256. How many
multiplications does it use (that is, how many times is line 3 executed) in the
worst case?

291. Analyze the algorithm for exponentiation in Problem 257. How
many multiplications does it use (that is, how many times is line 3 executed)
in the worst case?

292. Analyze the algorithm for computing factorials in Problem 258. How
many multiplications does it use (that is, how many times is line 3 executed)
in the worst case?

###### 6.1.3 Arrays

293. Analyze the array addition algorithm in Problem 259. How many additions does it use (that is, how many times is line 3 executed) in the worst
case?

294. Analyze the array maximum algorithm in Problem 260. How many
comparisons does it use (that is, how many times is line 3 executed) in the
worst case?


-----

**62** Chap. 6. Algorithm Analysis

295. Analyze the bubblesort algorithm in Problem 261. How many comparisons does it use (that is, how many times is line 3 executed) in the worst
case?

296. Analyze the pattern-matching algorithm in Problem 262. How many
accesses of the array P does it use (that is, how many times is line 6 executed)
in the worst case?

297. Analyze the matrix multiplication algorithm in Problem 263. How many
multiplications does it use (that is, how many times is line 5 executed) in the
worst case?

298. Analyze the algorithm for evaluating a polynomial in Problem 264. How
many multiplications does it use (that is, how many times is line 3 executed)
in the worst case?

###### 6.1.4 Fibonacci Numbers

299. Analyze the algorithm for computing Fibonacci numbers in Problem 265.
How many additions does it use (that is, how many times is line 3 executed)
in the worst case?

###### 6.2 RECURSIVE ALGORITHMS

The analysis of recursive algorithms is a little harder than that of nonrecursive ones.
First, you have to derive a recurrence relation for the running time, and then you
have to solve it. Techniques for the solution of recurrence relations are explained in
Chapter 4.
To derive a recurrence relation for the running time of an algorithm:

Decide what “n”, the problem size, is.

_•_
See what value of n is used as the base of the recursion. It will usually be a

_•_
single value (for example, n = 1), but may be multiple values. Suppose it is
_n0._

_• Figure out what T_ (n0) is. You can usually use “some constant c,” but sometimes a specific number will be needed.
The general T (n) is usually a sum of various choices of T (m) (for the recursive

_•_
calls), plus the sum of the other work done. Usually, the recursive calls will
be solving a subproblems of the same size f (n), giving a term “a _T_ (f (n))”
_·_
in the recurrence relation.

The “elementary operation” technique described in the first paragraph of this
chapter can be used to good effect here, too.


-----

Sec. 6.2. Recursive Algorithms **63**

###### 6.2.1 Arithmetic

300. Analyze the recursive algorithm from Problem 266. How
many additions does it use (that is, how many times is line 2 executed) in the
worst case?

301. Analyze the recursive algorithm for incrementing a natural number in
Problem 267. How many right-shifts does it use (that is, how many times is
line 3 executed) in the worst case?

302. Analyze the recursive algorithm for the addition of natural numbers in
Problem 268. How many times is line 3 executed in the worst case?

303. Analyze the recursive algorithm for the multiplication of natural
numbers in Problem 269. How many additions does it use (that is, how many
times is line 2 executed) in the worst case?

304. Analyze the recursive algorithm for the multiplication of natural numbers
in Problem 270. How many additions does it use (that is, how many times is
line 2 executed) in the worst case?

305. Analyze the recursive algorithm for the multiplication of natural numbers
in Problem 271. How many additions does it use (that is, how many times is
line 2 executed) in the worst case? You may assume that c 2 is an integer.
_≥_

306. Analyze the recursive algorithm for exponentiation in Problem 272. How
many multiplications does it use (that is, how many times is line 2 executed)
in the worst case?

307. Analyze the recursive algorithm for computing factorials in Problem 273.
How many multiplications does it use (that is, how many times is line 2
executed) in the worst case?

###### 6.2.2 Arrays

308. Analyze the recursive algorithm for computing the maximum value in an
array in Problem 274. How many comparisons does it use (that is, how many
times is line 2 executed) in the worst case?

309. Analyze the recursive algorithm that adds the values in an array in
Problem 275. How many additions does it use (that is, how many times is
line 2 executed) in the worst case?


-----

**64** Chap. 6. Algorithm Analysis

###### 6.2.3 Fibonacci Numbers

310. Analyze the algorithm for computing Fibonacci numbers in Problem 276.
How many additions does it use (that is, how many times is line 2 executed)
in the worst case?

311. Analyze the algorithm for computing Fibonacci numbers in Problem 277. How many additions does it use (that is, how many times is line 3
executed) in the worst case?

###### 6.3 COMBINED ITERATION AND RECURSION

The following questions ask you to analyze some recursive algorithms that have loops
in them. Naturally enough, you can do this by applying both of the techniques you
have used in this chapter.

312. Analyze the recursive version of bubblesort in Problem 278. How many
comparisons does it use (that is, how many times is line 3 executed) in the
worst case?

313. Analyze the variant of quicksort in Problem 279. How many comparisons does it use (that is, how many times are lines 5 and 6 executed) in
the worst case?

###### 6.4 HINTS

283 If you use the technique from the solution of Problem 280 blindly, you’ll get
the answer n(n 1)/2. This is wrong. More subtlety is necessary. The correct
_−_
answer is n(n +2)(2n 1)/24 if n is even, and something different if n is odd.
_−_
(You didn’t think I would give you the whole answer, did you?) You can
partially verify your solution in a few minutes by coding the algorithm as a
program and printing n and r for a few values of n.

284. I am looking for a big-O analysis of the running time, and an exact function
of n (with no big-O at the front) for the number of additions. You can do the
running time first, or if you are clever, you can observe that additions are the
“elementary operation,” count them exactly, and then put a big-O around
the function you get as answer to the second part of the question (reducing
it to the simplest form, of course) to give the answer for the first part of the
question.


-----

Sec. 6.5. Solutions **65**

300. Fibonacci numbers are involved (see Section 2.7 for definitions). Specifically,
you will need to apply the results from Problems 52 and 222.

###### 6.5 SOLUTIONS

280. The for-loop on lines 4–5 has the same effect as r := r + j. Therefore, the
for-loop on lines 3–5 has the following effect:
3–5. **for j := i + 1 to n do**
_r := r + j,_
equivalently, r := r + [�]j[n]=i+1 _[j][. Now,]_


_n_
� _j =_

_j=i+1_


_n_
�

_j_
_−_
_j=1_


_i_
� _j = n(n + 1)/2_ _i(i + 1)/2._

_−_
_j=1_


Therefore, the for-loop on lines 2–5 has the following effect:
2–5. **for i := 1 to n** 1 do
_−_
_r := r + n(n + 1)/2_ _i(i + 1)/2,_
_−_
equivalently, r := r + [�][n]i=1[−][1][(][n][(][n][ + 1)][/][2][ −] _[i][(][i][ + 1)][/][2). Now,]_

_n−1_
�(n(n + 1)/2 _i(i + 1)/2)_

_−_
_i=1_


_n−1_
�

_i_

_i=1_


(n 1)n(n + 1)
_−_
=

_−_ [1]
2 2


_n−1_
�

_i[2]_
_−_ [1]

2

_i=1_


= (n 1)n(n + 1)/2 _n(n_ 1)(2n 1)/12 _n(n_ 1)/4
_−_ _−_ _−_ _−_ _−_ _−_
(by Problems 1 and 2)
= _n(n[2]_ 1)/3.
_−_

Therefore, function mystery returns n(n[2] 1)/3. A sloppy analysis goes as
_−_
follows. The for-loop that begins on line 2 is executed for O(n) iterations. The
for-loop that begins on line 3 is executed for O(n) iterations. The for-loop
that begins on line 4 is executed for O(n) iterations. Lines 1 and 5 take O(1)
time. Therefore, function mystery runs in time O(n[3]). This analysis is tight
because the preceding paragraph showed that line 5 is executed n(n[2] 1)/3
_−_
times.

300. Let A(n) be the number of additions used in function g(n). Then A(0) =
_A(1) = 0 and for all n > 1, A(n) = A(n_ 1) + A(n 2) + 1. This recurrence
_−_ _−_
relation is a little tricky to solve, but repeated substitution will do it:

_A(n)_ = _A(n_ 1) + A(n 2) + 1
_−_ _−_
= (A(n 2) + A(n 3) + 1) + A(n 2) + 1
_−_ _−_ _−_


-----

**66** Chap. 6. Algorithm Analysis

= 2A(n 2) + A(n 3) + 1 + 1
_−_ _−_

= 2(A(n 3) + A(n 4) + 1) + A(n 3) + 1 + 1
_−_ _−_ _−_
= 3A(n 3) + 2A(n 4) + 1 + 1 + 2
_−_ _−_
= 3(A(n 4) + A(n 5) + 1) + 2A(n 4) + 1 + 1 + 2
_−_ _−_ _−_
= 5A(n 4) + 3A(n 5) + 1 + 1 + 2 + 3.
_−_ _−_

There is a pattern involving Fibonacci numbers (see Section 2.7) developing
here. It can be verified by induction on i 1 that after i substitutions,
_≥_


_A(n) = Fi+1A(n −_ _i) + FiA(n −_ _i −_ 1) +

Hence, taking i = n 1,
_−_


_i_
� _Fj._

_j=1_


_A(n)_ = _FnA(1) + Fn−1A(0) +_


_n−1_
� _Fj_

_j=1_


=


_n−1_
�

_Fj_
_j=1_


= _Fn+1 −_ 1 (see Problem 52).

The running time of procedure g(n) is clearly big-O of the number of additions, and is hence O(Fn+1) = O(1.62[n]) (for the latter, see the comment to
Problem 222).

303. Let n be the number of bits in z, and A(n) be the number of additions
used in the multiplication of y by z. Then A(0) = 0 and for all n 1,
_≥_
_A(n) = A(n_ 1) + 1. The solution to this recurrence is A(n) = n. (Can you
_−_
verify this by induction on n? If I didn’t tell you the answer, could you have
derived it for yourself?) The running time of procedure multiply is clearly
big-O of the number of additions, and is hence O(n).

###### 6.6 COMMENTS

291. Which algorithm would you use in practice, the one in this problem or the
one from Problem 290?

311. Which algorithm would you use in practice, the one in this problem, the one
from Problem 299, or the one from Problem 310?

313. The worst-case analysis of quicksort is often presented in class, but if not,
then it makes a good exercise.


-----

###### Chapter 7

### Divide-and-Conquer

Divide-and-conquer is perhaps the most commonly used algorithm design technique
in computer science. Faced with a big problem P, divide it into smaller problems,
solve these subproblems, and combine their solutions into a solution for P . But how
do you solve the smaller problems? Simply divide each of the small problems into
smaller problems, and keep doing this until the problems become so small that it is
trivial to solve them. Sound like recursion? Not surprisingly, a recursive procedure
is usually the easiest way of implementing divide-and-conquer.

###### 7.1 MAXIMUM AND MINIMUM

The following is a divide-and-conquer algorithm for finding the maximum value in an
array S[1..n]. The main body of the algorithm consists of a call to maximum(1, n).

**function maximum(x, y)**
**comment return maximum in S[x..y]**
1. **if y** _x_ 1 then return(max(S[x], S[y]))
_−_ _≤_
2. **else**
3. max1:=maximum(x, (x + y)/2 )
_⌊_ _⌋_
4. max2:=maximum( (x + y)/2 + 1, y)
_⌊_ _⌋_
5. **return(max(max1,max2))**

314. Prove that the algorithm is correct. You may assume that n is a
power of 2.

315. Write down a recurrence relation for the worst-case number of comparisons used by maximum(1, n). Solve this recurrence relation. You may
assume that n is a power of 2.

316. What is the running time of maximum(1, n)? Explain your answer.

Most textbooks introduce divide-and-conquer using the MAXMIN problem, the
problem of finding the largest and smallest values in an array of n values. It is

**67**


-----

**68** Chap. 7. Divide-and-Conquer

usually described for n a power of 2. The following problems ask you to extend this
to arbitrary n.

317. Design and analyze a divide-and-conquer MAXMIN algorithm
that uses 3n/2 2 comparisons for any n IN.
_⌈_ _⌉−_ _∈_

318. Consider the following MAXMIN algorithm. How many comparisons
does it use? Is it likely to be faster or slower than the divide-and-conquer
algorithm in practice?

**procedure maxmin2(S)**
**comment computes maximum and minimum of S[1..n]**
in max and min resp.
1. **if n is odd then max:=S[n]; min:=S[n]**
2. **else max:=** ; min:=
_−∞_ _∞_
3. **for i := 1 to** _n/2_ **do**
_⌊_ _⌋_
4. **if S[2i** 1] _S[2i]_
_−_ _≤_
5. **then small:=S[2i** 1]; large:=S[2i]
_−_
6. **else small:=S[2i]; large:=S[2i** 1]
_−_
7. **if small < min then min:=small**
8. **if large > max then min:=small**

319. Show that any comparison-based MAXMIN algorithm must use at
least 3n/2 2 comparisons in the worst case, for all n IN.
_⌈_ _⌉−_ _∈_

###### 7.2 INTEGER MULTIPLICATION

Another popular example of divide-and-conquer is the O(n[1][.][59]) time integer multiplication algorithm. The following questions will test your understanding of this
algorithm and its analysis.

320. What is the depth of recursion of the divide-and-conquer integer multiplication algorithm? At what depth does it start to repeat the same subproblems?

321. Suppose you are to write an algorithm for multiplying two n-bit
integers, and you are told that you have a computer with word size _n, and_

_[√]_
hence that you can multiply two _n-bit integers in O(1) time. Show that, by_

_[√]_
using the divide-and-conquer multiplication and stopping the recursion early,
you can multiply two n-bit integers in time O(n[1][.][2925]).

322. Devise an algorithm to multiply an n-bit integer by an m-bit integer,
where n _m, in time O(nm[log 3][−][1])._
_≥_


-----

Sec. 7.2. Integer Multiplication **69**

Complete the design of the following algorithm for performing integer multiplication
in time O(n[1][.][63]). (This is slower than the standard algorithm, but its verification
and analysis will test your abilities.) We use a technique similar to the standard
divide-and-conquer algorithm. Instead of dividing the inputs y and z into two parts,
we divide them into three parts. Suppose y and z have n bits, where n is a power
of 3. Break y into three parts, a, b, c, each with n/3 bits. Break z into three parts,
_d, e, f_, each with n/3 bits. Then,

_yz = ad2[4][n/][3]_ + (ae + bd)2[n] + (af + cd + be)2[2][n/][3] + (bf + ce)2[n/][3] + cf.

This can be computed as follows:

_r1_ := _ad_
_r2_ := (a + b)(d + e)
_r3_ := _be_
_r4_ := (a + c)(d + f )
_r5_ := _cf_
_r6_ := (b + c)(e + f )
_x_ := _r12[4][n/][3]_ + (r2 _r1_ _r3)2[n]_ + (r3 + r4 _r1_ _r5)2[2][n/][3]_
_−_ _−_ _−_ _−_

+ (r6 − _r3 −_ _r5)2[n/][3]_ + r5.

323. Show that x = yz.

324. Show that this algorithm runs in O(n[1][.][63]) bit-operations, as claimed.

Joe D. Student is confused. He was told to implement the divide-and-conquer
algorithm for integer multiplication, and find the value of n for which the divideand-conquer algorithm is faster than the naive algorithm (see Problem 252) on
_n-bit integers. It must be faster for large enough n since, as he saw in class, the_
naive algorithm takes time O(n[2]) and the divide-and-conquer algorithm takes time
_O(n[1][.][585]). Here is the Pascal data structure that he used:_
```
const Precision=5000;
type Bit=0..1;
   longinteger=packed array[1..Precision] of Bit;

```
He started by writing procedures to do addition, left-shifting, and so on. For
example, here is his addition procedure:
```
procedure LongAdd(var result,summand:longinteger);
 {result:=result+summand}
 var index,digitsum:integer;

```

-----

**70** Chap. 7. Divide-and-Conquer
```
   carry:Bit;
 begin{LongAdd}
  carry:=0;
  for index:=1 to Precision do
   begin{for}
    digitsum:=result[index]+summand[index]+carry;
    carry:=digitsum div 2;
    result[index]:=digitsum mod 2;
   end;{for}
  if carry>0 then LongError(LongOverflow)
 end;{LongAdd}

```
Joe carefully implemented the naive multiplication algorithm from Problem 252
as procedure LongMultiply, and the divide-and-conquer multiplication algorithm as
procedure FastLongMultiply. Both of these procedures worked perfectly. However,
he found that LongMultiply was faster than FastLongMultiply, even when he tried
multiplying 2[n] 1 by itself (which is guaranteed to make LongMultiply slow). Joe’s
_−_
data show that as n increases, FastLongMultiply becomes slower than LongMultiply
by more than a constant factor. Figure 7.1 shows his running times, and Figure 7.2
their ratio.

325. Show that the worst case for the naive integer multiplication algorithm
is, as claimed above, multiplying 2[n] 1 by itself.
_−_

326. What did Joe do wrong?

327. What can Joe do to fix his program so that FastLongMultiply is faster
than LongMultiply for large enough n?

Complete the design of the following algorithm for performing integer multiplication using O(n[1][.][585]/(log n)[0][.][585]) bit-operations. First, construct a table of all k-bit
products. To multiply two n-bit numbers, do the following. Perform the divideand-conquer algorithm with the base of recursion n _k. That is, if n_ _k, then_
_≤_ _≤_
simply look up the result in the table. Otherwise, cut the numbers in half and
perform the recursion as normal.

328. Show that a table of all k-bit products can be constructed using O(k4[k])
bit-operations.

329. Devise and solve a recurrence relation for the divide-and-conquer
multiplication algorithm when the base of recursion is T (n) = O(1) for all
_n_ _k. Your solution must be a function of both n and k._
_≤_

330. Show that the best value of k is Θ(log n), and that this gives an
algorithm that uses O(n[1][.][585]/(log n)[0][.][585]) bit-operations, as claimed.


-----

Sec. 7.2. Integer Multiplication **71**

###### Comparison of Multiplication Algorithms

Time (ms) x 10[6]

2.00

FastLongMultiply

1.90 LongMultiply

1.80

1.70

1.60

1.50

1.40

1.30

1.20

1.10

1.00

0.90

0.80

0.70

0.60

0.50

0.40

0.30

0.20

0.10

0.00

3
n x 10

0.00 0.50 1.00 1.50 2.00 2.50

**Figure 7.1.** Running times for procedures LongMultiply
and FastLongMultiply observed by Joe D. Student.


-----

**72** Chap. 7. Divide-and-Conquer

###### Ratio of Running Times


60.00

55.00

50.00

45.00

40.00

35.00

30.00

25.00

20.00

15.00

10.00

5.00


Ratio


0.00 3
n x 10

0.00 0.50 1.00 1.50 2.00 2.50

**Figure 7.2. The ratio of the running times for procedures**
LongMultiply and FastLongMultiply observed by Joe D. Student.


-----

Sec. 7.3. Strassen’s Algorithm **73**

###### 7.3 STRASSEN’S ALGORITHM

Strassen’s algorithm is a divide-and-conquer algorithm for multiplying n _n matrices_
_×_
in time O(n[2][.][81]). The key ideas behind the algorithm are that 2 2 matrices
_×_
can be multiplied using only seven multiplications instead of the usual eight (see
Problems 263 and 297), and that this can be used as the base of recursion in a
divide-and-conquer algorithm.

331. The standard description of Strassen’s algorithm assumes that n is a
power of 2. Devise an algorithm that runs in time O(n[2][.][81]) when n is not
necessarily a power of 2.

332. Suppose we were to come up with a variant of Strassen’s algorithm based
on the fact that 3 3 matrices can be multiplied in only m multiplications
_×_
instead of the normal 27. How small would m have to be for this algorithm
to be faster than Strassen’s algorithm for large enough n?

333. The current record for matrix multiplication is O(n[2][.][376]), due to Coppersmith and Winograd [18]. How small would m need to be in Problem 332
in order to improve on this bound?

Another version of Strassen’s algorithm uses the following identities. To compute

� _A_ _B_ � � _E_ _F_ � � _I_ _J_ �

= _,_

_C_ _D_ _G_ _H_ _·_ _K_ _L_


first compute the following values:

_s1 = G + H_ _m1 = s2s6_ _t1 = m1 + m2_
_s2 = s1_ _E_ _m2 = EI_ _t2 = t1 + m4_
_−_
_s3 = E −_ _G_ _m3 = FK_
_s4 = F −_ _s2_ _m4 = s3s7_
_s5 = J −_ _I_ _m5 = s1s5_
_s6 = L −_ _s5_ _m6 = s4L_
_s7 = L −_ _J_ _m7 = Hs8_
_s8 = s6_ _K._
_−_

Then,

_A_ = _m2 + m3_
_B_ = _t1 + m5 + m6_
_C_ = _t2 −_ _m7_
_D_ = _t2 + m5._

334. Prove that this algorithm is correct.


-----

**74** Chap. 7. Divide-and-Conquer

335. Analyze its running time. Is it likely to be faster or slower than the
standard version of Strassen’s algorithm in practice?

###### 7.4 BINARY SEARCH

Binary search is a classic divide-and-conquer algorithm that is usually covered in
more elementary courses, but deserves to be dusted off again for a brief inspection
during the algorithms course. I usually teach it for n a power of 2, and leave the
extension to general n as an exercise (Problem 336).

336. Show that the number of comparisons used by the binary search
algorithm when n is not necessarily a power of 2 is at most log n .
_⌈_ _⌉_

337. What is wrong with the following binary search algorithm?

**function search(A, x, ℓ, r)**
**comment find x in A[ℓ..r]**
**if ℓ** = r then return(ℓ)
**else**
_m :=_ (ℓ + r)/2
_⌊_ _⌋_
**if x** _A[m]_
_≤_
**then return(search(A, x, ℓ, m))**
**else return(search(A, x, m, r))**

338. Is the following algorithm for binary search correct? If so, prove it. If
not, give an example on which it fails.

**function search(A, x, ℓ, r)**
**comment find x in A[ℓ..r]**
**if ℓ** = r then return(ℓ)
**else**
_m :=_ _ℓ_ + (r _ℓ_ + 1)/2
_⌊_ _−_ _⌋_
**if x** _A[m]_
_≤_
**then return(search(A, x, ℓ, m))**
**else return(search(A, x, m + 1, r))**

339. Do an exact analysis for the average number of comparisons used
by binary search for successful searches, assuming that all elements in the
sequence are accessed with equal probability.

340. Use the binary search technique to devise an algorithm for the problem of finding square-roots of natural numbers: Given an n-bit natural number
_N_, compute _n_ using only O(n) additions and shifts.
_⌈[√]_ _⌉_


-----

Sec. 7.5. Quicksort **75**

The following problems ask you to modify binary search in some way. For each of
them, write pseudocode for the algorithm, devise and solve a recurrence relation for
the number of comparisons used, and analyze the running time of your algorithm.

341. Modify the binary search algorithm so that it splits the input not into two
sets of almost-equal sizes, but into two sets of sizes approximately one-third
and two-thirds.

342. Modify the binary search algorithm to give a ternary search algorithm
that splits the input not into two sets of almost-equal sizes, but into three sets
of sizes approximately one-third.

343. Let T [1..n] be a sorted array of distinct integers. Give a divide-andconquer algorithm that finds an index i such that T [i] = i (if one exists) and
runs in time O(log n).

###### 7.5 QUICKSORT

The following is a high-level version of Hoare’s quicksort algorithm. Suppose S is a
set of numbers.

**function quicksort(S)**
1. **if** _S_ 1
_|_ _| ≤_
2. **then return(S)**
3. **else**
4. Choose an element a from S
5. Let S1, S2, S3 be the elements of S that are respectively <, =, > a
6. **return(quicksort(S1),S2,quicksort(S3))**

The operation described in line 5 is known as pivoting on a.

344. The median of a set of n values is the _n/2_ th smallest value. Suppose
_⌈_ _⌉_
quicksort were to always pivot on the median value. How many comparisons
would be made then in the worst case?

345. Suppose quicksort were to always pivot on the _n/3_ th smallest value.
_⌈_ _⌉_
How many comparisons would be made then in the worst case?

An α-pseudomedian of a list of n distinct values (where 0 < α < 1) is a value that
has at least n[α] list elements larger than it, and at least n[α] list elements smaller than
it. The following is a divide-and-conquer algorithm for computing a pseudomedian
(that is, an α-pseudomedian for some value of α to be determined later). Assume


-----

**76** Chap. 7. Divide-and-Conquer

_n is a power of 3. If n = 3, then simply sort the 3 values and return the median._
Otherwise, divide the n items into n/3 groups of 3 values. Sort each group of
3, and pick out the n/3 medians. Now recursively apply the procedure to find a
pseudomedian of these values.

346. Let T (n) be the number of comparisons used by the preceding algorithm
for computing a pseudomedian. Write a recurrence relation for T (n), and
solve it exactly. Hence, show that the algorithm runs in time O(n).

347. Let E(n) be the number of values that are smaller than the value
found by the preceding algorithm. Write a recurrence relation for E(n), and
hence prove that the algorithm does return a pseudomedian. What is the
value of α?

348. Any odd number can be used instead of 3. Is there any odd number
less than 13 which is better? You may use the following table, which gives
the minimum number of comparisons S(n) needed to sort n 11 numbers.
_≤_

_n_ 1 2 3 4 5 6 7 8 9 10 11

_S(n)_ 0 1 3 5 7 10 13 16 19 22 26

349. Suppose the pseudomedian algorithm is used to find the pivot
value in quicksort. Does it improve the worst-case number of comparisons
made?

The following is an implementation of Quicksort on an array S[1..n] due to Dijkstra [21]. You were asked to prove it correct in Problem 279 and analyze it in
Problem 313.

1. **procedure quicksort(ℓ, r)**
2. **comment sort S[ℓ..r]**
3. _i := ℓ; j := r;_
4. _a := some element from S[ℓ..r];_
5. **repeat**
6. **while S[i] < a do i := i + 1;**
7. **while S[j] > a do j := j** 1;
_−_
8. **if i** _j then_
_≤_
9. swap S[i] and S[j];
10. _i := i + 1; j := j_ 1;
_−_
11. **until i > j;**
12. **if ℓ< j then quicksort(ℓ, j);**
13. **if i < r then quicksort(i, r);**

350. How many comparisons does it use to sort n values in the worst case?

|n|1|2|3|4|5|6|7|8|9|10|11|
|---|---|---|---|---|---|---|---|---|---|---|---|
|S(n)|0|1|3|5|7|10|13|16|19|22|26|


-----

Sec. 7.6. Towers of Hanoi **77**

351. How many comparisons does it use to sort n values on average ?

352. Suppose the preceding algorithm pivots on the middle value, that is,
line 4 is replaced by a := S[ (ℓ + r)/2 ]. Give an input of 8 values for which
_⌊_ _⌋_
quicksort exhibits its worst-case behavior.

353. Suppose the above algorithm pivots on the middle value, that is,
line 4 is replaced by a := S[ (ℓ + r)/2 ]. Give an input of n values for which
_⌊_ _⌋_
quicksort exhibits its worst-case behavior.

###### 7.6 TOWERS OF HANOI

The Towers of Hanoi problem is often used as an example of recursion in introductory programming courses. This problem can be resurrected later in an algorithms
course, usually to good effect. You are given n disks of differing diameter, arranged
in increasing order of diameter from top to bottom on the leftmost of three pegs.
You are allowed to move a single disk at a time from one peg to another, but you
must not place a larger disk on top of a smaller one. Your task is to move all
disks to the rightmost peg via a sequence of these moves. The earliest reference to
this problem known to the author is Edouard Lucas [55] in Graham, Knuth, and[´]
Patashnik [30].

354. How many moves does the divide-and-conquer algorithm use?

355. Show that the following algorithm solves the Towers of Hanoi
problem. Think of the pegs as being arranged in a circle, with clockwise moves
being from peg 1 to peg 2 to peg 3 to peg 1. If n is odd, then start by moving
the smallest disk one jump in the counterclockwise direction. Alternate between moving the smallest disk in this manner and the only other legal move
available. If n is even, then start by moving the smallest disk one jump in
the clockwise direction. Alternate between moving the smallest disk in this
manner and the only other legal move available.

356. Prove that any algorithm that solves the Towers of Hanoi problem must
make at least 2[n] 1 moves.
_−_

Each of the following problems asks you to devise a divide-and-conquer algorithm
for a variant of the Towers of Hanoi problem. Write pseudocode for each algorithm,
prove that it is correct, and analyze the number of moves made.

357. Devise a divide-and-conquer algorithm for the Towers of Hanoi
problem when moves between peg 1 and peg 3 are not allowed (that is, all
moves must be either to or from peg 2).


-----

**78** Chap. 7. Divide-and-Conquer

358. Devise an efficient divide-and-conquer algorithm for the Towers of Hanoi
problem when there are 2n disks of n different sizes, two of each size, and you
are not allowed to put a larger disk on top of a smaller one (but you can put
a disk on top of a same-size one).

359. Devise an efficient divide-and-conquer algorithm for the Towers of
Hanoi problem when all moves must be in a clockwise direction (that is, from
peg 1 to peg 2, from peg 2 to peg 3, or from peg 3 to peg 1.)

360. Devise an efficient divide-and-conquer algorithm for the Towers
of Hanoi problem that works when the disks are started in any legal position
(and still moves all disks to peg 3). How many moves does your algorithm
make?

361. Devise a divide-and-conquer algorithm for the Towers of Hanoi
_√_
problem when there are four pegs, using at most O(n2 2n) moves.

362. Devise a divide-and-conquer algorithm for the Towers of Hanoi
problem when there are k 4 pegs, using at most O( _[√]w_ _n[2]_ 2[w][ w][√][n/]√2) moves,
_≥_ _·_

where w = k 2 is the number of work-pegs.
_−_

363. Devise an efficient divide-and-conquer algorithm for the Towers of
Hanoi problem when the disks are colored alternately red and blue, and we
add the extra rule that no disk may be placed on any other disk of the same
color.

###### 7.7 DEPTH-FIRST SEARCH

_Depth-first search is a search technique for directed graphs. Among its many ap-_
plications, finding connected components of a directed graph and biconnected components of an undirected graph are the ones most commonly covered in algorithms
courses. Depth-first search is performed on a directed graph G = (V, E) by executing the following procedure on some v _V :_
_∈_

**procedure dfs(v)**
1. mark v used
2. **for each w** _V such that (v, w)_ _E do_
_∈_ _∈_
3. **if w is unused then**
4. mark (v, w) used
5. dfs(w)

The set of marked edges form a depth-first spanning tree of a connected component
of G.


-----

Sec. 7.8. Applications **79**

+

+ /

2                  - 5

3 4

**Figure 7.3. A DAG representing the arithmetic expression**
2 + 3 4 + 5/(3 4).
_∗_ _∗_

364. Suppose an arithmetic expression is given as a DAG (directed acyclic
graph) with common subexpressions removed. For example, the expression
2+3 4+5/(3 4) would be given as the DAG shown in Figure 7.3. Devise an
_∗_ _∗_
algorithm for evaluating such a DAG with out-degree 2 (that is, all vertices
have at most 2 outgoing edges) in time O(n).

365. An undirected graph G = (V, E) is said to be k-colorable if all the
vertices of G can be colored using k different colors such that no two adjacent
vertices have the same color. Design an algorithm that runs in time O(n + e)
to color a graph with two colors or determine that the graph is not 2-colorable.

366. A triangle in an undirected graph G = (V, E) is a set of three pairwise
distinct vertices u, v, w _V such that (u, v)_ _E, (v, w)_ _E, and (u, w)_ _E._
_∈_ _∈_ _∈_ _∈_
Design an algorithm to test whether an undirected graph has a triangle. If G
has n vertices and e edges, then your algorithm should run in time O(n + e).

367. Design an algorithm that, given a directed graph G = (V, E) and a
distinguished vertex s _V, determines for each v_ _V the shortest path from_
_∈_ _∈_
_s to v. If G has n vertices and e edges, then your algorithm must run in time_
_O(n + e)._

368. A forest is a graph composed of zero or more disconnected trees.
Design an algorithm that, given a graph G with n nodes, determines whether
_G is a forest in time O(n)._

###### 7.8 APPLICATIONS

The following problems ask you to solve new problems using divide-and-conquer.
For each of your algorithms, describe it in prose or pseudocode, prove it correct,
and analyze its running time.


-----

**80** Chap. 7. Divide-and-Conquer

369. Devise a divide-and-conquer algorithm for constructing a closed knight’s tour on an n _n chessboard for all even n_ 6 (see
_×_ _≥_
Problem 48 for definitions). Your algorithm must run in time O(n[2]).

370. The longest ascending subsequence problem is defined as follows.
Given an array A[1..n] of natural numbers, find the length of the longest
ascending subsequence of A. (A subsequence is a list A[i1], A[i2], . . ., A[im]
for some 1 ≤ _i1 < i2 < · · · < im ≤_ _n. The value m is called the length of_
the subsequence. Such a subsequence is called ascending if A[i1] ≤ _A[i2] ≤_

_· · · ≤_ _A[im].) Devise a divide-and-conquer algorithm for solving the longest_
ascending subsequence problem in time O(n[2]).

371. The maximum subsequence sum problem is defined as follows.
Given an array A[1..n] of natural numbers, find values of i and j with 1 _i_
_≤_ _≤_
_j_ _n such that_
_≤_
_j_
� _A[k]_

_k=i_

is maximized. Devise a divide-and-conquer algorithm for solving the maximum subsequence sum problem in time O(n log n).

372. Devise a divide-and-conquer algorithm for multiplying n complex numbers using only 3(n 1) real multiplications.
_−_

373. Suppose we are given a set of n numbers k1, . . ., kn, where each
_ki has an associated weight wi ≥_ 0 such that [�]i[n]=1 _[w][i][ = 1. The weighted]_
median of the set {(ki, wi) | 1 ≤ _i ≤_ _n} is the number km such that_

� _wl <_ [1] � _wl_

2 _[,]_ _≥_ [1]2 _[.]_

_kl<km_ _kl≤km_


For example, given

_k1 = 4.13, k2 = 2.76, k3 = 9.00, k4 = 3.09, k5 = 7.65,_

_w1 = 0.30, w2 = 0.15, w3 = 0.25, w4 = 0.10, w5 = 0.20_

the weighted median is k1 = 4.13 because

� _wl = w2 + w4 = 0.15 + 0.10 = 0.25,_

_kl<4.13_


� _wl = w2 + w4 + w1 = 0.15 + 0.10 + 0.30 = 0.55._

_kl≤4.13_

Design an efficient (that is, linear time) algorithm to find the weighted median. (Note that the kis need not be given in sorted order.) Prove that your
algorithm performs as claimed.


-----

Sec. 7.9. Hints **81**

374. An induced subgraph of a graph G = (V, E) is a graph H = (U, F )
such that U _V, and F = E_ (U _U_ ). Given an undirected graph G = (V, E)
_⊆_ _∩_ _×_
and an integer k, find the maximum induced subgraph H of G such that each
vertex in H has degree at least k, or determine that it does not exist. The
algorithm should run in time O(n + e).

375. Find an algorithm that, given a connected graph in which all
vertices have even degree, constructs an Eulerian cycle in time O(n + _e). (See_
also Problem 69.)

376. Let G = (V, E) be a directed graph (not necessarily acyclic). Design
an efficient algorithm to label the vertices of the graph with distinct labels
from 1 to _V_ such that the label of each vertex v is greater than the label of
_|_ _|_
at least one of v’s predecessors (if v has any), or to determine that no such
labeling is possible (w is a predecessor of v iff (w, v) _E). Your algorithm_
_∈_
should run in time O(n + e).

377. Given two sorted sequences with m, n elements, respectively, design
and analyze an efficient divide-and-conquer algorithm to find the kth element in the merge of the two sequences. The best algorithm runs in time
_O(log(max(m, n)))._

###### 7.9 HINTS

317. Separate the n numbers into disjoint subsets (finding the right decomposition
is crucial) and first run the known recursive algorithm on the subsets.

324. Observe that x is computed using only six multiplications of n/3-bit integers,
plus some additions and shifts. Solve the resulting recurrence relation.

326. Start by deriving and solving a recurrence relation for the number of times
that Joe’s procedure LongAdd is called by procedures LongMultiply and FastLongMultiply.

355. Show that this algorithm makes exactly the same moves as the standard
divide-and-conquer algorithm.

357. No, it is not enough to use the standard algorithm and replace every move
from peg 1 to peg 3 (for example) with two moves to and from peg 2. That
may require you to place a large disk on top of a small one.

359. No, it is not enough to use the standard algorithm and replace every counterclockwise move with two clockwise moves. That may require you to place a
large disk on top of a small one. It is possible to devise a divide-and-conquer


-----

**82** Chap. 7. Divide-and-Conquer

algorithm for moving all of the disks one peg clockwise using (4[n] 1)/3 moves.
_−_
This can be used to solve the Towers of Hanoi problem (which is to move all of
the disks one peg counterclockwise) in 2(4[n] 1)/3 moves. The best algorithm
_−_
_√_
known to the author uses less than (1 + 3)[n] 1 = O(2.73[n]) moves.

_−_

361. An analysis of a k-peg algorithm by Lu [54] can be found in in Veerasamy
and Page [81]. We are interested in the case k = 4, which slightly simplifies
the analysis. In addition, the analysis is much simpler if you prove it by
induction. If you try to pass off their analysis as your own, it is long enough
and idiosyncratic enough that your instructor will be sure to recognize it.


_w[√]_
362. An algorithm by Lu [54] was shown to use at most n2 _w!·n moves by Veerasamy_

and Page [81]. (If you read their paper, note that their k is the number of
work pegs, which is w in our notation.) The algorithm that I have in mind
has recurrence T (k, n) = T (k/2 + 1, _n)[2]._

_[√]_

363. Surprisingly, the standard algorithm solves this problem. You can prove it
by induction on n, but be careful about the bottom disk on each peg. The
induction hypothesis will have to be stronger than just the statement of the
required result. To get the idea, play with some examples.

365. Take note of which section this problem is in.

368. It’s easy to do this in time O(n + e), but that is not what is asked for. A
problem from Chapter 2 is relevant.

369. In order to construct closed knight’s tours on square chessboards, you will
need a method for constructing tours on rectangular boards. If you are smart
enough, you will only need n (n + 2) tours. You will also need some extra
_×_
structure in your tours to enable them to be joined at the corners (see Problem 48). You will have to devise an exhaustive search algorithm for finding
small tours for the base of your divide-and-conquer (see Problem 513), or you
can make use of the tours shown in Figure 7.4.

374. Use the adjacency list representation. Store for each v _V an additional_
_∈_
field called its degree. Start by giving an algorithm that sets this field to the
correct value. Then write a divide-and-conquer algorithm that, given a vertex
_v of degree less than k, deletes that vertex from the graph, and all vertices of_
degree less than k that are adjacent to it. Apply this algorithm to solve the
required problem.

375. See Problem 69.


-----

Sec. 7.10. Solutions **83**

r r r r r r r r✟ **✟❍**

**❆[❍]✟✁❆✟❍✟[✟❍]❆** **[✟]✟❍✟❆✟[✟][✟]❍❆✁**

r r r r r r r r

**✁❆✁❆** **❆** **❆✁** **✁** **❆✟✁❆✁[✟]❆**

r r r r r r❍✟❍✟✟ r r r r r r r r✟❍✟❍ **✟❍✟** r r r r r r r r✟ **❍**

**❆✟✁❍❆✟✟[✟❍]❍✟❆❍✁** **❆[❍]✟✁❍✟[❍]** **❍✁✟❍[❍]✁✟❍❆❍✁** **❆✟✁✁❆** **✁** **❆✁** **❆** **✁❍❆❆✁**

r r r r r r✟ r r r r r r r r r r r r r r r r✟❍ **❍**

**✁❍❍❆✁** **❆✟✁✁❆** **❍❍✁❆✁** **✁❍❍❍✟✟✁** **✁** **✁❆❆** **✁❆❆** **❆✟** **✁❆❍❆** **❍❆✁✁❆**

r r r r r r r r r r r r r r❍ r r r r r r r r✟

**❆✁❆❍❍✁❍❍❆❆✁** **✁❆** **✁** **❍❆** **❆** **❆** **❆✁❆** **❆✟✁** **❆✁❆[❍]✁❍** **✁❆❆**

r r r r r r r r r r r r r r✟ **✟** r r r r r r r r

**✟❆✁❆[✟❍]❍✁❆✁** **❆✟✁❆** **✁** **✁** **❆✟✁❆** **❆✁** **✁❆✁❆❆** **❆❍❍❆❆[❍]❆❍❆✁❆**

r r r r r r❍✟✟❍❍ r r r r r r r r❍ r r r r r r r r❍❍✟❍ **✟❍✟✟**

**✁✟❆❍❍✟✟❆❆❍✟❆** **❍❍✁❆** **✁❍❍✁✟❆✁[✟✟✟✁]❍❆❍❍✟✟❆✁** **✁✟❆❍❍❆[✟✁]❆✁** **✁✟❆✟❍❆❍[✟✁]✟❍✟❆✟❆✁❍❆**

r r r r r r r r r r r r r r r r r r r r r r

|r❍|r✟|r❍✟|r✟❍|r✟|r|
|---|---|---|---|---|---|
|❆✟ r❍|✁❍❆✟ r|✟ r|❍✟ r|❆❍ r✟|✁ r|
|✁ r|❆✁❍ r❍|❆ r|❆✟ r❍|✁✁ r|❆ r|
|❆✁ r|r✟|❍ r❍|✁ r|❆❆❍ r|✁ r|
|✟❆ r❍|✁❆❆ r❍✟|r✟❍|❍ r❍|✁❆ r✟|❆✁ r|
|✁✟ r|❆❍✟ r|❆❍ r|✟❍ r|❍✁ r|❆ r|

|❍r|✟r❍|❍✟r|❍r|r❍|✟r❍|✟r|r|
|---|---|---|---|---|---|---|---|
|❆✟ ❍r|✁❍✟ r|❍ r|❍ r❍|✁✟❍ r|✁✟❍ r|❆❍ r✟|✁ r|
|✁ r|❆✁❍ ❍r|✁ r|✁ r|✁❍ r|✟ r|✁❆ r|❆ r|
|✁❆ r|✁ ✟r|❍❆ r|❆ r✟|❆ r|r✟|❆ r|✁❆ r|
|❆✟ ❍r|✁❆ r✟❍|✁✟ r|✁❆ ❍r|❆✁✟ r|✁❆❆ ✟r❍|✁❆ ✟r|❆✁ r|
|✁✟ r|❆❍✁ r|✁❍ r|✁ r|✁✟❍ r|✟ r|❆❍✁ r|❆ r|

|r|❍ r|✟ r|✟ r|❍✟ r|✟ r|❍✟ r|✟ r|
|---|---|---|---|---|---|---|---|
|❆ r|✟✁❆ r|✟❍❆ r|✟ r|✟❆ r|❍✟ r|✟❆ r|❍✁ ✟ r|
|✁❆ r|✁❆ r|❆ ✟ r|❆✁ r|✁ r|❆ ❍ r|✟✁✁❆ r|❆ r|
|❆✁ r|✟✁❆ r|✁ r|❆✁ r|❆ ✟❍ r|✁ r|❍❆ ❍ r|❆✁ r|
|✁ r|❆❆ r|❆ ✟ r|✟ r|✁❆ ❍ r|❍❆ r|❆✁ r|❍❆✁ r|
|❆ r|✟✁ r|❆ r|❆✁❆ ❍ r|✁ r|❍ ❍ r|✁❆ r|❆ r|
|✁❆ r|✁❆❆ ❍ r|❍✟ r|✁ ✟❍ r|❍❆❆ r|❆ ✟ r|❍❆ ❍✟ r|✁❆ ✟ r|
|✁ r|✟❆ r|❍✟❆ r|❍ r|✟❍ r|✟❆ r|✟❆✁ r|❍❆ r|


r r r r r r r r r r❍✟❍ **✟❍✟✟** **✟✟** r r r r r r r r r r r r

**❆✟✁❍✟❆❍✁[❍]✟✟❍✟✁❍✟❆[✟❍]✟❆❍✁** **❆[❍]✟✁✟❍[✟][❍]✁[✟❍]❍✟✁❆❍✟[✟❍]✟[✟][✟❍]❍✟❆** **✁❍✟[✟❍][❍]❍✁❆[✟]❍✁**

r r r r r r r r r r r r r r r r r r r r r r✟

**❍❍✁✁❆[❍]❍❆** **❆✁** **❆❍❍❆✁✁❆✁** **✟✁❆✁❆✁** **✁✁✟❆[✟]✁** **❆✁✁❆** **✁** **✁❆✁❆**

r r r r r r r r r r✟❍ **✟❍** r r r r r r r r r r❍ r r r r r r r r r r r r✟ **❍✟** **✟** **❍**

**❆[❍]✟✁✟❍✟[❍][✟❍]❍✟[✟❍]❍❍✟✟[✟]✁❍✟[✟❍]❍✟[✟]❍[✟]❆✁** **✁✁❍❍✁** **✟[✟]✁❍✁❆✁✁** **❆✁❆** **✟✁❆** **✁** **✁✟✁** **✁❍✁❆✟** **❆❆** **❆✁❍✁❆**

r r r r r r r r r r❍ r r r r r r r r r r❍ **❍** r r r r r r r r r r r r❍✟❍✟ **✟**

**✁❍❍✁❆** **❆✁❍✁❆** **✁✁❍❆✁** **❆** **✁❆[❍]❆❍❍❆✁❍✁✁❍❆❆✁** **✁✁** **✟✁❆** **✟❍** **✁✟❍[✟✁]✟** **❆✁** **❆✁❆**

r r r r r r r r r r❍ r r r r r r r r r r❍ r r r r r r r r r r r r❍

**✁✁✟❍✁[✟]✁** **✟✁[✟][❍]❆❍✁❆** **✁❆** **✁✟❆** **[✟]❆✁** **❍❆[❍]✁❍❆❆** **✁** **✁✁✁❆** **❆[❍]✁✁❍** **❆❆** **✟❍[✟❆]✟✁✁[❍][✟❆]❆❍❆✁❆**

r r r r r r r r r r❍ **✟** r r r r r r r r r r✟ **✟** r r r r r r r r r r r r❍✟ **✟**

**❆✁** **❆✁** **✁❆✁✟✁❆[✟]❍✁❍❍❍❍❆❆✟✁❆✟❆[✟❆]❆** **✟❆✁[✟❆]❆✟✁❆[✟❆]❆** **✟✁❆** **✁✟✁✁✁** **✟✁❆❍❆[❍]❍✁** **✁❆✟[❍]✁❍[✟]** **✁✁** **❆✟✁** **✁✁❆**

r r r r r r r r r r✟ **❍✟** r r r r r r r r r r✟ **✟✟** **✟** r r r r r r r r r r r r✟ **❍✟**

**❆✟❆✁** **❆✁❆❆** **✟❍❆** **❆✁** **❆✁✁✟** **✟❆✟❆** **✁** **✁** **✟✁** **❆✁** **✟✁[✟]❆✁** **❆** **✟✁✁[❍]✟✁❍** **❍❆❆[❍]❆✁❍✁**

r r r r r r r r r r✟ r r r r r r r r r r✟ **✟** **✟** r r r r r r r r r r r r

**❆✁❆** **✁** **❆❆** **✟❆[❍]❍✁❆✁** **❆✁❆✟✁❆** **✟** **✁** **✟✁❆✁** **✁❆✁❆✟[✟✁]❆✁✁❆** **✟[✟✁]❆** **❆❆✁❆✁**

r r r r r r r r r r❍✟❍ **✟❍❍✟** **✟✟** r r r r r r r r r r r r r r r r r r r r r r❍❍✟✟❍❍✟❍✟❍❍✟✟❍❍✟

**✁✁❍❍✁✟❆✟❍[✟✟✟❆]✟❍✟❆✟❍❍✟[✟❍]✟❆✁❍❆** **✟✁✁❍❍✟✟❍❍✟✟✁❆✁[✟❍]❆✟❍✟❍❍✁[✟❆][✟❍]✁✟❍❍❆❍✁[✟❆]** **✁✟❆❍✟❆❍✟❍❍✁** **✟❆❍✟✟❍❆❍✟❍❍✁❆**

r r r r r r r r r r r r r r r r r r r r r r r r r r r r r r r r

**Figure 7.4. Knight’s tours for (in row-major order) 6** 6,
_×_
6 8, 8 8, 8 10, 10 10, and 10 12 boards.
_×_ _×_ _×_ _×_ _×_

###### 7.10 SOLUTIONS

314. Here is a full solution when n is not necessarily a power of 2. The size of
the problem is the number of entries in the array, y _x + 1. We will prove_
_−_
by induction on n = y _x + 1 that maximum(x, y) will return the maximum_
_−_
value in S[x..y]. The algorithm is clearly correct when n 2. Now suppose
_≤_
_n > 2, and that maximum(x, y) will return the maximum value in S[x..y]_
whenever y _x + 1 < n. In order to apply the induction hypothesis to the_
_−_
first recursive call, we must prove that (x + y)/2 _x + 1 < n. There are_
_⌊_ _⌋−_
two cases to consider. If y _x + 1 is even, then y_ _x is odd, and hence y + x_
_−_ _−_
is odd. Therefore,

� _x + y_ �

_x + 1 =_ _[x][ +][ y][ −]_ [1] _x + 1 =_ _[y][ −]_ _[x][ + 1]_ = _[n]_
_−_ _−_

2 2 2 2 _[< n.]_

|r❍|r|✟❍ r✟❍|r❍✟|r❍✟|r✟|r✟❍|r❍✟|r✟|r|
|---|---|---|---|---|---|---|---|---|---|
|❆✟ r❍|✁ r|✟❍✟❍ r|❍✟ r|❍✟ r|✁✟❍ r|✟ r|✟❍ r❍|❍❆ r|✁ r|
|✁ r❍|✁❆ r|❍ r✟|r|✁ r❍|r✟❍|r|r|❍✁❆ r|✁❆ r|
|✁ r|✁ r|✟❍✁ r|✁ r❍|✟ r✟|✁❍ r|❆❍ r✟❍|✁❆ r|✁❆ r✟|❆ r|
|❆✁ r|❆✁ r|✁❆ ✟ r|✁✟ r|✁❆❍ r❍|❆✟ r✟|✁ r|❆✟❍ r|❆❆ r|❆ r|
|❆✟ r|❆✁ r|❆✁ r|❆❆ r|✟ r✟|❆❍ r|❆ r|r❍✟|r|❆✁ r|
|❆✁ r❍|✁❆ r|❍✟ r✟❍|✁✟ r|❆❆ r✟❍|r❍✟|✟ r✟|❆ r✟❍|❍✁❆ r✟|✁ r|
|✁✟ r|❆ r|✟❍❍✁ r|✟❍ r|✟ r|❆❍✟ r|❍✟ r|✟ r|❆✁❍ r|❆ r|

|r|❍ r✟❍|r|r✟❍|r❍✟|r✟|r✟|r✟❍|r✟|r|
|---|---|---|---|---|---|---|---|---|---|
|❆ r|✟✁❍ ❍ r❍|✟❆❍ r|✁✟ r|✟❍ r|✁❍✟ r|✟❆ r|✟ r❍|❆❍ r|✁ r|
|✁ r|✁❆❍ ❍ r|❍✁ r|❆ r|❆✁ r✟❍|r|r|❆ r|✁✁❍❆ r|❆✁ r|
|✁ r|✁❍ ❍ r|r|✟ r|r❍|✁❆❍ r❍|✁❆ r❍|✁✁ r|❆✁ r|❆ r|
|✁ r|✁❍❆ r✟❍|✁ r|❆ r❍|✁❆ r|✁❍ r|✁❍ r|✁❆❍ r|❆ r|❆✁ r|
|✁❆ r|✟❆✁ r✟|❆❍ r|❆ r✟|✁❆❍ r|❆❆ r|✁ r✟|r|✁✁ r✟|✁❆ r|
|r|✟❆✁ r|❆✟ r✟|✁❆ r|❆ r✟|✟ r✟|✁❆ r|✁✟✁ r|✁✁ r✟|r|
|❆✁ r|✁✟ r|r✟|✟ r|❆✟❆ r✟|✁ r|✁ r|✟✁ r|❆ r✟|✁ r|
|✁❆ r|✁❆✟ ❍ r✟|✁❆ r❍|✟ r❍✟|r❍✟|❆ r✟|✁ r❍|✟ r❍✟|✁❆✁ r✟|❆✁ r|
|✁ r|✟❆❍✁ r|✟ r|❆❍✟ r|❍✟ r|✁❍ r|✟ r|✁✟❍ r|❍✁ r|❆ r|

|r❍|r✟❍|r✟|r❍|r✟|r❍✟|r✟|r❍|r✟❍|r❍|r|✟ r|
|---|---|---|---|---|---|---|---|---|---|---|---|
|❆✟ r|✁✟❍ r✟|✁❍ r|✟ r|✁❍❆✟ r|✟ r✟|❍❆ r|✟ r|✁❍ r|✟❍ r|✁❆ r|❍✁ r|
|✟✁❆ r|✁❆✁ r✟|r|✁ r|✁✟ r❍✟|❆ r|✁ r|❆✁ r✟|✁❆ r|✁ r❍|✁❆ r|✁❆ r|
|✟✁ r|❆ r|✁ r❍|✁✟✁ r✟|r✟❍|✁❍ r|✁❆✟ r✟|✁ r✟|❆ r|❆ r|❆✁ r|❍❆✁ r|
|r❍|✁✁ r|✟✁❆ r|✟❍ r|r❍|✁✟❍ r|✟ r✟|❆ r|❆ r❍✟|✁❆ r|❆✁ r|❆ r|
|❆✁ r❍|✁❍ r✟❍|r|❆❆ r|r❍|✟❍ r✟|r|✟ r|✁✁ r|❆❍ r✟|❆ r|✁❆ r|
|✟✁ r|❆❍❆ r✟|❍ r|✁ r|✁❆✟ r|✁❍ r✟❍|r|✁✁ r❍✟|❆✟ r|✁ r❍|✁ r|✁❆ r|
|✟ r|✁ r|❆✁ r✟|✁❆ r|✟✁ r|✁ r|✟✁❍ r|r✟|❍✁ r|❆❆ r|❆✁ r|❍✁ r|
|✁❆ r❍|✁❆✟ r❍✟|r✟❍|r❍|❆✁ r✟|✁❆ r❍|✟ r✟❍|❆ r❍✟|r✟❍|r❍|❆❆✁ r|❆✁ ✟ r|
|✁✟ r|❆❍✟ r|❆❍ r|✟❍ r|❍✁ r|✟ r|❆❍✟ r|✟❍ r|❆❍ r|✟❍ r|✁ r|❍❆ r|


(The last inequality holds since n > 2.) If y _x +1 is odd, then y_ _x is even,_
_−_ _−_
and hence y + x is even. Therefore,

� _x + y_ �

_x + 1 =_ _[x][ +][ y]_ _x + 1 =_ _[y][ −]_ _[x][ + 2]_ = _[n][ + 1]_ _< n._
_−_ _−_

2 2 2 2

(The last inequality holds since n > 1.) In order to apply the induction
hypothesis to the second recursive call, we must prove that y ( (x + _y)/2_ +
_−_ _⌊_ _⌋_


-----

**84** Chap. 7. Divide-and-Conquer

1) + 1 < n. There are two cases to consider. If y _x + 1 is even, then_
_−_


�� _x + y_
_y_
_−_

2


� �
+ 1 + 1 = y = _[y][ −]_ _[x][ + 1]_ = _[n]_
_−_ _[x][ +][ y][ −]_ [1]

2 2 2 _[< n.]_


If y _x + 1 is odd, then_
_−_


�� _x + y_
_y_
_−_

2


� �
+ 1 + 1 = y = _[y][ −]_ _[x][ + 1]_ 1/2 = _[n]_
_−_ _[x][ +][ y]_ _−_

2 2 2 2 _[< n.]_

_[−]_ [1]


Procedure maximum divides the array into two parts. By the induction hypothesis, the recursive calls correctly find the maxima in these parts. Therefore, since the procedure returns the maximum of the two maxima, it returns
the correct values.

315. Let T (n) be the number of comparisons used by maximum(x, y), where n =
_y_ _x + 1 is the size of the array chunk processed. Then if n is a power of 2,_
_−_
_T_ (1) = 0, and for all n > 1 a power of 2, T (n) = 2T (n/2) + 1. Hence, using
the techniques of Chapter 4, T (n) = n 1.
_−_

316. The running time of procedure maximum is clearly a constant times the number of comparisons. Hence, by the preceding, it runs in time O(n).

354. Let T (n) be the number of moves it takes to move n disks from peg i to peg
_j. Clearly,_

� 1 if n = 1
_T_ (n) =
2T (n 1) + 1 otherwise.
_−_

Hence, using the techniques of Chapter 4, T (n) = 2[n] 1.
_−_

355. Let D be a direction, either clockwise or counterclockwise. Let D be the
opposite direction. To move n disks in direction D, we are told to alternate
between the following two moves:

If n is odd, move the smallest disk in direction D. If n is even, move the

_•_
smallest disk in direction D.
Make the only other legal move.

_•_

We claim that when the recursive algorithm is used to move n disks in direction D, it alternates between the preceding two moves. This is enough to
prove correctness of the new algorithm. The proof of the claim is by induction
on n. The claim is obviously true when n = 1. Now suppose that the claim is
true for n disks. Suppose we use the recursive algorithm to move n + 1 disks
in direction D. It does the following:

Move n disks in direction D.

_•_
Move one disk in direction D.

_•_
Move n disks in direction D.

_•_


-----

Sec. 7.11. Comments **85**

Let

“D” denote moving the smallest disk in direction D,

_•_
“D” denote moving the smallest disk in direction D, and

_•_
“O” denote making the only other legal move.

_•_

**Case 1. n + 1 is odd. Then n is even, and so by the induction hypothesis,**
moving n disks in direction D uses moves:

_DODO_ _OD._
_· · ·_

(Note that by Problem 354, the number of moves is odd, so the preceding
sequence of moves ends with D, not O.) Hence, moving n+1 disks in direction
_D uses_
_DODO_ _OD_ _O DODO_ _OD_ _,_
_· · ·_ _· · ·_
� �� � � �� �
_n disks_ _n disks_

as required.
**Case 2. n + 1 is even. Then n is odd, and so by the induction hypothesis,**
moving n disks in direction D uses moves

_DODO_ _OD._
_· · ·_

(Note that by Problem 354, the number of moves is odd, so the preceding
sequence of moves ends with D, not O.) Hence, moving n+1 disks in direction
_D uses moves:_

_DODO_ _OD_ _O DODO_ _OD_ _,_
_· · ·_ _· · ·_
� �� � � �� �
_n disks_ _n disks_


as required. Hence, by induction, the claim holds for any number of disks.

369. A solution to this problem appears in Parberry [62].

###### 7.11 COMMENTS

321. See also Problem 329.

329. See also Problem 321.

330. So where does this algorithm get its speed from? The secret is in Problem 320.
Although it is faster than the standard divide-and-conquer, there is a faster
algorithm than this one (see Sch¨onhage and Strassen [70]).

336. Binary search is normally described and analyzed for n a power of 2. This
problem asks you to extend this to any value of n.

349. I don’t propose this as a viable alternative to quicksort. This is just an
exercise in the design, correctness proof, and analysis of divide-and-conquer
algorithms.


-----

**86** Chap. 7. Divide-and-Conquer

354. According to legend, there is a set of 64 gold disks on 3 diamond needles being
solved by priests of Brahma. The Universe is supposed to end when the task is
complete. If done correctly, it will take T (64) = 2[64] 1 = 1.84 10[19] moves.
_−_ _×_
At one move per second, that’s 5.85 10[11] years. More realistically, at 1
_×_
minute per move (since the largest disks must be very heavy) during working
hours, it would take 1.54 10[14] years. The current age of the Universe is
_×_
estimated at 10[10] years. Perhaps the legend is correct.
_≈_

360. There is an algorithm that will do this using at most 2[n] 1 moves. There is
_−_
even one that is provably optimal.

369. Alternative algorithms for constructing closed knight’s tours on rectangular
chessboards appear in Cull and DeCurtins [20] and Schwenk [71].

370. There is a faster algorithm for this problem. See Problem 409.

371. There is an O(n) time algorithm for this problem.


-----

###### Chapter 8

### Dynamic Programming

_Dynamic programming is a fancy name for divide-and-conquer with a table. In-_
stead of solving subproblems recursively, solve them sequentially and store their
solutions in a table. The trick is to solve them in the right order so that whenever
the solution to a subproblem is needed, it is already available in the table. Dynamic
programming is particularly useful on problems for which divide-and-conquer appears to yield an exponential number of subproblems, but there are really only a
small number of subproblems repeated exponentially often. In this case, it makes
sense to compute each solution the first time and store it away in a table for later
use, instead of recomputing it recursively every time it is needed.
In general, I don’t approve of busy-work problems, but I have found that undergraduates don’t really understand dynamic programming unless they fill in a few
tables for themselves. Hence, the following problems include a few of this nature.

###### 8.1 ITERATED MATRIX PRODUCT

The iterated matrix product problem is perhaps the most popular example of dynamic programming used in algorithms texts. Given n matrices, M1, M2, . . ., Mn,
where for 1 ≤ _i ≤_ _n, Mi is a ri−1×ri matrix, parenthesize the product M1·M2 · · · Mn_
so as to minimize the total cost, assuming that the cost of multiplying an ri−1 × ri
matrix by a ri × ri+1 matrix using the naive algorithm is ri−1riri+1. (See also
Problems 91 and 263.) Here is the dynamic programming algorithm for the matrix
product problem:

**function matrix(n)**
1. **for i := 1 to n do m[i, i] := 0**
2. **for d := 1 to n** 1 do
_−_
3. **for i := 1 to n** _d do_
_−_
4. _j := i + d_
5. _m[i, j] := mini≤k<j(m[i, k] + m[k + 1, j] + ri−1rkrj)_
6. **return(m[1, n])**

378. Find three other orders in which the cost table m can be filled in
(ignoring the diagonal).

**87**


-----

**88** Chap. 8. Dynamic Programming

379. Prove that there are Ω(2[n]) different orders in which the cost table m can
be filled in.

Fill in the cost table m in the dynamic programming algorithm for iterated matrix
products on the following inputs:

380. _n = 4; r0 = 2, r1 = 5, r2 = 4, r3 = 1, r4 = 10._

381. _n = 4; r0 = 3, r1 = 7, r2 = 2, r3 = 5, r4 = 10._

382. _n = 5; r0 = 12, r1 = 2, r2 = 15, r3 = 16, r4 = 8, r5 = 3._

383. _n = 5; r0 = 8, r1 = 3, r2 = 2, r3 = 19, r4 = 18, r5 = 7._

Find counterexamples to the following algorithms for the iterated matrix products
problem. That is, find n, r0, r1, . . ., rn such that, when the product of the matrices
with these dimensions is evaluated in the order given, the cost is higher than optimal.

384. Suppose n > 2, and that ri is the smallest of r1, r2, . . ., rn−1. Break
the product after Mi, and recursively apply this procedure to the products
_M1_ _M2_ _Mi and Mi+1_ _M2_ _Mn._
_×_ _× · · · ×_ _×_ _× · · · ×_

385. Multiply left to right.

386. Multiply right to left.

387. Start by cutting the product in half, and then repeat the same thing
recursively in each half.

388. Suppose ri is the largest of r1, r2, . . ., rn−1. Start by multiplying Mi by
_Mi+1. Repeat this until the product has been evaluated._

389. Suppose ri is the smallest of r1, r2, . . ., rn−1. Start by multiplying Mi
by Mi+1. Repeat this until the product has been evaluated.

390. Suppose ri is the largest of r1, r2, . . ., rn−1. Break the product after Mi,
and recursively apply this procedure to the products M1 _M2_ _Mi and_
_×_ _× · · · ×_
_Mi+1 × M2 × · · · × Mn._


-----

Sec. 8.2. The Knapsack Problem **89**

###### 8.2 THE KNAPSACK PROBLEM

The knapsack problem (often called the zero-one knapsack problem) is as follows:
given n rods of length s1, s2, . . ., sn, and a natural number S, find a subset of the
rods that has total length exactly S. The standard dynamic programming algorithm
for the knapsack problem is as follows. Let t[i, j] be true if there is a subset of the
first i items that has total length exactly j.

**function knapsack(s1, s2, . . ., sn, S)**
1. _t[0, 0] :=true_
2. **for j := 1 to S do t[0, j] :=false**
3. **for i := 1 to n do**
4. **for j := 0 to S do**
5. _t[i, j] := t[i_ 1, j]
_−_
6. **if j −** _si ≥_ 0 then t[i, j] := t[i, j] ∨ _t[i −_ 1, j − _si]_
7. **return(t[n, S])**

391. Fill in the table t in the dynamic programming algorithm for the knapsack problem on a knapsack of size 19 with rods of the following lengths:
15, 5, 16, 7, 1, 15, 6, 3.

Fill in the table t in the dynamic programming algorithm for the knapsack problem
on a knapsack of size 10 with rods of the following lengths:

392. 1, 2, 3, 4.

393. 5, 4, 3, 6.

394. 2, 2, 3, 3.

Find counterexamples to the following algorithms for the knapsack problem. That
is, find S, n, s1, . . ., sn such that when the rods are selected using the algorithm
given, the knapsack is not completely full.

395. Put them in the knapsack in left to right order (the first-fit algorithm).

396. Put them in smallest first (the best-fit algorithm).

397. Put them in largest first (the worst-fit algorithm).


-----

**90** Chap. 8. Dynamic Programming

###### 8.3 OPTIMAL BINARY SEARCH TREES

Binary search trees are useful for storing a set S of ordered elements, with operations:

search(x, S): return true iff x _S,_
_∈_
min(S): return the smallest value in S,
delete(x, S): delete x from S,
insert(x, S): insert x into S.

The optimal binary search tree problem is the following. Given the following
three sets of data,

1. S = {x1, . . . xn}, where xi < xi+1 for all 1 ≤ _i < n,_
2. the probability pi that we will be asked member(xi, S), for 1 ≤ _i ≤_ _n,_
3. the probability qi that we will be asked member(x, S) for some xi < x < xi+1
(where x0 = −∞, xn+1 = ∞), for 0 ≤ _i ≤_ _n,_

construct a binary search tree (see also Section 11.2) that has the minimum number
of expected comparisons.
The standard dynamic programming algorithm for this problem is as follows. Let
_Ti,j be the min-cost binary search tree for xi+1, . . ., xj, and c[i, j] be the expected_
number of comparisons for Ti,j.

**function bst(p1, p2, . . ., pn, q0, q1, . . ., qn)**
1. **for i := 0 to n do**
2. _w[i, i] := qi; c[i, i] := 0_
3. **for ℓ** := 1 to n do
4. **for i := 0 to n** _ℓ_ **do**
_−_
5. _j := i + ℓ_
6. _w[i, j] := w[i, j −_ 1] + pj + qj
7. _c[i, j] := mini<k≤j(c[i, k −_ 1] + c[k, j] + w[i, j])
8. **return(c[0, n])**

Fill in the cost table c in the dynamic programming algorithm for the optimal
binary search tree problem on the following inputs.

398. _n = 4, p1 = 0.01, p2 = 0.11, p3 = 0.2, p4 = 0.12; q0 = 0.1, q1 = 0.1,_
_q2 = 0.28, q3 = 0.03, q4 = 0.05._

399. _n = 4, p1 = 0.15, p2 = 0.32, p3 = 0.02, p4 = 0.07; q0 = 0.01, q1 = 0.16,_
_q2 = 0.21, q3 = 0.02, q4 = 0.04._

400. _n = 4, p1 = 0.07, p2 = 0.22, p3 = 0.07, p4 = 0.17; q0 = 0.03, q1 = 0.03,_
_q2 = 0.21, q3 = 0.09, q4 = 0.12._


-----

Sec. 8.4. Floyd’s Algorithm **91**

(a) 50 (b) (c)

10 100

1 2 2 1

12 5

4 30 4 30 3 4
6 6

65 65 25 4 9 3 1 2

70


21


8


44

**Figure 8.1. Some graphs.**

###### 8.4 FLOYD’S ALGORITHM

The all-pairs shortest-paths problem is as follows. Given a labeled directed graph
_G = (V, E), find for each pair of vertices v, w_ _V the cost of the shortest (that_
_∈_
is, the least-cost) path from v to w in G. The standard dynamic programming
algorithm for the all pairs shortest paths problem (Floyd’s algorithm) is as follows.
Suppose V = 1, 2, . . ., n .
_{_ _}_

**function floyd(C, n)**
1. **for i := 1 to n do**
2. **for j := 1 to n do**
3. **if (i, j)** _E_
_∈_
4. **then A[i, j] := cost of edge (i, j)**
5. **else A[i, j] :=**
_∞_
6. _A[i, i] := 0_
7. **for k := 1 to n do**
8. **for i := 1 to n do**
9. **for j := 1 to n do**
10. **if A[i, k] + A[k, j] < A[i, j] then A[i, j] := A[i, k] + A[k, j]**
11. **return(A)**

401. Fill in the cost table A in Floyd’s algorithm on the graphs shown in
Figure 8.1.

402. Show that Floyd’s algorithm on an undirected graph chooses a minimum cost edge (v, w) for each vertex v. Can an all-pairs shortest-path algorithm be designed simply by choosing such a cheapest edge for each vertex?
What if all edge costs are different?

Modify Floyd’s algorithm to solve the following problems on directed graphs. Analyze your algorithms.


-----

**92** Chap. 8. Dynamic Programming

403. Determine the number of paths (possibly infinite) between each pair
of vertices.

404. Determine the number of even-length paths and of odd-length paths
between each pair of vertices.

405. Determine the number of shortest paths between each pair of vertices.

406. Given an n-vertex graph whose vertices are labeled with distinct integers from 1 to n, the label of each path is obtained by taking the labels of
vertices on the path in order. Determine the label and length of the lexicographically first shortest path between each pair of vertices.

###### 8.5 APPLICATIONS

The problems in this section ask you to apply dynamic programming in new situations. One way to proceed is to start by devising a divide-and-conquer algorithm,
replace the recursion with table lookups, and devise a series of loops that fill in the
table in the correct order.

407. A context-free grammar in Chomsky Normal Form consists of

A set of nonterminal symbols N .

_•_
A set of terminal symbols T .

_•_
A special nonterminal symbol called the root.

_•_
A set of productions of the form either A _BC, or A_ _a, where_

_•_ _→_ _→_
_A, B, C_ _N_, a _T_ .
_∈_ _∈_

If A _N_, define (A) as follows:
_∈_ _L_

(A) = _bc_ _b_ (B), c (C), where A _BC_ _a_ _A_ _a_ _._
_L_ _{_ _|_ _∈L_ _∈L_ _→_ _} ∪{_ _|_ _→_ _}_

The language generated by a grammar with root R is defined to be (R). The
_L_
_CFL recognition problem is the following: For a fixed context-free grammar in_
Chomsky Normal Form, on input a string of terminals x, determine whether
_x is in the language generated by the grammar. Devise an algorithm for the_
CFL recognition problem. Analyze your algorithm.

408. Fill in the tables in the dynamic programming algorithm for the CFL
recognition problem (see Problem 407) on the following inputs. In each case,
the root symbol is S.

(a) Grammar: S _SS, S_ _s. String: ssssss._
_→_ _→_

(b) Grammar: S _AR, S_ _AB, A_ _a, R_ _SB, B_ _b. String:_
_→_ _→_ _→_ _→_ _→_
_aaabbb._


-----

Sec. 8.5. Applications **93**

|t h i|s i s as|t r|in go f c ha r s|
|---|---|---|---|


t h i s i s a s t r i n o f c hg a r s

t h i s i s a s t r i n o f c hg a r s

t h i s i s a s t r i n o f c hg a r s


Cost: 20 units

Cost: 17 units

Cost: 12 units

**Total: 49 units**

|s i s as|t r|in go f c ha r s|
|---|---|---|

|t r|in go f c ha r s|
|---|---|


**Figure 8.2. The cost of making the breaks in left-to-right**
order.

(c) Grammar: S _AX, X_ _SA, A_ _a, S_ _BY, Y_ _SB, B_ _b,_
_→_ _→_ _→_ _→_ _→_ _→_
_S_ _CZ, Z_ _SC, C_ _c. String: abacbbcaba._
_→_ _→_ _→_

409. Devise a dynamic programming algorithm that solves the longest
ascending subsequence (see Problem 370) in time O(n log n).

410. A certain string-processing language allows the programmer to break
a string into two pieces. Since this involves copying the old string, it costs
_n units of time to break a string of n characters into two pieces. Suppose a_
programmer wants to break a string into many pieces. The order in which
the breaks are made can affect the total amount of time used. For example,
suppose we wish to break a 20 character string after characters 3, 8, and 10
(numbering the characters in ascending order from the left-hand end, starting
from 1). If the breaks are made in left-to-right order, then the first breaks
costs 20 units of time, the second breaks costs 17 units of time, and the third
breaks costs 12 units of time, a total of 49 units of time (see Figure 8.2). If
the breaks are made in right-to-left order, then the first break costs 20 units
of time, the second break costs 10 units of time, and the third break costs 8
units of time, a total of 38 units of time (see Figure 8.3). Devise a dynamic
programming algorithm that, when given the numbers of the characters after
which to break, determines the cheapest cost of those breaks in time O(n[3]).

411. Find counterexamples to the following algorithms for the string-cutting problem introduced in Problem 410. That is, find the length of the string, and
several places to cut such that when cuts are made in the order given, the
cost in higher than optimal.

(a) Start by cutting the string as close to the middle as possible, and
then repeat the same thing recursively in each half.


-----

**94** Chap. 8. Dynamic Programming

|t h i|s i s as|t r|in go f c ha r s|
|---|---|---|---|


t h i s i s a s t r i n o f c hg a r s

t h i s i s a s t r i n o f c hg a r s

t h i s i s a s t r i n o f c hg a r s


Cost: 20 units

Cost: 10 units

Cost: 8 units

**Total: 38 units**

|t h i|s i s as|t r|
|---|---|---|

|t h i|s i s as|
|---|---|


**Figure 8.3. The cost of making the breaks in right-to-left**
order.

(b) Start by making (at most) two cuts to separate the smallest substring. Repeat this until finished. Start by making (at most) two cuts
to separate the largest substring. Repeat this until finished.

412. There are two warehouses V and W from which widgets are to be
shipped to destinations Di, 1 ≤ _i ≤_ _n. Let di be the demand at Di, for 1 ≤_ _i ≤_
_n, and rV, rW be the number of widgets available at V and W_, respectively.
Assume that there are enough widgets available to fill the demand, that is,
that

_n_

_rV + rW =_ � _di._ (8.1)

_i=1_


Let vi be the cost of shipping a widget from warehouse V to destination Di,
and wi be the cost of shipping a widget from warehouse W to destination Di,
for 1 ≤ _i ≤_ _n. The warehouse problem is the problem of finding xi, yi ∈_ IN for
1 ≤ _i ≤_ _n such that when xi widgets are sent from V to Di and yi widgets_
are sent from W to Di:

_• the demand at Di is filled, that is, xi + yi = di,_

_• the inventory at V is sufficient, that is,_ _i=1_ _[x][i][ =][ r][V][,]_

[�][n]

_• the inventory at W is sufficient, that is,_ _i=1_ _[y][i][ =][ r][W][,]_

[�][n]

and the total cost of shipping the widgets,

_n_
�(vixi + wiyi)

_i=1_


is minimized.

(a) Let gj(x) be the cost incurred when V has an inventory of x widgets,
and supplies are sent to destinations Di for all 1 ≤ _i ≤_ _j in the optimal_


-----

Sec. 8.5. Applications **95**

Advance Move cursor one character to the right

Delete Delete the character under the cursor, and move the cursor
to the next character.

Replace Replace the character under the cursor with another. The
cursor remains stationary.

Insert Insert a new character before the one under the cursor.
The cursor remains stationary.

Kill Delete all characters from (and including) the one under
the cursor to the end of the line. This can only be the last
operation.

**Table 8.1. Operations allowed on a smart terminal.**

manner (note that W is not mentioned because knowledge of the inventory for V implies knowledge of the inventory for W, by (8.1).) Write a
recurrence relation for gj(x) in terms of gj−1.

(b) Use this recurrence to devise a dynamic programming algorithm that
finds the cost of the cheapest solution to the warehouse problem. Analyze
your algorithm.

413. Consider the problem of neatly printing a paragraph of text on
a printer with fixed-width fonts. The input text is a sequence of n words
containing ℓ1, ℓ2, . . ., ℓn, characters, respectively. Each line on the printer can
hold up to M characters. If a printed line contains words i through j, then
the number of blanks left at the end of the line (given that there is one blank
between each pair of words) is

|Advance Delete Replace Insert Kill|Move cursor one character to the right Delete the character under the cursor, and move the cursor to the next character. Replace the character under the cursor with another. The cursor remains stationary. Insert a new character before the one under the cursor. The cursor remains stationary. Delete all characters from (and including) the one under the cursor to the end of the line. This can only be the last operation.|
|---|---|


_M_ _j + i_
_−_ _−_


_j_
�

_ℓk._
_k=i_


We wish to minimize the sum, over all lines except the last, of the cubes of
the number of blanks at the end of each line (for example, if there are k lines
with b1, b2, . . ., bk blanks at the ends, respectively, then we wish to minimize
_b[3]1_ [+] _[b]2[3]_ [+] _[· · ·]_ [+] _[b][3]k−1[). Give a dynamic programming algorithm to compute this]_
value. Analyze your algorithm.

414. A “smart” terminal changes one string displayed on the screen into
another by a series of simple operations. The cursor is initially on the first
character of the string. The operations are shown in Table 8.1. For example,
one way to transform the string algorithm to the string altruistic is shown
in Figure 8.4.


-----

**96** Chap. 8. Dynamic Programming

**Operation** **String**
```
                   Algorithm

```
advance `aLgorithm`
advance `alGorithm`
replace with t `alTorithm`
advance `altOrithm`
delete `altRithm`
advance `altrIthm`
insert u `altruIthm`
advance `altruiThm`
insert s `altruisThm`
advance `altruistHm`
insert i `altruistiHm`
insert c `altruisticHm`
kill `altruistic`

**Figure 8.4. Transforming algorithm to altruistic using**
the operations shown in Table 8.1. The cursor position is
indicated by a capital letter.

There are many sequences of operations that achieve the same result. Suppose that on a particular brand of terminal, the advance operation takes a
milliseconds, the delete operation takes d milliseconds, the replace operation
takes r milliseconds, the insert operation takes i milliseconds, and the kill
operation takes k milliseconds. So, for example, the sequence of operations to
transform algorithm into altruistic takes time 6a + d + r + 4i + k.

(a) Show that everything to the left of the cursor is a prefix of the new string,
and everything to the right of the cursor is a suffix of the old string.

(b) Devise a dynamic programming algorithm that, given two strings x[1..n]
and y[1..n], determines the fastest time needed to transform x to y.
Analyze your algorithm.

415. Suppose An = {a1, a2, . . ., an} is a set of distinct coin types,
where each ai ∈ IN, for 1 ≤ _i ≤_ _n. Suppose also that a1 < a2 < · · · < an. The_
coin-changing problem is defined as follows. Given C IN, find the smallest
_∈_
number of coins from An that add up to C, given that an unlimited number
of coins of each type are available. Design a dynamic programming algorithm
that on inputs An and C, outputs the minimum number of coins needed to
solve the coin-changing problem. Analyze your algorithm.


-----

Sec. 8.6. Finding the Solutions **97**

416. _Arbitrage is the use of discrepancies in currency-exchange rates to_
make a profit. For example, there may be a small window of time during which
1 U.S. dollar buys 0.75 British pounds, 1 British pound buys 2 Australian
dollars, and 1 Australian dollar buys 0.70 U.S. dollars. Then, a smart trader
can trade one U.S. dollar and end up with 0.75 2 0.7 = 1.05 U.S. dollars,
_×_ _×_
a profit of 5%. Suppose that there are n currencies c1, . . ., cn, and an n × n
table R of exchange rates, such that one unit of currency ci buys R[i, j] units
of currency cj. Devise and analyze a dynamic programming algorithm to
determine the maximum value of

_R[c1, ci1] · R[ci1, ci2] · · · R[cik−1_ _, cik_ ] · R[cik _, c1]._

417. You have $1 and want to invest it for n months. At the beginning of
each month, you must choose from the following three options:

(a) Purchase a savings certificate from the local bank. Your money will be
tied up for one month. If you buy it at time t, there will be a fee of CS(t)
and after a month, it will return S(t) for every dollar invested. That is,
if you have $k at time t, then you will have $(k − _CS(t))S(t) at time_
_t + 1._

(b) Purchase a state treasury bond. Your money will be tied up for six
months. If you buy it at time t, there will be a fee of CB(t) and after
six months, it will return B(t) for every dollar invested. That is, if you
have $k at time t, then you will have $(k − _CB(t))B(t) at time t + 6._

(c) Store the money in a sock under your mattress for a month. That is, if
you have $k at time t, then you will have $k at time t + 1.

Suppose you have predicted values for S, B, CS, CB for the next n months. Devise a dynamic programming algorithm that computes the maximum amount
of money that you can make over the n months in time O(n).

###### 8.6 FINDING THE SOLUTIONS

418. Show the contents of the array P for each of the parts of Problems 380–
383. Write down the cheapest parenthesization of each of the matrix products.

419. Modify the dynamic programming algorithm for the knapsack problem so that the actual packing of the knapsack can be found. Write an algorithm for recovering the packing from the information generated by your
modified dynamic programming algorithm.

420. Show the contents of the array P for each of the graphs in Problem 401.
Write down the shortest path between each pair of vertices.


-----

**98** Chap. 8. Dynamic Programming

421. Modify your dynamic programming algorithm for the string-cutting
problem (Problem 410) so that the cuts can be recovered. Write an algorithm
for recovering the cuts from the information generated by your modified dynamic programming algorithm.

422. Modify your dynamic programming algorithm for the warehouse problem (Problem 412) so that the values xi and yi for 1 ≤ _i ≤_ _n can be recovered._
Write an algorithm for recovering these values from the information generated
by your modified dynamic programming algorithm.

423. Modify your dynamic programming algorithm for the printing problem (Problem 413) so that the number of words on each line can be recovered.
Write an algorithm for recovering these values from the information generated
by your modified dynamic programming algorithm.

424. Modify your dynamic programming algorithm for the fastest editsequence problem (Problem 414) so that the fastest edit sequence can be
recovered. Write an algorithm for recovering this sequence of operations from
the information generated by your modified dynamic programming algorithm.

425. Modify your dynamic programming algorithm for the coin-changing
problem (Problem 415) so that the number of each type of coin can be recovered. Write an algorithm for recovering this data from the information
generated by your modified dynamic programming algorithm.

426. Modify your algorithm for Problem 416 to determine the sequence of
currencies i1, i2, . . ., ik that maximizes

_R[c1, ci1] · R[ci1, ci2] · · · R[ik−1, ik] · R[ik, 1]._

427. Modify your algorithm for Problem 417 so that it determines the
optimal investment strategy.

After graduation, you start working for a company that has a hierarchical supervisor
structure in the shape of a tree, rooted at the CEO. The personnel office has ranked
each employee with a conviviality rating between 0 and 10. Your first assignment
is to design a dynamic programming algorithm to construct the guest list for the
office Christmas party. The algorithm has input consisting of the hierarchy tree,
and conviviality ratings for each employee. The output is to be a guest list that
maximizes the total conviviality, and ensures that for every employee invited to
the party, his or her immediate supervisor (that is, their parent in the tree) is not
invited.

428. Design such a dynamic programming algorithm, and analyze it.


-----

Sec. 8.7. Hints **99**

429. You are not sure if the CEO should get invited to the party, but you
suspect that you might get fired if he is not. Can you modify your algorithm
to ensure that the CEO does get invited?

###### 8.7 HINTS

378. Start by drawing a picture of the array entries on which m[i, j] depends. Make
sure that the array is filled in such way that the required entries are there
when they are needed.

409. Construct an array B[1..n] such that B[i] contains the length of the longest
ascending subsequence that starts with A[i], for 1 _i_ _n. Fill B from back_
_≤_ _≤_
to front. From the information in B, you should be able to find the length of
the longest ascending subsequence. You should also, with a little thought, be
able to output a longest ascending subsequence (there may be more than one
of them, obviously) in time O(n).

413. In addition to the table of costs for subproblems, you will need to keep track of
the number of blanks in the last line of text in the solution of each subproblem.
The base case is more than just filling in the diagonal entries.

415. An O(nC) time algorithm can be constructed by exploiting the similarity between the coin changing problem and the knapsack problem (see Section 8.2).
It is easy to formulate an inferior algorithm that appears to run in time
_O(nC_ [2]), but with a little thought it can be analyzed using Harmonic numbers
to give a running time of O(C [2] log n), which is superior for C = o(n/ log n).

###### 8.8 SOLUTIONS

383. 1 2 3 4 5

1 0 48 352 1020 1096

2 0 114 792 978

3 0 684 936

4 0 2394

5 0

384. Suppose n = 3, and r0 = 1, r1 = 2, r2 = 32, r3 = 12. The suggested algorithm
parenthesizes the product as M1·(M2·M3), at a cost of 2·23·12+1·2·12 = 792.
The most efficient way to parenthesize the product is (M1 · M2) · M3, at a
cost of 1 2 32 + 1 32 12 = 448. For a larger example, take n = 7, and
_·_ _·_ _·_ _·_
dimensions 1, 2, 32, 12, 6, 5, 17, 12.

407. For each nonterminal symbol S ∈ _N_, keep a Boolean table tS[1..n, 1..n]. We

|1|2|3|4|5|
|---|---|---|---|---|
|0|48|352|1020|1096|
||0|114|792|978|
|||0|684|936|
||||0|2394|
|||||0|


-----

**100** Chap. 8. Dynamic Programming

will fill the tables so that for 1 ≤ _i ≤_ _j ≤_ _n, tS[i, j] is true iff the string_
_xixi+1_ _xj is in the language generated by S. tS[i, j] is true iff either i = j_
_· · ·_
and S → _xi, or there exists k such that i ≤_ _k < j and S →_ _TU_, where tT [i, k]
and tU [k + 1, j] are true.
**function cfl(x1x2 · · · xn)**
1. **for each nonterminal S do**
2. **for i := 1 to n do**
3. _tS[i, i] :=true iff S →_ _xi_
4. **for d := 1 to n** 1 do
_−_
5. **for i := 1 to n** _d do_
_−_
6. _j := i + d_
7. **for each nonterminal S do**
8. _tS[i, j] :=false_
9. **for each production S** _TU do_
_→_
10. _tS[i, j] := tS[i, j] ∨_ [�][j]k[−]=[1]i [(][t][T][ [][i, k][]][ ∧] _[t][U]_ [[][k][ + 1][, j][])]
11. **return(tR[1, n]) where R is the root**
Since there are O(1) nonterminals:

The for-loop on lines 1–3 costs O(n).

_•_
Line 10 costs O(n) (a single for-loop).

_•_
The for-loop on lines 7–10 costs O(n).

_•_
The for-loop on lines 5–10 costs O(n[2]).

_•_
The for-loop on lines 4–10 costs O(n[3]).

_•_

Therefore, the algorithm runs in time O(n[3]).

###### 8.9 COMMENTS

380. Although the easiest way to do this is to write a program to do it for you,
I recommend strongly that you do it by hand instead. It will help you to
understand the subtleties of the algorithm. However, there is nothing wrong
with using such a program to verify that your answer is correct.

415. In some cases, a greedy algorithm for this problem is superior to dynamic
programming (see Problem 471). See also Problem 95.


-----

###### Chapter 9

### Greedy Algorithms

A greedy algorithm starts with a solution to a very small subproblem and augments
it successively to a solution for the big problem. This augmentation is done in
a “greedy” fashion, that is, paying attention to short-term or local gain, without
regard to whether it will lead to a good long-term or global solution. As in real life,
greedy algorithms sometimes lead to the best solution, sometimes lead to pretty
good solutions, and sometimes lead to lousy solutions. The trick is to determine
when to be greedy.

###### 9.1 CONTINUOUS KNAPSACK

The continuous knapsack problem is similar to the knapsack problem studied in
Section 8.2. We are given n objects, A1, A2, . . ., An, where for all 1 ≤ _i ≤_ _n, object_
_Ai has length si and weight wi. We must fill a knapsack of length S as full as possible_
using fractional parts of the objects, so that the total weight is minimized, assuming
that the objects are uniformly dense (so that for all 0 ≤ _xi ≤_ 1, an xi-fraction of
_Ai has length xisi and weight xiwi). That is, we must find 0 < x1, x2, . . ., xn < 1_
that minimizes [�]i[n]=1 _[x][i][w][i][ subject to the constraint][ S][ =][ �]i[n]=1_ _[x][i][s][i][.]_
The greedy algorithm proceeds as follows. Define the density of object Ai to
be wi/si. Use as much of low-density objects as possible. That is, process each
in increasing order of density. If the whole thing fits, use all of it. If not, fill the
remaining space with a fraction of the current object, and discard the rest. That
is, we first sort the objects in nondecreasing density, so that wi/si _wi+1/si+1 for_
_≤_
1 _i < n. Then, we perform the following pseudocode:_
_≤_

_s := S; i := 1_
**while si ≤** _s do_
_xi := 1;s := s −_ _si; i := i + 1_
_xi := s/si_
**for j := i + 1 to n do xj := 0**

430. Show that the greedy algorithm gives a solution of minimum weight.

**101**


-----

**102** Chap. 9. Greedy Algorithms

431. Solve the continuous knapsack problem on the following inputs:

(a) S = 20; s1 = 9, s2 = 5, s3 = 7, s4 = 12, s5 = 3; w1 = 4, w2 = 4, w3 = 8,
_w4 = 5, w5 = 1._

(b) S = 18; s1 = 9, s2 = 5, s3 = 7, s4 = 12, s5 = 3; w1 = 18, w2 = 15,
_w3 = 28, w4 = 50, w5 = 6._

(c) S = 25; s1 = 12, s2 = 6, s3 = 17, s4 = 32, s5 = 23; w1 = 18, w2 = 15,
_w3 = 28, w4 = 50, w5 = 47._

###### 9.2 DIJKSTRA’S ALGORITHM

The single-source shortest-paths problem is defined as follows. Given a labeled,
directed graph G = (V, E) and a distinguished vertex s _V, find for each vertex_
_∈_
_w_ _V, the shortest (that is, least-cost) path from s to w. (See also Problem 367 for_
_∈_
the unweighted version of this problem, that is, all edge labels are equal to unity.)
Vertex s is called the source.
Dijkstra’s algorithm for the single-source shortest-paths problem is the following.
_C[i, j] denotes the cost of the edge from vertex i to vertex j._

1. _S :=_ _s_
_{_ _}_
2. **for each v** _V do_
_∈_
3. _D[v] := C[s, v]_
4. **if (s, v)** _E then P_ [v] := s else P [v] := 0
_∈_
5. **for i := 1 to n** 1 do
_−_
6. choose w _V_ _S with smallest D[w]_
_∈_ _−_
7. _S := S_ _w_
_∪{_ _}_
8. **for each vertex v** _V do_
_∈_
9. **if D[w] + C[w, v] < D[v] then**
10. _D[v] := D[w] + C[w, v]; P_ [v] := w

432. Show the contents of arrays D and P after each iteration of the main
for-loop in Dijkstra’s algorithm executed on the graphs shown in Figure 9.1,
with source vertex 1. Use this information to list the shortest paths from
vertex 1 to each of the other vertices.

433. Show that an arbitrary collection of single-source shortest paths in
an undirected graph does not necessarily form a spanning tree.

434. Show that the single-source shortest paths constructed by Dijkstra’s
algorithm on a connected undirected graph form a spanning tree. (See also
Problem 433.)

435. Is the spanning tree formed by Dijkstra’s algorithm on a connected
undirected graph a min-cost spanning tree? (See also Problem 434.)


-----

Sec. 9.3. Min-Cost Spanning Trees **103**

(a) 50 (b) (c)

10 100

1 2 2 1

12 5

4 30 4 30 3 4
6 6

65 65 25 4 9 3 1 2

70


21


8


44

**Figure 9.1. Some graphs.**

436. Suppose we want to solve the single-source longest path problem. Can we modify Dijkstra’s algorithm to solve this problem by changing
_minimum to maximum? If so, then prove your algorithm correct. If not, then_
provide a counterexample.

437. Suppose you are the programmer for a travel agent trying to determine the minimum elapsed time from DFW airport to cities all over the
world. Since you got an A in my algorithms course, you immediately think
of using Dijkstra’s algorithm on the graph of cities, with an edge between
two cities labeled with the flying time between them. But the shortest path
in this graph corresponds to shortest flying time, which does not include the
time spent waiting at various airports for connecting flights. Desperate, you
instead label each edge from city x to city y with a function fxy(t) that maps
from your arrival time at x to your arrival time at y in the following fashion:
If you are in x at time t, then you will be in y at time fxy(t) (including waiting
time and flying time). Modify Dijkstra’s algorithm to work under this new
formulation, and explain why it works. State clearly any assumptions that
you make (for example, it is reasonable to assume that fxy(t) ≥ _t)._

###### 9.3 MIN-COST SPANNING TREES

A graph S = (V, T ) is a spanning tree of an undirected graph G = (V, E) if S is
a tree (that is, S is connected and has no cycles), and T _E. It is a min-cost_
_⊆_
_spanning tree of a labeled graph if it is a spanning tree of smallest cost._
Prim’s algorithm constructs a spanning tree using a priority queue Q of edges,
as follows:


-----

**104** Chap. 9. Greedy Algorithms

1. _T := ∅; V1 := {1}; Q := empty_
2. **for each w** _V such that (1, w)_ _E do_
_∈_ _∈_
3 insert(Q, (1, w))
4. **while |V1| < n do**
5. _e :=deletemin(Q)_
6. Suppose e = (u, v), where u ∈ _V1_
7. **if v ̸∈** _V1 then_
8. _T := T_ _e_
_∪{_ _}_
9. _V1 := V1 ∪{v}_
10. **for each w** _V such that (v, w)_ _E do_
_∈_ _∈_
11. insert(Q, (v, w))

Kruskal’s algorithm constructs a spanning tree using the union-find abstract
data type (see Section 11.4). F is the set of vertex-sets in the forest.

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

438. Draw the spanning forest after every iteration of the main while-loop in
Kruskal’s algorithm on each of the graphs in Figure 9.1, ignoring the directions
on the edges.

439. Draw the spanning forest after every iteration of the main while-loop in
Prim’s algorithm on each of the graphs in Figure 9.1, ignoring the directions
on the edges.

440. Draw the spanning forest after every iteration of the main while-loop in
Kruskal’s algorithm on the graph shown in Figure 9.2. Number the edges in
order of selection.

441. Draw the spanning forest after every iteration of the main while-loop
in Prim’s algorithm on the graph shown in Figure 9.2. Number the edges in
order of selection.

442. Would Prim’s algorithm start by making the choice of edges shown in
Figure 9.4 for the graph shown in Figure 9.3?

443. Would Kruskal’s algorithm start by making the choice of edges shown in
Figure 9.5 on the graph shown in Figure 9.3?


-----

Sec. 9.3. Min-Cost Spanning Trees **105**

6 8

2 2 9 11


21


17


**Figure 9.2. A graph.**

3

5

2 4

2 12

1 4 5

6

1 8 10 11
9
7

6 7

3

**Figure 9.3. Another graph.**


6

1 8 10 11
9
7

6 7

3


6

1 8 10 11
9
7

6 7

3


6

1 8 10 11
9
7

6 7

3


6

1 8 10 11
9

7

6 7

3


**Figure 9.4. A min-cost spanning tree under construction**
using Prim’s algorithm?


-----

**106** Chap. 9. Greedy Algorithms


6

1 8 10 11
9
7

6 7

3


6

1 8 10 11
9
7

6 7

3


6

1 8 10 11
9
7

6 7

3


6

1 8 10 11
9
7

6 7

3


**Figure 9.5. A min-cost spanning tree under construction**
using Kruskal’s algorithm?


6

1 8 10 11
9
7

6 7

3


6

1 8 10 11
9
7

6 7

3


6

1 8 10 11
9
7

6 7

3


6

1 8 10 11
9
7

6 7

3


**Figure 9.6. A min-cost spanning tree under construction?**

444. Could a greedy algorithm for min-cost spanning trees start by making
the choice of edges shown in Figure 9.6 on the graph shown in Figure 9.3?

445. Could a greedy algorithm for min-cost spanning trees start by making
the choice of edges shown in Figure 9.7 on the graph shown in Figure 9.3?

446. Show that Prim’s algorithm and Kruskal’s algorithm always construct the same min-cost spanning tree on a connected undirected graph in
which the edge costs are distinct.

447. Show that Prim’s algorithm and Kruskal’s algorithm always construct the same min-cost spanning tree on a connected undirected graph in
which no pair of edges that share a vertex have the same cost.

448. Is the path between a pair of vertices in a min-cost spanning tree of
an undirected graph necessarily a min-cost path? Is this true if the min-cost
spanning tree is unique? If it is not unique?


-----

Sec. 9.3. Min-Cost Spanning Trees **107**


3


3


3


3


**Figure 9.7. A min-cost spanning tree under construction?**

449. Show how to modify Prim’s algorithm so that it runs in time
_O(n log k) on a graph that has only k different edge costs._

450. Here is a version of Prim’s algorithm that is different from the one
given earlier in this section. Is it correct? If so, prove it correct. If not, explain
why it is wrong and give a graph on which it fails.

1. _T := ∅; V1 := {1}; Q := empty_
2. **for each w** _V such that (1, w)_ _E do_
_∈_ _∈_
3 insert(Q, (1, w))
4. **while |V1| < n do**
5. _e :=deletemin(Q)_
6. Suppose e = (u, v), where u ∈ _V1_
7. _T := T_ _e_
_∪{_ _}_
8. _V1 := V1 ∪{v}_
9. **for each w** _V such that (v, w)_ _E do_
_∈_ _∈_
10. **if w ̸∈** _V1 then insert(Q, (v, w))_

In the vanilla version of Prim’s algorithm and Kruskal’s algorithm, it is not specified
what to do if a choice must be made between two edges of minimum cost.

451. Prove that for Prim’s algorithm, it doesn’t matter which of the two edges
is chosen.

452. Prove that for Kruskal’s algorithm, it doesn’t matter which of the two
edges is chosen.

453. Suppose that there are exactly two edges that have the same cost. Does
Prim’s algorithm construct the same min-cost spanning tree regardless of
which edge is chosen?


-----

**108** Chap. 9. Greedy Algorithms

454. Suppose that there are exactly two edges that have the same cost. Does
Kruskal’s algorithm construct the same min-cost spanning tree regardless of
which edge is chosen?

455. Suppose Prim’s algorithm and Kruskal’s algorithm choose the lexicographically first edge first. That is, if a choice must be made between two
distinct edges, e1 = (u1, v1) and e2 = (u2, v2) of the same cost, where u1 < v1
and u2 < v2, then the following strategy is used. Suppose the vertices are
numbered 1, 2, . . ., n. Choose e1 if u1 < u2, or u1 = u2 and v1 < v2. Otherwise, choose e2. Prove that under these conditions, both algorithms construct
the same min-cost spanning tree.

456. Design an algorithm for the max-cost spanning tree.

A directed spanning tree of a directed graph is a spanning tree in which the directions
on the edges point from parent to child.

457. Suppose Prim’s algorithm is modified to take the cheapest edge directed out of the tree.

(a) Does it find a directed spanning tree of a directed graph?
(b) If so, will it find a directed spanning tree of minimum cost?

458. Suppose Kruskal’s algorithm is used to construct a directed spanning
tree.

(a) Does it find a directed spanning tree of a directed graph?
(b) If so, will it find a directed spanning tree of minimum cost?

459. Consider the following algorithm. Suppose Prim’s algorithm is modified as described in Problem 457, and then run n times, starting at each vertex
in turn. The output is the cheapest of the n directed spanning trees.

(a) Does this algorithm output a directed spanning tree of a directed graph?
(b) If so, will it find a directed spanning tree of minimum cost?

Consider the following algorithm for finding a min-cost spanning tree. Suppose the
graph has vertices numbered 1, 2, . . ., n. Start with a forest containing n trees, each
consisting of a single vertex. Repeat the following until a single tree remains. For
each vertex v = 1, 2, . . ., n in turn, consider the cheapest edge with at least one
endpoint in the tree that contains v. If it has both endpoints in the same tree, then
discard it. If not, then add it to the spanning forest.

460. Is this algorithm correct? Justify your answer.

461. Explain how to implement this algorithm in time O(e log n).


-----

Sec. 9.4. Traveling Salesperson **109**

###### 9.4 TRAVELING SALESPERSON

The traveling salesperson problem is defined as follows. Given a directed labeled
graph, find a Hamiltonian cycle of minimum total cost. A “vanilla” greedy algorithm
for the traveling salesperson problem starts at node number 1, and moves along the
edge of minimum cost to the next node, and repeats this until it finds a node that
it has visited before, or can go no further.

462. Show that this greedy algorithm may fail to find a cycle.

463. Show that even when the greedy algorithm finds a cycle, it may not be
a Hamiltonian cycle, even when one exists in the graph.

464. Suppose the greedy algorithm does find a Hamiltonian cycle. Prove
that it is a Hamiltonian cycle of minimum cost.

465. Suppose the edge costs are distinct, and the greedy algorithm does
find a Hamiltonian cycle. Show that it is the only min-cost Hamiltonian cycle
in the graph.

466. Here is another greedy algorithm for the traveling salesperson problem. Simply run the vanilla greedy algorithm described above n times, starting at each vertex in turn, and output the cheapest Hamiltonian cycle found.
Suppose this greedy algorithm does output a Hamiltonian cycle. Can it be a
different cycle from the one found by the vanilla greedy algorithm? Justify
your answer.

Another greedy algorithm for the traveling salesperson problem proceeds as follows.
Start at node number 1, and move along the edge of minimum cost that leads to
an unvisited node, repeating this until the algorithm arrives at a vertex from which
all edges lead to visited nodes.

467. Show that this greedy algorithm may fail to find a cycle.

468. Suppose the graph has a Hamiltonian cycle. Will this algorithm find it?

469. Suppose this greedy algorithm finds a Hamiltonian cycle. Is it necessarily a Hamiltonian cycle of minimum cost? Justify your answer.

###### 9.5 APPLICATIONS

The problems in this section ask you to apply the greedy method in new situations.
One thing you will notice about greedy algorithms is that they are usually easy to
design, easy to implement, easy to analyze, and they are very fast, but they are
almost always difficult to prove correct.


-----

**110** Chap. 9. Greedy Algorithms

470. Given n files of length m1, m2, . . ., mn, the optimal tape-storage
_problem is to find which order is the best to store them on a tape, assuming_
that each retrieval starts with the tape rewound, each retrieval takes time
equal to the length of the preceding files in the tape plus the length of the
retrieved file, and that files are to be retrieved in the reverse order. The greedy
algorithm puts the files on the tape in ascending order of size. Prove that this
is the best order.

471. Suppose An = {a1, a2, . . ., an} is a set of distinct coin types,
where each ai ∈ IN, for 1 ≤ _i ≤_ _n. Suppose also that a1 < a2 < · · · < an. The_
coin-changing problem is defined as follows. Given C IN, find the smallest
_∈_
number of coins from An that add up to C, given that an unlimited number
of coins of each type are available.

(a) Suppose a1 = 1. A greedy algorithm will make change by using the
larger coins first, using as many coins of each type as it can before it
moves to the next lower denomination. Show that this algorithm does
not necessarily generate a solution with the minimum number of coins.

(b) Show that for all c ∈ IN, if An = {1, c, c[2], . . ., c[n][−][1]}, c ≥ 2, then for
all C IN, the greedy algorithm always gives a minimal solution to the
_∈_
coin-changing problem.

472. The vertex cover problem is defined as follows. Let G = (V, E) be an
undirected graph. A vertex cover of G is a set U _V such that for each edge_
_⊆_
(u, v) _E, either u_ _U or v_ _U_ . A minimum vertex cover is a vertex cover
_∈_ _∈_ _∈_
with the smallest number of vertices in it. The following is a greedy algorithm
for this problem:

**function cover(V, E)**
1. _U :=_
_∅_
2. **repeat**
3. let v _V be a vertex of maximum degree_
_∈_
4. _U := U_ _v_ ; V := V _v_
_∪{_ _}_ _−{_ _}_
5. _E := E_ (u, w) such that u = v or w = v
_−{_ _}_
6. **until E =**
_∅_
7. **return(U)**

Does this algorithm always generate a minimum vertex cover? Justify your
answer.

473. The one-processor scheduling problem is defined as follows. We are
given a set of n jobs. Each job i has a start time ti, and a deadline di. A
_feasible schedule is a permutation of the jobs such that when the jobs are_
performed in that order, then every job is finished before the deadline. A
greedy algorithm for the one-processor scheduling problem processes the jobs


-----

Sec. 9.6. Hints **111**

in order of deadline (the early deadlines before the late ones). Show that if a
feasible schedule exists, then the schedule produced by this greedy algorithm
is feasible.

###### 9.6 HINTS

430. Show that a greedy solution (x1, x2, . . ., xn) can be changed to an optimal
solution (y1, y2, . . ., yn) without affecting its length by doing the following for
_i = 1, 2, . . ., n. Change xi to yi and adjust the remaining xi+1, . . ., xn so that_
the length remains the same.

446. This can be proved directly by induction. But a more insightful way to do it
is to prove that the min-cost spanning tree is unique under these conditions.

447. See Problem 446.

449. This is really a data structures question.

471. For part (a), just play around until you get a counterexample. For part (b),
show that there is only one solution in which the number of coins of each type
is less than c, and that the min-cost solution must have this form. These two
facts should enable you to easily prove that the greedy algorithm does the
right thing.

###### 9.7 SOLUTIONS

430. Let X = (x1, x2, . . ., xn) be the solution generated by the greedy algorithm.
If all the xi are 1, then the solution is clearly optimal (it is the only solution).
Otherwise, let j be the smallest number such that xj ̸= 1. From the algorithm,

_xi = 1_ for 1 ≤ _i < j_
0 ≤ _xj < 1_
_xi = 0_ for _j < i ≤_ _n._

Therefore,

_j_
� _xisi = S._ (9.1)

_i=1_

Let Y = (y1, y2, . . ., yn) be a solution of minimal weight. We will prove that
_X must have the same weight as Y, and hence has minimal weight too. If_
_X = Y, we are done. Otherwise, let k be the least number such that xk ̸= yk._


-----

**112** Chap. 9. Greedy Algorithms

It must be the case that yk < xk. To see this, consider the three possible
cases:
**Case 1. k < j. Then xk = 1. Therefore, since xk** = yk, yk must be smaller
_̸_
than xk.
**Case 2. k = j. By the definition of k, xk** = yk. If yk > xk,
_̸_


_n_
� _yisi_ =

_i=1_

=


_k−1_
� _yisi + yksk +_

_i=1_

_k−1_
�

_xisi + yksk +_
_i=1_


_n_
� _yisi_

_i=k+1_

_n_
�

_yisi_

_i=k+1_


= _S + (yk_ _xk)sk +_
_−_

_>_ _S,_


_n_
� _yisi (by Equation 9.1, since k = j)_

_i=k+1_


which contradicts the fact that Y is a solution. Therefore, yk < xk.
**Case 3. k > j. Then xk = 0 and yk > 0, and so**


_n_
�

_yisi_
_i=j+1_

_n_
�

_yisi_
_i=j+1_


_n_
� _yisi_ =

_i=1_

=


_j_
�

_yisi +_
_i=1_

_j_
�

_xisi +_
_i=1_


= _S +_

_>_ _S._


_n_
�

_yisi (by Equation 9.1)_
_i=j+1_


This is not possible, hence Case 3 can never happen. In the other two cases,
_yk < xk as claimed. Now that we have established that yk < xk, we can_
return to the proof. Suppose we increase yk to xk, and decrease as many of
_yk+1, . . ., yn as necessary to make the total length remain at S. Call this new_
solution Z = (z1, z2, . . ., zn). Then,


(zk _yk)sk +_
_−_


(zk − _yk)sk_ _>_ 0, (9.2)
_n_
� (zi − _yi)si_ _<_ 0, (9.3)

_i=k+1_

_n_
� (zi − _yi)si_ = 0. (9.4)

_i=k+1_


-----

Sec. 9.7. Solutions **113**

Therefore,


_n_
� _ziwi_ =

_i=1_

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
�

_yiwi + zkwk +_
_i=1_

_n_
�

_yiwi −_ _ykwk −_
_i=1_


_n_
� _yiwi (by Equation 9.4)._

_i=1_


_n_
� _ziwi_

_i=k+1_

_n_
�

_ziwi_

_i=k+1_

_n_
�

_yiwi + zkwk +_
_i=k+1_


_n_
�

_ziwi_
_i=k+1_


_n_
� _yiwi + (zk_ _yk)wk +_

_−_
_i=1_


_n_
� (zi − _yi)wi_

_i=k+1_


_n_
� _yiwi + (zk_ _yk)skwk/sk +_

_−_
_i=1_

_n_
� _yiwi + (zk_ _yk)skwk/sk +_

_−_
_i=1_

(by Equation 9.4 and density)


_n_
� (zi − _yi)siwi/si_

_i=k+1_

_n_
� (zi − _yi)siwk/sk_

_i=k+1_


_n_
�

_yiwi +_
_i=1_


�


�


(zk _yk)sk +_
_−_


_n_
� (zi − _yi)si_

_i=k+1_


_wk/sk_


Now, since Y is a minimal-weight solution,


_n_
� _ziwi ̸<_

_i=1_


_n_
� _yiwi._

_i=1_


Hence, Y and Z have the same weight. But Z looks “more like” X than Y
does, in the sense that the first k entries of Z are the same as X, whereas
only the first k 1 entries of Y are the same as X. Repeating this proce_−_
dure sufficiently often transforms Y into X and maintains the same weight.
Therefore, X must have minimal weight.

470. Suppose we have files f1, f2, . . ., fn, of lengths m1, m2, . . ., mn, respectively.
Let i1, i2, . . ., in be a permutation of 1, 2, . . ., n. Suppose we store the files in
order

_fi1, fi2_ _, . . ., fin._


-----

**114** Chap. 9. Greedy Algorithms

To retrieve the kth file on the tape, fik, costs _j=1_ _[m][i]j_ [. Therefore, the cost]

[�][k]
of retrieving them all is


_n_
�

_k=1_


_k_
�

_mij =_
_j=1_


_n_
�(n − _k + 1)mik_ _._ (9.5)

_k=1_


To see this, consider the following table of costs:
_fi1:_ _mi1_
_fi2:_ _mi1+mi2_
_fi3:_ _mi1+mi2+mi3_
...
_fin−1:_ _mi1+mi2+mi3+· · ·+min−1_
_fin_ : _mi1+mi2+mi3+· · ·+min−1+min_
The left-hand side of Equation 9.5 adds this table by rows. If the total is
computed by columns, we get instead


_nmi1 + (n −_ 1)mi2 + (n − 2)mi3 + · · · + 2min−1 + min =


_n_
�(n − _k + 1)mik_ _,_

_k=1_


which is the right-hand side of Equation (9.5). The greedy algorithm picks
files fi in nondecreasing order of their size mi. It remains to prove that this
is the minimum cost permutation.
**Claim: Any permutation in nondecreasing order of mi’s has minimum cost.**
**Proof: Let Π = (i1, i2, . . ., in) be a permutation of 1, 2, . . ., n that is not**
in nondecreasing order of mi’s. We will prove that it cannot have minimum
cost. Since mi1, mi2, . . ., min is not in nondecreasing order, there must exist
1 ≤ _j < n such that mij > mij+1. Let Π[′]_ be permutation Π with ij and ij+1
swapped. The cost of permutation Π is


_C(Π)_ =

=


_n_
�(n − _k + 1)mik_

_k=1_

_j−1_
�(n − _k + 1)mik + (n −_ _j + 1)mij + (n −_ _j)mij+1_

_k=1_


+


_n_
� (n − _k + 1)mik_ _._

_k=j+2_


The cost of permutation Π[′] is


_n_
� (n−k+1)mik.

_k=j+2_


_C(Π[′]) =_


_j−1_
�(n−k+1)mik +(n−j +1)mij+1 +(n−j)mij +

_k=1_


-----

Sec. 9.8. Comments **115**

Hence,

_C(Π) −_ _C(Π[′])_ = (n − _j + 1)(mij −_ _mij+1) + (n −_ _j)(mij+1 −_ _mij_ )
= _mij_ _mij+1_
_−_
_>_ 0 (by definition of j).

Therefore, C(Π[′]) < C(Π), and so Π cannot be a permutation of minimum
cost. This is true of any Π that is not in nondecreasing order of mi’s. Therefore, the minimum-cost permutation must be in nondecreasing order of mi’s.

###### 9.8 COMMENTS

436, 456. These problems were suggested to the author by Farhad Shahrokhi in
1993.

471. See also Problem 95. In general, a dynamic programming algorithm is the
best solution to this problem (see Problem 415). This question is designed
to illustrate the point that a greedy algorithm is better in some (but not all)
cases.


-----

###### Chapter 10

### Exhaustive Search

Often it appears that there is no better way to solve a problem than to try all possible solutions. This approach, called exhaustive search, is almost always slow, but
sometimes it is better than nothing. It may actually be practical in real situations if
the problem size is small enough. The most commonly used algorithmic technique
used in exhaustive search is divide-and-conquer (see Chapter 7).
The approach taken to exhaustive search in this chapter is very different from
that taken by most textbooks. Most exhaustive search problems can be reduced to
the problem of generating simple combinatorial objects, most often strings, permutations, and combinations. Sections 10.1–10.4 cover some simple algorithms that
form our basic tools. Section 10.6 covers the application of these tools to various
interesting exhaustive search problems. Section 10.5 compares exhaustive search
algorithms to backtracking. Sometimes backtracking is faster, sometimes not.

###### 10.1 STRINGS

A bit-string is an array of n bits. Bit-strings are often used to represent sets
(the term usually used is the bit-vector representation of a set). The following
is a recursive algorithm for generating bit-strings. We assume the existence of a
procedure process(C) that processes a bit-string stored in an array C. Our aim is
to process all bit-strings of a fixed length.

**procedure binary(m)**
**comment process all binary strings of length m**
1. **if m = 0 then process(C) else**
2. _C[m] := 0; binary(m_ 1)
_−_
3. _C[m] := 1; binary(m_ 1)
_−_

474. Show that the algorithm is correct, that is, that a call to binary(n)
processes all binary strings of length n.

475. How many assignments to array C are made (that is, how often are
lines 2 and 3 executed)? Hence, deduce the running time of the procedure.

**116**


-----

Sec. 10.1. Strings **117**

The following algorithm generates all strings of n bits in an array C[1..n]. A sentinel
is used at both ends of C, so C is actually an array indexed from 0 to n + 1. The
operation “complement a bit” used in line 8 means change it from a 0 to a 1, or
vice-versa. It works by treating C as a binary number and repeatedly incrementing
it through all 2[n] possible values.

1. **for i := 0 to n + 1 do C[i] := 0**
2. **while C[n + 1] = 0 do**
3. process(C)
4. increment(C)

**procedure increment(C)**
5. _i := 1_
6. **while C[i** 1] = 0 do
_−_
7. Complement C[i]
8. _i := i + 1_

476. Prove that the algorithm is correct, that is, that procedure process(C)
is called once with C[1..n] containing each string of n bits.

477. Prove that for all n 1, the number of times that a bit of C is comple_≥_
mented (that is, the number of times that line 7 is executed) is 2[n][+1] (n +2).
_−_
Hence, deduce the running time of the algorithm.

A minimal-change algorithm for generating bit-strings generates them in such an
order that each string differs from its predecessor in exactly one place. The following
algorithm generates all of the bit-strings of length n in minimal-change order. The
array b is initially set to all zeros, and the bit-strings are generated with a call to
generate(n).

**procedure generate(n)**
1. **if n = 0 then process(b)**
2. **else**
3. generate(n 1)
_−_
4. Complement b[n]
5. generate(n 1)
_−_

478. Prove that this algorithm does generate the 2[n] bit-strings of length
_n in minimal-change order._

479. Prove that for all n 1, the number of times that a bit of b is comple_≥_
mented (that is, the number of times that line 4 is executed) is 2[n] 1. Hence,
_−_
deduce the running time of the algorithm.


-----

**118** Chap. 10. Exhaustive Search

A k-ary string is a string of digits drawn from 0, 1, . . ., k 1 . For example, if
_{_ _−_ _}_
_k = 2, then a k-ary string is simply a binary string._

480. Design an optimal exhaustive search algorithm for generating all k-ary
strings of length n in lexicographic order in time O(k[n]). For example, if k = 3
and n = 4, then your algorithm should generate the strings

0000, 0001, 0002, 0010, 0011, 0012, 0020, 0021, 0022, 0100, . . ., 2221, 2222.

481. Prove that your algorithm for Problem 480 is correct.

482. Analyze the running time of your algorithm for Problem 480.

A minimal-change algorithm for generating k-ary strings generates them in such an
order that each string differs from its predecessor in exactly one place.

483. Design a minimal-change exhaustive search algorithm for generating
all k-ary strings of length n. (See also Problem 480.)

484. Prove that your algorithm for Problem 483 is correct.

485. Analyze the running time of your algorithm for Problem 483.

###### 10.2 PERMUTATIONS

Consider the problem of exhaustively generating all permutations of n things. Suppose A[1..n] contains n distinct values. The following algorithm generates all permutations of A[1..n] in the following sense: A call to procedure permute(n) will result
in procedure process(A) being called once with A[1..n] containing each permutation
of its contents.

**procedure permute(n)**
1. **if n = 1 then process(A) else**
2. _B := A_
3. permute(n 1)
_−_
4. **for i := 1 to n** 1 do
_−_
5. swap A[n] with A[1]
6. permute(n 1)
_−_
7. _A := B cyclically shifted one place right_

486. Prove that this algorithm calls process(A) with A containing each
permutation of n entries exactly once.


-----

Sec. 10.2. Permutations **119**

487. What is the running time of this algorithm?

488. Show that the effect of line 7 is the same as performing a cyclic
shift of A[2..n]. Use this observation to eliminate the need for the array B.
Does this affect the running time of the algorithm?

Consider the following algorithm for generating all permutations. To generate all
permutations of any n distinct values in A[1..n], call permute(1).

**procedure permute(i)**
1. **if i = n then process(A) else**
4. permute(i + 1)
2. **for j := i + 1 to n do**
3. swap A[i] with A[j]
4. permute(i + 1)
5. swap A[i] with A[j]

489. Prove this algorithm correct.

490. How many swaps are made by this algorithm, as a function of n? What
is its running time?

The following is a minimal-change algorithm for generating permutations. That is,
each permutation generated differs from the previous one by having just two values
swapped. It is known as Heap’s algorithm (Heap [35]).

**procedure permute(n)**
1. **for i := 1 to n do A[i] := i**
2. **if n is odd**
3. **then oddpermute(n)**
4. **else evenpermute(n)**

**procedure oddpermute(n)**
5. **if n = 1 then process else**
6. evenpermute(n 1)
_−_
7. **for i := 1 to n** 1 do
_−_
8. swap A[1] and A[n]
9. evenpermute(n 1)
_−_

**procedure evenpermute(n)**
10. **if n = 1 then process else**
11. oddpermute(n 1)
_−_
12. **for i := 1 to n** 1 do
_−_
13. swap A[i] and A[n]
14. oddpermute(n 1)
_−_


-----

**120** Chap. 10. Exhaustive Search

491. Show that the algorithm is correct, that is, it generates all
permutations in minimal-change order.

492. Show that Heap’s algorithm uses the minimum number of swaps,
(that is, n! 1 swaps). What is its running time?
_−_

###### 10.3 COMBINATIONS

Consider the problem of generating all combinations of r things chosen from n, for
some 0 _r_ _n. We will, without loss of generality, assume that the n items to be_
_≤_ _≤_
chosen from are the natural numbers 1, 2, . . ., n.
The following algorithm generates all combinations of r things drawn from n
in the following sense: Procedure process(A) is called once with A[1..r] containing
each combination. To use it, call procedure choose(1, r).

**procedure choose(b, c)**
**comment choose c elements out of b..n**
1. **if c = 0 then process(A)**
2. **else for i := b to n** _c + 1 do_
_−_
3. _A[c] := i_
4. choose(i + 1, c 1)
_−_

493. Prove that this algorithm is correct.

494. Prove that the combinations generated by this algorithm are in descending order, that is, when process(A) is called, A[i] > A[i + 1] for all 1 _i < n._
_≤_

495. Let T (n, r) be the number of assignments to array A. Show that
� _n_ � � � _n_ ��
_T_ (n, r) ≤ _r_ _r_ . Hence, deduce that the algorithm runs in time O _r_ _r_ .

� _n_ �
496. Show that for all 1 ≤ _r ≤_ _n/2, T_ (n, r) ≤ 2 _r_ _−_ _r. Hence, deduce_
that the algorithm is optimal for r _n/2._
_≤_

A minimal-change algorithm for combinations generates them in such a manner
that each choice of r objects differs from the previous one by having one object
removed and replaced by another. The following is a minimal-change algorithm for
generating combinations. It is used by calling up(1, r).


-----

Sec. 10.4. Other Elementary Algorithms **121**

**procedure up(b, c)**
1. **if c = 0 then process(a)**
2. **else for i := b to n do**
3. _a[r_ _c + 1] := i_
_−_
4. **if i is odd then up(i + 1, c** 1) else down(i + 1, c 1)
_−_ _−_

**procedure down(b, c)**
5. **if c = 0 then process(a)**
6. **else for i := n downto b do**
7. _a[r_ _c + 1] := i_
_−_
8. **if i is odd then up(i + 1, c** 1) else down(i + 1, c 1)
_−_ _−_

497. Prove that the algorithm is correct, that is, that procedure
process(a) is called with a containing a sequence of combinations in minimalchange order.

498. How many assignments to a does the algorithm make? Hence, deduce
its running time.

499. Prove that the combinations generated by this algorithm are in ascending
order, that is, when process(a) is called, a[i] < a[i + 1] for all 1 _i < n._
_≤_

###### 10.4 OTHER ELEMENTARY ALGORITHMS

If n is even, a perfect matching of size n is an unordered sequence of unordered
pairs (v1, v2), (v3, v4), . . ., (vn−1, vn), where {v1, v2, . . ., vn} = {1, 2, . . ., n}. Note
that two perfect matchings are deemed to be identical even if the pairs are listed
in a different order, and the values within each pair are listed in a different order.
The following is an algorithm for generating all perfect matchings of size n in an
array M [1..n], where n is even:

**procedure match(n)**
1. **if n = 2 then process(M** ) else
2. match(n 2)
_−_
3. **for i := n** 2 downto 1 do
_−_
4. swap A[i] with A[n 1]
_−_
5. match(n 2)
_−_
6. circular shift A[1..n 1] one place right
_−_

500. Let M (n) be the number of perfect matchings of n values. Show that if
_n is even, then_

_n/2_

_M_ (n) = �(2i 1).

_−_
_i=1_


-----

**122** Chap. 10. Exhaustive Search

501. Prove that the algorithm is correct.

502. Show that the algorithm runs in time O(M (n)).

503. If n is odd, the definition of perfect matching is similar except that there
is a leftover value that is not paired with any other. What is M (n) when n is
odd? How can the above algorithm be used to generate all perfect matchings
when n is odd, in time O(M (n))?

Suppose you have m marbles and n jars, each of which can hold at most c marbles.

504. Use divide-and-conquer to design an algorithm that generates all of
the ways of distributing the marbles into the jars so that no jar holds more
than c marbles, where m _cn. Your algorithm must print the number of_
_≤_
marbles in each jar for each of the different ways of distributing the marbles.
So, for example, with m = 10, n = 3, and c = 5, the output of your algorithm
would be

0 5 5 3 2 5 4 3 3 5 3 2

1 4 5 3 3 4 4 4 2 5 4 1

1 5 4 3 4 3 4 5 1 5 5 0

2 3 5 3 5 2 5 0 5

2 4 4 4 1 5 5 1 4

2 5 3 4 2 4 5 2 3

505. Prove that your algorithm for Problem 504 is correct.

506. Analyze the running time of your algorithm for Problem 504.

###### 10.5 BACKTRACKING

Backtracking is a type of exhaustive search in which the combinatorial object is
constructed recursively, and the recursion tree is pruned, that is, recursive calls are
not made when the part of the current object that has already been constructed
cannot lead to a valid or optimal solution. For example, the recursive algorithm for
generating bit-strings from Section 10.1 can be modified easily to give a backtracking
algorithm for generating all bit-strings of length n with k or fewer bits. To use the
algorithm, call binary(n, 0).

**procedure binary(m, c)**
**comment process all binary strings of length m**
1. **if m = 0 then process(C) else**
2. _C[m] := 0; binary(m_ 1, c)
_−_
3. **if c < k then C[m] := 1; binary(m** 1, c + 1)
_−_

|0 5 5 1 4 5 1 5 4 2 3 5 2 4 4 2 5 3|3 2 5 3 3 4 3 4 3 3 5 2 4 1 5 4 2 4|4 3 3 4 4 2 4 5 1 5 0 5 5 1 4 5 2 3|5 3 2 5 4 1 5 5 0|
|---|---|---|---|


-----

Sec. 10.6. Applications **123**

Note that the pruning is done in line 3: If enough ones have been put into C
already, then the recursion tree is pruned to prevent more ones from being put in.

507. Show that the algorithm is correct, that is, that a call to binary(n, 0)
processes all binary strings of length n with k or fewer bits.

508. How many assignments to array C are made (that is, how often are
lines 2 and 3 executed)? Hence, deduce the running time of the procedure. Is
it asymptotically optimal?

The following is a backtracking algorithm for generating permutations. It fills an
arrayA[1..n] with n-ary strings, and prunes away nonpermutations by using an
additional array U [1..n]. U is a Boolean array, with U [i] set to true if i has not yet
been used in the permutation. Initially, all entries in U are assumed to be true.
The algorithm is used by calling permute(n).

**procedure permute(m)**
**comment process all permutations of length m**
1. **if m = 0 then process(A) else**
2. **for j := 1 to n do**
3. **if U** [j] then
4. _U_ [j]:=false
5. _A[m] := j; permute(m_ 1)
_−_
6. _U_ [j]:=true

509. Show that the algorithm is correct, that is, that a call to permute(n)
processes all permutations of length n.

510. How many assignments to array A are made (that is, how often are
lines 3 and 4 executed)? Hence, deduce the running time of the procedure. Is
it asymptotically optimal?

###### 10.6 APPLICATIONS

The problems in this section are to be solved by reduction to one of the standard
exhaustive search algorithms from Sections 10.1–10.4. Some of them require backtracking, and some do not.

511. A clique is an induced complete subgraph. The clique problem is the
following: Given a graph G and a natural number r, does G contain a clique
on r vertices? Devise an algorithm for the clique problem that runs in time
� _n_ ��
_O_ _r[2][ �]_ _r_ . Briefly describe how to improve the running time by a factor
of Ω(r).


-----

**124** Chap. 10. Exhaustive Search

512. Define the Ramsey number R(i, j) to be the smallest number
_n such that every graph on n vertices has either a clique of size i or an_
independent set of size j. Ramsey’s Theorem states that R(i, j) exists for all
_i, j_ IN. Devise an algorithm that, given i, j, finds R(i, j). Analyze your
_∈_
algorithm.

513. An open knight’s tour is a sequence of n[2] 1 knight’s moves
_−_
starting from some square of an n _n chessboard, such that every square_
_×_
of the board is visited exactly once. Design an algorithm for finding open
knight’s tours that runs in time O(n[2]8[n][2]). A closed knight’s tour, as we have
seen already, is a cyclic version of an open knight’s tour (that is, the start
point is reachable from the finish point a single knight’s move). Design an
algorithm for for finding closed knight’s tours that runs in time O(8[n][2]).

514. Suppose you have n students in a class and wish to assign them into
teams of two (you may assume that n is even). You are given an integer array
_P_ [1..n, 1..n] in which P [i, j] contains the preference of student i for working
with student j. The weight of a pairing of student i with student j is defined to
be P [i, j] _P_ [j, i]. The pairing problem is the problem of pairing each student
_·_
with another student in such a way that the sum of the weights of the pairings
is maximized. Design an algorithm for the pairing problem that runs in time
proportional to the number of pairings. Analyze your algorithm.

515. The 15-puzzle, invented by Sam Loyd, has been a source of entertainment for over a century. The puzzle consists of 15 square tiles numbered
1 through 15, arranged in row-major order in a square grid with a one-tile
gap. The aim is to randomize the puzzle and then attempt to return it to
the initial configuration by repeatedly sliding an adjacent tile into the gap
(see, for example, Figure 10.1). The general form of this puzzle, based on an
_n_ _n grid, is called the (n[2]_ 1)-puzzle. Design an algorithm that, given some
_×_ _−_
configuration of the (n[2] 1)-puzzle, finds a sequence of moves that return the
_−_
puzzle to the initial configuration, if such a sequence of moves exists. Your
algorithm should run in time O(n[2] + 4[k]), where k is the number of moves
required for solution of the puzzle.

516. The following puzzle is called Hi-Q. You are given a board in which 33
holes have been drilled in the pattern shown in Figure 10.2. A peg (indicated
by a square) is placed in every hole except the center one (indicated by a
circle). Pegs are moved as follows. A peg may jump over its neighbor in the
horizontal or vertical direction if its destination is unoccupied. The peg that
is jumped over is removed from the board. The aim is to produce a sequence
of jumps that removes all pegs from the board except for one. The generalized
HI-Q puzzle has n(n + 4m) holes arranged in a symmetrical cross-shape as
shown in Figure 10.3, for any m and any odd n. Design an algorithm that


-----

Sec. 10.6. Applications **125**


1 6 2 4

5 3 8

13 10 7 11
14 9 15 12

|6|Col2|2|4|
|---|---|---|---|
|1|5|3|8|
|13|10|7|11|
|14|9|15|12|

|Col1|6|2|4|
|---|---|---|---|
|1|5|3|8|
|13|10|7|11|
|14|9|15|12|

|1|6|2|4|
|---|---|---|---|
||5|3|8|
|13|10|7|11|
|14|9|15|12|

|1|6|2|
|---|---|---|
|5||3|
|13|10|7|
|14|9|15|

|1|Col2|2|4|
|---|---|---|---|
|5|6|3|8|
|13|10|7|11|
|14|9|15|12|


9 10 11

15 12


1 2 3 4
5 6 8

13 10 7 11
14 9 15 12

1 2 3 4
5 6 7 8

9 10 11
13 14 15 12

|1|2|3|4|
|---|---|---|---|
|5|6|7|8|
|13|9|10|11|
|14||15|12|

|1|2|3|4|
|---|---|---|---|
|5|6|7|8|
|13||10|11|
|14|9|15|12|

|1|2|3|4|
|---|---|---|---|
|5|6|7|8|
|13|10||11|
|14|9|15|12|

|1|2|3|
|---|---|---|
|5|6||
|13|10|7|
|14|9|15|

|1|2|Col3|4|
|---|---|---|---|
|5|6|3|8|
|13|10|7|11|
|14|9|15|12|

|1|2|3|4|
|---|---|---|---|
|5|6|7|8|
|13|9|10|11|
||14|15|12|

|1|2|3|4|
|---|---|---|---|
|5|6|7|8|
||9|10|11|
|13|14|15|12|

|1|2|3|4|
|---|---|---|---|
|5|6|7|8|
|9||10|11|
|13|14|15|12|

|1|2|3|
|---|---|---|
|5|6|7|
|9|10||
|13|14|15|

|1|2|3|4|
|---|---|---|---|
|5|6|7|8|
|9|10|11||
|13|14|15|12|

|1|2|3|4|
|---|---|---|---|
|5|6|7|8|
|9|10|11|12|
|13|14|15||


**Figure 10.1. Solving the 15-puzzle.**

After peg
The initial configuration
jumps peg

**Figure 10.2. The initial configuration of the Hi-Q puzzle**
(left), and the same configuration after a single move (right).
Pegs are indicated by a square, and empty holes are indicated
by a circle.

solves the Hi-Q puzzle. Let p = n(n + 4m). Your algorithm should run in
time O((4p)[p][−][2]).

517. The n-queens problem (also known as the peaceful queens
_problem) is the problem of determining the number of ways that n queens_
can be placed on an n _n chessboard so that no queen threatens any other_
_×_
(for example, Figure 10.4 shows one way of placing eight peaceful queens on
an 8 8 chessboard). Devise an exhaustive search algorithm that solves the
_×_
_n-queens problem._


-----

**126** Chap. 10. Exhaustive Search

_m_ _n_ _m_

**Figure 10.3. The generalized Hi-Q puzzle.**

**Figure 10.4. One way of placing eight peaceful queens on**
an 8 8 chessboard.
_×_

518. The I-C Ice Cream Company plans to place ice cream carts
at strategic intersections in Dallas so that for every street intersection, either
there is an ice cream cart there, or an ice cream cart can be reached by
walking along only one street to the next intersection. You are given a map of
Dallas in the form of a graph with nodes numbered 1, 2, . . ., n representing the
intersections, and undirected edges representing streets. For each ice cream
cart at intersection i, the city will levy $ci in taxes. The I-C Ice Cream
Company has k ice cream carts, and can make a profit if it pays at most
$d in taxes. Write a backtracking algorithm that outputs all of the possible
locations for the k carts that require less than $d in taxes. Analyze your
algorithm.

|m|n|m|
|---|---|---|
||||


-----

Sec. 10.6. Applications **127**

519. Design a backtracking algorithm that inputs a natural number C,
and outputs all of the ways that a group of ascending positive numbers can
be summed to give C. For example, if C = 6, the output should be
```
  1+2+3
  1+5
  2+4
  6

```
and if C = 10, the output should be
```
  1+2+3+4
  1+2+7
  1+3+6
  1+4+5
  1+9
  2+3+5
  2+8
  3+7
  4+6
  10

```
520. Devise an algorithm that, given a directed graph G, prints all
Hamiltonian cycles in G. If G has n vertices, your algorithm must run in time
_O(n!). Analyze the running time of your algorithm._

521. Devise an algorithm that, given a directed graph G, prints all
Hamiltonian cycles in G. If G has n vertices, your algorithm must run in time
_O((n_ 1)!). Analyze the running time of your algorithm.
_−_

522. The out-degree of a vertex v in a graph is the number of edges directed
out of v. The out-degree of a graph is the largest out-degree of its vertices.
Devise a backtracking algorithm that, given a directed graph G of out-degree
_d, determines whether G has a Hamiltonian cycle in time O(d[n]). Be sure to_
analyze the running time of your algorithm.

523. If you were given a graph and asked to find all Hamiltonian cycles
in it, which algorithm would you use, the algorithm from Problem 520 or the
algorithm from Problem 522? Explain your answer.

A dominating set of size k in a graph G = (V, E) is a set U _V of k vertices such_
_⊆_
that for all v _V, either v_ _U_, or there exists an edge (u, v) _E such that u_ _U_ .
_∈_ _∈_ _∈_ _∈_
For example, the shaded vertices in the graph of Figure 10.5 form a dominating set.


-----

**128** Chap. 10. Exhaustive Search

**Figure 10.5. A dominating set (shaded vertices).**

524. Let D(n, k) be the number of candidates for a dominating set in an
exhaustive search algorithm. Write a formula for D(n, k) in terms of n and k.

525. Devise an algorithm that, given G and k, finds a dominating set of
size k, if one exists. Your algorithm should run in time O(n[2]D(n, k)). Analyze
the running time of your algorithm.

526. Describe how to improve the running time of your algorithm to
_O(nD(n, k)). Justify briefly the running time of your modified algorithm._

A weighing matrix is an n _n matrix with entries from_ 1, 0, 1 such that the
_×_ _{−_ _}_
scalar product of any two rows is zero. That is, a matrix


_m1,1_ _m1,2_ _. . ._ _m1,n_
_m2,1_ _m2,2_ _. . ._ _m2,n_
...
_mn,1_ _mn,2_ _. . ._ _mn,n_




_,_



_M =_







where for all 1 _j_ _n and all 1_ _i < j,_
_≤_ _≤_ _≤_

_n_
�

_mi,kmj,k = 0._
_k=1_

527. Design an algorithm that finds all n _n weighing matrices in time_
_×_
_O(n[3]3[n][2]). Analyze your algorithm._

528. Describe how to reduce the running time of your algorithm to
_O(n3[n][2])._


-----

Sec. 10.6. Applications **129**


Preference
Matrices:

Candidate
Matching:

Weight:

|1|2|3|4|N|1|2|3|4|
|---|---|---|---|---|---|---|---|---|
|2|3|1|1|1 2 3 4|4|1|3|2|
|1|1|4|3||4|2|3|1|
|1|2|3|4||1|1|1|4|
|2|3|2|1||3|2|3|3|


P[1,2]N[2,1]+P[2,4]N[4,2]+P[3,1]N[1,3]+P[4,3]N[3,4]
= 3.4+3.2+1.3+2.4 = 12+6+3+8 = 29


P 1 2 3 4 N 1 2 3 4

1 2 3 1 1 1 4 1 3 2
2 1 1 4 3 2 4 2 3 1
3 1 2 3 4 3 1 1 1 4
4 2 3 2 1 4 3 2 3 3


Pilot:

Navigator:


1 2 3 4

1 2 3 4


**Figure 10.6.** The preference matrices P and N (top), a
candidate matching (center), and the sum of the weights of
the pairs in this matching (bottom).

Suppose you are given n pilots and n navigators. You have an integer array
_P_ [1..n, 1..n] in which P [i, j] is the preference of pilot i for navigator j, and an
integer array N [1..n, 1..n] in which N [i, j] is the preference of navigator i for pilot
_j. The weight of a pairing of pilot i with navigator j is defined to be P_ [i, j] _N_ [j, i].
_·_
The flight-assignment problem is the problem of pairing each pilot with a navigator
in such a way that the sum of the weights of the pairings is maximized. Figure 10.6
shows an example of the preference arrays, a candidate matching, and the sum of
the weights of the pairs in this matching:

529. Design an algorithm for the flight-assignment problem that runs in time
_O((n + 1)!). Analyze your algorithm._

530. Describe how to improve the running time of your algorithm from Problem 529
to O(n!).

The postage stamp problem is defined as follows. The Fussytown Post Office has n
different denominations of stamps, each a positive integer. Fussytown regulations
allow at most m stamps to be placed on any letter.

531. Design an algorithm that, given n different postage stamp values in
an array P [1..n] and the value of m, computes the length of the consecutive
series of postage values that can legally be realized under these rules starting
with the value 1. For example, if n = 4, m = 5, and the stamps have face
value 1, 4, 12, and 21, then all postage values from 1 to 71 can be realized.
Your algorithm should run in time O(n[m]).


-----

**130** Chap. 10. Exhaustive Search

**Figure 10.7. The 4-ominos.**

532. Design an algorithm that, given n and m, computes the m postage
stamp values that can realize the longest consecutive run of postage values
starting at 1. Analyze your algorithm.

A polyomino, or more precisely, an n-omino is a plane figure made up of n unit-size
squares lined up on a grid. For example, Figure 10.7 shows all of the 4-ominos.

533. Design an algorithm that runs in time O(3[n]) to generate all n-ominos,
including all rotations and reflections.

534. Modify your algorithm to remove all rotations and reflections.

###### 10.7 HINTS

487. Be very careful how you choose your recurrence relation. The obvious choice
of recurrence is quite difficult to solve. The right choice can make it easy.

489. Suppose that A[i] = i for 1 _i_ _n, and pretend that procedure process(A)_
_≤_ _≤_
prints the contents of A. Trace the algorithm by hand to see what it generates
when n = 1, 2, 3, 4. This should give you some intuition as to how it works,
what your induction hypothesis should be, and how the basic structure of
your proof should look.

491. See the hint for Problem 489. Your induction hypothesis should look something like the following:
When n is even, a call to evenpermute(n)

processes all permutations of the values in A[1..n], and

_•_
finishes with the entries in A permuted in some order in which, if re
_•_
peated n 1 times, cycles A[1] through all possible values from 1 to n.
_−_
Determining and describing this permutation is the difficult part.

When n is odd, a call to oddpermute(n)

processes all permutations of the values in A[1..n], and

_•_
finishes with the first and last entries in A swapped.

_•_


-----

Sec. 10.8. Solutions **131**

502. You may need to use the identity from Problem 23.

510. The answer is at most 1.718(n + 1)!. You will need to use the fact that
�n
_i=1_ _[i][! =][ e][ −]_ [1][ ≈] [1][.][718 (where][ e][ is the base of the natural logarithm).]

518. Think about dominating sets.

517. It is possible to solve this problem in time O(n!).

520. The running time gives away the technique to be used. Reduce the problem
to that of generating permutations.

525. Reduce the problem to that of generating combinations, and take advantage
of Section 10.3.

526. Use a minimal-change algorithm.

527. Use the algorithm from Problem 480.

528. See Problem 483.

###### 10.8 SOLUTIONS

487. Let T (n) be the running time of permute(n). Line 6 can be done in time
_O(n). Therefore, T_ (1) = c, and for n > 2, T (n) = nT (n 1) + d(n 1), for
_−_ _−_
some c, d IN. We claim that for all n 1, T (n) = (c + d)n! _d. The proof_
_∈_ _≥_ _−_
is by induction on n. The claim is certainly true for n = 1, since T (1) = c
and (c + d)1! _d = c. Now suppose the hypothesis is true for n. Then,_
_−_

_T_ (n + 1) = (n + 1)T (n) + dn
= (n + 1)((c + d)n! _d) + dn_
_−_
= (c + d)(n + 1)! _d._
_−_

Hence, the running time is O(n!), which is linear in the number of permutations.

520. The following algorithm prints all of the Hamiltonian cycles of a graph G.


-----

**132** Chap. 10. Exhaustive Search

**for each permutation P** [0..n 1] do
_−_
process(P )

**procedure process(P** )
**if hamiltonian(P** ) then print(P )

**function hamiltonian(P** ):boolean
ok:=true
**for i := 0 to n** 1 do
_−_
ok:=ok (P [i], P [(i + 1) mod n]) _E_
_∧_ _∈_
return(ok)
We use an optimal permutation generation algorithm such as one of the algorithms from Section 10.2. Since function hamiltonian(P ) takes time O(n),
the search takes time O(n _n!). The running time can be reduced to O(n!)_
_·_
by observing that all of the permutations can begin with vertex 1.

521. The solution is similar to the solution of Problem 520, but we use a minimalchange algorithm such as Heap’s algorithm (see Section 10.2) to generate
permutations.
We keep a Boolean array D[0..n 1], where D[i] is true iff (P [i], P [(i +1) mod
_−_
_n)_ _E, for 0_ _i < n, and a count of missing edges, called “missing.”_
_∈_ _≤_
We initialize the array and count when processing the first permutation. A
minimal change to P requires a minimal change to the array and the count.
Procedure process is exactly as in the solution to Problem 520.
missing:=0
_P_ := first permutation
process(P )
**for each permutation P in minimal-change order do**
Suppose P [x] and P [y] were just swapped
iprocess(P, x, y)

**procedure edge(i, j)**
_D[i] := (i, j)_ _E_
_∈_
**if (i, j)** _E then missing:=missing+1_
_̸∈_

**procedure iprocess(P, x, y)**
**if ihamiltonian(P, x, y) then print(P** )

**function ihamiltonian(P, x, y):boolean**
iedge(P [(x 1) mod n], P [x]);
_−_
iedge(P [x], P [(x + 1) mod n]);
iedge(P [(y 1) mod n], P [y]);
_−_
iedge(P [y], P [(y + 1) mod n]);
return(missing = 0)


-----

Sec. 10.9. Comments **133**

**procedure iedge(i, j)**
**if D[i]** ((i, j) _E) then_
_∧_ _̸∈_
_D[i]:=false; missing:=missing + 1_
**else if (not D[i])** ((i, j) _E) then_
_∧_ _∈_
_D[i]:=true; missing:=missing_ 1
_−_

The time needed to process the first permutation is O(n). The other n! 1
_−_
permutations require O(1) time each to process. The overhead for generating
the permutations is O(n!) with a minimal-change algorithm such as Heap’s
algorithm. Therefore, the total running time is O(n + (n! 1) + n!) = O(n!).
_−_
As before, this running time can be reduced by a factor of Ω(n) by observing
that all of the permutations can begin with vertex 1.

###### 10.9 COMMENTS

478. The algorithm generates the binary reflected Gray code (see also Problems 96
and 97).

497. The algorithm is adapted from Lam and Soicher [51]. You will find a correctness proof there, but there is an easier and clearer explanation. Another
interesting algorithm with a stronger minimal-change property is given by
Eades and McKay [23].

507. See also Problem 474.

508. See also Problem 475.

512. For more information on Ramsey numbers, consult Graham and Spencer [32],
and Graham, Rothschild, and Spencer [31].

513. See also Problems 48 and 369 (and associated comments), which deal with
closed knight’s tours. Backtracking for n _n closed knight’s tours is only_
_×_
practical for n = 6 (there are no tours for smaller n), in which case there
are 9, 862 closed knight’s tours. It is not known exactly how many 8 8
_×_
tours exist. Rouse Ball and Coxeter [8] describe an interesting random walk
algorithm that they attribute to Euler. A heuristic attributed to Warnsdorff
in 1823 by Conrad, Hindrichs, Morsy, and Wegener [15, 16] appears to help
both the exhaustive search and random walk algorithms find solutions faster:
When there is a choice of squares to move to, move to the one with the least
number of unused legal moves out of it. Takefuji and Lee [79] (reprinted in
Takefuji [78, Chapter 7]) describe a neural network for finding closed knight’s
tours, but empirical evidence indicates that their algorithm is impractical
(Parberry [62]).

517. Although an algorithm that runs in time O(n!) is considered very slow, it


-----

**134** Chap. 10. Exhaustive Search

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

**Table 10.1. The number of solutions to the n-queens prob-**
lem for 6 _n_ 18 and the running time required to ex_≤_ _≤_
haustively search for them using a naive exhaustive search
algorithm. The algorithm was implemented in Berkeley Unix
Pascal on a Sun Sparc 2.

is still usable in practice for very small n. Table 10.1 shows the number
of solutions to the n-queens problem and the running time required to find
them using Berkeley Unix Pascal on Sun Sparc 2. It is known that there is
at least one solution to the n-queens problem for all n 4 (see, for example,
_≥_
Bernhardsson [11]). Heuristics for finding large numbers of solutions (but not
necessarily all of them) include Takefuji [78], and Susic and Gu [77].

518. This problem was described to me by Mike Fellows.

|n|count|time|
|---|---|---|
|6 7 8 9 10 11 12 13|4 40 92 352 724 2,680 14,200 73,712|< 0.001 seconds < 0.001 seconds < 0.001 seconds 0.034 seconds 0.133 seconds 0.6 seconds 3.3 seconds 18.0 seconds|
|14 15|365,596 2,279,184|1.8 minutes 11.6 minutes|
|16 17|14,772,512 95,815,104|1.3 hours 9.1 hours|
|18|666,090,624|2.8 days|


-----

###### Chapter 11

### Data Structures

Algorithms and data structures are obviously very closely related. Firstly, you must
understand algorithms in order to design data structures, since an important issue
in choosing a particular data structure is the availability of efficient algorithms for
creating, updating, and accessing it. Secondly, you must understand data structures
in order to design algorithms, since the proper organization of data is often the
key to developing efficient algorithms. Some schools separate algorithms and data
structures into separate classes, but I prefer to teach them together. In case your
algorithms class requires it, here are some problems on advanced data structures,
principally heaps, binary search trees, AVL trees, 2–3 trees, and the union-find data
structure.

###### 11.1 HEAPS

A heap is a binary tree with the data stored in the nodes. It has two important
properties: balance and structure. Balance means that it is as much like a complete
binary tree as possible. Missing leaves, if any, are on the last level at the far right
(see, for example, Figure 11.1). Structure means that the value in each parent is no
greater than the values in its children (see, for example, Figure 11.2).

535. Prove that the value in each node is no greater than the values in its
descendants (that is, its children, its children’s children, etc.)

**Figure 11.1. A balanced binary tree.**

**135**


-----

**136** Chap. 11. Data Structures

3

9 5

11 20 10 24

21 15 30 40 12

**Figure 11.2. A heap.**

536. Prove by induction that a heap with n vertices has exactly _n/2_ leaves.
_⌈_ _⌉_

537. Suppose a heap is stored in an array H in the standard fashion.
That is, store the root in H[1], and for every node stored in H[k], store its
children in H[2k] and H[2k +1]. Prove that an n-node heap occupies the first
_n contiguous entries of H._

538. Suppose a heap is stored in an array H in the standard fashion (see
Problem 537). Prove that a list of the array elements H[1], H[2], . . ., H[n]
form a breadth-first traversal of the heap.

539. Devise a divide-and-conquer algorithm (see Chapter 7) for building a
heap stored in an array H[1..n] in O(n) time.

540. Give the array representation heap shown in Figure 11.2, and redraw the
heap and its array representation after each of the following operations have
been applied in sequence:

(a) deletemin, followed by
(b) insert the value 0.

541. Construct a heap containing the items 10, 2, 9, 16, 8, 6, 1, 3, 12. You
are to draw the heap (as a binary tree) at each of the major steps in the
construction.

(a) Inserting the items in the order given into an empty heap.
(b) Building the heap from the bottom up, as in heapsort.

542. Write a procedure that, given parameters A, n, and i, where A is the
array representation of an n-element heap, and 1 _i_ _n, deletes the element_
_≤_ _≤_
_A[i] from the heap in O(log n) time._

543. _Halving is the process of taking a set S of integers and separating it_
into two half-sized sets S1, S2, where all of the values in S1 are smaller than
all of the values in S2. Show that halving is equivalent to finding the median,
that is:


-----

Sec. 11.1. Heaps **137**

(a) If the median can be found using T (n) comparisons, then a set of size n
can be halved with T (n) + n 1 comparisons.
_−_

(b) If a set of size n can be halved using T (n) comparisons, then the median
can be found using T (n) + _n/2_ 1 comparisons.
_⌈_ _⌉−_

544. Devise a data structure that supports the following operations on
an n-element set: insert in time O(log n), and deletemin and deletemax in
_O(1) time._

The standard heapsort algorithm uses binary heaps, that is, heaps in which each
node has at most two children. In a k-ary heap, each node has at most k children.
Heapsort works not only with binary heaps, but with k-ary heaps for any k =
1, 2, 3, . . ..

545. Define k-ary heaps and describe a space-efficient implementation in
an array. In particular, describe in detail how to get from any heap element
to its parent and its k children.

546. Write pseudocode for k-ary heapsort.

547. What familiar sorting algorithm is k-ary heapsort for k = 1?

548. For k > 1, analyze the number of binary comparisons used by k-ary
heapsort in terms of n and k, determining the coefficient (depending on k) of
the most significant n-term. Which k minimizes this factor? Why is k = 2
probably best anyway?

A parallel priority queue is a priority queue in which the insert operation inserts
_p values, and the deletemin operation deletes the p smallest values in the priority_
queue and returns them in no particular order. A parallel heap is a data structure
with the same tree structure as a heap, but with p values per node. It also has the
property that all of the values in a node are smaller than the values in its children,
and all of the values in one sibling are smaller than the values in the other (it doesn’t
matter which is the “smaller” sibling). For example, Figure 11.3 shows a parallel
heap with p = 4.
Sequential algorithms for parallel heaps are fairly straightforward: An insert
operation is processed by first placing the p new items in the next unused node d,
which we will call dirty. Combine the values in d and its parent r, and place the
smallest p values into r, and the largest p values into d. Combine the values in d
and its sibling (if it has one), and place the largest p values into the sibling that
had the largest value between them, and the smallest p values into the other sibling.
Node r then becomes the dirty node, which is processed in a similar fashion. For
example, Figure 11.4 shows an insertion into a 4-node parallel heap with p = 4.


-----

**138** Chap. 11. Data Structures

6 1

2 5

19
20 [25]
15
9
8 30 [40]

32 26 25 18
27 45 22 16

**Figure 11.3. A parallel heap with p = 4.**

A deletemin operation is processed by removing the values from the root and
replacing them with the values from the last used node. Call the root dirty. Let
_d be the dirty node. Combine the values in d with those of its smallest child s,_
and place the smallest p values into d and the largest p values into s. Combine the
values in d and its sibling (if it has one), and place the largest p values into the
sibling that had the largest value between them, and the smallest p values into the
other sibling. Node s then becomes the dirty node, which is processed in a similar
fashion.

549. Show that the insert algorithm is correct, that is, it results in a
parallel heap.

550. Show that the deletemin algorithm, that is, it results in a parallel
heap.

551. Analyze the running time of the insert and deletemin algorithms.

###### 11.2 AVL TREES

A binary search tree is a binary tree with the data stored in the nodes. The following
two properties hold:

The value in each node is larger than the values in the nodes of its left subtree.

_•_
The value in each node is smaller than the values in the nodes of its right

_•_
subtree.

552. Prove that if the nodes of a binary search tree are printed in in-order,
they come out sorted.


-----

Sec. 11.2. AVL Trees **139**

Insert (50,3,23,10) Create a new node

6 1 6 1

2 5 2 5

19 19

20 [25] 20 [25]

15 15

30 [40] 8 9 30 [40] 8 9

32 26 32 26 50 3
27 45 27 45 10 23

Combine with parent Combine with sibling

6 1 6 1

2 5 2 5

19 19

3 [10] 15 3 [10] 15

20 23 8 9 20 23 8 9

3227 4526 50253040 26253027 50324540

Combine with parent Combine with sibling

3 1 3 1

2 5 2 5

10 19 15 10

20 236 8 15 9 19 2023 8 96

25 50 25 50

26 27 45 26 27 45

30 32 40 30 32 40

**Figure 11.4. An insertion into a 4-node parallel heap with**
_p = 4._ Heavily outlined nodes have been combined. The
dirty node is shaded.

|Insert (50,3,23,10) 6 1 2 5 25 19 20 15 30 40 8 9 32 26 2745|Create a new node 6 1 2 5 25 19 20 15 30 40 8 9 32 26 50 3 2745 10 23|
|---|---|
|Combine with parent 6 1 2 5 10 19 3 15 20 23 8 9 32 26 5030 2540 2745|Combine with sibling 6 1 2 5 10 19 3 15 20 23 8 9 25 50 26 27 45 30 32 40|
|Combine with parent 3 1 2 5 10 19 6 15 20 23 8 9 25 50 26 27 45 30 32 40|Combine with sibling 3 1 2 5 15 10 19 20 8 6 23 9 25 50 26 27 45 30 32 40|


-----

**140** Chap. 11. Data Structures

100

50 150

30 60 120 160

10 40

**Figure 11.5. An AVL tree.**

100

50 150

30 70 200

20 60 80

**Figure 11.6. A second AVL tree.**

An AVL tree is a binary search tree with one extra structure condition: For every
node, the magnitude of the difference in height between its left and right subtrees is
at most one. (the height of an AVL tree is the number of edges in the longest path
from the root to a leaf). This difference in height is maintained during insertions and
deletions using operations called single rotations and double rotations. Operations
```
insert, delete, member, and findmin can be performed in time O(log n).

```
553. Insert 5 into the AVL tree shown in Figure 11.5.

554. Insert 55 into the AVL tree shown in Figure 11.6.

555. Delete 30 from the AVL tree shown in Figure 11.7.

556. Find an AVL tree for which the deletion of a node requires two single
rotations. Draw the tree, indicate the node to be deleted, and explain why
two rotations are necessary and sufficient.


-----

Sec. 11.3. 2–3 Trees **141**

100

50 150

30 120 200

210

**Figure 11.7. A third AVL tree.**

557. Find an AVL tree for which the deletion of a node requires two double
rotations. Draw the tree, indicate the node to be deleted, and explain why
two rotations are necessary and sufficient.

558. Show that for all n IN, there exists an AVL tree for which the
_∈_
deletion of a node requires n (single or double) rotations. Show how such
a tree is constructed, indicate the node to be deleted, and explain why n
rotations are necessary and sufficient.

559. Prove that the height of an AVL tree with n nodes is at most
1.4404 log n.

###### 11.3 2–3 TREES

A 2–3 tree in a tree in which every internal vertex has 2 or 3 children, and every
path from the root to a leaf has the same length. The data are stored in the leaves in
sorted order from left to right. The internal nodes carry information to allow searching, for example, the largest values in the left and center subtrees. Insertions and
deletions are performed using a divide-and-conquer algorithm. Operations insert,
```
delete, member and findmin can be performed in time O(log n).

```
560. Insert the following elements in sequence into an initially empty 2–3
tree: 5, 2, 7, 0, 3, 4, 6, 1, 8, 9. Show the 2–3 tree after every insertion. Be sure
to include all of the information that is kept in the internal nodes. Delete the
element 3 from the resulting 2–3 tree.

561. Give a sequence of insertions and deletions that constructs the 2–3 trees
shown in Figure 11.8 (starting from the empty 2–3 tree each time). Draw the
2–3 tree after every insertion and deletion operation.


-----

**142** Chap. 11. Data Structures


(a) 3:5 (b) 2:5 (c)


2:4

|4|:5|
|---|---|

|3|:4|
|---|---|

|3|:4|
|---|---|


1 2 3 4 5 6 7 1 2 3 4 5 6 7 1 2 3 4 5 6 7

**Figure 11.8. Three 2–3 trees.**

###### 11.4 THE UNION-FIND PROBLEM

Given a set 1, 2, . . ., n initially partitioned into n disjoint subsets, one member
_{_ _}_
per subset, we want to perform the following operations:
```
  find(x): return the name of the subset that x is in, and

```
_•_
```
  union(x, y): combine the two subsets that x and y are in.

```
_•_

There is a standard data structure using a tree. Use a tree:

implemented with pointers and records;

_•_
set elements are stored in the nodes;

_•_
each child has a pointer to its parent;

_•_
there is an array P [1..n] with P [i] pointing to the node containing i.

_•_

There is an algorithm for union and find operations that works in worst-case time
_O(log n) and amortized time O(log[∗]n)._

562. Design an algorithm that can perform a sequence m union and
```
  find operations on a Universal set of n elements, consisting of a sequence of
  unions followed by a sequence of finds, in time O(m + n).

```
Suppose we modify the union-find algorithm so that the root of the shallower tree
points to the root of the deeper tree (instead of the root of the smaller tree pointing
to the root of the deeper tree).

563. Does this affect the running time of the algorithm in the worst case?

564. Does it affect the amortized running time when path compression is
used?

###### 11.5 APPLICATIONS

This section asks you to use your knowledge of data structures to design algorithms
for new problems.


-----

Sec. 11.5. Applications **143**

565. Design a data structure for a set in which insertions, deletions, and
membership queries can be processed in O(1) time in the worst case. You may
assume that the set elements are integers drawn from a finite set 1, 2, . . ., n .
_{_ _}_

566. Let S = {s1, s2, . . ., sℓ} and T = {t1, t2, . . ., tm} be two sets of integers such that 1 ≤ _si, tj ≤_ _n for all 1 ≤_ _i ≤_ _ℓ_ and 1 ≤ _j ≤_ _m. Design an_
algorithm for determining whether S = T in time O(ℓ + m).

567. Design an implementation of the following Abstract Data Type:
a set with the operations:

`insert(x, T` ) Insert item x into the set T .
`delete(k, T` ) Delete the kth smallest element from T .
`member(x, T` ) Return true iff x _T_ .
_∈_

All operations on an n item set are to take time O(log n).

568. Design an implementation of the following Abstract Data Type: a
set with the operations:

`insert(x, T` ) Insert item x into the set T .
`delete(x, T` ) Delete x from T .
`member(x, T` ) Return true iff x _T_ .
_∈_
`next(x, T` ) Return the smallest element of T greater than x
`union(S, T` ) Set S to the union of S and T .

The operations insert, delete, member, and next are to take time O(log n),
and union is to take time O(n).

569. Design an implementation of an Abstract Data Type consisting of a
set with the following operations:

`insert(S, x)` Insert x into the set S.
`delete(S, x)` Delete x from the set S.
`member(S, x)` Return true if x _S, false otherwise._
_∈_
`position(S, x)` Return the number of elements of S less than x.
`concatenate(S, T` ) Set S to the union of S and T, assuming every
element in S is smaller than every element of T .

All operations involving n-element sets are to take time O(log n).

570. The bin packing problem is the following. You are given n metal objects, each weighing between zero and one kilogram. You also have a collection
of large, but fragile bins. Your aim is to find the smallest number of bins that
will hold the n objects, with no bin holding more than one kilogram.


-----

**144** Chap. 11. Data Structures

The first-fit heuristic for the bin packing problem is the following. Take each
of the objects in the order in which they are given. For each object, scan the
bins in increasing order of remaining capacity, and place it into the first bin
in which it fits. Design an algorithm that implements the first-fit heuristic
(taking as input the n weights w1, w2, . . ., wn and outputting the number of
bins needed when using first-fit) in O(n log n) time.

571. Suppose (A, ·) is a semigroup, where A = {a1, . . ., an}. (That is,
_A is closed under “_ ”, and “ ” is associative.) Devise a data structure that

_·_ _·_
allows you to compute ai · ai+1 · · · aj for any i ≤ _j in only O(log n) semigroup_
operations.

572. Reduce the running time in Problem 571 to O(1) when (A, ) is a
_·_
group, and group inversion is allowed for free.

573. The Dallas Tollway uses a computerized toll collection system.
The highway is modeled as as an ordered list of toll booths t1, t2, . . ., tn in
which toll booth ti collects a toll of $ai, for 1 ≤ _i ≤_ _n. Design a data structure_
that can perform the following operations in O(log n) time.

`insert(k, a)` Insert a new toll booth after tk with toll $a.
`delete(k)` Delete toll booth tk.
`toll(i, j)` Return total toll for booths i through j, inclusive.
`update(i, j, a)` Add $a to the toll for booths i through j, inclusive.

574. Suppose we are to support a set of ordered pairs (p, k), where k is an
integer key and p is an integer priority. Devise a data structure in which the
following operations can be implemented in O(log n) time:

`insert(p, k)` Insert item with priority p and key k
`member(k)` Return item of smallest priority among those with key _k._
_≤_
`delete(k)` Delete all items with key k.

You are to design a memory-efficient data structure that is constructed from a
sequence of n values x1, x2, . . ., xn, and can quickly answer queries of the form:
“Given i, j, find the smallest value in xi, . . ., xj.”

575. Design a data structure that uses O(n log n) space and answers queries
in O(log n) time.

576. Design a data structure that uses O(n) space and answers queries in
_O(log n) time._


-----

Sec. 11.6. Hints **145**

577. Use your solution to Problem 576 to design a data structure to quickly
answer least-common-ancestor queries in a tree. That is, your data structure
will be constructed from a description of a tree, and using this data structure
you must answer queries of the form: “What is the least-common-ancestor of
tree vertices v and w?”

###### 11.6 HINTS

535. Prove it by induction on level.

537. Prove it by induction on n.

544. Use two heaps A and B, each containing _n/2_ elements (if n is odd, store
_⌈_ _⌉_
one item separately). Make A a min-heap, B a max-heap, and ensure that
for each 1 _i_ _n/2_, A[i] _B[i]. Then, the root of A will be the smallest_
_≤_ _≤⌈_ _⌉_ _≤_
value and the root of B will be the largest value.

551. See Problem 543.

559. Let N (h) be the minimum number of nodes in an AVL tree of height h.
Devise a recurrence relation for a lower bound for N (h) (start with N (0) = 1,
_N_ (1) = 2). Show that this recurrence has solution


�h
_._


_N_ (h) >


� _√_
1 + 5

2


562. It’s the standard union-find algorithm with path compression. The difficult
part is the amortized analysis.

570 You will need a data structure that allows you to find the “first bin in which
it fits” in time O(log n).

###### 11.7 SOLUTIONS

545. A k-ary heap is a k-ary tree with the data stored in the nodes. It has two
important properties: balance and structure. _Balance means that it is as_
much like a complete k-ary tree as possible. Missing leaves, if any, are on the
last level at the far right. Structure means that the value in each parent is
no greater than the values in its children. A k-ary heap on n vertices can be
efficiently implemented in storage using contiguous locations of a linear array
_A[1..n], such that the root of the heap is stored in A[1], the vertices are stored_
in level order, and for any level, the vertices in it are stored in left-to-right


-----

**146** Chap. 11. Data Structures

order. It can be shown that the parent of A[m] is A[ (m + k 2)/k ] and its
_⌊_ _−_ _⌋_
children are A[km _k + 2], . . ., A[min(km + 1, n)]._
_−_

559. Let N (h) be the minimum number of nodes in an AVL tree of height h.
Clearly, N (0) = 1 and N (1) = 2, and for h 2, N (h) > N (h 1) + _N_ (h 2).
_≥_ _−_ _−_
We claim that N (h) _c[h]_ for some choice of c. The proof is by induction on
_≥_
_h. The claim is true for h_ 2 provided c < 2. For h > 2, by the induction
_≤_
hypothesis,
_N_ (h) > N (h 1) + N (h 2) _c[h][−][1]_ + c[h][−][2].
_−_ _−_ _≥_

So we need (assuming c > 0) c[2] _c_ 1 0. The largest value of c for which
_−_ _−_ _≤_
_√_
this is true is (1 + 5)/2. Therefore, by induction,


�h


_N_ (h) >


� _√_
1 + 5

2


_._


What is the height of an AVL tree with n nodes? We know that


�h
_._


_n_ _N_ (h) >
_≥_


� _√_
1 + 5

2


Therefore,


log n
_h <_ _√_

log((1 + 5)/2)

_[≈]_ [1][.][4404 log][ n.]


567. We use a 2–3 tree augmented with extra fields in each internal node recording
how many leaves are descendants of the left, middle, and right children. The
insertion is done as normal, with extra code to increment the leaf-count of the
nodes on the path from the root to the new leaf, and to take care of the new
fields during node splitting. The deletion code is modified in a similar way,
with the extra modification that the location of the leaf to be deleted is done
using the new leaf-count fields in the obvious way (recall that in a 2–3 tree,
the leaves are in ascending order from left to right). The member operations
are done as normal.

###### 11.8 COMMENTS

537. You’ll see this result in all competent data structures textbooks, but you’ll
seldom see a proof of it.

570. This problem is -complete (see Chapter 12 if you don’t know what this
_NP_
means), and so it is unlikely that there is a polynomial-time algorithm for
finding an exact solution.


-----

###### Chapter 12

### -completeness
###### NP

Define to be the set of decision problems (that is, problems that have a yes/no
_P_
answer) that can be solved in polynomial time. If x is a bit string, let _x_ denote the
_|_ _|_
number of bits in x. Define to be the set of decision problems of the following
_NP_
form, where R, c IN: “Given x, does there exist y with _y_ _x_ such that
_∈P_ _∈_ _|_ _| ≤|_ _|[c]_
(x, y) _R.” That is,_ is the set of existential questions that can be verified in
_∈_ _NP_
polynomial time. Clearly, . It is not known whether =, although
_P ⊆NP_ _P_ _NP_
the consensus of opinion is that probably = . But it is known that there are
_P ̸_ _NP_
problems in with the property that if they are members of, then = .
_NP_ _P_ _P_ _NP_
That is, if anything in is outside of, then they are, too. They are called
_NP_ _P_
_-complete problems._
_NP_
A problem A is reducible to B if an algorithm for B can be used to solve A.
More specifically, if there is an algorithm that maps every instance x of A into an
instance f (x) of B such that x _A iff f_ (x) _B. A problem A is polynomial time_
_∈_ _∈_
_reducible to B, written A ≤p[m]_ _[B][, if there is a polynomial time algorithm that maps]_
every instance x of A into an instance f (x) of B such that x _A iff f_ (x) _B. Note_
_∈_ _∈_
that the size of f (x) can be no greater than a polynomial of the size of x.
Listing problems on -completeness is a little bit redundant. The truly dedi_NP_
cated student can practice by picking two random -complete problems from the
_NP_
long list in the back of Garey and Johnson [28] and attempting to prove that one
is reducible to the other. But here are a few problems that I find useful.

###### 12.1 GENERAL

This section contains a few general questions about -completeness. Many of
_NP_
them use variants of the satisfiability problem. The standard terminology is used
here: A literal is a complemented or uncomplemented variable, a clause is a disjunction of literals, and a Boolean formula is a conjunction of clauses. Then SAT
is defined as follows:

**SAT**
Instance: A Boolean formula F .

**147**


-----

**148** Chap. 12. -completeness
_NP_

Question: Is there a truth assignment to the variables of F that makes
_F true?_

578. Prove that “≤p[m][” is transitive, that is, if][ A][ ≤]p[m] _[B][ and][ B][ ≤]p[m]_ _[C][,]_
then A ≤p[m] _[C][.]_

579. 2SAT is the satisfiability problem with at most two literals per clause.
Show that 2SAT .
_∈P_

580. A monom is a conjunction of literals. A Boolean formula in disjunctive
_normal form is a disjunction of monoms. Consider the following problem:_

**DNF SAT**
Instance: A Boolean formula F in disjunctive normal form.
Question: Is there a truth assignment to the variables of F that
makes F true?

Prove that DNF SAT .
_∈P_

581. Show that the following problem can be solved in polynomial time:

**STRONG 3SAT**
Instance: A Boolean formula F in conjunctive normal form with
at most three literals per clause.
Question: Is there a truth assignment to the variables of F that
makes at least two literals in each clause of F true?

582. Show that the following problem can be solved in polynomial time:

**PARITY 3SAT**
Instance: A Boolean formula F in conjunctive normal form with
at most three literals per clause.
Question: Is there a truth assignment to the variables of F that
makes an odd number of literals in each clause of F true?

###### 12.2 COOK REDUCTIONS

The definition of “reduction” used in the preamble to this chapter is the one most
commonly used in algorithms classes. Technically, it is called a polynomial time
_many-one reduction or a Karp reduction (after Karp [43])._
There is another definition of reducibility that you will meet in the literature if
you read more about -completeness. A problem A is polynomial time Turing
_NP_
_reducible to B, written A ≤p[T]_ _[B][, if there is an algorithm for][ B][ that calls the]_


-----

Sec. 12.2. Cook Reductions **149**

algorithm for A as a subroutine, and this algorithm makes polynomially many calls
to A and runs in polynomial time if the calls to A are not counted. This type of
reduction is sometimes called a Cook reduction after Cook [17].

583. Prove that if A ≤p[T] _[B][ and][ B][ ∈P][, then][ A][ ∈P][.]_

584. Prove that if B ∈NP and for all A ∈NP, A ≤p[T] _[B][, then][ B][ is][ NP][-]_
complete.

585. Prove that “≤p[T] [” is transitive, that is, if][ A][ ≤]p[T] _[B][ and][ B][ ≤]p[T]_ _[C][, then]_
_A ≤p[T]_ _[C][.]_

586. Prove that if B ≤p[T] _[C][,][ C][ ∈NP][, and][ B][ is][ NP][-complete, then][ C][ is]_
-complete.
_NP_

Consider the following two versions of the satisfiability problem.

**SAT1**
Instance: A Boolean formula F .
Question: Is there a truth assignment to the variables of F that makes
_F true?_

**SAT2**
Instance: A Boolean formula F .
Output: A truth assignment to the variables of F that makes F true,
if one exists.

The former is the decision problem for satisfiability, and the second requires the
construction of a solution. Clearly the decision problem is Cook reducible to the
solution problem. The term self-reducibility, coined by Mike Paterson, is used to
describe problems for which the opposite is true.

587. Show that SAT2 ≤p[T] [SAT1.]

Consider the following variants of the traveling salesperson problem:

**TSP1**
Instance: A directed graph G with positive costs on the edges, and a
positive integer B.
Question: Is there a Hamiltonian cycle in G of cost at most B?

**TSP2**
Instance: A directed graph G with positive costs on the edges, and a
positive integer B.
Output: A Hamiltonian cycle in G of cost at most B, if one exists.


-----

**150** Chap. 12. -completeness
_NP_

**TSP3**
Instance: A directed graph G with positive costs on the edges, and a
positive integer B.
Output: A Hamiltonian cycle in G of minimum cost, if one exists.

588. Prove that TSP2 ≤p[T] [TSP1.]

589. Prove that TSP3 ≤p[T] [TSP2.]

590. Prove directly that TSP3 ≤p[T] [TSP1, without using the fact that “][≤]p[T] [”]
is transitive.

###### 12.3 WHAT IS WRONG?

Scientists have been working since the early 1970s to either prove or disprove that
= . This open problem is rapidly gaining popularity as one of the leading
_P ̸_ _NP_
mathematical open problems today (ranking with Fermat’s last theorem and the
Reimann hypothesis). There are several incorrect proofs that = announced
_P_ _NP_
every year. What is wrong with the following proofs that = ?
_P_ _NP_

591. It is known that the dominating set problem (see also Problem 523)
remains -complete even when the dominating set is required to be con_NP_
nected (see, for example, Garey and Johnson [28]). The interior nodes of a
breadth-first search tree form a connected dominating set. For each vertex
_v of a graph G = (V, E) with n vertices and e edges, find the breadth-first_
search tree rooted at v in time O(n + _e). Then, pick the tree with the smallest_
number of interior vertices. These form a minimum-size connected dominating
set, found in time O(ne + n[2]). Hence, = .
_P_ _NP_

592. It is known that 3SAT is -complete. Given a Boolean formula in
_NP_
conjunctive normal form with at most three literals per clause, use the distributive law to construct an equivalent formula in disjunctive normal form.
For example,

(x1 ∨ _x2 ∨_ _x3) ∧_ (x1 ∨ _x2) = (x1 ∧_ _x2) ∨_ (x2 ∧ _x1) ∨_ (x3 ∧ _x1) ∨_ (x3 ∧ _x2)._

Since DNF-SAT (see Problem 580), a satisfying assignment for the new
_∈P_
formula, and hence for the old formula, can be found in polynomial time. This
shows that 3SAT, and hence that = .
_∈P_ _P_ _NP_

593. The knapsack problem is defined as follows:

**KNAPSACK**
Instance: Positive integers s1, s2, . . ., sn, S
Question: Does there exist X ⊆{1, 2, . . ., n} such that [�]i∈X _[s][i][ =]_
_S?_


-----

Sec. 12.3. What is Wrong? **151**

It is known that KNAPSACK is -complete. However, in Section 8.2 we
_NP_
saw a dynamic programming algorithm for the knapsack problem that runs
in time O(nS). Therefore, KNAPSACK, and hence = .
_∈P_ _P_ _NP_

594. A split Turing machine is a variant of the Turing machine
in which the input and the computation are each split into two parts. (To
refresh your memory about standard Turing machines see, for example, Aho,
Hopcroft, and Ullman [1].) The first part of the computation (which uses a
Turing machine) has access to the first part of the input only, and the second
part of the computation (which uses Boolean formula evaluation) has access
both to the second part of the input and to the output of the first part of the
computation. The first part of the input is a string of bits that is presented
as input to a standard Turing machine in the usual manner, together with
the representation, in unary, of a natural number k. The Turing machine
computes in the normal manner, and produces an output of exactly k bits.
The second part of the input is the encoding of a Boolean formula using the
standard encoding scheme from Garey and Johnson [28].

A deterministic split Turing machine M is said to accept an input string
_x#y, where x_ IB[n], y IB[m], iff y is the encoding of a Boolean formula F
_∈_ _∈_
with k variables, and M on input x#1[k] outputs a satisfying assignment for
_F_ . The time taken by a computation of a deterministic split Turing machine
_M on input x#y is the number of steps taken by M on input x#1[k]. The time_
complexity of M is defined to be

_TM_ (n, m) = max{t | there is an x#y where x ∈ IB[n], y ∈ IB[m], where y
encodes a Boolean formula on k variables, such that the
computation of M on input x#1[k] takes time t .
_}_

A nondeterministic split Turing machine M is said to accept an input string
_x#y, where x_ IB[n], y IB[m], iff y is the encoding of a Boolean formula F with
_∈_ _∈_
_k variables, and some computation of M on input x#1[k]_ outputs a satisfying
assignment for F . The time taken by a computation of a deterministic split
Turing machine M on input x#y is the minimum over all accepting computations of M of the number of steps taken by M on input x#1[k]. The time
complexity of M is defined to be

_TM_ (n, m) = max{1} ∪{t | there is an x#y where x ∈ IB[n], y ∈ IB[m],
where y encodes a Boolean formula on k variables, such
that M takes time t to accept x#1[k] .
_}_

A split Turing machine M is said to run in polynomial time if there exists
a polynomial p such that for all m, n ≥ 1, TM (n, m) ≤ _p(n, m). The class_


-----

**152** Chap. 12. -completeness
_NP_

split- is then defined to be the set of languages accepted by a deterministic
_P_
split Turing machine in polynomial time, and the class split- is defined to
_NP_
be the set of languages accepted by a nondeterministic split Turing machine
in polynomial time.

We claim that split- = split- . The proof is as follows. Consider the
_P ̸_ _NP_
language S that consists of the strings ε#y such that y is the encoding of
a satisfiable Boolean formula F . Clearly, S split-, since the Turing
_∈_ _NP_
machine on input ε#1[k], where k is the number of variables in F, merely
need guess an output string of k bits, which it can do in time linear in k,
which is linear in the number of bits in y. However, S cannot be in split-,
_P_
since the deterministic part of the computation has access only to the number
of variables in F, and hence must give the same output for the two-variable
Boolean formulae x1∧x2 and x1∧x2. Both of these formulae are satisfiable, yet
since there is no truth assignment that satisfies them both, any deterministic
split Turing machine must make an error on one of them. Thus, S split-,
_∈_ _NP_
and S split-, and so split- = split- .
_̸∈_ _P_ _P ̸_ _NP_

Now, it is easy to see that = split- . To see that split-, simply
_P_ _P_ _P ⊆_ _P_
assume that L is encoded in binary, and append to every member of
_∈P_
_L a fixed string encoding the identity formula. Clearly, this is a member of_
split- . To see that split-, note that a deterministic Turing machine can
_P_ _P ⊆P_
simulate a split Turing machine with polynomial overhead in time by simply
simulating the Turing machine part and then evaluating the Boolean formula
on the result obtained. This implies that = split-, and it can be similarly
_P_ _P_
shown that = split- . Hence, = split- = split- = .
_NP_ _NP_ _P_ _P ̸_ _NP_ _NP_

###### 12.4 Circuits

An architecture is a finite combinational circuit (that is, a circuit constructed without feedback loops) with the gate functions left unspecified. A task for an architecture is an input-output pair, and a task set is a finite set of tasks. The loading
_problem is the following: Given an architecture and a task set, find functions for_
each of the gates that enable the circuit to give the correct output for each corresponding input in the task set. The following questions deal with the decision
problem version of the loading problem: Given an architecture and a task set, decide whether there exist functions for each of the gates that enable the circuit to
give the correct output for each corresponding input in the task set. The problems
in this section are from Parberry [63].

595. Show that the loading problem is -complete.
_NP_

596. Show that the loading problem for circuits of depth 2 is _NP_
complete.


-----

Sec. 12.5. One-in-Three 3SAT **153**

597. Show that the loading problem for circuits of fan-in 3 is _NP_
complete.

598. Show that the loading problem for circuits with node-function
set consisting of disjunctions and conjunctions of literals is -complete even
_NP_
for circuits with only four nodes.

A cyclic circuit is a network of gates that may have cycles. Time is quantized,
and at each step, one or more of the gates reads its inputs, and computes a new
output. All connections are directed, and self-loops are allowed. The gate-functions
are limited to are conjunction, disjunction, and complement. The circuit is said to
have converged to a stable configuration if the output of all gates remains fixed over
time. Consider the following problems:

**The Stable Configuration Problem (SNN)**
Instance: A cyclic circuit M .
Question: Does M have a stable configuration?

599. Show that SNN is -complete.
_NP_

600. Show that SNN is -complete for cyclic circuits of fan-in 2.
_NP_

###### 12.5 ONE-IN-THREE 3SAT

Consider the following variants of One-in-Three 3SAT:

**One-in-Three 3SAT (O3SAT1)**
Instance: A list of clauses C in which each clause contains at most
three literals.
Question: Is there a truth assignment for C in which each clause
contains exactly one true literal?

**One-in-Three 3SAT (O3SAT2)**
Instance: A list of clauses C in which each clause contains exactly
three literals.
Question: Is there a truth assignment for C in which each clause
contains exactly one true literal?

**One-in-Three 3SAT (O3SAT3)**
Instance: A list of clauses C in which each clause contains exactly
three variables, all uncomplemented.
Question: Is there a truth assignment for C in which each clause
contains exactly one true variable?


-----

**154** Chap. 12. -completeness
_NP_

**Balanced One-in-Three 3SAT (B3SAT)**
Instance: A list of clauses C in which each clause consists of three
variables and every variable appears in exactly three clauses.
Question: Is there a truth assignment for C in which each clause
contains exactly one true variable?

O3SAT1 is the original version of the problem studied by Schaefer [68], and O3SAT3
is the version listed by Garey and Johnson [28]. In the following problems, you may
assume that O3SAT1 is -complete.
_NP_

601. Prove that O3SAT2 is -complete.
_NP_

602. Prove that O3SAT3 is -complete.
_NP_

603. Prove that B3SAT is -complete.
_NP_

###### 12.6 FACTORIZATION

Let pi denote the ith prime number, starting with p1 = 2. The factorization problem
is defined as follows:

**FACTORIZATION**
Instance: A natural number, N .
Output: A list of pairs (pi, ai) for 1 ≤ _i ≤_ _k, such that N = p[a]1[1][p]2[a][2]_ _[· · ·][ p]k[a][k]_ [.]

604. Prove that if =, then FACTORIZATION can be solved in
_P_ _NP_
polynomial time.

The Smarandache function, η : IN IN, is defined as follows: η(k) is the smallest
_→_
_m_ IN such that k divides evenly into m!.
_∈_

605. Prove that if FACTORIZATION can be solved in polynomial time,
then the Smarandache function can be computed in polynomial time.

606. Prove that if the Smarandache function can be computed in polynomial time, then FACTORIZATION can be solved in polynomial time.

###### 12.7 HINTS

594. A lot of the details of this proof are missing. Most of them are correct. At
least one of them is wrong. It is up to you to discover which.

604. Prove a Turing reduction to the problem “is there a factor less than M .”


-----

Sec. 12.8. Solutions **155**

###### 12.8 SOLUTIONS

595–597. A solution to these problems can be found in Judd [41].

598. A solution to this problem can be found in Parberry [61].

599–600. A solution to this problem can be found in Parberry [63].

603. A solution to this problem can be found in Parberry [60]. However, the
reduction is from O3SAT3, not O3SAT1 as requested; so technically you’ll
have to solve Problem 602 in order to complete this proof.

###### 12.9 COMMENTS

578. Most textbooks (and classes) prove that if A ≤p[m] _[B][ and][ B][ ∈P][, then][ A][ ∈P][,]_
and omit the proof of this result saying only that it is “similar.”

591. This problem came out of a conversation with B. Chitturi in 1994.

594. In a fever-induced dream in 1993 I hallucinated that I had succeeded in proving that =, and this was the proof. I awoke at 3 A.M. and instantly
_P_ _NP_
knew that the proof was wrong (I was not that sick!).

595. For more information on the complexity of variants of the loading problem,
consult also Judd [39, 40, 42], Lin and Vitter [53], and Blum and Rivest [12,
13].


-----

###### Chapter 13

### Miscellaneous

Here are some miscellaneous problems, defined to be those that do not necessarily
fit into the earlier chapters, and those for which part of the problem is to determine
the algorithmic technique to be used. You’re on your own!

###### 13.1 SORTING AND ORDER STATISTICS

This section contains questions on sorting and order statistics (the latter is a fancy
name for “find the k smallest element”). These are mainly upper bounds. Problems
on lower bounds are mostly (but not exclusively) found in Section 13.2.

607. Show that n positive integers in the range 1 to k can be sorted in time
_O(n log k)._

608. Devise an algorithm for finding the k smallest elements of an unsorted
set of n integers in time O(n + k log n).

609. Show that finding the median of a set S and finding the kth smallest
element are reducible to each other. That is, if _S_ = n, any algorithm for
_|_ _|_
finding the median of S in time T (n) can be used to design an O(T (n)) time
algorithm for finding the kth smallest, and vice-versa, whenever the following
holds: T is monotone increasing and there exists a constant 0 < c < 1 such
that T (n/2) < c _T_ (n) for n IN.
_·_ _∈_

The nuts and bolts problem is defined as follows. You are given a collection of n
bolts of different widths, and n corresponding nuts. You are allowed to try a nut
and bolt together, from which you can determine whether the nut is too large, too
small, or an exact match for the bolt, but there is no way to compare two nuts
together, or two bolts together. You are to match each bolt to its nut.

610. Show that any algorithm for the nuts and bolts problem must
take Ω(n log n) comparisons in the worst case.

**156**


-----

Sec. 13.2. Lower Bounds **157**

611. Devise an algorithm for the nuts and bolts problem that runs
in time O(n log n) on average .

612. Suppose that instead of matching all of the nuts and bolts, you wish to
find the smallest bolt and its corresponding nut. Show that this can be done
with only 2n 2 comparisons.
_−_

###### 13.2 LOWER BOUNDS

The lower bounds considered in this section are for what is known as comparison_based algorithms. These are algorithms that store their input in memory, and the_
only operations permitted on that data are comparisons and simple data movements
(that is, the input data are not used for computing an address or an index). The
two most common techniques used are the adversary argument and the decision
_tree._

613. Show a matching lower bound for the sorting problem of Problem 607
in a comparison-based model.

614. Prove that any comparison-based algorithm that searches a sorted
array must make at least Ω(log n) comparisons.

615. Show that any comparison-based algorithm for finding the median must
use at least n 1 comparisons.
_−_

616. Show that any comparison-based algorithm for finding the second-smallest
of n values can be extended to find the smallest value also, without requiring
any more comparisons to be performed.

617. Show that at least n + log n 2 comparisons are necessary to find
_⌊_ _⌋−_
the smallest and second smallest of a list of n items.

618. Show that any comparison-based algorithm for sorting can be modified
to remove all duplicates without requiring any more comparisons to be performed.

619. Show that any comparison-based algorithm for removing duplicates
from a list of values must use Ω(n log n) comparisons.

620. Use decision trees to find a lower bound of

_n + 0.5 log n_ 2.66
_−_

on the number of comparisons required to find the median. You may use
Stirling’s approximation,
_√_
_n!_ 2πn(n/e)[n].
_∼_


-----

**158** Chap. 13. Miscellaneous

621. Show that if each of the n! permutations is equally likely, then
the average key is about n/3 places from its proper position in sorted order.
What does this say about the average case complexity of bubblesort?

###### 13.3 GRAPH ALGORITHMS

This section contains general questions on graph algorithms. More graph algorithm
problems can be found in Sections 2.10, 2.11, 7.7, 8.4, 9.2, 9.3, 9.4, and 13.4, and a
few scattered in applications sections in various chapters.

622. An ancestor query for a tree is a request for information about the
ancestor relationship between two nodes in the tree. It can be viewed as
evaluating the function:


ancestor(v, w) =








1 if v is a proper ancestor of w
_−_
1 if w is a proper ancestor of v
0 otherwise.


Design and analyze an algorithm that takes a tree as input and preprocesses
it so that ancestor queries can subsequently be answered in O(1) time. Preprocessing of an n-node tree should take O(n) time.

623. Let G = (V, E) be a directed graph with n vertices. A sink is a vertex
_s_ _V such that for all v_ _V, (v, s)_ _E. Devise an algorithm that, given the_
_∈_ _∈_ _̸∈_
adjacency matrix of G, determines whether or not G has a sink in time O(n).

624. Suppose a set of truck drivers work for a shipping company that delivers commodities between n cities. The truck drivers generally ignore their
instructions and drive about at random. The probability that a given truck
driver in city i will choose to drive to city j is pij. You may assume that for
all 1 ≤ _i, j ≤_ _n, 0 ≤_ _pij ≤_ 1, and that for all 1 ≤ _i ≤_ _n,_ [�]j[n]=1 _[p][ij][ = 1. Devise]_
an algorithm that determines in time O(n[3]) the most probable path between
cities i and j for all 1 _i, j_ _n._
_≤_ _≤_

625. A graph is triconnected if there is no pair of vertices whose removal
disconnects the graph. Design an algorithm that determines whether a graph
with n vertices and e edges is triconnected in time O(ne).

Let G = (V, E) be a directed labeled graph with n vertices and e edges. Suppose
the cost of edge (v, w) is ℓ(v, w). Suppose c = (v0, v2 . . ., vk−1) is a cycle, that is,
(vi, v(i+1)modk) ∈ _E for all 0 ≤_ _i < k. The mean cost of c is defined by_


_µ(c) = [1]_

_k_


_k−1_
� _w(vi, v(i+1)modk)._

_i=0_


-----

Sec. 13.3. Graph Algorithms **159**

Let µ be the cost of the minimum mean-cost cycle in G, that is, the minimum value
of µc over all cycles c in G.
Assume without loss of generality that every v _V is reachable from a source_
_∈_
vertex s ∈ _V . Let δ(v) be the cost of the cheapest path from s to v, and δk(v) be_
the cost of the cheapest path of length exactly k from s to v (if there is no path
from s to v of length exactly k, then δk(v) = ∞).

626. Show that if µ = 0, then G contains no negative-cost cycles and for
all v _V,_
_∈_

_δ(v) =_ min
0≤k≤n−1 _[δ][k][(][v][)][.]_

627. Show that if µ = 0, then for all vertices v _V,_
_∈_

_δn(v) −_ _δk(v)_
max 0.
0≤k≤n−1 _n −_ _k_ _≥_

628. Let c be a cycle of cost zero, and let u, v be any pair of vertices
on c. Suppose that the cost of the path from u to v along c is x. Prove that
_δ(v) = δ(u) + x._

629. Show that if µ = 0, then there exists a vertex v on the minimum
mean-cost cycle such that

_δn(v) −_ _δk(v)_
max = 0.
0≤k≤n−1 _n −_ _k_

630. Show that if µ = 0, then


_δn(v) −_ _δk(v)_
min max = 0.
_v∈V_ 0≤k≤n−1 _n −_ _k_

631. Show that if we add a constant c to the cost of every edge of G, then
_µ is increased by exactly c. Hence, show that_

_δn(v) −_ _δk(v)_
_µ = min_ max _._
_v∈V_ 0≤k≤n−1 _n −_ _k_

632. Give an O(ne) time algorithm to compute µ.


-----

**160** Chap. 13. Miscellaneous

###### 13.4 MAXIMUM FLOW

Suppose we are given a directed graph G = (V, E) in which each edge (u, v) _E_
_∈_
is labeled with a capacity c(u, v) IN. Let s, t _V be distinguished vertices called_
_∈_ _∈_
the source and sink, respectively. A flow in G is a function f : _E_ IN such that the
_→_
following two properties hold:

for all e _E, 0_ _f_ (e) _c(e), and_

_•_ _∈_ _≤_ _≤_
for all v _V, v_ = s, t,

_•_ _∈_ _̸_
� _f_ (u, v) = � _f_ (v, u)

_u∈V_ _u∈V_


(if (u, v) _E, we assume that c(u, v) = f_ (u, v) = 0).
_̸∈_

The total flow of f is defined to be

� _f_ (v, s) _f_ (s, v).

_−_
_v∈V_

The maximum flow problem is to find a flow f that has maximum total flow.
Algorithms for the maximum flow problem include the Ford-Fulkerson algorithm, the Dinic algorithm, and the Edmonds-Karp algorithm.

633. Let G = (V, E) be a DAG. Devise and analyze an efficient algorithm to find the smallest number of directed vertex-disjoint paths that cover
all vertices (that is, every vertex is on exactly one path).

634. Suppose we are given the maximum flow in a flow network G =
(V, E) with source s, sink t, and integer capacities. Suppose the capacity of a
single edge is increased by one. Give an O(n + e) algorithm for updating the
maximum flow, where G has n vertices and e edges.

635. Suppose we are given the maximum flow in a flow network G =
(V, E) with source s, sink t, and integer capacities. Suppose the capacity of a
single edge is decreased by one. Give an O(n + e) algorithm for updating the
maximum flow, where G has n vertices and e edges.

Consider a flow problem on a graph G = (V, E) with n vertices and e edges with all
capacities bounded above by a polynomial in n. For any given flow, let the largest
_edge flow be_
max
(u,v)∈E _[f]_ [(][u, v][)][.]

636. Show that two different maximum flows in G can have different largest
edge flows. Design an algorithm to find the minimum possible
largest edge flow over all maximum flows in G in time O(ne[2] log n).


-----

Sec. 13.5. Matrix Reductions **161**

Suppose we are given the maximum flow in a flow network G = (V, E) with source
_s, sink t, and integer capacities c(u, v) on each edge (u, v)_ _E. Suppose G has n_
_∈_
vertices and e edges. The following modified version of the standard Ford-Fulkerson
algorithm can be used to find a maximum flow in G.

**function max-flow-by-scaling(G, s, t)**
1. _c := max(u,v)∈E c(u, v)_
2. initialize flow f to zero
3. _k := 2[⌈][log][ c][⌉]_

4. **while k** 1 do
_≥_
5. **while there exists an augmenting path p of capacity** _k do_
_≥_
6. augment flow f along p
7. _k := k/2_
8. **return(f** )

637. Prove that max-flow-by-scaling returns a maximum flow.

638. Show that the residual capacity of a minimum cut of G is at most
2ke whenever line 4 is executed.

639. Prove that the inner while loop of lines 5–6 is executed O(e) times
for each value of k.

640. Conclude from the statements of Problems 638–639 that max-flowby-scaling can be implemented in time O(e[2] log c).

###### 13.5 MATRIX REDUCTIONS

Consider two problems A and B that have time complexities TA(n) and TB(n),
respectively. Problems A and B are said to be equivalent if TA(n) = Θ(TB(n)).
Some textbooks show that matrix multiplication is equivalent (under some extra
conditions) to matrix inversion. Here are some more problems along this line:

641. Show that multiplying two n _n matrices is equivalent to_
_×_
squaring an n _n matrix._
_×_

642. Show that multiplying two n _n matrices is equivalent to cubing_
_×_
an n _n matrix._
_×_

643. Show that multiplying two n _n matrices is equivalent to raising_
_×_
an n _n matrix to the fourth power._
_×_

644. Show that for all k 2, multiplying two n _n matrices is equivalent_
_≥_ _×_
to raising an n _n matrix to the kth power._
_×_


-----

**162** Chap. 13. Miscellaneous

645. Define the closure of an n × n matrix A to be _i=0_ _[A][i][, where][ A][0]_

[�][∞]

is the n _n identity matrix, and for k > 0, A[k]_ = A _A[k][−][1], where“_ ” denotes
_×_ _·_ _·_
matrix multiplication. (Note that closure is not defined for all matrices.) Show
that multiplying two n _n matrices is equivalent to computing the closure of_
_×_
an n _n matrix._
_×_

646. Show that multiplying two n _n matrices is equivalent to multiplying_
_×_
two n _n lower triangular matrices._
_×_

647. Show that multiplying two n _n matrices is equivalent to squaring_
_×_
an n _n lower triangular matrix._
_×_

648. Show that multiplying two n _n matrices is equivalent to cubing an_
_×_
_n_ _n lower triangular matrix._
_×_

649. Show that multiplying two n _n matrices is equivalent to raising an_
_×_
_n_ _n lower triangular matrix to the fourth power._
_×_

650. Show that for all k 2, multiplying two n _n matrices is equivalent_
_≥_ _×_
to raising an n _n lower triangular matrix to the kth power._
_×_

651. Show that multiplying n _n matrices is equivalent to computing the_
_×_
closure of an n _n lower triangular matrix. (See Problem 645 for the definition_
_×_
of matrix closure.)

###### 13.6 GENERAL

652. You are facing a high wall that stretches infinitely in both directions.
There is a door in the wall, but you don’t know how far away or in which
direction. It is pitch dark, but you have a very dim lighted candle that will
enable you to see the door when you are right next to it. Show that there
is an algorithm that enables you to find the door by walking at most O(n)
steps, where n is the number of steps that you would have taken if you knew
where the door is and walked directly to it. What is the constant multiple in
the big-O bound for your algorithm?

653. You are given an n 2 matrix of integers. You are allowed
_×_
to permute the rows of the matrix as monolithic items, and to perform comparisons on the elements of the matrix. Your task is to find an O(n log n)
time algorithm that permutes the rows so that neither column of the matrix contains an increasing subsequence (not necessarily contiguous) of length
exceeding _n_ .
_⌈[√]_ _⌉_

654. It’s Texas Chile Pepper day and you have a schedule of events that
looks something like this:


-----

Sec. 13.6. General **163**

8:30 – 9:15 Pepper Pancake Party
9:30 – 10:05 Pepper Eating Contest
9:50 – 11:20 Pepper Personality Profile
9:00 – 11:00 Pepper Parade
...

The schedule lists the times at which each event begins and ends. The events
may overlap. Naturally, you want to attend as many events as you can. Design
an efficient algorithm to find the largest set of nonoverlapping events. Prove
that your algorithm is correct. How fast is it?

655. Let A be an n _n matrix of zeros and ones._ A submatrix S of
_×_
_A is any group of contiguous entries that forms a square, more formally,_
_A[i, j]_ _ℓ_ _i_ _ℓ_ + k 1, m _j_ _m + k_ 1 for some 1 _ℓ, m_ _n, 0_
_{_ _|_ _≤_ _≤_ _−_ _≤_ _≤_ _−_ _}_ _≤_ _≤_ _≤_
_k_ min(n _ℓ_ + 1, n _m + 1). S is said to have size k. Design an algorithm_
_≤_ _−_ _−_
that determines the size of the largest submatrix of ones in A in time O(n[2]).

656. We wish to compute the laziest way to dial an n-digit number on a
standard push-button telephone using two fingers. We assume that the two
fingers start out on the and # keys, and that the effort required to move a
_∗_
finger from one button to another is proportional to the Euclidean distance
between them. Design and analyze an algorithm that computes in time O(n)
the method of dialing that involves moving your fingers the smallest amount
of total distance.

657. Suppose S = 1, 2, . . ., n and f : _S_ _S. If R_ _S, define f_ (R) =
_{_ _}_ _→_ _⊂_
_f_ (x) _x_ _R_ . Devise an O(n) time algorithm for determining the largest
_{_ _|_ _∈_ _}_
_R_ _S such that f_ (R) = R.
_⊂_

658. Let E be a set of m linear equations of the form xi = xj + cij over
the variables x1, . . ., xn (ci,j ∈ ZZ for all 1 ≤ _i, j ≤_ _n). Devise an O(m) time_
algorithm for determining whether the equations in E are consistent, that is,
whether an assignment of integers can be made to the variables so that all of
the equations in E are satisfied.

The following group of questions deals with the generalized version of the popular
Sam Loyd 15-puzzle, called the (n[2] 1)-puzzle. For definitions, see Problem 515.
_−_

659. Design an algorithm for the (n[2] 1)-puzzle that runs in time
_−_
_O(n[3]). Your algorithm must input a legal state of the puzzle and output a_
series of O(n[3]) moves that solves it.

660. Show that the worst case number of moves needed to solve the
(n[2] 1)-puzzle is at least n[3] _O(n[2])._
_−_ _−_


-----

**164** Chap. 13. Miscellaneous

661. Show that the average case number of moves needed to solve the
(n[2] 1)-puzzle is at least 2n[3]/3 _O(n[2])._
_−_ _−_

662. Show that for some constants 0 < α, β < 1, a random legal configuration of the (n[2] 1)-puzzle requires at least αn[3] moves to solve with
_−_
probability 1 1/e[−][βn][2] .
_−_

Suppose you are given a collection of gold coins that includes a clever counterfeit
(all the rest are genuine). The counterfeit coin is indistinguishable from the real
coins in all measurable characteristics except weight. You have a scale with which
you can compare the relative weight of coins. However, you do not know whether
the counterfeit coin is heavier or lighter than the real thing. Your problem is to find
the counterfeit coin and determine whether it is lighter or heavier than the rest.

663. Show that if there are 12 coins, the counterfeit coin can be
found in three weighings.

664. Show that if there are 39 coins, the counterfeit coin can be found in
four weighings.

665. Show that if there are n 3 coins, the counterfeit coin can be
_≥_
found in ⌈log3 2n⌉ weighings.

666. Show that if there are n ≥ 3 coins, at least ⌈log3 2n⌉ weighings are
needed to find the counterfeit coin.

Your job is to seat n rambunctious children in a theater with n balconies. You are
given a list of m statements of the form “i hates j.” If i hates j, then you do not
want to seat i above or in the same balcony as j, otherwise i will throw popcorn at
_j instead of watching the play._

667. Give an algorithm that assigns the balconies (or says that it is not
possible) in time O(m + n).

668. Design and analyze an algorithm for finding the minimum number of
balconies needed.

###### 13.7 HINTS

614. Show that if the search for two different elements x, y, where x < y, in the set
leads to the same leaf of the comparison tree, then the search for any element
_a of the universe with x < a < y must also lead to that leaf, which contradicts_
the correctness of the algorithm.


-----

Sec. 13.7. Hints **165**

627. Use both properties from Problem 626.

628. The cost of the path from v to u along c is _x._
_−_

629. Show that a min-cost path to any vertex on the minimum mean-cost cycle
can be extended along the cycle to the next vertex on the cycle.

633. Suppose V = {v1, . . ., vn}. Form a network G[′] = (V _[′], E[′]) as follows._

_V_ _[′]_ = _{s, t} ∪{x1, . . ., xn} ∪{y1, . . ., yn},_
_E[′]_ = _{(s, xi) | 1 ≤_ _i ≤_ _n} ∪{(yi, t) | 1 ≤_ _i ≤_ _n} ∪{(xi, yi) | (vi, vj) ∈_ _E}._

The capacity of all edges is one. Show that the minimum number of paths
that cover V in G is equal to n − _f_, where f is the maximum flow in G[′].

636. Consider the Edmonds-Karp algorithm for maximum flow.

641–645. Consider Problems 647–651. The lower triangular property can actually
make the problem easier, if you think about it for long enough. On the other
hand, there do exist nontriangular solutions, as the solution to Problem 641
given later demonstrates.

659. Use a combination of greedy and divide-and-conquer techniques. Suppose the
hole is immediately to the right of a square S. Let L, R, U, D denote moving
the hole one place left, right, up, and down, respectively. Then the sequence
of moves ULDLUR moves S one square diagonally up and to the right. Use
this sequence of moves, and others like it, to move each square to its correct
space, stopping when there is not enough space left to perform the maneuver.
Figure out how to finish it, and you’ve solved the problem! The best I can
do is 5n[3] Ω(n[2]) moves. Make sure that the configuration you come up with
_−_
is solvable. It can be shown that if the hole is in the lower right corner, the
solvable states of the puzzle are exactly those that can be made with an even
number of transpositions.

660. The Manhattan distance of a tile in square (i, k) that belongs in square (k, ℓ)
is defined to be _i_ _k_ + _j_ _ℓ_ . The Manhattan distance of a configuration
_|_ _−_ _|_ _|_ _−_ _|_
of the puzzle is defined to be the sum of the Manhattan distances of its tiles.
Show that the Manhattan distance is a lower bound on the number of moves
needed to solve the puzzle, and that there exists a configuration that has
Manhattan distance at least n[3] _O(n[2])._
_−_

661. Find a lower bound for the average Manhattan distance.

662. Find a lower bound for the Manhattan distance of a random configuration.
The best value that I can get for α is 16/243. You will need to use Chernoff
bounds. Let B(m, N, p) be the probability of obtaining at least m successes


-----

**166** Chap. 13. Miscellaneous

out of N Bernoulli trials, each with probability p of success. The following
result is a well-known consequence of the Chernoff bounds (see, for example,
Angluin and Valiant [5] and Valiant and Brebner [80]): Let β = m/Np 1.
_−_
If 0 _β_ 1, then β(m, N, p) _e[−][β][2][Np/][2]._
_≤_ _≤_ _≤_

663. Start by dividing the coins into three piles of four coins. Pick two piles and
compare their weights.

665. Start by solving Problems 663 and 664. Then generalize your solution.

###### 13.8 SOLUTIONS

641. The trick is to embed A and B into a larger matrix that, when squared, has
_AB has a submatrix. The solution can then be read off easily in optimal (that_
is, O(n[2])) time. There are many embeddings that work, including


� 0 _A_
_B_ 0


�2 � _AB_ 0
=
0 _AB_


�
_._


663. Actually, I’m not going to give you a solution. This problem is so popular
with mathematicians that you ought to be able to find one in the literature
somewhere. It even appears in a science fiction novel by Piers Anthony [6,
Chapter 16].

###### 13.9 COMMENTS

610. The nuts and bolts problem is from Rawlins [66].

611. This algorithm is mentioned in Alon et al. [4].

653. This problem was suggested to the author by Arny Rosenberg. Interestingly,
one can prove by a counting argument that one can so permute an n _k matrix,_
_×_
but an actual efficient algorithm is known only for k = 1, 2. For k = 1, this
is a relative of the Erd¨os-Szekeres Theorem, which states that there exists
in every sequence of n integers a monotonic subsequence (either ascending or
descending) of length _n_ (for more recent proofs of this theorem, see, for
_⌊[√]_ _⌋_
example, Dijkstra [22], and Seidenberg [73]).

659. Horden [36] gives an interesting history of this puzzle and its variants. See
also Gardner [27]. Early work on the 15-puzzle includes Johnson [38] and
Storey [76]. The minimum number of moves to solve each legal permutation
of the 8-puzzle has been found by exhaustive search by Schofield [69]. The
minimum number of moves needed to solve the 15-puzzle in the worst case
is unknown, but has been the subject of various papers in the AI literature,


-----

Sec. 13.9. Comments **167**

including Michie, Fleming and Oldfield [57] and Korf [48]. Ratner and Warmuth [65] have proved that the problem of determining the minimum length
number of moves for any given legal configuration of the (n[2] 1)-puzzle is
_−_
-complete, and they demonstrate an approximation algorithm that makes
_NP_
no more than a (fairly large) constant factor number of moves than necessary
for any given legal configuration. Kornhauser, Miller, and Spirakis [49] have
shown an algorithm for the (n[2] 1)-puzzle and its generalizations that always
_−_
runs in time O(n[3]).


-----

### Bibliography

[1] A. V. Aho, J. E. Hopcroft, and J. D. Ullman. The Design and Analysis of
_Computer Algorithms. Addison-Wesley, 1974._

[2] A. V. Aho, J. E. Hopcroft, and J. D. Ullman. Data Structures and Algorithms.
Addison-Wesley, 1983.

[3] A. V. Aho and J. D. Ullman. Foundations of Computer Science. Computer
Science Press, 1992.

[4] N. Alon, M. Blum, A. Fiat, S. Kannan, M. Naor, and R. Ostrovsky. Matching
nuts and bolts. In Proc. 5th Annual Symposium on Discrete Algorithms, pages
690–696, 1994.

[5] D. Angluin and L. Valiant. Fast probabilistic algorithms for Hamiltonian circuits and matchings. In Proceedings of the Ninth Annual ACM Symposium on
_Theory of Computing, pages 30–41. ACM Press, 1977._

[6] P. Anthony. With a Tangled Skein, volume 3 of Incarnations of Immortality.
Ballantine Books, 1985.

[7] S. Baase. Computer Algorithms: Introduction to Design and Analysis. AddisonWesley, 1978.

[8] W. W. Rouse Ball and H. S. M. Coxeter. Mathematical Recreations and Essays.
University of Toronto Press, 12th edition, 1974.

[9] J. Bentley. Programming Pearls. Addison-Wesley, 1986.

[10] J. Bentley. _More Programming Pearls: Confessions of a Coder._ AddisonWesley, 1988.

[11] B. Bernhardsson. Explicit solutions to the n-queens problem for all n. SIGART
_Bulletin, 2(2):7, 1991._

**168**


-----

Bibliography **169**

[12] A. Blum and R. L. Rivest. Training a 3-node neural network is NP-complete. In
_Neural Information Processing Systems 1, pages 494–501. Morgan Kaufmann,_
1989.

[13] A. Blum and R. L. Rivest. Training a 3-node neural network is NP-complete.
_Neural Networks, 5(1):117–127, 1992._

[14] G. Brassard and P. Bratley. Algorithmics: Theory and Practice. Prentice Hall,
1988.

[15] A. Conrad, T. Hindrichs, H. Morsy, and I. Wegener. Wie es dem springer
gelang, schachbretter beliebiger groesse und zwischen beliebig vorgegebenen anfangs- und endfeldern vollstaendig abzuschreiten. Spektrum der Wis_senschaft, pages 10–14, February 1992._

[16] A. Conrad, T. Hindrichs, H. Morsy, and I. Wegener. Solution of the knight’s
Hamiltonian path problem on chessboards. _Discrete Applied Mathematics,_
50:125–134, 1994.

[17] S. A. Cook. The complexity of theorem proving procedures. In Proceedings of
_the Third Annual ACM Symposium on Theory of Computing, pages 151–158._
ACM Press, 1971.

[18] D. Coppersmith and S. Winograd. Matrix multiplication via arithmetic progressions. Journal of Symbolic Computation, 9:251–280, 1990.

[19] T. H. Cormen, C. E. Leiserson, and R. L. Rivest. Introduction to Algorithms.
MIT Press, 1990.

[20] P. Cull and J. DeCurtins. Knight’s tour revisited. Fibonacci Quarterly, 16:276–
285, 1978.

[21] E. W. Dijkstra. A Discipline of Programming. Prentice Hall, 1976.

[22] E. W. Dijkstra. Some beautiful arguments using mathematical induction. Acta
_Informatica, 13:1–8, 1980._

[23] P. Eades and B. McKay. An algorithm for generating subsets of fixed size
with a strong minimal change property. Information Processing Letters, pages
131–133, 1984.

[24] L. Euler. Solution problematis ad geometriam situs pertinentis. Comentarii
_Academiae Scientarum Petropolitanae, 8:128–140, 1736._

[25] L. Euler. Solution d’une question curieuse qui ne paroit soumise `a aucune
analyse. Mem. Acad. Sci. Berlin, pages 310–337, 1759.

[26] S. Even. Graph Algorithms. Pitman, 1979.


-----

**170** Bibliography

[27] M. Gardner. The Mathematical Puzzles of Sam Loyd. Dover, 1959.

[28] M. R. Garey and D. S. Johnson. Computers and Intractability: A Guide to the
_Theory of NP-Completeness. W. H. Freeman, 1979._

[29] A. M. Gibbons. Algorithmic Graph Theory. Cambridge University Press, 1985.

[30] R. L. Graham, D. E. Knuth, and O. Patashnik. Concrete Mathematics: A
_Foundation for Computer Science. Addison-Wesley, 1989._

[31] R. L. Graham, B. L. Rothschild, and J. H. Spencer. Ramsey Theory. John
Wiley & Sons, 1990.

[32] R. L. Graham and J. H. Spencer. Ramsey theory. Scientific American, 263(1),
July 1990.

[33] D. H. Greene and D. E. Knuth. Mathematics for the Analysis of Algorithms.
Birkh¨auser, 1982.

[34] D. Harel. Algorithmics: The Spirit of Computing. Addison-Wesley, 1987.

[35] B. R. Heap. Permutations by interchanges. _Computer Journal, 6:293–294,_
1963.

[36] L. E. Horden. Sliding Piece Puzzles. Oxford University Press, 1986.

[37] E. Horowitz and S. Sahni. Fundamentals of Computer Algorithms. Computer
Science Press, 1978.

[38] W. A. Johnson. Notes on the 15 puzzle 1. American Journal of Mathematics,
2(4):397–399, 1879.

[39] J. S. Judd. Learning in networks is hard. In Proc. of the First International
_Conference on Neural Networks, pages 685–692. IEEE Computer Society Press,_
1987.

[40] J. S. Judd. _Neural Network Design and the Complexity of Learning._ PhD
thesis, University of Massachusetts, Amherst, MA, 1988.

[41] J. S. Judd. On the complexity of loading shallow neural networks. Journal of
_Complexity, 4:177–192, 1988._

[42] J. S. Judd. Neural Network Design and the Complexity of Learning. MIT Press,
1990.

[43] R. M. Karp. Reducibility among combinatorial problems. In R. E. Miller
and J. W. Thatcher, editors, Complexity of Computer Computations. Plenum
Press, New York, 1972.


-----

Bibliography **171**

[44] J. H. Kingston. Algorithms and Data Structures: Design, Correctness, Analy_sis. Addison-Wesley, 1990._

[45] D. E. Knuth. _Fundamental Algorithms, volume 1 of The Art of Computer_
_Programming. Addison-Wesley, second edition, 1973._

[46] D. E. Knuth. Sorting and Searching, volume 3 of The Art of Computer Pro_gramming. Addison-Wesley, 1973._

[47] D. E. Knuth. Seminumerical Algorithms, volume 2 of The Art of Computer
_Programming. Addison-Wesley, second edition, 1981._

[48] R. E. Korf. Depth-first iterative deepening: An optimal admissible tree search.
_Artificial Intelligence, 27(1):97–109, 1985._

[49] D. Kornhauser, G. Miller, and P. Spirakis. Coordinating pebble motion on
graphs, the diameter of permutation groups, and applications. In 25th An_nual Symposium on Foundations of Computer Science, pages 241–250. IEEE_
Computer Society Press, 1984.

[50] D. C. Kozen. The Design and Analysis of Algorithms. Springer-Verlag, 1992.

[51] C. W. H. Lam and L. H. Soicher. Three new combination algorithms with the
minimal change property. Communications of the ACM, 25(8), 1982.

[52] Lewis and Denenberg. Data Structures and Their Algorithms. Harper Collins,
1991.

[53] J.-H. Lin and J. S. Vitter. Complexity results on learning by neural nets.
_Machine Learning, 6:211–230, 1991._

[54] X.-M. Lu. Towers of Hanoi problem with arbitrary k 3 pegs. International
_≥_
_Journal of Computer Mathematics, 24:39–54, 1988._

[55] E. Lucas. R´ecr´eations Math´ematiques, volume 3. Gauthier-Villars, 1893.

[56] U. Manber. Introduction to Algorithms: A Creative Approach. Addison-Wesley,
1989.

[57] D. Michie, J. G. Fleming, and J. V. Oldfield. A comparison of heuristic, interactive, and unaided methods of solving a shortest-route problem. In D. Michie,
editor, Machine Intelligence 3, pages 245–255. American Elsevier, 1968.

[58] B. M. E. Moret and H. D. Shapiro. Design and Efficiency, volume 1 of Algo_rithms from P to NP. Benjamin/Cummings, 1991._

[59] C. H. Papadimitriou and K. Steiglitz. Combinatorial Optimization: Algorithms
_and Complexity. Prentice Hall, 1982._


-----

**172** Bibliography

[60] I. Parberry. On the computational complexity of optimal sorting network verification. In Proceedings of The Conference on Parallel Architectures and Lan_guages Europe, in Series Lecture Notes in Computer Science, volume 506, pages_
252–269. Springer-Verlag, 1991.

[61] I. Parberry. On the complexity of learning with a small number of nodes.
In Proc. 1992 International Joint Conference on Neural Networks, volume 3,
pages 893–898, 1992.

[62] I. Parberry. Algorithms for touring knights. Technical Report CRPDC-94-7,
Center for Research in Parallel and Distributed Computing, Dept. of Computer
Sciences, University of North Texas, May 1994.

[63] I. Parberry. Circuit Complexity and Neural Networks. MIT Press, 1994.

[64] P. W. Purdom Jr. and C. A. Brown. The Analysis of Algorithms. Holt, Rinehart, and Winston, 1985.

[65] D. Ratner and M. K. Warmuth. The (n[2] 1)-puzzle and related relocation
_−_
problems. Journal for Symbolic Computation, 10:11–137, 1990.

[66] G. Rawlins. Compared to What? An Introduction to the Analysis of Algorithms.
Computer Science Press, 1991.

[67] G. J. Rawlins. Compared to What?: An Introduction to the Analysis of Algo_rithms. Computer Science Press, 1992._

[68] T. J. Schaefer. The complexity of satisfiability problems. In Proceedings of
_the Tenth Annual ACM Symposium on Theory of Computing, pages 216–226._
ACM Press, 1978.

[69] P. D. A. Schofield. Complete solution of the eight puzzle. In N. L. Collins and
D. Michie, editors, Machine Intelligence 1, pages 125–133. American Elsevier,
1967.

[70] A. Sch¨onhage and V. Strassen. Schnelle multiplikation grosser zahlen. Com_puting, 7:281–292, 1971._

[71] A. J. Schwenk. Which rectangular chessboards have a knight’s tour? Mathe_matics Magazine, 64(5):325–332, 1991._

[72] R. Sedgewick. Algorithms. Addison-Wesley, 1983.

[73] A. Seidenberg. A simple proof of a theorem of Erd¨os and Szekeres. Journal of
_the London Mathematical Society, 34, 1959._

[74] J. D. Smith. Design and Analysis of Algorithms. PWS-Kent, 1989.

[75] D. Solow. How to Read and Do Proofs. Wiley, second edition edition, 1990.


-----

Bibliography **173**

[76] W. E. Storey. Notes on the 15 puzzle 2. American Journal of Mathematics,
2(4):399–404, 1879.

[77] R. Susic and J. Gu. A polynomial time algorithm for the n-queens problem.
_SIGART Bulletin, 1(3):7–11, 1990._

[78] Y. Takefuji. Neural Network Parallel Computing. Kluwer Academic Publishers,
1992.

[79] Y. Takefuji and K. C. Lee. Neural network computing for knight’s tour problems. Neurocomputing, 4(5):249–254, 1992.

[80] L. G. Valiant and G. J. Brebner. A scheme for fast parallel communication.
_SIAM Journal on Computing, 11(2):350–361, 1982._

[81] J. Veerasamy and I. Page. On the towers of Hanoi problem with multiple spare
pegs. International Journal of Computer Mathematics, 52:17–22, 1994.

[82] M. A. Weiss. Data Structures and Algorithm Analysis. Benjamin/Cummings,
1992.

[83] H. S. Wilf. Algorithms and Complexity. Prentice Hall, 1986.


-----

8-puzzle, 166
15-puzzle, 124, 163, 166
2–3 tree, 135, 141, 146
2-colorable, 79
2SAT, 148
3SAT, 150
balanced, see B3SAT
one-in-three, see O3SAT1, O3SAT2,
O3SAT3
parity, see parity 3SAT
strong, see strong 3SAT

accept, 151, 152
acyclic, 79, 81
addition, 47, 52, 59, 61–66, 69, 74, 81
adjacency
list, 82
matrix, 158
adversary, 157
airport, 103
all-pairs shortest-path, 91
_α-pseudomedian, see pseudomedian_
amortized
analysis, ix, 145
time, 142
ancestor, 145, 158
approximation algorithm, ix, 167
arbitrage, 97
architecture, 152
area, 25
areas, method of, see method of areas
arithmetic expression, 79
ascending, 80

**174**


### Index

assignment, 116, 120, 121, 123
operator, 3
satisfying, see satisfying assignment
truth, see truth assignment
average, 74, 77, 157, 158, 164, 165
AVL tree, 135, 140–141, 145, 146

B3SAT, 154
backtracking, 6, 116, 122–123, 126,
127, 133
balance, 135, 145
balanced one-in-three 3SAT, see B3SAT
balcony, 164
bank, 97
Bernoulli trial, 166
biconnected, 78
bin packing problem, 143–144
binary, 19, 24, 25, 152
comparison, 137
heap, 137
reflected Gray code, 133
search, 74–75, 85
tree, 90, 135, 138–140
string, 116, 118, 123
tree, 18, 135, 136, 138
binomial, 14
bolt, see nuts and bolts
Brahma, 86
breadth-first
search tree, 150
traversal, 136
bubblesort, 50, 55, 62, 64, 158


-----

Index **175**


capacity, 144, 160, 161, 165
ceiling, 10
Chernoff bound, 165, 166
chessboard, 12–14, 25, 26, 80, 82, 86,
124, 125
child, 18, 108, 135–138, 141, 142, 145,
146
Chomsky Normal Form, 92
circle, 18, 20
circuit, 152–153
cyclic, see cyclic circuit
city, 103, 126, 158
clause, 147, 148, 150, 153, 154
clique, 123, 124
problem, 123
closed knight’s tour, 12, 25, 80, 82, 86,
124, 133
closure, 162
coin, 19, 96, 98, 110, 111, 164, 166
coin-changing problem, 19, 96, 98, 110
color, 12, 14–18, 23, 26, 78, 79
colorable, 79
combination, 116, 120–121, 131
_Communications of the ACM, 5_
comparison-based algorithm, 68, 157–
158
complete binary tree, 18, 135
connected, 16, 18, 19, 26, 81, 102, 103,
106, 150
component, 78
dominating set, 150
context-free grammar, 92
continuous knapsack problem, 101–102
converge, 153
convex, 18
Cook reduction, 148–150
cost
max, see max cost
mean, see mean cost
min, see min-cost
counterfeit, 164
cycle, 16, 18, 20, 26, 103, 109, 153,
158, 159, 165
Eulerian, see Eulerian cycle


Hamiltonian, see Hamiltonian cycle
cyclic, 124
circuit, 153
shift, 118, 119

DAG, 79, 160
decision
problem, 147, 149, 152
tree, 157
degree, 16, 20, 26, 79, 81, 82, 110
out, see out-degree
delete, 82, 90, 96, 136, 137, 140, 141,
143, 144, 146
deletemax, 137
deletemin, 104, 107, 136–138, 140
dense, 101
density, 101
depth-first
search, 78–79
spanning tree, 78
descendant, 135, 146
dial, 163
Dijkstra’s algorithm, 102–103
dimension, 16, 17
Dinic algorithm, 160
directed spanning tree, 108
dirty, 137–139
disjunctive normal form, 148, 150
divide-and-conquer, x, 2, 6, 67–87, 92,
116, 122, 136, 165
division, 48, 61
DNF SAT, 148
dominating set, 127, 128, 131, 150
connected, see connected dominating set
double rotation, 140, 141
dynamic programming, x, 2, 6, 7, 87–
100, 115, 151

Edmonds-Karp algorithm, 160, 165
elementary operation, 59, 62, 64
Erd¨os-Szekeres Theorem, 166
Euclidean distance, 163


-----

**176** Index


Euler, Leonhard, 26, 133
Eulerian cycle, 16, 20, 26, 81
exhaustive search, x, 2, 116–134, 166
existential, 147
exponential, 87
time, x, 2
exponentiation, 49, 53, 61, 63

factorial, 49, 53, 61, 63
factorization, 154
feedback loop, 152
Fermat’s last theorem, 150
Fibonacci numbers, 14, 38, 51, 54, 58,
62, 64–66
first-fit heuristic, 143–144
floor, 10
flow, 7, 160
maximum, see maximum flow
Floyd’s Algorithm, 91–92
Ford-Fulkerson algorithm, 160, 161
forest, 79, 104, 108
spanning, see spanning forest

Gauss, 23, 24
geometry, ix, 18
grammar, see context-free grammar
graph, x, 5, 6, 16–18, 20, 26, 78, 79,
81, 82, 91, 92, 97, 102–104,
106–110, 123, 124, 126, 127,
131, 149, 150, 158, 160
Gray code, 19, 20, 133
greedy algorithm, x, 2, 6, 100–115,
165

halving, 136, 137
Hamiltonian
cycle, 16, 109, 127, 131, 149, 150
path, 16
Hanoi, see towers of Hanoi
heap, 135–138, 145
Heap’s algorithm, 119, 120, 132, 133
heapsort, 136, 137
height, 140, 141, 145, 146
heuristic, 133


first-fit, see first-fit heuristic
Hi-Q, 124–125
Horner’s rule, 51
horse, 15, 26
hypercube, 16–17

ice cream cart, 126
increment, 47, 52, 61, 63, 117, 146
independent set, 124
induced subgraph, 81, 123
induction, x, 1, 2, 8–27, 35, 38, 41–46,
51, 52, 57, 66, 82–85, 111,
130, 131, 136, 145, 146

_Journal of Algorithms, 5_

Karp
reduction, 148
Richard M., 148, 160, 165
knapsack problem, 89, 97, 99, 150–
151
continuous, see continuous knapsack problem
zero-one, see zero-one knapsack
problem
knight, 12
knight’s tour
closed, see closed knight’s tour
open, see open knight’s tour
Kruskal’s algorithm, 104, 106–108

language, 92, 100, 152
programming, see programming
language
string processing, see string processing language
level, 18, 135, 145
literal, 147, 148, 150, 153
loading, 152, 153, 155
longest ascending subsequence, 80, 93,
99
loop invariant, 46, 55–58
Loyd, Sam, 124, 163

Manhattan distance, 165


-----

Index **177**


marble, 122
matrix, 19, 87
adjacency, see adjacency matrix
inversion, 161
multiplication, 50, 62, 73–74, 161–
162
product, 19, 87, 88, 97
weighing, see weighing matrix
max cost spanning tree, 108
maximum
flow, 160–161, 165
subsequence sum, 80
MAXMIN, 67, 68
mean cost, 158
median, 75, 76, 136, 137, 156, 157
weighted, see weighted median
merge, 81
method of areas, 25
min-cost spanning tree, 102–108, 111
minimal-change, 117–121, 131–133
monom, 148

(n[2] 1)-puzzle, 124, 163, 164, 167
_−_
_n-queens problem, 125, 133–134_
neural network, 133
nonterminal symbol, 92, 99, 100
, 147, 149–152, 154, 155
_NP_
-complete, x, 3, 5, 7, 146–155
_NP_
nuts and bolts, 156–157, 166

O3SAT1, 153–155
O3SAT2, 153–154
O3SAT3, 153–155
one-in-three 3SAT, see O3SAT1, O3SAT2,
O3SAT3
one-processor scheduling problem, 110
open knight’s tour, 124
optimal, 86, 88, 93, 94, 98, 111, 118,
120, 122, 123, 132, 166
binary search tree, 90
tape-storage problem, 110
out-degree, 79, 127

, 147–152, 154, 155
_P_


parallel
algorithm, ix
heap, 137, 138
lines, 19
priority queue, 137
parent, 98, 108, 135, 137, 142, 145,
146
parenthesize, 38, 87, 97, 99
parity 3SAT, 148
Pascal, x, 3–5, 69, 134
path, 16, 18, 79, 91, 92, 97, 102, 103,
106, 140, 141, 146, 158–160,
165
compression, 142, 145
Hamiltonian, see Hamiltonian path
pattern-matching, 50, 62
peaceful queens problem, see n-queens
problem
perfect matching, 121, 122
permutation, 110, 113–116, 118–120,
123, 130–133, 158, 166
Pigeonhole Principle, 19
pivot, 75–77
polygon, 18
polynomial time, 147–152, 154
many-one reduction, 148
reducible, 147
Turing reduction, 148
polyomino, 130
popcorn, 164
postage stamp, 11–12, 22, 129
predecessor, 81
Prim’s algorithm, 103, 104, 106–108
prime, 154
priority, 144
queue, 103
parallel, see parallel priority queue
product rule, 36, 59
production, 92, 100
programming language, x
prune, 122, 123
pseudomedian, 75, 76

queen, 125


-----

**178** Index


quicksort, 55, 64, 66, 75–77, 85

Ramsey number, 124, 133
Ramsey’s Theorem, 124
recurrence relation, x, 1, 37–45, 62,
65–67, 70, 75, 76, 81, 95, 130,
145
recursion
tree, 122, 123
reflection, 130
Reimann hypothesis, 150
remaindering, 48, 61
repeated substitution, 41–45, 65
root, 17, 18, 35, 92, 98, 100, 136, 138,
140–142, 145, 146, 150
rooted tree, 17
rotation, 130
double, see double rotation
single, see single rotation

salesperson
traveling, see traveling salesperson
SAT, 147, 149
DNF, see DNF SAT
satisfiability problem, see SAT
satisfying assignment, 150, 151
savings certificate, 97
schedule, 110, 111, 162, 163
self-reducibility, 149–150
semigroup, 144
sentinel, 117
sibling, 137, 138
single rotation, 140, 141
single-source
longest-paths, 103
shortest-paths, 102
sink, 158, 160, 161
Smarandache function, 154
sort, 50, 55, 62, 64, 66, 75–77, 80, 81,
85, 101, 104, 136–138, 141,
156–158
source, 159–161
spanning


forest, 104, 108
tree, 18, 102
depth-first, see depth-first spanning tree
directed, see directed spanning
tree
max-cost, see max-cost spanning tree
min-cost, see min-cost spanning
tree
square-root, 74
stable configuration, 153
stamp, see postage stamp
Stirling’s approximation, 26, 157
Strassen’s algorithm, 73–74
string processing language, 93
strong 3SAT, 148
sum rule, 36, 59

task, 152
telephone, 163
terminal symbol, 92
Texas Chile Pepper Day, 162
tile, 12, 14, 124, 165
toll, 144
tournament, 16
towers of Hanoi, 77–78
travel agent, 103
traveling salesperson, 109, 149–150
treasury bond, 97
tree, 17–18, 26, 79, 98, 137, 141, 142,
145, 150, 158, 164
2-3, see 2-3 tree
AVL, see AVL tree
binary, see binary tree
complete, see complete binary
tree
decision, see decision tree
recursion, see recursion tree
spanning, see spanning tree
triangle, 19–21, 79
triconnected, 158
triomino, 12–14
truck, 158


-----

Index **179**

truth assignment, 148, 149, 152–154
Turing machine, 151

union-find, 135, 142, 145

vertex cover, 110

warehouse, 94, 95, 98
weighing matrix, 128
weighted median, 80

zero-one knapsack problem, 89


-----

###### Errata to “Problems on Algorithms”[∗]

 Ian Parberry[†]
 Department of Computer Sciences University of North Texas

 April 7, 1998

 This note contains corrections to Parberry [5]. An up-to-date copy of this document and other useful information can be found on the World-Wide Web (Parberry [7]). I welcome further errata and comments from readers — I prefer electronic mail, but if you must use more primitive modes of communication, full contact information can be found in [6].

 Then anyone who leaves behind him a written manual, and likewise anyone who receives it, in the belief that such writing will be clear and certain, must be ex- ceedingly simple-minded.

 — Plato, Phaedrus

 General Errata

 Apparently I couldn’t make up my mind whether the keyword “return” in my algorithms should be in bold face or Roman type. It appears in bold face in Chapters 5, 7–9, and 13; in Roman face in Chapters 5, 6, and 10. Out of 71 occurrences, 39 are in bold face.

 A foolish consistency is the hobgoblin of little minds.

 — Ralph Waldo Emerson

 Specific Errata

 Page 3, Line 1: The first comma should be a period. Page 6, Line 14: The second “but” should be deleted. Page 7, Last Paragraph: Wilf’s textbook is now out of print, and is very difficult to obtain in its original form. Fortunately, the author has made it generally available in postscript form from http://www.cis.upenn.edu/~wilf/index.html.

_∗Copyright c_ Ian Parberry. This Errata may be reproduced without fee provided that the copies are not
_⃝_
made for profit, and the full text, including the author information and this notice, are included.
_†Author’s address: Department of Computer Sciences, University of North Texas, P.O. Box 13886, Den-_
ton, TX 76203-6886, U.S.A. Electronic mail: ian@cs.unt.edu.

###### 1


-----

###### Page 10, Problem 22: That should be induction on n 2. If n = 0, the right side of ≥ inequality doesn’t make sense, and if n = 1 equality holds. Page 12, Problem 47: This problem does not have a comment associated with it; the
 should be deleted. Page 16, Line 10: In the set V, the first occurrence of v2 should be v1. Page 16, Problem 67: I intended the graph here to be undirected and with no self-loops, but this did not make it into the definition. I need to add to the definition of a graph at the start of Section 2.10 the extra property that V is an ordered set and for all (u, v) E, u < v. ∈ Page 20, Hint to Problem 37: The comma at the end of the second sentence should be a period. Page 21, Solution to Problem 8: The fourth line of the multiline equation should begin with “=”, not “ ”. − Page 22, Solution to Problem 37, Line 5: Change “all values up to n 1 cents” to “all − values from 8 to n 1 cents”. − Page 25, Comment to Problem 13, Line 6: Change “by Problem 1” to “by Problem 11”. Page 35, Solution to Problem 133: On line 4, the denominator of the fraction should be 6, not 2. Page 40, Problem 241: This problem should ask you to show that 2n 3 log n 1 − ⌊ ⌋− ≤ T (n) 2n log n 1. ≤ −⌊ ⌋− Page 40, Problem 242: That should be T (1) = 0, and T (n) = T ( n/2 )+T ( n/2 )+n 1 ⌈ ⌉ ⌊ ⌋ − (otherwise it is inconsistent with the answer given on p. 41); it is the number of comparisons used by mergesort. Page 45, Line 3: “skip it is” should read “skip it if”. Page 52, Problem 266: In Line 1 of the algorithm, the Roman “n” in the return statement should be an italic “n”. Page 52, Problem 269: In Line 2 of the algorithm, the final Roman “y” in the return statement should be an italic “y”.
�y0
###### Page 56, Hint to Problem 258: The loop invariant is xj = k=yj−1 [k][, for all][ j][ ≥] [1.] Page 56, Solution to Problem 250:

 Line 4: “line 8” should read “line 7”. Line 6: “lines 3–7” should read “lines 3–6”. Line 14: “line 6” should read “line 5”. Line 15: Delete the parenthetical comment “(see Problem 93)”. Line 17: “line 5” should read “line 4”. Line 15: Insert “(see Problem 93)” immediately before the period.

 Page 64, Hint to Problem 283: Insert a period after the problem number. Page 62, Problem 299: “line 3” should read “line 5”. Page 68, Problems 317–318: When I wrote Problem 317 I assumed that the standard recursive algorithm described at the start of Section 7.1 achieved this bound. But it doesn’t — it requires 5n/3 2 comparisons when n = 3 2[k]. To fix it, simply ensure − · that the sizes of the two recursive splits are not both odd. (Thanks to Mike Paterson for pointing all this out). Problem 317 should be rewritten, or a hint added to help

 2


-----

###### make this clearer. The algorithm of Problem 318 almost meets the required bound. It makes 2 more comparisons than necessary, and should be rewritten slightly to save them (hint: consider the second and third comparisons). Page 68, Problem 320: The second question is not worded very clearly. The algorithm could be called upon to solve duplicate subproblems at the first level of recursion, given suitable inputs (can you find one?), but I was looking for more. There comes a point before the bottom-most level of recursion at which the algorithm is obliged to solve duplicate sub-problems. This is also the key to the algorithm in Problems 328-330. Page 68, Problem 321: This problem has a comment, but is missing the . Page 68, Problem 322: The solution to this problem is a little bit more subtle than I first thought. It begins: “Break the n-bit number into n/m m-bit numbers.” The remainder of the analysis from that point is straightforward, but in that first step lies a small difficulty. It can be done by repeatedly shifting the large number to the right, removing single bits and reconstructing the pieces in m registers. One needs to keep two counters, one of which runs from 0 to m, and the other off which runs from 0 to n/m. Consider the second counter. A naive analysis would show that this requires O(n/m) increment operations, each of which takes O(log n log m) bit operations. However, one needs to − notice that the total is O(n/m) amortized time (see Problems 476, and 477). I need to increase the difficulty level of this problem and add a hint to this effect. √ Page 74, Problem 340: Change n to N . ⌈[√] ⌉ ⌈ ⌉
 Page 78, preamble to Section 7.7: Line 4 of the depth-first search algorithm should read “mark w used”. Page 79, Problem 366: This problem should be deleted. There is no known way to find triangles in time O(n + e), using depth-first search or otherwise. Of course, it can be solved in time O(ne). This problem could be replaced with the much easier one of finding a cycle (of any size) in a directed graph in time O(n). Page 80, Problem 371: The array A should contain integers, not natural numbers. Oth- erwise the problem is trivial. Page 82, Hint to Problem 361: Delete the second adjacent occurrence of the word “in”. Page 85, Solution to Problem 369: Perhaps this should be called a comment, not a solution. Page 87, Preamble to Section 8.1: In Line 6 of the algorithm, the Roman “m” should be replaced by an italic “m”. Page 88, Problem 384, Line 3: The second occurrence of “M2” should be “Mi+2”. Page 88, Problem 390, Line 3: “M2” should be “Mi+2”. Page 90, Preamble to Section 8.3, Lines 11–12: The operation “member” should be “search” (two occurrences). Page 91, Preamble to Section 8.4, Line 4: “all pairs shortest paths” should be “all- pairs shortest-paths”. Page 98, Problem 426: The function to be maximized should be:

 R[c1, ci1] · R[ci1, ci2] · · · R[cik−1, cik] · R[cik, c1].

 Page 99, Hint to Problem 415: The last three lines are wrong, and should be deleted. Page 106, Problem 447: The stated proposition is wrong! Here is a counterexample. The

 3


-----

###### problem should be changed to “prove or disprove”.

2

2 3

1 1

1 4

2

###### Page 107, Problem 449: The running time should be e log k. Page 107, Problem 450: The third line of the putative variant of Prim’s algorithm should have a period after the line number. Page 117, Line 3: “line 8” should read “line 7”. Page 119, Preamble to Problems 489, 490: The line numbering in procedure permute(i) is totally wrong. The lines should of course be numbered consecutively. Page 124, Problem 513, Line 4: The running time should be O(n8[n][2]) in line 4. One of the two consecutive instances of the word “for” in the last line should be deleted. Page 129, Problems 529, 530: Both of these problems should be flagged . A comment should also be added explaining that exhaustive search is unnecessary — the flight-assignment problem can be solved in polynomial time by reducing the problem to that of finding a maximum-weight matching. For a polynomial time algorithm for the latter, see, for example, Gabow [3], and Gabox and Tarjan [4]. Page 131, Hint to Problem 510: The series should read �∞i=1 [1][/i][! =][ e][ −] [1][ ≈] [1][.][718.] Page 131, Hints to Problems 517, 518: These hints are listed in the wrong order. Page 131, Hint to Problem 518: A note should be added that the reader should read ahead to p. 127 for the definition of dominating set. Either that, or Problem 518 should be moved after Problem 526. Page 131, Solution to Problem 487, Line 1: The sentence “Line 6 can be done in time O(n).” should be replaced by the observation that the work in all of the other lines can be done in time O(n). A comment should be made that the tail of “ + d(n 1)” − in the recurrence for T (n) is used because it makes the solution very simple. If the obvious “ + dn” is used, then the recurrence becomes very difficult to solve. Page 135, Preamble to Section 11.1: Heap operations have not been defined. A heap is a set S in which the following operations can be performed:

 insert(x) insert x into S, that is, S := S x ∪{ } findmin return the smallest value in S deletemin return and delete the smallest value in S

 Page 135, Problem 535: The should come after the . Page 136–137, Problem 543: This problem should be moved to Section 11.5. Page 137, Problem 544: This problem should ask for insert, deletemin, and deletemax in O(log n) time, and findmin and findmax in O(1) time. Page 138, Problem 550: Insert “is correct” after the word “algorithm”. Page 140, Line 3: Capitalize the word “the” at the start of the parenthetical comment.

 4


-----

###### Page 141, Preamble to Section 11.3, Line 1: Change the first occurrence of “in” to “is”. Page 142, Problem 562, Line 1: Insert “of” after the word “sequence”. Page 143, Problem 570: This problem has a hint and a comment, but lacks the appro- priate icons . Page 144, Problem 573: Change “as as” to “as” in line 2. Page 145, Hint to Problem 544: This hint is misleading, and should be deleted. (Less significantly, n/2 should be n/2 on lines 1 and 3). ⌈ ⌉ ⌊ ⌋ Page 145, Hint to Problem 570: Insert a period after the problem number. Page 150, Preamble to Section 12.3: “Riemann” is mis-spelled ‘Reimann” (also in the Index on p. 178). Fermat’s Last Theorem may have been proved recently. Page 155, Solutions: These aren’t really solutions, just bibliographic notes. Perhaps they should be moved to the Comments section. Page 155, Solutions to Problems 599–600: Change “this problem” to “these problems”. Page 157, Problem 620: This problem should be changed from finding the median to that of halving, which is dividing n values into two sets X, Y, of size n/2 and n/2, ⌈ ⌉ ⌊ ⌋ respectively, such that for all x X and y Y, x < y. A comment should be added ∈ ∈ explaining that this problem is merely practice in using decision trees, since there is a 3n/2 lower bound using the adversary method due to Blum et al. [2]. Page 164, Problem 665 This problem is much harder than I thought. An upper bound of ⌈log3 n⌉ +1 weighings is easy. A little more thought will get you ⌈log3 9n/4⌉ weighings. The best algorithm known to me uses ⌈log3 2n + 2⌉ weighings (see Aigner [1]). Page 171, references [46, 47]: For some reason BibTEX chose to list Knuth Vol. 3 before Vol. 2. Page 171, reference [52]: The authors’ initials are missing — H. R. Lewis and L. Denen- berg. Page 172, references [66, 67]: These appear to be the same book. The correct reference is [67]. Page 172, reference [75]: The second occurrence of the word “Edition” should be deleted.

 Acknowledgements

 The author is very grateful to the following individuals who helpfully pointed out many of the above errors in the manuscript: Timothy Dimacchia, Sally Goldman, Narciso Marti-Oliet, G. Allen Morris III, Paul Newell, Mike Paterson, Steven Skiena, Mike Talbert, Steve Tate, and Hung-Li Tseng.

 References

 [1] M. Aigner. Combinatorial Search. Wiley-Teubner, 1988.

 [2] M. Blum, R. L. Floyd, V. Pratt, R. L. Rivest, and R. E. Tarjan. Time bounds for selection. Journal of Computer and System Sciences, 7:448–461, 1973.

 5


-----

###### [3] H. N. Gabow. An efficient implementation of Edmond’s algorithm for maximum matching on graphs. Journal of the ACM, 23(2):221–234, 1976.

 [4] H. N. Gabow and R. E. Tarjan. Faster scaling algorithms for general graph-matching problems. Journal of the ACM, 38(4):815–853, 1991.

 [5] I. Parberry. Problems on Algorithms. Prentice Hall, 1995.

 [6] I. Parberry. Ian Parberry’s Home Page. A World-Wide Web Document with URL
```
  http://hercule.csci.unt.edu/ian, Created 1994.

 [7] I. Parberry. Problems on Algorithms. A World-Wide Web Document with URL
  http://hercule.csci.unt.edu/ian/books/poa.html, Created 1994.

 6

```

-----

#### Supplementary Problems

###### By Bill Gasarch


-----

###### Mathematical Induction

 1 Games

 1. Let A be any natural number. We define a sequence as an as follows: (1) a10 = A. (2) To obtain an, first write an−1 in base n − 1. Then let x be the number that is that string of symbols if it was in base n. Let an = x − 1. (EXAMPLE: if a20 = 1005 then I write 1005 in base 20 as 2T 5 = 2 20[2] + T 20 + 5 1 where T is the symbol for ten. So · · · x = 2 · (21)[2] + 10 · 21 + 5 · 1. So a21 = x − 1 = 1097 − 1 = 1096.) For which natural numbers A will the sequence go to infinity?

 2. Here is a game: there are n toothpicks on a table. There are two players, called player I and player II. Player I will go first. In each move the player whose turn it is will remove 1,2, or 3 toothpicks from the table. The player who removes the last toothpick wins. (Example game with n = 10: player I removes 3 (so there are 7 left), player II removes 2 (so there are 5 left), player I removes 2 (so there are 3 left), player II removes 3 (so there are 0 left, and Player II wins).) Player I has a FORCED WIN if there is a move he can make as his first move so that, NO MATTER WHAT PLAYER II does, player I can win the game. This is called a WINNING FIRST MOVE. Player II has a FORCED WIN if, whatever player I does for the first move, there is a move player II can make so that after that point, no matter what player I does, player II can win. Player II’s move is called a WINNING RESPONSE. (Example: if n = 4 then player II has a forced win: if (1) player I removes 1, player II removes 3, (2) if player I removes 2 then player II removes 2, (3) if player I removes 3 then player II removes 1. To specify a winning response you need to specify responses to all moves.)

 (a) Fill in the following sentence and justify: “Player I has a forced win iff X(n).”
 (b) Modify the game so that you can remove 1, 2, 3, 4, 5, 6, or 7 sticks. Fill in the following sentence and justify: “Player I has a forced win iff X(n).”
 (c) Let k N . Modify the game so that you can remove 1, 2, . . ., k ∈ − 1, or k sticks. Fill in the following sentence and justify: “Player I has a forced win iff X(n).”

 1


-----

###### (d) Let k N . Modify the game so that you can remove 1, 2, or 4 ∈ sticks. Fill in the following sentence and justify: “Player I has a forced win iff X(n).”
 (e) Let a1, . . ., ak ∈ N . Modify the game so that you can remove a1, . . ., ak sticks. Show that there exists A ∈ N and X ⊆{0, . . ., A− 1 such that, for all but a finite number of n N, if n sticks are } ∈ in the pile then Player I wins iff ( x X)[n x (mod A)]. ∃ ∈ ≡

 3. (a) Consider the following game played between FILLER and EMP- TYIER There is initially a box with a finite (nonempty) number of balls in it. Each ball has a natural number on it, called its rank. (There may be many balls of the same rank. For ex- ample, a box could have 100 balls of rank 1, 20000 of rank 2, and 4 of rank 1000.) In every round EMPTYIER makes the first move. EMPTYIER’s move consists of taking a ball from the box. FILLER then counters be replacing the ball with a finite number of balls of lower rank. (For example, he could re- place a ball of rank 1000 with 999999999999999 balls of rank 999, 888888888876234012 balls of rank 8, and 4 balls of rank 1.) EMP- TYIER wants the box to be empty eventually. FILLER wants the box to never be empty. Show that no matter what the initial box of balls has in it, EMPTYIER can win.

 (b) Consider the same game as above except that the balls are labeled with integers. Fill in the following sentence and prove it: “Player XXX can always win.”

 (c) Consider the same game as above except that the balls are labeled with positive rationals. Fill in the following sentence and prove it: “Player XXX can always win.”

 (d) Consider the same game as above except that the balls are labeled with ordered pairs of numbers, and we consider (a, b) to be of lower rank than (c, d) if either a < c or a = c and b < d. Fill in the following sentence and prove it: “Player XXX can always win.”

 (e) Fill in the following sentence and prove it: “If the game can be played with a set A with ordering such that the ordering ≤ has property XXX then the FILLER can win; however, if it has property NOT(XXX) then the EMPTYIER can win.”

 2


-----

###### 4. Consider the following game of “NIM”. There are two piles of stones of different sizes. Players alternate turns. At each turn a player may take as many stones as he or she likes from one (and only one) pile, but must take at least one stone. The goal is to take the last stone.

 The following is a winning strategy for the first player: Take stones from the larger pile so as to make the two piles have equal size. Prove that this really is a winning strategy using mathematical induction.

 5. Consider the following 2-player game. There are n sticks on the table. Player I can remove 1,2 or 3 sticks. Player II can remove 2,4, or 6 sticks. The player who removes the last stick WINS. Show that:

 if n 1 mod 2 then player I has a winning strategy. ̸≡

 2 Sequences, Summations, Products, and Recur- rences

 1. Consider the following sequence:

�
###### T (n) T (n 1) + 3 T (n 2) + 2n, T (0) = 0, T (1) = 1 . ≤ − −

 Show that T (n) 16n[2]. ≤

 2. Consider the following sequence:

 T (n) 3T (n 1) + 10, T (0) = 0 . ≤ −

 Find a constant c such that T (n) c[n]. ≤

 3. Consider the following sequence:
 T (n) T (n 2) + 5[√]n, T (0) = 0, T (1) = 1 . ≤ −

 Find a constant c such that T (n) cn[3][/][2]. (Hint: n 2 < n.) ≤ [√] − [√]

 4. Consider the following sequence:

 A(n) A( n/3 ) + A( n/5 ) + 2n, T (0) = 0 . ≤ ⌊ ⌋ ⌊ ⌋

 Find a constant c such that A(n) cn. ≤

 5. Let P (n) be a statement about an INTEGER n. Assume that the following two statements are known:

 3


-----

###### (a) P (10).

 (b) ( k)[P (k) P (k 2)]. ∀ → −

 For which integers n do we know that P (n) is true?

 6. Let an be defined as follows:

 a0 = 6 a1 = 21 a2 = 11 an = 3an−1 + an−3 + 10n + 2

 7. Show that (∀n ∈ N )[an ≡ 1 mod 5].
 8. Prove ( n Z)[n[4] + 1 0 (mod 5) n 0 (mod 5)]. ∀ ∈ ≡ → ≡

 9. Find a number a such that the following is true:

 ( n N, n a)[n[2] + 5n + 6 < 2[n]]. ∀ ∈ ≥

 Prove your claim by induction.

 10. Let P (n) be some property of the natural number n (e.g. P (n) could be ‘2[17][n] 10 (mod 8)’). Assume that P (10) and P (11) are known ≡ to be true. Assume that

 ( n 5)[P (n 1) P (n + 1)] ∀ ≥ − →

 is known. For which n can we conclude P (n) is true? Briefly explain.
 11. Define the sequence an by a0 = 1 and an = [�]i[n]=0[−][1] [a][i][. Find a function] f (n) such that (∀n)[an ≤ f (n)]. Prove your result.
 12. Let an be defined as below. Show that (∀n ≥ 1)[an ≡ 0 (mod 3)].

 a0 = 3 a1 = 6 (∀n ≥ 3)[an = (an−1 + an−2)[2] + 6n]

 13. Let P (n) be some property of the natural numbers. Assume that the following are known (1) For all primes q, P (q) is true, and (2) ( n )[P (n) P (n[2])]. For which n can we conclude P (n) is ∀ ∈N → ∈N true? Express your answer clearly. No explanation is needed.

 4


-----

###### 14. Let P (z) be some property of the integers. Assume that the following are known

 (a) P ( 23). −
 (b) ( z Z)[P (z) P (z + 3)]. ∀ ∈ →

 For which z can we conclude P (z) is true? (Express your answer clearly!) No justification required.

 15. Let a0 = 9, a1 = 4, a2 = 100, a3 = 64, and
 (∀n ≥ 4) �an = 25an−1a⌊log n⌋].�

 Let SQ = n N ( x N )[n = x[2]] . (That is, SQ is the set of all { ∈ | ∃ ∈ } squares.) Show that (∀n ≥ 0)[an ∈ SQ].
 16. A sequence b0, b1, . . . is INCREASING if (∀x)(∀y)[x < y → bx < by]. Let an be defined as follows: a0 = 10, a1 = 12, a2 = 13, a3 = 14, a4 = 15, a5 = 16, and

 (∀n ≥ 2) [an = an−1 + an−3 − an−5] .

 17. Describe the set of all a N such that the following is true: ∈
 (n[2] + 3n + a 0 (mod 5)) (n 0 (mod 5)). ≡ → ≡

 (No justification required.)
 18. Let S(n) = [�]i[n]=1 [i][(][i][ + 1). Find][ a, b][ such that][ S][(][n][) =][ an][3][ +][ bn][. Prove] that your answer is correct by induction.

 19. Define a sequence via a1 = 4 and
 (∀n ≥ 2)[an = a[2]n−1[]][.]

 Show that (∀n ≥ 1)[an ≤ 4 · 3[(3][n][)]].

 20. Let a0 = 4, a1 = 49, a2 = 104, and
 (∀n ≥ 3) �an = (a⌊ [n]2 [⌋][)][3][ +][ a][⌊√][n][⌋] [+ 11]� .
 Show that (∀n ≥ 0)[an ≡ 4 (mod 5)].

 5


-----

###### 21. Let P (q) be some property of the rational q. Assume that the following are known

 (a) P (1).
 (b) (∀q ∈ Q)[P (q) → P ( 2[q] [)].]

 Let A be the set of all q such that we can conclude P (q) is true. Write down the set A clearly but DO NOT use the notation “. . .” No justification required.

 22. Let a0 = 10, a1 = 90, and

 (∀n ≥ 2)[an = 5an−1 + 20an−2].

 Find POSITIVE constants A, B, C N, such that ∈
 (∀n ≥ 0)[A · (C − 1)[n] ≤ an ≤ B · C [n]].

 No justification required (but show work for partial credit).

 23. Let T (n) = 2T (n − 1) + T ( [n]2 [) +][ n][. Prove what you can about this]
 recurrence.

 24. Let T (n) ≤ T ( [3]4 [n][) +][ T] [(] [1]4 [n][) + 4][n][. Find a value of][ d][ such that for all]
 n, T (n) dn log n. ≤

 25. Let T (n) T (an) + T (bn) + cn. For what values of a, b and c is it ≤ possible to find a d such that for all n, T (n) dn log n. ≤

 26. Consider the following recurrence. Initial conditions T (0) = 0, T (1) = 5. T (n) = 7T (n 1) 12T (n 2). Solve the recurrence exactly. Then − − − express the answer more simply using O-notation.

 27. Prove by induction that if T is a tree then T is 2-colorable.

 28. Let T (n) be defined by T (1) = 10 and

 T (n) = T (n log n) + n. −

 Find a simple function f such that T (n) = Θ(f (n)). NO PROOF REQUIRED.

 29. Use mathematical induction to show that

 6


-----

###### (a)

 (b)


_n_
� _i(i + 1) =_ _[n][(][n][ + 1)(][n][ + 2)]_

###### 3

_i=1_


_n_
� _i2[i][−][1]_ = (n 1)2[n] 1

###### − −
_i=0_

###### 30. Assume every node of a tree with n nodes has either 0 or 3 children. How many leaves does the tree have? Prove your answer.

 31. Simplify the following summation:


_n_
�

_i=1_


_n_
�

_j=i_


_n−j_
� 1

_k=1_


###### 32. Simplify the following summation:


_n_
�

_i=1_


_n_
�

_j=n−i_


2j
� 1

_k=j_


###### 33. Consider the following code fragment.
```
    for i = 1 to n do
      for j = i to 2*i do
        for k = n-j+1 to n do
          output ‘foobar’

 a. Let T (n) denote the number of times ‘foobar’ is printed as a func- tion of n. Express T (n) as a summation (actually three nested summations).

 b. Give a closed-form solution for T (n) (i.e. no summations) by sim- plifying your summation. Show your work.

 34. a. Assume that Christmas has n days. Exactly how many presents did my “true love” send me? [If you do not understand this question, you should do some research.]

 7

```

-----

###### b. Using part (a), exactly how many presents did my “true love” send during the twelve days of Christmas?
 35. Evaluate the sum [�]k[∞]=0[(3][k][ −] [1)][x][3][k][ for 0][ < x <][ 1.]
 36. Evaluate [�]k[n]=1 [4][ ·][ 3][k]
 37. Consider the following code fragment.
```
    for i=1 to n do
      for j=i to 2*i do
        output ‘foobar’

 Let T (n) denote the number of times ‘foobar’ is printed as a function of n.

 a. Express T (n) as a summation (actually two nested summations).

 b. Simplify the summation. Show your work.

 38. Consider the following code fragment.
    for i=1 to n step 2 do
      for j=1 to i do
        output ‘foobar’

 Let T (n) denote the number of times ‘foobar’ is printed as a function of n. Express T (n) as two nested summations. Be careful your “formula” works for n both even and odd. Do not simplify the summation.

 39. Consider the following code fragment.
    for i=1 to n/2 do
      for j=i to n-i do
        for k=1 to j do
          output ‘foobar’

 Assume n is even. Let T (n) denote the number of times ‘foobar’ is printed as a function of n.

 (a) Express T (n) as three nested summations.

 (b) Simplify the summation. Show your work.

 8

```

-----

###### 40. Given an m n array of (positive and negative) numbers, find the × largest sum of values in a (contiguous) rectangle.

 a. Write down an English description of the “brute force” algorithm for the “maximum contiguous rectangle problem”. One or two sentences should suffice.

 b. Write down the “brute force” algorithm in pseudocode.

 c. How many times is the inner loop executed? Write it using sum- mations.

 d. Simplify your answer. Justify your work. [If you do this right, the solution involves very little calculation.]

 e. Find a better algorithm for the “maximum contiguous rectangle problem”. How well can you do?
 41. Approximate k=1 [k][3][ using integrals. Make sure to get an upper and]

[�][n]
###### lower bound.
 42. Approximate [�]k[n]=1 3k4−2


###### 43. Use integrals to give upper and lower bounds for [�]k[∞]=1 k[3]1[/][2][ .]
 √ 44. Appoximate j=0 j using an integral.

[�][n]

###### 45. Consider the following code fragment.
```
    for i=1 to n do

 for j=1 to lg i do ⌈ ⌉
        print ‘foobar’

 Let T (n) denote the number of times ‘foobar’ is printed as a function of n.

 (a) Express T (n) exactly as two nested summations.
 (b) Simplify down to one summation.
 (c) Give good upper and lower bounds for T (n).

 46. Find the solution for the recurrence relation

 T (n) = T (n c) + k −

 where both c and k are integer constants, n is a natural number, and T (x) is 0 if x is a negative integer.

 9

```

-----

###### 47. Solve the recurrence

� _T_ (n 2) + n _n > 1_
###### T (n) = − 0 otherwise

 assuming n is even. Show your calculations.

 48. Solve the recurrence T (n) = T (n 1) + 2n 1 (T (0) = 0) exactly. − − Justify your answer.

 49. Solve the recurrence T (n) = T (n 1) + 3n 2 (T (0) = 0) exactly. − − Justify your answer.

 50. Solve the recurrence

� _T_ (n/3) + 2 _n > 1_
###### T (n) = 0 otherwise

 assuming n is a power of 3. Show your calculations.

 51. Solve the recurrence T (n) = 4T (n/3) + 2n 1 (T (0) = 0) exactly. − Assume n is a power of 3. Justify your answer.

 52. Solve the recurrence T (n) = 3T (n/4) + 2n 1 (T (0) = 0) exactly. − Assume n is a power of 4. Justify your answer.

 53. Solve the recurrence

� _T_ (n/5) + 2 _n > 1_
###### T (n) = 3 otherwise

 assuming n is a power of 5. Show your calculations.

 54. Solve the recurrence T (n) = 5T (n/2) + 2n 1 (T (1) = 7) exactly. − Assume n is a power of 2. Justify your answer.

 55. Consider the following recurrence, defined for n a power of 5:


###### T (n) =


� 19 if n = 1
###### 3T (n/5) + n 4 otherwise −


###### a. Solve the recurrence exactly using the iteration method. Simplify as much as possible.

 b. Use mathematical induction to verify your solution.

 10


-----

###### 56. Consider the following recurrence, defined for n a power of 5:


###### T (n) =


� 7 if n = 1
###### 4T (n/5) + 2n 3 otherwise −


###### a. Solve the recurrence exactly using the iteration method. Simplify as much as possible.

 b. Use mathematical induction to verify your solution.

 57. Obtain exact solutions to the following two recurrences.

 a. T (n) = 5T (n/3) + 2n (T (1) = 7). Assume n is a power of 3.

 b. T (n) = 2T (n/6) + 5n (T (1) = 7). Assume n is a power of 6.

 58. Obtain exact solutions to the following two recurrences.

 a. T (n) = 4T (n/3) + 2n (T (0) = 0).

 b. T (n) = 3T (n/4) + 2n (T (0) = 0).

 59. Obtain exact solutions to the following two recurrences.

 a. Let n be a power of 2.


###### T (n) =


� 4 if n = 1
###### 5T (n/2) + 3n[2] otherwise


###### b. Let n be a power of 4.


###### T (n) =


� 3 if n = 1
###### 2T (n/4) + 4n otherwise


###### 60. Obtain exact solutions to the following two recurrences.

 (a) Let n be a power of 2.


###### T (n) =


� 3 if n = 1
###### 7T (n/2) + 4n[2] + 1 otherwise


###### (b) Let n be a power of 4.


###### T (n) =


� 4 if n = 1
###### 3T (n/4) + 5n 2 otherwise −

 11


-----

###### 61. Consider the following recurrence.


###### T (n) =


� 0 if n = 0
###### T ( n/2 ) + T ( n/4 ) + 3n otherwise ⌊ ⌋ ⌊ ⌋


###### Find a constant c such that T (n) cn. Try to make c as small as ≤ possible.

 62. Consider the following recurrence.


###### T (n) =


� 0 if n = 1
###### T ( 2n/3 ) + T ( n/6 ) + 5n otherwise ⌊ ⌋ ⌊ ⌋


###### Use constructive induction to find a constant c such that T (n) cn. ≤

 63. (a) Let r1, r2, . . ., rk be a list of positive fractions, i.e. 0 < ri < 1, such that i=1 [r][i] [<][ 1. Let][ a >][ 0 be a constant. Let]

[�][k]


###### T (n) ≤


_k_
� _T_ (⌊rin⌋) + an.

_i=1_


###### Show that T (n) is linear, i.e. T (n) cn for some constant c. ≤ What can you say about c?
 (b) What if i=1 [r][i] [= 1? What if][ �][k]i=1 [r][i] [>][ 1?]

[�][k]


###### 64. Let


###### T (n) =


� 2T (n/2) + 2 lg n if n > 1
###### 0 if n = 1


###### a. Use constructive induction to show that T (n) = an + b lg n + c. Find constants a, b, and c.

 b. Solve the recurrence using the iteration method.

 65. An S0 tree is a single node. An Si tree, i > 0, is created by taking two Si−1 trees and making the root of one a child of the root of the other. (These are the trees that create the largest height for as few nodes as possible for the UNION-FIND algorithm with balancing.)

 (a) Draw S0, S1, S2, and S3. You may also want to draw S4 for yourself.

 12


-----

###### (b) The nodes on level i are all nodes distance i from the root. Tree Sk will have nodes on levels 0, . . ., k (and thus have k + 1 levels). For S3, how many nodes are on levels 0, 1, 2, and 3.
 (c) Make a conjecture for how many nodes are on level i of Sk. (You may also want to look at S4.)
 (d) Prove your conjecture.

 66. Consider an F -tree created as follows. An F0-tree is a single node. An Fn+1-tree is created by taking two Fn-trees and making the root of one the two trees the child of the other tree. Here are the first few F -trees.

 a. How many nodes are there in an Fn tree. Justify your answer.
 b. Recall that the depth of a node is its distance from the root (so the root has depth 0, its children have level 1, etc.). Write down a recurrence for how many nodes there are at depth d in Fn? Note that there are two parameters.

 c. Guess a solution to your recurrence (by looking a few trees).

 d. Prove that your guess is correct using mathematical induction on your recurrence.

 13


-----

###### Floors and Ceilings

 1. Let r be a real number. Determine all real numbers ϵ such that the following statement is true: r + ϵ = r . ⌊ ⌋ ⌈ ⌉
 2. For which positive reals x does x + [1] ⌊ 6 [⌋] [=][ ⌊][x][ +][ 1]2 [⌋][?]


###### 3. Find a number x such that ( x )[2] < x[2] . ⌊ ⌋ ⌊ ⌋

 4. For which x is 4x = 4 x ? ⌈ ⌉ ⌈ ⌉
 5. For which real numbers x does the following hold: x + [1] ⌊ 3 [⌋] [=][ ⌊][x][ +][ 1]2 [⌊][.]

 6. For which real numbers x does x satisfy the following two conditions: (a) 1 < x < 2, and (b) x = x[2] . (HINT: Express x as 1 + ϵ where ⌊ ⌋[2] ⌊ ⌋ 0 < ϵ < 1.)

 14


-----

###### Combinatorics

 1. For this problem we express numbers in base 10. The last digit of a number is the rightmost digit of the number (e.g., the last digit of 39489 is 9). Find the largest x N such that the following statements ∈ is true:

 If A N and A = 59 then there are at least x numbers in A that ⊆ | | have the same last digit.

 2. Every Sunday Bill makes lunches for Carolyn. Lunch consists of a sandwich, a fruit, and a desert. Sandwich is either ham and cheese, peanut butter and jelly, egg salad, or tuna fish. Fruit is either an apple, an orange, or a coconut. Desert is either pretzels, a brownie, or an apple pie.

 (a) How many different lunchs can Bill make for Carolyn ?

 (b) If Carolyn does not like to have egg salad with apple pie, or tuna fish with an apple, then how many lunches can Bill make for Carolyn.

 (c) Why does Bill call Carolyn his ‘gnilrad’ ?

 3. Can you place 24 rooks on an 8 by 8 chessboard so that if you remove all but 4 then there will always be 2 that attack each other? How about 25?

 4. Let f be the function that takes a number x = dndn−1 · · · d0 (these are the digits of x base 10) to the sum of the 2001 powers of the digits (e.g., f (327) = 3[2001] + 2[2001] + 7[2001]). Show that, for any x, the set f (x), f (f (x)), f (f (f (x))), . . . is finite. { }

 5. Assume that there are at most 200 countries in the world. Assume that there are 900 people in a room. Find a number x such that the statement a is TRUE and statement b is FALSE. Briefly explain WHY statement a is TRUE and WHY statement b is FALSE.

 (a) There must exist x people in the room that are from the same country.
 (b) There must exist x +1 people in the room that are from the same country.

 15


-----

###### Probability

 1. Let r be a random number taking on the values 1, . . ., n, with proba- bility

 _n12_ 1n ≤ _i ≤_ _[n]4_

###### P (r = i) =

_n_ 4 _[< i][ ≤]_ _[n]2_

 21n _n2_ _[< i][ ≤]_ _[n]_

###### For the algorithm below perform an average case analysis.

 if (r n/4) then perform 10 operations ≤
 else

 if (r > n/4 and r n/2) then perform 20 operations ≤
 else

 if (r > n/2 and r 3n/4) then perform 30 operations ≤
 else perform n operations

 Perform an average case cost analysis of this algorithm.

 2. You are given a deck of fifty two cards which have printed on them a pair of symbols: an integer between 1 and 13, followed by one of the letters “S,” “H,” “D,” or “C,” There are 4 13 = 52 such possible × combinations, and you may assume that you have one of each type, handed to you face down.

 (a) Suppose the cards are randomly distributed and you turn them over one at a time. What is the average cost (i.e. number of cards turned over) of finding the card [11,H]?

 (b) Suppose you know that the first thirteen cards have one of the letters “H” or “D” on them, but otherwise all cards are randomly distributed. Now what is the average cost of finding [11,H]?

 3. Let P be a program that has the following behavior:

 (a) The only inputs are 1, 2, . . ., n, n is large, and n is divisible by { } 2.
 (b) If the input i is one of 1, 2, . . ., [n] { 2 [}][ then][ P][ takes][ i][4][ steps.]
 (c) If the input i is one of { [n]2 [+ 1][, . . ., n][}][ then][ P][ takes 2][i][ steps]


###### 16


-----

###### Find a distribution on the inputs such that every input has a nonzero probability of occurring and the expected running time is θ(n[17]).

 4. Suppose we have one loaded die and one fair die, where the probabil- ities for the loaded die are

 P (1) = P (2) = P (5) = P (6) = 1/6, P (3) = 1/7, P (4) = 4/21.

 (a) What is the probability that a toss of these two dice produces a sum of either seven or eleven?

 (b) What is the expected value of the sum of the values of the dice?

 (c) the product of the values of the dice?

 5. Let a be a random number taking on the values 1, . . ., n, with proba- bility 1/2 that it is contained in (n/3, 2n/3], and probability 1/4 that it is contained in either [1, n/3] or (2n/3, n]. Consider an algorithm that has the following behavior:

 if (a n/3) then perform i operations ≤
 else
 if (a > n/3 and a ≤ 2n/3) then perform log3 n operations
 else
 perform n[2] operations

 Perform an average case cost analysis of this algorithm.

 6. Given n numbers in a sorted list, we know that in general, the worst case cost for linear search is n, and its average cost is is (n + 1)/2, whereas the worst and average case costs for binary search are log2 n and (log2 n)/2. Suppose instead that we have a special situation where the probability that the item we are seeking is first in the list is p, and the probability that it in position i, 2 i n, is (1 p)/(n 1). For ≤ ≤ − − what values of p are we better off using linear search, in the sense that the average cost for linear search is higher than that for binary search?

 7. Let P be a program that has the following behavior:

 (a) The only inputs are 1, 2, . . ., n, n is large, and n is divisible by { } 3.
 (b) If the input is one of {1, 2, . . ., [n]3 [}][ then][ P][ takes log][ n][ steps.]

 17


-----

###### (c) If the input is one of { [n]3 [+ 1][, . . .,][ 2]3[n]

 [}][ then][ P][ takes][ n][ steps]
 (d) If the input is one of { [2]3[n] [+ 1][, . . ., n][}][ then][ P][ takes 2][n][ steps]

 Find a probability distribution on the inputs such that every input has a nonzero probability of occurring, but the expected time is θ(n).

 8. Let A[1..n] be a sorted list. We are pondering writing a program that will, given a number x, see if it is on the list. Suppose that we have a special situation where the probability that the item we are seeking is first in the list is p, and the probability that it is in the second position in the list is p, and the probability that it in position i, 3 i n, ≤ ≤ is (1 2p)/(n 2). For what values of p will the average case for − − linear search do better than log n? (Obtain an inequality involving p, without summations, but do not simplify it.)

 9. Consider the following experiments. For each of them find the expected value and the variance.

 (a) Roll a 6-sided die and a 4-sided die. Add the two values together. Both dice are fair.

 (b) Roll a 2-sided die and a 3-sided die. Multiply the two values together. Both dice are fair.

 (c) Roll a 3 sided die and another 3-sided die. Add the two values together. The first die has probability p1 of being 1, p2 of being 2, and p3 of being 3. The second die is fair. (In this case E and V will be in terms of p1, p2, and p3.)

 10. Let a be a random number taking on the values 1, . . ., n, with proba- bility 1/2 that it is contained in (n/3, 2n/3], and probability 1/4 that it is contained in [1, n/3], and probability 1/4 that it is in (2n/3, n]. Consider an algorithm that has the following behavior:

 if (a n/3) then perform a log a operations ≤


###### else if (a > n/3 and a ≤ 2n/3) then perform log3 n operations
 else perform n[2] operations

 Perform an average case cost analysis of this algorithm. The final answer can be in Θ notation.

 18


-----

###### 11. Given n (n > 10) numbers in a sorted list, we know that in general, the worst case cost for linear search is n, and its average cost is (n + 1)/2, whereas the average case for binary search is (roughly) log n (its actually (log n) c for some constant c). Suppose instead that we have − a special situation where the probability that the ith item is sought is pi, and (1) for i ≤ 10 we have pi = p, and (2) for i > 10 we have the probability that it is in position i is pi = [1]n[−]−[10]10[p] [. What is the average]
 case cost of linear search with this probability distribution (the answer will be in terms of p). For this problem do NOT use Θ-notation, you will need to look at exact results. Using a calculator find values of n > 10 and p < 1 such that linear search performs better than log n average case.

 12. We are going to pick a number from 1, . . ., n There are constants { } p1, p2, . . ., and a quantity A(n), such that the probability of picking i is pi = A(n)i. What is A(n)?

 13. Let n be a large number. Assume we pick numbers from the set 1, . . ., n, and after we get a number we square it. (Formally the { } sample space is 1, . . ., n and the random variable is X(a) = a[2].) { } Find a probability distribution such that E(X) = θ(log n).

 14. Let P be a program that has the following behavior:

 (a) The only inputs are 1, 2, . . ., n, n is large. { }
 (b) If the input i is log n then P takes 2[i] steps ≤
 (c) If the input i is such that log n < i ≤ [n]2 [then][ P][ takes][ n][2][ steps]
 (d) If the input i is such that i > [n]2 [then][ P][ takes][ n][3][ steps.]


###### Answer the following questions.

 (a) What is the expected run time if the distribution is uniform? You may use Θ-notation.
 (b) Find a distribution where the expected time is Θ(n[2]). (In this distribution all elements must occur with non-zero probability.)

 15. Let S = 1, 2, . . ., n . We are going to pick a number i out of S { } with the following probability distribution. Prob(i) = A(n) (where

_i[2]_
###### A(n) is some function of n). Once we have this number i we compute X(i) = i[3][.][2]. (a) Show A(n) = O(1). (b) Find E(X)? (Use Θ notation.)

 19


-----

###### 16. Let n be a large number. Let f be a function. Assume we pick numbers from the set 1, . . ., n, and after we get a number we apply { } f to the result. (Formally the sample space is 1, . . ., n and the { } random variable is X(i) = f (i).)

 (a) What is the expected value if f (i) = i[2] and the distribution is uniform? (Use Θ notation.)

 (b) Let a, b be reals such that 1 < a << b (a is much less than b). Assume that f (i) = i[b]. Show that there exists a distribution such that E(X) = Θ(n[a]). (There are several valid solutions to this problem, some of which do not use the assumption 1 < a << b and some of which do.)

 17. You play a game of throwing two six sided dice (with integer values 1, . . ., 6). You lose a dollar if the two dice have different values. You win d dollars if the two dice land on the same value d (i.e. you throw double d’s).

 a. What is the expected value of playing this game once.

 b. What is the variance of playing this game once.

 c. What is the standard deviation of playing this game once.

 d. What is the expected value of playing this game n times.
 e. What is the variance of playing this game once n times.

 f. What is the standard deviation of playing this game once n times.

 18. Consider an s-sided die, where the sides are marked with the numbers 1, 2, . . ., s, and each side has equal probability (1/s) of being rolled.

 (a) What is the expected value of one roll of this die.

 (b) What is the expected value of the sum of n (independent) rolls of this die.

 (c) What is the variance and standard deviation of one roll of this die.

 (d) What is the variance and standard deviation of the sum of n (independent) rolls of this die.

 (e) What is the probability of two rolls of this die summing to an integer t (2 t 2s)? (Give your answer as a function of s and ≤ ≤ t.)

 20


-----

###### (f) What is the probability of two rolls of this die both being s given that you know that at least one of the two rolls was an s. (Note: The roll that was an s is NOT necessarily the first roll.)

 19. A combination lock works by turning to the right three times and stopping a on particular integer from 1 to 60 (inclusive), turning to the left two times and stopping on a particular integer from 1 to 60, and then turning to the right and stopping on a final integer from 1 to 60. How many possible combinations are there.

 20. Assume a lock has C combinations. A thief tries a combination ran- domly. If it does not work he again tries a combination randomly, which may (or may not) be the same as the first. He keeps doing this until he finally opens the lock. On average, how many times will he try the lock?

 21. Professor Pascal wakes up in the morning. He remembers that either he has six blue socks and four red socks in the drawer or he has four blue socks and six red socks in the drawer, but he cannot remember which (assume each is equally likely). He pulls two socks randomly out of the drawer. It turns out that they are both blue. What is the probability that initially there were more blue socks.

 22. A coin is tossed n times, each time with an independent probability p of coming up heads and 1 p of coming up tails. Let H be the number − of heads occurring. What is

 (a) E[H], the expected number of heads?

 (b) V [H], the variance of H?

 (c) the standard deviation of H?

 (d) the probability that H > 2?

 Show your calculations.

 23. Consider a three-side die where a 1 has probability p of being rolled, a 2 has probability q of being rolled, and a 3 has probability r = 1 p q − − of being rolled.

 (a) Assume you roll the dice once.

 a. What is the expected value?

 21


-----

###### b. What is the variance? c. What is the standard deviation?

 (b) Assume n independent such dice are rolled and their values are summed.

 a. What is the expected value? b. What is the variance? c. What is the standard deviation?

 Show your calculations.

 24. Assume every child born has probability 1/2 of being a boy or a girl. Assume that (even within a family) children’s sexes are independent.

 (a) Mr. Jones has two children. The older one is a boy. What is the probability that they are both boys? Why?

 (b) Mr. Smith has two children. At least one is a boy. What is the probability that they are both boys? Why?

 (c) Mr. Johnson has three children. At least one is a boy. What is the probability that at least one is a girl? Why?

 22


-----

###### Asympototics

 1. For each of the following expressions f (n) find a simple g(n) such that f (n) = Θ(g(n)).

 (a) f (n) = [�]i[n]=1 1i [.]
 (b) f (n) = [�]i[n]=1[⌈] [1]i

 [⌉][.] (c) f (n) = [�]i[n]=1 [log][ i][.] (d) f (n) = log(n!).


###### 2. Place the following functions into increasing asymptotic order.
 f1(n) = n[2] log2 n, f2(n) = n(log2 n)[2], f3(n) = [�]i[n]=0 [2][i][,][ f][4][(][n][) =] log2([�][n]i=0 [2][i][).]

 3. Let a, b be real numbers such that a 0 and Let 0 b 1. ≥ ≤ ≤

 (a) Let a ≥ 0. Find a function fa that does not involve summations such that [�]i[n]=0 [a][i][ =][ θ][(][f][a][(][n][)). (The function][ f][a] [might involve sev-] eral cases and might depend on a.) (b) Let b ≥ 0. Find a function gb that does not involve summations such that [�]i[n]=1 [i][b][ =][ θ][(][g][b][(][n][)). (The function][ g][b] [might involve sev-] eral cases and might depend on b.) (c) For what values of a and b does fa(n) = O(gb(n)). (Only consider the cases where 0 a, b.) ≤

 4. Place the following functions into increasing asymptotic order. If two or more of the functions are of the same asymptotic order then indicate this.
 √ f1(n3) = [�]i[n]=1 i, f2(n) = ([√]n) log n, f3(n) = n[√]log n, f4(n) =
 12n 2 + 4n,

 5. Let k be an integer such that k 1. Find the constant A such that ≥ the following holds. [�]i[n]=1 [i][k][ =][ An][k][+1][ +][ O][(][n][k][). Prove your result.]

 6. Let a, b, c be real numbers such that a, b, c 10. Consider the recur- ≥ rence T (n) = aT ( [n]

_b_ [) +][ n][c][. You are given the option of either reducing]
###### a, b, or c by 1. You want to make T (n) as small as possible. For which values of a, b, c are you better off reducing a? For which values of a, b, c are you better off reducing b? For which values of a, b, c are you better off reducing c?

 23


-----

###### 7. Let a, b be real numbers such that a, b > 0. Consider the recurrence T (n) = T ( [n]

_a_ [)+] _[T]_ [(] _[n]b_ [)+] _[n][. Specify an infinite number of values for (][a, b][)]_

###### such that T (n) = Θ(n).

 8. Let a, b, c be numbers such that 0 a, b < 1, and c > 0. Let T (n) be ≤ defined by T (2) = 4 and T (n) = T (an) + T (bn) + cn.

 (a) Show that if a + b < 1 then T (n) is bounded by a linear function.

 (b) Show that if a + b = 1 then T (n) is bounded by O(n log n).

 (c) Does there exist a d such that, for all a, b, c as above, T (n) = O(n[d])? (Recall that O-notation just means that n[d] is an upper bound on T (n).)

 9. Let c > 0. Let T be the function defined by


###### T (0) = 1 T (n) = 81T ( [n]

3 [) +][ c][n]

###### Find a function g(n) such that T (n) = Θ(g(n)). (The function g may involve several cases depending on what c is. The cases should be clearly and easily specified.)
 10. (a) For what values of a, b does the following hold? [�]i[n]=0 ib[a][i][ =][ O][(1).]

_n_
###### (b) For which constants a is it the case that 3 2 + 2[n] = O(a[n])?
 11. (a) Find a function f such that [�]i[n]=1 [i][ log][ i][ = Θ(][f] [(][n][)).]
 √ (b) Find a simple function f such that [�]i[n]=1 i log i = Θ(f (n)). Ex- plain your answer.

 12. For each of the following expressions f (n) find a simple g(n) such that f (n) = Θ(g(n)). (You should be able to prove your result by exhibiting the relevant parameters, but this is not required for the hw.)

 (a) f (n) = [�]i[n]=1 [3][i][4][ + 2][i][3][ −] [19][i][ + 20.]
 (b) f (n) = [�]i[n]=1 [3(4][i][) + 2(3][i][)][ −] [i][19][ + 20.]
 (c) f (n) = [�]i[n]=1 [5][i][ + 3][2][i][.]


###### 13. Which of the following are true?
 (a) [�]i[n]=1 [3][i][ = Θ(3][n][−][1][).]

 24


-----

###### (b) [�]i[n]=1 [3][i][ = Θ(3][n][).]
 (c) [�]i[n]=1 [3][i][ = Θ(3][n][+1][).]
 14. Show that [�]i[∞]=0 4i[5]3i [=][ O][(1).]


###### 15. Let a, b be real numbers such that 0 a 1 and Let b 0. ≤ ≤ ≥

 (a) Find a function fa that does not involve summations such that
�ni=1 _[i][−][a][ = Θ(][f][a][(][n][)).]_ (The function fa might involve several
###### cases and might depend on a.)
 (b) Find a function gb that does not involve summations such that
�n
_i=0_ _[b][i][ = Θ(][g][b][(][n][)).]_

###### (c) For what values of a and b does fa(n) = O(gb(n))? (Only consider the cases where 0 a 1, and b 0.) ≤ ≤ ≥
 (d) For what values of a and b does gb(n) = O(fa(n))? (Only consider the cases where 0 a 1, and b 0.) ≤ ≤ ≥

 16. Let a, b be real numbers such a > 0 and b > 1. Consider the recurrence T (n) = aT ( [n]b [) +][ n][. You are given the option of either reducing][ a][ or][ b]
 by 1. You want to make T (n) as small as possible. For which values of a, b would reducing a by 1 reduce T (n)? For which values of a, b would reducing b by 1 reduce T (n)?

 17. Let a, b be real numbers such that a, b > 0. Consider the recurrence T (1) = 10, T (n) = T ( [n]a [) +][ T] [(] [n]b [) +][ n][. Specify an infinite number of]
 values for (a, b) such that T (n) = Θ(n).
 18. Let T (1) = 10 and T (n) = T ([√]n) + n. Show that T (n) = O(n).

 19. Let a, b be real numbers such that 100 a 100 and b > 0. − ≤ ≤

 (a) Find a function fa that does not involve summations such that
�ni=02 _[i][7][a][ = Θ(][f][a][(][n][)).]_ (The function fa might involve several
###### cases and might depend on a. Each case should be simple.)
 (b) Find a function gb that does not involve summations such that
�[√]n
_i=1_ _[b][12][i][ = Θ(][g][b][(][n][)).]_ (The function gb might involve several
###### cases and might depend on b. Each case should be simple.)

 20. For each of the following functions f find a simple function g such that f (n) = Θ(g(n)).

 25


-----

###### (a) f1(n) = (1000)2[n] + 4[n].
 (b) f2(n) = n + n log n + [√]n.
 (c) f3(n) = log(n[20]) + (log n)[10].
 (d) f4(n) = (0.99)[n] + n[100].

 21. Let c, d be real numbers such that c, d 0. Consider the recurrence ≥
 T (n) = 49T ( [n]
 7 [) +][ n][c][d][n][.]

 Find a function gc,d such that T (n) = Θ(gc,d). (The function gc,d might involve several cases and might depend on c and d. Each case should be simple.)

 22. Let a, b be real numbers such that a > 0 and 100 b 100. − ≤ ≤

 23. (a) Find a function fa that does not involve summations such that
�ni=12 _[a][7][i][ = Θ(][f][a][(][n][)).]_ (The function fa might involve several
###### cases and might depend on a. Each case should be simple.)
 (b) Find a function gb that does not involve summations such that
�ni=0 _[i][5][b][ = Θ(][g][b][(][n][)). (The function][ g][b]_ [might involve several cases]
###### and might depend on b. Each case should be simple.)
 (c) For what values of a and b does fa(n) = O(gb(n))? (Only consider the cases a > 0 and 100 b 100.) − ≤ ≤
 (d) For what values of a and b does fa(n) = Ω(gb(n))? (Only consider the cases a > 0 and 100 b 100.) − ≤ ≤

 24. Let a, b be any real numbers Let T be the function defined by


###### T (n) =


_n_
�

###### i[a](log n)[b].
_i=1_


###### Find a function ga,b(n) such that T (n) = Θ(g(n)). The function ga,b should be as simple as possible. (The function ga,b may involve several cases depending on what a, b is. The cases should be clearly and easily specified. NO PROOF REQUIRED.)

 25. For each pair of expressions (A, B) below, indicate whether A is O, o, Ω, ω, or Θ of B. Note that zero, one or more of these relations may hold for a given pair; list all correct ones.

 26


-----

###### A B (a) n[100] 2[n]
 √ (b) (lg n)[12] n √ (c) n n[cos(][πn/][8)]
 (d) 10[n] 100[n]
 (e) n[lg][ n] (lg n)[n]
 (f ) lg (n!) n lg n


###### 27


-----

###### Graph Problems

 1. Let Kn denote the complete graph with n vertices (i.e. each pair of vertices contains one edge between them), and let Kn[′] [denote the] modification of Kn in which one edge is removed.

 (a) When does Kn[′] [have an Euler path?]
 (b) When does Kn[′] [have a Hamiltonian cycle?]
 (c) What is the mininum number of colors needed for a proper col- oring of Kn[′] [?]

 2. Prove that in any (undirected) graph, the number of vertices of odd degree is even.

 3. Find a number a, 0 < a < 1 such that the following statement is true “If G is a planar graph on n vertices then at least an vertices have degree 99.” ≤

 4. Let n1, n2 be natural numbers such that n1 3 and n2 3. Let ≥ ≥ C(n1, n2) be the graph that is formed by taking Cn1, the cycle graph on n1 vertices, and Cn2, the cycle graph on n2 vertices, and connecting ALL the vertices of of Cn1 to ALL the vertices of Cn2.

 (a) For which values of (n1, n2) does C(n1, n2) have an Eulerian cy- cle?

 (b) For which values of (n1, n2) does C(n1, n2) have a Hamiltonian path?

 (c) For which values of (n1, n2) is C(n1, n2) 5-colorable but not 4- colorable?

 5. Let be a class of graphs with the following properties: (1) If G A ∈A and H is a subgraph of G, then H . (2) If G then G has a ∈A ∈A vertex of degree 10. Show that every graph in is 10-colorable. ≤ A

 6. Prove rigorously that if a graph has three vertices of degree 1, then that graph does not have a Hamiltonian path.

 7. For each of the following combinations of properties either exhibit a connected graph on 10 vertices that exhibits these properties, or show that no such graph can exist.

 28


-----

###### (a) Eulerian but not Hamiltonian.

 (b) Hamiltonian but not Eulerian.

 (c) Hamiltonian and 2-colorable.

 8. Consider the following real world problem: Given n cities you want to build a highway system such that, for any two cities x and y, there is a way to go from x to y that only passes through at most one other city. You want to minimize the number of roads you build. STATE this problem rigorously as a problem in graph theory.

 9. For every n, find the maximal number of edges that a graph with n vertices can have and still be unconnected.

 10. Show that if G is a planar graph then at least half the vertices have degree 10. ≤

 11. Give an example of a planar graph with an Eulerian path that has 2 vertices of degree 5.

 12. A graph is almost-planar if there exists a vertex v it such that if you remove that vertex then the graph is planar. Show that every almost- planar graph is 5-colorable (you may assume that every planar graph is 4-colorable).

 13. Let Wn be the ‘wheel graph’ (pictured below). Formally it has vertices 1, 2, . . ., n, n + 1 and edge set is the union of the sets { }
 (1, 2), (2, 3), . . ., (n 2, n 1), (n 1, n), (n, 1) { − − − }
 and

 (1, n + 1), (2, n + 1), . . ., (n, n + 1) . { }
 We only consider n 3. ≥

 (a) For which values of n is Wn 2-colorable?
 (b) For which values of n is Wn 3-colorable but not 2-colorable?
 (c) For which values of n is Wn 4-colorable but not 3-colorable?
 (d) For which values of n is Wn 5-colorable but not 4-colorable?

 14. Find a number c such that the following is true:

 29


-----

###### If G is a connected planar graph then at least at least [3]

4 _[of the vertices]_
###### have to have degree less than c.

 You must prove that your answer is correct. You may assume that the number of vertices in G is divisible by 4.

 15. For n, m ∈ N let Kn,m be the complete bipartite graph on n, m vertices (i.e., the left set has n vertices, the right set has m vertices, and for every left vertex a and right vertex b there is an edge between a and b).

 (a) Draw K1,3 and K3,4.
 (b) For what values of n, m does Kn,m have a cycle that includes every vertex exactly once.

 (c) For what values of n, m does Kn,m have a path that includes every vertex exactly once.

 16. For any graphs G and H the graph G H is formed by placing an ⊕ edge between EVERY vertex of G and EVERY vertex of H. Let n ≥ 3. Let Cn = (V, E) be the cycle graph (i.e., V = {1, . . ., n} and E = (1, 2), . . ., (n 1, n), (n, 1) .) { − }

 (a) Find all values of n, m such that Cn Cm 4-colorable but not ⊕ 3-colorable.

 (b) Find all values of n, m such that Cn Cm 5-colorable but not ⊕ 4-colorable.

 (c) Find all values of n, m such that Cn Cm 6-colorable but not ⊕ 5-colorable.
 17. Show that if a graph on n vertices has n[√]n edges then it must have ≥ a vertex of degree log n. (You may assume that n is large.) ≥

 18. Let G be a bipartite graph with m nodes on the left side and n nodes on the right side. What is the maximum number of edges G can have? What is the maximum number of edges G can have and still be disconnected?

 19. Define a notion of a k-partite graph. Phrase questions about k-partite graphs similar to those in the last questions.

 30


-----

###### 20. The courses 150, 251, 451, and 650 must be taught. Bill can teach 150 or 650. Clyde can teach 150 or 451. Diane can teach 451 or 650. Edna can teach 150 or 251.

 (a) Model this scenario with a graph.

 (b) Find all possible schedules that assign teachers to classes so that all four classes are taught and every teacher teaches just one class.

 21. Let T be a weighted tree. Let f be some function that is easily com- puted (it goes from Naturals to Naturals). An f -minimal spanning tree is a spanning tree where the weights are w1, ..., wm and [�]i[m]=1 [f] [(][w][i][) is] minimal among all spanning trees. Give an efficient algorithm to find the f -minimal spanning tree of a weighted tree.

 22. Let G = (V, E) be a directed graph.

 (a) Assuming that G is represented by an adjacency matrix A[1..n, 1..n], give a Θ(n[2])-time algorithm to compute the adjacency list repre- sentation of G. (Represent the addition of an element v to a list l using pseudocode by l l v .) ← ∪{ }
 (b) Assuming that G is represented by an adjacency list Adj[1..n], give a Θ(n[2])-time algorithm to compute the adjacency matrix of G.

 (c) Is there a reasonable assumption you can make to get the run time of part b down to O( E )? | |

 23. If we take a complete undirected graph (a graph that has n vertices, and edges between all pairs of vertices) and direct all the edges in some arbitrary manner, we obtain a graph called a tournament. (Think of n players playing a game, in which every two players play against each other, and the edge is directed towards the winner.) A directed Hamilton path in G, is a directed path that includes every vertex of G exactly once. Prove that every tournament has a Hamilton path. (Hint: Try Induction.)

 24. Prove that in a graph G = (V, E), the number of vertices that have odd degree are even. (Hint: First show that [�]v∈V [deg][(][v][) = 2][m][ where] m is the number of edges in G.)

 31


-----

###### 25. Describe concisely and accurately a linear-time algorithm for solving the single-source shortest paths problem in a weighted DAG. Give a rigorous, concise proof that your algorithm is correct.

 Hints: Topological sort; relaxation lemma; try your alg. on examples.

 26. Using depth first search, outline an algorithm that determines whether the edges of a connected, undirected graph can be directed to produce a strongly connected directed graph. If so, the algorithm outputs such an orientation of the edges. (Hint: Show that this can be done if and only if removing an edge leaves a connected graph.)

 27. An Euler Circuit for an undirected graph is a path which starts and ends at the same vertex and uses each edge exactly once.

 (a) Prove that a connected, undirected graph has an Euler circuit if and only if every vertex has even degree.

 (a) Give an O( V + E ) algorithm to find an Euler circuit if one | | | | exists.

 28. A bipartite graph is one whose vertex set can be partitioned into two sets A and B, such that each edge in the graph goes between a vertex in A and a vertex in B. (No edges between nodes in the same set are allowed.)

 Give an O( E + V ) algorithm that takes an input graph (represented | | | | in adjacency list form) and decides if the graph is bipartite. If the graph is bipartite, the algorithm should also produce the bipartition.

 (Hint: use BFS.)

 29. Consider the following problem: There is a set of movies M1, M2, . . ., Mk. There is also a set of customers, with each one indicating the two movies they would like to see this weekend. (Assume that customer i specifies a subset Si of the two movies that he/she would like to see. Movies are shown on saturday evening and sunday evening. Multiple movies may be screened at the same time.)

 You need to decide which movies should be televised on saturday, and which movies should be televised on sunday, so that every customer gets to see the two movies they desire. The question is: is there a schedule so that each movie is shown at most once? Design an efficient algorithm to find such a schedule if one exists?

 32


-----

###### (One naive solution would be to show all movies on both days, so that each customer can see one desired movie on each day. We would need k channels if k is the number of movies in this solution – hence if there is a solution in which each movie is shown at most once, we would like to find it.)

 30. Consider a rooted DAG (directed, acyclic graph with a vertex – the root – that has a path to all other vertices). Give a linear time (O( V + | | E )) algorithm to find the length of the longest simple path from the | | root to each of the other vertices. (The length of a path is the number of edges on it.)

 31. The diameter of a tree T = (V, E) is given by

 max
_u,v∈V_ _[δ][(][u, v][)]_

###### (where δ(u, v) is the number of edges on the path from u to v). De- scribe an efficient algorithm to compute the diameter of a tree, and show the correctness and analyze the running time of your algorithm.

 Hint: Use BFS or DFS.

 32. Show that the vertices of any n-vertex binary tree can be partitioned into two disconnected sets A and B by removing a single edge such that A and B are at most 3n/4. Give a simple example where this | | | | bound is met.

 33. Let G = (V, E) be an undirected graph. Give an O(n + e)-time algo- rithm to compute a path in G that traverses each edge in E exactly once in each direction.

 item Suppose you are given a set of tasks T, where task t takes time D[t] from start to finish. Tasks may be performed simultaneously, with the constraint that for each task t there is a set of tasks P [t] which must be completed before task t is begun.
 Let R = [�]t∈T [|][P] [[][t][]][|][.] Describe (give pseudo-code for) an O(|T | + R)-time, DFS-based algorithm which, given D and P, computes the minimum amount of time needed to complete all the tasks, or returns if it is not possible to meet the constraints. ∞
 Hint: work bottom-up.

 33


-----

###### 34. a Show that if (u, v) is the lightest edge on a cut, there exists a MST containing (u, v).

 b Show that if (u, v) is the heaviest edge on a cycle, there exists a MST not containing (u, v).

 35. A pseudo-tree in an undirected graph is a connected subgraph that is either a tree or a tree plus a single edge (so that it contains ex- actly one simple cycle). A pseudo-forest in is a collection of vertex- disjoint pseudo-trees. Describe and analyze a fast algorithm for finding a pseudo-forest of maximum total edge weight in an undirected graph with non-negative edge weights.

 FACT: There are algorithms for this problem that run a least as fast as the fastest known spanning tree algorithms.

 36. Let G = (V, E) be a directed graph. The reversal of G is a graph G[R] = (V, E[R]) where the directions of the edges have been reversed (i.e. E[R] = (i, j) (j, i) E ). { | ∈ }

 (a) Assuming that G is represented by an adjacency matrix A[1..n, 1..n], give an O(n[2])-time algorithm to compute the adjacency matrix A[R] for G[R].

 (b) Assuming that G is represented by an adjacency list Adj[1..n], give an O(n + e)-time algorithm to compute an adjacency list representation of G[R].

 37. Show that the vertices of any n-vertex binary tree can be partitioned into two disconnected sets A and B by removing a single edge such that A and B are at most 3n/4. Give a simple example where this | | | | bound is met.

 34


-----

###### Data Structures

 1. Let p1, . . ., pn be n points in the plane, with both coordinates in the set 1, 2, . . ., N . Devise an O(n[2]) data structure for them such that { } the following type of query can be answered in O(1) steps: given a rectangle, how many or p1, . . ., pn are in the rectangle.

 2. Recall that a heap allows inserts and deletes in O(log n) steps, and FINDMAX in O(1) steps. Devise a structure that allows inserts and deletes in O(log n) steps and both FINDMAX and FINDMIN in O(1) steps.

 3. Devise an (n log n) algorithm for the following problem: Given n points in the plane, find the pair with the shortest distance between them. (Hint: Sort the points on the x-coordinate and then store in some cleverly chosen data structure.)

 4. Let S be a set of n orthogonal lines in the plane (lines parallel to either the x-axis or y-axis). Devise a Data Structure for the following such that the following query will be easy: Given an orthogonal line (not in S), which of the n lines in S does it intersect?”

 5. Let S be a set of N intervals I1, . . ., IN which have endpoints in 1, 2, . . . n . Assume every interval in S has a natural number associ- { } ated to it. Devise a data structure such that the following operation are O(log n).
 (a) Given k, what is [�]k∈Ij∈S [(element associated to][ I][j][).]
 (b) Update by changing the value associated to an interval.

 6. Let S = {p1, . . ., pn} be n points in the plane. Devise a Data Structure for S such that the following operations can be carried out quickly

 (a) a) which pair of points is closest together,

 (b) b) insert a point,

 (c) c) delete a point.

 7. Let S = {p1, . . ., pn} be n points in the plane. Assume they all have x- coordinate in the set 1, 2, . . ., N . Devise a Data Structure to answer { } the following type of query: Given x0, x1 ∈{1, 2, . . ., N } and y0 a natural number, find {(x, y) | x0 ≤ x ≤ x1, y ≤ y0} ∩ S. The data

 35


-----

###### structure should take up no more than O(N +n) space, and each query should take O(k + log log n).

 8. Let S = {w1, . . ., wk} where the wi are (very long) strings. Devise a data structure that will support the following operations.

 (a) FIND:Σ[+] Σ[+]. FIND(w) returns the longest prefix of w that → is a subword of some wi.
 (b) FREQ:Σ[+] N. FREQ(w) returns how often w occurs as a sub- → word of any wi.
 (c) LOC:Σ[+] 2[N][×][N]. LOC(w) returns the places w occurs, e.g. if → the output is {(1, 3), (1, 7), (4, 5)} then there is a w in w1 starting in the 3[rd] position, a w in w1 starting in the 7[th] position, and a w in w4 starting in the 5[th] position.

 9. Let be a set of n disjoint sets. Devise a data structure that will A accommodate the following operations in the time bounds listed

 (a) UNION(X, Y ). This sets X to X Y, and destroys Y . ∪
 (b) FIND(x). This returns where x is (recall that the sets are all disjoint and these operations will keep them that way).

 (c) DEUNION: Undoes the last union

 (d) BACKTRACK: Undoes all the unions going back to and includ- ing the largest one formed.

 10. Picture an environment where updates and queries are coming in FAST. You might not have ANY time to do an update to the struc- ture, so you put the update itself in a buffer. Devise a structure for a set on integers where the queries are just to see if some integer is in the structure. How well does it do.

 11. A Deap is a data structure that is a tree such that (a) there is nothing at the root, (b) the left subtree is a Max-heap, (c) the right subtree is a Min-heap, (d) every leaf in the Max-heap is bigger that its corre- sponding leaf in the Min-heap.

 Show how to implement FINDMIN, FINDMAX in O(1), INSERT, and DELETEMIN and DELETEMAX in O(log n), and CREATE in O(n). (My notes about the reference claim that INSERT can be done in O(log log n) steps — but I am not sure I believe that.

 36


-----

###### 12. Devise a Data Structure for a weighted Directed Graph on n nodes that can do the following operations quickly.

 (a) Merge two components,

 (b) locate which component a vertex is in,

 (c) retrieve minimum edge in a component.

 13. Devise a Data Structure for a directed graph that can answer the following three types of queries.

 (a) Given two vertices x and y, determine if there is a path between them. If so, then output the path. This should take time O(1) if there is no path, and O(LENGTH OF PATH) if there is a path.

 (b) Given edge, delete it.

 (c) Given a non-edge, add it as an edge.

 14. Consider the move-to-front heuristic where you decide whether or not to move the item up probabilistically: the more often the item has been accessed, the more likely to move it up. Write pseudocode to implement this heuristic.

 15. Devise a data structure to store n horizontal lines so that you can tell, given an infinite vertical line, if it hits one of them. The data structure should take O(n[2]) space and be able to answer the query in O(1). Look into variants.

 37


-----

###### Analysis of Algorithms

 1. For the following program find a function f (n) such the runtime is Θ(f (n)).

 BEGIN

 Input(n)
 For i := 1 to n do [TAKES 5[i] STEPS]

 i := n
 While i ≥ [n]2 [do]
 begin

 SOMETHING THAT TAKES i STEPS

 i := i 1 −
 END

 2. Assume you could multiply two 3 3 matrices in 18 multiplications × and 54 additions. How fast can you multiply two n n matrices (you × may assume n is a power of 3). Is this better than the algorithm in class for n n matrices? Give conditions on a, b, c, and d such the × following statement holds when a, b, c, and d satisfy that condition: “If one could multiply 2 a a matrices using b multiplications and c × additions then one could multiply two n n matrices in a better way × than that shown in class.” (Try to make the conditions as general as possible.)

 3. The result of applying Gaussian elimination to a square matrix is an upper triangular matrix, U . Suppose you wish to solve the equation

 Ux = c

 for the unknown vector x, where U has n rows and columns and x and c are vectors of size n. How many multiplications are required? Justify your answer.

 38


-----

###### Divide and Conquer

 1. Assume we could multiply two 3 digit numbers with k multiplications.

 a. How fast (just the order, i.e. do not worry about the constants) is a new “fancy” multiplication algorithm based on this fact?

 b. How small does k have to be for this algorithm to be asymptoti- cally faster than the “standard” (O(n[2])) algorithm?

 c. How small does k have to be for this algorithm to be asymptoti- cally faster than the O(n[lg 3]) algorithm?

 2. Assume that additions and multiplications of numbers both take ex- actly one time unit.

 (a) Exactly how many multiplications does the standard matrix mul- tiplication algorithm use to multiply two n n matrices? Exactly × how many additions does it use? What is the exact time it uses to multiply two n n matrices? ×
 (b) What is the exact time to multiply two n n matrices using × Strassen’s algorithm?

 (c) For what values of n is Strassen’s algorithm better than the stan- dard algorithm? Justify your answer.

 3. Devise an O(n log n) algorithm for the following problem: Given n points in the plane, find the pair that is closed together.

 39


-----

###### Dynamic Programming

 1. Let k, n N . The (k, n)-egg problem is as follows: There is a building ∈ with n floors. You are told that there is a floor f such that if an egg is dropped off the f th floor then it will break, but if it is dropped off the (f 1)st floor it will not. (It is possible that f = 1 so the egg always − breaks, or f = n + 1 in which case the egg never breaks.) If an egg breaks when dropped from some floor then it also breaks if dropped from a higher floor. If an egg does not break when dropped from some floor then it also does not break if dropped from a lower floor. Your goal is, given k eggs, to find f . The only operation you can perform is to drop an egg off some floor and see what happens. If an egg breaks then it cannot be reused. You would like to drop eggs as few times as possible. Let E(k, n) be the minimal number of egg-droppings that will always suffice.

 (a) Show that E(1, n) = n.

1
###### (b) Show that E(k, n) = Θ(n k ).

 (c) Find a recurrence for E(k, n). Write a dynamic program to find E(k, n). How fast does it run?

 (d) Write a dynamic program that can be used to actually yield the optimal strategy for finding the floor f . How fast does it run?

 2. Let α and β be constants. Assume that in a tree it costs α to go left, and β to go right. Devise an algorithm that will, given keys k1, . . ., kn which have probabilities of being searched p1, . . ., pn, builds a tree with optimal worst case cost.

 3. Consider the following greedy algorithm for solving the chained matrix multiplication problem: Let the matrices A1, ..., An, have dimensions p1 × q1, ..., pn × qn. Look for the smallest dimension, say qi−1 and pi, and parenthesize between matrices Ai−1 and Ai, so that we multiply A1 to Ai−1 in the best possible way, Ai to An in the best possible way, and finally multiply the two resulting matrices. In order the determine how to multiply A1 to Ai−1 and Ai to An we apply the algorithm recursively.

 Show that this greedy algorithm does not find the optimal way to multiply a chain of matrices.

 40


-----

###### 4. Write an efficient algorithm to determine an order of evaluating the matrix product M1 × M2 × M3 . . . × Mn so as to minimize the scalar multiplications in the case where each M is of dimension 1 1, 1 × × d, d 1, d d for some fixed d. × ×

 5. We are given a collection of n books, which must be placed in a library book case. Let h[1..n] and w[1..n] be arrays, where h[i] denotes the height of the i-th book and w[i] denotes the width of the i-th book. Assume that these arrays are given by the books’ catalogue numbers (and the books MUST be shelved in this order), and that books are stacked in the usual upright manner (i.e., you CANNOT lay a book on its side). All book cases have width W, but you may have any height you like. The books are placed on shelves in the book case. You may use as many shelves as you like, placed wherever you like (up to the height of the book case), and you may put as many books on each shelf as you like (up to the width of the book case). Assume for simplicity that shelves take up no vertical height.

 The book-shelver’s problem is, given h[1..n], w[1..n], and W, what is the minimum height book case that can shelve all of these books. Below shows an example of a shelving. The height and width of the 6th book are shown to the right. (Notice that there is some unnecessarily wasted height on the third shelf.)

h[6]

w[6]

H

W

###### (a) Write down a recurrence for book shelver’s problem.

 (b) Use your recurrence to develop an efficient dynamic programming for solving the book shelver’s problem.

 (c) Analyze the running time of your algorithm.

 41


-----

###### 6. Consider the problem of not only finding the value of the maximum contiguous subsequence in an array, but also determining the two end- points. Give a linear time algorithm for solving this problem. [What happens if all entries are negative?]

 7. Assume that there are n numbers (some possibly negative) in an array, and we wish to find the maximum contiguous sum. Give an efficient algorithm for solving this problem. What is its time?

 8. Assume that there are n numbers (some possibly negative) in a circle, and we wish to find the maximum contiguous sum on the circle. Give an efficient algorithm for solving this problem. What is its time?

 9. Given an array a[1, . . ., n] of integers, consider the problem of finding the longest monotonically increasing subsequence of not necessarily contiguous entries in your array. For example, if the entries are 10, 3, 9, 5, 8, 13, 11, 14, then a longest monotonically increasing subsequence is 3, 5, 8, 11, 14. The goal of this problem is to find an efficient dynamic programming algorithm for solving this problem.

 HINT: Let L[i] be the length of the longest monotonically increasing sequence that ends at and uses element a[i].

 (a) Write down a recurrence for L[i].

 (b) Based on your recurrence, give a recursive program for finding the length of the longest monotonically increasing subsequence. What can you say about its running time?
 (c) Based on your recurrence, give a Θ(n[2]) dynamic programming algorithm for finding the length of the longest monotonically in- creasing subsequence.

 (d) Modify your algorithm to actually find the longest increasing sub- sequence (not just its length).

 (e) Improve your algorithm so that it finds the length of the longest monotonically increasing subsequence in Θ(n lg n) time.

 10. Consider the problem of computing the probability of which team will win a game consisting of many points. Assume team A has probability p of winning each point and team B has probability q = 1 p of winning − each point. Let P (i, j) be the probability that team A will win the game given that it needs i points to win and team B needs j points.

 42


-----

###### (a) Write down a recurrence for P (i, j).

 (b) Use your recurrence to develop an efficient dynamic programming algorithm for determining the probability that team A will win the game given that it needs i points and team B needs j points.

 (c) Analyze the running time of your algorithm.

 11. The traditional world chess championship is a match of 24 games. The current champion retains the title in case the match is a tie. Not only are there wins and losses, but some games end in a draw (tie). Wins count as 1, losses as 0, and draws as 1/2. The players take turns playing white and black. White has an advantage, because he moves first. Assume the champion is white in the first game, has probabilities ww, wd, and wl of winning, drawing, and losing playing white, and has probabilities bw, bd, and bl of winning, drawing, and losing playing black.

 (a) Write down a recurrence for the probability that the champion retains the title. Assume that there are g games left to play in the match and that the champion needs to win i games (which may end in a 1/2).

 (b) Based on your recurrence, give a dynamic programming to cal- culate the champion’s probability of retaining the title.

 (c) Analyze its running time assuming that the match has n games.

 12. You are given an n n matrix A whose entries are either 0 or 1. We × want to decompose this matrix into rectangular submatrices such that the entries in any submatrix are either all 0 or all 1. We limit the decompositions to a special type called guillotine decompositions. A guillotine decomposition of a subarray A[i1..i2, j1..j2] is defined recur- sively, as follows. If i1 = i2 and j1 = j2, then no further decomposition is possible. If i1 < i2 then select any i, i1 i < i2 and split the array ≤ horizontally just after row i, creating two new subarrays A[i1..i, j1..j2] and A[(i + 1)..i2, j1..j2]. If j1 < j2 then select any j, j1 j < j2 ≤ and split the array vertically just after column j, creating two new subarrays A[i1..i2, j1..j] and A[i1..i2, (j + 1)..j2]. If both i1 < i2 and j1 < j2 then you are free to make either type of cut. Once the two submatrices are formed, they may be further decomposed by a guil- lotine decomposition. An example of a guillotine decomposition into submatrices of one value is shown below.

 43


-----

###### 0 1 0 0 1 0 1 0 0 1

 0 1 0 0 1 0 1 0 0 1

 1 1 0 0 1 1 1 0 0 1

 1 1 1 0 0 1 1 1 0 0

 0 0 1 0 0 0 0 1 0 0

 Write a dynamic programming algorithm to determine the MINIMUM number of guillotine cuts needed to decompose the matrix A into sub- matrices of one value. Justify the correctness of your algorithm, and derive its running time. (Note: You do not have to output the actual cuts themselves, just the number of cuts.)

 13. Consider the problem of neatly printing a paragraph on a printer. The input text is a sequence of n words of lengths l1, l2, . . ., ln, measured in characters. We want to print this paragraph neatly on a number of lines that hold a maximum of M characters each. Our criterion for “neatness” is as follows. There MUST be at least one space between any two words on the same line. Except for the last line, if a given line contains words i through j, word i starts in the leftmost position of the line, and word j ends in the rightmost position of the line, and space is inserted between the words as evenly as possible. The amount of extra space between any two words on this line is
 M − [�]k[j] =i [l][k] 1,
 − j i −

 and the total cost of the line is the cube of this value multiplied times (j i). For the last line, we simply put one space between each word, − starting at the leftmost position of the line. We wish to minimize the sum of costs of all lines (except the last). Give a dynamic programming algorithm to determine the neatest way to print the words. It suffices to determine the minimum cost, not the actual printing method. You may assume that every word has length less than M/2, so that there are at least two words on each line. Analyze the running time and space of your algorithm.

 44


-----

###### Greedy Algorithms

 1. Write a greedy algorithm for the Traveling Salesperson Problem Find an infinite set of graphs for which it finds the optimal solution (no proof required). (The Traveling Salesperson problems is, given a weighted graph G, find the minimum cost hamiltonian cycle.)

 2. Give a GREEDY ALGORITHM that tries to find a coloring of a graph that uses the least number of colors. Give a class of graphs for which your algorithm succeeds in finding the least number of colors needed. Give a class of graphs for which your algorithm always uses more colors then it has to.

 3. Assume that you are given a set {x1, . . ., xn} of n points on the real line and wish to cover them with unit length closed intervals.

 (a) Describe an efficient greedy algorithm that covers the points with as few intervals as possible.

 (b) Prove that your algorithm works correctly.

 4. While walking on the beach one day you find a treasure trove. Inside there are n treasures with weights w1, . . ., wn and values v1, . . ., vn. Unfortunately you have a knapsack that only holds a total weight M . Fortunately there is a knife handy so that you can cut treasures if necessary; a cut treasure retains its fractional value (so, for example, a third of treasure i has weight wi/3 and value vi/3).

 (a) Describe a Θ(n lg n) time greedy algorithm to solve this problem.

 (b) Prove that your algorithm works correctly.

 (c) Improve the running time of your algorithm to Θ(n).

 5. Modify Kruskal’s algorithm as follows. Sort the edges of the graph in DECREASING order, and then run the algorithm as before. True or False: This modified algorithms produces a Maximum Cost Span- ning Tree. If True then prove your answer, and if False then give a counterexample.

 6. Modify Dijkstra’s algorithm as follows. (1) Initialize all d[v] values to, (2) rather than performing an Extract-Min, perform an Extract- −∞ Max, and (3) in relaxation, reverse all comparisons so that the shortest

 45


-----

###### path estimate d[v] increases rather than decreases. True or False: This modified algorithm determines the cost of the longest simple path from the source to each vertex. If True then prove your answer, and if False then give a counterexample.

 7. Suppose we are given a graph G (connected, undirected) with costs on the edges (all costs > 0). Now we construct a new graph G[′], which is the same as G, except for the costs. The cost of an edge e is defined to be 1/ce where ce is the cost of e in G.

 (a) Is the Minimum cost spanning tree in G, the Maximum cost span- ning tree in G[′]? Prove or disprove.
 (b) Suppose that P is the shortest path from s to v in G. Is P the longest simple path from s to v in G[′]? Prove, or disprove.

 8. Assume that we have a network (a connected undirected graph) in which each edge ei has an associated bandwidth bi. If we have a path P, from s to v, then the capacity of the path is defined to be the mini- mum bandwidth of all the edges that belong to the path P . We define capacity(s, v) = maxP (s,v) capacity(P ). (Essentially, capacity(s, v) is equal to the maximum capacity path from s to v.) Give an efficient algorithm to compute capacity(s, v), for each vertex v; where s is some fixed source vertex. Show that your algorithm is “correct”, and ana- lyze its running time. (Design something that is no more than O(n[2]), and with the right data structures takes O(m lg n) time.)

 9. Suppose that your boss gives you a connected undirected graph G, and you compute a minimum cost spanning tree T . Now he tells you that he wants to change the cost of an edge. Your job is to recompute the new minimum spanning tree (say T [′]). A good algorithm should recompute the MST by considering only those edges that might change.

 For each of the following situations, indicate whether 1) the MST cannot change 2) the MST can possibly change. If case 2) occurs then describe what changes might occur in the MST. State WHICH edges might possibly be deleted from the MST, and WHICH edges might possibly be inserted into the MST, and HOW you would select the edges to be inserted/deleted. (For extra credit: give a proof for your scheme.)

 46


-----

###### (a) He decreases the cost of an edge e that belongs to T .
 (b) He increases the cost of an edge e that belongs to T .
 (c) He decreases the cost of an edge f that does not belong to T .
 (d) He increases the cost of an edge f that does not belong to T .

 You do not need to design an algorithm, but to simply state the edges that need to be considered.

 10. Prove that if a connected undirected graph has distinct edge weights, then the minimum cost spanning tree is unique. (Hint: Recall the proof of Kruskal’s algorithm.)

 11. Prove the following lemma: If an edge of an undirected weighted graph is the unique most expensive edge on a cycle, then it is not in any minimum-weight spanning tree.

 12. Modify Dijkstra’s algorithm as follows. (1) Initialize all d[v] values to, (2) rather than performing an Extract-Min, perform an Extract- −∞ Max, and (3) in relaxation, reverse all comparisons so that the shortest path estimate d[v] increases rather than decreases. True or False: This modified algorithm determines the cost of the longest simple path from the source to each vertex. If True then prove your answer, and if False then give a counterexample.

 13. A coloring of an undirected graph is assignment of colors to the nodes so that no two neighboring nodes have the same color. In the graph coloring problem, we desire to find the minimum number of colors needed to color an undirected graph.

 One possible greedy algorithm for this problem is to start with an arbitrary node and color it “1”. Then to consider every other node one at a time and color it “1” if it does not neighbor a node already colored “1”. Now do the same for all of the remaining nodes using the color “2”. Continue in this fashion until all of the nodes in the graph are colored.

 (a) How would you implement this algorithm efficiently? Be brief but clear. What is your running time as a function of the number of vertices V, edges E, and colors C . | | | | | |
 (b) Prove that for every graph, the algorithm might get lucky and color it with as few colors as possible.

 47


-----

###### (c) Prove that the algorithm can be arbitrarily bad. In other words, for every constant α > 0 the ratio between the number of colors used by the greedy algorithm and by the optimal algorithm could be at least α.

 48


-----

###### Sorting and Selection

 1. Assume you have some kind of super-hardware that, when given two lists of length m that are sorted, merges them into one sorted list, and takes only m steps. Write down a recursive algorithm that uses
 [√] this hardware to sort lists of length n. Write down a recurrence to describe the run time. (For your own enlightenment replace m with
 [√] other functions and see what happens.)

 2. Consider the following variation of mergesort. Given a set of n num- bers, divide it into three subsets of equal size, sort each of the three subsets, merge the first two subsets in sorted order, and then merge the result with the third subset in sorted order. You may assume that you have available a procedure merge that merges two sorted lists of size n1 and n2 in time n1 + n2. You may also assume that n is a power of three.

 (a) Write an informal program that could implement this algorithm.

 (b) Analyze the cost of this algorithm.

 3. Let a be a number such that 0 a 1. Assume that you have a ≤ ≤ subroutine that finds the minimum of n numbers in n[a] steps. Using this subroutine, write an algorithm that sorts a list of n numbers. How fast does your algorithm run (you may use θ-notation). For what values of a is the algorithm better than θ(n log n) (you may assume n is large and reason asymptotically).

 4. Assume that you have special-purpose hardware that can take two sorted lists of equal size n and merge them in �(n) steps. Devise
 a sorting algorithm using this hardware that performs substantially better than O(n log n).

 5. Let A[1..n] be an array such that the first n n elements are already − [√] sorted (though we know nothing about the remaining elements. Write an algorithm that will sort A in substantially better than n log n steps.

 6. For what values of α, 0 α 1 is the following statement TRUE: ≤ ≤ Given an array A[1..n] where the first n n[α] are sorted (though we − know nothing about the remaining elements), A can be sorted in linear time (i.e., O(n) steps).

 49


-----

###### 7. Let P be a program that has the following format.

 PROCEDURE P

 begin

 Input(n) (this takes 0 steps)

 if n = 1 then execute 4 operations and stop. (if n = 1 this takes 0 ̸ operations.)

 Execute n operations
 Call P on input ⌊ [n]3

 [⌋]
 Execute n operations


###### Call P on input ⌊ [n]4

 [⌋]
 end


###### Write a recurrence for T (n), the running time of this program. Find a number c such that for all n 1, T (n) cn. ≥ ≤

 8. Assume you had a way of expressing the product of two numbers of n bits long by using a products of numbers that are [n]

_b_ [long, along with]
###### addition of c numbers. How fast can you multiply two numbers of n bits long. For what values of a, b, c is this better than the algorithm in class.

 9. In American we have coins for 1 cent, 5 cents, 10 cents, and 25 cents. Show that if you want x cents and the least amount of coins, the greedy algorithm is optimal. Exhibit of set of coin denominations for which greedy is not optimal, the includes a 1 cent coin.

 10. Devise a structure that allows MAX and MIN in O(1) steps, INSERT in O(log n) steps, and DELETE in O(n). (For your own enlighten- ment, and ONE extra point, come up with a structure that allows MAX and MIN in O(1) steps, INSERT in O(log n), and DELETE also in O(log n).)

 11. You wish to store a set of n numbers in either a heap or a sorted array. (Heap is MAX-heap, has MAX element on top, etc.) For each of the following desired properties state whether you are better off using a heap or an ordered array, or that it does not matter. Justify your answers.

 50


-----

###### (a) Want to find the MAX quickly.

 (b) Want to be able to delete an element quickly.

 (c) Want to be able to form the structure quickly.

 (d) Want to find the MIN quickly.

 12. Given n elements we are going to, in the course of time, (1) do an add or delete a times, (2) try to find MAX b times, (3) try to find MIN c times. We can assume a, b, c are much smaller than n. For what values of a, b, c are we better off using a heap? For what values are we better off using a sorted array. (You must also take into consideration the time spent forming these structures.)

 13. Assume that we are going to be sorting arrays A[1..n] but that we have a MAGIC algorithm that sorts arrays of size ≤ [n]3 [in][ n][ steps. Rewrite]
 the pseudocode for QUICKSORT on page 154 so that it can use this MAGIC algorithm. What is the worst case performance? What is the best case performance?

 14. For each of the following scenarios indicate if you would use QUICK- SORT or HEAPSORT and why.

 (a) It is absolutely crucial that the array gets sorted quickly.

 (b) The array is such that you have a good idea of where the median is.

 (c) Space is a crucial parameter- you can’t use even a little bit of extra space.

 (d) Space is relevant, but using a little extra space is okay.

 15. Assume that you have hardware that can sort log n elements in ONE step. We are thinking of sorting a list of n elements using this hard- ware. What is a LOWER BOUND on how well we can do? Explain your result. (You can assume that the only operations allowed are comparisons, the operation above, and swaps. Hence a variation of the decision tree model is appropriate.)

 16. Let f (n) be a function of n. Assume that we are going to sort n numbers from the set 1, . . ., f (n) . Assume that we use RADIX sort. { } Find an infinite number of functions f such that RADIX SORT per- forms substantially better than O(n log n).

 51


-----

###### 17. The algorithm for bucket sort is geared to take inputs in the range
 [0, 1) (fractions allowed of course). Let p be a positive natural number. Adjust the algorithm so it takes inputs that are natural numbers in 1, . . ., pn and uses p buckets. Discuss informally how this algorithm { } might behave if the inputs are chosen with the distribution Prob(x = i) = [K]i [(Where][ K][ is the appropriate constant). How might you adjust]
 the algorithm so that it performs well for this distribution?

 18. Consider the following two statements: (1) Sorting n elements RE- QUIRES Ω(n log n) operations, (2) Radix sort, counting sort, and bucket sort perform in time substantially better than O(n log n). These statements seem to be in contradiction. Explain carefully why they are not.

 19. Assume that you can find the median of 7 elements in 12 comparisons. Devise a linear-time MEDIAN FINDING algorithm that uses this. Give an upper bound on the number of comparisons used (do NOT use O-notation). Try to make the bound as tight as possible.

 20. Let a, b be numbers. Assume that you can find the median of a el- ements in b comparisons. Use this in the linear-time median finding algorithm. Give an upper bound on the number of comparisons used (do NOT use O-notation). Try to make the bound as tight as possible. Find values of a, b such that you can find medians in 4n comparisons. ≤

 21. For each of the following scenarios say whether you would use MERGE- SORT, QUICKSORT (or variants), RADIX SORT, or COUNTING SORT. Briefly explain why you chose the one you did.

 (a) The elements to be sorted are numbers from the set 1, . . ., log n { } but the only operations we are allowed to use are COMPARE and SWAP.

 (b) We have access to a VERY FAST median finding algorithm that we can use as a subroutine.

 (c) The elements to be sorted are numbers from the set 1, . . ., n { } and we have access to the actual bits of the number.

 (d) No bound is known on the elements to be sorted, but we need to guarantee fast performance.

 52


-----

###### 22. Assume that c 0. Assume you had some kind of super-hardware ≥ that, when given two lists of length m that are sorted, merges them into one sorted list, and takes only m[c] steps. Write down a recursive algorithm that uses this hardware to sort lists of length n Write down a recurrence to describe the run time. For what values of c does this algorithm perform substantially better than O(n log n)?

 23. Assume that n numbers are in a MAX-heap.

 (a) Show that the third largest element can be found in O(1) steps.
 (b) Show that if i is any constant then the ith largest element can be found in O(1) steps

 24. Let d(n) be a function of n such that d(n) << n. Imagine that we redesigned MAX-heaps so that instead of every internal node hav- ing 2 children (except possibly the rightmost internal node on the second-to-last level, which may have 1 or 2 children), they had d(n) children (except possibly the rightmost internal node on the second- to-last level, which may have 1, . . ., d(n) children). How fast would the following operations be? You may use Θ-notation. (a) FIND MAX, (b) INSERT, (c) DELETE MAX, (d) FIND (given a key, determine whether it is in the structure).

 25. Let d 0. We have special hardware labeled MAGIC that, given ≥ an array B[1..m], places the smallest [m]2 [elements into][ B][[1][..] [m]2 [] (not]
 necessarily in order), places the largest m

2 [into][ B][[(] _[m]2_ [+ 1)][..m][] (not]

###### necessarily in order), and returns the index of the largest element in the first partition (i.e., MAGIC does what PARTITION does in the usual QUICKSORT algorithm). Assume that this hardware works in m[d]
 steps. Describe a sorting algorithm similar to QUICKSORT that uses MAGIC to sort A[1..n]. For what d, will this sorting algorithm perform (1) much better than Θ(n log n), (2) much worse than Θ(n log n), (3) in Θ(n log n)?

 26. In answering a, b, and c no explanations are needed. Also, QUICK- SORT refers to the randomized version.

 (a) Give a scenario where RADIXSORT is better than MERGE- SORT.

 (b) Give a scenario where MERGESORT is better than QUICK- SORT.

 53


-----

###### (c) Give a scenario where QUICKSORT is better than RADIXSORT.

 27. Let a, b 0. We are going to be sorting numbers between 1 and ≥ n[a](log n)[b]. Find all values of a, b such that COUNTING SORT will perform substantially better than O(n log n).

 28. We are going to be sorting numbers in the interval [0, 1) using BUCK- ETSORT. (We use the version in the book where there are n buckets and each individual one is sorted by INSERTION SORT.)

 (a) Find an increasing function f such that the following holds: ‘If when doing BUCKETSORT we are guaranteed that no bucket has more than f (n) elements in it, then BUCKETSORT is guar- anteed to do substantially better than O(n log n).’

 (b) Find an infinite number of such functions with different orders of magnitude.

 29. Assume you have some kind of super-hardware that, when given two lists of length m that are sorted, merges them into one sorted list, and takes only m steps. Write down a recursive algorithm that uses
 [√] this hardware to sort lists of length n. Write down a recurrence to describe the run time. (For your own enlightenment replace m with
 [√] other functions and see what happens.)

 30. Assume that we have a MAGIC ALGORITHM that can, given an array of n elements, finds the [n]

3 _[rd][ largest element in][ √][n][ comparisons.]_
###### Use this to devise an algorithm that takes cn log n comparisons. similar to QUICKSORT. What is the lowest YOU can make c? (This last part is for speculation, not serious grading.)

 31. Assume that we have MAGIC HARDWARE that can sort k elements in 1 step.

 (a) Give an algorithm for sorting (n elements) that uses this hard- ware. What is its running time?

 (b) Give a lower bound on how well any algorithm with this hardware can do.

 32. Assume that we have MAGIC HARDWARE that can find the MAX of three elements in 1 step.

 54


-----

###### (a) Give an algorithm for MAX (of n elements) that uses this hard- ware. What is its running time?

 (b) Give a lower bound on how well any algorithm with this hardware can do. It should match the upper bound.

 33. Assume that the array A[1..n] only has numbers from 1, . . ., n[2] but { } that at most log log n of these numbers ever appear. Devise an algo- rithm that sorts A in substantially less than O(n log n).

 34. In some applications the lists one wants to sort are already ‘partially sorted’ Come up with a formal way to measure ‘how sorted’ a list is. Devise an algorithm that does very well on lists that are almost sorted (according to your definition). (Note— there is no one ‘right answer’ to this problem, however whatever answer you give must be well thought out. Your definition must be rigorous.)

 35. Let a, b be real numbers such that a, b 0. Assume you have some ≥ kind of super-hardware that, when given 12 sorted lists of length m, merges them in a[m]m[b] steps.

 (a) Write an algorithm that uses this hardware to, given an array A[1..n], sort it.

 (b) Let T (n) be the running time of your algorithm. Find a function fa,b such that T (n) = θ(fa,b). (The function fa,b might involve several cases.)

 (c) For what values of a, b does your algorithm run substantially faster than O(n log n)?

 36. Let a FEAP be just like a HEAP except that the internal nodes have FIVE children instead of TWO (only the right most internal node might have less than FIVE children).

 (a) Give an algorithm that does the following: given a FEAP and a new element, remove the root of the FEAP and insert the new element. (When you are done you must have a FEAP again.) You must describe your algorithm informally (i.e., NO CODE). Give an example of your algorithm at work.

 (b) How many comparisons does your algorithm take in the worst case? How many comparisons does your algorithm take in the

 55


-----

###### best case? How many moves does it make in the worst case? How many moves does it make in the best case? (Do not ignore multiplicative constants.)

 37. Assume that the array A[1..n] only has numbers from 1, . . ., n[1][.][2] but { } that all numbers that appear are multiples of n. (You may assume
 [√] that n and n[1][.][2] are integers.) Devise an O(n) algorithm to sort A.
 [√]

 38. Let a, b be real numbers such that a, b 0. Assume you have some ≥ kind of super-hardware that, when given an array A[1..m] returns the following: the ( [m]

5 [)][th][ largest element, the (] [2]5[m] [)][th][ largest element,]

###### the ( [3][m]

5 [)][th][ largest element, and the (] [4]5[m] [)][th][ largest element. Assume]

###### this hardware runs in time m[a](log m)[b]. (Formally the numbers above should be ⌊ [m]5

 [⌋][, etc., but you may ignore this for the purposes of this] problem.)

 (a) Write an algorithm that uses this hardware to sort lists of length n.

 (b) Let T (n) be the running time of your algorithm. Find a function fa,b such that T (n) = θ(fa,b). (The function fa,b might involve several cases and might depend on a and b.)

 39. (a) Exhibit an O(log n) algorithm that will, given a heap on n ele- ments and a number m with m log log n, find and delete the ≤ mth largest element in the heap. (The end result is a heap that has that one element deleted.)

 (b) Assume m is a constant. Find functions gB(n) and gW (n) such that your algorithm takes gB(n) + θ(1) comparisons in the Best case, and gW (n) + θ(1) comparisons in the Worst case. (Note that multiplicative constants are important.)

 (c) Assume m is log log n. Find functions hB(n) and hW (n) such that your algorithm takes hB(n) + θ(1) comparisons in the Best case, and hW (n) + θ(1) comparisons in the Worst case. (Note that multiplicative constants are important.)

 40. Consider the following problem: given a list of n elements, output some element larger than the median element. Derive both upper and lower bounds for this problem in terms of the number of comparisons needed. Also consider the model where you can ask k comparisons at a time.

 56


-----

###### 41. Assume that we have MAGIC HARDWARE that can find the 3rd largest of log n elements in 1 step. Give a lower bound on how well any algorithm with this hardware can do.

 42. Let A be an array of positive integers (> 0), where A(1) < A(2) < . . . < A(n). Write an algorithm to find an i such that A(i) = i (if one exists). What is the running time of your algorithm ?

 If the integers are allowed to be both positive and negative, then what is the running time of the algorithm (Hint: redesign a new algorithm for this part.) ?

 43. Consider a rectangular array of distinct elements. Each row is given in increasing sorted order. Now sort (in place) the elements in each column into increasing order. Prove that the elements in each row remain sorted.

 44. The professor claims that the Ω(n lg n) lower bound for sorting n num- bers does not apply to his workstation, in which the control flow of the program can split three ways after a single comparison ai : aj, accord- ing to whether ai < aj, ai = aj, or ai > aj. Show that the professor is wrong by proving that the number of three way comparisons required to sort n elements is still Ω(n lg n).

 45. Let hi-lo BE the problem of, given n numbers, find the smallest and largest elements on the list. You may assume that n is even.

 (a) Give an algorithm to solve HI-LO with 2n 3 comparisons. −
 (b) Give an algorithm that uses substantially less than 2n compar- isons. (HINT: Imagine you are running a tennis tournament and wish to find the best and worst players.)

 (c) Show that the algorithm presented in the last part is optimal.

 46. Write an algorithm Partition(A,p,r,s) to partition array A from p to r based on element A[s], using exactly r p comparisons. −

 47. Show how to implement quicksort in worst case O(n lg n) time. Your algorithm should be high level and very brief. (HINT: We need to choose the partition element carefully.) Supply the analysis, which should also be very brief.

 57


-----

###### 48. Consider the following quicksort-like sorting algorithm. Pick two el- ements of the list. Partition based on both of the elements. So the elements smaller than both are to the left, the elements in between are in the middle, and the elements larger than both are to the right.

 a. Write high level code for this algorithm.

 b. How many comparisons and exchanges does the partition algo- rithm use?

 c. Assume the partition elements always partition exactly into thirds. Write a recurrence for T (n), the number of comparisons. Find a constant a such that, for all n, T (n) an. ≤
 d. Assume the partition elements always partition so exactly one quarter are to the left, one half in the middle, and one quarter to the right. Write a recurrence for T (n), the number of compar- isons. Find a constant a such that, for all n, T (n) an. ≤
 e. Can you refine your analysis of this version of quicksort? For example, can you find its average case?

 49. The usual deterministic linear time (worst case) SELECT algorithm begins by breaking the set into groups of 5 elements each. Assume that we changed the algorithm to break the set into groups of 7 elements each.

 a. Write down the recurrence for the new running time. (You can let c be the number of comparisons needed to find the median of 7 elements.)

 b. Solve the recurrence.

 50. A d-ary heap is like a binary heap, but instead of two children, nodes have d children.

 (a) How would you represent a d-ary heap in an array?
 (b) What is the height of a d-ary heap of n elements in terms of n and d.

 (c) Explain loosely (but clearly) how to extract the maximum ele- ment from the d-ary heap (and restore the heap). How many comparisons does it require?

 (d) How many comparisons does it take to sort? Just get the high order term exactly, but show your calculations.

 58


-----

###### (e) What value(s) of d are optimal? Justify your answer.

 51. We are going to derive the average number of moves for quicksort using a somewhat unusual partitioning algorithm. We partition on the first element. Take it out. Look for the right most element that is smaller and place it in the first position (which is the newly opened position on the left side). Look for the left most element that is larger and place it in the newly opened position on the right side. Starting from there look for the right most element that is smaller and place it in the the newly opened position on the left side. Starting from there look for the left most element that is larger and place it in the newly opened position on the right side. Continue in this fashion until the pointers cross. Finally, put the partition element into the hole, which is its final position in the sorted array.

 (a) Assume that the partition element ends up in position q. What is the probability that an element originally to the left went to the right?

 (b) Assume that the partition element ends up in position q. What is the expected number of elements originally to the left that go to the right?

 (c) Assume that the partition element ends up in position q. What is the expected number of moves?

 (d) Write a recurrence for the expected number of moves.

 (e) Simplify the recurrence, but do not solve it.

 (f) To keep the calculations simple, assume you got the following recurrence:

_n−1_

###### T (n) = [2] � T (q) + q
 − [q][2]
 n [[] n []]

_q=1_


###### Use constructive induction to show that T (n) an ln n. Try to ≤ get a good value of a.
 (g) Heapsort makes about n lg n moves. How does quicksort com- pare?

 52. Devise an algorithm that finds the second largest of four elements.

 (a) Briefly describe the algorithm in English.

 (b) Give a decision tree for it.

 59


-----

###### 53. Let MAXn be the problem of finding the max of n numbers. Let SECn be the problem of finding the second largest of n numbers. We assume the decision tree model, i.e., only comparisons are the main operation.

 (a) Show that in any Decision Tree for MAXn, every branch has depth at least n 1. (HINT: if only n 2 comparisons are made − − then show that the maximum cannot be determined.)
 (b) Show that any Decision tree for MAXn has 2[n][−][1] leaves.
 (c) Let T be a Decision tree for SECn. Let i be such that 1 ≤ i ≤ n. Let Ti be formed as follows: take tree T and, whenever there is a comparison between xi and xj, eliminate the comparison by assuming that xi wins.
 i. Argue that Ti is essentially a decision tree to find MAX on {x1, . . ., xn} −{xi}. ii. Show that, for all i, Ti has 2[n][−][2] leaves. iii. Show that, for all i and j, the leaves of Ti and the leaves of Tj are disjoint. iv. Find a lower bound on the number of leaves in T by using the last two items. v. Show that T has depth n + lg n O(1). ⌈ ⌉−

 54. Assume you had a special hardware component that could find the minimum of n numbers in one step. Give upper and lower bounds
 [√] for sorting using this component.

 55. Assume you had a special hardware component that could sort n
 [√] numbers in one step. Give upper and lower bounds for sorting using this component.

 56. We are going to derive a lower bound for merging two lists of sizes m, n. (Assume all of the elements are distinct.)

 (a) Let S(m, n) be the number of arrangements of two lists X, Y where each list keeps its original order. In this problem you will find S(m, n) two ways.
 i. Show that �S(m,n)=m+n� using a combinatorial argument.
_m_
###### ii. In all of the arrangements, either the first element of X is the smallest or the first element of Y is the smallest (but

 60


-----

###### not both). Assume it is the first element of X. How many arrangements of the remaining elements are there? Assume it is the first element of Y . How many arrangements of the remaining elements are there? Based on this information, write down a recurrence for S(m, n). Show that �mm+n� is a solution to your recurrence.

 (b) Give a lower bound for the number of comparisons needed to merge two lists. Simplify your answer using Stirling’s formula.

 (c) What is your answer when m = n (write it as simply as possible). How does it compare to the lower bound of 2n 1. −

 57. Consider the problem of sorting a sequence of n 0’s and 1’s using comparisons. For each comparison of two values x and y, the algorithm learns which of x < y, x = y, or x > y holds.

 (a) Give an algorithm to sort in n 1 comparisons in the worst case. − Show that your algorithm is optimal.

 (b) Give an algorithm to sort in 2n/3 comparisons in the average case (assuming each of the n inputs is 0 or 1 with equal probability). Show that your algorithm is optimal.

 58. Assume you have a list of n elements, where each element is within k positions of its correct sorted position (on either side). (If k = 0 then the deck is sorted.)

 (a) Give a lower bound on the number of comparisons it takes to sort the list. Make your bound as exact as possible. A little looseness in your “proof” is acceptable here. Justify your answer.

 (b) Give an efficient comparison-based algorithm for sorting the list. How many comparisons does it use in the worst case.

 (c) Compare your upper and lower bounds.

 59. Consider the problem of partitioning n elements into k equal sized groups, so that the first group has the smallest n/k elements (not nec- essarily sorted), the second group has the next smallest n/k elements (not necessarily sorted), etc. (You may assume that k divides n.)

 a. Derive a lower bound for the number of comparisons needed for solving this problem.

 61


-----

###### b. Give an efficient algorithm for solving this problem.

 c. Analyze its running time.

 60. (a) Assume you are given a number X and two sorted lists of n numbers each: A1 A2 An and B1 B2 ≤ ≤· · · ≤ ≤ ≤· · · ≤ Bn. Design a linear (i.e. O(n)) time algorithm to determine how many pairs (i, j) there are such that Ai + Bj X. Justify the ≤ correctness and running time of your algorithm.

 (b) Show how to preprocess the lists A and B (in any way that you like and producing any data structure that you like) so that given X, the pair counting problem can be solved in o(n) time. How much preprocessing time do you use? How much storage is used? How much time is needed to answer one query (after preprocess- ing)?

 61. Illustrate the operation of radix sort on the following list of English words: RUT, TOP, SUP, POT, TON, OPT, TOR, ROT, TOO, OUT, SUR, PUT

 62. For this problem, assume that you have access to a procedure Merge(A,
```
  B, C, na, nb), that merges two sorted arrays A[1..na] and B[1..nb]
 into a single sorted array C[1..na+nb]. This procedure runs in O(na+ nb) time. Assume we also have access to unlimited dynamic array al- location.

 Suppose that you have a collection of n, 1-dimensional arrays each of length n, D[1..n][1..n], such that each array is sorted (i.e. D[i][j]
  <= D[i][j+1]). We want to compute a single sorted array that con tains all n[2] elements.

 The first strategy for accomplishing this is called cascading merging. First merge D[1] with D[2] to form an array of length 2n, then merge this array with D[3] to form an array of length 3n, etc. The final merge is between an array of length (n 1)n with D[n] to form the − final sorted array of length n[2]. See the figure below.

 62

```

-----

###### D[1] ❍❍ D[1] ❍❍

✟ ✟
✟ ❍❍ ✟

###### D[2] ✟✟❍❍ D[2] ❍❍❍❍

✟ ✟ ✟
✟ ✟ ✟

###### D[3] ✟✟ D[3] ❍❍✟✟

✟ ✟
✟ ✟

###### D[4] D[4]


###### Cascading Merging Balanced Merging

 The second strategy is called balanced merging. Assume that n is a power of 2. First merge pairs D[1] and D[2] together, D[3] and D[4] together, and so on until merging D[n-1] and D[n] together. The result is n/2 sorted arrays of size 2n each. Next, repeat the balanced merging on these arrays, resulting in n/4 arrays of size 4n each. This is repeated until there is 1 array of size n[2].

 (a) What is the total running time of cascading merging? Justify your answer.

 (b) What is the total running time of balanced merging? Justify your answer.

 For both parts (a) and (b) count only the time spent in the merging procedure.

 63. Suppose you have a list of n numbers consisting of k n distinct ≤ values. For 1 ≤ i ≤ k there are mi copies of the i-th value.

 (a) Show that

� _n!_ �
###### O n + lg
 m1!m2! . . . mk!
 comparisons are necessary to sort this list by a comparison-based sorting algorithm. (Note: You are required to show ONLY the lower bound, you do not need to show that this is always possible.) Note that any algorithm for this problem does NOT know in advance what the values of m1, m2, . . ., mk are.
 (b) Show that this many comparisons are sufficient to sort (i.e. give an algorithm). Derive the running time of your algorithm.

 64. Selection Sort can be thought of as a recursive algorithm as follows: Find the largest element and put it at the end of the list (to be sorted). Recursively sort the remaining elements.

 63


-----

###### a. Write down the recursive version of Selection Sort in pseudocode.

 b. Derive a recurrence for the exact number of comparisons the al- gorithm uses.

 c. Use the iteration method to solve the recurrence. Simplify as much as possible.

 d. Use mathematical induction to verify your solution.

 65. Insertion sort can be expressed as a recursive procedure as follows. In order to sort A[1 . . . n], recursively sort A[1 . . . n 1] and then insert − A[n] into the sorted array A[1 . . . n 1]. −

 a. Write the pseudocode for this (recursive) algorithm.

 b. Give a recurrence for the number of comparisons this algorithm uses in the worst-case.

 c. What is the solution to the recurrence. Prove it using mathemat- ical induction.

 66. Consider the following algorithm that merges two lists: X = x1, x2, . . ., xn and Y = y1, y2, . . ., yn. Assume n > 1 is a power of two. (For n = 1, just compare the two elements.)

 1) Separate X and Y into even and odd indexed items, so X [′] = x1, x3, . . ., xn−1 and X [′′] = x2, x4, . . ., xn, and Y [′] = y1, y3, . . ., yn−1 and Y [′′] = y2, y4, . . ., yn.
 2) Merge X [′] and Y [′] into U .
 3) Merge X [′′] and Y [′′] into V .
 4) Interleave U and V into u1, v1, u2, v2, u3, v3, . . ., un, vn.
 5) Compare each pair of elements vi and ui+1 (and exchange if vi > ui+1).

 Answer the following questions about the algorithm.

 (a) Write a recurrence for how many comparisons this merging algo- rithm uses.

 (b) Solve the recurrence using the iteration method.

 (c) Prove that this algorithm merges correctly.

 64


-----

###### 67. Consider an n n array A containing integer elements (positive, neg- × ative, and zero). Assume that the elements in each row of A are in strictly increasing order, and the elements if each column of A are in strictly decreasing order. (Hence there cannot be two zeroes in the same row or the same column.) Describe an efficient algorithm that counts the number of occurrences of the element 0 in A. Analyze its running time.

 68. Let f be a function defined on the interval 0 to 1 (i.e. 0 x 1), ≤ ≤ which achieves its maximum value at point xM, a point in the interval, and is strictly increasing for 0 ≤ x < xM and strictly decreasing for xM < x ≤ 1. (Note: xM may be 0 or 1.) The only operation you can do with f is evaluate it at points in its interval.

 (a) Write an algorithm to find xM with error at most ϵ, i.e., if your algorithm’s answer is p, then |p − xM | < ϵ. Use instructions of the form y f (x) to indicate evaluation of f at the point x. Try ← to use as few evaluations as possible. Count your evaluations as exactly as possible.

 (b) How many evaluations does your algorithm do in the worst case?

 65


-----

###### NP-Completeness

 1. If G = (V, E) is a graph then a vertex cover for G is a set V [′] ⊆ V such that for every edge in G one of the endpoints is in V [′]. Let

 A1 = {(G, k) | G has a vertex cover of size ≤ k}.

 A2 = {G | G has a vertex cover of size ≤ 12}.

 Show that A1 NP. Show that A1 is NP-complete. Show that A2 P. ∈ ∈ Show that A2 can be solved in O(n[a]) where a < 10.

 2. We define A ≤ww B if there are 12 functions f1, . . ., f12 such that each one can be computed in polynomial time and
 x ∈ A iff at least 6 elements of {f1(x), . . ., f12(x)} are in B.
 Show that if B ∈ P and A ≤ww B then A ∈ P.

 3. Assume f1 takes time p1(n), f2 takes time p2(n), . . ., f12 takes time p12(n), and the algorithm for B takes time q(n), where n is the length of the input. Express the runtime for the algorithm for A in terms of p1, p2, . . ., p12 and q.

 4. For each of the following sets state whether it is in NP or not (no proof required). Then state whether or not it is known to be in P. If it is known to be in P then give an algorithm for it that takes polynomial time. If it is not known to be in P then nothing more is required.

 (a) A1 = {(a1, . . ., ak, N ) | some subset of {a1, . . ., ak} adds up to a number that is N . ≤ } (b) A2 = {(a1, . . ., ak, N ) | some subset of {a1, . . ., ak} adds up to exactly N . } (c) A3 = {(a1, . . ., ak, N ) | some subset of {a1, . . ., ak} adds up to a number that is N ≥ }

 5. Let G be a graph where every edge is labelled with a different Boolean variable. Let v be a vertex of G. Let φG,v be the exclusive-OR of all the edges that have v as an endpoint. Let φG be the AND of all the φG,v as v ranges over the vertices of G. Is the following problem NP-complete: Given a graph G that has edges labelled with different Boolean variables, determine if φG is satisfiable.

 66


-----

###### 6. We define A ≤w B if there are 2 functions f1, f2 such that each one can be computed in polynomial time and
 x ∈ A iff f1(x) ∈ B and f2(x) /∈ B.
 Show that if B ∈ P and A ≤w B then A ∈ P. (Assume f1 takes time p1(n), f2 takes time p2(n), and the algorithm for B takes time q(n). With this, you should be able to express the running time for the algorithm for A in terms of p1, p2, and q.)

 7. Prove that P = NP, then P = co-NP.

 8. A stable set of vertices in a graph do not have any edges between them. The optimization version of this problem is to find a maximum stable set in a graph.

 a. Define a decision version of the stable set problem.

 b. Show that the decision version is in NP.

 c. Show that if you could solve the optimization version in polyno- mial time that you could also solve the decision version in poly- nomial time.

 d. Show that if you could solve the decision version in polynomial time that you could also solve the optimization version in poly- nomial time.

 e. Show that it is NP-complete. HINT: Use CLIQUE. (Or alterna- tively show that it is polynomially equivalent to the clique prob- lem.)

 f. Show that you can solve the decision version for constant size stable sets in polynomial time.

 9. The Hamiltonian path problem (HP) is: given an undirected graph G = (V, E), does there exist a simple path that passes through every vertex of G? The Directed Hamiltonian path problem (DHP) is: given a directed graph G = (V, E), does there exist a simple path that passes through every vertex of G? The Hamiltonian cycle problem (HC) is: given an undirected graph G = (V, E), does there exist a simple path that passes through every vertex of G? The Directed Hamiltonian cycle problem (DHC) is: given a directed graph G = (V, E), does there exist a simple path that passes through every vertex of G?

 67


-----

###### Show that all four of the problems above are in NP. For all pairs of problems P1, P2 from {HP, DHP, HC, DHC} show that P1 ≤p P2.
 (HINT on HP ≤p HC. You will need to change the graph. Replace some vertex v V by two new vertices, x and y, that are adjacent to ∈ the same vertices that v was. What else do you need to do? Try to “force” any Hamiltonian path to visit these vertices first and last.)

 10. Consider the problem DENSE SUBGRAPH: Given G, does it contain a subgraph H that has exactly K vertices and at least Y edges ? Prove that this problem is NP-complete. You could pick any problem to reduce from.

 11. Assume that the following problem is NP-complete. PARTITION: Given a finite set A and a “size” s(a) (a positive integer) for each� a ∈ A. Is there a subset A[′] ⊆ A such that [�]a∈A[′][ s][(][a][) =]
_a∈A−A[′][ s][(][a][) ?]_

###### Now prove that the following SCHEDULING problem is NP-complete: Given a set X of “tasks”, and a “length” ℓ(x) for each task, three processors, and a “deadline” D. Is there a way of assigning the tasks to the three processors such that all the tasks are completed within the deadline D? A task can be scheduled on any processor, and there are no precedence constraints. (Hint: first prove the NP-completeness of SCHEDULING with two processors.)

 12. Prove that the following ZERO CYCLE problem is NP-complete: Given a simple directed graph G = (V, E), with positive and negative weights w(e) on the edges e E. Is there a simple cycle of zero weight ∈ in G? (Hint: Reduce PARTITION to ZERO CYCLE.)

 13. Let A be an algorithm that accepts strings in a language L. Let p(n) be a polynomial. Assume that A runs in p(n) time if a given string x is in L, but in superpolynomial time if x is not in L. Give a polynomial time algorithm for recognizing strings in L.

 14. Prove that the following problem is NP-complete. SPANNING TREE WITH A FIXED NUMBER OF LEAVES: Given a graph G(V, E), and an integer K, does G contain a spanning tree with exactly K leaves ?

 (a) First prove that the problem is in NP by describing a “guessing” algorithm for it. (Write out the algorithm in detail.)

 68


-----

###### (b) Now prove that the problem is NP-hard, by reducing UNDI- RECTED HAMILTONIAN PATH to it. HAMILTONIAN PATH asks for a simple path that starts at some vertex and goes to some other vertex, going through each remain- ing vertex exactly once.

 15. Show that both of the following two problems are NP-complete. For each show that the problem is in NP, and show that a known NP- complete problem is reducible to this problem.

 Subgraph Isomorphism: Given two undirected graphs G1 = (V1, E1) and G2 = (V2, E2), is G1 is a subgraph of G2? More formally is there are 1–1 function π : V1 → V2 such that for all {u, v} ∈ E1, {π(u), π(v)} ∈ E2. (Hint: Use either CLIQUE or Hamiltonian Cycle.)

 Longest Simple Cycle: Given an undirected graph G and an inte- ger k, does G have a simple cycle of length greater than or equal to k? (Hint: Use Hamiltonian Cycle.)

 16. Assume that you are given access to function CLIQUE(G, K) that returns “True” if G contains a clique of size at least K, and “False” otherwise.

 (a) Use the function CLIQUE to determine, in polynomial time, the size of the largest clique by making. (Try and solve the problem by asking the function CLIQUE as few questions as possible.)

 (b) How can you use the function CLIQUE to actually compute a clique that is largest in size ? (Try and solve the problem by asking the function CLIQUE as few questions as possible.)

 17. The cycle cover problem (CC) is: given a directed graph G = (V, E) and an integer k is there a subset of vertices V [′] ⊆ V of size k such that every cycle of G passes through a vertex in V [′]? Prove that CC is NP-complete. (Hint: The proof that CC is in NP is tricky. Note that a graph can have an exponential number of cycles, so the naive verification algorithm will not work. The reduction is from vertex cover.)

 18. Suppose we had a Boolean function SAT (F ), which given a Boolean formula F in conjunctive normal form, in polynomial time returns

 69


-----

###### True if the function is satisfiable and False otherwise. (This is very unlikely since it would imply P = NP!) This function tells you nothing about how to set the variables to satisfy the formula. Show how to use this function to determine the actual variable assignment that makes the formula True.

 19. If G = (V, E) is a graph then a Dominating Set is a set V [′] ⊆ V such that, for all vertices v, either v ∈ V [′] or v is adjacent to an element of V [′].

 (a) Let DOM = (G, k) G has a dominating set of size k . Show { | } that DOM is NP-complete (Hint: Use the Vertex Cover prob- lem.)
 (b) Let PLANAR DOM = (G, k) G is planar and has a dominating set of size k . − { | } Show that PLANAR DOM is NP-complete (Hint: Use the − DOM problem.)
 (c) Let IND PLANAR DOM = (G, k) G is planar and has a dominating set of size k tha − − { |
 Show that IND PLANAR DOM is NP-complete (Hint: Use − − the PLANAR DOM problem.) −
 (d) Fix k. Let IND−PLANAR−DOMk = {G | G is planar and has a dominating set of size k
 Show that IND − PLANAR − DOMk can be solved in O(6[k]n) time where the constant does not depend on k. (Hint: Use that a planar graph always has a vertex of degree 5.) ≤

 20. Let q, k be a fixed constant. Let q-CNF be CNF where each clause has q literals. A formulas is MONOTONE if it has no negated variables. ≤

 (a) Let q k MONO SAT be the set of all q-CNF monotone − − − formulas that are satisfiable with an assignment that has at most k variables set to TRUE. Show that q k MONO SAT can − − − be solved in O(2[k]n) where the constant does not depend on k.
 (b) q k SAT be the set of all q-CNF formulas that are satisfiable − − with an assignment that has at most k variables set to TRUE. Show that q k SAT can be solved in O(2[k]n) where the constant − − does not depend on k.

 21. (a) Show that the problem of testing if a graph is k-colorable is NP- complete.
 (b) Show that if G is a graph and v is a node of degree d then G ≤ is d + 1-colorable iff G v is d + 1-colorable. −{ }

 70


-----

###### (c) Fix k. Show that determining if a graph is n k-colorable can − be done in O(2[k]n) time.

 22. If G = (V, E) is an undirected graph then let G = (V, E) be defined by (x, y) E iff (x, y) / E. ∈ ∈
 G is called the complement of G. Let HAMCGC be the set of graphs G such that either G or G has a Hamiltonian cycle. Show that HAMCGC is NP-complete. (Let HAMP be the set of all (H, a, b) such that H has a Hamiltonian Path that starts at a and ends at b. You may use the fact that HAMP is NP-complete.)

 23. (a) Let

 A = G either G or G has a Hamiltonian Cycle . { | }

 Either show A P or that A is NP-complete. ∈
 (b) Make up and solve similar problems to the one above where you take some property of graphs and ask if the graph or its compli- ment has it.

 71


-----

