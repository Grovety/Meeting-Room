# Installation & Setup

There are two ways to install the Meeting Room Panel software.

___

[**1. Quick Installation (recommended)**](https://github.com/Grovety/Meeting-Room/edit/main/Installation_and_Setup#-quick-installation)

   Use the prebuilt firmware and installer. 

   This is the fastest way to test the system and takes only a few minutes.
   
   ___

[**3. Development Installation**](https://github.com/Grovety/Meeting-Room/edit/main/Installation_and_Setup#-development-installation-repository)

   Clone the repository and build the firmware yourself.

   This option is recommended if you plan to modify the project or integrate it into your own system.
   ___

## ⚡ Quick Installation


Steps
1. Flash the firmware using Flashtool.exe
2. Connect the panel to Wi-Fi using the configuration tool
3. Add your Google Calendar ICS link


### Flash the firmware using Flashtool.exe

1.	Download the Firmware.7z archive: https://github.com/Grovety/Meeting-Room/raw/main/Firmware.7z

2.	Extract the archive.
   
4.	Connect the **CrowPanel ESP32-S3** (5" or 7") to your PC with a **USB Type-C** cable


![photo_2026-03-12_13-27-49-2](https://github.com/user-attachments/assets/1699f5bc-5391-42a7-9649-38bbdfd0da74)


5.	Run **Flashtool.exe** from the extracted folder and wait until the installation is complete.

___

   
<img width="441" height="91" alt="image" src="https://github.com/user-attachments/assets/6cc05146-ab30-4b1d-8727-89530ff47265" /> 

________________________________________

<img width="890" height="466" alt="image" src="https://github.com/user-attachments/assets/835aefde-05a4-455c-8ae8-7b4d18fa7846" /> 
___

Once finished, the application will start automatically on the panel.


5.	Close the installer window.

   
7.	Restart the panel (disconnect and reconnect the USB cable).

   
## Application Setup

After installing the firmware, you need to configure the device.

Steps
1.	Connecting the panel to Wi-Fi
2.	Linking your Google Calendar
3.	(Optional) Connecting the EnSens air quality module

   
### Connect to Wi-Fi
1.	Download the configurator application: https://github.com/Grovety/Meeting-Room/raw/main/CrowPanelConfigurator.exe

2.	Run **CrowPanelConfigurator.exe**.
The configurator will open and automatically detect the panel's COM port.
<img width="922" height="552" alt="image" src="https://github.com/user-attachments/assets/e3f40df8-a766-4f25-8a18-aac00b027ffd" />


3.	Enter your Wi-Fi credentials:
   
- SSID (network name)

- Password

And click Send WiFi to Panel to transfer the configuration to the panel.

<img width="922" height="552" alt="image" src="https://github.com/user-attachments/assets/d7c46e5b-301b-4b09-ac9d-cb48d832b1ed" />


The Wi-Fi settings are stored in the device’s non-volatile memory and will be used automatically on every boot.

<img width="921" height="551" alt="image" src="https://github.com/user-attachments/assets/1d3e6dfe-033b-4fa9-aa33-64f28ce70187" />

You can also connect to Wi-Fi directly from the panel.

Tap the gear icon in the top-left corner of the main screen to open the settings menu.
Select your Wi-Fi network from the list and enter the password using the on-screen touch keyboard.

![Photo1](https://github.com/user-attachments/assets/8f0aab15-5367-4bb6-908d-5f6e1970a895)

![photo2](https://github.com/user-attachments/assets/155fc49a-eb35-4c72-953b-302a23c825c9)



### Connect Google Calendar (Optional)

To display events from Google Calendar:

1. Get the ICS link
    - Open Google Calendar on your PC: https://calendar.google.com/calendar/
    - Under My calendars, locate the calendar you want, (1) click the three dots **(⋮)** next to the calendar name, (2) Select **Settings and sharing**
      
    
        <img width="573" height="386" alt="image" src="https://github.com/user-attachments/assets/c4d223fb-d7ed-4db1-8393-717f7617c803" />

         <img width="546" height="456" alt="image" src="https://github.com/user-attachments/assets/bf62ea24-6bf3-4c13-b5f0-4d44e3ed7a47" />

     - (3) Scroll to Integrate calendar, (4) сopy the Secret address in iCal format

      <img width="1044" height="747" alt="image" src="https://github.com/user-attachments/assets/05cdb8f2-f073-4359-8b22-0455118cfe10" />


     - Open **CrowPanelConfigurator.exe**, (5) Select "Send ICS URL" (6) Paste the ICS URL, (7) Click Send ICS URL to Panel

      <img width="922" height="552" alt="image" src="https://github.com/user-attachments/assets/885b0db5-ca16-43b2-bd00-d6353dcb8d4a" />


Open the Calendar screen on the panel and check that events appear.

### Connect the Air Quality Module (Optional)
If you want to monitor air quality:
1. Locate the W-M connector on the board.
2. Insert the EnSens module into the connector.
3.	Check the pin orientation.
The board has markings near the connector — make sure the module is aligned with the 0 / 1 markings.
4.	Open the Climate screen on the panel.
IAQ and CO₂ values should appear.

## 🚀 Development Installation (Repository)

If you want to modify the project or build the firmware yourself:
1. Get the project
2. Clone the repository:
git clone https://github.com/Grovety/Meeting-Room.git


or download the ZIP archive from GitHub.

### Flash the firmware
1.	Connect the board via USB-C
2.	Locate flash_tool.exe in the repository
3.	Run the tool — it will automatically detect the COM port
4.	Follow the on-screen instructions
After flashing completes, the board will reboot and start the application.


## 🐛 Troubleshooting


Problem: **Screen does not turn on after flashing**

Solution

•	Check the USB cable connection

•	Ensure flashing is completed without errors

•	Power-cycle the board

•	Repeat the flashing process if necessary

________________________________________


Problem: **Board not detected as a COM port**

Solution

•	Ensure the CP210x driver is installed

•	Try another USB cable

•	Reboot your PC

•	Check Device Manager for unknown devices

________________________________________


Problem: **Wi-Fi does not connect**

Solution

•	Verify the Wi-Fi password

•	Use a 2.4 GHz network (ESP32-S3 does not support 5 GHz)

•	Restart the board

________________________________________
Problem: **Calendar does not show events**

Solution

•	Ensure the ICS link is copied correctly

•	Check that the device has internet access

•	Confirm that the calendar contains events

•	Try sending the link again

________________________________________


Problem: **EnSens module not detected**

Solution

•	Ensure the module is fully inserted

•	Check orientation against the 0 / 1 markings

•	Reinsert the module and reboot the board

________________________________________


## Installing the CP210x Driver
If your computer does not recognize the board, install the USB-to-UART driver.
1.	Go to
https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers
2.	Download the Windows 64-bit driver
3.	Install the driver following the vendor instructions
4.	Reboot your computer
5.	Reconnect the board — it should appear in Device Manager as a COM port.

