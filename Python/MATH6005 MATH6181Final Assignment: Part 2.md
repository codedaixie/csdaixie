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


### MATH6005 MATH6181Final Assignment: Part 2

Course: MATH6005-Introduction to Python and MATH6181-Python & Forecasting
Semester: 2021:2022
Instructor:
Vuong Phan (t.v.phan@soton.ac.uk)
March 22, 2022
Final Assignment: Part 2 (week 8)
Rules for the Final Assignment: Part 2 (week 8) solution
• You will upload, on Blackboard, one single file.
• The file name, with all functions, must be in the format: .py, e.g.:
fdoo1r22.py. This file is the Final Assignment: Part 2 (week 8) solution that will be
uploaded on Blackboard.
• All functions must follow the prototypes, i.e., they must have the name specified, have the
input(s) set, and output the variables in the order specified in the prototypes.
• No partial credit will be given if the function is not working correctly, i.e., due to syntax
error, neglect to follow the prototype, etc..
• Only the functions must be in the upload file; any auxiliary or debugging code must be
removed of the upload file.
• Please include comments in your code to explain how it works. Fail to comment on your
code will result in 10 points reduction on your final assignment mark. Comment every
line of your code.
• You can use any function/package/library, including NumPy, Pandas, etc.
• The solution must have only functions. Do not define any function within another function.
• A template solution file is available on Blackboard.
1
Faculty of Social Sciences
School of Mathematical Sciences
The Ship Rendezvous Problem
1 Introduction
Your company has been contracted to provide a tool in Python to solve the Ship Rendezvous
problem (SRP) to enable a cruise company to minimise the time it takes for the support ship to
visit each of the cruise ships in the fleet.
The support ship must visit each of the n cruise ships exactly once and then return to the
port (where it started). The support ship travels at a constant speed and changes direction with
negligible time. Each cruise ship moves at a constant velocity (i.e. speed and direction). The
objective is to minimise the total time taken to visit all the cruise ships (i.e. the time taken
to reach the final ship).
This problem is considered in 2-dimensional (2D) Euclidean space. A problem instance is de fined by
specifying the starting (x, y) coordinates for all ships (including the support ship), the
velocity of the support ship, and the velocity of the cruise ships.
Note that it is certain that the SRP has a finite solution if the support ship is faster than all
other ships in the fleet. However, it is very likely (but not certain) that the SRP will not have a
complete solution (one where all the cruise ships are visited) if one or more of the cruise ships are
faster than the support ship.
2 Your Python Task
You must implement the greedy heuristic for the 2D Euclidean SRP in Python. Your program
must perform the following tasks:
• Read the data from a CSV file (a sample data file is provided on Blackboard sample_srp_data.csv);
• Run the greedy heuristic against the problem instance to obtain a solution;
• Output a list of indexes of unvisited cruise ships, a list of indexes of the visited cruise ships,
and the total time to visit all visitable cruise ships.
Greedy Heuristic for the SRP
A simple way of finding a solution to the SRP is to use a greedy heuristic. The greedy heuristic
works as follows
1. For each unvisited cruise ship, calculate how long it would take the support ship to intercept
it from the support ship’s current position.
2. Choose the cruise ship, i, which can be reached in the shortest amount of time.
3. Visit cruise ship i and update the positions of the ships in the fleet.
4. Return to 1 if there are any unvisited cruise ships that can be reached by the support ship.
2
Faculty of Social Sciences
School of Mathematical Sciences
In order to make the heuristic deterministic (i.e. to guarantee the same result each time it is run
on the same problem instance) you must specify how ties in Step 2 are broken. If there is a tie,
the algorithm should choose to visit the ship with the smallest index (for example, if ships 5 and
7 are tied, ship 5 should be chosen in preference to ship 7).
The Technical Appendix (at the end of this document) provides details on how to calculate
intercept times.
Function prototypes
import pandas as pd
def read_srp_input_data ( csv_file ):
’’’
function description
’’’
input_data =pd . read_csv ( csv_file )
return input_data
• The function must use the input variable csv_file to read the TXT file, inside of the
function. You cannot use a fixed path file. If the function does not read the file using the
input variable csv_file no partial credit will be given.
def findPath ( input_data ):
’’’
function description
’’’
unvisited_index = [] # It must be a LIST . It cannot be a tuple nor NumPy array .
visited_path = [] # It must be a LIST . It cannot be a tuple nor NumPy array .
total_time = 0 # it must be a float .
return unvisited_index , visited_path , total_time
• The function outputs must be in the order as specified on the prototype. If the function
outputs are not in the set order no partial credit will be given.
Example: There are 5 cruise ships on the fleet. Suppose that, using the Greedy Heuristic, the
support ship can only visit 3 of them with the indexes 1, 2, 4 (e.g. the 2 remained cruise ships with
the indexes 3, 5 cannot be visited). Remember that support ship should have index "0" and the
first cruise ship has index "1" and so on. Then an example for a solution looks like:
[3 , 5], [2 ,4 ,1], 45 .3
which mean that unvisited_index = [3,5], visited_path = [2,4,1] and total_time = 45.3. The
visited_path = [2,4,1] means that the support ship will visit the cruise ship with index 2 first, and
then the cruise ship with index 4, and finally the cruise ship with index 1.
Please, the debugging/testing code must not be in your solution file
that will be uploaded on Blackboard.
3
Faculty of Social Sciences
School of Mathematical Sciences
Advice on writing the code
Make sure you follow the guidelines below when writing your code:
• You can (and are encouraged to) create new functions if needed. These must follow the good
coding practices we have taught in the lectures and labs. However, your submission must
include all the functions provided in the template, with the exact same names provided in
the template.
• Your code should implement exactly the algorithm described above. Do not use an alterna tive. If you use a
different algorithm (even if the algorithm solves the problem correctly and
the results seem better) your assignment will be marked as incorrect.
• We will test your code against an unseen set of problem instances. We recommend that you
test your algorithm and make sure that your code returns the expected solutions for different
scenarios. To help you do this, you may create and test new CSV files for which you think
you know the expected behaviour.
• We will only use correct input CSV files to test your code. The assignment does not ask
you to include logic to handle non-numeric or incorrect CSV files. There are no extra marks
available for including this functionality.
4
Faculty of Social Sciences
School of Mathematical Sciences
Technical Appendix
This appendix contains some technical information to help you solve the proposed problem in the
assignment. Please, pay attention to these formula and specifications to ensure that your algorithm
produces the correct results.
Notation
We denote the starting coordinates of the support ship by (X0; Y0) and its speed by S. We consider
the ship i in the task force, where 1 ≤ i ≤ n. We denote its starting coordinates by (xi0; yi0).
Its velocity is split into x-component and y-component, vix and viy , respectively. Therefore the
position of ship i at time t > 0 is given by
(xit; yit) = (xi0 + tvix; yi0 + tviy)
Note that the speed of ship i (denoted by si) can be obtained from its velocity with the following
equation:
si = q v2
ix + v2
iy.
Calculating intercept times
To calculate intercept times, it is simplest to update the position of the ships at every step, so
that (X0; Y0) represents the current coordinates of the support ship and (xi0; yi0) represents the
current coordinates of ship i for 1 ≤ i ≤ n. Then the time, T, taken for the support ship to move
from its current position and intercept ship i is found by finding the smallest positive root of the
quadratic equation:
aT2 + bT + c = 0
where the coefficients are obtained as follows:
a = v2
ix + v2
iy − S2 b = 2 ((xi0 − X0)vix + (yi0 − Y0)viy) c = (xi0 − X0)2 + (yi0 − Y0)2.
Input Data
The input data for each problem instance will be presented in a comma separated value (CSV)
file. A correctly-formatted input file consists of N rows of data, where N ≥ 2. Row 1 corresponds
to the support ship, and the remaining rows (i.e. rows 2; ...; N) correspond to the ships to be
intercepted. Each row contains five pieces of information in the following order:
• Ship name/description (text).
• Start x-coordinate (decimal number).
• Start y-coordinate (decimal number).
• Velocity x-component (decimal number).
• Velocity y-component (decimal number).
