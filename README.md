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
I will be performing an App Review Sentiment Analysis on the Waze mobile app dataset so as to evaluate and understand the sentiments expressed in user reviews over a 15 year span; 2009 through 2023.</b> 

I will use data analysis techniques to determine whether the sentiments in these reviews are positive, negative, or neutral.</b>

I will also perform Exploratory Data Analysis on the dataset to answer a few questions derived along the way.</b>


 >note: The App Review Sentiment Analysis and EDA steps will be shown in detail within the Jupyter Notebook.


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
---
![ratings](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/f9439489-43fb-4538-a572-51aaec3152e2)



### As you can see, the above distribution of ratings chart gives us a clear picture of how many reviews fall into each rating category (from 1 to 5).

### The next step is to label the data with sentiments. We can use Textblob for this task.

 >note: TextBlob provides a polarity score ranging from -1 (very negative) to 1 (very positive) for a given text. We can use this score to classify each review’s sentiment as positive, neutral, or negative.

![sentlabels](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/30054ed1-189a-4be4-ac94-870ca95f641b)



### The dataset now includes sentiment labels for each review, classified as Positive, Negative, or Neutral based on the polarity score calculated by TextBlob.

### Lets now explore this dataset by analyzing the distribution of sentiments. It will give us a basic understanding of the general sentiment tendency in the reviews.<br>
---
![sents](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/3ec64920-1b98-4930-80a5-fd531573d960)


### In addition to the app having high ratings, reviewers also had many positive words in the reviews for the app.

### Lets now explore the relationship between the sentiments and the ratings. This analysis can help us understand whether there is a correlation between the sentiment of the text and the numerical rating. For this task, we can see how sentiments are distributed across different rating levels.
---
![sentsbyrate](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/a6544ea5-6e82-470a-b262-3c0c349ce86c)


### As you can see, most of the positive reviews fall within rating number 5 and most of the negative reviews fall within rating number 1. So there is a correlation between the sentiment of the text and the numerical rating.

### Let’s perform a text analysis of the dataset to identify common words or themes within each sentiment category.
---
![textblobpos](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/4a2dd42a-76b5-459b-9570-de83e1d9464c)
![textblobneg](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/a25e0aa7-4cee-486a-8701-1dab73f319d0)
![textblobneu](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/e1ce06f4-ff81-4b02-84cb-0d714f9f960c)

### As you can see, there are alot of positive words used in the review text for the positive sentiment.


# Exploratory Data Analysis
---
<p>
In my analysis I explore and answer the following questions:

1. From the distribution of ratings chart, which rating has the most user reviews? Least user reviews?
2. From the distribution of sentiments chart, what are the total number of user reviews from each sentiment? 
3. Based off the findings from the sentiment distribution across ratings chart, the negative sentiment is at its highest in rating number 1.
  How many reviews make up his sentimtent?
4. What app version has the most user reviews?
5. Are there any major differences in sentiments between app versions 3.9.4.0 and 4.99.1.1(latest app version in dataset)? If so, what are they?
6. Based off the findings from the distribution of negative sentiments across the top 17 app versions chart, which version has the most user reviews that are negatively ranked and how many are there?
7. Based off the findings from the distribution of years by user reviews chart, which year contains the most user reviews and which has the least overall?
8. Based off the findings from the sentiment distribution by year chart, the year with the most negative sentiments is 2021.
   How many negative user reviews were placed and the percentage out of all negative sentiments?
9.  Out of the 8,182 negative reviews placed in year 2021, how many are from app version 4.73.0.3?
10.  Out of the 7,326 negative user reviews in rating number 1 for year 2021, how many are from app version 4.73.0.3?
11. Based off the findings from the year distribution by ratings chart, We see that in rating number 1 there is a large percent of user reviews from year 2021 than any other year.  
     How many user reviews make up the positive, negative and neutral sentiments?




# Summary of Findings
--- 
### Question 1: From the distribution of ratings chart, which rating has the most reviews? Least reviews?
![Q1a](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/5eb23ef6-d310-4809-99c9-0365b7640770)

- Rating number 5 has 466,125 reviews which makes up 67% of all the reviews.
- Rating number 2 has 20,473 reviews which makes up only 3% of all the reviews.

### Question 2:   From the distribution of sentiments chart, what are the number of reviews for each sentiment? Which has the most reviews?
![Q2](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/a8cc75bd-71df-455c-821a-29cd2e619d7f)

- The positive sentiment has a total of 472,194 reviews which equates to 68% of all reviews.
- The neutral sentiment has a total of 181,093 reviews which equates to 26% of all reviews.
- The negative sentiment has a total of 38,851 reviews which equates to 6% of all reviews.

### Question 3: Based off the findings from the sentiment distribution across ratings chart, the negative sentiment is at its highest in rating number 1. How many reviews make up this sentiment?
![Q3a](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/2e12adba-e660-4fef-befb-e08468c2e836)
![Q3b](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/ea1018b4-fdc4-4e44-86ae-3dbb1349ce80)

- There are a total of 17,758 reviews which make up the negative sentiment in rating number 1 (this makes up 46% out of all negative sentiments).

### Question 4: What app version has the most user reviews?
![top17](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/3731e367-2aaa-4b7e-8729-f7fe57f9f98a)

- App version 3.9.4.0 has the most user reviews than any other version at 28,448 (released <b>March 11, 2015<b>).

