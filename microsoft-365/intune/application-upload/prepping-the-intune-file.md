# Prepping the Intune file

![](<../../../.gitbook/assets/0 (6).png>)

Go to Source

![](<../../../.gitbook/assets/1 (6).png>)

This is where all files will be stored. Doing so will make the process more easy.

![](<../../../.gitbook/assets/2 (6).png>)

We would first want to grab the version GUID. This is so that if a new version of the same program is released, we can run a single line powershell code to uninstall the old version without affecting the new version.

By using the following code, it will run the installer as per usual but it will also create a log file which we will need to locate the application's GUID:

msiexec /I \<filename+type> /L\*V \<logfilename>.txt

![](<../../../.gitbook/assets/3 (6).png>)

Running it will create a log file (1). Open it with a notepad.

![](<../../../.gitbook/assets/4 (4).png>)

For this application, the guid is under ProductCode. All GUID should look something like below:\
{1afa7b53-c06a-44ba-b9a1-ff7766d6507f}

![](<../../../.gitbook/assets/5 (4).png>)

Run CMD in the file directory. if you want to have a read of the commands for the IntuneWinAppUtil, enter the following code:

IntuneWinAppUtil -h

You can simply type the following code for assisted intune wrapper\
IntuneWinAppUtil

If you know what youre doing, use the following code and fill in the <> spaces:

IntuneWinAppUtil.exe -c \<source folder path> -s \<source setup file> -o \<output folder for wrapper to export>

![](<../../../.gitbook/assets/6 (4).png>)

Once completed. You should see the .intunewin file on the destination of your choosing. This will be used on the intune aspect of things.

![](<../../../.gitbook/assets/7 (3).png>)
