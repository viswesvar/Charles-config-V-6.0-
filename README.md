# Charles-config-V-6.0-
This is document written to configure Charles version greater than 5.0  
This article describes the steps to be able to analyse HTTP request in Android app version greater than 5.0.

# The requirements are:

 • Charles proxy
 • Android device
 • Android app apk (it can point to any environment, i.e. production or staging)
 
## Step-by-step guide
1. Clone or download the repository https://github.com/levyitay/AddSecurityExceptionAndroid
2. Download Charles certificate, install it on Android device and configure the proxy settings as described in 
https://community.tealiumiq.com/t5/Tealium-for-Android/Setting-up-Charles-to-Proxy-your-Android-Device/ta-p/5121
(If the you have problems installing the certificate by double-clicking, you can try `Settings > Wifi > 3 dots button at the top right corner > Advanced > Install certificates`)
3. Run the command `./addSecurityExceptions.sh <name-of-the-app>-debug.apk`  in you command line tool
4. Run Charles
5. Install the new APK generated into your Android device
6. You should now be able to see requests and responses in Charles logs
