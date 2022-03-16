# Yelp-DataSet-analysis-using-BigData-Tools
The Yelp dataset was originally released in order for students to do research and analysis in to how food trends begin and how they impact locations. The dataset includes data about businesses, reviews, users, checkins, tips, and photos. Here in my project I used users,review and business dataset.

## Table of Contents
1. [Introduction](##introduction)
2. [Goal](##goal)
3. [Technology Stack](##technology-stack)
4. [Bucket Calculation](##bucket-calculation)
5. [Project Architecture](##project-architecture)
6. [ER Diagram](##er-diagram)
7. [Analysis](##analysis)

## Introduction
Most businesses seek to get reviews on their goods and services one way or another. It is a most basic way for the business to improve their efficiency and subsequently their bottom-line. Get the review is not only the issue, ability to extract and visualize analytics from review data is critical to business success.

In this Project, we will use the yelp review dataset to analyze businesses and reviews over a period of time. Perhaps we will spot potential gaps in service delivery or see how business thrive in different scenarios.

Beyond processing this data, we will ingest the final output of our data processing in PowerBI and use the visualization tool to visualize various kinds of ad-hoc reports from the data.

## Goal
Goal is to create data pipeline for yelp dataset to finally load in hive external tables so that analysis team can make use of this data. Along with this goal is to extract required data using some free-form queries for geeral business usecases.

## Technology Stack
- HDFS
- Hive
- PowerBI

## Bucket Calculation

Block Size in HDFS = 128 MB

Size of review dataset = 5120 MB

5120/128 = 40

2^x = 40 where x will be number of buckets

Hence we will take number of bucket = 6

Size of user dataset = 3205 MB

3205/128 = 25

2^x = 25  where x will be number of buckets

Hence we will take number of bucket = 5


## Project Architecture

![image](https://user-images.githubusercontent.com/100192175/158570014-b898e40e-586f-41f2-ba52-9a4b3e798653.png)

## ER Diagram
<img width="540" alt="Yelp-ER-Diagram" src="https://user-images.githubusercontent.com/100192175/158572672-48e74fbd-1fc5-4955-a7f2-0e3a4251a2e7.png">

## Analysis

#### Top Users who posted reviews (by count)
<img width="658" alt="User_Review_Count" src="https://user-images.githubusercontent.com/100192175/158600926-6bf5117d-630e-41e5-8c0c-ca3af93dbf78.png">

#### Average Rating of business per year

#### Top users who posted funny reviews
<img width="960" alt="FunnyPerUser" src="https://user-images.githubusercontent.com/100192175/158602856-18e69751-aa69-45fb-bf81-0c989a512c65.png">

#### 
