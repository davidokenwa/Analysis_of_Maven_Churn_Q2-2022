# **Data-Driven Decision Making: Maven Telecom Churn Minimization Strategy**

> Customer churn is a major concern with subscription-based companies. What is it, and how can it be minimised? 
> In this BI consultancy project, I advised the CMO of a telecoms company on how to reduce churn.

|                             ![Churn Pic](https://github.com/davidokenwa/Analysis_of_Maven_Churn_Q2-2022/blob/main/churn_flaticon.jpg)                             | 
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------:| 
| **Churn Icon  from [Flaticon](https://www.flaticon.com/free-icons/failure)** |

In this article, I write about how I analysed and visualised 7043 customer data of Maven Communications, a 
California-based telecommunications company and the advice I gave its senior executives on minimising churn.

Every business wants to attract and retain customers. That’s how they grow. However, as in other aspects of life, 
businesses lose some customers and gain others. Customer churn is the percentage of customers who discontinue their 
subscriptions within a period. It can also be called churn rate or rate of attrition. On the other hand, growth rate 
is the percentage of new subscribers who joined a company in a given period. 

For a company to expand its customer base, its growth rate must exceed the churn rate. You can read more about churn 
rate in this [Investopedia article](https://www.investopedia.com/terms/c/churnrate.asp)

Churn rate is an important factor in the telecommunications industry. In most areas, many telecoms compete; thus, 
it is easy for subscribers to move from one company to another. 


## **Background and Dataset**
The data for this project contained information on all 7,043 customers of Maven Communications in Q2 2022. Each record 
represents one customer and includes details about their demographics, location, tenure, subscription services, status 
for the quarter (joined, stayed, or churned), and more. There were 37 columns in total. A portion of the data is shown 
in the screenshot. You can access the dataset [here](https://www.mavenanalytics.io/data-playground). 

|  ![raw data](https://github.com/davidokenwa/Analysis_of_Maven_Churn_Q2-2022/blob/main/raw%20data%20snippet.png)  | 
|:----------------------------------------------------------------------------------------------------------------------:| 
|                                                **Snippet of Raw Data**                                                 |

As a BI consultant, I wanted to find out the net growth or churn rate, separate the customers into segments (high-value 
and low-value) based on revenue generated, analyse the behaviour of customers in various segments, find out why 
customers left and map out strategies to reduce churn. I also wanted to see the ideal churning customer profile and 
staying profile. The dataset provided by [Maven Analytics](https://www.linkedin.com/company/maven-analytics/posts/?feedView=all) 
was a super exciting dataset to work with. At first, I had an “analyst’s block” (akin to writer’s block). I had to do 
some preliminary research, brainstorming and exploration to know the next steps for Maven Communications.

## **Project Steps**

I followed the steps outlined below to arrive at the dashboard and recommendations.
1. Preliminary research
2. Data cleaning
3. Data exploration
4. Data visualization
5. Key recommendations

| ![project steps](https://github.com/davidokenwa/Analysis_of_Maven_Churn_Q2-2022/blob/main/project%20steps.png) | 
|:--------------------------------------------------------------------------------------------------------------:| 
|         **Project Steps. Maven Churn Challenge, July 2022.** _Designed by David Okenwa in PowerPoint_          |

The tool used for the cleaning, processing and visualisation was Microsoft Excel. The Excel features I used here include
basic operations (addition, subtraction, multiplication and division, sum, average, percentages etc.), Pivot Tables, 
VLOOKUP, conditionals (COUNTIF, COUTIFS, SUMIFS), Filter, Sort, data labels, etc. One small but helpful function in my 
analysis was the ‘$’ sign for relative and absolute references. I made extensive use of it.

### **1. Preliminary Research**

Data analysts may often be required to analyse data in fields they do not have expertise in. To better understand the 
data and give more tangible insight, preliminary research on the industry/business would greatly help. Before working on
the data, I researched customer churn and the telecoms industry. From my research, I understood that churn rate is 
particularly important for the communications industry because the competition is intense, and it is very easy to switch from 
one to another. I also researched zip codes to learn how they work and how they are significant for telecom companies. The
preliminary research helped me overcome my analyst’s block.

|                                                                   ![researching](https://github.com/davidokenwa/Analysis_of_Maven_Churn_Q2-2022/blob/main/windows_unsplash.jpg)                                                                   | 
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:| 
| **Photo by [Windows](https://unsplash.com/@windows?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/research?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)** |

### **2. Data Cleaning**
The importance of ensuring data integrity, correcting wrong or inaccurate data, identifying missing data, and converting
from one data type to the other cannot be overstated. DataCamp recently shared a very helpful data cleaning checklist on
the [DataCamp LinkedIn page](https://www.linkedin.com/posts/datacampinc_data-cleaning-checklist-activity-6948658073720774656-z-34?utm_source=linkedin_share&utm_medium=member_desktop_web). 
It guides you on how to identify and resolve dirty data.

|                                                                     ![cleaning pic](https://github.com/davidokenwa/Analysis_of_Maven_Churn_Q2-2022/blob/main/jeshoots_unsplash.jpg)                                                                     | 
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:| 
| **Photo by [JESHOOTS.COM](https://unsplash.com/@jeshoots?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/cleaning?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)** |

In this step, I checked for duplicate values, missing values, wrong formatting, and inconsistent formatting. The dataset
was clean but checking for these gave me confidence in the dataset I needed to proceed to exploration.

| ![cleaned data](https://github.com/davidokenwa/Analysis_of_Maven_Churn_Q2-2022/blob/main/clean%20data%20snippet.png) | 
|:--------------------------------------------------------------------------------------------------------------------:| 
|                                    **Cleaned Data.** _The data was already clean_                                    |



### **3. Data exploration**

I enjoyed this part of the analysis. Here, I dug into the data, sliced, diced, and plotted charts to find patterns in 
the data for myself. I observed many patterns in the data, most of which correlated with my research. 

I observed 26.6 per cent of Maven’s customers churned in the last quarter. This was greater than the total amount who 
joined (14.9%) and resulted in a net loss of 11.7%.


| ![customer net loss](https://github.com/davidokenwa/Analysis_of_Maven_Churn_Q2-2022/blob/main/customer_loss.png) | 
|:----------------------------------------------------------------------------------------------------------------:| 
|                                              **Net Customer Loss**                                               |

Those who subscribed to the month-to-month subscription had much higher churn rates than the 1-year and 2-year subscribers.

| ![contract type](https://github.com/davidokenwa/Analysis_of_Maven_Churn_Q2-2022/blob/main/churn_by_contract-type.png) | 
|:---------------------------------------------------------------------------------------------------------------------:| 
|                   **Churn by Contract Type.** _Month-by-month subscribers have the highest churn._                    |

Eighty per cent of the revenue was generated from the top 40% of the customers (I tagged them the high-value customers).
I divided the data into two segments—high-value and low-value customers—and analysed the data to find the 
similarities and differences in their behaviour: their churn rates, their reasons for quitting, and what type of 
subscription they did. The high-value customers churned much less and mainly did the one or two-year subscription. 
Low-value customers were high-risk customers—they churned quickly—and largely subscribed on a month-to-month basis. Both segments had 
similar reasons for quitting, most of which were better competitor offers and dissatisfaction with the service.


| ![category analysis](https://github.com/davidokenwa/Analysis_of_Maven_Churn_Q2-2022/blob/main/churn%20category%20analysis.png) | 
|:------------------------------------------------------------------------------------------------------------------------------:| 
|                                             **High-value vs Low-Value Customers**                                              |

I dived deep into the top two reasons for churn in both high and low-value customers and saw that fibre-optic internet service 
is a source of concern for Maven. Some improvements need to be made to the fibre-optic internet service.

| ![deep dive](https://github.com/davidokenwa/Analysis_of_Maven_Churn_Q2-2022/blob/main/deep%20dive.png) | 
|:------------------------------------------------------------------------------------------------------:| 
|                                **Deep Dive: Top Two Churn Categories**                                 |

I analysed the top reasons customers gave for leaving. Concernedly, many persons churned because of the attitude of 
support persons and service providers. 

| ![churn reasons](https://github.com/davidokenwa/Analysis_of_Maven_Churn_Q2-2022/blob/main/reasons%20for%20leaving.png) | 
|:----------------------------------------------------------------------------------------------------------------------:| 
|                                             **Top Reasons Customers Left**                                             |

I visualised the ideal churn and stay profile. This highlighted several things at a glance, such as that fibre-optic 
internet service needs to be improved upon and staying customers make a two-year subscription whereas churning customers
make month-to-month subscriptions. The ideal churn profile from the data is a single female living in San Diego. She 
subscribes month-to-month, pays by mailed cheque, makes no additional subscription and has referred us to zero or one person.

| ![ideal profiles](https://github.com/davidokenwa/Analysis_of_Maven_Churn_Q2-2022/blob/main/ideal%20profiles.png) | 
|:----------------------------------------------------------------------------------------------------------------:| 
|                                        **Ideal Churn and Stay Profiles**                                         |

### **4. Data visualization**

After exploration, I had the task of arranging the insights gathered in a single-page dashboard. This was the most 
interesting part of the analysis for me. I had gotten inspiration from many awesome dashboards from the 
[winning entries](https://www.linkedin.com/posts/maven-analytics_maven-airlines-challenge-finalists-activity-6943509513886982144-GK3K?utm_source=linkedin_share&utm_medium=member_desktop_web) 
of the previous Maven Analytics challenge and wanted to try out some of them. It was even more fun because most of the 
dashboards I saw were done with specialised BI tools like Power Bi and Tableau; I wanted to replicate them in Excel, a 
less specialised tool for building dashboards.

| ![dashboard](https://github.com/davidokenwa/Analysis_of_Maven_Churn_Q2-2022/blob/main/000Dashboard_FULL.png) | 
|:------------------------------------------------------------------------------------------------------------:| 
|                  **Maven Churn Dashboard** _Designed by David Okenwa with Microsoft Excel_                   |

### **5. Key Recommendations**

After the preliminary exploration, I deep-dived into the data to answer three strategic questions to help Maven Communications:
1. How can we convert low-value to high-value customers?
2. What key areas does Maven need to improve on that will have the most effect on churn reduction? 
3. How can they drive growth with a focus on retention?
I found the answers for all these from the data and gave the following recommendations.

#### **Churn minimisation**
1. Aggressively market and incentivise one and two-year plans. This will help us in two ways
- One and two-year plans have the highest retention rate by far
- It would convert low-value customers into high-value customers

2. Improve the internet service, especially Fiber Optic. This would reduce churn due to competitors and dissatisfaction

3. Customer service and technical support staff should be trained in emotional intelligence and customer relations.
This would help save $580k churned due to staff's attitude.

#### **Retention-focused growth strategy**
We've only captured 0.002% of the total California population. To grow with a focus on retention;
4. Expansion drives should focus on cities with proven high retention rates.

5. Referral bonuses should be given as this will not only drive growth but also
increase the loyalty of customers. Our most loyal customers have referred us



---

### **Relevant Links**

Thank you for reading up to this point! Here are some relevant links:

* [Medium article](https://davidokenwa.medium.com/thoughts-behind-beautiful-dashboards-9fb8b24d9f6d)
* [LinkedIn Post](https://www.linkedin.com/posts/david-okenwa_david-okenwa-onyx-nobel-prize-data-challenge-activity-6936211331779805184-7q0O?utm_source=linkedin_share&utm_medium=member_desktop_web)
* [Dataset](https://www.mavenanalytics.io/data-playground)
* [DataCamp data cleaning checklist](https://www.linkedin.com/posts/datacampinc_data-cleaning-checklist-activity-6948658073720774656-z-34?utm_source=linkedin_share&utm_medium=member_desktop_web)
* [Flaticon](https://www.flaticon.com/search?word=team). (Get icons for free).
* [Unsplash](https://unsplash.com/). (Get beautiful images)