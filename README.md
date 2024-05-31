
# TerminalOnAndroid
Running Linux terminal on Android using Termux.

## Requisites:
1. Termux application from F-Droid only.
2. Android 7.0 or newer with available storage.
3. With good Network speed
## Follow Steps:

### Step 1: Install Termux
1. Download and install Termux from the F-Droid store or from their GitHub repo using one of the following links:
   - [Termux on F-Droid](https://f-droid.org/packages/com.termux/)
   - [Termux on GitHub](https://github.com/termux/termux-app/releases)

   **Note:** The official Termux Wiki and Termux GitHub pages indicate that you should not install the outdated version hosted on the Google Play Store.

2. Download the latest Termux version. At the time of writing, it is `termuxapp_v0.118.0+github-debug_arm64-v8a.apk` from the GitHub link above.

3. Once downloaded, install it and allow permissions if asked.

### Step 2: Update Termux
1. Open the Termux application.
2. Enter the following command to update Termux:
   ```sh
   pkg update -y
   ```

### Step 3: Setup Storage Permissions
1. Give storage permission to read and write on Android storage by entering the following command:
   ```sh
   termux-setup-storage  
   ```
2. Press the "Allow" button when prompted.

### Step 4: Install Required Packages
1. Install `wget`. When prompted, press `Y` and `Enter` to continue:
   ```sh
   pkg install wget   
   ```

### Step 5: Download and Install NetHunter
1. Download the NetHunter install file. Ensure you enter the correct address:
   ```sh
   wget -O install-nethunter-termux https://offs.ec/2MceZWr
   ```
2. Change the permissions to execute the file:
   ```sh
   chmod +x install-nethunter-termux
   ```

### Step 6: Install Kali Linux
1. Run the installation script:
   ```sh
   ./install-nethunter-termux
   ```
2. Enter the image that you want to install. We are going to install 2.
3. The installation will take a while. When asked to delete `rootfs`, enter `N`.

### Step 7: Run Kali Linux
1. After successful installation of NetHunter, run the following command to run Linux terminal as a root user:
   ```sh
   nh -r
   ```
### Step 8: Configure DNS
Once Kali Linux is running, you may need to configure DNS to point to Google's DNS servers. Run the following command:

```sh
echo "nameserver 8.8.8.8" > /etc/resolv.conf
echo "nameserver 8.8.4.4" >> /etc/resolv.conf
```
And that's it!

## Additional Information:
- You can run all your Linux commands as like terminal and install applications such as Git, Java, Python, Maven, Jenkins server, and access them through a local browser.
- Note that there are some limitations over network access due to Android security policies.
- You can create and edit your programming or coding files within this environment.
