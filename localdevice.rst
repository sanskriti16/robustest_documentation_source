Connecting your local devices to RobusTest Device Lab
=====================================================

Requirements

1. A computer system running MacOS, Linux, Windows
2. RobusTest Connect. You can get the RobusTest Connect software from link shared by RobusTest support team
3. Java Develoment Kit

Required software for Android device
Android SDK
Required Software for iOS device

XCode
HomeBrew - https://brew.sh
HomeBrew Modules - Run the following commands to install required packages. Look out for any errors when running the following commands

- brew update
- brew uninstall --ignore-dependencies libimobiledevice
- brew uninstall --ignore-dependencies usbmuxd
- brew uninstall --ignore-dependencies ideviceinstaller
- brew unlink libplist
- brew install --HEAD libplist
- brew install --HEAD usbmuxd
- brew unlink usbmuxd
- brew link usbmuxd
- brew install --HEAD libimobiledevice
- brew link --overwrite libimobiledevice
- brew install ideviceinstaller
- brew link --overwrite ideviceinstaller
- brew install mobiledevice
- brew install ios-deploy
- brew install ios-webkit-debug-proxy
- brew install libzip

Required software for Appium

Appium
iOS  Real Device - github.com/appium/appium-ios-device
Required Software for RobusTest Automator

Run the following commands from the command line while inside the robustest folder

easy_install pip
pip install virtualenv
virtualenv virtualenv
source ~/robustest/virtualenv/bin/activate
pip install requests pillow websocket websocket-client eventlet lxml
Enable Appium log streaming through RobusTest

In your appium installation look for the logsink.js file in the following folder
<node installation folder>/lib/node_modules/appium/build/lib
Replace the logsink.js file in your appium installation with the logsink.js file available here. Make sure you use the logsink.js file which is appropriate for your Appium version.
Installing RobusTest Agent

Unzip the downloaded software. The unzipped file should give you a folder “robustest”
Inside the robustest folder, you will find StartRobusTestAgent.sh file
Open this file in a text editor and provide necessary path for Android SDK
Open your terminal (command line)
Move to the robustest folder
Run the StartNode.sh script by running the command ./StartRobusTestAgent.sh from the command line