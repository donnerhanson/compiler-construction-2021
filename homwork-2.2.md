# Homework on Regular Expressions and NFA

(part of [CC 2021](https://github.com/alexhkurz/compiler-construction-2021/blob/master/lecture-by-lecture.md))

("the book" refers to [Introduction to Automata Theory, Languages, and Computation](http://ce.sharif.edu/courses/94-95/1/ce414-2/resources/root/Text%20Books/Automata/John%20E.%20Hopcroft,%20Rajeev%20Motwani,%20Jeffrey%20D.%20Ullman-Introduction%20to%20Automata%20Theory,%20Languages,%20and%20Computations-Prentice%20Hall%20%282006%29.pdf))

## Lecture 2.2

In the lecture, we worked through Exercise 2.5.3.a and used it to explain how NFAs and regular expressions work. To deepen your knowledge and try some exercises:

- Do Exercise 2.5.3.b and c.
- Read Section 3.1.1 "The Operators of Regular Expressions".
- Read Example 3.2.
- Do Exercise 3.2.4.


## Coming Soon

- Read the section on converting NFAs to DFAs from the [Short Introduction to Automata and Haskell](https://hackmd.io/zo6eujQmTQyMoFquFxdv0Q?view#Converting-NFAs-to-DFAs) together with Section 2.3.5 from the book.
- **Convert [these NFAs](https://github.com/alexhkurz/compiler-construction-2021/blob/master/Sources/nfas-assignment1.pdf) to DFAs**. Compare with the DFAs from the [first homework](https://hackmd.io/@alexhkurz/rycnvMvgu).
- Read Section 2.5.5 on eliminating $\epsilon$-transitions. 
- **Convert [these $\epsilon$-NFAs](https://github.com/alexhkurz/compiler-construction-2021/blob/master/Sources/enfas-assignment1.pdf) to DFAs**. Compare with the NFAs above.
- Read Section 3.1.2 on the definition of regular expressions
- Read Section 3.2.3 on converting regular expressions to automata

For further practice for midterm and final, try some of the exercises in Sections 2.3.7 and 2.5.6.

## Optional Homework and Further Reading

- Do the "Exercise on Converting NFAs to DFAs" from the [Short Introduction to Automata and Haskell](https://hackmd.io/zo6eujQmTQyMoFquFxdv0Q?view#Converting-NFAs-to-DFAs) which asks you to implement the algorithm in Haskell (you get a template, so it is just 3 lines of code).

- I didn't have time to think about how to do $\epsilon$-transitions in Haskell. I'd be curious to know if you gave it a try.

- Have a look at the article [(Rabin and Scott, 1959)](https://www.researchgate.net/publication/230876408_Finite_Automata_and_Their_Decision_Problems) which introduced non-deterministic automata. Both authors later made much deeper contributions to computer science (such as zero knowledge proofs and domain theory), but non-determinstic automata were important enough to grant them the "Nobel price of computer science", the Turing award, in 1976. 

    Most algorithms are deterministic and, until not so long ago, implementations on a modern computer were deterministic (even those using random numbers). So why are non-determinstic machines so important?

    - Specifications as opposed to implentations typically do not determine computations completely.
    - Modelling open systems, the environment is often best modelled non-determinstically. For example, 
      - an operating system interacting with a keyboard cannot predict which keys will be pressed next
      - in security modelling an attacker must allow the intruder any possible action
    - In the presence of concurrency or parallelism, the precise timing or even order of actions is not determined.
    - In algorithms, non-deterministic machines are crucial to describe the possibly most important class of algorithms, namely those in non-deterministic polynomial time (NP).
    - Non-deterministic automata and deterministic automata are equivalent, but non-determinstic automata can be exponentially smaller.

- Have a look at Kleene's orginal [Representation of Events in Nerve Nets and Finite Automata](http://www.dlsi.ua.es/~mlf/nnafmc/papers/kleene56representation.pdf) is difficult to follow today. It is still worth looking at. Here are some of my takeaways and questions.
  - The paper was motivated by what we would call today neural networks. The famous paper [(McCulloch and Pitts, 1943)](https://www.cs.cmu.edu/~./epxing/Class/10715/reading/McCulloch.and.Pitts.pdf) which Kleene takes as a starting point was very influential in many areas including AI and machine learning. 
  - It is also interesting to note that Turing machines are only mentioned in the last paragraph (before the appendix). While we see DFAs and Turing machines as members of the same hierarchy of machines, it is not clear how much Kleene's paper was influenced by Turing.
  - Kleene's "regular events" (Section 7) are easily recognisable as what we call regular expressions today. Our theorem from the lecture, that each regular expression corresponds to a finite automaton should be Theorem 4. How different is Kleene's proof from ours? Does he allow non-deterministic automata?
  - Kleene's "finite automata" (Section 8) do not yet have the clean mathematical definition we use today.
  - Regular languages are defined in Section 9 just before Lemma 7.
  - I didn't try to understand the proof that every finite automaton can be described by a regular expression (Theorem 5 in Section 9). It would be an interesting exercise to translate the proof in to modern language and then to determine which of the different textbook proofs correspond to it.
