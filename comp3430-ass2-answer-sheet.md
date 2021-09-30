# COMP3430 ANSWER SHEET



## Question 1

Please provide the two check codes you obtained from the data set generation program **for assignment 2** in the form: **ANU ID code / data set code**

```
Your student data set for the second data wrangling 2021 assignment
has been generated and written into file:

  data_wrangling_education_2021_u6828533.csv

Your ANU ID check code is:           cfa50ccf
Your student data set check code is: d43bbcab35aa

  *** Check this pair of codes is in the list provided on Wattle
  *** If not contact the course convenor.

####  cfa50ccf / d43bbcab35aa

```



## Question 2

**Upload** your merged and cleaned data set here.

Your data set must be a .**csv** (comma separated values) file.

You **MUST** name your file to upload as: **data_wrangling_merged_2021_*your_ANU_ID*.csv**, where you replace *your_ANU_ID* with your actual ANU ID.

data_wrangling_merged_2021_u6828533.csv



## Question **3** (0.50)

**Task 1, question (1):** For the two strings generated based on your ANU ID, **manually calculate the Jaccard similarity based on unigrams** (q = 1).

**Include both your workings (equations and calculations) as well as the final result.**

Round the final result to two decimal places (eg: 0.01 or 42.42).

Do not upload any code. We will not accept any type of code as valid answers. You need to calculate this manually.



With s1 = '1236828' and s2 = '1238533' and q = 1:

Q1 = {'1', '2', '3', '6', '8'}
Q2 = {'1', '2', '3', '8', '5'}

intersection(Q1, Q2) = {'1', '2', '3', '8'}
union(Q1, Q2) = {'1', '2', '3', '6', '8', '5'}
simJacc(s1, s2) = | intersection(Q1, Q2) | / | union(Q1, Q2) | = 4 / 6 = 0.67

Jaccard similarity based on unigrams is 0.67.



## Question 4 (0.50)

**Task 1, question (2):** For the two strings generated based on your ANU ID, **manually calculate the Dice similarity based on bigrams** (q = 2).

**Include both your workings (equations and calculations) as well as the final result.**

Round the final result to two decimal places (eg: 0.01 or 42.42).

Do not upload any code. We will not accept any type of code as valid answers. You need to calculate this manually.



With s1 = '1236828' and s2 = '1238533' and q = 2:

Q1 = {'12', '23', '36', '68', '82', '28'}
Q2 = {'12', '23', '38', '85', '53', '33'}

intersection(Q1, Q2) = {'12', '23'}
simDice(s1, s2) = 2 * | intersection(Q1, Q2) | / (| Q1 | + | Q2 |) = 2 * 2 / (6 + 6) = 1 / 3 = 0.33

Dice coefficient similarity based on bigrams is 0.33.



## Question **5** (1.00)

**Task 1, question (3):** For the two strings generated based on your ANU ID, **manually calculate the Levenshtein edit distance between the two strings, assuming costs of 1 for all types of edits**.

**Include both your workings (full edit matrix) as well as the final result.** Clearly show the rows and columns of your edit matrix and do not provide a description of the edit matrix.

**You only need to provide the full edit matrix and final edit distance, not the resulting string similarity.**

Do not upload any code. We will not accept any type of code as valid answers. You need to calculate this manually.



With s1 = '1236828' and s2 = '1238533' and assuming costs of 1 for all types of edits, the edit matrix below shows the number of edits between sub-strings:

|       |      | **1** | **2** | **3** | **8** | **5** | **3** | **3** |
| ----- | ---- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
|       | 0    | 1     | 2     | 3     | 4     | 5     | 6     | 7     |
| **1** | 1    | 0     | 1     | 2     | 3     | 4     | 5     | 6     |
| **2** | 2    | 1     | 0     | 1     | 2     | 3     | 4     | 5     |
| **3** | 3    | 2     | 1     | 0     | 1     | 2     | 3     | 4     |
| **6** | 4    | 3     | 2     | 1     | 1     | 2     | 3     | 4     |
| **8** | 5    | 4     | 3     | 2     | 1     | 2     | 3     | 4     |
| **2** | 6    | 5     | 4     | 3     | 2     | 2     | 3     | 4     |
| **8** | 7    | 6     | 5     | 4     | 3     | 3     | 3     | 4     |

```
 	 	1	2	3	8	5	3	3
 	0	1	2	3	4	5	6	7
1	1	0	1	2	3	4	5	6
2	2	1	0	1	2	3	4	5
3	3	2	1	0	1	2	3	4
6	4	3	2	1	1	2	3	4
8	5	4	3	2	1	2	3	4
2	6	5	4	3	2	2	3	4
8	7	6	5	4	3	3	3	4
```

Final Levenshtein edit distance is 4.00.



## Question **6** (1.00)

**Task 1, question (4):** For the two strings generated based on your ANU ID, **manually calculate the Levenshtein edit distance between the two strings, assuming a cost of 2 for substitutions, cost of 1 for inserts, and cost of 1 for deletes**.

**Include both your workings (full edit matrix) as well as the final result.** Clearly show the rows and columns of your edit matrix and do not provide a description of the edit matrix.

