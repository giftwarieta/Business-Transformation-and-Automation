# <a href="https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/ReadMe.MD">Back to ReadMe</a>

# Code Snippets

This section is meant to provide insights into some of the Power Fx codes used in the application

## Get Started Button

```
If(Connection.Connected=true,
Reset(Loginpwd);
Refresh('Daily Inspirational Quotes');
//Quote Selection
Set(varRandomNumber, RandBetween(1, 10));
Set(varqid, LookUp('Daily Inspirational Quotes', !IsBlank(QID)).QID);
Set(lowid, Min(varqid));
Set(highid,First(FirstN(SortByColumns('Daily Inspirational Quotes', "createdon",SortOrder.Descending))).QID);
Set(quoteid, Value(RandBetween(lowid,highid)));
Set(myrandomquote,LookUp('Daily Inspirational Quotes', RandBetween(lowid,highid) in QID, Quote & " - " & Author));
If(!IsBlank(LookUp(AppUsers, useremail in Email).Email),Set(varpass, true), Navigate('Update Profile'));,
Notify("Cannot proceed due to your internet connection issue. Please check your internet connection",NotificationType.Error, 3000));
```

## Login Button

![Login Screen Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/AppScreen/RegisterdAppUser_loginScreen_onpasswordInput.PNG "Login Screen Preview")

```
If(LookUp(AppUsers, useremail in Email).Password=Loginpwd.Text,
Set(varload,true);
//Quote Selection
Reset(Loginpwd);
Set(gender, LookUp(AppUsers,Email = useremail,Gender));
Set(varRandomNumber, RandBetween(1, 10));
Set(varqid, LookUp('Daily Inspirational Quotes', !IsBlank(QID)).QID);
Set(lowid, Min(varqid));
Set(highid,First(FirstN(SortByColumns('Daily Inspirational Quotes', "createdon",SortOrder.Descending))).QID);
Set(quoteid, Value(RandBetween(lowid,highid)));
Set(myrandomquote,LookUp('Daily Inspirational Quotes', RandBetween(lowid,highid) in QID, Quote & " - " & Author)) &&
Set(varpass, false) && If("Male" = Text(LookUp(AppUsers, useremail in Email).Gender),
Set(varload,false);
Navigate(Male_Home),
Set(varload,false);
Navigate(Home)),
Notify("Login failed. Please Check your password/internet connection and try again.",NotificationType.Error,3000));
```

## Female Home Screen Quotation display


Female User Home Screen Quotation Preview            |  Female Home Screen Birthday Message Preview Preview
:-------------------------:|:-------------------------:
![Female Home Quotation Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Female_quotation.PNG "Female Home Screen Quotation Preview")|![Female Home Screen Birthday Message Preview Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Female_birthday_msg.PNG "Female Home Screen Birthday Message preview")

```
If(Text(Today(),"dd/mm") in Text(LookUp(AppUsers, useremail in Email).DOB,"dd/mm"), "Happy Birthday " & username & "! May this day usher a new exciting phase in your life. Enjoy your celebration. - From the CEO", randomquote)
```

## Male Home Screen Quotation display
![Male Home Screen Quoatation Preview Preview](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Male_quotation.PNG "Male Home Screen Quotation Preview")

```
If(Text(Today(),"dd/mm") in Text(LookUp(AppUsers, useremail in Email).DOB,"dd/mm"), "Happy Birthday " & username & "! May this day usher a new exciting phase in your life. Enjoy your celebration. - From the CEO", "Take responsibility. Speak up. Stand with women and girls #WithHer")
```

## Password Change
![Password Change Process](https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Images/screenshots/Password_change_process.png "Password Change Process Screenshot")

On click the "Change Password Now" button, a confirmation popup message shows up
```
Set(varconfirm, true)
```
Popup display code to effect or cancel password change request
```
Set(varconfirm, false);
Set(varload, true);

Patch(AppUsers, LookUp(AppUsers,Email = useremail),
{
        Password: NewPwdTextInput.Text
});

Reset(NewPwdTextInput);
Reset(CurrentPwdTextInput);
Set(varload, false);
```

## <a href="https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/Power_Automate_Flow.md">Power Automate Flow</a>
