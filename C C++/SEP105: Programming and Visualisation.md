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


### SEP105: Programming and Visualisation

Project 3
T2 2022
Due Date: See the unit site
Written by: Benjamin Champion
Project 3 – Description
The Turing Moore Engineering company has tasked you with putting together a simulator that can
calculate the distance and velocity of a cannon ball fired out of a cannon. This data also needs to be
logged so future analysis can be performed on the data (probably not by you).
As a minimum, the program must display a Welcome message as the first thing displayed in the
program with the following information, each on a separate line:
• The message “Turing Moore Engineering Cannon Simulator 1.0”
• Your name (as shown on the unit site)
• Your Student ID
• Date the assignment is due in the format: dd/mm/yyyy
• The level of mark you are aiming to achieve (eg Desired Level: HD)
The following points apply to this document:
• This assessment is worth 40% of the total grade.
• The program must be written in C++ targeted at the Windows Operating System
• There is a defence presentation associated with your mark. Please see the rubric for more
information
• Only functions, types, etc that was covered in class between weeks 1-11 can be used in this
assessment
The following information describes the requirement for the different levels in this assignment. Before
completing tasks from a higher level all tasks from a lower level must first be completed.
Pass (P) Level (50 – 59):
To achieve a pass for the unit the software must be able to display the following behaviour:
• The user must be able to enter in a pitch angle for the cannon in degrees, to a maximum of
three decimal places
• The user must be able to enter in a velocity for the cannon ball as it leaves the cannon in m/s
to a maximum of three decimal places
• Display the maximum height of the cannon ball to the terminal
• Display the maximum distance the cannon ball has travelled to the terminal
• Log the distance and the velocity of the cannon ball in the x and y directions to a file called
log.csv for every 0.1s of the simulation. Each new data point should be on a new row (new
line) of the log.csv file. Each piece of information should be in its own cell (separated by a
comma). The log file should have these five titles displayed in the first row (one in each cell)
of the file:
o Time (s)
o x-distance (m)
o y-distance (m)
o x-velocity (m/s)
o y-velocity (m/s)
• All data that is written to the terminal should also be saved to an Output.txt file in the same
format that it is written to the terminal. When the program starts this file should be cleared,
then appended too until the program ends.
• The program should ask the user if they would like to exit (e), or restart (r) the program
Credit (C) Level (60 – 69):
• All functionality of the Pass level
• The user must be able to be choose weather to enter an initial velocity to the cannon ball, or
an applied force to the cannon ball
• The user should be able to enter in the initial height of the cannon
• The user must be able to enter in a target distance that the cannon ball is aiming for. The
difference between this distance, and the distance the cannon ball reached, should be
displayed after each shot.
• The simulation should stop when the cannon ball reaches the ground
Distinction (D) Level (70 – 79):
• All functionality of the Credit level
• The log file’s titles should be changed to log-0.csv and should be stored in a folder called Log
Files. Whenever the user makes a new shot, it should not override the previous log file, but
make a new log file with an indexed number (for example if the folder contained the files log0.csv and log1.csv, the program would make a new file called log-2.csv).
• A wind force can be entered by the user. This should be able to be entered in the following
format: magnitude,direction where the magnitude is in Newtons (N), and the direction is
between 0 – 360 degrees with due East (to the right of the screen) being 0⁰, and increasing in
a counter clockwise direction. For example: 10,270 would indicate a force pointing directly to
the ground of 10 Newtons. The wind force should be applied to the next shot
• When the program starts, the user should be prompted if they would like to use settings
stored in a settings.csv file. This settings files should contain the information for a single shot
in each row. Assume the user will be entering in the initial force into the settings file. An
example of the settings.csv file may be: the user wanted to make a shot at 45⁰, with a force
of 50N, with the cannon initially at a height of 1m, the target 12m away from the cannon and
a wind force of 5N at 26⁰. This would look like: 45,50,1,12,5,26 in the settings.csv file. Assume
the first row of the CSV file has titles appropriately labelling each of the columns to make it
easy for humans to enter data into the settings.csv file.
• If the user chooses to use the input data from the settings.csv file, the program will repeat
without any further input from the user until it has completed all of the rows of the
settings.csv file. The program should assume each row of the settings.csv file, except for the
first row containing the titles, is a new shot so it should treat it appropriately (for example
new log files are made).
High Distinction (HD) Level (80 – 100):
• All functionality of the Distinction level
• A new mode should be added where there are two cannons playing off against each other.
First, both players are asked what their name is which must be recorded. Then the heights of
the cannons off the ground, the distance between the cannons and the wind force, should be
randomly generated. Each player takes in turns entering in the angle and force that should be
applied to the cannon ball. After each shot a message should be displayed showing how far
away from the opponent the cannon ball landed. After each shot, a new wind force and angle
should be randomly generated and displayed to the user. When a player wins, a message
showing the name of the player should be displayed. Log files for both cannons should still be
created, storing all relevant data. The log file should also have the player name in its name (eg
if the player Bob was playing, and it was his first time playing, the log file would be BobLog0.csv) and be
stored in a folder called Player Log Files.
• Any other X-factors added to the program will be considered for additional marks. For
example, formatting of the information to the terminal, more functionality in the game. Marks
will only be awarded for X-factors after evidence of all desired functionality of the program is
demonstrated (Hint: don’t worry about this until you have finished and tested the rest of the
assignment).
Background
The last project you completed was seen by the owner of the Turing Moore Engineering, and they
were very impressed by your work. Therefore, they have decreed that you will only be given complex
programming challenges with little turn around time that have a direct impact on the company’s
bottom line!
The company has been approached by an entrepreneur who has commissioned the company to work
on a multimillion-dollar project. This project has the condition that a simple simulation of the project
is provided quickly to prove it will work. No simulation, the company won’t get paid! This entrepreneur
was obsessed with the simple game Bang! Bang! he played on his windows 95 computer when he was
a child and wants to make a real-world version of the game. In this game, two cannons are placed on
opposing hills and take turns to shoot a cannon ball at each other. The first cannon to hit the other
cannon was victorious. In the entrepreneur’s version of the game, the cannons will shoot rounds filled
with paint that will pop on impact. Similar to a large paint ball gun. The concept of the game is the
same, the competitors will fire the paint rounds from one cannon at another cannon one at a time
until one competitor hits the other’s cannon.
Prior knowledge
At a minimum to pass this assessment you will need to have skills in these areas. If you feel like you
are not as strong in these areas as you would like to be, I recommend you go and brush up on the
class content. Please note, depending on how you write your program you may use skills outside of
those listed here, or you may not need to use some of the things on this list. That is OK as there are
multiple ways to write a program with the same functionality.
• Flow Diagrams
• Initialising and manipulating variables (int, float, double, etc)
• Initialising and manipulating arrays (int a[], double b[], etc)
• Conditionals (&&, ||, etc)
• Decisions (if, switch)
• Looping (for, while, etc)
• Writing data to the console/terminal (printf, cout, etc)
• Reading data from the console/terminal (scanf, cin, etc)
• Functions
• Opening Files
• Closing Files
• Reading and Writing data from files
• Debugging (break points, single stepping, etc)
• Projectile Motion Calculations – See Hints. This should be common knowledge for an
engineering student or not too difficult to figure out.
Known Conditions
• This is a simple simulation, it only needs to work in 2D
• The cannon ball’s mass is 1.5kg
• The dimensions of the cannon ball do not need to be considered. All calculations can be made
assuming the cannon ball is the size of a single point.
• There are no external forces on the cannon ball once it has been fired (no drag, wind
resistance, etc) unless otherwise indicated
• The cannon is permanently fixed to the ground such that it will not move, including when it
fires the payload (cannon ball)
• The cannon can pitch its barrel up and down changing the angle the cannon ball will exit the
barrel
• The simulated cannon and the cannon ball are perfect and indestructible. For example, no
amount of force will destroy, deform, etc the cannon or the payload
• Gravity only effects the cannon ball, not the cannon
• Gravity is constant at 9.81m/s2
regardless to the height of the cannon ball, height of the
cannon, etc unless told otherwise
• The simulation will go for a maximum of 5 seconds unless otherwise stated
• The cannon ball does not bounce when it hits the ground, it can continue straight through
anything (including the ground) without slowing down or being affected in any way
• Assume any force that is applied to the cannon ball when it is launched is applied for 0.2s
What to submit
• A flow chart as a PDF – it is highly recommended that you make your flowchart BEFORE writing
any software
• All fully commented code files that pertain to the project (eg the main.cpp file). These files
must be the same files that generated the submitted executable file.
• An .exe of the final code – please note this executable will be tested on a Windows PC. It is up
to you to ensure that the software that you write will execute correctly on a Windows PC. If
you use a Windows PC and the methods that are described in class, the code will run and
execute on a Windows PC. If you use some other operating system (eg MAC, Linux) there is
no guarantee that the software you submit will run, or run correctly. Consider this your only
warning, any software that does not run for this reason will generate 0 marks.
• Any data and appropriate folders. For example, if the program needs a folder to hold some
data, another folder to write the output to, etc these folders should be included in the .zip
folder in the appropriate place relative to the .exe. Test your .exe before submitting to make
sure the folders are in the correct places.
• The entire project folder containing the software. This is independent to the other documents
you are required to add.
Hints
• It is recommended that you develop the program in stages, do not shoot for a High Distinction
straight away. First make a flowchart and program that will achieve a pass. Save this, make a
new program, copy in the previous solution and modify the flow chart and program to reach
a credit, etc. Make sure you have all of the functionality working of the previous level BEFORE
moving onto the next level. You only need to submit the most recent working version of the
program you do not need to submit earlier versions of the program.
• You will need to use your knowledge gained from the previous assignments to complete this
assignment, such as File IO, loops, if statements, maths, etc
• All of the calculations for this assessment can be found in any physics textbook that covers
projectile motion (which will be any good physics textbook from year 11 to first year
University). A quick google of projectile motion should also give you these equations! Some
common symbols to be aware of are:
o d – distance in metres (m)
o v – velocity in meters per second (m/s)
o a – acceleration in meters per second squared (m/s2
)
o t – time in seconds (s)
o g – acceleration due to gravity (9.81m/s2
)
o x – the x direction (right is positive)
o y – the y direction (up is positive)
• When performing these calculations for the log files, you will be able to continuously repeat
the same calculations over the time period (0.1s) over and over again to generate data for the
log file. When generating this data, remember the output from the previous time step
becomes the input for the next time step! For example, if the initial velocity of the first-time
step is 10m/s and the final velocity of the first time step is 9.9m/s, then the initial velocity of
the next time step will be 9.9m/s!
• Remember that you can use functions from the cmath library that we covered in the unit.
Generally in programming, trigonometric functions (sin, cos, tan, etc) take radians not degrees
as an input! This is the case with the cmath library. Therefore, you will need to convert any
angle entered in degrees into radians before you use it in these functions!
Rubric
All Assignments will be marked off the following Rubric. Please note:
• No marks will be awarded for a higher grade for the software until all of the functionality of
the lower grade is awarded.
• The flow chart must represent the code that was submitted. Do the flowchart before writing
any software! If the flow chart includes some functionality that was not included in the final
solution, this is OK. Code including functionality not included in the flow chart is not accepted
and you may be heavily penalised.
• The submitted code must be the same as the executable file that was submitted. If this is not
the case, ie the functionality of the code does not match what is observed in the executable,
it will be assumed that you have not written the code and you may be subject to academic
misconduct.
• The defence is a hurdle. If you do not pass the defence, you will not pass the unit
• There is nothing to prepare for the defence. The defence will go for around 4 minutes, where
you will be asked questions about the code that you have submitted. If you have written the
code, this should not be difficult to pass
• Times for the defences will be posted to the unit site
See next page for the rubric