**You only need to provide the full edit matrix and final edit distance, not the resulting string similarity.**

Do not upload any code. We will not accept any type of code as valid answers. You need to calculate this manually.



With s1 = '1236828' and s2 = '1238533' and assuming a cost of 2 for substitutions, cost of 1 for inserts, and cost of 1 for deletes, the edit matrix below shows the number of edits between sub-strings:

|       |      | **1** | **2** | **3** | **8** | **5** | **3** | **3** |
| ----- | ---- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
|       | 0    | 1     | 2     | 3     | 4     | 5     | 6     | 7     |
| **1** | 1    | 0     | 1     | 2     | 3     | 4     | 5     | 6     |
| **2** | 2    | 1     | 0     | 1     | 2     | 3     | 4     | 5     |
| **3** | 3    | 2     | 1     | 0     | 1     | 2     | 3     | 4     |
| **6** | 4    | 3     | 2     | 1     | 2     | 3     | 4     | 5     |
| **8** | 5    | 4     | 3     | 2     | 1     | 2     | 3     | 4     |
| **2** | 6    | 5     | 4     | 3     | 2     | 3     | 4     | 5     |
| **8** | 7    | 6     | 5     | 4     | 3     | 4     | 5     | 6     |

```
 	 	1	2	3	8	5	3	3
 	0	1	2	3	4	5	6	7
1	1	0	1	2	3	4	5	6
2	2	1	0	1	2	3	4	5
3	3	2	1	0	1	2	3	4
6	4	3	2	1	2	3	4	5
8	5	4	3	2	1	2	3	4
2	6	5	4	3	2	3	4	5
8	7	6	5	4	3	4	5	6
```

Final Levenshtein edit distance is 6.00.



## Question 7 (4.00)

**Task 2: Merging the data sets**

You must merge your two individual data sets into a single data set using the Social Security Number (SSN) attribute that is in common to both data sets. Address the following four aspects of the merging step:

1. How many SSN occurred in common in both data sets? How many occurred only in the medical data set, and how many occurred only in the education data set?

2. If there were records that only occurred in a single data set, describe what you did with them, and explain / justify why.

3. If there were duplicate records in an input data set (with the same SSN), describe what you did with them, and explain / justify why.

4. If there were any inconsistencies between records in the two data sets with the same SSN, what types of inconsistencies were there, and how many of each type? How did you deal with these inconsistencies, by either resolving them or processing them otherwise? Describe and justify your approaches taken.

**Clearly show your answers to questions 1. to 4.**

**Write a maximum of 400 words (15 lines of text). If you write more than these limits we will have to apply an over-word-limit penalty.**

**English writing mistakes and typographical errors will attract small penalties.**

1. Excluding the records with duplicated SSN except for the first occurrence for each data set, I find

   SSN occurred in common in both data sets: 16047

   SSN occurred only in the medical data set: 3953

   SSN occurred only in the education data set: 3194

   

2. For the records that only occurred in a single data set, I removed them in the merged data set by performing an inner join based on SSN. Because we want to find connections between an individual’s education, employment history, and health, records that only occur in a single data set are useless.

   

3. For the records with duplicated SSN in each dataset, I removed the duplicate records except for a record with the least missing values. This was done by first sorting the data sets by the number of null attributes of each record in descending order, and then dropping duplicates except for the first occurrence. Because the Social Security Number is the unique identifier for individuals, duplication is not allowed. And it's best that we only keep the records with the most complete information (i.e. records with the least missing values) for further data analysis.

   

4. For inconsistencies between records in the two data sets with the same SSN (excluding duplicates following the above steps), I found the following types of inconsistent data and their quantities:

   middle_name: 2831
   last_name: 41
   gender: 1638
   street_address: 6875
   suburb: 6781
   postcode: 8590
   state: 2964
   phone: 8818
   email: 6848

   The inconsistencies are composed of two causes: value missing and values from two data sets being not equal. 

   In terms of missingness, for a record's missing attribute from a data set, in the merged data set I set this attribute's value as the same attribute's value from the other data set. This is because I want to minimize the missing values for further data analysis, and personal data for the same individual can be mostly unchanged.

   In terms of inequivalence, I compared the timestamps of the two data sets and chose the latest attributes to be in the merged data set. Because all the types of data above can be updated over time, for instance, the last name can be changed after marriage, and gender can be changed for transgender people.



## Question 8 (4.00)

**Task 3: Missing and incorrect values**

Address the following four questions related to missing and incorrect values in the data sets:

1. Following the missing value patterns table we discussed in the labs and used in Assignment 1, find the combination of three attributes with the highest number of missing values (i.e. the three-attribute combinations with the largest numbers of records with missing values). Provide the attribute names and the corresponding number of records with missing values in your merged data set.

2. For the two attributes with the highest number of missing values (individually) in your merged data set, either:
    \- consider if you can impute these missing values. If so describe the approach you have taken to impute missing values and justify why you have taken this approach; or
    \- if you decided you cannot impute missing values in an attribute then describe and justify why you have not done any imputation.

