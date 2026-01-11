# The Complexity of Boolean Functions

## Ingo Wegener
#### Johann Wolfgang Goethe-Universit¨at

###### WARNING:

 This version of the book is for your personal use only. The material is copyrighted and may not be redistributed.


-----

Copyright c 1987 by John Wiley & Sons Ltd, and B. G. Teubner, Stuttgart.
_⃝_

All rights reserved.

No part of this book may be reproduced by any means, or transmitted, or translated
into a machine language without the written permission of the publisher.

**Library of Congress Cataloguing in Publication Data:**
Wegener, Ingo
The complexity of boolean functions.
(Wiley-Teubner series in computer science)
Bibliography: p.
Includes index.
1. Algebra, Boolean. 2. Computational complexity.
I. Title. II. Series.
AQ10.3.W44 1987 511.3’24 87-10388

ISBN 0 471 91555 6 (Wiley)

**British Library Cataloguing in Publication Data:**

Wegener, Ingo
The complexity of Boolean functions.—(Wiley-Teubner series in computer science).
1. Electronic data processing—Mathematics 2. Algebra, Boolean
I. Title. II. Teubner, B. G.
004.01’511324 QA76.9.M3

ISBN 0 471 91555 6

**CIP-Kurztitelaufnahme der Deutschen Bibliothek**

Wegener, Ingo
The complexity of Boolean functions/Ingo Wegener.—Stuttgart: Teubner; Chichester; New York; Brisbane; Toronto; Singapore: Wiley, 1987
(Wiley-Teubner series in computer science)
ISBN 3 519 02107 2 (Teubner)
ISBN 0 471 91555 6 (Wiley)

Printed and bound in Great Britain


-----

###### On this version of the “Blue Book”

 This version of “The Complexity of Boolean Functions,” for some people simply the “Blue Book” due to the color of the cover of the orig- inal from 1987, is not a print-out of the original sources. It is rather a “facsimile” of the original monograph typeset in L[A]TEX.
 The source files of the Blue Book which still exist (in 1999) have been written for an old version of troff and virtually cannot be printed out anymore. This is because the (strange) standard font used for the text as well as the special fonts for math symbols seem to be nowhere to find today. Even if one could find a solution for the special symbols, the available text fonts yield a considerably different page layout which seems to be undesirable. Things are further complicated by the fact that the source files for the figures have been lost and would have to be redone with pic.
 Hence, it has been decided to translate the whole sources to L[A]TEX in order to be able to fix the above problems more easily. Of course, the result can still only be an approximation to the original. The fonts are those of the CM series of L[A]TEX and have different parameters than the original ones. For the spacing of equations, the standard mechanisms of L[A]TEX have been used, which are quite different from those of troff. Hence, it is nearly unavoidable that page breaks occur at different places than in the original book. Nevertheless, it has been made sure that all numbered items (theorems, equations) can be found on the same pages as in the original.

 You are encouraged to report typos and other errors to Ingo Wegener by e-mail: wegener@ls2.cs.uni-dortmund.de


-----

-----

###### Preface

 When Goethe had fundamentally rewritten his IPHIGENIE AUF TAURIS eight years after its first publication, he stated (with resig- nation, or perhaps as an excuse or just an explanation) that, ˝Such a work is never actually finished: one has to declare it finished when one has done all that time and circumstances will allow.˝ This is also my feeling after working on a book in a field of science which is so much in flux as the complexity of Boolean functions. On the one hand it is time to set down in a monograph the multiplicity of important new results; on the other hand new results are constantly being added.

 I have tried to describe the latest state of research concerning re- sults and methods. Apart from the classical circuit model and the parameters of complexity, circuit size and depth, providing the basis for sequential and for parallel computations, numerous other models have been analysed, among them monotone circuits, Boolean formu- las, synchronous circuits, probabilistic circuits, programmable (univer- sal) circuits, bounded depth circuits, parallel random access machines and branching programs. Relationships between various parameters of complexity and various models are studied, and also the relationships to the theory of complexity and uniform computation models.

 The book may be used as the basis for lectures and, due to the inclusion of a multitude of new findings, also for seminar purposes. Numerous exercises provide the opportunity of practising the acquired methods. The book is essentially complete in itself, requiring only basic knowledge of computer science and mathematics.

 This book I feel should not just be read with interest but should encourage the reader to do further research. I do hope, therefore, to have written a book in accordance with Voltaire’s statement, ˝The most useful books are those that make the reader want to add to

**v**


-----

**vi**

###### them.˝

 I should like to express my thanks to Annemarie Fellmann, who set up the manuscript, to Linda Stapleton for the careful reading of the text, and to Christa, whose complexity (in its extended definition, as the sum of all features and qualities) far exceeds the complexity of all Boolean functions.

 Frankfurt a.M./Bielefeld, November 1986 Ingo Wegener


-----

###### Contents

 1. Introduction to the theory of Boolean functions and circuits 1 1.1 Introduction 1 1.2 Boolean functions, laws of computation, normal forms 3 1.3 Circuits and complexity measures 6 1.4 Circuits with bounded fan-out 10 1.5 Discussion 15 Exercises 19

 2. The minimization of Boolean functions 22 2.1 Basic definitions 22 2.2 The computation of all prime implicants and reductions of the table of prime implicants 25 2.3 The minimization method of Karnaugh 29 2.4 The minimization of monotone functions 31 2.5 The complexity of minimizing 33 2.6 Discussion 35 Exercises 36

 3. The design of efficient circuits for some fundamental functions 39 3.1 Addition and subtraction 39 3.2 Multiplication 51 3.3 Division 67 3.4 Symmetric functions 74 3.5 Storage access 76 3.6 Matrix product 78 3.7 Determinant 81 Exercises 83

**vii**


-----

**viii**

###### 4. Asymptotic results and universal circuits 87 4.1 The Shannon effect 87 4.2 Circuits over complete bases 88 4.3 Formulas over complete bases 93 4.4 The depth over complete bases 96 4.5 Monotone functions 98 4.6 The weak Shannon effect 1 06 4.7 Boolean sums and quadratic functions 107 4.8 Universal circuits 110 Exercises 117

 5. Lower bounds on circuit complexity 119 5.1 Discussion on methods 119 5.2 2 n - bounds by the elimination method 122 5.3 Lower bounds for some particular bases 125 5.4 2.5 n - bounds for symmetric functions 127 5.5 A 3n - bound 133 5.6 Complexity theory and lower bounds on circuit complexity 138 Exercises 142

 6. Monotone circuits 145 6.1 Introduction 145 6.2 Design of circuits for sorting and threshold functions 148 6.3 Lower bounds for threshold functions 154 6.4 Lower bounds for sorting and merging 158 6.5 Replacement rules 160 6.6 Boolean sums 163 6.7 Boolean convolution 168 6.8 Boolean matrix product 170 6.9 A generalized Boolean matrix product 173 6.10 Razborov’s method 180 6.11 An exponential lower bound for clique functions 184 6.12 Other applications of Razborov’s method 192


-----

**ix**

###### 6.13 Negation is powerless for slice functions 195 6.14 Hard slices of NP-complete functions 203 6.15 Set circuits - a new model for proving lower bounds 207 Exercises 214

 7. Relations between circuit size, formula size and depth 218 7.1 Formula size vs. depth 218 7.2 Circuit size vs. formula size and depth 221 7.3 Joint minimization of depth and circuit size, trade-offs 225 7.4 A trade-off result 229 Exercises 233

 8. Formula size 235 8.1 Threshold - 2 235 8.2 Design of efficient formulas for threshold - k 239 8.3 Efficient formulas for all threshold functions 243 8.4 The depth of symmetric functions 247 8.5 The Hodes and Specker method 249 8.6 The Fischer, Meyer and Paterson method 251 8.7 The Nechiporuk method 253 8.8 The Krapchenko method 258 Exercises 263

 9. Circuits and other non uniform computation methods vs. Turing machines and other uniform computation models 267 9.1 Introduction 267 9.2 The simulation of Turing machines by circuits: time and size 271 9.3 The simulation of Turing machines by circuits: space and depth 277 9.4 The simulation of circuits by Turing machines with oracles 279 9.5 A characterization of languages with polynomial circuits 282 9.6 Circuits and probabilistic Turing machines 285


-----

**x**

###### 9.7 May NP-complete problems have polynomial circuits ? 288 9.8 Uniform circuits 292 Exercises 294

 10. Hierarchies, mass production and reductions 296 10.1 Hierarchies 296 10.2 Mass production 301 10.3 Reductions 306 Exercises 318

 11. Bounded-depth circuits 320 11.1 Introduction 320 11.2 The design of bounded-depth circuits 321 11.3 An exponential lower bound for the parity function 325 11.4 The complexity of symmetric functions 332 11.5 Hierarchy results 337 Exercises 338

 12. Synchronous, planar and probabilistic circuits 340 12.1 Synchronous circuits 340 12.2 Planar and VLSI - circuits 344 12.3 Probabilistic circuits 352 Exercises 359

 13. PRAMs and WRAMs: Parallel random access machines 361 13.1 Introduction 361 13.2 Upper bounds by simulations 363 13.3 Lower bounds by simulations 368 13.4 The complexity of PRAMs 373 13.5 The complexity of PRAMs and WRAMs with small communication width 380 13.6 The complexity of WRAMs with polynomial resources 387 13.7 Properties of complexity measures for PRAMs and WRAMs 396 Exercises 411


-----

**xi**

###### 14. Branching programs 414 14.1 The comparison of branching programs with other models of computation 414 14.2 The depth of branching programs 418 14.3 The size of branching programs 421 14.4 Read-once-only branching programs 423 14.5 Bounded-width branching programs 431 14.6 Hierarchies 436 Exercises 439

 References 442

 Index 455


-----

**1**

###### 1. INTRODUCTION TO THE THEORY OF BOOLEAN FUNC- TIONS AND CIRCUITS

 1.1 Introduction

 Which of the following problems is easier to solve - the addition or the multiplication of two n-bit numbers ? In general, people feel that adds are easier to perform and indeed, people as well as our computers perform additions faster than multiplications. But this is not a satisfying answer to our question. Perhaps our multiplication method is not optimal. For a satisfying answer we have to present an algorithm for addition which is more efficient than any possible algorithm for multiplication. We are interested in efficient algorithms (leading to upper bounds on the complexity of the problem) and also in arguments that certain problems cannot be solved efficiently (leading to lower bounds). If upper and lower bound for a problem coincide then we know the complexity of the problem.

 Of course we have to agree on the measures of efficiency. Compar- ing two algorithms by examining the time someone spends on the two procedures is obviously not the right way. We only learn which algo- rithm is more adequat for the person in question at this time. Even different computers may lead to different results. We need fair crite- rions for the comparison of algorithms and problems. One criterion is usually not enough to take into account all the relevant aspects. For example, we have to understand that we are able to work only sequentially, i.e. one step at a time, while the hardware of computers has arbitrary degree of parallelism. Nowadays one even constructs parallel computers consisting of many processors. So we distinguish between sequential and parallel algorithms.

;
###### The problems we consider are Boolean functions f : 0 1 { }[n] →

;
###### 0 1 . There is no loss in generality if we encode all information by { }[m]

;
###### the binary alphabet 0 1 . But we point out that we investigate finite { }


-----

**2**

###### functions, the number of possible inputs as well as the number of pos- sible outputs is finite. Obviously, all these functions are computable. In 2 we introduce a rather general computation model, namely cir- § cuits. Circuits build a model for sequential computations as well as for parallel computations. Furthermore, this model is rather robust. For several other models we show that the complexity of Boolean functions in these models does not differ significantly from the circuit complexity. Considering circuits we do not take into account the spe- cific technical and organizational details of a computer. Instead of that, we concentrate on the essential subjects.

 The time we require for the computation of a particular function can be reduced in two entirely different ways, either using better com- puters or better algorithms. We like to determine the complexity of a function independently from the stage of the development of technol- ogy. We only mention a universal time bound for electronic computers.

:
###### For any basic step at least 5 6 10[−][33] seconds are needed (Simon (77)).
 ·

 Boolean functions and their complexity have been investigated since a long time, at least since Shannon’s (49) pioneering paper. The earlier papers of Shannon (38) and Riordan and Shannon (42) should also be cited. I tried to mention the most relevant papers on the com- plexity of Boolean functions. In particular, I attempted to present also results of papers written in Russian. Because of a lack of exchange several results have been discovered independently in both ˝parts of the world˝.

 There is large number of textbooks on ˝logical design˝ and ˝switch- ing circuits˝ like Caldwell (64), Edwards (73), Gumm and Pogun- tke (81), Hill and Peterson (81), Lee (78), Mendelson (82), Miller (79), Muroga (79), and Weyh (72). These books are essentially concerned with the minimization of Boolean functions in circuits with only two logical levels. We only deal with this problem in Ch. 2 briefly. The algebraical starting-point of Hotz (72) will not be continued here. We develop the theory of the complexity of Boolean functions in the sense of the book by Savage (76) and the survey papers by Fischer (74),


-----

**3**

###### Harper and Savage (73), Paterson (76), and Wegener (84 a). As al- most 60% of our more than 300 cited papers were published later than Savage’s book, many results are presented for the first time in a textbook. The fact that more than 40% of the relevant papers on the complexity of Boolean functions are published in the eighties is a statistical argument for the claim that the importance of this subject has increased during the last years.

 Most of the book is self-contained. Fundamental concepts of linear algebra, analysis, combinatorics, the theory of efficient algorithms (see Aho, Hopcroft and Ullman (74) or Knuth (81)) and the complexity theory (see Garey and Johnson (79) or Paul (78)) will be applied.

 1.2 Boolean functions, laws of computation, normal forms

 By Bn;m we denote the set of Boolean functions f : {0; 1}[n] → {0; 1}[m] . Bn also stands for Bn;1 . Furthermore we define the most important subclass of Bn;m, the class of monotone functions Mn;m . Again Mn = Mn;1 .

; : : : ; ; : : : ; ;

###### DEFINITION 2.1 : Let a = (a1 an), b = (b1 bn) ∈{0 1}[n] .
 We use the canonical ordering, i.e. a ≤ b iff ai ≤ bi for all i where 0 1 . A Boolean function is called monotone iff a b implies ≤ ≤ f(a) f(b) . ≤


###### For functions f ∈ Bn we have 2[n] different inputs, each of them can be mapped to 0 or 1 .

 PROPOSITION 2.1. : There exist 2[2][n] functions in Bn .


-----

**4**

###### Because of the large number of Boolean functions we avoid proofs by case inspection at least if n 3 . Since we use the 16 functions of ≥ B2 as basic operations, we discuss these functions. We have the two constant functions also denoted by 0 and 1 . Similarly, we use xi to denote not only a variable but also to denote the i -th projection. Two projections, x1 and x2, are contained in B2 as there are two negations, x1 and x2 (x = 1 iff x = 0) . The logical conjunction x ∧ y computes 1 iff x = y = 1, and the logical disjunction x y computes 1 iff x = 1 ∨

; ; ;
###### or y = 1 . Let x[1] = x and x[0] = x . For a b c 0 1 we get 8 ∈{ } different functions of type-, namely (x[a] y[b])[c] . Obviously x y = ∧ ∧ ∨

;
###### (x y) is of type- . The same holds for NAND(x y) = (x y) ¬ ∧ ∧ ¬ ∧

;
###### and NOR(x y) = (x y) = x y . The EXCLUSIVE - OR (XOR)- ¬ ∨ ∧ function also called parity is denoted by x y and computes 1 iff ⊕ exactly one of the variables equals 1 . The last 2 functions in B2 are XOR and its negation x y = (x y) called EQUIVALENCE. ≡ ¬ ⊕ ⊕ and are type- functions. We list some simple laws of computation. ≡ ⊕

;
###### PROPOSITION 2.2 : Let x y and z be Boolean variables.

 i) (Calculations with constants): x 0 = x, x 1 = 1, x 0 = 0, ∨ ∨ ∧ x 1 = x, x 0 = x, x 1 = x . ∧ ⊕ ⊕
 ii), and are associative and commutative. ∨ ∧ ⊕

; ; ;
###### iii) ( ), ( ) and ( ) are distributive, e.g. x (y z) = ∨ ∧ ∧ ∨ ⊕ ∧ ∧ ⊕ (x y) (x z) . ∧ ⊕ ∧
 iv) (Laws of simplification): x x = x, x x = 1, x x = x, x x = 0, ∨ ∨ ∧ ∧ x x = 0, x x = 1, x (x y) = x, x (x y) = x . ⊕ ⊕ ∨ ∧ ∧ ∨
 v) (Laws of deMorgan): (x y) = x y, (x y) = x y . ¬ ∨ ∧ ¬ ∧ ∨

 These laws of computation remain correct if we replace Boolean variables by Boolean functions. By induction we may generalize the

; ; ;
###### laws of deMorgan to n variables. We remark that ( 0 1 ) is the { } ⊕ ∧

Z
###### Galois field 2 . Instead of x ∧ y we often write only xy . In case of doubt we perform conjunctions at first, so x y z stands for (x y) z . ∧ ∨ ∧ ∨


-----

**5**

###### Similarly to the iterated sum Σ and the iterated product Π, we use �, and for iterated,, . ∧ ∨ ⊕ � �
 Before presenting computation models for Boolean functions we want to discuss how we can define and describe Boolean functions. Because we consider finite functions f ∈ Bn;m we can describe them by a complete table x → f(x) whose length is 2[n] . If f ∈ Bn it is sufficient to specify f[−][1](1) or f[−][1](0) . In general it is easier to describe a function by its behavior, e.g. f ∈ Bn computes 1 iff the number of ones in the input is larger than the number of zeros.

 As a second step we describe Boolean functions by Boolean opera- tions. The disjunctive and conjunctive normal form (DNF and CNF) are based on f[−][1](1) and f[−][1](0) resp.

; : : : ;
###### DEFINITION 2.2 : The minterm ma for a = (a(1) a(n)) ∈

;
###### {0 1}[n] is defined by ma(x) = x[a(1)]1 ∧· · · ∧ x[a(n)]n .
 The appropriate maxterm is sa(x) = x[¬]1 [a(1)] ∨· · · ∨ x[¬]n [a(n)] .


###### THEOREM 2.1 : f(x) = � ma(x) = � sb(x) .

a f[−][1](1) b f[−][1](0)
_∈_ _∈_

###### The first and second representation are called disjunctive and conjunc- tive normal form resp. (DNF and CNF).

 Proof : By definition, ma(x) = 1 iff x = a and sa(x) = 0 iff x = a . f(x) equals 1 iff x ∈ f[−][1](1) iff one of the minterms ma(x) for a ∈ f[−][1](1) computes 1 . Similar arguments work for the CNF of f . 2

 Since (f g)[−][1](1) = f[−][1](1) g[−][1](1) and (f g)[−][1](1) = f[−][1](1) g[−][1](1), ∧ ∩ ∨ ∪ it is easy to compute the DNF (or CNF) of f g or f g . Both rep- ∧ ∨ resentations are not convenient for the solution of Boolean equations.

; ;
###### We are not able to subtract terms, because neither ( 0 1 ) nor { } ∧

; ; ; ;
###### ( 0 1 ) is a group as ( 0 1 ) is. { } ∨ { } ⊕


-----

**6**

###### THEOREM 2.2 : (Ring sum expansion (RSE) of f) For each Boolean function f ∈ Bn there is exactly one 0-1-vector a = (aA)A⊆{1;:::;n} [such that]


###### � f(x) = aA ∧ [�] xi

A⊆{1;:::;n} i∈A


:
###### (2.1)


###### Proof : The existence of the vector a is proved constructively. We start with the CNF of f . Using the laws of deMorgan, we replace dis- junctions by conjunctions and negations, in particular, the maxterm sb(x) is replaced by ¬(x[b(1)]1 ∧· · · ∧ x[b(n)]n ) . Afterwards we replace nega- tions x by x 1 . Since we obtain a representation of f by and, ⊕ ∧ ⊕ we may apply the law of distributivity to get a -sum of -products ⊕ ∧ and constants. Since t ⊕ t = 0, we set aA = 1 iff the number of terms � xi(i ∈ A) in our sum is odd.
 For different functions f and g we obviously require different vectors a(f) and a(g) . Since the number of different vectors a = (aA)A 1;:::;n
_⊆{_ _}_
###### equals the number of functions f ∈ Bn, there cannot be two different vectors a and a[′] for f . 2

 The RSE of f is appropriate for the solution of Boolean equations. Since t t = 0, we may subtract t by -adding t . ⊕ ⊕

 1.3 Circuits and complexity measures

 We may use the normal forms of 2 for the computation of Boolean § functions. But intuitively simple functions may have exponential length for all normal forms. Consider for example f ∈ Bn where f(x) = 1 iff x1 + · · · + xn ≡ 0 mod 3 .
 In order to develop an appropriate computation model we try to simulate the way in which we perform calculations with long numbers.


-----

**7**

###### We only use a small set of well-known operations, the addition of dig- its, the application of multiplication tables, comparison of digits, and if - tests. All our calculations are based on these basic operations only. Here we choose a finite set Ωof one - output Boolean functions as ba
; : : : ;

###### sis. Inputs of our calculations are the variables x1 xn and w.l.o.g.
 also the constants 0 and 1 . We do neither distinguish between con- stants and constant functions nor between variables and projections x → xi . One computation step is the application of one of the ba- sic operations ω Ωto some inputs and/or already computed data. ∈ In the following we give a correct description of such a computation called circuit.


###### DEFINITION 3.1 : An Ω-circuit works for a fixed number n of

; : : : ;

###### Boolean input variables x1 xn . It consists of a finite number b

; : : : ;
###### of gates G(1) G(b) . Gate G(i) is defined by its type ω i ∈ Ω

; : : : ;
###### and, if ω i Bn(i), some n(i)-tuple (P(1) P(n(i))) of predecessors. ∈

; ; ; : : : ; ; ; : : : ;
###### P(j) may be some element from {0 1 x1 xn G(1) G(i − 1)} .
 By res G(i) we denote the Boolean function computed at G(i) . res is defined inductively. For an input I res I is equal to I .

; ; : : : ;

###### If G(i) = (ω i P(1) P(n(i))),

; : : : ; :
###### res G(i)(x) = ω i(res P(1)(x) res P(n(i))(x)) (3.1)


; : : : ;

###### Finally the output vector y = (y1 ym), where yi is some input or
 gate, describes what the circuit computes, namely f ∈ Bn;m, where

; : : : ;

###### f = (f1 fm) and f i is the function computed at yi .

 It is often convenient to use the representation of a circuit by a directed acyclic graph. The inputs are the sources of the graph, the vertex for the gate G(i) is labelled by the type ω i of G(i) and has n(i) numbered incoming edges from the predecessors of G(i) . If ω i is commutative, we may withdraw the numbering of edges.

 Our definition will be illustrated by a circuit for a fulladder

; ; ; ;

###### f(x1 x2 x3) = (y1 y0) . Here (y1 y0) is the binary representation of


-----

**8**

###### x1 +x2 +x3, i.e. x1 +x2 +x3 = y0 +2 y1 . We design a B2-circuit in the following way. y1, the carry bit, equals 1 iff x1 + x2 + x3 is at least 2, and y0, the sum bit, equals 1 iff x1 + x2 + x3 is odd. In particular, y0 = x1 x2 x3 can be computed by 2 gates. Since x1 x2 is already ⊕ ⊕ ⊕ computed, it is efficient to use this result for y1 . It is easy to check that

:
###### y1 = [(x1 ⊕ x2) ∧ x3] ∨ [x1 ∧ x2] (3.2)

 We obtain the following circuit where all edges are directed top - down.

; ; ; ; ; ;
###### G1 = (⊕ x1 x2) G2 = (⊕ G1 x3) G3 = (∧ x1 x2)

; ; ; ; ; ;
###### G4 = (∧ G1 x3) G5 = (∨ G3 G4) (y1 y0) = (G5 G2)

 x1 x2 x3

 G3 ∧ ⊕ G1

 ∧ G4

 ∨ G5 = y1 ⊕ G2

 Fig. 3.1

 In the following we define circuits in a more informal way.

 Many circuits are computing the same function. So we look for optimal circuits, i.e. we need criterions to compare the efficiency of circuits. If a circuit is used for a sequential computation the number of gates measures the time for the computation. In order to ease the discussion we assume that the necessary time is for all basic op- erations the same. Circuits (or chips) in the hardware of computers


-----

**9**

###### have arbitrary degree of parallelism. In our example G1 and G3 may be evaluated in parallel at the same time, afterwards the inputs of G2 and G4 are computed and we may evaluate these two gates in parallel, and finally G5 . We need only 3 instead of 5 computation steps.

 DEFINITION 3.2 : The size or complexity C(S) of a circuit S equals the number of its gates. The circuit complexity of f with respect to the basis Ω, CΩ(f), is the smallest number of gates in an Ω-circuit computing f . The depth D(S) of S is the length (number of gates) of the longest path in S . The depth of f with respect to Ω, DΩ(f), is the minimal depth of an Ω-circuit computing f .

 For sequential computations the circuit complexity (or briefly just complexity) corresponds to the computation time. In Ch. 9 we derive connections between depth and storage space for sequential computations. For parallel computations the size measures the cost for the construction of the circuit, and depth corresponds to computation time. In either case we should try to minimize simultaneously size and depth. It does not seem to be possible to realize this for all functions (see Ch. 7).

 We want to show that the circuit model is robust. The complexity measures do not really depend on the underlying basis if the basis is large enough. In 4 we show that the complexity of functions does § not increase significantly by the necessary (from the technical point of view) restrictions on the number of edges (or wires) leaving a gate.

 DEFINITION 3.3 : A basis Ωis complete if any Boolean function can be computed in an Ω-circuit.

; ; ;
###### The normal forms in 2 have shown that and § {∧ ∨ ¬} {⊕ ∧} are complete bases. By the laws of deMorgan even the smaller bases

; ; ;
###### and are complete, whereas is incomplete. Com- {∧ ¬} {∨ ¬} {∧ ∨} plexity and depth of Boolean functions can increase only by a constant


-----

**10**

###### factor if we switch from one complete basis to another. Therefore we may restrict ourselves to the basis B2 and denote by C(f) and D(f) the circuit complexity and depth resp. of f with respect to B2 . In Ch. 6 we prove that C ; (f)=C(f) can become arbitrarily large for
_{∧_ _∨}_

;
###### functions computable over . {∧ ∨}

 THEOREM 3.1 : Let Ωand Ω[′] be complete bases, c = max{CΩ(g) | g ∈ Ω[′]} and d = max{DΩ(g) | g ∈ Ω[′]} . Then CΩ(f) ≤ c CΩ[′](f) and DΩ(f) ≤ d DΩ[′](f) for all f ∈ Bn .

 Proof : We make use of the idea that subcircuits may be replaced by equivalent subcircuits. Here we replace gates for g Ω[′], which are ∈ small subcircuits, by optimal (with respect to size or depth) Ω-circuits for g . Starting with an Ω[′] - circuit computing f we obtain an Ω-circuit with the required properties. 2

 1.4 Circuits with bounded fan - out

 From the technical point of view it may be necessary to bound the fan-out of gates by some constant s, i.e. the result of a gate may be used only s times. The appropriate complexity measures are denoted by Cs;Ω and Ds;Ω . By definition


###### CΩ ≤· · · ≤ Cs+1;Ω ≤ Cs;Ω ≤· · · ≤ C1;Ω


:
###### (4.1)


###### Any function computable by an Ω-circuit may be computed by an Ω- circuit with fan-out 1 . This can be proved by induction on c = CΩ(f) .

            ###### Nothing has to be proved for c = 0 . For c 0 we consider an Ω-circuit

; : : : ;

###### for f with c gates. Let g1 gr be the functions computed at the

<
###### predecessors of the last gate. Since CΩ(gi) c, gi can be computed by an Ω-circuit with fan-out 1 . We take disjoint Ω-circuits with fan
; : : : ;

###### out 1 for g1 gr and combine them to an Ω-circuit with fan-out 1


-----

**11**

###### for f . The depth of the new circuit is not larger than that of the old one, thus DΩ(f) = Ds;Ω(f) for all s . In future we do not investigate Ds;Ω anymore. With the above procedure the size of the circuit may increase rapidly. For s 2, we can bound the increase of size by ≥ the following algorithm of Johnson, Savage and Welch (72). We also bound the fan-out of the variables by s .

               ###### If some gate G (or some variable) has fan-out r s we use s 1 − outgoing wires in the same way as before and the last outgoing wire to save the information of G . We build a subcircuit in which again res G is computed. We still have to simulate r − (s − 1) outgoing wires of G. If s 2, the number of unsimulated wires decreases with each ≥ step by s 1 . How can we save the information of gate G ? By − computing the identity x x . Let l (Ω) be the smallest number of → gates in order to compute a function g = res G at some gate given g

;
###### as input. We claim that l (Ω) 1 2 . Let ω Ωbe a nonconstant ∈{ } ∈ basic operation. Let ω ∈ Bm . Since ω is not constant, input vectors exist differing only at one position (w.l.o.g. the last one) such that

; : : : ; ; ; : : : ; ;

###### ω(a1 am 1 1) = ω(a1 am 1 0) . We need only one wire out

_−_ _̸_ _−_

; : : : ; ;

###### of G to compute ω(a1 am−1 res G) which equals res G, implying
 l (Ω) = 1, or ¬ res G . In the second case we repeat the procedure and compute ¬ (¬ res G) = res G implying l (Ω) = 2 . At the end we obtain a circuit for f in which the fan-out is bounded by s .

 THEOREM 4.1 : Let k be the fan-in of the basis Ω, i.e. the largest number of inputs for a function of Ω. If f ∈ Bn may be computed by an Ω-circuit and if s 2 then ≥

 Cs;Ω(f) ≤ (1 + l (Ω)(k − 1)=(s − 1)) CΩ(f): (4.2)

 Proof : If the fan-out of some gate is large, we need many gates of fan-out s for the simulation of this gate. But the average fan-out of the gates cannot be large. Since the fan-in is bounded by k the average fan-out cannot be larger than k . We explain these ideas in detail.


-----

**12**

###### Let r be the fan-out of some gate or variable. If p 0 is the ≥ smallest number such that s + p(s 1) r, then it is sufficient to − ≥ save the information of the gate p times. For this, l (Ω) p gates are sufficient. With the definition of p we conclude that

< :
###### s + (p 1)(s 1) r if r 1 (4.3) − − ≥

=
###### Therefore p is bounded by (r 1) (s 1) if r 1 . In an optimal − − ≥ circuit for f ∈ Bn at most n − 1 variables and at most one gate have fan-out 0 . Let c = CΩ(f) and let ri be the fan-out of the i -th gate and rj+c the fan-out of xj . We have to sum up all ri 1 where ri 1 . − ≥ The sum of all ri (where ri 1) equals the number of wires. Since the ≥ fan-in of the basis is k, the number of wires is bounded by ck . As at most n parameters ri are equal to 0 the sum of all ri 1 where ri 1 − ≥ is not larger than ck c . Thus the number of new gates is bounded −

=
###### by l (Ω)(ck c) (s 1) . Altogether we proved that − −

 Cs;Ω(f) ≤ c + c l (Ω)(k − 1)=(s − 1) (4.4)

= :
###### = (1 + l (Ω)(k − 1) (s − 1)) CΩ(f)

 2

 For each basis Ωthe number of gates is increased by a constant factor only. l (Ω) = 1 and k = 2, if Ω= B2 . For all s ≥ 2 we only have to double the number of gates. For s = 1 our algorithm does not work. The situation for s = 1 indeed is essentially different. In Ch. 8 we present examples in which C1;Ω(f)=CΩ(f) becomes arbitrarily large.

 DEFINITION 4.1 : The circuits whose fan-out of gates is bounded by 1 are called (Boolean) formulas. LΩ(f) = C1;Ω(f) is called the formula size of f .

 We have motivated circuits with bounded fan-out by technical re- strictions. These restrictions are not so strong that the fan-out is restricted to 1 . Nevertheless we investigate Boolean formulas in Ch. 7 and 8. One reason for this is that we obtain a strong connection be

-----

**13**

###### tween formula size and depth (see Ch. 7). Another reason is that Boolean formulas correspond to those expressions we usually call for- mulas. Given a formula we may also bound the fan-out of the inputs by 1 by using many copies of the inputs. From our graph representa- tion we obtain a tree where the root is the last gate. Basically this is the representation of arithmetical expressions by trees.

 We could be satisfied. Bounding the fan-out does not increase the depth of the circuit and the size has to be increased only by a small constant factor, if s 2 . But with both algorithms discussed we ≥ cannot bound the increase of size and depth simultaneously. This was achieved at first by an algorithm of Hoover, Klawe and Pippenger (84). Size and depth will increase only by a constant factor. Perhaps the breadth is still increasing (see Schnorr (77) for a discussion of the importance of breadth).

 We present the algorithm only for the case l (Ω) = 1 . We saw that p identity gates are sufficient to simulate a gate of fan-out r where p is the smallest integer such that r s + p(s 1) . For s = 3 we ≤ − show in Fig. 4.1 a how Johnson, Savage and Welch replaced a gate of fan-out 12 . In general, we obtain a tree consisting of a chain of p + 1 nodes whose fan-out is bounded by s . Any other tree with p+1 nodes, r leaves and fan-out bounded by s (as shown in Fig. 4.1 b) will also do the job. The root is the gate that has to be simulated, and the other p nodes are identity gates. The r outgoing wires can be used to simulate the r outgoing wires of the gate we simulate. The number of gates behaves as in the algorithm of Johnson et al. We have some influence on the increase in depth of the circuit by choosing appropriate trees.

; : : : ;

###### In a given circuit S with b gates G1 Gb we work bottom-up.
 Let Sb = S . We construct Si−1 from Si by replacing gate Gi by an appropriate tree. Then S[′] = S0 is a circuit of fan-out s equivalent to S . The best thing we could do in each step is to replace Gi by a tree Ti such that the longest path in Si−1, starting at the root of Ti, is kept as short as possible. In the following we describe an efficient algorithm for the choice of Ti .


-----

**14**

###### a) b) Fig. 4.1

 We define a weight function on the nodes of all trees T with r leaves, fan-out bounded by s and p + 1 inner nodes. Here r is the fan-out of Gi and p is the proper parameter. Let S(T) be the circuit produced by the replacement of Gi by T in Si . Then the weight of a node u T should be the length of the longest path in S(T) starting ∈ in u . The weight of the r leaves of T is given and the weight of the inner nodes is recursively defined by

:
###### w(u) = 1 + max w(u[′]) u[′] is son of u (4.5) { | }

 In order to choose a tree whose root has minimal weight, we use a so-called Huffman algorithm (for a discussion of this class of al- gorithms see Ahlswede and Wegener (86), Glassey and Karp (72) or Picard (65)).

 It is easier to handle trees where all inner nodes have fan-out ex- actly s. For that reason we add s + p(s 1) r dummy leaves whose − − weight is . Altogether we now have exactly s + p(s 1) leaves. −∞ −

 ALGORITHM 4.1 : Input : V, a set of s + p(s 1) nodes, and a weight function w on V . − Output : T a tree with p + 1 inner nodes of fan-out s . The leaves correspond uniquely to the nodes in V .


-----

**15**

               ###### Let W = V . If W = 1, T is constructed. While W 1, we choose | | | |

; : : : ;

###### those s nodes v1 vs ∈ W which have the smallest weight. These
 nodes become the sons of a new node v[′] whose weight is defined by

; : : : ;

###### (4.5). We remove v1 vs from W and add v[′] to W .


###### We would stray too much from the subject, if we presented those results on Huffman algorithms which lead to the following estimation of the depth of S[′] . For the size of S[′] we obtain the same bound as in Theorem 4.1.

 THEOREM 4.2 : Let S be an Ω-circuit with one output and let k be the fan-in of Ω. For s 2, we can efficiently construct an equivalent ≥ circuit S[′] whose fan-out is bounded by s such that

=
###### C(S[′]) (1 + l (Ω)(k 1) (s 1)) C(S) (4.6) ≤ − −

 and

:
###### D(S[′]) ≤ (1 + l (Ω) log s k) D(S) (4.7)

 In 5 we summarize the conclusions drawn from the results of 3 § § and 4. §

 1.5 Discussion

 It turned out that circuits build an excellent model for the compu- tation of Boolean functions. Certainly circuit complexity and depth of a Boolean function cannot be measured unambigously. These com- plexity measures depend on

 – the costs and the computation time of the different types of gates

 – the underlying basis and


-----

**16**

###### – the fan-out restriction.

 This effect is unpleasant. How can we find out whether f is eas- ier than g ? The results of 3 and 4 showed that the effect of § § the above mentioned criterions on circuit complexity and depth of a Boolean function can be estimated by a constant factor (with the only exceptions of incomplete bases and the fan-out restriction 1). If we ignore constant factors, we can limit ourselves to a fixed circuit model. The basis is B2, all gates cause the same cost, and the fan-out is not restricted. Comparing two functions f and g not only C(f) and C(g) but also D(f) and D(g) differ ˝by a constant factor˝. In fact we do not consider some definite function f but natural sequences of functions fn . Instead of the addition of two 7-bit numbers, a function f ∈ B14;8, we investigate the sequence of functions fn B2n;n+1 where fn is the ∈ addition of two n-bit numbers.

 Let (fn) and (gn) be sequences of functions. If C(fn) = 11 n and

=
###### C(gn) = n[2], C(fn) ≤ C(gn) for n ≤ 11 but C(fn) C(gn) is bounded by 11 and converges to 0 . We state that (gn) is more complex than (fn), since for all circuit models the quotient of the complexity of fn and the complexity of gn converges to 0 . We ignore that gn may be computed more efficiently than fn for small n. We are more interested in the asymptotic behavior of C(fn) and C(gn) .
 Certainly, it would be best to know C(fn) exactly. If it is too difficult to achieve this knowledge, then, in general, the asymptotic behavior describes the complexity of fn quite good. Sometimes the concentration on asymptotics may lead to absurd results.

=
###### If C(fn) = 15 n[34816] and C(gn) = 2[n][=][100], C(fn) C(gn) converges to 0, but for all relevant n the complexity of fn is larger than the complexity of gn . But this is an unrealistic example that probably would not occur. In the following we introduce the ˝big-oh˝ notation.


-----

**17**

; N R ;                       ###### DEFINITION 5.1 : Let f g : such that f(n) g(n) 0 for → large n .

=
###### i) f = O(g) (f does not grow faster than g) if f(n) g(n) c for some ≤ constant c and large n .

 ii) f = Ω(g) if g = O(f) .

 iii) f = Θ(g) (f and g have the same asymptotic behavior) if f = O(g) and g = O(f) .

=
###### iv) f = o(g) (f grows slower than g) if f(n) g(n) tends to 0 .

 v) f = ω(g) if g = o(f) .

 vi) f grows polynomially if f = O(p) for some polynomial p . Notation: f = n[O(1)] .

              ###### vii) f grows exponentially if f = Ω(2[n][ε]) for some ε 0 .

 We try to estimate C(fn) and C(gn) as accurately as possible. Often we have to be satisfied with assertions like the following. The number of gates of the circuits Sn for fn has the same asymptotic behavior as n, n log n, n[2], n[3] or even 2[n] . We want to emphasize the structural difference of algorithms with n, n log n, n[2], n[3] or 2[n] computation steps. In Table 5.1 we compute the maximal input size of a problem which can be solved in a given time if one computation step can be

:
###### performed within 0 001 seconds. The reader should extend this table by multiplying the running times T(n) by factors not too large and by adding numbers not too large.

 The next table shows how much we gain if we perform 10 compu- tation steps in the same time as we did 1 computation step before. Constant factors for T(n) do not play any role in this table.

 For the polynomially growing functions the maximal possible input length is increased by a constant factor which depends on the degree of the polynomial. But for exponentially growing functions the maximal possible input length is only increased by an additive term. There- fore functions whose circuit size is polynomially bounded are called efficiently computable while the other functions are called intractable.


-----

**18**

###### T(n) Maximal input length which can be processed within
 1 sec. 1 min. 1 h.

 n 1 000 60 000 3 600 000
 n log2 n 140 4 893 200 000
 n[2] 31 244 1 897
 n[3] 10 39 153
 2[n] 9 15 21

 Tab. 5.1

 T(n) Maximal input length which Remarks
 can be processed before afterwards

 n m 10 m
 n log n m (nearly) 10 m

: :
###### n[2] m 3 16 m 10 3 16[2] ≈

: :
###### n[3] m 2 15 m 10 2 15[3] ≈

:
###### 2[n] m m + 3 3 10 2[3][:][3] ≈

 Tab. 5.2

 This notation is based on the experience that algorithms whose run- ning time is a polynomial of very large degree or whose running time is of size 2[n][ε] for a very small ε are exceptions.

|T(n)|Maximal input length which can be processed within 1 sec. 1 min. 1 h.|
|---|---|
|n n log n 2 n2 n3 2n|1 000 60 000 3 600 000 140 4 893 200 000 31 244 1 897 10 39 153 9 15 21|

|T(n)|Maximal input length which can be processed before afterwards|Remarks|
|---|---|---|
|n n log n n2 n3 2n|m 10 m m (nearly) 10 m m 3 16 m : m 2 15 m : m m + 3 3 :|10 3 162 ≈ : 10 2 153 ≈ : 10 233 ≈ :|


-----

**19**

###### At the end of our discussion we refer to a property distinguishing circuits and programs for computers. A program for the sorting prob- lem or the multiplication of matrices or any other reasonable problem should work for instances of arbitrary length. A circuit can work only for inputs of a given length. For problems like the ones men- tioned above, we have to construct sequences of circuits Sn such that Sn solves the problem for instances of length n. The design of Sn and the design of Sm are independent if n ̸= m . Therefore we say that cir- cuits build a non uniform computation model while software models like Turing machines build a uniform model. Non uniform models are adequate for the hardware of computers. Designing circuits we do not have if-tests to our disposal, but we can do different things for dif- ferent input lengths. Hence it happens that any sequence of Boolean functions fn Bn may be computed by (a sequence of) circuits while ∈ not all sequences fn Bn can be computed by a computer or a Turing ∈ machine. Furthermore, it is not astonishing that Turing machine pro- grams may be simulated efficiently by circuits (see Ch. 9). Because of our way of thinking most of the sequences of circuits we design may be described uniformly and therefore can be simulated efficiently by Turing machines.

 EXERCISES

 1. What is the cardinality of Bn;m?

; ; ;

###### 2. Let f(x1 x2 x3) = (y1 y0) be the fulladder of § 3. y1 is monotone

;
###### but y0 is not. Design an {∧ ∨}-circuit for y1 .


###### 3. f is called non degenerated if f depends essentially on all its vari- ables, i.e. the subfunctions of f for xi = 0 and xi = 1 are different. Let Nk be the number of non degenerated functions f ∈ Bk and N0 = 2 .


-----

**20**


###### � Then

0 k n
_≤_ _≤_


###### �n�
k Nk = |Bn| .


###### 4. The fraction of degenerated functions f ∈ Bn tends to 0 as n →∞ .

 5. How many functions have the property that we cannot obtain a constant subfunction even if we replace n 1 variables by con- − stants ?

;
###### 6. Let f g ∈ Mn, t = x1 · · · xn, t[′] = x1 ∨· · · ∨ xn .
 a) t f g t f or t g . ≤ ∨ ⇒ ≤ ≤
 b) f g t[′] f t[′] or g t[′] . ∧ ≤ ⇒ ≤ ≤

;
###### 7. Let different functions f g ∈ Bn be given by their RSE. How can one construct an input a where f(a) = g(a) without testing all ̸ inputs ?

 8. Design circuits of small size or depth for the following functions :


###### a) fn(x1


; : : : ;
###### xn


; : : : ; ; ; : : : ;

###### a) fn(x1 xn y1 yn) = 1 iff xi = yi for all i .
 ̸
 b) fn(x0 ; : : : ; xn−1 ; y0 ; : : : ; yn−1) = 1 iff � xi 2[i] > � yi 2[i] .

0 i n 1 0 i n 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_

; : : : ;

###### c) fn(x1 xn) = 1 iff x1 + · · · + xn ≥ 2 .


###### 9. Which functions f ∈ B2 build a complete basis of one function ?

 10. Which of the following bases are complete even if the constants are not given for free ?

; ; ;
###### a), b), c) . {∧ ¬} {∨ ¬} {⊕ ∧}

; ; ; ;
###### 11. sel ∈ B3 is defined by sel(x y z) = y, if x = 0, and sel(x y z) = z, if x = 1 . Is sel a complete basis ? { }


-----

**21**

;
###### 12. Each function computed by an -circuit is monotone. {∧ ∨}

;
###### 13. Let Ω Ω[′] be complete bases. Define constants c and d such that each Ω[′]-circuit S[′] can be simulated by an Ω-circuit S such that C(S) c C(S[′]) and D(S) d D(S[′]) . ≤ ≤

 14. Compute l ({f}) (see § 4) for each nonconstant f ∈ B2 .

 15. Construct a sequence of graphs Gn such that the algorithm of Johnson et al. constructs graphs G′n [whose depth d(G]′n[) grows] faster than c d(Gn) for any constant c if s = 2 .

 16. Specify for the following functions ˝easy˝ functions with the same asymptotic behavior.

=

###### a) n[2] (n log[3] n)
 −


###### � b) log i

1 i n
_≤_ _≤_

###### c) � i[−][1]

1 i n
_≤_ _≤_

###### � d) i 2[−][i] .

1 i n
_≤_ _≤_

        ###### 17. log n = o(n[ε]) for all ε 0 .

 18. n[log n] does not grow polynomially and also not exponentially.

 19. If f grows polynomially, there exists a constant k such that f(n) n[k] + k for all n . ≤


-----

**22**

###### 2. THE MINIMIZATION OF BOOLEAN FUNCTIONS

 2.1 Basic definitions

 How can we design good circuits ? If we consider specific functions like addition or multiplication we take advantage of our knowledge about the structure of the function (see Ch. 3). Here we treat the design of circuits for rather structureless functions. Unfortunately, this situation is not unrealistic, in particular for the hardware construction of computers. The inputs of such a Boolean function f ∈ Bn;m may be the outputs of another Boolean function g ∈ Bk;n . The properties of f are described by a table x f(x) . Since the image of g may be →

; ;
###### a proper subset of 0 1, f is not always defined for all a 0 1 . { }[n] ∈{ }[n] Such Boolean functions are called partially defined.

 DEFINITION 1.1 : A partially defined Boolean function is a func
; ; ;
###### tion f : {0 1}[n] →{0 1 ? } . B[∗]n [is the set of all partially defined] Boolean functions on n variables. A circuit computes f ∈ B[∗]n [at gate G iff f(x) = res][G][(x) for all]

;
###### x f[−][1]( 0 1 ). ∈ { }

;
###### Since inputs outside of f[−][1]( 0 1 ) are not possible (or just not { } expected ?!), it does not matter which output a circuit produces for inputs a ∈ f[−][1](?) . Since Bn ⊆ B[∗]n [, all our considerations are valid also] for completely defined Boolean functions. We assume that f is given by a table of length N = 2[n] . We are looking for efficient procedures for the construction of good circuits. The running time of these algorithms has to be measured in terms of their input size, namely N, the length of the table, and not n, the length of the inputs of f .


-----

**23**

###### The knowledge of circuits, especially of efficient circuits for an ar- bitrary function is far away from the knowledge that is required to design always efficient circuits. Therefore one has restricted oneself to a subclass of circuits. The term ˝minimization of a Boolean function˝ stands for the design of an optimal circuit in the class of Σ2-circuits (for generalizations of the concept of Σ2-circuits see Ch. 11). Inputs

; ; : : : ; ;

###### of Σ2-circuits are all literals x1 x1 xn xn . In the first step we may
 compute arbitrary conjunctions (products) of literals. In the second step we compute the disjunction (sum) of all terms computed in the first step. We obtain a sum-of-products for f which also is called poly- nomial for f . The DNF of f is an example of a polynomial for f . Here we look for minimal polynomials, i.e. polynomials of minimal cost.

 From the practical point of view polynomials have the advantage that there are only two logical levels needed, the level of disjunctions is following the level of conjunctions.

 DEFINITION 1.2 :

 i) A monom m is a product (conjunction) of some literals. The cost of m is equal to the number of literals of m .

 ii) A polynomial p is a sum (disjunction) of monoms. The cost of p is equal to the sum of the costs of all m which are summed up by p .
 iii) A polynomial p computes f ∈ B[∗]n [if p(x) = f(x) for x][ ∈] [f][−][1][(][{][0][;][ 1][}][) .] p is a minimal polynomial for f, if p computes f and no polynomial computing f has smaller cost than p .

 Sometimes the cost of a polynomial p is defined as the number of monoms summed up by p . By both cost measures the cost of the circuit belonging to p is approximately reflected. On the one hand we need at least one gate for the computation of a monom, and on the other hand l gates are sufficient to compute a monom of length l and to add it to the other monoms. Since different monoms may share the same submonom we may save gates by computing these submonoms only once. The following considerations apply to both cost measures.


-----

**24**

###### Let p = m1 mk be a polynomial for f . mi(a) = 1 implies ∨· · · ∨

;
###### p(a) = 1 and f(a) ∈{1 ?} . If m[−]i [1][(1)][ ⊆] [f][−][1][(?), we could cancel m][i] and would obtain a cheaper polynomial for f .

 DEFINITION 1.3 : A monom m is an implicant of f if m[−][1](1) ⊆

;
###### f[−][1]( 1 ? ) and m[−][1](1) f[−][1](?) . I(f) is the set of all implicants of f . { } ̸⊆

 We have already seen that minimal polynomials consist of impli- cants only. Obviously the sum of all implicants computes f . If m and m[′] are implicants, but m is a proper submonom of m[′], m m[′] = m by ∨ the law of simplification, and we may cancel m[′] .

 DEFINITION 1.4 : An implicant m I(f) is called prime implicant ∈ if no proper submonom of m is an implicant of f . PI(f) is the set of all prime implicants of f .

 To sum up we have proved

 THEOREM 1.1 : Minimal polynomials for f consist only of prime implicants.

 All algorithms for the minimization of Boolean functions start with the computation of all prime implicants. Afterwards PI(f) is used to construct a minimal polynomial. It is not known whether one may compute efficiently minimal polynomials without computing implicitly PI(f) .


-----

**25**

###### 2.2 The computation of all prime implicants and reductions of the table of prime implicants

 The set of prime implicants PI(f) may be computed quite efficiently by the so-called Quine and McCluskey algorithm (McCluskey (56), Quine (52) and (55)). It is sufficient to present the algorithm for completely defined Boolean functions f ∈ Bn . The easy generalization to partially defined Boolean functions is left to the reader. Since f is given by its table x f(x) implicants of length n can be found directly. → For each a ∈ f[−][1](1) the corresponding minterm ma is an implicant. It is sufficient to know how all implicants of length i 1 can be computed − if one knows all implicants of length i .

 LEMMA 2.1 : Let m be a monom not containing xj or xj . m is an implicant of f iff m xj and m xj are implicants of f .

 Proof : If m ∈ I(f), we can conclude m xj(a) = 1 ⇒ m(a) = 1 ⇒ f(a) = 1, hence m xj I(f) . Similarly m xj I(f) . If m xj, m xj I(f), ∈ ∈ ∈ we can conclude m(a) = 1 ⇒ m xj(a) = 1 or m xj(a) = 1 ⇒ f(a) = 1, hence m I(f) . 2 ∈

 ALGORITHM 2.1 (Quine and McCluskey) :

;
###### Input : The table (a f(a)) of some f ∈ Bn .
 Output : The nonempty sets Qk and Pk of all implicants and prime implicants resp. of f with length k . In particular PI(f) is the union of all Pk . Qn is the set of all minterms ma such that f(a) = 1, i = n . While Qi ̸= ̸◦

 i := i 1 ; −

;

###### Qi := {m | ∃ j : xj, xj are not in m but m xj m xj ∈ Qi+1 } ;
 Pi+1 := {m ∈ Qi+1 | ∀ m[′] ∈ Qi : m[′] is not a proper sub- monom of m . }


-----

**26**

###### By Lemma 2.1 the sets Qk are computed correctly. Also the sets of prime implicants Pk are computed correctly. If an implicant of length k has no proper shortening of length k 1 which is an implicant, then − it has no proper shortening which is an implicant and therefore it is a prime implicant. In order to obtain an efficient implementation of Al- gorithm 2.1 we should make sure that Qi does not contain any monom twice. During the construction of Qi it is not necessary to test for all

;

###### pairs (m[′] m[′′]) of monoms in Qi+1 whether m[′] = m xj and m[′′] = m xj for

;

###### some j . It is sufficient to consider pairs (m[′] m[′′]) where the number of
 negated variables in m[′′] is by 1 larger than the corresponding number in m[′] . Let Qi+1;l be the set of m ∈ Qi+1 with l negated variables. For m[′] ∈ Qi+1;l and all negated variables xj in m[′] it is sufficient to test whether the monom m[′]j [where we have replaced x][j][ in m][′][ by x][j][ is in] Qi+1;l −1 . Finally we should mark all m ∈ Qi+1 which have shortenings in Qi . Then Pi+1 is the set of unmarked monoms m ∈ Qi+1 .


###### We are content with a rough estimation of the running time of the Quine and McCluskey algorithm. The number of different monoms is 3[n] . For each j either xj is in m or xj is in m or both are not in m . Each monom is compared with at most n other monoms. By binary search according to the lexicographical order O(n) comparisons are sufficient to test whether m is already contained in the appropriate Qi;l . This search has to be carried out not more than two times for each of the at most n 3[n] tests. So the running time of the algorithm is bounded by O(n[2] 3[n]) . The input length is N = 2[n] . Using the abbreviation log for log2 we have estimated the running time by O(N[log 3] log[2] N) . Mileto and Putzolu (64) and (65) investigated the average running time of the algorithm for randomly chosen Boolean functions.

 The relevant data on f is now represented by the table of prime implicants.


-----

**27**

###### DEFINITION 2.1 : The table of prime implicants (PI-table) for f is

; : : : ;

###### a matrix whose rows correspond to the prime implicants m1 mk

; : : : ;

###### of f and whose columns correspond to the inputs y1 ys ∈ f[−][1](1) .

;
###### The matrix entry at place (i j) equals mi(yj) .


###### Due to the properties of prime implicants the disjunction of all prime implicants equals f and for a disjunction of some prime impli- cants g we know that g f . We are looking for a cheap set of prime ≤ implicants whose disjunction equals f . It is sufficient and necessary to choose for each yj f[−][1](1) some mi such that mi(yj) = 1 . A choice of ∈ prime implicants is a choice of rows in the PI-table. If and only if the submatrix consisting of the chosen rows contains no column without any 1 the disjunction of the chosen prime implicants equals f.

 We can simplify our problem by two easy reduction rules. Let ri be the row corresponding to the prime implicant mi and let cj be the column corresponding to yj ∈ f[−][1](1) .

 LEMMA 2.2 :

 i) If the only 1-entry of cj is contained in ri, we have to choose mi and may cancel ri and all ck such that mi(yk) = 1 .
 ii) If cj ≤ cj[′] for some j ̸= j[′], we may cancel cj[′] .

 Proof : i) Obviously mi is the only prime implicant such that mi(yj) = 1 . Therefore we have to choose mi . If mi(yk) = 1, we have done the job for the input yk . ii) We still have to choose a prime implicant mi such that mi(yj) = 1 . Since cj ≤ cj[′] implies mi(yj[′]) = 1, we ensure that we choose a prime implicant for input yj[′] . 2

 We perform the reductions until no further reductions are possible. The result of this procedure is called a reduced PI-table.


-----

**28**

###### EXAMPLE 2.1 : We save the first step and define f ∈ B4 by Q4, the set of implicants of length 4 .
 Q4: Q4;4 = ̸◦, Q4;3 = {a b c d ; a b c d}, Q4;2 = {a b c d ; a b c d ; a b c d}, Q4;1 = {a b c d ; a b c d ; a b c d}, Q4;0 = {a b c d} .
 Q3: Q3;3 = ̸◦, Q3;2 = {a b c ; a b c ; b c d}, Q3;1 = {a b d ; a c d ; a b c ; a c d ; b c d}, Q3;0 = {a b c ; a c d ; b c d} .
 P4 = ̸◦ .
 Q2: Q2;2 = ̸◦, Q2;1 = {b c}, Q2;0 = {c d; a c} .

;
###### P3 = {a b c a b d} .
 Q1 = ̸◦ .
 P2 = Q2 .

; ; ; ; :
###### PI(f) = a b c a b d b c c d a c { }

 The PI-table of f

 0010 0011 0100 0101 0111 1010 1011 1110 1111

 a b c 0 0 1 1 0 0 0 0 0
 a b d 0 0 0 1 1 0 0 0 0
 b c 1 1 0 0 0 1 1 0 0
 c d 0 1 0 0 1 0 1 0 1
 a c 0 0 0 0 0 1 1 1 1

;

###### c1 c3 and c8 have a single one. Therefore a minimal polynomial

; ;
###### has to contain a b c b c and a c . We may cancel r1 r3 and r5 and all
 columns up to c5 . We could have cancelled c6 since c8 c6 or c7 since ≤ c9 c7 . We obtain the following reduced table. ≤

|Col1|0010 0011 0100 0101 0111 1010 1011 1110 1111|
|---|---|
|a b c a b d b c c d a c|0 0 1 1 0 0 0 0 0 0 0 0 1 1 0 0 0 0 1 1 0 0 0 1 1 0 0 0 1 0 0 1 0 1 0 1 0 0 0 0 0 1 1 1 1|


-----

**29**

###### 0111

 a b d 1
 c d 1

 For a minimal polynomial we choose the cheaper prime implicant c d . Here the minimal polynomial is uniquely determined and equals a b c ∨ b c a c c d . Using three logical levels we obtain a more efficient ∨ ∨ circuit by the representation a b c c ( b a d ) . In our example ∨ ∨ ∨ the construction of a minimal polynomial from the reduced PI-table was trivial. In general, this is a hard problem as we shall see in 5. §

 2.3 The minimization method of Karnaugh

 For larger n, at least for n 7, computers should be used for the ≥ minimization of Boolean functions. The method of Karnaugh (53) is advantageous if one tries to perform the minimization for n 6 ≤ with one’s own hand. The main idea is a better representation of our information.

;
###### The set of inputs 0 1 is an n-dimensional cube. A monom m { }[n] of length k corresponds to an (n k)-dimensional subcube where the −

;
###### k variables of m are fixed in the right way. f is a coloring of 0 1 by { }[n] the colors 0 and 1 . m is an implicant iff the corresponding subcube is 1-colored. It is even a prime implicant iff no larger subcube, i.e. shorter

;
###### monom, is 1-colored. A vector a 0 1 has n neighbors which differ ∈{ }[n] from a in exactly one position. The recognition of neighborhoods is exceptionally simple in the Karnaugh diagrams.

|Col1|0111|
|---|---|
|a b d c d|1 1|


-----

**30**

###### EXAMPLE 3.1 : The Karnaugh diagram for the function of Exam- ple 2.1

 a b 00 01 11 10
 c d

 00 0 1 0 0
 01 0 1 0 0
 11 1 1 1 1
 10 1 0 1 1

; ; ;
###### We find f(a b c d) in column ab and row cd . Where are the neigh
; ; ;
###### bors of (a b c d) ? It is easy to check that the neighbors can be reached by one step in one of the four directions. The left neighbor of an element in the first column is the last element in the same row, and

<
###### so on. These diagrams are clearly arranged for n = 4 . For n 4, we even obtain smaller diagrams. For n = 5, we use two of the diagrams above, one for e = 0 and one for e = 1 . Then the fifth neighbor may be found at the same position of the other diagram. For n = 6, we already have to work with 4 of these diagrams. For n 7 the situation ≥ becomes unintelligible and Karnaugh diagrams should not be used.

 In our example each one in the diagram corresponds to an implicant of length 4 . Ones which are neighbors correspond to implicants of length 3 . The ones in the first column correspond to a b c and the first two ones in the second column correspond to a b c . The 1-colored subcube for a b c can be enlarged to the 1-colored subcube of the ones in the first and last column corresponding to the implicant b c . Since the 1-colored subcube for a b c cannot be enlarged, a b c is a prime implicant. We easily detect prime implicants in Karnaugh diagrams. Furthermore, we see that the one in the first row is contained only in one maximal 1-colored subcube, namely for a b c, which therefore

|a b c d|00 01 11 10|
|---|---|
|00 01 11 10|0 1 0 0 0 1 0 0 1 1 1 1 1 0 1 1|


-----

**31**

###### has to be contained in a minimal polynomial. Altogether we follow the same procedure as described in 2 but we have a more adequat § representation of the information. Veitch (52) suggested a similar procedure.

 2.4 The minimization of monotone functions

 Quine (53) has shown that the computation of the always unique minimal polynomial for a monotone Boolean function is easy.

 THEOREM 4.1 : Each prime implicant of a monotone function f ∈ Mn only contains positive literals.

 Proof : Let m = m[′] xj ∈ I(f) . It is sufficient to prove that the short- ening m[′] ∈ I(f) . If m[′](a) = 1 either aj = 0 implying m[′] xj(a) = 1 and f(a) = 1 or aj = 1 . In the last case let b be defined by bj = 0 and bi = ai for i ̸= j . Then m[′] xj(b) = 1 implying f(b) = 1 . Since b ≤ a and f is monotone, also f(a) = 1 . In either case m[′](a) = 1 implies f(a) = 1 . Hence m[′] I(f) . 2 ∈

 THEOREM 4.2 : For monotone functions f the unique minimal polynomial consists of all prime implicants.

 Proof : By Lemma 2.2 it is sufficient to construct for each m PI(f) ∈ some input a f[−][1](1) such that m(a) = 1 and m[′](a) = 0 for all ∈ m[′] PI(f), m[′] = m . By Theorem 4.1 we may assume w.l.o.g. that ∈ ̸ m(x) = x1 · · · xk . Let ai = 1 iff i ≤ k . Obviously m(a) = 1 . If m[′](a) = 1, m[′] = m and m[′] PI(f), m[′] can contain by Theorem 4.1 ̸ ∈ and by definition of a only variables xi where i ≤ k . Therefore m[′] is a proper submonom of m and m is no prime implicant. Contradiction. 2


-----

**32**

###### The minimal polynomial for f ∈ Mn is also called monotone dis- junctive normal form (MDNF).

 THEOREM 4.3 : The set of functions computable by monotone

;
###### circuits, i.e. -circuits, is equal to the set of monotone functions. {∧ ∨}

 Proof : By Theorem 4.1 each monotone function may be computed by a monotone circuit. By induction on the number of gates of a mono- tone circuit we prove that monotone circuits compute only monotone

; ; ; : : : ;
###### functions. The inputs 0 1 x1 xn are monotone. For the induction
 step it is sufficient to prove that f g and f g are monotone if f and ∧ ∨ g are monotone. Let a b . Then ≤

; ;
###### (f g)(a) = min f(a) g(a) min f(b) g(b) = (f g)(b) (4.1) ∧ { } ≤ { } ∧

 and

; ; :
###### (f g)(a) = max f(a) g(a) max f(b) g(b) = (f g)(b) (4.2) ∨ { } ≤ { } ∨

 2

 Monotone circuits will be investigated in detail in Ch. 6. The mono
;
###### tone basis {∧ ∨} is denoted by Ωm and the corresponding complexity measures are denoted by Cm and Dm .


-----

**33**

###### 2.5 The complexity of minimizing

 So far we have described efficient algorithms for the computation of PI(f) and the reduced PI-table. No efficient algorithm for the sec- ond part, the computation of a minimal polynomial from the reduced PI-table, is known. We argue that with high probability no such algo- rithm exists. For this purpose we use the concept of NP-completeness (see Garey and Johnson (79)). For all those who are not familiar with the NP-theory we give the following short explanation. Many (more than 1000) problems are known to be NP-complete. It can be proved that one of the following statements is correct. Either all NP-complete problems have polynomial algorithms or no NP-complete problem may be solved by a polynomial algorithm. The conjecture of most of the experts is that the second statement holds. One of the well-known NP-complete problems is the set cover problem which we prove to be equivalent to our minimization problem.


###### DEFINITION 5.1 : An instance of the set cover problem is given

; : : : ; ; : : : ;

###### by different sets S1 Sm ⊆{1 n} such that the union of all Si

; : : : ;
###### is 1 n, and some number k m . The problem is to decide { } ≤

; : : : ;
###### whether the union of k of the sets Si equals {1 n} .

 The problem of determining the minimum k such that k subsets

; : : : ;
###### are sufficient to cover 1 n is not easier. The connection with our { } minimization problem is easy to see. The inputs a f[−][1](1) correspond ∈

; : : : ;
###### to the elements 1 n and the prime implicants correspond to the sets Si . In particular, j ∈ Si iff mi(yj) = 1 . We may still hope that minimization problems only lead to easy instances of the set cover problem. This hope has been destroyed by Paul (75).


-----

**34**

###### DEFINITION 5.2 : A 0-1-matrix is called reduced if each row con- tains at least one 1-entry, each column contains at least two 1-entries and if no columns c and c[′] have the property c c[′] . ≤

 THEOREM 5.1 : For each reduced matrix M there exists a Boolean function f, whose reduced PI-table equals M . Furthermore f can be chosen such that all prime implicants of the reduced PI-table have the same length.

 Proof : Let n be the number of rows of M and let S be the set of columns of M . It will turn out that the following function f ∈ Bn+2 satisfies the assertion of the theorem.

;
###### For a ∈{0 1}[n] we denote a1 ⊕· · · ⊕ an, the parity of a, by |a| . The vector of zeros only is denoted by 0 .

; ;
###### f(a 0 0) = 1 a = 0 . (5.1) ̸

; ; ;
###### f(a 1 1) = 0 for all a 0 1 . (5.2) ∈{ }[n]

; ;
###### f(a 1 0) = 1 if a = 0, a S and a = 0 . (5.3) ̸ ̸∈ | |

; ;
###### f(a 0 1) = 1 if a = 0, a S and a = 1 . (5.4) ̸ ̸∈ | |

 We claim that PI(f) consists of the following three subsets where ma again is the minterm for a .

 PI(f) = {ma xn+1 | a ̸= 0, a ̸∈ S, |a| = 1} (5.5)

 ∪{ma xn+2 | a ̸= 0, a ̸∈ S, |a| = 0}

:
###### ∪{xi xn+1 xn+2 | 1 ≤ i ≤ n}

 At first it is easy to see that all monoms in (5.5) are implicants and no monom is a shortening of another one. Therefore it is sufficient to prove that all other implicants of f are lengthenings of the monoms in (5.5).


-----

**35**

###### Let t ∈ I(f) . Because of (5.2) t contains either xn+1 or xn+2 or both of them. Because of (5.1) t contains some xi if it contains xn+1 and xn+2 . If t contains xn+1 but not xn+2, then t contains a full minterm ma . Otherwise t does not contain xi and xi for some i and we

; ;
###### find vectors a and a[′] differing only at position i such that t(a 0 1) =

; ; ; ; ; ;

###### t(a[′] 0 1) = 1 implying f(a 0 1) = f(a[′] 0 1) = 1 . Because of (5.4)
 a = a[′] = 1 which is impossible if a and a[′] differ only at one position. | | | |

;
###### Altogether t contains xn+1 and ma for some a ∈{0 1}[n] . Again (5.4) implies that a = 0, a S and a = 1 . Similar arguments hold if t ̸ ̸∈ | | contains xn+2 but not xn+1 . Altogether we have proved (5.5).

; ;
###### We consider the PI-table of f . The column for (a 0 1) f[−][1](1) ∈ has a single one in the row ma xn+1 . The PI-table may be reduced

; ; ; ;
###### by eliminating the row ma xn+1 and the columns (a 0 1) and (a 0 0) .

; ;
###### Similar arguments hold for rows ma xn+2 and inputs (a 1 0) ∈ f[−][1](1) . We obtain the following partially reduced PI-table M[′] . M[′] has rows for

; ;
###### xi xn+1 xn+2 (1 ≤ i ≤ n) and columns for (a 0 0) and some a ∈ S . The

; ; ; ; ; ;
###### columns (a 0 1) and (a 1 0) have all been eliminated. Column (a 0 0) has been eliminated either during the elimination of row ma xn+1 iff a ̸∈ S and |a| = 1 or during the elimination of row ma xn+2 iff a ̸∈ S

; ;
###### and |a| = 0 . Furthermore xi xn+1 xn+2(a 0 0) = ai . Therefore the partially reduced PI-table M[′] is equal to the given matrix M . Since M is reduced, M[′] is reduced too. All prime implicants have length 3 . 2

 2.6 Discussion

 As we have shown the minimization of a Boolean function is (prob- ably) a hard problem. Furthermore, a minimal polynomial for f does not lead to an optimal circuit for f . We only obtain an optimal circuit in the rather restricted class of two-level-circuits. The following ex- ample of Lupanov (65 a) shows that a very simple function may have


-----

**36**

###### an expensive minimal polynomial.

 PROPOSITION 6.1 : Let f(x) = x1 xn be the parity function. ⊕· · ·⊕ Then C(f) n 1 but the minimal polynomial consists of 2[n][−][1] prime ≤ − implicants of length n each.

 Proof : By definition C(f) ≤ n − 1 . PI(f) is the set of minterms ma such that a1 ⊕· · · ⊕ an = 1 . Since |m[−]a [1][(1)][|][ = 1, all prime implicants] are necessary for the minimal polynomial. 2

 In Ch. 11 we show that even k-level-circuits computing the parity function require an exponential number of gates. Of course parity is an extreme example. Korshunov (81 b) and Kuznetsov (83 b) have shown that for almost all f ∈ Bn the number of prime implicants in a

=

###### minimal polynomial is at least (1−εn) 2[n] (log n log logn) where εn → 0

: =
###### and at most 1 6 2[n] (log n log logn) . In Ch. 4 we construct efficiently

= =

###### a circuit with at most 2[n] n + o(2[n] n) gates for each f ∈ Bn .
 Finally we mention that it is possible to develop a dual theory by exchanging the roles of and and of 0 and 1 . Instead of monoms ∧ ∨ we obtain Boolean sums and instead of (prime) implicants (prime) clauses. For monotone functions the monotone conjunctive normal form (MCNF) is the counterpart of the MDNF.

 EXERCISES

 1. Compute a minimal polynomial for

; ; ;
###### f(a b c d) = a b c d a b c d a b c d a b c d a b c d ∨ ∨ ∨ ∨ ∨
 a b c d a b c d ∨

 2. How often do we obtain m ∈ Qi while constructing Qi according to the Quine and McCluskey algorithm ?


-----

**37**

###### 3. Describe the set of prime implicants of f ∈ Bn where f computes 1 iff x1 + · · · + xn ̸≡ 0 mod k .


###### 4. Define a function f ∈ Bn with Ω(3[n]

 5. D(f) ≤ n + log n for all f ∈ Bn .


=
###### n) prime implicants.


###### 6. Define a function f ∈ Bn which has not a unique minimal polyno- mial.

; ;
###### 7. Design polynomial -circuits for the parity function such {∧ ∨ ¬} that the number of logical levels grows as slowly as possible.

 8. Prove the dual counterpart of Proposition 6.1 for the parity func- tion.

;
###### 9. Let f g ∈ Mn . f ≤ g ⇔∀ p ∈ PI(f) ∃ q ∈ PI(g) : p ≤ q .

 10. Compute all prime implicants and prime clauses of T[n]k [, the][ k] [-th] threshold function, computing 1 iff the number of ones in the input is at least k .

 For the following problems (Oberschelp (84)) we need some defini
; : : : ;
###### tions. Let S = 0 s 1 and let i j i + j mod s . An interval { − } ⊕ ≡

; ; ; : : : ;

###### [a b] contains a a 1 b . A (generalized) rectangle is a Cartesian ⊕ product of intervals. For a rectangle D S[n] and some c S 0 the ⊆ ∈ −{ } corresponding monom m is defined by m(x) = c if x D and m(x) = 0 ∈ otherwise. m I(f) if m f . m PI(f) if no implicant m[′] I(f) ∈ ≤ ∈ ∈ corresponds to D[′] and c[′] such that D D[′], D = D[′] and c = c[′] or ⊆ ̸

<
###### D = D[′] and c c[′] . The partial derivative of f at a with respect to xi is defined by


@ =@
###### f xi(a) = min{f(a1


; : : : ;
###### ai 1
_−_


; ;
###### ai ⊕ 1 ai+1


; : : : ; ;
###### an) f(a1


; : : : ; :
###### an)}


-----

**38**

###### 11. For s = 2 the above definitions of monoms and (prime) implicants are equal to the definitions in 1. §

 12. The order of partial derivatives is arbitrary.

 13. @f =@ [j]xi = @f =@ [j][′]xi if j; j[′] ≥ s − 1 .

 14. Describe the set of functions f : S[n] S such that →

@f =@ [i(1)]x1 · · · @ [i(n)]xn(a) = b .


<
###### 15. g : S[n] → S has a local maximum at a if g(bi) g(a) for all

; : : : ; ; ; ; : : : ;

###### bi = (a1 ai−1 ai ⊕ 1 ai+1 an) .
 If g = @f =@ [i(1)]x1 @ [i(n)]xn has a local maximum at a, the monom · · ·

; ;

###### h corresponding to D = [a1 a1 ⊕ i(1)] × · · · × [an an ⊕ i(n)] and
 c = g(a) is a prime implicant of f .

 16. By the consideration of all local maxima we do not detect all prime implicants. Describe an algorithm for the computation of all prime implicants. Consider at first the case s = 2 .


-----

**39**

###### 3. THE DESIGN OF EFFICIENT CIRCUITS FOR SOME FUN- DAMENTAL FUNCTIONS

 In this chapter we design for some fundamental functions circuits of small size and small depth. The design methods we use are im- portant, since they are quite general. It may be astonishing that we already need clever and subtle methods for the design of efficient ad- dition, multiplication and division circuits. The basic methods learnt in school are not efficient enough. In order to estimate the value of our circuits we mention that for all functions f ∈ Bn;m considered in this chapter n 1 gates and depth log n are necessary (see Ch. 5). − ⌈ ⌉ Here and in the rest of the book we use the so-called upper and lower Gaussian brackets.

Z Z :
###### x = min z z x and x = max z z x ⌈ ⌉ { ∈ | ≥ } ⌊ ⌋ { ∈ | ≤ }

; : : : ; ;

###### The binary number a = (an 1 a0) 0 1 has the value a =
_−_ _∈{_ _}[n]_ _|_ _|_

###### a0 2[0] + · · · + an−1 2[n][−][1] .

 3.1 Addition and subtraction

 DEFINITION 1.1 : The addition function fn[add] ∈ B2n;n+1 has two n-bit numbers x and y as inputs and computes the (n + 1)-bit repre- sentation s of x + y . | | | |

 In this section fn means fn[add] . How efficient is the addition method we learnt in school ? We use a halfadder to compute s0 = x0 y0 and ⊕ the carry bit c0 = x0 ∧ y0 . Afterwards we use n − 1 fulladders for the computation of si and ci from xi, yi and ci−1 . Finally sn = cn−1 .


-----

**40**

###### Already in Ch. 1 we have defined a fulladder of size 5 and depth 3 by

 sj = xj ⊕ yj ⊕ cj−1 and (1.1)


###### cj = xj yj ∨ (xj ⊕ yj) cj−1


:
###### (1.2)


###### Altogether we obtain a circuit of size 5n 3 and depth 2n 1 . Here − − we compute in parallel all xj yj and xj yj . Afterwards sj and cj can ⊕ be computed in depth 2 if cj−1 is computed.

 THEOREM 1.1 : The school method of addition leads to a circuit of size 5n 3 and depth 2n 1 . − −

 This circuit is of minimal size (see Ch. 5). But its depth is far too large. This is not astonishing, since the method has been designed for sequentially working people. We try to reduce the depth. The problem is the computation of the carry bits. Later we compute all carry bits in advance. Now we compute the sum under the condition that the carry bits have certain values. Afterwards we select the right output. This procedure due to Sklansky (60 a) and (60 b) is called Conditional Sum Adder.
 For the sake of simplicity we assume that n = 2[k] . It should always be easy for the reader to generalize the algorithms to arbitrary n .
 The numbers x and y have n = 2[k] bits and can be divided into 2[k][−][l]
 blocks each of length 2[l] . The i -th block of x of length L = 2[l], namely (xiL−1 ; : : : ; x(i−1)L), is denoted by Xi;l . Our problem is the addition of
 X1;k (the number x) and Y1;k where the carry bit at position 0 is 0 . The subproblem Pi;l ;c [where 0][ ≤] [l][ ≤] [k, 1][ ≤] [i][ ≤] [2][k][−][l][ and c][ ∈{][0][;][ 1][}]

; : : : ;

###### is the problem of adding Xil, namely (xiL−1 x(i−1)L), Yil, namely
 (yiL−1 ; : : : ; y(i−1)L), and c . Altogether we have to solve P1;k;0 .
 Since we are looking for a circuit of small depth, we solve the problems Pi;l ;c [for fixed][ l][ in parallel. For][ l][ = 0 and c = 0 we have to] compute the sum bits xj yj and the carry bits xj yj . For l = 0 ⊕ ∧ and c = 1 we have to compute the sum bits xj yj and the carry bits ⊕ xj yj . Altogether step 0, the solution of all Pi;0;c, can be realized ∨


-----

**41**


###### with 4n gates in depth 1 .
 In step l (1 ≤ l ≤ k) we solve all problems Pi;l ;c [where we may use] the results of all problems Pi;l −1;c . Let us consider Pi;l ;c [in more detail.]

; : : : ; ; : : : ;

###### We have to add the summands (xiL 1 x(i 1)L), (yiL 1 y(i 1)L)
_−_ _−_ _−_ _−_

###### and c . In order to use the solutions of smaller problems, we describe the summands in another way where L[′] = 2[l] [−][1] .


###### Summands for Pi;l ;c [:] � ; : : : ; ; ; : : : ; ; x2iL[′] 1 x(2i 1)L′ x(2i 1)L′ 1 x(2i 2)L′[�] (1.3)
_−_ _−_ _−_ _−_ _−_

###### � ; : : : ; ; ; : : : ; : y2iL[′] 1 y(2i 1)L′ y(2i 1)L′ 1 y(2i 2)L′[�] and c
_−_ _−_ _−_ _−_ _−_

###### By (1.3) the second half of the solution of Pi;l ;c [is the solution of] P2i−1;l −1;c without the foremost carry c[′] . The first half of the solution of Pi;l ;c [is the solution of P]2i;l −1;c[′][ . Since c is given we may directly] use the solution of P2i−1;l −1;c . But c[′] is not known in advance. c[′] is an output of P2i−1;l −1;c . Let z[0]j [((2i][ −] [1)L][′][ ≤] [j][ ≤] [2iL][′][) and z]j[1] [be the] output bits of P2i;l −1;0 and P2i;l −1;1 resp. Using c[′] we may select the right output bit (z[0]j [if c][′][ = 0 or z]j[1] [if c][′][ = 1) by]
 zj = (c[′] ∧ z[1]j [)][ ∨] [(c][′][ ∧] [z]j[0][)] (1.4)

 in depth 2 using 3 gates. Altogether step l can be realized in depth 2 using for each of the 2[k][−][l] 2 problems 3(2[l] [−][1] + 1) gates. The circuit
 · size of step l is 3(2[k] + 2[k][−][l+1]) .

 The depth of the whole circuit is 1 + 2k = 2 log n + 1 and the size is

 � 4n + 3(2[k] + 2[k][−][l] [+1]) = 4n + 3k 2[k] + 3(2[k+1] 2) (1.5)
 −
1 _l_ k
_≤_ _≤_

:
###### = 3n log n + 10n 6 −

 THEOREM 1.2 : The Conditional Sum Adder may be realized (if n = 2[k]) in depth 2 log n + 1 and size 3n log n + 10n 6 . −


-----

**42**

###### According to our remark at the beginning of this chapter the depth of this circuit is only double the size of the lower bound. But the size of the circuit is not linear. The Carry Look Ahead Adder due to Of- man (63) simultaneously has size O(n) and depth O(log n) . Constant factors for depth have stronger consequences than constant factors for size. Therefore the adder of Brent (70) of size O(n log n) and depth log n + O(log[1][=][2] n) is interesting. Krapchenko (70) came up with an adder of linear size and depth log n + O(log[1][=][2] n) .

 THEOREM 1.3 : Krapchenko’s adder for n-bit numbers has size 3n + 6 2[m] and depth m + 7(2m)[1][=][2] + 16 where m = log n . · ⌈ ⌉
 For n = 2[k] the size of Krapchenko’s adder is only by the factor

:
###### of 1 8 larger than the minimal size for an adder. The additive term 7(2m)[1][=][2] + 16 for the depth seems to be quite large, in particular for small n . In fact the additive term is smaller but our estimations are not exact. The following proof is long and technically involved, although the ideas are easy.


###### Proof of Theorem 1.3 : Krapchenko’s adder S consists of five parts

; : : : ;

###### S1 S5 . In S1 uj = xj yj and vj = xj yj are computed by n half ⊕ adders. The crucial part is the computation of the carry bits cj in S2, S3 and S4 . Afterwards, it is easy to compute in S5 the outputs s0 = v0, sj = vj ⊕ cj−1 for 1 ≤ j ≤ n − 1 and sn = cn−1 . Therefore

 C(S1) = 2n D(S1) = 1 and (1.6)

:
###### C(S5) = n − 1 D(S5) = 1 (1.7)

 By applying (1.2) for j + 1 times we can compute cj from the u- and v-parameters.

 cj = uj ∨ vj cj−1 = uj ∨ uj−1 vj ∨ vj−1 vj cj−2 = · · · = (1.8)


###### � = ui vi+1 vj
 · · ·
0 i j
_≤_ _≤_


:


###### This can be interpreted in the following way. Carry cj = 1 iff for some i ≤ j at position i we have two ones (ui = 1) and at the positions


-----

**43**

; : : : ;
###### i + 1 j exactly a zero and a one (vi+1 = · · · = vj = 1). More generally, we define for b a ≥


;
###### va+1


###### Gb;a = gb−a+1 (ub


;
###### vb


; : : : ;
###### ua+1


;
###### ua) = (1.9)


###### � = ui vi+1 vb
 · · ·
a i b
_≤_ _≤_


###### Vb;a = va vb · · ·


:
###### (1.10)


###### In particular cj = Gj;0 . In Fig. 1.1 we give a triangle representation for Gd;a where one has to combine the rows by disjunctions. Let a <

<
###### b d . Since

 Gd;a : ua va+1 : : : vb−1 vb vb+1 vb+2 : : : vd−1 vd
 ua+1 : : : vb 1 vb vb+1 vb+2 : : : vd 1 vd Vd;b+1

_−_ _−_

###### · · · · · · · · · · · · · · · · · · · · · · · · · · ·

: : :

###### ub vb+1 vb+2 vd 1 vd

_−_
###### Gb;a


###### ub+1 vb+2 vd 1 vd · · · −
 · · · · · · · · · · · · ud 1 vd
_−_
###### ud Gd;b+1

 Fig. 1.1

 Gd;a = Gd;b+1 Gb;a Vd;b+1 and (1.11) ∨


###### Vd;a = Vb;a Vd;b+1


:
###### (1.12)


###### According to Fig. 1.1 G-functions are called triangles and V-functions are called rectangles.
 In S2 we compute some not too large triangles and rectangles. For

; : : : ;
###### some parameter τ to be chosen later we partition 0 n 1 to { − }

; ; : : : ;
###### blocks of size 2 4 2[τ] and compute the corresponding triangles and rectangles. These results are used in S3 for the computation of all carry


-----

**44**

###### bits cj where j = k 2[τ] −1 for some k . In S4 we fill the gaps and compute all cj .

 We have already computed triangles of size 1, namely uj, and rectangles of size 1, namely vj . By (1.11) and (1.12) we may compute rectangles and triangles of size 2[l] from the rectangles and triangles of size 2[l] [−][1] with 1 and 2 gates resp. in depth 2 . The number of blocks of size 2[l] may be estimated by 2[m][−][l] . Altogether

:
###### C(S2) ≤ 3 · 2[m](1 − 2[−][τ] ) and D(S2) = 2τ (1.13)

 S4 is rather simple too. In S3 we have computed all ck 2τ 1 . The
_−_
###### other carry bits are computed in τ steps where we compute all c τ l
k 2 _−_ 1
_−_
###### in step l . For even k these carry bits have already been computed. For odd k = 2j + 1 by (1.8) – (1.12)

 c τ l (1.14)
(2j+1) 2 _−_ 1 =
_−_


###### G(2j+1) 2τ −l −1; (2j) 2τ −l ∨ V(2j+1) 2τ −l −1; (2j) 2τ −l c(2j) 2τ −l −1


:


###### The terms on the right-hand side are computed in S2, S3 or in earlier steps of S4 . The depth of step l is 2 while the size is 2 for each new

; : : : ;
###### carry. j may take values in 0 2[m][−][τ] [+][l] [−][1] 1 . Thus { − }

:
###### C(S4) ≤ 2 · 2[m](1 − 2[−][τ] ) and D(S4) = 2τ (1.15)

 In S3 we use the triangles u[′]j [and rectangles v]j[′] [of size 2][τ][ as inputs]

; ; : : : ;

###### (0 ≤ j ≤ 2[m][−][τ] − 1) and compute all G[′]j;0 [= g][j+1][(u]j[′] vj[′] u[′]0[) . By]
 (1.11) and (1.12) we can conclude that G[′]j;0 [is the carry bit at position] (j + 1) 2[τ] 1 . We have to solve the problem of computing all carry − bits but the input size has been reduced from n to 2[m][−][τ] .


###### At first we explain our ideas by an implementation of small depth and large size. Afterwards we bound depth and size simultaneously. Considering depth only to consider one output only is sufficient, say G2m 1;0 = g 2m(u2m 1 ; v2m 1 ; : : : ; u0) .
_−_ _−_ _−_


-----

**45**


###### Again by (1.11) and (1.12)

 G2m 1;0 = (1.16)
_−_
###### � G2m i 2r 1; 2m (i+1) 2r V2m 1; 2m i 2r :

_−_ _−_ _−_ _−_ _−_
0 i 2[m][−][r] 1
_≤_ _≤_ _−_

###### All triangles on the right side have length 2[r], the rectangles can be computed in depth m, all conjunctions between triangles and rect- angles can be done in parallel and by divide-and-conquer, the outer disjunction can be performed in depth m r . −

 D(g m) m r + 1 + max D(g r); m ; (1.17)
2 _≤_ _−_ _{_ 2 _}_

###### since all triangles and rectangles can be computed in parallel. For the �l � sake of simplicity let us assume that m = h(l ) = . Then we choose
2
###### r = h(l 1) . By induction we can prove that −

:
###### D(g 2h(l )) ≤ h(l + 1) (1.18)
 For l = 1, m = 0 and g1 has depth 0 ≤ h(2) = 1 . For the induction step l 1 l we apply (1.17). By induction hypothesis the depth − → of g r is bounded by h(l ) = m . Thus the depth of g m is bounded
2 2
_l_ _l_ 1 _l_ +1
###### � � � − � � � by 2m r + 1 or 2 + 1 = = h(l + 1) . Furthermore − 2 − 2 2 �l +1� �l �
2 = 2 + l = m + O(m[1][=][2]) and for n ≤ 2[m] the depth of gn is
###### bounded by log n + O(log[1][=][2] n) .

 In order to guarantee also linear size we have reduced the number of inputs by the use of S2 and S4 and we use a more complicated implementation of all g-functions. Here we have 2[m][′] inputs where �t� m[′] = m τ . We choose the smallest t such that m[′] = h(t) . − ≤ 2
t 1
###### � − � < Since m[′], it is easy to prove that
2

< :
###### t (2m[′])[1][=][2] + 2 (1.19)

;
###### For 1 l t and 0 j 2[m][′] 1 let d(l j) be the largest multiple of ≤ ≤ ≤ ≤ − 2[h(][l] [)] not larger than j . Then

; ; ; :
###### j 2[h(][l] [)] + 1 d(l j) j in particular d(t j) = 0 (1.20) − ≤ ≤

 For 2 l t and 0 j 2[m][′] 1 let ≤ ≤ ≤ ≤ −


-----

**46**

; ; ; =
###### e(l j) = (d(l 1 j) d(l j)) 2[h(][l] [−][1)] − −

<
###### By (1.20) we obtain for l t


:
###### (1.21)


<
###### 2[h(][l] [)][−][h(][l] [−][1)] = 2[l] [−][1] and (1.22)


; ; = <
###### e(l j) (j d(l j)) 2[h(][l] [−][1)] 2[h(][l] [)][−][h(] ≤ −

; ; = =
###### e(t j) = d(t 1 j) 2[h(t][−][1)] j 2[h(t][−][1)] − ≤


<
###### 2[m][′][−][h(t][−][1)] 2[t][−][1] ≤


:
###### (1.23)


###### We now compute all triangles G[′] and rectangles V[′] based on the inputs u[′]j [and v]j[′] [. The rectangles are computed in t][ −] [1 steps (1][ ≤] [l][ ≤]

;
###### t 1). In step l we compute for 1 k e(l +1 j) and 0 j 2[m][′] 1 − ≤ ≤ ≤ ≤ −

 V[′] (1.24)
j; d(l ;j) k 2[h(][l] [)][ =]
_−_


###### Vj[′] ; d(l ;j) [∧] 1 �r kVd([′] l ;j)−(r−1) 2[h(][l] [)]−1; d(l ;j)−r 2[h(][l] [)]

_≤_ _≤_


:


###### The correctness of (1.24) is obvious. It is necessary to prove that the

;
###### rectangles on the right side are computed before step l . For k = e(l j),

; ;
###### we get d(l j) = d(l − 1 j) − k 2[h(][l] [−][1)] by (1.21). Therefore Vj[′]; d(l ;j) [has]

;
###### been computed before. For the other rectangles let j[′] = d(l j) (r − −

;
###### 1) 2[h(][l] [)] 1 . By definition of d(l j) we can find some k such that −

;
###### d(l j) = k 2[h(][l] [)], thus j[′] = (k r) 2[h(][l] [)] + 2[h(][l] [)] 1 . − −

; ;
###### Furthermore d(l j) r 2[h(][l] [)] = (k r) 2[h(][l] [)] = d(l j[′]) by definition of d . − − So also the other rectangles are of the form Vj[′][′] ; d(l ;j[′]) [and are computed]
 before step l .

 The triangles are computed in t 1 steps (2 l t). In step l we − ≤ ≤ compute for 0 j 2[m][′] 1 ≤ ≤ −

 G[′]j; d(l ;j) [= G]j[′] ; d(l 1;j)
_−_ _[∨]_
###### � V[′] (1.25)

j; d(l 1;j) (r 1) 2[h(][l] _[−][1)][ ∧]_
1 r e(l ;j) _−_ _−_ _−_
_≤_ _≤_


###### G[′]
d(l 1;j) (r 1) 2[h(][l] _[−][1)]_ ; d(l 1;j) r 2[h(][l] _[−][1)]_
_−_ _−_ _−_ _−_ _−_


:


###### (1.25) is correct by our standard arguments. The rectangles are com- puted before step l as has been shown above. The triangles on the right have been computed at step l − 1 . Finally G[′]j; d(t;j) [= G]j[′] ; 0 [is the] carry bit at position (j + 1) 2[τ] 1 . −


-----

**47**

###### We estimate the depth and size of S3 . In (1.24) we compute the

;
###### conjunction of at most e(l + 1 j) rectangles. By (1.22) and (1.23) this can be done in depth l . In (1.25) we perform the conjunctions in depth 1 in parallel. Afterwards we compute the disjunction of at most

;
###### e(l j) + 1 terms. By (1.22) the depth of step l is bounded by l and by (1.23) the depth of step t is bounded by m[′] h(t 1) + 1 . Altogether − − by (1.19)

 D(S3) ≤ 1 + · · · + t − 1 + m[′] − h(t − 1) + 1 = m[′] + t (1.26)

< :
###### m[′] + (2m[′])[1][=][2] + 2

 The size of S3 is estimated in the same way. For the computation of all rectangles the following number of gates is sufficient.
 � � � k � � 2[l] (2[l] 1)=2
 ≤ −

1 _l_ t 1 0 j 2[m][′] 1 1 k e(l +1;j) 1 _l_ t 1 0 j 2[m][′] 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_ _≤_ _≤_ _≤_ _≤_ _−_ _≤_ _≤_ _−_


=
###### = 2[m][′][ �]2(4[t][−][1] 1) 3 2[t][−][1][�] − −


:
###### (1.27)


###### The number of gates for the triangles is estimated by
 � � ; � :
 2 e(l j) 2[m][′][ �]2[t+1] 2t 1 (1.28) ≤ − −

2 _l_ t 0 j 2[m][′] 1
_≤_ _≤_ _≤_ _≤_ _−_

###### By (1.27) and (1.28)


:

###### C(S3) ≤ 2[m][′] 2[2t][−][1] (1.29)


###### We summarize our complexity estimations.

 D(S) m[′] + (2m[′])[1][=][2] + 4τ + 4 = m + (2m[′])[1][=][2] + 3τ + 4 (1.30) ≤

 and

 C(S) 3n + 5 2[m](1 2[−][τ] ) + 2[m][′] 2[2t][−][1] (1.31) ≤ · −

<
###### where m = log n, m[′] = m τ and t (2m[′])[1][=][2] + 2 . For ⌈ ⌉ −
 � τ = 2(2m)[1][=][2][�] + 3 (1.32)

 m[′] + 2t 1 m and the bounds of the theorem are proved. 2 − ≤


-----

**48**

###### Since addition is the most fundamental operation, we present an- other adder which simultaneously has linear size and logarithmic depth (Ladner and Fischer (80)). The structure of this adder is easier than Krapchenko’s adder.

 At first we solve the prefix problem, the efficient computation of all prefixes pi = x1 ◦· · · ◦ xi for an associative operation ◦ . Later we explain how the prefix problem may be used for the design of an efficient adder. Ladner and Fischer present a family of algorithms Ak(n) for inputs of length n . For n = 1 nothing has to be done. Let

 ###### n 1 .
 A0(n) : In parallel we apply A1(⌈n=2⌉) to x1 ; : : : ; x⌈n=2⌉ and A0(⌊n=2⌋)
 to x⌈n=2⌉+1 ; : : : ; xn . Afterwards pi is computed for i ≤⌈n=2⌉ . All
 pi = (x1 ◦· · · ◦ x⌈n=2⌉) ◦ (x⌈n=2⌉+1 ◦· · · ◦ xi) for i > ⌈n=2⌉ may be computed in one step each in parallel.

=
###### Ak(n) (k ≥ 1) : In parallel we compute the ⌊n 2⌋ pairs x1 ◦ x2,

; : : : =

###### x3 x4 . Afterwards we apply Ak 1( n 2 ) to these pairs and, if ◦ − ⌈ ⌉

; =

###### n is odd, xn . We compute all p2i p1 and pn . The missing ⌊n 2⌋− 1
 prefixes p2i+1 = p2i x2i+1 can be computed in parallel. ◦

; ;
###### By C(k n) and D(k n) we denote the size and depth resp. of Ak(n) .

;
###### Furthermore D[∗](k n) is the depth of pn using Ak(n) . Considering the description of the algorithms we conclude

; ; ;
###### C(k 1) = D(k 1) = 0 (1.33)

; ; = ; = = ;
###### C(0 n) = C(1 n 2 ) + C(0 n 2 ) + n 2 (1.34) ⌈ ⌉ ⌊ ⌋ ⌊ ⌋

; ; = ; ; = ; ; = ;
###### D(0 n) = max D(1 n 2 ) D[∗](1 n 2 ) + 1 D(0 n 2 ) + 1 { ⌈ ⌉ ⌈ ⌉ ⌊ ⌋ } (1.35)

; ; = = ;
###### C(k n) = C(k 1 n 2 ) + 2 n 2 1 (1.36) − ⌈ ⌉ ⌊ ⌋−

; ; = ;
###### D(k n) D(k 1 n 2 ) + 2 (1.37) ≤ − ⌈ ⌉

; ; = :
###### D[∗](k n) D(k 1 n 2 ) + 1 (1.38) ≤ − ⌈ ⌉

 We have used the fact that Ak(n) computes pn before the last step. The solution of (1.33) – (1.38) easily follows from induction.


-----

**49**

###### THEOREM 1.4 : The prefix problem is solved by Ak(n) . For 0 k log n ≤ ≤⌈ ⌉

;
###### C(k n) 2n(1 + 2[−][k]) and (1.39) ≤

; :
###### D(k n) k + log n (1.40) ≤ ⌈ ⌉

 How can we use the prefix problem for the addition of binary num- bers ? We use the subcircuits S1 and S5 of Krapchenko’s adder with size 2n and n − 1 resp. and depth 1 each. S1 computes a coding of the inputs bits.


;

###### uj = xj yj vj = xj yj
 ⊕


:
###### (1.41)


###### After having computed the carry bits we compute the result by


###### s0 = v0


; ;
###### sj = vj ⊕ cj−1 for 1 ≤ j ≤ n − 1 sn = cn−1


:
###### (1.42)


;

###### We know that cj = uj ∨ vj cj−1 . Since (uj vj) may take the values

; ; ; ; ;
###### (0 0), (0 1) and (1 0) we consider the functions A(0 0), A(0 1) and

;
###### A(1 0) where

; ; :
###### A(u v)(c) = u v c for c 0 1 (1.43) ∨ ∈{ }

 By definition we may compute the carry bits by


;

###### ci = A(ui vi) ◦· · · ◦ A(u0


; :
###### v0)(0) (1.44)


###### This looks like the prefix problem.

; ; ; ; ; ;
###### We have to prove that G = ( A(0 0) A(0 1) A(1 0) ) is a monoid. { } ◦

;
###### Since the functions are defined on 0 1 it is easy to check by case { } inspection that

; ; ; ;
###### A(0 0) A(u v) = A(0 0) (1.45) ◦

; ; ; ;
###### A(0 1) A(u v) = A(u v) and (1.46) ◦

; ; ; :
###### A(1 0) A(u v) = A(1 0) (1.47) ◦

 The operation on sets of functions is always associative. Therefore ◦ the conditions for the application of the prefix algorithms are fulfilled.


-----

**50**

###### We only have to design a circuit for the operation . ◦

; ; ;
###### Let A(u v) = A(u2 v2) ◦ A(u1 v1) . Again by (1.45) – (1.47) it is easy
 to check that


;
###### (u v) = (u2 ∨ u1v2


; :
###### v1v2) (1.48)


###### Here we find again the characteristic computation of triangles and rectangles as in Krapchenko’s adder. By (1.48) a subcircuit for the operation ◦ has size 3 and depth 2 . By the prefix algorithm Ak(n) we

; ; ; ; ; ; ;

###### may compute all (Gi Vi) ∈{(0 0) (0 1) (1 0)} such that A(Gi Vi)

; ; ;

###### is equal to A(ui vi) ◦· · · ◦ A(u0 v0) with a circuit of size 3 C(k n)

; ;
###### and depth 2 D(k n) . By (1.43) and (1.44) ci = A(Gi Vi)(0) = Gi . We
 may save n gates, since we may eliminate the gates for the computation of Vi . Vi is not necessary for the computation of ci, and the prefix algorithm uses Vi only for the computation of other Vj (see (1.48)).

;
###### Summarizing, the depth of the resulting circuit is 2 D(k n)+2 and

;
###### its size is 3 C(k n) + 2n 1 . By Theorem 1.4 we have proved −

 THEOREM 1.5 : For 0 k log n there exist adders based ≤ ≤⌈ ⌉ on prefix algorithms whose size is (8 + 6 2[−][k]) n and whose depth is · 2 log n + 2k + 2 . ⌈ ⌉

 Even the most fundamental operation, the addition, is as we have seen a fascinating problem.

 We do not consider the subtraction of binary numbers in detail. The complexity of subtraction is nearly the same as the complex- ity of addition. If we use the first bit of a number as a sign (0 = negative number, 1 = positive number), we have to distinguish be- tween the different cases. More appropriate is the use of the well- known 1-complement or 2-complement of binary numbers. These representations of binary numbers are easy to compute. Afterwards we may use the same algorithms for addition and subtraction (see e.g. Spaniol (76)).


-----

**51**

###### 3.2 Multiplication

 DEFINITION 2.1 : The multiplication function fn[mult] ∈ B2n;2n has two n-bit numbers x and y as inputs and computes the 2n-bit repre- sentation p of x y . | | · | |


###### We learnt in school how to multiply x and y . For each i we multiply yi by x, the result is zi = (zi;n−1 ; : : : ; zi;0) where zi;j = yi xj . By a shift
 which is gratis in circuits we compute |zi| 2[i] . Finally we add all |zi| 2[i]
 in order to compute the product of x and y . The computation of all zi;j can be done by n[2] gates in depth 1 . By divide-and-conquer we can add the n numbers in log n addition steps. With the efficient adders ⌈ ⌉ of 1 we obtain the following result. §

 LEMMA 2.1 : The school method for the multiplication implemented with efficient addition circuits leads to a circuit of size O(n[2]) and depth O(log[2] n) .

 The depth can be reduced by an easy trick due to Ofman (63) and Wallace (64). Since the addition of n-bit numbers requires depth Ω(log n), they used Carry Save Adder (CSA gates). CSA gates

; ;
###### have three n-bit numbers a b c as inputs and produce two (n + 1)-bit numbers u and v as outputs such that a + b + c = u + v . | | | | | | | | | |

 LEMMA 2.2 : CSA gates may be realized in size 5n and depth 3 .

 Proof : We use n fulladders. By the i -th fulladder we add ai, bi and ci and produce the sum bit ui and the carry bit vi+1 (0 ≤ i ≤ n − 1). Moreover un = v0 = 0 . Finally

 � � |a| + |b| + |c| = (ai + bi + ci) 2[i] = (ui + 2vi+1) 2[i] (2.1)

0 i n 1 0 i n 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_


-----

**52**


###### � � : = ui 2[i] + vi 2[i] = |u| + |v|

0 i n 0 i n
_≤_ _≤_ _≤_ _≤_


###### 2

 We improve the school method for multiplication by the application of this ingenious but nevertheless simple idea. The numbers zi again are computed with n[2] gates in depth 1 . The following CSA gates work on numbers whose length is bounded by 2n, thus all CSA gates have linear size and depth 3 . The number of summands is reduced by 1 by each CSA gate. Therefore n 2 CSA gates are sufficient to reduce − the number of summands from n to 2 . Finally we use Krapchenko’s adder to add these two summands. The resulting circuit has quadratic size. In order to reduce the depth we always use the largest possible number of CSA gates in parallel. If we still have 3k + i summands where i 0,1,2 we may reduce the number of summands to 2k + i ∈{ } by k parallel CSA gates. Let n0 = n and let nj be the number of summands after the j -th step. Obviously n1 ≤ 3[2][n+][ 2]3 [and by induction]


###### �2 ≤
 3


###### �2 �2 + + · · ·
 3


###### � 2 �2 3 [+] 3


j[�]
###### �


###### �j

:
###### n + 2 (2.2)
 ·


###### �2 nj ≤
 3


###### �j n +


###### � � � � For j = log3=2 n, we conclude nj 3 . So log3=2 n + 1 steps are ≤ sufficient to reduce the number of summands to 2 .

 THEOREM 2.1 : The school method for multiplication implemented with CSA gates and a Krapchenko adder leads to a circuit of size O(n[2]) and depth O(log n) .

 This multiplication circuit is asymptotically optimal with respect to depth. It is hard to imagine that o(n[2]) gates are sufficient for multiplication. Let us try a divide-and-conquer algorithm. Let n = 2[k]

; ;

###### and let x = (x[′] x[′′]) and y = (y[′] y[′′]) be divided into two parts of length

=
###### n 2 . Then


-----

**53**

###### p = x y = (2[n][=][2] x[′] + x[′′] ) (2[n][=][2] y[′] + y[′′] ) (2.3) | | | | | | | | | | | | | |

:
###### = 2[n] x[′] y[′] + 2[n][=][2] ( x[′] y[′′] + x[′′] y[′] ) + x[′′] y[′′] | | | | | | | | | | | | | | | |

=
###### In (2.3) we multiply four times numbers of length n 2 . The multi- plications by 2[n] or 2[n][=][2] are shifts which are gratis in circuits. Moreover we perform three additions which have linear size. For the size of the resulting circuit C[∗](n) we obtain the recursion

=
###### C[∗](n) 4 C[∗](n 2) + c[∗] n and C[∗](1) = 1 (2.4) ≤

 for some constant c[∗] . By Exercise 1 C[∗](n) = Θ(n[2]) and nothing has been gained. Karatsuba and Ofman (63) reduced the number of

=
###### multiplications of n 2-bit numbers from 4 to 3 . We compute |p1| = |x[′]| |y[′]|, |p2| = |x[′′]| |y[′′]| and |p3| = (|x[′]|+|x[′′]|) (|y[′]|+ |y[′′]|) . Now the term |x[′]| |y[′′]| + |x[′′]| |y[′]| can be obtained as |p3|− (|p1| +

=
###### |p2|) . We note that p3 is a product of two numbers of length n 2 + 1 . It is easy to see that C(n) C(n 1) + O(n) for the size C(n) of ≤ − multiplication circuits. Besides the three multiplications the circuit has by earlier results size O(n) and depth O(log n) . Altogether, since the multiplications can be done in parallel,

= ; = ;
###### C(n) 3 C(n 2) + O(n) D(n) D(n 2) + O(log n) (2.5) ≤ ≤

:
###### C(1) = D(1) = 1

 Obviously D(n) = O(log[2] n) and, by Exercise 1, C(n) = O(n[log 3]) .

 THEOREM 2.2 : Circuits for multiplication may have size O(n[log 3])

:
###### and depth O(log[2] n) . log 3 1 585 . ≈

 For sequential computations the school method of addition is op- timal whereas the school method of multiplication is not. Only for rather long numbers the multiplication method of Karatsuba and Of- man is better than the school method. The reader is asked to investi- gate exactly the following multiplication method M(k) . If n k, use ≤

        ###### the school method and, if n k, start with the method of Karatsuba and Ofman but solve subproblems for numbers with at most k bits by


-----

**54**

###### the school method. The optimal k is kopt = 17 . Since 2[20] ≈ 10[6], we have improved the school method for numbers of reasonable size.

 The depth of the Karatsuba and Ofman circuit can also be reduced to O(log n) . Such a reduction was easy for the school method by the use of CSA gates. Here we have to consider additions, subtractions and multiplications by powers of 2 . In the following we present a redundant representation of numbers where these operations can be

<
###### performed efficiently. We know that p 2[2n] and therefore we can | |

Z
###### compute |p| exactly if we perform our calculations modm, i.e. in m, for some m 2[2n] . The following representation of numbers has been ≥ investigated by Mehlhorn and Preparata (83).

Z Z
###### DEFINITION 2.2 : A radix-4 representation of x ∈ m, where m

; : : : ;

###### is a Fermat ring, i.e. m = 2[p] + 1 and p even, is a vector (xL 1 x0)
_−_

= �
###### such that L = p 2 + 1, −3 ≤ xi ≤ 3 and x = xi 4[i] .

0 i L 1
_≤_ _≤_ _−_


###### Radix-4 representations and computations in Fermat rings will also play an important role in a further multiplication method that we dis
; : : : ;

###### cuss later. The binary representation (x[′]p x[′]0[) of x can be under-]
 stood as a radix-4 representation by taking xi = x[′]2i [+ 2 x]2i+1[′] [. Obvi-] ously it is easy to change the sign in constant depth and linear size. Therefore we do not have to consider subtractions but only additions.

; : : : ; ; : : : ;

###### Let (xL 1 x0) and (yL 1 y0) be radix-4 representations of
_−_ _−_

###### x and y which we like to add. We start our computation similar to a CSA gate. We compute vi and ci such that xi + yi = vi + 4 ci . Since

; ; ; ;
###### −6 ≤ xi + yi ≤ 6, it is possible to choose vi ∈{−2 −1 0 1 2} and

; ;
###### ci ∈{−1 0 1} . The exact definition of vi and ci is given in Tab. 2.1.

 The trick is to represent 3 not as 0 4 + 3 1, but as 1 4 + ( 1) 1 . · · · − ·
 By this trick, −3 ≤ s[∗]i [= v][i][ +c][i][−][1][ ≤] [3 . If c][L][−][1][ = 0, we have computed]


###### by (s[∗]L 1
_−_


; : : : ;
###### s[∗]0[) a radix-4 representation of x + y . Otherwise we have]


###### to add s[∗], whose radix-4 representation is (s[∗]L 1
_−_


; : : : ;
###### s[∗]0[), and c][L][−][1][4][L][ .]


-----

**55**

|x + y i i|6 5 4 3 2 1 0 1 2 3 4 5 6 − − − − − −|
|---|---|
|v i c i|2 1 0 1 2 1 0 1 2 1 0 1 2 − − − − − 1 1 1 1 0 0 0 0 0 1 1 1 1 − − − −|


###### Tab. 2.1

 By definition,

 4[L] = 4 2[p] = 4 m 4 4 mod m (2.6) · − ≡−


; : : : ; ; ;
###### and (0 0 −cL−1 0) is a radix-4 representation of cL−1 4[L] mod m .


###### Either −3 ≤ s[∗]1 [−] [c][L][−][1][ ≤] [3 or c][L][−][1][ =][ −][1 and s]1[∗] [= 3 or c][L][−][1][ = 1 and]
 s[∗]1 [=][ −][3 . In the first case we obtain a radix-4 representation of x + y]


###### by (s[′]L 1
_−_


; : : : ;
###### s[′]0[) where s][′]1 [= s]1[∗] [and s][′]i [= s]i[∗] [for all other i . In the]
 [−] [c][L][−][1]


###### other cases we have to work harder. In our description of the algorithm

 we use if-tests which are not possible in circuits. In circuits we have to

 perform the computations for both situations and at the end to select

 the right result (such a selection has been described in detail in 1 for §


###### the Conditional Sum Adder). If |s[∗]1 [−] [c][L][−][1][|][ = 4, we add (s]L[∗] −1


; : : : ;
###### s[∗]0[)]


; : : : ; ; ;
###### and (0 0 cL 1 0) by the same procedure as we started to add − −


###### (xL 1
_−_


; : : : ; ; : : : ;
###### x0) and (yL 1 y0) . We claim that the procedure stops.
_−_


###### Since |s[∗]1 [−] [c][L][−][1][|][ = 4, we get v]1[∗] [= 0 and][ |][c]0[∗][| ≤] [1 . Therefore we]


; : : : ;

###### obtain the vector (s[∗∗]L−1 s[∗∗]0 [) where][ |][s]1[∗∗][|][ =][ |][v]1[∗] [+ c]0[∗][| ≤] [1 . Since]


###### |c[∗]L−1[| ≤] [1, it is not possible that][ |][s]1[∗∗][−][c]L[∗] −1[|][ = 4 . Hence (s][∗∗]L−1


; : : : ;
###### s[∗∗]2 [,]


###### s[∗∗]1 L 1
 [−] [c][∗] −


;
###### s[∗∗]0 [) is a radix-4 representation of x + y .]


-----

**56**

###### We also have to consider the computation of a radix-4 represen- tation for x 2[s] mod m . A multiplication by a power of 2 consists of a multiplication by a power of 4 and, if necessary, a multiplication by 2, i.e. an addition. That is why we consider only the computation of x 4[r] mod m . Since 4[L] 4 mod m, as already shown, ≡−
 x 4[r] ≡ � xh−r 4[h] + � xL−r+h 4[h](−4) mod m (2.7)

r h L 1 0 h r 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_


###### for 0 r L 1 . Therefore it is sufficient to add the radix-4 represen- ≤ ≤ −

; : : : ; ; ; : : : ; ; : : : ; ; ; : : : ; ;

###### tations (xL 1 r x0 0 0) and (0 0 xL 1 xL r 0) .
_−_ _−_ _−_ _−_ _−_ _−_

###### Finally we consider the transformation of a radix-4 representation

; : : : ;

###### (xL 1 x0) of some number x into its binary representation. Let
_−_

; ; ; ;

###### x[+]i = max{xi 0} and x[−]i = min{xi 0} . Let (x[+]i;1 x[+]i;0[) and (x]i[−];1 x[−]i;0[)]
 be the binary representation of x[+]i and −x[−]i resp. We obtain the binary representation of x by an ordinary subtraction of x[+] and x[−]

; ; : : : ; ;

###### which have the binary representations (x[+]L 1;1 x[+]L 1;0 x[+]0;1 x[+]0;0[) and]
_−_ _−_

; : : : ;

###### (x[−]L 1;1 x[−]0;0[) . We summarize our results.]
_−_

###### THEOREM 2.3 : The binary representation of x is also a radix-4 representation of x . Numbers in radix-4 representation can be added, subtracted and can be multiplied by a power of 2 with circuits of linear size and constant depth. Furthermore, they can be transformed into binary representation in linear size and logarithmic depth.

 Since the recursion depth of the Karatsuba - Ofman algorithm is log n, we obtain the following improvement of Theorem 2.2.

 THEOREM 2.4 : The Karatsuba and Ofman algorithm for multi- plication can be implemented such that the resulting circuit has size O(n[log 3]) and depth O(log n) .

 In the rest of this section we present a circuit for multiplication due to Sch¨onhage and Strassen (71). The circuit simultaneously has size O(n log n log log n) and depth O(log n) . No multiplication circuit of


-----

**57**

###### smaller size is known. The problem whether multiplication circuits of linear size exist or whether multiplication is harder than addition with respect to circuit size is still open. Unfortunately the multiplication circuit beats the other circuits only for very long numbers. These long numbers are interesting for special applications, e.g. public key cryptosystems. The algorithm is recursive, so we should solve small subproblems with other methods.

 To ensure that the subproblems are of the same type as the initial

;
###### problem, we make the following assumptions. n = 2[k], 0 x y ≤| | | | ≤ 2[n], and we are only interested in p mod (2[n] + 1) . We obtain the | |

=
###### correct result if we start with n 2-bit numbers. In the following we do

;
###### not distinguish between x and x . Also we assume that x y 2[n] 1 . | | ≤ − The cases x = 2[n] or y = 2[n] are easy and are treated in parallel. At the end the correct result is selected. Since 2[n] 1 mod (2[n] + 1), ≡− 2[n]y 2[n] + 1 y mod (2[n] + 1) and we only have to subtract y from ≡ −

;
###### 2[n] + 1 . If x y 2[n] 1, their binary representations have length n . ≤ −
 After these preliminary remarks we discuss the ideas of the multi- plication method of Sch¨onhage and Strassen. While it is obvious that for the multiplication of polynomials we have to multiply numbers, it is interesting to see that the multiplication of numbers can be done by the multiplication of polynomials. We partition x and y into b blocks

; : : : ; ; : : : ;

###### of l bits each, i.e. x = (xb 1 x0) and y = (yb 1 y0), where
_−_ _−_

; ;

###### xi yi ∈{0 1}[l] . The parameters are chosen as


=
###### b = 2[⌊][k][=][2][⌋] and l = n b = 2[⌈][k][=][2][⌉]


:
###### (2.8)


###### Let f(z) = � xi z[i] and g(z) = � yi z[i] be polynomials. By

0 i b 1 0 i b 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_

###### definition x = f(2[l] ) and y = g(2[l]), thus p = x y = h(2[l] ) where h = f g . Therefore we can multiply x and y by multiplying the polynomials f and g and evaluating h at 2[l] . How can we compute the coefficients vk of h ? By the law of distributivity vk is the sum of all xi yj where i + j = k .


-----

**58**

; : : : ;

###### DEFINITION 2.3 : The convolution v = (v2b 2 v0) of x =
_−_

; : : : ; ; : : : ;

###### (xb 1 x0) and y = (yb 1 y0) is given by
_−_ _−_


###### � vk = xi yj
 ·
i+j=k


:
###### (2.9)


###### If we compute all vk by (2.9) we have to perform b[2] multiplications of l -bit numbers. Since bl = n, this is no improvement to previous methods. The following trick is convenient. By the fundamental the- orem of algebra a polynomial f of degree d 1 is uniquely determined − by the value of f at d different inputs. For the sake of simplicity we treat h as a polynomial of degree 2b 1 . Altogether we may multiply − the polynomials f and g by evaluating f and g at 2b different inputs

; : : : ;

###### a1 a2b, by computing h(ai) = f(ai) g(ai) and by computing the

; : : : ;
###### coefficients of h from h(a1) h(a2b) .

; : : : ;
###### Later we shall see that the computation of f(a1) f(a2b) can be

; : : : ;

###### done very efficiently if we choose the right values for a1 a2b . In
 the second step we have to perform 2b multiplications. The method can only be efficient if the numbers to be multiplied are much shorter than x and y . Sch¨onhage and Strassen observed that the length of the numbers can be reduced by Chinese Remaindering (explained later in this section) and that the number of multiplications can be reduced to b by replacing the convolution by its negative envelope.

; : : : ;

###### DEFINITION 2.4 : The negative envelope w = (wb 1 w0) of the
_−_

###### convolution v of x and y is given by


###### � � wi = xj · yi−j − xj · yb+i−j

0 j i i<j b 1
_≤_ _≤_ _≤_ _−_


:
###### (2.10)


###### If we define v2b−1 = 0, we obtain the following connection between the convolution and its negative envelope, wi = vi vb+i . Now we are − able to present the main steps of the multiplication algorithm.


-----

**59**


###### ALGORITHM 2.1 : We use the notation introduced above.
 Step 1 : Compute wi[′] [= w][i][ mod (2][2][l][ + 1) for 0][ ≤] [i][ ≤] [b][ −] [1 .] (This will be done by the recursive procedure we have discussed.)
 Step 2 : Compute wi[′′] [= w][i][ mod b for 0][ ≤] [i][ ≤] [b][ −] [1 .] (This will be done directly.)
 Step 3 : Compute wi from wi[′] [and w]i[′′] [for 0][ ≤] [i][ ≤] [b][ −] [1 .] (This will be done by Chinese Remaindering.)

; : : : ;

###### Step 4 : Compute p, the product of x and y, from (wb 1 w0) .
_−_

###### (This will be done by standard methods.)

 We still have to work hard to implement the four steps of the algorithm efficiently. At first we discuss the efficiency of the algorithm. In Step 1 we perform recursively b multiplications of numbers of length 2l . These multiplications are done in parallel. All other work will be done by a circuit of size O(bl log b) = O(n log n) and depth O(log n) . So we obtain a circuit of size C(n) and depth D(n), where

 C(n) b C(2l ) + O(n log n) and (2.11) ≤

:
###### D(n) D(2l ) + O(log n) (2.12) ≤

 Since l (2n)[1][=][2], it is easy to show that D(n) = O(log n) . For ≤

=
###### C[′](n) = C(n) n we obtain by (2.11)

:
###### C[′](n) 2 C[′](4 n[1][=][2]) + O(log n) (2.13) ≤

 Now it is not difficult (though a little bit tedious) to prove C[′](n) = O(log n log log n) and C(n) = O(n log n log log n) .

 For the implementation we do the easier steps first. Why is it sufficient to compute the negative envelope of the convolution ?


###### LEMMA 2.3 : p ≡ � wi 2[i][ l] mod (2[n] + 1) .

0 i b 1
_≤_ _≤_ _−_


-----

**60**

###### Proof : We have already seen that


###### � p = h(2[l] ) = vi · 2[i][l]

0 i 2b 1
_≤_ _≤_ _−_


;
###### (2.14)


###### where v2b−1 = 0 . Since wi = vi − vb+i, it is sufficient to prove that vb+i · 2[(b+i)][l] equals −vb+i · 2[i][l] mod (2[n] + 1) . This is obvious since 2[b][l] = 2[n] 1 mod (2[n] + 1) . 2 ≡−

 By (2.10) we can estimate wi by


###### (b 1 i) 2[2][l] − − − ·


<
###### wi


<
###### (i + 1) 2[2][l] ·


:
###### (2.15)


###### Therefore wi mod (b(2[2][l] +1)) is sufficient for the unique identification of wi . The length of a radix-4 representation of wi mod (b(2[2][l] + 1)) is O(l log b) . We have to add b numbers, therefore the depth is bounded by O(log n) . We estimate the length of the numbers. In particular, we do not add w0 2[0][l] and wb−1 2[(b][−][1)][l] at the beginning, but always ˝neigh- boring˝ numbers. After the j -th addition step we have computed sums of 2[j] ˝neighboring˝ numbers. Due to the structure of the numbers wi 2[i][l] the length of these O(b 2[−][j]) sums is O(l log b+2[j]l ) . The number of gates of the j -th addition step is bounded by O(2[−][j]n log n+n) . Sum
; : : : ;
###### ming up for j 0 log n, the size is bounded by O(n log n) . ∈{ ⌈ ⌉} We now have computed the sum p[∗] of all wi 2[i][l] . It is necessary to

<

###### compute p ≡ p[∗] mod (2[n] + 1) . Since wi b(2[2][l] + 1), p[∗] ≤ 2[3n] .
 We partition the binary representation of p[∗] to three blocks of length n each, i.e. p[∗] = p2 2[2n] + p1 2[n] + p0 . Since 2[n] ≡−1 mod (2[n] + 1), p ≡ p2 − p1 + p0 mod (2[n] + 1) . We compute p[′] = p2 − p1 + p0 . Obvi
<

###### ously 2[n] p[′] 2[n+1] . We compute p[′], p[′] + 2[n] + 1 and p[′] (2[n] + 1) − ≤ −

; : : : ;
###### and select the number in 0 2[n] as p . Altogether we have imple- { } mented Step 4 efficiently.

 For the implementation of Step 3 we make use of the Chinese Re- mainder Theorem which we prove in its general form. In 3 we apply § the theorem in its general form.


-----

**61**

; : : : ;

###### THEOREM 2.5 (Chinese Remainder Theorem) : Let m1 mk be

: : : ; : : : ;
###### relatively prime and m = m1 · · mk . For given a1 ak there is a

; : : : ;
###### unique a ∈{0 m − 1} such that a ≡ ai mod mi for all i . This a is given by


###### a ≡ � ai · ri · si mod m (2.16)

1 i k
_≤_ _≤_


= =
###### where ri = m mi and si (m mi)[−][1] mod mi ≡


:


###### Proof : It is an easy fact from elementary number theory that si is well

=
###### defined, since mi and m mi are relatively prime. Since mj is a factor

=
###### of m mi if i ̸= j, ri ≡ 0 mod mj . By definition ri si ≡ 1 mod mi . So a ≡ ai mod mi . The uniqueness of the solution is easy to prove too. If a and b are solutions, a − b ≡ 0 mod mi . Because of the relative

; ; : : : ;
###### primality of all mi even a − b ≡ 0 mod m . Since a b ∈{0 m − 1}, we conclude a = b . 2

 Here we like to compute wi mod (b(2[2][l] + 1)) from wi[′] [≡] [w][i][ mod] (2[2][l] + 1) and wi[′′] [≡] [w][i][ mod b . Since b is a power of 2, b and 2][2][l][ + 1] are relatively prime. We claim
 wi = wi[′] [+ (2][2][l][ + 1)[(w]i[′′] i[) mod b]][:] (2.17)
 [−] [w][′]

 By the Chinese Remainder Theorem it is sufficient to investigate wi mod b and wi mod (2[2][l] + 1) . The second number equals wi[′] [. Since] b 2[2][l], 2[2][l] 0 mod b . Therefore the right-hand side of (2.17) mod ≤ ≡ b is equal to wi[′′] [. By (2.17) all w][i][ can be computed in size O(n log n)] and depth O(log n) . Also Step 3 is implemented efficiently.
 The computation of all wi ≡ wi mod b is rather easy since b is rather small. Since b is a power of 2 we know x[′]i [≡] [x][i][ mod b and y]i[′] [≡] yi mod b . We hide all computations in a multiplication of long but not � � too long numbers. Let f[′](z) = x[′]i [z][i][ and g][′][(z) =] yi[′] [z][i][ .]

0 i b 1 0 i b 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_

###### For m = 3 log b let x[′′] = f[′](2[m]) and y[′′] = g[′](2[m]) . x[′′] is the sequence

; : : : ;

###### x[′]b−1 [, 2 log b zeros, x]b[′] −2 2 log b zeros, x[′]0 [, similarly for y][′′][ . By]


-----

**62**

###### Theorem 2.4 we may compute x[′′] y[′′] = f[′] g[′](2[m]) by a circuit of size
 · O((b log b)[log 3]) = o(n log n) and depth O(log(b log b)) = O(log n) . By definition of the convolution vector v[′] of x[′] and y[′] we know that � ; : : : ; < f[′] g[′](2[m]) = vk[′] [2][mk][ . Since x]i[′] yi[′] [∈{][0][;] b − 1}, 0 ≤ vk[′]

0 k 2b 1
_≤_ _≤_ _−_

###### b[3] = 2[m] . Thus f[′] g[′](2[m]) contains all vk[′] [as substrings. Now it is easy] to compute efficiently all wi[′′] i b+i[) mod b .]
 [≡] [(v][′] [−] [v][′]


###### The most difficult part is the computation of all wi[′] [≡] [w][i][ mod (2][2][l][ +] 1) in Step 1. Here we use the recursive procedure discussed at the beginning. The ideas for the computation of the negative envelope of convolution are discussed here in the general situation that vectors

; : : : ; ; : : : ;

###### a = (a0 an−1) and b = (b0 bn−1) are given. ai and bi are
 elements of a commutative ring with a one. The negative envelope

; : : : ;

###### w = (w0 wn 1) is defined similarly to (2.10). We like to evaluate

_−_
###### the polynomials f and g whose vectors of coefficients are a and b, resp., at 2n (for the convolution) or n (for the negative envelope) different inputs. The naive procedure has Θ(n[2]) arithmetic operations. By choosing the inputs carefully we get by with only O(n log n) arithmetic operations.

 This so-called Fast Fourier Transform has already been described by Runge and K¨onig (24) and has been rediscovered for computer

; ; : : : ;

###### science by Cooley and Tukey (65). As inputs we choose r[0] r[1] r[n][−][1]


###### where r is an n-th root of identity.

 DEFINITION 2.5 : r is an n-th root of identity in a commutative ring R with one if r = 1, r[n] = 1 and � r[jk] = 0 for 1 k n 1 . ̸ ≤ ≤ −

0 j n 1
_≤_ _≤_ _−_

###### First of all we prove the existence of roots of identity in some Fermat rings.


-----

**63**

###### LEMMA 2.4 : Let n and r = 1 be powers of 2 and m = r[n][=][2] + 1 . ̸

Z
###### Then r is an n-th root of identity in m and n[−][1] and r[−][1] are defined

Z
###### in m .

 Proof : The existence of n[−][1] and r[−][1] again follows from elementary number theory, since n and r are relatively prime to m . By definition r = 1 . Since r[n][=][2] 1 mod m, r[n] 1 mod m . For the last condition ̸ ≡− ≡ we prove by induction on p = log n
 � � :
 r[jk] = (1 + r[2][i][k]) (2.18)
0 j n 1 0 i p 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_

###### This claim is obvious for p = 1 . The induction step follows from the following elementary calculation
 � �
 r[jk] = (1 + r[k]) (r[2])[jk] (2.19)
0≤j≤n−1 0≤j≤(n=2)−1

###### = (1 + r[k]) � (1 + (r[2])[2][i][ k]) = � (1 + r[2][i][ k]):

0 i p 2 0 i p 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_

###### Now it is sufficient to prove that one of the factors 1+r[2][i][ k] 0 mod m . ≡

<
###### Let k = 2[s] k[′] and k[′] odd. Then 0 s p . Furthermore, if i = ≤

=
###### p 1 s, 2[i] k = 2[p][−][1][−][s] 2[s] k[′] = k[′] n 2 . Since r[n][=][2] 1 mod m, − − ≡− 1 + r[2][i][ k] (1 + ( 1)[k][′]) 0 mod m. 2 ≡ − ≡

 Later we apply the Fast Fourier Transform for m = 2[2][l] + 1 and n = b . Since l = b or l = 2b, the existence of a b-th and a 2b-th root of identity is guaranteed and so is the existence of b[−][1], (2b)[−][1]
 and r[−][1] .


; : : : ;

###### DEFINITION 2.6 : Let a = (a0 an 1) R[n] and let r be an

_−_ _∈_
###### n-th root of identity in R . Let f be the polynomial of degree n whose

; : : : ;

###### coefficients are a0 an−1 . The Discrete Fourier Transform DFTn(a)

; : : : ;
###### is given by f(r[0]) f(r[n][−][1]) . � In particular fj := f(r[j]) = ai r[ij] .

0 i n 1
_≤_ _≤_ _−_


-----

**64**

###### DFTn can be written as matrix vector product of the matrix A, whose elements are r[ij], and the column vector a .

 THEOREM 2.6 : The Discrete Fourier Transform DFTn(a) can be

; ;
###### computed by an arithmetic circuit ( + -circuit) of size O(n log n) { − ∗} and depth O(log n) .

 Proof : This efficient algorithm again is based on divide-and-conquer and on the properties of roots of identity.

 � fj = ai r[ij] = (2.20)

0 i n 1
_≤_ _≤_ _−_

###### = � a2i (r[2j])[i] + r[j] � a2i+1 (r[2j])[i] :

0 i (n=2) 1 0 i (n=2) 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_


; ; : : : ;

###### Instead of evaluating f at r[0] r[1] r[n][−][1] we may evaluate the polynomi
; ; : : : ; ; ; : : : ; ; ; : : : ;

###### als given by (a0 a2 an 2) and (a1 a3 an 1) at r[0] r[2] r[2n][−][2] .

_−_ _−_

###### Since r[n] = 1, it is even sufficient to evaluate both polynomials of de
= ; ; : : : ;
###### gree (n 2) 1 at r[0] r[2] r[n][−][2] . Since it is easy to prove that r[2] is −
 an (n =2 )-th root of identity, we may compute DFTn=2(a0 ; a2 ; : : : ; an 2)

_−_
###### and DFTn=2(a1 ; a3 ; : : : ; an 1) by the same procedure. To start with we

_−_

; ; : : : ;

###### compute r[0] r[1] r[n][−][1] . Afterwards we may compute fj with two fur ther operations. The preprocessing, the computation of all r[i], can be done in linear size and logarithmic depth. The problem is not harder than the prefix problem (see 1). For the complexity of the other § computations we obtain the following recurring relations

= = :
###### C(n) 2 C(n 2) + 2n and D(n) D(n 2) + 2 (2.21) ≤ ≤

 Here we took advantage of the fact that the two subproblems and afterwards the computation of all fj can be done in parallel. By (2.21) the claim of the theorem follows. 2

 Now we know how to evaluate polynomials efficiently at certain inputs. We have already discussed that we also like to compute ef- ficiently the coefficients of a polynomial given by its values at these


-----

**65**

###### well-chosen inputs. DFTn(a) = Aa is a matrix vector product. If A[−][1]
 exists, DFT[−]n [1][(b) = A][−][1][b is the inverse Discrete Fourier Transform.] If b = DFTn(a), also a = DFT[−]n [1][(b).]

 LEMMA 2.5 : If n[−][1] and r[−][1] exist, then A[−][1] exists also, and its elements are n[−][1]r[−][ij] .

 Proof : We prove that the product of A = (r[ij]) and B = (n[−][1]r[−][ij]) is the identity matrix. � The elements of AB are given by n[−][1] r[ik] r[−][jk] . If i = j, this

0 k n 1
_≤_ _≤_ _−_

    - <
###### equals 1. For i j (the case i j is analogous)
 � r[ik] r[−][jk] = � r[(i][−][j)k] = 0 (2.22)

0 k n 1 0 k n 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_

###### by the last property of roots of identity. 2

 Since r[−][1] also is an n-th root of identity (it is easy to check the three properties) we obtain the following corollary.

 COROLLARY 2.1 : The inverse Discrete Fourier Transform DFT[−]n [1][(a) can be computed by an arithmetic circuit of size O(n log n)] and depth O(log n) .

 Now we combine our observations and compute the negative enve- lope of convolution.


###### THEOREM 2.7 : Let R be a commutative ring with a one, a =

; : : : ; ; ; : : : ; ; : : : ; ; ; : : : ;

###### (a0 an 1 0 0), b = (b0 bn 1 0 0) R[2n], r be an n-th

_−_ _−_ _∈_

###### root of identity such that r[−][1] and n[−][1] exist.
 i) DFT[−]2n[1][(DFT][2n][(a)][∗][DFT][2n][(b)), where][ ∗] [is the componentwise mul-] tiplication, is the convolution of a and b .
 ii) Let s be a (2n)-th root of identity and r = s[2] .

; ; : : : ; ; ; : : : ;

###### Let a[∗] = (a0 s a1 s[n][−][1] an 1), b[∗] = (b0 s b1 s[n][−][1] bn 1) and

_−_ _−_


-----

**66**


; ; : : : ; ; : : : ;

###### w[∗] = (w0 s w1 s[n][−][1] wn 1) where w = (w0 wn 1) is the

_−_ _−_

; : : : ; ; : : : ;

###### negative envelope of a = (a0 an 1) and b = (b0 bn 1) .

_−_ _−_

###### Then w[∗] = DFT[−]n [1][(DFT][n][(a][∗][)][ ∗] [DFT][n][(b][∗][)) .]

 Proof : Part i) is a formal description of the algorithm for the compu- tation of the convolution already discussed. At first both polynomials are evaluated at the same 2n inputs. Then the product polynomial is evaluated at these inputs, and finally the coefficients of the product polynomial are computed.


; : : : ; ; : : : ;

###### For Part ii) let (f0 fn 1) = DFTn(a[∗]), (g0 gn 1) = DFTn(b[∗])

_−_ _−_

; : : : ;

###### and (h0 hn 1) be the vector claimed to be equal to w[∗] . Then by

_−_
###### definition

 hm = n[−][1] � fi gi r[−][im] (2.23)

0 i n 1
_≤_ _≤_ _−_


###### � = n[−][1]

0 i n 1
_≤_ _≤_ _−_


###### �

0 j n 1
_≤_ _≤_ _−_


###### �
 s[j] aj s[k] bk r[(j+k][−][m)i]
0 k n 1
_≤_ _≤_ _−_


###### � �
 � � � : = s[j+k] aj bk n[−][1] r[(j+k][−][m) i]
 ·

0 j n 1 0 k n 1 0 i n 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_ _≤_ _≤_ _−_

###### If j + k = m or j + k = m + n the inner sum is 1, since r[n] = 1 . Otherwise the inner sum is 0 . Therefore


###### � hm = s[m] � aj bk + s[n] � aj bk

j+k=m j+k=n+m


###### �


###### (2.24)


###### = s[m] (vm − vn+m) = s[m] wm


:


###### Here we used the fact that s[n] = r[n][=][2] = 1 . 2 −

 We apply Theorem 2.7. ii for the computation of all wi[′] [≡] [w][i][ mod]

Z
###### (2[2][l] +1) . We work in the Fermat ring m where m = 2[2][l] +1 . The roots of identity and the multiplicative inverses we need are well-defined. In our application n is replaced by b, a power of 2 . Also the (2b)-th root of identity s and the b-th root of identity r = s[2] can be chosen by


-----

**67**

###### Lemma 2.4 as power of 2 . Since r[b] = s[2b] = 1, also r[−][1] = r[b][−][1], s[−][1] = s[2b][−][1] and b[−][1] = 2[−⌊][k][=][2][⌋] = r[b] 2[−⌊][k][=][2][⌋] can be chosen as power of 2 . Using radix-4 representations all additions and all multiplications by a power of 2 have size O(l ) and constant depth. By Theorem 2.6, Corollary 2.1 and Theorem 2.7 we have to perform O(b log b) of these operations and b multiplications of numbers of 2l bits. These b multiplications can be done in parallel. The depth of the other operations is O(log b) = O(log n) . Since O(bl log b) = O(n log n), the algorithm of Sch¨onhage and Strassen fulfils the complexity estimations of (2.11) and (2.12). We have proved the following result.

 THEOREM 2.8 : The algorithm of Sch¨onhage and Strassen leads to a circuit for multiplication of size O(n log n log log n) and depth O(log n) .

 3.3 Division

= =
###### Since y z = y(1 z), we consider only the computation of the in- verse z[−][1] . In general the binary expansion of z[−][1] is not finite, e.g. for z = 3 . So we are satisfied with the computation of the n most

= <
###### significant bits of z[−][1] . W.l.o.g. 1 2 z 1 . ≤

 DEFINITION 3.1 : The division function fn[div] ∈ Bn−1;n has

; ; : : : ;
###### (zn−1 = 1 zn−2 z0) as input.

= = =
###### For z = 1 2 zn−1 + (1 2)[2] zn−2 + · · · + (1 2)[n] z0 the n most significant
 bits of z[−][1] build the output of fn[div] .

 The school method of division produces the output bits one after

; : : : ;

###### another. The divisor always is (zn 1 z0), the ˝actual˝ dividend
_−_


-----

**68**

; ; : : : ;
###### changes. At first the dividend is (1 0 0) . During one step we subtract the divisor from the dividend if the divisor is not larger than the dividend. If the divisor is not larger the next output bit is 1, otherwise 0 . We obtain the new dividend by multiplying (in the first case) the result of the subtraction or (in the second case) the old dividend by 2 . By our previous results we are able to estimate the efficiency of the school method.

 THEOREM 3.1 : The school method of division leads to a circuit of size O(n[2]) and depth O(n log n) .

 The depth of such a circuit cannot be accepted. Anderson, Earle, Goldschmidt and Powers (67) presented a circuit of depth O(log[2] n) . At the beginning of 2 we have reduced the multiplication of two § numbers to the addition of n numbers. Here we reduce division to

< =
###### repeated multiplication. Let x = 1 z . Then 0 x 1 2 and by − ≤ the binomial formula we obtain the following basic relation where x(j) stands for x[2][j] .

 1 1 1
 (3.1)
 z [=] 1 x [=] 1 x 1 + x(0) 1 + x(1) 1 + x(k 1) [=]
 − − [·][ 1 + x(0)] [·][ 1 + x(1)] [· · ·][ 1 + x(k] −[ −] [1)]
 Pk(x)

:

###### =
 1 x(k) −


=
###### Since x 1 2, the denominator is approximately 1 . We compute ≤ approximations for all x(j), afterwards an approximation P[∗]k[(x) for]

<
###### Pk(x) . Since 1 z[−][1] ≤ 2, we may take the n most significant bits of P[∗]k[(x) as output bits if]


###### |P[∗]k[(x)][ −] [z][−][1][| ≤] [2][−][n+1]


:
###### (3.2)


###### We compute x[∗](j) by computing the first s bits of (x[∗](j 1))[2] following −
 the binary point. Similarly we compute P[∗]j [(x) by computing the first]
 s bits of P[∗]j 1[(x)][ ·][ (1 + x][∗][(j][ −] [1)) following the binary point. How large]
_−_

###### do we have to choose s and k such that P[∗]k[(x) fulfils (3.2) ?]


-----

**69**

###### Let δ = 2[−][s] . In each step we are rounding off the result by at most δ . Since the old errors are squared, the errors are growing slowly.

 LEMMA 3.1 : x(j) 2 δ x[∗](j) x(j) . − ≤ ≤

 Proof : The second inequality is obvious since we are only rounding off the results. The first inequality is proved by induction.

= =
###### For j = 0 the assertion is obvious. Since x 1 2, x(j) 1 4 for j 1 ≤ ≤ ≥ and 4 δ x(j) δ . By induction hypothesis ≤
 x[∗](j + 1) x[∗](j)[2] δ (x(j) 2 δ)[2] δ x(j)[2] 4 δ x(j) δ ≥ − ≥ − − ≥ − −

:
###### x(j + 1) 2 δ (3.3) ≥ −

 2

 LEMMA 3.2 : Pj(x) − εj(x) ≤ P[∗]j [(x)][ ≤] [P][j][(x)]

=
###### where εj(x) = (3j − 2) δ (1 − x(j − 1)) (1 − x) .

 Proof : Again the second inequality is obvious. Since ε1(x) = δ and P1(x) = 1 + x, the first inequality holds for j = 1 . Since we are rounding off the results by at most δ, we can conclude by induction hypothesis and Lemma 3.1 that

 P[∗]j [(x)][ ≥] [P]j[∗]−1[(x) (1 + x][∗][(j][ −] [1))][ −] [δ] (3.4)
 (Pj 1(x) εj 1(x)) (1 + x(j 1) 2 δ) δ ≥ − − − − − −
 Pj 1(x) (1 + x(j 1)) εj 1(x) (1 + x(j 1)) ≥ − − − − −

:
###### 2 δ Pj 1(x) δ − − −

<
###### The first term is equal to Pj(x). Since x(j − 1) x(j − 2),

< =
###### εj 1(x)(1 + x(j 1)) (3 j 5) δ (1 x(j 2))(1 + x(j 2)) (1 x)
_−_ _−_ _−_ _−_ _−_ _−_ _−_

= :
###### = (3 j 5) δ (1 x(j 1)) (1 x) (3.5) − − − −

=
###### Furthermore by definition 2 δ Pj 1(x) = 2 δ(1 x(j 1)) (1 x) and
_−_ _−_ _−_ _−_


-----

**70**

< =
###### δ δ (1 x(j 1)) (1 x) . By these estimations, (3.4) and (3.5) − − −

   - = :
###### P[∗]j [(x)] Pj(x) − (3 j − 2)(1 − x(j − 1)) (1 − x) = Pj(x) − εj(x)
 (3.6)

 2

 We combine our estimations. By the triangle inequality

 |z[−][1] − P[∗]k[(x)][| ≤|][z][−][1][ −] [P][k][(x)][|][ +][ |][P][k][(x)][ −] [P][∗]k[(x)][|][:] (3.7)

 By (3.1)

 |z[−][1] − Pk(x)| = |z[−][1] − (1 − x(k)) z[−][1]| (3.8)

= :
###### = x(k) (1 x) 2 2[−][2][k] − ≤ ·


###### By Lemma 3.2

 |Pk(x) − P[∗]k[(x)][| ≤] [ε][k][(x)][ ≤] [(3 k][ −] [2)][ ·][ 2][ ·][ 2][−][s]


:
###### (3.9)


###### (3.8) and (3.9) can be estimated by 2[−][n] if we choose

:
###### k = log n + 1 and s = n + 3 + log k (3.10) ⌈ ⌉ ⌈ ⌉
 By this choice |z[−][1] − P[∗]k[(x)][| ≤] [2][−][n+1][ and we may output the n most] significant bits of P[∗]k[(x). Altogether we perform one subtraction and] 2k 2 multiplications of (s+1)-bit numbers which have to be performed − sequentially.

 THEOREM 3.2 : The algorithm of Anderson et al. leads to a circuit for division which has depth O(log[2] n) and size O(n[2] log n) (if we use convential multiplication circuits) or size O(n log[2] n log log n) (if we use Sch¨onhage and Strassen multiplication circuits).

 For several years one believed, that depth O(log[2] n) is necessary for division circuits. Reif (83) was the first to beat this bound. Generaliz- ing the ideas of Sch¨onhage and Strassen (see 2) to the multiplication § of n numbers he designed a division circuit of polynomial size and


-----

**71**

###### depth O(log n log log n) . Afterwards Beame, Cook and Hoover (84) applied methods of McKenzie and Cook (84) and proved that the depth of division is Θ(log n) .
 One-output circuits of depth d have at most 2[d] 1 gates. Therefore − circuits of depth O(log n) always have polynomial size. Since the new division circuit beats the older ones only for rather large n, we do not estimate accurately the depth of the new circuit. Because of the approximation algorithm introduced at the beginning of this section, it is sufficient to prove that n n-bit numbers may be multiplied in depth O(log n) . Then we can compute all x[∗](j) in parallel in depth O(log n) and afterwards we multiply all 1 + x[∗](j) in depth O(log n) .

 For the basic results of number theory that we apply the reader is referred to any textbook on number theory, e.g. Ayoub (63). For our algorithm it is crucial that problems for small numbers may be solved

; ; : : : ; ;

###### efficiently by table-look-up. Let T be a table (a1 b1) (aN bN)
 where N and the length of each ai are bounded by a polynomial in n .

; : : : ;

###### If all ai are different, we may compute for x ∈{a1 aN} in depth
 O(log n) that bi which has the same index as x = ai . Obviously we can test in depth O(log n) whether x = aj . Let cj = 1 iff x = aj . All cj can be computed in parallel. Afterwards all ym where ym is the m-th output bit, can be computed in parallel as disjunction of all cj ∧ bjm (1 ≤ j ≤ N). Here bjm is the m-th bit of bj . Altogether the circuit has depth O(log n) . In general, tables of functions f have exponential length and table-look-up is not very efficient.

 By table-look-up circuits we multiply the input numbers modulo small prime numbers. By the Chinese Remainder Theorem these prod- ucts are sufficient to compute the product exactly. The size of the product is bounded by M = (2[n] 1)[n] . Therefore it is sufficient to −

            ###### compute the product mod m for some m M . We describe the main steps of our algorithm before we discuss their efficient implementation.

 ALGORITHM 3.1 :

; : : : ;

###### Input : x1 xn, n n-bit numbers.


-----

**72**

###### Output : x, the product of all xi, as binary number.
 Step 1 : Choose the smallest r such that p, the product of the r

; : : : ;

###### smallest primes p1 pr, is larger than M .
 Step 2 : Compute yij ≡ xi mod pj for all 1 ≤ i ≤ n and 1 ≤ j ≤ r .
 � � Step 3 : Compute x[j] ≡ yij ≡ xi mod pj for 1 ≤ j ≤ r .

1 i n 1 i n
_≤_ _≤_ _≤_ _≤_

###### Step 4 : Use the Chinese Remainder Theorem to compute x (or x mod p, which is the same) from all x[j] .


###### The computations in Step 1 depend only on the input length which is fixed for circuits. All pi and p can be computed in advance and are inputs of the circuit. Since pi ≥ 2, r ≤ n[2] . Better estimations of r can be computed by the prime number theorem. Likewise by the prime

; : : : ;

###### number theorem pmax = max{p1 pr} is bounded by a polynomial
 q(n) .

 The computation of all yij in Step 2 can be done in parallel. All ajk 2[k] mod pj are independent of the input and can be computed in ≡ advance, i.e. all ajk are inputs of the circuit. Let xik be the k -th bit of xi . Then


###### � � xi = xik 2[k] ≡ xik ajk mod pj

0 k n 1 0 k n 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_


:
###### (3.11)


;
###### Since xik ∈{0 1}, all xik ajk can be computed in depth 1 . As we already know (see § 2), the sum sij of all xik ajk can be computed in

<

###### depth O(log n) . Since 0 ≤ sij npj, we may compute a table of all

<
###### sij − l pj for 0 ≤ l n in depth O(log n) . By table-look-up we choose

; : : : ;
###### that sij − l pj which lies in {0 pj − 1} and is therefore equal to yij .

 In Step 3 we take advantage of some properties of prime numbers.

; : : : ;
###### Gj = {1 pj − 1} is a cyclic group with respect to multiplication modpj . This implies the existence of a generator g ∈ Gj such that for

; : : : ;
###### all k ∈ Gj there exists a unique index ind(k) ∈{0 pj − 2} with respect to g and Gj such that


-----

###### k ≡ g[ind(k)] mod pj


**73**

:
###### (3.12)


###### At first we test in parallel whether some yij = 0 (1 ≤ i ≤ n). In this case x[j] = 0 . Otherwise we compute x[j] in the following way. The

;
###### table (k ind k) for 1 ≤ k ≤ pj − 1 (with respect to g and Gj) does not depend on the input and is computed in advance. By table-look-up we compute in parallel in depth O(log n) all ind(yij) . Afterwards we compute in parallel in depth O(log n) all I(j), where I(j) is the sum

<
###### of all ind(yij) . Since 0 ≤ I(j) n(pj − 1), we can compute in parallel in depth O(log n) all I[∗](j) ≡ I(j) mod (pj − 1) . These computations are done similarly to the computation of yij from sij in Step 2. It is an easy fact from elementary number theory that g[p][′][−][1] 1 mod p[′] for ≡ prime numbers p[′] . Therefore


###### � � x[j] ≡ yij ≡ g[ind(y][ij][)] ≡ g[I(j)] ≡ g[I][∗][(j)] mod pj

1 i n 1 i n
_≤_ _≤_ _≤_ _≤_


:
###### (3.13)


###### Finally we can compute x[j] from I[∗](j) by table-look-up. Instead of multiplying all yij, it is sufficient to add all ind(yij), and we know already that the sum of n numbers can be computed efficiently.

 By the Chinese Remainder Theorem 2.5

 � x ≡ x[j] rj mod p (3.14)

1 j n
_≤_ _≤_


= =
###### where rj = ujvj, uj = p pj and vj (p pj)[−][1] mod pj . The numbers ≡ rj do not depend on the input and can be computed in advance. We

< <

###### multiply in parallel all x[j] and rj . Since 0 ≤ x[j] pj and 0 ≤ rj p,
 these multiplications have depth O(log n) as has the addition of all

<

###### x[j] rj . Obviously, 0 ≤ x[∗] p n pmax for the sum x[∗] of all x[j] rj, and x can
 be computed from x[∗] in depth O(log n) similarly to the computation of yij from sij in Step 2.

 Altogether we obtain an efficient implementation of Algorithm 3.1.

 THEOREM 3.3 : The algorithm of Beame, Cook and Hoover leads to a division circuit of depth O(log n) and polynomial size.


-----

**74**

###### It is still an open problem whether one can design a division circuit whose depth is bounded by c log n for a small constant c and whose size is acceptable.

 The methods for the design of the division circuit may also be applied to the approximation of power series. The computation of the n most significant bits of e.g. e[x] or ln x is possible in depth O(log n) (Alt (84)).

 3.4 Symmetric functions

 The class of symmetric functions contains many fundamental func- tions like sorting and all types of counting functions.

 DEFINITION 4.1 : Sn;m is the class of all symmetric functions f ∈ Bn;m, that is all functions f such that for all permutations π ∈ Σn

; : : : ; ; : : : ;

###### f(x1 xn) = f(xπ(1) xπ(n)) .


;
###### Each vector a 0 1 with exactly i ones is a permutation of ∈{ }[n] any other vector with exactly i ones. That is why f is symmetric iff f only depends on the number of ones in the input. For symmetric

;
###### functions we may shorten the table (a f(a)) for f to the (value) vector

; : : : ;

###### v(f) = (v0 vn) such that f(x) = vi if x1+· · ·+xn = i . We introduce
 some fundamental symmetric functions.

 DEFINITION 4.2 :
 i) E[n]k[(x) = 1 iff x][1][ +][ · · ·][ + x][n][ = k (exactly - k - function).]


###### ii) T[n]k[(x) = 1 iff x][1][ +][ · · ·][ + x][n][ ≥] [k (threshold - k - function).]

: : : ;
###### iii) S[n](x) = (T[n]1[(x)][;] T[n]n[(x)) (sorting function).]
 iv) C[n]k;m[(x) = 1 iff x][1][ +][ · · ·][ + x][n][ ≡] [k mod m (counting function).]


-----

**75**

###### If the input length (and upper index) n is uniquely determined by the context, then we can omit n . The term sorting function for S[n] is justified, since for inputs x with exactly k ones T1(x) = · · · = Tk(x) = 1 but Tk+1(x) = · · · = Tn(x) = 0 . The output is the sorted sequence

; : : : ;

###### of the inputs. The functions E0 En build a kind of basis for all
 symmetric functions, since for all f ∈ Sn


###### f(x) = � Ek(x) ∧ vk

0 k n
_≤_ _≤_


:
###### (4.1)


###### v0


; : : : ;
###### vn are constants independent from the input, thus


; : : : ;

###### C(f) ≤ C(E0 En) + n and (4.2)

; : : : ; :

###### D(f) ≤ D(E0 En) + ⌈log(n + 1)⌉ (4.3)


###### Furthermore Tk = Ek En . Because of the algorithms for the ∨· · · ∨

; : : : ;

###### prefix problem (see § 1) we can compute S[n] from E1 En by a circuit
 of linear size and logarithmic depth.

 Due to these observations it is essential to design an efficient circuit

; : : : ;

###### for the computation of E0 En . At first we compute with n − 2
 CSA gates and one Krapchenko adder the binary representation a =

; : : : ;

###### (ak−1 a0) of x1 + · · · + xn . Here k = ⌈log(n + 1)⌉ . The depth of
 this circuit is O(log n) . The length of the summands is 1 .

 At step j of the adder-tree the inputs of the CSA gates are of length j, hence the CSA gates have size O(j) . The number of CSA gates at step j may be estimated by [1] � 2�j−1 n . Since the sum of all

3 3

###### � 2�j−1
 j is a constant, the size of the adder-tree is O(n) .
3

###### Ei(x) = 1 iff the number |a| represented by a is equal to i . There
; : : : ; ; : : : ;

###### fore Ei(x) is a minterm on ak−1 a0 . We compute E0 En by

; : : : ;

###### the computation of all minterms on ak−1 a0 .

; : : : ;

###### LEMMA 4.1 : All minterms on x1 xn can be computed by a
 circuit of size 2[n] + O(n 2[n][=][2]) and depth O(log n) .


###### Proof : O(n 2[n][=][2]) gates are sufficient to compute in parallel all 2[⌈][n][=][2][⌉]


###### minterms on x1 ; : : : ; x n=2 and all 2[⌊][n][=][2][⌋] minterms on x n=2 +1

_⌈_ _⌉_ _⌈_ _⌉_


; : : : ;
###### xn .


-----

**76**

; : : : ;

###### Afterwards each of the 2[n] minterms on x1 xn can be computed
 with one gate. 2


; : : : ;

###### By this lemma E0 En can be computed from a in linear size
 and logarithmic depth since k = log(n + 1) . Altogether we obtain ⌈ ⌉ an efficient circuit for all symmetric functions.

 THEOREM 4.1 : Each symmetric function f ∈ Sn with one output as well as the sorting function may be computed by a circuit of size O(n) and depth O(log n) .

 The proof of Theorem 4.1 is due to Muller and Preparata (75) though the result has been proved implicitly already by Lupanov (62 a). By Theorem 4.1 we have designed efficient circuits for sev- eral fundamental functions.

 3.5 Storage access

 DEFINITION 5.1 : The storage access function SAn Bn+k where ∈

; : : : ;

###### n = 2[k] is defined on a k-bit number a = (ak 1 a0) and n variables
_−_

; : : : ; ;

###### x = (x0 xn−1) . SAn(a x) = x|a| .


###### We consider a storage of n memory cells containing the 1-bit in
; : : : ;

###### formations x0 xn−1 . The vector a contains the number of the

;
###### memory cell whose contents is interesting for us. SAn(a x) computes the contents of this memory cell. Bit ak−1 decides whether we should


-----

**77**


###### search in the first or in the second half of the memory. Therefore


;
###### x0


###### SAn(ak 1
_−_


; : : : ;
###### a0


; : : : ;
###### xn 1) = (5.1)
_−_


###### = (ak 1 SAn=2(ak 2
_−_ _∧_ _−_


; : : : ;
###### a0


; xn=2


; : : : ;
###### xn 1))
_−_ _∨_


###### (ak 1 SAn=2(ak 2 ∨ − ∧ −


; : : : ;
###### a0


;
###### x0


; : : : ; x(n=2) 1)):
_−_


###### Since SA1(x0) = x0, (5.1) leads to a circuit for SAn of size C(n) and depth D(n) where

= ; = ;
###### C(n) = 2 C(n 2) + 3 D(n) = D(n 2) + 2 (5.2)

:
###### C(1) = D(1) = 0

 The solution of this recurring relation is C(n) = 3n 3 and D(n) = − 2 log n .

 LEMMA 5.1 : The storage access function SAn can be computed by a circuit of size 3n 3 and depth 2 log n . −

 In Ch. 5 we prove a lower bound of 2n 2 for the circuit size of − SAn . Klein and Paterson (80) proved that this lower bound is nearly optimal.
 Let Mi(a) be the minterm of length k computing 1 iff |a| = i . Obviously


###### SAn(a; x) = � Mi(a) ∧ xi

0 i n 1
_≤_ _≤_ _−_


:
###### (5.3)


###### In order to beat the (3n 3)-bound of Lemma 5.1 we partition a − into two halves b = (ak 1 ; : : : ; a k=2 ) and c = (a k=2 1 ; : : : ; a0) . Then
_−_ _⌊_ _⌋_ _⌊_ _⌋−_

###### a = b 2[⌊][k][=][2][⌋] + c . For r = 2[⌈][k][=][2][⌉] and s = 2[⌊][k][=][2][⌋] we conclude from | | | | | | (5.3) by the law of distributivity that

 SAn(a; x) = � � Mi(b) ∧ Mj(c) ∧ xis+j (5.4)

0 i r 1 0 j s 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_

###### � �
 = � Mi(b) ∧ � Mj(c) ∧ xis+j :

0 i r 1 0 j s 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_


-----

**78**

###### By Lemma 4.1 we can compute all Mi(b) and all Mj(c) by a circuit of

=
###### size r+s+o(r+s) = O(n[1][=][2]) and depth log(k 2) = log log n 1 . For ⌈ ⌉ ⌈ ⌉− the computation of all Mj(c) ∧ xis+j n ∧-gates and n − r ∨-gates are
 [�]

=
###### sufficient, the depth of this part of the circuit is k 2 +1 . Afterwards ⌊ ⌋ SAn(a,x) can be computed by r ∧-gates and r − 1 ∨-gates in depth

=
###### k 2 + 1 . This way we have proved ⌈ ⌉

 THEOREM 5.1 : The storage access function SAn can be computed by circuits of size 2n + O(n[1][=][2]) and depth log n + log log n + 1 . ⌈ ⌉

 3.6 Matrix product

 For the sake of simplicity we consider here only square matrices of n rows and n columns. As it is well known the matrix product of two matrices of integers or reals is defined by


###### � zij = xik ykj

1 k n
_≤_ _≤_


:
###### (6.1)


; ;
###### We investigate arithmetic circuits ( + -circuits, straight line pro- { − ∗} grams) for the computation of Z = (zij) . Arithmetic circuits lead to Boolean circuits if we replace each arithmetic operation by a Boolean circuit of suitable input size for this operation. Furthermore we are in- terested in the Boolean matrix product which is useful in graph theory (see Exercises). Here we consider matrices X = (xij) and Y = (yij) of ones and zeros only. The Boolean matrix product Z = (zij) is defined by


###### � zij = xik ykj
 ∧
1 k n
_≤_ _≤_


:
###### (6.2)


###### Obviously the Boolean (arithmetic) matrix product can be computed with n[3] conjunctions (multiplications) and n[3] n[2] disjunctions (ad- − ditions) in depth log n + 1 . Strassen (69) proved in his pioneering ⌈ ⌉


-----

**79**

###### paper that this school method is not optimal for the arithmetic matrix product. His arithmetic circuit has size O(n[log 7]) and depth O(log n) . Arlazarov, Dinic, Kronrod and Faradzev (70) designed an arithmetic

=

###### circuit of size O(n[3] log n) that only works for 0-1-matrices but is bet ter than the school method also for very small n . For 9 years no one improved Strassen’s algorithm. Then a violent development started. Its end was the arithmetic circuit of Coppersmith and Winograd (82)

< :
###### whose size is O(n[c]) for some c 2 496 . Pan (84) gives a survey on this development. Now Strassen (86) improved the exponent to some

< :
###### c 2 479 . We describe here only Strassen’s classical algorithm and point out how the computation of the Boolean matrix product may be improved by this algorithm too.

 Strassen’s algorithm depends on divide-and-conquer. Again we

=
###### assume n = 2[k] . We partition X, Y and Z into four matrices of n 2

=
###### rows and n 2 columns each.


###### �


###### �


###### �


###### � Y11 Y12 Y21 Y22


;
###### Z =


###### � Z11 Z12 Z21 Z22


###### X =


###### � X11 X12 X21 X22


;
###### Y =


:


###### It is easy to see that the submatrices Zij may be computed similarly to the product of 2 × 2-matrices, e.g. Z12 = X11Y12 +X12Y22 . Here ad
= =
###### ditions and multiplications are operations on (n 2) (n 2)-matrices. × By the school method we perform 8 matrix multiplications and 4 ma- trix additions. The addition of two n n-matrices obviously can be × performed with n[2] additions in depth 1 while multiplications seem to be harder.

 By our experience with divide-and-conquer algorithms we should try to get by with less than 8 multiplications. It was a long way from this knowledge to the following algorithm. Though it is diffi- cult to discover such an algorithm, it is easy to check its correctness. We describe the 7 multiplications of the algorithm, but before these multiplications we have to perform 10 additions and subtractions to compute the factors.


-----

**80**


; ;
###### m1 = (X12 − X22) · (Y21 + Y22) m2 = (X11 + X22) · (Y11 + Y22)


;
###### m3 = (X11 − X21) · (Y11 + Y12) m4 = (X11 + X12) · Y22

; ;
###### m5 = X11 (Y12 Y22) m6 = X22 (Y21 Y11) · − · −


;
###### (6.3)


###### m7 = (X21 + X22) · Y11


:


###### Now it is easy to verify that


###### �


###### Z =


###### � m1 + m2 m4 + m6 m4 + m5 − m6 + m7 m2 m3 + m5 m7 − −


:
###### (6.4)


###### Let C(n) and D(n) be the size and depth resp. of Strassen’s arithmetic circuit. Then


= =
###### C(n) = 7 C(n 2) + 18(n 2)[2]

 C(1) = D(1) = 1

 implying


; = ;
###### D(n) = D(n 2) + 3 (6.5)


###### THEOREM 6.1 : Strassen’s algorithm leads to an arithmetic circuit for matrix multiplication of size 7n[log 7] 6n[2] and depth 3 log n + 1 . −

:
###### (log 7 2 81) . ≈

 We emphasize that Strassen’s algorithm as well as Karatsuba and Ofman’s multiplication algorithm is based on additions, multiplica- tions and subtractions. If only additions and multiplications (of posi- tive numbers) are admissible operations, then the school method can- not be improved (see Ch. 6). The profitable use of subtractions for a problem where subtractions seem to be superfluous should be taken as a warning. One should be very careful with stating that certain operations are obviously not efficient for certain problems.

 Fischer and Meyer (71) applied Strassen’s algorithm to Boolean matrix multiplication. Similar results for the other matrix multipli- cation methods have been obtained by Lotti and Romani (80) and Adleman, Booth, Preparata and Ruzzo (78).


-----

**81**

;

###### The inputs of the Boolean matrix product are numbers xij yij ∈

;
###### {0 1} . Let zij be the Boolean matrix product and z[∗]ij [the conventional] matrix product. Obviously

;
###### 0 ≤ z[∗]ij [≤] [n][;] z[∗]ij [is an integer] and (6.6)

:
###### z[∗]ij [= 0] ⇔ zij = 0

 Strassen’s algorithm consists of additions, substractions and multipli- cations. Therefore, by (6.6), we can compute z[∗]ij [correctly if we perform]

Z        ###### all computations in m for some m n . In particular, the length of the numbers is O(log n) . Finally all zij, by (6.6) the disjunction of all bits of z[∗]ij [, can be computed in parallel in depth O(log log n) . Since all] multiplications of Strassen’s agorithm can be done in parallel, we may estimate the complexity of the new algorithm for the Boolean matrix product by our results of 1 and 2. § §

 THEOREM 6.2 : The Boolean matrix product can be computed in size O(n[log 7] log n log log n log log log n) and depth O(log n) .

 3.7 Determinant

 In Ch. 9 we consider the simulation of programs by circuits in gen- eral. Here we investigate as a second example the computation of the determinant (the first one was the Boolean matrix product). The well known algorithm based on Gaussian elimination whose time complex- ity is O(n[3]) can be simulated by a circuit of size O(n[3]) . Gaussian elimination is a typical sequential algorithm, so we need additional tricks to reduce the depth.


###### DEFINITION 7.1 : The determinant of a Boolean n n-matrix X × with respect to the field Z2 is detn(X) = [�] x1;π(1) · : : : · xn;π(n) .

_π∈Σn_


-----

**82**

###### ALGORITHM 7.1 (Gaussian elimination) (see e.g. MacLane and Birkhoff (67)) :

 1. det(x11) = x11 .

 2. If the first column of X consists of zeros only, detn(X) = 0 .

Z
###### 3. The componentwise addition (in 2) of one row of X to another does not change the determinant of the matrix. If the first column of X contains a one, e.g. xm;1 = 1, we add the m-th row to all other rows starting with a one. We obtain a matrix X[′] with a single one in the first column and detn(X) = detn(X[′]) .

 4. By expansion according to the first column of X[′] we eliminate the first column and the m-th row and obtain an (n 1) (n 1)- − × − matrix X[′′] where detn 1(X[′′]) = detn(X) .
_−_

###### THEOREM 7.1 : detn may be computed by a circuit of size 3n[3] + n[2] 4n. −

 Proof : We simulate the Gaussian elimination algorithm. Let X =

; ; : : : ;

###### X[n] X[n][−][1] X[1] be the matrices constructed by the algorithm. Since
 X[i] has i columns and i rows, we can test with i 1 gates whether − the first column of X[i] contains zeros only (gi = 0) or at least a one (gi = 1). detn(X) = g1 · · · · · gn can be computed with n − 1 gates.
 We only have to describe how to compute X[k][−][1] from X[k] = (yij) . We may assume that gk = 1, otherwise detn(X) = 0 will be computed

; : : : ;

###### correctly independent from gk−1 g1 . um = y11∧· · ·∧ym−1;1∧ym1 =
 1 iff the m-th row of X[k] is the first one starting with a one. All

; : : : ;

###### u1 uk can be computed by 2k − 3 gates (if k ≥ 2) . We use these

; : : : ;

###### pointers for selecting v = (v1 vk), the first row of X[k] starting with
 a one. Obviously vj, the disjunction of all uryrj, can be computed by

Z
###### 2k − 1 gates. v is added (componentwise in 2) to all rows of X[k]
 starting with a one. Since we eliminate afterwards the first column we


-----

**83**

###### do not compute this column. We compute

;
###### zij = yi1 ∧ yij ∨ (yi1 ∧ (vr ⊕ yij)) (1 ≤ i ≤ k 2 ≤ j ≤ k) (7.1)

 by altogether 4k (k 1) gates. Finally we have to eliminate the m- −

; : : : ;

###### th row where um = 1 . Let t1 = u1 and tj = tj−1 ∨ uj . t1 tk−1
 can be computed by k − 2 gates. Then t1 = · · · = tm−1 = 0 while tm = · · · = tk−1 = 1 . Therefore the elements yij[∗] [of X][k][−][1][ can be] computed by

 yij[∗] [= t][i][ z][ij][ ∨] [t][i][ z][i+1][;][j] (7.2)

 by 3 (k 1)[2] gates. Altogether the number of gates for the computation − of gk and X[k][−][1] from X[k] equals

 (k 1) + (2k 3) + k (2k 1) + 4k (k 1) + (k 2) + 3 (k 1)[2] − − − − − −

;
###### = 9k[2] 7k 3 (7.3) − −

 and the number of gates in the whole circuit equals

:

###### n 1 + (9k[2] 7k 3) = 3n[3] + n[2] 4n (7.4) − − − −
 [�]

2 k n
_≤_ _≤_

###### 2

 EXERCISES

=
###### 1. Prove that the recursion relation R(n) = a R(n b) + cn, R(1) = c

      - ;      ###### for n = b[k], b 1, a c 0 has the solution R(n) = Θ(n), if

<  ###### a b, R(n) = Θ(n log n), if a = b, R(n) = Θ(n[log][b][ a]), if a b .

 2. The Carry-Look-Ahead Adder partitions the input bits into g(n) groups of nearly the same size. If we know the carry bit for some group we add the bits of this group using the school method and we compute directly by (1.8) the carry bit for the next group. Estimate size and depth of this adder.


-----

**84**

###### 3. The Carry-Look-Ahead Adder of second order adds the bits of a group by a Carry-Look-Ahead Adder (of first order). Estimate size and depth of this adder.

 4. Estimate size and depth of the Conditional-Sum Adder, if the numbers are partitioned into a) 3 b) k parts of nearly the same size.

 5. Design efficient circuits for the transformation of an integer given by its sign and the binary representation of its absolute value into its 2-complement representation and vice versa.

 6. Design efficient circuits for subtraction.

=
###### 7. The adder tree of n − 2 CSA gates has at least depth log3=2(n 2) .

 8. Investigate the mixed multiplication algorithm M(k) .

 9. Two complex numbers can be multiplied with only three multipli- cations of reals and some additions and subtractions.

 10. Let X and Y be independent random variables that take the value

; : : : ;
###### k ∈{0 n − 1} with probability pk and qk resp. Compute the distribution of X + Y, the so-called convolution of X and Y .

R
###### 11. has only for n = 2 an n-th root of identity.

=n

C
###### 12. e[i 2][π] is an n-th root of identity in .

 13. Design an efficient circuit for the computation of x 2[−][k], where x is given by a radix-4 representation.


-----

**85**

###### 14. Solve the recurring relations (2.11) and (2.12).

 15. Design a circuit for division based on Newton’s approximation method.

; ; ; ; ; ;
###### 16. Multiply (0 1 0), (1 0 1) and (1 1 1) by the method of Beame, Cook and Hoover.

=
###### 17. For f ∈ Sn (4.1) consists either for f or for f of at most (n + 1) 2 summands.

:
###### 18. Design a circuit for f ∈ Sn whose size is bounded by 11 5 n + o(n) .

 19. Prove a good upper bound on C(f) for f ∈ Sn;m .


; : : : ;

###### 20. Estimate the size of the circuit for (E0 En) in § 4 as exact as
 possible.

; : : : ; ;
###### 21. Let G(x) = ( 1 n E(x)) be a graph defined by the variables { }

< ;
###### xij (1 ≤ i j ≤ n), i.e. {i j} ∈ E(x) iff xij = 1 . X[k], the k -th Boolean power of matrix X = (xij) (where xij = xji and xii = 1)

;
###### contains a one at position (i j) iff G(x) contains a path from i to j of length bounded by k .

 22. Design an efficient circuit for the decision whether the graph G(x) is connected.

 23. Implement Strassen’s algorithm for arbitrary n and compute the number of arithmetic operations.

 24. Compute the number of arithmetic operations of the following

                  ###### algorithm A(l ) for matrix multiplication. Let n = 2[k] . If k l the


-----

**86**

###### algorithm applies Strassen’s method. Problems and subproblems of size m 2[l] are solved by the school method. (See Mehlhorn (77) ≤ for a discussion of A(l ) .)

 25. Design for f ∈ Bn;n where fi(x) is the conjunction of all xj (i ̸= j) a circuit of size not larger than 3n 6 . −


###### 26. f(x1


; : : : ;
###### xn


;
###### y1


; : : : ; �
###### yn) = xi yj has linear circuit size

1 i;j n; i j m
_≤_ _≤_ _|_ _−_ _|≤_


###### for all m .


###### 27. f(x1


; : : : ;
###### xn) = x1 ∨ (x2 ∧ (x3 ∨ (· · · ))) has logarithmic depth.


;
###### 28. Design efficient circuits for f g ∈ Sn where

;
###### f(x) = 1 if x1 + · · · + xn mod 4 ∈{1 3}

; :
###### g(x) = 1 if x1 + · · · + xn mod 5 ∈{1 3}


-----

**87**

###### 4. ASYMPTOTIC RESULTS AND UNIVERSAL CIRCUITS

 4.1 The Shannon effect

 For many fundamental functions we have designed efficient circuits. Is it possible to compute each function by an efficient circuit ? In this chapter we prove that almost all functions are hard functions, optimal circuits for almost all functions have exponential size and linear depth. This can be proved quite easily using Shannon’s counting argument (Shannon (49)). The number of circuits with small circuit size or small depth grows much slower than the number of different Boolean functions implying that almost all functions are hard. This means that a random Boolean function is hard with very large probability. We obtain a random Boolean function by 2[n] independent coin tosses with an unbiased coin, for each input a the output f(a) is determined by one of the coin tosses. By this experiment we can expect a Boolean function that has no recognizable structure. This lack of structure implies that the function is hard. The converse is not correct. We shall see later that certain functions whose structure is easy to describe are (probably) hard. Hence, the structure of our fundamental functions is only a necessary condition for the existence of efficient circuits.

 In this chapter we investigate the complexity of almost all func- tions, or equivalently, the expected complexity of a random function. It turns out that almost all functions have nearly the same complex- ity as the hardest function. This effect is called Shannon effect by Lupanov (70).

 DEFINITION 1.1 : The notion ˝almost all functions f of a class Fn Bn have property P ˝ stands for the assertion that ⊆

= :
###### |{f ∈ Fn | f has P}| |Fn| → 1 as n →∞ (1.1)


-----

**88**

###### DEFINITION 1.2 : For a complexity measure CM and a class of func- tions Fn we denote by CM(Fn) the complexity of the hardest functions in Fn, i.e. max{CM(f)|f ∈ Fn} .

 DEFINITION 1.3 : The Shannon effect is valid for a class of functions Fn and a complexity measure CM if CM(f) ≥ CM(Fn) − o(CM(Fn)) for almost all f ∈ Fn .

 We prove that the Shannon effect is valid for several classes of Boolean functions and complexity measures. With Shannon’s count- ing argument we prove that almost all functions are hard, i.e. their complexity is at least an o(an) for some large an . Then we design − circuits (or formulas) for all functions whose complexity is bounded by an .
 For almost all functions we obtain nearly optimal circuits. These circuits may be used for f ∈ Bn if we have no idea of designing a better circuit for f . In Ch. 3 we have seen that we can design much more efficient circuits for many fundamental functions.

 4.2 Circuits over complete bases

 In order to apply Shannon’s counting argument we estimate the number of B2-circuits of size b .

; =
###### LEMMA 2.1 : At most S(b n) = (b + n + 1)[2b] 16[b] b b! functions f ∈ Bn can be computed by B2-circuits of size b .

 Proof : We estimate the number of B2-circuits of size b . For each gate there are |B2| = 16 possibilities to choose its type and b + n + 1 possi- bilities to choose each of its two predecessors, namely the other b 1 − gates, n variables and 2 constants. Each B2-circuit computes at most


-----

**89**

###### b different functions at its gates. Finally we take into account that each circuit is counted b! times, namely for b! different numberings of its gates. Altogether we obtain the claimed bound. 2

 If b = b(n) = C(Bn), |Bn| functions in Bn can be computed by a B2
;
###### circuit of size b . By Lemma 2.1 we can conclude S(b n) ≥|Bn| . We

;
###### use this inequality for an estimation of b . When considering S(b n)

;
###### and |Bn| as functions of n we see that S(b n) is exponential while |Bn|

;
###### is even double exponential. Since S(b n) as a function of b is also only exponential, b = b(n) grows exponentially. We now estimate b more exactly. By Stirling’s Formula b! c b[b+1][=][2] e[−][b] for some constant ≥

 ###### c 0 and thus

;
###### log S(b n) ≥ log |Bn| ⇒ (2.1)
 2b log(b + n + 1) + 4b + log b


=
###### (b + 1 2) logb + b log e log c 2[n] − − ≥

 For n sufficiently large, b n + 1 and therefore ≥


:


=
###### b log b + (6 + log e)b + (1 2) logb log c 2[n] − ≥

 If b 2[n]n[−][1], we could conclude ≤


:
###### (2.2)


=
###### 2[n]n[−][1](n log n + 6 + log e) + (1 2)(n log n) log c 2[n] (2.3) − − − ≥

 which for large n is false. Therefore

:
###### C(Bn) ≥ 2[n]n[−][1] for sufficiently large n (2.4)

 We can prove even more. If we consider a subclass B[∗]n [of B][n][ such that]
 log |B[∗]n[| ≥] [2][n][ −] [2][n][n][−][1][ log log n =: a(n)]
 we can prove in the same way that C(B[∗]n[)][ ≥] [2][n][n][−][1][ for sufficiently large] n. In particular, we may choose B[∗]n [as the class of those 2][a(n)][ functions] in Bn of the smallest circuit size.


-----

**90**

###### THEOREM 2.1 : For sufficiently large n at least |Bn|(1 − 2[−][r(n)]) of the |Bn| functions in Bn, where r(n) = 2[n] n[−][1] log logn, have circuit size at least 2[n] n[−][1] . In particular, almost all f ∈ Bn have circuit size at least 2[n] n[−][1] .

 We now show that 2[n] n[−][1] + o(2[n] n[−][1]) gates are sufficient for the computation of an arbitrary f ∈ Bn . At first we present two less efficient circuits. The first one is called decoding circuit. Let f0 Bn 1 ∈ − and f1 ∈ Bn−1 be the subfunctions of f ∈ Bn for xn = 0 and xn = 1 resp. Obviously

 f = (xn ∧ f0) ∨ (xn ∧ f1) (2.5)

 implying

;
###### C(Bn) 2C(Bn 1) + 3 C(B2) = 1 and (2.6) ≤ −

:
###### C(Bn) ≤ 2[n] − 3 (2.7)

 We note that decoding circuits are even formulas. Decoding circuits can be improved in the following simple way. In a decoding circuit we compute all 2[n][−][3] subfunctions in B3 in disjoint subcircuits. It is much more efficient to compute all 2[8] functions in B3 in advance. Let C[∗](Bk) be the circuit complexity for the computation of all functions in Bk . By (2.5)

 C[∗](Bk) C[∗](Bk 1) + 3 Bk and (2.8) ≤ − | |

;
###### C[∗](B2) ≤ 16 hence


###### C[∗](Bk) ≤ 3 · 2[2][k] + 6 · 2[2][k][−][1]


:
###### (2.9)


###### For the computation of f we compute at first all functions in Bk . The decoding circuit for f can stop after n k steps, since all necessary − subfunctions are already computed. Similarly to (2.7) 3 2[n][−][k] 3 gates
 · − are sufficient to compute f if the functions in Bk are given. Hence


-----

**91**

###### C(Bn) ≤ 3(2[n][−][k] + 2[2][k]) + 6 · 2[2][k][−][1] for arbitrary k . (2.10)

 For k = log n 1 ⌈ ⌉−

:
###### C(Bn) ≤ 12 · 2[n] n[−][1] + o(2[n] n[−][1]) (2.11)

 These simple ideas already lead to circuits whose size is for almost all Boolean functions only by a factor of 12 larger than the size of an optimal circuit. In order to eliminate the factor 12, we have to

;
###### work harder. Lupanov (58) introduced the so-called (k s) - Lupanov representation of Boolean functions. We represent the values of f by a

; : : : ;

###### table of 2[k] rows for the different values of (x1 xk) and 2[n][−][k] columns

; : : : ;

###### for the different values of (xk+1 xn) . The rows are partitioned to
 � ; : : : ; ; : : : ; p = 2[k] s[−][1][�] ≤ 2[k] s[−][1] + 1 blocks A1 Ap such that A1 Ap−1
 contain s rows and Ap contains s[′] ≤ s rows. We try to find simpler functions than f and to reduce f to several of these simpler functions.

; : : : ;

###### Let fi(x) = f(x) if (x1 xk) ∈ Ai and fi(x) = 0 otherwise. Obviously
 f = f1 fp . ∨· · · ∨
 Let Bi;w be the set of columns whose intersection with Ai is equal to w ∈{0; 1}[s] (for i = p, w ∈{0; 1}[s][′]) and let fi;w(x) = fi(x) if (xk+1 ; : : : ; xn) ∈ Bi;w and fi;w(x) = 0 otherwise. Obviously f is the
 disjunction of all fi;w . Now consider the 2[k] × 2[n][−][k] table of fi;w . All rows outside of Ai consist of zeros only, the rows of Ai have only two different types of columns, columns w and columns of zeros only. We represent fi;w as the conjunction of fi[1];w [and f]i[2];w [where f]i[1];w[(x) = 1 iff for]

; : : : ;

###### some j wj = 1 and (x1 xk) is the j -th row of Ai, and fi[2];w[(x) = 1]
 iff (xk+1 ; : : : ; xn) ∈ Bi;w . Altogether we obtain Lupanov’s (k; s)-repre sentation


; : : : ;
###### xk) ∧ fi[2];w[(x][k+1]


###### � fi[1];w[(x][1]

w


###### f(x1


; : : : ; xn) = �

1 i p
_≤_ _≤_


; : : : ; :
###### xn) (2.12)


###### We may compute f now in the following way.


-----

**92**

###### Step 1 : By Lemma 4.1, Ch. 3, we compute with O(2[k] + 2[n][−][k]) gates

; : : : ; ; : : : ;

###### all minterms on {x1 xk} and on {xk+1 xn} .
 Step 2 : We compute all fi[1];w [by their DNF, the minterms are already] computed. Since the blocks Ai are disjoint, each minterm is used at most once for fixed w . Altogether 2[s] 2[k] gates are sufficient.
 Step 3 : We compute all fi[2];w [by their DNF, the minterms are already] computed. Since the blocks Bi;w are disjoint for fixed i, each minterm is used once for fixed i . Altogether p 2[n][−][k] gates are sufficient.
 Step 4 : By (2.12) 2 p 2[s] gates are sufficient to compute f if all fi[1];w [and] fi[2];w [are given.]

 The number of gates of our circuit can be estimated, since p ≤ 2[k] s[−][1] + 1, by


###### O(2[k] + 2[n][−][k]) + 2[s+k] + 2[n] s[−][1] + 2[n][−][k] + 2[k+s+1] s[−][1] + 2[s+1]

 We choose k = 3 log n and s = n 5 log n . ⌈ ⌉ −⌈ ⌉


:
###### (2.13)


###### THEOREM 2.2 : C(f) ≤ 2[n] n[−][1] + o(2[n] n[−][1]) for all f ∈ Bn .

 By Theorem 2.1 and Theorem 2.2 we have proved that the Shannon effect is valid for Bn and B2-circuit size. Lupanov’s circuits are nearly optimal and for almost all Boolean functions much better than min- imal polynomials, i.e. optimal circuits of 2 logical levels. Lupanov’s circuits have only 4 logical levels.


-----

**93**

###### 4.3 Formulas over complete bases

 We proceed as in 2. §

;
###### LEMMA 3.1 : At most F(b n) = (n + 2)[b+1] 16[b] 4[b] functions f ∈ Bn can be computed by B2-formulas of size b .

 Proof : We estimate the number of B2-formulas of size b . W.l.o.g. the last gate is the only one without successor and the output is computed at the last gate. As already discussed in Ch. 2 B2-formulas are binary trees if we copy the variables and constants. There exist less than 4[b]
 binary trees with b inner nodes. For each gate starting at the root of the tree we have for each of the two predecessors at most the two possibilities of choosing an inner node or a leaf. Each gate is labelled by one of the 16 functions of B2 . Finally each of the b + 1 leaves is labelled by one of the n variables or the 2 constants. Altogether we obtain the claimed bound. 2

;
###### If b = b(n) = L(Bn), log F(b n) ≥ log |Bn| implying


###### (b + 1) log(n + 2) + 6b 2[n] ≥


:
###### (3.1)


###### (3.1) is not fulfilled for b = 2[n] log[−][1] n(1 (log log n)[−][1]) and suffi- − ciently large n . The same estimation holds for classes B[∗]n [where]
 [⊆] [B][n] log |B[∗]n[|][ = 2][n][(1][ −] [log][−][1][ n) .]

 THEOREM 3.1 : For sufficiently large n at least |Bn|(1 − 2[−][s(n)]) of the |Bn| functions in Bn, where s(n) = 2[n] log[−][1] n, are of formula size at least 2[n] log[−][1] n(1 − (log log n)[−][1]) . In particular, almost all f ∈ Bn are of formula size at least 2[n] log[−][1] n(1 (log log n)[−][1]) . −

 We already proved in § 2 an upper bound of 2[n] − 3 on L(Bn) . By


-----

**94**

;
###### Lupanov’s (k s)-representation we shall obtain for each f ∈ Bn a B2- formula with 6 logical levels and (2 + o(1))2[n] log[−][1] n gates. Since in formulas all gates have fan-out 1 we have to compute the functions fi[1];w [and f]i[2];w [in another way as in][ §][ 1. As only a few inputs are mapped] to 1 by fi[1];w [or f]i[2];w [, we consider functions f][ ∈] [B][n][ where][ |][f][−][1][(1)][|][ = r is] small.

;
###### DEFINITION 3.1 : L(r n) = max{L(f) | f ∈ Bn, |f[−][1](1)| = r} .

;
###### The obvious upper bound on L(r n) is rn 1, consider the DNF. − This upper bound has been improved by Finikov (57) for small r .

;
###### LEMMA 3.2 : L(r n) 2n 1 + r2[r][−][1] . ≤ −

 Proof : We describe a function f ∈ Bn where |f[−][1](1)| = r by an r × n- matrix consisting of the r inputs in f[−][1](1) . For small r, in particular

<
###### r log n, several columns of the matrix are the same. We make the most of this fact.

 We do not increase the formula size of f by interchanging the roles of xj and xj . With such interchanges we obtain a matrix whose first row consists of zeros only. Now the number l of different columns in

; : : : ;

###### the matrix is bounded by 2[r][−][1] . Let c1 cl be the different columns
 and A(i) be the set of numbers j such that the j -th column equals ci . Let a(i) be the minimal element of A(i) .

 By definition, f(x) = 1 iff x equals one of the rows of the matrix. This can now be tested efficiently. f1 tests whether for each i all variables xj (j ∈ A(i)) have the same value, and afterwards f2 tests whether x and some row agree at the positions a(i) (1 ≤ i ≤ l ). f2 is the disjunction of r monoms of length l, hence L(f2) ≤ rl − 1, and


###### f1(x) =
 [�]

1 i _l_
_≤_ _≤_


###### �� � �
 xp ∨ xp (3.2)
p A(i) p A(i)
_∈_ _∈_


-----

**95**

###### implying L(f1) ≤ 2n−1 . Since f = f1 ∧f2 and l ≤ 2[r][−][1], we have proved the lemma. 2

;
###### LEMMA 3.3 : L(r n) (2 + o(1))nr log[−][1] n if r log[2] n . ≤ ≥

 � � Proof : For r[′] = log(n log[−][2] n) we represent f as a disjunction of

=
###### ⌈r r[′]⌉ functions fi, where |fi[−][1](1)| ≤ r[′] . We apply Lemma 3.2 to all fi . Therefore, if r log[2] n, ≥

; = =
###### L(r n) r r[′] 1 + r r[′] (2n 1 + r[′] 2[r][′][−][1]) (3.3) ≤⌈ ⌉− ⌈ ⌉ −

:
###### = (2 + o(1))nr log[−][1] n

 2

 Lupanov (62 b) applied this result to the construction of efficient for- mulas.

 THEOREM 3.2 : The formula size of all f ∈ Bn is bounded by (2 + o(1))2[n] log[−][1] n .

;
###### Proof : We use Lupanov’s (k s)-representation. Again by (2.12) 2p 2[s]
 gates are sufficient if all fi[1];w [and f]i[2];w [are computed. By definition, each] fi[1];w [can be computed as disjunction of at most s minterms of length k .] All fi[1];w [can be computed by disjoint formulas with altogether p 2][s][ks] gates. Let qi(r) be the number of vectors w which appear exactly r times as a column in block Ai . The sum of all qi(r) equals the number of different vectors w and is therefore bounded by 2[s] . The sum of all rqi(r) equals 2[n][−][k], which is the number of columns. If w appears r times as a column in Ai, |(fi[2];w[)][−][1][(1)][|][ = r . f]i[2];w [is defined on m = n][ −] [k]

<
###### variables. If r log[2] m, we compute fi[2];w [by its DNF, otherwise we] apply Lemma 3.3. Altogether for each block Ai


-----

**96**

###### � ;
 L(fi[2];w[)][ ≤] [�] L(r m)qi(r) (3.4)
w r

###### � � ≤ (rm − 1)qi(r) + (2 + o(1)) rm log[−][1] mqi(r)

r<log[2] m r log[2] m

_≥_

###### ≤ m log[2] m qi(r) + (2 + o(1)) m log[−][1] m rqi(r)
 [�] [�]

r r

:
###### 2[s] m log[2] m + (2 + o(1)) 2[m] m log[−][1] m ≤

 Altogether we obtain a formula for f of at most

 2p 2[s] + p 2[s] ks + p 2[s] m log[2] m + (2 + o(1)) p 2[m] m log[−][1] m (3.5)

 gates. We prove the theorem by choosing k = 2 log n and s = ⌈ ⌉ n 3 log n, implying m = n 2 log n and, since p 2[k] s[−][1] + 1, −⌈ ⌉ −⌈ ⌉ ≤ p = O(n) as well as p 2[m] 2[n] s[−][1] + 2[m] . 2 ≤

 4.4 The depth over complete bases

 Here the lower bound for almost all Boolean functions can be de- rived easily from the results on formula size by the following funda- mental lemma. A partial converse is proved in Ch. 7.

 LEMMA 4.1 : D(f) log(L(f) + 1) for all Boolean functions. ≥⌈ ⌉

 Proof : Using the results of 4, Ch. 1, we can consider a Boolean § formula of depth D(f) for f . A formula is a binary tree. Binary trees of depth d have at most 2[d] 1 inner gates. Therefore our formula for − f has size l bounded by 2[D(f)] 1 . Hence L(f) l 2[D(f)] 1 and the − ≤ ≤ − lemma follows. 2

 We combine Theorem 3.1 with Lemma 4.1.


-----

**97**

###### THEOREM 4.1 : The depth of almost all f ∈ Bn is at least n log logn o(1). − −

 THEOREM 4.2 : The depth of each f ∈ Bn is not larger than n + log n 1 . ⌈ ⌉−

 Proof : W.l.o.g. we assume that f[−][1](1) 2[n][−][1] and use the DNF. | | ≤ Otherwise we could use the CNF. All minterms can be computed in parallel in depth log n . As the number of minterms is bounded by ⌈ ⌉ 2[n][−][1], we can sum up the minterms in depth n 1 . 2 −

 By Theorem 4.1 and Theorem 4.2 the Shannon effect is valid for Bn and the depth of B2-circuits. The trivial upper bound of Theorem 4.2 has been improved several times. We describe the history of these improvements.

 DEFINITION 4.1 : Let log[(1)] x = log x and log[(k)] x = log log[(k][−][1)] x .

          ###### For x 1, log[∗] x = 0 and, for x 1, log[∗] x is the minimal k such ≤ that log[(k)] x 1 . ≤

 log[∗] x is an increasing function tending to as x . But log[∗] x ∞ →∞ is growing rather slowly. So log[∗] x 5 for all x 2[65536] . ≤ ≤ Let a(n) be the following number sequence : a(0) = 8, a(i) = 2[a(i][−][1)] + a(i − 1) . Now we are able to describe the improved bounds on D(Bn) .
 Spira (71 b): n + log[∗] n . Muller and Preparata (71): n + i for n a(i) . ≤ McColl and Paterson (77): n + 1 . Gaskov (78): n log log n + 2 + o(1) . −

 The bound of Gaskov is optimal at least up to small additive terms (see Theorem 4.1). McColl and Paterson even use a circuit scheme, i.e. a fixed underlying graph. For different functions only the types of the gates are changed. By easy counting arguments one can prove that the depth of a circuit scheme cannot be smaller than n 1 . −


-----

**98**

###### Because already the simple construction of Theorem 4.2 is not too bad, we only discuss some ideas of the construction of McColl and Paterson. For each partition of the set of variables X to an m-element set Z and an (n m)-element set Y we can generalize (2.5) to −
 f(y ; z) = � ; c) = � ; c)): (4.1)

c 0;1 c 0;1
_∈{_ _}[m][m][c][(z)][ ∧]_ [f(y] _∈{_ _}[m][(s][c][(z)][ ∨]_ [f(y]


###### McColl and Paterson ˝smuggled˝ the computation of mc(z) or sc(z)

;
###### into the computation of f(y c) . This leads to a saving of depth if we are content with the computation of an approximation of f . These approximations can be chosen such that f can be computed efficiently from its approximations.

 4.5 Monotone functions

 The importance of the class of monotone functions will be discussed in Ch. 6. We know already that the minimal polynomial of a mono- tone function is the unique MDNF. We have considered in Ch. 3 the following monotone functions: threshold functions, sorting function, and Boolean matrix product. Further examples can be found in Ch. 6.

 In order to apply Shannon’s counting argument to the estimation of C(Mn) and Cm(Mn) we have to estimate |Mn| . This problem has been formulated (in another context) already by Dedekind. Contributions to this problem can be traced back to Alekseev (73), Gilbert (54), Hansel (66), Kleitman (69) and (73), Kleitman and Markowsky (75), and Korshunov (77) and (81 a). We cite the results of Korshunov who obtained his exact bounds by a description of the structure of almost all f ∈ Mn .


-----

**99**


###### DEFINITION 5.1 : Let M[t]n [contain all f][ ∈] [M][n][ such that]

< ;

###### x1 + · · · + xn t − 1 ⇒ f(x) = 0 (5.1)

     - ;

###### x1 + · · · + xn t + 1 ⇒ f(x) = 1 (5.2)

;

###### |{x | x1 + · · · + xn = t − 1 and f(x) = 1}| ≤ 2[⌊][n][=][2][⌋] and (5.3)

:

###### |{x | x1 + · · · + xn = t + 1 and f(x) = 0}| ≤ 2[⌊][n][=][2][⌋] (5.4)


= �n�
###### THEOREM 5.1 : Let k = ⌊n 2⌋ and E(n) = k . Almost all f ∈ Mn are in M[k]n [, if n is even, and in M]n[k] n, if n is odd. Furthermore,
 [∪] [M][k+1]

=

###### let an ∼ bn iff an bn → 1 as n →∞ . Then


###### �� n � � |Mn| ∼ 2[E(n)] exp = (2[−][n][=][2] + n[2] 2[−][n][−][5] − n 2[−][n][−][4]) n 2 1 −

 if n is even, and


;
###### (5.5)


###### �� n � |Mn| ∼ 2 · 2[E(n)] exp = (2[−][(n+3)][=][2] − n[2] 2[−][n][−][6] − n 2[−][n][−][3]) (n 3) 2 −
 � n � �

;

###### + (2[−][(n+1)][=][2] + n[2] 2[−][n][−][4])

=
###### (n 1) 2 −
 if n is odd.

 By these results almost all monotone Boolean functions have only

=
###### prime implicants and prime clauses whose length is about n 2 . For our purposes (see also § 2 and § 3) a good estimation of log |Mn| is sufficient. Such a result is much easier to prove.

 PROPOSITION 5.1 : The number of monotone functions f ∈ Mn is � n � larger than 2[E(n)] where E(n) = n=2 is larger than c2[n]n[−][1][=][2] for some
_⌊_ _⌋_

   ###### constant c 0 .

 Proof : The estimation of E(n) follows from Stirling’s formula. E(n) is

=
###### the number of different monotone monoms of length n 2 . For each ⌊ ⌋ subset T of this set of monoms we define fT as the disjunction of all

=
###### m T . Since no monom of length n 2 is a shortening of another, ∈ ⌊ ⌋


-----

**100**

###### PI(fT) = T and fT ̸= fT[′] if T ̸= T[′] . We have defined 2[E(n)] different functions fT Mn . 2 ∈

 Now we can apply the results in 2 and 3 on the number of § § circuits or formulas of size b . If we consider monotone circuits or formulas, we may replace the factor 16[b] by 2[b], since |Ωm| = 2 . By Shannon’s counting argument we obtain from elementary calculations the following results.

;                                  
###### THEOREM 5.2 : For some constants c1 c2 0 almost all f ∈ Mn
 have (monotone) circuit size bounded below by c1 2[n] n[−][3][=][2], (mono- tone) formula size bounded below by c2 2[n] n[−][1][=][2] log[−][1] n, and (mono
=
###### tone) depth bounded below by n − (1 2) logn − log logn + log c2 .


###### What is known about upper bounds ? One can show for the (mono- tone) circuit size upper bounds of the same size as the lower bounds of Theorem 5.2. Lupanov (62 a) and (65 b), who proved asymp- totically optimal bounds on the circuit and formula size of almost all Boolean functions, could design for monotone functions only cir- cuits of size larger than 2[n] n[−][3][=][2] . Pippenger (76) and (78) described for all monotone functions B2-circuits of size O(2[n] n[−][3][=][2]) . The old O(2[n] n[−][3][=][2] log[2] n) bound of Reznik (62) on Cm(Mn) has been improved at first by Pippenger (76) to O(2[n] n[−][3][=][2] log n), and finally Red’kin (79) proved that all monotone functions can be computed by monotone cir- cuits of size O(2[n] n[−][3][=][2]) . This implies that for almost all monotone functions f ∈ Mn C(f) and Cm(f) are of the same size. In Ch. 6 we learn that for certain f ∈ Mn C(f) may be much smaller than Cm(f) .
 Since the O(2[n] n[−][3][=][2]) bounds are rather complicated, we only prove the O(2[n] n[−][3][=][2] log n) bound of Pippenger for monotone circuits. More important than the actual size of the bound it is to learn why no monotone function belongs to the hardest functions in Bn . The fol- lowing circuit design takes advantage of structural particularities of monotone functions.


-----

**101**

###### The fundamental equality (2.5) for decoding circuits, namely f = (xn ∧ f0) ∨ (xn ∧ f1), contains a negation. For monotone functions, f0 f1, and, considering the cases xn = 0 and xn = 1, we can prove ≤ the following monotone decompositions of f ∈ Mn .


###### f = f0 ∨ (xn ∧ f1) = (xn ∨ f0) ∧ f1


:
###### (5.6)


###### Applying the first part of (5.6) n m times, we obtain −

; : : : ;

###### f(x1 xn) = (5.7)
 � �� xi(j) ∧ f(x1 ; : : : ; xm ; i(m + 1); : : : ; i(n))�:

i(m+1);:::;i(n) 0;1 i(j)=1
_∈{_ _}_


###### Later on we discuss how we compute the 2[n][−][m] subfunctions of f

; : : : ;

###### on x1 xm efficiently in common. Furthermore we need all mono
; : : : ;

###### tone monoms on xm+1 xn . These monoms can be computed with
 2[n][−][m] (n m) 1 -gates, since the empty monom and the n m − − − ∧ − monoms of length 1 are given and each monom of length l can be computed with one -gate from a monom of length l 1 and a vari- ∧ − able. After having computed the subfunctions of f in (5.7), less than 3 2[n][−][m] gates are sufficient for the computation of f . ·
 According to the law of simplification xy y = y, it is not possible ∨ that both p and some proper shortening or lengthening of p are prime

; : : : ;

###### implicants of f . If p1 pr is a chain of monoms, i.e. pi+1 is the
 lengthening of pi by one variable, then at most one monom of the chain is a prime implicant of f . We show how we may partition the set of monoms into the smallest possible number of chains. These chains are grouped into b blocks. Then we compute all subfunctions of f in the following three steps.

; : : : ;

###### Step 1 : Compute all monoms on x1 xm . This can be done with
 less than 2[m] gates.

 Step 2 : Compute for each block all monotone functions having only prime implicants of that block, or equivalently, having at most one prime implicant of each chain of the block.


-----

**102**

; : : : ;

###### Step 3 : Each subfunction f[′] of f on x1 xm can be computed

; : : : ;

###### as the disjunction of f1[′] fb[′] [where f]i[′] [is the disjunction of all prime]
 implicants of f[′] belonging to the i -th block. Thus Step 3 can be im- plemented with (b 1) 2[n][−][m] -gates. − ∨


###### As Step 2 will be implemented by -gates only, the whole circuit ∨ will contain only 4 logical levels.
 � m � = Since there exist E(m) = ⌊m=2⌋ monoms of length ⌊m 2⌋, which have to belong to different chains, E(m) chains are necessary. By solving the marriage problem we prove that E(m) chains suffice.

;
###### LEMMA 5.1 : Let G = (A B E A B) be a bipartite graph. For ∪ ⊆ ×

;
###### A[′] A let Γ(A[′]) be the set of vertices b B such that (a b) E for ⊆ ∈ ∈ some a A[′] . G contains A vertex disjoint edges iff ΓA[′] A[′] for ∈ | | | | ≥| | all A[′] A . ⊆

 Sketch of Proof : Obviously the condition is necessary. For the sufficiency part of the proof e = E A, since ΓA A . | | ≥| | | | ≥| |
 Case 1 : e = A . Since ΓA A, all edges are vertex disjoint. | | | | ≥| |
 Case 2 : A[′] : = A[′] = A and ΓA[′] = A[′] . Let B[′] = ΓA[′], ∃ ̸◦ ̸ ̸ | | | | A[′′] = A A[′] and B[′′] = B B[′] . The condition of the lemma is fulfilled − − for the smaller subgraphs on A[′] B[′] and A[′′] B[′′] . By induction ∪ ∪ hypothesis we obtain A[′] and A[′′] vertex disjoint edges resp. on these | | | | subgraphs, altogether A vertex disjoint edges. | |

       ###### Case 3 : A[′] = : ΓA[′] A[′] . By eliminating an arbitrary edge we ∀ ̸ ̸◦ | | | | obtain a smaller graph fulfilling the condition of the lemma.

;               -               
###### Case 4 : A[′] = A[′] = A: ΓA[′] A[′], ΓA = A and E A . ∀ ̸ ̸◦ ̸ | | | | | | | | | | | |
 The degree of some b B is at least 2 . By eliminating some edge ∈

;
###### (a b) we obtain a smaller graph fulfilling the condition of the lemma. 2


-----

**103**

; : : : ;

###### Now we build E(m) chains containing all monoms on x1 xm .

=
###### We start on level m 2 where each chain contains one monom of ⌊ ⌋
= � m �
###### length m 2 . We show how the monoms of length k + 1 can be ⌊ ⌋ k+1 �m� = added to the chains containing one monom of length k m 2 .
k _≥⌊_ _⌋_
###### The addition of the short monoms can be performed in the same way.

 Let A and B contain the monoms of length k+1 and k resp. a A ∈ and b B are connected by an edge iff a is a lengthening of b . If ∈ we find a set S of A vertex disjoint edges, we can add each monom | |

;
###### a A to that chain ending in b where (a b) S . We only have to ∈ ∈ check the condition of Lemma 5.1. Let A[′] A be a set of l monoms. ⊆ Each monom of length k + 1 has k + 1 shortenings in B, therefore (k + 1)l edges are leaving A[′] and go to ΓA[′] . Each monom of length k has m k lengthenings in A, therefore at most (m k)r, where − − r = ΓA[′], edges are gathered by ΓA[′] . Since all edges leaving A[′] are | | gathered by ΓA[′],

 (k + 1)l (m k)r (5.8) ≤ −

 implying l r, since k+1 m k . Since the condition of Lemma 5.1 ≤ ≥ − is fulfilled, our construction is possible. The set of all monoms can be

; : : : ;

###### partitioned to E(m) chains C1 CE(m) .


###### If C1


; : : : ;
###### Ci build a block B, at most


###### S(B) = (|Cj| + 1) (5.9)
 [�]

1 j i
_≤_ _≤_

###### monotone functions have at most one prime implicant of each chain Cj (1 ≤ j ≤ i) and no other prime implicant. These functions can be

; : : : ;

###### computed by a circuit of size S(B), if the monoms on x1 xm are
 given. This is easy to see, since any function with l prime implicants can be computed with one -gate from a function with l 1 prime ∨ −

; : : : ;

###### implicants and a monom. If we join the chains to b blocks B1 Bb,
 Step 2 and 3 of our circuit can be implemented with ΣS(Bi) and (b − 1) 2[n][−][m] gates resp.

 b has to be chosen such that Step 2 and 3 can both be implemented efficiently. The ˝size˝ S(B) of the blocks should be bounded by some


-----

**104**

###### parameter 2[s] . Since each chain Cj contains at most m + 1 monoms, each chain increases the size of a block at most by the factor of m+2 . So we build the blocks by adding as many chains as possible without skipping the size bound 2[s] . Then at most one block has a size less

=

###### than 2[s] (m + 2) . We estimate the number of blocks b . The sum of
 all |Cj| is 2[m], since each monom is in exactly one chain. Let H(Cj) = log(|Cj| + 1) . Then for all blocks B with at most one exception by (5.9)
 � H(C) = log S(B) s log(m + 2): (5.10)
 ≥ −
C B
_∈_

###### Because of the concativity of log
 � �
 H(Cj) = E(m) E(m)[−][1] log(|Cj| + 1) (5.11)
1 j E(m) 1 j E(m)
_≤_ _≤_ _≤_ _≤_

###### � � ≤ E(m) log � E(m)[−][1](|Cj| + 1)

1 j E(m)
_≤_ _≤_

:
###### = E(m) log(2[m] E(m)[−][1] + 1)

 Combining (5.10) and (5.11) we can estimate b by

1
###### � �− : b 1 + E(m) log(2[m] E(m)[−][1] + 1))(s log(m + 2) (5.12) ≤ −

 The size of the whole circuit can be estimated by


###### 3 2[n][−][m] + 2[m] + b 2[s] + (b 1) 2[n][−][m] · · −


;
###### (5.13)


###### since, by definition, S(B) 2[s] for all blocks B . We may choose m and ≤ s and can estimate b by (5.12). Let

= = ;
###### m = n 3 and s = (2 3)n log n (5.14) ⌊ ⌋ −
 then, by Stirling’s formula, E(m) = Θ(2[n][=][3] n[−][1][=][2]), and s is linear in n, hence by (5.12)

:
###### b = O(2[n][=][3] n[−][3][=][2] log n) (5.15)

 Inserting (5.14) and (5.15) into (5.13) we have proved the following upper bound on Cm(Mn) .

 THEOREM 5.3 : Each monotone function f ∈ Mn can be computed by a monotone circuit of size O(2[n] n[−][3][=][2] log n) .


-----

**105**

###### McColl (78 b) proved the following upper bound on Dm(Mn) . The proof is rather simple, but contains the idea of smuggling computation steps into other computations.

 THEOREM 5.4 : Each monotone function f ∈ Mn can be computed by a monotone circuit of depth n .

; ; : : : ; ;

###### Proof : We define for f ∈ Mn functions g1 h1 gn−1 hn−1 such that

;
###### Dm(gi) Dm(hi) ≤ i and f = g1 ∨· · · ∨ gn−1 as well as f = h1 ∧· · · ∧ hn−1 . This obviously implies the theorem. We prove the assertion by induction on n . For n = 2 the claim is obvious. For the induction step we use the representations of f in (5.6), namely f0 ∨ (xn ∧ f1) and

;

###### (xn ∨ f0) ∧ f1 . Since f0 f1 ∈ Mn−1, by induction hypothesis
 f0 = g1 ∨· · · ∨ gn−2 where Dm(gi) ≤ i and (5.16)

:
###### f1 = h1 ∧· · · ∧ hn−2 where Dm(hi) ≤ i (5.17)

 g1 has depth 1 . If g1[∗] [has depth 2, g]1[∗] [also can be]
 [∨] [g][2] [∨· · · ∨] [g][n][−][2] computed in depth n 1 . Thus there is some place in the computation − of f0 where we may smuggle in xn . g1[∗] [= x][n] [∨] [g][1] [has depth 2, so x][n] [∨] [f][0] has depth n− 1 . f = (xn ∨ f0) ∧ f1 has depth n where f1 = h1 ∧· · ·∧ hn−2 and hn−1 = xn ∨f0 such that Dm(hi) ≤ i . By dual arguments we obtain the other representation of f . 2

 We have seen that the Shannon effect is valid for Mn and monotone depth. Henno (79) generalized McColl’s design to functions in m- valued logic. By a further improvement of Henno’s design Wegener (82 b) proved the Shannon effect also for the monotone functions in m- valued logic and (monotone) depth.


-----

**106**

###### 4.6 The weak Shannon effect

 The proof of the Shannon effect for various classes of functions and complexity measures is a main subject in Russian language literature. There also weak Shannon effects are studied intensively. The Shannon effect is valid for Fn and CM iff almost all functions f ∈ Fn have nearly the same complexity k(n) and k(n) = CM(Fn) is the complexity of the hardest function in Fn . The weak Shannon effect concentrates on the first aspect.

 DEFINITION 6.1 : The weak Shannon effect is valid for the class of functions Fn and the complexity measure CM if CM(f) ≥ k(n) − o(k(n)) and CM(f) ≤ k(n) + o(k(n)) for almost all f ∈ Fn and some number sequence k(n) .

 The validity of the weak Shannon effect for Mn and circuit size and monotone circuit size has been proved by Ugolnikov (76) and Nurmeev (81) resp. It is not known whether the Shannon effect is valid too. The complexity k(n) of almost all functions is not even known for the (monotone) circuit size. How can the weak Shannon effect be proved without knowing k(n) ? Often Nigmatullin’s (73) variational principle is used. If the weak Shannon effect is not valid

                 ###### there exist some number sequence k(n), some constant c 0, and

;

###### some subclasses Gn Hn Fn such that for infinitely many n
 ⊆

; ;
###### |Gn| |Hn| = Ω(|Fn|) (6.1)


;
###### CM(f) ≤ k(n) if f ∈ Gn

;
###### CM(f) ≥ (1 + c)k(n) if f ∈ Hn


;
###### and (6.2)

:
###### (6.3)


###### Since Gn and Hn are large subclasses, there are functions gn Gn and ∈ hn Hn which do not differ too much. Furthermore this implies that ∈ hn cannot be much harder than gn in contradiction to (6.2) and (6.3).


-----

**107**

###### Nurmeev’s proof is based on Korshunov’s description of the struc- ture of almost all f ∈ Mn (see § 5). However, the proof is technically involved.

 4.7 Boolean sums and quadratic functions

 In contrast with the large classes of Boolean functions, Bn and Mn, we consider here the smaller classes of k-homogeneous functions.

 DEFINITION 7.1 : A Boolean function f ∈ Mn is called k-homo- geneous if all prime implicants of f are of length k . H[k]n [and H]n[k] ;m [are] the classes of k-homogeneous functions. 1-homogeneous functions are called Boolean sums, 2-homogeneous functions are called quadratic.

 Important examples are the threshold functions, the Boolean ma- trix product and the clique functions (see Ch. 6).
 �n� Since there are monoms of length k and since a k-homogeneous
k
###### function is a non empty disjunction of such monoms,


###### �n�

;
###### |H[k]n[|][ = 2][b(n][;][k)][ −] [1] where b(n k) = k


:
###### (7.1)


###### �n� (For constant k, = Θ(n[k])). With Shannon’s counting argument
k
###### the following lower bounds can be proved.

 THEOREM 7.1 : For constant k, the (monotone) circuit size as well as the (monotone) formula size of almost all f ∈ H[k]n [is Ω(n][k][ log][−][1][ n) .]

 We shall see that these bounds are asymptotically optimal for k ≥ 2 . The case k = 1 is treated as an exercise. At first we prove that it is sufficient to investigate the case k = 2 .


-----

**108**

###### LEMMA 7.1 : i) C(H[k]n[)][ ≤] [C][m][(H][k]n[) .]
 ii) Cm(H[k]n[)][ ≤] [C][m][(H]n[k][−];n[1][) + 2n][ −] [1 .]
 iii) Cm(H[k]n;n[)][ ≤] [n C][m][(H][k]n[) .]

 Proof : i) and iii) are obvious by definition. For ii) let f ∈ H[k]n [and let] gi[′] [be the disjunction of all prime implicants of f containing x][i][ . We] factor out xi, hence gi[′] [= x][i][ ∧] [g][i][ for some g][i][ ∈] [H]n[k][−][1] . The assertion follows, since

 f(x) = � xi ∧ gi(x): (7.2)

1 i n
_≤_ _≤_

###### 2

 By Lemma 7.1 an O(n[2] log[−][1] n)-bound for H[1]n;n [implies the same] bound for H[2]n [and O(n][k][ log][−][1][ n)-bounds for H]n[k][−];n[1] [and H]n[k] [. Savage (74)] presented the following design of monotone circuits for f ∈ H[1]n;n [. The]

=
###### variables are partitioned to b = n log n blocks of at most log n ⌈ ⌊ ⌋⌉ ⌊ ⌋ variables each. All Boolean sums on each block can be computed with less than 2[⌊][log n][⌋] n -gates similarly to the computation of monoms ≤ ∨ in § 5. Now each fi ∈ H[1]n [can be computed with b][ −] [1][ ∨][-gates from] its subfunctions on the blocks. Since we have n outputs and b blocks, we can compute f with (2b 1)n -gates. We combine this result with − ∨ Lemma 7.1.

 THEOREM 7.2 : Each k-homogeneous function f ∈ H[k]n [can be] computed by a (monotone) circuit of size (2+o(1)) n[k] log[−][1] n, if k 2 . ≥

 We note that we have designed asymptotically optimal monotone circuits for almost all f ∈ H[1]n;n [which consist of][ ∨][-gates only. In Ch. 6] we get to know some f ∈ H[1]n;n [such that optimal monotone circuits] for f have to contain -gates disproving the conjecture that Boolean ∧ sums may be computed optimally using -gates only. ∨
 Similar results for formulas are much harder to achieve. Using the MDNF of f each prime implicant requires its own -gate. We can ∧


-----

**109**

###### compute efficiently many prime implicants by the law of distributivity. With m + r 1 gates we can compute mr monoms of length 2 by − (x1 ∨· · · ∨ xm) ∧ (xm+1 ∨· · · ∨ xm+r) . The ratio of profit, number of monoms, and costs, number of gates, is best, if m = r and m is large. It is only useful to compute monoms of length 2 which are prime implicants of f .

: : : ;
###### For f ∈ H[2]n [we consider the following graph G(f) on][ {][1][;] n} .

;
###### G(f) contains the edge {i j} iff xixj ∈ PI(f) . A complete bipartite graph on disjoint m-vertex sets A and B contained in G(f) is called Km;m . Such a Km;m corresponds to m[2] prime implicants which can be computed with 2m 1 gates. Since the result has to be connected − with other terms, we define the cost of a Km;m as 2m . If we can cover G(f) by a(m) copies of Km;m (1 ≤ m ≤ n=2), then f can be computed by a monotone formula of size
 � :
 2 a(m) m 1 (7.3) −
1 m n=2
_≤_ _≤_

###### This suggests the following greedy algorithm. Starting with G(f) search the largest complete bipartite subgraph, Km;m, compute its edges with 2m−1 gates, eliminate the edges of this copy of Km;m in G(f) and continue in the same way. At the end compute the disjunction of all intermediate results. It is highly probable that the so constructed monotone formula for f will not have size larger than O(n[2] log[−][1] n) . But this is difficult to prove.

 Bublitz (86) investigated an algorithm that leads to monotone for- mulas which might be not as good as the formulas of the greedy algorithm above. For some carefully selected decreasing sequence m(1); : : : ; m(k) = 1 he searches always for the largest Km;m where m equals some m(i) . By this approach it is easier to estimate the efficiency of the algorithm.

 THEOREM 7.3 : L(H[k]n[)][ ≤] [L][m][(H][k]n[)][ ≤] [22 n][k][ log][−][1][ n, if k][ ≥] [2 .]

 Proof : By (7.2) we have to prove the claim for k = 2 only. For n 54 ≤


-----

**110**

###### �n� we use the MDNF of f whose size is bounded by 2 = n[2] n and
2 _−_
###### smaller than 22 n[2] log[−][1] n . For n 55 let k = log[∗] n (see Def. 4.1) and ≥
 � �

= :
###### m(i) = (log n) (4 log[(k][−][i)] n) for 1 i k 2 and m(k 1) = 1 ≤ ≤ − −
 (7.4)

 We use the approach discussed above. Let e(i) be the number of edges of G(f) after the elimination of all Km(i);m(i) . Obviously e(0) = �n� PI(f) and by results of graph theory (see Bollob´as (78)) | | ≤ 2

= :
###### e(i) n[2](m(i) n)[1][=][m(i)] for 1 i k 2 and e(k 1) = 0 (7.5) ≤ ≤ ≤ − −

 By elementary but tedious computations one can prove for n 55 ≥ that


###### e(i) n[2] ≤


= :
###### (4[i] log[(k][−][i][−][1)] n) for 0 i k 2 (7.6) ≤ ≤ −


###### After the elimination of all Km(i−1);m(i−1) the graph has at most e(i − 1) edges, each Km(i);m(i) has m(i)[2] edges, therefore the algorithm selects at most e(i − 1)=m(i)[2] copies of Km(i);m(i) . The cost of these subgraphs

=
###### altogether is bounded by 2e(i 1) m(i) . According to (7.4) and (7.6) −

=

###### this can be estimated by 16 n[2] (4[i][−][1] log n) . Summing up these terms
 we obtain the upper bound of 22 n[2] log[−][1] n . 2

 We emphasize the power of Shannon’s counting argument which leads to asymptotically optimal results for large classes like Bn and Mn as well as for small classes like Hn[k] [. For almost all functions in] these classes we know nearly optimal circuits.

 4.8 Universal circuits

 Each circuit computes a definite Boolean function. We now discuss the concept of programmable circuits, which are also called universal circuits. What does it mean to program a circuit ? How do we ˝read in˝ such a program ? The only inputs of a Boolean circuit are Boolean


-----

**111**

; : : : ;

###### variables. Programmable circuits have input variables x1 xn, the

; : : : ;

###### true input variables, and y1 ym, the program variables or con trol bits. For each of the 2[m] input vectors for y, the 2[m] admissible programs, some Boolean function fy Bn is computed by the circuit. ∈


; ;
###### DEFINITION 8.1 : A programmable circuit S is called (n c d)-uni- versal if it contains n true input variables and c distinguished gates such that for each circuit S[′] of size c[′] c and depth d[′] d there is ≤ ≤ some admissible program such that the i -th distinguished gate of S computes the same function as the i -th gate of S[′] (1 i c[′]). ≤ ≤

 Efficient universal circuits offer the possibility of applying the same circuit to several purposes. We design two types of universal circuits. The first one is optimal with respect to size but the depth is rather large (whether it is possible to reduce depth is discussed in 2 of § Ch. 7) whereas the other one is optimal with respect to depth and also is of reasonable size. Since depth and time of parallel computers are related, we refer to some papers on the construction of universal parallel computers, namely Galil and Paul (83) and Meyer auf der Heide (86).

; ;
###### We begin with lower bounds. Each (n c d)-universal circuit obvi- ously has depth Ω(d) . What about its size ?

; ;
###### THEOREM 8.1 : Each (n c )-universal circuit has size Ω(c log c) ∞ if c = O(2[n]n[−][1]) .

 The condition c = O(2[n]n[−][1]) is not really to be seen as a restriction, since each f ∈ Bn has circuit size O(2[n]n[−][1]) (see § 2).

 Proof of Theorem 8.1 : We prove the theorem by counting arguments. If the universal circuit has m control bits, it can compute at most 2[m] c different functions. For small r, each Boolean function f ∈ Br has


-----

**112**

###### circuit size bounded by c . Due to the results of 2 r can be chosen § as log c + log logc k for some appropriate constant k . In particular −

:
###### 2[m]c ≥|Br| ⇒ m − log c ≥ 2[r] = Ω(c log c) (8.1)

 Since m = Ω(c log c) and since we have to consider control bits of positive fan-out only, the size of the circuit is Ω(c log c) . 2

 For the construction of universal circuits we design universal gates and universal graphs. A universal gate has two true inputs x1 and x2, four control bits y1, y2, y3, and y4 and computes


:

###### y1 x1 x2 y2 x1 x2 y3 x1 x2 y4 x1 x2 (8.2) ∨ ∨ ∨


###### For each f ∈ B2 there are control bits such that the universal gate

;

###### realizes f(x1 x2) by its DNF.

 The construction of universal graphs is much more difficult. Valiant (76 b) designed universal circuits of size O(c log c) if c n . ≥ By the results of 4, Ch. 1, we have to consider only circuits of fan- §

; : : : ;

###### out 2 . We have to simulate the gates G[′]1 G[′]c[′][ of each circuit S][′]

; : : : ;

###### at the distinguished gates G1 Gc[′] of the universal circuit S . The
 distinguished gates of S will be universal gates, i.e. that the type of G[′]i [can be simulated. Since G]j[′] [may be a direct successor of G]i[′] [in S][′][,]

 ###### if j i, we have to be able to transfer the result of Gi to any other

     ###### gate Gj where j i . We design the universal circuit in such a way that, if G[′]j [is direct successor of G]i[′] [in S][′][, we have a path from G][i][ to G][j] in S such that on all edges of this graph the result of G[′]i [is computed.] Since the successors of G[′]i [are different for different S][′][, we use univer-] sal switches consisting of two true inputs x1 and x2, one control bit y, and two output bits computing


:

###### z1 = y x1 y x2 and z2 = y x1 y x2 (8.3) ∨ ∨


###### In either case both inputs are saved, but by setting the control bit y we control in which direction the inputs are transferred to. If y = 1, z1 = x1 and z2 = x2, and, if y = 0, z1 = x2 and z2 = x1 .


-----

**113**

###### We are looking for an (n+c)-universal circuit, i.e. a directed acyclic graph G of fan-out and fan-in 2 with the following properties. There are n + c distinguished nodes for n true input variables and for the simulation of c gates. Furthermore, for each circuit S[′] with n inputs

;

###### and c gates of fan-out and fan-in 2 we may map each edge (v[′] w[′]) in
 S[′] to a path from the corresponding node v to w in S such that all these paths are edge disjoint. Replacing the c distinguished nodes for the gates in S by universal gates and all not distinguished nodes by universal switches, we may simulate all circuits S[′] . By the following lemma we reduce the problem to the simulation of graphs of fan-out and fan-in 1 .

;
###### LEMMA 8.1 : Let G = (V E) be a directed acyclic graph of fan-out and fan-in 2 . Then E may be partitioned to E1 and E2, such that

;
###### Gi = (V Ei) has fan-out and fan-in 1 for i = 1 and i = 2 .


; : : : ; ; : : : ; ; : : : ;

###### Proof : Let V = {a1 an}, V[′] = {b1 bn}, V[′′] = {c1 cn}

;

###### and let G[∗] = (V[′] V[′′] E[∗]) be the bipartite graph containing the edge ∪

; ;

###### (bi cj) if (ai aj) ∈ E . We may add some edges such that all nodes of
 G[∗] have degree 2 . Then the assumptions of Lemma 5.1 are fulfilled implying the existence of n vertex disjoint edges. If E1 contains these edges and E2 the other edges (and if we destroy the new edges), we obtain a partition of E as required. 2

 Now it is sufficient to design an (n + c)-universal circuit G[∗] for the simulation of graphs S[′] with fan-out and fan-in 1, such that in G[∗] the fan-out and fan-in of the distinguished nodes is 1 . Then we take two copies of G[∗] and identify the distinguished nodes. This new graph has fan-out and fan-in 2 and may simulate all circuit graphs S[′] with fan-out and fan-in 2 and c gates. We partition the edge set of S[′] by Lemma 8.1 and simulate the edges of E1 and E2 in the first and second copy of G[∗] resp. This leads to the design of a size optimal universal circuit.


-----

**114**

; ;
###### THEOREM 8.2 : If c n, (n c )-universal circuits of size O(c log c) ≥ ∞ may be designed.

 Proof : According to our preliminary remarks we only have to con- struct graphs U(m) of size O(m log m), fan-out and fan-in 2 for all nodes, fan-out and fan-in 1 for m distinguished nodes, such that all directed acyclic graphs of size m and fan-out and fan-in 1 can be sim- ulated. For m = 1 a single node and for m = 2 two connected nodes are appropriate. For m 4 and m = 2k + 2, we use a recursive con- ≥ struction whose skeleton is given in Fig. 8.1. The edges are directed from left to right. For m[′] = m − 1 we eliminate pm . The skeleton of

; : : : ;

###### U(m) has to be completed by two copies of U(k) on {q1 qk} and

; : : : ;

###### on {r1 rk} . Since the q- and r-nodes have fan-out and fan-in 1
 in the skeleton of U(m) as well as in U(k) (by induction hypothesis), these nodes have fan-out and fan-in 2 in U(m) . Obviously the dis
; : : : ;

###### tinguished nodes p1 pm have fan-out and fan-in 1 in U(m) . How
 can we simulate directed acyclic graphs G of size m and fan-out and

;

###### fan-in 1 ? We understand the pairs (p2i 1 p2i) of nodes as supernodes.
_−_

###### The fan-out and fan-in of the supernodes is 2 . By Lemma 8.1 we par
;

###### tition the set of edges of G to E1 and E2 . Edges (p2i−1 p2i) in G are

;

###### simulated directly. The edges leaving a supernode, w.l.o.g. (p1 p2),
 can be simulated in the following way. If the edge leaving p1 is in E1 and the edge leaving p2 is in E2 (the other case is similar), we shall use edge disjoint paths from p1 to q1 and from p2 to r1 .


###### q1 qk 1 qk
_−_


###### p1


###### r1


###### rk 1 rk
_−_

###### Fig. 8.1 The skeleton of U(m) .


-----

**115**

###### If the edges leaving p1 and p2 end in the supernodes p2i−1;2i and p2j−1;2j resp. we shall take a path from q1 to qi−1 and from r1 to rj−1 resp. in the appropriate U(k) . All these paths can be chosen edge disjoint by induction hypothesis. Finally the paths from qi−1 and ri−1 to p2i−1 and p2i can be chosen edge disjoint. Thus the simulation is always successful.

 Let C(m) be the size of U(m) . Then, by construction

= ; ; :
###### C(m) 2 C( m 2 1) + 5 m C(1) = 1 C(2) = 2 (8.4) ≤ ⌈ ⌉−

 This implies C(m) = O(m log m) . In our application m = n+c . Since n c, U(n + c) = O(c log c) . 2 ≤

 Cook and Hoover (85) designed a depth optimal universal circuit.

; ;
###### THEOREM 8.3 : If c n and c d log c, (n c d)-universal ≥ ≥ ≥ circuits of size O(c[3] d log[−][1] c) and depth O(d) may be designed.

 The assumption c d log d is not really a restriction, since it is ≥ ≥ easy to see that C(S) D(S) log C(S) for all circuits S . Perhaps ≥ ≥ it is possible to design universal circuits of depth O(d) and of smaller size. Until now we have some trade-off. If we use universal circuits of optimal depth the circuit size increases significantly. If we use the given circuits of size c and depth d, we have to pay the cost for the production of different types of circuits.

 Proof of Theorem 8.3 : We want to simulate all circuits S[′] of size c[′] c and depth d[′] d . What do we know about the depth of the ≤ ≤ i -th gate G[′]i [of S][′][? Not much. G]i[′] [may be a gate in depth 1 where] some path of length d 1 starts. It may also be a gate in depth i . − Therefore, in order to simulate all circuits S[′] in depth O(d), we cannot wait until all possible predecessors of the i -th gate are simulated.

 For some parameter h chosen later, we simulate the circuits in

: : : =
###### Step 0,, Step d h . Step 0 consists of the inputs of the circuit. ⌈ ⌉


-----

**116**

###### In each further step we simulate all gates. Let zi;m be the simulation of the i -th gate in Step m . If the depth of the i -th gate in S[′] is at most mh, zi;m will simulate this gate correctly. Finally, each gate is

=
###### simulated correctly after Step d h . ⌈ ⌉
 We may choose zi;0 = 0 . For the computation of zi;m we use the input variables and the simulations z1;m−1 ; : : : ; zc;m−1 . In order to
 apply only correct simulations, if zi;m has to be correct, we look for the predecessors of the i -th gate in distance h . If a path starting

<
###### from the i -th gate backwards ends after l h steps at some in- put, this input will be chosen 2[h][−][l] times as predecessor in distance h . For each of the 2[h] predecessors in distance h we have n + c pos- sibilities: x1 ; : : : ; xn ; z1;m−1 ; : : : ; zc;m−1 . We use a binary tree of depth
 k = log(n + c) with n + c leaves for the n + c possibilities. The ⌈ ⌉ nodes are universal selectors y x1 y x2 where y is a control bit. With ∨ these universal selector trees we may select the right predecessors in distance h . If we have to simulate the i -th gate correctly, its depth is at most mh, and the depth of its predecessors in distance h is at most m(h 1), these gates are correctly simulated in the previous step. −

 Obviously each circuit of depth h can be simulated by a complete binary tree of depth h whose nodes are universal gates. Since we have chosen the predecessors correctly, we can compute zi;m by such a

; ;
###### universal computation tree. Altogether we have designed an (n c d)- universal circuit.

=
###### What is the depth and size of it ? We have d h steps. Each ⌈ ⌉ step consists of parallel universal selector trees of depth 2 log(n + c) ⌈ ⌉ and parallel universal computation trees of depth 4 h . Therefore the depth of the universal circuit is

= :
###### d h (2 log(n + c) + 4 h) (8.5) ⌈ ⌉ ⌈ ⌉

 The depth is O(d) if h = Ω(log c) . We note that it is possible to bound the depth by approximately 6 d . In each step each of the c gates is simulated by one universal computation tree of size O(2[h]) and 2[h] universal selector trees of size O(n+c) = O(c) . Altogether the size


-----

**117**

###### may be estimated by

:
###### O(dh[−][1] c[2] 2[h]) (8.6)

 For h = log c the size is O(c[3] d log[−][1] c) . 2 ⌈ ⌉

        ###### If h = ε log c for some ε 0, the depth still is O(d) though the constant factor increases by approximately ε[−][1] but the size decreases to O(c[2+][ε] d log[−][1] c) .

 The concept of universal or programmable circuits leads to quite efficient circuit schemes.

 EXERCISES

 1. The Shannon effect is valid for Bn and C{∧;∨;¬} .

 2. Estimate C(Bn;m) for fixed m and discuss the result.

 3. Prove Theorem 5.2.

 4. Let h(n) = Ω(n) . Apply Shannon’s counting argument to | | CΩ(n)(Bn) . For which h(n) the bounds are a) non exponential b) polynomial ?

 5. If f(x) = xi(1) xi(k) for different i(j), then C(f) = Cm(f) = ∨· · · ∨ L(f) = Lm(f) = k − 1 .

 6. The weak Shannon effect but not the Shannon effect is valid for H[1]n [and C .]

 7. Define a class of Boolean functions such that Shannon’s counting argument leads to much too small bounds.


-----

**118**

###### 8. Let P[k]n [⊆] [B][n][ be the class of functions f which may be computed] by a polynomial whose monoms have not more than k literals. Estimate C(P[k]n[) .]

 9. f ∈ H[2]n [can be computed with n][ −] [1][ ∧][-gates.]

 10. Which is the smallest n such that each f ∈ H[2]n [can be computed] with n 2 -gates ? (Bloniarz (79)). − ∧

 11. Lm(T[n]2[) = O(n log n) .]

 12. Apply the algorithms of § 7 to T[n]2 [and estimate the size of the] constructed formulas.

 13. Estimate the depth of the universal graph U(m) in 8. §


-----

**119**

###### 5. LOWER BOUNDS ON CIRCUIT COMPLEXITY

 5.1 Discussion on methods

 For almost all Boolean functions we know nearly optimal circuits (see Ch. 4). But almost all functions have circuit complexity 2[n] n[−][1] + o(2[n] n[−][1]) . Usually we are in another situation. The function for which we should design an efficient circuit is described by some of its prop- erties, and it is quite easy to design a circuit of size o(2[n] n[−][1]) . For many fundamental functions (see Ch. 3) we can design circuits whose size is a polynomial of small degree. For other important functions, among them several NP-complete functions, the best known circuits have exponential size but size 2[o(n)] . In this situation we have to ask whether we can improve the best known circuits, and in the positive case, whether we can bound the possible improvements. For (explicitly defined) functions f we like to prove lower bounds on C(f) .

 This is the hardest problem in the theory of Boolean functions. The results known are poor. Why is it more difficult to prove lower bounds than to prove upper bounds ? For an upper bound on C(f) it is sufficient to design an efficient circuit, to prove that it computes f, and to estimate its size. We are concerned only with one circuit for f . For a lower bound on C(f) it is necessary to prove that all circuits computing f have a certain circuit size. It is difficult to describe properties of all efficient circuits for f . Although e.g. subtractions and negations resp. seem to be useless for matrix multiplication, they are not useless at all. Optimal circuits cannot be designed without negations (see Ch. 3 and Ch. 6).

 We used the notion ˝explicitly defined Boolean function˝ in order to exclude tricks like diagonalization. If we consider the lexicograph- ical order on the tables of all fn Bn and if we define fn[∗] ∈ [∈] [B][n][ as the] lexicographically first function where C(fn[∗][)][ ≥] [2][n][ n][−][1][, we obtain by de-]


-----

**120**

###### finition a sequence of hard functions. Everybody will admit that the sequence fn[∗] [is not ˝explicitly defined˝. We discuss this notion in][ §][ 6.]
 The Boolean functions we actually consider are explicitly defined. In particular, if the union of all fn[−][1][(1) is in NP, the sequence f][n][ is] explicitly defined. Therefore, a reader who is not familiar with com- plexity theory should not have any problem. All functions known to him are explicitly defined, and he should not try tricks like the diag- onalization trick for the definition of fn[∗] [above.]
 We need the notion ˝explicitly defined˝ to explain the poorness of the known results. Until now nobody was able to prove for some ex- plicitly defined Boolean function fn Bn a lower bound on C(fn) larger ∈ than 3 n . Large lower bounds for non explicitly defined Boolean func- tions are easily achievable, but are of no use regarding our problem. Thus it is necessary to concentrate on the investigation of explicitly defined functions.

 The situation is better for more restricted computation models. In Ch. 6, 8, 11, 12, and 14 we prove in several restricted models larger lower bounds for explicitly defined Boolean functions.

 Since a long time it has been tried to prove lower bounds on circuit complexity (Yablonskii (57)). A simple but general lower bound has been derived by Lamagna and Savage (73).

 DEFINITION 1.1 : f ∈ Bn is called non degenerated if f depends essentially on all its variables, i.e. if the subfunctions of f for xi = 0 and xi = 1 are different.

 THEOREM 1.1 : C(f) ≥ n − 1 for any non degenerated f ∈ Bn .

 Proof : We count the number of edges in an optimal circuit for f . If xi has fan-out 0, the output f of the circuit cannot depend essentially on xi . If another gate than the output gate has fan-out 0, this gate could be eliminated. Therefore the number of edges is at least n+c 1 −


-----

**121**

###### where c = C(f) . Each gate has fan-in 2 implying that the number of edges equals 2 c . Hence 2c n + c 1 and c n 1 . 2 ≥ − ≥ −

 This simple linear bound is optimal for some functions like x1 ⊕· · · ⊕ xn. Usually one does not consider degenerated one-output functions, since one can eliminate unnecessary variables. The situa- tion is different for functions with many outputs. The Boolean matrix product consists of degenerated functions. The i -th output bit si of

; ; : : : ; ;

###### the addition function depends essentially on xi yi x0 y0, only sn−1
 and sn are non degenerated. Applications and generalizations of the simple linear bound are treated in the exercises. Harper, Hsieh and Savage (75) and Hsieh (74) improved the lower bound for many func
=
###### tions to (7 6)n 1 . −
 The proof of Theorem 1.1 is based only on the graph structure of the circuit. The hope to prove nonlinear lower bounds by graph theo- retical arguments only (described e.g. by Valiant (76 a)) has been de- stroyed. Though it is astonishing, graphs like superconcentrators may have linear size (Bassalygo (82), Gabber and Galil (79), Margulis (75), Pippenger (77 a)). Nevertheless graph theoretical arguments build a powerful tool for all types of lower bound proofs.

 The (up to now) most successful method for general circuits is the elimination method. One replaces some variables in such a way by constants that one obtains a subfunction of the same type (in order to continue by induction) and that one may eliminate several unnecessary gates. A gate G becomes unnecessary if it computes a constant or a variable. If G is not an output gate, it becomes already unnecessary if one input is replaced by a constant. If the other input is g, the output of G is 0, 1, g or g . 0,1 and g are computed elsewhere. If G computes g, we use g and change the type of the successors of G in the appropriate way. The disadvantage of this approach is that we analyze only the top of the circuit. The effect of the replacement of variables by constants on gates far off the inputs is hard to understand. This leads to the prediction that nonlinear lower bounds will not be


-----

**122**

###### proved by the elimination method. We discuss some applications of this method in 2 – 5. § §
 The most promising approach for the proof of nonlinear lower bounds is to analyze the value of each single gate for the compu- tation of the considered function. Such an approach has already been suggested by Schnorr (76 b), but has been applied successfully only for monotone circuits (see Ch. 6).

 In order to gather knowledge on the structure of optimal circuits one might try to characterize the class of all optimal circuits for some function. This problem is already hard. Even simple functions may have a large number of structurally different optimal circuits (see Sat- tler (81) and Blum and Seysen (84)).

 5.2 2n - bounds by the elimination method

 The first bound of size 2n O(1) has been proved by Kloss and − Malyshev (65). We discuss some other applications of the elimination method.

 DEFINITION 2.1 : A Boolean function f ∈ Bn belongs to the class

: : : ;
###### Q[n]2;3 [if for all different i][;][ j][ ∈{][1][;] n} we obtain at least three different subfunctions by replacing xi and xj by constants and if we obtain a subfunction in Q2[n];[−]3[1] (if n ≥ 4) by replacing xi by an appropriate constant ci .

 Q[n]2;3 [is defined in such a way that a lower bound can be proved] easily (Schnorr (74)).

 THEOREM 2.1 : C(f) ≥ 2n − 3 if f ∈ Q[n]2;3 [.]


-----

**123**

###### Proof : Each function f ∈ Q[n]2;3 [is non degenerated. If f would not] depend essentially on xi, f could have at most two subfunctions with respect to xi and xj . Let G be the first gate in an optimal circuit S for f . Because of the optimality of S the predecessors of G are different variables xi and xj . If xi and xj both have fan-out 1, f depends on xi and xj only via G, which may compute only 0 or 1 . Hence f can have at most two subfunctions with respect to xi and xj . W.l.o.g. we may assume that the fan-out of xi is at least 2 . If n = 3, at least 4 edges are leaving the variables, and we may prove the existence of 3 gates by the method of Theorem 1.1. If n ≥ 4, we replace xi by ci . At least the two successors of xi can be eliminated. Furthermore we obtain a circuit for a function in Q[n]2;[−]3[1] containing by induction hypothesis at least 2n 5 gates. Therefore the original circuit contains at least 2n 3 − − gates. 2

 COROLLARY 2.1 : The circuit size of the counting functions C[n]k;3 [is] at least 2n 3 if n 3 . − ≥

 Proof : By Def. 4.2, Ch. 3, C[n]k;3[(x) = 1 iff x][1][+][· · ·][+x][n][ ≡] [k mod 3 . The] restrictions of C[n]k;3 [with respect to x][i][ and x][j][ are the different functions]

;

###### C[n]k;[−]3[2] Ck[n]−[−]1[2];3 [, and C]k[n]−[−]2[2];3 [. If n][ ≥] [4, C]k[n];[−]3[1] [, the subfunction of C]k[n];3 [for]
 xi = 0, is in Q2[n];[−]3[1] [.] 2

 The following lower bound for the storage access function SAn has

;
###### been proved by Paul (77). We repeat that SAn(a x) = x|a| .

 THEOREM 2.2 : C(SAn) ≥ 2 n − 2 .

 Proof : Replacing some address variable ai by a constant has the effect that the function becomes independent from half of the x-variables. Therefore we replace only x-variables, but this does not lead to storage access functions. In order to apply induction, we investigate a larger class of functions.


-----

**124**


###### Let Fs Bn+k be the class of functions f such that ⊆


;
###### x0


; : : : ;
###### xn 1) = x a if a S (2.1)
_−_ _|_ _|_ _|_ _| ∈_


###### f(ak 1
_−_


; : : : ;
###### a0


; : : : ;
###### for some s-element set S ⊆{0 n − 1}. Since SAn ∈ Fn, it is sufficient to prove a 2s − 2 lower bound for functions in Fs . The assertion is trivial for s = 1 . For s 2 we prove that we obtain a ≥ circuit for a function in Fs−1 after having eliminated 2 gates.
 Case 1 : ∃ i ∈ S : xi has fan-out at least 2 . Replace xi by a constant. This eliminates at least the successors of xi . S is replaced by S−{i}.
 Case 2 : ∃ i ∈ S : xi has fan-out 1 and the successor gate G is of type-∧ (see § 2, Ch. 1). Then G computes (x[b]i [∧] [g][c][)][d][ for some function g and]

; ; ;
###### some constants b c d ∈{0 1} . If we replace xi by b, the output of G is replaced by the constant 0[d] . Since the circuit computes a function in Fs−1, G cannot be the output gate. G and its successors, at least 2 gates, can be eliminated.

 Case 3 : ∃ i ∈ S : xi has fan-out 1 and the successor gate G is of type-⊕ (see § 2, Ch. 1). Then G computes xi ⊕ g ⊕ b for some function

;
###### g and some constant b 0 1 . Again G is not the output gate. Let ∈{ } j ∈ S −{i} and |a| = j . The circuit has to compute xj independently from the value of xi . A change of the value of xi leads to a change of the result at G . Since for |a| = j ∈ S−{i} the value of xi does not have any influence on the output, we obtain a function in Fs−1, if we replace xi by an arbitrary function. In particular, we choose the function g . Then G computes the constant b, and G and its successors, at least 2 gates, can be eliminated. 2

 In Ch. 3 we have proved an upper bound of 2n+O(n[1][=][2]) on C(SAn) . An example where upper and lower bound exactly agree is the addition function. The 5n 3 upper bound (Theorem 1.1, Ch. 3, the school − method for addition) has been proved to be optimal by Red’kin (81).


-----

**125**

###### 5.3 Lower bounds for some particular bases

 The proof of Theorem 2.2 makes clear that type- gates are more ⊕ difficult to deal with than type- gates. By replacing one input of a ∧ type- gate by a constant it is impossible to replace its output by a ⊕ constant. Therefore it is not astonishing that lower bounds for the

;
###### basis U2 = B2 −{⊕ ≡} are easier to prove. Schnorr (74) proved that parity requires in U2-circuits three times as many gates as in B2-circuits.

;
###### THEOREM 3.1 : For n ≥ 2 and c ∈{0 1} the B2-circuit complexity of the parity function x1 ⊕· · · ⊕ xn ⊕ c is n − 1 while its U2-circuit complexity equals 3(n 1) . −

 Proof : The assertion on B2-circuits follows from the definition and Theorem 1.1. The upper bound for U2-circuits follows, since x ⊕ y is equal to (x y) (x y) . For the lower bound we prove the existence of ∧ ∨ ∧ some xi whose replacement by a suitable constant eliminates 3 gates. This implies the assertion for n = 2 directly and for n 3 by induction. ≥
 Let G be the first gate of an optimal circuit for parity. The inputs are different variables xi and xj . The fan-out of xi is at least 2 . Other- wise, since G is of type-∧, we could replace xj by a constant such that G is replaced by a constant. This would imply that the output became independent from xi in contradiction to the definition of parity. We replace xi by such a constant that G becomes replaced by a constant. Since parity is not replaced by a constant, G has positive fan-out. We may eliminate G and the successors of G and G[′], where G[′] is another successor of xi . Either these are at least 3 gates, or G[′] is the only successor of G . Then G[′] as successor of G and xi is replaced by a constant, and we can eliminate also the successors of G[′] . In either case we eliminate at least 3 gates. 2


-----

**126**

###### As a further example we compute the complexity of the equality test fn[=] [∈] [B][2n][ defined by]


###### fn[=][(x][1]


; : : : ;
###### xn


;
###### y1


; : : : ;
###### xn) = (y1


; : : : ; :
###### yn) (3.1)


; : : : ;
###### yn) = 1 iff (x1


###### THEOREM 3.2 : C(fn[=][) = 2 n][ −] [1 and C][U]2[(f]n[=][) = 4 n][ −] [1 .]

 Proof : The upper bounds follow, since

 fn[=][(x][;][ y) = (x][1] [≡] [y][1][)][ ∧· · · ∧] [(x][n] [≡] [y][n][)] and (3.2)

:
###### (xi ≡ yi) = (xi ∧ yi) ∨ (xi ∧ yi) (3.3)
 The lower bound on C(fn[=][) follows from Theorem 1.1. The basis of] the induction for the lower bound on the U2-complexity is contained in Theorem 3.1.

;

###### Now it is sufficient to prove the existence of some pair (xi yi) of
 variables and some constant c such that we may eliminate 4 gates if we replace xi and yi by c . Similarly to the proof of Theorem 3.1 we find some variable z, whose replacement by a suitable constant c eliminates 3 gates. Afterwards the function is not independent from the partner z[′] of z . Replacing z[′] also by c eliminates at least one further gate. 2

; ;
###### Red’kin (73) proved that the {∧ ∨ ¬}-complexity of fn[=] [is 5n][ −] [1 .]

; ;
###### Furthermore parity has complexity 4(n 1) in -circuits and − {∧ ∨ ¬}

; ;
###### complexity 7(n 1) in - or -circuits. Soprunenko (65) − {∧ ¬} {∨ ¬} investigated the basis {NAND} . The complexity of x1 ∧· · · ∧ xn is 2(n − 1) whereas the complexity of x1 ∨· · · ∨ xn is 3(n − 1) .


-----

**127**


:
###### 5.4 2 5 n - bounds for symmetric functions

 The 2 n lower bounds for B2-circuits in § 2 were quite easy to prove. No easy proof of a larger lower bound is known. So Paul’s (77)

:
###### 2 5 n bound for a generalized storage access function (of no practical relevance) was a qualitative improvement. Stockmeyer (77) applied the ideas of Paul to several fundamental symmetric functions. Here

; : : : ;

###### the value vector v(f) = (v0 vn) of a symmetric function f ∈ Sn

: : : ;

###### is written as a word v0 vn . By W we denote the words in {0 1}[4]
 having three different subwords of length 2 . W has 8 elements, namely 0100, 0010, 0011, 0110, 1001, 1100, 1011, and 1101 . Stockmeyer proved that symmetric functions where some w W is near the middle ∈ of v(f) are not very easy.

 THEOREM 4.1 : If the value vector v(f) of f ∈ Sn can be written as w[′] w w[′′] where w W and the length of w[′] as well as of w[′′] is at least ∈ k, f has circuit complexity at least 2 n + k 3 . −

 At first we apply this bound to threshold and counting functions.

 COROLLARY 4.1 : C(T[n]k[)][ ≥] [2n + min][{][k][ −] [2][;][ n][ −] [k][ −] [1][} −] [3 if] 2 ≤ k ≤ n − 1 . In particular, C(T[n]⌈n=2⌉[)][ ≥] [2][:][5 n][ −] [5 .]

 Proof : v(T[n]k[) = 0][k][−][2][(0011)1][n][−][k][−][1][ where 0][m][ is a word of m zeros. If]

= :
###### k = n 2, k 2 as well as n k 1 is at least 0 5 n 2 . 2 ⌈ ⌉ − − − −

< <
###### COROLLARY 4.2 : C(C[n]k;m[)][ ≥] [2][:][5 n][ −] [0][:][5 m][ −] [4 if 0][ ≤] [k] m n and m 3 . ≥

 Proof : Exercise. 2

 Proof of Theorem 4.1 : Let S[k]n [be the subclass of symmetric functions] f ∈ Sn whose value vector has the form w[′] w w[′′] for some w ∈ W and


-----

**128**

;
###### words w[′] and w[′′] of a length of at least k . Let C(n k) be the complexity of the easiest function in S[k]n [. Then we have to prove that]

; :
###### C(n k) 2 n + k 3 (4.1) ≥ −

 Subfunctions of symmetric functions f are easy to describe. If v(f) =

: : :

###### v0 vn, the subfunction of f where we replace some xi by 0 or 1, has

: : : : : :

###### value vector v0 vn−1 or v1 vn resp.
 We prove (4.1) by induction on k . For k = 0 we prove S[0]n [⊆] [Q]2[n];3 and apply Theorem 2.1. Since f ∈ S[0]n [, v(f) contains some subword] vm vm+1 vm+2 vm+3 W . Let f00, f01, and f11 be the subfunctions ∈ of f where we have replaced xi and xj both by zeros, by different values, and both by ones resp. We consider only the positions m and m + 1 of the value vectors of f00, f01, and f11 . These subwords are vm vm+1, vm+1 vm+2 and vm+2 vm+3 and by definition of W f00, f01 and f11 are different. If n ≥ 4, we may replace xi by a constant

: : :

###### such that vm vm+3 is a subword of the value vector of the produced
 subfunction f[′] . Hence f[′] ∈ S[0]n−1 [.]
 For k 1 we prove ≥

; ; ; ;
###### C(n k) min C(n 1 k 1) + 3 C(n 2 k 1) + 5 (4.2) ≥ { − − − − }

 by the elimination method. (4.1) can be derived from (4.2) by induc- tion. For the proof of (4.2) it is sufficient to prove that we either may eliminate 3 gates by replacing some xi by a constant (the subfunction of f obviously is in Sn[k][−][1]1[), or we may eliminate 5 gates by replacing]
_−_
###### some xi and xj by different constants (in this case the subfunction of f is in Sn[k][−][1]2[) .]
_−_

###### We investigate an optimal circuit for f ∈ S[k]n [.] Furthermore we choose among all optimal circuits one where the number of edges leav- ing the variables is as small as possible. At the moment we may forget this condition, it will be useful in the last case of the proof. We do not replace more than 2 variables by constants. Since k 1, n 5 ≥ ≥ and we cannot obtain constant subfunctions. Therefore gates being replaced by constants have at least one successor which also can be eliminated.


-----

**129**

###### If some variable xi has fan-out at least 3 or fan-out 2 and some type- gate as a direct successor, we may eliminate 3 gates by replac- ∧ ing xi by an appropriate constant.

 In all other cases we consider the first gate A of the circuit and its different inputs xi and xj . Since f ∈ S[k]n [⊆] [S]n[0] [⊆] [Q]2[n];3 [, we may conclude] as in the proof of Theorem 2.1 that w.l.o.g. xj has fan-out 2 . Let C1 be the second successor of xj and B1 the second successor of xi if such a successor exists. In the following we assume the existence of B1, otherwise the proof is easier.

 By our preliminary remarks all gates A, B1 and C1 are type-⊕ gates. Because of the optimality of the circuit B1 = C1 . We build ̸

; : : : ;

###### the maximal chain of gates C1 Cq such that Cr is of type-⊕ and
 is the only successor of Cr−1 . Hence either Cq is the output gate or it has at least two successors or the only successor is of type-∧ . Let Er be that predecessor of Cr different from Cr−1 . Similarly we build the

; : : : ;

###### chain B1 Bp . The part of the circuit we consider is described in
 Fig. 4.1. The label of a gate describes only the type of the gate. We rebuild this circuit such that the C-chain has length 1 . It is impossible that Bl = Cm . Otherwise xi = xj = 0 and xi = xj = 1 would lead to the same subfunction contradicting f ∈ Q[n]2;3 [. If B][1] [exists, the circuit]


###### xi xj


###### E1


###### A + C1

 E2

+ C2

###### Eq

+ Cq


###### Fig. 4.1


-----

**130**

###### is symmetric with respect to xi and xj . W.l.o.g. we assume that no path leads from Bp to Cq . This implies Bp = Em . Furthermore ̸

<
###### Bl = Em for l p, since otherwise Bl +1 = Cm . Indeed no path can ̸ lead from Bl to Em . Such a path would pass through Bp and could be extended to Cq . Altogether the C-chain receives no information from the B-chain. Let em be the function computed at Em . At Cq we

;
###### compute xj ⊕ e1 ⊕· · · ⊕ eq ⊕ a for some a ∈{0 1} . The intermediate

; : : : ;

###### results at C1 Cq−1 are necessary only for the computation of the

<
###### result at Cq, since all Ci (i q) have fan-out 1 . Without increasing the number of gates or the number of edges leaving the variables we rebuild the circuit by computing at some gate E the function e1 ⊕
 · · · ⊕ eq ⊕ a and at gate C the function xj ⊕ resE . The new situation is shown in Fig. 4.2.

 Either C is the output gate or C has fan-out at least 2 or C has exactly one successor which is of type-∧ . No path leads from B1 to E . Because of the optimality of the circuit A = E . ̸
 It is essential that we do not decide which of the variables xi and xj is replaced by 0 and which is replaced by 1 . In place of that we

;
###### replace for some appropriate e ∈{0 1} xi by resE ⊕e . How can this be done if resE depends on xi and/or xj? Such a dependence is possible

;
###### only via A where resA = xi ⊕ xj ⊕ c for some c ∈{0 1} . Since xi and xj will be replaced by different values, resA will always be replaced by c . At first we replace A by c . Then resE is independent from xi


###### xi xj


###### E


###### B1 + A + C Fig. 4.2


-----

**131**

###### and xj, and we can perform the intended replacements of xi and xj . We obtain a subfunction f[′] ∈ S[k]n[−]−[1]2 [of f . It is sufficient to show that] we can eliminate A, C and 3 further gates. Let G be the set of direct successors of A or C . Since A = E, A, C G . All gates in G can ̸ ̸∈ be eliminated, since at least one input is constant.

 Case 1 : G 3 . We eliminate at least 3 further gates. | | ≥

 Case 2 : G = 2 . Let G be a direct successor of A and H = G be | | ̸ a direct successor of C . Since G = 2, the fan-out of C is bounded | | by 2 . We distinguish three subcases as shown in Fig. 4.3.

 Case 2.1 : C has fan-out 2 . Since resA and resC are constant, also resG is constant. If D ̸= H, we eliminate G, H and D . If D = H, resD is constant, and we eliminate G, H, and the successors of H .

 Case 2.2 : C has fan-out 1 . By construction the only successor H of C is of type- . We choose the constant e (see above) in such a ∧ way that H is replaced by a constant. Therefore H has a successor D .


###### xi xj


###### E


###### E


###### xi xj


###### xi xj E


+ C + A + C + A + C +


###### Case 2.1


###### Case 2.2.a

 Fig. 4.3


###### Case 2.2.b


-----

**132**

###### If D ̸= G, we eliminate G, H, and D (Case 2.2.a). If D = G, resG is constant, and we eliminate G, H, and the successors of G (Case 2.2.b).

 Case 3 : G = 1 . The only successor of A and C is gate G of type- | | ∧ (see Fig. 4.4).

 Case 3.1 : E is a variable, say xm . We show that Case 3.1 is impos
;
###### sible. Because of the optimality of the circuit m i j . For suitable ̸∈{ }

; ; ;
###### constants a b c 0 1 ∈{ }

 resG = (xi ⊕ xj ⊕ a) ∧ (xj ⊕ xm ⊕ b) ⊕ c (4.3)

:
###### = xj(xi ⊕ xm ⊕ 1 ⊕ a ⊕ b) ⊕ xi xm ⊕ a xm ⊕ b xi ⊕ a b ⊕ c
 If we replace xi by 0 and xm by 1 ⊕ a ⊕ b, resG and therefore the whole circuit becomes independent from xj . But the subfunction f[′] of f we have to compute is not constant. Since f[′] is symmetric, it depends essentially on xj . Contradiction.

 Case 3.2 : E is a gate. We rebuild the circuit as shown in Fig. 4.4. The number of gates is not increased, but the number of edges leaving


###### xm


###### xi xj E

 A + C +

 G ∧

 Case 3


###### xi xj


###### Case 3.1 Case 3.2

 Fig. 4.4


###### xi xj E


-----

**133**

###### variables is decreased by 1 . If resG = resG[′], this is a contradiction to our specific choice of the optimal circuit at the beginning of the proof.

; ; ;

###### For suitable constants c0 c1 c2 ∈{0 1}


###### resG = (xi ⊕ xj ⊕ c0) ∧ (xj ⊕ resE ⊕c1) ⊕ c2

 Similarly


:
###### (4.4)


###### resG[′] = (xi ⊕ resE ⊕d0) ∧ (xj ⊕ resE ⊕d1) ⊕ d2 (4.5)

; ; ;

###### where we may choose d0 d1 d2 ∈{0 1} in an arbitrary way. If we
 define d0 = 1 ⊕ c0 ⊕ c1, d1 = c1 and d2 = c2, then resG = resG[′] . Also Case 3.2 is impossible. We have proved (4.2). 2


###### 5.5 A 3n - bound

 The methods of Paul (77) have been further developed by Schnorr (80) whose proof of a 3n-bound is not complete. Blum (84) stepped into the breach. He modified the function considered by Schnorr. Then he could apply many of Schnorr’s ideas in such a way that the problems in Schnorr’s proof discovered by the author do not occur. In contrast to the functions considered up to now this function is of no practical relevance.

; : : : ; ; : : : ;

###### DEFINITION 5.1 : Let n = 2[k], a = (ak 1 a0), b = (bk 1 b0),
_−_ _−_

; : : : ; ; : : : ;

###### c = (ck 1 c0), x = (x0 xn 1) and p, q, r be Boolean variables.
_−_ _−_

###### f ∈ Bn+3k+3 is defined by

; ; ; ; ; ; � �
###### f(a b c p q r x) = q ∧ (x|a| ∧ x|b|) ∨ (p ∧ x|b| ∧ x[r]|c|[)] ∨ (5.1)

:
###### q ∧ (x|a| ⊕ x|b|)

 For p = 0 we obtain the function considered by Paul (77). The object of this section is the proof of the following theorem.


-----

**134**

###### THEOREM 5.1 : C(f) 3 n 3 . ≥ −

 Since f is based on the storage access function, we consider the class

; ;
###### Fs of all functions g ∈ Bn+3k+3 which agree with f if |a| |b| |c| ∈ S for some s-element set S . Since f ∈ Fn, it is sufficient to prove a 3s − 3 lower bound for all g ∈ Fs . This is done by induction on s . For s = 1 the lower bound is trivial. The following cases can be dealt with the methods of 4. §
 – ∃ i ∈ S : xi has fan-out at least 3 .
 – ∃ i ∈ S : xi has fan-out 2 and some direct successor is a gate of type- . ∧
 – ∃ i ∈ S : all direct successors of xi are gates of type-⊕ .

 In all these cases we may replace xi by some constant or some function resE ⊕ e (for a gate E and a constant e) such that we can eliminate 3 gates and obtain a circuit for a function in Fs−1 . The case, that each xi has exactly one successor Gi of type-∧, cannot be excluded here as it could in § 4. If some Gi had at least two successors, we again could eliminate 3 gates by replacing xi by an appropriate constant. Therefore we assume that Qi is the unique successor of the type-∧ gate Gi for i ∈ S . By G and Q we denote the sets of all Gi and Qi .
 In this last case the elimination method was not successful. By a precise analysis of the structure of optimal circuits we prove the existence of 3s 3 gates. −

 LEMMA 5.1 : G contains s gates.

 Proof : Otherwise Gi = Gj for some i ̸= j . Replacing xi by an appropriate constant the output of the circuit becomes independent from xj in contradiction to the definition of Fs . 2


-----

**135**

###### We introduce some notation for the analysis of optimal circuits.

 DEFINITION 5.2 : A path from gate A to gate B is denoted by

;

###### [A B] . R is the output gate where the result is computed. A path

;

###### [A B] is called free if no inner node of the path is contained in G . A gate A is called split if its fan-out is at least 2 . A split B is called free

;
###### if there are free paths [B R] via at least two direct successors of B . A

; ;

###### gate C is a collector of free paths [Gi R] and [Gj R] (i ̸= j) if C lies on
 both paths, and if the paths enter C via different edges.


###### LEMMA 5.2 : If i ∈ S, then there exists a free path [Gi


;
###### R] .


###### Proof : Otherwise we could replace all xj (j ∈ S −{i}) in such a way by constants that resR becomes independent from xi in contradiction to the definition of Fs . 2

; ;

###### LEMMA 5.3 : Let C be a collector of free paths [Gi R] and [Gj R] .
 Then at least one of the statements ( ) or ( ) holds : ∗ ∗∗


###### (∗) There exists a free split B ̸= C on [Gi


; ;
###### C] or [Gj C] .


;

###### (∗∗) C is of type-⊕, and there exists a free path [Gi Gj] or [Gj


;
###### Gi] .


###### Proof : We assume that ( ) and ( ) are both false. ∗ ∗∗
 Case 1 : C is of type-⊕ . We replace all variables but xi and xj by constants. |a| = i, |b| = j, |c| ∈ S, p = 0, q = 1, r and xm (m ̸∈ S)

;
###### arbitrary, xk (k ∈ S −{i j}) such that Gk computes a constant. By definition f is replaced by xi ∧ xj . Since (∗) and (∗∗) both are false, all information on xi and xj is transmitted via the unique free paths

; ;

###### [Gi C] and [Gj C] . One input of C is x[u]i [, the other x]j[v] [, hence its]

; ; ;
###### output is xi ⊕ xj ⊕ w for some u v w ∈{0 1} . The output of C is the same for xi = xj = 0 or xi = xj = 1 . The same must hold for R where xi xj is computed. Contradiction. ∧
 Case 2 : C is of type- . We replace the variables in the same way as ∧ in Case 1 with the only exception that q = 0 . Hence f is replaced by


-----

**136**

###### xi xj . If the result of Gi depends essentially on xj, we shall replace ⊕ xj by an appropriate constant such that the result at Gi and therefore the output at R become independent from xi . This contradicts the fact that xi xj is computed at R . Therefore the result at gate C is ⊕

; ;
###### (x[u]i [∧] [x]j[v][)][w][ for some u][;][ v] w ∈{0 1} and all information on xi and xj is transmitted via C . This is the same contradiction as before, since we may replace xj by v in order to make R independent of xi . 2

 Now it is quite easy to prove that G Q contains exactly 2 s gates. ∪

 LEMMA 5.4 : G Q contains 2 s gates. ∪

 Proof : By Lemma 5.1, G contains s gates. If Qi = Qj for some i ̸= j,

; ;

###### Qi would be the collector of all free paths [Gi R] and [Gj R] . Since
 statement ( ) cannot hold, statement ( ) of Lemma 5.3 holds. A free ∗ ∗∗

;

###### path [Gi Gj] passes Qi and can be extended via Gj to Qj = Qi . The
 circuit would not be cycle free.
 It remains to prove that Gj = Qi . If i = j, this follows by definition. ̸ If i ̸= j and Gj = Qi, all information concerning xi is transmitted via Gj . By an appropriate replacement of xj by a constant the circuit would become independent from xi in contradiction to the definition of Fs . 2

 LEMMA 5.5 : The circuit contains at least s 2 free splits. −

 Before we prove this essential lemma we deduce from it by a wire counting argument the theorem.

 Proof of Theorem 5.1 : At least 2(s 2) free edges (wires) are leaving − free splits by Lemma 5.5. At least 2 of the s gates of Q do not belong to the considered s 2 free splits. By Lemma 5.2 at least one free edge −


-----

**137**

###### is leaving each Qi . We consider the graph consisting of those 2s − 2 free edges we have found and those free paths leading these free edges to R . By definition we do not consider any gate in G . The gates in Q are gathering at most s of these edges, since the other s input edges are entering from gates in G . In order to gather the other s 2 free − edges to the output R further s 3 gates are necessary. 2 −

 Proof of Lemma 5.5 : We choose j ∈ S such that Gj is the last G-gate in the numbering of the gates. In the following we refer always to the

;

###### numbering of gates. Let C be the first collector of free paths [Gk R]

; ;

###### and [Gl R] where k l ∈ S −{j} and k ̸= l . By Lemma 5.3 we either

; ;

###### find a free split D ̸= C on [Gk C] or [Gl C] or we find a free path

; ;

###### [Gk Gl ] or vice versa. By Lemma 5.2 there is a split on [Gk Gl ] . If
 we find a free split on these paths we shall choose the first free split,

; ;

###### otherwise the first split. If the chosen split is on [Gk C] or [Gk Gl ] we
 exclude xk from further consideration, otherwise we exclude xl . At the end of this procedure we have chosen s 2 different splits. −

 We prove that we indeed have chosen s 2 free splits. Otherwise −

; ; ;

###### for some first collector C of free paths [Gk R] and [Gl R] (k l ∈ S −

; ;

###### {j}, k ̸= l ) we cannot find any free split on [Gk C] or [Gl C] . By

;

###### Lemma 5.3 C is of type-⊕ and w.l.o.g. the free path [Gk Gl ] has

;
###### no free split. We prove for all m S k l (including m = j) ∈ −{ }

; ;

###### the existence of a free path [Gm Gk] or [Gm Gl ] in contradiction to
 the choice of j . We assume that this claim is false. We replace all variables but xk, xl, xm and r by constants. |a| = k, |b| = l, |c| = m,

; ;
###### q = 1, p = 1, xi (i ̸∈ S) arbitrary and xi (i ∈ S−{k l m}) such that Gi is replaced by a constant. By definition R is replaced by xk xl xl xm[r] [.] ∨

 Case 1 : The result of Gl does not depend essentially on xk . We replace xm such that Gm is replaced by a constant and r such that x[r]m [= 0 . Then R is replaced by x][k][x][l] [. We deduce a contradiction in] the same way as in Case 1 of the proof of Lemma 5.3.


-----

**138**

###### Case 2 : The result of Gl depends essentially on xk . Then for some

;
###### d ∈{0 1} the result of Gl still depends on xk if we replace r by d . If no

; ;

###### free path [Gm Gk] or [Gm Gl ] exists, then the function computed at Gl

; ;
###### can be represented as (x[u]k [∧] [x]l[v][)][w][ for some u][;][ v] w ∈{0 1} . If xk = u, Gl is replaced by a constant and the circuit becomes independent from xl . But the function computed at R, namely u xl ∨ xl xm[d] [, depends] essentially on xl for arbitrary u and d . Contradiction. 2


###### The lower bound of Theorem 5.1 based on N = n + 3k + 3, the number of variables, is of size 3 N o(N) . −
 The proofs of 4 and 5 are so burdensome that one is convinced § § that this is not the right way to obtain much larger lower bounds. But the reader should not lose his courage and try out his own ideas for the proof of lower bounds.

 5.6 Complexity theory and lower bounds on circuit complexity

 In 1 we have shown that it is easy to define a sequence of provably § hard functions by the simple trick of diagonalization. In this section we discuss more generally whether and how concepts (like diagonal- ization) and results of complexity theory may lead to lower bounds on circuit complexity. Furthermore we discuss the notion ˝explicitly defined˝. For the rest of this section we assume that the reader is familiar with fundamental concepts of complexity theory. But if the reader should not have this knowledge, this section should still give him a better understanding of the problems we are faced with.

 The sequence of functions fn[∗] [defined by diagonalization in][ §][ 1 can be] computed by a Turing machine whose working tape is 2[O(n)]-bounded.

; : : : ; ;

###### For an input x = (x1 xn) ∈{0 1}[n] we may write the table of a


-----

**139**

###### function f ∈ Bn on the working tape and can compute the lexicograph- ical successor of f . We start with the lexicographically first function, the constant 0 . For each function f we produce one after another each � circuit of size 2[n]n[−][1][�] 1 and compare its output with f . If we find − a circuit for f we produce the next Boolean function. Otherwise the considered function f is equal to fn[∗] [, and by table-look-up we compute] the output fn[∗][(x) . Therefore Turing machines with large resources are] powerful enough to construct hard Boolean functions. Nevertheless explicitly defined Boolean functions are defined via Turing machines.

N N
###### DEFINITION 6.1 : Let s: → . The sequence fn ∈ Bn of Boolean functions is s-explicitly defined if the language L = fn[−][1][(1) can be de-]
 [�]n
 cided by a Turing machine whose working tape is bounded by O(s(n)) .

 Because of our above considerations we should not use exponential s . Furthermore, Scarpellini (85) has defined by diagonalization n[k+1]- explicitly Boolean functions fn Bn of circuit size Ω(n[k] log[−][1] n) . But ∈ many fundamental functions (those considered in Ch. 3 e.g.) can be computed on working tapes of polylog length (O(log[k] n)), and many NP-complete functions can be computed at least on linear working tapes. Therefore Definition 6.1 is interesting for functions s growing at most linear.

 Diagonalization is not the only trick to define non explicitly hard functions (see e.g. Ehrenfeucht (72) and Stockmeyer (74)). We shall prove for a whole class of Boolean functions exponential lower bounds. These functions are not defined by diagonalization. Nevertheless they are not s-explicitly defined for any polynomial s .

;
###### DEFINITION 6.2 : A language L 0 1 is called EXP - TAPE ⊆{ }[∗]

;

###### - HARD if each language L[′] 0 1, which can be decided for ⊆{ }[∗] some polynomial p by a Turing machine of working tape 2[p(n)], is polynomially reducible to L (L[′] ≤p L). L[′] ≤p L if there exists a Turing


-----

**140**

###### machine M whose time complexity is bounded by a polynomial and whose output resM(w) for input w is in L iff w ∈ L[′] .

 Meyer and Stockmeyer (72) proved that the following language L is EXP - TAPE - HARD. L consists of all binary codings of two regular expressions for the same language where the coding allows the abbreviation α[2] for the concatenation of α and α .

 THEOREM 6.1 : Let L be EXP - TAPE - HARD. Let gn Bn be ∈

               ###### defined by gn[−][1][(1) = L] [∩{][0][;][ 1][}][n][ . Then for some d,][ ε] 0 and infinitely many n


###### C(gn) ≥ d 2[n][ε]


:
###### (6.1)


###### Proof : Let fn[∗] [be the sequence of Boolean functions defined by]
 [∈] [B][n] diagonalization in § 1. Then C(fn[∗][)][ ≥] [2][n][ n][−][1][ . Let L][′][ be the union of] all fn[∗]−1(1) . Since L′ can be decided by a 2O(n) tape bounded Turing machine, L[′] ≤p L . Let M be a Turing machine for this reduction.

; : : : ;

###### We design a circuit for fn[∗] [consisting of subcircuits for g][1] gn and
 beyond that only a polynomial number of gates. Since C(fn[∗][) is large,] some of the circuits for g-functions cannot be efficient. We apply a result which we shall prove in 2, Ch. 9. If the Turing machine M[∗] §
 is t(n) time bounded and decides L[∗], the circuit complexity of hn, defined by h[−]n [1][(1) = L][∗] [∩{][0][;][ 1][}][n][ is bounded by O(t(n) logt(n)) .]
 Since the reduction machine M is p(n) time bounded for some poly- nomial p, also the length of its output is bounded by p(n) if the input w has length n . We extend the outputs, if necessary, by blanks B such that the output (for each input of length n) has length p(n) .

; ; : : : ; ; ;

###### These outputs can be encoded by (a1 b1 ap(n) bp(n)) ∈{0 1}[2 p(n)]

;

###### where (ai bi) is an encoding of the i -th output letter. By the re sult cited above all ai and bi can be computed by a circuit of size O(p(n) logp(n)) .


-----

**141**

; : : : ;

###### Now we apply in parallel the circuits S1 Sp(n) . Si tests whether

; ; : : : ; ;

###### exactly (a1 b1) (ai bi) are encodings of zeros and ones. It com
; : : : ; ; ;

###### putes x = (x1 xi) ∈{0 1}[i] where xj = 1 iff (aj bj) is an encoding
 of 1 . Then Si applies an optimal circuit for gi to compute gi(x) . Fi- nally Si computes yi such that yi = 1 iff gi(x) = 1 and resM(w) has length i . Hence


###### fn[∗][(w) = 1][ ⇔] [w][ ∈] [L][′][ ⇔] [res][M][(w)][ ∈] [L] (6.2)

:
###### ⇔ y1 ∨· · · ∨ yp(n) = 1

 The so constructed circuit for fn[∗] [contains one copy of an optimal circuit] for gi (1 ≤ i ≤ p(n)) and beyond that q(n) gates for a polynomial q . Therefore

 � : 2[n] n[−][1] ≤ C(fn[∗][)][ ≤] [q(n) +] C(gi) (6.3)

1 i p(n)
_≤_ _≤_


; : : : ;
###### We define i(n) ∈{1 p(n)} such that gi(n) is one of the hardest

; : : : ;

###### functions among g1 gp(n) . By (6.3)

= :
###### C(gi(n)) ≥ (2[n] n[−][1] − q(n)) p(n) (6.4)
 As the results of § 2, Ch. 4, show, C(gi(n)) is bounded by O(2[i(n)] i(n)[−][1]) . Therefore the sequence i(n) has infinitely many different values. Fur- thermore i(n) p(n) cn[k] for appropriate constants c and k implying ≤ ≤

=
###### n (i(n) c)[1][=][k] and ≥

           ###### C(gi(n)) ≥ d 2[(i(n))][ε] for some d, ε 0 . (6.5)

 2

 Many arguments used in this chapter have not been published. Some of them were developed during discussions with several col- leagues, others, I got to know by hearsay. Some of the colleagues who have contributed to these arguments are M. F¨urer, A. Meyer,


-----

**142**

###### W. Paul, B. Scarpellini, and L. Valiant.

 EXERCISES

 1. Apply the simple linear bound (Theorem 1.1) to the functions considered in Ch. 3.

 2. Generalize the simple linear bound to Ω-circuits where Ω ⊆ Br .


###### 3. If f1


; : : : ;
###### fm are different functions


###### C(f1


; : : : ; ; : : : ; :
###### fm) ≥ m − 1 + min{C(f1) C(fm)}


; : : : : : :
###### 4. Let g(x y) = ( (f(x)∆y1) ∆ym) for some ∆ ∈ B2 and some non constant f . For which ∆the equality C(g) = C(f)+m holds ?

 5. Let S be an optimal circuit for f with respect to circuit size. Let g and h be the input functions of the output gate. Then

; =
###### max C(g) C(h) C(f) 2 1 . { } ≥⌈ ⌉−

 6. Let S be an optimal circuit for f with respect to depth. Let g and h be the input functions of the output gate. Then

;
###### max D(g) D(h) = D(f) 1 . { } −

 7. The fulladder for the addition of 3 bits has 5 gates. Prove that a) 4 b) 5 gates are necessary.

 8. Let fn Bn;2 be defined by fn(x) = (x1 xn ; x1 xn) . ∈ ∧· · · ∧ ⊕· · · ⊕
 Then C(fn) = 2n − 2 .

 9. Design optimal circuits for the function fn of Exercise 8 which have (if n 3) gates of fan-out larger than 1 . ≥


-----

**143**

###### 10. Estimate the circuit complexity of fn where fn(x) = 1 iff x1+· · ·+xn is even (0 is not even).

 11. Let fn(x) = (x1 xn 1) (x2 xn) . Then C(fn) = 2n 3 . ⊕· · ·⊕ − ∨ ∧· · ·∧ −

: : : : : :

###### 12. Let fn(x) = x1 xn x1 xn . By the elimination method one
 ∨
 can prove only a lower bound of size n+Ω(1) . Try to prove larger lower bounds.


###### 13. Prove lower bounds for the functions defined in the Exercises 26, 27, and 28 in Ch. 3.

 14. fn[≥] n [(x][;][ y) = 1 iff][ |][x][| ≥|][y][|][ . The B][2][-complexity]
 [∈] [B][2n][ is defined by f][≥] of fn[≥] [is at least 2n][ −] [1, its U][2][-complexity is at least 4n][ −] [3 .]

 15. Let Gn be the class of those functions g ∈ Bn such that for some

; : : : ; ; : : : ; ; : : : ;
###### disjoint partition of 1 n to i(1) i(m), j(1) j(l ) { } { } { }

; : : : ;
###### and k(1) k(l ) { }


###### � g(x) = xi(r) xj(r) xk(r)
 ⊕ [�]
1≤r≤m 1≤r≤l


:


###### Estimate the circuit complexity of functions g ∈ Gn;2 (Satt- ler (81)).

:
###### 16. Almost all f ∈ Sn have circuit complexity bounded below by 2 5 n− o(n) .

 17. Count the number of f ∈ Sn whose value vector does not contain any word in W as a subword. Design efficient circuits for these functions.

 18. Prove Corollary 4.2.


-----

**144**

###### 19. Apply Theorem 4.1 to E[n]k [(see Def. 4.2, Ch. 3).]

 20. Complete the proof of Theorem 5.1.

; ; ; ;
###### 21. Let fn(a b c r x) = x[r]a
_|_ _|_ _[∧]_ [(x][|][b][|][ ⊕] [x][|][c][|][) (compare Def. 5.1). Modify]
###### the proof of Theorem 5.1 and prove that C(fn) ≥ 3n − 3 .

 22. Define a short 0-1-encoding of circuits. Describe how a Turing machine with short working tape can simulate encoded circuits.


-----

**145**

###### 6. MONOTONE CIRCUITS

 6.1 Introduction

 The most important incomplete basis is the monotone basis Ωm =

;
###### . We know already that a Boolean function is computable over {∧ ∨} Ωm iff it is monotone. Although monotone circuits cannot be more effi- cient than circuits over complete bases, the investigation of monotone circuits is a fundamental subject.

 One main problem is the testing of the correctness of circuits. Monotone circuits can be tested much easier than circuits over com- plete bases (see e.g. Lee (78)). Furthermore, the monotone disjunctive normal form is a natural and monotone computation of a monotone function.

 If we replace in a monotone disjunctive normal form for f conjunc- tions by multiplications and disjunctions by additions, we obtain a monotone polynomial p(f) . Lower bounds on the monotone circuit complexity of f imply lower bounds of the same size on the monotone arithmetic complexity of p(f) (see Exercises). Monotone computa- tions of monotone polynomials have absolute numerical stability (see e.g. Miller (75)).


###### Can negations be useful for the computation of monotone func- tions ? The best circuits for sorting and Boolean matrix product

=
###### both include negations (see Ch. 3). How large is Cm(f) C(f) for these and other monotone functions ? The quotient is Θ(log n) for sorting,

=

###### ω(n[1][=][4]) for the Boolean matrix product, and Ω(n[1][=][2] (log[2] n log log n))
 for the Boolean convolution (n is the number of variables). For the log- ical permanent (deciding whether a graph includes a perfect matching) the quotient even is superpolynomial (n[Ω(log n)]). The question whether negation may be exponentially powerful is still not answered.


-----

**146**

=
###### Lower bounds on Cm(f) C(f) require lower bounds on Cm(f) . We present several methods for the proof of polynomial lower bounds and Razborov’s bound for exponential lower bounds.

 Since the logical permanent (see above) has polynomial circuit com- plexity one might suppose that lower bounds on Cm(f) cannot have any implications on C(f) . But for the fundamental class of slice functions f we can prove that Cm(f) − C(f) is bounded by O(n log[2] n) . Therefore lower bounds of size ω(n log[2] n) on Cm(f) imply lower bounds of the same size on C(f) . Since we know NP-complete slice functions, the NP = P-conjecture might be proved by lower bounds on the monotone ̸ circuit complexity. From the theory of slice functions we can learn a lot about the structure of circuits, and we obtain a new model for the proof of lower bounds on the circuit complexity of explicitly defined Boolean functions.

 The theory of slice functions is presented in 13 - 15. In 2 we § § § design efficient monotone circuits for threshold functions and sorting. In 3 - 12 we discuss lower bound methods. The lower bounds § § we obtain may be generalized to many other functions by reduction methods (see also Ch. 10, 3). §

; : : : ; ; : : : ;

###### DEFINITION 1.1 : f(x1 xn) is called a projection of g(y1 ym)

; : : : ; ; : : : ;

###### if f(x1 xn) = g(σ(y1) σ(ym)) for some mapping σ :

; : : : ; ; ; ; ; : : : ; ;

###### {y1 ym} →{0 1 x1 x1 xn xn} . The projection is monotone
 if σ(yj) (1 ≤ j ≤ m) is not a negated variable.


###### PROPOSITION 1.1 : C(f) ≤ C(g) if f is a projection of g . Cm(f) ≤ Cm(g) if f is a monotone projection of g .

 Skyum and Valiant (85) and Valiant (79) studied monotone pro- jections intensively. For a sequence of functions gn Bn and some ∈ Boolean functions f the (monotone) P-complexity of f with respect to (gn) is the smallest m such that f is a (monotone) projection of gm . In this model negation can be exponentially powerful (Skyum (83)) as it can be in arithmetic computations (Valiant (80)).


-----

**147**

###### At the end of this introduction we discuss some properties of mono
; ;
###### tone circuits. Why is it much more difficult to investigate - {∧ ∨ ¬} circuits than to investigate monotone circuits ? If f ∈ Bn is given by

;
###### PI(f) it is a hard problem to compute PI(¬f) . If f g ∈ Mn are given by PI(f) and PI(g) it is easy to compute PI(f g) and PI(f g) . By ∨ ∧ definition

 f g = � t � t[′] = � t: (1.1) ∨ ∨

t PI(f) t[′] PI(g) t PI(f) PI(g)
_∈_ _∈_ _∈_ _∪_


###### We have proved in Theorem 4.2, Ch. 2, that each monotone polynomial for a monotone function includes all prime implicants. Hence

:
###### PI(f g) PI(f) PI(g) (1.2) ∨ ⊆ ∪

 A monom t PI(f) PI(g) is not a prime implicant of f g iff some ∈ ∪ ∨ proper shortening of t is an element of PI(f) PI(g) . Hence we obtain ∪ the following characterization of PI(f g) . ∨

:
###### PI(f g) = t PI(f) PI(g) ∄ t[′] PI(f) PI(g) : t ≨ t[′] (1.3) ∨ { ∈ ∪ | ∈ ∪ }

 No new prime implicant is computed at an -gate. Similarly we con- ∨ clude that

 �� � � � f g = t t[′][�] (1.4) ∧ ∧

t PI(f) t[′] PI(g)
_∈_ _∈_


###### � = t t[′]

t PI(f); t[′] PI(g)
_∈_ _∈_


###### and

; ;
###### PI(f g) = t t[′] t PI(f) t[′] PI(g) (1.5) ∧ { | ∈ ∈

; :
###### ∄ u PI(f) u[′] PI(g) : t t[′] ≨ u u[′] ∈ ∈ }

 We compute PI(f g) by listing all t t[′] where t PI(f) and t[′] ∧ ∈ ∈ PI(g) and by erasing afterwards all monoms for which we find a proper shortening in the list. A prime implicant t of f is also a prime implicant of f g iff some (not necessarily proper) shortening t[′] of t is a prime ∧ implicant of g .


-----

**148**

###### 6.2 Design of circuits for sorting and threshold functions

 The only symmetric and monotone functions are the threshold functions. The sorting function consists of all nontrivial threshold functions. The efficient computation of threshold functions by mono- tone circuits is fundamental for the theory of slice functions. The linear sorting circuit of Ch. 3 is not monotone. In that circuit the inputs xi are summed up which cannot be done in monotone circuits. Most of the well-known sorting algorithms (see e.g. Aho, Hopcroft and Ullman (74)) use if-tests. These algorithms cannot be simulated by

; ; ; ;
###### monotone circuits. But comparisons (x y) (min(x y) max(x y)) →

; ;
###### can be realized easily by two gates (x y) (x y x y) . We use → ∧ ∨

; : : : ;

###### these comparisons as basic gates. The variables x1 xn are given

; <
###### in an array A . The meaning of the basic step (i j) (1 i j n) is ≤ ≤ the following. We compare A(i) and A(j) and store the minimum at array place i and the maximum at array place j . Algorithms of this type are called sorting networks.

 It is easy to simulate the well-known bubble sort. In step k

; ; : : :
###### (0 k n 2) we carry out the basic steps (1 2), (2 3),, ≤ ≤ −

;
###### (n k 1 n k). Afterwards the k + 1 largest inputs are in increas- − − −

; : : : ;
###### ing order at the array places n k n . The large inputs climb up − �n� the array like bubbles. Altogether comparisons and n(n 1) mono2 _−_
###### tone gates are sufficient for the computation of the sorting function. If we want to compute T[n]k [we may stop the sorting algorithm after] step k − 2 . T[n]k [is the disjunction of the elements at the array places]

; : : : ;
###### 1 n + 1 k . Hence −
 Cm(T[n]k[)][ ≤] [2 ((n][ −] [1) +][ · · ·][ + (n][ −] [k + 1)) + (n][ −] [k)] (2.1)

:

###### = 2 (k 1)n k[2] − −

 This result is interesting for small k . For large k we apply the du- ality principle for monotone functions. The dual function fd of f is

; : : : ;

###### ¬f(x1 xn) . By the rules of de Morgan we obtain a monotone cir cuit for fd by replacing in a monotone circuit for f ∧-gates by ∨-gates


-----

**149**

###### and vice versa. Obviously Cm(f) = Cm(fd) . The dual function of T[n]k

; : : : ;

###### is ¬T[n]k[(x][1] xn) . (T[n]k[)][d][ computes 1 iff at most k][ −] [1 of the negated]
 variables are 1 iff at least n k + 1 of the variables are 1 . Hence − (T[n]k[)][d][ = T][n]n−k+1 [. We summarize our results.]


###### PROPOSITION 2.1 : i) Cm(T[n]k[) = C][m][(T][n]n k+1[) .]
_−_

###### ii) Cm(S[n]) ≤ n(n − 1) .
 iii) Cm(T[n]k[)][ ≤] [(2k][ −] [1)n][ −] [k][2][ .]

 The reader is asked to look for improvements of these simple upper bounds. We present a sorting network (Batcher (68)) whose size is O(n log[2] n) and whose depth is O(log[2] n) . This sorting network is based on the ˝sorting by merging˝ principle. W.l.o.g. n = 2[k] .

 ALGORITHM 2.1.a :


###### Input : Boolean variables x1


; : : : ;
###### xn .


###### Output : S[n](x1


; : : : ;
###### xn) = (T[n]n[(x][1]


; : : : ; ; : : : ;
###### xn) T[n]1[(x][1]


; : : : ;
###### xn)) .


###### Step 1. If n = 1 nothing has to be done.
 Step 2. If n = 2[k] > 1 call this algorithm for x1 ; : : : ; xn=2 and for
 xn=2+1 ; : : : ; xn . This can be done in parallel.

 Step 3. Use a merging algorithm to merge the two output sequences of Step 2.

 Batcher designed an efficient monotone merging circuit. Merging is much easier in non monotone circuits where we can simulate if-tests. Batcher’s merging algorithm is recursive. Let a1 am and ≤· · · ≤ b1 bm be the sorted input sequences. ai may be smaller than ≤· · · ≤ b1, but ai also may be larger than bm . Altogether m+1 rank numbers are possible for ai . We merge the subsequences of elements with odd indices and also the subsequences of elements with even indices (odd- even-merge). After having done this we still have to merge two sorted


-----

**150**

###### lists. But only two rank numbers are possible for each element.

 ALGORITHM 2.1.b :


###### Input : a1


; : : : ;
###### am and b1


; : : : ;
###### bm, two sorted lists of Boolean variables.


###### Output : z1


; : : : ;
###### zn (n = 2m), the sorted list of all ai and bj .


###### Step 1. If m = 1 one comparison is sufficient.

    ###### Step 2. If m 1 call this algorithm for the sequences of all ai (i odd) and all bj (j odd), and also call this algorithm for the sequences of all ai (i even) and all bj (j even). This can be done in parallel. Let

; : : : ; ; : : : ;

###### v1 vm and w1 wm be the output sequences.
 Step 3. Compute by m − 1 (parallel) comparisons z1 = v1, zn = wm,

; ;

###### z2i = min{vi+1 wi} and z2i+1 = max{vi+1 wi} for 1 ≤ i ≤ m − 1 .


###### We prove the correctness of Algorithm 2.1. This is obvious for

; : : : ;

###### part a. Let k and l be the number of zeros in (a1 am) and

; : : : ; =

###### (b1 bm) resp. ⌈k 2⌉ of the 0-elements of the a-sequence have

=
###### an odd index, and k 2 have an even index. Hence the v-sequence ⌊ ⌋

= =
###### contains p = k 2 + l 2 zeros, and the w-sequence contains q = ⌈ ⌉ ⌈ ⌉

= =
###### k 2 + l 2 zeros. Obviously 0 p q 2 . For the three possible ⌊ ⌋ ⌊ ⌋ ≤ − ≤ values of p q we represent the v- and the w-sequence in such a way − that wi, which we compare with vi+1 in step 3, stands below vi+1 .


###### p

: : : : : :
###### 0 0 0 0 1 1

: : : : : :
###### 0 0 1 1 1 1 p q = 2 −


###### p

: : : : : :
###### 0 0 0 1 1 1

: : : : : :
###### 0 0 0 1 1 1 p q = 0 −


###### p

: : : : : :
###### 0 0 0 0 1 1

: : : : : :
###### 0 0 0 1 1 1 p q = 1 −


-----

**151**

; : : : ;

###### Now it is obvious that z1 zn is the sorted sequence of the in puts. What is the complexity of Batcher’s algorithm ? Let M(m) and DM(m) be the number of comparisons and the depth of the merging algorithm for m a power of 2 .

= ;
###### M(m) = 2 M(m 2) + m 1 and M(1) = 1 hence (2.2) −

:
###### M(m) = m log m + 1 (2.3)

= ;
###### DM(m) = DM(m 2) + 1 and DM(1) = 1 hence (2.4)

:
###### DM(m) = log m + 1 (2.5)

 Let S(n) and DS(n) be the number of comparisons and the depth of Batcher’s sorting algorithm for n = 2[k] .

= = ;
###### S(n) = 2 S(n 2) + M(n 2) and S(1) = 0 hence (2.6)

= ;
###### S(n) = n(log n)(log n 1) 4 + n 1 (2.7) − −

= = ;
###### DS(n) = DS(n 2) + DM(n 2) and DS(1) = 0 hence (2.8)

= :
###### DS(n) = (log n)(log n + 1) 2 (2.9)

 DEFINITION 2.1 : The merging function M[n] is the partial Boolean function which is equal to the sorting function if x1 x n=2 and ≤· · · ≤ ⌊ ⌋ x⌊n=2⌋+1 ≤· · · ≤ xn .

 THEOREM 2.1 : If n = 2[k]

= ;
###### Cm(S[n]) ≤ n(log n)(log n − 1) 2 + 2 n − 2 (2.10)

= ;
###### Dm(S[n]) ≤ (log n)(log n + 1) 2 (2.11)
 Cm(M[n]) ≤ n log n − n + 2 and (2.12)

:
###### Dm(M[n]) ≤ log n (2.13)


###### Batcher’s algorithm is appropriate for practical purposes. Not only

; : : : ;

###### x1 xn is sorted but also all blocks of length 2[i] (1 ≤ i ≤ k) namely


-----

**152**

; : : : ; <

###### xj+1 xj[′] where j = r 2[i] (0 ≤ r 2[k][−][i]) and j[′] = j + 2[i] are sorted.
 In 4 we prove that Batcher’s merging algorithm is asymptotically § optimal. The upper bound for sorting has been improved by Ajtai, Koml´os and Szemer´edi (83).

 THEOREM 2.2 : One can design a sorting network of size O(n log n) and depth O(log n) .

 We do not present this AKS sorting network as it is rather com- plicated. Theorem 2.2 is a powerful theoretical result. But the AKS sorting network beats Batcher’s sorting network only for very large n, in particular, only for n larger than in real life applications (see e.g. Paterson (83)). The AKS sorting network sorts the input sequence but no subsequence. It is an open problem whether Batcher’s algorithm can be improved significantly for small n .

 For the majority function we do not know of any monotone circuit of size o(n log n) . The monotone complexity of the majority function is still unknown. For constant k we improve Proposition 2.1. We design a monotone circuit of size kn + o(n) . This result has been announced by Adleman and has been proved by Dunne (84). The conjecture that kn o(n) monotone gates are necessary is also open. −

 THEOREM 2.3 : Cm(T[n]k[)][ ≤] [kn + o(n) for constant k .]


###### Proof : T[n]k [is the disjunction of all monotone monoms of length k .]

; : : : ; ; : : : ;

###### If B1 Br form a partition of X = {x1 xn} the function

: : : ;
###### T[r]k[(T][1][(B][1][)][;] T1(Br)) has only prime implicants of length k . The number of prime implicants is large if all Bi are of almost the same size. Certainly, we do not obtain all prime implicants of length k . Therefore we use several partitions of X .
 For the sake of simplicity we concentrate on those n where n = p[k]
 for some natural number p . Let p(k) = p[k] and r = p(k 1) . We −


-----

**153**

; : : : ;

###### prove that k partitions B[q]1 B[q]p(k−1) [(1][ ≤] [q][ ≤] [k) are sufficient,]
 namely that


###### � � : : : ; �: T[p(k)]k (X) = Tk[p(k][−][1)] T[p]1[(B][q]1[)][;] T[p]1[(B][q]p(k 1)[)] (2.14)

_−_
1 q k
_≤_ _≤_

###### In order to obtain all monoms of length k, we have to ensure for all

; : : : ; ; : : : ;
###### different j(1) j(k) the existence of some q such that xj(1) xj(k)
 are elements of different sets of the q-th partition. Such a construc- tion will be explained later. At first we estimate the size of the cir- cuit. For the computation of T[p]k [at the end we apply the circuit of] Proposition 2.1. Besides the computation of T[p(k]k [−][1)] we only need k 1 + k(n p(k 1)) k n gates. Since p = n[1][=][k] − − − ≤
 Cm(T[p(k)]k ) ≤ k n + k Cm(T[p(k]k [−][1)]) (2.15)
 � = = : : : � : k n 1 + (k p) + (k p)[2] + + k[k][−][1](2 k p) = k n + o(n) ≤

; : : : ; ; : : : ;
###### A number r 1 p[k] or r 1 p[k][−][1] is represented by ∈{ } ∈{ }

; : : : ; ; : : : ; ; : : : ;

###### a vector r = (r1 rk) 0 p 1 or r = (r1 rk 1)
 ∈{ − }[k] − ∈

; : : : ;
###### {0 p − 1}[k][−][1] . For 1 ≤ r ≤ p[k][−][1] the set B[q]r [includes the p variables]

; : : : ; ; ; ; : : : ;

###### xi where i = (r1 rq−1 j rq rk−1) for some 0 ≤ j ≤ p − 1 . It is
 obvious that the sets B[q]r [(1][ ≤] [r][ ≤] [p][k][−][1][) build a partition of X . We]

; : : : ; ; : : : ;
###### claim that we find for different j(1) j(k) 1 p[k] some q such ∈{ }

; : : : ;

###### that xj(1) xj(k) are in different sets of the q-th partition.

 If xi and xj are in the same set Br[q] [, i and j agree at all but the][ q][-th]

;

###### position. If i ̸= j and q ̸= q[′], it is impossible that xi xj ∈ B[q]r [∩][B]r[q][′][′][ . This]

         ###### proves the claim for k = 2 . For k 2 either q = k is appropriate or two indices, w.l.o.g. j(k 1) and j(k), agree on all but the last position. We − obtain j[′](l ) by cancelling the last position of j(l ) . Then j[′](k 1) = j[′](k) −

; : : : ;
###### and among j[′](1) j[′](k) are at most k 1 different vectors. We obtain − B[′][q]r [(1][ ≤] [q][ ≤] [k][ −] [1) by cancelling the last position of all elements in]

: : : ;
###### B[q]r [. By induction hypothesis we find some q][ ∈{][1][;] k − 1} such that for l ̸= m either j[′](l ) = j[′](m) or xj′(l ) and xj′(m) are not in the same set B[′][q]r [. This q is appropriate. If j][′][(][l] [) = j][′][(m), j(][l] [) and j(m)] differ at the last position, hence xj(l ) and xj(m) are for l ̸= m not in the same set B[q]r [.] 2


-----

**154**

###### 6.3 Lower bounds for threshold functions

 We consider T[n]1 [, T]2[n] [, T]3[n] [and the majority function T][n]⌈n=2⌉ [.] By C[∨]m[(f) and C][∧]m[(f) we denote the minimal number of][ ∨][-gates and][ ∧][-ga-] tes resp. in a monotone circuit for f . In monotone circuits we cannot apply the deMorgan rules, and we cannot replace -gates by -gates ∧ ∨ or vice versa. Alon and Boppana (85) proved that many -gates are ∨ only useful if there also are several -gates available. ∧

 PROPOSITION 3.1 : Let f ∈ Mn . Then for k = max{C[∧]m[(f)][;][ 1][}]

k 1
###### � − � : C[∧]m[(f) + C][∨]m[(f)][ ≤] [C][m][(f)][ ≤] [k n +] 2 − 1 (3.1)

 Proof : The first inequality is obvious as is the second inequality for

      ###### C[∧]m[(f) = 0 . For C][∧]m[(f)] 0 let us consider a monotone circuit for f with

; : : : ;

###### k ∧-gates, and let f1 fk−1 be the outputs of the first k − 1 ∧-gates
 and let fk = f . It is sufficient to prove that fi can be computed out

; : : : ; ; ; : : : ;

###### of the ˝inputs˝ x1 xn f1 fi−1 with n + i − 2 additional gates.
 fi = s1 (s2 s3) where sj is the disjunction of some of the ˝inputs˝. ∨ ∧ If input t is in s1, then it can be cancelled in s2 and s3 . Hence we can

;

###### choose s1 s2 and s3 in such a way that each input is contained in at
 most one sj . By this representation we can compute fi with at most n + i 2 additional gates. 2 −


###### THEOREM 3.1 : i) C[∧]m[(T][n]1[) = 0, C][∨]m[(T][n]1[) = C][m][(T][n]1[) = n][ −] [1 .]
 ii) C[∧]m[(T][n]2[) =][ ⌈][log n][⌉] [, C][∨]m[(T][n]2[) = 2n][ −] [4 .]

    ###### iii) Cm(T[n]2[)] 2n − 4 + ⌈log n⌉ .

 Proof : Part i) is obvious. The first claim of Part ii) is left as an exercise. We omit the proof of Part iii) (Bloniarz (79)). Later we get

<
###### to know another example where C[∧]m[(f) + C][∨]m[(f)] Cm(f) .


-----

**155**

###### We only prove that C[∨]m[(T][n]2[) = 2n][ −] [4 . In a sorting network the]

; : : : ; ;
###### following 2n 3 comparisons are sufficient (1 2),, (n 1 n), (1 2), − −

: : : ;
######, (n 2 n 1) . We may save one -gate, since we do not have to − − ∨ compute T[n]1 [, the maximum of the comparison (n][ −] [1][;][ n) . This proves] the upper bound.

 The lower bound is proved by the elimination method and induc
               ###### tion on n . The claim is obvious for n = 2 . For n 2 we consider a monotone circuit for T[n]2 [with the minimal number of][ ∨][-gates. It is] sufficient to find some i such that the replacement xi = 0 eliminates at least 2 -gates. ∨

 Let G be the first gate of the circuit. Its predecessors are different variables xi and xj . The outdegree of xi is at least 2 (see Ch. 5). Each path from xi to the output gate contains an ∨-gate. Otherwise xi = 0 would replace T2[n] [by 0 . The first][ ∨][-gates on these paths may be] eliminated. The only case to be considered, is that one where only one such -gate H exists. Let I and J be the predecessors of H . If there ∨ are paths from xi to I and from xi to J we replace the outputs of I, J and H by 0 for xi = 0 . Similarly to the above arguments each path from H to the output gate contains an -gate, and the first -gate can ∨ ∨ also be eliminated. Otherwise there is no path from xi to (w.l.o.g.) I . All paths from xi to the output pass through J . In particular, there is some path from xj via G to J consisting of ∧-gates only. If xj = 0, resJ is replaced by 0, and the output becomes independent from xi in contradiction to the fact that T[n]2 [is replaced by T]2[n][−][1] for xj = 0 . 2

 We only cite the largest lower bounds known on Cm(T[n]3[) and] Cm(T[n]n=2
_⌈_ _⌉[) (Dunne (84)).]_

###### THEOREM 3.2 : Cm(T[n]3[)][ ≥] [2][:][5 n][ −] [5][:][5 .]

 THEOREM 3.3 : Cm(T[n]n=2
_⌈_ _⌉[)][ ≥]_ [3][:][5 n][ −] [O(1) .]


-----

**156**

###### We prove a weaker result containing most of the ideas of the proof of Theorem 3.3. Theorem 3.4 combined with Theorem 3.2 leads to a 3:25 n − 11 lower bound on Cm(T⌈n=2⌉) .

 THEOREM 3.4 : Cm(T[n]n=2 3[) + 4(n][ −] [l] [)][ −] [1 for some]
_⌈_ _⌉[)][ ≥]_ [C][m][(T][l]

=
###### l n 2 + 3, if n 5 . ≤⌊ ⌋ ≥

                ###### Proof : If n = 5 or n = 6 we may choose l = n . If n 6 we apply the elimination method. We prove that we can eliminate at least 4 or 8 gates by replacing 1 or 2 variables resp. by constants. This replacement is performed until we obtain a subfunction T[l]3 [, T]l[l] −2 [,] T2[l] [−][1] or Tl[l] −[−]2[1] [. In the last two cases we replace in the last step only one] variable. Then we eliminate at least 3 gates. Altogether we eliminate at least 4(n − l ) − 1 gates and obtain a circuit for T[l]3 [or T]l[l] −2 [. By] the duality principle Cm(T[l]3[) = C][m][(T][l]l 2[) . It is easy to see that][ l][ ≤]
_−_

=
###### n 2 + 3 . ⌊ ⌋

< <
###### We investigate a monotone circuit for T[r]k [where 3] k r − 2 .
 Case 1 : ∃ xi : outdegree(xi) ≥ 3 or outdegree(xi) = 2 and one of the direct successors of xi has outdegree bounded below by 2 .
 We replace xi by a constant in such a way that a direct successor of the highest outdegree is replaced by a constant. At least 4 gates can be eliminated.

 Case 2 : ∃ xi : outdegree(xi) = 2 and the direct successors of xi are of the same type, w.l.o.g. of type- . ∧
 We can eliminate at least 4 gates if xi is replaced by 0 .

 In all other cases we consider some gate G where a longest path of the circuit starts. The inputs of G are different variables xi and xj of outdegree 2 . W.l.o.g. G is of type- . The other direct successors of ∨ xi and xj, namely G1 and G2, are of type-∧ . The gates G, G1 and G2 have outdegree 1 . The situation is shown in Fig. 3.1.


-----

**157**


###### xj


###### h


###### xi

 G1 ∧ G

 G3


###### Fig. 3.1


###### If G3 is of type-∧, we can eliminate at least 4 gates if xi = 0 . Therefore we assume that G3 is of type-∨ and, with similar arguments, that G4 is of type-∧ . In particular G3 ̸= G4 . Since the longest path of the circuit starts at G, either g = xk or g = xk xl or g = xk xl . If ∧ ∨ g = xk, outdegree(xk) ≥ 2 . Otherwise the circuit is independent from xk if xi = xj = 0 . If xk = 0 we can eliminate at least 4 gates: G, G4, the direct successors of G4 and the other direct successor of xk . If g = xk xl or g = xk xl we go through the same discussion about ∧ ∨ G[′], the gate where g is computed. The only situation we still have to discuss is described in Fig. 3.2.

 If xi = xj = 0, we can eliminate G, G1, G2 and G5 and hence also G[′] . Since G1, G2 and G5 are replaced by 0, we can even eliminate 3 additional gates. If only one variable is to be replaced, we choose


###### xi

 G1 ∧ G


###### xj


###### xk xl

 G ∨ G

 Fig. 3.2


-----

**158**

###### xi = 0 . At least 3 gates can be eliminated. We should mention that G1 = G2 . Otherwise the output would be independent from xi if ̸ xj = xk = xl = 0 . 2

 Before Razborov’s superpolynomial lower bounds were discovered (see 10 - 12) the following bound based on Theorem 3.1 and the duality § § principle was the largest one for explicitly defined monotone functions of one output (Tiekenheinrich (84)).

 THEOREM 3.5 : Cm(f) ≥ 4n − 12 for f ∈ Mn defined by


; : : : ;
###### xn−1) ∨ (xn ∧ T[n]2[−][1](x1


###### f(x1


; : : : ;
###### xn) = Tn[n][−]2[1][(x][1]
_−_


; : : : ;
###### xn 1)) (3.2)
_−_


###### Proof : C[∨]m[(f)][ ≥] [2(n][ −] [1)][ −] [4 = 2n][ −] [6, since T][n]2[−][1] is a subfunction of f (for xn = 1) . Cm[∧] [(f)][ ≥] [2n][ −] [6, since T][n]n[−]−[1]2 [is a subfunction of f (for] xn = 0) and Cm[∧] [(T]n[n][−]2[1][) = C]m[∨] [(T][n]2[−][1]) by the duality principle. 2
_−_

###### 6.4 Lower bounds for sorting and merging

 We prove Ω(n log n) lower bounds for sorting as well as for merging. Because of these lower bounds the AKS sorting network and Batcher’s merging network are asymptotically optimal. The lower bound for merging implies the lower bound for sorting. Nevertheless we present a simple proof for the lower bound on sorting (Lamagna (75), Lamagna and Savage (74), Pippenger and Valiant (76), van Voorhis (72)).

 THEOREM 4.1 : Cm(S[n]) ≥ log(n!) ≥ n log n − O(n) .

 Proof : log(n!) = n log n O(n) by Stirling’s formula. We apply the − elimination method. We prove the existence of some input xi such


-----

**159**

###### that ⌈log n⌉ gates can be eliminated if xi = 0 . Afterwards the circuit computes S[n][−][1] . Hence

:

###### Cm(S[n]) ≥⌈log n⌉ + Cm(S[n][−][1]) ≥ [�] ⌈log i⌉≥ log(n!) (4.1)

1 i n
_≤_ _≤_

###### If xi = 0, Tn[n] [is replaced by the constant 0 . In a monotone circuit] we compute the constant 0 at some gate G only if at some input of G the constant 0 is computed. By backtracking we find a path Pi from xi to the output Tn[n] [such that all gates compute 0 if x][i][ = 0 . Since the] indegree of all gates is 2, at least one path Pi (1 ≤ i ≤ n) is of length not smaller than ⌈log n⌉ . We replace the corresponding input xi by 0 . 2

 The lower bound for the merging function has been proved by La- magna (79).

=
###### THEOREM 4.2 : Cm(M[n]) ≥ (1 2)n log n − O(n) .


###### Proof : Let n = 2k . We only consider inputs where xk ≤· · · ≤ x1

; : : : ; ; : : : ;

###### and yk ≤· · · ≤ y1 . Then the outputs are T1[n] T[n]n [. T]i[n] T[n]i+k
 depend essentially on xi . If x1 = · · · = xi−1 = 1, xi+1 = · · · = xk = 0, y1 = · · · = yj = 1 and yj+1 = · · · = yk = 0, then T[n]i+j [is equal to x][i][ .] In this situation only the functions 0, 1 and xi are computed in the circuit. xi can be computed at gate G only if at least one input equals xi . Therefore there is some path from input xi to output T[n]i+j [such] that at each gate on this path xi is computed.

;
###### Let d(i j) be the length of a shortest path from xi to T[n]j [if i][ ≤] [j][ ≤]

;
###### i + k and d(i j) = 0 else. Let e(j) = j, if j k, and e(j) = n j + 1, ≤ −

 ###### if j k . Then at least e(j) x-variables are connected with output T[n]j [.]

;
###### Hence, for fixed j, the sum of all d(i j) is the external path length of some binary tree with at least e(j) leaves. The following lower bound on the external path length is well-known (or can be proved as an easy


-----

**160**

###### exercise).
 � ; :
 d(i j) e(j) log e(j) 2[⌈][log e(j)][⌉] + e(j) =: t(j) (4.2) ≥ ⌈ ⌉−
1 i k
_≤_ _≤_

; : : : ;

###### Let y1 = · · · = yl = 1 and yl +1 = · · · = yk = 0 . Then T[n]l +1 T[n]l +k
 are not constant. If x1 = · · · = xk = 0 they all compute 0 . We increase

; : : : ;

###### at first x1, then x2 then xk from 0 to 1 . The output T[n]l +i [switches]
 from 0 to 1 after we have switched xi . We find some path p(i) from xi to T[n]l +i [such that the results at all gates switch at that moment from 0]

; : : : ;
###### to 1 . Because of monotonicity these paths p(1) p(k) are disjoint. Hence we have proved the existence of
 � ;
 d(i i + l ) (4.3)
1 i k
_≤_ _≤_

###### gates. The largest of these lower bounds is at least as large as the average lower bound.


###### 1
 � � ;
 Cm(M[n]) ≥ d(i i + l ) (4.4)
 k + 1 0 l k 1 i k

_≤_ _≤_ _≤_ _≤_

###### 1 1
 � � ; �
 = d(i j) t(j)
 ≥
 k + 1 1 j n 1 i k k + 1 1 j n

_≤_ _≤_ _≤_ _≤_ _≤_ _≤_

###### = [1]
 2[n log n][ −] [O(n)]
 by (4.2) and the definition of e(j) . 2

 6.5 Replacement rules

 A replacement rule for monotone circuits is a theorem of the fol- lowing type: ˝If some monotone circuit for f computes at some gate G a function g with certain properties and if we replace gate G by a circuit for the monotone function h (depending perhaps on g), then the new circuit also computes f .˝ If h is a constant or a variable, the given circuit is not optimal. In particular, we obtain results on


-----

**161**

###### the structure of optimal monotone circuits. Later we apply replace- ment rules also in situations where h is a more complicated function. Nechiporuk (71) and Paterson (75) used already replacement rules. Mehlhorn and Galil (76) presented the replacement rules in the gen- eralized form we discuss here.

 It is easy to verify the correctness of the replacement rules, but it is difficult and more important to get a feeling why such replacement rules work. Let g be computed in a monotone circuit for f . If t ∈ PI(g) but t t[′] PI(f) for all monoms t[′] (including the empty monom), ̸∈ t is of no use for the computation of f . At -gates t can only be ∧ lengthened. At -gates either t is saved or t is eliminated by the law ∨ of simplification. Because of the conditions on t we have to eliminate t and all its lengthenings. Hence it is reasonable to conjecture that g can be replaced by h where PI(h) = PI(g) t . If all prime implicants −{ } of f have a length of at most k and if all prime implicants of g have a length of at least k + 1, we can apply the same replacement rule several times and can replace g by the constant 0 .

;
###### THEOREM 5.1 : Let f g ∈ Mn and t ∈ PI(g) where t t[′] ̸∈ PI(f) for all monoms t[′] (including the empty monom). Let h be defined by PI(h) = PI(g) t . If g is computed in some monotone circuit for f −{ } and if we replace g by h the new circuit also computes f .

 Proof : Let S be the given circuit for f and let S[′] be the new circuit computing f[′] . By definition h g . Hence by monotonicity f[′] f . If ≤ ≤ f[′] = f we choose some input a where f[′](a) = 0 and f(a) = 1 . Since ̸ we have changed S only at one gate, h(a) = 0 and g(a) = 1 . Since g = h t, t(a) = 1 . Let t[∗] be a prime implicant of f where t[∗](a) = 1 . ∨ We prove that t is a submonom of t[∗] in contradiction to the definition of t .

 Let xi be a variable in t . ai = 1 since t(a) = 1 . Let bi = 0 and bj = aj if j ̸= i . Obviously b ≤ a and t(b) = 0 . Hence f[′](b) = 0, h(b) = 0 and g(b) = 0 . For input b the circuits S and S[′] compute the


-----

**162**

###### same output since they compute the same value at that gate where they differ. Hence f(b) = f[′](b) = 0 . In particular t[∗](b) = 0 . Since b and a differ only at position i, xi is a variable in t[∗] and t is a submonom of t[∗] . 2

 THEOREM 5.2 : Let g ∈ Mn be a function which is computed in some monotone circuit S for f ∈ Mn . Let t, t1 and t2 be monoms such that


###### t t1


;
###### t t2 ∈ I(g) and (5.1)


###### ∀ t[∗] monom : t[∗] t t1


; :
###### t[∗] t t2 ∈ I(f) ⇒ t[∗] t ∈ I(f) (5.2)


###### If we replace g by h = g t the new circuit S[′] also computes f . ∨

 We motivate the replacement rule by the following considerations. We assume that t t1 and t t2 are even prime implicants of g . Follow- ing the discussion for the first replacement rule only (not necessarily proper) lengthenings of t t1 and t t2 are useful for the computation of f . Since both monoms are prime implicants of the same function, ˝ S treats t t1 the same way as t t2 ˝. By (5.2) for all common useful lengthenings of t t1 and t t2 already the appropriate lengthening of t is useful. In h = g ∨ t we replace t t1 and t t2 by t .

 Proof of Theorem 5.2 : Let f[′] be the function computed by S[′] . f[′] f ≥ by monotonicity since h g . If f[′] = f we choose some input a where ≥ ̸ f[′](a) = 1 and f(a) = 0 . In particular h(a) = 1, g(a) = 0 and t(a) = 1 . We choose t[′] PI(f[′]) where t[′](a) = 1 . If t t[′] I(f), we could conclude ∈ ∈ that f(a) = 1 in contradiction to the construction of a . By (5.2) it is sufficient to prove t[′] t tj ∈ I(f) for j = 1 and j = 2 . Let b be an input where t[′] t tj(b) = 1 . Then f[′](b) = 1 (since t[′] ∈ PI(f[′])), g(b) = 1 (since t tj ∈ I(g)) and h(b) = 1 (since h ≥ g). For input b the circuits S and S[′] compute the same output since they compute the same value at that gate where they differ. Hence f(b) = f[′](b) = 1 . Altogether t[′] t tj ∈ I(f) since t[′] t tj(b) = 1 implies f(b) = 1 . 2


-----

**163**

###### 6.6 Boolean sums

 A Boolean sum f with one output is the disjunction of some, e.g. s, variables. Obviously Cm(f) = C{∨}(f) = s − 1 . The class of Boolean sums f ∈ Mn;n with n outputs has been investigated very thoroughly, since on the one hand the complexity of each single output is well- known, but on the other hand it is difficult to determine the complexity of n-output functions. At first we prove lower bounds on C (f), and
_{∨}_
###### then we prove that -gates are only of little help for Boolean sums. ∧

 DEFINITION 6.1 : A Boolean sum f ∈ Mn;n is called (h; k)-disjoint, if each sample of h + 1 outputs has at most k common summands.

 The following results are based on Mehlhorn (79) who generalized the results of Nechiporuk (71) and Wegener (80). Independently Pip
;
###### penger (77) investigated (2 2)-disjoint Boolean sums.


###### LEMMA 6.1 : Let f = (f1 ; : : : ; fn) ∈ Mn;n and let fi be a Boolean sum
 of si variables. Then � ��sik[−][1][�] − 1�h[−][1] ≤ C{∨}(f) ≤ [�] (si − 1): (6.1)

1 i n 1 i n
_≤_ _≤_ _≤_ _≤_

###### Proof : The upper bound is obvious. For the lower bound we consider an optimal -circuit for f . The only functions computed in - {∨} {∨} circuits are Boolean sums, since constants may be eliminated. At least � si−1 gates are necessary for the computation of fi and at least sik[−][1][�]− 1 of the functions computed at these gates are Boolean sums of more than k summands. We only count these gates. By Definition 6.1 such a gate is useful for at most h outputs. Hence the lower bound follows. 2


-----

**164**

###### One might conjecture that -gates are powerless for Boolean sums. ∧ This has been disproved by Tarjan (78).

 THEOREM 6.1 : Let f ∈ M11;14 be defined by
 f1 = p ∨ y, f2 = q ∨ z, f3 = r ∨ y, f4 = s ∨ z, f5 = x1 y, f6 = x1 x2 y, f7 = x1 x2 x3 y, ∨ ∨ ∨ ∨ ∨ ∨ f8 = x1 z, f9 = x1 x2 z, f10 = x1 x2 x3 z, ∨ ∨ ∨ ∨ ∨ ∨ f11 = p ∨ u ∨ x1 ∨ x2 ∨ x3 ∨ y, f12 = q ∨ u ∨ x1 ∨ x2 ∨ x3 ∨ z, f13 = r ∨ w ∨ x1 ∨ x2 ∨ x3 ∨ y, f14 = s ∨ w ∨ x1 ∨ x2 ∨ x3 ∨ z .

<
###### Then Cm(f) ≤ 17 18 = C{∨}(f) .


###### Proof : At first we compute f1


; : : : ;
###### f10 with 10 gates. Let


:
###### g = f7 f10 = x1 x2 x3 yz (6.2) ∧ ∨ ∨ ∨

 Then

; ;
###### f11 = f1 ∨ (g ∨ u) f12 = f2 ∨ (g ∨ u) (6.3)

; :
###### f13 = f3 ∨ (g ∨ w) f14 = f4 ∨ (g ∨ w)

 One -gate and 6 -gates are sufficient for the computation of ∧ ∨

; : : : ; ; : : : ;

###### f11 f14 if f1 f10 and the variables are given. Hence Cm(f) ≤ 17 .
 Obviously C (f) 18 . For the lower bound it is sufficient to
_{∨}_ _≤_

; : : : ;

###### prove that 8 ∨-gates are necessary for the computation of f11 f14 if

; : : : ;

###### f1 f10 and the variables are given and if ∧-gates are not available.
 This proof is left as an exercise. 2

 This function is (see Exercises) a further example where

< :
###### C[∧]m[(f) + C][∨]m[(f) = 0 + 16] 17 ≤ Cm(f) (6.4)

 Now we estimate the power of -gates for Boolean sums. ∧

 THEOREM 6.2 : Let f ∈ Mn;n be an (h; k)-disjoint Boolean sum

;
###### where fi is a Boolean sum of si variables. Let h[′] = max{1 h − 1} . Then


-----

**165**


###### �� � :
 (h h[′])[−][1][ �] sik[−][1][�] − 1 ≤ Cm(f) ≤ C{∨}(f) ≤ [�] (si − 1) (6.5)

1 i n 1 i n
_≤_ _≤_ _≤_ _≤_

###### Proof : We only have to prove the lower bound. We represent g ∈ Mn as g1 g2 where g1 consists of the prime implicants of g of length 1 . ∨ All prime implicants of the outputs fi are of length 1 . By our first replacement rule (Theorem 5.1) we can replace g by g1 . If g1 is a constant or a variable we save the gate for the computation of g . If g1 is a Boolean sum of two variables we replace the gate for the computation of g by a gate for the computation of g1 . If g1 is a sum of more than two variables it might be expensive to compute g1 . For such a situation Wegener (80) introduced the assumption that some functions besides the variables are given for nothing. Here this is the class of all Boolean sums of at most k variables. The set of functions given for nothing is to be chosen carefully. If the set is too large, it may be easy to compute f . It the set is too small, we cannot apply the replacement rules in sufficiently many situations. Let C[∗]m [and C][∗]{∨} denote the complexity measures Cm and C{∨} if the Boolean sums of at most k variables are given for nothing. By the same arguments as before we prove the bounds of (6.1) also for C[∗]
_{∨}[(f) .]_

###### Let us consider an optimal monotone -circuit for f . Let a and b ∗ be the number of - and -gates resp. in this circuit. We prove that ∨ ∧ we can replace each -gate by at most h new -gates. After such a ∧ ∨ replacement we can even eliminate some other gate. At the end of this procedure we obtain a -circuit over the basis for f . Hence ∗ {∨}
 C[∗]{∨}[(f)][ ≤] [a + (h][ −] [1)b][ ≤] [h][′][(a + b) = h][′][C]m[∗] [(f)][ ≤] [h][′][ C][m][(f)][:] (6.6)

 Applying Lemma 6.1 in its generalized form, we obtain the lower bound (6.5).

 We always replace the last -gate G where g is computed and s and ∧ t are input functions. Again we represent g = g1 g2 . If the number ∨ of prime implicants of g1 is at most k we replace g by g1 which is given as input of the -circuit. In this case we are done. ∗


-----

**166**

; : : : ;

###### In the other case let w.l.o.g. f1 fl be the outputs which are
 successors of G . Since the prime implicants of g1 have length 1, and

; : : : ;

###### since no ∧-gate is a successor of G, the outputs f1 fl have the
 prime implicants of g1 in common. These are more than k variables.

;
###### l h, since f is (h k)-disjoint. We replace gate G by the constant 0 . ≤ Then fj (1 ≤ j ≤ l ) is replaced by hj . We claim that

; : : : ; :
###### fj = s ∨ hj or fj = t ∨ hj for j ∈{1 l } (6.7)

 By (6.7) we can replace G by at most l h -gates. Since G is ≤ ∨ replaced by 0 we can eliminate also the direct successors of G . If G has no direct successor, hj = 0 and we need no new gate. Altogether it is sufficient to prove (6.7).

 fj ≤ s ∨ hj and fj ≤ t ∨ hj, since fj = g ∨ hj and g = s ∧ t . If (6.7) does not hold, we can choose inputs a and b where fj(a) = fj(b) = 0 but (s ∨ hj)(a) = (t ∨ hj)(b) = 1 . Let input c be defined by ci = ai ∨ bi . (s ∨ hj)(c) = (t ∨ hj)(c) = 1, since c ≥ a and c ≥ b . Furthermore

:
###### fj(c) = (g ∨ hj)(c) = [(s ∧ t) ∨ hj](c) = 1 (6.8)

 Hence xi PI(fj) and ci = 1 for some i . By definition of c either ai = 1 ∈ or bi = 1 in contradiction to the fact that fj(a) = fj(b) = 0 . For this last argument it is essential that fj is a Boolean sum. 2

;
###### COROLLARY 6.1 : Optimal monotone circuits for (1 1)-disjoint Boolean sums consist of -gates only. ∨


;
###### The explicit construction of (h k)-disjoint Boolean sums which maximize s1 + · · · + sn is equivalent to the explicit solution of Zarankiewicz’s problem. A Boolean sum f ∈ Mn;n can be represented

; : : : ; ; : : : ;

###### by a bipartite graph G(f) on the vertices x1 xn and f1 fn . G(f)

; ;

###### contains the edge (fi xj) iff xj ∈ PI(fi) . f is (h k)-disjoint iff G(f) does
 not contain any complete bipartite graph Kh+1;k+1 . Such a Kh+1;k+1 consists of h + 1 vertices of the first and k + 1 vertices of the second

;
###### class such that all edges between these vertices exist. Let z(n j) be


-----

**167**

###### the maximal number of edges in a bipartite graph G where G does not contain any Kj;j and G consists of 2n vertices. It is known (see Bollob´as (78)) that

 1 2 �� � � � ; < : 1 n[2][−][2][=][(j+1)][�] z(n j) (j 1)[1][=][j] n[2][−][1][=][j] + [t][ −] [1] n (6.9) − ≤ −
 j! 2

 In general it is not known how to construct such graphs. Constructive solutions are only known for j = 2 (Kovari, S´os and Tur´an (54)) and j = 3 (Brown (66)).

;
###### COROLLARY 6.2 : We can define explicitly (1 1)-disjoint and

;
###### (2 2)-disjoint Boolean sums whose monotone complexity is Θ(n[3][=][2]) and Θ(n[5][=][3]) resp.

;
###### We present only the construction of the most complex (1 1)-disjoint Boolean sums. Let n = p[2] for some prime number p . The construc
Z
###### tion is based on the fact that straight lines in p intersect in at most one point (projective geometry). For later applications we present the Boolean sum or the corresponding bipartite graph by an n n-matrix ×

; ; ; <
###### M with elements in {0 1} . M(i j) = 1 iff xj ∈ PI(fi) for 0 ≤ i j n .

; ; ; < ;
###### Let i = a + bp and j = c + dp for 0 a b c d p . Then M(i j) = 1 ≤ iff c a + bd mod p . This definition is illustrated by the submatrix ≡ Mb;d of all elements with constant b and d . Then


###### q

: : : : : :
###### 0 0 0 1 0 0 0

: : : : : :
###### 0 0 0 0 1 0 0
 · · · · · · · · · · · · · · · · · · · · ·

: : : : : :
###### 0 0 0 0 0 0 1

: : : : : :
###### 1 0 0 0 0 0 0
 · · · · · · · · · · · · · · · · · · · · ·

: : : : : :
###### 0 0 1 0 0 0 0


###### 
 


###### Mb;d =


###### 
 


:
###### q b d mod p (6.10) ≡


;
###### The corresponding Boolean sums are (1 1)-disjoint. Otherwise we could find some ik = ak + bkp and jl = cl + dl p (1 ≤ k, l ≤ 2) such

; ;

###### that i1 = i2 j1 = j2 and M(ik jl ) = 1 . ̸ ̸


-----

**168**

###### By definition

 cl ≡ ak + bkdl mod p for 1 ≤ k, l ≤ 2 and (6.11)

:
###### b1(d1 − d2) ≡ c1 − c2 ≡ b2(d1 − d2) mod p (6.12)

 Since p is prime either b1 = b2 or d1 = d2 . Either both rows or both columns belong to the same submatrices. But by (6.10) these submatrices do not have two ones in the same row or in the same

;
###### column. The Boolean sums are (1 1)-disjoint and each fi is the sum of p variables. By Theorem 6.2 Cm(f) is equal to n(p − 1) = n[3][=][2] − n .

 6.7 Boolean convolution

 We repeat the definition of the Boolean convolution.


###### fk(x0


; : : : ;
###### xn 1
_−_


;
###### y0


; : : : ; :
###### yn−1) = xi yj (0 ≤ k ≤ 2n − 2) (7.1)
 [�]

i+j=k


###### By (7.1) 2 n[2] 2 n 1 gates suffice. One conjectures that this number − − of gates is also necessary in monotone circuits. Negations are powerful for the Boolean convolution. By the results of Ch. 3 we compute the Boolean convolution if we multiply the binary numbers
 x[′] = 0 [�]i<nxi 2[ki] and y[′] = 0 [�]i<nyi 2[ki]

_≤_ _≤_


###### where k = ⌈log n⌉ + 1, i.e. we separate xi and xi+1 by ⌈log n⌉ zeros. x[′]
 and y[′] are binary numbers of length Θ(n log n) and can be multiplied by the method of Sch¨onhage and Strassen with O(n log[2] n log log n) gates.

 For the monotone complexity of the Boolean convolution several lower bounds have been proved, namely lower bounds of size n log n (Pippenger and Valiant (76)), n[4][=][3] (Blum (85)), and n[3][=][2] (Weiß (83)), see also Wegener (84 b) when comparing the methods. Weiß applies the elimination method in conjunction with information flow argu

-----

**169**

###### ments. We investigate a larger class of functions since the subfunctions of the Boolean convolution are not convolution functions.

;
###### DEFINITION 7.1 : A monotone function f : X Y 0 1 is
##### ·∪ →{ }[m]
###### bilinear if each prime implicant of f consists of one x-variable and one y-variable. f is even semi-disjoint if PI(fi) ∩ PI(fj) = ̸◦ for i ̸= j and each variable is contained in at most one prime implicant of each output.

 Obviously the Boolean convolution is a semi-disjoint bilinear form.

 THEOREM 7.1 : Let f be a semi-disjoint bilinear form and let ri be the number of outputs depending essentially on xi . Then


###### Cm(f) ≥ [�] ri[1][=][2]

1 i n
_≤_ _≤_


:
###### (7.2)


###### COROLLARY 7.1 : The monotone complexity of the Boolean convo- lution is at least n[3][=][2] while its circuit complexity is O(n log[2] n log log n) .

 Proof of Theorem 7.1 : If we replace x1 by 0 we obtain a subfunction of f which is a semi-disjoint bilinear form with unchanged parameters

; : : : ;

###### r2 rn . Therefore it is sufficient to prove that we can eliminate at
 least r1[1][=][2] gates if x1 = 0 . Let s1 be the number of outputs depending essentially on x1 and consisting of only one prime implicant. If x1 = 0 we can eliminate those s1 ∧-gates where such outputs are computed. In the following we eliminate at least (r1 − s1)[1][=][2] ∨-gates, altogether at least r1[1][=][2] gates.

 We consider only outputs fk that depend essentially on x1 and have

; : : : ;

###### more than one prime implicant. Let G0 Gm be a path from x1 to
 fk . This path includes at least one ∨-gate Gl where xi yj for some i ̸= 1 and some j is an implicant of the computed function gl . Otherwise each prime implicant of gl would include either x1 or two x-variables or


-----

**170**

###### two y-variables. For x1 = 0 gl could be replaced by Theorem 5.1 by 0 and this would also hold for fk in contradiction to the assumptions.

 Let G[∗] be the set of all first ∨-gates on the paths from x1 to the considered outputs fk where some xi yj for i ̸= 1 is implicant. By our above-mentioned arguments one input of each gate in G[∗] can be replaced by 0 if x1 = 0 . Therefore all gates in G[∗] can be eliminated if x1 = 0 . The gates in G[∗] form a bottleneck. We prove that this bottleneck cannot be too tight.

; : : : ; ; : : : ;

###### Let G[∗] = {G1 Gp} . We choose i(1) i(p) ̸= 1 and

; : : : ;
###### j(1) j(p) such that xi(l ) yj(l ) I(gl ) where gl is computed at Gl . ∈ If xi(l ) = yj(l ) = 1 for 1 ≤ l ≤ p all gates in G[∗] compute the con- stant 1 . The output fk does not depend on x1 any longer. Let s be chosen such that x1 ys PI(fk) . Since variables are only replaced by ∈ ones, either fk is replaced by 1 or fk is replaced by a function fk[′] [where] ys PI(fk′) . The second possibility would imply that xi(l ) ys PI(fk) ∈ ∈ for some l . This contradicts the definition of semi-disjoint bilinear forms since i(l ) ̸= 1 . Hence fk is replaced by 1 and xi(l ) yj(m) ∈ PI(fk) for some 1 ≤ l, m ≤ p . This conclusion holds for all r1 − s1 outputs considered.

 Due to the definition of semi-disjoint bilinear forms the prime im- plicants are different for different outputs. Only p[2] different prime implicants can be constructed from the chosen p x-variables and p y-variables. Hence p[2] ≥ r1 − s1 and |G[∗]| = p ≥ (r1 − s1)[1][=][2] . 2

 6.8 Boolean matrix product

; ;
###### The Boolean (I J K)-matrix product fIJK of an I × K-matrix and a K J-matrix is defined by ×


-----

**171**


###### � : zij = xik ykj (1 ≤ i ≤ I, 1 ≤ j ≤ J) (8.1)

1 k K
_≤_ _≤_

###### THEOREM 8.1 : C[∨]m[(f][IJK][) = I J (K][ −] [1), C][∧]m[(f][IJK][) = I J K and] Cm(fIJK) = 2 I J K − I J .


###### The upper bounds follow from definition. Pratt (75 a) proved the

=
###### necessity of IJK 2 -gates, before Paterson (75) and Mehlhorn and ∧ Galil (76) proved independently the exact bounds. The proof of the lower bound for -gates can be simplified by using the methods of ∨ Weiß (83) (see 7). Before we prove Theorem 8.1 we investigate the § Boolean matrix product fn of two n × n-matrices. By Theorem 8.1 Cm(fn) = 2 n[3] − n[2] and by the results of Ch. 3 C(fn) = O(n[c]) for some

< =
###### constant c 5 2 . Since fn is defined on 2 n[2] variables and has n[2]
 outputs we should express the bounds in dependence of N = n[2] .

 COROLLARY 8.1 : The monotone complexity of the Boolean matrix product fn ∈ M2N;N is 2 N[3][=][2] − N while its circuit complexity is O(N[c])

< =
###### for some c 5 4 .

 Proof of Theorem 8.1, -gates : It is obvious that the Boolean ∨ matrix product is a semi-disjoint bilinear form. But the lower bound of Theorem 7.1 is not sharp enough for our purposes. We prove that we can always eliminate at least J ∨-gates if we replace xik (1 ≤ i ≤ I, 1 ≤ k ≤ K − 1) by 0 . There are J outputs zij (1 ≤ j ≤ J) that depend essentially on xik and have at least two prime implicants. We prove that the bottleneck G[∗] of Theorem 7.1 has at least J gates.

; : : : ;

###### Let G[∗] = {G1 Gp} be the bottleneck for xik . Then we find
 sets X[∗] and Y[∗] of p x-variables and p y-variables resp. such that the replacement of these variables by ones forces all zij (1 ≤ j ≤ J) to com- pute 1 . Hence Y[∗] contains some yk(j);j (1 ≤ j ≤ J) and |G[∗]| = p ≥ J. 2


-----

**172**

###### For the lower bound on the number of -gates we apply the second ∧ replacement rule of Theorem 5.2.

 DEFINITION 8.1 : The variables xik (1 ≤ i ≤ I) and ykj (1 ≤ j ≤ J) are called variables of type k .

 LEMMA 8.1 : Let g be computed in a monotone circuit for the Boolean matrix product. If two different variables of type k are prime implicants of g, g can be replaced by the constant 1 .

;

###### Proof : Let t1 t2 ∈ PI(g) be variables of type k . If t = 1,

;

###### t t1 t t2 ∈ PI(g). In order to apply Theorem 5.2 we only have to
 establish (5.2). Let t[∗] be a monom and zij be an output where

;

###### t[∗] t t1 t[∗] t t2 I(zij) . Hence for some k[′] and k[′′] t[∗] t t1 is a length ∈ ening of xik[′] yk[′]j and t[∗] t t2 is a lengthening of xik[′′]yk[′′]j . If already t[∗] t is a lengthening of one of these monoms, t[∗] t ∈ I(zij), and we have proved (5.2). Otherwise k[′] = k = k[′′], since t1 and t2 are variables of type k . t[∗] t t1 and t[∗] t t2 are lengthenings of xik ykj but t[∗] t is not. Since t1 = t2, t1 = xik and t2 = ykj or vice versa. To make xik ykj a ̸ part of t[∗] t t1 and t[∗] t t2, xik and ykj have to be members of t[∗] t and t[∗] t ∈ I(zij) . 2


###### Proof of Theorem 8.1, ∧-gates : We replace all xi1 (1 ≤ i ≤ I) by 1 and all y1j (1 ≤ j ≤ J) by 0 . Then the circuit computes an

; ;
###### (I J K 1)-matrix product and we can proceed by induction. It is − sufficient to prove that we can eliminate at least I J -gates by the ∧ replacement considered.

 Let Gij be the first gate where we compute a function gij such that xi1 y1j PI(gij) . By definition of zij, Gij is well defined, and because ∈ of the considerations of § 1 Gij is an ∧-gate (at ∨-gates no new prime implicant is created). Let g1 and g2 be the inputs of Gij . By definition


-----

**173**

###### of Gij and (1.5) w.l.o.g. t1 = xi1 PI(g1) and t2 = y1j PI(g2) . If ∈ ∈ xi1 = 1, g1 is replaced by 1 and Gij can be eliminated. It is sufficient

; ;
###### to prove that Gij ̸= Gi[′]j[′] if (i j) ̸= (i[′] j[′]) . Otherwise each variable

; ;

###### xi1 xi[′]1 y1j and y1j[′] of type 1 is a prime implicant of g1 or g2 . Since
 i ̸= i[′] or j ̸= j[′], either g1 or g2 has two different variables of type 1 as prime implicant. This input can be replaced by 1 (see Lemma 8.1). W.l.o.g. we assume that such replacements are done in advance. 2


###### 6.9 A generalized Boolean matrix product

 Several new methods for the proof of lower bounds on the complex- ity of monotone circuits have been developed during the investigation of the following generalized Boolean matrix product (Wegener (79 a) and (82 a)). Let Y be the Boolean matrix product of matrix X1 and the transposed of matrix X2 . yij = 1 iff the i -th row of X1 and the j -th row of X2 ˝have a common 1˝. This consideration of the Boolean matrix product can be generalized to a ˝direct˝ matrix product of m

; : : : ;

###### M × N-matrices X1 Xm . For each choice of one row of each ma trix the corresponding output computes 1 iff the chosen rows have a common 1 .

 DEFINITION 9.1 : The generalized Boolean matrix product fMN[m] [is a]

;
###### monotone function on m M N variables with M[m] outputs (m M 2). ≥ The variables form m M × N-matrices. x[i]hl [is the element of the][ i] [-th]

;
###### matrix at position (h l ) . x[i]hl [is a variable of type][ l][ .]


; : : : ;

###### For 1 ≤ h1 hm ≤ M let


: : :
###### x[m]
hml


###### yh1


;::: ;hm [=] � x[1]h1l [x]h[2]2l

1 _l_ N
_≤_ _≤_


:
###### (9.1)


: : :
###### x[m]hml [is a prime implicant of type][ l][ .]


###### (h1


; : : : ; ;
###### hm l ) = x[1]h1l


-----

**174**

###### THEOREM 9.1 : Cm(fMN[m] [)][ ≤] [N M][m][ (2 + (M][ −] [1)][−][1][)][ ≤] [3 N M][m][ .]

; : : : ; ;

###### Proof : N M[i] ∧-gates are sufficient to compute all (h1 hi l ) if all

; : : : ; ;
###### (1 hi 1 l ) are already computed. Hence the number of -gates
_−_ _∧_

###### may be estimated by


:

###### N M[i] N (M[m+1] 1)(M 1)[−][1] N M[m] (1 + (M 1)[−][1])
 ≤ − − ≤ −

 [�]

2 i m
_≤_ _≤_

###### (9.2)

 Afterwards each output can be computed with N 1 -gates. 2 − ∨

 It is possible to save a small amount of the -gates. For the simple ∧ Boolean matrix product we proved in 8 that one -gate is necessary § ∧ for each prime implicant, and that K 1 -gates are necessary for − ∨ outputs with K prime implicants. If we could generalize these ideas to fMN[m] [, we would obtain the following lower bounds: N M][m][ on the] number of -gates and (N 1) M[m] on the number of -gates. It was ∧ − ∨ proved (Wegener (79 a)) that the number of -gates can be reduced ∨ (for m constant and M large) approximately to N M[m] (m 1)[−][1] (see − Exercises). No good lower bound on the number of -gates is known. ∨

=
###### We can prove the necessity of (1 2) N M[m] -gates. At first we carry ∧ out an analysis of the structure of optimal monotone circuits for fMN[m] [.] Again we apply replacement rules.
 Notation: x[i]0l [= 1 .]


###### LEMMA 9.1 : Let g be computed in a monotone circuit for fMN[m] [. Let]

; : : : ; ; ; : : : ; ; ; : : : ; ;

###### (i1 im l ), (j1 jm l ) ∈ PI(g) for some l ∈{1 N} and ik jk ∈

; ; : : : ;
###### {0 1 M} . Let A = {k | ik = jk}, and let t be the conjunction of all x[k]
ikl [where k][ ∈] [A . Then g can be replaced by h = g][ ∨] [t .]

###### Proof : Let t1 = [�] x[k]ikl [and t][2][ =][ �] x[k]jkl [. By definition of A, t][1]

k A k A
_̸∈_ _̸∈_

###### and t2 have no common variable. According to Theorem 5.2 it is sufficient to prove (5.1) and (5.2). (5.1) is fulfilled by assumption. If


-----

**175**

###### (5.2) was not fulfilled, we would choose a monom t[∗] and an output (h1 ; : : : ; hm) = yh1 ;:::;hm [such that t][∗] [t t]1 [and t][∗] [t t]2 [are implicants of]

; : : : ; ; : : : ; ;

###### (h1 hm) but t[∗] t is not. Then t[∗] t t1 includes some (h1 hm l [′])

; : : : ; ;

###### but t[∗] t does not include (h1 hm l [′]) . Hence l = l [′] . The same

; : : : ; ;

###### holds for t[∗] t t2 . That means (h1 hm l ) is a submonom of t[∗] t t1
 and t[∗] t t2 but not of t[∗] t . The variable that is not included in t[∗] t is a common variable of t1 and t2 in contradiction to the definition of t1 and t2 . 2


###### We interpret this lemma. A monom is ˝useful˝ for some fMN[m] [if it] is a (not necessarily proper) shortening of a prime implicant of fMN[m] [.] If g includes several useful monoms of type l, we can replace g by g t where t is the common part of all useful monoms of type l, i.e. ∨ t is the monom consisting of all variables which are members of all useful monoms of type l . The replacement of g by g t should not ∨ cause any costs. Therefore we do not count -gates and assume that ∨ all monoms of less than m variables are given as inputs. The length of a useful monom is bounded by m and the common part of different useful monoms includes less than m variables.

 Circuits in this model (only -gates are counted, monoms of length ∧ less than m are given as inputs) are called -circuits, the appropriate ∗ complexity measure is C[∗]m [. A][ ∗][-circuit S for f]MN[m] [can now be trans-] formed into a ˝standard˝ ∗-circuit for fMN[m] [of the same complexity. We] manipulate the gates of S according to their natural numbering. Let g be computed at some gate. Let tl = 0, if g includes at most one useful monom of type l, and let tl be the common part of all useful monoms of type l which are prime implicants of g, otherwise. We can replace g by g ∨ t1 ∨· · · ∨ tN without any costs. We obtain a ∗-circuit S[′] for fMN[m] [. In S][′][ all inputs and outputs of][ ∧][-gates have at most one] useful monom of type l as prime implicant. This standard form of -circuits makes the following considerations much more easier. The ∗ assumption that certain functions besides the variables and constants are given as inputs has been applied for the first time in circuit theory


-----

**176**

###### to the generalized matrix product (Wegener (79 a)).

=
###### In that paper a (2 m) N M[m] lower bound has been proved using the elimination method and the pigeon hole principle. Wegener (82 a)

=
###### improved that bound and proved a (1 2) N M[m] lower bound which is only by a small constant factor smaller than the known upper bounds. More important than the new bound was the application of a new method for proving lower bounds. The method is based on the defi- nition of a suitable value function to estimate the value of each gate for the computation of the outputs.

               - =
###### THEOREM 9.2 : Cm(fMN[m] [)][ ≥] [C]m[∧] [(f]MN[m] [)][ ≥] [C]m[∗] [(f]MN[m] [)] (1 2) N M[m] if m 2 . ≥

=
###### For m = 2 or m = 3 the (2 m) N M[m]-bound is better than the bound of Theorem 9.2.

 COROLLARY 9.1 : For n 4 let m(n) = log n, M(n) = 2, ≥ ⌊ ⌋

=
###### N(n) = ⌊n (2 log n)⌋ and hn = fM(n)N(n)[m(n)] [. h][n][ is defined on at most n] variables and has at most n outputs. The monotone circuit complexity

=

###### of hn is of size n[2] log n .


###### Proof of Theorem 9.2 : We only have to prove the last inequality. Let S be an optimal ∗-circuit for fMN[m] [. We assume that S is in stan-] dard form, i.e. the inputs and outputs of -gates have at most one ∧ prime implicant which is a useful monom of type l . We try to esti- mate the value of each -gate G for the computation of each prime ∧

; : : : ; ;

###### implicant (h1 hm l ) . A function vG : PI(fMN[m] [)][ →] [[0][;][ 1] is called]
 value function if


###### v(G) := �

1≤h1 ; :::; hm≤M


###### � vG(h1

1 _l_ N
_≤_ _≤_


; : : : ;
###### hm


; :
###### l ) 1 (9.3) ≤


###### At each gate we can distribute at most the value 1 among the prime implicants. This ensures that for an optimal -circuit S ∗


-----

**177**


###### � v(S) := v(G) ≤ C[∧]m[(S) = C][∗]m[(f]MN[m] [)] (9.4)

G -gate in S
_∧_

###### is a lower bound on C[∗]m[(f]MN[m] [) . Finally we prove the necessity of giving]

= ; : : : ; ;
###### value 1 2 to each prime implicant, i.e. we prove for all (h1 hm l )
 that


; �
###### l ) := vG(h1

G -gate in S
_∧_


; : : : ;
###### hm


; - = :
###### l ) 1 2 (9.5)


###### v(h1


; : : : ;
###### hm


###### Combining (9.3) – (9.5) we have proved that


###### C[∗]m[(f]MN[m] [)][ ≥] �

1≤h1 ; :::; hm≤M

   - = :
###### (1 2) N M[m]


###### � v(h1

1 _l_ N
_≤_ _≤_


; : : : ;
###### hm


;
###### l ) (9.6)


###### At first we define a value function. Then we discuss why we think that such a value function works. Let G be an -gate in an optimal ∧ ∗-circuit for fMN[m] [. Let g][′][ and g][′′][ be the inputs of G and g = res][G][ . We]

; : : : ; ; : : : ;

###### define vG as the sum of vG[′] [and v]G[′′] [. Let i][1] iq[′] ∈{1 N} be the
 types such that some tj PI(fMN[m] [) of type i][j][ is prime implicant of g] ∈ but not of g[′] . Then

 vG[′] [(t][j][) = 1][=][(2q][′][)] for 1 ≤ j ≤ q[′] and (9.7)

 vG[′] [(t) = 0] for all other t ∈ PI(fMN[m] [) .]

 Obviously


###### v[′](G) := �

1≤h1 ; :::; hm≤M


###### � vG[′] [(h][1]

1 _l_ N
_≤_ _≤_


; : : : ;
###### hm


; = :
###### l ) 1 2 (9.8) ≤


###### vG[′′] [is defined in the same way but with respect to g][′′][ instead of g][′][ .] Then (9.3) is fulfilled. It remains to prove (9.5).

 We discuss some arguments what makes the value function v a good choice. v is relatively simple, the image of vG has at most 4 elements. vG(t) is equal to


-----

**178**

###### 1 –
 2q[′][ + 1]2q[′′][ if t][ ∈] [PI(g), t][ ̸∈] [PI(g][′][)][ ∪] [PI(g][′′][), these prime implicants]
 are created at G,


###### 1 –
 2q[′][ if t][ ∈] [PI(g)][ ∩] [PI(g][′′][), t][ ̸∈] [PI(g][′][),]
 1 –
 2q[′′][ if t][ ∈] [PI(g)][ ∩] [PI(g][′][), t][ ̸∈] [PI(g][′′][), these prime implicants are]
 preserved at G,


###### – 0 if t PI(g) or t PI(g) PI(g[′]) PI(g[′′]) . ̸∈ ∈ ∩ ∩

 The prime implicants created at G get the highest score at G . This is in accordance with our intuition. This score is quite small if q[′] and q[′′] are quite large. What reasons are there for hoping that each of

               - =
###### these prime implicants t scores enough, i.e. v(t) 1 2? If q[′] and q[′′] are both large, then g has many prime implicants with variables of different types. These ˝dirty˝ monoms cannot be lengthened to prime implicants of fMN[m] [. The only possibility to eliminate these dirty] monoms is that t scores sufficiently often.

; : : : ; ;

###### Proof of (9.5) : We consider the prime implicant t = (h1 hm l )
 and the corresponding output yt := yh1 ;:::;hm [. Let S be an optimal]
 ∗-circuit for fMN[m] [in standard form, and let S(t) be the subcircuit con-] sisting of the following inputs and gates. A gate G of S belongs to S(t) if some path in S leads from G to the output yt and if t is a prime implicant of all functions computed on this path (including G). Furthermore the inputs of the gates we just discussed belong to S(t) . S(t) is a connected subcircuit with output yt . For each input g of S(t), t PI(g), but t is a prime implicant of all functions computed ̸∈ within the circuit.

 If both direct predecessors of some gate G are inputs of S(t), G is an ∧-gate. Otherwise t ̸∈ PI(resG) . If an input of S(t) has an ∧-gate as direct successor, some proper shortening of t is a prime implicant of that input.


-----

**179**

; : : : ;

###### Let s1 sD be the inputs of S(t) leading directly into an ∧-gate.
 Let G(i) be an ∧-gate with input si and let vG(i)[∗] [= v]G(i)[′] [if s][i][ is the first]

                  ###### input of G(i) and v[∗] 0 .
G(i) [= v]G(i)[′′] [otherwise. In either case v]G(i)[∗] [(t)]
###### Instead of (9.5) we prove the stronger result


###### b1 + · · · + bD


- =
###### 1 2 (9.9)


###### for bi = vG(i)[∗] [(t) . W.l.o.g. b][1][ ≥· · · ≥] [b][D][ . We choose some w][i][ ∈] [PI(s][i][)] such that some proper lengthening wi[∗] [of w][i][ is prime implicant of]

     ###### resG(i), vG(i)[∗] [(w]i[∗][)] 0, and the type of wi[∗] [differs from the types of]

; : : : ;

###### w1[∗] wi[∗]−1 [.] We can always choose w1[∗] [= t .] If the choice of wi
 according to our rules is impossible, v[∗]
G(i) [is positive for at most i][ −] [1]
###### prime implicants. Hence bi ≥ (2(i − 1))[−][1] and, since b1 ≥· · · ≥ bD,


###### b1 + · · · + bD ≥ i bi


- = :
###### 1 2 (9.10)


; : : : ;

###### In the following we assume that w1 wD are chosen according to
 our rules. By construction wi ∈ PI(si) and


: : :
###### sD


###### w1


: : :
###### wD ≤ s1


:
###### (9.11)


###### We claim that


###### s1


: : :
###### sD ≤ yt


:
###### (9.12)


###### Let a be an input where si(a) = 1 for 1 ≤ i ≤ D . S(t) is a circuit where all inputs leading into -gates are equal to 1 . Furthermore no ∧ -gate of S(t) has two inputs of S(t) as direct predecessors. Now it is ∨ easy to prove by induction that for input a all gates of S(t) compute 1, in particular yt(a) = 1 . Because of (9.11) and (9.12)


###### w1


: : : :
###### wD ≤ yt (9.13)


: : :

###### We consider that input a where all variables of w1 wD are set to 1
 and all other variables are set to 0 . By (9.13) yt(a) = 1 . All variables

; : : : ;

###### of wi are of type li and l1 lD are different. Since wi is a proper


-----

**180**

         ###### shortening of wi[∗] [and v]G(i)[∗] [(w]i[∗][)] 0, wi includes at most m−1 variables. Hence a is an input where for each type at most m 1 variables are − set to 1 . By definition of fMN[m] [y][t][(a) = 0 . Because of this contradiction]

; : : : ;

###### it is impossible to choose w1 wD according to our rules. 2

 6.10 Razborov’s method

 In 3 – 9 we heard about several methods for the proof of lower § § bounds on the monotone complexity of Boolean functions. For func- tions with one output we proved only linear bounds, and for functions with n outputs the largest bound is of size Θ(n[2] log[−][1] n) (see 9). § Razborov (85 a) and (85 b) developed a method for the proof of expo- nential lower bounds. The method itself can be described in a rather simple way (like the elimination method or the method of value func- tions). The ingenious part is the successful application to important functions.

; ;

###### In monotone circuits we work in the lattice (Mn ∧ ∨) . Instead
 of f ∈ Mn we consider now f[−][1](1) . Let M[∗]n [be the set of all f][−][1][(1)] where f ∈ Mn, i.e. the set of all up-sets. Then we work in the lat
; ;

###### tice (M[∗]n ∩ ∪) . Razborov investigates computations in sublattices
 of M[∗] = M[∗]n [. We state formally the concepts before we discuss the] method.


; ;
###### DEFINITION 10.1 : (L ) is called a legitimate lattice if the ⊓ ⊔ following conditions are fulfilled.

: : : ; ; ;
###### i) L ⊆ M[∗], x[−]1 [1][(1)][;] x[−]n [1][(1)][;][ ̸][◦] {0 1}[n] ∈ L .

;
###### ii) For M N L the meet (the lattice theoretic intersection) M N ∈ ⊓ ∈ L is well defined and M N M N . ⊓ ⊆ ∩

;
###### iii) For M N L the join (the lattice theoretic union) M N L is ∈ ⊔ ∈ well defined and M N M N . ⊔ ⊇ ∪


-----

**181**

###### The deviation of the operations and from and is measured ⊓ ⊔ ∩ ∪

; ;
###### by δ (M N) = (M N) (M N) and δ (M N) = (M N) (M N) .
_⊓_ _∩_ _−_ _⊓_ _⊔_ _⊔_ _−_ _∪_

###### DEFINITION 10.2 : The complexity of f ∈ Mn (or f[−][1](1) ∈ M[∗]) with respect to a legitimate lattice L is defined by


;
###### Nt ∈ L : (10.1)


;
###### CL(f) = min{t | ∃ M M1


;
###### N1


; : : : ;
###### Mt


###### M f[−][1](1) δ (Mi ⊆ ∪ [�] ⊔

1 i t
_≤_ _≤_

###### f[−][1](1) M δ (Mi ⊆ ∪ [�] ⊓

1 i t
_≤_ _≤_


;
###### Ni) and

; :
###### Ni)}


###### THEOREM 10.1 : CL(f) is a lower bound on Cm(f) for f ∈ Mn and each legitimate lattice L .

 Proof : Let S be an optimal monotone circuit for f . Let fi and gi (1 ≤ i ≤ t = Cm(f)) be the inputs of the i -th gate of S . S[∗] results from S by the replacements xi → x[−]i [1][(1), 0][ ↛][◦] [, 1][ →{][0][;][ 1][}][n][,][ ∧→⊓] [,] ∨→⊔ . S[∗] is a computation in L . Let Mi and Ni be the inputs of the i -th gate of S[∗], and let M be the output of S[∗] . We prove by induction on t that these sets fulfil the conditions described in (10.1). The basis of the induction (t = 0) is obvious. For the induction step we distinguish whether the t-th gate is an -gate ((10.2) and (10.3)) or ∨ an -gate ((10.4) and (10.5)). By definition and induction hypothesis ∧


;

###### M = Mt ⊔ Nt = Mt ∪ Nt ∪ δ⊔(Mt Nt) (10.2)


;

###### ⊆ ft[−][1][(1)][ ∪] [g]t[−][1][(1)][ ∪] [�] δ⊔(Mi Ni) = f[−][1](1) ∪ [�] δ⊔(Mi

1 i t 1 i t
_≤_ _≤_ _≤_ _≤_


; ;
###### Ni)


-----

**182**


###### � f[−][1](1) = ft[−][1][(1)][ ∪] [g]t[−][1][(1)][ ⊆] [M][t][ ∪] [N][t][ ∪] δ⊓(Mi

1 i t 1
_≤_ _≤_ _−_


;
###### Ni) (10.3)


###### Mt Nt δ (Mi ⊆ ⊔ ∪ [�] ⊓

1 i t
_≤_ _≤_


; ; ;
###### Ni) M δ (Mi Ni) ⊆ ∪ [�] ⊓

1 i t
_≤_ _≤_


###### M = Mt ⊓ Nt (10.4)


###### � ⊆ Mt ∩ Nt ⊆ (ft[−][1][(1)][ ∩] [g]t[−][1][(1))][ ∪] δ⊔(Mi

1 i t 1
_≤_ _≤_ _−_


;
###### Ni)


###### f[−][1](1) δ (Mi ⊆ ∪ [�] ⊔

1 i t
_≤_ _≤_


;
###### Ni) and


###### f[−][1](1) = ft[−][1][(1)][ ∩] [g]t[−][1][(1)][ ⊆] [(M][t][ ∩] [N][t][)][ ∪] � δ⊓(Mi ; Ni) (10.5)

1 i t 1
_≤_ _≤_ _−_


###### = Mt Nt δ (Mi ⊓ ∪ [�] ⊓

1 i t
_≤_ _≤_


; ; :
###### Ni) = M δ (Mi Ni) ∪ [�] ⊓

1 i t
_≤_ _≤_


###### 2

 A more careful analysis of (10.3) and (10.4) shows that we even proved


###### � M f[−][1](1) δ (Mi ⊆ ∪ ⊔

i _i-th gate is an_ -gate
_|_ _∧_

###### f[−][1](1) M � δ (Mi ⊆ ∪ ⊓

i _i-th gate is an_ -gate
_|_ _∨_


;
###### Ni) and (10.6)

; :
###### Ni) (10.7)


###### We try to better understand computations in L . Exactly the func- tions f where f[−][1](1) ∈ L have CL-complexity 0 . Again we have to choose an appropriate class of functions which are given as inputs. If f[−][1](1) L, then f[−][1](1) cannot be computed in an L-circuit. (10.1) ̸∈ describes sufficiently good approximations M of f[−][1](1) . We do not demand that the approximating sets M, Mi and Ni can be computed in an L-circuit of size t .

 How should we choose a lattice L where it can be proved that CL(f) is large ? If L is too ˝dense˝, we can choose M in such a way that f[−][1](1) M and M f[−][1](1) are small sets. Then these sets can be − −


-----

**183**

###### covered with a small number of δ-sets. If L is too ˝coarse-grained˝, i.e. has only few elements, δ-sets are large and again f[−][1](1) M and − M f[−][1](1) can be covered by a small number of δ-sets. In the extreme − case L consists only of x[−]i [1][(1) for 1][ ≤] [i][ ≤] [n,][ ̸][◦] [and][ {][0][;][ 1][}][n][ and]

; ;
###### M[′] ⊓ N[′] = ̸◦ and M[′] ⊔ N[′] = {0 1}[n] for M[′] N[′] ∈ L . Then CL(f) ≤ 1,

;
###### since we can choose M = {0 1}[n] and M1 = N1 = ̸◦ .
 The lattice we choose should depend on the function f whose mono- tone complexity we like to estimate. L should not contain a good ap- proximation of f and δ-sets should be small. Razborov used lattices where δ -sets include only a small number of minimal elements of
_⊓_
###### f[−][1](1) (prime implicants) and δ -sets include only a small number of
_⊔_
###### maximal elements of f[−][1](1) (prime clauses). Furthermore L includes only sets M where f[−][1](1) M or M f[−][1](1) is large. In particular, we − − prove a lower bound min on the minimal number of prime implicants and prime clauses in (f[−][1](1) M) (M f[−][1](1)) for M L . Then we − ∪ − ∈ prove an upper bound max on the number of prime implicants in δ _⊓_

=
###### sets and of prime clauses in δ -sets. Then CL(f) min max. By max
_⊔_ _≥_
###### we estimate the maximal value of one computation step with respect to L . The value necessary for the computation of f in an L-circuit is at least min . Hence Razborov generalized the concepts that certain functions besides the variables and constants are given as inputs and that one should try to estimate the value of computation steps. His estimations are much more rough than those in 9. This might be § the key to the success of Razborov’s method.

 These general considerations are useful for understanding Razborov’s method. Nevertheless it is difficult to choose a good lat- tice. So far, only one type of lattice has been applied successfully. Razborov proved n[Ω(log n)]-bounds. Alon and Boppana (85) improved these bounds to exponential bounds by a better analysis of Razborov’s lattice.


-----

**184**

###### 6.11 An exponential lower bound for clique functions

 DEFINITION 11.1 : The clique function cl n;m MN where N = �n2� ∈
 is defined on the variables xi;j (1 ≤ i < j ≤ n). cl n;m(x) = 1 iff G(x) = (V = {1; : : : ; n}; E(x) = {(i; j) | xi;j = 1}) includes an m- clique, i.e. m vertices which are all directly connected by an edge.

=
###### The clique function is NP-complete if m = n 2 . Hence we suppose that circuits for cl n;n=2 cannot have polynomial size. For monotone circuits we can prove an exponential lower bound. At first we define a

; ;
###### legitimate lattice L = L(n r l ) where the parameters l 2 and r 2 ≥ ≥ are fixed later.


; ; : : : ;
###### DEFINITION 11.2 : Let W W1 Wr be (not necessarily differ ent) sets and A a class of sets.

; : : : ; ; : : : ;

###### i) W1 Wr imply W (W1 Wr ⊢ W) if |W| ≤ l, |Wi| ≤ l for
 1 ≤ i ≤ r and Wi ∩ Wj ⊆ W for all i ̸= j .

; : : : ; ; : : : ;

###### ii) A implies W (A ⊢ W) if W1 Wr ⊢ W for some W1 Wr ∈
 A .

 iii) A is closed if (A W) implies (W A) . ⊢ ∈
 iv) A[∗] is the intersection of all closed B A . ⊇

 LEMMA 11.1 : i) A[∗] is closed.

 ii) A A[∗] . ⊆
 iii) (A[∗])[∗] = A[∗] .

 iv) A B A[∗] B[∗] . ⊆ ⇒ ⊆

 Proof : ii) and iv) follow by definition, and iii) follows from i). For the proof of i) we assume that A[∗] W . If B is closed and B A, by ⊢ ⊇ definition B A[∗] and hence B W . Since B is closed, W B for all ⊇ ⊢ ∈ closed B A . This implies W A[∗], and A[∗] is closed. 2 ⊇ ∈


-----

**185**

; : : : ;
###### DEFINITION 11.3 : Let V = 1 n and V(l ) = W V { } { ⊆ | W l . For A V(l ) let A be the set of graphs on V containing | | ≤ } ⊆ ⌈ ⌉

; ;
###### a clique on some W A . (L ) is defined by ∈ ⊓ ⊔

; ; ;
###### L = L(n r l ) = A A V(l ) is closed (11.1) {⌈ ⌉| ⊆ } ∪{̸◦}

 A B = A B and (11.2) ⌈ ⌉⊓⌈ ⌉ ⌈ ∩ ⌉

:
###### A B = (A B)[∗] (11.3) ⌈ ⌉⊔⌈ ⌉ ⌈ ∪ ⌉

; ;
###### LEMMA 11.2 : (L ) is a legitimate lattice. ⊓ ⊔

 Proof : The properties we have to establish are described in Defini- tion 10.1.
 i) L ⊆ M[∗]N [, since we identify graphs and vectors in][ {][0][;][ 1][}][N][ (see]

;
###### Def. 11.1). L by definition. V(l ) = 0 1 L, since V(l ) ̸◦ ∈ ⌈ ⌉ { }[N] ∈ is closed. Let Fij be the class of all W ∈ V(l ) including i and j . Fij is closed. Hence ⌈Fij⌉ = x[−]ij [1][(1)][ ∈] [L .]

;
###### ii) Let A B V(l ) be closed. Similar to the proof of Lemma 11.1 ⊆ it follows that A B V(l ) is closed. Hence A B L . If ∩ ⊆ ⌈ ∩ ⌉∈ G A B = A B, G contains a clique on some W A B . ∈⌈ ⌉⊓⌈ ⌉ ⌈ ∩ ⌉ ∈ ∩ Hence G A B . ∈⌈ ⌉⊓⌈ ⌉
 iii) By Lemma 11.1 (A B)[∗] V(l) is closed and (A B)[∗] L . If ∪ ⊆ ⌈ ∪ ⌉∈ G A B, G contains a clique on some W A B (A B)[∗] . ∈⌈ ⌉⊔⌈ ⌉ ∈ ∪ ⊆ ∪ Hence G A B . ∈⌈ ⌉⊔⌈ ⌉
 2

 Before we estimate the L-complexity of clique functions, we inves- tigate the structure of closed systems A . If B A, also all B[′] B ∈ ⊇

; : : : ;
###### where B[′] l are elements of A . Obviously B B B[′] . This ob- | | ≤ ⊢ servation allows us to describe closed systems by their minimal sets, namely sets B A where no proper subset of B is included in A . A ∈ consists of its minimal sets, and all sets of at most l elements includ- ing a minimal set. Later we shall establish relations between prime


-----

**186**

###### implicants in δ-sets and minimal sets in closed systems. Therefore it is important to prove that closed systems have not too many minimal sets.

 LEMMA 11.3 : In each closed system A the number of minimal sets with at most k elements is bounded by (r 1)[k] . −

 Proof : A system F of sets of at most k elements has the property

; ; ; : : : ;
###### P(r k) if there are no sets W W1 Wr F and U ⫋ W such that
 ∈ Wi ∩ Wj ⊆ U for all i ̸= j . The system of all minimal sets of A with at

;
###### most k elements has property P(r k) . Otherwise, by definition of the notion closed, U would be a set in A and W would not be minimal. We

;
###### prove by induction on r that systems F with property P(r k) contain at most (r 1)[k] sets. −
 If F would contain different sets W1 and W2 for r = 2, we could choose U = W1 W2 . Since W1 and W2 are both minimal sets, U is ∩ a proper subset of W1 and W2 and for W = W1 we have proved that

;
###### F does not fulfil property P(2 k) .

;
###### For the induction step let F be a system with property P(r k) . We fix D F . For C D let ∈ ⊆

; :
###### FC = {W − C | W ∈ F W ∩ D = C} (11.4)

;
###### FC has property P(r − 1 k −|C|) . Otherwise we choose

; ; : : : ;

###### W[′] W1[′] Wr[′] 1 i j

_−_ _[∈]_ [F][C][, U][′][ ⫋] [W][′][ such that W][′] _[∩]_ [W][′] _[⊆]_ [U][′][ for i][ ̸][= j .]
###### Let W = W[′] ∪ C ∈ F, U = U[′] ∪ C ⫋ W, Wi = Wi[′] [∪] [C][ ∈] [F for] 1 ≤ i ≤ r − 1 and Wr = D ∈ F . Since C ⊆ D, Wi ∩ Wj ⊆ U for i ̸= j

;
###### in contradiction to the assumption that F has property P(r k) . By induction hypothesis |FC| ≤ (r − 2)[k][−|][C][|] . Since D is fixed, the condi- tion W D = C is fulfilled for only one set C . If W D = C = W[′] D ∩ ∩ ∩ but W = W[′], also W C = W[′] C . Finally we make use of the fact ̸ − ̸ − that D k, since D F . | | ≤ ∈


-----

**187**

D

###### � � �| |� |F| = |FC| ≤ i (r − 2)[k][−][i] (11.5)

C⊆D 0≤i≤|D|

###### � �k� :
 (r 2)[k][−][i] = (r 1)[k]
 ≤ i − −

0 i k
_≤_ _≤_

###### 2

 We provide some auxiliary means for the estimation of the size of δ -sets. These sets can be described as C[∗] C for some appropriate
_⊔_ _⌈_ _⌉−⌈_ _⌉_
###### system C . How can C[∗] be constructed out of C ? Let C[′] = W C C W . By definition C[∗] = C iff C[′] = . { ̸∈ | ⊢ } ̸◦ If C[′] = we improve C by choosing some minimal set W C[′] and ̸ ̸◦ ∈ adding W and all sets W[′] W where W[′] l to C . We obtain a ⊇ | | ≤ system B where C ⫋ B C[∗] and B[∗] = C[∗] . We continue with B in ⊆ the same way. The number of such improvement steps is bounded by V(l ) n[l], since the improving set W V(l ) . This upper bound | | ≤ ∈ may be improved to l ! (r+1)[l] but this is not essential for our purposes.
 (m − 1)-partite graphs correspond to inputs in cl [−]n;[1]m[(0) . Such a]

; : : : ;
###### graph G can be described by a coloring h : V 1 m 1 of →{ − } the vertices. The vertices i and j are connected by an edge in G(h) iff h(i) = h(j) . Later we have difficulties to choose the right (m 1)- ̸ − partite graph. Therefore we investigate randomly chosen (m 1)- − partite graphs or random colorings of graphs. For a coloring h the graph G(h) contains a clique on the vertex set W V iff the vertices ⊆ of W have different colors, i.e. W is colored. The uniform distribution on all g[n] colorings of V with g colors yields a random coloring of V .


; ; : : : ;
###### LEMMA 11.4 : Let g ≥ l, A ⊆ V(l ), W W1 Wr ∈ A,

; : : : ;

###### W1 Wr ⊢ W . Let E (or Ei) be the event that W (or Wi) is
 colored. Let C Ei be the complementary event of Ei . Then


###### � Pr(E ∩ C E1 ∩· · · ∩ C Er) ≤ 1 − [g(g][ −] [1)][ · · ·][ (g][ −] [l][ + 1)]
 g[l]


###### �r (11.6)


; : : : ;

###### Proof : Since Wi∩Wj ⊆ W, the events C E1 C Er are independent
 if W is colored, i.e. if E happens. This follows since the sets Wi − W


-----

**188**

###### are disjoint. Hence

 Pr(E ∩ C E1 ∩· · · ∩ C Er) ≤ Pr(C E1 ∩· · · ∩ C Er | E) (11.7)

:

###### = [�] Pr(C Ei | E) = [�] (1 − Pr(Ei | E))

1 i r 1 i r
_≤_ _≤_ _≤_ _≤_


###### By (11.7) it suffices to prove that Pr(Ei | E) is at least

: : : =
###### g · · (g − l + 1) g[l]. Let p(i) = |Wi ∩ W| and q(i) = |Wi − W| . Then p(i) + q(i) = |Wi| ≤ l . The event E implies for the set Wi that Wi ∩ W is colored with p(i) different colors. The probability that then the q(i) elements of W − Wi get other and different colors is


: : :

###### g j (g l + 1) − · −
 = [g][ ·] g g[l]


:
###### (11.8)

 2


###### �

0 j<q(i)
_≤_


###### g p(i) j − − �
 ≥ g 0 j<l

_≤_


###### LEMMA 11.5 : Let C V(l ), g l and h be a random coloring ⊆ ≥ of V . Then


:
###### (11.9)


###### � : : : (g l + 1) · − Pr(G(h) C[∗] C ) n[l] 1 ∈⌈ ⌉−⌈ ⌉ ≤ − [g][ ·]
 g[l]


###### �r


###### Proof : We already described a construction of C[∗] out of C in at most

; ; : : : ;
###### n[l] steps. Let C0 = C C1 Cp = C[∗] be the steps of this construction
 (0 p n[l] ). It is sufficient to prove that ≤ ≤


:
###### (11.10)


###### � : : : (g l + 1) · − Pr(G(h) Ci Ci 1 ) 1 ∈⌈ ⌉−⌈ − ⌉ ≤ − [g][ ·]
 g[l]


###### �r


###### Let Wi be the chosen set for the construction of Ci out of Ci−1 . G(h) contains a clique on D iff D is colored. G(h) is not in Ci 1 iff all sets ⌈ − ⌉ in Ci−1 are not colored. G(h) is in ⌈Ci⌉ iff some set in Ci is colored. By construction Wi has to be colored. Furthermore by construction

; : : : ;

###### Ci−1 ⊢ Wi, i.e. B1 Br ⊢ Wi for sets Bj ∈ Ci−1 . Altogether the

; : : : ;

###### event G(h) ∈⌈Ci⌉−⌈Ci−1⌉ implies that B1 Br are not colored
 but Wi is colored. The probability of this event has been estimated in Lemma 11.4.


-----

**189**

###### Lemma 11.5 is a useful bound for the probability that a random (m 1)-partite graph is in some δ -set. Now we are prepared to prove − ⊔ the lower bound.

= = �
###### THEOREM 11.1 : Let 4 m (1 4)(n logn)[2][=][3], l = m[1][=][2][�] and ≤ ≤ � � r = 4 m[1][=][2] log n . Then

 Cm(cl n;m) ≥ CL(n;r;l )(cl n;m) (11.11)


###### � n
 4m[3][=][2] log n


(l +1)=2
###### �⌈ ⌉ ≥ [1]
 8


###### �(m1[=]2+1)=2


###### ≥ [1]
 8


###### � n
 m(r 1) −


:


###### � = = In particular for m = (1 4)(n logn)[2][=][3][�]

 Cm(cl n;m) = exp(Ω((n= log n)[1][=][3])): (11.12)

 Proof : The first inequality of (11.11) follows from Theorem 10.1. The last inequalities of (11.11) and (11.12) follow from easy calculations. The lower bound on CL(cl n;m) is still to be proved.
 Let t = CL(cl n;m) and let M; M1 ; N1 ; : : : ; Mt ; Nt be sets fulfilling
 the conditions of (10.1), the definition of CL . By definition we can

; ; ; : : : ; ;
###### choose closed systems A A1 B1 At Bt in V(l ) where M = ⌈A⌉,
 Mi = ⌈Ai⌉ and Ni = ⌈Bi⌉ .

 Case 1 : M is not the set of all graphs.


###### � n � We consider those graphs which contain exactly the edges of
m
###### an m-clique, i.e. the graphs corresponding to prime implicants. Each

;

###### of these graphs is by (10.1) contained in M or some δ (Mi Ni) . We
_⊓_

###### prove that M can include at most half of these graphs, and that each
= �
###### δ -set can include at most 4 (m(r 1) n)[⌈][(][l] [+1)][=][2][⌉][�] [n] of these graphs.
_⊓_ _−_ m
###### In order to cover all m-cliques, it is necessary that


###### � n � � n �
 ≥
 m m


###### �m(r 1) − 4
 n


(l +1)=2
###### �⌈ ⌉ � n �
 t + [1]
 m 2


:
###### (11.13)


###### (11.13) implies (11.11).


-----

**190**

###### At first we estimate the quantity of m-cliques that can be included in M . Each set W A has at least two elements, since each graph ∈ contains each clique on one vertex and M is not the set of all graphs. Let B be a set of m elements where the clique on B belongs to M . Then we find some minimal set D A where D B . By Lemma 11.3 ∈ ⊆ A has at most (r 1)[k] minimal sets D with k elements. D can be −
n k
###### � − � responsible only for m-cliques, because this is the number of mm k
_−_
###### element sets B D . Hence the number of m-cliques in M is bounded ⊇ by
 � n k �
 � − :
 (r 1)[k] (11.14) − m k
2 k _l_ _−_
_≤_ _≤_

n n k
###### � �=� − � = = By elementary calculations (n m)[k] and m(r 1) n
m m−k _≥_ _−_ _≤_

=
###### 1 2 . Hence


###### � n k � � n �
 � − � =
 (r 1)[k] (r 1)[k] (m n)[k] (11.15) − ≤ − m k m
2 k _l_ _−_ 2 k _l_
_≤_ _≤_ _≤_ _≤_


###### � n �� = = � n �
 (1 2)[k] (1 2)
 ≤ ≤ m m

2 k _l_
_≤_ _≤_


:


###### By similar methods we investigate δ (Mi
_⊓_


;
###### Ni) . By definition


###### δ (Mi
_⊓_


;
###### Ni) = (Mi ∩ Ni) − (Mi ⊓ Ni) (11.16)

:
###### = ⌈Ai⌉∩⌈Bi⌉−⌈Ai ∩ Bi⌉


;

###### If the m-clique on Z belongs to δ (Mi Ni) we can find some minimal
_⊓_

###### set U ⊆ Z in Ai and some minimal set W ⊆ Z in Bi, but no subset of Z belongs to Ai ∩ Bi . Since Ai and Bi are closed, U ∪ W ⊆ Z will be

            ###### in Ai ∩ Bi if |U ∪ W| ≤ l . Hence |U ∪ W| l, and one of the sets U or

=
###### W includes at least (l + 1) 2 elements. If the m-clique on Z belongs ⌈ ⌉

; =

###### to δ⊓(Mi Ni), a minimal set of Ai or of Bi with at least ⌈(l + 1) 2⌉
 elements is included in Z . In the same way as before we can estimate

;

###### the number of m-cliques in δ (Mi Ni) by
_⊓_


-----

**191**


###### � n k � � n ��m(r 1)
 � − −
 2(r 1)[k] 2 − ≤ m k m n
(l +1)=2 k _l_ _−_
_⌈_ _⌉≤_ _≤_

###### � n ��m(r 1)
 −
 = 4 m n


(l +1)=2
###### �⌈ ⌉ �


###### �1


###### �i


0 i<
_≤_ _∞_


###### 2


###### (11.17)


(l +1)=2
###### �⌈ ⌉


:


###### Case 2 : M is the set of all graphs.

 We consider the class of complete (m 1)-partite graphs, this class − includes only graphs in cl [−]n;[1]m[(0). By (10.1) each of these graphs is]

;

###### contained in some δ⊔(Mi Ni) . For Ci = Ai ∪ Bi


###### δ (Mi
_⊔_


;
###### Ni) = (Mi ⊔ Ni) − (Mi ∪ Ni) (11.18)

:
###### = ⌈(Ai ∪ Bi)[∗]⌉−⌈Ai ∪ Bi⌉ = ⌈C[∗]i [⌉−⌈][C][i][⌉]


###### Let h be a random (m 1)-coloring of V, then G(h) is a complete − (m 1)-partite graph. By Lemma 11.5, the definitions of l and r and − an elementary calculation

 � � Pr G(h) ∈⌈C[∗]i [⌉−⌈][C][i][⌉] (11.19)

=
###### n[l][ �]1 (m 1) (m l ) (m 1)[l] [�][r] ≤ − − · · · − −

_√_ _√_
m 2 m m
_−_ _−√_
###### n n = n and ≤


###### � � Pr ∃ 1 ≤ i ≤ t : G(h) ∈⌈C[∗]i [⌉−⌈][C][i][⌉] ≤ t n[−√][m]


:
###### (11.20)


###### Since all complete (m 1)-partite graphs are in the union of all δ -sets, − ⊔
_√_
###### the left-hand probability of (11.20) is equal to 1 . Hence t n m . The ≥ claim follows since for m 4 ≥


:
###### (11.21)

 2


(l +1)=2
###### �⌈ ⌉


_√m_ 1
###### n ≥
 8


###### � n
 m(r 1) −


-----

**192**

###### 6.12 Other applications of Razborov’s method

 By similar methods Alon and Boppana (85) proved also the follow- ing bounds.

 DEFINITION 12.1 : cl n;p;q is the class of all monotone functions �n� f ∈ MN (where N = 2 ) such that f(x) = 0 if G(x) (see Def. 11.1) contains no p-clique and f(x) = 1 if G(x) contains a q-clique.

 THEOREM 12.1 : Let f ∈ cl n;p;q, 4 ≤ p ≤ q and p[∗]q ≤ n=(8 logn) for p[∗] = p[1][=][2] . Then


###### �(p∗+1)=2 ≥ [1]
 8 [2][(p][∗][+1)][=][2]


###### Cm(f) ≥ [1]
 8


###### � n
 4p[∗]q log n


:
###### (12.1)


###### � � � = � In particular, for p = log[4] n and q = n (8 log[3] n)


###### Cm(f) = n[Ω(log n)]


:
###### (12.2)


###### Hence it is even difficult to approximate clique functions.


###### THEOREM 12.2 : Cm(cl n;m) = Ω(n[m]


=
###### log[m] n) for constant m .


=

###### Theorem 12.2 improves an Ω(n[m] log[2m] n)-bound of Razborov.
 This bound is not far away from the obvious O(n[m])-upper bound. We show that negations are powerful for the computation of clique functions.

 THEOREM 12.3 : Let BMn be the Boolean matrix product of n × n- � n � matrices. For constant m and t = m=3
_⌈_ _⌉_

###### C(cl n;m) = O(C(BMt)) = o(n[(5][=][2)][⌈][m][=][3][⌉]): (12.3)


-----

**193**

###### Proof : The second equality holds, since t ≤ n[⌈][m][=][3][⌉] and C(BMt) = o(t[5][=][2]) (Coppersmith and Winograd (82), see Ch. 3, 6). For the first § assertion we assume that 6 is a divisor of m . Otherwise we could add up to 5 vertices to the graph which are all connected to all other vertices.

 How can we reduce the clique function to matrix multiplication ? The rows and columns of the t t-matrix correspond to the vertex × sets A ⊆ V of size m=3 . The matrix entry yA;B should be equal to 1 iff A and B are disjoint and the graph G(x) implied by the input vector x contains the clique on A B . Obviously G(x) includes an m-clique ∪ iff for some sets A; B and C yA;B = yA;C = yB;C = 1 . We compute the Boolean matrix product Z = Y[2] . By definition zA;B = 1 iff for some C yA;C = yC;B = 1 . Hence we can compute

 cl n;m(x) = zA;B yA;B (12.4)

A[�];B

###### with O(t[2]) gates. Since BMt has t[2] different outputs, C(BMt) ≥ t[2], and it is sufficient to prove that all yA;B can be computed with O(t[2])

=
###### gates. Let yA = 1 iff G(x) includes the clique on A . All yA (|A| = m 3) can be computed with O(t) gates, since m is constant. yA;B = 0 if A and B are not disjoint. If A and B are disjoint, we partition A to A[′]

=
###### and A[′′] and B to B[′] and B[′′] where the partition sets are of size m 6 . Obviously


###### yA;B = yA[′]∪B[′] ∧ yA[′]∪B[′′] ∧ yA[′′]∪B[′] ∧ yA[′′]∪B[′′] ∧ yA ∧ yB


;
###### (12.5)


###### and all yA;B can be computed with O(t[2]) gates. 2

 We know now that C(f) = o(Cm(f)) for sorting, Boolean convolu- tion, Boolean matrix product, and certain clique functions. The lower

=
###### bounds known on Cm(f) C(f) are polynomial. Can this quotient be superpolynomial or even exponential ? To answer this question we consider perfect matchings.

;
###### DEFINITION 12.2 : PMn is defined on n[2] variables xij (1 ≤ i j ≤ n) .


-----

**194**


###### PMn(x) = [�] x1;π(1) ∧· · · ∧ xn;π(n)

_π∈Σn_


:
###### (12.6)


###### PMn is called logical permanent (if ∨ is replaced by ⊕ we obtain the determinant). PMn(x) = 1 iff the bipartite graph G(x) on V ∪ W =

; ; : : : ; ; ;

###### {v1 w1 vn wn} with edge set E(x) = {(vi wj) | xij = 1} includes a
 perfect matching, i.e. n vertex disjoint edges.

 Hopcroft and Karp (73) designed a polynomial algorithm for the decision whether or not a bipartite graph includes a perfect match- ing. Therefore (see Ch. 9) we can design circuits of polynomial size for PMn . Razborov (85 a) proved that the monotone complexity is superpolynomial.

 THEOREM 12.4 : Cm(PMn) = n[Ω(log n)] but C(PMn) = n[O(1)] . In

=
###### particular, Cm(PMn) C(PMn) is superpolynomial.

=
###### It is still an open problem whether Cm(f) C(f) can be exponential. Finally we present the largest lower bound known on the monotone complexity of explicitly defined Boolean functions. We should notice that cl n;m is defined on Θ(n[2]) variables. The following bound has been proved by Alon and Boppana (85) with Razborov’s method, the first exponential bound for this function is due to Andreev (85).


###### DEFINITION 12.3 : Polyq;s is defined on n = q[2] variables xij

;
###### (1 i j q) where q is prime. Let G(x) be the bipartite graph spec- ≤ ≤ ified by x (see Def. 12.2).

Z
###### Polyq;s(x) = 1 iff a polynomial p over the field q exists such that

;

###### degree(p) ≤ s − 1 and G(x) includes all edges (vi wp(i)) .

 THEOREM 12.5 : Cm(Polyq;s) = exp(Ω(n[1][=][4] log[1][=][2] n))

= =
###### for s = (1 2)(q logq)[1][=][2] .

 Superpolynomial and exponential lower bounds on the monotone circuit complexity of other Boolean functions can be proved via mono

-----

**195**

###### tone projections (see 1) or other monotone reductions (see Ch. 10, § 3). §

 6.13 Negation is powerless for slice functions

 Because of Theorem 12.4 one might conjecture that lower bounds on Cm(f) have no implications on C(f) . In the following we present a fundamental class of functions where negation is almost powerless, we prove that Cm(f) = O(C(f) + n log[2] n) for slice functions. Lower bounds on Cm(f) of size ω(n log[2] n) imply lower bounds of the same size on C(f) .

 Our problem is the simulation of circuits by monotone circuits. At

; ;
###### first we switch to the complete basis, the number of gates {∧ ∨ ¬} only needs to be increased by a constant factor (see Ch. 1, 3). Then § we double all -gates and -gates, one output of a pair is negated, the ∧ ∨ other one not. After that we can apply the deMorgan rules without increasing the number of gates. Finally we obtain a so-called standard circuit where only variables are negated. The most difficult problem is the replacement of xi by a monotone function. Such a replacement depends on the output of the circuit, since xi is not monotone. The concept of pseudo complements is due to Berkowitz (82).

 DEFINITION 13.1 : Let f ∈ Mn;m . A function hi ∈ Mn is a pseudo complement for xi with respect to f if in each standard circuit for f xi can be replaced by hi .

 DEFINITION 13.2 : f ∈ Bn is called k-slice if f(x) = 0 for inputs x with less than k ones and f(x) = 1 for inputs x with more than k ones. f = (f1 ; : : : ; fm) ∈ Bn;m is called k-slice if all fi ∈ Bn are k-slices.


-----

**196**

###### Slice functions are monotone. The interesting inputs for a k-slice

;
###### are those with exactly k ones, the elements of the k -th slice of 0 1 . { }[n]

; : : : ;

###### THEOREM 13.1 : Let X = {x1 xn} and Xi = X−{xi} . T[n]k[−][1](Xi)
 is a pseudo complement for xi with respect to k-slices f .

 Proof : Let f[′] be that function computed by a standard circuit for f after we have replaced xi by T[n]k[−][1](Xi) . We claim that f[′] = f . If input a includes less than k ones, f(a) = 0 and T[n]k[−][1](Xi)(a) = 0 ≤ ai . f[′](a) = 0, since standard circuits are monotone below the inputs. If input a includes more than k ones, f(a) = 1, T[n]k[−][1](Xi)(a) = 1 ≥ ai and f[′](a) = 1 by monotonicity. If input a includes exactly k ones

:
###### ai = 1 ⇔ ai = 0 ⇔ T[n]k[−][1](Xi)(a) = 1 (13.1)

 f(a) = f[′](a), since we do not have changed the circuit for these inputs. Altogether f[′] = f . 2

 The following generalization of Dunne (84) is left as an exercise.

 PROPOSITION 13.1 : hi Mn is a pseudo complement for xi with ∈ respect to f ∈ Mn;m iff


###### ∀ 1 ≤ j ≤ m : fj | xi=0 ≤ hi ≤ fj | xi=1


:
###### (13.2)


###### All f ∈ Mn have pseudo complements, but these pseudo comple- ments may be hard to compute. Slice functions have pseudo comple- ments which are easy to compute. Moreover, slice functions set up a basis of all monotone functions (Wegener (85 a) and (86 b)).

 DEFINITION 13.3 : The k -th slice f[k] of f ∈ Bn is defined by


###### f[k] = (f ∧ E[n]k[)][ ∨] [T][n]k+1 [= (f][ ∧] [T]k[n][)][ ∨] [T][n]k+1


:
###### (13.3)


###### THEOREM 13.2 : i) C(f) C(f[0] ≤


; : : : ;
###### f[n]) + O(n) .


-----

**197**


; : : : ;

###### ii) C(f[0] f[n]) C(f) + O(n) .
 ≤

; : : : ;

###### iii) Cm(f[0] f[n]) ≤ Cm(f) + O(n log n) if f monotone.
 iv) Cm(f[k]) ≤ Cm(f) + O(n) if f monotone and k constant.

 Proof : ii), iii), and iv) follow from (13.3) and the known upper bounds on the complexity of threshold functions. i) follows from


###### � f = (f[k] ∧ E[n]k[)][:] (13.4)

0 k n
_≤_ _≤_

###### 2

; : : : ;

###### Since C(f) = Θ(C(f[0] f[n])), if C(f) = Ω(n), we can investigate

; : : : ; ; : : : ;

###### (f[0] f[n]) instead of f . (f[0] f[n]) is called monotone representation
 of f, since f[k] is monotone. Even for non monotone f ∈ Bn we can com
; : : : ; ; : : : ;

###### pare C(f[0] f[n]) with Cm(f[0] f[n]) . Theorem 13.1 has the following
 corollary.


###### COROLLARY 13.1 : i) Cm(f[k]) ≤ O(C(f[k])) + Cm(k) where Cm(k) = Cm(Tk[n][−][1](Xi) | 1 ≤ i ≤ n) .

; : : : ; ; : : : ;

###### ii) Cm(f[0] f[n]) ≤ [�] O(C(f[k])) + Cm(0 n) where

0 k n
_≤_ _≤_

; : : : ; ;
###### Cm(0 n) = Cm(T[n]k[−][1](Xi) | 1 ≤ i ≤ n 0 ≤ k ≤ n) .

 Lower bounds on the monotone complexity of the k -th slice f[k] of some explicitly defined f ∈ Bn of size ω(Cm(k)) imply a lower bound of the same size on the circuit complexity of f . This fact offers a strong motivation for the investigation of monotone circuits and slice functions. We point out that we can use efficient circuits (over the basis B2) for f ∈ Mn for the design of efficient monotone circuits for

; : : : ;

###### (f[0] f[n]) but not for the design of efficient monotone circuits for f .
 (13.4) has no monotone analogue.

 What is the monotone complexity of the pseudo complements for slice functions ? The sets Xi are more or less alike. One might believe


-----

**198**

###### that it is sufficient to sort X and to remove xi afterwards. But this last step is impossible in monotone circuits. The best monotone circuits for all Tk[n][−][1](Xi) (1 ≤ i ≤ n) have been designed by Paterson (pers. comm.), Valiant (86), and Wegener (85 a).

; ;
###### THEOREM 13.3 : Cm(k) = O(n min{k n − k log[2] n}) .

 Proof : The following circuit is suitable for small k . Obviously


###### � ; : : : ; T[n]k[−][1](Xi) = T[i]p[−][1][(x][1] xi−1) ∧ T[n]k−[−]p[i] [(x][i+1]

0 p k
_≤_ _≤_


; : : : ;
###### xn) and (13.5)


; : : : ; �
###### xi 1) xi
_−_ _∧_


###### T[i]p[(x][1]


; : : : ; ; : : : ; �
###### xi) = T[i]p[−][1][(x][1] xi−1) ∨ T[i]p[−]−[1]1[(x][1]


:
###### (13.6)


; : : : ;

###### Because of (13.6) all T[i]p[(x][1] xi) (1 ≤ i ≤ n, 1 ≤ p ≤ k) can be com
; : : : ;

###### puted with at most 2 n k gates, the same holds for all T[n]k[−]p[i] [(x][i+1] xn)
_−_

###### (0 i n 1, 0 p k 1) . Because of (13.5) 2 n k further gates ≤ ≤ − ≤ ≤ − suffice for the computation of all T[n]k[−][1](Xi) . Hence Cm(k) ≤ 6 n k and by the duality principle also Cm(k) ≤ 6 n (n − k) .
 For k not too small and not too large the following attack is promis
; : : : ;
###### ing. W.l.o.g. n = 2[m] . For each r 0 m we partition X to 2[m][−][r] ∈{ }
 blocks of successive variables of 2[r] variables. Let Xir be the 2[r]-block that includes xi .
 We use a Batcher sorting network to sort X with O(n log[2] n) gates. As mentioned in § 2 we sort simultaneously all Xir . Xi = X −{xi} is the disjoint union of Zi;m−1 ; : : : ; Zi;0 where Zir is some 2[r]-block. We can
 sort Xi and compute Tk[n][−][1](Xi) by merging Zi;m−1 ; : : : ; Zi;0 . If we merge
 the small blocks at first, the intermediate results are of interest only for T[n]k[−][1](Xi) . If we merge Zi;m−1 and Zi;m−2, the result is of interest for all those 2[m][−][2] sets Xj where xj ̸∈ Zi;m−1 ∪ Zi;m−2 . Using this approach we merge always a large set and a smaller one. Now we make the most of the fact that we only compute T[n]k[−][1](Xi) and that we do not sort Xi .
 By Yir we denote the union of Zi;m−1 ; : : : ; Zi;r, in particular Yi0 =
 Xi . Since Yir = X − Xir, only 2[m][−][r] sets Yir are different. We are


-----

**199**

###### interested in the element of rank k in Yi0 (the k -th largest element of Yi0) . If we know the elements of rank k − 1 and k in Yi1, we can merge them with the 1-block Zi0, and the middle element is equal to T[n]k[−][1](Xi) . In general it suffices to know the elements of rank k−2[r+1] + 1; : : : ; k in Yi;r+1 . Since Yir is the disjoint union of Yi;r+1 and Zir, the

; : : : ;
###### elements of rank k − 2[r] + 1 k of Yir are the 2[r] middle elements in the output of a merging network if we merge the elements of rank k−2[r+1]+1; : : : ; k in Yi;r+1 with the elements in Zi;r . All other elements in Yi;r+1 cannot be elements of rank k − 2[r] + 1; : : : ; k in Yir .
 Thus we start with the sorted sets Yi;m−1 = Zi;m−1 ; : : : ; Zi0 . For

; : : : ; ; : : : ;
###### r = m 2 0 we compute the elements of rank k 2[r] + 1 k − − in Yir by merging the elements of rank k − 2[r+1] + 1; : : : ; k in Yi;r+1 and the elements in Zir . The middle 2[r] elements are the elements we are looking for. Using the Batcher merging network O((r + 1) 2[r+1]) gates suffice. For fixed r we need 2[m][−][r] of these merging networks, hence O((r + 1) 2[m]) = O((r + 1)n) gates. For all r together O(nm[2]) = O(n log[2] n) gates suffice. 2

 For practical purposes it is important to notice that the circuits in the proof of Theorem 13.3 are not only asymptotically efficient but also efficient for small n.

 We do not know of a nonlinear lower bound on the monotone com- plexity of some explicitly defined slice function f ∈ Mn . Razborov’s method cannot be applied directly to slice functions. Till today this is only a hypothesis many experts believe in, among them Razborov (pers. comm.). One should try to formalize this hypothesis and to prove the formal statement.

=
###### In 14 we discuss central slices, i.e. n 2-slices, and argue why § they are more important than k-slices for constant k . For central slices we have to prove ω(n log[2] n) bounds on the monotone complexity in order to obtain results for circuits over complete bases. Smaller lower bounds can work only for functions which have more efficient


-----

**200**

###### pseudo complements. Such classes of functions were introduced by Wegener (86 b).

 DEFINITION 13.4 : F[k]n [⊆] [M][n][ is the class of all k-slices f for which] the set of variables can be partitioned in such a way into k disjoint sets

; : : : ;

###### X[1] X[k] that each prime implicant of f of length k includes exactly
 one variable of each class. (The disjunction of the prime implicants of length k is a multilinear form.)

 The j -th variable of X[i] is denoted by x[i]j [(1][ ≤] [i][ ≤] [k, 1][ ≤] [j][ ≤] [n(i) =] |X[i]|) . Let hi be the disjunction of all variables in X[i] and let gi be the conjunction of all hj (j ̸= i) . Obviously n − k gates suffice for the computation of all hi . Then 3k − 6 gates suffice, if k ≥ 2, for the computation of all gi (Exercise 25, Ch. 3, generalized to monotone circuits). If we estimate the number of gates by 3k 3, the estimation − holds also for k = 1 . Let


###### yj[i] [= x]j[i] and z[i]j [=][ �] ym[i]
 [∧] [g][i]

m=j
_̸_


:
###### (13.7)


###### All yj[i] [can be computed with n gates, afterwards all z]j[i] [for fixed i can] be computed with at most 3n(i) 3 gates. Altogether we can compute − all yj[i] [and z]j[i] [with at most 5n] [−] [k] [−] [3 gates. y]j[i] [and z]j[i] [are almost pseudo] inputs and pseudo complements for x[i]j [with respect to functions in F]n[k] [.]

 THEOREM 13.4 : All yj[i] [and z]j[i] [can be computed with O(n) gates. If] we replace in a standard circuit for f ∈ F[k]n [x]j[i] [by y]j[i] [and x]j[i] [by z]j[i] [, then] f is replaced by some function f[∗] where f = f[∗] ∨ T[n]k+1 [. Hence]
 Cm(f) = O(C(f)) + O(n) + Cm(T[n]k+1[)][:] (13.8)

 Proof : We only have to prove that f = f[∗] ∨ T[n]k+1 [. If input a includes] either less than k ones or exactly k ones but not from k different classes, f(a) = 0 and T[n]k+1[(a) = 0 . Since y]j[i][(a) = 0][ ≤] [x][i]j[(a) and z][i]j[(a) =]


-----

**201**

###### 0 ≤ x[i]j[(a)][;][ f][∗][(a) = 0 by monotonicity. If input a includes exactly k ones] from different classes, T[n]k+1[(a) = 0 . The set of prime implicants of y]j[i] is the set of all monoms including exactly one variable of each class among them x[i]j [. PI(z]j[i][) is the set of all monoms including exactly one] variable of each class but not x[i]j [. Hence x]j[i][(a) = y]j[i][(a), x][i]j[(a) = z][i]j[(a)] and f(a) = f[∗](a) . If a includes more than k ones, T[n]k+1[(a) = 1 and] f(a) = 1, since f is a k-slice. In this case the correcting term T[n]k+1 [is] necessary. 2

 DEFINITION 13.5 : G[k]n 2 [for which]
 [⊆] [M][n][ is the class of all g = g][∗] [∨][T][∗] the set of variables can be partitioned in such a way into k disjoint

; : : : ;

###### sets X[1] X[k] that each prime implicant of g[∗] includes exactly one
 variable of each class. T[∗]2[(X) is the disjunction of all T][n(i)]2 [(X][i][) .]

 THEOREM 13.5 : If we replace in a standard circuit for g ∈ G[k]n x[i]j [by y]j[i] [and x]j[i] [by z]j[i] [, then g is replaced by some function g][′][ where] g = g[′] ∨ T[∗]2 [. Hence]

:
###### Cm(g) = O(C(g)) + O(n) (13.9)

 Proof : The proof is similar to that of Theorem 13.4. Cm(T[∗]2[) = O(n),] since Cm(T[n(i)]2 [) = O(n(i)) .] 2

 COROLLARY 13.2 : i) C(f) = Θ(Cm(f)) for f ∈ F[k]n [if C][m][(f) =]

; ;
###### ω(n min k n k log n ) . { − }
 ii) C(g) = Θ(Cm(g)) for g ∈ G[k]n [.]

 According to Corollary 13.2 already lower bounds of size n log n or n log[∗] n on the monotone complexity of certain functions imply similar bounds for circuits over complete bases.


-----

**202**

###### Dunne (84) applied the concept of slice functions and proved for the most complex (n − k)-homogeneous functions f ∈ H[n]n[−][k] (see Ch. 4, § 7) that C(f) = Θ(Cm(f)) . More precisely, Cm(f) = O(C(f))+O(n[k][−][1]) for f ∈ Hn[n][−][k] and constant k .
 The monotone complexity of the set of all pseudo complements has been determined by Wegener (86 b).

; : : : ;
###### THEOREM 13.6 : Cm(0 n) = Θ(n[2]) .

 Proof : The lower bound is obvious, since we consider n(n 1) different −

;
###### outputs Tp[n][−][1](Xi) (1 ≤ p ≤ n − 1 1 ≤ i ≤ n) .
 For the upper bound we analyze Batcher’s merging network for merging sorted lists of different size k = 2[i] and l = 2[j], w.l.o.g. k l . ≥ We only modify Step 1 of Algorithm 2.1.b. If l = 1, k comparisons

;
###### suffice. Hence M(k l ), the number of comparisons, fulfils the following recursion equation.

; = ; = = ; :
###### M(k l ) = 2 M(k 2 l 2) + (k + l ) 2 1 and M(k 1) = k − (13.10)

 Since the depth of recursion is only log l,

; = :
###### M(k l ) = (k + l )(log l ) 2 + k l + 1 (13.11) −

 W.l.o.g. n = 2[m] . We apply a Batcher sorting network and sort X and all n 2[−][r] blocks of 2[r] successive variables. For this step O(n log[2] n) gates suffice. As in the proof of Theorem 13.3 Xi is the disjoint union of Zi;m−1 ; : : : ; Zi;0 where Zir is some 2[r]-block. Again Yir is the union
 of Zi;m−1 ; : : : ; Zir, hence Yi0 = Xi . We sort Yir by merging Yi;r+1 and
 Zir . The size of Yi;r+1 is bounded by n, hence M(n; 2[r]) ≤ nr + n comparisons suffice. For fixed r (0 r m 2) we need 2[m][−][r] of these ≤ ≤ − merging networks, hence

 2[m][−][r](nr + n) = n[2](r + 1) 2[−][r] (13.12)

 comparisons. Summing up for all r we can esimate the number of gates by 6 n[2] . 2


-----

**203**

###### This result implies that for all functions f ∈ Bn which cannot be computed very efficiently, it is almost sufficient to investigate

; : : : ;

###### the monotone complexity of the monotone representation (f[0] f[n])

; : : : ; =

###### of f . More precisely, C(f) = Ω(Cm(f[0] f[n]) n) and C(f) =

; : : : ;

###### Θ(C(f[0] f[n])) .


###### 6.14 Hard slices of NP-complete functions

 According to Theorem 13.2 there is for each f ∈ Bn some k such

=
###### that C(f[k]) = Ω(C(f) n) . Difficult functions have difficult slices, but they also may have easy slices, e.g. for k = 0 or k = n . We like to know which slice is hard, and we ask for relations between the complexity of f[k] and f[k+1] .

 As examples for probably hard functions we consider NP-complete functions, in particular the clique function cl n;m for m = n=2 (see Def. 11.1). cl n;m has �mn � prime implicants, one for each vertex set A �m� of size m . All prime implicants tA are of length 2, tA is testing whether all edges on A exist. The �m2 �-slice of cl n;m has the same �m� prime implicants and additional prime implicants of length + 1 .
2
###### This slice looks similar to cl n;m, but this slice is easy to compute (Wegener (85 a)).

 DEFINITION 14.1 : If f ∈ Mn has only prime implicants of length k, f[k] is called the canonical slice of f .

 THEOREM 14.1 : The circuit complexity of the canonical slice of cl n;m MN where N = �n2� is O(N), its monotone complexity ∈ O(N log N), for constant m only O(N) .


-----

**204**

###### �m� Proof : The canonical slice is the M-slice for M = .
2


###### cl [M]n;m [= (c][l][ n][;][m][ ∧] [E]M[N] [)][ ∨] [T][N]M+1 [= (c][l][ n][;][m][ ∧] [T]M[N] [)][ ∨] [T][N]M+1


:
###### (14.1)


###### In (14.1) we can replace cl n;m by any function g which equals cl n;m on graphs with exactly M edges. T[N]M [and T]M+1[N] [have circuit complexity] O(N) .

 A graph with exactly M edges includes an m-clique iff the M edges set up an m-clique. This happens iff at least m vertices have degree at least m 1 . This condition can be expressed by threshold functions. − Let Xi = {x1i ; : : : ; xi−1;i, xi;i+1 ; : : : ; xin}. Xi includes the variables de scribing the edges adjacent to vertex i . In (14.1) we can replace cl n;m

: : : ;
###### by T[n]m [(T]m[n][−]−[1]1[(X][1][)][;] Tm[n][−]−[1]1[(X][n][)) . All these n + 1 threshold functions] have circuit complexity O(n), altogether O(n[2]) = O(N) . The results for monotone circuits follow in the same way. 2

 DEFINITION 14.2 : f[∗] = f[⌈][n][=][2][⌉] is the central slice of f ∈ Bn .

 �n=2� THEOREM 14.2 : For n even and l ≥ 2
 Cm(cl [l]n;n=2[)][ ≤] [C][m][(c][l] [∗]5n;5n=2[)][:] (14.2)

< �n=2� �n�
###### If l 2, cl [l]n;n=2 [= T]l[N]+1 [for N =] 2 .

 This theorem due to Dunne (84) implies that the central slice of cl n;n=2 has polynomial (monotone) circuits iff cl n;n=2 has polynomial circuits. Furthermore cl [∗]n;n=2 [is an NP-complete predicate, since the] reduction in the following proof can be computed in polynomial time.


###### Proof of Theorem 14.2 : It is sufficient to prove that cl [l]n;n=2 [is a sub-]

; : : : ; ; ; : : : ;

###### function of cl [∗]5n;5n=2 [. We denote the vertices by v][1] vn w1 w4n
 and replace all variables corresponding to edges which are adjacent


-----

**205**

; : : : ;

###### to some w-node by an appropriate constant. The vertices w1 w2n
 form a 2n-clique, and these vertices are connected to all v-vertices.

;

###### The variables for the edges (wi w2n+i) (1 ≤ i ≤ 2n) are replaced by 0 .
 �4n� Altogether + 4n[2] variables should be replaced by constants.
2
###### �2n� Until now we have decided that + 2n[2] edges exist and that 2n
2
###### edges do not exist. We still have to decide about �4n� �2n�
 + 4n[2] 2n[2] 2n = 8n[2] 3n (14.3) − − − −
 2 2

 ��5n�= � ��2n� edges. Let r = 2 l +2n[2][�] . Then 0 r 8n[2] 3n . We
2 _−_ _−_ 2 _≤_ _≤_ _−_

###### decide that exactly r of the 8n[2] 3n variable edges exist. Altogether − ��5n�= � the graph contains now 2 l edges.
2 _−_

=
###### It remains to be proved that the graph on V includes an n 2-clique

=
###### or more than l edges iff the graph on V W includes an 5n 2-clique ∪ ��5n�= � = or more than 2 edges. Each n 2-clique on V can be extended
2

= ; : : : ;
###### to a 5n 2-clique on V ∪ W by adding w1 w2n . If the graph on
 W included a (2n + 1)-clique, this clique would include for some i the vertices wi and w2n+i . This is impossible, since wi and w2n+i are not

= =
###### connected. Hence a 5n 2-clique on V W implies an n 2-clique on ∪ V . The assertion on the number of edges is obvious, since the graph ��5n�= � includes 2 l edges adjacent to some w-vertex. 2
2 _−_


###### Results similar to those in Theorem 14.1 and 14.2 can also be proved for other NP-complete predicates (see Exercises). In order to obtain more results on the complexity of the slices of some function, we compare the complexity of the k-slice with the complexity of the (k + 1)-slice of some function f. Dunne (84) proved that f[k+1] is not much harder than f[k], whereas Wegener (86 b) proved that f[k+1] may be much easier than f[k] .

 THEOREM 14.3 : Let f ∈ Mn have prime implicants of length k only. Then Cm(f[k+][l] ) = O(n Cm(f[k+][l] [−][1])) for l ≥ 1 .


-----

**206**

###### Proof : The key to the proof is the realization of f[k+][l] by

 � f[k+][l] (x) = f[k+][l] [−][1](hi(x)) ∧ T[n]k+l [(x)][ ∨] [T][n]k+l +1[(x)] (14.4)

1 i n
_≤_ _≤_


###### for hi(x) = y where yi = 0 and yj = xi xj for i ̸= j . (14.4) implies

;

###### the theorem, since Cm(f[k+][l] [−][1]) = Ω(n), Cm(T[n]k+l T[n]k+l +1[) = O(n][2][) and]

; : : : ;

###### Cm(h1 hn) = O(n[2]) .

 (14.4) is obvious for inputs with less or more than k + l ones. Let a be an input with exactly k + l ones. W.l.o.g. ai = 1 iff i ≤ k + l . If

 - ; : : : ;
###### i k + l, hi(a) = (0 0) and f[k+][l] [−][1](hi(a)) = 0 . If i ≤ k + l, hi(a) differs from a only at position i, in particular hi(a) includes k + l − 1 ones.

 If f[k+][l] [−][1](hi(a)) = 1, p(hi(a)) = 1 for some p ∈ PI(f) . Since hi(a) ≤ a, p(a) = 1 and f[k+][l] (a) = 1 .

 If f[k+][l] (a) = 1, p(a) = 1 for some p PI(f) . By our assumption ∈ p has length k . By definition of a the variables of p have indices j ≤ k + l . Since l ≥ 1, p(hi(a)) = 1 for some i such that xi is not in p . Hence f[k+][l] [−][1](hi(a)) = 1 . 2

; �n−1�� �n−1��−1
###### THEOREM 14.4 : Let c(k n) = log . There are
k 1 k 1
_−_ _−_
###### functions f ∈ Mn with prime implicants of length k only, such that

;             ###### Cm(f[k]) = Ω(c(k n)) and Cm(f[l] ) = O(n log n) for l k .

 Proof : Let Fk;n be the set of all functions f such that all prime implicants have length k and each monom of length k not including x1 is a prime implicant of f . Then f ∈ Fk;n is defined by a subset
n 1
###### of all monoms of length k including x1 . Hence log |Fk;n| = �k−−1� .

;
###### By Shannon’s counting argument Cm(f[k]) = Ω(c(k n)) for almost all f ∈ Fk;n .


-----

**207**

                 ###### It suffices to prove that f[l] = T[n]l [for f][ ∈] [F][k][;][n][ and][ l] k . By definition f[l] = (f ∧ T[n]l [)][ ∨] [T]l[n]+1 [. Obviously f][l][ ≤] [T]l[n] [. Let T]l[n][(a) = 1 .]

         ###### Then a includes l ones. Since l k, input b, defined by b1 = 0 and bi = ai for i ̸= 1, includes at least k ones, and, by definition of Fk;n, f(b) = 1 . 2

 6.15 Set circuits - a new model for proving lower bounds

 We are not able to prove non linear lower bounds on the circuit complexity of explicitly defined Boolean functions. For monotone cir- cuits we know several methods for the proof of lower bounds, and for slice functions f lower bounds on Cm(f) imply lower bounds on C(f) . Hence we should apply our lower bound methods to slice functions. The reader should convince himself that our bounds (at least in their pure form) do not work for slice functions. In this section we dis- cuss some particularities of monotone circuits for slice functions f and present some problems whose solution implies lower bounds on Cm(f) and therefore also on C(f) (Wegener (85 a) and (86 b)).

 Let PIk(g) be the set of prime implicants of g whose length is k .

<
###### Let M[k]n [be the set of f][ ∈] [M][n] [where PI][l] [(f) =][ ̸][◦] [for][ l] k . M[k]n [includes] all k-slices.

 LEMMA 15.1 : Let S be a monotone circuit for f ∈ M[k]n [. If we replace] the inputs xi by yi = xi ∧ T[n]k [, then the new circuit S][′][ also computes f .]

 The proof of this and the following lemmas is left to the reader. For the computation of the pseudo inputs n + Cm(T[n]k[) gates suffice.] All functions computed in S[′] are in M[k]n [. In the following sense slice] functions are the easiest functions in M[k]n [.]


-----

**208**

;
###### LEMMA 15.2 : Let f f[′] ∈ M[k]n [and PI][k][(f) = PI][k][(f][′][) . If f is a k-slice,] f = f[′] ∨ T[n]k+1 [and C][m][(f)][ ≤] [C][m][(f][′][) + C][m][(T]k+1[n] [) + 1 .]

 Hence we consider prime implicants of length k only. If we do not compute any shorter prime implicants, prime implicants of length k will not be eliminated by the law of simplification.

;
###### LEMMA 15.3 : Let f g ∈ M[k]n [. Then]

 PIk(f ∨ g) = PIk(f) ∪ PIk(g) and (15.1)

:
###### PIk(f ∧ g) = PIk(f) ∩ PIk(g) (15.2)

 These lemmas motivate the so-called set circuits.

 DEFINITION 15.1 : The inputs of a set circuit are for some k the sets Yi = PI(xi T[k]n[) and the operations are binary unions and] ∧ intersections. The set complexity of f ∈ M[k]n [, denoted by SC(f), is the] least number of gates in a set circuit for PIk(f) .

 THEOREM 15.1 : Let f be a k-slice. Then

;

###### i) Cm(f) ≤ SC(f) + Cm(T[n]k T[n]k+1[) + n + 1 .]

; ;
###### ii) SC(f) ≤ Cm(f) ≤ O(C(f)) + O(n min{k n − k log[2] n}) .


###### Proof : We only combine the assertions of Lemma 15.1, 15.2, 15.3, Theorem 13.1, Corollary 13.1, and Theorem 13.3. 2

 Set circuits form the principal item of monotone circuits and cir- cuits for slice functions. So we obtain a set theoretical or combinatorial representation of circuits.
 For the classes of functions F[k]n [and G]n[k] [(see Def. 13.4 and 13.5) we] can use the pseudo inputs yj[i] [and in set circuits the sets Y]j[i] [= PI(y]j[i][),] the prime implicants in Yj[i] [all have exactly one variable of each class]


-----

**209**

###### X[i] . This holds for all gates of a set circuit with inputs Yj[i] [. This leads] to both a geometrical and combinatorial representation of set circuits.

 The set of monoms with exactly one variable of each class X[i]
 (1 i k) can be represented as the set theoretical product ≤ ≤

: : : ; ; : : : ;
###### Q = n(i) where (r(1) r(k)) Q corresponds to the
### ×1 i n[{][1][;] } ∈
_≤_ _≤_

: : :

###### monom x[1]r(1) x[k]r(k) [. Q is a k-dimensional, discrete cuboid. Input Y]j[i]

; : : : ;
###### corresponds to the (k 1)-dimensional subcuboid of all (r(1) r(k)) − where r(i) = j . The set of prime implicants of f ∈ F[k]n [or g][ ∈] [G]n[k] [cor-] responding to vertices in Q forms a subset Q(f) or Q(g) of Q, called pattern of f or g . Set circuits for f or g correspond to computations of Q(f) or Q(g) by unions and intersections out of the (k 1)-dimensional − subcuboids of Q .

 For n = 2 k and n(1) = = n(k) = 2 we work on the k-dimen- · · ·

; ;
###### sional cube 0 1 (or 1 2 ) . There is a one-to-one relation between { }[k] { }[k]

;
###### subsets Q[′] of {0 1}[k] and functions in F[k]n [or G]n[k] [. If we could prove for]

;
###### some explicitly defined set Q[′] 0 1 that ω(n) binary unions and ⊆{ }[k] intersections are necessary for the computation of Q[′] out of all (k 1)- −

;
###### dimensional subcubes of 0 1, then we would have proved a lower { }[k] bound of the same size on the circuit complexity of the corresponding g ∈ G[k]n [.]
 In order to illustrate our geometrical approach as well as for later purposes, we prove that the canonical slice of the Boolean convolution has linear complexity.

 THEOREM 15.2 : The monotone complexity of the canonical slice of the Boolean convolution is linear.

 Proof : The canonical slice is the 2-slice, the Boolean convolu- tion is a function in F[2]2n;2n−1 [.] Hence the cuboid considered is

; : : : ;
###### the square 1 n . The i -th row corresponds to the set of { }[2]

; : : : ;

###### monoms Ai = {xi y1 xi yn} and the j -th column corresponds to

; : : : ;

###### Bj = {x1 yj xn yj} . These sets are inputs of the set circuit. We


-----

**210**

###### have to compute the Boolean convolution, i.e. the diagonal sets Tk = {xi yj|i + j = k} . It is sufficient to design a set circuit of linear

; : : : ;

###### size for T2 T2n .
 W.l.o.g. n = m[2] . We partition the square to m[2] subsquares of side length m each (see Fig. 15.1).

 1. Dl = A(l −1)m+1 ∪· · · ∪ A(l −1)m+m (1 ≤ l ≤ m) (m[2] − m gates).
 2. El = B(l −1)m+1 ∪· · · ∪ B(l −1)m+m (1 ≤ l ≤ m) (m[2] − m gates).

;
###### 3. Fij = Di ∩ Ej (1 ≤ i j ≤ m) (m[2] gates). Fij are the subsquares of side length m .


###### 4. Gij = Fij (2 ≤ l ≤ 2m) (m[2] − 2m + 1 gates).
 [�]

i+j=l

###### Gl is the l -th diagonal consisting of subsquares.
 5. Hl = Al ∪ Am+l ∪· · · ∪ A(m−1)m+l (1 ≤ l ≤ m) (m[2] − m gates).
 6. Il = Bl ∪ Bm+l ∪· · · ∪ B(m−1)m+l (1 ≤ l ≤ m) (m[2] − m gates).

;
###### 7. Jij = Hi ∩ Ij (1 ≤ i j ≤ m) (m[2] gates).

;
###### Jij includes of each subsquare the element at position (i j) .
 8. Kl = Jij (2 ≤ l ≤ 2m) (m[2] − 2m + 1 gates).
 [�]

i+j=l

###### Kl consists of all l -th diagonals of subsquares.
 Tk cuts at most two adjacent diagonals of subsquares, say Gh(k) and perhaps Gh(k)+1 (see Fig. 15.1). The intersection of Tk and Gh(k) con- sists of all d[′](k)-th diagonals of the subsquares in Gh(k) . Let d[′′](k) be the corresponding parameter for the intersection of Gh(k)+1 and Tk . Hence
 9. Tk = (Gh(k) ∩ Kd′(k)) ∪ (Gh(k)+1 ∩ Kd′′(k)) if k − 1 is not a multiple of m and m + 2 k m[2] m, and ≤ ≤ − Tk = Gh(k) Kd′(k) otherwise. ∩ Here 2 k 2n and 6n 8m + 3 gates suffice. ≤ ≤ −
 Altogether the set circuit consists of 14n 16m + 5 gates. 2 −


-----

###### x x [x]


**211**

###### n = 16, m = 4, k = 12, h(k) = 3,

 d1(k) = 8, d2(k) = 4,

 T12 = (G3 ∩ K8) ∪ (G4 ∩ K4)

 Fig. 15.1

|Col1|x|x x x|Col4|
|---|---|---|---|
|x|x x x|||
|x x x||||
|||||


###### At the end of this section we discuss relations between functions of n outputs and their corresponding one output function. These considerations result in another combinatorial problem whose solution would probably imply lower bounds for slice functions.

; : : : ; ; : : : ; ; : : : ;

###### Let x = (x1 xn) and y = (y1 yn) . For f1 fn Mn we
 ∈

; ; : : : ;
###### define g g1 gn Mn by
 ∈

; ; � ; :
###### gi(x y) = yi ∧ fi(x) and g(x y) = gi(x y) (15.3)

1 i n
_≤_ _≤_


###### LEMMA 15.4 : i) Cm(g1


; : : : ;
###### gn) = Cm(f1


; : : : ;
###### fn) + n .


###### ii) Cm(g) ≤ Cm(g1


; : : : ;
###### gn) + n − 1 .


###### Proof : The upper bounds follow from the definition and the lower bound can be proved by the elimination method. 2

 For many functions, in particular those functions we have investi- gated in 4 – 9, we suppose that equality holds in Lemma 15.4 ii. § §

; : : : ; _′_ n

###### Let us consider k-slices F1 Fn ∈ Mn . Then Fi = Fi ∨ Tk+1 [where]
 PI(Fi′) = PIk(Fi) . Since yi Fi is in general no slice, we define the ∧

; ; : : : ;
###### (k + 1)-slices G G1 Gn by


-----

**212**


;
###### Gi(x y) = G[′]i[(x][;][ y)][ ∨] [T][2n]k+2[(x][;][ y)] where (15.4)

_′_ ; ; � ; :
###### G[′]i[(x][;][ y) = y][i] [∧] [F][i] (x) and G(x y) = Gi(x y) (15.5)

1 i n
_≤_ _≤_

###### Since yi ∧ T[n]k+1[(x)][ ≤] [T][2n]k+2[(x][;][ y), we can replace in (15.4) F]i[′] [by F][i][ . By] definition we obtain the following upper bounds.


###### LEMMA 15.5 : i) Cm(G1


; : : : ;
###### Gn) ≤ Cm(F1


; : : : ;
###### Fn)+Cm(T[2n]k+2[)+2n .]


###### ii) Cm(G) ≤ Cm(G1


; : : : ;
###### Gn) + n − 1 .


###### Even a partial converse of Lemma 15.5 ii can be proved.

; : : : ;

###### LEMMA 15.6 : CΩ(G1 Gn) ≤ CΩ(G) + CΩ(T[2n]k+2[) + 2n for Ω] [∈]

;

###### {B2 Ωm} .


###### Proof : The assertion follows from the following representation of Gi .

;
###### G(x y) ∧ yi ∨ T[2n]k+2[(x][;][ y)] (15.6)

2n

###### � � ′ � = yj ∧ Fj (x) ∨ Tk+2[(x][;][ y)] ∧ yi ∨ T[2n]k+2[(x][;][ y)]

1 j n
_≤_ _≤_


###### �� � = (F[′]i[(x)][ ∧] [y][i][)][ ∨] F[′]j[(x)][ ∧] [y][j][ ∧] [y][i] ∨ (T[2n]k+2[(x][;][ y)][ ∧] [y][i][)][ ∨] [T][2n]k+2[(x][;][ y)]

j=i
_̸_

2n
###### = (Fi′(x) ∧ yi) ∨ Tk+2[(x][;][ y) = G][i][(x][;][ y)][:]


###### 2

 What about a partial converse of Lemma 15.5 i ? In opposition to Lemma 15.4 i we cannot apply the elimination method. If we set y1 = · · · = yn = 1 and if k ≤ n − 2, T[2n]k+2[(x][;][ y) = 1 and G][i][(x][;][ y) =]

; : : : ;

###### 1 . We even suppose that Cm(F1 Fn) can be much larger than

; : : : ; ; : : : ;

###### Cm(G1 Gn) . To underpin this supposition, let F1 Fn ∈ F[k]n [,]

; : : : ; ; : : : ;

###### i.e. our geometrical view works for F1 Fn . Then G1 Gn
 ∈ F[k+1]n, the (k + 1)-st dimension concerns the y-variables. The patterns

; : : : ;

###### F1 Fn are defined on the same k-dimensional cuboid Q . Gi has
 to be constructed on a (k+1)-dimensional cuboid Q[′] . More precisely,


-----

**213**

###### the pattern of Gi equals the pattern of Fi and has to be constructed on that k-dimensional subcuboid Qi of Q[′] where the last dimension is

; : : : ;

###### fixed to i. G1 Gn can be constructed ˝in parallel˝ on the disjoint

; : : : ;

###### subcuboids Qi of Q[′], but F1 Fn have to be constructed on the
 same cuboid Q . Obviously Q and Qi are isomorphic. We illustrate these considerations in an example.

; : : : ;

###### Let f1 fn be the Nechiporuk Boolean sums (see § 6). Then

; : : : ; ; : : : ;

###### Cm(f1 fn) = Θ(n[3][=][2]) . Let F1 Fn be the canonical slices, i.e.

; : : : ; ; ; : : : ;

###### the 1-slices, of f1 fn, and let G G1 Gn be defined by (15.4)
 and (15.5). We consider the pattern of G, which is a subset of the square {1; : : : ; n}[2] . The pattern of G consists of the subpatterns Mb;d of (6.10), so G is composed of small diagonals. Similarly to Theorem 15.2 we can prove


###### LEMMA 15.7 : Cm(G) = O(n) .

; : : : ;

###### By Lemma 15.6 also Cm(G1 Gn) = O(n) . Lemma 15.6 can now

; : : : ;
###### be made clear. G is a pattern in the square {1 n}[2], Gi the subpat- tern in the i -th row. Let us consider again the algorithm for the proof of Theorem 15.2. We compute ˝in parallel˝ different useful patterns in different rows. This approach cannot be used for the computation

; : : : ; ; : : : ;

###### of F1 Fn . In that case we work on the cuboid {1 n}[1], i.e.

; : : : ;
###### the set 1 n, and we cannot work ˝in parallel˝. We suppose { }

; : : : ; ; : : : ; ; : : : ;

###### that SC(f1 fn), Cm(F1 Fn) and therefore also C(F1 Fn)
 are nonlinear. We reformulate in a pure set theoretical setting the

; : : : ;

###### problem of computing SC(f1 fn) . Nonlinear lower bounds for this
 problem imply lower bounds of the same size on the circuit complexity

; : : : ;

###### of the explicitly defined Boolean sums f1 fn .


; : : : ;
###### Inputs : 1 n . { } { }
 Operations :, (binary). ∩ ∪

; : : : ;

###### Outputs : H1 Hn where Hi = {j | xj ∈ PI(fi)} .

; : : : ;

###### Problem : SC(H1 Hn) = ? ( = (|Hi| − 1) ?) .

 [�]

1 i n
_≤_ _≤_


-----

**214**

###### EXERCISES :

 1. Let f ∈ Mn be in MDNF. If we replace ∧ by ∗ and ∨ by +, we obtain the polynomial p(f) . Then Cm(f) ≤ C{+;∗}(p(f)), but equality does not hold in general.

 2. If a sorting network sorts all 0-1-sequences, it also sorts all se- quences of real numbers.

 3. C[∧]m[(T][n]2[) =][ ⌈][log n][⌉] [.]


###### 4. C[∧]m[(f) = 2 n for f(x][1]


; : : : ; x3n) = � T[3]2[(x][3i][−][2]

1 i n
_≤_ _≤_


;
###### x3i 1
_−_


;
###### x3i) .


###### 5. C[∧]m[(S][n][) = C][∨]m[(S][n][) = Ω(n log n) .]

 6. Each monotone circuit for S[n] includes a permutation network, i.e. for π ∈ Σ[n] there are disjoint paths from xi to the output T[n]π(i) [.]

 7. The minimal external path length of binary trees with n leaves is n log n 2[⌈][log n][⌉] + n . ⌈ ⌉−

 8. Let f be a semi-disjoint bilinear form.

;
###### Then Cm(f) ≥ min{|X| |Y|}[−][1](t(1) + · · · + t(m)) where t(j) is defined in (4.2).

 9. Formulate the replacement rules dual to Theorem 5.1 and 5.2 and discuss applications.

 10. The replacement rules of Theorem 5.1 and 5.2 are powerless for slice functions.

 11. Let g be computed in a monotone circuit for the Boolean convo
;
###### lution. Let t t[′] ∈ PI1(g). Can g be replaced by the constant 1 ?


-----

**215**

###### 12. Let g be computed in a monotone circuit for f . a) g can be replaced by 0 t PI(g) t[′] monom : t t[′] PI(f) . ⇔∀ ∈ ∀ ̸∈ b) g can be replaced by 1 (g h f h f) . ⇔ ≤ ⇒ ≤

 13. Let f be the Boolean sum of Theorem 6.1. Then Cm(f) = 17 and C (f) = 18 .
_{∨}_

###### 14. Which is the largest lower bound that can be proved using (6.9) and Theorem 6.2 ?

;
###### 15. Apply the methods of the proof of Theorem 7.1 to (1 1)-disjoint Boolean sums.

 16. For a semi-disjoint bilinear form f let G(f) be the bipartite graph

; ;
###### including the edge (r s) iff xr ys PI(fk) for some k . Let V(r s) ∈

;
###### be the connected component including the edge (r s) . f is called

;
###### a disjoint bilinear form iff V(r s) and PI(fk) have at most one edge (or prime implicant) in common.

 a) The Boolean matrix product is a disjoint bilinear form.

 b) The Boolean convolution is not a disjoint bilinear form.

 17. If f ∈ Mn;n is a disjoint bilinear form, | PI(f)| = O(n[3][=][2]) .

 18. If f ∈ Mn;m is a disjoint bilinear form, Cm[∧] [(f) =] � | PI(fk)| .

1 k m
_≤_ _≤_


###### 19. The monograph Savage (76) contains a proof that � C[∨]m[(f) =] (| PI(fk)| − 1) for disjoint bilinear forms.

1 k m
_≤_ _≤_

###### a) The proof is incorrect. Find the error.


-----

**216**


###### b) Barth (80) presented the following counterexample.

; <

###### g is defined on xi yi (0 ≤ i 2n[2]). The output gk (k =

; : : : ; ; : : : ;

###### (k0 k3) ∈{0 n − 1}[4]) has the prime implicants xa(k)yb(k)
 and xc(k)yd(k) where a(k) = k3n + k0, b(k) = k2n + k1, c(k) = n[2] + k1n + k0, d(k) = n[2] + k3n + k2 . Hint: Consider the MCNF of g .

 20. Optimal monotone circuits for the Boolean matrix product are unique up to associativity and commutativity.

 21. Maximize N M[m] for m M N n and M[m] n . ≤ ≤

 22. Apply the elimination method to the generalized matrix product fMN[m] [.]

 23. Let P(n) be the circuit complexity of the Boolean matrix product. Prove upper bounds on C(fMN[m] [) depending on n and P(n) .]

 24. Investigate the MCNF of fMN[m] [. How many][ ∨][-gates are sufficient] for the computation of fMN[m] [?]


###### 25. Design ∗-circuits for fMN[m] with N M[m] ∧-gates where
 i + 1

; : : : ; ;

###### v(h1 hm l ) = for all prime implicants (i fixed, m
 2i
 large).
 a) For almost all gates v(G) = [1]
 2 [.]
 b) For almost half of the gates v(G) = 0, for the other gates v(G) = 1 .

 26. B PI(f) is called isolated if r = s or r = t for r PI(f) . Compute ⊆ ∈ the size of the largest isolated set for a) the Boolean convolution b) the clique function.

 27. Schnorr (76 c) conjectured by analogy with his results on arith- metic circuits that C[∨]m[(f)][ ≥|][B][|][ for isolated sets B . Wegener (79 b)]


-----

**217**


###### presented the following counterexample. Let yhh[′]h[′′] be the outputs of fM2[3] [and let g be defined on M][3][ + 6M][2][ variables by]

; � :

###### g(x[i]jl zhh[′]h[′′]) = yhh[′]h[′′] zhh[′]h[′′]

1 h;h[′] ;h[′′] M
_≤_ _≤_

###### PI(g) is isolated but C[∨]m[(g)][ ≤] [M][3][ + 6M][2][ + 3M][ −] [1 (use the MCNF] for fM2[3] [) .]

 28. Cm(f) = Θ(2[n]n[−][3][=][2]) for almost all slices f ∈ Mn .

 29. If C(f) = Ω(2[n]n[−][1]), f has Ω(n[1][=][2]) slices of complexity Ω(2[n]n[−][2]) .

 30. Prove Proposition 13.1.

 31. The canonical slice of the Boolean matrix product has complexity O(n[2]) .

 32. Design efficient circuits for the canonical slices of the following functions : a) Perfect matching PMn (see Def. 12.2). b) UHCn (and DHCn) . UHCn(x) = 1 iff the undirected graph G(x) on n vertices specified by the variables x includes a Hamilto- nian circuit, i.e. a circuit of length n . DHC is the same function for directed graphs.

 33. Cm(DHC[l]n[)][ ≤] [C][m][(DHC][∗]7n[) if n][ ≤] [l][ ≤] [n(n][ −] [1) .]

 34. Prove Lemma 15.1, 15.2, 15.3, and 15.7.


-----

**218**

###### 7. RELATIONS BETWEEN CIRCUIT SIZE, FORMULA SIZE AND DEPTH

 We investigate the relations between the complexity measures cir- cuit size C, formula size L and depth D . A more intensive study of formulas (in Ch. 8) is motivated by the result that D(f) = Θ(log L(f)) . For practical purposes circuits of small size and depth are preferred. It is an open problem, whether functions of small circuit size and small depth always have circuits of small size and depth. Trade-offs can be proved only for formula size and depth.

 7.1 Formula size vs. depth

 The relations between formula size and depth have been in- vestigated also for arithmetic computations (Brent, Kuck and Murayama (73), Muller and Preparata (76), and Preparata and Muller (76)). The results are similar to those for Boolean formulas, D(f) = Θ(log L(f)), hence formula size is also a complexity measure for parallel time.

 DEFINITION 1.1 : The selection function sel ∈ B3 is defined by

; ; :
###### sel(x y z) = xy xz (1.1) ∨

 For a basis Ω


###### k(Ω) = [D][Ω][(sel) + 1]
 log 3 1 −


:
###### (1.2)


###### The variable x decides which of the variables y or z we se- lect. If sel is computable over Ω, k(Ω) is small. In particular,

= :
###### k(B2) = 3 (log 3 − 1) ≈ 5 13. Obviously sel is not monotone. Let

; ;
###### sel[′](x y z) = y xz . Then sel[′] = sel for all inputs where y z . ∨ ≤


-----

**219**

=
###### Since Dm(sel[′]) = 2, we define k(Ωm) = 3 (log3 − 1) . The following theorem has been proved for complete bases by Spira (71 a) and for the monotone basis by Wegener (83). Krapchenko (81) improved the constant factor of the upper bound for several bases.

 THEOREM 1.1 : Let f ∈ Bn and Ω ⊆ B2 complete, or f ∈ Mn and Ω= Ωm . Then

:
###### log(LΩ(f) + 1) ≤ DΩ(f) ≤ k(Ω) log(LΩ(f) + 1) (1.3)

 Proof : The first inequality is rather easy. Let S be a depth optimal circuit and let d = DΩ(f) . We find a formula F for f of depth d (see Ch. 1). F is a binary tree of depth d, hence the number of gates (inner nodes) of F is bounded by 2[d] − 1 . Hence LΩ(f) ≤ 2[d] − 1 .
 The second inequality is proved by induction on l = LΩ(f) . The

            ###### assertion is obvious for l 2, since k(Ω) 2 . Let l 3 and let F ≤ ≥ be an optimal formula for f . If the depth of F is too large, we shall rebuild F such that the depth decreases. During this procedure the size can increase exponentially. F is a binary tree. Let F1 and F2 be the right and left subtree of F computing f1 and f2 resp. The size of F1 or F2 is denoted by l 1 or l 2 resp. W.l.o.g. l 1 l 2 . Then ≤

; = ; = :
###### l 1 + l 2 = l − 1 0 ≤ l 1 ≤ (l − 1) 2 1 ≤ (l − 1) 2 ≤ l 2 ≤ l − 1 (1.4)
 We apply the induction hypothesis to F1, since this subtree is small enough. For F2 we have to work harder. Let F0 be the smallest subtree

=

###### of F2 with at least ⌈l 2 3⌉ gates. Both the right and the left subtree of

=

###### F0 have at most ⌈l 2 3⌉− 1 gates. Hence we can estimate l 0, the size
 of F0, by


= = :
###### 3⌉− 1) + 1 ≤ (2l 2 + 1) 3 (1.5)


###### 1 ≤⌈l 2


=
###### 3⌉≤ l 0 ≤ 2(⌈l 2


###### F0 is a subtree of F2 of medium size. Let f0 be the function computed by F0, and let f2;i for i ∈{0; 1} be the function computed by F2 if we replace the subformula F0 by the constant i . By definition


###### f2 = sel(f0


; f2;0


; f2;1): (1.6)


-----

**220**

###### If F2 is a monotone formula, f2;0 f2;1 and ≤


###### f2 = sel[′](f0


; f2;0


; f2;1): (1.7)


###### We compute f0 ; f2;0 and f2;1 in parallel and f2 by (1.6) or (1.7). In the
 following we identify sel and sel[′] . Then

 DΩ(f2) ≤ DΩ(sel) + max{DΩ(f0); DΩ(f2;0); DΩ(f2;1)} and (1.8)

; :
###### DΩ(f) ≤ 1 + max{DΩ(f1) DΩ(f2)} (1.9)


###### We apply the induction hypothesis to f0 ; f1 ; f2;0 and f2;1 . Because of
 (1.4), (1.5) and the definition of f2;0 and f2;1

= =
###### LΩ(f0) ≤ (2l 2 + 1) 3 ≤ (2l − 1) 3 and (1.10)


###### LΩ(f2;i) ≤ l 2 − l 0 ≤ 2l 2
 Hence


= = :
###### 3 (2l 1) 3 (1.11) ≤ −


= :
###### DΩ(f2) ≤ DΩ(sel) + k(Ω) log((2l − 1) 3 + 1) (1.12)

=
###### Since LΩ(f1) = l 1 ≤ (l − 1) 2, we obtain by induction hypothesis for DΩ(f1) a smaller upper bound than for DΩ(f2) in (1.12). Hence by definition of k(Ω)

=
###### DΩ(f) ≤ 1 + DΩ(sel) + k(Ω) log(2 3) + k(Ω) log(l + 1) (1.13)

:
###### = k(Ω) log(l + 1)

 2

 The lower bound is optimal, since D(f) = log n and L(f) = n 1 ⌈ ⌉ − for f(x) = x1 ∧· · · ∧ xn . We know that DΩ(f) ≤ c DΩ[′](f) for complete

;
###### bases Ωand Ω[′] and some constant c = c(Ω Ω[′]) . In connection with Theorem 1.1 we obtain

;
###### COROLLARY 1.1 : Let Ω Ω[′] ∈ B2 be complete bases. Then
 LΩ(f) ≤ (LΩ[′](f) + 1)[c k(Ω][′][)] − 1 for some constant c . (1.14)

 For complete bases Ωand Ω[′] the complexity measures LΩ and LΩ[′] are polynomially connected. Pratt (75 b) investigated more pre

-----

**221**

###### cisely the effect of a change of basis for complete bases Ω ⊆ B2 .

:
###### The exponent c k(Ω[′]) in (1.14) can be replaced by log3 10 ≈ 2 096 . This result is almost optimal, since L(x1 ⊕· · · ⊕ xn) = n − 1 and L ; ; (x1 xn) = Θ(n[2]) (see Ch. 8).
_{∧_ _∨_ _¬}_ _⊕· · · ⊕_

###### 7.2 Circuit size vs. formula size and depth

 We know hardly anything about the dependence of circuit size on depth. The best result is due to Paterson and Valiant (76).

 THEOREM 2.1 : log(C(f) + 1) D(f) = O(C(f) log[−][1] C(f)) . ≤

 The first inequality is obvious, since C(f) L(f), and optimal, ≤ since C(x1 ∧· · · ∧ xn) = n − 1 . The upper bound is not much better than the trivial bound D(f) C(f) . The largest known lower bound ≤ on the formula size (over a complete basis) of an explicitly defined function is of size n[2] (see Ch. 8). According to Theorem 1.1 we do not know any ω(log n) bound on the depth of explicitly defined functions. In particular, we cannot prove D(f) = ω(log C(f)) for some function f .

 Proof of Theorem 2.1 : The idea of the proof can be described rather easily. Its realization is technically involved. We partition a size optimal circuit for f into two parts of nearly the same size such that no path leads from the second part to the first one. If this partition cuts many edges, the circuit has large width, and it is sufficient to reduce the depth of both parts. If this partition cuts only a small number of m edges, the output f depends on the first part only via the

; : : : ;

###### functions g1 gm computed on these edges. Let fc(x) be the output

; : : : ; ;
###### if (g1(x) gm(x)) = c ∈{0 1}[m] .


###### � f(x) = (2.1)

c 0;1
_∈{_ _}[m][g][1][(x)][c(1)][ ∧· · · ∧]_ [g][m][(x)][c(m)][ ∧] [f][c][(x)]


-----

**222**

###### is the ˝disjunctive normal form of f with respect to the inputs

; : : : ; ; : : : ;

###### g1 gm ˝ . We compute g1 gm and all fc in parallel with small
 depth and compute f by (2.1). Since in this case m is small, we hope to obtain a circuit of small depth.

 We measure the size of a circuit S by the number E(S) of its edges starting in gates. Obviously E(S) 2 C(S) and E(f) 2 C(f) for the ≤ ≤ proper complexity measure E . Let

 D(z) = max D(f) E(f) z (2.2) { | ≤ }
 be the maximum depth of a function f whose size is bounded by z . We look for an upper bound on D . Let

:
###### A(d) = max z D(z) d (2.3) { | ≤ }
 Hence, by definition,

;
###### D(A(d)) d (2.4) ≤
 and A is almost the inverse of D . D is an increasing function, which can only increase slowly. Let D(f) = D(z) and let S be a circuit for f where E(S) z . If we replace the first gate of S by a new variable, ≤ we obtain a circuit S[′] for f[′] where E(S[′]) z 1 . Hence ≤ −

:
###### D(z 1) D(z) = D(f) D(f[′]) + 1 D(z 1) + 1 (2.5) − ≤ ≤ ≤ −

 After these definitions we explain in detail our ideas discussed above. We choose some function f where E(f) = A(r) + 1 and

  ###### D(f) r . Let S be a circuit for f where z := E(S) = E(f) and let

; : : : ;

###### G1 Gc be the gates of S . As indicated, we partition S into two

; : : : ; ; : : : ;

###### parts X = {G1 Gi} and Y = {Gi+1 Gc} . What is a good
 choice for i ? Let M X be the set of gates having a direct successor ⊆ in Y . Let m = M and let x and y be the number of edges between | | gates in X and Y resp. Then

;
###### x + y + m z (2.6) ≤
 since at least m edges connect a gate in X with a gate in Y . We investigate 2x+m z in dependence of i . If i = c, then x = z, m = 0, − and 2x+m z = z . If i = 0, then x = m = 0 and 2x+m z = z . If − − − we decrease i by 1, one gate G switches from X to Y, x decreases at most by 2 (the edges for the inputs of G), m decreases at most by 1 (the gate G) . Hence 2x + m z decreases at most by 5, and we can −


-----

**223**

###### choose some i such that

:
###### 2x + m z 2 (2.7) | − | ≤
 We claim that

; :
###### 2w + m z + 2 for w = max x y (2.8) ≤ { }
 (2.8) follows from (2.7) if w = x . By (2.6) and (2.7)

; :
###### x + y + m z 2x + m + 2 hence y x + 2 (2.9) ≤ ≤ ≤
 If w = y, 2w + m y + (x + 2) + m z + 2, and (2.8) holds. ≤ ≤
 On the one hand we can compute the functions computed at gates G M in depth D(x) and then f in depth D(y) . Hence ∈
 D(f) D(x) + D(y) 2D(w) and (2.10) ≤ ≤

=        - = :
###### D(w) D(f) 2 r 2 ≥ ⌊ ⌋
 On the other hand we can apply the representation of f in (2.1). All gi can be computed in parallel in depth D(x), their conjunction can be computed in depth log m . Parallel to this we can compute all ⌈ ⌉ fc in parallel in depth D(y) . Afterwards f can be computed in depth 1 + m . Hence by (2.8)

;
###### D(f) max D(x) + log m D(y) + 1 + m (2.11) ≤ { ⌈ ⌉ }

:
###### D(w) + log m + 1 + m D(w) 2w + z + 3 + log m ≤ ⌈ ⌉ ≤ − ⌈ ⌉

 The rest of the proof is a tedious computation. By (2.10) and the definition of A

= < :
###### A( r 2 ) w (2.12) ⌊ ⌋
 The function w D(w) 2w is strictly decreasing, since by (2.5) → −

< :
###### D(w) 2w D(w 1) + 1 2w D(w 1) 2(w 1) (2.13) − ≤ − − − − −
 We use (2.11) and estimate w by (2.12) and m by z (see (2.9)). Hence by the definition of f, (2.11), (2.4) and (2.5)

< = =
###### r D(f) D(A( r 2 ) + 1) 2 (A( r 2 ) + 1) + z + 3 + log z ≤ ⌊ ⌋ − ⌊ ⌋ ⌈ ⌉ (2.14)

= = :
###### r 2 + 1 2 A( r 2 ) + z + 1 + log z ≤⌊ ⌋ − ⌊ ⌋ ⌈ ⌉
 By definition z = A(r) + 1 . Hence by (2.14)


-----

**224**

= = < :
###### 2A( r 2 ) + r 2 2 z + log z = A(r) + 1 + log(A(r) + 1) ⌊ ⌋ ⌈ ⌉− ⌈ ⌉ ⌈ ⌉ (2.15)

 For a constant k 1 we define ≥

= :
###### H(r) = (r 2) logr + 2 log r kr (2.16) −
 By elementary transformations it can be shown that for sufficiently

       ###### large R, all k 1 and r R ≥

= =     - :
###### 2 H( r 2 ) + r 2 2 H(r) + 1 + log(H(r) + 1) (2.17) ⌊ ⌋ ⌈ ⌉− ⌈ ⌉
 We claim that A(r) H(r) for some appropriate k and all r . Parame- ≥

               ###### ter k is chosen such that A(r) H(r) for r R . If r R by (2.15), ≥ ≤ the induction hypothesis and (2.17)

         - = =
###### A(r) + 1 + log(A(r) + 1) 2 A( r 2 ) + r 2 2 (2.18) ⌈ ⌉ ⌊ ⌋ ⌈ ⌉−

= =       - ;
###### 2 H( r 2 ) + r 2 2 H(r) + 1 + log(H(r) + 1) ≥ ⌊ ⌋ ⌈ ⌉− ⌈ ⌉
 hence A(r) H(r) . ≥
 We summarize our results.

     - =
###### 2 C(f) E(f) A(r) H(r) (r 2) logr kr and (2.19) ≥ ≥ ≥ −

:
###### D(f) = D(z) D(z 1) + 1 = D(A(r)) + 1 r + 1 (2.20) ≤ − ≤

=
###### For sufficiently large r the function (r 2) logr kr is increasing. Hence −

          
###### for some appropriate constant k[′] 0

= =
###### C(f) (1 4)(D(f) 1) log(D(f) 1) (k 2) (D(f) 1) (2.21) ≥ − − − −

:
###### k[′] D(f) log D(f) ≥
 This implies D(f) = O(C(f) log[−][1] C(f)) . 2

 We add some remarks on the relations between circuit size and formula size. Obviously C(f) L(f), and this bound is optimal for ≤ x1 xn . By Theorem 1.1 and 2.1 we conclude that ∧· · · ∧

:
###### log L(f) = O(C(f) log[−][1] C(f)) (2.22)

 The largest differences known between L(f) and C(f) are proved in Ch. 8. For a storage access function f for indirect addresses C(f) = Θ(n) but L(f) = Ω(n[2] log[−][1] n) and for the parity function g and Ω=

; ;
###### {∧ ∨ ¬} CΩ(g) = Θ(n) but LΩ(f) = Θ(n[2]) .


-----

**225**

###### 7.3 Joint minimization of depth and circuit size, trade-offs

 A circuit is efficient if size and depth are small. For the existence of efficient circuits for f it is not sufficient that C(f) and D(f) are small. It might be possible that all circuits of small depth have large size and vice versa. In Ch. 3 we have designed circuits of small depth and size, the only exception is division. We do not know whether there is a division circuit of size O(n log[2] n log log n) and depth O(log n) . For the joint minimization of depth and circuit size we define a new complexity measure PCD (P = product).

 DEFINITION 3.1 : For f ∈ Bn and a basis Ω

 PCDΩ(f) = min{C(S) D(S) | S is an Ω-circuit for f} and (3.1)

:
###### PLDΩ(f) = min{L(S) D(S) | S is an Ω-formula for f} (3.2)

 Obviously CΩ(f) DΩ(f) ≤ PCDΩ(f) . For many functions we have proved that C(f) D(f) = Θ(PCD(f)), e.g. for addition both are of size n log n . Are there functions where PCD(f) is asymptoti- cally larger than C(f) D(f)? What is the smallest upper bound on

=
###### PCD(f) C(f) D(f)? All these problems are unsolved. We know that C(f) D(f) = Ω(n log n) for all f ∈ Bn depending essentially on n vari- ables. But we cannot prove for any explicitly defined function f ∈ Bn that all circuits of logarithmic depth have nonlinear size. In 4 we § present a function f where L(f) D(f) = o(PLD(f)) . This result is called a trade-off result. In general, trade-offs are results of the following type. We have two types of resources c1 and c2 for some problem P which we like to minimize simultaneously. But for each solution S where c1(S) is small c2(S) is not small and vice versa. Results of this type have been proved for several problems. We refer to Carlson and Savage (83) for the problem of optimal representations of trees and graphs and to Paterson and Hewitt (80) for the investigation of peb- ble games which are models for time - place trade-offs for sequential


-----

**226**

###### computations. For VLSI chips (see also Ch. 12, 2) one tries to min- § imize the area A of the chip and simultaneously the cycle length T . It has turned out that AT[2] is a suitable joint complexity measure. By information flow arguments one can prove for many problems, among them the multiplication of binary numbers, that AT[2] = Ω(n[2]) . Since for multiplication A = Ω(n) and T = Ω(log n) chips where AT[2] = O(n[2]) may exist only for Ω(log n) = T = O(n[1][=][2]) . Mehlhorn and Preparata (83) designed for this range of T VLSI chips optimal with respect to AT[2] . The user himself can decide whether A or T is more important to him. We are far away from similar results for circuit size and depth.

 7.4 A trade-off result

 Since no trade-off between circuit size and depth is known, we present a trade-off between formula size and depth. Although DΩ(f) = Θ(log LΩ(f)) for all f ∈ Bn, this result does not imply that PLDΩ(f) = Θ(LΩ(f)DΩ(f)) . On the contrary we present an example f where

; ;
###### LΩ(f)DΩ(f) = o(PLDΩ(f)) for Ω= Ωm and Ω= {∧ ∨ ¬} . Fur- thermore we get to know methods for such trade-offs.

 DEFINITION 4.1 : The carry function fn B2n is defined by ∈


###### fn(x1


; : : : ;
###### xn


;
###### y1


; : : : ; yn) = � xi yi yn

###### · · ·
1 i n
_≤_ _≤_


:
###### (4.1)


###### This function is important for the addition of binary numbers a

;
###### and b . Let xi = ai bi and yi = ai bi . Then fn(x y) is the fore- ∧ ⊕ most carry (see Ch. 3, (1.8)). Hence by the results of Ch. 3, 1 § CΩ(fn) = Θ(n), DΩ(fn) = Θ(log n) and PCDΩ(fn) = Θ(n log n) for

; ; ; ;

###### Ω ∈{B2 {∧ ∨ ¬} Ωm}, and there is no trade-off. But here we inves tigate formula size and depth.


-----

**227**

###### THEOREM 4.1 : i) There is a monotone formula for fn of size O(n) and depth O(n) .
 ii) There is a monotone formula for fn of size O(n log n) and depth O(log n) .

; ; ; ;

###### iii) PLDΩ(fn) = O(n log[2] n) for Ω ∈{Ωm {∧ ∨ ¬} B2} .


###### iv) LΩ(fn) = Θ(n) for Ω ∈{Ωm


; ; ; ;
###### {∧ ∨ ¬} B2} .


###### v) DΩ(fn) = Θ(log n) for Ω ∈{Ωm


; ; ; ;
###### {∧ ∨ ¬} B2} .


###### Proof : iii), iv) and v) follow from i) and ii). i) follows from the Horner scheme

; :
###### fn(x y) = yn (xn (yn 1 (y1 x1) )) (4.2) ∧ ∨ − ∧· · · ∧ · · ·

 The second assertion can be proved by a recursive approach. Here and in the rest of this chapter we do not count the gates of a formula but the leaves of the proper binary tree which is by 1 larger than the real

; ;

###### formula size. W.l.o.g. n = 2[k] . We divide x = (x[′] x[′′]) and y = (y[′] y[′′])
 in two parts of the same length. Then


###### fn(x; y) = (fn=2(x[′]

 For this formula Fn


; y[′]) ∧ yn=2+1 ∧· · · ∧ yn) ∨ fn=2(x[′′]


; :
###### y[′′]) (4.3)


###### L(Fn) = 2 L(Fn=2) + n=2; L(F1) = 2; hence (4.4)

= ;
###### L(Fn) = (1 2) n logn + 2 n

 D(Fn) = max{D(Fn=2); log(n=2)} + 2; D(F1) = 1; (4.5)

 hence

:
###### D(Fn) = 2 log n + 1 2

 The following trade-offs have been proved by Commentz-Wal- ter (79) for the monotone basis and by Commentz-Walter and Satt
; ;
###### ler (80) for the basis . {∧ ∨ ¬}

 1 THEOREM 4.2 : PLDm(fn) ≥
 128 [n log][2][ n .]


-----

**228**

###### THEOREM 4.3 : PLD{∧;∨;¬}(fn) ≥ 8 [1] [n log n log logn(log log log logn)][−][1]

 Actually these are only asymptotic results. Obviously, for both

; ;
###### bases Ω= Ωm and Ω= {∧ ∨ ¬}, LΩ(fn) ≥ 2 n and DΩ(fn) ≥ log(2n), hence PLDΩ(fn) ≥ 2 n log(2n) . The lower bound of Theorem 4.2 is not better than this simple bound if n 2[256], and the bound of ≤ Theorem 4.3 does not beat the simple bound if n 2[2][38] . ≤
 Before we discuss the essential ideas of the proof of Theorem 4.2 we anticipate some technical lemmas. The proof of Theorem 4.3 is based on the same ideas but is technically even more involved and therefore omitted.


; : : : ;
###### LEMMA 4.1 : If we replace for j ̸∈ J ⊆{1 n} xj by 0 and yj by 1 we obtain the subfunction fm, where m = |J|, on the set of variables

;

###### {xj yj | j ∈ J} .

 Proof : Obvious. 2

 LEMMA 4.2 : If we replace x1 and yn by 1 we obtain

; : : : ; ; ; : : : ;

###### fn[d]−1[(y][1] yn−1 x2 xn) where fn[d]−1 [is the dual function of f][n][−][1] [.]


###### Proof : We apply the rules of deMorgan and the law of distributivity.


###### fn[d] 1[(y][1]
_−_


; : : : ;
###### yn 1
_−_


; ; : : : ;
###### x2 xn) = ¬fn−1(y1


; : : : ;
###### yn 1
_−_


;
###### x2


; : : : ;
###### xn) (4.6)


###### � � � � = ¬ yi xi+1 · · · xn = ¬ ¬ (yi ∨ xi+1 · · · ∨ xn)

1 i n 1 1 i n 1
_≤_ _≤_ _−_ _≤_ _≤_ _−_

###### = xn ∨ xn−1 yn−1 ∨ xn−2 yn−2 yn−1 ∨· · · ∨ x2 y2 · · · yn−1 ∨ y1 · · · yn−1


;
###### = fn(1 x2


; : : : ; ;
###### xn y1


; : : : ;
###### yn 1
_−_


; :
###### 1) 2


d 1+s 1 d 1+s d+s
###### � − − � � − � � � LEMMA 4.3 : + if s 1 .
d−1 d−1 _≤_ d _≥_

###### Proof : Elementary. 2


-----

**229**

###### �d+s� LEMMA 4.4 : Let m(p) = max ds p . Then { d | ≤ } log m(p) 2 p[1][=][2] . ≤

 Proof : By Stirling’s formula we can approximate n! by (2π)[1][=][2] n[n+1][=][2] e[−][n], more precisely, the quotient of n! and its approxi
;
###### mation is in the interval [1 e[1][=][(11n)]] . Hence


###### �d + s� 1 �d + s log
 ≤
 d 11(d + s) [log e][ −] [1]2 [log(2][π][) + 1]2 [log] ds


###### � (4.7)


###### + (d + s) log(d + s) d log d s log s − −

 d log(d + s) d log d + s log(d + s) s log s ≤ − −


###### � d d s s = (d + s) −
 d + s [log] d + s d + s [log] d + s

 [−]
 � d s �

;

###### = (d + s) H
 d + s d + s


###### �


###### where

;
###### H(x 1 x) = x log x (1 x) log(1 x) (4.8) − − − − −

 is the entropy function. W.l.o.g. d s . Since ≤

; = ;
###### H(x 1 x) 2x log x for x 1 2 (4.9) − ≤− ≤


###### �d + s� �d + s log 2 d log
 ≤
 d d


###### � � = 2 d log 1 + [s]
 d


###### �


:
###### (4.10)


###### We only investigate numbers d and s where ds p and d s, hence ≤ ≤

= = =
###### d[2] p and α := p d[2] 1 . Furthermore d = (p α)[1][=][2] and s d = ≤ ≥

= =
###### sd d[2] p d[2] = α . Hence ≤


###### � p log m(p) max 2 ≤ {
 α


###### �1=2

:
###### log(1 + α) α 1 (4.11) | ≥ }


###### Let g(α) = α[−][1][=][2] log(1 + α) . Then g(1) = 1 and g is decreasing for α 1 . Hence the maximum in (4.11) is 2 p[1][=][2] . 2 ≥


-----

**230**

###### Now we begin with the proof of Theorem 4.2. Instead of designing a formula for fn of minimal complexity with respect to PLDm we choose

;
###### another way. For given d and s we look for the maximal n =: t(d s) such that there is a monotone formula Fn for fn where D(Fn) ≤ d

= ;
###### and L(Fn) n ≤ s . Upper bounds on t(d s) imply lower bounds on PLDm(fn) . The main result is the following lemma.

      - ;      - ;
###### LEMMA 4.5 : d 0 s 1 : log t(d s) 8 (d s)[1][=][2] . ∀ ≤

 We prove at first, how this lemma implies the theorem.

 Proof of Theorem 4.2 : Let Fn be an optimal formula for fn with

<
###### respect to PLDm . Let d = D(Fn) and s be chosen such that s − 1

= ;
###### L(Fn) n ≤ s . Obviously s ≥ 2 . By definition n ≤ t(d s) and by Lemma 4.5
 PLDm(fn) = L(Fn)D(Fn) ≥ n(s − 1)d ≥ [1] (4.12)
 2 [n s d]
 1 1 ≥
 128 [n log][2][ t(d][;][ s)][ ≥] 128 [n log][2][ n][:]


###### 2

;
###### It is easier to work with t(d s) than with PLDm . The main reason is that depth and formula size are both bounded independently. s is a bound for the average number of leaves of the formula labelled by xi or yi . It would be more convenient to have bounds on the number of xi- and yj-leaves (for fixed i and j) and not only on the average number.

;
###### Let t[′](d s) be the maximal n such that there is a monotone formula

; ; : : : ;
###### Fn for fn such that D(Fn) ≤ d and for i j ∈{1 n} the number of

; ;
###### xi- and yj-leaves is bounded by s . Obviously t[′](d s) ≤ t(d s) . We

; ;
###### prove an upper bound on t(d s) depending on t[′](d s), and afterwards

;
###### we estimate the more manageable measure t[′](d s) .

; ;
###### LEMMA 4.6 : t(d s) 3 t[′](d 6s) . ≤


-----

**231**

;
###### Proof : Let Fn be a monotone formula for fn where n = t(d s), D(Fn) ≤ d and L(Fn) ≤ s n . Let I be the set of all i such that the number of xi-leaves in Fn is bounded by 3 s . Since L(Fn) ≤ s n,

=
###### I (2 3) n . Let J be the corresponding set for the y-variables. Then | | ≥

= =
###### |J| ≥ (2 3) n and |H| ≥ (1 3) n for H = I ∩ J . For i ̸∈ H we replace xi by 0 and yi by 1 . By Lemma 4.1 we obtain a formula F[′] for f|H| where D(F[′]) d, and each variable is the label of at most 3 s leaves. Hence ≤

; ; :
###### t(d s) = n 3 H 3 t[′](d 6s) (4.13) ≤ | | ≤

 2

; �d+s�
###### LEMMA 4.7 : t[′](d s) 1 . ≤ d −

 This lemma is the main step of the proof. Again we first show that this lemma implies the theorem.

;
###### Proof of Lemma 4.5 : By Lemma 4.7 t[′](d s) is bounded by m(ds) for the function m of Lemma 4.4. Hence

; ;
###### log t(d s) log t[′](d 6s) + log 3 2 (6 ds)[1][=][2] + log 3 (4.14) ≤ ≤


###### 8 (ds)[1][=][2] ≤


:


###### 2

 For the proof of Lemma 4.7 we investigate the last gate of monotone formulas for fn . If this gate is an ∧-gate we apply Lemma 4.2 and investigate the corresponding dual formula whose last gate is an - ∨ gate. If fn = g1 ∨g2, we find by the following lemma large subfunctions of fn in g1 and g2 .

; : : : ;
###### LEMMA 4.8 : If fn = g1 ∨ g2, there is a partition of {1 n} to I and J such that we may replace the variables xi and yi for i ̸∈ I (i ̸∈ J) by constants in order to obtain the subfunction f|I| (f|J|). Furthermore g1 or g2 depends essentially on all y-variables.


-----

**232**

###### Proof : Since x1 y1 · · · yn ∈ PI(fn) ⊆ PI(g1) ∪ PI(g2), x1 y1 · · · yn is a prime implicant of gj for j = 1 or j = 2, in particular gj depends essentially on all y-variables.

: : :

###### pi = xi yi yn (1 ≤ i ≤ n) are the prime implicants of fn . Let I

; : : : ;
###### be the set of all i where pi ∈ PI(g1) and J = {1 n} − I . Then pj ∈ PI(g2) for j ∈ J . We set xk = 0 and yk = 1 for k ̸∈ I . Each prime implicant of g1 equals some pi (i ∈ I) or is a lengthening of some pk (k ̸∈ I). These pk are replaced by 0, since xk = 0 . In pi (i ∈ I) the y-variables yk (k ̸∈ I) are replaced by 1 . Altogether g1 is replaced by f|I| . The same arguments work for g2 . 2

 Finally we finish the proof of Theorem 4.2 by the proof of Lemma 4.7.

 Proof of Lemma 4.7 : Induction on d . The assertion is trivial if d = 0

;                -                ###### or s 1, since t[′](d s) = 0 . Let d 0 and s 1 and let us assume ≤

<

###### that the assertion holds for all d[′] d . Let F be a monotone formula

; ; ; : : : ;
###### for fn where n = t[′](d s), D(F) ≤ d, and for all i j ∈{1 n} the number of xi- and yj-leaves is bounded by s .

 Case 1 : The last gate of F is an -gate. ∨
 Let g1 and g2 be the inputs of the last gate, hence fn = g1 g2 . By ∨ Lemma 4.8 we assume w.l.o.g. that g1 depends essentially on all y
; : : : ;
###### variables. Let I and J form the partition of 1 n whose existence { } also has been proved in Lemma 4.8. The depth of the formulas for

; ; : : : ;
###### g1 and g2 is bounded by d − 1 . For all i j ∈{1 n} the number of xi- and yj-leaves in the formula for g2 is bounded by s − 1, since the formula for g1 includes at least one yj-leaf. Hence |I| + |J| = n,

; ;
###### I t[′](d 1 s) and J t[′](d 1 s 1) and by Lemma 4.3 and the | | ≤ − | | ≤ − − induction hypothesis

; ; ;
###### t[′](d s) = n I + J + 1 t[′](d 1 s) + t[′](d 1 s 1) + 1 ≤| | | | ≤ − − − (4.15)


-----

**233**


###### �d 1 + s� �d 1 + s 1� �d + s� − − − :
 1 + 1 + 1 1
 ≤ − − ≤ − d 1 d 1 d − −

 Case 2 : The last gate of F is an -gate. ∧
 Let x1 = 1 and yn = 1 . Then fn is replaced by fn[d]−1 [. If we replace] -gates by -gates and vice versa, we obtain a monotone formula for ∧ ∨ fn−1 whose last gate is an ∨-gate. Similarly to Case 1 we can prove

; ;
###### that I t[′](d 1 s) and J t[′](d 1 s 1) for some partition I and | | ≤ − | | ≤ − −

; : : : ;
###### J of 1 n 1 . Here I + J = n 1 . (4.15) works also in this { − } | | | | − situation. 2

 As already acknowledged we do not know much about trade-offs between formula size or circuit size and depth.

 EXERCISES

 1. Generalize Spira’s theorem to complete bases Ω ⊆ Br .

 2. Compute CΩ(sel) and DΩ(sel) for different bases Ω ⊆ B2, in par
;
###### ticular Ω= NAND and Ω= . { } {⊕ ∧}

 3. Let F be a formula of size l and let F[′] be the equivalent formula constructed in the proof of Spira’s theorem. Estimate the size of F[′] .

 4. Which functions are candidates for the relation D(f) = ω(log C(f)) ?

 5. Let n = 2[m] and let f be the Boolean matrix product of n n- × matrices. What is the minimal size of a monotone circuit for f whose depth is bounded by m + 1 ?


-----

**234**

###### 6. Generalize the result of Exercise 5 to B2-circuits.

; : : : ;

###### 7. Let f = (f0 f2n 2) be the Boolean convolution and n = 2[m] .

_−_
###### Let gi = fi ∨ fi+n for 0 ≤ i ≤ n − 2 and gn−1 = fn−1 . Solve the

; : : : ;

###### problems of Exercise 5 and 6 for g0 gn−1 .


-----

**235**

###### 8. FORMULA SIZE

 The depth of a circuit corresponds to the parallel computation time. Since D(f) = Θ(log L(f)) (Theorem of Spira, see Ch. 7, 1), § the study of the formula size of Boolean functions is well motivated.

 The formula size of f is equal to the minimal number of gates in a formula for f . The number of gates or inner nodes of a binary tree is by 1 less than the number of leaves of the tree. Often it is easier to deal with the number of leaves, e.g. the number of leaves of a binary tree is equal to the sum of the number of leaves in the left subtree and the number of leaves in the right subtree. Hence we denote the formula size of f by L[∗](f) and we define L(f) = L[∗](f) + 1 . It causes no problems to call L also formula size.

 Because of their central role, we investigate threshold functions in 1 – 3 and symmetric functions in 4. In 5 – 8 we present and § § § § § apply some methods for the proof of lower bounds on the formula size of explicitly defined functions.

 8.1 Threshold - 2

 We know that the (monotone) circuit complexity of T[n]k [is linear for] fixed k (see Ch. 6, 2). The monotone formula size is superlinear, it § is of size n log n .

 THEOREM 1.1 : Lm(T[n]2[) = O(n log n) . If n = 2][k][, L][m][(T][n]2[)][ ≤] [n log n .]


###### Proof : W.l.o.g. n = 2[k] . Otherwise we add some 0-inputs. Let

; =

###### x = (x[′] x[′′]) where x[′] and x[′′] consist of n 2 variables each. Obviously

 � � T[n]2[(x) =] T1[n][=][2][(x][′][)][ ∧] [T]1[n][=][2][(x][′′][)] ∨ T2[n][=][2][(x][′][)][ ∨] [T]2[n][=][2][(x][′′][)][:] (1.1)


-----

**236**

###### Since Lm(T[n]1[) = n, we conclude that]
 Lm(T[n]2[)][ ≤] [n + 2 L][m][(T]2[n][=][2][)] and Lm(T[2]2[) = 2][:] (1.2)

 Hence Lm(T[n]2[)][ ≤] [n log n .] 2

 This simple approach is optimal if n = 2[k] . We prove this claim for

; ;
###### the monotone basis (Hansel (64)). For the complete basis {∧ ∨ ¬} we refer to Krichevskii (64). We investigate the structure of monotone formulas for T[n]2 [and prove the existence of an optimal monotone single-] level formula.

 DEFINITION 1.1 : A monotone formula or circuit is a single-level formula or circuit if no directed path combines -gates. ∧

 It is reasonable to conjecture that all quadratic functions (all prime implicants are monotone and have length 2) have optimal single-level formulas and circuits. This claim is open for circuits and has been disproved for formulas (see Exercises).

 LEMMA 1.1 : There is an optimal monotone formula for T[n]2 [which] is a single-level formula.

 Proof : Let F be an optimal monotone formula for T[n]2 [. We reconstruct] F until we obtain a single-level formula F[′] for T[n]2 [of the same size as F .] If F is not a single-level formula, let G be the first -gate of F which ∧ has some ∧-gate as (not necessarily direct) predecessor. Let g = resG and let g1 and g2 be the inputs of G . Then g1 and g2 are computed by single-level formulas. Hence g1 = t1 u1 up where t1 is a ∨ ∨· · · ∨ Boolean sum and all uj are computed at ∧-gates Hj . Let uj1 and uj2 be the inputs of Hj . Then uj = uj1 uj2 and uj1 and uj2 are Boolean ∧ sums. If uj1 and uj2 contain the same variable xi, the subformula for uj is not optimal. We may replace xi in uj1 and in uj2 by 0 . Then uj is replaced by u[′]j [where u][j][ = u]j[′]
 [∨] [x][i][ . Instead of two x][i][-leaves one x][i][-leaf]


-----

**237**

###### suffices. Hence uj1 and uj2 have no common variable and all prime implicants have length 2 . Similarly g2 = t2 w1 wq . ∨ ∨· · · ∨
 We rearrange the ∨-gates in the formulas for g1 and g2, such that

; ;

###### t1 t2 u = u1 up, and w = w1 wq are computed. Then
 ∨· · · ∨ ∨· · · ∨ g1 = t1 u, g2 = t2 w and ∨ ∨

:
###### g = g1 g2 = t1 t2 ∨ t1w ∨ t2u ∨ u w (1.3)

 We replace the subformula for g by a subformula for

 g[′] = t1 t2 ∨ u ∨ w (1.4)

 of the same size. Let f be the function computed by the new formula. T[n]2 2[(a) = 0 but f][′][(a) = 1]
 [≤] [f][′][, since g][ ≤] [g][′][ . Let us assume, that T][n] for some input a . Then g(a) = 0 and g[′](a) = 1 . This is only possible if u(a) = 1 or w(a) = 1 . But u and w have only prime implicants of length 2, hence T[n]2[(a) = 1 in contradiction to the assumption. The] new formula is an optimal monotone formula for T[n]2 [. We continue in] the same way until we obtain a single-level formula. 2

 THEOREM 1.2 : Lm(T[n]2[)][ ≥] [n log n .]

 Proof : We investigate an optimal monotone formula F for T[n]2 [.] W.l.o.g. (see Lemma 1.1) we assume that F is a single-level formula.

; : : : ;

###### Let G1 Gp be the ∧-gates where ui = ui1 ∧ui2 (1 ≤ i ≤ p) are com
; : : : ;
###### puted. ui1 and ui2 are disjoint Boolean sums. For (j(1) j(p)) ∈ {1; 2}[p] we replace all variables in u1;j(1) ; : : : ; up;j(p) by 0 . Since the
 output of F is 0 we have replaced at least n − 1 variables by 0 . If xi

; : : : ;
###### is not replaced by 0, (j(1) j(p)) is an element of Mi . If all vari
; : : : ;
###### ables are replaced by 0, (j(1) j(p)) is an element of M0 . Hence

; ; : : : ; ;

###### M0 M1 Mn build a partition of {1 2}[p] .
 Let (j(1); : : : ; j(p)) ∈ Mm and m ≥ 1 . If xm is a summand of ui;1 (or ui;2), then j(i) = 2 (or j(i) = 1). If xm is neither a summand of ui;1 nor of ui;2, j(i) may be 1 or 2 . Let p(m) be the number of indices i such that ui does not depend on xm . Then |Mm| = 2[p(m)] and p − p(m) is the number of xm-leaves. Hence


-----

**238**


###### � � Lm(T[n]2[) =] (p − p(m)) = n p − log |Mm| (1.5)

1 m n 1 m n
_≤_ _≤_ _≤_ _≤_


###### �� = n p − n log |Mm|[1][=][n][�]

1 m n
_≤_ _≤_


:


###### We apply the well-known inequality between the arithmetic and the geometric mean :


= �� �1=n
###### (1 n) [�] ai ≥ ai

1 i n 1 i n
_≤_ _≤_ _≤_ _≤_


:
###### (1.6)


###### Since the sets M1


; : : : ;
###### Mn are disjoint, |M1| + · · · + |Mn| ≤ 2[p] . Hence


###### � = � Lm(T[n]2[)][ ≥] [n p][ −] [n log] (1 n) |Mm| (1.7)
 [�]

1 m n
_≤_ _≤_

= :
###### n p n log(1 n) n log 2[p] = n log n ≥ − −


###### 2

< <
###### COROLLARY 1.1 : Lm(T[n]k[) = Ω(n log n) if 1] k n .

=
###### Proof : For k ≤⌈n 2⌉ we use the fact that T[n]2[−][k+2] is a subfunction

    - =
###### of T[n]k [. For k] ⌈n 2⌉ we apply the duality principle, which implies Lm(T[n]k[) = L][m][(T][n]n+1 k[) .] 2
_−_

###### In 2 we prove that this bound is asymptotically optimal if k or §

=
###### n k is constant. For k = n 2 we prove better lower bounds in 8 − §

; ;
###### (for the basis ). {∧ ∨ ¬}


-----

**239**

###### 8.2 Design of efficient formulas for threshold - k

 It is quite easy to design an optimal monotone formula for T[n]2 [but it]

               ###### is much harder to design optimal formulas for T[n]k [, if k] 2 is constant. The reader is asked to design a formula of size o(n log[2] n) for T[n]3 [. The] methods of 1 lead to the recursive approach §


###### � T[n]k[(x) =] Tp[n][=][2][(x][′][)][ ∧] [T]k[n]−[=][2]p[(x][′′][)][:] (2.1)

0 p k
_≤_ _≤_

###### These formulas for T[n]k [have size O(n(log n)][k][−][1][) (Korobkov (56)] and Exercises). Khasin (69) constructed formulas of size

=

###### O(n(log n)[k][−][1] (log log n)[k][−][2]), Kleiman and Pippenger (78) improved

log[∗] n
###### �k� the upper bound to O( n log n) and Friedman (84) designed
2
###### asymptotically optimal formulas of size O(n log n) . All these bounds are proved constructively, i.e. there is an algorithm which constructs for given n formulas of the announced size for T[n]k [and the running time] of the algorithm is a polynomial p(n) .
 Much earlier Khasin (70) proved that Lm(T[n]k[) = O(n log n), but his] proof is not constructive. We only discuss the main ideas of Khasin’s paper. T[n]k [is the disjunction of all monotone monoms of length k . It] is easy to compute many of these prime implicants by a small formula.

; : : : ; ; : : : ;
###### W.l.o.g. n = mk . Let A(1) A(k) be a partition of 1 n into { } k blocks of size m each. Then for each permutation π ∈ Σn


###### � fπ(x) =

1 j k
_≤_ _≤_


###### �
 xπ(i) (2.2)
i A(j)
_∈_


###### is a formula of size n and fπ is the disjunction of many, exactly m[k], prime implicants of length k each. We hope that T[n]k [is the disjunction] of a small number of functions fπ . Which permutations should be chosen ? Since Khasin could not solve this problem, he computed the mean number of missing prime implicants if one chooses randomly O(log n) permutations π . This number is O(n log n) . So there is a good choice of O(log n) permutations π such that T[n]k [is the disjunction] of O(log n) formulas fπ of size n each and O(n log n) prime implicants


-----

**240**

###### of length k each. Hence the size of the formula for T[n]k [is O(n log n) .]

 We present the constructive solution due to Friedman (84). We obtain a formula of size c n log n for a quite large c . It is possible to reduce c by more complicated considerations. We again consider

; : : : ;
###### functions f as described in (2.2). If A(1) A(k) is an arbitrary

; : : : ; : : :
###### partition of {1 n}, f has formula size n and f ≤ T[n]k [. x][i(1)] xi(k) ∈

; : : : ;

###### PI(f) iff the variables xi(1) xi(k) are in different sets of the partition.
 Hence we are looking for sets Am;j (1 ≤ m ≤ k, 1 ≤ j ≤ r) with the following properties


###### – A1;j


; : : : ; Ak;j are disjoint subsets of {1; : : : ; n} for each j,


; : : : ; ; : : : ;
###### – for different i(1) i(k) 1 n we find some j such that ∈{ } each Am;j contains exactly one of the elements i(1); : : : ; i(k) .

 Then


###### � T[n]k [= F][1] [∨· · · ∨] [F][r] where Fj =

1 m k
_≤_ _≤_


###### �
 xi
i∈Am;j


:
###### (2.3)


###### The first property ensures that all prime implicants have length k . The second property ensures that each monom of length k is a prime implicant of some Fj . A class of sets Am;j with these properties is called

;
###### an (n k)-scheme of size r . The size of the corresponding formula is r n .

 We explain the new ideas for k = 2 . W.l.o.g. n = 2[r] . Let posj(l )

; : : : ;
###### be the j -th bit of the binary representation of l 1 2[r] where ∈{ } 1 j r . The sets ≤ ≤

 Am;j = {l | posj(l ) = m} for 0 ≤ m ≤ 1 and 1 ≤ j ≤ r (2.4)

;
###### build an (n 2)-scheme of size r = log n . This simple construction

; ; : : : ;
###### is successful since for different l l [′] 1 2[r] we find a position j ∈{ } where posj(l ) ̸= posj(l [′]) .

 If k = 3, we could try to work with the ternary representation of

; ;
###### numbers. In general we cannot find for different numbers l l [′] l [′′]
 ∈

; : : : ;
###### {1 n} a position j such that posj(l ), posj(l [′]) and posj(l [′′]) (ternary


-----

**241**

; ;
###### representation) are different. For example : 1 (0 1), 2 (0 2), → →

;
###### 4 (1 1) . Instead of that we work with b-ary numbers for some large →

; : : : ;
###### but constant b . We look for a large set S 1 b such that two ⊆{ }[r]

= ; ;
###### vectors in S agree at less than (1 3) m positions. Let l l [′] l [′′] S be
 ∈ different. We label all positions where at least two of these vectors

=
###### agree. Altogether we label less than 3 (1 3) m = m positions, since �3� ; ; there are 3 = different pairs of vectors. The vectors l l [′] l [′′] differ
2

###### at all positions which are not labelled. Let


###### Am; (j; t(1) ; t(2) ; t(3)) = {s ∈ S | posj(s) = t(m)} (2.5)

< <
###### for 1 m 3, 1 j r, 1 t(1) t(2) t(3) b . ≤ ≤ ≤ ≤ ≤ ≤

 If we fix T = (j; t(1); t(2); t(3)), the sets A1;T ; A2;T and A3;T are

; ;

###### disjoint. Let s1 s2 s3 ∈ S be different. Then there is some j, an

;
###### unlabelled position, such that posj(s1) posj(s2) and posj(s3) are dif
< <
###### ferent. Let t(1) t(2) t(3) be the ordered sequence of posj(si) (1 ≤ i ≤ 3). Then s1 ; s2 ; s3 are in different sets A1;T ; A2;T and A3;T for

; ; ; ;
###### T = (j t(1) t(2) t(3)) . Hence we have constructed a ( S 3)-scheme | | �b� of size r . Since b is constant, r should be of size O(log S ) .
3 _|_ _|_


###### The same idea works for arbitrary k . For some constant b we look

; : : : ;
###### for a large set S 1 b such that two vectors in S agree at less ⊆{ }[r]
= �k� ; : : : ;
###### than r 2 positions. Let s1 sk be different elements of S . For
 �k� =�k� each of the pairs of vectors there are less than r positions where
2 2

; : : : ;

###### these vectors agree. Hence there is some position j = j(s1 sk)
 where all vectors differ. By

 Am; (j; t(1) ; ::: ; t(k)) [=][ {][s][ ∈] [S][ |][ pos]j[(s) = t(m)][}] (2.6)

< <
###### for 1 m k, 1 j r, 1 t(1) t(k) b ≤ ≤ ≤ ≤ ≤ · · · ≤

; �b�
###### we obtain a ( S k)-scheme of size r . If it is possible to choose | | k S in such a way that r = O(log S ) we are done. We then choose | |

; : : : ;
###### r large enough that S n . Afterwards we identify 1 n with | | ≥ different elements of S . By (2.3) we obtain a formula for T[n]k [of size] �b� r n = O(n log n) .
k


-----

**242**


###### For the construction we apply a greedy algorithm.

 �k� LEMMA 2.1 : Let l =, b = 2[2][l], c = 2 l and r = c r[′] for some r[′] .
2

; : : : ;
###### Then there is an algorithm which constructs some set S 1 b ⊆{ }[r]

= �k�
###### of size b[r][′] such that two vectors in S agree at less than r positions.
2
###### The running time of the algorithm is a polynomial p(b[r][′]) .

 Before we prove this lemma we show that it implies the main result of this section.

 THEOREM 2.1 : For constant k monotone formulas for T[n]k [of size] O(n log n) can be constructed in polynomial time.

 Proof : We apply the algorithm of Lemma 2.1 for the smallest r[′]

; �b�
###### such that b[r][′] n and obtain an (n k)-scheme of size r n . Since ≥ k r[′] = O(log n), also r = O(log n) and the formula has size O(n log n) . 2


###### Proof of Lemma 2.1 : We consider an r-dimensional array for the

; : : : ;
###### elements of 1 b . If we choose some vector s as an element of S, { }[r]

=
###### all vectors which differ from s in at most R = (1 (1 l )) r positions are − forbidden as further vectors in S . The number of forbidden vectors � r � � r � < is at most b[R] . We use the rough estimate 2[r] . Hence the
R R

###### number of forbidden vectors is bounded by

 b[r log][b][ 2+R] where (2.7)

= =
###### r logb 2 + R = r (logb 2 + 1 − (1 l )) = r (1 − (1 2l ))
 (2.8)

= :
###### = r (1 (1 c)) = r r[′] − −


=
###### Here we used the fact that logb 2 = 1 (2l ) . The greedy algorithm

; : : : ;
###### works as follows. Choose s1 ∈{1 b}[r] arbitrary. Label all forbid
; : : : ; ; : : : ;

###### den vectors. If s1 si−1 are chosen, choose si ∈{1 b}[r] as an


-----

**243**

###### arbitrary non-forbidden vector and label all vectors forbidden by si .

; : : : ;

###### If i ≤ b[r][′], the number of vectors forbidden by s1 si−1 is bounded

<

###### by (i − 1)b[r][−][r][′] b[r] and si can be chosen. Hence the algorithm works.
 The running time is bounded by a polynomial p(b[r]) and hence by a polynomial q(b[r][′]) . 2


###### 8.3 Efficient formulas for all threshold functions

 It is a hard struggle to design asymptotically optimal (monotone) formulas for T[n]k [and constant k . The design of a polynomial formula] �n� is easy, since we can take the MDNF which consists of prime
k
###### �n� implicants. In general k is not polynomially bounded. Since T[n]k [is a] subfunction of T[2n]n [, we consider only the majority function T]m[n] [where] n = 2m .

; ;
###### Since some time -formulas of size O(n[3][:][37]) are known. We {∧ ∨ ¬} are more interested in the monotone formula size of the threshold functions. Polynomial monotone formulas for all threshold functions imply (see Ch. 6, 13 – 15) that the monotone formula size of slice § § functions is only by polynomial factors larger than the formula size

; ;
###### over the basis and also over all complete bases (see Ch. 7, {∧ ∨ ¬} 1). By Theorem 1.1 in Ch. 7 the monotone depth of slice functions § is then of the same size as the depth of these functions.

 The sorting network of Ajtai et al. (83) has depth O(log n) . Hence the monotone formula size of all threshold functions is polynomially bounded. The degree of this polynomial is very large (see Ch. 6, 2). § We prove non constructively the existence of monotone formulas for the majority function of size O(n[5][:][3]) (Valiant (84)).

 We consider random formulas of different levels. For some p chosen later a random formula of level 0 equals xj (1 ≤ j ≤ n) with probabil- ity p and equals 0 with probability 1 − np . A random formula Fi of level i equals


-----

**244**


###### Fi = (G1 ∨ G2) ∧ (G3 ∨ G4) (3.1)

; : : : ;

###### where G1 G4 are independently chosen random formulas of level
 i − 1 . The size of Fi is bounded by 4[i] = 2[2i] . If the probability that Fi = Tm[n] [is positive, then there is some monotone formula of size 2][2i][ for] T[n]m [. Why do we hope that F][i][ sometimes equals T]m[n] [? In G][1][ ∨] [G][2][ and] G3 G4 prime implicants are shortened but are lengthened again by ∨ the following conjunction. Furthermore the experiment is symmetric with respect to all variables.

;
###### It is sufficient to prove that for all a 0 1 ∈{ }[n]


###### � � Prob Fi(a) ̸= T[n]m[(a)]

 This implies


<
###### 2[−][n][−][1]


:
###### (3.2)


###### � � � � � Prob Fi ̸≡ T[n]m ≤ Fi(a) ̸= T[n]m[(a)] ≤ (3.3)

a 0;1
_∈{_ _}[n][ Prob]_


###### Hence

 Lm(T[n]m[)][ ≤] [2][2i]

 Let


= :
###### 2[n] 2[−][n][−][1] = 1 2 ≤

:
###### (3.4)


###### � � fi = max Prob(Fi(a) = 1) | T[n]m[(a) = 0] and (3.5)

 � �: hi = max Prob(Fi(a) = 0) | T[n]m[(a) = 1]

 LEMMA 3.1 : fi = fi[4]−1 [−] [4f]i[3]−1 [+ 4f]i[2]−1 and hi = −h[4]i−1 [+ 2h]i[2]−1 [.]

 Proof : Because of the monotonicity of Fi and its symmetry with respect to all variables Fi has its worst behavior on inputs with exactly m 1 or m ones. Let a be an input with m 1 ones. The event − − Gj(a) = 1 has probability fi−1 by definition. The event (G1∨G2)(a) = 1 has probability 1 (1 fi 1)[2] as has the event (G3 G4)(a) = 1 . Hence − − − ∨ the event that Fi(a) = 1 has probability (1 − (1 − fi−1)[2])[2] = fi .


-----

**245**

###### Let b be an input with m ones. The event Gj(b) = 0 has probability hi−1 by definition. The event (G1 ∨ G2)(b) = 0 has probability h[2]i−1 [as] has the event (G3 ∨ G4)(b) = 0 . Hence the event that Fi(b) = 0 has probability 1 − (1 − h[2]i−1[)][2][ = h][i][ .] 2

; ; : : :

###### What is the behavior of the sequence f0 f1 for some given f0 ?
 By elementary calculations

 √

; ; ; =
###### fi = fi−1 ⇔ fi−1 ∈{0 α 1 (3 + 5) 2} (3.6)
 √

=

###### for α = (3 5) 2 and −


###### √

= ; ; ; :

###### hi = hi−1 ⇔ hi−1 ∈{−(1 + 5) 2 0 1 − α 1} (3.7)

;
###### The only fix points in the interval (0 1) are fi−1 = α and hi−1 = 1 − α . Considering the representation of fi and hi in Lemma 3.1 we note that

< < < < <

###### fi fi−1 iff fi−1 α and that hi hi−1 iff hi−1 1 − α . If f0 α and

<

###### h0 1 − α, then fi and hi are decreasing sequences converging to 0 .

; <

###### To us it is important that fl hl 2[−][n][−][1] for some l = O(log n) (see
 (3.2) – (3.4)).

=
###### It turned out that p = 2α (2m 1) is a good choice. Let a be an − input with m 1 ones. Then −

=
###### f0 = Prob(F0(a) = 1) = (m − 1)p = α − α (n − 1) (3.8)

:
###### = α Ω(n[−][1]) −

 Let b be an input with m ones. Then

 h0 = Prob(F0(a) = 0) = 1 − Prob(F0(b) = 1) = 1 − mp (3.9)

= :
###### = 1 α α (n 1) = 1 α Ω(n[−][1]) − − − − −

 We shall see that α − f0 and 1 − α − h0 are large enough such that fi and hi decrease fast enough.
 The function fi − fi−1 is continuous (in fi−1) . Hence fi − fi−1 is

;

###### bounded below by a positive constant if fi 1 [ε[′] α ε] for some fixed
_−_ _∈_ _−_

;  - < <
###### ε ε[′] 0 . If fi α − ε, fj ε[′] for some j = i + O(1) . But for which i

< <

###### it holds that fi α − ε if f0 = α − Ω(n[−][1]) ? For which l fl 2[−][n][−][1] if


-----

**246**


###### fj


<
###### ε[′] ?


< < ; ;

###### By Lemma 3.1 fi 4 fi[2]−1 [and h][i] 4 h[2]i−1 [for f][i][−][1] hi−1 ∈ (0 1] . Let

= ; <   ###### ε[′] = 1 16 and fj hj ε[′] . For l j and k = 2[l] [−][j]


< <
###### · · · 4[k][−][1] fj[k]


< =
###### (1 4)[k] = 2[−][2k] (3.10)


<
###### 4[3] fl[4] 2
_−_


###### fl


<
###### 4 fl[2] 1
_−_


###### and also hl


<
###### 2[−][2k] . If l = j + log n, k n and ⌈ ⌉ ≥


< :
###### 2[−][2k] 2[−][2n] 2[−][n][−][1] (3.11) ≤ ≤


###### fl


;
###### hl


< < ; <

###### If fi α − ε and hi 1 − α − ε, then fl hl 2[−][n][−][1] for
 l = i + log n + O(1). ⌈ ⌉

         ###### It is easy to check that for δ 0
 fi−1 = α − δ ⇒ fi = α − 4αδ + O(δ[2]) and (3.12)

:
###### hi−1 = 1 − α − δ ⇒ hi = 1 − α − 4αδ + O(δ[2]) (3.13)

 Hence


<  - < <
###### ∀ γ 4α ∃ ε 0 ∀ 0 δ ε : fi = α − δ ⇒ fi
 hi−1 = 1 − α − δ ⇒ hi


<
###### α γδ and −

< :
###### 1 α γδ − − (3.14)


            ###### We know that f0 ≤ α − c n[−][1] for some c 0 . Hence by (3.14) fi ≤

< =

###### α γ[i] c n[−][1] if γ[i][−][1] c n[−][1] ε . If we choose i = (log n) (log γ) + c[′] −

<

###### for some appropriate c[′], then fi α − ε and (by similar arguments)

< <

###### hi 1 − α − ε . Altogether Prob(Fl = Tm[n] [)][ ≥] [1][=][2 for all][ γ] 4 α, some
 appropriate c[′′] depending on γ and


:

###### l = (log n)(1 + log[−][1] γ) + c[′′] (3.15)

 The size of Fl is bounded by


###### √

; <
###### 2[2][l] = O(n[β]) where β = 2(1 + log[−][1] γ) γ 4α = 2(3 −


:
###### 5) (3.16)


###### Choosing γ = 4α η for some small η we obtain a monotone formula − for T[n]m [of size O(n][5][:][271][) .]

 THEOREM 3.1 : The monotone formula size of each threshold func- tion T[n]k [is bounded by O(n][5][:][271][) .]


-----

**247**

###### The best lower bounds on the formula size of the majority function

; ;
###### (over the monotone basis and over ) are of size Ω(n[2]) . Hence {∧ ∨ ¬} the investigation of the (monotone) formula size of threshold functions is not yet complete.

 8.4 The depth of symmetric functions

 We are not able to prove ω(log n) lower bounds on the depth of explicitly defined Boolean functions. For functions depending es- sentially on n variables a log n lower bound is obvious. Most of ⌈ ⌉

             ###### the lower bounds of size c log n for some c 1 follow from Ω(n[c]) bounds on the formula size. There are only few exceptions where lower bounds on the depth are proved directly. McColl (78 c) proved such bounds for symmetric functions and the complete bases NAND { }

;
###### and NAND . Since the methods are similar, we concentrate us { →} on the basis NAND . Further results for special functions are proved { } by McColl (76).

 We know already (see Theorem 4.1, Ch. 3) that the depth of all symmetric functions is Θ(log n) . For the proof of lower bounds over the basis NAND we make the most of the cognition that NAND- { } circuits of small depth compute only functions of short prime impli- cants.

 LEMMA 4.1 : If f can be computed by a NAND-circuit of depth 2 d + 1, the length of each prime implicant of f is bounded by 2[d] .

 Proof : Induction on d . If d = 0, the depth is bounded by 1 . The only

;

###### functions which are computable in depth 1 are xi, xi = NAND(xi xi)

;

###### and xi xj = NAND(xi xj) . All prime implicants have length 2[d] = 1 . ∨
 Let us now assume that the lemma holds for all functions of depth d[′] 2d+1 . Let f be a function of depth 2d+2 or 2d+3, and let S be ≤


-----

**248**

###### a depth optimal circuit for f . At least one of the direct predecessors of the output gate is also a gate. Hence


###### � f = NAND NAND(h1


; ;
###### h2) NAND(h3


; �
###### h4) = (h1 ∧ h2) ∨ (h3 ∧ h4) (4.1)


###### � or f = NAND NAND(h1


; ; �
###### h2) xi = (h1 ∧ h2) ∨ xi


; : : : ;

###### for functions h1 h4 whose prime implicants have by induction hy pothesis lengths bounded by 2[d] . Thus the length of the prime impli- cants of f is bounded by 2[d+1] . 2

 LEMMA 4.2 : Let t be an implicant of f ∈ Sn of length s . Then the value vector v(f) of f contains a substring of length n s+1 consisting − of ones only.

 Proof : We replace s variables by constants in such a way that t and hence also f are replaced by 1 . The substring of v(f) for this subfunction has length n s + 1 and consists of ones only. 2 −

 THEOREM 4.1 : If f ∈ Sn is not constant,

:
###### D{NAND}(f) ≥ 2 log n − (2 log 3 − 1) (4.2)

;
###### Proof : Since f = NAND(f f), f and f have almost the same depth. ¬ ¬ If the depth is small, the prime implicants of f and f are short and ¬ v(f) and v( f) have long substrings consisting of ones only. Hence v(f) ¬ has a long substring of ones only and a long substring of zeros only.

=
###### The length of the shorter substring is bounded by (n + 1) 2 .

<
###### Case 1 : 2[k] n 3 2[k][−][1] . ≤ ·

;
###### We choose d so that D{NAND}(f) ∈ {2d − 1 2d} . Then D{NAND}(¬f) ≤ 2d + 1 . By Lemma 4.1 the lengths of the prime im- plicants of f and f are bounded by 2[d] . v(f) contains a 0-sequence ¬ whose length is at least n + 1 2[d] and a 1-sequence whose length is −


-----

**249**

###### at least n + 1 2[d] . The length of v(f) is n + 1 . Hence −

:
###### n + 1 2(n + 1 2[d]) and 2[d+1] n + 1 2[k] + 1 (4.3) ≥ − ≥ ≥

 Since d and k are natural numbers

 D{NAND}(f) ≥ 2 d − 1 ≥ 2 k − 1 = 2 (k − 1) + 1 (4.4)

    - = :
###### 2 log(n 3) + 1 = 2 log n (2 log 3 1) − −

<
###### Case 2 : 3 2[k][−][1] n 2[k+1] . · ≤

;
###### We use similar arguments. Let D{NAND}(f) ∈{2d 2d + 1}, hence D{NAND}(¬f) ≤ 2d+2 . v(f) contains a 1-sequence (0-sequence) whose length is at least n + 1 2[d] (n + 1 2[d+1]) . Hence − −
 n + 1 n + 1 2[d] + n + 1 2[d+1] 3 2[d] n + 1 3 2[k][−][1] + 1 ≥ − − ⇒ · ≥ ≥ · (4.5)

:
###### ⇒ D{NAND}(f) ≥ 2 d ≥ 2 k ≥ 2 (log n − 1) ≥ 2 log n − (2 log 3 − 1)

 2

 8.5 The Hodes and Specker method

 After intensive studies on the depth and formula size of symmetric functions and above all threshold functions we switch over to general methods for the proof of lower bounds on the formula size of Boolean functions. Many applications on the Hodes and Specker method are presented by Hodes (70). Hodes and Specker (68) stated only that their method yields nonlinear bounds. Vilfan (72) proved that the bounds actually are of size n log[∗] n . Pudl´ak (84 a) combined the re- sults of Hodes and Specker and the Ramsey theory (see e.g. Graham, Rothschild and Spencer (80)) and proved the following theorem.


###### THEOREM 5.1 : For each binary basis Ωthere is some εΩ


###### 0 such


-----

**250**

###### that the following statement holds for all r ≥ 3 and all f ∈ Bn whose formula size with respect to Ωis bounded above by εΩn(log logn − r) . There is a set of n − r variables such that the subfunction f[′] ∈ Br of f where we have replaced these n r variables by zeros is symmetric, −

; : : : ;

###### and its value vector v(f[′]) = (v0 vr) has the following form: v1 =
 v3 = v5 = · · · and v2 = v4 = v6 = · · · . Hence f[′] is uniquely defined

;

###### by v0 v1 and v2 .


###### The proof is based on the fundamental principle of the Ramsey theory. Simple objects, here formulas of small size, are locally simple, i.e. have very simple symmetric functions on not too few variables as subfunctions. We leave out the proof here. A direct application of the Ramsey theory to lower bounds on the formula size has been worked out by Pudl´ak (83). Since the Ramsey numbers are increasing very fast, such lower bounds have to be of small size.

 Here we explain only one simple application of this method, more applications are posed as exercises.

 THEOREM 5.2 : L(T[n]2[) = Ω(n log log n) .]

 Proof : Let r = 3 . If we replace n−3 variables by zeros, T[n]2 [is replaced] by T[3]2 [. For the value vector of T]2[3] [v][1][ ̸][= v][3][ .] 2

 This is the largest known lower bound on L(T[n]2[) .]


-----

**251**

###### 8.6 The Fischer, Meyer and Paterson method

 Also the method due to Fischer, Meyer and Paterson (82) is based on the fact that simple functions have very simple subfunctions. This method yields larger lower bounds than the Hodes and Specker method but for a smaller class of functions. The class of very simple functions

;
###### is the class of affine functions x1 ⊕· · ·⊕ xm ⊕ c for c ∈{0 1} . The size of an affine function is the number of variables on which it depends essentially. A subfunction f[′] of f is called a central restriction of f if n1 − n0 ∈{0,1} for the number of variables replaced by ones (n1) and zeros (n0) .

 THEOREM 6.1 : Let a(f) be the maximal size of an affine sub- function of f when considering only central restrictions. Then for all

N
###### Boolean functions f ∈ Bn (n ∈ )

               ###### L(f) ε n (log n log a(f)) for some constant ε 0 . (6.1) ≥ −

 We also omit the tedious proof of this theorem. The following result states a rather general criterion for an application of this method. Afterwards we present a function for which the bound of Theorem 6.1 is tight.

 THEOREM 6.2 : If f(a) = c for all inputs with exactly k ones and f(a) = c for all inputs with exactly k + 2 ones, then


###### � ; � L(f) ε[′] n log min k n k for some constant ε[′] ≥ { − }


###### 0 . (6.2)


=
###### Proof : W.l.o.g. k n 2 . At first we prove the assertion for ≤⌊ ⌋

=
###### k = n 2 . It is sufficient to prove that a(f) 2 . Let us consider ⌊ ⌋ ≤

=
###### a central restriction f[′] ∈ B3 of f . Then ⌈(n − 3) 2⌉ variables have

=
###### been replaced by ones and (n 3) 2 variables have been replaced ⌊ − ⌋


-----

**252**

= ; ; ; ;
###### by zeros. Since k (n 3) 2 = 1, f[′](1 0 0) = c but f[′](1 1 1) = c . −⌈ − ⌉ Hence f[′] is not affine.

< =
###### If k ⌊n 2⌋, we consider an optimal formula F for f . Let bi be the number of leaves of F labelled by xi . Then we replace those n − 2k variables by zeros which have the largest b-values. The formula size of the subfunction f[′] ∈ B2k is at least ε[′] (2 k) log k as we have proved in the last paragraph. Hence there is some variable xi such that at least ε[′] log k leaves of the subformula F[′] of F are labelled by xi . By definition, bj ε[′] log k for all xj which we have replaced by zeros. ≥ Hence

:
###### L(f) = L(F) (n 2k) ε[′] log k + ε[′] (2 k) log k = ε[′] n log k (6.3) ≥ −

 2

 THEOREM 6.3 : L(C[n]0;4[) = Θ(n log n) for the counting function C][n]0;4 [.]

 Proof : C[n]0;4[(a) = 1 iff a][1][ +][ · · ·][ + a][n][ ≡] [0 mod 4 (see Def. 4.1, Ch. 3).] The lower bound follows from Theorem 6.2, since each substring of v(C[n]0;4[) of length 4 contains exactly one 1 . Hence we may choose k]

= =
###### such that n 2 2 k n 2 + 2 . − ≤ ≤
 For the upper bound we assume w.l.o.g. that n = 2[m] . Let D[n]1[(x) and D][n]0[(x) be the last two bits of x][1][ +][ · · ·][ + x][n][ .] Then � � C[n]0;4[(x) = NOR] D[n]1[(x)][;][ D][n]0[(x)] . Obviously L(D[n]0[(x)) = n, since]

; =

###### D[n]0[(x) = x][1][ ⊕· · · ⊕] [x][n][ . Let x = (x][′] x[′′]) where x[′] and x[′′] contain n 2
 variables each. Then

 � �; D[n]1[(x) = D]1[n][=][2][(x][′][)][ ⊕] [D]1[n][=][2][(x][′′][)][ ⊕] D0[n][=][2][(x][′][)][ ∧] [D]0[n][=][2][(x][′′][)] (6.4)
 L(D[n]1[)][ ≤] [2 L(D]1[n][=][2][) + n] and L(D[2]1[) = 2][:] (6.5)

 Hence L(D[n]1[)][ ≤] [n log n and L(C][n]0;4[)][ ≤] [n(1 + log n) .] 2


-----

**253**

###### 8.7 The Nechiporuk method

 The lower bound due to Nechiporuk (66) is based on the observa- tion that there cannot be a small formula for a function with many different subfunctions. There have to be different subformulas for dif- ferent subfunctions.

 DEFINITION 7.1 : Let S X be a set of variables. All subfunctions ⊆ f[′] of f, defined on S, are called S-subfunctions.


###### THEOREM 7.1 : Let f ∈ Bn depend essentially on all its variables,

; : : : ;

###### let S1 Sk X be disjoint sets of variables, and let si be the number
 ⊆ of Si-subfunctions of f . Then


###### L(f) ≥ N(S1


; : : : ; =
###### Sk) := (1 4) log si
 [�]

1 i k
_≤_ _≤_


:
###### (7.1)


###### Proof : Let F be an optimal formula for f and let ai be the number of leaves labelled by variables xj Si . It is sufficient to prove that ∈

=
###### ai (1 4) log si . Let Ti be that subtree of F consisting of all leaves ≥ labelled by some xj Si and consisting of all paths from these leaves ∈ to the output of F . The indegree of the nodes of Ti is 0, 1 or 2 . Let Wi be the set of nodes of indegree 2 . Since it is obvious that |Wi| = ai − 1, it is sufficient to prove that

= :
###### |Wi| ≥ (1 4) logsi − 1 (7.2)

 Let Pi be the set of paths in Ti starting from a leaf or a node in Wi, ending in a node in Wi or at the root of Ti and containing no node in Wi as inner node. There are at most |Wi| + 1 different end-points of paths in Pi . Because of the definition of Pi there are at most two Pi- paths ending in some gate G . These paths can be found by starting in G and going backwards until a node in Wi or a leaf is reached. Hence


-----

**254**

:
###### |Pi| ≤ 2 (|Wi| + 1) (7.3)

 The different replacements of the variables xj Si lead to si dif- ̸∈ ferent subformulas. We measure the local influence of different re- placements. Let p be a path in Pi and let us fix a replacement of all variables xj Si . If h is computed at the first gate of p, then the func- ̸∈ tion computed on the last edge of p is 0, 1, h or h, since no variable xk Si has any influence on this path. Since Ti can be partitioned ∈ into the paths p ∈ Pi, the number of Si-subfunctions is bounded by 4[|][P][i][|] . Hence

 si ≤ 4[|][P][i][|] (7.4)

 and (7.2) follows from (7.3) and (7.4). 2


###### What is the largest possible size of the Nechiporuk bound

; : : : ;

###### N(S1 Sk) ?

; : : : ;

###### THEOREM 7.2 : If f ∈ Bn, the Nechiporuk bound N(S1 Sk) is
 not larger than 2 n[2] log[−][1] n .


###### Proof : Let t(i) = |Si| . There are 2[n][−][t(i)] possibilities of replacing
 the variables xj Si by constants, and there are not more than 2[2][t(i)] ̸∈
 functions on Si . Hence

; :
###### log si ≤ min{n − t(i) 2[t(i)]} (7.5)


    - <
###### W.l.o.g. t(i) log n iff i ≤ q . Since the sets Si are disjoint, q n log[−][1] n and
 � :
 log si ≤ [�] (n − t(i)) ≤ n[2] log[−][1] n (7.6)
1 i q 1 i q
_≤_ _≤_ _≤_ _≤_


###### Furthermore
 �

q<i k log si ≤ q<[�]i k2[t(i)]
_≤_ _≤_


:
###### (7.7)


-----

**255**

###### Since the function x 2[x] is convex, the right-hand side of (7.7) is → maximal if as many t(i) as possible are equal to log n, the upper bound for these t(i) . Hence also (7.7) is bounded by n[2] log[−][1] n . 2

 Indeed it is possible to prove by Nechiporuk’s method bounds of size n[2] log[−][1] n . The Nechiporuk function is dealt with in the Exercises. We prove a bound of this size for a storage access function for indirect addressing (Paul (77)).

 DEFINITION 7.2 : The storage access function (for indirect address- ing) ISAn ∈ Bn where n = 2p + k for some p = 2[2][l] and k = log p −

; : : : ; ; : : : ;

###### log logp is defined on the variables x = (x1 xp), y = (y0 yp 1)

_−_

; : : : ;

###### and a = (a0 ak 1) .

_−_

; : : : ;

###### Let d = (x|a| logp+1 x(|a|+1) logp) where |a| is the binary number rep
; ;
###### resented by a . Then ISAn(x y a) = y|d| .


###### THEOREM 7.3 : L(ISAn) = Ω(n[2] log[−][1] n) and C(ISAn) ≤ 2n+o(n) .

; : : : ;

###### Proof : Let Si = {xi log p+1 x(i+1) log p} for 0 ≤ i ≤ p log[−][1] p−1 . For
 fixed i we replace the a-variables by constants so that a = i . Then | | y is the value table of the Si-subfunction. All 2[p] different value tables lead to different Si-subfunctions. Hence si ≥ 2[p] and by the Nechiporuk method

= :
###### L(ISAn) ≥ (1 4) p[2] log[−][1] p = Ω(n[2] log[−][1] n) (7.8)

 By Theorem 5.1, Ch. 3, the circuit complexity of SAn, the stor- age access function for direct addressing, is bounded by 2n + o(n) . Hence each x|a| log p+j (1 ≤ j ≤ log p) can be computed by 2 p log[−][1] p + o(p log[−][1] p) gates. The whole vector d can be computed with 2p+o(p) gates. Afterwards ISAn can be computed with 2p + o(p) gates. Alto- gether 4p + o(p) = 2n + o(n) gates are sufficient for the computation of ISAn . 2


-----

**256**

###### Nechiporuk’s method has been applied to many functions. We re- fer to Harper and Savage (72) for the marriage problem and to Pater- son (73) for the recognition of context free languages. We investigate the determinant (Kloss (66)) and the clique functions (Sch¨urfeld (84)). The determinant detn BN where N = n[2] is defined by ∈


###### det
n [(x][11]


; : : : ; xnn) = x1;π(1)

###### [�]

_π∈Σn_


: : : xn;π(n)


:
###### (7.9)


=
###### THEOREM 7.4 : L(detn) ≥ (1 8) (n[3] − n[2]) .

 Proof : Let Si = {xj;(i+j)modn | 1 ≤ j ≤ n} contain the variables of some secondary diagonal. Since the determinant does not change if we interchange rows or columns, we conclude that s1 = · · · = sn . We only consider Sn, the variables of the main diagonal, and prove the existence of 2[(n][2][−][n)][=][2]Sn-subfunctions. Then the theorem follows by the Nechiporuk method.
 Let yj = xjj . We replace the variables below the main diagonal by fixed constants in the following way.


###### y1 c12 c13 :::: c1;n−2 c1;n−1 c1n
 1 y2 c23 :::: c2;n−2 c2;n−1 c2n
 0 1 y3 :::: c3;n−2 c3;n−1 c3n

:: :: :: :::: :: :: ::

###### 0 0 0 :::: 1 yn 1 cn 1;n
_−_ _−_

::::
###### 0 0 0 0 1 yn


###### 
 


###### gc(y1


; : : : ;
###### yn) = det
n


###### 
 


:
###### (7.10)


= <
###### Since there are (n[2] − n) 2 matrix elements cij (i j) above the main diagonal, it is sufficient to prove that gc and gc[′] are different functions for different c and c[′] .

;

###### For n = 2 gc(y1 y2) = y1 y2 c12 and the assertion is obvious. The
 ⊕ case n = 3 is left as an exercise.


-----

**257**

   ###### For n 3 we apply matrix operations which do not change the determinant. We multiply the second row by y1 and add the result to the first row. The new first row equals


;
###### (0 y1 y2 c12 ⊕


;
###### y1 c23 c13 ⊕


; : : : ; :
###### y1 c2n c1n) (7.11) ⊕


###### The first column has a one in the second row and zeros in all other rows. Hence we can erase the first column and the second row of the matrix. For y1 = 1 we obtain an (n − 1) × (n − 1)-matrix of type (7.10). By induction hypothesis we conclude that gc and gc[′] differ if cij ̸= c[′]ij [for some i][ ≥] [3 or c][1k][ ⊕] [c][2k][ ̸][= c]1k[′] [⊕] [c]2k[′] [for some k][ ≥] [3 .]

 By similar arguments for the last two columns (instead of the first two rows) we conclude that gc and gc[′] differ if cij ̸= c[′]ij [for some] j ≤ n − 2 or ck;n−1 ⊕ ckn ̸= c[′]k;n−1 [⊕] [c]kn[′] [for some k][ ≤] [n][ −] [2 . Alto-] gether we have to consider only the situation where cij = c[′]ij [for all]

; ; ; ; ; ; ; ;
###### (i j) ̸∈{(1 n − 1) (1 n) (2 n − 1) (2 n)} and c1k ⊕ c2k = c[′]1k [⊕] [c]2k[′] [for]

;
###### k ∈{n − 1 n} . Let y1 = 0 . Then we can erase the first column and the second row of the matrix. We obtain (n 1) (n 1)-matrices − × − M and M[′] which agree at all positions except perhaps the last two positions of the first row. Since c ̸= c[′] and c1k ⊕ c2k = c[′]1k [⊕] [c]2k[′] [for] k n 1; n, c1;n 1 = c1;n 1[′] or c1n = c1n[′] or both. By an expansion ∈{ − } − ̸ − ̸ according to the first row we compute the determinants of M and M[′] . The summands for the first n 3 positions are equal for both matrices. − The (n − 2)-th summand is yn if c1;n−1 = 1 (c1[′] ;n−1 [= 1 resp.) and 0] else, and the last summand is 1 if c1n = 1 (c1n[′] [= 1 resp.) and 0 else.] Hence gc(y) ⊕ gc[′](y) is equal to yn or 1 or yn ⊕ 1 according to the three cases above. This ensures that gc ̸= gc[′] if c ̸= c[′] . 2

 The clique function cln;m MN where N = �n2� (see Def. 11.1, Ch. 6) ∈ checks whether the graph G(x) contains an m-clique.

 THEOREM 7.5 : L(cln;m) ≥ (1=48)(n − m)[3] − o((n − m)[3]) if m ≥ 3 .


-----

**258**

###### Proof : It is sufficient to prove the claim for m = 3, since cln (m 3);3
_−_ _−_
###### is a subfunction of cln;m . We only have to replace all edges adjacent

; : : : ;
###### to the nodes n m + 4 n by ones. −
 Let Si = {xi;i+1 ; : : : ; xin} for 1 ≤ i ≤ n − 1 . In order to estimate the
 number of Si-subfunctions, we replace all edges adjacent to the nodes

; : : : ;
###### 1 i 1 by zeros. These nodes are isolated and cannot belong to a −

<
###### 3-clique. We replace the variables xkl (i+1 ≤ k l ≤ n) in such a way

; : : : ;
###### by constants, that the graph on the nodes i+1 n does not contain a 3-clique. Different replacements lead to different Si-subfunctions. If akl = 1 for one replacement and a[′]kl [= 0 for another replacement, let] xik = xil = 1 and xij = 0 for all other j . The first graph contains

; ;
###### the 3-clique on i k l, but the second graph does not contain any { } 3-clique at all.

 Hence the number of Si-subfunctions is not smaller than the num- ber of graphs on n i vertices without any 3-clique. We partition −

=
###### the set of vertices into two sets M1 and M2 of size ⌈(n − i) 2⌉ and

=
###### (n i) 2 resp. No bipartite graph contains a 3-clique. Hence ⌊ − ⌋ the number of Si-subfunctions is at least 2[⌈][(n][−][i)][=][2][⌉⌊][(n][−][i)][=][2][⌋] . By the Nechiporuk method

 L(cln;3) ≥ (1=4) � ⌈(n − i)=2⌉⌊(n − i)=2⌋ (7.12)

1 i n 1
_≤_ _≤_ _−_


###### = (1=16) � (n i)[2] o(n[3]) = (1=48) n[3] o(n[3]):
 − − −
1 i n 1
_≤_ _≤_ _−_

###### 8.8 The Krapchenko method


###### 2


###### The lower bound methods of 5 – 7 work for all (binary) bases. § § Then the parity function f(x) = x1 xn is a simple function. For ⊕· · · ⊕ an input a f[−][1](c) all neighbors, i.e. all inputs b which differ from ∈ a at exactly one position, are elements of f[−][1](c) . For the functions


-----

**259**

###### g(x) = xi computed at the inputs each vector a ∈ g[−][1](c) has exactly one neighbor in g[−][1](c) . Using only gates of type-, i.e. using the basis ∧

; ;
###### U = B2 −{⊕ ≡}, the number of pairs of neighbors (a b), such that h(a) = h(b) for the computed function h, is increasing only slowly. ̸ This observation is the principal item of the Krapchenko method. Hence this method works only for the basis U .

 We assume that the leaves of a formula can be labelled by any literal (xi or xi) . Then we can apply the rules of deMorgan, and all inner nodes are labelled by or . We do not present the proof due ∧ ∨ to Krapchenko (71, 72 b) but a simpler proof due to Paterson (pers. comm.).

 DEFINITION 8.1 : A formal complexity measure FC is a function

N
###### FC : Bn → such that i) FC(xi) = 1 for 1 ≤ i ≤ n,
 ii) FC(f) = FC(¬f) for f ∈ Bn and

;
###### iii) FC(f ∨ g) ≤ FC(f) + FC(g) for f g ∈ Bn .

 By this definition and the rules of deMorgan also FC(f g) ∧ ≤ FC(f) + FC(g) . LU is a formal complexity measure. Moreover LU is the largest formal complexity measure.

 LEMMA 8.1 : LU(f) ≥ FC(f) for any f ∈ Bn and any formal com- plexity measure FC .

 Proof : By induction on l = LU(f) . If l = 1, f = xi or f = xi, and

        ###### FC(f) = 1 . Let l = LU(f) 1 and let F be an optimal U-formula for f . W.l.o.g. the last gate of F is an -gate whose input functions are ∨ g and h . Hence f = g h . The subformulas for g and h are optimal, ∨ too. By the induction hypothesis

:
###### LU(f) = LU(g) + LU(h) ≥ FC(g) + FC(h) ≥ FC(f) (8.1)

 2


-----

**260**

###### We look for a formal complexity measure FC such that for many difficult functions f FC(f) is large and can be estimated easily.

; ;
###### DEFINITION 8.2 : Let H(A B) be the set of neighbors (a b) ∈ A B . Let ×

;
###### KAB = |H(A B)|[2] |A|[−][1] |B|[−][1] and (8.2)

; :
###### K(f) = max{KAB | A ⊆ f[−][1](1) B ⊆ f[−][1](0)} (8.3)

 THEOREM 8.1 : LU(f) ≥ K(f) for all Boolean functions f .

 Proof : It is sufficient to prove that the Krapchenko measure K is a formal complexity measure.

 i) Claim : K(xi) = 1 . ˝ ˝ : Let B be the set containing only the zero vector, and let A be ≥ the set containing only the i -th unit vector. ˝ ≤ ˝ : Each vector in x[−]i [1][(0) has only one neighbor in x]i[−][1][(1) and vice] versa.

 ii) K(f) = K( f) by definition, since the definition of K(f) is symmetric ¬ with respect to f[−][1](0) and f[−][1](1).

 iii) Claim : K(f g) K(f) + K(g) . ∨ ≤ We choose A (f g)[−][1](1) and B (f g)[−][1](0) in such a way that ⊆ ∨ ⊆ ∨ K(f∨g) = KAB . Then B ⊆ f[−][1](0) and B ⊆ g[−][1](0). We partition A into

;
###### disjoint sets Af ⊆ f[−][1](1) and Ag ⊆ g[−][1](1). Then H(A B) is the disjoint

; ; ;

###### union of H(Af B) and H(Ag B) . Let ag = |Ag|, hf = |H(Af B)| and
 so on. Then

 K(f g) = h[2]a[−][1]b[−][1] and (8.4) ∨

:

###### K(f) + K(g) ≥ h[2]f [a]f[−][1][b][−][1][ + h]g[2][a][−]g [1][b][−][1]

 It is sufficient to prove that


###### h[2] a[−][1] b[−][1] ≤ h[2]f [a]f[−][1] b[−][1] + h[2]g [a]g[−][1] [b][−][1]


:
###### (8.5)


###### We make use of the facts that h = hf + hg and a = af + ag . Hence

:
###### (8 5) ⇔ (hf + hg)[2] af ag ≤ h[2]f [a][g][ (a][f][ + a][g][) + h]g[2] [a][f][ (a][f][ + a][g][)] (8.6)


-----

###### ⇔ 0 ≤ h[2]f [a]g[2] [−] [2 h][f][ h][g][ a][f][ a][g][ + h]g[2] [a]f[2] [= (h][f][ a][g][ −] [h][g][ a][f][)][2]

 LEMMA 8.2 : K(f) ≤ n[2] for all f ∈ Bn .


:


**261**

###### 2


; ;
###### Proof : H(A B) min n A n B, since each vector has only | | ≤ { | | | |} n neighbors. 2

 THEOREM 8.2 : For the parity function fn(x) = x1 ⊕· · · ⊕ xn L(fn) = n and LU(fn) ≥ n[2] . If n = 2[k], LU(fn) = n[2] .

 Proof : Obviously L(fn) = n . If A = fn[−][1][(1) and B = f]n[−][1][(0),][ |][A][|][ =] B = 2[n][−][1] . Each neighbor of a A lies in B and vice versa, i.e. | | ∈

;
###### |H(A B)| = n 2[n][−][1] . Hence LU(fn) ≥ n[2] by Theorem 8.1.
 We still have to prove an upper bound on LU(fn) for n = 2[k] .

; =

###### Let x = (x[′] x[′′]) where x[′] and x[′′] have length n 2 each.


###### fn(x) = �fn=2(x[′]) ∧ (¬fn=2(x[′′]))� ∨ �(¬fn=2(x[′])) ∧ fn=2(x[′′])�: (8.7)


###### Hence

 LU(fn) ≤ 4 LU(fn=2); LU(f1) = 1; and LU(fn) ≤ n[2]


:
###### (8.8)

 2


###### This difference between the bases B2 and U has been proved by Krapchenko (72 a). The Krapchenko method yields good lower bounds for several symmetric functions (see Theorem 8.2 and Exercises). It is easy to prove that the Nechiporuk bound is linear for all symmet- ric functions. The Nechiporuk method is sometimes useful also for functions with short prime implicants (cln;3 in Theorem 7.5). For such functions no nonlinear lower bound can be proved by the Krapchenko bound (Sch¨urfeld (84)).

 THEOREM 8.3 : Let l PI(f) be the smallest number such that some polynomial for f contains only prime implicants of length l ≤ l PI(f) .


-----

**262**

###### Let l PC(f) be defined in a similar way for prime clauses. Then K(f) ≤ l PI(f) l PC(f) .

 Proof : Let A f[−][1](1) and B f[−][1](0) . For a A we find some prime ⊆ ⊆ ∈ implicant t of f such that t(a) = 1 and the length of t is bounded by l PI(f). If a[′] ∈ f[−][1](0) is a neighbor of a, t(a[′]) = 0 . Hence a and a[′]
 differ in a position i where xi or xi is a literal of t .

; ;
###### This implies |H(A B)| ≤ l PI(f)|A| . Similarly |H(A B)| ≤ l PC(f)|B| . Altogether KA;B ≤ l PI(f)l PC(f) . 2

 As a further example we apply the Krapchenko method to the determinant.

=
###### THEOREM 8.4 : LU(detn) ≥ (1 12) n[4] .

 Proof : Let A = det[−]n [1][(1) and B = det]n[−][1][(0) .][ |][A][|][ is the number of]

Z ; ; ;
###### regular n × n-matrices over the field 2 = ({0 1} ⊕ ∧) . The first row of such a matrix has to be different from the zero vector, we have 2[n] 1 − possibilites for the choice of this row. If we have chosen i 1 linearly − independent vectors, these vectors are spanning a vector space of 2[i][−][1]
 vectors. For the choice of the i -th row we have therefore 2[n] 2[i][−][1] −
 possibilities. Hence

 � � � � |A| = 2[n] − 2[i][−][1][�] = αn 2[n][2] where αn = 1 − 2[−][i][�] . (8.9)

1 i n 1 i n
_≤_ _≤_ _≤_ _≤_


;
###### Since (1 a)(1 b) 1 a b for a b 0, − − ≥ − − ≥

= � = � = :
###### αn = (1 2) 1 − 2[−][i][�] ≥ (1 2) 1 − [�] 2[−][i][�] ≥ (1 4) (8.10)
 [�]

2 i n 2 i n
_≤_ _≤_ _≤_ _≤_


= =

###### Furthermore αn (1 − αn) ≥ 1 3 and αn−1 ≥ αn .
 Let M be a given n n-matrix and M[′] a neighbor of M . W.l.o.g. ×

;
###### M and M[′] differ exactly at position (1 1) . We compute detn M and detn M[′] by an expansion of the first row. Then detn M ̸= detn M[′] iff the (n 1) (n 1)-matrix M[∗] consisting of the last n 1 rows − × − − and columns of M (or M[′]) is regular. We have n[2] possibilities for the


-----

**263**

###### choice of the position where M and M[′] differ, αn−1 2[(n][−][1)][2] possibilities for the choice of M[∗] and 2[2(n][−][1)] possibilities for the choice of the other members of the i -th row and the j -th column if M and M[′] differ at

;
###### position (i j) . Hence


; = :
###### |H(A B)| = n[2] 2[2(n][−][1)] αn−1 2[(n][−][1)][2] = (1 2) αn−1 n[2] 2[n][2] (8.11)

 Altogether


###### K(det n−1 [n][4][ 2][2n][2] αn−1
n [)][ ≥] _α[(1]n 2[=][4)][n][2][ α](1[2] −_ _αn) 2[n][2][ = 1]4_ _αn_


###### αn 1
_−_ :

###### n[4] (8.12) ≥ [1] 1 − αn 12 [n][4]
 2


###### EXERCISES

 1. L(f g) = L(f)+L(g) if f and g depend essentially on disjoint sets ∨ of variables.

 2. (Bublitz (86)) Let


###### f(x1


; : : : ;
###### x6) = x1 x4 x1 x6 x2 x4 x2 x6 x3 x6 x4 x5 x4 x6 ∨ ∨ ∨ ∨ ∨ ∨


:


###### a) There is a single-level circuit of size 7 for f .

 b) Cm(f) = 7 .
 c) L[∗]m[(f) = 7 .]
 d) All single-level formulas for f have at least 8 gates.

 3. Let L[∧]m[(f) and L][∨]m[(f) be the minimal number of][ ∧][-gates and][ ∨][-] gates resp. in monotone formulas for f .
 a) L[∧]m[(f) + L][∨]m[(f)][ ≤] [L][∗]m[(f) .]
 b) L[∗]m[(T][4]2[) = 7 .]
 c) L[∧]m[(T][4]2[) = 2 .]


-----

**264**

###### d) L[∨]m[(T][4]2[) = 4 .]

 4. Prove that the Korobkov formulas for T[n]k [(see (2.1)) have size] O(n(log n)[k][−][1]) .

 5. The Fibonacci numbers are defined by a0 = a1 = 1 and an = an−1 + an−2 . It is well-known that


###### 5) .


###### √ � an = Φ[n+1] − (Φ −


###### 5)[n+1][�]


###### √ √

= =

###### 5 for Φ = (1 2)(1 +


;
###### Let Ω= {NAND →} where (x → y) = x ∨ y and DΩ(f) ≤ d . Then f is a disjunction of monoms whose length is bounded by ad .

 6. We use the notation of Exercise 5. If f ∈ Sn is not constant, √ DΩ(f) ≥ logΦ( 5n) − 3 .

< <
###### 7. Let 1 k n − 3, f ∈ Bn, f(a) = 0 for inputs a with exactly k ones and f(a) = 1 for inputs a with exactly k + 2 ones. Then L(f) = Ω(n log log n) .


; ; : : : ; ; : : : ;
###### 8. Let f f[′] ∈ Sn, v(f) = (v0 vn) and v(f[′]) = (vn v0) . Esti mate L(f) L(f[′]) . −

 9. There are 16 symmetric functions fn Sn with linear formula size. ∈ For all other fn Sn L(fn) = Ω(n log logn) . ∈

 10. Design efficient formulas for C[n]0;8 [and for C]0[n];3 [.]

 11. Apply the Meyer, Fischer and Paterson method and the Hodes and Specker method to threshold functions.

 12. How large is the fraction of f ∈ Sn with L(f) = o(n log n) ?

 13. Apply the Nechiporuk method to circuits over Br .


-----

**265**

###### 14. The Nechiporuk method yields only linear bounds for symmetric functions.

 15. (Nechiporuk (66)) Let m and n be powers of 2, m = O(log n),

;
###### m and n large enough that there are different yij ∈{0 1}[m],

=
###### 1 i l = n m, 1 j m, having at least two ones each. Let ≤ ≤ ≤ ≤ xij be variables, and let gi;j;k(x) be the disjunction of all xkl such that yij has a 1 at position l . Let
 f(x) = 1 i l�; 1 j mxij ∧ �1 k�l ; k=igi;j;k(x)�:

_≤_ _≤_ _≤_ _≤_ _≤_ _≤_ _̸_


###### Then L(f) = Ω(n[2] log[−][1] n) .

 16. (Sch¨urfeld (84), just as 17. and 18.) Let f ∈ MN . Let k be the maximal length of a prime implicant of f . Then f has at most 2 |Si|[k][−][1] Si-subfunctions. The Nechiporuk bound is not larger than N[2][−][(1][=][k)] .

; ; �
###### 17. Let f(x y z) = zij xik ykj be the one-output function corre
1 i;j;k n
_≤_ _≤_

###### sponding to the Boolean matrix product (see 15, Ch. 6). Then § L(f) = Θ(n[3]) .


###### 18. We generalize the definition of f in Exercise 17. Let k 3 and ≥

; : : : ; ;

###### let X[1] X[k][−][1] Z be (k 1)-dimensional n n-matrices of
 − × · · · × Boolean variables. For N = k n[k][−][1] let f ∈ MN be the disjunction of all
 zi(1):::i(k−1) xr(1)[1] :::r(k−2)i(1) [· · ·][ x]r(1)[k][−][1]:::r(k−2)i(k−1)
 (1 i(j), r(j) n). Then L(f) = Ω(N[2][−][1][=][(k][−][1)]) . ≤ ≤

 19. Describe all f ∈ Bn where K(f) = n[2] for the Krapchenko mea- sure K .


-----

**266**

###### 20. Let f ∈ Bn . Let f(a) = c for all inputs a with exactly k ones and f(a) = c for all inputs a with exactly k + 1 ones. Estimate K(f) .

 21. ⌈2 log n⌉≤ DU(x1 ⊕· · · ⊕ xn) ≤ 2 ⌈log n⌉ .


-----

**267**

###### 9. CIRCUITS AND OTHER NON UNIFORM COMPUTATION MODELS VS. TURING MACHINES AND OTHER UNIFORM COMPUTATION MODELS

 9.1 Introduction

 Circuits represent a hardware model for the computation of Boolean functions. For a given sequence fn Bn we look for circuits ∈ Sn computing fn with small size (cost of the circuit, computation time for sequential computations) and small depth (computation time for parallel computations). Moreover we prefer circuits where n → Sn can be computed by an efficient algorithm. It is easy to check that most of the circuits we have designed can be constructed efficiently. An exception is the monotone formula for the majority function (Ch. 8, 3), and also the O(log n)-depth division circuit (Ch. 3, 3) cannot § § be computed very efficiently. A circuit has to be designed only once and can be applied afterwards for many computations. So the time for the construction of a circuit is not so important as the computation time of the circuit.

 How do circuits differ from software models ? A circuit works only for inputs of a definite length, whereas a reasonable program works for inputs of arbitrary length. A hardware problem is a Boolean function fn Bn . Obviously each fn is computable. A software problem is a ∈

;
###### language L 0 1, i.e. a subset of the set of all finite 0-1-sequences. ⊆{ }[∗] It is well-known that many languages are not computable. So we look for conditions implying that there is an efficient uniform algorithm for L if there is a sequence Sn of efficient non uniform circuits for fn where fn[−][1][(1) = L][ ∩{][0][;][ 1][}][n][ . And we ask whether we can design efficient] circuits Sn for fn if we know an efficient algorithm for L, the union of

N
###### all fn[−][1][(1) (n][ ∈] ) .
 Efficient simulations are known between the different uniform com- putation models (models for the software of computers). So we con

-----

**268**

###### sider Turing machines as a representative of uniform computation models. In 2 and 3 we present efficient simulations of Turing § § machines by circuits. Since there are non computable (non recursive) languages, we cannot simulate in general sequences of circuits by Tur- ing machines. In 4 we simulate efficiently circuits by non uniform § Turing machines.

;
###### Are there languages L 0 1 for which we do not know any ⊆{ }[∗] polynomial Turing program but for which we can design efficient cir- cuits, more precisely, efficient circuits Sn for fn defined by fn[−][1][(1) =]

;
###### L 0 1 ? In 5 we characterize languages with polynomial cir- ∩{ }[n] § cuits, and in 6 we simulate efficiently probabilistic Turing machines § by circuits. Nevertheless it is not believed that NP-complete languages can have polynomial circuits. In 7 we discuss some consequences if § certain NP-complete languages would have polynomial circuits.

 We prefer efficient circuits Sn for fn Bn, which can be constructed ∈ efficiently. In 8 we compare some definitions for such circuits called § uniform circuits. We close this introduction with a short survey of some concepts of the complexity theory.

 A (deterministic) Turing machine works on one on both sides un
Z
###### limited working tape. Each register i of the tape contains a letter ∈

; : : : ;

###### of a finite alphabet Σ . At the beginning the input (x1 xn) is

; : : : ;
###### contained in the registers 0 n 1, all other registers are empty − (contain the letter B = blank). The central unit of the machine is at each point of time in one state q Q where Q is finite. The state at ∈ the beginning of the computation is defined by q0 . The machine has a head which can read one register and which can move from register i to register i 1 or i + 1 . The head starts at register 0 . The program − is given by a transition function δ : Q Σ Q Σ R,L,N . If × → × × { }

; ; ;
###### the machine is in state q and reads a and if δ(q a) = (q[′] a[′] d), then
 the machine replaces the contents of the considered register by a[′], the new state of the machine is q[′], and the head moves one step in direction d (R = right, L = left, N = no move) . The computation stops in some definite state q[∗] . The result of the computation can be


-----

**269**

###### read consecutively in the registers starting at register 0 until the first register contains the letter B . Turing machines may have more than

N
###### one tape. Then there is one head for each of the k tapes (k ), and ∈ the action of the machine depends on all letters which are read by the k heads.

 For input x let t(x) be the number of steps until the machine stops and let s(x) be the number of different registers which are scanned by the head of the machine. The computation time t and the space s of the Turing machine are defined by

 t(n) = max t(x) x = n (1.1) { | | | }

 where x is the length of x and | |

:
###### s(n) = max s(x) x = n (1.2) { | | | }

; N N
###### For S T : we denote by DTIME(T) and DSPACE(S) the set → of languages which can be decided by deterministic Turing machines in time O(T(n)) or space O(S(n)) resp. A machine decides L if it computes 1 if x L and 0 if x L . ∈ ̸∈

 DEFINITION 1.1 : P is the class of languages which can be decided by deterministic Turing machines in polynomial time.

 In order to classify languages according to their complexity, one

;
###### considers non deterministic Turing machines. Then δ(q a) is a subset

; ;
###### of Q Σ R L N . There is a number of admissible computation × × { } steps. A non deterministic Turing machine accepts L if there is some admissible computation on x with output 1 iff x L . For x L ∈ ∈ the computation time tndet(x) is the length of a shortest accepting computation path. Moreover

; :
###### tndet(n) = max({tndet(x) | |x| = n x ∈ L} ∪{1}) (1.3)

 DEFINITION 1.2 : NP is the class of languages which can be decided by non deterministic Turing machines in polynomial time.


-----

**270**

###### The subclass of NP-complete languages contains the most diffi- cult problems in NP in the following sense. Either P = NP or no NP-complete language is in P (see Cook (71), Karp (72), Specker and Strassen (76), and Garey and Johnson (79)). The majority of the experts believes that NP = P . Then all NP-complete languages ̸ (one knows of more than 1000 ones) have no polynomial algorithm. We mention only two NP-complete languages, the set of all n-vertex

=
###### graphs (n arbitrary) with an n 2-clique and the class of all sets of Boolean clauses (disjunctions of literals) which can be satisfied simul- taneously (SAT = satisfiability problem).

 In order to describe the complexity of a language L relative to another language A, one considers Turing machines with oracle A . These machines have an extra tape called oracle tape. If the machine reaches the oracle state, it can decide in one step whether the word y written on the oracle tape is an element of A . If one can design an efficient Turing machine with oracle A for L the following holds. An efficient algorithm for A implies an efficient algorithm for L, because we can use the algorithm for A as a subroutine replacing the oracle queries of the Turing machines with oracle A .

 DEFINITION 1.3 : Let A be a language. P(A) or NP(A) is the class of languages which can be decided by a polynomial deterministic or non deterministic resp. Turing machine with oracle A . For a class C of languages P(C) is the union of all P(A) where A C, NP(C) is ∈ defined similarly.

 DEFINITION 1.4 : The following hierarchy of languages is called the Stockmeyer hierarchy (Stockmeyer (76)). Σ0 = Π0 = ∆0 = P . Σn = NP(Σn−1), in particular Σ1 = NP . Πn consists of all L whose complement is contained in Σn and ∆n = P(Σn−1) .

 Obviously Σn−1 ⊆ Σn . It is an open problem whether this hier- archy is proper. If Σn = Σn+1, also Σn = Σn+k for all k ≥ 0 . In order to prove NP ̸= P, it is sufficient to prove that Σn ̸= P for some


-----

**271**

###### n 1 . Kannan (82) proved by diagonalization the existence of lan- ≥

;
###### guages Lk ∈ Σ3 ∩ Π3 such that |Lk ∩{0 1}[n]| is polynomially bounded and Lk has no circuits of size O(n[k]) . At the end of this survey we state a characterization of the classes Σn and Πn (Stockmeyer (76)).

 THEOREM 1.1 : L ∈ Σn (L ∈ Πn) iff the predicate ˝x ∈ L˝ can be expressed by a quantified formula


;
###### (Q1 x1) · · · (Qn xn) T(x x1


; : : : ;
###### xn) (1.4)


; : : : ;

###### where x1 xn are vectors of variables of polynomial length, T is
 a predicate which can be decided in polynomial time and where

; : : : ;

###### Q1 Qn is an alternating sequence of quantifiers ∃ and ∀ and Q1 = ∃
 (Q1 = ∀) .

 The problem whether Σn = Σn+1 is the problem whether we can eliminate efficiently quantifiers.

 9.2 The simulation of Turing machines by circuits: time and size

 We like to simulate efficiently Turing machines by circuits. Let

;
###### M be a deterministic Turing machine deciding L 0 1 in time ⊆{ }[∗] t(n) . We look for circuits Sn for fn defined by fn[−][1][(1) = L][ ∩{][0][;][ 1][}][n]
 whose size is small with respect to t(n) . The easiest solution is a step-by-step simulation. The difficulty is the simulation of the head (if-tests). After t steps the position of the head l (t) can take any

; : : : ; ; : : : ;
###### value in t 0 t depending on the input. For this reason {− } we simulate Turing machines at first by special Turing machines with simple head moves. These Turing machines can be simulated easily by circuits.

 DEFINITION 2.1 : A Turing machine is called oblivious if the sequence of head moves is the same for all inputs of the same length.


-----

**272**

;
###### For oblivious Turing machines pos(t n), the position of the head on inputs of length n after t t(n) steps, is well defined. The t- ≤ th configuration of an oblivious Turing machine M on an input x of

;
###### length n is described uniquely by its state q(t x) and the contents

; ;
###### b(t x j) of register j where t(n) j t(n) . We use an arbitrary − ≤ ≤ encoding of Q and Σ by 0-1-sequences of length log Q and log Σ ⌈ | |⌉ ⌈ | |⌉

; ; ;
###### resp. The 0 -th configuration is known, since q(0 x) = q0, b(0 x j) =

; ;
###### xj+1 if 0 ≤ j ≤ n − 1 and b(0 x j) = B otherwise. The output is b(t(n),x,0). Let δ1 and δ2 be the first two projections of the transition function δ . Then

; ; ; ; ; ; ;
###### q(t + 1 x) = δ1(q(t x) b(t x pos(t n))) (2.1)

; ; ; ; ; ;
###### b(t + 1 x j) = b(t x j) if j = pos(t n) and (2.2) ̸

; ; ; ; ; ; ; ; :
###### b(t + 1 x pos(t n)) = δ2(q(t x) b(t x pos(t n))) (2.3)

 Since δ is a finite function, there is a circuit of size O(1) for δ . Since

;
###### pos(t n) is known in advance, we can simulate M by t(n) copies of the circuit for δ .

 THEOREM 2.1 : If L can be decided by an oblivious Turing machine in time t(n), fn ∈ Bn defined by fn[−][1][(1) = L][ ∩{][0][;][ 1][}][n][ can be computed] by a circuit of size O(t(n)) .

 This theorem holds also for oblivious Turing machines with k tapes. The problem is the simulation of Turing machines M by oblivious ones: At first we describe a simple simulation which will be improved later. The simulation works step-by-step. We use markers # (a new letter not contained in the alphabet of M) and the alphabet (Σ # )[2] . ∪{ } Then there is space for two letters in each register. After the simula- tion of the t-th step of M the registers t 1 and t+n of M[′] contain the − −

; ; : : : ;
###### mark (# #) . The first letter in register j t t+ n 1 equals ∈{− − } the contents of this register after the t-th step of M . The second letter is equal to # for that register read by the head of M, all other second letters equal B . The head of M[′] is at the left mark (#[;] #) .


-----

**273**

###### In O(n) steps the ˝0 -th step˝ can be simulated. For the simulation of the t-th step M[′] has to know the state q of M . The left mark is shifted by one position to the left, then the head of M[′] turns to

;
###### the right until it finds the marked register (a #) . M[′] evaluates in

; ; ;
###### its central unit δ(q a) = (q[′] a[′] d), it bears in mind q[′] instead of q,

;

###### replaces the contents of the register by (a[′] B), if d = R, and by

;

###### (a[′] #), if d = L or d = N . If d = R, the next register to the right

; ;
###### with contents (b B) is marked by (b #) in the next step. One goes

;
###### right to the right mark (# #) which is shifted one position to the

;

###### right. The head turns back to the left. If d = L, (a[′] #) is replaced

; ;

###### by (a[′] B), and the register to the left containing (a[′′] B) is marked by

; ;

###### (a[′′] #) . The simulation stops when the left mark (# #) is reached.
 M[′] is oblivious, and the t-th computation step is simulated in O(t+n) steps. Altogether t[′](n) = O(t(n)[2]) for the running time of M[′] . A more efficient simulation is due to Fischer and Pippenger ((73) and (79)) (see also Schnorr (76 a)).


###### THEOREM 2.2 : A deterministic Turing machine M with time com- plexity t(n) can be simulated by an oblivious Turing machine M[′] with time complexity O(t(n) log t(n)) .

 Proof : Again we use a step-by-step simulation. We shift the in- formation of the tape in such a way that each step is ˝simulated in register 0 ˝. A move of the head to the right (left) is simulated by a shift of the information to the left (right). This idea again leads to an O((t(n)[2]) algorithm. To improve the running time we divide the information into blocks such that a few small blocks have to be shifted often, but large blocks have to be shifted rarely.
 We like to shift a block of length l = 2[m] in time O(l ) l positions to the right or left. This can be done by an oblivious Turing machine with 3 tapes. One extra tape is used for adding always 1 until the sum equals l which is stored on a second track of the tape. The second extra tape is used to copy the information.


-----

**274**

###### On the working tape we use 3 tracks, namely the alphabet (Σ # )[3] for a new letter # . If a register with contents a Σ ∪{ } ∈

; ;
###### is scanned for the first time, this contents is identified with (a # #) .

; ; Z
###### Each track j ∈{1 2 3} is divided into blocks B[j]i [(i][ ∈] ) where B[j]0 [con-] tains position 0 of track j and B[j]i [for i][ ̸][= 0 contains the 2][|][i][|−][1][ positions]

; : : : ;    - ; : : : ; <

###### 2[i][−][1] 2[i] 1 if i 0 or (2[|][i][|] 1) 2[|][i][|−][1] if i 0 of track j . A
 − − − − block is called empty when it contains only #’s and is called full when

;

###### it contains no # . The segment Si consists of the blocks B[1]i B[2]i [and]
 B[3]i [. A segment is called clean if the number of full blocks is 1 or 2 . At] the beginning all blocks are either full or empty, and all segments are clean. Clean segments contain some information and provide space for further informations. They serve as a buffer.
 The program sim(k) simulates 2[k] steps of M . We demand that the following statements hold after each simulation step.

 (1) Each block is either full or empty.

 (2) The contents of the tape of M after t computation steps can be read after t simulation steps by reading the full blocks B[j]i [according]

;
###### to the lexicographical order on the pairs (i j) .

 (3) The head of M[′] scans register 0, segment S0 . In the first track of this register is the information that M reads at that time.
 (4) During the simulation of 2[m] steps the head only visits the segments

; : : : ; ; : : : ;

###### S−(m+1) Sm+1 . At the end of the simulation S−m Sm are
 clean, and the number of full blocks of S−(m+1) (or Sm+1) is at most by 1 larger or smaller than at the beginning.


###### At the beginning of the simulation (1) – (4) are fulfilled. sim(0) is a simple program which easily can be performed obliviously. M[′] knows the state q of the simulated machine M and reads in the first track of

; ; ;
###### S0 the same information a as M does. Let δ(q a) = (q[′] a[′] d) . M[′] bears
 q[′] in mind instead of q . It replaces in the first track a by a[′] . If d = L, the letter in the last full block of S−1 is transmitted to the first block of S0, all informations in S0 are transmitted from B[j]0 [to B]0[j+1] (j ≤ 2) . If now B[3]0 [is full, its information is transmitted to B]1[1] [, the information]


-----

**275**

###### of B[j]1 [is transmitted to B]1[j+1] (j ≤ 2) . If d = R, the contents of B[1]0 is transmitted to the last empty block of S−1, the information of B[j]0 (j ≥ 2) is transmitted to B[j]0[−][1] . If B[1]0 [is empty now, the information of] B[1]1 [is transmitted to B]0[1] [, the information of B]1[j] [(j][ ≥] [2) is transmitted] to B1[j][−][1] . At the end the head is at position 0 . All these transmissions

;

###### are possible, since S−1 S0 and S1 are clean at the beginning. Hence
 S0 is clean at the end of sim(0) . Altogether sim(0) is an oblivious program of constant time complexity fulfilling (1) – (4).

        ###### sim(k) is defined for k 0 recursively by

:
###### sim(k) : sim(k 1); clean(k); sim(k 1); clean(k) (2.4) − −

 The program clean(k) should clean up S−k and Sk . We have seen that after the application of sim(0) S−1 and S1 can be unclean. Let us investigate sim(k) as a non recursive procedure. sim(k) consists of 2[k] simulation steps sim(0) where the t-th step is followed by

; : : : ;
###### clean(1) clean(l ) for l = max m 2[m][−][1] divides t . By counting { | } the number of simulation steps, it is easy to see which clean-procedures have to be performed.

 We explain how clean(k) cleans up Sk (a similar program cleans S k) . The head turns to the right until it scans the first register of
_−_
###### Sk . This can be done easily by counting the number of steps on an extra tape. We distinguish three cases. In order to have the program oblivious, the head simulates all three cases, but the actions are per- formed only for the right case. If Sk is clean, there is nothing to be done. If all blocks of Sk are empty, the first block of Sk+1 is broken into two pieces and transmitted to the first two blocks of Sk . The contents of B[j]k+1 [(j][ ≥] [2) is transmitted to B]k+1[j][−][1] [. If all blocks of S][k][ are] full, the last two blocks are concatenated and transmitted to the first block of Sk+1 . The contents of B[j]k+1 [(j][ ≤] [2) is transmitted to B]k+1[j+1] [.]

 We prove by induction on k that sim(k) fulfils (1) – (4). This has

                 ###### been proved already for k = 0 . We investigate sim(k) for k 0 . By induction hypothesis sim(k − 1) fulfils (1) – (4). By (4) S−(k+1) and Sk+1 are clean, since they are not visited during sim(k − 1) . Hence


-----

**276**

; : : : ;

###### clean(k) works. Afterwards S−k Sk are clean, and by induction
 hypothesis sim(k 1) works correctly. Afterwards clean(k) is called − for the second time. This call for clean(k) would cause problems only if Sk is empty and Sk was empty before the first call of clean(k) or Sk is full in both situations. In the first case Sk+1 may be empty now, in the second case Sk+1 may be full now. But such situations do not occur. If Sk was empty before the first call of clean(k), we have filled it up with two full blocks. Because of (4) the number of full blocks is decreased by the second call of sim(k − 1) at most by 1, and Sk cannot be empty again. If Sk was full before the first call of clean(k), we have cleared out two blocks. Because of (4) the number of full blocks is increased by the second call of sim(k − 1) at most by 1, and Sk cannot be full again. Hence clean(k) works. Altogether sim(k) works and fulfils (1) – (4).

 By our considerations sim( log t(n) ) is an oblivious Turing ma- ⌈ ⌉ chine M[′] simulating M . The running time is O(t(n)) for all calls of sim(0) and O(2[k]) for each call of clean(k) . Since clean(k) is called only once for 2[k] simulation steps, the whole time spent for clean(k)

     ###### is O(t(n)) . If k log t(n), sim( log t(n) ) does not call clean(k) at ⌈ ⌉ ⌈ ⌉ all. Hence the running time of M[′] is t[′](n) = O(t(n) logt(n)) . 2

 If we want to simulate the Turing machine M by circuits, we can assume that s(n) is known to the circuit designer. We use markers ## in the registers s(n) and s(n) which do not change M since M never − reaches these registers. The simulating oblivious Turing machine can

         ###### omit all calls of clean(k) for k ⌈log s(n)⌉ . Information from S−(k+1) or Sk+1 will never be used in register 0 . Then the running time of the oblivious Turing machine is only O(t(n) log s(n)) . From these considerations, Theorem 2.1 and Theorem 2.2 we obtain the main result of this chapter.

 THEOREM 2.3 : If L can be decided by a deterministic Turing machine in time t(n) and space s(n), fn ∈ Bn defined by fn[−][1][(1) =]


-----

**277**

;
###### L 0 1 can be computed by a circuit of size O(t(n) log s(n)) . ∩{ }[n]

 9.3 The simulation of Turing machines by circuits: space and depth

 The circuit we have constructed in 2 has large depth § O(t(n) logs(n)), since we have simulated the sequential computation of the given Turing machine step-by-step. Here we design circuits of small depth with respect to the space complexity of the Turing ma- chine.
 If fn Bn depends essentially on all n variables, the space complex- ∈ ity of each Turing machine for the union of all fn[−][1][(1) fulfils s(n)][ ≥] [n .] The Turing machine has to read all inputs, but the space is not used for work. Therefore we assume that the input is given on a read-only input tape. The space complexity s(x) for input x is the number of different registers that the Turing machine scans on the working tape, if x is the input. Now it is possible that Turing machines need only sublinear space s(n) = o(n) .

 For example the language of all sequences consisting of ones only can now be decided with 1 register (for the output) on the working tape. The corresponding Boolean functions fn(x) = x1 xn have ∧· · · ∧ circuit depth log n . All functions depending essentially on n vari- ⌈ ⌉ ables have depth Ω(log n) . Hence it is not astonishing that the depth of our circuit depends on

;
###### l (n) = max s(n) log n (3.1) { ⌈ ⌉}

 and not only on s(n) . Before we formulate the main result of this sec- tion (Borodin (77)), we prove a simple connection between the time complexity and the space complexity of Turing machines. If a Tur- ing machine runs too long on a short working tape, it reaches some configuration for the second time. This computation cycle is repeated infinitely often, and the machine never stops. Let the registers of


-----

**278**

; : : : ;
###### the working tape be numbered by 1 s(n) when the input x has length n . Then a configuration is a vector


; ; ; : : : ;
###### (q i a1 as(n)


;
###### j) (3.2)


; : : : ;
###### where q Q is the current state, i 1 n is the position of the ∈ ∈{ }

; : : : ;
###### head on the input tape, j 1 s(n) is the position of the head ∈{ } on the working tape, and ak ∈ Σ is the contents of register k . Hence k(n), the number of different configurations, fulfils

:
###### log k(n) log Q + log n + s(n) log Σ + log s(n) (3.3) ≤ | | | |

  ###### If t(n) k(n), the Turing machine runs for some input in a cycle and does not stop at all on this input. Hence by (3.3)

:
###### log t(n) log k(n) = O(l (n)) (3.4) ≤

 THEOREM 3.1 : If L can be decided by a deterministic Turing machine in time t(n) and space s(n), then


###### D(fn) = O(l (n) logt(n)) = O(l (n)[2]) for fn[−][1][(1) = L][ ∩{][0][;][ 1][}][n]


:
###### (3.5)


###### Proof : We assume that the Turing machine does not stop in q[∗], but that it remains in q[∗] and does not change the contents of the registers of the working tape. Then the computation on x can be described by

; : : : ;
###### the sequence of configurations k0(x) kt(n)(x) and x ∈ L iff regis- ter 1 of the working tape contains a 1 in kt(n)(x) .
 For each configuration k(x) the direct successor k[′](x) is unique. k[′](x) does not depend on the whole input vector but only on that bit xi which is read by the Turing machine in configuration k(x) . Let A = A(x) be the k(n) × k(n)-matrix where ak;k[′] = 1 (k, k[′] confi- gurations) iff k[′] is the direct successor of k on input x . Since ak;k[′] depends only on one bit of x, A can be computed in depth 1 . Let A[i] = (a[i]k;k[′][) be the][ i] [-th power of A with respect to Boolean matrix] multiplications. Since


###### a[i]k;k[′][ =][ �] k; k[′′][ ∧] [a][k][′′]

k[′′][ a][i][−][1]


;k[′]


;
###### (3.6)


-----

**279**

###### a[i]k;k[′][ = 1 iff on input x and starting in configuration k we reach con-] figuration k[′] after t steps. We compute by log t(n) Boolean matrix ⌈ ⌉ multiplications A[T] for T = 2[⌈][log t(n)][⌉] . The depth of each matrix mul- tiplication is log k(n) + 1 . Finally ⌈ ⌉


###### fn(x) = a[T]k0
 [�]

k∈Ka


; k (3.7)


###### for the starting configuration k0 and the set of accepting con- figurations Ka . Altogether fn(x) can be computed in depth 1 + log t(n) ( log k(n) + 1) + log k(n) . The theorem follows ⌈ ⌉ ⌈ ⌉ ⌈ ⌉ from (3.4). 2

 9.4 The simulation of circuits by Turing machines with oracles

 Each Boolean function fn Bn can be computed by a Turing ma- ∈ chine in n steps without working tape. The machine bears in mind the whole input x and accepts iff x ∈ fn[−][1][(1) . But the number of states of] the machine is of size 2[n] and grows with n . We like to design a Tur- ing machine which decides L, the union of all fn[−][1][(1) where f][n] [∈] [B][n] [.] But L can be non recursive even if C(fn) is bounded by a polynomial. A simulation of circuits by Turing machines is possible if we provide the Turing machine with some extra information depending on the length of the input but not on the input itself (Pippenger (77 b),(79), Cook (80)).

 DEFINITION 4.1 : A non uniform Turing machine M is a Turing machine provided with an extra read-only tape (oracle tape) contain- ing for inputs x of length n an oracle an . The computation time t(x) is defined in the usual way, the space s(x) is the sum of the num- ber of different registers on the working tape scanned on input x and ⌈log |an|⌉ .


-----

**280**

###### The summand ⌈log |an|⌉ for the space complexity is necessary for the generalization of the results of 3. We have to add m § ∈

; : : : ;
###### {1 |an|}, the position of the head on the oracle tape, to a config
; ; ; : : : ; ;
###### uration vector k = (q i a1 as(n) j) (see (3.2)). If the space com plexity is defined as done in Definition 4.1, the estimation (3.4) holds also for non uniform Turing machines. Hence the results of 2 and § 3 hold also for non uniform Turing machines. §


###### THEOREM 4.1 : If cn = C(fn) = Ω(n), L, the union of all fn[−][1][(1),] can be decided by a non uniform Turing machine where t(n) = O(c[2]n[)] and s(n) = O(cn) .

 Proof : The oracle an is an encoding of an optimal circuit Sn for

; : : : ;
###### fn Bn . We number the inputs and gates of Sn by 1 n + cn . ∈ A gate is encoded by its number, its type and the numbers of its direct predecessors. The encoding of a gate has length O(log cn), the encoding an of Sn has length O(cn log cn), hence log |an| = O(log cn) .
 The Turing machine can now simulate the circuit given in the oracle step-by-step. After the simulation of i 1 gates, the results of these − gates are written on the working tape. The i -th gate is simulated by looking for the inputs of the gate (on the input tape or on the working tape), by applying the appropriate ω ∈ B2 to these inputs and by writing the result on the working tape. It is easy to see that each gate can be simulated in time O(cn) and we obviously need cn registers on one working tape for the results of the gates and O(log cn) registers on another working tape for counting. 2

 THEOREM 4.2 : If dn = D(fn) = Ω(log n), L, the union of all fn[−][1][(1), can be decided by a non uniform Turing machine where t(n) =] O(n 2[d][n]) and s(n) = O(dn) .

 Proof : The oracle an is an encoding of a depth optimal formula Fn for fn . Formulas can be simulated with very little working tape, since


-----

**281**

###### the result of each gate is used only once. We number the gates of a formula of depth dn in postorder. The postorder of a binary tree T with left subtree Tl and right subtree Tr is defined by

:
###### postorder(T) = postorder(Tl ) postorder(Tr) root(T) (4.1)

; ; : : : ;

###### A gate is encoded by its type and numbers il ir ∈{0 n} . If
 il = 0, the left direct predecessor is another gate and, if il = j ∈

; : : : ;
###### {1 n}, the left direct predecessor is the variable xj . In the same way ir is an encoding of the right predecessor. Each gate is encoded by O(log n) bits. Since formulas of depth d contain at most 2[d] 1 − gates, log |an| = O(dn) .

 The Turing machine simulates the formula given in the oracle step- by-step. If we consider the definition of the postorder, we conclude that gate G has to be simulated immediately after we have simulated the left and the right subtree of the tree rooted at G . If we erase all results that we have already used, only the results of the roots of the two subtrees are not erased. Hence the inputs of G can be found in the following way. The value of variables is looked up on the input

; ;
###### tape, the result of the j 0 1 2 inputs which are other gates are ∈{ } the last j bits on the working tape. These j bits are read and erased, and the result of G is added at the right end of the working tape.

 Since each gate can be simulated in time O(n) the claim on the computation time of the Turing machine follows. It is easy to prove by induction on the depth of the formula that we never store more than dn results on that working tape where we store the results of the gates. We use O(log n) registers on a further working tape for counting. Hence the space complexity s(n) of the Turing machine is bounded by O(dn) . 2

; N N
###### DEFINITION 4.2 : Let T S : . →
 i) SIZE(T) or DEPTH(S) is the class of sequences fn Bn which can ∈ be computed by circuits of size O(T(n)) or depth O(S(n)) resp.


-----

**282**

;
###### ii) NUTIME(T) or NUSPACE(S) is the class of languages L 0 1 ⊆{ }[∗]
 which can be decided by non uniform Turing machines in time O(T(n)) or space O(S(n)) resp.

 In 2 and Theorem 4.1 we compared the size of circuits with the § time of Turing machines. In 3 and Theorem 4.2 we have found a § tight relation between the depth of circuits and the space of Turing machines. We collect these results in the following theorem, again identifying languages and sequences of Boolean functions.

 THEOREM 4.3 : i) SIZE(T[O(1)]) = NUTIME(T[O(1)]) if T(n) = Ω(n) .
 ii) DEPTH(S[O(1)]) = NUSPACE(S[O(1)]) if S(n) = Ω(log n) .

 Savage (72) considered another type of non uniform Turing ma- chines. These Turing machines compute only a single Boolean function fn Bn . The complexity C(n) of the Turing machine is measured by ∈ p t(n) logs(n) where p is the number of bits in the Turing machine ∥ ∥ ∥ ∥ program. Such a Turing machine can be simulated by a circuit of size O(C(n)), the proof makes use of the ideas in the proof of Theorem 2.3.

 9.5 A characterization of languages with polynomial circuits

 Based on the knowledge gained in 2 – 4 we prove a general § § characterization of languages with polynomial circuits (Karp and Lip- ton (80)). This characterization is used later for a simulation of prob- abilistic Turing machines by circuits.

N
###### DEFINITION 5.1 : Let F be a class of functions h : Σ[∗] . Poly → is the class of all h where h(n) is bounded by a polynomial. Let C | |

; ; ;
###### be a class of languages L 0[;] 1 and let : ( 0 1 )[2] 0 1 ⊆{ }[∗] ⟨· · ⟩ { }[∗] →{ }[∗]


-----

**283**

; ;
###### be an injective encoding where x y = O( x + y ) and (x y) can be |⟨ ⟩| | | | |

;
###### computed in time O( x + y ) from x y . Then | | | | ⟨ ⟩

= ; ; ;
###### C F = L 0 1 B C h F : L = x x h( x ) B { ⊆{ }[∗] | ∃ ∈ ∈ { | ⟨ | | ⟩∈ }} (5.1)

 is the class of languages L which are relative to some oracle function h F in the class C . ∈

=
###### For P Poly (see Def. 1.1 for the definition of P) the oracle word of polynomial length can be the encoding of a circuit of polynomial size. Hence the following theorem (Pippenger (79)) is not surprising.

=
###### THEOREM 5.1 : L ∈ P Poly iff fn defined by fn[−][1][(1) = L][ ∩{][0][;][ 1][}][n]
 has polynomial circuit size.

=
###### Proof : If L P Poly, then ∈

;
###### L = x x h( x ) B (5.2) { | ⟨ | | ⟩∈ }

 for some B P and h Poly . Hence there is some non uniform ∈ ∈ polynomially time bounded Turing machine with oracle h(n) deciding

;
###### whether x h( x ) B . This Turing machine M decides L by (5.2). ⟨ | | ⟩∈ By Theorem 2.3 M can be simulated by circuits of polynomial size.
 If C(fn) ≤ p(n) for some polynomial p, let h(n) be the standard encoding of a circuit Sn for fn of size p(n) . Let B be the set of all

;
###### x y where y is an encoding of a circuit on x inputs computing 1 ⟨ ⟩ | | on input x . It is an easy exercise to prove that B P . By definition ∈

; =
###### L = x x h( x ) B and hence L P Poly . 2 { | ⟨ | | ⟩∈ } ∈

=
###### It is interesting that also NP Poly can be described by properties of circuits.

;
###### DEFINITION 5.2 : The language L 0 1 has polynomial gen- ⊆{ }[∗]

N
###### erating circuits Sn (n ∈ ) if k(n), the number of inputs of Sn, and


-----

**284**

###### g(n), the number of gates of Sn, are bounded by a polynomial and if

; ; : : : ; ;
###### for some selected gates or inputs G(0 n) G(n n) of Sn
 L ∩{0; 1}[n] = �(res G(1;n)(a); : : : ; res G(n;n)(a)) | a ∈{0; 1}[k(n)] ; (5.3)
 res G(0;n)(a) = 1�:


###### We explain this definition by the following considerations. Let L have polynomial circuits, i.e. there are circuits Sn of polynomial size for fn where fn[−][1][(1) = L][ ∩{][0][;][ 1][}][n][ . Then these circuits are also generating.]

; : : : ; ; ; : : : ; ;

###### We choose the inputs x1 xn as G(1 n) G(n n) and the output

;
###### gate as G(0 n) . Then (5.3) is fulfilled by definition of fn . This result is also a corollary of the following theorem (Sch¨oning (84), Yap (83)),

= =
###### since P Poly NP Poly. ⊆

=
###### THEOREM 5.2 : L NP Poly iff L has polynomial generating ∈ circuits.

=
###### Proof : If L NP Poly, then ∈

;
###### L = x x h( x ) B (5.4) { | ⟨ | | ⟩∈ }

 for some B ∈ NP and h ∈ Poly . Since NP = Σ1, there is by Theo- rem 1.1 some L[′] P and some polynomial p such that ∈

; ; ; :
###### L = x y 0 1 : x h( x ) y L[′] (5.5) { | ∃ ∈{ }[p(][|][x][|][)] ⟨ | | ⟩∈ }

 Since L[′] ∈ P, we find circuits Sn of polynomial size q(n) working on

;
###### n + p(n) input variables (x y) and the oracle h(n) as constant input

; ;
###### and computing 1 iff ⟨x h(n) y⟩∈ L[′] . Sn are generating circuits for L[′] .

; ; : : : ; ; ; : : : ; ;
###### We define G(1 n) G(n n) as the inputs x1 xn and G(0 n) as
 the output gate of Sn .
 If Sn is a sequence of polynomial generating circuits for L, we define

; ; : : : ; ;
###### h(n) as the encoding of Sn, G(0 n) G(n n) and k(n) . Then h ∈

;
###### Poly. Let B be the set of all x y where for n = x y is the encoding ⟨ ⟩ | |

; ; : : : ; ;
###### of a circuit on k(n) inputs and of n+1 gates G(0 n) G(n n) and of k(n) such that there is an input a ∈{0; 1}[k(n)] for which res G(0;n)(a) = 1


-----

**285**

###### and res G(i;n)(a) = xi for 1 ≤ i ≤ n . B ∈ NP, since a non deterministic Turing machine guesses a correctly. Moreover

;
###### L = x x h( x ) B (5.6) { | ⟨ | | ⟩∈ }

=
###### and hence L NP Poly. 2 ∈

= =
###### It is an open problem whether P Poly = NP Poly. ̸

 9.6 Circuits and probabilistic Turing machines

 DEFINITION 6.1 : For probabilistic Turing machines the set of states Q contains three selected states qa, qr and q? . If one of these states is reached, the machine stops. If the stopping state is qa, the input is accepted (output 1), if it is qr, the input is rejected (output 0), if it is q?, the machine does not decide about the input (no output).

; ; ;

###### If q ̸∈{qa qr q?}, δ(q a) ∈ (Q × Σ × {R,L,N})[2] . Each of the two

=
###### admissible computation steps is performed with probability 1 2 .


###### Probabilistic Turing machines can simulate deterministic computa
;
###### tion steps. Then both triples in δ(q a) are the same. The output M(x) of a probabilistic Turing machine M on input x is a random variable. The running time t(n) is the length of the longest computation path on inputs of length n .

 DEFINITION 6.2 : Let χL(x) = 1 iff x ∈ L .

;
###### i) PP (probabilistic polynomial) is the class of languages L 0 1, ⊆{ }[∗] such that there is some ppTm (polynomially time bounded prob- abilistic Turing machine) M where for all x

       - =
###### Prob(M(x) = χL(x)) 1 2 (Monte Carlo algorithms). (6.1)


-----

**286**

###### ii) BPP (probabilistic polynomial with bounded error) is the class of

;
###### languages L 0 1 such that there is some ppTm M and some ⊆{ }[∗]

  ###### ε 0 where for all x

       - = :
###### Prob(M(x) = χL(x)) 1 2 + ε (6.2)

;
###### iii) R (random) is the class of languages L 0 1 such that there ⊆{ }[∗] is some ppTm M where

      - =
###### Prob(M(x) = 1) 1 2 for x L and (6.3) ∈

:
###### Prob(M(x) = 0) = 1 for x L ̸∈

 iv) ZPP (probabilistic polynomial with zero error) is the class of lan
;
###### guages L 0 1 such that there is some ppTm M where ⊆{ }[∗]

              - =
###### Prob(M(x) = 0) = 0 and Prob(M(x) = 1) 1 2 for x L ∈
 and (6.4)

              - =
###### Prob(M(x) = 1) = 0 and Prob(M(x) = 0) 1 2 for x L ̸∈

 (Las Vegas algorithms).

 We do not like to discuss the quality of different casinos, but we state that Las Vegas algorithms never tell lies, whereas Monte Carlo algorithms may compute wrong results on nearly half of the compu- tation paths. It is easy to prove (see Exercises) that

:
###### P ZPP R BPP PP and R NP (6.5) ⊆ ⊆ ⊆ ⊆ ⊆

 The error probability of BPP algorithms can be decreased by inde- pendent repetitions of the algorithm.

 LEMMA 6.1 : Let M be a ppTm for L BPP fulfilling (6.2). Let ∈ Mt (t odd) be that probabilistic Turing machine which simulates M for t times independently and which accepts (rejects) x if more than

=
###### t 2 simulations accept (reject) x and which otherwise does not decide about x . Then

       ###### Prob(Mt(x) = χL(x)) 1 − 2[−][m] if (6.6)


-----

**287**


###### 2 t (6.7) ≥− �
 log 1 4ε[2][�] [(m][ −] [1)][:] −

=
###### Proof : Let E be an event whose probability p is larger than 1 2 + ε . Then


###### p[i](1 p)[i] −


< = = =
###### (1 2 + ε)[i](1 2 ε)[i] = (1 4 ε[2])[i] − −


:
###### (6.8)


=
###### Let ai for i ≤ t 2 be the probability that E happens exactly i times in t independent repetitions of the experiment. Then


###### �t� ai = p[i](1 − p)[t][−][i] i


###### �t�

< =

###### (1 4 ε[2])[t][=][2] −
 i


:
###### (6.9)


###### Hence
 �t�

      - = �
###### Prob(Mt(x) = χL(x)) 1 − (1 4 − ε[2])[t][=][2] (6.10)
 i

0 i t=2
_≤_ _≤⌊_ _⌋_

= = :
###### = 1 (1 4 ε[2])[t][=][2] 2[t][−][1] = 1 (1 2)(1 4ε[2])[t][=][2] − − − −

 Choosing t according to (6.7), (6.6) follows from (6.10). 2

 If the number of repetitions is bounded by a polynomial, Mt is polynomially time bounded. Adleman (78) proved that languages L ∈ R have polynomial circuits. Bennett and Gill (84) could generalize this result.

 THEOREM 6.1 : If L ∈ BPP, fn defined by fn[−][1][(1) = L][ ∩{][0][;][ 1][}][n][ has] polynomial circuit size.

 Proof : We look for a computation path which is correct for all inputs of the same length. Such a computation path will be used as an oracle.

 We apply Lemma 6.1. This ensures the existence of a ppTm M for L whose error probability is bounded by 2[−][2][|][x][|] . W.l.o.g. M stops for all inputs x of length n after exactly p(n) computation steps where p is a polynomial. A computation path is described by a vector

;
###### a ∈{0 1}[p(n)] . In step t the (at + 1)-th possible computation step


-----

**288**

;
###### is performed. There are 2[n+p(n)] pairs (x a) of inputs of length n and computation paths a of length p(n) . For fixed x the number of com- putation paths leading to wrong results is bounded by 2[p(n)][−][2n] . Hence

;
###### the number of pairs (x a) where a is a wrong computation path for input x is bounded by 2[p(n)][−][n] . Since 2[p(n)] 2[p(n)][−][n] 1, there is at − ≥

;
###### least one computation path h(n) 0 1 which is correct for all ∈{ }[p(n)] inputs of length n. By definition h Poly. Let ∈

; ; :
###### B = x y y 0 1, M(x) = 1 on computation path y {⟨ ⟩| ∈{ }[p(][|][x][|][)] } (6.11)

 Then B P, since a deterministic Turing machine can simulate di- ∈ rectly a probabilistic Turing machine on a given computation path. Hence

; =
###### L = x x h( x ) B P Poly (6.12) { | ⟨ | | ⟩∈ } ∈
 and, by Theorem 5.1, fn defined by fn[−][1][(1) = L][∩{][0][;][ 1][}][n][ has polynomial] circuit size. 2

 BPP and R contain languages which are not known to be contained in P .

 9.7 May NP-complete problems have polynomial circuits ?

 If NP = P, all NP-complete problems have polynomial circuits. But let us assume like most of the experts do that NP = P . Never- ̸ theless there is the possibility that NP-complete languages have poly- nomial circuits. This would imply for problems in NP that non uni- form circuits are much more powerful than uniform Turing machines. Again, hardly anyone expects such a result. We corroborate this ex- pectation in this section. If, for example, SAT (see 1) has polyno- § mial circuits, then Stockmeyer’s hierarchy collapses at an early stage.


-----

**289**

###### Again, the experts do not expect that. But beware of experts. The experts also believed that non uniform algebraic decision trees cannot solve NP-complete problems in polynomial time. However Meyer auf der Heide (84) proved that the knapsack problem can be solved by algebraic decision trees in polynomial time.

 DEFINITION 7.1 : A language L is called polynomially self-reducible if it can be decided by a polynomially time bounded Turing machine with oracle L which asks its oracle for inputs of length n only for words

<
###### of length m n .

 LEMMA 7.1 : SAT is polynomially self-reducible.

 Proof : Let the input be a set of clauses where at least one clause includes x1 or x1 . Then we replace at first x1 by 1 and ask the oracle whether the new set of clauses can be satisfied. Afterwards we repeat this procedure for x1 = 0 . We accept iff one of the oracle questions is answered positively. 2

;
###### For a language L we denote by L≤n the union of all Lm = L∩{0 1}[m]

;
###### for m n . Let L(M) or L(M B) be the language decided by the ≤ Turing machine M or the Turing machine M with oracle B resp.

 LEMMA 7.2 : Let A be polynomially self-reducible, and let M be a polynomially time bounded Turing machine according to Defini
;
###### tion 7.1. If L(M B)≤n = B≤n, then A≤n = B≤n .

 Proof : By induction on n . If n = 0, M is not allowed to ask the oracle. Hence it does the same for all oracles.


; ;
###### A≤0 = L(M A)≤0 = L(M B)≤0 = B≤0


:
###### (7.1)


; ;
###### If L(M B)≤n+1 = B≤n+1, also L(M B)≤n = B≤n and by the induction hypothesis A≤n = B≤n . Since M asks on inputs x, where |x| ≤ n + 1,


-----

**290**

###### the oracle only for words y, where y n, | | ≤

; ; ;
###### A≤n+1 = L(M A)≤n+1 = L(M A≤n)≤n+1 = L(M B≤n)≤n+1 (7.2)


;
###### = L(M B)≤n+1 = B≤n+1


:


###### 2

 This lemma serves as technical tool for the proof of the following theorem (Balcaz´ar, Book and Sch¨oning (84)). The complexity classes Σk and Σk(A) are defined in § 1.

=

###### THEOREM 7.1 : Let A ∈ Σk Poly be polynomially self-reducible.
 Then Σ2(A) ⊆ Σk+2 .

 Before we prove this theorem, we use it to prove the announced result due to Karp and Lipton (80).

 THEOREM 7.2 : If SAT has polynomial circuits, then Σ3 = Σ2 and the Stockmeyer hierarchy collapses at the third stage.


=
###### Proof : If SAT has polynomial circuits, then SAT P Poly = ∈

=

###### Σ0 Poly (Theorem 5.1). Hence Σ2(SAT) ⊆ Σ2 ⊆ Σ3 (Theorem 7.1
 and Lemma 7.1). Since SAT is NP-complete, Σ3 = NP(NP(NP)) = Σ2(SAT) . Hence Σ2 = Σ3 . 2

 Proof of Theorem 7.1 : Let M be a Turing machine deciding A and

=

###### fulfilling the properties of Definition 7.1. Since A ∈ Σk Poly, there
 are some language B ∈ Σk and some h ∈ Poly such that


;
###### A≤n = {x | ⟨x h(n)⟩∈ B}≤n


:
###### (7.3)


;
###### Also Bw = {x | ⟨x w⟩∈ B} ∈ Σk . Let L[′] ∈ Σ2(A) . We have to prove L[′] ∈ Σk+2 . By Theorem 1.1 there is a polynomially time bounded Turing machine M[′] with oracle A such that


-----

; ;
###### L[′] = {x | (∃ y)q(∀ z)q : ⟨x y z⟩∈ L(M[′]


**291**

; :
###### A) (7.4) }


###### Here q is a polynomial where q( x ) is a bound for y and z . Since | | | | | | M[′] is working in polynomial time r( x ), also the length of each oracle | | word is bounded by r( x ) . Let p[′] be the polynomial p r . We want | | ◦ to prove that

; ; ; ;
###### L[′] = {x | (∃ w)p[′] : ((∀ u)r R(u w) ∧ (∃ y)q (∀ z)q S(w x y z))} (7.5)

; � ; �
###### where R(u w) holds iff u ∈ Bw ⇔ u ∈ L(M Bw) and


; ; ; ;
###### S(w x y z) holds iff x y L(M[′] ⟨ ⟩∈


;
###### Bw) .


;
###### R S ∈ P(Σk) since Bw ∈ Σk . (7.5) implies

; ; ; ; :
###### L[′] = {x | (∃ w)p[′] (∃ y)q (∀ u)r (∀z)q : R(u w) ∧ S(w x y z)} (7.6)

 Hence L[′] ∈ Σk+2 by Theorem 1.1. We still have to prove (7.5).

;
###### We claim that the predicate ˝ (∀ u)rR(u w) ˝ is equivalent to A≤r(n) = (Bw)≤r(n) . Since |u| ≤ r(n), the given predicate is equiv
;
###### alent to (Bw)≤r(n) = L(M Bw)≤r(n) . This implies A≤r(n) = (Bw)≤r(n) by Lemma 7.2. The other part follows from the definition of M .

 By (7.3) there is always some w where w p[′]( x ) and | | ≤ | |

;
###### ˝ (∀ u)r R(u w) ˝ holds. Only for such words we have to consider the second predicate. Then we can replace the oracle Bw by A . By (7.4)

; ; ;
###### x ∈ L[′] iff ˝ (∃ y)q (∀ z)q S(w x y z) ˝ holds. This proves (7.5). 2

 Sch¨oning (83) introduced two hierarchies between P and NP . Ko and Sch¨oning (85) proved for the so-called ˝low-hierarchy˝ (see Ex- ercises), that languages A NP with polynomial circuits are already ∈ contained in the third level of this hierarchy.


-----

**292**

###### 9.8 Uniform circuits

 We have simulated deterministic non uniform Turing machines and also probabilistic Turing machines efficiently by circuits. Circuits can be simulated efficiently only by non uniform Turing machines. Instead of considering the more powerful non uniform Turing machines, we ask for restricted circuits such that these so-called uniform circuits can be simulated efficiently by (uniform) Turing machines. We only give a brief introduction (without proofs) to this subject.

 The standard encoding SCn of a circuit Sn is the encoding of its gates by the type of the gate and the numbers of the direct predecessors (see § 4). If n → SCn can be computed efficiently with respect to n, then the circuits Sn can be simulated efficiently (again see § 4). There are a lot of possibilities how we can define what ˝efficient computation of n → SCn ˝ means.

 DEFINITION 8.1 : A sequence of circuits Sn of size cn and depth dn is called UB-uniform or UBC-uniform, if n → SCn can be computed by a Turing machine whose space is bounded by O(dn) or O(log cn) resp.

 Here B stands for Borodin (77) and C for Cook (79). Cook also introduced the classes NC and NCk (NC = Nick’s Class celebrating the paper of Pippenger (79)). These classes (with the modification of unbounded fan-in - and -gates) are important also as complex- ∧ ∨ ity classes for parallel computers. Since Ruzzo (81) characterized the classes NCk by alternating Turing machines (see Chandra, Kozen and Stockmeyer (81)), this type of Turing machines describes parallel com- puters.

;

###### DEFINITION 8.2 : NC = UBC - SIZE,DEPTH(n[O(1)] log[O(1)] n) is the
 class of languages L such that fn defined by fn[−][1][(1) = L][ ∩{][0][;][ 1][}][n][ can] be computed by UBC-uniform circuits of polynomial size and polylog


-----

**293**

###### depth (the depth is a polynomial with respect to log n) .

;

###### NCk = UBC - SIZE,DEPTH(n[O(1)] log[k] n) .

;
###### THEOREM 8.1 : If k ≥ 2, NCk = A - SPACE,TIME(log n log[k] n) is the class of languages which can be decided by an alternating Turing machine of space O(log n) and time O(log[k] n) .


###### Further definitions of uniform circuits (Ruzzo (81)) refer to the complexity of the structure of the circuits (Goldschlager (78)). For a

; : : : ;

###### gate G and p = (p1 pm) ∈{L,R}[∗] let G(p) be the gate Gm where
 G0 = G and Gi is the pi-predecessor (L = left, R = right) of Gi−1 . G(ε) = G for the empty word ε .

 DEFINITION 8.3 : The direct connection language DCL of a se
; ; ;
###### quence of circuits Sn is the set of all ⟨n g p y⟩ where g is the number

; ;
###### of some input or gate G in Sn, p ∈{ε L R} and y is the type of G if p = ε or y is the number of G(p) if p = ε . The extended connection ̸

N ;
###### language ECL of Sn (n ∈ ) is defined in the same way but p ∈{L R}[∗]
 and |p| ≤ log cn .

 DEFINITION 8.4 : Let Sn be a sequence of circuits of size cn and depth dn .
 i) Sn is called UD-uniform if DCL can be decided by Turing machines in time O(log cn) .
 ii) Sn is called UE-uniform if ECL can be decided by Turing machines in time O(log cn) .
 iii) Sn is called UE[∗]-uniform if ECL can be decided by alternating Turing machines in time O(dn) and space O(log cn) .

 THEOREM 8.2 : Let Sn be a sequence of circuits of size cn and depth dn .


-----

**294**

###### i) Sn UE-uniform ⇒ Sn UD-uniform ⇒ Sn UBC-uniform ⇒ Sn UB-uniform.

 ii) Sn UE-uniform ⇒ Sn UE[∗]-uniform ⇒ Sn UB-uniform.
 iii) Sn UBC-uniform ⇒ Sn UE[∗]-uniform if dn ≥ log[2] cn .

 These properties are easy to prove. More results have been proved by Ruzzo (81). They are summarized in the following theorem.

; ;
###### THEOREM 8.3 : Let X D E E[∗] . ∈

;

###### i) NC = UX - SIZE,DEPTH(n[O(1)] log[O(1)] n) .

;

###### ii) If k ≥ 2, NCk = UX - SIZE,DEPTH(n[O(1)] log[k] n) .


###### Hence the proposed definitions are rather robust. Only the notion of UB-uniformity seems to be too weak. Most of the circuits we have designed are uniform, many fundamental functions are in NCk for small k .

 EXERCISES

 1. An oblivious t(n) time bounded Turing machine with k tapes can be simulated by circuits of size O(t(n)) .

 2. A t(n) time bounded Turing machine with k tapes can be simu- lated by an O(t(n)[2]) time bounded Turing machine with one tape.

 3. Specify an oblivious Turing machine for sim(0) .


-----

**295**

###### 4. Estimate the size of the circuits designed in 3. §

 5. Prove (6.5).

 6. Let ACP (almost correct polynomial) be the class of languages L such that L is almost decided by a polynomial Turing machine, i.e. the number of errors on inputs of length n is bounded by a polynomial q(n) . If L ACP, L has polynomial circuits. ∈

 7. Let APT (almost polynomial time) be the class of languages L which can be decided by a Turing machine whose running time is for some polynomial p for at least 2[n] p(n) inputs of length n − bounded by p(n). If L APT, L has polynomial circuits. ∈

 8. Let Lk = {A ∈ NP | Σk(A) ⊆ Σk} (low hierarchy) and Hk = {A ∈ NP | Σk+1 ⊆ Σk(A)} (high hierarchy). Let PH be the union of all Σk . If PH ̸= Σk, then Lk ∩ Hk = ̸◦ .

 9. If PH = Σk, then Lk = Hk = NP .

 10. Let Sn be a sequence of circuits of size cn and let s(n) = Ω(log cn) . Then the following statements are equivalent : a) (n → SCn) ∈ DSPACE(s(n)) . b) ECL DSPACE(s(n)) . ∈ c) DCL DSPACE(s(n)) . ∈

;
###### 11. Prove Theorem 8.2. Hint: DSPACE(t) A-SPACE,TIME(t t[2]) . ⊆

 12. Which of the circuits designed in Ch. 3 and Ch. 6 are uniform ? Which of the functions investigated in Ch. 3 and Ch. 6 are in NC or in NCk ?


-----

**296**

###### 10. HIERARCHIES, MASS PRODUCTION AND REDUCTIONS

 10.1 Hierarchies

 How large are the ˝gaps˝ in the complexity hierarchies for Boolean functions with respect to circuit size, formula size and depth ? A gap is a non-empty interval of integers none of which is the complexity of any Boolean function. Other hierarchies are investigated in Ch. 11 and Ch. 14.

 Let B[∗]n [denote the set of all Boolean functions depending essentially] on n variables, n is fixed for the rest of this section. For any complexity measure M, let M(r) be the set of all f ∈ B[∗]n [where M(f)][ ≤] [r . The] gap problem is to find for each r the smallest increment r[′] = m(r) such that M(r) is a proper subset of M(r + r[′]) .

 We are interested in cΩ(j), l Ω(j) and dΩ(j) for binary bases Ω. Tiekenheinrich (83) generalized the depth results to arbitrary bases. Obviously cΩ(j) is only interesting for those j where CΩ(j + 1) ̸= ̸◦ and CΩ(j) ̸= B[∗]n [. For any complexity measure M, let M(B]n[∗][) be the] complexity of the hardest function in B[∗]n [with respect to M . It has] been conjectured that

 dΩ(j) = cΩ(j) = l Ω(j) = 1 for all Ωand all interesting j . (1.1)

;
###### It is easy to prove that dΩ(j) ≤ 2 and cΩ(j) l Ω(j) ≤ j + 1 (Mc- Coll (78 a)). The best results are summarized in the following theorem (Wegener (81) and Paterson and Wegener (86)).

 THEOREM 1.1 :

<
###### dΩ(j) = 1 for all Ω ⊆ B2 and ⌈log n⌉− 1 ≤ j DΩ(B[∗]n[) .] (1.2)


;
###### Ωm} . Then


###### Let Ω ∈{B2


;
###### U2


-----

**297**

###### cΩ(j) = 1 if n − 2 ≤ j ≤ CΩ(B[∗]n−1[)][;] (1.3)

< <
###### cΩ(j) ≤ n if CΩ(B[∗]n−1[)] j CΩ(B[∗]n[)] and (1.4)

<
###### l Ω(j) ≤ n if n − 2 ≤ j LΩ(B[∗]n[)][:] (1.5)

 For any complete basis Ω ⊆ B2 there is a constant k(Ω) such that

 cΩ(j) ≤ k(Ω) if n − 2 ≤ j ≤ CΩ(B[∗]n−1[)] and (1.6)

< <
###### cΩ(j) ≤ k(Ω)n if CΩ(B[∗]n−1[)] j CΩ(B[∗]n[)][:] (1.7)

 The proof of the general claim (1.2) is technically involved. (1.5)– (1.7) can be proved by the same methods as (1.3) and (1.4). Hence

;

###### we shall present the proof of (1.2)-(1.4) for the bases B2 U2 and Ωm .
 Before doing so we state some counterexamples.

 (1.1) is false for some bases and small n, and we even know an example

    ###### where cΩ(j) n . We note that B[∗]2 [= U]2[∗]
 [∪{⊕][;][ ≡}][ .]
 Ω= U2 : CΩ(U2) = 1 but CΩ(⊕) = CΩ(≡) = 3 (Theorem 3.1, Ch. 5). Therefore cΩ(1) = 2 . Similarly l Ω(1) = 2 .

; ;
###### Ω = {∧ ∨ ¬} : CΩ(U2) = 2 but CΩ(⊕) = CΩ(≡) = 4 (Red’kin (73)). Therefore cΩ(2) = 2 . Similarly l Ω(2) = 2 .

;
###### Ω= {∧ ¬} : CΩ(U2) = 4 but CΩ(⊕) = CΩ(≡) = 7 (Red’kin (73)).

          ###### Therefore cΩ(5) = 2 and cΩ(4) = 3 2 = n . Similarly l Ω(4) = 3 .

 Proof of Theorem 1.1 : The idea of the proof is to take some function f in B[∗]n [of maximal complexity and construct a chain of functions] from the constant function 0 up to f such that the circuit size cannot increase by much at any step in the chain. We then conclude that there can be no large gaps.
 Let f ∈ B[∗]n [be a function of maximal circuit size with respect to Ω.]

; : : : ;

###### Let f[−][1](1) = {a1 ar} . For the case Ω= Ωm we shall assume that


-----

**298**

<
###### the a’s are ordered in some way, so that for s t, at does not contain

; : : : ;

###### more ones than as . Let f0 0, f1 fr = f where ≡


###### fk[−][1][(1) =][ {][a][1]


; : : : ; :
###### ak} for 0 ≤ k ≤ r (1.8)


###### Obviously DΩ(f1) = ⌈log n⌉, CΩ(f1) = n − 1 and f1 ∈ B[∗]n [. For the case] Ω= Ωm each fk is monotone. If fk(a) = 1 and b ≥ a, also f(b) = 1 and i ≤ j for ai = b and aj = a . Hence fk(b) = 1 .

; : : : ;
###### For any ak = (e(1) e(n)) define the minterm
 mk(x) = x[e(1)]1 ∧· · · ∧ x[e(n)]n (1.9)

 and the monom


###### tk(x) = � xi

i e(i)=1
_|_


:
###### (1.10)


<
###### Then for 0 k ≤ r we have fk = fk−1 ∨ mk while in the monotone case we have also fk = fk−1 ∨ tk . This follows, since mk(x) = 1 iff x = ak and tk(x) = 1 iff x ≥ ak . In all cases we see that

;
###### DΩ(fk) max DΩ(fk 1) log n + 1 and (1.11) ≤ { − ⌈ ⌉}

:
###### CΩ(fk) Ck(fk 1) + n (1.12) ≤ −

 It is possible that fk ̸∈ B[∗]n [. If f][k][ depends essentially only on m vari-]

; : : : ;

###### ables, we assume w.l.o.g. that these variables are x1 xm . In

; : : : ;

###### fk = fk−1 ∨ mk or fk = fk−1 ∨ tk we replace xm+1 xn by 0 . Therefore
 (1.12) is improved to


:
###### CΩ(fk) CΩ(fk 1) + m (1.13) ≤ −

 Let p(x) = xm+1 ∧· · · ∧ xn . Then fk[∗] [= f][k][ ∨] [p][ ∈] [B]n[∗] [. Let m]k[′] [and t]k[′] [be] the subfunctions of mk and tk resp. for xm+1 = · · · = xn = 0 . Then the depth of m[′]k [∨] [p and t]k[′] [∨] [p is bounded by][ ⌈][log n][⌉] [+ 1, and the] circuit size of these functions is bounded by n − 1 . Obviously fk is a subfunction of fk[∗] [. Hence]

 DΩ(fk) ≤ DΩ(fk[∗][)][ ≤] [max][{][D][Ω][(f][k][−][1][)][;][ ⌈][log n][⌉] [+ 1][}][ + 1] (1.14)


-----

**299**

###### ≤ max{DΩ(fk[∗]−1[)][;][ ⌈][log n][⌉] [+ 1][}][ + 1] and

 CΩ(fk) ≤ CΩ(fk[∗][)][ ≤] [C][Ω][(f][k][−][1][) + n][ ≤] [C][Ω][(f]k[∗]−1[) + n][:] (1.15)

 DΩ(f1[∗][) =][ ⌈][log n][⌉] [and for any][ ⌈][log n][⌉] [+ 2][ ≤] [j][ ≤] [D][Ω][(B][∗]n[) we find] some i(j) such that DΩ(fi(j)[∗] [) = j . It is an exercise to prove the existence] of some g ∈ B[∗]n [such that D][Ω][(g) =][ ⌈][log n][⌉] [+ 1 . We have proved (1.2)] and by (1.15) also (1.4).


###### To prove our optimal result (1.3) for the lower range of circuit size we need to go up from fk−1 to fk in smaller steps. We will explain this construction only for the complete bases, since for the monotone case it is similar. Let V(h) be the set of variables on which h is depending

; : : : ;

###### essentially. We shall construct a sequence h0 hm Bn with the
 ∈ following properties.

 CΩ(hi) CΩ(hi 1) + 1 (1.16) ≤ −

;
###### CΩ(h0) = 0 CΩ(hm) = CΩ(B[∗]n 1[) + 1] (1.17)
_−_

:
###### V(hi 1) V(hi) (1.18)
_−_ _⊆_

###### Let gi ∈ B[∗]n [be the disjunction of h][i] [and all variables not in V(h][i][) .] Then CΩ(g0) = n − 1, CΩ(gm) = CΩ(B[∗]n−1[) + 1 and]

 CΩ(gi) = CΩ(hi) + n V(hi) CΩ(hi 1) + 1 + n V(hi 1) (1.19) −| | ≤ − −| − |

:
###### = CΩ(gi 1) + 1
_−_

###### For any n − 1 ≤ j ≤ CΩ(B[∗]n−1[) + 1 we find some i(j) such that] CΩ(gi(j)) = j . This proves (1.3).

; : : : ;

###### We construct h0 hm . Let f ∈ B[∗]n−1 [be of maximal circuit size.]
 Let fr = f and r = |f[−][1](1)| . We construct fk−1 as before by removing a (minimal) element of fk[−][1][(1), but now regarding f][k][ as a member] of B[∗] The effect of this is to ensure that
s(k) [where s(k) =][ |][V(f][k][)][|][ .]


-----

**300**

###### V(fk−1) ⊆ V(fk) . Then fk = fk−1 ∨ mk where mk is a minterm on the variables in V(fk) . The procedure stops after r − r[′] steps with fr[′] ≡ 0 . We note that no function fk depends essentially on xn . This variable is used as a pointer in an interpolating sequence. Let mk(x) be the conjunction of all x[e(i)]i (1 ≤ i ≤ s(k)) . Let
 fk−1;i = fk−1 ∨ (xn ∧ x[e(1)]1 ∧· · · ∧ x[e(i)]i ) for 0 ≤ i ≤ s(k): (1.20)


###### Then the sequence h0


; : : : ;
###### hm is defined as the sequence


;s(r[′]+1)


; : : : ; fr 1;s(r)
_−_


; fr;0


###### fr[′]


;0


; : : : ;
###### fr′


; : : : ; fr 1;0
_−_


:


###### (1.17) is fulfilled, since fr[′] ;0 [= x]n [, f]r;0 [= f]r [∨] [x]n [, f]r [∈] [B]n[∗]−1 [and]
 CΩ(fr) = CΩ(B[∗]n 1[) .]
_−_

###### We prove (1.16). In an optimal circuit for fk−1;i we replace xn by z = xn ∧ x[e(i+1)]i+1 . The new circuit has CΩ(fk−1;i)+1 gates. We interpret z as a new ˝variable˝ and conclude that the new circuit computes


###### fk−1 ∨ z ∧ x[e(1)]1 ∧· · · ∧ x[e(i)]i = fk−1;i+1


:
###### (1.21)


###### In an optimal circuit for fk−1;s(k) we replace xn by 1 . Then we com- pute fk (see (1.20)). Since fk;0 = fk ∨ xn, also CΩ(fk;0) ≤ CΩ(fk−1;s(k)) .
 We prove (1.18). Let s = s(k) . V(fk 1;i) is a subset of
_−_
###### {x1 ; : : : ; xs ; xn} . We regard fk−1;i as a member of Bs+1 . fk−1;i depends
 essentially on xn . Let ak be that vector which has been removed from fk[−][1][(1) for the construction of f]k[−]−[1]1[(1) . Then a][k][ ∈{][0][;][ 1][}][s][ and] fk−1;i(ak ; 0) = 0 but fk−1;i(ak ; 1) = 1 . If xn = 0, fk−1;i = fk−1 and
 fk−1;i depends essentially on all variables in V(fk−1) = {x1 ; : : : ; xs[′]}
 where s[′] = s(k − 1) . Moreover fk−1;i depends essentially on x1 ; : : : ; xi .
 If fk−1;i was not depending essentially on xj (j ≤ i) we could use the procedure for the proof of (1.16) and would obtain a circuit for fk not depending on xj . This would be a contradiction to the

; : : : ; ;

###### fact that fk depends essentially on x1 xs . For s[′′] = max{s[′] i},
 V(fk 1;i) = x1 ; : : : ; xs[′′] ; xn . Therefore V(fk 1;i) V(fk 1;i+1) and
_−_ _{_ _}_ _−_ _⊆_ _−_

###### V(fk 1;s) = x1 ; : : : ; xs ; xn = V(fk;0) . 2
_−_ _{_ _}_


-----

**301**

###### The counterexamples show that Theorem 1.1 is at least almost opti- mal. The general proof of (1.2) (Wegener (81)) is based on the assump- tion that the constants 0 and 1 are inputs of the circuit. Strangely enough, this assumption is necessary at least for small n . Let Ωbe

; ;
###### the complete basis 1 (Ring-Sum-Expansion) and let 1 be not { ∧ ⊕}

;

###### an input of the circuit. B[∗]1 [=][ {][x][1] x1}, DΩ(x1) = 0 but DΩ(x1) = 2 .
 Therefore dΩ(0) = 2 .

 10.2 Mass Production

 Test sequences for the purpose of medical research, experiments in physical sciences or inquiries in social sciences often require large sample size. It is impossible to analyze directly all data. In some pre- processing phase one performs a data reduction, i.e. the same function is applied to the data of each single test.

 DEFINITION 2.1 : The direct product f × g ∈ Bn+m;k+l of f ∈ Bn;k and g ∈ Bm;l is defined by

; ; :
###### (f g)(x y) = (f(x) g(y)) (2.1) ×

 Similarly f1 ×· · ·×fr is defined and r×f is the direct product of r copies of f .

 It is possible to compute r f by r copies of an optimal circuit for × f . We ask whether one can save gates for the mass production of f . Obviously this is not possible for simple functions like x1 xn . ∧· · · ∧ Moreover one might believe that it makes no sense to compute func- tions depending on variables of different copies of f . But we have already seen that the encoding of independent information in a com- mon bit string is useful for certain applications, see e.g. the application of the Chinese Remainder Theorem in Ch. 3.


-----

**302**

###### Let us consider medical tests. If x is the data of some person, f(x) = 1 iff this person is infected by some definite pathogenic agent. If r f has large complexity and if it is known that only a small number × of people may be infected, it is useful to compute at first whether at all any person is infected.

 DEFINITION 2.2 : The direct disjunction ∨(f × g) ∈ Bn+m of f ∈ Bn and g ∈ Bm is defined by

; :
###### (f g)(x y) = f(x) g(y) (2.2) ∨ × ∨

 Similarly ∨(f1 × · · · × fr) and ∨(r × f) are defined.

 If (r f) can be computed more efficiently than r f, we use ∨ × × the following strategy. We compute (r f) . If the output is 0, no ∨ × person is infected and we stop. Otherwise we compute (s f) for ∨ ×

<
###### some s r and some subset of persons and so on. Some remarks on how to choose good strategies are included in the monograph of Ahlswede and Wegener (86). Here we investigate the complexity of r f and (r f) . The following table shows in which situation savings × ∨ × are possible for mass production.

 C Cm L

 f f Yes No No ×
 (f f) Yes Open problem No ∨ ×

 Tab. 2.1

 It is easy to prove the results on formula size.

 THEOREM 2.1 : i) LΩ(f × g) = LΩ(f) + LΩ(g) for all f, g and Ω.
 ii) LΩ(∨(f × g)) = LΩ(f) + LΩ(g) + 1 if ∨∈ Ωand f and g are not constant.

|Col1|C C L m|
|---|---|
|f f × (f f) ∨ ×|Yes No No Yes Open problem No|


-----

**303**

###### Proof : i) Because of the fan-out restriction of formulas we need dis- joint formulas for f and g .
 ii) The upper bound is obvious since Ω. Let a f[−][1](0). By ∨∈ ∈

;
###### definition (f g)(a y) = g(y) . Therefore each formula for (f g) ∨ × ∨ × has at least LΩ(g) + 1 leaves labelled by y-variables. The existence of LΩ(f) + 1 x-leaves is proved in the same way. Altogether each formula for ∨(f × g) has at least LΩ(f) + LΩ(g) + 2 leaves. This implies the lower bound. 2

 The result on monotone circuits has been proved by Galbiati and Fischer (81).

 THEOREM 2.2 : Cm(f × g) = Cm(f) + Cm(g) .

 Proof : We assume that an optimal monotone circuit S for f g × contains less than Cm(f) + Cm(g) gates. Then there are gates in S having x- and y-variables as (not necessarily direct) predecessors. Let H be the first of these gates computing h(x,y) out of the inputs h1(x) and h2(y). W.l.o.g. H is an ∧-gate, ∨-gates are handled in the dual way. Let f[′] and g[′] be the functions computed instead of f and g resp. if we replace H by the constant 0 . By monotonicity f[′] f and g[′] g . ≤ ≤

; ;
###### If f[′] = f, there are a and b where f[′](a b) = 0 and f(a b) = 1 . Also ̸

;
###### f[′](a 0) = 0, since the circuit is monotone (here 0 is also the vector

;
###### consisting of zeros only). f(a 0) = 1, since f does not depend on

; ; ;
###### the y-variables. Therefore f[′](a 0) = f(a 0) implying h(a 0) = 1 and ̸ h2(0) = 1 . Again by monotonicity h2 ≡ 1 in contradiction to the optimality of S . Similar arguments prove g[′] = g . Hence f[′] = f and g[′] = g in contradiction to the optimality of S . 2

 We have proved that optimal monotone circuits for f g consist of × disjoint optimal monotone circuits for f and g . It does not help to join x- and y-variables. Uhlig ((74) and (84)) proved that the situation is totally different for circuits over complete bases.


-----

**304**

###### THEOREM 2.3 : C(r × f) ≤ 2[n] n[−][1] + o(2[n] n[−][1]) if f ∈ Bn and log r = o(n log[−][1] n) .

 For hard functions mass production leads to extreme savings of resources. If C(f) = Ω(2[n] n[−][1]) (as for almost all f ∈ Bn, see Ch. 4),

 ###### ε 0 and n sufficiently large, the complexity of 2[o(n][=][ log n)] copies of f is at most by a factor 1 + ε larger than the complexity of f . For all practical purposes this result is not of large value, since most of the interesting functions have circuit complexity bounded by O(2[α][n]) for

<
###### some α 1 .

 Theorem 2.3 holds also for (r f) which can be computed from ∨ × r f by r 1 additional gates. The use of mass production for (r f) × − ∨ × has also been proved by Paul (76). His methods differ from those of Uhlig. Paul considered Turing machines for the computation of (r f) and applied the efficient simulation of Turing machines by ∨ × circuits (see Ch. 9, 2). These results disprove the conjecture that § Ashenhurst decompositions (Ashenhurst (57)) lead to optimal circuits.

 DEFINITION 2.3 : An Ashenhurst decomposition of f ∈ Bn is given by


###### f(x) = g(xπ(1)


; : : : ;
###### xπ(m)


;
###### h(xπ(m+1)


; : : : ;
###### xπ(n))) (2.3)


; : : : ;
###### for some m ∈{1 n − 2}, g ∈ Bm+1 and permutation π .

 The general proof of Theorem 2.3 is technically involved. Therefore we consider only the case r = 2 . This is sufficient for the ˝Yes˝-entries in Tab. 2.1.

;
###### Proof of Theorem 2.3 for r = 2 : We design a circuit for (f(x) f(y)) .

; : : : ; ; : : : ;

###### For some k specified later let x[′] = (x1 xk) and x[′′] = (xk+1 xn) .

<
###### Similarly y[′] and y[′′] . For 0 ≤ l 2[k] let fl be the subfunction of f where we replace the first k inputs of f by the binary representation (of length k) of l . By i and j we denote the numbers whose binary representations are x[′] and y[′] resp. Then we have to compute fi(x[′′])


-----

**305**

###### and fj(y[′′]) . Let g0 = f0, gl = fl −1 ⊕ fl for 1 ≤ l ≤ 2[k] − 1 and gl = fl −1 for l = L := 2[k] . Then


###### fl = g0 gl = gl +1 gL ⊕· · · ⊕ ⊕· · · ⊕


:
###### (2.4)


###### Let us assume for the moment that i j . Then it is sufficient to ≤

; : : : ; ; : : : ;
###### compute g0(x[′′]) gi(x[′′]) and gj+1(y[′′]) gL(y[′′]) .
 We compute z[l] = x[′′] if 0 l i and z[l] = y[′′] if i + 1 l L . O(k) ≤ ≤ ≤ ≤ gates are sufficient for each l to compute τ [l] = 1 iff l i . Afterwards ≤ O(1) gates are sufficient to select each of the n k bits of z[l] . Altogether − we need O(n 2[k]) gates for the computation of all z[l] . For all l we compute gl (z[l] ) . Since gl depends only on n − k variables, we need altogether (see Ch. 4, 2) only §
 (2[k] + 1)(2[n][−][k] (n k)[−][1] + o(2[n][−][k] (n k)[−][1])) (2.5) − −
 gates. Afterwards we compute a[l] = gl (z[l] ) if l ≤ i and a[l] = 0 else and also b[l] = gl (z[l] ) if l ≥ j + 1 and b[l] = 0 else. This again can be done by O(n 2[k]) gates. Now f(x) = fi(x[′′]) is the ⊕-sum of all a[l] and f(y) = fj(y[′′]) is the ⊕-sum of all b[l] .
 The total number of gates is O(n 2[k]) plus the number in (2.5). If k = ω(1) and k = o(n) the number of gates is bounded by 2[n] n[−][1] + o(2[n] n[−][1]) .

 In general we do not know whether i j . O(n) gates are suffi- ≤ cient to compute τ = 0 iff i j . We interchange x and y iff τ = 1 ≤ (O(n) gates). Then we use the circuit described above and compute

; ;
###### (f(x) f(y)) if τ = 0 and (f(y) f(x)) if τ = 1 . By O(1) additional gates

;
###### we compute (f(x) f(y)) in all cases. 2

 The fundamental idea is the encoding of x[′′] and y[′′] by the z-vectors in such a way that only 2[k] + 1 and not 2[k+1] functions on n k vari- − ables have to be computed. The idea is the same for larger r but the encoding is more difficult. For monotone functions we improve Theo- rem 2.3 using the asymptotic results of Ch. 4, 5, and the fact that § subfunctions of monotone functions are monotone and the methods of Uhlig.


-----

**306**

###### COROLLARY 2.1 : C(r × f) = O(2[n] n[−][3][=][2]) if f ∈ Mn and log r = o(n log[−][1] n) .

 10.3 Reductions

 Reducibility is a key concept in the complexity theory. Polynomial- time reducibility is central to the concept of NP-completeness (see Garey and Johnson (79)). Reducibility can be used to show that the complexities of different problems are related. This can be possible even though we do not know the complexity of some problem. Re- ducibility permits one to establish lower and upper bounds on the complexity of problem A relative to problem B or vice versa. If A is reducible to B, this means that A is not much harder than B . Lower bounds on the complexity of A translate to similar lower bounds on the complexity of B . An efficient algorithm for B translates to a similarly efficient algorithm for A . This requires that the necessary resources for the reducibility function are negligible compared to the complexity of A and B .

 The monograph of Garey and Johnson (79) is an excellent guide to reducibility concepts based on Turing machine complexity. Because of the efficient simulations of Turing machines by circuits (Ch. 9, 2–3) § all these results can be translated to results on circuit complexity.

 We discuss three reducibility concepts that were defined with view on the complexity of Boolean functions. The three concepts are NC1- reducibility, projection reducibility and constant depth reducibility.

 NC1-reducibility is defined via circuits with oracles (Cook (83), Wilson (83)). We remember that NCk is the class of all se- quences fn Bn having UBC-uniform circuits Sn of polynomial size and ∈ O(log[k] n) depth (see Ch. 9, 8). §


-----

**307**

###### DEFINITION 3.1 : For gn Bn;m(n) a circuit with oracle g = (gn) ∈ consists of B2-gates and oracle gates computing some gn . The size of a gn-oracle gate is n + m(n) and its depth is ⌈log n⌉ .

 DEFINITION 3.2 : The sequence f = (fn) is NC1-reducible to g = (gn) if fn can be computed by UBC-uniform circuits Sn with or- acle g and logarithmic depth. Notation : f ≤1 g .

 NC1-reducibility is reflexive (f ≤1 f) and transitive (f ≤1 g ≤1 h ⇒ f ≤1 h) . The proof of these properties is left as an exercise. It is intuitively evident that f is not harder than g if f ≤1 g . This intuition is made precise in the following theorem.

 THEOREM 3.1 : f ∈ NCk if f ≤1 g and g ∈ NCk .

 Proof : Since f ≤1 g, there are UBC-uniform circuits Sn with oracle g and O(log n) depth computing fn . The size of Sn is polynomially bounded as for all circuits of logarithmic depth. Since g ∈ NCk, there are UBC-uniform circuits Tn of polynomial size and O(log[k] n) depth computing gn . Let Un be those circuits where we have replaced gr- gates in Sn by copies of Tr . The circuits Un are UBC-uniform. They have polynomial size, since we have replaced polynomially many gates by circuits of polynomial size.

 We estimate the length of a path p in Un . Let p[′] be the correspond- ing path in Sn . Gates of depth 1 on p[′] have not been lengthened. Gates of depth log r on p[′] have been replaced by paths of length O(log[k] r) . ⌈ ⌉ Hence the length of p is bounded by O(log n) plus the sum of some O(log[k] ri) such that the sum of all O(log ri) is bounded by O(log n) . Since the function x x[k] is convex, the length of p is bounded by → O(log[k] n) . This establishes the bound on the depth of Un . 2


-----

**308**

###### We often have used (see Ch. 3) implicitly the notion of NC1- reducibility, although we have not discussed the uniformity of the circuits. In order to practise the use of this reducibility concept, we present some NC1-reducibility results on arithmetic functions (Alt (84), Beame, Cook and Hoover (84)). Let MUL (more precisely MULn) be the multiplication of two n-bit integers, SQU the squaring of an n-bit integer, POW the powering of an n-bit number, i.e. the

; ; : : : ;
###### computation of x x[2] x[n] and DIV the computation of the n most
 significant bits of x[−][1] .

 THEOREM 3.2 : MUL =1 SQU ≤1 POW =1 DIV .

 Proof : MUL =1 SQU, since both problems are in NC1 . For this claim we use the circuits designed in Ch. 3. Nevertheless we state

;
###### explicit reductions. SQU ≤1 MUL, since SQU(x) = MUL(x x) . MUL ≤1 SQU, since

=
###### x y = (1 2) ((x + y)[2] x[2] y[2]) (3.1) − −

 and there are UBC-uniform circuits of logarithmic depth for addition, subtraction, and division by 2 .

 SQU ≤1 POW, since SQU is a subproblem of POW .

 SQU ≤1 DIV by transitivity and POW ≤1 DIV . An explicit reduction is given by


###### 1

:

###### x[2] = x (3.2)

1 1 _−_
x x+1

###### [−]
 DIV ≤1 POW, since the most significant bits of x[−][1] can be computed by some approximation

 x[−][1] 1 + (1 x) + (1 x)[2] + + (1 x)[k] (3.3) ≈ − − · · · −

 (see Ch. 3, 3). §


-----

**309**


###### POW ≤1 DIV . Let
 1 y := 2[2 n][3] 2[−][i 2 n][2] x[i] (3.4)
 1 − 2[−][2 n][2] x [= 2][2 n][3][ �]0≤i<∞


###### = � 2[2 n][2][ (n][−][i)] x[i]

0 i<
_≤_ _∞_


:


###### x[n] has at most n[2] significant bits. After computing enough (but poly
; ; : : : ;
###### nomially many) bits of y we can read off x x[2] x[n] in the binary
 representation of y . 2

 We have proved SQU ≤1 MUL by the relation SQU(x) =

;
###### MUL(x x) . The oracle circuit for SQU consists of a single oracle gate. Such reductions are called projections (see Ch. 6, 1) by Skyum § and Valiant (85).

 DEFINITION 3.3 : The sequence f = (fn) is projection reducible to g = (gn) if


###### fn(x1


; : : : ; ; : : : ;
###### xn) = gp(n)(σn(y1) σn(yp(n))) (3.5)


; : : : ;

###### for some polynomially bounded p(n) and some σn : {y1 yp(n)} →

; ; : : : ; ; ; ;

###### {x1 x1 xn xn 0 1} .
 Notation : f ≤proj g .

 Projection reducibility is reflexive and transitive. There is a whole theory on projection reducibility which we only touch slightly. We summarize some results of Chandra, Stockmeyer and Vishkin (84).

 DEFINITION 3.4 : Input UG (DG) means that the input is the adjacency matrix of an m-vertex undirected (directed) graph.

 EUL CYC : Input: UG. Output 1 G contains a cycle traversing ⇔ every edge exactly once.

 UCYC : Input: UG. Output 1 G contains a cycle. ⇔
 CON : Input: UG. Output 1 G is connected. ⇔


-----

**310**

###### STR CON : Input: DG. Output 1 G is strongly connected. ⇔
 UST CON : Input: UG. Output 1 ⇔ G contains a path v1 → vm .
 DST CON : Input: DG. Output 1 G contains a directed path ⇔ v1 vm . →

; ;
###### NET FLOW : Input: m-bit unary numbers c(i j) for 1 i j m and ≤ ≤ an m[2]-bit unary number f . The m-bit unary representation of k is

; ;
###### 0[m][−][k] 1[k] . Output 1 The network with capacity c(i j) on edge (i j) ⇔ allows an integral flow of size at least f from v1 to vm . A flow is a

N ; ; ; ;
###### function ϕ : E → 0 where ϕ(i j) ≤ c(i j), ϕ(i 1) = 0, ϕ(m j) = 0

; ;

###### and ϕ(i j) = ϕ(j k) for j = 1 and j = m .
 ̸ ̸

 [�] [�]

i k

###### BIP MATCH : Input: the adjacency matrix of a bipartite graph G on 2 m vertices and an m-bit unary number k . Output 1 G contains ⇔ a matching of size k, i.e. k vertex-disjoint edges.

 BIP PERF MATCH : BIP MATCH for k = m .

 CIRC VAL : Input: The (standard) encoding of a circuit S and the specification of an input a . Output 1 S computes 1 on a . ⇔

 THEOREM 3.3 : EUL CYC =proj UCYC =proj CON =proj UST CON ≤proj STR CON =proj DST CON ≤proj NET FLOW =proj BIP MATCH =proj BIP PERF MATCH ≤proj CIRCVAL .

 Proof : We only prove some of the assertions in order to present some methods.

 CON ≤proj EUL CYC : Given an undirected graph G, we describe an undirected graph G[′] such that G is connected iff G[′] has an Eulerian

; : : : ;

###### cycle. Let V = {v1 vm} be the vertex set of G . Then G[′] has 3 m+
 �m� ; ; <
2 vertices denoted by vi yi zi (1 ≤ i ≤ m) and uij (1 ≤ i j ≤ m) .

; ; ;

###### We declare that the edges {vi yi}, {vi zi} and {yi zi} exist, i.e. the ap
;

###### propriate variables are replaced by the constant 1 . The edges {vi uij},

; ; ;

###### {vj uij} and {vi vj} exist in G[′] iff {vi vj} exists in G, i.e. these vari ables are replaced by xij . All other edges do not exist, these variables are set to 0 .


-----

**311**

###### We use the well-known fact that a graph contains an Eulerian cycle iff it is connected except for isolated vertices and the degree of all vertices is even. By construction the degree of all vertices in G[′] is always even. If G is connected, uij is either isolated or connected to vi, so are zi and yi . Since all v-vertices are connected also in G[′], all non-isolated vertices in G[′] are connected. If G[′] is connected except for isolated vertices, vi and vj have to be connected by a path p without

; ;

###### cycles in G[′] . If p uses the edges {vk ukl } and {ukl vl } (the only
 possibility of reaching ukl ) we may use instead of these two edges the

;

###### edge {vk vl } and obtain a path from vi to vj in G .

; ;
###### DST CON ≤proj NET FLOW : Let c(i j) = 1 if (vi vj) ∈ E and

;
###### c(i j) = 0 else. Let f = 1 . There is a flow of size 1 or larger from v1 to vm iff there is a directed path from v1 to vm in the given graph G .
 BIP PERF MATCH ≤proj BIP MATCH : This is obvious, since BIP PERF MATCH is BIP MATCH for k = m .

 BIP MATCH ≤proj NET FLOW : Let G be the given bipartite graph

; : : : ; ; : : : ;

###### on u1 um and v1 vm . For the flow problem we add two vertices

;
###### s and t and look for a flow from s to t . The capacities are 1 for (s ui)

; ;

###### and (vi t) for 1 ≤ i ≤ m and all edges (ui vj) in G . All other capacities
 are 0 . Obviously there is a flow of size f from s to t iff G contains a matching of size f .

 BIP PERF MATCH ≤proj CIRC VAL : There is a polynomial al- gorithm for BIP PERF MATCH due to Hopcroft and Karp (73) (see also Ch. 6, 12). By the simulations of Ch. 9, 2 there are also § § polynomial circuits Sn for this problem. We consider CIRC VAL for circuits of size c(Sn) and n[2] inputs. The variables for the encoding of a circuit are replaced by the constants describing the encoding of Sn, and the variables for the inputs are replaced by the variables for the edges in the bipartite graph. 2


-----

**312**

###### f ≤proj g iff fn is a special case of some gm where m is not too large with respect to n . This happens if f is really a special case of g (as for BIP PERF MATCH ≤proj BIP PERF MATCH) or if g is a general model (as CIRC VAL ) and also for problems which at the first glance have nothing in common (as for CON ≤proj EUL CYC) . Much more complicated projection reductions than those presented are known. If f ≤proj g, (fn) is not much harder than (gn) .
 Often weaker reducibility concepts are sufficient for the conclusion that (fn) is not much harder than (gn) . Let us compare parity PAR

; : : : ;

###### where PARn(x1 xn) = x1 xn and majority MAJ where
 ⊕· · · ⊕ MAJn(x) = T[n]⌈n=2⌉[(x) . MAJ][ ≤|]proj [PAR, since each subfunction of a] parity function is a parity function or a negated parity function. Also PAR ≤| proj MAJ . Projections of MAJm are functions of the following type, the output is 1 iff � αixi ≥ k for some k and αi ∈ Z . This is

1 i m
_≤_ _≤_

###### not equal to PARn . Nevertheless PAR is not much harder than MAJ by the following reduction :

 PARn(x) = T[n]k[(x)][ ∧] [(][¬][T][n]k+1[(x))][:] (3.6)
 [�]

k odd


###### All T[n]k [are subfunctions of MAJ][2n][ .]
 This leads to another reducibility concept, the so-called constant depth reducibility. It refers to bounded-depth circuits which we in- vestigate in detail in the next chapter. For these circuits all literals

;

###### xi xi (1 ≤ i ≤ n) are inputs, and all gates are ∧-gates and ∨-gates of
 unbounded fan-in. Polynomials refer to depth 2 circuits.


;
###### DEFINITION 3.5 : SIZE - DEPTH(S(n) D(n)) is the class of all se- quences fn Bn which can be computed by unbounded fan-in circuits ∈ of size at most S(n) and depth at most D(n) simultaneously.

; ;
###### SIZE - DEPTH(poly const) is the union of all SIZE - DEPTH(cn[k] d) .

 DEFINITION 3.6 : The sequence f = (fn) is constant depth reducible to g = (gn) if there is a polynomial p(n) and a constant c such that each fn is computed by an unbounded fan-in circuit of depth at most


-----

**313**

###### c and size p(n) containing oracle gates for gj or gj with j ≤ p(n) - the size and the depth of the oracle gates is 1 - and on each path is at most one oracle gate. Notation : f ≤cd g .

 THEOREM 3.4 : i) ≤cd is reflexive and transitive.
 ii) f ≤proj g ⇒ f ≤cd g .

;
###### iii) f ≤cd g, g ∈ SIZE - DEPTH(S(n) D(n)), S and D monotone ⇒

;
###### f SIZE - DEPTH(p(n) S(p(n)) c D(p(n))) for some polynomial p ∈

;
###### and constant c . In particular g SIZE - DEPTH(poly const) ∈ ⇒

;
###### f SIZE - DEPTH(poly const) . ∈

 The easy proof of this theorem is left as an exercise. By Theo- rem 3.4 ii the results of Theorem 3.3 hold also for constant depth re- ducibility. For ˝simple˝ problems like PAR and MAJ nothing can be proved with projection reducibility, but a lot is known about constant depth reducibility. Some of the following results have been proved by Furst, Saxe and Sipser (84) but most of them are due to Chandra, Stockmeyer and Vishkin (84).

 DEFINITION 3.7 :


; : : : ;

###### PAR : Input: x1 xn . Output x1 xn .
 ⊕· · · ⊕

; : : : ;

###### ZMc (zero mod 2[c]) : Input: x1 xn . Output 1 ⇔
 x1 + · · · + xn ≡ 0 mod 2[c] .
 MUL : Multiplication of two m-bit numbers, n = 2m .
 SOR : The sorting problem for m m-bit numbers, n = m[2] .

 MADD (multiple addition) : The addition of m m-bit numbers, n = m[2] .

; : : : ;

###### THR : Input: x1 xm and an m-bit unary number k. Output
 T[m]k [(x), n = 2m .]


###### MAJ : Input: x1


; : : : ;
###### xn . Output T[n]n=2
_⌈_ _⌉[(x).]_


-----

**314**

; : : : ;

###### BCOUNT : Input: x1 xn . Output: the binary representation of
 x1 + · · · + xn .

; : : : ;

###### UCOUNT : Input: x1 xn . Output: the n-bit unary representation
 of x1 + · · · + xn .

 THEOREM 3.5 : PAR =cd ZMc ≤cd MUL =cd SOR =cd MADD =cd THR =cd MAJ =cd BCOUNT =cd UCOUNT ≤cd UST CON .

 By Theorem 3.4 ii we can combine the results of Theorem 3.3 and Theorem 3.5. The lower bound for parity (which we prove in Ch. 11) translates to lower bounds for all problems in Theorem 3.3 and Theorem 3.5. Again reducibility is a powerful tool.

; : : : ;
###### We do not prove that MUL UCOUNT ≤cd UST CON, only

;
###### the weaker claim PAR ZMc ≤cd UST CON . This claim is sufficient for the translation of the lower bound on parity to the other problems.

 Proof of Theorem 3.5 :
 PAR ≤cd ZMc : We use 2[c][−][1] copies of each xi and an oracle gate for ZMc on these n2[c][−][1] inputs. ¬
 ZMc ≤cd PAR : Obviously PAR = ¬ ZMc for c = 1 . Because of transitivity it is sufficient to prove ZMc ≤cd ZM(c-1) if c ≥ 2 . Let

; : : : ; <

###### x1 xn be the inputs and let us compute yij = xixj for 1 ≤ i j ≤ n .
 It is sufficient to prove that


; : : : ;
###### xn) ∧ (3.7)


###### ZMc(x1


; : : : ;
###### xn) = ZM(c-1)(x1


###### ZM(c-1)(y12 ; : : : ; yn 1;n):

_−_


###### Let s be the sum of all xi and t the sum of all yij . Then

 � = t = yij = (1 2) xi xj (3.8)

1 i<j n [�]i=j
_≤_ _≤_ _̸_


= ��� �2 � � = :
###### = (1 2) xi − x[2]i = (1 2) (s[2] − s)

1 i n 1 i n
_≤_ _≤_ _≤_ _≤_


-----

**315**

=
###### If s 0 mod 2[c], s (s 2) 0 mod 2[c][−][1] and t 0 mod 2[c][−][1], since ≡ ≡ ≡ ≡

=
###### t = (s 2)(s 1) . This proves in (3.7). If s t 0 mod 2[c][−][1] but − ≤ ≡ ≡ s 0 mod 2[c], s = j 2[c][−][1] for some odd j . Since c 2, also s 1 is ̸≡ ≥ − odd. Hence (s 1) j is odd. Moreover −

=
###### t = (s 2) (s 1) = (s 1) j 2[c][−][2] (3.9) − −

 in contradiction to t 0 mod 2[c][−][1] . This proves in (3.7). ≡ ≥
 PAR ≤cd UCOUNT : Because of transitivity this implies that the first group (PAR, ZMc) is constant depth reducible to the second

; : : : ;
###### group (MUL UCOUNT) of problems.

: : : ;
###### UCOUNT(x) equals (T[n]n[(x)][;] T[n]1[(x)) .] We compute UCOUNT(x) and UCOUNT(x) . Then we compute PAR(x) ¬ by (3.6).

 For the proof that the second group of problems contains equiv- alent problems with respect to constant depth reducibility it is (by transitivity) sufficient to prove that MAJ ≤cd MUL ≤cd MADD ≤cd BCOUNT ≤cd SOR ≤cd UCOUNT ≤cd THR ≤cd MAJ .
 MAJ ≤cd MUL : If we are able to compute the binary representation

=
###### cn of x1 + · · · +xn, we are done. MAJ(x) = 1 iff x1 + · · · +xn ≥⌈n 2⌉ . This comparison can be performed in depth 2 and polynomial size by the disjunctive normal form, since the length of cn is k = ⌈log(n + 1)⌉ . For the computation of cn we use a padding trick already used in Ch. 3, § 2. Let a be the binary number of length n k with xi at position k(i−1) and zeros elsewhere. Then a is the sum of all xi 2[k(i][−][1)] . Let b be the binary number of length n k with ones at the positions k(i 1) for − 1 i n and zeros elsewhere. Then b is the sum of all 2[k(i][−][1)] . We ≤ ≤ compute (at an oracle gate) c, the product of a and b . Then c is the sum of all ci 2[k(i][−][1)] with k-bit numbers ci contained in c . It is easy to see that cn = x1 + · · · + xn .
 MUL ≤cd MADD : Obvious by the school method for multiplication.
 MADD ≤cd BCOUNT : Let ai = (ai;m−1 ; : : : ; ai;0) for 1 ≤ i ≤ m be
 the m numbers we have to sum up. We use in parallel oracle gates to compute the l = ⌈log(m + 1)⌉-bit numbers bj = a1;j + · · · +am;j . Then


-----

**316**

###### s = a1 + · · · + am is also the sum of all bj 2[j] . Since the length of all b’s is l, we add bj 2[j] and bj+l 2[j+][l] without any gate by concatenating the strings for bj and bj+l . In this way we obtain l numbers of length m + l each whose sum equals s .

 Again we add the bits at the same position. But we have (by Definition 3.6) no more oracle gates. Since l is already small, the dis- junctive normal form has polynomial size with respect to n = m[2] . We continue in the same way until we obtain two numbers x and y whose sum is s . At step 0 we have l (0) = m summands. If l (i 1) is the − number of summands at step i 1, l (i) = log(l (i 1) + 1) . The − ⌈ − ⌉ number of necessary steps is not bounded by a constant. Therefore we use this procedure only for two steps and compute l (2) = O(log log m) summands whose sum is s . We estimate the number of bits in these summands on which xi or yi depends essentially. Each bit of the sum- mands in step 3 depends on l (2) bits of the summands in step 2 . If the number of necessary steps is k, xi or yi depends on l (2)l (3) · · · l (k − 1) bits. Since l (j) = O(log l (j 1)), l (j)l (j + 1)[2] = o(l (j)[2]) and by in- − duction l (j) · · · l (k − 1) = o(l (j)[2]) . Therefore xi and yi depend on o(l (2)[2]) = o(log m) bits of the summands computed in step 2 . So we compute xi and yi by their disjunctive normal forms from the sum- mands in step 2 . Finally we add x and y by a circuit of polynomial size and constant depth. The existence of such a circuit is proved in Ch. 11, 2. The proof is easy by the methods of Ch. 3, 1. § §

; : : : ;

###### BCOUNT ≤cd SOR : Let s = (sk−1 s0) where k = ⌈log(n + 1)⌉ be

; : : : ;

###### the binary representation of x1 + · · · + xn . By sorting x1 xn with

; : : : ;

###### an oracle gate we obtain the unary representation y = (yn y1)
 of s . Let y0 = 1, yn+1 = 0 and zi = yi ∧ yi+1 for 0 ≤ i ≤ n . Then zi = 1 iff i = s . Let bi = (bi;k−1 ; : : : ; bi;0) be the binary representation
 of i . Then sj is the disjunction of all zi bij . ∧
 SOR ≤cd UCOUNT : It is proved in Ch. 11, § 2 (or easy to see) that there are polynomial comparator circuits of constant depth. The

< ; : : : ;
###### output is 1 iff x y (or for another circuit x ≤ y) . Let a1 am
 be the m-bit numbers that have to be sorted. We compute cij = 1


-----

**317**

<

###### iff ai aj or ai = aj and i ≤ j . Then we compute in parallel by
 oracle gates dj, the sum of all cij . dj is the unary representation of

; : : : ;

###### the position of aj in the sorted list of a1 am . By similar methods
 as in the last reduction ˝BCOUNT ≤cd SOR˝ we compute the sorted

; : : : ;

###### list of a1 am .
 UCOUNT ≤cd THR : We compute in parallel by oracle gates yi =

; : : : ; ; ; : : : ; ; : : : ;

###### THR(x1 xn i) . Then UCOUNT(x1 xn) = (yn y1) .

; : : : ;

###### THR ≤cd MAJ : The input consists of x1 xm and k =

; : : : ;

###### (km k1), a number in unary representation. We compute by an

; : : : ; ; ; : : : ; ;

###### oracle gate z = MAJ(x1 xm k1 km 1) .
 z = 1 iff x1 + · · · + xm + k1 + · · · + km + 1 ≥ m + 1 . There are l ones in k if k represents l . Then k1 + · · · + km = m − l . Hence z = 1 iff

;
###### x1 + · · · + xm ≥ l iff THR(x k) = 1 .


###### In order to relate the complexity of PAR and ZMc to all prob- lems considered in Theorem 3.3 we prove PAR ≤cd UST CON . We compute the adjacency matrix A of an undirected graph G on the

; : : : ; ; : : : ;

###### vertices v0 vn+1 . Let x1 xn be the inputs of PAR and let
 x0 = xn+1 = 1 . Let aii = 0 and let

< :
###### aij = xi ∧ xi+1 ∧· · · ∧ xj−1 ∧ xj for i j (3.10)

 G contains exactly one path from v0 to vn+1, this path passes through all vi with xi = 1 . The length of this path is even iff x1 xn = ⊕· · · ⊕ 1 . We square in polynomial size and constant depth the Boolean matrix A . The result is B, the adjacency matrix of the graph G[′]
 where vi and vj are connected by an edge iff they are connected in G by a path of length 2 . i.e. v0 and vn+1 are connected by a path iff x1 xn = 1 . Therefore one oracle gate for UST CON is sufficient ⊕· · ·⊕ for the computation of x1 xn . 2 ⊕· · · ⊕

 Often it is easier to prove lower bounds by reduction than to prove lower bounds directly. The number of reducibility results is large.


-----

**318**

###### EXERCISES

 1. Let N[∗]n [be the class of all f][ ∈] [M]n[∗] [whose prime implicants all have]

=
###### length ⌈n 2⌉ . Then there is for each ⌈log n⌉≤ j ≤ D(N[∗]n[) (or] Dm(N[∗]n[)) a function g][j][ ∈] [N][∗]n [where D(g][j][) = j (or D][m][(g][j][) = j) .]

;
###### 2. Prove (1.2) for the bases and NAND . {∧ ⊕} { }

 3. Prove dΩ(j) ≤ 2 for all binary bases and all interesting j .

 4. Prove (1.5).

 5. Prove (1.3) and (1.4) for further bases.

<
###### 6. cΩ(j) = 1 for n = 2, 0 ≤ j CΩ(B[∗]2[) and Ω=][ {∧][;][ ⊕}][ or Ω=] NAND . { }

 7. Almost all f ∈ Bn have no Ashenhurst decomposition.

 8. Assume that Cm(∨(f × g)) ≥ Cm(f) + Cm(g) for arbitrary Boolean functions f and g . Prove by this assumption asymptotically op- timal bounds on the monotone circuit size of the Boolean matrix product and the generalized Boolean matrix product (see Ch. 6, 9). §

 9. Prove Theorem 2.2 using the replacement rule of Theorem 5.1, Ch. 6, and its dual version.

 10. (Fischer and Galbiati (81) just as Exercise 11). Let f ∈ Mn+1

; : : : ; ; ; : : : ; ;

###### depend on x1 xn z and g ∈ Mm+1 depend on y1 ym z .

;
###### Then Cm(f g) = Cm(f) + Cm(g) . Hint: A gate G is called mixed, if G has not only x-variables but also y-variables as predecessors.


-----

**319**

;
###### Let H be the first mixed gate of a monotone circuit for (f g),

; ; ;
###### w.l.o.g. an ∧-gate. Let h(x y z) = resH and let h1(x z) and h2(y,z) be the inputs of H .

; ;
###### a) H can be replaced by 0 if h1(0 1) = h2(0 1) = 0 .

; ; ;
###### b) If h1(0 1) = 1 and H is not superfluous, h1(0 0) = h2(0 0) = 0,

; ; ; ; ; ;
###### z ∧ h2(0 z) = h1(x z) ∧ h2(0 z) and z ∧ h2(y z) = h1(0 z) ∧ h2(y z) . c) Either H can be replaced by 0 or h1 or h2 can be replaced by z .

; : : : ; ; : : : ; ; ;

###### 11. Let h ∈ Bn, x = (x1 xn), y = (y1 yn), f(x z1 z2) =

; ; ;
###### z1 ∧ (z2 ∨ h(x)) and g(y z1 z2) = z2 ∧ (z1 ∨ h(y)) . Then Cm(f g) ≤
 Cm(h) + 3n + 4 .

; : : : ;

###### Hint: Compute h(u1 un) with ui = xiz1 yiz2 .
 ∨


###### 12. ≤1 is reflexive and transitive.

 13. ≤proj is reflexive and transitive.

 14. Prove Theorem 3.4.

 15. Prove directly PAR ≤cd MUL .

 16. Try to prove directly more of the assertions of Theorem 3.5.


-----

**320**

###### 11. BOUNDED - DEPTH CIRCUITS

 11.1 Introduction

 A polynomial p for the Boolean function f is a disjunction of monoms computing f (see Ch. 2). Polynomials are circuits of two

; ; : : : ; ;

###### logical levels. All literals x1 x1 xn xn are inputs. The monoms
 are computed on the first level, an -level. On the second level, an ∧ -level, these monoms are combined by a disjunction. In this chapter ∨ we investigate circuits of k logical levels.


###### DEFINITION 1.1 : A Σk-circuit (Πk-circuit) is a circuit consisting of k logical levels. All inputs of gates on level l are outputs of gates on

; ; : : : ; ;

###### level l − 1 . On level 0 we have the inputs x1 x1 xn xn . ∧- and ∨
; ; ; : : :
###### gates of unbounded fan-in are available. The levels k k 2 k 4 − − consist of -gates ( -gates) and the other levels consist of -gates ∨ ∧ ∧ ( -gates). ∨

 This model is robust. Negations inside the circuit are powerless. We copy all gates and negate one of the copies of each gate. No additional gate is necessary for the application of the deMorgan rules (bottom-up). At the end of this procedure only inputs are negated. If an input of an -gate G is the output of an -gate G[′], we replace ∧ ∧ the edge from G[′] to G by edges from all direct predecessors of G[′] to G . Also the synchronization of Σk- and Πk-circuits is no essential restriction. An edge from a gate G on level l to a gate G[′] on level

 
###### l [′] l + 1 may be simulated by l [′] (l + 1) new gates on the levels
 −

; : : : ;
###### l + 1 l [′] − 1 computing res G . The size of the circuit is at most multiplied by the number of logical levels which should be small.

 Hardware designers prefer circuits with a small number of logical levels. Hence it is a fundamental problem to decide whether sequences

;
###### of functions fn Bn are in SIZE - DEPTH(poly const) (see Def. 3.5, ∈


-----

**321**

###### Ch. 10). In 3 we prove that polynomial circuits for the parity func- §

=
###### tion have depth Ω((logn) (log log n)) . Applying the reducibility re- sults of Ch. 10, 3, we conclude that many fundamental functions §

;
###### with polynomial circuit size are not in SIZE - DEPTH(poly const) . Therefore we should use circuits where the number of logical levels is increasing with the input length.

 In 2 we prove for some fundamental functions that they are in §

;
###### SIZE - DEPTH(poly const) and design almost optimal circuits for the parity function. The announced lower bound for the parity function is proved in 3. In 4 we describe which symmetric functions are § §

;
###### contained in SIZE - DEPTH(poly const) . In 5 we discuss hierarchy § problems.

 We finish this introduction with two concluding remarks. Bounded- depth circuits also represent an elegant model for PLAs (pro- grammable logic arrays). Furthermore results on bounded-depth cir- cuits are related to results on parallel computers (see Ch. 13).

 11.2 The design of bounded-depth circuits

 Let fn Bn . If the number of prime implicants (or prime clauses) ∈

N
###### of fn is bounded by a polynomial, then the sequence fn (n ∈ ) has polynomial Σ2-circuits (Π2-circuits). Hence this sequence is in

;
###### SIZE - DEPTH(poly const) . We mention two examples, the thresh- old functions T[n]k [and the clique functions c][l][ n][;][k][ (see Def. 11.1, Ch. 6)] for constant k . Furthermore all functions depending essentially on

;
###### only O(log n) input bits are in SIZE - DEPTH(poly const) . An ex
; : : : ;

###### ample is the transformation of the binary representation (x1 xk)

; : : : ;
###### (n = 2[k]) of some number x 0 n 1 into its unary representa- ∈{ − }

; : : : ;

###### tion (y1 yn) .
 Chandra, Stockmeyer and Vishkin (84) proved that the following

;
###### fundamental functions are in SIZE - DEPTH(poly const) .


-----

**322**

###### DEFINITION 2.1 :

 ADD : Addition of two m-bit numbers, n = 2m .

 COM : The comparison problem for two m-bit numbers x =

; : : : ; ; : : : ;     
###### (xm 1 x0) and y = (ym 1 y0) . Output 1 x y .
_−_ _−_ _⇔|_ _|_ _|_ _|_

###### n = 2 m .

 MAX : The computation of the maximum of m m-bit numbers, n = m[2] .

 MER : The merging problem for two sorted lists of m m-bit numbers, n = 2 m[2] .

 U B : Input: an n-bit unary number k . Output: the binary → representation of k .

 THEOREM 2.1 : ADD, COM, MAX, MER and U B are in →

;
###### SIZE - DEPTH(poly const) .


###### Proof : ADD : We implement the carry look-ahead method (see Ch. 3, § 1). We compute uj = xjyj and vj = xj ⊕yj (0 ≤ j ≤ m−1) in depth 2 .

: : :

###### The carry bit cj is the disjunction of all uivi+1 vj (0 ≤ i ≤ j) (see
 Ch. 3, (1.8)). The sum bits sj are computed by s0 = v0, sn = cn−1 and sj = vj ⊕ cj−1 (1 ≤ j ≤ n − 1) . The size of the circuit is O(n[2]) (the number of wires is O(n[3])) and the depth is 4 if vj and sj are computed by Π2-circuits for a ⊕ b .

   - ;
###### COM : |x| |y| if there is an i such that yi = 0 xi = 1 and yj = xj for

  ###### all j i . This can be computed by


###### �
 � � � �[�]

0 i m 1 xi ∧ yi ∧ i<j m 1 (xj ∧ yj) ∨ (xj ∧ yj)
_≤_ _≤_ _−_ _≤_ _−_


:
###### (2.1)


###### The circuit size is O(m[2]) = O(n[2]) and the depth is 4 .

; : : : ;

###### MAX : Let a1 am be m m-bit numbers. We compute in depth 4

;
###### with O(m[4]) gates cij = 1 iff ai ≥ aj (1 ≤ i j ≤ m) . Let di be the conjunction of all cij . Then di = 1 iff ai is the maximum. The j -th bit of the output is computed as the disjunction of all aijdi . The size of the circuit is O(m[4]) = O(n[2]), and the depth is 6 .


-----

**323**

###### MER : Let a1 am and b1 bm be sorted lists. We ≤· · · ≤ ≤· · · ≤

<

###### compute cij = 1 iff bi aj . For each j, cmj c1j is the unary repre · · · sentation of the number of b’s less than aj . Let cj = 0[m][−][j] cmj c1j 1[j] . · · · Then cj is the unary representation of aj’s position in the merged list. In parallel we compute dij = 1 iff ai bj and dj = 0[m][−][j] dmj d1j 1[j], ≤ · · · the unary representation of bj’s position in the merged list. For z = z2m · · · z1, z2m+1 = 0 and 0 ≤ k ≤ 2m, EQk(z) = zk ∧ zk+1 tests whether z is the unary representation of k . Finally the i -th bit of the k -th number in the merged list is
 � (EQk(cj) ∧ aji) ∨ � (EQk(dj) ∧ bji): (2.2)

1 j m 1 j m
_≤_ _≤_ _≤_ _≤_


###### The size of the circuit is O(m[4]) = O(n[2]), and the depth is 6 .

; : : : ;

###### U → B : Let (xn x1) be the input, x0 = 1 and xn+1 = 0 .
 Let di = xixi+1 . Then di = 1 iff x is the unary representation of i, 0 ≤ i ≤ n . The j -th bit of the output is the disjunction of all di such that the j -th bit of i is 1 . The number of gates is O(n), the number of wires is O(n log n), and the depth is 2 . 2

 THEOREM 2.2 : If k(n) = O(log[r] n) for some fixed r, T[n]
k(n) [is in]

;
###### SIZE - DEPTH(poly const) .

 The proof of this theorem is postponed to Ch. 12, 3. The proof § is not constructive. We shall design efficient probabilistic circuits for T[n]
k(n) [and shall show how such circuits are simulated by deterministic]
###### circuits.

 There are only few papers on lower bounds for functions in

;
###### SIZE - DEPTH(poly const) . We refer to Chandra, Fortune and Lip- ton (83) and (85) and Hromkovic (85). It is more important to decide

;
###### which functions belong to SIZE - DEPTH(poly const), the class of efficiently computable functions.
 In the next section we prove that the parity function PARn does not belong to this class. Here we design almost optimal circuits for PARn . PARn consists of 2[n][−][1] prime implicants and 2[n][−][1] prime clauses, all of


-----

**324**

###### them are necessary in Σ2- and Π2-circuits resp. Hence the complexity of PARn in depth 2 circuits is 2[n][−][1] + 1 . In the following we allow negations which we eliminate afterwards as described in 1. §
 For k-level circuits we compute PARn in k − 1 steps. W.l.o.g. n = r[k][−][1] . In Step 1 we compute PARr on r[k][−][2] blocks of r variables each. In Step 2 we compute PARr on r[k][−][3] blocks of r outputs of Step 1 each. Hence we compute the parity of r[2] bits at each output of Step 2. We continue in the same way. After Step i we have computed the parity of r[k][−][1][−][i] blocks of r[i] variables each, in particular, we compute PARn in Step k − 1 . We use an alternating sequence of Σ2- and

; : : : ;
###### Π2-circuits for Step 1 k − 1 . Then it is possible to combine the second level of the Σ2-circuits (Π2-circuits) on Step i and the first level of the Π2-circuits (Σ2-circuits) on Step i + 1 . Altogether we obtain Σk-circuits and Πk-circuits for PARn . The number of subcircuits for PARr is r[k][−][2] + r[k][−][3] + · · · + 1 ≤ r[k][−][1] = n, each of these subcircuits contains 2[r][−][1] + 1 gates.

 THEOREM 2.3 : i) PAR has Σk- and Πk-circuits of size O(n 2[n][1][=][(k][−][1)]) .
 ii) PAR has Σk(n)- and Πk(n)-circuits of size O(n[2] log[−][1] n) if k(n) =

=
###### (log n) log logn + 1 . ⌈ ⌉

 Proof : i) has already been proved for n = r[k][−][1] . The general case is left as an exercise.

 ii) In Step i we combine the outputs of Step i 1 to the least number of − blocks whose size is bounded by log n + 1 . The number of blocks in ⌈ ⌉
; � = �
###### Step i is bounded by max 1 n log[i] n . k(n) 1 steps are sufficient { } − in order to obtain one block, since (log n)[k(n)][−][1] n . Altogether we ≥

=
###### require less than 2 ⌊n log n⌋ Σ2- and Π2-parity circuits working on at most log n + 1 inputs. 2 ⌈ ⌉


-----

**325**

###### 11.3 An exponential lower bound for the parity function

 The number of papers on Σ2- and Π2-circuits is immense, but there are almost no results on Σk- and Πk-circuits for k ≥ 3 which were proved before 1980. Then exponential lower bounds on the monotone Σ3-complexity have been proved by Tkachev (80), Kuznetsov (83 a), Valiant (83) (for clique functions) and Yao (83) (for the majority func- tion). Yao proved exponential lower bounds even on the monotone Σ4-complexity of some clique functions.

 The decisive break-through was the paper of Furst, Saxe and Sipser (84). They proved that parity is not in

;
###### SIZE - DEPTH(poly const) . Their non polynomial lower bound for Σk-circuits was improved by an exp(Ω(log[2] n))-lower bound of Ajtai (83). The first exponential lower bound for arbitrary constant depth was proved by Boppana (84), but only for the monotone Σk-complexity of the majority function. Another break-through was the proof of exponential lower bounds for depth k parity circuits. The original bound and methods due to Yao (85) have been improved by H˚astad (86).


###### THEOREM 3.1 : For some constant n0 and n ≥ n[k]0 [Σ][k][- and Π][k][-] circuits for the parity function x1 xn have more than 2[c(k)n][1][=][(k][−][1)] ⊕· · · ⊕

= =
###### gates, c(k) = (1 10)[k][=][(k][−][1)] 1 10 . ≈

;
###### COROLLARY 3.1 : PAR is not in SIZE - DEPTH(poly const) .

 COROLLARY 3.2 : Polynomial size parity circuits must have depth
 log n of at least
 c + log log n [for some constant c .]


###### The corollaries follow easily from Theorem 3.1. Because of our upper bounds in Theorem 2.3, these results are nearly optimal.


-----

**326**

###### We give an outline of the proof of Theorem 3.1. The proof is by induction on k . The induction basis k = 2 is easy. For the induction step we try to convert depth k circuits to not very large depth k 1 − circuits. If the second level is an -level, each function on level 2 is ∧ computed by a Π2-circuit. It is possible to replace these Π2-circuits by Σ2-circuits for the same functions. Then the second and the third level of the circuit are -levels which we combine in order to obtain ∨ depth k − 1 circuits. The problem is that the Σ2-complexity of g may be exponential even if the Π2-complexity is small, say polynomial.

 In the following way the problem can be avoided. We replace sev- eral variables in such a way by constants that all functions on level 2 have small Σ2-circuits and that the number of remaining variables is yet large enough. Nobody knows how to construct such a replace- ment. Again we use probabilistic methods. We hope that many re- placements serve our purposes. In order to prove the existence of a good replacement, it is sufficient to prove that the probability of a good replacement is positive.

; : : : ;

###### DEFINITION 3.1 : A restriction is a function ρ : {x1 xn} →

; ;
###### {0 1 ∗} . Then gρ is the projection of g where we replace xi by ρ(xi)

;
###### if ρ(xi) ∈{0 1} . For a random restriction ρ ∈ Rp (0 ≤ p ≤ 1) the random variables ρ(xi) (1 ≤ i ≤ n) are independent and ρ(xi) = 0

= =
###### with probability (1 − p) 2, ρ(xi) = 1 with probability (1 − p) 2 and ρ(xi) = ∗ with probability p . For ρ ∈ Rp, gρ is a random function.

 The following main lemma tells us that if we apply a random re- striction, we can with high probability convert Π2-circuits to equiva- lent Σ2-circuits of small size. We need the notion of the 1-fan-in of a circuit. This is the maximal fan-in of all gates on the first level. The proof of the first technical lemma is left to the reader.


-----

**327**

###### LEMMA 3.1 : The equation � 4 p �t � 2 p �t 1 + = 1 + + 1 (3.1)
 (1 + p) α (1 + p) α

<
###### has a unique positive root. If p = o(1), α (2 p) ln[−][1] ϕ 5 p t, where ≈ ϕ is the golden ratio, i.e. the root of ϕ[2] = ϕ + 1 .

 MAIN LEMMA 3.2 : Let S be a Π2-circuit of 1-fan-in t computing g ∈ Bn and let ρ ∈ Rp . The probability that gρ can be computed by a Σ2-circuit of 1-fan-in s is at least 1 − α[s] .

 The Main Lemma is equivalent to its dual version. We prove a more general version of the Main Lemma . Let l PI(f) denote the maximal length of a prime implicant of f . We use the convention that a conditional probability is 0 if the probability of the condition in question is 0 .


; : : : ;

###### LEMMA 3.3 : Let g1 gm be sums of at most t literals each. Let
 g = g1 ∧· · · ∧ gm and f ∈ Bn . For ρ ∈ Rp we have


###### Pr(l PI(g ρ) ≥ s | fρ ≡ 1) ≤ α[s]


:
###### (3.2)


###### Lemma 3.3 implies the Main Lemma 3.2 by choosing f 1 . ≡

 Proof of Lemma 3.3 : We prove this lemma by induction on m . If m = 0, the lemma is obvious since g 1 . ≡

   - ;
###### Let m 0 . Since Pr(A) max Pr(A B) Pr(A B), also ≤ { | | }

 Pr(l PI(g ρ) ≥ s | fρ ≡ 1) ≤ (3.3)

; ; ; :
###### max{Pr(l PI(g ρ) ≥ s | fρ ≡ 1 g1ρ ≡ 1) Pr(l PI(g ρ) ≥ s | fρ ≡ 1 g1ρ ̸≡ 1}

 The estimation of the first term is easy by the induction hypothesis. We choose f ∧ g1 instead of f and g[′] = g2 ∧· · · ∧ gm instead of g . If the condition (f ∧ g1)ρ ≡ 1 holds, g ρ = g[′]ρ [. Therefore the first term is] bounded by α[s] .


-----

**328**

###### The estimation of the second term is more difficult. W.l.o.g. g1 is the sum of all xi ∈ T and |T| ≤ t . Otherwise we interchange the roles of some xi and xi . Let ρ[′] or ρ˝ be that part of ρ which concerns the variables in T or not in T resp. Notation: ρ = ρ[′] ρ[′′] . The condition g1ρ ̸≡ 1 is equivalent to the condition that ρ[′](xi) ̸= 1 for all xi T . Hence each prime implicant of g ρ contains - if g1ρ 1 ∈ ̸≡
 - some xi ∈ T . For Y ⊆ T let PI Y(g ρ) be the set of prime implicants of g ρ containing, for xi T, xi or xi iff xi Y . Let l PI Y(g ρ) be the ∈ ∈ length of a longest prime implicant in PI Y(g ρ) and let ρ[′](Y) ≡∗ be the event that ρ[′](xi) = ∗ for all xi ∈ Y . Then

;
###### Pr (l PI(g ρ) ≥ s | fρ ≡ 1 g1ρ[′] ̸≡ 1) (3.4)

 � ; ≤ Pr(l PIY(g ρ) ≥ s | fρ ≡ 1 g1ρ[′] ̸≡ 1)

Y T; Y=
_⊆_ _̸_ _◦̸_


###### = � Pr(ρ[′](Y) ≡∗| fρ ≡ 1; g1ρ[′] ̸≡ 1) ·

Y T; Y=
_⊆_ _̸_ _◦̸_

; ; ;

###### · Pr(l PI Y(g ρ) ≥ s | fρ ≡ 1 g1ρ[′] ̸≡ 1 ρ[′](Y) ≡∗)

 since Pr(l PIY(g ρ) ≥ s | ρ[′](Y) ̸≡∗) = 0 . We claim that

 2p Y
; � �| _|_
###### Pr (ρ[′](Y) ≡∗| fρ ≡ 1 g1ρ[′](Y) ̸≡ 1) ≤ and (3.5)
 1 + p

; ;
###### Pr (l PI Y(g ρ) ≥ s | fρ ≡ 1 g1ρ[′] ̸≡ 1 ρ[′](Y) ≡∗) ≤ (2[|][Y][|] − 1) α[s][−|][Y][|] (3.6)

 hold. By (3.4) – (3.6) it is easy to estimate the second term in (3.3). We add in (3.4) the term for Y = which is estimated in (3.5) and ̸◦ (3.6) by 0 . Hence, by the definition of α

;
###### Pr (l PI(g ρ) ≥ s | fρ ≡ 1 g1ρ[′] ̸≡ 1) (3.7)


Y
###### �| | (2[|][Y][|] 1) α[s][−|][Y][|] −


###### � ≤

Y T
_⊆_


###### � 2p
 1 + p


###### �i (2[i] 1) α[−][i] −


###### α[s][ �] ≤

0 i T
_≤_ _≤|_ _|_


###### � T �� 2p | | i 1 + p


-----

**329**


i[�]
###### �


###### α[s][ �] ≤

0 i t
_≤_ _≤_


###### �t� [�]� 4p i (1 + p)α


###### �i � 2 p −
 (1 + p)α


###### �� 4 p = α[s] 1 +
 (1 + p)α


###### �t � 2 p 1 + −
 (1 + p)α


###### = α[s]


t[�]
###### �


:


###### Proof of (3.5) : The condition g1ρ[′] 1 is equivalent to the condition ̸≡

;
###### that ρ(xi) ∈{0 ∗} for xi ∈ T . Then ρ(xi) takes the values 0 and ∗

= =
###### with probability (1 − p) (1 + p) and 2p (1 + p) resp. Since all ρ(xi) are independent


###### 2p Y � �| | Pr(ρ[′](Y) ≡∗| g1ρ[′] ̸≡ 1) =
 1 + p


:
###### (3.8)


###### The additional condition fρ ≡ 1 implies a tendency that more variables are replaced by constants. Therefore the event ρ[′](Y) should have ≡∗ smaller probability. For a definite proof we use the equivalence of the inequalities Pr(A B) Pr(A) and Pr(B A) Pr(B) . For the proof of | ≤ | ≤ (3.5) it is by (3.8) and this equivalence sufficient to prove

; :
###### Pr(fρ ≡ 1 | ρ[′](Y) ≡∗ g1ρ[′] ̸≡ 1) ≤ Pr(fρ ≡ 1 | g1ρ[′] ̸≡ 1) (3.9)
 Two restrictions are called equivalent if they agree on all xi ̸∈ Y . It is sufficient to prove (3.9) for all equivalence classes. Each equivalence class contains exactly one restriction ρ where ρ[′](Y) ≡∗ . If fρ ̸≡ 1 or g1ρ[′] 1 for this restriction, the left-hand side of (3.9) equals 0 for this ≡ equivalence class and (3.9) holds. Otherwise fρ ≡ 1 for all ρ equivalent to ρ, since the additional replacement of variables does not influence a constant.

 Proof of (3.6) : We like to exclude g1 from our considerations. Then it is possible to apply the induction hypothesis. The condition ˝g1ρ[′] 1 ̸≡

;
###### and ρ[′](Y) ≡∗˝ is satisfied iff ρ[′](xi) ∈{0 ∗} for xi ∈ T and ρ[′](xi) = ∗ for xi ∈ Y . Here two restrictions are called equivalent if they agree on all xi ∈ T . It is sufficient to prove for a fixed equivalence class


###### Pr(l PI Y(g ρ) ≥ s | fρ ≡ 1) ≤ (2[|][Y][|] − 1) α[s][−|][Y][|]


:
###### (3.10)


-----

**330**

###### Each prime implicant t ∈ PI Y(g ρ) is of the form t = t[′] t[′′] for some
 monom t[′] on all variables in Y and some monom t[′′] on some variables
 xi ̸∈ T . If we replace the variables in Y such that t[′] is replaced by 1,
 we obtain a subfunction g ρ σ(t) of g ρ where t[′′] ∈ Π(g ρ σ(t)) . Since
 g1 is the sum of all xi T, t[′] contains at least one xi T . Hence ∈ ∈

;
###### l PI Y(g ρ) ≥ s only if there is some σ : Y →{0 1}, σ ̸≡ 0, such that the
 length of a longest prime implicant of g ρ σ (a monom on the variables
 xi ̸∈ T) is at least s −|Y|, notation l [∗]PI[(g][ ρ σ][)][ ≥] [s][ −|][Y][|][ . We conclude]

 Pr (l PI Y(g ρ) ≥ s | fρ ≡ 1) ≤ (3.11)


###### � : ≤ Pr (l [∗]PI[(g][ ρ σ][)][ ≥] [s][ −|][Y][| |][ f][ρ] [≡] [1)]

_σ:Y_ 0;1 ; σ 0
_→{_ _}_ _̸≡_

###### The right-hand side of (3.11) consists of 2[|][Y][|] 1 terms. It is sufficient −
 to estimate each of these terms by α[s][−|][Y][|] .

;
###### We fix some σ : Y 0 1, σ 0 . We have fixed ρ[′] σ but →{ } ̸≡
 ρ[′′] ∈ Rp is still a random restriction on the variables xi ̸∈ T . In order
 to apply the induction hypothesis we want to consider functions on
 the variables xi ̸∈ T . Let f[∗] be the conjunction of all functions which
 we obtain from fρ[′] by replacing the variables in (ρ[′])[−][1](∗) by constants.
 Then f[∗] is defined on the variables xi T . fρ[∗][′′][ ≡] [1 iff f][ρ][ ≡] [1 . Similarly] ̸∈
 let g[∗] be the conjunction of all functions which we obtain from g ρ[′] σ by
 replacing the variables in (ρ[′])[−][1]( ) (T Y) by constants. Then g[∗] is ∗ ∩ −
 defined on the variables xi ̸∈ T . The prime implicants of g[∗] are exactly
 those prime implicants of g ρ[′] σ containing only variables xi T . Let ̸∈
 gj[∗] [be defined in a similar way. Then g][∗] [= g]1[∗] m [. Since g][1][ is]
 [∧· · · ∧] [g][∗]
 the sum of all xi ∈ Y, g1[∗] [≡] [1 . For all legitimate replacements (g][j][)][ ρ][′][ σ] is replaced by a constant or by some definite function gj[′] [. Hence, if]
 j ≥ 2, gj[∗] [is a sum of at most t literals and g][∗] [is the conjunction of]
 m − 1 of those gj[∗] [. Since we have also shown that f][∗] [and g][∗] [are defined]
 on the variables xi ̸∈ T and that ρ[′′] ∈ Rp is a random restriction, it is


-----

**331**

###### possible to apply the induction hypothesis. We conclude

 Pr(l [∗]PI[(g][ ρ σ][)][ ≥] [s][ −|][Y][| |][ f][ρ][ ≡] [1) =] (3.12)


###### = Pr(l PI(g[∗]ρ[′′][)][ ≥] [s][ −|][Y][| |][ f]ρ[∗][′′][ ≡] [1)][ ≤] [α][s][−|][Y][|]


:


###### 2

 The Main Lemma has many applications. The most appropri- ate function is the parity function, as all prime implicants and prime clauses of the parity function have length n, and all subfunctions are parity functions or negated parity functions.

 LEMMA 3.4 : For some constant n0, n ≥ n[k]0[−][1] and k ≥ 2 the parity function on n variables cannot be computed by a Σk- or Πk-circuit

=
###### which for s = t = (1 10) n[1][=][(k][−][1)] simultaneously has 1-fan-in bounded

; : : : ;
###### by t and at most 2[s] gates on the levels 2 k .

 Proof : Induction on k . The claim is obvious for k = 2 since Σ2- and Π2-circuits for the parity function have 1-fan-in n .
 We assume that the assertion holds for k − 1 but not for k . Let Sn be depth k circuits for x1 xn such that the 1-fan-in is bounded ⊕· · · ⊕

; : : : ;
###### by t, and the number of gates on the levels 2 k is bounded by 2[s] . W.l.o.g. the second level is an -level. The gates of this level are ∧ outputs of Π2-circuits with 1-fan-in t . We apply the Main Lemma for p = n[−][1][=][(k][−][1)] . The expected number of remaining variables is m = n p = n[(k][−][2)][=][(k][−][1)] . For large n, the probability that at least m variables

=
###### are left is larger than 1 3 . For each Π2-circuit the probability of the circuit being converted to an equivalent Σ2-circuit of 1-fan-in s is at

< =
###### least 1 α[s] . For large n, α 5 pt = 1 2 . Hence the probability of − less than m variables being left or some Π2-circuit cannot be converted

= <
###### in the described way is bounded by (2 3) + (2α)[s] . Since 2α 1, this probability is less than 1 for large n . Then there is a partial


-----

**332**

###### replacement of variables such that the circuit computes the parity of m = n[(k][−][2)][=][(k][−][1)] variables, and all Π2-circuits can be converted to

= =
###### equivalent Σ2-circuits of 1-fan-in s = (1 10) n[1][=][(k][−][1)] = (1 10) m[1][=][(k][−][2)] . Afterwards the second and the third level are -levels, and by merging ∨ them the depth of the circuit will decrease to k 1 . The number of −

; : : : ;
###### gates on the levels 2 k 1 has not increased and is bounded by 2[s] . − Since n ≥ n0[k][−][1], also m ≥ n0[k][−][2] . It is easy to prove that all conclusions hold for n ≥ n0[k][−][1] . The depth k−2 circuit for the parity of m variables contradicts the induction hypothesis. 2

 Now it is easy to prove Theorem 3.1.

 Proof of Theorem 3.1 : If the theorem is false, there is a depth k circuit for the parity of n ≥ n[k]0 [variables with at most 2][s][ gates, s =]

=
###### (1 10)[k][=][(k][−][1)]n[1][=][(k][−][1)] . This circuit can be understood as a depth k + 1

= =
###### circuit of 1-fan-in 1 . Let p = 1 10 and ρ ∈ Rp . If p = 1 10 and

=
###### t = 1, then α = 2 11 . If n0 is chosen in the right way, there is a

=
###### restriction such that the circuit computes the parity on m = n 10 variables, and all (w.l.o.g.) Π2-circuits on level 2 can be converted to

=
###### equivalent Σ2-circuits of 1-fan-in s . If n0 ≥ 10, m = n 10 ≥ n[k]0[−][1] .

=
###### Furthermore s = (1 10)m[1][=][(k][−][1)] . The new depth k circuit for the parity on m variables contradicts Lemma 3.4, since the number of

; : : : ;
###### gates on the levels 2 k is bounded by 2[s] . 2

 11.4 The complexity of symmetric functions

 Upper and lower bounds on the depth k complexity of the parity function almost agree, the upper bound is based on a simple design. For all symmetric and almost all Boolean functions we decide in this


-----

**333**

;
###### section whether they belong to SIZE - DEPTH(poly const) (Brust- mann and Wegener (86)). Our results are based on the lower bound techniques due to H˚astad (86). Weaker results based on the lower bound technique due to Furst, Saxe and Sipser (84) have been ob- tained by Fagin, Klawe, Pippenger and Stockmeyer (85) and Denen- berg, Gurevich and Shelah (83). It is fundamental to know a lower bound for the majority function.

 THEOREM 4.1 : For some constant n0 and all n ≥ n[k]0 [Σ][k][- and Π][k][-]
 circuits for the majority function have more than 2[c(k) n][1][=][(k][−][1)] gates,

= =
###### c(k) = (1 10)[k][=][(k][−][1)] 1 10 . ≈

 Proof : This theorem has been proved by H˚astad (86) in a way similar to his bound for the parity function. The analysis of the probabilities is harder, since we have to ensure that the restriction gives out the same number of ones and zeros.

 We are satisfied with the proof of a weaker bound based on the reducibility of parity to majority. Let Ck(MAJn) be the Σk-complexity of the majority function. By duality the Πk-complexity is the same. With less than n Ck(MAJn) gates we compute in Πk-circuits E[⌈]l [n][=][2][⌉] = Tl[⌈][n][=][2][⌉] ∧ (¬Tl[⌈]+1[n][=][2][⌉][) for all odd][ l] ∈{1; : : : ; ⌈n=2⌉} . PAR⌈n=2⌉ is the disjunction of these E[⌈]l [n][=][2][⌉] . Hence

 Ck+1(PAR⌈n=2⌉) ≤ n Ck(MAJn) (4.1)

 and by Theorem 3.1


###### Ck(MAJn) ≥ n[−][1] 2[c(k+1) (n][=][2)][1][=][k] for n ≥ n[k+1]0


:
###### (4.2)

 2


###### From now on we denote by Ck(f) the depth k complexity of f . We require some results on the structure of symmetric functions.

; : : : ;

###### DEFINITION 4.1 : Let v(f) = (v0 vn) be the value vector of
 a symmetric function f ∈ Sn . By vmax(f) we denote the length of a


-----

**334**

###### longest constant substring of v(f) . For f ∈ Bn let l min(f) be the length of a shortest prime implicant or prime clause.

 LEMMA 4.1 : l min(f) = n + 1 − vmax(f) for f ∈ Sn .

 Proof : A prime implicant t of length k with l variables and k l − negated variables implies vl = · · · = vn−k+l = 1 and therefore the existence of a constant substring of v(f) of length n + 1 k . Fur- − thermore, we obtain a maximal constant substring. If vl −1 = 1 or vn−k+l +1 = 1, we could shorten t by a variable or negated variable resp. If vl = · · · = vn−k+l = 1 is a maximal constant substring of v(f), then the monom x1 xl xl +1 xk is a prime implicant of f of · · · · · · length k . Dual arguments hold for prime clauses and substrings of v(f) consisting of zeros. 2

=
###### THEOREM 4.2 : For c(k) = (1 10)[k][=][(k][−][1)] we denote by H(n,k) H˚astad’s lower bound function 2[c(k)n][1][=][(k][−][1)] .
 i) If fn Sn and l = l min(fn) = O(log[r] n) for some constant r, then ∈

;
###### f = (fn) ∈ SIZE - DEPTH(poly const) .

=
###### ii) If fn ∈ Sn and l = l min(fn) ≤ (n + 1) 2, then for l ≥ n[k+1]0

; = :
###### Ck(fn) ≥ H(l k + 1) l (4.3)

         - =
###### iii) If fn Sn and l = l min(fn) (n + 1) 2, then for w = vmax(fn) and ∈ w ≥ n[k+1]0

; = ; = :
###### Ck(fn) ≥ H(w k + 1) w ≥ H(n + 1 − l k + 1) l (4.4)
 iv) If fn ∈ Bn (not necessarily symmetric) and l min(fn) ≥ n − O(log[r] n) for some constant r, then for constant k and large n

; :
###### Ck(fn) ≥ H(n k) (4.5)

; : : : ;

###### Proof : We identify the vector (v0 vn) with the string v0 vn .
 · · · By duality we assume that there is always a maximal constant sub- string consisting of zeros. For w = vmax(fn), v(f) = s 0[w] s[′] . W.l.o.g. (otherwise we negate the variables) s is not longer than s[′] .


-----

**335**

###### i) vi = 1 only for some i ≤ l − 1 and some i ≥ n − l + 1 . fn is the disjunction of all T[n]i i+1[) where v][i][ = 1 . By Theorem 2.2 and by]
 [∧] [(][¬][T][n]

;
###### duality all these functions are in SIZE - DEPTH(poly const) .

=
###### ii) By our assumptions s[′] = 1 t, and the length of s[′] is at least l 2 . ⌈ ⌉ Since w l, v(f) contains the substring 0[l] 1 t where the length of t is ≥

= =
###### at least ⌈l 2⌉− 1 . For ⌈l 2⌉≤ m ≤ l let gm ∈ Sl be that symmetric function whose value vector is a substring of 0[l] 1 t starting with 0[m]1 .

=
###### All these value vectors start with ⌈l 2⌉ zeros, and gm computes 1 for inputs with exactly m ones. Hence the disjunction of all gm is the majority function on l variables. Since all gm are subfunctions of fn

= :
###### Ck+1(MAJl ) ≤ (⌊l 2⌋ + 1) Ck(fn) + 1 (4.6)

 The lower bound (4.3) follows from Theorem 4.1.

=
###### iii) By Lemma 4.1 w (n + 1) 2 . Hence v(f) contains a substring ≤

=
###### 0[w]1t where the length of t is at least w 2 1 . The lower bound ⌈ ⌉− (4.4) follows from similar arguments as (4.3).

 iv) It is sufficient to prove that we can copy H˚astad’s proof for these functions. The Main Lemma works for all fn Bn . In the proof ∈ of Lemma 3.4 and Theorem 3.1 only a few properties of the parity

                - =
###### functions are used, namely the facts that l min(PARn) = n n 10 and that each subfunction of a parity function is a function of the same type.

 l min(f) is the minimum number of variables which have to be re- placed by constants in order to obtain a constant subfunction. Hence l min(g) ≥ l min(f) − (n − m) if g ∈ Bm is a subfunction of f ∈ Bn . In his lower bound proof for depth k circuits H˚astad constructed subfunc
; ; : : : ; ; =

###### tions on n[(k][−][2)][=][(k][−][1)] n[(k][−][3)][=][(k][−][1)] n[1][=][(k][−][1)] (1 10)n[1][=][(k][−][1)] variables.
 For these functions g ∈ Bm we have l min(g) ≥ m − O(log[r] n) = m O(log[r] m) . All these functions belong to the class of functions − with large l min-value. Since l min(g) is a lower bound on the 1-fan-in of depth 2 circuits for g, the lower bound (4.5) can be proved by H˚astad’s

            - =
###### proof, if n is large enough so that l min(g) m 10 . 2


-----

**336**

###### COROLLARY 4.1 : Let f = (fn) where fn Sn . ∈

;
###### Then f ∈ SIZE - DEPTH(poly const) iff l min(fn) = O(log[r] n) for some constant r .

 Proof : The if-part is Theorem 4.2 i. The only if-part follows from the definition of H˚astad’s function and the lower bounds in Theo- rem 4.2 ii – iv. 2

;
###### COROLLARY 4.2 : Ck(f) ≥ H(n k) for almost all f ∈ Bn .

 Proof : Bublitz, Sch¨urfeld, Voigt and Wegener (86) investigated prop- erties of l min and proved the following assertion (see Theorem 7.8, Ch. 13). l min(f) ∈ In for almost all f ∈ Bn and intervals In where n −⌊log n⌋∈ In and the length of In is smaller than 2 . Hence the corollary follows from Theorem 4.2 iv. 2

 The bounds we have proved depend only on l min(f). Is it reasonable to conjecture that Ck(f) depends for all f ∈ Bn essentially only on l min(f) ? The answer is negative. Let n = m[2] and let the set of variables be partitioned to m blocks of size m each. Let hn compute 1 iff at least one block contains ones only. Then l min(hn) = m = n[1][=][2]
 but hn has linear depth 2 circuits.
 For symmetric functions l min(f) describes rather precisely the size and the structure of the set of all prime implicants and prime clauses and therefore the complexity of f . If l min(f) is not too small, a random subfunction of f is with large probability not a simple function. The same holds for arbitrary Boolean functions only if l min(f) is very large. For hn defined above, l min(hn) is quite large. It is highly probable that a random subfunction of hn is a constant.


-----

**337**

###### 11.5 Hierarchy results

 We have proved that the parity function has large complexity with respect to depth k circuits. This lower bound implies many others by the reducibility results of Ch. 10, 3. What happens if unbounded § fan-in parity gates are added to the set of admissible gates ? Then ZMc is easy to compute, since ZMc ≤cd PAR . Razborov (86) proved

; ;
###### that the complexity of the majority function in depth k - {∧ ∨ ⊕} circuits of unbounded fan-in is exponential. This holds also for all functions f with MAJ ≤cd f . It is an open problem to decide which functions are difficult in depth k circuits consisting of threshold gates of unbounded fan-in.

 Razborov’s new and striking result belongs to the class of hierarchy results, since we increase the power of the basis in order to be able to solve more problems with polynomial circuits. We turn our thoughts to another type of hierarchy results.

 DEFINITION 5.1 : Let Σk(P) and Πk(P) be the class of all sequences f = (fn) of functions fn Bn which can be computed by polynomial ∈ Σk-circuits and Πk-circuits resp. Σ[m]k [(P) and Π]k[m][(P) are defined in a] similar way with respect to monotone depth k circuits.

 Obviously for all k

; ;
###### Σk(P) ⊆ Σk+1(P) ⊆ SIZE - DEPTH(poly const) (5.1)

; ;
###### Πk(P) ⊆ Πk+1(P) ⊆ SIZE - DEPTH(poly const) (5.2)

;
###### Σk(P) ⊆ Πk+1(P) Πk(P) ⊆ Σk+1(P) and (5.3)
 Σ[m]k [(P)][ ⊆] [Σ][k][(P)][ ∩{][f = (f][n][)][ |][ f][n][ ∈] [M][n][}][:] (5.4)

 The problem is whether these inclusions are proper. The answer is always positive. This has been proved by Okol’nischkova (82) for (5.4) and by Sipser (83) for (5.1) – (5.3). Sipser’s proof is non constructive. One is interested in explicitly defined functions which separate the


-----

**338**

###### complexity classes. This was first done by Klawe, Paul, Pippenger and Yannakakis (84) for monotone depth k circuits and then by Yao (85) in the general case.

 DEFINITION 5.2 : Let n = m[k] . Let us denote the variables by xi(1); ::: ;i(k) [(1][ ≤] [i(j)][ ≤] [m) . Let Q =][ ∃] [, if k is odd, and Q =][ ∀] [, if k is] even. Then Fk;n(x) = 1 iff the predicate

 ∃ i(1) ∀ i(2) ∃ i(3) : : : Q i(k) : xi(1); ::: ;i(k) [= 1] (5.5)

 is satisfied.

 In the preceding section we discussed already F2;n = hn .

 THEOREM 5.1 : Let Fk = (Fk;n) . Then Fk ∈ Σ[m]k [(P), but all depth] k − 1 circuits for Fk have exponential size.

 Again H˚astad (86) proved similar results with simpler proofs. We do not present the proofs which are based on the lower bound method for the parity function.

 Such hierarchy results have further implications. Furst, Saxe and Sipser (84) have shown tight relations to classical complexity problems. The results of this chapter imply that the complexity classes Σk and Σk+1 (see Def. 1.4, Ch. 9) as well as the complexity classes Σk and PSPACE can be separated by oracles.

 EXERCISES

 1. If a Σk-formula is defined on n variables and consists of b gates, then the number of wires can be bounded by b (n + b) and the number of leaves can be bounded by b n .


-----

**339**

###### 2. Let f be computed by a Σk-circuit of size c . Estimate the Σk- formula size of f .

 3. (Chandra, Stockmeyer and Vishkin (84)). Let fn Bn be com- ∈

                  ###### puted by circuits of cn binary gates and depth dn . For ε 0,

=

###### fn can be computed in depth O(dn (ε log logn)) circuits with
 O(2[(log n)][ε] cn) gates of unbounded fan-in.

 4. Prove upper bounds on the depth k complexity of the majority function. Hint: Exercise 3.

 5. (Chandra, Fortune and Lipton (83)). There is a constant k such that all x1 ∨· · · ∨ xi (1 ≤ i ≤ n) can be computed by a Σk-circuit with O(n) wires.

 6. Design good Σk-circuits for Fk;n .

 7. Prove Theorem 2.3 i for all n .

 8. Prove Lemma 3.1.

 9. Define l max and vmin in the dual way to l min and vmax . Then l max(f) + vmin(f) = n + 1 for f ∈ Sn .

;
###### 10. Ck(f) ≥ H(n k) for almost all f ∈ Sn .

 11. Let p(f) be the number of prime implicants and prime clauses of f . Prove for f ∈ Sn upper and lower bounds on p(f) depending on l min(f).


-----

**340**

###### 12. SYNCHRONOUS, PLANAR AND PROBABILISTIC CIRCUITS

 In this chapter we investigate some more circuit models. Circuits should be synchronized and it should be possible to embed the cir- cuits on chips of small area. In the last section we discuss efficient simulations of probabilistic circuits by deterministic circuits.

 12.1 Synchronous circuits

 DEFINITION 1.1 : A synchronous circuit is a circuit with the ad- ditional property that all paths from the inputs to some gate G have the same length.

 In Ch. 11 we have considered only synchronous bounded-depth circuits, since this restriction does not change essentially the model of bounded-depth circuits. Let Cs and Ds be the complexity measures for synchronous circuits with binary gates. We remember that PCD(f) is the product complexity (see Def. 3.1, Ch. 7), namely the minimal C(S) D(S) for all circuits S computing f .

 THEOREM 1.1 : i) Ds(f) = D(f) for all f ∈ Bn .
 ii) Cs(f) ≤ PCD(f) ≤ C(f)[2] for all f ∈ Bn .

 Proof : i) and the second inequality of ii) are obvious. Let S be a circuit for f where C(S) D(S) = PCD(f) . For each gate G, let d(G) be the length of the longest path to G . Let G1 and G2 be the direct predecessors of G, w.l.o.g. d(G1) ≥ d(G2) . Then d(G1) = d(G) − 1 . We add a path of d(G) − d(G2) − 1 identity gates to the edge from G2


-----

**341**

###### to G . The resulting circuit S[′] is synchronous, for each G in S we have added at most D(S) − 1 gates. Hence Cs(f) ≤ C(S[′]) ≤ C(S) D(S) . 2

 If we had proved ω(n log n) lower bounds on the synchronous circuit size of explicitely defined Boolean functions, we would obtain for the first time similar bounds for the product complexity. The best we can prove are lower bounds of size n log n .

 THEOREM 1.2 : The synchronous circuit size of the addition of two n-bit numbers is Θ(n log n) .

; : : : ;

###### Proof : The upper bound is left as an exercise. Let s = (sn s0) be

; : : : ; ; : : : ;

###### the sum of a = (an−1 a0) and b = (bn−1 b0) . si depends essen tially on ai ; bi ; : : : ; a0 ; b0 . Hence the depth of sn ; : : : ; s⌈n=2⌉ is at least
 ⌈log n⌉ . The vector (sn ; : : : ; s⌈n=2⌉) can take all 2[m] values in {0; 1}[m]

= ; : : : ;
###### where m = ⌊n 2⌋ + 1 . Let G1 Gr be those gates whose depth
 equals d log n . These gates build a bottleneck for the informa- ≤⌈ ⌉ tion flow from the inputs to the outputs sn ; : : : ; s n=2 . If r < m, we

_⌈_ _⌉_

=
###### could not distinguish between 2[m] situations. Hence r m n 2, and ≥ ≥

=
###### the circuit contains at least (1 2) n logn gates. 2


###### This result implies that the size of each synchronous adder is con- siderably larger than the size of an optimal asynchronous adder. For functions f with one output no example in which C(f) = o(Cs(f)) is known. One might think that the carry function cn, the disjunction of all ui vi+1 · · · vn (0 ≤ i ≤ n), is a candidate for such a gap (see also Ch. 7, § 4). But Cs(cn) is linear (Wippersteg (82)). Harper (77) and Harper and Savage (79) generalized the bottleneck argument of The- orem 1.2 to functions with one output. The gates on level l D(f) ≤ contain all necessary information on f and all subfunctions of f . There- fore the number of gates on level l cannot be small if f has many subfunctions.

;
###### DEFINITION 1.2 : For f ∈ Bn let N(f A) be the number of sub
; : : : ;

###### functions g of f on the set of variables A ⊆ X = {x1 xn} . Let


-----

**342**


1

; �n�− � ;
###### N[′](f a) = log N(f A) (1.1) a

A X; A =a
_⊆_ _|_ _|_

;
###### be the average of all log N(f a) for A = a . | |

;
###### If N[′](f a) is large, f has many subfunctions. If also D(f) is large, the number of gates on many levels cannot be very small. Hence Cs(f) cannot be very small either.


###### LEMMA 1.1 : Let f ∈ Bn depend essentially on the b variables in

<

###### B . If r = 2 a b (n a b + 1)[−][1] 1, then − −


1

###### �n�−
; �
###### N[′](f a) ≤ a

0 k b
_≤_ _≤_


###### �b��n b�
 −
 2[k] (1 r)[−][1] ≤ −
 k a k
 −


:
###### (1.2)


###### Proof : The number of sets A X of size a where A B = k equals ⊆ | ∩ |
b n b
###### � �� − � . The subfunctions of f on these sets A depend essentially at
k a k
_−_

;
###### most on the variables in A B . Hence log N(f A) 2[k] implying the ∩ ≤ first inequality.

b n b
###### � �� − � Let s(k) = 2[k] . Then
k a k
_−_

###### a k −
 q(k) := [s(k + 1)] = 2 [b][ −] [k] (1.3)
 s(k) k + 1 n a b + 1 + k
 − −


###### ab 2 ≤
 n a b + 1 [= q(0)][:] − −


<
###### Since q(0) = r 1, we estimate the sum by a geometric series.

1 1

###### �n�− �n�− �n b
 � − �� :
 s(k) r[k] (1 r)[−][1] (1.4) ≤ ≤ −
 a a a

0 k b 0 k b
_≤_ _≤_ _≤_ _≤_

###### 2


###### THEOREM 1.3 : If f ∈ Bn and

=
###### D(f) d := log(δ(n a + 1) (2a + δ)) (1.5) ≥ ⌊ − ⌋

< < ; : : : ;
###### for some 0 δ 1 and a 1 n, then ∈{ }


-----

**343**

; :
###### Cs(f) ≥ (1 − δ) d N[′](f a) (1.6)

 Proof : It is sufficient to prove that each synchronous circuit for f

; : : : ; ;
###### contains on level l 1 d at least (1 δ) N[′](f a) gates. Let ∈{ } −

; : : : ; ; : : : ;

###### G1 Gm be the gates on level l and let g1 gm be the func tions computed at these gates. Since f(x) is determined by g(x) =

; : : : ;
###### (g1(x) gm(x)),


; ; �
###### N(f A) ≤ N(g A) ≤ N(gi

1 i m
_≤_ _≤_


;
###### A) (1.7)


###### and by taking the logarithm and computing the average


; � ; :
###### N[′](f a) ≤ N[′](gi a) (1.8)

1 i m
_≤_ _≤_


###### Since D(gi) ≤ l ≤ d, gi depends essentially on at most 2[d] ≤

=
###### δ(n a+1) (2a+δ) =: b variables. For this choice of b, the parameter r −

<
###### defined in Lemma 1.1 equals δ . Hence r 1 and by Lemma 1.1


###### N[′](gi


; :
###### a) (1 δ)[−][1] (1.9) ≤ −


###### By (1.8) and (1.9)

;
###### N[′](f a) m (1 δ)[−][1] (1.10) ≤ −

; : : : ;
###### and the number of gates on each level l 1 d is at least ∈{ }

;
###### (1 δ) N[′](f a). 2 −

 Obviously the lower bound of Theorem 1.3 cannot be larger than O(n log n) . Harper and Savage (79) proved by this theorem an Ω(n log n) lower bound on the synchronous circuit size of the determi- nant (see Def. 7.1, Ch. 3).


-----

**344**

###### 12.2 Planar and VLSI - circuits

 The theory of VLSI-circuits is too extensive to be presented in a short section. For the technological aspects we refer to the monograph of Mead and Conway (80) and for the aspects of the complexity theory to Ullman (84). We discuss only the fundamental model of VLSI- circuits (Brent and Kung (80), Thompson (79) and (80)), some lower bound techniques and some relations to planar circuits.

 DEFINITION 2.1 : A graph is planar if it can be embedded in the plane in such a way that no edges cross each other. A circuit is planar if its underlying graph is planar. C[∗]p[(f) is the planar circuit size of f if] the inputs can be copied. Cp(f) is the planar circuit size of f ∈ Bn;m if the inputs and outputs of the circuit occur once on an outer circle in

; : : : ; ; ; : : : ;

###### the order x1 xn fm(x) f1(x) .


###### We talk about planar -circuits and planar circuits shortly. Formu- ∗ las can be simulated directly by planar -circuits. For planar circuits ∗ we need planar circuits for crossings.

; ;
###### LEMMA 2.1 : Let f(y z) = (z y) . Then Cp(f) = 3 .


###### Proof :


y z

z y


###### Fig. 2.1

|y|Col2|z|
|---|---|---|
||y||
||||


###### 2


###### THEOREM 2.1 : C(f) ≤ C[∗]p[(f)][ ≤] [C][p][(f)][ ≤] [6 C(f)][2][ for all f][ ∈] [B][n][ .]


-----

**345**

###### Proof : The first two inequalities follow from the definition. For the last inequality we consider an optimal circuit S for f . Let c = C(f) .

; ;
###### We embed input xi at (i 0) and gate Gj at (0 −j) . An edge e from xi or Gi to Gj is embedded by a continuous function αe = (αe;1 ; αe;2)
 where αe;k : [0; 1] → R for k ∈{1,2}, αe(0) = (i; 0) or αe(0) = (0; −i) resp. and αe(1) = (0; −j) . We define all embeddings such that αe;2 is

; : : : ;

###### decreasing. If the edges leading to G1 Gi−1 are embedded, then
 we embed the two edges leading to Gi in such a way that all previous edges are crossed once at most. Since the circuit contains 2 c edges, �2 c� the number of crossings is bounded by = c (2 c 1) . We replace
2 _−_
###### each crossing by the planar circuit of Lemma 2.1. In addition to the c gates of S we obtain at most 3 c (2 c 1) new gates. 2 −


###### The same ideas work for functions f ∈ Bn;m with many outputs. If we ensure that the outputs are computed at the last gates, they can be embedded on an outer circle of the planar circuit. For this purpose it is sufficient to add at first m 1 new output gates. −
 The following claim is used implicitly in many papers.

 CLAIM : If f is computed in a circuit with c gates and d crossings of edges, then Cp(f) ≤ c + 3d .

 The Claim seems to be obvious. We only have to replace each crossing by the planar circuit of Lemma 2.1. As was pointed out by McColl (pers. comm.) this is no proof of the Claim. It is not for sure that the produced circuit is cycle-free. Let us consider a circuit, like the sorting circuit in Ch. 3, 4, whose width is linear at the top and § at the bottom, but only logarithmic in the middle (see Fig. 2.2). Let G be the leftmost gate, and let G[′] be the rightmost gate at the bottom of the circuit. Let us assume that we like to compute at G[′′], a new leftmost output, the conjunction of resG and resG[′] . We minimize the number of crossings, if we embed the edge from G[′] to G[′′] as described

; ;
###### in Fig. 2.2. The edges e[′] = (v w) and e[′′] = (G[′] G[′′]) lying on the same
 path cross.


-----

**346**


: : : : : : : : :

###### x1 xn

 . . . . . . .G[′]
 G


###### Fig. 2.2


###### If we replace this crossing by the planar circuit of Lemma 2.1, we ob- tain a cycle starting at w leading via G[′] to the z-input of the ˝crossing- circuit˝, then leading to the y-output of the ˝crossing-circuit˝ and back to w .

 This problem does not occur for our embedding in the proof of Theorem 2.1. All edges are embedded top-down. If some edges e and e[′] lie on the same path, their embeddings do not cross.
 Theorem 2.1 implies an upper bound of O(2[2n] n[−][2]) on the planar circuit complexity of all f ∈ Bn . Savage (81) improved this simple bound.

 THEOREM 2.2 : i) C[∗]p[(f)][ ≤] [(2 + o(1)) 2][n][ log][−][1][ n for all f][ ∈] [B][n][ .]
 ii) Cp(f) ≤ 5 · 2[n] for all f ∈ Bn .

 Proof : i) follows from Theorem 3.2, Ch. 4, and the fact that C[∗]p[(f)][ ≤]

; : : : ;

###### L(f) . For the proof of ii) we compute all minterms on x1 xn . If all

; : : : ;

###### 2[i][−][1] minterms on x1 xi−1 are computed, we take a wire starting at
 xi . This wire runs at the right hand side of the circuit to its bottom


-----

**347**

; : : : ;

###### and crosses all 2[i][−][1] wires for the monoms m on x1 xi−1 . Then we
 compute all m xi and m xi . We have used 2[i] gates for the computation of the minterms and 3 2[i][−][1] gates for the crossings, i.e. 5 2[i][−][1] gates · · in Step i . For all steps the number of gates is bounded by 5 2[n] . f or · f is the disjunction of at most 2[n][−][1] minterms. If we do not compute ¬ unnecessary minterms in Step n, f or f can be computed with 5 2[n] ¬ ·
 gates. The Claim is proved, as Cp(f) = Cp(¬f) . 2

 The upper bound on Cp(f) has been improved by McColl and Pa
=
###### terson (84) to (61 48) 2[n] . McColl (85 b) proved that for almost all

= =
###### f ∈ Bn the planar circuit complexity is larger than (1 8) 2[n] − (1 4) n . This implies that C[∗]p[(f) = o(C][p][(f)) for almost all f][ ∈] [B][n][ .]

 With information flow arguments and the Planar Separator Theo- rem due to Lipton and Tarjan ((79) and (80)), Savage (81) proved Ω(n[2])-bounds on the planar circuit complexity of several n-output functions. Larger lower bounds imply (due to Theorem 2.1) nonlinear bounds on the circuit complexity of the same functions.

 The investigation of planar circuits is motivated by the realization

                  ###### of circuits on chips. Today, chips consist of h levels, where h 1 is a small constant. We introduce the fundamental VLSI-circuit model.

      ###### For some constant λ 0, gates occupy an area of λ[2], and the min- imum distance between two wires is λ . A VLSI-circuit of h levels on a rectangular chip of length l λ and width w λ consists of a three- dimensional array of cells of area λ[2] . Each cell can contain a gate, a wire or a wire branching. Wires ˝cross˝ each other at different levels of the circuit. A crossing of wires occupies a constant amount of area. The area occupied by a wire depends on the embedding of the circuit.

 VLSI-circuits are synchronized sequential machines. The output of gate G at the point of time t may be the input of gate G at the point of time t + 1, i.e. the circuits are in general not cycle-free. For each input there is a definite input port, a cell at the border of the chip,


-----

**348**

###### where and a definite point of time when it is read. In particular, no input is copied. For each output there is a definite output port where and a definite point of time when it is produced.

 The following complexity measures are of interest. A = l w, the area of the chip, T, the number of clock cycles from the first reading of an input to the production of the last output, and P, the period. VLSI-circuits may be pipelined, i.e. we may start the computation on the next input before the last computation is finished if this causes no problem. P is the minimum number of clock cycles between the

=
###### starting of two independent computations. D := n P is called the data rate of the circuit.

; : : : ;

###### We consider the addition of a = (an 1 a0) and b =
_−_

; : : : ;

###### (bn 1 b0) . At first we use only one synchronized fulladder of
_−_

;

###### depth d . At the point of time d t + 1, at bt and the carry bit ct−1
 are the inputs of the fulladder. Hence A = Θ(1), T = dn and

;

###### P = T − d + 1 . If we connect n fulladders in series and input at bt
 and ct−1 to the (t + 1)-st fulladder at the point of time d t + 1, then A = Θ(n), T = d n and P = 1 . It turned out that A T[2] is the appropriate complexity measure (see Ullman (84)).

 Relations between (planar) circuits and VLSI-circuits have been studied by Savage ((81) and (82)). For each clock cycle a VLSI-circuit is a circuit with at most h A gates. We simulate the T clock cycles by T copies of the circuit for one clock cycle. This implies the following theorem.

 THEOREM 2.3 : If f ∈ Bn;m is computed by a VLSI-circuit of area A in time T, then C(f) h A T . ≤

 The T copies of the VLSI-circuits can be embedded in the plane

;
###### in such a way that we obtain at most O(A T min(A T)) = O(A T[2]) crossings of wires.

 What is the VLSI-complexity of almost all Boolean functions ? The planar circuit in the proof of Theorem 2.2 has some very long wires.


-----

**349**

###### Therefore a divide-and-conquer approach for the computation of all minterms is used. Using the H-pattern due to Mead and Rem (79), Kramer and van Leeuwen (82) designed VLSI-circuits for each f ∈ Bn where A = O(2[n]), T = O(n) and P = O(1) . This is optimal for almost all f ∈ Bn . The result on P is obviously optimal. The result on T cannot be improved, since D(f) is a lower bound on the number of clock cycles of a VLSI-circuit. Finally there is only a finite number of types of cells. Hence the number of different circuits on a chip of area A is O(c[A]) for some constant c . In order to compute all f ∈ Bn, A = Ω(2[n]) for almost all f ∈ Bn .
 There is a large number of design methods for VLSI-circuits. So we make no attempt to present these methods. Most of the lower bounds are proved by information flow arguments. We present the method due to Vuillemin (83) leading to Ω(n[2])-bounds on AT[2] for several fundamental functions.

 DEFINITION 2.2 : Let Σn be the symmetric group of all permu
; : : : ;
###### tations on 1 n . A subgroup G of Σn is called transitive if for all

; ; : : : ;
###### i j 1 n there is some π G where π(i) = j . ∈{ } ∈

 DEFINITION 2.3 : f ∈ Bn+m;n is called transitive of degree n if there is some transitive subgroup G of Σn such that for each π ∈ G there is

; : : : ;

###### some y[π] = (y1[π] ym[π] [) where]


; : : : ;
###### ym[π] [) = (x][π][(1)]


;
###### y1[π]


; : : : ; :
###### xπ(n)) (2.1)


###### f(x1


; : : : ;
###### xn


###### If f is transitive of degree n, it must be possible to transport the i -th input bit (1 i n) to the j -th output port. This data flow ≤ ≤ is possible in a short time only on a large area. Hence we hope to prove nontrivial lower bounds on A T[2] for functions f transitive of high degree. At first we present examples of transitive functions of high degree.


###### DEFINITION 2.4 : CYCSH : cyclic shifts. Input: x0


; : : : ;
###### xn−1,


-----

**350**

; : : : ;

###### y1 ym where m = ⌈log n⌉ . Let y be the binary number represented

; : : : ; ; : : : ;

###### by (y1 ym) . Output: z0 zn−1 where zi = x(i+y)modn .

; ;
###### MUL : Input: n-bit numbers x y M . Output: the n-bit number z xy mod M . ≡
 CYCCON : Cyclic convolution. Input: 2 n k-bit numbers

; ; : : : ; ; ; : : : ;

###### x0 y0 xn−1 yn−1 . Output: n k-bit numbers z0 zn−1 where


###### � : zl ≡ xi yj mod M for M = 2[k] − 1 (2.2)

i+j _l modn_
_≡_


; : : : ;

###### MVP : matrix-vector-product. Input: n k-bit numbers x1 xn and

;
###### an n× n-matrix Y = (yij) where yij ∈{0 1} . Output: n k-bit numbers

; : : : ;

###### z1 zn where
 zl ≡ � yl ixi mod M for M = 2[k] − 1: (2.3)

1 i n
_≤_ _≤_


###### 3-MATMUL : multiplication (modM for M = 2[k] 1) of three n n- − × matrices of k-bit numbers.

 LEMMA 2.2 : CYCSH and MUL are transitive of degree n, CYCCON and MVP are transitive of degree n k, and 3-MATMUL is transitive of degree n[2] k .

 Proof : CYCSH : Let G be the transitive group of all cyclic shifts πj where πj(i) ≡ (i + j) mod n . CYCSH computes this group by defi- nition.

; : : : ;
###### MUL : We fix M = 2[n] 1 and y = 2[s] for some s 0 n 1 . − ∈{ − } Then 2[n] 1 mod M and ≡

 � z ≡ x y = xi 2[i+s] (2.4)

0 i n 1
_≤_ _≤_ _−_

###### � � : ≡ xi 2[i+s] + xi 2[i+s][−][n] mod M

0 i n s 1 n s i n 1
_≤_ _≤_ _−_ _−_ _−_ _≤_ _≤_ _−_


; : : : ; ; ; : : : ;

###### The binary representation of z is (xn s xn 1 x0 xn s 1) and
_−_ _−_ _−_ _−_

###### the cyclic shift πn−s is computed. Hence MUL computes the transitive group of cyclic shifts.


-----

**351**

###### CYCCON : Let G be the group of all permutations πi;j (0 ≤ i < n, 0 ≤ j < k) . For πi;j the cyclic shift πi is applied to the vector

; : : : ;

###### (x0 xn−1) and then the cyclic shift πj is applied to each vector
 xm (0 ≤ m ≤ n − 1) . Obviously this group is transitive of degree n k . The permutation πi;j is computed if we set yi = 2[j] and ym = 0 for m ̸= i . Then zl ≡ xl −i yi mod M, if l ≥ i, and zl ≡ xn+l −i yi mod M,

<
###### if l i . In the same way as in the proof for MUL, it follows that zl is equal to xl −i or xn+l −i shifted by j positions. Furthermore the x-vectors have been shifted by i positions.

 MVP and 3-MATMUL : These examples are left as exercises. 2

 THEOREM 2.4 : If f is transitive of degree n, then A T[2] = Ω(n[2]) for each VLSI-circuit computing f .

 Proof : It is sufficient to prove A = Ω(D[2]) . Since T P = n D[−][1], it ≥ follows then that

:
###### A T[2] = Ω(D[2](n D[−][1])[2]) = Ω(n[2]) (2.5)

 The claim is trivial if D = O(1) . Otherwise let h be the number of levels, l λ the length and w λ the width of a VLSI-circuit for f . W.l.o.g. w l . By a longitudinal cut we partition the chip into a right part ≥ R and a left part L . If this cut is shifted one cell, then the number of output ports in each part is increased or decreased by a constant summand. At most P outputs may leave the same output port. Since P = n D[−][1] and D = ω(1), P = o(n) . Hence it is possible to cut the circuit in such a way that for Rout and Lout, the number of outputs leaving the circuit in the right part and left part resp.,

:
###### Lout Rout = Ω(n) (2.6) ≥
 Since the cut is longitudinal, we have cut c = O(l ) wires. Since

;
###### A = l w l [2] = Ω(c[2]) (2.7) ≥
 it is sufficient to prove c = Ω(D).

 Let G be the transitive group computed by f and let π G . If ∈ the control variables are fixed in such a way that we compute π, then


-----

**352**

###### xi has to cross the cut if the input port for xi is in another part of the circuit than the output port for the π[−][1](i)-th output. In this case

; ;
###### k(i π) := 1, otherwise k(i π) := 0 .
 Let Gij be the set of all π ∈ G where π(i) = j . It follows from elementary group theory (see e.g. Huppert (67)) that all Gij are of the same size. Hence π[−][1](j) = i for G n[−][1] permutations π G . It | | ∈ follows that � k(i; π) = |G| n[−][1] Lout ; (2.8)

_π_ G
_∈_

###### if the input port for xi lies in R, and � k(i; π) = |G| n[−][1] Rout ; (2.9)

_π_ G
_∈_


###### if the input port for xi lies in L . Therefore � � k(i; π) ≥ n |G| n[−][1] min{Lout ; Rout} = |G| Rout

_π∈G1≤i≤n_


:
###### (2.10)


###### In particular, there is some π G such that for the computation of π ∈ at least Rout inputs have to cross the cut. Since only c wires connect

<
###### the two parts of the circuit, P cannot be very small. If P Rout c[−][1], the data queue at the cut would be increasing. Hence, by (2.6),
 n D[−][1] = P ≥ Rout c[−][1] = Ω(n c[−][1]) (2.11)

 and c = Ω(D). 2

 12.3 Probabilistic circuits

 In Ch. 9, 6, we have simulated probabilistic Turing machines effi- § ciently by circuits. This approach leads e.g. to polynomial circuits for primality testing. Here we go the same way for probabilistic circuits.

 DEFINITION 3.1 : The inputs of a probabilistic circuit S are

; : : : ;

###### the inputs x1 xn of a Boolean function and some further inputs


-----

**353**

; : : : ;

###### y1 ym which take the values 0 and 1 independently with probabil
=
###### ity 1 2 . According to this probability distribution the output S(x) of S on input x is a random variable.

; ; <
###### DEFINITION 3.2 : Let A B 0 1 and 0 q p 1 . The ⊆{ }[n] ≤ ≤

;
###### probabilistic circuit S separates A and B with respect to (p q) if

 x A : Pr(S(x)) = 1) p and (3.1) ∀ ∈ ≥

:
###### x B : Pr(S(x)) = 1) q (3.2) ∀ ∈ ≤

; ; ; ;
###### Notation: (S A B p q) .

; ; ; = ; =
###### S is an ε-computation of f, if (S f[−][1](1) f[−][1](0) (1 2)+ ε 1 2) is satis- fied.

 The following considerations can be generalized to circuits with binary gates or formulas. But we concentrate our view upon bounded- depth circuits with gates of unbounded fan-in (see Ch. 11). We shall prove Theorem 2.2, Ch. 11, by designing probabilistic circuits for threshold functions.

 At first, we present simple transformations and show how prob- abilistic circuits of very small error probability lead to determinis- tic circuits. Afterwards we investigate how we can reduce the error probability. On the one hand, we improve log[−][r] n-computations to log[−][r+1] n-computations, if r 2, and on the other hand, we improve ≥ log[−][1] n-computations to computations of very small error probability. All results are due to Ajtai and Ben-Or (84).

; ; ; ; ; ;
###### LEMMA 3.1 : Let (S A B p q) be satisfied for A B 0 1 and ⊆{ }[n]

<
###### 0 q p 1 . ≤ ≤

    - ; ; ; ;

###### i) If p p[′] q[′] q, (S A B p[′] q[′]) is satisfied. ≥ ≥
 ii) There is a probabilistic circuit S[′] such that C(S[′]) = C(S), D(S[′]) =

; ; ; ;

###### D(S) and (S[′] B A 1 q 1 p) are satisfied.
 − −
 iii) For each positive integer l there is a probabilistic circuit Sl such

; ; ; ;

###### that C(Sl ) ≤ l C(S)+1, D(Sl ) ≤ D(S)+1 and (Sl A B p[l] q[l] ) are


-----

**354**


###### satisfied.

<   ###### iv) If q 2[−][n] and p 1 − 2[−][n], there is a deterministic circuit Sd

; ; ; ;

###### such that C(Sd) ≤ C(S), D(Sd) ≤ D(S) and (Sd A B 1 0) are
 satisfied.

 Proof : i) Obvious by definition.

 ii) We negate the output of S and apply the deMorgan rules bottom- up.

 iii) We use l copies of S with independent random inputs and combine the outputs by an ∧-gate. Sl (x) = 1 iff all copies of S compute 1 . The assertion follows since the copies of S have independent random inputs.

<
###### iv) Since q p, A and B are disjoint. Let f be defined by f[−][1](1) = A . For x A B, the error probability, i.e. the probability that ∈ ∪ S(x) = f(x), is smaller than 2[−][n] . Let I(x) be the random variable ̸ where I(x) = 1 iff S(x) = f(x) and I(x) = 0 otherwise. Then E(I(x)) = ̸ Pr(S(x) = f(x)) . Hence ̸


###### �� � � < : E I(x) = E(I(x)) 1 (3.3)

x A B x A B
_∈_ _∪_ _∈_ _∪_

; : : : ;

###### For fixed y1 ym, I, the sum of all I(x), is the number of errors
 on the inputs x A B . I is always a nonnegative integer. By (3.3) ∈ ∪

< ; : : : ;
###### E(I) 1 . Therefore there is a vector (y1[∗] ym[∗] [)][ ∈{][0][;][ 1][}][m][ which]
 leads to zero error. Sd is constructed by replacing the random inputs

; : : : ; ; : : : ;

###### y1 ym by the constants y1[∗] ym[∗] [.] 2


; : : : ;

###### No efficient algorithm for the computation of y1[∗] ym[∗] [is known.]
 In general, the methods of this section lead only to non uniform cir- cuits even if the given probabilistic circuits are uniform. The step in Lemma 3.1 iv is the only non uniform step.

; ; ; = ; =
###### LEMMA 3.2 : If (S A B (1 + log[−][r] n) 2 1 2) is satisfied for some r 2, then there is a probabilistic circuit S[′] such that C(S[′]) = ≥


-----

**355**

; ; ; = ; =

###### O(n[2](log n)C(S)), D(S[′]) D(S)+2 and (S[′] A B (1+log[−][r+1] n) 2 1 2) ≤
 are satisfied.

 Proof : W.l.o.g. n = 2[k] . Then


; ; ; = ; =
###### (S A B (1 + log[−][r] n) 2 1 2) L. 3.1 i & iii → l = 2 logn

; ; ; ;

###### (S1 A B n[−][2](1 + 2 log[−][r+1] n) n[−][2]) → L. 3.1 ii

; ; ; ;

###### (S2 B A 1 − n[−][2] 1 − n[−][2](1 + 2 log[−][r+1] n)) → L. 3.1 i & iii
 � � l = (n[2] 1) ln 2 −

; ; ; = ; =

###### (S3 B A 1 2 (1 − log[−][r+1] n) 2) → L. 3.1 ii

; ; ; = ; = :

###### (S4 A B (1 + log[−][r+1] n) 2 1 2)

 Let S[′] = S4 . The assertions on C(S[′]) and D(S[′]) follow directly from Lemma 3.1. The only crucial part is the computation of p[l] and q[l] if we apply L. 3.1 iii. This is easy for the first application of L. 3.1 iii, since

=
###### (1 2)[l] = n[−][2] and (3.5)


###### (1 + log[−][r] n)[2 log n]


- :
###### 1 + (2 log n) (log[−][r] n) = 1 + 2 log[−][r+1] n (3.6)


###### For the second application we assume that n is large. For small n we use the DNF for f defined by f[−][1](1) = B . We set exp x = e[x] and { } apply the well-known estimations


###### � �n−1 −x 1 + x e[x] and 1 e ≤ − [x] ≥
 n


:
###### (3.7)


###### � � < Now l = (n[2] 1) ln2 (n[2] 1) ln 2 and n[2] ln 2 l 3 ln 2 . Hence − ≤ − −

=
###### (1 n[−][2])[l] (1 n[−][2])[(n][2][−][1) ln 2] e[−] [ln 2] = 1 2 (3.8) − ≥ − ≥

 for the first term. For the second term
 � �l 1 n[−][2](1 + 2 log[−][r+1] n) (3.9) −

<
###### exp n[−][2] (n[2] 3) (ln 2) (1 + 2 log[−][r+1] n) {− − }

= � �:
###### = (1 2)[n][−][2][(n][2][−][3)] exp n[−][2] (n[2] 3) (ln 2) 2 log[−][r+1] n − −


-----

**356**

###### We estimate the first factor by

= = = �
###### (1 2)[n][−][2][(n][2][−][3)] = (1 2) 8[n][−][2] = (1 2) exp (ln 8)n[−][2][�] (3.10)

= :
###### = (1 2) (1 + O(n[−][2]))

            - :
###### For the second factor 2 n[−][2] (n[2] 3) (ln 2) 1 3 for large n . If x 0 − ≥


###### � exp x = {− }

0 i<
_≤_ _∞_


###### ( x)[i] − � : : : �
 1 x 1 ≤ − − [x] i! 2 4! 6!

 [−] [x][3] [−] [x][5] [−]


:
###### (3.11)


###### Hence for large n

 � � exp n[−][2](n[2] 3) (ln2) 2 log[−][r+1] n − −


< : :
###### 1 1 2 log[−][r+1] n (3.12) −


###### By (3.9), (3.10) and (3.12) � �l < = : 1 n[−][2](1 + 2 log[−][r+1] n) (1 2) (1 + O(n[−][2])) (1 1 2 log[−][r+1] n) − −
 (3.13)

< =
###### (1 2) (1 log[−][r+1] n) for large n . −

 2


; ; ; = ; =
###### LEMMA 3.3 : If (S A B (1 + log[−][1] n) 2 1 2) is satisfied, then there is a deterministic circuit S[′] such that C(S[′]) = O(n[6](log[2] n)C(S)),

; ; ; ;

###### D(S[′]) D(S) + 4 and (S[′] A B 1 0) are satisfied. ≤

 Proof : We leave the details to the reader and present only a sketch of the proof.

; ; ; = ; =
###### (S A B (1 + log[−][1] n) 2 1 2) L. 3.1 i & iii l = 2 log n (3.14) →

; ; ; ;

###### (S1 A B 2 n[−][2] n[−][2]) → L. 3.1 ii

; ; ; ;

###### (S2 B A 1 − n[−][2] 1 − 2 n[−][2]) → L. 3.1 i & iii l = 2 n[2] ln n

; ; ; ;

###### (S3 B A n[−][2] n[−][4]) → L. 3.1 ii

; ; ; ;

###### (S4 A B 1 − n[−][4] 1 − n[−][2]) → L. 3.1 i & iii l = n[3]

; ; ; ;

###### (S5 A B 1 − 2 n[−][1] e[−][n]) → L. 3.1 ii

; ; ; ;

###### (S6 B A 1 − e[−][n] 2 n[−][1]) → L. 3.1 i & iii l = n

; ; ; ;

###### (S7 B A 1 − 2ne[−][n] (2 n[−][1])[n]) → L. 3.1 ii

; ; ; ;

###### (S8 A B 1 − (2 n[−][1])[n] 2ne[−][n]) → L. 3.1 iv

; ; ; ;

###### (S[′] A B 1 0)
 2


-----

**357**

###### We combine Lemma 3.2 with Lemma 3.3.

              ###### THEOREM 3.1 : If Sn is for some r 0 a sequence of log[−][r] n-computations of fn ∈ Bn, if C(Sn) is bounded by a polynomial and if D(Sn) is bounded by a constant, then

;
###### f = (fn) ∈ SIZE - DEPTH(poly const) .

 We are now ready to prove Theorem 2.2, Ch. 11.

 THEOREM 3.2 : If k(n) = O(log[r] n) for some fixed r, then

;
###### f = (T[n] const) .
k(n)[)][ ∈] [SIZE - DEPTH(poly]


###### Proof : W.l.o.g. k = k(n) log[r] n and n = 2[l] . We design a proba- ≤

= =
###### bilistic circuit S of size n n k + 1 and depth 2 . We use n k blocks ⌈ ⌉ ⌈ ⌉ of random inputs, the block size is l = log n . There exist n minterms

; : : : ;

###### m[j]1 m[j]n [on the][ j] [-th block of random inputs. We compute x][i][ ∧] [m]i[j]

=
###### for all 1 ≤ i ≤ n and 1 ≤ j ≤⌈n k⌉ . The disjunction of all xi ∧ m[j]i for fixed j is a random xr (according to the uniform distribution). We compute the disjunction of all xi∧m[j]i [, the disjunction of][ ⌈][n][=][k][⌉] [random] x-inputs.

 Let pk(s) be the probability that S(x) = 1 if the input contains s ones. Since 1 − n[s] [is the probability that a random x-input equals 0,]
 we conclude


###### � �⌈n=k⌉ −s=k pk(s) = 1 − 1 − [s] ≈ 1 − e
 n


:
###### (3.15)


###### Obviously s → pk(s) is increasing. Thus the circuit S satisfies

;
###### (S (T[n]k[)][−][1][(1), (T][n]k[)][−][1][(0), p][k][(k)][;][ p][k][(k][ −] [1)) . For small k or n we use] the DNF for T[n]k [. Otherwise it is easy to prove that]

: : :
###### pk(k) ≥ pk(k − 1)(1 + k[−][2]) and 0 5 ≤ pk(k − 1) ≤ 0 9 (3.16)

:
###### If pk(k − 1) = 0 5, we could apply directly Theorem 3.1, since k[−][2] ≥

               - :
###### log[−][2r] n . One possible way to deal with pk(k − 1) 0 5 is described in Exercise 13. 2


-----

**358**

###### We have seen that log[−][r] n-computations can be simulated efficiently by deterministic computations. What about n[−][ε]-computations for

   ###### some ε 0? If they had been simulated efficiently, we would ob- tain by the construction in Theorem 3.2 and Theorem 3.1 circuits of polynomial size and constant depth for T[n]
k(n) [and k(n) = n][ε][ . This]
###### would be a contradiction to Corollary 4.1, Ch. 11. Hence the simula- tion of Ajtai and Ben-Or is optimal if we allow a polynomial increase of the circuit size and a constant number of additional logical levels.

 Although the majority function is not in

;
###### SIZE - DEPTH(poly const), it can be proved by the above methods that some approximation of the majority function is contained in this class (Stockmeyer (83), Ajtai and Ben-Or (84)).

 THEOREM 3.3 : There is for constant r a sequence of circuits Sn of polynomial size and constant depth which compute functions fn ∈ Bn such that

=
###### fn(x) = 1 if x1 + · · · + xn ≥ (n 2) (1 + log[−][r] n) and (3.17)


###### fn(x) = 0 if x1 + · · · + xn


< = :
###### n 2 (3.18)


###### We have pointed out that the last step in our simulation of probabilistic circuits by deterministic circuits, the application of Lemma 3.1 iv, is non uniform. Hence it is possible that functions fn Bn can be computed by uniform probabilistic circuits of poly- ∈ nomial size and small error probability, but cannot be computed by uniform deterministic circuits of polynomial size. This leads to the definition of the complexity classes RNC and RNCk (Cook (83), for the definition of NC and NCk see Def. 8.2, Ch. 9). Here we consider circuits with binary gates.


-----

**359**

###### DEFINITION 3.3 : RNC (RNCk) is the class of languages L such that for fn defined by fn[−][1][(1) = L][∩{][0][;][ 1][}][n][ there are U][BC][-uniform proba-] bilistic circuits of polynomial size and polylog depth (depth O(log[k] n)) satisfying

;
###### Pr(Sn(x) = fn(x) | x ∈ fn[−][1][(a))][ ≥] [3][=][4] for a ∈{0 1} . (3.19)

 We are content with this definition and the remark that many RNCk algorithms are known.

 EXERCISES

 1. Prove the upper bound in Theorem 1.2.

 2. Each synchronous circuit for the addition of an n-bit number and a 1-bit number has size Ω(n log n) .

 3. Estimate Cs(f) for all f ∈ Bn by synchronizing Lupanov’s circuit (Ch. 4, 2). §

 4. Each synchronous circuit for the computation of the pseudo com- plements of a k-slice (Ch. 6, 13) contains at least log(n 1) § ⌈ − ⌉ � �n� � log( + 2) gates.
k

###### 5. The complete graph Km is planar iff m ≤ 4 .

 6. The complete bipartite graph K3;3 is not planar.

 7. (McColl (81)). The following functions are not computable in monotone, planar circuits.

; ;
###### a) f1(x y) = (y x) .


-----

**360**

; ;
###### b) f2(x y) = (xy x) .

; ;
###### c) f3(x y) = (xy x ∨ y) .

< <
###### 8. (McColl (85 a)). T[5]3 [(and also T]k[n] [for 2] k n − 1) is not computable in a monotone, planar circuit.

 9. (McColl (85 a)). T[n]2 [is computable in monotone, planar circuits.]

 10. Complete the proof of Lemma 2.2 for MVP and 3-MATMUL .

 11. Prove results similar to Lemma 3.1 – 3.3 and Theorem 3.1 for probabilistic circuits with binary gates.


< ; ; ; ;

###### 12. Let 0 ≤ qi pi ≤ 1 and let (Si A B pi qi) be satisfied for 1 ≤ i ≤
 m . In S[∨] and S[∧] we combine the outputs of all Si by an ∨-gate and

; ; ; ; ; ; ;

###### -gate resp. Compute p q p q such that (S[∨] A B p q ) ∧ ∨ ∨ ∧ ∧ ∨ ∨

; ; ; ;

###### and (S[∧] A B p q ) are satisfied.

_∧_ _∧_

; ; ; ; ; : : : ;
###### 13. Let (S A B p q) be satisfied and r 0 2[k] 1 . Then there ∈{ − } is a circuit S[′] such that C(S[′]) C(S)+O(2[k]), D(S[′]) D(S)+O(1) ≤ ≤

; ; ; ;

###### and (S[′] A B (r + p) 2[−][k] (r + q) 2[−][k]) are satisfied.


###### 14. Compare the construction of bounded-depth circuits for the threshold functions with the construction of monotone formulas for the majority function in Ch. 8, 3. §


-----

**361**

###### 13. PRAMs AND WRAMs: PARALLEL RANDOM ACCESS MA- CHINES

 13.1 Introduction

 Circuits represent a hardware model of parallel computations but not a model of parallel computers. A parallel computer consists of many computers (so-called processors) which work together. Since several years vector computers are used, these are based on the SIMD concept (single-instruction-multiple-data-stream). At each single time step one can apply a definite type of operation (e.g. addition) to vec- tors and not only to numbers. This concept is appropriate for numer- ical applications (simulations in physics and geological explorations, meteorological computations for an improved weather-forecast, etc.), but for several combinatorial algorithms it is too restrictive.

 Nowadays, one is designing MIMD computers (multiple-instruct- ion-multiple-data-stream) that consist of up to 1024 processors. Each processor has its own program. The processors may work together by communicating with each other. If each pair of processors was con- �1024� nected by a communication channel, we would have = 523 776
2
###### connections. Hence this approach is impractical. The communica- tion graph (vertices are processors, edges are communication channels) should be a graph of small degree. There are communication graphs like for instance the cube-connected-cycle and the shuffle-exchange- network which have constant degree (for an arbitrary number of pro- cessors) and which allow fast communication between arbitrary pro- cessors.

 It is difficult to design algorithms for these realistic parallel com- puters, since one always has to pay attention to the ˝distance˝ of processors which like to communicate. Hence one considers parallel computers of a simpler communication structure. Processors are not connected via communication channels, instead of that all processors


-----

**362**

###### have random access to a shared memory. Processor j obtains informa- tion from processor i by reading an information written by processor i . These parallel random access machines represent no realistic model, but on the one hand it is convenient to design algorithms in this model, and, on the other hand, efficient algorithms are known for the simula- tion of these algorithms on those realistic parallel computers discussed above (see e.g. Mehlhorn and Vishkin (84) or Alt, Hagerup, Mehlhorn and Preparata (86)). Hence we investigate only parallel random ac- cess machines, nowadays the standard model of parallel computers at least for the purposes of the complexity theory.

 DEFINITION 1.1 : A parallel random access machine (PRAM) for n Boolean inputs consists of processors Pi (1 ≤ i ≤ p(n)), a read-only

; : : : ; ; : : : ;

###### input tape of n cells M1 Mn containing the inputs x1 xn and

<
###### a shared memory of cells Mj (n j ≤ n + c(n)), all containing at

;
###### first zeros. Pi starts in the state q(i 0) . At time step t, depending

;
###### on its state q(i t), Pi reads the contents of some cell Mj of the shared

;
###### memory, then, depending on q(i t) and the contents of Mj, it assumes

; ;
###### a new state q(i t+1), and, depending on q(i t+1), it writes some in- formation into some cell of the shared memory. The PRAM computes fn Bn in time T(n) if the cell Mn+1 of the shared memory contains ∈

; : : : ;

###### on input x = (x1 xn) at time step T(n) the output fn(x) .


###### We distinguish between some models of PRAMs with different rules for solving read and write conflicts.

 – An EREW PRAM (exclusive read, exclusive write) works correctly only if at any time step and for any cell at most one processor reads the contents of this cell and at most one processor writes into this cell.

 – A CREW PRAM (concurrent read, exclusive write) or shortly PRAM allows that many processors read the contents of the same cell at the same time step, but it works correctly only if at any time step and for any cell at most one processor writes into this cell.


-----

**363**

###### – A CRCW PRAM (concurrent read, concurrent write) or shortly WRAM solves write conflicts. If more than one processor tries to write at time step t into cell Mj, then the processor with the smallest number wins. This processor writes its information into Mj, all other competitors fail to write.

 – A WRAM satisfies the common write rule (CO WRAM) if when- ever several processors are trying to write into a single cell at the same time step, the values that they try to write are the same.

 Our PRAM models are non uniform. Nevertheless, we shall de- sign uniform algorithms. For efficient algorithms the computation time T(n), the number of processors p(n) and the communication width c(n) should be simultaneously small. Moreover, the computa- tion power of the single processors should be restricted realistically. For lower bounds we choose the model as general as possible.

 In 2 we compare the different models and obtain efficient algo- § rithms via simulations. All functions with efficient circuits of bounded- depth can be computed efficiently by CO WRAMs. The reverse holds for WRAMs of restricted computation power. This result, which is proved in 3, enables us to generalize lower bounds proved in the § previous chapters. In 4 – 6 we discuss lower bound methods. The § § lower bounds depend on combinatorial measures which we investigate in 7. §

 13.2 Upper bounds by simulations

 THEOREM 2.1 : i) Each function fn Bn can be computed in ∈ time log n + 1 by an EREW PRAM with n powerful processors and ⌈ ⌉ communication width n .


-----

**364**

###### ii) Each fn ∈ Bn can be computed in time ⌈log n⌉ + 2 by a PRAM with n 2[n] realistic processors and communication width n 2[n] .

 iii) Each fn Bn can be computed in time 2 by a CO WRAM with ∈ n 2[n] realistic processors and communication width 2[n] .

 Proof : i) At time step 0 processor Pi reads the i -th input xi, stores this value in its internal memory and writes it into Yi, i.e. the i -th cell Mn+i of the shared memory. At time step t, processor Pi reads

             ###### the contents of Yj where j = i + 2[t][−][1] . If j n, Pi does nothing. If j ≤ n, Pi concatenates the contents of its internal memory and the contents of Yj . The result is stored in its internal memory and written into Yi . It is easy to prove that Pi knows after time step t the vector

; : : : ; ;

###### (xi xj) where j = min{n i + 2[t] − 1} . After time step ⌈log n⌉, P1

; : : : ; ; : : : ;

###### knows (x1 xn) . P1 evaluates f(x1 xn) and writes the result
 into the output cell Y1 .

 ii) We use the DNF of f . Each minterm can be evaluated in time log n + 1 by n realistic processors and communication width n . A ⌈ ⌉ minterm is a conjunction of n literals x[a(k)]k . We use a binary tree as in the proof of i), but the conjunction is a simple function. Instead

; : : : ;

###### of (xi xj) we only store x[a(i)]i ∧· · · ∧ x[a(j)]j . All minterms can be
 evaluated in parallel by a PRAM. Before the last step there is for each a ∈ fn[−][1][(1) a processor P(a) knowing m][a][(x). W.l.o.g. Y][1][ contains 0 .] P(a) writes 1 into Y1 iff ma(x) = 1 . There is no write conflict, since at most one minterm computes 1 .


###### iii) The disjunction of n literals can be computed by a CO WRAM consisting of n realistic processors in one time step and communication width 1 . Each processor reads one input and writes 1 into the output cell iff its literal equals 1 . We use the CNF of f and evaluate all maxterms in parallel. Moreover we write 1 into Y1 . In the second step a processor P(a) for a ∈ f[−][1](0) reads sa(x) and writes 0 into Y1 iff sa(x) = 0 . 2


-----

**365**

###### These simple algorithms are not efficient algorithms, since either the number of processors grows exponentially or the processors are too powerful. We have seen that it is possible to simulate the DNF or CNF for f . This idea can be extended to circuits (van Leeuwen (83), Stockmeyer and Vishkin (84)).

 THEOREM 2.2 : i) Let S be a circuit of binary gates computing fn Bn with s gates in depth d . Then there is a PRAM com- ∈

=
###### puting fn in time O(d) with p = ⌈s d⌉ realistic processors and communication width s .
 ii) Let S be a circuit of unbounded fan-in gates computing fn ∈ Bn with s gates and e edges in depth d . Then there is a CO WRAM computing fn in time d+1 with e realistic processors and commu- nication width s .

 Proof : i) The depth of a gate is the length of a longest path from an input to this gate. Let Ni be the number of gates of depth i in S .

=

###### These gates are partitioned to p blocks of at most ⌈Ni p⌉ gates each.
 We simulate the circuit level by level. A processor may simulate a binary gate in two steps of time. Hence the i -th level is simulated in

=

###### 2 ⌈Ni p⌉ steps by p processors. The result of each gate is written into
 a definite cell of the shared memory. The time for this simulation is estimated by
 � 2 ⌈Ni =p⌉≤ 2 d + 2 (N1 + · · · + Nd)=p (2.1)

1 i d
_≤_ _≤_

= :
###### 2 d + 2 s (d s) = 4 d ≤

 ii) There is for each gate of the circuit a cell in the shared memory and for each edge of the circuit a processor. In time step 0 the contents of the cells representing -gates are replaced by ones. In time step i ∧ (1 i d) all gates on the i -th level are simulated. The processors ≤ ≤ for the edges leading to these gates read the inputs of the edges. If the level is an -level a processor writes 0 into the corresponding cell for ∧


-----

**366**

###### the gate iff the processor has read 0 . -gates are simulated similarly. ∨ 2

 This theorem leads to efficient PRAM algorithms. We obtain for many fundamental functions O(log n)-time algorithms on PRAMs with a polynomial number of realistic processors and polynomial com- munication width (see Ch. 3). By the results of Ch. 10, 3, and Ch. 11 § we obtain for certain fundamental problems O(1)-time algorithms on CO WRAMs with a polynomial number of realistic processors and polynomial communication width. In 4 we prove Ω(log n)-bounds § on the PRAM complexity of many fundamental functions even if the number of processors, the power of processors and the communication width are unlimited. These results imply that realistic CO WRAMs may be faster by a factor of Θ(log n) than PRAMs of unlimited re- sources. This speed up is optimal because of the following results.

 THEOREM 2.3 : A WRAM of p processors, communication width c and time complexity t may be simulated by an EREW PRAM with (c + n) p processors, communication width c + (c + n)p and time com- plexity t (4 + 2 log p ) . ⌈ ⌉

 Proof : The simulation is step-by-step. The c cells of the shared memory are simulated directly by c cells. Furthermore each of the n input cells and the c cells of the shared memory is simulated once for each processor. We assume that we have simulated i computation steps. Then the information of each of the c + n cells of the WRAM is copied and written into p definite cells. This can be done for each cell by p processors in time log p + 1 without read conflicts. If the ⌈ ⌉ information is copied r times, r processors may read the information and may write it into r other cells and so on. Afterwards we simulate one computation step. Each processor can read the information in its own cells, i.e. without read conflict. Each processor simulates the internal computation and marks that of its cells representing the cell in which it tries to write. For each cell of the shared memory p processors


-----

**367**

###### are sufficient to compute in time log p +1 the number of the processor ⌈ ⌉ who wins the write conflict according to the rules. This is simply the computation of the minimum of at most p numbers. Each processor is informed whether it has won the write conflict. Afterwards all winners write their information into the corresponding cells which causes no write conflict. The whole computation step has been simulated in 4 + 2 log p steps. 2 ⌈ ⌉

 WRAMs can be simulated rather efficiently by simple EREW PRAMs. What is the difference between WRAMs and CO WRAMs ? This question has been answered by Kucera (82).

 THEOREM 2.4 : A WRAM of p processors, communication width c �p� and time complexity t may be simulated by a CO WRAM of
2

###### processors, communication width c + p and time complexity 4 t .

 Proof : The simulation is step-by-step. We use processors Pj

<
###### (1 ≤ j ≤ p) for the simulation and Pij (1 ≤ i j ≤ p) for some extra �p� work. Since Pj and Pij never work simultaneously 2 processors are sufficient if p 3 . The case p = 2 is obvious. Each computation step ≥ is simulated in 4 steps. At first the processors Pj (1 ≤ j ≤ n) simulate the reading and the internal computations of the WRAM, and Pj writes into the j -th extra cell of the shared memory the number of that cell into which Pj likes to write. In the following two steps Pij decides whether Pj loses a write conflict against Pi . Pij writes a mark # into the j -th extra cell iff Pj has lost a write conflict against Pi . This causes no conflict for CO WRAMs. All processors writing at this time step write the same letter, namely the mark # . In the fourth step Pj reads whether it has lost a write conflict. Only if Pj has not lost a write conflict, Pj simulates the write phase of the WRAM. This causes no write conflict at all. 2


-----

**368**

###### All these simulations lead to upper bounds on the time complexity of parallel computers. For several fundamental functions we obtain (nearly) optimal algorithms. For many other functions new ideas for the design of efficient parallel algorithms are needed. Because we did not present efficient algorithms for non fundamental functions, we shall not discuss efficient parallel algorithms for such functions.

 13.3 Lower bounds by simulations

 Stockmeyer and Vishkin (84) have proved that restricted WRAMs may be simulated efficiently by circuits of unbounded fan-in gates. We restrict the computation power of the single processors in such a way that each single step may be simulated by a polynomial circuit of constant depth. This is the only restriction we actually need.

 Each processor p follows some program of l (p) lines. Its current

; : : : ;
###### state l 1 l (p) describes the actual line of the program. The ∈{ } initial state is l = 1 . The processor has a local random access memory. We give a list of legitimate operations.

 – M(r) = c (reading of constants). The constant c is written into the r -th cell of the local memory.

 – M(r) = M(i) (direct reading). The contents of the i -th cell of the local memory is written into the r -th cell of the local memory.

 – M(r) = M(i) M(j) (computation step). Let x and y be the contents ◦ of the i -th and j -th cell of the local memory resp. Then z = x y is ◦ written into the r -th cell of the local memory. The function is one ◦ of a finite list of operations. We allow only operations which can be computed by polynomial circuits of constant depth and where the

; ;
###### length z of the output z is bounded by max x + 1 y + 1 n . By | | {| | | | } the results of Ch. 11, 2, the list may include addition, subtraction, § comparison and also the multiplication of numbers of length O(log n) .


-----

**369**

=
###### – M(r) = M(i) l c (indirect reading). Let I be the contents of ∗ { } the i -th cell of the local memory. The contents of the I -th cell of the local/common (or shared) memory is written into the r -th cell of the local memory.

=
###### – M(r) = M(i) l c (indirect writing). The contents of the i -th cell ∗ { } of the local memory is written into the j -th cell of the local/common memory, j is the contents of the r -th cell of the local memory.

<=
###### – GO TO l if M(i) = M(j) (if-tests). It is tested whether the con- tents of the i -th cell of the local memory is smaller than / equal to the contents of the j -th cell of the local memory. In the positive case we proceed to line l of the program. Otherwise we proceed (as usual) to the next line of the program.

 – STOP (end of the program).

 The so-restricted WRAMs are called RES WRAMs. The program size is the number of bits in the program.

 THEOREM 3.1 : Let fn Bm where m = n[2] . Let Wn be a sequence ∈ of RES WRAMs computing fn, if the input is given in n blocks of n bits each, with p(n) processors of program size s(n), unlimited com- munication width and time complexity t(n) . Then for some polynomial Q, there are circuits Sn computing fn with

; ; ;
###### Q(n p(n) s(n) t(n)) unbounded fan-in gates in depth O(t(n)) .

 Proof : Although the communication width is unlimited, only a lim- ited number of cells is available. The numbers of the input have length n and the length of the numbers in the programs is bounded by s(n) . RES WRAMs cannot produce large numbers in short time. The length of all numbers used by Wn is bounded by

; :
###### L(n) = max n s(n) + t(n) (3.1) { }

 We simulate Wn step-by-step. The difficulty is to find the infor- mation in the memories, since by numbers of length L(n) one may address 2[L(n)] different cells. These are 2[L(n)] possible addresses. For


-----

**370**

###### each definite input each processor may change the contents of at most t(n) cells. Therefore the circuits use an internal representation of the memories of Wn . Everything written at time step k gets the inter- nal address k . If this information is deleted at a later time step, the information is marked as invalid. The index l refers to the local memory and index c to the common memory. For all 1 p p(n), ≤ ≤

; ;
###### 1 ≤ k ≤ t(n), k ≤ t ≤ t(n) we shall define al (p k), vl (p k) and

; ; ;
###### wl (p k t) . al (p k) is a number of length L(n) and indicates the ad- dress of that cell of the local memory into which the p-th processor has written at time step k . vl (p,k) is also a number of length L(n) and equals the number which the p-th processor has written at time step k . The bit wl (p,k,t) indicates whether at time step t the information the p-th processor has written into the local memory at time step k is still

; ; ; ;
###### valid (wl (p k t) = 1) or has been deleted (wl (p k t) = 0) . In the

; ; ; ;
###### same way we define ac(p k), vc(p k) and wc(p k t) . At the begin- ning all local cells contain zeros, only the first n cells of the common

; ;
###### memory contain the input. Hence we define ac(i 0) = i, vc(i 0) = xi

; ;
###### and wc(i 0 0) = 1 for 1 ≤ i ≤ n . Here we assume, like we do in the whole proof, that numbers are padded with zeros if they have not the necessary length. All other parameters are equal to 0 for t = 0 .

 Let l (p) be the number of lines in the program of the p-th proces
; ; ; ;
###### sor. Let i(p l ), j(p l ), c(p l ) and r(p l ) be the parameters in the l -th line of the p-th program. Here and in the following we assume that non existing parameters are replaced by zeros and that the empty dis
; ;
###### junction is zero. Let ic(p l t) = 1 iff during the (t+1)-st computation

; ;
###### step processor p is in line l of its program. Obviously ic(p l 0) = 1 iff l = 1 .

 Let us assume that t computation steps of Wn have been simulated correctly. This is satisfied at the beginning for t = 0 . We describe

;
###### the simulation of the (t+1)-st computation step. Let EQ(a b) = 1 iff a = b, let


; : : : ;
###### a ∧ bm) and (3.2)


###### a ∧ (b1


; : : : ;
###### bm) = (a ∧ b1


-----

; : : : ;
###### bm) = (a1 ∨ b1


**371**

; : : : ;
###### am ∨ bm) (3.3)


###### (a1


; : : : ;
###### am) ∨ (b1


; ;
###### for arbitrary m . We simulate each line of each program. Let R(p l t) be the result produced by the p-th processor during the (t + 1)-st computation step, if the processor is in line l of the program. The result is the information which will be written into some cell or the

; ;
###### result of an if-test. Let A(p l t) be the address of the cell into which

; ; ; ; ;
###### R(p l t) will be written. Let I(p l t) be the contents of the i(p l )-th cell of the local memory before the (t + 1)-st computation step. Then
 I(p; l ; t) = � �EQ(i(p; l ); al(p; k)) ∧ wl (p; k; t) ∧ vl (p; k)�: (3.4)

1 k t
_≤_ _≤_


###### The equality test ensures that we are looking for information at the correct address only, and the validity bit wl ensures that we con- sider only valid information. If we consider a computation step or

; ; ; ;
###### an if-test, we compute J(p l t) in the same way. R(p l t) equals

; ; ; ; ;
###### c(p l ) (reading of constants), or I(p l t) J(p l t) (computation step), ◦

; ; ; ; <= ; ;
###### or I(p l t) (indirect writing), or 1 or 0 if I(p l t) = J(p l t) or

; ; = ; ;
###### I(p l t) = J(p l t) resp. (if-test). For steps of indirect reading ≥ ̸

; ; ; ;
###### R(p l t) equals the contents of the cell I(P l t) of the local or common

; ; ;
###### memory. Hence R(p l t) can be computed by (3.4) if we replace i(p l )

; ; ; ;
###### by I(p l t) . For the common memory we replace al (p k), vl (p k), and

; ; ; ; ; ;
###### wl (p k t) by ac(p[′] k), vc(p[′] k) and wc(p[′] k t) resp. and compute the
 disjunction over all p[′], since each processor may have written into the

; ;
###### common memory. In every case all R(p l t) are computed in poly
; ;
###### nomial size and constant depth. Only for indirect writing, A(p l t)

; ;
###### is not a constant. Then A(p l t) is computed in the same way as

; ;
###### R(p l t) . Finally

; � ; ; ; ;
###### R(p t) = ic(p l t) R(p l t) and (3.5)
 ∧
1 _l_ _l_ (p)
_≤_ _≤_

; � ; ; ; ;
###### A(p t) = ic(p l t) A(p l t) (3.6)
 ∧
1 _l_ _l_ (p)
_≤_ _≤_


###### are the actual results and addresses.

 This information is used for an updating of our parameters. The

; ; ; ;
###### instruction counter ic(p l t + 1) equals 1 iff ic(p l 1 t) = 1 and line −

; ;
###### l 1 does not contain an if-test or ic(p l [′] t) = 1, line l [′] contains an if- −


-----

**372**

; ;
###### test and the result of this test leads us to line l . Hence all ic(p l t+1) are computed in polynomial size and constant depth.

;
###### Let λ(p t) = 1 iff the p-th processor writes into its local memory

;
###### during the (t + 1)-st computation step. Let γ(p t) = 1 iff the p-th processor tries to write into the common memory during the (t+1)-st

; ;
###### computation step. λ(p t) as well as γ(p t) is the disjunction of some

; ; ;
###### ic(p l t) . Now the local memories are updated. Let al (p t + 1) =

; ; ; ; ; ;
###### A(p t), vl (p t + 1) = R(p t) and wl (p t + 1 t + 1) = λ(p t) . For

; ; ; ; ;
###### 1 ≤ k ≤ t, let wl (p k t + 1) = 0 iff wl (p k t) = 0 or λ(p t) = 1

; ;
###### and al (p k) = A(p t) . An information is not valid iff it was not valid before or the p-th processor writes into that cell of its local memory where this information has been stored.

 For the updating of the common memory we have to decide write

;
###### conflicts. Let γ[′](p t) = 1 iff the p-th processor actually writes some information into the common memory at the (t + 1)-st computation step. Then

; ; � ; ; ; ; �;
###### γ[′](p t) = γ(p t) ( γ(q t) EQ(A(q t) A(p t))) (3.7) ∧ ¬ ∧

1 [�]q<p
_≤_


###### since a processor loses a write conflict iff a processor with a smaller

; ;
###### number tries to write into the same cell. Finally ac(p t+1) = A(p t),

; ; ; ; ;
###### vc(p t + 1) = R(p t) and wc(p t + 1 t + 1) = γ[′](p t) . For 1 ≤ k ≤ t,

; ; ; ; ; ;
###### wc(p k t + 1) = 0 iff wc(p k t) = 0 or γ[′](p[′] t) = 1 and ac(p[′] t) =

;

###### A(p[′] t) for some p[′] . One computation step can be simulated in poly nomial size and constant depth.

 At the end of the simulation we compute the output in the same way as we have read the contents of cells. 2

 Combining this simulation and the lower bounds of Ch. 11 we ob- tain lower bounds on the complexity of RES WRAMs.


-----

**373**

###### 13.4 The complexity of PRAMs

 We know (Theorem 2.1) that all Boolean functions f ∈ Bn can be computed by an EREW PRAM in time log n +1 . This upper bound ⌈ ⌉ is proved by doubling the information of each processor in each step. If a (very powerful) processor knows the whole input a, it can compute the output and write it into the output cell. Here we consider lower bounds. If a PRAM stops the computation with output 1, it has to be sure that f(a) = 1 . Let t be a shortest prime implicant covering a, i.e. t(a) = 1 . Let l be the length of t . If we have knowledge on less than l input bits, and if these bits agree with a, we do not know that the output equals 1 .

;
###### DEFINITION 4.1 : Let f ∈ Bn . For a ∈ f[−][1](1) let l (f a) be the length of a shortest prime implicant t PI(f) such that t(a) = 1 . For ∈

;
###### a f[−][1](0) let l (f a) be the length of a shortest prime clause s PC(f) ∈ ∈ such that s(a) = 0 . Let

; ;
###### l max(f) = max{l (f a) | a ∈{0 1}[n]} and (4.1)

; ; :
###### l min(f) = min{l (f a) | a ∈{0 1}[n]} (4.2)

 Obviously l min(f) is the length of a shortest prime implicant or prime clause and (4.2) agrees with Definition 4.1, Ch. 11. Since l max(f) and l min(f) will play an important role in the following sections, we

;
###### interpret l (f a) also in another way. An implicant of length k cor
;
###### responds to an (n k)-dimensional subcube C of 0 1 such that f − { }[n] computes 1 for all a C . A prime implicant t has the additional ∈ property that C cannot be extended, i.e. f is not constant on any cube C[′] where C is a proper subcube of C[′] . This implies the following

;
###### characterization of l (f a) .

;
###### LEMMA 4.1 : l (f a) is the maximum k such that f is not constant

;
###### on any (n k + 1)-dimensional subcube of 0 1 containing a . − { }[n]


-----

**374**

;
###### l (f a) is called sensitive complexity of f at input a (Vishkin and Wigderson (85)). We believe that it is more adequate to interpret this measure using the fundamental notion of prime implicants and prime clauses.

 We also remark that l max(f) may be small even when f has long prime implicants and prime clauses.

 LEMMA 4.2 : Let SAn Bn+k where n = 2[k] be the storage access ∈ function. Then l max(SAn) = l min(SAn) = k + 1 but SAn has a prime implicant and a prime clause of length 2[k] each.

 Proof : The proof is left as an exercise. 2

;
###### By our considerations above we have to know at least l (f a) bits, if the input is a, before we may know the output. One might believe that one can at most double his information in one computation step. This leads to the conjecture that the PRAM time complexity of f is not smaller than ⌈log l max(f)⌉ . For the disjunction ORn of n variables, l max(ORn) = n . The conjecture is false, since ORn can be computed by an EREW PRAM in less than log n steps (Cook, Dwork and ⌈ ⌉ Reischuk (86)).

 √ 2 � = � : THEOREM 4.1 : Let a = (1 + 5) 2 ≈ 2 618 . ORn can be
 computed by an EREW PRAM with n realistic processors and com- munication width n in time ⌈loga n⌉ .

 Proof : It is essential that a processor may transfer information if it does not write. We consider the situation of two memory cells M and M[′] containing the Boolean variables x and y resp. and a processor P knowing the Boolean variable z . P reads the contents of M[′], computes r = y z and writes 1 into M iff r = 1 . Then M contains x y z, ∨ ∨ ∨ the disjunction of 3 variables. If r = 1, this value is written into M . If r = 0, x y z = x . M contains this information, since P does not ∨ ∨ write anything.


-----

**375**

###### This idea can be generalized and parallelized. W.l.o.g. the in- put tape is not read-only, and we have no further memory cells. Let

; ; : : : ;
###### OR(i j) be the disjunction of xi xi+j−1 . Let Pt(i) be the knowl edge of the i -th processor after t computation steps, and let Mt(i) be the contents of the i -th memory cell after t computation steps. Then

; ;
###### P0(i) = OR(i G0) for G0 = 0 and M0(i) = OR(i H0) for H0 = 1 . Let

; ;
###### Pt 1(i) = OR(i Gt 1) and Mt 1(i) = OR(i Ht 1) .
_−_ _−_ _−_ _−_

###### During the t-th computation step the i -th processor reads the con- tents of the (i + Gt 1)-th cell (if i + Gt 1 n) and computes
_−_ _−_ _≤_

###### Pt(i) = Pt 1(i) Mt 1(i + Gt 1) (4.3)
_−_ _∨_ _−_ _−_


; ; ; :
###### = OR(i Gt−1) ∨ OR(i + Gt−1 Ht−1) = OR(i Gt−1 + Ht−1)


                  ###### We have simplified the notation and have assumed that xj = 0 if j n . The i -th processor writes 1 into the (i Ht 1)-th cell (if i Ht 1 1) − − − − ≥ iff Pt(i) = 1 . As in our example at the beginning of the proof

 Mt(i) = Mt 1(i) Pt(i + Ht 1) (4.4)
_−_ _∨_ _−_


; ;
###### = OR(i Ht−1) ∨ OR(i + Ht−1 Gt−1 + Ht−1)

; :
###### = OR(i Gt−1 + 2 Ht−1)


###### Hence Gt = Gt−1 + Ht−1 and Ht = Gt−1 + 2 Ht−1 . We set F2t = Gt and F2t+1 = Ht . Then


; ;
###### F0 = 0 F1 = 1 F2t = F2t−2 + F2t−1


;
###### F2t+1 = F2t−1 + F2t


:
###### (4.5)


###### This is the well-known recursion for the Fibonacci numbers


###### √ � Ft = Φ[t] − (Φ −


###### 5)[t][�]


###### √ √

= = :

###### 5 for Φ = ( 5 + 1) 2 (4.6)


###### Hence Mt(1) is the disjunction of the first F2t+1 variables. We stop the computation if F2t+1 ≥ n . 2

 By this result we have improved the obvious upper bound by a small constant factor. Cook, Dwork and Reischuk (86) have proved that this is nearly optimal. The PRAM complexity of ORn is Θ(log n) .


-----

**376**

###### By Theorem 4.1 this result is not obvious.

 √

= :

###### THEOREM 4.2 : Let b = (5 + 21) 2 4 791 . The PRAM time
 ≈ complexity (number of processors, communication width and compu- tation power of the processors are unlimited) of f ∈ Bn is not smaller than logb n if l max(f) = n .

;
###### Proof : Let a[∗] be an input where l (f a[∗]) = n . Then f is not con
;
###### stant on any 1-dimensional subcube of 0 1 containing a[∗] . Hence { }[n] f(a[∗](i)) ̸= f(a[∗]) for the neighbors a[∗](i) of a[∗], where a[∗](i)j = a[∗]j [for i][ ̸][= j] and a[∗](i)i = 1 − a[∗]i [.]
 We introduce some notation. An index i influences a processor P at time step t on input a if the state of P at t on a differs from the state of P at t on a(i) . In a similar way we define the influence of

; ; ; ;
###### an index on a memory cell. Let K(P t a) and L(M t a) be the set of indices influencing P and M resp. at t on a .

; ; ; ;
###### Obviously K(P 0 a) = ̸◦, L(Mi 0 a) = {i} if i ≤ n and

; ;     
###### L(Mi 0 a) = ̸◦ if i n . Let T be the computation time of a PRAM

; ;

###### computing f and let M1 be the output cell. Then L(M1 T a[∗]) =

; : : : ; ;
###### 1 n, since l (f a[∗]) = n . We shall estimate the information flow. { }

; ;

###### If L(M1 t a[∗]) grows only slowly with t, then T is large.


###### We anticipate the results of our estimations. We prove for


; ;
###### K0 = 0 L0 = 1 Kt+1 = Kt + Lt


;
###### Lt+1 = 3 Kt + 4 Lt


;
###### (4.7)


###### all processors P, memory cells M, inputs a and time steps t that


; ; ; ;
###### |K(P t a)| ≤ Kt and |L(M t a)| ≤ Lt


:
###### (4.8)


###### √ The recursion (4.7) has for b[′] = (5 −


=
###### 21) 2 the solution


###### √

=
###### Kt = (b[t] − b[′][t]) 21 and (4.9)


###### √ Lt = ((3 +

 Hence


###### √ √

=

###### 21)b[t] + ( 21 3)b[′][t]) (2 21) b[t]
 − ≤


:
###### (4.10)


-----

###### n = |L(M1


**377**

; ; :
###### T a[∗])| ≤ LT ≤ b[T] and T ≥ logb n (4.11)


###### We prove (4.8) by induction on t . The assertion is obvious for t = 0 . A processor P may store all available information and may read the contents of one memory cell M . Hence

; ; ; ; ; ;
###### K(P t + 1 a) K(P t a) L(M t a) (4.12) ⊆ ∪

 and by induction hypothesis


; ;
###### |K(P t + 1 a)| ≤ Kt + Lt = Kt+1


:
###### (4.13)


###### A memory cell M is influenced in a complicated way if no processor writes into M . If processor P writes into M at t + 1 on a, then all information in M is deleted and M is influenced only by indices influencing P . Hence

; ; ; ;
###### L(M t + 1 a) K(P t + 1 a) and (4.14) ⊆


; ;
###### |L(M t + 1 a)| ≤ Kt+1 = Kt + Lt ≤ 3 Kt + 4 Lt = Lt+1


:
###### (4.15)


###### If no processor writes into M at t+1 on a, then M may be influenced by those indices which have influenced M before. Furthermore, index i may influence M at t + 1 on a if some processor P writes into M at t + 1 on input a(i) . Hence

; ; ; ; ; ;
###### L(M t + 1 a) L(M t a) Y(M t + 1 a) (4.16) ⊆ ∪

; ;
###### for the set Y(M t+1 a) of indices i such that some processor P writes into M at t + 1 on a(i) but not on a. It is sufficient to prove that


; ;
###### |Y(M t + 1 a)| ≤ 3 Kt+1


:
###### (4.17)


; ;
###### For a bound on the size of Y(M t+1 a) we investigate the situation

; ; ;
###### where 1 2 Y(M t + 1 a) . P[′] and P[′′] write into M at t + 1 on a(1) ∈ and a(2) resp., and P[′] and P[′′] do not write into M at t + 1 on a . This

; ; ; ;

###### is possible only if 1 K(P[′] t+1 a(1)) and 2 K(P[′′] t+1 a(2)) . The ∈ ∈

; ; ; ;

###### assumptions 1 K(P[′′] t + 1 a(2)), 2 K(P[′] t + 1 a(1)) and P[′] = P[′′] ̸∈ ̸∈ ̸
 lead to a write conflict on the input a[′] = a(1)(2) = a(2)(1) . P[′] writes on a(1) into M and is not influenced by index 2 . Hence P[′] writes on a[′]
 into M . The same holds for P[′′] = P[′] in contradiction to the definition ̸


-----

**378**

###### of PRAM programs.

; ;

###### We conclude that P[′] = P[′′] or 1 K(P[′′] t + 1 a(2)) or ∈

; ;

###### 2 K(P[′] t + 1 a(1)). ∈

; ;
###### Now we investigate the general situation in which Y(M t + 1 a) =

; : : : ;

###### {u1 ur} . Let zi be the number of that processor which writes
 into M at t + 1 on a(ui) . We construct a bipartite graph G on the

; : : : ; ; : : : ; ;

###### vertices v1 vr and w1 wr . G contains the edge (vi wj) iff ui
 ∈

; ; ; ;
###### K(P(zj) t + 1 a(uj)) . Since |K(P(zj) t + 1 a(uj))| ≤ Kt+1, the degree of wj is bounded by Kt+1 . Hence


###### e ≤ r Kt+1 (4.18)

 for the number of edges e of G . Our preliminary investigations imply

;

###### that for each pair (ui uj) where P(zi) ̸= P(zj), G contains at least

; ;

###### one of the edges (vi wj) and (vj wi) . We estimate the number of
 these pairs. There are r possibilities for ui . If P(zi) = P(zj), then

; ;
###### uj K(P(zi) t + 1 a) . This is possible for at most Kt+1 indices. ∈ Hence there are at least r − Kt+1 possibilities for uj . We have counted each pair twice. Hence


= :
###### e ≥ r(r − Kt+1) 2 (4.19)

 We combine (4.18) with (4.19) and obtain the following estimation for

; ;
###### r = Y(M t + 1 a) . | |


=
###### r(r − Kt+1) 2 ≤ r Kt+1 and r ≤ 3 Kt+1


:
###### (4.20)

 2


###### The following conjecture is a natural generalization of Theorem 4.2.

 CONJECTURE : T(f) = Ω(log l max(f)) for the PRAM time complex- ity T(f) of Boolean functions f .

 This conjecture is open. Only a (perhaps) weaker lower bound has been proved.

;
###### DEFINITION 4.2 : For a 0 1, let Γ(a) be the neighborhood ∈{ }[n] of a consisting of those n vectors which differ from a at exactly one


-----

**379**

;
###### position. The critical complexity c(f a) of f at a is the number of neighbors b Γ(a) where f(a) = f(b) . The critical complexity c(f) of ∈ ̸ f is defined by

; ; :
###### c(f) = max c(f a) a 0 1 (4.21) { | ∈{ }[n]}

 THEOREM 4.3 : T(f) ≥ logb c(f) for the PRAM time complexity of √

=

###### Boolean functions f and b = (5 + 21) 2 .


;
###### Proof : Let a[∗] be an input where c(f a[∗]) = c(f) . W.l.o.g. f(a[∗]) = ̸ f(a[∗](i)) for 1 i c(f) . Let f[′] be that subfunction of f on c(f) ≤ ≤

                ###### variables where we have replaced the variables xj for j c(f) by a[∗]j [.]

;

###### Obviously l (f[′] a[∗]) = c(f) is equal to the number of variables of f[′] .
 T(f[′]) ≥ logb c(f) by Theorem 4.2, and T(f) ≥ T(f[′]), since f[′] is a subfunction of f . 2

 PROPOSITION 4.1 : c(f) ≤ l max(f) for all f ∈ Bn .

; ; ;
###### Proof : It is sufficient to prove c(f a) l (f a) for all a 0 1 . ≤ ∈{ }[n]

;
###### Let k = c(f a) . Then f(b) = f(a) for k neighbors b of a, and f is not ̸

;
###### constant on any (n k+1)-dimensional subcube of 0 1 containing a . − { }[n] 2

 Because of Proposition 4.1 the conjecture is not weaker than The- orem 4.3. The conjecture is a more natural assertion, since l max is a more natural complexity measure than c . It is open, whether the conjecture is really stronger than Theorem 4.3. What is the largest difference between c(f) and l max ? Does there exist a sequence fn Bn such that c(fn) = o(l max(fn)) or ∈ even log c(fn) = o(log l max(fn)) ? Only in the second case the conjec- ture is stronger than Theorem 4.3.


-----

**380**

###### In 7 we estimate the critical and the sensitive complexity of al- § most all functions and of the easiest functions. It will turn out that the bound of Theorem 4.3 is often tight.

 13.5 The complexity of PRAMs and WRAMs with small communi- cation width

 It is reasonable to restrict the communication width of PRAMs and WRAMs (Vishkin and Wigderson (85)). We begin the discussion with an efficient algorithm.

 THEOREM 5.1 : ORn and PARn can be computed in time � = � � O (n m)[1][=][2] + log m by an EREW PRAM with O (n m)[1][=][2][�] realistic processors and communication width m .

 Proof : We consider only PARn, the algorithm for ORn is similar. At �k� < �k+1� first we consider the case m = 1 . Let n = 1 + + k .
2 _≤_ 2 _· · ·_

###### �k+1� Then k = O(n[1][=][2]) . We compute the parity of variables by k
2
###### processors in time k + 1 . The set of inputs is partitioned to blocks

; : : : ;

###### A1 Ak where |Ai| = i . The i -th processor computes in time i the
 parity of the variables in Ai . During the (i + 1)-st computation step the i -th processor reads the contents of the common memory cell. If

; : : : ;

###### this is the parity of the variables in the blocks A1 Ai−1, the i -th

; : : : ;

###### processor computes the parity of the variables in the blocks A1 Ai
 by a binary parity gate and writes the result into the common memory cell. By induction we conclude that the k -th processor writes the result into the common memory cell during the (k + 1)-st computation step.

   - =
###### If m 1, we partition the variables to m blocks of at most n m ⌈ ⌉ � = variables each. For each block O (n m)[1][=][2][�] processors are sufficient � = to compute the parity in time O (n m)[1][=][2][�] and communication width � 1 . Using O (nm)[1][=][2][�] processors and communication width m, these


-----

**381**

###### computations can be performed in parallel. Afterwards m processors compute in time log m + 1 the parity of the m results and so the ⌈ ⌉ parity of all variables. W.l.o.g. m n, otherwise the result follows ≤ directly. 2

 COROLLARY 5.1 : Each f ∈ Bn can be computed in time � = � � O (n m)[1][=][2] + log m by an EREW PRAM with O (nm)[1][=][2][�] powerful processors and communication width m .

 Proof : We use the approach of the proof of Theorem 5.1 and col- lect during each time step all available information as in the proof of Theorem 2.1 i. 2

 THEOREM 5.2 : If a WRAM computes fn Bn in time T(fn) with ∈

=
###### communication width m, then T(fn) ≥ (l min(fn) m)[1][=][2] .

 The upper and lower bounds of Theorem 5.1 and 5.2 are of the same size if l min(fn) = Θ(n) and m = O(n log[−][2] n) . In particular l min(PARn) = n . In § 7 we prove that l min(fn) = Θ(n) for almost all fn Bn, almost all fn Mn, almost all fn Sn and several fundamental ∈ ∈ ∈ functions. Hence Theorem 5.2 is a powerful result. If l min(fn) is small, the complexity of WRAMs of small communication width cannot be described correctly by l min(fn) . Obviously l min(ORn) = 1 and ORn can be computed in time 1 with communication width 1 . Let


###### gn(x1


; : : : ; :
###### xn) = x1 ∨ (x2 ⊕· · · ⊕ xn) (5.1)


###### Then l min(gn) = 1, but by Theorem 5.2 and the fact that PARn 1
_−_
###### is a subfunction of gn the time complexity of gn is not smaller than

=
###### ((n 1) m)[1][=][2] . −

 Proof of Theorem 5.2 : We add m processors with numbers larger than those of the given processors. The i -th additional processor al- ways reads the contents of the i -th memory cell (not on the read-only


-----

**382**

###### input tape) and tries to write this information again into the same cell. Hence for each memory cell there is always a processor which writes into it.

 Let k = l min(f). A processor which knows less than k inputs, does not know the output. The processors gather their information from reading inputs on the input tape or information in common memory cells. During t computation steps a processor may read directly at most t inputs. For efficient computations the amount of information flowing through the common memory cells needs to be large. We estimate this information flow. We construct (deterministic) restric- tions such that for the so-constructed subfunctions the contents of all memory cells does not depend on the input.

 At the beginning we consider all inputs, namely the cube E0 = {0; 1}[n] . We construct cubes E1;1 ; : : : ; E1;m ; : : : ; ET;1 ; : : : ; ET;m (T =
 T(fn)) such that each cube is a subcube of the one before. Let us construct Et;l and E[′] be the previous cube, namely Et;l −1 if l > 1 or Et−1;m if l = 1 . For a ∈ E[′] let p(a) be the number of the processor that writes into the l -th memory cell Ml at t on a . We choose at;l E[′] ∈
 such that p(at;l ) ≤ p(a) for a ∈ E[′] . Let i1 ; : : : ; ir be the indices of
 those inputs which the p(at;l )-th processor has read during the first t computation steps directly on the input tape. Obviously r t . ≤ Let Et;l be the set of all a ∈ E[′] which agree with at;l at the positions i1 ; : : : ; ir . Et;l is a subcube of E[′] whose dimension is by r smaller than
 the dimension of E[′] . Since r ≤ t, the dimension of ET;m is at least


= :

###### n m t = n m T(T + 1) 2 (5.2) − −
 [�]

1 t T
_≤_ _≤_

###### CLAIM : fn is constant on ET;m .

 By this claim it is easy to prove the theorem. The largest subcube on which fn is constant has dimension n − l min(fn) . Hence


-----

= =
###### l min(fn) ≤ m T(T + 1) 2 and T ≥ (l min(fn) m)[1][=][2]


**383**

:
###### (5.3)


###### Proof of the Claim : The diction, that a processor writes the same in several situations, should also include the case that a processor never writes. We prove that the computation paths for the inputs a ∈ ET;m are essentially the same. The initial configuration does not depend on the input. Then we choose some input a[′] and a processor p[′] that writes on a[′] into the first common cell at t = 1 such that no processor

<
###### p p[′] writes on some a ∈ E0 into M1 at t = 1 . We restrict the input set to those inputs which agree with a[′] at that position which has been read by p[′] . Let a ∈ E1;1 . No processor p < p[′] writes into M1 on a at t = 1 (by construction). Processor p[′] cannot distinguish between a and a[′] . Hence p[′] writes on both inputs the same into M1 and switches to the same state.

 Let us consider Et;l and the previous cube E[′] . We assume that the

; : : : ;
###### contents of all Mi at the time steps 0 t−1 and of Mi (1 ≤ i ≤ l −1) at time step t do not depend on a E[′] . Then we choose some input ∈ a[′] ∈ E[′] and a processor p[′] writing on a[′] into Ml at time step t such that

<
###### no processor p p[′] writes on some a ∈ E[′] into Ml at t . We restrict the input set to those inputs which agree with a[′] at those positions which have been read by p[′] on the input tape. Let a ∈ Et;l . No processor

<
###### p p[′] writes into Ml on a at t (by construction). Processor p[′] does the same on a and a[′], since it has read the same information on the input tape and in the common memory. Hence p[′] writes the same on a and on a[′] into Ml and switches to the same state.
 The contents of the output cell M1 is for all a ∈ ET;m the same. Hence f is constant on ET;m . 2

 THEOREM 5.3 : If a PRAM computes fn Bn in time T(fn) with ∈

=
###### communication width m, then T(fn) ≥ (l max(fn) m)[1][=][3] .


-----

**384**

###### This result improves the bound of Theorem 5.2 only for PRAMs and functions where l max(fn) is much larger than l min(fn) . We present two examples. Obviously l min(ORn) = 1 but l max(ORn) = n . Obviously l min(cl n;3) = 3, and the reader may easily verify that
n 1
###### l max(cl n;3) = � −2 � .

;
###### Proof of Theorem 5.3 : Let e be an input where l (f e) = l max(fn) . Again we construct a sequence of cubes E0 = {0; 1}[n], E1;1 ; : : :,
 E1;m ; : : : ; ET;1 ; : : : ; ET;m for T = T(fn) . Each cube is a subcube of
 its predecessor. Since we only know that e is a difficult input, we en- sure that e ∈ Et;l . E.g. for ORn, e consists of zeros only. If e ̸∈ Et;l, the subfunction of ORn on Et;l is a simple function, namely a constant.
 We discuss the construction of Et;l out of E[′] where E[′] = Et;l −1 or E[′] = Et−1;m or E[′] = E0 .
 Case 1 : There is no input a ∈ E[′] such that a processor writes into Ml on a at time step t . Then Et;l = E[′] .
 Case 2 : The i -th processor writes into Ml on input e at t . Let

; : : : ;

###### i1 ir be the indices of those inputs which the i -th processor has
 read on e during the first t computation steps directly on the input tape. Then r ≤ t . Let Et;l be the set of all a ∈ E[′] which agree with e

; : : : ;

###### at the positions i1 ir .
 Case 3 : No processor writes into Ml on input e at t, but there are some input a ∈ E[′] and some processor p such that p writes into Ml on a at t . Again Et;l is the set of all a[′] ∈ E[′] which agree with e at some

; : : : ;

###### positions i1 ir . Here we choose a minimal set of indices such that
 no processor writes into Ml on some input b ∈ Et;l at t .


###### CLAIM 1 : e ∈ ET;m and f is constant on ET;m .

 Proof : e ∈ Et;l for all t and l by our construction. The second part of the assertion is proved in the same way as the Claim in the proof of Theorem 5.2. 2


-----

**385**

###### CLAIM 2 : For the construction of Et;l we fix at most t(t + 1)=2 additional variables.

 The proof of this claim is postponed. It follows from the claim, that we altogether fix not more than

=

###### m t(t + 1) 2 m T[3] (5.4)
 ≤

 [�]

1 t T
_≤_ _≤_

###### variables. By Claim 1, f is constant on an (n mT[3])-dimensional −

;
###### subcube of 0 1 containing e . Hence { }[n]


; =
###### l max(fn) = l (f e) ≤ m T[3] and T ≥ (l max(fn) m)[1][=][3]

 It is sufficient to prove Claim 2.


:
###### (5.5)


; : : : ;
###### Proof of Claim 2 : We only have to consider Case 3. Let a(1) a(k) be those inputs for which some processor writes into Ml at t . Let i(j) be the number of the processor corresponding to a(j) . Let Et;l be the set of all a E[′] which agree with e at all positions which ∈

; : : : ;
###### have been read for some j 1 k by the i(j)-th processor on ∈{ } input a(j) during the first t computation steps directly on the input tape. Obviously no processor writes into Ml on some input b ∈ Et;l at t . We have fixed at most k t variables. This estimate is too rough.
 For a more profound analysis, we construct Et;l in a few more steps. We always consider one input only. Let Et;l ;0 [= E][′][ . Let E]t;l ;h [be the set] of all a ∈ Et;l ;h−1 [which agree with e at all positions which have been] read by the i(h)-th processor on a(h) during the first t computation steps. We assume w.l.o.g. that the inputs a(i) are ordered in the following way. a(1) is defined as before. If there is still some input a ∈ Et;l ;h−1 [such that some processor writes into M]l [at t, then a(h) = a .] Otherwise the construction is finished, we set Et;l = Et;l ;h−1 [. Now it is]

;
###### sufficient to prove that at most max 0 t h + 1 additional variables { − } are fixed for the construction of Et;l ;h [out of E]t;l ;h−1 [. Then the number]

=
###### of fixed variables can be estimated by t + + 1 = t(t + 1) 2 . · · ·
 The new claim is proved by induction on h . The assertion is ob

-----

**386**

###### vious for h = 1, since a processor reads at most t inputs during t

        ###### computation steps. For h 1, let R(h 1) and R(h) be the set − of variables we fix for the construction of Et;l ;h−1 [and E]t;l ;h [resp. By]

;
###### the induction hypothesis, R(h 1) max 0 t h + 2 . Since | − | ≤ { − } a(h) was a candidate which could have been chosen as a(h 1), also −

;
###### R[′](h 1) max 0 t h 2 for the set of variables R[′](h 1) which | − | ≤ { − − } − would have been fixed by variables if we chose a(h) as a(h 1) . Ob- − viously R(h) = R[′](h 1) R(h 1), so it is sufficient to prove that − − − the intersection of R[′](h 1) and R(h 1) is not empty. Then R(h) is − − a proper subset of R[′](h 1) . −
 Let i(h 1) and i(h) be the numbers of those processors that write − on a(h − 1) and a(h) resp. at t into Ml .
 Case 1 : i(h 1) = i(h) . If R[′](h 1) and R(h 1) are disjoint, we − ̸ − − define an input b in the following way.

 bj = a(h − 1)j if j ∈ R(h − 1) (5.6)
 bj = a(h)j if j ∈ R[′](h − 1)
 bj = ej if j ̸∈ (R(h − 1) ∪ R[′](h − 1)) .

 On input a(h 1), the i(h 1)-st processor reads on the input tape − − during the first t computation steps only variables which either have been fixed for the construction of Et;l ;h−1 [or have indices in R(h][ −] [1) .] On input b, the i(h 1)-st processor reads the same information, as − all fixed variables agree with e . Since the i(h 1)-st processor writes − on a(h − 1) into Ml at t, it writes also on b into Ml at t . In the same way we conclude that the i(h)-th processor writes on b into Ml at t . The assumption, that R[′](h 1) and R(h 1) are disjoint, leads to a − − write conflict which cannot be solved by a PRAM.

 Case 2 : i(h 1) = i(h) . The inputs a(h 1) and a(h) agree on all − − variables which have been fixed during the construction of Et;l ;h−2 [.] Let t[′] be the first time step where the i(h)-th processor reads on the input tape on a(h 1) a variable which has not been fixed. During the −

; : : : ;
###### computation steps 1 t[′] 1 the i(h)-th processor cannot distinguish − between a(h 1) and a(h) . Hence it reads on both inputs at t[′] in the −


-----

**387**

###### same input cell. The index of this cell is contained in R(h 1) and in − R[′](h 1) . 2 −

 Beame (published by Vishkin and Wigderson (85)) considered an- other complexity measure.

;
###### DEFINITION 5.1 : Let m(f) = min f[−][1](0) f[−][1](1) and let M(f) = {| | | |} n log m(f) . −

 THEOREM 5.4 : If a PRAM computes fn Bn in time T(fn) with ∈

=
###### communication width m, then T(fn) ≥ (M(fn) m)[1][=][2] .

 We omit the proof of this theorem. Obviously M(PARn) = 1 and we obtain a trivial bound. But M(ORn) = n and the lower bound

= =
###### (n m)[1][=][3] of Theorem 5.3 is improved to (n m)[1][=][2] . This bound is optimal for ORn if m = O(n log[−][2] n) (see Theorem 5.1). For a com- parison of the lower bounds of Theorem 5.3 and 5.4 we remark that M(fn) ≤ l max(fn) for all fn ∈ Bn and M(fn) = O(1) for almost all fn ∈ Bn (see Exercises).

 13.6 The complexity of WRAMs with polynomial resources

 In 5 we have proved lower bounds on the time complexity of § WRAMs with very small communication width. Other lower bounds under severe restrictions (either on the number of processors or on the computation power of the processors or on the input size (in the non Boolean case)) have been proved. Beame ((86 a) and (86 b)) proved the first optimal bounds for non-trivial Boolean functions and WRAMs with polynomial resources (number of processors or commu
=
###### nication width). He proved an Ω((log n) log log n)-bound for parity, but actually, the proof works as H˚astad’s proof (see Ch. 11) for all


-----

**388**

###### functions f where l min(f) is sufficiently large. The lower bound can be extended via the simulation of 2 and the reducibility results of § Ch. 10, 3, to many fundamental functions and graph functions. The § optimality of the lower bound follows from the simulation in 2 and § the upper bound of Ch. 11, 2. §
 Beame’s proof works with probabilistic methods. One of the cru- cial ideas is the description of a computation by processor and cell partitions.

 DEFINITION 6.1 : For each WRAM, its i -th processor Pi, its

; : : : ;
###### j -th common memory cell Mj and any time step t ∈{0 T} we

; ;
###### define the processor partition P(i t) and the cell partition M(j t) .

;
###### Two inputs x and y are equivalent with respect to P(i t) iff they lead to the same state of Pi at time step t . Two inputs x and y are

;
###### equivalent with respect to M(j t) iff they lead to the same contents of Mj at time step t .

; : : : ; ;

###### DEFINITION 6.2 : Let A = (A1 Am) be a partition of {0 1}[n] .
 Let fi(x) = 1 iff x ∈ Ai . Let (as in Ch. 11, § 3) l PI(fi) denote the maximal length of a prime implicant of fi . The degree d(A) of A is the maximum of all l PI(fi) .

 Since ANDn, the conjunction of n variables, can be computed by a WRAM in one step, the degree of a cell partition may increase vio- lently during one step. But after having applied a random restriction ρ (see Def. 3.1, Ch. 11), with large probability the degree is not too large. The projection g ρ of a parity function again is a parity function. Hence the degree of the output cell at the end of the computation, i.e. at time step T, is as large as the input size. We choose restrictions such that on the one hand the number of variables does not decrease too fast and, on the other hand, the degree of the partition does only increase slowly. Then the computation time T cannot be too small for the parity function.


-----

**389**

###### Another fundamental notion is that of graded sets of Boolean func- tions.

 DEFINITION 6.3 : A graded set of Boolean functions is a set F of Boolean functions on the same set of n variables together with a grade

N
###### function γ : F such that γ(f) = γ(g) implies f g 0 . → ∪{∞} ∧ ≡

;
###### F determines a partition [F ] of 0 1 . Two inputs x and y are { }[n] equivalent with respect to [F ] iff either f(x) = f(y) = 1 for some f F ∈

<
###### and g(x) = g(y) = 0 for all g F where γ(g) γ(f) or f(x) = f(y) = 0 ∈ for all f F . ∈

 We often make use of the following fact. If ρ is a restriction shrink
; ;
###### ing the input set from {0 1}[n] to {0 1}ρ[n] [, then [][F][ρ][] = [][F] []][ρ] [where][ F][ρ] is the class of all fρ for f ∈ F . In particular we are interested in the following graded set of Boolean functions.

;
###### DEFINITION 6.4 : Let F (j t) be the following graded set of Boolean functions for a given WRAM, a memory cell number j and a time step t . The function f describing an equivalence class with respect

;
###### to P(i t) such that Pi tries to write on inputs of this equivalence

;
###### class into the j -th memory cell at time step t is in F (j t) and has grade i . The function f describing an equivalence class with respect

; ;
###### to M(j t 1) is in F (j t) and has grade . − ∞

;
###### LEMMA 6.1 : i) F (j t) is a graded set of Boolean functions.

; ;
###### ii) [F (j t)] is a refinement of M(j t) .

 Proof : i) follows directly from the definitions.

;
###### ii) We have to prove that x and y are equivalent with respect to M(j t)

;
###### if they are equivalent with respect to [F (j t)] .

; ;
###### Since M(j t 1) is a partition of 0 1, it is impossible that f(x) = 0 − { }[n]

;
###### for all f [F (j t)] . Hence, if x and y are equivalent with respect to ∈

; ;

###### [F (j t)], then f(x) = f(y) = 1 for some f F (j t) and g(x) = g(y) = 0 ∈


-----

**390**

; < <
###### for all g F (j t) where γ(g) γ(f) . If γ(f) = i, the i -th ∈ ∞ processor is on x and y at t in the same state and tries to write the same information into the j -th memory cell. Since no processor with

<
###### a number l i tries to write on x or y at t into Mj, the i -th processor wins the write conflict. On x and y the same information is written into the j -th cell at t . If γ(f) =, no processor writes into the j -th ∞ cell at t for x or y . The contents of this cell remains unchanged. Since

;
###### in this situation x and y are equivalent with respect to M(j t 1), − the contents of the cell is the same for x and y . Hence x and y are

;
###### equivalent with respect to M(j t) . 2

 4 p r � � LEMMA 6.2 : If β satisfies = 2, then
 β(1 + p) [+ 1]


###### 4 p β =
 (1 + p) (2[1][=][r] 1) −


< :
###### 6 p r (6.1)


###### Proof : The easy proof is left to the reader. 2

 MAIN LEMMA 6.3 : i) Let F be a graded set of Boolean functions

;        ###### on {0 1}[n] . Let d([F ]) ≤ r for some r 0 and let ρ ∈ Rp be a random restriction. Then


###### Pr (d([Fρ]) ≥ s) ≤ β[s]


<
###### (6 p r)[s] (6.2)


###### for the constant β of Lemma 6.2.

;
###### ii) The same assertion holds for arbitrary partitions A of 0 1 in- { }[n] stead of [F ] .

 This Main Lemma is proved by Beame (86 b) in a way similar to our proof of the Main Lemma 3.2 in Ch. 11. Although the proof contains some new estimations we do not present it here.

 THEOREM 6.1 : i) Let W be a WRAM computing the parity of n variables in time T = T(n) with p(n) processors and communication width c(n) . Then for large n


-----

**391**

;
###### (6.3)

;
###### and (6.4)


;

###### p(n) + c(n) ≥ [1]
 4 [2][(1][=][24) n][1][=][T]

;

###### p(n) ≥ [1]
 4 [2][(1][=][96) n][1][=][T]

 c(n) ≥ [1]
 4 [2][(1][=][12) (n][=][T!)][1][=][T]


:
###### (6.5)


###### ii) If p(n) is bounded by a polynomial, then

 log n log n log n
 � �
 T(n) ≥
 O(1) + log log n [=] log logn (log logn)[2]

 [−] [O]


:
###### (6.6)


###### iii) If c(n) is bounded by a polynomial, then


###### log n log n
 � �
 T(n) ≥
 2 log logn (log logn)[2]
 [−] [O]


:
###### (6.7)


###### We again emphasize that these bounds hold for all functions fn where l min(fn) is sufficiently large and for all functions fn Bn where ∈ PAR ≤cd f = (fn) . Part ii and Part iii of Theorem 6.1 are simple corollaries to (6.4) and (6.5) resp. The proofs of (6.3) – (6.5) follow the same pattern. We present the proof of (6.4) which seems to be the most important assertion.

; : : : ;
###### Proof of (6.4) : We define restrictions ρ(1) ρ(T) such that ρ(t)

; : : : ;
###### may be applied after ρ(1) ρ(t 1) have been applied. Let π(t) be −

; : : : ; ;
###### the composition of ρ(1) ρ(t) . Let Et be the subcube of {0 1}[n] on which fπ(t) for f ∈ Bn is defined. Let Dt be the dimension of Et and let s = log 4 p(n) .
 We prove for t ≥ 1 that we can choose π(t) such that Dt ≥

= ;
###### (1 48) n (96 s)[−][(t][−][1)] and the degree of all partitions P(i t)π(t) and

; ; ;
###### M(j t)π(t) is bounded by s . P(i t)π(t) and M(j t)π(t) are the partitions

; ; ;
###### P(i t) and M(j t) restricted to Et = {0 1}π[n](t) [.]
 First we show how this claim implies (6.4). Let M1 be the output

;
###### cell. Then the degree of M(1 T)π(T) is equal to DT . The claim implies that


-----

**392**


;
###### s ≥ d(M(1 T)π(T)) = DT ≥ [1]
 48 [n (96 sd)][−][(T][−][1)]


;
###### (6.8)


= :
###### (96 s)[T] 2 n n and s (1 96) n[1][=][T] (6.9) ≥ ≥ ≥

 Since s = log 4 p(n), (6.4) follows from (6.9).

 We prove the claim by induction on t . At time step t = 1 the i -th processor reads one memory cell, and the state afterwards depends on

;
###### a single input bit. Hence the degree of P(i 1) is bounded by 1 s and ≤

;
###### the degree of P(i 1)π(1) cannot be larger.

; ;
###### By Lemma 6.1 ii, [F (j 1)] is a refinement of M(j 1) . By definition

;
###### each f F (j 1) is a function describing an equivalence class of some ∈

; ;
###### P(i 1) or M(j 0) . All these functions depend on at most one variable.

=
###### Let ρ ∈ Rq for q = 1 48 be a random restriction. The Main Lemma implies for r = 1


;
###### Pr (d([F (j 1)ρ]) ≥ s) ≤ (6 q)[s] = 8[−][s] = 2[−][2s][−][2]


= :
###### p(n) (6.10)


###### Each processor knows at most one variable. Hence there are at most two memory cells into which a definite processor may write at time

;
###### step 1 . For at most 2 p(n) memory cells Mj the degree of [F (j 1)ρ]

;
###### may be larger than s . The probability that the degree of all [F (j 1)ρ]

;
###### is less than s is at least 1 − 2[−][2s][−][1] . Since [F (j 1)ρ] is a refinement

; ;
###### of M(j 1)ρ, the function f describing an equivalence class of M(j 1)ρ is the disjunction of some functions gi describing equivalence classes

;
###### of [F (j 1)ρ] . If l PI(gi) ≤ s, also l PI(f) ≤ s . Hence the degree of

; ;
###### M(j 1)ρ is bounded by the degree of [F (j 1)ρ] . The probability that

=
###### D1 ≥ n 48, the expected number of remaining variables, is at least

=
###### 1 3 . Hence we can choose a restriction ρ(1) for which all conditions hold simultaneously.

 For the induction step we assume that the claim holds for some t 1 . The state of the i -th processor at t+1 depends only on the state ≥

;
###### of this processor at t (the partition P(i t)) and on the contents of that cell which the processor reads at t . For all inputs of an equivalence

;
###### class of P(i t) this is the same cell. Hence each equivalence class

; ;
###### of P(i t + 1) is the intersection of some equivalence class of P(i t)


-----

**393**

;
###### and some equivalence class of some M(j t) . If g[′] describes the class of

; ;
###### P(i t) and g[′′] describes the appropriate class of M(j t), then g = g[′] g[′′] ∧

;
###### describes the equivalence class of P(i t + 1) . Obviously l PI(g) is not larger than l PI(g[′]) + l PI(g[′′]) . Hence, by the induction hypothesis,

 � ; � � ; � � ; � : d P(i t + 1)π(t) ≤ d P(i t)π(t) + max M(j t)π(t) ≤ 2 s (6.11)
j

###### We look for a restriction ρ(t+1) which keeps the degrees of the proces- sor and cell partitions small and keeps the number of variables large. Let ρ ∈ Rq be a random restriction for some q chosen later. By (6.11) and the Main Lemma for r = 2 s


###### Pr �d(P(i; t + 1)π(t) ;ρ) ≥ s�


<
###### (12 q s)[s]


:
###### (6.12)


;
###### Now we consider the j -th memory cell Mj . By Lemma 6.1 [F (j t+1)]

;
###### is a refinement of M(j t + 1), this holds also when we restrict the sets

;
###### to Et . By Definition 6.4 each equivalence class of some [F (j t + 1)]π(t)

;
###### is an equivalence class of some P(i t + 1) or an equivalence class of

;
###### M(j t) . By the induction hypothesis and (6.11)

; ;
###### d([F (j t + 1)]π(t)) ≤ 2 s (6.13)

;
###### and also the degree of M(j t+1)π(t) is bounded by 2 s . If no processor writes into Mj at t + 1, the degree is even bounded by s . In the same way as we have proved (6.12) we also conclude that


###### Pr �d(M(j; t + 1)π(t) ;ρ) ≥ s�


<
###### (12 q s)[s]


:
###### (6.14)


###### We hope that the degree of all processor and all cell partitions is simul- taneously bounded by s for some restriction ρ . We have to consider p(n) processors and infinitely many memory cells. But for those mem- ory cells which no processor writes into at t + 1 it is for sure by the induction hypothesis that the degree of M(j; t + 1)π(t) ;ρ is bounded by

;
###### s . By (6.11) the equivalence classes of P(i t + 1)π(t) are described by functions whose prime implicants have a length of at most 2 s . Such a prime implicant is satisfied for a fraction of 2[−][2s] of all inputs. Hence

;
###### P(i t + 1)π(t) partitions the input set to at most 2[2 s] subsets. This


-----

**394**

###### implies that the i -th processor may write only into one of 2[2 s] different memory cells at t + 1 . Altogether for only 2[2 s] p(n) memory cells Mj it is not for sure that the degree of M(j; t + 1)π(t) ;ρ is bounded by s .

=
###### Let q = 1 (96 s) . The probability that the degree of all processor and cell partitions (with respect to π(t) and ρ) is not bounded by s is (since s = 4 log p(n)) at most

 (2[2 s] + 1) p(n) (12 q s)[s] = (2[2 s] + 1) p(n) 2[−][3 s] (6.15)
 = (1 + 2[−][2 s]) p(n) 2[−][s]
 1 = (1 + 2[−][2 s]) p(n)
 4 p(n) [= 1]4 [(1 + 2][−][2 s][)][:]


=

###### The probability that Dt+1 is less than its expected value Dt (96 s) ≥

= =
###### (1 48) n (96 s)[−][t] is bounded by 2 3 . Since


###### 1 � 1 + 2[−][2 s][�] + [2] 4 3


< ;
###### 1 (6.16)


###### we can choose a restriction ρ(t+1) such that all assertions are satisfied for time step t + 1 . 2

 Beame (86 b) generalized his methods (in a way similar to those of H˚astad (86) for bounded-depth circuits, see Ch. 11, 5) and defined § explicitly functions for the following hierarchy results which we present without proofs.

 THEOREM 6.2 : i) For any T such that

 log n log n
 � �
 T = (6.17)
 3 log logn log logn[2]
 [−] [ω]
 there is a Boolean function f ∈ Bn which can be computed by a WRAM with p(n) = n[O(1)] processors in time T but which cannot be computed by a WRAM with p(n) = n[O(1)] processors in time T 1 . − The same holds if the number of processors p(n) and the commu- nication width c(n) simultaneously are bounded by a polynomial.


-----

**395**


###### ii) For any T such that

 log n log n
 � �
 T = (6.18)
 5 log logn log logn[2]
 [−] [ω]


###### there is a Boolean function f ∈ Bn which can be computed by a WRAM with communication width c(n) = n[O(1)] in time T but which cannot be computed by a WRAM with communication width c(n) = n[O(1)] in time T 1 . −

 Essentially the proof of Theorem 6.1 depends only on l min(fn) . The only argument which depends on the parity function is the equality

; ;
###### d(M(1 T)π(T)) = DT in (6.8). The degree of M(1 T)π(T) equals the dimension of the restricted input set, since l min(fn) = n for the parity

;
###### function fn . In the general case the degree of M(1 T)π(T) is not smaller than l PI(gn) where gn = (fn)π(T) . l PI(gn) is not smaller than l min(fn) − (n − DT) (see the proof of Theorem 4.2 iv, Ch. 11). Hence
 s ≥ l min(fn) − n + [1] (6.19)
 48 [n (96 s)][−][(T][−][1)]

 for s = log 4 p(n) . This implies

:
###### 96[T] s[T][−][1](s + n − l min(fn)) ≥ 2 n (6.20)

 For almost all fn ∈ Bn, l min(fn) ≥ n −⌊log n⌋− 1 (see § 7). W.l.o.g. p(n) ≥ n . Then s ≥ n − l min(fn) and


###### 2 n ≤ 96[T] s[T][−][1](s + n − l min(fn)) ≤ 2 · 96[T] s[T]


;
###### (6.21)


= :
###### (96 s)[T] n and s (1 96) n[1][=][T] (6.22) ≥ ≥

 THEOREM 6.3 : The lower bounds of Theorem 6.1 hold for almost all fn Bn . ∈

 Furthermore (6.20) holds for all fn Bn . If l min(fn) is not too ∈ small, we obtain powerful lower bounds on the WRAM complexity of these functions.


-----

**396**

###### 13.7 Properties of complexity measures for PRAMs and WRAMs

 All the powerful lower bounds for bounded-depth circuits, PRAMs or WRAMs depend essentially on one of the following three combinato- rial complexity measures: c(f), the critical complexity of f (Def. 4.2), l min(f), the minimal sensitive complexity or the length of a shortest prime implicant or prime clause of f (Def. 4.1, Ch. 11 and Ch. 13), and l max(f), the maximal sensitive complexity or the length of a longest necessary prime implicant or prime clause of f (Def. 4.1). We inves- tigate these complexity measures in detail. If nothing else is stated explicitly the results are due to Bublitz, Sch¨urfeld, Voigt and We- gener (86).

 We begin with the relations between the single complexity mea- sures.

 THEOREM 7.1 : i) l min(f) ≤ l max(f) and c(f) ≤ l max(f) for all f ∈ Bn .
 ii) l min(ORn) = 1 but c(ORn) = l max(ORn) = n for the symmetric and monotone function ORn Bn . ∈

=
###### iii) There are functions fn ∈ Bn where c(fn) = ⌊n 2⌋+2 but l max(fn) = n 1 . −

=
###### iv) For all n = 6 m, there are functions fn Bn where c(fn) = (1 2) n ∈

=
###### but l min(fn) = (5 6) n .
 v) c(f) ≥ l max(f) 2[l][ max][(f)][−][n] for all f ∈ Bn, in particular c(fn) = n iff l max(fn) = n for fn Bn . ∈

 Proof : i) The first part is obvious and the second part is Proposi- tion 4.1.

 ii) is obvious.

; : : : ;

###### iii) Let fn Sn be defined by its value vector v(fn) = (v0 vn) ∈

= ; =
###### where vi = 1 iff i ∈{⌊n 2⌋ ⌊n 2⌋ + 1} . The assertion holds for


-----

**397**

###### these functions. The proof is left to the reader (who should apply Theorem 7.3).

 iv) Let f ∈ B4 be defined by the following Karnaugh diagram.

 f 0 0 0 1 1 1 1 0
 0 0 0 1 1 1 0 1 0 0 0 1 1 1 1 1 0 1 1 0 0 1 0 0

 By case inspection, c(f) = 2 and l min(f) = 3 . If n = 4m, let fn Bn be equal to the -sum of m copies of f on disjoint sets of ∈ [�]

= =
###### variables. Then c(fn) = (1 2) n and l min(fn) = (3 4) n . Paterson (pers. comm.) defined some f ∈ B6 where c(f) = 3 and l min(f) = 5 . This leads considering the above arguments to the claim of Part iv of the theorem.

 v) We use a pigeon-hole argument. Let k = l max(f) . Then we find an (n k)-dimensional subcube S where f is constant such that f is not − constant on any subcube S[′] which properly contains S . By definition
 � ; :
 c(f a) c(f) S = c(f) 2[n][−][k] (7.1) ≤ | |
a S
_∈_

###### There are k dimensions to increase S, but in each dimension we find a neighbor b of some a S where f(a) = f(b) . Hence ∈ ̸ �c(f ; a) k: (7.2)
 ≥
a S
_∈_

###### The assertion follows from (7.1) and (7.2). 2

=
###### It is an open problem to prove optimal bounds on l min(fn) c(fn)

=
###### or l max(fn) c(fn) . The importance of such bounds has already been discussed in § 4. We obtain optimal results for the classes Mn of monotone functions and Sn of symmetric functions (Wegener (85 b)).


-----

**398**

###### THEOREM 7.2 : c(f) = l max(f) for all f ∈ Mn .

 Proof : Because of Theorem 7.1 i it is sufficient to prove the ˝ ˝-part. ≥

;
###### Let t be a prime implicant of f of length k . Let a 0 1 be defined ∈{ }[n] such that ai = 1 iff xi is contained in t . Since t(a) = 1, also f(a) = 1 . Monoms m, where m(a) = 1, are shortenings of t . Hence t is the unique prime implicant where t(a) = 1 . If b is a neighbor of a such that ai = 1 but bi = 0 for some i, then t(b) = 0 . By monotonicity

;
###### t[′](b) = 0 for all t[′] PI(f) and f(b) = 0 . Hence c(f) c(f a) = k . ∈ ≥ Dual arguments hold for prime clauses. 2

 We remember that vmax(fn) and vmin(fn) denote for fn Sn the ∈ length of a longest and shortest maximal constant substring of v(fn) resp. (see Ch. 11, 4 and Exercises). §

 THEOREM 7.3 : i) l min(f) = n + 1 − vmax(f) for f ∈ Sn .
 ii) l max(f) = n + 1 − vmin(f) for f ∈ Sn .

; : : : ;

###### iii) Let v(f) = (v0 vn) for f ∈ Sn and let v−1 = vn+1 = −1 . If
 vi ̸= vi+1 and vi ̸= vi−1 for some i, then c(f) = n . Otherwise


;
###### c(f) = max{k + 1 n − k | vk ̸= vk+1

 iv) l min(f) ≤ c(f) ≤ l max(f) for f ∈ Sn .

 Proof : i) see Lemma 4.1 in Ch. 11.

 ii) see Exercise 9 in Ch. 11.


; :
###### 0 k n 1 (7.3) ≤ ≤ − }


;
###### iii) If a 0 1 contains i ones, a has i neighbors with i 1 ones and ∈{ }[n] − n i neighbors with i + 1 ones. −
 iv) is obvious by i and iii. 2

=
###### Later we prove that c(f) ≥⌈(n + 1) 2⌉ for all non constant f ∈ Sn . The example in the proof of Theorem 7.1 iii is that symmetric function where l max(fn)[=]c(fn) is maximum. Hence the quotient is bounded by 2 .


-----

**399**

###### By Theorem 7.3, l min(f), c(f) and l max(f) can be computed for f ∈ Sn from v(f) in linear time O(n) . For further fundamental func- tions it is possible to compute the complexity with respect to these complexity measures. But in general this computation is NP-hard. Therefore it is helpful to know the complexity of an easiest function in some class. This yields a lower bound for all other functions in this class.

 DEFINITION 7.1 : Let Fn Bn be a class of functions and let M ⊆ be a complexity measure for the functions in Fn . Then M(Fn) is the minimal M(f) for all f ∈ Fn depending essentially on all n variables.

 Obviously l min(Bn) = l min(Mn) = l min(Sn) = 1 and this assertion leads to useless lower bounds. The situation is different for the critical and the maximal sensitive complexity. The lower bounds of the fol- lowing theorem have been proved by Simon (83) and the upper bounds by Wegener (85 b).

 THEOREM 7.4 : If n 2, ≥
 1
 (7.4)
 2 [log n][ −] 2 [1] [log logn + 1]2

 [≤] [c(B][n][)][ ≤] [l][ max][(B][n][)][ ≤] [l][ max][(M][n][)]
 = c(Mn) ≤ [1]
 2 [log n + 1]4 [log logn + O(1)][:]


###### Proof : It follows from Theorem 7.1 and Theorem 7.2 that c(Bn) ≤ l max(Bn) ≤ l max(Mn) = c(Mn) .

 For the upper bound we define a monotone storage access function

; : : : ; ; : : : ;

###### MSAn on n + k variables x = (x1 xk) and y = (y1 yn) where
 � k � ; : : : ; = n = ⌊k=2⌋ . Let A be the class of all subsets of {1 k} of size ⌊k 2⌋

; : : : ;
###### and let α : A 1 n be one-to-one. Then →{ }


-----

**400**


; �� �
###### MSAn(x y) = T[k]k=2 +1[(x)][ ∨] [�] xi yα(A)
_⌊_ _⌋_ _∧_

A _A_ i A
_∈_ _∈_


:
###### (7.5)


=
###### Only address vectors with exactly ⌊k 2⌋ ones are valid for MSAn . We claim that

= :
###### c(MSAn) = ⌈k 2⌉ + 1 (7.6)

=
###### Obviously the length of all prime implicants is k 2 +1 . For inputs in ⌊ ⌋

< =
###### MSA[−]n [1][(0) let][ l][ be the number of ones in x . If][ l] ⌊k 2⌋−1, the input

= =
###### is 0-critical. If l = k 2 1, the input is at most k ( k 2 1) = ⌊ ⌋− − ⌊ ⌋−

=
###### ⌈k 2⌉ +1-critical, since we have to change some xi from 0 to 1 in order to obtain an input in MSA[−]n [1][(1). Some of these inputs are][ ⌈][k][=][2][⌉] [+ 1-]

=
###### critical, e.g. if all yj = 1 . If l = ⌊k 2⌋, we have to change one of the

= =
###### k −⌊k 2⌋ = ⌈k 2⌉ 0-entries in x or the appropriate yj in order to find a neighbor in MSA[−]n [1][(1). Since][ l][ ≤⌊][k][=][2][⌋] [for inputs in MSA]n[−][1][(0), we] have proved the claim.
 For arbitrary n, we consider the smallest m such that MSAm is defined on at least n variables. We define fn Bn as a subfunction ∈ of MSAm where the appropriate number of y-variables is replaced by ones. Then fn depends essentially on n variables and c(fn) ≤ c(MSAm) . We obtain the upper bound in (7.4) by (7.6) and Stirling’s formula.

 The lower bound is proved by counting methods. At first we prove a simple combinatorial claim.

;
###### CLAIM : Let G be a subgraph of the cube Cn = {0 1}[n] where in Cn the vertices with Hamming distance 1 are connected by an edge. If the degree of each vertex in G is at least r, then G has at least 2[r]
 vertices.

 Proof of the Claim : By induction on n . Obviously n r . If n = r, ≥

            ###### G = Cn and G contains 2[n] vertices. If n r, we partition Cn to Cn[0] 1
_−_
###### and C[1]n−1 [by fixing the last dimension to 0 and 1 resp. If G is contained] in C[0]n−1 [or in C]n[1]−1 [, the claim follows from the induction hypothesis.] Otherwise G is partitioned to G0 ⊆ C[0]n−1 [and G][1][ ⊆] [C]n[1]−1 [. The degree] of each vertex in G0 or G1 is at least r − 1, since only one neighbor


-----

**401**

###### is in the other subcube. It follows from the induction hypothesis that G0 and G1 contain at least 2[r][−][1] vertices each. Hence G contains at least 2[r] vertices. 2

 For the proof of the lower bound let f ∈ Bn depend essentially on n

;
###### variables. We color the cube Cn = {0 1}[n] by coloring the vertex a by

;
###### f(a) and the edge (a b) by 1 if f(a) = f(b) and by 0 otherwise. Since ̸

;
###### c(f a) ≤ c := c(f), each vertex is connected to at most c 1-edges. Cn contains at most c 2[n][−][1] 1-edges.

 We look for a lower estimate on the number of 1-edges. We fix i ∈

; : : : ;
###### {1 n} . Let C0 and C1 be the (n − 1)-dimensional subcubes where we have fixed the i -th dimension to 0 and 1 resp. We estimate the number of 1-edges between C0 and C1 . Since f depends essentially on xi there is a 1-edge between some a ∈ C0 and a(i) ∈ C1 . Again a(i) is

;
###### the i -th neighbor of a . We consider the graph G of all vertices (b b(i))

; ;
###### where b ∈ C0 . The vertices (b b(i)) and (b[′] b[′](i)) are connected by
 an edge iff b and b[′] are neighbors in C0 and f(b[′]) = f(b) ̸= f(b(i)) =

;
###### f(b[′](i)) . Let H be the set of vertices (b b(i)) which can be reached

; ;
###### in G from (a a(i)) . Since f(b) = f(b(i)) for (b b(i)) H, at least ̸ ∈ |H|1-edges are connecting C0 and C1 .

;
###### We claim that each (b b(i)) H has at least n 2c + 1 neighbors ∈ − in G . At most c 1-edges are leaving b, one of them leads to b(i) . At most c 1-edges are leaving b(i), one of them leads to b . Hence there are at least n 2c+1 dimensions to which b and b(i) are connected by −

;
###### 0-edges. These neighbors are in G . The graph of all b where (b b(i)) ∈ H is a subgraph of some (n 1)-dimensional cube where the degree − of each vertex is at least n 2c + 1 . From the combinatorial claim − it follows that this graph contains at least 2[n][−][2c+1] vertices. Hence we have at least 2[n][−][2c+1] 1-edges in the i -th dimension and altogether at least n 2[n][−][2c+1] 1-edges. We combine this result with the upper bound c 2[n][−][1] on the number of 1-edges. Thus

 n 2[n][−][2c+1] c 2[n][−][1] 4 n c 2[2c] (7.7) ≤ ⇒ ≤


-----

**402**


  ###### c [1] ⇒
 2 [log n][ −] [1]2 [log logn + 1]2


:


###### 2

 THEOREM 7.5 : i) If f ∈ Bn depends essentially on n variables, then a PRAM computing f has time complexity Ω(log logn) .
 ii) MSAn depends essentially on more than n variables and can be computed by a PRAM with O(n log n) processors and communi- cation width O(n log n) in time O(log log n) .

 Proof : i) follows from Theorem 7.4 and Theorem 4.3. For the proof of ii we refer to Wegener (85 b). 2

 This result indicates again how excellent the lower bound of The- orem 4.3 is.

=
###### THEOREM 7.6 : c(Sn) = l max(Sn) = ⌈(n + 1) 2⌉ .

 Proof : Obviously c(Sn) ≤ l max(Sn) . For fn = T[n]⌈(n+1)=2⌉ [,][ l][ max][(f][n][) =]

=
###### ⌈(n + 1) 2⌉, since T[n]k [has only prime implicants of length k and prime]

=
###### clauses of length n + 1 − k . Hence l max(Sn) ≤⌈(n + 1) 2⌉ . If f ∈ Sn is not constant, vi = vi+1 for some i . By Theorem 7.3 iii ̸

; =
###### c(f) max i + 1 n i (n + 1) 2 (7.8) ≥ { − } ≥⌈ ⌉

=
###### and c(Sn) ≥⌈(n + 1) 2⌉ . 2

 The lower bound of Theorem 7.4 is optimal, but it implies only a lower bound of Θ(log n) on the critical and maximal sensitive com- plexity of Boolean functions. That is why one looked for fundamental classes of functions for which one can prove better results. One exam- ple is the class of symmetric functions (see Theorem 7.6), and another one is the class of graph properties.

 �n� DEFINITION 7.2 : A Boolean function f on N = 2 variables xij

<
###### (1 ≤ i j ≤ n) is a graph property if for all permutations π ∈ Σn


-----

###### f(x1;2


**403**

; : : : ; xn−1;n) = f(xπ(1);π(2) ; : : : ; xπ(n−1);π(n)) (7.9)


###### is satisfied. We denote the set of all (monotone) graph properties by GN and MGN resp.

 Obviously all graph problems are described by graph properties. A graph problem does not depend on the numbering of the vertices.

= <
###### THEOREM 7.7 : i) ⌊n 4⌋ c(GN) ≤ l max(GN) ≤ n − 1 .
 ii) c(MGN) = l max(MGN) = n − 1 .

 Part i has been proved by Tur´an (84), his conjecture that c(GN) = n − 1 is still open. Only the weaker assertion that c(MGN) = n 1 has been proved by Wegener (85 b). We present only the proof − of Part ii of the Theorem which includes the upper bound of Part i. The proof of the lower bound of Part ii is more typical than the proof of the lower bound of Part i and supports our philosophy that the complexity of functions is described by the length and structure of the prime implicants and prime clauses.

 Proof of Theorem 7.7 ii : For the upper bound we investigate the graph property ˝no vertex is isolated˝ (Tur´an (84)). The proper func- tion f ∈ GN is obviously monotone. Its monotone conjunctive normal form is


###### � �� �; f(x) = 1 i n 1 j<ixji ∨ i<[�]j nxij (7.10)

_≤_ _≤_ _≤_ _≤_


###### each prime clause has length n 1 . The i -th clause computes 0 iff the − i -th vertex is isolated. The prime implicants correspond to minimum graphs without isolated vertices. These are spanning forests where each tree contains at least 2 vertices. The number of edges in spanning forests, and therefore also the length of prime implicants, is bounded by n − 1 . Hence l max(MGN) ≤ n − 1 .
 Since MGN MN, l max(MGN) = c(MGN) by Theorem 7.2. It is ⊆ sufficient to prove that l max(MGN) ≥ n − 1 . All prime implicants


-----

**404**

###### and prime clauses of monotone functions are necessary. Therefore it is sufficient to prove for f ∈ MGN the existence of a prime implicant or prime clause whose length is at least n 1 . This is equivalent to − the existence of a minimum satisfying graph with at least n 1 edges − or a maximum non satisfying graph with at least n 1 missing edges. − A graph G is called satisfying for f ∈ GN iff G satisfies the graph property described by f .

 We assume that all minimum satisfying graphs have at most n 2 − edges, otherwise we are done. We construct a maximum non satisfying graph with at least n 1 missing edges. −
 Let l be the maximal number of isolated vertices in a minimum satisfying graph. For a graph G let m(G) be the minimal degree of a non isolated vertex. Let m be the minimal m(G) for all minimum satisfying graphs with l isolated vertices. We claim that

= :
###### m (2 n 4) (n l ) (7.11) ≤⌊ − − ⌋
 For the proof of this claim we investigate a graph G[∗] defining m . G[∗]
 has, by our assumption, at most n 2 edges. The sum of the degrees − of all vertices is at most 2n 4 . The degree of each of the n l non − − isolated vertices is at least m . Hence the sum of the degrees of all vertices is at least m(n l ) . This implies m(n l ) 2n 4 and − − ≤ − (7.11).

 We construct a maximum non satisfying graph G . Let G[′] consist

; : : : ;

###### of a complete graph Kn−l −1 on the vertices v1 vn−l −1 and l + 1

; : : : ;

###### isolated vertices vn−l vn . It follows from the definition of l that
 G[′] is non satisfying. We add as many edges as possible, until we obtain a maximum non satisfying graph G . For i ≥ n − l, vertex vi is

<
###### connected to at most m − 1 vertices vk where k n − l . Otherwise we could embed G[∗] into G and by monotonicity G would be satisfying.

;
###### For this purpose we identify the vertices vj (j ̸= i j ≥ n − l ) with the l isolated vertices of G[∗] . We identify vi with a vertex v[∗] of degree m in G[∗] and m neighbors of vi with the m neighbors of v[∗] .
 We prove that at least n 1 edges are missing in G . The number of −

; : : : ; ; : : : ;

###### missing edges between the vertex sets v1 vn−l −1 and vn−l vn
 is at least (n l 1 (m 1))(l + 1) . We are done if − − − −


-----

**405**

:
###### (n l m)(l + 1) n 1 (7.12) − − ≥ −

 If l = 0, m = 1 by (7.11) and (7.12) is satisfied. Otherwise it is by (7.11) sufficient to prove that

= :
###### (n l (2 n 4) (n l ))(l + 1) n 1 (7.13) − − − − ≥ −

 If l 1, this is equivalent to ≥

= :
###### l [2] 2 l n + l + n[2] 3 n + 3 (n 4) l (7.14) − − ≥ −

 For l 1 it is sufficient to have ≥
 l [2] 2 l n + l + n[2] 3 n + 3 n 4 or (7.15) − − ≥ −

= = :
###### l n (1 2) (3 n 27 4)[1][=][2] (7.16) ≤ − − −

 In particular, the assertion is proved for n 3 . To capture the cases ≤ where (7.16) is not satisfied we distinguish between two cases.

 Case 1 : G[∗] is not the complete graph on n−l vertices, Kn−l, together with l isolated vertices.
 In this case m ≤ n−l −2 and n−l −m ≥ 2 . Hence vi is for i ≥ n−l

<
###### not connected to at least two of the vertices vj where j n − l . The number of missing edges is at least 2(l + 1) . This is at least n 1 iff −

=
###### l (n 3) 2 (7.17) ≥ −

 is satisfied. It is easy to see that always either (7.16) or (7.17) is satisfied.

 Case 2 : G[∗] is equal to the complete graph on n − l vertices, Kn−l, together with l isolated vertices.
 �r� This minimum satisfying graph has, for r = n l, edges. It − 2 follows from our assumption that �r�

:
###### n 2 (7.18) ≤ −
 2

 Until now we have not counted the missing edges within the vertex

; : : : ;

###### set vn−l vn . Since m ≥ 1, at least l + 1 = n − r + 1 edges are


-----

**406**

###### missing between the two vertex sets. Let z be the number of vertices vi (i ≥ n − l ) which are not connected to at least two vertices vj where

<
###### j n l . Then we may count at least n r + 1 + z missing edges − − between the two vertex sets. Furthermore there are n r + 1 z − − vertices vi (i ≥ n − l ) for which only one edge to the other vertex set is missing. If z r 2, we have already counted enough missing edges. ≥ − Otherwise we partition the n − r + 1 − z vertices vi (i ≥ n − l ) with one missing edge to r − 1 equivalence classes. vi and vj are equivalent if they have the same missing neighbor vk (1 ≤ k ≤ n − l − 1 = r − 1) . If vi and vj are in the k -th equivalence class the edge between vi and vj is missing. Otherwise vi, vj and all vl (1 ≤ l ≤ r − 1, l ̸= k) build an r-clique and G is a satisfying graph.

 Let N(k) be the size of the k -th equivalence class. Altogether we have proved the existence of


###### � n r + 1 + z + −

1 k r 1
_≤_ _≤_ _−_


###### �N(k)�
 (7.19)
 2


###### missing edges. The parameters N(k) satisfy the condition
 � :
 N(k) = n r + 1 z (7.20) − −
1 k r 1
_≤_ _≤_ _−_

###### �N(k)� The sum of all where the parameters N(k) satisfy (7.20) is min2
###### �x� ; : : : ; imal (because of the convexity of x ) if N(1) N(r 1) → 2 { − } consists of at most two numbers M and M + 1 . If the sum of all N(k) �N(k)� is 2 (r 2 z) + (z + 1), the sum of all is minimal if N(k) = 2 − − 2 for r 2 z terms and N(k) = 1 for z + 1 terms. Then the sum of all − − �N(k)� is at least r 2 z and the number of missing edges is at least
2 _−_ _−_
###### n 1 . Hence we are done if −

 n r + 1 z 2 (r 2 z) + (z + 1) = 2 r 3 z (7.21) − − ≥ − − − −

 is satisfied. (7.21) is equivalent to

= :
###### r (n + 4) 3 (7.22) ≤

 It is easy to prove that (7.18) implies (7.22). 2


-----

**407**

###### It follows from Theorem 7.7 and Theorem 4.3 that the PRAM time complexity of all graph properties is Ω(log N) and from Theorem 7.7 and Theorem 5.3 that the time complexity of all graph properties � = with respect to PRAMs of communication width m is Ω (n m)[1][=][3][�] = � = � = Ω N[1][=][6] m[1][=][3][�] . The last lower bound can be improved to Ω (N m)[1][=][3][�]
 for most of the fundamental graph properties f ∈ GN by proving that l max(f) = Θ(N) for these graph properties. Nearly all fundamental graph properties are monotone. Sch¨urfeld and Wegener (86) present conditions which can be tested efficiently and which lead for most of the fundamental graph properties to the assertion that these graph properties are Θ(N)-critical.

 We have seen that some functions have small critical and small maximal sensitive complexity, that several functions have small min- imal sensitive complexity and that many functions have a large com- plexity with respect to the complexity measures. We present tight

;

###### bounds for the complexity of almost all functions in Bn Mn or Sn .
 These results have already been applied in Ch. 11, 4 and Ch. 13, 6, § § and they generalize all lower bounds of Ch. 11 and Ch. 13.

 THEOREM 7.8 : i) The fraction of f ∈ Bn where c(f) = n − 1 or c(f) = n tends to e[−][1] or 1 e[−][1] resp., hence c(f) n 1 for almost − ≥ − all f ∈ Bn .
 ii) c(f) = l max(f) for almost all f ∈ Bn .
 iii) Let α(n) be any function tending to as n . Then ∞ →∞


###### � � n log(n + log[2] n log n + α(n)) − −


<
###### l min(f) (7.23)

 n log(n log n α(n)) ≤ −⌊ − − ⌋


###### for almost all f ∈ Bn, in particular l min(f) ∈ In for almost all f ∈ Bn and some intervals In containing n −⌊log n⌋ and at most one further positive integer.

 Proof : i) We motivate the result. Consider a random Boolean func- tion, i.e. all 2[2][n] f ∈ Bn have the same probability. Then for all


-----

**408**

;
###### a 0 1 ∈{ }[n]

; ;
###### Pr(c(f a) = n) = 2[−][n] and Pr(c(f a) = n 1) = n 2[−][n] −


:
###### (7.24)


; ;
###### Let us assume for a moment that c(f a) and c(f b) are independent,

;
###### which is only satisfied if d(a b) 3 for the Hamming distance d . ≥ Then
 Pr(c(f) = n) = 1 (1 2[−][n])[2][n] 1 e[−][1] and (7.25) − − → −
 Pr(c(f) n 1) = 1 (1 (n + 1) 2[−][n])[2][n] 1 as n . (7.26) ≥ − − − → →∞

;
###### The critical complexity c(f a) is not independent from the critical �n� complexity of only n+ of the other 2[n] 1 inputs. Thus we suggest
2 _−_
###### that (7.25) and (7.26) are almost correct.

;
###### Let Xa(f) = 1 if c(f a) = n − 1 and Xa(f) = 0 otherwise. Let X(f) be the sum of all Xa(f), then X(f) is the number of (n − 1)-critical inputs. Since

        - ;
###### Pr(c(f) n 1) Pr(X 0) (7.27) ≥ − ≥

 it is sufficient to prove that Pr(X = 0) 0 as n . From → →∞ Chebyshev’s inequality follows that

= = :
###### Pr(X = 0) V(X) E[2](X) = E(X[2]) E[2](X) 1 (7.28) ≤ −
 Obviously E(Xa) = n 2[−][n] and E(X) = n . By definition


###### X[2] = [�]a X[2]a [+][ �]a=b Xa Xb = [�]a Xa + a[�]=b Xa Xb

_̸_ _̸_


:
###### (7.29)


###### By case inspection, we prove that

 � ; : E(Xa Xb) = O n[2] 2[−][2n][�] if d(a b) ≤ 2 (7.30)

;
###### If d(a b) 3, c(f,a) and c(f,b) are independent and ≥


###### E(Xa Xb) = E(Xa) E(Xb) = n[2] 2[−][2 n]

 Altogether


:
###### (7.31)


###### � E(X[2]) E(X) + E[2](X) + O n[4] 2[−][n][�] and (7.32) ≤
 �
 Pr(X = 0) n[2] 2[−][n][�] 1 (7.33) ≤ [1] −
 n [+ 1 + O]
 tends to 0 as n . →∞


-----

**409**

###### By a more complicated calculation, using the method of factorial moments, one proves that the number of n-critical inputs is asymp- totically Poisson distributed with parameter λ = 1 . In particular

 Pr(c(f) = n) 1 e[−][1] as n . (7.34) → − →∞

 For a detailed proof of these claims we refer to Bublitz, Sch¨urfeld, Voigt and Wegener (86). (7.34) together with the fact that Pr(c(f) n 1) 1 as n implies the assertions of Part i. ≥ − → →∞

 ii) follows from i, Theorem 7.1 i and Theorem 7.1 v.

 iii) Again we investigate random Boolean functions f ∈ Bn . For f we

;
###### color the vertex a of the input cube 0 1 by f(a) . We want to prove { }[n] that

 Pr (l min(f) ≤ n − c(n)) → 1 (7.35)
 for c(n) = log(n log n α(n)) and ⌊ − − ⌋
 Pr(l min(f) ≤ n − d(n)) → 0 (7.36)
 � � : for d(n) = log(n + log[2] n log n + α(n)) −


###### To prove (7.35) we observe that l min(f) ≤ n − c(n) iff there

;
###### exists a c(n)-dimensional subcube of 0 1 colored by one color. { }[n]

;
###### We partition {0 1}[n] to 2[n][−][c(n)] disjoint c(n)-dimensional subcubes Ci (1 ≤ i ≤ 2[n][−][c(n)]) . Then the events Ei: ˝not all vertices of Ci have the same color˝ are independent. Obviously the probability of Ei is 1 2[−][2][c(n)][+1] . Hence −

 Pr (l min(f) ≤ n − c(n)) ≥ 1 − Pr(∀ i : Ei) (7.37)

 � 1 1 2[−][2][c(n)][�][2][n][−][c(n)] ≥ − −


###### �� = 1 1 2[−][2][c(n)][�][2][2c(n)] [�][2][n][−][c(n)][−][2c(n)] − −


:


###### The right-hand side of this inequality tends to 1 if n c(n) 2[c(n)] tends − − to infinity. This property is fulfilled for c(n) = log(n log n α(n)) . ⌊ − − ⌋


-----

**410**

###### For the second assertion we observe that a function f where l min(f) ≤ n − d(n) has to possess an implicant or a clause of length n d(n) . An implicant or a clause of length n d(n) determines − −
 the value of f on 2[d(n)] inputs. Therefore there are 2[2][n][−][2][d(n)] functions f ∈ Bn with the same fixed implicant or clause of length n−d(n) . Fur- � n � thermore there are 2 2[n][−][d(n)] different implicants and clauses of
n d(n)
_−_
###### length n d(n) . Thus −
 � n � Pr (l min(f) ≤ n − d(n)) ≤ 2[−][2][n] 2 2[n][−][d(n)] 2[2][n][−][2][d(n)] n d(n) −
 (7.38)

:

###### 2[n+1+d(n) (log n][−][1)][−][2][d(n)] ≤
 The right-hand side of this inequality tends to zero if 2[d(n)] (n + 1 + − d(n) (log n 1)) tends to infinity. This happens if −
 � � : d(n) = log(n + log[2] n log n + α(n)) (7.39) −
 2


=
###### THEOREM 7.9 : i) c(f) = l max(f) = ⌈n 2⌉ +1 for almost all f ∈ Mn .

=
###### ii) l min(f) = ⌊n 2⌋− 1 for almost all f ∈ Mn .

 Proof : The proof is based on the characterization of almost all f ∈ Mn due to Korshunov (81 a), see Theorem 5.1, Ch. 4. His result implies that for almost all f ∈ Mn

=
###### a1 + · · · + an ≤⌊n 2⌋− 2 ⇒ f(a) = 0 and (7.40)

= :
###### a1 + · · · + an ≥⌈n 2⌉ + 2 ⇒ f(a) = 1 (7.41)
 Since prime implicants correspond to minimal ones and prime clauses correspond to maximal zeros, we know that for almost all f ∈ Mn the length of any prime implicant or prime clause may take only the values

= ; : : : ; =
###### n 2 1 n 2 + 2 . Hence ⌊ ⌋− ⌈ ⌉

= =
###### ⌊n 2⌋− 1 ≤ l min(f) ≤ l max(f) = c(f) ≤⌈n 2⌉ + 2 (7.42)
 for almost all f ∈ Mn . For the proof of the exact bounds of the theorem we refer to Bublitz, Sch¨urfeld, Voigt and Wegener (86). Here we are satisfied with the weaker result (7.42). 2


-----

**411**

###### THEOREM 7.10 : i) c(f) = l max(f) = n for almost all f ∈ Sn .
 ii) Let α(n) be any function tending to as n . Then ∞ →∞

 n − log n − α(n) ≤ l min(f) ≤ n − log n + α(n) (7.43)

 for almost all f ∈ Sn .

 Proof : i) c(f) = n if the value vector v(f) contains 0 1 0 or 1 0 1 as a

;
###### substring. Obviously almost all v 0 1 contain 0 1 0 or 1 0 1 as ∈{ }[n+1] a substring.
 ii) By Theorem 7.3 i l min(f) = n + 1 − vmax(f) for f ∈ Sn . The claim (7.43) is equivalent to

 log n − α(n) ≤ vmax(f) ≤ log n + α(n) (7.44)

 for almost all f ∈ Sn . This is a well-known result about the longest constant substring of a random 0-1-string of length n + 1 (see e.g. Feller (68)). 2

 EXERCISES

 1. (Cook, Dwork and Reischuk (86)). A PRAM is called almost oblivious if the number of the memory cell into which the i -th processor writes at time step t is allowed to depend on the input length but not on the input itself. A PRAM is called oblivious if also the decision whether the i -th processor writes at time step t may depend on the input length and not on the input itself. The time complexity of oblivious PRAMs computing f is not smaller than ⌈log c(f)⌉ + 1 . Hint: Kt+1 = Lt+1, Lt+1 = Kt + Lt .

 2. The time complexity of almost oblivious PRAMs computing f is not smaller than t if c(f) ≥ F2t+1, the (2t+1)-st Fibonacci number. Hint: Kt+1 = Kt + Lt, Lt+1 = Kt+1 + Lt .


-----

**412**

###### 3. Prove Theorem 7.5 ii.

 4. The graph property ˝no vertex is isolated˝ can be decided by a PRAM with O(N) realistic processors in time log N + O(1) .

 5. Estimate the size and the depth of the circuit designed in the proof of Theorem 3.1.

 6. The processors of a non deterministic WRAM (N-WRAM) may flip during one computation step independent unbiased coins. An

;
###### N-WRAM accepts a 0 1 iff there is an accepting compu- ∈{ }[n] tation path. There is an N-WRAM with O(n) processors and communication width 1 computing T[n]2 [in O(1) steps.]

 7. Prove Lemma 4.2.

 8. Let f ∈ Bn be defined by a set of clauses or implicants and k ∈

; : : : ;
###### 1 n . It is NP-hard to decide whether c(f) k . The same { } ≥ holds for l min and l max .

 9. Investigate the complexity of the outputs of

 a) the binary addition,

 b) the binary multiplication,

 c) the Boolean matrix product,

 d) the Boolean convolution

 with respect to c, l min and l max .

 10. How long are the prime implicants and prime clauses of the mono- tone storage access functions ?


-----

**413**

###### 11. How long are the prime implicants and prime clauses of fn[t] [∈] [B][n] where fn[t][(a) = 1 iff a][i][ =][ · · ·][ = a][i+t][−][1][ (indices modn) for some i ?]

 12. Each non constant graph property depends on all N variables.

 13. The graph properties

 a) G contains a k-clique,

 b) G contains a Hamiltonian circuit,

 c) G contains an Eulerian circuit,

 d) G contains a perfect matching

 are Θ(N)-critical.

 14. The graph property ˝ G contains a vertex whose degree is at least

< <
###### dn ˝ is Θ(N)-critical, if 0 d 1 . ⌈ ⌉

 15. The graph property ˝ G contains no isolated vertex˝ has minimal

=
###### sensitive complexity n 2 . ⌈ ⌉

; ; ;
###### 16. l min(f) = min{l (f 0) l (f 1)} for f ∈ Mn and the constant inputs 0 and 1 .

=
###### 17. Determine the number of f ∈ Mn where l min(f) ≥⌊n 2⌋ + 1 .

 18. Let M be the complexity measure of Def. 5.1. Then M(f) ≤ l max(f) for all f ∈ Bn and M(f) = O(1) for almost all f ∈ Bn .

< <
###### 19. The number of f ∈ Sn where c(f) n or l max(f) n is 2 Fn−1 for the (n − 1)st Fibonacci number Fn−1 .


-----

**414**

###### 14. BRANCHING PROGRAMS

 14.1 The comparison of branching programs with other models of computation

 DEFINITION 1.1 : A branching program (BP) is a directed acyclic graph consisting of one source (no predecessor), inner nodes of fan- out 2 labelled by Boolean variables and sinks of fan-out 0 labelled by Boolean constants. The computation starts at the source which also is an inner node. If one reaches an inner node labelled by xi, one proceeds to the left successor, if the i -th input bit ai equals 0, and one proceeds to the right successor, if ai = 1 . The BP computes f ∈ Bn if one reaches for the input a a sink labelled by f(a) .

 A branching program may be understood as a single processor of arbitrary computation resources which can read at most one input bit per time unit.

 DEFINITION 1.2 : The size of a BP is equal to the number of inner nodes (computation nodes), and the depth of a BP is equal to the length of a longest path. The corresponding complexity measures for f ∈ Bn are denoted by BP(f) and BPD(f) .

 The branching program depth is a measure for the computation time. What is the meaning of the branching program size ? Obviously, a BP of size c can be written as a (non uniform) program of GO TO’s depending on if-tests on the Boolean variables. Then c is the number of GO TO’s, i.e. the program size. The following relations between the branching program size BP(f) and the space complexity S(f) of non uniform Turing machines (see Def. 4.1, Ch. 9) for f have been proved by Cobham (66) and Pudl´ak and Z´ak (83).


-----

**415**

###### THEOREM 1.1 : If fn Bn, then ∈
 � � ; �� S(fn) = O log max{BP(fn) n} and (1.1)

; :
###### BP(fn) = 2[O(h(n))] where h(n) = max{S(fn) log n} (1.2)

 Proof : Let Gn be a BP for fn of size BP(fn) . We simulate Gn by a non uniform Turing machine whose oracle is an encoding of Gn . We encode each node of Gn by its number (O(log BP(fn)) bits), the number of its direct successors (O(log BP(fn)) bits) and the index of its label (O(log n) bits). The encoding of Gn has length look on the input tape for the input bit tested at this node and copy the encoding of the successor node. Hence the space complexity of the Turing machine is bounded by (1.1).

 Let M be a non uniform Turing machine for fn with space complex- ity S(fn) . The number of configurations of M is bounded by 2[O(h(n))]
 (see (3.3) and § 4, Ch. 9). We simulate M by a BP Gn . Each configura- tion of M is simulated by a node, the initial configuration is the source, accepting configurations are 1-sinks, and rejecting configurations are 0-sinks. The successors of a node v simulating the configuration c are the nodes for the configurations c0 and c1 which are the successor configurations of c if M reads on the input tape 0 and 1 resp. The label of v is xi if c is neither accepting nor rejecting and the head of the input tape reads xi . Hence (1.2) is proved. 2

 Moreover, there are tight relations between branching programs and circuits (see e.g. Wegener (84 b)).

 THEOREM 1.2 : i) C(f) ≤ 3 BP(f) for all f ∈ Bn .
 ii) D(f) ≤ 2 BPD(f) for all f ∈ Bn .

; ;
###### iii) BP(f) ≤ LΩ(f) + 1 for all f ∈ Bn and Ω= {∧ ∨ ¬} .


-----

**416**

###### Proof : i) Let G be a BP for f of size BP(f) . At an inner node labelled
 by xi we select the left successor if xi = 0 and the right successor if

; ;
###### xi = 1 . The selection function sel(x y z) = x y ∨ x z selects y if x = 0
 or z if x = 1 . Hence we obtain a circuit over the basis sel with { }
 BP(f) gates for f if we reverse the direction of the edges, all inner
 nodes are sel-gates with the following inputs: xi, the former label of
 the node, v0, the former left successor of the node, and v1, the former
 right successor of the node. The assertion follows since C(sel) = 3 .

 ii) can be proved in a similar way starting with a depth optimal BP.

 D(sel) = 2 .

 iii) is proved by induction on l = LΩ(f). The assertion is obvious

        ###### for l = 0 . Let l = LΩ(f) 0, and let the assertion be proved for
 functions of smaller formula size. Let F be an optimal formula for

 f . If the last gate of F is a -gate, the assertion follows from the ¬
 induction hypothesis, since f and f have the same BP size. If the ¬
 last gate of F is an -gate, f = g h for some functions g and h, where ∧ ∧
 LΩ(g)+LΩ(h) = l −1 . By induction hypothesis, BP(g)+BP(h) ≤ l +1 .
 Hence it is sufficient to prove that BP(f) BP(g) + BP(h) . We use ≤
 optimal BPs G(g) for g and G(h) for h . We obtain a BP G(f) for f

 of size BP(g) + BP(h) in the following way. The source of G(f) is the

 source of G(g) and all 1-sinks of G(g) are identified with the source
 of G(h) . Similar arguments work for an -gate. 2 ∨

 The branching program complexity of f lies in the interval

= ;

###### [C(f) 3 LΩ(f) + 1]. For almost all f ∈ Bn, BP(f) is close to the left end of the interval.


-----

**417**


=
###### THEOREM 1.3 : i) BP(f) ≥ (1 3) 2[n] n[−][1] for almost all f ∈ Bn .
 ii) BP(f) = O(2[n] n[−][1]) for all f ∈ Bn .

 Proof : i) follows from Theorem 2.1, Ch. 4, and Theorem 1.2 i.

 ii) follows from a simple simulation of the improved decoding circuit in 2, Ch. 4. 2 §

 DEFINITION 1.3 : A BP G is synchronous if for all nodes v in G all paths from the source to v have the same length d(v) . The width w(l ) of level l is the number of nodes v with d(v) = l . The width of G is the maximum w(l ) .

 Bounded-depth circuits with gates of unbounded fan-in can be sim- ulated efficiently by branching programs of small width.

 THEOREM 1.4 : If f ∈ Bn can be computed by a circuit with c gates of unbounded fan-in ( -, -gates) and k logical levels, then f can be ∧ ∨

;
###### computed by a BP G of depth c[k][−][1] n and width max 2 k . Hence the { }

;
###### size of G is at most c[k][−][1] n max 2 k . { }


###### Proof : Induction on k . For k = 1 we can compute the conjunction or disjunction of at most n literals. This can be done by a BP of depth n and width 2 . The BP can be constructed in such a way that it has only two sinks, both on the same level.

  - ; : : : ;
###### If k 1, let g1 gm be the functions computed in k − 1 logical

; : : : ;

###### levels. By the induction hypothesis there are BPs G1 Gm of depth

; ; : : : ;
###### c[k][−][2] n and width max{2 k − 1} for g1 gm . If the last gate of the
 circuit is a conjunction (similar arguments work for a disjunction),

; : : : ;

###### we join the BPs G1 Gm in the same way as G(g) and G(h) in
 the proof of Theorem 1.2. We have to ensure that the new BP is synchronous. Therefore we gather the 1-sinks of each Gi on a new path which increases the width by 1 . If k = 2, the new path is not necessary, since Gi has only one 1-sink at its bottom. Since m ≤ c, we obtain a BP for f of depth c[k][−][1] n and width k . 2


-----

**418**

###### This theorem implies that functions with c prime implicants can be computed by a BP of depth c n and width 2 . The theorem also implies that lower bounds on the complexity of width-bounded BPs are harder to achieve than lower bounds on depth-bounded circuits.

;
###### For instance, the parity function is not in SIZE - DEPTH(poly const) but has width-2 BPs of depth n . At the computation nodes on level i (0 ≤ i ≤ n − 1) we test xi+1 . If x1 ⊕· · · ⊕ xi+1 = 0, we proceed to the first node on level i + 1, otherwise to the second node on level i + 1 . On level n the first node is a 0-sink, the second one a 1-sink. We discuss width-bounded BPs more detailed in 5. §

 14.2 The depth of branching programs

 DEFINITION 2.1 : A function f ∈ Bn with BPD(f) = n is called elusive.

 This notation has been introduced by Bollob´as (76). Kahn, Saks and Sturtevant (84) used the notion evasive instead of elusive. The elusiveness of many functions can be proved by the following relation (Bublitz, Sch¨urfeld, Voigt and Wegener (86)) and results of Ch. 13.

 THEOREM 2.1 : BPD(f) ≥ l max(f) ≥ c(f) for all f ∈ Bn .

 Proof : The second inequality has been proved in Proposition 4.1,

;
###### Ch. 13. For the first inequality we consider an input a 0 1 where ∈{ }[n]

; <
###### k := l (f a) = l max(f) If BPD(f) k, the computation path for a in

<
###### some depth-optimal BP for f has length l k . We have tested at most l variables and f is constant on some (n l )-dimensional cube − containing a . Since n l n k + 1, this contradicts the definition − ≥ − of k . 2


-----

**419**

###### This result indicates that many functions are elusive. This fact is also underlined by the following asymptotic results.

 THEOREM 2.2 : i) Almost all f ∈ Bn are elusive.

 ii) Almost all f ∈ Mn are elusive.

 iii) All non constant f ∈ Sn are elusive.


###### Proof : i) (Rivest and Vuillemin (76)). If BPD(f) n 1, we consider ≤ − a depth-optimal decision tree for f . A decision tree is a BP whose nodes have fan-in bounded by 1 . This restriction does not increase the depth. We add computation nodes such that all leaves (sinks) are lying on level n 1 . Since the BP is a tree, we assume w.l.o.g. − that no variable is tested twice on any computation path. Hence each of the 2[n][−][1] leaves is reached for 2 inputs a and b with Hamming

;
###### distance d(a b) = 1 . Each 1-leaf is reached by one input a where a, | | the number of ones in a, is even and one input b where b is odd. | | We conclude that the sets a f[−][1](1) a even and a f[−][1](1) { ∈ | | | } { ∈ |

; : : : ;
###### a odd have the same size k 0 2[n][−][1] if BPD(f) n 1 . For | | } ∈{ } ≤ − �2n−1� fixed k, there are possibilities of choosing k inputs out of the

k
###### 2[n][−][1] inputs with a even. The same holds for a odd. Therefore N(n), | | | | the number of non elusive f ∈ Bn, can be estimated by

n 1 n 1
###### �2 − ��2 − �
 � N(n) (2.1) ≤
 k k

0 k 2[n][−][1]
_≤_ _≤_

n 1 n
###### �2 − �� 2[n][−][1] � � 2 �
 � : = =
 k 2[n][−][1] k 2[n][−][1]

0 k 2[n][−][1] _−_
_≤_ _≤_

###### The number of all f ∈ Bn is 2[2][n] . Hence the assertion i follows from a simple application of the Stirling formula.

 ii) has been proved by Bublitz, Sch¨urfeld, Voigt and Wegener (86) using results of Rivest and Vuillemin (76) and Korshunov (81 a). We do not present the proof here.


n 1
###### �2 −
 k

n 1
###### �2 −
 k


n 1
###### ��2 −
 k


###### � (2.1)


-----

**420**

###### iii) If f ∈ Sn is not constant, then v(f), the value vector of f, is not constant either. Let vi = vi+1 . We consider a depth-optimal decision ̸ tree for f . We follow that path where the first i tested variables have value 1 and the next n 1 i tested variables have value 0 . Afterwards − − it might be possible that the number of ones in the input is i or i + 1 . Since vi = vi+1, we have to test the last variable and the depth of the ̸ tree is n . 2

 It is easy to describe functions with the minimum BP depth.

 THEOREM 2.3 : i) If f depends essentially on n variables, then BPD(f) log(n + 1) . ≥⌈ ⌉
 ii) There are functions f ∈ Bn depending essentially on n variables where BPD(f) = log(n + 1) . ⌈ ⌉

 Proof : i) If f depends essentially on xi, each BP for f contains at least one inner node labelled by xi . Since the fan-out in a BP is bounded by 2, the lower bound follows.

 ii) Consider a binary tree with n inner nodes and depth log(n + 1) ⌈ ⌉ and label exactly one inner node by xi (1 ≤ i ≤ n) . The leaves are labelled in such a way that brothers have different labels. The

; : : : ;

###### function f, computed by this BP, depends essentially on x1 xn
 and its BP depth is log(n + 1) . 2 ⌈ ⌉

 Another example of a simple function with respect to BP depth is the storage access function SAn Bn+k where n = 2[k] (see Def. 5.1, ∈

; : : : ;

###### Ch. 3). First of all, we test the k address variables ak−1 a0 and
 then x|a| . Hence

:
###### BPD(SAn) = k + 1 = ⌈log(n + k + 1)⌉ (2.2)

 It is often difficult to decide whether f is elusive. Elusiveness proofs follow, in general, the pattern of the proof of Theorem 2.2 iii. For each


-----

**421**

###### BP for f one tries to define an input a whose computation path has length n .

 �n� The input size for graph properties is N = . The results of
2

=
###### Ch. 13 imply that BPD(f) ≥ n 4 for all f ∈ GN, BPD(f) ≥ n − 1 for all f ∈ MGN and BPD(f) = Ω(N) for most of the fundamental graph properties. Best, van Emde Boas and Lenstra (74) described a graph property (scorpion graphs) whose BP depth is small, namely at most

                   ###### 6 n . Aanderaa and Rosenberg conjectured that there is some ε 0 such that BPD(f) ≥ ε N for all f ∈ MGN . This conjecture has been

=
###### proved by Rivest and Vuillemin (76) for ε = 1 16 and by Kleitman

=
###### and Kwiatkowski (80) for ε = 1 9 . Kahn, Saks and Sturtevant (84) achieved the best result which is

=
###### BPD(f) ≥ (1 4) N − o(N) for all n and f ∈ MGN and (2.3)
 BPD(f) = N for n = 6 or n = p[k] (p prime) and f ∈ MGN . (2.4)

 The extended conjecture of Karp that all f ∈ MGN are elusive is still open. Further examples of elusive graph properties are ˝the graph contains a k-clique˝ and ˝the graph is k-colorable˝ (Bollob´as (76)). For additional results on elusiveness we refer to Bollob´as (78) and Hedtst¨uck (85).

 14.3 The size of branching programs

 There is no theory on design methods for size optimal BPs. What is known about lower bounds ? We cannot expect ω(n[2])-bounds, since BP(f) L ; ; (f) + 1 (Theorem 1.2 i). The Krapchenko method ≤ {∧ ∨ ¬} cannot be translated to BPs, since this method yields its largest bound for the parity function, and the parity function has linear BPs. But the idea of the Nechiporuk method (Ch. 8, 7) works also for BPs. §


-----

**422**

###### THEOREM 3.1 : Let f ∈ Bn depend essentially on all its variables,

; : : : ;

###### let S1 Sk X be disjoint sets of variables and let si be the number
 ⊆ of Si-subfunctions of f . Then


###### �� = �: BP(f) = Ω (log si) (log logsi) (3.1)

1 i k
_≤_ _≤_

;
###### Proof : We estimate N(r t), the number of BPs of size t on r variables. The number of edges is 2 t, since each inner node has fan-out 2 . Each

; : : : ;

###### edge leaving vi may select its end out of vi+1 vt and the two sinks.
 There are r possible labellings for each inner node. Hence


;
###### N(r t) r[t]((t + 1)!)[2] r[t] t[2t] ≤ ≤


; :
###### if t 3 (3.2) ≥


###### Let r(i) = |Si| and let t(i) be the number of nodes in an optimal BP for f labelled with some xj Si . Each Si-subfunction of f can be ∈ computed by a BP of size t(i) . We only have to replace the other variables by the appropriate constants. Hence


;
###### si ≤ N(r(i) t(i)) ≤ r(i)[t(i)](t(i))[2t(i)]


; :
###### if t(i) 3 (3.3) ≥


###### Since f depends essentially on all variables, r(i) t(i). Therefore ≤


###### si ≤ t(i)[3t(i)]


;
###### if t(i) 3 and (3.4) ≥


= :
###### t(i) = Ω((log si) (log log si)) (3.5)

 Since, by definition, BP(f) is the sum of all t(i), we have proved the theorem. 2

 From the arguments used in Ch. 8, 7, we obtain the follow- § ing results. By Theorem 3.1 one cannot prove larger lower bounds � � than bounds of size n[2] log[−][2] n . BP(ISAn) = Ω n[2] log[−][2] n but C(ISAn) = O(n) for the storage access function for indirect address- ing, BP(detn) = Ω �n[3] log[−][1] n� for the determinant and BP(cl n;m) = � � Ω (n m)[3] log[−][1] n for clique functions. −
 Pudl´ak (84 b) translated the Hodes and Specker method (Ch. 8,

=
###### 5) to BPs and proved Ω(n(log log n) (log log log n)) lower bounds on §


-----

**423**

###### the BP complexity of threshold functions T[n]k [where k and n][−][k are not] too small. Budach (84) applied topological methods, but he obtained only bounds for decision trees.

 14.4 Read-once-only branching programs

 DEFINITION 4.1 : A read-k-times-only branching program (BPk) is a branching program where each variable is tested on each com- putation path at most k times. The minimum size of a BPk for f is denoted by BPk(f) .

 A BP1 is called read-once-only branching program. This computa- tion model was introduced by Masek (76). The corresponding machine model is the non uniform eraser Turing machine, i.e. a Turing machine that erases each input bit after having read it. For BPks each input bit is given k times. Theorem 1.1 holds also for read-once-only BPs and eraser Turing machines. Hence lower bounds on the BP1- com- plexity lead to lower bounds on the space complexity of eraser Turing machines. The same holds for upper bounds.

 For read-k-times-only BPs and k 2 no lower bounds are known ≥ which are essentially larger than lower bounds for general BPs. Hence we consider in this section only read-once-only BPs.
 At first we show that optimal BP1s for symmetric functions f ∈ Sn can be designed by an efficient algorithm working on the value vector v(f) of f (Wegener (84 b)). In the following we denote by Sn the class of all non constant symmetric functions f ∈ Bn .

 THEOREM 4.1 : For all f ∈ Sn there is an optimal BP1 which is synchronous and where all computation nodes on level l are labelled by xl +1 .


-----

**424**

###### Proof : The following claim holds for all BP1s but in general not for BPs. If p is a path in a BP1, then there is an input a(p) for which p is part of the computation path. Let fp be the subfunction of f where we have replaced the variables read on p by the proper constants.
 Now we consider an optimal BP1 G for f ∈ Sn . Let p[′] and p[′′] be paths from the source to the computation node v . We claim, that l (p[′]) = l (p[′′]), where l (p) is the length of p, that we read the same input variables on p[′] and p[′′] (perhaps with different results) and that fp[′] = fp[′′] .

;
###### If v is followed for some b 0 1 by b-sinks only, v can be replaced ∈{ } by a b-sink. Hence we assume that fp[′] and fp[′′] are not constant. fp[′] is a symmetric function on n l (p[′]) variables. By Theorem 2.2 iii the − longest path p starting in v has length n l (p[′]) . The same holds for − p[′′] . Hence l (p[′]) = l (p[′′]) . On p[′] and p[′′] we read all variables that have not been read on p . In particular, we read on p[′] and p[′′] the same set of variables. The BP1 with source v computes fp[′] and fp[′′] . Hence fp[′] = fp[′′] .

 Now we relabel the computation nodes such that the nodes on level l (the BP is synchronous by the claim above) are labelled by xl +1 . We claim that the new BP1 G[′] computes f . Let p be a path in G from the source to a b-sink. If we have chosen m0 times the left successor and m1 times the right successor on p, then f(a) = b for all inputs a with at least m0 zeros and at least m1 ones. If the same path is used in G[′], the input contains at least m0 zeros and at least m1 ones. The output b is computed correctly. 2

 By this theorem on the structure of optimal BP1s for symmet- ric functions f, we can design optimal BP1s efficiently. The level 0 consists of the source labelled by x1 . At each node v on level l we still have to compute a symmetric function fv on n − l variables. The

; : : : ;

###### node v gets a second label i indicating that (vi vi+n l) is the value

_−_
###### vector of fv . This additional label is i = 0 for the source. For a node v on level l labelled by xl +1 and i we need two successors v[0] and v[1] on


-----

**425**

###### level l + 1 with labels xl +2 (if l + 2 ≤ n) and i or i + 1 resp. The only problem is now to decide which nodes on level l + 1 can be merged or replaced by sinks. A node can be replaced by a constant iff the proper value vector is constant. Two nodes can be merged iff the proper value vectors coincide.

 The number of nodes constructed on level l + 1 is at most 2 N(l ) where N(l ) is the minimum number of nodes on level l in an optimal BP1 for f . This consequence results from the fact that all nodes on level l for which we have constructed successors belong to an optimal BP1 for f . We know the value vectors which belong to the nodes on level l + 1 . By a generalized bucket sort we sort these value vec- tors in time O(nN(l )) according to the lexicographical order. In time O(nN(l )) it can be decided which nodes can be replaced by sinks and which nodes can be merged. We continue until all nodes are replaced by sinks on level n . Altogether we have constructed an optimal BP1 for f ∈ Sn in time O(n BP1(f)) . If we can handle also large numbers in one unit of time, we can decrease the running time of the algorithm to O(BP1(f)) . But then the space complexity is large, namely O(2[n]) . The original algorithm can be performed with linear space.

 THEOREM 4.2 : There is an O(n BP1(f))-time and O(n)-space algorithm for the computation of an optimal BP1 for f ∈ Sn given by its value vector.

 Together with this algorithm we obtain the following characteriza- tion of the BP1-complexity of symmetric functions.

 THEOREM 4.3 : For f ∈ Sn let rl (f) (0 ≤ l ≤ n − 1) be the number

; : : : ;

###### of different non constant subvectors (vi vi+n l) (0 i l ) of the

_−_ _≤_ _≤_
###### value vector v(f) .


###### � : i) BP1(f) = rl (f)

0 _l_ n 1
_≤_ _≤_ _−_


-----

**426**

###### � � ; � ii) BP1(f) min l + 1 2[n][−][l] [+1] 2 ≤ −

0 _l_ n 1
_≤_ _≤_ _−_


###### = n[2]


= :
###### 2 n log n + O(n) −


###### Proof : i) follows from Theorem 4.1 and the algorithm from Theorem 4.2. For ii) we state that rl (f) ≤ l +1 (we consider only l +1 subvectors) and that rl (f) ≤ 2[n][−][l] [+1] − 2 (we consider non constant vectors of length n l + 1) . 2 −

 If the value vector of f ∈ Sn is a de Bruijn sequence (see Exercises), we obtain a symmetric function of maximum BP1-complexity. The proofs of the following results on the majority function T[n]n=2
_⌈_ _⌉_ [and the]

=
###### exactly - ⌈n 2⌉ function E[n]⌈n=2⌉ [are left as an exercise.]

=

###### THEOREM 4.4 : i) BP1(T[n]n=2 4 + Θ(n) .
_⌈_ _⌉[) = n][2]_

=

###### ii) BP1(E[n]n=2 4 + Θ(n) .
_⌈_ _⌉[) = n][2]_

###### iii) BPk(E[n]n=2
_⌈_ _⌉[) = O(n][(k+1)][=][k][) .]_

###### iv) BP(E[n]n=2
_⌈_ _⌉[) = O(n log][2][ n][=][ log log n) .]_


###### All symmetric functions have BP1-complexity bounded by O(n[2]) (Theorem 4.3 ii). Because of the small number of subfunctions many computation paths can be merged after a short time. For many other functions f one can prove that paths, whose lengths are at most d, cannot end in a sink and cannot be merged with other computation paths. Then each BP1 for f contains at its top a complete binary tree of d levels and therefore at least 2[d] 1 computation nodes. This − lower bound method has been introduced by Wegener (84 c) for the proof of lower bounds on the BP1-complexity of clique functions cl n;k (see Def. 11.1, Ch. 6). Dunne (85) applied this method to the logical permanent PMn (perfect matching, see Def. 12.2, Ch. 6) and to the Hamiltonian circuit functions (see Exercise 32 b, Ch. 6).


-----

**427**

###### THEOREM 4.5 : Let G be a BP1 for the clique function cl n;k . Let p and q be different paths in G starting at the source and ending �k� in v(p) and v(q) resp. If at most k(1) = 1 ones and at most
2 _−_
###### k(0) = n k[2] + 2 zeros have been read on p and q, then neither v(p) − nor v(q) is a sink and v(p) = v(q) . In particular ̸


###### � BP1(cl n;k) ≥

0 m k(0)+k(1)
_≤_ _≤_


###### �

m k(0) j k(1)
_−_ _≤_ _≤_


###### �m� j


:
###### (4.1)


###### Proof : (4.1) follows easily from the first part of the theorem. For each

; : : : ;

###### 0-1-sequence a1 am with at most k(0) zeros and k(1) ones there is
 a computation node in G . The lower bound in (4.1) is equal to the number of these sequences.

 We turn to the proof of the structural results. Before we have not tested all variables of a prime implicant or a prime clause with the right result we do not reach a sink. cl n;k is monotone. Consequently, the variables of a prime implicant have to be ones. All prime implicants of cl n;k have length �k2� > k(1), they correspond to a minimal graph with
 a k-clique. According to the results of Ch. 13 prime clauses correspond to maximal graphs without any k-clique. The largest maximal graphs are by Tur´an’s theorem (see e.g. Bollob´as (78)) complete (k 1)- −

= =
###### partite graphs where the size of all parts is n (k 1) or n (k 1) . ⌊ − ⌋ ⌈ − ⌉ We have to estimate the number of missing edges. This number is

=
###### underestimated if we assume that all parts have size n (k 1) and −

=
###### each vertex is not connected to n (k 1) 1 other vertices. Hence − −

= =
###### l (0) (1 2)n(n (k 1) 1) for the length l (0) of the shortest prime ≥ − −

     ###### clause. Since l (0) k(0), neither v(p) nor v(q) is a sink.

 Let us assume that w = v(p) = v(q) . Since p and q are different paths, there is a first node w[′] where the paths separate. W.l.o.g. w[′] is labelled by x1;2 . Let Gp and Gq be the partially specified graphs spec- ified by the computation paths p and q resp. Edges tested positively are called existing, whereas edges tested negatively are called forbid- den, all other edges are called variable. W.l.o.g. the edge (1,2) exists in Gp and is forbidden in Gq . Let G[′] be the part of G whose source


-----

**428**

###### is w . We shall prove the existence of a path r from w to some sink such that we have to reach a 1-sink on the compound path (p,r) and a

;
###### 0-sink on (q r) . This will contradict the assumption that v(p) = v(q) .

 Let A be the set of vertices i 1,2 such that i lies on some ̸∈{ } existing edge in Gq . Since Gq contains at most k(1) edges,

:
###### A 2 k(1) = k[2] k 2 (4.2) | | ≤ − −

; ;
###### Let B be a set of vertices j 1 2 such that for each edge e = (i i[′]) ̸∈{ } forbidden in Gp, i ∈ B or i[′] ∈ B . It is possible to choose B such that

:
###### B k(0) = n k[2] + 2 (4.3) | | ≤ −

; : : : ;
###### The set C := 1 n A B contains at least k vertices, among { } − − them the vertices 1 and 2 . Let D C be chosen such that D = k ⊆ | |

;
###### and 1 2 D . Let r be the path from w to a sink where we choose ∈

;
###### the right successor, the 1-successor, iff i j ∈ D for the label xij of the

;
###### computation node. The path (p r) leads to a 1-sink, since no edge on D has been tested negatively. Let Gq;r be the graph specified on (q; r) . Only vertices in D ∪ A may have positive degree. Since Gq does not contain any k-clique and only edges on D are tested positively on r, a k-clique in Gq;r has to contain two vertices of D . Since the edge (1; 2) is forbidden, a k-clique in Gq;r has to contain a vertex i ∈ D −{1; 2}

; ;
###### and a vertex j A . The edge (i j) is not tested positively on (q r) . ∈ Hence Gq;r does not contain any k-clique, and the path (q; r) leads to a 0-sink. 2

 COROLLARY 4.1 : i) BP1(cl n;k) = Ω(n[k(k][−][1)][=][2][−][1]) for constant k .
 ii) BP1(cl n;m(n)) ≥ 2[n][=][3][−][o(n)] for m(n) = �(2n=3)[1][=][2][�] .
 iii) BP1(cl n;n=2) ≥ 2[n][=][6][−][o(n)] .
 iv) The space complexity of eraser Turing machines for cl n;n=2 is �n� Ω(n) = Ω(N[1][=][2]) where N = is the input size.
2

###### �k(0)+k(1)� Proof : i) follows from (4.1) where is the largest term.
k(1)


-----

**429**

=
###### ii) By definition of m(n), k(0) and k(1) are of size n 3 o(n) . Each − BP1 for cl n;m(n) contains at the top a complete binary tree of depth

=
###### n 3 o(n) . −
 iii) cl n−m(n); n=2−m(n) is a subfunction of cl n;n=2 . Let m(n) = n=2 − � = = (n 3)[1][=][2][�] . Then k(0) and k(1) are of size n 6 o(n) . −
 iv) is a corollary to iii. 2

 Larger lower bounds have been proved by Ajtai, Babai, Hajnal, Koml´os, Pudl´ak, R¨odl, Szemer´edi and Tur´an (86).

 THEOREM 4.6 : Let cl n;3 be the graph property computing 1 if
 [�] the number of triangles (3-cliques) in the graph specified by x is odd. Then BP1 ([�] cl n;3) = 2[Ω(N)] and the space complexity of eraser Turing machines for [�] cl n;3 is Ω(n[2]) = Ω(N) .

 Recently Kriegel and Waack (86) gave an easier proof of a 2[Ω(N)]- bound for another function. We do not prove these theorems. We prove two results which we shall apply in 6. The first one is due to § Wegener (86 a).

 DEFINITION 4.2 : cl [∗]n;k [∈] [MG][N][ is the graph property which tests] whether a graph contains a k-clique of special type, these are k-cliques

; : : : ;

###### where at least k − 2 vertices i1 ik−2 build a consecutive sequence

; ; : : : ;
###### i i + 1 i + k 3 mod n . −

 � THEOREM 4.7 : BP1(cl [∗]n;k(n)[) = 2][m(n)][ if k(n) =] n[1][=][3][�] and m(n) =

=
###### (1 4) n[2][=][3] o(n[2][=][3]) . −

 Proof : After m(n) positive tests we still have not found a k-clique

=
###### of special type. After m(n) negative tests at most (1 2) n[2][=][3] vertices lie on a forbidden edge. Hence there is a consecutive sequence of k(n) vertices which may still build a k(n)-clique of special type. The depth of all sinks is larger than m(n) .


-----

**430**

###### It is now sufficient to prove that two paths p and q whose lengths are bounded by m(n) and which start at the source of a BP1 for cl [∗]n;k(n) cannot stop at the same node. Again w.l.o.g. (1,2) exists in Gp but is forbidden in Gq . There is a set of vertices D such that |D| = k(n), D contains the vertices 1 and 2, D contains a consecutive sequence of k(n) 2 vertices, and no edge incident to some i D 1,2 has been − ∈ −{ } tested on p or q . The proof is completed on the pattern of the proof of Theorem 4.5. 2

 DEFINITION 4.3 : cl on GN (n even) is the graph property which ∈

=
###### tests whether a graph contains an n 2-clique but no edge outside of this clique.

 This so-called clique-only function has been investigated by Pudl´ak and Z´ak (83) and Z´ak (84). The function has short prime clauses. If the edges (1,2) and (1,3) exist, but (2,3) is forbidden, we know that �n� cl on(x) = 0 . But all prime implicants have length N = 2 . It is possible to prove that the ˝width˝ of a BP1 for cl on is somewhere not too small.

 THEOREM 4.8 : BP1(cl on) ≥ 2[n][=][3][−][o(n)] .

 Proof : W.l.o.g. n can be divided by 6 . Let G be a BP1 for cl on .

=
###### For a vertex set H of size n 2 let p(H) be the computation path for the graph that contains only the clique on H . Let v(H) be the first

=
###### computation node on p(H) where at least n 2 2 vertices lie on an −

=
###### existing edge. We claim that v(H) = v(H[′]) if H H[′] n 2 3 . We ̸ | ∩ | ≤ − conclude the theorem from our claim before we prove the claim. We

; : : : ;
###### partition the vertex set {1 n} to three sets M1, M2 and M3 each
= = �n=3�
###### of size n 3 . The number of subsets of Mi of size n 6 is a = n=6 . Let Mi;j (1 ≤ j ≤ a) be these sets. We consider Hj, the union of M1;j, M2;j and M3;j for 1 ≤ j ≤ a . Then |Hj ∩ Hj[′]| ≤ n=2 − 3 if j ̸= j[′] .

; : : : ;
###### The computation nodes v(H1) v(Ha) are different due to the claim above. Hence G contains at least a = 2[n][=][3][−][o(n)] computation nodes.


-----

**431**

###### For the proof of the claim we assume that v(H) = v(H[′]) although

=
###### H H[′] n 2 3 . Let p[∗](H) and p[∗](H[′]) be those parts of p(H) and | ∩ | ≤ −
 p(H[′]) resp. that lead from the source to v(H) . On p[∗](H) and p[∗](H[′])

 we have tested the same set of variables. Otherwise some path, where

 not all variables are tested, would lead from the source to a 1-sink

 although all prime implicants have length N .

 We investigate the computation path leading from the source via

 p(H) to v(H) and then via p(H[′]) to a 1-sink. The computation path

= =
###### is the path p(H[′′]) for some set H[′′] of size n 2 . H H[′′] n 2 2 by | ∩ | ≥ −
 definition of v(H) . In particular, H[′′] contains some vertex i H[′] . We ̸∈
 prove the claim by proving that H[′] = H[′′] . Each positive test increases

 the number of vertices lying on existing edges at most by 2 . Hence

;
###### there is some j H[′] such that no edge (j ) has been tested positively ∈ ·

;
###### on p[∗](H[′]) . For all k H[′] j, the edge (j k) is tested positively on ∈ −{ }
 the second part of p(H[′]) and therefore on p(H[′′]) . All these vertices
 k ∈ H[′] and j have to belong to H[′′] because of the definition of cl on . 2

 We have proved exponential lower bounds on the BP1-complexity
 of NP-complete functions like cl n;n=2 but also on the BP1-complexity
 of functions in P like cl on, cl [∗]n;k(n) [and][ �] [c][l][ n][;][3][ .]

 14.5 Bounded-width branching programs

 We have defined the width of BPs in Definition 1.3. By Theo- rem 1.4 all f ∈ Bn can be computed by a width-2 BP. Therefore w-k-BP(f), the minimum size of a width-k BP for f, is well-defined for k 2 . We have already proved in Theorem 1.4 that depth-bounded ≥


-----

**432**

###### circuits can be simulated efficiently by width-bounded branching pro- grams. But the converse is false. The parity function has linear width-2 complexity but exponential size in circuits of constant depth (see Ch. 11, 3). Later we present a complete characterization of BPs § of bounded width and polynomial size.

 Before that we report the history of lower bounds. Borodin, Dolev, Fich and Paul (83) proved that width-2 BPs for the majority function � � have size Ω n[2] log[−][1] n . By probabilistic methods Yao (83) improved this result. Width-2 BPs for the majority function cannot have poly- nomial size. Shearer (pers. comm.) proved an exponential lower bound on the width-2 BP complexity of the counting function C[n]1;3 computing 1 iff x1 + · · · + xn ≡ 1 mod 3 .
 For k 3 no large lower bounds on the width-k BP complexity ≥ of explicitly defined Boolean functions are known. Using the Ram- sey theory (see e.g. Graham, Rothschild and Spencer (80)) Chandra, Fortune and Lipton (83) proved that there is no constant k such that the majority function can be computed in width-k BPs of linear size. Ajtai et al. (86) could prove non trivial lower bounds for BPs whose width is not larger than (log n)[O(1)] (poly log). Almost all symmetric functions, and in particular the following explicitly defined function ˝ x1 +· · ·+xn is a quadratic residue mod p for a fixed prime p between n[1][=][4] and n[1][=][3] ˝, cannot be computed by poly log - width BPs of size

=
###### o(n(logn) log log n) .

 All these results are motivated by the conjecture that the ma- jority function cannot be computed by BPs of constant width and polynomial size. But this conjecture has been proved false by Bar- rington (86).

 THEOREM 5.1 : Let fn Bn . There is for some constant k a ∈ sequence of width-k BPs Gn computing fn with polynomial size iff there is a sequence Sn of circuits with binary gates computing fn with polynomial size and depth O(log n) .


-----

**433**

###### Each symmetric function fn Sn can be computed by a circuit of ∈ linear size and logarithmic depth (Theorem 4.1, Ch. 3). Hence The- orem 5.1 implies the existence of polynomial BPs of constant width for all symmetric functions, among them the majority function. We prove Theorem 5.1 in several steps.

 Proof of Theorem 5.1, only-if-part : Let Gn be BPs computing fn in constant width k and polynomial size p(n) . The nodes of Gn are denoted in the following way: vi;j (1 ≤ i ≤ k, 0 ≤ j ≤ p(n)) is the i -th node on level j, v1;0 is the source, w.l.o.g. we have only two sinks both on level p(n), v1;p(n) is the 1-sink, v2;p(n) the 0-sink. Let gi;j;i[′] ;j[′][(x) = 1 if]
 starting at the node vi;j on input x we reach vi[′] ;j[′][ . Then f]n [= g]1;0;1;p(n) [.]
 The functions gi;j;i[′] ;j+1 [depend essentially at most on one input vari-]
 able, namely the label of vi;j . These functions can be computed at a

< <
###### single gate. Let j j[′] j[′′] . Each path from level j to level j[′′] has to
 pass through level j[′] . Hence


###### gi;j;i[′′]


;j[′′][(x) =] � gi;j;i[′]

1 i[′] k
_≤_ _≤_


;j[′][(x)][ ∧] [g]i[′]


;j[′]


;i[′′]


;j[′′][(x)][:] (5.1)


###### This leads to a divide-and-conquer approach. W.l.o.g. p(n) = 2[m(n)] . Then m(n) = O(log n) . We proceed in m(n) steps. In Step 0 we compute in parallel all gi;j;i[′] ;j+1[(x). In Step r we apply (5.1) and com-]
 pute in parallel all gi;j;i[′′] ;j[′′][ where j is a multiple of 2][r][, j][′′][ = j + 2][r]
 and j[′] = j + 2[r][−][1] . The functions on the right-hand side of (5.1) are computed in Step r−1 . In Step m(n) we compute g1;0;1;p(n) = fn . Alto- gether we apply (5.1) not more than 2 k[2] p(n) times. (5.1) can be real- ized by a circuit of size 2 k and depth log k +1 . Hence there is a cir- ⌈ ⌉ cuit for fn of size 4 k[3] p(n) and depth (⌈log k⌉+1) ⌈log p(n)⌉ = O(log n) . 2

 For the if-part Barrington introduced a new type of BPs.

 DEFINITION 5.1 : A permutation σ ∈ Σ5 is called a 5-cycle if

; ; ; ; : : : ;
###### σ[i](j) = j for i 1 2 3 4 and j 1 5 . We present a 5- ̸ ∈{ } ∈{ }


-----

**434**

###### cycle σ by the string (a1 a2 a3 a4 a5) where σ(ai) = ai+1 for i ≤ 4 and σ(a5) = a1 .

 DEFINITION 5.2 : A permutation branching program (PBP) of width k and length (or depth) l is given by a sequence of instruc
; ; < ;
###### tions (j(i) gi hi) for 0 ≤ i l, where 1 ≤ j(i) ≤ n and gi hi ∈ Σk .
 A PBP has on each level 0 ≤ i ≤ l k nodes v1;i ; : : : ; vk;i . On level i
 we realize σi(x) = gi if xj(i) = 0 and σi(x) = hi if xj(i) = 1 . The PBP computes σ(x) = σl −1(x) · · · σ0(x) ∈ Σk on input x . The PBP com- putes fn ∈ Bn via τ if σ(x) = id for x ∈ fn[−][1][(0) and][ σ][(x) =][ τ][ ̸][= id for] x ∈ fn[−][1][(1).]


###### LEMMA 5.1 : A PBP for f of width k and length l can be simulated by a BP of width k and length k l .

 Proof : The PBP has k ˝sources˝ on level 0 . We obtain k BPs of width k and length l (one for each source). The nodes vm;i (1 ≤ m ≤ k) are labelled by xj(i), and the wires from level i to level i+1 correspond to gi and hi . The nodes on the last level are replaced by sinks. In the r -th BP the τ (r)-th node on the last level is replaced by a 1-sink, all other sinks are 0-sinks. This BP computes 1 iff σ(x)(r) = τ (r) . Hence f(x) = 1 iff all BPs compute 1 . Similarly to the proof of Theorem 1.4 we combine the k BPs to a BP for f . We do not have to increase the width since all sinks lie on the last level. 2

 Hence it is sufficient to design PBPs of width 5 . We restrict our- selves to 5-cycles τ which have properties that serve our purposes.

 LEMMA 5.2 : If the PBP G computes f via the 5-cycle τ and ρ is another 5-cycle, then there is a PBP G[′] of the same length computing f via ρ .

 Proof : The existence of ϑ ∈ Σ5 where ρ = ϑ τ ϑ[−][1] follows from elementary group theory (or by case inspection). In G[′] we simply


-----

**435**

###### replace the permutations gi and hi in the sequence of instructions by ϑ gi ϑ[−][1] and ϑ hi ϑ[−][1] resp. Then the output permutations id and τ are replaced by ϑ id ϑ[−][1] = id and ϑ τ ϑ[−][1] = ρ . 2

 LEMMA 5.3 : If the PBP G computes f via the 5-cycle τ, then there is a PBP G[′] of the same length computing f via a 5-cycle. ¬

 Proof : Obviously τ [−][1] is a 5-cycle. We only change the last instruc- tion : gl −1 is replaced by τ [−][1] gl −1 and hl −1 is replaced by τ [−][1] hl −1 . Then σ[′](x) = τ [−][1] σ(x) . Hence σ[′](x) = τ [−][1] for x ∈ f[−][1](0) and σ[′](x) = id for x ∈ f[−][1](1) . G[′] computes ¬f via τ [−][1] . 2

 LEMMA 5.4 : There are 5-cycles τ1 and τ2 such that τ1 τ2 τ1[−][1] τ2[−][1] is a 5-cycle.

 Proof : (1 2 3 4 5) (1 3 5 4 2) (5 4 3 2 1) (2 4 5 3 1) = (1 3 2 5 4) . 2

 THEOREM 5.2 : Let f be computed by a depth-d circuit S over the basis U2 . Then there is a PBP G computing f in width 5 and length 4[d] .

 Proof : The proof is by induction on d . For d = 0 the assertion is obvious. For the induction step we assume (by Lemma 5.3 w.l.o.g.) that the last gate of S is an ∧-gate where f is computed as f = f1 ∧ f2 . Hence, by induction hypothesis, for f1 and f2 there are PBPs G1 and G2 of length 4[d][−][1] each computing f1 and f2 via the 5-cycles ρ1 and ρ2 resp. By Lemma 5.2 and Lemma 5.4 we replace ρ1 and ρ2 by τ1 and τ2 resp. such that τ1 τ2 τ1[−][1] τ2[−][1] is a 5-cycle. Furthermore there are PBPs G3 and G4 of length 4[d][−][1] each computing f1 and f2 via the 5-cycles τ1[−][1] and τ2[−][1] resp. (see Lemma 5.2). If we concatenate the PBPs G1, G2, G3 and G4, we obtain a PBP G of length 4[d] . Let σ(x) = σ1(x) σ2(x) σ3(x) σ4(x) ∈ Σ5 be the permutation computed by G .


-----

**436**

###### 1. f1(x) = f2(x) = 0 ⇒ σ1(x) = · · · = σ4(x) = id ⇒ σ(x) = id .
 2. f1(x) = 0, f2(x) = 1 ⇒ σ1(x) = σ3(x) = id, σ2(x) = τ2, σ4(x) = τ2[−][1] ⇒ σ(x) = id .
 3. f1(x) = 1, f2(x) = 0 ⇒ σ(x) = id (similarly to Case 2).
 4. f1(x) = f2(x) = 1 ⇒ σ(x) = τ1 τ2 τ1[−][1] τ2[−][1], a 5-cycle and therefore unequal to id .
 Hence G computes f = f1 f2 in width 5 and length 4[d] . 2 ∧

 Proof of Theorem 5.1, if-part : We only have to concatenate the constructions of Theorem 5.2 and Lemma 5.1. 2

 This result explains also why one was not able to prove non polyno- mial lower bounds on the width-k BP complexity of explicitly defined functions if k 5 . ≥

 14.6 Hierarchies

 We have proved implicitly that certain functions are hard in some models and simple in other models. We summarize these results.

 THEOREM 6.1 : The majority function has non polynomial com- plexity with respect to circuits of constant depth and BPs of width 2, but it has polynomial complexity with respect to monotone circuits, monotone formulas, BP1s and BPs of width 5 .

 THEOREM 6.2 : The clique function cl [∗]n;k(n) [for cliques of special] � type and size k(n) = n[1][=][3][�] has exponential complexity with respect to BP1s, but it has polynomial complexity with respect to width-2


-----

**437**

###### BPs, depth-2 circuits, monotone circuits, and monotone formulas.

 Proof : The number of prime implicants of cl [∗]n;k(n) [can easily be esti-] mated by O(n[3]) . 2

 THEOREM 6.3 : � cl n;3 has exponential complexity with respect to BP1s, but it has polynomial complexity with respect to BPs of constant width and circuits.

 Proof : We only have to prove the upper bound. In constant depth we decide with O(n[3]) binary gates for each 3-clique whether it exists. Then we compute the parity of these results in logarithmic depth and size O(n[3]) . Finally we apply Theorem 5.1. 2

 In Ch. 11, § 5, we have seen that the classes Σk(P) build a proper hierarchy.

 DEFINITION 6.1 : Let w-k-BP(P) be the class of sequences f = (fn) of functions fn Bn which can be computed by width-k BPs of ∈ polynomial size.

 Obviously w-k-BP(P) w-(k + 1)-BP(P) for k 2 . The results ⊆ ≥ of Barrington (86) (see 5) imply that this hierarchy collapses at the § fifth level. But, from the results on the majority function, we know that w-2-BP(P) ⫋ w-5-BP(P) .

 DEFINITION 6.2 : Let BPk(P) be the class of sequences f = (fn) of functions fn Bn which can be computed by read-k-times-only BPs ∈ of polynomial size.


-----

**438**

###### Obviously BPk(P) BP(k + 1)(P) for all k . We conjecture that ⊆ the classes BPk(P) build a proper hierarchy. But we only know that the first step of the hierarchy is proper (Wegener (84 c)).

 THEOREM 6.4 : BP1(P) ⫋ BP2(P) .

 Proof : By Theorem 4.8, (cl on) ̸∈ BP1(P) . We design BP2s of
 polynomial size for cl on . We use the following simple characterization
 of the clique-only function. cl on(x) = 1 iff in G(x), the graph specified

=
###### by x, the degree of each vertex is 0 or n 2 1, and there is some vertex −

= <
###### i[∗] of degree n 2 1 such that all vertices i i[∗] have degree 0 and all −
 vertices of positive degree are connected to i[∗] .

 It is easy to design a BP1 on m variables which has size O(m[2])

 and m + 1 sinks and where all inputs with exactly i ones reach the
 i -th sink (0 ≤ i ≤ m) . Let Tl (1 ≤ l ≤ n) be such a BP1 for all

;
###### variables representing edges (l ·) . The source of T1 is the source of

<
###### the BP2 we construct. For l n, the sink 0 of Tl is the source of Tl +1,

=
###### and the sink n 2 − 1 of Tl is the source of Hl which we define later.
 All other sinks including those of Tn are 0-sinks. If we reach such a
 sink, cl on(x) = 0 . If we reach the source of Hl, we know that the

; : : : ;
###### vertices 1 l 1 are isolated in G(x) and that the vertex l equals −
 the vertex i[∗] in the characterization above. Hl is the concatenation


###### of Hl ;l +1


; : : : ; Hl ;n [. In H]l ;j [we test whether the vertex j has the right]


###### degree and whether it is, if necessary, connected to i[∗] = l . At first we

 ˝compute˝ (similar to the BP1 Tl ) d[∗](j), the number of vertices j[′] ≠ l

; =
###### connected by an edge to the vertex j . If d[∗](j) 0 n 2 2 we reach ̸∈{ − }

;
###### 0-sinks. If d[∗](j) = 0 and the edge (l j) exists (does not exist), we

 reach a 0-sink (the source of Hl ;j+1[) . If d][∗][(j) = n][=][2][ −] [2 and the edge]
 (l ; j) exists (does not exist), we reach the source of Hl ;j+1 [(a 0-sink).]
 If j = n, the source of Hl ;n+1 [is replaced by a 1-sink. The so defined]
 BP computes clon, if n ≥ 6 .


-----

**439**

###### The size of each Tl and Hl ;j [is O(n][2][) . Hence the total size is O(n][4][) .]
 The BP is a read-twice-only BP. Each path leads for some l at most


; : : : ; Hl ;n [. The edge (i][;][ j) is tested]


###### through the BP1s T1


; : : : ; Tl, Hl ;l +1


###### in Ti, if i ≤ l, in Tj, if j ≤ l, in Hl ;i [, if][ l] < i, and in Hl ;j [, if][ l] < j .
 Hence each edge is tested at most twice. 2

 We present a candidate which is in BPk(P) and probably not in BP(k 1)(P) . An edge in an undirected graph is a two-element subset − of the set of vertices. A k-hyperedge in a hypergraph is a k-element vertex set.

 DEFINITION 6.3 : The k-hyperclique-only function k cl on is defined �n� on variables representing the possible k-hyperedges of a hyperk
###### graph. k cl on(x) = 1 iff the hypergraph H(x) specified by the variables

=
###### contains exactly all k-hyperedges on an n 2 vertex set.

 EXERCISES

 1. The number of 1-leaves in a decision tree for f ∈ Bn is not smaller than the number of gates on level 1 in a Σ2-circuit for f .

 2. Let DT(f) be the decision tree complexity of f . Then D(f) ≤ c log(DT(f) + 1) for some constant c .

 3. Estimate the time complexity of the Turing machine we used for the proof of (1.1).

 4. Let f ∈ Bn be not elusive. Let f[′] ∈ Bn be a function differing from f on exactly one input. Then f[′] is elusive.


-----

**440**

###### 5. BP(PARn) = 2n − 1 .

 6. Determine BP1(E[n]k[) and BP1(T][n]k[) exactly.]

 7. The upper bound in Theorem 4.3 ii is optimal. Hint: Consider de Bruijn sequences (see e.g. Knuth (81)) as value vectors.

 8. Prove Theorem 4.4. Hint: Chinese Remainder Theorem.

 9. Design an efficient algorithm for the construction of optimal deci- sion trees for symmetric functions.

 10. Prove a counterpart of Theorem 4.3 for decision trees.

 11. Determine DT(PARn) .

 12. BP1(cl on) = 2[O(n)] .

 13. There is a BP1 for cl n;k where two paths, on which at most k(1)+1 variables are tested positively and at most O(k(0)) variables are tested negatively, lead to the same node.

 14. (Dunne (85), just as 15.). Assume that for f ∈ Bn, all sets

; : : : ;

###### V ⊆{x1 xn} of size bounded by m, and all xi ̸∈ V there

; : : : ; ;

###### is a restriction ρ : {x1 xn} − (V ∪{xi}) →{0 1} such that

; ;
###### fρ(V xi) ∈{xi xi} . Then BP1(f) ≥ 2[m][−][1] − 1 .


###### 15. The BP1-complexity of the Hamiltonian circuit function and the BP1-complexity of the logical permanent are exponential.

 16. Prove an upper bound (as small as possible) on the constant-width BP-complexity of the majority function.


-----

**441**


###### 17. (k cl on) ∈ BPk(P) .


-----

**442**

###### References

Adleman(78): Two theorems on random polynomial time. 19.FOCS,75-83.
Adleman;Booth;Preparata;Ruzzo(78): Improved time and space bounds for Boolean
matrix multiplication. Acta Informatica 11, 61-70.
Ahlswede;Wegener(86): Search problems. Wiley (in press).
Aho;Hopcroft;Ullman(74): The design and analysis of computer algorithms.
Addison-Wesley.
Ajtai(83): Σ[1]1[-formulae on finite structures. Ann.Pure and Appl.Logic 24, 1-48.]
Ajtai;Babai;Hajnal;Koml´os;Pudl´ak;R¨odl;Szemer´edi;Tur´an(86): Two lower bounds
for branching problems. 18.STOC, 30-38.
Ajtai;Ben-Or(84): A theorem on probabilistic constant depth computations.
16.STOC, 471-474.
Ajtai;Koml´os;Szemer´edi(83): An 0(n log n) sorting network. 15. STOC, 1-9.
Alekseev(73): On the number of k-valued monotonic functions. Sov.
Math.Dokl.14,87-91.
Alt(84): Comparison of arithmetic functions with respect to Boolean circuit depth.
16.STOC, 466-470.
Alt;Hagerup;Mehlhorn;Preparata(86): Simulation of idealized parallel computers on
more realistic ones. 12.MFCS, LNCS 233, 199-208.
Alon;Boppana(85): The monotone circuit complexity of Boolean functions.
Preprint.
Anderson;Earle;Goldschmidt;Powers(67): The IBM system/360 model 91: floatingpoint execution unit. IBM J.Res.Dev.11, 34-53.
Andreev(85): On a method for obtaining lower bounds for the complexity of individual monotone functions. Sov.Math.Dokl. 31, 530-534.
Arlazarov;Dinic;Kronrod;Faradzev(70): On economical construction of the transitive closure of a directed graph. Sov.Math.Dokl.11, 1209-1210.
Ashenhurst(57): The decomposition of switching functions. Symp. Theory of
Switching, 74-116.
Ayoub(63): An introduction to the analytical theory of numbers. Amer.Math.Soc.
Balc´azar;Book;Sch¨oning(84): Sparse oracles, lowness and highness. 11.MFCS,
LNCS 176, 185-193.
Barrington(86):Bounded-width polynomial-size branching programs recognize exactly those languages in NC[1]. 18.STOC, 1-5.
Barth(80): Monotone Bilinearformen. TR Univ. Saarbr¨ucken.
Bassalygo(82): Asymptotically optimal switching circuits. Probl.Inf.Transm.17,
206-211.
Batcher(68): Sorting networks and their applications. AFIPS 32, 307-314.
Beame(86a): Limits on the power of concurrent-write parallel machines. 18.STOC,
169-176.
Beame(86b): Lower bounds in parallel machine computation. Ph.D.Thesis, Univ.
Toronto.


-----

**443**

Beame;Cook;Hoover(84): Log depth circuits for division and related problems.
25.FOCS, 1-6.
Bennet;Gill(81): Relative to a random oracle A, P[A] = NP[A] = coNP[A] with proba_̸_ _̸_
bility 1. SIAM J.on Comp.10, 96-113.
Berkowitz(82): On some relationship between monotone and non-monotone circuit
complexity. TR Univ. Toronto.
Best;van Emde Boas;Lenstra(74): A sharpened version of the Aanderaa-Rosenberg
conjecture. TR Univ.Amsterdam.
Bloniarz(79): The complexity of monotone Boolean functions and an algorithm for
finding shortest paths in a graph. Ph.D.Th., MIT.
Blum(84): A Boolean function requiring 3n network size. TCS 28, 337-345.
�
Blum(85): An Ω n[4][=][3][�] lower bound on the monotone network complexity of the
n-th degree convolution. TCS 36, 59-70.
Blum;Seysen(84): Characterization of all optimal networks for a simultaneous computation of AND and NOR. Acta Inform.21, 171-182.
Bollob´as(76): Complete subgraphs are elusive. J.on Comb.Th.21, 1-7.
Bollob´as(78): Extremal graph theory. Academic Press.
Boppana(84): Threshold functions and bounded depth monotone circuits.
16.STOC, 475-479.
Borodin(77): On relating time and space to size and depth. SIAM J.on Comp.6,
733-744.
Borodin;Dolev;Fich;Paul(83): Bounds for width two branching programs. 15.STOC,
87-93.
Brent(70): On the addition of binary numbers. IEEE Trans.on Comp.19, 758-759.
Brent;Kuck;Maruyama(73): The parallel evaluation of arithmetic expressions without division. IEEE Trans.on Comp.22, 532-534.
Brent;Kung(80): The chip complexity of binary arithmetic. 12.STOC, 190-200.
Brown(66): On graphs that do not contain a Thompsen graph. Can.Math.Bull.9,
281-285.
Brustmann;Wegener(86): The complexity of symmetric functions in bounded-depth
circuits. TR Univ.Frankfurt.
Bublitz(86): Decomposition of graphs and monotone formula size of homogeneous
functions. Acta Inform. (in press).
Bublitz;Sch¨urfeld;Voigt;Wegener(86): Properties of complexity measures for
PRAMs and WRAMs. TCS (in press).
Budach(84): A lower bound for the number of nodes in a decision tree. TR
Univ.Berlin (GDR).
Caldwell(64): Der logische Entwurf von Schaltkreisen. Oldenbourg.
Carlson;Savage(83): Size-space tradeoffs for oblivious computations. JCSS 26, 6581.
Chandra;Fortune;Lipton(83): Lower bounds for constant depth circuits for prefix
functions. 10.ICALP, 109-117.


-----

**444**

Chandra;Fortune;Lipton(85): Unbounded fan-in circuits and associative functions.
JCSS 30; 222-234.
Chandra;Furst;Lipton(83): Multiparty protocols. 15.STOC, 94-99.
Chandra;Kozen;Stockmeyer(81): Alternation. JACM 28, 114-133.
Chandra;Stockmeyer;Vishkin(82): A complexity theory for unbounded fan-in parallelism. 23.FOCS, 1-13.
Chandra;Stockmeyer;Vishkin(84): Constant depth reducibility. SIAM J.on
Comp.13, 423-439.
Cobham(66): The recognition problem for the set of perfect squares. 7.SWAT,
78-87.
Commentz-Walter(79): Size-depth tradeoff in monotone Boolean formulae. Acta
Inform.12, 227-243.
Commentz-Walter;Sattler(80): Size-depth tradeoff in non-monotone Boolean formulae. Acta Inform.14, 257-269.
Cook(71): The complexity of theorem proving. 3.STOC, 151-158.
Cook(79): Deterministic CFL’s are accepted simultaneously in polynomial time and
log squared space. 11.STOC, 338-345.
Cook(80): Towards a complexity theory of synchronous parallel computation.
Symp.on Logic and Algorithmic, 75-100.
Cook(83): The classification of problems which have fast parallel algorithms. FCT,
LNCS 158, 78-93.
Cook;Dwork;Reischuk(86): Upper and lower time bounds for parallel random access
machines without simultaneous writes. SIAM J.on Comp. 15, 87-97.
Cook;Hoover(85): A depth-universal circuit. SIAM J.on Comp.14, 833-839.
Cooley;Tukey(65): An algorithm for the machine calculation of complex Fourier
series. Math.Comp.19, 297-301.
Coppersmith;Winograd(82): On the asymptotic complexity of matrix multiplication. SIAM J.on Comp.11, 472-492.
Denenberg;Gurevich;Shelah(83): Cardinalities definable by constant depth polynomial size circuits. TR Univ. Harvard.
Dunne(84): Techniques for the analysis of monotone Boolean networks. Ph.D.Th.,
Univ. Warwick.
Dunne(85): Lower bounds on the complexity of 1-time only branching programs.
FCT, LNCS 199, 90-99.
Edwards(73): The principles of switching circuits. MIT Press.
Ehrenfeucht(72): Practical decidability. TR Univ.of Colorado.
Fagin;Klawe;Pippenger;Stockmeyer(85): Bounded depth, polynomial-size circuits
for symmetric functions. TCS 36, 239-250.
Feller(68): An introduction to probability theory and its applications. Wiley.
Finikov(57): On a family of classes of functions in the logic algebra and their realization in the class of π-schemes. Dokl.Akad.Nauk.115, 247-248.
Fischer(74): Lectures on network complexity. TR Univ. Frankfurt.


-----

**445**

Fischer;Meyer(71): Boolean matrix multiplication and transitive closure. 12.SWAT,
129-131.
Fischer;Meyer;Paterson(82): Ω(n log n) lower bounds on length of Boolean formulas.
SIAM J.on Comp.11, 416-427.
Friedman(84): Constructing O(n log n) size monotone formulae for the k-th elementary symmetric polynomial of n Boolean variables. 25.FOCS, 506-515.
Furst;Saxe;Sipser(84): Parity, circuits and the polynomial time hierarchy.
Math.Syst.Th.17, 13-27.
Gabber;Galil(79): Explicit constructions of linear size superconcentrators.
20.FOCS, 364-370.
Galbiati;Fischer(81): On the complexity of 2-output Boolean networks. TCS 16,
177-185.

Galil;Paul(83): An efficient general purpose parallel computer. JACM 30, 360-387.

Garey;Johnson(79): Computers and intractability: A guide to the theory of NPcompleteness. W.H.Freeman.

Gaskov(78): The depth of Boolean functions. Probl.Kibernet. 34, 265-268.

Gilbert(54): Lattice theoretic properties of frontal switching functions.
J.Math.Phys.33, 57-97.

Glassey;Karp(72): On the optimality of Huffman trees. SIAM J.on Comp.1, 31-39.

Goldschlager(78): A unified approach to models of synchronous parallel machines.
10.STOC, 89-94.

Graham;Rothschild;Spencer(80): Ramsey theory. John Wiley.

Gumm;Poguntke(81): Boolesche Algebra. BI.

Hansel(64): Nombre minimal de contacts de fermeture n´ecessaire pour r´ealiser une
fonction Bool´eenne symm´etriques de n variables. C.R.Acad.Sci.Paris 258,
6037-6040.

Hansel(66): Sur le nombre de fonctions Bool´eennes monotones de n variables.
C.R.Acad.Sci.Paris 262, 1088-1090.

Harper(77): An n log n lower bound on synchronous combinational complexity.
Proc.AMS 64, 300-306.

Harper;Hsieh;Savage(75): A class of Boolean functions with linear combinational
complexity. TCS 1, 161-183.

Harper;Savage(72): On the complexity of the marriage problem. Adv.Math.9, 299312.

Harper;Savage(73): Complexity made simple. Symp.on Comb.Th., 2-15.

Harper;Savage(79): Lower bounds on synchronous combinational complexity. SIAM
J.on Comp.8, 115-119.

Hastad(86): Almost optimal lower bounds for small depth circuits. 18.STOC, 6-20.

Hedtst¨uck(85): Uber die Argumentkomplexit¨at Boolescher Funktionen. Diss. Univ.[¨]
Stuttgart.

Henno(79): The depth of monotone functions in multivalued logic. IPL 8, 176-177.


-----

**446**

Hill;Peterson(81): Switching theory & logical design. John Wiley.
Hodes(70): The logic complexity of geometric properties in the plane. JACM 17,
339-347.
Hodes;Specker(68): Length of formulas and elimination of quantifiers. Contr.to
Math.Logic. North-Holland.
Hoover;Klawe;Pippenger(84): Bounding fan-out in logical networks. JACM 31, 1318.
Hopcroft;Karp(73): An n[5][=][2] algorithm for maximum matching in bipartite graphs.
SIAM J.on Comp.2, 225-231.
Hotz(74): Schaltkreistheorie. de Gruyter.
Hromkovic(85): Linear lower bounds on unbounded fan-in Boolean circuits. IPL 21,
71-74.
Hsieh(74): Intersection theorems for systems of finite vector spaces and other combinatorial results. Ph.D.Th., MIT.
Huppert(67): Finite groups I. Springer.
Johnson;Savage;Welch(72): Combinational complexity measures as a function of
fan-out. TR.
Kahn;Saks;Sturtevant(84): A topological approach to evasiveness. Combinatorica
4, 297-306.
Kannan(82): Circuit-size lower bounds and non-reducibility to sparse sets. IC 55,
40-56.
Karatsuba;Ofman(63): Multiplication of multidigit numbers on automata.
Sov.Phys.Dokl.7, 595-596.
Karnaugh(53): The map method for synthesis of combinational logic circuits. AIEE
Trans.Comm.Elect.72, 593-598.
Karp(72): Reducibility among combinatorial problems. Complexity of computer
computations. Plenum Press. 85-104.
Karp;Lipton(80): Some connections between non uniform and uniform complexity
classes. 12.STOC, 302-309.
Khasin(69): On realizations of monotonic symmetric functions by formulas in the
basis +,,-. Syst.Th.Res.21, 254-259.

_•_
Khasin(70): Complexity bounds for the realization of monotone symmetrical functions by means of formulas in the basis +,,-. Sov.Phys.Dokl.14, 1149-1151.

_•_
Klawe;Paul;Pippenger;Yannakakis(84): On monotone formulae with restricted
depth. 16.STOC, 480-487.
Kleiman;Pippenger(78): An explicit construction of short monotone formulae for
the symmetric functions. TCS 7, 325-332.
Klein;Paterson(80): Asymptotically optimal circuit for a storage access function.
IEEE Trans.of Comp.29, 737-738.
Kleitman(69): On Dedekind’s problem: The number of monotone Boolean functions.
Proc.AMS 21, 677-682.
Kleitman(73): The number of Sperner families of subsets of an n element set. Colloq.Math.Soc. J´anos Bolyai 10, 989-1001.


-----

**447**

Kleitman;Kwiatkowski(80): Further results on the Aanderaa-Rosenberg conjecture.
J.on Comb.Th.(B) 28, 85-95.
Kleitman;Markowsky(75): On Dedekind’s problem: the number of isotone Boolean
functions II. Trans.AMS 213, 373-390.
Kloss(66): Estimates of the complexity of solutions of systems of linear equations.
Sov.Math.Dokl.7, 1537-1540.
Kloss;Malyshev(65): Estimates of the complexity of certain classes of functions.
Vestn.Moskov.Univ.Ser.1 4, 44-51.
Knuth(81): The art of computer programming. Addison Wesley.
Ko;Sch¨oning(85): On circuit-size complexity and the low hierarchy in NP. SIAM
J.on Comp.14, 41-51.
Korobkov(56): The realization of symmetric functions in the class of π-schemes.
Dokl.Akad.Nauk.109, 260-263.
Korshunov(77): The solution to a problem of Dedekind on the number of monotone
Boolean functions. Dokl.Akad.Nauk.233, 543-546.
Korshunov(81a): On the number of monotone Boolean functions. Probl.Kibern.38,
5-108.
Korshunov(81b): On the complexity of the shortest disjunctive normal forms of
Boolean functions. Met.Diskr.Anal.37, 9-41.
Kovari;S´os;Tur´an(54): On a problem of K. Zarankiewicz. Coll.Math. 3, 50-57.
Kramer;van Leeuwen(82): The complexity of VLSI circuits for arbitrary Boolean
functions. TR Univ. Utrecht.
Krapchenko(70): Asymptotic estimation of addition time of parallel adder.
Syst.Th.Res.19, 105-122.
Krapchenko(71): Complexity of the realization of a linear function in the class of
_π-circuits. Math.Notes Acad.Sci.USSR 10, 21-23._
Krapchenko(72a): The complexity of the realization of symmetrical functions by
formulae. Math.Notes.Acad.Sci.USSR 11, 70-76.
Krapchenko(72b): A method of obtaining lower bounds for the complexity of πschemes. Math.Notes Acad.Sci.USSR 11, 474-479.
Krichevskii(64): Complexity of contact circuits realizing a function of logical algebra.
Sov.Phys.Dokl.8, 770-772.
Kriegel;Waack(86): Lower bounds on the complexity of real-time branching programs. TR AdW Berlin (GDR).
Kucera(82): Parallel computation and conflicts in memory access. IPL 14, 93-96.
Kuznetsov(83a): On the complexity of the realization of a sequence of Boolean
functions by formulas of depth 3 in the basis ; &; . Ver.Met.Kibern.19,
_{∨_ _−}_
40-43.
Kuznetsov(83b): On the lower estimate of the length of the shortest disjunctive
normal form for almost all Boolean functions. Ver.Met. Kibern.19, 44-47.
Ladner;Fischer(80): Parallel prefix computation. JACM 27, 831-838.
Lamagna(75): The complexity of monotone functions. Ph.D.Th., Brown Univ.


-----

**448**

Lamagna(79): The complexity of monotone networks for certain bilinear forms,
routing problems, sorting and merging. IEEE Trans.on Comp.28, 773-782.
Lamagna;Savage(73): On the logical complexity of symmetric switching functions
in monotone and complete bases. TR Brown Univ.
Lamagna;Savage(74): Combinational complexity of some monotone functions.
15.SWAT, 140-144.
Lee(78): Modern switching theory and digital design. Prentice Hall.
Lipton;Tarjan(79): A separator theorem for planar graphs. SIAM J.on
Appl.Math.36, 177-189.
Lipton;Tarjan(80): Applications of a planar separator theorem. SIAM J.on Comp.9,
615-627.
Lotti;Romani(80): Application of approximating algorithms to Boolean matrix multiplication. IEEE Trans.on Comp.29, 927-928.
Lupanov(58): A method of circuit synthesis. Izv.VUZ Radiofiz 1, 120-140.
Lupanov(61): Implementing the algebra of logic functions in terms of bounded depth
formulas in the basis &; ; . Sov.Phys.Dokl.6, 107-108.
_∨_ _−_
Lupanov(62a): On the principle of local coding and the realization of functions of certain classes of networks composed of functional elements.
Sov.Phys.Dokl.6, 750-752.
Lupanov(62b): Complexity of formula realization of functions of logical algebra.
Probl.Kibern.3, 782-811.
Lupanov(65a): On the realization of functions of logical algebra by formulae of finite
classes (formulae of limited depth) in the basis ; +; . Probl.Kibern.6, 1-14.
_•_ _−_
Lupanov(65b): A method of synthesis of control systems - the principle of local
coding. Probl.Kibern.14, 31-110.
Lupanov(70): On circuits of functional elements with delay. Probl.Kibern.23, 43-81.
Mac Lane;Birkhoff(67): Algebra. Mac Millan.
Margulis(75): Explicit construction of concentrators. Probl.of Inform.Transm.,
Plenum Press.
Masek(76): A fast algorithm for the string editing problem and decision graph
complexity. M.Sc.Th. MIT.
McCluskey(56): Minimization of Boolean functions. Bell Syst.Techn.J.35, 14171444.
McColl(76): Some results on circuit depth. Ph.D.Th., Univ. Warwick.
McColl(78a): Complexity hierarchies for Boolean functions. Acta Inform.11, 71-77.
McColl(78b): The maximum depth of monotone formulae. IPL 7, 65.
McColl(78c): The circuit depth of symmetric Boolean funtions. JCSS 17, 108-115.
McColl(81): Planar crossovers. IEEE Trans.on Comp.30, 223-225.
McColl(85a): On the planar monotone computation of threshold functions.
2.STACS, LNCS 182, 219-230.
McColl(85b): Planar circuits have short specifications. 2.STACS, LNCS 182, 231242.


-----

**449**

McColl;Paterson(77): The depth of all Boolean functions. SIAM J.on Comp.6, 373380.

McColl;Paterson(84): The planar realization of Boolean functions. TR Univ. Warwick.

McKenzie;Cook(84): The parallel complexity of some Abelian permutation group.
TR Univ. Toronto.

Mead;Conway(80): Introduction to VLSI systems. Addison Wesley.

Mead;Rem(79): Cost and performance of VLSI computing structures. IEEE J.Solid
State Circuits 14, 455-462.

Mehlhorn(77): Effiziente Algorithmen. Teubner.

Mehlhorn(79): Some remarks on Boolean sums. Acta Inform.12, 371-375.

Mehlhorn;Galil(76): Monotone switching circuits and Boolean matrix product.
Computing 16, 99-111.

Mehlhorn;Preparata(83): Area-time optimal VLSI integer multiplier with minimum
computation time. IC 58, 137-156.

Mehlhorn;Vishkin(84): Randomized and deterministic simulations of PRAMs by
parallel machines with restricted granularity of parallel memories. Acta
Inform.21, 339-374.

Mendelson(82): Boolesche Algebra und logische Schaltungen. McGraw-Hill.

Meyer;Stockmeyer(72): The equivalence problem for regular expressions with squaring requires exponential time. 13.SWAT, 125-129.
Meyer auf der Heide(84): A polynomial linear search algorithm for the n-dimensional
knapsack problem. JACM 31, 668-676.
Meyer auf der Heide(86): Efficient simulations among several models of parallel
computers. SIAM J.on Comp.15, 106-119.
Mileto;Putzolu(64): Average values of quantities appearing in Boolean function minimization. IEEE Trans.El.Comp.13, 87-92.
Mileto;Putzolu(65): Statistical complexity of algorithms for Boolean function minimization. JACM 12, 364-375.
Miller,R.E.(79): Switching theory. Robert E.Krieger Publ.Comp.
Miller,W.(75): Computer search for numerical instability. JACM 22, 512-521.
Muller;Preparata(75): Bounds to complexities of networks for sorting and switching.
JACM 22, 195-201.
Muller;Preparata(76): Restructing of arithmetic expressions for parallel evaluation.
JACM 23, 534-543.
Muroga(79): Logic design and switching theory. John Wiley.
Nechiporuk(66): A Boolean function. Sov.Math.Dokl.7, 999-1000.
Nechiporuk(71): On a Boolean matrix. Syst.Th.Res.21, 236-239.
Nigmatullin(67a): Certain metric relations in the unit cube. Discr.Anal.9, 47-58.
Nigmatullin(67b): A variational principle in an algebra of logic. Discr.Anal.10,
69-89.


-----

**450**

Nurmeev(81): On circuit complexity of the realization of almost all monotone
Boolean functions. Iz.VUZ Mat.25, 64-70.
Oberschelp(84): Fast parallel algorithms for finding all prime implicants for discrete
functions. LNCS 171, 408-420.
Ofman(63): On the algorithmic complexity of discrete functions. Sov.Phys.Dokl.7,
589-591.
Okol’nishnikova(82): On the influence of negations on the complexity of a realization of monotone Boolean functions by formulas of bounded depth.
Met.Diskr.Anal.38, 74-80.
Pan(84): How can we speed up matrix multiplication? SIAM Rev.26, 393-415.
Paterson(73): New bounds on formula size. 3.TCS-GI, 17-26.
Paterson(75): Complexity of monotone networks for Boolean matrix product. TCS
1, 13-20.
Paterson(76): An introduction to Boolean function complexity. Ast´erisque 38-39,
183-201.
Paterson(83): An improved depth 0(log n) comparator network for sorting. Oberwolfach Conf.on Compl.Th.
Paterson;Hewitt(80): Comparative schematology. Proj.MAC Conf.on
Conc.Syst.and Par.Comp., 119-127.
Paterson;Valiant(76): Circuit size is nonlinear in depth. TCS 2, 397-400.
Paterson;Wegener(86): Nearly optimal hierarchies for network and formula size.
Acta Inform.23, 217-221.
Paul(75): Boolesche Minimalpolynome und Uberdeckungsprobleme. Acta Inform.4,[¨]
321-336.
Paul(76): Realizing Boolean functions on disjoint sets of variables. TCS 2, 383-396.
Paul(77): A 2:5 n lower bound on the combinational complexity of Boolean functions. SIAM J.on Comp.6, 427-443.
Paul(78): Komplexit¨atstheorie. Teubner.
Picard(65): Th´eorie des questionnaires. Gauthier-Villars.
Pippenger(76): The realization of monotone Boolean functions. 8. STOC, 204-210.
Pippenger(77a): Superconcentrators. SIAM J.on Comp.6, 298-304.
Pippenger(77b): Fast simulation of combinatorial logic networks by machines without random-access storage. 15.Allerton Conf.on Comm.,Contr.and Comp.
Pippenger(77c): On another Boolean matrix. TR IBM Yorktown Heights.
Pippenger(78): The complexity of monotone Boolean functions. Math.Syst.Th.11,
289-316.
Pippenger(79): On simultaneous resource bounds. 20.FOCS, 307-311.
Pippenger;Fischer (73): Relations among complexity measures. TR IBM Yorktown
Heights.
Pippenger;Fischer(79): Relations among complexity measures. JACM 26, 361-381.
Pippenger;Valiant(76): Shifting graphs and their applications. JACM 23, 423-432.


-----

**451**

Pratt(75a): The power of negative thinking in multiplying Boolean matrices. SIAM
J.on Comp.4, 326-330.
Pratt(75b): The effect of basis on size of Boolean expressions. 16.FOCS, 119-121.
Preparata;Muller(71): On the delay required to realize Boolean functions. IEEE
Trans.on Comp.20, 459-461.
Preparata;Muller(76): Efficient parallel evaluation of Boolean expressions. IEEE
Trans.on Comp.25, 548-549.
Pudl´ak(83): Boolean complexity and Ramsey theorems. TR Univ. Prague.
Pudl´ak(84a): Bounds for Hodes-Specker theorem. LNCS 171, 421-445.
Pudl´ak(84b): A lower bound on complexity of branching programs. 11.MFCS,
LNCS 176, 480-489.
Pudl´ak;Z´ak(83): Space complexity of computations. TR Univ. Prague.[ˇ]
Quine(52): The problem of simplifying truth functions. Am.Math.Soc.61, 521-531.
Quine(53): Two theorems about truth functions. Bol.Soc.Math.Mex.10, 64-70.
Quine(55): A way to simplify truth functions. Am.Math.Monthly 62, 627-631.
Razborov(85a): A lower bound on the monotone network complexity of the logical
permanent. Matemat.Zametki 37, 887-900.
Razborov(85b): Lower bounds on the monotone complexity of some Boolean functions. Dokl.Akad.Nauk.281, 798-801.
Razborov(86): Lower bounds on the size of bounded-depth networks over the basis
; . Preprint.
_{∧_ _⊕}_
Red’kin(73): Proof of minimality of circuits consisting of functional elements.
Syst.Th.Res.23, 85-103.
Red’kin(79): On the realization of monotone Boolean functions by contact circuits.
Probl.Kibern.35, 87-110.
Red’kin(81): Minimal realization of a binary adder. Probl.Kibern.38, 181-216,272.
Reif(83): Logarithmic depth circuits for algebraic functions. 24.FOCS, 138-145.
Reznik(62): The realization of monotonic functions by means of networks consisting
of functional elements. Sov.Phys.Dokl.6, 558-561.
Riordan;Shannon(42): The number of two-terminal series-parallel networks. J.on
Math.Phys.21, 83-93.
Rivest;Vuillemin(76): On recognizing graph properties from adjacency matrices.
TCS 3, 371-384.
Runge;K¨onig(24): Die Grundlehre der mathematischen Wissenschaften 11.
Springer.
Ruzzo(81): On uniform circuit complexity. JCSS 22, 365-383.
Sattler(81): Netzwerke zur simultanen Berechnung Boolescher Funktionen. 5.TCSGI, LNCS 104, 32-40.
Savage(72): Computational work and time on finite machines. JACM 19, 660-674.
Savage(74): An algorithm for the computation of linear forms. SIAM J.on Comp.3,
150-158.
Savage(76): The complexity of computing. John Wiley.


-----

**452**

Savage(81): Planar circuit complexity and the performance of VLSI algorithms.
VLSI Syst.and Comp., Comp.Sc.Press.
Savage(82): Bounds on the performance of multilective VLSI algorithms. TR Brown
Univ.
Scarpellini(85): Complex Boolean functions obtained by diagonalization. TCS 36,
119-126.
Schnorr(74): Zwei lineare untere Schranken f¨ur die Komplexit¨at Boolescher Funktionen. Computing 13, 155-171.
Schnorr(76a): The network complexity and the Turing machine complexity of finite
functions. Acta Inform.7, 95-107.
Schnorr(76b): The combinational complexity of equivalence. TCS 1, 289-295.
Schnorr(76c): A lower bound on the number of additions in monotone computations.
TCS 2, 305-315.
Schnorr(77): The network complexity and the breadth of Boolean functions.
Stud.Logic Found.Math.87, 491-504.
Schnorr(80): A 3-n lower bound on the network complexity of Boolean functions.
TCS 10, 83-92.
Sch¨onhage;Strassen(71): Schnelle Multiplikation großer Zahlen. Computing 7, 281292.
Sch¨oning(83): A low and a high hierarchy within NP. JCSS 27, 14-28.
Sch¨oning(84): On small generators. TCS 34, 337-341.
Sch¨urfeld(83): New lower bounds on the formula size of Boolean functions. Acta
Inform.19, 183-194.
Sch¨urfeld;Wegener(86): On the CREW PRAM complexity of Boolean functions.
Parallel Computing 85, Eds.Feilmeier, Joubert, Schendel; Elsevier Publ.,
247-252.
Shannon(38): A symbolic analysis of relay and switching circuits. Trans.AIEE 57,
713-723.
Shannon(49): The synthesis of two-terminal switching circuits. Bell Syst.Techn.J.28,
59-98.
Simon,H.U.(83): A tight Ω(log log n) bound on the time for parallel RAM’s to compute nondegenerate Boolean functions. FCT, LNCS 158, 439-444.
Simon,J.(77): Physical limits on the speed of computing. TR Univ. Campinas.
Sipser(83): Borel sets and circuit complexity. 15. STOC, 61-69.
Sklansky(60a): An evaluation of several two-sum and binary adders. IRE
Trans.Elect.Comp.9, 213-226.
Sklansky(60b): Conditional-sum addition logic. IRE Trans.Elect.Comp. 9, 226-231.
Skyum(83): A measure in which Boolean negation is exponentially powerful. IPL
17, 125-128.
Skyum;Valiant(85): A complexity theory based on Boolean algebra. JACM 32,
484-502.
Soprunenko(65): Minimal realizations of functions by circuits using functional elements. Probl.Kibern.15, 117-134.


-----

**453**

Spaniol(76): Arithmetik in Rechenanlagen. Teubner.
Specker;Strassen(76): Komplexit¨at von Entscheidungsproblemen. LNCS 43.
Spira(71a): On time-hardware complexity tradeoffs for Boolean functions. 4.Hawaii
Symp.on Syst.Sc., 525-527.
Spira(71b): On the time necessary to compute switching functions. IEEE Trans.on
Comp.20, 104-105.
Stockmeyer(74): The complexity of decision problems in automata and logic. TR
MIT.
Stockmeyer(76): The polynomial-time hierarchy. TCS 3, 1-22.
Stockmeyer(77): On the combinational complexity of certain symmetric Boolean
functions. Math.Syst.Th.10, 323-326.
Stockmeyer(83): The complexity of approximate counting. 15.STOC, 118-126.
Stockmeyer;Vishkin(84): Simulation of parallel random access machines by circuits.
SIAM J.on Comp.13, 409-422.
Strassen(69): Gaussian elimination is not optimal. Num.Math.13, 354-356.
Strassen(86): Relative bilinear complexity and matrix multiplication. TR Univ.
Z¨urich.
Tarjan(78): Complexity of monotone networks for computing conjunctions.
Ann.Discr.Math.2, 121-133.
Thompson(79): Area time complexity for VLSI. 11.STOC, 81-88.
Thompson(80): A complexity theory for VLSI. Ph.D.Th., Carnegie-Mellon Univ.
Tiekenheinrich(83): Verallgemeinerungen des Tiefenhierarchiesatzes f¨ur Boolesche
Funktionen. Dipl.arb. Univ. Bielefeld.
Tiekenheinrich(84): A 4n-lower bound on the monotone network complexity of a
one-output Boolean function. IPL 18, 201-202.
Tkachev(80): On the complexity of realizations of a sequence of Boolean functions
by Boolean circuits and π-schemes under some additional restrictions on the
construction of the schemes. Comb.and Alg.Meth.in Appl.Math., 161-207.
Tur´an(84): The critical complexity of graph properties, IPL 18, 151-153.
Ugolnikov(76): On the realizations of monotone functions by circuits of functional
elements. Probl.Kibern.31, 167-185.
Uhlig(74): On the synthesis of self-correcting schemes from functional elements with
a small number of reliable elements. Math.Notes Acad.Sci.USSR 15, 558562.
Uhlig(84): Zur Parallelberechnung Boolescher Funktionen. TR Ing.hochsch. Mittweida.
Ullman(84): Computational aspects of VLSI. Comp.Sc.Press.
Valiant(76a): Graph-theoretic properties in computational complexity. JCSS 13,
278-285.
Valiant(76b): Universal circuits. 8.STOC, 196-203.
Valiant(79): Completeness classes in algebra. 11.STOC, 249-261.
Valiant(80): Negation can be exponentially powerful. TCS 12, 303-314.


-----

**454**

Valiant(83): Exponential lower bounds for restricted monotone circuits. 15.STOC,
110-117.
Valiant(84): Short monotone formulae for the majority function. J.of Algorithms 5,
363-366.
Valiant(86): Negation is powerless for Boolean slice functions. SIAM J.on Comp.15,
531-535.
van Leeuwen(83): Parallel computers and algorithms. Coll.on Par.Comp.and Alg.
van Voorhis(72): An improved lower bound for sorting networks. IEEE Trans.on
Comp.21, 612-613.
Veitch(52): A chart method for simplifying truth functions. Proc.Ass. Comput.Mach., 127-133.
Vilfan(72): The complexity of finite functions. Ph.D.Th., MIT.
Vishkin;Wigderson(85): Trade-offs between depth and width in parallel computation. SIAM J.on Comp.14, 303-314.
Vuillemin(83): A combinatorial limit to the computing power of VLSI circuits. IEEE
Trans.on Comp.32, 294-300.
Wallace(64): A suggestion for a fast multiplier. IEEE Trans.on Comp.13, 14-17.
Wegener(79a): Switching functions whose monotone complexity is nearly quadratic.
TCS 9, 83-97.
Wegener(79b): A counterexample to a conjecture of Schnorr referring to monotone
networks. TCS 9, 147-150.
Wegener(80): A new lower bound on the monotone network complexity of Boolean
sums. Acta Inform.13, 109-114.
Wegener(81): An improved complexity hierarchy on the depth of Boolean functions.
Acta Inform.15, 147-152.
Wegener(82a): Boolean functions whose monotone complexity is of size n[2] = log n.

TCS 21, 213-224.
Wegener(82b): Best possible asymptotic bounds on the depth of monotone functions
in multivalued logic. IPL 15, 81-83.
Wegener(83): Relating monotone formula size and monotone depth of Boolean functions. IPL 16, 41-42.
Wegener(84a): Proving lower bounds on the monotone complexity of Boolean functions. LNCS 171, 446-456.
Wegener(84b): Optimal decision trees and one-time-only branching programs for
symmetric Boolean functions. IC 62, 129-143.
Wegener(84c): On the complexity of branching programs and decision trees for
clique functions. TR Univ. Frankfurt.
Wegener(85a): On the complexity of slice functions. TCS 38, 55-68.
Wegener(85b): The critical complexity of all (monotone) Boolean functions and
monotone graph properties. IC 67, 212-222.
Wegener(86a): Time-space trade-offs for branching programs. JCSS 32, 91-96.
Wegener(86b): More on the complexity of slice functions. TCS 43, 201-211.


-----

**455**

�
Weiß(83): An Ω n[3][=][2][�] lower bound on the monotone complexity of Boolean convolution. IC 59, 184-188.
Weyh(72): Elemente der Schaltungsalgebra. Oldenbourg.
Wilson(83): Relativized circuit complexity. 24.FOCS, 329-334.
Wippersteg(82): Einige Ergebnisse f¨ur synchrone Schaltkreise. Dipl.arb. Univ.
Bielefeld.
Yablonskii(57): On the impossibility of eliminating trial of all functions from P2 in
solving some problems on circuit theory. Dokl.Akad.Nauk.USSR 124, 44-47.
Yao(83): Lower bounds by probabilistic arguments. 24.FOCS, 420-428.
Yao(85): Separating the polynomial-time hierarchy by oracles. 26.FOCS, 1-10.
Yap(83): Some consequences of non-uniform conditions of uniform classes. TCS 26,
287-300.
Z´ak(84): An exponential lower bound for one-time-only branching programs.
11.MFCS, LNCS 176, 562-566.

FCT - Fundamentals of Computation Theory
FOCS - Symp. on Foundations of Computer Science
IC - Information and Control
ICALP - Int.Colloquium on Automata, Languages and Programming
IPL - Information Processing Letters
JACM - Journal of the Association for Computing Machinery
JCSS - Journal of Computer and System Sciences
LNCS - Lecture Notes in Computer Science
MFCS - Mathematical Foundations of Computer Science
STACS - Symp. on Theoretical Aspects of Computer Science
STOC - Symp. on Theory of Computing
SWAT - Symp. on Switching and Automata Theory
TCS - Theoretical Computer Science
TCS-GI - GI Conf. Theoretical Computer Science
TR - Technical Report


-----

**456**

**Index**

**addition 7,39,124,313,322,341,348**
affine function 251
Ajtai,Kom[´]los and Szeme´redi sorting
network 152
almost all 87
arithmetic circuit 64
Ashenhurst decomposition 304

**basis 7**
Batcher sorting network 149
bilinear function 169
bipartite matching 310
Boolean convolution 58,168,209,350
Boolean matrix product 78,107,170,350
Boolean sum 36,107,163,213
BPP 286
branching program 414

**canonical slice 203**
carry function 39,226,341
carry-look-ahead-adder 83
carry save adder 51
cell partition 388
central slice 204
Chinese Remainder Theorem 61
circuit 7
circuit size 9
circuit value problem 310
clause 36
clique function 107,184,189,192,203,
204,257,270,384,421,422,427,436
clique-only function 430,438
communication width 363
comparison function 143,322
complete basis 9
conditional sum adder 40
configuration 278
conjunctive normal form 5
connectivity 85,309
constant depth reducibility 312
counting function 74,123,127,252,314
CO WRAM 363
CRCW PRAM 363
CREW PRAM 362
critical complexity 379

**data rate 348**
de Morgan laws 4
decision tree 419


decoding circuit 90
depth 9
determinant 81,256,262,343,422
direct product 301
Discrete Fourier Transform 63
disjoint bilinear form 215
disjunctive normal form 5
division 67,308
dual function 148

**elimination method 121**
elusive function 418
equality test 126
EREW PRAM 362
essential dependence 19,120
Eulerian cycle 309
evasive function 418
exactly - k - function 74,426
explicitly defined function 119,139
exponential growth 17
EXP TAPE HARD 139

**f** an-in 11
fan-out 10
Fast Fourier Transform 62
Fischer, Meyer and Paterson method
251
formula 12
formula size 12

**gate 7**
generating circuit 283
graded set of Boolean functions 389
graph property 402

**Hamiltonian circuit 217,426**
hierarchy 296,337,394,436
(h; k)-disjoint Boolean sum 163
Hodes and Specker method 249
homogeneous function 107
Horner scheme 227

**implicant 24**

**Karnaugh diagram 30**
Krapchenko method 258
(k; s) - Lupanov representation 91

**Las Vegas algorithm 286**
logical level 23,320


-----

logical permanent 193,426

**majority function 154,243,312,313,**
333,426,436
marriage problem 102
mass production 301
maxterm 5
merging function 149,151,158,322
minimal polynomial 23
minterm 5
monom 23
monotone basis 145
monotone circuit 145
monotone disjunctive normal form 32
monotone function 3
monotone representation 197
monotone storage access function 399
Monte Carlo algorithm 285
multiplication 51,226,308,313,350

**NC - Nick’s class 292**
NC1 reducibility 307
Nechiporuk method 253,421
negative envelope of convolution 58
network flow problem 310
non degenerated function 19,120
non deterministic Turing machine 269
non uniform computation model 19,
279,363,414
NP 33,269
NP - completeness 33,184,203,270,288

**oblivious Turing machine 271**
odd-even merge 149
1 - fan-in 326
oracle 270,307

**P 269**
parity function 36,125,261,312,313,324
380,387
partially defined function 22
perfect matching 193,426
period 348
permutation branching program 434
Πk-circuit 320
planar circuit 344
polynomial 23
polynomial growth 17
P = Poly 283
prefix problem 48
prime clause 36


**457**

prime implicant 24
probabilistic computation model 285,
352
processor partition 388
programmable circuit 110
projection reducibility 146,309
pseudo complement 195

**quadratic function 107**
Quine and McCluskey algorithm 25

**radix - 4 -representation 54**
random restriction 326
read-once-only branching program
423
replacement rule 160
ring sum expansion 6
root of identity 62

**satisfiability problem 270,289**
Sch¨onhage and Strassen algorithm 56
selection function 20,218
self reducibility 289
semi-disjoint bilinear form 169
sensitive complexity 374
set circuit 208
set cover problem 33
Shannon effect 88
Shannon’s counting argument 87
Σk-circuit 320
single level 236
size 9
SIZE - DEPTH(poly; const) 312
slice function 195
sorting function 148,158,313
sorting network 74,148
space complexity 269
Stockmeyer hierarchy 270
storage access function 76,123,374,420
storage access function for indirect
addressing 255,422
Strassen algorithm 79
strong connectivity 310
subtraction 50
symmetric function 74
synchronous circuit 340

**table of prime implicants 27**
threshold function 74,107,127,148,154,
196,235,239,243,250,313,323,357,422


-----

**458**

time complexity 269
trade-off 225
transitive function 349
Turing machine 268

**uniform computation models 267,292**
universal circuit 110
universal gate 112
universal graph 112

**value function 176**
value vector 74
variational principle 106
VLSI 226,347

**weak Shannon effect 106**
width of a branching program 417
WRAM 363


-----

