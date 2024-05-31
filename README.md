# TerminalOnAndroid
Running linux terminal on android using termux.

# Requisites:
1. Termux application from f-droid only.
2. Android Phone with storage available.

# Follow steps:
1. You will need to install Termux. You can get Termux from the F-Droid store or from their

GitHub repo using one of the following links (In the demo we use GitHub):
• https://f-droid.org/packages/com.termux/

• https://github.com/termux/termux-app/releases

Take note that the official Termux Wiki and Termux GitHub pages indicates that 
**you should not install the outdated version hosted on the Google Play Store**

2. Download the latest Termux version at the time of writing it is termuxapp_v0.118.0+github-debug_arm64-v8a.apk from the github link above.

3. Once downloaded install it with allow permission if asked.
4. Open termux application
5. Enter the following command:
   ```
   pkg update -y
   ```
6. Give storage pemission to read and write on android storage.
   Enter the following command:

   ```
    termux-setup-storage  
   ```
 Press "Allow" button.
7. Install wget and when you’re asked Do you want to continue, press Y and Enter.
  ```
   pkg install wget   
  ```
8. When you get asked to “Do you want to continue” press Y and Enter.
9. Download the NetHunter install file. Ensure that you enter the correct address.
```
   wget -O install-nethunter-termux https://offs.ec/2MceZWr
```
10. Change the permissions so that you can execute the file:
``
chmod +x install-nethunter-termux
```
12. Enter the image that you want to install. We are going to install 2.
13. The installation will take a while, when asked to delete rootfs, enter N.

14. After successful installation of nethunter, run following command to run linux terminal as a root user.
```
nh -r
'''
And that's it. 
Here we can run all our linux 
also install and use applications git and repositories, maven, jenkins server and access them through local browser.
But it has some limitations over network access because of android serurities policy reasons.
 
