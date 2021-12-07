[Back](../readme.md)
# Setting up your programming environment on your personal laptop

The instructions may differ based on if you are using Windows, MacOS, or Linux.

Unfortunately this software is unavailable on ChromeOS without some workarounds.

If you do have a ChromeBook and can not bring in a Windows, MacOS, or Linux laptop please speak to one of the code team leads.


***
⚠️ **Please ask a code team lead if any of these instructions do not make sense or if you encounter issues.** ⚠️
***


## Software Installation Guide

1. <b>Install GitHub Desktop</b>

    The installer is on this [site](
https://desktop.github.com), follow the prompts and log into your GitHub account when asked.  



2. <b>Install IntelliJ IDEA Community Edition </b>

    This is the software where you will be writing the robot code. You can download it [here](
https://www.jetbrains.com/idea/download/), please get the community edition as it is free (we are not using any features that are only in Ultimate). 



3. <b>Prepare IntelliJ IDEA for Android Development</b>
    1. Click `Create New Project`
    2. Install the Java JDK:
        At the top of the window you should see a drop down for `Project SDK`, click it, then click `Download JDK...` select version 11 and set the vendor to `Eclipse Temurin (AdoptOpenJDK HotSpot)` then click download. 
    3. Install Android SDK:
        On the side bar, click Android, then when it mentions that you do not have the Android SDK, follow it's prompts to install it. 



4. <b> Join the ScarlettRobotics GitHub Organization </b>

    First check if you are in the ScarlettRobotics organization on GitHub, by going to this [site](https://github.com/settings/organizations), and logging into your GitHub account. If you see ScarlettRobotics, proceed to the next step. 

    If not: contact a code team lead to add you to the organization. 


5. <b>Clone the FTC-2021 repository</b>

    In GitHub Desktop, after you have signed in, click current repository, then add, then clone, and find FTC-2021 in the list, hit clone. After, hit fetch orgin at the top of the window. 



6. <b>Open the repository in IntelliJ IDEA</b>

    On the main page of GitHub Desktop, there is an option to `Open the repository in your external editor`, if it says `Open in JetBrains IntelliJ Idea`, please click that button. If it does not show up, try closing and reopening GitHub desktop.

    If it still does not show `Open in JetBrains IntelliJ Idea`: Open IntelliJ IDEA, go to `File` in the top menu bar, then `Open...`, go to your Documents folder (in your user folder), then `GitHub`, then `FTC-2021`. 

    <b>When it opens, hit trust this project.</b>



7. <b>Build the project in IntelliJ IDEA</b>

    Hit the green hammer in the top right of the IntelliJ IDEA window, and let it run. <b>This will take a while.</b> Open the build tab on the bottom of the window to see it progress.



8. <b>Download Android SDK 29</b>

    The build will leave a few error messages, <b>this is normal</b>. In the build tab, click on the error that says `Failed to install the following Android SDK packages...` at the bottom of the build tab. Hit `Install missing SDK package(s)`, and follow the prompts. 
    
    Build the program again with the green hammer. 



9. <b>Fix SDK location not found error (if it occurs)</b>
    
    <b> If you experience this error (not everyone will): </b>

    Create a new file called `local.properties` in the root of the project folder and add the following infromation depending on your OS:

    Windows: `sdk.dir=C:\\Users\\UserName\\AppData\\Local\\Android\\sdk` with `UserName` replaced with your Windows Username

    MacOS: `sdk.dir = /Users/USERNAME/Library/Android/sdk` with `UserName` replaced with your MacOS Username

    Linux: `sdk.dir = /home/USERNAME/Android/Sdk` with `UserName` replaced with your Linux username

## You are all done!! Happy Coding!

        
