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

### COMP2610/COMP6261

Information Theory, Semester 2 2022

Assignment 2
Due Date: Monday 26 September 2022, 5:00 pm
Assignment 2 weighting is 20% of the course mark.
Instructions:
Marks:
1. The mark for each question is indicated next to the question. For questions where you
are asked to prove results, if you can not prove a precedent part, you can still attempt
subsequent parts of the question assuming the truth of the earlier part.
2. COMP2610 students: Answer Questions 1-3 and Question 4. You are not expected to
answer Question 5. You will be marked out of 100.
3. COMP6261 students: Answer Questions 1-3 and Question 5. You are not expected to
answer Question 4. You will be marked out of 100.
Submission:
1. Submit your assignment together with a cover page as a single PDF on Wattle.
2. Clearly mention whether you are a COMP2610 student or COMP6261 student in
the cover page.
3. All assignments must be done individually. Plagiarism is a university offence and will be
dealtwith according to university procedureshttp://academichonesty.anu.edu.au/UniPolicy.html.
1
Question 1: Inequalities [20 marks total]
**All students are expected to attempt this question.
Question 1(a)
Let the average height of a Raccoon is 10 inches.
1. UseMarkov’s inequality to derive an upper bound on the probability that a certain raccoon
is at least 15 inches tall. (You may leave your answer as a fraction.) [3 Marks]
2. Suppose the standard deviation in raccoon’s height distribution is 2 inches. Use Chebyshev’s inequality to derive a lower bound on the probability that a certain raccoon is
between 5 and 15 inches tall. (You may leave your answer as a fraction.) [3 Marks]
Question 1(b)
A coin is known to land heads with probability (?) < 1/6 . The coin is flipped # times for
some even integer # .
1. Using Markov’s inequality, provide a bound on the probability of observing #/3 or more
heads. [3 Marks]
2. Using Chebyshev’s inequality, provide a bound on the probability of observing #/3 or
more heads. Express your answer in terms of # . [3 Marks]
3. For # 2 {3, 6, . . . , 30}, in a single plot, show the bounds from part (a) and (b), as well as
the exact probability of observing #/3 or more heads. [Note: To demonstrate, you can
choose any specific value of p < 1/6. Also, you can choose any plotting tool] [8 Marks]
2
Question 2 : Markov Chain [30 marks total]
**All students are expected to attempt this question.

