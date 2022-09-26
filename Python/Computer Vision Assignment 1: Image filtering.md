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


### Computer Vision Assignment 1: Image filtering

Computer Vision 2022 Assignment 1: Image fil tering
In this prac you will research, implement and test some image filtering opera tions. Image filtering by
convolution is a fundamental step in many computer
vision tasks and you will find it useful to have a firm grasp of how it works. For
example, later in the course we will come across Convolutional Neural Networks
(CNNs) which are built from convolutional image filters.
The main aims of the prac are:
• to understand the basics of how images are stored and processed in mem ory;
• to gain exposure to several common image filters, and understand how
they work;
• to get practical experience implementing convolutional image filters;
• to test your intuition about image filtering by running some experiments;
• to report your results in a clear and concise manner.
This assignment relates to the following ACS CBOK areas: abstraction, design,
hardware and software, data and information, HCI and programming.
General instructions
Follow the instructions in this Python notebook and the accompanying file
a1code.py to answer each question. It’s your responsibility to make sure your
answer to each question is clearly labelled and easy to understand. Note that
most questions require some combination of Python code, graphical output, and
text analysing or describing your results. Although we will check your code as
needed, marks will be assigned based on the quality of your write up rather than
for code correctness! This is not a programming test - we are more interested
in your understanding of the topic.
Only a small amount of code is required to answer each question. We will make
extensive use of the Python libraries
• numpy for mathematical functions
• skimage for image loading and processing
• matplotlib for displaying graphical results
• jupyter for Jupyter Notebooks
You should get familiar with the documentation for these libraries so that you
can use them effectively.
1
The Questions
To get started, below is some setup code to import the libraries we need. You
should not need to edit it.
# Numpy is the main package for scientific computing with Python.
import numpy as np
#from skimage import io
# Imports all the methods we define in the file a1code.py
from a1code import *
# Matplotlib is a useful plotting library for python
import matplotlib.pyplot as plt
# This code is to make matplotlib figures appear inline in the
# notebook rather than in a new window.
%matplotlib inline
plt.rcParams['figure.figsize'] = (10.0, 8.0) # set default size of plots
plt.rcParams['image.interpolation'] = 'nearest'
plt.rcParams['image.cmap'] = 'gray'
# Some more magic so that the notebook will reload external python modules;
# see http://stackoverflow.com/questions/1907993/autoreload-of-modules-in-ipython
%load_ext autoreload
%autoreload 2 %reload_ext autoreload
Question 0: Numpy warm up! (5%)
Before starting the assignment, make sure you have a working Python 3 instal lation, with up to date
versions of the libraries mentioned above. If this is all
new to you, I’d suggest downloading an all in one Python installation such as
Anaconda. Alternatively you can use a Python package manager such as pip or
conda, to get the libraries you need. If you’re struggling with this please ask a
question on the MyUni discussion forum.
For this assignment, you need some familiarity with numpy syntax. The numpy
QuickStart should be enough to get you started:
https://numpy.org/doc/stable/user/quickstart.html
Here are a few warm up exercises to make sure you understand the basics.
Answer them in the space below. Be sure to print the output of each question
so we can see it!
1. Create a 1D numpy array Z with 12 elements. Fill with values 1 to 12.
2
2. Reshape Z into a 2D numpy array A with 3 rows and 4 columns.
3. Reshape Z into a 2D numpy array B with 4 rows and 3 columns.
4. Calculate the matrix product of A and B.
5. Calculate the element wise product of 𝐴 and 𝐵𝑇
(B transpose).
You need to be comfortable with numpy arrays because that is how we store
images. Let’s do that next!
Question 1: Loading and displaying an image (10%)
Below is a function to display an image using the pyplot module in matplotlib.
Implement the load() and print_stats() functions in a1code.py so that the
following code loads the mandrill image, displays it and prints its height, width
and channel.
def display(img, caption=''):
# Show image using pyplot
plt.figure()
plt.imshow(img)
plt.title(caption)
plt.axis('off')
plt.show()
image1 = load('images/cat.jpg')
display(image1, 'cat')
print_stats(image1)
Return to this question after reading through the rest of the assignment. Find 2
more images to use as test cases in this assignment for all the following questions
and display them below. Use your print_stats() function to display their height,
width and number of channels. Explain why you have chosen each image.
### Your code to load and display your images here
Your explanation of images here
Question 2: Image processing (20%)
Now that you have an image stored as a numpy array, let’s try some operations
on it.
1. Implement the crop() function in a1code.py. Use array slicing to crop
the image.
2. Implement the resize() function in a1code.py.
3
3. Implement the change_contrast() function in a1code.py.
4. Implement the greyscale() function in a1code.py.
5. Implement the binary() function in a1code.py.
What do you observe when you change the threshold of the binary function?
Apply all these functions with different parameters on your own test images.
# This should crop the head from the cat image
crop_img = crop(image1, 278, 5, 508, 272)
display(crop_img)
print_stats(crop_img)
resize_img = resize(crop_img, 0.5, 0.6 )
display(resize_img)
print_stats(resize_img)
contrast_img = change_contrast(image1, 0.5)
display(contrast_img)
print_stats(contrast_img)
contrast_img = change_contrast(image1, 1.5)
display(contrast_img)
print_stats(contrast_img)
grey_img = greyscale(image1)
display(grey_img)
print_stats(grey_img)
binary_img = binary(grey_img, 0.3)
display(binary_img)
print_stats(binary_img)
binary_img = binary(grey_img, 0.7)
display(binary_img)
print_stats(binary_img)
# Add your own tests here...
Question 3: Convolution (20%)
3.1 2D convolution
Using the definition of 2D convolution from week 1, implement the convolution
operation in the function conv2D() in a1code.py.
test_conv2D()
4
3.2 RGB convolution
In the function conv in a1code.py, extend your function conv2D to work on RGB
images, by applying the 2D convolution to each channel independently.
3.3 Gaussian filter convolution
Use the gauss2D function provided in a1code.py to create a Gaussian kernel,
and apply it to your images with convolution. You will obtain marks for trying
different tests and analysing the results, for example:
• try varying the image size, and the size and variance of the filter
• subtract the filtered image from the original - this gives you an idea of
what information is lost when filtering
What do you observe and why?
3.4 Sobel filters
Define a horizontal and vertical Sobel edge filter kernel and test them on your
images. You will obtain marks for testing them and displaying results in inter esting ways, for example:
• apply them to an image at different scales
• considering how to display positive and negative gradients
• apply different combinations of horizontal and vertical filters
# Your code to answer 3.3, 3.4 and displaay results here.
Your comments/analysis of your results here...
Question 4: Image sampling and pyramids (25%)
4.1 Image Sampling
Apply your resize() function to reduce an image (I) to 0.125 height and width,
and then to enlarge the image back to its original size to get an image (I’).
Display and compare I and I’.
Apply a Sobel filter to I to get the edge image E.
Apply a Sobel filter to I’ to get the edge image E’.
Display and compare E and E’. What do you observe and why?
5
4.2 Image Pyramids
Creat a Gaussian pyramid as described in week2’s lecture on an image.
Apply a Gaussian kernel to an image I, and resize it with ratio 0.5, to get 𝐼1.
Repeat this step to get 𝐼2, 𝐼3 and 𝐼4.
Display these four images following the zebra example shown in the lecture note.
What is your observation?
# Your answers to question 4 here
Your comments/analysis of your results here...
Question 5: Auto correlation (20%)
Recall from week 2 that cross-correlation is a measure of similarity between a
template and an image. It is defined similarly to convolution.
5.1 Correlation function
Implement the function corr() in a1code.py, based on your convolution func tion. Hint: numpy’s flip() function
may be useful here.
5.2 Auto-correlation
We will experiment with auto-correlation, where the template patch is taken
from the image it is being compared to. Use the cropped eye from Question 2
as your template. Calculate the correlation of that template with every location
in the image, and display the output as an image. Where is the maximum
similarity? (Hint: numpy functions argmax() and unravel() will be useful
here). For simplicity, you can use a greyscale version of the image and template.
Is it what you expect? Why or why not?
5.3 Modified auto-correlation
Try modifying your correlation template or the base image in different ways,
and analyse the effect on correlation results. For example:
• if you did not find the correct location in 5.2, try centering the template
about its mean (i.e. subtracting the mean brightness from each pixel)
• if you did find the correct location in 5.2, try using resize() and
change_contrast() on the image. Where does it fail?
6
As before you will obtain marks for coming up with interesting tests and analysis,
and displaying your results clearly.
# Your code to answer question 5 and display results here
