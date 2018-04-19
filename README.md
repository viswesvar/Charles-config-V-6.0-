# Charles-config-V-6.0-
This document is written inorder to configure Charles-proxy for Android version greater than 5.0. Below the steps
are provided for the configuration.

# Goal
To analyse HTTP request in Android application with charles-proxy with Android device version greater than 5.0.

# The requirements are:
 • Charles proxy
 • Android device
 • Android app apk (it can point to any environment, i.e. production or staging) recommanded deubug version.
 
## Step-by-step guide
1. Clone or download the repository https://github.com/levyitay/AddSecurityExceptionAndroid
2. Download charles https://www.charlesproxy.com/download/latest-release/
3. Download Charles certificate, install it on Android device and configure the proxy settings as described in 
https://community.tealiumiq.com/t5/Tealium-for-Android/Setting-up-Charles-to-Proxy-your-Android-Device/ta-p/5121
(If the you have problems installing the certificate by double-clicking, you can try `Settings > Wifi > 3 dots button at the top right corner > Advanced > Install certificates`)
4. Run the command `./addSecurityExceptions.sh <name-of-the-app>-debug.apk`  in you command line tool
5. Run Charles
6. Install the new APK generated into your Android device
7. You should now be able to see requests and responses in Charles logs
