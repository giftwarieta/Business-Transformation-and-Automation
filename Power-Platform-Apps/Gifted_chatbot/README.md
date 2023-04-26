# Gifted Job Vacancy Bot
This repository hold the entire project file for the Gifted Job Vacancy Bot, the documentations and the GitHub actions for committing changes and deployment.

## Solution Overview
This Solution is developed to enable staffs of an organization to check available job vacancies (and apply for vacant roles of their interest) and events in the organization by simply chatting with a bot called Gifted.
<a href="https://giftwarieta.com.ng/Giftedchatbot.html" target="_blanK">Click here</a> to have a feel and interact with the bot using a web browser feel. You can trigger the conversation with a "hi" or greeting the bot.

## Solution Justification
The solution helps improve Staff vacancy notification experience at the comfort of the user with just a simple "hi" to trigger the communication.

## Solution Taxonomy
Below are the listed order through which this solution was developed, after which each element of the deployment will be documented accordingly.

1. #### Business requirement document evaluation.

* Problem review.
* Use case discovery.
* Design conceptualization.
* FitGap Analysis.
* Database Design
* Workflow design and Power automate flow creation
* Chatbot Solution Design

2. #### Database design
  The database for event and job vacancy were built with Microsoft Dataverse for easy integration purpose

* Job Vacancy: this table holds the information about available job vacancies. This is a vital table used for the jobbot embeded in the app.
Below are the created columns
  1. JobID - autonumber column (Format is JV{DATETIMEUTC:yyyyddMM}-{SEQNUM:1})
  2. Recruiting Department - text column
  3. Vacancy Type - choice column (Internal and External options)
  4. Job Vacancy Name - text column
  5. Job Description - text column (textarea format)
  6. Job Requirement - text column (textarea format)
  7. Due Date - Date only column

![Job Vacancy Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/Gifted_chatbot/Images/Job%20Vacancies.PNG)

* Job Application: this table holds the information of users who applied for a job role via the job bot in the application. This is a vital table used for the jobbot embeded in the app.
Below are the required columns
  1. ApplicationID - autonumber column
  2. Email
  3. Full Name
  4. Job Role

![Job Application Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/Gifted_chatbot/Images/JobApplication_Table.PNG)

* Events: this table holds about events
Below are the required columns
  1. Name - text column
  2. Description - text column (text area format)
  3. Start Date - Date only column
  4. End Date - Date only column
  5. Availability - text column

![Event Dataverse Table Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/Gifted_chatbot/Images/Event_dataverse.PNG)

3. #### Power Automate Flow
  * Job Search Flow
  * Event Search Flow

## Design Approach
The design concept follows a nutural language process (NLP) approach with regards to inquiry about a job role availability.

Below are screenshots from the Power virtual agent work flow
![Flow](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/Gifted_chatbot/Images/jobbotlogicPreview1.PNG)
![Flow](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/Gifted_chatbot/Images/jobbotlogicPreview2.PNG)

## Chatbot Outlook
![Chat bot preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/Gifted_chatbot/Images/JobbotApp.PNG)


I hope this has been helpful in understanding how this solution was created.

Now let's go check the Application Lifecycle Management (ALM) model, click here to explore
