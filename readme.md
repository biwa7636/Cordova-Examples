# Cordova Demos
===

This repository contains a set of Cordova (PhoneGap) example apps. Each folder contains the www folder for a project. To use it, you may either copy the files manually into a www folder, or use the --link-to option of the Cordova CLI.

Each folder has its own readme with individual instructions for the project.

Here are some example instructions to help quickly get something up and running. 

##  1. Prerequisite
	- [cordova](https://cordova.apache.org/docs/en/latest/guide/cli/index.html) 
	- phonegap [desktop](http://docs.phonegap.com/getting-started/1-install-phonegap/desktop/)/[cli](http://docs.phonegap.com/references/phonegap-cli/) (if you want to see examples running on your phone)

##  2. Preparation

make a tmp workspace 

```
mkdir ~/Desktop/myworkspace && cd $_
```

download the examples 

```
git clone https://github.com/cfjedimaster/Cordova-Examples.git
```
create an application (--link-to=<PATH>: symlink to custom www assets without creating a copy.), replace arialscreensaver with the name of the app you like

```    
cordova create --link-to=Cordova-Examples/arialscreensaver/www/ myApp && cd $_
```

add in the [platforms](https://cordova.apache.org/docs/en/4.0.0/guide/platforms/) that interest you 
    
```
cordova platform add browser ios
```

Note: I may have skipped a few commands when I first started the environment, like ios-sim, etc, you might also need to add in the relevant plugin by issuing the command `cordova plugin add ...`, a quick Google search can help you find the solution. 

## 3. Run the code
	
### - option1: Browser (easiest)
```
cordova emulate browser
```

<a href="/resources/screenshots/readme_browser.png"><img width="150" src="/resources/screenshots/readme_browser.png" align="middle"></a>


### - option2: Phone Emulator
```
cordova emulate ios
```

<a href="/resources/screenshots/readme_ios.png"><img width="150" src="/resources/screenshots/readme_ios.png" align="middle"></a>


### - option3: Device

There are several ways to deploy application to a device, my favorite way so far is to use phonegap so that I can avoid hassles like [here](https://stackoverflow.com/questions/30736932/xcode-error-could-not-find-developer-disk-image), [here](https://stackoverflow.com/questions/39501020/code-sign-error-on-xcode-8-and-ios-10-cordova-project) and [here](https://stackoverflow.com/questions/18727894/how-can-i-find-my-apple-developer-team-id-and-team-agent-apple-id) just for the purpose of playing without getting too serious. 

There is application loaded at this stage
Add an existing project by pointing to the myApp folder, start and remember the address
Download the phonegap from Appstore and point the app to the address above
Successfully download and run smoothly on your phone
For more information, please refer to the official document of Phonegap DesktopApp/CLI

<a href="/resources/screenshots/readme_phonegapdesktop_empty.png"><img width="150" src="/resources/screenshots/readme_phonegapdesktop_empty.png" align="middle"></a><a href="/resources/screenshots/readme_phonegapdesktop_loaded.png"><img width="150" src="/resources/screenshots/readme_phonegapdesktop_loaded.png" align="middle"></a><a href="/resources/screenshots/readme_device_phonegap.PNG"><img width="150" src="/resources/screenshots/readme_device_phonegap.PNG" align="middle"></a><a href="/resources/screenshots/readme_device_deployed.PNG"><img width="150" src="/resources/screenshots/readme_device_deployed.PNG" align="middle"></a>
