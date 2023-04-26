# <a href="https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/ReadMe.MD">Back to ReadMe</a>

# App OnStart Property Code

On App Startup, the app connects to all the dataverse tables which the app uses. Hence internet avalaibility is key to usage.
The app randomly selects an Inspirational quote from the "Daily Inspirational Quote" table for displaay on the home screen of the app for only the female users (the male user gets a static quote). But on the birthday of the user, it displays a birthday message as seen in the image below (this logic is on the male_home screen)

  * The different menus utilized in the app, from female home menu, male menu to footer menu is generated onstart of the application.
  * Button properties and theme properties are also defined here.
Below is a codesnippet of all the codes used on the app onstart property. You can easily copy it for testing


```
//Connecting to User account
"Welcome " & Office365Users.MyProfileV2().givenName;
Set(userfname, Office365Users.MyProfileV2().givenName);
Set(userlname, Office365Users.MyProfileV2().surname);
Set(username, Office365Users.MyProfileV2().displayName);
Set(useremail, Office365Users.MyProfileV2().mail);
Set(userimage, User().Image);


//Set theme color

Set(altcolor, RGBA(0, 153, 0, 1));
Set(maincolor, RGBA(116, 39, 116, 1));

//Button Hover
Set(althover, RGBA(0, 153, 0, 0.2));
Set(mainhover, RGBA(116, 39, 116, 0.2));


//Quote Selection
Set(varRandomNumber, RandBetween(1, 10));
Set(varqid, LookUp('Daily Inspirational Quotes', !IsBlank(QID)).QID);
Set(lowid, Min(varqid));
Set(highid,First(FirstN(SortByColumns('Daily Inspirational Quotes', "createdon",SortOrder.Descending))).QID);
Set(quoteid, RandBetween(lowid,highid));
Set(randomquote,LookUp('Daily Inspirational Quotes', RandBetween(lowid,highid) in QID, Quote & " - " & Author));


//Female Footer menu creation
Set(globalnavitem,
Table(
{
    MenuText: "Home",
    MenuIcon: Icon.Home,
    ScreenToGo: Home
},
{
    MenuText: "Health Tips",
    MenuIcon: Icon.Hospital,
    ScreenToGo: 'Health Tips'
},
{
    MenuText: "SDGs",
    MenuIcon: Icon.Globe,
    ScreenToGo: SDGs
},
{
    MenuText: "Setting",
    MenuIcon: Icon.Settings,
    ScreenToGo: Setting
}
)
);

//Male Footer menu creation
Set(maleglobalnavitem,
Table(
{
    MenuText: "Home",
    MenuIcon: Icon.Home,
    ScreenToGo: Male_Home
},
{
    MenuText: "Health Tips",
    MenuIcon: Icon.Hospital,
    ScreenToGo: 'Health Tips'
},
{
    MenuText: "SDGs",
    MenuIcon: Icon.Globe,
    ScreenToGo: SDGs
},
{
    MenuText: "Setting",
    MenuIcon: Icon.Settings,
    ScreenToGo: Setting
}
)
);

//Female Main Menu
Set(globalMenu,
Table(
{
    MenuText: "SkillUp",
    MenuIcon: Icon.Ribbon,
    ScreenToGo: SkillUp
},
{
    MenuText: "Chat With JobBot",
    MenuIcon: Icon.Message,
    ScreenToGo: 'Chat With Jobbot'
},
{
    MenuText: "Setting",
    MenuIcon: Icon.Settings,
    ScreenToGo: Setting
},
{
    MenuText: "Health Tips",
    MenuIcon: Icon.Hospital,
    ScreenToGo: 'Health Tips'
},
{
    MenuText: "Speak Up",
    MenuIcon: Icon.Support,
    ScreenToGo: 'Speak Up'
},
{
    MenuText: "Admin",
    MenuIcon: Icon.AddUser,
    ScreenToGo: Admin
},
{
    MenuText: "SDGs",
    MenuIcon: Icon.Globe,
    ScreenToGo: SDGs
},
{
    MenuText: "About App",
    MenuIcon: Icon.Information,
    ScreenToGo: 'About App'
},
{
    MenuText: "Exit App",
    MenuIcon: Icon.Leave,
    ScreenToGo: 'Exit App'
}));

//Male Main Menu
Set(maleglobalMenu,
Table(
{
    MenuText: "Health Tips",
    MenuIcon: Icon.Hospital,
    ScreenToGo: 'Health Tips'
},
{
    MenuText: "About App",
    MenuIcon: Icon.Information,
    ScreenToGo: 'About App'
},
{
    MenuText: "Admin",
    MenuIcon: Icon.AddUser,
    ScreenToGo: Admin
},
{
    MenuText: "SDGs",
    MenuIcon: Icon.Globe,
    ScreenToGo: SDGs
},
{
    MenuText: "Setting",
    MenuIcon: Icon.Settings,
    ScreenToGo: Setting
},
{
    MenuText: "Exit App",
    MenuIcon: Icon.Leave,
    ScreenToGo: 'Exit App'
}));

```

## <a href="https://github.com/giftwarieta/Business-Transformation-and-Automation/blob/main/Power-Platform-Apps/SDGs_Innovate_App/ReadMe.MD">Navigate to On App Startup (Power Fx functionality) Section</a>
