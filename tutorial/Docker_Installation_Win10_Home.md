# Docker Installation on Windows 10 Home
Written by Tanner Stern<br>
GitHub: [tannerstern](https://github.com/tannerstern/)<br>
Last updated: 04/07/2020

Sources: [hessi9's post](https://forums.docker.com/t/installing-docker-on-windows-10-home/11722/25) and [mapk's post](https://forums.docker.com/t/installing-docker-on-windows-10-home/11722/29) on the [Installing Docker on Windows 10 Home disucssion](https://forums.docker.com/t/installing-docker-on-windows-10-home/11722/)

# Pre-Installation Notes
* Follow these instructions **in order** because the order matters
* Pay attention to **details**; this is not a hard tutorial to follow, but it is complicated
* If you run into problems, do not despair! Contact the professor and patiently troubleshoot

# Step 1: Install Hyper-V and Container
1. Save and close any open documents or projects
   * Your computer will restart multiple times throughout this installation
1. Download [hyperv.bat](hyperv.bat) and [containers.bat](containers.bat)
   * Put them in an easyily accessible file
   * These files are Windows Batch files. They will install Windows Components necessary to make Docker run.
   * If you get a warning from **Windows Smartscreen**, click "More info" and then "Run anyway." This is your computer recognizing these files as downloaded from the internet and being cautious about running them.
1. Right-click on the **hyperv.bat** and select "Run as administrator"
   * The command prompt will open
   * You will see several progress bars flash in the window
   * This installation will take a few minutes
1. When prompted, type **y** to restart your computer
   * This prompt will appear in the command prompt after the batch file runs
1. When the restart is completed, do the same for **container.bat**
   * Remember to right-click and "Run as administrator"
   * When prompted, type **y** to restart your computer

# Step 2: Make Registry Changes
1. Note: Be **very careful** in this next section
   * Editing the Windows registry is like performing open-heart surgery
   * Follow these directions exactly and make **only** those changes described here
   * **Do not** restart your computer until this tutorial is over (as a precaution)
1. Open the Windows registry editor tool
   * This can be done by clicking the Start button and typing "regedit" or searching for "Registry Editor"
1. Navigate to **\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion**
   * Use the folder tree on the left side of the window
   * When you get to **CurrentVersion**, make sure you have clicked on (selected) the CurrentVersion **folder** and not one of its subfolders
1. Find the **EditionID** key
   * After you have selected **CurrentVersion**, you will see keys and values on the right side of the window
   * The keys are arranged alphabetically by default
1. Right-click and "Modify..." the EditionID; change it from "Core" to "Professional"
   * The initial value of the key should be "Core"
   * We want to change this value to "Professional" (case-sensitive)
   * We will undo this change after we install Docker
1. Click "OK" but leave the Registry Editor window open

# Step 3: Install Docker
1. If you haven't already, download the Docker [installer](https://www.docker.com/products/docker-desktop)
1. Run the installer as you would any other installer
   * The default settings are fine
   * If you encounter any errors that reference "Hyper-V" or "Containers" as missing, you might have missed something in Step 1. Go back and check.
   * If you encounter any errors that reference how you need Windows Pro, you might have missed something in Step 2. Go back and check.
1. The installer will notify you when it has installed successfully
   * You are almost done!
1. Go back to the Registry Editor and **change EditionID back to "Core"**
   * This is a very important step, do not skip it!
   * Make sure you click "OK" and close the Registry Editor when you are done

# Final Notes
* Docker can take a long time to start up, so if it seems like it is not opening, be patient
* Docker may be running after the installation
* You can tell if Docker is running by looking at your system tray
   * This is the area of your taskbar by the clock (bottom-right)
   * Docker might be hidden; click the arrow to expand the tray to see all icons