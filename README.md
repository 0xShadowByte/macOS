# Virtualizing macOS: A Hands-On Lab for System Administration and Troubleshooting

# Objective

The objective of running macOS in a virtual machine within my home lab is to gain hands-on experience with macOS system administration, software testing, and troubleshooting in a controlled environment. By setting up macOS on VMware Workstation Pro, I aim to explore macOS configurations, Terminal commands, and security features, which will enhance my familiarity with the operating system. This setup also allows me to experiment with enterprise tools such as MDM (Jamf), Active Directory integration, and macOS security hardening without the need for dedicated Apple hardware. Additionally, it serves as a learning platform for resolving boot errors, disk management issues, and optimizing virtualization settings for macOS compatibility.

# Skills Learned

- Disk Utility in macOS may require formatting the virtual drive as APFS before installation.
- Recovery Mode access allows troubleshooting issues like disk erasure failures and network problems.
- OneDrive syncing can interfere with VM file locations, requiring manual adjustments.
- Understanding macOS bootloader behavior is essential to resolving “No compatible bootloader found” errors.
- Running macOS on a VM provides a safe space to practice software deployment, security settings, and automation.
- Networking configurations (NAT vs. Bridged mode) impact internet connectivity within the macOS VM.

# Tools

- VMware Workstation Pro 17
- macOS Ventura

# Content

- Installing and running macOS Ventura on VMware Workstation Pro 17
- Explore and getting comfortable with the interface
- Personalize macOS
- Explore Finder, Safari, and Calender
- Using Multitasking Features
- File Management with Time Machine

# Steps

## Part I. Installing and running macOS Ventura on VMware Workstation Pro 17

Step 1: Download and install VMware Workstation Player. You'll also want to install Auto-Unlocker v2.0.1 from GitHub (https://github.com/paolo-projects/auto-unlocker/releases/tag/v2.0.1) so that your PC VM can run macOS. Download macOS Ventura ISO 

