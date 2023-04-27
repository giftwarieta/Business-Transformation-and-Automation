# <a href="https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/ReadMe.MD">Back to ReadMe</a>

# Access Logic on App
1. On first login, the user is prompted to update his/her profile with Gender, Date of Birth and password. This stage is critical in the application functionality as it determines the screens a user can access and certain privileges the user have. By default, the user is given a **"User"** right.

![Update Profile Screen](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/UpdateProfile.PNG)

2. On subsequent login, if the user has been registered as a user in the AppUsers dataverse table, only password would be requested.

![Login Screen](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/RegisterdAppUser_loginScreen.PNG)

3. If a female is logged in, the home menu and screens available for views are different from that which is accessible by the male user as the app is mainly built to promote Gender Equality - empower women and female children who uses the app - skillUp opportunities and SpeakUp functionality.

Below is a code snippet of navigating between home screen based on gender

![App Footer](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Footer_menu.PNG)

```
If("Male" = Text(LookUp(AppUsers, useremail in Email).Gender),Navigate(Male_Home),Navigate(Home));
```

Below is a code snippet of navigating between footer menus based on gender

Female User Home Screen           |  Male User Home Screen
:-------------------------:|:-------------------------:
![Female User Home Screen](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/Female_home.PNG "Female User Home Screen")|![Male User Home Screen](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/male.PNG "Male User Home Screen")


```
If("Male" = Text(LookUp(AppUsers, useremail in Email).Gender), maleglobalnavitem, globalnavitem);
```


## <a href="https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/AppOnStartup_code.md">Navigate to On App Startup (Power Fx functionality) Section</a>
