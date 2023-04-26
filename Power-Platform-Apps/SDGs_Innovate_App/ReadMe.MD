# SDGs Innovate App

This is an application developed with the aim of promoting Gender Equality (the Sustainable Development Goal 5). The target of this goal is to achieve achieve gender equality and empower all women and girls.


## Business Case
SDG 5 aims to achieve gender equality by ending all forms of discrimination, violence and any harmful practices against women and girls in the public and private spheres. It also calls for the full participation of women and equal opportunities for leadership at all levels of political and economic decision-making.

Women especially in the developing countries of the world are not priviledged to be empowered like the males especially in the areas of financial and skill empowerment.

My goal with the SDGs Innovate App, is to create a platform where the female users would be able to learn skills which will eventually empower them financially and for career growth.

## My Approach:
Using the Agile methodology, I implemented the solution by leveraging on ##Powerapp canvas app, Power Virtual Agent, Dataverse and Power Automate

## UI/UX
The app is built with simplicity and user's ease of interractivity in mind especially when accessing the app on their mobile phone.

The choice of color is deliberate as it symbolizes gender equality. According to the International women's day website, the use of these three colors is very significant: purple, green and white.
![App color code used](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/App_color_codes_used.png)

While using the application, users have the options to toggle between the theme (default or modified theme) of their choice from the Setting section of the app as shown below.

![Appp Setting on default theme](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/App_setting.PNG)

![Appp Setting on modified theme](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/setting_modifiedTheme.PNG)

## Dataverse table creation
Below are the tables created

* AppUser: this table holds the information of login users who have now been authorized to use the app. This table plays a key role in identifying the user's gender and admin role determining privileges to viewable screens.
Below are the created columns
  1. Email - email column
  2. Given Name - text column
  3. Full Name - text column
  4. Gender - choice column (Female and Male options only)
  5. DOB - Date Only column
  6. User Role - Choice column (User and Admin)
  7. Password - text

![AdminUser Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/AppUser_table_preview.PNG)

  
* Daily Inspirational Quote: this table holds the quotations that are displayed randomly on the home screen of the application for users.
Below are the created columns
  1. QID - autonumber column
  2. Quote
  3. Author
  4. Category

![Daily Inspirational Quote Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Daily_Inspirational_Quote_table_preview.PNG)

* Gender Equality Complaint: this table holds all logged in complaints from the Speak Up screen of the app. This screen is only accessible by female users.
Below are the created columns
  1. Email - email column
  2. First Name - text column
  3. Last Name - text column
  4. Full Name - text column
  5. Complain - Choice column which enables multiple selection
  6. Additional Comment - text column in text area format

![Gender Equality Complaint Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Gender_Equality_Complaints_table_preview.PNG)

  
* Health Tip: this table holds the quotations that are displayed randomly on the home screen of the application for users.
Below are the created columns
  1. Tip Name - Text column
  2. Tip Description - text column
  3. Health Tip Category - choice column

![Health Tip Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Daily_Inspirational_Quote_table_preview.PNG)

  
* Skills: this table holds the details of the skills that would empower the female users to be better in their career or generate income easily.
Below are the created columns
  1. Name: text column
  2. Overview - text column (textarea format)
  3. VideoLink - URL column
  4. Skill Type - choice column (Vocational and Tech options)

![Daily Inspirational Quote Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Daily_Inspirational_Quote_table_preview.PNG)

  
* UN SDGs: this table holds details of the 17 Sustainable Development Goal.
Below are the created columns
  1. QID - autonumber column
  2. Quote
  3. Author
  4. Category

![Daily Inspirational Quote Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Daily_Inspirational_Quote_table_preview.PNG)

* Job Vacancy: this table holds the information about available job vacancies. This is a vital table used for the jobbot embeded in the app. (<a href="https://github.com/giftwarieta/Business-Transformation-and-Automation/tree/main/Power-Platform-Apps/Gifted_chatbot" target="_blank">read more here</a>)
Below are the created columns
  1. JobID - autonumber column (Format is JV{DATETIMEUTC:yyyyddMM}-{SEQNUM:1})
  2. Recruiting Department - text column
  3. Vacancy Type - choice column (Internal and External options)
  4. Job Vacancy Name - text column
  5. Job Description - text column (textarea format)
  6. Job Requirement - text column (textarea format)
  7. Due Date - Date only column

![Job Vacancy Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Job%20Vacancies.PNG)

* Job Application: this table holds the information of users who applied for a job role via the job bot in the application. This is a vital table used for the jobbot embeded in the app. (<a href="https://github.com/giftwarieta/Business-Transformation-and-Automation/tree/main/Power-Platform-Apps/Gifted_chatbot" target="_blank">read more here</a>)
Below are the required columns
  1. ApplicationID - autonumber column
  2. Email
  3. Full Name
  4. Job Role

![Job Application Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Job%20Application%20Table.PNG)







## Benefits of this automation
By automating this process, I was able to streamline the administrative tasks associated with issuing training certificates and ensure that every participant receives their certificate promptly. This also helps to enhance the overall experience for participants and reinforce the value of your company's courses. Additionally, the automated system will free up your staff's time, enabling them to focus on developing and delivering high-quality courses to your growing base of participants.


Test the solution by <a href="https://forms.office.com/r/FxKqgd1U48" target="_blank">clicking here</a>.
