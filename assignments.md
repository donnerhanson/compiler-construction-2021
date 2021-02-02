## Assignments

### Introduction

Programming assignments are part of the [assessment](assessment.md). Some general rules: 
- If the assignment does not specify (enough) milestones create your own. Document them in the README.
- Your repo must show a trail of your work. I will **not** grade your programs if your repo only shows the finished product without the work leading up to the intermediate milestones.
- All programs must be tested.
- No points for programs that do not run. If you have specific problems get in touch before the deadline.
- Grading will be based on correctness, but readability and maintanability will also be taken into consideration.

See also the info on [git best practices](git-best-practices.md). 

**Assignments** can be done in groups of up to 2 students. Writing a compiler is difficult. Assignments are not intended (only) as a test of your abilities, but are (also) part of the learning process. So do not hesitate to ask me questions in class, on the discussion forum, in office hourse, or directly via email. Note that [participation]() is part of the assessment. 

If you get stuck in one of the Assignments 2-5:
- Read my notes and the relevant sections of the book. If you have any questions on this, **ask on the discussion forum** as this may be of interest to everybody.
- Discuss with your team member. Try to implement the relevant case. Write your own test programs.
- If you remain stuck after putting in all this work, commit your code to the repo and send me an email. 


For these, fork the repo [here]() (link to be added).

## Assignments 

Rough estimate of deadlines:

| Assignment | Deadline |
|:---:|:---:|
1| End of Feb 
2| 2nd half of March
3| Mid April
4| Early May

### Assignment 1

This assignment is best done in groups of two, but can also be done individually. 

[Grammar and Parser for C++](http://www.grammaticalframework.org/ipl-book/assignments/assignment1/assignment1.html). You can start from `bnfc/examples/cpp/cpp.cf`, see also [here](https://github.com/alexhkurz/compiler-construction-2020/blob/master/Sources/Cpp/cpp.cf).  
  - Deadlines for the test programs is as follows. Submit each of them via email to me.
      - `hello.cc`: tba
      - `greet.cc`: tba 
      - `med.cc`: tba
      - `grade.cc`: tba
      - `palin.cc`: tba
      - `grammar.cc`: tba
  - Deadline for all programs in `test/good` and  `test/bad`: 

This assignment is a great opportunity to practice proper use of git. Provide a full trail of your work under git. In particular, each time your parser parses successfully a new testfile, it is time to make sure that this grammar is pushed to git. You can then create a new branch to work on the new version of the grammar and merge it back to master when it passes the new test-file. Branches also allow you to work in a group on different versions of the grammar at the same time. For example, while one of you works on statements, the other works on arithmetic expressions.

Use git to share your current version of the grammar with me if you want to ask me a question.
 
### Assignment 2

Assignment 2: [Type Checker for CPP](https://github.com/ChapmanCPSC/compiler-assignments/blob/master/README.md). 

This assignment is based on [Assignment 2 IPL](http://www.grammaticalframework.org/ipl-book/assignments/assignment2/assignment2.html).

For 2021: Finer breakdown of this assignment in more deadlines.
 
### Assignment 3

Assignment 3: [Interpreter for CPP](https://github.com/ChapmanCPSC/compiler-assignments/blob/master/README.md). Deadlines should be mid April ...

This assignment is based on [Assignment 3 IPL](http://www.grammaticalframework.org/ipl-book/assignments/assignment3/assignment3.html).
  
For 2021: Finer breakdown of this assignment in more deadlines.

### Assignment 4

Assignment 4: [Compiling C++ to Webassembly](https://github.com/ChapmanCPSC/compiler-assignments/blob/master/README.md). Deadlines should be early May ...

For 2021: Finer breakdown of this assignment in more deadlines.

