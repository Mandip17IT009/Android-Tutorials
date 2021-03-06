# Welcome to Android Tutorials
Purpose : Learning Only

## Software Required: Android Studio

## Tutorial 1

Introduction to Android and Create “Custom Message” application. That will display “Custom Message” in the middle of the screen in the Black color with the Yellow background.

Learning Outcome: We can learn how to change the background color in the application adding color in color.xml and add custom message in the app with black color.  

[Tutorial-1](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR1_17IT009.rar)
    [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/PR1.JPG)

## Tutorial 2

Create an android application to calculate sum of two numbers and gives result in Toast Message.

Learning Outcome: In above application we can create a functionality in which user can enter two numbers and then click on ADD button it will display sum of that number in toast message for to develop this app we use TextView, EditText, Button and Toast Message functionalities of the android. 

[Tutorial-2](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR2_17IT009.rar)
    [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/PR2.JPG)

## Tutorial 3

Create an application that will display Toast (Message) on specific interval of time.

Learning Outcome: In above application we can create a functionality in which every several intarval of time it can show toast message of the timer seconds. For that in this we use chronometer provided by android which can start and after every 5 second it will display the current second of the timer.

[Tutorial-3](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR3_17IT009.rar)
  [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/PR3.1.JPG)

## Tutorial 4

Create a temperature converter Application. (Fahrenheit-Celsius)

Learning Outcome: In above application we can create a functionality in which user enter the value which can give the Celsius to Fahrenheit and Fahrenheit to Celsius for that we use EditText, ToggleButton for to convert give value either in Celsius or Fahrenheit and Button, when submit is clicked it popup converted value in Toast massage. 

[Tutorial-4](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR4_17IT009.rar)
  [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/PR4.1.JPG)

## Tutorial 5

Create a login application with following features: 
1. Successful Login message in TextView with Green background if Username & password is correct
2. Failure message in TextView with Red background if Username or password is incorrect.
3. Disable Login Button after three wrong login attempts.
4. Close application if user selects Cancel Button.

Learning Outcome: In above application we can create a functionality of  Login page in which user enter his Username and password for the login. For that we use EditText for to take username and password, TextView for to display the number of  attempts and the login success or fail message, when login is clicked it popup the message for login success or fail. We learn in the finish and System.exit() for to exit the app.

[Tutorial-5](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR5_17IT009.rar)
  [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/PR5.1.JPG)

## Tutorial 6

Create an application which turns ON or OFF Torch/Flashlight of Camera.

Learning Outcome: In above application we can create a functionality of  to access the rear camera mobile flash light in which we put one ON/OFF button for to On and Off the flashlight when there is flashlight is on it will provide one another functionality by delay button when button is click the flashlight is start blinking. By this we can learn how to use mobile hardware components by android and other things like Runnable, ToggleButton, Handler for to put delay.

[Tutorial-6](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR6_17IT009.rar)
  [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/PR6.1.JPG)


## Tutorial 7

Create an application that will change color of the screen, based on selected options from the menu.

Learning Outcome: In above application we can create a functionality of  to create menu and using that options go to the next page for that we create one option_menu.xml and add menu items in it and then in MainActivity.java we can create onCreateOptionMenu() for to create menu and onSelectOptionMenu() for to select option and according that it will perform the task.

[Tutorial-7](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR7_17IT009.rar)
  [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/PR7.1.JPG)

## Tutorial 8

Create an application with the help of fragment.

Learning Outcome: In above application we can create a functionality of fragments in which we can create two fragment one fragment contain buttons and second can affect according to button clicks for that we can use fragment tag and create different .xml and .java files for the fragments.

[Tutorial-8](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR8_17IT009.rar)
  [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/PR8.1.JPG)

## Tutorial 9

Create an application with the help of web view.

Learning Outcome: In above application we can create a functionality of Web view in which we can create WebView functionality of android for that we use <WebView> tag in activity_main.xml file and then import WebView class and create object of this class and give reference of WebView and pass url of website into loadUrl() function. This will fetch the website from internet and display it in application.

