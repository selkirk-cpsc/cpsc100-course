# CPSC 100: Introduction to Computer Programming

Course notes and interactive demos for CPSC 100 at Selkirk College.

**[Course info](https://selkirk-cpsc.github.io/cpsc100-course/course/) · [Schedule](https://selkirk-cpsc.github.io/cpsc100-course/schedule/) · [Setting up your coding environment](https://selkirk-cpsc.github.io/cpsc100-course/setup/)**

Assignments, tutorial submissions, grades and all due dates are on [Moodle](https://learn.selkirk.ca/).

## Lecture Notes

Each week's lecture written out as a chapter you can read top to bottom, with the code, flow diagrams and links to the demos.

| Week | Chapter |
|---|---|
| 1 | [What is a Program?](https://selkirk-cpsc.github.io/cpsc100-course/lectures/lecture01/) |
| 2 | [Variables, Data Types, and Basic I/O](https://selkirk-cpsc.github.io/cpsc100-course/lectures/lecture02/) |
| 3 | [Operators, Expressions, and the Standard Library](https://selkirk-cpsc.github.io/cpsc100-course/lectures/lecture03/) |
| 4 | [Control Flow; Conditionals](https://selkirk-cpsc.github.io/cpsc100-course/lectures/lecture04/) |
| 5 | [Loops](https://selkirk-cpsc.github.io/cpsc100-course/lectures/lecture05/) |
| 6 | [Strings and Arrays in C](https://selkirk-cpsc.github.io/cpsc100-course/lectures/lecture06/) |
| 7 | [Midterm 1 Review](https://selkirk-cpsc.github.io/cpsc100-course/lectures/lecture07/) |
| 8 | [Functions and Scope Part 1: Functions](https://selkirk-cpsc.github.io/cpsc100-course/lectures/lecture08-part1/) |
| 8 | [Functions and Scope Part 2: Scope](https://selkirk-cpsc.github.io/cpsc100-course/lectures/lecture08-part2/) |

## Interactive Demos

Each demo steps through a flow diagram one box at a time. As you follow the arrows, you can watch the variables, the output and the trace table change. Use **Next** / **Back**, or the arrow keys.

### Week 4: Branching

| Demo | What it shows |
|---|---|
| [Grade Classifier](https://selkirk-cpsc.github.io/cpsc100-course/demos/grade-classifier/) | Follow a score through an `if` / `else if` / `else` chain of diamonds. Swap the order of the tests to see why the strictest boundary must come first. |

### Week 5: Loops

| Demo | What it shows |
|---|---|
| [While Loop](https://selkirk-cpsc.github.io/cpsc100-course/demos/while-loop/) | Print the numbers from `num` up to 9. The test comes before the loop body, so the body can run zero times. |
| [Do..While Loop](https://selkirk-cpsc.github.io/cpsc100-course/demos/do-while/) | Keep asking for a menu option until the user picks 1 to 4. The loop body always runs at least once. |
| [Nested Loops](https://selkirk-cpsc.github.io/cpsc100-course/demos/nested-loops/) | An inner loop inside an outer loop. Watch the output grid fill one row at a time as `inner` resets for every row. |

### Week 6: Strings and Arrays

| Demo | What it shows |
|---|---|
| [Letter Counter](https://selkirk-cpsc.github.io/cpsc100-course/demos/count-letter/) | Walk a string one index at a time until the `'\0'` terminator, counting how many times a letter appears. |
| [Palindrome Checker](https://selkirk-cpsc.github.io/cpsc100-course/demos/palindrome/) | Move two indices, `left` and `right`, inward from both ends of a word, and use `break` to stop at the first mismatch. |
| [Array Index Explorer](https://selkirk-cpsc.github.io/cpsc100-course/demos/array-index/) | Read and write `marks[i]` for any index. C doesn't check bounds, so an out-of-range index quietly reads or overwrites a neighbouring variable. |
| [2D Array](https://selkirk-cpsc.github.io/cpsc100-course/demos/2d-array/) | Walk a 2D grid with a nested loop and watch each element light up in both the grid view and the single strip of memory C really uses (row-major order). |

### Week 7: Midterm 1 Review

| Demo | What it shows |
|---|---|
| [Tracing a Loop](https://selkirk-cpsc.github.io/cpsc100-course/demos/review-loop-trace/) | A new loop to trace, built like Problem 4: multiples of 3 are subtracted from `total`, other values of `i` add 2. Fill in your trace table on the page and it checks each row as the program reaches the test. Change the loop limit to see the body run zero times. |
| [Tracing Nested Loops](https://selkirk-cpsc.github.io/cpsc100-course/demos/review-nested-trace/) | New nested loops to trace, built like Problem 7: the inner loop starts at `j = i`, and each run adds `i` (not `j`) to `sum`. Fill in your trace table on the page and it checks each row as the program reaches the `sum` box. |

### Week 8: Functions and Scope

| Demo | What it shows |
|---|---|
| [Changing a Copy](https://selkirk-cpsc.github.io/cpsc100-course/demos/add-one/) | `main()` passes `x` to `addOne()`, which adds one to its parameter `n`. Watch `n` become 6 while `x` stays 5: the function only ever had a copy. |
| [Each Call Gets Its Own Variables](https://selkirk-cpsc.github.io/cpsc100-course/demos/scope-calls/) | `add_ten()` and `add_hundred()` both have a local `x`. Watch a new box of variables appear for each function call and disappear when it returns, so a second call to `add_ten()` starts over at 0. |
| [Scope Explorer](https://selkirk-cpsc.github.io/cpsc100-course/demos/scope-explorer/) | Run the lecture's scope examples one line at a time and watch each call's variables appear and disappear. Click any variable to shade every line where it can be used, or to see why a use is out of scope, including a loop's block scope. |
| [Ordinary Local vs. static](https://selkirk-cpsc.github.io/cpsc100-course/demos/static-local/) | Call `count_calls()` three times with `calls` declared `static`, then as an ordinary local. One version counts 1, 2, 3; the other starts over every call. |

### Other Topics

| Demo | What it shows |
|---|---|
| [strcat and the Stack](https://selkirk-cpsc.github.io/cpsc100-course/demos/strcat-stack/) | Two functions take turns using the same stack memory. An uninitialized `greeting` picks up another function's leftover password, and `strcat` adds onto the end of it. Tick the fix to start `greeting` as `""`. |

You can type your own word into the string demos, or your own values into the 2D array demo, to see how the loop behaves.

---

*Notes by Ryan Bradshaw, based on earlier notes by Jonathan Doyle and Tanmay Deshpande. The notes and pages are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) and the code under MIT: see the [licence](https://github.com/selkirk-cpsc/cpsc100-course/blob/main/LICENSE.md).*
