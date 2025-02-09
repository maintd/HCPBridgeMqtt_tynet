# How to Flash the Firmware

## Set up software

Download and install VS Code to your Computer: https://code.visualstudio.com/download

After that, open VS Code and go to "Extensions", search for PlatformIO and install it, following any instructions if a restart or something is needed

## Get firmware

1. On the main repo, click the green Get Code Button and download the firmware as a zip.
2. Extract the zip file and remember where you put it on your PC.
3. Go to VSCode, click the PlatformIO Symbol at the bottom to switch to the Plugin UI.
4. Click the "Open Folder" button and select the HCPBridgeESp32 folder inside the extracted firmware.

![image](Images/project.png)

## Configuration

1. In this step you can preset the preferences. On first boot they will be stored on the memory of the ESP.
2. After you have to change it from the Web UI or reset the ESP memory to load again the data from the configuration file.
3. Use the left sidebar again and click on the folder symbol to switch to the file list.
4. Before you can flash the firmware, you will need to change the configuration in the configuration.h file located in the src folder.

You need to set your Wi-Fi name and password as well as the connection details to your MQTT Server if you want to use that feature.

![image](Images/configuration.png)

## Build and flash

1. Go back to the PlatformIO UI and click on the ESP model you got under "Project Tasks".
2. ESP32 for older boards and ESP32S3 for newer boards (for example all PCBs with a Tynet logo)
3. Open the "General Tasks" of the board you got and click "Build".

![image](Images/upload.png)

This should prepare the firmware for your board including your configuration. If all goes well, the terminal will show a green success message.

If this works, you can connect your device and click "Upload Task" to flash it. This should also result in a success info in green text inside the terminal.

After this, you can replug your device from USB to restart it, and it should connect to your Wi-Fi Router and MQTT Server.

Finally, you can connect it via the RJ12 cable to your garage door and start the BUS scan. If it is successful, the two communication LEDs should blink fast.
With this the MQTT as well as web controls on the devices IP should also work, and you are done :)
