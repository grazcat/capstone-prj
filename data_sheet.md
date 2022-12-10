# Datasheet Template

As far as you can, complete the model datasheet. If you have got the data from the internet, you may not have all the information you need, but make sure you include all the information you do have. 

## Motivation

**- For what purpose was the dataset created?**

The data-set aims to answer the following key questions:

    - Does various predicting factors which has been chosen initially really affect the Life expectancy? What are the predicting variables actually affecting the life expectancy?
    - Should a country having a lower life expectancy value(<65 increase its healthcare expenditure in order to improve its average lifespan?
    - How does Infant and Adult mortality rates affect life expectancy?
    - Does Life Expectancy has positive or negative correlation with eating habits, lifestyle, exercise, smoking, drinking alcohol etc.
    - What is the impact of schooling on the lifespan of humans?
    - Does Life Expectancy have positive or negative relationship with drinking alcohol?
    - Do densely populated countries tend to have lower life expectancy?
    - What is the impact of Immunization coverage on life Expectancy?

- **Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)? Who funded the creation of the dataset?**

The data was collected from WHO (World Health Organization) and United Nations website with the help of Deeksha Russell and Duan Wang.
 
## Composition

- **What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)?**

he data-set related to life expectancy, health factors for 193 countries has been collected from the same WHO data repository website and its corresponding economic data was collected from United Nation website. Among all categories of health-related factors only those critical factors were chosen which are more representative. It has been observed that in the past 15 years , there has been a huge development in health sector resulting in improvement of human mortality rates especially in the developing nations in comparison to the past 30 years. Therefore, in this project we have considered data from year 2000-2015 for 193 countries for further analysis. The individual data files have been merged together into a single data-set. On initial visual inspection of the data showed some missing values. As the data-sets were from WHO, we found no evident errors.
The final merged file(final dataset) consists of 22 Columns and 2938 rows which meant 20 predicting variables. All predicting variables was then divided into several broad categories:​Immunization related factors, Mortality factors, Economical factors and Social factors.

- **How many instances of each type are there?**
There are 2938 instances

- **Is there any missing data?**

Missing data was handled in R software by using Missmap command. The result indicated that most of the missing data was for population, Hepatitis B and GDP. The missing data were from less known countries like Vanuatu, Tonga, Togo, Cabo Verde etc. Finding all data for these countries was difficult and hence, it was decided to exclude these countries from the final model data-set.
Null fields have been filled using the average of the related dimensions for running the linear model

- **Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by    doctor–patient confidentiality, data that includes the content of individuals’ non-public communications)?**

Yes. It mostly consists of medical data but they are aggregated data. They can be traced back to the single country.

## Collection process

- **How was the data acquired?**
The data-set related to life expectancy, health factors for 193 countries has been collected from the same WHO data repository website and its corresponding economic data was collected from United Nation website. 
- **If the data is a sample of a larger subset, what was the sampling strategy?** 
It has been observed that in the past 15 years , there has been a huge development in health sector resulting in improvement of human mortality rates especially in the developing nations in comparison to the past 30 years. Therefore, in this project we have considered data from year 2000-2015 for 193 countries for further analysis.

- **Over what time frame was the data collected?**
2000-2015

## Preprocessing/cleaning/labelling

- **Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)? If so, please provide a description. If not, you may skip the remaining questions in this section.**

The individual data files have been merged together into a single data-set. On initial visual inspection of the data showed some missing values. As the data-sets were from WHO, we found no evident errors. Missing data was handled in R software by using Missmap command. The result indicated that most of the missing data was for population, Hepatitis B and GDP. The missing data were from less known countries like Vanuatu, Tonga, Togo, Cabo Verde etc. Finding all data for these countries was difficult and hence, it was decided that to exclude these countries from the final model data-set. 

- **Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)?**
N/A
 
## Uses

- **What other tasks could the dataset be used for?**
N/A
- Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses? For example, is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) or other risks or harms (e.g., legal risks, financial harms)? If so, please provide a description. Is there anything a dataset consumer could do to mitigate these risks or harms? 
N/A
- **Are there tasks for which the dataset should not be used? If so, please provide a description.**
N/A

## Distribution

- **How has the dataset already been distributed?**
It is distributed by [Kaggle](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who). There might also be other places where the dataset is available.

- **Is it subject to any copyright or other intellectual property (IP)license, and/or under applicable terms of use (ToU)?**

Other: The data-sets are made available to public for the purpose of health data analysis by WHO.

## Maintenance

- **Who maintains the dataset?**
As far the authors of the datasheet know, it is unmaintained.