3. Describe what incorrect or impossible values you found in attributes in your merged data set, and provide how many such incorrect or impossible values there are for each attribute. Also, describe why you believe these values are impossible or incorrect.

4. Describe how you were dealing with the incorrect or impossible values identified in your merged data set (for example correcting them in some way or another).

**Clearly show your answers to questions 1. to 4.**

**Write a maximum of 400 words (15 lines of text). If you write more than these limits we will have to apply an over-word-limit penalty.**

**English writing mistakes and typographical errors will attract small penalties.**



1. The combination of three attributes with the highest number of missing values and the corresponding number of records with missing values are:

   

   marital_status	occupation	credit_card_number	

   ​            0                        0                            0                           1347

   

   P.S. My merged data set was cleaned following the steps in Task 2 so that the missing values might have been changed a lot. This task was finished with Python.

   

2. In my merged data set, the two attributes with the highest number of missing values are salary and marital_status.

   For salary, I performed "median value imputation". To start with, I found there were 2375 records which had a salary of -9999. I reckoned they were alternatives for missing values during data collection, and these values will extremely affect the attribute's distribution and measure of central tendency. Hence, I replaced those impossible values with NaN. Then, I draw the histogram of salary distribution and found it's a skewed distribution for numerical variables. For skewed data, a better measure of the center of data is the median. Hence, I replaced the missing value with the median counted from the non-null salary values, which was 85200.

   For marital_status, I performed "missing value imputation" by replacing all missing attribute values with the same constant label "not-specified". It is because martial statuses are various in type and an individual's marital status is unpredictable, so it's better to use a global constant to fill in the missing value.

   

3. I found the following types of incorrect values and their quantities, with reasons:

   salary: 2375 records are -9999. Salary can't be negative.

   weight: 1585 records are -99. Weight can't be negative.

   state: 185 records are in uppercase. It's incorrect to use both lowercase and uppercase for representing states, and I decide that the ones in lowercase are correct.

   age_at_consultation: 1632 records have unequal age_at_consultation and the interval between years of consultation and birth.



4. Dealing with the incorrect values above:

   salary: I replaced values of -9999 with NaN, and further replaced the missing value with the median. (Task 3.2)

   weight: I used bmi value and height value to calculate the correct weight value for each record with an incorrect weight.

   state: I converted all uppercase state abbreviations into lowercase.

   age_at_consultation: I replaced the age_at_consultation with the interval between years of consultation and birth.
   
   

## Question 9 (4.00)

**Task 4: Other data cleaning**

Perform other data cleaning tasks that you think are important, keeping in mind the **final use of the cleaned and merged data set, to examine links between an individual’s education, employment, and their health**.

Things you may wish to consider include (but are not limited to):

1. Do any of the attributes in your merged data set have data quality issues with regard to the data quality dimensions we discussed in Lecture 5 that are not covered by Tasks 2 and 3.

2. Are any data reduction or transformation tasks required?

3. Are there values that seem to be in the wrong attribute(s)? If so how can you correct them?

4. Any other problems you detected that you think are worth correcting.

You should consider up to four extra data exploration and data cleaning tasks, and for each describe what you have done, justify why you have done it (within the context of the final use of the cleaned data set described above), and any numerical results relevant to the task that you think are important.



**Clearly show your answers to questions 1. to 4.**

**Write a maximum of 400 words (15 lines of text). If you write more than these limits we will have to apply an over-word-limit penalty.**

**English writing mistakes and typographical errors will attract small penalties.**



1. Timeliness is a core data quality dimension. Our research topic involves health, but health consultation has limited time stability since it represents an individual's health condition at a point in time. It only makes sense if we are using up-to-date values, otherwise, if the time difference for health consultation and employment is too large, we will get the wrong conclusions. For reference, Australia kept health records for 7 years in law. In my merged data set at this stage, there are 965 records of which the interval in timestamps exceeds 7 years. So I chose to drop those records and only keep the records with a time interval of fewer than 7 years.

2. In Australia, the legal age for marriage and a credit card are both 18 years old. However, there are 2535 records of which age_at_consultation is less than 18 but marital_status is not recorded as "not-married", and there are 443 records of which age_at_employment is less than 18 but credit_card_number is not null. For correction, I replaced the martial_status of non-adult records' by consultation with "not-married", and replaced the credit_card_number of non-adult records by employment with "not-available". I found occupation attribute has the same problem with credit_card_number, so I also corrected this attribute in the same way.

3. Among my medical data set and my education data set, there are 2 records of which the first_name is “nan”, and 1 record of which the last_name is “null”. When reading CSV, they will be automatically recognized as missing values, which will affect further cleaning and analysis processes. To deal with this problem, I replaced these name values with the strings `"nan*" and "null*"`.

4. According to our research topic, data transformation can be performed. 

   As for education, I referred to the Australian Qualifications Framework (AQF) and replaced the education labels with integer values ranging from 0 to 10. This is because numeric attributes can reflect the level of education level directly, and it can benefit further model building for our research topic. 

   As for salary, I observe that the salary data are too large in scale. The data should be normalized to avoid reliance on the choice of measurement units. Hence, I utilized the MinMaxScaler to scale each salary value to fall within a smaller range of [0, 1].