Question 2(a)
Randomvariables - ,. , / are said to form aMarkov chain in that order (denoted by - ! . ! /)
if their joint probability distribution can be written as:
?(- ,. , /) = ?(-) · ?(. |-) · ?(/ |. )
1. Suppose (- ,. , /) forms a Markov chain. Is it possible for (-;. ) = (-; /)? If yes,
give an example of - ,. , / where this happens. If no, explain why not. [3 Marks]
2. Suppose (- ,. , /) does not form a Markov chain. Is it possible for (-;. ) (-; /)?
If yes, give an example of - ,. , / where this happens. If no, explain why not. [3 Marks]
3. If - ! . ! / then show that [6 Marks]
? (-; /) ? (-;. )
? (-;. |/) ? (-;. )
Question 2(b)
Let - ! (. , /) ! ) form a Markov chain, where by Markov property we mean:
?(G, H, I, C) = ?(G)?(H, I |G)?(C |H, I)
Or simply:
?(C |H, I, G) = ?(C |H, I)
Do the following:
1. Prove that (-;. , /) (-;)). [5 Marks]
2. Find the condition that (-;. , /) = (-;)). [3 Marks]
Question 2(c)
Recall that Markov’s inequality states that if - is a non-negative random variable, for any 0 > 0,
%(- 0) ? E[-]
0
1. Give an example of a non-negative random variable X for which Markov’s statement is
an equality, i.e.for any 0 > 0, [3 Marks]
%(- 0) = E[-]
0
3
2. Given an example of a random variable . (not necessarily non-negative) for which
Markov’s statement reverses, i.e. for any 0 0, [3 Marks]
%(. 0) E[. ]
0
3. Let / be a random variable such that E[/] = 0. Then, for any 0 > 0, Markov’s inequality
tells us that, for any 0 > 0,
%( |/ | 0) ? E[|/ |]
0
while Chebyshev’s inequality tells us that
%( |/ | 0) ? V[/]
02
Is it possible for the bound inMarkov’s inequality to be tighter than that from Chebyshev’s
inequality for some 0 > 0, i.e. does there exist a / and 0 > 0 such that [2 Marks]
E[|/ |]
0
<
V[/]
02
?
If yes, provide an example of a random variable / and a number 0 > 0 for which this is
true. If no, provide a proof that this is impossible. [2 Marks]
4
Question 3: AEP [25 marks total]
**All students are expected to attempt this question.
Let - be an ensemble with outcomes A- = {h, t} with ?? = 0.8 and ?C = 0.2. Consider
-# - e.g., # i.i.d flips of a bent coin.
a) Calculate (-). [3 Marks]
b) What is the size of the alphabet A-# of the extended ensemble -#? [3 Marks]
c) What is the Raw bit content 0(-4)? [4 Marks]
d) Express Entropy (-# ) as a function of N. [5 Marks]
e) LetSX be the smallest set of #-outcome sequences with %(x 2 SX) 1X where 0 ? X ? 1.
Use any program language of your choice to plot 1# X (-# ) (‘Normalised Essential Bit
Content’) vs X for various values of # (include some small values of # such as 10 as
well as large values greater than 1000. Describe your observations and comment on any
insights. [10 Marks]
5
Question 4: AEP [25 marks total]
**Only COMP2610 students are expected to attempt this question.
Let - be an ensemble with alphabet A- = {0, 1} and probabilities ( 25 , 35 )
a) Calculate (-). [3 Marks]
b) Recall that -# denotes an extended ensemble. What is the alphabet of the extended ensemble
-3? [2 Marks]
c) Give an example of three sequences in the typical set (for # = 3, )#V = 0.2). [5 Marks]
d) What is the smallest Xsufficient subset of -3 when X = 1/25 andwhen X = 1/10 ? [5 Marks]
e) Suppose # = 1000, what fraction of the sequences in -# are in the typical set (at V = 0.2)
? [7 Marks]
f) If # = 1000, and a sequence in -# is drawn at random, what is the (approximate) probability
that it is in the # , V-typical set? [3 Marks]
6
Question 5: AEP [25 marks total]
**Only COMP6261 students are expected to attempt this question.
Suppose a music collection consists of 4 albums: the album Alina has 7 tracks; the album
Beyonce has 12; the album Cecilia has 15; and the album Derek has 14.
1. How many bits would be required to uniformly code:
(a) all the albums? Give an example uniform code for the albums. [3 Marks]
(b) only the tracks in the album Alina. Give an example of a uniform code for the tracks
assuming they are named “Track 1”, “Track 2”, etc. [3 Marks]
(c) all the tracks in the music collection? [2 Marks]
2. What is the rawbit content required to distinguish all the tracks in the collection? [2 Marks]
3. Suppose every track in the music collection has an equal probability of being selected.
Let denote the album title of a randomly selected track from the collection.
(a) Write down the ensemble for – that is, its alphabet and probabilities. [2 Marks]
(b) What is the raw bit content of 4? [2 Marks]
(c) What is the smallest value of X such that the smallest X-sufficient subset of 4 contains
fewer than 256 elements? [2 Marks]
(d) What is the largest value of X such that the essential bit content X (4) is strictly
greater than zero? [2 Marks]
4. Suppose the album titles ensemble A is as in part (c).
(a) Compute an approximate value for the entropy () to two decimal places (you may
use a computer or calculator to obtain the approximation but write out the expression
you are approximating). [2 Marks]
(b) Approximately how many elements are in the typical set )#V for when # = 100 and
V = 0.1? [3 Marks]
(c) Is it possible to design a uniform code to send large blocks of album titles with a 95%
reliability using at most 1.5 bits per title? Explain why or why not. [2 Marks]
