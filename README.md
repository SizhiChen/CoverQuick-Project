# CoverQuick-Project
## 1.	Introduction

CoverQuick, an AI-powered tool, assists job seekers globally in creating job documents such as resumes and cover letters. The demographics of the users include students, career changers, and immigrants looking to apply to remote roles in various industries. In this project, we analyzed the CoverQuick dataset of job applications and resumes to ascertain the primary industries, roles, and demographics the company should focus on. The data is structured in a JSON format, which was used to determine where best to allocate CoverQuick's marketing efforts to reach their ideal customers.

The dataset used in this project contains 11,976 unique users, each characterized by their ID, Resume Content, and Job Description. The data cleaning process was not initiated at the start but was performed sectionally to ensure data integrity and accuracy.

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/4e4b245b-c776-4a81-9380-1c7724bbd03f)

#### Figure 1. Data Description 

## 2.	Preliminary Analysis

The dataset contained several essential resume sections including Education, Experience, and Skills. Each of these sections underwent an initial analysis:

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/48f486fc-10d6-440d-953c-009f9addab42)

#### Figure 2. Number of Education Background Histogram

In Figure 2, it shows the Number of Education Background histogram. Before we started to make the histogram, we did the data cleaning for the Education part. 

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/bf1e4db9-ce38-4f98-b923-d9742ac67b40)

#### Figure 3. Education Data Cleaning Process.

In Figure 3, we did the data cleaning for the Education. What we did exactly is that we find some of the dictionary in JSON doesn’t contain all the elements. However, it is understandable that some people may have some issues in some sections, but we believe that the school’s name should not be missing. So, we go though all the dictionaries in JSON file and if the school’s name is empty, we consider that this user does not have this educational background. After cleaning the data for the education section, a histogram was produced showing the number of educational backgrounds each user has. It revealed that most users have 1 to 3 educational backgrounds, with only a few having more than 3.

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/aca200df-e89a-4a2c-91ce-245b220a23d0)

#### Figure 4. Number of Skill Histogram

In Figure 4, it shows the Number of Skill histogram. Before we started to make the histogram, we did the data cleaning for the skill part.

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/c25c5522-bb39-400a-8dfa-9670e4cbc930)

#### Figure 5. Skill Data Cleaning Process.

In Figure 5, we did the same thing with the education part, we examine the section name in skill part, and if it is empty, we consider that this user does not have this skill. After the data cleaning, it revealed that most users have less than 5 skills, with only a handful of users having more than 5.

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/94dd9acb-d91d-4249-a7ce-7b2e8760bd42)

#### Figure 6. Number of Experience Background Histogram

In Figure 6, it shows the Number of Experience Background in histogram. Before we started to make the histogram, we did the data cleaning for the working experience part.

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/2b7719e7-1c2d-4ab4-9659-113b3fb7ae83)

#### Figure 7. Working Experience Data Cleaning Process.

We did the same thing for the Working Experience part. After the data was cleaned for the experience section and revealed that most users have work experience between 2 to 5 jobs, few have more than 5, and some have less than two job experiences.

# 3.	Country and Age Analysis

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/c7c07edd-353e-4a04-90a2-144d99750a0c)

#### Figure 8. Histogram for Top 10 Country by Users

The country column needed extensive data cleaning due to spelling errors and inconsistent writing formats (e.g., Canada and CA). After standardizing the country names, a histogram was created to visualize the data. We can see in the Histogram that most of the user is from the United States, and the second is Canada, etc. Figure 9 below shows the code about how we are checking the spelling mistake.

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/9bdc7e98-4056-4d9c-8469-59f2ccf2c4a9)

#### Figure 9. Checking the Spelling Mistake for Country

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/1633a0b7-c8e4-442f-aec4-759d27e92703)

#### Figure 10. Age Distribution

In Figure 10, we have the histogram for age distribution. The age of users was calculated based on their earliest graduation year, assuming that they graduated on time at 22 years old. We can see that most of the users are from 20 to 30 years old. And only a few of them higher than 40.

# 4.	Advanced Analysis

The advanced analysis involved determining the top 10 industries, skills, companies, and locations by user count, and evaluating the quality of all resumes and those specific to the top three industries.

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/0615b196-1457-407f-9f26-d194135fc2b2)

#### Figure 11. Top 10 Industries

