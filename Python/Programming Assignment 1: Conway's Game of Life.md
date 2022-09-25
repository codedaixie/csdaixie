## Panda学长CS代写
**创始于北美 ｜专注cs全科代写 ｜ 100%原创MOSS查重**

**Panda学长**代写各类程序语言* *: C语言代写, C++代写, 算法作业代写, 数据结构代写, AI/MachineLearning代写, python代写, java代写, matlab代写, 汇编代写, scala代写, SQL/Database代写, racket代写, 安卓/Android代写, IOS/swift代写, racket代写, 网络代写, web代写, OS/操作系统代写, R代写* *

**为什么选择Panda学长CS代写？**

- 我们有经验丰富学历强大的**代写老师**，均毕业于常青藤/清华/北大/北航等顶级CS专业，大部分都是TOP ACMer、LeetCoder, 最快24-48小时即可完成，用技术和耐心帮助客户高效高质量提交作业。
- 我们**价格公道**，绝无高昂的中介费(比中介会便宜很多) 
- 我们的老师都是互相认识的好伙伴，有严格的评价机制，三次差评团队成员就要**强制退出**
- 我们的客服也是由**代写老师轮流担任**，在20分钟内准确高效的评估作业时间和难度，完成后团队有专人负责代码审计。相比于黑中介和个人代写不靠谱，我们团队让您的作业拿到更多分数
- **无限期售后服务**，真正的一站式无忧服务
- 专注留学生编程作业代写,起步于北美，cs业务遍及全球英语国家: [北美CS代写](https://github.com/codedaixie/csdaixie),[美国CS代写](https://github.com/codedaixie/csdaixie),[英国CS代写](https://github.com/codedaixie/csdaixie),[加拿大CS代写](https://github.com/codedaixie/csdaixie),[澳洲CS代写](https://github.com/codedaixie/csdaixie),[新西兰CS代写](https://github.com/codedaixie/csdaixie),[新加坡CS代写](https://github.com/codedaixie/csdaixie),[香港CS代写](https://github.com/codedaixie/csdaixie)

Please feel free to contact us anytime！

**客服24h咨询方式     **微信：cube787**


<img src='https://github.com/codedaixie/csdaixie/blob/main/image/down.png'>
<img src='https://github.com/codedaixie/csdaixie/blob/main/image/logo.png' width='85%'>
### Programming Assignment 1: Conway's Game of Life
### CSE 220: Systems Programming
**Introduction
In this project youwill implement a simplified version of JohnHorton Conway’s Game of Life. The Game of Life
is a particular model of cellular automaton, which is a method of modeling certain computations and interactions. Cellular automata theory is outside the scope of this class, but we can still explore this model.
The Game of Life models an infinite grid of cells, in which every cell is either alive or dead. A simple and
deterministic set of rules is used to step through generations of these cells by determining whether, from one
generation to the next, a particular cell lives on, dies, or creates life. We will simplify this model by placing it
on a finite grid, but otherwise following the rules of the Game of Life.
Conway’s Game of Life is a well-studiedmodel, as it exhibits some interesting properties. In fact, it has been
proven that the Game of Life is computationally Turing complete, meaning that any computation that can be
modeled by a digital computer can be performed by developing the correct starting position in the Game of
Life and iterating until the desired result is computed as a pattern of cells.
This assignment will give you practice dealing with C arrays and references to arrays, including multidimensional arrays. It will give you practice in separating repeated computations out into functions. It will
introduce the concept of modifying a program’s data model to simplify computation.
Likemany real-world problems, this assignmentwill bemostly either entirely correct or entirelywrong. There
will be a limited opportunity to get partial credit by following the instructions for output format closely even
if your game is not capable of correct deterministic operation, but because errors in early generations will lead
to rapid degeneration in later generations, correct operation is critical for significant credit.
This document is long, but there is a reason for that. Please read it carefully and in its entirety before
starting your assignment!
You will have two weeks to complete this project.
InMemoriam
John Conway passed away in April of 2020 of complications from COVID-19. The Game of Life, while
possibly
his most well known creation, is far from his only contribution to mathematics or computation.
The following Life input is attributed to RandallMunroe, author of theXKCDweb comic. Following the rules
in this document, it transforms into a “glider” that departs the disintegrating body and flies off to the upper
right. In our implementation, it becomes a “block” still life (you can find these terms defined in the resources
linked later in this document), but in a complete implementation of Life it travels forever, upward and to the
right, for an infinite distance. You can find it as the input file inputs/conway.life in the given code.
Rest in peace, John Horton Conway, 1937–2020.
1 Getting Started
You should read this entire handout and all of the given code before you get started. You should have
received
a GitHub Classroom invitation for this project. Follow it and check out the resulting repository.
1
It is probably best to read a good description of the Game of Life as your first step. I recommend the
Wikipedia Article as a good starting point.
Some other good resources include:
ConwayLife.com, a community for people exploring the Game of Life and its properties
The LifeWiki, which contains an enormous amount of interesting and helpful information
2 Requirements
You are required to implement the rules of Conway’s Game of Life, with the change that all cells not displayed
in the required viewport are always considered dead.
Your program must compute the rules of the Game of Life on a grid that is 80 cells wide by 24 cells high,
assuming that all cells outside of this grid are dead. These constants are defined in the given file life.h as
GRIDX
anad GRIDY, respectively.
The rules of Life are simple, and applied to every cell in the grid in the exact same fashion. Life proceeds in
generations, where the state of the cells in generationG entirely determines the state of the cells in generation
G + 1. The state of each cell in generation G + 1 is determined by the state of its eight neighboring cells in
generation G; specifically, the number of those cells that are alive or dead. The neighbors of a cell are the
cells
immediately to its left, right, and on the four diagonals between those cells. The rules for a cell c are as
follows:
If c is alive and has fewer than 2 live neighbors, it dies.
If c is alive and has more than 3 live neighbors, it dies.
If c is alive and has exactly 2 or 3 live neighbors, it remains alive.
If c is dead and has exactly 3 live neighbors, it becomes alive.
The neighbors of the cell marked in the center of this grid are the cells marked in gray:
X
Your implementation will use the character 'X' to represent a live cell, and the space character ' ' to represent a dead cell. There are two constants defined in the given code, LIVE and DEAD, for this purpose.
Your implementation must accept two command line arguments, a filename and a generation number. The
filename is a file containing a starting state to be passed to the given function parse_life() (documented elsewhere in this handout), which will produce a grid with the initial state of the game, and the generation number
is the generation which your program should output. Generation 0 is the starting state of the game as parsed
by parse_life().
Upon reaching the stated generation, your program must output the state of the grid, using exactly the
format described here. Any difference in format, including extra or missing whitespace, will result in reduced
credit on this assignment. The grid should be output as follows:
Every row of the GRIDY rows in the grid must be output as a single line of text ending in a newline.
Every cell of the GRIDX cells in a row of the gridmust be output as a single character, either an ASCII space
for a dead cell or an ASCII X for a live cell.
Your output will therefore be exactly 24 lines of exactly 80 characters each. Any deviation from this output
is incorrect. In particular, extra whitespace at the beginnings or ends of lines, for example, will look like extra
dead cells.
Any invocation with fewer than one argument or more than two arguments should print an error message
and exit (e.g., return from main()) with a non-zero exit status, with one exception: you may accept extra arguments beginning with a dash (-) character to enable different behaviors in your program for your own use in
testing.
2
3 Given Code
You are given a significant quantity of code, but it all essentially boils down to three things:
Reading starting positions from files on disk
Clearing the terminal
Constants
There are extensive comments in the given code to help you understand what you have been given.
You can find a parser for starting positions expressed in three common formats in src/parser.c. You do
not need to read and understand this file, but you may find it helpful for your understanding of C and your
development as a programmer to read through it. It solves real problems in practical ways. You do need to
understand how to use the function parse_life(), which has a comment block describing its usage. Simply
speaking, it takes a filename as an argument (such as would be passed to your program as argv[1]) and
returns
a 24 row by 80 column matrix of char cells that are either LIVE or DEAD, as appropriate.
There is also a function, clearterm(), that clears the terminal screen. You can use this alongwith your output
code and the function usleep() to produce animations for testing. (See Section 4.2 for more information.) This
function takes no arguments and returns no value.
Several constants are defined for you, as well. They are;
GRIDY: The number of rows in your grid of cells
GRIDX: The number of columns in your grid of cells
LIVE: The “live” cell character, 'X'
DEAD: The “dead” cell character, ' '
All of the given functions and constants are defined in the file src/life.h. This file is already included in
src/main.c, where you should place your main function and begin your implementation.
You should not need to change any of the given code, although youmay do so if you like. I do not recommend
this.
You may create as many source files as you need in the source directory, but you must add their filenames
to the SOURCEFILES variable in the Makefile or they will not be correctly submitted to Autograder.
4 Testing
Due to the nature of this program, debugging and testing can be tricky; in particular, errors from generation to
generation can be difficult to isolate without voluminous output. I recommend several techniques for tackling
testing and debugging in this assignment:
Compute generational changes on paper or in an image editor. It can be difficult to determine whether a
particular evolution is correct or not just by looking. In my implementation, I drew and computed a number of
Life states by hand and compared them to my program’s output.
In general, if you try to do this projectwithout jotting down indices, calculations, portions of the grid, etc. on
paper, youwill probablywaste a lot of time looking for trivial one-off errors, computations that are accidentally
rotated in the matrix, and the like. Don’t be afraid to write things down!
Output internal state to files or standard error— or just alongside the normal output. We have not talked
much about output to anything but the normal terminal output, but there are two separate output streams to
the terminal, standard output and standard error, that enable you to separate normal program output from
errors and debugging. You can print to standard error using fprintf(stderr, format, ...), which takes a format
string like printf() but outputs it slightly differently. We will cover the details another time, but in particular
it will allow you to output debugging information without breaking the checks performed by make test.
3
You can also open files using fopen() and write to them using functions like fprintf(). You need not dig into
this now if you don’t want to, but it is discussed in Chapter 7 of K&R.
Youmight, for example, want to output both the normal generational output and a neighbor count for every
cell in a generation. I found this particular information very handy in debugging my implementation.
Note that your final submitted projectmust not produce spurious output on either standard output or standard error, or it will not receive full credit.
Use a variety of test inputs. The given code has several example inputs in inputs/, as well as expected
outputs
that they can be checked against in outputs/. You can perform some automated checks using make test, but
there
are inputs not tested in inputs/, and you may wish to fetch additional inputs from one of the Life web sites in
Section 1, or even draw your own. You can easily draw states in the Life 1.05 format, which is described on
the
LifeWiki and an example of which is in inputs/tumbler.life.
Testing your project thoroughly is key to receiving full credit on this project. In particular, make sure you
test the life-and-death behavior of cells around the border of the grid, as the final Autograder will certainly test
this.
4.1 Useful Life Constructions
There are two classes of test inputs which are likely to be particularly useful to you: still lifes and oscillators.
A still life is a pattern that does not change at all from generation to generation. An example pattern, the
block, can be found in inputs/block.life. It consists of four live cells in a rectangle configuration. An oscillator
is a pattern that repeats itself on some fixed interval. One of the simplest possible oscillators, the blinker,
is provided in inputs/blinker.rle. It repeats itself every other generation, forming a short vertical line in one
generation and a short horizontal line in the next.
You will want to look at some of the patterns available on the LifeWiki, which has categories for both still
lifes and oscillators. These patterns are valuable for testing because they have known, sometimes non-trivial,
behaviors.
4.2 Animation
While you are not required to do so to receive full credit, I recommend that you implement an
“animationmode” in
your program. If it is started with only one argument, it should display generations on the terminal, one after
another, with a brief pause between. You can accomplish this by drawing one generation, calling the usleep()
function to sleep for 300-500ms (usleep()’s argument is in microseconds, so use 300000 or 500000) after
each
generation, then calling the given function clearterm() before drawing another.
In combination with hand-computing generations or comparing against known oscillators or still lifes
found on the LifeWiki, this can help you isolate bugs in your generational computations. It’s also just plain
fun to watch!
4.3 Given Tests
You have been given several input files along with pre-computed expected outputs. You can compare your
program’s execution against these files using the command make test from the top-level source directory, or
you can run your program and compare the outputs yourself. Careful examination of the recipe for make test
should reveal how to write similar tests yourself. I will provide a working implementation of the life program
that you can use to produce outputs against which you may compare your program’s behavior on inputs of
your own choosing, as well.
4.4 Achieving Full Credit
If you test your solution with only the given tests, you will almost assuredly not receive full credit on this
assignment.
In particular, the given tests dominimal-to-no checking for the life-and-death status of cells around the border
of the grid (see Section 5.6, below). In this and in all other assignments in this course, you are expected to
create
and run tests on your own. The links at the top of this document provide a rich source of test cases.
4
5 Guidance
The guidance in this section is intended to help you successfully complete this project correctly and in a
timely
manner. You are not required to use any particular data representation or any particular implementation techniques. However, the advice here is borne out of years of experience writing non-trivial programs.
5.1 X- or Y-outer Dimensions
Your matrices can be defined with their outer dimension being either the X or Y dimension. However, the
parse_life() function returns a matrix with an outer Y dimension, and it is convenient to print matrices to the
screen using an inner X dimension, so I recommend that you declare your state matrices to have an outer Y
dimension and inner X dimension.
5.2 AlternatingMatrices
Because each generation of the Game of Life is dependent only on the previous generation, it is convenient
and
efficient to perform all computations on two identical matrices. Onematrix represents the current generation,
and the other represents the next. After each generation, the roles of the two generations will swap.
This can be conveniently accomplished by declaring a three-dimensionalmatrix, where the third dimension
is 2, as follows:
char grids [2][Y][X];
This represents twomatrices with an outer Y dimension of X and an inner X dimension of Y. In generation 0,
grids[0]would be used as the current generation, and the next generation computed on grids[1]. In generation
1, their roles would swap. The roles can be easily swapped using the modulus operator, %. For example:
current = 0;
for (int current = 0; ; current = (current + 1) % 2) {
/* Do something */
}
Note that the calculation before the modulus operator must be parenthesized. The value of current will
alternate between 0 and 1 in every iteration of this loop.
5.3 Matrices with Borders
Since your implementation is required to compute its visible field as if every cell outside of the field is dead, it
may be convenient to place a border of dead cells around the GRIDY by GRIDX matrix and never recompute
those
cells to avoid having to deal with computing the cells around the border of your matrix with special cases. My
implementation computes every cell using exactly the same functionwith no conditionals for cells at the edges
of the matrix.
Remember if you do this that your internal matrices will have to be of size GRIDY + 2 by GRIDX + 2, and that
you will recompute the sub-matrix from [1][1] to [GRIDY][GRIDX] (assuming you use Y as our outer
dimension).
5.4 I/O
As mentioned in Section 4, you can find documentation for the C standard I/O library in Chapter 7 of K&R.
However, even if you do not read this chapter, there are some functions you may want to be aware of (and
may
want to read the man pages for):
putchar(): This outputs a single character
printf(): We’ve seen this before, but it’s very flexible in ways we have not yet explored
fwrite(): You can fwrite() to the FILE * named stdout to write a specified number of bytes to your program’s
output
5
5.5 Using Functions
You will probably want to define several functions that operate on matrices. You can declare a function to take
a two-dimensional matrix by defining an array argument with specified dimensions. Note, however, that you
cannot pass the output of parse_life() in this fashion, as it does not return a true two-dimensional matrix (for
reasons we will discuss later). A function accepting a matrix as an argument might be defined as:
void use_matrix(char grid[Y][X]);
Note that both the Y and X dimensions are specified in this definition. Remember that youmust specify all
dimensions except the outermost, and that youmay specify even the outermost, when usingmulti-dimensional
arrays in this fashion.
Example functions that you should consider implementing are:
? A function to compute the number of neighbors of a given cell
? A function to compute the next generation
? A function to output the state of your grid of cells
In general, if a function is more than a couple of dozen lines long, you should consider whether it can be
divided up. Sometimes it cannot, or it is not worth it, but often ways can be found to separate out bits of logic
in a way that simplifies the overall implementation.
5.6 Likely Problem Areas
The singlemost likely problem in your implementation is miscalculation around the edges of thematrix and in
the corners. If you choose to use the border of dead cells described in Section 5.3, then this problem is
greatly
reduced. The next most likely concern is miscalculation of the number of neighbors due to counting the cell
itself.
6 Submission
To create a submission tarball to be uploaded to Autograder, run the command make submission from your
Git
workspace. This will generate the file life.tar, which you should upload to Autograder.
Remember to run make submission before every submission to ensure that you are submitting yourmost
recent
code, and make sure that you are submitting the correct file. Many students have problems when they submit
something from a previous project, and cannot figure out why their project won’t build!
7 Grading
This assignment is worth 5% of your course grade. Points for this project will be assigned as follows:
Points Description
2 Handout quiz (will not be represented on Autograder)
2 life exits with an error message when invoked with invalid arguments
4 life 0 correctly outputs the starting state (generation 0) for arbitrary input files
4 life correctly computes the given blinker and pulsar oscillators through their
entire periods
8 life correctly computes automata over many generations
This project will be worth 5% of your final course grade, including the handout quiz (which is 0.5% of your
final course grade, or 10% of this assignment). The Autograder provided to you will not evaluate all 18 points
for correctness, and you are responsible for testing your project thoroughly. It will be possible to receive full
credit on the Autograder and substantially less than full credit in the gradebook.
**
