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

### QBUS2820 Predictive Analytics Individual Assignment 1

QBUS2820 Predictive Analytics
Individual Assignment 1
Key information
1. Required submissions (through Canvas/Assignments/Individual Assignment 1)
a. ONE written report (word or pdf format)
b. ONE Jupyter Notebook .ipynb
Please upload both files to canvas in the SAME submission, as separate files (NO
zip file).
2. Due date/time and closing date/time: See Canvas. The late penalty for the
assignment is 5% of the assigned mark per day, starting after 23.59pm on the due
date.
3. Weight: 30% of the total mark of the unit.
4. Length: The main text of your report should have a maximum of 10 pages with the
usual font size 11-12. You should write a complete report including sections such as
business context, problem formulation, data processing, Exploratory Data Analysis
(EDA), methodology, analysis, conclusions and limitations, etc.
5. If you wish to include additional material, you can do so by creating an appendix.
There is no page limit for the appendix. Keep in mind that making good use of your
audience’s time is an essential business skill. Every sentence, table and figure have
to count. Extraneous and/or wrong material will reduce your mark no matter the
quality of the assignment.
6. Anonymous marking: As the anonymous marking policy of the University, please
only include your student ID in the submitted report, and do NOT include your
name. The file name of your report and code file should follow the following format.
Replace "SID" with your Student ID. Example: SID_Qbus2820_Assignment1.
7. Presentation/clarity is part of the assignment. Markers will allocate 10% marks for
clarity of writing and presentation. Numbers with decimals should be reported to
the fourth decimal point.
Key rules:
Carefully read the requirements for each part of the assignment.
Please follow any further instructions announced on Canvas.
You must use Python for the assignment. Use "random_state= 1" when needed, e.g.
when using “train_test_split” function of Python. For all other parameters that are not
specified in the questions, use the default values of the corresponding Python
functions.
Reproducibility is fundamental in data analysis, so that you will be required to submit a
Jupyter Notebook that generates your results. Not submitting your code will lead to a
loss of 50% of the assignment marks.
The notebook must run without errors and produce results consistent with the report
when accessed through Kernel -> Restart & Run All from the Jupyter menu, assuming
that the train and test datasets are in the same folder as the notebook. Failure to do so
can results in a loss of up to 50% of the assignment marks.
Failure to read information and follow instructions may lead to a loss of marks.
Furthermore, note that it is your responsibility to be informed of the University of
Sydney and Business School rules and guidelines, and follow them.
The Task
You will work on the Houses Data set. This is a dataset about residential property sales in
the US, gathered from 2006 to 2010. The dataset consists of multiple variables measuring
properties of the houses.
The assignment consists of applying models and model selection methodologies to arrive at
models that predict the price of the sale of the houses, given some of the other variables
measured.
1. Problem description
A primary goal of finding a model that is accurate in predicting the prices of the houses
when they are sold. The accuracy of the predictions is measured in Mean Absolute Error
(MAE).
A secondary goal is to get an understanding of which are the main factors that drive prices,
according to the model, this would require that at least one of the models uses a few
variables or that you can create a coherent explanation out of one of the models if all use
many variables.
Select three models, one from each model family to predict the target variable 'SalePrice’.
These model families are:
a linear regression model,
a kNN regression model,
A third model. This model can be any model of your choice that is not linear
regression nor kNN (might even be a model not covered in the QBUS2820 unit). This
is to encourage you to self-explore and self-study, since the ability of self-study is
critical in the field of machine learning which is evolving rapidly.
All the models need to be fine-tuned with hyperparameter search (when appropriate) and
potentially variable selection. The methodology should maximize the predictive accuracy
and the. When the three models have been tuned, you will compute an accurate estimate
of the prediction error of these models and make a final decision among the three. In the
conclusions, you also have to give an explanation of the driving factors of house prices, if
the chosen model is not explainable, then use another (or several) and carefully justify the
tradeoffs.
The model selection exercise:
intro/business context/problem formulation
3
exploratory data analysis
The three models
The conclusions section
Represents the main body of the report and makes 85% of the grade of the assignment.
In addition to the model selection above, the following short exercises. Create a section for
each of the questions and remember to explain and discuss the methodology in the report
as in the main body.
(5%) Find the best predictive model that uses a single predictor (only one variable).
(5%) Instead of optimizing for the mean absolute error, how would you change your
methodology to optimize for the median error? This is a theoretical question,
answer with a proposed methodology, no need to code it in the notebook.
Select 3 houses at random from the dataset and:
(5%) Predict sale prices for those three houses for the year 2022. Reason your
answer. You can use any of the three candidate models or use a new model.
Bonus question: Approximate bias and variance of the selected of the Expected Prediction
Error of the more accurate model chosen in the main body of the report. The
approximation is for a dataset of 70% size of the original dataset. Comment on the
limitations of your solution. The bonus exercise is an extra 5% on top of the grade of the
assignment, it can be used to counteract errors but cannot make the total grade for the
assignment over 100%.
The main marks come from the report, this is you can have a ‘perfect’ notebook but
if there is no explanation if the report then it will not be given marks.
Always give a reasoned answer, why do you chose a particular variable selection
method and not other? Why did you choose a particular ‘third’ model? Why did you
choose a particular method for estimating the errors? Etc.
You do not need to ‘re-state’ the properties of the models, but need to critically
justify what the models are adding to the analysis what are the benefits to those
models and the drawbacks. The same goes for other decisions in the
You might need to make ‘suboptimal’ decisions due to, for example, computation
times, failure to meet assumptions of the models, etc. In this case remember to
state the reason for the decision and the potential problems.
The grading of the assignment will be based on the methodology and justifications,
removing points for methodological errors, incomplete sections, etc. There is no ‘minimum’
predictive accuracy to be reached, but you need to apply a good methodology.
The dataset is a popular one in data analysis, described in:
https://doi.org/10.1080/10691898.2011.11889627
or http://jse.amstat.org/v19n3/decock.pdf
It is used in a practice Kaggle competition:
2. Written report
The purpose of the report is to describe, explain, and justify your solution. Be concise and
objective. Find ways to say more with less. When in doubt, put it in the appendix. Below are
some guidelines on how to work on the Task.
Preparation. You read and understood the assignment requirements and are aware that
this is part of the assessment. You understand that machine learning is grounded in
rigorous logic and theory that should inform your practical analysis. You understand that
there is no single right solution and that trying different approaches and discovering
empirically what works best for a particular problem is natural and desirable in this type of
analysis.
Business context and problem formulation. The report includes a discussion of the context
for the analysis, the problem and questions/hypotheses to be addressed, and how you plan
to measure the success of your proposed solutions.
Data processing. You make sure that the dataset is free of errors and correctly processed
for your analysis. You handle missing values and other issues appropriately. You describe
the data processing steps in a clear and concise way.
Exploratory data analysis (EDA). Your report describes your EDA process, presenting only
selected results. You studied key variables individually. You note any features of the data
that are relevant for model building (some variables might be ‘invalid’ for predictive
purposes). You note the presence of outliers and any other anomalies that can affect the
analysis. You explain the relevance of the EDA results to your subsequent modelling. Your
EDA section in the report is concise, leaving additional figures and tables to the appendix if
needed. Outliers should be clear (e.g. negative values for counting variables). EDA is not the
place to do variable selection and outliers of a non clear nature (e.g. very large values)
should be either not removed or further analyzed using the predictive model performance.
The dataset has many variables and you are not expected to report on all of them
individually, just report your methodology and main findingd.
Variable selection. You describe and explain your process for variable selection. Your
choices are justified by data analysis and/or trial and error. Other that potentially invalid
variables from the dataset, the decision should be driven by the performance of the models,
not based on opinions (you are free to comment on the disagreements between your
background knowledge and the models).
Methodology and modelling. You clearly describe and justify the models, methods, and
algorithms in your analysis. The choice of methods is logically related to the assignment
requirements, the substantive problem, underlying theoretical knowledge, and data
analysis. This may involve systematic trial and error, but the report should focus on your
final solutions. Your methodology pays attention to statistical variability. You report all
5
crucial assumptions and check them as relevant via formal and informal diagnostics. You
clearly recognize when an assumption is not satisfied or questionable. Some problems may
be unfixable given the available data and methods. In this case you can identify what
additional information or methodology could allow you to fix these problems.
Analysis and conclusions. Your analysis is rich. You correctly interpret the results and
discuss how they address the substantive question. The reasoning from methodology and
results to your conclusions is logical and convincing. You are not misled by overfitting. Your
analysis pays attention to statistical variability. You make no claims for which you have no
evidence. You do not make statements that imply causation when discussing associations.
You explicitly acknowledge when limitations of the data or methods lead to uncertainty
about your answer to the substantive question.
Writing. Your writing is concise, clear, precise, and free of grammatical and spelling errors.
You use appropriate technical terminology. Your paragraphs and sentences follow a clear
logic and are well connected. There is a clear distinction between the essential parts of the
report and less important material (use the appendix). Your text refers to meaningful names
for variables and subjects. If you use an abbreviation or label, you first have to define it.
Report. Your report is well organized and professionally presented and formatted, as if it
had been prepared for a client later in your career. There are clear divisions between
sections and paragraphs.
Tables. Your tables are appropriately formatted and have a clear layout. The tables have
informative rows and column labels. The tables are as much as possible easy to be
understood on their own (in the real world, a significant part of your audience will skim-read
by going straight to the tables). The tables do not contain information which is irrelevant to
the discussion in your report. Your table is not an image. The tables are placed near the
relevant discussion in your report. There is no text around your tables.
Figures. Your figures are easy to understand and have informative titles, captions, labels,
and legends. The figures are well formatted and laid out. The figures are placed near the
relevant discussion in your report and are references from the text of the report. Your
figures have appropriate definition and were directly saved from Python into an image file
format. There is no text around your figures.
Numbers. All numerical results are reported to four-decimal point.
Referencing. You add citations for your sources. The references follow a recognizable style
(e.g. the Harvard Referencing System, MLA, APA, Vancouver, etc.)
Python code. The code is presented in a neat and compact way. The code uses meaningful
variable names and can be easily followed by someone with training in Python and statistics.
Someone should be able to run your code and reproduce all the results that appear in your
report. Your code has comments that clearly indicate which parts correspond to which
sections of your report. You explicitly acknowledge when you borrow pieces of code from
sources other than the lecture and tutorial materials.
