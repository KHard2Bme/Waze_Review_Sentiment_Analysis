# Waze Review Sentiment Analysis 🚗 🚙
---

## Table of Contents

- [Project Overview](#project-overview)
- [Python Libraries Used](#python-libraries-used)
- [Data Sources](#data-sources)
- [App Review Sentiments Analysis](#app-review-sentiments-analysis)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Summary of Findings](#summary-of-findings)
- [Figure 1](#Figure-1)
- [Results from Findings](#results-from-findings)


# Project Overview
---
I will be performing an App Review Sentiment Analysis on the Waze mobile app dataset so that I can evaluate and understand the sentiments expressed in user reviews over a 15 year span; 2009 through 2023.</b> 

I will use data analysis techniques to determine whether the sentiments in these reviews are positive, negative, or neutral.</b>

I will also perform Exploratory Data Analysis on the dataset to answer a few questions derived along the way.</b>


 >note: The App Review Sentiment Analysis and EDA steps will be shown in detail within the Waze Review Sentiment Analysis.ipynb Notebook.


# Python Libraries Used
---
*pandas, numpy, seaborn, matplotlip, datetime


# Data Sources
---

The primary dataset used for this analysis is the "WAZE_REVIEWS.csv" file obtained from Kaggle which contains 780,073 rows and 9 columns.<br>

The dataset covers user reviews regarding the Waze mobile app during the years 2009 through 2023.<br>

I am also using website uptodown.com for verification of dates each Waze author app version was released on; https://waze.en.uptodown.com/android/versions).<b>


# App Review Sentiments Analysis
---

### Lets first explore the dataset by analyzing the distribution of ratings. It will provide insight into the overall sentiment of the reviews.<br>

![dist1](https://github.com/user-attachments/assets/74e2637e-6bd9-46f4-9320-099fdc453dd1)
![ratings](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/f9439489-43fb-4538-a572-51aaec3152e2)


### As you can see, the above distribution of ratings chart gives us a clear picture of how many reviews fall within each rating category.
---
### The next step is to label the data with sentiments. We can use Textblob for this task.

 >note: TextBlob provides a polarity score ranging from -1 (very negative) to 1 (very positive) for a given text. We can use this score to classify each review’s sentiment as positive, neutral, or negative.

![app_review](https://github.com/user-attachments/assets/e4daa9d6-c1de-42f4-bcf8-b42b3788dc96)


### The dataset now includes sentiment labels for each review classified as positive, negative, or neutral based on the polarity score calculated by TextBlob.
---

### Lets now explore this dataset by analyzing the distribution of sentiments. It will give us a basic understanding of the general sentiment tendency in the reviews.<br>

![sent1](https://github.com/user-attachments/assets/92e5f57f-a53f-47c5-a326-2dccaf72bd5a)
![sents](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/3ec64920-1b98-4930-80a5-fd531573d960)

### In addition to the app having high ratings, reviewers also had many positive words in the reviews for the app.
---
### Lets now explore the relationship between the sentiments and the ratings. This analysis can help us understand whether there is a correlation between the sentiment of the text and the numerical rating. For this task, we can see how sentiments are distributed across different rating levels.

![sent_dist](https://github.com/user-attachments/assets/7d68131c-7818-43ca-be74-c18932084045)
![sentsbyrate](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/a6544ea5-6e82-470a-b262-3c0c349ce86c)

### As you can see, most of the positive reviews fall within rating number 5 while most of the negative reviews fall within rating number 1. So there is a correlation between the sentiment of the text and the numerical rating.
---
### Let’s finally perform a text analysis of the dataset to identify common words or themes within each sentiment category.

![textblobpos](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/4a2dd42a-76b5-459b-9570-de83e1d9464c)
![textblobneg](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/a25e0aa7-4cee-486a-8701-1dab73f319d0)
![textblobneu](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/e1ce06f4-ff81-4b02-84cb-0d714f9f960c)

### As you can see, there are alot of positive words used in the review text for the positive sentiment.


# Exploratory Data Analysis
---
<p>
In my analysis I explore and answer the following questions:

1. From the distribution of ratings chart, which rating has the most user reviews? Least user reviews?
2. From the distribution of sentiments chart, what are the total number of reviews for each sentiment?
3. Based off the sentiment distribution across ratings chart, the negative sentiment is at its highest in rating number 1. 
   How many reviews make up this sentiment?
4. How many app versions are there and what app version has the most user reviews?
5. Are there any major differences in sentiment distribution between app versions 3.9.4.0 and 4.99.1.1? If so, what are they?
6. Based off the negative sentiment distribution across Top 10 app versions chart, which version has the most reviews that are negatively ranked and how many are there?
7. The dataset is made up of how many years? 
   Based off the distribution of years by user reviews chart, which year contains the most reviews and which has the least overall?
8. Based off the sentiment distribution by year chart, how many negative reviews were placed in year 2021 and what is the percentage out of all negative sentiments?
9.  Out of the 8,182 negative reviews placed in year 2021, how many are from app version 4.73.0.3?
10.  Out of the 7,326 negative user reviews in rating number 1 for year 2021, how many are from app version 4.73.0.3?
11.  Based off the distribution of sentiments in rating number 1 for year 2021 chart, we see that in rating number 1 there is a large percent of reviews from year 2021 than any other year.    
   How many user reviews make up the positive, negative and neutral sentiments?






# Summary of Findings
--- 
### Question 1: From the distribution of ratings chart, which rating has the most reviews? Least reviews?
![Q1a](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/5eb23ef6-d310-4809-99c9-0365b7640770)

- Rating number 5 has 466,125 reviews which makes up 67% of all the reviews.
- Rating number 2 has 20,473 reviews which makes up only 3% of all the reviews.

### Question 2: From the distribution of sentiments chart, what are the total number of reviews for each sentiment?
![Q2](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/a8cc75bd-71df-455c-821a-29cd2e619d7f)

- The positive sentiment has a total of 472,194 reviews which equates to 68% of all reviews.
- The neutral sentiment has a total of 181,093 reviews which equates to 26% of all reviews.
- The negative sentiment has a total of 38,851 reviews which equates to 6% of all reviews.

### Question 3: Based off the sentiment distribution across ratings chart, the negative sentiment is at its highest in rating number 1. How many reviews make up this sentiment?

![3](https://github.com/user-attachments/assets/75d91040-cd7c-4c82-ac37-b8625738b73f)
![3a](https://github.com/user-attachments/assets/99793ddf-1486-4a16-8ad0-249f06fed3cd)

- There are a total of 17,758 reviews which make up the negative sentiment in rating number 1 (this makes up 31% of all negative sentiments).

### Question 4:  How many app versions are there and what app version has the most user reviews?

![4a](https://github.com/user-attachments/assets/44bb1b16-012b-4337-92d9-70e271857893)
![4](https://github.com/user-attachments/assets/407c7fad-6b3f-40f9-9a93-ac8d40a2db3f)

- There are a total of 324 app versions, and app version 3.9.4.0 has the most user reviews than any other at 28,448 (released <b>March 11, 2015<b>).

### Question 5:  Are there any major differences in sentiment distribution between app versions 3.9.4.0 and 4.99.1.1? If so, what are they?
![pie3940](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/c4c55cbd-721f-46d9-ab23-041634ee8862)
![pie49911](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/a4d8cfb4-53cf-4008-a0bd-3cb57ff8e76c)

 >note: The latest app version in the dataset is 4.99.1.1 which was released on <b>November 16, 2023.<b>

- Both app versions have a large percentage of positive sentiments overall. Version 3.9.4.0 has a noticable lead, showing 69% of its user reviews being positive as opposed to version 4.99.1.1 showing only 42%.

### Question 6: Based off the negative sentiment distribution across Top 10 app versions chart, which version has the most reviews that are negatively ranked and how many are there?
![6a](https://github.com/user-attachments/assets/7f0dfaf7-c329-4eff-8d86-0049953748ed)
![6](https://github.com/user-attachments/assets/8f6026c5-586a-43e8-a8fc-e71da77a85d6)


- The app version with the most negative reviews is 4.73.0.3, which is 42% (4,254) of the top 10 app versions and 11% (4,254) of entire dataset. 

### Question 7: The dataset is made up of how many years? Based off the distribution of years by user reviews chart, which year contains the most reviews and which has the least overall?
![yearsbyuserreview](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/c430e6f1-f629-4162-8ac9-a326dbf2397b)
![7](https://github.com/user-attachments/assets/c546b6d1-426d-4d9f-99ca-ad761346ad6d)

- The dataset is comprised of 15 years worth of data
- Year 2016 has a total of 118,139 reviews which equates to 17% of all reviews.
- Year 2009 has a total of 240 reviews which equates to 4% of all reviews.
 
### Question 8: Based off the sentiment distribution by year chart, how many negative reviews were placed in year 2021 and what is the percentage out of all negative sentiments?
![sentbyyear](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/6c8025d4-8ecc-41a3-8cd6-624d27598161)
![Q8neg](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/23f2cf00-53b8-4601-aebd-a781e5b40a85)

![8](https://github.com/user-attachments/assets/4c636a24-f014-4a08-9ecf-01d97ba2e3a0)
![8a](https://github.com/user-attachments/assets/a0a3be45-5604-4ed2-9384-d2e4b22b551d)

- For the year 2021, there was a total of 8,182 reviews placed which is 21% of all the negative sentiments.
  
### Question 9:  Out of the 8,182 negative reviews placed in year 2021, how many are from app version 4.73.0.3?
![9](https://github.com/user-attachments/assets/1acbdd1b-5770-45ed-98d6-b79e28605d1b)


- Out of the 8,182 negative reviews in year 2021 approximatley 4,244 (52%) of them are from the author app version 4.73.0.3.
  
### Question 10:  Out of the 7,326 negative user reviews in rating number 1 for year 2021, how many are from app version 4.73.0.3?
![10](https://github.com/user-attachments/assets/7c85e45d-33b6-4e6b-a81d-085e9e196a83)
![10a](https://github.com/user-attachments/assets/a9d2e864-0679-4c04-a317-51b6d23e2764)


- Out of the 7,326 negative reviews in rating number 1 for year 2021, approximatley 4,136 (56%) of them are from the author app version 4.73.0.3.
  
### Question 11: Based off the distribution of sentiments in rating number 1 for year 2021 chart, we see that in rating number 1 there is a large percent of reviews from year 2021 than any other year. How many user reviews make up the positive, negative and neutral sentiments?

![Q11](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/1e1bb1d2-6414-43c5-96cb-192b0d2bbd4a)
![11](https://github.com/user-attachments/assets/ad3716a5-df96-468b-964d-74fa4ab08212)
![11next](https://github.com/user-attachments/assets/d6f479ce-db39-4501-b327-57fa621a5545)
![11third](https://github.com/user-attachments/assets/5f915317-4b3c-4d49-8caa-e279e4347522)


![Q11pie](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/b17dea89-bc44-40ac-8f90-bc0d693efad4)


- For positive sentiments the total number is 1,707 which equates to 9% for 2021.
- For negative sentiments the total number is 7,326 which equates to 38% for 2021.
- For neutral sentiments the total number is 10,048 which equates to 53% for 2021.

# Figure 1  
List of negative user reviews starting from app version 4.73.0.3 ( released on April 6, 2021) to version 4.99.1.1 ( released on November 16, 2023)
---
![releasevers1](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/a77280a9-40ec-429f-a64d-54a6c11104ab)
![releasevers2](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/1a3af5ac-a6f0-4df4-b145-86810a2c0d3e)
![releasevers3](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/56a2420b-234c-40ea-b7f6-ed0633ed8887)



# Results From Findings
---
I originaly chose this dataset so that i could perform a Sentiment Analysis on opinions expressed in the review text, this helping me determine viewer's attitude towards the Waze mobile app. After spending quite some time performing an exploratory data analysis on the data I discovered some very interesting trends and patterns.

Based on the Waze mobile app dataset we can tell that most of the user reviews were ranked high at rating number 5, as well as having a very positive overall sentiment.

These stats are very impressive for the Management Team, but they must also understand the reviews which fall within rating number 1, those having high negative sentiments.

Knowing this will enable the company to respond quicker at developing patches and rolling them out in a timely fashion in new releases. In this manner the higher ratings and sentiments always outnumber the lower ones.

In regards to user reviews ranked within rating number 1, 31% (17,758) of these are categorized as having a negative sentiment.

Of those categorized as negative, 38% (7,326) of these were placed in 2021 with approximately 56% (4,136) of the users on app version 4.73.0.3.

If you look at the data from the negative sentiments point of you, 6% (38,851) of all user reviews were categorized as negative.

Of those categorized as negative, the year 2021 had the most user reviews than any other year by 21% (8,182), with approximately 52% (4,244) of the users being on app version 4.73.0.3.  

So, as you can see 2021 was the year which had the most reviews categorized as negative, with more than 50% of the users being on app version 4.73.0.3. What exactly were the major issues affecting this app version?

It was not possible for me to try and read through roughly 4,000 reviews for app verion 4.73.0.3, but instead i chose to analyze the trend of negative reviews captured starting with 4.73.0.3 all the way up to the latest release being 4.99.1.1.

If you look at the app versions report; Figure 1, you will see that as newer releases came out the count of negative sentiments decreased over time; with an occasional up and down fluctuation.

You can surmise that management has paid close attention to many of the user concerns and resolved a large portion of them over time.

In the end, the folks at Waze were able to respond quickly to these complaints, resulting in their most recent reviews ranking high at number 5 and having a very positive sentiment overall.





