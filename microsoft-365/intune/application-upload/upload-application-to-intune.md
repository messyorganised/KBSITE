# Upload application to Intune

![](<../../../.gitbook/assets/0 (5).png>)

To add application. Go to Apps (1) > All apps (2) > Add (3).

![](<../../../.gitbook/assets/1 (5).png>)

Select the drop down (1) > Select your application type (2)

![](<../../../.gitbook/assets/2 (5).png>)

Once selected, press Select (1)

![](<../../../.gitbook/assets/3 (5).png>)

A new window will appear. Select app package file (1) > Find and select your .intunewin file.

![](<../../../.gitbook/assets/4 (3).png>)

Fill in all required \* Input.

Some details will be autopopulated. Feel free to make the changes to your liking.

Press Next (1) when you are finished

![](<../../../.gitbook/assets/5 (3).png>)

As per previous, ensure any auto populated details are correct. Press next (1) when you are ready to proceed.

![](<../../../.gitbook/assets/6 (3).png>)

This page specify the requirements that the hardware must meet before the app is installed.

I have set the operating system architecture to 64-bit only (1) and minimum operating system to Win10 1607 (2) to targe all 64bit devices. You can modify this to your needs.

Once completed. Press Next (3)

![](<../../../.gitbook/assets/7 (2).png>)

Configure your rule format. This is a requirement even if youre not using it.

Click add (1) > Select the file type for the rule to be triggered (2) > enter your file GUID (3) (the one we extracted in previous KB) > Set version check to No (4) > Press OK when you are done. (5)

Your new rule should be populated in the Type tab. Once it is, Pres Next (6)

![](<../../../.gitbook/assets/8 (2).png>)

Due to the nature of our setup. We will skip Dependencies and Superseded tab. Feel free to read them in your spare time.

Assignments

For this tutorial, we want to set up the program across all devices. So we will press 'Add all devices (1) > Next (2)

![](<../../../.gitbook/assets/9 (1).png>)

Review your configuration and Press Create (1) when you are done!

![](../../../.gitbook/assets/10.png)
