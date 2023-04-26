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

```
If(Text(Today(),"dd/mm") in Text(LookUp(AppUsers, useremail in Email).DOB,"dd/mm"), "Happy Birthday " & username & "! May this day usher a new exciting phase in your life. Enjoy your celebration. - From the CEO", randomquote)
```

## Male Home Screen Quotation display

```
If(Text(Today(),"dd/mm") in Text(LookUp(AppUsers, useremail in Email).DOB,"dd/mm"), "Happy Birthday " & username & "! May this day usher a new exciting phase in your life. Enjoy your celebration. - From the CEO", "Take responsibility. Speak up. Stand with women and girls #WithHer")
```
