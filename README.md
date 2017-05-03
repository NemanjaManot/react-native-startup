# React Native Startup
## Installation for different OS

## Content
- [About](#about)
- [Setup and bundling](#setup-and-bundling)
- [Installation on MAC](#installation-on-mac)
- [Installation on Windows or Linux](#installation-on-windows-or-linux)
- [Useful links for learning React Native](#useful-links-for-learning-react-native)

## About

###### Official definition
> *React Native lets build mobile apps using only JavaScript. It uses the same design as React, letting you compose a rich mobile UI from declarative components.*

###### React.js VS React Native
React Native is a consequence of React (the library). We are still writing React code, but the framework we are using (React Native) offers additional functionality to run app on iOS or Android. If someone know React, he already know most of React Native.

A few simple examples of the differences between React.js and React Native:
 * RN instead of `div` or `p`  use components like `<View>` or `<Text>`
 * RN don't use CSS, we just style our application using JavaScript
 * Instead of routing to different web pages, you are navigating between different scenes of your application, when you use RN


## Setup and bundling

When you start a new project with ReactJS, you probably will choose a bundler like Webpack and try to figure out which bundling modules you need for your project. React-Native comes with everything you need and you most likely wouldn’t need more.

To run your app, you will need to have [**Xcode**](https://itunes.apple.com/us/app/xcode/id497799835?mt=12) (for iOS, on Mac only) or [**Android Studio**](https://developer.android.com/studio/index.html) (for Android, on Windows or Linux) installed on your computer. You can either decide to run it on a simulator/emulator of the platform you want to use or directly on your own devices.


## Installation on MAC

* [Follow instruction](https://facebook.github.io/react-native/docs/getting-started.html)

<img src="http://i.imgur.com/BhsonI0.jpg"></img>

**1.** Install [**Xcode**](https://itunes.apple.com/us/app/xcode/id497799835?mt=12). You must have latest version installed.

**2.** [**HomeBrew**](https://brew.sh/). Follow instruction and install HomeBrew.

**3.** After installing HomeBrew run the following commands in a Terminal:

`brew install node`

`brew install watchman`

**NOTE:** If you have already installed Node on your system, make sure it is version 4 or newer.

**4.** Install watchman

`brew install watchman`

**5.** React Native CLI

`npm install -g react-native-cli`


- Test iOS app:
Change directory and start new project 
```
react-native init TestProject
cd TestProject
react-native run-ios
```

**NOTE:** If you want to start android device on Mac, you follow [this steps](https://facebook.github.io/react-native/docs/getting-started.html) and/or steps on Windows/Linux instalation (under this) – download, install and setup Android Studio and environment variables.




## Installation on Windows or Linux

* [Follow instruction](https://facebook.github.io/react-native/docs/getting-started.html)

**NOTE:** Installation process for Windows and Linux are similar with a few differences.

**1.** Install [Java SDK](http://www.oracle.com/technetwork/java/javase/downloads/index-jsp-138363.html)

**2.** Install [Node](https://nodejs.org/en/)

**3.** Install [Python 2](https://www.python.org/downloads/) **(only on Windows)**

**4.** Download and install [Android Studio](https://developer.android.com/studio/index.html)

**5.** Install React Native command line tools

`npm install -g react-native-cli`

**6.** Start with test project in appropriate folder

`react-native init TestProject`

**7.** Start Android Studio and open your TestProject. Navigate: .../TestProject/android

When project start you probably have some message like this:

<img src="http://i.imgur.com/eu6119z.jpg"></img>

All you need to do is click that blue text and install some things.

After that you have new message and you must to do same thing again – click blue text and install.

<img src="http://i.imgur.com/En2f45p.jpg"></img>

**8.** Create android emulator

  - In Android Studio open > Tools / Android / AVD Manager
  - Click – *Create new device* (or something like that)
  - Choose a device (e.g Nexus 5) and click *Next*
  - Select **Marshmallow 23** and click *Download*. After installation click *Next* > *Finish*. 
  - Run your Virtual Device – click on *green play button* – and emulator is now working, but not done yet...
  
  **9.1.** Environment Variables **(for Windows)**
  - Go to System Properties, open *Advanced* window and click on *Environment Variables* button.
  - Adding new variables – click *New* button.
  - Set *variable name* to **JAVA_HOME**
  - Browse *variable value* to: **C:\ProgramFiles\Java\jdk1.8.0_101**
  - In the same place, in list of variables find *Path* and click *Edit*. Now, click on *New* button and set a new path, something like this:
  
  `C:\Users\YourComputerName\AppDada\Local\Android\sdk\platform-tools`
  
  **9.2.** Environment Variables **(for Linux)**
  
  Add the following lines to your **~/.profile** (or equivalent) config file:
  
  - First - open .profile:
  
  `gedit ~/.profile`
  
  - Paste at the end of file something like this:
  ```
  export ANDROID_HOME=${HOME}/Android/Sdk
  export PATH=${PATH}:${ANDROID_HOME}/tools
  export PATH=${PATH}:${ANDROID_HOME}/platform-tools
  ```
  
  - After that save and update changes (maybe and restart computer)
  
  `source ~/.profile`
  
  
  - e.g – my .profile file looks like this
  
  ```
  export HOME=/home/nemanja
  export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64/
  export ANDROID_HOME=$HOME/Android/Sdk/
  export PATH=${PATH}:$ANDROID_HOME/platform-tools:$ANDROID_HOME/tools
  export ANDROID_SDK_HOME=$HOME/android-studio/bin/
  ```
  
  
  - Test Android app:
  
  Path to your TestProject
  
  ```
  cd TestProject
  react-native run-android
  ```
  
  **NOTE:** In my case (i working on Linux) after opening emulator and path to my project i must do this steps:
  ```
  cd TestProject
  react-native start
  react-native run-android
  ```
  
  
  ## Useful links for learning React Native
  
  - [React native website](https://facebook.github.io/react-native/docs/tutorial.html): Best resources for React native you can find here
  - [React Native and Redux](https://www.udemy.com/the-complete-react-native-and-redux-course/): Fantastic tutorial by Stephen Grider which i recommend everyone who want to learn React Native. This course covering all things you need to know to start with RN - installing and setup environment for different OS, begginer and intermediate concepts in RN, testing and debbuging your app...
  - [React Native Advanced](https://www.udemy.com/react-native-advanced/): Another tutorial by Stephen Grider, but this time advanced concepts like animations, maps, notifications, navigation and more
  - For everything else you probably find answer on Google and Stackoverflow.