In Figure 11, we have the Top 10 industries. Utilizing OpenAI to determine the industry for each resume revealed that most users are applying for roles within the Information Technology, followed by Healthcare, Advertising and Marketing, Business, Retail, Education, Customer Service, Human Resources, and Software Development. At the beginning, we want to build or find a model and train only 3000 of them. However, we can’t achieve it because the best model we have is only 36% accuracy. So, finally, we just run all the job descriptions one by one and then create this histogram.

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/2c3f199b-e81e-446e-bbf1-5e881fdd01d6)

#### Figure 12. Top 10 Skills by Users

In Figure 12, we have the top 10 skills by users. Given the majority of users are from the Information Technology industry, it is unsurprising that, apart from Excel and PowerPoint, the majority of top skills were coding related.

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/1938ebd0-cd82-4c97-b387-8787a2b53def)

#### Figure 13. Top 10 Companies by Users Worked

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/2d5c50b1-536e-4d56-8c40-0aad1175ce9d)

#### Figure 14. Top 10 Locations by Users Worked

In Figure 13 and 14, we also find the top 10 companies by Users and their top 10 locations to work. Interestingly, we found that most of people are work remotely, it probably because of the Covid situation.

# 5.	Quality of Resumes

The quality of the resumes was determined based on six criteria:

Presence of key sections (Education, Experience, Skills)  
Length of the resume  
Usage of action verbs  
Usage of pronouns  
Number of bullet points  
Number of spelling mistakes  

Each of these criteria was categorized as Poor, Good, or Excellent based on a predetermined measurement standard. Here are all the measurement standards:
1. Whether the resume has important section?  
If any sections from education, experience, and project is empty, we consider it to be Poor.  
Besides, for all other users who have all 3 sections, if the user doesn’t put skill into the resume, we consider it to be Good.  
Others will all be Excellent.  

2. How long is the resume?  
If the resume contains 300 to 500 words, we consider it to be Excellent.  
If the resume contains less than 200 words or more than 1000 words, we consider it to be Poor.  
Others will all be Good.  

3. Did the User use the action verb?  
If the User uses less than 5 action verbs, we consider it to be Poor.  
If the User uses action verbs between 5 to 10, we consider it to be Good.  
All the Users use action verbs more than 10, we consider it to be Excellent.  

4. Did the User use the pronoun?  
If the User doesn’t use pronoun, we consider it to be Excellent.  
If the User uses pronoun between 1 to 3, we consider it to be Good.  
All the Users use pronoun more than 3, we consider it to be Poor.  

5. How many bullet points are there in the resume?  
If the User has more than 10 bullet points, we consider it to be Excellent.  
If the User has bullet point between 3 to 10, we consider it to be Good.  
All the Users have bullet point less than 3, we consider it to be Poor.  

6.	How many spelling mistakes are there in the resume?  
If the User has less than 10 spelling mistakes, we consider it to be Excellent.  
If the User has spelling mistake between 10 to 50, we consider it to be Good.  
All the Users have spelling mistakes of more than 50, we consider it to be Poor.  

Figure 15 below shows the measurement standards example.

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/66045b2a-1ced-4b27-b1ad-fcbfafb6ee09)

#### Figure 15. Measurement Standards Example

Based on the overall scoring, resumes with more than two Poor ratings were deemed overall Poor. Conversely, resumes with no Poor ratings and more than two Excellent ratings were deemed overall Excellent. All other resumes were categorized as Good. Figure 16 below shows the Quality histogram for all the resumes.

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/20f0f130-dcd7-45c8-bc3a-86b55b9dfb47)

#### Figure 16. Quality Histogram for all the Resumes

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/a5637c05-fcda-4062-be8a-c548b59e2296)

#### Figure 17. Quality of Resumes for Information Technology Companies

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/d4149076-83c5-4c59-9ba0-e2203018b7c6)

#### Figure 18. Quality of Resumes for Healthcare Companies

![image](https://github.com/SizhiChen/CoverQuick-Project/assets/46178324/e0824160-1cf2-4ea4-9542-6a0238ae5a53)

#### Figure 19. Quality of Resumes for Advertising and Marketing Companies

In Figure 17, 18, and 19, we also make the top 3 industries quality of resumes.  
In summary, this comprehensive analysis provides valuable insights into the preferred industries, skill sets, and the quality of resumes in the CoverQuick dataset. These insights are crucial to strategizing and optimizing CoverQuick's marketing efforts to attract its target users.

# Reference
1.	What is AI Analytics? (2022, May 24). Anodot. https://www.anodot.com/learning-center/ai-analytics/

2.	CoverQuick Log In. (n.d.). https://app.coverquick.co/


