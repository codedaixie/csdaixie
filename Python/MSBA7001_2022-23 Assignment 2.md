### MSBA7001_2022-23 Assignment 2
### MSBA7001
** ã Dr. DING Chao, September 2022
MSBA7001_2022-23 Assignment 2
• 6 problems, 32pts. • Keep all files in the same fold. Use relative path when reading and writing files.
• Save your code in a Jupyter Notebook file named “A2.ipynb”. • Compress all the following files as “A2.rar” or “A2.zip” and submit it on Moodle. - A2.ipynb
- Q1_fitness.csv
- Q2_words.csv
- Q5_mountains.csv
- Q6_screenshot.jpg
- Q6_teachers.csv
- fitness.json
- policy.txt
- stop_words.txt
• Due Sept 22 (Thursday), 11:30am
Question 1 (4pts) – HK fitness track
Note: this was a 2019 exam question.
As of now, there are 34 fitness walking tracks in 18 districts of Hong Kong. Each track has a track 
length and expected energy consumption. For instance, there is a track in the Ap Lei Chau Wind 
Tower Park with a track length of 1200 meters and energy consumption between 50 and 60 
calories. Your job is to extract all the tracks’ data.
The “fitness.json” file has information about all the 34 fitness walking tracks. Detailed description 
of each track is stored as key-value pairs as follows: 
Description of the main keys is listed in the following table.
Key Description
Title Name of venue where the fitness walking track is located
DistrictL Region name. Valid value(s):
- Hong Kong Island
length mincal maxcal
ã Dr. DING Chao, September 2022
- Kowloon
- New Territories
DistrictS Districts under the region (DistrictL)
Route Track length and energy consumption
Latitude Latitude of the track
Longitude Longitude of the track
From “Route”, one may find the track length (as length), minimum calories (as mincal), and 
maximum calories (as maxcal) required on the track. Read the json file and extract all related 
information of each track. 
Create a list called q1list to store the complete data. There should be 34 tracks in the list.
In three separate cells, execute the following codes one by one and show the outputs.
len(q1list)
print(q1list[:5])
print(q1list[-5:])
Finally, write the complete data to a csv file named “Q1_fitness.csv”. The header should be: “title, 
districts, districtl, latitude, longitude, length, mincal, maxcal”. It has 35 rows (including the 
header).
Your csv file should look like this when opened in Excel. 
Requirements
1. Use the csv module to write to the csv file.
2. DO NOT use pandas.read_json.
ã Dr. DING Chao, September 2022
Question 2 (5pts) – CE policy address
Note: this question is modified from a 2018 exam question.
On Oct 10th 2018, the Chief Executive of the HKSAR, Mrs. Carrie Lam, gave a policy address to 
the Legislative Council. The policy address lays out future plans for housing, health care and 
more. The speech is available at: https://www.policyaddress.gov.hk/2018/eng/speech.html
The speech
….
The entire speech is saved in the text file “policy.txt”. Your goal is to find the frequency of each 
unique word in the text. 
To obtain clean data, you need to remove punctuations before making the count. Note that in 
addition to the common English punctuations, the following Chinese punctuations are also in 
the document. You need to remove all such English and Chinese punctuations from the text.
“”‘’
To obtain meaningful data, you also need to remove stop words. Stop words refer to the most 
common words in a language such as “the,” “from,” and “are” in English. These words appear 
to be of little value, thus need to be removed. Read the text file “stop_words.txt”, where it has 
a list of common English stop words. Remove all the stop words from your answer.
For simplicity, you do not need to handle any other punctuations or variations of words such as 
“that’s” vs “that”, “yours” vs “your”.
ã Dr. DING Chao, September 2022
Count the frequency of unique words and create a DataFrame called q2df to store the complete 
data.
In three separate cells, execute the following codes one by one and show the outputs.
q2df.shape
q2df.head()
q2df.tail() 
In addition, create a DataFrame called q2df_sample, which is a sample of all words with a 
frequency higher than 20. Sort this sample in descending order and show it in the output like 
below.
Finally, write the complete data in a csv file named “Q2_words.csv”. The header should be 
“word, frequency”.
ã Dr. DING Chao, September 2022
Question 3 (5pts) – top movies
Write a program to read the page: https://www.imdb.com/chart/top. Extract the following 
information from each movie.
Create a DataFrame called q3df to store the complete data. There should be 250 movies.
In four separate cells, execute the following codes one by one and show the outputs.
q3df.shape
q3df.head()
q3df[100:106]
q3df.tail() 
In your output, values in the rating and user columns may look different from the example as 
they update overtime. 
Requirement: use only regular expressions for data extraction (do not use BeautifulSoup 4).
id
name
year
user rating
ã Dr. DING Chao, September 2022
Question 4 (4pts) – fake jobs
Build a crawler to extract fake jobs on the following page:
https://realpython.github.io/fake-jobs/
Use BeautifulSoup 4 to retrieve the following information: 
Create a DataFrame called q4df to store the complete data. There should be 100 jobs.
In three separate cells, execute the following codes one by one and show the outputs.
q4df.shape
q4df.head()
q4df.tail() 
In addition, show all 4 “engineer” related jobs in “AA” state. Your output should look like this:
position
company
city state
ã Dr. DING Chao, September 2022
Question 5 (6pts) – JP mountains
There are “100 Famous Japanese Mountains” in Japan. Detailed mountain information can be 
found on the following webpage:
https://www.peakbagger.com/list.aspx?lid=5651
Your task is to build a web crawler to extract the highlighted values of all the 100 mountains. 
When extracting the data, you are encouraged to check the first few mountains as a test before 
applying your code to the entire 100 mountains as it takes a little bit of time. You are also 
encouraged to print out a check point for every 10 mountains extracted.
Create a DataFrame called q5df to store the complete data. There should be 100 mountains.
In four separate cells, execute the following codes one by one and show the outputs.
q5df.shape
q5df.head()
q5df[50:56]
q5df.tail() 
In addition, show mountains whose elevation is between 2000m and 2500m in the Kanto 
region. Your output should look like this:
name region elev
lat long
domain/peak.aspx?pid=10882
id
ã Dr. DING Chao, September 2022
Finally, write the complete data to a csv file named “Q5_mountains.csv”. There should be a 
total of 101 rows (including the header) in the file.
Requirement: DO NOT use pandas.read_html.
When opening the pages, you may run into an SSL error. See the following fix.
import requests
requests.packages.urllib3.disable_warnings()
url = ' https://www.peakbagger.com/list.aspx?lid=5651' r = requests.get(url, verify = False)
soup = BeautifulSoup(r.text, 'html.parser')
ã Dr. DING Chao, September 2022
Question 6 (8pts) – MSc(BA) teachers
Build a crawler to extract profiles of all MSc(BA) teachers on the following page:
https://www.fbe.hku.hk/msba/about-us/our-faculty
Just a hint, this question is slightly difficult because the source code is a little messy. You need to 
make several trial-and-error attempts before getting your code to work. I tested for about half 
an hour when designing this question.
Create a DataFrame called q6df to store the complete data. There should be 26 teachers. Show 
the complete data in your output.
university country
name
url
ã Dr. DING Chao, September 2022
In addition, save all 26 teachers’ profile images in a folder called “images”. The folder should be 
in the same directory as your code file.
Python treats images as the type of bytes. A byte consists of 8 binary numbers. Therefore, when 
writing an image, use the mode ‘wb’ (write binary) and return content from the response (see 
below). Again, you may run into an SSL error. See Question 5 for the fix.
import requests
r = requests.get(url)
with open(filepath, 'wb') as handle:
handle.write(r.content)
The image title should have the following structure: name.extension 
- Dr. Michael C.L. CHAU.jpg
- Dr. Shan HUANG.png
Name comes from the name column and extension from the url column. - From name column: 'Dr. Michael C.L. CHAU' - From url column: 'https://fbeo.fbe.hku.hk/msba/f/page/254212/266832/300
p300/Dr_Michael_CHAU_2019.jpg'
Note that images may have different extensions such as jpg, jpeg, png. So, do observe the data 
closely before designing your code. After saving all the images, take a screenshot like below and 
name it “Q6_screenshot.jpg”
Finally, write the complete data to a csv file named “Q6_teachers.csv”. There should be a total 
of 27 rows (including the header) in the file. **
