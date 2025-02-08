# Instructions :-

1.) Navigate to About Phone -> Build Number. Click on it 6 to 7 times, upon which You are now a developer is shown.

2.) Now, navigate back to Settings -> Developer Options and select the option Enable USB debugging.

3.) Connect the device to a computer through USB.

4.) Now, open Command Prompt and execute the following command:

    adb devices

which will show you the connected devices.

5.) Then execute following command to take log:

    adb logcat > file.txt
This will generate the ADB logs and the logs will be saved to the file.txt file.

6.) You can now share the file.txt file to me.
<br>

# Additional :- 
* To capture logs for specific issues (e.g., camera crashes, etc ), follow these steps:
  
  Open the app or service that is crashing (e.g., the camera app) while capturing the ADB log.
  ( for example, if your camera is crashing or specific feature of camera is not working then you need to try to use that specific feature which is not working. )

<br> <a href="https://github.com/user-attachments/assets/81e826a2-cb90-4dcc-8e3c-6c42f0234163" target="_blank"> <img src="https://github.com/user-attachments/assets/81e826a2-cb90-4dcc-8e3c-6c42f0234163" width="300"> </a> <br> <br> 
![Screencast 2024-08-06 18_13_20](https://github.com/user-attachments/assets/fca838d1-fc2b-4542-a96d-ff0b6f1ed7e1)


        
