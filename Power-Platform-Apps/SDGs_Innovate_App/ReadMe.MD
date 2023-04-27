# SDGs Innovate App

This is an application developed with the aim of promoting Gender Equality (the Sustainable Development Goal 5). The target of this goal is to achieve achieve gender equality and empower all women and girls.

This application is an entry for the Global Power Platform Bootcamp 2023 Lagos #GPPB2023NIG <a href="https://youtu.be/PUjrWXKrO_4" target="_blank">Click here to watch the short video demo</a>

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

Default Theme           |  Modified Theme
:-------------------------:|:-------------------------:
![App Setting on default theme](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/App_setting.PNG "Default Theme")|![Appp Setting on modified theme](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/setting_modifiedTheme.PNG "Modified Theme")



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

![Gender Equality Complaint Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/1bbd5f40277ffeb3874a2eeaad7c8aa190252f63/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Gender_Equality_Complaints_table_preview.PNG)

  
* Health Tip: this table holds the quotations that are displayed randomly on the home screen of the application for users.
Below are the created columns
  1. Tip Name - Text column
  2. Tip Description - text column
  3. Health Tip Category - choice column

![Health Tip Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/HealthTip_dataverse_table_preview.PNG)

  
* Skills: this table holds the details of the skills that would empower the female users to be better in their career or generate income easily.
Below are the created columns
  1. Name: text column
  2. Overview - text column (textarea format)
  3. VideoLink - URL column
  4. Skill Type - choice column (Vocational and Tech options)

![Skills Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Skills_dataverse_table_preview.PNG)

  
* UN SDGs: this table holds details of the 17 Sustainable Development Goal.
Below are the created columns
  1. Goal Id - autonumber column
  2. Goal Name
  3. Target
  4. Image

![UN SDGs Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/UNSDGs_table_preview.PNG)

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
Below are the created columns
  1. ApplicationID - autonumber column
  2. Email
  3. Full Name
  4. Job Role

![Job Application Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Job%20Application%20Table.PNG)


## App Screenshots
Below are screenshots of some of the screens in the application

Get Started Screen           |  Update Profile Screen
:-------------------------:|:-------------------------:
![Get Started Screen](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/GetStarted.PNG "Get Started Screen")|![Update Profile Screen](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/UpdateProfile.PNG "Update Profile Screen")

Login Screen without password input           |  Login Screen with password input
:-------------------------:|:-------------------------:
![Login Screen 1](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/RegisterdAppUser_loginScreen.PNG "Login Screen 1")|![Login Screen 2](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/RegisterdAppUser_loginScreen_onpasswordInput.PNG "Login Screen 1")

Home Screen           |  SDGs Screen
:-------------------------:|:-------------------------:
![Home Screen](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/Female_home.PNG "Home Screen")|![SDGs Screen](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/SDGs.PNG "SDGs Screen")

Skills Screen           |  Tech Screen        |  Tech Screen Preview
:-------------------------:|:-------------------------:|:-------------------------:
![Skill Screen](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/SkillUp.PNG "Skill Screen")|![Tech Screen](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/TechSkillPreview.PNG "Tech Screen")|![Tech Screen Details](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/TechSkill.PNG "Tech Screen Details")


Tech Skill Screen Preview           |  Vocational Skill screen preview        |  Job Bot Screen preview
:-------------------------:|:-------------------------:|:-------------------------:
![TechSkill Screen](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/TechSkill2.PNG "Tech Skill Screen")|![Vocational Skill Screen](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/VocationalSkill.PNG "Vocational Screen")|![Jobbot](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/Jobbot.PNG "Job Bot")

Health Tip Screen           |  SpeakUp Screen
:-------------------------:|:-------------------------:
![Health](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/HealthTips.PNG "Health Tip Screen")|![SpeakUp Screen](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/Speakup%20section.PNG "SpeakUp Screen")

<a href="https://github.com/giftwarieta/Business-Transformation-and-Automation/tree/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen">More Screen Preview</a>

## More details about app development
1. <a href="https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/AccessLogic_on_app.md">Access Logic on app</a>
2. <a href="https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/AppOnStartup_code.md">App Onstart property code (Power Fx functionality)</a>
3. <a href="https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Code_snippets.md">Code snippets</a>
4. <a href="https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Power_Automate_Flow.md">Power Automate Flow</a>


I hope you are learning more about how this app was built and some of its functionality 🌹👌👍👏

