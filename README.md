# Google-Fiber---Google-Business-Int-Case-Study
This is the project I completed as a part of the Google Business Intelligence Certificate.

## Case Study Overview

The Google Fiber customer service team’s goal is to determine how often customers are calling customer support after their first inquiry; this will help leadership understand how effectively the team is able to answer customer questions the first time. The dashboard you create should demonstrate an understanding of this goal and provide your stakeholders with insights about repeat caller volumes in different markets and the types of problems they represent. As part of the interview process, you have been asked to create a dashboard that will: 

* Help them understand how often customers are calling customer support after their first inquiry; this will help leadership understand how effectively the team is able to answer customer questions the first time

* Provide insights into the types of customer issues that seem to generate more repeat calls

* Explore repeat caller trends in the three different market cities

* Design charts so that stakeholders can view trends by week, month and year.

## Data

Data was provided in the form of 3 CSV files. All 3 files had an identical format so no cleaning was necessary before loading them into tableau. 

The files contained data about the number of initial contacts to the Company's customer service team as well as the number of repeat contacts over a 7 day period following the first contact. A repeat contact is defined as any customer that called the customer service team more than once in a 7 day period following their initial contact. The data was structured as follows:

<img width="479" alt="image" src="https://github.com/user-attachments/assets/eac4cefa-8357-420b-8904-d08f16770058" />



* date Created = Date of first contact
* contacts_n = total Intital contacts on Date Created
* contacts_n_1 = Total contacts that called a second time 1 day after their initial contact
* contacts_n_2 = Total contacts that called a second time 2 days after their initial contact
* contacts_n_3 = Total contacts that called a second time 3 daya after their initial contact
* contacts_n_4 = Total contacts that called a second time 4 days after their initial contact
* contacts_n_5 = Total contacts that called a second time 5 days after their initial contact
* contacts_n_6 = Total contacts that called a second time 6 days after their initial contact
* contacts_n_7 = Total contacts that called a second time 7 days after their initial contact
* new_type = Coded column for Problem Type
* new_market = Coded column for Market


The problem type definitions were provided seperately by the management team. I used those definitions to create a helper table that I added to tableau as a supplement. This table was structered as follows:


<img width="168" alt="image" src="https://github.com/user-attachments/assets/d10882bc-2a8c-4118-8477-666eb93b709d" />


* new_type = Primary key from data table
* problem_type = problem types provided by management team

### Data Preparation
All tables were loaded into tableau. The 3 CSV files with data about call volumes were unioned within Tableau. The supplementle table with the problem types was also loaded into Tableau and a table relationship was created with the 2 new_type columns from each dataset. 

Three new calculated columns were created to address the businesses questions:

* Total Contacts = Aggregation of contacts_n. This number repreesents the total initial contacts to customer service
* Total Repeat Contacts = Aggregation of contacts_n_1, contacts_n_2, contacts_n_3, contacts_n_4, contacts_n_5, contacts_n_6, contacts_n_7. This number represents the total volume of repeat callers. 
* Rate of Repeat Contacts = Total Repeat Contacts divided by Total Contacts. This represents the total percentage of callers that called more than once over a 7 day period.

## Visualizations

The following dashboard was created within Tableau to give the Management Team the abiility to slice the data within each market and by problem type. 

<div>
    <a href="https://www.loom.com/share/7340f42788ed4fe7b802f34aab381e81">
      <p>PowerPoint - Google Fiber Executive Summary - PowerPoint - 12 January 2025 - Watch Video</p>
    </a>
    <a href="https://www.loom.com/share/7340f42788ed4fe7b802f34aab381e81">
      <img style="max-width:300px;" src="https://cdn.loom.com/sessions/thumbnails/7340f42788ed4fe7b802f34aab381e81-a1524f928ec7dd74-full-play.gif">
    </a>
  </div>

You can access the full interactive Dashboard on Tableau Public here:
https://public.tableau.com/app/profile/billie.jo.smith/viz/GoogleFiberCaseStudy_17361098727700/ExecutiveSummary

## Analysis

### Market 1

Market 1 is by far largets in terms of overall call volume:

<img width="485" alt="image" src="https://github.com/user-attachments/assets/7caf2c15-ebe3-46be-b74c-a668d6a6d06f" />

Market 1 has high rates of repeat callers in 3 categories:
* Account Management
* Internet and Wifi
* Technician Troubleshooting

<img width="491" alt="image" src="https://github.com/user-attachments/assets/0a5fd3ad-018d-4a5e-989c-4464f9948d1b" />


### Market 2

Market 2 has by far the lowest overall rate of repeat callers, but still a fairly high rate of repeat calls for Account Management

<img width="524" alt="image" src="https://github.com/user-attachments/assets/68136c46-ae69-4110-aa4b-c2f0725e1bde" />


### Market 3

Market 3 has a the highest rate of repeat callers, although markets 1 and 3 are both quite high.

<img width="513" alt="image" src="https://github.com/user-attachments/assets/6ec2417c-ba1f-4fbc-b85d-f6edc5fe77ab" />

Market 3 has a high rate of repeat callers in 3 categories:
* Account Management
* Internet and Wifi
* Scheduling

<img width="540" alt="image" src="https://github.com/user-attachments/assets/9e6f2d72-6ac7-4061-8382-84ea40770ae9" />

## Recomendations

### Next Steps

* Investigate the reasons for additional calls for Account Management in all 3 markets
* Determine why the number of repeat calls is higher than first contacts in Market 3 for Account Management Issues (this could be a data integrity issue)
* Investigate the reasons for repeat callers for Internet and Wifi in Markets 1 and 3
* Investigate the reasons for repeat callers for Scheduling in Market 3
* Review Customer service practices in market 2 and compare them to Markets 1 and 3 to determine why Market 2 has a significantly lower rate in all problem categories

Link to PDF of Executive Summary:

https://acrobat.adobe.com/id/urn:aaid:sc:US:59f850b1-eb1b-46e3-96d9-17f01f2c7f61





