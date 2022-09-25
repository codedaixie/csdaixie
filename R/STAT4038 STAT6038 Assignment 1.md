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

### STAT4038/STAT6038 Assignment 1

(STAT4038/STAT6038)


Assignment 1 for Semester 1, 2022


INSTRUCTIONS:
• This assignment is worth 15% of your overall marks for this course.
• You must complete this assignment by yourself. If you copy someone else’s work or
allow your work to be copied, you will receive a mark of zero for the assignment and
risk very severe academic consequences.
• Your report should be submitted to Turnitin on Wattle as a single pdf document (less
than 25MB) including the following:
1. The assignment cover sheet (available to download from Wattle).
2. Your assignment (no more than 10 pages).
3. An appendix including the R codes you used. Failure to upload the R code will
result in a penalty.
• Assignments should be typed. Your assignment may include some carefully edited R
output (e.g. graphs, tables) showing the results of your data analysis and a discussion
of these results, as well as some carefully selected code. Please be selective about
what you present and only include as many pages and as much R output as necessary
to justify your solution. Clearly label each part of your report with the part of the
question that it refers to.
• Unless otherwise advised, use a significance level of 5%. Round numeric answers to 4
decimal places (e.g., 0.0012).
• Marks may be deducted if these instructions are not strictly adhered to, and marks
will certainly be deducted if the total report is of an unreasonable length, i.e. more
than 10 pages including graphs and tables. You may include an appendix that is in
addition to the above page limits; however the appendix will not be assessed. It will
only be checked if there is some question about what you have actually done.
• Name your report “Course code-Uid”, e.g., “STAT2008-u1234567”.
• Try to submit your assignment at least 15 mins before the deadline in case something
unexpected happens, for instance internet issue.
• Late submissions will NOT be accepted. Extensions will usually be granted on med ical or compassionate
grounds on production of appropriate evidence, but must have
lecturer’s permission at least 24 hours before the deadline.
Assignment 1 - Sem 1, 2022 Page 1 of 3
Question 1 [50 Marks]
The dataset “fat” (available to download from Wattle) contains estimates of the per centage of adipose tissue
(body.fat) and other related measurements taken on a sample
of 252 adult men. The measurements include a derived variable, BMI or body mass
index, which is frequently used as a measure of obesity and is based on simple weight
and height measurements.
For this assignment, we are interested in whether or not BMI, which is relatively easy
to measure, can be used to predict the percentage of adipose tissue (body.fat), which has to be estimated using an underwater weighing technique.
(a) [5 marks] Let “body.fat” be the response variable Y and “BMI” be the predic tor variable X. Conduct an
exploratory data analysis to assess whether the two
variables are associated. Is there a statistically significant correlation between the
variables?
Use the cor.test() function to conduct a suitable hypothesis test. Clearly specify
the hypotheses you are testing and present and interpret the results.
(b) [15 marks] Fit a simple linear regression (SLR) model. Construct a plot of the
residuals against the fitted values, a normal Q-Q plot of the residuals, a bar plot of
the leverages for each observation and a bar plot of Cook’s distances for each obser vation. Use these plots
(and other means) to comment on the model assumptions
and on any unusual data points.
(c) [10 marks] Produce the ANOVA (Analysis of Variance) table for the SLR model
and conduct the F-test based on the output. What is the coefficient of determina tion for this model and how
should you interpret this summary measure?
(d) [10 marks] What are the estimated coefficients of the SLR model in part (b) and
the standard errors associated with these coefficients? Interpret the values of these
estimated coefficients and perform t-tests to test whether or not these coefficients
differ significantly from zero. What do you conclude as a result of these t-tests?
(e) [10 marks] Body mass index values less than 18.5 are typically categorised as “un derweight”; from 18.5
to 25 as “normal”, 25 to 30 as “overweight” and over 30 as
“obese”. Use this SLR model to predict the body.fat percentage for groups of males
with typical BMI values 17.5 (“moderately underweight”), 21.5 (“normal”), 27.5
(“overweight”) and 35 (“obese”), respectively. Find 95% confidence intervals for
these predictions. Do you think this SLR model is a good model for making these
predictions? If you believe this SLR model is not very appropriate, make some sug gestions on how to
improve the model (simply make suggestions, you don’t need
to actually refit the model and produce more outputs).
Assignment 1 - Sem 1, 2022 Page 2 of 3
Question 2 [50 Marks]
Data file “housing.csv” contains data on housing prices in the Seattle area in 2015. The
data have been placed on Wattle. While there are number of variables available, for this
assignment you will only consider the following:
• price: the price that the house was sold at in USD
• bedrooms: the number of bedrooms in the house
• bathrooms: the number of bathrooms in the house
• sqft.living: square footage of total living space
We are interested in whether or not “sqft.living”, square footage of total living space,
can be used to predict “price”, the price of that house.
(a) [10 marks] Let “price” be the response variable Y and “sqft.living” be the predictor
variable X. Is there a linear association between the two variables? You may want
to experiment with some transformations, like the natural log (log()) to one or
both of your variables to assess the linear association. Make a choice at this stage,
for your transformed variables and provide justification for this choice.
(b) [15 marks] With your chosen transformations, fit a simple linear regression (SLR)
model. Construct a plot of the residuals against the fitted values, a normal Q-Q
plot of the residuals, a bar plot of the leverages for each observation and a bar
plot of Cook’s distances for each observation. Use these plots (and other means)
to comment on the model assumptions and on any unusual data points.
(c) [15 marks] Write down the estimated model that you have fitted in part (b). Then
write this estimated model in terms of the original untransformed variables X and Y
(e.g. back-transform the model into the original scale). Based on the mathematical
expression, what happens to b Y when the value of X is multiplied by a factor of k?
Generate a scatter plot of X and Y on the original scale, then add the fitted curve
representing this estimated model in this scatter plot.
(d) [10 marks] Construct the following covariate in R which examines the square foot
of living space per number of bathrooms and bedrooms:
˜X =
sqf t.living
bedrooms + bathrooms + 1
Fit a SLR using ˜X. Use the same transformation for the response as you did in
part (b) (keep ˜X in its original scale). Interpret the model. How do this model
compare to the one in parts (b)?
Assignment 1 - Sem 1, 2022 Page 3 of 3
