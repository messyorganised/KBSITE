# Upload application to Intune

## Intro

This KB will provide you a step by step guide on how to upload your application to intune.

![](<../../../.gitbook/assets/0 (5).png>)



***

## Prerequisite

In this KB specifically, we will be using our previously created .intunewin wrapper.

Article for that will be in the link below

{% embed url="https://app.gitbook.com/o/2mIS1DZ5tiCeMulycQRc/s/Nd1kg8pQ1SIiRF58IH9i/~/changes/49/microsoft-365/intune/application-upload/prepping-the-intune-file" fullWidth="false" %}

Access to site's Intune.



***

## Step-by-Step Guide

### 1. Adding the file to Intune.

To add application. Go to Apps (1) > All apps (2) > Add (3).

![](<../../../.gitbook/assets/1 (5).png>)

Select the drop down (1) > Select your application type (2)

![](<../../../.gitbook/assets/2 (5).png>)

Once selected, press Select (1)

![](<../../../.gitbook/assets/3 (5).png>)

A new window will appear. Select app package file (1) > Find and select your .intunewin file. (2)

![](<../../../.gitbook/assets/4 (3).png>)

Fill in all required \* Input.

Some details will be auto populated. Feel free to make the changes to your liking.

Press Next (1) when you are finished

![](<../../../.gitbook/assets/5 (3).png>)

As per previous, ensure any auto populated details are correct. Press next (1) when you are ready to proceed.

![](<../../../.gitbook/assets/6 (3).png>)



### 2. Configure the requirement for application to be eligible for install

This page specify the requirements that the hardware must meet before the app is installed.

I have set the operating system architecture to 64-bit only (1) and minimum operating system to Win10 1607 (2) to targe all 64bit devices. You can modify this to your needs.

Once completed. Press Next (3)

![](<../../../.gitbook/assets/7 (2).png>)



### 3. Configure your rule item.

Click add (1) > Select the file type for the rule to be triggered (2) > enter your file GUID (3) (the one we extracted in previous KB) > Set version check to No (4) > Press OK when you are done. (5)

Your new rule should be populated in the Type tab. Once it is, Pres Next (6)

![](<../../../.gitbook/assets/8 (2).png>)

### Note

Due to the nature of our setup. We will skip Dependencies and Superseded tab. Feel free to read them in your spare time.



### 4. Assign your application assignments

This is where you set assignments on what user, hardware or groups the application is applied for.

For this tutorial, we want to set up the program across all devices. So we will press 'Add all devices (1) > Next (2)

![](<../../../.gitbook/assets/9 (1).png>)

Review your configuration and Press Create (1) when you are done!

![](../../../.gitbook/assets/10.png)

***

## Outro

Once you have applied the configuration. The application will install on its assigned groups, users, hardware on the next automatic cycle.&#x20;
