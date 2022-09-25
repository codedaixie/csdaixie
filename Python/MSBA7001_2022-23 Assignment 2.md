### MSBA7001_2022-23 Assignment 2
### MSBA7001
** MSBA7001_2022-23 Assignment 2
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
more. The speech is available at: https://www.policyadd **