### Question 5:  Are there any major differences in sentiments between app versions 3.9.4.0 and 4.99.1.1(latest app version in dataset)? If so, what are they?
![pie3940](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/c4c55cbd-721f-46d9-ab23-041634ee8862)
![pie49911](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/a4d8cfb4-53cf-4008-a0bd-3cb57ff8e76c)

 >note: The latest app version in the dataset is 4.99.1.1 which was released on <b>November 16, 2023.<b>

- Both app versions have a large percentage of positive sentiments overall. Version 3.9.4.0 has a noticable lead, showing 69% of its user reviews being positive as opposed to version 4.99.1.1 showing only 42%.

### Question 6: Based off the findings from the distribution of negative sentiments across the top 17 app versions chart, which version has the most user reviews that are negatively ranked and how many are there?
![sentacrosstop17](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/8020848e-f313-4075-a8b6-92ee904d0c7a)
![top17neg](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/0de3afdd-7ad6-4e6c-b7d3-5bdec84dc63a)

- Version 4.73.0.3 has the most reviews that are negatively ranked with a total of 4,254, which is 11% out of all negative sentiments.

### Question 7:  Based off the findings from the distribution of years by user reviews chart, which year contains the most user reviews and which has the least overall?
![yearsbyuserreview](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/c430e6f1-f629-4162-8ac9-a326dbf2397b)
![allyears](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/60b4c875-2643-4580-9060-341f614e773f)

- Year 2016 has a total of 118,139 reviews which equates to 17% of all reviews in a 15 year span.
- Year 2009 has a total of 240 reviews which equates to 4% of all reviews in a 15 year span.

### Question 8:  Based off the findings from the sentiment distribution by year chart, the year with the most negative sentiments is 2021. How many negative user reviews were placed and the percentage out of all negative sentiments?
![sentbyyear](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/6c8025d4-8ecc-41a3-8cd6-624d27598161)
![Q8neg](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/23f2cf00-53b8-4601-aebd-a781e5b40a85)


![yr2021a](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/8fd694e1-93cb-421e-a70e-ec1c29a5a1bd)
![yr2021b](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/4b4df050-9839-4555-9e1e-316aede26fed)

- For the year 2021, there was a total of 8,182 reviews placed which is 21% of all the negative sentiments.
  
### Question 9:  Out of the 8,182 negative reviews placed in year 2021, how many are from app version 4.73.0.3?
![47303neg](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/6cf0acce-79d3-4f0e-bfad-52c48bdc82ca)

- Out of the 8,182 negative reviews in year 2021 approximatley 4,244 (52%) of them are from the author app version 4.73.0.3.
  
### Question 10:  Out of the 7,326 negative user reviews in rating number 1 for year 2021, how many are from app version 4.73.0.3?
![Q10a](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/52b1e246-abf4-492e-85b2-6d5941abe688)
![Q10b](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/0d2b59db-a74b-455c-84d6-2f8d65a0cbc2)

- Out of the 7,326 negative reviews in rating number 1 for year 2021, approximatley 4,136 (56%) of them are from the author app version 4.73.0.3.
  
### Question 11: Based off the findings from the year distribution by ratings chart, We see that in rating number 1 there is a large percent of user reviews from year 2021 than any other year. How many user reviews make up the positive, negative and neutral sentiments?
![Q11](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/1e1bb1d2-6414-43c5-96cb-192b0d2bbd4a)


![2021rating1pos](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/37c47c77-1a9a-4a0c-8353-e646d7ff24a9)
![2021rating1neg](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/252f4abc-8330-4c40-af1e-7012145b8fda)
![2021rating1neut](https://github.com/KHard2Bme/Waze_Review_Sentiment_Analysis/assets/146769989/e7f85203-7049-4c9a-93ca-569a8896e837)
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
I originaly chose this dataset so that i could perform a Sentiment Analysis on opinions expressed in the review text, to determine viewer's attitude towards the Waze mobile app, but after spending quite some time performing an exploratory data analysis on the data I discovered some very interesting trends and patterns.

Based on the waze mobile app dataset we can tell that most of the user reviews were ranked high at rating number 5, in addition to having a very positive overall sentiment.

This is very good news for Management and Application Development Teams, but we also need to look at high reviews that fall within rating number 1, especially those categorized within the negative sentiment. This will help us to understand what the pain points are and then fixes can be applied to next releases.

In regards to user reviews ranked within rating number 1, 31% (17,758) of these are categorized as having a negative sentiment.

Of those categorized as negative, 38% (7,326) of these were placed in 2021 with approximately 56% (4,136) of the users on app version 4.73.0.3.

If you look at the data from the negative sentiments point of you, 6% (38,851) of all user reviews were categorized as negative.

Of those negatively categorized, year 2021 had the most user reviews than any other year by 21% (8,182), with approximately 52% (4,244) of the users being on app version 4.73.0.3.  

So, as you can see 2021 was the year which had the most reviews categorized as negative, with more than 50% of the users being on app version 4.73.0.3 (released on April 6, 2021). What exactly were the major issues affecting this app?

if I were to read each negative review (about 4,200) I would most likely understand what specific issues there are plaguing users, but instead i chose to gauge the count of negative reviews captured from every app version released after version 4.73.0.3.

If you look at the app versions report; Figure 1, you will see that as the release versions increase the count of negative sentiments decreases (trend), with an occasional up and down fluctuation.

It appears that Management has paid close attention to many of the user concerns and resolved these issues over time within newer releases.

In the end, the folks at Waze were able to respond quickly to this issue, resulting in them having most of their user reviews ranked high at number 5 and having a very positive sentiment overall.





