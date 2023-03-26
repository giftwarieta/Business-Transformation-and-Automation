# Certificate Automation

This certification automation is aimed at generating a customized pdf certificate to training attendees. Test the solution by <a href="https://forms.office.com/r/FxKqgd1U48" target="_blank">clicking here</a>.
## Business Case
Over the past few years, an EduTech company that offers online training courses to individuals across Africa, has experienced significant growth and now has hundreds of participants enrolled in each course.
 
Previously, the company used a manual process to issue training certificates to participants who completed a course. This process involved reviewing attendance forms and manually creating and sending certificates to participants. However, with the increasing number of participants and courses, this process has become overwhelming and time-consuming.

To address this challenge, you've been requested to implement a cost-effective automated system for issuing training certificates to participants. The system will be designed to ensure that every participant who fills the attendance form receives a certificate in a timely and efficient manner.

To accomplish this, you'll need to develop a system that can:

* Automatically generate a unique certificate for each participant who fills the attendance form, including the name of the course, the name of the participant and date of certificate issue.
* Automatically send the certificate to the email address provided by the participant in the attendance form.

## My Approach:
Using the Agile methodology, I implemented the solution by leveraging on #sharepoint and #powerautomate
* Created a sharepoint list that contains the following columns
  * Your Full Name
  * Your Email Address
  * Answers' Column for each of the below questions:
  1. How could the training/workshop be improved?
  2. How likely are you to recommend this training/workshop to a friend or colleague?
  * Completion Time

* Create a Microsoft Form that contains the below fields
  * Your Full Name
  * Your Email Address
  * How could the training/workshop be improved?
  * How likely are you to recommend this training/workshop to a friend or colleague?
  * Completion Time

* Created a backend flow using Power automate to implement the process flowchart whose image is seen below


The image below, shows the process flowchart of the solutionscreenshot of a sample certificate sent to a participant.
![Automation Flowchart](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/Certification_Automation/Images/Certificate_generation_automation_flowchart.jpg)

The image below, shows a sample certificate screenshot sent to a participant.
![Sample Certificate screenshot](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/Certification_Automation/Images/automated_certificate_screenshot.PNG)


The image below, shows screenshots of the participant attendance form designed with Microsoft Form. Kindly note that the layout can be changed to different layout
![Attendance Form Home Page](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/Certification_Automation/Images/Attendance_form_homepage.PNG)

![Attendance Main Form](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/Certification_Automation/Images/Attendance_MainForm.PNG)

## Benefits of this automation
By automating this process, I was able to streamline the administrative tasks associated with issuing training certificates and ensure that every participant receives their certificate promptly. This also helps to enhance the overall experience for participants and reinforce the value of your company's courses. Additionally, the automated system will free up your staff's time, enabling them to focus on developing and delivering high-quality courses to your growing base of participants.


Test the solution by <a href="https://forms.office.com/r/FxKqgd1U48" target="_blank">clicking here</a>.
