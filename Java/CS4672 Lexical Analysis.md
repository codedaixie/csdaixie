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


### CS4672 Lexical Analysis

Requirement

Your task is to develop a Lexer (aka Scanner) for the programming language whose lexical structure is described in this document:

This document is shared with UF affiliates only, so you will need to log into google with your Gatorlink ID. Please do NOT send requests for permission for access from another google account.

Provided Code
ILexer.java
Interface for the Lexer itself, your lexer class should implement this interface
IToken.java
Interface for the Tokens, your token class should implement this interface. Also, the enum Kind, which distinguishes the different tokens is defined in this interface. When determining the position of a token in the input source code, start counting both lines and columns at 1.
CompilerComponentFactory.java
Factory class to provide instantiations of your lexer. You will need to modify a line or two in this class.
PLCException.java
The superclass of all the Exceptions that we will throw in the compiler
LexicalException.java
The Exception that should be thrown for all errors in the input that are discovered during lexing.
LexerTests.java
Example Junit tests. This class will be expanded with additional tests and used for grading so it is essential that your code runs with this code and passes these tests. The examples also demonstrate how to write tests, including tests where an exception is expected. You may (and should!) add additional tests to this class; your version will not be graded.
For you to develop
A class (or classes) that implements the IToken interface and represents tokens.
A class that implements the ILexer interface and tokenizes its input according to the given lexical structure.
repeatedly invoking next() should return all of the tokens in order. After all the tokens have been returned, subsequent calls should return a token with kind EOF.
If an error is discovered, throw a LexicalException. The error message will not be graded but you will appreciate it later if your error messages are informative.
You may implement your lexer so that it generates tokens on demand, or you may compute all the tokens first and then return them when requested. If you choose the latter approach, make sure that no exceptions are thrown until the error occurs. (For example, if the input is “123 @”, the first call to next should return a NUM_LIT token with 123. The second call should throw an exception.) The ERROR kind may be useful for managing exceptions, it is not required to be used and no ITokens with kind ERROR should ever be returned from next() or peek().
Modify CompilerComponentFactory.java so that its getLexer method returns an instance of your ILexer implementing class.
All of your classes for this project should be in package edu.ufl.cise.plpfa22;

Do not modify the provided code except CompilerComponentFactory.java and LexerTests.java.

Turn in
A jar file with containing the Java sources of all the code (including provided code) needed to test your lexer implementation. (Do not include .class files). Name your jar file Lastname0_Lastname1_HW1.jar (or Lastname_HW1.jar if your group only has one member). Note that some IDEs default to including class files, so double check that your jar file contains the source files only.

A zip file containing your git repository WITH its history. The contents will not be graded, but failure to turn it in may result in a zero on the assignment. It may be used in cases of academic dishonesty, to determine contributions of team members, and to evaluate software engineering practices. To obtain this file, go to the parent of your local git repository and create a zip file. Your git repository should contain a (hidden) directory called .git (dot git). Do NOT use the “download zip file” option on github-it does not include the history.

Hints
Study the lexical structure and determine its DFA. Systematically implement the DFA as discussed in class.
Work incrementally, testing as you go.
Avoid static variables as they do not always behave as expected during unit testing.
You may use Integer.parseInt to convert a string to an int value. If a NumberFormatException is thrown, this should be caught and converted to a LexicalException.
Before turning in:
Remove debug printing
Check for and remove extraneous import statements. Unless otherwise specifically indicated, only classes from the standard java distribution should be used. Nonstandard import statements may cause your code to fail to compile on our system, which would result in a zero on the project.
Double check that you have complied with the instructions above.
