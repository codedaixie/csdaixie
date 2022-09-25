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

### COMP4650/6490 Document Analysis – Semester 2 / 2022

**Assignment 2
Due 17:00 on Wednesday 28 September 2022 AEST (UTC +10)
Last updated August 22, 2022
Overview
In this assignment you will:
1. Develop a better understanding of how machine learning models are trained in practice, including
partitioning of datasets and evaluation.
2. Become familiar with the scikit-learn1 package for machine learning with text.
3. Become familiar with the PyTorch2 framework for implementing neural network-based machine
learning models.
Throughout this assignment you will make changes to the provided code to improve or complete existing
models. In some cases, you will write your own code from scratch after reviewing an example.
Submission
The answers to this assignment (including your code files) have to be submitted online in Wattle.
You will produce an answers file with your responses to each question. Your answers file must be
a PDF file named u1234567.pdf where u1234567 should be replaced with your Uni ID.
You should submit a ZIP file containing all of the code files and your answers PDF file, BUT NO
DATA.
Marking
This assignment will be marked out of 15, and it will contribute 15% of your final course mark.
Your answers to coding questions (or coding parts of each question) will be marked based on the quality
of your code (is it efficient, is it readable, is it extendable, is it correct).
Your answers to discussion questions (or discussion parts of each question) will be marked based on how
convincing your explanations are (are they sufficiently detailed, are they well-reasoned, are they backed
by appropriate evidence, are they clear, do they use appropriate visual aids such as tables, charts, or
diagrams).
Question 1: Movie Review Sentiment Classification (4 marks)
For this question you have been provided with a movie review dataset. The dataset consists of 50,000
review articles written for movies on IMDb, each labelled with the sentiment of the review – either
positive or negative. Your task is to apply logistic regression with dense word vectors to the movie review
dataset to predict the sentiment label from the review text.
1https://scikit-learn.org/
2https://pytorch.org/
1
A simple approach to building a sentiment classifier is to train a logistic regression model that uses
aggregated pre-trained word embeddings. While this approach, with simple aggregation, normally works
best with short sequences, you will try it out on the movie reviews.
You have been provided with a Python file dense_linear_classifier.py which reads in the dataset and
splits it into training, testing, and validation sets; and then loads the pre-trained word embeddings. These
embeddings were extracted from the spacy-2.3.5 Python package’s en_core_web_mdmodel and, to save
disk space, were filtered to only include words that occur in the movie reviews.
Your task is to use a logistic regression classifier with aggregated word embedding features to determine the sentiment labels of documents from their text. First implement the document_to_vector function
which converts a document into a vector by first tokenising it (the TreebankWordTokenizer in the nltk
package would be an excellent choice) and then aggregating the word embeddings of those words that exist
in the dense word embedding dictionary. You will have to work out how to handle words that are missing
from the dictionary. For aggregation, the mean is recommended but you could also try other functions
such as max. Next, implement the fit_model and test_model functions using your document_to_vector
function and LogisticRegression from the scikit-learn package. Using fit_model, test_model, and
your training and validation sets you should then try several values for the regularisation parameter C
and select the best based on accuracy. To try regularisation parameters, you should use an automatic
hyperparameter search method. Next, re-train your classifier using the training set concatenated with the
validation set and your best C value. Evaluate the performance of your model on the test set.
Answer the following questions in your answer PDF:
1. What range of values for C did you try? Explain, why this range is reasonable. Also explain what
search technique you used and why it is appropriate here.
2. What was the best performing C value?
3. What was your final accuracy?
Also make sure you submit your code.
Hint: If you do the practical exercise in Lab 3 this question will be much easier.
Tip: If you use TreebankWordTokenizer then for efficiency you should instantiate the class as a global
variable. The TreebankWordTokenizer compiles many regular expressions when it is initialised; doing
this every time youwant to tokenise a sentence is very inefficient. For more details see the documentation3
for TreebankWordTokenizer.
Question 2: GenreClassification (Kaggle competition: 4marks,Write-up: 3marks)
For this task you will design and implement a classification algorithm that identifies the genre of a piece
of text. This task will be run as a competition on Kaggle. Your marks for this question will be partially
based on your results in this competition, but your mark will not be affected by other students’ scores,
instead you will be graded against several benchmark solutions. The other part of your mark will come
from your code and write-up.
The dataset consists of text sequences from English language books in the genres:
Each text sequence is 10 contiguous sentences. Your task is to build the best classifier when evaluated
with macro averaged F1 score.
Note: the training data and the test data come from different sets of books. You have been provided with
docids (examples with the same docid come from the same book) for the training data but not the test
data.
You have been provided with an example solution in genre_classifier_0pc.py which shows you how
to read in the training data (genre_train.json), test data (genre_test.json) and output a CSV file that
the judging system can read. This solution is provided only as an example (it is the 0% benchmark for
this problem), you will want to build your own solution from scratch.
Setup
Please register for Kaggle4 using any email account you like. You do not have to use your full or real
name if you would prefer not to.
Submit solutions to https://www.kaggle.com/t/5daca656a1e14e159cfd31131ae1c1e0
To ensure student submissions are anonymous to other students but not the examiner, a unique Kaggle ID
has been provided on Wattle as text feedback to a dummy assignment called “Kaggle Unique ID”. This
dummy assignment does not accept submissions, and its only purpose is to distribute unique ids. Set
your “team name” to your unique id (e.g. pid123456789). This will allow us to match your submission
to your assignment for marking purposes. Note that “team name” is a Kaggle term, this is an individual
assignment, and so you should not work with others to complete it.
The Kaggle contest deadline is the same as the assignment deadline. For late submissions see below.
Rules
These rules are designed to ensure a degree of fairness between students with different access to computational resources and to ensure that the task is not trivial. Breaching the contest rules will likely result
in 0 marks for the competition part of this assignment.
Do not use additional supervised training data. That is, you are not allowed to collect a new genre
classification dataset to use for training. Pre-training on other tasks, such as language modelling,
is permitted.
Pre-trained non-contextual word vectors (such as word2vec, GloVe, fasttext) may be used even
if they require an additional download (e.g. you may use word vectors from spacy, genism, or
fasttext).
You may use the pre-trained transformers distilbert-base-cased or distilbert-base-uncased
from the transformers5 library, but other pre-trained transformers are not permitted.
You can use the following libraries (in addition to Python standard libraries): numpy, scipy, pandas,
torch, transformers, tensorflow, nltk, sklearn, xgboost, gensim, spacy, imblearn, torchnlp.
If you would like to use other libraries, please ask on the Piazza forum well in advance of the
assignment deadline.
This is an individual task, do not collude with other individuals. Copying code from other
people’s models or models available on the internet is not permitted.
4https://www.kaggle.com/
5https://github.com/huggingface/transformers
3
Judging system
You will upload your predictions for the test set as a CSV file for judging.
You are allowed to submit up to 5 times per UTC Day. Since you get immediate feedback from
every submission it is best to start submitting early and plan ahead.
The results shown on the public scoreboard prior to the conclusion of the contest only include 50%
of the test data. Your solution will be judged on the other 50% of the test data when computing
final rankings and marks.
The judging system allows you to choose which of all your submissions you want to be your final
one.
Competition marking
Marks will be assigned based on which judge baselines you beat on the hidden 50% of the test data. If,
for example, you beat the 80% baseline but do not beat the 90% baseline you will be awarded a mark
on a linear scale between these two based on your macro averaged F1 score. Exceeding the score of
the 100% baseline will give you a mark of 100% for the competition component of this question. (The
100% baseline and all other baselines can be trained in less than 24 hours on a laptop PC without GPU
support – your solution may make use of any compute resources available to you). Using Google Colab6
is recommended if you want to do GPU training but do not have access to a dedicated GPU.
Write-up
A fraction of your marks will be based on a write-up that a minimum describes:
How your final solution works.
How you trained and tested your model (e.g. validation split(s), hyperparameter search etc.).
What models you tested, which worked, and which didn’t.
Why you think these other models didn’t work.
Aim for 1 page or slightly less. Only the first 2 pages will be marked. Bullet points are acceptable if they
are understandable.
What to submit
Submit the code of your best solution (including training pipeline) to Wattle. Also make sure your
“team name” is set to your unique Kaggle ID. Do not submit stored parameters or data.
Submit your write-up in your answer PDF file.
In one of the three cases below, you should also submit a CSV file with your model’s output in the
correct judging format. The CSV file should be named with your Uni ID, e.g. your_uid.csv.
(a) You have been granted an extension, OR
(b) You could not use Kaggle and only if you could not use Kaggle, OR
(c) You decide to submit within 24 hours after the assignment deadline (i.e. late submission,
with 5% penalty).
6https://cloudstor.aarnet.edu.au/plus/s/tqqb8VfcM8IpBTx
4
Question 3: RNN Name Generator (4 marks)
Your task is to develop an autoregressive RNN model which can generate people’s names. The RNN will
generate each character of a person’s name given all previous characters. Your model should look like
the following when training:
Note that the input is shown here as a sequence of characters but in practice the input will be a sequence
of character ids. There is also a softmax non-linearity after the linear layer but this is not shown in the
diagram. The output (after the softmax) is a categorical probability distribution over the vocabulary,
what is shown as the output here is the ground truth label. Notice that the input to the model is just the
expected output shifted to the right one step with the (beginning of sentence token) prepended.
The three dots to the right of the diagram indicate that the RNN is to be rolled out to some maximum
length. When generating sequences, rather than training, the model should look like the following:
Specifically, we choose a character from the probability distribution output by the network and feed it as
input to the next step. Choosing a character can be done by sampling from the probability distribution or
by choosing the most likely character (otherwise known as argmax decoding).
The character vocabulary consists of the following:
“” The null token padding string.
The beginning of sequence token.
. The end of sequence token.
a-z All lowercase characters.
A-Z All uppercase characters.
0-9 All digits.
“ ” The space character.
Starter code is provided in rnn_name_generator.py, and the list of names to use as training and validation
sets are provided in names_small.json.
5
To complete this question you will need to complete three functions and one class method: the function seqs_to_ids, the forward method of class RNNLM, the function train_model, and the function
gen_string. In each case you should read the description provided in the starter code.
seqs_to_ids: Takes as input a list of names. Returns a 2D numpy matrix containing the names represented using token ids. All output rows (each row corresponds to a name) should have the
same length of max_length, achieved by either truncating the name or padding it with zeros. For
example, an input of: [“Bec.”, “Hannah.”, “Siqi.”] with a max_length set to 6 should return
(normally we will use max_length = 20 but for this example we use 6)
[[30 7 5 2 0 0]
[36 3 16 16 3 10]
[47 11 19 11 2 0]]
Where the first row represents “Bec.” and two padding characters, the second row represents
“Hannah”, the third row represents “Siqi.” with one padding character.
forward: A method of class RNNLM. In this function you need to implement the GRU model shown in the
diagram above. The layers have all been provided for you in the class initialiser.
train_model: In this method you need to train the model by mini-batch stochastic gradient decent. The
optimiser and loss function are provided to you. Note that the loss function takes logits (output of
the linear layer before softmax is applied) as input. At the end of every epoch you should print the
validation loss using the provided calc_val_loss function.
gen_string: In this method you will need to generate a new name, one character at a time. You will also
need to implement both sampling and argmax decoding.
For this question, please include in your answers PDF the most likely name your code generates using
argmax decoding as well as 10 different names generated using sampling. Also remember to submit
your code. Your code should all be in the original rnn_name_generator.py file, other files will not be
marked. For this question you should not import additional libraries, use only those provided in the
starter code (you may uncomment the import tqdm statement if you want to use it as a progress bar).
For example, one of the names sampled from the model solution was: Dasbie Miohmazie
