+++
title="Fixing Windows 11"
description="fixing windows 11 by trimming the iso"
date=2024-04-11

[taxonomies]
tags = ["windows"]
categories = ["tech"]
+++

#### Bloat in windows

Following is the list of bloat windows ships with, which can be removed

- Clipchamp
- News
- Weather
- Xbox (although Xbox Identity provider is still here, so it should be possible to be reinstalled with no issues)
- GetHelp
- GetStarted
- Office Hub
- Solitaire
- PeopleApp
- PowerAutomate
- ToDo
- Alarms
- Mail and Calendar
- Feedback Hub
- Maps
- Sound Recorder
- Your Phone
- Media Player
- QuickAssist
- Internet Explorer
- Tablet PC Math
- Edge
- OneDrive

Lets remove these things by using a tool called `tiny11builder`.

It is a script for creating a bloat-free Windows 11 iso. Utilizing only Microsoft’s DISM utility and `oscdimg.exe` from the Windows ADK for bootable ISO creation. Features an unattended answer file for OOBE Microsoft Account bypass and /compact flag deployment. This script is open-source and can be found at [github/ntdevlabs/tiny11builder](https://github.com/ntdevlabs/tiny11builder)

#### Steps

- We need to make sure to set the execution policy to be `Unrestricted` in PowerShell. To do that use the following command in PowerShell.

    ```ps
    # run this as administrator
    PS C:\Users\Sakshat> Set-ExecutionPolicy unrestricted
    ```

- Then download Windows 11 from the [Microsoft website](https://www.microsoft.com/software-download/windows11)

- Mount the downloaded ISO image using Windows Explorer.
- Select the drive letter where the image is mounted (only the letter, no colon (:))
- Select the SKU that you want the image to be based.
- When the image is completed, you will see it in the folder where the script was extracted, with the name `tiny11.iso`
- Connect your USB Flash drive. Please note that you will be erasing all the data on it.
- Download and launch [Rufus](https://rufus.ie/en/).
- Select your USB drive if it's not already selected by default.
- Click Select and choose the `tiny11.iso` file from your storage drive. 
- Click Start at the bottom of the window. 
- Create a second partition and format it as NTFS. It should take all the remaining disk space.
- Check remove requirement for TPM, data collection if you want. These are optional.
- Click Ok if warned that the process will destroy all data on your USB Flash drive. 
- Rufus will now take a few minutes to drive to your drive. When it is done, you will have a USB Flash drive that can boot to install windows.