[Tutorial-9](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR9_17IT009.rar)
  [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/PR9.JPG)

## Tutorial 10

Create an application with the help of database.

Here, In this as a database we use google sheet for that we devloped one API. Which is devloped in google Script which code is:

```
var ss = SpreadsheetApp.openByUrl("Add your google database sheet URL");

var sheet = ss.getSheetByName('Enteries'); match 
function doPost(e){
var entry = e.parameter.action;

if(entry == 'addEntry'){
  return addEntry(e);

}
}

function doGet(e){

  var records={};
  var rows = sheet.getRange(2, 1, sheet.getLastRow() - 1,sheet.getLastColumn()).getValues();
      data = [];
  for (var r = 0, l = rows.length; r < l; r++) {

    var row     = rows[r],
        record  = {};
    record['entryName'] = row[1];
    record['phone']=row[2];

    data.push(record);
    
   }
  records.entry = data;
  var result=JSON.stringify(records);
  return ContentService.createTextOutput(result).setMimeType(ContentService.MimeType.JSON);

}

function addEntry(e){

var date = new Date();
var entry  =  "Entry "+sheet.getLastRow(); // Entry 1
var entryName = e.parameter.entryName;
var phone = e.parameter.phone;
sheet.appendRow([entry,entryName,phone,date]);
   return ContentService.createTextOutput("Success").setMimeType(ContentService.MimeType.TEXT);

}
```

Learning Outcome: In above application we can create a functionality with database in which we can enter some detail of person and add it to the database and we can also display that detail into the application fetching from database for the database we use the google sheet and for the backend part we can generate one API using google script.  
reference by: http://www.crazycodersclub.com/

[Tutorial-10](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR10_17IT009.rar)
  [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/pr10.1.JPG)

## Tutorial 11

Creating an application that provides Single Sign-on (SSO) with Chrome Custom Tabs via the AppAuth library, and optionally push managed configuration to provide a user login hint.

Learning Outcome: In above application we can create a functionality for to sign in into the app using the google sign in authentication for that we configure first google API and then that API is use into the app for to the google sign in here we sign in the app using google and then able to sign out from the app. No need to create the new account for the app and then sign in threw that. 
reference by: https://www.youtube.com/watch?v=lQChsNFeAMc

[Tutorial-11](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR11_17IT009.rar)
  [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/PR11.3.jpg)


## Tutorial 12

Create an application to handle support voice interaction.

Learning Outcome: In above application we can create a functionality for to sign in into the app using the google sign in authentication for that we configure first google API and then that API is use into the app for to the google sign in here we sign in the app using google and then able to sign out from the app. No need to create the new account for the app and then sign in threw that.       
reference by: https://www.youtube.com/watch?v=0bLwXw5aFOs

[Tutorial-12](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR12_17IT009.rar)
  [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/PR12.1.jpg)

## Tutorial 13

Create an application to play video using YouTube API in PIP mode.

Learning Outcome: In above application we can create a functionality in which we are playing a video in our app and we are also set PIP mode for the our application which is very much useful when user need to work with more then one app at a same time. But in this app we set only one static video for play and it will automatic start when the app is start. Here in app, we also provide the media control access for the video.

[Tutorial-13](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR13_17IT009)
  [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/PR13.1.jpg)

## Tutorial 14

Create an application that uses end-to-end process of training a machine learning model that can recognize handwritten digit images with TensorFlow and deploy it to an Android app.

Learning Outcome: In above application we can create a functionality in which we need to write the number between 1-9 and our application give you that how much accurately he try understand that whatever you write is which number. For that we develop one ML-model in TensorFlow Lite which can understand human hand writing and deploy it in one application. For that we learn that how train the ML-model in TensorFlow Lite and how to deploy it in android application.

[Tutorial-14](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/Practicals/WCMC_PR14_17IT009.rar)
  [App_look](https://github.com/Mandip17IT009/WCMC_17IT009/blob/master/output/PR14.1.jpg)
