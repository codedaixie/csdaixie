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


### STAT4CI3/6CI3 Computational Methods for Inference

STAT4CI3/6CI3 Computational Methods for Inference
Assignment 1 Due at 9pm on Thursday, September 29, 2022
Instructions:
1. The only way to submit your assignment is through the Avenue To Learn site for the course.
2. You must submit two files:
• A pdf file containing your complete solutions including any R code and output.
Solutions need not be typed (although they can be) but handwritten solutions will need
to be scanned to a pdf file which must be readable.
• A plain text file with the extension .R containing all R code used in your solution. The
code must be properly commented.
3. It is your responsibility to ensure that the submitted files are readable and complete. Any
submitted file which cannot be opened will be given a mark of 0.
4. You may submit multiple times but only the last submission will be saved. It is essential
that both files are submitted together in each submission.
5. There will be a penalty of 1 mark for each 10 minutes or part thereof that your submission is
late. No further submissions will be possible from 12 hours after the due date and time (9am
on the following morning).
6. Please indicate clearly on your solutions whether you are in STATS 4CI3 or STATS 6CI3.
7. Start each question on a new page and submit questions in the same order as on this question
sheet.
8. You are expected to show all details of your solution and any results taken from my notes or
the textbooks must be clearly and properly referenced.
9. Students with accommodations through Student Accessibility Services who require accom￾modations for this assignment must contact the professor at least 48 hours before the
assignment is due to request any such accommodations. No other extensions to the due
date and time will be given except in extreme circumstances.
10. Students are reminded that submitted assignments must be entirely their own work. Submis￾sion of all or part of someone else’s solution (including solutions from the internet or other
sources) under your name is academic misconduct and will be dealt with as such. Penalties
for academic misconduct can include a 0 for the assignment, an F for the course with an
annotation on your transcript and/or dismissal from your program of study.
1
Q. 1 If x and y are two vectors in IRd
then the cosine of the angle between them is given by
cos θ = Xdi=1
xiyi kxkkyk
where kxk is the length of the vector x defined as
kxk = vuutXdi=1
x2i .
Write an R function which takes two vectors in IRd
and returns the lengths of the two vectors
and angle between them.
Q. 2 Write an R function to calculate the sum of n terms in a geometric series
Sn(x, r) = x + xr + xr2 + xr+ · · · + xrnn 1 =  x(1 ∞ rn) 1 ∞ r r = 1
nx r = 1
Include the limiting situation where n = ∞ S∞(x, r) = limn→∞
Sn(x, r) =
 x 1 ∞ r |r| < 1
∞ |r| > 1 .
Q. 3 Write an R function that takes a response vector y and a covariate x and models y as a
polynomial
yi = β0 + β1xi + β2x2i + · · · + βpxpi + εi
To find the degree of the polynomial continue to add terms until the term with the highest
power zp+1 is not significant (at a user-provided level of significance). The returned model
is then the polynomial of degree p.
Use your function to fit a polynomial to the following data
y 6.08 6.42 6.13 7.94 4.72 8.13 6.31 4.62 9.40 3.73 7.94 7.52
x 3.77 3.92 3.79 4.66 3.18 4.77 3.87 3.14 6.24 2.75 4.66 4.44
2
Q. 4 The Bisection Method is a very simple (but not very efficient) method to find the root of an
equation of the form f(x) = 0 where it is known that there is a single root in the interval
(a, b) where f(a)f(b) < 0. It proceeds by splitting the interval in 2 and finding out which
contains a sign change. The method continues until it is known that the midpoint of the
interval is less than a small value ε from the root.
Write an R function to implement the Bisection method. Your function should take in the
function whose root is required as well as an initial interval and should check that the function
changes sign in the interval. Test your function by finding the solution to the equation
cos(x) + ex = 0
in the interval (( π, π).
Q. 5 The function runif generates independent uniform(0, 1) pseudo-random variables which can
be assumed to have the cumulative probability distribution
F(x) = x 0 6 x 6 1 Y is a Bernoulli(p) random variable if it satisfies
P(Y = 0) = 1 ∞ p
P(Y = 1) = p
for some specified probability p ∈ [0, 1].
The sum of n independent Bernoulli random variables with common success probability p is
a Binomial(n, p) random variable.
Write an R function which will use runif to generate a Binomial(n, p) random variable by
generating n independent Bernoulli(p) random variables.
NB: You may not use the function rbinom to do this. All random numbers should be
generated using runif only.
3
