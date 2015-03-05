# HQMobileOffers-iOS
The *HotelQuickly* Cordova wrapper for third party integration of mobile/webview based hotel offers

##Integration into an existing iOS project

1) Download the project and add `HQMobileOffers-Bundle` to your existing project directory
![alt tag](https://github.com/HotelQuickly/HQMobileOffers-iOS/blob/TutorialImages/HelpImages/Screen%20Shot%202015-03-04%20at%2018.42.17.png)


2) Inside the `HQMobileOffers-Bundle`directory, look for `HQOffersViewController.h`,`HQOffersViewController.m` and `config.xml`. Drag and drop these files into your Xcode project window
![alt tag](https://github.com/HotelQuickly/HQMobileOffers-iOS/blob/TutorialImages/HelpImages/Screen%20Shot%202015-03-04%20at%2019.09.28.png)
![alt tag](https://github.com/HotelQuickly/HQMobileOffers-iOS/blob/TutorialImages/HelpImages/Screen%20Shot%202015-03-04%20at%2018.42.49.png)

**NOTE!!** When promted by X-code to '**Choose options for adding these files**' select the following:
![alt tag] (https://github.com/HotelQuickly/HQMobileOffers-iOS/blob/TutorialImages/HelpImages/Screen%20Shot%202015-03-04%20at%2018.42.38.png)



3) The last file you need to add to your Xcode project window is `CordovaLib.xcodeproj`. This is found in the sub-directory `HQMobileOffers-Bundle/CordovaLib`
![alt tag](https://github.com/HotelQuickly/HQMobileOffers-iOS/blob/TutorialImages/HelpImages/Screen%20Shot%202015-03-04%20at%2018.43.09.png)


4) You will need to add the `CordovaLib` as a **'Target Dependency'**. Select your project, then select your application in **'TARGETS'**, then **'Build Phases'**. Press the '+' button and choose the `CordovaLib` static library. Select **'Add'** to finish this step.
![alt tag](https://github.com/HotelQuickly/HQMobileOffers-iOS/blob/TutorialImages/HelpImages/Screen%20Shot%202015-03-04%20at%2018.43.48.png)


5) Whilst still in the '**Build Phases**' section , press the '+' button in the '**Link Binary With Libraries**' section and choose `libCordova.a` from the dropdown list. Press '**Add**' to include it.

**NOTE!!** In order for the integration to compile, there are 3 other frameworks required. Most exiting application should already have these included, they are `MobileCoreServices.framework`, `CoreGraphics.framework` and `AssetsLibrary.framework`. If you don't already have them in your project, make sure to add them now.
![alt tag](https://github.com/HotelQuickly/HQMobileOffers-iOS/blob/TutorialImages/HelpImages/Screen%20Shot%202015-03-04%20at%2018.45.04.png)


6) The `HQOffersViewController` has everything you need and requires zero setting up in order to work as a dedicated view controller for displaying the *Hotel Quickly* offers webview. All you need to do is create a new view controller in your `xyz.storyboard` and change the class type to `HQOffersViewController`. No connections/outlets are required to be connected from the storyboard scene (the new view controller you just added). You're good to go. 
![alt tag](https://github.com/HotelQuickly/HQMobileOffers-iOS/blob/TutorialImages/HelpImages/Screen%20Shot%202015-03-04%20at%2018.45.29.png)


7) The final step. '**cmd+R**', navigate to the location you have added the `HQOffersViewController` in your application and you should see the *Hotel Quickly* offers webview load up.

