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
- Set up MDM via Jamf for a macOS device

# Tools

- VMware Workstation Pro 17
- macOS Ventura
- Jamf Pro (Demo)
- ARD (Apple Remote Desktop)

# Content

- Installing and running macOS Ventura on VMware Workstation Pro 17
- Explore and getting comfortable with the interface
- Personalize macOS
- Explore Finder, Safari, and Calender
- Using Multitasking Features
- File Management with Time Machine
- Install and Configure Apple Remote Desktop

## Part I. Installing and running macOS Ventura on VMware Workstation Pro

### Task 1: Download and install VMware Workstation Player

You'll also want to install Auto-Unlocker v2.0.1 from GitHub (https://github.com/paolo-projects/auto-unlocker/releases/tag/v2.0.1) so that your PC VM can run macOS. Download macOS Ventura ISO 

![image](https://github.com/user-attachments/assets/1dcc2c30-7785-4f1f-b216-f839e9b2b20a)

![image](https://github.com/user-attachments/assets/0429cd8a-2bda-45b8-9d97-b0580d8b2e52)

### Task 2: Create a New Virtual Machine

Open VMware and choose Create a New Virtual Machine. Select Installer disc image file (iso) and browse to the macOS image file, in our case its macOS Ventura ISO. Select as the operating system and choose the correct version (macOS 10.x or higher). Follow the prompts to allocate disk space, memory, and CPU resources (at least 4GB of RAM and 40GB of hard disk space). Once the ISO is finished downloading, upload the ISO image file onto VMware Workstation Pro 17 so it can run.

![image](https://github.com/user-attachments/assets/31ff9dec-33fa-4d89-b809-99db7447e1d9)

![image](https://github.com/user-attachments/assets/dc9c8a99-7850-43a0-8917-fa31c49cc868)

![image](https://github.com/user-attachments/assets/a7c54330-54fc-4d03-9bb4-7bac7676b020)

### Task 3: Once we're in disk utility, click on VMware SATA Hard Drive Media. Then click on erase. 

![image](https://github.com/user-attachments/assets/9087ea2b-f352-457a-bd26-3cc614bbd357)

![image](https://github.com/user-attachments/assets/c16cca9d-eaf2-41de-a54b-38ff24bcc7b6)

![image](https://github.com/user-attachments/assets/8499db94-b437-4fb6-9e0a-7213c78e6f21)

### Task 4: Once the drive is deleted, quit out oof Disk Utility and update/install macOS 13 beta. Select the drive we want, and in this case it would be VenturaVM

![image](https://github.com/user-attachments/assets/ae18a6a8-b7ab-4523-a0ec-7cdd1667ba69)

![image](https://github.com/user-attachments/assets/5da0e0fe-e64d-4240-8257-cfa5cd5610ea)

![image](https://github.com/user-attachments/assets/f6564988-1c27-4426-874e-e0bd856bfc45)

### Task 5: Finishing up the setup by creating a computer account. Skipped the appleID set up.

![image](https://github.com/user-attachments/assets/73bbabe1-ee48-49b6-bb29-18aa4b11806d)

![image](https://github.com/user-attachments/assets/a9d8d78d-ce16-4c0f-9206-22ca5f4543a8)

## Part II. Explore and Get Comfortable with the Interface

### Task 1: Explore the Desktop and Dock. 

Familiarize yourself with the Desktop, Dock, and Menu Bar. Desktop: Click anywhere on the Desktop to make sure you're in the right place. You should see icons like "Trash" and possibly some files or folders. Dock: The Dock is the bar at the bottom of your screen. Hover over icons like Safari, Finder, Mail, and Calendar. Click to open them. Menu Bar: At the top of the screen, the Menu Bar shows various menus depending on the app you're using. Explore options like Apple Menu (), File, and Edit.

![image](https://github.com/user-attachments/assets/ef1510e7-804f-43e3-aad1-7f42f57ba2d3)

### Task 2: Use Spotlight Search. 

Learn how to use Spotlight Search for quick access to apps, documents, and system settings.
Press Command + Space to open Spotlight (Space + Win for PC). Try searching for common apps like Safari, Finder, or System Preferences. Type the name of a file or folder, and see how Spotlight shows results.

![image](https://github.com/user-attachments/assets/3f899534-7077-4ed5-b25a-bc0be2dbfe68)

## Part III. Use Finder to Organize Files and Folders

### Task 1: Open Finder and Navigate

Learn how to use Finder to browse files and folders. Click on the Finder icon in the Dock (smiley face icon).
Navigate to Your Home Folder. In Finder, look at the Sidebar on the left. Click on Home to see folders like Documents, Downloads, and Desktop. Open a Folder: Double-click a folder to open it and see its contents.

![image](https://github.com/user-attachments/assets/cd9b3784-8216-48aa-8cd2-8b3e6235de9f)

![image](https://github.com/user-attachments/assets/8d664e7b-a4b7-4e05-a92b-25b66468f211)

### Task 2: Create, Rename, and Organize Files

Practice creating and organizing files/folders. Create a Folder: In Finder, navigate to the Desktop. Right-click and choose New Folder. Name the folder "Practice". Create a File: Open TextEdit from the Dock, type some text (e.g., "This is my first file"), and save it to the "Practice" folder on the Desktop. Rename a File: In Finder, click once on your file to select it, then press Return and type a new name (e.g., "My First File"). Move Files: Drag your file from the Desktop into the "Practice" folder to organize it.

![image](https://github.com/user-attachments/assets/5b9f7bbd-5e9a-4a1d-b3b4-71eccce80cd4)

### Task 3: Use the Sidebar to Quickly Access Folders. 

Practice navigating the Finder Sidebar for quick access to common folders. In Finder, you'll notice the Sidebar on the left, which includes quick links to Documents, Downloads, and Applications. Click on Documents to open it and see your files. Drag a file from the Desktop into the Documents folder to move it. Once you drag the file from Desktop and into Documents folder, it will disappear from desktop and reappear in documents folder automatically. 

![image](https://github.com/user-attachments/assets/5f2012e9-c3c9-4413-b719-7ab536394fc5)

![image](https://github.com/user-attachments/assets/9701a00c-71e8-44a4-9cea-8a40d2e21d07)

## Part IV. Customizing Settings: Personalize macOS

### Task 1: Change System Preferences

Explore system settings to customize macOS. Open system settings, click on the Apple Menu (the apple logo) in the top-left corner of the screen and select system settings. To change the desktop background, click on Desktop & Screen Saver in the systems preferences widnow. Choose a different desktop wallpaper or select a photo from your collection.

If you're on a macbook you can adjust the trackpad settings by going to click on trackpad towards the bottom of the left hand pane in system preferences. Go ahead and try adjusting the settings for scrolling, tapping, and gestures to get some practice.

![image](https://github.com/user-attachments/assets/654c1213-9342-4415-8acb-d5f8ec3bd266)

![image](https://github.com/user-attachments/assets/d9baccfc-327f-4ddb-861b-0fcdb0f88ae8)

![image](https://github.com/user-attachments/assets/d74c983a-1863-4920-9462-5f8bfd858e84)

### Task 2: Customize the Dock and Menu Bar

Personalize the Dock and Menu Bar for easier navigation. Change Dock Settings from In system settings, go to Dock & Menu Bar. Experiment with settings: size (adjust the size of the dock), position on screen (choose whether the dock appears on the left, bottom, or right of the screen), or add/remove apps from dock (drag apps to and from the dock). You can right-click an app and select options to keep in dock or remove it.

![image](https://github.com/user-attachments/assets/aec1ac7f-c286-4d3e-a298-382cd4750376)

![image](https://github.com/user-attachments/assets/8e8ea9e1-501b-4ead-8cc1-1df0eaea2ded)

## Part V. Using Apps: Explore Finder, Safari, and Calendar

### Task 1: Using Finder to Search for Files

Search and filter files using Finder. Open Finder and use the search bar in the top-right corner to search for a specific file. Try searching for the file you created earlier ("Practice Folder"). Use the Filter options to refine your search by file type or date.

![image](https://github.com/user-attachments/assets/cb7c11ec-5855-4412-a8a9-544af0717598)

### Task 2: Explore Safari

Learn how to browse the web using Safari. Open Safari from the Dock. Type a website URL (e.g., www.apple.com) into the address bar and press Return to navigate. Use tabs: click the + button in Safari to open a new tab, and try browsing multiple websites simultaneously. Use Bookmarks: click Bookmarks in the menu bar to save your favorite websites. Practice using the Reader Mode by clicking the icon in the address bar when available.

![image](https://github.com/user-attachments/assets/25582029-63cb-496e-a385-1aa4334ac558)

![image](https://github.com/user-attachments/assets/6971a720-d2e3-4d1c-915f-50fae6331f56)

### Task 3: Using Calendar to Schedule Events

Learn how to use the Calendar app to schedule and manage events. Open the Calendar app from the Dock. Click on a day to add an event. For example, hover over a random day, double click to create New Event. Enter an event title, such as "Learn macOS Basics," and set a time, set a reminder for the event, and click apply. Explore the Week, Month, and Day views to see your schedule in different layouts.

![image](https://github.com/user-attachments/assets/fd80a57e-0eed-4cff-a7b4-314733593894)

![image](https://github.com/user-attachments/assets/8d8f28f2-24b8-4f74-8ef6-eb500f4e6dbd)

## Part VI. Using Multitasking Features

### Task 1: Split View for Multitasking

Use Split View to work in two apps side by side. Open two apps, like Safari and Finder. Click and hold the green maximize button in the top-left corner of one app's window. Drag the window to one side of the screen, then release. Select the second app to fill the other side of the screen. Practice resizing the Split View windows. 

To exit Split View move your cursor to the top of the screen, this will bring up the window buttons. In either app, click the green maximize button again too exit Split View.

![image](https://github.com/user-attachments/assets/5b28fef4-55b6-49d2-8357-534c782aa0af)

![image](https://github.com/user-attachments/assets/0902a556-be0b-4bd9-a785-f0814df08a07)

### Task 2: Use Mission Control to Manage Windows

Get comfortable with Mission Control to manage multiple windows. Swipe up with three fingers on your trackpad (or press the F3 key) to enter Mission Control. (Tip: if F3 shortcut doesn't work then try Ctrl + Up Arrow shortcut). In Mission Control, you'll see all the open windows of your current desktop. To move a window to a different desktop, click and drag the window to the top of the screen where you'll see Desktop Spaces. Drop the window onto one of the Desktops at the top. If you don't hae multiple desktops yet, Mission Control will create a new one. 

![image](https://github.com/user-attachments/assets/08cd28e4-ca22-436c-9722-9438d6f4ed59)

![image](https://github.com/user-attachments/assets/1b5d4c72-0666-4fce-ab1b-4518a08c61c4)

![image](https://github.com/user-attachments/assets/b6e8cfbf-1dc5-43b4-b496-b13e1f292c9c)

## Part VII. File Management with Time Machine

### Task 1. Set up and practice using Time Machine for backups

Open system settings and click Time Machine, if you can't find it type in "Time Machine" in the search bar. Connect an external drive or use an available network drive for backups. Toggle Time Machine on and choose the backup disk. Wait for Time Machine to start backing up automatically. After a backup, try restoring a file by clicking Enter Time Machine from the Time Machine menu in the menu bar. You've succesfully set up Time Machine for backups and restored a file. 

![image](https://github.com/user-attachments/assets/9bc11346-ff2e-472a-8bda-12844bd62d85)


# Setting up MDM for Mac devices via Jamf

### Task 1: Set up Jamf Pro Account(If you don't have one)

Sign up for Jamf Pro Demo by visiting the Jamf Pro Demo page to create a few demo account. Once you have access, log into your Jamf Pro dashboard. Jamf Pro's demo environment will give you full access to the features for managing devices.

![image](https://github.com/user-attachments/assets/d74d4a68-7bfb-40f2-8bb8-99da52ea9a00)

### Task 2: Prepare your macOS Device

Ensure macOS is updated to the latest version compatible with MDM (macOS Ventura 13.7.5). Unenroll the device from any exisitng MDM if applicable. On the macOS device, ensure that remote management is allowed in the settings.

![image](https://github.com/user-attachments/assets/f145a10b-cbf8-4062-83e0-f7bd12cd046a)

![image](https://github.com/user-attachments/assets/84f52695-cf6a-49d1-82b9-4c591ef0c9d6)

### Task 3: Create a PreStage Enrollment Profile

In Jamf Pro, go to Devices > PreStage Enrollments. Click New to create a PreStage Enrollment profile for macOS devices. For set up: wi-fi configuration (set network settings for automatic wi-fi connection), skip steps (skip initial setup steps, like Apple ID, during the enrollment process), and supervised mode (enable to allow full management and additional control over the device). Then save the PreStage Enrollment profile

### Task 4: Enroll the Device

In Jamf Pro, navigate to Devices > Enrollments > Enrollment Methods. Choose a enrollment method, either apple school/business manager (for automatted enrollment) or apple configurator 2 (for manual enrollment). Folloow the on-screen instructions to download the Jamf MDM Profile on the macOS device. Install the Profile on the macOS device. After installation, the device will be connected to Jamf Pro and begin receiving MDM settings.

### Task 5: Configure Device Management Settings

Go to Configuration profiles such as (wi-fi configuration, security settings, and VPN or app management). Assign these profiles to the enrolled macOS device.

### Task 6: Monitor and Manage the Device

In Jamf Pro, you can view the device's status in the Device Inventory. You can deploy updates, enforce policy, and track compliance.

# Managing macOS Devices Using Apple Remote Desktop

### Task 1: Enable Remote Management on Target macOS Devices

On each macOS device you want to control remotely, make sure that remote management is allowed under settings. (System Settings > General > Sharing) Enable Remote Management by checking the box. Click options and select the actions you want to allow (i.e. observe, control, or copy files). Set the appropriate user access rights (admin or standard user). Ensure the target devices are connected to the network.

![image](https://github.com/user-attachments/assets/88eecb52-7488-4977-8e18-85b8c13c8340)

![image](https://github.com/user-attachments/assets/591716ad-c3c4-446e-8d65-c32f3f015e97)

![image](https://github.com/user-attachments/assets/d31233e6-4d64-43b5-85b4-4ddb744be308)

### Task 2: Install and Configure Apple Remote Desktop

Install Apple Remote Desktop (ARD) on your macOS Ventura system. Open ARD and add remote devices. To do so open ARD and click Scanner to search for available devices on the network. Add the devices to your list by selecting them and clicking add. Authenticate with the credentials of the remote devices.

### Task 3: Remote Control Setup

Select a device from the ARD interface and click Control to start a remote session. Explore the following features (observe: view what the user is doing, control: take full control of the device, send text: send messages to the remote user, lock screen: lock the remote system for security purposes, transfer files: send files to/from remote devices.

### Task 4: Automate Common Administrative Tasks

Use Applescript or Automator in combination with ARD to automate tasks such as installing software remotely on multiple macOS devices, running scripts for system maintenance and/or restarting systems or applications remotely.

### Task 5: Monitor and Troubleshoot Devices

Use the Reports feature in ARD to monitor system status. Troubleshoot remote devices by accessing their logs (Console app) and using Network Utility for network issues. You can also rebot or restart the device remotely if necessary.


