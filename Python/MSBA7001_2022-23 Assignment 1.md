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

### MSBA7001_2022-23 Assignment 1
** MSBA7001_2022-23 Assignment 1
• 6 problems, 20 pts
• Save your codes in a Jupyter Notebook file named “A1.ipynb”
• Compress your answer file as “A1.rar” or “A1.zip” and submit it on Moodle
• Due Sept 6 (Tuesday), 11:30am
Problem 1 (2pts)
Write a program to print the following pattern – a hollow pyramid. The number of rows is 
determined by user input. For simplicity, we assume the user will enter a positive integer 
number. On each row, the exact width of blanks between asterisks is decided by yourself, as
long as the pattern looks like a pyramid. Requirement: only use one simple for loop; do NOT
use nested for loop.
Problem 2 (3pts)
ord is a built-in string method which converts a character to a numeric value, and chr is a 
built-in integer method which converts a numeric value to a character. For example:
>>> ord('a')
97
>>> chr(65)
A
Define your own function tri_letters(n) which accepts a positive integer n (1 < n < 10) and prints 
a triangle of letters like the example shown below. The number of rows is determined by n. On 
each row, letters are separated by one space. In your answer, test a few samples like below.
Requirement: use a nested for loop.
 tri_letters(3)
A B C
A B 
A 
 tri_letters(20)
WARNING: your input is not valid
1
 tri_letters('abc')
WARNING: your input is not valid
 tri_letters(8)
A B C D E F G H
A B C D E F G 
A B C D E F 
A B C D E 
A B C D 
A B C 
A B 
A 
Problem 3 (3pts)
Define your own function sorting(sequence) to sort any given sequence of letters in ascending 
order. For example, given an original list ['b', 'z', 'a', 'd', 'k', 'o', 'e'], your function should 
produce: ['a', 'b', 'd', 'e', 'k', 'o', 'z']. There is no need for user input, just take this list as given 
and pass it as an argument to your function. Requirement: use a nested loop; do NOT use the 
built-in functions of min and max.
Problem 4 (4pts)
Define your own function leap_year(year) to determine if year is a leap year or not. For 
simplicity, we will consider a year to be valid if 0 < year < 9999. In your answer, test a few 
samples like below. Requirement: use a while loop; do NOT use try/except; do NOT use the 
calendar module.
 leap_year(2000)
'Leap year'
 leap_year('MSBA')
'WARNING: your input is not valid'
 leap_year(-1990)
'WARNING: your input is not valid'
 leap_year(1990.83)
'WARNING: your input is not valid'
>>> leap_year(1800)
'Regular year'
 leap_year(187000)
'WARNING: your input is not valid'
2
Problem 5 (4pts)
Rotating a letter means to shift it through the alphabet, wrapping around to the beginning if 
necessary, so ’A’ rotated by 3 is ’D’ and ’Z’ rotated by 1 is ’A’. Define your own function called 
rotate_letter(letter, n) that accepts a letter and an integer n, and returns a new letter that is 
rotated by the amount of n. You may want to refer back to Problem 2 for ord and chr. In your 
answer, test a few samples like below. No particular requirement.
rotate_letter('t', 3)
'w'
 rotate_letter('Y', 5)
'D'
 rotate_letter('k', 20.1)
'WARNING: Your input is not valid.'
 rotate_letter('abc', 19)
'WARNING: Your input is not valid.'
>>> rotate_letter('D', -4)
'Z'
 rotate_letter('?', 8)
'WARNING: Your input is not valid.'
 rotate_letter(7, 109)
'WARNING: Your input is not valid.'
 rotate_letter(20, 'k')
'WARNING: Your input is not valid.'
Problem 6 (4pts) 
Write a program to find out all six-digit consecutive numbers (such as 123456, 345678, and 
789012) in the first million digits of pi. Read from the text file “pi_million_digits.txt”. Your 
answer should look like below. Requirement: use a for loop to generate all the possible six￾digit consecutive combinations but do not start with a base of 012345678901234.
These are the possible six-digit consecutive combinations:
012345 123456 234567 345678 456789 567890 678901 789012 890123 90
1234
The following are in the first million digits of pi:
012345 234567 345678 456789 567890 678901 890123 
3 **
