#### Reinhard Diestel
## Graph Theory

##### Electronic Edition 2000

c Springer-Verlag New York 1997, 2000
_⃝_

This is an electronic version of the second (2000) edition of the above
Springer book, from their series Graduate Texts in Mathematics, vol. 173.
The cross-references in the text and in the margins are active links: click
on them to be taken to the appropriate page.

The printed edition of this book can be ordered from your bookseller, or
electronically from Springer through the Web sites referred to below.

Softcover $34.95, ISBN 0-387-98976-5
Hardcover $69.95, ISBN 0-387-95014-1

Further information (reviews, errata, free copies for lecturers etc.) and
electronic order forms can be found on

[http://www.math.uni-hamburg.de/home/diestel/books/graph.theory/](http://www.math.uni-hamburg.de/home/diestel/books/graph.theory/)
[http://www.springer-ny.com/supplements/diestel/](http://www.springer-ny.com/supplements/diestel/)


-----

### Preface

Almost two decades have passed since the appearance of those graph theory texts that still set the agenda for most introductory courses taught
today. The canon created by those books has helped to identify some
main fields of study and research, and will doubtless continue to influence
the development of the discipline for some time to come.
Yet much has happened in those 20 years, in graph theory no less
than elsewhere: deep new theorems have been found, seemingly disparate
methods and results have become interrelated, entire new branches have
arisen. To name just a few such developments, one may think of how
the new notion of list colouring has bridged the gulf between invariants such as average degree and chromatic number, how probabilistic
methods and the regularity lemma have pervaded extremal graph theory and Ramsey theory, or how the entirely new field of graph minors and
tree-decompositions has brought standard methods of surface topology
to bear on long-standing algorithmic graph problems.
Clearly, then, the time has come for a reappraisal: what are, today,
_the essential areas, methods and results that should form the centre of_
_an introductory graph theory course aiming to equip its audience for the_
_most likely developments ahead?_
I have tried in this book to offer material for such a course. In
view of the increasing complexity and maturity of the subject, I have
broken with the tradition of attempting to cover both theory and applications: this book offers an introduction to the theory of graphs as part
of (pure) mathematics; it contains neither explicit algorithms nor ‘real
world’ applications. My hope is that the potential for depth gained by
this restriction in scope will serve students of computer science as much
as their peers in mathematics: assuming that they prefer algorithms but
will benefit from an encounter with pure mathematics of some kind, it
seems an ideal opportunity to look for this close to where their heart lies!
In the selection and presentation of material, I have tried to ac

-----

introductory text should be lean and concentrate on the essential, so as
to offer guidance to those new to the field. As a graduate text, moreover,
it should get to the heart of the matter quickly: after all, the idea is to
convey at least an impression of the depth and methods of the subject.
On the other hand, it has been my particular concern to write with
sufficient detail to make the text enjoyable and easy to read: guiding
questions and ideas will be discussed explicitly, and all proofs presented
will be rigorous and complete.
A typical chapter, therefore, begins with a brief discussion of what
are the guiding questions in the area it covers, continues with a succinct
account of its classic results (often with simplified proofs), and then
presents one or two deeper theorems that bring out the full flavour of
that area. The proofs of these latter results are typically preceded by (or
interspersed with) an informal account of their main ideas, but are then
presented formally at the same level of detail as their simpler counterparts. I soon noticed that, as a consequence, some of those proofs came
out rather longer in print than seemed fair to their often beautifully
simple conception. I would hope, however, that even for the professional
reader the relatively detailed account of those proofs will at least help
to minimize reading time. . .
If desired, this text can be used for a lecture course with little or
no further preparation. The simplest way to do this would be to follow
the order of presentation, chapter by chapter: apart from two clearly
marked exceptions, any results used in the proof of others precede them
in the text.
Alternatively, a lecturer may wish to divide the material into an easy
basic course for one semester, and a more challenging follow-up course
for another. To help with the preparation of courses deviating from the
order of presentation, I have listed in the margin next to each proof the
reference numbers of those results that are used in that proof. These
references are given in round brackets: for example, a reference (4.1.2)
in the margin next to the proof of Theorem 4.3.2 indicates that Lemma
4.1.2 will be used in this proof. Correspondingly, in the margin next to
Lemma 4.1.2 there is a reference [ 4.3.2 ] (in square brackets) informing
the reader that this lemma will be used in the proof of Theorem 4.3.2.
Note that this system applies between different sections only (of the same
or of different chapters): the sections themselves are written as units and
best read in their order of presentation.
The mathematical prerequisites for this book, as for most graph
theory texts, are minimal: a first grounding in linear algebra is assumed
for Chapter 1.9 and once in Chapter 5.5, some basic topological concepts about the Euclidean plane and 3-space are used in Chapter 4, and
a previous first encounter with elementary probability will help with
Chapter 11. (Even here, all that is assumed formally is the knowledge


-----

text.) There are two areas of graph theory which I find both fascinating and important, especially from the perspective of pure mathematics
adopted here, but which are not covered in this book: these are algebraic
graph theory and infinite graphs.
At the end of each chapter, there is a section with exercises and
another with bibliographical and historical notes. Many of the exercises
were chosen to complement the main narrative of the text: they illustrate new concepts, show how a new invariant relates to earlier ones,
or indicate ways in which a result stated in the text is best possible.
Particularly easy exercises are identified by the superscript _[−], the more_
challenging ones carry a [+]. The notes are intended to guide the reader
on to further reading, in particular to any monographs or survey articles
on the theme of that chapter. They also offer some historical and other
remarks on the material presented in the text.
Ends of proofs are marked by the symbol □. Where this symbol is
found directly below a formal assertion, it means that the proof should
be clear after what has been said—a claim waiting to be verified! There
are also some deeper theorems which are stated, without proof, as background information: these can be identified by the absence of both proof
and □.
Almost every book contains errors, and this one will hardly be an
exception. I shall try to post on the Web any corrections that become
necessary. The relevant site may change in time, but will always be
accessible via the following two addresses:

[http://www.springer-ny.com/supplements/diestel/](http://www.springer-ny.com/supplements/diestel/)
http://www.springer.de/catalog/html-files/deutsch/math/3540609180.html

Please let me know about any errors you find.
Little in a textbook is truly original: even the style of writing and
of presentation will invariably be influenced by examples. The book that
no doubt influenced me most is the classic GTM graph theory text by
Bollob´as: it was in the course recorded by this text that I learnt my first
graph theory as a student. Anyone who knows this book well will feel
its influence here, despite all differences in contents and presentation.
I should like to thank all who gave so generously of their time,
knowledge and advice in connection with this book. I have benefited
particularly from the help of N. Alon, G. Brightwell, R. Gillett, R. Halin,
M. Hintz, A. Huck, I. Leader, T. �Luczak, W. Mader, V. R¨odl, A.D. Scott,
P.D. Seymour, G. Simonyi, M. Skoviera, R. Thomas, C. Thomassen and[ˇ]
P. Valtr. I am particularly grateful also to Tommy R. Jensen, who taught
me much about colouring and all I know about k-flows, and who invested immense amounts of diligence and energy in his proofreading of the
preliminary German version of this book.


-----

**About the second edition**

Naturally, I am delighted at having to write this addendum so soon after
this book came out in the summer of 1997. It is particularly gratifying
to hear that people are gradually adopting it not only for their personal
use but more and more also as a course text; this, after all, was my aim
when I wrote it, and my excuse for agonizing more over presentation
than I might otherwise have done.
There are two major changes. The last chapter on graph minors
now gives a complete proof of one of the major results of the RobertsonSeymour theory, their theorem that excluding a graph as a minor bounds
the tree-width if and only if that graph is planar. This short proof did
not exist when I wrote the first edition, which is why I then included a
short proof of the next best thing, the analogous result for path-width.
That theorem has now been dropped from Chapter 12. Another addition
in this chapter is that the tree-width duality theorem, Theorem 12.3.9,
now comes with a (short) proof too.
The second major change is the addition of a complete set of hints
for the exercises. These are largely Tommy Jensen’s work, and I am
grateful for the time he donated to this project. The aim of these hints
is to help those who use the book to study graph theory on their own,
but not to spoil the fun. The exercises, including hints, continue to be
intended for classroom use.
Apart from these two changes, there are a few additions. The most
noticable of these are the formal introduction of depth-first search trees
in Section 1.5 (which has led to some simplifications in later proofs) and
an ingenious new proof of Menger’s theorem due to B¨ohme, G¨oring and
Harant (which has not otherwise been published).
Finally, there is a host of small simplifications and clarifications
of arguments that I noticed as I taught from the book, or which were
pointed out to me by others. To all these I offer my special thanks.
The Web site for the book has followed me to

[http://www.math.uni-hamburg.de/home/diestel/books/graph.theory/](http://www.math.uni-hamburg.de/home/diestel/books/graph.theory/)

I expect this address to be stable for some time.
Once more, my thanks go to all who contributed to this second
edition by commenting on the first—and I look forward to further comments!

December 1999 _RD_


-----

### Contents

Preface . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . vii

###### 1. The Basics . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 1

1.1. Graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2

1.2. The degree of a vertex . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 4

1.3. Paths and cycles . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 6

1.4. Connectivity . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 9

1.5. Trees and forests . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 12

1.6. Bipartite graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 14

1.7. Contraction and minors . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 16

1.8. Euler tours . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 18

1.9. Some linear algebra . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20

1.10. Other notions of graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 25

Exercises . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 26

Notes . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 28

###### 2. Matching . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 29

2.1. Matching in bipartite graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 29

2.2. Matching in general graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 34

2.3. Path covers . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 39

Exercises . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 40


-----

###### 3. Connectivity . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 43

3.1. 2-Connected graphs and subgraphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 43
3.2. The structure of 3-connected graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . 45
3.3. Menger’s theorem . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 50
3.4. Mader’s theorem . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 56
3.5. Edge-disjoint spanning trees . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 58
3.6. Paths between given pairs of vertices . . . . . . . . . . . . . . . . . . . . . . . . . . . 61
Exercises . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 63
Notes . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 65

###### 4. Planar Graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 67

4.1. Topological prerequisites . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 68
4.2. Plane graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 70
4.3. Drawings . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 76
4.4. Planar graphs: Kuratowski’s theorem . . . . . . . . . . . . . . . . . . . . . . . . . . . 80
4.5. Algebraic planarity criteria . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 85
4.6. Plane duality . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 87
Exercises . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 89
Notes . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 92

###### 5. Colouring . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 95

5.1. Colouring maps and planar graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 96
5.2. Colouring vertices . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 98
5.3. Colouring edges . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 103
5.4. List colouring . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 105
5.5. Perfect graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 110
Exercises . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 117
Notes . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 120

###### 6. Flows . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 123

6.1. Circulations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 124
6.2. Flows in networks . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 125
6.3. Group-valued flows . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 128
6.4. k-Flows for small k . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 133
6.5. Flow-colouring duality . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 136
6.6. Tutte’s flow conjectures . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 140
Exercises . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 144


-----

###### 7. Substructures in Dense Graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 147

7.1. Subgraphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 148

7.2. Szemer´edi’s regularity lemma . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 153

7.3. Applying the regularity lemma . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 160

Exercises . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 165

Notes . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 166

###### 8. Substructures in Sparse Graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 169

8.1. Topological minors . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 170

8.2. Minors . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 179

8.3. Hadwiger’s conjecture . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 181

Exercises . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 184

Notes . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 186

###### 9. Ramsey Theory for Graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 189

9.1. Ramsey’s original theorems . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 190

9.2. Ramsey numbers . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 193

9.3. Induced Ramsey theorems . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 197

9.4. Ramsey properties and connectivity . . . . . . . . . . . . . . . . . . . . . . . . . . . . 207

Exercises . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 208

Notes . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 210

###### 10. Hamilton Cycles . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 213

10.1. Simple sufficient conditions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 213

10.2. Hamilton cycles and degree sequences . . . . . . . . . . . . . . . . . . . . . . . . . . . 216

10.3. Hamilton cycles in the square of a graph . . . . . . . . . . . . . . . . . . . . . . . . 218

Exercises . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 226

Notes . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 227

###### 11. Random Graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 229

11.1. The notion of a random graph . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 230

11.2. The probabilistic method . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 235

11.3. Properties of almost all graphs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 238

11.4. Threshold functions and second moments . . . . . . . . . . . . . . . . . . . . . . . 242

Exercises . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 247


-----

###### 12. Minors, Trees, and WQO . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 251

12.1. Well-quasi-ordering . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 251

12.2. The graph minor theorem for trees . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 253

12.3. Tree-decompositions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 255

12.4. Tree-width and forbidden minors . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 263

12.5. The graph minor theorem . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 274

Exercises . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 277

Notes . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 280

Hints for all the exercises. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 283

Index . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 299

Symbol index . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 311


-----

# 1 The Basics

This chapter gives a gentle yet concise introduction to most of the terminology used later in the book. Fortunately, much of standard graph
theoretic terminology is so intuitive that it is easy to remember; the few
terms better understood in their proper setting will be introduced later,
when their time has come.
Section 1.1 offers a brief but self-contained summary of the most
basic definitions in graph theory, those centred round the notion of a
graph. Most readers will have met these definitions before, or will have
them explained to them as they begin to read this book. For this reason,
Section 1.1 does not dwell on these definitions more than clarity requires:
its main purpose is to collect the most basic terms in one place, for easy
reference later.
From Section 1.2 onwards, all new definitions will be brought to life
almost immediately by a number of simple yet fundamental propositions.
Often, these will relate the newly defined terms to one another: the
question of how the value of one invariant influences that of another
underlies much of graph theory, and it will be good to become familiar
with this line of thinking early.
By N we denote the set of natural numbers, including zero. The set
Z/nZ of integers modulo n is denoted by Zn; its elements are written as Zn

_i := i + nZ. For a real number x we denote by ⌊x⌋_ the greatest integer
⩽ _x, and by ⌈x⌉_ the least integer ⩾ _x. Logarithms written as ‘log’ are_ _⌊x⌋, ⌈x⌉_
taken at base 2; the natural logarithm will be denoted by ‘ln’. A set log, ln
_A = { A1, . . ., Ak } of disjoint subsets of a set A is a partition of A if_ _partition_
_A =_ [�]i[k]=1 _[A][i][ and][ A][i][ ̸][=][ ∅]_ [for every][ i][. Another partition][ {][ A]1[′] _[, . . ., A][′]ℓ_ _[}][ of]_
_A refines the partition A if each A[′]i_ [is contained in some][ A][j][. By [][A][]][k][ we] [A][k]
denote the set of all k-element subsets of A. Sets with k elements will
be called k-sets; subsets with k elements are k-subsets. _k-set_


-----

###### 1.1 Graphs

_graph_ A graph is a pair G = (V, E) of sets satisfying E [V ][2]; thus, the ele_⊆_
ments of E are 2-element subsets of V . To avoid notational ambiguities,
we shall always assume tacitly that V _E =_ . The elements of V are the
_∩_ _∅_
_vertex_ _vertices (or nodes, or points) of the graph G, the elements of E are its_
_edge_ _edges (or lines). The usual way to picture a graph is by drawing a dot for_
each vertex and joining two of these dots by a line if the corresponding
two vertices form an edge. Just how these dots and lines are drawn is
considered irrelevant: all that matters is the information which pairs of
vertices form an edge and which do not.


5

4


7


1


3

2


_Fig. 1.1.1. The graph on V = { 1, . . ., 7 } with edge set_
_E = {{ 1, 2 }, { 1, 5 }, { 2, 5 }, { 3, 4 }, { 5, 7 }}_

_on_ A graph with vertex set V is said to be a graph on V . The vertex
_V (G), E(G)_ set of a graph G is referred to as V (G), its edge set as E(G). These
conventions are independent of any actual names of these two sets: the
vertex set W of a graph H = (W, F ) is still referred to as V (H), not as
_W_ (H). We shall not always distinguish strictly between a graph and its
vertex or edge set. For example, we may speak of a vertex v _[∈]_ _G (rather_
than v _[∈]_ _V (G)), an edge e_ _[∈]_ _G, and so on._
_order_ The number of vertices of a graph G is its order, written as _G_ ;
_|_ _|_
_|G|, ∥G∥_ its number of edges is denoted by ∥G∥. Graphs are finite or infinite
according to their order; unless otherwise stated, the graphs we consider
are all finite.
_∅_ For the empty graph (∅, ∅) we simply write ∅. A graph of order 0 or 1
_trivial_
is called trivial . Sometimes, e.g. to start an induction, trivial graphs can
_graph_
be useful; at other times they form silly counterexamples and become a
nuisance. To avoid cluttering the text with non-triviality conditions, we
shall mostly treat the trivial graphs, and particularly the empty graph,
_∅_
with generous disregard.
_incident_ A vertex v is incident with an edge e if v _[∈]_ _e; then e is an edge at v._
_ends_ The two vertices incident with an edge are its endvertices or ends, and
an edge joins its ends. An edge _x, y_ is usually written as xy (or yx).
_{_ _}_
If x _[∈]_ _X and y_ _[∈]_ _Y, then xy is an X–Y edge. The set of all X–Y edges_
_E(X, Y )_ in a set E is denoted by E(X, Y ); instead of E( _x_ _, Y ) and E(X,_ _y_ )
_{_ _}_ _{_ _}_
we simply write E(x, Y ) and E(X, y). The set of all the edges in E at a
( )


-----

Two vertices x, y of G are adjacent, or neighbours, if xy is an edge _adjacent_
of G. Two edges e = f are adjacent if they have an end in common. If all _neighbour_
_̸_
the vertices of G are pairwise adjacent, then G is complete. A complete _complete_
graph on n vertices is a K _[n]; a K_ [3] is called a triangle. _K[n]_
Pairwise non-adjacent vertices or edges are called independent.
_inde-_
More formally, a set of vertices or of edges is independent (or stable)
_pendent_
if no two of its elements are adjacent.
Let G = (V, E) and G[′] = (V _[′], E[′]) be two graphs. We call G and_
_G[′]_ _isomorphic, and write G ≃_ _G[′], if there exists a bijection ϕ: V →_ _V_ _[′]_ _≃_
with xy ∈ _E ⇔_ _ϕ(x)ϕ(y) ∈_ _E[′]_ for all x, y ∈ _V . Such a map ϕ is called_
_isomor-_
an isomorphism; if G = G[′], it is called an automorphism. We do not
_phism_
normally distinguish between isomorphic graphs. Thus, we usually write
_G = G[′]_ rather than G _G[′], speak of the complete graph on 17 vertices,_
_≃_
and so on. A map taking graphs as arguments is called a graph invariant _invariant_
if it assigns equal values to isomorphic graphs. The number of vertices
and the number of edges of a graph are two simple graph invariants; the
greatest number of pairwise adjacent vertices is another.

1


_G[′]_


4


6


3


4

5
_G_


3


5


1


4

5


3


2

6

5 3

_G ∪_ _G[′]_ _G_ _−_ _G[′]_ _G ∩_ _G[′]_


_Fig. 1.1.2. Union, difference and intersection; the vertices 2,3,4_
induce (or span) a triangle in G ∪ _G[′]_ but not in G

We set G ∪ _G[′]_ := (V ∪ _V_ _[′], E ∪_ _E[′]) and G ∩_ _G[′]_ := (V ∩ _V_ _[′], E ∩_ _E[′])._ _G ∩_ _G[′]_
If G ∩ _G[′]_ = ∅, then G and G[′] are disjoint. If V _[′]_ _⊆_ _V and E[′]_ _⊆_ _E, then_ _subgraph_
_G[′]_ is a subgraph of G (and G a supergraph of G[′]), written as G[′] _⊆_ _G._ _G[′]_ _⊆_ _G_
Less formally, we say that G contains G[′].
If G[′] _⊆_ _G and G[′]_ contains all the edges xy _[∈]_ _E with x, y_ _[∈]_ _V_ _[′], then_
_induced_
_G[′]_ is an induced subgraph of G; we say that V _[′]_ _induces or spans G[′]_ in G, _subgraph_
and write G[′] =: G [ V _[′]_ ]. Thus if U ⊆ _V is any set of vertices, then G [ U ]_ _G [ U ]_
denotes the graph on U whose edges are precisely the edges of G with
both ends in U . If H is a subgraph of G, not necessarily induced, we
abbreviate G [ V (H) ] to G [ H ]. Finally, G[′] _⊆_ _G is a spanning subgraph_ _spanning_


-----

_G_ _G[′]_ _G[′′]_

_Fig. 1.1.3. A graph G with subgraphs G[′]_ and G[′′]:
_G[′]_ is an induced subgraph of G, but G[′′] is not

_−_ If U is any set of vertices (usually of G), we write G − _U for_
_G [ V ∖_ _U ]. In other words, G_ _−_ _U is obtained from G by deleting all the_
vertices in U _V and their incident edges. If U =_ _v_ is a singleton,
_∩_ _{_ _}_
we write G − _v rather than G −{ v }. Instead of G −_ _V (G[′]) we simply_
+ write G − _G[′]. For a subset F of [V ][2]_ we write G − _F := (V, E ∖_ _F_ ) and
_G + F := (V, E_ _F_ ); as above, G _e_ and G + _e_ are abbreviated to
_∪_ _−{_ _}_ _{_ _}_
_edge-_
_G_ _e and G + e. We call G edge-maximal with a given graph property_
_maximal_ _−_
if G itself has the property but no graph G + xy does, for non-adjacent
vertices x, y _[∈]_ _G._
_minimal_ More generally, when we call a graph minimal or maximal with some
_maximal_ property but have not specified any particular ordering, we are referring
to the subgraph relation. When we speak of minimal or maximal sets of
vertices or edges, the reference is simply to set inclusion.
_G ∗_ _G[′]_ If G and G[′] are disjoint, we denote by G ∗ _G[′]_ the graph obtained
_comple-_ from G ∪ _G[′]_ by joining all the vertices of G to all the vertices of G[′]. For
example, K [2] _K_ [3] = K [5]. The complement G of G is the graph on V
_ment G_ _∗_
with edge set [V ][2] ∖ _E. The line graph L(G) of G is the graph on E in_
_line graph_
_L(G)_ which x, y _[∈]_ _E are adjacent as vertices if and only if they are adjacent_
as edges in G.

_G_ _G_

_Fig. 1.1.4. A graph isomorphic to its complement_

###### 1.2 The degree of a vertex

Let G = (V, E) be a (non-empty) graph. The set of neighbours of a
_N_ (v) vertex v in G is denoted by NG(v), or briefly by N (v).[1] More generally

1 Here, as elsewhere, we drop the index referring to the underlying graph if the


-----

for U ⊆ _V, the neighbours in V ∖_ _U of vertices in U are called neighbours_
_of U_ ; their set is denoted by N (U ).
The degree (or valency) dG(v) = d(v) of a vertex v is the number _degree d(v)_
_E(v)_ of edges at v; by our definition of a graph,[2] this is equal to the
_|_ _|_
number of neighbours of v. A vertex of degree 0 is isolated . The number _isolated_
_δ(G) := min { d(v) | v ∈_ _V } is the minimum degree of G, the number_ _δ(G)_
∆(G) := max { d(v) | v _[∈]_ _V } its maximum degree. If all the vertices_ ∆(G)
of G have the same degree k, then G is k-regular, or simply regular . A _regular_
3-regular graph is called cubic. _cubic_
The number

1

�

_d(G) :=_ _d(v)_

_|V |_ _v ∈V_ _d(G)_

_average_
is the average degree of G. Clearly, _degree_

_δ(G) ⩽_ _d(G) ⩽_ ∆(G) .

The average degree quantifies globally what is measured locally by the
vertex degrees: the number of edges of G per vertex. Sometimes it will
be convenient to express this ratio directly, as ε(G) := _E_ _/_ _V_ . _ε(G)_
_|_ _|_ _|_ _|_
The quantities d and ε are, of course, intimately related. Indeed,
if we sum up all the vertex degrees in G, we count every edge exactly
twice: once from each of its ends. Thus

_|E| =_ [1]2 � _d(v) =_ [1]2 _[d][(][G][)][ · |][V][ |][,]_

_v ∈V_


and therefore
_ε(G) =_ [1]2 _[d][(][G][)][ .]_

**Proposition 1.2.1. The number of vertices of odd degree in a graph is** [ 10.3.3 ]
_always even._

_Proof ._ A graph on V has 12 �v ∈V _[d][(][v][) edges, so][ �]_ _[d][(][v][) is an even]_
number. 

If a graph has large minimum degree, i.e. everywhere, locally, many
edges per vertex, it also has many edges per vertex globally: ε(G) =
1
2 _[d][(][G][)][ ⩾]_ [1]2 _[δ][(][G][). Conversely, of course, its average degree may be large]_

even when its minimum degree is small. However, the vertices of large
degree cannot be scattered completely among vertices of small degree: as
the next proposition shows, every graph G has a subgraph whose average
degree is no less than the average degree of G, and whose minimum
degree is more than half its average degree:


-----

[ 3.6.1 ] **Proposition 1.2.2. Every graph G with at least one edge has a sub-**
_graph H with δ(H) > ε(H) ⩾_ _ε(G)._

_Proof . To construct H from G, let us try to delete vertices of small_
degree one by one, until only vertices of large degree remain. Up to
which degree d(v) can we afford to delete a vertex v, without lowering ε?
Clearly, up to d(v) = ε : then the number of vertices decreases by 1
and the number of edges by at most ε, so the overall ratio ε of edges to
vertices will not decrease.
Formally, we construct a sequence G = G0 ⊇ _G1 ⊇_ _. . . of induced_
subgraphs of G as follows. If Gi has a vertex vi of degree d(vi) ⩽ _ε(Gi),_
we let Gi+1 := Gi _vi; if not, we terminate our sequence and set_
_−_
_H := Gi. By the choices of vi we have ε(Gi+1) ⩾_ _ε(Gi) for all i, and_
hence ε(H) ⩾ _ε(G)._
What else can we say about the graph H? Since ε(K [1]) = 0 < ε(G),
none of the graphs in our sequence is trivial, so in particular H = . The
_̸_ _∅_
fact that H has no vertex suitable for deletion thus implies δ(H) > ε(H),
as claimed.       
###### 1.3 Paths and cycles

_path_ A path is a non-empty graph P = (V, E) of the form

_V = { x0, x1, . . ., xk }_ _E = { x0x1, x1x2, . . ., xk−1xk },_

where the xi are all distinct. The vertices x0 and xk are linked by P and
are called its ends; the vertices x1, . . ., xk−1 are the inner vertices of P .
_length_ The number of edges of a path is its length, and the path of length k is
_P_ _[k]_ denoted by P _[k]. Note that k is allowed to be zero; thus, P_ [0] = K [1].

_G_ _P_

_Fig. 1.3.1. A path P = P_ [6] in G

We often refer to a path by the natural sequence of its vertices,[3]

writing, say, P = x0x1 . . . xk and calling P a path from x0 to xk (as well
as between x0 and xk).

3 More precisely, by one of the two natural sequences: x0 . . . xk and xk . . . x0
denote the same path. Still, it often helps to fix one of these two orderings of V (P )
notationally: we may then speak of things like the ‘first’ vertex on P with a certain


-----

For 0 ⩽ _i ⩽_ _j ⩽_ _k we write_ _xPy,_ _P[˚]_

_Pxi := x0 . . . xi_
_xiP := xi . . . xk_
_xiPxj := xi . . . xj_
and
_P˚ := x1 . . . xk−1_
_P˚xi := x0 . . . xi−1_
˚xiP := xi+1 . . . xk
˚xiP˚xj := xi+1 . . . xj−1

for the appropriate subpaths of P . We use similar intuitive notation for
the concatenation of paths; for example, if the union Px _xQy_ _yR of_
_∪_ _∪_
three paths is again a path, we may simply denote it by PxQyR. _PxQyR_


_z_


_z_


_x_


_Q_


_x_ _xPyQz_


_Fig. 1.3.2. Paths P_, Q and xPyQz

Given sets A, B of vertices, we call P = x0 . . . xk an A–B path if _A–B path_
_V (P_ ) ∩ _A = { x0 } and V (P_ ) ∩ _B = { xk }. As before, we write a–B_ _inde-_
path rather than _a_ –B path, etc. Two or more paths are independent
_{_ _}_ _pendent_
if none of them contains an inner vertex of another. Two a–b paths, for
instance, are independent if and only if a and b are their only common
vertices.
Given a graph H, we call P an H-path if P is non-trivial and meets _H-path_
_H exactly in its ends. In particular, the edge of any H-path of length 1_
is never an edge of H.
If P = x0 . . . xk−1 is a path and k ⩾ 3, then the graph C :=
_P + xk−1x0 is called a cycle. As with paths, we often denote a cycle_ _cycle_
by its (cyclic) sequence of vertices; the above cycle C might be written
as x0 . . . xk−1x0. The length of a cycle is its number of edges (or vertices); _length_
the cycle of length k is called a k-cycle and denoted by C _[k]._ _C[k]_
The minimum length of a cycle (contained) in a graph G is the girth _girth g(G)_
_g(G) of G; the maximum length of a cycle in G is its circumference. (If_ _circum-_
_G does not contain a cycle, we set the former to_, the latter to zero.) _ference_
_∞_
An edge which joins two vertices of a cycle but is not itself an edge of _chord_
the cycle is a chord of that cycle. Thus, an induced cycle in G, a cycle in
_induced_
( )


-----

_Fig. 1.3.3. A cycle C_ [8] with chord xy, and induced cycles C [6], C [4]

If a graph has large minimum degree, it contains long paths and
cycles:

[ 3.6.1 ] **Proposition 1.3.1. Every graph G contains a path of length δ(G) and**
_a cycle of length at least δ(G) + 1 (provided that δ(G) ⩾_ 2).

_Proof . Let x0 . . . xk be a longest path in G. Then all the neighbours of_
_xk lie on this path (Fig. 1.3.4). Hence k ⩾_ _d(xk) ⩾_ _δ(G). If i < k is_
minimal with xixk ∈ _E(G), then xi . . . xkxi is a cycle of length at least_
_δ(G) + 1._       
_x0_ _xi_ _xk_

_Fig. 1.3.4. A longest path x0 . . . xk, and the neighbours of xk_

Minimum degree and girth, on the other hand, are not related (unless we fix the number of vertices): as we shall see in Chapter 11, there
are graphs combining arbitrarily large minimum degree with arbitrarily
large girth.
_distance_
_dG(x, y)_ The distance dG(x, y) in G of two vertices x, y is the length of a
shortest x–y path in G; if no such path exists, we set d(x, y) := . The
_∞_
greatest distance between any two vertices in G is the diameter of G,
_diameter_
denoted by diam(G). Diameter and girth are, of course, related:
diam(G)

**Proposition 1.3.2. Every graph G containing a cycle satisfies g(G) ⩽**
2 diam(G) + 1.

_Proof . Let C be a shortest cycle in G. If g(G) ⩾_ 2 diam(G) + 2, then
_C has two vertices whose distance in C is at least diam(G) + 1. In G,_
these vertices have a lesser distance; any shortest path P between them
is therefore not a subgraph of C. Thus, P contains a C-path xPy.
Together with the shorter of the two x–y paths in C, this path xPy


-----

A vertex is central in G if its greatest distance from any other ver-� _central_

tex is as small as possible. This distance is the radius of G, denoted� _radius_

by rad(G). Thus, formally, rad(G) = minx∈V (G) maxy ∈V (G) dG(x, y).� rad(G)

As one easily checks (exercise), we have

rad(G) ⩽ diam(G) ⩽ 2 rad(G) .

Diameter and radius are not directly related to the minimum or

average degree: a graph can combine large minimum degree with large
diameter, or small average degree with small diameter (examples?).

The maximum degree behaves differently here: a graph of large

order can only have small radius and diameter if its maximum degree
is large. This connection is quantified very roughly in the following

proposition:

[ 9.4.1 ]
**Proposition 1.3.3. A graph G of radius at most k and maximum degree**

[ 9.4.2 ]

_at most d has no more than 1 + kd[k]_ _vertices._

_Proof ._ Let z be a central vertex in G, and let Di denote the set of

vertices of G at distance i from z. Then V (G) = [�]i[k]=0 _[D][i][, and][ |][D][0][|][ = 1.]_

Since ∆(G) ⩽ _d, we have |Di| ⩽_ _d |Di−1| for i = 1, . . ., k, and thus_
_|Di| ⩽_ _d[i]_ by induction. Adding up these inequalities we obtain





_|G| ⩽_ 1 +


_k_
�

_i=1_


_d[i]_ ⩽ 1 + kd[k].


A walk (of length k) in a graph G is a non-empty alternating se-� _walk_

quence v0e0v1e1 . . . ek−1vk of vertices and edges in G such that ei =
_{ vi, vi+1 } for all i < k. If v0 = vk, the walk is closed_ . If the vertices
in a walk are all distinct, it defines an obvious path in G. In general,
every walk between two vertices contains[4] a path between these vertices
(proof?).

###### 1.4 Connectivity

A non-empty graph G is called connected if any two of its vertices are� _connected_

linked by a path in G. If U _V (G) and G [ U ] is connected, we also call_
_⊆_
_U itself connected (in G)._

[ 1.5.2 ]
**Proposition 1.4.1. The vertices of a connected graph G can always be**

_enumerated, say as v1, . . ., vn, so that Gi := G [ v1, . . ., vi ] is connected_
_for every i._

4 We shall often use terms defined for graphs also for walks, as long as their


-----

_Proof . Pick any vertex as v1, and assume inductively that v1, . . ., vi_
have been chosen for some i < |G|. Now pick a vertex v _[∈]_ _G −_ _Gi. As G_
is connected, it contains a v–v1 path P . Choose as vi+1 the last vertex
of P in G − _Gi; then vi+1 has a neighbour in Gi. The connectedness of_
every Gi follows by induction on i.       
Let G = (V, E) be a graph. A maximal connected subgraph of G
_component_ is called a component of G. Note that a component, being connected, is
always non-empty; the empty graph, therefore, has no components.

_Fig. 1.4.1. A graph with three components, and a minimal_
spanning connected subgraph in each component

If A, B _V and X_ _V_ _E are such that every A–B path in_
_⊆_ _⊆_ _∪_
_separate_ _G contains a vertex or an edge from X, we say that X separates the_
sets A and B in G. This implies in particular that A _B_ _X. More_
_∩_ _⊆_
generally we say that X separates G, and call X a separating set in G,
if X separates two vertices of G _X in G. A vertex which separates_
_−_
_cutvertex_ two other vertices of the same component is a cutvertex, and an edge
_bridge_ separating its ends is a bridge. Thus, the bridges in a graph are precisely
those edges that do not lie on any cycle.

_v_ _x_ _y_ _w_

_e_

_Fig. 1.4.2. A graph with cutvertices v, x, y, w and bridge e = xy_

_k-connected_ _G is called k-connected (for k_ _[∈]_ N) if |G| > k and G _−_ _X is connected_
for every set X _V with_ _X_ _< k. In other words, no two vertices of G_
_⊆_ _|_ _|_
are separated by fewer than k other vertices. Every (non-empty) graph
is 0-connected, and the 1-connected graphs are precisely the non-trivial
connected graphs. The greatest integer k such that G is k-connected
_connectivity_
is the connectivity κ(G) of G. Thus, κ(G) = 0 if and only if G is
_κ(G)_
disconnected or a K [1], and κ(K _[n]) = n −_ 1 for all n ⩾ 1.
If _G_ _> 1 and G_ _F is connected for every set F_ _E of fewer_
_|_ _|_ _−_ _⊆_
_ℓ-edge-_

|v x y e|Col2|w|
|---|---|---|


-----

_G_ _H_

_Fig. 1.4.3. The octahedron G (left) with κ(G) = λ(G) = 4,_
and a graph H with κ(H) = 2 but λ(H) = 4

such that G is ℓ-edge-connected is the edge-connectivity λ(G) of G. In _edge-_
particular, we have λ(G) = 0 if G is disconnected. _connectivity_
For every non-trivial graph G we have _λ(G)_

_κ(G) ⩽_ _λ(G) ⩽_ _δ(G)_

(exercise), so in particular high connectivity requires a large minimum
degree. Conversely, large minimum degree does not ensure high connectivity, not even high edge-connectivity (examples?). It does, however,
imply the existence of a highly connected subgraph:

**Theorem 1.4.2. (Mader 1972)**

[ 8.1.1 ]
_Every graph of average degree at least 4k has a k-connected subgraph._

[ 11.2.3 ]
_Proof . For k ∈_ _{ 0, 1 } the assertion is trivial; we consider k ⩾_ 2 and a
graph G = (V, E) with _V_ =: n and _E_ =: m. For inductive reasons it
_|_ _|_ _|_ _|_
will be easier to prove the stronger assertion that G has a k-connected
subgraph whenever

(i) n ⩾ 2k − 1 and

(ii) m ⩾ (2k − 3)(n − _k + 1) + 1._

(This assertion is indeed stronger, i.e. (i) and (ii) follow from our assumption of d(G) ⩾ 4k: (i) holds since n > ∆(G) ⩾ _d(G) ⩾_ 4k, while
(ii) follows from m = [1]2 _[d][(][G][)][n][ ⩾]_ [2][kn][.)]

We apply induction on n. If n = 2k − 1, then k = [1]2 [(][n][ + 1), and]

hence m ⩾ [1]2 _[n][(][n]_ _[−]_ [1) by (ii). Thus][ G][ =][ K] _[n][ ⊇]_ _[K]_ _[k][+1][, proving our claim.]_

We now assume that n ⩾ 2k. If v is a vertex with d(v) ⩽ 2k − 3, we can
apply the induction hypothesis to G _v and are done. So we assume that_
_−_
_δ(G) ⩾_ 2k − 2. If G is k-connected, there is nothing to show. We may
therefore assume that G has the form G = G1 ∪ _G2 with |G1 ∩_ _G2| < k_
and |G1|, |G2| < n. As every edge of G lies in G1 or in G2, G has no edge
between G1 _G2 and G2_ _G1. Since each vertex in these subgraphs has_
_−_ _−_
at least δ(G) ⩾ 2k − 2 neighbours, we have |G1|, |G2| ⩾ 2k − 1. But then

|Col1|Col2|
|---|---|


-----

(completing the proof): if neither does, we have

_∥Gi∥_ ⩽ (2k − 3)(|Gi| − _k + 1)_

for i = 1, 2, and hence

_m ⩽_ _∥G1∥_ + ∥G2∥

⩽ (2k − 3)�|G1| + |G2| − 2k + 2�

⩽ (2k − 3)(n − _k + 1)_ (by |G1 ∩ _G2| ⩽_ _k −_ 1)

contradicting (ii).       
###### 1.5 Trees and forests

_forest_ An acyclic graph, one not containing any cycles, is called a forest. A con_tree_ nected forest is called a tree. (Thus, a forest is a graph whose components
_leaf_ are trees.) The vertices of degree 1 in a tree are its leaves. Every nontrivial tree has at least two leaves—take, for example, the ends of a
longest path. This little fact often comes in handy, especially in induction proofs about trees: if we remove a leaf from a tree, what remains is
still a tree.

_Fig. 1.5.1. A tree_

[ 1.6.1 ]

[ 1.9.6 ] **Theorem 1.5.1. The following assertions are equivalent for a graph T** _:_

[ 4.2.7 ]
(i) T is a tree;
(ii) any two vertices of T are linked by a unique path in T _;_
(iii) T is minimally connected, i.e. T is connected but T _e is discon-_
_−_
_nected for every edge e ∈_ _T_ _;_
(iv) T is maximally acyclic, i.e. T contains no cycle but T + xy does,


-----

The proof of Theorem 1.5.1 is straightforward, and a good exercise
for anyone not yet familiar with all the notions it relates. Extending our
notation for paths from Section 1.3, we write xTy for the unique path _xTy_
in a tree T between two vertices x, y (see (ii) above).
A frequently used application of Theorem 1.5.1 is that every connected graph contains a spanning tree: by the equivalence of (i) and (iii),
any minimal connected spanning subgraph will be a tree. Figure 1.4.1
shows a spanning tree in each of the three components of the graph
depicted.

**Corollary 1.5.2. The vertices of a tree can always be enumerated, say**
_as v1, . . ., vn, so that every vi with i ⩾_ 2 has a unique neighbour in
_{ v1, . . ., vi−1 }._

_Proof . Use the enumeration from Proposition 1.4.1._ - (1.4.1)

[ 1.9.6 ]
**Corollary 1.5.3. A connected graph with n vertices is a tree if and** [ 3.5.1 ]

_only if it has n_ 1 edges. [ 3.5.4 ]
_−_

[ 4.2.7 ]

_Proof ._ Induction on i shows that the subgraph spanned by the first [ 8.2.2 ]
_i vertices in Corollary 1.5.2 has i_ 1 edges; for i = n this proves the
_−_
forward implication. Conversely, let G be any connected graph with n
vertices and n − 1 edges. Let G[′] be a spanning tree in G. Since G[′] has
_n −_ 1 edges by the first implication, it follows that G = G[′]. 
[ 9.2.1 ]
**Corollary 1.5.4. If T is a tree and G is any graph with δ(G) ⩾** _|T_ _|−_ 1, [ 9.2.3 ]
_then T_ _G, i.e. G has a subgraph isomorphic to T_ _._
_⊆_

_Proof . Find a copy of T in G inductively along its vertex enumeration_
from Corollary 1.5.2. 
Sometimes it is convenient to consider one vertex of a tree as special;
such a vertex is then called the root of this tree. A tree with a fixed root _root_
is a rooted tree. Choosing a root r in a tree T imposes a partial ordering
on V (T ) by letting x ⩽ _y if x_ _[∈]_ _rTy. This is the tree-order on V (T_ ) _tree-order_
associated with T and r. Note that r is the least element in this partial
order, every leaf x = r of T is a maximal element, the ends of any edge
_̸_
of T are comparable, and every set of the form { x | x ⩽ _y } (where y_
is any fixed vertex) is a chain, a set of pairwise comparable elements. _chain_
(Proofs?)
A rooted tree T contained in a graph G is called normal in G if _normal tree_
the ends of every T -path in G are comparable in the tree-order of T .
If T spans G, this amounts to requiring that two vertices of T must be
comparable whenever they are adjacent in G; see Figure 1.5.2. Normal
spanning trees are also called depth-first search trees, because of the way


-----

_G_

_T_

_r_

_Fig. 1.5.2. A depth-first search tree with root r_

Normal spanning trees provide a simple but powerful structural tool
in graph theory. And they always exist:

[ 6.5.3 ] **Proposition 1.5.5. Every connected graph contains a normal spanning**
_tree, with any specified vertex as its root._

_Proof . Let G be a connected graph and r_ _[∈]_ _G any specified vertex. Let T_
be a maximal normal tree with root r in G; we show that V (T ) = V (G).
Suppose not, and let C be a component of G _T_ . As T is normal,
_−_
_N_ (C) is a chain in T . Let x be its greatest element, and let y ∈ _C be_
adjacent to x. Let T _[′]_ be the tree obtained from T by joining y to x; the
tree-order of T _[′]_ then extends that of T . We shall derive a contradiction
by showing that T _[′]_ is also normal in G.
Let P be a T _[′]-path in G. If the ends of P both lie in T_, then they
are comparable in the tree-order of T (and hence in that of T _[′]), because_
then P is also a T -path and T is normal in G by assumption. If not,
then y is one end of P, so P lies in C except for its other end z, which
lies in N (C). Then z ⩽ _x, by the choice of x. For our proof that y and_
_z are comparable it thus suffices to show that x < y, i.e. that x ∈_ _rT_ _[′]y._
This, however, is clear since y is a leaf of T _[′]_ with neighbour x.       
###### 1.6 Bipartite graphs

_r-partite_ Let r ⩾ 2 be an integer. A graph G = (V, E) is called r-partite if
_V admits a partition into r classes such that every edge has its ends_
in different classes: vertices in the same partition class must not be
_bipartite_ adjacent. Instead of ‘2-partite’ one usually says bipartite.
An r-partite graph in which every two vertices from different par_complete_
tition classes are adjacent is called complete; the complete r-partite
_r partite_


-----

_K2,2,2 = K2[3]_


_Fig. 1.6.1. Two 3-partite graphs_

complete r-partite graph K _[n][1]_ _∗_ _. . . ∗_ _K_ _[n][r]_ is denoted by Kn1,...,nr ; if _Kn1,...,nr_

_n1 = . . . = nr =: s, we abbreviate this to Ks[r][. Thus,][ K]s[r]_ [is the complete�] _Ks[r]_

_r-partite graph in which every partition class contains exactly s ver-_
tices.[5] (Figure 1.6.1 shows the example of the octahedron K2[3][; compare]

its drawing with that in Figure 1.4.3.) Graphs of the form K1,n are

called stars.� _star_

= =


_Fig. 1.6.2. Three drawings of the bipartite graph K3,3 = K3[2]_

Clearly, a bipartite graph cannot contain an odd cycle, a cycle of odd� _odd cycle_

length. In fact, the bipartite graphs are characterized by this property:

[ 5.3.1 ]
**Proposition 1.6.1. A graph is bipartite if and only if it contains no**

[ 6.4.2 ]

_odd cycle._

_Proof . Let G = (V, E) be a graph without odd cycles; we show that G is_
(1.5.1)

bipartite. Clearly a graph is bipartite if all its components are bipartite
or trivial, so we may assume that G is connected. Let T be a spanning
tree in G, pick a root r _[∈]_ _T_, and denote the associated tree-order on V
by ⩽T . For each v _[∈]_ _V, the unique path rTv has odd or even length._
This defines a bipartition of V ; we show that G is bipartite with this
partition.

Let e = xy be an edge of G. If e _[∈]_ _T_, with x <T y say, then

_rTy = rTxy and so x and y lie in different partition classes. If e /[∈]_ _T_
then Ce := xTy + e is a cycle (Fig. 1.6.3), and by the case treated
already the vertices along xTy alternate between the two classes. Since
_Ce is even by assumption, x and y again lie in different classes.�_ 

5 Note that we obtain a Ksr [if we replace each vertex of a][ K][r][ by an independent]


-----

_Fig. 1.6.3. The cycle Ce in T + e_

###### 1.7 Contraction and minors

In Section 1.1 we saw two fundamental containment relations between
graphs: the subgraph relation, and the ‘induced subgraph’ relation. In
this section we meet another: the minor relation.
_G/e_ Let e = xy be an edge of a graph G = (V, E). By G/e we denote the
_contraction_ graph obtained from G by contracting the edge e into a new vertex ve,
which becomes adjacent to all the former neighbours of x and of y. Formally, G/e is a graph (V _[′], E[′]) with vertex set V_ _[′]_ := (V ∖ _{ x, y })_ _∪{ ve }_
_ve_ (where ve is the ‘new’ vertex, i.e. ve /[∈] _V ∪_ _E) and edge set_

� �
_E[′]_ := _vw ∈_ _E | { v, w } ∩{ x, y } = ∅_

� �
_∪_ _vew | xw_ _[∈]_ _E ∖_ _{ e } or yw_ _[∈]_ _E ∖_ _{ e }_ _._

_x_

_ve_
_e_


_y_


_G_ _G/e_

_Fig. 1.7.1. Contracting the edge e = xy_


More generally, if X is another graph and { Vx | x ∈ _V (X) } is a_
partition of V into connected subsets such that, for any two vertices
_x, y_ _[∈]_ _X, there is a Vx–Vy edge in G if and only if xy_ _[∈]_ _E(X), we call_
_MX_ _G an MX and write[6]_ _G = MX (Fig. 1.7.2). The sets Vx are the branch_
_branch sets_ _sets of this MX. Intuitively, we obtain X from G by contracting every_

6 Thus formally, the expression MX—where M stands for ‘minor’; see below—
refers to a whole class of graphs, and G = MX means (with slight abuse of notation)


-----

_z_


_x_


_X_


_Y_ _Vx_


_G_


_Fig. 1.7.2. Y ⊇_ _G = MX, so X is a minor of Y_

branch set to a single vertex and deleting any ‘parallel edges’ or ‘loops’
that may arise.
If Vx = U ⊆ _V is one of the branch sets above and every other_
branch set consists just of a single vertex, we also write G/U for the _G/U_
graph X and vU for the vertex x ∈ _X to which U contracts, and think_ _vU_
of the rest of X as an induced subgraph of G. The contraction of a
single edge uu[′] defined earlier can then be viewed as the special case of
_U = { u, u[′]_ _}._

**Proposition 1.7.1. G is an MX if and only if X can be obtained**
_from G by a series of edge contractions, i.e. if and only if there are_
_graphs G0, . . ., Gn and edges ei_ _[∈]_ _Gi such that G0 = G, Gn ≃_ _X, and_
_Gi+1 = Gi/ei for all i < n._

_Proof . Induction on |G| −|X|._ 
If G = MX is a subgraph of another graph Y, we call X a minor of Y
and write X ≼ _Y . Note that every subgraph of a graph is also its minor;_ _minor; ≼_
in particular, every graph is its own minor. By Proposition 1.7.1, any
minor of a graph can be obtained from it by first deleting some vertices
and edges, and then contracting some further edges. Conversely, any
graph obtained from another by repeated deletions and contractions (in
any order) is its minor: this is clear for one deletion or contraction, and
follows for several from the transitivity of the minor relation (Proposition
1.7.3).
If we replace the edges of X with independent paths between their
ends (so that none of these paths has an inner vertex on another path
_subdivision_
or in X), we call the graph G obtained a subdivision of X and write
_TX_
_G = TX.[7]_ If G = TX is the subgraph of another graph Y, then X is a
_topological_
_topological minor of Y (Fig. 1.7.3)._
_minor_

7 So again TX denotes an entire class of graphs: all those which, viewed as a
topological space in the obvious way, are homeomorphic to X. The T in TX stands


-----

_G_ _X_
_Y_

_Fig. 1.7.3. Y ⊇_ _G = TX, so X is a topological minor of Y_

If G = TX, we view V (X) as a subset of V (G) and call these vertices
_branch_
the branch vertices of G; the other vertices of G are its subdividing
_vertices_
_vertices. Thus, all subdividing vertices have degree 2, while the branch_
vertices retain their degree from X.

[ 4.4.2 ] **Proposition 1.7.2.**

[ 8.3.1 ]
(i) Every TX is also an MX (Fig. 1.7.4); thus, every topological
_minor of a graph is also its (ordinary) minor._

(ii) If ∆(X) ⩽ 3, then every MX contains a TX; thus, every minor
_with maximum degree at most 3 of a graph is also its topological_
_minor._         
_Fig. 1.7.4. A subdivision of K_ [4] viewed as an MK [4]

[ 12.4.1 ] **Proposition 1.7.3. The minor relation ≼** _and the topological-minor_
_relation are partial orderings on the class of finite graphs, i.e. they are_
_reflexive, antisymmetric and transitive._       
###### 1.8 Euler tours

Any mathematician who happens to find himself in the East Prussian
city of K¨onigsberg (and in the 18th century) will lose no time to follow the


-----

_Fig. 1.8.1. The bridges of K¨onigsberg (anno 1736)_

the old city that traverses each of the bridges shown in Figure 1.8.1
exactly once.
Thus inspired,[8] let us call a closed walk in a graph an Euler tour if
it traverses every edge of the graph exactly once. A graph is Eulerian if _Eulerian_
it admits an Euler tour.

_Fig. 1.8.2. A graph formalizing the bridge problem_

**Theorem 1.8.1. (Euler 1736)**

[ 2.1.5 ]
_A connected graph is Eulerian if and only if every vertex has even degree._

[ 10.3.3 ]
_Proof . The degree condition is clearly necessary: a vertex appearing k_
times in an Euler tour (or k + 1 times, if it is the starting and finishing
vertex and as such counted twice) must have degree 2k.

8 Anyone to whom such inspiration seems far-fetched, even after contemplating


-----

Conversely, let G be a connected graph with all degrees even, and
let

_W = v0e0 . . . eℓ−1vℓ_

be a longest walk in G using no edge more than once. Since W cannot
be extended, it already contains all the edges at vℓ. By assumption, the
number of such edges is even. Hence vℓ = v0, so W is a closed walk.
Suppose W is not an Euler tour. Then G has an edge e outside W
but incident with a vertex of W, say e = uvi. (Here we use the connectedness of G, as in the proof of Proposition 1.4.1.) Then the walk

_ueviei . . . eℓ−1vℓe0 . . . ei−1vi_

is longer than W, a contradiction.      
###### 1.9 Some linear algebra

_vertex_ Let G = (V, E) be a graph with n vertices and m edges, say V =
_spaceV(G)_ _{vector space over the 2-element field v1, . . ., vn } and E = { e1, . . ., em } F. The2 = { vertex space 0, 1 } of all functions V(G) of G V → is theF2._
Every element of (G) corresponds naturally to a subset of V, the set of
_V_
those vertices to which it assigns a 1, and every subset of V is uniquely
represented in (G) by its indicator function. We may thus think of
_V_
+ _V(G) as the power set of V made into a vector space: the sum U + U_ _[′]_
of two vertex sets U, U _[′]_ _⊆_ _V is their symmetric difference (why?), and_
_U =_ _U for all U_ _V . The zero in_ (G), viewed in this way, is the
_−_ _⊆_ _V_
empty (vertex) set ∅. Since { { v1 }, . . ., { vn } } is a basis of V(G), its
_standard basis, we have dim_ (G) = n.
_V_
In the same way as above, the functions E → F2 form the edge
_edge space_
_space_ (G) of G: its elements are the subsets of E, vector addition
_E(G)_ _E_
amounts to symmetric difference, _E is the zero, and F =_ _F for_
_∅⊆_ _−_
_standard_
_basis_ all F ⊆ _E. As before, { { e1 }, . . ., { em } } is the standard basis of E(G),_
and dim (G) = m.
_E_
Since the edges of a graph carry its essential structure, we shall
mostly be concerned with the edge space. Given two edge sets F, F _[′ ∈]_
_E(G) and their coefficients λ1, . . ., λm and λ[′]1[, . . ., λ]m[′]_ [with respect to the]
standard basis, we write

_⟨F, F_ _[′]⟩_ _⟨F, F_ _[′]⟩_ := λ1λ[′]1 [+][ . . .][ +][ λ][m][λ]m[′] _[∈]_ [F][2] _[.]_

Note that ⟨F, F _[′]⟩_ = 0 may hold even when F = F _[′]_ ≠ _∅:_ indeed,


-----

in common. Given a subspace of (G), we write
_F_ _E_

_F_ _[⊥]_ := �D ∈ _E(G) | ⟨F, D⟩_ = 0 for all F ∈ _F�_ _._ _F_ _[⊥]_

This is again a subspace of (G) (the space of all vectors solving a certain
_E_
set of linear equations—which?), and we have

dim + dim = m .
_F_ _F_ _[⊥]_

_cycle space_
The cycle space = (G) is the subspace of (G) spanned by all
_C_ _C_ _E_ _C(G)_
the cycles in G—more precisely, by their edge sets.[9] The dimension of
(G) is the cyclomatic number of G.
_C_

**Proposition 1.9.1. The induced cycles in G generate its entire cycle** [ 3.2.3 ]
_space._

_Proof . By definition of_ (G) it suffices to show that the induced cycles
_C_
in G generate every cycle C _G with a chord e. This follows at once_
_⊆_
by induction on _C_ : the two cycles in C + e with e but no other edge in
_|_ _|_
common are shorter than C, and their symmetric difference is precisely C. 
**Proposition 1.9.2. An edge set F** _E lies in_ (G) if and only if every [ 4.5.1 ]
_⊆_ _C_
_vertex of (V, F_ ) has even degree.

_Proof . The forward implication holds by induction on the number of_
cycles needed to generate F, the backward implication by induction on
the number of cycles in (V, F ). 
If { V1, V2 } is a partition of V, the set E(V1, V2) of all the edges of
_G crossing this partition is called a cut. Recall that for V1 = { v } this_ _cut_
cut is denoted by E(v).

**Proposition 1.9.3. Together with** _, the cuts in G form a subspace_ [ 4.6.3 ]
_∅_ _C[∗]_
_of_ (G). This space is generated by cuts of the form E(v).
_E_

_Proof . Let_ denote the set of all cuts in G, together with . To prove
_C[∗]_ _∅_
that C[∗] is a subspace, we show that for all D, D[′] _∈_ _C[∗]_ also D + D[′]

(= D − _D[′]) lies in C[∗]. Since D + D = ∅_ _[∈]_ _C[∗]_ and D + ∅ = D _[∈]_ _C[∗],_
we may assume that D and D[′] are distinct and non-empty. Let
_{ V1, V2 } and { V1[′][, V][ ′]2_ _[}][ be the corresponding partitions of][ V][ .]_ Then
_D + D[′]_ consists of all the edges that cross one of these partitions but
not the other (Fig. 1.9.1). But these are precisely the edges between
(V1 ∩ _V1[′][)][ ∪]_ [(][V][2] _[∩]_ _[V][ ′]2_ [) and (][V][1] _[∩]_ _[V][ ′]2_ [)][ ∪] [(][V][2] _[∩]_ _[V][ ′]1_ [), and by][ D][ ̸][=][ D][′][ these two]

9 For simplicity, we shall not normally distinguish between cycles and their edge


-----

_V1[′]_
_D[′]_
_V2[′]_

_D_

_Fig. 1.9.1. Cut edges in D + D[′]_

sets form another partition of V . Hence D + D[′ ∈] _C[∗], and C[∗]_ is indeed
a subspace of (G).
_E_
Our second assertion, that the cuts E(v) generate all of, follows
_C[∗]_
from the fact that every edge xy _[∈]_ _G lies in exactly two such cuts (in E(x)_
and in E(y)); thus every partition { V1, V2 } of V satisfies E(V1, V2) =
�v ∈V1 _[E][(][v][).]_      
The subspace =: (G) of (G) from Proposition 1.9.3 will be
_cut space_ _C[∗]_ _C[∗]_ _E_
_C[∗](G)_ called the cut space of G. It is not difficult to find among the cuts
_E(v) an explicit basis for_ (G), and thus to determine its dimension
_C[∗]_
(exercise); together with Theorem 1.9.5 this yields an independent proof
of Theorem 1.9.6.
The following lemma will be useful when we study the duality of
plane graphs in Chapter 4.6:

[ 4.6.2 ] **Lemma 1.9.4. The minimal cuts in a connected graph generate its**
_entire cut space._

_Proof . Note first that a cut in a connected graph G = (V, E) is minimal_
if and only if both sets in the corresponding partition of V are connected
in G. Now consider any connected subgraph C _G. If D is a component_
_⊆_
of G _C, then also G_ _D is connected (Fig. 1.9.2); the edges between D_
_−_ _−_

_D_

_G_ _−_ _D_

|V1|V2|
|---|---|
|V 1|V 2|
|||


-----

and G _D thus form a minimal cut. By choice of D, this cut is precisely_
_−_
the set E(C, D) of all C–D edges in G.
To prove the lemma, let a partition { V1, V2 } of V be given, and
consider a component C of G [ V1 ]. Then E(C, V2) = E(C, G − _C) is_
the disjoint union of the edge sets E(C, D) over all components D of
_G_ _C, and is thus the disjoint union of minimal cuts (see above). Now_
_−_
the disjoint union of all these edge sets E(C, V2), taken over all the
components C of G [ V1 ], is precisely our cut E(V1, V2). So this cut is
generated by minimal cuts, as claimed. 
**Theorem 1.9.5. The cycle space** _and the cut space_ _of any graph_
_C_ _C[∗]_
_satisfy_

= _and_ = _._
_C_ _C[∗⊥]_ _C[∗]_ _C[⊥]_

_Proof . Let us consider a graph G = (V, E). Clearly, any cycle in G has_
an even number of edges in each cut. This implies .
_C ⊆C[∗⊥]_
Conversely, recall from Proposition 1.9.2 that for every edge set
_F /[∈]_ _C there exists a vertex v incident with an odd number of edges in F_ .
Then ⟨E(v), F _⟩_ = 1, so E(v) _[∈]_ _C[∗]_ implies F /[∈] _C[∗⊥]. This completes the_
proof of = .
_C_ _C[∗⊥]_
To prove =, it now suffices to show = ( )[⊥]. Here
_C[∗]_ _C[⊥]_ _C[∗]_ _C[∗⊥]_
( )[⊥] follows directly from the definition of . But since
_C[∗]_ _⊆_ _C[∗⊥]_ _⊥_

dim + dim = m = dim + dim ( )[⊥],
_C[∗]_ _C[∗⊥]_ _C[∗⊥]_ _C[∗⊥]_

_C[∗]_ has the same dimension as (C[∗⊥])[⊥], so C[∗] = (C[∗⊥])[⊥] as claimed. 
**Theorem 1.9.6. Every connected graph G with n vertices and m edges** [ 4.5.1 ]
_satisfies_

dim (G) = m _n + 1_ _and_ dim (G) = n 1 .
_C_ _−_ _C[∗]_ _−_

(1.5.1)
_Proof . Let G = (V, E). As dim_ + dim = m by Theorem 1.9.5, it
_C_ _C[∗]_ (1.5.3)
suffices to find m _n + 1 linearly independent vectors in_ and n 1
_−_ _C_ _−_
linearly independent vectors in : since these numbers add up to m,
_C[∗]_
neither the dimension of nor that of can then be strictly greater.
_C_ _C[∗]_
Let T be a spanning tree in G. By Corollary 1.5.3, T has n 1
_−_
edges, so m _n + 1 edges of G lie outside T_ . For each of these m _n + 1_
_−_ _−_
edges e _[∈]_ _E ∖_ _E(T_ ), the graph T + e contains a cycle Ce (see Fig. 1.6.3
and Theorem 1.5.1 (iv)). Since none of the edges e lies on Ce[′] for e[′] ≠ _e,_
these m _n + 1 cycles are linearly independent._
_−_
For each of the n − 1 edges e _[∈]_ _T_, the graph T − _e has exactly two_
components (Theorem 1.5.1 (iii)), and the set De of edges in G between
these components form a cut (Fig.1.9.3). Since none of the edges e _[∈]_ _T_


-----

_Fig. 1.9.3. The cut De_

_incidence_
_matrix_ The incidence matrix B = (bij)n×m of a graph G = (V, E) with
_V = { v1, . . ., vn } and E = { e1, . . ., em } is defined over F2 by_

_bij :=_ � 1 if vi ∈ _ej_
0 otherwise.

As usual, let B[t] denote the transpose of B. Then B and B[t] define linear
maps B: (G) (G) and B[t]: (G) (G) with respect to the standard
_E_ _→V_ _V_ _→E_
bases.

**Proposition 1.9.7.**

(i) The kernel of B is (G).
_C_

(ii) The image of B[t] _is C[∗](G)._        
_adjacency_
_matrix_ The adjacency matrix A = (aij)n×n of G is defined by

_aij :=_ � 1 if vivj ∈ _E_
0 otherwise.

Our last proposition establishes a simple connection between A and B
(now viewed as real matrices). Let D denote the real diagonal matrix
(dij)n×n with dii = d(vi) and dij = 0 otherwise.

**Proposition 1.9.8. BB[t]** = A + D.      

-----

###### 1.10 Other notions of graphs

For completeness, we now mention a few other notions of graphs which
feature less frequently or not at all in this book.
A hypergraph is a pair (V, E) of disjoint sets, where the elements _hypergraph_
of E are non-empty subsets (of any cardinality) of V . Thus, graphs are
special hypergraphs.
_directed_
A directed graph (or digraph) is a pair (V, E) of disjoint sets (of
_graph_
_vertices and edges) together with two maps init: E_ _V and ter: E_ _V_
_→_ _→_
assigning to every edge e an initial vertex init(e) and a terminal vertex init(e)
ter(e). The edge e is said to be directed from init(e) to ter(e). Note that ter(e)
a directed graph may have several edges between the same two vertices
_x, y. Such edges are called multiple edges; if they have the same direction_
(say from x to y), they are parallel . If init(e) = ter(e), the edge e is called
a loop. _loop_
A directed graph D is an orientation of an (undirected) graph G if _orientation_
_V (D) = V (G) and E(D) = E(G), and if_ init(e), ter(e) = _x, y_ for
_{_ _}_ _{_ _}_
_oriented_
every edge e = xy. Intuitively, such an oriented graph arises from an
_graph_
undirected graph simply by directing every edge from one of its ends to
the other. Put differently, oriented graphs are directed graphs without
loops or multiple edges.
A multigraph is a pair (V, E) of disjoint sets (of vertices and edges) _multigraph_
together with a map E _V_ [V ][2] assigning to every edge either one
_→_ _∪_
or two vertices, its ends. Thus, multigraphs too can have loops and
multiple edges: we may think of a multigraph as a directed graph whose
edge directions have been ‘forgotten’. To express that x and y are the
ends of an edge e we still write e = xy, though this no longer determines
_e uniquely._
A graph is thus essentially the same as a multigraph without loops
or multiple edges. Somewhat surprisingly, proving a graph theorem more
generally for multigraphs may, on occasion, simplify the proof. Moreover,
there are areas in graph theory (such as plane duality; see Chapters 4.6
and 6.5) where multigraphs arise more naturally than graphs, and where
any restriction to the latter would seem artificial and be technically
complicated. We shall therefore consider multigraphs in these cases, but
without much technical ado: terminology introduced earlier for graphs
will be used correspondingly.
Two differences, however, should be pointed out. First, a multigraph may have cycles of length 1 or 2: loops, and pairs of multiple
edges (or double edges). Second, the notion of edge contraction is simpler in multigraphs than in graphs. If we contract an edge e = xy in
a multigraph G = (V, E) to a new vertex ve, there is no longer a need
to delete any edges other than e itself: edges parallel to e become loops
at ve, while edges xv and yv become parallel edges between ve and v


-----

map e[′] init(e[′]), ter(e[′]) of G has to be adjusted to the new vertex
_�→{_ _}_
set in G/e. The notion of a minor adapts to multigraphs accordingly.

_ve_

_e_
_G_ _G/e_

_Fig. 1.10.1. Contracting the edge e in the multigraph corre-_
sponding to Fig. 1.8.1

Finally, it should be pointed out that authors who usually work with
multigraphs tend to call them graphs; in their terminology, our graphs
would be called simple graphs.

###### Exercises

1.[−] What is the number of edges in a K _[n]?_

2. Let d _[∈]_ N and V := { 0, 1 }[d]; thus, V is the set of all 0–1 sequences of
length d. The graph on V in which two such sequences form an edge if
and only if they differ in exactly one position is called the d-dimensional
_cube. Determine the average degree, number of edges, diameter, girth_
and circumference of this graph.

(Hint for circumference. Induction on d.)

3. Let G be a graph containing a cycle C, and assume that G contains
a path of length at least k between two vertices of C. Show that G
_√_
contains a cycle of length at least _k. Is this best possible?_

4.[−] Is the bound in Proposition 1.3.2 best possible?

5. Show that rad(G) ⩽ diam(G) ⩽ 2 rad(G) for every graph G.

6.[+] Assuming that d ⩾ 2 and k ⩾ 3, improve the bound in Proposition
1.3.3 to d[k].

7.[−] Show that the components of a graph partition its vertex set. (In other
words, show that every vertex belongs to exactly one component.)

8.[−] Show that every 2-connected graph contains a cycle.

9. (i)[−] Determine κ(G) and λ(G) for G = P _[k], C_ _[k], K_ _[k], Km,n (k, m, n ⩾_ 3).

(ii)[+] Determine the connectivity of the n-dimensional cube (defined in
Exercise 2).

(Hint for (ii). Induction on n.)


-----

11.[−] Is there a function f : N → N such that, for all k _[∈]_ N, every graph of
minimum degree at least f (k) is k-connected?

12. Let α, β be two graph invariants with positive integer values. Formalize
the two statements below, and show that each implies the other:

(i) α is bounded above by a function of β;

(ii) β can be forced up by making α large enough.

Show that the statement

(iii) β is bounded below by a function of α

is not equivalent to (i) and (ii). Which small change would make it so?

13.[+] What is the deeper reason behind the fact that the proof of Theorem
1.4.2 is based on an assumption of the form m ⩾ _cn −_ _b rather than_
just on a lower bound for the average degree?

14. Prove Theorem 1.5.1.

15. Show that any tree T has at least ∆(T ) leaves.

16. Show that the ‘tree-order’ associated with a rooted tree T is indeed a
partial order on V (T ), and verify the claims made about this partial
order in the text.

17. Let G be a connected graph, and let r _∈_ _G be a vertex._ Starting
from r, move along the edges of G, going whenever possible to a vertex
not visited so far. If there is no such vertex, go back along the edge by
which the current vertex was first reached (unless the current vertex
is r; then stop). Show that the edges traversed form a normal spanning
tree in G with root r.

(This procedure has earned those trees the name of depth-first search
trees.)

18. Let T be a set of subtrees of a tree T . Assume that the trees in T have
pairwise non-empty intersection. Show that their overall intersection
� _T is non-empty._

19. Show that every automorphism of a tree fixes a vertex or an edge.

20. Are the partition classes of a regular bipartite graph always of the same
size?

21. Show that a graph is bipartite if and only if every induced cycle has
even length.

22. Find a function f : N _→_ N such that, for all k _[∈]_ N, every graph of average
degree at least f (k) has a bipartite subgraph of minimum degree at
least k.

23. Show that the minor relation ≼ defines a partial ordering on any set of
(finite) graphs. Is the same true for infinite graphs?

24.[−] Show that the elements of the cycle space of a graph G are precisely


-----

25. Given a graph G, find among all cuts of the form E(v) a basis for the
cut space of G.

26. Prove that the cycles and the cuts in a graph together generate its
entire edge space, or find a counterexample.

27. Give a direct proof of the fact that the cycles Ce defined in the proof
of Theorem 1.9.6 generate the cycle space.

28. Give a direct proof of the fact that the cuts De defined in the proof of
Theorem 1.9.6 generate the cut space.

29. What are the dimensions of the cycle and the cut space of a graph with
_k components?_

###### Notes

The terminology used in this book is mostly standard. Alternatives do exist,
of course, and some of these are stated when a concept is first defined. There
is one small point where our notation deviates slightly from standard usage.
Whereas complete graphs, paths, cycles etc. of given order are mostly denoted
by Kn, Pk, Cℓ and so on, we use superscripts instead of subscripts. This has
the advantage of leaving the variables K, P, C etc. free for ad-hoc use: we
may now enumerate components as C1, C2, . . ., speak of paths P1, . . ., Pk, and
so on—without any danger of confusion.
Theorem[10] 1.4.2 is due to W. Mader, Existenz n-fach zusammenh¨angender Teilgraphen in Graphen gen¨ugend großer Kantendichte, Abh. Math. Sem.
_Univ. Hamburg 37 (1972) 86–97._ Theorem 1.8.1 is from L. Euler, Solutio
problematis ad geometriam situs pertinentis, Comment. Acad. Sci. I. Petro_politanae 8 (1736), 128–140._
Of the large subject of algebraic methods in graph theory, Section 1.9 does
not claim to convey an adequate impression. The standard monograph here is
N.L. Biggs, Algebraic Graph Theory (2nd edn.), Cambridge University Press
1993. Another comprehensive account is given by C.D. Godsil & G.F. Royle,
_Algebraic Graph Theory, in preparation._ Surveys on the use of algebraic
methods can also be found in the Handbook of Combinatorics (R.L. Graham,
M. Gr¨otschel & L. Lov´asz, eds.), North-Holland 1995.

10 In the interest of readability, the end-of-chapter notes in this book give references
only for Theorems and only in cases where these references cannot be found in a


-----

# 2 Matching

Suppose we are given a graph and are asked to find in it as many independent edges as possible. How should we go about this? Will we
be able to pair up all its vertices in this way? If not, how can we be
sure that this is indeed impossible? Somewhat surprisingly, this basic
problem does not only lie at the heart of numerous applications, it also
gives rise to some rather interesting graph theory.
A set M of independent edges in a graph G = (V, E) is called a
_matching. M is a matching of U_ _V if every vertex in U is incident_ _matching_
_⊆_
with an edge in M . The vertices in U are then called matched (by M ); _matched_
vertices not incident with any edge of M are unmatched .
A k-regular spanning subgraph is called a k-factor . Thus, a sub- _factor_
graph H _G is a 1-factor of G if and only if E(H) is a matching of V ._
_⊆_
The problem of how to characterize the graphs that have a 1-factor, i.e.
a matching of their entire vertex set, will be our main theme in this
chapter.

###### 2.1 Matching in bipartite graphs

For this whole section, we let G = (V, E) be a fixed bipartite graph with _G = (V, E)_
bipartition { A, B }. Vertices denoted as a, a[′] etc. will be assumed to lie _A, B_
in A, vertices denoted as b etc. will lie in B. _a, b etc._
How can we find a matching in G with as many edges as possible?
Let us start by considering an arbitrary matching M in G. A path in G
which starts in A at an unmatched vertex and then contains, alternately,
_alternating_
edges from E ∖ _M and from M_, is an alternating path with respect to M . _path_
An alternating path P that ends in an unmatched vertex of B is called
_augment-_
an augmenting path (Fig. 2.1.1), because we can use it to turn M into _ing path_


-----

_A_ _B_ _A_ _B_

_Fig. 2.1.1. Augmenting the matching M by the alternating_
path P

matching (consider the edges at a given vertex), and the set of matched
vertices is increased by two, the ends of P .
Alternating paths play an important role in the practical search for
large matchings. In fact, if we start with any matching and keep applying
augmenting paths until no further such improvement is possible, the
matching obtained will always be an optimal one, a matching with the
largest possible number of edges (Exercise 1). The algorithmic problem
of finding such matchings thus reduces to that of finding augmenting
paths—which is an interesting and accessible algorithmic problem.

Our first theorem characterizes the maximal cardinality of a matching
in G by a kind of duality condition. Let us call a set U _V a cover of E_
_⊆_
_vertex_
_cover_ (or a vertex cover of G) if every edge of G is incident with a vertex in U .

**Theorem 2.1.1. (K¨onig 1931)**
_The maximum cardinality of a matching in G is equal to the minimum_
_cardinality of a vertex cover._

_M_ _Proof . Let M be a matching in G of maximum cardinality. From every_
edge in M let us choose one of its ends: its end in B if some alternating
path ends in that vertex, and its end in A otherwise (Fig. 2.1.2). We
_U_ shall prove that the set U of these _M_ vertices covers G; since any vertex
_|_ _|_
cover of G must cover M, there can be none with fewer than _M_ vertices,
_|_ _|_
and so the theorem will follow.

_U ∩_ _B_

_U ∩_ _A_


-----

Let ab _[∈]_ _E be an edge; we show that either a or b lies in U_ . If
_ab_ _[∈]_ _M_, this holds by definition of U, so we assume that ab /[∈] _M_ . Since
_M is a maximal matching, it contains an edge a[′]b[′]_ with a = a[′] or b = b[′].
In fact, we may assume that a = a[′]: for if a is unmatched (and b = b[′]),
then ab is an alternating path, and so the end of a[′]b[′ ∈] _M chosen for_
_U was the vertex b[′]_ = b. Now if a[′] = a is not in U, then b[′ ∈] _U_, and
some alternating path P ends in b[′]. But then there is also an alternating
path P _[′]_ ending in b: either P _[′]_ := Pb (if b _[∈]_ _P_ ) or P _[′]_ := Pb[′]a[′]b. By the
maximality of M, however, P _[′]_ is not an augmenting path. So b must be
matched, and was chosen for U from the edge of M containing it. 
Let us return to our main problem, the search for some necessary
and sufficient conditions for the existence of a 1-factor. In our present
case of a bipartite graph, we may as well ask more generally when G
contains a matching of A; this will define a 1-factor of G if _A_ = _B_,
_|_ _|_ _|_ _|_
a condition that has to hold anyhow if G is to have a 1-factor.
A condition clearly necessary for the existence of a matching of A
is that every subset of A has enough neighbours in B, i.e. that

_|N_ (S)| ⩾ _|S|_ for all S ⊆ _A._ _conditionmarriage_

The following marriage theorem says that this obvious necessary condition is in fact sufficient:

_marriage_
**Theorem 2.1.2. (Hall 1935)**
_theorem_
_G contains a matching of A if and only if |N_ (S)| ⩾ _|S| for all S ⊆_ _A._

We give three proofs for the non-trivial implication of this theorem, i.e.
that the ‘marriage condition’ implies the existence of a matching of A.
The first of these is based on K¨onig’s theorem; the second is a direct
constructive proof by augmenting paths; the third will be an independent
proof from first principles.

**First proof. If G contains no matching of A, then by Theorem 2.1.1**
it has a cover U consisting of fewer than |A| vertices, say U = A[′] _∪_ _B[′]_

with A[′] _A and B[′]_ _B. Then_
_⊆_ _⊆_

_|A[′]| + |B[′]| = |U_ _| < |A|,_
and hence

_|B[′]| < |A| −|A[′]| = |A ∖_ _A[′]|_

(Fig. 2.1.3). By definition of U, however, G has no edges between A ∖ _A[′]_

and B ∖ _B[′], so_

_|N_ (A ∖ _A[′])| ⩽_ _|B[′]| < |A ∖_ _A[′]|_


-----

_A[′]_

_B[′]_

_Fig. 2.1.3. A cover by fewer than |A| vertices_

_M_ **Second proof. Consider a matching M of G that leaves a vertex of A**
unmatched; we shall construct an augmenting path with respect to M .
Let a0, b1, a1, b2, a2, . . . be a maximal sequence of distinct vertices ai _[∈]_ _A_
and bi ∈ _B satisfying the following conditions for all i ⩾_ 1 (Fig. 2.1.4):

(i) a0 is unmatched;

_f_ (i) (ii) bi is adjacent to some vertex af (i) ∈ _{ a0, . . ., ai−1 };_

(iii) aibi ∈ _M_ .

By the marriage condition, our sequence cannot end in a vertex of A:
the i vertices a0, . . ., ai−1 together have at least i neighbours in B, so
we can always find a new vertex bi ̸= b1, . . ., bi−1 that satisfies (ii). Let
_k_ _bk ∈_ _B be the last vertex of the sequence. By (i)–(iii),_

_P_ _P := bkaf_ (k)bf (k)af 2(k)bf 2(k)af 3(k) . . . af r(k)

with f _[r](k) = 0 is an alternating path._


_a2_

_a0_

_a1_

_a3_

_a4_


_b2_

_b1_

_b3_

_b4_

_b5_


_Fig. 2.1.4. Proving the marriage theorem by alternating paths_

What is it that prevents us from extending our sequence further?
If bk is matched, say to a, we can indeed extend it by setting ak := a,
unless a = ai with 0 < i < k, in which case (iii) would imply bk = bi
with a contradiction. So bk is unmatched, and hence P is an augmenting


-----

**Third proof. We apply induction on** _A_ . For _A_ = 1 the assertion
_|_ _|_ _|_ _|_
is true. Now let |A| ⩾ 2, and assume that the marriage condition is
sufficient for the existence of a matching of A when _A_ is smaller.
_|_ _|_
If |N (S)| ⩾ _|S| + 1 for every non-empty set S ⫋_ _A, we pick an edge_
_ab_ _[∈]_ _G and consider the graph G[′]_ := G _−{ a, b }. Then every non-empty_
set S ⊆ _A ∖_ _{ a } satisfies_

_|NG[′]_ (S)| ⩾ _|NG(S)| −_ 1 ⩾ _|S|,_

so by the induction hypothesis G[′] contains a matching of A ∖ _{ a }. To-_
gether with the edge ab, this yields a matching of A in G.
Suppose now that A has a non-empty proper subset A[′] with |B[′]| = _A[′], B[′]_
_|A[′]| for B[′]_ := N (A[′]). By the induction hypothesis, G[′] := G [ A[′] _∪_ _B[′]_ ] _G[′]_
contains a matching of A[′]. But G − _G[′]_ satisfies the marriage condition
too: for any set S ⊆ _A ∖_ _A[′]_ with |NG−G[′] (S)| < |S| we would have
_|NG(S ∪_ _A[′])| < |S ∪_ _A[′]|, contrary to our assumption. Again by induc-_
tion, G − _G[′]_ contains a matching of A ∖ _A[′]. Putting the two matchings_
together, we obtain a matching of A in G. 
**Corollary 2.1.3. If |N** (S)| ⩾ _|S| −_ _d for every set S ⊆_ _A and some_ [ 2.2.3 ]
_fixed d ∈_ N, then G contains a matching of cardinality |A| − _d._

_Proof . We add d new vertices to B, joining each of them to all the ver-_
tices in A. By the marriage theorem the new graph contains a matching
of A, and at least |A|− _d edges in this matching must be edges of G._ 
**Corollary 2.1.4. If G is k-regular with k ⩾** 1, then G has a 1-factor.

_Proof . If G is k-regular, then clearly_ _A_ = _B_ ; it thus suffices to show by
_|_ _|_ _|_ _|_
Theorem 2.1.2 that G contains a matching of A. Now every set S _A_
_⊆_
is joined to N (S) by a total of k _S_ edges, and these are among the
_|_ _|_
_k |N_ (S)| edges of G incident with N (S). Therefore k |S| ⩽ _k |N_ (S)|, so
_G does indeed satisfy the marriage condition._ 
Despite its seemingly narrow formulation, the marriage theorem
counts among the most frequently applied graph theorems, both outside graph theory and within. Often, however, recasting a problem in
the setting of bipartite matching requires some clever adaptation. As a
simple example, we now use the marriage theorem to derive one of the
earliest results of graph theory, a result whose original proof is not all
that simple, and certainly not short:

**Corollary 2.1.5. (Petersen 1891)**


-----

(1.8.1) _Proof . Let G be any 2k-regular graph (k ⩾_ 1), without loss of generality
connected. By Theorem 1.8.1, G contains an Euler tour v0e0 . . . eℓ−1vℓ,
with vℓ = v0. We replace every vertex v by a pair (v[−], v[+]), and every
edge ei = vivi+1 by the edge vi[+][v]i[−]+1 [(Fig. 2.1.5). The resulting bipartite]
graph G[′] is k-regular, so by Corollary 2.1.4 it has a 1-factor. Collapsing
every vertex pair (v[−], v[+]) back into a single vertex v, we turn this 1factor of G[′] into a 2-factor of G.        
_v[−]_

_v_

_v[+]_

_Fig. 2.1.5. Splitting vertices in the proof of Corollary 2.1.5_

###### 2.2 Matching in general graphs

_CG_ Given a graph G, let us denote by CG the set of its components, and by
_q(G)_ _q(G) the number of its odd components, those of odd order. If G has a_
1-factor, then clearly
_Tutte’s_
_condition_ _q(G −_ _S) ⩽_ _|S|_ for all S ⊆ _V (G),_

since every odd component of G _S will send a factor edge to S._
_−_

_S_ _S_


_G_

_Fig. 2.2.1. Tutte’s condition q(G −_ _S) ⩽_ _|S| for q = 3, and the_
contracted graph HS from Theorem 2.2.3.


_HS_


Again, this obvious necessary condition for the existence of a 1-factor


-----

**Theorem 2.2.1. (Tutte 1947)**
_A graph G has a 1-factor if and only if q(G −_ _S) ⩽_ _|S| for all S ⊆_ _V (G)._

_Proof . Let G = (V, E) be a graph without a 1-factor. Our task is to_ _V, E_
find a bad set S _V, one that violates Tutte’s condition._ _bad set_
_⊆_
We may assume that G is edge-maximal without a 1-factor. Indeed,
if G[′] is obtained from G by adding edges and S ⊆ _V is bad for G[′], then_
_S is also bad for G: any odd component of G[′]_ _S is the union of_
_−_
components of G _S, and one of these must again be odd._
_−_
What does G look like? Clearly, if G contains a bad set S then, by
its edge-maximality and the trivial forward implication of the theorem,

_all the components of G_ _S are complete and every vertex_
_−_ ( )
_s ∈_ _S is adjacent to all the vertices of G −_ _s._ _∗_

But also conversely, if a set S _V satisfies (_ ) then either S or the
_⊆_ _∗_
empty set must be bad: if S is not bad we can join the odd components
of G _S disjointly to S and pair up all the remaining vertices—unless_
_−_
_G_ is odd, in which case is bad.
_|_ _|_ _∅_
So it suffices to prove that G has a set S of vertices satisfying ( ).
_∗_
Let S be the set of vertices that are adjacent to every other vertex. If _S_
this set S does not satisfy ( ), then some component of G _S has non-_
_∗_ _−_
adjacent vertices a, a[′]. Let a, b, c be the first three vertices on a shortest _a, b, c_
_a–a[′]_ path in this component; then ab, bc _[∈]_ _E but ac /[∈]_ _E. Since b /[∈]_ _S,_
there is a vertex d _[∈]_ _V such that bd /[∈]_ _E. By the maximality of G, there_ _d_
is a matching M1 of V in G + ac, and a matching M2 of V in G + bd. _M1, M2_

_a_

_d_ 1

_b_

1 2 2

_C_

_c_ 1
_P_

_Fig. 2.2.2. Deriving a contradiction if S does not satisfy (∗)_

Let P = d . . . v be a maximal path in G starting at d with an edge _v_
from M1 and containing alternately edges from M1 and M2 (Fig. 2.2.2).
If the last edge of P lies in M1, then v = b, since otherwise we could
continue P . Let us then set C := P + _bd. If the last edge of P lies in M2,_
then by the maximality of P the M1-edge at v must be ac, so v ∈ _{ a, c };_
then let C be the cycle dPvbd. In each case, C is an even cycle with
every other edge in M2, and whose only edge not in E is bd. Replacing
in M2 its edges on C with the edges of C − _M2, we obtain a matching_


-----

**Corollary 2.2.2. (Petersen 1891)**
_Every bridgeless cubic graph has a 1-factor._

_Proof ._ We show that any bridgeless cubic graph G satisfies Tutte’s
condition. Let S _V (G) be given, and consider an odd component C of_
_⊆_
_G_ _S. Since G is cubic, the degrees (in G) of the vertices in C sum to an_
_−_
odd number, but only an even part of this sum arises from edges of C.
So G has an odd number of S–C edges, and therefore has at least 3 such
edges (since G has no bridge). The total number of edges between S and
_G_ _S thus is at least 3q(G_ _S). But it is also at most 3_ _S_, because G
_−_ _−_ _|_ _|_
is cubic. Hence q(G − _S) ⩽_ _|S|, as required._      
In order to shed a little more light on the techniques used in matching theory, we now give a second proof of Tutte’s theorem. In fact,
we shall prove a slightly stronger result, a result that places a structure
interesting from the matching point of view on an arbitrary graph. If the
graph happens to satisfy the condition of Tutte’s theorem, this structure
will at once yield a 1-factor.
_factor-_
A graph G = (V, E) is called factor-critical if G = and G _v_
_critical_ _̸_ _∅_ _−_
has a 1-factor for every vertex v ∈ _G. Then G itself has no 1-factor,_
_matchable_ because it has odd order. We call a vertex set S _V matchable to_
_⊆_
_G −_ _S if the (bipartite[1]) graph HS, which arises from G by contracting_
the components C ∈ _CG−S to single vertices and deleting all the edges_
_HS_ inside S, contains a matching of S. (Formally, HS is the graph with
vertex set S ∪CG−S and edge set { sC | ∃ _c ∈_ _C : sc ∈_ _E }; see Fig. 2.2.1.)_

**Theorem 2.2.3. Every graph G = (V, E) contains a vertex set S with**
_the following two properties:_

(i) S is matchable to G _S;_
_−_

(ii) every component of G _S is factor-critical._
_−_

_Given any such set S, the graph G contains a 1-factor if and only if_
_|S| = |CG−S|._

For any given G, the assertion of Tutte’s theorem follows easily from
this result. Indeed, by (i) and (ii) we have |S| ⩽ _|CG−S| = q(G −_ _S)_
(since factor-critical graphs have odd order); thus Tutte’s condition of
_q(G −_ _S) ⩽_ _|S| implies |S| = |CG−S|, and the existence of a 1-factor_
follows from the last statement of Theorem 2.2.3.

(2.1.3) **Proof of Theorem 2.2.3.** Note first that the last assertion of the
theorem follows at once from the assertions (i) and (ii): if G has a
1-factor, we have q(G − _S) ⩽_ _|S| and hence |S| = |CG−S| as above;_


-----

conversely if |S| = |CG−S|, then the existence of a 1-factor follows straight
from (i) and (ii).
We now prove the existence of a set S satisfying (i) and (ii). We
apply induction on _G_ . For _G_ = 0 we may take S = . Now let G
_|_ _|_ _|_ _|_ _∅_
be given with _G_ _> 0, and assume the assertion holds for graphs with_
_|_ _|_
fewer vertices.
Let d be the least non-negative integer such that _d_

_q(G −_ _T_ ) ⩽ _|T_ _| + d_ for every T ⊆ _V ._ (∗)

Then there exists a set T for which equality holds in ( ): this follows
_∗_
from the minimality of d if d > 0, and from q(G −∅) ⩾ _|∅| + 0 if d = 0._
Let S be such a set T of maximum cardinality, and let C := CG−S. _S, C_
We first show that every component C ∈ _C is odd. If |C| is even,_
pick a vertex c _[∈]_ _C, and let S[′]_ := S ∪{ c } and C[′] := C − _c. Then C_ _[′]_ has
odd order, and thus has at least one odd component. Hence, q(G _−_ _S[′]) ⩾_
_q(G_ _S) + 1. Since T := S satisfies (_ ) with equality, we obtain
_−_ _∗_

_q(G −_ _S[′]) ⩾_ _q(G −_ _S) + 1 = |S| + d + 1 = |S[′]| + d ⩾_ _q(G −_ _S[′])_
(∗)

with equality, which contradicts the maximality of S.
Next we prove the assertion (ii), that every C ∈ _C is factor-critical._
Suppose there exist C _[∈]_ _C and c_ _[∈]_ _C such that C_ _[′]_ := C − _c has no_
1-factor. By the induction hypothesis (and the fact that, as shown earlier, for fixed G our theorem implies Tutte’s theorem) there exists a set
_T_ _[′]_ _⊆_ _V (C_ _[′]) with_
_q(C_ _[′]_ _−_ _T_ _[′]) > |T_ _[′]| ._

Since |C| is odd and hence |C _[′]| is even, the numbers q(C_ _[′]_ _−_ _T_ _[′]) and |T_ _[′]|_
are either both even or both odd, so they cannot differ by exactly 1. We
may therefore sharpen the above inequality to

_q(C_ _[′]_ _−_ _T_ _[′]) ⩾_ _|T_ _[′]| + 2 ._

For T := S ∪{ c } ∪ _T_ _[′]_ we thus obtain

_q(G −_ _T_ ) = q(G − _S) −_ 1 + q(C _[′]_ _−_ _T_ _[′])_

⩾ _|S| + d −_ 1 + |T _[′]| + 2_

= _T_ + d
_|_ _|_

⩾ _q(G −_ _T_ )
(∗)

with equality, again contradicting the maximality of S.
It remains to show that S is matchable to G _S. If S =_, this
_−_ _∅_


-----

equality, this implies that too is non-empty. We now apply Corollary
_C_
_H_ 2.1.3 to H := HS, but ‘backwards’, i.e. with A := C. Given C[′] _⊆C,_
set S[′] := NH (C[′]) ⊆ _S. Since every C ∈_ _C[′]_ is an odd component also of
_G −_ _S[′], we have_

_|NH_ (C[′])| = |S[′]| ⩾ _q(G −_ _S[′]) −_ _d ⩾_ _|C[′]| −_ _d ._
(∗)

By Corollary 2.1.3, then, H contains a matching of cardinality

_d = q(G_ _S)_ _d =_ _S_ _,_
_|C| −_ _−_ _−_ _|_ _|_

which is therefore a matching of S.       
_S_ Let us consider once more the set S from Theorem 2.2.3, together
_C_ with any matching M in G. As before, we write C := CG−S. Let us
denote by kS the number of edges in M with at least one end in S, and
_kS_ _, kC_ by kC the number of edges in M with both ends in G − _S. Since each_
_C ∈_ _C is odd, at least one of its vertices is not incident with an edge of_
the second type. Therefore every matching M satisfies

� �

_kS ⩽_ _|S|_ and _kC ⩽_ [1]2 _|V | −|S| −|C|_ _._ (1)


_M0_ Moreover, G contains a matching M0 with equality in both cases: first
choose _S_ edges between S and according to (i), and then use (ii) to
_|_ _|_ [�] _C_
find a suitable set of [1]2 �|C| − 1� edges in every component C _[∈]_ _C. This_

matching M0 thus has exactly

� �

_|M0| = |S| +_ [1]2 _|V | −|S| −|C|_ (2)

edges.
Now (1) and (2) together imply that every matching M of maximum
cardinality satisfies both parts of (1) with equality: by |M _| ⩾_ _|M0|_
and (2), M has at least |S| + [1]2 �|V | −|S| −|C|� edges, which implies by

(1) that neither of the inequalities in (1) can be strict. But equality
in (1), in turn, implies that M has the structure described above: by
_kS = |S|, every vertex s_ _[∈]_ _S is the end of an edge st_ _[∈]_ _M with t_ _[∈]_ _G_ _−_ _S,_
and by kC = [1]2 �|V | −|S| −|C|� exactly [1]2 [(][|][C][| −] [1]� edges of M lie in C,

for every C _[∈]_ _C. Finally, since these latter edges miss only one vertex in_
each C, the ends t of the edges st above lie in different components C
for different s.
The seemingly technical Theorem 2.2.3 thus hides a wealth of structural information: it contains the essence of a detailed description of all
maximum-cardinality matchings in all graphs.[2]


2 A reference to the full statement of this structural result, known as the Gallai

-----

###### 2.3 Path covers

Let us return for a moment to K¨onig’s duality theorem for bipartite
graphs, Theorem 2.1.1. If we orient every edge of G from A to B, the
theorem tells us how many disjoint directed paths we need in order to
cover all the vertices of G: every directed path has length 0 or 1, and
clearly the number of paths in such a ‘path cover’ is smallest when it
contains as many paths of length 1 as possible—in other words, when it
contains a maximum-cardinality matching.
In this section we put the above question more generally: how many
paths in a given directed graph will suffice to cover its entire vertex set?
Of course, this could be asked just as well for undirected graphs. As it
turns out, however, the result we shall prove is rather more trivial in
the undirected case (exercise), and the directed case will also have an
interesting corollary.
A directed path is a directed graph P = with distinct vertices
_̸_ _∅_
_x0, . . ., xk and edges e0, . . ., ek−1 such that ei is an edge directed from_
_xi to xi+1, for all i < k. We denote the last vertex xk of P by ter(P_ ). ter(P )
In this section, path will always mean ‘directed path’. A path cover of a _path_
directed graph G is a set of disjoint paths in G which together contain _path cover_
all the vertices of G. Let us denote the maximum cardinality of an
independent set of vertices in G by α(G). _α(G)_

**Theorem 2.3.1. (Gallai & Milgram 1960)**
_Every directed graph G has a path cover by at most α(G) paths._

_Proof . Given two path covers P1, P2 of a graph, we write P1 < P2 if_ _P1 < P2_
_{ ter(P_ ) | P ∈ _P1 } ⊆{ ter(P_ ) | P ∈ _P2 } and |P1| < |P2|. We shall prove_
the following:

_If_ _is a <-minimal path cover of G, then G contains an_
_P_
_independent set { vP | P_ _[∈]_ _P } of vertices with vP_ _[∈]_ _P for_ (∗)
_every P_ _[∈]_ _P._

Clearly, ( ) implies the assertion of the theorem.
_∗_
We prove (∗) by induction on |G|. Let P = { P1, . . ., Pm } be given _P, Pi, m_
as in (∗), and let vi := ter(Pi) for every i. If { vi | 1 ⩽ _i ⩽_ _m } is_ _vi_
independent, there is nothing more to show; we may therefore assume
that G has an edge from v2 to v1. Since P2v2v1 is again a path, the
minimality of P implies that v1 is not the only vertex of P1; let v be _v_
the vertex preceding v1 on P1. Then P _[′]_ := { P1v, P2, . . ., Pm } is a path _P_ _[′]_
cover of G[′] := G − _v1 (Fig. 2.3.1). We first show that P_ _[′]_ is <-minimal _G[′]_
with this property.
Suppose that P _[′′]_ _< P_ _[′]_ is another path cover of G[′]. If a path P _[∈]_ _P_ _[′′]_

ends in v, we may replace P in P _[′′]_ by Pvv1 to obtain a smaller path


-----

_v1_ _v2_

_v_

_P1_ _P2_


_Pm_

|P 2|. . .|
|---|---|


_Fig. 2.3.1. The path cover P_ _[′]_ of G[′]

_P_ _∈_ _P_ _[′′]_ ends in v2 (but none in v), we replace P in P _[′′]_ by Pv2v1,
again contradicting the minimality of P. Hence { ter(P ) | P _[∈]_ _P_ _[′′]_ _} ⊆_
_{ v3, . . ., vm }, and in particular |P_ _[′′]| ⩽_ _|P| −_ 2. But now P _[′′]_ and the
trivial path { v1 } together form a path cover of G that contradicts the
minimality of .
_P_
Hence is minimal, as claimed. By the induction hypothesis,
_P_ _[′]_
_{ V (P_ ) | P _[∈]_ _P_ _[′]_ _} has an independent set of representatives. But this is_
also a set of representatives for P, and (∗) is proved.       
As a corollary to Theorem 2.3.1 we now deduce a classic result from
the theory of partial orders. Recall that a subset of a partially ordered
_chain_ set (P, ⩽) is a chain in P if its elements are pairwise comparable; it is
_antichain_ an antichain if they are pairwise incomparable.

**Corollary 2.3.2. (Dilworth 1950)**
_In every finite partially ordered set (P, ⩽), the minimum number of_
_chains covering P is equal to the maximum cardinality of an antichain_
_in P_ _._

_Proof . If A is an antichain in P of maximum cardinality, then clearly_
_P cannot be covered by fewer than_ _A_ chains. The fact that _A_ chains
_|_ _|_ _|_ _|_
will suffice follows from Theorem 2.3.1 applied to the directed graph on
_P with the edge set { (x, y) | x < y }._       
###### Exercises

1. Let M be a matching in a bipartite graph G. Show that if M is suboptimal, i.e. contains fewer edges than some other matching in G, then
_G contains an augmenting path with respect to M_ . Does this fact
generalize to matchings in non-bipartite graphs?


-----

2. Describe an algorithm that finds, as efficiently as possible, a matching
of maximum cardinality in any bipartite graph.

3. Find an infinite counterexample to the statement of the marriage theorem.

4. Let k be an integer. Show that any two partitions of a finite set into
_k-sets admit a common choice of representatives._

5. Let A be a finite set with subsets A1, . . ., An, and let d1, . . ., dn _[∈]_ N.
Show that there are disjoint subsets Dk ⊆ _Ak, with |Dk| = dk for all_
_k ⩽_ _n, if and only if_
� �

_Ai_ ⩾ _di_

��� ���

_i∈I_ _i∈I_

for all I ⊆{ 1, . . ., n }.

6.[+] Prove Sperner’s lemma: in an n-set X there are never more than [�]⌊n/n2⌋�

subsets such that none of these contains another.

(Hint. Construct [�]⌊n/n2⌋� chains covering the power set lattice of X.)

7. Find a set S for Theorem 2.2.3 when G is a forest.

8. Using (only) Theorem 2.2.3, show that a k-connected graph with at
least 2k vertices contains a matching of size k. Is this best possible?

9. A graph G is called (vertex-) transitive if, for any two vertices v, w _[∈]_ _G,_
there is an automorphism of G mapping v to w. Using the observations following the proof of Theorem 2.2.3, show that every transitive
connected graph is either factor-critical or contains a 1-factor.

(Hint. Consider the cases of S = ∅ and S ̸= ∅ separately.)

10. Show that a graph G contains k independent edges if and only if
_q(G −_ _S) ⩽_ _|S| + |G| −_ 2k for all sets S ⊆ _V (G)._

(Hint. For the ‘if’ direction, suppose that G has no k independent
edges, and apply Tutte’s 1-factor theorem to the graph G ∗ _K_ _[|][G][|−][2][k]._
Alternatively, use Theorem 2.2.3.)

11.[−] Find a cubic graph without a 1-factor.

12. Derive the marriage theorem from Tutte’s theorem.

13.[−] Prove the undirected version of the theorem of Gallai & Milgram (without using the directed version).

14. Derive the marriage theorem from the theorem of Gallai & Milgram.

15.[−] Show that a partially ordered set of at least rs + 1 elements contains
either a chain of size r + 1 or an antichain of size s + 1.

16. Prove the following dual version of Dilworth’s theorem: in every finite partially ordered set (P, ⩽), the minimum number of antichains
covering P is equal to the maximum cardinality of a chain in P .


-----

18.[+] Find a partially ordered set that has no infinite antichain but cannot
be covered by finitely many chains.

(Hint. N × N.)

###### Notes

There is a very readable and comprehensive monograph about matching in
finite graphs: L. Lov´asz & M.D. Plummer, Matching Theory, Annals of Discrete Math. 29, North Holland 1986. All the references for the results in this
chapter can be found there.
As we shall see in Chapter 3, K¨onig’s Theorem of 1931 is no more than the
bipartite case of a more general theorem due to Menger, of 1929. At the time,
neither of these results was nearly as well known as Hall’s marriage theorem,
which was proved even later, in 1935. To this day, Hall’s theorem remains one
of the most applied graph-theoretic results. Its special case that both partition
sets have the same size was proved implicitly already by Frobenius (1917) in
a paper on determinants.
Our proof of Tutte’s 1-factor theorem is based on a proof by Lov´asz
(1975). Our extension of Tutte’s theorem, Theorem 2.2.3 (including the informal discussion following it) is a lean version of a comprehensive structure theorem for matchings, due to Gallai (1964) and Edmonds (1965). See Lov´asz &
Plummer for a detailed statement and discussion of this theorem.
Theorem 2.3.1 is due to T. Gallai & A.N. Milgram, Verallgemeinerung
eines graphentheoretischen Satzes von R´edei, Acta Sci. Math. (Szeged) 21
(1960), 181–186.


-----

# 3 Connectivity

Our definition of k-connectedness, given in Chapter 1.4, is somewhat
unintuitive. It does not tell us much about ‘connections’ in a k-connected
graph: all it says is that we need at least k vertices to disconnect it. The
following definition—which, incidentally, implies the one above—might
have been more descriptive: ‘a graph is k-connected if any two of its
vertices can be joined by k independent paths’.
It is one of the classic results of graph theory that these two definitions are in fact equivalent, are dual aspects of the same property. We
shall study this theorem of Menger (1927) in some depth in Section 3.3.
In Sections 3.1 and 3.2, we investigate the structure of the 2-connected and the 3-connected graphs. For these small values of k it is still
possible to give a simple general description of how these graphs can be
constructed.
In the remaining sections of this chapter we look at other concepts of
connectedness, more recent than the standard one but no less important:
the number of H-paths in a graph for a given subgraph H; the number of
edge-disjoint spanning trees; and the existence of disjoint paths linking
up several given pairs of vertices.

###### 3.1 2-Connected graphs and subgraphs

A maximal connected subgraph without a cutvertex is called a block . _block_
Thus, every block of a graph G is either a maximal 2-connected subgraph,
or a bridge (with its ends), or an isolated vertex. Conversely, every such
subgraph is a block. By their maximality, different blocks of G overlap
in at most one vertex, which is then a cutvertex of G. Hence, every edge
of G lies in a unique block, and G is the union of its blocks.
In a sense, blocks are the 2-connected analogues of components, the


-----

determined fully by that of its components, however, it is not captured
completely by the structure of its blocks: since the blocks need not be
disjoint, the way they intersect defines another structure, giving a coarse
picture of G as if viewed from a distance.
The following proposition describes this coarse structure of G as
formed by its blocks. Let A denote the set of cutvertices of G, and
_B_
the set of its blocks. We then have a natural bipartite graph on A
_∪B_
_block_
_graph_ formed by the edges aB with a _[∈]_ _B. This block graph of G is shown in_
Figure 3.1.1.

_B[′]_
_B[′]_

_a[′]_ _a[′]_

_B_ _B_

_a_

_a_

_Fig. 3.1.1. A graph and its block graph_

**Proposition 3.1.1. The block graph of a connected graph is a tree.**

                       
Proposition 3.1.1 reduces the structure of a given graph to that of its
blocks. So what can we say about the blocks themselves? The following
proposition gives a simple method by which, in principle, a list of all
2-connected graphs could be compiled:

[ 4.2.5 ] **Proposition 3.1.2. A graph is 2-connected if and only if it can be**
_constructed from a cycle by successively adding H-paths to graphs H_
_already constructed (Fig. 3.1.2)._


-----

_Proof ._ Clearly, every graph constructed as described is 2-connected.
Conversely, let a 2-connected graph G be given. Then G contains a
cycle, and hence has a maximal subgraph H constructible as above. _H_
Since any edge xy ∈ _E(G) ∖_ _E(H) with x, y ∈_ _H would define an H-_
path, H is an induced subgraph of G. Thus if H = G, then by the
_̸_
connectedness of G there is an edge vw with v ∈ _G −_ _H and w ∈_ _H. As_
_G is 2-connected, G_ _w contains a v–H path P_ . Then wvP is an H-path
_−_
in G, and H _wvP is a constructible subgraph of G larger than H. This_
_∪_
contradicts the maximality of H. 
###### 3.2 The structure of 3-connected graphs

We start this section with the analogue of Proposition 3.1.2 for 3connectedness: our first theorem describes how every 3-connected graph
can be obtained from a K [4] by a succession of elementary operations
preserving 3-connectedness. We then prove a deep result of Tutte about
the algebraic structure of the cycle space of 3-connected graphs; this will
play an important role again in Chapter 4.5.

**Lemma 3.2.1. If G is 3-connected and** _G_ _> 4, then G has an edge e_ [ 4.4.3 ]
_|_ _|_
_such that G/e is again 3-connected._

_Proof . Suppose there is no such edge e. Then, for every edge xy ∈_ _G,_ _xy_
the graph G/xy contains a separating set S of at most 2 vertices. Since
_κ(G) ⩾_ 3, the contracted vertex vxy of G/xy (see Chapter 1.7) lies
in S and |S| = 2, i.e. G has a vertex z /∈ _{ x, y } such that { vxy, z }_ _z_
separates G/xy. Then any two vertices separated by { vxy, z } in G/xy
are separated in G by T := _x, y, z_ . Since no proper subset of T
_{_ _}_
separates G, every vertex in T has a neighbour in every component C _C_
of G _T_ .
_−_
We choose the edge xy, the vertex z, and the component C so that
_C_ is as small as possible, and pick a neighbour v of z in C (Fig. 3.2.1). _v_
_|_ _|_

_x_
_y_
_z_ _v_

_C_
_T_


-----

By assumption, G/zv is again not 3-connected, so again there is a vertex
_w_ _w such that_ _z, v, w_ separates G, and as before every vertex in _z, v, w_
_{_ _}_ _{_ _}_
has a neighbour in every component of G _z, v, w_ .
_−{_ _}_
As x and y are adjacent, G _z, v, w_ has a component D such that
_−{_ _}_
_D ∩{ x, y } = ∅. Then every neighbour of v in D lies in C (since v_ _[∈]_ _C),_
so D ∩ _C ̸= ∅_ and hence D ⫋ _C by the choice of D. This contradicts the_
choice of xy, z and C.       
**Theorem 3.2.2. (Tutte 1961)**
_A graph G is 3-connected if and only if there exists a sequence G0, . . ., Gn_
_of graphs with the following properties:_
(i) G0 = K [4] _and Gn = G;_
(ii) Gi+1 has an edge xy with d(x), d(y) ⩾ 3 and Gi = Gi+1/xy, for
_every i < n._

_Proof . If G is 3-connected, a sequence as in the theorem exists by Lemma_
3.2.1. Note that all the graphs in this sequence are 3-connected.
Conversely, let G0, . . ., Gn be a sequence of graphs as stated; we
_xy_ show that if Gi = Gi+1/xy is 3-connected then so is Gi+1, for every i < n.
_S_ Suppose not, let S be a separating set of at most 2 vertices in Gi+1, and
_C1, C2_ let C1, C2 be two components of Gi+1 _S. As x and y are adjacent, we_
_−_
may assume that { x, y }∩ _V (C1) = ∅_ (Fig. 3.2.2). Then C2 contains nei
_y_
_x_

_C1_ _S_ _C2_

_Fig. 3.2.2. The position of xy_ _∈_ _Gi+1 in the proof of Theo-_
rem 3.2.2

ther both vertices x, y nor a vertex v /[∈] _{ x, y }: otherwise vxy or v would_
be separated from C1 in Gi by at most two vertices, a contradiction.
But now C2 contains only one vertex: either x or y. This contradicts
our assumption of d(x), d(y) ⩾ 3.      
Theorem 3.2.2 is the essential core of a result of Tutte known as his
_wheel theorem.[1]_ Like Proposition 3.1.2 for 2-connected graphs, it enables
us to construct all 3-connected graphs by a simple inductive process
depending only on local information: starting with K [4], we pick a vertex
_v in a graph constructed already, split it into two adjacent vertices v[′], v[′′],_
and join these to the former neighbours of v as we please—provided only
that v[′] and v[′′] each acquire at least 3 incident edges, and that every
former neighbour of v becomes adjacent to at least one of v[′], v[′′].


-----

**Theorem 3.2.3. (Tutte 1963)**
_The cycle space of a 3-connected graph is generated by its non-separating_ [ 4.5.2 ]
_induced cycles._

_Proof ._ We apply induction on the order of the graph G considered. (1.9.1)
In K [4], every cycle is a triangle or (in terms of edges) the symmetric
difference of triangles. As these are both induced and non-separating,
the assertion holds for _G_ = 4.
_|_ _|_
For the induction step, let e = xy be an edge of G for which _e = xy_
_G[′]_ := G/e is again 3-connected; cf. Lemma 3.2.1. Then every edge _G[′]_
_e[′ ∈]_ _E(G[′]) ∖_ _E(G) is of the form e[′]_ = uve, where at least one of the
two edges ux and uy lies in G. We pick one that does (either ux or uy),
and identify it notationally with the edge e[′]; thus e[′] now denotes both
the edge uve of G[′] and one of the two edges ux, uy. In this way we may
regard E(G[′]) as a subset of E(G), and E(G[′]) as a subspace of E(G); thus
all vector operations will take place unambiguously in (G).
_E_
Let us consider an induced cycle C ⊆ _G. If e_ _[∈]_ _C and C = C_ [3], we
call C a fundamental triangle; then C/e = K [2]. If e _[∈]_ _C but C ̸= C_ [3], _[fundamental]triangle_
then C/e is a cycle in G[′]. Finally if e /[∈] _C, then at most one of x, y_
lies on C (otherwise e would be a chord), so the vertices of C in order
also form a cycle in G[′] if we replace x or y by ve; this cycle, too, will
be denoted by C/e. Thus, as long as C is not a fundamental triangle,
_C/e will always denote a unique cycle in G[′]. Note, however, that in the_ _C/e_
case of e /[∈] _C the edge set of C/e when viewed as a subset of E(G) need_
not coincide with E(C), or even be a cycle at all; an example is shown
in Figure 3.2.3.

_x_ _x_

_u_ _w_ _u_ _e[′]_ _e[′′]_ _w_ _u_ _e[′′]_ _w_


_C_


_C/e_


_E(C/e) ⊆_ _G_


_Fig. 3.2.3. One of the four possibilities for E(C/e) when e /∈_ _C_

Let us refer to the non-separating induced cycles in G or G[′] as basic _basic cycles_
cycles. An element of (G) will be called good if it is a linear combination _good_
_C_
of basic cycles in G; we thus want to show that every element of (G) is
_C_
good. The basic idea of our proof is to contract a given cycle C _[∈]_ _C(G)_
to C/e, generate C/e in C(G[′]) by induction, and try to lift the generators
back to basic cycles in G that generate C.
We start by proving three auxiliary facts.


-----

A fundamental triangle, wxyw say, is clearly induced in G. If it separated G, then { ve, w } would separate G[′], which contradicts the choice
of e. This proves (1).

_If C_ _G is an induced cycle but not a fundamental trian-_
_⊆_ (2)
_gle, then C +_ _C/e_ + _D_ _[∈]_ _{ ∅, {e} } for some good D_ _[∈]_ _C(G)._

The gist of (2) is that, in terms of ‘generatability’, C and C/e differ only
a little: after the addition of a permissible error term D, at most in the
edge e. In which other edges, then, can C and C/e differ? Clearly at
most in the two edges eu = uve and ew = vew incident with ve in C/e;
cf. Fig. 3.2.3. But these differences between the edge sets of C/e and
_C are levelled out precisely by adding the corresponding fundamental_
triangles uxy and xyw (which are basic by (1)). Indeed, let Du denote
the triangle uxy if eu /∈ _C and ∅_ otherwise, and let Dw denote xyw if
_ew /∈_ _C and ∅_ otherwise. Then D := Du + Dw satisfies (2) as desired.
Next, we show how to lift basic cycles of G[′] back to G:

_For every basic cycle C_ _[′]_ _G[′]_ _there exists a basic cycle_
_⊆_ (3)
_C = C(C_ _[′]) ⊆_ _G with C/e = C_ _[′]._

If ve /∈ _C_ _[′], then (3) is satisfied with C := C_ _[′]. So we assume that ve ∈_ _C_ _[′]._
_u, w_ Let u and w be the two neighbours of ve on C _[′], and let P be the u–w_
_P_ path in C _[′]_ avoiding ve (Fig. 3.2.4). Then P ⊆ _G._

_x_

_u_ _w_

_y_

_P_

_Fig. 3.2.4. The search for a basic cycle C with C/e = C_ _[′]_

We first assume that _ux, uy, wx, wy_ _E(G), and consider (as_
_{_ _} ⊆_
_Cx, Cy_ candidates for C) the cycles Cx := uPwxu and Cy := uPwyu. Both are
induced cycles in G (because C _[′]_ is induced in G[′]), and clearly Cx/e =
_Cy/e = C_ _[′]._ Moreover, neither of these cycles separates two vertices
of G − (V (P ) ∪{ x, y }) in G, since C _[′]_ does not separate such vertices
in G[′]. Thus, if Cx (say) is a separating cycle in G, then one of the
components of G − _Cx consists just of y. Likewise, if Cy separates G_
then one of the arising components contains only x. However, this cannot
happen for both Cx and Cy at once: otherwise NG({ x, y }) ⊆ _V (P_ ) and
hence NG({ x, y }) = { u, w } (since C[′] has no chord), which contradicts


-----

It remains to consider the case that _ux, uy, wx, wy_ _E(G), say_
_{_ _} ̸⊆_
_ux /[∈]_ _E(G). Then, as above, either uPwyu or uPwxyu is a basic cycle_
in G, according as wy is an edge of G or not. This completes the proof
of (3).

We now come to the main part of our proof, the proof that every
_C_ _[∈]_ _C(G) is good. By Proposition 1.9.1 we may assume that C is an_ _C_
induced cycle in G. By (1) we may further assume that C is not a
fundamental triangle; so C/e is a cycle. Our aim is to argue as follows.
By (2), C differs from C/e at most by some good error term D (and
possibly in e); by (3), the basic cycles Ci[′] [of][ G][′][ that sum to][ C/e][ by]
induction can be contracted from basic cycles of G, which likewise differ
from the Ci[′] [only by a good error term][ D][i][ (and possibly in][ e][); hence these]
basic cycles of G and all the error terms together sum to C—except that
the edge e will need some special attention.
By the induction hypothesis, C/e has a representation

_C/e = C1[′]_ [+][ . . .][ +][ C]k[′] _C1[′]_ _[, . . ., C]k[′]_

in C(G[′]), where every Ci[′] [is a basic cycle in][ G][′][. For each][ i][, we obtain from]
(3) a basic cycle C(Ci[′][)][ ⊆] _[G][ with][ C][(][C]i[′][)][/e][ =][ C]i[′]_ [(in particular,][ C][(][C]i[′][) is]
not a fundamental triangle), and from (2) some good Di ∈ _C(G) such_
that

_C(Ci[′][) +][ C]i[′]_ [+][ D][i][ ∈] _[{ ∅][,][ {][e][} }][ .]_ (4)

We let

_Ci := C(Ci[′][) +][ D][i]_ [;] _C1, . . ., Ck_

then Ci is good, and by (4) it differs from Ci[′] [at most in][ e][. Again by (2),]
we have

_C + C/e + D_ _[∈]_ _{ ∅, {e} }_

for some good D _[∈]_ _C(G), i.e. C + D differs from C/e at most in e. But_ _D_
then C + D + C1 + _. . ._ + _Ck differs from C/e_ + _C1[′]_ [+] _[. . .]_ [+] _[C]k[′]_ [=][ ∅] [at most]
in e, that is,

_C + D + C1 + . . . + Ck ∈_ _{ ∅, {e} } ._

Since C + D + C1 + . . . + Ck _[∈]_ _C(G) but {e} /[∈]_ _C(G), this means that in_
fact

_C + D + C1 + . . . + Ck = ∅_ _,_

so C = D + C1 + . . . + Ck is good. 

-----

###### 3.3 Menger’s theorem

The following theorem is one of the cornerstones of graph theory.

[ 3.6.2 ]

[ 8.1.2 ] **Theorem 3.3.1. (Menger 1927)**

[ 12.3.9 ] _Let G = (V, E) be a graph and A, B_ _V . Then the minimum number_

_⊆_

[ 12.4.4 ] _of vertices separating A from B in G is equal to the maximum number_

[ 12.4.5 ]
_of disjoint A–B paths in G._

We offer three proofs. Whenever G, A, B are given as in the theorem,
_k_ we denote by k = k (G, A, B) the minimum number of vertices separating
_A from B in G. Clearly, G cannot contain more than k disjoint A–B_
paths; our task will be to show that k such paths exist.

**First proof. We prove the following stronger statement:**

_If_ _is any set of fewer than k disjoint A–B paths in G_
_P_
_then there is a set_ _of_ + 1 disjoint A–B paths whose
_Q_ _|P|_
_set of ends includes the set of ends of the paths in_ _._
_P_

Keeping G and A fixed, we let B vary and apply induction on _G_ _B_ .
_|_ _−_ _|_
Let R be an A–B path that avoids the (fewer than k) vertices of B that
lie on a path in . If R avoids all the paths in, then := _R_
_P_ _P_ _Q_ _P ∪{_ _}_
is as desired. (This will happen for _G_ _B_ = 0 when all A–B paths are
_|_ _−_ _|_
trivial.) If not, let x be the last vertex of R that lies on some P _[∈]_ _P_
(Fig. 3.3.1). Put B[′] := B ∪ _V (xP ∪_ _xR) and P_ _[′]_ := �P ∖ _{ P }�_ _∪{ Px }._
Then |P _[′]| = |P| and k(G, A, B[′]) ⩾_ _k(G, A, B), so by the induction_
hypothesis there is a set Q[′] of |P| + 1 disjoint A–B[′] paths whose ends
include those of the paths in . Then contains a path Q ending in x,
_P_ _[′]_ _Q[′]_
and a unique path Q[′] whose last vertex y is not among the last vertices
of the paths in . If y /[∈] _xP_, we let be obtained from by adding
_P_ _[′]_ _Q_ _Q[′]_
_xP to Q, and adding yR to Q[′]_ if y /[∈] _B. Otherwise y_ _[∈]_ ˚xP, and we let
_Q be obtained from Q[′]_ by adding xR to Q and adding yP to Q[′].       
_R_

_P_

_x_ _xP_

_P_

_A_ _xR_ _B_


-----

**Second proof. We show by induction on** _G_ + _G_ that G contains k
_|_ _|_ _∥_ _∥_
disjoint A–B paths. For all G, A, B with k _[∈]_ _{ 0, 1 } this is true. For_
the induction step let G, A, B with k ⩾ 2 be given, and assume that the
assertion holds for graphs with fewer vertices or edges.
If there is a vertex x _[∈]_ _A_ _∩_ _B, then G_ _−_ _x contains k −_ 1 disjoint A–B
paths by the induction hypothesis. (Why?) Together with the trivial
path _x_, these form the desired paths in G. We shall therefore assume
_{_ _}_
that
_A_ _B =_ _._ (1)
_∩_ _∅_

We first construct the desired paths for the case that A and B are
separated by a set X ⊆ _V with |X| = k and X ̸= A, B. Let CA be_ _X_
the union of all the components of G − _X meeting A; note that CA ̸= ∅,_
since |A| ⩾ _k = |X| but A ̸= X. The subgraph CB defined likewise is not_ _CA, CB_
empty either, and CA ∩ _CB = ∅. Let us write GA := G [ V (CA)_ _∪_ _X ] and_
_GB := G [ V (CB) ∪_ _X ]. Since every A–B path in G contains an A–X_ _GA, GB_
path in GA, we cannot separate A from X in GA by fewer than k vertices.
Thus, by the induction hypothesis, GA contains k disjoint A–X paths
(Fig. 3.3.2). In the same way, there are k disjoint X–B paths in GB. As
_X_ = k, we can put these paths together to form k disjoint A–B paths.
_|_ _|_

_A_

_A_
_B_

_GA_ _GB_

_X_

_Fig. 3.3.2. Disjoint A–X paths in GA_

For the general case, let P be any A–B path in G. By (1), P has
an edge ab with a /[∈] _B and b /[∈]_ _A. Let Y be a set of as few vertices as_ _ab_
possible separating A from B in G _−_ _ab (Fig. 3.3.3). Then Ya := Y ∪{ a }_ _Y_
and Yb := Y ∪{ b } both separate A from B in G, and by definition of k _Ya, Yb_
we have
_|Ya|, |Yb| ⩾_ _k ._

If equality holds here, we may assume by the case already treated that
_{ Ya, Yb } ⊆{ A, B }, so { Ya, Yb } = { A, B } since a /[∈]_ _B and b /[∈]_ _A. Thus,_
_Y = A ∩_ _B. Since |Y | ⩾_ _k −_ 1 ⩾ 1, this contradicts (1).
We therefore have either |Ya| > k or |Yb| > k, and hence |Y | ⩾ _k._
By the induction hypothesis, then, there are k disjoint A–B paths even


-----

_a_ _b_

_P_

_A_ _B_
_Y_

_Fig. 3.3.3. Separating A from B in G −_ _ab_

Applied to a bipartite graph, Menger’s theorem specializes to the
assertion of K¨onig’s theorem (2.1.1). For our third proof, we now adapt
the alternating path proof of K¨onig’s theorem to the more general set_P_ up of Theorem 3.3.1. Let again G, A, B be given, and let P be a set of
disjoint A–B paths in G. We write

�
_V [ P ] :=_ _{ V (P_ ) | P _[∈]_ _P }_

�
_E [ P ] :=_ _{ E(P_ ) | P _[∈]_ _P } ._

A walk W = x0e0x1e1 . . . en−1xn in G with ei ̸= ej for i ̸= j is said
to be alternating with respect to if the following three conditions are
_P_
_alternating_
satisfied for all i < n (Fig. 3.3.4):
_walk_

(i) if ei = e _[∈]_ _E [ P ], then W traverses the edge e backwards, i.e._
_xi+1 ∈_ _P˚xi for some P ∈_ _P;_

(ii) if xi = xj with i ̸= j, then xi _[∈]_ _V [ P ];_

(iii) if xi _[∈]_ _V [ P ], then { ei−1, ei } ∩_ _E [ P ] ̸= ∅.[2]_

_W_

_xn_

_x0_ _P_

_B_

_A_

_Fig. 3.3.4. An alternating walk from A to B_


-----

Let us consider a walk W = x0e0x1e1 . . . en−1xn from A ∖ _V [ P ]_ _W, xi, ei_
to B ∖ _V [ P ], alternating with respect to P. By (ii), any vertex outside_
_V [ P ] occurs at most once on W_ . Since the edges ei of W are all distinct,
(iii) implies that any vertex in V [ ] occurs at most twice on W . This
_P_
can happen in two ways: if xi = xj with 0 < i < j < n, say, then

_either ei−1, ej ∈_ _E [ P ] and ei, ej−1 /∈_ _E [ P ]_

_or ei, ej−1 ∈_ _E [ P ] and ei−1, ej /[∈]_ _E [ P ] ._

**Lemma 3.3.2. If such a walk W exists, then G contains** +1 disjoint
_|P|_
_A–B paths._

_Proof . Let H be the graph on V [ P ]_ _∪{ x0, . . ., xn } whose edge set is the_
symmetric difference of E [ P ] with { e0, . . ., en−1 }. In H, the ends of
the paths in and of W have degree 1 (or 0, if the path or W is trivial),
_P_
and all other vertices have degree 0 or 2. For each of the + 1 vertices
_|P|_
_a ∈_ (A ∩ _V [ P ]) ∪{ x0 }, therefore, the component of H containing a is_
a path, P = v0 . . . vk say, which starts in a and ends in A or B. Using _P_
conditions (i) and (iii), one easily shows by induction on i = 0, . . ., k 1
_−_
that P traverses each of its edges e = vivi+1 in the forward direction with
respect to P or W . (Formally: if e ∈ _P_ _[′]_ with P _[′ ∈]_ _P, then vi ∈_ _P_ _[′]˚vi+1;_
if e = ej ∈ _W_, then vi = xj and vi+1 = xj+1.) Hence, P ends in B. As
we have |P| + 1 disjoint such paths P, this completes the proof. 
**Third proof of Menger’s theorem. Let P be a set of as many disjoint** _P_
_A–B paths in G as possible._ Unless otherwise stated, all alternating
walks considered are alternating with respect to . We set
_P_

_A1 := A ∩_ _V [ P ]_ and _A2 := A ∖_ _A1,_ _A1, A2_
and

_B1 := B ∩_ _V [ P ]_ and _B2 := B ∖_ _B1 ._ _B1, B2_

For every path P _[∈]_ _P, let xP be the last vertex of P that lies on_ _xP_
some alternating walk starting in A2; if no such vertex exists, let xP be
the first vertex of P . Clearly, the set

_X := { xP | P_ _[∈]_ _P }_ _X_

has cardinality ; it thus suffices to show that X separates A from B.
_|P|_
Let Q be any A–B path in G; we show that Q meets X. Suppose _Q_
not. By the maximality of, the path Q meets V [ ]. Since the A–
_P_ _P_
_V [_ ] path in Q is trivially an alternating walk, Q also meets the vertex
_P_
set V [ ] of
_P_ _[′]_

_′_


-----

_y, P_ let y be the last vertex of Q in V [ ], let P be the path in containing y,
_P_ _[′]_ _P_
_x, W_ and let x := xP . Finally, let W be an alternating walk from A2 to x,
as in the definition of xP . By assumption, Q avoids X and hence x,
so y ∈ _P˚x, and W ∪_ _xPyQ is a walk from A2 to B (Fig. 3.3.5)._ If
this walk is alternating and ends in B2, we are home: then G contains
+ 1 disjoint A–B paths by Lemma 3.3.2, contrary to the maximality
_|P|_
of .
_P_

_P_ _x_

_y_

_Q_

_yQ_
_z_

_W_

_Fig. 3.3.5. Alternating walks in the third proof of Menger’s the-_
orem

How could W _xPyQ fail to be an alternating walk? For a start,_
_∪_
_W might already use an edge of xPy. But if x[′]_ is the first vertex of W
_x[′], W_ _[′]_ on xP˚y, then W _[′]_ := Wx[′]Py is an alternating walk from A2 to y. (By
_Wx[′]_ we mean the initial segment of W ending at the first occurrence of
_x[′]_ on W ; from there onwards, W _[′]_ follows P back to y.) Even our new
walk W _[′]yQ need not yet be alternating: W_ _[′]_ might still meet ˚yQ. By
definition of and W, however, and the choice of y on Q, we have
_P_ _[′]_

_V (W_ _[′]) ∩_ _V [ P ] ⊆_ _V [ P_ _[′]_ ] and _V (˚yQ) ∩_ _V [ P_ _[′]_ ] = ∅ _._

Thus, W _[′]_ and ˚yQ can meet only outside P.
_z_ If W _[′]_ does indeed meet ˚yQ, let z be the first vertex of W _[′]_ on ˚yQ. As
_z lies outside V [ P ], it occurs only once on W_ _[′]_ (condition (ii)), and we let
_W_ _[′′]_ _W_ _[′′]_ := W _[′]zQ. On the other hand if W_ _[′]_ _∩˚yQ = ∅, we set W_ _[′′]_ := W _[′]_ _∪_ _yQ._
In both cases, W _[′′]_ is alternating with respect to P _[′], because W_ _[′]_ is and ˚yQ
avoids V [ P _[′]_ ]. (Note that W _[′′]_ satisfies condition (iii) at y in the second
case, while in the first case (iii) is not applicable to z.) By definition of,
_P_ _[′]_
therefore, W _[′′]_ avoids V [ P ] ∖ _V [ P_ _[′]_ ]; in particular, V (˚yQ) ∩ _V [ P ] = ∅._
Thus W _[′′]_ is also alternating with respect to P, and it ends in B2. (Note
that y cannot be the last vertex of W _[′′], since y ∈_ _P˚x and hence y /∈_ _B.)_
Furthermore, W _[′′]_ starts in A2, because W does. We may therefore
use W _[′′]_ with Lemma 3.3.2 to obtain the desired contradiction to the
maximality of P.      

-----

A set of a–B paths is called an a–B fan if any two of the paths have _fan_
only a in common.

**Corollary 3.3.3. For B ⊆** _V and a_ _[∈]_ _V ∖_ _B, the minimum number of_ [ 10.1.2 ]
_vertices_ = a separating a from B in G is equal to the maximum number
_̸_
_of paths forming an a–B fan in G._

_Proof . Apply Theorem 3.3.1 with A := N_ (a). 
**Corollary 3.3.4. Let a and b be two distinct vertices of G.**

(i) If ab /[∈] _E, then the minimum number of vertices ̸= a, b separating_
_a from b in G is equal to the maximum number of independent_
_a–b paths in G._

(ii) The minimum number of edges separating a from b in G is equal
_to the maximum number of edge-disjoint a–b paths in G._

_Proof . (i) Apply Theorem 3.3.1 with A := N_ (a) and B := N (b).
(ii) Apply Theorem 3.3.1 to the line graph of G, with A := E(a)
and B := E(b). 
[ 4.2.10 ]
**Theorem 3.3.5. (Global Version of Menger’s Theorem)** [ 6.6.1 ]

[ 9.4.2 ]
(i) A graph is k-connected if and only if it contains k independent
_paths between any two vertices._

(ii) A graph is k-edge-connected if and only if it contains k edge_disjoint paths between any two vertices._

_Proof . (i) If a graph G contains k independent paths between any two_
vertices, then _G_ _> k and G cannot be separated by fewer than k ver-_
_|_ _|_
tices; thus, G is k-connected.
Conversely, suppose that G is k-connected (and, in particular, has
more than k vertices) but contains vertices a, b not linked by k indepen- _a, b_
dent paths. By Corollary 3.3.4 (i), a and b are adjacent; let G[′] := G _ab._ _G[′]_
_−_
Then G[′] contains at most k 2 independent a–b paths. By Corollary
_−_
3.3.4 (i), we can separate a and b in G[′] by a set X of at most k 2 _X_
_−_
vertices. As _G_ _> k, there is at least one further vertex v /[∈]_ _X_ _a, b_ _v_
_|_ _|_ _∪{_ _}_
in G. Now X separates v in G[′] from either a or b—say, from a. But
then X _b_ is a set of at most k 1 vertices separating v from a in G,
_∪{_ _}_ _−_
contradicting the k-connectedness of G.
(ii) follows straight from Corollary 3.3.4 (ii).   

-----

###### 3.4 Mader’s theorem

In analogy to Menger’s theorem we may consider the following question: given a graph G with an induced subgraph H, up to how many
independent H-paths can we find in G?
In this section, we present without proof a deep theorem of Mader,
which solves the above problem in a fashion similar to Menger’s theorem.
Again, the theorem says that an upper bound on the number of such
paths that arises naturally from the size of certain separators is indeed
attained by some suitable set of paths.
_X_ What could such an upper bound look like? Clearly, if X _V (G_ _H)_
_⊆_ _−_
_F_ and F _E(G_ _H) are such that every H-path in G has a vertex or an_
_⊆_ _−_
edge in X _F_, then G cannot contain more than _X_ _F_ independent
_∪_ _|_ _∪_ _|_
_H-paths. Hence, the least cardinality of such a set X_ _F is a natural_
_∪_
upper bound for the maximum number of independent H-paths. (Note
that every H-path meets G _H, because H is induced in G and edges_
_−_
of H do not count as H-paths.)
In contrast to Menger’s theorem, this bound can still be improved.
Clearly, we may assume that no edge in F has an end in X: otherwise
this edge would not be needed in the separator. Let Y := V (G _−_ _H)_ ∖ _X,_
_CF_ and denote by CF the set of components of the graph (Y, F ). Since every
_H-path avoiding X contains an edge from F_, it has at least two vertices
_∂C_ in ∂C for some C _[∈]_ _CF, where ∂C denotes the set of vertices in C with_
a neighbour in G _X_ _C (Fig. 3.4.1)._ The number of independent
_−_ _−_

_C_
###### CF

_∂C_

_H_
_X_

_Fig. 3.4.1. An H-path in G −_ _X_

_H-paths in G is therefore bounded above by_


� 12 _[|][∂C][|]�[�]_ _,_


_MG(H)_


� �
_MG(H) := min_ _|X| +_

_C ∈CF_


_X_ where the minimum is taken over all X and F as described above: X
_⊆_

_V (G_ _H) and F_ _E(G_ _H_ _X) such that every H-path in G has a_
_−_ _⊆_ _−_ _−_


-----

Now Mader’s theorem says that this upper bound is always attained
by some set of independent H-paths:

**Theorem 3.4.1. (Mader 1978)**
_Given a graph G with an induced subgraph H, there are always MG(H)_
_independent H-paths in G._

In order to obtain direct analogues to the vertex and edge version
of Menger’s theorem, let us consider the two special cases of the above
problem where either F or X is required to be empty. Given an induced
subgraph H ⊆ _G, we denote by κG(H) the least cardinality of a vertex_ _κG(H)_
set X _V (G_ _H) that meets every H-path in G. Similarly, we let_
_⊆_ _−_
_λG(H) denote the least cardinality of an edge set F ⊆_ _E(G) that meets_ _λG(H)_
every H-path in G.

**Corollary 3.4.2. Given a graph G with an induced subgraph H, there**
_are at least_ [1]2 _[κ][G][(][H][)][ independent][ H][-paths and at least][ 1]2_ _[λ][G][(][H][)][ edge-]_

_disjoint H-paths in G._


_Proof ._ To prove the first assertion, let k be the maximum num- _k_
ber of independent H-paths in G. By Theorem 3.4.1, there are sets
_X_ _V (G_ _H) and F_ _E(G_ _H_ _X) with_
_⊆_ _−_ _⊆_ _−_ _−_


�
_k =_ _X_ +
_|_ _|_

_C ∈CF_


� 1 �

2 _[|][∂C][|]_


such that every H-path in G has a vertex in X or an edge in F . For every
_C ∈_ _CF with ∂C ̸= ∅, pick a vertex v ∈_ _∂C and let YC := ∂C ∖_ _{ v }; if_
_∂C = ∅, let YC := ∅. Then_ � 12 _[|][∂C][|]�_ ⩾ [1]2 _[|][Y][C][|][ for all][ C][ ∈]_ _[C][F][ . Moreover,]_

for Y := [�]C ∈CF _[Y][C][ every][ H][-path has a vertex in][ X][ ∪]_ _[Y][ . Hence]_ _Y_


�
_k ⩾_ _|X| +_

_C ∈CF_


1
2 2 2 _[κ][G][(][H][)]_

_[|][Y][C][|][ ⩾]_ [1] _[|][X][ ∪]_ _[Y][ |][ ⩾]_ [1]


as claimed.
The second assertion follows from the first by considering the line
graph of G (Exercise 16). 
It may come as a surprise to see that the bounds in Corollary 3.4.2
are best possible (as general bounds): one can find examples for G and
_H where G contains no more than_ [1]2 _[κ][G][(][H][) independent][ H][-paths or no]_

more than [1]

2 _[λ][G][(][H][) edge-disjoint][ H][-paths (Exercises 17 and 18).]_


-----

###### 3.5 Edge-disjoint spanning trees

The edge version of Menger’s theorem tells us when a graph G contains k
edge-disjoint paths between any two vertices. The actual routes of these
paths within G may depend a lot on the choice of those two vertices:
having found the paths for one pair of endvertices, we are not necessarily
better placed to find them for another pair.
In a situation where quick access to a set of k edge-disjoint paths
between any two vertices is desirable, it may be a good idea to ask for
more than just k-edge-connectedness. For example, if G has k edge_disjoint spanning trees, there will be k canonical such paths between_
any two vertices, one in each tree.
When do such trees exist? If they do, the graph is clearly k-edgeconnected. The converse is easily seen to be false; indeed, it is not
even clear whether any edge-connectivity, however large, will imply the
existence of k edge-disjoint spanning trees. Our first aim in this section
will be to study conditions under which k edge-disjoint spanning trees
exist.
As before, it is easy to write down some obvious necessary conditions
for the existence of k edge-disjoint spanning trees. With respect to any
partition of V (G) into r sets, every spanning tree of G has at least r 1
_−_
_cross-edges_ _cross-edges, edges whose ends lie in different partition sets (why?). Thus_
if G has k edge-disjoint spanning trees, it has at least k (r 1) cross_−_
edges.
Once more, this obvious necessary condition is also sufficient:

**Theorem 3.5.1. (Tutte 1961; Nash-Williams 1961)**
_A multigraph contains k edge-disjoint spanning trees if and only if for_
_every partition P of its vertex set it has at least k (_ _P_ 1) cross-edges.
_|_ _| −_

Before we prove Theorem 3.5.1, let us note a surprising corollary:
to ensure the existence of k edge-disjoint spanning trees, it suffices to
raise the edge-connectivity to just 2k:

[ 6.4.4 ] **Corollary 3.5.2. Every 2k-edge-connected multigraph G has k edge-**
_disjoint spanning trees._

_Proof . Every set in a vertex partition of G is joined to other partition_
sets by at least 2k edges. Hence, for any partition into r sets, G has
at least [1]2 �ri=1 [2][k][ =][ kr][ cross-edges. The assertion thus follows from]

Theorem 3.5.1.      
_G = (V, E)_ For the proof of Theorem 3.5.1, let a multigraph G = (V, E) and
_k, F_ _k ∈_ N be given. Let F be the set of all k-tuples F = (F1, . . ., Fk) of


-----

edges, i.e. such that ∥F _∥_ := ��E [ F ]�� with E [ F ] := E(F1) ∪ _. . . ∪_ _E(Fk)_ _E[F_ ], ∥F _∥_
is as large as possible.
If F = (F1, . . ., Fk) _[∈]_ _F and e_ _[∈]_ _E ∖_ _E [ F ], then every Fi + e con-_
tains a cycle (i = 1, . . ., k): otherwise we could replace Fi by Fi + _e in F_
and obtain a contradiction to the maximality of _F_ . Let us consider
_∥_ _∥_
an edge e[′] ≠ _e of this cycle, for some fixed i. Putting Fi[′]_ [:=][ F][i][ +][ e][ −] _[e][′][,]_
and Fj[′] [:=][ F][j][ for all][ j][ ̸][=][ i][, we see that][ F][ ′][ := (][F][ ′]1[, . . ., F]k[ ′] [) is again in][ F][;]
_edge_
we say that F _[′]_ has been obtained from F by the replacement of the _replacement_
edge e[′] with e. Note that the component of Fi containing e[′] keeps its
vertex set when it changes into a component of Fi[′][. Hence for every path]
_x . . . y ⊆_ _Fi[′]_ [there is a unique path][ xF][i][y][ in][ F][i][; this will be used later.] _xFiy_
We now consider a fixed k-tuple F [0] = (F1[0][, . . ., F]k[ 0][)][ ∈] _[F][. The set]_ _F_ [0]
of all k-tuples in that can be obtained from F [0] by a series of edge
_F_
replacements will be denoted by F [0]. Finally, we let _F_ [0]

�
_E[0]_ := (E ∖ _E [ F ])_ _E[0]_

_F ∈F_ [0]

and G[0] := (V, E[0]). _G[0]_

**Lemma 3.5.3. For every e[0][ ∈]** _E ∖_ _E [ F_ [0] ] there exists a set U ⊆ _V that_
_is connected in every Fi[0]_ _[(][ i][ = 1][, . . ., k][) and contains the ends of][ e][0][.]_

_Proof . As F_ [0] _∈_ _F_ [0], we have e[0] _∈_ _E[0]; let C_ [0] be the component of G[0] _C[0]_
containing e[0]. We shall prove the assertion for U := V (C[0]). _U_
Let i _[∈]_ _{ 1, . . ., k } be given; we have to show that U is connected_ _i_
in Fi[0][. To this end, we first prove the following:]

_Let F = (F1, . . ., Fk) ∈_ _F_ [0], and let (F1[′][, . . ., F]k[ ′] [)][ have been]
_obtained from F by the replacement of an edge of Fi. If_ (1)
_x, y are the ends of a path in Fi[′]_ _[∩]_ _[C]_ [0][, then also][ xF][i][y][ ⊆] _[C]_ [0][.]

Let e = vw be the new edge in E(Fi[′][)][ ∖] _[E][ [][ F][ ]; this is the only edge of]_
_Fi[′]_ [not lying in][ F][i][. We assume that][ e][ ∈] _[xF]i[ ′][y][: otherwise we would have]_
_xFiy = xFi[′][y][ and nothing to show. It suffices to show that][ vF][i][w][ ⊆]_ _[C]_ [0][:]
then (xFi[′][y][ −] _[e][)][ ∪]_ _[vF][i][w][ is a connected subgraph of][ F][i][ ∩]_ _[C]_ [0][ that contains]
_x, y, and hence also xFiy. Let e[′]_ be any edge of vFiw. Since we could
replace e[′] in F _∈_ _F_ [0] by e and obtain an element of F [0] not containing e[′], we have e[′ ∈] _E[0]. Thus vFiw ⊆_ _G[0], and hence vFiw ⊆_ _C_ [0] since
_v, w_ _[∈]_ _xFi[′][y][ ⊆]_ _[C]_ [0][. This proves (1).]
In order to prove that U = V (C [0]) is connected in Fi[0] [we show that,]
for every edge xy _[∈]_ _C_ [0], the path xFi[0][y][ exists and lies in][ C] [0][. As][ C] [0][ is]
connected, the union of all these paths will then be a connected spanning
subgraph of Fi[0] [[][ U][ ].]
So let e = xy _[∈]_ _C_ [0] be given. As e _[∈]_ _E[0], there exist an s_ _[∈]_ N
and k-tuples F _[r]_ = (F1[r][, . . ., F]k[ r][) for][ r][ = 1][, . . ., s][ such that each][ F][ r][ is]


-----

_F := F_ _[s]_ in (1), we may think of e as a path of length 1 in Fi[′] _[∩]_ _[C]_ [0][.]
Successive applications of (1) to F = F _[s], . . ., F_ [0] then give xFi[0][y][ ⊆] _[C]_ [0]

as desired.       
(1.5.3) **Proof of Theorem 3.5.1.** We prove the backward implication by
induction on _G_ . For _G_ = 2 the assertion holds. For the induction
_|_ _|_ _|_ _|_
step, we now suppose that for every partition P of V there are at least
_k (_ _P_ 1) cross-edges, and construct k edge-disjoint spanning trees in G.
_|_ _|−_
_F_ [0] Pick a k-tuple F [0] = (F1[0][, . . ., F]k[ 0][)][ ∈] _[F][. If every][ F]i[ 0]_ [is a tree, we are]
done. If not, we have


_F_ [0] =
_∥_ _∥_


_k_
� _∥Fi[0][∥]_ _[< k][ (][|][G][| −]_ [1)]

_i=1_


by Corollary 1.5.3. On the other hand, we have ∥G∥ ⩾ _k (|G| −_ 1) by
assumption: consider the partition of V into single vertices. So there
_e[0]_ exists an edge e[0][ ∈] _E ∖_ _E [ F_ [0] ]. By Lemma 3.5.3, there exists a set
_U_ _U ⊆_ _V that is connected in every Fi[0]_ [and contains the ends of][ e][0][; in]
particular, |U _| ⩾_ 2. Since every partition of the contracted multigraph
_G/U induces a partition of G with the same cross-edges,[3]_ _G/U has at_
least k ( _P_ 1) cross-edges with respect to any partition P . By the
_|_ _| −_
induction hypothesis, therefore, G/U has k edge-disjoint spanning trees
_T1, . . ., Tk. Replacing in each Ti the vertex vU contracted from U by the_
spanning tree Fi[0] _[∩]_ _[G][ [][ U][ ] of][ G][ [][ U][ ], we obtain][ k][ edge-disjoint spanning]_
trees in G.       
_graph_
_partition_ Let us say that subgraphs G1, . . ., Gk of a graph G partition G if
their edge sets form a partition of E(G). Our spanning tree problem may
then be recast as follows: into how many connected spanning subgraphs
can we partition a given graph? The excuse for rephrasing our simple
tree problem in this more complicated way is that it now has an obvious
dual (cf. Theorem 1.5.1): into how few acyclic (spanning) subgraphs
can we partition a given graph? Or for given k: which graphs can be
partitioned into at most k forests?
An obvious necessary condition now is that every set U _V (G)_
_⊆_
induces at most k ( _U_ 1) edges, no more than _U_ 1 for each forest.
_|_ _| −_ _|_ _| −_
Once more, this condition turns out to be sufficient too. And surprisingly, this can be shown with the help of Lemma 3.5.3, which was designed
for the proof of our theorem on edge-disjoint spanning trees:

**Theorem 3.5.4. (Nash-Williams 1964)**
_A multigraph G = (V, E) can be partitioned into at most k forests if and_
_only if ∥G [ U ]∥_ ⩽ _k (|U_ _| −_ 1) for every non-empty set U ⊆ _V ._


-----

_Proof . The forward implication was shown above. Conversely, we show_ (1.5.3)
that every k-tuple F = (F1, . . ., Fk) _[∈]_ _F partitions G, i.e. that E [ F ] =_
_E. If not, let e_ _[∈]_ _E ∖_ _E [ F ]. By Lemma 3.5.3, there exists a set U ⊆_ _V_
that is connected in every Fi and contains the ends of e. Then G [ U ]
contains |U _| −_ 1 edges from each Fi, and in addition the edge e. Thus
_∥G [ U ]∥_ _> k (|U_ _| −_ 1), contrary to our assumption. 
The least number of forests forming a partition of a graph G is called
the arboricity of G. By Theorem 3.5.4, the arboricity is a measure for _arboricity_
the maximum local density: a graph has small arboricity if and only if
it is ‘nowhere dense’, i.e. if and only if it has no subgraph H with ε(H)
large.

###### 3.6 Paths between given pairs of vertices

A graph with at least 2k vertices is said to be k-linked if for every 2k dis- _k-linked_
tinct vertices s1, . . ., sk, t1, . . ., tk it contains k disjoint paths P1, . . ., Pk
with Pi = si . . . ti for all i. Thus unlike in Menger’s theorem, we are not
merely asking for k disjoint paths between two sets of vertices: we insist
that each of these paths shall link a specified pair of endvertices.
Clearly, every k-linked graph is k-connected. The converse, however,
is far from true: being k-linked is generally a much stronger property
than k-connectedness. But still, the two properties are related: our aim
in this section is to prove the existence of a function f : N → N such that
every f (k)-connected graph is k-linked.
As a lemma, we need a result that would otherwise belong in Chapter 8:

**Theorem 3.6.1. (Mader 1967)**
_There is a function h: N →_ N such that every graph with average degree
_at least h(r) contains K_ _[r]_ _as a topological minor, for every r ∈_ N.

(1.2.2)
_Proof . For r ⩽_ 2, the assertion holds with h(r) = 1; we now assume that (1.3.1)
_r ⩾_ 3. We show by induction on m = r, . . ., �2r� that every graph G with
average degreem edges; for m d =(G�)2r ⩾� this implies the assertion with2[m] has a topological minor X with h(r) = 2 r vertices and[(]r2[)].
If m = r then, by Propositions 1.2.2 and 1.3.1, G contains a cycle
of length at least ε(G) + 1 ⩾ 2[r][−][1] + 1 ⩾ _r + 1, and the assertion follows_
with X = C _[r]._
Now let r < m ⩽ �2r�, and assume the assertion holds for smaller m.
Let G with d(G) ⩾ 2[m] be given; thus, ε(G) ⩾ 2[m][−][1]. Since G has a
component C with ε(C) ⩾ _ε(G), we may assume that G is connected._
( )


-----

_ε(G/U_ ) ⩾ 2[m][−][1]; such a set U exists, because G itself has the form G/U
with _U_ = 1. Since G is connected, we have N (U ) = .
_|_ _|_ _̸_ _∅_
_H_ Let H := G [ N (U ) ]. If H has a vertex v of degree dH (v) < 2[m][−][1], we
may add it to U and obtain a contradiction to the maximality of U : when
we contract the edge vvU in G/U, we lose one vertex and dH (v) + 1 ⩽
2[m][−][1] edges, so ε will still be at least 2[m][−][1]. Therefore d(H) ⩾ _δ(H) ⩾_
2[m][−][1]. By the induction hypothesis, H contains a TY with _Y_ = r
_|_ _|_
and _Y_ = m 1. Let x, y be two branch vertices of this TY that are
_∥_ _∥_ _−_
non-adjacent in Y . Since x and y lie in N (U ) and U is connected in G,
_G contains an x–y path whose inner vertices lie in U_ . Adding this path
to the TY, we obtain the desired TX.      
How can Theorem 3.6.1 help with our aim to show that high connectivity will make a graph k-linked? Since high connectivity forces the
average degree up (even the minimum degree), we may assume by the
theorem that our graph contains a subdivision K of a large complete
graph. Our plan now is to use Menger’s theorem to link the given vertices si and ti disjointly to branch vertices of K, and then to join up the
correct pairs of those branch vertices inside K.

**Theorem 3.6.2. (Jung 1970; Larman & Mani 1970)**
_There is a function f_ : N → N such that every f (k)-connected graph is
_k-linked, for all k_ _[∈]_ N.

(3.3.1) _Proof ._ We prove the assertion for f (k) = h(3k) + 2k, where h is a
_G_ function as in Theorem 3.6.1. Let G be an f (k)-connected graph. Then
_K_ _d(G) ⩾_ _δ(G) ⩾_ _κ(G) ⩾_ _h(3k); choose K = TK_ [3][k] _⊆_ _G as in Theorem_
_U_ 3.6.1, and let U denote its set of branch vertices.
_si, ti_ For the proof that G is k-linked, let distinct vertices s1, . . ., sk and
_t1, . . ., tk of G be given._ By definition of f (k), we have κ(G) ⩾ 2k.
Hence by Menger’s theorem (3.3.1), G contains disjoint paths P1, . . ., Pk,
_Pi, Qi_ _Q1, . . ., Qk, such that each Pi starts in si, each Qi starts in ti, and all_
_P_ these paths end in U but have no inner vertices in U . Let the set P of
these paths be chosen so that their total number of edges outside E(K)
is as small as possible.
_ui_ Let u1, . . ., uk be those k vertices in U that are not an end of a
_Li_ path in P. For each i = 1, . . ., k, let Li be the U -path in K (i.e., the
_vi_ subdivided edge of the K [3][k]) from ui to the end of Pi in U, and let vi be
the first vertex of Li on any path P _[∈]_ _P. By definition of P, P has no_
more edges outside E(K) than PviLiui does, so viP = viLi and hence
_Mi_ _P = Pi (Fig. 3.6.1). Similarly, if Mi denotes the U_ -path in K from ui
_wi_ to the end of Qi in U, and wi denotes the first vertex of Mi on any
path in P, then this path is Qi. Then the paths siPiviLiuiMiwiQiti are


-----

_ui_


_si_ _P_ _wi_

_vi_ _Qi_ _ti_

_Pi_ _Li_ _Mi_

_Fig. 3.6.1. Constructing an si–ti path via ui_

In our proof of Theorem 3.6.2 we did not try to find any particularly
good bound on the connectivity needed to force a graph to be k-linked;
the function f we used grows exponentially in k. Not surprisingly, this
is far from being best possible. It is still remarkable, though, that f can
in fact be chosen linear: as Bollob´as & Thomason (1996) have shown,
every 22k-connected graph is k-linked.

###### Exercises

For the first three exercises, let G be a graph and a, b _[∈]_ _V (G). Suppose that_
_X ⊆_ _V (G)_ ∖ _{ a, b } separates a from b in G. We say that X separates a from b_
_minimally if no proper subset of X separates a from b in G._

1.[−] Show that X separates a from b minimally if and only if every vertex
in X has a neighbour in the component Ca of G − _X containing a, and_
another in the component Cb of G − _X containing b._

2. Let X _[′]_ _⊆_ _V (G) ∖_ _{ a, b } be another set separating a from b, and define_
_Ca[′]_ [and][ C]b[′] [correspondingly. Show that both]

_Ya := (X ∩_ _Ca[′]_ [)][ ∪] [(][X][ ∩] _[X]_ _[′][)][ ∪]_ [(][X] _[′][ ∩]_ _[C]a[)]_
and

_Yb := (X ∩_ _Cb[′]_ [)][ ∪] [(][X][ ∩] _[X]_ _[′][)][ ∪]_ [(][X] _[′][ ∩]_ _[C]b[)]_

separate a from b (see figure).

_X_ _[′]_ _X_


_X_


_X_ _[′]_


3. Do Ya and Yb separate a from b minimally if X and X _[′]_ do? Are |Ya|
and |Yb| minimal for vertex sets separating a from b if |X| and |X _[′]| are?_

4. Let X and X _[′]_ be minimal separating vertex sets in G such that X
meets at least two components of G − _X_ _[′]. Show that X_ _[′]_ meets all the


-----

5.[−] Prove the elementary properties of blocks mentioned at the beginning
of Section 3.1.

6. Show that the block graph of any connected graph is a tree.

7. Show, without using Menger’s theorem, that any two vertices of a 2connected graph lie on a common cycle.

8. For edges e, e[′ ∈] _G write e ∼_ _e[′]_ if either e = e[′] or e and e[′] lie on some
common cycle in G. Show that ∼ is an equivalence relation on E(G)
whose equivalence classes are the edge sets of the non-trivial blocks
of G.

9. Let G be a 2-connected graph but not a triangle, and let e be an edge
of G. Show that either G − _e or G/e is again 2-connected._

10. Let G be a 3-connected graph, and let xy be an edge of G. Show that
_G/xy is 3-connected if and only if G −{ x, y } is 2-connected._

11. (i) Show that every cubic 3-edge-connected graph is 3-connected.

(ii) Show that a graph is cubic and 3-connected if and only if it can
be constructed from a K [4] by successive applications of the following
operation: subdivide two edges by inserting a new vertex on each of
them, and join the two new subdividing vertices by an edge.

12.[−] Show that Menger’s theorem is equivalent to the following statement.
For every graph G and vertex sets A, B ⊆ _V (G), there exist a set P of_
disjoint A–B paths in G and a set X ⊆ _V (G) separating A from B in_
_G such that X has the form X = { xP | P_ _[∈]_ _P } with xP_ _∈_ _P for all_
_P_ _[∈]_ _P._

13. Work out the details of the proof of Corollary 3.3.4 (ii).

14. Let k ⩾ 2. Show that every k-connected graph of order at least 2k
contains a cycle of length at least 2k.

15. Let k ⩾ 2. Show that in a k-connected graph any k vertices lie on a
common cycle.

16. Derive the edge part of Corollary 3.4.2 from the vertex part.

(Hint. Consider the H-paths in the graph obtained from the disjoint
union of H and the line graph L(G) by adding all the edges he such
that h is a vertex of H and e _[∈]_ _E(G) ∖_ _E(H) is an edge at h.)_

17.[−] To the disjoint union of the graph H = K [2][m][+1] with k copies of K [2][m][+1]

add edges joining H bijectively to each of the K [2][m][+1]. Show that the
resulting graph G contains at most km = 12 _[κ][G][(][H][) independent][ H][-]_
paths.

18. Find a bipartite graph G, with partition classes A and B say, such that
1


-----

19.[+] Derive Tutte’s 1-factor theorem (2.2.1) from Mader’s theorem.

(Hint. Extend the given graph G to a graph G[′] by adding, for each
vertex v _[∈]_ _G, a new vertex v[′]_ and joining v[′] to v. Choose H ⊆ _G[′]_ so that
the 1-factors in G correspond to the large enough sets of independent
_H-paths in G[′].)_

20. Find the error in the following short ‘proof’ of Theorem 3.5.1. Call a
partition non-trivial if it has at least two classes and at least one of the
classes has more than one element. We show by induction on |V | + |E|
that G = (V, E) has k edge-disjoint spanning trees if every non-trivial
partition of V into r sets (say) has at least k(r − 1) cross-edges. The
induction starts trivially with G = K [1] if we allow k copies of K [1] as a
family of k edge-disjoint spanning trees of K [1]. We now consider the
induction step. If every non-trivial partition of V into r sets (say) has
more than k(r − 1) cross-edges, we delete any edge of G and are done by
induction. So V has a non-trivial partition { V1, . . ., Vr } with exactly
_k(r −_ 1) cross-edges. Assume that |V1| ⩾ 2. If G[′] := G [ V1 ] has k
disjoint spanning trees, we may combine these with k disjoint spanning
trees that exist in G/V1 by induction. We may thus assume that G[′]

has no k disjoint spanning trees. Then by induction it has a non-trivial
vertex partition { V1[′][, . . ., V][ ′]s _[}][ with fewer than][ k][(][s][ −]_ [1) cross-edges.]
Then { V1[′][, . . ., V][ ′]s _[, V]2[, . . ., V]r_ _[}][ is a non-trivial vertex partition of][ G][ into]_
_r + s −_ 1 sets with fewer than k(r − 1) + k(s − 1) = k((r + s − 1) − 1)
cross-edges, a contradiction.

21.[−] Show that every k-linked graph is (2k − 1)-connected.

###### Notes

Although connectivity theorems are doubtless among the most natural, and
also the most applicable, results in graph theory, there is still no comprehensive
monograph on this subject. Some areas are covered in B. Bollob´as, Extremal
_Graph Theory, Academic Press 1978, in R. Halin, Graphentheorie, Wissen-_
schaftliche Buchgesellschaft 1980, and in A. Frank’s chapter of the Handbook of
_Combinatorics (R.L. Graham, M. Gr¨otschel & L. Lov´asz, eds.), North-Holland_
1995. A survey specifically of techniques and results on minimally k-connected
graphs (see below) is given by W. Mader, On vertices of degree n in minimally
_n-connected graphs and digraphs, in (D. Mikl´os, V.T. S´os & T. Sz˝onyi, eds.)_
_Paul Erd˝os is 80, Vol. 2, Proc. Colloq. Math. Soc. J´anos Bolyai, Budapest 1996._
Our proof of Tutte’s Theorem 3.2.3 is due to C. Thomassen, Planarity and
duality of finite and infinite graphs, J. Combin. Theory B 29 (1980), 244–271.
This paper also contains Lemma 3.2.1 and its short proof from first principles.
(The lemma’s assertion, of course, follows from Tutte’s wheel theorem—its
significance lies in its independent proof, which has shortened the proofs of
both of Tutte’s theorems considerably.)
An approach to the study of connectivity not touched upon in this chapter is the investigation of minimal k-connected graphs, those that lose their
_k-connectedness as soon as we delete an edge. Like all k-connected graphs,_


-----

(1969), their minimum degree is exactly k. The existence of a vertex of small
degree can be particularly useful in induction proofs about k-connected graphs.
Halin’s theorem was the starting point for a series of more and more sophisticated studies of minimal k-connected graphs; see the books of Bollob´as and
Halin cited above, and in particular Mader’s survey.
Our first proof of Menger’s theorem is due to T. B¨ohme, F. G¨oring and
J. Harant (manuscript 1999); the second to J.S. Pym, A proof of Menger’s
theorem, Monatshefte Math. 73 (1969), 81–88; the third to T. Gr¨unwald (later
Gallai), Ein neuer Beweis eines Mengerschen Satzes, J. London Math. Soc. 13
(1938), 188–192. The global version of Menger’s theorem (Theorem 3.3.5) was
first stated and proved by Whitney (1932).
Mader’s Theorem 3.4.1 is taken from W. Mader, Uber die Maximalzahl[¨]
kreuzungsfreier H -Wege, Arch. Math. 31 (1978), 387–402. The theorem may
be viewed as a common generalization of Menger’s theorem and Tutte’s 1factor theorem (Exercise 19). Theorem 3.5.1 was proved independently by
Nash-Williams and by Tutte; both papers are contained in J. London Math.
_Soc. 36 (1961). Theorem 3.5.4 is due to C.St.J.A. Nash-Williams, Decompo-_
sitions of finite graphs into forests, J. London Math. Soc. 39 (1964), 12. Our
proofs follow an account by Mader (personal communication). Both results
can be elegantly expressed and proved in the setting of matroids; see § 18 in
B. Bollob´as, Combinatorics, Cambridge University Press 1986.
In Chapter 8.1 we shall prove that, in order to force a topological K _[r]_ minor in a graph G, we do not need an average degree of G as high as h(r) = 2[(][r]2[)]

(as used in our proof of Theorem 3.6.1): the average degree required can
be bounded above by a function quadratic in r (Theorem 8.1.1). The improvement of Theorem 3.6.2 mentioned in the text is due to B. Bollob´as &
A.G. Thomason, Highly linked graphs, Combinatorica 16 (1996), 313–320.
N. Robertson & P.D. Seymour, Graph Minors XIII: The disjoint paths problem, J. Combin. Theory B 63 (1995), 65-110, showed that, for every fixed k,
there is an O(n[3]) algorithm that decides whether a given graph of order n is
_k-linked. If k is taken as part of the input, the problem becomes NP-hard._


-----

# 4 Planar Graphs

When we draw a graph on a piece of paper, we naturally try to do this
as transparently as possible. One obvious way to limit the mess created
by all the lines is to avoid intersections. For example, we may ask if we
can draw the graph in such a way that no two edges meet in a point
other than a common end.
Graphs drawn in this way are called plane graphs; abstract graphs
that can be drawn in this way are called planar . In this chapter we
study both plane and planar graphs—as well as the relationship between
the two: the question of how an abstract graph might be drawn in
fundamentally different ways. After collecting together in Section 4.1 the
few basic topological facts that will enable us later to prove all results
rigorously without too much technical ado, we begin in Section 4.2 by
studying the structural properties of plane graphs. In Section 4.3, we
investigate how two drawings of the same graph can differ. The main
result of that section is that 3-connected planar graphs have essentially
only one drawing, in some very strong and natural topological sense. The
next two sections are devoted to the proofs of all the classical planarity
criteria, conditions telling us when an abstract graph is planar. We
complete the chapter with a section on plane duality, a notion with
fascinating links to algebraic, colouring, and flow properties of graphs
(Chapters 1.9 and 6.5).
The traditional notion of a graph drawing is that its vertices are
represented by points in the Euclidean plane, its edges are represented by
curves between these points, and different curves meet only in common
endpoints. To avoid unnecessary topological complication, however, we
shall only consider curves that are piecewise linear; it is not difficult to
show that any drawing can be straightened out in this way, so the two
notions come to the same thing.


-----

###### 4.1 Topological prerequisites

In this section we briefly review some basic topological definitions and
facts needed later. All these facts have (by now) easy and well-known
proofs; see the notes for sources. Since those proofs contain no graph
theory, we do not repeat them here: indeed our aim is to collect precisely
those topological facts that we need but do not want to prove. Later,
all proofs will follow strictly from the definitions and facts stated here
(and be guided by but not rely on geometric intuition), so the material
presented now will help to keep elementary topological arguments in
those proofs to a minimum.
A straight line segment in the Euclidean plane is a subset of R[2] that
has the form { p + λ(q − _p) | 0 ⩽_ _λ ⩽_ 1 } for distinct points p, q _[∈]_ R[2].
_polygon_ A polygon is a subset of R[2] which is the union of finitely many straight
line segments and is homeomorphic to the unit circle. Here, as later, any
subset of a topological space is assumed to carry the subspace topology.
A polygonal arc is a subset of R[2] which is the union of finitely many
straight line segments and is homeomorphic to the closed unit interval

[ 0, 1 ]. The images of 0 and of 1 under such a homeomorphism are the
_endpoints of this polygonal arc, which links them and runs between them._
_arc_ Instead of ‘polygonal arc’ we shall simply say arc. If P is an arc between
_x and y, we denote the point set P ∖_ _{ x, y }, the interior of P_, by P[˚].
Let O ⊆ R[2] be an open set. Being linked by an arc in O defines
an equivalence relation on O. The corresponding equivalence classes are
_region_ again open; they are the regions of O. A closed set X ⊆ R[2] is said to
_separate_ _separate O if O ∖_ _X has more than one region. The frontier of a set_
_frontier_ _X ⊆_ R[2] is the set Y of all points y _[∈]_ R[2] such that every neighbourhood
of y meets both X and R[2] ∖ _X. Note that if X is open then its frontier_
lies in R[2] ∖ _X._
The frontier of a region O of R[2] ∖ _X, where X is a finite union of_
points and arcs, has two important properties. The first is accessibility:
if x _[∈]_ _X lies on the frontier of O, then x can be linked to some point in O_
by a straight line segment whose interior lies wholly inside O. As a consequence, any two points on the frontier of O can be linked by an arc whose
interior lies in O (why?). The second notable property of the frontier of
_O is that it separates O from the rest of R[2]. Indeed, if ϕ: [ 0, 1 ]_ _→_ _P ⊆_ R[2]

is continuous, with ϕ(0) ∈ _O and ϕ(1) /∈_ _O, then P meets the frontier of_
_O at least in the point ϕ(y) for y := inf { x | ϕ(x) /[∈]_ _O }, the first point_
of P in R[2] ∖ _O._

[ 4.2.1 ]

[ 4.2.4 ]

[ 4.2.5 ] **Theorem 4.1.1. (Jordan Curve Theorem for Polygons)**

[ 4.2.10 ]

[ 4.3.1 ] _For every polygon P ⊆_ R[2], the set R[2] ∖ _P has exactly two regions, of_

[ 4.5.1 ] _which exactly one is bounded. Each of the two regions has the entire_


-----

With the help of Theorem 4.1.1, it is not difficult to prove the
following lemma.

[ 4.2.5 ]
**Lemma 4.1.2. Let P1, P2, P3 be three arcs, between the same two end-** [ 4.2.6 ]
_point but otherwise disjoint._ [ 4.2.10 ]
(i) R[2] ∖ (P1 ∪ _P2 ∪_ _P3) has exactly three regions, with frontiers_
_P1_ _P2, P2_ _P3 and P1_ _P3._
_∪_ _∪_ _∪_
(ii) If P is an arc between a point in _P[˚]1 and a point in_ _P[˚]3 whose_
_interior lies in the region of R[2]_ ∖ (P1 ∪ _P3) that contains_ _P[˚]2, then_
_P˚ ∩_ _P[˚]2 ̸= ∅._


_P1_


_P2_
_P3_


_Fig. 4.1.1. The arcs in Lemma 4.1.2 (ii)_

Our next lemma complements the Jordan curve theorem by saying
that an arc does not separate the plane. For easier application later, we
phrase this a little more generally:

[ 4.2.1 ]
**Lemma 4.1.3. Let X1, X2 ⊆** R[2] _be disjoint sets, each the union of_ [ 4.2.3 ]
_finitely many points and arcs, and let P be an arc between a point in_
_X1 and one in X2 whose interior_ _P[˚] lies in a region O of R[2]_ ∖ (X1 _X2)._
_∪_
_Then O ∖_ _P[˚] is a region of R[2]_ ∖ (X1 ∪ _P ∪_ _X2)._

_P_

_O_

_X1_ _X2_

_Fig. 4.1.2. P does not separate the region O of R[2]_ ∖ (X1 ∪ _X2)_

It remains to introduce a few terms and facts that will be used only
once, when we consider notions of equivalence for graph drawings in
Chapter 4.3.
As usual, we denote by S[n] the n-dimensional sphere, the set of _S[n]_
points in R[n][+1] at distance 1 from the origin. The 2-sphere minus its
‘north pole’ (0, 0, 1) is homeomorphic to the plane; let us choose a fixed
such homeomorphism π: S[2] ∖ _{ (0, 0, 1) }→_ R[2] (for example, stereograph- _π_


-----

R[2] ∖ _P_, let us call C := π[−][1](P ) a circle on S[2], and the sets π[−][1](O) and
_S[2]_ ∖ _π[−][1](P ∪_ _O) the regions of C._
Our last tool is the theorem of Jordan and Schoenflies, again adapted slightly for our purposes:

[ 4.3.1 ] **Theorem 4.1.4. Let ϕ: C1** _C2 be a homeomorphism between two_
_→_
_circles on S[2], let O1 be a region of C1, and let O2 be a region of C2._
_Then ϕ can be extended to a homeomorphism C1 ∪_ _O1 →_ _C2 ∪_ _O2._

###### 4.2 Plane graphs

_plane_
A plane graph is a pair (V, E) of finite sets with the following properties
_graph_
(the elements of V are again called vertices, those of E edges):

(i) V ⊆ R[2];
(ii) every edge is an arc between two vertices;
(iii) different edges have different sets of endpoints;
(iv) the interior of an edge contains no vertex and no point of any
other edge.

A plane graph (V, E) defines a graph G on V in a natural way. As long
as no confusion can arise, we shall use the name G of this abstract graph
also for the plane graph (V, E), or for the point set V _E; similar_
_∪_ [�]
notational conventions will be used for abstract versus plane edges, for
subgraphs, and so on.[1]

For every plane graph G, the set R[2] ∖ _G is open; its regions are the_
_faces_ _faces of G. Since G is bounded—i.e., lies inside some sufficiently large_
disc D—exactly one of its faces is unbounded: the face that contains
R[2] ∖ _D. This face is the outer face of G; the other faces are its inner_
_F_ (G) _faces. We denote the set of faces of G by F_ (G). Note that if H _G_
_⊆_
then every face of G is contained in a face of H.
In order to lay the foundations for the (easy but) rigorous introduction to plane graphs that this section aims to provide, let us descend
once now into the realm of truly elementary topology of the plane, and
prove what seems entirely obvious:[2] that the frontier of a face of a plane
graph G is always a subgraph of G—not, say, half an edge. The following lemma states this formally, together with two similarly ‘obvious’
properties of plane graphs:

1 However, we shall continue to use ∖ for differences of point sets and − for graph
differences—which may help a little to keep the two apart.
2 Note that even the best intuition can only ever be ‘accurate’, i.e., coincide with
what the technical definitions imply, inasmuch as those definitions do indeed formalize what is intuitively intended. Given the complexity of definitions in elementary


-----

[ 4.5.1 ]
**Lemma 4.2.1. Let G be a plane graph and e an edge of G.**

[ 4.5.2 ]
(i) If X is the frontier of a face of G, then either e _X or X_ ˚e = _._
_⊆_ _∩_ _∅_

(ii) If e lies on a cycle C _G, then e lies on the frontier of exactly_
_⊆_
_two faces of G, and these are contained in distinct faces of C._

(iii) If e lies on no cycle, then e lies on the frontier of exactly one face
_of G._

(4.1.1)
_Proof . We prove all three assertions together. Let us start by considering_
(4.1.3)
one point x0 ∈ ˚e. We show that x0 lies on the frontier of either exactly
two faces or exactly one, according as e lies on a cycle in G or not. We
then show that every other point in ˚e lies on the frontier of exactly the
same faces as x0. Then the endpoints of e will also lie on the frontier of
these faces—simply because every neighbourhood of an endpoint of e is
also the neighbourhood of an inner point of e.
_G is the union of finitely many straight line segments; we may as-_
sume that any two of these intersect in at most one point. Around every
point x ∈ ˚e we can find an open disc Dx, with centre x, which meets _Dx_
only those (one or two) straight line segments that contain x.
Let us pick an inner point x0 from a straight line segment S ⊆ _e._ _x0, S_
Then Dx0 ∩ _G = Dx0 ∩_ _S, so Dx0 ∖_ _G is the union of two open half-discs._
Since these half-discs do not meet G, they each lie in a face of G. Let
us denote these faces by f1 and f2; they are the only faces of G with x0 _f1, f2_
on their frontier, and they may coincide (Fig. 4.2.1).


_f1_


_Dx0_

_x0_
_f2_


_Fig. 4.2.1. Faces f1, f2 of G in the proof of Lemma 4.2.1_

If e lies on a cycle C ⊆ _G, then Dx0 meets both faces of C (Theo-_
rem 4.1.1). The faces f1, f2 of G are therefore contained in distinct faces
of C—since C _G, every face of G is a subset of a face of C—and in_
_⊆_
particular f1 ̸= f2. If e does not lie on any cycle, then e is a bridge and
thus links two disjoint point sets X1, X2 with X1 _X2 = G ∖˚e. Clearly,_
_∪_
_f1 ∪˚e ∪_ _f2 is the subset of a face f of G −_ _e. (Why?) By Lemma 4.1.3,_
_f ∖˚e is a face of G. But f ∖˚e contains f1 and f2 by definition of f_, so
_f1 = f ∖˚e = f2 since f1, f2 and f are all faces of G._
Now consider any other point x1 _[∈]_ ˚e. Let P be the arc from x0 to _x1_
_x1 contained in e. Since P is compact, finitely many of the discs Dx_ _P_
with x ∈ _P cover P_ . Let us enumerate these discs as D0, . . ., Dn in the _D0, . . ., Dn_
natural order of their centres along P ; adding Dx0 or Dx1 as necessary,
we may assume that D0 = Dx0 and Dn = Dx1. By induction on n, one


-----

_z_ (D0 ∪ _. . . ∪_ _Dn) ∖_ _e to a point z_ _[∈]_ _D0 ∖_ _e (Fig. 4.2.2); then y and z are_
equivalent in R[2] ∖ _G. Hence, every point of Dn ∖_ _e lies in f1 or in f2, so_
_x1 cannot lie on the frontier of any other face of G. Since both half-discs_
of D0 ∖ _e can be linked to Dn ∖_ _e in this way (swap the roles of D0_
and Dn), we find that x1 lies on the frontier of both f1 and f2.       
_y_

_e_

_z_

_x0_ _x1_

_D0_ _P_ _Dn_

_Fig. 4.2.2. An arc from y to D0, close to P_

**Corollary 4.2.2. The frontier of a face is always the point set of a**
_subgraph._      
The subgraph of G whose point set is the frontier of a face f is said to
_boundary_ _bound f and is called its boundary; we denote it by G [ f ]. A face is_
_G [ f ]_ said to be incident with the vertices and edges of its boundary. Note
that if H ⊆ _G then every face f of G is contained in a face f_ _[′]_ of H. If
_G [ f ] ⊆_ _H then f = f_ _[′]_ (why?); in particular, f is always also a face of
its own boundary G [ f ]. These basic facts will be used frequently in the
proofs to come.

[ 4.6.1 ] **Proposition 4.2.3. A plane forest has exactly one face.**

(4.1.3) _Proof . Use induction on the number of edges and Lemma 4.1.3._ 
With just one exception, different faces of a plane graph have different boundaries:

[ 4.3.1 ] **Lemma 4.2.4. If a plane graph has different faces with the same bound-**
_ary, then the graph is a cycle._

(4.1.1) _Proof . Let G be a plane graph, and let H_ _G be the boundary of_
_⊆_
distinct faces f1, f2 of G. Since f1 and f2 are also faces of H, Proposition
4.2.3 implies that H contains a cycle C. By Lemma 4.2.1 (ii), f1 and f2
are contained in different faces of C. Since f1 and f2 both have all of H
as boundary, this implies that H = C: any further vertex or edge of H
would lie in one of the faces of C and hence not on the boundary of the
other. Thus, f1 and f2 are distinct faces of C. As C has only two faces,
it follows that f1 ∪ _C ∪_ _f2 = R[2]_ and hence G = C.       
[ 4.3.1 ]

[ 4.4.3 ]

**Proposition 4.2.5. In a 2-connected plane graph, every face is bounded**

[ 4 5 1 ]


-----

_Proof . Let f be a face in a 2-connected plane graph G. We show by_ (3.1.2)
(4.1.1)
induction on _G_ that G [ f ] is a cycle. If G is itself a cycle, this holds
_|_ _|_ (4.1.2)
by Theorem 4.1.1; we therefore assume that G is not a cycle.
By Proposition 3.1.2, there exist a 2-connected plane graph H _G_ _H_
_⊆_
and a plane H-path P such that G = H _P_ . The interior of P lies in a _P_
_∪_
face f _[′]_ of H, which by the induction hypothesis is bounded by a cycle C. _f_ _[′], C_
If f is also a face of H, we are home by the induction hypothesis.
If not, then the frontier of f meets P ∖ _H, so f ⊆_ _f_ _[′]. Therefore f is a_
face of C ∪ _P_, and is hence bounded by a cycle (Lemma 4.1.2 (i)). 
_maximal_
A plane graph G is called maximally plane, or just maximal, if we
_plane graph_
cannot add a new edge to form a plane graph G[′] ⫌ _G with V (G[′]) = V (G)._
We call G a plane triangulation if every face of G (including the outer _plane_
face) is bounded by a triangle. _triangulation_

[ 4.4.1 ]
**Proposition 4.2.6. A plane graph of order at least 3 is maximally plane**

[ 5.4.2 ]
_if and only if it is a plane triangulation._

_Proof . Let G be a plane graph of order at least 3. It is easy to see that_ (4.1.2)
if every face of G is bounded by a triangle, then G is maximally plane.
Indeed, any additional edge e would have its interior inside a face of G
and its ends on the boundary of that face. Hence these ends are already
adjacent in G, so G _e cannot satisfy condition (iii) in the definition of_
_∪_
a plane graph.
Conversely, assume that G is maximally plane and let f _[∈]_ _F_ (G) be _f_
a face; let us write H := G [ f ]. Since G is maximal as a plane graph, _H_
_G [ H ] is complete: any two vertices of H that are not already adjacent_
in G could be linked by an arc through f, extending G to a larger plane
graph. Thus G [ H ] = K _[n]_ for some n—but we do not know yet which _n_
edges of G [ H ] lie in H.
Let us show first that H contains a cycle. If not, then G ∖ _H ̸= ∅:_
by G ⊇ _K_ _[n]_ if n ⩾ 3, or else by |G| ⩾ 3. On the other hand we have
_f ∪_ _H = R[2]_ by Proposition 4.2.3 and hence G = H, a contradiction.
Since H contains a cycle, it suffices to show that n ⩽ 3: then H = K[3]

as claimed. Suppose n ⩾ 4, and let C = v1v2v3v4v1 be a cycle in G [ H ] _C, vi_
(= K _[n]). By C ⊆_ _G, our face f is contained in a face fC of C; let fC[′]_
be the other face of C. Since the vertices v1 and v3 lie on the boundary _fC_ _, fC[′]_
of f, they can be linked by an arc whose interior lies in fC and avoids G.


_v_


_C_


_fC ⊇_ _f_ _v4_

_v3_


-----

Hence by Lemma 4.1.2 (ii), the plane edge v2v4 of G [ H ] runs through
_fC[′]_ [rather than][ f][C][ (Fig. 4.2.3). Analogously, since][ v][2][, v][4][ ∈] _[G][ [][ f][ ], the]_

edge v1v3 runs through fC[′] [. But the edges][ v][1][v][3][ and][ v][2][v][4][ are disjoint, so]

this contradicts Lemma 4.1.2 (ii).� 
The following classic result of Euler (1752)—here stated in its sim
plest form, for the plane—marks one of the common origins of graph
theory and topology. The theorem relates the number of vertices, edges
and faces in a plane graph: taken with the correct signs, these numbers
always add up to 2. The general form of Euler’s theorem asserts the same
for graphs suitably embedded in other surfaces, too: the sum obtained
is always a fixed number depending only on the surface, not on the
graph, and this number differs for distinct (orientable closed) surfaces.
Hence, any two such surfaces can be distinguished by a simple arithmetic
invariant of the graphs embedded in them![3]

Let us then prove Euler’s theorem in its simplest form:

**Theorem 4.2.7. (Euler’s Formula)**

_Let G be a connected plane graph with n vertices, m edges, and ℓ_ _faces._

_Then_

_n_ _m + ℓ_ = 2 .
_−_


(1.5.1)
(1.5.3) _Proof . We fix n and apply induction on m. For m ⩽_ _n −_ 1, G is a tree

and m = n 1 (why?), so the assertion follows from Proposition 4.2.3.
_−_

_e, G[′]_ Now let m ⩾ _n. Then G has an edge e lying on a cycle; let G[′]_ :=

_f1, f2_ _G −_ _e. By Lemma 4.2.1 (ii), e lies on the boundary of exactly two faces_

_f1,2_ _f1, f2 of G; we put f1,2 := f1 ∪˚e ∪_ _f2. We shall prove that_

_F_ (G) ∖ _{ f1, f2 } = F_ (G[′]) ∖ _{ f1,2 }, ψ_ (∗)

without assuming that f1,2 _[∈]_ _F_ (G[′]). However, since ˚e must lie in some
face of G[′] and this will not be a face of G, by (∗) it can only be f1,2.
Thus again by (∗), G[′] has one face less than G. As G[′] also has one edge
less than G, the assertion then follows from the induction hypothesis
for G[′].

For our proof of (∗) we first consider any f _[∈]_ _F_ (G) ∖ _{ f1, f2 }. By_

Lemma 4.2.1 (i), we have G [ f ] ⊆ _G ∖˚e = G[′]. So f is also a face of G[′]_

(but obviously not equal to f1,2) and hence lies in F (G[′]) ∖ _{ f1,2 }._

_f_ _[′]_ Conversely, let a face f _[′]_ ≠ _f1,2 of G[′]_ be given. Since e lies on the

boundary of both f1 and f2, we can link any two points of f1,2 by an

_f1[′],2_ arc in R[2] ∖ _G[′], so f1,2 lies inside a face f1[′],2_ [of][ G][′][.] Our assumption

of f _[′]_ ≠ _f1,2 therefore implies f_ _[′]_ _̸⊆_ _f1,2 (as otherwise f_ _[′]_ _⊆_ _f1,2 ⊆_ _f1[′],2_

3 This fundamental connection between graphs and surfaces lies at the heart of


-----

and hence f _[′]_ = f1,2 = f1[′],2[); let][ x][ be a point in][ f][ ′][ ∖] _[f][1][,][2][. Then][ x][ lies]_ _x_
in some face f ̸= f1, f2 of G. As shown above, f is also a face of G[′]. _f_
Hence x ∈ _f ∩_ _f_ _[′]_ implies f = f _[′], and we have f_ _[′ ∈]_ _F_ (G) ∖ _{ f1, f2 } as_
desired. 
[ 4.4.1 ]
**Corollary 4.2.8. A plane graph with n ⩾** 3 vertices has at most 3n _−_ 6 [ 5.1.2 ]
_edges. Every plane triangulation with n vertices has 3n_ 6 edges. [ 8.3.5 ]
_−_

_Proof . By Proposition 4.2.6 it suffices to prove the second assertion. In a_
plane triangulation G, every face boundary contains exactly three edges,
and every edge lies on the boundary of exactly two faces (Lemma 4.2.1).
The bipartite graph on E(G) _F_ (G) with edge set _ef_ _e_ _G [ f ]_ thus
_∪_ _{_ _|_ _⊆_ _}_
has exactly 2 _E(G)_ = 3 _F_ (G) edges. According to this identity we may
_|_ _|_ _|_ _|_
replace ℓ with 2m/3 in Euler’s formula, and obtain m = 3n − 6. 
Euler’s formula can be useful for showing that certain graphs cannot
occur as plane graphs. The graph K [5], for example, has 10 > 3 5 6
_·_ _−_
edges, more than allowed by Corollary 4.2.8. Similarly, K3,3 cannot be a
plane graph. For since K3,3 is 2-connected but contains no triangle, every
face of a plane K3,3 would be bounded by a cycle of length ⩾ 4 (Proposition 4.2.5). As in the proof of Corollary 4.2.8 this implies 2m ⩾ 4ℓ,
which yields m ⩽ 2n − 4 when substituted in Euler’s formula. But K3,3
has 9 > 2 6 4 edges.
_·_ _−_
Clearly, along with K [5] and K3,3 themselves, their subdivisions cannot occur as plane graphs either:

[ 4.4.5 ]
**Corollary 4.2.9. A plane graph contains neither K** [5] _nor K3,3 as a_ [ 4.4.6 ]
_topological minor._ 
Surprisingly, it turns out that this simple property of plane graphs identifies them among all other graphs: as Section 4.4 will show, an arbitrary
graph can be drawn in the plane if and only if it has no (topological) K [5]

or K3,3 minor.

As we have seen, every face boundary in a 2-connected plane graph
is a cycle. In a 3-connected graph, these cycles can be identified combinatorially:

[ 4.3.2 ]
**Proposition 4.2.10. The face boundaries in a 3-connected plane graph**

[ 4.5.2 ]
_are precisely its non-separating induced cycles._

(3.3.5)
_Proof . Let G be a 3-connected plane graph, and let C_ _G. If C is a_ (4.1.1)
_⊆_
non-separating induced cycle, then by the Jordan curve theorem its two (4.1.2)
faces cannot both contain points of G ∖ _C. Therefore it bounds a face_
of G.
Conversely, suppose that C bounds a face f . By Proposition 4.2.5, _C, f_


-----

are linked by a C-path in G, because G is 3-connected. This path and
_e both run through the other face of C (not f_ ) but do not intersect,
a contradiction to Lemma 4.1.2 (ii).
It remains to show that C does not separate any two vertices x, y _[∈]_
_G_ _C. By Menger’s theorem (3.3.5), x and y are linked in G by three_
_−_
independent paths. Clearly, f lies inside a face of their union, and by
Lemma 4.1.2 (i) this face is bounded by only two of the paths. The third
therefore avoids f and its boundary C.       
###### 4.3 Drawings

_planar_
An embedding in the plane, or planar embedding, of an (abstract) graph
_embedding_
_G is an isomorphism between G and a plane graph G[˜]. The latter will_
_drawing_ be called a drawing of G. We shall not always distinguish notationally
between the vertices and edges of G and of G[˜].
In this section we investigate how two planar embeddings of a graph
can differ. For this to make sense, we first have to agree when two embeddings are to be considered the same: for example, if we compose one
embedding with a simple rotation of the plane, the resulting embedding
will hardly count as a genuinely different way of drawing that graph.
To prepare the ground, let us first consider three possible notions
of equivalence for plane graphs (refining abstract isomorphism), and see
_G; V, E, F_ how they are related. Let G = (V, E) and G[′] = (V _[′], E[′]) be two plane_
_G[′]; V_ _, E[′]_ _, F[′]_ _[′]_ graphs, with face sets F (G) =: F and F (G[′]) =: F _[′]. Assume that G and_
_G[′]_ are isomorphic as abstract graphs, and let σ: V → _V_ _[′]_ be an isomor_σ_ phism. Setting xy _σ(x)σ(y), we may extend σ in a natural way to a_
_�→_
bijection V ∪ _E →_ _V_ _[′]_ _∪_ _E[′]_ which maps V to V _[′]_ and E to E[′], and which
preserves incidence (and non-incidence) between vertices and edges.
Our first notion of equivalence between plane graphs is perhaps
the most natural one. Intuitively, we would like to call our isomorphism σ ‘topological’ if it is induced by a homeomorphism from the
plane R[2] to itself. To avoid having to grant the outer faces of G and
_G[′]_ a special status, however, we take a detour via the homeomorphism
_π_ _π: S[2]_ ∖ _{ (0, 0, 1) } →_ R[2] chosen in Section 4.1: we call σ a topological
_isomorphism between the plane graphs G and G[′]_ if there exists a homeo_topological_
morphism ϕ: S[2] _S[2]_ such that ψ := π _ϕ_ _π[−][1]_ induces σ on V _E._
_isomorphism_ _→_ _◦_ _◦_ _∪_
(More formally: we ask that ψ agree with σ on V, and that it map every
plane edge e _[∈]_ _G onto the plane edge σ(e)_ _[∈]_ _G[′]. Unless ϕ fixes the point_
(0, 0, 1), the map ψ will be undefined at π(ϕ[−][1](0, 0, 1)).)
It can be shown that, up to topological isomorphism, inner and
outer faces are indeed no longer different: if we choose as ϕ a rotation
of S[2] mapping the π[−][1]-image of a point of some inner face of G to the


-----

_Fig. 4.3.1. Two drawings of a graph that are not topologically_
isomorphic—why not?

face of ψ(G). (To ensure that the edges of ψ(G) are again piecewise
linear, however, one may have to adjust ϕ a little.)
If σ is a topological isomorphism as above, then—except possibly
for a pair of missing points where ψ or ψ[−][1] is undefined—ψ maps the
faces of G onto those of G[′] (proof?). In this way, σ extends naturally
to a bijection σ: V ∪ _E ∪_ _F →_ _V_ _[′]_ _∪_ _E[′]_ _∪_ _F_ _[′]_ which preserves incidence of
vertices, edges and faces.
Let us single out this last property of a topological isomorphism
as the defining property for our second notion of equivalence for plane
graphs: let us call our given isomorphism σ between the abstract graphs
_G and G[′]_ a combinatorial isomorphism of the plane graphs G and G[′][ combinatorial]
_isomorphism_
if it can be extended to a bijection σ: V ∪ _E ∪_ _F →_ _V_ _[′]_ _∪_ _E[′]_ _∪_ _F_ _[′]_ that
preserves incidence not only of vertices with edges but also of vertices
and edges with faces. (Formally: we require that a vertex or edge x _[∈]_ _G_
shall lie on the boundary of a face f _[∈]_ _F if and only if σ(x) lies on the_
boundary of the face σ(f ).)

_G_ _G[′]_

_Fig. 4.3.2. Two drawings of a graph that are combinatorially_
isomorphic but not topologically—why not?

If σ is a combinatorial isomorphism of the plane graphs G and G[′], it
maps the face boundaries of G to those of G[′]. Let us raise this property
to our third definition of equivalence for plane graphs: we call our isomor- _graph-_
phism σ of the abstract graphs G and G[′] a graph-theoretical isomorphism _theoretical_
of the plane graphs G and G[′] if _isomorphism_

� _σ(G [ f ]) : f ∈_ _F_ � = � _G[′]_ [ f _[′]_ ] : f _[′ ]∈_ _F_ _[′][ �]_ _._

Thus, we no longer keep track of which face is bounded by a given


-----

some face or not, and we require that σ map the subgraphs that do
onto each other. At first glance, this third notion of equivalence may
appear a little less natural than the previous two. However, it has the
practical advantage of being formally weaker and hence easier to verify,
and moreover, it will turn out to be equivalent to the other two notions
in most cases.
As we have seen, every topological isomorphism between two plane
graphs is also combinatorial, and every combinatorial isomorphism is also
graph-theoretical. The following theorem shows that, for most graphs,
the converse is true as well:


**Theorem 4.3.1.**
(i) Every graph-theoretical isomorphism between two plane graphs is
_combinatorial. Its extension to a face bijection is unique if and_
_only if the graph is not a cycle._
(ii) Every combinatorial isomorphism between two 2-connected plane
_graphs is topological._

(4.1.1)
(4.1.4)
(4.2.4) _Proof . Let G = (V, E) and G[′]_ = (V _[′], E[′]) be two plane graphs, put_
(4.2.5) _F_ (G) =: F and F (G[′]) =: F _[′], and let σ: V ∪_ _E →_ _V_ _[′]_ _∪_ _E[′]_ be an isomorphism between the underlying abstract graphs.
(i) If G is a cycle, the assertion follows from the Jordan curve theorem. We now assume that G is not a cycle. Let and be the sets of
_H_ _H[′]_
all face boundaries in G and G[′], respectively. If σ is a graph-theoretical
isomorphism, then the map H _σ(H) is a bijection between_ and .
_�→_ _H_ _H[′]_
By Lemma 4.2.4, the map f _G [ f ] is a bijection between F and_,
_�→_ _H_
and likewise for F _[′]_ and H[′]. The composition of these three bijections is
a bijection between F and F _[′], which we choose as σ: F →_ _F_ _[′]. By con-_
struction, this extension of σ to V _E_ _F preserves incidences (and is_
_∪_ _∪_
unique with this property), so σ is indeed a combinatorial isomorphism.
_σ_ (ii) Let us assume that G is 2-connected, and that σ is a combinatorial isomorphism. We have to construct a homeomorphism ϕ: S[2] _S[2]_
_→_

which, for every vertex or plane edge x _[∈]_ _G, maps π[−][1](x) to π[−][1](σ(x))._
_σ˜_ Since σ is a combinatorial isomorphism, ˜σ : π[−][1] _σ_ _π is an incidence_
_◦_ _◦_
preserving bijection from the vertices, edges and faces[4] of G[˜] := π[−][1](G)
_G,˜_ ˜G[′] to the vertices, edges and faces of G[˜][′] := π[−][1](G[′]).
We construct ϕ in three steps. Let us first define ϕ on the vertex
set of G[˜], setting ϕ(x) := ˜σ(x) for all x _[∈]_ _V ( G[˜])._ This is trivially a
homeomorphism between V ( G[˜]) and V ( G[˜][′]).
As the second step, we now extend ϕ to a homeomorphism between
_G˜ and ˜G[′]_ that induces ˜σ on V ( ˜G) ∪ _E( ˜G). We may do this edge by_

4 By the ‘vertices, edges and faces’ of ˜G and ˜G′ we mean the images under π−1

of the vertices, edges and faces of G and G[′] (plus (0, 0, 1) in the case of the outer
face). Their sets will be denoted by V (G[˜] ), E(G[˜] ), F (G[˜] ) and V (G[˜] _[′]), E(G[˜]_ _[′]), F_ (G[˜] _[′]),_


-----

_S[2]_ _⊇_


_σ˜_

_G˜_ _G˜[′]_ _S[2]_


_π_ _π_

� �


R[2] _⊇_


_G_ _G[′]_ R[2]

_σ_


_Fig. 4.3.3. Defining ˜σ via σ_

edge, as follows. Every edge xy of G[˜] is homeomorphic to the edge
_σ˜(xy) = ϕ(x)ϕ(y) of G[˜][′], by a homeomorphism mapping x to ϕ(x) and_
_y to ϕ(y). Then the union of all these homeomorphisms, one for every_
edge of G[˜], is indeed a homeomorphism between G[˜] and G[˜][′]—our desired
extension of ϕ to G[˜]: all we have to check is continuity at the vertices
(where the edge homeomorphisms overlap), and this follows at once from
our assumption that the two graphs and their individual edges all carry
the subspace topology in R[3].
In the third step we now extend our homeomorphism ϕ: G[˜] → _G[˜][′]_ to
all of S[2]. This can be done analogously to the second step, face by face.
By Proposition 4.2.5, all face boundaries in G[˜] and G[˜][′] are cycles. Now if
_f is a face of G[˜] and C its boundary, then ˜σ(C) :=_ [�]{ ˜σ(e) | e _[∈]_ _E(C) }_
bounds the face ˜σ(f ) of G[˜][′]. By Theorem 4.1.4, we may therefore extend
the homeomorphism ϕ: C _σ˜(C) defined so far to a homeomorphism_
_→_
from C _f to ˜σ(C)_ _σ˜(f_ ). We finally take the union of all these home_∪_ _∪_
omorphisms, one for every face f of G[˜], as our desired homeomorphism
_ϕ: S[2]_ _→_ _S[2]; as before, continuity is easily checked._ 

So far, we have considered ways of comparing plane graphs. We
now come to our actual goal, the definition of equivalence for planar
embeddings. Let us call two planar embeddings σ1, σ2 of a graph G
_equivalent_
_topologically (respectively, combinatorially) equivalent if σ2 ◦_ _σ1[−][1]_ is a to- _embeddings_
pological (respectively, combinatorial) isomorphism between σ1(G) and
_σ2(G)._ If G is 2-connected, the two definitions coincide by Theorem
4.3.1, and we simply speak of equivalent embeddings. Clearly, this is
indeed an equivalence relation on the set of planar embeddings of any
given graph.
Note that two drawings of G resulting from inequivalent embeddings
may well be topologically isomorphic (exercise): for the equivalence of
two embeddings we ask not only that some (topological or combinatorial) isomorphism exist between the their images, but that the canonical
isomorphism σ2 ◦ _σ1[−][1]_ be a topological or combinatorial one.
Even in this strong sense, 3-connected graphs have only one embedding up to equivalence:

**Theorem 4.3.2. (Whitney 1932)**


-----

(4.2.10) _Proof . Let G be a 3-connected graph with planar embeddings σ1: G_ _→_ _G1_
and σ2: G → _G2. By Theorem 4.3.1 it suffices to show that σ2 ◦_ _σ1[−][1]_ is
a graph-theoretical isomorphism, i.e. that σ1(C) bounds a face of G1 if
and only if σ2(C) bounds a face of G2, for every subgraph C ⊆ _G. This_
follows at once from Proposition 4.2.10.       
###### 4.4 Planar graphs: Kuratowski’s theorem

_planar_ A graph is called planar if it can be embedded in the plane: if it is
isomorphic to a plane graph. A planar graph is maximal, or maximally
_planar_, if it is planar but cannot be extended to a larger planar graph
by adding an edge (but no vertex).
Drawings of maximal planar graphs are clearly maximally plane.
The converse, however, is not obvious: when we start to draw a planar
graph, could it happen that we get stuck half-way with a proper subgraph
that is already maximally plane? Our first proposition says that this
can never happen, that is, a plane graph is never maximally plane just
because it is badly drawn:

**Proposition 4.4.1.**

(i) Every maximal plane graph is maximally planar.

(ii) A planar graph with n ⩾ 3 vertices is maximally planar if and
_only if it has 3n_ 6 edges.
_−_

(4.2.6)
(4.2.8) _Proof . Apply Proposition 4.2.6 and Corollary 4.2.8._ 
Which graphs are planar? As we saw in Corollary 4.2.9, no planar
graph contains K [5] or K3,3 as a topological minor. Our aim in this section
is to prove the surprising converse, a classic theorem of Kuratowski: any
graph without a topological K [5] or K3,3 minor is planar.
Before we prove Kuratowski’s theorem, let us note that it suffices
to consider ordinary minors rather than topological ones:

**Proposition 4.4.2. A graph contains K** [5] _or K3,3 as a minor if and only_
_if it contains K_ [5] _or K3,3 as a topological minor._

(1.7.2) _Proof ._ By Proposition 1.7.2 it suffices to show that every graph G
with a K [5] minor contains either K [5] as a topological minor or K3,3 as
a minor. So suppose that G ≽ _K_ [5], and let K ⊆ _G be minimal such_
that K = MK [5]. Then every branch set of K induces a tree in K, and
between any two branch sets K has exactly one edge. If we take the
tree induced by a branch set Vx and add to it the four edges joining it


-----

_Fig. 4.4.1. Every MK_ [5] contains a TK [5] or MK3,3

of K, Tx has exactly 4 leaves, the 4 neighbours of Vx in other branch
sets (Fig. 4.4.1).
If each of the five trees Tx is a TK1,4 then K is a TK [5], and we are
done. If one of the Tx is not a TK1,4 then it has exactly two vertices
of degree 3. Contracting Vx onto these two vertices, and every other
branch set to a single vertex, we obtain a graph on 6 vertices containing
a K3,3. Thus, G ≽ _K3,3 as desired._ 
We first prove Kuratowski’s theorem for 3-connected graphs. This
is the heart of the proof: the general case will then follow easily.

**Lemma 4.4.3. Every 3-connected graph G without a K** [5] _or K3,3 minor_
_is planar._

(3.2.1)
_Proof . We apply induction on_ _G_ . For _G_ = 4 we have G = K [4], and
_|_ _|_ _|_ _|_ (4.2.5)
the assertion holds. Now let _G_ _> 4, and assume the assertion is true_
_|_ _|_
for smaller graphs. By Lemma 3.2.1, G has an edge xy such that G/xy _xy_
is again 3-connected. Since the minor relation is transitive, G/xy has no
_K_ [5] or K3,3 minor either. Thus, by the induction hypothesis, G/xy has
a drawing G[˜] in the plane. Let f be the face of G[˜] − _vxy containing the_ _G˜_
point vxy, and let C be the boundary of f . Let X := NG(x) ∖ _{ y } and_ _f, C_
_Y := NG(y) ∖_ _{ x }; then X ∪_ _Y ⊆_ _V (C), because vxy ∈_ _f_ . Clearly, _X, Y_

_G˜[′]_ := ˜G −{ vxyv | v ∈ _Y ∖_ _X }_ _G˜_ _[′]_

may be viewed as a drawing of G _y, in which the vertex x is represented_
_−_
by the point vxy (Fig. 4.4.2). Our aim is to add y to this drawing to
obtain a drawing of G.
Since G[˜] is 3-connected, G[˜] − _vxy is 2-connected, so C is a cycle_
(Proposition 4.2.5). Let x1, . . ., xk be an enumeration along this cycle of _x1, . . ., xk_
the vertices in X, and let Pi = xi . . . xi+1 be the X-paths on C between _Pi_
them (i = 1, . . ., k; with xk+1 := x1). For each i, the set C ∖ _Pi is_


-----

_x2_


_x1_

_x5_

_f1_ _P4_

_x (= vxy)_

_f_

_x4_
_x3_


_Fig. 4.4.2._ _G[˜]_ _[′]_ as a drawing of G _−_ _y: the vertex x is represented_
by the point vxy

_fi_ denote the other face of Ci by fi. Since fi contains points of f (close
to x) but no points of C, we have fi ⊆ _f_ . Moreover, the plane edges xxj
with j /[∈] _{ i, i + 1 } meet Ci only in x and end outside fi in C ∖_ _Pi, so fi_
meets none of those edges. Hence fi R[2] ∖ _G[˜][′], that is, fi is contained_
_⊆_
in a face of G[˜][′]. (In fact, fi is a face of G[˜][′], but we do not need this.)
In order to turn G[˜][′] into a drawing of G, let us try to find an i
such that Y ⊆ _V (Pi); we may then embed y into fi and link it up to_
its neighbours by arcs inside fi. Suppose there is no such i: how then
can the vertices of Y be distributed around C? If y had a neighbour
in some P[˚]i, it would also have one in C − _Pi, so G would contain a_
_TK3,3 (with branch vertices x, y, xi, xi+1 and those two neighbours_
of y). Hence Y ⊆ _X. Now if |Y | = |Y ∩_ _X| ⩾_ 3, we have a TK[5] in G.
So |Y | ⩽ 2; in fact, |Y | = 2, because d(y) ⩾ _κ(G) ⩾_ 3. Since the two
vertices of Y lie on no common Pi, we can once more find a TK3,3 in G,
a contradiction.       
Compared with other proofs of Kuratowski’s theorem, the above
proof has the attractive feature that it can easily be adapted to produce
a drawing in which every inner face is convex (exercise); in particular,
every edge can be drawn straight. Note that 3-connectedness is essential
here: a 2-connected planar graph need not have a drawing with all inner
faces convex (example?), although it always has a straight-line drawing
(Exercise 12).
It is not difficult, in principle, to reduce the general Kuratowski
theorem to the 3-connected case by manipulating and combining partial
drawings assumed to exist by induction. For example, if κ(G) = 2 and
_G = G1 ∪_ _G2 with V (G1 ∩_ _G2) = { x, y }, and if G has no TK_ [5] or TK3,3
subgraph, then neither G1 + xy nor G2 + xy has such a subgraph, and
we may try to combine drawings of these graphs to one of G + xy. (If
_xy is already an edge of G, the same can be done with G1 and G2.)_
For κ(G) ⩽ 1, things become even simpler. However, the geometric
operations involved require some cumbersome shifting and scaling, even


-----

The following more combinatorial route is just as easy, and may be
a welcome alternative.

**Lemma 4.4.4. Let** _be a set of 3-connected graphs. Let G be a graph_ [ 8.3.1 ]
_X_
_with κ(G) ⩽_ 2, and let G1, G2 be proper induced subgraphs of G such
_that G = G1 ∪_ _G2 and |G1 ∩_ _G2| = κ(G). If G is edge-maximal without_
_a topological minor in X_ _, then so are G1 and G2, and G1 ∩_ _G2 = K_ [2].

_Proof . Note first that every vertex v ∈_ _S := V (G1 ∩_ _G2) has a neigh-_ _S_
bour in every component of Gi − _S, i = 1, 2: otherwise S ∖_ _{ v } would_
separate G, contradicting _S_ = κ(G). By the maximality of G, every
_|_ _|_
edge e added to G lies in a TX ⊆ _G + e with X_ _∈_ _X_ . For all the _X_
choices of e considered below, the 3-connectedness of X will imply that
the branch vertices of this TX all lie in the same Gi, say in G1. (The
position of e will always be symmetrical with respect to G1 and G2, so
this assumption entails no loss of generality.) Then the TX meets G2 at
most in a path P corresponding to an edge of X. _P_
If S =, we obtain an immediate contradiction by choosing e with
_∅_
one end in G1 and the other in G2. If S = { v } is a singleton, let e
join a neighbour v1 of v in G1 _S to a neighbour v2 of v in G2_ _S_
_−_ _−_
(Fig. 4.4.3). Then P contains both v and the edge v1v2; replacing vPv1
with the edge vv1, we obtain a TX in G1 ⊆ _G, a contradiction._

_e_ _P_

_v1_ _v2_

_TX_

_v_

_G1_ _G2_

_Fig. 4.4.3. If G + e contains a TX, then so does G1 or G2_

So _S_ = 2, say S = _x, y_ . If xy /[∈] _G, we let e := xy, and in the_ _x, y_
_|_ _|_ _{_ _}_
arising TX replace e by an x–y path through G2; this gives a TX in G,
a contradiction. Hence xy ∈ _G, and G [ S ] = K_ [2] as claimed.
It remains to show that G1 and G2 are edge-maximal without a
topological minor in X . So let e[′] be an additional edge for G1, say.
Replacing xPy with the edge xy if necessary, we obtain a TX either
in G1 + e[′] (which shows the edge-maximality of G1, as desired) or in G2
(which contradicts G2 ⊆ _G)._ 
**Lemma 4.4.5. If |G| ⩾** 4 and G is edge-maximal with TK [5], TK3,3 ̸⊆ _G,_


-----

(4.2.9) _Proof ._ We apply induction on _G_ . For _G_ = 4, we have G = K [4]
_|_ _|_ _|_ _|_
and the assertion holds. Now let _G_ _> 4, and let G be edge-maximal_
_|_ _|_
_G1, G2_ without a TK [5] or TK3,3. Suppose κ(G) ⩽ 2, and choose G1 and G2 as
in Lemma 4.4.4. For X := { K [5], K3,3 }, the lemma says that G1 ∩ _G2 is_
_x, y_ a K [2], with vertices x, y say. By Lemmas 4.4.4, 4.4.3 and the induction
hypothesis, G1 and G2 are planar. For each i = 1, 2 separately, choose a
_fi_ drawing of Gi, a face fi with the edge xy on its boundary, and a vertex
_zi_ _zi_ = x, y on the boundary of fi. Let K be a TK [5] or TK3,3 in the
_̸_
_K_ abstract graph G + z1z2 (Fig. 4.4.4).

_z1_ _x_ _z2_

_K_

_y_

_G1_ _G2_

_Fig. 4.4.4. A TK_ [5] or TK3,3 in G + z1z2

If all the branch vertices of K lie in the same Gi, then either Gi + _xzi_
or Gi + yzi (or Gi itself, if zi is already adjacent to x or y, respectively)
contains a TK [5] or TK3,3; this contradicts Corollary 4.2.9, since these
graphs are planar by the choice of zi. Since G + _z1z2 does not contain four_
independent paths between (G1 − _G2) and (G2 −_ _G1), these subgraphs_
cannot both contain a branch vertex of a TK [5], and cannot both contain
two branch vertices of a TK3,3. Hence K is a TK3,3 with only one branch
vertex v in, say, G2 − _G1. But then also the graph G1 +_ _v +_ _{ vx, vy, vz1 },_
which is planar by the choice of z1, contains a TK3,3. This contradicts
Corollary 4.2.9.       
**Theorem 4.4.6. (Kuratowski 1930; Wagner 1937)**

[ 4.5.1 ]
_The following assertions are equivalent for graphs G:_

[ 12.4.3 ]
(i) G is planar;

(ii) G contains neither K [5] _nor K3,3 as a minor;_

(iii) G contains neither K [5] _nor K3,3 as a topological minor._

(4.2.9) _Proof ._ Combine Corollary 4.2.9 and Proposition 4.4.2 with Lemmas
4.4.3 and 4.4.5.       
**Corollary 4.4.7. Every maximal planar graph with at least four ver-**
_tices is 3-connected._


-----

###### 4.5 Algebraic planarity criteria

In this section we show that planarity can be characterized in purely
algebraic terms, by a certain abstract property of its cycle space. Theorems relating such seemingly distant graph properties are rare, and their
significance extends beyond their immediate applicability. In a sense,
they indicate that both ways of viewing a graph—in our case, the topological and the algebraic way—are not just formal curiosities: if both are
natural enough that, quite unexpectedly, each can be expressed in terms
of the other, the indications are that they have the power to reveal some
genuine insights into the structure of graphs and are worth pursuing.
Let G = (V, E) be a graph. We call a subset of its edge space
_F_
(G) simple if every edge of G lies in at most two sets of . For example, _simple_
_E_ _F_
the cut space (G) has a simple basis: according to Proposition 1.9.3 it
_C[∗]_
is generated by the cuts E(v) formed by all the edges at a given vertex v,
and an edge xy ∈ _G lies in E(v) only for v = x and for v = y._

**Theorem 4.5.1. (MacLane 1937)**
_A graph is planar if and only if its cycle space has a simple basis._ [ 4.6.3 ]

_Proof ._ The assertion being trivial for graphs of order at most 2, we
(1.9.2)

consider a graph G of order at least 3. If κ(G) ⩽ 1, then G is the union (1.9.6)
of two proper induced subgraphs G1, G2 with |G1 ∩ _G2| ⩽_ 1. Then C(G) (4.1.1)
is the direct sum of C(G1) and C(G2), and hence has a simple basis if (4.2.1)

(4.2.5)

and only if both C(G1) and C(G2) do (proof?). Moreover, G is planar if (4.4.6)
and only if both G1 and G2 are: this follows at once from Kuratowski’s
theorem, but also from easy geometrical considerations. The assertion
for G thus follows inductively from those for G1 and G2. For the rest of
the proof, we now assume that G is 2-connected.
We first assume that G is planar and choose a drawing. By Lemma
4.2.5, the face boundaries of G are cycles, so they are elements of (G).
_C_
We shall show that the face boundaries generate all the cycles in G; then
(G) has a simple basis by Lemma 4.2.1. Let C _G be any cycle, and_
_C_ _⊆_
let f be its inner face. By Lemma 4.2.1, every edge e with ˚e _f lies on_
_⊆_
exactly two face boundaries G [ f _[′]_ ] with f _[′]_ _⊆_ _f_, and every edge of C lies
on exactly one such face boundary. Hence the sum in (G) of all those
_C_
face boundaries is exactly C.
Conversely, let { C1, . . ., Ck } be a simple basis of C(G). Then, for
every edge e ∈ _G, also C(G −_ _e) has a simple basis. Indeed, if e lies_
in just one of the sets Ci, say in C1, then { C2, . . ., Ck } is a simple
basis of C(G − _e); if e lies in two of the Ci, say in C1 and C2, then_
_{ C1 + C2, C3, . . ., Ck } is such a basis._ (Note that the two bases are
indeed subsets of (G _e) by Proposition 1.9.2.) Thus every subgraph_
_C_ _−_
of G has a cycle space with a simple basis. For our proof that G is planar,


-----

those of their subdivisions) do not have a simple basis: then G cannot
contain a TK [5] or TK3,3, and so is planar by Kuratowski’s theorem.
Let us consider K [5] first. By Theorem 1.9.6, dim (K [5]) = 6; let
_C_
_B = { C1, . . ., C6 } be a simple basis, and put C0 := C1 + . . . + C6. As_
_B is linearly independent, none of the sets C0, . . ., C6 is empty, and so_
each of them contains at least three edges (cf. Proposition 1.9.2). The
simplicity of therefore implies
_B_

18 = 6 · 3 ⩽ _|C1| + . . . + |C6|_

⩽ 2 ∥K [5]∥−|C0|

⩽ 2 · 10 − 3 = 17,

a contradiction; for the middle inequality note that every edge in C0 lies
in just one of the sets C1, . . ., C6.
For K3,3, Theorem 1.9.6 gives dim C(K3,3) = 4; let B = { C1, . . ., C4 }
be a simple basis, and put C0 := C1 + . . . + C4. Since K3,3 has girth 4,
each Ci contains at least four edges, so

16 = 4 · 4 ⩽ _|C1| + . . . + |C4|_

⩽ 2 ∥K3,3∥−|C0|

⩽ 2 · 9 − 4 = 14,

a contradiction.       
It is one of the hidden beauties of planarity theory that two such
abstract and seemingly unintuitive results about generating sets in cycle spaces as MacLane’s theorem and Tutte’s theorem 3.2.3 conspire to
produce a very tangible planarity criterion for 3-connected graphs:

**Theorem 4.5.2. (Tutte 1963)**
_A 3-connected graph is planar if and only if every edge lies on at most_
_(equivalently: exactly) two non-separating induced cycles._

(3.2.3)
(4.2.1)

_Proof . The forward implication follows from Propositions 4.2.10 and_

(4.2.5)
(4.2.10) 4.2.1 (and Proposition 4.2.5 for the ‘exactly two’ version); the backward
implication follows from Theorems 3.2.3 and 4.5.1.       

-----

###### 4.6 Plane duality

In this section we shall use MacLane’s theorem to uncover another connection between planarity and algebraic structure: a connection between
the duality of plane graphs, defined below, and the duality of the cycle
and cut space hinted at in Chapters 1.9 and 3.5.
_plane_
A plane multigraph is a pair G = (V, E) of finite sets (of vertices
_multigraph_
and edges, respectively) satisfying the following conditions:

(i) V ⊆ R[2];
(ii) every edge is either an arc between two vertices or a polygon
containing exactly one vertex (its endpoint);
(iii) apart from its own endpoint(s), an edge contains no vertex and
no point of any other edge.

We shall use terms defined for plane graphs freely for plane multigraphs.
Note that, as in abstract multigraphs, both loops and double edges count
as cycles.
Let us consider the plane multigraph G shown in Figure 4.6.1. Let
us place a new vertex inside each face of G and link these new vertices
up to form another plane multigraph G[∗], as follows: for every edge e of
_G we link the two new vertices in the faces incident with e by an edge e[∗]_

crossing e; if e is incident with only one face, we attach a loop e[∗] to the
new vertex in that face, again crossing the edge e. The plane multigraph
_G[∗]_ formed in this way is then dual to G in the following sense: if we
apply the same procedure as above to G[∗], we obtain a plane multigraph
very similar to G; in fact, G itself may be reobtained from G[∗] in this way.

_e_ **_e[∗]_**
_G_

###### G[∗]

_Fig. 4.6.1. A plane graph and its dual_

To make this idea more precise, let G = (V, E) and (V _[∗], E[∗]) be any_
two plane multigraphs, and put F (G) =: F and F ((V _[∗], E[∗])) =: F_ _[∗]. We_
_plane_
call (V _[∗], E[∗]) a plane dual of G, and write (V_ _[∗], E[∗]) =: G[∗], if there are_ _dual G[∗]_
bijections
_F →_ _V_ _[∗]_ _E →_ _E[∗]_ _V →_ _F_ _[∗]_

_f �→_ _v[∗](f_ ) _e �→_ _e[∗]_ _v �→_ _f_ _[∗](v)_

satisfying the following conditions:


-----

(ii) |e[∗] _∩_ _G| = |˚e[∗]_ _∩˚e| = |e ∩_ _G[∗]| = 1 for all e_ _[∈]_ _E;_
(iii) v ∈ _f_ _[∗](v) for all v ∈_ _V ._

The existence of such bijections implies that both G and G[∗] are connected (exercise). Conversely, every connected plane multigraph G has
a plane dual G[∗]: if we pick from each face f of G a point v[∗](f ) as a
vertex for G[∗], we can always link these vertices up by independent arcs
as required by condition (ii), and there is always a bijection V → _F_ _[∗]_

satisfying (iii) (exercise).
If G[∗]1 [and][ G]2[∗] [are two plane duals of][ G][, then clearly][ G]1[∗] _[≃]_ _[G]2[∗][; in fact,]_
one can show that the natural bijection v1[∗][(][f] [)][ �→] _[v]2[∗][(][f]_ [) is a topological]
isomorphism between G[∗]1 [and][ G]2[∗][. In this sense, we may speak of][ the]
plane dual G[∗] of G.
Finally, G is in turn a plane dual of G[∗]. Indeed, this is witnessed
by the inverse maps of the bijections from the definition of G[∗]: setting
_v[∗](f_ _[∗](v)) := v and f_ _[∗](v[∗](f_ )) := f for f _[∗](v)_ _[∈]_ _F_ _[∗]_ and v[∗](f ) _[∈]_ _V_ _[∗], we_
see that conditions (i) and (iii) for G[∗] transform into (iii) and (i) for G,
while condition (ii) is symmetrical in G and G[∗]. Thus, the term ‘dual’
is also formally justified.

Plane duality is fascinating not least because it establishes a connection between two natural but very different kinds of edge sets in a
multigraph, between cycles and cuts:

[ 6.5.2 ] **Proposition 4.6.1. For any connected plane multigraph G, an edge set**
_E ⊆_ _E(G) is the edge set of a cycle in G if and only if E[∗]_ := { e[∗] _| e_ _[∈]_ _E }_
_is a minimal cut in G[∗]._

(4.1.1)
_Proof . By conditions (i) and (ii) in the definition of G[∗], two vertices_
(4.2.3)
_v[∗](f1) and v[∗](f2) of G[∗]_ lie in the same component of G[∗] _−_ _E[∗]_ if and
only if f1 and f2 lie in the same region of R[2] ∖ [�] _E: every v[∗](f1)–v[∗](f2)_
path in G[∗]− _E[∗]_ is an arc between f1 and f2 in R[2] ∖ [�] _E, and conversely_
every such arc P (with P ∩ _V (G) = ∅) defines a walk in G[∗]−_ _E[∗]_ between
_v[∗](f1) and v[∗](f2)._
Now if C _G is a cycle and E = E(C) then, by the Jordan curve_
_⊆_
theorem and the above correspondence, G[∗]− _E[∗]_ has exactly two components, so E[∗] is a minimal cut in G[∗].
Conversely, if E ⊆ _E(G) is such that E[∗]_ is a cut in G[∗], then, by
Proposition 4.2.3 and the above correspondence, E contains the edges
of a cycle C ⊆ _G. If E[∗]_ is minimal as a cut, then E cannot contain any
further edges (by the implication shown before), so E = E(C).      
Proposition 4.6.1 suggests the following generalization of plane duality to a notion of duality for abstract multigraphs. Let us call a multi_abstract_
graph G[∗] an abstract dual of a multigraph G if E(G[∗]) = E(G) and the
_dual_
minimal cuts in G[∗] are precisely the edge sets of cycles in G. Note that


-----

**Proposition 4.6.2. If G[∗]** _is an abstract dual of G, then the cut space_
_of G[∗]_ _is the cycle space of G, i.e._

(G[∗]) = (G) .
_C[∗]_ _C_

_Proof ._ By Lemma 1.9.4,[5] (G[∗]) is the subspace of (G[∗]) = (G) (1.9.4)
_C[∗]_ _E_ _E_
generated by the minimal cuts in G[∗]. By assumption, these are precisely
the edge sets of the cycles in G, and these generate C(G) in E(G). 
We finally come to one of the highlights of classical planarity theory: the planar graphs are characterized by the fact that they have an
abstract dual. Although less obviously intuitive, this duality is just as
fundamental a property as planarity itself; indeed the following theorem
may well be seen as a topological characterization of the graphs that
have a dual:

**Theorem 4.6.3. (Whitney 1933)**
_A graph is planar if and only if it has an abstract dual._

(1.9.3)
_Proof . Let G be a graph. If G is plane, then every component C of G has_
(4.5.1)
a plane dual C _[∗]. Let us consider these C_ _[∗]_ as abstract multigraphs, pick
a vertex in each of them, and identify these vertices. In the connected
multigraph G[∗] obtained, the set of minimal cuts is the union of the sets
of minimal cuts in the multigraphs C _[∗]. By Proposition 4.6.1, these cuts_
are precisely the edge sets of the cycles in G, so G[∗] is an abstract dual
of G.
Conversely, suppose that G has an abstract dual G[∗]. By Theorem
4.5.1 and Proposition 4.6.2 it suffices to show that C[∗](G[∗]) has a simple
basis, which it has by Proposition 1.9.3. 
###### Exercises

1. Show that every graph can be embedded in R[3] with all edges straight.

2.[−] Show directly by Lemma 4.1.2 that K3,3 is not planar.

3.[−] Find an Euler formula for disconnected graphs.

4. Show that every connected planar graph with n vertices, m edges and
finite girth g satisfies m ⩽ _g−g_ 2 [(][n][ −] [2).]

5. Show that every planar graph is a union of three forests.

5 Although the lemma was stated for graphs only, its proof remains the same for


-----

6. Let G1, G2, . . . be an infinite sequence of pairwise non-isomorphic
graphs. Show that if lim sup ε(Gi) > 3 then the graphs Gi have unbounded genus—that is to say, there is no (closed) surface S in which
all the Gi can be embedded.

(Hint. You may use the fact that for every surface S there is a constant
_χ(S) ⩽_ 2 such that every graph embedded in S satisfies the generalized
Euler formula of n − _m + ℓ_ ⩾ _χ(S).)_

7. Find a direct proof for planar graphs of Tutte’s theorem on the cycle
space of 3-connected graphs (Theorem 3.2.3).

8.[−] Show that the two plane graphs in Fig. 4.3.1 are not combinatorially
(and hence not topologically) isomorphic.

9. Show that the two graphs in Fig. 4.3.2 are combinatorially but not
topologically isomorphic.

10.[−] Show that our definition of equivalence for planar embeddings does
indeed define an equivalence relation.

11. Find a 2-connected planar graph whose drawings are all topologically
isomorphic but whose planar embeddings are not all equivalent.

12.[+] Show that every plane graph is combinatorially isomorphic to a plane
graph whose edges are all straight.

(Hint. Given a plane triangulation, construct inductively a graphtheoretically isomorphic plane graph whose edges are straight. Which
additional property of the inner faces could help with the induction?)

Do not use Kuratowski’s theorem in the following two exercises.

13. Show that any minor of a planar graph is planar. Deduce that a graph
is planar if and only if it is the minor of a grid. (Grids are defined in
Chapter 12.3.)

14. (i) Show that the planar graphs can in principle be characterized as
in Kuratowski’s theorem, i.e., that there exists a set X of graphs such
that a graph G is planar if and only if G has no topological minor in X .

(ii) More generally, which graph properties can be characterized in this
way?

15.[−] Does every planar graph have a drawing with all inner faces convex?

16. Modify the proof of Lemma 4.4.3 so that all inner faces become convex.

17. Does every minimal non-planar graph G (i.e., every non-planar graph G
whose proper subgraphs are all planar) contain an edge e such that
_G −_ _e is maximally planar? Does the answer change if we define ‘mini-_
mal’ with respect to minors rather than subgraphs?

18. Show that adding a new edge to a maximal planar graph of order at


-----

19. Prove the general Kuratowski theorem from its 3-connected case by
manipulating plane graphs, i.e. avoiding Lemma 4.4.5.

(This is not intended as an exercise in elementary topology; for the
topological parts of the proof, a rough sketch will do.)

20. A graph is called outerplanar if it has a drawing in which every vertex
lies on the boundary of the outer face. Show that a graph is outerplanar
if and only if it contains neither K [4] nor K2,3 as a minor.

21. Let G = G1 ∪ _G2, where |G1 ∩_ _G2| ⩽_ 1. Show that C(G) has a simple
basis if both C(G1) and C(G2) have one.

22.[+] Find a cycle space basis among the face boundaries of a 2-connected
plane graph.

23. Show that a 2-connected plane graph is bipartite if and only if every
face is bounded by an even cycle.

24.[−] Let G be a connected plane multigraph, and let G[∗] be its plane dual.
Prove the following two statements for every edge e _[∈]_ _G:_

(i) If e lies on the boundary of two distinct faces f1, f2 of G, then
_e[∗]_ = v[∗](f1) v[∗](f2).

(ii) If e lies on the boundary of exactly one face f of G, then e[∗] is
a loop at v[∗](f ).

25.[−] What does the plane dual of a plane tree look like?

26.[−] Show that the plane dual of a plane multigraph is connected.

27.[+] Show that a plane multigraph has a plane dual if and only if it is
connected.

28. Let G, G[∗] be mutually dual plane multigraphs, and let e _[∈]_ _E(G). Prove_
the following statements (with a suitable definition of G/e):

(i) If e is not a bridge, then G[∗]/e[∗] is a plane dual of G − _e._

(ii) If e is not a loop, then G[∗] _−_ _e[∗]_ is a plane dual of G/e.

29. Show that any two plane duals of a plane multigraph are combinatorially isomorphic.

30. Let G, G[∗] be mutually dual plane graphs. Prove the following statements:

(i) If G is 2-connected, then G[∗] is 2-connected.

(ii) If G is 3-connected, then G[∗] is 3-connected.

(iii) If G is 4-connected, then G[∗] need not be 4-connected.

31. Let G, G[∗] be mutually dual plane graphs. Let B1, . . ., Bn be the blocks
of G. Show that B1[∗][, . . ., B]n[∗] [are the blocks of][ G][∗][.]

32. Show that if G[∗] is an abstract dual of a multigraph G, then G is an


-----

33. Show that a connected graph G = (V, E) is planar if and only if there
exists a connected multigraph G[′] = (V _[′], E) (i.e. with the same edge_
set) such that the following holds for every set F ⊆ _E: the graph (V, F_ )
is a tree if and only if (V _[′], E ∖_ _F_ ) is a tree.

###### Notes

There is an excellent monograph on the embedding of graphs in surfaces,
including the plane: B. Mohar & C. Thomassen, Graphs on Surfaces, Johns
Hopkins University Press, to appear. Proofs of the results cited in Section 4.1,
as well as all references for this chapter, can be found there. A good account
of the Jordan curve theorem, both polygonal and general, is given also in
J. Stillwell, Classical topology and combinatorial group theory, Springer 1980.
The short proof of Corollary 4.2.8 uses a trick that deserves special mention: the so-called double counting of pairs, illustrated in the text by a bipartite graph whose edges can be counted alternatively by summing its degrees
on the left or on the right. Double counting is a technique widely used in
combinatorics, and there will be more examples later in the book.
The material of Section 4.3 is not normally standard for an introductory
graph theory course, and the rest of the chapter can be read independently of
this section. However, the results of Section 4.3 are by no means unimportant.
In a way, they have fallen victim to their own success: the shift from a topological to a combinatorial setting for planarity problems which they achieve
has made the topological techniques developed there dispensable for most of
planarity theory.
In its original version, Kuratowski’s theorem was stated only for topological minors; the version for general minors was added by Wagner in 1937.
Our proof of the 3-connected case (Lemma 4.4.3) can easily be strengthened
to make all the inner faces convex (exercise); see C. Thomassen, Planarity and
duality of finite and infinite graphs, J. Combin. Theory B 29 (1980), 244–271.
The existence of such ‘convex’ drawings for 3-connected planar graphs follows
already from the theorem of Steinitz (1922) that these graphs are precisely
the 1-skeletons of 3-dimensional convex polyhedra. Compare also W.T. Tutte,
How to draw a graph, Proc. London Math. Soc. 13 (1963), 743–767.
As one readily observes, adding an edge to a maximal planar graph (of
order at least 6) produces not only a topological K [5] _or K3,3, but both. In_
Chapter 8.3 we shall see that, more generally, every graph with n vertices
and more than 3n − 6 edges contains a TK [5] and, with one easily described
class of exceptions, also a TK3,3. Seymour conjectures that every 5-connected
non-planar graph contains a TK [5] (unpublished).
The simple cycle space basis constructed in the proof of MacLane’s theorem, which consists of the inner face boundaries, is canonical in the following
sense: for every simple basis B of the cycle space of a 2-connected planar graph
there exists a drawing of that graph in which B is precisely the set of inner face
boundaries. (This is proved in Mohar & Thomassen, who also mention some
further planarity criteria.) Our proof of the backward direction of MacLane’s


-----

a planar embedding is actually constructed from a simple basis, is adopted in
K. Wagner, Graphentheorie, BI Hochschultaschenb¨ucher 1972.
The proper setting for duality phenomena between cuts and cycles in abstract graphs (and beyond) is the theory of matroids; see J.G. Oxley, Matroid
_Theory, Oxford University Press 1992._


-----

-----

# 5 Colouring

How many colours do we need to colour the countries of a map in such
a way that adjacent countries are coloured differently? How many days
have to be scheduled for committee meetings of a parliament if every
committee intends to meet for one day and some members of parliament
serve on several committees? How can we find a school timetable of minimum total length, based on the information of how often each teacher
has to teach each class?
_vertex_
A vertex colouring of a graph G = (V, E) is a map c: V → _S such_ _colouring_
that c(v) = c(w) whenever v and w are adjacent. The elements of the
_̸_
set S are called the available colours. All that interests us about S is
its size: typically, we shall be asking for the smallest integer k such that
_chromatic_
_G has a k-colouring, a vertex colouring c: V_ 1, . . ., k . This k is the
_→{_ _}_ _number_
(vertex-) chromatic number of G; it is denoted by χ(G). A graph G with _χ(G)_
_χ(G) = k is called k-chromatic; if χ(G) ⩽_ _k, we call G k-colourable._

2


3


1


1


2


_Fig. 5.0.1. A vertex colouring V →{ 1, . . ., 4 }_

Note that a k-colouring is nothing but a vertex partition into k
_colour_
independent sets, now called colour classes; the non-trivial 2-colourable
_classes_
graphs, for example, are precisely the bipartite graphs. Historically,


-----

above, which leads to the problem of determining the maximum chromatic number of planar graphs. The committee scheduling problem, too,
can be phrased as a vertex colouring problem—how?
_edge_
An edge colouring of G = (V, E) is a map c: E _S with c(e)_ = c(f )
_colouring_ _→_ _̸_
for any adjacent edges e, f . The smallest integer k for which a k-edge_chromatic_ _colouring exists, i.e. an edge colouring c: E →{ 1, . . ., k }, is the edge-_
_index_ _chromatic number_, or chromatic index, of G; it is denoted by χ[′](G).
_χ[′](G)_ The third of our introductory questions can be modelled as an edge
colouring problem in a bipartite multigraph (how?).
Clearly, every edge colouring of G is a vertex colouring of its line
graph L(G), and vice versa; in particular, χ[′](G) = χ(L(G)). The problem of finding good edge colourings may thus be viewed as a restriction
of the more general vertex colouring problem to this special class of
graphs. As we shall see, this relationship between the two types of
colouring problem is reflected by a marked difference in our knowledge
about their solutions: while there are only very rough estimates for χ,
its sister χ[′] always takes one of two values, either ∆or ∆+ 1.

###### 5.1 Colouring maps and planar graphs

If any result in graph theory has a claim to be known to the world
outside, it is the following four colour theorem (which implies that every
map can be coloured with at most four colours):

**Theorem 5.1.1. (Four Colour Theorem)**
_Every planar graph is 4-colourable._

Some remarks about the proof of the four colour theorem and its history
can be found in the notes at the end of this chapter. Here, we prove the
following weakening:

**Proposition 5.1.2. (Five Colour Theorem)**
_Every planar graph is 5-colourable._

(4.1.1)
(4.2.8) _Proof . Let G be a plane graph with n ⩾_ 6 vertices and m edges. We
assume inductively that every plane graph with fewer than n vertices
_n, m_ can be 5-coloured. By Corollary 4.2.8,

_d(G) = 2m/n ⩽_ 2 (3n − 6)/n < 6 ;

_v_ let v _[∈]_ _G be a vertex of degree at most 5. By the induction hypothesis,_
_H_ the graph H := G _v has a vertex colouring c: V (H)_ 1, . . ., 5 . If c
_−_ _→{_ _}_
_c_ uses at most 4 colours for the neighbours of v, we can extend it to a 5colouring of G. Let us assume, therefore, that v has exactly 5 neighbours,


-----

Let D be an open disc around v, so small that it meets only those _D_
five straight edge segments of G that contain v. Let us enumerate these
segments according to their cyclic position in D as s1, . . ., s5, and let _s1, . . ., s5_
_vvi be the edge containing si (i = 1, . . ., 5; Fig. 5.1.1). Without loss of_ _v1, . . ., v5_
generality we may assume that c(vi) = i for each i.

_v1_


_v5_


_P_
_s5_ _v_

_D_

_s3_
_s4_

_v3_
_v4_


_Fig. 5.1.1. The proof of the five colour theorem_

Let us show first that every v1– v3 path P ⊆ _H separates v2 from_ _P_
_v4 in H. Clearly, this is the case if and only if the cycle C := vv1Pv3v_ _C_
separates v2 from v4 in G. We prove this by showing that v2 and v4 lie
in different faces of C.
Consider the two regions of D ∖ (s1 ∪ _s3)._ One of these regions
meets s2, the other s4. Since C ∩ _D ⊆_ _s1 ∪_ _s3, the two regions are_
each contained within a face of C. Moreover, these faces are distinct:
otherwise, D would meet only one face of C, contrary to the fact that
_v lies on the boundary of both faces (Theorem 4.1.1). Thus D ∩_ _s2 and_
_D ∩_ _s4 lie in distinct faces of C. As C meets the edges vv2 ⊇_ _s2 and_
_vv4_ _s4 only in v, the same holds for v2 and v4._
_⊇_
Given i, j _[∈]_ _{ 1, . . ., 5 }, let Hi,j be the subgraph of H induced by_ _Hi,j_
the vertices coloured i or j. We may assume that the component C1 of
_H1,3 containing v1 also contains v3. Indeed, if we interchange the colours_
1 and 3 at all the vertices of C1, we obtain another 5-colouring of H;
if v3 /∈ _C1, then v1 and v3 are both coloured 3 in this new colouring,_
and we may assign colour 1 to v. Thus, H1,3 contains a v1– v3 path P .
As shown above, P separates v2 from v4 in H. Since P ∩ _H2,4 = ∅,_
this means that v2 and v4 lie in different components of H2,4. In the
component containing v2, we now interchange the colours 2 and 4, thus
recolouring v2 with colour 4. Now v no longer has a neighbour coloured 2,
and we may give it this colour. 
As a backdrop to the two famous theorems above, let us cite another
well-known result:

**Theorem 5.1.3. (Gr¨otzsch 1959)**


-----

###### 5.2 Colouring vertices

How do we determine the chromatic number of a given graph? How can
we find a vertex-colouring with as few colours as possible? How does
the chromatic number relate to other graph invariants, such as average
degree, connectivity or girth?
Straight from the definition of the chromatic number we may derive
the following upper bound:

**Proposition 5.2.1. Every graph G with m edges satisfies**


�

_χ(G) ⩽_ [1]2 [+]


2m + [1]4 _[.]_


_Proof . Let c be a vertex colouring of G with k = χ(G) colours. Then_
_G has at least one edge between any two colour classes: if not, we could_
have used the same colour for both classes. Thus, m ⩾ [1]2 _[k][(][k]_ _[−]_ [1). Solving]

this inequality for k, we obtain the assertion claimed.       
One obvious way to colour a graph G with not too many colours is
_greedy_
the following greedy algorithm: starting from a fixed vertex enumeration
_algorithm_
_v1, . . ., vn of G, we consider the vertices in turn and colour each vi with_
the first available colour—e.g., with the smallest positive integer not
already used to colour any neighbour of vi among v1, . . ., vi−1. In this
way, we never use more than ∆(G) + 1 colours, even for unfavourable
choices of the enumeration v1, . . ., vn. If G is complete or an odd cycle,
then this is even best possible.
In general, though, this upper bound of ∆+ 1 is rather generous,
even for greedy colourings. Indeed, when we come to colour the vertex
_vi in the above algorithm, we only need a supply of dG[ v1,...,vi ](vi) + 1_
rather than dG(vi)+1 colours to proceed; recall that, at this stage, the algorithm ignores any neighbours vj of vi with j > i. Hence in most graphs,
there will be scope for an improvement of the ∆+1 bound by choosing a
particularly suitable vertex ordering to start with: one that picks vertices
of large degree early (when most neighbours are ignored) and vertices
of small degree last. Locally, the number dG[ v1,...,vi ](vi) + 1 of colours
required will be smallest if vi has minimum degree in G [ v1, . . ., vi ]. But
this is easily achieved: we just choose vn first, with d(vn) = δ(G), then
choose as vn−1 a vertex of minimum degree in G − _vn, and so on._
The least number k such that G has a vertex enumeration in which
_colouring_ each vertex is preceded by fewer than k of its neighbours is called
_number_ the colouring number col(G) of G. The enumeration we just discussed
col(G) shows that col(G) ⩽ maxH⊆G δ(H) + 1. But for H ⊆ _G clearly also_
col(G) ⩾ col(H) and col(H) ⩾ _δ(H) + 1, since the ‘back-degree’ of the_
last vertex in any enumeration of H is just its ordinary degree in H,


-----

**Proposition 5.2.2. Every graph G satisfies**

_χ(G) ⩽_ col(G) = max { δ(H) | H ⊆ _G } + 1 ._

                    
[ 9.2.1 ]
**Corollary 5.2.3. Every graph G has a subgraph of minimum degree at** [ 9.2.3 ]
_least χ(G) −_ 1. - [ 11.2.3 ]

The colouring number of a graph is closely related to its arboricity; see
the remark following Theorem 3.5.4.

As we have seen, every graph G satisfies χ(G) ⩽ ∆(G) + 1, with
equality for complete graphs and odd cycles. In all other cases, this
general bound can be improved a little:

**Theorem 5.2.4. (Brooks 1941)**
_Let G be a connected graph. If G is neither complete nor an odd cycle,_
_then_
_χ(G) ⩽_ ∆(G) .

_Proof . We apply induction on |G|. If ∆(G) ⩽_ 2, then G is a path or
a cycle, and the assertion is trivial. We therefore assume that ∆:= ∆
∆(G) ⩾ 3, and that the assertion holds for graphs of smaller order.
Suppose that χ(G) > ∆.
Let v _[∈]_ _G be a vertex and H := G −_ _v._ Then χ(H) ⩽ ∆: by _v, H_
induction, every component H _[′]_ of H satisfies χ(H _[′]) ⩽_ ∆(H _[′]) ⩽_ ∆unless
_H_ _[′]_ is complete or an odd cycle, in which case χ(H _[′]) = ∆(H_ _[′]) + 1 ⩽_ ∆
as every vertex of H _[′]_ has maximum degree in H _[′]_ and one such vertex is
also adjacent to v in G.
Since H can be ∆-coloured but G cannot, we have the following:

_Every ∆-colouring of H uses all the colours 1, . . ., ∆_ _on_
(1)
_the neighbours of v; in particular, d(v) = ∆._

Given any ∆-colouring of H, let us denote the neighbour of v coloured i by vi, i = 1, . . ., ∆. For all i ̸= j, let Hi,j denote the subgraph _v1, . . ., v∆_
of H spanned by all the vertices coloured i or j. _Hi,j_


_For all i ̸= j, the vertices vi and vj lie in a common com-_ (2)
_ponent Ci,j of Hi,j._

Otherwise we could interchange the colours i and j in one of those components; then vi and vj would be coloured the same, contrary to (1).

_Ci,j is always a vi– vj path._ (3)

Indeed, let P be a vi– vj path in Ci,j. As dH (vi) ⩽ ∆ _−_ 1, the neighbours


_Ci,j_


-----

contrary to (1). Hence the neighbour of vi on P is its only neighbour
in Ci,j, and similarly for vj. Thus if Ci,j ̸= P, then P has an inner
vertex with three identically coloured neighbours in H; let u be the first
such vertex on P (Fig. 5.2.1). Since at most ∆ 2 colours are used
_−_
on the neighbours of u, we may recolour u. But this makes P˚u into a
component of Hi,j, contradicting (2).

_vj_ _j_ _i_ _j_ _Ci,j_

_i_

_v_

_j_ _i_


_vi_


_P˚u_


_Fig. 5.2.1. The proof of (3) in Brooks’s theorem_

_For distinct i, j, k, the paths Ci,j and Ci,k meet only in vi._ (4)

For if vi ̸= u ∈ _Ci,j ∩_ _Ci,k, then u has two neighbours coloured j and two_
coloured k, so we may recolour u. In the new colouring, vi and vj lie in
different components of Hi,j, contrary to (2).
The proof of the theorem now follows easily. If the neighbours of v
are pairwise adjacent, then each has ∆neighbours in N (v) _v_ already,
_∪{_ _}_
so G = G [ N (v) _v_ ] = K [∆+1]. As G is complete, there is nothing to
_∪{_ _}_
_v1, . . ., v∆_ show. We may thus assume that v1v2 /[∈] _G, where v1, . . ., v∆_ derive their
_c_ names from some fixed ∆-colouring c of H. Let u ̸= v2 be the neighbour
_u_ of v1 on the path C1,2; then c(u) = 2. Interchanging the colours 1 and 3
_c[′]_ in C1,3, we obtain a new colouring c[′] of H; let vi[′][,][ H]i,j[′] [,][ C]i,j[′] [etc. be defined]
with respect to c[′] in the obvious way. As a neighbour of v1 = v3[′] [, our]
vertex u now lies in C2[′] _,3_ [, since][ c][′][(][u][) =][ c][(][u][) = 2. By (4) for][ c][, however,]
the path ˚v1C1,2 retained its original colouring, so u _[∈]_ ˚v1C1,2 ⊆ _C1[′]_ _,2[.]_
Hence u _[∈]_ _C2[′]_ _,3_ 1,2[, contradicting (4) for][ c][′][.]      
_[∩]_ _[C]_ _[′]_

As we have seen, a graph G of large chromatic number must have
large maximum degree: at least χ(G) 1. What else can we say about
_−_
the structure of graphs with large chromatic number?
One obvious possible cause for χ(G) ⩾ _k is the presence of a K_ _[k]_

subgraph. This is a local property of G, compatible with arbitrary values
of global invariants such as ε and κ. Hence, the assumption of χ(G) ⩾ _k_
does not tell us anything about those invariants for G itself. It does,
however, imply the existence of a subgraph where those invariants are
large: by Corollary 5.2.3, G has a subgraph H with δ(H) ⩾ _k −_ 1, and


-----

So are those somewhat denser subgraphs the ‘cause’ for the large
value of χ? Do they, in turn, necessarily contain a graph of high chromatic number—maybe even one from some small collection of canonical
such graphs, such as K _[k]? Interestingly, this is not so: those subgraphs of_
large but ‘constant’ average degree—bounded below only by a function
of k, not of _G_ —are not nearly dense enough to contain (necessarily)
_|_ _|_
any particular graph of high chromatic number, let alone K _[k].[1]_

Yet even if the above local structures do not appear to help, it
might still be the case that, somehow, a high chromatic number forces
the existence of certain canonical highly chromatic subgraphs. That this
is in fact not the case will be our main result in Chapter 11: according
to a classic result of Erd˝os, proved by probabilistic methods, there are
_graphs of arbitrarily large chromatic number and yet arbitrarily large_
_girth (Theorem 11.2.2). Thus given any graph H that is not a forest, for_
every k _[∈]_ N there are graphs G with χ(G) ⩾ _k but H ̸⊆_ _G.[2]_

Thus, contrary to our initial guess that a large chromatic number
might always be caused by some dense local substructure, it can in fact
occur as a purely global phenomenon: after all, locally (around each
vertex) a graph of large girth looks just like a tree, and is in particular
2-colourable there!

So far, we asked what a high chromatic number implies: it forces
the invariants δ, d, ∆and κ up in some subgraph, but it does not imply
the existence of any concrete subgraph of large chromatic number. Let
us now consider the converse question: from what assumptions could we
deduce that the chromatic number of a given graph is large?
Short of a concrete subgraph known to be highly chromatic (such
as K _[k]), there is little or nothing in sight: no values of the invariants_
studied so far imply that the graph considered has a large chromatic
number. (Recall the example of Kn,n.) So what exactly can cause high
chromaticity as a global phenomenon largely remains a mystery!
Nevertheless, there exists a simple—though not always short—
procedure to construct all the graphs of chromatic number ⩾ _k. For_
_k-con-_
each k ∈ N, let us define the class of k-constructible graphs recursively _structible_
as follows:

(i) K _[k]_ is k-constructible.

(ii) If G is k-constructible and x, y _[∈]_ _V (G) are non-adjacent, then also_
(G + xy)/xy is k-constructible.

1 This is obvious from the examples of Kn,n, which are 2-chromatic but whose
connectivity and average degree n exceeds any constant bound. Which (non-constant)
average degree exactly will force the existence of a given subgraph will be the topic
of Chapter 7.
2 By Corollaries 5.2.3 and 1.5.4, of course, every graph of sufficiently high chro

-----

(iii) If G1, G2 are k-constructible and there are vertices x, y1, y2 such
that G1 ∩ _G2 = { x }, xy1_ _[∈]_ _E(G1) and xy2_ _[∈]_ _E(G2), then also_
(G1 ∪ _G2) −_ _xy1 −_ _xy2 + y1y2 is k-constructible (Fig. 5.2.2)._

_y1_ _y2_ _y1_ _y2_

_x_ _x_

_Fig. 5.2.2. The Haj´os construction (iii)_

One easily checks inductively that all k-constructible graphs—and hence
their supergraphs—are at least k-chromatic. Indeed, if (G + xy)/xy as
in (ii) has a colouring with fewer than k colours, then this defines such
a colouring also for G, a contradiction. Similarly, in any colouring of
the graph constructed in (iii), the vertices y1 and y2 do not both have
the same colour as x, so this colouring induces a colouring of either G1
or G2 and hence uses at least k colours.
It is remarkable, though, that the converse holds too:

**Theorem 5.2.5. (Haj´os 1961)**
_Let G be a graph and k_ _[∈]_ N. Then χ(G) ⩾ _k if and only if G has a_
_k-constructible subgraph._

_Proof ._ Let G be a graph with χ(G) ⩾ _k; we show that G has a k-_
constructible subgraph. Suppose not; then k ⩾ 3. Adding some edges
if necessary, let us make G edge-maximal with the property that none
of its subgraphs is k-constructible. Now G is not a complete r-partite
graph for any r: for then χ(G) ⩾ _k would imply r ⩾_ _k, and G would_
contain the k-constructible graph K[k].
Since G is not a complete multipartite graph, non-adjacency is not
an equivalence relation on V (G). So there are vertices y1, x, y2 such that
_y1x, xy2_ _y1x, xy2 /∈_ _E(G) but y1y2 ∈_ _E(G). Since G is edge-maximal without_
a k-constructible subgraph, each edge xyi lies in some k-constructible
_H1, H2_ subgraph Hi of G + xyi (i = 1, 2).
_H2[′]_ Let H2[′] [be an isomorphic copy of][ H][2] [that contains][ x][ and][ H][2] _[−]_ _[H][1]_
_v[′]_ _etc._ but is otherwise disjoint from G, together with an isomorphism v �→ _v[′]_
from H2 to H2[′] [that fixes][ H][2] _[∩]_ _[H]2[′]_ [pointwise. Then][ H][1] _[∩]_ _[H]2[′]_ [=][ {][ x][ }][, so]

_H := (H1 ∪_ _H2[′]_ [)][ −] _[xy][1]_ _[−]_ _[xy]2[′]_ [+][ y][1][y]2[′]

is k-constructible by (iii). One vertex at a time, let us identify in H each


-----

each of these identifications amounts to a construction step of type (ii).
Eventually, we obtain the graph

(H1 ∪ _H2) −_ _xy1 −_ _xy2 + y1y2 ⊆_ _G ;_

this is the desired k-constructible subgraph of G. 
###### 5.3 Colouring edges

Clearly, every graph G satisfies χ[′](G) ⩾ ∆(G). For bipartite graphs, we
have equality here:

**Proposition 5.3.1. (K¨onig 1916)**
_Every bipartite graph G satisfies χ[′](G) = ∆(G)._

_Proof . We apply induction on_ _G_ . For _G_ = 0 the assertion holds. (1.6.1)
_∥_ _∥_ _∥_ _∥_
Now assume that ∥G∥ ⩾ 1, and that the assertion holds for graphs with
fewer edges. Let ∆:= ∆(G), pick an edge xy _[∈]_ _G, and choose a ∆-_ ∆, xy
edge-colouring of G _xy by the induction hypothesis. Let us refer to_
_−_
the edges coloured α as α-edges, etc. _α-edge_
In G _xy, each of x and y is incident with at most ∆_ 1 edges.
_−_ _−_
Hence there are α, β _[∈]_ _{ 1, . . ., ∆_ _} such that x is not incident with an_ _α, β_
_α-edge and y is not incident with a β-edge. If α = β, we can colour the_
edge xy with this colour and are done; so we may assume that α = β,
_̸_
and that x is incident with a β-edge.
Let us extend this edge to a maximal walk W whose edges are
coloured β and α alternately. Since no such walk contains a vertex twice
(why not?), W exists and is a path. Moreover, W does not contain y:
if it did, it would end in y on an α-edge (by the choice of β) and thus
have even length, so W + _xy would be an odd cycle in G (cf. Proposition_
1.6.1). We now recolour all the edges on W, swapping α with β. By the
choice of α and the maximality of W, adjacent edges of G _xy are still_
_−_
coloured differently. We have thus found a ∆-edge-colouring of G _xy_
_−_
in which neither x nor y is incident with a β-edge. Colouring xy with β,
we extend this colouring to a ∆-edge-colouring of G. 
**Theorem 5.3.2. (Vizing 1964)**
_Every graph G satisfies_

∆(G) ⩽ _χ[′](G) ⩽_ ∆(G) + 1 .

_Proof . We prove the second inequality by induction on_ _G_ . For _G_ = 0 _V, E_
_∥_ _∥_ _∥_ _∥_
( ) ∆ ∆( )


-----

given, and assume that the assertion holds for graphs with fewer edges.
_colouring_ Instead of ‘(∆+ 1)-edge-colouring’ let us just say ‘colouring’. An edge
_α-edge_ coloured α will again be called an α-edge.
For every edge e _[∈]_ _G there exists a colouring of G −_ _e, by the_
induction hypothesis. In such a colouring, the edges at a given vertex
_v use at most d(v) ⩽_ ∆colours, so some colour β _[∈]_ _{ 1, . . ., ∆+ 1 } is_
_missing_ _missing at v. For any other colour α, there is a unique maximal walk_
(possibly trivial) starting at v, whose edges are coloured alternately α
_α/β - path_ and β. This walk is a path; we call it the α/β - path from v.
Suppose that G has no colouring. Then the following holds:

_Given xy_ _[∈]_ _E, and any colouring of G −_ _xy in which the_
_colour α is missing at x and the colour β is missing at y,_ (1)
_the α/β - path from y ends in x._

Otherwise we could interchange the colours α and β along this path and
colour xy with α, obtaining a colouring of G (contradiction).
_xy0_ Let xy0 _∈_ _G be an edge._ By induction, G0 := G − _xy0 has a_
_G0, c0, α_ colouring c0. Let α be a colour missing at x in this colouring. Further,
_y1, . . ., yk_ let y0, y1, . . ., yk be a maximal sequence of distinct neighbours of x in G,
such that c0(xyi) is missing in c0 at yi−1 for each i = 1, . . ., k. For each
_Gi_ of the graphs Gi := G − _xyi we define a colouring ci, setting_

_ci(e) :=_ � _c0(xyj+1)_ for e = xyj with j _[∈]_ _{ 0, . . ., i −_ 1 }
_ci_ _c0(e)_ otherwise;

note that in each of these colourings the same colours are missing at x
as in c0.
_β_ Now let β be a colour missing at yk in c0. Clearly, β is still missing
at yk in ck. If β were also missing at x, we could colour xyk with β
and thus extend ck to a colouring of G. Hence, x is incident with a
_β-edge (in every colouring). By the maximality of k, therefore, there is_
an i _[∈]_ _{ 1, . . ., k −_ 1 } such that

_i_ _c0(xyi) = β ._

_P_ Let P be the α/β - path from yk in Gk (with respect to ck; Fig. 5.3.1).
By (1), P ends in x, and it does so on a β-edge, since α is missing at x.
As β = c0(xyi) = ck(xyi−1), this is the edge xyi−1. In c0, however, and
hence also in ci−1, β is missing at yi−1 (by (2) and the choice of yi); let
_P_ _[′]_ _P_ _[′]_ be the α/β - path from yi−1 in Gi−1 (with respect to ci−1). Since P _[′]_
is uniquely determined, it starts with yi−1Pyk; note that the edges of
_P˚x are coloured the same in ci−1 as in ck. But in c0, and hence in ci−1,_
there is no β-edge at yk (by the choice of β). Therefore P _[′]_ ends in yk,


-----

_yk_


_P_

_Gk_


_y0_


_Fig. 5.3.1. The α/β - path P in Gk_

Vizing’s theorem divides the finite graphs into two classes according
to their chromatic index; graphs satisfying χ[′] = ∆are called (imaginatively) class 1, those with χ[′] = ∆+ 1 are class 2 .

###### 5.4 List colouring

In this section, we take a look at a relatively recent generalization of the
concepts of colouring studied so far. This generalization may seem a little
far-fetched at first glance, but it turns out to supply a fundamental link
between the classical (vertex and edge) chromatic numbers of a graph
and its other invariants.
Suppose we are given a graph G = (V, E), and for each vertex of
_G a list of colours permitted at that particular vertex: when can we_
colour G (in the usual sense) so that each vertex receives a colour from
its list? More formally, let (Sv)v ∈V be a family of sets. We call a vertex
colouring c of G with c(v) _[∈]_ _Sv for all v_ _∈_ _V a colouring from the_
_lists Sv. The graph G is called k-list-colourable, or k-choosable, if, for_ _k-choosable_
every family (Sv)v ∈V with |Sv| = k for all v, there is a vertex colouring
of G from the lists Sv. The least integer k for which G is k-choosable is _choice_
the list-chromatic number, or choice number ch(G) of G. _number_
List-colourings of edges are defined analogously. The least integer ch(G)
_k such that G has an edge colouring from any family of lists of size k_
is the list-chromatic index ch[′](G) of G; formally, we just set ch[′](G) := ch[′](G)
ch(L(G)), where L(G) is the line graph of G.
In principle, showing that a given graph is k-choosable is more difficult than proving it to be k-colourable: the latter is just the special case
of the former where all lists are equal to 1, . . ., k . Thus,
_{_ _}_

ch(G) ⩾ _χ(G)_ and ch[′](G) ⩾ _χ[′](G)_


-----

In spite of these inequalities, many of the known upper bounds for
the chromatic number have turned out to be valid for the choice number, too. Examples for this phenomenon include Brooks’s theorem and
Proposition 5.2.2; in particular, graphs of large choice number still have
subgraphs of large minimum degree. On the other hand, it is easy to construct graphs for which the two invariants are wide apart (Exercise 24).
Taken together, these two facts indicate a little how far those general
upper bounds on the chromatic number may be from the truth.
The following theorem shows that, in terms of its relationship to
other graph invariants, the choice number differs fundamentally from the
chromatic number. As mentioned before, there are 2-chromatic graphs
of arbitrarily large minimum degree, e.g. the graphs Kn,n. The choice
number, however, will be forced up by large values of invariants like δ, ε
or κ:

**Theorem 5.4.1. (Alon 1993)**
_There exists a function f_ : N _→_ N such that, given any integer k, all graphs
_G with average degree d(G) ⩾_ _f_ (k) satisfy ch(G) ⩾ _k._

The proof of Theorem 5.4.1 uses probabilistic methods as introduced in
Chapter 11.

Empirically, the choice number’s different character is highlighted
by another phenomenon: even in cases where known bounds for the
chromatic number could be transferred to the choice number, their proofs
have tended to be rather different.
One of the simplest and most impressive examples for this is the list
version of the five colour theorem: every planar graph is 5-choosable.
This had been conjectured for almost 20 years, before Thomassen found
a very simple induction proof. This proof does not use the five colour
theorem—which thus gets reproved in a very different way.

**Theorem 5.4.2. (Thomassen 1994)**
_Every planar graph is 5-choosable._

(4.2.6) _Proof . We shall prove the following assertion for all plane graphs G with_
at least 3 vertices:


_Suppose that every inner face of G is bounded by a trian-_
_gle and its outer face by a cycle C = v1 . . . vkv1. Suppose_
_further that v1 has already been coloured with the col-_
_our 1, and v2 has been coloured 2. Suppose finally that_
_with every other vertex of C a list of at least 3 colours is_
_associated, and with every vertex of G_ _C a list of at least_
_−_
5 colours. Then the colouring of v1 and v2 can be extended


( )
_∗_


-----

Let us check first that ( ) implies the assertion of the theorem.
_∗_
Let any plane graph be given, together with a list of 5 colours for each
vertex. Add edges to this graph until it is a maximal plane graph G.
By Proposition 4.2.6, G is a plane triangulation; let v1v2v3v1 be the
boundary of its outer face. We now colour v1 and v2 (differently) from
their lists, and extend this colouring by ( ) to a colouring of G from the
_∗_
lists given.
Let us now prove ( ), by induction on _G_ . If _G_ = 3, then G =
_∗_ _|_ _|_ _|_ _|_
_C and the assertion is trivial._ Now let |G| ⩾ 4, and assume (∗) for
smaller graphs. If C has a chord vw, then vw lies on two unique cycles _vw_
_C1, C2 ⊆_ _C + vw with v1v2 ∈_ _C1 and v1v2 /∈_ _C2. For i = 1, 2, let Gi_
denote the subgraph of G induced by the vertices lying on Ci or in its
inner face (Fig. 5.4.1). Applying the induction hypothesis first to G1
and then—with the colours now assigned to v and w—to G2 yields the
desired colouring of G.


_G1_


_v1_


2 _v2 = w_

_v_

_G2_

_Fig. 5.4.1. The induction step with a chord vw; here the case_
of w = v2

If C has no chord, let v1, u1, . . ., um, vk−1 be the neighbours of vk in _u1, . . ., um_
their natural cyclic order order around vk;[3] by definition of C, all those
neighbours ui lie in the inner face of C (Fig. 5.4.2). As the inner faces


_vk_


_v1_


_vk−1_

_C_ _[′]_


_v2_


_Fig. 5.4.2. The induction step without a chord_


-----

of C are bounded by triangles, P := v1u1 . . . umvk−1 is a path in G, and
_C[′]_ _C_ _[′]_ := P ∪ (C − _vk) a cycle._

We now choose two different colours j, ℓ = 1 from the list of̸ _vk and_
delete these colours from the lists of all the vertices ui. Then every list of
a vertex on C _[′]_ still has at least 3 colours, so by induction we may colour
_C_ _[′]_ and its interior, i.e. the graph G − _vk. At least one of the two colours_
_j, ℓ_ is not used for vk−1, and we may assign that colour to vk.         
As is often the case with induction proofs, the trick of the proof
above lies in the delicately balanced strengthening of the assertion
proved. Note that the proof uses neither traditional colouring arguments
(such as swapping colours along a path) nor the Euler formula implicit in
the standard proof of the five colour theorem. This suggests that maybe
in other unsolved colouring problems too it might be of advantage to
aim straight for their list version, i.e. to prove an assertion of the form
ch(G) ⩽ _k instead of the formally weaker χ(G) ⩽_ _k. Unfortunately,_
this approach fails for the four colour theorem: planar graphs are not in
general 4-choosable.

As mentioned before, the chromatic number of a graph and its choice
number may differ a lot. Surprisingly, however, no such examples are
known for edge colourings. Indeed it has been conjectured that none
exist:

**List colouring conjecture. Every graph G satisfies ch[′](G) = χ[′](G).**

We shall prove the list colouring conjecture for bipartite graphs. As
a tool we shall use orientations of graphs, defined in Chapter 1.10. If D
_N_ [+](v) is a directed graph and v _[∈]_ _V (D), we denote by N_ [+](v) the set, and by
_d[+](v)_ _d[+](v) the number, of vertices w such that D contains an edge directed_
from v to w.
To see how orientations come into play in the context of colouring,
let us recall the greedy algorithm from Section 5.2. In order to apply the
algorithm to a graph G, we first have to choose a vertex enumeration
_v1, . . ., vn of G. The enumeration chosen defines an orientation of G:_
just orient every edge vivj ‘backwards’, from vi to vj if i > j. Then, for
each vertex vi to be coloured, the algorithm considers only those edges
at vi that are directed away from vi: if d[+](v) < k for all vertices v, it will
use at most k colours. Moreover, the first colour class U found by the
algorithm has the following property: it is an independent set of vertices
to which every other vertex sends an edge. The second colour class has
the same property in G _U_, and so on.
_−_
The following lemma generalizes this to orientations D of G that do
not necessarily come from a vertex enumeration, but may contain some
( )


-----

if, for every vertex v _[∈]_ _D −_ _U_, there is an edge in D directed from v
to a vertex in U . Note that kernels of non-empty directed graphs are
themselves non-empty.

**Lemma 5.4.3. Let H be a graph and (Sv)v ∈V (H) a family of lists. If H**
_has an orientation D with d[+](v) < |Sv| for every v, and such that every_
_induced subgraph of D has a kernel, then H can be coloured from the_
_lists Sv._

_Proof . We apply induction on_ _H_ . For _H_ = 0 we take the empty
_|_ _|_ _|_ _|_
colouring. For the induction step, let _H_ _> 0. Let α be a colour occur-_ _α_
_|_ _|_
ring in one of the lists Sv, and let D be an orientation of H as stated.
The vertices v with α ∈ _Sv span a non-empty subgraph D[′]_ in D; by _D[′]_
assumption, D[′] has a kernel U = . _U_
_̸_ _∅_
Let us colour the vertices in U with α, and remove α from the lists
of all the other vertices of D[′]. Since each of those vertices sends an edge
to U, the modified lists Sv[′] [for][ v][ ∈] _[D][ −]_ _[U][ again satisfy the condition]_
_d[+](v) < |Sv[′]_ _[|][ in][ D][ −]_ _[U]_ [. Since][ D][ −] _[U][ is an orientation of][ H][ −]_ _[U]_ [, we]
can thus colour H _U from those lists by the induction hypothesis. As_
_−_
none of these lists contains α, this extends our colouring U _α_ to
_→{_ _}_
the desired list colouring of H. 
**Theorem 5.4.4. (Galvin 1995)**
_Every bipartite graph G satisfies ch[′](G) = χ[′](G)._

_Proof . Let G =: (X_ _Y, E), where_ _X, Y_ is a vertex bipartition of G. _X, Y, E_
_∪_ _{_ _}_
Let us say that two edges of G meet in X if they share an end in X, and
correspondingly for Y . Let χ[′](G) =: k, and let c be a k-edge-colouring _k_
of G. _c_
Clearly, ch[′](G) ⩾ _k; we prove that ch[′](G) ⩽_ _k. Our plan is to use_
Lemma 5.4.3 to show that the line graph H of G is k-choosable. To apply _H_
the lemma, it suffices to find an orientation D of H with d[+](v) < k for
every vertex v, and such that every induced subgraph of D has a kernel.
To define D, consider adjacent e, e[′ ∈] _E, say with c(e) < c(e[′]). If e and_ _D_
_e[′]_ meet in X, we orient the edge ee[′ ∈] _H from e[′]_ towards e; if e and e[′]

meet in Y, we orient it from e to e[′] (Fig 5.4.3).
Let us compute d[+](e) for given e _[∈]_ _E = V (D). If c(e) = i, say,_
then every e[′ ∈] _N_ [+](e) meeting e in X has its colour in 1, . . ., i 1,
_{_ _−_ _}_
and every e[′ ∈] _N_ [+](e) meeting e in Y has its colour in _i + 1, . . ., k_ .
_{_ _}_
As any two neighbours e[′] of e meeting e either both in X or both in
_Y are themselves adjacent and hence coloured differently, this implies_
_d[+](e) < k as desired._
It remains to show that every induced subgraph D[′] of D has a _D[′]_
kernel. We show this by induction on |D[′]|. For D[′] = ∅, the empty set
is a kernel; so let |D[′]| ⩾ 1. Let E[′] := V (D[′]) ⊆ _E. For every x ∈_ _X_ _E[′]_


-----

1

2

1 3

2

_X_ _Y_


_G_


_Fig. 5.4.3. Orienting the line graph of G_

_U_ _c-value, and let U denote the set of all those edges ex. Then every edge_
_e[′ ∈]_ _E[′]_ ∖ _U meets some e ∈_ _U in X, and the edge ee[′ ∈]_ _D[′]_ is directed
from e[′] to e. If U is independent, it is thus a kernel of D[′] and we are
home; let us assume, therefore, that U is not independent.
_e, e[′]_ Let e, e[′ ∈] _U be adjacent, and assume that c(e) < c(e[′]). By definition_
of U, e and e[′] meet in Y, so the edge ee[′ ∈] _D[′]_ is directed from e to e[′].
_U_ _[′]_ By the induction hypothesis, D[′] _−_ _e has a kernel U_ _[′]. If e[′ ∈]_ _U_ _[′], then U_ _[′]_
is also a kernel of D[′], and we are done. If not, there exists an e[′′ ∈] _U_ _[′]_

such that D[′] has an edge directed from e[′] to e[′′]. If e[′] and e[′′] met in X,
then c(e[′′]) < c(e[′]) by definition of D, contradicting e[′ ∈] _U_ . Hence e[′] and
_e[′′]_ meet in Y, and c(e[′]) < c(e[′′]). Since e and e[′] meet in Y, too, also e
and e[′′] meet in Y, and c(e) < c(e[′]) < c(e[′′]). So the edge ee[′′] is directed
from e towards e[′′], so again U _[′]_ is also a kernel of D[′].       
By Proposition 5.3.1, we now know the exact list-chromatic index
of bipartite graphs:

**Corollary 5.4.5. Every bipartite graph G satisfies ch[′](G) = ∆(G).**

                       
###### 5.5 Perfect graphs

As discussed in Section 5.2, a high chromatic number may occur as a
purely global phenomenon: even when a graph has large girth, and thus
locally looks like a tree, its chromatic number may be arbitrarily high.
Since such ‘global dependence’ is obviously difficult to deal with, one may
become interested in graphs where this phenomenon does not occur, i.e.
whose chromatic number is high only when there is a local reason for it.
Before we make this precise, let us note two definitions for a graph G.
_ω(G)_ The greatest integer r such that K _[r]_ _G is the clique number ω(G) of G,_
_⊆_
and the greatest integer r such that K _[r]_ _G (induced) is the indepen-_
_⊆_
( ) ( ) ( ) ( ) ( )


-----

A graph is called perfect if every induced subgraph H _G has_ _perfect_
_⊆_
chromatic number χ(H) = ω(H), i.e. if the trivial lower bound of ω(H)
colours always suffices to colour the vertices of H. Thus, while proving
an assertion of the form χ(G) > k may in general be difficult, even
in principle, for a given graph G, it can always be done for a perfect
graph simply by exhibiting some K[k][+1] subgraph as a ‘certificate’ for
non-colourability with k colours.
At first glance, the structure of the class of perfect graphs appears
somewhat contrived: although it is closed under induced subgraphs (if
only by explicit definition), it is not closed under taking general subgraphs or supergraphs, let alone minors (examples?). However, perfection is an important notion in graph theory: the fact that several
fundamental classes of graphs are perfect (as if by fluke) may serve as a
superficial indication of this.[4]

What graphs, then, are perfect? Bipartite graphs are, for instance.
Less trivially, the complements of bipartite graphs are perfect, too—
a fact equivalent to K¨onig’s duality theorem 2.1.1 (Exercise 34). The
so-called comparability graphs are perfect, and so are the interval graphs
(see the exercises); both these turn up in numerous applications.
In order to study at least one such example in some detail, we
prove here that the chordal graphs are perfect: a graph is chordal (or _chordal_
_triangulated_ ) if each of its cycles of length at least 4 has a chord, i.e. if
it contains no induced cycles other than triangles.
To show that chordal graphs are perfect, we shall first characterize
their structure. If G is a graph with induced subgraphs G1, G2 and S,
such that G = G1 _G2 and S = G1_ _G2, we say that G arises from G1_
_∪_ _∩_
and G2 by pasting these graphs together along S. _pasting_

**Proposition 5.5.1. A graph is chordal if and only if it can be con-** [ 12.3.11 ]
_structed recursively by pasting along complete subgraphs, starting from_
_complete graphs._

_Proof . If G is obtained from two chordal graphs G1, G2 by pasting them_
together along a complete subgraph, then G is clearly again chordal:
any induced cycle in G lies in either G1 or G2, and is hence a triangle
by assumption. Since complete graphs are chordal, this proves that all
graphs constructible as stated are chordal.
Conversely, let G be a chordal graph. We show by induction on _G_
_|_ _|_
that G can be constructed as described. This is trivial if G is complete.
We therefore assume that G is not complete, in particular _G_ _> 1, and_
_|_ _|_
that all smaller chordal graphs are constructible as stated. Let a, b ∈ _G_ _a, b_

4 The class of perfect graphs has duality properties with deep connections to
optimization and complexity theory, which are far from understood. Theorem 5.5.5
shows the tip of an iceberg here; for more, the reader is referred to Lov´asz’s survey


-----

_X_ be two non-adjacent vertices, and let X ⊆ _V (G) ∖_ _{ a, b } a minimal_
_C_ set of vertices separating a from b. Let C denote the component of
_G1, G2_ _G −_ _X containing a, and put G1 := G [ V (C) ∪_ _X ] and G2 := G −_ _C._
Then G arises from G1 and G2 by pasting these graphs together along
_S_ _S := G [ X ]._
Since G1 and G2 are both chordal (being induced subgraphs of G)
and hence constructible by induction, it suffices to show that S is com_s, t_ plete. Suppose, then, that s, t ∈ _S are non-adjacent. By the minimality_
of X = V (S) as an a–b separator, both s and t have a neighbour in C.
Hence, there is an X-path from s to t in G1; we let P1 be a shortest such
path. Analogously, G2 contains a shortest X-path P2 from s to t. But
then P1 _P2 is a chordless cycle of length ⩾_ 4 (Fig. 5.5.1), contradicting
_∪_
our assumption that G is chordal.      
_G1_ _s_ _G2_

_P1_ _P2_

_a_ _t_

_b_
_S_

_Fig. 5.5.1. If G1 and G2 are chordal, then so is G_

**Proposition 5.5.2. Every chordal graph is perfect.**

_Proof ._ Since complete graphs are perfect, it suffices by Proposition
5.5.1 to show that any graph G obtained from perfect graphs G1, G2 by
pasting them together along a complete subgraph S is again perfect. So
let H ⊆ _G be an induced subgraph; we show that χ(H) ⩽_ _ω(H)._
Let Hi := H ∩ _Gi for i = 1, 2, and let T := H ∩_ _S. Then T is_
again complete, and H arises from H1 and H2 by pasting along T . As
an induced subgraph of Gi, each Hi can be coloured with ω(Hi) colours.
Since T is complete and hence coloured injectively, two such colourings,
one of H1 and one of H2, may be combined into a colouring of H with
max { ω(H1), ω(H2) } ⩽ _ω(H) colours—if necessary by permuting the_
colours in one of the Hi.       
We now come to the main result in the theory of perfect graphs, the
_perfect graph theorem:_

_perfect_
_graph_ **Theorem 5.5.3. (Lov´asz 1972)**


-----

We shall give two proofs of Theorem 5.5.3. The first of these is Lov´asz’s
original proof, which is still unsurpassed in its clarity and the amount
of ‘feel’ for the problem it conveys. Our second proof, due to Gasparian
(1996), is in fact a very short and elegant linear algebra proof of another
theorem of Lov´asz’s (Theorem 5.5.5), which easily implies Theorem 5.5.3.

Let us prepare our first proof of the perfect graph theorem by a
lemma. Let G be a graph and x ∈ _G a vertex, and let G[′]_ be obtained
from G by adding a vertex x[′] and joining it to x and all the neighbours
of x. We say that G[′] is obtained from G by expanding the vertex x to
_expanding_
an edge xx[′] (Fig. 5.5.2).
_a vertex_

_x_ _x′_

_G[′]_

_G_
_H_

_X ∖_ _{ x }_

_Fig. 5.5.2. Expanding the vertex x in the proof of Lemma 5.5.4_

**Lemma 5.5.4. Any graph obtained from a perfect graph by expanding**
_a vertex is again perfect._

_Proof . We use induction on the order of the perfect graph considered._
Expanding the vertex of K [1] yields K [2], which is perfect. For the induction step, let G be a non-trivial perfect graph, and let G[′] be obtained
from G by expanding a vertex x ∈ _G to an edge xx[′]. For our proof that_ _x, x[′]_
_G[′]_ is perfect it suffices to show χ(G[′]) ⩽ _ω(G[′]): every proper induced_
subgraph H of G[′] is either isomorphic to an induced subgraph of G or
obtained from a proper induced subgraph of G by expanding x; in either
case, H is perfect by assumption and the induction hypothesis, and can
hence be coloured with ω(H) colours.
Let ω(G) =: ω ; then ω(G[′]) ∈ _{ ω, ω + 1 }. If ω(G[′]) = ω + 1, then_ _ω_

_χ(G[′]) ⩽_ _χ(G) + 1 = ω + 1 = ω(G[′])_

and we are done. So let us assume that ω(G[′]) = ω. Then x lies in no
_K_ _[ω]_ _⊆_ _G: together with x[′], this would yield a K_ _[ω][+1]_ in G[′]. Let us colour
_G with ω colours. Since every K_ _[ω]_ _G meets the colour class X of x but_ _X_
_⊆_
not x itself, the graph H := G _−_ (X ∖ _{ x }) has clique number ω(H) < ω_ _H_
(Fig. 5.5.2). Since G is perfect, we may thus colour H with ω 1 colours.
_−_
Now X is independent, so the set (X ∖ _{ x })_ _∪{ x[′]_ _} = V (G[′]_ _−_ _H) is also_
independent. We can therefore extend our (ω 1)-colouring of H to an
_−_


-----

**Proof of Theorem 5.5.3. Applying induction on** _G_, we show that
_|_ _|_
_G = (V, E)_ the complement G of any perfect graph G = (V, E) is again perfect. For
_K_ _|G| = 1 this is trivial, so let |G| ⩾_ 2 for the induction step. Let K denote
_α_ the set of all vertex sets of complete subgraphs of G. Put α(G) =: α,
_A_ and let A be the set of all independent vertex sets A in G with |A| = α.
Every proper induced subgraph of G is the complement of a proper
induced subgraph of G, and is hence perfect by induction. For the perfection of G it thus suffices to prove χ(G) ⩽ _ω(G) (= α). To this end,_
we shall find a set K _[∈]_ _K such that K ∩_ _A ̸= ∅_ for all A _[∈]_ _A; then_

_ω(G_ _K) = α(G_ _K) < α = ω(G),_
_−_ _−_

so by the induction hypothesis

_χ(G) ⩽_ _χ(G −_ _K) + 1 = ω(G −_ _K) + 1 ⩽_ _ω(G)_

as desired.
Suppose there is no such K; thus, for every K ∈ _K there exists a_
_AK_ set AK ∈ _A with K ∩_ _AK = ∅. Let us replace in G every vertex x by a_
_Gx_ complete graph Gx of order

_k(x)_ _k(x) :=_ ��{ K ∈ _K | x ∈_ _AK }��_ _,_

joining all the vertices of Gx to all the vertices of Gy whenever x and y are

_G[′]_ adjacent in G. The graph G[′] thus obtained has vertex set [�]x∈V _[V][ (][G][x][),]_
and two vertices v _[∈]_ _Gx and w_ _[∈]_ _Gy are adjacent in G[′]_ if and only if
_x = y or xy_ _[∈]_ _E. Moreover, G[′]_ can be obtained by repeated vertex
expansion from the graph G [ { x _[∈]_ _V | k(x) > 0 } ]. Being an induced_
subgraph of G, this latter graph is perfect by assumption, so G[′] is perfect
by Lemma 5.5.4. In particular,

_χ(G[′]) ⩽_ _ω(G[′]) ._ (1)

In order to obtain a contradiction to (1), we now compute in turn the
actual values of ω(G[′]) and χ(G[′]). By construction of G[′], every maximal
complete subgraph of G[′] has the form G[′] [ [�]x∈X _[G][x][ ] for some][ X][ ∈]_ _[K][.]_

_X_ So there exists a set X _[∈]_ _K such that_


�
_ω(G[′]) =_ _k(x)_

_x∈X_

= ��{ (x, K) : x ∈ _X, K ∈_ _K, x ∈_ _AK }��_

�
= _|X ∩_ _AK|_

_K ∈K_


-----

the last inequality follows from the fact that |X ∩ _AK| ⩽_ 1 for all K
(since AK is independent but G [ X ] is complete), and |X ∩ _AX_ _| = 0 (by_
the choice of AX ). On the other hand,

�
_G[′]_ = _k(x)_
_|_ _|_

_x∈V_


= ��{ (x, K) : x ∈ _V, K ∈_ _K, x ∈_ _AK }��_

�
= _|AK|_

_K ∈K_


= _α ._
_|K| ·_

As α(G[′]) ⩽ _α by construction of G[′], this implies_

_|G[′]|_
_χ(G[′]) ⩾_ = |K| . (3)

_α(G[′])_ [⩾] _[|][G]α[′][|]_


Putting (2) and (3) together we obtain

_χ(G[′]) ⩾_ _|K| > |K| −_ 1 ⩾ _ω(G[′]),_

a contradiction to (1). 
Since the following characterization of perfection is symmetrical in
_G and G, it clearly implies Theorem 5.5.3. As our proof of Theorem_
5.5.5 will again be from first principles, we thus obtain a second and
independent proof of the perfect graph theorem.

**Theorem 5.5.5. (Lov´asz 1972)**
_A graph G is perfect if and only if_

_|H| ⩽_ _α(H) · ω(H)_ (∗)

_for all induced subgraphs H_ _G._
_⊆_

_Proof . Let us write V (G) =: V =: { v1, . . ., vn }, and put α := α(G)_ _V, vi, n_
and ω := ω(G). The necessity of ( ) is immediate: if G is perfect, then _α, ω_
_∗_
every induced subgraph H of G can be partitioned into at most ω(H)
colour classes each containing at most α(H) vertices, and ( ) follows.
_∗_
To prove sufficiency, we apply induction on n = _G_ . Assume that
_|_ _|_
every induced subgraph H of G satisfies ( ), and suppose that G is not
_∗_
perfect. By the induction hypothesis, every proper induced subgraph of
_G is perfect. Hence, every non-empty independent set U_ _V satisfies_
_⊆_


-----

Indeed, while the first equality is immediate from the perfection of G _U_,
_−_
the second is easy: ‘⩽’ is obvious, while χ(G − _U_ ) < ω would imply
_χ(G) ⩽_ _ω, so G would be perfect contrary to our assumption._
Let us apply (1) to a singleton U = _u_ and consider an ω-colouring
_{_ _}_
of G _u. Let K be the vertex set of any K[ω]_ in G. Clearly,
_−_

_if u /∈_ _K then K meets every colour class of G −_ _u;_ (2)

_if u ∈_ _K then K meets all but exactly one colour class of G −_ _u._ (3)

_A0_ Let A0 = { u1, . . ., uα } be an independent set in G of size α.
Let A1, . . ., Aω be the colour classes of an ω-colouring of G − _u1, let_
_Aω+1, . . ., A2ω be the colour classes of an ω-colouring of G −_ _u2, and_
_Ai_ so on; altogether, this gives us αω + 1 independent sets A0, A1, . . ., Aαω
in G. For each i = 0, . . ., αω, there exists by (1) a K _[ω]_ _⊆_ _G −_ _Ai; we_
_Ki_ denote its vertex set by Ki.
Note that if K is the vertex set of any K _[ω]_ in G, then

_K ∩_ _Ai = ∅_ _for exactly one i_ _[∈]_ _{ 0, . . ., αω + 1 }._ (4)

Indeed, if K ∩ _A0 = ∅_ then K ∩ _Ai ̸= ∅_ for all i ̸= 0, by definition of Ai
and (2). Similarly if K ∩ _A0 ̸= ∅, then |K ∩_ _A0| = 1, so K ∩_ _Ai = ∅_ for
exactly one i ̸= 0: apply (3) to the unique vertex u _[∈]_ _K ∩_ _A0, and (2)_
to all the other vertices u _[∈]_ _A0._
_J_ Let J be the real (αω + 1) (αω + 1) matrix with zero entries in
_×_
_A_ the main diagonal and all other entries 1. Let A be the real (αω +1) _n_
_×_
matrix whose rows are the incidence vectors of the subsets Ai ⊆ _V : if_
_ai1, . . ., ain denote the entries of the ith row of A, then aij = 1 if vj ∈_ _Ai,_
_B_ and aij = 0 otherwise. Similarly, let B denote the real n × (αω + 1)
matrix whose columns are the incidence vectors of the subsets Ki ⊆ _V ._
Now while |Ki ∩ _Ai| = 0 for all i by the choice of Ki, we have Ki ∩_ _Aj ̸= ∅_
and hence |Ki ∩ _Aj| = 1 whenever i ̸= j, by (4). Thus,_

_AB = J._

Since J is non-singular, this implies that A has rank αω + 1. In particular, n ⩾ _αω + 1, which contradicts (∗) for H := G._       
By definition, every induced subgraph of a perfect graph is again
perfect. The property of perfection can therefore be characterized by
forbidden induced subgraphs: there exists a set of imperfect graphs
_H_
such that any graph is perfect if and only if it has no induced subgraph
isomorphic to an element of . (For example, we may choose as the
_H_ _H_
set of all imperfect graphs with vertices in N.)
Naturally, it would be desirable to keep as small as possible. In
_H_


-----

need only contain two types of graph: the odd cycles of length ⩾ 5 and
their complements. (Neither of these are perfect—why?) Or, rephrased
slightly:

**Perfect Graph Conjecture. (Berge 1966)**
_A graph G is perfect if and only if neither G nor G contains an odd cycle_
_of length at least 5 as an induced subgraph._

Clearly, this conjecture implies the perfect graph theorem. In fact, that
theorem had also been conjectured by Berge: until its proof, it was
known as the ‘weak’ version of the perfect graph conjecture, the above
conjecture being the ‘strong’ version.
Graphs G such that neither G nor G contains an induced odd cycle
of length at least 5 have been called Berge graphs. Thus all perfect graphs
are Berge graphs, and the perfect graph conjecture claims that all Berge
graphs are perfect. This has been approximately verified by Pr¨omel &
Steger (1992), who proved that the proportion of perfect graphs to Berge
graphs on n vertices tends to 1 as n .
_→∞_

###### Exercises

1.[−] Show that the four colour theorem does indeed solve the map colouring
problem stated in the first sentence of the chapter. Conversely, does
the 4-colourability of every map imply the four colour theorem?

2.[−] Show that, for the map colouring problem above, it suffices to consider maps such that no point lies on the boundary of more than three
countries. How does this affect the proof of the four colour theorem?

3. Try to turn the proof of the five colour theorem into one of the four
colour theorem, as follows. Defining v and H as before, assume inductively that H has a 4-colouring; then proceed as before. Where does
the proof fail?

4. Calculate the chromatic number of a graph in terms of the chromatic
numbers of its blocks.

5.[−] Show that every graph G has a vertex ordering for which the greedy
algorithm uses only χ(G) colours.

6. For every n > 1, find a bipartite graph on 2n vertices, ordered in such
a way that the greedy algorithm uses n rather than 2 colours.

7. Consider the following approach to vertex colouring. First, find a maximal independent set of vertices and colour these with colour 1; then
find a maximal independent set of vertices in the remaining graph and
colour those 2, and so on. Compare this algorithm with the greedy


-----

8. Show that the bound of Proposition 5.2.2 is always at least as sharp as
that of Proposition 5.2.1.

9. Find a function f such that every graph of arboricity at least f (k) has
colouring number at least k, and a function g such that every graph of
colouring number at least g(k) has arboricity at least k, for all k _[∈]_ N.
(The arboricity of a graph is defined in Chapter 3.5.)

10.[−] A k-chromatic graph is called critically k-chromatic, or just critical,
if χ(G − _v) < k for every v_ _∈_ _V (G)._ Show that every k-chromatic
graph has a critical k-chromatic induced subgraph, and that any such
subgraph has minimum degree at least k − 1.

11. Determine the critical 3-chromatic graphs.

12.[+] Show that every critical k-chromatic graph is (k − 1) - edge-connected.

13. Given k _[∈]_ N, find a constant ck > 0 such that every graph G with
_|G| ⩾_ 3k and α(G) ⩽ _k contains a cycle of length at least ck |G|._

14.[−] Find a graph G for which Brooks’s theorem yields a significantly weaker
bound on χ(G) than Proposition 5.2.2.

15.[+] Show that, in order to prove Brooks’s theorem for a graph G = (V, E),
we may assume that κ(G) ⩾ 2 and ∆(G) ⩾ 3. Prove the theorem under
these assumptions, showing first the following two lemmas.

(i) Let v1, . . ., vn be an enumeration of V . If every vi (i < n) has
a neighbour vj with j > i, and if v1vn, v2vn _[∈]_ _E but v1v2 /∈_ _E,_
then the greedy algorithm uses at most ∆(G) colours.

(ii) If G is not complete and vn has maximum degree in G, then vn
has neighbours v1, v2 as in (i).

16. Given a graph G and k _[∈]_ N, let PG(k) denote the number of vertex
colourings V (G) →{ 1, . . ., k }. Show that PG is a polynomial in k of
degree n := |G|, in which the coefficient of k[n] is 1 and the coefficient
of k[n][−][1] is −∥G∥. (PG is called the chromatic polynomial of G.)

(Hint. Apply induction on ∥G∥. In the induction step, compare the
values of PG(k), PG−e(k) and PG/e(k).)

17.[+] Determine the class of all graphs G for which PG(k) = k (k − 1)[n][−][1]. (As
in the previous exercise, let n := |G|, and let PG denote the chromatic
polynomial of G.)

18. In the definition of k-constructible graphs, replace the axiom (ii) by

(ii)[′] _Every supergraph of a k-constructible graph is k-constructible;_

and the axiom (iii) by

(iii)[′] _If G is a graph with vertices x, y1, y2 such that y1y2_ _∈_ _E(G)_
_but xy1, xy2 /∈_ _E(G), and if both G + xy1 and G + xy2 are k-_
_constructible, then G is k-constructible._

Show that a graph is k-constructible with respect to this new definition


-----

19.[−] An n × n - matrix with entries from { 1, . . ., n } is called a Latin square
if every element of { 1, . . ., n } appears exactly once in each column and
exactly once in each row. Recast the problem of constructing Latin
squares as a colouring problem.

20. Without using Proposition 5.3.1, show that χ[′](G) = k for every kregular bipartite graph G.

21. Prove Proposition 5.3.1 from the statement of the previous exercise.

22.[+] For every k _[∈]_ N, construct a triangle-free k-chromatic graph.

23.[−] Without using Theorem 5.4.2, show that every plane graph is 6-listcolourable.

24. For every integer k, find a 2-chromatic graph whose choice number is
at least k.

25.[−] Find a general upper bound for ch[′](G) in terms of χ[′](G).

26. Compare the choice number of a graph with its colouring number:
which is greater? Can you prove the analogue of Theorem 5.4.1 for
the colouring number?

27.[+] Prove that the choice number of K2[r] [is][ r][.]

28. The total chromatic number χ[′′](G) of a graph G = (V, E) is the least
number of colours needed to colour the vertices and edges of G simultaneously so that any adjacent or incident elements of V ∪ _E are coloured_
differently. The total colouring conjecture says that χ[′′](G) ⩽ ∆(G)+2.
Bound the total chromatic number from above in terms of the listchromatic index, and use this bound to deduce a weakening of the
total colouring conjecture from the list colouring conjecture.

29.[−] Find a directed graph that has no kernel.

30.[+] Prove Richardson’s theorem: every directed graph without odd directed
cycles has a kernel.

31. Show that every bipartite planar graph is 3-list-colourable.
(Hint. Apply the previous exercise and Lemma 5.4.3.)

32.[−] Show that perfection is closed neither under edge deletion nor under
edge contraction.

33.[−] Deduce Theorem 5.5.5 from the perfect graph conjecture.

34. Use K¨onig’s Theorem 2.1.1 to show that the complement of any bipartite graph is perfect.

35. Using the results of this chapter, find a one-line proof of the following
theorem of K¨onig, the dual of Theorem 2.1.1: in any bipartite graph
without isolated vertices, the minimum number of edges meeting all
vertices equals the maximum number of independent vertices.

36. A graph is called a comparability graph if there exists a partial ordering
of its vertex set such that two vertices are adjacent if and only if they


-----

37. A graph G is called an interval graph if there exists a set { Iv | v _[∈]_ _V (G) }_
of real intervals such that Iu ∩ _Iv ̸= ∅_ if and only if uv _[∈]_ _E(G)._

(i) Show that every interval graph is chordal.

(ii) Show that the complement of any interval graph is a comparability graph.

(Conversely, a chordal graph is an interval graph if its complement is a
comparability graph; this is a theorem of Gilmore and Hoffman (1964).)

38. Show that χ(H) _[∈]_ _{ ω(H), ω(H) + 1 } for every line graph H._

39.[+] Characterize the graphs whose line graphs are perfect.

40. Show that a graph G is perfect if and only if every non-empty induced
subgraph H of G contains an independent set A ⊆ _V (H) such that_
_ω(H −_ _A) < ω(H)._

41.[+] Consider the graphs G for which every induced subgraph H has the
property that every maximal complete subgraph of H meets every maximal independent vertex set in H.

(i) Show that these graphs G are perfect.

(ii) Show that these graphs G are precisely the graphs not containing
an induced copy of P [3].

42.[+] Show that in every perfect graph G one can find a set A of independent
vertex sets and a set O of vertex sets of complete subgraphs such that
� _A = V (G) =_ [�] _O and every set in A meets every set in O._

(Hint. Lemma 5.5.4.)

43.[+] Let G be a perfect graph. As in the proof of Theorem 5.5.3, replace
every vertex x of G with a perfect graph Gx (not necessarily complete).
Show that the resulting graph G[′] is again perfect.

44. Let H1 and H2 be two sets of imperfect graphs, each minimal with
the property that a graph is perfect if and only if it has no induced
subgraph in Hi (i = 1, 2). Do H1 and H2 contain the same graphs, up
to isomorphism?

###### Notes

The authoritative reference work on all questions of graph colouring is T.R.
Jensen & B. Toft, Graph Coloring Problems, Wiley 1995. Starting with a brief
survey of the most important results and areas of research in the field, this
monograph gives a detailed account of over 200 open colouring problems, complete with extensive background surveys and references. Most of the remarks
below are discussed comprehensively in this book, and all the references for
this chapter can be found there.
The four colour problem, whether every map can be coloured with four
colours so that adjacent countries are shown in different colours, was raised by
a certain Francis Guthrie in 1852. He put the question to his brother Frederick,


-----

first brought to the attention of a wider public when Cayley presented it to
the London Mathematical Society in 1878. A year later, Kempe published
an incorrect proof, which was in 1890 modified by Heawood into a proof of
the five colour theorem. In 1880, Tait announced ‘further proofs’ of the four
colour conjecture, which never materialized; see the notes for Chapter 10.
The first generally accepted proof of the four colour theorem was published by Appel and Haken in 1977. The proof builds on ideas that can be
traced back as far as Kempe’s paper, and were developed largely by Birkhoff
and Heesch. Very roughly, the proof sets out first to show that every plane
triangulation must contain at least one of 1482 certain ‘unavoidable configurations’. In a second step, a computer is used to show that each of those
configurations is ‘reducible’, i.e., that any plane triangulation containing such
a configuration can be 4-coloured by piecing together 4-colourings of smaller
plane triangulations. Taken together, these two steps amount to an inductive
proof that all plane triangulations, and hence all planar graphs, can be 4coloured.
Appel & Haken’s proof has not been immune to criticism, not only because of their use of a computer. The authors responded with a 741 page
long algorithmic version of their proof, which addresses the various criticisms
and corrects a number of errors (e.g. by adding more configurations to the
‘unavoidable’ list): K. Appel & W. Haken, Every Planar Map is Four Col_orable, American Mathematical Society 1989. A much shorter proof, which_
is based on the same ideas (and, in particular, uses a computer in the same
way) but can be more readily verified both in its verbal and its computer part,
has been given by N. Robertson, D. Sanders, P.D. Seymour & R. Thomas, The
four-colour theorem, J. Combin. Theory B 70 (1997), 2–44.
A relatively short proof of Gr¨otzsch’s theorem was found by C. Thomassen,
Gr¨otzsch’s 3-color theorem and its counterparts for the torus and the projective
plane, J. Combin. Theory B 62 (1994), 268–279. Although not touched upon
in this chapter, colouring problems for graphs embedded in surfaces other
than the plane form a substantial and interesting part of colouring theory;
see B. Mohar & C. Thomassen, Graphs on Surfaces, Johns Hopkins University
Press, to appear.
The proof of Brooks’s theorem indicated in Exercise 15, where the greedy
algorithm is applied to a carefully chosen vertex ordering, is due to Lov´asz
(1973). Lov´asz (1968) was also the first to construct graphs of arbitrarily
large girth and chromatic number, graphs whose existence Erd˝os had proved
by probabilistic methods ten years earlier.
A. Urquhart, The graph constructions of Haj´os and Ore, J. Graph Theory
**26 (1997), 211–215, showed that not only do the graphs of chromatic number**
at least k each contain a k-constructible graph (as by Haj´os’s theorem); they
are in fact all themselves k-constructible. Algebraic tools for showing that
the chromatic number of a graph is large have been developed by Kleitman &
Lov´asz (1982), and by Alon & Tarsi (1992); see Alon’s paper cited below.
List colourings were first introduced in 1976 by Vizing. Among other
things, Vizing proved the list-colouring equivalent of Brooks’s theorem. Voigt
(1993) constructed a plane graph of order 238 that is not 4-choosable; thus,
Thomassen’s list version of the five colour theorem is best possible. A stim

-----

classical graph invariants (including a proof of Theorem 5.4.1) is given by
N. Alon, Restricted colorings of graphs, in (K. Walker, ed.) Surveys in Combi_natorics, LMS Lecture Notes 187, Cambridge University Press 1993. Both the_
list colouring conjecture and Galvin’s proof of the bipartite case are originally
stated for multigraphs. Kahn (1994) proved that the conjecture is asymptotically correct, as follows: given any ϵ > 0, every graph G with large enough
maximum degree satisfies ch[′](G) ⩽ (1 + ϵ)∆(G).
The total colouring conjecture was proposed around 1965 by Vizing and
by Behzad; see Jensen & Toft for details.
A gentle introduction to the basic facts about perfect graphs and their applications is given by M.C. Golumbic, Algorithmic Graph Theory and Perfect
_Graphs, Academic Press 1980. Our first proof of the perfect graph theorem_
follows L. Lov´asz’s survey on perfect graphs in (L.W. Beineke and R.J. Wilson,
eds.) Selected Topics in Graph Theory 2, Academic Press 1983. The theorem
was also proved independently, and only a little later, by Fulkerson. Our
second proof, the proof of Theorem 5.5.5, is due to G.S. Gasparian, Minimal
imperfect graphs: a simple approach, Combinatorica 16 (1996), 209–212. The
approximate proof of the perfect graph conjecture is due to H.J. Pr¨omel &
A. Steger, Almost all Berge graphs are perfect, Combinatorics, Probability
_and Computing 1 (1992), 53–79._


-----

# 6 Flows

Let us view a graph as a network: its edges carry some kind of flow—of
water, electricity, data or similar. How could we model this precisely?
For a start, we ought to know how much flow passes through each
edge e = xy, and in which direction. In our model, we could assign
a positive integer k to the pair (x, y) to express that a flow of k units
passes through e from x to y, or assign _k to (x, y) to express that k_
_−_
units of flow pass through e the other way, from y to x. For such an
assignment f : V [2] _→_ Z we would thus have f (x, y) = −f (y, x) whenever
_x and y are adjacent vertices of G._
Typically, a network will have only a few nodes where flow enters
or leaves the network; at all other nodes, the total amount of flow into
that node will equal the total amount of flow out of it. For our model
this means that, at most nodes x, the function f will satisfy Kirchhoff’s
_law_
_Kirchhoff’s_
� _f_ (x, y) = 0 . _law_

_y ∈N_ (x)

In this chapter, we call any map f : V [2] _→_ Z with the above two
properties a ‘flow’ on G. Sometimes, we shall replace Z with another
group, and as a rule we consider multigraphs rather than graphs.[1] As
it turns out, the theory of those ‘flows’ is not only useful as a model for
real flows: it blends so well with other parts of graph theory that some
deep and surprising connections become visible, connections particularly
with connectivity and colouring problems.

1 For consistency, we shall phrase some of our proposition for graphs only: those
whose proofs rely on assertions proved (for graphs) earlier in the book. However, all


-----

###### 6.1 Circulations

In the context of flows, we have to be able to speak about the ‘directions’
_G = (V, E)_ of an edge. Since, in a multigraph G = (V, E), an edge e = xy is not
identified uniquely by the pair (x, y) or (y, x), we define directed edges as
triples:

_E→_ _E→ := { (e, x, y) | e ∈_ _E; x, y ∈_ _V ; e = xy } ._

_direction_
Thus, an edge e = xy with x = y has the two directions (e, x, y) and
(e, x, y) _̸_
(e, y, x); a loop e = xx has only one direction, the triple (e, x, x). For
_←e_ given _→e = (e, x, y) ∈_ _E→, we set_ _←e := (e, y, x), and for an arbitrary set_
_F→_ _E→ of edge directions we put_
_⊆_

_F←_ _F← := {_ _←e |_ _→e ∈_ _F→ } ._

Note that _E→ itself is symmetrical:_ _E← =_ _E→. For X, Y_ _V and_ _F→_ _E→,_
_⊆_ _⊆_
define

_F→ (X, Y )_ _F→ (X, Y ) := { (e, x, y) ∈_ _F→ | x ∈_ _X; y ∈_ _Y ; x ̸= y },_

_F→ (x, Y )_ abbreviate _F→ ({ x }, Y ) to_ _F→ (x, Y ) etc., and write_

_F→ (x)_ _F→ (x) :=_ _F→ (x, V ) =_ _F→ ({ x }, { x }) ._

_X_ Here, as below, X denotes the complement V ∖ _X of a vertex set X ⊆_ _V._
Note that any loops at verticestions of _F→ (X, Y ) and_ _F→ (x)._ _x ∈_ _X ∩_ _Y are disregarded in the defini-_
0 Let H be an abelian semigroup,[2] written additively with zero 0.
_→_
_f_ Given vertex sets X, Y _V and a function f_ : _E_ _H, let_
_⊆_ _→_

� _→_
_f_ (X, Y ) _f_ (X, Y ) := _f_ (e) .

_⃗e ∈_ _E[⃗]_ (X,Y )

_f_ (x, Y ) Instead of f ( _x_ _, Y ) we again write f_ (x, Y ), etc.
_{_ _}_
_circulation_ From now on, we assume that H is a group. We call f a circulation
on G (with values in H), or an H-circulation, if f satisfies the following
two conditions:

(F1) f (e, x, y) = −f (e, y, x) for all (e, x, y) ∈ _E→ with x ̸= y;_

(F2) f (v, V ) = 0 for all v ∈ _V ._

2 This chapter contains no group theory. The only semigroups we ever consider
for H are the natural numbers, the integers, the reals, the cyclic groups Zk, and


-----

If f satisfies (F1), then

_f_ (X, X) = 0

for all X _V . If f satisfies (F2), then_
_⊆_


�
_f_ (X, V ) = _f_ (x, V ) = 0 .

_x∈X_

Together, these two basic observations imply that, in a circulation, the
net flow across any cut is zero:

[ 6.3.1 ]
**Proposition 6.1.1. If f is a circulation, then f** (X, X) = 0 for every [ 6.5.2 ]
_set X_ _V ._ [ 6.6.1 ]
_⊆_

_Proof . f_ (X, X) = f (X, V ) − _f_ (X, X) = 0 − 0 = 0. 
Since bridges form cuts by themselves, Proposition 6.1.1 implies
that circulations are always zero on bridges:

**Corollary 6.1.2. If f is a circulation and e = xy is a bridge in G, then**
_f_ (e, x, y) = 0. 
###### 6.2 Flows in networks

In this section we give a brief introduction to the kind of network flow
theory that is now a standard proof technique in areas such as matching
and connectivity. By way of example, we shall prove a classic result of
this theory, the so-called max-flow min-cut theorem of Ford and Fulkerson. This theorem alone implies Menger’s theorem without much difficulty (Exercise 3), which indicates some of the natural power lying in
this approach.
Consider the task of modelling a network with one source s and
one sink t, in which the amount of flow through a given link between
two nodes is subject to a certain capacity of that link. Our aim is to
determine the maximum net amount of flow through the network from
_s to t. Somehow, this will depend both on the structure of the network_
and on the various capacities of its connections—how exactly, is what
we wish to find out.
Let G = (V, E) be a multigraph, s, t _[∈]_ _V two fixed vertices, and_ _G = (V, E)_
_→_
_c:_ _E →_ N a map; we call c a capacity function on G, and the tuple _s, t, c, N_
_N := (G, s, t, c) a network_ . Note that c is defined independently for _network_
_→_
the two directions of an edge. A function f : _E →_ R is a flow in N if it _flow_


-----

(F1) f (e, x, y) = −f (e, y, x) for all (e, x, y) _[∈]_ _E→ with x ̸= y;_
(F2[′]) f (v, V ) = 0 for all v ∈ _V ∖_ _{ s, t };_
(F3) f ( _→e) ⩽_ _c(_ _→e) for all_ _→e ∈_ _E→._

_integral_ We call f integral if all its values are integers.

1
1

3

1 _t_

_s_ 2 3

1

0

2

_Fig. 6.2.1. A network flow in short notation: all values refer to_
the direction indicated (capacities are not shown)

_f_ Let f be a flow in N . If S ⊆ _V is such that s_ _[∈]_ _S and t_ _[∈]_ _S, we call_
_cut in N_ the pair (S, S) a cut in N, and c(S, S) the capacity of this cut.
_capacity_ Since f now has to satisfy only (F2[′]) rather than (F2), we no longer
have f (X, X) = 0 for all X _V (as in Proposition 6.1.1). However, the_
_⊆_
value is the same for all cuts:

**Proposition 6.2.1. Every cut (S, S) in N satisfies f** (S, S) = f (s, V ).

_Proof . As in the proof of Proposition 6.1.1, we have_

_f_ (S, S) = f (S, V ) _f_ (S, S)
_−_

�
= _f_ (v, V ) 0

_−_

(F1) _[f]_ [(][s, V][ ) +]

_v ∈S∖{ s }_

=
(F2[′]) _[f]_ [(][s, V][ )][ .]

                       
The common value of f (S, S) in Proposition 6.2.1 will be called the total
_total value_
_value of f and denoted by_ _f_ ;[3] the flow shown in Figure 6.2.1 has total
_|f_ _|_ _|_ _|_
value 3.
By (F3), we have

_|f_ _| = f_ (S, S) ⩽ _c(S, S)_

for every cut (S, S) in N . Hence the total value of a flow in N is never
larger than the smallest capacity of a cut. The following max-flow min_cut theorem states that this upper bound is always attained by some_
flow:

3 Thus, formally, |f _| may be negative. In practice, however, we can change the_


-----

**Theorem 6.2.2. (Ford & Fulkerson 1956)** _max-flow_
_In every network, the maximum total value of a flow equals the minimum_ _min-cut_
_capacity of a cut._ _theorem_

_Proof . Let N = (G, s, t, c) be a network, and G =: (V, E). We shall define_
a sequence f0, f1, f2, . . . of integral flows in N of strictly increasing total
value, i.e. with

_|f0| < |f1| < |f2| < . . ._

Clearly, the total value of an integral flow is again an integer, so in fact
_|fn+1| ⩾_ _|fn| + 1 for all n. Since all these numbers are bounded above_
by the capacity of any cut in N, our sequence will terminate with some
flow fn. Corresponding to this flow, we shall find a cut of capacity
_cn = |fn|. Since no flow can have a total value greater than cn, and no_
cut can have a capacity less than |fn|, this number is simultaneously the
maximum and the minimum referred to in the theorem.
For f0, we set f0(→e) := 0 for all _→e ∈_ _E→. Having defined an integral_
flow fn in N for some n _[∈]_ N, we denote by Sn the set of all vertices v _Sn_
such that G contains an s–v walk x0e0 . . . eℓ−1xℓ with

_fn(e→i) < c(e→i)_

for all i < ℓ; here, _e→i := (ei, xi, xi+1) (and, of course, x0 = s and xℓ_ = v).
If t _[∈]_ _Sn, let W = x0e0 . . . eℓ−1xℓ_ be the corresponding s–t walk; _W_
without loss of generality we may assume that W does not repeat any
vertices. Let
_ϵ := min { c(e→i) −_ _fn(e→i) | i < ℓ_ _} ._ _ϵ_

Then ϵ > 0, and since fn (like c) is integral by assumption, ϵ is an integer.
Let

_fn+1:_ _→e �→_  _ffnn((→→ee) +) − ϵϵ_ forfor _→→ee = =_ _ee→←ii,, i i = 0 = 0, . . ., ℓ, . . ., ℓ_ _−−_ 1;1;

 _fn(→e)_ for e /∈ _W_ .

Intuitively, fn+1 is obtained from fn by sending additional flow of value ϵ
along W from s to t (Fig. 6.2.2).

1
1

1

3

_W_ _t_

_s_ 2 3

1

0

2

_Fig. 6.2.2. An ‘augmenting path’ W with increment ϵ = 2, for_


-----

Clearly, fn+1 is again an integral flow in N . Let us compute its total
value |fn+1| = fn+1(s, V ). Since W contains the vertex s only once, _e→0_
is the only triple (e, x, y) with x = s and y ∈ _V whose f_ -value was
changed. This value, and hence that of fn+1(s, V ) was raised. Therefore
_|fn+1| > |fn| as desired._
If t /[∈] _Sn, then (Sn, Sn) is a cut in N_ . By (F3) for fn, and the
definition of Sn, we have

_fn(→e) = c(_ _→e)_

for all _→e ∈_ _E→(Sn, Sn), so_

_|fn| = fn(Sn, Sn) = c(Sn, Sn)_

as desired.       
Since the flow constructed in the proof of Theorem 6.2.2 is integral,
we have also proved the following:

**Corollary 6.2.3. In every network (with integral capacity function)**
_there exists an integral flow of maximum total value._       
###### 6.3 Group-valued flows

Let G = (V, E) be a multigraph and H an abelian group. If f and
_f + g_ _g are two H-circulations then, clearly, (f + g):_ _→e_ _f_ ( _→e) + g(→e) and_
_�→_
_−f_ _−f_ : _→e �→−f_ (→e) are again H-circulations. The H-circulations on G thus
form a group in a natural way.
_nowherezero_ A function f : _E→ →_ _H is nowhere zero if f_ (→e) ̸= 0 for all _→e ∈_ _E→. An_
_H-circulation that is nowhere zero is called an H-flow_ .[4] Note that the
_H-flow_ set of H-flows on G is not closed under addition: if two H-flows add
up to zero on some edge _→e, then their sum is no longer an H-flow. By_
Corollary 6.1.2, a graph with an H-flow cannot have a bridge.
For finite groups H, the number of H-flows on G—and, in particular,
their existence—surprisingly depends only on the order of H, not on H
itself:

**Theorem 6.3.1. (Tutte 1954)**
_For every multigraph G there exists a polynomial P such that, for any_
_finite abelian group H, the number of H-flows on G is P_ � _H_ 1�.
_|_ _| −_

4 This terminology seems simplest for our purposes but is not standard; see the


-----

_Proof . Let G =: (V, E); we use induction on m :=_ _E_ . Let us assume (6.1.1)
_|_ _|_
first that all the edges of G are loops. Then, given any finite abelian
groupwhen all edges are loops, there are H, every map _E→ →_ _H ∖_ _{ 0 }� is anH_ _H1�-flow onm such maps, and G. Since | PE→ :=| = | xEm|_

_|_ _| −_

is the polynomial sought.
Now assume there is an edge e0 = xy _[∈]_ _E that is not a loop; let_ _e0 = xy_
_e→0 := (e0, x, y) and E′ := E ∖_ _{ e0 }. We consider the multigraphs_ _E[′]_

_G1 := G −_ _e0_ and _G2 := G/e0 ._

By the induction hypothesis, there are polynomials Pi for i = 1, 2 such _P1, P2_
that, for any finite abelian group H and k := _H_ 1, the number of _k_
_|_ _| −_
_H-flows on Gi is Pi(k). We shall prove that the number of H-flows on_
_G equals P2(k) −_ _P1(k); then P := P2 −_ _P1 is the desired polynomial._
Let H be given, and denote the set of all H-flows on G by F . We _H_
are trying to show that _F_

_|F_ _| = P2(k) −_ _P1(k) ._ (1)

The H-flows on G1 are precisely the restrictions to _E→[′]_ of those H-circu
lations on G that are zero on e0 but nowhere else. Let us denote the set
of these circulations on G by F1; then _F1_

_P1(k) = |F1| ._

Our aim is to show that, likewise, the H-flows on G2 correspond bijectively to those H-circulations on G that are nowhere zero except possibly
on e0. The set F2 of those circulations on G then satisfies _F2_

_P2(k) = |F2|,_

and F2 is the disjoint union of F1 and F . This will prove (1), and hence
the theorem.

_E[′](x, y)_

_x_ _e0_ _y_ _v0_

_G_ _G2_

_Fig. 6.3.1. Contracting the edge e0_

In G2, let v0 := ve0 be the vertex contracted from e0 (Fig. 6.3.1; _v0_


-----

and the set of H-flows on G2. Given f, let g be the restriction of f to
_E→[′]_ ∖ _E→[′](y, x). (As the x–y edges e_ _[∈]_ _E[′]_ become loops in G2, they have on
ly the one direction (e, v0, v0) there; as its g-value, we choose f (e, x, y).)
Then g is indeed an H-flow on G2; note that (F2) holds at v0 by Proposition 6.1.1 for G, with X := _x, y_ .
_{_ _}_
It remains to show that the map f _g is a bijection. If we are given_
_�→_
already determined asan H-flow g on G2 and try to find an f ( _→e) = g(→e) for all f_ _[∈]→eF ∈2 withE→[′]_ ∖ fE→ �→[′](y, xg); by (F1), we, then f ( _→e) is_

further have f ( _→e) = −f_ (←e) for all _→e ∈_ _E→[′](y, x). Thus our map f �→_ _g is_
bijective if and only if for given g there is always a unique way to define
the remaining values of f (e→0) and f (e←0) so that f satisfies (F1) in e0 and
(F2) in x and y.
_V_ _[′]_ This is indeed the case. Let V _[′]_ := V ∖ _{ x, y }. As g satisfies (F2),_
the f -values fixed already are such that

_f_ (x, V _[′]) + f_ (y, V _[′]) = g(v0, V_ _[′]) = 0 ._ (2)


With

(F2) for f requires


� _→_ � � �
_h :=_ _f_ (e) = _g(e, v0, v0)_ _,_

_⃗e ∈_ _E→[′]_ (x,y) _e ∈E[′](x,y)_


and

so we have to set


0 = f (x, V ) = f (e→0) + h + f (x, V ′)

0 = f (y, V ) = f (e←0) − _h + f_ (y, V ′),


_f_ (e→0) := −f (x, V ′) − _h_ and _f_ (e←0) := −f (y, V ′) + h .

Then f (e→0) + f (e←0) = 0 by (2), so f also satisfies (F1) in e0.      
_flow_
The polynomial P of Theorem 6.3.1 is known as the flow polynomial
_polynomial_
of G.

[ 6.4.5 ] **Corollary 6.3.2. If H and H** _[′]_ _are two finite abelian groups of equal_
_order, then G has an H-flow if and only if G has an H_ _[′]-flow._      
Corollary 6.3.2 has fundamental implications for the theory of algebraic flows: it indicates that crucial difficulties in existence proofs of
_H-flows are unlikely to be of a group-theoretic nature. On the other_
hand, being able to choose a convenient group can be quite helpful; we


-----

Let k ⩾ 1 be an integer and G = (V, E) a multigraph. A Z-flow f _k_
on G such that 0 < |f (→e)| < k for all _→e ∈_ _E→ is called a k-flow_ . Clearly, _k-flow_
any k-flow is also an ℓ-flow for all ℓ> k. Thus, we may ask which is
the least integer k such that G admits a k-flow—assuming that such a k
_flow_
exists. We call this least k the flow number of G and denote it by ϕ(G);
_number_
if G has no k-flow for any k, we put ϕ(G) := . _ϕ(G)_
_∞_
The task of determining flow numbers quickly leads to some of the
deepest open problems in graph theory. We shall consider these later
in the chapter. First, however, let us see how k-flows are related to the
more general concept of H-flows.
There is an intimate connection between k-flows and Zk-flows. Let
_σk denote the natural homomorphism i �→_ _i from Z to Zk. By compo-_ _σk_
sition with σk, every k-flow defines a Zk-flow. As the following theorem
shows, the converse holds too: from every Zk-flow on G we can construct
a k-flow on G. In view of Corollary 6.3.2, this means that the general
question about the existence of H-flows for arbitrary groups H reduces
to the corresponding question for k-flows.

**Theorem 6.3.3. (Tutte 1950)** [ 6.4.1 ]

[ 6.4.2 ]

_A multigraph admits a k-flow if and only if it admits a Zk-flow._ [ 6.4.3 ]

[ 6.4.5 ]
_Proof . Let g be a Zk-flow on a multigraph G = (V, E); we construct a_
_k-flow f on G. We may assume without loss of generality that G has_ _g_
_→_
no loops. Let|f (→e)| < k for all F be the set of all functions→e ∈ _E→, and σk ◦_ _f = g; note that, like f_ : _E →_ Z that satisfy (F1), g, any f _[∈]_ _F is_ _F_
nowhere zero.
Let us show first that F = . Since we can express every value
_̸_ _∅_
_fg(:_ _→eE→) → ∈_ ZZk such that as i with | |fi|( < k→e)| < k and then put for all _→e ∈ fE→( and→e) := σ ik, there is clearly a map ◦_ _f = g. For each edge_
_e ∈_ _E, let us choose one of its two directions and denote this by_ _→e. We_
may then define f _[′]:_ _E→ →_ Z by setting f _[′](→e) := f_ ( _→e) and f ′(←e) := −f_ (→e)
for every e ∈ _E. Then f_ _[′]_ is a function satisfying (F1) and with values in
the desired range; it remains to show that σk ◦ _f_ _[′]_ and g agree not only
on the chosen directions _→e but also on their inverses_ _←e. Since σk is a_
homomorphism, this is indeed so:

(σk ◦ _f_ _[′])(←e) = σk(−f_ (→e)) = −(σk ◦ _f_ )(→e) = −g(→e) = g( _←e) ._

Hence f _[′ ∈]_ _F_, so F is indeed non-empty.
Our aim is to find an f _[∈]_ _F that satisfies Kirchhoff’s law (F2), and_
is thus a k-flow. As a candidate, let us consider an f _[∈]_ _F for which the_ _f_


-----

�

_K_ _K(f_ ) := _f_ (x, V )

_|_ _|_
_x∈V_

of all deviations from Kirchhoff’s law is least possible. We shall prove

that K(f ) = 0; then, clearly, f (x, V ) = 0 for every x, as desired.
Suppose K(f ) ̸= 0. Since f satisfies (F1), and hence [�]x∈V _[f]_ [(][x, V][ ) =]
_x_ _f_ (V, V ) = 0, there exists a vertex x with

_f_ (x, V ) > 0 . (1)

_X_ Let X ⊆ _V be the set of all vertices x[′]_ for which G contains a walk
_x0e0 . . . eℓ−1xℓ_ from x to x[′] such that f (ei, xi, xi+1) > 0 for all i < ℓ;
_X_ _[′]_ furthermore, let X _[′]_ := X ∖ _{ x }._
We first show that X _[′]_ contains a vertex x[′] with f (x[′], V ) < 0. By
definition of X, we have f (e, x[′], y) ⩽ 0 for all edges e = x[′]y such that
_x[′ ∈]_ _X and y_ _[∈]_ _X. In particular, this holds for x[′]_ = x. Thus, (1) implies
_f_ (x, X _[′]) > 0. Then f_ (X _[′], x) < 0 by (F1), as well as f_ (X _[′], X_ _[′]) = 0._
Therefore

�

_f_ (x[′], V ) = f (X _[′], V ) = f_ (X _[′], X) + f_ (X _[′], x) + f_ (X _[′], X_ _[′]) < 0,_

_x[′ ]∈X_ _[′]_

_x[′]_ so some x[′ ∈] _X_ _[′]_ must indeed satisfy

_f_ (x[′], V ) < 0 . (2)

_W_ As x[′ ∈] _X, there is an x–x[′]_ walk W = x0e0 . . . eℓ−1xℓ such that
_f_ (ei, xi, xi+1) > 0 for all i < ℓ. We now modify f by sending some flow
_→_
_f_ _[′]_ back along W, letting f _[′]:_ _E →_ Z be given by


_f_ ( _→e) −_ _k_ for _→e = (ei, xi, xi+1), i = 0, . . ., ℓ_ _−_ 1;
_f_ ( _→e) + k_ for _→e = (ei, xi+1, xi), i = 0, . . ., ℓ_ _−_ 1;
_f_ ( _→e)_ for e /[∈] _W_ .


_f_ _[′]:_ _→e �→_








By definition of W, we have |f _[′](→e)| < k for all_ _→e ∈_ _E→. Hence f_ _[′], like f_,
lies in F .
How does the modification of f affect K? At all inner vertices v
of W, as well as outside W, the deviation from Kirchhoff’s law remains
unchanged:

_f_ _[′](v, V ) = f_ (v, V ) for all v _[∈]_ _V ∖_ _{ x, x[′]_ _}._ (3)

For x and x[′], on the other hand, we have


-----

Since g is a Zk-flow and hence

_σk(f_ (x, V )) = g(x, V ) = 0 _[∈]_ Zk
and

_σk(f_ (x[′], V )) = g(x[′], V ) = 0 _[∈]_ Zk,

_f_ (x, V ) and f (x[′], V ) are both multiples of k. Thus f (x, V ) ⩾ _k and_
_f_ (x[′], V ) ⩽ _−k, by (1) and (2). But then (4) implies that_

_|f_ _[′](x, V )| < |f_ (x, V )| and _|f_ _[′](x[′], V )| < |f_ (x[′], V )| .

Together with (3), this gives K(f _[′]) < K(f_ ), a contradiction to the choice
of f .
Therefore K(f ) = 0 as claimed, and f is indeed a k-flow.   
Since the sum of two Zk-circulations is always another Zk-circulation,
Zk-flows are often easier to construct (by summing over suitable partial
flows) than k-flows. In this way, Theorem 6.3.3 may be of considerable
help in determining whether or not some given graph has a k-flow. In
the following sections we shall meet a number of examples for this.

###### 6.4 k-Flows for small k

Trivially, a graph has a 1-flow (the empty set) if and only if it has no
edges. In this section we collect a few simple examples of sufficient
conditions under which a graph has a 2-, 3- or 4-flow. More examples
can be found in the exercises.

**Proposition 6.4.1. A graph has a 2-flow if and only if all its degrees** [ 6.6.1 ]
_are even._

_Proof . By Theorem 6.3.3, a graph G = (V, E) has a 2-flow if and only if_ (6.3.3)
it has a Z2-flow, i.e. if and only if the constant map _E→ →_ Z2 with value 1
satisfies (F2). This is the case if and only if all degrees are even. 
_even_
For the remainder of this chapter, let us call a graph even if all its vertex _graph_
degrees are even.

**Proposition 6.4.2. A cubic graph has a 3-flow if and only if it is bi-**


-----

(1.6.1)
_Proof ._ Let G = (V, E) be a cubic graph. Let us assume first that
(6.3.3)
_G has a 3-flow, and hence also a Z3-flow f_ . We show that any cycle
_C = x0 . . . xℓx0 in G has even length (cf. Proposition 1.6.1). Consider_
two consecutive edges on C, say ei−1 := xi−1xi and ei := xixi+1. If f
assigned the same value to these edges in the direction of the forward
orientation of C, i.e. if f (ei−1, xi−1, xi) = f (ei, xi, xi+1), then f could
not satisfy (F2) at xi for any non-zero value of the third edge at xi.
Therefore f assigns the values 1 and 2 to the edges of C alternately, and
in particular C has even length.
Conversely, let G be bipartite, with vertex bipartition _X, Y_ .
Since G is cubic, the map _E→ →_ Z3 defined by f (e, x, y) := 1 and { _}_
_f_ (e, y, x) := 2 for all edges e = xy with x _[∈]_ _X and y_ _[∈]_ _Y is a Z3-_
flow on G. By Theorem 6.3.3, then, G has a 3-flow.      
What are the flow numbers of the complete graphs K _[n]? For odd_
_n > 1, we have ϕ(K_ _[n]) = 2 by Proposition 6.4.1. Moreover, ϕ(K_ [2]) =,
_∞_
and ϕ(K [4]) = 4; this is easy to see directly (and it follows from Propositions 6.4.2 and 6.4.5). Interestingly, K [4] is the only complete graph with
flow number 4:

**Proposition 6.4.3. For all even n > 4, ϕ(K** _[n]) = 3._

(6.3.3) _Proof . Proposition 6.4.1 implies that ϕ(K_ _[n]) ⩾_ 3 for even n. We show,
by induction on n, that every G = K _[n]_ with even n > 4 has a 3-flow.
For the induction start, let n = 6. Then G is the edge-disjoint union
of three graphs G1, G2, G3, with G1, G2 = K [3] and G3 = K3,3. Clearly
_G1 and G2 each have a 2-flow, while G3 has a 3-flow by Proposition 6.4.2._
The union of all these flows is a 3-flow on G.
Now let n > 6, and assume the assertion holds for n 2. Clearly, G is
_−_
the edge-disjoint union of a K _[n][−][2]_ and a graph G[′] = (V _[′], E[′]) with G[′]_ =
_K_ _[n][−][2]_ _K_ [2]. The K _[n][−][2]_ has a 3-flow by induction. By Theorem 6.3.3, it
_∗_
thus suffices to find a Z3-flow on G[′]. For every vertex z of the K _[n][−][2]_ _⊆_ _G[′],_
of thelet fz be a K [2] in Z G3-flow on the triangle[′]. Let f : _E→[′]_ _→_ Z3 be the sum of these flows. Clearly, zxyz ⊆ _G[′], where e = xy is the edge f is_

nowhere zero, except possibly in (e, x, y) and (e, y, x). If f (e, x, y) = 0,
_̸_
then f is the desired Z3-flow on G[′]. If f (e, x, y) = 0, then f + fz (for
any z) is a Z3-flow on G[′].       
**Proposition 6.4.4. Every 4-edge-connected graph has a 4-flow.**

(3.5.2) _Proof . Let G be a 4-edge-connected graph. By Corollary 3.5.2, G has_
two edge-disjoint spanning trees Ti, i = 1, 2. For each edge e /∈ _Ti, let_
_f1,e, f2,e_ _Ci,e be the unique cycle in Ti + e, and let fi,e be a Z4-flow of value i_
around Ci,e—more precisely: a Z4-circulation on G with values i and −i


-----

Let f1 := [�]e/∈T1 _[f][1][,e][. Since each][ e /][∈]_ _[T][1]_ [lies on only one cycle][ C][1][,e][′] _f1_
(namely, for e = e[′]), f1 takes only the values 1 and −1 (= 3) outside T1.
Let

_F := { e ∈_ _E(T1) | f1(e) = 0 }_

and f2 := [�]e∈F _[f][2][,e][. As above,][ f][2][(][e][) = 2 =][ −][2 for all][ e][ ∈]_ _[F]_ [. Now] _f2_
_f := f1 + f2 is the sum of Z4-circulations, and hence itself a Z4-circula-_ _f_
tion. Moreover, f is nowhere zero: on edges in F it takes the value 2, on
edges of T1 _F it agrees with f1 (and is hence non-zero by the choice_
_−_
of F ), and on all edges outside T1 it takes one of the values 1 or 3. Hence,
_f is a Z4-flow on G, and the assertion follows by Theorem 6.3.3._ 
The following proposition describes the graphs with a 4-flow in terms
of those with a 2-flow:

**Proposition 6.4.5.**

(i) A graph has a 4-flow if and only if it is the union of two even
_subgraphs._

(ii) A cubic graph has a 4-flow if and only if it is 3-edge-colourable.

(6.3.2)
_Proof . Let Z[2]2_ [=][ Z][2] _[×]_ [Z][2] [be the Klein four-group. (Thus, the elements of] (6.3.3)
Z[2]2 [are the pairs (][a, b][) with][ a, b][ ∈] [Z][2][, and (][a, b][)+(][a][′][, b][′][) = (][a] [+] _[a][′][, b]_ [+] _[b][′][).)]_
By Corollary 6.3.2 and Theorem 6.3.3, a graph has a 4-flow if and only
if it has a Z[2]2 [-flow.]
(i) now follows directly from Proposition 6.4.1.
(ii) Let G = (V, E) be a cubic graph. We assume first that G has a
Zall[2]2 a[-flow] ∈ Z[ f][2]2[, we have][, and define an edge colouring][ f] [(]→e) = f (←e) for every[ E][ →]→e ∈[Z]E→2[2] ; let us colour the edge[∖] _[{][ 0][ }][. As][ a][ =][ −][a][ for]_
_e with this colour f_ ( _→e). Now if two edges with a common end v had_
the same colour, then these two values of f would sum to zero; by (F2),
_f would then assign zero to the third edge at v. As this contradicts the_
definition of f, our edge colouring is correct.
Conversely, since the three non-zero elements of Z[2]2 [sum to zero,]
every 3-edge-colouringf ( _→e) = f_ ( _←e) = c(e) for all c: E →→e ∈Z[2]2E→[∖]._ _[{][ 0][ }][ defines a][ Z]2[2]_ [-flow on][ G][ by letting]□

**Corollary 6.4.6. Every cubic 3-edge-colourable graph is bridgeless.**

                    

-----

###### 6.5 Flow-colouring duality

In this section we shall see a surprising connection between flows and
colouring: every k-flow on a plane multigraph gives rise to a k-vertexcolouring of its dual, and vice versa. In this way, the investigation of
_k-flows appears as a natural generalization of the familiar map colouring_
problems in the plane.
_G = (V, E)_ Let G = (V, E) and G[∗] = (V _[∗], E[∗]) be dual plane multigraphs. For_
_G[∗]_ simplicity, let us assume that G and G[∗] have neither bridges nor loops
and are non-trivial. For edge sets F _E, let us write_
_⊆_

_F_ _[∗]_ _F_ _[∗]_ := { e[∗∈] _E[∗]_ _| e_ _[∈]_ _F } ._

Conversely, if a subset of E[∗] is given, we shall usually write it immediately in the form F _[∗], and thus let F ⊆_ _E be defined implicitly via the_
bijection e �→ _e[∗]._
Suppose we are given a circulation g on G[∗]: how can we employ the
duality between G and G[∗] to derive from g some information about G?
The most general property of all circulations is Proposition 6.1.1, which
says that g(X, X) = 0 for all X ⊆ _V_ _[∗]. By Proposition 4.6.1, the minimal_
cuts E[∗](X, X) in G[∗] correspond precisely to the cycles in G. Thus if we
take the composition f of the maps e �→ _e[∗]_ and g, and sum its values
over the edges of a cycle in G, then this sum should again be zero.
Of course, there is still a technical hitch: since g takes its arguments
not in E[∗] but in _E→[∗], we cannot simply define f as above: we first have_
to refine the bijection→e _∈_ _E→ canonically one of the two directions of e �→_ _e[∗]_ into one from _E→ to_ _E e→[∗][∗], i.e. assign to every._ This will be the
purpose of our first lemma. After that, we shall show that f does indeed
sum to zero along any cycle in G.
If C = v0 . . . vℓ−1v0 is a cycle with edges ei = vivi+1 (and vℓ := v0),
we shall call

_C→_ _C→ := { (ei, vi, vi+1) | i < ℓ_ _}_

_cycle with_ _→_
a cycle with orientation. Note that this definition of _C depends on the_
_orientation_
vertex enumeration chosen to denote C: every cycle has two orientations.
Conversely, of course, C can be reconstructed from the set _C→. In practice,_
we shall therefore speak about C freely even when, formally, only _C→ has_
been defined.

**Lemma 6.5.1. There exists a bijection** _[∗]:_ _→e �→_ _→e ∗_ _from_ _E→ to_ _E→[∗]_ _with_
_the following properties._
(i) The underlying edge of _→e ∗_ _is always e∗, i.e._ _→e ∗_ _is one of the two_
_directions_ _e→[∗],_ _e←[∗]_ _of e[∗]._
(ii) IfF C[∗] = ⊆ EG[∗]( is a cycle,X, X), then there exists an orientation F := E(C), and if X ⊆ _V_ _[∗]C→is such that of C with_


-----

The proof of Lemma 6.5.1 is not entirely trivial: it is based on the
so-called orientability of the plane, and we cannot give it here. Still,
the assertion of the lemma is intuitively plausible. Indeed if we define for e = vw and e[∗] = xy the assignment (e, v, w) �→ (e, v, w)[∗∈]
_{ (e[∗], x, y), (e[∗], y, x) } simply by turning e and its ends clockwise onto e[∗]_

(Fig. 6.5.1), then the resulting map _→e �→_ _→e ∗_ satisfies the two assertions
of the lemma.

###### X

_C→_ **_X_**

_Fig. 6.5.1. Oriented cycle-cut duality_

_→_ _→_
Given an abelian group H, let f : _E_ _H and g:_ _E[∗]_ _H be two maps_ _f, g_
_→_ _→_
such that
_f_ (→e) = g(→e ∗)

for all _→e ∈_ _E→. For_ _F→ ⊆_ _E→, we set_


_→_ � _→_
_f_ (F ) := _f_ (e) .

_⃗e ∈_ _F[⃗]_

**Lemma 6.5.2.**
(i) The map g satisfies (F1) if and only if f does.
(ii) The map g is a circulation on G[∗] _if and only if f satisfies (F1)_
_and f_ (C→) = 0 for every cycle _C→ with orientation._


_f_ (C→ ) etc.


(4.6.1)
_Proof ._ Assertion (i) follows from Lemma 6.5.1 (i) and the fact that
(6.1.1)
_→e �→_ _→e ∗_ is bijective.
For the forward implication of (ii), let us assume that g is a circulation on G[∗], and consider a cycle C ⊆ _G with some given orientation._
Let F := E(C). By Proposition 4.6.1, F _[∗]_ is a minimal cut in G[∗], i.e.
_F_ _[∗]_ = E[∗](X, X) for some suitable X ⊆ _V_ _[∗]. By definition of f and g,_
Lemma 6.5.1 (ii) and Proposition 6.1.1 give

_→_ � _→_ � _→_
_f_ (C ) = _f_ (e) = _g(d) = g(X, X) = 0_

_⃗e ∈_ _C[⃗]_ _⃗d ∈E→[∗](X,X)_


-----

the corresponding value for our given orientation of C must be zero.
For the backward implication it suffices by (i) to show that g satisfies (F2), i.e. that g(x, V _[∗]) = 0 for every x_ _[∈]_ _V_ _[∗]. We shall prove that_
_g(x, V (B)) = 0 for every block B of G[∗]_ containing x; since every edge
of G[∗] at x lies in exactly one such block, this will imply g(x, V _[∗]) = 0._
_B_ So let x _[∈]_ _V_ _[∗]_ be given, and let B be any block of G[∗] containing x. Since G[∗] is a non-trivial plane dual, and hence connected, we
_F_ _[∗], F_ have B − _x ̸= ∅. Let F_ _[∗]_ be the set of all edges of B at x (Fig. 6.5.2),


###### X


_C_


_Fig. 6.5.2. The cut F_ _[∗]_ in G[∗]

_X_ and let X be the vertex set of the component of G[∗] _−_ _F_ _[∗]_ containing x.
Then = V (B _x)_ _X, by the maximality of B as a cutvertex-free_
_∅̸_ _−_ _⊆_
subgraph. Hence
_F_ _[∗]_ = E[∗](X, X) (1)

by definition of X, i.e. F _[∗]_ is a cut in G[∗]. As a dual, G[∗] is connected,
so G[∗][ X ] too is connected. Indeed, every vertex of X is linked to x by
a path P ⊆ _G[∗]_ whose last edge lies in F _[∗]. Then P −_ _x is a path in_
_G[∗][ X ] meeting B. Since x does not separate B, this shows that G[∗][ X ]_
is connected.
Thus, X and X are both connected in G[∗], so F _[∗]_ is even a minimal
_C_ cut inProposition 4.6.1. By Lemma 6.5.1 (ii), G[∗]. Let C ⊆ _G be the cycle with C has an orientation E(C) = F that exists byC→ such that_
_{_ _→e ∗_ _|_ _→e ∈_ _C→ } =_ _E→[∗](X, X). By (1), however,_ _E→[∗](X, X) =_ _E→[∗](x, V (B)),_
so
_g(x, V (B)) = g(X, X) = f_ (C→) = 0

by definition of f and g.       
With the help of Lemma 6.5.2, we can now prove our colouring-flow
duality theorem for plane multigraphs. If P = v0 . . . vℓ is a path with
edges ei = vivi+1 (i < ℓ), we set (depending on our vertex enumeration
of P )

_P→_ _P→ := { (ei, vi, vi+1) | i < ℓ_ _}_

_v0 →_ _vℓ_ _→_ A _→_


-----

**Theorem 6.5.3. (Tutte 1954)**
_For every dual pair G, G[∗]_ _of plane multigraphs,_

_χ(G) = ϕ(G[∗]) ._

_Proof ._ Let G =: (V, E) and G[∗] =: (V _[∗], E[∗])._ For |G| ∈ _{ 1, 2 } the_ (1.5.5)
assertion is easily checked; we shall assume that |G| ⩾ 3, and apply _V, E_
induction on the number of bridges in G. If e _[∈]_ _G is a bridge then e[∗]_ _V_ _[∗], E[∗]_
is a loop, and G[∗] _e[∗]_ is a plane dual of G/e (why?). Hence, by the
_−_
induction hypothesis,

_χ(G) = χ(G/e) = ϕ(G[∗]_ _−_ _e[∗]) = ϕ(G[∗]) ;_

for the first and the last equality we use that, by |G| ⩾ 3, e is not the
only edge of G.
So all that remains to be checked is the induction start: let us
assume that G has no bridge. If G has a loop, then G[∗] has a bridge,
and χ(G) = ∞ = ϕ(G[∗]) by convention. So we may also assume that G
has no loop. Then χ(G) is finite; we shall prove for given k ⩾ 2 that G _k_
is k-colourable if and only if G[∗] has a k-flow. As G—and hence G[∗]—
has neither loops nor bridges, we may apply Lemmas 6.5.1 and 6.5.2
to G and G[∗]. Let _→e �→_ _→e ∗_ be the bijection between _E→ and_ _E→[∗]_ from
Lemma 6.5.1.
We first assume that G[∗] has a k-flow. Then G[∗] also has a Zk-flow g. _g_
As before, let f : _E→ →_ Zk be defined by f (→e) := g(→e ∗). We shall use f to _f_
define a vertex colouring c: V → Zk of G.
Let T be a normal spanning tree of G, with root r, say. Put c(r) := 0.
For every other vertex v _[∈]_ _V let c(v) := f_ (P→ ), where _P→ is the r →_ _v_
path in T . To check that this is a proper colouring, consider an edge
_e = vw_ _[∈]_ _E. As T is normal, we may assume that v < w in the tree_
order of T . If e is an edge of T then c(w) _c(v) = f_ (e, v, w) by definition
_−_
ofP→ denote the c, so c(v) ̸= v c(ww) since path in g (and hence T . Then _f_ ) is nowhere zero. If e /[∈] _T_, let
_→_

_c(w)_ _c(v) = f_ (P→ ) = _f_ (e, w, v) = 0
_−_ _−_ _̸_

by Lemma 6.5.2 (ii).
Conversely, we now assume that G has a k-colouring c. Let us define _c_
_f_ : _E→ →_ Z by

_f_ (e, v, w) := c(w) _c(v),_ _f_
_−_

and g: _E→[∗]_ _→_ Z by g(→e ∗) := f ( _→e). Clearly, f satisfies (F1) and takes_ _g_
values in 1, . . ., (k 1), so by Lemma 6.5.2 (i) the same holds
for g. By definition of { ± _±_ _f −, we further have }_ _f_ (C→) = 0 for every cycle _C→_


-----

###### 6.6 Tutte’s flow conjectures

How can we determine the flow number of a graph? Indeed, does every
(bridgeless) graph have a flow number, a k-flow for some k? Can flow
numbers, like chromatic numbers, become arbitrarily large? Can we
characterize the graphs admitting a k-flow, for given k?
Of these four questions, we shall answer the second and third in this
section: we prove that every bridgeless graph has a 6-flow. In particular,
a graph has a flow number if and only if it has no bridge. The question asking for a characterization of the graphs with a k-flow remains
interesting for k = 3, 4, 5. Partial answers are suggested by the following
three conjectures of Tutte, who initiated algebraic flow theory.
The oldest and best known of the Tutte conjectures is his 5-flow
_conjecture:_

**Five-Flow Conjecture. (Tutte 1954)**
_Every bridgeless multigraph has a 5-flow._

Which graphs have a 4-flow? By Proposition 6.4.4, the 4-edgeconnected graphs are among them. The Petersen graph (Fig. 6.6.1), on
the other hand, is an example of a bridgeless graph without a 4-flow:
since it is cubic but not 3-edge-colourable (Ex. 19, Ch. 5), it cannot have
a 4-flow by Proposition 6.4.5 (ii).

_Fig. 6.6.1. The Petersen graph_

Tutte’s 4-flow conjecture states that the Petersen graph must be
present in every graph without a 4-flow:

**Four-Flow Conjecture. (Tutte 1966)**
_Every bridgeless multigraph not containing the Petersen graph as a mi-_
_nor has a 4-flow._

By Proposition 1.7.2, we may replace the word ‘minor’ in the 4-flow


-----

Even if true, the 4-flow conjecture will not be best possible: a K [11],
for example, contains the Petersen graph as a minor but has a 4-flow,
even a 2-flow. The conjecture appears more natural for sparser graphs,
and indeed the cubic graphs form an important special case. (See the
notes.)
A cubic bridgeless graph or multigraph without a 4-flow (equivalently, without a 3-edge-colouring) is called a snark . The 4-flow conjecture _snark_
for cubic graphs says that every snark contains the Petersen graph as
a minor; in this sense, the Petersen graph has thus been shown to be
the smallest snark. Snarks form the hard core both of the four colour
theorem and of the 5-flow conjecture: the four colour theorem is equivalent to the assertion that no snark is planar (exercise), and it is not
difficult to reduce the 5-flow conjecture to the case of snarks.[5] However,
although the snarks form a very special class of graphs, none of the
problems mentioned seems to become much easier by this reduction.[6]

**Three-Flow Conjecture. (Tutte 1972)**
_Every multigraph without a cut consisting of exactly one or exactly three_
_edges has a 3-flow._

Again, the 3-flow conjecture will not be best possible: it is easy to construct graphs with three-edge cuts that have a 3-flow (exercise).

By our duality theorem (6.5.3), all three flow conjectures are true
for planar graphs and thus motivated: the 3-flow conjecture translates
to Gr¨otzsch’s theorem (5.1.3), the 4-flow conjecture to the four colour
theorem (since the Petersen graph is not planar, it is not a minor of a
planar graph), the 5-flow conjecture to the five colour theorem.

We finish this section with the main result of the chapter:

**Theorem 6.6.1. (Seymour 1981)**
_Every bridgeless graph has a 6-flow._

(3.3.5)
_Proof ._ Let G = (V, E) be a bridgeless graph. Since 6-flows on the (6.1.1)
components of G will add up to a 6-flow on G, we may assume that (6.4.1)
_G is connected; as G is bridgeless, it is then 2-edge-connected. Note_
that any two vertices in a 2-edge-connected graph lie in some common
even connected subgraph—for example, in the union of two edge-disjoint
paths linking these vertices by Menger’s theorem (3.3.5 (ii)). We shall
use this fact repeatedly.

5 The same applies to another well-known conjecture, the cycle double cover con_jecture; see Exercise 13._
6 That snarks are elusive has been known to mathematicians for some time; cf.


-----

_H0, . . ., Hn_ We shall construct a sequence H0, . . ., Hn of disjoint connected and
_F1, . . ., Fn_ even subgraphs of G, together with a sequence F1, . . ., Fn of non-empty
sets of edges between them. The sets Fi will each contain only one or
_Vi, Ei_ two edges, between Hi and H0 ∪ _. . . ∪_ _Hi−1. We write Hi =: (Vi, Ei),_

_H_ _[i]_ _H_ _[i]_ := (H0 ∪ _. . . ∪_ _Hi) + (F1 ∪_ _. . . ∪_ _Fi)_

_V_ _[i], E[i]_ and H _[i]_ =: (V _[i], E[i]). Note that each H_ _[i]_ = (H _[i][−][1]_ _∪_ _Hi) + Fi is connected_
(induction on i). Our assumption that Hi is even implies by Proposition
6.4.1 (or directly by Proposition 1.2.1) that Hi has no bridge.
As H0 we choose any K [1] in G. Now assume that H0, . . ., Hi−1 and
_F1, . . ., Fi−1 have been defined for some i > 0. If V_ _[i][−][1]_ = V, we terminate
_n_ the construction and set i − 1 =: n. Otherwise, we let Xi ⊆ _V_ _[i][−][1]_ be
_Xi_ minimal such that Xi ̸= ∅ and

��E(Xi, V i−1 ∖ _Xi)��_ ⩽ 1 (1)

(Fig. 6.6.2); such an Xi exists, because V _[i][−][1]_ is a candidate. Since G
is 2-edge-connected, (1) implies that E(Xi, V _[i][−][1]) ̸= ∅. By the mini-_
mality of Xi, the graph G [ Xi ] is connected and bridgeless, i.e. 2-edge_Fi_ connected or a K [1]. As the elements of Fi we pick one or two edges
from E(Xi, V _[i][−][1]), if possible two. As Hi we choose any connected even_
subgraph of G [ Xi ] containing the ends in Xi of the edges in Fi.

_V_ _[i][−][1]_ ∖ _Xi_

_H_ _[i][−][1]_

_Hi_
_Fi_ _Xi_

_V_ _[i][−][1]_

_Fig. 6.6.2. Constructing the Hi and Fi_

_H_ When our construction is complete, we set H _[n]_ =: H and E[′] :=
_E[′]_ _E ∖_ _E(H)._ By definition of n, H is a spanning connected subgraph
of G.
_fn, . . ., f0_ We now define, by ‘reverse’ induction, a sequence fn, . . ., f0 of Z3_C→e_ circulations on G. For every edge e ∈ _E[′], let_ _C→e be a cycle (with orienta-_
tion) in H + e containing e, and fe a positive flow around _C→e; formally,_
_→_ _→_ _←_
_fe_ we let fe be a Z3-circulation on G such that fe[−][1](0) = _E ∖_ (Ce ∪ _Ce)._
_fn_ Let fn be the sum of all these fe. Since each e[′ ∈] _E[′]_ lies on just one of


-----

Assume now that Z3-circulations fn, . . ., fi on G have been defined _fi_
for some i ⩽ _n, and that_


_→_
_→_ _→_ �
_fi(e) ̸= 0 for all_ _e ∈_ _E[′]_ _∪_

_j>i_


_F→j,_ (2)


where _F→j := {_ _→e ∈_ _E→ | e ∈_ _Fj }. Our aim is to define fi−1 in such a way_ _F→j_

that (2) also holds for i 1.
_−_
We first consider the case that |Fi| = 1, say Fi = { e }. We then _e_
let fi−1 := fi, and thus have to show that fi is non-zero on (the two
directions of) e. Our assumption of |Fi| = 1 implies by the choice of
_Fi that G contains no Xi–V_ _[i][−][1]_ edge other than e. Since G is 2-edgeconnected, it therefore has at least—and thus, by (1), exactly—one edge
_e[′]_ between Xi and V _[i][−][1]_ ∖ _Xi. We show that fi is non-zero on e[′]; as_ _e[′]_
_{ e, e[′]_ _} is a cut in G, this implies by Proposition 6.1.1 that fi is also_
non-zero on e.
To show that fi is non-zero on e[′], we use (2): we show that e[′ ∈]
_E[′]_ _∪_ [�]j>i _[F][j][, i.e. that][ e][′][ lies in no][ H][k][ and in no][ F][j][ with][ j][ ⩽]_ _[i][. Since][ e][′]_

has both ends in V _[i][−][1], it clearly lies in no Fj with j ⩽_ _i and in no Hk_
with k < i. But every Hk with k ⩾ _i is a subgraph of G [ V_ _[i][−][1]_ ]. Since e[′]

is a bridge of G [ V _[i][−][1]_ ] but Hk has no bridge, this means that e[′] _∈/_ _Hk._
Hence, fi−1 does indeed satisfy (2) for i − 1 in the case considered.
It remains to consider the case that |Fi| = 2, say Fi = { e1, e2 }. _e1, e2_
Since Hi and H _[i][−][1]_ are both connected, we can find a cycle C in H _[i]_ = _C_
(Hi _H_ _[i][−][1])+_ _Fi that contains e1 and e2. If fi is non-zero on both these_
edges, we again let ∪ _fi−1 := fi. Otherwise, there are directions_ _e→1 and_
_e→2 of e1 and e2 such that, without loss of generality, fi(e→1) = 0 and_
a flow of value 1 aroundfi(e→2) ∈ _{ 0, 1 }. Let_ _C→ be the orientation ofC→ (formally: let g be a C with Z3-circulation one→2 ∈_ _C→, and let G such g be_
that g(e→2) = 1 and g[−][1](0) = _E→ ∖_ (C→ ∪ _C←)). We then let fi−1 := fi + g._
By choice of the directionsSince fi−1 agrees with fi on all ofe→1 and _Ee→→2[′]_,∪ f[�]i−j>i1 is non-zero on both edges.F→j and (2) holds for i, we

again have (2) also for i 1.
_−_
Eventually, f0 will be a Z3-circulation on G that is nowhere zero
except possibly on edges of H0 ∪ _. . . ∪_ _Hn. Composing f0 with the map_
_h �→_ 2h from Z3 to Z6 (h ∈ _{ 1, 2 }), we obtain a Z6-circulation f on G_ _f_
with values in { 0, 2, 4 } for all edges lying in some Hi, and with values
in { 2, 4 } for all other edges. Adding to f a 2-flow on each Hi (formally:
a Z6-circulation on G with values in { 1, −1 } on the edges of Hi and 0
otherwise; this exists by Proposition 6.4.1), we obtain a Z6-circulation
on G that is nowhere zero. Hence, G has a 6-flow by Theorem 6.3.3.

                    

-----

###### Exercises

1.[−] Prove Proposition 6.2.1 by induction on |S|.

2. (i)[−] Given n _[∈]_ N, find a capacity function for the network below such
that the algorithm from the proof of the max-flow min-cut theorem will
need more than n augmenting paths W if these are badly chosen.

_s_ _t_

(ii)[+] Show that, if all augmenting paths are chosen as short as possible,
their number is bounded by a function of the size of the network.

3.[+] Derive Menger’s Theorem 3.3.4 from the max-flow min-cut theorem.

(Hint. The edge version is easy. For the vertex version, apply the edge
version to a suitable auxiliary graph.)

4.[−] Let f be an H-circulation on G and g: H → _H_ _[′]_ a group homomorphism.
Show that g ◦ _f is an H_ _[′]-circulation on G. Is g ◦_ _f an H_ _[′]-flow if f is an_
_H-flow?_

5.[−] Given k ⩾ 1, show that a graph has a k-flow if and only if each of its
blocks has a k-flow.

6.[−] Show that ϕ(G/e) ⩽ _ϕ(G) whenever G is a multigraph and e an edge_
of G. Does this imply that, for every k, the class of all multigraphs
admitting a k-flow is closed under taking minors?

7.[−] Work out the flow number of K [4] directly, without using any results
from the text.

8. Let H be a finite abelian group, G a graph, and T a spanning tree
of G. Show that every mapping from the directions of E(G) ∖ _E(T_ ) to
_H that satisfies (F1) extends uniquely to an H-circulation on G._

Do not use the 6-flow Theorem 6.6.1 for the following three exercises.

9. Show that ϕ(G) < ∞ for every bridgeless multigraph G.

10. Assume that a graph G has m spanning trees such that no edge of G
lies in all of these trees. Show that ϕ(G) ⩽ 2[m].

11.[+] Let G be a bridgeless connected graph with n vertices and m edges. By
considering a normal spanning tree of G, show that ϕ(G) ⩽ _m −_ _n + 2._

12. Show that every graph with a Hamilton cycle has a 4-flow. (A Hamilton
_cycle of G is a cycle in G that contains all the vertices of G.)_

13. A family of (not necessarily distinct) cycles in a graph G is called a
_cycle double cover of G if every edge of G lies on exactly two of these_
cycles. The cycle double cover conjecture asserts that every bridgeless
multigraph has a cycle double cover. Prove the conjecture for graphs


-----

14.[−] Determine the flow number of C [5] _∗_ _K_ [1], the wheel with 5 spokes.

15. Find bridgeless graphs G and H = G − _e such that 2 < ϕ(G) < ϕ(H)._

16. Prove Proposition 6.4.1 without using Theorem 6.3.3.

17.[+] Prove Heawood’s theorem that a plane triangulation is 3-colourable if
and only if all its vertices have even degree.

18.[−] Find a bridgeless graph that has both a 3-flow and a cut of exactly
three edges.

19. Show that the 3-flow conjecture for planar multigraphs is equivalent to
Gr¨otzsch’s Theorem 5.1.3.

20. (i)[−] Show that the four colour theorem is equivalent to the non-existence of a planar snark, i.e. to the statement that every cubic bridgeless
planar multigraph has a 4-flow.

(ii) Can ‘bridgeless’ in (i) be replaced by ‘3-connected’?

21.[+] Show that a graph G = (V, E) has a k-flow if and only if it admits an
orientation D that directs, for every X ⊆ _V, at least 1/k of the edges_
in E(X, X) from X towards X.

22.[−] Generalize the 6-flow Theorem 6.6.1 to multigraphs.

###### Notes

Network flow theory is an application of graph theory that has had a major
and lasting impact on its development over decades. As is illustrated already
by the fact that Menger’s theorem can be deduced easily from the max-flow
min-cut theorem (Exercise 3), the interaction between graphs and networks
may go either way: while ‘pure’ results in areas such as connectivity, matching
and random graphs have found applications in network flows, the intuitive
power of the latter has boosted the development of proof techniques that have
in turn brought about theoretic advances.
The standard reference for network flows is L.R. Ford & D.R. Fulkerson,
_Flows in Networks, Princeton University Press 1962. A more recent and com-_
prehensive account is given by R.K. Ahuja, T.L. Magnanti & J.B. Orlin, Net_work flows, Prentice-Hall 1993. For more theoretical aspects, see A. Frank’s_
chapter in the Handbook of Combinatorics (R.L. Graham, M. Gr¨otschel &
L. Lov´asz, eds.), North-Holland 1995. A general introduction to graph algorithms is given in A. Gibbons, Algorithmic Graph Theory, Cambridge University Press 1985.
If one recasts the maximum flow problem in linear programming terms,
one can derive the max-flow min-cut theorem from the linear programming
duality theorem; see A. Schrijver, Theory of integer and linear programming,
Wiley 1986.
The more algebraic theory of group-valued flows and k-flows has been
developed largely by Tutte; he gives a thorough account in his monograph


-----

covered also in F. Jaeger’s survey, Nowhere-zero[7] flow problems, in (L.W. Beineke & R.J. Wilson, eds.) Selected Topics in Graph Theory 3, Academic Press
1988. For the flow conjectures, see also T.R. Jensen & B. Toft, Graph Coloring
_Problems, Wiley 1995. Seymour’s 6-flow theorem is proved in P.D. Seymour,_
Nowhere-zero 6-flows, J. Combin. Theory B 30 (1981), 130–135. This paper also indicates how Tutte’s 5-flow conjecture reduces to snarks. In 1998,
Robertson, Sanders, Seymour and Thomas announced a proof of the 4-flow
conjecture for cubic graphs.
Finally, Tutte discovered a 2-variable polynomial associated with a graph,
which generalizes both its chromatic polynomial and its flow polynomial.
What little is known about this Tutte polynomial can hardly be more than
the tip of the iceberg: it has far-reaching, and largely unexplored, connections
to areas as diverse as knot theory and statistical physics. See D.J.A. Welsh,
_Complexity: knots, colourings and counting (LMS Lecture Notes 186), Cam-_
bridge University Press 1993.

7 In the literature the term ‘flow’ is often used to mean what we have called ‘cir

-----

# 7 Substructures in
### Dense Graphs

In this chapter and the next, we study how global parameters of a graph,
such as its edge density or chromatic number, have a bearing on the
existence of certain local substructures. How many edges, for instance,
do we have to give a graph on n vertices to be sure that, no matter how
these edges happen to be arranged, the graph will contain a K _[r]_ subgraph
for some given r? Or at least a K _[r]_ minor? Or a topological K _[r]_ minor?
Will some sufficiently high average degree or chromatic number ensure
that one of these substructures occurs?
Questions of this type are among the most natural ones in graph
theory, and there is a host of deep and interesting results. Collectively,
these are known as extremal graph theory.
Extremal graph problems in this sense fall neatly into two categories,
as follows. If we are looking for ways to ensure by global assumptions
that a graph G contains some given graph H as a minor (or topological
minor), it will suffice to raise _G_ above the value of some linear function
_∥_ _∥_
of _G_ (depending on H), i.e. to make ε(G) large enough. The existence
_|_ _|_
of such a function was already established in Theorem 3.6.1. The precise
growth rate needed will be investigated in Chapter 8, where we study
substructures of such ‘sparse’ graphs. Since a large enough value of ε
gives rise to an H minor for any given graph H, its occurrence could be
forced alternatively by raising some other global invariants (such as κ
or χ) which, in turn, force up the value of ε, at least in some subgraph.
This, too, will be a topic for Chapter 8.
On the other hand, if we ask what global assumptions might imply
the existence of some given graph H as a subgraph, it will not help
to raise any of the invariants ε, κ or χ, let alone any of the other in

-----

given any graph H that contains at least one cycle, there are graphs
of arbitrarily large chromatic number not containing H as a subgraph
(Theorem 11.2.2). By Corollary 5.2.3 and Theorem 1.4.2, such graphs
have subgraphs of arbitrarily large average degree and connectivity, so
these invariants too can be large without the presence of an H subgraph.
Thus, unless H is a forest, the only way to force the presence of an H
subgraph in an arbitrary graph G by global assumptions on G is to raise
_G_ substantially above any value implied by large values of the above
_∥_ _∥_
invariants. If H is not bipartite, then any function f such that f (n)
edges on n vertices force an H subgraph must even grow quadratically
with n: since complete bipartite graphs can have [1]4 _[n][2][ edges,][ f]_ [(][n][) must]

exceed [1]

4 _[n][2][.]_
_dense_ Graphs with a number of edges roughly[1] quadratic in their number
of vertices are usually called dense; the number ∥G∥��|G2 _|�—the propor-_
_edge_
tion of its potential edges that G actually has—is the edge density of G.
_density_
The question of exactly which edge density is needed to force a given
subgraph is the archetypal extremal graph problem in its original (narrower) sense; it is the topic of this chapter. Rather than attempting to
survey the wide field of (dense) extremal graph theory, however, we shall
concentrate on its two most important results and portray one powerful
general proof technique.
The two results are Tur´an’s classic extremal graph theorem for
_H = K_ _[r], a result that has served as a model for countless similar_
theorems for other graphs H, and the fundamental Erd˝os-Stone theorem, which gives precise asymptotic information for all H at once (Section 7.1). The proof technique, one of increasing importance in the
extremal theory of dense graphs, is the use of the Szemer´edi regularity
_lemma. This lemma is presented and proved in Section 7.2. In Sec-_
tion 7.3, we outline a general method for applying the regularity lemma,
and illustrate this in the proof of the Erd˝os-Stone theorem postponed
from Section 7.1. Another application of the regularity lemma will be
given in Chapter 9.2.

###### 7.1 Subgraphs

Let H be a graph and n ⩾ _|H|. How many edges will suffice to force an_
_H subgraph in any graph on n vertices, no matter how these edges are_
arranged? Or, to rephrase the problem: which is the greatest possible
number of edges that a graph on n vertices can have without containing
a copy of H as a subgraph? What will such a graph look like? Will it
be unique?

1 Note that, formally, the notions of sparse and dense make sense only for families


-----

A graph G _H on n vertices with the largest possible number of_
_̸⊇_
edges is called extremal for n and H; its number of edges is denoted by _extremal_
ex(n, H). Clearly, any graph G that is extremal for some n and H will ex(n, H)
also be edge-maximal with H _G. Conversely, though, edge-maximality_
_̸⊆_
does not imply extremality: G may well be edge-maximal with H _G_
_̸⊆_
while having fewer than ex(n, H) edges (Fig. 7.1.1).

_Fig. 7.1.1. Two graphs that are edge-maximal with P_ [3] _̸⊆_ _G; is_
the right one extremal?

As a case in point, we consider our problem for H = K _[r]_ (with r > 1).
A moment’s thought suggests some obvious candidates for extremality
here: all complete (r 1)-partite graphs are edge-maximal without con_−_
taining K _[r]. But which among these have the greatest number of edges?_
Clearly those whose partition sets are as equal as possible, i.e. differ in
size by at most 1: if V1, V2 are two partition sets with |V1|−|V2| ⩾ 2, we
may increase the number of edges in our complete (r 1)-partite graph
_−_
by moving a vertex from V1 across to V2.
The unique complete (r − 1)-partite graphs on n ⩾ _r −_ 1 vertices
whose partition sets differ in size by at most 1 are called Tur´an graphs;
we denote them by T _[r][−][1](n) and their number of edges by tr−1(n)_ _T_ _[r][−][1](n)_
(Fig. 7.1.2). For n < r − 1 we shall formally continue to use these _tr−1(n)_
definitions, with the proviso that—contrary to our usual terminology—
the partition sets may now be empty; then, clearly, T _[r][−][1](n) = K_ _[n]_ for
all n ⩽ _r −_ 1.

_Fig. 7.1.2. The Tur´an graph T_ [3](8)

The following theorem tells us that T _[r][−][1](n) is indeed extremal for_


-----

**Theorem 7.1.1. (Tur´an 1941)**

[ 7.1.2 ]
_For all integers r, n with r > 1, every graph G_ _K_ _[r]_ _with n vertices and_

[ 9.2.2 ] _̸⊇_
ex(n, K _[r]) edges is a T_ _[r][−][1](n)._

_Proof . We apply induction on n. For n ⩽_ _r −_ 1 we have G = K _[n]_ =
_T_ _[r][−][1](n) as claimed. For the induction step, let now n ⩾_ _r._
Since G is edge-maximal without a K _[r]_ subgraph, G has a sub_K_ graph K = K _[r][−][1]. By the induction hypothesis, G_ _K has at most_
_−_
_tr−1(n −_ _r + 1) edges, and each vertex of G −_ _K has at most r −_ 2
neighbours in K. Hence,

�r 1�
_−_
_∥G∥_ ⩽ _tr−1(n −_ _r + 1) + (n −_ _r + 1)(r −_ 2) + = tr−1(n) ; (1)
2

the equality on the right follows by inspection of the Tur´an graph T _[r][−][1](n)_
(Fig. 7.1.3).

_r −_ 2


�r−1�
2


_tr−1(n −_ _r + 1)_


_Fig. 7.1.3. The equation from (1) for r = 5 and n = 14_

Since G is extremal for K _[r]_ (and T _[r][−][1](n)_ _K_ _[r]), we have equality_
_̸⊇_
in (1). Thus, every vertex of G _K has exactly r_ 2 neighbours in K—
_−_ _−_
_x1, . . ., xr−1_ just like the vertices x1, . . ., xr−1 of K itself. For i = 1, . . ., r − 1 let

_V1, . . ., Vr−1_ _Vi := { v ∈_ _V (G) | vxi /∈_ _E(G) }_

be the set of all vertices of G whose r 2 neighbours in K are precisely the
_−_
vertices other than xi. Since K _[r]_ _̸⊆_ _G, each of the sets Vi is independent,_
and they partition V (G). Hence, G is (r 1)-partite. As T _[r][−][1](n) is the_
_−_
unique (r 1)-partite graph with n vertices and the maximum number of
_−_
edges, our claim that G = T _[r][−][1](n) follows from the assumed extremality_
of G.       
The Tur´an graphs T _[r][−][1](n) are dense: in order of magnitude, they_
have about n[2] edges. More exactly, for every n and r we have

1 2 _[r][ −]_ [2]
( )


-----

with equality whenever r 1 divides n (Exercise 8). It is therefore
_−_
remarkable that just ϵn[2] more edges (for any fixed ϵ > 0 and n large)
give us not only a K _[r]_ subgraph (as does Tur´an’s theorem) but a Ks[r] [for]
any given integer s—a graph itself teeming with K _[r]_ subgraphs:

**Theorem 7.1.2. (Erd˝os & Stone 1946)**
_For all integers r ⩾_ 2 and s ⩾ 1, and every ϵ > 0, there exists an integer
_n0 such that every graph with n ⩾_ _n0 vertices and at least_

_tr−1(n) + ϵn[2]_

_edges contains Ks[r]_ _[as a subgraph.]_

We shall prove this theorem in Section 7.3.

The Erd˝os-Stone theorem is interesting not only in its own right: it
also has a most interesting corollary. In fact, it was this entirely unexpected corollary that established the theorem as a kind of meta-theorem
for the extremal theory of dense graphs, and thus made it famous.
Given a graph H and an integer n, consider the number hn :=
ex(n, H)/�n2�: the maximum edge density that an n-vertex graph can
have without containing a copy of H. Could it be that this critical
density is essentially just a function of H, that hn converges as n →∞?
Theorem 7.1.2 implies this, and more: the limit of hn is determined by a
very simple function of a natural invariant of H—its chromatic number!

**Corollary 7.1.3. For every graph H with at least one edge,**


�n�−1
lim = _[χ][(][H][)][ −]_ [2]
_n→∞_ [ex(][n, H][)] 2 _χ(H) −_ 1 _[.]_


For the proof of Corollary 7.1.3 we need as a lemma that tr−1(n)
never deviates much from the value it takes when r 1 divides n (see
_−_
above), and that tr−1(n)/�n2� converges accordingly. The proof of the
lemma is left as an easy exercise with hint (Exercise 9).

**Lemma 7.1.4.** [ 7.1.2 ]


�n�−1
lim = _[r][ −]_ [2]
_n→∞_ _[t][r][−][1][(][n][)]_ 2 _r −_ 1 _[.]_


-----

_r_ **Proof of Corollary 7.1.3. Let r := χ(H). Since H cannot be coloured**
with r − 1 colours, we have H ̸⊆ _T_ _[r][−][1](n) for all n_ _[∈]_ N, and hence

_tr−1(n) ⩽_ ex(n, H) .

On the other hand, H ⊆ _Ks[r]_ [for all sufficiently large][ s][, so]

ex(n, H) ⩽ ex(n, Ks[r][)]

_s_ for all those s. Let us fix such an s. For every ϵ > 0, Theorem 7.1.2
implies that eventually (i.e. for large enough n)

ex(n, Ks[r][)][ < t][r][−][1][(][n][) +][ ϵn][2][.]

Hence for n large,

_tr−1(n)/�n2�_ ⩽ ex(n, H)/�n2�

⩽ ex(n, Ks[r][)][/]�n2�

_< tr−1(n)/�n2�_ + ϵn[2]/�n2�

= tr−1(n)/�n2� + 2ϵ/(1 − _n[1]_ [)]

⩽ _tr−1(n)/�n2�_ + 4ϵ (assume n ⩾ 2).

ex(Therefore, sincen, H)/�n2�. Thus tr−1(n)/�n2� converges to _[r]r[−]−[2]1_ [(Lemma 7.1.4), so does]


�n�−1
lim = _[r][ −]_ [2]
_n→∞_ [ex(][n, H][)] 2 _r −_ 1

as claimed. 
For bipartite graphs H, Corollary 7.1.3 says that substantially fewer
than �n2� edges suffice to force an H subgraph. It turns out that


2
_c1n[2][−]_ _r+1 ⩽_ ex(n, Kr,r) ⩽ _c2n[2][−]_ _r[1]_

for suitable constants c1, c2 depending on r; the lower bound is obtained
by random graphs,[2] the upper bound is calculated in Exercise 13. If H
is a forest, then H _G as soon as ε(G) is large enough, so ex(n, H)_
_⊆_
is at most linear in n (Exercise 5). Erd˝os and S´os conjectured in 1963
that ex(n, T ) ⩽ [1]2 [(][k][ −] [1)][n][ for all trees with][ k][ ⩾] [2 edges; as a general]

bound for all n, this is best possible for every T . See Exercises 15–18 for
details.


-----

###### 7.2 Szemer´edi’s regularity lemma

More than 20 years ago, in the course of the proof of a major result on
the Ramsey properties of arithmetic progressions, Szemer´edi developed a
graph theoretical tool whose fundamental importance has been realized
more and more in recent years: his so-called regularity or uniformity
_lemma. Very roughly, the lemma says that all graphs can be approx-_
imated by random graphs in the following sense: every graph can be
partitioned, into a bounded number of equal parts, so that most of its
edges run between different parts and the edges between any two parts
are distributed fairly uniformly—just as we would expect it if they had
been generated at random.
In order to state the regularity lemma precisely, we need some definitions. Let G = (V, E) be a graph, and let X, Y _V be disjoint. Then_
_⊆_
we denote by ∥X, Y ∥ the number of X–Y edges of G, and call _∥X, Y ∥_

_d(X, Y ) :=_

_[∥]X[X, Y]Y[ ∥]_ _d(X, Y )_

_|_ _| |_ _|_

the density of the pair (X, Y ). (This is a real number between 0 and 1.) _density_
Given some ϵ > 0, we call a pair (A, B) of disjoint sets A, B _V ϵ-regular_
_⊆_
_ϵ-regular_
if all X _A and Y_ _B with_
_⊆_ _⊆_ _pair_

_|X| ⩾_ _ϵ |A|_ and _|Y | ⩾_ _ϵ |B|_

satisfy
��d(X, Y ) − _d(A, B)��_ ⩽ _ϵ ._

The edges in an ϵ-regular pair are thus distributed fairly uniformly: the
smaller ϵ, the more uniform their distribution.
Consider a partition { V0, V1, . . ., Vk } of V in which one set V0 has _exceptional_
been singled out as an exceptional set. (This exceptional set V0 may _set_
be empty.[3]) We call such a partition an ϵ-regular partition of G if it
satisfies the following three conditions:

_ϵ-regular_
(i) |V0| ⩽ _ϵ |V |;_ _partition_
(ii) |V1| = . . . = |Vk|;

(iii) all but at most ϵk[2] of the pairs (Vi, Vj) with 1 ⩽ _i < j ⩽_ _k are_
_ϵ-regular._

The role of the exceptional set V0 is one of pure convenience: it
makes it possible to require that all the other partition sets have exactly
the same size. Since condition (iii) affects only the sets V1, . . ., Vk, we

3 So V0 may be an exception also to our terminological rule that partition sets


-----

may think of V0 as a kind of bin: its vertices are disregarded when
the uniformity of the partition is assessed, but there are only few such
vertices.

**Lemma 7.2.1. (Regularity Lemma)**

[ 9.2.2 ] _For every ϵ > 0 and every integer m ⩾_ 1 there exists an integer M
_such that every graph of order at least m admits an ϵ-regular partition_
_{ V0, V1, . . ., Vk } with m ⩽_ _k ⩽_ _M_ _._

The regularity lemma thus says that, given any ϵ > 0, every graph
has an ϵ-regular partition into a bounded number of sets. The upper
bound M on the number of partition sets ensures that for large graphs
the partition sets are large too; note that ϵ-regularity is trivial when
the partition sets are singletons, and a powerful property when they are
large. In addition, the lemma allows us to specify a lower bound m on
the number of partition sets; by choosing m large, we may increase the
proportion of edges running between different partition sets (rather than
inside one), i.e. the proportion of edges that are subject to the regularity
assertion.
Note that the regularity lemma is designed for use with dense
graphs:[4] for sparse graphs it becomes trivial, because all densities of
pairs—and hence their differences—tend to zero (Exercise 22).
The remainder of this section is devoted to the proof of the regularity lemma. Although the proof is not difficult, a reader meeting the
regularity lemma here for the first time is likely to draw more insight
from seeing how the lemma is typically applied than from studying the
technicalities of its proof. Any such reader is encouraged to skip to the
start of Section 7.3 now and come back to the proof at his or her leisure.

We shall need the following inequality for reals µ1, . . ., µk > 0 and
_e1, . . ., ek ⩾_ 0:
� _e[2]i_

⩾ [(][�] _[e][i][)][2]_ _._ (1)
_µi_ � _µi_


This follows from the Cauchy-Schwarz inequality [�] _a[2]i_ � _b2i_ [⩾] [(][�] _[a][i][b][i][)][2]_

by taking ai := _[√]µi and bi := ei/[√]µi._
_G = (V, E)_ Let G = (V, E) be a graph and n := _V_ . For disjoint sets A, B _V_
_|_ _|_ _⊆_
_n_ we define

_A, B_
_∥_ _∥[2]_

_q(A, B)_ _q(A, B) :=_ _d[2](A, B) =_

_[|][A][| |][B][|]_

_n[2]_ _A_ _B_ _n[2][ .]_

_|_ _| |_ _|_

For partitions of A and of B we set
_A_ _B_


_q(A, B)_ _q(A, B) :=_ � _q(A[′], B[′]),_
_A[′ ]∈A; B[′ ]∈B_


-----

and for a partition P = { C1, . . ., Ck } of V we let

�
_q(P) :=_ _q(Ci, Cj) ._ _q(P)_

_i<j_

However, if P = { C0, C1, . . ., Ck } is a partition of V with exceptional
_set C0, we treat C0 as a set of singletons and define_

_q(_ ) := q( [˜]),
_P_ _P_

where P[˜] := �C1, . . ., Ck� _∪_ �{ v } : v ∈ _C0�._ _P˜_
The function q( ) plays a pivotal role in the proof of the regularity
_P_
lemma. On the one hand, it measures the uniformity of the partition :
_P_
if has too many irregular pairs (A, B), we may take the pairs (X, Y ) of
_P_
subsets violating the regularity of the pairs (A, B) and make those sets
_X and Y into partition sets of their own; as we shall prove, this refines_
into a partition for which q is substantially greater than for . Here,
_P_ _P_
‘substantial’ means that the increase of q( ) is bounded below by some
_P_
constant depending only on ϵ. On the other hand,


�
_q(P) =_ _q(Ci, Cj)_

_i<j_


�
=

_i<j_


_|Ci| |Cj|_

_d[2](Ci, Cj)_
_n[2]_


�

⩽ [1] _|Ci| |Cj|_

_n[2]_

_i<j_

⩽ 1 .

The number of times that q( ) can be increased by a constant is thus
_P_
also bounded by a constant—in other words, after some bounded number
of refinements our partition will be ϵ-regular! To complete the proof of
the regularity lemma, all we have to do then is to note how many sets
that last partition can possibly have if we start with a partition into m
sets, and to choose this number as our desired bound M .
Let us make all this precise. We begin by showing that, when we
refine a partition, the value of q will not decrease:

**Lemma 7.2.2.**

(i) Let C, D _V be disjoint. If_ _is a partition of C and_ _is a_
_⊆_ _C_ _D_
_partition of D, then q(C, D) ⩾_ _q(C, D)._


-----

_Proof . (i) Let C =: { C1, . . ., Ck } and D =: { D1, . . ., Dℓ_ _}. Then_

�
_q(C, D) =_ _q(Ci, Dj)_

_i,j_


1

�

=

_n[2]_

_i,j_


2
_∥Ci, Dj∥_

_|Ci| |Dj|_


�� �2

⩾ 1 _i,j_ _[∥][C][i][, D][j][∥]_
(1) _n[2]_ �i,j _[|][C][i][| |][D][j][|]_

1 _C, D_

_∥_ _∥[2]_

=

_n[2]_ ��i _[|][C][i][|]���j_ _[|][D][j][|]�_


= q(C, D) .

(ii) Let P =: { C1, . . ., Ck }, and for i = 1, . . ., k let Ci be the partition of Ci induced by P _[′]. Then_

�
_q(P) =_ _q(Ci, Cj)_

_i<j_


⩽
(i)


�

_q(Ci, Cj)_
_i<j_


⩽ _q(P_ _[′]),_

since q(P _[′]) =_ [�]i _[q][(][C][i][) +][ �]i<j_ _[q][(][C][i][,][ C][j][).]_ 
Next, we show that refining a partition by subpartitioning an irregular pair of partition sets increases the value of q a little; since we are
dealing here with a single pair only, the amount of this increase will still
be less than any constant.


**Lemma 7.2.3. Let ϵ > 0, and let C, D** _V be disjoint. If (C, D) is not_
_⊆_
_ϵ-regular, then there are partitions C = (C1, C2) of C and D = (D1, D2)_
_of D such that_

_q(C, D) ⩾_ _q(C, D) + ϵ[4][ |][C][| |][D][|]_ _._

_n[2]_

_Proof . Suppose (C, D) is not ϵ-regular. Then there are sets C1 ⊆_ _C and_
_D1 ⊆_ _D with |C1| > ϵ |C| and |D1| > ϵ |D| such that_

_η_ _> ϵ_ (2)
_|_ _|_

_η_ for η := d(C1, D1) − _d(C, D). Let C := { C1, C2 } and D := { D1, D2 },_


-----

Let us show that and satisfy the conclusion of the lemma. We
_C_ _D_
shall write ci := |Ci|, di := |Di|, eij := ∥Ci, Dj∥, c := |C|, d := |D| _ci, di, eij_
and e := _C, D_ . As in the proof of Lemma 7.2.2, _c, d, e_
_∥_ _∥_


1

�

_q(_ _,_ ) =
_C_ _D_

_n[2]_

_i,j_


_e[2]ij_

_cidj_


_e[2]ij_

_cidj_


�


1
=

_n[2]_


� _e211_ �

+
_c1d1_

_i+j>2_


�
_._


� _e211_ + [(][e][ −] _[e][11][)][2]_

_c1d1_ _cd −_ _c1d1_


⩾
(1)


1

_n[2]_


By definition of η, we have e11 = c1d1e/cd + ηc1d1, so


_n[2]_ _q(C, D) ⩾_ 1 � _c1d1e_ + ηc1d1�2

_c1d1_ _cd_


1
+

_cd −_ _c1d1_


� _cd −_ _c1d1_ �2

_e −_ _ηc1d1_
_cd_


= _[c][1][d][1][e][2]_ + η[2]c1d1

_c[2]d[2][ + 2][eηc]cd[1][d][1]_

+ _[cd][ −]_ _[c][1][d][1]_ _e[2]_ + _η[2]c[2]1[d][2]1_

_−_ [2][eηc][1][d][1]
_c[2]d[2]_ _cd_ _cd −_ _c1d1_

_e[2]_
⩾ _cd_ [+][ η][2][c][1][d][1]


⩾
(2)


_e[2]_

_cd_ [+][ ϵ][4][cd]


since c1 ⩾ _ϵc and d1 ⩾_ _ϵd by the choice of C1 and D1._ 
Finally, we show that if a partition has enough irregular pairs of
partition sets to fall short of the definition of an ϵ-regular partition,
then subpartitioning all those pairs at once results in an increase of q by
a constant:

**Lemma 7.2.4. Let 0 < ϵ ⩽** 1/4, and let P = { C0, C1, . . ., Ck }
_be a partition of V, with exceptional set C0 of size |C0| ⩽_ _ϵn and_
_|C1| = . . . = |Ck| =: c. If P is not ϵ-regular, then there is a partition_ _c_
_P_ _[′]_ = { C0[′] _[, C]1[′]_ _[, . . ., C]ℓ[′]_ _[}][ of][ V][ with exceptional set][ C]0[′]_ _[, where][ k][ ⩽]_ _[ℓ]_ [⩽] _[k][4][k][,]_
_such that |C0[′]_ _[|][ ⩽]_ _[|][C][0][|][ +][ n/][2][k][, all other sets][ C]i[′]_ _[have equal size, and]_


-----

_Cij_ _Proof . For all 1 ⩽_ _i < j ⩽_ _k, let us define a partition Cij of Ci and_
a partition Cji of Cj, as follows. If the pair (Ci, Cj) is ϵ-regular, we let
_Cij := { Ci } and Cji := { Cj }. If not, then by Lemma 7.2.3 there are_
partitions Cij of Ci and Cji of Cj with |Cij| = |Cji| = 2 and

_q(Cij, Cji) ⩾_ _q(Ci, Cj) + ϵ[4][ |][C][i][| |][C][j][|]_ = q(Ci, Cj) + _[ϵ][4][c][2]_ (3)

_n[2]_ _n[2][ .]_


_Ci_ For each i = 1, . . ., k, let Ci be the unique minimal partition of Ci that
refines every partition Cij with j ̸= i. (In other words, if we consider two
elements of Ci as equivalent whenever they lie in the same partition set
of Cij for every j ̸= i, then Ci is the set of equivalence classes.) Thus,
_|Ci| ⩽_ 2[k][−][1]. Now consider the partition

_k_
�

_C_ _C := { C0 } ∪_ _Ci_
_i=1_


of V, with C0 as exceptional set. Then C refines P, and

_k ⩽_ _|C| ⩽_ _k2[k]._ (4)

_C0_ Let C0 := �{ v } : v ∈ _C0�. Now if P is not ϵ-regular, then for more_
than ϵk[2] of the pairs (Ci, Cj) with 1 ⩽ _i < j ⩽_ _k the partition Cij is_
non-trivial. Hence, by our definition of q for partitions with exceptional
set, and Lemma 7.2.2 (i),

� � �
_q(C) =_ _q(Ci, Cj) +_ _q(C0, Ci) +_ _q(Ci)_

1⩽i<j 1⩽i 0⩽i


⩾ � _q(Cij, Cji) +_ � _q�C0, { Ci }�_ + q(C0)

1⩽i<j 1⩽i


⩾
(3)


� _q(Ci, Cj) + ϵk[2][ ϵ]n[4][c][2][ +][2]_ � _q�C0, { Ci }�_ + q(C0)

1⩽i<j 1⩽i


� _kc_
= q( ) + ϵ[5]
_P_

_n_


�2


⩾ _q(P) + ϵ[5]/2 ._

(For the last inequality, recall that |C0| ⩽ _ϵn ⩽_ [1]4 _[n][, so][ kc][ ⩾]_ [3]4 _[n][.)]_

In order to turn into our desired partition, all that remains to
_C_ _P_ _[′]_
do is to cut its sets up into pieces of some common size, small enough that
all remaining vertices can be collected into the exceptional set without
making this too large. Let C1[′] _[, . . ., C]ℓ[′]_ [be a maximal collection of dis-]
_/_ _[k]_


-----

_C_ _[∈]_ _C ∖_ _{ C0 }, and put C0[′]_ [:=][ V][ ∖] [�] _[C]i[′][. Then][ P]_ _[′][ =][ {][ C]0[′]_ _[, C]1[′]_ _[, . . ., C]ℓ[′]_ _[}]_ _P_ _[′]_
is indeed a partition of V . Moreover, [˜] refines [˜], so
_P_ _[′]_ _C_

_q(P_ _[′]) ⩾_ _q(C) ⩾_ _q(P) + ϵ[5]/2_

by Lemma 7.2.2 (ii). Since each set Ci[′] 0 [is also contained in one]

_[̸][=][ C]_ _[′]_
of the sets C1, . . ., Ck, but no more than 4[k] sets Ci[′] [can lie inside the]
same Cj (by the choice of d), we also have k ⩽ _ℓ_ ⩽ _k4[k]_ as required.
Finally, the sets C1[′] _[, . . ., C]ℓ[′]_ [use all but at most][ d][ vertices from each set]
_C ̸= C0 of C. Hence,_

_|C0[′]_ _[|][ ⩽]_ _[|][C][0][|][ +][ d][ |C|]_

⩽ _|C0| +_ _[c]_
(4) 4[k][ k][2][k]

= |C0| + ck/2[k]

⩽ _|C0| + n/2[k]._

                    
The proof of the regularity lemma now follows easily by repeated
application of Lemma 7.2.4:

**Proof of Lemma 7.2.1. Let ϵ > 0 and m ⩾** 1 be given; without loss _ϵ, m_
of generality, ϵ ⩽ 1/4. Let s := 2/ϵ[5]. This number s is an upper bound _s_
on the number of iterations of Lemma 7.2.4 that can be applied to a
partition of a graph before it becomes ϵ-regular; recall that q(P) ⩽ 1 for
all partitions .
_P_
There is one formal requirement which a partition { C0, C1, . . ., Ck }
with |C1| = . . . = |Ck| has to satisfy before Lemma 7.2.4 can be (re-)
applied: the size |C0| of its exceptional set must not exceed ϵn. With
each iteration of the lemma, however, the size of the exceptional set can
grow by up to n/2[k]. (More precisely, by up to n/2[ℓ], where ℓ is the
number of other sets in the current partition; but ℓ ⩾ _k by the lemma,_
so n/2[k] is certainly an upper bound for the increase.) We thus want
to choose k large enough that even s increments of n/2[k] add up to at
most [1]

2 _[ϵn][, and][ n][ large enough that, for any initial value of][ |][C][0][|][ < k][, we]_
have |C0| ⩽ 12 _[ϵn][. (If we give our starting partition][ k][ non-exceptional]_
sets C1, . . ., Ck, we should allow an initial size of up to k for C0, to be
able to achieve |C1| = . . . = |Ck|.)
So let k ⩾ _m be large enough that 2[k][−][1]_ ⩾ _s/ϵ. Then s/2[k]_ ⩽ _ϵ/2,_ _k_
and hence
_k +_ _[s]_ (5)

2[k][ n][ ⩽] _[ϵn]_


whenever k/n ⩽ _ϵ/2, i.e. for all n ⩾_ 2k/ϵ.
Let us now choose M . This should be an upper bound on the


-----

of Lemma 7.2.4, where in each iteration this number may grow from its
current value r to at most r4[r]. So let f be the function x _x4[x], and_
_�→_
_M_ take M := max _f_ _[s](k), 2k/ϵ_ ; the second term in the maximum ensures
_{_ _}_
that any n ⩾ _M is large enough to satisfy (5)._
We finally have to show that every graph G = (V, E) of order at
least m has an ϵ-regular partition { V0, V1, . . ., Vk } with m ⩽ _k ⩽_ _M_ . So
_n_ let G be given, and let n := |G|. If n ⩽ _M_, we partition G into k := n
singletons, choosing V0 := ∅ and |V1| = . . . = |Vk| = 1. This partition of
_G is clearly ϵ-regular. Suppose now that n > M_ . Let C0 ⊆ _V be minimal_
such that k divides |V ∖ _C0|, and let { C1, . . ., Ck } be any partition of_
_V ∖_ _C0 into sets of equal size. Then |C0| < k, and hence |C0| ⩽_ _ϵn by (5)._
Starting with { C0, C1, . . ., Ck } we apply Lemma 7.2.4 again and again,
until the partition of G obtained is ϵ-regular; this will happen after at
most s iterations, since by (5) the size of the exceptional set in the
partitions stays below ϵn, so the lemma could indeed be reapplied up to
the theoretical maximum of s times.      
###### 7.3 Applying the regularity lemma

The purpose of this section is to illustrate how the regularity lemma
is typically applied in the context of (dense) extremal graph theory.
Suppose we are trying to prove that a certain edge density of a graph G
suffices to force the occurrence of some given subgraph H, and that we
have an ϵ-regular partition of G. The edges inside almost all the pairs
(Vi, Vj) of partition sets are distributed uniformly, although their density
may depend on the pair. But since G has many edges, this density cannot
be zero for all the pairs: some sizeable proportion of the pairs will have
positive density. Now if G is large, then so are the pairs: recall that
the number of partition sets is bounded, and they have equal size. But
any large enough bipartite graph with equal partition sets, fixed positive
edge density (however small!) and a uniform distribution of edges will
contain any given bipartite subgraph[5]—this will be made precise below.
Thus if enough pairs in our partition of G have positive density that H
can be written as the union of bipartite graphs each arising in one of
those pairs, we may hope that H _G as desired._
_⊆_
These ideas will be formalized by Lemma 7.3.2 below. We shall then
use this and the regularity lemma to prove the Erd˝os-Stone theorem
from Section 7.1; another application will be given later, in the proof of
Theorem 9.2.2.
Before we state Lemma 7.3.2, let us note a simple consequence of
the ϵ-regularity of a pair (A, B): for any subset Y _B that is not too_
_⊆_

5 Readers already acquainted with random graphs may find it instructive to com

-----

small, most vertices of A have about the expected number of neighbours
in Y :

**Lemma 7.3.1. Let (A, B) be an ϵ-regular pair, of density d say, and let**
_Y ⊆_ _B have size |Y | ⩾_ _ϵ |B|. Then all but at most ϵ |A| of the vertices_
_in A have (each) at least (d_ _ϵ)_ _Y_ _neighbours in Y ._
_−_ _|_ _|_

_Proof . Let X_ _A be the set of vertices with fewer than (d_ _ϵ)_ _Y_
_⊆_ _−_ _|_ _|_
neighbours in Y . Then _X, Y_ _<_ _X_ (d _ϵ)_ _Y_, so
_∥_ _∥_ _|_ _|_ _−_ _|_ _|_

_d(X, Y ) =_

_[∥][X, Y][ ∥]_

_X_ _Y_ _[< d][ −]_ _[ϵ][ =][ d][(][A, B][)][ −]_ _[ϵ .]_
_|_ _| |_ _|_

Since (A, B) is ϵ-regular, this implies that |X| < ϵ |A|. 
Let G be a graph with an ϵ-regular partition { V0, V1, . . ., Vk }, with
exceptional set V0 and |V1| = . . . = |Vk| =: ℓ. Given d _[∈]_ (0, 1 ], let R be _R_
the graph with vertices V1, . . ., Vk in which two vertices are adjacent if
and only if they form an ϵ-regular pair in G of density ⩾ _d. We shall call_
_regularity_
_R a regularity graph of G with parameters ϵ, ℓ_ and d. Given s _[∈]_ N, let _graph_
us now replace every vertex Vi of R by a set Vi[s] [of][ s][ vertices, and every] _Vi[s]_
edge by a complete bipartite graph between the corresponding s-sets.
The resulting graph will be denoted by Rs. (For R = K _[r], for example,_ _Rs_
we have Rs = Ks[r][.)]
The following lemma says that subgraphs of Rs can also be found
in G, provided that ϵ is small enough and the Vi are large enough. In
fact, the values of ϵ and ℓ required depend only on (d and) the maximum
degree of the subgraph:

**Lemma 7.3.2. For all d** _[∈]_ (0, 1 ] and ∆ ⩾ 1 there exists an ϵ0 > 0 with [ 9.2.2 ]
_the following property: if G is any graph, H is a graph with ∆(H) ⩽_ ∆,
_s_ _[∈]_ N, and R is any regularity graph of G with parameters ϵ ⩽ _ϵ0,_
_ℓ_ ⩾ _s/ϵ0 and d, then_

_H ⊆_ _Rs_ _⇒_ _H ⊆_ _G ._

_Proof . Given d and ∆, choose ϵ0 < d small enough that_ _d, ∆_

∆+ 1

(1) _ϵ0_
(d − _ϵ0)[∆]_ _[ϵ][0][ ⩽]_ [1 ;]

such a choice is possible, since (∆+ 1)ϵ/(d _ϵ)[∆]_ 0 as ϵ 0. Now let _G, H, R, Rs_
_−_ _→_ _→_
_G, H, s and R be given as stated. Let { V0, V1, . . ., Vk } be the ϵ-regular_ _Vi_
partition of G that gave rise to R; thus, ϵ ⩽ _ϵ0, V (R) = { V1, . . ., Vk }_ _ϵ, k, ℓ_


-----

_ui, h_ of Rs (not just isomorphic to one), with vertices u1, . . ., uh say. Each
_σ_ vertex ui lies in one of the s-sets Vj[s] [of][ R][s][; this defines a map][ σ][:][ i][ �→] _[j][.]_
_vi_ Our aim is to define an embedding ui �→ _vi ∈_ _Vσ(i) of H in G; thus,_
_v1, . . ., vh will be distinct, and vivj will be an edge of G whenever uiuj_
is an edge of H.
Our plan is to choose the vertices v1, . . ., vh inductively. Throughout
the induction, we shall have a ‘target set’ Yi _Vσ(i) assigned to each i;_
_⊆_
this contains the vertices that are still candidates for the choice of vi.
Initially, Yi is the entire set Vσ(i). As the embedding proceeds, Yi will
get smaller and smaller (until it collapses to { vi } when vi is chosen):
whenever we choose a vertex vj with j < i and ujui ∈ _E(H), we delete_
all those vertices from Yi that are not adjacent to vj. The set Yi thus
evolves as

_Vσ(i) = Yi[0]_ _[⊇]_ _[. . .][ ⊇]_ _[Y]i[ i]_ [=][ {][ v][i] _[}][,]_

where Yi[j] [denotes the version of][ Y][i][ current after the definition of][ v][j][ (and]
any corresponding deletion of vertices from Yi[j][−][1]).
In order to make this approach work, we have to ensure that the
target sets Yi do not get too small. When we come to embed a vertex uj,
we consider all the indices i > j with ujui ∈ _E(H); there are at most ∆_
such i. For each of these i, we wish to select vj so that

_Yi[j]_ [=][ N] [(][v][j][)][ ∩] _[Y]i[ j][−][1]_ (2)

is large, i.e. not much smaller than Yi[j][−][1]. Now this can be done by
Lemma 7.3.1 (with A = Vσ(j), B = Vσ(i) and Y = Yi[j][−][1]): unless Yi[j][−][1]
is tiny (of size less than ϵℓ), all but at most ϵℓ choices of vj will be such
that (2) implies
_|Yi[j][|][ ⩾]_ [(][d][ −] _[ϵ][)][|][Y]i[ j][−][1]| ._ (3)

Doing this simultaneously for all of the at most ∆values of i considered,
we find that all but at most ∆ϵℓ choices of vj from Vσ(j), and in particular
from Yj[j][−][1] _⊆_ _Vσ(j), satisfy (3) for all i._
It remains to show that the sets Y considered for Lemma 7.3.1 above
are indeed never tiny, and that |Yj[j][−][1]|− ∆ϵℓ ⩾ _s to ensure that a suitable_
choice for vj exists: since σ(j[′]) = σ(j) for at most s − 1 of the vertices
_uj[′] with j[′]_ _< j, a choice between s suitable candidates for vj will suffice_
to keep vj distinct from v1, . . ., vj−1. But all this follows from our choice
of ϵ0. Indeed, the initial target sets Yi[0] have size ℓ, and each Yi has
vertices deleted from it only when some vj with j < i and ujui ∈ _E(H)_
is defined, which happens at most ∆times. Thus,

_|Yi[j][| −]_ [∆][ϵℓ] (3)[⩾] (d − _ϵ)[∆]ℓ_ _−_ ∆ϵℓ ⩾ (d − _ϵ0)[∆]ℓ_ _−_ ∆ϵ0ℓ (1)⩾ _ϵ0ℓ_ ⩾ _s_

whenever j < i, so in particular |Yi[j][|][ ⩾] _[ϵ][0][ℓ]_ [⩾] _[ϵℓ]_ [and][ |][Y]j[ j][−][1]| − ∆ϵℓ ⩾ _s._


-----

We are now ready to prove the Erd˝os-Stone theorem.

(7.1.1)
**Proof of Theorem 7.1.2. Let r ⩾** 2 and s ⩾ 1 be given as in the (7.1.4)
statement of the theorem. For s = 1 the assertion follows from Tur´an’s
_r, s_
theorem, so we assume that s ⩾ 2. Let γ > 0 be given; this γ will play _γ_
the role of the ϵ of the theorem. Let G be a graph with _G_ =: n and
_|_ _|_

_∥G∥_ ⩾ _tr−1(n) + γn[2]._ _∥G∥_

(Thus, γ < 1.) We want to show that Ks[r] _[⊆]_ _[G][ if][ n][ is large enough.]_
Our plan is to use the regularity lemma to show that G has a regularity graph R dense enough to contain a K[r] by Tur´an’s theorem. Then
_Rs contains a Ks[r][, so we may hope to use Lemma 7.3.2 to deduce that]_
_Ks[r]_ _[⊆]_ _[G][.]_
On input d := γ and ∆:= ∆(Ks[r][), Lemma 7.3.2 returns an][ ϵ][0] _[>][ 0;]_ _d, ∆_
since the lemma’s assertion about ϵ0 becomes weaker when ϵ0 is made _ϵ0_
smaller, we may assume that

_ϵ0 < γ/2 < 1 ._ (1)

To apply the regularity lemma, let m > 1/γ and choose ϵ > 0 small
enough that ϵ ⩽ _ϵ0 and_ _m, ϵ_

_δ := 2γ −_ _ϵ[2]_ _−_ 4ϵ − _d −_ [1] _δ_

_m [>][ 0 ;]_


this is possible, since 2γ − _d −_ _m[1]_ _[>][ 0. On input][ ϵ][ and][ m][, the regularity]_

lemma returns an integer M . Let us assume that _M_

_Ms_
_n ⩾_ _n_

_ϵ0(1 −_ _ϵ)_ _[.]_

Since this number is at least m, the regularity lemma provides us with
an ϵ-regular partition { V0, V1, . . ., Vk } of G, where m ⩽ _k ⩽_ _M_ ; let _k_
_|V1| = . . . = |Vk| =: ℓ. Then_ _ℓ_

_n ⩾_ _kℓ,_ (2)


and


_ℓ_ = _[n][ −|][V][0][|]_ ⩾ _[n][ −]_ _[ϵn]_ = n [1][ −] _[ϵ]_ ⩾ _[s]_

_k_ _M_ _M_ _ϵ0_


by the choice of n. Let R be the regularity graph of G with parameters _R_
_ϵ, ℓ, d corresponding to the above partition. Since ϵ ⩽_ _ϵ0 and ℓ_ ⩾ _s/ϵ0, the_
regularity graph R satisfies the premise of Lemma 7.3.2, and by definition


-----

that Ks[r] _[⊆]_ _[G][, all that remains to be checked is that][ K]_ _[r][ ⊆]_ _[R][ (and hence]_
_Ks[r]_ _[⊆]_ _[R][s][).]_
Our plan was to show K _[r]_ _R by Tur´an’s theorem. We thus have to_
_⊆_
check that R has enough edges, i.e. that enough ϵ-regular pairs (Vi, Vj)
have density at least d. This should follow from our assumption that G

this lies substantially above the approximate edge densityhas at least tr−1(n) + γn[2] edges, i.e. an edge density of aboutr−[r]r2[−]−[2]1 [+ 2][γ][:]
Tur´an graph T _[r][−][1](k), and hence substantially above any density thatr−1_ [of the]
_G could have if no more than tr−1(k) of the pairs (Vi, Vj) had density_
⩾ _d—even if all those pairs had density 1!_
Let us then estimate _R_ more precisely. How many edges of G
_∥_ _∥_
lie outside ϵ-regular pairs? At most �|V20|� edges lie inside V0, and by
condition (i) in the definition of ϵ-regularity these are at most [1]2 [(][ϵn][)][2]

edges. At most |V0|kℓ ⩽ _ϵnkℓ_ edges join V0 to other partition sets. The
at most ϵk[2] other pairs (Vi, Vj) that are not ϵ-regular contain at most
_ℓ[2]_ edges each, together at most ϵk[2]ℓ[2]. The ϵ-regular pairs of insufficient
density (< d) each contain no more than dℓ[2] edges, altogether at most
1 �ℓ� edges inside each of the
2 _[k][2][dℓ][2][ edges. Finally, there are at most]_ 2
partition sets V1, . . ., Vk, together at most [1]2 _[ℓ][2][k][ edges. All][ other][ edges]_

of G lie in ϵ-regular pairs of density at least d, and thus contribute to
edges of R. Since each edge of R corresponds to at most ℓ[2] edges of G,
we thus have in total

_∥G∥≤_ 2[1] _[ϵ][2][n][2][ +][ ϵnkℓ]_ [+][ ϵk][2][ℓ][2][ +][ 1]2 _[k][2][dℓ][2][ +][ 1]2_ _[ℓ][2][k][ +][ ∥][R][∥]_ _[ℓ][2][.]_


Hence, for all sufficiently large n,

2 _[ϵ][2][n][2][ −]_ _[ϵnkℓ]_ _[−]_ _[ϵk][2][ℓ][2][ −]_ [1]2 _[dk][2][ℓ][2][ −]_ [1]2 _[kℓ][2]_

_∥R∥≥_ 2[1] _[k][2][ ∥][G][∥−]_ [1] 1

2 _[k][2][ℓ][2]_


�


_≥_
(1,2)

_≥_
(2)


1 � _tr−1(n) + γn2 −_ 12 _[ϵ][2][n][2][ −]_ _[ϵnkℓ]_
2 _[k][2]_ _−_ 2ϵ − _d −_ [1]

_n[2]/2_ _k_


12 _[k][2]�_ _tr−1(n)_ + 2γ − _ϵ[2]_ _−_ 4ϵ − _d −_ [1]

_n[2]/2_ _m_


�


� �n�−1�

= [1]2 _[k][2]_ _tr−1(n)_ 1 − [1]

2 _n_


� �
+ δ


_>_ [1]2 _[k][2][ r][ −]_ [2]

_r_ 1
_−_

⩾ _tr−1(k) ._

(The strict inequality follows from Lemma 7.1.4.) Therefore K _[r]_ _R by_
_⊆_
Theorem 7.1.1, as desired. 

-----

###### Exercises

1.[−] Show that K1,3 is extremal without a P [3].

2.[−] Given k > 0, determine the extremal graphs of chromatic number at
most k.

3. Determine the value of ex(n, K1,r) for all r, n _[∈]_ N.

4. Is there a graph that is edge-maximal without a K [3] minor but not
extremal?

5. Show that, for every forest F, the value of ex(n, F ) is bounded above
by a linear function of n.

6.[+] Given k > 0, determine the extremal graphs without a matching of
size k.

(Hint. Theorem 2.2.3 and Ex. 10, Ch. 2.)

7. Without using Tur´an’s theorem, show that the maximum number of
edges in a triangle-free graph of order n > 1 is ⌊n[2]/4⌋.

8. Show that

_tr−1(n) ⩽_ [1]2 _[n][2][ r][ −]_ [2]

_r −_ 1 _[,]_

with equality whenever r − 1 divides n.

9. Show that tr−1(n)/[�][n]2� converges to (r − 2)/(r − 1) as n →∞.


(Hint. tr−1((r − 1)⌊ _r−n1_ _[⌋][)][ ⩽]_ _[t][r][−][1][(][n][)][ ⩽]_ _[t][r][−][1][(][(][r][ −]_ [1)][⌈] _r−n1_ _[⌉][)][.)]_

10.[+] Given non-adjacent vertices u, v in a graph G, denote by G [ u → _v ] the_
graph obtained from G by first deleting all the edges at u and then
joining u to all the neighbours of v. Show that K _[r]_ _̸⊆_ _G [ u →_ _v ] if_
_K_ _[r]_ _̸⊆_ _G. Applying this operation repeatedly to a given extremal graph_
for n and K _[r], prove that ex(n, K_ _[r]) = tr−1(n): in each iteration step,_
choose u and v so that the number of edges will not decrease, and so
that eventually a complete multipartite graph is obtained.

11. Show that deleting at most (m − _s)(n −_ _t)/s edges from a Km,n will_
never destroy all its Ks,t subgraphs.

12. For 0 < s ⩽ _t ⩽_ _n let z(n, s, t) denote the maximum number of edges in_
a bipartite graph whose partition sets both have size n, and which does
not contain a Ks,t. Show that 2 ex(n, Ks,t) ≤ _z(n, s, t) ≤_ ex(2n, Ks,t).

13.[+] Let 1 ⩽ _r ⩽_ _n be integers. Let G be a bipartite graph with bipartition_
_{ A, B }, where |A| = |B| = n, and assume that Kr,r ̸⊆_ _G. Show that_
� �d(x)� �n�

⩽ (r − 1) _._

_r_ _r_

_x∈A_

Using the previous exercise, deduce that ex(n, Kr,r) ⩽ _cn[2][−][1][/r]_ for some


-----

14. The upper density of an infinite graph G is the infimum of all reals α
such that the finite graphs H ⊆ _G with ∥H∥[�][|][H]2_ _[|]�−1 > α have bounded_
order. Show that this number always takes one of the countably many
values 0, 1, [1]2 _[,][ 2]3_ _[,][ 3]4_ _[, . . .][.]_

(Hint. Erd˝os-Stone.)

15. Prove the following weakening of the Erd˝os-S´os conjecture (stated at
the end of Section 7.1): given integers 2 ⩽ _k < n, every graph with n_
vertices and at least (k − 1)n edges contains every tree with k edges as
a subgraph.

16. Show that, as a general bound for arbitrary n, the bound on ex(n, T )
claimed by the Erd˝os-S´os conjecture is best possible for every tree T .
Is it best possible even for every n and every T ?

17.[−] Prove the Erd˝os-S´os conjecture for the case when the tree considered
is a star.

18. Prove the Erd˝os-S´os conjecture for the case when the tree considered
is a path.

(Hint. Use the result of the next exercise.)

19. Show that every connected graph G contains a path of length at least
min { 2δ(G), |G| − 1 }.

20.[−] In the definition of an ϵ-regular pair, what is the purpose of the requirement that |X| > ϵ |A| and |Y | > ϵ |B|?

21.[−] Show that any ϵ-regular pair in G is also ϵ-regular in G.

22. Prove the regularity lemma for sparse graphs, that is, for every sequence
(Gn)n∈N of graphs Gn of order n such that ∥Gn∥/n[2] _→_ 0 as n →∞.

###### Notes

The standard reference work for results and open problems in extremal graph
theory (in a very broad sense) is still B. Bollob´as, Extremal Graph Theory,
Academic Press 1978. A kind of update on the book is given by its author in
his chapter of the Handbook of Combinatorics (R.L. Graham, M. Gr¨otschel &
L. Lov´asz, eds.), North-Holland 1995. An instructive survey of extremal graph
theory in the narrower sense of our chapter is given by M. Simonovits in
(L.W. Beineke & R.J. Wilson, eds.) Selected Topics in Graph Theory 2, Academic Press 1983. This paper focuses among other things on the particular
role played by the Tur´an graphs. A more recent survey by the same author
can be found in (R.L. Graham & J. Neˇsetˇril, eds.) The Mathematics of Paul
_Erd˝os, Vol. 2, Springer 1996._
Tur´an’s theorem is not merely one extremal result among others: it is
the result that sparked off the entire line of research. Our proof of Tur´an’s
theorem is essentially the original one; the proof indicated in Exercise 10 is


-----

Our version of the Erd˝os-Stone theorem is a slight simplification of the
original. A direct proof, not using the regularity lemma, is given in L. Lov´asz,
_Combinatorial Problems and Exercises (2nd edn.), North-Holland 1993. Its_
most fundamental application, Corollary 7.1.3, was only found 20 years after
the theorem, by Erd˝os and Simonovits (1966).
Of our two bounds on ex(n, Kr,r) the upper one is thought to give the
correct order of magnitude. For vastly off-diagonal complete bipartite graphs
this was verified by J. Koll´ar, L. R´onyai & T. Szab´o, Norm-graphs and bipartite Tur´an numbers, Combinatorica 16 (1996), 399–406, who proved that
ex(n, Kr,s) ⩾ _crn[2][−]_ _r[1] when s > r! ._

Details about the Erd˝os-S´os conjecture, including an approximate solution for large k, can be found in the survey by Koml´os and Simonovits cited
below. The case where the tree T is a path (Exercise 18) was proved by
Erd˝os & Gallai in 1959. It was this result, together with the easy case of stars
(Exercise 17) at the other extreme, that inspired the conjecture as a possible
unifying result.
The regularity lemma is proved in E. Szemer´edi, Regular partitions of
graphs, Colloques Internationaux CNRS 260—Probl`emes Combinatoires et
_Th´eorie des Graphes, Orsay (1976), 399–401. Our rendering follows an ac-_
count by Scott (personal communication). A broad survey on the regularity lemma and its applications is given by J. Koml´os & M. Simonovits in
(D. Mikl´os, V.T. S´os & T. Sz˝onyi, eds.) Paul Erd˝os is 80, Vol. 2, Proc. Colloq.
Math. Soc. J´anos Bolyai (1996); the concept of a regularity graph and Lemma 7.3.2 are taken from this paper. An adaptation of the regularity lemma
for use with sparse graphs was developed independently by Kohayakawa and
by R¨odl; see Y. Kohayakawa, Szemer´edi’s regularity lemma for sparse graphs,
in (F. Cucker & M. Shub, eds.) Foundations of Computational Mathematics,
Selected papers of a conference held at IMPA in Rio de Janeiro, January 1997,
Springer 1997.


-----

-----

# 8 Substructures in
### Sparse Graphs

In this chapter we study how global assumptions about a graph—on its
average degree, chromatic number, or even (large) girth—can force it to
contain a given graph H as a minor or topological minor. As we know
already from Mader’s theorem 3.6.1, there exists a function h such that
an average degree of d(G) ⩾ _h(r) suffices to create a TK_ _[r]_ subgraph
in G, and hence a (topological) H minor if r ⩾ _|H|._ Since a graph
with n vertices and average degree d has [1]2 _[dn][ edges this shows that, for]_

every H, there is a ‘constant’ c (depending on H but not on n) such
that a topological H minor occurs in every graph with n vertices and
at least cn edges. Such graphs with a number of edges about linear[1] in
their order are called sparse—so this is a chapter about substructures in _sparse_
sparse graphs.
The first question, then, will be the analogue of Tur´an’s theorem:
given a positive integer r, what is the minimum value of the above ‘constant’ c for H = K[r], i.e. the smallest growth rate of a function h(r) as
in Theorem 3.6.1? This was a major open problem until very recently;
we present its solution, which builds on some fascinating methods the
problem has inspired over time, in Section 8.1.
If raising the average degree suffices to force the occurrence of a
certain minor, then so does raising any other invariant which in turn
forces up the average degree. For example, if d(G) ⩾ _c implies H ≼_ _G,_
then so will χ(G) ⩾ _c + 1 (by Corollary 5.2.3). However, is this best_
possible? Even if the value of c above is least possible for d(G) ⩾ _c to_
imply H ≼ _G, it need not be so for χ(G) ⩾_ _c + 1 to imply H ≼_ _G. One_
of the most famous conjectures in graph theory, the Hadwiger conjecture,


-----

suggests that there is indeed a gap here: while a value of c = c[′]r[√]log r
(where c[′] is independent of both n and r) is best possible for d(G) ⩾ _c_
to imply H ≼ _G (Section 8.2), the conjecture says that χ(G) ⩾_ _r will_
do the same! Thus, if true, then Hadwiger’s conjecture shows that the
effect of a large chromatic number on the occurrence of minors somehow
goes beyond that part which is well-understood: its effect via mere edge
density. We shall consider Hadwiger’s conjecture in Section 8.3.

###### 8.1 Topological minors

In this section we prove that an average degree of cr[2] suffices to force
the occurrence of a topological K _[r]_ minor in a graph; complete bipartite
graphs show that, up to the constant c, this is best possible (Exercise 5).
The following theorem was proved independently around 1996 by
Bollob´as & Thomason and by Koml´os & Szemer´edi.

**Theorem 8.1.1. There exists a c ∈** R such that, for every r ∈ N, every
_graph G of average degree d(G) ⩾_ _cr[2]_ _contains K_ _[r]_ _as a topological_
_minor._

The proof of this theorem, in which we follow Bollob´as & Thomason,
will occupy us for the remainder of this section. A set U _V (G) will_
_⊆_
_linked_ be called linked (in G) if for any distinct vertices u1, . . ., u2h ∈ _U there_
are h disjoint paths Pi = u2i−1 . . . u2i in G, i = 1, . . ., h.[2] The graph G
(k, ℓ)-linked itself is (k, ℓ)-linked if every k-set of its vertices contains a linked ℓ-set.
How can we hope to find the TK _[r]_ in G claimed to exist by Theorem 8.1.1? Our basic approach will be to identify first some r-set X
as a set of branch vertices, and to choose for each x ∈ _X a set Yx of_
_r_ 1 neighbours, one for every edge incident with x in the K _[r]. If the_
_−_
constant c from the theorem is large enough, the r + r(r 1) = r[2]
_−_

vertices of X ∪ [�] _Yx can be chosen distinct: by Proposition 1.2.2, G has_
a subgraph of minimum degree at least ε(G) = 12 _[d][(][G][)][ ⩾]_ 12 _[cr][2][, so we]_
can choose X and its neighbours inside this subgraph. Having fixed X
and the sets Yx, we then have to link up the correct pairs of vertices in
_Y :=_ [�] _Yx by disjoint paths in G −_ _X, to obtain the desired TK_ _[r]._
This would be possible at once if Y were linked in G _X. Unfortu-_
_−_
nately, this is unrealistic to hope for: no average degree, however large,
will force every r(r 1)-set to be linked. (Why not?) However, if we
_−_
pick for X significantly more than the r vertices needed eventually, and
for each x ∈ _X significantly more than r −_ 1 neighbours as Yx, then Y
might become so large that the high average degree of G guarantees the

2 Thus, in a k-linked graph—see Chapter 3.6—every set of up to 2k + 1 vertices


-----

existence of some large linked subset Z _Y . This would be the case if_
_⊆_
_G were (k, ℓ)-linked for some k ⩽_ _|Y | and ℓ_ ⩾ _|Z|._
As above, a large enough constant c will easily ensure that X and Y
can be chosen with many vertices to spare. Another problem, however,
is more serious: it will not be enough to make ℓ (and hence Z) large in
absolute terms. Indeed, if k (and Y ) is much larger still, it might happen
that Z, although large, consists of neighbours of only a few vertices in X!
We thus have to ensure that ℓ is large also relative to k. This will be the
purpose of our first lemma (8.1.2): it establishes a sufficient condition
for G to be (k, _k/2_ )-linked.
_⌈_ _⌉_
What is this sufficient condition? It is the assumption that G has a
particularly dense minor H, one whose minimum degree exceeds [1]2 _[|][H][|]_

by a positive fraction of k. (In particular, H will be dense in the sense
of Chapter 7.) In view of Theorem 3.6.2, it is not surprising that such
a dense graph H is highly linked. Given sufficiently high connectivity
of G (which again follows easily if c is large enough), we may then try
to link up the vertices of any Y as above to distinct branch sets of H by
disjoint paths in G avoiding most of the other branch sets, and thus to
transfer the linking properties of H to a _k/2_ -set Z _Y (Fig. 8.1.1)._
_⌈_ _⌉_ _⊆_


_X_


_x1_ _x2_ _x3_

|Z|Col2|Col3|
|---|---|---|
||||
||||


_Fig. 8.1.1. Finding a TK_ [3] in G with branch vertices x1, x2, x3

What is all the more surprising, however, is that the existence of
such a dense minor H can be deduced from our assumption of d(G) ⩾ _cr[2]._
This will be shown in another lemma (8.1.3); the assertion of the theorem
itself will then follow easily.

**Lemma 8.1.2. If G is k-connected and has a minor H with 2δ(H) ⩾**


-----

(3.3.1) _Proof ._ Let V := { Vx | x _[∈]_ _V (H) } be the set of branch sets in G_

_V, Vx_ corresponding to the vertices of H. For our proof that G is (k, _k/2_ )_⌈_ _⌉_
_v1, . . ., vk_ linked, let k distinct vertices v1, . . ., vk _∈_ _G be given._ Let us call a
_linkage_ sequence P1, . . ., Pk of disjoint paths in G a linkage if the Pi each start
in vi and end in pairwise distinct sets V ∈ _V; the paths Pi themselves will_
_link_ be called links. Since our assumptions about H imply that |H| ⩾ _k, and_
_G is k-connected, such linkages exist: just pick k vertices from pairwise_
distinct sets V _[∈]_ _V, and link them disjointly to { v1, . . ., vk } by Menger’s_
theorem.
_P_ Now let P = (P1, . . ., Pk) be a linkage whose total number of edges

_P1, . . ., Pk_ outside [�]V ∈V _[G][ [][ V][ ] is as small as possible. Thus, if][ f]_ [(][P] [) denotes the]
_f_ (P ) number of edges of P not lying in any G [ Vx ], we choose P so as to
minimize [�]i[k]=1 _[f]_ [(][P][i][). Then for every][ V] _∈_ _V that meets a path Pi ∈_ _P_
there exists one such path that ends in V : if not, we could terminate Pi
in V and reduce f (Pi). Thus, exactly k of the branch sets of H meet a
link. Let us divide these sets into two classes:


_U_

_W_


_U := { V ∈_ _V | V meets exactly one link }_
_W := { V_ _[∈]_ _V | V meets more than one link } ._

Since H is dense and each U ∈ _U meets only one link, it will be easy to_
show that the starting vertices vi of those links form a linked set in G.
Hence, our aim is to show that |U| ⩾ _⌈k/2⌉, i.e. that U is no smaller_
than . (Recall that + = k.) To this end, we first prove the
_W_ _|U|_ _|W|_
following:

_Every V_ _∈_ _W is met by some link which leaves V again_ (1)
_and next meets a set from_ _(where it ends)._
_U_


_x_ Suppose Vx _[∈]_ _W is a counterexample to (1). Since_

2δ(H) ⩾ _|H| +_ [3]2 _[k][ ⩾]_ _[δ][(][H][) +][ 3]2_ _[k,]_


we have δ(H) ⩾ [3]2 _[k][. As][ |U ∪W|][ =][ k][, this implies that][ x][ has a neighbour]_

_y in H with Vy ∈_ _V ∖_ (U ∪W); let wxwy be an edge of G with wx ∈ _Vx_
and wy ∈ _Vy. Let Q = w . . . wxwy be a path in G [ Vx ∪{ wy } ] of whose_
_Pi_ vertices only w lies on any link, say on Pi (Fig. 8.1.2). Replacing Pi in
_Pi[′]_ _P by Pi[′]_ [:=][ P][i][wQ][ then yields another linkage.]
If Pi is not the link ending in Vx, then f (Pi[′][)][ ⩽] _[f]_ [(][P][i][). The choice]
of P then implies that f (Pi[′][) =][ f] [(][P][i][), i.e. that][ P][i][ ends in the branch set]
_W it enters immediately after Vx. Since Vx is a counterexample to (1)_
we have W /[∈] _U, i.e. W_ _[∈]_ _W. Let P ̸= Pi be another link meeting W_ .
Then P does not end in W (because Pi ends there); let P _[′]_ _⊆_ _P be the_
(minimal) initial segment of P that ends in W . If we now replace Pi and


-----

_P_ _[′]_ _W_ _[∈]_ _W_

_Fig. 8.1.2. If Pi does not end in Vx, we replace Pi and P by Pi[′]_
and P _[′]_

We now assume that Pi does end in Vx; then f (Pi[′][) =][ f] [(][P][i][) + 1.]
As Vx ∈ _W, there exists a link Pj that meets Vx and leaves it again; let_
_Pj[′]_ [be the initial segment of][ P][j][ ending in][ V][x][ (Fig 8.1.3). Then][ f] [(][P][ ′]j[)][ ⩽]
_f_ (Pj) − 1. In fact, since replacing Pi and Pj with Pi[′] [and][ P]j[ ′] [in][ P][ yields]
another linkage, the choice of P implies that f (Pj[′][) =][ f] [(][P][j][)][ −] [1, so][ P][j]
ends in the branch set W it enters immediately after Vx. Then W _[∈]_ _W_
as before, so we may define P and P _[′]_ as before. Replacing Pi, Pj and P
by Pi[′][,][ P]j[ ′] [and][ P][ ′][ in][ P][, we finally obtain a linkage that contradicts the]
choice of . This completes the proof of (1).
_P_

_Vy_ _[∈]_ _V ∖_ (U ∪W)

_Vx_ _[∈]_ _W_

_wy_

_Pi[′]_

_Pi_

_w_ _Pi_

_Pj[′]_
_Pj_
_P_

##### H

_P_ _[′]_ _W_ _[∈]_ _W_

_Fig. 8.1.3. If Pi ends in Vx, we replace Pi, Pj, P by Pi[′][, P][ ′]j_ _[, P][ ′]_

With the help of (1) we may define an injection as follows:
_W →U_
given W _[∈]_ _W, choose a link that passes through W and next meets a_
set U _∈_ _U, and map W �→_ _U_ . (This is indeed an injection, because
different links end in different branch sets.) Thus |U| ⩾ _|W|, and hence_
_|U| ⩾_ _⌈k/2⌉._
Let us assume the enumeration of v1, . . ., vk to be such that the
( )


-----

_|H|_ + [3]2 _[k][, we can find for any two sets][ V][x][, V][y][ ∈]_ _[U][ at least][ 3]2_ _[k][ sets][ V][z][ such]_

that xz, yz _[∈]_ _E(H). At least k/2 of these sets Vz do not lie in U ∪W._
Thus whenever U1, . . ., U2h are distinct sets in U (so h ⩽ _u/2 ⩽_ _k/2), we_
may find inductively h distinct sets V _[i][ ∈]_ _V ∖_ (U ∪W) (i = 1, . . ., h) such
that V _[i]_ is joined in G to both U2i−1 and U2i. For each i, any vertex of
_U2i−1 can be linked by a path through V_ _[i]_ to any desired vertex of U2i,
and these paths will be disjoint for different i. Joining up the appropriate
pairs of paths from P in this way, we see that the set { v1, . . ., vu } is
linked in G, and the lemma is proved. 
**Lemma 8.1.3. Let k ⩾** 6 be an integer. _Then every graph G with_
_ε(G) ⩾_ _k has a minor H such that 2δ(H) ⩾_ _|H| +_ [1]6 _[k][.]_


_G0_ _Proof ._ We begin by choosing a (≼-)minimal minor G0 of G with
_ε(G0) ⩾_ _k. The minimality of G0 implies that δ(G0) > k and ε(G0) = k_
(otherwise we could delete a vertex or an edge of G0), and hence

_k + 1 ⩽_ _δ(G0) ⩽_ _d(G0) = 2k ._


_x0_ Let x0 _[∈]_ _G0 be a vertex of minimum degree._
If k is odd, let m := (k + 1)/2 and

_G1 := G0 [ { x0 } ∪_ _NG0(x0) ] ._


Then |G1| = δ(G0) + 1 ⩽ 2k + 1 ⩽ 2(k + 1) = 4m. By the minimality of G0, contracting any edge x0y of G0 will result in the loss of at
least k + 1 edges. The vertices x0 and y thus have at least k common
neighbours, so δ(G1) ⩾ _k + 1 = 2m (Fig. 8.1.4)._

_y_


⩾ _k_


_x0_


_NG0_ (x0)

_Fig. 8.1.4. The graph G1 ≼_ _G: a first approximation to the_
desired minor H


If k is even, we let m := k/2 and

_G1 := G0 [ NG0(x0) ] ._


-----

Thus in either case we have found an integer m ⩾ _k/2 and a graph_ _m_
_G1 ≼_ _G such that_ _G1_
_|G1| ⩽_ 4m (1)

and δ(G1) ⩾ 2m, so

_ε(G1) ⩾_ _m ⩾_ _k/2 ⩾_ 3 . (2)

As 2δ(G1) ⩾ 4m ⩾ _|G1|, our graph G1 is already quite a good_
candidate for the desired minor H of G. In order to jack up its value
of 2δ by another 16 _[k][ (as required for][ H][), we shall reapply the above]_
contraction process to G1, and a little more rigorously than before: step
by step, we shall contract edges as long as this results in a loss of no
more than [7]

6 _[m][ edges per vertex. In other words, we permit a loss of edges]_
slightly greater than maintaining ε ⩾ _m seems to allow. (Recall that,_
when we contracted G to G0, we put this threshold at ε(G) = k.) If this
second contraction process terminates with a non-empty graph H0, then
_ε(H0) will be at least_ [7]6 _[m][, higher than for][ G][1][! The][ 1]6_ _[m][ thus gained will]_

suffice to give the graph H1, obtained from H0 just as G1 was obtained
from G0, the desired high minimum degree.
But how can we be sure that this second contraction process will
indeed end with a non-empty graph? Paradoxical though it may seem,
the reason is that even a permitted loss of up to 7
6 _[m][ edges (and one]_
vertex) per contraction step cannot destroy the m |G1| or more edges
of G1 in the |G1| steps possible: the graphs with fewer than m vertices
towards the end of the process would simply be too small to be able to
shed their allowance of [7]

6 _[m][ edges—and, by (1), these small graphs would]_
account for about a quarter of the process!
Formally, we shall control the graphs H in the contraction process
not by specifying an upper bound on the number of edges to be discarded
at each step, but by fixing a lower bound for _H_ in terms of _H_ . This
_∥_ _∥_ _|_ _|_
bound grows linearly from a value of just above �m2 � for |H| = m to a
value of less than 4m[2] for |H| = 4m. By (1) and (2), H = G1 will satisfy
this bound, but clearly it cannot be satisfied by any H with _H_ = m;
_|_ _|_
so the contraction process must stop somewhere earlier with _H_ _> m._
_|_ _|_
To implement this approach, let


_f_ (n) := [1]6 _[m][(][n][ −]_ _[m][ −]_ [5)] _f_

and

_H :=_ �H ≼ _G1 : ∥H∥_ ⩾ _m |H| + f_ (|H|) − �m2 �[�] _._ _H_

By (1),


_f_ (|G1|) ⩽ _f_ (4m) = [1]2 _[m][2][ −]_ [5]6 _[m <]_ �m2 � _,_


-----

For every H _[∈]_ _H, any graph obtained from H by one of the following_
three operations will again be in :
_H_

(i) deletion of an edge, if ∥H∥ ⩾ _m |H| + f_ (|H|) − �m2 � + 1;

(ii) deletion of a vertex of degree at most [7]

6 _[m][;]_

(iii) contraction of an edge xy _[∈]_ _H such that x and y have at most_
7
6 _[m][ −]_ [1 common neighbours in][ H][.]

Starting with G1, let us apply these operations as often as possible, and
_H0_ let H0 ∈ _H be the graph obtained eventually. Since_

_∥K_ _[m]∥_ = m |K _[m]| −_ _m −_ �m2 �

and

_f_ (m) = − 6[5] _[m >][ −][m,]_

_K_ _[m]_ does not have enough edges to be in ; thus, contains no graph
_H_ _H_
_x1_ on m vertices. Hence |H0| > m, and in particular H0 ̸= ∅. Let x1 ∈ _H0_
be a vertex of minimum degree, and put

_H1_ _H1 := H0 [ { x1 } ∪_ _NH0(x1) ] ._

We shall prove that the minimum degree of H := H1 is as large as
claimed in the lemma.
Note first that

_δ(H1) >_ [7]6 _[m .]_ (3)

Indeed, since H0 is minimal with respect to (ii) and (iii), we have d(x1) >
7
6 _[m][ in][ H][0][ (and hence in][ H][1][), and every vertex][ y][ ̸][=][ x][1][ of][ H][1][ has more]_
than 7 7
6 _[m][ −]_ [1 common neighbours with][ x][1][ (and hence more than] 6 _[m]_
neighbours in H1 altogether). In order to convert (3) into the desired
inequality of the form

2δ(H1) ⩾ _|H1| + αm,_

we need an upper bound for |H1| in terms of m. Since H0 lies in H but
is minimal with respect to (i), we have


_∥H0∥_ _< m |H0| +_ � 16 _[m][ |][H][0][| −]_ [1]6 _[m][2][ −]_ [5]6 _[m]�_ _−_ �m2 � + 1

= [7]

6 _[m][ |][H][0][| −]_ [4]6 _[m][2][ −]_ [1]3 _[m][ + 1]_


⩽ [7] _m |H |_ 4 _m2_ (4)


-----

By the choice of x1 and definition of H1, therefore,

_|H1| −_ 1 = δ(H0)

⩽ 2 ε(H0)


_<_
(4)

⩽
(1)


7
3 _[m][ −]_ [4]3 _[m][2][/][|][H][0][|]_

7
3 _[m][ −]_ [1]3 _[m]_


so |H1| ⩽ 2m. Hence,


= 2m,

2δ(H1) > 3 _[m]_
(3) [2][m][ +][ 1]


⩾ _|H1| +_ [1]3 _[m]_

⩾ _|H1| +_ [1]6 _[k]_
(2)

as claimed. 
**Proof of Theorem 8.1.1. We prove the assertion for c := 1116. Let** (1.4.2)
_G be a graph with d(G) ⩾_ 1116r[2]. By Theorem 1.4.2, G has a subgraph
_G0 such that_ _G0_
_κ(G0) ⩾_ 279r[2] ⩾ 276r[2] + 3r .

Pick a set X := { x1, . . ., x3r } of 3r vertices in G0, and let G1 := G0 − _X._ _X_
For each i = 1, . . ., 3r choose a set Yi of 5r neighbours of xi in G1; let _G1, Yi_
these sets Yi be disjoint for different i. (This is possible since δ(G0) ⩾
_κ(G0) ⩾_ 15r[2] + |X|.)
As

_δ(G1) ⩾_ _κ(G1) ⩾_ _κ(G0) −|X| ⩾_ 276r[2],

we have ε(G1) ⩾ 138r[2]. By Lemma 8.1.3, G1 has a minor H with
2δ(H) ⩾ _|H| + 23r[2]_ and is therefore (15r[2], 7r[2])-linked by Lemma 8.1.2;
let Z ⊆ [�]i[3]=1[r] _[Y][i][ be a set of 7][r][2][ vertices that is linked in][ G][1][.]_ _Z_
For all i = 1, . . ., 3r let Zi := Z ∩ _Yi. Since Z is linked, it suffices_ _Zi_
to find r indices i with |Zi| ⩾ _r −_ 1: then the corresponding xi will be
the branch vertices of a TK _[r]_ in G0. If r such i cannot be found, then
_|Zi| ⩽_ _r −_ 2 for all but at most r − 1 indices i. But then


_Z_ =
_|_ _|_


3r
�

_|Zi| ⩽_ (r − 1) 5r + (2r + 1)(r − 2) < 7r[2] = |Z|,
_i=1_


-----

Although Theorem 8.1.1 already gives a good estimate, it seems
very difficult to determine the exact average degree needed to force a
_TK_ _[r]_ subgraph, even for small r. We shall come back to the case of
_r = 5 in Section 8.3; more results and conjectures are given in the notes._

The following almost counter-intuitive result of Mader implies that
the existence of a topological K _[r]_ minor can be forced essentially by large
girth. In the next section, we shall prove the analogue of this for ordinary
minors.

**Theorem 8.1.4. (Mader 1997)**
_For every graph H of maximum degree d ⩾_ 3 there exists an integer k
_such that every graph G of minimum degree at least d and girth at least k_
_contains H as a topological minor._

As discussed already in Chapter 5.2 and the introduction to Chapter 7, no constant average degree, however large, will force an arbitrary
graph to contain a given graph H as a subgraph—as long as H contains
at least one cycle. By Proposition 1.2.2 and Corollary 1.5.4, on the other
hand, any graph G contains all trees on up to ε(G) + 2 vertices. Large
average degree therefore does ensure the occurrence of any fixed tree T
as a subgraph. What can we say, however, if we would like T to occur
as an induced subgraph?
Here, a large average degree appears to do as much harm as good,
even for graphs of bounded clique number. (Consider, for example,
complete bipartite graphs.) It is all the more remarkable, then, that
the assumption of a large chromatic number rather than a large average
degree seems to make a difference here: according to a conjecture of
Gy´arf´as, any graph of large enough chromatic number contains either a
large complete graph or any given tree as an induced subgraph. (Formally: for every integer r and every tree T, there exists an integer k such
that every graph G with χ(G) ⩾ _k and ω(G) < r contains an induced_
copy of T .)
The weaker topological version of this is indeed true:

**Theorem 8.1.5. (Scott 1997)**
_For every integer r and every tree T there exists an integer k such that_
_every graph with χ(G) ⩾_ _k and ω(G) < r contains an induced copy of_
_some subdivision of T_ _._


-----

###### 8.2 Minors

According to Theorem 8.1.1, an average degree of cr[2] suffices to force the
existence of a topological K _[r]_ minor in a given graph. If we are content
with any minor, topological or not, an even smaller average degree will
do: in a pioneering paper of 1968, Mader proved that every graph with an
average degree of at least cr log r has a K _[r]_ minor. The following result,
the analogue to Theorems 7.1.1 and 8.1.1 for general minors, determines
the precise average degree needed as a function of r, up to a constant c:

**Theorem 8.2.1. (Kostochka 1982; Thomason 1984)**
_There exists a c_ _[∈]_ R such that, for every r _[∈]_ N, every graph G of average
_degree d(G) ⩾_ _c r[√]log r has a K_ _[r]_ _minor. Up to the value of c, this_
_bound is best possible as a function of r._

The easier implication of the theorem, the fact that in general an average
degree of c r[√]log r is needed to force a K _[r]_ minor, follows from considering random graphs, to be introduced in Chapter 11. The converse implication, the fact that this average degree suffices, is proved by methods
similar to those described in Section 8.1.
Rather than proving Theorem 8.2.1, we therefore devote the remainder of this section to another striking result on forcing minors. At first
glance, this result is so surprising that it seems almost paradoxical: as
long as we do not merely subdivide edges, we can force a K _[r]_ minor in a
graph simply by raising its girth (Corollary 8.2.3)!

**Theorem 8.2.2. (Thomassen 1983)**
_Given an integer k, every graph G with girth g(G) ⩾_ 4k − 3 and δ(G) ⩾ 3
_has a minor H with δ(H) ⩾_ _k._

_Proof . As δ(G) ⩾_ 3, every component of G contains a cycle. In particu- (1.5.3)
lar, the assertion is trivial for k ⩽ 2; so let k ⩾ 3. Consider the vertex
set V of a component of G, together with a partition { V1, . . ., Vm } of _V, Vi_
_V into as many connected sets Vi with at least 2k −_ 2 vertices each as _m_
possible. (Such a partition exists, since |V | ⩾ _g(G) > 2k −_ 2 and V is
connected in G.)
We first show that every G [ Vi ] is a tree. To this end, let Ti be a
spanning tree of G [ Vi ]. If G [ Vi ] has an edge e /[∈] _Ti, then Ti +_ _e contains_
a cycle C; by assumption, C has length at least 4k 3. The edge (about)
_−_
opposite e on C therefore separates the path C − _e, and hence also Ti,_
into two components with at least 2k 2 vertices each. Together with
_−_
the sets Vj for j ̸= i, these two components form a partition of V into
_m + 1 sets that contradicts the maximality of m._
So each G [ Vi ] is indeed a tree, i.e. G [ Vi ] = Ti. As δ(G) ⩾ 3, the _Ti_
degrees in G of the vertices in Vi sum to at least 3 |Vi|, while the edges


-----

at least |Vi| + 2 ⩾ 2k edges joining Vi to V ∖ _Vi. We shall prove that_
every Vi sends at most two edges to each of the other Vj; then Vi must
send edges to at least k of those Vj, so the Vi are the branch sets of an
_MH ⊆_ _G with δ(H) ⩾_ _k._
Suppose, without loss of generality, that G has three V1–V2 edges.
Then there are vertices v1 ∈ _V1 and v2 ∈_ _V2 such that G [ V1 ∪_ _V2 ] contains_
three independent v1–v2 paths P1, P2, P3 (Fig. 8.2.1). At most one of

_P1_

_P1[′]_

_P2[′]_ _P2_

_v1_
_v2_

_P3[′]_

_V1_ _P3_ _V2_

_Fig. 8.2.1. Three edges between V1 and V2_

these paths can be shorter than [1]

2 _[g][(][G][). We assume that][ P][1][ has length]_
at least ⌈ 2[1] _[g][(][G][)][⌉]_ [⩾] [2][k][ −] [1 and let][ P][ ′]1 [:= ˚]P1; then |P1[′][|][ ⩾] [2][k][ −] [2. Since]

_P2 ∪_ _P3 is a cycle of length at least 4k −_ 3, we can further find disjoint
paths P2[′][, P]3[ ′] _[⊆]_ _[P][2]_ _[∪]_ _[P][3]_ [with 2][k][ −] [2 vertices each. Since][ G][ [][ V][1] _[∪]_ _[V][2]_ [] is]
connected, there exists a partition of V1 _V2 into three connected sets_
_∪_
_V1[′][, V]2[ ′][, V][ ′]3_ [such that][ V][ (][P]i[ ′][)][ ⊆] _[V][ ′]i_ [for][ i][ = 1][,][ 2][,][ 3. Replacing the two sets]
_V1, V2 in our partition of V with the three sets V1[′][, V]2[ ′][, V][ ′]3_ [, we obtain a]
partition of V that contradicts the maximality of m. 

The following combination of Theorems 8.2.1 and 8.2.2 brings out
the paradoxical character of the latter particularly well:

**Corollary 8.2.3. There exists a c ∈** R such that, for every r ∈ N, every
_graph G with girth g(G) ⩾_ _c r[√]log r and δ(G) ⩾_ 3 has a K _[r]_ _minor._

_Proof . We prove the corollary for c := 4c[′], where c[′]_ is the constant from
Theorem 8.2.1. Let G be given as stated. By Theorem 8.2.2, G has a
minor H with δ(H) ⩾ _c[′]r[√]log r. By Theorem 8.2.1, H (and hence G)_
has a K _[r]_ minor. 

-----

###### 8.3 Hadwiger’s conjecture

As we saw in the preceding two sections, an average degree of c r[√]log r
suffices to force an arbitrary graph to have a K _[r]_ minor, and an average
degree of cr[2] forces it to have a topological K _[r]_ minor. If we replace
‘average degree’ above with ‘chromatic number’ then, with almost the
same constants c, the two assertions remain true: this is because every
graph with chromatic number k has a subgraph of average degree at
least k 1 (Corollary 5.2.3).
_−_
Although both functions above, c r[√]log r and cr[2], are best possible
(up to the constant c) for the said implications with ‘average degree’,
the question arises whether they are still best possible with ‘chromatic number’—or whether some slower-growing function would do in that
case. What is lurking behind this problem about growth rates, of course,
is a fundamental question about the nature of the invariant χ: can this
invariant have some direct structural effect on a graph in terms of forcing
concrete substructures, or is its effect no greater than that of the ‘unstructural’ property of having lots of edges somewhere, which it implies
trivially?
Neither for general nor for topological minors is the answer to this
question known. For general minors, however, the following conjecture
of Hadwiger suggests a positive answer; the conjecture is considered by
many as one of the deepest open problems in graph theory.

**Conjecture. (Hadwiger 1943)**
_The following implication holds for every integer r > 0 and every_
_graph G:_

_χ(G) ⩾_ _r_ _⇒_ _G ≽_ _K_ _[r]._

Hadwiger’s conjecture is trivial for r ⩽ 2, easy for r = 3 and r = 4
(exercises), and equivalent to the four colour theorem for r = 5 and
_r = 6. For r ⩾_ 7, the conjecture is open. Rephrased as G ≽ _K_ _[χ][(][G][)], it is_
true for almost all graphs.[3] In general, the conjecture for r + 1 implies
it for r (exercise).

The Hadwiger conjecture for any fixed r is equivalent to the assertion that every graph without a K _[r]_ minor has an (r 1)-colouring. In
_−_
this reformulation, the conjecture raises the question of what the graphs
without a K _[r]_ minor look like: any sufficiently detailed structural description of those graphs should enable us to decide whether or not they
can be (r 1)-coloured.
_−_
For r = 3, for example, the graphs without a K _[r]_ minor are precisely
the forests (why?), and these are indeed 2-colourable. For r = 4, there


-----

is also a simple structural characterization of the graphs without a K _[r]_

minor:

[ 12.4.2 ] **Proposition 8.3.1. A graph with at least three vertices is edge-maximal**
_without a K_ [4] _minor if and only if it can be constructed recursively from_
_triangles by pasting_ [4] _along K_ [2]s.

(1.7.2)
_Proof . Recall first that every MK_ [4] contains a TK [4], because ∆(K [4]) = 3
(4.4.4)
(Proposition 1.7.2); the graphs without a K [4] minor thus coincide with
those without a topological K [4] minor. The proof that any graph constructible as described is edge-maximal without a K [4] minor is left as an
easy exercise; in order to deduce Hadwiger’s conjecture for r = 4, we
only need the converse implication anyhow. We prove this by induction
on _G_ .
_|_ _|_
Let G be given, edge-maximal without a K [4] minor. If _G_ = 3 then
_|_ _|_
_G is itself a triangle, so let |G| ⩾_ 4 for the induction step. Then G is
not complete; let S _V (G) be a separating set with_ _S_ = κ(G), and let
_⊆_ _|_ _|_
_C1, C2 be distinct components of G_ _−_ _S. Since S is a minimal separator,_
every vertex in S has a neighbour in C1 and another in C2. If |S| ⩾ 3,
this implies that G contains three independent paths P1, P2, P3 between
a vertex v1 ∈ _C1 and a vertex v2 ∈_ _C2. Since κ(G) = |S| ⩾_ 3, the graph
_G −{ v1, v2 } is connected and contains a (shortest) path P between two_
different Pi. Then P ∪ _P1 ∪_ _P2 ∪_ _P3 = TK_ [4], a contradiction.
Hence κ(G) ⩽ 2, and the assertion follows from Lemma 4.4.4[5] and
the induction hypothesis.       
One of the interesting consequences of Proposition 8.3.1 is that all
the edge-maximal graphs without a K [4] minor have the same number of
edges, and are thus all ‘extremal’:

**Corollary 8.3.2. Every edge-maximal graph G without a K[4]** _minor_
_has 2_ _G_ 3 edges.
_|_ _| −_

_Proof . Induction on |G|._       
**Corollary 8.3.3. Hadwiger’s conjecture holds for r = 4.**

_Proof . If G arises from G1 and G2 by pasting along a complete graph,_
then χ(G) = max { χ(G1), χ(G2) } (see the proof of Proposition 5.5.2).
Hence, Proposition 8.3.1 implies by induction on _G_ that all edge-maxi_|_ _|_
mal (and hence all) graphs without a K [4] minor can be 3-coloured.      
4 This was defined formally in Chapter 5.5.
5 The proof of this lemma is elementary and can be read independently of the


-----

It is also possible to prove Corollary 8.3.3 by a simple direct argument
(Exercise 13).

By the four colour theorem, Hadwiger’s conjecture for r = 5 follows
from the following structure theorem for the graphs without a K [5] minor,
just as it follows from Proposition 8.3.1 for r = 4. The proof of Theorem
8.3.4 is similar to that of Proposition 8.3.1, but considerably longer. We
therefore state the theorem without proof:

**Theorem 8.3.4. (Wagner 1937)**
_Let G be an edge-maximal graph without a K_ [5] _minor. If |G| ⩾_ 4 then
_G can be constructed recursively, by pasting along triangles and K_ [2]s,
_from plane triangulations and copies of the graph W (Fig. 8.3.1)._

= =

_Fig. 8.3.1. Three representations of the Wagner graph W_

Using Corollary 4.2.8, one can easily compute which of the graphs 4.2.8
constructed as in Theorem 8.3.4 have the most edges. It turns out that
these extremal graphs without a K [5] minor have no more edges than those
that are extremal with respect to { MK [5], MK3,3 }, i.e. the maximal
planar graphs:

**Corollary 8.3.5. A graph with n vertices and no K** [5] _minor has at most_
3n − 6 edges. 
Since χ(W ) = 3, Theorem 8.3.4 and the four colour theorem imply
Hadwiger’s conjecture for r = 5:

**Corollary 8.3.6. Hadwiger’s conjecture holds for r = 5.** 
The Hadwiger conjecture for r = 6 is again substantially more difficult than the case r = 5, and again it relies on the four colour theorem. The proof shows (without using the four colour theorem) that any
minimal-order counterexample arises from a planar graph by adding one
vertex—so by the four colour theorem it is not a counterexample after all.

**Theorem 8.3.7. (Robertson, Seymour & Thomas 1993)**

|=|Col2|
|---|---|
|||


-----

By Corollary 8.3.5, any graph with n vertices and more than 3n 6
_−_
edges contains an MK [5]. In fact, it even contains a TK [5]. This inconspicuous improvement is another deep result that had been conjectured
for over 30 years:

**Theorem 8.3.8. (Mader 1998)**
_Every graph with n vertices and more than 3n_ 6 edges contains K [5] _as_
_−_
_a topological minor._

No structure theorem for the graphs without a TK [5], analogous to
Proposition 8.3.1 and Theorem 8.3.4, is known. However, Mader has
characterized those with the greatest possible number of edges:

**Theorem 8.3.9. (Mader 1997)**
_A graph is extremal without a TK_ [5] _if and only if it can be constructed_
_recursively from maximal planar graphs by pasting along triangles._

###### Exercises

1. Prove, from first principles, the theorem of Wagner (1964) that every
graph of chromatic number at least 2[r] contains K _[r]_ as a minor.

(Hint. Apply induction on r.)

2. Prove, from first principles, the result of Mader (1967) that every graph
of average degree at least 2[r][−][2] contains K _[r]_ as a minor.

(Hint. Induction on r.)

3.[−] Derive Wagner’s theorem (Ex. 1) from Mader’s theorem (Ex. 2).

4.[+] Given an integer r > 0, find an integer k such that every grid with k
additional edges has a K _[r]_ minor, provided that all the ends of the new
edges have distance at least k in the grid both from each other and
from the grid boundary. (Grids are defined in Chapter 12.3.)

5.[+] Show that any function h as in Theorem 3.6.1 satisfies the inequality
_h(r) >_ [1]8 _[r][2][ for all even][ r][, and hence that Theorem 8.1.1 is best possible]_

up to the value of the constant c.

6. Prove the statement of Lemma 8.1.3 for k < 6.

7. Explain how exactly the term of [1]6 _[k][ in the statement of Lemma 8.1.3]_

is used in the proof of Theorem 8.1.1. Could it be replaced by k/1000,
or by zero?

8. Explain how exactly the number 76 [in the proof of Lemma 8.1.3 was]
3


-----

9.[+] For which trees T is there a function f : N → N tending to infinity, such
that every graph G with χ(G) < f (d(G)) contains an induced copy of T ?
(In other words: can we force the chromatic number up by raising the
average degree, as long as T does not occur as an induced subgraph?
Or, as in Gy´arf´as’s conjecture: will a large average degree force an
induced copy of T if the chromatic number is kept small?)

10.[−] Derive the four colour theorem from Hadwiger’s conjecture for r = 5.

11.[−] Show that Hadwiger’s conjecture for r + 1 implies the conjecture for r.

12.[−] Using the results from this chapter, prove the following weakening of
Hadwiger’s conjecture: given any ϵ > 0, every graph of chromatic number at least r[1+][ϵ] has a K _[r]_ minor, provided that r is large enough.

13.[+] Prove Hadwiger’s conjecture for r = 4 from first principles.

14.[+] Prove Hadwiger’s conjecture for line graphs.

15. (i)[−] Show that Hadwiger’s conjecture is equivalent to the statement
that G ≽ _K_ _[χ][(][G][)]_ for all graphs G.

(ii) Show that any minimum-order counterexample G to Hadwiger’s
conjecture (as rephrased above) satisfies K _[χ][(][G][)][−][1]_ _̸⊆_ _G and has a con-_
nected complement.

16. Show that any graph constructed as in Theorem 8.3.1 is edge-maximal
without a K [4] minor.

17. Prove the implication δ(G) ⩾ 3 ⇒ _G ⊇_ _TK_ [4].

(Hint. Theorem 8.3.1.)

18. A multigraph is called series-parallel if it can be constructed recursively
from a K [2] by the operations of subdividing and of doubling edges. Show
that a 2-connected multigraph is series-parallel if and only if it has no
(topological) K [4] minor.

19. Prove Corollary 8.3.5.

20. Characterize the graphs with n vertices and more than 3n − 6 edges
that contain no TK3,3. In particular, determine ex(n, TK3,3).

(Hint. By a theorem of Wagner, every edge-maximal graph without a
_K3,3 minor can be constructed recursively from maximal planar graphs_
and copies of K [5] by pasting along K [2]s.)

21. By a theorem of Pelik´an, every graph of minimum degree at least 4
contains a subdivision of K−[5] [, a][ K] [5][ minus an edge. Using this theorem,]
prove Thomassen’s 1974 result that every graph with n ⩾ 5 vertices
and at least 4n − 10 edges contains a TK [5].

(Hint. Show by induction on |G| that if ∥G∥ ⩾ 4n − 10 then for every
vertex x _[∈]_ _G there is a TK_ [5] _⊆_ _G in which x is not a branch vertex.)_


-----

###### Notes

The investigation of graphs not containing a given graph as a minor, or topological minor, has a long history. It probably started with Wagner’s 1935
PhD thesis, in which he sought to ‘detopologize’ the four colour problem by
classifying the graphs without a K [5] minor. His hope was to be able to show
abstractly that all those graphs were 4-colourable; since the graphs without
a K [5] minor include the planar graphs, this would amount to a proof of the
four colour conjecture involving no topology whatsoever. The result of Wagner’s efforts, Theorem 8.3.4, falls tantalizingly short of this goal: although it
succeeds in classifying the graphs without a K [5] minor in structural terms,
planarity re-emerges as one of the criteria used in the classification. From this
point of view, it is instructive to compare Wagner’s K [5] theorem with similar
classification theorems, such as his analogue for K [4] (Proposition 8.3.1), where
the graphs are decomposed into parts from a finite set of irreducible graphs.
See R. Diestel, Graph Decompositions, Oxford University Press 1990, for more
such classification theorems.
Despite its failure to resolve the four colour problem, Wagner’s K [5] structure theorem had consequences for the development of graph theory like few
others. To mention just two: it prompted Hadwiger to make his famous conjecture; and it inspired the notion of a tree-decomposition, which is fundamental
to the work of Robertson and Seymour on minors (see Chapter 12). Wagner
himself responded to Hadwiger’s conjecture with a proof that, in order to force
a K _[r]_ minor, it does suffice to raise the chromatic number of a graph to some
value depending only on r (Exercise 1). This theorem then, along with its
analogue for topological minors proved independently by Dirac and by Jung,
prompted the question of which average degree suffices to force the desired
minor.
The deepest contribution in this field of research was no doubt made
by Mader, in a series of papers from the late sixties. Our proof of Lemma
8.1.3 is presented intentionally in a step-by-step fashion, to bring out some of
Mader’s ideas. Mader’s own proof—not to mention that of Thomason’s best
possible version of the lemma, as used in the original proof of Theorem 8.1.1—
is wrapped up so elegantly that it becomes hard to see the ideas behind it.
Except for this lemma, our proof of Theorem 8.1.1 follows B. Bollob´as &
A.G. Thomason, Proof of a conjecture of Mader, Erd˝os and Hajnal on topological complete subgraphs, Europ. J. Combinatorics 19 (1998), 883–887.
The constant c from the theorem was shown by J. Koml´os & E. Szemer´edi,
Topological cliques in graphs II, Combinatorics, Probability and Computing 5
(1996), 79–90, to be no greater than about [1]2 [, which is not far from the lower]

bound of [1]8 [given in Exercise 5.]

Theorem 8.1.4 is from W. Mader, Topological subgraphs in graphs of large
girth, Combinatorica 18 (1998), 405–412. For H = K _[r], the theorem says that_
every graph G with δ(G) ⩾ _r −_ 1 and g(G) large contains a TK _[r]. For r = 5,_
Mader conjectured that g(G) ⩾ 5 should be enough, and that the requirement
of δ(G) ⩾ 4 could be weakened further: he conjectured that any graph of girth
at least 5, large enough order n, and 2n _−_ 4 or more edges has a topological K [5]

minor. (To see that this implies the minimum degree version of the conjecture


-----

general H, Mader improved Theorem 8.1.4 by weakening the requirement of
_δ(G) ⩾_ _d to d(G) ⩾_ _d_ _−_ 1+ _ϵ for arbitrary ϵ > 0 (where now the girth k required_
to force a TH in such graphs G depends on ϵ as well as on H); see W. Mader,
Subdivisions of a graph of maximal degree n + 1 in graphs of average degree
_n + ϵ and large girth, manuscript 1999._
Theorem 8.1.5 is due to A.D. Scott, Induced trees in graphs of large chromatic number, J. Graph Theory 24 (1997), 297–311. Theorem 8.2.1 was
proved independently by Kostochka (1982; English translation: A.V. Kostochka, Lower bounds of the Hadwiger number of graphs by their average degree,
_Combinatorica 4 (1984), 307–316) and by A.G. Thomason, An extremal func-_
tion for contractions of graphs, Math. Proc. Camb. Phil. Soc. 95 (1984), 261–
265. Theorem 8.2.2 was taken from Thomassen’s survey, Paths, Circuits and
Subdivisions, in (L.W. Beineke & R.J. Wilson, eds.) Selected Topics in Graph
_Theory 3, Academic Press 1988._
The proof of Hadwiger’s conjecture for r = 4, hinted at in Exercise 13, is
given by Hadwiger himself in the 1943 paper containing his conjecture. For a
while, there was a counterpart to Hadwiger’s conjecture for topological minors,
the conjecture of Haj´os that χ(G) ⩾ _r even implies G ⊇_ _TK_ _[r]. A counterex-_
ample to this conjecture was found in 1979 by Catlin; a little later, Erd˝os and
Fajtlowicz even proved that Haj´os’s conjecture is false for almost all graphs
(see Chapter 11).
Mader’s Theorem 8.3.8 that 3n _−_ 5 edges force a topological K [5] minor had
been conjectured by Dirac in 1964. Its proof comprises two papers: W. Mader,
3n − 5 edges do force a subdivision of K5, Combinatorica 18 (1998), 569–595;
and W. Mader, An extremal problem for subdivisions of K5[−][,][ J. Graph Theory]
**30 (1999), 261–276. His proof of Theorem 8.3.9 has not been published yet.**
Dirac’s conjecture has been extended by Seymour, who conjectures that every
5-connected non-planar graph should contain a TK [5] (unpublished).


-----

-----

# 9 Ramsey Theory
### for Graphs

In this chapter we set out from a type of problem which, on the face of
it, appears to be similar to the theme of the last two chapters: what kind
of substructures are necessarily present in every large enough graph?
The regularity lemma of Chapter 7.2 provides one possible answer
to this question, saying as it does that every (large) graph G contains
large random-like bipartite subgraphs. If we are looking for more definite substructures, however, such as subgraphs isomorphic to some given
graphs H, then these H will have to be sufficiently complementary in
kind to cater for the variety allowed for G. For example: given an
integer r, does every large enough graph contain either a K[r] or an induced K _[r]? Does every large enough connected graph contain either a_
_K_ _[r]_ or else a large induced path or star?
Despite its similarity to extremal problems in that we are looking
for local implications of global assumptions, the above type of question
leads to a kind of mathematics with a distinctive flavour of its own.
Indeed, the theorems and proofs in this chapter have more in common
with similar results in algebra or geometry, say, than with most other
areas of graph theory. The study of their underlying methods, therefore,
is generally regarded as a combinatorial subject in its own right: the
discipline of Ramsey theory.
In line with the subject of this book, we shall focus on results that
are naturally expressed in terms of graphs. Even from the viewpoint of
general Ramsey theory, however, this is not as much of a limitation as
it might seem: graphs are a natural setting for Ramsey problems, and
the material in this chapter brings out a sufficient variety of ideas and
methods to convey some of the fascination of the theory as a whole.


-----

###### 9.1 Ramsey’s original theorems

In its simplest version, Ramsey’s theorem says that, given an integer
_r ⩾_ 0, every large enough graph G contains either K[r] or K _[r]_ as an induced
subgraph. At first glance, this may seem surprising: after all, we need
about (r 2)/(r 1) of all possible edges to force a K _[r]_ subgraph in G
_−_ _−_
(Cor. 7.1.3), but neither G nor G can be expected to have more than half
the total number of edges. However, as the Tur´an graphs illustrate well,
squeezing many edges into G without creating a K _[r]_ imposes additional
structure on G, which may help us find an induced K _[r]._
So how could we go about proving Ramsey’s theorem? Let us try
to build a K _[r]_ or K _[r]_ in G inductively, starting with an arbitrary vertex
_v1 ∈_ _V1 := V (G). If |G| is large, there will be a large set V2 ⊆_ _V1 ∖_ _{ v1 }_
of vertices that are either all adjacent to v1 or all non-adjacent to v1.
Accordingly, we may think of v1 as the first vertex of a K _[r]_ or K _[r]_ whose
other vertices all lie in V2. Let us then choose another vertex v2 ∈ _V2_
for our K _[r]_ or K _[r]. Since V2 is large, it will have a subset V3, still fairly_
large, of vertices that are all ‘of the same type’ with respect to v2 as
well: either all adjacent or all non-adjacent to it. We then continue our
search for vertices inside V3, and so on (Fig. 9.1.1).

_v1_ _V2_ _v1_ _V3_

_v2_

_Fig. 9.1.1. Choosing the sequence v1, v2, . . ._

How long can we go on in this way? This depends on the size of
our initial set V1: each set Vi has at least half the size of its predecessor Vi−1, so we shall be able to complete s construction steps if G has
order about 2[s]. As the following proof shows, the choice of s = 2r 3
_−_
vertices vi suffices in order to find among them the vertices of a K _[r]_

or K _[r]._

**Theorem 9.1.1. (Ramsey 1930)**

[ 9.2.2 ] _For every r_ _[∈]_ N there exists an n _[∈]_ N such that every graph of order at
_least n contains either K_ _[r]_ _or K_ _[r]_ _as an induced subgraph._

_Proof . The assertion is trivial for r ⩽_ 1; we assume that r ⩾ 2. Let
_n := 2[2][r][−][3], and let G be a graph of order at least n. We shall define_
a sequence V1, . . ., V2r−2 of sets and choose vertices vi ∈ _Vi with the_
following properties:


-----

(ii) Vi ⊆ _Vi−1 ∖_ _{ vi−1 } (i = 2, . . ., 2r −_ 2);

(iii) vi−1 is adjacent either to all vertices in Vi or to no vertex in Vi
(i = 2, . . ., 2r 2).
_−_

Let V1 ⊆ _V (G) be any set of 2[2][r][−][3]_ vertices, and pick v1 _[∈]_ _V1 arbitrarily._
Then (i) holds for i = 1, while (ii) and (iii) hold trivially. Suppose now
that Vi−1 and vi−1 ∈ _Vi−1 have been chosen so as to satisfy (i)–(iii) for_
_i −_ 1, where 1 < i ⩽ 2r − 2. Since

_|Vi−1 ∖_ _{ vi−1 }| = 2[2][r][−][1][−][i]_ _−_ 1

is odd, Vi−1 has a subset Vi satisfying (i)–(iii); we pick vi _[∈]_ _Vi arbitrarily._
Among the 2r − 3 vertices v1, . . ., v2r−3, there are r − 1 vertices that
show the same behaviour when viewed as vi−1 in (iii), being adjacent
either to all the vertices in Vi or to none. Accordingly, these r − 1 vertices
and v2r−2 induce either a K _[r]_ or a K _[r]_ in G, because vi, . . ., v2r−2 ∈ _Vi_
for all i. 
The least integer n associated with r as in Theorem 9.1.1 is the Ramsey _Ramsey_
_number R(r) of r; our proof shows that R(r) ⩽_ 2[2][r][−][3]. In Chapter 11 we _number_
shall use a simple probabilistic argument to show that R(r) is bounded _R(r)_
below by 2[r/][2] (Theorem 11.1.3).

It is customary in Ramsey theory to think of partitions as colourings:
a colouring of (the elements of) a set X with c colours, or c-colouring for _c-colouring_
short, is simply a partition of X into c classes (indexed by the ‘colours’).
In particular, these colourings need not satisfy any non-adjacency requirements as in Chapter 5. Given a c-colouring of [X][k], the set of all [X][k]
_k-subsets of X, we call a set Y_ _X monochromatic if all the elements_
_⊆_ _mono-_
of [Y ][k] have the same colour,[1] i.e. belong to the same of the c partition _chromatic_
classes of [X][k]. Similarly, if G = (V, E) is a graph and and all the edges
of H _G have the same colour in some colouring of E, we call H a mono-_
_⊆_
_chromatic subgraph of G, speak of a red (green, etc.) H in G, and so on._
In the above terminology, Ramsey’s theorem can be expressed as
follows: for every r there exists an n such that, given any n-set X, every
2-colouring of [X][2] yields a monochromatic r-set Y _X. Interesting-_
_⊆_
ly, this assertion remains true for c-colourings of [X][k] with arbitrary c
and k—with almost exactly the same proof!
To avoid repetition, we shall use this opportunity to demonstrate a
common alternative proof technique: we first prove an infinite version
of the general Ramsey theorem (which is easier, because we need not
worry about numbers), and then deduce the finite version by a so-called
_compactness argument._

1 Note that Y is called monochromatic, but it is the elements of [Y ]k, not of Y,


-----

[ 12.1.1 ] **Theorem 9.1.2. Let k, c be positive integers, and X an infinite set. If**

[X][k] _is coloured with c colours, then X has an infinite monochromatic_
_subset._

_Proof . We prove the theorem by induction on k, with c fixed. For k = 1_
the assertion holds, so let k > 1 and assume the assertion for smaller
values of k.
Let [X][k] be coloured with c colours. We shall construct an infinite
sequence X0, X1, . . . of infinite subsets of X and choose elements xi ∈ _Xi_
with the following properties (for all i):

(i) Xi+1 ⊆ _Xi ∖_ _{ xi };_

(ii) all k-sets { xi } ∪ _Z with Z_ _∈_ [Xi+1][k][−][1] have the same colour,
which we associate with xi.

We start with X0 := X and pick x0 _[∈]_ _X0 arbitrarily. By assumption,_
_X0 is infinite. Having chosen an infinite set Xi and xi ∈_ _Xi for some i,_
we c-colour [Xi ∖ _{ xi }][k][−][1]_ by giving each set Z the colour of { xi } ∪ _Z_
from our c-colouring of [X][k]. By the induction hypothesis, Xi ∖ _{ xi }_
has an infinite monochromatic subset, which we choose as Xi+1. Clearly,
this choice satisfies (i) and (ii). Finally, we pick xi+1 ∈ _Xi+1 arbitrarily._
Since c is finite, one of the c colours is associated with infinitely
many xi. These xi form an infinite monochromatic subset of X.      
To deduce the finite version of Theorem 9.1.2, we make use of a
standard graph-theoretical tool in combinatorics:

**Lemma 9.1.3. (K¨onig’s Infinity Lemma)**
_Let V0, V1, . . . be an infinite sequence of disjoint non-empty finite sets,_
_and let G be a graph on their union. Assume that every vertex v in a_
_set Vn with n ⩾_ 1 has a neighbour f (v) in Vn−1. Then G contains an
_infinite path v0v1 . . . with vn ∈_ _Vn for all n._

_f_ (f (v))

_f_ (v) _v_

_V0_

_V1_ _V2_ _V3_

_Fig. 9.1.2. K¨onig’s infinity lemma_

_Proof . Let_ be the set of all paths of the form v f (v) f (f (v)) . . . ending
_P_
in V0. Since V0 is finite but P is infinite, infinitely many of the paths in
_P end at the same vertex v0 ∈_ _V0. Of these paths, infinitely many also_


-----

paths, infinitely many agree even on their vertex v2 in V2—and so on.
Although the set of paths considered decreases from step to step, it is
still infinite after any finite number of steps, so vn gets defined for every
_n ∈_ N. By definition, each vertex vn is adjacent to vn−1 on one of those
paths, so v0v1 . . . is indeed an infinite path. 
**Theorem 9.1.4. For all k, c, r ⩾** 1 there exists an n ⩾ _k such that every_ [ 9.3.3 ]
_n-set X has a monochromatic r-subset with respect to any c-colouring_
_of [X][k]._

_Proof . As is customary in set theory, we denote by n_ _[∈]_ N (also) the
set 0, . . ., n 1 . Suppose the assertion fails for some k, c, r. Then for _k, c, r_
_{_ _−_ _}_
every n ⩾ _k there exist an n-set, without loss of generality the set n, and_
a c-colouring [n][k] _c such that n contains no monochromatic r-set. Let_
_→_
_bad_
us call such colourings bad ; we are thus assuming that for every n ⩾ _k_ _colouring_
there exists a bad colouring of [n][k]. Our aim is to combine these into a
bad colouring of [N][k], which will contradict Theorem 9.1.2.
For every n ⩾ _k let Vn ̸= ∅_ be the set of bad colourings of [n][k]. For
_n > k, the restriction f_ (g) of any g ∈ _Vn to [n −_ 1][k] is still bad, and
hence lies in Vn−1. By the infinity lemma, there is an infinite sequence
_gk, gk+1, . . . of bad colourings gn ∈_ _Vn such that f_ (gn) = gn−1 for all
_n > k. For every m ⩾_ _k, all colourings gn with n ⩾_ _m agree on [m][k], so_
for each Y _∈_ [N][k] the value of gn(Y ) coincides for all n > max Y . Let
us define g(Y ) as this common value gn(Y ). Then g is a bad colouring
of [N][k]: every r-set S ⊆ N is contained in some sufficiently large n,
so S cannot be monochromatic since g coincides on [n][k] with the bad
colouring gn. 
The least integer n associated with k, c, r as in Theorem 9.1.4 is the _Ramsey_
_Ramsey number for these parameters; we denote it by R(k, c, r)._ _number_
_R(k, c, r)_

###### 9.2 Ramsey numbers

Ramsey’s theorem may be rephrased as follows: if H = K _[r]_ and G
is a graph with sufficiently many vertices, then either G itself or its
complement G contains a copy of H as a subgraph. Clearly, the same is
true for any graph H, simply because H _K[h]_ for h := _H_ .
_⊆_ _|_ _|_
However, if we ask for the least n such that every graph G with _Ramsey_
_n vertices has the above property—this is the Ramsey number R(H)_ _number_
of H—then the above question makes sense: if H has only few edges, it _R(H)_
should embed more easily in G or G, and we would expect R(H) to be
smaller than the Ramsey number R(h) = R(K _[h])._
A little more generally, let R(H1, H2) denote the least n _[∈]_ N such _R(H1, H2)_


-----

_H1, H2, only very rough estimates are known for R(H1, H2). Interesting-_
ly, lower bounds given by random graphs (as in Theorem 11.1.3) are often
sharper than even the best bounds provided by explicit constructions.
The following proposition describes one of the few cases where exact
Ramsey numbers are known for a relatively large class of graphs:

**Proposition 9.2.1. Let s, t be positive integers, and let T be a tree of**
_order t. Then R(T, K_ _[s]) = (s_ 1)(t 1) + 1.
_−_ _−_

(5.2.3)
_Proof . The disjoint union of s_ 1 graphs K _[t][−][1]_ contains no copy of T,
(1.5.4) _−_
while the complement of this graph, the complete (s 1)-partite graph
_−_
_Kt[s]−[−]1[1][, does not contain][ K]_ _[s][. This proves][ R][(][T, K]_ _[s][)][ ⩾]_ [(][s][ −] [1)(][t][ −] [1) + 1.]
Conversely, let G be any graph of order n = (s 1)(t 1)+1 whose
_−_ _−_
complement contains no K _[s]. Then s > 1, and in any vertex colouring_
of G (in the sense of Chapter 5) at most s 1 vertices can have the same
_−_
colour. Hence, χ(G) ⩾ _⌈n/(s −_ 1)⌉ = t. By Corollary 5.2.3, G has a
subgraph H with δ(H) ⩾ _t_ _−_ 1, which by Corollary 1.5.4 contains a copy
of T .       
As the main result of this section, we shall now prove one of those
rare general theorems providing a relatively good upper bound for the
Ramsey numbers of a large class of graphs, a class defined in terms
of a standard graph invariant. The theorem deals with the Ramsey
numbers of sparse graphs: it says that the Ramsey number of graphs H
with bounded maximum degree grows only linearly in _H_ —an enormous
_|_ _|_
improvement on the exponential bound from the proof of Theorem 9.1.1.

**Theorem 9.2.2. (Chv´atal, R¨odl, Szemer´edi & Trotter 1983)**
_For every positive integer ∆_ _there is a constant c such that_

_R(H) ⩽_ _c |H|_

(7.1.1) _for all graphs H with ∆(H) ⩽_ ∆.
(7.2.1)

_Proof . The basic idea of the proof is as follows. We wish to show that_

(7.3.2)
(9.1.1) _H ⊆_ _G or H ⊆_ _G if |G| is large enough (though not too large). Consider_
an ϵ-regular partition of G, as provided by the regularity lemma. If
enough of the ϵ-regular pairs in this partition have positive density, we
may hope to find a copy of H in G. If most pairs have zero or low density,
we try to find H in G. Let R, R[′] and R[′′] be the ‘regularity graphs’[2] of
_G whose edges correspond to the pairs of density ⩾_ 0; ⩾ 1/2; < 1/2;
respectively. Then R is the edge-disjoint union of R[′] and R[′′].
Now to obtain H _G or H_ _G, it suffices by Lemma 7.3.2 to_
_⊆_ _⊆_
ensure that H is contained in a suitable ‘inflated regularity graph’ Rs[′]

2 Later, we shall define R′′ a little differently, so that it complies with our formal


-----

or Rs[′′][. Since][ χ][(][H][)][ ⩽] [∆(][H][)+1][ ⩽] [∆+1, this will be the case if][ s][ ⩾] _[α][(][H][)]_
and we can find a K [∆+1] in R[′] or in R[′′]. But that is easy to ensure: we
just need that K _[r]_ _R, where r is the Ramsey number of ∆+ 1, which_
_⊆_
will follow from Tur´an’s theorem because R is dense.
For the formal proof let now ∆ ⩾ 1 be given. On input d := 1/2 ∆, d
and ∆, Lemma 7.3.2 returns an ϵ0; since the lemma’s assertion about ϵ0 _ϵ0_
becomes weaker if ϵ0 is made smaller, we may assume that ϵ0 < 1. Let
_m := R(∆+ 1) be the Ramsey number of ∆+ 1. Let ϵ ⩽_ _ϵ0 be positive_ _m, ϵ_
but small enough that, for k = m (and hence for all k ⩾ _m),_

1
2ϵ < (1)

_m_ 1 _k [.]_
_−_ _[−]_ [1]


Finally, let M be the integer returned by the regularity lemma (7.2.1) _M_
on input ϵ and m.
All the quantities defined so far depend only on ∆. We shall prove
the theorem with
_M_
_c :=_ _c_

_ϵ0 (1 −_ _ϵ)_ _[.]_

So let H with ∆(H) ⩽ ∆be given, and let s := |H|. Let G be an _s_
arbitrary graph of order n ⩾ _c |H|; we show that H ⊆_ _G or H ⊆_ _G._ _G, n_
By Lemma 7.2.1, G has an ϵ-regular partition { V0, V1, . . ., Vk } with _k_
exceptional set V0 and |V1| = . . . = |Vk| =: ℓ, where m ⩽ _k ⩽_ _M_ . Then _ℓ_

_ℓ_ = _[n][ −|][V][0][|]_ ⩾ _[n][ −]_ _[ϵn]_ = n [1][ −] _[ϵ]_ ⩾ _cs_ [1][ −] _[ϵ]_ = _[s]_ _._ (2)

_k_ _M_ _M_ _M_ _ϵ0_


Let R be the regularity graph with parameters ϵ, ℓ, 0 corresponding to _R_
this partition. By definition, R has k vertices and


�k
_∥R∥_ ⩾
2


�
_ϵk[2]_
_−_


�

= [1] 1

2 _[k][2][�]_ _−_ [1]

_k_

_[−]_ [2][ϵ]

_>_ 12 _[k][2][�]1 −_ [1] 1
(1) _k_ _m_ 1 [+ 1]k

_[−]_ _−_

= [1]

2 _[k][2][ m][ −]_ [2]

_m_ 1
_−_


�


⩾ _tm−1(k)_

edges. By Theorem 7.1.1, therefore, R has a subgraph K = K _[m]._ _K_
We now colour the edges of R with two colours: red if the edge
corresponds to a pair (Vi, Vj) of density at least 1/2, and green otherwise.


-----

the spanning subgraph of R formed by the green edges and those whose
corresponding pair has density exactly 1/2. Then R[′] is a regularity graph
of G with parameters ϵ, ℓ and 1/2. And R[′′] is a regularity graph of G,
with the same parameters: as one easily checks, every pair (Vi, Vj) that
is ϵ-regular for G is also ϵ-regular for G.
By definition of m, our graph K contains a red or a green K _[r], for_
_r_ _r := χ(H) ⩽_ ∆+ 1. Correspondingly, H ⊆ _Rs[′]_ [or][ H][ ⊆] _[R]s[′′][. Since][ ϵ][ ⩽]_ _[ϵ][0]_
and ℓ ⩾ _s/ϵ0 by (2), both R[′]_ and R[′′] satisfy the requirements of Lemma
7.3.2, so H ⊆ _G or H ⊆_ _G as desired._      
So far in this section, we have been asking what is the least order of a
graph G such that every 2-colouring of its edges yields a monochromatic
copy of some given graph H. Rather than focusing on the order of G, we
might alternatively try to minimize G itself, with respect to the subgraph
_Ramsey-_
relation. Given a graph H, let us call a graph G Ramsey-minimal for H
_minimal_
if G is minimal with the property that every 2-colouring of its edges
yields a monochromatic copy of H.
What do such Ramsey-minimal graphs look like? Are they unique?
The following result, which we include for its pretty proof, answers the
second question for some H:

**Proposition 9.2.3. If T is a tree but not a star, then infinitely many**
_graphs are Ramsey-minimal for T_ _._

(1.5.4)
(5.2.3) _Proof . Let |T_ _| =: r. We show that for every n_ _[∈]_ N there is a graph of
(11.2.2) order at least n that is Ramsey-minimal for T .
Let us borrow the assertion of Theorem 11.2.2 from Chapter 11: by
that theorem, there exists a graph G with chromatic number χ(G) > r[2]

and girth g(G) > n. If we colour the edges of G red and green, then the
red and the green subgraph cannot both have an r-(vertex-)colouring in
the sense of Chapter 5: otherwise we could colour the vertices of G with
the pairs of colours from those colourings and obtain a contradiction
to χ(G) > r[2]. So let G[′] _G be monochromatic with χ(G[′]) > r. By_
_⊆_
Corollary 5.2.3, G[′] has a subgraph of minimum degree at least r, which
contains a copy of T by Corollary 1.5.4.
Let G[∗] _⊆_ _G be Ramsey-minimal for T_ . Clearly, G[∗] is not a forest: the edges of any forest can be 2-coloured (partitioned) so that no
monochromatic subforest contains a path of length 3, let alone a copy
of T . (Here we use that T is not a star, and hence contains a P [3].) So G[∗]

contains a cycle, which has length g(G) > n since G[∗] _G. In particular,_
_⊆_
_|G[∗]| > n as desired._       

-----

###### 9.3 Induced Ramsey theorems

Ramsey’s theorem can be rephrased as follows. For every graph H = K _[r]_

there exists a graph G such that every 2-colouring of the edges of G
yields a monochromatic H _G; as it turns out, this is witnessed by_
_⊆_
any large enough complete graph as G. Let us now change the problem
slightly and ask for a graph G in which every 2-edge-colouring yields
a monochromatic induced H _G, where H is now an arbitrary given_
_⊆_
graph.
This slight modification changes the character of the problem dramatically. What is needed now is no longer a simple proof that G is
‘big enough’ (as for Theorem 9.1.1), but a careful construction: the
construction of a graph that, however we bipartition its edges, contains
an induced copy of H with all edges in one partition class. We shall call
_Ramsey_
such a graph a Ramsey graph for H.
_graph_
The fact that such a Ramsey graph exists for every choice of H is
one of the fundamental results of graph Ramsey theory. It was proved
around 1973, independently by Deuber, by Erd˝os, Hajnal & P´osa, and
by R¨odl.

**Theorem 9.3.1. Every graph has a Ramsey graph. In other words, for**
_every graph H there exists a graph G that, for every partition { E1, E2 }_
_of E(G), has an induced subgraph H with E(H) ⊆_ _E1 or E(H) ⊆_ _E2._

We give two proofs. Each of these is highly individual, yet each offers a
glimpse of true Ramsey theory: the graphs involved are used as hardly
more than bricks in the construction, but the edifice is impressive.

**First proof. In our construction of the desired Ramsey graph we shall**
repeatedly replace vertices of a graph G = (V, E) already constructed
by copies of another graph H. For a vertex set U ⊆ _V let G [ U →_ _H ]_ _G [ U →_ _H ]_
denote the graph obtained from G by replacing the vertices u ∈ _U with_
copies H(u) of H and joining each H(u) completely to all H(u[′]) with _H(u)_
_uu[′ ∈]_ _E and to all vertices v_ _[∈]_ _V ∖_ _U with uv_ _[∈]_ _E (Fig. 9.3.1). Formally,_

_G_


-----

_G [ U_ _H ] is the graph on_
_→_

(U × V (H)) ∪ ((V ∖ _U_ ) × { ∅})

in which two vertices (v, w) and (v[′], w[′]) are adjacent if and only if either
_vv[′ ∈]_ _E, or else v = v[′ ∈]_ _U and ww[′ ∈]_ _E(H).[3]_

We prove the following formal strengthening of Theorem 9.3.1:


_For any two graphs H1, H2 there exists a graph G =_
_G(H1, H2)_ _G(H1, H2) such that every edge colouring of G with the_
_colours 1 and 2 yields either an induced H1 ⊆_ _G with all_
_its edges coloured 1 or an induced H2 ⊆_ _G with all its_
_edges coloured 2._


( )
_∗_


This formal strengthening makes it possible to apply induction on
_|H1| + |H2|, as follows._
If either H1 or H2 has no edges (in particular, if |H1| + |H2| ⩽ 1),
then ( ) holds with G = K _[n]_ for large enough n. For the induction step,
_∗_
we now assume that both H1 and H2 have at least one edge, and that
(∗) holds for all pairs (H1[′] _[, H]2[′]_ [) with smaller][ |][H]1[′] _[|][ +][ |][H]2[′]_ _[|][.]_
_xi_ For each i = 1, 2, pick a vertex xi ∈ _Hi that is incident with an_
_Hi[′][, H]i[′′]_ edge. Let Hi[′] [:=][ H][i][ −] _[x][i][, and let][ H]i[′′]_ [be the subgraph of][ H]i[′] [induced by]
the neighbours of xi.
We shall construct a sequence G[0], . . ., G[n] of disjoint graphs; G[n] will
be the desired Ramsey graph G(H1, H2). Along with the graphs Gi, we
shall define subsets V _[i]_ _V (G[i]) and a map_
_⊆_

_f_ : V [1] _. . ._ _V_ _[n]_ _V_ [0] _. . ._ _V_ _[n][−][1]_
_∪_ _∪_ _→_ _∪_ _∪_

such that
_f_ (V _[i]) = V_ _[i][−][1]_ (1)

_f_ _[i]_ for all i ⩾ 1. Writing f _[i]_ := f ◦ _. . . ◦_ _f for the i-fold composition of f_
whenever it is defined, and f [0] for the identity map on V [0] = V (G[0]), we
_origin_ thus have f _[i](v)_ _[∈]_ _V_ [0] for all v _[∈]_ _V_ _[i]. We call f_ _[i](v) the origin of v._
The subgraphs G[i] [ V _[i]_ ] will reflect the structure of G[0] as follows:

_Vertices in V_ _[i]_ _with different origins are adjacent in G[i]_ _if_
(2)
_and only if their origins are adjacent in G[0]._

Assertion (2) will not be used formally in the proof below. However,
it can help us to visualize the graphs G[i]: every G[i] (more precisely, every
_G[i]_ [ V _[i]_ ]—there will also be some vertices x _[∈]_ _G[i]_ _−_ _V_ _[i]) is essentially an_
inflated copy of G[0] in which every vertexw _[∈]_ _G[0]_ has been replaced by

3 The replacement of V ∖ _U by (V ∖_ _U_ ) × { ∅} is just a formal device to ensure
that all vertices of G [ U → _H ] have the same form (v, w), and that G [ U →_ _H ] is_


-----

the set of all vertices in V _[i]_ with origin w, and the map f links vertices
with the same origin across the various G[i].
By the induction hypothesis, there are Ramsey graphs

_G1 := G(H1, H2[′]_ [)] and _G2 := G(H1[′]_ _[, H][2][)][ .]_ _G1, G2_

Let G[0] be a copy of G1, and set V [0] := V (G[0]). Let W0[′][, . . ., W]n[ ′] _−1_ [be the] _G[0], V_ [0]
subsets of V [0] spanning an H2[′] [in][ G][0][. Thus,][ n][ is defined as the number] _Wi[′]_
of induced copies of H2[′] [in][ G][0][, and we shall construct a graph][ G][i][ for] _n_
every set Wi[′]−1[,][ i][ = 1][, . . ., n][. Since][ H][1][ has an edge,][ n][ ⩾] [1: otherwise]
_G[0]_ could not be a G(H1, H2[′] [). For][ i][ = 0][, . . ., n][ −] [1, let][ W]i[ ′′] [be the image] _Wi[′′]_
of V (H2[′′][) under some isomorphism][ H]2[′] _i_ [].]

_[→]_ _[G][0][ [][ W][ ′]_
Assume now that G[0], . . ., G[i][−][1] and V [0], . . ., V _[i][−][1]_ have been defined
for some i ⩾ 1, and that f has been defined on V [1] _∪_ _. . . ∪_ _V_ _[i][−][1]_ and
satisfies (1) for all j ⩽ _i. We expand G[i][−][1]_ to G[i] in two steps. For the
first step, consider the set U _[i][−][1]_ of all the vertices v _[∈]_ _V_ _[i][−][1]_ whose origin _U_ _[i][−][1]_
_f_ _[i][−][1](v) lies in Wi[′′]−1[. (For][ i][ = 1, this gives][ U][ 0][ =][ W][ ′′]0_ [.) Expand][ G][i][−][1]

to a graph G[˜][i][−][1] by replacing every vertex u ∈ _U_ _[i][−][1]_ with a copy G2(u) _G2(u)_
of G2, i.e. let
_G˜[i][−][1]_ := G[i][−][1] [ U _[i][−][1]_ _→_ _G2 ]_ _G˜_ _[i][−][1]_

(see Figures 9.3.2 and 9.3.3). Set f (u[′]) := u for all u ∈ _U_ _[i][−][1]_ and

_G[1]_ _x(F_ )

_H1[′]_ [(][u][)]
_H1[′′][(][u][)]_

_G2(u)_ _v[′]_ _V_ [1]

_u[′]_

_G[0]_

_u_ _v_
_W0[′]_ _W0[′′]_

_Fig. 9.3.2. The construction of G[1]_

_u[′ ∈]_ _G2(u), and f_ (v[′]) := v for all v[′] = (v, ∅) with v _[∈]_ _V_ _[i][−][1]_ ∖ _U_ _[i][−][1]._
(Recall that (v, ∅) is simply the unexpanded copy of a vertex v _[∈]_ _G[i][−][1]_

in G[˜][i][−][1].) Let V _[i]_ be the set of those vertices v[′] or u[′] of G[˜][i][−][1] for which _V_ _[i]_
_f has thus been defined, i.e. the vertices that either correspond directly_
to a vertex v in V _[i][−][1]_ or else belong to an expansion G2(u) of such a


-----

_i_ 1, then (2) holds again for i (in G[˜][i][−][1]). The graph G[˜][i][−][1] is already
_−_
the ‘essential part’ of G[i]: the part that looks like an inflated copy of G[0].
In the second step we now extend G[˜][i][−][1] to the desired graph G[i] by
_F_ adding some further vertices x /[∈] _V_ _[i]. Let F denote the set of all families_
_F of the form_

_F =_ �H1[′] [(][u][)][ |][ u][ ∈] _[U][ i][−][1][�]_ _,_

_H1[′]_ [(][u][)] where each H1[′] [(][u][) is an induced subgraph of][ G][2][(][u][) isomorphic to][ H]1[′] _[.]_
(Less formally: F is the collection of ways to select from each G2(u)
_x(F_ ) exactly one induced copy of H1[′] [.) For each][ F][ ∈] _[F][, add a vertex][ x][(][F]_ [)]
to G[˜][i][−][1] and join it to all the vertices of H1[′′][(][u][) for every][ u][ ∈] _[U][ i][−][1][,]_
_H1[′′][(][u][)]_ where H1[′′][(][u][) is the image of][ H]1[′′] [under some isomorphism][ H]1[′] _[→]_ _[H]1[′]_ [(][u][)]
_G[i]_ (Fig. 9.3.2). Denote the resulting graph by G[i]. This completes the
inductive definition of the graphs G[0], . . ., G[n].
Let us now show that G := G[n] satisfies ( ). To this end, we prove
_∗_
the following assertion ( ) about G[i] for i = 0, . . ., n:
_∗∗_


_For every edge colouring with the colours 1 and 2, G[i]_ _con-_
_tains either an induced H1 coloured 1, or an induced H2_
_coloured 2, or an induced subgraph H coloured 2 such that_
_V (H)_ _V_ _[i]_ _and the restriction of f_ _[i]_ _to V (H) is an isomor-_
_⊆_
_phism between H and G[0]_ [ Wk[′] []][ for some][ k][ ∈] _[{][ i, . . ., n]_ _[−]_ [1][ }][.]


( )
_∗∗_


Note that the third of the above cases cannot arise for i = n, so ( ) for
_∗∗_
_n is equivalent to (_ ) with G := G[n].
_∗_
For i = 0, (∗∗) follows from the choice of G[0] as a copy of G1 =
_G(H1, H2[′]_ [) and the definition of the sets][ W][ ′]k[. Now let 1][ ⩽] _[i][ ⩽]_ _[n][, and]_
assume ( ) for smaller values of i.
_∗∗_
Let an edge colouring of G[i] be given. For each u _[∈]_ _U_ _[i][−][1]_ there is a
copy of G2 in G[i]:
_G[i]_ _⊇_ _G2(u) ≃_ _G(H1[′]_ _[, H][2][)][ .]_

If G2(u) contains an induced H2 coloured 2 for some u ∈ _U_ _[i][−][1], we are_
done. If not, then every G2(u) has an induced subgraph H1[′] [(][u][)][ ≃] _[H]1[′]_
coloured 1. Let F be the family of these graphs H1[′] [(][u][), one for each]
_x_ _u_ _[∈]_ _U_ _[i][−][1], and let x := x(F_ ). If, for some u _[∈]_ _U_ _[i][−][1], all the x–H1[′′][(][u][)]_
edges in G[i] are also coloured 1, we have an induced copy of H1 in G[i]

and are again done. We may therefore assume that each H1[′′][(][u][) has a]
_yu_ vertex yu for which the edge xyu is coloured 2. Let

_Uˆ_ _[i][−][1]_ _Uˆ_ _[i][−][1]_ := { yu | u ∈ _U_ _[i][−][1]_ _} ⊆_ _V_ _[i]._

Then f defines an isomorphism from


ˆ


_Gˆ[i][−][1]_ : _G[i][ �]_ _Uˆ_ _[i][−][1]_ _∪_ �(v ∅) | vV (G[i][−][1]) ∖ _U_ _[i][−][1][��]_


-----

to G[i][−][1]: just map every yu to u and every (v, ∅) to v. Our edge colouring
of G[i] thus induces an edge colouring of G[i][−][1]. If this colouring yields an
induced H1 ⊆ _G[i][−][1]_ coloured 1 or an induced H2 ⊆ _G[i][−][1]_ coloured 2, we
have these also in G[ˆ][i][−][1] _G[i]_ and are again home.
_⊆_
By ( ) for i 1 we may therefore assume that G[i][−][1] has an induced
_∗∗_ _−_
subgraph H _[′]_ coloured 2, with V (H _[′]) ⊆_ _V_ _[i][−][1], and such that the restric-_ _H_ _[′]_
tion of f _[i][−][1]_ to V (H _[′]) is an isomorphism from H_ _[′]_ to G[0] [ Wk[′] []][ ≃] _[H]2[′]_
for some k _[∈]_ _{ i −_ 1, . . ., n − 1 }. Let H[ˆ] _[′]_ be the corresponding induced _Hˆ_ _[′]_
subgraph of G[ˆ][i][−][1] _G[i]_ (also coloured 2); then V ( H[ˆ] _[′])_ _V_ _[i],_
_⊆_ _⊆_

_f_ _[i](V ( H[ˆ]_ _[′])) = f_ _[i][−][1](V (H_ _[′])) = Wk[′]_ _[,]_

and f _[i]: H[ˆ]_ _[′]_ _→_ _G[0]_ [ Wk[′] [] is an isomorphism.]

_x_

_G[i]_

_H_

_Hˆ_ _′_ _G2(u)_ _G2y_

_yu_ _yu′_ _Hˆ_ _′_ _G2_ _G2_

_V_ _[i]_

_U_ _[i][−][1]_

_H_ _[′]_ _H_ _[′]_

_u_ _u[′]_

_V_ _[i][−][1]_

_G[0]_ _H2[′]_

_Wi[′]−1_ _Wi[′′]−1_

_H2_ _V_ [0]

_x2_

_Fig. 9.3.3. A monochromatic copy of H2 in G[i]_

If k ⩾ _i, this completes the proof of (∗∗) with H := H[ˆ]_ _[′]; we therefore_
assume that k < i, and hence k = i 1 (Fig. 9.3.3). By definition
_−_
of U _[i][−][1]_ and G[ˆ][i][−][1], the inverse image of Wi[′′]−1 [under the isomorphism]
_f_ _[i]: H[ˆ]_ _[′]_ _→_ _G[0]_ [ Wi[′]−1 [] is a subset of ˆ][U][ i][−][1][. Since][ x][ is joined to precisely]
those vertices of H[ˆ] _[′]_ that lie in U[ˆ] _[i][−][1], and all these edges xyu have colour 2,_
the graph H[ˆ] _[′]_ and x together induce in G[i] a copy of H2 coloured 2, and


-----

Let us return once more to the reformulation of Ramsey’s theorem
considered at the beginning of this section: for every graph H there
exists a graph G such that every 2-colouring of the edges of G yields
a monochromatic H _G. The graph G for which this follows at once_
_⊆_
from Ramsey’s theorem is a sufficiently large complete graph. If we
ask, however, that G shall not contain any complete subgraphs larger
than those in H, i.e. that ω(G) = ω(H), the problem again becomes
difficult—even if we do not require H to be induced in G.
Our second proof of Theorem 9.3.1 solves both problems at once:
given H, we shall construct a Ramsey graph for H with the same clique
number as H.
For this proof, i.e. for the remainder of this section, let us view
_bipartite_ bipartite graphs P as triples (V1, V2, E), where V1 and V2 are the two
vertex classes and E ⊆ _V1 × V2 is the set of edges. The reason for this_
more explicit notation is that we want embeddings between bipartite
graphs to respect their bipartitions: given another bipartite graph P _[′]_ =
_embedding_ (V1[′][, V][ ′]2 _[, E][′][), an injective map][ ϕ][:][ V][1]_ _[∪]_ _[V][2]_ _[→]_ _[V][ ′]1_ _[∪]_ _[V][ ′]2_ [will be called an]
_P →_ _P_ _[′]_ _embedding of P in P_ _[′]_ if ϕ(Vi) ⊆ _Vi[′]_ [for][ i][ = 1][,][ 2 and][ ϕ][(][v][1][)][ϕ][(][v][2][) is an edge]
of P _[′]_ if and only if v1v2 is an edge of P . (Note that such embeddings
are ‘induced’.) Instead of ϕ: V1 ∪ _V2 →_ _V1[′]_ _[∪]_ _[V][ ′]2_ [we may simply write]
_ϕ: P →_ _P_ _[′]._
We need two lemmas.

**Lemma 9.3.2. Every bipartite graph can be embedded in a bipartite**
_E_ _graph of the form (X, [X][k], E) with E = { xY | x_ _[∈]_ _Y }._

_Proof . Let P be any bipartite graph, with vertex classes { a1, . . ., an }_
and { b1, . . ., bm }, say. Let X be a set with 2n + m elements, say

_X = { x1, . . ., xn, y1, . . ., yn, z1, . . ., zm } ;_

we shall define an embedding ϕ: P (X, [X][n][+1], E).
_→_
Let us start by setting ϕ(ai) := xi for all i = 1, . . ., n. Which
(n + 1)-sets Y ⊆ _X are suitable candidates for the choice of ϕ(bi) for_
a given vertex bi? Clearly those adjacent exactly to the images of the
neighbours of bi, i.e. those satisfying

_Y ∩{ x1, . . ., xn } = ϕ(NP (bi)) ._ (1)

Since d(bi) ⩽ _n, the requirement of (1) leaves at least one of the n + 1_
elements of Y unspecified. In addition to ϕ(NP (bi)), we may therefore
include in each Y = ϕ(bi) the vertex zi as an ‘index’; this ensures that
_ϕ(bi) ̸= ϕ(bj) for i ̸= j, even when bi and bj have the same neighbours_
in P . To specify the sets Y = ϕ(bi) completely, we finally fill them up


-----

Our second lemma already covers the bipartite case of the theorem:
it says that every bipartite graph has a Ramsey graph—even a bipartite
one.

**Lemma 9.3.3. For every bipartite graph P there exists a bipartite**
_graph P_ _[′]_ _such that for every 2-colouring of the edges of P_ _[′]_ _there is_
_an embedding ϕ: P →_ _P_ _[′]_ _for which all the edges of ϕ(P_ ) have the same
_colour._

_Proof . We may assume by Lemma 9.3.2 that P has the form (X, [X][k], E)_ (9.1.4)
with E = { xY | x _[∈]_ _Y }. We show the assertion for the graph P_ _[′]_ := _P, X, k, E_
(X _[′], [X_ _[′]][k][′]_ _, E[′]), where k[′]_ := 2k − 1, X _[′]_ is any set of cardinality _P_ _[′], X_ _[′], k[′]_

_|X_ _[′]| = R_ �k[′], 2�kk′�, k |X| + k − 1� _,_

(this is the Ramsey number defined after Theorem 9.1.4), and

_E[′]_ := { x[′]Y _[′]_ _| x[′ ]∈_ _Y_ _[′]_ _} ._ _E[′]_

Let us then colour the edges of P _[′]_ with two colours α and β. Of the _α, β_
_|Y_ _[′]| = 2k −_ 1 edges incident with a vertex Y _[′ ∈]_ [X _[′]][k][′]_, at least k must
have the same colour. For each Y _[′]_ we may therefore choose a fixed k-set
_Z_ _[′]_ _⊆_ _Y_ _[′]_ such that all the edges x[′]Y _[′]_ with x[′ ∈] _Z_ _[′]_ have the same colour; _Z[′]_
we shall call this colour associated with Y _[′]._ _associated_
The sets Z _[′]_ can lie within their supersets Y _[′]_ in �kk′� ways, as follows.

Let X _[′]_ be linearly ordered. Then for every Y _[′ ∈]_ [X _[′]][k][′]_ there is a unique
order-preserving bijectionof �k′� possible images. _σY_ _[′]_ : Y _[′]_ _→{ 1, . . ., k[′]_ _}, which maps Z_ _[′]_ to one _σY ′_

_kWe now colour [X_ _[′]][k][′]_ with the 2�kk′� elements of the set

[ 1, . . ., k[′] ][k] _α, β_
_{_ _}_ _× {_ _}_


as colours, giving each Y _[′ ∈]_ [X _[′]][k][′]_ as its colour the pair (σY ′ (Z _[′]), γ),_
as the Ramsey number with parameterswhere γ is the colour α or β associated with k[′], 2 Y�kk[′]′. Since� and k | |XX[′]|| was chosen + k − 1, we

know that X _[′]_ has a monochromatic subset W of cardinality k |X| + _k −_ 1. _W_
All Z _[′]_ with Y _[′]_ _⊆_ _W thus lie within their Y_ _[′]_ in the same way, i.e. there
exists an S _[∈]_ [{ 1, . . ., k[′] _}][k]_ such that σY _[′]_ (Z _[′]) = S for all Y_ _[′ ∈]_ [W ][k][′],
and all Y _[′ ∈]_ [W ][k][′] are associated with the same colour, say with α. _α_
We now construct the desired embedding ϕ of P in P _[′]. We first_ _ϕ|X_
define ϕ on X =: { x1, . . ., xn }, choosing images ϕ(xi) =: wi ∈ _W so_ _xi, wi, n_
that wi < wj in our ordering of X _[′]_ whenever i < j. Moreover, we choose
the wi so that exactly k − 1 elements of W are smaller than w1, exactly
_k −_ 1 lie between wi and wi+1 for i = 1, . . ., n − 1, and exactly k − 1
are bigger than wn. Since |W _| = kn + k −_ 1, this can indeed be done


-----

_k −_ 1


###### �


_w1_

_w2_


_Y_ _[′]_

_Z_ _[′]_


_Z˜[′]_

_Y˜_ _[′]_


_k −_ 1

_k −_ 1


�

###### �


_wn_

�

_k −_ 1

_X_ _[′]_


_Fig. 9.3.4. The graph of Lemma 9.3.3_


_ϕ|[X]k_ We now define ϕ on [X][k]. Given Y _∈_ [X][k], we wish to choose
_ϕ(Y ) =: Y_ _[′ ∈]_ [X _[′]][k][′]_ so that the neighbours of Y _[′]_ among the vertices
in ϕ(X) are precisely the images of the neighbours of Y in P, i.e. the
vertices ϕ(x) with x _[∈]_ _Y, and so that all these edges at Y_ _[′]_ are coloured α.
To find such a set Y _[′], we first fix its subset Z_ _[′]_ as { ϕ(x) | x _[∈]_ _Y }_
(these are k vertices of type wi) and then extend Z _[′]_ by k[′] _−_ _k further_
vertices u _[∈]_ _W ∖_ _ϕ(X) to a set Y_ _[′ ∈]_ [W ][k][′], in such a way that Z _[′]_ lies
correctly within Y _[′], i.e. so that σY_ _[′]_ (Z _[′]) = S. This can be done, because_
_k −_ 1 = k[′] _−_ _k other vertices of W lie between any two wi. Then_

_Y_ _[′]_ _∩_ _ϕ(X) = Z_ _[′]_ = { ϕ(x) | x _[∈]_ _Y },_


so Y _[′]_ has the correct neighbours in ϕ(X), and all the edges between Y _[′]_

and these neighbours are coloured α (because those neighbours lie in Z _[′]_

and Y _[′]_ is associated with α). Finally, ϕ is injective on [X][k]: the images
_Y_ _[′]_ of different vertices Y are distinct, because their intersections with
_ϕ(X) differ. Hence, our map ϕ is indeed an embedding of P in P_ _[′]._ 

-----

**Second proof of Theorem 9.3.1. Let H be given as in the theorem,**
and let n := R(r) be the Ramsey number of r := _H_ . Then, for every _r, n_
_|_ _|_
2-colouring of its edges, the graph K = K _[n]_ contains a monochromatic _K_
copy of H—although not necessarily induced.
We start by constructing a graph G[0], as follows. Imagine the vertices of K to be arranged in a column, and replace every vertex by a row
of �n� vertices. Then each of the �n� columns arising can be associated
_r_ _r_
with one of the �nr� ways of embedding V (H) in V (K); let us furnish
this column with the edges of such a copy of H. The graph G[0] thus arising consists of �nr� disjoint copies of H and (n − _r)�nr�_ isolated vertices
(Fig. 9.3.5).

�n�

� ��r �


_r_

_n −_ _r_


_n_

|r|H|H|H H . . .|Col5|
|---|---|---|---|---|


_Fig. 9.3.5. The graph G[0]_

In order to define G[0] formally, we assume that V (K) = 1, . . ., n
_{_ _}_
and choose copies H1, . . ., H(nr[) of][ H][ in][ K][ with pairwise distinct vertex]
sets. (Thus, on each r-set in V (K) we have one fixed copy Hj of H.)
We then define


_V (G[0]) :=_ �(i, j) | i = 1, . . ., n; j = 1, . . ., �nr��


(nr[)]
�
_E(G[0]) :=_


�(i, j)(i[′], j) | ii[′ ]∈ _E(Hj)�_ _._


_G[0]_


_j=1_

The idea of the proof now is as follows. Our aim is to reduce the
general case of the theorem to the bipartite case dealt with in Lemma 9.3.3. Applying the lemma iteratively to all the pairs of rows of G[0],
we construct a very large graph G such that for every edge colouring
of G there is an induced copy of G[0] in G that is monochromatic on all
the bipartite subgraphs induced by its pairs of rows, i.e. in which edges
between the same two rows always have the same colour. The projection
of this G[0] _G to_ 1, . . ., n (by contracting its rows) then defines an
_⊆_ _{_ _}_
edge colouring of K. By the choice of |K|, one of the Hj ⊆ _K will be_
monochromatic. But this Hj occurs with the same colouring in the jth
column of our G[0], where it is an induced subgraph of G[0], and hence


-----

Formally, we shall define a sequence G[0], . . ., G[m] of n-partite graphs
_G[k], with n-partition { V1[k][, . . ., V]n[ k]_ _[}][ say, and then let][ G][ :=][ G][m][. The]_
graph G[0] has been defined above; let V1[0][, . . ., V]n[ 0] [be its rows:]

_Vi[0]_ _Vi[0]_ [:=] �(i, j) | j = 1, . . ., �nr�� _._

_ek, m_ Now let e1, . . ., em be an enumeration of the edges of K. For k =
_i1, i2_ 0, . . ., m − 1, construct G[k][+1] from G[k] as follows. If ek+1 = i1i2, say,
_P_ let P = (Vi[k]1[, V]i[ k]2[, E][) be the bipartite subgraph of][ G][k][ induced by its]
_P_ _[′]_ _i1th and i2th row. By Lemma 9.3.3, P has a bipartite Ramsey graph_
_W1, W2_ _P_ _[′]_ = (W1, W2, E[′]). We wish to define G[k][+1] _⊇_ _P_ _[′]_ in such a way that every
(monochromatic) embedding P → _P_ _[′]_ can be extended to an embedding
_ϕp, q_ _G[k]_ _→_ _G[k][+1]. Let { ϕ1, . . ., ϕq } be the set of all embeddings of P in P_ _[′],_
and let

_V (G[k][+1]) := V1[k][+1]_ _∪_ _. . . ∪_ _Vn[k][+1],_


where


_W1_ for i = i1
_W2_ for i = i2
�qp=1[(][V][ k]i _[× {][ p][ }][)]_ for i /∈ _{ i1, i2 }._


_Vi[k][+1]_ :=








(Thus for i ̸= i1, i2, we take as Vi[k][+1] just q disjoint copies of Vi[k][.) We]
now define the edge set of G[k][+1] so that the obvious extensions of ϕp to
all of V (G[k]) become embeddings of G[k] in G[k][+1]: for p = 1, . . ., q, let
_ψp: V (G[k]) →_ _V (G[k][+1]) be defined by_

_ψp(v) :=_ � (ϕv, pp(v)) forfor v / v _[∈][∈]_ _PP_
and let

_q_
�

_E(G[k][+1]) :=_ _{ ψp(v)ψp(v[′]) | vv[′ ]∈_ _E(G[k]) } ._

_p=1_

Now for every 2-colouring of its edges, G[k][+1] contains an induced copy
_ψp(G[k]) of G[k]_ whose edges in P, i.e. those between its i1th and i2th row,
have the same colour: just choose p so that ϕp(P ) is the monochromatic
induced copy of P in P _[′]_ that exists by Lemma 9.3.3.
We claim that G := G[m] satisfies the assertion of the theorem. So
let a 2-colouring of the edges of G be given. By the construction of
_G[m]_ from G[m][−][1], we can find in G[m] an induced copy of G[m][−][1] such that
for em = ii[′] all edges between the ith and the i[′]th row have the same
colour. In the same way, we find inside this copy of G[m][−][1] an induced
copy of G[m][−][2] whose edges between the ith and the i[′]th row have the
same colour also for ii[′] = em−1. Continuing in this way, we finally arrive
at an induced copy of G[0] in G such that, for each pair (i, i[′]), all the
edges between Vi[0] [and][ V][ 0]i[′][ have the same colour. As shown earlier, this]


-----

###### 9.4 Ramsey properties and connectivity

According to Ramsey’s theorem, every large enough graph G has a very
dense or a very sparse induced subgraph of given order, a K[r] or K _[r]. If_
we assume that G is connected, we can say a little more:

**Proposition 9.4.1. For every r** _[∈]_ N there is an n _[∈]_ N such that every
_connected graph of order at least n contains K_ _[r], K1,r or P_ _[r]_ _as an induced_
_subgraph._

_Proof . Let d + 1 be the Ramsey number of r, let n > 1 + rd_ _[r], and let G_
be a graph of order at least n. If G has a vertex v of degree at least d +1
then, by Theorem 9.1.1 and the choice of d, either N (v) induces a K _[r]_ in
_G or { v } ∪_ _N_ (v) induces a K1,r. On the other hand, if ∆(G) ⩽ _d, then_
by Proposition 1.3.3 G has radius > r, and hence contains two vertices
at a distance ⩾ _r. Any shortest path in G between these two vertices_
contains a P _[r]._ 
The collection of ‘typical’ induced subgraphs in Proposition 9.4.1
is smallest possible in the following sense. If is any set of connected
_G_
graphs with the same property, i.e. such that, given r _[∈]_ N, every large
enough connected graph G contains an induced copy of a graph of order ⩾ _r from G, then G contains arbitrarily large complete graphs, stars_
and paths. (Note that if we take a complete graph, a star or a path as G,
and then all its subgraphs are again of that type.) But Proposition 9.4.1
tells us that we need no more than these.
In principle, we could look for a set like for any assumed connectiv_G_
ity k. We could try to find a ‘minimal’ set (in the above sense) of typical
_k-connected graphs, one such that every large k-connected graph has a_
large subgraph in this set. Unfortunately, seems to grow very quickly
_G_
with k: already for k = 2 it becomes thoroughly messy if (as for k = 1)
we insist that those subgraphs be induced. By relaxing our specification
of containment from ‘induced subgraph’ to ‘topological minor’ and on to
‘minor’, however, we can give some neat characterizations up to k = 4.

**Proposition 9.4.2. For every r** _[∈]_ N there is an n _[∈]_ N such that every
_2-connected graph of order at least n contains C_ _[r]_ _or K2,r as a topological_
_minor._

(1.3.3)
_Proof . Let d be the n associated with r in Proposition 9.4.1, and let G_
(3.3.5)
be a 2-connected graph with more than 1+ _rd_ _[r]_ vertices. By Proposition
1.3.3, either G has a vertex of degree > d or diam(G) ⩾ rad(G) > r.
In the latter case let a, b ∈ _G be two vertices at distance > r. By_
Menger’s theorem (3.3.5), G contains two independent a–b paths. These


-----

Assume now that G has a vertex v of degree > d. Since G is 2connected, G _v is connected and thus has a spanning tree; let T be_
_−_
a minimal tree in G _v that contains all the neighbours of v. Then_
_−_
every leaf of T is a neighbour of v. By the choice of d, either T has a
vertex of degree ⩾ _r or T contains a path of length ⩾_ _r, without loss of_
generality linking two leaves. Together with v, such a path forms a cycle
of length ⩾ _r. A vertex u of degree ⩾_ _r in T can be joined to v by r_
independent paths through T, to form a TK2,r. 
**Theorem 9.4.3. (Oporowski, Oxley & Thomas 1993)**
_For every r ∈_ N there is an n ∈ N such that every 3-connected graph of
_order at least n contains a wheel of order r or a K3,r as a minor._

Let us call a graph of the form C _[n]_ _∗_ _K_ [2] (n ⩾ 4) a double wheel, the
1-skeleton of a triangulation of the cylinder as in Fig. 9.4.1 a crown, and
the 1-skeleton of a triangulation of the M¨obius strip a M¨obius crown.

_Fig. 9.4.1. A crown and a M¨obius crown_

**Theorem 9.4.4. (Oporowski, Oxley & Thomas 1993)**
_For every r_ _[∈]_ N there is an n _[∈]_ N such that every 4-connected graph
_with at least n vertices has a minor of order ⩾_ _r that is a double wheel,_
_a crown, a M¨obius crown, or a K4,s._

Note that the minors occurring in Theorems 9.4.3 and 9.4.4 are themselves 3- and 4-connected, respectively, and are not minors of one another. Thus in each case, the collection of minors is minimal in the sense
discussed earlier.

###### Exercises

1.[−] Determine the Ramsey number R(3).

2. Deduce the case k = 2 (but c arbitrary) of Theorem 9.1.4 directly from
Theorem 9.1.1.

3.[+] Construct a graph on R that has neither a complete nor an edgeless
induced subgraph on |R| = 2[ℵ][0] vertices. (So Ramsey’s theorem does
not extend to uncountable sets.)

4.[+] Use Ramsey’s theorem to show that for any k, ℓ _[∈]_ N there is an n _[∈]_ N
such that every sequence of n distinct integers contains an increasing
subsequence of length k +1 or a decreasing subsequence of length ℓ +1.
Find an example showing that n > kℓ. Then prove the theorem of


-----

5. Sketch a proof of the following theorem of Erd˝os and Szekeres: for every
_k_ _[∈]_ N there is an n _[∈]_ N such that among any n points in the plane,
no three of them collinear, there are k points spanning a convex k-gon,
i.e. such that none of them lies in the convex hull of the others.

6. Prove the following result of Schur: for every k _[∈]_ N there is an n _[∈]_ N
such that, for every partition of { 1, . . ., n } into k sets, at least one of
the subsets contains numbers x, y, z such that x + y = z.

7. Let (X, ⩽) be a totally ordered set, and let G = (V, E) be the graph
on V := [X][2] with E := {(x, y)(x[′], y[′]) | x < y = x[′] _< y[′]}._

(i) Show that G contains no triangle.

(ii) Show that χ(G) will get arbitrarily large if |X| is chosen large
enough.

8. A family of sets is called a ∆-system if every two of the sets have the
same intersection. Show that every infinite family of sets of the same
finite cardinality contains an infinite ∆-system.

9. Prove the following weakening of Scott’s Theorem 8.1.5: for every r _[∈]_ N
and every tree T there exists a k _[∈]_ N such that every graph G with
_χ(G) ⩾_ _k and ω(G) < r contains a subdivision of T in which no two_
branch vertices are adjacent in G (unless they are adjacent in T ).

10. Use the infinity lemma to show that, given k _[∈]_ N, a countably infinite graph is k-colourable (in the sense of Chapter 5) if all its finite
subgraphs are k-colourable.

11. Let m, n _[∈]_ N, and assume that m − 1 divides n − 1. Show that every
tree T of order m satisfies R(T, K1,n) = m + n − 1.

12. Prove that 2[c] _< R(2, c, 3) ⩽_ 3c! for every c _[∈]_ N.

(Hint. Induction on c.)

13.[−] Derive the statement (∗) in the first proof of Theorem 9.3.1 from the
theorem itself, i.e. show that (∗) is only formally stronger than the
theorem.

14. Show that the Ramsey graph G for H constructed in the second proof
of Theorem 9.3.1 does indeed satisfy ω(G) = ω(H).

15. Show that, given any two graphs H1 and H2, there exists a graph
_G = G(H1, H2) such that, for every vertex-colouring of G with colours_
1 and 2, there is either an induced copy of H1 coloured 1 or an induced
copy of H2 coloured 2 in G.

(Hint. Apply induction as in the first proof of Theorem 9.3.1.)

16. Show that every infinite connected graph contains an infinite path or
an infinite star.

17.[−] The K _[r]_ from Ramsey’s theorem, last sighted in Proposition 9.4.1, conspicuously fails to make an appearance from Proposition 9.4.2 onwards.
C i b d?


-----

###### Notes

Due to increased interaction with research on random and pseudo-random[4]

structures (the latter being provided, for example, by the regularity lemma),
the Ramsey theory of graphs has recently seen a period of major activity and
advance. Theorem 9.2.2 is an early example of this development.
For the more classical approach, the introductory text by R.L. Graham,
B.L. Rothschild & J.H. Spencer, Ramsey Theory (2nd edn.), Wiley 1990,
makes stimulating reading. This book includes a chapter on graph Ramsey
theory, but is not confined to it. A more recent general survey is given by
J. Neˇsetˇril in the Handbook of Combinatorics (R.L. Graham, M. Gr¨otschel &
L. Lov´asz, eds.), North-Holland 1995. The Ramsey theory of infinite sets forms
a substantial part of combinatorial set theory, and is treated in depth in
P. Erd˝os, A. Hajnal, A. M´at´e & R. Rado, Combinatorial Set Theory, NorthHolland 1984. An attractive collection of highlights from various branches
of Ramsey theory, including applications in algebra, geometry and point-set
topology, is offered in B. Bollob´as, Graph Theory, Springer GTM 63, 1979.
K¨onig’s infinity lemma, or K¨onig’s lemma for short, is contained in
the first-ever book on the subject of graph theory: D. K¨onig, Theorie der
_endlichen und unendlichen Graphen, Akademische Verlagsgesellschaft, Leipzig_
1936. The compactness technique for deducing finite results from infinite (or
vice versa), hinted at in Section 9.1, is less mysterious than it sounds. As
long as ‘infinite’ means ‘countably infinite’, it is precisely the art of applying
the infinity lemma (as in the proof of Theorem 9.1.4), no more no less. For
larger infinite sets, the same argument becomes equivalent to the well-known
theorem of Tychonov that arbitrary products of compact spaces are compact—
which has earned the compactness argument its name. Details can be found
in Ch. 6, Thm. 10 of Bollob´as, and in Graham, Rothschild & Spencer, Ch. 1,
Thm. 4. Another frequently used version of the general compactness argument
is Rado’s selection lemma; see A. Hajnal’s chapter on infinite combinatorics in
the Handbook cited above.
Theorem 9.2.2 is due to V. Chv´atal, V. R¨odl, E. Szemer´edi & W.T. Trotter,
The Ramsey number of a graph with bounded maximum degree, J. Combin.
_Theory B 34 (1983), 239–243. Our proof follows the sketch in J. Koml´os &_
M. Simonovits, Szemer´edi’s Regularity Lemma and its applications in graph
theory, in (D. Mikl´os, V.T. S´os & T. Sz˝onyi, eds.) Paul Erd˝os is 80, Vol. 2,
Proc. Colloq. Math. Soc. J´anos Bolyai (1996). The theorem marks a breakthrough towards a conjecture of Burr and Erd˝os (1975), which asserts that the
Ramsey numbers of graphs with bounded average degree in every subgraph are
linear: for every d _[∈]_ N, the conjecture says, there exists a constant c such that
_R(H) ⩽_ _c |H| for all graphs H with d(H_ _[′]) ⩽_ _d for all H_ _[′]_ _⊆_ _H. This conjecture_
has been verified also for the class of planar graphs (Chen & Schelp 1993) and,
more generally, for the class of graphs not containing K _[r]_ (for any fixed r) as
a topological minor (R¨odl & Thomas 1996). See Neˇsetˇril’s Handbook chapter
for references.

4 Concrete graphs whose structure resembles the structure expected of a random
graph are called pseudo-random. For example, the bipartite graphs spanned by an


-----

Our first proof of Theorem 9.3.1 is based on W. Deuber, A generalization
of Ramsey’s theorem, in (A. Hajnal, R. Rado & V.T. S´os, eds.) Infinite and
_finite sets, North-Holland 1975._ The same volume contains the alternative
proof of this theorem by Erd˝os, Hajnal and P´osa. R¨odl proved the same result
in his MSc thesis at the Charles University, Prague, in 1973. Our second
proof of Theorem 9.3.1, which preserves the clique number of H for G, is due
to J. Neˇsetˇril & V. R¨odl, A short proof of the existence of restricted Ramsey
graphs by means of a partite construction, Combinatorica 1 (1981), 199–202.
The two theorems in Section 9.4 are due to B. Oporowski, J. Oxley &
R. Thomas, Typical subgraphs of 3- and 4-connected graphs, J. Combin. The_ory B 57 (1993), 239–257._


-----

-----

# 10 Hamilton Cycles

In Chapter 1.8 we briefly discussed the problem of when a graph contains
an Euler tour, a closed walk traversing every edge exactly once. The
simple Theorem 1.8.1 solved that problem quite satisfactorily. Let us
now ask the analogous question for vertices: when does a graph G contain
a closed walk that contains every vertex of G exactly once? If |G| ⩾ 3,
_Hamilton_
then any such walk is a cycle: a Hamilton cycle of G. If G has a Hamilton
_cycle_
cycle, it is called hamiltonian. Similarly, a path in G containing every
_Hamilton_
vertex of G is a Hamilton path.
_path_
To determine whether or not a given graph has a Hamilton cycle is
much harder than deciding whether it is Eulerian, and no good characterization[1] is known of the graphs that do. We shall begin this chapter
by presenting the standard sufficient conditions for the existence of a
Hamilton cycle (Sections 10.1 and 10.2). The rest of the chapter is then
devoted to the beautiful theorem of Fleischner that the ‘square’ of every
2-connected graph has a Hamilton cycle. This is one of the main results
in the field of Hamilton cycles. The simple proof we present (due to R´ıha)[ˇ]
is still a little longer than other proofs in this book, but not difficult.

###### 10.1 Simple sufficient conditions

What kind of condition might be sufficient for the existence of a Hamilton
cycle in a graph G? Purely global assumptions, like high edge density,
will not be enough: we cannot do without the local property that every
vertex has at least two neighbours. But neither is any large (but constant) minimum degree sufficient: it is easy to find graphs without a Hamilton cycle whose minimum degree exceeds any given constant bound.

1 The notion of a ‘good characterization’ can be made precise; see the introduction


-----

The following classic result derives its significance from this background:

**Theorem 10.1.1. (Dirac 1952)**
_Every graph with n ⩾_ 3 vertices and minimum degree at least n/2 has
_a Hamilton cycle._

_Proof . Let G = (V, E) be a graph with |G| = n ⩾_ 3 and δ(G) ⩾ _n/2._
Then G is connected: otherwise, the degree of any vertex in the smallest
component C of G would be less than |C| ⩽ _n/2._
Let P = x0 . . . xk be a longest path in G. By the maximality of P,
all the neighbours of x0 and all the neighbours of xk lie on P . Hence
at least n/2 of the vertices x0, . . ., xk−1 are adjacent to xk, and at least
_n/2 of these same k < n vertices xi are such that x0xi+1_ _[∈]_ _E. By the_
pigeon hole principle, there is a vertex xi that has both properties, so
we have x0xi+1 _[∈]_ _E and xixk_ _[∈]_ _E for some i < k (Fig. 10.1.1)._

_. . ._ _xi+1_ _. . ._

_x0_ _P_ _xi_ _xk_

_Fig. 10.1.1. Finding a Hamilton cycle in the proof Theorem 10.1.1_

We claim that the cycle C := x0xi+1PxkxiPx0 is a Hamilton cycle
of G. Indeed, since G is connected, C would otherwise have a neighbour
in G _C, which could be combined with a spanning path of C into a_
_−_
path longer than P . 

Theorem 10.1.1 is best possible in that we cannot replace the bound
of n/2 with ⌊n/2⌋: if n is odd and G is the union of two copies of K _[⌈][n/][2][⌉]_

meeting in one vertex, then δ(G) = _n/2_ but κ(G) = 1, so G cannot
_⌊_ _⌋_
have a Hamilton cycle. In other words, the high level of the bound of
_δ ⩾_ _n/2 is needed to ensure, if nothing else, that G is 2-connected:_
a condition just as trivially necessary for hamiltonicity as a minimum
degree of at least 2. It would seem, therefore, that prescribing some
high (constant) value for κ rather than for δ stands a better chance of
implying hamiltonicity. However, this is not so: although k-connected
graphs contain long cycles in terms of k (Ex. 14, Ch. 3), the graphs Kn,k
show that their circumference need not grow with n.
There is another invariant with a similar property: a low independence number α(G) ensures that G has long cycles (Ex. 13, Ch. 5),
though not necessarily a Hamilton cycle. Put together, however, the
two assumptions of high connectivity and low independence number
surprisingly complement each other to produce a sufficient condition for


-----

**Proposition 10.1.2. Every graph G with |G| ⩾** 3 and κ(G) ⩾ _α(G)_
_has a Hamilton cycle._

_Proof . Put κ(G) =: k, and let C be a longest cycle in G. Enumerate the_ (3.3.3)
vertices of C cyclically, say as V (C) = { vi | i ∈ Zn } with vivi+1 ∈ _E(C)_ _k_
for all i ∈ Zn. If C is not a Hamilton cycle, pick a vertex v ∈ _G −_ _C and_
a v–C fan F = { Pi | i _[∈]_ _I } in G, where I ⊆_ Zn and each Pi ends in vi.
Let F be chosen with maximum cardinality; then vvj /[∈] _E(G) for any_
_j /[∈]_ _I, and_
_|F| ⩾_ min { k, |C| } (1)

by Menger’s theorem (3.3.3).
For every i _[∈]_ _I, we have i_ +1 /[∈] _I: otherwise, (C ∪_ _Pi ∪_ _Pi+1)_ _−_ _vivi+1_
would be a cycle longer than C (Fig. 10.1.2, left). Thus _<_ _C_, and
_|F|_ _|_ _|_
hence |I| = |F| ⩾ _k by (1). Furthermore, vi+1vj+1 /[∈]_ _E(G) for all i, j_ _[∈]_ _I,_
as otherwise (C ∪ _Pi ∪_ _Pj) + vi+1vj+1 −_ _vivi+1 −_ _vjvj+1 would be a cycle_
longer than C (Fig. 10.1.2, right). Hence { vi+1 | i _[∈]_ _I }∪{ v } is a set of_
_k + 1 or more independent vertices in G, contradicting α(G) ⩽_ _k._ 
_v_ _v_

_Pi+1_ _Pj_

_vi+1_ _Pi_ _F_ _vj+1_ _vj_ _vi_ +1 _Pi_

_vi_

_vi_

_C_ _C_

_Fig. 10.1.2. Two cycles longer than C_

It may come as a surprise to learn that hamiltonicity for planar
graphs is related to the four colour problem. As we noted in Chapter 6.6,
the four colour theorem is equivalent to the non-existence of a planar
snark, i.e. to the assertion that every bridgeless planar cubic graph has
a 4-flow. It is easily checked that ‘bridgeless’ can be replaced with ‘3connected’ in this assertion, and that every hamiltonian graph has a
4-flow (Ex. 12, Ch. 6). For a proof of the four colour theorem, therefore,
it would suffice to show that every 3-connected planar cubic graph has
a Hamilton cycle!
Unfortunately, this is not the case: the first counterexample was
found by Tutte in 1946. Ten years later, Tutte proved the following
deep theorem as a best possible weakening:

**Theorem 10.1.3. (Tutte 1956)**


-----

###### 10.2 Hamilton cycles and degree sequences

Historically, Dirac’s theorem formed the point of departure for the discovery of a series of weaker and weaker degree conditions, all sufficient
for hamiltonicity. The development culminated in a single theorem that
encompasses all the earlier results: the theorem we shall prove in this
section.
If G is a graph with n vertices and degrees d1 ⩽ _. . . ⩽_ _dn, then the_
_degree_
_sequence_ _n-tuple (d1, . . ., dn) is called the degree sequence of G. Note that this_
sequence is unique, even though G has several vertex enumerations giving
rise to its degree sequence. Let us call an arbitrary integer sequence
_hamiltonian_
_sequence_ (a1, . . ., an) hamiltonian if every graph with n vertices and a degree
sequence pointwise greater than (a1, . . ., an) is hamiltonian. (A sequence
_pointwise_
_greater_ (d1, . . ., dn) is pointwise greater than (a1, . . ., an) if di ⩾ _ai for all i.)_
The following theorem characterizes all hamiltonian sequences:

**Theorem 10.2.1. (Chv´atal 1972)**
_An integer sequence (a1, . . ., an) such that 0 ⩽_ _a1 ⩽_ _. . . ⩽_ _an < n and_
_n ⩾_ 3 is hamiltonian if and only if the following holds for every i < n/2:

_ai ⩽_ _i ⇒_ _an−i ⩾_ _n −_ _i ._

(a1, . . ., an) _Proof ._ Let (a1, . . ., an) be an arbitrary integer sequence such that
0 ⩽ _a1 ⩽_ _. . . ⩽_ _an < n and n ⩾_ 3. We first assume that this sequence
satisfies the condition of the theorem and prove that it is hamiltonian.
Suppose not; then there exists a graph G = (V, E) with a degree sequence
(d1, . . ., dn) (d1, . . ., dn) such that

_di ⩾_ _ai_ for all i (1)

_G = (V, E)_ but G has no Hamilton cycle. Let G be chosen with the maximum num_v1, . . ., vn_ ber of edges, and let (v1, . . ., vn) be an enumeration of V with d(vi) = di
for all i. By (1), our assumptions for (a1, . . ., an) transfer to (d1, . . ., dn),
i.e.,

_di ⩽_ _i ⇒_ _dn−i ⩾_ _n −_ _i_ for all i < n/2. (2)

_x, y_ Let x, y be distinct and non-adjacent vertices in G, with d(x) ⩽ _d(y)_
and d(x) + d(y) as large as possible. One easily checks that the degree
sequence of G + _xy is pointwise greater than (d1, . . ., dn), and hence than_
(a1, . . ., an). Hence, by the maximality of G, the new edge xy lies on a
_x1, . . ., xn_ Hamilton cycle H of G + _xy. Then H −_ _xy is a Hamilton path x1, . . ., xn_
in G, with x1 = x and xn = y say.
As in the proof of Dirac’s theorem, we now consider the index sets


-----

Then I _J_ 1, . . ., n 1, and I _J =_ because G has no Hamilton
_∪_ _⊆{_ _−_ _}_ _∩_ _∅_
cycle. Hence

_d(x) + d(y) =_ _I_ + _J_ _< n,_ (3)
_|_ _|_ _|_ _|_


so h := d(x) < n/2 by the choice of x. _h_
Since xiy /∈ _E for all i ∈_ _I, all these xi were candidates for the_
choice of x (together with y). Our choice of _x, y_ with d(x) + d(y)
_{_ _}_
maximum thus implies that d(xi) ⩽ _d(x) for all i_ _[∈]_ _I. Hence G has at_
least |I| = h vertices of degree at most h, so dh ⩽ _h. By (2), this implies_
that dn−h ⩾ _n −_ _h, i.e. the h + 1 vertices vn−h, . . ., vn all have degree at_
least n _h. Since d(x) = h, one of these vertices, z say, is not adjacent_ _z_
_−_
to x. Since

_d(x) + d(z) ⩾_ _h + (n −_ _h) = n,_


this contradicts the choice of x and y by (3).

Let us now show that, conversely, for every sequence (a1, . . ., an) of
the theorem with


_ah ⩽_ _h_ and _an−h ⩽_ _n −_ _h −_ 1

for some h < n/2, there exists a graph that has a pointwise greater degree _h_
sequence than (a1, . . ., an) but no Hamilton cycle. Clearly it suffices,
given h, to show this for the greatest such sequence (a1, . . ., an), the
sequence


(h, . . ., h
����
_h times_


_, n_ _h_ 1, . . ., n _h_ 1
_−_ _−_ _−_ _−_
� �� �
_n−2h times_


_, n_ 1, . . ., n 1
_−_ _−_
� �� �
_h times_


) . (4)


_vh_

_v2_
_v1_


_K_ _[n][−][h]_

_vn−h+1_
_Kh,h_


_vn_


_vh+1_


_Fig. 10.2.1. Any cycle containing v1, . . ., vh misses vh+1_

As Figure 10.2.1 shows, there is indeed a graph with degree sequence
(4) but no Hamilton cycle: the graph with vertices v1, . . ., vn and edge
set


-----

i.e. the union of a K _[n][−][h]_ on the vertices vh+1, . . ., vn and a Kh,h with
partition sets { v1, . . ., vh } and { vn−h+1, . . ., vn }.        
By applying Theorem 10.2.1 to G _K_ [1], one can easily prove the
_∗_
following adaptation of the theorem to Hamilton paths. Let an integer sequence be called path-hamiltonian if every graph with a pointwise
greater degree sequence has a Hamilton path.

**Corollary 10.2.2. An integer sequence (a1, . . ., an) such that n ⩾** 2 and
0 ⩽ _a1 ⩽_ _. . . ⩽_ _an < n is path-hamiltonian if and only if every i ⩽_ _n/2_
_is such that ai < i ⇒_ _an+1−i ⩾_ _n −_ _i._      
###### 10.3 Hamilton cycles in the square of a graph

_G[d]_ Given a graph G and a positive integer d, we denote by G[d] the graph on
_V (G) in which two vertices are adjacent if and only if they have distance_
at most d in G. Clearly, G = G[1] _G[2]_ _. . . Our goal in this section is_
_⊆_ _⊆_
to prove the following fundamental result:

**Theorem 10.3.1. (Fleischner 1974)**
_If G is a 2-connected graph, then G[2]_ _has a Hamilton cycle._

We begin with three simple lemmas. Let us say that an edge e _[∈]_ _G[2]_

_bridges_ _bridges a vertex v_ _[∈]_ _G if its ends are neighbours of v in G._

**Lemma 10.3.2. Let P = v0 . . . vk be a path (k ⩾** 1), and let G be the
_graph obtained from P by adding two vertices u, w, together with the_
_edges uv1 and wvk (Fig. 10.3.1)._

(i) P [2] _contains a path Q from v0 to v1 with V (Q) = V (P_ ) and
_vk−1vk_ _∈_ _E(Q), such that each of the vertices v1, . . ., vk−1 is_
_bridged by an edge of Q._

(ii) G[2] _contains disjoint paths Q from v0 to vk and Q[′]_ _from u to w,_
_such that V (Q)_ _∪_ _V (Q[′]) = V (G) and each of the vertices v1, . . ., vk_
_is bridged by an edge of Q or Q[′]._

_u_ _w_

|Col1|P|
|---|---|


_v0_


_v1_


_vk_


-----

_Proof . (i) If k is even, let Q := v0v2 . . . vk−2vkvk−1vk−3 . . . v3v1. If k is_
odd, let Q := v0v2 . . . vk−1vkvk−2 . . . v3v1.
(ii) If k is even, let Q := v0v2 . . . vk−2vk; if k is odd, let Q :=
_v0v1v3 . . . vk−2vk. In both cases, let Q[′]_ be the u–w path on the remaining
vertices of G[2]. 
**Lemma 10.3.3. Let G = (V, E) be a cubic multigraph with a Hamilton**
_cycle C. Let e ∈_ _E(C) and f ∈_ _E ∖_ _E(C) be edges with a common end v_
_(Fig. 10.3.2). Then there exists a closed walk in G that traverses e once,_
_every other edge of C once or twice, and every edge in E ∖_ _E(C) once._
_This walk can be chosen to contain the triple (e, v, f_ ), that is, it traverses
_e in the direction of v and then leaves v by the edge f_ _._


_e_


_e_

_v_ _v[′]_
_v[′′]_

_f_

_G[′]_


_G_


_Fig. 10.3.2. The multigraphs G and G[′]_ in Lemma 10.3.3

(1.2.1)
_Proof . By Proposition 1.2.1, C has even length. Replace every other_
(1.8.1)
edge of C by a double edge, in such a way that e does not get replaced.
In the arising 4-regular multigraph G[′], split v into two vertices v[′], v[′′],
making v[′] incident with e and f, and v[′′] incident with the other two
edges at v (Fig. 10.3.2). By Theorem 1.8.1 this multigraph has an Euler
tour, which induces the desired walk in G. 
**Lemma 10.3.4. For every 2-connected graph G and x ∈** _V (G), there is a_
_cycle C ⊆_ _G that contains x as well as a vertex y ̸= x with NG(y) ⊆_ _V (C)._

_Proof . If G has a Hamilton cycle, there is nothing more to show. If_
not, let C _[′]_ _G be any cycle containing x; such a cycle exists, since G_
_⊆_
is 2-connected. Let D be a component of G − _C_ _[′]. Assume that C_ _[′]_ and
_D are chosen so that_ _D_ is minimal. Since G is 2-connected, D has
_|_ _|_
at least two neighbours on C _[′]._ Then C _[′]_ contains a path P between
two such neighbours u and v, whose interior P[˚] does not contain x and
has no neighbour in D (Fig. 10.3.3). Replacing P in C _[′]_ by a u–v path
through D, we obtain a cycle C that contains x and a vertex y ∈ _D. If_
_y had a neighbour z in G −_ _C, then z would lie in a component D[′]_ ⫋ _D_
of G _−_ _C, contradicting the choice of C_ _[′]_ and D. Hence all the neighbours


-----

_D_


_x_


_v_
_y_


_C_

_Fig. 10.3.3. The proof of Lemma 10.3.4_

**Proof of Theorem 10.3.1. We show by induction on** _G_ that, given
_|_ _|_
any vertex x[∗∈] _G, there is a Hamilton cycle H in G[2]_ with the following
property:

_Both edges of H at x[∗]_ _lie in G._ (∗)

For |G| = 3, we have G = K [3] and the assertion is trivial. So let |G| ⩾ 4,
_x[∗]_ assume the assertion for graphs of smaller order, and let x[∗∈] _V (G) be_
_C_ given. By Lemma 10.3.4, there is a cycle C ⊆ _G that contains both x[∗]_
_y[∗]_ and a vertex y[∗] = x[∗] whose neighbours in G all lie on C.
_̸_

If C is a Hamilton cycle of G, there is nothing to show; so assume
that G _C_ = . Consider a component D of G _C. Let D[˜] denote_
_−_ _̸_ _∅_ _−_
the graph G/(G _D) obtained from G by contracting G_ _D into a new_
_−_ _−_
_P(D)_ vertex ˜x. If |D| = 1, set P(D) := { D }. If |D| > 1, then D[˜] is again
2-connected. Hence, by the induction hypothesis, D[˜] [2] has a Hamilton
_C˜_ cycle C[˜] whose edges at ˜x both lie in D[˜] . Note that the path C[˜] _x˜ may_
_−_
have some edges that do not lie in G[2]: edges joining two neighbours of ˜x
that have no common neighbour in G (and are themselves non-adjacent
_P(D)_ in G). Let E[˜] denote the set of these edges, and let P(D) denote the set
of components of ( C[˜] _x˜)_ _E; this is a set of paths in G[2]_ whose ends
_−_ _−_ [˜]
are adjacent to ˜x in D[˜] (Fig. 10.3.4).

_P(D)_

_D_

_x˜_

_Fig. 10.3.4. P(D) consists of three paths, one of which is trivial_

_P_ Let P denote the union of the sets P(D) over all components D


-----

_The elements of_ _are pairwise disjoint paths in G[2]_ _avoid-_
_P_
_ing C, and V (G) = V (C) ∪_ [�]P _[∈]P_ _[V][ (][P]_ [)][. Every end][ y][ of a]
_path P_ _[∈]_ _P has a neighbour on C in G; we choose such a_
neighbour and call it the foot of P at y.


(1)


_foot_


If P ∈ _P is trivial, then P has exactly one foot. If P is non-trivial, then_

_P has a foot at each of its ends. These two feet need not be distinct,_
however; so any non-trivial P has either one or two feet.
We shall now modify a little, preserving the properties summa_P_
rized under (1); no properties of other than those will be used later in
_P_
the proof. If a vertex of C is a foot of two distinct paths P, P _[′ ∈]_ _P, say_
at y _[∈]_ _P and at y[′ ∈]_ _P_ _[′], then yy[′]_ is an edge and Pyy[′]P _[′]_ is a path in G[2];
we replace P and P _[′]_ in P by this path. We repeat this modification of
until the following holds:
_P_

_No vertex of C is a foot of two distinct paths in_ _._ (2)
_P_

For i = 1, 2 let Pi ⊆P denote the set of all paths in P with exactly i _P1, P2_
feet, and let Xi ⊆ _V (C) denote the set of all feet of paths in Pi. Then_ _X1, X2_
_X1 ∩_ _X2 = ∅_ by (2), and y[∗] _∈/_ _X1 ∪_ _X2._
Let us also simplify G a little; again, these changes will affect neither
the paths in nor the validity of (1) and (2). First, we shall assume from
_P_
now on that all elements of are paths in G itself, not just in G[2]. This
_P_
assumption may give us some additional edges for G[2], but we shall not
use these in our construction of the desired Hamilton cycle H. (Indeed,
_H will contain all the paths from_ whole, as subpaths.) Thus if H lies
_P_
in G[2] and satisfies ( ) for the modified version of G, it will do so also
_∗_
for the original. For every P _[∈]_ _P, we further delete all P_ –C edges in G
except those between the ends of P and its corresponding feet. Finally,
we delete all chords of C in G. We are thus assuming without loss of
generality:


_The only edges of G between C and a path P_ _∈_ _P are_
_the two edges between the ends of P and its corresponding_
_feet. (If_ _P_ = 1, these two edges coincide.) The only edges
_|_ _|_
_of G with both ends on C are the edges of C itself._


(3)


Our goal is to construct the desired Hamilton cycle H of G[2] from
the paths in and suitable paths in C [2]. As a first approximation, we
_P_
shall construct a closed walk W in the graph

_G˜ := G −_ � _P1,_ _G˜_

a walk that will already satisfy a ( )-type condition and traverse every
_∗_
path in P2 exactly once. Later, we shall modify W so that it passes


-----

paths from P1. For the construction of W we assume that P2 ̸= ∅; the
case of P2 = ∅ is much simpler and will be treated later.
We start by choosing a fixed cyclic orientation of C, a bijection
_i �→_ _vi from Z|C| to V (C) with vivi+1 ∈_ _E(C) for all i_ _[∈]_ Z|C|. Let us
think of this orientation as clockwise; then every vertex vi ∈ _C has a right_
_v[+], right_ neighbour vi[+] [:=][ v][i][+1][ and a][ left][ neighbour][ v]i[−] [:=][ v][i][−][1][. Accordingly, the]
_v[−], left_ edge v[−]v lies to the left of v, the edge vv[+] lies on its right, and so on.
A non-trivial path P = vivi+1 . . . vj−1vj in C such that V (P ) _∩_ _X2 =_
_interval_ _{ vi, vj } will be called an interval_, with left end vi and right end vj.
Thus, C is the union of |X2| = 2 |P2| intervals. As usual, we write P =:

[ v, w ] etc. [ vi, vj ] and set (vi, vj) := P[˚] as well as [ vi, vj) := P˚vj and (vi, vj ] := ˚viP .
For intervals [ u, v ] and [ v, w ] with a common end v we say that [ u, v ]
lies to the left of [ v, w ], and [ v, w ] lies to the right of [ u, v ]. We denote
_I_ _[∗], P_ _[∗]_ the unique interval [ v, w ] with x[∗∈] (v, w ] as I _[∗], the path in P2 with_
_Q[∗]_ foot w as P _[∗], and the path I_ _[∗]wP_ _[∗]_ as Q[∗].
For the construction of W, we may think of G[˜] as a multigraph M
on X2 whose edges are the intervals on C and the paths in P2 (with their
feet as ends). By (2), M is cubic, so we may apply Lemma 10.3.3 with
_W_ _e := I_ _[∗]_ and f := P _[∗]. The lemma provides us with a closed walk W in G[˜]_
which traverses I _[∗]_ once, every other interval of C once or twice, and
every path in P2 once. Moreover, W contains Q[∗] as a subpath. The two
edges at x[∗] of this path lie in G; in this sense, W already satisfies (∗).

Let us now modify W so that W passes through every vertex of C
exactly once. Simultaneously, we shall prepare for the later inclusion of
_e(v)_ the paths from P1 by defining a map v �→ _e(v) that is injective on X1_
and assigns to every v ∈ _X1 an edge e(v) of the modified W with the_
following property:

_The edge e(v) either bridges v or is incident with it. In the_
( )
_latter case, e(v)_ _[∈]_ _C and e(v) ̸= vx[∗]._ _∗∗_

For simplicity, we shall define the map v �→ _e(v) on all of V (C) ∖_ _X2,_
a set that includes X1 by (2). To ensure injectivity on X1, we only
have to make sure that no edge vw _[∈]_ _C is chosen both as e(v) and_
as e(w). Indeed, since |X1| ⩾ 2 if injectivity is a problem, and P2 ̸= ∅
by assumption, we have |C − _y[∗]| ⩾_ _|X1| + 2 |P2| ⩾_ 4 and hence |C| ⩾ 5;
thus, no edge of G[2] can bridge more than one vertex of C, or bridge a
vertex of C and lie on C at the same time.
For our intended adjustments of W at the vertices of C, we consider
the intervals of C one at a time. By definition of W, every interval is of
one of the following three types:

_Type 1_ : W traverses I once;
_Type 2_ : W traverses I twice, in one direction and back immediately
afterwards (formally: W contains a triple (e, x, e) with x _[∈]_ _X2_


-----

_Type 3_ : W traverses I twice, on separate occasions (i.e., there is no
triple as above).

By definition of W, the interval I _[∗]_ is of type 1. The vertex x in the
definition of a type 2 interval will be called the dead end of that interval. _dead end_
Finally, since Q[∗] is a subpath of W and W traverses both I _[∗]_ and P _[∗]_

only once, we have:

_The interval to the right of I_ _[∗]_ _is of type 2 and has its dead_
(4)
_end on the left._

Consider a fixed interval I = [ x1, x2 ]. Let y1 be the neighbour _I, x1, x2_
of x1, and y2 the neighbour of x2 on a path in P2. Let I _[−]_ denote the _y1, y2_
interval to the left of I. _I_ _[−]_
Suppose first that I is of type 1. We then leave W unchanged on I.
If I ̸= I _[∗]_ we choose as e(v), for each v _[∈]_ [˚]I, the edge to the left of v. As
_I_ _[−]_ ≠ _I_ _[∗]_ by (4), and hence x1 ̸= x[∗], these choices of e(v) satisfy (∗∗). If
_I = I_ _[∗], we define e(v) as the edge left of v if v_ _[∈]_ (x1, x[∗] ] ∩ [˚]I, and as the
edge right of v if v _[∈]_ (x[∗], x2). These choices of e(v) are again compatible
with ( ).
_∗∗_
Suppose now that I is of type 2. Assume first that x2 is the dead
end of I. Then W contains the walk y1x1Ix2Ix1I _[−]_ (possibly in reverse
order). We now apply Lemma 10.3.2 (i) with P := y1x1I˚x2, and replace
in W the subwalk y1x1Ix2Ix1 by the y1–x1 path Q ⊆ _G[2]_ of the lemma
(Fig. 10.3.5). Then V (Q[˚]) = V (P ) ∖ _{ y1, x1 } = V ([˚]I)._ The vertices


_y1_


_y1_

_Q_
_W_


_I_ _[−]_ _x1_ _I_ _x2_


_x1_ _e(x[−]2_ [)] _x2_


_Fig. 10.3.5. How to modify W on an interval of type 2_

_v ∈_ (x1, x[−]2 [) are each bridged by an edge of][ Q][, which we choose as][ e][(][v][).]
As e(x[−]2 [) we choose the edge to the left of][ x]2[−] [(unless][ x]2[−] [=][ x][1][). This]
edge, too, lies on Q, by the lemma. Moreover, by (4) it is not incident with x[∗] (since x2 is the dead end of I, by assumption) and hence
satisfies (∗∗). The case that x1 is the dead end of I can be treated in
the same way: using Lemma 10.3.2 (i), we replace in W the subwalk
_y2x2Ix1Ix2 by a y2–x2 path Q ⊆_ _G[2]_ with V (Q[˚]) = V ([˚]I), choose as e(v)
for v _[∈]_ (x[+]1 _[, x][2][) an edge of][ Q][ bridging][ v][, and define][ e][(][x]1[+][) as the edge]_
to the right of x[+]1 [(unless][ x]1[+] [=][ x][2][).]
Suppose finally that I is of type 3. Since W traverses the edge y1x1
only once and the interval I _[−]_ no more than twice, W contains y1x1I
and I _[−]_ _∪_ _I as subpaths, and I_ _[−]_ is of type 1. By (4), however, I _[−]_ ≠ _I_ _[∗]._
Hence, when e(v) was defined for the vertices v _[∈]_ [˚]I _[−], the rightmost edge_


-----

edge. Since W traverses I [+] no more than twice, it must traverse the
edge x2y2 immediately after one of its two subpaths y1x1I and x[−]1 _[x][1][I][.]_
Take the starting vertex of this subpath (y1 or x[−]1 [) as the vertex][ u][ in]
Lemma 10.3.2 (ii), and the other vertex in { y1, x[−]1 _[}][ as][ v][0][; moreover, set]_
_vk := x2 and w := y2. Then the lemma enables us to replace these two_
subpaths of W between { y1, x[−]1 _[}][ and][ {][ x][2][, y][2][ }][ by disjoint paths in][ G][2]_

(Fig. 10.3.6), and furthermore assigns to every vertex v ∈ [˚]I an edge e(v)
of one of those paths, bridging v.


_y1_


_y2_ _y1_ _y2_

_x1_ _I_ _x2_ _v0_ _x1_ _x2 = vk_


_Fig. 10.3.6. A type 3 modification for the case u = y1 and k odd_

Following the above modifications, W is now a closed walk in G[˜][2].
Let us check that, moreover, W contains every vertex of G[˜] exactly once.
For vertices of the paths in P2 this is clear, because W still traverses every
such path once and avoids it otherwise. For the vertices of C − _X2, it_
follows from the above modifications by Lemma 10.3.2. So how about
the vertices in X2?
Let x _[∈]_ _X2 be given, and let y be its neighbour on a path in P2. Let_
_I1 denote the interval I that satisfied yxI ⊆_ _W before the modification_
of W, and let I2 denote the other interval ending in x. If I1 is of type 1,
then I2 is of type 2 with dead end x. In this case, x was retained in W
when W was modified on I1 but skipped when W was modified on I2,
and is thus contained exactly once in W now. If I1 is of type 2, then x
is not its dead end, and I2 is of type 1. The subwalk of W that started
with yx and then went along I1 and back, was replaced with a y–x path.
This path is now followed on W by the unchanged interval I2, so in this
case too the vertex x is now contained in W exactly once. Finally, if I1
is of type 3, then x was contained in one of the replacement paths Q, Q[′]

from Lemma 10.3.2 (ii); as these paths were disjoint by the assertion of
the lemma, x is once more left on W exactly once.
We have thus shown that W, after the modifications, is a closed walk
in G[˜][2] containing every vertex of G[˜] exactly once, so W defines a Hamilton
_H˜_ cycle H[˜] of G[˜][2]. Since W still contains the path Q[∗], H[˜] satisfies ( ).
_∗_

Up until now, we have assumed that P2 is non-empty. If P2 = ∅,
_H˜_ let us set H[˜] := G[˜] = C; then, again, H[˜] satisfies ( ). It remains to turn
_∗_
_H˜ into a Hamilton cycle H of G[2]_ by incorporating the paths from P1.
In order to be able to treat the case of P2 = ∅ along with the case of


-----

every v _[∈]_ _C −_ _y[∗], set_

_e(v) :=_ � _vv[+]_ if v _[∈]_ [ x[∗], y[∗])
_vv[−]_ if v ∈ (y[∗], x[∗]).

(Here, [ x[∗], y[∗]) and (y[∗], x[∗]) denote the obvious paths in C defined analogously to intervals.) As before, this map v _e(v) is injective, satis-_
_�→_
fies (∗∗), and is defined on a superset of X1; recall that y[∗] cannot lie
in X1 by definition.
Let P _∈_ _P1 be a path to be incorporated into H[˜]_, say with foot _P, v_
_v_ _[∈]_ _X1 and ends y1, y2. (If |P_ _| = 1, then y1 = y2.) Our aim is to replace_ _y1, y2_
the edge e := e(v) in H[˜] by P ; we thus have to show that the ends of P _e_
are joined to those of e by suitable edges of G[2].
By (2) and (3), v has only two neighbours in G[˜], its neighbours
_x1, x2 on C. If v is incident with e, i.e. if e = vxi with i_ _[∈]_ _{ 1, 2 }, we_
replace e by the path vy1Py2xi ⊆ _G[2]_ (Fig. 10.3.7). If v is not incident

_y1_ _P_ _y2_

_v_ _e_

_x1_ _x2_

_C_

_Fig. 10.3.7. Replacing the edge e in H[˜]_

with e then e bridges v, by (∗∗). Then e = x1x2, and we replace e
by the path x1y1Py2x2 ⊆ _G[2]_ (Fig. 10.3.8). Since v �→ _e(v) is injective_
on X1, assertion (2) implies that all these modifications of H[˜] (one for
every P _∈_ _P1) can be performed independently, and hence produce a_
Hamilton cycle H of G[2]. _H_

_y1_ _P_ _y2_

_v_

_x1_ _x2_

_C_ _e_

_Fig. 10.3.8. Replacing the edge e in H[˜]_

Let us finally check that H satisfies ( ), i.e. that both edges of H
_∗_
at x[∗] lie in G. Since (∗) holds for H[˜], it suffices to show that any edge
_e = x[∗]z of H[˜] that is not in H (and hence has the form e = e(v) for some_ _e, z_
_v_ _[∈]_ _X1) was replaced by an x[∗]–z path whose first edge lies in G._ _v_
Where can the vertex v lie? Let us show that v must be incident
with e. If not then P2 ̸= ∅, and e bridges v. Now P2 ̸= ∅ and v _[∈]_ _X1_
together imply that |C − _y[∗]| ⩾_ _|X1| + 2 |P2| ⩾_ 3, so |C| ⩾ 4. As e ∈ _G_


-----

So v is indeed incident with e. Hence v _[∈]_ _{ x[∗], z } by definition of e,_
while e ̸= vx[∗] by (∗∗). Thus v = x[∗], and e was replaced by a path of
the form x[∗]y1Py2z. Since x[∗]y1 is an edge of G, this replacement again
preserves ( ). Therefore H does indeed satisfy ( ), and our induction is
_∗_ _∗_
complete. 
We close the chapter with a far-reaching conjecture generalizing
Dirac’s theorem:

**Conjecture. (Seymour 1974)**
_Let G be a graph of order n ⩾_ 3, and let k be a positive integer. If G
_has minimum degree_

_k_
_δ(G) ⩾_

_k + 1_ _[n,]_

_then G has a Hamilton cycle H such that H_ _[k]_ _G._
_⊆_

For k = 1, this is precisely Dirac’s theorem. The case k = 2 had already
been conjectured by P´osa in 1963 and was proved for large n by Koml´os,
S´ark¨ozy & Szemer´edi (1996).

###### Exercises

1. Show that every uniquely 3-edge-colourable cubic graph is hamiltonian. (‘Unique’ means that all 3-edge-colourings induce the same edge
partition.)

2. Prove or disprove the following strengthening of Proposition 10.1.2:
‘Every k-connected graph G with |G| ⩾ 3 and χ(G) ⩾ _|G|/k has a_
Hamilton cycle.’

3. Given a graph G, consider a maximal sequence G0, . . ., Gk such that
_G0 = G and Gi+1 = Gi + xiyi for i = 0, . . ., k −_ 1, where xi, yi are two
non-adjacent vertices of Gi satisfying dGi (xi)+ _dGi_ (yi) ⩾ _|G|. The last_
graph of the sequence, Gk, is called the Hamilton closure of G. Show
that this graph depends only on G, not on the choice of the sequence
_G0, . . ., Gk._

4. Let x, y be two nonadjacent vertices of a connected graph G, with
_d(x) + d(y) ⩾_ _|G|._ Show that G has a Hamilton cycle if and only
if G + xy has one. Using the previous exercise, deduce the following
strengthening of Dirac’s theorem: if d(x) + d(y) ⩾ _|G| for every two_
non-adjacent vertices x, y _[∈]_ _G, then G has a Hamilton cycle._

5. Given an even positive integer k, construct for every n ⩾ _k a k-regular_
graph of order 2n + 1.


-----

7.[−] Let G be a graph with fewer than i vertices of degree at most i, for
every i < |G|/2. Use Chv´atal’s theorem to show that G is hamiltonian.
(Thus in particular, Chv´atal’s theorem implies Dirac’s theorem.)

8. Find a connected graph G whose square G[2] has no Hamilton cycle.

9.[+] Show by induction on |G| that the third power G[3] of a connected graph
_G contains a Hamilton path between any two vertices. Deduce that G[3]_

is hamiltonian.

10. Show that the square of a 2-connected graph contains a Hamilton path
between any two vertices.

11. An oriented complete graph is called a tournament. Show that every
tournament contains a (directed) Hamilton path.

12.[+] Let G be a graph in which every vertex has odd degree. Show that
every edge of G lies on an even number of Hamilton cycles.

(Hint. Let xy _∈_ _E(G) be given._ The Hamilton cycles through xy
correspond to the Hamilton paths in G − _xy from x to y. Consider the_
set H of all Hamilton paths in G − _xy starting at x, and show that an_
even number of these end in y. To show this, define a graph on H so
that the desired assertion follows from Proposition 1.2.1.)

###### Notes

The problem of finding a Hamilton cycle in a graph has the same kind of origin
as its Euler tour counterpart and the four colour problem: all three problems
come from mathematical puzzles older than graph theory itself. What began
as a game invented by W.R. Hamilton in 1857—in which ‘Hamilton cycles’
had to be found on the graph of the dodecahedron—reemerged over a hundred years later as a combinatorial optimization problem of prime importance:
the travelling salesman problem. Here, a salesman has to visit a number of
customers, and his problem is to arrange these in a suitable circular route.
(For reasons not included in the mathematical brief, the route has to be such
that after visiting a customer the salesman does not pass through that town
again.) Much of the motivation for considering Hamilton cycles comes from
variations of this algorithmic problem.
A detailed discussion of the various degree conditions for hamiltonicity
referred to at the beginning of Section 10.2 can be found in R. Halin, Graphen_theorie, Wissenschaftliche Buchgesellschaft 1980. All the relevant references_
for Sections 10.1 and 10.2 can be found there, or in B. Bollob´as, Extremal
_Graph Theory, Academic Press 1978._
The ‘proof’ of the four colour theorem indicated at the end of Section 10.1,
which is based on the (false) premise that every 3-connected cubic planar graph
is hamiltonian, is usually attributed to the Scottish mathematician P.G. Tait.
Following Kempe’s flawed proof of 1879 (see the notes for Chapter 5), it seems
that Tait believed to be in possession of at least one ‘new proof of Kempe’s the

-----

this subject in 1883, he seems to have been aware that he could not—really—
prove the above statement about Hamilton cycles. His account in P.G. Tait,
Listing’s topologie, Phil. Mag. 17 (1884), 30–46, makes some entertaining
reading.
A shorter proof of Tutte’s theorem that 4-connected planar graphs are
hamiltonian was given by C. Thomassen, A theorem on paths in planar graphs,
_J. Graph Theory 7 (1983), 169–176. Tutte’s counterexample to Tait’s assump-_
tion that even 3-connectedness suffices (at least for cubic graphs) is shown in
Bollob´as, and in J.A. Bondy & U.S.R. Murty, Graph Theory with Applications,
Macmillan 1976 (where Tait’s attempted proof is discussed in some detail).
Proposition 10.1.2 is due to Chv´atal & Erd˝os (1972). Our proof of Fleischner’s theorem is based on S. R´ıha, A new proof of the theorem by Fleisch-[ˇ]
ner, J. Combin. Theory B 52 (1991), 117–123. Seymour’s conjecture is from
P.D. Seymour, Problem 3, in (T.P. McDonough and V.C. Mavron, eds.) Com_binatorics, Cambridge University Press 1974. P´osa’s conjecture was proved for_
large n by J. Koml´os, G.N. S´ark¨ozy & E. Szemer´edi, On the square of a Hamiltonian cycle in dense graphs, Random Structures and Algorithms 9 (1996),
193–211.


-----

# 11 Random Graphs

At various points in this book, we already encountered the following
fundamental theorem of Erd˝os: for every integer k there is a graph
_G with g(G) > k and χ(G) > k. In plain English: there exist graphs_
combining arbitrarily large girth with arbitrarily high chromatic number.
How could one prove such a theorem? The standard approach would
be to construct a graph with those two properties, possibly in steps
by induction on k. However, this is anything but straightforward: the
global nature of the second property forced by the first, namely, that
the graph should have high chromatic number ‘overall’ but be acyclic
(and hence 2-colourable) locally, flies in the face of any attempt to build
it up, constructively, from smaller pieces that have the same or similar
properties.
In his pioneering paper of 1959, Erd˝os took a radically different
approach: for each n he defined a probability space on the set of graphs
with n vertices, and showed that, for some carefully chosen probability
measures, the probability that an n-vertex graph has both of the above
properties is positive for all large enough n.
This approach, now called the probabilistic method, has since unfolded into a sophisticated and versatile proof technique, in graph theory as
much as in other branches of discrete mathematics. The theory of ran_dom graphs is now a subject in its own right. The aim of this chapter_
is to offer an elementary but rigorous introduction to random graphs:
no more than is necessary to understand its basic concepts, ideas and
techniques, but enough to give an inkling of the power and elegance
hidden behind the calculations.
Erd˝os’s theorem asserts the existence of a graph with certain properties: it is a perfectly ordinary assertion showing no trace of the randomness employed in its proof. There are also results in random graphs
that are generically random even in their statement: these are theorems


-----

last section, we give a detailed proof of a theorem of Erd˝os and R´enyi
that illustrates a proof technique frequently used in random graphs, the
so-called second moment method .

###### 11.1 The notion of a random graph

_V_ Let V be a fixed set of n elements, say V = 0, . . ., n 1 . Our aim is
_{_ _−_ _}_
_G_ to turn the set G of all graphs on V into a probability space, and then
to consider the kind of questions typically asked about random objects:
What is the probability that a graph G _[∈]_ _G has this or that property?_
What is the expected value of a given invariant on G, say its expected
girth or chromatic number?
Intuitively, we should be able to generate G randomly as follows.
For each e _[∈]_ [V ][2] we decide by some random experiment whether or not
_e shall be an edge of G; these experiments are performed independently,_
and for each the probability of success—i.e. of accepting e as an edge
_p_ for G—is equal to some fixed[1] number p _[∈]_ [ 0, 1 ]. Then if G0 is some
fixed graph on V, withn _m edges say, the elementary event { G0 } has a_
_q_ probability of p[m]q[(] 2[)][−][m] (where q := 1 _p): with this probability, our_
_−_
randomly generated graph G is this particular graph G0. (The probability that G is isomorphic to G0 will usually be greater.) But if the
probabilities of all the elementary events are thus determined, then so
is the entire probability measure of our desired space . Hence all that
_G_
remains to be checked is that such a probability measure on, one for
_G_
which all individual edges occur independently with probability p, does
indeed exist.[2]

In order to construct such a measure on formally, we start by
_G_
defining for every potential edge e ∈ [V ][2] its own little probability space
Ωe Ωe := { 0e, 1e }, choosing Pe({ 1e }) := p and Pe({ 0e }) := q as the
_Pe_ probabilities of its two elementary events. As our desired probability
_G(n, p)_ space G = G(n, p) we then take the product space

�

Ω Ω:= Ωe .
_e∈[V ][2]_

1 Often, the value of p will depend on the cardinality n of the set V on which our
random graphs are generated; thus, p will be the value p = p(n) of some function
_n �→_ _p(n)._ Note, however, that V (and hence n) is fixed for the definition of G:
for each n separately, we are constructing a probability space of the graphs G on
_V = { 0, . . ., n −_ 1 }, and within each space the probability that e _[∈]_ [V ][2] is an edge
of G has the same value for all e.
2 Any reader ready to believe this may skip ahead now to the end of Proposi

-----

Thus, formally, an element of Ωis a map ω assigning to every e _[∈]_ [V ][2]

either 0e or 1e, and the probability measure P on Ωis the product _P_
measure of all the measures Pe. In practice, of course, we identify ω
with the graph G on V whose edge set is

_E(G) = { e | ω(e) = 1e },_

_random_
and call G a random graph on V with edge probability p.
_graph_
Following standard probabilistic terminology, we may now call any
set of graphs on V an event in G(n, p). In particular, for every e _[∈]_ [V ][2] _event_
the set

_Ae := { ω | ω(e) = 1e }_ _Ae_

of all graphs G on V with e ∈ _E(G) is an event: the event that e is an_
edge of G. For these events, we can now prove formally what had been
our guiding intuition all along:

**Proposition 11.1.1. The events Ae are independent and occur with**
_probability p._

_Proof . By definition,_

�
_Ae = { 1e } ×_ Ωe′ .

_e[′]≠_ _e_

Since P is the product measure of all the measures Pe, this implies


�
_P_ (Ae) = p · 1 = p .

_e[′]≠_ _e_

Similarly, if { e1, . . ., ek } is any subset of [V ][2], then

� � �
_P (Ae1 ∩_ _. . . ∩_ _Aek_ ) = P _{ 1e1 } × . . . × { 1ek } ×_ Ωe

_e/∈{ e1,...,ek }_

= p[k]


= P (Ae1) · · · P (Aek ) .

                    
As noted before, P is determined uniquely by the value of p and our
assumption that the events Ae are independent. In order to calculate
probabilities in (n, p), it therefore generally suffices to work with these
_G_
two assumptions: our concrete model for (n, p) has served its purpose
_G_
and will not be needed again.
As a simple example of such a calculation, consider the event that G
contains some fixed graph H on a subset of V as a subgraph; let _H_ =: k _k_
_|_ _|_
and _H_ =: ℓ. The probability of this event H _G is the product of_ _ℓ_
_∥_ _∥_ _⊆_


-----

_k_
contrast, the probability that H is an induced subgraph of G is p[ℓ]q[(]2[)][−][ℓ]:
now the edges missing from H are required to be missing from G too,
and they do so independently with probability q.
The probability PH that G has an induced subgraph isomorphic
to H is usually more difficult to compute: since the possible instances
of H on subsets of V overlap, the events that they occur in G are not
independent. However, the sum (over all k-sets U _V ) of the probabil-_
_⊆_
ities P [ H ≃ _G [ U ] ] is always an upper bound for PH_, since PH is the
measure of the union of all those events. For example, if H = K _[k], we_
have the following trivial upper bound on the probability that G contains
an induced copy of H:

[ 11.2.1 ]

[ 11.3.4 ] **Lemma 11.1.2. For all integers n, k with n ⩾** _k ⩾_ 2, the probability
_that G ∈_ _G(n, p) has a set of k independent vertices is at most_

�n� _k_
_P [ α(G) ⩾_ _k ] ⩽_ _q[(]2[)]._
_k_

_Proof ._ The probability that a fixed k-set U _V is independent in_
_k_ _⊆_
_G is q[(]2[)]. The assertion thus follows from the fact that there are only_
�nk� such sets U .        
Analogously, the probability that G ∈ _G(n, p) contains a K_ _[k]_ is at
most
�n� _k_
_P [ ω(G) ⩾_ _k ] ⩽_ _p[(]2[)]._
_k_

Now if k is fixed, and n is small enough that these bounds for the probabilities P [ α(G) ⩾ _k ] and P [ ω(G) ⩾_ _k ] sum to less than 1, then G_
contains graphs that have neither property: graphs which contain neither a K _[k]_ nor a K _[k]_ induced. But then any such n is a lower bound for
the Ramsey number of k !
As the following theorem shows, this lower bound is quite close to
the upper bound of 2[2][k][−][3] implied by the proof of Theorem 9.1.1:

**Theorem 11.1.3. (Erd˝os 1947)**
_For every integer k ⩾_ 3, the Ramsey number of k satisfies

_R(k) > 2[k/][2]._


_Proof . For k = 3 we trivially have R(3) ⩾_ 3 > 2[3][/][2], so let k ⩾ 4. We show
that, for all n ⩽ 2[k/][2] and G _[∈]_ _G(n,_ [1]2 [), the probabilities][ P][ [][ α][(][G][)][ ⩾] _[k][ ]]_

and P [ ω(G) ⩾ _k ] are both less than_ [1]2 [.]

Since p = q = [1]2 [, Lemma 11.1.2 and the analogous assertion for][ ω][(][G][)]


-----

_P [ α(G) ⩾_ _k ], P [ ω(G) ⩾_ _k ] ⩽_ �nk�� 12 �(k2[)]

_<_ �n[k]/2[k][�] 2[−] 2[1] _[k][(][k][−][1)]_


⩽ �2[k][2][/][2]/2[k][�] 2[−] 2[1] _[k][(][k][−][1)]_

= 2[−][k/][2]

_<_ 12 _[.]_

                    
In the context of random graphs, each of the familiar graph invariants (like average degree, connectivity, girth, chromatic number, and so
_random_
on) may be interpreted as a non-negative random variable on (n, p),
_G_ _variable_
a function

_X:_ (n, p) [ 0, ) .
_G_ _→_ _∞_

The mean or expected value of X is the number _mean_
_expectation_
�
_E(X) :=_ _P_ ( _G_ ) _X(G) ._

_{_ _}_ _·_
_G_ _∈G(n,p)_ _E(X)_

Note that the operator E, the expectation, is linear: we have E(X + _Y ) =_
_E(X) + E(Y ) and E(λX) = λE(X) for any two random variables X, Y_
on G(n, p) and λ ∈ R.
Computing the mean of a random variable X can be a simple and
effective way to establish the existence of a graph G such that X(G) < a
for some fixed a > 0 and, moreover, G has some desired property .
_P_
Indeed, if the expected value of X is small, then X(G) cannot be large for
more than a few graphs in G(n, p), because X(G) ⩾ 0 for all G ∈ _G(n, p)._
Hence X must be small for many graphs in (n, p), and it is reasonable
_G_
to expect that among these we may find one with the desired property .
_P_
This simple idea lies at the heart of countless non-constructive existence proofs using random graphs, including the proof of Erd˝os’s theorem
presented in the next section. Quantified, it takes the form of the following lemma, whose proof follows at once from the definition of the
expectation and the additivity of P :

**Lemma 11.1.4. (Markov’s Inequality)** [ 11.2.2 ]
_Let X ⩾_ 0 be a random variable on G(n, p) and a > 0. Then [ 11.4.1 ]

[ 11.4.3 ]

_P [ X ⩾_ _a ] ⩽_ _E(X)/a ._

_Proof ._

�
_E(X) =_ _P_ ( _G_ ) _X(G)_
_{_ _}_ _·_


-----

�
⩾ _P_ ({ G }) · X(G)

_G∈G(n,p)_
_X(G)⩾a_


�
⩾ _P_ ({ G }) · a

_G∈G(n,p)_
_X(G)⩾a_

= P [ X ⩾ _a ] · a ._

                       
Since our probability spaces are finite, the expectation can often
be computed by a simple application of double counting, a standard
combinatorial technique we met before in the proofs of Corollary 4.2.8
and Theorem 5.5.3. For example, if X is a random variable on (n, p)
_G_
that counts the number of subgraphs of G in some fixed set of graphs
_H_
on V, then E(X), by definition, counts the number of pairs (G, H) such
that H _G, each weighted with the probability of_ _G_ . Algorithmically,
_⊆_ _{_ _}_
we compute E(X) by going through the graphs G _[∈]_ _G(n, p) in an ‘outer_
loop’ and performing, for each G, an ‘inner loop’ that runs through the
graphs H _[∈]_ _H and counts ‘P_ ({ G })’ whenever H ⊆ _G. Alternatively,_
we may count the same set of weighted pairs with H in the outer and
_G in the inner loop: this amounts to adding up, over all H_, the
_⊆H_
probabilities P [ H _G ]._
_⊆_
To illustrate this once in detail, let us compute the expected number
of cycles of some given length k ⩾ 3 in a random graph G _[∈]_ _G(n, p). So_
_X_ let X: G(n, p) → N be the random variable that assigns to every random
graph G its number of k-cycles, the number of subgraphs isomorphic
to C _[k]. Let us write_

(n)k (n)k := n (n − 1)(n − 2) · · · (n − _k + 1)_

for the number of sequences of k distinct elements of a given n-set.

[ 11.2.2 ]

[ 11.4.3 ] **Lemma 11.1.5. The expected number of k-cycles in G ∈** _G(n, p) is_


_E(X) = [(][n][)][k]_

2k [p][k][.]

_Proof . For every k-cycle C with vertices in V =_ 0, . . ., n 1, the
_{_ _−_ _}_
vertex set of the graphs in G(n, p), let XC: G(n, p) →{ 0, 1 } denote the
_indicator random variable of C:_

� 1 if C _G;_
_XC: G �→_ _⊆_
0 otherwise.
Since XC takes only 1 as a positive value, its expectation E(XC) equals
the measure P [ XC = 1 ] of the set of all graphs in G(n, p) that contain C.
But this is just the probability that C _G:_
_⊆_


-----

How many such cycles C = v0 . . . vk−1v0 are there? There are (n)k
sequences v0 . . . vk−1 of distinct vertices in V, and each cycle is identified
by 2k of those sequences—so there are exactly (n)k/2k such cycles.
Our random variable X assigns to every graph G its number of kcycles. Clearly, this is the sum of all the values XC(G), where C varies
over the (n)k/2k cycles of length k with vertices in V :

�
_X =_ _XC ._

_C_

Since the expectation is linear, (1) thus implies


�� � �
_E(X) = E_ _XC_ = _E(XC) = [(][n]2k [)][k]_ _[p][k]_

_C_ _C_

as claimed. 
###### 11.2 The probabilistic method

Very roughly, the probabilistic method in discrete mathematics has developed from the following idea. In order to prove the existence of an
object with some desired property, one defines a probability space on
some larger—and certainly non-empty—class of objects, and then shows
that an element of this space has the desired property with positive
probability. The ‘objects’ inhabiting this probability space may be of
any kind: partitions or orderings of the vertices of some fixed graph arise
as naturally as mappings, embeddings and, of course, graphs themselves.
In this section, we illustrate the probabilistic method by giving a detailed
account of one of its earliest results: of Erd˝os’s classic theorem on large
girth and chromatic number.
Erd˝os’s theorem says that, given any positive integer k, there is a
graph G with girth g(G) > k and chromatic number χ(G) > k. Let us
call cycles of length at most k short, and sets of _G_ _/k or more vertices_ _short_
_|_ _|_
_big. For a proof of Erd˝os’s theorem, it suffices to find a graph G without_ _big/small_
short cycles and without big independent sets of vertices: then the colour
classes in any vertex colouring of G are small (not big), so we need more
than k colours to colour G.
How can we find such a graph G? If we choose p small enough, then
a random graph in (n, p) is unlikely to contain any (short) cycles. If
_G_
we choose p large enough, then G is unlikely to have big independent
vertex sets. So the question is: do these two ranges of p overlap, that
is, can we choose p so that, for some n, it is both small enough to give


-----

(n, p) will contain at least one graph without either short cycles or big
_G_
independent sets.
Unfortunately, such a choice of p is impossible: the two ranges of p
do not overlap! As we shall see in Section 11.4, we must keep p below
_n[−][1]_ to make the occurrence of short cycles in G unlikely—but for any
such p there will most likely be no cycles in G at all (Exercise 19), so G
will be bipartite and hence have at least n/2 independent vertices.
But all is not lost. In order to make big independent sets unlikely,
we shall fix p above n[−][1], at n[ϵ][−][1] for some ϵ > 0. Fortunately, though,
if ϵ is small enough then this will produce only few short cycles in G,
even compared with n (rather than, more typically, with n[k]). If we then
delete a vertex in each of those cycles, the graph H obtained will have
no short cycles, and its independence number α(H) will be at most that
of G. Since H is not much smaller than G, its chromatic number will
thus still be large, so we have found a graph with both large girth and
large chromatic number.
To prepare for the formal proof of Erd˝os’s theorem, we first show
that an edge probability of p = n[ϵ][−][1] is indeed always large enough to
ensure that G _[∈]_ _G(n, p) ‘almost surely’ has no big independent set of ver-_
tices. More precisely, we prove the following slightly stronger assertion:

**Lemma 11.2.1. Let k > 0 be an integer, and let p = p(n) be a function**
_of n such that p ⩾_ (6k ln n)n[−][1] _for n large. Then_


lim
_n→∞_ _[P][ [][ α][ ⩾]_ 2[1] _[n/k][ ] = 0][ .]_

(11.1.2) _Proof . For all integers n, r with n ⩾_ _r ⩾_ 2, and all G ∈ _G(n, p), Lemma_
11.1.2 implies

�n� _r_
_P [ α ⩾_ _r ] ⩽_ _q[(]2[)]_
_r_

_r_
2[)]
⩽ _n[r]q[(]_

�
= _nq[(][r][−][1)][/][2][�][r]_

�
⩽ _ne[−][p][(][r][−][1)][/][2][�][r]_ ;


here, the last inequality follows from the fact that 1 − _p ⩽_ _e[−][p]_ for all p.
(Compare the functions x _e[x]_ and x _x + 1 for x =_ _p.)_ Now
_�→_ _�→_ _−_
if p ⩾ (6k ln n)n[−][1] and r ⩾ [1]2 _[n/k][, then the term under the exponent]_

satisfies
_ne[−][p][(][r][−][1)][/][2]_ = ne[−][pr/][2 +][ p/][2]

⩽ _ne[−][(3][/][2) ln][ n][ +][ p/][2]_

⩽ _n n[−][3][/][2]_ _e[1][/][2]_
_√_ _√_


-----

Since p ⩾ (6k ln n)n[−][1] for n large, we thus obtain for r := ⌈ 2[1] _[n/k][⌉]_

lim
_n→∞_ _[P][ [][ α][ ⩾]_ 2[1] _[n/k][ ] = lim]n→∞_ _[P][ [][ α][ ⩾]_ _[r][ ] = 0][,]_

as claimed. 

**Theorem 11.2.2. (Erd˝os 1959)**
_For every integer k there exists a graph H with girth g(H) > k and_ [ 9.2.3 ]
_chromatic number χ(H) > k._

(11.1.4)
_Proof . Assume that k ⩾_ 3, fix ϵ with 0 < ϵ < 1/k, and let p := n[ϵ][−][1]. Let (11.1.5)

_X(G) denote the number of short cycles in a random graph G ∈_ _G(n, p),_ _p, ϵ, X_
i.e. its number of cycles of length at most k.
By Lemma 11.1.5, we have


_k_
�

_n[i]p[i]_ ⩽ [1]2 [(][k][ −] [2)][ n][k][p][k][ ;]
_i=3_


_E(X) =_


_k_
�

_i=3_


(n)i

2i [p][i][ ⩽] 2[1]


note that (np)[i] ⩽ (np)[k], because np = n[ϵ] ⩾ 1. By Lemma 11.1.4,

_P [ X ⩾_ _n/2 ] ⩽_ _E(X)�(n/2)_

⩽ (k − 2) n[k][−][1]p[k]

= (k 2) n[k][−][1]n[(][ϵ][−][1)][k]
_−_

= (k 2) n[kϵ][−][1].
_−_

As kϵ 1 < 0 by our choice of ϵ, this implies that
_−_

lim
_n→∞_ _[P][ [][ X][ ⩾]_ _[n/][2 ] = 0][ .]_

Let n be large enough that P [ X ⩾ _n/2 ] <_ [1]2 [and][ P][ [][ α][ ⩾] 2[1] _[n/k][ ]][ <][ 1]2_ [;] _n_

the latter is possible by our choice of p and Lemma 11.2.1. Then there
is a graph G _[∈]_ _G(n, p) with fewer than n/2 short cycles and α(G) <_
1
2 _[n/k][. From each of those cycles delete a vertex, and let][ H][ be the graph]_
obtained. Then |H| ⩾ _n/2 and H has no short cycles, so g(H) > k. By_
definition of G,

_H_
_|_ _|_
_χ(H) ⩾_

_α(H)_ [⩾] _α[n/](G[2])_ _[> k .]_

                    
**Corollary 11.2.3. There are graphs with arbitrarily large girth and**
_arbitrarily large values of the invariants κ, ε and δ._

(1 4 2)
A


-----

###### 11.3 Properties of almost all graphs

_property_ A graph property is a class of graphs that is closed under isomorphism,
one that contains with every graph G also the graphs isomorphic to G.
If p = p(n) is a fixed function (possibly constant), and is a graph prop_P_
erty, we may ask how the probability P [ G _[∈]_ _P ] behaves for G_ _[∈]_ _G(n, p)_
as n →∞. If this probability tends to 1, we say that G ∈ _P for almost_
_almost all_
_etc._ _all (or almost every) G_ _[∈]_ _G(n, p), or that G_ _[∈]_ _P almost surely; if it_
tends to 0, we say that almost no G _[∈]_ _G(n, p) has the property P. (For_
example, in Lemma 11.2.1 we proved that, for a certain p, almost no
_G_ _[∈]_ _G(n, p) has a set of more than_ [1]2 _[n/k][ independent vertices.)]_

To illustrate the new concept let us show that, for constant p, every
fixed abstract[3] graph H is an induced subgraph of almost all graphs:

**Proposition 11.3.1. For every constant p ∈** (0, 1) and every graph H,
_almost every G_ _[∈]_ _G(n, p) contains an induced copy of H._

_Proof . Let H be given, and k := |H|. If n ⩾_ _k and U ⊆{ 0, . . ., n −_ 1 }
is a fixed set of k vertices of G, then G [ U ] is isomorphic to H with
a certain probability r > 0. This probability r depends on p, but not
on n (why not?). Now G contains a collection of _n/k_ disjoint such
_⌊_ _⌋_
sets U . The probability that none of the corresponding graphs G [ U ] is
isomorphic to H is (1 _r)[⌊][n/k][⌋], since these events are independent by_
_−_
the disjointness of the edges sets [U ][2]. Thus

_P [ H ̸⊆_ _G induced ] ⩽_ (1 − _r)[⌊][n/k][⌋]_ _n−→→∞_ [0][,]

which implies the assertion.       
The following lemma is a simple device enabling us to deduce that
quite a number of natural graph properties (including that of Proposi_Pi,j_ tion 11.3.1) are shared by almost all graphs. Given i, j ∈ N, let Pi,j
denote the property that the graph considered contains, for any disjoint
vertex sets U, W with |U _| ⩽_ _i and |W_ _| ⩽_ _j, a vertex v /[∈]_ _U ∪_ _W that is_
adjacent to all the vertices in U but to none in W .

**Lemma 11.3.2. For every constant p ∈** (0, 1) and i, j ∈ N, almost every
_graph G ∈_ _G(n, p) has the property Pi,j._

3 The word ‘abstract’ is used to indicate that only the isomorphism type of H is
known or relevant, not its actual vertex and edge sets. In our context, it indicates


-----

_Proof . For fixed U, W and v_ _[∈]_ _G −_ (U ∪ _W_ ), the probability that v is
adjacent to all the vertices in U but to none in W, is

_p[|][U]_ _[|]q[|][W][ |]_ ⩾ _p[i]q[j]._

Hence, the probability that no suitable v exists for these U and W, is

(1 − _p[|][U]_ _[|]q[|][W][ |])[n][−|][U]_ _[|−|][W][ |]_ ⩽ (1 − _p[i]q[j])[n][−][i][−][j]_

(for n ⩾ _i + j), since the corresponding events are independent for_
different v. As there are no more than n[i][+][j] pairs of such sets U, W
in V (G) (encode sets U of fewer than i points as non-injective maps
0, . . ., i 1 0, . . ., n 1, etc.), the probability that some such
_{_ _−_ _} →{_ _−_ _}_
pair has no suitable v is at most

_n[i][+][j](1_ _p[i]q[j])[n][−][i][−][j],_
_−_

which tends to zero as n →∞ since 1 − _p[i]q[j]_ _< 1._ 
**Corollary 11.3.3. For every constant p ∈** (0, 1) and k ∈ N, almost every
_graph in_ (n, p) is k-connected.
_G_

_Proof . By Lemma 11.3.2, it is enough to show that every graph in P2,k−1_
is k-connected. But this is easy: any graph in P2,k−1 has order at least
_k + 2, and if W is a set of fewer than k vertices, then by definition of_
_P2,k−1 any other two vertices x, y have a common neighbour v /∈_ _W_ ; in
particular, W does not separate x from y. 
In the proof of Corollary 11.3.3, we showed substantially more than
was asked for: rather than finding, for any two vertices x, y /∈ _W_, some
_x–y path avoiding W_, we showed that x and y have a common neighbour
outside W ; thus, all the paths needed to establish the desired connectivity could in fact be chosen of length 2. What seemed like a clever
trick in this particular proof is in fact indicative of a more fundamental
phenomenon for constant edge probabilities: by an easy result in logic,
any statement about graphs expressed by quantifying over vertices only
(rather than over sets or sequences of vertices)[4] is either almost surely
true or almost surely false. All such statements, or their negations,
are in fact immediate consequences of an assertion that the graph has
property Pi,j, for some suitable i, j.
As a last example of an ‘almost all’ result we now show that almost
every graph has a surprisingly high chromatic number:

4 In the terminology of logic: any first order sentence in the language of graph


-----

**Proposition 11.3.4. For every constant p** _[∈]_ (0, 1) and every ϵ > 0,
_almost every graph G_ _[∈]_ _G(n, p) has chromatic number_


_n_

_χ(G) >_ [log(1][/q][)]

_·_
2 + ϵ log n [.]

(11.1.2) _Proof . For any fixed n ⩾_ _k ⩾_ 2, Lemma 11.1.2 implies


�n� _k_
_P [ α ⩾_ _k ] ⩽_ _q[(]2[)]_
_k_

_k_
2[)]
⩽ _n[k]q[(]_

= q[k][ log]log[ n] q [+][ 1]2 _[k][(][k][−][1)]_


= q


_k2_ �− log(12 log/q n) [+][k][−][1][�]

_._


For
log n
_k := (2 + ϵ)_

log(1/q)

the exponent of this expression tends to infinity with n, so the expression
itself tends to zero. Hence, almost every G _[∈]_ _G(n, p) is such that in any_
vertex colouring of G no k vertices can have the same colour, so every
colouring uses more than


_n_ _n_

_·_

_k_ [= log(1]2 +[/q] ϵ [)] log n

colours. 
By a result of Bollob´as (1988), Proposition 11.3.4 is sharp in the
following sense: if we replace ϵ by _ϵ, then the lower bound given for χ_
_−_
turns into an upper bound.

Most of the results of this section have the interesting common feature that the values of p played no role whatsoever: if almost every
graph in G(n, [1]2 [) had the property considered, then the same was true]

for almost every graph in (n, 1/1000). How could this happen?
_G_
Such insensitivity of our random model to changes of p was certainly
not intended: after all, among all the graphs with a certain property
_P_
it is often those having ‘only just’ that are the most interesting—for
_P_
those graphs are most likely to have different properties too, properties
to which might thus be set in relation. (The proof of Erd˝os’s theorem
_P_
is a good example.) For most properties, however—and this explains the
above phenomenon—the critical order of magnitude of p around which
the property will ‘just’ occur or not occur lies far below any constant


-----

Let us then see what happens if p is allowed to vary with n. Almost immediately, a fascinating picture unfolds. For edge probabilities
_p whose order of magnitude lies below n[−][2], a random graph G_ _[∈]_ _G(n, p)_
almost surely has no edges at all. As p grows, G acquires more and
more structure: from about p = _n n[−][2]_ onwards, it almost surely has

_[√]_
a component with more than two vertices, these components grow into
trees, and around p = n[−][1] the first cycles are born. Soon, some of these
will have several crossing chords, making the graph non-planar. At the
same time, one component outgrows the others, until it devours them
around p = (log n)n[−][1], making the graph connected. Hardly later, at
_p = (1 + ϵ)(log n)n[−][1], our graph almost surely has a Hamilton cycle!_
It has become customary to compare this development of random
graphs as p grows to the evolution of an organism: for each p = p(n),
one thinks of the properties shared by almost all graphs in (n, p) as
_G_
properties of ‘the’ typical random graph G _[∈]_ _G(n, p), and studies how_
_G changes its features with the growth rate of p. As with other species,_
the evolution of random graphs happens in relatively sudden jumps: the
critical edge probabilities mentioned above are thresholds below which
almost no graph and above which almost every graph has the property
considered. More precisely, we call a real function t = t(n) with t(n) = 0
_̸_
_threshold_
for all n a threshold function for a graph property if the following
_P_ _function_
holds for all p = p(n), and G ∈ _G(n, p):_

� 0 if p/t 0 as n
lim _→_ _→∞_
_n→∞_ _[P][ [][ G][ ∈]_ _[P][ ] =]_ 1 if p/t →∞ as n →∞.

If has a threshold function t, then clearly any positive multiple ct of t
_P_
is also a threshold function for ; thus, threshold functions in the above
_P_
sense are only ever unique up to a multiplicative constant.[5]

Which graph properties have threshold functions? Natural candidates for such properties are increasing ones, properties closed under the
addition of edges. (Graph properties of the form _G_ _G_ _H_, with
_{_ _|_ _⊇_ _}_
_H fixed, are common increasing properties; connectedness is another.)_
And indeed, Bollob´as & Thomason (1987) have shown that all increasing
properties, trivial exceptions aside, have threshold functions.
In the next section we shall study a general method to compute
threshold functions.

5 Our notion of threshold reflects only the crudest interesting level of screening:
for some properties, such as connectedness, one can define sharper thresholds where
the constant factor is crucial. Note also the role of the constant factor in our com

-----

###### 11.4 Threshold functions and second moments

Consider a graph property of the form

= _G_ _X(G) > 0_ _,_
_P_ _{_ _|_ _}_

_X ⩾_ 0 where X ⩾ 0 is a random variable on G(n, p). Countless properties can
be expressed naturally in this way; if X denotes the number of spanning
trees, for example, then corresponds to connectedness.
_P_
How could we prove that has a threshold function t? Any such
_P_
proof will consist of two parts: a proof that almost no G _[∈]_ _G(n, p) has_
when p is small compared with t, and one showing that almost every
_P_
_G has_ when p is large.
_P_
If X is integral, we may use Markov’s inequality for the first part
of the proof and find an upper bound for E(X) instead of P [ X > 0 ]:
if E(X) is small then X(G) can be positive—and hence at least 1—only
for few G _[∈]_ _G(n, p). Besides, the expectation is much easier to calculate_
than probabilities: without worrying about such things as independence
or incompatibility of events, we may compute the expectation of a sum of
random variables—for example, of indicator random variables—simply
by adding up their individual expected values.
For the second part of the proof, things are more complicated. In
order to show that P [ X > 0 ] is large, it is not enough to bound E(X)
from below: since X is not bounded above, E(X) may be large simply
because X is very large on just a few graphs G—so X may still be zero
for most G _[∈]_ _G(n, p).[6]_ In order to prove that P [ X > 0 ] → 1, we thus
have to show that this cannot happen, i.e. that X does not deviate a lot
from its mean too often.
The following elementary tool from probability theory achieves just
that. As is customary, we write

_µ_ _µ := E(X)_

and define σ ⩾ 0 by setting

_σ[2]_ _σ[2]_ := E�(X _µ)[2][�]_ _._
_−_

This quantity σ[2] is called the variance or second moment of X; by
definition, it is a (quadratic) measure of how much X deviates from its
mean. Since E is linear, the defining term for σ[2] expands to

_σ[2]_ = E(X [2] 2µX + µ[2]) = E(X [2]) _µ[2]._
_−_ _−_

6 For some p between n−1 and (log n)n−1, for example, almost every G ∈ _G(n, p)_
has an isolated vertex (and hence no spanning tree), but its expected number of


-----

Note that µ and σ[2] always refer to a random variable on some fixed
probability space. In our setting, where we consider the spaces (n, p),
_G_
both quantities are functions of n.
The following lemma says exactly what we need: that X cannot
deviate a lot from its mean too often.

**Lemma 11.4.1. (Chebyshev’s Inequality)**
_For all real λ > 0,_

_P_ � _|X −_ _µ| ⩾_ _λ_ � ⩽ _σ[2]/λ[2]._

_Proof . By Lemma 11.1.4 and definition of σ[2],_ (11.1.4)

_P [ |X −_ _µ| ⩾_ _λ ] = P [ (X −_ _µ)[2]_ ⩾ _λ[2]_ ] ⩽ _σ[2]/λ[2]._

                    
For a proof that X(G) > 0 for almost all G _[∈]_ _G(n, p), Chebyshev’s_
inequality can be used as follows:

**Lemma 11.4.2. If µ > 0 for n large, and σ[2]/µ[2]** 0 as n _, then_
_→_ _→∞_
_X(G) > 0 for almost all G_ _[∈]_ _G(n, p)._

_Proof . Any graph G with X(G) = 0 satisfies_ _X(G)_ _µ_ = µ. Hence
_|_ _−_ _|_
Lemma 11.4.1 implies with λ := µ that

_P [ X = 0 ] ⩽_ _P_ � _|X −_ _µ| ⩾_ _µ_ � ⩽ _σ[2]/µ[2]_ _n−→→∞_ [0][ .]

Since X ⩾ 0, this means that X > 0 almost surely, i.e. that X(G) > 0
for almost all G _[∈]_ _G(n, p)._ 
As the main result of this section, we now prove a theorem that will
at once give us threshold functions for a number of natural properties.
Given a graph H, we denote by PH the graph property of containing a _PH_
copy of H as a subgraph. We shall call H balanced if ε(H _[′]) ⩽_ _ε(H) for_ _balanced_
all subgraphs H _[′]_ of H.

**Theorem 11.4.3. (Erd˝os & R´enyi 1960)**
_If H is a balanced graph with k vertices and ℓ_ ⩾ 1 edges, then t(n) := _k, ℓ_
_k/ℓ_


-----

(11.1.4) _Proof . Let X(G) denote the number of subgraphs of G isomorphic to H._
(11.1.5)

_X_ Given n ∈ N, let H denote the set of all graphs isomorphic to H whose
vertices lie in { 0, . . ., n − 1 }, the vertex set of the graphs G _[∈]_ _G(n, p):_

_H_ _H :=_ �H _[′]_ _| H_ _[′]_ _≃_ _H, V (H_ _[′]) ⊆{ 0, . . ., n −_ 1 }� _._

Given H _[′ ∈]_ _H and G ∈_ _G(n, p), we shall write H_ _[′]_ _⊆_ _G to express that_
_H_ _[′]_ itself—not just an isomorphic copy of H _[′]—is a subgraph of G._
_h_ By h we denote the number of isomorphic copies of H on a fixed
_k-set; clearly, h ⩽_ _k! . As there are_ �nk� possible vertex sets for the graphs
in, we thus have
_H_


�n� �n�
_|H| =_ _h ⩽_ _k! ⩽_ _n[k]._ (1)
_k_ _k_


_p, γ_ Given p = p(n), we set γ := p/t; then

_p = γn[−][k/ℓ]._ (2)

We have to show that almost no G ∈ _G(n, p) lies in PH if γ →_ 0 as n _→∞,_
and that almost all G _[∈]_ _G(n, p) lie in PH if γ →∞_ as n →∞.
For the first part of the proof, we find an upper bound for E(X), the
expected number of subgraphs of G isomorphic to H. As in the proof of
Lemma 11.1.5, double counting gives

�
_E(X) =_ _P [ H_ _[′]_ _G ] ._ (3)

_⊆_
_H_ _[′ ∈]H_

For every fixed H _[′ ∈]_ _H, we have_

_P [ H_ _[′]_ _G ] = p[ℓ],_ (4)
_⊆_

because _H_ = ℓ. Hence,
_∥_ _∥_

_E(X) =_ ⩽ _n[k](γn[−][k/ℓ])[ℓ]_ = γ[ℓ]. (5)
(3,4) _[|H|][ p][ℓ]_ (1,2)

Thus if γ 0 as n, then
_→_ _→∞_

_P [ G_ _[∈]_ _PH ] = P [ X ⩾_ 1 ] ⩽ _E(X) ⩽_ _γ[ℓ]_ _n−→→∞_ [0]


-----

We now come to the second part of the proof: we show that almost
all G ∈ _G(n, p) lie in PH if γ →∞_ as n →∞. Note first that, for n ⩾ _k,_


�


�n� 1

_n[−][k]_ =

_k_ _k!_


� _n_

_n_ _n_

_[· · ·][ n][ −]_ _[k][ + 1]_


�k

�k
; (6)


1
⩾

_k!_

1
⩾

_k!_


� _n_ _k + 1_
_−_

_n_

�
1
_−_ _[k][ −]_ [1]

_k_


thus, n[k] exceeds �nk� by no more than a factor independent of n.
Our goal is to apply Lemma 11.4.2, and hence to bound σ[2]/µ[2] =
�E(X [2]) _µ[2][�]/µ[2]_ from above. As in (3) we have
_−_

�
_E(X_ [2]) = _P [ H_ _[′]_ _H_ _[′′]_ _G ] ._ (7)

_∪_ _⊆_
(H _[′],H_ _[′′])_ _∈H[2]_

Let us then calculate these probabilities P [ H _[′]_ _H_ _[′′]_ _G ]._ Given
_∪_ _⊆_
_H_ _[′], H_ _[′′ ∈]_ _H, we have_

_P [ H_ _[′]_ _∪_ _H_ _[′′]_ _⊆_ _G ] = p[2][ℓ][−∥][H]_ _[′][∩][H]_ _[′′][∥]._

Since H is balanced, ε(H _[′]_ _∩_ _H_ _[′′]) ⩽_ _ε(H) = ℓ/k. With |H_ _[′]_ _∩_ _H_ _[′′]| =: i_ _i_
this yields ∥H _[′]_ _∩_ _H_ _[′′]∥_ ⩽ _iℓ/k, so by 0 ⩽_ _p ⩽_ 1,

_P [ H_ _[′]_ _∪_ _H_ _[′′]_ _⊆_ _G ] ⩽_ _p[2][ℓ][−][iℓ/k]._ (8)

We have now estimated the individual summands in (7); what does
this imply for the sum as a whole? Since (8) depends on the parameter
_i = |H_ _[′]_ _∩_ _H_ _[′′]|, we partition the range H[2]_ of the sum in (7) into the
subsets

_Hi[2]_ [:=] � (H _[′], H_ _[′′]) ∈_ _H[2]_ : |H _[′]_ _∩_ _H_ _[′′]| = i_ � _,_ _i = 0, . . ., k,_ _Hi[2]_

and calculate for each Hi[2] [the corresponding sum]


�
_Ai :=_


_i_ _[P][ [][ H]_ _[′][ ∪]_ _[H]_ _[′′][ ⊆]_ _[G][ ]]_ _Ai_


by itself. (Here, as below, we use [�]i [to denote sums over all pairs] �i

(H _[′], H_ _[′′])_ _[∈]_ _Hi[2][.)]_
If i = 0 then H _[′]_ and H _[′′]_ are disjoint, so the events H _[′]_ _⊆_ _G and_
_H_ _[′′]_ _G are independent. Hence,_
_⊆_

�


-----

�
=

0 _[P][ [][ H]_ _[′][ ⊆]_ _[G][ ]][ ·][ P][ [][ H]_ _[′′][ ⊆]_ _[G][ ]]_


�
⩽ _P [ H_ _[′]_ _⊆_ _G ] · P [ H_ _[′′]_ _⊆_ _G ]_

(H _[′],H_ _[′′])_ _∈H[2]_

�� � �� �
= _P [ H_ _[′]_ _G ]_ _P [ H_ _[′′]_ _G ]_

_⊆_ _·_ _⊆_
_H_ _[′ ∈]H_ _H_ _[′′ ∈]H_


= (9)
(3) _[µ][2][.]_

Let us now estimate Ai for i ⩾ 1. Writing [�][′] for [�]H _[′ ∈]H_ [and][ �][′′]

�′ for [�]H _[′′ ∈]H_ _[,][ we note that][ �]i_ [can be written as][ �][′][ �][′′]|H _[′]∩H_ _[′′]|=i_ [. For]

fixed H _[′]_ (corresponding to the first sum [�][′]), the second sum ranges
over
�k��n _k�_

_−_

_h_

_i_ _k_ _i_

_−_


summands: the number of graphs H _[′′ ∈]_ with _H_ _[′′]_ _H_ _[′]_ = i. Hence,
_H_ _|_ _∩_ _|_
for all i ⩾ 1 and suitable constants c1, c2 independent of n,


�
_Ai =_

_i_ _[P][ [][ H]_ _[′][ ∪]_ _[H]_ _[′′][ ⊆]_ _[G][ ]]_


��n _k_
_−_
_k_ _i_
_−_


�
_h p[2][ℓ]p[−][iℓ/k]_


⩽
(8)


�′ [�]k
_i_


�
_h p[2][ℓ][�]γ n[−][k/ℓ][�][−][iℓ/k]_


�k
=
(2) _i_

_[|H|]_


��n _k_
_−_
_k_ _i_
_−_


⩽ _|H| p[ℓ]c1 n[k][−][i]_ _h p[ℓ]γ[−][iℓ/k]_ _n[i]_

=
(5) _[µ c][1][n][k][h p][ℓ][γ][−][iℓ/k]_


�n�

⩽ _µ c2_ _h p[ℓ]γ[−][iℓ/k]_
(6) _k_


=
(1,5) _[µ][2][c][2][γ][−][iℓ/k]_

⩽ _µ[2]c2γ[−][ℓ/k]_

if γ ⩾ 1. By definition of the Ai, this implies with c3 := kc2 that


_E(X_ [2])/µ[2] =
(7)


_k_

� �
_A0/µ[2]_ + _Ai/µ[2][�]_ ⩽ 1 + c3γ[−][ℓ/k]

(9)
_i=1_


and hence
_σ[2]_ _E(X_ [2]) _µ[2]_
_−_


⩽ _−ℓ/k_ 0


-----

By Lemma 11.4.2, therefore, X > 0 almost surely, i.e. almost all G _[∈]_
_G(n, p) have a subgraph isomorphic to H and hence lie in PH_ . 
Theorem 11.4.3 allows us to read off threshold functions for a number of natural graph properties.

**Corollary 11.4.4. If k ⩾** 3, then t(n) = n[−][1] _is a threshold function for_
_the property of containing a k-cycle._ 
Interestingly, the threshold function in Corollary 11.4.4 is independent of the cycle length k considered: in the evolution of random graphs,
cycles of all (constant) lengths appear at about the same time!
There is a similar phenomenon for trees. Here, the threshold function does depend on the order of the tree considered, but not on its
shape:

**Corollary 11.4.5. If T is a tree of order k ⩾** 2, then t(n) = n[−][k/][(][k][−][1)]

_is a threshold function for the property of containing a copy of T_ _._

We finally have the following result for complete subgraphs:

**Corollary 11.4.6. If k ⩾** 2, then t(n) = n[−][2][/][(][k][−][1)] _is a threshold func-_
_tion for the property of containing a K_ _[k]._

_Proof . K_ _[k]_ is balanced, because ε(K _[i]) =_ [1]2 [(][i] _[−]_ [1)][ <][ 1]2 [(][k][ −] [1) =][ ε][(][K] _[k][) for]_

_i < k. With ℓ_ := ∥K _[k]∥_ = [1]2 _[k][(][k][ −]_ [1), we obtain][ n][−][k/ℓ] [=][ n][−][2][/][(][k][−][1)][.] 
It is not difficult to adapt the proof of Theorem 11.4.3 to the case
that H is unbalanced. The threshold then becomes t(n) = n[−][1][/ε][′][(][H][)],
where ε[′](H) := max { ε(F ) | F ⊆ _H }; see Exercise 22._

###### Exercises

1.[−] What is the probability that a random graph in G(n, p) has exactly m
edges, for 0 ⩽ _m ⩽_ [�][n]2� fixed?

2. What is the expected number of edges in G _[∈]_ _G(n, p)?_

3. What is the expected number of K _[r]-subgraphs in G_ _[∈]_ _G(n, p)?_

4. Characterize the graphs that occur as a subgraph in every graph of
sufficiently large average degree.

5. In the usual terminology of measure spaces (and in particular, of probability spaces), the phrase ‘almost all’ is used to refer to a set of points
whose complement has measure zero. Rather than considering a limit
of probabilities in G(n, p) as n →∞, would it not be more natural to
define a probability space on the set of all finite graphs (one copy of
each) and to investigate properties of ‘almost all’ graphs in this space,


-----

6. Show that if almost all G _[∈]_ _G(n, p) have a graph property P1 and almost_
all G _[∈]_ _G(n, p) have a graph property P2, then almost all G_ _[∈]_ _G(n, p)_
have both properties, i.e. have the property P1 ∩P2.

7.[−] Show that, for constant p _[∈]_ (0, 1), almost every graph in G(n, p) has
diameter 2.

8. Show that, for constant p _[∈]_ (0, 1), almost no graph in G(n, p) has a
separating complete subgraph.

9. Derive Proposition 11.3.1 from Lemma 11.3.2.

10.[+] (i) Show that with probability 1 an infinite random graph G _[∈]_ _G(ℵ0, p)_
has all the properties Pi,j (i, j _[∈]_ N).

(ii) Show that any two (infinite) graphs having all the properties Pi,j
are isomorphic.

(Thus, up to isomorphism, there is only one countably infinite random
graph.)

11. Let ϵ > 0 and p = p(n) > 0, and let r ⩾ (1 + ϵ)(2 ln n)/p be an integervalued function of n. Show that almost no graph in G(n, p) contains r
independent vertices.

12. Show that for every graph H there exists a function p = p(n) such that
limn→∞ _p(n) = 0 but almost every G_ _[∈]_ _G(n, p) contains an induced_
copy of H.

13.[+] (i) Show that, for every 0 < ϵ ⩽ 1 and p = (1 − _ϵ)(ln n)n[−][1], almost_
every G _[∈]_ _G(n, p) has an isolated vertex._

(ii) Find a probability p = p(n) such that almost every G _[∈]_ _G(n, p) is_
disconnected but the expected number of spanning trees of G tends to
infinity as n →∞.

(Hint for (ii): A theorem of Cayley states that K _[n]_ has exactly n[n][−][2]

spanning trees.)

14.[+] Given r _∈_ N, find a c > 0 such that, for p = cn[−][1], almost every
_G_ _[∈]_ _G(n, p) has a K_ _[r]_ minor. Can c be chosen independently of r?

15. Find an increasing graph property without a threshold function, and a
property that is not increasing but has a threshold function.

16.[−] Let H be a graph of order k, and let h denote the number of graphs
isomorphic to H on some fixed set of k elements. Show that h ⩽ _k!._
For which graphs H does equality hold?

17.[−] For every k ⩾ 1, find a threshold function for { G | ∆(G) ⩾ _k }._

18.[−] Given d _[∈]_ N, is there a threshold function for the property of containing
a d-dimensional cube (see Ex. 2, Ch. 1)? If so, which; if not, why not?

19. Show that t(n) = n[−][1] is also a threshold function for the property of
containing any cycle.

20. Does the property of containing any tree of order k (for k ⩾ 2 fixed)


-----

21.[+] Given a graph H, let P be the property of containing an induced copy
of H. If H is complete then, by Corollary 11.4.6, P has a threshold
function. Show that P has no threshold function if H is not complete.

22.[+] Prove the following version of Theorem 11.4.3 for unbalanced subgraphs. Let H be any graph with at least one edge, and put ε[′](H) :=
max { ε(F ) | ∅̸= F ⊆ _H }._ Then the threshold function for PH is
_t(n) = n[−][1][/ε][′][(][H][)]._

(Hint. Imitate the proof of Theorem 11.4.3. Instead of the sets Hi,
consider the sets HF[2] [:=][ {][ (][H] _[′][, H]_ _[′′][)][ ∈]_ _[H][2][ |][ H]_ _[′][ ∩]_ _[H]_ _[′′][ =][ F][ }][. Replace]_
the distinction between the cases of i = 0 and i > 0 by the distinction
between the cases of ∥F _∥_ = 0 and ∥F _∥_ _> 0.)_

###### Notes

There are a number of monographs and texts on the subject of random
graphs. The most comprehensive of these is B. Bollob´as, Random Graphs,
Academic Press 1985. Another advanced but very readable monograph is
S. Janson, T. �Luczak & A. Ruci´nski, Topics in Random Graphs, in preparation; this concentrates on areas developed since Random Graphs was published. E.M. Palmer, Graphical Evolution, Wiley 1985, covers material similar
to parts of Random Graphs but is written in a more elementary way. Compact introductions going beyond what is covered in this chapter are given
by B. Bollob´as, Graph Theory, Springer GTM 63, 1979, and by M. Karo´nski,
_Handbook of Combinatorics (R.L. Graham, M. Gr¨otschel & L. Lov´asz, eds.),_
North-Holland 1995.
A stimulating advanced introduction to the use of random techniques in
discrete mathematics more generally is given by N. Alon & J.H. Spencer, The
_Probabilistic Method, Wiley 1992. One of the attractions of this book lies_
in the way it shows probabilistic methods to be relevant in proofs of entirely
deterministic theorems, where nobody would suspect it. Another example for
this phenomenon is Alon’s proof of Theorem 5.4.1; see the notes for Chapter 5.
The probabilistic method had its first origins in the 1940s, one of its
earliest results being Erd˝os’s probabilistic lower bound for Ramsey numbers
(Theorem 11.1.3). Lemma 11.3.2 about the properties Pi,j is taken from Bollob´as’s Springer text cited above. A very readable rendering of the proof that,
for constant p, every first order sentence about graphs is either almost surely
true or almost surely false, is given by P. Winkler, Random structures and
zero-one laws, in (N.W. Sauer et al., eds.) Finite and Infinite Combinatorics
_in Sets and Logic (NATO ASI Series C 411), Kluwer 1993._
The seminal paper on graph evolution is P. Erd˝os & A. R´enyi, On the
evolution of random graphs, Publ. Math. Inst. Hungar. Acad. Sci. 5 (1960),
17–61. This paper also includes Theorem 11.4.3 and its proof. The generalization of this theorem to unbalanced subgraphs was first proved by Bollob´as in
1981, using advanced methods; a simple adaptation of the original Erd˝os-Renyi
proof was found by Ruci´nski & Vince (1986), and is presented in Karo´nski’s


-----

There is another way of defining a random graph G, which is just as
natural and common as the model we considered. Rather than choosing the
edges of G independently, we choose the entire graph G uniformly at random
from among all the graphs on { 0, . . ., n − 1 } that have exactly M = M (n)
edges: then each of these graphs occurs with the same probability of _M�,_

[�][N]
where N := 2�. Just as we studied the likely properties of the graphs in

[�][n]
_G(n, p) for different functions p = p(n), we may investigate how the properties_
of G in the other model depend on the function M (n). If M is close to pN, the
expected number of edges of a graph in G(n, p), then the two models behave
very similarly. It is then largely a matter of convenience which of them to
consider; see Bollob´as for details.
In order to study threshold phenomena in more detail, one often considers
the following random graph process: starting with a K _[n]_ as stage zero, one
chooses additional edges one by one (uniformly at random) until the graph
is complete. This is a simple example of a Markov chain, whose M th stage
corresponds to the ‘uniform’ random graph model described above. A survey
about threshold phenomena in this setting is given by T. �Luczak, The phase
transition in a random graph, in (D. Mikl´os, V.T. S´os & T. Sz˝onyi, eds.) Paul
_Erd˝os is 80, Vol. 2, Proc. Colloq. Math. Soc. J´anos Bolyai (1996)._


-----

# 12 Minors,
### Trees, and WQO

Our goal in this last chapter is a single theorem, one which dwarfs any
other result in graph theory and may doubtless be counted among the
deepest theorems that mathematics has to offer: in every infinite set of
_graphs there are two such that one is a minor of the other. This graph_
_minor theorem (or minor theorem for short), inconspicuous though it_
may look at first glance, has made a fundamental impact both outside
graph theory and within. Its proof, due to Neil Robertson and Paul
Seymour, takes well over 500 pages.
So we have to be modest: of the actual proof of the minor theorem,
this chapter will convey only a very rough impression. However, as with
most truly fundamental results, the proof has sparked off the development of methods of quite independent interest and potential. This is
true particularly for the use of tree-decompositions, a technique we shall
meet in Sections 12.3 and 12.4. Section 12.1 gives an introduction to well_quasi-ordering, a concept central to the minor theorem. In Section 12.2_
we apply this concept to prove the minor theorem for trees. The chapter
finishes with an overview in Section 12.5 of the proof of the general graph
minor theorem, and of some of its immediate consequences.

###### 12.1 Well-quasi-ordering

A reflexive and transitive relation is called a quasi-ordering. A quasi_well-quasi-_
ordering ⩽ on X is a well-quasi-ordering, and the elements of X are _ordering_


-----

_good pair_ there are indices i < j such that xi ⩽ _xj. Then (xi, xj) is a good pair_
of this sequence. A sequence containing a good pair is a good sequence;
_good/bad_
thus, a quasi-ordering on X is a well-quasi-ordering if and only if every
_sequence_
infinite sequence in X is good. An infinite sequence is bad if it is not
good.

**Proposition 12.1.1. A quasi-ordering ⩽** _on X is a well-quasi-ordering_
_if and only if X contains neither an infinite antichain nor an infinite_
_strictly decreasing sequence x0 > x1 > . . .._

(9.1.2) _Proof ._ The forward implication is trivial. Conversely, let x0, x1, . . .
be any infinite sequence in X. Let K be the complete graph on N =
0, 1, . . . . Colour the edges ij (i < j) of K with three colours: green
_{_ _}_
if xi ⩽ _xj, red if xi > xj, and amber if xi, xj are incomparable. By_
Ramsey’s theorem (9.1.2), K has an infinite induced subgraph whose
edges all have the same colour. If there is neither an infinite antichain
nor an infinite strictly decreasing sequence in X, then this colour must
be green, i.e. x0, x1, . . . has an infinite subsequence in which every pair
is good. In particular, the sequence x0, x1, . . . is good.       
In the proof of Proposition 12.1.1, we showed more than was needed:
rather than finding a single good pair in x0, x1, . . ., we found an infinite
increasing subsequence. We have thus shown the following:

**Corollary 12.1.2. If X is well-quasi-ordered, then every infinite se-**
_quence in X has an infinite increasing subsequence._       
The following lemma, and the idea of its proof, are fundamental to
the theory of well-quasi-ordering. Let ⩽ be a quasi-ordering on a set X.
⩽ For finite subsets A, B ⊆ _X, write A ⩽_ _B if there is an injective mapping_
_f_ : A → _B such that a ⩽_ _f_ (a) for all a ∈ _A. This naturally extends ⩽_ to

[X][<ω] a quasi-ordering on [X][<ω], the set of all finite subsets of X.

[ 12.2.1 ] **Lemma 12.1.3. If X is well-quasi-ordered by ⩽, then so is [X][<ω].**

_Proof . Suppose that ⩽_ is a well-quasi-ordering on X but not on [X][<ω].
We start by constructing a bad sequence (An)n _∈N in [X][<ω], as follows._
Given n ∈ N, assume inductively that Ai has been defined for every
_i < n, and that there exists a bad sequence in [X][<ω]_ starting with
_A0, . . ., An−1. (This is clearly true for n = 0: by assumption, [X][<ω]_

contains a bad sequence, and this has the empty sequence as an initial
segment.) Choose An ∈ [X][<ω] so that some bad sequence in [X][<ω] starts
with A0, . . ., An and |An| is as small as possible.
Clearly, (An)n _∈N is a bad sequence in [X][<ω]; in particular, An ̸= ∅_


-----

By Corollary 12.1.2, the sequence (an)n _∈N has an infinite increasing_
subsequence (ani)i _∈N. By the minimal choice of An0, the sequence_

_A0, . . ., An0−1, Bn0, Bn1, Bn2, . . ._

is good; consider a good pair. Since (An)n _∈N is bad, this pair cannot_
have the form (Ai, Aj) or (Ai, Bj), as Bj ⩽ _Aj._ So it has the form
(Bi, Bj). Extending the injection Bi _Bj by ai_ _aj, we deduce again_
_→_ _�→_
that (Ai, Aj) is good, a contradiction. 
###### 12.2 The graph minor theorem for trees

The minor theorem can be expressed by saying that the finite graphs
are well-quasi-ordered by the minor relation ≼. Indeed, by Proposition 12.1.1 and the obvious fact that no strictly descending sequence
of minors can be infinite, being well-quasi-ordered is equivalent to the
non-existence of an infinite antichain, the formulation used earlier.
In this section, we prove a strong version of the graph minor theorem
for trees:

**Theorem 12.2.1. (Kruskal 1960)**
_The finite trees are well-quasi-ordered by the topological minor relation._

We shall base the proof of Theorem 12.2.1 on the following notion
of an embedding between rooted trees, which strengthens the usual embedding as a topological minor. Consider two trees T and T _[′], with roots_
_r and r[′]_ say. Let us write T ⩽ _T_ _[′]_ if there exists an isomorphism ϕ, from _T ⩽_ _T_ _[′]_
some subdivision of T to a subtree T _[′′]_ of T _[′], that preserves the tree-order_
on V (T ) associated with T and r. (Thus if x < y in T then ϕ(x) < ϕ(y)
in T _[′]; see Fig. 12.2.1.) As one easily checks, this is a quasi-ordering on_
the class of all rooted trees.

_ϕ(r)_
_ϕ_

_T_
_r_

_T_ _[′]_

_r[′]_


-----

(12.1.3) **Proof of Theorem 12.2.1. We show that the rooted trees are well-**
quasi-ordered by the relation ⩽ defined above; this clearly implies the
theorem.
Suppose not. To derive a contradiction, we proceed as in the proof
of Lemma 12.1.3. Given n _[∈]_ N, assume inductively that we have chosen
a sequence T0, . . ., Tn−1 of rooted trees such that some bad sequence of
_Tn_ rooted trees starts with this sequence. Choose as Tn a minimum-order
rooted tree such that some bad sequence starts with T0, . . ., Tn. For each
_rn_ _n_ _[∈]_ N, denote the root of Tn by rn.
_An_ Clearly, (Tn)n _∈N is a bad sequence. For each n, let An denote the_
set of components of Tn − _rn, made into rooted trees by choosing the_
neighbours of rn as their roots. Note that the tree-order of these trees

_A_ is that induced by Tn. Let us prove that the set A := [�]n _∈N_ _[A][n][ of all]_
these trees is well-quasi-ordered.
_T_ _[k]_ Let (T _[k])k_ _∈N be any sequence of trees in A. For every k_ _[∈]_ N choose
_n(k)_ an n = n(k) such that T _[k][ ∈]_ _An. Pick a k with smallest n(k). Then_

_T0, . . ., Tn(k)−1, T_ _[k], T_ _[k][+1], . . ._

is a good sequence, by the minimal choice of Tn(k) and T _[k]_ ⫋ _Tn(k). Let_
(T, T _[′]) be a good pair of this sequence. Since (Tn)n_ _∈N is bad, T cannot_
be among the first n(k) members T0, . . ., Tn(k)−1 of our sequence: then
_T_ _[′]_ would be some T _[i]_ with i ⩾ _k, i.e._

_T ⩽_ _T_ _[′]_ = T _[i]_ ⩽ _Tn(i) ;_

since n(k) ⩽ _n(i) by the choice of k, this would make (T, Tn(i)) a good_
pair in the bad sequence (Tn)n _∈N. Hence (T, T_ _[′]) is a good pair also in_
(T _[k])k_ _∈N, completing the proof that A is well-quasi-ordered._
By Lemma 12.1.3,[1] the sequence (An)n _∈N in [A][<ω]_ has a good pair
_i, j_ (Ai, Aj); let f : Ai → _Aj be an injection such that T ⩽_ _f_ (T ) for all T _[∈]_ _Ai._
We now extend the union of the embeddings T _f_ (T ) to a map ϕ from
_→_
_V (Ti) to V (Tj) by letting ϕ(ri) := rj. This map ϕ preserves the tree-_
order of Ti, and it defines an embedding to show that Ti ⩽ _Tj, since the_
edges rir _[∈]_ _Ti map naturally to the paths rjTjϕ(r). Hence (Ti, Tj) is a_
good pair in our original bad sequence of rooted trees, a contradiction.

                       
1 Any readers worried that we might need the lemma for sequences or multisets rather than just sets here, please note that isomorphic elements of An are not


-----

###### 12.3 Tree-decompositions

Trees are graphs with some very distinctive and fundamental properties;
consider Theorem 1.5.1 and Corollary 1.5.2, or the more sophisticated
example of Kruskal’s theorem. It is therefore legitimate to ask to what
degree those properties can be transferred to more general graphs, graphs
that are not themselves trees but tree-like in some sense.[2] In this section,
we study a concept of tree-likeness that permits generalizations of all
the tree properties referred to above (including Kruskal’s theorem), and
which plays a crucial role in the proof of the graph minor theorem.
Let G be a graph, T a tree, and let V = (Vt)t∈T be a family of vertex
sets Vt ⊆ _V (G) indexed by the vertices t of T_ . The pair (T, V) is called
a tree-decomposition of G if it satisfies the following three conditions:
_tree-_
(T1) V (G) = [�]t∈T _[V][t][;]_ _decomposition_

(T2) for every edge e ∈ _G there exists a t ∈_ _T such that both ends of e_
lie in Vt;

(T3) Vt1 ∩ _Vt3 ⊆_ _Vt2 whenever t1, t2, t3 ∈_ _T satisfy t2 ∈_ _t1Tt3._

Conditions (T1) and (T2) together say that G is the union of the subgraphs G [ Vt ]; we call these subgraphs and the sets Vt themselves the
_parts of (T,_ ) and say that (T, ) is a tree-decomposition of G into these _parts_
_V_ _V_
parts. Condition (T3) implies that the parts of (T, ) are organized _into_
_V_
roughly like a tree (Fig. 12.3.1).


_t1_


_Vt3_


?


_t3_ _e?_
_t?_

?

_t2_

_T_
_G_

_Fig. 12.3.1. Edges and parts ruled out by (T2) and (T3)_

Before we discuss the role that tree-decompositions play in the proof
of the minor theorem, let us note some of their basic properties. Consider
a fixed tree-decomposition (T, V) of G, with V = (Vt)t∈T as above. (T, V), Vt
Perhaps the most important feature of a tree-decomposition is that
it transfers the separation properties of its tree to the graph decomposed:

2 What exactly this ‘sense’ should be will depend both on the property considered


-----

**Lemma 12.3.1. Let t1t2 be any edge of T and let T1, T2 be the com-**
_ponents of T −_ _t1t2, with t1 ∈_ _T1 and t2 ∈_ _T2. Then Vt1 ∩_ _Vt2 separates_
_U1 :=_ [�]t∈T1 _[V][t][ from][ U][2][ :=][ �]t∈T2_ _[V][t][ in][ G][ (Fig. 12.3.2).]_

_T2_
_T1_ _t2_ _U2_

_U1_ _t1_

_Vt1 ∩_ _Vt2_

_Fig. 12.3.2. Vt1 ∩_ _Vt2 separates U1 from U2 in G_

_Proof . Both t1 and t2 lie on every t–t[′]_ path in T with t ∈ _T1 and t[′ ∈]_ _T2._
Therefore U1 ∩ _U2 ⊆_ _Vt1 ∩_ _Vt2 by (T3), so all we have to show is that G_
has no edge u1u2 with u1 ∈ _U1 ∖_ _U2 and u2 ∈_ _U2 ∖_ _U1. If u1u2 is such_
an edge, then by (T2) there is a t ∈ _T with u1, u2 ∈_ _Vt. By the choice of_
_u1 and u2 we have neither t ∈_ _T2 nor t ∈_ _T1, a contradiction._      
Note that tree-decompositions are passed on to subgraphs:

[ 12.4.2 ] **Lemma 12.3.2. For every H ⊆** _G, the pair_ �T, (Vt ∩ _V (H))t∈T_ � _is a_
_tree-decomposition of H._      
Similarly for contractions:

**Lemma 12.3.3. Suppose that G is an MH with branch sets Uh,**
_h_ _[∈]_ _V (H)._ _Let f_ : V (G) → _V (H) be the map assigning to each ver-_
_tex of G the index of the branch set containing it. For all t ∈_ _T let_
_Wt := { f_ (v) | v ∈ _Vt }, and put W := (Wt)t∈T . Then (T, W) is a tree-_
_decomposition of H._

_Proof ._ The assertions (T1) and (T2) for (T, ) follow immediately
_W_
from the corresponding assertions for (T, V). Now let t1, t2, t3 ∈ _T be_
as in (T3), and consider a vertex h ∈ _Wt1_ _Wt3 of H; we show that_
_∩_
_h ∈_ _Wt2. By definition of Wt1 and Wt3, there are vertices v1 ∈_ _Vt1 ∩_ _Uh_
and v3 ∈ _Vt3 ∩_ _Uh. Since Uh is connected in G and Vt2 separates v1 from_
_v3 in G by Lemma 12.3.1, Vt2 has a vertex in Uh. By definition of Wt2,_
this implies h ∈ _Wt2._       

-----

**Lemma 12.3.4. Given a set W ⊆** _V (G), there is either a t_ _[∈]_ _T such_
_that W ⊆_ _Vt, or there are vertices w1, w2 ∈_ _W and an edge t1t2 ∈_ _T such_
_that w1, w2 lie outside the set Vt1_ _Vt2 and are separated by it in G._
_∩_

_Proof . Let us orient the edges of T as follows. For each edge t1t2_ _[∈]_ _T_,
define U1, U2 as in Lemma 12.3.1; then Vt1 _Vt2 separates U1 from U2._
_∩_
If Vt1 _Vt2 does not separate any two vertices of W that lie outside it,_
_∩_
we can find an i _[∈]_ _{ 1, 2 } such that W ⊆_ _Ui, and orient t1t2 towards ti._
Let t be the last vertex of a maximal directed path in T ; we claim
that W ⊆ _Vt. Given w_ _[∈]_ _W_, let t[′ ∈] _T be such that w_ _[∈]_ _Vt[′]_ . If t[′] ≠ _t,_
then the edge e at t that separates t[′] from t in T is directed towards t,
so w also lies in Vt[′′] for some t[′′] in the component of T − _e containing t._
Therefore w _[∈]_ _Vt by (T3)._ 
The following special case of Lemma 12.3.4 is used particularly often:

**Lemma 12.3.5. Any complete subgraph of G is contained in some part** [ 12.4.2 ]
_of (T, V)._ 
As indicated by Figure 12.3.1, the parts of (T, ) reflect the struc_V_
ture of the tree T, so in this sense the graph G decomposed resembles a
tree. However, this is valuable only inasmuch as the structure of G within
each part is negligible: the smaller the parts, the closer the resemblance.
This observation motivates the following definition. The width of _width_
(T, ) is the number
_V_

max �|Vt| − 1 : t ∈ _T_ � _,_

_tree-width_
and the tree-width tw(G) of G is the least width of any tree-decompositw(G)
tion of G. As one easily checks,[3] trees themselves have tree-width 1.
By Lemmas 12.3.2 and 12.3.3, the tree-width of a graph will never
be increased by deletion or contraction:

**Proposition 12.3.6. If H ≼** _G then tw(H) ⩽_ tw(G). 
Graphs of bounded tree-width are sufficiently similar to trees that it
becomes possible to adapt the proof of Kruskal’s theorem to the class of
these graphs; very roughly, one has to iterate the ‘minimal bad sequence’
argument from the proof of Lemma 12.1.3 tw(G) times. This takes us a
step further towards a proof of the graph minor theorem:

**Theorem 12.3.7. (Robertson & Seymour 1990)**
_For every integer k > 0, the graphs of tree-width < k are well-quasi-_
_ordered by the minor relation._

3 Indeed the ‘−1’ in the definition of width serves no other purpose than to make


-----

In order to make use of Theorem 12.3.7 for a proof of the general
minor theorem, we should be able to say something about the graphs it
does not cover, i.e. to deduce some information about a graph from the
assumption that its tree-width is large. Our next theorem achieves just
that: it identifies a canonical obstruction to small tree-width, a structural phenomenon that occurs in a graph if and only if its tree-width is
large.
_touch_ Let us say that two subsets of V (G) touch if they have a vertex in
common or G contains an edge between them. A set of mutually touching
_bramble_ connected vertex sets in G is a bramble. Extending our terminology of
_cover_ Chapter 2.1, we say that a subset of V (G) covers (or is a cover of) a
bramble if it meets every element of . The least number of vertices
_B_ _B_
_order_ covering a bramble is the order of that bramble.
The following simple observation will be useful:

**Lemma 12.3.8. Any set of vertices separating two covers of a bramble**
_also covers that bramble._

_Proof . Since each set in the bramble is connected and meets both of the_
covers, it also meets any set separating these covers.       
A typical example of a bramble is the set of crosses in a grid. The
_grid_ _k_ _k grid is the graph on_ 1, . . ., k with the edge set
_×_ _{_ _}[2]_

(i, j)(i[′], j[′]) : _i_ _i[′]_ + _j_ _j[′]_ = 1 _._
_{_ _|_ _−_ _|_ _|_ _−_ _|_ _}_

The crosses of this grid are the k[2] sets

_Cij := { (i, ℓ) | ℓ_ = 1, . . ., k } ∪{ (ℓ, j) | ℓ = 1, . . ., k } .

Thus, the cross Cij is the union of the grid’s ith column and its jth row.
Clearly, the crosses of the k _k grid form a bramble of order k: they_
_×_
are covered by any row or column, while any set of fewer than k vertices
misses both a row and a column, and hence a cross.
The following result is sometimes called the tree-width duality theo_rem:_

**Theorem 12.3.9. (Seymour & Thomas 1993)**
_Let k ⩾_ 0 be an integer. A graph has tree-width ⩾ _k if and only if it_
_contains a bramble of order > k._

(3.3.1) _Proof . For the backward implication, let_ be any bramble in a graph G.
_B_
We show that every tree-decomposition (T, (Vt)t∈T ) of G has a part that
meets every set in .
_B_
As in the proof of Lemma 12.3.4 we start by orienting the edges t1t2


-----

for each B disjoint from X there is an i _[∈]_ _{ 1, 2 } such that B ⊆_ _Ui ∖_ _X_
(defined as in Lemma 12.3.1); recall that B is connected. Moreover, this
_i is the same for all such B, because they touch. We now orient the edge_
_t1t2 towards ti._
If every edge of T is oriented in this way and t is the last vertex of
a maximal directed path in T, then Vt meets every set in B—just as in
the proof of Lemma 12.3.4.
To prove the forward direction, we now assume that G contains no
bramble of order > k. We show that for every bramble in G there is
_B_
a _-admissible tree-decomposition of G, one in which any part of order_ _B-_
_B_ _admissible_

_> k fails to cover_ . For = this implies that tw(G) < k, because
_B_ _B_ _∅_
every set covers the empty bramble.
Let B be given, and assume inductively that for every bramble B[′] _B_
with more sets than there is a -admissible tree-decomposition of G.
_B_ _B[′]_
(The induction starts, since no bramble in G has more than 2[|][G][|] sets.)
Let X _V (G) be a cover of_ with as few vertices as possible; then _X_
_⊆_ _B_
_ℓ_ := |X| ⩽ _k is the order of B. Our aim is to show the following:_ _ℓ_

_For every component C of G_ _X there exists a_ _-admissible_
_−_ _B_ ( )
_tree-decomposition of G [ X_ _V (C) ] with X as a part._ _∗_
_∪_

Then these tree-decompositions can be combined to a -admissible tree_B_
decomposition of G by identifying their nodes corresponding to X. (If
_X = V (G), then the tree-decomposition with X as its only part is_ _B_
admissible.)
So let C be a fixed component of G _X, write H := G [ X_ _V (C) ],_ _C, H_
_−_ _∪_
and put B[′] := B ∪{ C }. If B[′] is not a bramble then C fails to touch _B[′]_
some element of, and hence Y := V (C) _N_ (C) does not cover .
_B_ _∪_ _B_
Then the tree-decomposition of H consisting of the two parts X and Y
satisfies ( ).
_∗_
So we may assume that is a bramble. Since X covers but
_B[′]_ _B_
not, we have _>_ . Our induction hypothesis therefore ensures
_B[′]_ _|B[′]|_ _|B|_
that G has a B[′]-admissible tree-decomposition (T, (Vt)t∈T ). If this de- _T, (Vt)t∈T_
composition is also -admissible, there is nothing more to show. If not,
_B_
then one of its parts of order > k, Vs say, covers B. Since no set of fewer _s_
than ℓ vertices covers, Lemma 12.3.8 implies with Menger’s theorem
_B_
(3.3.1) that Vs and X are linked by ℓ disjoint paths P1, . . ., Pℓ. As Vs _Pi_
fails to cover B[′] and hence lies in G − _C, the paths Pi meet H only in_
their ends xi ∈ _X._ _xi_
For each i = 1, . . ., ℓ pick a ti ∈ _T with xi ∈_ _Vti, and let_ _ti_

_Wt := (Vt ∩_ (X ∪ _V (C))) ∪{ xi | t ∈_ _sTti } ;_

for all t ∈ _T (Fig. 12.3.3). Then (T, (Wt)t∈T ) is the tree-decomposition_


-----

_Vs_

_Fig. 12.3.3. Wt contains x2 and x3 but not x1; Wt′ contains no xi_

_xi have been added to some of the parts. Despite these additions, we_
still have |Wt| ⩽ _|Vt| for all t: for each xi ∈_ _Wt ∖_ _Vt we have t ∈_ _sTti,_
so Vt contains some other vertex of Pi (Lemma 12.3.1); that vertex does
not lie in Wt, because Pi meets H only in xi. Moreover, (T, (Wt)t∈T )
clearly satisfies (T3), because each xi is added to every part along some
path in T, so it is again a tree-decomposition.
As Ws = X, all that is left to show for (∗) is that this decomposition
is B-admissible. Consider any Wt of order > k. Then Wt meets C,
because |X| = ℓ ⩽ _k. Since (T, (Vt)t∈T ) is B[′]-admissible and |Vt| ⩾_
_|Wt| > k, we know that Vt fails to meet some B ∈_ _B; let us show that Wt_
does not meet this B either. If it does, it must do so in some xi ∈ _Wt ∖_ _Vt._
Then B is a connected set meeting both Vs and Vti but not Vt. As t ∈ _sTti_
by definition of Wt, this contradicts Lemma 12.3.1. 
Often, Theorem 12.3.9 is stated in terms of the bramble number of a
graph, the largest order of any bramble in it. The theorem then says that
the tree-width of a graph is exactly one less than its bramble number
(Exercise 15).
How useful even the easy backward direction of Theorem 12.3.9 can
be is exemplified once more by our example of the crosses bramble in the
_k_ _k grid: this bramble has order k, so by the theorem the k_ _k grid_
_×_ _×_
has tree-width at least k 1. (Try to show this without the theorem!)
_−_
In fact, the k _k grid has tree-width k (Exercise 16). But more_
_×_
important than its precise value is the fact that the tree-width of grids
tends to infinity with their size. For as we shall see, large grid minors
pose another canonical obstruction to small tree-width: not only do
large grids (and hence all graphs containing large grids as minors; cf.
Proposition 12.3.6) have large tree-width, but conversely every graph of
large tree-width has a large grid minor (Theorem 12.4.4).
Yet another canonical obstruction to small tree-width is described


-----

Given any two vertices t1, t2 ∈ _T_, Lemma 12.3.1 implies that every
_Vt with t_ _[∈]_ _t1Tt2 separates Vt1 from Vt2 in G._ Let us call our treedecomposition (T, ) of G linked, or lean,[4] if it satisfies the following _linked/lean_
_V_
condition:

(T4) given any s ∈ N and t1, t2 ∈ _T_, either G contains s disjoint Vt1–Vt2
paths or there exists a t _[∈]_ _t1Tt2 such that |Vt| < s._

The ‘branches’ in a lean tree-decomposition are thus stripped of any bulk
not necessary to maintain their connecting qualities: if a branch is thick
(the parts along a path in T large), then G is highly connected along
this branch.
In our quest for tree-decompositions into ‘small’ parts, we now have
two criteria to choose between: the global ‘worst case’ criterion of width,
which ensures that T is nontrivial (unless G is complete) but says nothing
about the tree-likeness of G among parts other than the largest, and
the more subtle local criterion of leanness, which ensures tree-likeness
everywhere along T but might be difficult to achieve except with trivial
or near-trivial T . Surprisingly, though, it is always possible to find a
tree-decomposition that is optimal with respect to both criteria at once:

**Theorem 12.3.10. (Thomas 1990)**
_Every graph G has a lean tree-decomposition of width tw(G)._

The proof of Theorem 12.3.10 is not too long but technical, and we shall
not present it. The fact that this theorem gives us a very useful property
of minimum-width tree-decompositions ‘for free’ has made it a valuable
tool wherever tree-decompositions are applied.

The tree-decomposition (T, ) of G is called simplicial if all the _simplicial_
_V_
separators Vt1 _Vt2 induce complete subgraphs in G. This assumption_
_∩_
can enable us to lift assertions about the parts of the decomposition to
_G itself. For example, if all the parts in a simplicial tree-decomposition_
of G are k-colourable, then so is G (proof?). The same applies to the
property of not containing a K _[r]_ minor for some fixed r. Algorithmically,
it is easy to obtain a simplicial tree-decomposition of a given graph into
irreducible parts. Indeed, all we have to do is split the graph recursively
along complete separators; if these are always chosen minimal, then the
set of parts obtained will even be unique (Exercise 22).
Conversely, if G can be constructed recursively from a set of
_H_
graphs by pasting along complete subgraphs, then G has a simplicial
tree-decomposition into elements of . For example, by Wagner’s The_H_
orem 8.3.4, any graph without a K [5] minor has a supergraph with a
simplicial tree-decomposition into plane triangulations and copies of the


-----

Wagner graph W, and similarly for graphs without K [4] minors (see Proposition 12.4.2).
Tree-decompositions may thus lead to intuitive structural characterizations of graph properties. A particularly simple example is the
following characterization of chordal graphs:

[ 12.4.2 ] **Proposition 12.3.11. G is chordal if and only if G has a tree-decompo-**
_sition into complete parts._

(5.5.1) _Proof . We apply induction on_ _G_ . We first assume that G has a tree_|_ _|_
decomposition (T, V) such that G [ Vt ] is complete for every t _[∈]_ _T_ ; let
us choose (T, V) with |T _| minimal. If |T_ _| ⩽_ 1, then G is complete and
hence chordal. So let t1t2 ∈ _T be an edge, and for i = 1, 2 define Ti_
and Gi := G [ Ui ] as in Lemma 12.3.1. Then G = G1 _G2 by (T1)_
_∪_
and (T2), and V (G1 ∩ _G2) = Vt1 ∩_ _Vt2 by the lemma; thus, G1 ∩_ _G2 is_
complete. Since (Ti, (Vt)t∈Ti) is a tree-decomposition of Gi into complete
parts, both Gi are chordal by the induction hypothesis. (By the choice
of (T, V), neither Gi is a subgraph of G [ Vt1 ∩ _Vt2 ] = G1 ∩_ _G2, so both_
_Gi are indeed smaller than G.) Since G1_ _G2 is complete, any induced_
_∩_
cycle in G lies in G1 or in G2 and hence has a chord, so G too is chordal.
Conversely, assume that G is chordal. If G is complete, there is
nothing to show. If not then, by Proposition 5.5.1, G is the union of
smaller chordal graphs G1, G2 with G1 _G2 complete. By the induction_
_∩_
hypothesis, G1 and G2 have tree-decompositions (T1, V1) and (T2, V2)
into complete parts. By Lemma 12.3.5, G1 _G2 lies inside one of those_
_∩_
parts in each case, say with indices t1 ∈ _T1 and t2 ∈_ _T2. As one easily_
checks, ((T1 ∪ _T2) + t1t2, V1 ∪V2) is a tree-decomposition of G into com-_
plete parts.       
**Corollary 12.3.12. tw(G) = min** �ω(H) 1 _G_ _H; H chordal�._
_−_ _|_ _⊆_

_Proof . By Lemma 12.3.5 and Proposition 12.3.11, each of the graphs H_
considered for the minimum has a tree-decomposition of width ω(H) 1.
_−_
Every such tree-decomposition induced one of G by Lemma 12.3.2, so
tw(G) ⩽ _ω(H) −_ 1 for every H.
Conversely, let us construct an H as above with ω(H) _−_ 1 ⩽ tw(G).
Let (T, V) be a tree-decomposition of G of width tw(G). For every t _[∈]_ _T_
let Kt denote the complete graph on Vt, and put H := [�]t[∈]T _[K][t][. Clearly,]_

(T, ) is also a tree-decomposition of H. By Proposition 12.3.11, H is
_V_
chordal, and by Lemma 12.3.5, ω(H) 1 is at most the width of (T, ),
_−_ _V_
i.e. at most tw(G).       

-----

###### 12.4 Tree-width and forbidden minors

If is any set or class of graphs, then the class
_H_

Forb≼(H) := { G | G ̸≽ _H for all H_ _[∈]_ _H }_ Forb≼(H)

of all graphs without a minor in is a graph property, i.e. is closed under
_H_
isomorphism.[5] When it is written as above, we say that this property
_forbidden_
is expressed by specifying the graphs H _[∈]_ _H as forbidden (or excluded_ ) _minors_
_minors._
By Proposition 1.7.3, Forb≼(H) is closed under taking minors: if (1.7.3)
_G[′]_ ≼ _G_ _[∈]_ Forb≼(H) then G[′ ∈] Forb≼(H). Graph properties that are
closed under taking minors will be called hereditary in this chapter. _hereditary_
Every hereditary property can in turn be expressed by forbidden minors:

**Proposition 12.4.1. A graph property** _can be expressed by forbidden_ [ 12.5.1 ]
_P_
_minors if and only if it is hereditary._

_Proof ._ For the ‘if’ part, note that P = Forb≼(P), where P is the _P_
complement of P. 
In Section 12.5, we shall return to the general question of how a given
hereditary property is best represented by forbidden minors. In this
section, we are interested in one particular type of hereditary property:
bounded tree-width.
Thus, let us consider the property of having tree-width less than
some given integer k. By Propositions 12.3.6 and 12.4.1, this property
can be expressed by forbidden minors. Choosing their set as small as
_H_
possible, we find that = _K_ [3] for k = 2: the graphs of tree-width
_H_ _{_ _}_
_< 2 are precisely the forests. For k = 3, we have_ = _K_ [4] :
_H_ _{_ _}_

**Proposition 12.4.2. A graph has tree-width < 3 if and only if it has**
_no K_ [4] _minor._

(8.3.1)
(12.3.2)

_Proof ._ By Lemma 12.3.5, we have tw(K [4]) ⩾ 3. By Proposition 12.3.6, (12.3.5)

therefore, a graph of tree-width < 3 cannot contain K [4] as a minor. (12.3.11)
Conversely, let G be a graph without a K [4] minor; we assume that
_|G| ⩾_ 3. Add edges to G until the graph G[′] obtained is edge-maximal
without a K [4] minor. By Proposition 8.3.1, G[′] can be constructed recursively from triangles by pasting along K [2]s. By induction on the
number of recursion steps and Lemma 12.3.5, every graph constructible
in this way has a tree-decomposition into triangles (as in the proof of
Proposition 12.3.11). Such a tree-decomposition of G[′] has width 2, and
by Lemma 12.3.2 it is also a tree-decomposition of G. 

-----

A question converse to the above is to ask for which H (other than
_K_ [3] and K [4]) the tree-width of the graphs in Forb≼(H) is bounded. Interestingly, it is not difficult to show that any such H must be planar.
(4.4.6) Indeed, as all grids and their minors are planar (why?), every class
Forb≼(H) with non-planar H contains all grids; yet as we saw after
Theorem 12.3.9, the grids have unbounded tree-width.
The following deep and surprising theorem says that, conversely, the
tree-width of the graphs in Forb≼(H) is bounded for every planar H:

**Theorem 12.4.3. (Robertson & Seymour 1986)**
_Given a graph H, the graphs without an H minor have bounded tree-_
_width if and only if H is planar._

The rest of this section is devoted to the proof of Theorem 12.4.3.

To prove Theorem 12.4.3 we have to show that forbidding any planar
graph H as a minor bounds the tree-width of a graph. In fact, we only
have to show this for the special cases when H is a grid, because every
planar graph is a minor of some grid. (To see this, take a drawing of the
graph, fatten its vertices and edges, and superimpose a sufficiently fine
plane grid.) It thus suffices to show the following:

**Theorem 12.4.4. (Robertson & Seymour 1986)**
_For every integer r there is an integer k such that every graph of tree-_
_width at least k has an r_ _r grid minor._
_×_

Our proof of Theorem 12.4.4, which is much shorter than the original
proof, proceeds as follows. Let r be given, and let G be any graph of
large enough tree-width (depending on r). We first show that G contains
a large family A = { A1, . . ., Am } of disjoint connected vertex sets such
that each pair Ai, Aj ∈ _A can be linked in G by a family Pij of many_
disjoint Ai–Aj paths avoiding all the other sets in A. We then consider
all the pairs (Pij, Pi[′]j[′] ) of these path families. If we can find a pair
among these such that many of the paths in Pij meet many of the paths
in Pi[′]j[′], we shall think of the paths in Pij as horizontal and the paths
in Pi[′]j[′] as vertical and extract a subdivision of an r × r grid from their
union. (This will be the difficult part of the proof, because these paths
will in general meet in a less orderly way than they do in a grid.) If
not, then for every pair (Pij, Pi[′]j[′] ) many of the paths in Pij avoid many
of the paths in Pi[′]j[′] . We can then select one path Pij ∈ _Pij from each_
family so that these selected paths are pairwise disjoint. Contracting
each of the connected sets A _[∈]_ _A will then give us a K_ _[m]_ minor in G,
which contains the desired r × r grid if m ⩾ _r[2]._
To implement these ideas formally, we need a few definitions. Let
_externally_
us call a set X _V (G) externally k-connected in G if_ _X_ _k and for_
_k connected_ _⊆_ _|_ _| ≥_


-----

_Y –Z paths in G that have no inner vertex or edge in G [ X ]. Note that_
the vertex set of a k-connected subgraph of G need not be externally
_k-connected in G. On the other hand, any horizontal path in the r_ _r_
_×_
grid is externally k-connected in that grid for every k ⩽ _r. (How?)_
One of the first things we shall prove below is that any graph of
large enough tree-width—not just grids—contains a large externally kconnected set of vertices (Lemma 12.4.5). Conversely, it is easy to show
that large externally k-connected sets (with k large) can exist only in
graphs of large tree-width (Exercise 30). So, like large grid minors, these
sets form a canonical obstruction to small tree-width: they can be found
in a graph if and only if its tree-width is large.
An ordered pair (A, B) of subgraphs of G will be called a premesh _premesh_
in G if G = A _B and A contains a tree T such that_
_∪_

(i) T has maximum degree 3;
_≤_

(ii) every vertex of A _B lies in T and has degree_ 2 in T ;
_∩_ _≤_

(iii) T has a leaf in A _B, or_ _T_ = 1 and T _A_ _B._
_∩_ _|_ _|_ _⊆_ _∩_

The order of such a premesh is the number _A_ _B_, and if V (A _B) is_ _order_
_|_ _∩_ _|_ _∩_
externally k-connected in B then this premesh is a k-mesh in G. _k-mesh_

**Lemma 12.4.5. Let G be a graph and let h** _k_ 1 be integers. If G
_≥_ _≥_
_contains no k-mesh of order h then G has tree-width < h + k_ 1.
_−_

_Proof . We may assume that G is connected. Let U_ _V (G) be max-_ _U_
_⊆_
imal such that G [ U ] has a tree-decomposition D of width < h + k − 1 _D_
with the additional property that, for every component C of G _U_, the
_−_
neighbours of C in U lie in one part of and (G _C,_ _C[˜]) is a premesh_
_D_ _−_
of order _h, where C[˜] := G [ V (C)_ _N_ (C) ]. Clearly, U = . _C˜_
_≤_ _∪_ _̸_ _∅_
We claim that U = V (G). Suppose not. Let C be a component of _C_
_G_ _U_, put X := N (C), and let T be a tree associated with the premesh _X_
_−_
(G _C,_ _C[˜])._ _T_
_−_
By assumption, _X_ _h; let us show that equality holds here. If_
_|_ _| ≤_
not, let u _[∈]_ _X be a leaf of T (respectively { u } := V (T_ )) as in (iii), and
let v _[∈]_ _C be a neighbour of u. Put U_ _[′]_ := U ∪{ v } and X _[′]_ := X ∪{ v },
let T _[′]_ be the tree obtained from T by joining v to u, and let D[′] be the
tree-decomposition of G [ U _[′]_ ] obtained from D by adding X _[′]_ as a new
part (joined to a part of containing X, which exists by our choice
_D_
of U ; see Fig. 12.4.1). Clearly still has width < h + k 1. Consider
_D[′]_ _−_
a component C _[′]_ of G − _U_ _[′]. If C_ _[′]_ _∩_ _C = ∅_ then C _[′]_ is also a component of
_G_ _−_ _U_, so N (C _[′]) lies inside a part of D (and hence of D[′]), and (G_ _−_ _C_ _[′],_ _C[˜][′])_
is a premesh of order ≤ _h by assumption. If C_ _[′]_ _∩_ _C ̸= ∅, then C_ _[′]_ _⊆_ _C_
and N (C _[′]) ⊆_ _X_ _[′]. Moreover, v_ _[∈]_ _N_ (C _[′]): otherwise N_ (C _[′]) ⊆_ _X would_
separate C _[′]_ from v, contradicting the fact that C _[′]_ and v lie in the same


-----

_Fig. 12.4.1. Extending U and D when |X| < h_

check that (G _C_ _[′],_ _C[˜][′]) is again a premesh of order_ _h, contrary to the_
_−_ _≤_
maximality of U .
Thus _X_ = h, so by assumption our premesh (G _C,_ _C[˜]) cannot_
_|_ _|_ _−_
_Y, Z_ be a k-mesh; let Y, Z _X be sets to witness this. Let_ be a set of
_⊆_ _P_
as many disjoint Y –Z paths in H := G [ V (C) _Y_ _Z ]_ _E(G [ Y_ _Z ])_
_∪_ _∪_ _−_ _∪_
as possible. Since all these paths are ‘external’ to X in C[˜], we have
_k[′]_ _k[′]_ := |P| < |Y | = |Z| ⩽ _k by the choice of Y and Z. By Menger’s_
_S_ theorem (3.3.1), Y and Z are separated in H by a set S of k[′] vertices.
Clearly, S has exactly one vertex on each path in ; we denote the path
_P_
_Ps_ containing the vertex s _[∈]_ _S by Ps (Fig. 12.4.2)._

_H_

_Ps_

_C_

_Y_

_T_ _[′]_

_v_ _s_

_S_

_T_

_Z_

_U_

_C_ _[′]_

_X_

_Fig. 12.4.2. S separates Y from Z in H_

Let X _[′]_ := X ∪ _S and U_ _[′]_ := U ∪ _S, and let D[′]_ be the treedecomposition of G [ U _[′]_ ] obtained from D by adding X _[′]_ as a new part.
Clearly, |X _[′]| ≤|X| + |S| ≤_ _h + k −_ 1. We show that U _[′]_ contradicts the
maximality of U .
Since Y _Z_ _N_ (C) and _S_ _<_ _Y_ = _Z_ we have S _C_ =, so
_∪_ _⊆_ _|_ _|_ _|_ _|_ _|_ _|_ _∩_ _̸_ _∅_
_U_ _[′]_ is larger than U . Let C _[′]_ be a component of G − _U_ _[′]. If C_ _[′]_ _∩_ _C = ∅,_
we argue as earlier. So C _[′]_ _⊆_ _C and N_ (C _[′]) ⊆_ _X_ _[′]. As before, C_ _[′]_ has at
_v_ least one neighbour v in S ∩ _C, since X cannot separate C_ _[′]_ _⊆_ _C from_


-----

and Z \ S; we assume it has none in Y \ S. Let T _[′]_ be the union of T
and all the Y –S subpaths of paths Ps with s _[∈]_ _N_ (C _[′]) ∩_ _C; since these_
subpaths start in Y \ S and have no inner vertices in X _[′], they cannot_
meet C _[′]. Therefore (G −_ _C_ _[′],_ _C[˜][′]) is a premesh with tree T_ _[′]_ and leaf v;
the degree conditions on T _[′]_ are easily checked. Its order is |N (C _[′])| ≤_
_|X| −|Y | + |S| = h −|Y | + k[′]_ _< h, a contradiction to the maximality_
of U . 
**Lemma 12.4.6. Let k** 2 be an integer. Let T be a tree of maximum
_≥_
_degree ⩽_ 3 and X ⊆ _V (T_ ). Then T has a set F of edges such that every
_component of T_ _F has between k and 2k_ 1 vertices in X, except that
_−_ _−_
_one such component may have fewer vertices in X._

_Proof . We apply induction on_ _X_ . If _X_ 2k 1 we put F = . So
_|_ _|_ _|_ _| ≤_ _−_ _∅_
assume that _X_ 2k. Let e be an edge of T such that some component
_|_ _| ≥_
_T_ _[′]_ of T − _e has at least k vertices in X and |T_ _[′]| is as small as possible._
As ∆(T ) ≤ 3, the end of e in T _[′]_ has degree at most two in T _[′], so_
the minimality of T _[′]_ implies that |X ∩ _V (T_ _[′])| ≤_ 2k − 1. Applying the
induction hypothesis to T − _T_ _[′]_ we complete the proof. 
**Lemma 12.4.7. Let G be a bipartite graph with bipartition (A, B),**
_A_ = a, _B_ = b, and let c _a and d_ _b be positive integers. Assume_
_|_ _|_ _|_ _|_ _≤_ _≤_
_that G has at most (a_ _c)(b_ _d)/d edges. Then there exist C_ _A and_
_−_ _−_ _⊆_
_D_ _B such that_ _C_ = c and _D_ = d and C _D is independent in G._
_⊆_ _|_ _|_ _|_ _|_ _∪_

_Proof . As_ _G_ (a _c)(b_ _d)/d, fewer than b_ _d vertices in B have_
_||_ _|| ≤_ _−_ _−_ _−_
more than (a _c)/d neighbours in A. Choose D_ _B so that_ _D_ = d and
_−_ _⊆_ _|_ _|_
each vertex in D has at most (a _c)/d neighbours in A. Then D sends_
_−_
a total of at most a _c edges to A, so A has a subset C of c vertices_
_−_
without a neighbour in D. 
Given a tree T, call an r-tuple (x1, . . ., xr) of distinct vertices of T
_good_
_good if, for every j = 1, . . ., r −_ 1, the xj–xj+1 path in T contains none _r-tuple_
of the other vertices in this r-tuple.

**Lemma 12.4.8. Every tree T of order at least r(r** 1) contains a good
_−_
_r-tuple of vertices._

_Proof . Pick a vertex x ∈_ _T_ . Then T is the union of its subpaths xTy,
where y ranges over its leaves. Hence unless one of these paths has at
least r vertices, T has at least |T _|/(r −_ 1) ⩾ _r leaves. Since any path of_
_r vertices and any set of r leaves gives rise to a good r-tuple in T_, this
proves the assertion. 
Our next lemma shows how to obtain a grid from two large systems


-----

**Lemma 12.4.9. Let d, r** 2 be integers such that d _r[2][r][+2]._ _Let_
_≥_ _≥_
_G be a graph containing a set_ _of r[2]_ 1 disjoint paths and a set
_H_ _−_
_V = { V1, . . ., Vd } of d disjoint paths. Assume that every path in V meets_
_every path in H, and that each path H_ _[∈]_ _H consists of d consecutive_
_(vertex-disjoint) segments such that Vi meets H only in its ith segment,_
_for every i = 1, . . ., d (Fig. 12.4.3). Then G has an r_ _r grid minor._
_×_

_H_

_. . ._

_H_ [1] _. . ._

_H_ [2] _. . ._

_H_

_H_ _[r]_ _. . ._

_. . ._

_V1_ _Vd_

_Fig. 12.4.3. Paths intersecting as in Lemma 12.4.9_

|Col1|Col2|Col3|Col4|H|Col6|Col7|Col8|Col9|Col10|Col11|
|---|---|---|---|---|---|---|---|---|---|---|
|||||H|||||||
|||||||. . .|||||
|||||||. . .|||||
|||||||. . .|||||
|||||||. .|||||
|||||||. . . .|||||
|||||||. . .|||||
||||||||||||
||||||||||||


_Proof . For each i = 1, . . ., d, consider the graph with vertex set_ in
_H_
which two paths are adjacent whenever Vi contains a subpath between
them that meets no other path in H. Since Vi meets every path in H, this
_Ti_ is a connected graph; let Ti be a spanning tree in it. Since |H| ≥ _r(r −_ 1),
Lemma 12.4.8 implies that each of these d ≥ _r[2](r[2])[r]_ trees Ti has a good
_r-tuple of vertices. Since there are no more than (r[2])[r]_ distinct r-tuples
_H_ [1], . . ., H _[r]_ on H, some r[2] of the trees Ti have a common good r-tuple (H [1], . . ., H _[r])._
_I, ik_ Let I = { i1, . . ., ir2 } be the index set of these trees (with ij < ik for
_H[′]_ _j < k) and put H[′]_ := { H [1], . . ., H _[r]_ _}._

Here is an informal description of how we construct our r _r grid._
_×_
Its ‘horizontal’ paths will be the paths H [1], . . ., H _[r]. Its ‘vertical’ paths_
will be pieced together edge by edge, as follows. The r 1 edges of the
_−_
first vertical path will come from the first r − 1 trees Ti, trees with their
index i among the first r elements of I. More precisely, its ‘edge’ between
_H_ _[j]_ and H _[j][+1]_ will be the sequence of subpaths of Vij (together with some
connecting horizontal bits taken from paths in ) induced by the
_H \ H[′]_
edges of an H _[j]–H_ _[j][+1]_ path in Tij that has no inner vertices in H[′]; see
Fig. 12.4.4. (This is why we need (H [1], . . ., H _[r]) to be a good r-tuple_
in every tree Ti.) Similarly, the jth edge of the second vertical path
will come from an H _[j]–H_ _[j][+1]_ path in Tir+j, and so on.[6] To merge these
individual edges into r vertical paths, we then contract in each horizontal

6 Although we need only r − 1 edges for each vertical path, we reserve r rather
than just r − 1 of the paths Vi for each vertical path to make the indexing more lucid.


-----

_H_ _[j]_ _H_ _[j][+1]_

_H_ _[′]_ _H_ _H_ _[′′]_

_P_

_H_ [1]

_H_ [3]
_H_ [2]

The H _[j]–H_ _[j][+1]_ path P in Tij


_H_ _[j]_


_H_

_H_ _[′]_

_H_ _[′′]_


_H_ _[j][+1]_

_H_ [1]

_H_ _[j]_


The H _[j]–H_ _[j][+1]_ path P _[′]_ in G


_Vij_

|Col1|Col2|Vi|Col4|Col5|Col6|Col7|Col8|Col9|
|---|---|---|---|---|---|---|---|---|
|||ij|||||||
|||i th segment j|||||||
|||P′|||||||
||||||||||
|||||P′|||||
|||P′|||||||
||||||||||
||||||||||
|||V i|||||||


_Vi1_ _Vij_ _Vir+1_ _Vi2r+1_


_P_

_H_ _[j][+1]_

_H_ _[r]_

� �� � � �� � � �� �
contract contract contract. . .

_P_ _[′]_ viewed as a (subdivided) H _[j]–H_ _[j][+1]_ edge

_Fig. 12.4.4. An H_ _[j]–H_ _[j][+1]_ path in Tij inducing segments of Vij
for the jth edge of the grid’s first vertical path

|Col1|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Col10|Col11|Col12|Col13|Col14|Col15|Col16|Col17|Col18|Col19|Col20|Col21|Col22|Col23|Col24|Col25|Col26|Col27|Col28|Col29|Col30|Col31|Col32|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|||||||||||||||||||||||||||||||||
|||||||||||||||||||||||||||||||||
|1|||||P′|||||||||||||||||||||||||||
|||||||||||||||||||||||||||||||||
|||||||||||||||||||||||||||||||||


-----

path the initial segment that meets the first r paths Vi with i _[∈]_ _I, then_
contract the segment that meets the following r paths Vi with i _[∈]_ _I, and_
so on.
Formally, we proceed as follows. Consider all j, k _[∈]_ _{ 1, . . ., r }. (We_
shall think of the index j as counting the horizontal paths, and of the
index k as counting the vertical paths of the grid to be constructed.) Let
_Hk[j]_ _Hk[j]_ [be the minimal subpath of][ H] _[j][ that contains the][ i][th segment of][ H]_ _[j]_
_Hˆ_ _[j]_ for all i with i(k−1)r < i ≤ _ikr (put i0 := 0). Let H[ˆ]_ _[j]_ be obtained from
_H_ _[j]_ by first deleting any vertices following its ir2th segment and then
_vk[j]_ contracting every subpath Hk[j] [to one vertex][ v]k[j] [. Thus, ˆ][H] _[j][ =][ v]1[j]_ _[. . . v]r[j][.]_
Given j ∈ _{ 1, . . ., r −_ 1 } and k ∈ _{ 1, . . ., r }, we have to define a_
path Vk[j] [that will form the subdivided ‘vertical edge’][ v]k[j] _[v]k[j][+1]. This path_
will consist of segments of the path Vi together with some otherwise
unused segments of paths from H \ H[′], for i := i(k−1)r+j; recall that,
by definition of H[ˆ] _[j]_ and H[ˆ] _[j][+1], this Vi does indeed meet H_ _[j]_ and H _[j][+1]_

precisely in vertices that were contracted into vk[j] [and][ v]k[j][+1], respectively.
_Vk[j]_ To define Vk[j][, consider an][ H] _[j][–][H]_ _[j][+1][ path][ P][ =][ H][1][ . . . H][t][ in][ T][i][ that has]_
no inner vertices in H[′]. (Thus, H1 = H _[j]_ and Ht = H _[j][+1].)_ Every
edge HsHs+1 of P corresponds to an Hs–Hs+1 subpath of Vi that has
no inner vertex on any path in . Together with (parts of) the ith
_H_
segments of H2, . . ., Ht−1, these subpaths of Vi form an H _[j]–H_ _[j][+1]_ path
_P_ _[′]_ in G that has no inner vertices on any of the paths H [1], . . ., H _[r]_ and
meets no path from H outside its ith segment. Replacing the ends of P _[′]_

on H _[j]_ and H _[j][+1]_ with vk[j] [and][ v]k[j][+1], respectively, we obtain our desired
path Vk[j] [forming the][ j][th (subdivided) edge of the][ k][th ‘vertical’ path of]
our grid. Since the paths P _[′]_ are disjoint for different i and different pairs
(j, k) give rise to different i, the paths Vk[j] [are disjoint except for possible]
common ends vk[j] [. Moreover, they have no inner vertices on any of the]
paths H [1], . . ., H _[r], because none of these H_ _[j]_ is an inner vertex of any of
the paths P ⊆ _Ti used in the construction of Vk[j][.]_      
**Proof of Theorem 12.4.4. We are now ready to prove the following**
quantitative version of our theorem (which clearly implies it):

_Let r, m > 0 be integers, and let G be a graph of tree-width_
_at least r[4][m][2][(][r][+2)]. Then G contains either the r_ _r grid_
_×_
_or K_ _[m]_ _as a minor._

Since K _[r][2]_ contains the r _r grid as a subgraph we may assume that_
_×_ _m_
_c, k_ 2 ≤ _m ≤_ _r[2]. Put c := r[4(][r][+2)], and let k := c[2][(]_ 2 [)]. Then c ⩾ 2[16] and
hence 2m + 3 _c[m], so G has tree-width at least_
_≤_

_c[m][2]_ = c[m]k ⩾ (2m + 3)k ⩾ (m + 1)(2k − 1) + k − 1,

(A, B) enough for Lemma 12.4.5 to ensure that G contains a k-mesh (A, B)
( )( ) _A_


-----

premesh (A, B); then X := V (A _B)_ _V (T_ ). By Lemma 12.4.6, T has _X_
_∩_ _⊆_
_X_ _/(2k_ 1) 1 = m disjoint subtrees each containing at least k vertices
_|_ _|_ _−_ _−_
of X; let A1, . . ., Am be the vertex sets of these trees. By definition of a _A1, . . ., Am_
_k-mesh, B contains for all 1 ≤_ _i < j ≤_ _m a set Pij of k disjoint Ai–Aj_ _Pij_
paths that have no inner vertices in A. These sets Pij will shrink a little
and be otherwise modified later in the proof, but they will always consist
of ‘many’ disjoint Ai–Aj paths.
One option in our proof will be to find single paths Pij _[∈]_ _Pij that_
are disjoint for different pairs ij and thus link up the sets Ai to form a
_K_ _[m]_ minor of G. If this fails, we shall instead exhibit two specific sets Pij
and Ppq such that many paths of Pij meet many paths of Ppq, forming
an r _r grid between them by Lemma 12.4.9._
_×_
Let us impose a linear ordering on the index pairs ij by fixing an
arbitrary bijection σ : { ij | 1 ≤ _i < j ≤_ _m } →{ 0, 1, . . .,_ �m2 � _−_ 1 }. For _σ_
_ℓ_ = 0, 1, . . . in turn, we shall consider the pair pq with σ(pq) = ℓ and
choose an Ap–Aq path Ppq that is disjoint from all previously selected
such paths, i.e. from the paths Pst with σ(st) < ℓ. At the same time, we
shall replace all the ‘later’ sets Pij—or what has become of them—by
smaller sets containing only paths that are disjoint from Ppq. Thus for
each pair ij, we shall define a sequence Pij = Pij[0] _[,][ P]ij[1]_ _[, . . .][ of smaller and]_
smaller sets of paths, which eventually collapses to Pij[ℓ] [=][ {][ P][ij][ }][ when][ ℓ]
has risen to ℓ = σ(ij).
More formally, let ℓ[∗] _≤_ �m2 � be the greatest integer such that, for _ℓ[∗]_
all 0 ≤ _ℓ< ℓ[∗]_ and all 1 ⩽ _i < j ⩽_ _m, there exist sets Pij[ℓ]_ [satisfying the]
following five conditions:

(i) Pij[ℓ] [is a non-empty set of disjoint][ A][i][–][A][j][ paths in][ B][ that meet][ A]
only in their endpoints.

Whenever a set Pij[ℓ] [is defined, we shall write][ H]ij[ℓ] [:=][ �] _[P]ij[ℓ]_ [for the union] _Hij[ℓ]_
of its paths.

(ii) If σ(ij) < ℓ then Pij[ℓ] [has exactly one element][ P][ij][, and][ P][ij][ does] _Pij_
not meet any path belonging to a set Pst[ℓ] [with][ ij][ ̸][=][ st][.]

(iii) If σ(ij) = ℓ, then |Pij[ℓ] _[|][ =][ k/c][2][ℓ][.]_

(iv) If σ(ij) > ℓ, then |Pij[ℓ] _[|][ =][ k/c][2][ℓ][+1][.]_

(v) If ℓ = σ(pq) < σ(ij), then for every e _[∈]_ _E(Hij[ℓ]_ [)] _[\]_ _[E][(][H]pq[ℓ]_ [) there are]
no k/c[2][ℓ][+1] disjoint Ai–Aj paths in the graph (Hpq[ℓ] _ij[)][ −]_ _[e][.]_

_[∪]_ _[H]_ _[ℓ]_

Note that, by (iv), the paths considered in (v) do exist in Hij[ℓ] [. The]
purpose of (v) is to force those paths to reuse edges from Hpq[ℓ] [when-]
ever possible, using new edges e /∈ _Hpq[ℓ]_ [only if necessary. Note further]
that since σ(ij) < �m2 � by definition of σ, conditions (iii) and (iv) give
_|Pij[ℓ]_ _[| ≥]_ _[c][2][ whenever][ σ][(][ij][)][ ≥]_ _[ℓ][.]_
Clearly if ℓ[∗] = �m2 � then by (i) and (ii) we have a (subdivided) K _[m]_


-----

Let us show that ℓ[∗] _> 0. Let pq := σ[−][1](0) and put Ppq[0]_ [:=][ P][pq][. To]
define Pij[0] [for][ σ][(][ij][)][ >][ 0 put][ H][ij][ :=][ �] _[P][ij][, let][ F][ ⊆]_ _[E][(][H][ij][)][ \][ E][(][H]pq[0]_ [)]
be maximal such that (Hpq[0] _[∪]_ _[H][ij][)][ −]_ _[F][ still contains][ k/c][ disjoint][ A][i][–][A][j]_
paths, and let Pij[0] [be such a set of paths. Since the vertices from][ A][p][ ∪] _[A][q]_
have degree 1 in Hpq[0] _[∪]_ _[H][ij]_ [unless they also lie in][ A][i] _[∪]_ _[A][j][, these paths]_
have no inner vertices in A. Our choices of Pij[0] [therefore satisfy (i)–(v)]
for ℓ = 0.
_ℓ_ Having shown that ℓ[∗] _> 0, let us now consider ℓ_ := ℓ[∗] _−_ 1. Thus,
conditions (i)–(v) are satisfied for ℓ but cannot be satisfied for ℓ + 1.
_pq_ Let pq := σ[−][1](ℓ). If Ppq[ℓ] [contains a path][ P][ that avoids a set][ Q][ij] [of]
some |Pij[ℓ] _[|][/c][ of the paths in][ P]ij[ℓ]_ [for all][ ij][ with][ σ][(][ij][)][ > ℓ][, then we can]
define Pij[ℓ][+1] for all ij as before (with a contradiction). Indeed, let st :=
_σ[−][1](ℓ_ + 1) and put Pst[ℓ][+1] := Qst. For σ(ij) > ℓ + 1 write Hij := [�] _Qij,_
let F ⊆ _E(Hij) \ E(Hst[ℓ][+1][) be maximal such that (][H]st[ℓ][+1]_ _∪_ _Hij) −_ _F still_
contains at least |Pij[ℓ] _[|][/c][2][ disjoint][ A][i][–][A][j][ paths, and let][ P]ij[ℓ][+1]_ be such a set
of paths. Setting Ppq[ℓ][+1] := { P } and Pij[ℓ][+1] := Pij[ℓ] [=][ {][ P]ij[ ℓ] _[}][ for][ σ][(][ij][)][ < ℓ]_
then gives us a family of sets Pij[ℓ][+1] that contradicts the maximality of ℓ[∗].
Thus for every path P ∈ _Ppq[ℓ]_ [there exists a pair][ ij][ with][ σ][(][ij][)][ > ℓ]
such that P avoids fewer than |Pij[ℓ] _[|][/c][ of the paths in][ P]ij[ℓ]_ [. For some]
_P_ _⌈|Ppq[ℓ]_ _[|][/]�m2_ �⌉ of these P that pair ij will be the same; let P denote the set
_ij_ of those P, and keep ij fixed from now on. Note that |P| ≥|Ppq[ℓ] _[|][/]�m2_ � =
_c |Pij[ℓ]_ _[|][/]�m2_ � by (iii) and (iv).
Let us use Lemma 12.4.7 to find sets V ⊆P ⊆Ppq[ℓ] [and][ H ⊆P]ij[ℓ]
such that

� _c_ �

_|V| ⩾_ [1]2 _[|P|]_ _≥_ _ij[|]_

_m[2][ |P]_ _[ℓ]_

= r[2]
_|H|_

and every path in meets every path in . We have to check that the
_V_ _H_
bipartite graph with vertex sets P and Pij[ℓ] [in which][ P][ ∈] _[P][ is adjacent]_
to Q _[∈]_ _Pij[ℓ]_ [whenever][ P][ ∩] _[Q][ =][ ∅]_ [does not have too many edges. Since]
every P _[∈]_ _P has fewer than |Pij[ℓ]_ _[|][/c][ neighbours (by definition of][ P][), this]_
graph indeed has at most

_|P||Pij[ℓ]_ _[|][/c][ ⩽]_ _[|P||P]ij[ℓ]_ _[|][/][6][r][2]_

⩽ _⌊|P|/2⌋|Pij[ℓ]_ _[|]�2r[2]_

⩽ _⌊|P|/2⌋�|Pij[ℓ]_ _[|][/r][2][ −]_ [1]�

= �|P| −⌈|P|/2⌉��|Pij[ℓ] _[| −]_ _[r][2][��]r[2]_


_V, H_ edges, as required. Hence, V and H exist as claimed.
Although all the (‘vertical’) paths in meet all the (‘horizontal’)
_V_
paths in, these paths do not necessarily intersect in such an orderly
_H_
way as required for Lemma 12.4.9. In order to divide the paths from


-----

appropriate segments, we shall first pick a path Q _[∈]_ _H to serve as a_
yardstick: we shall divide Q into segments each meeting lots of paths
from V, select a ‘non-crossing’ subset V1, . . ., Vd of these vertical paths,
one from each segment (which is the most delicate task; we shall need
condition (v) from the definition of the sets Pij[ℓ] [here), and finally divide]
the other horizontal paths into the ‘induced’ segments, accommodating
one Vn each.
So let us pick a path Q _[∈]_ _H, and put_ _Q_

_d :=_ _c/m_ = _r[2][r][+4]/m_ _r[2][r][+2]._ _d_
_⌊[√]_ _⌋_ _⌊_ _⌋≥_


Note that |V| ⩾ (c/m[2])|Pij[ℓ] _[|][ ⩾]_ _[d][2][|P]ij[ℓ]_ _[|][.]_
For n = 1, 2, . . ., d − 1 let en be the first edge of Q (on its way from _en_
_Ai to Aj) such that the initial component Qn of Q −_ _en meets at least_ _Qn_
_nd |Pij[ℓ]_ _[|][ different paths from][ V][, and such that][ e][n][ is not an edge of][ H]pq[ℓ]_ [.]
As any two vertices of Q that lie on different paths from are separated
_V_
in Q by an edge not in Hpq[ℓ] [, each of these][ Q][n] [meets exactly][ nd][ |P]ij[ℓ] _[|]_
paths from V. Put Q0 := ∅ and Qd := Q. Since |V| ≥ _d[2]|Pij[ℓ]_ _[|][, we have]_
thus divided Q into d consecutive disjoint segments Q[′]n [:=][ Q][n] _[−]_ _[Q][n][−][1]_
(n = 1, . . ., d) each meeting at least d |Pij[ℓ] _[|][ paths from][ V][.]_ _Q[′]1[, . . ., Q][′]d_
For each n = 1, . . ., d 1, Menger’s theorem (3.3.1) and conditions
_−_
(iv) and (v) imply that Hpq[ℓ] _ij_ [has a set][ S][n][ of][ |P]ij[ℓ] _[| −]_ [1 vertices such] _Sn_

_[∪]_ _[H]_ _[ℓ]_
that (Hpq[ℓ] _ij[)]_ _[−]_ _[e][n][ −]_ _[S][n][ contains no path from][ A][i][ to][ A][j][. Let][ S][ denote]_ _S_

_[∪]_ _[H]_ _[ℓ]_
the union of all these sets Sn. Then |S| < d |Pij[ℓ] _[|][, so each][ Q]n[′]_ [meets at]
least one path Vn ∈ _V that avoids S (Fig. 12.4.5)._ _Vn_

_Q_
_Q[′]1_ _e1_ _. . ._ _en−1_ _Q[′]n_ _en_ _. . ._ _e_ _d_ _−1_ _Q[′]d_


_H_


_r[2]_ _−_ 1


_Sn−1_ _Sn_

_Ai_ _Vn_ _Aj_

_Fig. 12.4.5. Vn meets every horizontal path but avoids S_

Clearly, each Sn consists of a choice of exactly one vertex x from
every path P _[∈]_ _Pij[ℓ]_ _[\{][ Q][ }][. Denote the initial component of][ P][ −]_ _[x][ by][ P][n][,]_
put P0 := ∅ and Pd := P, and let Pn[′] [:=][ P][n] _[−]_ _[P][n][−][1]_ [for][ n][ = 1][, . . ., d][.] _P1[′][, . . ., P][ ′]d_


-----

_n = 1, . . ., d (and hence in particular that Pn[′]_ _[̸][=][ ∅][, ie. that][ P][n][−][1]_ _[⊂]_ _[P][n][).]_
Indeed Vn cannot meet Pn−1, because Pn−1 ∪ _Vn ∪_ (Q − _Qn−1) would_
then contain an Ai–Aj path in (Hpq[ℓ] _ij[)][ −]_ _[e][n][−][1][ −]_ _[S][n][−][1][, and likewise]_

_[∪]_ _[H]_ _[ℓ]_
(consider Sn) Vn cannot meet P − _Pn. Thus for all n = 1, . . ., d, the_
path Vn meets every path P _[∈]_ _H \ { Q } precisely in its nth segment Pn[′]_ [.]
Applying Lemma 12.4.9 to the path systems H \ { Q } and { V1, . . ., Vd }
now yields the desired grid minor. 
###### 12.5 The graph minor theorem

Hereditary graph properties, those that are closed under taking minors,
occur frequently in graph theory. Among the most natural examples
are the properties of being embeddable in some fixed surface, such as
planarity.
By Kuratowski’s theorem, planarity can be expressed by forbidding
the minors K [5] and K3,3. This is a good characterization of planarity in
the following sense. Suppose we wish to persuade someone that a certain
graph is planar: this is easy (at least intuitively) if we can produce a
drawing of the graph. But how do we persuade someone that a graph
is non-planar? By Kuratowski’s theorem, there is also an easy way to
do that: we just have to exhibit an MK [5] or MK3,3 in our graph, as
an easily checked ‘certificate’ for non-planarity. Our simple Proposition
12.4.2 is another example of a good characterization: if a graph has tree
width < 3, we can prove this by exhibiting a suitable tree-decomposition;
if not, we can produce an MK [4] as evidence.
Theorems that characterize a hereditary property by a set
_P_ _H_
of forbidden minors are doubtless among the most attractive results in
graph theory. As we saw in the proof of Proposition 12.4.1, there is
always some such characterization: that where is the complement
_H_ _P_
of . However, one naturally seeks to make as small as possible. And
_P_ _H_
as it turns out, there is indeed a unique smallest such set : the set
_H_

_HP := { H | H is ≼-minimal in P }_

satisfies P = Forb≼(H) and is contained in every other such set H.

**Proposition 12.5.1. P = Forb≼(HP** ), and HP ⊆H for every set H
_with P = Forb≼(H)._ 
Clearly, the elements of HP are incomparable under the minor relation ≼. Now the graph minor theorem of Robertson & Seymour says


-----

**Theorem 12.5.2. (Graph Minor Theorem; Robertson & Seymour)**
_The finite graphs are well-quasi-ordered by the minor relation ≼._

So every HP is finite, i.e. every hereditary graph property can be
represented by finitely many forbidden minors:

**Corollary 12.5.3. Every graph property that is closed under taking**
_minors can be expressed as Forb≼(H) with finite H._ 
As a special case of Corollary 12.5.3 we have, at least in principle,
a Kuratowski-type theorem for every surface:

**Corollary 12.5.4. For every surface S there exists a finite set of graphs**
_H1, . . ., Hn such that Forb≼(H1, . . ., Hn) contains precisely the graphs_
_not embeddable in S._

The minimal set of forbidden minors has been determined explicitly
for only one surface other than the sphere: for the projective plane it
is known to consist of 35 forbidden minors. It is not difficult to show
that the number of forbidden minors grows rapidly with the genus of the
surface (Exercise 34).

The complete proof of the graph minor theorem would fill a book
or two. For all its complexity in detail, however, its basic idea is easy to
grasp. We have to show that every infinite sequence

_G0, G1, G2, . . ._

of finite graphs contains a good pair: two graphs Gi ≼ _Gj with i < j._
We may assume that G0 ≼ _Gi for all i ⩾_ 1, since G0 forms a good pair
_̸_
with any graph Gi of which it is a minor. Thus all the graphs G1, G2, . . .
lie in Forb≼(G0), and we may use the structure common to these graphs
in our search for a good pair.
We have already seen how this works when G0 is planar: then the
graphs in Forb≼(G0) have bounded tree-width (Theorem 12.4.3) and are
therefore well-quasi-ordered by Theorem 12.3.7. In general, we need only
consider the cases of G0 = K _[n]: since G0 ≼_ _K_ _[n]_ for n := |G0|, we may
assume that K _[n]_ ⋠ _Gi for all i ⩾_ 1.
The proof now follows the same lines as above: again the graphs in
Forb≼(K _[n]) can be characterized by their tree-decompositions, and again_
their tree structure helps, as in Kruskal’s theorem, with the proof that
they are well-quasi-ordered. The parts in these tree-decompositions are
no longer restricted in terms of order now, but they are constrained in
more subtle structural terms. Roughly speaking, for every n there exists
a finite set of closed surfaces such that every graph without a K _[n]_ minor
_S_


-----

one of the surfaces S _[∈]_ _S. (The ‘nearly’ hides a measure of disorderliness_
that depends on n but not on the graph to be embedded.) By a generalization of Theorem 12.3.7—and hence of Kruskal’s theorem—it now
suffices, essentially, to prove that the set of all the parts in these treedecompositions is well-quasi-ordered: then the graphs decomposing into
these parts are well-quasi-ordered, too. Since is finite, every infinite
_S_
sequence of such parts has an infinite subsequence whose members are
all (nearly) embeddable in the same surface S _[∈]_ _S. Thus all we have to_
show is that, given any closed surface S, all the graphs embeddable in
_S are well-quasi-ordered by the minor relation._
This is shown by induction on the genus of S (more precisely,
on 2 _χ(S), where χ(S) denotes the Euler characteristic of S) using_
_−_
the same approach as before: if H0, H1, H2, . . . is an infinite sequence
of graphs embeddable in S, we may assume that none of the graphs
_H1, H2, . . . contains H0 as a minor. If S = S[2]_ we are back in the case
that H0 is planar, so the induction starts. For the induction step we
now assume that S ̸= S[2]. Again, the exclusion of H0 as a minor constrains the structure of the graphs H1, H2, . . ., this time topologically:
each Hi with i ⩾ 1 has an embedding in S which meets some noncontractible closed curve Ci ⊆ _S in no more than a bounded number_
of vertices (and no edges), say in Xi ⊆ _V (Hi). (The bound on |Xi|_
depends on H0, but not on Hi.) Cutting along Ci, and sewing a disc on
to each of the one or two closed boundary curves arising from the cut,
we obtain one or two new closed surfaces of larger Euler characteristic.
If the cut produces only one new surface Si, then our embedding of
_Hi_ _Xi still counts as a near-embedding of Hi in Si (since Xi is small)._
_−_
If this happens for infinitely many i, then infinitely many of the surfaces Si are also the same, and the induction hypothesis gives us a good
pair among the corresponding graphs Hi. On the other hand, if we get
two surfaces Si[′] [and][ S]i[′′] [for infinitely many][ i][ (without loss of generality]
the same two surfaces), then Hi decomposes accordingly into subgraphs
_Hi[′]_ [and][ H]i[′′] [embedded in these surfaces, with][ V][ (][H]i[′] _i_ [) =][ X][i][. The]

_[∩]_ _[H]_ _[′′]_
set of all these subgraphs taken together is again well-quasi-ordered by
the induction hypothesis, and hence so are the pairs (Hi[′][, H]i[′′][) by Lem-]
ma 12.1.3. Using a sharpening of the lemma that takes into account
not only the graphs Hi[′] [and][ H]i[′′] [themselves but also how][ X][i][ lies in-]
side them, we finally obtain indices i, j not only with Hi[′] [≼] _[H]j[′]_ [and]
_Hi[′′]_ [≼] _[H]j[′′][, but also such that these minor embeddings extend to the de-]_
sired minor embedding of Hi in Hj—completing the proof of the minor
theorem.

In addition to its impact on ‘pure’ graph theory, the graph minor
theorem has had far-reaching algorithmic consequences. Using their tree
structure theorem for the graphs in Forb≼(K _[n]), Robertson & Seymour_


-----

there is a polynomial-time algorithm[7] that decides whether or not the
input graph contains H as a minor. By the minor theorem, then, every
hereditary graph property can be decided in polynomial (even cubic)
_P_
time: if H1, . . ., Hk are the corresponding minimal forbidden minors,
then testing a graph G for membership in reduces to testing the k
_P_
assertions Hi ≼ _G!_
The following example gives an indication of how deeply this algorithmic corollary affects the complexity theory of graph algorithms. Let
us call a graph knotless if it can be embedded in R[3] so that none of its
cycles forms a non-trivial knot. Before the graph minor theorem, it was
an open problem whether knotlessness is decidable, that is, whether any
algorithm exists (no matter how slow) that decides for any given graph
whether or not that graph is knotless. To this day, no such algorithm
is known. The property of knotlessness, however, is easily ‘seen’ to be
hereditary: contracting an edge of a graph embedded in 3-space will not
create a knot where none had been before. Hence, by the minor theorem,
there exists an algorithm that decides knotlessness—even in polynomial
(cubic) time!
However spectacular such unexpected solutions to long-standing
problems may be, viewing the graph minor theorem merely in terms
of its corollaries will not do it justice. At least as important are the
techniques developed for its proof, the various ways in which minors are
handled or constructed. Most of these have not even been touched upon
here, yet they seem set to influence the development of graph theory for
many years to come.

###### Exercises

1.[−] Let ⩽ be a quasi-ordering on a set X. Call two elements x, y _∈_ _X_
_equivalent if both x ⩽_ _y and y ⩽_ _x._ Show that this is indeed an
equivalence relation on X, and that ⩽ induces a partial ordering on the
set of equivalence classes.

2. Let (A, ⩽) be a quasi-ordering. For subsets X ⊆ _A write_

Forb⩽(X) := { a _[∈]_ _A | a ̸⩾_ _x for all x_ _[∈]_ _X } ._

Show that ⩽ is a well-quasi-ordering on A if and only if every subset
_B ⊆_ _A that is closed under ⩾_ (i.e. such that x ⩽ _y_ _[∈]_ _B ⇒_ _x_ _[∈]_ _B) can_
be written as B = Forb⩽(X) with finite X.

3. Prove Proposition 12.1.1 and Corollary 12.1.2 directly, without using
Ramsey’s theorem.

7 indeed a cubic one—although with a typically enormous constant depending


-----

4. Given a quasi-ordering (X, ⩽) and subsets A, B ⊆ _X, write A ⩽[′]_ _B if_
there exists an order preserving injection f : A → _B with a ⩽_ _f_ (a) for
all a _[∈]_ _A. Does Lemma 12.1.3 still hold if the quasi-ordering considered_
for [X][<ω] is ⩽[′]?

5.[−] Show that the relation ⩽ between rooted trees defined in the text is
indeed a quasi-ordering.

6. Show that the finite trees are not well-quasi-ordered by the subgraph
relation.

7. The last step of the proof of Kruskal’s theorem considers a ‘topological’
embedding of Tm in Tn that maps the root of Tm to the root of Tn.
Suppose we assume inductively that the trees of Am are embedded in
the trees of An in the same way, with roots mapped to roots. We thus
seem to obtain a proof that the finite rooted trees are well-quasi-ordered
by the subgraph relation, even with roots mapped to roots. Where is
the error?

8.[+] Show that the finite graphs are not well-quasi-ordered by the topological
minor relation.

9.[+] Given k _[∈]_ N, is the class { G | G ̸⊇ _P_ _[k]_ _} well-quasi-ordered by the_
subgraph relation?

10. Show that a graph has tree-width at most 1 if and only if it is a forest.

11. Let G be a graph, T a set, and (Vt)t∈T a family of subsets of V (G) satisfying (T1) and (T2) from the definition of a tree-decomposition. Show
that there exists a tree on T that makes (T3) true if and only if there
exists an enumeration t1, . . ., tn of T such that for every k = 2, . . ., n
there is a j < k satisfying Vtk ∩ [�]i<k _[V][t][i][ ⊆]_ _[V][t][j]_ [.]

(The new condition tends to be more convenient to check than (T3).
It can help, for example, with the construction of a tree-decomposition
into a given set of parts.)

12. Prove the following converse of Lemma 12.3.1: if (T, V) satisfies condition (T1) and the statement of the lemma, then (T, V) is a treedecomposition of G.

13. Can the tree-width of a subdivision of a graph G be smaller than tw(G)?
Can it be larger?

14. Let (T, (Vt)t∈T ) be a tree-decomposition of a graph G. For each vertex
_v_ _∈_ _G, set Tv := { t ∈_ _T | v_ _∈_ _Vt }._ Show that Tv is always connected in T . More generally, for which subsets U ⊆ _V (G) is the set_
_{ t_ _[∈]_ _T | Vt ∩_ _U ̸= ∅} always connected in T (i.e. for all tree-decompo-_
sitions)?

15.[−] Show that the tree-width of a graph is one less than its bramble number.

16. Apply Theorem 12.3.9 to show that the k × k grid has tree-width at


-----

17. Let B be a maximum-order bramble in a graph G. Show that every
minimum-width tree-decomposition of G has a unique part covering B.

18.[+] In the second half of the proof of Theorem 12.3.9, let H _[′]_ be the union
of H and the paths P1, . . ., Pℓ, let H _[′′]_ be the graph obtained from H _[′]_

by contracting each Pi, and let (T, (Wt[′′][)]t∈T [) be the tree-decomposi-]
tion induced on H _[′′]_ (as in Lemma 12.3.3) by the decomposition that
(T, (Vt)t∈T ) induces on H _[′]. Is this, after the obvious identification of_
_H_ _[′′]_ with H, the same decomposition as the one used in the proof, i.e.
is Wt[′′] [=][ W]t [for all][ t][ ∈] _[T]_ [?]

19. Show that any graph with a simplicial tree-decomposition into kcolourable parts is itself k-colourable.

20. Let H be a set of graphs, and let G be constructed recursively from
elements of H by pasting along complete subgraphs. Show that G has
a simplicial tree-decomposition into elements of H.

21. Given a tree-decomposition (T, (Vt)t∈T ) of G and t _[∈]_ _T_, let Ht denote
the graph obtained from G [ Vt ] by adding all the edges xy such that
_x, y_ _[∈]_ _Vt ∩_ _Vt′ for some neighbour t[′]_ of t in T ; the graphs Ht are called
the torsos of this tree-decomposition. Show that G has no K [5] minor
if and only if G has a tree-decomposition in which every torso is either
planar or a copy of the Wagner graph W (Fig. 8.3.1).

22.[+] Call a graph irreducible if it is not separated by any complete subgraph.
Every (finite) graph G can be decomposed into irreducible induced
subgraphs, as follows. If G has a separating complete subgraph S,
then decompose G into proper induced subgraphs G[′] and G[′′] with G =
_G[′]_ _∪_ _G[′′]_ and G[′] _∩_ _G[′′]_ = S. Then decompose G[′] and G[′′] in the same way,
and so on, until all the graphs obtained are irreducible. By Exercise 20,
_G has a simplicial tree-decomposition into these irreducible subgraphs._
Show that they are uniquely determined if the complete separators were
all chosen minimal.

23.[+] If F is a family of sets, then the graph G on F with XY _∈_ _E(G) ⇔_
_X ∩_ _Y ̸= ∅_ is called the intersection graph of F . Show that a graph
is chordal if and only if it is isomorphic to the intersection graph of a
family of (vertex sets of) subtrees of a tree.

24. A tree-decomposition of a graph is called a path-decomposition if its
decomposition tree is a path. Show that a graph has a path-decomposition into complete graphs if and only if it is isomorphic to an interval
graph. (Interval graphs are defined in Ex. 37, Ch. 5.)

25. (continued)

The path-width pw(G) of a graph G is the least width of a path-decomposition of G. Prove the following analogue of Corollary 12.3.12 for
path-width: every graph G satisfies pw(G) = min ω(H) − 1, where the
minimum is taken over all interval graphs H containing G.


-----

27. Let P be a hereditary graph property. Show that strengthening the
notion of a minor (for example, to that of topological minor) increases
the set of forbidden minors required to characterize P.

28. Deduce from the minor theorem that every hereditary property can be
expressed by forbidding finitely many topological minors. Is the same
true for every property that is closed under taking topological minors?

29. Show that every horizontal path in the k × k grid is externally kconnected in that grid.

30.[+] Show that the tree-width of a graph is large if and only if it contains
a large externally k-connected set of vertices, with k large. For example, show that graphs of tree-width < k contain no externally (k + 1)connected set of 3k vertices, and that graphs containing no externally
(k + 1)-connected set of 3k vertices have tree-width < 4k.

31.[+] (continued)

Find an N → N[2] function k �→ (h, ℓ) such that every graph with an
externally ℓ-connected set of h vertices contains a bramble of order at
least k. Deduce the weakening of Theorem 12.3.9 that, given k, every
graph of large enough tree-width contains a bramble of order at least k.

32. Without using the minor theorem, show that the chromatic number of
the graphs in any ≼-antichain is bounded.

33. Seymour’s self-minor conjecture asserts that ‘every countably infinite
graph is a proper minor of itself’. Make this assertion precise, and
deduce the minor theorem from it.

34. Given an orientable surface S of genus g, find a lower bound in terms
of g for the number of forbidden minors needed to characterize embeddability in S.

(Hint. The smallest genus of an orientable surface in which a given
graph can be embedded is called the (orientable) genus of that graph.
Use the theorem that the genus of a graph is equal to the sum of the
genera of its blocks.)

###### Notes

Kruskal’s theorem on the well-quasi-ordering of finite trees was first published
in J.A. Kruskal, Well-quasi ordering, the tree theorem, and V´aszonyi’s conjecture, Trans. Amer. Math. Soc. 95 (1960), 210–225. Our proof is due to NashWilliams, who introduced the versatile proof technique of choosing a ‘minimal
bad sequence’. This technique was also used in our proof of Higman’s Lemma
12.1.3.
Nash-Williams generalized Kruskal’s theorem to infinite graphs. This
extension is much more difficult than the finite case; it is one of the deepest
theorems in infinite graph theory. The general graph minor theorem becomes
false for arbitrary infinite graphs, as shown by R. Thomas, A counterexample


-----

(1988), 55–57. Whether or not the minor theorem extends to countable graphs
remains an open problem.
The notions of tree-decomposition and tree-width were first introduced
(under different names) by R. Halin, S-functions for graphs, J. Geometry 8
(1976), 171–186. Among other things, Halin showed that grids can have arbitrarily large tree-width. Robertson & Seymour reintroduced the two concepts, apparently unaware of Halin’s paper, with direct reference to K. Wagner,
¨Uber eine Eigenschaft der ebenen Komplexe, Math. Ann. 114 (1937), 570–
590. (This is the classic paper that introduced simplicial tree-decompositions to prove Theorem 8.3.4; cf. Exercise 21.) Simplicial tree-decompositions
are treated in depth in R. Diestel, Graph Decompositions, Oxford University
Press 1990.
Robertson & Seymour themselves usually refer to the graph minor theorem as Wagner’s conjecture. It seems that Wagner did indeed discuss this
problem in the 1960s with his then students Halin and Mader. However,
Wagner apparently never conjectured a positive solution; he certainly rejected
any credit for the ‘conjecture’ when it had been proved.
Robertson & Seymour’s proof of the graph minor theorem is given in
the numbers IV–VII, IX–XII and XIV–XX of their series of over 20 papers
under the common title of Graph Minors, which has been appearing in the
_Journal of Combinatorial Theory, Series B, since 1983. Of their theorems cited_
in this chapter, Theorem 12.3.7 is from Graph Minors IV, while Theorems
12.4.3 and 12.4.4 are from Graph Minors V. Our short proof of these latter
theorems is from R. Diestel, K.Yu. Gorbunov, T.R. Jensen & C. Thomassen,
Highly connected sets and the excluded grid theorem, J. Combin. Theory B
**75 (1999), 61–73.**
Theorem 12.3.9 is due to P.D. Seymour & R. Thomas, Graph searching
and a min-max theorem for tree-width, J. Combin. Theory B 58 (1993),
22–33. Our proof is a simplification of the original proof. B.A. Reed gives
an instructive introductory survey on tree-width and graph minors, including some algorithmic aspects, in (R.A. Bailey, ed) Surveys in Combinatorics
_1997_, Cambridge University Press 1997, 87–162. Reed also introduced the
term ‘bramble’; in Seymour & Thomas’s paper, brambles are called ‘screens’.
The obstructions to small tree-width actually used in the proof of the
graph minor theorem are not brambles but so-called tangles. Tangles are
more powerful than brambles and well worth studying. See Graph Minors X
or Reed’s survey for an introduction to tangles and their relation to brambles
and tree-decompositions.
Theorem 12.3.10 is due to R. Thomas, A Menger-like property of treewidth; the finite case, J. Combin. Theory B 48 (1990), 67–76.
As a forerunner to Theorem 12.4.3, Robertson & Seymour proved its
following analogue for path-width (Graph Minors I): excluding a graph H as
a minor bounds the path-width of a graph if and only if H is a forest. A short
proof of this result, with optimal bounds, can be found in the first edition of
this book, or in R. Diestel, Graph Minors I: a short proof of the path width
theorem, Combinatorics, Probability and Computing 4 (1995), 27–30.
The 35 minimal forbidden minors for graphs to be embedded in the projective plane were determined by D. Archdeacon, A Kuratowski theorem for


-----

the number of forbidden minors needed for an arbitrary closed surface is given
in P.D. Seymour, A bound on the excluded minors for a surface, J. Combin.
_Theory B (to appear). B. Mohar, Embedding graphs in an arbitrary surface in_
linear time, Proc. 28th Ann. ACM STOC (Philadelphia 1996), 392–397, has
developed a set of algorithms, one for each surface, that decide embeddability
in that surface in linear time. As a corollary, Mohar obtains an independent and constructive proof of the ‘generalized Kuratowski theorem’, Corollary
12.5.4. Another independent and short proof of this corollary, which builds on
Theorem 12.4.3 and Graph Minors IV but on no other papers of the Graph
Minors series, was found by C. Thomassen, A simpler proof of the excluded
minor theorem for higher surfaces, J. Combin. Theory B 70 (1997), 306–311.
A survey of the classical forbidden minor theorems is given in Chapter 6.1 of
R. Diestel, Graph Decompositions, Oxford University Press 1990. More recent
developments are surveyed in R. Thomas, Recent excluded minor theorems, in
(J.D. Lamb & D.A. Preece, eds) Surveys in Combinatorics 1999, Cambridge
University Press 1999, 201–222.
For every graph X, Graph Minors XIII gives an explicit algorithm that
decides in cubic time for every input graph G whether X ≼ _G. The constants_
in the cubic polynomials bounding the running time of these algorithms depend on X but are constructively bounded from above. For an overview of
the algorithmic implications of the Graph Minors series, see Johnson’s NPcompleteness column in J. Algorithms 8 (1987), 285–303.
The concept of a ‘good characterization’ of a graph property was first
suggested by J. Edmonds, Minimum partition of a matroid into independent
subsets, J. Research of the National Bureau of Standards (B) 69 (1965) 67–72.
In the language of complexity theory, a characterization is good if it specifies
two assertions about a graph such that, given any graph G, the first assertion
holds for G if and only if the second fails, and such that each assertion, if true
for G, provides a certificate for its truth. Thus every good characterization
has the corollary that the decision problem corresponding to the property it
characterizes lies in NP ∩ co-NP.


-----

### Hints for all the Exercises

**Caveat. These hints are intended to set on the right track anyone who**
has already spent some time over an exercise but somehow failed to make
much progress. They are not designed to be particularly intelligible
without such an initial attempt, and they will rarely spoil the fun by
giving away the key idea. They may, however, narrow ones mind by
focusing on what is just one of several possible ways to think about a
problem. . .

###### Hints for Chapter 1

1.[−] How many edges are there at each vertex?

2. Average degree and edges: consider the vertex degrees. Diameter: how
do you determine the distance between two vertices from the corresponding 0–1 sequences? Girth: does the graph have a cycle of length 3?
Circumference: partition the d-dimensional cube into cubes of lower
dimension and use induction.

3. Consider how the path intersects C. Where can you see cycles, and can
they all be short?

4.[−] Can you find graphs for which Proposition 1.3.2 holds with equality?

5. Estimate the distances within G as seen from a central vertex.

6.[+] Consider the cases d = 2 and d > 2 separately. For d > 2, give a sharper
bound on |Di| for i > 0 than the one used in the proof of Proposition
1.3.3.

7.[−] Assume the contrary, and derive a contradiction.


-----

9. (i) Straightforward from the definitions.

(ii) Prove κ ⩾ _n by induction on n: partition the n-dimensional cube_
into cubes of lower dimension, and show inductively that the deletion
of < n vertices leaves a connected subgraph.

10. For the first inequality, consider the endvertices of a set of λ(G) edges
whose deletion disconnects G. Use the definition of λ(G) to show the
second inequality.

11.[−] Try to find counterexamples for k = 1.

12. Rephrase (i) and (ii) as statements about the existence of two N → N
functions. To show the equivalence, express each of these functions in
terms of the other. Show that (iii) may hold even if (i) and (ii) do not,
and strengthen (iii) to remedy this.

13.[+] Try to imitate the proof assuming ε(G) ⩾ 2k instead of condition (ii).
Why does this fail, and why does condition (ii) remedy the problem?

14. Show (i) ⇒ (ii) ⇒ (iii) ⇒ (iv) ⇒ (i) from the definitions of the
relevant concepts.

15. Consider paths emanating from a vertex of maximum degree.

16. Theorem 1.5.1.

17. Induction.

18. The easiest solution is to apply induction on |T _|. What kind of vertex_
of T will be best to delete in the induction step?

19. Induction on |T _| is a possibility, but not the only one._

20. Count the edges.

21. Show that if a graph contains any odd cycle at all it also contains an
induced one.

22. Apply Proposition 1.2.2. Split the subgraph thus found into two sides
so that every vertex has many neighbours on the opposite side.

23. Try to carry the proof for finite graphs over to the infinite case. Where
does it fail?

24.[−] Use Proposition 1.9.2.

25. Why do all the cuts E(v) generate the cut space? Will they still do so
if we omit one of them? Or even two?

26. Start with the case that the graph considered is a cycle.

27. Induction on |F ∖ _E(T_ )| for given F _[∈]_ _C(G)._

28. Induction on |D ∩ _E(T_ )| for a given cut D.

29. Apply Theorem 1.9.6.


-----

###### Hints for Chapter 2

1. Compare the given matching with a matching of maximum cardinality.

2. Augmenting paths.

3. If you have S ⫋ _S[′]_ _⊆_ _A with |S| = |N_ (S)| in the finite case, the
marriage condition ensures that N (S) ⫋ _N_ (S[′]): increasing S makes
more neighbours available. Use the fact that this fails when S is infinite.

4. Apply the marriage theorem.

5. Construct a bipartite graph in which A is one side, and the other side
consists of a suitable number of copies of the sets Ai. Define the edge
set of the graph so that the desired result can be derived from the
marriage theorem.

6.[+] Construct chains in the power set lattice of X as follows. For each
_k < n/2, use the marriage theorem to find a 1–1 map ϕ from the set A_
of k-subsets to the set B of (k + 1)-subsets of X such that Y ⊆ _ϕ(Y )_
for all Y _∈_ _A._

7. Decide where the leaves should go: in factor-critical components or
in S?

8. Distinguish between the cases of |S| ≤ 1 and |S| ≥ 2.

9. The case S = ∅ is easy. In the other case, look for a vertex that meets
every maximum-cardinality matching. What are the consequences of
this for the other vertices?

10. For the ‘if’ direction consider the graph suggested in the hint: does it
have a 1-factor? If not, then consider the set of vertices supplied by
Tutte’s 1-factor theorem. For an alternative solution, apply the remarks
on maximum-cardinality matchings which follow Theorem 2.2.3.

11.[−] Corollary 2.2.2.

12. Let G be a bipartite graph that satisfies the marriage condition, with
bipartition (A, B) say. Reduce the problem to the case of |A| = |B|. To
verify the premise of Tutte’s theorem for a given set S ⊆ _V (G), bound_
_|S| from below in terms of the number of components of G −_ _S that_
contain more vertices from A than from B and vice versa.

13.[−] Consider any smallest path cover.

14. Direct all the edges from A to B.

15.[−] Dilworth.

16. Start with the set of minimal elements in P .

17. Think of the elements of A as being smaller than their neighbours in B.

18.[+] Let (x, y) ⩽ (x[′], y[′]) if and only if x ⩽ _x[′]_ and y ⩽ _y[′]._


-----

###### Hints for Chapter 3

1.[−] Recall the definitions of ‘separate’ and ‘component’.
2. Describe in words what the picture suggests.
3. Use Exercise 1 to answer the first question. The second requires an
elementary calculation, which the figure may already suggest.
4. Only the first part needs arguing; the second then follows by symmetry.
So suppose a component of G − _X is not met by X_ _[′], and refer to_
Exercise 1. Where does X _[′]_ lie? Are all our assumptions about X _[′]_

consistent?
5.[−] How can a block fail to be a maximal 2-connected subgraph? And what
else follows then?
6. Deduce the connectedness of the block graph from that of the graph
itself, and its acyclicity from the maximality of each block.
7. Prove the statement inductively using Proposition 3.1.2. Alternatively, choose a cycle through one of the two vertices and with minimum
distance from the other vertex. Show that this distance cannot be
positive.
8. Belonging to the same block is an equivalence relation on the edge set;
see Exercise 5.
9. Induction along Proposition 3.1.2.
10. Assuming that G/xy is not 3-connected, distinguish the cases when vxy
lies inside or outside a separating set of at most 2 vertices.
11. (i) Consider the edges incident with a smaller separator.
(ii) Induction shows that all the graphs obtained by the construction are
cubic and 3-connected. For the converse, consider a maximal subgraph
_TH ⊆_ _G such that H is constructible as stated; then show that H = G._
12.[−] Can any choice of X and P as suggested by Menger’s theorem fail?
13. Choose the disjoint A–B paths in L(G) minimal.
14. Consider a longest cycle C. How are the other vertices joined to C?
15. Consider a cycle through as many of the k given vertices as possible.
If one them is missed, can you re-route the cycle through it?
16. Consider the graph of the hint. Show that any subset of its vertices
that meets all H-paths (but not H) corresponds to a similar subset
of E(G) ∖ _E(H)._ What does a pair of independent H-paths in the
auxiliary graph correspond to in G?
17.[−] How many paths can a single K [2][m][+1] accomodate?
18. Choose suitable degrees for the vertices in B.
19.[+] Let H be the (edgeless) graph on the new vertices. Consider the sets
_X and F that Mader’s theorem provides if G[′]_ does not contain |G|/2
independent H-paths. If G has no 1-factor, use these to find a suitable
set that can play the role of S in Tutte’s theorem.
20. Think small.
21.[−] If two vertices s, t are separated by fewer than 2k − 1 vertices, extend
d _k_ _S_ d h h _G_ _k l_ k d


-----

###### Hints for Chapter 4

1. Embed the vertices inductively. Where should you not put the new
vertex?

2.[−] Figure 1.6.2.

3.[−] Make the given graph connected.

4. This is a generalization of Corollary 4.2.8.

5. Theorem 3.5.4.

6. Imitate the proof of Corollary 4.2.8.

7. Proposition 4.2.10.

8.[−] Express the difference between the two drawings as a formal statement
about vertices, faces, and the incidences between them.

9. Combinatorially: use the definition. Topologically: express the relative
position of the short (respectively, the long) branches of G[′] formally as
a property of G[′] which any topological ismorphism would preserve but
_G lacks._

10.[−] Reflexivity, symmetry, transitivity.

11. Look for a graph whose drawings all look the same, but which admits
an automorphism that does not extend to a homeomorphism of the
plane. Interpret this automorphism as σ2 ◦ _σ1[−][1][.]_

12.[+] Star-shape: every inner face contains a point that sees the entire face
boundary.

13. Work with plane rather than planar graphs.

14. (i) The set X may be infinite.

(ii) If Y is a TX, then every TY is also a TX.

15.[−] By the next exercise, any counterexample can be disconnected by at
most two vertices.

16. Incorporate the extra condition into the induction hypothesis of the
proof. It may help to disallow polygons with 180 degree angles.

17. Number of edges.

18. Use that maximal planar graphs are 3-connected, and that the neighbours of each vertex induce a cycle.

19. If G = G1 ∪ _G2 with G1 ∩_ _G2 = K_ [2], we have a problem. This will go
away if we embed a little more than necessary.

20. Use a suitable modification of the given graph G to simulate outerplanarity.

21. Use the fact that C(G) is the direct sum of C(G1) and C(G2).

22.[+] Euler.

23. The face boundaries generate C(G).

24.[−] Which are the faces that e[∗] (viewed as a polygonal arc) can meet?

25.[−] How many vertices does it have?

26.[−] Join two given vertices of the dual by a straight line, and use this to


-----

27.[+] To show existence, define the required bijections F → _V_ _[∗], E →_ _E[∗],_
_V →_ _F_ _[∗]_ successively in this order, while at the same time constructing G[∗]. Show that connectedness is necessary to ensure that these three
functions can all be made bijective.

28. Solve the previous exercise first.

29. Use the bijections that come with the two duals to define the desired
isomorphism and to prove that it is combinatorial.

30. Apply Menger’s theorem and Proposition 4.6.1. For (iii), consider a
4-connected graph with six vertices.

31. Apply induction on n, starting with part (i) of the previous exercise.

32. Theorem 1.9.5.

33. For the forward implication, consider G[′] := G[∗]. For the converse, apply
a suitable planarity criterion.

###### Hints for Chapter 5

1.[−] Duality.

2.[−] Whenever more than three countries have some point in common, apply
a small local change to the map where this happens.

3. Where does the five colour proof use the fact that v has no more neighbours than there are colours?

4. How can the colourings of different blocks interfere with each other?

5.[−] Use a colouring of G to derive a suitable ordering.

6. Consider how the removal of certain edges may lead the greedy algorithm to use more colours.

7. Describe more precisely how to implement this alternative algorithm.
Then, where is the difference to the traditional greedy algorithm?

8. Compare the number of edges in a subgraph H as in 5.2.2 with the
number m of edges in G.

9. To find f, consider a given graph of small colouring number and partition it inductively into a small number of forest. For g, use Proposition 5.2.2 and the easy direction of Theorem 3.5.4.

10.[−] Remove vertices successively until the graph becomes critically kchromatic. What can you say about the degree of any vertex that
remains?

11. Proposition 1.6.1.

12.[+] Modify colourings of the two sides of a hypothetical cut of fewer than
_k −_ 1 edges so that they combine to a (k − 1)-colouring of the entire
graph (with a contradiction).

13. Proposition 1.3.1.

14.[−] For which graphs with large maximum degree does Proposition 5.2.2


-----

15.[+] (i) How will v1 and v2 be coloured, and how vn?

(ii) Consider the subgraph induced by the neighbours of vn.

16. For the induction start, explicitly calculate PG(k) for |G| = n and
_∥G∥_ = 0.

17.[+] Derive from the polynomial the number of edges and the number of
components of G; see the previous exercise.

18. Imitate the proof of Theorem 5.2.5.

19.[−] _Kn,n._

20. How are edge colourings related to matchings?

21. Construct a bipartite ∆(G)-regular graph that contains G as subgraph.
It may be necessary to add some vertices.

22.[+] Induction on k. In the induction step k → _k + 1, consider using several_
copies of the graph you found for k.

23.[−] Vertex degrees.

24. _Kn,n. To choose n so that Kn,n is not even k-choosable, consider lists_
of k-subsets of a k[2]-set.

25.[−] Vizing’s theorem.

26. All you need are the definitions, Proposition 5.2.2, and a standard
argument from Chapter 1.2.

27.[+] Try induction on r. In the induction step, you would like to to delete
one pair of vertices and only one colour from the other vertices’ lists.
What can you say about the lists if this is impossible? This information
alone will enable you to find a colouring directly, without even looking
at the graph again.

28. Show that χ[′′](G) ⩽ ch[′](G) + 2, and use this to deduce χ[′′](G) ⩽
∆(G) + 3 from the list colouring conjecture.

29.[−] Do bipartite graphs have a kernel?

30.[+] Call a set S of vertices in a directed graph D a core if D contains a
directed v–S path for every vertex v _[∈]_ _D −_ _S. If, in addition, D con-_
tains no directed path between any two vertices of S, call S a strong
_core. Show first that every core contains a strong core. Next, define_
inductively a partition of V (D) into ‘levels’ L0, . . ., Ln such that, for
even i, Li is a suitable strong core in Di := D − (L0 ∪ _. . . ∪_ _Li−1), while_
for odd i, Li consists of the vertices of Di that send an edge to Li−1.
Show that, if D has no directed odd cycle, the even levels together form
a kernel of D.

31. Construct the orientation needed for Lemma 5.4.3 in steps: if, in the
current orientation, there are still vertices v with d[+](v) ⩾ 3, reverse the
directions of an edge at v and take care of the knock-on effect of this
change. If you need to bound the average degree of a bipartite planar
graph, remember Euler’s formula.

32.[−] Start with a non-perfect graph.

33.[−] Do odd cycles or their complements satisfy (∗)?


-----

35. Look at the complement.

36. Define the colour classes of a given induced subgraph H ⊆ _G induc-_
tively, starting with the class of all minimal elements.

37. (i) Can the vertices on an induced cycle contain each other as intervals?

(ii) Use the natural ordering of the reals.

38. Compare ω(H) with ∆(G) (where H = L(G)).

39.[+] Which graphs are such that their line graphs contain no induced cycles
of odd length ⩾ 5? To prove that the edges of such a graph G can be
coloured with ω(L(G)) colours, imitate the proof of Vizing’s theorem.

40. Use A as a colour class.

41.[+] (i) Induction.

(ii) Assume that G contains no induced P [3]. Suppose some H has a
maximal complete subgraph K and a maximal set A of independent
vertices disjoint from K. For each vertex v _[∈]_ _K, consider the set of_
neighbours of v in A. How do these sets intersect? Is there a smallest
one?

42.[+] Start with a candidate for the set O, i.e. a set of maximal complete
subgraphs covering the vertex set of G. If all the elements of O happen to have order ω(G), how does the existence of A follow from the
perfection of G? If not, can you expand G (maintaining perfection) so
that they do and adapt the A for the expanded graph to G?

43.[+] Reduce the general case to the case when all but one of the Gx are
trivial; then imitate the proof of Lemma 5.5.4.

44. Apply the property of H1 to the graphs in H2, and vice versa.

###### Hints for Chapter 6

1.[−] Move the vertices, one by one, from S to S. How does the value of
_f_ (S, S) change each time?

2. (i) Trick the algorithm into repeatedly using the middle edge in alternating directions.

(ii) At any given time during the algorithm, consider for each vertex
_v the shortest s–v walk that qualifies as an initial segment of an aug-_
menting path. Show for each v that the length of this s–v walk never
decreases during the algorithm. Now consider an edge which is used
twice for an augmenting path, in the same direction. Show that the
second of these paths must have been longer than the first. Now derive
the desired bound.

3.[+] For the edge version, define the capacity function so that a flow of maximum value gives rise to sufficiently many edge-disjoint paths. For the
vertex version, split every vertex x into two adjacent vertices x[−], x[+].
Define the edges of the new graph and their capacities in such a way
that positive flow through an edge x[−]x[+] corresponds to the use of x


-----

4.[−] _H-flows are nowhere zero, by definition._

5.[−] Use the definition and Proposition 6.1.1.

6.[−] Do subgraphs also count as minors?

7.[−] Try k = 2, 3, . . . in turn. In searching for a k-flow, tentatively fix the
flow value through an edge and investigate which consequences this has
for the adjacent edges.

8. To establish uniqueness, consider cuts of a special type.

9. Express G as the union of cycles.

10. Combine Z2 -flows on suitable subgraphs to a flow on G.

11.[+] Begin by sending a small amount of flow through every edge outside T .

12. View G as the union of suitably chosen cycles.

13. Corollary 6.3.2 and Proposition 6.4.1.

14.[−] Duality.

15. Take as H your favourite graph of large flow number. Can you decrease
its flow number by adding edges?

16. Euler.

17.[+] Theorem 6.5.3.

18.[−] Search among small cubic graphs.

19. Theorem 6.5.3.

20. (i) Theorem 6.5.3.

(ii) Yes it can. Show, by considering a smallest counterexample, that
if every 3-connected cubic planar multigraph is 3-edge-colourable (and
hence has a 4-flow), then so is every bridgeless cubic planar multigraph.

21.[+] For the ‘only if’ implication apply Proposition 6.1.1. Conversely, consider a circulation f on G, with values in { 0, ±1, . . ., ±(k − 1) }, that
respects the given orientation (i.e. is positive or zero on the edge directions assigned by D) and is zero on as few edges as possible. Then
show that f is nowhere zero, as follows. If f is zero on e = st _[∈]_ _E and_
_D directs e from t to s, define a network N = (G, s, t, c) such that any_
flow in N of positive total value contradicts the choice of f, but any
cut in N of zero capacity contradicts the property assumed for D.

22.[−] Convert the given multigraph into a graph with the same flow properties.

###### Hints for Chapter 7

1.[−] Straightforward from the definition.

2.[−] When constructing the graphs, start by fixing the colour classes.

3. It is not difficult to determine an upper bound for ex(n, K1,r). What
remains to be proved is that this bound can be achieved for all r and n.

4. Proposition 1.7.2 (ii).


-----

6.[+] What is the maximum number of edges in a graph of the structure given
by Theorem 2.2.3 if it has no matching of size k? What is the optimal
distribution of vertices between S and the components of G − _S? Is_
there always a graph whose number of edges attains the corresponding
upper bound?

7. Consider a vertex x _∈_ _G of maximum degree, and count the edges_
in G − _x._

8. Choose k and i so that n = (r − 1)k + i with 0 ⩽ _i < r −_ 1. Treat the
case of i = 0 first, and then show for the general case that tr−1(n) =
12 _rr−−12_ [(][n][2][ −] _[i][2][) +][ �]2[i]�._

9. The bounds given in the hint are the sizes of two particularly simple
Tur´an graphs—which ones?

10.[+] How can you choose v so that the number of edges does not decrease?
Where in the graph can the operation be repeated, and what does the
situation look like when nothing new happens?

11. Choose among the m vertices a set of s vertices that are still incident
with as many edges as possible.

12. For the first inequality, double the vertex set of an extremal graph for
_Ks,t to obtain a bipartite graph with twice as many edges but still not_
containing a Ks,t.

13.[+] For the displayed inequality, count the pairs (x, Y ) such that x _[∈]_ _A and_
_Y ⊆_ _B, with |Y | = r and x adjacent to all of Y . For the bound on_
ex(n, Kr,r), use the estimate (s/t)[t] _≤_ [�][s]t� _≤_ _s[t]_ and the fact that the
function z �→ _z[r]_ is convex.

14. Assume that the upper density is larger than 1 − _r−1_ 1 [. What does this]

mean precisely, and what does the Erd˝os-Stone theorem then imply?

15. Corollary 1.5.4 and Proposition 1.2.2.

16. Complete graphs.

17.[−] Average degree.

18. Do [1]2 [(][k][ −] [1)][n][ edges force a subgraph of suitable minimum degree?]

19. Consider a longest path P in G. Where do its endvertices have their
neighbours? Can G [ P ] contain a cycle on V (P )?

20.[−] Why would it be impractical to include, say, 1-element sets X, Y in the
comparison?

21.[−] Apply the definition of an ϵ-regular pair.

22. Sparse graphs have few edges. How does that affect the average degree
condition in the definition of ϵ-regularity?


-----

###### Hints for Chapter 8

1. For the induction step, partition the vertex set of the given graph G
into two sets V1 and V2 so that colourings of G [ V1 ] and G [ V2 ] can be
combined to a colouring of G.

2. Imitate the start of the proof of Lemma 8.1.3.

3.[−] Does a large chromatic number force up the average degree? If in doubt,
consult Chapter 5.

4.[+] Try parallel paths in the grid as branch sets.

5.[+] How can we best make a TK [2][r] fit into a Ks,s when we want to keep s
small?

6. Split the argument into the cases of k = 0 and k ⩾ 1.

7. How are the two lemmas used in the proof of the theorem?

8. Study the motivational chat preceding the definition of f in the proof.

9.[+] Consider your favourite graphs with high average degree and low chromatic number. Which trees do they contain induced? Is there some
reason to expect that exactly these trees may always be found induced
in graphs of large average degree and small chromatic number?

10.[−] What does planarity have to do with minors?

11.[−] Consider a suitable supergraph.

12.[−] Average degree.

13.[+] Show by induction on |G| that any 3-colouring of an induced cycle in
_G ̸≽_ _K_ [4] extends to all of G.

14.[+] Reduce the statement to critical k-chromatic graphs and apply Vizing’s
theorem.

15. (i) is easy. In the first part of (ii), distinguish between the cases that
the graph is or is not separated by a K _[χ][(][G][)][−][1]. Show the second part_
by induction on the chromatic number. In the induction step split the
vertex set of the graph into two subsets.

16. Induction on the number of construction steps.

17. Induction on |G|.

18. Note the previous exercise.

19. Which of the graphs constructed as in Theorem 8.3.4 have the largest
average degree?

20. Which of the graphs constructed as in the hint have the largest average
degree?

21. Consider the subgraph of G induced by the neighbours of x.


-----

###### Hints for Chapter 9

1.[−] Can you colour the edges of K [5] red and green without creating a red
or a green triangle? Can you do the same for a K [6]?

2. Induction on c. In the induction step, unite two of the colour classes.

3.[+] Choose a well-ordering of R, and compare it with the natural ordering.
Use the fact that countable unions of countable sets are countable.

4.[+] The first and second question are easy. To prove the theorem of Erd˝os
and Szekeres, use induction on k for fixed ℓ, and consider in the induction step the last elements of increasing subsequences of length k.
Alternatively, apply Dilworth’s Theorem.

5. Use the fact that n ⩾ 4 points span a convex polygon if and only if
every four of them do.

6. Translate the given k-partition of { 1, 2, . . ., n } into a k-colouring of the
edges of K _[n]._

7. (i) is easy. For (ii) use the existence of R(2, k, 3).

8. Begin by finding infinitely many sets whose pairwise intersections all
have the same size.

9. The exercise offers more information than you need. Consult Chapter 8.1 to see what is relevant.

10. Consider an auxiliary graph whose vertices are coloured finite subgraphs of the given graph.

11. Imitate the proof of Proposition 9.2.1.

12. The lower bound is easy. Given a colouring for the upper bound, consider a vertex and the neighbours joined to it by suitably coloured
edges.

13.[−] Given H1 and H2, construct a graph H for which the G of Theorem
9.3.1 satisfies (∗).

14. Show inductively for k = 0, . . ., m that ω(G[k]) = ω(H).

15. For the induction step, construct G(H1, H2) from the disjoint union of
_G(H1, H2[′]_ [) and][ G][(][H]1[′] _[, H][2][) by joining some new vertices in a suitable]_
way.

16. Infinity lemma.

17.[−] How exactly does Proposition 9.4.1 fail if we delete K _[r]_ from the statement?

###### Hints for Chapter 10

1. Consider the union of two colour classes.

2. Will the proof of Proposition 10.1.2 go through if we assume χ(G) ⩾
_|G|/k instead of α(G) ⩽_ _k? What do k-connected graphs look like that_
satisfy the first condition but not the second?


-----

4. Figure 10.1.1.

5. Induction on k with n fixed; for the induction step consider G.

6.[−] Recall the definition of a hamiltonian sequence.

7.[−] On which kind of vertices does the Chv´atal condition come to bear?
To check the validity of the condition for G, first find such a vertex.

8. How does an arbitrary connected graph differ from the kind of graph
whose square contains a Hamilton cycle by Fleischner’s theorem? How
could this difference obstruct the existence of a Hamilton cycle?

9.[+] In the induction step consider a minimal cut.

10. Condition (∗) in the proof of Fleischner’s theorem.

11. Induction.

12.[+] How can a Hamilton path P _∈_ _H be modified into another? In how_
many ways? What has this got to do with the degree in G of the last
vertex of P ?

###### Hints for Chapter 11

1.[−] Consider a fixed choice of m edges on { 0, 1, . . ., n }. What is the probability that G _[∈]_ _G(n, p) has precisely this edge set?_

2. Consider the appropriate indicator random variables, as in the proof of
Lemma 11.1.5.

3. Consider the appropriate indicator random variables.

4. Erd˝os.

5. What would be the measure of the set { G } for a fixed G?

6. Consider the complementary properties.

7.[−] _P2,1._

8. Apply Lemma 11.3.2.

9. Induction on |H| with the aid of Exercise 6.

10.[+] (i) Given a pair U, U _[′], calculate the probability that every other vertex_
is joined incorrectly to U ∪ _U_ _[′]. What, then, is the probability that this_
happens for some pair U, U _[′]?_

(ii) Enumerate the vertices of G and G[′] jointly, and construct an isomorphism G → _G[′]_ inductively.

11. Imitate the proof of Lemma 11.2.1.

12. Imitate the proof of Proposition 11.3.1. To bound the probabilities
involved, use the inequality 1 − _x ⩽_ _e[−][x]_ as in the proof of Lemma
11.2.1.

13.[+] (i) Calculate the expected number of isolated vertices, and apply Lemma 11.4.2 as in the proof of Theorem 11.4.3.

(ii) Linearity.


-----

15. For the first problem modify an increasing property slightly, so that it
ceases to be increasing but keeps its threshold function. For the second,
look for an increasing property whose probability does not really depend
on p.

16.[−] Permutations of V (H).

17.[−] This is a result from the text in disguise.

18.[−] Balance.

19. For p/t → 0 apply Lemmas 11.1.4 and 11.1.5. For p/t →∞ apply Corollary 11.4.4.

20. There are only finitely many trees of order k.

21.[+] Show first that no such threshold function t = t(n) can tend to zero as
_n →∞. Then use Exercise 12._

22.[+] Examine the various steps in the proof of Theorem 11.4.3, and note
which changes will be needed. In the final steps of the proof, how are
the sums AF defined, and why is the sum of all the AF with ||F _|| = ∅_
equal to A0? For ||F _|| ̸= ∅, calculate a bound on AF, and show that_
each AF /µ[2] tends to zero as n →∞, as before.

###### Hints for Chapter 12

1.[−] Antisymmetry.

2. Proposition 12.1.1.

3. To prove Proposition 12.1.1, consider an infinite sequence in which
every strictly decreasing subsequence is finite. How does the last element of a maximal decreasing subsequence compare with the elements
that come after it? For Corollary 12.1.2, start by proving that at least
one element forms a good pair with infinitely many later elements.

4. An obvious approach is to try to imitate the proof of Lemma 12.1.3
for ⩽[′]; if it fails, what is the reason? Alternatively, you might try to
modify the injective map produced by Lemma 12.1.3 into an orderpreserving one, without losing the property of a ⩽ _f_ (a) for all a.

5.[−] This is an exercise in precision: ‘easy to see’ is not a proof. . .

6. Start by finding two trees T, T _[′]_ with |T _| < |T_ _[′]| but T ̸⩽_ _T_ _[′]; then iterate._

7. Does the original proof ever map the root of a tree to an ordinary vertex
of another tree?

8.[+] When we try to embed a graph TG in another graph H, the branch
vertices of the TG can be mapped only to certain vertices of H. Enlarge
_G to a similar graph H that does not contain G as a topological minor_
because these vertices of H are inconveniently positioned in H. Then
iterate this example to obtain an infinite antichain.

9.[+] It is. One possible proof uses normal spanning trees with labels, and
imitates the proof of Kruskal’s theorem.


-----

11. For the forward implication, apply Corollary 1.5.2. For the converse,
use induction on k.

12. To prove (T2), consider the edge e of Figure 12.3.1. Checking (T3) is
easy.

13. For the first question, recall Proposition 12.3.6. For the second, try to
modify a tree-decomposition of G into one of the TG without increasing
its width.

14. Lemma 12.3.1 relates the separation properties of a graph G to those
of its decomposition tree T . This exercise illuminates this relationship from the dual viewpoint of connectedness: how are the connected
subgraphs of G related to those of T ?

15.[−] This is just a reformulation of Theorem 12.3.9.

16. Modify the proof given in the text that the k × k grid has tree-width
at least k − 1.

17. Existence was shown in Theorem 12.3.9; the task is to show uniqueness.

18.[+] Work out an explicit description of the sets Wt[′] [similar to the definition]
of the Wt, and compare the two.

19. Induction.

20. Induction.

21. Use the previous exercise and a result from Chapter 8.3. And don’t
despair at a subgraph of W !

22.[+] Show that the parts are precisely the maximal irreducible induced subgraphs of G.

23.[+] Exercise 14.

24. For the forward implication, interpret the subpaths of the decomposition path as intervals. Which subpath corresponds naturally to a given
vertex of G?

25. Follow the proof of Corollary 12.3.12.

26.[+] They do. To prove it, show first that every connected graph G contains
a path whose deletion decreases the path-width of G. Then apply
induction on a suitable set of trees, deleting a suitable path in the
induction step.

27. Consider minimal sets such as XP in Proposition 12.5.1.

28. To answer the first part, construct for each forbidden minor X a finite
set of graphs whose exclusion as topological minors is equivalent to
forbidding X as a minor. For the second part recall Exercise 8.

29. Find the required paths one by one.

30.[+] One direction is just a weakening of Lemma 12.4.5. For the other,
imitate the proof of Lemma 12.3.4.

31.[+] Let X be an externally ℓ-connected set of h vertices in a graph G, where
_h and ℓ_ are large. Consider a small separator S in G: clearly, most of
_X will lie in the same component of G −_ _S. Try to make these ‘large’_
components, perhaps together with their separators S, into the desired


-----

32. Consult Chapter 8.2 for substructures to be found in graphs of large
chromatic number.

33. Derive the minor theorem first for connected graphs.

34. _K_ [5].


-----

### Index

Page numbers in italics refer to definitions; in the case of author names,
they refer to theorems due to that author. The alphabetical order ignores
letters that stand as variables; for example, ‘k-colouring’ is listed under
the letter c.


abstract
dual, 88 –89
graph, 3, 67, 76, 238
acyclic, 12, 60
adjacency matrix, 24
adjacent, 3
Ahuja, R.K., 145
algebraic
colouring theory, 121
flow theory, 128–143
graph theory, ix, 20–25, 28
planarity criteria, 85–86
algorithmic graph theory, 145, 276–277,
281–282
almost, 238, 247–248
Alon, N., 106, 121–122, 249
alternating
path, 29
walk, 52
antichain, 40, 41, 42, 252
Appel, K., 121
arboricity, 61, 99, 118
arc, 68
Archdeacon, D., 281
articulation point, see cutvertex
at, 2
augmenting path
for matching, 29, 40, 285
for network flow, 127, 144


average degree, 5
of bipartite planar graph, 289
bounded, 210
and chromatic number, 101, 106, 178,
185
and connectivity, 11
forcing minors, 169, 179, 184
forcing topological minors, 61, 170–
178
and girth, 237
and list colouring, 106
and minimum degree, 5–6
and number of edges, 5
and Ramsey numbers, 210
and regularity lemma, 154, 166

bad sequence, 252, 280
balanced, 243
Behzad, M., 122
Berge, C., 117
Berge graph, 117
between, 6, 68
Biggs, N.L., 28
bipartite graphs, 14 –15, 27, 91, 95
edge colouring of, 103, 119
flow number of cubic, 133–134
forced as subgraph, 152, 160
list-chromatic index of, 109–110, 122
matching in, 29–34


-----

Birkhoff, G.D., 121
block, 43
graph, 44, 64
B¨ohme, T., 66
Bollob´as, B., 28, 65, 66, 166, 170, 210,
227, 228, 240, 241, 249, 250
bond, see (minimal) cut
space, see cut space
Bondy, J.A., 228
boundary
of a face, 72 –73
bounded subset of R[2], 70
bramble, 258 –260, 281
number, 260, 278
order of, 258
branch
set, 16
vertex, 18
bridge, 10, 36, 125, 135, 215
to bridge, 218
Brooks, R.L., 99, 118
theorem, 99
list colouring version, 121
Burr, S.A., 210

capacity, 126
function, 125
Catlin, P.A., 187
Cayley, A., 121, 248
central vertex, 9, 283
certificate, 111, 274, 282
chain, 13, 40, 41
Chebyshev inequality, 243, 295
Chen, G., 210
choice number, 105
and average degree, 106
of bipartite planar graphs, 119
of planar graphs, 106
_k-choosable, 105_
chord, 7
chordal, 111 –112, 120, 262, 279
_k-chromatic, 95_
chromatic index, 96, 103
of bipartite graphs, 103
vs. list-chromatic index, 105, 108
and maximum degree, 103–105
chromatic number, 95, 139
and K[r]-subgraphs, 100–101, 110–111
of almost all graphs, 240
and average degree, 101, 106, 178,
185
vs. choice number, 105–106
and connectivity, 100


and flow number, 139
forcing minors, 181–185
forcing short cycles, 101, 237
forcing subgraphs, 100–101, 178, 209
forcing a triangle, 119, 209
and girth, 101, 237
as a global phenomenon, 101, 110
and maximum degree, 99
and minimum degree, 99, 100
and number of edges, 98
chromatic polynomial, 118, 146
Chv´atal, V., 194, 215, 216, 228
circle on S[2], 70
circuit, see cycle
circulation, 124, 137, 146
circumference, 7
and connectivity, 64, 214
and minimum degree, 8
class 1 vs. class 2, 105
clique number, 110 –117, 202, 262
of random graph, 232
threshold function, 247
closed
under addition, 128
under isomorphism, 238, 263
wrt. minors, 119, 144, 263
wrt. subgraphs, 119
wrt. supergraphs, 241
walk, 9, 19
cocycle space, see cut space
_k-colourable, 95_
colour class, 95
colour-critical, see critically k-chromatic
colouring, 95 –122
algorithms, 98, 117
and flows, 136–139
number, 99, 118, 119
plane graphs, 96–97, 136–139
in Ramsey theory, 191
total, 119
3-colour theorem, see three colour thm.
4-colour theorem, see four colour thm.
5-colour theorem, see five colour thm.
combinatorial
isomorphism, 77, 78
set theory, 210
compactness argument, 191, 210
comparability graph, 111, 119
complement
of a bipartite graph, 111, 119
of a graph, 4
and perfection, 112, 290
of a property, 263


-----

bipartite, 14
matching, see 1-factor
minor, 179–184, 275
multipartite, 14, 151
part of path-decomposition, 279
part of tree-decomposition, 262
_r-partite, 14_
separator, 261, 279
subgraph, 101, 110–111, 147–151,
232, 247, 257
topological minor, 61–62, 170–178,
184, 186
complexity theory, 111, 274, 282
component, 10
connected, 9
2-connected graphs, 43–45
3-connected graphs, 45–49, 79–80
_k-connected, 10, 64_
externally, 264, 280
minimally connected, 12
minimally k-connected, 65
and vertex enumeration, 9, 13
connectedness, 9, 12, 297
connectivity, 10 –11, 43–66
and average degree, 11
and circumference, 64
and edge-connectivity, 11
external, 264, 280
and girth, 237
and Hamilton cycles, 215
and linkability, 62, 65
and minimum degree, 11
and plane duality, 91
and plane representation, 79–80
Ramsey properties, 207–208
of a random graph, 239
_k-constructible, 101_ –102, 118
contains, 3
contraction, 16 –18
and 3-connectedness, 45–46
and minors, 16–18
in multigraphs, 25–26
and tree-width, 256
convex
drawing, 82, 90, 92
polygon, 209
core, 289
cover
by antichains, 41
of a bramble, 258
by chains, 40, 42
by edges, 119
by paths, 39–40


by vertices, 30, 258
critical, 118
critically k-chromatic, 118, 293
cross-edges, 21, 58
crosses in grid, 258
crown, 208
cube
_d-dimensional, 26, 248_
of a graph, G[3], 227
cubic graph, 5
connectivity of, 64
1-factor in, 36, 41
flow number of, 133–134, 135
cut, 21
capacity of, 126
-cycle duality, 136–138
-edge, see bridge
flow across, 125
minimal, 22, 88
in network, 126
space, 22 –24, 28, 85, 89
cutvertex, 10, 43–44
cycle, 7 –9
-cut duality, 136–138
directed, 119
double cover conjecture, 141, 144
expected number, 234
Hamilton, 144, 213 –228
induced, 7–8, 21, 47, 86, 111, 117,
290
length, 7
long, 8, 26, 64, 118
in multigraphs, 25
non-separating, 47, 86
odd, 15, 99, 117, 290
with orientation, 136 –138
short, 101, 179–180, 235, 237
space, 21, 23–24, 27–28, 47–49, 85–
86, 89, 92–93
threshold function, 247
cyclomatic number, 21

degeneracy, see colouring number
degree, 5
sequence, 216
deletion, 4
∆-system, 209
dense graphs, 148, 150
density
edge density, 148
of pair of vertex sets, 153
upper density, 166
depth-first search tree, 13, 27


-----

diameter, 8 –9, 248
and girth, 8
and radius, 9
Diestel, R., 186, 281
difference of graphs, 4
digon, see double edge
digraph, see directed graph
Dilworth, R.P., 40, 285, 294
Dirac, G.A., 111, 186, 187, 214, 226
directed
cycle, 119
edge, 25
graph, 25, 108, 119
path, 39
direction, 124
disjoint graphs, 3
distance, 8
double
counting, 75, 92, 114–115, 234, 244
edge, 25
wheel, 208
drawing, 67, 76 –80
convex, 92
straight-line, 90
dual
abstract, 88 –89, 91
and connectivity, 91
plane, 87, 91
duality
cycles and cuts, 23–24, 88–89, 136
flows and colourings, 136–139, 291
of plane multigraphs, 87–89

edge, 2
crossing a partition, 21
directed, 25
double, 25
of a multigraph, 25
plane, 70
_X–Y edge, 2_
edge-chromatic number, see chromatic
_index_
edge colouring, 96, 103–105, 191
and flow number, 135
and matchings, 119
_ℓ-edge-connected, 10_
edge-connectivity, 11, 55, 58
edge contraction, 16
and 3-connectedness, 45
vs. minors, 17
in multigraph, 25
edge cover, 119
edge density, 5, 148


forcing subgraphs, 147–167
forcing minors/topological minors,
169–180
and regularity lemma, 154, 166
edge-disjoint spanning trees, 58–61
edge-maximal, 4
vs. extremal, 149, 182
without MK[5], 183
without TK[4], 182
without TK[5], TK3,3, 84
without TK3,3, 185
edge space, 20, 85
Edmonds, J., 42, 282
embedding
of bipartite graphs, 202 –204
in the plane, 76, 80–93
in S[2], 69–70, 77
in surface, 74, 92, 274–276, 280, 281–
282
empty graph, 2
end
of edge, 2, 25
of path, 6
endpoints of arc, 68
endvertex, 2, 25
terminal vertex, 25
equivalence
of planar embeddings, 76–80, 79, 90
of points in R[2], 68
in quasi-order, 277
Erd˝os, P., 101, 121, 151, 152, 163, 166,
167, 187, 197, 208, 209, 210, 215,
228, 232, 235–237, 243, 249, 295
Erd˝os-S´os conjecture, 152, 166, 167
Euler, L., 18–19, 74
Euler
characteristic, 276
formula, 74 –75, 89, 90, 289
tour, 19 –20, 291
Eulerian graph, 19
even
degree, 19, 33
graph, 133, 135, 145
event, 231
evolution of random graphs, 241, 249
exceptional set, 153
excluded minors, see forbidden minors
existence proof, probabilistic, 121, 229,
233, 235–237
expanding a vertex, 113
expectation, 233 –234, 242
exterior face, see outer face
externally k-connected, 264, 280


-----

bipartite graph, 165
vs. edge-maximal, 149, 182
graph theory, 147, 151, 160, 166
graph, 149 –150
without MK[5], 183
without TK[4], 182
without TK[5], 184
without TK3,3, 185

face, 70
factor, 29
1-factor, 29–38
1-factor theorem, 35, 42, 66
2-factor, 33
_k-factor, 29_
factor-critical, 36, 285
Fajtlowicz, S., 187
fan, 55
-version of Menger’s theorem, 55
finite graph, 2
first order sentence, 239
first point on frontier, 68
five colour theorem, 96, 121, 141
list version, 106, 121
five-flow conjecture, 140, 141
Fleischner, H., 218, 295
flow, 123–146, 125 –126
_H-flow, 128_ –133
_k-flow, 131_ –134, 140–143, 145
2-flow, 133
3-flow, 133–134, 141
4-flow, 134–135, 140–141
6-flow theorem, 141 –143
-colouring duality, 136–139, 291
conjectures, 140–141
group-valued, 128–133, 144
integral, 126, 128
network flow, 125 –128, 291
number, 131 –134, 140, 144
in plane graphs, 136–139
polynomial, 130, 146
total value of, 126
forbidden minors
and chromatic number, 181–185
expressed by, 263, 274–277
minimal set of, 274, 280, 281
planar, 264
and tree-width, 263–274
forcibly hamiltonian, see hamiltonian
_sequence_
forcing
_MK[r], 179–184, 186_
_TK[5], 184, 187_


high connectivity, 11
induced trees, 178
large chromatic number, 101–103
linkability, 62–63, 66, 171–174
long cycles, 8, 26, 118, 213–228
long paths, 8, 166
minor with large minimum degree,
174, 179
short cycles, 179–180, 237
subgraph, 13, 147–167
tree, 13, 178
triangle, 119, 209
Ford, L.R. Jr., 127, 145
forest, 12
partitions, 60–61
minor, 281
four colour problem, 120, 186
four colour theorem, 96, 141, 145, 181,
183, 185, 215, 227
history, 120–121
four-flow conjecture, 140 –141
Frank, A., 65, 145
Frobenius, F.G, 42
from . . . to, 6
frontier, 68
Fulkerson, D.R., 122, 127, 145

Gallai, T., 39, 42, 66, 167
Gallai-Edmonds matching theorem, 36–
38, 42
Galvin, F., 109
Gasparian, G.S., 122
genus
and colouring, 121
of a surface, 276
of a graph, 90, 280
geometric dual, see plane dual
Gibbons, A., 145
Gilmore, P.C., 120
girth, 7
and average degree, 237
and chromatic number, 101, 121,
235–237
and connectivity, 237
and diameter, 8
and minimum degree, 8, 179–180, 237
and minors, 179–180
and planarity, 89
and topological minors, 178
Godsil, C., 28
Golumbic, M.C., 122
good
characterization, 274, 282


-----

sequence, 252
Gorbunov, K.Yu., 281
G¨oring, F., 66
Graham, R.L., 210
graph, 2 –4, 25, 26
invariant, 3
minor theorem, 251, 274–277, 275
partition, 60
plane, 70 –76, 87–89, 96–97, 106–108,
136–139
process, 250
property, 238
simple, 26
graphic sequence, see degree sequence
graph-theoretical isomorphism, 77 –78
greedy algorithm, 98, 108, 117
grid, 90, 184, 258
minor, 260, 264–274
theorem, 264
tree-width of, 260, 278, 281
Gr¨otzsch, H., 97, 141, 145
group-valued flow, 128–133
Gr¨unwald, T., 66
Guthrie, F., 120
Gy´arf´as, A., 178, 185

Hadwiger, H., 181, 186, 187
conjecture, 169–170, 181 –183, 185,
186–187
Hajnal, A., 197, 210
Haj´os, G., 102, 187
construction, 101–102
Haken, W., 121
Halin, R., 65–66, 227, 280–281
Hall, P., 31, 42
Hamilton, W.R., 227
Hamilton closure, 226
Hamilton cycle, 213 –228
in almost all graphs, 241
and degree sequence, 216–218, 226
in G[2], 218–226
in G[3], 227
and the four colour theorem, 215
and 4-flows, 144, 215
and minimum degree, 214
in planar graphs, 215
power of, 226
sufficient conditions, 213–218
Hamilton path, 213, 218
hamiltonian
graph, 213
sequence, 216
Harant, J., 66


Heawood, P.J., 121, 145
Heesch, H., 121
hereditary graph property, 263, 274–277
algorithmic decidability, 276–277
Higman, D.G., 252, 280
Hoffman, A.J., 120
hypergraph, 25

in (a graph), 7
incidence, 2
encoding of planar embedding, see
_combinatorial isomorphism_
map, 25–26
matrix, 24
incident, 2, 72
increasing property, 241, 248
independence number, 110 –117
and connectivity, 214–215
and Hamilton cycles, 215
and long cycles, 118
and path cover, 39
of random graph, 232, 248
independent
edges, 3, 29–38
events, 231
paths, 7, 55, 56–57, 283
vertices, 3, 39, 110, 232
indicator random variable, 234, 295
induced subgraph, 3, 111, 116–117, 290
of almost all graphs, 238, 248
cycle, 7–8, 21, 47, 75, 86, 111, 117,
290
of all imperfect graphs, 116–117, 120
of all large connected graphs, 207
in Ramsey theory, 196–206
in random graph, 232, 249
tree, 178
infinite graphs, ix, 2, 28, 41, 166, 209,
248, 280
infinity lemma, 192, 210, 294
initial vertex, 25
inner face, 70
inner vertex, 6
integral
flow, 126, 128
function, 126
random variable, 242
interior
of an arc, 68
of a path, P[˚], 6–7
internally disjoint, see independent
intersection, 3
graph, 279


-----

into, 255
intuition, 70, 231
invariant, 3
irreducible graph, 279
isolated vertex, 5, 248
isomorphic, 3
isomorphism, 3
of plane graphs, 76–80
isthmus, see bridge

Jaeger, F., 146
Janson, S., 249
Jensen, T.R., 120, 146, 281
Johnson, D., 282
join, 2
Jordan, C., 68, 70
Jung, H.A., 62, 186

Kahn, J., 122
Karo´nski, M., 249
Kempe, A.B., 121, 227
kernel
of incidence matrix, 24
of directed graph, 108 –109,119
Kirchhoff’s law, 123, 124
Klein four-group, 135
Kleitman, D.J., 121
knotless graph, 277
knot theory, 146
Kohayakawa, Y., 167
Koll´ar, J., 167
Koml´os, J., 167, 170, 186, 210, 226
K¨onig, D., 30, 42, 52, 103, 119, 192,
210
duality theorem, 30, 39, 111
infinity lemma, 192, 210, 294
K¨onigsberg bridges, 19
Kostochka, A.V., 179
Kruskal, J.A., 253, 280, 296
Kuratowski, C., 80 –84, 274
Kuratowski-type characterization, 90,
274–275, 281–282

Larman, D.G., 62
Latin square, 119
leaf, 12, 27
lean tree-decomposition, 261
length
of a cycle, 7
of a path, 6, 8
of a walk, 9
line (edge), 2


linear algebra, 20–25, 47–49, 85–86, 116
linear programming, 145
linked
by an arc, 68
by a path, 6
_k-linked, 61_ –63, 66
vs. k-connected, 62, 65
(k, ℓ)-linked, 170
set, 170
tree-decomposition, 261
vertices, 6, 68
list
-chromatic index, 105, 108–110, 121–
122
-chromatic number, see choice num_ber_
colouring, 105 –110, 121–122
bipartite graphs, 108–110, 119
Brooks’s theorem, 121
conjecture, 108, 119, 122
_k-list-colourable, see k-choosable_
logarithms, 1
loop, 25
Lov´asz, L., 42, 112, 115, 121, 122, 167
�Luczak, T., 249, 250

MacLane, S., 85, 92
Mader, W., 11, 56 –57, 61, 65, 66, 178,
_184, 186, 187_
Magnanti, T.L., 145
Mani, P., 62
map colouring, 95–97, 117, 120, 136
Markov chain, 250
Markov’s inequality, 233, 237, 242, 244
marriage theorem, 31, 33, 42, 285
matchable, 36
matching, 29 –42
in bipartite graphs, 29–34, 111
and edge colouring, 119
in general graphs, 34–38
of vertex set, 29
M´at´e, A., 210
matroid theory, 66, 93
max-flow min-cut theorem, 125, 127,
144, 145
maximal, 4
acyclic graph, 12
planar graph, 80, 84, 90, 92, 183, 185
plane graph, 73, 80
maximum degree, 5
bounded, 161, 194
and chromatic number, 99
and chromatic index, 103–105


-----

and radius, 9, 26
and Ramsey numbers, 194–196
Menger, K., 42, 50 –55, 64, 144, 288
_k-mesh, 265_
Milgram, A.N., 39
minimal, 4
connected graph, 12
_k-connected graph, 65_
cut, 22, 88, 136
set of forbidden minors, 274, 280,
281–282
non-planar graph, 90
separating set, 63
minimum degree, 5
and average degree, 5
and choice number, 106
and chromatic number, 99, 100
and circumference, 8
and connectivity, 11, 65–66
forcing Hamilton cycle, 214, 226
forcing long cycles, 8
forcing long paths, 8, 166
forcing short cycles, 179–180, 237
forcing trees, 13
and girth, 178, 179–180, 237
and linkability, 171
minor, 16–19, 17
_K3,3, 92, 185_
_K[4], 182, 263_
_K[5], 183, 186_
_K[5]_ and K3,3, 80–84
_K[6], 183_
_K[r], 180, 181_
of all large 3- or 4-connected graphs,
208
forbidden, 181–185, 263 –277, 279,
280, 281–282
forced, 174, 179–186
infinite, 280
of multigraph, 26
Petersen graph, 140
and planarity, 80–84, 90
relation, 18, 274
theorem, 251, 274–277, 275
for trees, 253–254
proof, 275–276
vs. topological minor, 18–19, 80
and WQO, 251–277
(see also topological minor)
M¨obius
crown, 208
ladder, 183
Mohar, B., 92, 121, 281–282


first, see Markov’s inequality
second, 242–247
monochromatic (in Ramsey theory)
induced subgraph, 196–206
(vertex) set, 191 –193
subgraph, 191, 193–196
multigraph, 25 –26
list chromatic index of, 122
plane, 87
multiple edge, 25
Murty, U.S.R., 228

Nash-Williams, C.St.J.A., 58, 60, 66,
280
neighbour, 3, 4
Neˇsetˇril, J., 210, 211
network, 125 –128
theory, 145
node (vertex), 2
normal tree, 13 –14, 27, 139, 144, 296
nowhere
dense, 61
zero, 128, 146
null, see empty

obstruction
to small tree-width, 258–260, 264–
265, 280, 281
octahedron, 11, 15
odd
component, 34
cycle, 15, 99, 117, 290
degree, 5
on, 2
one-factor theorem, 35, 66
Oporowski, B., 208
order
of deletion/contraction, 17
of a bramble, 258
of a graph, 2
of a mesh or premesh, 265
partial, 13, 18, 27, 40, 41, 120, 277
quasi-, 251 –252, 277–278
tree-, 13, 27
well-quasi-, 251 –253, 275, 277, 278,
280
orientable surface, 280
plane as, 137
orientation, 25, 108, 145, 289
cycle with, 136 –137
oriented graph, 25
Orlin, J.B., 145


-----

outerplanar, 91
Oxley, J.G., 93, 208

Palmer, E.M., 249
parallel
edges, 25
paths, 293
parity, 5, 34, 37, 227
part of tree-decomposition, 255
partially ordered set, 40, 41, 42
_r-partite, 14_
partition, 1, 60, 191
pasting, 111, 182, 183, 185, 261
path, 6 –9
_a–b-path, 7, 55_
_A–B-path, 7, 50–55_
_H-path, 7, 44–45, 56–57, 64, 65, 66_
alternating, 29, 32
between given pairs of vertices, 61–
63, 66, 170
cover, 39 –40, 285
-decomposition, 279
directed, 39
disjoint paths, 39, 50–55
edge-disjoint, 55, 57, 58
-hamiltonian sequence, 218
independent paths, 7, 55, 56–57, 283
induced, 207
length, 6
linkage, 61–63, 66, 170, 172
long, 8
-width, 279, 281
Pelik´an, J., 185
perfect, 111 –117, 119–120, 122
graph conjecture, 117
graph theorem, 112, 115, 117, 122
matching, see 1-factor
Petersen, J., 33, 36
Petersen graph, 140 –141
physics, 146
piecewise linear, 67
planar, 80 –89, 274
embedding, 76, 80–93
planarity criteria
Kuratowski, 84
MacLane, 85
Tutte, 86
Whitney, 89
plane
dual, 87
duality, 87–89, 91, 136–139, 288
graph, 70 –76,
multigraph, 87 –89, 136–139


Plummer, M.D., 42
point (vertex), 2
pointwise greater, 216
polygon, 68
polygonal arc, 68, 69
P´osa, L., 197, 226
power of a graph, 218
precision, 296
premesh, 265
probabilistic method, 229, 235–238, 249
projective plane, 275, 281
Pr¨omel, H.J., 117, 122
property, 238
of almost all graphs, 238–241, 247–
248
hereditary, 263
increasing, 241
pseudo-random graph, 210
Pym, J.S., 66

quasi-ordering, 251 –252, 277–278

radius, 9
and diameter, 9, 26
and maximum degree, 9, 26
Rado, R., 210
Rado’s selection lemma, 210
Ramsey, F.P., 190 –193
Ramsey
graph, 197
-minimal, 196
numbers, 191, 193 –194, 209, 210, 232
Ramsey theory, 189–208
and connectivity, 207–208
induced, 196–206
infinite, 192, 208, 210
random graph, 179, 194, 229–250, 231
evolution, 241
infinite, 248
process, 250
uniform model, 250
random variable, 233
indicator r.v., 234, 295
reducible configuration, 121
Reed, B.A., 281
refining a partition, 1, 155–159
region, 68 –70
on S[2], 70
regular, 5, 33, 226
_ϵ-regular_
pair, 153, 166
partition, 153


-----

graph, 161
inflated, Rs, 194
lemma, 148, 153–164, 154, 167, 210
R´enyi, A., 243, 249
Richardson, M., 119
rigid-circuit, see chordal
ˇR´ıha, S., 228
Robertson, N., 66, 121, 183, 186, 257,
_264, 275, 281_
R¨odl, V., 167, 194, 197, 211
R´onyai, L., 167
root, 13
rooted tree, 13, 253, 278
Rothschild, B.L., 210
Royle, G.F., 28
Ruci´nski, A., 249

Sanders, D.P., 121
S´ark¨ozy, G.N., 226
saturated, see edge-maximal
Schelp, R.H., 210
Schoenflies, A.M., 70
Schrijver, A., 145
Schur, I, 209
Scott, A.D., 167, 178, 209
second moment, 242 –247
self-minor conjecture, 280
separate
a graph, 10, 50, 55, 56
the plane, 68
separating set, 10
sequential colouring, see greedy algo_rithm_
series-parallel, 185
_k-set, 1_
set system, see hypergraph
Seymour, P.D., 66, 92, 121, 141, 183,
186, 187, 226, 257, 258, 264, 275,
280, 281
shift-graph, 209
Simonovits, M., 166, 167, 210
simple
basis, 85, 92–93
graph, 26
simplicial tree-decomposition, 261, 275,
279, 281
sink, 125
six-flow theorem, 141
snark, 141
planar, 141, 145, 215
S´os, V., 152, 166, 167
source, 125
spanned subgraph, 3


subgraph, 3
trees, 13, 14
edge disjoint, 58–60
number of, 248
sparse graphs, 147, 169–185, 194
Spencer, J.H., 210, 249
Sperner’s lemma, 41
square
of graph, 218
Latin, 119
stability number, see independence
_number_
stable set, 3
standard basis, 20
star, 15, 166, 196
induced, 207
star-shape, 287
Steger, A., 117, 122
Steinitz, E., 92
stereographic projection, 69
Stone, A.H., 151, 160
straight line segment, 68
strong core, 289
subcontraction, see minor
subdividing vertex, 18
subdivision, 18
subgraph, 3
of all large k-connected graphs, 207–
208
forced by edge density, 147–164
of high connectivity, 11
induced, 3
of large minimum degree, 5–6, 99,
118
sum
of edge sets, 20
of flows, 133
supergraph, 3
symmetric difference, 20, 29–30, 40, 53
system of distinct representatives, 41
Szab´o, T., 167
Szekeres, G., 208, 209
Szemer´edi, E., 154, 170, 186, 194, 226
see also regularity lemma

tail, see initial vertex
Tait, P.G., 121, 227–228
tangle, 281
Tarsi, M., 121
terminal vertex, 25
Thomas, R., 121, 183, 208, 210, 258,
280


-----

Thomassen, C., 65, 92, 106, 121, 179,
185, 187, 228, 281, 282
three colour theorem, 97
three-flow conjecture, 141
threshold function, 241 –247, 250
Toft, B., 120, 146
topological isomorphism, 76, 78, 88
topological minor, 17 –18
_K3,3, 92, 185_
_K[4], 182, 185, 263_
_K[5], 92, 184_
_K[5]_ and K3,3, 75, 80–84
_K[5]_
_−[, 185]_
_K[r], 61, 170–178_
of all large 2-connected graphs, 207
forced by average degree, 61, 170–178
forced by chromatic number, 181
forced by girth, 178
induced, 178
as order relation, 18
vs. ordinary minor, 18–19, 80
and planarity, 75, 80–84, 90
tree (induced), 178
and WQO of general graphs, 278
and WQO of trees, 253
torso, 279
total chromatic number, 119
total colouring, 119
conjecture, 119, 122
total value of a flow, 126
touching sets, 258
tournament, 227
transitive graph, 41
travelling salesman problem, 227
tree, 12 –14
cover, 61
as forced substructure, 13, 178, 185
normal, 13 –14, 27, 139, 144, 296
-order, 13
threshold function for, 247
well-quasi-ordering of trees, 253–254
tree-decomposition, 186, 255 –262, 278,
280–281
induced on subgraphs, 256
induced on minors, 256
lean, 261
obstructions, 258–260, 264–265, 280,
281
part of, 255
simplicial, 261, 275, 279, 281
width of, 257
tree-width, 257 –274
and brambles, 258–260, 278, 281


and forbidden minors, 263–274
of grid, 260, 278, 281
of a minor, 257
of a subdivision, 278
obstructions to small, 258–260, 264–
265, 280, 281
triangle, 3
triangulated, see chordal
triangulation, see plane triangulation
trivial graph, 2
Trotter, W.T., 194
Tur´an, P., 150
theorem, 150, 195
graph, 149 –152, 166, 292
Tutte, W.T., 35, 46, 47, 58, 65, 66, 86,
92, 128, 131, 139, 145, 146, 215,
228
flow conjectures, 140 –141
Tutte polynomial, 146
Tychonov, A.N., 210

unbalanced subgraph, 247, 249
uniformity lemma, see regularity lemma
union, 3
unmatched, 29
upper density, 166
Urquhart, A., 121

valency (degree), 5
value of a flow, 126
variance, 242
vertex, 2
-chromatic number, 95
colouring, 95, 98–103
-connectivity, 10
cover, 30
cut, see separating set
of a plane graph, 70
space, 20
-transitive, 41
Vince, A., 249
Vizing, V.G., 103, 121, 122, 289, 290,
293
Voigt, M., 121

Wagner, K., 84, 93, 183, 184, 185, 186,
281
‘Wagner’s Conjecture’, 281
Wagner graph, 183, 261–262, 279
walk, 9
alternating, 52
closed, 9


-----

well-ordering, 294
well-quasi-ordering, 251 –282
Welsh, D.J.A., 146
wheel, 46
theorem, 46, 65


Whitney, H., 66, 80, 89
width of tree-decomposition, 257
Winkler, P., 249

Zykov, A.A., 166


-----

### Symbol Index

The entries in this index are divided into two groups. Entries involving
only mathematical symbols (i.e. no letters except variables) are listed on
the first page, grouped loosely by logical function. The entry ‘[ ]’, for
example, refers to the definition of induced subgraphs H [ U ] on page 4
as well as to the definition of face boundaries G [ f ] on page 72.
Entries involving fixed letters as constituent parts are listed on the
second page, in typographical groups ordered alphabetically by those
letters. Letters standing as variables are ignored in the ordering.


2
_∅_
= 3
3
_≃_
3
_⊆_
⩽ 251
≼ 16

+ 4, 19, 128
4, 70, 128
_−_

_∈_ 2
∖ 70
3
_∪_
3
_∩_
4
_∗_

1
_⌊⌋_
1
_⌈⌉_
2, 126
_| |_
2, 153
_∥∥_

[ ] 4, 72


_,_ 19
_⟨_ _⟩_
_/_ 15, 16, 24
_,_, . . . 19
_C[⊥]_ _F_ _[⊥]_

0, 1, 2, . . . 1
(n)k, . . . 232
_E(v), E[′](w), . . ._ 2
_E(X, Y ), E[′](U, W_ ), . . . 2
(e, x, y), . . . 124

_E,→_ _F,→_ _C→, . . ._ 124, 136, 138

_←e,_ _E,←_ _F←, . . ._ 124
_f_ (X, Y ), g(U, W ), . . . 124
_G[∗], F_ _[∗],_ _→e ∗, . . . 88, 136, 140_
_G[2], H_ [3], . . . 216

_G, X,_, . . . 4, 124, 258
_G_
(S, S), . . . 126
_xy, x1 . . . xk, . . ._ 2, 7
_xP, Px, xPy, xPyQz, . . . 7_
_P,˚_ ˚xQ, . . . 7, 68


-----

F2 19
N 1
Zn 1

_CG_ 34
(G) 20
_C_
(G) 21
_C[∗]_
(G) 19
_E_
(n, p) 228
_G_
_PH_ 241
_Pi,j_ 236
(G) 19
_V_

_C_ _[k]_ 7
_E(G)_ 2
_E(X)_ 231
_F_ (G) 70
Forb≼(X ) 257
_G(H1, H2)_ 196
_K_ _[n]_ 3
_Kn1,...,nr_ 14
_Ks[r]_ 14
_L(G)_ 4
_MX_ 15
_N_ (v), N (U ) 4
_N_ [+](v) 108
_P_ 229
_P_ _[k]_ 6
_PG_ 118
_R(H)_ 191
_R(H1, H2)_ 191
_R(k, c, r)_ 191
_R(r)_ 189
_Rs_ 161
_S[n]_ 69
_TX_ 16
_T_ _[r][−][1](n)_ 149
_V (G)_ 2

ch(G) 105
ch[′](G) 105


col(G) 99
_d(G)_ 5
_d(v)_ 5
_d[+](v)_ 108
_d(x, y)_ 8
_d(X, Y )_ 153
diam(G) 8
ex(n, H) 149
_f_ _[∗](v)_ 88
_g(G)_ 7

_i_ 1
init(e) 23
log, ln 1
pw(G) 259
_q(G)_ 34
rad(G) 9
_tr−1(n)_ 149
ter(e) 23
tw(G) 255
_ve, vxy, vU_ 15, 16
_v[∗](f_ ) 88

∆(G) 5

_α(G)_ 110
_δ(G)_ 5
_ε(G)_ 5
_κ(G)_ 10
_κG(H)_ 56
_λ(G)_ 11
_λG(H)_ 56
_µ_ 240
_π : S[2]_ ∖ _{ (0, 0, 1) } →_ R[2] 69
_σk : Z →_ Zk 131
_σ[2]_ 240
_ϕ(G)_ 131
_χ(G)_ 95
_χ[′](G)_ 96
_χ[′′](G)_ 119
_ω(G)_ 110


-----

**Reinhard Diestel received a PhD from the University of Cambridge, follow-**
ing research 1983–86 as a scholar of Trinity College under B´ela Bollob´as. He
was a Fellow of St. John’s College, Cambridge, from 1986 to 1990. Research
appointments and scholarships have taken him to Bielefeld (Germany), Oxford
and the US. He became a professor in Chemnitz in 1994 and has held a chair
at Hamburg since 1999.
Reinhard Diestel’s main area of research is graph theory, including infinite
graph theory. He has published numerous papers and a research monograph,


-----

