# Lecture by Lecture  

**Homework** is essential preparation for midterm and final but not graded. Ask any questions on the discussion forum. **Excursions** are optional.

## Part 1: Lexing, Finite Automata, Regular Expressions

In the first week we find that automata are a good specification language to specify algorithms searching for patterns in text.

- L1.1: [Searching for Strings](https://hackmd.io/@alexhkurz/Sk555wUlu). Don't forget the [Homework](https://hackmd.io/@alexhkurz/rycnvMvgu).

- L1.2: Answers to homework questions. [Introduction to Automata and Haskell](https://hackmd.io/@alexhkurz/HylLKujCP). Excursion on [*Why do Java and Python not have goto statements?*](https://hackmd.io/@alexhkurz/rJ5wS-0f8) Practice what you have learned with this important [Homework](homework-1.2.md).

In the second week we go one level up, from automata as a specification language for search algorithms to regular expressions as a specification language for automata (and languages).

- L2.1: [Composing Automata (with Homework)](https://hackmd.io/@alexhkurz/ryV_FU7XI) ... [Handwritten notes from the lecture](Sources/Notes-from-the-lecture-Composing-Automata.pdf) ... 

- L2.2: [Regular Expressions](https://hackmd.io/@alexhkurz/HkoNj8mmU) ... [Handwritten notes from the lecture](Sources/Notes-from-lecture-2.2.pdf) ... [Homework](https://hackmd.io/@alexhkurz/S1EVYe7bO) ...  

In the third week, we learn how to convert regular expressions to NFA and NFA to DFA.

- L3.1: Continued from last lecture's [Regular Expressions](https://hackmd.io/@alexhkurz/HkoNj8mmU). We reviewed Exercises 2.5.3.b and c from [Composing Automata](https://hackmd.io/@alexhkurz/ryV_FU7XI) in detail. We also wrote out a DFA for Exercise 2.3.4.a and then discussed the algorithm converting NFA to DFA. For a summary of the lecture as well as practice questions see the new [homework](https://hackmd.io/@alexhkurz/HJ1BAFYbd).

- L.3.2: Continued from [Regular Expressions](https://hackmd.io/@alexhkurz/HkoNj8mmU). We first reviewed the [homework](https://hackmd.io/@alexhkurz/HJ1BAFYbd) and looked at the Haskell implementation of the conversion from NFA to DFA from the [Introduction to Automata and Haskell](https://hackmd.io/@alexhkurz/HylLKujCP). Then we reviewed Exercise 2.5.3.a from the homework of [Composing Automata](https://hackmd.io/@alexhkurz/ryV_FU7XI). Most importantly, we learned an algorithm of how to eliminate epsilon-transitions. For practice questions see the [homework](https://hackmd.io/@alexhkurz/Sy8EDt3Wu). 

This finishes what I consider the most important aspects of DFA, NFA, and regular expressions: **(1)** How to use DFA to search for/recognise patterns of strings (=languages) in a text. **(2)** How to use regular expressions to specify languages. **(3)** How to translate regular expressions to NFA and how to translate NFA to DFA. To summarize:

        reg.exp. ~> NFA ~> DFA ~> code

If we had time the next steps in the story of finite automata would be the following. **(a)** For every DFA there is a regular expression. This completes the proof the famous Kleene theorem that regular expressions and finite automata are equivalent in the sense that they recognise the same languages (called regular languages). **(b)** For every DFA there is an equivalent minimal DFA. This is important as the minimal DFA is the most efficient implementation (in terms of space) of a regular language. 

For **midterm and final** the most relevant skills from Part 1 are: equivalence of regular expressions and NFA, the algorithm that eliminates epsilon-transitions, the algorithm that converts NFA to DFA 

## Part 2: Parsing and Context-Free Grammars

- L4.1: [Assignment 1](https://hackmd.io/@alexhkurz/HJ4KjezfO).
- L4.2: [Introduction to Shift-Reduce Parsing](https://hackmd.io/@alexhkurz/rk5PsF2EI) ... handwritten [notes](https://github.com/alexhkurz/compiler-construction-2021/blob/master/Sources/Notes-from-the-lecture-intro-shift-reduce.pdf) from the lecture ...
- L5.1: Introduction to [Shift/reduce and reduce/reduce conflicts](https://hackmd.io/@alexhkurz/SJx6T5R48) and the  [LALR(1) parser](https://hackmd.io/@alexhkurz/SJ4sbGyrU) generated by BNFC/Happy. 
- L5.2: Question and Answer Session.
- L6.1: To put the theory we have seen so far in context, I reviewed the [Chomsky Hierarchy](https://www.youtube.com/watch?v=224plb3bCog) and gave a prove of the undecidability of the [Halting Problem](https://www.youtube.com/watch?v=macM_MtS_w4&t=0s).  In the comments to the linked videos you find more on this topic, all highly recommended. I also enjoyed watching [Halting Problem in Python](https://www.youtube.com/watch?v=r__GZ7ubU0M). Here are my [handwritten notes](https://github.com/alexhkurz/compiler-construction-2021/blob/master/Sources/Notes-from-the-lecture-chomsky-hierarchy-halting-problem.pdf) from the lecture. In the afternoon lecture, we also looked at ["The tourist saw the astronomer with the telescope"](https://github.com/alexhkurz/compiler-construction-2021/blob/master/Sources/The_tourist_saw_the_astronomer_with_the_telescope.pdf) from the point of view of shift-reduce conflicts.
- L6.2: We talked about the rightmost column in the table summarising the [Chomsky hierarchy](https://en.wikipedia.org/wiki/Chomsky_hierarchy#The_hierarchy). Read Chapter 3.9 to 4.3 of [IPL](http://www.cse.chalmers.se/edu/year/2012/course/DAT150/lectures/plt-book.pdf). Then we returned to Assignment 1 and reviewed some examples of how to [debug a grammar](https://hackmd.io/@alexhkurz/SkXrrBuSI). 

## Part 3: Type Checking

**Stocktaking:** We have covered the first three chapters of the book [Implementing Programming Languages](http://www.cse.chalmers.se/edu/year/2012/course/DAT150/lectures/plt-book.pdf). This could be a good time to read through these chapters to consolidate what we learned. We will now turn to Chapter 4 of [IPL](http://www.cse.chalmers.se/edu/year/2012/course/DAT150/lectures/plt-book.pdf). Reasons why type checking is important:

- The copy language is not context free.
- Compile-time errors are cheaper than run-time errors.
- Information in the types can be used to produce more efficient code.
- Types can be used to disambiguate over-loaded operations.

For us there is another one, namely that type checking can be seen as "interpretation at compile time". Everything we learn about typechecking will help us to understand interpretation better.

- L7.1: Working towards Assignment 3, the [Type Checker for CPP](http://www.grammaticalframework.org/ipl-book/assignments/assignment2/assignment2.html). Main source is Chapter 4 of the book. *Homework:* Read Chapter 4.1 to 4.3 of [IPL](http://www.cse.chalmers.se/edu/year/2012/course/DAT150/lectures/plt-book.pdf). 

- L7.2: [Assignment 2](https://github.com/ChapmanCPSC/compiler-assignments/blob/master/Typechecker/). Read Chapter 4.4 to 4.6 of [IPL](http://www.cse.chalmers.se/edu/year/2012/course/DAT150/lectures/plt-book.pdf).

- L8.1: Revision for midterm.

- L8.2: Midterm in class.

- L9.1 and 9.2: Back to the typechecker. Read Chapter 4.8 of [IPL](http://www.cse.chalmers.se/edu/year/2012/course/DAT150/lectures/plt-book.pdf).

## Part 4: Interpreter

- L10.1: Interpreter and Operational Semantics. Read Chapters 5.1 and 5.2 of [IPL](http://www.cse.chalmers.se/edu/year/2012/course/DAT150/lectures/plt-book.pdf).

- L10.2: Starting [Assignment 3](https://github.com/ChapmanCPSC/compiler-assignments/blob/master/Interpreter/README.md) on the Interpreter.

- L11.1: Read Chapter 5.3 of the book.

- L11.2: Read Chapter 5.4 and 5.5 of the book. [Homework](https://hackmd.io/@alexhkurz/S1wmI_yPO).

- L12.1: Seminar announcement ... Discussion Midterm ... JVM, [IPL](http://www.cse.chalmers.se/edu/year/2012/course/DAT150/lectures/plt-book.pdf), [Slides Chapter 5](https://github.com/alexhkurz/compiler-construction-2021/blob/master/Sources/5-slides-ipl-book.pdf)

## Part 5: Code Generation

- L 12.2: [Compiling C++ to WASM](https://github.com/alexhkurz/compiler-construction-2021/blob/master/lecture-12.1.md) and [Assignment 4](https://github.com/ChapmanCPSC/compiler-assignments/blob/master/Compiler/README.md).


---

**Midterm:** First Thursday after Spring Break, Thursday April 1, in class. **Practice test:** [Automata](https://github.com/alexhkurz/compiler-construction-2021/blob/master/Sources/practice-test-1-dfas.pdf), [Grammar](https://github.com/alexhkurz/compiler-construction-2021/blob/master/Sources/practice-test-2.md). If you want to check your solution send it to me via email. [Solution](https://github.com/alexhkurz/compiler-construction-2021/blob/master/Sources/Notes-from-the-lecture-on-practice-midterm.pdf). See also the recordings of the Tuesday lecture. Solutions: [Midterm-Morning](https://github.com/alexhkurz/compiler-construction-2021/blob/master/Sources/Midterm-Morning-Solutions.pdf), [Midterm-Afternoon](https://github.com/alexhkurz/compiler-construction-2021/blob/master/Sources/Midterm-Afternoon-Solutions.pdf), [Shift-Reduce-Parsing](https://hackmd.io/@alexhkurz/Sys8OPQUO).

---

coming up:

Code generation.

Last day of instruction: May 15

---





