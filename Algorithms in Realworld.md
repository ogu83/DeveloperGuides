Algorithms in the Real World:

Lecture Notes (Fall  )

Guy Blello ch

April ,  

Abstract

This do cument contains the lecture notes taken by the students in the course \Al
gorithms in the Real World" taught at UC Berkeley during the Fall semester,  .

The class covered the following set of ten topics: Compression, Cryptography, Linear

Programming, Integer Programming, Triangulation, N-b o dy simulation, VLSI Physi
cal Design, Pattern Matching in Biology, Indexing, and Clustering. Between  and 

lectures were dedicated to each topic. For all topics we lo oked b oth at algorithms and

at case studies in which the problems are used in real-world applications. The class

was a graduate class and assumed that the students came in with a working knowledge

of the material covered in a standard algorithms textb o ok, such as Cormen, Leiserson

and Rivest's \Intro duction to Algorithms". A goal of the class was to have the stu
dents gain an appreciation of how interesting algorithms and data-structures are used

in many real-world applications.

The notes contained in this do cument are based on what was covered in the lectures

and are not meant to b e complete, and although the scrib e takers corrected many of

the mistakes in my lectures, I exp ect many others got through. I must also ap ologize

that the notes contain very few references to the original work on which they rely.

Instead I have included at the end of the do cument a list of primary texts on the topics

from which one can �nd further information. Also, there is a web page asso ciated with

the class that has many more online p ointers

http://www.cs.berkeley.edu/~guyb/algs.html.

I would like to thank all the students who to ok the notes that app ear in this

do cument. They did an excellent job and in many cases went far b eyond the call of

duty in p olishing them and generating �gures.


-----

Contents

List of Algorithms 

Compression  (Ben Zhao) 

 Intro duction to Compression 

. Information Theory : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. The English Language : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Basic Compression Algorithms 

. Pre�x Co des : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Hu�man Co des : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Shannon-Fano Co ding : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Arithmetic Co ding : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Deriving Probabilities : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Lemp el-Ziv Overview 

. LZ and LZW : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. LZ (Sliding Windows) : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Compression  (Gabriel Moy) 

 Lossless Compression: review and expansion 

. Can we compress all strings? : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Hu�man Co des Revisited : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Arithmetic Co ding Revisited : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Conditional Entropy and Markov Chains : : : : : : : : : : : : : : : : : : : : 

. The JBIG Standard : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Tries and use in LZW : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Other Lossless Compression Techniques : : : : : : : : : : : : : : : : : : : : : 

 Lossy Compression 

. Scalar Quantization : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Vector Quantization : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. Transform Co ding : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. Cho osing a Transform : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Compression  (Ben Liblit) 


-----

 Case Studies 

. JPEG : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. MPEG : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Other Lossy Transform Co des 

. Wavelet Compression : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Fractal Compression : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Mo del-Based Compression : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

Cryptography  (Tzu-Yi Chen) 

 De�nitions and Primitives 

. De�nitions : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Primitives : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Proto cols 

. Digital Signatures : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Key Exchange : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Authentication : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Some Other Proto cols : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Symmetric (private-key) Algorithms 

. Symmetric Ciphers (Blo ck Ciphers) : : : : : : : : : : : : : : : : : : : : : : : 

. DES (Data Encryption Standard) : : : : : : : : : : : : : : : : : : : : : : : : 

Cryptography  (David Opp enheimer) 

 Blo ck ciphers 

. Feistel networks : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Security and Blo ck Cipher Design Goals : : : : : : : : : : : : : : : : : : : : 

. DES Security : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Di�erential Cryptanalysis : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Linear Cryptanalysis : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. IDEA : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Blo ck Cipher Encryption Sp eeds : : : : : : : : : : : : : : : : : : : : : : : : : 

 Stream ciphers 

. Stream ciphers vs. Blo ck cipher : : : : : : : : : : : : : : : : : : : : : : : : : 

. RC : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Public-Key Algorithms 

. Merkle-Hellman Knapsack Algorithm : : : : : : : : : : : : : : : : : : : : : : 

. RSA : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0


-----

Cryptography  (Marat Boshernitsan) 

 Some group theory 

. Groups: Basics : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Integers mo dulo n : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Generators (primitive elements) : : : : : : : : : : : : : : : : : : : : : : : : : 

. Discrete logarithms : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Public Key Algorithms (continued) 

. RSA algorithm (continued) : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Factoring : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. ElGamal Algorithm : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Probabilistic Encryption 

. Generation Random Bits : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Blum-Goldwasser : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Quantum Cryptography 

 Kerb eros (A case study) 

. How Kerb eros Works : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Tickets and Authenticators : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Kerb eros messages : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Linear Programming  (Richard C. Davis) 0

 Intro duction 0

. Some Optimization Problems : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. Applications of Linear Programming : : : : : : : : : : : : : : : : : : : : : : 

. Overview of Algorithms : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Linear Programming Formulation : : : : : : : : : : : : : : : : : : : : : : : : 

. Using Linear Programming for Maximum-Flow : : : : : : : : : : : : : : : : : 

 Geometric Interpretation 

 Simplex Metho d 

. Tableau Metho d : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Finding an Initial Corner Point : : : : : : : : : : : : : : : : : : : : : : : : : 

. Another View of the Tableau : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Improvements to Simplex : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Linear Programming  (Steven Czerwinski) 


-----

 Duality 

. Duality: General Case : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Example : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Duality Theorem : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Ellipsoid Algorithm 

. Description of algorithm : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Reduction from general case : : : : : : : : : : : : : : : : : : : : : : : : : : :

 Interior Point Metho ds

. Centering : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 00

. Optimizing techniques : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. A�ne scaling metho d : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. Potential reduction : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. Central tra jectory : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

 Algorithm summary 0

 General Observation 0

Integer Programming  (Andrew Begel) 0

 Intro duction and History 0

 Applications 0

. Knapsack Problem : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. Traveling Salesman Problem : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. Other Constraints Expressible with Integer Programming : : : : : : : : : : : 

. Piecewise Linear Functions : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Algorithms 

. Linear Programming Approximations : : : : : : : : : : : : : : : : : : : : : : 

. Search Techniques : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Implicit Enumeration (0- Programs) : : : : : : : : : : : : : : : : : : : : : : 

Integer Programming  (Stephen Chenney) 

 Algorithms (continued) 

. Problem Sp eci�c Asp ects : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Cutting Plane Algorithm : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Recent Developments : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 


-----

 Airline Crew Scheduling (A Case Study) 

. The Problem : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Set Covering and Partitioning : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Generating Crew Pairings : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. TRIP : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. New System : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Triangulation  (Aaron Brown) 

 Intro duction to Triangulation 

 Basic Geometrical Op erations 

. Degeneracies and Numerical Precision : : : : : : : : : : : : : : : : : : : : : : 

. The Line-side Test : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. The In-circle Test : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Convex Hulls 

. Dual: Convex Polytop es : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Algorithms for Finding Convex Hulls : : : : : : : : : : : : : : : : : : : : : : 

 Delaunay Triangulations and Voronoi Diagrams 

. Voronoi Diagrams : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Delaunay Triangulations : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Prop erties of Delaunay Triangulations : : : : : : : : : : : : : : : : : : : : : 

. Algorithms for Delaunay Triangulation : : : : : : : : : : : : : : : : : : : : : 

Triangulation  (Franklin Cho) 

 Divide-and-Conquer Delaunay Triangulation 

 Incremental Delaunay Triangulation Algorithm 

 Mesh Generation 

. Rupp ert's Algorithm : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

Triangulation  (Michael Downes) 

 Triangulation in Finite Element Metho ds (Mark Adams) 

. FEM Intro : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Approximating the Weak Form with Subspaces : : : : : : : : : : : : : : : : 

. Picking Go o d Subspaces : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Linear System Solvers : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Multigrid : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 


-----

. Unstructured Multigrid Algorithms : : : : : : : : : : : : : : : : : : : : : : : 

. Parallel Multigrid Solver for FE : : : : : : : : : : : : : : : : : : : : : : : : : 0

 Distance Metrics for Voronoi Diagrams and Delaunay Triangulations 

 Surface Mo deling Using Triangulation 

. Terrain Mo deling : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

N-Bo dy Simulations  (Ta jh Taylor) 

 Delaunay Triangulation - more applications 

 N-Bo dy Intro duction 

. Basic Assumptions : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Applications : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. History of Algorithms : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Mesh-based Algorithms 0

 Tree-based Algorithms 

. Barnes-Hut Algorithm : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Fast Multip ole Metho d : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

N-b o dy Simulations  (Steve Gribble) 

 Fast Multip ole Metho d (Review) 

. The Four Ideas : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Interaction Lists : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Callahan and Kosara ju's Algorithm 

. Well Separated Pair Decomp ositions : : : : : : : : : : : : : : : : : : : : : : 

. De�nitions : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Algorithm: Tree Decomp osition : : : : : : : : : : : : : : : : : : : : : : : : : 

. Algorithm: Well-Separated Realization : : : : : : : : : : : : : : : : : : : : : 

. Bounding the size of the realization : : : : : : : : : : : : : : : : : : : : : : :  0

 N-b o dy Summary  

VLSI Physical Design  (Rich Vuduc)  

 Some notes regarding the homework assignment  

. Representing a Delaunay triangulation : : : : : : : : : : : : : : : : : : : : :  

. Incremental Delaunay : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : :  


-----

. Rupp ert Meshing : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Surface Approximation : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Intro to VLSI Physical Design Automation 0

. Overview : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. The role of algorithms : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. Evolution : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

 Summary 0

VLSI Physical Design  (Mehul Shah) 0

 Intro duction to VLSI Routing 0

 Global Routing Algorithms 

 Two-Terminal Nets: Shortest Paths 

. Dijkstra's Algorithm : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Maze Routing : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Multi-Terminal Nets: Steiner Trees 

. Steiner Trees : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Optimal S-RST for separable MSTs : : : : : : : : : : : : : : : : : : : : : : : 

VLSI  & Pattern Matching  (Noah Treuhaft) 0

 Integer Programming For Global Routing 0

. Concurrent Layout : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

. Hierarchical Layout : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Detailed Routing (Channel Routing) 

. Intro duction : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Left Edge Algorithm (LEA) : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Greedy : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Sequence Matching And Its Use In Computational Biology 

. DNA : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Proteins : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Human Genome Pro ject : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Sequence Alignment : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Pattern Matching  (Felix Wu) 


-----

 Longest Common Subsequence 

 Global Sequence Alignment 

. Cost Functions for Protein Matching : : : : : : : : : : : : : : : : : : : : : : 

 Sequence Alignment Algorithms 

. Recursive Algorithm : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Memoizing : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Dynamic Programming : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Space E�ciency : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

 Gap Mo dels 

 Lo cal Alignment 

 Multiple Alignment 

 Biological Applications 

Indexing and Searching  (Helen J. Wang) 

 Pattern Matching (continued) 

. Ukkonen's Algorithm : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Intro duction to Indexing and Searching 

 Inverted File Indexing 

. Inverted File Compression : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Representing and Accessing Lexicons : : : : : : : : : : : : : : : : : : : : : : 

Indexing and Searching  (Ben Horowitz) 

 Evaluating information retrieval e�ectiveness 

 Signature �les 

. Generating signatures : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Searching on Signatures : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Query logic on signature �les : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Cho osing signature width : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. An example: TREC : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

 Vector space mo dels 0

. Selecting weights : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Similarity measures : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. A simple example : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 


-----

. Implementation of cosine measures using inverted lists : : : : : : : : : : : : 

. Relevance feedback : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Clustering : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Latent semantic indexing (LSI) 

. Singular value decomp osition (SVD) : : : : : : : : : : : : : : : : : : : : : : 

. Using SVD for LSI : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. An example of LSI : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Applications of LSI : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Performance of LSI on TREC : : : : : : : : : : : : : : : : : : : : : : : : : : 0

Evolutionary Trees and Web Indexing (Amar Chaudhary) 

 Evolutionary Trees (Andris Ambainis) 

. Parsimony : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Maximum-Likeliho o d : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Distance metho ds : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Finding authoritative web pages using link structure (David Wagner) 

. A naive approach using adjacency : : : : : : : : : : : : : : : : : : : : : : : : 

. An algorithm for �nding communities within topics : : : : : : : : : : : : : : 

Clustering (Josh MacDonald) 

 Principle Comp onent Analysis 

 Intro duction to Clustering 

. Applications : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Similarity and Distance Measures : : : : : : : : : : : : : : : : : : : : : : : : 

 Clustering Algorithms 

. Bottom-Up Hierarchical Algorithms : : : : : : : : : : : : : : : : : : : : : : : 

. Top-Down Hierarchical Algorithms : : : : : : : : : : : : : : : : : : : : : : : 

. Optimization Algorithms : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Density Search Algorithms : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Summary : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Guest lecture Eric Brewer on HotBot (Carleton Miyamoto) 0

 Comment on Assignment (Guy) 0

 Goals of HotBot 


-----

 Internal Architecture 

. Semantics : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Hardware : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Data Base Mo del : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Score : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Filters : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Optimizations 

. Caching : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Compression : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Data Base : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Parallelism : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Misc. : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

 Crawling 

 Summary 

Other Material 

 References by Topic 

. Compression : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Cryptography : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

. Linear and Integer Programming : : : : : : : : : : : : : : : : : : : : : : : :  0

. Triangulation : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : :  0

. N-b o dy Simulation : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : :  

. VLSI Physical Design : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : :  

. Pattern Matching in Biology : : : : : : : : : : : : : : : : : : : : : : : : : : :  

. Indexing and Searching : : : : : : : : : : : : : : : : : : : : : : : : : : : : : :  

. Clustering : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : :  

 Assignments  

Assignment  (Compression) : : : : : : : : : : : : : : : : : : : : : : : : : : : : : :  

Assignment  (Cryptography) : : : : : : : : : : : : : : : : : : : : : : : : : : : : :  

Assignment  (Integer and Linear Programming) : : : : : : : : : : : : : : : : : :  

Assignment  (Triangulation and N-b o dy) : : : : : : : : : : : : : : : : : : : : : : 

Assignment  (VLSI and Pattern Matching) : : : : : : : : : : : : : : : : : : : : : 0


-----

List Of Algorithms

The following algorithms are covered to some extent in these notes, ranging from a short

overview to a full lecture.

Compression

Hu�man Co ding : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Arithmetic Co ding : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

LZ and LZW : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

LZ (Sliding Windows) : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

JPEG Co ding : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

MPEG Co ding : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Wavelet Compression : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Cryptography

DES : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

RC : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Merkle-Hellman Knapsack Algorithm : : : : : : : : : : : : : : : : : : : : : : : : : 

RSA : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

ElGamal : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Blum-Goldwasser : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Linear Programming

Simplex : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Ellipsoid Algorithm: Khachian : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Interior Point: A�ne Scaling : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

Interior Point: Potential Reduction : : : : : : : : : : : : : : : : : : : : : : : : : : 0

Interior Point: Central Tra jectory : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

Integer Programming

Branch and Bound Enumeration : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Implicit Enumeration : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Cutting Plane : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Crew Scheduling: Anbil, Tanga and Johnson : : : : : : : : : : : : : : : : : : : : : 

Triangulation

Convex Hull: Giftwrapping : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Convex Hull: Graham Scan : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Convex Hull: Mergehull : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Convex Hull: Quickhull : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Delaunay Triangulation: Blello ch, Miller, and Talmor : : : : : : : : : : : : : : : : 

Delaunay Triangulation: Incremental : : : : : : : : : : : : : : : : : : : : : : : : : 

Meshing: Rupp ert's Algorithm : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

Surface Mo deling: Garland and Heckb ert : : : : : : : : : : : : : : : : : : : : : : : 


-----

N-b o dy Simulation

Particle Mesh (using FFT : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

Barnes-Hut : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Fast Multip ole Metho d: Greengard and Rokhlyn : : : : : : : : : : : : : : : : : : 

Callahan and Kosara ju : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

VLSI Physical Design

Shortest paths: Dijkstra's Algorithm : : : : : : : : : : : : : : : : : : : : : : : : : 

Shortest paths: Hadlo ck's Algorithm : : : : : : : : : : : : : : : : : : : : : : : : : 

Optimal Rectilinear Steiner Trees : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Routing with Integer Programming : : : : : : : : : : : : : : : : : : : : : : : : : : 0

Detailed Routing: Left Edge Algorithm : : : : : : : : : : : : : : : : : : : : : : : : 

Detailed Routing: Greedy Algorithm : : : : : : : : : : : : : : : : : : : : : : : : : 

Pattern Matching in Biology

Sequence Alignment: Memoizing : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Sequence Alignment: Dynamic Programming : : : : : : : : : : : : : : : : : : : : : 

Sequence Alignment: Hirschb erg : : : : : : : : : : : : : : : : : : : : : : : : : : : : 0

Alignment with Gaps: Waterman-Smith-Beyer : : : : : : : : : : : : : : : : : : : : 

Alignment with Gaps: Gotoh : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Lo cal Alignment: Smith-Waterman : : : : : : : : : : : : : : : : : : : : : : : : : : 

Sequence Alignment: Ukkonen : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Indexing and Searching

Inverted File Compression : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Searching Signature Files : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Vector Space Searching : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Latent Semantic Indexing (LSI) : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Authoritative Pages: Kleinb erg : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Clustering

Bottom-up Hierarchical Clustering : : : : : : : : : : : : : : : : : : : : : : : : : : 

Splinter Group Clustering : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 

Clustering with Linear Programming : : : : : : : : : : : : : : : : : : : : : : : : : 

Density Search Clustering : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : : 


-----

Algorithms in the Real World Notes by Ben Zhao

Lecture # (Compression ) �c   Ben Zhao and Guy Blello ch

 Intro duction to Compression

� Information Theory

� Lossless Compression

. Hu�man Co ding

. Shannon-Fano Co ding

. Arithmetic Co ding

. LZ and LZW (GIF, UNIX Compress...)

. LZ (gzip, ZIP, ...)

. PPM (prediction by partial matching)

� Lossy Compression

. Transform Co ding (Blo cks: JPEG, MPEG, Wavelets...)

. Vector Quantization

. Information Theory

How much can we compress any given data? It Dep ends on how much \information" the

data contains.

Entropy

Shannon b orrowed the the notion of entropy from statistical physics to capture the infor
mation contained in an information source. For a set of p ossible messages S, it is de�ned

as,

X 


H (S ) =


pi


log




i pi

message that can b e sent by the source. The entropy is a


where pi


th

is the probability of i


measure of the average numb er of bits needed to send a message, therefore larger entropies

represent more information. Perhaps counter intuitively, the more random a set of messages



(the more even the probabilities) the more information they contain. The terms log  pi


represent the numb er of bits used to co de message i (the information contained in Si

Therefore messages with higher probability will use fewer bits.


).


-----

Table : Information Content of the English Language


Examples:


pi


= f0:; 0:; 0:; 0:; 0:g


H =  � 0: � log 

= : + 0:

= :


 +  � 0: � log


 


pi


= f0:; 0:; 0:; 0:; 0: g


H = 0: � log

= 0: + :

= 


 +  � 0: � log











pi


= f0:; 0:0; 0:0; 0:0 ; 0 :0 g




H = 0: � log

= 0: + 

= :


(


) +  � 0:0 � log 











Note that the more uneven the distribution, the lower the Entropy.

. The English Language

We might b e interested in how much information the English Language contains. This could

b e used as a b ound on how much we can compress English, and could also allows us to

compare the density (information content) of di�erent languages.

One way to measure the information content is in terms of the average numb er of bits p er

character. Table  shows a few ways to measure the information of English in terms of bits
p er-character. If we assume equal probabilities for all characters, a separate co de for each

character, and that there are  printable characters (the numb er on a standard keyb oard)

then each character would take dlog e =  bits. The entropy assuming even probabilities is


-----

Table : Lossless compression ratios for text compression on Calgary Corpus

log  = : bits/char. If we give the characters a probability distribution (based on a corpus

of English text) the entropy is reduced to ab out . bits/char. If we assume a separate co de

for each character (for which the Hu�man co de is optimal) the numb er is slightly larger .

bits/char.

Note that so far we have not taken any advantage of relationships among adjacent or

nearby characters. If you break text into blo cks of  characters, measure the entropy of those

blo cks (based on measuring their frequency in an English corpus) you get an entropy of ab out

 bits. When we divide this by the fact we are co ding  characters at a time, the entropy

(bits) p er character is .. If we group larger and larger blo cks p eople have estimated that

the entropy would approach . (or lower). It is imp ossible to actually measure this b ecause

there are to o many p ossible strings to run statistics on, and no corpus large enough.

This value . bits/char is an estimate of the information content of the English language.

Assuming it is approximately correct, this b ounds how much we can exp ect to compress

English text if we want lossless compression. Table  also shows the compression rate of

various compressors. All these, however, are general purp ose and not designed sp eci�cally for

the English language. The last one, BOA, is the current state-of-the-art for general-purp ose

compressors. To reach the . bits/char the compressor would surely have to \know" ab out

English grammar, standard idioms, etc..

A more complete set of compression ratios for the Calgary corpus for a variety of com
pressors is shown in Table . The Calgary corpus is a standard b enchmark for measuring

compression ratios and mostly consists of English text. In particular it consists of  b o oks, 

pap ers,  bibliography,  collection of news articles,  programs,  terminal session,  ob ject

�les,  geophysical data, and  bit-map b/w image. The table shows how the state of the

art has improved over the years.


-----

 Basic Compression Algorithms

We will �rst discuss co des that assign a unique bit-string for co ding each symb ol (Hu�man

co des and Shannon Fano co des) and then discuss Arithmetic co ding which \blends" the

co des from di�erent symb ols.

. Pre�x Co des

� each symb ol (message) is a leaf in a binary tree

� the co de is enco ded in the path from ro ot to the leaf (left = 0, right = )

� Property: No co de is a pre�x of another co de

The average length of a pre�x co de assuming a probability distribution on the symb ols

P

th

is de�ned as la = i pi li where pi is the probability of the i symb ol and li is the length of

its co de (the depth of its leaf ).

. Hu�man Co des

Hu�man co des are an optimal set of pre�x co des. They are optimal in the sense that no

other pre�x co de will have a shorter average length.

To build a Hu�man co de tree:


� start with a forest of trees each representing a symb ol and with weight wi

� Rep eat until single tree


= pi


{ select two trees with lowest weights (w

{ combine into single tree with weight w

Prop erties of Hu�man Co ding:


and w

+ w


)


. The length of the co de for symb ol i is approximately log




(




pi


). (In the original lecture





I said that dlog


(


)e is an upp er b ound on the length of each co de. This is actually


 pi

not true, as p ointed out by a student. Consider the probabilities :0; :0; :; :. A


Hu�man co ding will give the probability .0 a length , which is - dlog


(=:)e = .




It is the last time I trust \Data and Image Compression" by Gilb ert Held.)




. The average length la

integer, for all i.


of a Hu�man co de matches the entropy if pi


j


=


where j is any


-----

. Shannon-Fano Co ding

Also a pre�x co de, but tree is built from the top down, as opp osed to b eing built from

b ottom-up as in the Hu�man Co ding. First sort S by probabilities, then partition list of

messages into two partitions, such that the subsums of the probabilities in each partition is

as close to 0% as p ossible. Each partition is assigned a branch with a  or a 0. Rep eat

pro cess until tree is fully built and all messages are separated into leaves.

make_codes(S)

if |S| =  then S[0]

else

sort S by probabilities

split S into S and S such that W(S) approx. W(S)

return node(make_code(S), make_code(S))

where W(S) represents the sum of the probabilities in the set S. Unlike Hu�man co des,

Shannon-Fano co des do not always give optimal pre�x co des.

. Arithmetic Co ding

Given the probability of each symb ol, we start with a probability range of . Then we

separate the range of  into discrete partitions according to the probabilities of each symb ol.

So if P (a) = 0: and P (b) = 0:, then 0% of the range is one partition for the symb ol a.

As each symb ol is read from the input, the range is further re�ned as the lower and upp er


b ounds of the range are mo di�ed by the probability of the new symb ol. If we use Li


and Ui


to denote the lower and upp er b ounds, and li


and ui


to denote the range of probability for


that single symb ol (i.e. la

and

Properties:


= 0 and ua


= 0:), then we have:


Li

Ui


= Li�

= Li�


+ (Ui�

+ (Ui�


� Li�


� Li� ) � ui


) � l


i


� might not b e able to emit co de until seen full message (in cases where the range

straddles 0., the �rst bit cannot b e output until the range falls to one side of 0.)

� asymptotically approaches entropy

� can require arbitrary precision arithmetic to implement (although we will see a nice

trick in the next class)

� often used together with other metho ds (i.e. as a back-end)

A solution to the straddling and precision problems is to separate the input into �xed size

blo cks (e.g. 00 symb ols), and output compressed co de for each blo ck


-----

. Deriving Probabilities

For Hu�man, Shannon-Fano and Arithmetic co ding we need probabilities. How do we derive

them.

� Static vs. Dynamic

{ Static for a single do cument: We could measure the probabilities over the do cu
ment we plan to send and use those. In this case we have to send the probabilities

(or generated co des) to the deco der.

{ Static for a language: We could use a pre-measured set of probabilities. In this

case the deco der could already know the probabilities.

{ Dynamic: We could up date the probabilities as we are sending a do cument based

on what we have seen. In this case the deco der can also calculate the probabilities

on the �y as it deco des the message (we don't have to send them).

� Single symb ols vs. Groups of Symb ols

{ We could measure the probability of each symb ol indep endent of its context.

{ We could measure the probability based on a context (i.e. previous symb ols). This

is discussed further in the next class and will usually give much b etter compression.

PPM: Prediction by partial matching

This is one of general-purp ose algorithms that gets the b est compression ratios (although it

is certainly not the fastest). It is based on generating static probabilities over the current

do cument using the symb ols and their context. The algorithm can b e outlined as follows.

� Try �nding all multiple o ccurrences (matches) of strings of length n in the message (n

is a preset constant).

� For leftovers, try to �nd multiple o ccurrences of strings of n � .

� rep eat until all p ossible matches are found, and assign a probability to each string

according to # of o ccurrences.

� Send the probabilities along with the arithmetic co ding of the message that uses the

probabilities.

 Lemp el-Ziv Overview

The Lemp el-Ziv algorithms compress by building a table of previously seen strings. They do

not use probabilities (a string is either in the table or it is not). There are two main variants

based on two pap ers they wrote, one in   (LZ) and the other in   (LZ).

� LZ (Dictionary Based)


-----

Table : LZ Enco ding on \aaaaaa"

Table : LZ Enco ding on \ab cab ca"

{ LZW: Lemp el-Ziv-Welch

{ LZC: Lemp el-Ziv Compress

{ LZMW: (Unix Compress, GIF)

� LZ (Sliding Window)

{ Window instead of dictionary

{ LZSS: LZ-Storer-Szymanski (gzip, ZIP, many others)

Traditionally, LZ is b etter but slower.

. LZ and LZW

Basically starts with a string lo okup table (dictionary) consisting of the standard characters,

and generates a dynamic table of new string patterns of increasing length. The decompression

algorithm dep ends on it b eing able to generate the same table as the compressor.

Enco de:

w = NIL

while (K = readchar()) {

if wK in dictionary

w = wK

else {

output code for w

add wK to dictionary

w = K }

}

output code for w

Key is noting that the co de for for a new string wK is not output until the second time it

is seen. This makes it p ossible for the deco der to know what the co de represents. If in the


-----

Table : LZ Deco ding on \a b c  " and on \a  "

else clause we output the new co de for wK instead of w the message would b e imp ossible to

deco de.

Tables  and  show two examples of the enco der. Note that the second example shows

a contingency that must b e accounted for, when the input has a long string of the same

character. The deco der must b e able to recognize this and know that co de  is \aa". This

is handled by the else clause b elow.

Deco de:

w = lookup(readcode())

output w

while ( c = readcode()) {

if C in dictionary

wn = lookup(C)

else

wn = stringcat(w, w[0])

output wn

K = wn[0]

add wK to dictionary

w = wn

}

Tables  shows two examples of deco ding.

Prop erties:

. Dynamic: (e.g. works well with tar �les which have many formats), adaptable.

. No need to send the dictionary (In LZW need to send clear signals to clear dictio
nary/string table)


-----

. Can use Tries to store the dictionary/lo okup tables, making lo okups e�ectively exe
cutable in unit time.

What happ ens when dictionary gets to o large?

. Throw dictionary away when reaching a certain size (GIF)

. Throw dictionary away when not e�ective (Unix Compress)

. Throw Least Recently Used entry away when reaches a certain size (BTLZ  - British

Telecom Standard)

. LZ (Sliding Windows)

This scheme involves a �nite lo okahead window, and the X most recently characters enco ded

as the dictionary. lo ok in the lo okahead window to �nd the longest string that starts at the

b eginning of the bu�er and has already o ccurred in the dictionary. Then output: . p osition

of prev. o ccurrence in window, . length of string, . next char. Then advance windows by

length + .

Example:

        0     

a a c a a c a b c a b || a b a c <--- Data Source

<-----Dictionary-----> || <--L.B.-->

(previously encoded) (lookahead buffer)

Lookahead buffer encoded as <0, , c>

LZSS Variant:

Don't output next char, instead there are two output formats:

(0, p osition, length)

(, char)

Typically only output �rst format if length � . Use Hu�man co ding to co de the outputs.

Optimization: Use Trie to quickly search for match in window (gzip).

Example: Window size = 

Input : aaaaaa

Output: (, a) (0, , )

Input : abcabca

Output: (, a) (, b) (, c) (0, , ) (, a)


-----

Algorithms in the Real World Notes by Gabriel Moy

Lecture # (Compression ) �c   Gabriel Moy and Guy Blello ch

� Review and expansion on previous class

{ Can we compress all strings?

{ Hu�man co des (grouping and cho osing b etween co des with equal average length).

{ Integer implementation of arithmetic co ding

{ Conditional entropy and Markov mo dels

{ The JBIG standard

{ The use of Tries is LZW and space issues

{ Run length co ding (used for Fax co ding) and residual compression (used in the

lossless JPEG standard)

� Lossy compression

{ Intro

{ Scalar quantization

{ Vector quantization

{ Intro to transform co ding

 Lossless Compression: review and expansion

. Can we compress all strings?

Can a compression algorithm compress some messages without expanding others?

Not if all strings are valid inputs

For a character set of size m and messages of length n, if one string is compressed to


l < n � l og


(m), then at least one string must expand to l - n � l og


(m).


GZIP will only expand slightly if no compression is p ossible. Alternatively, GZIP might

check to see if no compression o ccurred.

. Hu�man Co des Revisited

It can b e shown that H (s) � R < H (s) +  where H (s) is entropy and R is the average co de

length. Pro of of this inequality will b e a homework problem. The di�erence H (s) � R is the

overhead caused by Hu�man co ding.

A standard trick to reduce the overhead p er-symb ol is to group symb ols. For example,

if there are  symb ols, we can generate the probabilities for all  pairs by multiplying the

probabilities of the symb ols (there will b e at most  unique probabilities). Now generate a


-----

Hu�man co de for these probabilities and use it to co de two symb ols at a time. Note that

we are not taking advantage of patterns among characters as done with the LZ algorithms

or Conditional Entropy discussed later (we are assuming the probability of each symb ol is

indep endent of others). Since the overhead is now distributed across pairs of symb ols the

average p er-symb ol overhead is b ounded by /. If we group ed  symb ols it would b e /.

This works �ne for a few symb ols, but the table of probabilities and the numb er of entries

in the Hu�man tree will quickly grow large when increasing the numb er of symb ols in the

group.

All Hu�man co des for a given set of probabilities will have the same length, but there

are di�erent p ossible ways of enco ding.

symb ol probability co de  co de 

a 0. 0 0

b 0.  00

c 0. 000 

d 0. 000 00

e 0. 00 0

Both co dings pro duce an average of . bits p er symb ol

With these two co dings, one has a high variance in length (co de ), while the other has

a low variance (co de ). With low variance co ding, a constant character transmission rate

is more easily achieved. Also, bu�er requirements in a low variance co ding scheme might b e

less. Lowest variance co ding can b e guaranteed by the following construction.

� After joining two no des with the lowest probabilities (highest priority), give this joint

probability a lower priority than other existing no des with the same probability.

� In the example ab ove, after 'd' and 'e' are joined, the pair will have the same probability

as 'c' and 'a' (.), but is given a lower probability so that 'c' and 'a' are joined next.

� Now, 'ac' has the lowest priority in the group of 0. probabilities

� 'b' and 'de' are joined, and �nally, 'ac' is joined with 'b de' revealing the tree shown in

Figure 

###### 0 1

 0 1 0 1

 b a c 0 1

 d e

Figure : Binary tree for Hu�man co de 


-----

. Arithmetic Co ding Revisited

It can b e shown that Arithmetic co ding is b ounded as follows: m � H (s) � l � m � H (s) + 

where m is the length of the input, l is the length of the output, and H(s) is the p er-symb ol

entropy.

An e�cient and easy way of implementing arithmetic co ding is by using the following

integer implementation. The implementation won't give exact arithmetic co ding b ecause

of roundo� error, but will b e close. If b oth sender and receiver use the same arithmetic

they will round in the same way making it p ossible for the receiver to deco de the message

prop erly.

The Integer Implementation is as follows:


� Assume probabilities are counts c

Pi


; c


; : : : ; c


(Fractions will also work)





m


� Cumulative Count: Ci

Pm

� Total Count: T =


cj


� Cumulative Count: Ci = j = cj

Pm

� Total Count: T = j = cj

� As with any arithmetic co ding we start with a �xed-sized region and narrow it each

time we co de a new character. In our integer implementation the region is initialized

k


to [0::(R � )] where R = 


(i.e. is a p ower of ).


� To avoid narrowing to a region of size less than , we scale (expand) the region by a

factor of  under the following conditions:

{ If the region is narrowed down such that it is either in the top or b ottom half of

the space, output a  or 0, resp ectively, and scale using the appropriate scaling

rule.

{ If the region is narrowed down to the second and third quarters, then the region

will b e expanded ab out the middle using scale rule #, describ ed b elow.

� The Algorithm

k

{ Let u and l b e integers < K = 


{ Initial values: u0

�


= K � ; l0


= 0

�

Cxj


{ uj

{ lj


= lj �


= lj �


+

�


� lj �


+ )

C


(uj �


� 

�


� lj �


+


(uj �


+ )


T

xj �

T


� Scaling Rules

{ #: If uj

output 


=  : : : and lj


=  : : : then (the region of interest is in the top half )


shift u to the left and insert a 

shift l to the left and insert a 0

output s zeros, where s is the numb er of times expanded ab out the middle region

set s = 0


-----

{ #: If uj

output 0


= 0 : : : and lj = 0 : : : then (the region of interest is in the b ottom half )


shift u to the left and insert a 

shift l to the left and insert a 0

output s ones, where s is the numb er of times expanded ab out the middle region

set s = 0


{ #: If uj


= 0 : : : and lj


= 0 : : : then (the region of interest is in the second and


third quarters of the range)

s = s + 

shift u to the left and insert a 

shift l to the left and insert a 0

complement the MSB (most signi�cant bit) of l and u

Question:

If we expand ab out the middle, expand ab out the middle, and expand in the top, what

output do we get?

Following the rules, s gets incremented twice by expanding ab out the middle. When we

expand in the top half, we output a  and s numb er of zeros (in this case, s=). Output:

00

Example:


Let c


= 0; c


= ; c


=


Which gives C0


= 0; C


= 0; C


= ; C

k





= T = 0


We chose a k such that  � T < K = 

In this case, T = 0, so k = ; K = .

The message we want to transmit is 


i ui


binary li


binary output scale rule xi


Cxi


�


C


xi


0   0 00000000  0 0

 0 000 0 00000000   0

 0 000  000  Rule 

  000  0000 Rule 

  00  00000  0 

  00000  00000 0 Rule 

  00000  000000 0 Rule 

  0000  000000 0 Rule 

  000  000000  Rule 

  000  0000000 0 Rule 

  00  0000000 Rule 

   0 0 00000000  0 0

  00000 0 00000000


-----

###### P(b|w)

 P(w|w) Sw Sb P(b|b)

 P(w|b)

Figure : A two state Markov Mo del

. Conditional Entropy and Markov Chains

Conditional entropy comes into use in b oth lossless and lossy techniques. Compression can

b e increased by knowing the context of the message (symb ol). For example, in images, the

surrounding pixels can b e used as the context. In black and white faxes, if there is a black

pixel, and the surrounding areas also contain black pixels, it is highly probable that the next

pixel is also black. For text, previous characters can b e used as the context.

The conditional entropy of T based on context S is de�ned by the equation:





H (T jS ) =

w her e


X

j


P (Sj


jSj


)l og


)


X

i


P (Ti


P (Ti jSj


)


P (Sj

P (Ti jSj


) = pr obabil ity of context Sj

) = pr obabil ity of Ti in context S


j


It is not hard to show that if T is indep endent of the context S then H (T jS ) = H (T )

otherwise H (T jS ) < H (T ). In other words, knowing the context can only reduce the entropy.

A way to represent these conditional probabilities is through a Markov Mo del (or Markov

Chain). Figure  shows a Markov Mo del where there are two states, white (Sw) and black

(Sb), and conditional probabilities:

P (w jw ) = pr obabil ity of g etting a w hite pixel if the pr ev ious pixel w as w hite

P (w jb) = pr obabil ity of g etting a w hite pixel if the pr ev ious pixel w as bl ack

P (bjb) = pr obabil ity of g etting a bl ack pixel if the pr ev ious pixel w as bl ack

P (bjw ) = pr obabil ity of g etting a bl ack pixel if the pr ev ious pixel w as w hite

In the case of a fax machine, the probabilities of staying in the same state, P (bjb) and

P (w jw ), are higher than the probability of switching states.

Conditional probabilities can b e used with arithmetic co ding to co de messages with

average length that asymptotically matches the conditional entropy. The idea is that for

every context we have a separate narrowing function based on the probabilities for that

context.


-----

|Col1|O|O|O|Col5|
|---|---|---|---|---|
|O|O|O|O|A|
|O|O|X|||

|Col1|O|O|O|O|O|A|
|---|---|---|---|---|---|---|
|O|O|O|O|X|||


###### (a) (b)


###### 1 0 0 0 1 0 0 1

 1 0 0 0 0 0 1

|Col1|0|0|0|Col5|
|---|---|---|---|---|
|1|0|0|0|1|
|1|0|0|||

|Col1|0|0|1|1|1|0|
|---|---|---|---|---|---|---|
|0|0|0|1|1|||


###### (a) (b)

Figure : a) Three-line neighb orho o d b) Two-line neighb orho o d

. The JBIG Standard

JBIG stands for the Joint Bilevel Image Pro cessing Group. Probabilities are generated based

on context. This standard is used for black and white, where the table of probabilities is

k


only 


, where k is the numb er of pixels used as the context. Neighb orho o ds are used as the


context. Example neighb orho o ds are shown in Figure . In the JBIG standard, there is

also what is known as a roaming pixel. One of the context pixels, 'A' in Figure , is p ossibly

lo cated n pixels away. The current pixel is denoted by 'X'. This is useful when there are

vertical lines b eing transmitted. If the JBIG standard was used on color images, then the

table would grow to o large to b e practical. After building a probability table, the image is

then sent after b eing arithmetically enco ded. There is also a default probability table that

was made after analyzing thousands of images.

. Tries and use in LZW

An example trie structure is shown in Figure . When using a trie structure for LZW,

searches can b e done in unit time, since the previous search is the parent of the next search.

The problem with using tries is that the amount of memory needed for a trie can get large.

Consider a dictionary of size 0 . The p ointers in the trie need to b e l og (0 ) bits = .

bytes long. If we have  symb ols the amount of memory we will need is 0  entries - 

child p ointers - . bytes/p ointer � . Megabytes!

Another way of storing the dictionary is by using hash tables. The choice of whether to

use a hash table or a trie structure dep ends mostly on the size of the dictionary and the

available memory.

. Other Lossless Compression Techniques

In older fax machines, run length compression is used to transmit and receive messages. The

algorithm creates a list of numb ers that corresp ond to the numb er of consecutive black dots

then the numb er of consecutive white dots and rep eats until the end of the message. The

list is then Hu�man co ded and transmitted to the receiving fax, which deco des by applying

the algorithm in reverse. This metho d works OK for black and white images, but JBIG is

two to three times b etter.


-----

###### B
 Etc...
 C D A B C D

Figure : A trie structure

Residual compression is another lossless compression technique. It is used in lossless

JPEG, which handles b oth grey-scale and color images. Residual compression guesses the

next pixel value based on context and outputs the di�erence b etween the guess and actual

value. The di�erences are Hu�man co ded and transmitted. Guesses of the next pixel are

usually a weighted sum of pixels in the neighb orho o d. For the most part, the guesses

are go o d. Instead of Hu�man co ding the original pixel values we now Hu�man co de (or

arithmetic co de) the residuals. The residuals will tend to have a lower entropy than the

original data (i.e. 0s and low values have high probabilities, while high values have low

probabilities) giving us a more e�cient co ding. Note that the residual values can b e negative.

 Lossy Compression

There are many ways to achieve lossy compression. Some of these include

� scalar quantization,

� vector quantization,

� transform co ding (wavelets, blo ck cosine in JPEG and MPEG),

� fractal co ding, and mo del based co ding.

Judging the e�ectiveness of lossy compression is di�cult. Unlike lossless compression where

measures are easily quanti�able (compression ratio, time, etc.), lossy compression also has

some qualitative measures. In fact many p eople argue that the quantitative measures for

lossy compression such as ro ot-mean-square error are not go o d measures of human p ercep
tion.

. Scalar Quantization

This is the simplest technique. The idea is to group a large numb er of regions to a smaller

numb er of regions. An example of this is using only the most signi�cant  bits of an  bit

message. This is an example of a uniform scalar quantization. The function is shown in

Figure a.


-----

###### Output

 0 4 8 12 16 20 24 28 32 ...

 (b)


###### 9

 8

 7

 6

 5

 4

 3

 2

 1

 0


###### Output

 0 4 8 12 16 20 24 28 32 ...

 (a)


###### 9

 8

 7

 6

 5

 4

 3

 2

 1

 0


###### Input


###### Input


Figure : a) Uniform Scalar Quantization b) Nonuniform Scalar Quantization

Non-uniform scalar quantizations might have a function similar to Figure b. Non
uniform quantizations are useful when some regions have more useful information than

others. For example, di�erences in low values of red are more sensitive to the eyes than

di�erences in high values of red. In this case, keeping as much information when the val
ues are low is imp ortant, while grouping some of the high values will lead to a very go o d

approximation. For images, this allows for b etter quality for the same compression.

. Vector Quantization

The idea of vector quantization is given a set S of p ossible vectors to generate a representative

subset R � S which can b e used to approximate the elements of S . The set R are called

the co de vectors. The incoming data gets parsed into vectors and the enco der �rst �nds the

closest (by Euclidean norms) co de vector. The index of the co de vector can now b e sent

(p ossibly after the normal Hu�man co ding). The quality of this compression will dep end on

the size of the co deb o ok. Figure  shows a blo ck diagram of vector quantization.

What should b e used as the vectors? In images, the values of red, green, and blue can b e

used as a vector. Vector quantization can b e used to reduce  bit color to  bit color. Many

terminals use some sort of vector quantization to save on screen memory, and it is supp orted

by the graphics hardware. For sp eech, a pre-de�ned numb er, K, of consecutive samples can

b e used as the vector. Another way to break up an image into vectors is to represent blo cks

of pixels as a vector.

Vector quantization used along with a residual metho d pro duces a lossless compression.

All that needs to b e transmitted is the index of the co de vector and the di�erence b etween

the co de vector and the actual vector.

. Transform Co ding


To use transform co ding, a linear set of basis functions (�i


) that span the space must �rst


b e selected. Some common sets include sin, cos, spherical harmonics, Bessel functions,

wavelets, and rotation. Figure  shows some examples of the �rst three basis functions for


-----

###### Encode

 Source
 Codebook Index

 Find
 Generate Vectors Closest
 Code Vector

 Decode

 Index Codebook

 Generate Output

 Out

Figure : Vector Quantization

###### Cosine f(x)

 i

 0 1 2

 Polynomial

 0 1 2

 Wavelet

 0 1 2

Figure : Transforms

cosine, p olynomial, and wavelet transformations. The wavelet transform is esp ecially go o d

at capturing lo cal features.

th

|Source|Col2|Col3|
|---|---|---|
|Source Codebook Index Find Generate Vectors Closest Code Vector Decode Index Codebook Generate Output Out|Codebook Index Find Closest Code Vector||
||||

|0|1|2|Col4|
|---|---|---|---|
|||||


The general equation for generating the i

to transform is

n

X


transform co e�cient �i


given a function F (x)


(xj


)F (xj


�i

w her e �i


=

j =

th

= i


�i


)


tr ansf or med coef f icient


. Cho osing a Transform

The goals we have when cho osing a transform are:

� Decorrelate the data

� Low co e�cients for many terms

� Some basis functions can b e ignored by p erception


-----

Low co e�cients for many terms will allow us to either drop them and only send the larger

co e�cients. The higher frequency cosines will not b e able to b e p erceived, so it is allowable

to drop them. This is low pass �ltering a signal (taking only the lower frequency comp onents

of a FFT).

Question:

Why not use a Fourier (or cosine) transform across the whole image?

Imagine a totally white background with a black pixel in the middle. This is represented

as an impulse function, and the Fourier transform of an impulse function is  for all frequen
cies. To adequately represent the image, we will not b e able to drop any co e�cients since

they are all of the same magnitude. JPEG blo cks the image o� b efore applying transforms.


-----

Algorithms in the Real World Notes by Ben Liblit

Lecture # (Compression ) �c   Ben Liblit and Guy Blello ch

� Case Studies

. JPEG Enco ding

. MPEG Enco ding

� Other Lossy Transform Co des

. Wavelet Compression

. Fractal Compression

. Mo del-Based Compression

 Case Studies

In previous lectures we examined several algorithms for lossless and lossy compression. Now

we draw together these isolated parts into complete compression schemes suitable for use on

real-world data.

We will examine, as case studies, two p opular lossy compression schemes: JPEG for still

images, and MPEG for video.

. JPEG

.. JPEG Intro duction

JPEG is a lossy compression scheme for color and grayscale images. It has several imp ortant

prop erties:

� designed for natural, real-world scenes

JPEG sustains excellent compression rations on photographic material and naturalistic

artwork. It p erforms p o orly on carto ons, line drawings, and other images with large

areas of solid color delimited by sharp b oundaries.

� tunable lossy compression

JPEG discards data at several phases of the compression. In general, data is discarded

where it will have the smallest sub jective impact on a human viewer. JPEG contains

tunable quality \knobs" that allow one to trade o� b etween compression e�ectiveness

and image �delity.

� -bit color

JPEG maintains  bits of color data, in contrast to GIF's limit of  bits. In practice,

this can mean that GIF discards more data than JPEG, since GIF must �rst quantize

an image down to no more than  distinct colors.


-----

Figure : Steps in JPEG compression.

JPEG forms an excellent case study in compression b ecause it synthesizes a numb er of

distinct algorithms:

� Transform Co ding

� Scalar Quantization

� Di�erence Co ding

� Run Length Co ding

� Hu�man or Arithmetic Co ding

We will highlight each of these techniques as they app ear in the algorithm, b elow.

.. JPEG Compression Steps


-----

. (optional) Convert image from RGB to YIQ.

RGB is a three-dimensional vector space that describ es colors in a manner conve
nient for computer hardware. YIQ is a di�erent color space that more closely matches

sub jective human color p erception. The \I" represents the relative balance of orange

versus cyan. The \Q" comp onent represents the relative balance of green versus ma
genta. The \I" and \Q" comp onents collectively represent the hue, or \chrominance"

of any pixel. The \Y" comp onent represents the overall brightness, or luminosity, of

a color. This brightness is weighted to re�ect the sensitivities of human vision: green

contributes most to p erceived luminance, red contributes ab out half as strongly, and

blue has the least impact.

When converting the the image to YIQ, we must cho ose how many bits will b e used to

represent each comp onent. We generally devote four times as many bits to luminance

(Y) as we do to chrominance (IQ). The eye is much more sensitive to small changes in

brightness than it is to small changes in hue.

Incidentally, NTSC television transmissions enco de colors using the YIQ color space,

with the largest p ortion of bandwidth devoted to luminance. Also, since brightness

is represented using a single luminosity comp onent, black and white televisions can

display this value directly and simply ignore the two chrominance comp onents.

. Sub divide the image into blo cks of  �  pixels.

Small, �xed-size blo cks will greatly simplify subsequent computation. Small blo cks also

help to limit cosine transformation \leakage" should the image contain sharp (high
frequency) discontinuities. Without these blo cks, a single sharp feature could bleed

into the entire rest of the image.

. For each  �  blo ck, apply the discrete cosine transformation to pro duce a transformed

 �  blo ck with the same bit depth.

This is a deployment of transform co ding, indep endently applied to the horizontal and

vertical axes of each blo ck.

. Reduce the overall depth of these transformed blo cks by a scaling factor.

This is a deployment of scalar quantization. The quantization error that this necessarily

intro duces is the most signi�cant source of information loss in JPEG compression.

One could simply divide all entries by some uniform value, but this will not actually

give the b est results. When images are intended for use by human viewers, some bits

are more imp ortant than others. Instead, variable scaling factors are derived from

an  �  quantization table. Each element in the transformed blo ck is divided by the

corresp onding element in the quantization table. This allows us to b e selective in where

we discard information.

The JPEG standard de�nes two such tables. One is used for chrominance (I, Q), and

is not presented here. The other is used for luminance (Y), and is shown in Table .

Notice that the largest co e�cients are in the lower right corner, while the smallest


-----

  0   0  

      0 

    0   

      0 

     0 0 

     0  

    0  0 0

     00 0

Table : JPEG default quantization table, luminance plane.

are toward the upp er left. This will discard the most bits from high frequencies, and

the fewest bits from low frequencies. Psychometric studies show that the human eye

is more sensitive to lower frequencies, so this is where we can least a�ord to discard

information.

Abstractly, the default tables represent the relative imp ortance of features in any image.

If we were to uniformly double all of the quantization co e�cients, we would still b e

using the same relative imp ortance, but we would b e discarding more bits. Thus, the

entire quantization table may b e scaled by any single factor to improve compression

while reducing image quality.

In most JPEG compressors, this single factor is the \quality knob" made available

to the user. A scaling factor of  is a rough upp er limit for high-�delity repro duc
tion; factors up to  will b e lossy but presentable; factors as high as  may still b e

recognizable but are unusable for most practical tasks.

After quantization, the DCT co e�cients will lie in a much narrower range. This

reduces their overall entropy and will make subsequent compression more e�ective. In

fact, much of the high-frequency region toward the lower-right may have b een reduced

to zeros.

. Enco de the DC comp onents.

This is a deployment of di�erence co ding followed by Hu�man or arithmetic co ding.

The DC comp onent contains most of the information in the image. Across an entire

image, the DC comp onent is large and varied. Within any lo cal region, though, the

DC comp onent is often close to the previous value. Thus, instead of enco ding the

(high-entropy) DC values directly, we enco de the (low-entropy) di�erences b etween

DC values. Sp eci�cally, for each DC comp onent in each  �  blo ck, we enco de the

di�erence from the corresp onding DC comp onent in the previous  �  blo ck.

These di�erences will tend to b e small, and thus amenable to entropy co ding. Either

Hu�man or arithmetic co ding is used to further compress the DC di�erence stream.

. Linearize the AC comp onents.


-----

Figure : Zig-zag scanning of JPEG blo cks.

In order to sequentially enco de the AC comp onents of an  �  blo ck, we must �rst

represent it as a simple  �  vector. The obvious approach would b e to iterate across

the  cells in row-ma jor or column-ma jor order. A much b etter approach is to zig-zag

across the blo ck, as shown in Figure .

Why is this desirable? Recall that the upp er-left region represents high-frequency

features, while the lower-right represents low-frequency features. A zig-zag path groups

low- and high-frequency co e�cients close together in the  �  vector.

This means that successive co e�cients will tend to have similar values. Furthermore,

many co e�cients will b e zero, particularly toward the low-frequency lower-right corner.

These correlations will make subsequent compression much more e�ective.

. Enco de the AC comp onents.

This is a deployment of run length enco ding followed by Hu�man or arithmetic co ding.

AC comp onents are enco ded as (skip, value) pairs, where skip is the numb er of zeros

and value is the next non-zero comp onent. The sp ecial pair (0, 0) designates the end

of a blo ck.

The co de pairs are then further compressed using Hu�man or arithmetic co ding.

. MPEG

.. MPEG Intro duction

Correlation improves compression. This is a recurring theme in all of the approaches we

have seen; the more e�ectively a technique is able to exploit correlations in the data, the

more e�ectively it will b e able to compress that data.

This principle is most evident in MPEG enco ding. MPEG compresses video streams. In

theory, a video stream is a sequence of discrete images. In practice, successive images are

highly interrelated. Barring cut shots or scene changes, any given video frame is likely to


-----

Figure 0: MPEG I-frames intersp ersed with P-frames.

Playback order: 0        

Frame typ e: I B B P B B P B B I

Data stream order: 0        

Table : MPEG B-frames p ostp oned in data stream.

b ear a close resemblance to neighb oring frames. MPEG will exploit this strong correlation

to achieve far b etter compression rates than would b e p ossible with isolated images.

Each frame in an MPEG image stream is enco ded using one of three schemes:

I-frame, or intra-frame. I-frames are enco ded as isolated images. They do not take advan
tage of redundant information in any other frames.

P-frame, or predictive co ded frame. A P-frame can take advantage of redundant informa
tion in the previous I- or P-frame.

B-frame, or bidirectionally predictive co ded frame. A B-frame can take advantage of

similar information in b oth the preceding and the succeeding I- or P-frame.

Figure 0 shows a simpli�ed MPEG stream containing just I- and P-frames. Figure 

shows a more complex stream that adds B-frames.

I-frames and P-frames app ear in an MPEG stream in simple, chronological order. How
ever, B-frames are moved forward so that they app ear after their neighb oring I- and P-frames.

This guarantees that each frame app ears after any frame up on which it may dep end. An

MPEG enco der can deco de any frame by bu�ering the two most recent I- or P-frames en
countered in the data stream. Table  shows how B-frames are p ostp oned in the data stream

so as to simplify deco der bu�ering.

MPEG enco ders are free to mix the frame typ es in any order. When the scene is relatively

static, P- and B-frames could b e used, while ma jor scene changes could b e enco ded using


-----

Figure : MPEG I- and P-frames intersp ersed with B-frames.

I-frames. In practice, most enco ders use some �xed pattern like the ones shown here: two

or three P-frames b etween each pair of I-frames, and two or three B-frames b etween those.

.. MPEG Enco ding: I-Frames

Because I-frames are indep endent, an I-frame can b e deco ded quickly and simply, without

requiring additional information from elsewhere in the MPEG stream. Thus, I-frames form

anchor p oints for fast random access, reverse playback, error recovery, and the like.

I-frames are enco ded using a variant of JPEG. First, each frame is converted into the

YCrCb color space, a variant of JPEG's YIQ. The frame is then sub divided into  � 

pixel blo cks, called \macroblo cks". The luminance data (Y) is represented at full resolution:

each  �  macroblo ck is simply split into four  �  subblo cks. Chrominance data (Cr

and Cb) is represented at one quarter resolution: each  �  macroblo ck is reduced to a

single  �  subblo ck for each hue axis.

We now have six  �  blo cks (four Y, one Cr, one Cb). Enco ding of these  � 

blo cks pro ceeds using same JPEG scheme presented ab ove. Each blo ck is cosine-transformed,

quantized, zig-zag sequenced, run-length enco ded, and Hu�man enco ded to a �nal bit stream.

One imp ortant di�erence from MPEG concerns the quantization phase. In its original

form, MPEG-I did not supp ort JPEG's variable quantization table. Rather, all co e�cients

were scaled by a single constant value. MPEG-I I restored variable, nonuniform quantization.

.. MPEG Enco ding: P-Frames

P-frames are sub divided into macroblo cks using the same technique describ ed ab ove.

However, we will not enco de the macroblo cks directly. Rather, we will attempt to enco de

the di�erence b etween each macroblo ck and a similar macroblo ck from an earlier frame.

For each macroblo ck in the current (\target") frame, we search for a matching group of

pixels in the preceding (\reference") I-frame or P-frame. In many cases, we may �nd an


-----

Figure : P-frame enco ding.


-----

excellent match at the same p osition in the reference frame. If that region of the frame

represents static background scenery, it will likely b e unchanged from target to reference.

In general, though, we wish to accommo date motion. Thus, we search for a go o d target

match throughout some larger region of the reference image. Ultimately, we will �nd our

b est match at some (x, y) o�set from the p osition of our target macroblo ck. This o�set, or

\motion vector", is Hu�man enco ded for each target macroblo ck.

The motion vector may direct us to the b est match, but it is unlikely to direct us to a

set of pixels that are truly identical. Here we use di�erence co ding. We form a macroblo ck

representing the di�erence b etween the target macroblo ck and b est-match reference mac
roblo ck. This di�erence macroblo ck is enco ded using the same JPEG technique used for

I-frame macroblo cks: DCT, quantize, RLE, etc.

In practice, the search for a go o d match for each target macroblo ck is the most com
putationally di�cult part of MPEG enco ding. With current technology, realtime MPEG

enco ding is only p ossible with the help of custom hardware. Note, though, that while the

search for a match is extremely di�cult, using the motion vector so derived is as simple as

extracting a �xed-size blo ck of pixels given an (x, y) o�set into a bu�ered frame. Enco ders

are hard; deco ders are easy.

One �nal p oint: it is entirely p ossible that for some target macroblo ck, we will �nd no

similar region in the reference frame. Should this happ en, we simply give up on di�erence

co ding for that blo ck. We omit the motion vector and JPEG-enco de the target macroblo ck

directly. In a sense, we have fallen back onto I-frame co ding for just that macroblo ck.

.. MPEG Enco ding: B-Frames

B-frames were not present in MPEG's predecessor, H.. They were added in an e�ort

to address the following situation: p ortions of an intermediate P-frame may b e completely

absent from all previous frames, but may b e present in future frames. For example, consider

a car entering a shot from the side. Supp ose an I-frame enco des the shot b efore the car

has started to app ear, and another I-frame app ears when the car is completely visible. We

would like to use P-frames for the intermediate scenes. However, since no p ortion of the car

is visible in the �rst I-frame, the P-frames will not b e able to \reuse" that information. The

fact that the car is visible in a later I-frame do es not help us, as P-frames can only lo ok back

in time, not forward.

B-frames lo ok for reusable data in b oth directions. The overall technique is identical to

that used in P-frames. For each macroblo ck in the target image, search for a similar collection

of pixels in the reference. However, whereas P-frames searched in only the preceding I- or P
frame, B-frames also search in the succeeding I- or P-frame. We �nd the b est match in each

frame, and record b oth. The b est match in the previous frame is enco ded as a backward
predicted motion vector; the b est match in the next frame is enco ded as a forward-predicted

motion vector.

Recall that a P-frame also enco des the di�erence b etween the target and the reference.

B-frames have two motion vectors, and therefore two references. We simply merge the two

reference blo cks and enco de the di�erence b etween this average and our target.


-----

Figure : B-frame enco ding.


-----

Like P-frames, B-frames may fail to �nd a go o d match in either the forward or backward

reference. Should this happ en, we omit that motion vector and rely exclusively up on the

other. In a sense, we will have fallen back on P-frame or backward P-frame co ding for just

that macroblo ck. If no go o d match can b e found in either direction, we directly enco de the

raw target macroblo ck as though for an I-frame.

.. MPEG Compression E�ectiveness

How e�ective is MPEG compression? We can examine typical compression ratios for each

frame typ e, and form an average weighted by the ratios in which the frames are typically

interleaved.

Starting with a  � 0 pixel, -bit color image, typical compression ratios for MPEG-I

are:

Typ e Size Ratio

I  Kb :

P  Kb 0:

B . Kb 0:

Avg . Kb :

If one  � 0 frame requires . Kb, how much bandwidth do es MPEG require in

order to provide a reasonable video feed at thirty frames p er second?

0f r ames=sec � :K b=f r ame � b=bit = :M bits=sec

Thus far, we have b een concentrating on the visual comp onent of MPEG. Adding a stereo

audio stream will require roughly another 0. Mbits/sec, for a grand total bandwidth of

. Mbits/sec.

This �ts nicely within the . Mbit/sec capacity of a T line. In fact, this sp eci�c limit

was a design goal in the formation of MPEG. Real-life MPEG enco ders track bit rate as

they enco de, and will dynamically adjust compression qualities to keep the bit rate within

some user-selected b ound. This bit-rate control can also b e imp ortant in other contexts. For

example, video on a multimedia CD-ROM must �t within the relatively p o or bandwidth of

a typical CD-ROM drive.

.. MPEG in the Real World

MPEG has found a numb er of applications in the real world, including:

. Direct Broadcast Satellite. MPEG video streams are received by a dish/deco der, which

unpacks the data and synthesizes a standard NTSC television signal.

. Cable Television. Trial systems are sending MPEG-I I programming over cable televi
sion lines.


-----

. Media Vaults. Silicon Graphics, Storage Tech, and other vendors are pro ducing on
demand video systems, with twenty �le thousand MPEG-enco ded �lms on a single

installation.

. Real-Time Enco ding. This is still the exclusive province of professionals. Incorp orating

sp ecial-purp ose parallel hardware, real-time enco ders can cost twenty to �fty thousand

dollars.

 Other Lossy Transform Co des

. Wavelet Compression

.. Wavelet Intro duction

JPEG and MPEG decomp ose images into sets of cosine waveforms. Unfortunately, cosine is a

p erio dic function; this can create problems when an image contains strong ap erio dic features.

Such lo cal high-frequency spikes would require an in�nite numb er of cosine waves to enco de

prop erly. JPEG and MPEG solve this problem by breaking up images into �xed-size blo cks

and transforming each blo ck in isolation. This e�ectively clips the in�nitely-rep eating cosine

function, making it p ossible to enco de lo cal features.

An alternative approach would b e to cho ose a set of basis functions that exhibit go o d

lo cality without arti�cial clipping. Such basis functions, called \wavelets", could b e applied

to the entire image, without requiring blo cking and without degenerating when presented

with high-frequency lo cal features.

How do we derive a suitable set of basis functions? We start with a single function,

called a \mother function". Whereas cosine rep eats inde�nitely, we want the wavelet mother

function, �, to b e contained within some lo cal region, and approach zero as we stray further

away:


lim

x!�


�(x) = 0


The family of basis functions are scaled and translated versions of this mother function.

For some scaling factor s and translation factor l,

s


�


(x) = �(


x � l )


sl

.. Haar Wavelets

Haar wavelets are derived from the following mother function:



><  : 0 < x � =


�(x) =


>:


� : = < x � 

0 : x � 0 or x  - 


Figure  shows a family of seven Haar basis functions. Of the many p otential wavelets,

Haar wavelets are probably the most describ ed but the least used. Their regular form makes


-----

�00 =�(x)


###### 1

|1|Col2|
|---|---|
|||
|||


�0 =�(x)

###### ½

�0 =�(x)

###### ¼


�

�

###### ¼


=�(x�)

###### ½

=�(x�)

###### ½


###### 1

|Col1|Col2|
|---|---|
|½||

|½|Col2|
|---|---|
|||
|||


�


=�(x�)

###### ¾

 ½


�


=�(x�)

|Col1|½|
|---|---|
|¼||

|Col1|¾|
|---|---|
|½||

|Col1|1|
|---|---|
|||

|¼|Col2|
|---|---|
|||
|||


Figure : A small Haar wavelet family of size seven.


-----

###### 0.06 0.05 0.04 0.03 0.02 0.01 0 -0.01 -0.02

 0.05

 0


###### 0 500 1000 1500 2000 2500


###### 0.06
 0.05 Coiflet_3

 0.04

 0.03

 0.02

 0.01

 0

 -0.01
 0 500 1000 1500 2000 2500

 0.06 0.05 Symmlet_6 0.04 0.03 0.02 0.01 0 -0.01 -0.02 0 500 1000 1500 2000 2500


###### -0.05 0 100 200 300 400 500 600


Figure : A sampling of p opular wavelets.

the underlying mathematics simple and easy to illustrate, but tends to create bad blo cking

artifacts if actually used for compression.

Many other wavelet mother functions have also b een prop osed. The Morret wavelet

convolves a Gaussian with a cosine, resulting in a p erio dic but smo othly decaying function.

This function is equivalent to a wave packet from quantum physics, and the mathematics of

Morret functions have b een studied extensively. Figure  shows a sampling of other p opular

wavelets. Figure  shows that the Daub echies wavelet is actually a self-similar fractal.

.. Wavelets in the Real World

Summus Ltd. is the premier vendor of wavelet compression technology. Summus claims to

achieve b etter quality than JPEG for the same compression ratios, but has b een loathe to

divulge details of how their wavelet compression actually works. Summus wavelet technology

has b een incorp orated into such items as:

� Wavelets-on-a-chip for missile guidance and communications systems.

� Image viewing plugins for Netscap e Navigator and Microsoft Internet Explorer.

� Desktop image and movie compression in Corel Draw and Corel Video.

� Digital cameras under development by Fuji.


-----

###### 0.07

 0.06

 0.05

 0.04

 0.03

 0.02

 0.01

 0

 -0.01


###### 3 [x 10-3]


###### -0.02 0 500 1000 1500 2000 2500

Figure : Self-similarity in the Daub echies wavelet.

In a sense, wavelet compression works by characterizing a signal in terms of some un
derlying generator. Thus, wavelet transformation is also of interest outside of the realm of

compression. Wavelet transformation can b e used to clean up noisy data or to detect self
similarity over widely varying time scales. It has found uses in medical imaging, computer

vision, and analysis of cosmic X-ray sources.

. Fractal Compression

.. Function Fixed Points


A function f (x) is said to have a �xed p oint xf


if xf


= f (xf


). For example:


f (x) = ax + b

b


) xf


=


 � a

This was a simple case. Many functions may b e to o complex to solve directly. Or a

function may b e a black b ox, whose formal de�nition is not known. In that case, we might

try an iterative approach. Keep feeding numb ers back through the function in hop es that

we will converge on a solution:


x0

xi


= guess

= f (xi� )


For example, supp ose that we have f (x) as a black b ox. We might guess zero as x0

iterate from there:


and


-----

x0

x

x

x

x

x

x

x

x


= 0

= f (x0

= f (x

= f (x

= f (x

= f (x

= f (x

= f (x

= f (x


) = 

) = :

) = :

) = :

) = : 

) = : 

) = : 

) = : 


In this example, f (x) was actually de�ned as =x + . The exact �xed p oint is , and

the iterative solution was converging up on this value.

Iteration is by no means guaranteed to �nd a �xed p oint. Not all functions have a single

�xed p oint. Functions may have no �xed p oint, many �xed p oints, or an in�nite numb er

of �xed p oints. Even if a function has a �xed p oint, iteration may not necessarily converge

up on it.

.. Fractal Compression and Fixed Points

In the ab ove example, we were able to asso ciate a �xed p oint value with a function. If

we were given only the function, we would b e able to recompute the �xed p oint value.

Put di�erently, if we wish to transmit a value, we could instead transmit a function that

iteratively converges on that value.

This is the idea b ehind fractal compression. However, we are not interested in transmit
ting simple numb ers, like \". Rather, we wish to transmit entire images. Our �xed p oints

will b e images. Our functions, then, will b e mappings from images to images.

Our enco der will op erate roughly as follows:

. Given an image, i, from the set of all p ossible images, I mag e.

. Compute a function f : I mag e ! I mag e such that f (i) � i.

. Transmit the co e�cients that uniquely identify f .

Our deco der will use the co e�cients to reassemble f and reconstruct its �xed p oint, the

image:

. Receive co e�cients that uniquely identify some function f : I mag e ! I mag e.

. Iterate f rep eatedly until its value converges on a �xed image, i.

. Present the decompressed image, i.


-----

Figure : Identifying self-similarity. Range blo cks app ear on the left; one domain blo ck

app ears on the left. The arrow identi�es one of several collage function that would b e

comp osited into a complete image.

Clearly we will not b e using entirely arbitrary functions here. We want to cho ose functions

from some family that the enco der and deco der have agreed up on in advance. The memb ers

of this family should b e identi�able simply by sp ecifying the values for a small numb er of

co e�cients. The functions should have �xed p oints that may b e found via iteration, and

must not take unduly long to converge.

The function family we cho ose is a set of \collage functions", which map regions of an

image to similar regions elsewhere in the image, mo di�ed by scaling, rotation, translation,

and other simple transforms. This is vaguely similar to the search for similar macroblo cks

in MPEG P- and B-frame enco ding, but with a much more �exible de�nition of similarity.

Also, whereas MPEG searches for temp oral self-similarity across multiple images, fractal

compression searches for spatial self-similarity within a single image.

Figure  shows a simpli�ed example of decomp osing an image info collages of itself. Note

that the enco der starts with the sub divided image on the right. For each \range" blo ck, the

enco der searchers for a similar \domain" blo ck elsewhere in the image. We generally want

domain blo cks to b e larger than range blo cks to ensure go o d convergence at deco ding time.

.. Fractal Compression in the Real World

Fractal compression using iterated function systems was �rst describ ed by Dr. Michael

Barnsley and Dr. Alan Sloan. Although they claimed extraordinary compression rates, the

computational cost of enco ding was prohibitive. The ma jor vendor of fractal compression

technology is Iterated Systems, cofounded by Barnsley and Sloan.

To day, fractal compression app ears to achieve compression ratios comp etitive with JPEG

at reasonable enco ding sp eeds. Details on Iterated's current techniques are, sadly, few and

far b etween.

Fractal compression describ es an image in terms of itself, rather than in terms of a pixel

grid. This means that fractal images can b e somewhat resolution-indep endent. Indeed, one

can easily render a fractal image into a �ner or coarser grid than that of the source image.

This resolution indep endence may have use in presenting quality images across a variety of


-----

screen and print media.

. Mo del-Based Compression

We brie�y present one last transform co ding scheme, mo del-based compression. The idea

here is to characterize the source data in terms of some strong underlying mo del. The p opular

example here is faces. We might devise a general mo del of human faces, describing them in

terms of anatomical parameters like nose shap e, eye separation, skin color, cheekb one angle,

and so on. Instead of transmitting the image of a face, we could transmit the parameters

that de�ne that face within our general mo del. Assuming that we have a suitable mo del for

the data at hand, we may b e able to describ e the entire system using only a few bytes of

parameter data.

Both sender and receiver share a large b o dy of a priori knowledge contained in the mo del

itself (e.g., the fact that faces have two eyes and one nose). The more information is shared

in the mo del, the less need b e transmitted with any given data set. Like wavelet compres
sion, mo del-based compression works by characterizing data in terms of a deep er underlying

generator. Mo del-based enco ding has found applicability in such areas as computerized

recognition of four-legged animals or facial expressions.


-----

Algorithms in the Real World Notes by Tzu-Yi Chen

Lecture # (Cryptography ) �c   Tzu-Yi Chen and Guy Blello ch

� Cryptography

. De�nitions and Primitives

. Proto cols

(a) Digital Signatures

(b) Key Exchange

(c) Authentication

(d) Some Other Proto cols

. Symmetric (private-key) Algorithms

(a) Symmetric Ciphers

i. Blo ck Ciphers

(b) DES (Data Encryption Standard)

In the original class the �rst  minutes was sp ent on Fractal and mo del compression.

This material was incorp orated into the lecture notes of the previous class.

 De�nitions and Primitives

Like compression, this is a large �eld in its own right. In this class we fo cus on the algorithmic

asp ects of the �eld, paying little or no attention to other issues such as p olitics.

We b egin with a series of basic de�nitions, building up to some primitives.

. De�nitions

Cryptography General term referring to the �eld.

Cryptology The mathematics b ehind cryptography.

Encryption Enco ding. Sometimes this is used as a general term.

Cryptanalysis The breaking of co des.

Steganography The hiding of messages. This is an emerging �eld which studies the hiding

of messages inside messages. A simple example is the hiding of a watermark in a piece

of pap er.

Cipher A metho d or algorithm for encrypting and decrypting.


-----

Figure : Flowchart showing the encryption and decryption of a message.

A few more terms are b est describ ed with the aid of Figure . Referring to Figure ,

algorithms in which the two keys key and key are the same are often called symmetric

or private-key algorithms (since the key needs to b e kept private) and algorithms in which

the two keys are di�erent are often called asymmetric or public-key algorithms (since either

key or key can b e made public dep ending on the application).

Next we list some commonly used names : : : each name represents a sp eci�c role.

Alice initiates a message or proto col.

Bob second participant.

Carol third participant.

Trent trusted middleman.

Eve eavesdropp er.

Mallory malicious active attacker.

Finally we de�ne security by asking ourselves what it means to b e secure. There are two

de�nitions.

Truly Secure An algorithm is truly secure if encrypted messages cannot b e deco ded with
out the key.

In   Shannon proved that for something to b e truly secure, the key must b e as long

as the message. Informally, the intuition is that something is not secure if the message

contains more information than the key.

An example of a secure algorithm is the one-time-pad in which the enco der and deco der

b oth have the same random key which is the same length as the message. The enco der

XORs the message with the key, the deco der then deco des the message by XORing what

he receives with the same random key. Each random key can only b e used once.

Security Based on Computational Cost Here something is secure if it is \infeasible"

the break | meaning that no (probabilistic) p olynomial time algorithm can deco de a

message.


-----

Notice that if P = N P, nothing is secure based on computational cost since we could

e�ectively nondeterministically try all keys.

. Primitives

Here we de�ne several primitives, giving examples of most.

One-way Functions A one-way function y = f (x) is a function where it is easy to compute

y from x, but \hard" to compute x from y . One-way functions can b e further classi�ed based

on the meaning of the word \hard".

Strong A strong one-way function f is one where for most y, no single p olynomial time



algorithm can compute x (i.e.  � jxjk ).

Weak A weak one-way function f is one where for a reasonable numb er of y no single



p olynomial time algorithm can compute x (i.e. jxjk ).

Some examples of one-way functions are the following:

Factoring y = u � v, where u and v are primes. If u and v are primes, it is hard to generate

them from y .


p olynomial time algorithm can compute x (i.e.


).


x











Discrete Log y = g


mo d p, where p is a prime and g is a generator (i.e. g


; g


; g


; : : :


generate all i such that 0 � i < p. This is b elieved to b e ab out as hard as factoring.

DES with a �xed message y = DES x (M ).

Note that these are only conjectured to b e one-way functions.

One-way Trap do or Functions This is a one-way function with a \trap do or". The

trap do or is a key that makes it easy to invert the function.

e


An example is RSA, where the function is y = x


mo d N, where N = p � q . p,q, and e are


prime, p and q are trap do ors (only one is needed). So, in public-key algorithms, f (x) is the

public key (e.g. e, N ), whereas the trap do or is the private key (e.g. p or q ).

One-way Hashing Functions A one-way hashing function is written y = H (x). H is a

many-to- function, and y is often de�ned to b e a �xed length (numb er of bits) indep endent

of the length of x. The function H is chosen so that calculating y from x is easy, but given

a y calculating any x such that y = H (x) is \hard".

 Proto cols

Here we describ e a numb er of basic proto cols, showing p ossible implementations. We note

that in general a proto col which can b e implemented using a symmetric (private-key) cryp
tosystem can also b e implemented using an asymmetric (public-key) cryptosystem | a

primary di�erence is that the former may require a trusted middleman.


-----

. Digital Signatures

Digital signatures can b e used to:

� Convince a recipient of the author of a message.

� Prove authorship.

� Make tamp ering with a signed message without invalidating the signature di�cult.

They can b e implemented b oth using symmetric and asymmetric cryptosystems as illustrated

b elow.

###### Trent
 E  (M)KA E  (M+Signature)KB

 Alice Bob

Figure  : Flowchart showing an implementation of digital signatures using a symmetric

cryptosystem.

Using a symmetric Cyptosystem: In Figure  Alice and Trent share the private key

|Trent (M) E (M K A B Alice Bob|Col2|
|---|---|
|Alice|Bob|


KA


and Bob and Trent share the private key K


B


. Trent (a trusted middleman) receives


a message from Alice which he can decrypt using KA . Because he can decrypt it using


KA


, he knows Alice sent the message. He now encrypts the deco ded message plus


a signature saying that Alice really sent this message using KB


. He sends this new


version to Bob, who can now deco de it using the key KB


.

|Col1|E  (M)|Col3|
|---|---|---|
|Alice|E (M) K I|Bob|
||||


Figure 0: Flowchart showing an implementation of digital signatures using an asymmetric

cryptosystem.


Using an asymmetric Cyptosystem: In Figure 0 KI


is Alice's private key. Bob de

crypts the message using her public key. The act of encrypting the message with a

private key that only Alice knows represents her signature on the message.

The following is a more e�cient implementation using an asymmetric cryptosystem.

In Figure  H (M ) is a one-way hash of M . Up on receiving M, Bob can verify that it


indeed come from Alice by decrypting H (M ) using Alice's public key K

that M do es in fact hash to the value encrypted.


and checking


I


-----

|Col1|E  (H(M)) + M|Col3|
|---|---|---|
|Alice|E (H(M)) + M K I|Bob|
||||


Figure : Flowchart showing a more e�cient implementation of digital signatures using an

asymmetric cryptosystem.

. Key Exchange

These are proto cols for exchanging a key b etween two p eople. Again, they can b e imple
mented b oth with symmetric and asymmetric cryptosystems as follows:

###### Trent generates k
 E  (k)KA E  (k)KB

 Alice Bob

Figure : Flowchart showing an implementation of key exchange using a symmetric cryp
tosystem.

Using a symmetric Cyptosystem: In Figure , Alice and Trent share the private key

|Trent generates k E (k) E (k) K K A B Alice Bob|Col2|
|---|---|
|Alice|Bob|


KA


and Bob and Trent share the private key KB


. Trent generates a key k, then enco des


k with KA


to send to Alice and enco des k with KB


to send to Bob.

|Alice generates k|E (k) K I|Bob|
|---|---|---|
||||


Figure : Flowchart showing an implementation of key exchange using an asymmetric

cryptosystem.


Using an asymmetric Cyptosystem: In Figure  KI


is Bob's public key. Alice gener

ates a key k, which she encrypts with Bob's public key. Bob decrypts the message

using his private key.

. Authentication

These proto cols are often used in password programs (e.g. the Unix passwd function) where

a host needs to authenticate that a user is who they say they are.

Figure  shows a basic implementation of an authentication proto col. Alice sends p to

the host. The host computes f (p). The host already has a table which has y and checks to

see that f (p) = y . f is a one-way function.


-----

|p Alice|Host f(p) =? y y stored in table|
|---|---|


Figure : Flowchart showing a basic implementation of an authentication proto col.

To make it less likely that Mallory will b e able to pretend to b e Alice to the host, sequences

of passwords can b e used. Sequences of passwords are used by having Alice give the host

n


a random numb er R. The host computes x0


= R; x


= f (R); x


= f (f (R)); : : : xn


= f


(R)


and gives all but x


. Now, the �rst time Alice logs in, she uses


n


to Alice. The host keeps xn


xn�


as the password. The host computes f (xn�


) and compares it to the x


which it has.


n


If the two are equivalent, Alice has b een authenticated. Now the host replaces xn


with x


n�


.


The next time Alice logs in, she uses xn�


. Because each password is only used once by


Alice, and f is a one-way function, sequences of passwords are more secure.

. Some Other Proto cols

Some other proto cols which are not discussed here are:

� Secret sharing

� Timestamping services

� Zero-knowledge pro ofs

� Blind-signatures

� Key-escrow

� Secure-elections

� Digital Cash

 Symmetric (private-key) Algorithms

We discuss blo ck ciphers and then brie�y intro duce the well known and widely used blo ck

cipher DES. We b egin discussion of how DES works, saving much for the next lecture.

. Symmetric Ciphers (Blo ck Ciphers)

Blo ck ciphers divide the message to b e encrypted into blo cks (e.g.  bits each) and then

convert one blo ck at a time. Hence:

0


Ci


= f (k ; Mi


) Mi


= f


(k ; Ci


)


-----

Notice that if Mi


= M


j


= C


j


. This is undesirable b ecause if someone (Eve or Mallory)


, Ci


notices the same blo ck of co de going by multiple times, they know that this means identical

blo cks were co ded. Hence they've gained some information ab out the original message.

There are various ways to avoid this. For example, something called cipher block chaining

(CBC) encrypts as follows.


Ci


= Ek (Ci�


� Mi


)


This has the e�ect that every co de word dep ends on the co de works that app ear b efore it

and are therefore not of any use out of context. Cipher blo ck chaining can b e decrypted as

follows.


Mi


= Ci�


� Dk


(Ci


)


Unfortunately, this could still cause problems across messages. Note that if two messages

b egin the same way, their enco dings will also b egin the same way (but once the two messages

di�er, their enco dings will b e di�erent from then on). Because many messages that p eople

want to send b egin with standard headers (e.g. sp ecifying the typ e of �le b eing sent), this

means someone could gain information ab out the message b eing sent by creating a table of

all the encrypted headers that they have seen. One way to �x this problem is to attach a

random blo ck to the front of every message.

. DES (Data Encryption Standard)

DES was designed by IBM for NIST (the National Institute of Standards and Technology)

with \consultation" from the NSA in  .

DES uses -bit blo cks and -bit keys. It is still used heavily, for example by banks

when they encrypt the PIN that you typ e in at an ATM machine. However, DES is no

longer very safe | sup ercomputers can crack it in a few hours. Nevertheless, b ecause it is

so common, we describ e how it works here, b eginning by describing some of the computing

comp onents used in DES.

Sp eci�cally, we describ e some bit manipulations:

Substitution A �xed mapping. For example:

000 ! 0

00 ! 0

00 ! 000

0 ! 00

00 ! 00

.

.

.

This is often stored as a table.

Permutation A rearrangement of order. For example:


b0


b


b


b b


! b


b b


b0


b


This is also often stored as a table.


-----

Expansion Permutation A rearrangement of order that may rep eat some bits of the input

in the output. For example:


b0


b


b


b


! b


b


b


b0


b


b0


-----

Algorithms in the Real World Notes by David Opp enheimer

Lecture # (Cryptography ) �c   David Opp enheimer and Guy Blello ch

Outline

� Why do DES and other blo ck ciphers work?

� Di�erential and linear cryptanalysis

� Sample blo ck cipher: IDEA

� Sample stream cipher: RC

� Public-key algorithms

{ Merkle-Hellman Knapsack Algorithm

{ RSA

 Blo ck ciphers

Blo ck ciphers encrypt plaintext in blo cks and decrypt ciphertext in blo cks.

. Feistel networks

Many blo ck ciphers take the form of Feistel networks. The structure of a Feistel network is

illustrated in Figure .

In a Feistel network, the input is divided evenly into a left and right blo ck, and the output

of the i'th round of the cipher is calculated as


Li

Ri


= Ri�

= Li�


� f (Ri�


; Ki


)


The go o d prop erty of Feistel networks is that f can b e made arbitrarily complicated, yet

the input can always b e recovered from the output as


Ri�

Li�


= Li

= Ri


� f (Li


; Ki


)


Therefore even if f is not invertible, the algorithm itself will b e invertible, allowing for


decryption (if you know the Ki


's, of course).


Feistel networks are part of DES, Lucipher, FEAL, Khufu, LOKI, GOST, Blow�sh, and

other blo ck cipher algorithms. You can see the Feistel structure in one round of DES, which

is depicted in Figure .


-----

###### L i-1 R i-1

 f

 L i R i

Figure : Feistel Network


###### Ki


###### (Schneier, figure 12.2)

Figure : One round of DES (there are  rounds all together).


-----

. Security and Blo ck Cipher Design Goals

This raises the question of how to design f so that the cipher is secure.

Confusion, di�usion, and the avalanche e�ect are three goals of blo ck cipher design.

Confusion decorrelates the output from the input. This can b e achieved with substitutions.

Di�usion spreads (di�uses) the correlations in the input over the output. This can b e

achieved with permutations: the bits from the input are mixed up and spread over the

output. A go o d blo ck cipher will b e designed with an avalanche e�ect, in which one input

bit rapidly a�ects all output bits, ideally in a statistically even way. By \rapidly" we mean

after only a few rounds of the cipher.

The ideal f for a blo ck cipher with -bit blo cks would b e a totally random -bit ! 






� 


0

= 


bit key-dep endent substitution. Unfortunately this would require a table with 




entries for a cipher with -bit keys (like DES): for each of the 




keys you'd need a mapping


from each of the 


p ossible inputs to the appropriate -bit output.


Since this would require to o much storage, we approximate the ideal by using a pseu
dorandom mapping with substitutions on smaller blo cks. An algorithm that rep eatedly

p erforms substitutions on smaller blo cks (so the storage requirements for the mapping are

feasible) and permutations across blo cks is called a substitution-permutation network. This

is an example of a product cipher b ecause it iteratively generates confusion and di�usion. A

cipher with the same structure in each round, rep eated for multiple rounds, is called an iter
ated block cipher. DES is an example of an iterated blo ck cipher, a substitution-p ermutation

network, and a pro duct cipher.

. DES Security

DES was designed with the ab ove goals in mind. It was also designed to resist an attack

called di�erential cryptanalysis, which was not publicly known at the time.

.. E-b ox and P-b ox

The DES E-box (lab eled as the expansion p ermutation in Figure ) takes  bits as input

and pro duces  bits as output as shown in Figure . The  output bits are the  input

bits with some of the input bits rep eated. In particular, for each blo ck of  input bits, the

�rst and fourth bits app ear twice in the output while the two middle bits app ear once. The

E-b ox therefore enhances the avalanche e�ect, b ecause  outputs from an S-b ox in round R

will b ecome the input to  S-b oxes in round R+. The E-b ox also enables the use of  bits

of the key in the XOR op eration that follows the E-b ox.

The DES P-Box is a straight -bit p ermutation (every input bit is used exactly once in

the output)

.. S-b ox

There are  S-b oxes; each takes six bits as input and pro duces  bits as output. Some

imp ortant security prop erties of the S-b oxes are

� The output bits are not a linear function of the inputs, nor close to a linear function


-----

###### 32

 48


###### 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16

 1 2 3 4 5 6 7 8 9 10 1112 1314 15 16 1718 1920 21 22 2324

 (Schneier fig. 12.3)

Figure : The DES E-b ox

|2 8|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Col10|Col11|Col12|Col13|Col14|Col15|Col16|Col17|Col18|Col19|Col20|Col21|Col22|Col23|Col24|Col25|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
||||||||||||||||||||||||||
||||||||||||||||||||||||||


� A di�erence of  bit in the input to an S-b ox a�ects at least  bits in the output


� For any -bit input di�erence i


, no more than  of the  p ossible input pairs





� i


with di�erence i


� i





may result in the same output di�erence.


We will see that this last prop erty is imp ortant in making DES resistant to di�erential

cryptanalysis.

.. Weaknesses of DES




� Some keys are insecure. Of the 


p ossible DES keys,  of them are p o or choices.


Luckily this is few enough that a DES encryption program can check to see if the key

you want to use is one of these bad keys, and if so tell you not to use it.

{ Weak keys: There are four weak keys: 0x00000000 000 000, 0x0000000FFFFFFF,

0xFFFFFFF0000000, and 0xFFFFFFFFFFFFFF. When you use a weak key, the

subkey used in each DES round is identical. This makes cryptanalysis a lot easier.


It also makes Ek


(X ) = Dk


(X ) since DES decryption follows the same algorithm


as encryption but uses the subkeys in the reverse order. (If the subkeys are all

the same, then obviously the forward and reverse order of them are identical.)

{ Semiweak keys: There are twelve semiweak keys. When you use a semiweak key,

there are only two di�erent subkeys used among the  DES rounds (each unique

subkey is used  times). This makes cryptanalysis easier.

{ Possibly weak keys: There are forty-eight possibly weak keys. When you use a

p ossibly weak key, there are only four unique subkeys generated; each one is used

 times. Again, this makes cryptanalysis easier.


-----

###### a1


###### S-Box 5


###### b0 b1 b2 b 3

Figure : S-Box 

� S-b ox  is strongly biased. Refer to Figure . b0


� b


� b


� b


= a


for  of the


 p ossible inputs to S-b ox . Ideally this should b e true for exactly half () of the

p ossible inputs. Linear cryptanalysis can take advantage of this bias.

.. DES in the Real World

DES is used frequently in the \real world."

� Banks

{ bank machines

{ inter-bank transfers

� ISDN (some)

� Kerb eros

� Unix password authentication (almost)

� Privacy-enhanced mail (PEM)

DES is not used in many newer systems b ecause of the small -bit keysize. However,

triple-DES (or -DES) provides signi�cantly more security while still using the DES algo
rithm. The basic idea is to encrypt multiple times using di�erent keys. In -DES,

C = EK  (DK  (EK  (P )))

P = DK  (EK  (DK  (C )))

Note that you cannot simply use C = EK  (EK  (P )) for DES (or any other blo ck al

gorithm) and get much b etter security than simply using one key. If the algorithm is a


group, then this is completely equivalent to saying C = E


K  (P ) for some K


and you have


gained nothing. If the algorithm is not a group, there is a sp ecial attack which lets you �nd


n+

the key in 


encryptions for an algorithm with an n-bit key, instead of the exp ected 


n


encryptions. DES is not a group.


-----

Figure  : Di�erential Cryptanalysis

. Di�erential Cryptanalysis


De�ne �V = V


� V


and �Y = Y





.


� Y


Refer to Figure  which shows part of one round of DES. The basic idea b ehind di�er
ential cryptanalysis is that for any given �V, not all values of �Y are equally likely. If a

cryptanalyst is able to force someone to encrypt a pair of plaintext messages with a �V that

he knows, he can lo ok at the corresp onding pair of encrypted messages, compute their �Y,


and use �V, �Y, and the V 's to get some information ab out K ey


. Of course, you need


i

lots of pairs of messages b efore the deltas b ecome statistically signi�cant enough to give you

information ab out the key.

This idea is applied one round at a time. The more rounds there are in the cipher,

the harder it is to derive the original key using this technique b ecause the statistical bias

decreases with each round.

Di�erential cryptanalysis makes -round DES signi�cantly easier to break than brute

force, but has little e�ect on the security of -round DES. The designers of DES knew

ab out di�erential cryptanalysis and designed the S-b oxes (and chose the numb er of rounds)

to resist this attack.

. Linear Cryptanalysis

Linear cryptanalysis allows an attacker to gain some information ab out one bit of a key if

he knows a plaintext and its corresp onding ciphertext. The idea is that (the XOR of some

plaintext bits) � (the XOR of some ciphertext bits), a one-bit by one-bit XOR that gives

you a one-bit result, gives you information ab out the XOR of some of the key bits. This

works when there is a bias in the linear approximation for an S-b ox. S-b ox  is the most

biased S-b ox for DES.


-----

###### i bit 26 of
 26
 round i’s key

 a
 26

 S-box 5

 b b b b
 17 18 19 20

Figure 0: Linear Cryptanalysis using S-Box 

Refer to Figure 0 which shows the op eration of S-b ox . If you use linear cryptanalysis,

|S-box 5|Col2|Col3|
|---|---|---|
||||


knowing something ab out i


(the second input bit to S-b ox , if we numb er input bits to


the array of S-b oxes starting with bit  on the left) and b


, b


, and b0


(the seventeenth





, b


through twentieth output bits from the array of S-b oxes) will tell you something ab out the


'th bit of the key used in that round. This is b ecause () i


is the XOR of the 'th bit of


the key used in that round, with the 'th bit of the output from the expansion p ermutation

for that round (which you know if you know the input bits to that round), and () S-b ox


 has the following statistical bias: i


� b





� b0


for only  of the  p ossible





= b


� b


inputs to S-b ox . Armed with enough plaintext-ciphertext pairs, linear approximations for

the S-b oxes, and a mo del of the S-b oxes' biases, you can do statistical analysis to learn ab out

the key.

Linear cryptanalysis is the most successful attack on DES. Still, it's not much b etter

than a brute force key search.

. IDEA

IDEA, illustrated in Figure , is another blo ck cipher. It op erates on -bit blo cks and uses

-bit keys. IDEA is a pro duct cipher. It comp oses three algebraic groups:

� Addition (which provides the di�usion prop erty)

� Multiplication (which provides the confusion prop erty)

� XOR

IDEA has some weak keys, but they're not weak in the same sense as DES keys. (If you

use a weak IDEA key, an attacker can �gure out which key you used by using a chosen



plaintext attack.) There are 


weak IDEA keys, but since there are so many more p ossible


-----

###### X1 X2 X3 X4

 Z1(1) Z2(1) Z3(1) Z4(1)

 one round Z5(1)

 Z6(1)

 seven more rounds

 Z1(9) Z2(9) Z3(9) Z4(9)

 Y1 Y2 Y3 Y4

 Xi = 16-bit plaintext subblock
 (Schneier fig. 13.9)
 Yi = 16 bit ciphertext subblock Zi(r) = 16-bit key subblock

 = bit-by-bit XOR of 16-bit subblocks
 16 = addition modulo 2  of 16-bit integers
 16 = multiplication modulo 2  + 1 of 16-bit integers with the
 zero subblock corresponding to 2[16]

Figure : The IDEA cipher

|) Z2(1) Z3(1) Z4(1) d Z5(1) Z6(1) s Z2(9) Z3(9) Z4(9) Y1 Y2 Y3 Y4 Xi = 16-bit plaintext subblock (Schneier fig. 13.9 Yi = 16 bit ciphertext subblock Zi(r) = 16-bit key subblock = bit-by-bit XOR of 16-bit subblocks 16 = addition modulo 2 of 16-bit integers 16 = multiplication modulo 2 + 1 of 16-bit integers with the|Col2|Z3(1)|Col4|Z4(1)|
|---|---|---|---|---|
||||||
|||Z5(1) Z6(1)|||
||||||


-----

IDEA keys than DES keys, the chances of picking one of these randomly is smaller than the

chance of picking one of the weak DES keys randomly.

Eight-round IDEA has sto o d up to all attacks to date. IDEA is used in PGP.

. Blo ck Cipher Encryption Sp eeds

Encryption Sp eeds of some Blo ck Ciphers on a  MHz SX

algorithm sp eed (KB/sec) algorithm sp eed (KB/sec)

Blow�sh ( rounds)  MDC (using MD) 

Blow�sh ( rounds)  MDC (using MD) 

Blow�sh (0 rounds) 0 MDC (using SHA) 

DES  NewDES 

FEAL- 00 REDOC I I 

FEAL-  REDOC I I I 

FEAL-  RC-/ 

GOST  RC-/ 

IDEA 0 RC-/ 

Khufu ( rounds)  RC-/0 

Khufu ( rounds)  SAFER ( rounds) 

Khufu ( rounds)  SAFER ( rounds) 

Luby-Racko� (using MD)  SAFER (0 rounds) 

Luby-Racko� (using MD)  SAFER ( rounds) 

Luby-Racko� (using SHA)  -Way 

Lucifer  Triple-DES 

from Schneier, Table .

 Stream ciphers

. Stream ciphers vs. Blo ck cipher

Block ciphers op erate on blo cks of plaintext; for each input blo ck they pro duce an output

blo ck. Stream ciphers usually encrypt/decrypt one bit at a time. The di�erence is illustrated

in Figure , which depicts the op eration of a typical blo ck cipher and a typical stream cipher.

Stream ciphers seem to b e more p opular in Europ e, while blo ck ciphers seem to b e more

p opular in the United States.

A stream cipher uses a function (F in the picture) that takes a key and pro duces a stream


of pseudorandom bits (bi


in the picture). One of these bits is XORed with one bit of the


plaintext input (mi


), pro ducing one bit of the ciphertext output (ci


).


A blo ck cipher mode combines the cipher algorithm itself with feedback (usually). Fig
ure  illustrates a blo ck algorithm in CBC (Cipher Blo ck Chaining) mo de. Because the

ciphertext for blo ck i- is used in calculating the ciphertext for blo ck i, identical plaintext

blo cks will not always encrypt to the same ciphertext (as is true when a blo ck algorithm is

used directly without feedback).


-----

##### Block Cipher             Stream Cipher


###### K


###### m
 i c i


###### m i


###### c state F i 0 F
 (key)
 state
 i


Figure : Blo ck v. Stream Cipher

###### K

 c m F i
 i

 c
 i-1

Figure : A blo ck cipher in CBC mo de

Blo ck ciphers are typically more e�ciently implemented in software than stream ciphers

b ecause blo ck ciphers op erate on many bits at a time.

. RC

RC is a stream cipher that generates one byte at a time. The key is used to generate a

|K|Col2|
|---|---|
|F c i-1||
|||


-element table S0


; S


; S





; : : : S


which contains a p ermutation of the numb ers 0 to .





Once this table has b een initialized, the following pseudo co de for RC generates one byte

on each round.

i=j=0

while (generating) {

i = (i+) mod 

j = (j+S_i) mod 

swap S_i and S_j

t = (S_i + S_j) mod 

output = S_t

}


-----

###### c -1
 m m F F

 K K public private

Figure : One-way trap do or function

The byte-sized output is XORed with a byte of plaintext to pro duce a byte of ciphertext

on each iteration.

RC is used in Lotus Notes, Oracle Secure SQL, and other pro ducts.

 Public-Key Algorithms

Public-key algorithms are based on one-way trap do or functions. As previously mentioned,

a one-way function is \easy" to apply in the forward direction but \hard" to apply in the

reverse direction. One-way functions with a trapdoor are \easy" to apply in the forward

direction and \hard" to apply in the reverse direction unless you know a secret. If you know

the secret, then the function is also \easy" to apply in the reverse direction.

Public key algorithms use two keys: a private key and a public key. Alice generates a

public-private keypair. She publishes her public key and keeps the corresp onding private

key private. To send Alice a message, Bob encrypts using Alice's public key. To decrypt the

message, Alice uses her private key. In contrast to symmetric encryption, two parties wishing

to communicate using a public-key algorithm don't need to meet in p erson to exchange a

secret key { they just need to lo ok up each other's public keys in the public key directory.

Exactly how to implement a secure public key distribution system (e.g. a secure public key

directory) is quite another story.

Encrypting a message with a public key can b e thought of as applying the \forward"

direction of a one-way function. The corresp onding private key is the \trap do or" that makes

the one-way function easy to reverse, allowing the encrypted message to b e decrypted. This

is illustrated in Figure .

. Merkle-Hellman Knapsack Algorithm

The Merkle-Hel l man Knapsack Algorithm is a public-key algorithm that derives its \security"

from the NP-complete knapsack problem. The designers of this algorithm b elieved that to

decrypt a message encrypted using the algorithm, a p erson would need to solve the knapsack

problem. Unfortunately they were wrong: while the knapsack problem itself is NP-complete,

|Col1|F|c|-1 F|Col5|
|---|---|---|---|---|


-----

the instances of the problem which are used for encryption using their algorithm make it

p ossible to decrypt without having to solve an NP-complete problem.

The knapsack problem says: Given a vector M of weights and a sum S, calculate the

P

b o olean vector B such that i Bi Mi = S .

How can this b e turned into a public-key algorithm? To encrypt, �rst break the input

into blo cks of size kM k bits. (M should b e a very long vector.) For each blo ck calculate

P

a sum Ci = i Bi Mi, where Bi is the plaintext. The series of Ci values calculated is the

ciphertext. The vector M used to encrypt each blo ck is the public key.

The corresp onding private key is a di�erent vector of weights; we'll call it M'. M' has the

following imp ortant prop erties: () it is a series of sup erincreasing weights (we assume M

P

0


Mi


= S { in other words, M' can also b e used to solve for B given S.


was not), and ()


Bi


i


The facts that makes this a sensible public-key algorithm are that () one can �nd B

given a sup erincreasing M' in p olynomial time, but not in p olynomial time if given only a

non-sup erincreasing M, and () it is easy to turn a sup erincreasing knapsack sequence into

a normal knapsack sequence. () Makes it easy to compute your public key once you've

selected your private key. Unfortunately, the way the authors generate the public key from

the private key makes it p ossible for an adversary to compute the private key from the public

key; the message can then b e decrypted in p olynomial time. This is the weakness in the

algorithm.

The U.S. patent on the Merkle-Hellman knapsack public key algorithm expired on August

,  .

. RSA

While Merkle-Hellman's security was based on the di�culty of solving the knapsack prob
lem, the RSA algorithm's security is based on the di�culty of factoring large numb ers (in

particular, pro ducts of large primes).

To compute a public-private keypair:

. Pick big, random primes p and q

. Calculate n = pq

. Cho ose e relatively prime to (p � )(q � ). Note that e do es not need to b e random.

�


. Calculate d = e


mo d (p � )(q � )


The public key is (e; n). The private key is (d; n).

e


To encrypt: c = m

d

To decrypt: m = c


mo d n

mo d n


We'll now show that E


(E


d


e (m)) = m.

e

Ed (Ee (m)) = (m

ed

= m


d

)


-----

= m


k (p�)(q �)+

k (p�)(q �)


= m � m

(p�)(q �)k

= m � m

k

= m � 

= m

(Note that all op erations are p erformed mod n.)

(p�)(q �)k


k


The one tricky part of this pro of is the step m � m


(mo d n) = m � 


(mo d n). This


step is explained in the next lecture after a discussion of some group theory. Brie�y, it is


b ecause kZpq

kGk


k = (p � )(q � ) and a theorem that says For al l �nite groups G, for every a


in G, a


= I, where in this case I = .


If factoring is easy, then breaking RSA b ecomes easy.


-----

Algorithms in the Real World Notes by Marat Boshernitsan

Lecture # (Cryptography ) �c   Marat Boshernitsan and Guy Blello ch

� Some group theory

� RSA summary

� ElGamal

� Probabilistic Encryption (Blum-Goldwasser)

� Quantum Cryptography

� Kerb eros case Study

 Some group theory

. Groups: Basics

A group is a set G with binary op eration � de�ned on G, such that the following prop erties

are satis�ed:

. Closure. For all a; b  G, we have a � b  G.

. Asso ciativity. For all a; b; c  G, we have (a � b) � c = a � (b � c).

. Identity. There is an element I  G, such that for all a  G, a � I = I � a = a.

. Inverse. For every a  G, there exists a unique element b  G, such that a � b =

b � a = I .

For example, integers Z under the op eration of addition form a group: identity is 0 and the

inverse of a is �a.

. Integers mo dulo n


For prime p, Zp


is a group of integers mo dulo p:


� Zp


� f; ; ; :::; p � g


� � � multiplication mo d p

� I � 


�

� a


�

� a � a


=  (mo d p)


-----

Example: Z


= f; ; ; ; ; g. Note that if p is not a prime, Zp


is not a group under �,


b ecause there isn't necessarily an inverse. All encryption algorithms assume existence of an

inverse. So, for n not prime, we de�ne:

�


� Z

n


� fm :  � m < n; g cd(n; m) = g (i.e. integers that are relatively prime to n)


� � � multiplication mo d n

� I � 


�

� a


�

� a � a

�


=  (mo d p)

�


�


�

= , 


= ,


�


Example: Z0


= f; ; ; g, 

�

Q

�


= , 

�




= . It is not to o hard to show


that the size of Zn


 �


is


p


pP


p


where P are the primes dividing n, including n if it is

�


prime. If n is a pro duct of two primes p and r, then jZ

n

. Generators (primitive elements)


j = pr ( � =p)( � =r ) = (p � )(r � ).

n


For a group G, element a  G is a generator of G if G = fa


: n  Z g (i.e. G is


\generated" by the p owers of a). For Z


we have:


Here,  and  are the generators of Z

�


while , ,  and  are not since none of them will


generate . For Z


we have:


0

�

So,  and  are the generators of Z

0


. Note that any element to the p ower of the size of the


group gives identity. In fact, there's a theorem stating that this is always true:

jGj


Theorem  For al l �nite groups G and for any a  G, a

element in G.


= I, where I is the identity


jZp j


p�

= a


= , and for two primes p and q


From this theorem, it follows that for a  Zp

�


, a


= I . The latter fact is essential for RSA.


�

and a  Z

pq


jZ

, a


j


(p�)(q �)

= a


pq


-----

. Discrete logarithms

�


If g is a generator of Zp

x


(or Zp


if p is not prime), then for all y there is a unique x such


that y = g


(mo d p). We call this x the discrete logarithm of y, and use the notation


log


(y ) = x (mo d p).


g

For Example: in Z, log


() = , but log


() = ; (no inverse), and log


() = f; g











(multiple inverses) b ecause  is not a generator of Z


.


 Public Key Algorithms (continued)

. RSA algorithm (continued)

Here are the  steps of the RSA algorithms, again

. Pick two random large primes p and q (on the order of a few hundred digits). For

maximum security, cho ose p and q to b e of the same length.

. Compute their pro duct n = pq .

. Randomly cho ose the encryption key e, such that e and (p � )(q � ) are relatively

prime. Then, �nd the decryption key d, such that ed mo d (p � )(q � ) = . I.e.,

ed = k (p � )(q � ) + , for some integer k . The numb ers e and n are the public

key, and the numb ers d and n are the private key. The original primes p and q are

discarded.

e


. To encrypt a message m: c = m

d

. To decrypt a cipher c: m = c


(mo d n).

(mo d n).


d

Why do es this work? Note that m = c


e d

= (m )


= m


ed


k (p�)(q �)+

= m


(p�)(q �)

= (m


k

)


m


(all op erations mo d n). But m is relatively prime to n (b ecause n = pq and p; q are primes),


�

and so m is in Z

n


. By the theorem in Section ., m to the p ower of the size of Z


�

n


is , so


(p�)(q �)

(m


k

)


k

m = 


e

m = m. In practice, we pick small e to make m


cheap er.


The p erformance �gures of RSA (relative to blo ck ciphers) are fairly unimpressive. Run
ning on Sparc  with -bit n, -bit e, the encryption throughput is 0.0 secs/blo ck, which

translates into  Kbits/sec. The decryption throughput is even worse with 0. secs/blo ck

( Kbits/sec). Such sp eeds are to o slow even for a mo dem. With sp ecial-purp ose hardware

(circa  ), we can b o ost the throughput to  Kbits/sec which is fast enough for a mo dem,

but is slow for pretty much everything else. In comparison, IDEA blo ck cipher implemented

in software can achieve 00 Kbits/sec. Because of its slowness, RSA is typically used to

exchange secret keys for blo ck ciphers that are then used to enco de the message.

In the \real world", the RSA algorithm is used in X.0 (ITU standard), X . (ANSI

prop osed standard), PEM, PGP, Entrust, and many other software packages.


-----

. Factoring

The security of RSA is based on the di�culty of factoring large numb ers. The state of the

art in factoring is as follows:







(+O ())(ln(n))

� Quadratic sieve (QS): T (n) = e




(ln(ln(n))) 


. This algorithm was used in  


to factor  -digit (-bit) numb er. It to ok 00 Machines  months to complete this

task.







(: +O ())(ln(n))




 (ln(ln(n)))


� Numb er �eld sieve (NFS): T (n) = e


. This algorithm is ab out


 times faster than QS on the  -digit numb er and is b etter for numb ers greater than

0 digits. It was used in   to factor 0 digit (-bit) numb er with approximately

the same amount of work as taken by QS on  -digits.

. ElGamal Algorithm

The ElGamal encryption scheme is based on the di�culty of calculating discrete logarithms.

The following are the steps of ElGamal:

. Pick a prime p.


. Pick some g, such that g is a generator for Zp .


x


. Pick random x and calculate y, such that y = g

y as the public key. The private key will b e x.


(mo d p). Now, distribute p, g, and


. To encrypt, cho ose a random numb er k, such that k is relatively prime to p � .


k


k


Calculate a = g


(mo d p) and b = y

b


m (mo d p). The cypher is the pair (a, b).


. To decrypt, calculate m =


x


(mo d p).

b


a


k


k x


m

k x


Why do es ElGamal work? Because m =


=


y m

g k x


=


g

g


= m (mo d p). To break


ax


ElGamal, one would need to either �gure out x from y or k from a. Both require calculating

discrete logs which is di�cult.

Performance-wise, ElGamal takes ab out twice the time of RSA since it calculates two

p owers. It is used by TRW (trying to avoid the RSA patent).

 Probabilistic Encryption

One of the problems with RSA encryption is that there is a p ossibility of gaining some infor

mation from public key. For instance, one could use public key Epublic


to encrypt randomly


generated messages to see if it is p ossible to get some information ab out the original message.

This problem can b e remedied by mapping every message m to multiple c randomly.


Now, even if cryptoanalist has c, m, and Epublic, she cannot tell whether c = Ek

was used to encrypt m).


(m) (i.e. k


One such probabilistic encryption scheme, Blum-Goldwasser, is based on generating

strings of random bits.


-----

. Generation Random Bits

This metho d is called Blum-Blum-Shub (BBS) and is based on the di�culty of factoring:

given a single bit, predicting the next bit is as hard as factoring. Here are the steps:

. Pick primes p and q, such that p mo d  = q mo d  = .

. Calculate n = pq (called Blum integer).

. For each m we want to encrypt, cho ose random seed x that is relatively prime to n

(g cd(x; n) = ).

. The state of the algorithm is calculated as follows:




� x0

� xi

th

. The i


= x



= x

i�


bit is then calculated by taking the least-signi�cant bit of xi


(mo d n)

(mo d n)


.


mo d(p�)(q �)


mo d(p�)(q �)


Note that now we have xi

In other words, given x0

th


i

= x0


(mo d n) and x0


�i

= xi


(mo d n).


and th prime factors p and q of n it is not hard to generate any


i


bit and vice versa. We shall now see how these prop erties can b e used to construct an


encryption scheme.

. Blum-Goldwasser

Blum-Goldwasser is a public key probabilistic encryption scheme using BBS. The public key

is n, the private key is the factorization of n, i.e. p and q . The following are the steps to

encrypting a message:

th


. For each bit mi


of the message (0 � i < l ) compute ci = bi


� mi


where bi


is i


bit of


BBS (as in usual stream cipher).


. App end xl


to the end of message, where l is the length of ciphertext in bits.

l


mo d(p�)(q �)


To decrypt, we use the private key p and q to generate x0


from xl


(x0


�

= xl


)


and then use the BBS formula to regenerate xi


, and hence bi . The security of this scheme is


based on di�culty of calculating x0


from xl


without knowing the factorization of n.


Note that this encryption scheme achieves the desired probabilistic prop erty: each time

we co de the same message with the same key we get di�erent cipher (provided x is chosen


randomly for each message). Furthermore the extra information we need to send (xl

minimal.


) is


-----

 Quantum Cryptography

[This section has b een expanded based on the material from

http://eve.physics.ox.ac.uk/NewWeb/Research/crypto.html]

Quantum cryptography makes use of the fact that measuring quantum prop erties can change

the state of a system, e.g. measuring the momentum of a particle spreads out its p osition.

Such prop erties are called non-commuting observables. This implies that someone eaves
dropping on a secret communication will destroy the message making it p ossible to devise a

secure communication proto col.

Photon p olarization is one such prop erty that can b e used in practice. A photon may b e

p olarized in one of the four p olarizations: 0, , 0, or  degrees. According to the laws

of quantum mechanics, in any given measurement it is p ossible to distinguish only b etween

rectilinear p olarizations (0 and 0), or diagonal p olarizations ( and ), but not b oth.

Furthermore, if the photon is in one of the rectilinear p olarizations and someone tries to

measure its diagonal p olarization the pro cess of measurement will destroy the original state.

After the measurement it will have equal likeliho o d of b eing p olarized at 0 or 0 indep endent

of its original p olarization.

These prop erties lead to the following is a key exchange proto col based on two non
commuting observables (here, rectilinear and diagonal p olarizations):

. Alice sends Bob photon stream randomly p olarized in one of  directions.

. Bob measures photon p olarization, cho osing the kind of measurement (diagonal or

rectilinear) at random. Keeping the results of the measurement private, Bob then tells

Alice (via an op en channel), the kinds of measurement that he used.

. Alice tells Bob which of his measurements are correct (also via an op en channel).

. Bob and Alice keep only the correct values, translating them into 0's and 's.

Although this scheme do es not prevent eavesdropping, Alice and Bob will not b e fo oled,

b ecause any e�ort to tap the channel will b e detected (Alice and Bob will end up with

di�erent keys) and the eavesdropp er will not have the key either (since she is very unlikely

to have made the same measurements as Bob).

While practical uses of quantum cryptography are yet to b e seen, a working quantum key

distribution system has b een built in a lab oratory at the IBM T. J. Watson research center.

This prototyp e implementation can transmit over admittedly mo dest length of 0cm at rate

it 0 bits/second. Nevertheless, as new photon sources, new photo-detectors and b etter

optical �b ers are b eing built, we shall see quantum cryptography b ecoming more practical.

 Kerb eros (A case study)

Kerb eros is a trusted authentication proto col. A Kerb eros service, sitting on the network,

acts as a trusted arbitrator. Kerb eros provides secure network authentication, allowing


-----

###### 1. Request for Ticket-Granting Service 2. Ticket-Granting Ticket 3. Request for Servver Ticket
 TGS 4. Server Ticket 5. Request for Service

 3

 4

 5
 Server

Figure : Kerb eros authentication steps.

c client

s server

a client's network address

v b eginning and ending validity time for ticket

t timestamp


Kx

Kx;y

fmgKx

Tx;y

Ax;y


x's secret key

session key for x and y

m encrypted in x's secret key

x's ticket to use y

authenticator from x to y

Table : Kerb eros Notation


a p erson to access di�erent machines on the network. Kerb eros is based on symmetric

cryptography (DES).

. How Kerb eros Works

The basic Kerb eros authentication steps are outlined in Figure . The client, a user or

an indep endent software program, requests a Ticket-Granting Ticket (TGT) from Kerb eros

server lo cated on a trusted and secure machine. Kerb eros replies with this ticket, encrypting

it with client's secret key. To use the requested service, the client requests a ticket for that

server from Ticket-Granting Sever (TGS). TGS replies to client with the server ticket, which

the client uses along with authenticator to request services from the server.


-----

. Tickets and Authenticators

Kerb eros uses two kinds of credentials: tickets and authenticators. The tickets have the

following format (refer to Table  for notation):


T


= s; fc; a; v ; K


()


c;s


c;s


gKs


A ticket is go o d for a single server and a single client. It contains the client's name and


network address c, a, the server's name s, a timestamp v, and a session key Kc;s


. Once the


client gets this ticket, he can use it multiple times to access the server { until the ticket

expires.

The authenticator takes this form:


Ac;s


= fc; t; k ey gKc;s


()


The client generates an authenticator each time he wants to use service on a server. The

authenticator contains the clients name c, a timestamp t, and an optional additional session

key. An authenticator can only b e used once, but the client can regenerate authenticators

as needed.

. Kerb eros messages

There are �ve Kerb eros messages:

. Client to Kerb eros: c; tg s. This message is sent whenever the client wants to talk to

Ticket-Granting Server. Up on receipt of this message, Kerb eros lo oks up client in its

database and generates the session key to b e used b etween the client and TGS.


. Kerb eros to client: fKc;tg s


gK


c


; fT


. There are two parts in this message, one


c;tg s


gKtg s


containing session key to b e used b etween client and TGS (Kc;tg s


) encrypted with


clients key (K


) encrypted with TGS's secret


c


), and the other containing TGT (Tc;tg s


key (Ktg s


). The client cannot decrypt this latter part, but uses it to talk to TGS. Note


that Kerb eros do es not communicate with TGS directly and the tickets have limited

lifetime.


. Client to TGS: fAc;s


gKc;tg s


s fTc;tg s


gKtg s


. This is the message sent by the client to TGS.


The �rst part of this message contains information that proves client's identity to TGS.

The second part is precisely the TGT Kerb eros sent to client.


. TGS to client: fKc;s gKc;tg s


fT


c;s


gKs


. This message is similar to Kerb eros' resp onse to


clients initial request. It contains the session key to b e used b etween client and the

server as well as the ticket for the client to use when requesting service. These also

have limited lifetimes, dep ending on the kind of service requested.


. Client to server: fAc;s


gKc;s


fTc;s


gKs


. With this message the client authenticates itself


to the server as well as presents it with the ticket it received from TGS.


-----

Algorithms in the Real World Notes by Richard C. Davis

Lecture # (Linear Programming ) �c   Richard C. Davis and Guy Blello ch

� Linear Programming and Optimization

. Intro duction

. Geometric Interpretation

. Simplex Metho d

. Improvements to Simplex

 Intro duction

Optimization is a very imp ortant problem in industry. Numerous companies use it to stream
line their op erations by �nding optimal tradeo�s b etween demand for pro ducts or services,

manufacturing costs, storage costs, repair costs, salary costs, etc.

� 0+ software packages available

� 00+ pap ers just on interior-p oint metho ds

� 00+ b o oks in the library

� 0+ courses at most universities

� Dozens of companies

� Delta Airlines claims they save $00 million a year with their optimization application

. Some Optimization Problems

Optimization problems typically try to minimize (or maximize) some cost function, which

is often called the objective function given some set of constraints. Here are some common

optimization problems

Unconstrained Optimization:

n


minff (x) : x  R

where f is an ob jective function of n real values.

Constrained Optimization:


g


g


minff (x) : ci


(x) � 0; i  I ; ci


n

(x) = 0; i  E ; x  R


where I is a set of indices of inequalities, E is a set of indices of equalities, and ci

set of constraint functions each on n variables.


is a


-----

Quadratic Programming:



T


T


T

x : ai


g


Qx + c


x � bi


T

; i  I ; ai


x = bi


n

; i  E x  R


minf


x




Here we constrain the ob jective function to b e quadratic in the input variables x and

the constraint functions to b e linear.

Linear Programming:


T

minfc


n

x : Ax � b; x � 0; x  R


n m

; c  R ; b  R


m�n

; A  R g


Here b oth the ob jective and the constraint functions are linear. We also do not include

any equalities, but these are easy to express with the inequalities. We will see that

there are many equivalent formats to express linear programs.

Integer Linear Programming:


T

minfc


x : Ax � b; x � 0; x  Z


n


n


m


m�n

; A  R g


; c  R


; b  R


Same as the linear program except that the variables x are integers instead of reals.

Often referred to as just Integer Programs (IPs). We will also consider problems in

which some of the variables are integers and some are reals. These are called mixed

integer linear programs (MIPs).

In this class and the next we will b e discussing solutions to linear programs. In the

following two classes we will discuss integer programs. Note that while linear programs can

b e solved in p olynomial time, solving integer programs is NP-hard. We will not discuss non
linear programs (general constrained optimization), although some of the solutions we will

discuss for linear programs, e.g. the interior p oint metho ds, can also b e applied to nonlinear

ob jective functions.

. Applications of Linear Programming

� As a substep in pretty much all the integer and mixed-integer linear programming

(MIP) techniques.

� Selecting a mix: Oil mixtures, p ortfolio selection, ...

� Distribution: How much of a commo dity should distribute to di�erent lo cations.

� Allo cation: How much of a resource should allo cate to di�erent tasks.

� Network Flows

Although linear programs do have a reasonable numb er of direct applications in industry,

most larger applications require MIP programs since

. many resources are integral, and

. integer variables can b e used to mo del yes/no decisions (0- programming).

Therefore the most used application of linear programming is probably the �rst one men
tioned ab ove (substep of MIP programs).


-----

Table : Examples of Large Mo dels

. Overview of Algorithms

� Simplex (Dantzig  )

� Ellipsoid (Khachian   )  - the \�rst" p olynomial-time algorithm

� Interior Point  - the \�rst" practical p olynomial-time algorithm

{ Pro jective Metho d (Karmarkar  )

{ A�ne Metho d (Dikin  )

{ Logarithmic Barrier Metho d (Frisch  , Fiacco  , Gill et. al  )

The word \�rst" app ears in quotes b ecause other p olynomial-time algorithms were around

when Khachian and Karmarkar published their work, but they were not known to b e

p olynomial-time algorithms until after these algorithms were published. Note that many

of the interior p oint metho ds can b e applied to nonlinear programs.

In the constraint equation Ax � b of a linear program, x and b are vectors and A is a

matrix. Each row of A corresp onds to one constraint equation and each column corresp onds

to one variable. In practice the matrix A is often sparse (most entries are zero) since

each constraint typically only dep ends on a few of the variables. This allows many of the

algorithms to use sp ecial, fast subroutines designed to work with sparse-matrices. The

current state of the art in such solvers allows us to work with problems where the matrices

have 0-00 thousand rows/columns, and where 00 thousand to  million of the items in

the matrices are nonzeros. Table shows the size of some problems.

Though the simplex algorithm is not a p olynomial-time algorithm in the general case

(contrived examples can take exp onential time), it is very fast for most problems. For this

reason, it is still an op en question as to whether or not interior p oint metho ds are \sup erior"

to the simplex metho d and for what problem typ es. Here are two quotes that illustrate the

battle b etween simplex and interior p oint metho ds:

� \The results of this pap er demonstrate that the initial claims of the computational

sup eriority of interior p oint metho ds are now b eginning to app ear."   - Lustig, Marsten

and Shanno,   (ORSA Journal of Computing,  ()).


-----

Table 0: Running Times of Large Mo dels in seconds.

� \It is our opinion that the results of Lustig, Marsten and Shanno somewhat overstate

the p erformance of [the interior p oint metho ds] relative to the simplex metho d."   
Bixby,   (ORSA Journal of Computing,  ()).

Table 0 shows a comparison of the simplex metho d (running on either the original problem,

or the dual, as explained in the next lecture) and an interior p oint metho d, the Barrier +

Crossover metho d. The example problems are the same ones in Table . Note that the

algorithms have widely varying p erformance dep ending on the problem given. The running

time of b oth algorithms is very much dep endent on the typ e of problem. This is part of

why it is di�cult to see whether or not interior p oint metho ds are \sup erior" to the simplex

metho d.

It is clear, however, that () interior p oint metho ds are b ecoming more dominant over

time and () the app earance of interior p oint metho ds has sparked a resurgence of interest

in �nding more e�cient techniques for the simplex metho d.

. Linear Programming Formulation

There are many ways to formulate linear programs, and di�erent algorithms often use di�er
ent formulations as inputs. Fortunately it is typically easy to convert among the formulations.

For example the formulation presented earlier

T


minimize c


x (this is the objective function)


sub ject to Ax � b, x � 0

can b e converted to

T


minimize c


x


sub ject to Ax = b, x � 0

by adding slack variables. For example:


x


+ x


� 


can b e converted to


-----

x


+ x


� y


=  and y


� 0


That is, slack variables like y


must b e added to the vector x for each row or A to convert


the expression Ax � b to Ax = b. This formulation with the equality constraints Ax = b is

the formulation that is used by the simplex metho d.

. Using Linear Programming for Maximum-Flow

Before describing the algorithms for solving linear programs we describ e how linear programs

can b e use to solve maximum �ow problems. Consider the �ow problem shown in Figure .

In this problem the numb ers on the edges represent the maximum �ow allowed through the

edges (its capacity). The goal is to maximize the total �ow from the input (IN) to the output

(OUT) with the constraints that the net �ow into each no de has to b e zero, and no �ow

along an edge can b e greater than the capacity. To convert this to a linear programming

0


problem, take every edge ei


and create two edges, xi


and x

i


, one for p ositive �ow in one


direction, and the other for p ositive �ow in the other direction. The linear programming

formulation will have one variable for each direction of each edge.

###### 1

 7
 5 IN OUT
 2 7 2
 3 x2
 x
 1 6 3
 x3

Figure : A network maximum-�ow problem.

###### x x’ 2 2
 x’ 1
 x 3 x
 1
 x’ 3

Figure : Part of a Network Converted for Linear Programming

For each vertex, we add a constraint that forces the �ow into the vertex to equal the

�ow out of the vertex. Lo ok at the highlighted vertex in Figure  connected to the edges


lab eled x


, x


, and x


. This will b e converted to the network shown in Figure . Adding


the constraint that input �ow equal output �ow, we have


0

= x


0

+ x


x


+ x


0

+ x


+ x


-----

We then add two inequality constraints p er edge to include the capacity constraints. For

0


edge x

edge x0


in Figure , these inequalities will b e x


�  and x


� . Finally, we add one more


connecting \OUT" to \IN", but we place no constraints on this �ow. This completes


the formulation of the network �ow problem as a linear programming problem. Maximizing


the value of x0


will �nd the maximal �ow for this network.


 Geometric Interpretation

We can visualize linear programming problems geometrically. We present a two dimensional

example. (Here we are maximizing instead of minimizing, but the ideas are still the same.)


maximize z = x


sub ject to x

x


x + x

� x � 

 + x � 

x � 0

x ; x � 0


Each inequality represents a halfspace, as shown in Figure . The intersection of these

halfspaces is the region of p oints that abide by all the constraints. This is called the feasible

region. The �gure also shows that the ob jective function increases in one direction. The

maximal value of x is the p oint in the feasible region that is farthest in the direction of this

vector.

###### 2x1 + x2 <= 18
 x2

 x2 <= 10


###### Direction of

 Objective Function

 (2x1 + 3x2)


###### Feasible Region

 Corner Points

 x1

|x2|2x1 + x2 <= 18|
|---|---|
||x Feasible Regio x1|
|||
|||


###### x1 - 2x2 <= 4

Figure : Geometric interpretation of Linear Programming

There are some interesting things to note here. First of all, the maximal p oint must

b e on a corner formed by the intersection of the halfspace b oundaries. These corners are


-----

sometimes called extreme points. Also note that the feasible region could b e in�nite, allowing

the maximum value of the ob jective function to b e in�nite, or it might not exist at all,

meaning there is no solution.


As discussed earlier, we can add the slack variables x


, and x





, to the �rst, second,





, x


and third constraints, and the new formulation will lo ok as follows.


maximize z = x


+ x

 + x


= 

= 

= 0

� 0


sub ject to x � x + x

x + x + x

x + x

x ; x ; x ; x ; x


Figure  shows a geometric interpretation for slack variables. As each variable increases,

we move further into the feasible region. When the slack variable is 0, we are actually on

the line corresp onding to that slack variable.

###### x5

 x1

 x4

 x3
 x2

Figure  : Geometric interpretation of Slack Variables

 Simplex Metho d

This is one of the earliest metho ds for solving linear programs. Its running time is exp onential

in the worst case, but for many problems it runs much faster than that. Intuitively, the basic

algorithm works as follows

. Find any corner of the feasible region (if one exists).

. Let's say this corner is at the intersection of n hyp erplanes. For each plane, calculate

the dot pro duct of the ob jective function cost vector c with the unit vector normal to

the plane (facing inward).

|Col1|Col2|
|---|---|
||x5 x1 x4 x3 x2|
|||


-----

. If all dot pro ducts are negative, then DONE (the problem is already maximized).

. Else, select the plane with the maximum dot pro duct.

. The intersection of the remaining n �  hyp erplanes forms a line. Move along this line

until the next corner is reached.

. Goto .

Following these steps, the algorithm moves from corner to corner until the maximal

solution is reached. At each step, it moves away from a plane in such that the rate of

change of the ob jective function is maximized. There are actually di�erent p ossible ways

of deciding which plane to leave and more complicated variants of simplex use di�erent

metho ds. Figure 0 shows how simplex can start at (0,0) and move to the maximal solution.

On the �rst step it cho oses the hyp erplane (line in  dimensions) marked x to move away

from, and on the second step it cho oses the hyp erplane marked x.

At each step, the variable corresp onding to the hyp erplane that the current p oint leaves

is called the entering variable, and the variable corresp onding to the hyp erplane that the

current p oint moves to is called the departing variable. In the �rst step of the example in

Figure 0 variable x is the entering variable and variable x is the departing variable. This

sounds counter-intuitive, but it will make more sense as we delve into the details of simplex.

In particular the value of an entering variable will change from zero to nonzero, while the

value of a departing variable will change from nonzero to zero.

###### End

 x5
 Departing

 x4
 x1

 C

 x3

 x2
 Entering

 Start

Figure 0: Geometric View of the Simplex Algorithm

Note that this is a geometrical explanation of simplex. The actual algorithm is a little

cleverer than this... we don't have to �nd a unit vector p ointing in the direction of each of

the outgoing lines at each step.

|Start|End|
|---|---|
||x5 x4 x1 C x3 x2|
|||


-----

. Tableau Metho d

The Tableau Metho d is a rather elegant organization for the simplex metho d. Our formula
tion once again is as follows.

###### n

 m
#### A b

###### -c 0

Figure : The Tableau

T

|n|Col2|Col3|
|---|---|---|
|A b -c 0|||
||A|b|
||-c|0|


maximize c


x


sub ject to Ax = b, x � 0

The Tableau for this problem is shown in Figure . It is an (m + ) � (n + ) matrix. The

m +  rows corresp ond to the m constraint equations plus the negative of the cost vector.

(Without going into to o much detail, it is negative b ecause we are maximizing. If we were

minimizing, the vector c would b e p ositive here.) The n +  columns corresp ond to the n

comp onents of the vector x (including original variables and slack variables) and the vector

b in the equation Ax = b.

###### m n-m

 Values of


###### Identity

 Matrix


###### m


###### basic

 variables

 b’ >= 0

 Current Cost

 "Slopes" (if all >= 0 then done)

|1 0 1 1 0 1|F|b’|
|---|---|---|
|0|r|v|


###### Basic Variables


###### Free Variables (=0)


Figure : The Tableau after an Initial Point has b een Found

The �rst step of the simplex algorithm is to �nd a corner (extreme p oint) of the feasible

region. For the moment, let's forget ab out how we �nd this p oint, and lo ok a what this do es

to the Tableau, as shown in Figure .

In a corner, n � m of the variables must have the value 0 (corresp onding to the intersection

of n � m hyp erplanes). One way to see why this happ ens is to refer to Figure  . Since, we

have  variables, and  constraints,  variables must b e 0. Rememb er that when a variable


-----

has a zero value, the current p oint lies on that hyp erplane. Since a corner, in this example,

is where two lines meet, two of our variables must b e 0. This is an easy way to see what is

happ ening in a tableau. We'll return to this example later.

The n � m variables that are 0 are the free variables. The other m variables have p ositive

values, and are called the basic variables. If we arrange our tableau so that the m basic

variables are on the left, we can use Gaussian elimination on the tableau to put it in the

form shown in Figure , with ones on the diagonal. When arranged this way, the elements

0


of the vector b


on the right b ecome the values of the basic variables at the current p oint x


(rememb er, the free variables are all 0). Furthermore, since we are assuming the solution is

0


feasible then all the elements of b


must b e nonnegative.


We can also use Gaussian elimination to make comp onents of the cost vector �c corre
sp onding to the basic variables equal to 0. Through the pro cess of elimination, the b ottom,

right corner of the tableau comes to hold the current cost. Also, the comp onents of the

cost vector corresp onding to the free variables b ecome the slopes, i.e. the rate at which the

current cost would decrease if that free variable were increased from 0.

Now we can see how the simplex metho d pro ceeds. At each step we are given a tableau

like the one in Figure . The most negative element of the cost vector tells us which free

variable we need to increase from zero. In our two-dimensional example of Figure , this

tells us which line we need to move away from in order to maximally increase our ob jective


function. The variable xi


which we must increase is called the entering variable b ecause it


is entering the set of basic variables. Figure  (a) illustrates this step.

We have chosen which line to move away from, but we have not chosen which line to

move to. In other words, we have to cho ose a departing variable which will leave the set of

basic variables and b ecome zero. Figure  (b) shows how this is done. Lo ok at the vector u

0


corresp onding to the entering variable chosen ab ove, and lo ok at the vector b


that contains


the values of the basic variables at our current p oint x. For each basic variable xi

0


, compute


the ratio bi


=ui . This ratio indicates how much the ob jective function can increase if we use


xi


as the departing variable. In the -D example, this tells us how much the function can


increase if we move from one line to the other. (Note: it cannot increase more than this,

b ecause we would have to leave the feasible region). We must cho ose the basic variable with

the smallest ratio as the departing variable, b ecause we cannot leave the feasible region.

Note: this ratio is taken only over the p ositive comp onents of u, b ecause a negative ratio

would indicate that the cost function would decrease if we moved toward that line, and we

don't want to do that!

Now that the entering variable and the departing variable have b een chosen, we simply

swap their columns in the tableau, as shown in Figure (c), and then p erform Gaussian

elimination, as shown in Figure  (d), to get the tableau back into the state it was at the

b eginning of the simplex step. We rep eat these steps until there are no negative slop es (in

which case there is no way to increase the ob jective function and the maximum has b een

0


reached), or until there are no p ositive ratios b

i


=ui


(in which case the maximum value is


in�nite - it is di�cult to explain why this is true, but it is).

An example is in order. Figure  shows how the tableau would lo ok for our earlier

example in Figures  and  . Figure  (a) shows the initial tableau for this example.

Our initial p oint is (0,0), so it only takes a little rearranging to put the tableau in the state


-----

###### a)

 b)

 c)

 d)

|Col1|Col2|u|Col4|Col5|
|---|---|---|---|---|
|1 0 1 1 0 1||||b’|
|0|||r|v|


###### min{r } (entering variable) i

 u

 1

 1

 b’
 min{b’ /u }i i
 1

 1

 0 r v

 Departing Variable

 1 u1 0
 1 u2 0

 b’
 u m-1 1
 0 um 1 0
 0 ru 0 r v

 Swap

 1 0

 1 0
 F b’i+1
 i+1
 1
 0 0 1

 0 0 r v
 i+1 i+1

 Gauss Jordan Elimination

Figure : Simplex Steps Performed on a Tableau

|Col1|Col2|Col3|Col4|u|Col6|Col7|
|---|---|---|---|---|---|---|
|1 1||||||b’|
||1||||||
|||1|||||
|0|||||r|v|

|1 1 0|u 1 u 2 u m u m|-1 1|Col4|0 0 1 0|Col6|b’|
|---|---|---|---|---|---|---|
|0|r u|||0|r|v|

|1 1 0|0 0 1 0|1|F i+1|b’ i+|
|---|---|---|---|---|
|0|0||r i+1|v i+|


-----

###### x1-2x2+x3 = 4

|1|-2|1|0|0|4|
|---|---|---|---|---|---|
|2|1|0|1|0|18|
|0|1|0|0|1|10|
|-2|-3|0|0|0|0|

|1|0|0|1|-2|4|
|---|---|---|---|---|---|
|0|1|0|2|1|18|
|0|0|1|0|1|10|
|0|0|0|-2|-3|0|


###### bi/ui

|Col1|Col2|Col3|Col4|u|Col6|
|---|---|---|---|---|---|
|1|0|0|1|-2|4|
|0|1|0|2|1|18|
|0|0|1|0|1|10|
|0|0|0|-2|-3|0|

|1|0|0|1|-2|4|
|---|---|---|---|---|---|
|0|1|0|2|1|18|
|0|0|1|0|1|10|
|0|0|0|-2|-3|0|

|1|0|-2|1|0|4|
|---|---|---|---|---|---|
|0|1|1|2|0|18|
|0|0|1|0|1|10|
|0|0|-3|-2|0|0|

|1|0|0|1|2|24|
|---|---|---|---|---|---|
|0|1|0|2|-1|8|
|0|0|1|0|1|10|
|0|0|0|-2|3|30|


###### x3 x4 x2 x1 x5

 Perform Gaussian Elimination
 to Complete the Step (f)


###### x3 x4 x2 x1


###### x5


###### Perform Swap

 (e)


Figure : An Example of Simplex Steps on a Tableau


-----

shown in Figure  (b). In Figure  (c) we �nd the minimum value of the cost vector, which

0


corresp onds to the maximal slop e. Figure  (d) shows the ratios bi


=ui


, and which columns


we cho ose to swap. In Figure  (e) we see the tableau after the swap, and in Figure  (f )

we see the tableau after Gaussian elimination.

. Finding an Initial Corner Point

We have not yet discussed how to �nd the initial corner p oint needed to start the simplex

metho d. If we were originally given the problem in the form Ax � b; x � 0 and b � 0, then

we can add slack variables and use them as our initial basic variables (i.e., our initial corner

is where all variables x are 0 and the slack variables y equal b). However, if we are given the

problem in the form Ax = b, we will need to �nd an initial corner. One way to do this is to

use the simplex metho d to solve a slightly mo di�ed version of the original problem. Given

the tableau in Figure , we can extend it further by adding m arti�cial variables, one for

each row (these are analogous to the m slack variables we previously considered). These will

form an identity matrix as shown in Figure . (Note: the vector b must b e p ositive, but

any problem can b e put in this form by negating the rows with negative values in b.)


###### n

 0

#### A b

###### 1

 -c 0

 Highly negative costs (highly positive values)


###### Artificial

 Variables


###### m


###### m

|1 0 0 1|A|b|
|---|---|---|
||-c|0|


Figure : A Mo di�ed Tableau that will �nd a Starting Corner Point

If we give each of these arti�cial variables a highly negative cost (which corresp onds to

high p ositive values in the tableau b ecause it holds �c). We can solve this with the simplex

metho d as if it were a normal tableau. The arti�cial variables will b e the set of basic variables

in the �rst step (again, we can make the cost vector 0 b elow them by Gaussian elimination)

and the other variables will b e free.

Our vector x will quickly move away from the arti�cial variables b ecause the algorithm

maximizes the ob jective function (cost) and these variables have high negative values. So on,

the arti�cial variables will b e free variables, and some other set of m variables will b e the basic

variables. When this happ ens, we can remove the columns corresp onding to the arti�cial

variables, and we will have a tableau that we can use to start solving the original problem.

On the other hand, if this pro cess ends and there are still arti�cial variables in the basis,

then there is no feasible region for the original problem.


-----

. Another View of the Tableau

Figure  shows another way to lo ok at the tableau. Once we have moved the basic variables

to the left and the free variables to the right, we end up with the matrix shown in Figure 

a. Gaussian elimination turns the matrix B into the identity matrix, which is equivalent

�


to left-multiplying the top three blo cks by B


. Elimination of cb


on the b ottom row is


equivalent to subtracting cb

Figure  b.


times the top of the matrix from the b ottom. This is shown in

#### N b

###### c
 n 0

 Tableau at a Corner Point

 (a)

 -1 -1
#### B N B b

###### -1 -1 c B  N-c c B  b b n b

|B|N|b|
|---|---|---|
|c b|c n|0|

|I|-1 B N|Col3|Col4|
|---|---|---|---|
|||||
|0|-1 c B N-c b n|||
|||||


###### Tableau after Gaussian Elimination

 (b)

Figure : Another way to lo ok at a Tableau

Note that the tableau is likely to b e very dense. Even when the original formulation of

�


the problem is very sparse the inverse B


will typically b e dense.


. Improvements to Simplex

The density of the tableau, mentioned in the previous section, is a ma jor problem. Typically

the matrix A starts out very sparse|it is not unusual that  out of every 0,000 elements

�


that are nonzero. Since B


will b e dense, however, algorithms cannot a�ord to calculate it

�


directly. For this reason, it is common to keep the matrix B


in the factored form...


�

U



�


�

L

m


�

� � � L




U


�




�

� � � U

m


...which can b e much sparser than B


. The trick (and ma jor improvement over the last


decade) is up dating this factorization in place when exchanging variables.

Here are some other improvements.


-----

� Improved pricing (i.e. don't always go down the maximum slop e). One example of

this is normalized pricing in which prices are weighted by the length of the path to the

departing variable.

� Better factoring routines (for initial factorization).

� \Perturbation Metho d" for dealing with stalling. The Simplex metho d can stall when

it hits a degeneracy (i.e. a place where more than m lines meet in a corner in the -D

case    - one of them is redundant) and will sometimes stall by leaving a redundant line,

only to return to the same corner.

� Various hacks in how to store the sparse matrices (e.g. store b oth in column and row

ma jor order).

� Better Pro cessing.

Sp eeds have improved by -00 times (dep ending on mo del) due to algorithmic improve
ments over the last 0 years.


-----

Algorithms in the Real World Notes by Steven Czerwinski

Lecture # (Linear Programming ) �c   Steven Czerwinski and Guy Blello ch

� Duality

� Ellipsoid Algorithm

� Interior Point Metho ds

. A�ne scaling

. Potential reduction

. Central tra jectory

 Duality

Duality refers to the prop erty that linear programming problems can b e stated b oth as

minimization and maximization problems. For any problem, there is a primal and a dual.

The primal usually refers to the most natural way we describ e the original problem. This

can either b e a minimization or maximization problem, dep ending on the sp eci�cs. The dual

represents an alternative way to sp ecify the original problem, such that it is a minimization

problem if the primal is a maximization and vice versa. Solving the dual is equivalent to

solving the original problem.

For example, supp ose we have the following:

Primal problem: Maximize z = cx

such that Ax � b and x � 0

(n equations, m variables)

Then, for our dual, we have: (notice the change in m and n)

Dual problem: Minimize z = y b

such that y A � c and y � 0

(m equations, n variables)

So why do we care ab out the dual for a problem? One reason is that we often �nd that

the dual is easier to solve. The dual can also b e used for sensitivity analysis which determines

how much the solution would change with changes in c; A or b. Finally, it can b e used in

conjunction with the primal problem to help solve some of the interior p oint metho ds.

. Duality: General Case

In converting maximization problems to minimization problems and vice versa, we �nd that

every variable in the primal pro duces a constraint in the dual. Likewise, every constraint in

the primal pro duces a variable in the dual.


-----

Table : Rules for converting b etween Primals and Duals

We also �nd there is corresp ondence b etween the variable's restrictions in the primal,

with the constraint's equality sign in the dual. For example, if a variable must b e greater

than 0 in a minimization problem, then the constraint the variable pro duces in the dual

will b e stated as a \less than" relationship. Similarly, there is a corresp ondence b etween

the constraints' equality signs in the primal to the restrictions on the variables in the dual.

Table  summaries these corresp ondences.

. Example

We are given the following maximization problem:


maximize: x


+ x


� x


s.t. x

x

x


+ x

 � x


+ x

 � 


� 0


= 0


+ x





+ x


x ; x


� 0


From this description, we easily determine the following:


  �



0



 

0

  

 � 0

  









x =

c =

b =

A =








h














x

x

x


i








We can now pro duce the dual:


-----

minimize: 0Y


+ Y


� 0Y


s.t. Y

Y

Y

Y


+ Y


� 0; Y


+ Y


 � 

� 


� Y

+ Y


+ Y

= �


� 0


The co e�cients come from transp osing A. To determine the equality/inequality typ e we use


the rules in Table . For example the �rst inequality Y


+ Y


�  corresp onds to





+ Y


variable x

dual.


in the primal. Since x


� 0 in the primal, the inequality typ e is also � in the


Notice, since the �rst constraint is pro duce by multiplying A's �rst column vector with


Y, it corresp onds to the x


variable in the primal (b ecause the �rst column in A contains


all of x


's co e�cients). Therefore, the �rst constraint in the dual must have an \equal"


relationship since x


is unrestricted in the primal.


. Duality Theorem

The Duality theorem states:

If x is feasible for P (given b elow) and y is feasible for D then: cx � y b and at optimality,

cx = y b. We call y b � cx the Duality Gap. The magnitude of the duality gap is a go o d way

to determine how close we are to an optimal solution and is used in some of the interior

p oint metho ds.

P: Max z = cx

s.t. Ax � b

x � 0

D: Min Z = y b

s.t. y A � c

y � 0

 Ellipsoid Algorithm

Created by Khachian in ', the ellipsoid algorithm was the �rst known p olynomial-time

algorithm for linear programming. (There were other p oly-time algorithms around, but they

had not b een proven to b e so.) The ellipsoid algorithm do es not solve linear programming

problems of the general form, but rather it solves any problem stated in the following way:

Find x sub ject to Ax � b (i.e. �nd any feasible solution).

However, we will show that any linear programming problem can b e reduced to this form.

If L equals the numb er of bits used to represent A and b, then the running time of the




algorithm is b ound by O (n


L). Unfortunately the algorithm takes this much time for most


problems (it is very unusual that it �nds a solution any faster). Simplex's worse case running




time is larger than O (n


L), but for most problems it do es much b etter. Therefore Simplex


-----

###### Ek


###### Feasible Region

 Ek+1


###### R R 1 2

Figure : An iteration in the Ellipsoid Algorithm

ends up b eing b etter than the Ellipsoid algorithm in practice for most problems even though

its worst-case running time is worse.

. Description of algorithm

|a k c k k R 1|c k+1 E k R 2|
|---|---|


The idea b ehind the ellipsoid algorithm is that we start with some ellipsoid E0


which encloses


an area in the solution space, and is guaranteed to contain the feasible region of the solution.

Basically, at each iteration of the algorithm, we create new ellipsoids Ek that are smaller

than the previous, but still are guaranteed to contain the feasible region. Eventually, we will

�nd a p oint that satis�es the problem (recall that we are satis�ed with any feasible p oint).

Sp eci�cally, for each iteration k of the algorithm we do the following:


. Determine ck

. Determine ak


= the center of Ek


= the constraint most violated by ck


.


.


. Use the a


into two regions. One of these regions R


contains


k


hyp erplane to split Ek


ck


, and the other R


contains the feasible region.

k + such that it contains all p oints in Ek


\ R


. We then construct E


, but is smaller than


Ek


.


Figure  illustrates these steps.

For n variables Khachian showed the following prop erty of this algorithm:


-----

V ol ume(Ek + )


=






n+


V ol ume(Ek


)




. Reduction from general case

As stated, we can convert the general form of linear programming problems to a form suitable

to use the ellipsoid algorithm on.

Supp ose we have the following problem stated in the general form: Maximize cx sub ject


0 0

to Ax � b, and x � 0. We can convert it to the form A x

Find any x, y such that


0

� b


as shown b elow:


0

Here x and y together form x


, the combination of the left sides of the equations form A

0


Ax � b ()

�x � 0 ()

y A � �c ()

�y � 0 ()

�cx + by � 0 ()

0


,


and the combination of the right sides of equations form b


. Equations () and () come from


the original problem, and equations () and () come from its dual. Equation () will only

b e true at a single p oint when the original problem is optimized (the duality gap must b e


0 0

non-negative). In this way, if any solution to A x

solution for the original problem.

 Interior Point Metho ds


0

� b


is found, then it will b e the optimal


Interior p oint metho ds are considered the �rst practical p olynomial time metho ds for linear

programming. Unlike simplex, the interior p oint metho ds do not touch any b oundaries until

the end when they �nd the optimal solution. Instead, these metho ds work by traveling

through the interior of the feasible region (see Figure ) by using a combination of the

following two terms:

Optimizing term This moves the algorithm towards the ob jective.

Centering term This keeps it away from the b oundaries.

Generally, interior p oint metho ds take many fewer steps than the simplex metho d (often less

than 00), but each step is considerably more exp ensive. The overall relative cost of simplex

and interior p oint metho ds is very problem sp eci�c and is e�ected by prop erties b eyond just

the size of the problem. For example the times dep end strongly on the matrix structure.

Interior p oint metho ds have b een used since the 0s for nonlinear programming. Roughly

categorized, the metho ds include the following:


-----

Figure : Walking on the interior p oints

Fuel Continent Car Initial

Size xk xk x0k  xk

Non-zeros k  k k 0k

Iterations    

Cholesky non-zeros .M .M .M .M

Time s s s s

Table : Performance of the central tra jectory metho d on  b enchmarks

Name Numb er of iterations

A�ne scaling no known time b ounds

Potential reduction O (nL)

p


Central tra jectory O (


xL)


Karmarkar proved p olynomial time b ounds for his metho d (p otential reduction) in  .

Table  shows some example running times for a central tra jectory metho d (Lustig, Marsten,

and Shanno ) on four di�erent b enchmark problems. As the table shows, the time sp ent

in each iteration is greatly in�uenced by the numb er of Cholesky non-zeros present in the

matrix.

In the following discussion we will assume we are trying to solve a linear program of the

form

minimize: cx

sub ject to: Ax = b

x � 0

. Centering

There are several di�erent techniques to compute the centering term for interior p oint meth
o ds. This section describ es a few of those techniques.


-----

###### X i[’s]

.. Analytical center


###### Distance to constraint

Figure  : The analytical center


We can use analytical centering by minimizing

m

X

lg xi

i=


If xi


= 0 are the b oundaries of the feasible region (we assume they are), then xi


are the


distances to the b oundaries from our current p oint. See Figure  .

.. Elliptical Scaling

In elliptical scaling, we start with a small ellipsoid centered around the current p oint. We

then expand the ellipsoid in each dimension of the problem. The expansion in a dimension

stops when the ellipsoid touches a constraint. Since our inequality constraints are of the

form x � 0, the equation will b e of the form:




x



c


+




x



c


= 


The ellipsoid will then b e a measure of how uncentered the p oint is and can b e used to

scale space to bias our selection of a direction toward the longer dimensions of the ellipsoid,

and thus away from constraints which are close by (the shorter dimensions). See Figure 0.

We will see how this is used in the a�ne scaling metho d.


-----

Figure 0: Elliptical Scaling

. Optimizing techniques

.. Pro jection

If our problem is constrained to Ax = b, then we know that our feasible region is contained

in a hyp erplane. If A has n rows and m columns, then it is contained in a m � n dimen
sional hyp erplane in m dimensional space. (Assuming the rows in A are indep endent.) The

hyp erplane basis is called the nul l space of A We can also view A as b eing the \slop es" for

the hyp erplane, while b represents the \o�sets".

We can use this to �nd the optimal solution for the problem. If ~c is the direction of the

~


optimal solution, then we should take a step in the direction of


d. See Figure . We must


do this b ecause ~c would take us o� the hyp erplane and therefore, out of the feasible region.

Instead, we pro ject c into the hyp erplane, and step in that direction.

~


Here's how we compute d :


~

d = ~c � ~n

= c � A


T

(AA

T


T


�

)


Ac


T


�

)


A)c


= (I � A

= P � c


(AA


T

where P = (I � A


T

(AA


�

) A), the pro jection matrix.


Calculating P � c (the pro jection) must b e done at each iteration of the metho d since, as

we will see, A will change. So, solving for the pro jection matrix is a ma jor computational

concern.

T


We �nd that it is more e�cient to solve AA


w = Ac for w . We can then use w to


calculate the pro jection b ecause of the following relationship:


T

P c = (I � A


T �

(AA )


T

A)c = c � A


w


-----

T

Computing AA


Figure : Pro jection into the null space

w = Ac is more e�cient b ecause it can b e solved using a sparse solver


(e.g. Cholesky Factorization). Otherwise, calculating P directly can generate a dense matrix,

which is problematic b oth in terms of runtime and in the space it would require.

.. Newton's Metho d

We can use Newton's Metho d to help determine the direction in which we should travel in

the interior of the feasible region to optimize the solution. Often, the function we are trying

to optimize will not b e linear in x, and could b e comp osed of transcendental functions such

as lg or ln, as in the central tra jectory case. We can approximate the minimum of these

functions using a Newton's metho d, and more easily determine the direction of the optimal

solution. We can see how this is done through a little math.

First, we will just lo ok at the general case of minimizing some -dimensional function


f (x). We can write f (x) as a Taylor expansion around some p oint x0




0


00


.




f (x) � f (x0


) + f


(x0


)(x � x0


) +


(x


0


)(x � x0


)


f




To get the minimum of the function, we take the derivative and set it to 0, which gives:


0


00


0 = f (x0 ) + f (x0 )(x � x0 )

0

f (x0 )

x = x0 � 00

f (x0 )

In multiple dimensions we can write this in matrix form as


0 = f

x = x


(x0

0 �


) + f

0


T

rf (xc )


x � xc


~ �

d = (F (xc ))


=


where f (x) is now a function of n variables, xc


is the p oint we are expanding ab out, and


F (xc


) = r � rf (x) evaluated at xc

F (x) =


, an n � n matrix which is called the Hessian matrix, i.e.















@ f


@ f


@ f


@ x x


@ x


 x


@ x xn


@ f


@ f


@ f


@ x x


@ x


 x


� � �

� � �

� � �

� � �


@ x xn















@ f


@ f


@ f


@ x


x


x





x


n


n





@ xn


@ xn


-----

rf (xc


) is a vector of the �rst derivatives of f (x) evaluated at xc


.


If we constrain the newton step to b e on a hyp erplane (i.e. Ax = b), it is called a

~


constrained Newton step. In general we �rst pick a direction


d based on a Newton step (or


other metho d) and then pro ject the step onto the constraining hyp erplane, as discussed in

the previous section.

. A�ne scaling metho d

The a�ne scaling metho d is basically a biased steep est descent search (biased away from

the b oundaries of the feasible region). Supp ose we had the following problem to solve:

minimize: cx

s.t. Ax = b,

x � 0

To solve this using the a�ne scaling metho d, at each iteration we solve:

minimize: cz

s.t. Az = 0,

�


z D


z � 


where D is a matrix whose only non-zero terms are along its main diagonal. The terms on

�


this diagonal are the co ordinates of the current p oint: x


; x


; x


; � � �. The equation z D


z � 


is the de�nition for the interior of an ellipsoid, as describ ed earlier (see Figure 0).


We up date our x at each iteration by setting xk +


= xk


+ � � z, where z is the direction


we found in the ab ove minimization problem, and � is selected to bring us close to the

b oundary, but not all the way there.

�


In this pro cess, the cz minimization acts as the optimization term, while the z D


z � 


acts as the centering term. In order to understand how this works, we should realize Ax = b

is a slice of the ellipsoid. In fact, it is the same hyp erplane that we describ ed in the ellipsoid

0


scaling metho d. In order to minimize the function, we should step in the c

0


direction, where


c


is the pro jection of c into the hyp erplane. However, the a�ne scaling metho d steps in the


direction of z .

How do we get z ? We construct hyp erplanes p erp endicular to c, and keep moving them

back until we �nd one such hyp erplane that intersects the ellipsoid only once. We then

construct z to b e the di�erence b etween the current p oint and the intersection p oint. By

stepping in the direction of z, we are centering the p oint b ecause z will tend to p oint to

constraints that are far away. In fact, as the current p oint comes closer and closer to a

constrain, z will p oint further and further away from that constraint.

0


See Figure  for a picture of this construction of z, c

.. Computation at each iteration


, and the hyp erplanes.


0


In order to ease the computation of z, we make a substitution of variables, by setting z = D z .

Then, we have


-----

Figure : An iteration of the A�ne Scaling Metho d

0

minimize: cD z

0


s.t. AD z


0


0T


T

D


= 0,

�


D


z


D z


� 


The last equation simpli�es to z z � , which is just a sphere. With this in mind, we can say

0


our direction z


is unbiased and throw out the z z �  constraint. To �nd the minimum we

0


now just take a steep est descent step on cD z

0


that keeps us within the hyp erplane de�ned


by AD z


= 0. This leads us to,

0

z


= � (I � B


T


�

)


B ) � cD


T

(B B


| {z }

projection

0

where B = AD . To get z in our original space we just substitute back z = D z

0


0


. The vector


z


is negative since we are trying to �nd a minimum and therefore descending.


.. Overall computation

Now that we know what we have to compute during each iteration, let's step back and see how

the entire pro cess works. In the following algorithm we will assume we �nd the pro jection

by using Cholesky factorization to solve the linear system, as describ ed in Section ... The

linear equation could also b e solved using other techniques, such as iterative solvers.

. Find a starting feasible interior p oint x0


T

. Symb olically factor AA

T


T


. Since the non-zero structure of B B


on each step is going to


b e the same as AA


, we can precompute the order of the op erations in the Cholesky


-----

Figure : Picking an alpha

factorization, along with its non-zero structure. Since we are only doing this once, we

can p otentially sp end some time trying to minimize the \�ll" (the numb er of additional

T


non-zero's that app ear in the Cholesky factorization that did not app ear in AA

. Rep eat until done


� B = ADi


, where Di

T


T

w = B D c by multiplying out B D c and factoring B B


is a diagonal matrix with the xi


along the diagonal.


).

with


� Solve for w in B B


help from the precomputed symb olic factorization.


0

� z


= �(D c � B

0


T


w )


� z = Di


z


� xi+


= xi


(substituting back to the original space)

+ �z


As mentioned, we should pick � so that the step is taken some fraction of the way to the

nearest b oundary. See Figure . In practice � is selected so that it go es .  of the way to

the b oundary.

. Potential reduction

In the p otential reduction metho d, we reword the minimization problem to b e

Pn


minimize: q ln(cx � by ) �

s.t. Ax = b, x � 0


ln(xj


)


j =


y A + s = 0, s � 0

As we can see, this metho d makes use of the problem's dual. The minimization criteria is

partly based on the duality gap (cx � by ). Also, the s variables are the slack variables.

The �rst quantity in the minimization (q ln(cx � by )) represents the optimizing term. It

will go to � at the optimal solution. Therefore, this term will dominate near the optimal

solution.

Pn


ln(xj


) is the analytical center term.


j =


-----

In order to optimize the solution at each iteration, we can either do a constrained Newton

step, or a transformation with a steep est descent. This second metho d is what Karmarkar

used in his version of the p otential reduction metho d.

There are several advantages of this metho d over the a�ne scaling metho d:

� There are guaranteed b ounds on the running time.

� The duality gap used in the minimization allows the user to sp ecify an error tolerance

for the solution.

� It is more e�cient in practice.

. Central tra jectory

The central tra jectory is the metho d of choice these days. It falls under the category of

Log Barrier metho ds, which date back to the 0s where they were used to solve nonlinear

problems.

To p erform central tra jectory, at each iteration step k, we do the following:

Pn


.


minimize: cx � �k j = ln(xj )

s.t. Ax = b; x      - 0

(approximate using a constrained Newton step)


. Select �k +


� �k


This will terminate when �k


approaches 0.


It turns out that with the \appropriate" schedule of �k


, the central tra jectory approach


reduces to the p otential reduction approach. We can therefore view it as a generalization.

Currently the primal-dual version of the central tra jectory approach using \higher order"

approximations (rather than Newton's) seems to b e the b est interior-p oint algorithm in

practice.

 Algorithm summary

. Overall, the current state of the art uses very sophisticated algorithms to solve linear

programming problems in practice. Even the linear algebra packages used to p erform

the computations use complicated math in order to optimize computation time.

. Practice matches theory reasonably well.

. We �nd interior-p oint metho ds dominant when:

� Large n

� Small Cholesky factors

� The problem is highly degenerate, meaning the many of the constraints cross each

other.


-----

. Ellipsoid algorithms are not currently practical, since they always take the worse case

time.

. Large linear programming problems take hours/days to solve. Parallelism is very im
p ortant to sp eed up the optimization.

. There are many interior-p oint metho ds, but they all share the same intuition.

We lo oked at a slide that showed the running times of large mo dels. For some interior

t


p oint metho ds, AA


y = Ac was to o dense, so the programs ran out of memory and couldn't


complete their tasks.

Some algorithms use interior p oint metho ds to get close to a solution, then snap to a

b oundary and use simplex metho ds to �nish o� the answer.

 General Observation

Mathematics has b ecome increasingly imp ortant for \Real World" algorithms. Just over the

last 0 years, the complexity of math employed in algorithms has increased dramatically.

� Compression

. Information theory

. Markov mo dels

. Transforms (for lossy compression)

� Cryptography

. Group theory

. Numb er theory

� Linear Programming

. Matrix algebra

. Optimization

. Graph theory


-----

Algorithms in the Real World Notes by Andrew Begel

Lecture #0 (Integer Programming ) �c   Andrew Begel and Guy Blello ch

� History

� Knapsack Problem

� Traveling Salesman Problem

� Algorithms

. Linear Program as Approximation

. Branch and Bound (integer ranges)

. Implicit (0- variables)

. Cutting Planes (postponed)

 Intro duction and History

Linear integer programming (often just called integer programming, or IP) is a linear program

with the additional constraint that all variables must b e integers, for example:

maximize cx

sub ject to Ax � b

x � 0

n

x  Z

There are several problems related to integer programming:

Mixed integer programming (MIP): Some of the variables are constrained to b e inte
gers and others are not.

zero-one programming: All the variables are constrained to b e binary (0 or ).

Integer quadratic programming: The cost function can b e quadratic.

Integer programming was intro duced by Danzig in  . In  , he showed that TSP

(traveling salesman problem) was a sp ecial case of integer programming. Gomory found the

�rst convergent algorithm in  . In  0, Land and Doig created the �rst general branch

and b ound techniques for solving integer programming problems.

Integer and mixed integer programming has b ecome \dominant" over linear programming

in the past decade. It saves many industries (e.g. airline, trucking) more than one billion

dollars a year. The state of the art in algorithms is branch-and-b ound + cutting plane +

separation (solving sub-problems). General purp ose packages don't tend to work as well

with integer programming as they do with linear programming. Most techniques employ

some form of problem-sp eci�c knowledge.


-----

 Applications

IP and MIP can b e applied to a numb er of di�erent problem areas:

� Facility lo cation { Where should we lo cate a warehouse or a Burger King to minimize

shipping costs?

� Set covering and Set partitioning { Scheduling crews for Delta

� Multicomo dity distribution { Routing deliveries for Safeway

� Capital budgeting { Developing a budget for Microsoft

� Other applications { VLSI layout, clustering, etc.

Here we will describ e how various problems can b e expressed as integer programs.

. Knapsack Problem

It lo oks trivial, but it's NP-complete.

Maximize cx

sub ject to ax � b,

x binary

where:

b = maximum weight


ci

ai

xi


= utility of item i

= weight of item i

(

; if item i is selected

=

0; otherwise


. Traveling Salesman Problem

n

X

We want to minimize

i=

sub ject to

n

X


n

X

j =


c


i;j


xi;j


= ; for i = ; : : : ; n

= ; for j = ; : : : ; n

� n � ; for i; j = ; : : : ; n


j =0

n

X

i=0


xi;j

xi;j


ti


� tj


+ nxi;j


-----

where:


ci;j

xi;j

ti


= distance from city i to city j

(

; if city j visited immediately after city i

=

0; otherwise

= arbitrary real numb ers we need to solve for,

but we don't really care ab out their values


The �rst set of n constraint restricts the numb er of times the solution enters each city to

. The second set of n constraint restricts the numb er of times the solution leaves each city

to . The last set of constraints are used to eliminate subtours. In particular the constraints

make sure that any tour includes city , which in conjunction with the �rst and second set

of constraints forces a single tour.

To see why the last set of constraints forces any tour to include city , lets consider a

tour that do es not include the city and show a contradiction. Lets say the tour visits the


sequence of cities v


; : : : ; vl


none of which is city . Lets add up the equations taken





; v ; v


from the last set of constraints for each pair of cities that are visited one after the other

in the tour. Since it is a tour, each tvi will app ear once p ositively and once negatively in

this sum, and will therefore cancel. This leaves us with nl � (n � )l, which is clearly a

contradiction.

. Other Constraints Expressible with Integer Programming


Logical constraints (x ; x


binary):

Either x


or x


) x

) x


+ x

� x


= 

� 0


If x


then x


Integer constraints can also b e applied to combine constraints:


x � M y � b

x � M ( � y ) � b


x � b

x � b


Either or


a

a


)


a

a


y binary


The M is a scalar and needs to b e \large" (x, a


, and a





are vectors). This works since if


y =   then the �rst equation is always true and the second needs to b e satis�ed, while if

y = 0 then the second is always true and the �rst needs to b e satis�ed. Since y is constrained

to b e binary, one needs to b e satis�ed.

A similar approach can b e used to handle m out of n constraints.

. Piecewise Linear Functions

Consider a minimization problem with the following ob jective function

(

0 x = 0

c(x) =

k + cx x � 0

and assume that x � M . This can b e expressed as the following integer program:


-----

minimize k y + cx


such that xi

xi


� M y

� 0


y  f0; g

The �rst inequality forces y to b e  if x is anything other than 0. This basic approach can

b e generalized to arbitrary piecewise linear functions.

 Algorithms

. Linear Programming Approximations

The LP solution is an upp er b ound on the IP solution. If the LP is infeasible, then the IP

is infeasible. If the LP solution is integral (all variables have integer values), then it is the

IP solution, to o.

Some LP problems (e.g. transp ortation problem, assignment problem, min-cost network

�ow) will always have integer solutions. These can b e classi�ed as problems with a unimo d
ular matrix A. (Unimo dular ) detA = 0;  or �).

Other LP problems have real solutions that must b e rounded to the nearest integer. This

can violate constraints, however, as well as b eing non-optimal. It is go o d enough if integer

values take on large values or the accuracy of constraints is questionable. You can also

prepro cess problems and add constraints to make the solutions come out closer to integers.

. Search Techniques

We will now describ e two search techniques for solving integer programms b oth based on a

general Branch-and-Bound approach. The �rst technique works for general integer programs

and the second for 0- programs. For historical reasons, the �rst is called the Branch and

Bound algorithm, even though b oth algorithms are in fact based on branch and b ound. Both

algorithms require exp onential time in the general case.

.. Branch and Bound

The branch and b ound approach basically builds a tree of p ossible solutions by splitting

at each no de of the tree based on a value for one of the variables (e.g., all solutions with

x <  go to the left branch and all solutions with x �  go to the right branch). Such a tree

can easily end up having a numb er of no des that is exp onential in the numb er of variables.

However, by judicially pruning the tree we can hop e to greatly reduce the numb er of no des

that have to b e searched. The \b ound" refers to the pruning of the tree so that we don't

have to search further.

Each time the algorithms branches left or right it adds a constraint (e.g., x < ). The

pruning is based on keeping the b est previous solution found (lets assume a maximization

problem) and then using a linear program to get an upp er b ound on the solution given

the current constraints. If the solution to the linear program is less than the b est previous

solution then the no de do es not have to b e searched further. There is freedom in the basic


-----

function I P (C ; c; z �)

// C is the set of constraints Ax � b

// c is the ob jective vector

// z � is the cost of the current b est solution (initially �)

// Returns the cost of the optimal solution with constraints C

if b etter than z �, otherwise returns z*

z ; x; f = LP (C ; c)

// f indicates whether LP (C ; c) is feasible or not

if not(f ) return z � // no feasible solution

if z � z � return z � // upp er b ound less than current b est solution

if integer(x) return z // new b est solution found

0


pick a non integer variable x

i

0


from x


Cd


= C ; xi


� bx

i


c


z � = I P (Cd


z � = I P (Cd ; c; z �)

0

Cu = C ; �xi � �dxi

z � = I P (Cu ; c; z �)


Cu


= C ; �x


0

i


e


return z �

end

Figure : The Branch and Bound Algorithm for Integer Programming.

algorithm in selecting the next no de to expand. The most common approaches are to use

either a depth �rst search (DFS) or b est-�rst search. Depth-�rst search has the advantage

that it more quickly �nds an initial solution and leaves less no des \op en" (each of which

requires space to store). Best-�rst search has the advantage that it might �nd the b est

solution faster. A compromise is to use b eam search by limiting the numb er of partial

solutions that can b e left op en in a b est-�rst search.

Figure  shows a branch-and-b ound algorithm that uses DFS and pruning to solve the

maximization problem

maximize cx

n

sub ject to Ax � b, x � 0, x  Z

The algorithm passes around the current b est solution z � and adds constraints to the

constraint set C each time it expands a no de by making recursive calls. The algorithm stops

expanding a no de (b ounds or prunes the no de) if either () the linear program given the

current set of constraints is infeasible () the solution to the linear program is less than the

current b est solution () the linear program has an integer solution.


-----

function I P (C ; c; xf ; z �)

// C is the set of constraints Ax � b

// c is the ob jective vector


// xf


a subset of the variables which are �xed


// z* is the cost of the current b est solution


x = xf


+ 0 (set free variables to zero)


// this is the b est solution ignoring inequalities since c � 0

// it is not necessarily feasible

if cx � z � return z � // lower b ound greater than current b est solution

if feasible(C ; x) return cx // new b est feasible solution found


if no feasible completion to xf


return z �


pick a non �xed variable xi


from x


xf 0


= xf



[ fxi


= 0g


z � = I P (A; c; xf 0; z �)


xf 


= xf



[ fxi


= g


z � = I P (A; c; xf ; z �)

return z �

end


Figure : The Implicit Enumeration Algorithm for 0- Programming.

Note that given the solution of the linear program at a no de, solving the problem at the

two children is much easier than solving it from scratch since we are already very close to

the solution. The dual simplex metho d can b e used to quickly resolve an LP after adding

one additional constraint.

. Implicit Enumeration (0- Programs)

We want to solve the problem:

minimize cx

n

sub ject to Ax � b, c � 0, x  f0; g

Note that this formulation assumes that the co e�cients of c are all p ositive. It is not hard

to convert problems with negative co e�cients into this form.

Figure  shows an algorithm based on the \implicit enumeration" with depth-�rst-search

for solving such a problem. Unlike the previous technique, implicit enumeration do es not

require linear programming. To generate a lower b ound on the solution (upp er b ound for

a maximization problem) it uses a solution in which all variables are binary but that do es


-----

not necessarily ob ey the inequality constraints. The previous branch-and-b ound technique

generated the upp er b ound by using a solution (the LP solution) that ob eys all the inequality

constraints, but is not necessarily integral.

Here's how to implement the substeps. To check for feasible(C ; x) we can just plug x into

C . To check if there are no feasible completions we can check each constraint.

For example, if


= fx

+ x


and one of the constraints is

then

which is imp ossible since x


xf = fx = ; x = 0g

x + x � x + x � 

 �  + x �  � 0 + x � 

x + x � �

and x are binary.


xf

x


Note that this check is not necessarily always going to tell us that there are no p ossible

completions even if there aren't. It is also p ossible to run more complicated tests that involve

multiple inequalities at a time, which might �nd a completion is infeasible when the simple

technique do es not.


-----

Algorithms in the Real World Notes by Stephen Chenney

Lecture # (Integer Programming ) �c   Stephen Chenney and Guy Blello ch

� Algorithms

. Problem sp eci�c asp ects

. Cutting Plane metho d

. Recent developments

� Airline Crew Scheduling

. The Problem

. Set Covering and Partitioning

. Generating Crew Pairings

. TRIP

. New system

 Algorithms (continued)

. Problem Sp eci�c Asp ects

There are many places in the branch-and-b ound and implicit-enumeration algorithms in

which domain sp eci�c knowledge can help the algorithms. Here we mention some of these.

� In branch-and-b ound domain sp eci�c knowledge can b e used to cho ose the next variable

to branch on in the search algorithms, and which branch to take �rst. For example

based on the domain we might know that certain variables are \more" imp ortant than

others, or that solutions are more likely to lie to one side or the other of the branch.

The implicit enumeration algorithm is similar|domain sp eci�c knowledge can help

cho ose a variable to �x and which branch to try �rst.

� Domain sp eci�c knowledge can b e used to help generate cuts. In the cutting plane

algorithm (later in these notes), a constraint must b e added at each step. Domain

knowledge can b e used to cho ose a more restrictive constraint, moving you toward the

solution faster. Domain knowledge also determines if approximations are acceptable,

which allows for more aggressive cutting planes.

� Domain sp eci�c heuristics can b e used for predicting upp er b ounds for more aggressive

pruning of the tree. Knowing an upp er b ound a-priori means that many branches can

b e eliminated based on their linear program's cost even b efore any integer solution is

found.


-----

� Domain sp eci�c knowledge can b e used to help quickly check for feasibility. For in
stance, knowing which constraints are more likely to b e unsatis�able suggests an or
dering for testing constraints.

� Domain sp eci�c knowledge can help solve the linear program or sp ecify that a particular

approximate solution is go o d enough. See the Airline Crew Scheduling problem later

in these notes for an example of b oth these cases.

. Cutting Plane Algorithm

The basic idea is to add a new constraint (geometrically, a new hyp erplane) at each step. This

plane will cut out non-integer solutions and move the solution closer to an integer solution.

Figure  shows the intuition. A new plane is added at each step to cut o� the corner of

the feasible region containing the linear program solution. In Figure  the limiting case

is shown, where the new constraints approximate a curve b ounding the acceptable integer

solutions.

###### x2

 B

 x’=0

 C
 A
 x’’=0

 G

 H
 E Objective
 I F
 D function
 increases

 x
 1

Figure : The Basic Approach. Initially, the solution to the linear program is at D. This

is not an integer solution, so constraint x' is added, moving the linear solution to F. Then

constraint x" is added, giving H as the linear, and integer, solution.

The cutting plane algorithm is:

function I P (A; c)

x = LP (A; c)

while not(integer(x) or infeasible(x))

b egin

add constraint to A

x = LP (A; c)

end


-----

Figure : Curve Phenomenon in the Basic Approach

Under some circumstances (problem sp eci�c) it is acceptable to add constraints that cut

o� the optimal solution if it makes �nding a go o d solution faster.

. Recent Developments

� Go o d formulations|heuristics and theory. The goal is to get an LP solution as close as

p ossible to the IP solution. Examples: Disaggregation and adding constraints (cuts).

� Prepro cessing|Automatic metho ds for reformulation. There's some interesting graph

theory involved.

� Cut generation (branch and cut). The idea is to add cuts during the branch-and-b ound.

� Column generation|improve formulation by intro ducing an exp onential numb er of

variables. Solve an integer subproblem.

 Airline Crew Scheduling (A Case Study)

. The Problem

American Airlines, and all other airlines, must schedule crew (pilots and �ight attendants)

on �ight segments to minimize costs.

� over ,000 pilots and �ight attendants.

� over . billion dollars p er year in crew cost.


-----

This pro cess assumes that �ight segments are already �xed. In other words, the airline has

already decided which planes will �y where and when. Obviously, determining the aircraft

schedules is an optimization problem in itself, and the  problems are not indep endent. But

treating them indep endently makes them tractable and gives go o d answers.

In these notes  metho ds are covered:

�  0- : TRIP (Trip Reevaluation and Improvement Program) This is a lo cal opti
mization approach which starts with a (hop efully go o d) guess.

�  -present?: Global optimization, approximately.

. Set Covering and Partitioning

Before describing airline crew scheduling we brie�y discuss the general problem of set covering

and partitioning. Set partitioning will b e used in the crew scheduling algorithm.

Given m sets and n items.

(

; if set j includes item i Columns = sets


Aij

cj

xj

Set Covering:

Set Partitioning:


=

0; otherwise Rows = items

= cost of set j

(

; if set j is included

=

0; otherwise

minimize cx

sub ject to Ax � ; x binary

minimize cx

sub ject to Ax = ; x binary


As a standard application, consider a distribution problem with some p ossible warehouse

lo cations (the sets) and some areas (the items) that must b e served. There is a cost asso ciated

with building and op erating each warehouse, and we want to cho ose the warehouses to build

such that all the areas are covered and the cost of building and op erating is minimal.

For example:

set memb ers cost


s

s

s

s

s

s

s


fa; c; dg :

fb; cg :

fb; eg :

fa; dg :

fc; eg :

fb; c; eg :

fc; dg :


-----

 0 0  0 0 0

0   0 0  0

  0 0   

 0 0  0 0 

0 0  0   0



















A =



















The b est cover is fs


; s


; s


g = :. The b est partition is fs


; s





g = :.


. Generating Crew Pairings

A crew pairing is a set of �ights a crew memb er will �y, starting and �nishing at their base.

Pairings are broken into duty p erio ds (one p er day, separated by overnight rests) which are

broken into segments (individual �ights). An example, with base at DFW, is:

Duty p erio d 

Sign in: :00

DFW :00    - 0:00 AUS (segment )

AUS :00    - :00 ORD (segment )

ORD :00    - 0:00 SFO (segment )

Sign out: :

Overlay is SFO

Duty p erio d 

Sign in: :00

SFO :00    - :00 LAX (segment )

LAX 0:00    - : SAN (segment )

SAN :00    -  :0 DFW (segment )

Sign out:  :

National pairings typically last - days (i.e., - duty p erio ds). International pairings

may last for a week, b ecause there are generally fewer, longer �ights. A crew memb er will

work  or  pairings p er month. Pairings are actually assembled into groups, called bidlines,

which is yet another optimization pro cess. Recent work has fo cussed on the bidline problem,

but we will not discuss it here. A crew memb er bids for bidlines each month. Bidlines are

then distributed according to seniority based rank.

The optimization problem is: given all the segments that need to b e covered for a month,

�nd the optimal grouping of segments into pairings, according to the constraints and costs

we will de�ne next.

The constraints, apart from the obvious ones (such as segments in a pairing can't overlap

in time) are related to union and Federal Aviation Agency (FAA) rules. For example:


-----

� Maximum  hours of �ying time p er duty p erio d

� Maximum  hours total duty time (which is �ying plus time b etween �ights).

� There is a minimum lay-over time, which dep ends on the numb er of hours �own in the

previous duty p erio d.

� There is a minimum time b etween �ight in the duty p erio d, so that the crew can move

from plane to plane.

The cost of a pairing can include b oth direct and indirect costs (such as employee satis
faction). Example contributors to the cost are:

� Total duty p erio d time  - obviously related to the salary paid.

� Time away from base  - also related to salary paid, but also part of employee satisfaction.

� Numb er and lo cation of overlays  - hotels (at least) are paid for by the airline, and some

cities are more exp ensive than others.

� Numb er of time-zone changes  - an employee satisfaction, and mayb e union requirement.

� Cost of changing planes.

The overall goal is to cover all segments with a valid set of pairings that minimize

cost. We must also consider the numb er of crew available at crew bases (this will also b e

a factor in scheduling �ights in the �rst place). The problem is simpli�ed in part b ecause

�ights are roughly the same each day, but it is made more di�cult b ecause �ight schedules

change at the end of the month. For this reason, in part, pairings are generally done on a

monthly basis.

One p ossible approach is to consider all valid pairings and generate costs for each. Then

solve it as a set covering problem:

minimize cx

sub ject to Ax � ; x binary

(

; if pairing j covers segment i


Aij

cj

xj


=

0; otherwise

= cost of pairing j

(

; if pairing j is included

=

0; otherwise


Problem: There are billions of p ossible pairings. For the metho ds we will discuss, a

subset of p ossible pairings is considered and in some way optimized. For example, with the

segments:


-----

. DFW 00-00 LGA

. LGA 00-00 ORD

. ORD 00-00 RDU

. ORD 00- 00 DFW

. RDU  00-00 LGA

. RDU  00-00 DFW

. LGA 00-00 ORD

. DFW 00-00 RDU

we might generate the p ossible pairings (this is not an exhaustive list):

. DFW - LGA - ORD - DFW

. LGA - ORD - RDU  - LGA

. ORD - RDU  - DFW - LGA - ORD

. DFW - RDU  - DFW

. DFW - RDU  - LGA - ORD - DFW

which corresp onds to the matrix


 0  0 0

0   0 0

0   0 0

 0 0 0 

0  0 0 

0 0   0

 0 0 0 

0 0 0  

































A =

































where each column is a pairing (set) and each row is a segment (element that needs to

b e covered). Someone can then price each pairing for us giving us a cost vector


c = [c


c


c





c


]


c


. TRIP

TRIP (Trip Reevaluation and Improvement Program) was in use until around  . As

the name suggests, it reevaluates a previous solution and then attempts to improve it. The

initial solution is generally taken to b e that of the previous month, mo di�ed to adjust for

schedule changes. We then rep eat the following steps until no improvement is found:

. Select a small set of pairings from the current solution. The pairings selected should

come from roughly the same region (covering similar cities). We will generally cho ose

-0.


-----

. Generate all the valid pairings that cover the same segments. There will typically b e a

few thousand. Note that if we chose pairings from disjoint cities in the previous step,

we would b e able to generate no new pairings for this step.

. Generate the cost of each new pairing.

. Optimize over these pairings by solving the set partitioning problem. This will generate

a new set of pairings that cover the same segments but at minimal cost.

The advantage of this metho d is that it solves small sub-problems. The big disadvantage is

that it only do es lo cal optimization. If �nding a b etter solution requires optimizing over a

large numb er of p ossible pairings and segments, we won't �nd it.

. New System

Describ ed by Anbil, Tanga and Johnson in   (IBM Systems Journal, ()). The system

may have b een in use since then, although we don't know if it has b een replaced by a b etter

technique. A later pap er on the bidline problem suggests it hasn't. The basic algorithm is:

. Generate a large p o ol of pairings (around  million).

. Solve an LP approximation using a sp ecialized technique.

. Uses branch-and-b ound for the IP solution, but with heuristic pruning.

Each linear program solved takes around  hour. The algorithm do es not guarantee the

b est solution for the chosen p o ol b ecause of pruning, but it do es generate signi�cantly b etter

solutions than the previous metho d.

.. Generating a Po ol of Pairings

This is sp eculative, since the authors say very little ab out it.

We need to generate  million initial pairings out of billions of p ossible pairings.

. � No de: time and airp ort

� Edge: (directed) �ight segment, wait time, or overlay

� Edge weight: \excess cost" of edge. The excess cost is the amount that edge

would cost ab ove the minimum it could cost. For example, there might b e a �xed

cost for a wait indep endent of its length (just to get on and o� the plane) and

we don't include this, and a variable cost based on the length, and we do include

this.

. Find the  millions shortest paths in the graph that start and end at a crew base.

No des in the graph will generally have many edges coming in and going out. Incoming

edges will b e wait times and overlays ending at that time, and �ights arriving at that time.

Outgoing edges will b e overlays or wait times starting at that no de, and �ights leaving at

that time.

The algorithm given is a heuristic that prefers short time away from base.


-----

.. Solving the LP Approximation

An LP problem with  million columns is to o big to solve directly, so instead the following

is done (referred to as the SPRINT approach, Figure ):

. A = select a small set of m columns (each column is a pairing). m � 000

. Rep eat until the optimal is found:

� Optimize based on A

� Use the basis generated to \price" the remaining variables. Then set A to the m

�


new \b est" columns. (i.e., minimum r = cb


B


N � cn


)

|Old Subproblem|Col2|Col3|
|---|---|---|
|837 4163|||
||||
||||


Figure : The SPRINT approach to solving the  million column problem. The numb er of

rows is , which also gives the numb er of columns in the basis. The basis is always kept

for the next round. The remaining 000 �  =  columns from the subproblem are

combined with all other columns to select the b est ones for the next round.

.. Using the LP for the IP

In practice, the variable values for the optimal LP solution are spread b etween 0 and .

This says that the optimal linear solution is to use pieces of many pairings to cover all the

segments|it's like saying we want part of a crew p erson. Obviously, we need to either use

all or none of a pairing.

The intuition for generating the IP solution is to lo ok for follow on segments. A follow on

for a segment is simply the segment that follows it in the �nal set of pairings. The heuristic

we will use for pruning is to assume that a pair of adjacent segments that app ear in many

go o d pairings should b e a follow on in the �nal solution.

So we run the following algorithm to select exactly which pairings to use:


-----

� Solve the LP approximation across  million columns (as just discussed).

� Select approximately 0K pairings with the b est reduced costs.

� Rep eat until all segments have a follow on (or end at base):

. For all columns (pairings) with nonzero values in the linear program solution,


consider all adjacent segments (si


; sj


) in the itineraries (this includes wraparound


so the last segment in the itinerary is followed by the �rst). Note that if there are

n rows (segments) then at most n columns will have nonzero values in the linear

program solution (i.e. only the basis can have nonzero values).


. For each follow-on (si


; s


j


) b eing considered weight it with the sum of the values


of the linear program solution for the column (pairing) it app ears. For example

if (,) are adjacent in pairing  which has value . and pairing  which has

value ., then its total weight will b e .. Select the follow-on with the largest

weight. The intuition is that this follow-on o ccurs in many go o d segments, so we

will assume it b elongs in the �nal solution. This is similar to cho osing a variable

to �x in the implicit enumeration algorithm.


0

) and throw out all the pairings that include (si


0

. Fix (si


0

; sj


; sk


); k = j . This is the


pruning step.

. Resolve the LP (across the 0K pairings minus those that have b een deleted).

. If the solution b ecomes infeasible, add columns from the original  million that

satisfy all the follow-ons we have �xed.

As an example, recall our previous set of p ossible pairings, and the asso ciated matrix


= x


 0  0 0

0   0 0

0   0 0

 0 0 0 

0  0 0 

0 0   0

 0 0 0 

0 0 0  

































An LP solution is x


= x


















A = 













= x = x


= =.


The pairings, expressed in term of the order of their segments si


were:


x

x


= (s ;

= (s ;


; s

; s




s


; s

; s


)

)


x

x


= (s


; s


; s

; s


; s

)


)





; s


x

 (s


= (s


; s


)











; s


-----

The follow-ons (including wraparound) and their weights are:

Follow-on Pair Summed Weight

(; ) =

(; ) =

(; ) 

(; ) =

(; ) =

(; ) =

(; ) =

(; ) =

(; ) =

(; ) =

(; ) =

(; ) 

(; ) =

(; ) =

The follow-ons (; ) and (; ) are the only ones that app ear twice. We �x these two

follow-ons (whenever multiple follow-ons have weight , we �x them all). Fixing these follow
ons do es not eliminate any pairings. For the next step we will have to �x the other follow

ons in turn, and see which is b est, or add more pairings.

.. Additional Constraints

We must also somehow account for the numb er of crew available at each base. To do so, we

add constraints on the maximum hours available from each base. This is easy to do in the

formulation of the linear-program by adding a row for each base and then for each pairing

(column) we place the numb er of hours it requires in the row of its home (where it starts

and ends). We then use this as an inequality constraint so the sum of each base-row is less

than the total numb er of hours available at that base.

We also need to patch b etween months. To do this we separately schedule the �rst  days

of each month with additional constraints put in (referring to the previous months ending).

Finally, we must have a scheme to manage cancelled or delayed �ights. Currently this is done

by hand. Every base has a small set of reserve crew which can b e put on duty if required.

.. Conclusions

� Sp ecial purp ose techniques were used.

� The optimization pro cess was largely separated from the cost and constraints rules.

� A  million variable LP was solved as a sub-step, plus a large numb er of smaller LPs.

� It is currently di�cult to �nd out exactly how much money is saved (older pap ers were

far more forthcoming).


-----

� Current and future work:

{ Putting pairings together into bidlines and optimizing jointly. This is really the

same as making the pairings a month long, with lay-over holidays as part of the

\pairings" and additional constraints.

{ Handling real-time constraints (cancellations, rerouting).

{ Joint �ight and crew scheduling. This is a much bigger problem.


-----

Algorithms in the Real World Notes by Aaron Brown

Lecture # (Triangulation ) �c   Aaron Brown and Guy Blello ch

Outline

� Intro duction to Triangulation

� Basic Geometric Op erations

. Degeneracies and Precision Issues

. Line Side Test

. In-Circle Test

� Convex Hulls

. Dual Problem: Convex Polytop es

. Algorithms

{ Giftwrapping

{ Graham Scan

{ Mergehull

{ Quickhull

� Voronoi Diagrams

� Delaunay Triangulations (dual of Voronoi diagrams)

. Prop erties

. Algorithms

{ Naive Algorithm

{ Solution via Reduction to D Convex Hull

{ Direct Algorithms

The following three lectures cover triangulation, which is one of the many problems in

the larger �eld of \computational geometry". Problems in computational geometry have

found many applications in industry. We will also cover convex-hulls and Voronoi-diagrams

b ecause they are closely related to triangulation.


-----

 Intro duction to Triangulation

Triangulation is a pro cess that takes a region of space and divides it into subregions. The

space may b e of any dimension (although we will fo cus primarily on the two-dimensional

problem here), and the subregions typically are shap ed as triangles (D), tetrahedrons (D),

etc. The goal of triangulation is to pro duce a sub division that ob eys certain \nice" prop erties,

for example one in which the output triangles are as close to equilateral as p ossible.

Triangulation is used in many real-world applications. One such application is �nite

element simulation, in which a partial di�erential equation (PDE) is simulated over a con
tinuous surface or space by �rst using a triangulation to break the space into small, discrete

elements, then simulating the PDE discretely over the elements. Finite element simulations

are common in �uid �ow applications and similar problems; an example that illustrates the

role of the triangulation can b e seen at:

http://www.cs.cmu.edu/~scandal/applets/airflow.html

Other imp ortant applications of triangulation include:

� Surface approximation: a continuous surface is approximated by a mesh of triangles.

This is used in graphics applications (e.g., face representation), compression of surface

representations, interp olation of surfaces, and construction applications (e.g., optimiz
ing dirt movement to contour a region for new construction).

� Nearest neighbor structure identi�cation: the triangulation includes data identifying

the nearest neighb ors of each p oint in the triangulated data set. This is p otentially

useful for clustering applications, etc.

In general, triangulation op erates on several di�erent typ es of input. The simplest case

(and the one that we fo cus on in these notes) is when the input is just a set of p oints which

de�ne the vertices of the output triangulation. Another p ossibility is that the input data

is a b oundary de�ning a region of space. In this case, the triangulation must generate the

interior p oints needed to complete the triangulation. Finally, the input can b e sp eci�ed

as a density function '(x; y ; z ), which sp eci�es the density of triangles across the region to

b e triangulated. This last format is esp ecially useful in simulation, as it allows the p erson

developing the mo del to fo cus triangle detail (and thus simulation accuracy) on critical

p ortions of the mo del.

 Basic Geometrical Op erations

. Degeneracies and Numerical Precision

Before getting into the triangulation algorithms themselves, we �rst need to consider two im
p ortant issues that arise when these algorithms are implemented in the real world: handling

of Degeneracies and numerical precision.

Degeneracies o ccur (in two dimensions) when three or more p oints are co-linear, or when

four or more p oints lie on the same circle. Sp ecial care is often needed in triangulation

algorithms to make them robust with resp ect to degeneracies.


-----

Another related problem that crops up in the real world is the issue of numerical precision.

Since (in general) computers op erate with only a �xed amount of �oating-p oint precision

errors are intro duced by most arithmetic op erations. These errors can lead to inconsistent

answers, esp ecially when p oints are almost degenerate. For example if three p oints a, b and

c are almost on a line the answer to whether a is ab ove b � c could di�er dep ending on how

you calculate it. There are three p otential solutions to the numerical precision problem (and

the related degeneracy problem):

. Assume that the problem do esn't exist. Many existing implementations do this, but

it is a bad idea.

. Design the algorithm to b e robust with resp ect to degeneracies and to lack of precision

(e.g., by using exact or adaptive arithmetic). This is the b est solution.

. Randomly p erturb the input data to avoid degeneracies. This may work in most cases,

but the p ossibility of degeneracies or precision problems still remains.

Luckily, most triangulation algorithms only use two basic op erations which are sensitive

to degeneracies and numerical precision: the line side test and the in-circle test. These

op erations encapsulate all of the needed co ordinate comparisons, and thus they are the only

routines that need b e implemented in in�nite-precision or adaptive-precision arithmetic. The

rest of the triangulation algorithms are primarily combinatorics and graph manipulations.

. The Line-side Test

Given a p oint C and a line AB, the line-side test answers the question: \is C ab ove or b elow

AB ?"

tB

��

�

�

�

� t

C

�

t�


A

The line-side test is easily implemented via a matrix determinant op eration; if the deter
minant op eration is built with adaptive-precision arithmetic, the line-side test will b e stable


with resp ect to numerical precision. Let the line b e de�ned by p oints A = (xa


; ya


) and


B = (xb


; yb


), and let the test p oint b e C = (xc

�

�

� xa

�


D =


�

�

�


; yc ). Then let:

�

�

ya  �

�

yb  �

�

yc  �


xb

xc


-----

(,)

t


(0,0) t                    - t(,0)

Figure  : Example of applying the line-side test.

Then the p oint C is \ab ove" the line A � B i� D - 0. Notice as well that the area of triangle

AB C is given by D =.

As an example, consider the line AB and the p oint C with A = (0; 0), B = (; 0), and

C = (; ), as illustrated in Figure  . In this case,


t 

0 0 

 0 

  




�

�

�

�

�

�

�


D =


�

�

�

�

�

�

�


=  - 0:


Thus, C is ab ove AB, and the triangle area is

. The In-circle Test


= .





Given three p oints A, B, C, and D, the in-circle test answers the question: \is D in the

circle de�ned by A, B, and C ?"

B

#s

s

A

s

D

s

C

"!

As in the line-side test, the in-circle test can b e implemented with a matrix determinant.

Again, if the determinant op eration uses adaptive-precision arithmetic, the in-circle test

should b e stable. Notice, however, that A, B, and C only de�ne a unique circle if they are

not colinear.


As b efore, let A = (xa


; ya


), B = (xb


; yb ), C = (xc


; yc


), and D = (x


d


). Then the


; yd


particular matrix determinant used for the in-circle test is:


xa

xb

xc

xd




+ ya



+ y


b



+ yc



+ y

d


ya

yb

yc

yd




xa



xb



xc



x

d


�

�

�

�

�

�

�

�

�











D =


�

�

�

�

�

�

�

�

�


Then the p oint D is in the circle de�ned by AB C i� D - 0.

Notice that this algorithm generalizes to higher dimensions (as do es the line-side test). In

this case, in d dimensions, d +  p oints determine the d-dimensional sphere, and D b ecomes

a (d + ) � (d + ) determinant.


-----

 Convex Hulls

Given a set of p oints S, the convex hul l problem is to �nd the smallest convex region that

contains all p oints in S . The b oundary of the region is called the convex hul l of S, and is

usually sp eci�ed by a set of p oints and their neighb or relation.

� Extreme Point

�

Xs��


��

�

s

s


XXXXX

s

s

s

s


�

�

�

L

L

s L

L s

�

@I

� @

�

�

�


�s

�

�

�

s

�

s


s

L

L

L


Convex Hull


�

s�

L

L

L


@


Extreme Point


L

L


s


as aaaa(ss ((((((�s�

Figure 0: Example of a D Convex Hull

Convex hulls are well-de�ned in any dimension; a -dimensional example is given in

Figure 0. The -D convex hull can b e thought of the shap e that results when a rubb er

band is stretched to surround a set of nails, one at each p oint in S ; similarly, the -D convex

hull is similar to the shap e that would b e formed if a ballo on were stretched to tightly

surround the p oints S in -space.

. Dual: Convex Polytop es

c


.....�...l.................


�


a


b

e ...................

�e

e


�

.....................


l R�..........................

��l.......�..................l

R�..........................


?

��

I


d


�l c

l

l

�

�

f

�

�


......................#

#I

l

l


�

�

�

�

e

b

ee

e


�


�R�.......................... e


d

e


l�

� l......�..............l

I�

l

#

 #

#


e l


...............#.......

I

#




f


�.I .�..................... #e#

g .#I e


e


�

�I


e

� ...................

e


(a) (b)

Figure : (a) Example D Convex Polytop e Problem (b) Solution

The convex hull problem has a dual formulation in the problem of convex polytopes.

The convex p olytop e problem is to �nd the region in space that is the intersection of a


-----

set of halfspaces (we assume all the halfspaces include the origin). This problem arises in

certain linear programming algorithms. Figure a illustrates an example of a -D convex

p olytop e problem. The solution to a convex p olytop e problem in general is a list of the

\non-redundant" half-spaces (e.g., those lines, planes, or hyp erplanes that de�ne the convex

region). In the example of Figure a, the solution is (b; d; c; f ; e), illustrated in Figure b.

The convex hull problem and the convex p olytop e problems are duals, as a problem and

solution to one can b e mapp ed into a problem and solution to the other. Thus an algorithm

for �nding convex hulls can b e used to �nd convex p olytop es as well.

The transformation that takes an instance of the convex p olytop e problem to a convex hull


problem is the following, in D. Let the ith half-space b e de�ned by the line `i

In higher dimensions, the equation is of the form:

d

X


: ai x + bi


y = .


`i


ij xj


= :


:


a


j =

Then the dual problem is to �nd the convex hull of the p oints pi

!


, where (in D):

!

aid


;




+ ai


ai

;



+ bi

ai




ai


bi

+ b




:



i

; : : : ;


a




i


In higher dimensions,


Pi

;



id


=



ai


:


Pi


=




ai




+ ai


ai

+ � � � + a




+ ai




+ � � � + aid


ai + ai + � � � + aid ai + ai + � � � + aid

See Figure  for a graphical illustration.

` Z

Z "

"

" Z

" Z

" Z

@ " Z

""@ Z �� =)

` @ ��ZZ

@ ��

@��

��@


a




i


p

s s p

D

D

D

D

s Ds


s


p


D


p


@


`

`

Figure : Mapping Convex Polytop es to Convex Hulls

. Algorithms for Finding Convex Hulls

The following is a summary of the most p opular algorithms for �nding convex hulls. Notice

that the algorithms are classi�ed into categories that are similar to those used to classify

sorting algorithms. Those marked with a dagger (y) are considered further b elow. In the

time b ounds, n is the numb er of p oints in the input set S, and h is the numb er of p oints

in the hull H . The algorithms and b ounds we list here are for -dimensions although many

algorithms generalize to higher dimensions.


-----

� Basic algorithms

{ Giftwrapping


: O (nh)


y


� Incremental algorithms

y


{ Graham Scan : T (sort) + O (n)


{ Unordered Insertion: T (sort) + O (n)

� Divide and Conquer algorithms

{ \Merge-based" D&C algorithms

y


� Mergehull : T (sort) + O (n)


{ \Divide-based" D&C algorithms


y





) worst, O (n log n) average


� Quickhull


: O (n) b est, O (n


� Kirkpatrick-Seidel: O (n log h)

{ Random Sampling: O (n log n)

The theoretical lower-b ound on �nding a convex hull is O (n log h).

.. Giftwrapping

The idea b ehind the giftwrapping algorithm (in -d) is to move from p oint to p oint along

the convex hull. To start, an extreme p oint is chosen as the �rst p oint on the hull (this can

b e done easily by cho osing the p oint in S with largest x-value).

Then, on each step, the p oint in S with the smallest angle � is chosen to b e the next

p oint in the hull, where � is de�ned as the angle b etween a ray originating at the current

p oint and continuing along the ray that connects the previous and current p oints, and a ray

connecting the current p oint and the test p oint. This is explained much more clearly in a

picture in Figure .

Each step of the algorithm takes O (n) time, since jS j = n and p otentially all p oints in

S must b e examined to determine the one with minimum angle. Since the algorithm do es

h steps (one for each p oint on the hull), the running time of the algorithm is O (nh). If all




the p oints lie on the hull then the algorithm will take O (n


) time. Because of this worst

case b ehavior the algorithm is rarely used in practice, although it is parallelizable and do es

generalize to D.

Note that this algorithm also requires additional primitives b esides the line-side and

in-circle tests.

.. Graham Scan

The Graham Scan algorithm constructs the convex hull in two pieces (the top and b ottom),

then connects them together. For each half, it b egins by sorting the p oints in decreasing

order of their x co ordinates. Then, starting at the largest (or smallest) x, it scans through

the p oints, building the hull along the way. As it encounters a new p oint, it connects it to


-----

.


�0..

.

.

L ..

.

L .




L

L

L

L

L

L


XXX


.

..

..

� ....

XX..

t




. . .�. �.. . .�. . .tXXXX

�

�

t

t

t




t


t��

t


.


L


t


0


t


t

Figure : Giftwrapping Algorithm

the previous p oint, assuming that it will b e in the hull. If adding that p oint causes the hull

to b e non-convex, the algorithm adds a bridge to the appropriate p oint to ensure that the

hull remains convex. This is illustrated in Figure ; the dashed lines are the bridges added.




.


. . . . . ......�...ese. . . . . . . . .�.Cs

.. � e � C

.

.. � e�s�

... s�� 


. .


.s. . .

�\

\

�

\




C

C

C

C

C


�

�s


.

.

\,.s




,







s


0

Figure : Graham Scan Algorithm

The running time for the Graham Scan algorithm is T (n) = T (sort) + O (n), since the

algorithm must take n steps (one for each p oint in the scan), and the amortized cost p er

step can b e shown to b e O (). Since T (sort) is �(n log n) for comparison-based sorts, the

Graham Scan algorithm is essentially an O (n log n) algorithm (unless the data lends itself

to a non-comparison-based sorting algorithm).

Finally, note that this algorithm is inherently sequential, and thus do es not parallelize

well. Even on a sequential machine, it is not the most e�cient in practice. Furthermore,

it do es not generalize to higher dimensions. However, it do es have an interesting historical

note in that it was develop ed at Bell Labs in resp onse to a real application, and thus is one


-----

of the few hull algorithms that were not theoretically motivated.

.. Mergehull

The Mergehull algorithm is a divide-and-conquer algorithm that is similar in structure to

merge sort. Mergehull has a trivial divide phase, and do es most of its work during the merge

phase.

Mergehull's divide stage is simple: the algorithm merely splits the input set S into two


subsets S


, S


by one of the co ordinates. It then recursively solves S


and S


(e.g., it


computes the convex hull for b oth S


and S ).


After the recursion returns, the algorithm must merge the two convex hulls for S


and


S


into a single convex hull for S . Conceptually, this involves lo cating two bridges b etween


the hulls|line segments connecting two p oints in S


to two p oints in S . Once the bridges


are added to connect the two hulls, the interior segments of the subhulls are discarded. See

Figure  for an illustration. Finding the bridges and discarding the inside edges requires an

Overmars dual binary search, which takes time O (log n). Note that it is not su�cient just

to place the bridges b etween the minima and maxima of the two sub-hulls.


�� .ls . .l. . . . . . . . . . . . . . . . . . . . . .Xs XXXXXXs

�s ls L

�� E L

s� E LL

E

�� EEs �

� �

�

� ��s

� ..s

�QsQQQ �s��� eee � ��

Q.�s�. . . . . . . . . . . . . . . . . . . . . . . . . . . . .e. .�s�


s


.


Split

Figure : Mergehull Algorithm

If we assume that the p oints are presorted (to make the sub division in the divide phase

take constant time) and that tree data structures are used throughout, the recurrence for

the mergehull algorithm is:


�


T (n) = T


�

n




+ O (log n)


= O (n)

When added to the time of the original sort, the total time is O (n log n).


-----

It is interesting to note that the mergehull algorithm parallelizes, and that the parallel

algorithm do es well in practice (it obtains a nearly linear sp eedup with the numb er of pro
cessors). The parallelization is rather simple: the set S of input p oints is �rst divided into P

regions (rather than in half, as ab ove). Each of the P pro cessors is then assigned one of the

regions, for which it sequentially generates a convex hull. Then, the P regions are merged

by �nding bridges in parallel.

Finally, the mergehull algorithm can b e generalized to three or more dimensions. As

the dimensionality increases, however, the merge b ecomes more di�cult. For example, in

D, the bridges b etween subhulls are no longer line segments, but instead are surfaces that

connect the hulls. Finding these surfaces is more exp ensive: in D, the merge takes O (n)

time, so the total time for mergehull is O (n log n), even when the input p oints are presorted.

.. Quickhull

The Quickhull algorithm is another variant on the recursive divide-and-conquer metho d

for �nding convex hulls. Unlike the mergehull algorithm that we have just seen, quickhull

concentrates its work on the divide phase of the algorithm, and uses a trivial merge step.

It is thus very similar in structure to the quicksort sorting algorithm, and we will see b elow

that it has similar time complexity.

Quickhull works (in D) by lo cating three p oints A, B, and C on the convex hull of

its input S (with C ab ove b oth A and B ), then recursively re�ning the hull b etween AC

and C B . Since b oth halves of the recursion meet at C, which is on the hull, the merge is

essentially a no-op. When the algorithm completes, the upp er half-hull b etween A and B

will b e complete. The algorithm is then rep eated for the lower half-hull. Figure  details

the pro cess graphically.

C

.t

.H

s ��.... Hs HHs

� s .. HH s

�� s ..... dsmax s HHHH

A .�t. . . . . . . . . . . ... . . . . . . . . . . . . . . . . . . . . . . H. .H. .t B

s s

Figure : Quickhull Algorithm

The tricky part in Quickhull is implementing the divide stage. A typical algorithm (which

works well in the average case but do es not guarantee the b est time b ound) is the following.

We start out with two p oints A, B on the convex hull. These can b e found on the �rst

iteration by taking the p oints in S with minimum and maximum x co ordinate. Then, apply

the following algorithm:

. Find the furthest p oint C from the line joining A and B . To do this, the line-side test

(describ ed in Section .) can b e used, as it returns the area of the triangle AB C, and


-----

the triangle with largest area is the one that has the furthest p oint C . Note that, when

building the upp er half-hull, C should b e ab ove AB, whereas C should b e ab ove the

inverse line B A when building the lower half-hull.

. Discard all p oints in triangle AB C, as they clearly will not b e on the b oundary of the

�nal hull (since AB C is contained within the hull).

. Recurse on A; C and C ; B to fully re�ne the hull b etween A and C, and b etween C

and B .

. Connect the two resulting hulls at C .

. Rep eat for the lower half-hull, and connect it at A and B .




The worst-case running time of the quickhull algorithm is O (n


), for if the splits (choices


of C ) are bad, the algorithm may only eliminate one p oint on each recursion, resulting in a

recursion depth of n and a p er-recursion cost of n. The input distribution that forces this

worst-case time is if all the input p oints are distributed along a semicircle with exp onentially

decreasing distance from the left-hand p oint (see Figure ).

Figure : Worst-case Input Distribution for Quickhull

Despite this p o or worst-case b ound, quickhull runs in O (n log n) time for most \realistic"

p oint sets. In fact, in practice it can often run as fast as O (n), since the algorithm discards

p oints in step , ab ove, reducing the size of the input set for later recursions.

There is also a technique develop ed by Kirkpatrick and Seidel that lo cates the ideal

\pivot" p oint C using two-variable linear programming. This variant guarantees the optimal

time complexity of O (n log h). The technique is conceptually similar to the metho d of using

the true sample median to force quicksort to run in �(n log n). The technique involves

�nding the bridge segment that connects across the median x co ordinate b efore recursively

solving the subhulls themselves. This is the same bridge as found by mergehull, but instead

of requiring the solved subhulls for each half it uses linear-programming to �nd the bridge

directly in O (n) time.

Finally, note that quickhull parallelizes easily, and generalizes to three dimensions (in




which case the running time is O (n log


h) for an algorithm by Edelsbrunner and Shi).


-----

 Delaunay Triangulations and Voronoi Diagrams

We will not consider the problem of generating Delaunay triangualations, but we �rst con
sider the dual problem of generating Voronoi Diagrams.

. Voronoi Diagrams


A Voronoi diagram (or Dirichlet tessellation) is a partition of space into regions V (pi ) based


on a set of input p oints pi


 S such that:


V (pi


) = fp : jpi


� pj � jpj


� pj;  j = ig:


where jpi


� pj indicates the distance from pi


to p (here we assume this distance is Euclidean,


but later we will brie�y discuss other distance metrics). What this prop erty means is that,


for a p oint pi


, its Voronoi region V (pi


) will contain all p oints that are closer to pi


than to


any other p oint in S .

Voronoi diagrams are well-de�ned in any dimension. In two dimensions, the Voronoi

regions are convex p olygons; in three dimensions, they are convex p olyhedra, and so forth.

Figure  gives an example of a D Voronoi diagram.

��

t

J � t

J �

J ���H

J �� H

t


J�

�

�

�

�


HH


t


Figure : A D Voronoi Diagram

Note that there are actually many di�erent ways to represent the diagram. One way is

to return for each original p oint the set of Voronoi neighb ors (p oints that share a Voronoi

edge). Another is to return the graph structure formed by the Voronoi edges.

. Delaunay Triangulations

The dual graph of a Voronoi diagram is called a Delaunay triangulation. Given a Voronoi

diagram, the Delaunay triangulation is formed by connecting the p oints at the centers of

every pair of neighb oring Voronoi regions. See Figure  for an example. Note that the

the Delaunay triangulation will always consist of triangles, since the Delaunay edges join

neighb oring Voronoi regions, and two neighb or regions of adjacent Voronoi edges will them
selves b e neighb ors. Note that a Delaunay edge is always p erp endicular to the Voronoi edge

that the two neighb ors share, but that the Delaunay edge do es not necessarily cross the

corresp onding Voronoi edge, as illustrated in Figure 0.


-----

t

PP

%L P


t

�S

S

� . .


.

.

.

.

.

.

.

..


.


.


.


.

.

.

.

.

.

P.

. P


.


.


.


. . ..!�St.�.�..S�.!..�..S......!.....S..... ..tXS!�".�.!�X.�S�"..�.C.h"tC..%..XC.......C..C%ht,.tl,.X....%.h..l..,.X...........hl.,lX....L..ht.Lh,"..L."..........L...t.@"..."".......@.."".......@..."."@P... ...t"�P�.��.��t. . . .

.

.

.

.

Figure  : A Delaunay Triangulation (and asso ciated Voronoi diagram)

. . . . . . . . . .. .. .. ..sSs�..�..S�.. ..S�.. ..s.. .. .. ..


Figure 0: Example of a Delaunay edge that do es not cross its Voronoi edge


-----

Finally, note that degeneracies can b e encountered in forming a Delaunay triangulation.

In particular, if two Voronoi regions intersect only at a corner, there will b e more than one

p ossible triangulation (recall that a triangulation contains only non-overlapping triangles).

This is illustrated in Figure .

Voronoi Edge

�

�

�

DelaunaPotenytialEdge ..ss..-.............................................ss��� Delaunay Edge

Figure : A degenerate case for Delaunay triangulation

. Prop erties of Delaunay Triangulations

Delaunay triangulations have certain \nice" prop erties, including:

� The Delaunay triangulation of a non-degenerate set of p oints is unique. Thus there is

only one triangulation that ob eys the following set of prop erties.

� A circle through the three p oints of a Delaunay triangle contains no other p oints. Also,

the intersection of the three corresp onding Voronoi edges is at the center of the circle,

as shown in Figure . This prop erty generalizes to spheres in D and so forth.

� The minimum angle across all the angles in all the triangles in a Delaunay triangulation

is greater than the minimum angle in any other triangulation of the same p oints.

These prop erties tend to result in triangles that are \fat" (closer to equilateral) rather than

\skinny". This is a prop erty that is highly desirable in applications, esp ecially �nite element

simulations where the geometry of the �nite elements a�ects the accuracy and quality of the

simulation.

. Algorithms for Delaunay Triangulation

The Delaunay triangulation for a set of p oints can b e found using one of several typ es of

algorithms: a naive direct algorithm, by reducing the problem to a convex hull problem and

applying a convex hull algorithm, and by using a direct algorithm. We will consider each of

these cases in turn.


.


  -


-----

Figure : Circle test for Delaunay triangles

.. Naive Algorithm

A naive way of �nding the Delaunay triangulation is the following: for every three-p oint
subset of the input set, check if any other p oint is in its circle. I� not, those three p oints

de�ne a Delaunay triangle.





triples of p oints to check, and


This algorithm runs in O (n




) time, since there are n


each check takes O (n) time (since the in-circle test must b e applied n times). Although

p olynomial-time, this algorithm is quite impractical since, as we will see, there are algorithms

that run in O (n log n) time (and the constant factors in the big-O are quite small).

.. Solution via Reduction to D Convex Hull

A more practical metho d for �nding the Delaunay triangulation of a set of d-dimensional

p oints uses a reduction of the Delaunay triangulation problem to the problem of �nding a

convex hull in d +  dimensions. For the typical D triangulation case, a D convex hull is

used.

The reduction is as follows. The original input p oints P are pro jected upward onto a

three-dimensional parab olic surface centered at the origin. Then, the D convex hull of those

pro jected p oints is found. When the hull is represented as a neighb or graph and pro jected

back down to the two-dimensional plane, the result is the Delaunay triangulation of P . More

precisely, given P, we �rst form:


o


0





P


=


) : (x; y )  P


:


n



(x; y ; x

0


+ y


Then let C =LowerConvexHull(P


), represented as a neighb or graph. Then, the neighb or


graph of C is equivalent to Delaunay(P ).

The reason that this works is related to the prop erties of the Delaunay triangulation,

in particular, the prop erty that states that any circle through three p oints of the input set

containing no other p oints circumscrib es a Delaunay triangle through those three p oints.

Recall that any slice of a D parab olic surface maps onto a circle in the x-y plane. Also,

notice that any face of the D convex hull de�nes a slice through the parab ola. Thus the

pro jection of this slice onto the plane is a circle, and the circle will pass through the pro jection


-----

of the three p oints on the plane. Since the slice is only for a single hull face, there will b e

no other pro jected p oints in that circle, so the pro jection of the hull face de�nes a Delaunay

triangle. Since this works for all hull faces, the result faces of the convex hull in -D are the

Delaunay triangles in -D (when pro jected down).

Using this reduction to �nd the Delaunay triangulation gives an e�cient algorithm that

runs in O (n log n). However, there are still b etter algorithms in practice, such as some of

the direct algorithms describ ed in the next section.

.. Direct Algorithms

The following algorithms can b e used to �nd either Voronoi diagrams or Delaunay triangula
tions, as the two problems are duals of each other. Those algorithms marked with a dagger

(y) are easy to parallelize.


log n)


y




: O (n


� Intersecting Halfspaces


This algorithm works as follows: for each input p oint, draw a line to every other p oint.

Generate a halfspace separating the input p oint from every other p oint (by bisecting

the lines drawn in the �rst step). Compute the halfspace intersection of these halfspaces

(a convex hull problem running in O (n log n)). This gives a Voronoi region. Rep eat

for all n p oints.

� Radial Sweep

� Incremental Construction: O (n log n) (exp ected time)

� Plane Sweep: O (n log n)

� Divide and Conquer Algorithms

{ Merge-based: O (n log n)

y


{ Split-based


: O (n log n)


In this class we will only discuss the incremental and the split-based divide-and-conquer

algorithms.


-----

Algorithms in the Real World Notes by Franklin Cho

Lecture # (Triangulation ) �c   Franklin Cho and Guy Blello ch

� Divide-and-conquer Delaunay triangulation and its parallel implementation

� Meshing (triangulation) given a b oundary

{ Applications to solid mo deling and computer graphics

 Divide-and-Conquer Delaunay Triangulation

In this section, we will examine the divide-and-conquer approach to Delaunay triangulation

by Blello ch, Miller and Talmor. This algorithm p erforms most of the work on split rather

than merge, which allows for easy parallelization. For each recursive call, we keep

� B = Delaunay b oundary of region

� P = Interior p oints


Initially, we set B = Convex Hull(Pinput


) and P = Pinput


� B . We will assume -D data


set for now. We also assume that the input p oints are pre-sorted in x and y . Here is the

pseudo-co de for the Delaunay triangulation algorithm:

Function D T (P ; B )

if jP j = 0 then b oundary solve(B )

else


xm


= median p oint along x-axis


L = split b oundary (set of Delaunay edges along x = xm

l = p oints in L


)


Plef t = fp  P : px < xm ; p = l g

Pr ig ht = fp  P : px   - xm ; p = l g

Tlef t = D T (Plef t, intersect(B ; L))

Tr ig ht = D T (Pr ig ht, intersect(B ;reverse(L))

Return Tlef t and Tr ig ht

In the �rst line of the function, b oundary solve is called if the region contains no interior

p oints. There are known linear-time algorithm to triangulate a region with no interior p oints.

The di�cult part of the algorithm is �nding the Delaunay edges along the line x = xm

(Figure ). As shown in the previous lecture, we can obtain the Delaunay triangulation of





0




= f(x; y ; x


a set of p oints P by pro jecting the p oints onto a -dimensional parab ola P

0


+ y


) :


(x; y )  P g and then pro jecting LowerConvexHull(P


) back onto the x-y plane. Based on


this idea, we �nd the Delaunay edges along x = xm


by �rst pro jecting the p oints onto the


-----




0





parab ola P


= f(x � xm ; y ; (x � x


m)


) : (x; y )  P g, which is centered on the line x = xm

0


.


+ y


Notice that the edges of the lower convex hull of P

00

the x-y plane (Figure ). We then form the set P


by pro jecting the p oints in P


corresp ond to the Delaunay edges on

0


onto the


+ y





00


plane x = xm


, i.e., P


= f(y ; (x � xm

0




)


) : (x; y )  P g (note we have just dropp ed the

00


�rst co ordinate from P


. The lower convex hull of P


(in -D) corresp onds to the Delaunay


edges along x = xm


(Figure ).


Let us analyze the asymptotic b ehavior of the ab ove algorithm. Let n b e the total numb er

of interior p oints (n = jP j), let m b e the numb er of p oints on the b order B, and let N b e

the total numb er of p oints (N = n + m).


The median xm


can b e found in O () since we assume that the input p oints are pre

sorted. The translation and pro jection trivially takes O (n). The convex hull of C can b e

found in O (n) since the p oints are sorted. Since we are dividing the p oints by their median,

we are guaranteeing that each sub-problem has no more than half as many interior p oints


-----

-----

-----

as the original problem. Therefore, the running time of the op erations on the interior p oints

can b e describ e by the following recurrence relation:

n


T (n) < T (


) + O (n)




By solving this recurrence relation, we obtain the total running time of O (n log n) for the

op erations on interior p oints.

Now, let us analyze the b order-merge op eration. For each level of recursion, the b order
merge op erations take O (m) time. Note that we cannot guarantee that the size of the b order

in each sub-problem is half the size of the original b order. However, we can still place an

upp er b ound on the total amount of time sp ent on b order-merge. Given that there are N

total p oints, the numb er of edges in the triangulation of the p oints is b ounded by N . Since

each b oundary edges is counted twice, the absolute upp er b ound on the numb er of edges in

each level of recursion is N . Therefore, an upp er b ound on m on each level of recursion is

N . Since there are at most log N levels of recursion, the total time sp ent merging b orders

is b ounded by N log N = O (N log N ).

Counting b oth op erations on p oints and b orders, the total running time of the algorithm

is O (N log N ) (since n < N ). Note that each op eration on p oints and b orders can b e

parallelized easily.

In practice, the following test results were obtained:

� When this algorithm was tested on b oth uniform and non-uniform inputs, it was found

that input sets with uniform and normal distribution bucket well (i.e., it divides nicely

when the input set is divided along the median). On the other hand, Kuzmin (zo omed)

and line distributions don't bucket well.

� Overall, the running time with non-uniform distributed input set is at most . times

slower than the running time with uniform distributed input. (Previously, the non
uniform inputs to ok at least  times longer).

� This algorithm scales well with problem size, and can solve problems to o big for serial

machine. The parallel algorithm is only ab out  times slower than a sequential co de.

(Previously, the parallel algorithm ran  times slower than a sequential co de).

� This algorithm is a practical parallel D Delaunay triangulation algorithm, and it is

the �rst to b e comp etitive with serial co de.

Do es this algorithm generalize to D? Yes in theory, but the algorithm requires D convex

hull generation as a subroutine, and it is not clear how to parallelize this op eration. Also,

the b order merge is more complicated with D b orders. Generalizing this algorithm to D

would b e an interesting future work.

 Incremental Delaunay Triangulation Algorithm

In this section, we will discuss the incremental approach to constructing the Delaunay tri
angulation. The incremental approach means that the p oints are added one at a time.


-----

Whenever a p oint is added, we up date the Delaunay triangulation so that at each stage, a

complete Delaunay triangulation is generated with the p oints added so far.

In this algorithm, we assume that the p oints in P are already Delaunay triangulated. To

0


add a new p oint p


:


0

. Lo cate the triangle t in D T (P ) which contains p


0

. Add p


0

and add the edges from p


to the three corners of t


. Fix up neighb oring regions by \edge �ipping"

Step  requires more explanation. For each of the newly formed triangle Tnew


Step  requires more explanation. For each of the newly formed triangle Tnew, we p erform

the in-circle-test to see if Tnew is well-formed: we form the circumcircle of Tnew, and test if

it contains any of the other p oints. If it do es, then Tnew is not well-formed, and we \�ip"

the edge (Figure ). This is rep eated for newly created triangles and is discussed in more

detail in Lecture .


the in-circle-test to see if Tnew


###### (a) new point p’ is added to triangle t, and

 new edges are formed to the three corners of t


###### (b) Perform in-circle-test for each sub-triangle,

 and fix up the neighboring region by "edge flipping"


Figure : Step  of the Incremental Delaunay triangulation. If the in-circle-test fails, then

the edge is \�ipp ed".

 Mesh Generation

In this section, we will discuss mesh generation, also called unstructured grid generation, or

just triangulation. Given a b oundary, we want to triangulate the interior by p ossibly adding

p oints. We want the �nal triangulation to have the following prop erties:

. Bounded asp ect ratio for triangles, i.e. triangles that are not skinny (don't have any

small angles).


-----

. As few triangles as p ossible. This criterion is imp ortant for �nite element analysis, for

example, b ecause the running time is a function of the numb er of triangles.

Although, as discussed previously, Delaunay triangulation guarantees the triangulation of

a set of p oints that has the greatest minimum angle (at least in -D), as Figure  illustrates

it is often p ossible to create triangles with larger minimum angles by adding extra p oints.

###### (a) Input Widget

 (b) Triangulation without adding points

 (c) Triangulation with 6 interior and 10

 boundary points added

Figure : Extra p oints can b e added to reduce the asp ect ratio of the triangles

. Rupp ert's Algorithm

�


Given a set of D segments and an angle � � 0

input set such that for each triangulated region:

. no angle is less than �


, Rupp ert's algorithm triangulates the


. numb er of triangles is within a constant factor of optimal

�


�


Although � � 0


is the limit that has b een proved, � � 0


works well in practice.


Rupp ert's algorithm works very well in practice, and is used in the \triangle" application.

The basic idea b ehind Rupp ert's algorithm is:


-----

. Start with Delaunay triangulation of endp oints of segments. As shown previously,

Delaunay triangulation would pro duce the maximum minimum angle.

. Get rid of skinny triangles by

� splitting segments in half

� adding a new p oint in the center of existing triangle

To describ e the algorithm, we will use the following terminology. A segment denotes

either the input segment, or part of an input segment. An edge denotes a Delaunay edge. A

vertex denotes endp oint of a segment or an edge (the Delaunay vertices). A p oint encroaches

on a segment if it is inside the segment's diametrical circle. A diametrical circle of a segment

is a circle with the segment as its diameter.

Here is the pseudo-co de for Rupp ert's Algorithm:

S = input segments

V = endp oints of S

T = D T (V ) // Delaunay Triangulation

Rep eat

while any s  S is encroached up on, split s in half, up date T

let t b e a skinny triangle in T (i.e., t contains an angle smaller than �)

p = circumcenter(t)


if p encroaches on segment s


; s


; ::; sk


,


split s

else


; s


; ::; sk


in half, up date T


V = V [ p, up date T = D T (V )

Until no segment is encroached up on and no angle is < �

Output T

Figure  illustrates Rupp ert's algorithm:


-----

###### smallest angle


###### (c) p is the circumcenter of a skinny triangle. p encroaches on s3 and s4, and therefore we must split s3 and s4


###### s q p

 (b) p and q encroach on s. Therefore, we split s

 (d) After s3 and s4 have been split


Figure : Successive steps of Rupp ert's algorithm


-----

Let us analyze the running time of this algorithm. If output has n triangles, then the

algorithm go es through at most n iterations, and each iteration makes at most n up dates.




Therefore, the worst-case running time is O (n


). The algorithm runs in O (n log n) time in


practice. It is currently not known whether Rupp ert's algorithm can b e parallelized.

The pro of of \within constant factor of optimal" clause is based on the concept of \lo cal

feature size". Given a p oint x, the lo cal feature size lfs(x; y ) is de�ned to b e the minimum

radius of the circle centered at (x; y ) that contains two non-incident segments. lfs(x) is a

continuous function. We will state without pro of that:

Z




V < C


dxdy


A




(lfs(x; y ))


where V is the numb er of vertices returned by Rupp ert's triangulation, C is a constant

and A ranges over the area of the widget. Furthermore it is p ossible to prove that any

triangulation requires at least

Z




C


dxdy


vertices (C


< C




A (lfs(x; y ))

). These together show that the numb er of vertices generated by Rupp ert's


algorithm is within a constant factor of optimal.


-----

Algorithms in the Real World Notes by Michael Downes

Lecture # (Triangulation ) �c   Michael Downes and Guy Blello ch

� Mark Adams : Finite Element Metho ds

. FEM Intro

. Approximating the Weak Form with Subspaces

. Picking Go o d Subspaces

. Linear System Solvers

. Multigrid

. Unstructured Multigrid Algorithms

. Parallel Multigrid Solver for FE

� Distance Metrics for Voronoi Diagrams and Delaunay Triangulations

� Surface Mo deling Using Triangulation

. Terrain Mo deling

(a) Metho ds for Representing Terrains

(b) Bene�ts of Triangulation

(c) Algorithm

 Triangulation in Finite Element Metho ds (Mark

Adams)

We b egin with a lo ok at the �nite element metho d (FEM) and a parallel algorithm for solving

FEM problems which makes use of the Delaunay triangulation.

. FEM Intro

We will examine the basic FEM approach by applying it to the heat equation,

!





@


T




@




T




@




T




k


+


@ T

@ t


+


+ Q = �c


@ x


@ y


@ z


de�ned on a domain � with b oundary @ � where T is temp erature, and Q is the heat

generated in the domain. Take T = 0 on the b oundary of �, and for simplicity assume that

we are lo oking at the steady state case in D, so


@ T

@ t


@


@ y




T




@




T




= 0:


=


=


@ z


-----

Thus, we have





@


T




k


+ Q = 0:


@ x

This is referred to as the strong form of the equation. In order to apply the �nite element

metho d, we must develop a computable form of this equation : the weak form. We start by

writing a residual for the strong form as




@


T




R�


= k


+ Q � 0:


@ x

Using this equation, the so-called weighted residual form is

Z


W �R�


@ � = 0


�

where W is some arbitrary function of p osition with the prop erty that W s:t: W = 0

on @ �. This assumption of W = 0 on the b oundary, called a Dirichlet b oundary condition,

gives us a particular weak form of the original equation called the Galerkin form. We have

!

Z 


@


T




W � k


+ W � Q


@ � = 0;


� @ x

and by applying integration by parts, we arrive at the weak form.

!

Z

@ W @ T

k � W � Q @ � = 0

� @ x @ x

. Approximating the Weak Form with Subspaces

We now apply the �nite element approximation by discretizing the domain of the problem

into no des and intro ducing functions which interp olate the solution over these no des. In

other words, we construct basis sets � and ' such that

n

X


~

T  span(�

~


; � ;


; :::�


n)

m )


� �i


~

T =

~


ui

i=

n

X


W  span('


; '


; :::'


W =


wi


� 'i








where the ui


form the solution we seek, and the wi


i=

are the weights intro duced earlier. The


sets � and ' are often taken to b e the same. This pro duces a particular sort of approximation

known as a Bubnov-Galerkin approximation.

Applying these subspace de�nitions to the weak form of the heat equation, we get

!

n Z n

X X @ 'i @ �j

wi uj k � 'i � Q @ � = 0 wi:

� @ x @ x

i= j =

Thus, for i =  : : : n

!

n Z Z

X @ 'i @ �j

uj k @ � = 'i � Q@ �:

� @ x @ x �

j =


-----

We now have a linear system Au = f which we can solve for u. In this case,

!

Z


@ �j

@ x

!


@ �


�

Z

�


@ 'i

@ x


'i


k


and


Aij

f


=

i =


� Q


@ �:


. Picking Go o d Subspaces

In order to achieve accurate results, we must take care in selecting the subspaces � and '.

Metho ds which make use of sine transforms and wavelets, referred to as sp ectral metho ds

and element free FEM, resp ectively, are o ccasionally used, primarily in research. However,

the ma jority of FE work uses piecewise linear (or quadratic etc.) p olynomials. Figure 

illustrates the use of D piecewise linear p olynomials for the subspaces. Here we have chosen

n = , and we have applied the Bubnov-Galerkin approximation of � = '. As can b e seen in

the �gure, the domain � has b een discretized into no des, represented by empty circles. The

hat functions interp olate b etween solutions at no dal p oints. Note that we assume that we

have solution values at the b oundaries of the domain. Figure 0 depicts a similar situation

but this time in D with D piecewise linear p olynomials. The dotted lines show the hat

function over one no de in the mesh.

The no des which discretize the domain de�ne the elements which give the metho d its

name. In D these elements are usually triangles or quadrilaterals. In D they are normally

tetrahedra or hexahedra. Hexahedral elements have a part of a higher order space than

tetrahedral elements, so one can use larger hexahedral elements and less of them to get a

solution which is as accurate as a solution generated from a mesh with a larger numb er of

smaller tetrahedral elements. This can cut down on computation time. However, it is much

easier to automate the pro cess of generating triangular and tetrahedral meshes, so these

elements are particularly appropriate for large, complex mo dels.

. Linear System Solvers

We now turn our attention to metho ds for solving the linear systems generated by the FEM.

This is normally the most costly step in a FEM solution. Recall that we want to solve

for u in Au = f . In this equation, A is sparse and there are roughly a constant numb er

of non-zeros p er row. In addition, A is symmetric in structure (i.e., nonzeros vs zeros are

symmetric), and can have symmetric or non-symmetric co e�cients. Finally, we normally




have a fairly large system with 0


+

� 0


equations. We can solve this system using either


direct or iterative metho ds which we brie�y examine b elow.

.. Direct Metho ds (e.g., Gauss Elimination)

T





Start by factoring A ) LU s:t: L


; U Upp er Triangular. The cost of this step � O (n

=


):


Now, solve Ly = f for y and U u = y for u. The cost � O (n


):


-----

###### Ω

 φ

 φ

 φ

 φ

 φ

Figure  : D Piecewise Linear FE Shap e Functions


###### 1

 2

 3

 4

 5


The cost of this metho d is sensitive to vertex ordering, so we have a graph problem. This

ordering problem has b een studied extensively, and is NP complete. Successful solutions

include nested dissection, a divide and conquer algorithm, and minimum degree, a greedy

algorithm.

.. Iterative Metho ds

The total cost of any of these metho ds is (numb er of iterations) �O (n), since for FE dis
cretizations a matrix vector multiply has cost = O (n).

Matrix Splitting

Take A = (D � U ) where, for example, D = diag onal ) J acobi

�


Substituting into the equation Au = f and rearranging, we have u = D

�


(f + U u) ),


so the iterative form is uk +


= D


(f + U uk


).




The numb er of iterations � O (n)

Conjugate Gradients (CG)


f ; :::g


Lo ok for the "b est" solution in spanff ; Af ; A




f ; A


-----

Figure 0: D FE Mesh

=


The numb er of iterations � O (n

Domain Decomp osition


)


"Divide and conquer" the spatial domain.

Multigrid

"Divide and conquer" the frequency domain.

numb er of iterations � O ()

Preconditional Conjugate Gradient (PCG)

�

The mathematical idea is to premultiply b oth sides of the equation by the matrix M � A


.


Thus, M Au = M f . Note that we don't explicitly compute M Au = M f in practice. We just

want a preconditioner for which solving M z = y is cheap in comparison to its e�ectiveness.

One can cho ose from a variety of di�erent preconditioners which vary greatly in their

cost and overall e�ectiveness. Note that by e�ectiveness we refer to how fast the iterative

metho d converges to a solution. Examples of preconditioners include :

� Matrix splitting, in which we use the inverse of a diagonal matrix D. This metho d is

cheap but ine�ective.


-----

�


� Direct metho d, in which we directly calculate M = A

e�ective, but also very exp ensive.


in  iteration. This is extremely


� Incomplete factorization, in which we take A � LU . This metho d is not all that cheap

but is fairly e�ective.

� Domain decomp osition, in which we use a blo ck diagonal matrix instead of a diagonal

matrix as in the case of matrix splitting. This has cost and e�ectiveness similar to that

of incomplete factorization.

� Multigrid. This metho d is rather exp ensive, but it is very e�ective. We will use this

metho d in the algorithm discussed b elow.

. Multigrid

Simple iterative metho ds are go o d for large problems and reduce \high frequency" error, i.e.,

they smo oth the residual. Hence, we will use cheap iterative metho ds at multiple scales of

resolution so that the iterative metho ds are used in cases for which they work b est. The basic

idea is that we want to generate coarser meshes from an initial �ne mesh by reducing the

numb er of vertices in a �ner mesh and then remeshing. We then solve the problems on the

coarser mesh and interp olate back to the �ner mesh. Figure  shows a simple progression

of coarser meshes.


###### 2

 2

 2

 2

 2


###### 2


###### 1


###### 1


###### 2


###### 2


###### 2

 2

 2

 2

 2


###### 1

|2|Col2|2|Col4|2|Col6|2|2|
|---|---|---|---|---|---|---|---|
|||||||||
|2||2||2||2||
|||||||||
|2||2||2||2||
|||||||||
|2||2||2||2||
|||||||||
|2||2||2||2||

|11|Col2|11|Col4|11|Col6|Col7|
|---|---|---|---|---|---|---|
|||||1 1|||
|1||1|||||
||||||||
|1||1|||||


###### (3) (2) (1) P  : 9 by 9 grid of points P  : 5 by 5 grid of points P  : 3 by 3 grid of points  7 by 7 grid of unknowns  3 by 3 grid of unknowns  1 by 1 grid of unknowns
 Points labeled 2 are Points labeled 1 are part of next coarser grid part of next coarser grid

Figure : Classic Multigrid Sequence of Grids

. Unstructured Multigrid Algorithms

We apply the following algorithm recursively :

� Evenly coarsen vertex set ! smaller vertex set

� Mesh this vertex set


� Create interp olation op erators Ri


and matrices Ai


, for coarse grids


-----

We coarsen a set of mesh no des by �nding the maximal indep endent set of these no des and

using this as the set of no des for the new coarse set. This new set is meshed using Delaunay

tessellation. We use the �nite element shap e functions (the �'s) to generate interp olation

T


op erators (Ri


), and we calculate the coarse grid matrices using Ai+


= Ri


Ai


R

i


. Figures 


and  show examples of the grid coarsening pro cess.

Figure : Sample Input Grid

. Parallel Multigrid Solver for FE

Mark Adams has implemented a parallel version of the algorithm discussed ab ove by mak
ing use of and developing a variety of software comp onents. The system uses MPI for the

message passing implementation, and a package called ParMetis to partition a mesh into


sections which can then b e assigned to separate pro cessors. The Ri


and Ai


are determined


by Adam's MGFeap program. The matrix A0 is generated using a serial FE co de called

FEAP. A program called PETSc handles the parallel preconditional conjugate gradient cal
culations and the multigrid infrastructure and provides numerical primitives with a multigrid

preconditioner.


-----

Figure : Sample Coarse Grids

 Distance Metrics for Voronoi Diagrams and Delau
nay Triangulations

We are not restricted to using only Euclidean distances when computing a Voronoi diagram

or its dual, the Delaunay triangulation. Other p ossible distance metrics include :

� distances measured on spheres or conics

� Manhattan distance in which only the paths along co ordinate axis directions are con

sidered, i.e., d = �x


+ �x


� Supremum distance for which d = max(�x; �x


)


� Karlsruhe distance which is a sort of p olar distance for which

(


� r

+ r


j + j�


� �


j if j�


� �





j < � =


d =


jr

jr


j other w ise


� weighted distance for which d(p; pi

seeds


) = =wi


jx � xi j


j for all p oints p where pi


are the


� shortest path on a graph, for example the shortest path b etween two p oints on a city

map if the path must stay on streets


-----

 Surface Mo deling Using Triangulation

We will examine the use of triangulations in mo deling and interp olating surfaces, particularly

with resp ect to terrain mo deling. In the �rst case, we wish to reduce the time and space

required to represent and manipulate surfaces. For the second, we want to �nd interp olating

surfaces b etween data p oints. Techniques to achieve these goals can b e applied to problems

in �elds such as terrain mo deling, computer graphics, medical imaging in which surface

mo dels are built by pro cessing consecutive D slices of a volume of interest, and geophysical

mo deling used, for example, in oil exploration.

. Terrain Mo deling

Terrain mo deling has b een used for decades in military vehicle simulators and map displays

in order to accurately represent landscap e features. The dirt moving application discussed

in an earlier lecture also makes use of terrain mo deling.

.. Metho ds for Representing Terrains

We could use a variety of di�erent approaches to mo del terrains. For example, we could

describ e a terrain as a collection of line segments approximating the curves of a contour

plot. However, it would b e di�cult to convert such a representation from one measurement

system to another, e.g., from feet to meters. In addition, it is unclear how one would

determine elevation values for p oints near but not on contours. Another option is to use a

height �eld to store elevation data, but this representation is discontinuous and uses large

amounts of space to store regions with constant elevations which could b e compressed.

We could also view terrain mo deling as a lossy compression problem. From this p oint of

view we need to select an appropriate set of basis functions for the compression. If we use

triangles as the bases, then we can use large triangles in terrain areas in which the slop e is

not changing much and smaller ones only in areas of changing slop e. Thus, we compress the

regions of constant slop e. In particular, the second derivative of the terrain surface gives a

measure of lo cal feature size, so we want to have a greater density of triangles in regions with

large second derivative values. This is, in fact, the representation used in terrain mo deling.

It is interesting to note that the use of TINS, or triangulated irregular networks, in terrain

mo deling dates from the  0s, b efore e�cient Delaunay algorithms were known.

.. Bene�ts of Triangulation

Using a triangulation to represent a terrain provides a numb er of imp ortant b ene�ts. For

example, as discussed ab ove, such a representation do es not require much space, since large

triangles can b e used to represent areas of constant elevation, and we only need dense

concentrations of triangles in areas where the slop e changes rapidly. In addition, most

mo dern graphics systems are optimized for rendering triangles, so rendering the terrain is

quite e�cient. It is also straight forward to �nd the slop e of a triangle, so �nding the slop e

at a particular p oint in the terrain is easy. Furthermore, constant height lines in the terrain


-----

are straight lines on the approximating triangles, so reconstructing contour lines is fairly

easy.

.. Algorithm

Our basic problem is to generate a triangulation based on a given mesh of height values.

Once the triangulation has b een calculated, we can �nd a height value for any p oint (x; y )

by interp olating b etween the heights of the corners of the triangle containing (x; y ). We can

calculate an error metric for our triangulation by �nding the di�erence b etween the height

value in the original mesh for p oint (x; y ) and the interp olated value from the triangulation.


Thus, if It (x; y ) = interp olated value at (x; y ) based on corners of triangle containing the


p oint, z (x; y ) = value at x; y in the original mesh, and error at x; y = e(x; y ), then e(x; y ) =


jz (x; y ) � It(x; y )j. We make use of this error metric in the following algorithm due to Garland


and Heckb ert to calculate a triangulation.

function Surface Mo del(M ; �)

// M is the input mesh of altitudes

// � is the b ound on the maximum error

// The Output P is a subset of the original mesh p oints and its triangulation T

P = the  corners of M

T = DelaunayTriangulation(P )

rep eat while (max(fe(x; y ) : (x; y )  M g)    - �)

select p oint p with maximum error

P = P [ fpg

T = DelaunayTriangulation (P )

return P and T

end

.. Finding max(e(x; y ))

We use a priority queue to �nd the max error at each step. The queue contains one entry

p er triangle, and the entries are ordered on the maximum error for each triangle. For each

new triangle, we calculate its maximum error and insert it into the queue. Note that for

each iteration i, there are  + i p oints and i triangles.

.. Running Time

Assume there are n p oints in the original mesh and m p oints in the �nal solution (m � n).

We can use the incremental metho d to add a new p oint to the Delaunay triangulation on

th


each step (we need not start from scratch). Then the times for the i


iteration are


\exp ected" worst case

�nd maximum error : O (log (i)) O (log (i))

mo dify Delaunay triangulation : O () O (i)

�nd errors for each p oint in new triangles : O (n=i) O (n)


-----

and the total times are

Total (exp ected) :

Total (worst case) :


m

X

i=


log (i) + n=i = O ((n + m) log (m))

m

X

log (i) + n = O (nm)

i=


Note that for the \exp ected time" for �nding the errors for each p oint in new triangles

all of the triangles are assumed to b e approximately the same size, so for n p oints and i

triangles, each triangle will cover n=i of the p oints.


-----

Algorithms in the Real World Notes by Ta jh Taylor

Lecture # (N-Bo dy Simulations ) �c   Ta jh Taylor and Guy Blello ch

� Delaunay Triangulation  - more applications

� N-Bo dy Problems

. Intro duction

{ Basic Assumptions

{ Applications

{ History of Algorithms

. Mesh-based Algorithms

{ Particle mesh (using FFT)

. Tree-based Algorithms

{ Barnes-Hut Algorithm

{ Fast Multip ole Metho d

 Delaunay Triangulation - more applications

� Studying structure of galaxies

use Euclidean minimum spanning tree to study clustering characteristics

� Prediction of protein folding

run statistics on triangulated protein structures

� Studies of structural damage in metals

e.g. study growth of \voids"

� Animal and plant ecology

� Human space patterns

\central space" theory


-----

 N-Bo dy Intro duction

Particles in motion

The goal of N-Bo dy problems is to determine the motion over time of b o dies (particles) due

to forces from other b o dies. Typical calculated forces include electrostatic force and gravity.

The basic metho d used for solving the problem is to lo op forever, stepping discretely through

time and doing the following at each timestep:


� Up date p ositions using velo cities (~xi+

~


= ~xi


+ �t~vi


)


� Calculate forces


F


� Up date velo cities (~vi+


= ~vi


+




m


~

�tFi


)


Our fo cus will b e on metho ds for calculating the forces. Note that it is p ossible to use

multiple resolutions for time, i.e. di�erent �t for di�erent particles, but we will only consider

uniform �t.

. Basic Assumptions

We will consider the particles to b e in three-dimensional space, and we will use the following

de�nitions:




Potential �(~x) /

~






r


Coulomb Force


~x) / (for  b o dy)

r

~

F = m r�(~x) /


In general the p otential �(~x) is a continuous function over space, and if it is known

everywhere, we can calculate forces on all the b o dies by taking the gradient.


-----

Figure : An area over which the p otential �(~x) is de�ned. The balls represent di�erent

sized particles.

. Applications

Astronomy : Formation of galaxies

� Questions:

Is the universe expanding?

How much \dark matter" is out there?

� Forces are gravitational

� State of the art simulations:




� 0




b o dies running for 0


steps.


 week on 00 pro cessors ( ).

Biology/Chemistry: Molecular Dynamics

� Electrostatic + other forces

(Bond forces, Lennard-Jones p otential)

� State of the art (protein folding):




0


b o dies for 0





timesteps


� Note that it is easier to use a cuto� radius for limiting electrostatic calculations, b ecause

distant charges cancel each other out.

Others

� Plasma Physics


-----

###### mesh

 particle

Figure : Mesh-based N-b o dy metho ds

� Partial Di�erential Equations

� Fluid Dynamics { \vortex particles"

. History of Algorithms

.. Particle-Particle (the naive metho d)


###### cell


This metho d simply calculates the force b etween all pairs of particles.




� The time required to calculate all interactions is O (n




).


� This is ine�cient for systems with 0

.. Mesh Based Metho ds


+ b o dies.


Particle Mesh (PM): Breaks space into a uniform mesh and places each particle in the

appropriate cell of the mesh. Uses a discrete Fourier transform (DFT) to solve a partial

di�erential equation (PDE) over the mesh.

� Invented in the  0s.

� For m cells, O (m log m) time is required.

Particle-Particle Particle-Mesh (PM): A combination of direct particle-particle in
teractions for close particles and the particle-mesh metho d for distant particles.

� Invented in the early  0s.

� Provides b etter accuracy for the same time as PM.


-----

(a) A quadtree in a Top-down method


(b) Nearest neighbor groupings in a bottom
up method


Figure : Tree-based N-b o dy metho ds

Nested-Grid Particle-Mesh (NGPM): Uses a nested mesh with di�erent \resolutions".

� Invented around  .

� Is related to multigrid metho ds.

.. Tree Based Metho ds

Top-down particle-cell: Divides space into a quadtree ( dimensional) or o ctree ( di
mensional). When a cell (inner no de of the quad or o cttree) is far enough away from a

particle we can calculate the force to the center of mass of the cell instead of having to

calculate the force to each particle in the cell. For example, in Figure  (a) the particle

in the upp er left could group the two particles in the lower right together and calculate the

force to their center-of-mass.

� App el ( ) pro duced the �rst tree-based solution.

� Barnes-Hut re�ned it in  .

� For n particles, O (n log n) time is required (under certain assumptions).

Bottom-up particle-cell: Similar to the top-down metho d but the tree is created b ottom
up by grouping neighb oring particles or cells (see Figure  (b)).

� Press pro duced an algorithm in  .

� O (n log n) time is required (under certain assumptions).


-----

###### ρ (x,y) y

 x

Figure : Visualization of the mass density function.

Cell-cell (Fast multip ole metho d, FMM): Also uses a tree but allows for \cell-cell

interactions" as well as \particle-cell interactions".

� Incorp orates four main ideas: multip ole expansions, error b ounds on dropping terms,

dual expansion, and translation of expansions.

� These are the fastest known metho ds for solving N-Bo dy problems.

� Done by Greengard in  .

� O (n) time is required for uniform distributions. Non-uniform distributions may in
crease the required time.

Tree-co de particle-mesh: Mixes ideas from particle-mesh metho ds and tree-based meth
o ds.

� Work by Xi in   .

 Mesh-based Algorithms

The goal is to solve the following PDE (Poisson's equation)




r


�(~x) = � G�(~x)


where �(~x) is the \mass density" (Figure  shows an example). The solution to this equation

gives the p otential over space, which can then b e used to calculate the force on each particle.

The Poisson equation is the same as used for heat �ow, or �uid �ow without compression or

viscosity. Poisson's equation can b e solved by various metho ds, including sp ectral metho ds

(DFT), �nite element, or �nite volume metho ds. Here we will discuss using sp ectral metho ds

and the FFT, an approach that has b een used extensively in astronomical n-b o dy problem.

Particle mesh (using FFT)

We are given the density function �(~x) and want to solve for the p otential �(~x) in the




equation r


�(~x) = � G�(~x). We �rst discretize space by breaking it into a uniform mesh.


Solving for the p otential on this mesh will give us an approximate answer to the continuous


-----

solution and as long as the mesh is \�ne enough" the approximation will b e reasonably go o d.

We will discuss how �ne it has to b e later.

For simplicity let's start by assuming -dimensional space, and let's consider the Discrete

Fourier transform of the density function �(x) (assuming x go es from 0 to n �  in discrete

steps of ). The DFT is

n�

X

� ixj =n


�j


=


�(x)e


x=0

which transforms our density function into a set of frequency comp onents (i is the imaginary

p


numb er


�). Since Poisson's equation is linear we can solve for each frequency comp onent

th


separately. Lets use the notation wj

iwj x

the density function: fj (x) = �j e

get


= � j =n and consider the j


frequency comp onent of


. If we plug this comp onent into Poisson's equation, we


x




r �


(x) = � G�j




iwj

e






wj


j


The solution to this equation is


iwj

e


x


 iwj

since r e


x




= �wj


�j (x) = �� G�j  e = �� G  fj (x)

wj wj

iwj x

e . In other words, to solve for the jth


frequency comp onent of


the p otential � we simply multiply the jth




frequency comp onent of the density function by


�� G


.


wj


We can similarly solve for each of the other frequency comp onents of the p otential,

then add up the solutions to get the solution to our initial problem. This is equivalent to




convolving the frequency comp onent j with =w


and then transforming back to co ordinate


j

space, which can b e done with a second DFT. This idea can b e applied in multiple dimensions

by taking a multidimensional DFT. In this case the solution for a particular comp onent with


frequencies wj


; wk


and wl


would b e




+ w

l


�j k l (~x) = �� G


fj k l (~x)




wj






+ w

k


where j; k and l are the frequency comp onents in the x, y and z dimensions resp ectively.

So the overall algorithm in three dimensions has �ve steps:

� Break space into discrete uniform mesh of p oints.

� Assign each particle to a p oint (or set of p oints) to generate � for each p oint.

� Do a -D FFT on the mesh.

� Convolve the results with the sum of inverse square frequencies.

� Do an inverse FFT back to the original mesh p oints.


-----

This will give �(~x) over the mesh from which we can derive the forces. For m mesh p oints

the algorithm will take O (m log m) time.

The problems with this metho d is that in order to get reasonable accuracy there should

b e no more than one particle p er cell, and ideally there should b e a few cells separating

each particle. This works �ne if the particles are uniformly distributed, but if the particles

are nonuniformly distributed the simulation would require a numb er of cells that is very

much larger than the numb er of particle. This is b ecause the mesh has to �ne enough to

accommo date the smallest distance b etween particles. For su�ciently nonuniform p oints the




numb er of mesh p oints required could b ecome greater than n

than the naive all-pair interactions.

 Tree-based Algorithms


and therefore run even slower


The approach taken by tree based metho ds is to approximate far away particles by some




sort of center of mass rather than by direct interactions.


The further away you are from


a set of p oints, the more you can group together and consider as a center-of-mass. These

\centers of mass" are then organized hierarchically (in a tree) so that the approaches can

determine which sets of p oints to approximate by their centers of mass. The ro ot of the tree

will include all the particles, and at each no de of the tree the children will partition the set of

particles of that no de, usually by partitioning the space taken by that no de. The closer you

are to the p oints, the further down in the tree you will need to go so that you will consider

smaller sets of particles.

We will call a set of particles group ed together with a center of mass, a cel l. In the

algorithms we will consider three typ es of interactions, particle-particle (direct interactions

b etween two particles, particle-cell (interaction b etween a particle and the center of mass of a

cell), and cell-cell (interactions b etween two centers-of-mass). These are shown in Figure .

In this class we will only consider top-down tree-based algorithms.

. Barnes-Hut Algorithm

The �rst tree-based algorithm we consider is the Barnes-Hut algorithm, which use particle
particle and particle-cell interactions, but no cell-cell interactions. It consists of building a

tree using an o ct-tree in  dimensions or a quad-tree in  dimensions, and then using the

tree to calculate the force on each particle. Each division evenly splits up the space so, for

example, in a quadtree each step will consists of dividing a square into  squares. Note

that this will not necessarily evenly divide the particles, so the tree in general will not b e

balanced. The algorithm for building the tree works top down and is de�ned by the following

co de



Center of mass is used informally here since later we will show that some of the algorithms approximate

a set of particles by more complicated functions.


-----

###### particle particle

 particle

 cell

 cell cell

Figure : Particle-particle, particle-cell, and cell-cell interactions.

function Build Tree(P )

// P is a set of p oints along with a b ounding b ox

if Particle Count(P ) � � // where � is an integer threshold (� � )

return P

else


(P


; P





; : : :) = partition(P ) // the quadtree or o ctree division

(divides space evenly)


; P


a = Make Empty Tree()


for �  (P


; P


; P


; : : :)


a = Add Child(a; build tree(� ))

return a

Figure  gives an example of a set of p oints in -dimensions along with the tree built

by this co de. Once the tree has b een built the force algorithm is quite simple and is given

in Figure 0. The well separated function tells when to approximate the force for a group

of particles using the center of mass for the group (see Figure ). � is a user-sp eci�ed

parameter that controls the accuracy of the results. A smaller � will increase accuracy but

also increase runtime, and larger � will decrease accuracy and runtime.

For \reasonable" distributions each particle interacts with a constant numb er of cells on

each level of the tree, and there are O (log n) levels. Therefore each particle takes O (log n)

time and the total time for the Barnes-Hut algorithm is O (n log n). One can show, for

example, that for uniform distributions in -d:


-----

###### 11
 1 h/2

 12

 1

 2 3 8 12

 4 5 6 7 9

 10 11

Figure  : An example of a quadtree partition of space and the corresp onding tree used in

the Barnes Hut algorithm (assumes � = ).

|2|Col2|Col3|Col4|Col5|Col6|Col7|
|---|---|---|---|---|---|---|
|||||6|7||
||3||5|8|||
|||4|||||
|1||||9|||
||||||10||
|||||||11|
|||||12|||

|h/2|h|
|---|---|
|||


-----

function Barnes Hut(P )

T = Build Tree(P )

r = ro ot of T

for p  P

~


Fp


= Calculate Force(p; r )


function Calculate Force(p; c)

// p is a particle

// c is a no de of the tree, which is either a particle or cell

if Is Particle(c)

if p = c return 0 // don't include the p oint itself

else return Force(p; c) // particle-particle force calculation

if Well Separated(p; c)

return Force(p, Centermass(c)) // particle-cell force calculation

~

F = 0

0


for c

~


 children of c


0


F += Calculate Force(p; c )

~


return


F


function Well Separated(p; c)

return s(c) < � � d(p; Center(c))

Figure 0: Co de for the Barnes-Hut algorithm. Assumes the leaves of the tree are individual

particles, i.e., � = 

###### s(c)

 center

 d

 p

Figure : Well Separated calculation on a cell c and particle p.


-----

Total Interactions: I (n; � ) �


�



�


n log


(n)





For � = :, which is typically required for go o d accuracy, this gives � 0n lg n. Using a

very rough calculation (we are dropping some lower order terms) this outp erforms calculating




all pairs interactions when 0n lg n � n


=, which is when n - 0000. At � = :, which is


the ab out the highest used, the tradeo� is at around 000 particles. Barnes-Hut is therefore

not useful for a small numb er of particles. It, however, can do much b etter than the all-pairs

algorithm for larger n.

Exercise: For a million particles and � = : ab out how much faster is Barnes-Hut over

using all pairs?

The Barnes-Hut algorithm is highly parallelizable since the lo op over the particles once

the tree is built is completely parallel, and it is not to o hard to build the tree in parallel.

There have b een many parallel implementations of the Barnes-Hut algorithm.

. Fast Multip ole Metho d

This metho d was pioneered by Greengard and Rokhlyn in  , and it won an ACM Thesis

Award for Greengard. It was the �rst linear-time algorithm for N-Bo dy problems (for uniform

or near uniform p oints). They were also the �rst to have proven error b ounds.

The metho d has four main ideas in it, each of which will b e covered in more detail:

� Multip ole expansions

� Error b ounds on dropping terms

� Dual lo cal expansion

� Translation of expansions

For nonuniform p oints, FMM can take O (n log n) time to �nd a set of \well-separated"

p oints, but the force calculation is still O (n).

Idea : Multip ole expansions

For any cluster of particles, their net force can b e approximated using a multip ole expansion

(see Figure ) which is taken around a �xed p oint. The �rst term of the expansion is often

called the monop ole term, the next group of  terms are called the dip ole terms, and the

next group of  indep endent terms are called the quadrap ole terms.

The multip ole expansion is analogous to a Taylor-series expansion, but in d. Like the

Taylor-series expansion the earlier terms have a larger magnitude when far enough from the

origin, and the function can b e approximated by dropping higher order terms. In the case of

multip ole-expansions the force and p otential due to higher-order terms drops o� faster as a

function of r (see the last two rows Figure ), which is what allows us to drop these terms

far from the center.


-----

p    

Terms    






r





r






r





r






r





r


Potential

Force

Idea : Error Bounds




r





r


Figure : Multip ole expansion.


For distributions with only p ositive sources (e.g., gravitation) we can b ound the ratio of the

force due to higher terms of the p otential relative to the �rst term, and therefore b ound the

error due to dropping terms after a given p. This is p ossible at a su�cient distance from

the particles since the higher terms diminish faster than the �rst term (see the third row in

Figure ). To see this consider the following diagram:

### ?

###### cr

 r

### ?

###### outside


###### q i


### ?


P


Lets de�ne M =


qi


as the sum of the masses inside the sphere de�ned by r . A lower


b ound on the force due to the monop ole of these masses (�rst term of the expansion) on a


mass m


on the outer sphere is


)


F


�


m M



(((c + )r )


-----

# ?
## ?

(a) multip ole expansion approximation (b) lo cal expansion approximation

Figure : Multip ole (outer) and lo cal (inner) expansions.


Similarly an upp er b ound on the force due to the other multip ole terms on m

p�


r


m


M

p+


Fp


�


:


((c � )r )

th

With these b ounds we can then b ound the ratio of the contribution of the p

�rst term by




is

term to the


Ep


=


Fp

F


�


(c + )

p+

(c � )


Assuming c is greater than , this b ound decreases exp onentially with p and allows us to

b ound the numb er of terms p we need for a given accuracy (we can actually get tighter

b ounds if we are more careful). It also shows how having larger c gives b etter error b ounds.

As we go outside the outer sphere our approximation can only get b etter.

Idea : Dual Expansion

Our previous multip ole expansion assumed we know the sources inside an inner sphere and

are trying to approximate the p otential (or forces) due to them outside an outer sphere (see

Figure (a)). There is also a dual expansion in which the sources are known outside the

outer sphere and we want an approximation the p otential contribution due to them inside

the inner sphere (see Figure (b)). These dual expansions turn out to b e very imp ortant in

the Fast Multip ole Metho d. We will refer to them as the local or inner expansion. We will

refer to our original expansion as the multipole or outer expansion.

Idea : Translation of Expansions

The �nal idea is that the expansions can b e translated from one center to another. Further
more we can translate b etween the two di�erent kinds of expansions. This is illustrated in


-----

###### Outer-Outer

 Outer-Inner

 Inner-Inner

Figure : Example translations

Figure . In this �gure we are trying to approximate the forces due to the particles in the

left b ox on the particles in the right b ox. We �rst combine the outer (multip ole) expansions

on the left in a tree like fashion by translating each expansion to its parent in the tree and

summing the children into the parent. We then translate the total outer expansion to an

inner (lo cal) expansion in the right b ox. Finally we translate this inner expansion down the

tree to each of the lo cations on the right. The running time for each translation is dep endent




on the numb er of terms. With a naive implementation each translation can run in O (p


)




time but this can b e reduced to O (p




log p


) with a FFT-style translation.


The translation of the outer expansion to an inner expansion in another b ox is called a

cell-cell interaction. This is b ecause we are e�ectively having the cells interact rather than

having particles interact directly (note that in the example of Figure  no particle on the

right interacts directly with a particle on the left).

Why cell-cell interactions?

To motivate why cell-cell interactions and b oth forms of expansions are imp ortant consider

Figure . In the example the goal is to determine the p otential (or force) on each particle

due to all other particles outside of its own cell. To do this we will use expansions for

each cell. We �rst consider the cost (numb er of interactions) when using just particle-cell

interactions and then show that we can do much b etter by using cell-cell interactions.

Particle-Cell Cost


p

n to calculate multip ole expansions within each cell each cell


�


p

n �


p

n cells.


� n �


p

n for particle-cell interactions (each particle has to lo ok at the other


-----

Figure : Example cell-cell interactions. Assume there are n total particles with


p

n parti

cles within each cell (circle) and that the cells are well separated from each other.

=


� Total = O (n

Cell-Cell Cost


)


p

n to calculate multip ole expansions within each cell

p

n for outer-inner (multip ole-lo cal) translations | every cell translates to every


�

�

�


p

n �

p

n �


p

n �

of its


other cell and we add up the contribution at each cell


p

n to translate the lo cal expansion from the center-of-mass of each cell to each

p

n elements.


� Total = O (n)

FMM: Using a tree

We now consider putting the ideas together into the Fast Multiple Algorithm. There are

three phases, each which uses a tree.

� Bottom up: forming multip ole expansions

{ outer-outer translation from children to parents

� Top down: forming lo cal expansions

{ inner-inner translation from parent to child

{ outer-inner translation from interaction list


-----

� Direct interactions with neighb ors at leafs

For a parameter k and for cells on the same level (i.e. of the same resolution), we make

the following de�nitions.

De�nition: two cells are near neighbors of each other if they are within k cells of each

other. Note that two cells with touching corners are considered to have a distance of one.

De�nition: two cells are wel l separated if they are not near neighb ors.


De�nition: a cell c

. well-separated(c


is in c 's interaction list if

; c ) and


. near-neighb or(p(c


); p(c


))


where p(c) indicates the parent of c.

In practice k = , and in -dimensional space the size of the interaction lists is then .

d


In general it is not hard to show that the size of an interaction list is (

Total Time (for a uniform distribution)


� )(k + ).




Assume k = . Place p




particles p er leaf cell (n=p




leaf cells).


Assuming translations take p


time:


!


n



p

l+






Leaf multip oles p

d

X

Up Tree

l=

d

X




p


l

+ 




p


)


Down Tree


l

( � 

!

n



p






p


l=



Lo cal expansion p


Total Time = O (np

�p

Error Bound � :


)


There is a clear tradeo� b etween time and accuracy.

Figure  shows a comparison of runtimes for the various algorithms for two di�erent

accuracies. The BH (rect.) is a variant of Barnes-Hut that uses multip ole expansions in

rectilinear co ordinates. The BH (spher.) is a a variant of Barnes-Hut that uses multip ole

expansions in spherical co ordinates. The PMTA is an algorithms that combines the ideas

of Barnes-Hut and FMM. Comparisons are given for sets of particles that all have the same

charge (chargeless) and for particles which have b oth p ositive and negative charges (charged).


-----

###### 1.4e+13 1.2e+13 1.0e+13 8.0e+12 6.0e+12 4.0e+12 2.0e+12
 0


###### BH BH PMTA FMM (rect.) (spher.)

 Grav. Elec. (chargeless) (charged)


###### 2.4e+12 2.0e+12 1.6e+12 1.2e+12 8.0e+11 4.0e+11
 0


###### BH BH PMTA FMM (rect.) (spher.)

 Grav. Elec. (chargeless) (charged)


(a) high accuracy execution times (b) low accuracy execution times

Figure : Runtimes for the various algorithms.


-----

Algorithms in the Real World Notes by Steve Gribble

Lecture # (N-b o dy Simulations ) �c   Steve Gribble and Guy Blello ch

� N-b o dy continued: Callahan & Kosara ju Algorithm

� Fast Multip ole Metho d (Review)

. The Four Ideas

. Interaction Lists

� Callahan and Kosara ju's Algorithm

. Well Separated Pair Decomp ositions

. De�nitions

. Algorithm: Tree Decomp osition

. Algorithm: Well-Separated Realization

. Bounding the size of the realization

� N-b o dy Summary

 Fast Multip ole Metho d (Review)

. The Four Ideas

The four main ideas b eing the fast multip ole metho d (FMM) were:

� Multip ole expansion  - a Taylor-series like expansion of the p otential due to a cluster

of particles around an origin. The expansion converges at p oints outside the cluster so

that the p otential can b e approximated by only keeping the �rst p terms. We call this

the outer or multip ole expansion.

� Error b ounds on dropping terms  - the numb er of terms in the expansion dictates

the accuracy of the expansion

� Dual lo cal expansion  - an expansion of the p otential due to particles outside a

cluster which converges for p oints inside the cluster. We call this the inner or lo cal

expansion.

� Translation of expansions  - b eing able to translate a inner or outer expansion to a

new origin, or translate an outer to an inner expansion at a di�erent origin.

A �fth idea (Figure ) is to use a tree-structure to organize the particles and to deter
mine a strategy for grouping the particles and p erforming the outer/outer, outer/inner, and

inner/inner translations. We call each no de of the tree a cel l.


-----

###### outer/inner inner/inner outer/outer

 (outer/inner used on interaction list)

Figure : Fifth idea          - using a tree for translations

. Interaction Lists

In the fast multip ole metho d, the interaction list (Figure ) dictates the particles that a

given cell will interact with (cross edges in Figure ). The interaction list for a cell c consists

of all the cells at the same level of the tree which () are well-separated from c and () are

children of cells that are not well-separated from the parent of c. In Figure , for example,

we assume a cell is well separated if it is  cells away. Clearly all the outer shaded cells are

 away from the center cell c and are therefore well-separated. Also the parents of these

cells are not well-separated from the parent of c (note that parent cells are marked with the

thicker lines). One issue is how to �nd particles in the interaction list. Here are two p ossible

metho ds:

. Uniform distributions: a hierarchy of meshes can b e used in this situation. Simply

lo ok at neighb ors at an appropriate resolution in the mesh hierarchy.

. Non-uniform distributions: a mesh hierarchy may b e very sparsely p opulated, so

a Barnes-Hut tree-like structure may b e more appropriate in this case.

###### ������������
 �
 ������ �� � ���� Interaction List
 �
 � � ��
 � �� ������

Figure : The Interaction List

|Col1|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Col10|� Interactio|
|---|---|---|---|---|---|---|---|---|---|---|
|||��|��|��|��|��|��||||
|||�|�|�|�|�|�||||
|||��||�||��|��||||
|||�||� �||�|�||||
|||�||||�|�||||
|||�|�|�|�|�|�||||
||||||||||||
||||||||||||
||||||||||||


-----

 Callahan and Kosara ju's Algorithm

We now discuss an algorithm due to Callahan and Kosara ju for generating a tree and

interactions-lists for non-uniform distributions (\A Decomp osition of Multi-Dimensional

Point-Sets with Applications to k -Nearest-Neighb ors and n-Bo dy Potential Fields.", JACM,

(), January  ). The algorithm has the nice prop erty that it is very simple, although

the pro of of its b ounds is a little involved. The particular tree-structure it creates is called a

well-separated pair decomp osition. It uses a somewhat more general de�nition of interaction

lists than used in the previous section (for example, it allows interactions b etween cells on

di�erent levels). The algorithm works in any dimension, requires at most O (n log n) time to

build the tree for n particles and guarantees that there will b e a total of O (n) interactions

(size of the interaction lists summed over all cells).

. Well Separated Pair Decomp ositions

The tree structure used by the algorithm is based on the notion of a tree decomp osition

of p oints. Given the set of p oints fa, b, c, d, e, f, gg, a tree decomposition of these p oints

rep eatedly splits this set into subsets, as in Figure .

###### {a, b, c, d, e, f, g}

 {a, b, c, d}
 {e, f, g}


###### {e,f} {a, b, c}
 d

 {b, c}
 a e f

 b c

Figure : A tree decomp osition D of p oints.


###### g


A wel l-separated realization of a tree decomp osition is a set of interaction edges b etween

vertices (cells) in the tree (edges represent outer/inner translations) such that () the cells

at the two ends of the edge are well-separated (we will de�ne well-separated later in these

notes) and () there is exactly one path b etween any two leaves that go es up the tree any

numb er of levels (including 0), across a single interaction-edge, and back down the tree any

numb er of levels. The second prop erty guarantees that each particle will interact exactly

once with every other particle. Figure 00 shows an example of a well-separated realization

for the tree decomp osition given in Figure . You can verify that there is exactly one path

b etween every leaf. We will de�ne well-separated realizations more formally in Section ..

Together the tree-decomp osition and the well-separated realization on that tree are called

a wel l separated pair decomposition. The Callahan-Kosara ju algorithm consists of generating


-----

###### A single path up, across, and down between
 g any two leaves.


###### a e f

 b c

Figure 00: A well-separated \realization" of D .

the tree and the realization in two steps. We will see that we can build the tree-decomp osition

in O (n log n) time and �nd the well-separated realization given the tree in O (n) time. Fur
thermore we can b ound the size of the well-separated realization (total numb er of interaction

edges) by O (n).

The well-separated pair decomp osition has applications b oth to the N-b o dy problem

and to computational geometry. For the N-b o dy problem the tree is used for outer/outer

translations (going up the tree) and inner/inner translations (going down the tree), and the

well-separated realization is used for outer/inner translations. In computational geometry

the well-separated pair decomp osition can b e used to �nd the k -nearest-neighb ors for each

p oint. This requires some augmentation to the tree and is discussed in the Callahan and

Kosara ju pap er.

For the N-b o dy problem the time taken by one step of building the tree, �nding the


interaction edges, and doing all the translations to calculate the forces is k


n log n + k


n,


where the �rst term is for building the tree and the second linear term is for �nding the


interaction edges and translating the expansions. In practice the constant k


is very much


larger than k


. Furthermore in many cases it is p ossible to use the same tree (or only slightly


mo di�ed tree) for multiple steps. Therefore from a practical standp oint the algorithm runs

in almost linear time.

. De�nitions

� Bounding Rectangle R(P ): the smallest rectangle that contains p oints P and is

aligned with the axes (Figure 0).


� lmax


: maximum length over the dimensions of a rectangle. lmax


(P ) is the maximum


length of R(P ).

� Well-separated: Given two rectangles, let r b e the smallest radius that contains

them b oth (see Figure 0). For a given separation constant s two rectangles are well

separated if d  - sr .


-----

Figure 0: Bounding Rectangle

###### r

 r
 d

Figure 0: Well Separated

� Interaction Pro duct A � B :


0

A � B = ffp; p


0

gjp  A; p


0

 B ; p = p


g


� Realization of A � B is a set ffA ; B


g; : : : fAk ; Bk


gg such that:


. Ai

. Ai

. (A


� A; Bi


= ;

i ) \ (Aj

k


� B for all i =  : : : k


\ Bi

i � B


. (Ai � Bi ) \ (Aj � Bj ) = ; for all i = j, i.e., there are no rep eated interactions

k

. A � B = [i= Ai � Bi, i.e., all interactions are included.

This formalizes the interaction edges in the tree and guarantees that there is only one

path b etween two leaves. In particular rule  guarantees that no leaf interacts with

itself, rule  guarantees that no leaf interacts more than once with another leaf and

rule  guarantees that every leaf interacts with every other leaf.


. A � B = [


A


� A well separated realization is a realization such that for all i, Ai

separated.


and Bi


are well


� A well-separated pair decomp osition is a tree decomp osition plus a well-separated

realization P � P where subsets are no des of the tree (Figure 0).

. Algorithm: Tree Decomp osition

The algorithm partitions space by recursively cutting b ounding rectangles in half along their

longest dimension. It can b e de�ned as follows:


-----

###### T


###### g


###### a e f

 b c

Figure 0: Subsets are no des of the tree

function Build Tree(P )

// P is a set of p oints

if jP j =  then return Leaf(P )

else

S = plane that splits R(P ) p erp endicular to its longest dimension


P


= Split P by the plane S





; P


return Tree No de(Build Tree(P


), Build Tree(P


), R(P ))


end

An example of the algorithm on a set of  p oints is given in (Figure 0). The algorithm

###### splits of physical space in half

Figure 0: Building the tree

returns a tree with the b ounding rectangle stored at each internal no de and the original

p oints at the leaves. The b ounding rectangles are needed for building the well-separated

realization (e.g. to determine when no des are well separated).

For uniformly distributed sets of p oints the Build Tree algorithm will run in O (n log n)

time without any sp ecial tricks since �nding the b ounding rectangle and splitting P take

O (n) time and the two recursive calls will b e on sets of approximately the same size (i.e.,


-----

we have a standard T (n) = T (n=) + O (n) style recurrence). Furthermore the algorithm

is highly parallel since the two recursive calls can b e made in parallel and the data can b e

split in parallel In fact for most \practical" sets of p oints this will b e true.

If the cut do es not evenly divide the p oints, however, the naive algorithm could take




O (n


) time. For example, if there is a sequence of p oints that are exp onentially approaching


a �xed p oint. In this case the algorithm can b e slightly mo di�ed so that it still runs in

O (n log n) time. This mo di�ed version is outlined as follows.

. Keep the p oints in linked lists sorted by each dimension

. In the selected dimension, come in from b oth sides until the cut is found

. Remove cut elements and put aside

. Rep eat making cuts until the size of the largest subset is less than (=)n

. Create subsets and make recursive calls.

The runtime for building the tree is thus sp eci�ed by

k

X


T (n) =


T (ni


) + O (n)


k

= n and maxi= (ni


i=



n.




such that


Pk

i=


ni


) =


This solves to O (n log n) indep endent of how inbalanced the tree ends up b eing. A

problem is that it do es not parallelize easily. Callahan and Kosara ju show how it can b e

parallelized, but the parallel version is even more complicated and is not work-e�cient (the




pro cessor-time pro duct is O (n log


n)). We will not cover this complicated parallel version


since in practice parallelizing the simple version is b oth more e�cient and likely to b e highly

e�ective.

. Algorithm: Well-Separated Realization

Once we have a decomp osition tree we can use it to build the well-separated realization.

The following algorithm returns the set of interaction edges in the well-separated realiza
tion. The basic idea is to �rst generate interaction edges within the left and right children

(recursive calls to WSR) and then generate interaction edges b etween the two children (call

to WSR Pair).

function WSR(T )

// T is a decomp osition tree

if Is Leaf(T ) return ;

else

return WSR(Left(T )) [

WSR(Right(T )) [

WSR Pair(Left(T ),Right(T ))

end


-----

function WSR Pair(T ;


; T


)


// T


and T


are two disjoint decomp osition trees


if Well Separated(T,

else


, T )


) return fEdge(T


; T





)g


if (lmax(T





 ))


) - lmax(T


return WSR Pair(Left(T ), T ) [ WSR Pair(Right(T), T )

else

return WSR Pair(T, Left(T )) [ WSR Pair(T, Right(T))

end

The idea of WSR Pair(T, T ) is to return an interaction edge if T and T are well separated.


return WSR Pair(Left(T

else


), T





Otherwise it picks the no de with a larger lmax


and splits that no de and calls itself recursively


on the smaller and the two halves of the larger.

Figure 0 gives an example of the algorithm along with call tree for WSR Pair(T


; T ).


In the example the algorithm determines that lmax


(T





(T


) and therefore splits T


in


) - lmax


the recursive calls. At the next level it splits T


, at which p oint it determines that T


is well


separated from T





and therefore makes no more recursive calls on that branch.

###### T

 T1
 T21 T11 T12 T2 L1

 T22 L2

 WSR_Pair(T1,T2)  L1>L2

 WSR_Pair(T1,T21) WSR_Pair(T1,T22)

|T11|T12|
|---|---|

|T|Col2|
|---|---|
|T1 T11 T12 T2 L2|T21|
||T22|


###### WSR_Pair(T11,T21) WSR_Pair(T12,T21)

Figure 0: Generating the Realization. The tree represents the call tree for WSR Pair.

. Bounding the size of the realization

By b ounding the size of the realization we b oth b ound the numb er of interaction edges and

also b ound the runtime for building the realization since the runtime of WSR is prop ortional

to the numb er of edges it creates.

We will use the following to b ound the total numb er of interaction edges generated by

WSR (size of realization):


-----

Figure 0: Non-intersecting rectangles

� Prop erties of the tree no des - show b ounding rectangles are not \to o thin"

� Bound # of non-intersecting rectangles that can touch a cub e of �xed size (Figure 0).

This assumes the rectangles are not to o thin.


� Bound # of calls to WSR Pair(T


, T


or T


.








) for each cell T


We de�ne an outer rectangle for each b ounding rectangle such that these outer rectangles

�ll space (i.e., the union of all rectangles at a given level of a tree �ll the initial space). The

outer rectangle for each no de in the decomp osition tree is de�ned as follows and illustrated

in Figure 0.





>>

>>>

<

>>

>>>

>:


Smallest enclosing cub e at ro ot

Use hyp erplane that

divides R(P ) to internally

^


^

R(P ) =

>>

>>>

>:

^ lmax

min(R (A)) �


divide

(p(A))


R(P )


Lemma  l


, where p(A) = parent of A in the tree.




Proof: By induction.

Base: true when p(A) = ro ot, since lmin


^

(R (A)) =


lmax(p(A))




.


Induction: if true for p(A) then true for A,


min(R^ (A)) = lmin

^


^


Case : l


(R (p(A))). True, since lmax


(p(A)) � lmax


^ lmax(p(p(A)))

tion lmin (R(p(A))) =  .

^ ^

Case : lmin(R (A)) < lmin (R(p(A))). First we note that lmax


(p(p(A))) and by induc
^


(p(A)) and l


min(R (A)) must


b e along the same dimension since Build Tree cut p erp endicular to lmax(p(A)) and


R^ (p(A)) contains R(p(A))


if lmin


(R^ (A)) has decreased it must have b een cut. Since


lmax


(p(A))




cutting R(p(A)) in half will mean that lmin


(R^ (A)) �


.





-----

|^ R1 R1|^ R2 R2|
|---|---|

|^ ^ R1 R2 R2 R1 ^ R1 ^ R3 R1 R3 ^ R2 R2 R4 ^ R4|Col2|Col3|
|---|---|---|
||^ R1 R1|^ R3 R3|
||^ R2 R2||
|||R4 ^ R4|


Figure 0: Outer Rectangle

###### l’

 l(c)
 +2 l’


###### l(C)


###### ( One factor for each      dimension )


Figure 0: Pro of of Lemma 


-----

###### possibly well separated P2

 Lmax
 P1 P3 well separated

 ( s * sqrt(d) + 2 * sqrt(d) + 1 ) lmax

Figure 0 : Well separatedness

0

|Col1|P2|
|---|---|

|Col1|P1|poss P2 P3|
|---|---|---|
||||


Lemma  Given a d-cube C and a set S of disjoint d-cubes of length l

!d

l (C )


that overlap C, then


jS j �


+ 


0


),pthen for P


.

Proof: By picture (Figure 0). 

It's not hard to show that if lmax(P


l

maxp


) � l


(P


not to b e well separated


from P


it must intersect a d-cub e of length (s


d + 


d + )lmax


(P


) centered at the center


of P


(Figure 0 ).


Note: we will only split P


in WSR Pair(P


, P ) if P


and P


are not well separated.

0


Putting everything together


Consider for a given no de P of the decomp osition tree, all invo cations WSR Pair(P,P

0


) such


that lmax


(P ) � lmax

0


(P


).


. all P


must b e indep endent (consider recursive structure of the algorithm WSR Pair)

0


))


lmax (p(P



0


0


0

)) �


so we can b ound the numb er of P


. we know lmin

.


(R^ (P


to


p


jP


j < ((s


p

d + 


d

d + ) + )


Therefore, the total # of calls to WSR Pair(P,P


) is b ound by

d


p

n((s


p

d + 


d + ) + )


= O (n)


The factor of two at the front comes from the fact that we are counting non-leaf invo cations


of WSR Pair(T


,T


) while the interactions are created by leaf invo cations. However, the


total numb er of leafs is at most twice the numb er of internal no des|see Figure 0.

We note that this b ound is very conservative and in practice the algorithm actually uses

many fewer interactions.


-----

###### recursive call tree


###### what we counted

 what we want

 worst case

Figure 0: Counting leaves only


 N-b o dy Summary

� Algorithms

{ Particle-Particle

{ Particle-mesh (several variants)

{ Particle-cell (App el, Barnes-Hut, Press)

{ Cell-cell (FMM, Callahan-Kosara ju)

� Applications

{ Astronomy

{ Molecular Dynamics

{ Fluid Dynamics (elementless metho ds)

{ Plasma Physics


-----

Algorithms in the Real World Notes by Rich Vuduc

Lecture # (VLSI Physical Design ) �c   Rich Vuduc and Guy Blello ch

� Notes regarding the homework assignment

. Representing Delaunay triangulations

. Incremental Delaunay

. Rupp ert meshing

. Surface approximation

� Intro to VLSI Physical Design

. Overview of the VLSI pro cess

. The role of algorithms in physical design

� Summary

� References

 Some notes regarding the homework assignment

Here we discuss a few implementation details that are relevant to a few of the recent algo
rithms which we have considered.

. Representing a Delaunay triangulation

There are a numb er of application-dep endent approaches to storing the mesh triangulations,

such as the one shown in Figure . Below, we discuss three p ossibilities: neighb or graph,

quad edge, and triangle representations.

Figure : A sample mesh.


-----

###### 2


###### 3

 4 5


###### 1


###### 6 7

Figure : In the neighbor graph representation, we interpret the triangulation as a graph

and store each vertex with a list of its neighb oring vertices.

.. Neighb or graph

In the neighbor graph representation, we treat the no des of the mesh as vertices in a graph,

as shown in Figure . There, for each vertex we would store its adjacent vertices:

vertex neighb ors

 f , ,  g

 f , , ,  g

 f ,  g

 f , , , ,  g

 f , , ,  g

etc. : : :

It is generally helpful to keep each list of adjacent vertices ordered (in the ab ove example, we

have stored them in counterclo ckwise order, but you could use any ordering that is convenient

for your application).

.. Quad edge

Instead of using only vertices for our primary representation, we could store edges instead.

One clever way to store edges is called the quad edge data structure (Guibas and Stol�, ACM




Trans. Graphics, (),  )


. This data structure is de�ned along with an \edge algebra"


which allows one to traverse a triangulation easily. In this representation we keep a structure

for each edge which stores the  adjoining edges as we travel clo ckwise and counter clo ckwise

from each endp oint of the edge. For example in Figure  the four edges adjoining edge 

are , ,  and , and the four edges adjoining edge  are , ,  and . In fact the data

structure keeps a p ointer to one of the  �elds within each of these adjoining edges. This

makes it p ossible to easily circle around a vertex or an edge. The table b elow shows an

example of our internal representation for the mesh shown in Figure . The value after

the dot represents which of the  entries in the edge is b eing p ointed to.



This was the format used by Garland and Heckb ert [] in their original work. However, in comments to

Prof. Blello ch they mentioned that this representation was not particularly well-suited to their application.


-----

###### 2

 1
 6
 5 7

 4
 12

 8
 9
 3
 10

 11

Figure : For the quad-edge format, we store each edge along with the  adjoining edges

(when traveling clo ckwise and counterclo ckwise).

edge neighb oring edges

 f .0, ., ., . g

: : :

 f .0, ., ., . g

 f ., ., .0, . g

: : :

 f .0, ., ., . g

f 0.0, ., .0, . g

: : :

 f .0, 0., ., . g

: : :

To circle around a vertex we start at an even �eld of an edge structure (.0 or .) and

follow the p ointers, and to circle around a face (triangle) we start at an o dd �eld (. or .).

For example, to circle around the vertex in the middle starting at edge  we simply start by

following .0 and continue around touching edges , ,,  and back to  (more sp eci�cally

.0, ., ., .0, .0). Similarly to circle around triangle (,,) we can start from . and

visit ., . and back to ..

The algebra on the quad-edge data structure suggested by Guibas and Stol� uses the three

op erations next, rotate, and symmetric which take a p ointer and return a new p ointer.

The next op eration circles around a vertex or triangle, the rotate op eration switches from

a vertex to a triangle (the one that shares the edge, next edge, and vertex) or vise versa,

and the symmetric op eration switches to the vertex at the other end of the edge. Assuming

each quad-edge is an array of  \p ointers" each consisting of a p ointer to another quad-edge

and an index within the quad-edge, then for a p ointer (e,i) the op erations are de�ned as:

next(e,i) = e[i]

rotate(e,i) = (e, i+)

symmetric(e,i) = (e, i+)


-----

Figure : Mesh representation using triangles. Triangle  shares sides with triangles  and

.

where + is de�ned mo dulo .

.. Triangles

Lastly, we turn to what is p erhaps the most natural representation: triangles. With each

triangle, it may b e useful to store the  other with which it shares a side. So, for the example

shown in Figure , our table of data might lo ok something like:

triangle side-adjacent triangles

 f , ,  g

 f , ,  g

 f , ,  g

 f , ,  g

 f , ,  g

 f , ,  g

In addition to the neighb oring triangles it is typically useful to store the vertices of each

triangle. In this representation the function opposite(p,T) which given a triangle T and

a vertex (p oint) p on that triangle returns the triangle opp osite that p oint is often useful.

For example, in Figure  given the leftmost p oint and triangle , opposite would return

triangle .

. Incremental Delaunay

Recall that in the incremental Delaunay algorithm of previous lectures, we are given a

triangulation to which we wish to add an additional p oint. The suggested approach is based

on a depth-�rst search style algorithm. Figure  illustrates the action of the following

pseudo co de to insert a p oint p into an existing triangulation.


-----

function Insert(p; R)

// p a p oint

// R an existing triangulation

T = the triangle containing p


(T


; T


; T


 ) = the triangles created by splitting T by p


Patch(p; T

Patch(p; T

Patch(p; T

end


)

)

)


function Patch(p; T )

0


T


= Opp osite(p; T )

0


if InCircle(p; T


)


(T


; T


) = Flip(T ; T


0

)





Patch(p; T

Patch(p; T


)

)


end

The function Flip �ips two adjacent triangles so the crossedge changes.

. Rupp ert Meshing

In this section we discuss two issues to consider when implementing Rupp ert's meshing

algorithm [].

The �rst relates to how one �nds encroaching p oints. First, recall that a p oint p en
croaches up on a segment s if p lies within the diametrical circle de�ned by s (see Figure ).

To determine which p oints encroach up on s, it is su�cient to check endp oints of all Delau
nay edges that come out of an endp oint of the segment. In a practical implementation, one

would probably need a data structure that facilitates moving from p oint to p oint within

the triangulation; one p ossibility would b e a data structure that keeps neighb oring triangles

with each p oint.

The second issue relates to the creation of phantom smal l angles, which is b est explained

by an example. In particular, supp ose that our input p olygon is the one shown in Figure 

(top). Recall that an initial step in computing the triangulation requires that we compute

the convex hull of the input p olygon; this could result in the creation of phantom smal l

angles such as the one shown in Figure  (bottom-left). An easy solution is to �rst create

a b ounding b ox around the input p olygon, as shown in Figure  (bottom-right).

. Surface Approximation

One imp ortant step in the surface approximation algorithm discussed in a previous lecture is

to �nd the largest error in a newly added triangle. This requires examining every p oint within

the triangle. One technique for doing so might b e to b ound the triangle under consideration

by a rectangle �rst, then scan the pixels within the triangle row- or column-wise. For each


-----

###### p

 p

 T T1 T2

 T’

Figure : (Top-left) We wish to add the p oint p to an existing triangulation, and p happ ens


to fall within the triangle T . (Top-right) Adding p creates the smaller triangles T


, T


.





, T


(Bottom-left) We consider the action of the Patch subroutine at some p oint in the recursion

for the p oint p and some other triangle T (i.e., not necessarily the same as ab ove). (Bottom
0


right) Result after executing flip(p, T


).


###### diametrical circle

 s

 p

Figure : In the situation shown, we wish to see if there are any p oints in the triangulation

that encroach on the segment s (e.g., p).


-----

###### bounding-box


###### phantom angle

 convex-hull edge

Figure : (Top) Input p olygon. (Bottom-left) Initial convex-hull computation results in

creation of tiny \phantom small angles." (Bottom-right) One easy solution is to placing a

b ounding b ox around the �gure, and then triangulate this new �gure.

###### . . . . . . . . . .. . . . . . . .. . .
 . . . . . . .

 scan

Figure : In computing the error of a newly added triangle in the surface approximation

algorithm, we can b ound the triangle by a b ox and scan, testing whether or not the pixel

lies within the triangle b efore using it to compute the error.

pixel that we scan, we can check whether or not it falls within the triangle b efore computing

its error. (See Figure .) A fancier metho d would �nd the edges that b order on the left

and right and only scan the horizontal lines b etween them.

 Intro to VLSI Physical Design Automation

Since the dark ages (i.e., the  0's), a typical integrated circuit design has grown from

a hundred transistors to the millions of transistors required by mo dern micropro cessors.

Very large scale integration (VLSI) refers to the pro cess of integrating such a large numb er

of transistors for fabrication; VLSI physical design is the pro cess of converting a circuit

description into a layout. The ability to lay out such enormous circuits has b een made

p ossible by the intelligent application of computer algorithms.


-----

Here, we give a brief overview of the overall VLSI physical design pro cess, and show

where algorithms play a key role. We will b e making a numb er of references to diagrams



shown in [].

. Overview

The following is a high-level description of the VLSI design pro cess. The fo cus of our

discussions will b e on step  b elow.

. System sp eci�cation: The �rst step involves the creation of a formal, high-level

representation of the system. In this stage, we consider the desired functionality,

p erformance, and physical requirements of the �nal pro duct.

. Functional design: In this step, we break down the system into functional sub
units, and sp ecify the relationships b etween them (for example, by generating a timing

diagram or showing the desired �ow b etween sub-units).

. Logic design: In this pro cess, we formalize the logical structure of our functional

design, typically by generating b o olean formulas. An interesting problem is how to

minimize such expressions, and neat algorithms like binary decision diagrams have

found applications here. However, we will not b e discussing these.

. Circuit design: From the logic design, we next need to generate a circuit represen
tation. We have to consider p ower and sp eed requirements of our original design, and

often p erform simulations of electrical b ehavior in this stage (e.g., through the use of

PSpice software).

. Physical design: In this stage (the fo cus of our discussions), we must actually lay out

the circuit designs. We must ensure that our resulting layout conforms to the physical

and geometric constraints of our system, which we formulate as design rules. These

design rules are essentially guidelines based on physical constraints due to limitations

in the fabrication pro cess.

. Fabrication: This stage is the actual physical manufacturing step, in which we prepare

the wafer and dep osit/di�use various materials onto the wafer.

. Packaging, testing, and debugging: In this stage, we test the actual manufactured

and packaged chip.

It is imp ortant to note that this entire design pro cess is iterative, i.e., there is a kind of

\feedback" e�ect in which we examine the results, p erform any necessary hand-tuning, and

re-run the pro cess, continually re�ning our previous results.



In fact, most of the material here is simply a paraphrase of material that app ears in [].


-----

.. Physical design

We now turn our attention to the physical design cycle which will b e our fo cus. The following

is a brief summary of the high-level pro cess. Note that the input to this pro cess is the circuit



design, and the output will b e a layout ready for the fabrication stage.

. Partitioning: We must �rst break down, or partition, the input circuit into more

manageable blo cks (or sub circuits, or mo dules). In the partitioning pro cess, we must

consider the size and numb er of blo cks, as well as the numb er of interconnections which

will obviously a�ect the routing. The set of interconnections is called a netlist. For

large designs, the blo cks may b e hierarchical.

. Flo orplanning and placement: In �oorplanning, we consider such factors as the

exact size of the blo cks generated in the previous step. This is a computationally

di�cult step, and often requires a design engineer to do this by hand. During placement,

we p osition the blo cks exactly as they will app ear on the chip. We want to lay out

the blo cks in such a way so as to minimize the area required to complete all the

interconnections. This is generally an iterative pro cess in which we lay out the blo cks,

and continually re�ne the placements.

Furthermore, it is crucial to use a go o d placement strategy b ecause the placement

essentially determines the routing (see b elow).

. Routing: In the routing phase, we lay out the interconnections (i.e., put down wires)

sp eci�ed by the netlist that was generated in the partitioning phase (ab ove). We refer

to the space not o ccupied by blo cks as the routing space. We partition this space

into rectangular regions called channels and switchboxes. Our router must make the

connections using only these two typ es of regions, and it must do so in such a way so

as to minimize wire length.

The routing pro cess can b e divided into two phases. In the �rst phase, called global

routing, in which the global router must make a list of channels (i.e., passageways)

through which to route the wire. The next phase, called detailed routing, completes

the actual p oint-to-p oint wiring.

Although the routing problem is computationally hard, many heuristic algorithms have

b een develop ed.

. Compaction: In this �nal phase, we compress the generated layout to reduce the

total area. A smaller area would enable us to increase the yield.

.. Design styles

Although we have taken the entire physical design pro cess and broken it up into smaller

subproblems, we have noted that each subproblem is still computationally hard. To make

these problems more tractable (and thus reduce the time-to-market and increase the yield),

we can further restrict our design metho dology into one of the following design styles:



Automation of the entire physical design pro cess is akin to the idea of building a \silicon compiler."


-----

. Full custom: We use this term to refer to a design style which places few (if any)

constraints on the physical design pro cess. For example, we would place no restrictions

on where a blo ck could b e placed (e.g., on a grid). Clearly, this is the most di�cult

design style to automate b ecause of the high degree of freedom. A ful l custom approach

is really only appropriate when p erformance must b e high. For instance, this is the

metho d of choice for the layout of mo dern micropro cessors. An example is shown in

[] (Figure .).

. Standard cell: In the standard cel l design style, we predesign certain functional units

as standard cells, or standard blo cks, and create a cel l library of \pre-packaged" blo cks

that we can then use for placement. Each cell is preanalyzed and pretested. Given that

the cells are predesigned, the main challenge is the layout and routing. An example

of a standard cell layout is shown in [] (Figure .). Notice that the blo cks are all of

a similar shap e and size, and that their layout is much more regular than the layout

of the full-custom design shown in [] (Figure .). Observe that in the standard cell

design, our only (roughly sp eaking) degree of freedom is the ability to shift blo cks to

op en up routing channels b etween placed cells.

. Gate arrays: A gate array is like a standard cell except that all the \cells" are

the same, and laid out in an array form as shown in [] (Figure .). The name is

indicative of the idea that the cells could b e as simple as a single gate (a -input NAND

gate is shown). Furthermore, the routing channels are basically predetermined. The

advantage of the gate array style over the previous two is its simplicity. In particular, it

is cheap er and easier to pro duce a wafer based on this style. Routing is also simpli�ed,

since we only have to make connections and not worry ab out minimizing the area used.

An example of a routed gate array for a simple logic circuit is shown in [] (Figure

.).

However, the cost is the rigidity imp osed|we would certainly b e forced to pro duce

larger chips and incur a p erformance p enalty.

. Field programmable gate arrays: A �eld programmable gate array (FPGA) is

something in-b etween the gate array and standard cell. An example is shown in []


(Figure .). Each \cell" of a FPGA (lab eled by Bi


in the �gure) can b e viewed as a


lo okup table that can b e programmed. Furthermore, there is no free region over which

we do our routing; instead, the wires are �xed, and we connect the cells by burning

in fuses (shown as squares and circles). The �gure shows a sample logic circuit which

has b een partitioned into four regions. We construct the lo okup table for each region,

and this is what is programmed into the cells of the FPGA (in this example, the four


left-most cells lab eled Bi


). The connections appropriate fuses are burned in (shown as


darkened circles and squares). The partitioning problem for FPGAs is di�erent from

that of the other design styles, but the placement and routing problems are similar to

those of the gate array.

We summarize the various tradeo�s alluded to ab ove as follows [] (table .):


-----

Figure  : The op eration of an nMOS transistor. (a) A vertical cross-section of a transistor

based on the n � p � n junction. (b) When a voltage has b een applied to the gate, the induced

electric �eld alters the conducting prop erties of the channel, thereby allowing current to �ow.

(c) Schematic representations of the pro cess. [Taken from [] (Figure .).]

style

Area compact compact to mo derate mo derate large

Performance high high to mo derate mo derate low

Fabrication layers all all routing layer none

In general, within a given column of the table there is a correlation b etween the rows.

Moreover, the columns are roughly ordered in decreasing cost.

.. Transistor level

When we discuss algorithms in future lectures, it will b e su�cient to formulate the routing

and placement problem at an abstract level. However, in this section, we will very brie�y

lo ok at the \small picture" for a little p ersp ective.

Figure  shows a diagram of the vertical cross-section of a nMOS transistor, as well as

its schematic representations. An nMOS transistor is an example of a more general kind of

transistor called a �eld-e�ect transistor. In such a device, we can control the �ow of current

b etween the two terminals (lab eled source and drain) by controlling the voltage applied to the

non-conducting terminal called the gate. In particular, applying a voltage to the gate sets up

an electric �eld that changes the conducting prop erties of the region lab eled channel thereby

allowing current to �ow from the source to the drain. For a more general intro duction to

the basic solid-state physics b ehind the op eration of these devices, see [] and [].

By combining several transistors, we can construct basic logic gates such as the NAND

gate shown in Figure 0. See the �gure caption for a rough description of its op eration.

Finally, note that in the �gure of the NAND gate, there are various rectangular shaded

regions which represent di�erent materials. These materials must ob ey certain rules, namely,

they must b e of certain dimensions and must b e separated by di�erent amounts, as shown

in Figure . These are the kinds of rules and constraints we will b e sub ject to in our

automation algorithms.


-----

Figure 0: The layout of CMOS NAND gate (left) using four transistors, and its schematic

representation (right). The input to the NAND are lab eled A and B, and the output is

C. The b ottom two transistors are n-channel and op en when their gates are high while the

top two are p-channel and op en when their gates are low. (Basic operation) When A and

B are b oth high, the channels of the upp er-two transistors are closed and the b ottom two

are op ened, thus enabling a connection from GND to C. In all other cases, the channels of

at least one of the lower transistors will b e closed which will break the connection b etween

GND and C, whereas when either channel of the upp er two transistors are op en, C will b e

pulled up to VDD. [Taken from [] (Figure .).]

Figure : Size and separation rules. The dimensions have b een characterized in terms of

the design parameter �. The \." of the terms \. micron technology," et al., refer to this

parameter. [Taken from [] (Figure .0).]


-----

. The role of algorithms

Algorithms have played a crucial role in the explosive growth of VLSI technology. Graph

theory has played a particularly imp ortant part. Here is a list of some of the many algorithms

that have b een applied to VLSI physical design automation:

. Graphs

� spanning trees

� shortest path

� matching

� Steiner trees

� maximum indep endent set

� maximum clique

. Computational geometry

� intersection of lines or rectangles

. Optimization

� integer programming

These algorithms have found applications in many of the design areas discussed in the phys
ical design overview, namely

� layout

� partitioning

� placement

� routing

� compaction

Furthermore, these algorithms are applicable in all the di�erent design styles (full-custom,

standard cell, etc.). We will b e paying particular attention to the routing problem.

Our overall goal will b e either to minimize area given physical constraints on our design,

or to maximize functionality in a given �xed area. We will have to b e concerned with how

to:

minimize delays : In particular, we can accomplish by minimizing wirelength and reducing

capacitance (by keeping the overall layouts small).

reducing the numb er of layers Increasing the numb er of layers required in a design greatly

increases fabrication costs.


-----

reducing the numb er of pins : Of particular concern in multi-chip mo dules.

All of the ma jor designers and manufacturers of VLSI chips are investing heavily in au
tomation research and techniques. However, hand-tuning still has an imp ortant place in the

design phases.

. Evolution

We will close by summarizing the history of development to ols in physical design automation.

Year Design To ols

 0-  Manual design

 -  Layout editors

Automatic routers

E�cient partitioning algorithms

 -  Automatic placement to ols

Well de�ned phases of design of circuits

Signi�cant theoretical development in all phases

 -present Performance driven placement and routing to ols

(in particular, an emphasis on space and sp eed)

Parallel algorithms for physical design

Signi�cant development in underlying graph theory

(i.e., the use of theoretical results)

Combinatorial optimization problems for layout

 Summary

In the �rst section, we gave some notes ab out implementation metho ds for several triangu
lation algorithms. In particular, we discussed some ideas for data structure representation,

with the triangle representation seeming the most useful.

We then gave a brief overview of the entire VLSI design pro cess, and intro duced the

physical design stage in more detail. We showed that algorithms play an imp ortant role,

our overall goal b eing to minimize the layout area (to increase our chip's p erformance) while

sub ject to various constraints of our physical design (e.g., separation).

References

[] M. Garland and P. Heckb ert. \Fast p olygonal approximation of terrains and height

�elds." CMU Technical Rep ort, CMU-CS- -, Carnegie Mellon University, Pitts
burgh, PA, Septemb er  .

[] J. Rupp ert. \A Delaunay re�nement algorithm for quality -dimensional mesh genera
tion." NASA Technical Rep ort, RNR- -00, January  .

[] N. Sherwani. Algorithms for VLSI Physical Design Automation. Kluwer,  .


-----

[] C. Kittel. Introduction to Solid-State Physics. Merriam, (�ll in details),  .

[] On-line course notes on \Hetero junction Devices" from the University of Colorado.

[http://ece-www.colorado.edu/~bart/.htm]


-----

Algorithms in the Real World Notes by Mehul Shah

Lecture # (VLSI Physical Design ) �c   Mehul Shah and Guy Blello ch

� Intro duction to VLSI Routing

� Global Routing

� Two terminal routing (shortest paths)

. Dijkstra's algorithm

. Maze routing

� Multi terminal routing (Steiner trees)

. Steiner tree de�nitions

. Optimal rectilinear steiner trees

 Intro duction to VLSI Routing

In the physical design of VLSI circuits, the routing phase consists of �nding the layouts for

the wires connecting the terminals on circuit blo cks or gates. It assumes the lo cations of

the blo cks have already b een determined, although some routing schemes allow a certain

amount of movement of the blo cks to make space for wires. The basic problem is illustrated

in Figure . A terminal is a lo cation on a blo ck, typically along one of the edges, which

needs to b e connected to other blo cks. A net is a set of terminals that all need to b e

connected to each other. A netlist is a collection of nets that need to b e routed. The routing

space is the space in which we are allowed to place wires, typically any space not taken by

blo cks. The routing space b etween two blo cks is called a channel. The routing problem is

the problem of lo cating a set of wires in the routing space that connect all the nets in the

netlist. The capacities of channels, width of wires, and wire crossings often need to b e taken

into consideration in the problem.

Given that there can b e millions of transistors on a chip and tens of thousands of nets to

route, each with a large numb er of p ossible routes, the routing problem is computationally

very di�cult. In fact, as we will see, even �nding an optimal layout (minimum wire-length)

for a single net is NP-hard. Because of the hardness of the problem, most routing algorithms

are approximate and will not necessarily �nd the b est solution. The �rst simpli�cation

that is typically made is to divide the problem into two phases called global routing and

detailed routing. In global routing the exact geometric details are ignored and only the

\lo ose route" for the wires are determined. More sp eci�cally, the op en regions through

which each wire �ows is computed. This lo ose route is converted to an exact layout in the

latter phase. Detailed routing completes the p oint-to-p oint wiring by sp ecifying geometric

information such as the lo cation and width of wires and their layer assignments. Even with

this breakdown into global and detailed routing each phase remains NP-hard and further


-----

Figure : Some de�nitions.

approximations are used to solve them. In this lecture, we concentrate on the global routing

phase.

The optimality goal of global routing is dep endent up on the nature of the chip design. For

full custom and standard cell designs, the ob jective is to minimize the total area of the �nal

chip. Thus, in the full custom designs the total wire length is minimized, or the maximum

wire length is minimized, or changes to placement are minimized. In the standard cell design,

the maximum wire length is minimized or the total channel heights are minimized. In gate

arrays, the previous phases assign gates to blo cks, and the primary goal is to determine

the feasibility of routing. If feasible, the maximum wire lengths are minimized; otherwise,

di�erent assignments are sought. Variants of shortest paths algorithms are employed for

many of these computations.

 Global Routing Algorithms

In the global routing phase, the input is a netlist consisting of a set of nets each of which is

a set of terminals. We will distinguish b etween two-terminal nets and multi-terminal nets.

Most chips will have b oth typ es and di�erent algorithms are often used for each.

In addition to the netlist we need some way to sp ecify the routing space. This is typically

done as a graph. There are two graph mo dels which are often used: the grid graph mo del

and the channel-intersection graph mo del. In the grid graph mo del the chip is mo deled as a

regular n � m grid graph with vertices that do not b elong to the routing space removed (e.g.,

vertices o ccupied by a blo ck, or p ossibly already routed to capacity). Wires can b e routed

along any edges of this graph and one typically assumes each edge has unit capacity (i.e,

only one wire can b e routed on it). All edges in this mo del have the same length. Figure 

shows an example|the shaded vertices b elong to blo cks and therefore do not b elong to the


-----

###### A


###### 2


###### C


###### 7
 2
 B

 B 2 2 1
 2
 A
 2
 C

 8 4
 B

Figure : An example of a channel-intersection graph mo del. The circles are the vertices,

the letters are terminals, and the numb ers sp ecify the length of each edge.

graph. In the channel-intersection graph mo del vertices are placed at all intersections of the

channels, and at the terminals. The lengths of the edges are no longer all the same and the

capacity of each edge represents the numb er of wires that can b e routed along it. Figure 

shows an example. We will consider algorithms for b oth typ es of graphs.

Generally, two approaches are taken to route the nets. The �rst approach is to route

sequentially by laying down one net at a time based on constraints from previous nets, and

the second is to route all the nets simultaneously. The �rst approach will typically not

give as go o d routes, but is computationally much more feasible. In this lecture we will just

consider the �rst approach and in the next lecture we will consider an algorithm based on

integer-programming for the second approach.

When laying down the nets sequentially, dep ending on the order the nets are laid out,

some nets already routed may blo ck others yet to b e routed. One approach to mollify

this problem is to sequence the net according to various factors: its criticality, p erimeter

of the b ounding rectangle, and numb er of terminals. However, sequencing techniques are

not always su�cient, in which case, \rip-up and reroute" and \shove-aside" techniques are

employed. The \rip-up and reroute" technique involves removing the o�ending wires which

blo ck the a�ected nets and rerouting them. The \shove-aside" technique moves wires to

allow for completion of failed connections. Another approach is to route nets with two or

three terminals �rst since there are few choices for routing them and they comprise a large

p ortion of the netlist.

We now consider the following algorithms for laying down each net.

� Two terminal algorithms (shortest paths)

. Dijkstra's algorithm (intersection graphs)

. Maze routing and Hadlo ck's algorithm (grid graphs)

� Multi-terminal algorithms (Steiner trees)


-----

. Optimal rectilinear steiner trees

 Two-Terminal Nets: Shortest Paths

The shortest path problem we consider involves an undirected graph G = (V ; E ) with p ositive

edge weights (representing the length of each edge). Our goal is to �nd a path from a given

source to a destination that minimizes the sum of edges weights along the path.

. Dijkstra's Algorithm

Dijkstra's algorithm is one such single source shortest path algorithm, and in fact in its

general form �nds the shortest path from the source to all vertices. The algorithm starts

from the source vertex and pro ceeds outward maintaining a set S of vertices that have b een

searched. Any vertex that is not in S but is a neighb or of a vertex in S is said to b e in the

fringe. It pro ceeds until all vertices are lab eled with their shortest distance from the source

(or until the destination is encountered). The algorithm and an example of one of the steps

is shown in Figure . The last three lines maintain the invariant b etween iterations since

d[v ] is correct when v is added to S and b ecause for all new fringe no des their shortest path

through S [ fv g is either through S, which was previously correct, or through v which has

length d[v ] + w (u; v ).

If the fringe vertices are maintained in a priority queue with their distance to S as the

priority, then each findmin and mo di�cation of the d[u] takes O (log n) time, where n = jV j.

Since there are at most n findmin op erations and at most m = jE j mo di�cations to the d[u]

(one for each edge), the time is b ound by O (m log n). A Fib onacci heap implementation of

the queue, however, can reduce the amortized running time to O (n log n + m) (see CLR).

Note, if all edge weights are constant and equal then this metho d reduces to breadth-�rst

search.

If all we want to �nd is the shortest path to a single destination d, then Dijkstra's

algorithm can terminate as so on as d  S (as so on as d is visited). The algorithm, however,

moves uniformly in all directions from the source in a b est-�rst manner, so in general a large

part of the graph might b e visited b efore d. For graphs which can b e emb edded in Euclidean

space (i.e. the triangle inequality holds for edges within the graph), the e�ciency of this

search can b e improved by biasing the search toward the destination. This optimization can

b e very b ene�cial when making two-terminal connections in VLSI layout.

To bias the search toward the destination the mo di�ed algorithm uses a di�erent priority

for selecting the next vertex to visit. Instead of d[v ], the length of the path from the source,

it uses d[v ] + L(v ; d), where L(v ; d) is the Euclidean distance from v to the destination d.

By including L(v ; d), the search will b e biased toward vertices with shorter distance to the

destination. However, we have to make sure that the algorithm still works correctly. This is

guaranteed by the following theorem, which is illustrated Figure .


Theorem  For a step of the modi�ed Dijkstra's algorithm, in Figure  if P


+ L


�


P


+ L





� P


+ P


.


then P


-----

function Dijkstra(G; s)

// G = (V ; E ) is a input graph with nonnegative edge weights w (u; v ); (u; v )  E

// s is the source vertex

// Result: for each v  V, d[v ] = shortest distance from s to v

forall (v  V ), d[v ] = 

d[s] = 0

S = ;

while S = V // not all vertices have b een searched

// Lo op Invariants:

// for all v  S, d[v ] is shortest path from s to v

// for all v  F r ing e, d[v ] is shortest path exclusively through S from s to v

v = no de v  F r ing e with minimum d[v ]

// Note that d[v ] is the shortest path to v from s b ecause

// : shortest path through S to v is d[v ] (by the lo op invariant)

// : any path through a vertex u  (V � S ) must b e at least as long as d[v ]

// since d[u] � d[v ] and all edge weights are nonnegative.

S = S [ fv g // \visit" v

for u  neighb ors(v )

d[u] = min(d[u]; d[v ] + w (v ; u))

end

###### Fringe
 6
 3

 3

 3
 Searched
 2
 2
 2 S 3

 4 2 3
 2
 2
 4

 3 2
 7

Figure : The co de for Dijkstra's algorithm and a snapshot of one iteration.


-----

###### P : Minimum Path Length L : Euclidean Distance

Figure : Incorp orating the Euclidean distance into the priority maintains the invariant

while forcing Dijkstra's algorithm to move in the direction of the destination.


Proof: P


� L


, a prop erty of Euclidean graphs. Also, L


� L


� L


, which follows from


the triangle inequality. Our assumption states:


P


� P


+ L


� L


Thus,




P

P


� P

� P


+ L

+ P


This theorem implies that if we use P + L as the priority then when P


+ L


is the fringe


vertex with the minimum priority we are sure there is no shorter path to it through some u

not in the searched vertices S and our invariant is maintained.

Exercise: Consider an n � n grid graph in which al l edges have unit weight. If the source is

in the midd le of the left boundary and the destination is in the midd le of the right boundary,

how many vertices wil l the modi�ed Dijkstra's algorithm take compared to the original? How

about if the source is on the lower left and the destination on the upper right?

. Maze Routing

Finding shortest paths on a grid-graph is a sp ecial case of the general shortest path problem

where all weights are the same (unit). In the context of VLSI routing, �nding such shortest

paths for two-terminal nets is called maze routing. A simple approach for maze routing is

to p erform a breadth-�rst search from source to destination (this is referred to as \Lee's


-----

|Col1|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Col10|
|---|---|---|---|---|---|---|---|---|---|
|||||||||||
||||||D|||||
|S||||||||||
|||||||||||
|||||||||||


Figure : The right �gure shows the path determined by a maze route b etween S and

D on a grid graph mo del of the circuit area in the left �gure. For Hadlo ck's algorithm,

M (S; D ) = , and d(P ) =  b ecause the path turns away from D once.

Algorithm" in the VLSI community). Such a search is faster than Dijkstra's algorithm

since it only takes constant time to visit each vertex. However, like Dijkstra's unmo di�ed

algorithm it makes no attempt at heading toward the destination.

In a similar spirit to the mo di�ed version of Dijkstra's algorithm Hadlo ck observed that

the length of a path on a grid from s to t is M (s; t) + d(P ), where M (s; t) is the Manhattan

distance and d(P ) is the numb er of edges on path P directed away from the target (see

Figure ). Hence, the path can b e minimized if and only if d(P ) is minimized. Thus,

instead of lab eling each vertex on the fringe with the distance, it is lab eled with the numb er

of times the b est path to it has turned away from the target. Hadlo ck's algorithm, therefore

uses the detour numb er d(P ) for the priority in the shortest-path search. As with the

mo di�ed version of Dijkstra's algorithm, this has the e�ect of moving the search toward the

destination.

 Multi-Terminal Nets: Steiner Trees

. Steiner Trees

Given a graph with a subset of vertices lab eled as demand p oints, a minimum Steiner tree

is the minimum set of edges which connect the demand p oints. Figure  gives an example

of a minimum Steiner tree. A minimum spanning tree (MST) is a tree which connects all

vertices with edges with minimum total weight. Finding the minimum Steiner tree is an

NP-hard problem; however, �nding the minimum spanning tree is tractable and, in fact,

quite e�cient. Thus, �nding a minimum spanning tree is the initial step in many of the

algorithms for approximating minimum Steiner trees.

Usually in VLSI circuits, wires are laid down only in horizontal or vertical directions.

Thus, for multi-terminal nets, the demand p oints are a set of vertices on a grid, and the

routing problem is to �nd a minimum rectilinear Steiner tree (RST), one with horizontal or

vertical edges. Finding the minimum RST remains NP-hard so heuristics are employed. A

useful fact to note, however, is that the cost of a minimum RST is at most = the cost of a


-----

###### (A) (B)

 Demand Point

Figure : Given the demand p oints, (B) shows the minimum cost Steiner tree of (A).

minimum spanning tree. Thus, in practice, an approximate minimum RST is computed by

rectilinearizing each edge of a minimum spanning tree (see Figure ).

Various metho ds for rectilinearizing edges in a MST exist. A layout which transforms

each diagonal edge using only one turn on the grid is called an L-RST. A layout which uses

two turns for each diagonal edge is called a Z-RST. A layout which uses an arbitrary numb er

of turns but never go es \away" from the destination is called an S-RST. These variants

are illustrated in Figure  . Notice that an optimal RST may have costs smaller than

the optimal S-RST, which may have cost smaller than the optimal Z-RST, which likewise

may have a cost smaller than the optimal L-RST. The fewer the restrictions, the b etter the

approximation to a minimum RST.

. Optimal S-RST for separable MSTs

If a MST of a given graph ob eys the separability prop erty, then there exists a metho d to

�nd an optimal S-RST from the MST. The separability prop erty states that any pair of non
adjacent edges must have non-overlapping b ounding rectangles (see Figure 0). Given such

a graph the approximate RST algorithm works as follows. First, it calculates the minimum

spanning tree of the given p oints. Then, the MST is hung by one of the leaves of the tree.

Then starting at the ro ot edge it recursively computes the optimal Z-layouts of the subtrees

ro oted at the children. Each combination of optimal Z-RSTs of the children is merged in

with the Z-layout of the ro ot no de. The least cost merged layout is the optimal Z-layout of

the entire tree. Pseudo co de for this algorithm is given in Figure 0 (D).

Note, the separability of the MST insures that the optimal S-RST has the same cost as

the optimal Z-RST. This algorithm runs in p olynomial time and provides an optimal S-RST,

but not necessarily an optimal RST!


-----

###### MST RST

Figure : A comparison of a rectilinear Steiner tree (RST) and minimum spanning tree

(MST) on a grid graph.

###### MST edge


###### L-RST


###### Z-RST


###### S-RST RST

Figure  : This illustrates the various transformations of an MST edge into rectilinear

edges.


-----

###### 3


###### edge 5


###### 4


###### 2


###### 1


###### 1


###### 3

|6|Col2|Col3|Col4|Col5|
|---|---|---|---|---|
||||||
||||||
||2||||


###### 5

 6 4

 (A) (B) (C)


function LeastCost(ze


,Te


)


// ze

// Te


a Z-layout for edge e

the subtree of edges hanging from e (including e)


// Returns the minimum cost Z-layout of edges in Te with the constraint that

// edge e is laid out using ze (all other edges are unconstrained).

b egin


if no children in Te

else


then return ze


for each child edge ei


of Te


for each Z-layout zij of ei

Lij = LeastCost(zij,Tei )

for each combination (Lx ; Ly


; : : :)


M


; Ly ; : : : merged with z


xy :::


= Layouts Lx


e


return minimum cost Mxy :::


end

(D)

Figure 0: (A) shows a separable MST, (B) shows the MST in (A) hung by leaf , (C)

shows a generic MST hung by one of its leaves up on which the LeastCost function op erates,

and (D) shows the co de for the LeastCost function.


-----

Algorithms in the Real World Notes by Noah Treuhaft

Lecture # (VLSI  & Pattern Matching ) �c   Noah Treuhaft and Guy Blello ch

� Integer Programming For Global Routing

{ Concurrent Layout

{ Hierarchical Layout

� Detailed Routing (Channel Routing)

{ Intro duction

{ Left Edge Algorithm (LEA)

{ Greedy

� Sequence Matching And Its Use In Computational Biology

{ DNA

{ Proteins

{ Human Genome Pro ject

{ Sequence Alignment

 Integer Programming For Global Routing

. Concurrent Layout

Concurrent layout optimizes all nets together rather than adding one net to the solution at a

time. The goal is to minimize total wire length, and it can b e met with an integer program.

Recall that a net is a set of terminals that must b e all connected to each other, and that

a netlist is a set of nets that need to b e routed. Supp ose that the netlist consists of n nets.


Let Ti


= fTi


; Ti


: : : T


ili g b e all the Steiner trees that connect net i (li


is the numb er of such


trees). The following integer program �nds and optimal route for our nets.


Pli

j =


ij ) � xij


minimize

sub ject to


P

n

i=

Pli

j =

P


xij


L(T


=  i = ;  : : : ; n


xij


� C (e) e  E


i;j :e(Tij


 if Tij


is used


where xij


=


L(Tij


0 otherwise

) = total length of tree Tij


C (e) = capacity restriction of edge e

E = set of all edges

It minimizes the total length of all included Steiner trees across all nets. The �rst constraint

ensures that only one tree p er net is included while the second ensures that the solution


-----

###### Trunks

 Upper boundary

 Tracks
 Dogleg
 Via

 Lower boundary

|Col1|Col2|Col3|Col4|Col5|Col6|Col7|Col8|Col9|Col10|Col11|Col12|
|---|---|---|---|---|---|---|---|---|---|---|---|
|||||||||||||
|ia||||||||Dogleg||||
|||||||||||||
|||||||||||||


###### Terminals


###### Branches


Figure : Channel routing de�nitions.

do es not exceed the capacity of any edge. Although this is a nice concise description of the

problem, it is infeasible to solve for any reasonably sized circuit. To make the problem more

feasible, a hierarchical application of the approach is used.

. Hierarchical Layout

In hierarchical layout, a �o orplan is prepro cessed by partitioning it into a hierarchy of sub
blo cks. At each no de of the resulting tree, the sub-blo cks can then b e routed with a mo di�ed

version of the concurrent routing program. The mo di�cation involves replacing the �rst

constraint with

Pli


where ni


j = xij = ni i = ;  : : : ; n

is the numb er of nets that connect the same set of blo cks. (In partitioning the


�o orplan, we create equivalence classes of nets. Since the algorithm actually routes these


equivalence classes, the ni


account for the fact that they may contain more than one net.)


The mo di�ed program is solved at each no de in the tree in top-down order.

The numb er of variables in b oth the concurrent and hierarchical programs can b e reduced

using various techniques; see chapter  of N. Sherwani, Algorithms for VLSI Physical Design

Automation, Kluwer,  .

 Detailed Routing (Channel Routing)

. Intro duction

A channel is the space b etween two standard-cell blo cks, and is used for routing wires b etween

the terminals of those and other blo cks. This typ e of routing is known as channel routing.

For channel routing, we know where wires enter the channel (at the terminals of the blo cks

that b ound the channel). The goal is to optimize the routing of wires within the channel to

allow the b est compaction of blo cks afterward. Figure  describ es some terminology for

channel routing.


-----

Switchb oxes are formed by the intersection of two channels. Routing algorithms for

switchb oxes are slightly di�erent from those for channels, but they have the same �avor.

Channel routing can b e grid-based or gridless. Grid-based routing requires that wires �t

on a regular grid. Gridless routing is more �exible in its wire placement. This �exibility

makes it useful for routing wires of di�erent thicknesses, which arise when the wires must

carry di�erent currents.

Semiconductor technology usually provides multiple wiring layers, and channel routing

algorithms must b e able to make use of these layers. Two typ es of mo del exist for the use

of multiple layers: reserved and unreserved. Reserved layer-mo dels restrict all wires within

a given layer to running in a single orientation (either horizontally or vertically), and are

commonly used for routing programmable logic arrays (PLA's). An unreserved layer-mo del,

in which wires can b e routed b oth horizontally and vertically within the same layer, is more

�exible.

There are four p opular two-layer routing algorithms.

� Left-edge algorithm (LEA) (Hashimoto and Stevens  )

� Constraint graph ( )

� Greedy (Rivest Fiduccia )

� Hierarchical ( )

LEA and Greedy are discussed b elow.

. Left Edge Algorithm (LEA)

The three steps of LEA are as follows.

. Determine the interval of each net. The interval of a net is simply the region b ounded

by its leftmost and rightmost terminals. (O(n))

. Sort these intervals by their leftmost p oints. (O(n log n))

. For each interval, �nd the �rst free track and place the interval on that track. Infor
mation ab out currently-o ccupied tracks can b e maintained in a balanced tree so that

inserting, deleting, and �nding the minimum take logarithmic time.

This algorithm e�ectively do es plane-sweeping, which app ears in computational geome
try. In plane-sweeping, elements are sorted in one of two dimensions, and then swept through

in the other. Figure  shows an example.

Simple LEA has two limitations.

� Each net must b e routed on a single track. This limits the quality of the resultant

routes.

� It cannot account for vertical constraints. This makes some nets imp ossible to route.

Various extensions (such as allowing doglegs) solve these problems.


-----

Figure : Example of the LEA channel routing algorithm. The left half show the intervals

that are routed in the right half.

Figure : Example of the greedy channel router.

. Greedy

Here is the greedy channel router algorithm. For each column i in order:

. Connect the terminals at column i either to the tracks containing their nets or to the

�rst empty tracks. Note that connecting b oth terminals to tracks containing their nets

might not b e p ossible, in which case one of the tracks must b e split. Splitting a track

involves simply using two tracks (and thus two parallel wires) for some part of a single

net.

. Join any tracks that were split during the previous iteration (i.e., that were split when

pro cessing the previous column).

. If any split tracks could not b e joined in the previous step, reduce the distance b etween

those tracks.

. Move each net toward the b oundary on which its next terminal lies.

Figure  shows an example of a greedily-routed channel.


-----

 Sequence Matching And Its Use In Computational

Biology

. DNA

DNA is a sequence of base-pairs (bps) of the four nucleotide bases|Adenosine, Cytosine,

Thymine, and Guanine (or a, c, t, and g). A human genome consists of DNA: approximately




and  � 0


 � 0




bps divided into  chromosomes, each with b etween  � 0


bps. Each


chromosome|b ecause it is DNA|is a sequence of bps, and is used to generate proteins:

transcription translation


DNA


�! mRNA


�! Protein


. Proteins

Proteins comprise 0 di�erent amino acids (gly, trp, cys, : : : ). Each bp triple in DNA co des

one of these amino acids. Since there are  p ossible triples, this is a many-to-one mapping.

(Four of triples serve to mark the b eginnings and ends of proteins rather than co ding amino

acids). The structure of a protein, as determined by its amino acids, controls how it folds,

which in turn determines its function. Protein folding|and therefore function|can b e

computed as an N-b o dy problem.

Goals in molecular biology are

. to extract genome sequences for various organisms,

. to determine the structure and purp ose of the proteins co ded by these sequences, and

. to use that knowledge to study and cure genetic diseases, design new drugs, and study

evolution.

. Human Genome Pro ject

The goal of the human genome pro ject is to generate a map of each human chromosome.

The basic approach is as follows.

. Divide chromosomes using restriction enzymes, which function as microscopic scalp els.

These enzymes break chromosomal DNA b etween di�erent bps.

. Clone the DNA fragments using host cells (usually bacteria).

. Find an exact map of a p ortion of the fragments (e.g., the �rst and last 00 bps). This

can b e done with a divide-and-conquer technique.

. Use sequence alignment to determine how the mapp ed fragments �t together.

. Find an exact map of the desired subset of the fragments.


-----

. Sequence Alignment

Sequence alignment answers this question: \How similar are two bp sequences?" It tries to

�nd the closest match, allowing for mutations (X ! Y ), insertions ( ! Y ), and deletions

(X ! ), but minimizing the numb er of these di�erences. For example,

acta_gtc__tac

| | ||| ||

_cgacgtcgata_

contains one mutation, three insertions, and two deletions. Notice that mutations can b e

mo deled as an insertion-deletion pair ( X ! Y ). Insertions and deletions are know collec
tively as indels.

There are three typ es of sequence alignment.

Global Aligns two sequences A and B, like the diff utility.

Lo cal Aligns A with any part of B (i.e., �nds the b est match or matches for A within B),

like the agrep utility.

Multiple Finds matches among n sequences (i.e., align them all up together).

For b oth global and lo cal alignment, we may want to �nd the n b est matches rather than

the single b est match.

Multiple alignment problems typically are NP-hard, so approximations are used.


-----

Algorithms in the Real World Notes by Felix Wu

Lecture #0 (Pattern Matching ) �c   Felix Wu and Guy Blello ch

� Longest Common Subsequence (LCS)

� Global sequence alignment

{ Recursive algorithm

{ Memoizing

{ Dynamic programming

{ Space e�ciency

� Gap mo dels

� Lo cal alignment

� Multiple alignment

� Biological applications

 Longest Common Subsequence

De�nition: A subsequence is any subset of the elements of a sequence that maintains the

same relative order. If A is a subsequence of B, this is denoted by A � B .

0


For example, if A = a


a


a


a





 is a subsequence of A since the

is not a subsequence of A since





a


, the sequence A

00


elements app ear in order, while the sequence A


= a a a

= a a a


the elements a


and a


are reversed.


The Longest Common Subsequence (LCS) of two sequences A and B is a sequence C

such that C � A, C � B, and jC j is maximized.

Example:

A = abacdac; B = cadcddc; C = acdc

_abacdac

| || |

cad_cddc

In this example, C is a LCS of A and B since it is a subsequence of b oth and there are

no subsequences of length .

Applications:

� The UNIX diff command works by �nding the LCS of two �les, where each line is

treated as a character. It then prints out lines which are not in the LCS, indicating

insertions, deletions, and changes.


-----

� For screens A and B, we can de�ne the edit distance of A and B, D (A; B ) = jAj +

jB j � jLC S (A; B )j. The edit distance gives the numb er of characters in either screen

which are not in the LCS, and hence measures the numb er of commands needed to

change the screen from A to B . Maximizing the LCS minimizes the edit distance.

 Global Sequence Alignment

The global sequence alignment problem is a generalization of LCS; instead of only noticing

whether characters are the same or di�erent, we have an arbitrary cost function which de�nes

the relationship b etween characters. (In what follows, we will b e maximizing \costs"; hence,

the cost function is really a measure of similarity.)

Let c(a; b) b e a cost function, giving a value for any pair a and b of alphab et symb ols,

including the blank character ( ). We can formally de�ne an alignment of A and B as a


0

pair of sequences A


and B


0


which are just A and B with added blanks, and for which


0

jA


j = jB


0

j = l . The value of an alignment is given by

l

X


0


c(A [i]; B


0


V (A ; B


0

) =


0

[i]):


i=

Our goal then is to �nd an optimal alignment, i.e. one whose value is a maximum.

Note that if we de�ne costs so that c(x; y ) =  if x = y, and 0 otherwise, we get LCS as

a sp ecial case.

Example:

A = abacdac, B = cadcddc


0

A

0

B


00

= _abacdac A


= cad_cddc B


= aba_cdac


| || | | || |

00


= _cadcddc


Both of these alignments have the same value when we use the LCS cost function, but for


00

the following cost function (which treats b's and c's as b eing similar), (A

value.

a b c d

a  0 0 0 0

b 0   0 0

c 0   0 0

d 0 0 0  0

0 0 0 0 -


; B


00

) has a higher


Notice the negative cost of two blanks. This is necessary to prevent unnecessary padding

of sequences with extra blanks.


-----

. Cost Functions for Protein Matching

With proteins, we have an alphab et of 0 amino acids, and hence a cost matrix with 0

entries. (We assume the matrix is symmetric, since we have no reason to order the proteins

we are comparing.) There are a numb er of p ossible cost functions:

� Identity: We could use the LCS cost function and view amino acids as just b eing the

same or di�erent.

� Genetic co de: We can assign costs which are inversely related to the minimum

numb er of DNA changes required to convert a DNA triple for one amino acid into a

DNA triple for the other.

� Chemical similarity: We can take into account the relative sizes, shap es, and charges

of di�erent amino acids.

� Exp erimental: We could use standard matrices (e.g. Dayhoft, Blosum) which are

based on observed prop erties of amino acids and/or their observed relative e�ect on

tertiary structure.

In practice the cost function of choice is application sp eci�c and a topic of hot debate.

 Sequence Alignment Algorithms

. Recursive Algorithm

A recursive solution to the sequence alignment problem takes the last character of each

sequence and tries all three p ossible alignments: either the characters are aligned together,

the �rst character is aligned with a blank, or the second character is aligned with a blank.

Taking the maximum over all three choices gives a solution. ML-style co de for this would

lo ok like the following:

OptAlgn(_,_) = C(_,_).

OptAlgn(_,A:a) = C(_,a) + OptAlgn(_,A).

OptAlgn(B:b,_) = C(b,_) + OptAlgn(B,_).

OptAlgn(B:b,A:a) = max(C(b,a) + OptAlgn(B,A),

C(b,_) + OptAlgn(B,A:a),

C(_,a) + OptAlgn(B:b,A)).

For the sp ecial case of LCS, all costs involving a blank are 0, and we know that it is

always to our advantage to align characters if they match. Hence, we get the following co de:

LCS(_,A:a) = 0.

LCS(B:b,_) = 0.

LCS(B:x,A:x) =  + LCS(B,A).

LCS(B:b,A:a) = max(LCS(B,A:a), LCS(B:b,A)).


-----

A naive implementation of this recursive solution has an exp onential running time, since

each call spawns three recursive calls over which we take the maximum. This is easily

recti�ed by memoizing, however.

. Memoizing

If jAj = n and jB j = m, note that there are only nm distinct calls we could make to OptAlgn.

By simply recording the results of these calls as we make them, we get an O (nm) algorithm.

The co de for LCS follows: (We assume the matrix M is initialized to INVALID.)

int LCS(int i, int j) {

if (M[i,j] != INVALID) return M[i,j];

if (i == 0 || j == 0) r = 0;

else if (A[i] == B[j]) r =  + LCS(i-, j-);

else r = max(LCS(i-, j), LCS(i, j-));

return M[i,j] = r;

}

. Dynamic Programming

Instead of �lling in the matrix of values as they are computed, we can �ll in the values row

by row. This is the dynamic programming solution, for which we have the following co de:

for i =  to n

for j =  to m

if (A[i] == B[j]) M[i,j] =  + M[i-,j-];

else M[i,j] = max(M[i-,j], M[i,j-]);

For example, with A = tcat and B = atcacac, we get the following matrix:

a t c a c a c

0 0 0 0 0 0 0 0

t 0 0      

c 0 0      

a 0       

t 0       

To actually �nd the optimal alignments, we can think of each entry as having edges to

the neighb oring entries from which it could have b een calculated. That is, each entry can

have edges p ointing to its upp er, left, and upp er left neighb ors, dep ending on whether it

could have b een calculated by adding one to its diagonal neighb or and whether its value is

the same as either its upp er or left neighb ors. A p ortion of the induced graph for the matrix

ab ove lo oks like:


-----

t c a c

t    

"                -                
c    

An optimal alignment is then a path from the lower right corner of the table to the upp er

left. In the matrix fragment ab ove, the two paths corresp ond to aligning the tc as tc or

as t c. Finding all p ossible paths gives us all optimal alignments. As with memoizing, this

algorithm runs in O (nm) time.

. Space E�ciency




Our time b ound is essentially the b est p ossible for the general case


, but we would like to use


less space. In particular, notice that each row of the matrix dep ends only on the previous

row. Hence, by �lling in the matrix row-by-row and reusing the space for each row, we could

compute the value of the optimal alignment using just O (m) space. Without something

clever, however, this do es not give us an actual alignment since we throw away the path as

we go (rememb er that we have to traverse backwards through the matrix to generate the

alignment path).

(As an aside, note that if we were to run this algorithm in parallel, we would want to �ll

in the matrix diagonal by diagonal so that each entry would b e indep endent of the others

currently b eing worked on.)

In order to actually generate an alignment using only O (m) space, we use the following

divide-and-conquer algorithm:

. Calculate the entries of the matrix row-by-row, discarding intermediate results, until

we reach the middle row.

. Once we get to the middle row as we calculate each additional row, we keep track

of where in the middle row each new entry came from. (This is easily derived from

the corresp onding information ab out the previous row.) If we have more than one

p ossibility, we cho ose arbitrarily. (Hence, this algorithm will only output one solution.)

. When we reach the last row, we will know which entry in the middle row the b ottom

right corner came from (i.e. we will know the middle no de along the solution path).

Supp ose that middle row entry is entry k . Now we recursively solve the problem of

�nding the path from the b ottom right to (n=; k ) and from (n=; k ) to the upp er left.

It may seem that this algorithm is doing redundant work since it recursively resolves the

same solution over and over again. Although this is indeed true note, however, that in the

recursion the algorithm only needs to recur on the upp er left and b ottom right quadrants.

Hence, it is doing half as much work at each level of the recursion, leading to a constant

factor increase in time, not a log factor as one might supp ose. More formally, the recurrence

we get is:

T (n; m) = T (n=; k ) + T (n=; m � k ) + O (nm) = O (nm):



We will describ e a more e�cient metho d for small edit-distances in the next class.


-----

Since we only keep track of an extra set of p ointers one p er column, this algorithm uses

only O (m) space. (A slight optimization is to orient our matrix so that m is the smaller of

the two dimensions.) The algorithm was invented in the context of �nding the longest com
mon subsequence by Hirschb erg (\A linear-space algorithm for computing maximal common

subsequences", Communications of the ACM, :0{,  ) and generalized to align
ment by Myers and Miller (\Optimal alignments in linear space", Computer Applications in

the Biosciences, :{,  ).

 Gap Mo dels

For many applications, consecutive indels (insertions or deletions, also called gaps) really

need to b e treated as a unit. In other words, a gap of  characters isn't really twice as bad

as a gap of  character. There are various ways of dealing with this problem, dep ending on

what sort of gap mo del we want to allow.


In the most general case, we can de�ne arbitrary costs xk

we have the Waterman-Smith-Beyer algorithm:


for gaps of length k . For this


S00 = 0

Si0 = xi

S0j = xj

Sij = max





<

>:


maxk

maxk


Si�;j �


+ C (ai


)


(ai ; bj

+ xk )

+ xk )


(Si;j �k

(Si�k ;j


This is similar to our previous algorithms, except that for each entry, instead of only

lo oking at gaps of length , which corresp onds to lo oking at the left and upp er neighb ors in


the matrix, we lo ok at all p ossible gap lengths. To calculate Sij


this requires us to lo ok at


the entire row i and column j generated so far. Hence, the running time of the algorithm is







+ n m). Furthermore, since we need all previous rows, we cannot make this algorithm


O (nm


space e�cient.

In practice, our gap mo dels are likely to b e relatively simple, and for these simpler mo dels,

we can again achieve the time/space b ounds we were able to get b efore. For example, with


an a�ne gap mo del, we have xk


= � + � k . (This is p opular in computational biology, where


something like xk


= �( + k =) is typical.) An algorithm due to Gotoh for the a�ne gap


mo del is as follows:


Ei�;j + �

Si�;j + � + �

Fi;j � + �

Si;j � + � + �

Si�;j � + C (ai

Eij

Fij


Eij

Fij

Sij


(

= max

(

= max



><

= max

  
:


E0j = �

Fi0 = �


S0j

Si0


; bj


)


i


= � + � j

= � + � i


The Eij


matrix calculates optimal alignments in which the second sequence ends in


blanks, the F


matrix calculates optimal alignments in which the �rst sequence ends in


ij


-----

blanks, and the Sij


matrix calculates overall optimal alignments. The basic idea is that


since each additional blank (after the �rst one) has the same cost, we can essentially use the

same algorithm as b efore, just using the E and F values to b e sure we add in � when we

intro duce the �rst blank in a gap. This algorithm runs in O (nm) time and can b e made

space e�cient as b efore.

The following is a summary of some di�erent gap mo dels and the running times of their

asso ciated algorithms.

Gap function form Running time




General O (nm




+ n


m)


Linear (xk


= � + � k ) O (nm)


Logarithmic (xk


= � + � log k ) O (nm)


Concave downwards O (nm log n)

Piecewise linear, l segments O (l nm)

 Lo cal Alignment

Sometimes instead of aligning two entire sequences, we want to align a smaller sequence at

multiple lo cations within a larger one. For example, to �nd areas of DNA which might have

similar functionality to some segment, we can �nd the b est matches to our segment within

the DNA.

Global alignment algorithms are easily converted into lo cal ones by simply adding an

extra argument 0 to the max function computing the optimal alignment. So, for example,

for the general gap mo del




+ C (ai


)


Si�;j �


maxk

maxk

0


(ai ; bj

+ xk )

+ xk )


(Si;j �k

(Si�k ;j


Sij


= max



>>

<


>>

:


This has the e�ect of not p enalizing an alignment for the large gaps at the ends of the

sequence. For example, with

(

 if a = b

C (a; b) =

�= if a = b


and xk


= �( + k =), we get the following alignment matrix.

a t c a c a c

0 0 0 0 0 0 0 0

t 0 0  0 0 0 0 0

c 0 0 0  /  0 

a 0  0 /  /  /

t 0 0  / / / / /


-----

In this case, the b est match aligns tca with tca (the one  in the matrix). In general,

we might want to �nd multiple matches with high scores. In this case we might pick out the

highest k entries from the matrix, although we probably don't want to include entries that

are just extensions of previous matches we have found. In the ab ove example we might not

want to pick the value / that follows , but instead pick the .

 Multiple Alignment

Another problem is to align multiple sequences at once so as to maximize the numb er of pairs

of aligned symb ols. This is used to reconstruct a sequence from its overlapping fragments; the

overlaps will not b e p erfect b ecause of imprecision in the sequencing of the fragments. Alter
natively, we can also use multiple alignment with sequences from di�erent family memb ers,

in order to �nd genes shared by the family memb ers.

Unfortunately, multiple alignment is NP-hard. Hence, there are two typ es of algorithms:

those that take exp onential time and those that are approximate. In exp onential time, we

can extend our earlier dynamic programming algorithms to work in a p-dimensional matrix,

p


where p is the numb er of sequences we are trying to align. This takes O (n

and is impractical for p more than ab out .


) time and space


Alternatively, we can extend the pairwise metho ds hierarchically to get an approximate

solution. For this, we do all pairwise comparisons, cluster the results, and then build an

alignment b ottom-up from the cluster tree.

 Biological Applications

One of the most intensive uses of pattern matching is in database search engines used by

biologists to compare new sequences with databases of old ones. These databases can have

as many as 00,000s of sequences with querying by web or email. Such shared search engines

are useful b ecause algorithms and data are up dated more rapidly and more centrally, and

considerable computing p ower can b e brought to b ear on the problem. Both lo cal and global

alignment algorithms are used.

On a smaller scale, pattern matching is also used for genome sequencing. This can b e done

in one of two ways. The �rst metho d involves sequencing the 00 bp (base pair) ends of the

fragments of a sequence, which are then assembled using multiple alignment. Alternatively,

one piece can b e fully sequenced, and the rest of the sequence can b e constructed outward

using single alignment.


-----

Algorithms in the Real World Notes by Helen J. Wang

Lecture # (Indexing and Searching ) �c   Helen J. Wang and Guy Blello ch

� Pattern Matching (continued)

. Ukkonen's Algorithm for more e�cient dynamic programming

� Intro duction to Indexing and Searching

� Inverted �le indexing

. Compressing the p osting lists

. Representing and accessing the lexicon

 Pattern Matching (continued)

So far we have discussed algorithms that take at least O (nm) time for two sequences of

length n and m. In an application such as diff this can b e prohibitively exp ensive. If we

0


had two �les of 00; 000 lines each, the algorithm would require 0


string compares, which


would take hours. However, diff can actually run much faster than this when the �les to

b e compared are similar (i.e., the typical situation in which they b oth come from the same

source and just involve minor changes).

We will now consider an algorithm for edit-distance which takes O (min(n; m)D ) time,

where D is the edit distance b etween the two strings. The runtime is therefore output

dep endent. This algorithm can also b e used for the longest common subsequence and a

variant is used in the diff program.

. Ukkonen's Algorithm

Consider the minimum edit distance problem:


Di0

D0j

Dij


= i

= j

(

=


Di�;j �

 + min(D


i;j � ; D


ai


= bi


()


i�;j ) otherwise


This problem can b e viewed as a weighted directed graph laid over the n � m matrix of


Di;j . It can then b e solved by �nding a shortest path in the graph from D


0;0


to D


. This


n;m


graph has a unit weight edge b etween neighb ors in the same row or column. These edges


represent an insertion or deletion|the  + min(Di;j �


; Di�;j ) case in Equation . The graph


also has zero weight diagonal edges from Di�;j �


to D


= bi


|representing the


i;j


whenever ai


ai


= bi


case in Equation . Figure (a) shows an example of such a graph. In this graph


-----

the length of a path represents the cost of those set of mo di�cations. Therefore the shortest


path from D


gives the set of changes for the minimum edit distance. Note that we


0;0


to Dn;m


don't actually have to construct the graph since we can determine the edges from a lo cation


i; j simply by lo oking at ai


; ai+


; b


j


and bj + .


###### _ a t c a


###### _

 t

 a

 t

 a


###### _ a t c a
 1 1 1 1

 0

 1

 0 0
 1

 1 1

 0 0

 1 1 1 1


###### 2 7


###### 1

 1


###### _

 t

 a

 t

 a


###### 2 9


(a) Graph (b) Shortest Path

Figure : Graph representation of the minimum edit distance problem for the strings atca

and tata. In the right �gure the circled values sp ecify the distances and the uncircled values

sp ecify the visiting order for Dijkstra's algorithm. The shaded path represents the shortest

path.

To �nd the shortest path we can use a standard algorithm such as Dijkstra's algorithm

(Figure (b) gives an example). Since all the fringe no des in the algorithm will have one

of two priorities (the distance to the current vertex, or one more) the algorithm can b e

optimized to run in constant time for each visited vertex. If we searched the whole graph

the running time would therefore b e O (nm), which is the same as our previous algorithms

for edit distance. As we will show, however, we can get much b etter b ounds on the numb er

of vertices visited when the edit distance is small.


Theorem  Dij


� jj � ij


Proof: All edges in the graph have weight � 0 and all horizontal and vertical edges have

weight . Since jj � ij is the minimum distance in edges from the diagonal, and the path

starts on the diagonal (at 0,0), any path to lo cation (i; j ) must cross at least jj � ij horizontal

and vertical edges. The weight of the path must therefore b e at least jj � ij. 


Given that Dijkstra's algorithm visits vertices in the order of their distance D

theorem implies that the algorithm will only search vertices that are within Dnm

diagonal (see Figure ). This leads to a running time of


ij, this

of the


-----

T = O (Dnm


min(n; m))


###### Dnm

Figure : Bounding visited vertices

In practice programs such as diff do not use Dijkstra's algorithm but instead they use

a metho d in which they try increasingly large bands around the diagonal of the matrix (see

Figure ). On each iteration the width of the band is doubled and the algorithm only �lls


in the entries in the band. This is continued while Dnm


- w = where w is the width of the


band. The co de for �lling each band is a simple nested lo op.

The technique can b e used in conjunction with our previous divide-and-conquer algorithm

to generate a space-e�cient version.

 Intro duction to Indexing and Searching

Indexing addresses the issue of how information from a collection of do cuments should b e

organized so that queries can b e resolved e�ciently and relevant p ortions of the data ex
tracted quickly. We will cover a variety of indexing metho ds. To b e as general as p ossible,

a document col lection or document database can b e treated as a set of separate do cuments,

each describ ed by a set of representative terms, or simply terms (each term might have addi
tional information, such as its lo cation within the do cument). An index must b e capable of

identifying all do cuments that contain combinations of sp eci�ed terms, or that are in some

other way judged to b e relevant to the set of query terms. The pro cess of identifying the

do cuments based on the terms is called a search or query of the index. Figure  illustrates

the de�nitions.


-----

|w|Col2|
|---|---|
|||


###### w = 15


###### w = 31


Figure : Using increasingly wide bands.

Applications of indexing:

Indexing has b een used for many years in a wide variety of applications. It has gained

particular recent interest in the area of web searching (e.g. AltaVista, Hotb ot, Lycos, Excite,

...). Some applications include

� Web searches

� Library article and catalog searches

� Law, patent searches

� Information �ltering, e.g. get interesting New York Time articles.

The goals of these applications:

� Sp eed { want minimal information retrieval latency

� Space { storing the do cument and indexing information with minimal space

� Accuracy { returns the \right" set of do cuments

� Up dates { ability to mo dify index on the �y (only required by some applications)


-----

###### Index Query

 "Document List"

Figure : Overview of Indexing and Searching

The main approaches:

� Full text scanning (e.g. grep, egrep)

� Inverted �le indexing (most web search engines)

� Signature �les

� Vector space mo del

Typ es of queries:

� b o olean (and, or, not)

� proximity (adjacent, within)

� key word set

� in relation to other do cuments (relevance feedback)

Allowing for:

� pre�x matches (AltaVista do es this)

� wildcards

� edit distance b ounds (egrep)


-----

Techniques used across metho ds

� case folding: London = london

� stemming: compress = compression = compressed

(several o�-the-shelf English language stemmers are available)

� ignore stop words: to, the, it, be, or, ...

Problems arise when search on To be or not to be or the month of May

� Thesaurus: fast = rapid

(handbuilt clustering)

Granularity of Index

The Granularity of the index refers to the resolution to which term lo cations are recorded

within each do cument. This might b e at the do cument level, at the sentence level or exact

lo cations. For proximity searches, the index must know exact (or near exact) lo cations.

 Inverted File Indexing

Inverted �le indices are probably the most common metho d used for indexing do cuments.

Figure  shows the structure of an inverted �le index. It consists �rst of a lexicon with one

entry for every term that app ears in any do cument. We will discuss later how the lexicon can

b e organized. For each item in the lexicon the inverted �le index has an inverted �le entry

(or posting list) that stores a list of p ointers (also called postings) to all o ccurrences of the

term in the main text. Thus to �nd the do cuments with a given term we need only lo ok for

the term in the lexicon and then grab its p osting list. Bo olean queries involving more than

one term can b e answered by taking the intersection (conjunction) or union (disjunction) of

the corresp onding p osting lists.

We will consider the following imp ortant issues in implementing inverted �le indices.

� How to minimize the space taken by the p osting lists.

� How to access the lexicon e�ciently and allow for pre�x and wildcard queries.

� How to take the union and intersection of p osting lists e�ciently.

. Inverted File Compression

The total size of the p osting lists can b e as large as the do cument data itself. In fact, if the

granularity of the p osting lists is such that each p ointer p oints to the exact lo cation of the

term in the do cument, then we can in e�ect recreate the original do cuments from the lexicon

and p osting lists (i.e., it contains the same information). By compressing the p osting lists

we can b oth reduce the total storage required by the index, and at the same time p otentially

reduce access time since fewer disk accesses will b e required and/or the compressed lists can


-----

|Aard Zulu|Col2|
|---|---|
|Aard||
|||
|Zulu||


###### Lexicon Posting lists


###### Document File


Figure : Structure of Inverted Index

�t in faster memory. This has to b e balanced with the fact that any compression of the

lists is going to require on-the-�y uncompression, which might increase access times. In this

section we discuss compression techniques which are quite cheap to uncompress on-the-�y.

The key to compression is the observation that each p osting list is an ascending sequence

of integers (assume each do cument is indexed by an integer). The list can therefore b e

represented by a initial p osition followed by a list of gaps or deltas b etween adjacent lo cations.

For example:

original p osting list: elephant: [, , 0, , , , , ]

p osting list with deltas: elephant: [, , , , , , , ]

The advantage of using the deltas is that they can usually b e compressed much b etter

than indices themselves since their entropy is lower. To implement the compression on

the deltas we need some mo del describing the probabilities of the deltas. Based on these

probabilities we can use a standard Hu�man or Arithmetic co ding to co de the deltas in each

p osting list. Mo dels for the probabilities can b e divided into global or lo cal mo dels (whether

the same probabilities are given to all lists or not) and into �xed or dynamic (whether the

probabilities are �xed indep endent of the data or whether they change based on the data).

An example of a �xed mo del is the � co de. Think of a co de in terms of the implied

�l(c)


probability distribution P (c) = 


. This is the inverse of the de�nition of entropy. For


-----

Table : � co ding for  through 

example, binary co de gives a uniform distribution since all co des are the same length, while

the unary co des ( = 0;  = 0;  = 0;  = 0; : : : ) gives an exp onential decay distribution

(p() = =; p() = =; p() = =; p() = =; : : : ). The � co de is in b etween these two


extreme probability distributions. It represents the integer i as a unary co de for  + b(log


(i))c


blog (i)c




. The unary part sp eci�es the lo cation of the most


followed by the binary co de for i � 


signi�cant non-zero bit of i, and then the binary part co des the remaining less signi�cant

bits. Figure  illustrates viewing the � co des as a pre�x tree, and Table  shows the

co des for -. The length of the � co des is


li

The implied probabilities are therefore


=  +  log (i)


�l(i)

P [i] = 


+ log(i)

= 


=






i


This gives a reasonable mo del of the deltas in p osting lists and for the TREC database

(discussed in the next class) gives a factor of  compression compared with binary co des (see

Table ). By adjusting the co de based on the length of the p osting list (i.e. using a lo cal

metho d), the compression can b e improved slightly. An example is the Bernoulli distribution

(see Table ).

In dynamic metho ds the probabilities are based on statistics from the actual deltas rather

than on a �xed mo del such as the � co de. As with the static mo dels, these metho ds can

either b e global or lo cal. For a global metho d we simply measure the probability of every

delta and co de based on these probabilities. For lo cal metho ds we could separately measure

the probabilities for each p osting list, but this would take to o much space to store the

probabilities (we would have to store separate probabilities for every list). A solution is to

batch the p osting lists into groups based on their length. In particular create one batch for

each integer value of blog (l eng th)c. In this way we only have log (n) sets of probabilities,

where n is the length of the longest p osting list. Results comparing the metho ds are shown

in Table  (from Managing Gigabytes, by Witten, Mo�at, and Bell, Van Nostrand Reinhold,

 ).


-----

###### 4 5 7 6

Figure  : � co de


###### 8--15


Table : Compression of p osting �les for the TREC database using various techniques in

terms of average numb er of bits p er p ointer.

. Representing and Accessing Lexicons

There are many ways to store the lexicon. Here we list some of them

� Sorted { just store the terms one after the other in a sorted array

� Tries { store terms as a trie data structure

� B-trees { well suited for disk storage

� Perfect hashing { assuming lexicon is �xed, a p erfect hash can b e calculated

� Front-co ding { stores terms sorted but do es not rep eat front part of terms (see Ta
ble ). Requires much less space than a simple sorted array.


-----

, jezeb el , , eb el 0, , jezeb el

, jezer , l, r , l, r

, jezerit , , it , , it

, jeziah , , iah , , iah

, jeziel , , el 0, , jeziel

, jezliah , , liah , , liah

, jezoar , , oar , , oar

, jezrahiah , , rahiah , , rahiah

, jezreel , , eel 0, , jezreel

,jezreelites , , ites , , ites

, jibsam , , ibsam , , ibsam

, jidlaph , , dlaph , , dlaph

Table : Front co ding (the term b efore jezeb el was jezaniah). The pair of numb ers represent

where a change starts and the numb er of new letters. In the -in- co ding every th term is

co ded completely making it easier to search for terms.

Numb er Term

 abhor

 b ear

 laab er

 lab or

 lab orator

 lab our

 lavacab er

 slab

Table : Basic terms

When cho osing among the metho ds one needs to consider b oth the space taken by the

data structure and the access time. Another consideration is whether the structure allows for

easy pre�x queries (e.g., all terms that start with wux). Of the ab ove metho ds all except for

p erfect hashing allow for easy pre�x searching since terms with the same pre�x will app ear

adjacently in the structure.

Wildcard queries (e.g., w*x) can b e handled in two ways. One way is to use n-grams,

by which fragments of the terms are indexed (adding a level of indirection) as shown in

Table  for the terms listed in Table . Another way is to use a rotated lexicon as shown

in Table .


-----

Table : N-Gram


-----

Table : Rotated lexicon


-----

Algorithms in the Real World Notes by Ben Horowitz

Lecture # (Indexing and Searching ) �c   Ben Horowitz and Guy Blello ch

� Evaluating information retrieval e�ectiveness

� Signature �les

{ Generating signatures

{ Accessing signatures

{ Query logic on signature �les

{ Cho osing signature width

{ An example: TREC

� Vector space mo dels

{ Selecting weights

{ Similarity measures

{ A simple example

{ Implementation

{ Relevance feedback

{ Clustering

� Latent semantic indexing (LSI)

{ Singular value decomp osition (SVD)

{ Using SVD for LSI

{ An example of LSI

{ Applications of LSI

{ Performance of LSI on TREC

 Evaluating information retrieval e�ectiveness

Two measures are commonly used to evaluate the e�ectiveness of information retrieval meth
o ds: precision and recal l. The precision of a retrieval metho d is the fraction of the do cuments

retrieved that are relevant to the query:

numb er retrieved that are relevant

precision =

total numb er retrieved

The recal l of a retrieval metho d is the fraction of relevant do cuments that were retrieved:

numb er relevant that are retrieved

recall =

total numb er relevant


-----

 Signature �les

Signature �les are an alternative to inverted �le indexing. The main advantage of signature

�les is that they don't require that a lexicon b e kept in memory during query pro cessing. In

fact they do not require a lexicon at all. If the vo cabulary of the stored do cuments is rich,

then the amount of space o ccupied by a lexicon may b e a substantial fraction of the amount

of space �lled by the do cuments themselves.

Signature �les are a probabilistic metho d for indexing do cuments. Each term in a do c
ument is assigned a random signature, which is a bit vector. These assignments are made

by hashing. The descriptor of do cument is the bitwise logical OR of the signatures of its

terms. As we will see, queries to signature �les sometimes resp ond that a term is present in

a do cument when in fact the term is absent. Such false matches necessitate a three-valued

query logic.

There are three main issues to discuss: () generating signatures, () searching on signa
tures, and () query logic on signature �les.

. Generating signatures

The width W of each of the signatures, is the numb er of bits in each term's signature. Out of

these bits some typically small subset of them are set to  and the rest are set to zero. The

parameter b sp eci�es how many are set to . Typically, ,000 � W � 0,000 . (Managing

Gigabytes seems to suggest that typically  � b � 0.) The probability of false matches may

b e kept arbitrarily low by making W large, at the exp ense of increasing the lengths of the

signature �les.

To generate the signature of a term, we use b hash functions as follows

for i =  to b


signature[hashi


(term) % w ] = 


In practice we just have one hash function, but use i as an additional parameter.

To generate the signature of a do cument we just take the logical or of the term signatures.

As an example, consider the list of terms from the nursery rhyme \Pease Porridge Hot" and

corresp onding signatures:


-----

p ot 0000 000 00 0000

some 000 000 0000 000

the 00 000 0000 0000

Note that a term may get hashed to the same lo cation by two hash functions. In our example,

the signature for hot has only two bits set as a result of such a collision. If the do cuments

are the lines of the rhyme, then the do cument descriptors will b e:

Do cument Text Descriptor

 Pease p orridge hot, p ease p orridge cold, 00  000 00

 Pease p orridge in the p ot, 0  00 000

 Nine days old. 00 00 000 00

 Some like it hot, some like it cold, 00 0 00 0

 Some like it in the p ot, 0  0 00

 Nine days old. 00 00 000 00

. Searching on Signatures

To check whether a term T o ccurs in a do cument, check whether all the bits which are set

in T 's signature are also set in the do cument's descriptor. If not, T do es not app ear in the

do cument. If so, T probably o ccurs in the do cument; b ecause some combination of other

term signatures might have set these bits in T 's descriptor, it cannot b e said with certainty

whether or not T app ears in the do cument. For example, since the next-to-last bit in the

signature for it is set, it can only o ccur in the fourth and �fth do cuments, and indeed it

o ccurs in b oth. The term the can o ccur in do cuments two, three, �ve, and six; but in fact,

it o ccurs only in the second and �fth.

The question remains of how we e�ciently check which do cuments match the signature

of the term (include all its bits). Consider the following (naive) pro cedure: to �nd the

descriptor strings for which the bits in a given signature are set, pull out all descriptors, and

for each descriptor, check whether the appropriate bits are set for each descriptor. When the

descriptors are long and there are many �les, this approach will involve many disk accesses,

and will therefore b e to o exp ensive.


-----

A substantially more e�cient metho d is to access columns of the signature �le, rather than

rows. This technique is called bit-slicing. The signature �le is stored on disk in transp osed

form. That is, the signature �le is stored in column-ma jor order; in the naive approach, the

signature �le was stored in row-ma jor order. To pro cess a query for a single term, only b

columns need to b e read from disk; in the naive approach, the entire signature �le needed

to b e read. The bitwise and of these b columns yields the do cuments in which the term

probably o ccurs. For example, to check for the presence of porridge, take the and of columns

T


two, six, and eleven, to obtain [00]


. (This query returned two false matches.)


. Query logic on signature �les

We have seen that collisions b etween term signatures can cause a word to seem present in a

do cument when in fact the word is absent; on the other hand, words that seem absent are

absent. If, for example, pease is absent from a do cument D, then the answer to \Is pease is

D ?" is No; if pease seems to b e present, then the answer is Mayb e.

For queries with negated terms (for example, \Is pease absent from do cument d?") the

situation is reversed. For example, since pease has bits six, eight, and  set, it cannot

o ccur in do cuments three, four, or six, so for these do cuments the appropriate answer is Yes.

However, the other do cuments might contain pease, so for these do cuments the appropriate

answer is Mayb e.

More generally, queries in signature �les need to b e evaluated in three-valued logic.

Atomic queries (e.g. \Is nine present?") have two resp onses, No and Mayb e. More complex

queries | queries built from atomic queries using not, and, and or | get evaluated using

the following rules:

not and n m y or n m y

n y n n n n n n m y

m m m n m m m m m y

y n y n m y y y y y

Consider, for example, the evaluation of \(some or not hot) and p ease":

Do c. s h p not h s or not h (s or not h) and p

 m m m m m m

 m m m m m m

 n n n y y n

 m m n m m n

 m m m m m m

 n n n y y n

. Cho osing signature width

How should W b e chosen so that the exp ected numb er of false matches is less than or equal

to some numb er z ? It turns out that W should b e set to



( )

=B

 � ( � p)


-----

where

p, the probability that an arbitrary bit in a do cument descriptor is set, is given


=b

;


by


z

N


B, the total numb er of bits set in the signature of an average do cument, is given

f b


by


�


;


N


q


N is the numb er of do cuments;

f is the numb er of (document, term) pairs;

b is the numb er of bits p er query; and

q is the numb er of terms in each query.

The analysis used to derive ( ) can b e found in Witten, Mo�at, and Bell, Managing Giga
bytes, chapter , Section .. One assumption made in this analysis is that all do cuments

contain roughly the same numb er of distinct terms. Clearly, this assumption do es not always

hold.

. An example: TREC

As an example, consider the TREC (Text REtrieval Conference) database. The TREC

database, which is used to b enchmark information retrieval exp eriments, is comp osed of

roughly ,000,000 do cuments | more than Gbytes of ASCI I text | drawn from a variety

of sources: newspap ers, journal abstracts, U.S. patents, and so on. (These �gures were true

of TREC in  . It has probably grown in size since then.) In this example, we assume that

TREC contains a mere 0,000 do cuments, with  Million do cument-term pairs totaling

more than Gbytes of text.

Consider making queries on a single term and assume we want at no more than  false




match. We assume b = . To calculate W by equation ( ) we have, f =  � 0




; N =


: � 0


; z = ; q = , which gives:

p =

B =


�



: � 0



 � 0



: � 0


�


�=






= :


= 0





W = 00

Thus, the total space o ccupied by the signature �le is (; 00=) � 0Kbytes = Mbytes

(ab out / of the space required by the do cuments themselves). For b = , a query on a

term will read  slices of 0Kbits, which is 0Kbytes (ab out .% of the total database).

 Vector space mo dels

Bo olean queries are useful for detecting b o olean combinations of the presence and absence

of terms in do cuments. However, Bo olean queries never yield more information than a Yes

or No answer. In contrast, vector space mo dels allow search engines to quantify the degree of

similarity b etween a query and a set of do cuments. The uses of vector space mo dels include:


-----

Ranked keyword searches, in which the search engine generates a list of do cuments

which are ranked according to their relevance to a query.

Relevance feedback, where the user sp eci�es a query, the search engine returns a set of

do cuments; the user then tells the search engine which do cuments among the set are

relevant, and the search engine returns a new set of do cuments. This pro cess continues

until the user is satis�ed.

Semantic indexing, in which search engines are able to return a set of do cuments whose

\meaning" is similar to the meanings of terms in a user's query.

In vector space mo dels, do cuments are treated as vectors in which each term is a separate

dimension. Queries are also mo deled as vectors, typically 0- vectors. Vector space mo dels

are often used in conjunction with clustering to accelerate searches; see Section (.) b elow.

. Selecting weights

In vector space mo dels, do cuments are mo deled by vectors, with separate entries for each

distinct term in the lexicon. But how are the entries in these vectors obtained? One approach

would b e to let the entry wd;t, the weight of term t in do cument d, b e  if t o ccurs in d and

0 otherwise. This approach, however, do es not distinguish b etween a do cument containing

one o ccurrence of elephant and a do cument containing �fty o ccurrences of elephant. A b etter


approach would b e to let wd;t


b e fd;t, the numb er of times t o ccurs in do cument d. However,


it seems that �ve o ccurrences of a word shouldn't lead to a weight that is �ve times as heavy,

and that the �rst o ccurrence of a term should count for more than subsequent o ccurrences.

Thus, the following rule for setting weights is often used: set wd;t to log  ( + fd;t ). Under

this rule, an order of magnitude increase in frequency leads to a constant increase in weight.


These heuristics for setting fd;t


all fail to take account of the \information content" of


a term. If supernova app ears less frequently than star, then intuitively supernova conveys


more information. Borrowing from information theory, we say that the weight wt


of a term


in a set of do cuments is log  (N =ft ), where N is the numb er of do cuments and ft is the

numb er of do cuments in which the term app ears.

One way to represent the weight of a term t in do cument d is by combining these ideas:


in a set of do cuments is log


(N =f


wd;t


( + fd;t


= log


(N =ft ) log


)








It should b e emphasized that this rule for setting wd;t

. Similarity measures


is one among many prop osed heuristics.


To score a do cument according to its relevance to a query, we need a way to measure the


similarity b etween a query vector vq


and a do cument vector vd


. One similarity measure is


inverse Euclidean distance, =kvq


� vd k. This measure discriminates against longer do cu

ments, since vd


which are distant from the origin are likely to b e farther away from typical


vq


. Another is the dot pro duct v


q


� vd . This second measure unfairly favors longer do cu

ments. For example, if v


= v


. One solution to the problems with


� vd


= vq


� vd


d


d


, then vq





-----

b oth these measures is to normalize the lengths of the vectors in the dot pro duct, thereby

obtaining the following similarity measure:


wq


� vd


kvq kkvd


k


This similarity measure is called the cosine measure, since if � is the angle b etween vectors

~x and ~y, then cos � = ~x � ~y =(k~xkk~y k).

. A simple example

Supp ose we have the set of do cuments listed in the following table. These do cuments give rise


to the frequency matrix [fd;t

in the table:


], frequencies ft


of terms, and informational contents log


(N =ft


)





 apple ballo on ballo on elephant apple apple   0 0 

 cho colate ballo on ballo on cho colate apple cho colate duck     0

 ballo on ballo on ballo on ballo on elephant ballo on 0  0 0 

 cho colate ballo on elephant 0   0 

 ballo on apple cho colate ballo on    0 0

 elephant elephant elephant cho colate elephant 0 0  0 


log


(N =ft


) .00 0. 0. . 0.


For simplicity, supp ose w


the weight matrix [wd;t


wd;t is calculated according to the rule wd;t = fd;t � log  (N =ft ). Then

] would b e as follows (the norms of each row of the weight matrix are

a b c d e kvd k

  . 0 0 . .0

  . . . 0 .

 0 . 0 0 . .

 0 . . 0 . 0.

  . . 0 0 .


underneath kvd


k):


Then, for the queries listed b elow, the cosine measure gives the following similarities:

Do c. no. Query

d c c, d a, b, e a, b, c, d, e

kvq k = : kvq k = 0: kvq k = : kvq k = : kvq k = : 0

 0.00 0.00 0.00 0.  0.

 0. 0. 0. 0. 0. 

 0.00 0.00 0.00 0.0 0.

 0.00 0. 0. 0.0 0.0

 0.00 0. 0.0 0. 0.0

 0.00 0. 0.0 0. 0.

Note that in the second query, the fourth do cument b eats the second b ecause the fourth is

shorter overall. For each of the other queries, there is a single do cument with a very high

similarity to the query.


-----

. Implementation of cosine measures using inverted lists

Directly computing the dot pro duct of a query vector and all do cument vector s is to o

exp ensive, given the fact that b oth vectors are likely to b e sparse. A more economical

alternative is to keep (do cument, weight) pairs in the p osting lists, so that a typical inverted

�le entry would lo ok like


ht; [(dt; ; wd


; wdt;


; wdt;m


;t


)]i:


;t


); (dt;


;t


); : : : ; (dt;m


t;


Here, t is a term, dt;i


is a p ointer to the ith do cument containing term t, and wdt;i


;t


is weight


of t in do cument dt;i


. (Heuristics for calculating w


d;t


were given in Section ..) For example,


the inverted �le entry for apple might b e

happle; [(; ); (; ); ( ; )]i:

Fortunately, the weights wdt;i ;t can typically b e compressed at least as well as the distances

dt;i+ � dt;i in the inverted �le entry.


These p osting lists help quicken the search for the do cuments which are most similar to

a query vector. In the following algorithm Q is a list of query terms, which we assume are


unweighted; A = fad


j a


d


is the score so far for do cument dg is a set of accumulators; and


wd


is the weight of do cument d, which we assume has b een precomputed. This algorithm


returns the k do cuments which are most relevant to the query.

Search(Q)

For each term t  Q


ht; Pt i = Search lexicon for t


Pt


= Uncompress(Pt)


For each (d; wd;t


) in P


t


If ad

ad

Else

ad


 A

= ad + wd;t

= wd;t


A = A [ fad

For each ad  A


g


ad


= ad


=Wd


Return the k do cuments with the highest ad .

In this algorithm, the inverted �le entries for every term t  Q are pro cessed in full. Each

do cument d that app ears in some such inverted �le entry adds a cosine contribution to the


accumulator ad . At the end, the accumulator values are normalized by the weights Wd


. Note


that there is no need to normalize by the weight wq

particular query.


of the query, as wq


is constant for any


The size of A can grow very large, so some search engines place an a priori b ound on


the numb er of accumulators ad


in A. One might think this approach would result in p o or


retrieval e�ectiveness, since the most relevant do cuments may b e found by the last terms

in the query. However, exp eriments with TREC and a standard collection of queries have

shown that ,000 accumulators su�ce to extract the top ,000 do cuments.


-----

. Relevance feedback

In the query systems discussed so far, the user p oses a query vq0, the search engine answers

it, and the pro cess ends. But supp ose the user has the ability to mark a set of do cuments R0


as relevant, and a set I0


as irrelevant. The search engine then mo di�es vq


and


0


to obtain vq


fetches a set of do cuments relevant to vq


. This is called relevance feedback, and continues


until the user is satis�ed. It requires the initial query to b e adapted, emphasizing some

terms, de-emphasizing others, and p erhaps intro ducing entirely new terms. One prop osed

strategy for up dating the query is the Dec Hi strategy:




A


vqi+


= vqi


� vn


:


+


0

X

@

dRi


vd


To obtain the (i + )th query, the vectors for the most relevant do cuments Ri (chosen by the

user) are added to the ith query vector, and the vector vn of the least relevant do cument is

subtracted. A more general up date rule is

X X


v


+ ! vqi


+ �


vd


+ �


vd


;


qi+


= � vq0


dRi

where �, !, �, and � are weighting constants, with � � 0.


dIi


One p otential problem with these up date rules is that the query vectors v qi


for i � 


can have far more terms than the initial query vq0


; thus, these subsequent queries may b e


to o exp ensive to evaluate. One solution is to sort the terms in the relevant do cuments by


decreasing weight, and select a subset of them to in�uence vqi+

clustering, which is describ ed in the next section.


. Another solution is to use


Exp eriments indicate that one round of relevance feedback improves resp onses from

search engines, and two rounds yield a small additional improvement.

. Clustering

Clustering may b e used to sp eed up searches for complicated queries, and to �nd do cuments

which are similar to each other. The idea is to represent a group of do cuments which are all

close to each other by a single vector, for example the centroid of the group. Then, instead

of calculating the relevance of each do cument to a query, we calculate the relevance of each

cluster vector to a query. Then, once the most relevant cluster is found, the do cuments

inside this cluster may b e ranked against the query. This approach may b e extended into a

hierarchy of clusters; see �gure ..

There are many techniques for clustering, as well as many other applications. Clustering

will b e discussed in the Novemb er  lecture.

 Latent semantic indexing (LSI)

All of the metho ds we have seen so far to search a collection of do cuments have matched words

in users' queries to words in do cuments. These approaches all have two drawbacks. First,


-----

###### +’s are centroids
 o o’s are documents
 o o +oo o o + o ellipses are clusters

 o
 +

 o o o o+ o o o o+ o
 o o

Figure 0: A hierarchical clustering approach

since there are usually many ways to express a given concept, there may b e no do cument

that matches the terms in a query even if there is a do cument that matches the meaning

of the query. Second, since a given word may mean many things, a term in a query may

retrieve irrelevant do cuments. In contrast, latent semantic indexing allows users to retrieve

information on the basis of the conceptual content or meaning of a do cument. For example,

the query automobile will pick up do cuments that do not contain automobile, but that do

contain car or p erhaps driver.

. Singular value decomp osition (SVD)

.. De�nition

LSI makes heavy use of the singular value decomp osition. Given an m � n matrix A with

T


m � n, the singular value decomp osition of A (in symb ols, SVD(A)), is A = U �V


, where:


T


T


. U


U = V


V = In


, the n � n identity matrix.


. � = diag (� ; : : : ; �n ), the matrix with all 0's except for the �i 's along the diagonal.

If � is arranged so that � � � � � � � � �n, then the SVD of A is unique (except for


. � = diag (� ;


; : : : ; �n


the p ossibility of equal � ). Further, if r denotes rank(A), then �i


- 0 for  � i � r, and


�j


= 0 for j � r + . Recall that the rank of a matrix is the numb er of indep endent rows


(or columns).

We will use Uk


to denote the �rst k columns of U, Vk


the �rst k columns of V, and �k


the �rst k columns and rows of �. For latent semantic indexing, the key prop erty of the

SVD is given by the following theorem:

T


Theorem: Let A = U �V

De�ne


b e the singular value decomp osition of the m � n matrix A.

T


Ak


= Uk


�k


:


Vk


-----

De�ne the distance b etween two m � n matrices A and B to b e


m

X

i=


n

X

(a

j =


:


ij




� bij )


Then Ak


is the matrix of rank k with minimum distance to A.


This basically says that the b est approximation of A (for the given metric) using a

mapping of a k dimensional space back to the full dimension of A is based on taking the �rst

k columns of U and V .

T


In these scrib e notes, we will refer to Ak

T


= Uk �k


Vk


as the truncated SVD of A. In


the singular value decomp osition U �V

T


, the columns of U are the orthonormal eigenvectors


of AA


and are called the left singular vectors. The columns of V are the orthonormal

T


eigenvectors of A


A and are called the right singular vectors. The diagonal values of � are

T


the nonnegative square ro ots of the eigenvalues of AA

of A.


, and are called the singular values


The calculation of the SVD uses similar techniques as for calculating eigenvectors. For




dense matrices, calculating the SVD takes O (n


) time. For sparse matrices, the Lanczos


algorithm is more e�cient, esp ecially when only the �rst k columns of U and V are required.

. Using SVD for LSI

To use SVD for latent semantic indexing, �rst construct a term-by-do cument matrix A.


Here, At;d


=  if term t app ears in do cument d. Since most words do not app ear in most


do cuments, the term-by-do cument matrix is usually quite sparse. Next, computing SVD(A),

generate U, �, and V . Finally, retain only the �rst k terms of U, �, and V . From these we


could reconstruct Ak

�, and V directly.


, which is an approximation of A, but we actually plan to use the U,


The truncated SVD Ak


describ es the do cuments in k -dimensional space rather than the


n dimensional space of A (think of this space as a k dimensional hyp erplane through the

space de�ned by the original matrix A). Intuitively, since k is much smaller than the numb er


of terms, Ak


\ignores" minor di�erences in terminology. Since A


k


is the closest matrix of


rank (dimension) k to A, terms which o ccur in similar do cuments will b e near each other in

the k -dimensional space. In particular, do cuments which are similar in meaning to a user's

query will b e near the query in k -dimensional space, even though these do cuments may share

no terms with the query.

Let q b e the vector representation of a query. This vector gets transformed into a vector

q^ in k -dimensional space, according to the equation


T


�

�k


q^ = q


Uk


:


The pro jected query vector q^ gets compared to the do cument vectors, and do cuments get

ranked by their proximity to the q^. LSI search engines typically use the cosine measure

as a measure of nearness, and return all do cuments whose cosine with the query do cument

exceeds some threshold. (For details on the cosine measure, see Section ..)


-----

. An example of LSI

Supp ose we want to apply LSI to the small database of b o ok titles given in Figure  (a).

Note that these titles fall into two basic categories, one having to do with the mathematics

of di�erential equations (e.g. B and B0) and one having to do with algorithms (e.g. B

and B). We hop e that the LSI will separate these classes. Figure  (b) shows the term
by-do cument matrix A for the titles and for a subset of the terms (the non stop-words that

app ear more than once).


Now for k =  we can generate U


and V


using an SVD. Now supp ose that we are





, �


interested in all do cuments that p ertain to application and theory. The co ordinates for the

T �


query application theory are computed by the rule q^ = q


U


�



C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

A


, as follows:

: 0

0 :


0



0

0

0

0

0

0

0

0

0

0

0

0

0




0

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

@


0:0 �0:

0:0 �0:

0: �0: 

0:0 0:

0:  0:0

0:0 �0:0

0:00 �0:

0:00 �0:0

0:0 0:

0:0 0:0

0:0 0:

0: �0: 

0: 0:0 

0:00 �0:

0:0  0:0

0:0 0:


T

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

C

A


!�


q^ = (0:0 � 0:) =


0

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

B

@


All do cuments whose cosine with q^ exceeds 0: are illustrated in the shaded region of Fig
ure . Note that B, whose sub ject matter is very close to the query, yet whose title

contains neither theory nor application, is very close to the query vector. Also note that the

mapping into  dimensions clearly separates the two classes of articles, as we had hop ed.

. Applications of LSI

As we have seen, LSI is useful for traditional information retrieval applications, such as

indexing and searching. LSI has many other applications, some of which are surprising.

Cross-language retrieval. This application allows queries in two languages to b e

p erformed on collections of do cuments in these languages. The queries may b e p osed in

either language, and the user sp eci�es the language of the do cuments that the search engine

should return.

For this application, the term-by-do cument matrix contains do cuments which are com
p osed of text in one language app ended to the translation of this text in another language.

For example, in one exp eriment, the do cuments were a set of abstracts that had versions


-----

B Attractors for Semigroups and Evolution Equations

B Automatic Di�erentiation of Algorithms: Theory, Implementation, and Application

B Geometrical Asp ects of Partial Di�erential Equations

B Ideals, Varieties, and Algorithms { An Intro duction to Computational Algebraic

Geometry and Commutative Algebra

B Intro duction to Hamiltonian Dynamical Systems and the N-Bo dy Problem

B Knapsack Problems: Algorithms and Computer Implementations

B Metho ds of Solving Singular Systems of Ordinary Di�erential Equations

B Nonlinear Systems

B0 Ordinary Di�erential Equations

B Oscillation Theory for Neutral Di�erential Equations with Delay

B Oscillation Theory of Delay Di�erential Equations

B Pseudo di�erential Op erators and Nonlinear Partial Di�erential Equations

B Sinc Metho ds for Quadrature and Di�erential Equations

B Stability of Sto chastic Di�erential Equations with Resp ect to Semi-Martingales

B The Boundary Integral Approach to Static and Dynamic Contact Problems

B The Double Mellin-Barnes Typ e Integrals and Their Applications to Convolution

Theory

(a)

Terms Do cuments

B B B B B B B B B B0 B B B B B B B

algorithms 0 0  0  0  0 0 0 0 0 0 0 0 0 0

application 0 0  0 0 0 0 0 0 0 0 0 0 0 0 0 

delay 0 0 0 0 0 0 0 0 0 0   0 0 0 0 0

di�erential 0 0 0  0 0 0  0       0 0

equations   0  0 0 0  0       0 0

implementation 0 0  0 0 0  0 0 0 0 0 0 0 0 0 0

integral  0 0 0 0 0 0 0 0 0 0 0 0 0 0  

intro duction 0 0 0 0   0 0 0 0 0 0 0 0 0 0 0

metho ds 0 0 0 0 0 0 0  0 0 0 0 0  0 0 0

nonlinear 0 0 0 0 0 0 0 0  0 0 0  0 0 0 0

ordinary 0 0 0 0 0 0 0  0  0 0 0 0 0 0 0

oscillation 0 0 0 0 0 0 0 0 0 0   0 0 0 0 0

partial 0 0 0  0 0 0 0 0 0 0 0  0 0 0 0

problem 0 0 0 0 0   0 0 0 0 0 0 0 0  0

systems 0 0 0 0 0  0   0 0 0 0 0 0 0 0

theory 0 0  0 0 0 0 0 0 0   0 0 0 0 

(b)

Figure : An example set of do cument titles and the corresp onding matrix A. Taken from

\Using Linear Algebra for Intelligent Information Retrieval" by Berry, Dumais and O'Brien,

CS- -0, University of Tennessee.


-----

 Berry, Dumais and O'Brien

######  0.2
 B8

 B13
 methods B10
 B4 differential
 ordinary
  0.1 partial B14 equations
 B15
 nonlinear

 systems
 B9

 0.0 0.2 0.4 0.6 0.8 1.0
 B1 B2
 B6

 introduction

 B16 oscillation
 delay

 - 0.2 B5
 B11
 integral
 problem B12

 QUERY
 implementation
 application
 B7
 B17
 algorithms

 -0.5

 theory

 B3

Fig. . A Two-dimensional plot of terms and documents along with the query application

theory.

Figure : The -dimensional p ositioning of the do cuments and terms for a set of  articles.


-----

in b oth French and English. The truncated SVD of the term-do cument matrix is then

computed. After the SVD, monolingual do cuments can b e \folded in" | a monolingual

do cument will get represented as the vector sum of its constituent terms, which are already

represented in the LSI space.

Exp eriments showed that the retrieval of French do cuments in resp onse to English queries

was as e�ective as �rst translating the queries into French, then p erforming a search on

a French-only database. The cross-language retrieval metho d was nearly as e�ective for

retrieving abstracts from an English-Kanji database, and for p erforming searches on English

and Greek translations of the Bible.

Mo deling human memory: LSI has b een used to mo del some of the asso ciative re
lationships in human memory, in particular, the typ e of memory used to recall synonyms.

Indeed, LSI is often describ ed as a metho d for �nding synonyms | words which have similar

meanings, like cow and bovine, are close to each other in LSI space, even if these words never

o ccur in the same do cument. In one exp eriment, researchers calculated the truncated SVD

of a term-by-do cument matrix for an encyclop edia. They then tested the truncated SVD on

a synonym test, which had questions like

levied:

(A) imp osed

(B) b elieved

(C) requested

(D) correlated

For a multiple-choice synonym test, they then computed the similarity of the �rst word (e.g.

levied) to each choice, and picked the closest alternative as the synonym. The truncated

SVD scored as well as the average student.

Matching p eople: LSI has b een used to automate the assignment of reviewers to sub
mitted conference pap ers. Reviewers were describ ed by articles they had written. Submitted

pap ers were represented by their abstracts, and then matched to the closest reviewers. In

other words, reviewers were �rst placed in LSI space, and then p eople who submitted pap ers

were matched to their closest reviewers. Analysis suggested that these automated assign
ments, which to ok less than one hour, were as go o d as those of human exp erts.

. Performance of LSI on TREC

Recall that the TREC collection contains more then ,000,000 do cuments, more than Gbytes

of ASCI I text. TREC also contains 00 standard b enchmarking queries. A panel of human

judges rates the e�ectiveness of a search engine by hand-scoring the do cuments returned

by the search engine when p osed with these queries. These 00 queries are quite detailed,

averaging more than 0 words in length.

Because TREC queries are quite rich, a smaller advantage can b e exp ected for any

approach that involves enhancing user's queries, as LSI do es. Nonetheless, when compared

with the b est keyword searches, LSI p erformed fairly well. For information retrieval tasks,

LSI p erformed % b etter. For information �ltering tasks, LSI p erformed % b etter. (In


-----

information �ltering applications, a user has a stable pro�le, and new do cuments are matched

against these long-standing interests.)

The cost of computing the truncated SVD on the full TREC collection was prohibitively

exp ensive. Instead, a random sample of 0,000 do cuments and 0,000 terms was used. The

resulting term-by-do cument matrix was quite sparse, containing only less than .00% non

zero entries. The Lanczos algorithm was used to �nd A

hours of CPU time on a SUN SPARCstation 0.


; this computation required 


00


-----

Algorithms in the Real World Notes by Amar Chaudhary

Lecture # (Evolutionary Trees and Web Indexing) �c   Amar Chaudhary and Guy

Blello ch

Outline

To day we have two student lectures.

� Evolutionary Trees (Andris Ambainis)

. Parsimony

. Maximum-Likeliho o d

. Distance Metho ds

� Finding Authoritative Web Pages Using the Web's Link Structure (David Wagner)

 Evolutionary Trees (Andris Ambainis)

An evolutionary tree, or phy l og eny, is a tree which describ es the ancestral relationships

among a set of sp ecies. The leaves of an evolutionary tree corresp ond to the sp ecies b eing

compared, and internal no des corresp ond to (p ossibly extinct) ancestral sp ecies. Figure 

shows a simple evolutionary tree for cats, dogs and lynxes. Domestic cats and lynxes share

a feline ancestor distinct from dogs, but all three sp ecies share a common ancestor as well.

�

�

�

�� A

�

�� A

�

�� A

�

�� A

�)�

A

A

A

�

A A

�

A A

�

A A

�

A A

�

A A

�

A A

�

A A

�

A A

�

A A

�

A A

�� A AU

AU

Cat (felix domesticus) Lynx (lynx canadiensis) Dog (canis familiaris)

Figure : An evolutionary tree for cats, dogs and lynxes


-----

Scientists have b een studying and creating phylogenies for over a century. Traditionally,

morphological information and taxonomies were used as data for creating evolutionary trees.

This pro cess was often guided more by intuition than a rigorous set of rules. To day, more

systematic metho ds based on DNA sequencing are used. DNA sequencing provides a much

larger b o dy data which can b e precisely analyzed. Such data b oth demands and facilitates

computer algorithms for generating evolutionary trees.

Three algorithms for creating evolutionary trees will b e discussed in the following sub
sections. In each case, we assume that the DNA sequences have already b een aligned using

multiple alignment, and that each p osition in the sequence is indep endent.

. Parsimony

In the parsimony metho d, the b est tree is the one which explains the data using the smallest

numb er of evolutionary changes:

ACAA


�


Q

Q


�


 0


�

�

�+

ACTA


Q

Q

Q

Qs

ACAA


�

 �

�

��


A

A




A

AAU


J

J 0

J

J^

ACAA


ACGT AGTA


�

�

�

�/�

CCAA


Figure : A parsimony mo del for sequences ACGT, AGTA, CCAA and ACAA. The

numb ers on the edges indicate the numb er of mutations b etween no des

Parsimony can b e formulated as a Steiner Tree problem. For example, given a set of m

n


aligned DNA sequence of length n, consider the n dimensional hyp ercub e G = fA; G; C ; T g


.


The weights on the edges of this graph are the distance metric b etween the two endp oints.

Each DNA sequence is a vertex on this graph. The problem of parsimony is to �nd the

minimum steiner tree with these vertices as demand p oints.

Analysis

If we are given the tree structure with the leaves assigned, we can �nd a minimum-cost

assignment for the internal no des using dynamic programming. However, to �nd the tree

that minimizes the numb er of changes is an NP-hard problem.

We can approximate the solution, however, using lo cal search heuristics. First, we �nd a

\go o d" tree. One way to do this is using a greedy metho d: starting with the set of sp ecies,

keep connecting the two subtrees with the most closely-related ro ots until there is only one

tree. We then apply rearrangement op erations to the tree and check if the rearranged tree

has a lower cost. Possible rearrangement op erations include:

� Swap two subtrees that are children of neighb oring no des.


-----

� Remove a subtree and attach it to some other no de.

This pro cess can b e rep eated a �xed numb er of times, or until we �nd a lo cal minimum.

Discussion

Parsimony assumes that mutations are rare. In fact, this may not the case. Indeed, it is p os
sible using parsimony to construct evolutionary trees that are \p ositively misleading" (i.e.,

the probability of getting the wrong tree approaches one as the amount of data approaches

in�nity) [J].

Despite b eing NP-hard and p ositively misleading, parsimony remains p opular among

evolutionary biologists. It has the advantage of b eing simple, intuitive and app ealing. A

recent study of Rice and Warnow shows that on arti�cial data, parsimony p erforms quite

well [RW ].

. Maximum-Likeliho o d

The maximum-likeliho o d metho d generates an evolutionary tree from a sto chastic mo del of

evolution. The same mo del can b e used to generate trees for di�erent sets of sp ecies.

To simplify this presentation, we �rst assume that DNA sequences are binary (i.e., se
quences of 0's and 's).

We will describ e sto chastic mo dels called Cavender-Farris trees. Such a tree has a prob
ability asso ciated with each edge as well as an initial state probability asso ciated with the


ro ot. Given a tree with ro ot probability pR


and probabilities pe


for each edge e, each p osition


of the binary sequence is generated as follows:

. The ro ot is lab eled  with probability pR


and 0 with probability  � pr


.


. Each lab eled no de broadcasts its lab el to all its children.

. When a lab el is broadcast over edge e, it gets reversed with probability pe


.


Figure  shows an example of a Cavender-Farris tree. We generate a sequence for a no de

X (i.e., sp ecies X ) by rep eatedly running the sto chastic pro cess and adding the lab el of X

to the sequence, as illustrated in �gure . This metho d relies on the assumption that all

p ositions in a DNA sequence are indep endent.

When using four states (i.e., A,G,C,T), each edge is assigned a probability matrix instead


of a scalar probability pe


:













pAA

pCA

pGA

pTA


pAC

pCC

pGC

pTC


pAG

pCG

pGG

pTG


pAT

pCT

pGT

pTT













where pXY


is the probability that X changes to Y. Biologists often assume that some or all


pXY


are related, or even equal.


-----

0.


�

�

�

0. �

�

�

��


B

B

B

B


B

B

B


0.0

B

B

B

B

B

B

B

BBN

C


�

�


B


B


0. 0.0


�

�

�

�

��

A


B


B

B

B

BN.

B


0

�

�

�

�

�

0


B

B

B

B

B

B

B


Figure : A sto chastic mo del as a Cavender-Farris tree






B

B

B

B

B

B

B

B


�

�

�

�

�




B

B


B

B

B


0 


�

�

�

�

�



A

A

A

AU


�

�ip

�

�

�


A

A

A

AU


B

B

BN


A

A

A

AU


B

B

B

B

BN


�

�ip

�

�

�


 0 0

A B C


�

�

�

�




 

A B C


A


B


B

BN



C


Figure : Generating sequences from the sto chastic mo del in �gure . Edges over which

the lab el has b een �ipp ed are marked with \�ip."


-----

Given a sto chastic mo del of evolution, the maximum-likeliho o d metho d �nds a tree T


that maximizes pT (S ) where S is the set of DNA sequences and pT


(S ) is the probability that


T will generate all the sequences in S .

This metho d is much more general than parsimony, which has a �xed mo del of evolution

that may b e incorrect. Assuming that the chosen sto chastic mo del of evolution is accurate,

this metho d will give a correct evolutionary tree for any set of sp ecies. However, it is the

most computationally exp ensive of the metho ds discussed in this lecture, and is rarely used

on large trees.

. Distance metho ds

In the distance metho d, we create a matrix D consisting of similarity measures b etween pairs

of sp ecies in the set b eing studied. Then, we �nd a tree that generates the distance matrix

closest to D . This metho d is illustrated by the following example.

An example

Take three sp ecies, a, b and c with the following DNA sequences:

a: ACAAAAACAA

b: ACTTGAACAT

c: TCTAAAACAT

Now generate a similarity matrix for a, b and c:









� 0: 0:

0: � 0:

0: 0: �









The similarity measure used is dxy


= M =L where:


M is the numb er of p ositions with synonymous characters.

U is the numb er of p ositions with non-synonymous characters.

G is the numb er of p ositions with gaps in one sequence and residue in another.


W


= )


G


is the weight of gaps. (For this example WG


L = M + U + WG G

Transform the similarity matrix into a matrix with estimates of \evolutionary time" b e

tween sp ecies. We estimate the evolutionary time txy


b etween two sp ecies x and y as


txy


= ln( � dxy


).









� : 0: 

: � 0: 

0:  0:  �









Now, �nd a tree with no des a, b and c such that the distance b etween each of these no des is

the same as the evolutionary time b etween the corresp onding sp ecies:

Note that the tree in �gure  is undirected.


-----

�

�


c

.

S

S

S


.


.�

�

�

�

�


S

S

S

SS

b


a


Figure : An evolutionary that �ts the time matrix for sp ecies a, b and c.

Analysis

If the data precisely �ts some tree, then this metho d is relatively simple. However, real

data have random errors. If no tree exactly �ts the data, �nding the tree that is closest to

a distance matrix is NP-complete under several de�nitions of \closeness." In practice, the

following heuristic, called nearest-neighbor joining [SN] is often used:


0

� Intro duce closeness measure d (x; y ) = (n � )d(x; y ) �


P

x


d(x; z ) �


P

y


d(y ; z )


� Rep eat until only one no de remains:

0

. Search for x and y that minimize d


0


(x; y ).


. Replace x and y with a new no de xy .

. Calculate d(xy ; z ) = (d(x; z ) + d(y ; z ) � d(x; y ))=

The evolutionary tree will the tree where each pair of no des x and y is connected its joint

xy :

��

x PP

��PPP-��

xy

�*




� ��

���

�

�

y

��


Figure : A branch of the evolutionary tree joining nearest neighb ors x and y .

 Finding authoritative web pages using link struc
ture (David Wagner)

To day's web search engines do keyword searching. This technique is very p owerful, but it

handles broad queries quite p o orly. The quantity of hits is often very high, and the quality


-----

of these hits varies widely.

We want to b e able to identify authoritative sources for broad queries. This lecture

presents an algorithm which:

. Views the web as a directed graph.

. Picks a relevant subgraph using standard search techniques.

. Analyzes the resulting link structure.

Why analyze the link structure? Take two pages p and q such that p has a link to q .

Through this link, the creator of page p has in some sense conferred authority on q . For

example, the \Algorithms in the Real World" class page contains a large numb er of links to

related pages. These linked pages can b e considered authoritative sources on algorithms in

the real world.

. A naive approach using adjacency

The \authoritativeness" of p can b e measured using the in-degree of p, or the numb er of

pages which link to p. More precisely, we want the in-degree of p in a subgraph induced by

the keyword search for the query. Such a subgraph can b e generated by taking the top 00

pages returned by a standard search engine (like AltaVista or HotBot) as a ro ot set, and

then adding all \adjacent" pages (i.e., pages with links into and out of the ro ot set).

This approach do es not work very well in practice. For example, a search on the word

\java" will probably return pages on the programming language, the island in Indonesia and

the p opular ca�einated b everage. It is likely that the user only wanted one of these topics.

However, an analysis of the link structure in this query result will likely reveal three

subgraphs, separated roughly by topic and with few interconnecting links b etween them.

This prop erty leads to an improved search algorithm.

. An algorithm for �nding communities within topics

Hubs are pages that p oint to multiple relevant authoritative pages. The b est known example

of a hub is Yaho o. An authority is a page that is p ointed to by multiple relevant hubs. For

example, the JavaSoft home page is an authority, since is linked by most hubs that catalogue

Java links.

We want to �nd communities, or sets of hubs H and authorities A such that H + A

resembles a dense bipartite graph.

We will now de�ne an iterative algorithm for �nding communities. Page p is assigned

weights x[p] and y [p] that represent authority weight and hub weight, resp ectively. The hub

weight x[p] is the sum of authority weights of its outgoing links. Likewise, y [p] is the sum

of the hub weights of pages that p oint to p. Figure 0 illustrates how x[p] and y [p] are

calculated.

The algorithm can b e implemented using linear algebra. Let A b e the adjacency matrix


of the graph induced by the keyword search. Apq


is  if p has a link to q and 0 otherwise. At


-----

��

��.SZXZXXXXXX


S Z XXXz��

��

S Z �

�

��. �S��Z�Z ��� ��


�

P

ZP


�Z �

S Z

PPS�P � ZZ~��

� �PPPq


S


��P

Z

Z


Z

�


S

Z�


��


�

���


Z��S��

�� Z


�


��


��� � ZZ~S


   

�


��

�

�

� �


-Sw

��* ��

�


���

��

��

Figure  : A subgraph representing a community. Hubs (on the left) p oint to authorities

(on the right).

��

q

��PP

P

P

P

�� PP

PPq��

             - P

q


    

p x[p] =


��

��


�����


���:��

��

�� q


q


��

��


�

�

�

�

����

�

�

p PP

��PP

P

P

P

P


��

��

- y [p] =

q

��

��


P


y [qi

x[qi


]

]


� 

PPq

��q

Figure 0: Calculating the hub weight and authority weight of a page p


-----

T


each iteration, let x = A


y and y = Ax. Normalize x and y, and rep eat the pro cess until x


and y converge. From linear algebra, we know that x and y will eventually converge to the


T

principal eigenvectors of A


T

A and AA


.


Each eigenvector corresp onds to one community. The principal eigenvector corresp onds

to the most prominent community, but other eigenvectors can b e used to examine other

communities in the topic. It is interesting to note the similarities b etween the linear algebra

approach to �nding communities and the use of SVD in latent semantic indexing as describ ed

T


in the previous lecture. Recall that in �nding the S V D (A) = U �V

T


that the columns


of U are the normalized eigenvectors of AA

T


and the columns of V are the normalized


eigenvectors of A


A. Using U


gives us the principal eigenvectors (the ones with the





and V


highest eigenvalue). In fact, the iterative approach mentioned ab ove (often called rep eated

squaring) is just one of the many approaches to solve for the �rst eigenvectors for the SVD.

Here are some examples of real queries using this algorithm:

� The principal eigenvector of the query \java" includes JavaSoft, the comp.lang.java

FAQ, etc.

� The query \net censorship" includes the sites for EFF, CDT, VTW and ACLU, all of

which are organizations that play a prominent role in free sp eech issues on the net.

� The query \ab ortion" returns pro-life pages as one eigenvector and pro-choice pages as

another. Each side of the issue tends to form a bipartite graph with very few cross-links

to the opp osition.

This metho d works surprisingly well for broad queries, and shows promise for some other

search tasks, such as \similar page" queries (i.e. search for pages with information similar

to a given page). However, for very sp eci�c queries, the authoritative search do es not work

very well. Rather, it tends to �nd authorities for generalizations of the query topic. It might

b e p ossible to use lexical ranking function to keep the authoritative search oriented, but this

is left op en for future work.

For further reading

More details on the authoritative searching technique can b e found elsewhere. [K ].

References

[J] J. Felsenstein, \Cases in which parsimony or compatibility metho ds will b e

p ositively misleading." Systematic Zoology, :0-0,  .

[K ] J. Kleinb erg. \Authoritative Sources in a Hyp erlinked Environment." IBM

Research Rep ort RJ 00, May  . This pap er will also app ear in the

�

Pro ceedings of the ACM SIAM Symp osium on Discrete Algorithms,  .

[RW ] Kenneth Rice and Tandy Warnow, \Parsimony is Hard to Beat." COCOON .


-----

[SN] N. Saifou, M. Nei. \The neighb or-joining metho d: a new metho d for uncon
structing phylogenic trees." Mol.Biol.Evol., :0-,  .


-----

Algorithms in the Real World Notes by Josh MacDonald

Lecture # (Clustering) �c   Josh MacDonald and Guy Blello ch

� Principle Comp onent Analysis

. LSI

. Authoritative Sources

� Intro duction to Clustering

. Applications

. Distance and similarity measures

� Clustering Algorithms

. Bottom-up Hierarchical

. Top-down Hierarchical

. Optimization

. Density Search

 Principle Comp onent Analysis

The study of principle component analysis (PCA) go es back at least as far as  0 and has

a numb er of closely related �elds:

� factor analysis

� latent semantic indexing

� latent vectors

� Hotelling

� singular value decomp osition

� principle comp onents

� SV transform

The ob jective of PCA is to �nd the eigenvectors and asso ciated eigenvalues of a similarity

or correlation matrix. For n items an n � n similarity matrix S is one in which the entry


Sij


represents the similarity b etween items i and j |the matrix is typically symmetric. The


eigenvector of S with the highest eigenvalue sp eci�es the direction that b est \separates" the

items. In particular it is the pro jection of the items into a  dimensional space that b est

maintains the similarity metric (i.e., similar items have close values in the eigenvector).


-----

Here we will brie�y lo ok at how latent semantic indexing and authoritative sources are

just sp ecial cases of PCA. Recall that the singular value decomp osition of an m � n matrix

A yields the following:

T

A = U �V

where


T


T


U


U = V


V = I


and � is a diagonal matrix with diagonal entries �


; �


; : : :. If A has rank r (numb er of


indep endent rows or columns) then U has dimension m � r, V has dimension n � r, and �

has dimension r � r . (In lecture  we assumed that for m � n that r is replaced with n in

the stated sizes, but when r < n only the �rst r columns, or rows, are actually imp ortant

and the rest can b e dropp ed.) By using the ab ove equations, we get


T


T

A = (U �V

T

= (V � U

 T


T

)

T


)

)



A with eigenvalue �i




(0)

. Similarly,


A


(U �V


)(U �V


= V �

and by multiplying by V on the right we get

T


V


T


A


AV = V �

= V �







V


V


T

T

T


This shows that each column of V is an eigenvector of A

T


each column of U is an eigenvector of AA


with eigenvalue �

i


. We can therefore think of

T


the columns of V as the principal comp onents of a similarity matrix A

T


A and the columns

T


of U as the principal comp onents of a similarity matrix AA


. Since A


A is just all the


dot pro ducts of the columns, the \similarity" measure b eing used by V is dot pro duct of

columns, and the \similarity" measure b eing used by U is dot pro duct of rows.

Latent Semantic Indexing

We discussed latent semantic indexing as a metho d for improving text-retrieval with the

hop es of �nding content which did not directly match our query, but was semantically \close".

Here the matrix elements Aij represents the weight of each term i in a do cument j . Thus

each row represent a term in the dictionary, and each column represent a do cument. In this

framework, U represents the principal comp onents of the dot pro duct of rows (i.e., term
term similarities), and V represents the principal comp onents of the dot pro duct of columns

(i.e., the do cument-do cument similarities). If we normalize the rows of A, for example, then

the similarity measure b eing used to generate U is simply the cosine measure.

Authoritative Sources

The hyp er-linked graph of do cuments represent a directed graph from which we construct


an adjacency matrix A (i.e., place a  in Aij


if there is a link from i to j and a 0 otherwise).


-----

T

The matrix A


A now represents for each pair of do cuments i and j how many links they

T


have in common, and the matrix AA


represent for each pair of do cuments i and j how


many common pages link to b oth of them. These matrices can b e thought of as similarity

measures b etween sources, and destinations, resp ectively. In the de�nitions given in the last

class a \hub" is a page that p oints to multiple relevant authoritative pages. The principal

T


comp onent of A


A (also the �rst column of U in the SVD decomp osition of A) will give the


\principal hub". An \authority" is a page that is p ointed to by multiple relevant hubs. The

T


principal comp onent of AA


(also the �rst column of V in the SVD decomp osition of A)


will give the \principal authority".

 Intro duction to Clustering

The ob jective of clustering is, given a set of ob jects and a measure of similarity or distance

b etween the ob jects, cluster into groups of similar (nearby) ob jects. Clustering is also called:

� typ ology

� grouping

� clumping

� classi�cation

� unsup ervised learning

� numerical taxonomy

. Applications

There are many applications of clustering, here are a few:

� biology: multiple alignment, evolutionary trees

� business: marketing research, risk analysis

� lib eral arts: classifying painters, writers, musicians

� computer science: compression, vector quantization, information retrieval, color reduc
tion

� so ciology and psychology: p ersonality typ es, classifying criminals, classifying survey

resp onses and exp erimental data.

� indexing and searching: group results into categories (Hearst and Pederson,  )


-----

. Similarity and Distance Measures

To cluster the items in a set we need some notion of distance and/or similarity b etween

items. Typically when one talks ab out a distance measure d(i; j ) b etween items i and j in a

set E one assumes that d is a metric for E, and therefore abides by the following conditions:

d(i; j ) � 0

d(i; i) = 0

d(i; j ) = d(j; i)

d(i; j ) � d(i; k ) + d(k ; j )

The fourth condition is the familiar triangle inequality. These conditions are met for com
mon metrics such as the Euclidean distance and the Manhattan distance. Metrics may b e

combined, so, for example, the maximum of two metrics is itself a metric space. Many

clustering algorithms that use distance measures assume all four conditions are met.

A similarity is a measure of how close two p oints are in a space. We are familiar with

cosine measures, dot-pro ducts, and identity as measures of similarity. In general, however,

similarities might b e supplied by a black b ox or by human judgment.

One question is whether similarities and distances can b e used interchangeably. Given an

arbitrary distance measure we can always come up with a corresp onding similarity measure:



s(i; j ) =

 + d(i; j )

Given a similarity measure (ranging from 0 to ) we might also try the corresp onding distance

metric




d(i; j ) =


� 


s(i; j )

This measure, however, do es not necessarily form a metric. Therefore one should b e careful

when using such a transformation to generate a distance from a similarity, esp ecially if it

is going to b e applied in a clustering algorithm that assumes the distance function forms a

metric.

 Clustering Algorithms

We will b e considering four classes of algorithms for clustering.

� Bottom-up Hierarchical (agglomerative)

� Top-down Hierarchical (divisive)

� Optimization

� Density searches


-----

###### k i j


Figure : Lance and Williams' Rule

The various algorithms we consider not only vary in how they work but in what they

are optimizing. In some applications it is imp ortant to have a �xed numb er of clusters,

while in others it is b etter to �nd \natural" clusters which will return a numb er of clusters

that dep ends on the nature of the data. In some applications, such as some index searching

techniques, a hierarchy of clusters is required while in others it is not. In some applications

it is b est to minimize the maximum distance within each cluster, while in others it is b etter

to minimize the average distance. There is therefore no single \correct" clustering of a set

of items, but instead what constitutes a go o d clustering will dep end on the application.

. Bottom-Up Hierarchical Algorithms

The basic algorithm for b ottom-up, or agglomerative, metho ds is to b egin with a set of p oints

and appropriate distance measure, and initially place each p oint in its own group. And then

while the numb er of groups is greater than one, merge the closest pair of groups into a single

group. This basic structure leads to a whole collection of di�erent metho ds dep ending on

how distance b etween groups is measured. Some common measures are minimum, maximum,

centroid, average, or sum-of-squares distance b etween the p oints in each group. The last,

sum-of-squares metho d is also known as \Wards' metho d", and uses the function:


S S (G ) � S S (G


) � S S (G )


where


X

xG;y G


S S (G) =




jGj


(dxy




)


Note that when using minimum as the distance measure the metho d simply �nds the mini
mum spanning tree of the graph in which the items are the vertices and the distance d(i; j )

is used as the weight of an edge from i to j .

An interesting generalization of the ab ove �ve group-distance measures is due to Lance

and Williams,  . They show a function that generalizes the previous metrics for the

distance b etween cluster k and the cluster consisting of sub-clusters i and j . The metric


must b e recursively applied. There are four parameters, �i, �j

numb er of elements inside cluster x.


, �, and � . nx


represents the


dk (ij )


= �i


dk i


+ �


j


dk j


+ � dij


+ � jdk i


� dk j


j


With this formula, we can pro duce the nearest neighb or metric,


�i


= �j







=







; � = 0; � = �


-----

the furthest neighb or metric,

the centroid metric,


; � = 0; � =

nj


�i


= �j







=







=

nk


ni

+ ni


+ ni


=


ni

; �j

+ nj

; �j =


ni

nk


+ nj

+ nj


; � = ��i �j

; � =


�nk


and Wards' metho d,


�i

nk


�i


=


nk


+ ni


+ n


j


+ nj


nk


+ ni


+ n


j


. Top-Down Hierarchical Algorithms

Top-down clustering approaches are broken into polythetic and monothetic metho ds. A

monothetic approach divides clusters based on analysis of one variable at a time. A p olythetic

approach divides clusters into arbitrary subsets.

Splinter Group Accumulation

A technique called splinter group accumulation removes the most outstanding item in a

cluster and adds it to another, rep eating until moving the item will increase the total cost

measure. Pseudo-co de for this algorithm follows, where we assume the measure we are trying

to optimize is the average distance within a group.


C

C


= P

= fg


lo op


for each pi




P

pj


di




jC j


d(i; j )


=


 C

P

j pj


d(i; j ) �


C


C


jC


if max di


- 0


C

C

else


= C

= C



[ Pi

� Pi


return

We could also use a di�erent measure in the co de ab ove, such as Wards' metho d.

Graph Separators


A cut of a graph separates vertices V into two sets, V

sum of each edge weight crossing the cut:


and V


. The weight of a cut is the


X

j V


Wcut


=


X

iV


wij


-----

Assuming we use a similarity measure, the goal is to �nd a cut which minimizes Wcut,

where the weights are the similarities, while keeping the two clusters approximately the same

size. Various conditions can b e used, such as forcing the ratio of sizes to b e b ounded by

some numb er, usually less than two. In the general case, �nding the optimal separator is

NP-hard.

Finding go o d separators for graphs is a topic of its own. Other applications of graphs

separators include

� Solving sparse linear systems (nested dissection). The goal is to minimize �l l.

� Distributing graphs or sparse matrices on multipro cessors. The goal is to minimize

parallel communication during program execution.

� VLSI layout{�nding placements that minimize communication.

For geometric problems, metho ds such as the k d-tree or circular cuts can b e used to

compute separators. Without geometric information, the spectral method uses a technique

similar to singular value decomp osition (or principal comp onent analysis). The principal

comp onent (actually the second eigenvector since the �rst turns out to b e \trivial") is used

to separate the p oints | the p oints are split by the median value of the vector.

. Optimization Algorithms

Expressed as an optimization problem, clustering attempts to divide data into k groups to

maximize or minimize some measure, e.g.,

� sum of intra-group distances

� sum squared of intra-group distances

� maximum intra-group distances

Most measures lead to an NP-hard problem and heuristics are often applied.

Optimization as an Integer Program

One technique uses integer programming to minimize the sum of intra-group distances.

Stated as an integer programming problem:


Pn

j =


xij


minimize


Pn

i=


dij


sub ject to

 � i � n

 � j � n

 � k � g

Pg


y


j = ij

 Pg

g k = z

yik + yj k


= 

ij k � xij

�  � z


ij k


-----

where g is the numb er of groups, xij


=  if ob ject i and j are in the same group, yik


= 


if ob ject i is in group k, and zij k


=  if ob jects i and j are in group k . The �rst condition


states that each ob ject must b e in one group. The second condition states that i and j may

app ear in at most one group together. The �nal condition relates y and z, stating that if

two ob jects are in the same group, z is true.

. Density Search Algorithms

Density search techniques try to �nd regions of \high density". There are many such tech
niques. A particularly simple metho d starts with the minimum-spanning-tree for the graph:

. �nd MST

. remove all edges with weights much greater than the average for its vertices

. �nd connected comp onents.

This metho d has the advantage of �nding \natural" groupings rather than �xing the

numb er of groups, b ecause the size and granularity of the clusters it pro duces are dep endent

on the parameter used to remove edges.

. Summary

There are many algorithms for clustering. The key question to b e answered b efore picking

an algorithm is what the mo del of a go o d clustering is. The challenge for authors of these

algorithms to day seems to b e making clustering fast for large collections of data.


-----

Algorithms in the Real World Notes by Carleton Miyamoto

Lecture # (Guest lecture Eric Brewer on HotBot) �c   Carleton Miyamoto and Guy

Blello ch

� Comment on Assignment (Guy)

� Goals of HotBot

� Internal Architecture

. Semantics

. Hardware

. Data Base Mo del

. Score

. Filters

� Optimizations

. Caching

. Compression

. Parallelism

. Misc.

� Crawling

� Summary

� References

 Comment on Assignment (Guy)

Problem 

Problem  in the last assignment could b e done by combining the a�ne gap and space

e�ciency examples given in class and in the readings. There, however, were a few caveats

which needed to b e addressed.

First, the algorithm must keep separate p ointers for the E and S entries. This is necessary

b ecause the path could have come from an E or S crossing. The F entries can b e generated

on the �y.

Second, gaps which cross the middle row must b e dealt with carefully (Fig. ). If not

the algorithm could double charge for that gap. A solution is to store b oth p ointers back to

the middle row for b oth E and S.

Only four arrays of size O(m) are required in a space e�cient algorithm (see Fig. ).

They hold E, S, and the p ointers p ointing back to the lo cation in the middle row from where

E and S came.


-----

T Middle Row

,TT

, Q

, Q

Q

Gap ends

`````

Figure : A gap may cross the middle row

Pointers for last row


Middle Row


�


�


�


......P....�................ �.............. Q.........�..Q Middle Row

Last Row

Figure : Keep two arrays for each of S and E


.


-----

 Goals of HotBot

History

HotBot originated in the Berkeley NOW pro ject. An application was needed that would

show the b ene�ts of clustering. A search engine was decided up on as the killer app. b ecause

its requirements closely matched what cluster computing could provide.

Availability

In order to achieve x uptime, a mission critical infrastructure is necessary. Fault tolerance

and redundancy are cornerstones in achieving this goal. The multiple individual machines

in clusters provide a natural metho d.

Scalability

Additionally, a search engine must expand its service as client requests grow. Since growth in

the WEB, however, is o ccurring at a staggering rate, big, exp ensive machines, quickly would

b ecome overloaded, with replacement the only upgrade option. So, incremental scalability

could provide a large economic advantage over the longer term.

Not only the hardware, but the software design must take all this into account. Fine

grained parallelism and multi-pro cessor supp ort should adapt well in this environment.

Both the availability and scalability requirements for a search engine could b e addressed

by the NOW clusters.

 Internal Architecture

. Semantics

The semantics of a search engine are simple. Although the search engine itself must b e highly

available, that data it contains do es not. The WEB can always b e used as a last recourse to

retrieve any requested information.

Additionally, a very weak consistency mo del can b e maintained. Known as BASE [], it

allows stale information to p ersist for a limited time.

. Hardware

Currently 0 UltraSPARC CPUs p ower HotBot. The system is very homogeneous, which

allows a no de to take over for an arbitrary one when necessary. These are connected to a

vast numb er of RAID disk subsystems which contain over 0.TB of data.

If a single no de go es down, the data asso ciated with that no de b ecomes temp orarily

unavailable. This is okay due to the weak consistency mo del. Also, this constitutes only

a small fraction of the total data. Note that the system as a whole, however, continues to

pro cess requests despite this.


-----

id = id


@�

�@


##

#


H

H


H

HH

Do cuments

Key:

@�


�@ Equi-join

List

@� Semi-join


@�

�@

Z


,,

,

,

id, f


Select top 0

�

�

id = id

Z

Z

Z

�lter


id = id


@�

�@


�@

Figure : An example of a search query


In comparison to a single, large, p owerful SMP system, HotBot's commo dity parts are

faster and cost less. For example, in order to expand the service, additional, ordinary systems

can b e b ought, adding their p ower to the current set. SMP's, however, are not additive in

this resp ect, nor do they provide any form of fault tolerance in system up-time. At the very

least, replication is necessary, requiring additional, exp ensive hardware.

. Data Base Mo del

The search engine algorithms can b e describ ed in relational data base (RDBMS) terms.

There exists a relation w (a row in a table) for each unique word in each do cument found

in the WEB: w[do cument ID, score, p osition information]. The entry keeps track of the

do cument in which the word was found (using a unique ID). The score helps in matching the

word to a search and is discussed b elow. The p osition information helps in phrase searching.

There are currently ab out 0M words in HotBot's database with an average of ab out K

lines p er word. HotBot has to deal with some words which o ccur in almost every do cument

and with many words that o ccur very infrequently.

There is also a relation D for all do cuments on the WEB where: D[ID, URL, etc ...

]. This identi�es each do cument with a unique ID, as well as information to retrieve the

do cument later.

When the RDBMS needs to b e up dated with fresh data, an atomic swap op eration swaps

a new data base to replace the old b etween queries. This allows hot up dates to o ccur without

any interruption of service.

When a search query is received by HotBot, it go es through a series of relational joins.

For example, if the query \A B �lter:C" is received (i.e. search for A and B, then apply a

b o olean �lter on the output based on C), Fig.  shows the relational op erations. The �rst

equi-join (lower left) is doing the search for A (think of it as an \and" op eration). It then

creates a list of the result, sorted by score (f ). The semi-join then executes the b o olean �lter

on the list. The top ten scores are selected and a �nal equi-join is done to get the asso ciated


-----

..


......


Frequency of word


.


.


.


.


.

.


.


.


.


.


.


.


.


.


.


.

Score = f


. . . . . . . .


Figure : Determining the score

do cuments for the result page to return to the client.

. Score

The score (f ) determines when a word matches a query and how closely. Higher scores

(weights) cause the do cument to app ear higher on HotBot's priority lists to the RDBMS

joins and on the result page returned to the client. The value is calculated as a function of

a few di�erent attributes, which includes:

. Numb er of times a word app ears in the do cument

. Do cument length

. If the word app ears in the do cument title

This function is then broken down into equal area slices, and a \score" from 0 to  is

assigned to each slice. See Fig.  for an example of how the function and slices could

app ear.

. Filters

As shown in an example ab ove, �lters allow the query to express b o olean matches. In fact,

�lters are implemented as meta-words, where w contains all do cuments that would match

the sp eci�c �lter. As a result, a �lter can b e thought of as the addition of this meta-word on

the search line. Filters are use-full in expressing searches on features of pages that cannot b e

expressed otherwise (such as do es the page contain an image). Note, however, that less-than

and greater-than op erators cannot b e easily addressed by this mechanism. Dates, however,

are imp ortant and do require some typ e of less-than, greater-than functionality. HotBot uses

a trick which expands a date query into log(n) b o olean queries, where \n" is the numb er of

bits in the date sp eci�cation.


-----

 Optimizations

In order to achieve b etter throughput of query transactions, optimizations help to streamline

the search pro cess.

. Caching

Instead of just caching do cuments, HotBot also caches search results. In fact, the \next 0"

button is actually another full search that completes quickly b ecause of the cache.

. Compression

Extensive compression helps to minimize the fo otprint of the data. Score and p osition

information are split with IDs stored in b oth lists. Compression then allows the p osition

information, which is used infrequently, to o ccupy minimal space. A typ e of delta-enco ding

is used (similar to Hu�man) that uses a variable numb er of bits.

In HotBot, b ecause of the large amount of data, nothing is uncompressed, even when

loaded directly into memory, until necessary. The reasoning is that the additional page faults

that would b e generated by uncompressing when loading into memory outweighs the time

to uncompress the data more often [, ].

. Data Base

HotBot uses a technique called join selectivity to sp eed its RDBMS op erations. It orders

op erations which have the highest probability of resulting in a short list �rst. This reduces

the work of future RDBMS op erations. For example, applying very sp eci�c b o olean �lters

�rst could reduce list sizes for later equi-joins.

In addition, HotBot spreads the RDBMS data across many no des in the cluster (by

do cument ID in the D relation) at a relatively �ne grain. Single no de failures b ecome

manageable and the amount of data a�ected minimal. Also, when up dating, the �ne grains

allow atomic swaps of the data to b e simple and require little additional space.

. Parallelism

When optimizing for parallelism, \balance" is the key word. If all no des are working to their

fullest, and there are no single b ottlenecks, this allows for the highest degree of parallelism.

HotBot attempts to address this by:

. Randomizing data across the no des

. Use a large numb er of disks to hide seek latency

The randomizing reduces the risk of hot sp ots forming within the cluster (similar to the

arguments in []).

HotBot also executes each query in parallel. Because each no de is resp onsible for part of

the total database, it �rst issues the query to each no de (Fig. ). The no des then send the


-----

@�

�@


id = id

H

H

HH


H


##

#


Select top 0

U


�

�

�

�

� �

�

Select top 0

id, f


@

T

@

T @

TT


Do cuments

Figure : Parallelization of queries


@� id = id

�@

TCP connection

��

Master

��P

P

""" � @@ PPPPP

"" �� @


P

P


��

N

��


��


��


��


PP


  


..............


��


��


��


Figure : Naive fanout

highest scoring subset of their results back to a \master" no de. This then takes the union of

the answers, returns the top scores among all of the no des resp onding, then do es the �nal

equi-join to asso ciate the answers with the do cuments. Note that every query utilizes every

no de.

Another problem is how the fanout from the original master no de, that initially receives

the query, happ ens as the queries are b eing distributed (Fig. ). A naive solution would

b e to send the queries in sequence starting from the �rst no de. This, however, could lead

to hot sp ots or head of line blo cking (queries are arti�cially blo cked on a resource due to a

previous query) o ccurring in the fanout chain.

HotBot attempts to avoid problems by using two techniques (Fig. ):

. Fanout in multiple levels (a fat tree structure)

. At each stage, fanout to random no des


-----

TCP connection

��

Master

��P

P

"""""�� � @@@PPPPPPPP


��


��


��


P��


? ? ? .............. ?


�� �� �� ��

H

� T H E

H

� T H E

H

� T H E

� T HH

�� �� �� ��EE

? ? ? .................. ?

�� �� �� ��

� D e � J

� D e � J

� D e � J

�� D e � JJ

D

Figure : Optimized fanout (each ? is a random no de)

In the future, HotBot could take advantage of knowledge of the physical network layout.

A more optimized fanout may know where the limiting bisection bandwidths b etween cut
sets of the network are lo cated and incur less tra�c over those connections.

. Misc.

Some additional optimizations are done to sp eed up each query:

. Precomputation: As much information as p ossible is computed o�-line. For example,

the scores can b e computed and stored as the pages are read in from the WEB. Also,

�lters (i.e. meta-words) can b e created and managed b efore queries requesting the

information arrive.

. Partitions of the no des are up dated at varying times. This gives a b etter illusion that

the data is up-to-date. Some data, such as news groups are up dated more frequently.

. HotBot will dynamically skip words that are to o exp ensive to compute. This usually

o ccurs with words that app ear in many do cuments, such as \a" or \the".

 Crawling

HotBot has a separate partition that crawls the WEB at ab out 0M pages a day. It uses

\p opular" sites (such as p ossibly Yaho o) as the ro ots of these searches. These up dates

eventually enter the HotBot database at various times.


-----

 Summary

The b ene�ts gained from clustering matched the exp ectations placed on search engines well.

Their availability, scalability, and price/p erformance ratio cannot b e achieved even by more

exp ensive SMP servers.

References

[] A. Fox, S. Gribble, Y. Chawathe, E. Brewer, and P. Gauthier, Cluster-Based Scalable

Network Services, (To app ear at SOSP-, Oct.  ).

[] Fred Douglis. The Compression Cache: Using On-line Compression to Extend Physical

Memory. USENIX Pro ceedings, Winter  .

[] D. Banks, M Stemm. Investigating Virtual Memory Compression on Portable Architec
tures. http://HTTP.CS.Berkeley.EDU/~stemm/classes/cs.ps.gz

[] Waldspurger and Weihl. Lottery Scheduling: Flexible Proportional-Share Resource Man
agement. Pro ceedings of the First Symp osium of Op erating System Design and Imple
mentation, Novemb er  .


-----

 References by Topic

. Compression

Primary Texts

Khalid Sayo o d. Introduction to Data Compression. Morgan Kaufmann,  .

Other Sources

Timothy C. Bell, John G. Cleary, and Ian H. Witten. Text compression. Prentice Hall,  0.

Gilb ert Held and Thomas R. Marshall. Data and Image Compression: Tools and Techniques.

Wiley,   (th ed.)

Mark Nelson. The Data Compression Book. M&T Bo oks,  .

James A. Storer (Editor). Image and Text Compression. Kluwer,  .

Ian H. Witten, Alistair Mo�at, and Timothy C. Bell. Managing Gigabytes: Compressing

and Indexing Documents and Images. Van Nostrand Reinhold,  .

. Cryptography

Primary Texts

Alfred J. Menezes, Paul C. van Oorschot and Scott A. Vanstone. Handbook of Applied

Cryptography. CRC Press,  .

Bruce Schneier. Applied Cryptography. Wiley,  .

Douglas R. Stinson. Cryptography: Theory and Practice. CRC Press,  .

Other Sources

G. Brassard. Modern Cryptology: a tutorial. Spinger-Verlag,  .

N. Koblitz. A course in number theory and cryptography. Springer-Verlag,  .

C. P�eeger. Security in Computing. Prentice-Hall,   .

A. Saloma. Public-key cryptography. Springer-Verlag,  0.

Jennifer Seb erry and Josed Pieprzyk. Cryptography: An Introduction to Computer Security.

Prentice-Hall,   .

D. Welsh. Codes and Cryptography. Claredon Press,  .


-----

. Linear and Integer Programming

Texts

M. Bazaraa, J. Jarvis, and H. Sherali. Linear Programming and Network Flows. Wiley,

 0.

Dimitris Bertsimas and John N. Tsitsiklis. Introduction to Linear Optimization. Athena

Scienti�c,  

J. P. Ignizio and T. M. Cavalier, Linear Programming. Prentice Hall,  

G. L. Nemhauser, A.H.G. Rinno oy Kan, and M. J. To dd (ed.). Optimization. Elsevier,   .

George L. Nemhauser and Laurence A. Wolsey. Integer and combinatorial optimization.

Wiley,  .

H. M Salkin and K. Mathur. Foundations of Integer Programming. North-Holland,   .

Rob ert J. Vanderb ei. Linear Programming: Foundations and Extensions. Academic Pub
lishers,  

Stavros A. Zenios (ed.). Financial optimization. Cambridge University Press,  .

Useful Overview Pap ers

G. L. Nemhauser. The age of optimization: solving large-scale real-world problems. Op era
tions Research, (), Jan.-Feb.  , pp. -.

E. L. Johnson and G. L. Nemhauser. Recent developments and future directions in mathe
matical programming. IBM Systems Journal, vol., no.;  ; pp.  - .

I. J. Lustig, R. E. Marsten and D. F. Shanno. Interior point methods for linear programming:

computational state of the art. ORSA Journal on Computing, vol., no.; Winter  ; pp.

-.

. Triangulation

Primary Texts

M. de Berg, M. van Kreveld M. Overmars, and O. Schwarzkopf. Computational Geometry,

Algorithms and Applications. Springer-Verlag,  .

Other Texts

J. E. Go o dman, and J. O'Rourke (Editors). Handbook of Discrete and Computational Ge
ometry. CRC Press,  .

K. Mulmuley. Computational Geometry: An Introduction Through Randomized Algorithms.

Prentice Hall,  .


-----

J. Nievergelt and K. Hinrichs. Algorithms and data structures: with applications to graphics

and geometry. Prentice Hall,  .

J. Pach and P.K. Agarwal. Combinatorial Geometry. John Wiley and Sons,  .

Preparata, Franco P. Computational geometry: an introduction. Springer-Verlag,  .

A. Okab e, B. Bo ots, and K. Sugihara. Spatial Tessel lations: Concepts and Applications of

Voronoi Diagrams. John Wiley,  .

O'Rourke. Computational Geometry in C. Cambridge University Press,  .

. N-b o dy Simulation

Susanne Pfalzner and Paul Gibb on. Many Body Tree Methods in Physics. Cambridge

University Press,  .

L. Greengard. Fast algorithms for classical physics. Science, vol. , no. ,  Aug.

 , pp. 0 -.

J. E. Barnes and P. Hut. A hierarchical O(N Log N) force calculation algorithm. Nature,

():-, Decemb er  .

. VLSI Physical Design

Primary Texts

N. Sherwani. Algorithms for VLSI Physical Design Automation, Second Edition. Kluwer,

 .

M. Sarrafzadeh and C. K. Wong. An Introduction to VLSI Physical Design. McGraw-Hill,

 .

Other Texts

P. Banerjee. Paral lel Algorithms for VLSI Computer-Aided Design. Prentice Hall,  .

A. B. Kahng and G. Robins. On Optimal Interconnections for VLSI. Kluwer Academic

Publishers,  .

B. Korte, L Lovasz, H. J. Promel, and A. Schrijver (eds.). Paths, �ows, and VLSI-layout.

Springer Verlag,  0.

T. Lengauer, Combinatorial algorithms for integrated circuit layout. Wiley,  0.

M. Pecht and Y. T. Wong (editors). Advanced Routing of Electronic Modules. CRC Press,

 .

M. Sarrafzadeh and D.T. Lee (editors). Algorithmic Aspects of VLSI Layout (Lecture Notes

Series on Computing, Vol ). World Scienti�c,  .


-----

. Pattern Matching in Biology

Dan Gus�eld. Algorithms on String, Trees, and Sequences. Cambridge University Press,

 .

Arthur M. Lesk. Computational molecular biology: sources and methods for sequence anal
ysis. Oxford University Press,  .

Graham A Stephen. String searching algorithms. World Scienti�c,  .

M.S. Waterman. Introduction to Computational Biology: Maps, Sequences, Genomes. Chap
man & Hall,  .

. Indexing and Searching

Christos Faloutsos. Searching Multimedia Data Bases by Content. Kluwer Academic,  .

Frakes and Baeza-Yates (ed.). Information Retrieval: Data Structures and Algorithms. Pren
tice Hall,  

Frants V. J., Shapiro J., Voiskunskii V. G. Automated Information Retrieval Theory and

Methods. Academic Press, Aug  .

Lesk M. Practical Digital Libraries Books, Bytes & Bucks. Morgan Kaufman Publishers,

 .

Salton. Automatic Text Processing: The Transformation, Analysis and Retrieval of Infor
mation by Computer. Addison-Wesley,   .

Sparck Jones K. and Willett P. (editors). Readings in Information Retrieval. Morgan Kauf
man Publishers,  .

Ian H. Witten, Alistair Mo�at, and Timothy C. Bell. Managing Gigabytes: Compressing

and Indexing Documents and Images. Van Nostrand Reinhold,  .

. Clustering

Leonard Kaufman and Peter J. Rousseeuw. Finding Groups in Data : An Introduction to

Cluster Analysis. Wiley,  0.

Everitt, Brian. Cluster analysis (d ed.). Wiley,  .

E. Backer. Computer-Assisted Reasoning in Cluster Analysis. Prentice Hall,  .

 Assignments


-----

Algorithms in the Real World

Assignment # (Compression) Due Date:  Sept 

Collab oration p olicy: You are welcome to talk ab out this or other assignments with

others and even discuss problems using a whiteb oard or scratch pap er. You are not allowed,

however, to show or give any work that you did on your own p ertaining to the assignment

to someone else.

Problem : Assume an alphab et S = fa; b; cg has the probabilities


p


= : pc


= :


a


= : pb


(a) What is the entropy H (S )?

(b) What is the average length of the Hu�man co de for S (rememb er to weigh the average

based on the probabilities).

(c) What is the average length of the Hu�man co de if you group characters into pairs.

(d) For a long string what is the average p er-character length of an arithmetic co de for S

(assume the asymptotic value and that the message abides by the probabilities).

(e) For a long string what is the average p er-character length of an arithmetic co de for S

assuming your mo del are the probabilities given ab ove, but you are co ding a message

which consists of just c's (i.e., your data do es not �t your mo del).

(f ) Given the following conditional probabilities what is the conditional entropy (this is

the average p er-character length that would b e achieved by a go o d co de that takes

advantage of the probabilities).

p(aja) = : p(bja) = : p(cja) = :

p(ajb) = : p(bjb) = : p(cjb) = :

p(ajc) = : p(bjc) = : p(cjc) = :

The notation p(xjy ) is the probability of x given that the previous character is y .

P


Problem : Prove that the average length l


=


li


pi


for a Hu�man co de for a set of


a


messages S is b ounded by the inequality la


� H (S ) + . To prove this you can assume the


Hu�man co de is optimal. Note that given a maximum probability pm

of (


a tigher upp er b ound


pm

+ :0 pm


� :

< :


la


<


H (S ) + pm

H (S ) + pm


can b e shown. Feel free to prove this stronger result.


-----

Problem : Assume we are co ding a  letter alphab et with LZW and we start with the

dictionary containing the  letters fa; b; c; dg in lo cations 0, ,  and . Entries are added to

the dictionary in sequential order. Deco de the following message that was co ded with LZW.

0 0    

Problem : Using the LZSS (the variant of LZ describ ed in the reading \Intro duction

to data compression" by Peter Gutmann) and assuming a window size W and a lo okahead

bu�er size B, how many co de words will it take to co de a message of length L that contains

all the same character. Assume each <o�set,size> pair or character is a co deword. Also

assume the window is initialized to some other character.

Problem : Lets say we had the following sequence of values

0        0 -0  -  -  -

(a) Would we would get b etter compression by doing a cosine transform across the whole

group of  or by blo cking the  entries into two groups of  and transforming each

separately? Explain brie�y?

(b) If using a wavelet transform are we b etter o� blo cking the entries into two groups of ?


-----

Algorithms in the Real World

Assignment # (Cryptography) Due Date:  Oct 

Problem :

Assume you design an encryption scheme with a single round DES (instead of the usual

 rounds and ignoring the initial and �nal p ermutations). If you know a message cipher


pair (m


; c





assuming c





(m


).


) for a key k for the values given b elow, what is m


= D E S k


Assume the following hexidecimal values for m


 ; c


and c .


m

c

c


= FDE 0CDB

= 0CDB EE

= 0CDB CD


If you show the �rst  (leftmost) hexidecimal digits of m

the rest.

Problem :


that will convince me you know





Assume we have a  � -bit s-b ox used in a blo ck ciphers. For each of the following three

substitutions explain what is wrong.


Input out


out


out


Problem :


0  0 

   

   

   

 0  

   0

   

   

�


(a) Assuming p and q are primes, express x


mo d pq as a p ositive p ower of x.


(b) Given public key e = , n =   enco de the value  using RSA.

(c) Assuming the same public key, deco de the value 0 (you might want to write a short

program to do it).

(d) In RSA for some n lets say e =  (a standard choice in some systems). If I accidentally

give away d show how one can use this information to factor n.


-----

Problem :

(a) Using ElGamal Encryption with the public key p = ; g = ; y =  encrypt the value

with random k = .

(b) Decrypt the pair (,).

(c) Given p =  why is 0 a bad value for g ?

Problem :


(a) Generate the �rst  bits of the BBS random bit generator assuming that n = ; r0


=  .


(b) For an arbitrary Blum integer n = pq give an upp er b ound on the p erio d of the generator

(how many iterations it takes b efore it rep eats). This need not b e the strongest upp er
b ound but you will get more credit the stronger it is.


-----

Algorithms in the Real World

Assignment # (Integer and Linear Programming) Due Date:  Oct 

Please feel free to send me email if there are any ambigouous questions.

Problem : Strang Chapter  problem ..

Problem : Strang Chapter  problem ...

Problem : Strang Chapter  problem ...

Problem :

Consider the following problem


maximize x + x

sub ject to x + x


� 


(a) Starting with the initial solution (x

scaling interior-p oint metho d.


; x


x; x � 0

) = :; : solve this problem using the a�ne


(b) Illustrate the progress of the algorithm on the the graph in x

Problem :


space.





� x


n


n

: Ax � bg and T = fx  R


: B x � dg. Assuming that S and T are


Let S = fx  R


nonempty, describ e a p olynomial time algorithm (in n) for checking whether S � T .

Problem :

Formulate the following problem as a mixed integer programming problem.


maximize f (x) + f


(x)


+ x � 

 + x � 

+ x �


sub ject to at least two of the following


x

x

x


x ; x


� 0

(

0 + x ; 0 � x


where


� 


f

f


(x ) =

(x ) =


(


 + x ; otherwise

 + x ; 0 � x � 


 + x


otherwise


-----

Problem :

Solve the following problem using the branch-and-b ound integer programming pro cedure

describ e in class. Feel free to do it graphically.


maximize x

sub ject to x


+ x

� x


�x


+ x


� 

� 

� 


x


+ x


x ; x

x ; x


� 0

integers


Problem :

Solve the following problem using implicit enumeration (the 0- programming technique)

describ e in class.


minimize x


minimize x + x + x + x

sub ject to �x + x � x � x

�x � x � x + x

x ; x ; x ; x binary


+ x


� �

 � �


-----

Algorithms in the Real World

Assignment # (Triangulation and N-b o dy) Due Date:  Nov 

Implement one of the following algorithms:

. Rup ert's Meshing Algorithm

. Garland and Heckb ert's Surface Mo deling Algorithm

. Callahan and Kosara ju's Well-Separated Pair Decomp osition Algorithm

Feel free to work in groups of two, although I will exp ect a b etter job from a group of two.

Also feel free to come and discuss the algorithms with me. I've describ ed each of these

algorithms in class and have also made pap ers available that describ e the algorithms in more

detail. Two of the pap ers are available on the web, and the third is in a JACM issue that is

available the CS reading ro om (So da ).

Note: Source co de for some of these algorithms is available on the web. If you cho ose to do

a problem, please do not lo ok at anyone elses source until you have handed in your imple
mentation. You should feel free, however, to use other p eoples co de for various subroutines

such as implementing a heap. Make sure you reference the co de.

I have made some co de for incremental Delaunay Triangulation available, which you might

�nd useful for either of the �rst two algorithms. This is taken from the b o ok "Graphics Gems

IV", edited by Paul Heckb ert, Academic Press,  . A copy of the asso ciated chapter

is available outside my do or. The co de is also available as part of a compressed tar �le

asso ciated with the b o ok. You might �nd, however, that it is just as easy if not easier to

design your co de from scratch since deciphering the co de is not trivial. Also, as I mentioned

in class, you might �nd a triangle based representation simpler (the co de uses the quadedge

representation). If you do use any part of the co de, make sure to note in your co de which

parts you used.

You might also �nd Jonathan Shewchuk's Show-me co de (showme.c) useful for plotting a

set of triangles, or b oundaries.

Rup ert's Meshing Algorithm

You should implement the algorithm and run it on the test sets given b elow and rep ort

back the numb er of triangles for minimum angles in the ranges sp eci�ed. Ideally you should

generate a p ostscript drawing of the �nal triangulations. Although the drawings are not

required they will certainly help you debug your program. The algorirthm is describ ed in:

Jim Rup ert. \A Delaunay Re�nement Algorithm for Quality -Dimensional Mesh

Generation." Journal of Algorithms, ():-, May  .


-----

The test data �les: (Note: these use the Poly format from Jonathan Schewchuk's Triangle

co de)

� The letter A from Rup ert's pap er. Run this from  to  degrees in steps of  degrees.

� Lake Sup erior from Rup ert's pap er. Run this from 0 to  degrees in  degree steps.

Note that this input has an internal angle that is just slightly larger than  degrees,

so it will not work with larger angles.

� A guitar from Jonathan Schewchuk. Run this from  to  degrees in steps of 

degrees.

Note that all data is included in a b ounding b ox. This simpli�es the problem of dealing with

exterior triangles (all triangles in the b ox are considered interior). In your implementation

you don't need to remove the triangles in the exterior (b etween b ox and surface) nor in

the "holes". You can therefore ignore the "holes" data at the end of the .p oly �les. If

you do chose to remove the triangles, however, you can use the "holes" data by starting at

each triangle with the hole p oint and removing triangles outwards until you hit a b oundary

segment. If you cho ose to remove them please state this in your results.

Garland and Heckb ert's Surface Mo deling Algorithm

You should implement the algorithm and run it on the test sets given b elow and rep ort back

the numb er of triangles for a range of maximum errors. Again generating a drawing of the

triangulation will b e helpful but is not necessary. The algorirthm is describ ed in:

Michael Garland and Paul Heckb ert. \Fast Polygonal Approximation of Terrains

and Height Fields." CMU-CS- -, CS Dept, Carnegie Mellon U., Sept.  .

The algorithm I want you to implement is numb er I I I in the pap er (the version I describ ed

in class).

The test data �les: (Note: these are binary �les in STM format)

� Crater lake

� Ashby Gap, Virginia

� Desert around Mt. Tiefort, California

� Ozark, Missouri


-----

Callahan and Kosara ju's Well-Separated Pair Decomp osition Algorithm:

You should implement the algorithm in  or  dimensions and run it on the Kuzmin mo del

with 0K and 00K p oints (I originally said Plummer mo del, but I cannot �nd an equation

for generating a Plummer distribution...if you do, please feel free to use it, but tell me.)

For b oth sizes you should rep ort the numb er of interactions as a function of the separation

constant s ranging from  to  in increments of .. The algorirthm is describ ed in:

Paul B. Callahan and S. Rao Kosara ju. \A Decomp osition of Multi-Dimensional

Point-Sets with Applications to k-Nearest-Neighb ors and n-Bo dy Potential Fields."

JACM, ():- 0, January  .

Available for copying in the CS reading ro om.


-----

Algorithms in the Real World

Assignment # (VLSI and Pattern Matching) Due Date:  Nov 

Please feel free to send me email if there are any ambiguous questions.

Problem : Consider the following graph.

A. Find a minimum cost Rectilinear Steiner Tree (RST) for the following set of p oints (the

shaded p oints are the demand p oints).

B. Is this an S-RST? If not show the minimum cost S-RST.

Problem : For the following routing problem the three nets A; B and C need to b e

connected. The numb ers on the edges represent their lengths, and assume that the capacity

of every edge is .


###### A


###### 2


###### C


###### 7
 2
 B

 B 2 2 1
 2
 A
 2
 C

 8 4
 B

A. Sp ecify an integer (0-) program for which the solution gives the minimum total wire

length.

B. Solve the program (you do not need to show your work).

Problem : Describ e an O (nm) time O (n + m) space algorithm for �nding a minimum

cost alignment assuming an a�ne gap cost mo del. Pseudo co de with comments would b e the

b est way to describ e it.


-----

Problem : (Extra Credit.) Describ e an O (nm log (m + n)) time algorithms for �nding

a minimum cost alignment assuming the gap cost function x(k ) (where k is the length of the

gap) is concave downward (i.e. the second derivative is always negative).


-----

