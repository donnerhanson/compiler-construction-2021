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

---

coming up soon:

shift-reduce parsing

---

Spring break: March 22-27

Last day of instruction: May 15

---