![image](https://github.com/user-attachments/assets/1dcc2c30-7785-4f1f-b216-f839e9b2b20a)

![image](https://github.com/user-attachments/assets/0429cd8a-2bda-45b8-9d97-b0580d8b2e52)

Step 2: Create a New Virtual Machine

Open VMware and choose Create a New Virtual Machine. Select Installer disc image file (iso) and browse to the macOS image file, in our case its macOS Ventura ISO. Select as the operating system and choose the correct version (macOS 10.x or higher). Follow the prompts to allocate disk space, memory, and CPU resources (at least 4GB of RAM and 40GB of hard disk space). Once the ISO is finished downloading, upload the ISO image file onto VMware Workstation Pro 17 so it can run.

![image](https://github.com/user-attachments/assets/31ff9dec-33fa-4d89-b809-99db7447e1d9)

![image](https://github.com/user-attachments/assets/dc9c8a99-7850-43a0-8917-fa31c49cc868)

![image](https://github.com/user-attachments/assets/a7c54330-54fc-4d03-9bb4-7bac7676b020)

Step 3: Once we're in disk utility, click on VMware SATA Hard Drive Media. Then click on erase. 

![image](https://github.com/user-attachments/assets/9087ea2b-f352-457a-bd26-3cc614bbd357)

![image](https://github.com/user-attachments/assets/c16cca9d-eaf2-41de-a54b-38ff24bcc7b6)

![image](https://github.com/user-attachments/assets/8499db94-b437-4fb6-9e0a-7213c78e6f21)

Step 4: Once the drive is deleted, quit out oof Disk Utility and update/install macOS 13 beta. Select the drive we want, and in this case it would be VenturaVM

![image](https://github.com/user-attachments/assets/ae18a6a8-b7ab-4523-a0ec-7cdd1667ba69)

![image](https://github.com/user-attachments/assets/5da0e0fe-e64d-4240-8257-cfa5cd5610ea)

![image](https://github.com/user-attachments/assets/f6564988-1c27-4426-874e-e0bd856bfc45)

Step 5: Finishing up the setup by creating a computer account. Skipped the appleID set up.

![image](https://github.com/user-attachments/assets/73bbabe1-ee48-49b6-bb29-18aa4b11806d)

![image](https://github.com/user-attachments/assets/a9d8d78d-ce16-4c0f-9206-22ca5f4543a8)

## Part II: Explore and Get Comfortable with the Interface

Task 1: Explore the Desktop and Dock. Familiarize yourself with the Desktop, Dock, and Menu Bar.
Desktop: Click anywhere on the Desktop to make sure you're in the right place. You should see icons like "Trash" and possibly some files or folders. Dock: The Dock is the bar at the bottom of your screen. Hover over icons like Safari, Finder, Mail, and Calendar. Click to open them. Menu Bar: At the top of the screen, the Menu Bar shows various menus depending on the app you're using. Explore options like Apple Menu (), File, and Edit.

![image](https://github.com/user-attachments/assets/ef1510e7-804f-43e3-aad1-7f42f57ba2d3)

Task 2: Use Spotlight Search. Learn how to use Spotlight Search for quick access to apps, documents, and system settings.
Press Command + Space to open Spotlight (Space + Win for PC). Try searching for common apps like Safari, Finder, or System Preferences. Type the name of a file or folder, and see how Spotlight shows results.

![image](https://github.com/user-attachments/assets/3f899534-7077-4ed5-b25a-bc0be2dbfe68)

## Part III: Use Finder to Organize Files and Folders

Task 1: Open Finder and Navigate
Learn how to use Finder to browse files and folders. Click on the Finder icon in the Dock (smiley face icon).
Navigate to Your Home Folder: In Finder, look at the Sidebar on the left. Click on Home to see folders like Documents, Downloads, and Desktop. Open a Folder: Double-click a folder to open it and see its contents.

Task 2: Create, Rename, and Organize Files
Practice creating and organizing files/folders. Create a Folder: In Finder, navigate to the Desktop. Right-click and choose New Folder. Name the folder "Practice". Create a File: Open TextEdit from the Dock, type some text (e.g., "This is my first file"), and save it to the "Practice" folder on the Desktop. Rename a File: In Finder, click once on your file to select it, then press Return and type a new name (e.g., "My First File"). Move Files: Drag your file from the Desktop into the "Practice" folder to organize it.

Task 3: Use the Sidebar to Quickly Access Folders. Practice navigating the Finder Sidebar for quick access to common folders. In Finder, you'll notice the Sidebar on the left, which includes quick links to Documents, Downloads, and Applications. Click on Documents to open it and see your files. Drag a file from the Desktop into the Documents folder to move it.

3. Customizing Settings: Personalize macOS
Task 1: Change System Preferences
Goal: Explore System Preferences to customize macOS.
Steps:
Open System Preferences: Click on the Apple Menu () in the top-left corner of the screen and select System Preferences.
Change Desktop Background: In System Preferences, click Desktop & Screen Saver. Choose a different desktop wallpaper or select a photo from your collection.
Adjust Trackpad Settings: Go back to System Preferences and click on Trackpad. Try adjusting the settings for scrolling, tapping, and gestures.
Task 2: Customize the Dock and Menu Bar
Goal: Personalize the Dock and Menu Bar for easier navigation.
Steps:
Change Dock Settings: In System Preferences, go to Dock & Menu Bar. Experiment with settings like:
Size: Adjust the size of the Dock.
Position on Screen: Choose whether the Dock appears on the left, bottom, or right of the screen.
Add/Remove Apps from Dock: Drag apps to and from the Dock. You can right-click an app and select Options to Keep in Dock or remove it.

4. Using Apps: Explore Finder, Safari, and Calendar
Task 1: Using Finder to Search for Files
Goal: Search and filter files using Finder.
Steps:
Open Finder and use the search bar in the top-right corner to search for a specific file. Try searching for the file you created earlier ("My First File").
Use the Filter options to refine your search by file type or date.
Task 2: Explore Safari
Goal: Learn how to browse the web using Safari.
Steps:
Open Safari from the Dock.
Type a website URL (e.g., www.apple.com) into the address bar and press Return to navigate.
Use Tabs: Click the + button in Safari to open a new tab, and try browsing multiple websites simultaneously.
Use Bookmarks: Click Bookmarks in the menu bar to save your favorite websites.
Practice using the Reader Mode by clicking the icon in the address bar when available.
Task 3: Using Calendar to Schedule Events
Goal: Learn how to use the Calendar app to schedule and manage events.
Steps:
Open the Calendar app from the Dock.
Click on a day to add an event. For example, click on a random day and choose New Event.
Enter an event title, such as "Learn macOS Basics," and set a time.
Set a reminder for the event, and click Add.
Explore the Week, Month, and Day views to see your schedule in different layouts.

5. Using Multitasking Features
Task 1: Split View for Multitasking
Goal: Use Split View to work in two apps side by side.
Steps:
Open two apps, like Safari and Finder.
Click and hold the green maximize button in the top-left corner of one app's window.
Drag the window to one side of the screen, then release.
Select the second app to fill the other side of the screen.
Practice resizing the Split View windows.
Task 2: Use Mission Control to Manage Windows
Goal: Get comfortable with Mission Control to manage multiple windows.
Steps:
Swipe up with three fingers on your trackpad (or press the F3 key) to enter Mission Control.
Drag windows to different desktops or organize them for multitasking.
Click on a desktop to switch between them.

6. Bonus Task: File Management with Time Machine
Goal: Set up and practice using Time Machine for backups.
Steps:
Open System Preferences and click Time Machine.
Connect an external drive or use an available network drive for backups.
Toggle Time Machine on and choose the backup disk.
Wait for Time Machine to start backing up automatically.
After a backup, try restoring a file by clicking Enter Time Machine from the Time Machine menu in the menu bar.

