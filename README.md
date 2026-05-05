# Below loom video explains how to setup the app in you local
https://www.loom.com/share/f9e7d90ae901409c8184dd6f175362f9?sid=e9b7bf15-f061-4bcf-9503-1ccea546e4a0

## Clone the repo and install dependencies

```bash

`Clone the repository`

git clone https://github.com/Schedula-Services/Schedula-Android-App3.git
cd Schedula-Android-App3/

`Install dependencies`

$ npm install
or
$ yarn install
```

## Install Android studio and setup the development environment

### Node and JDK
- You will need Node, the React Native command line interface, a JDK, and Android Studio.

- Install Node & JDK. It is recommended to install `Node` via [Chocolatey](https://chocolatey.org/install).
- React Native also requires Java SE Development Kit (JDK), which can be installed using Chocolatey as well. Open an Administrator Command Prompt (right click Command Prompt and select "Run as Administrator"), then run the following command: `choco install -y nodejs-lts microsoft-openjdk17`

- If you have already installed `Node` on your system, make sure it is `Node 18` or newer. If you already have a JDK on your system, it is recommended `JDK17`.


### Android Studio
- While you can use any editor of your choice to develop your app, you will need to install Android Studio in order to set up the necessary tooling to build your React Native app for Android.

    - **Install Android Studio**

        [Download and install Android Studio](https://developer.android.com/studio/index.html) While on Android Studio installation wizard, make sure the boxes next to all of the following items are checked:

            1. Android SDK
            2. Android SDK Platform
            3. Android Virtual Device

        Then, click "Next" to install all of these components. If the checkboxes are grayed out, you will have a chance to install these components later on. Once setup has finalized and you're presented with the Welcome screen, proceed to the next step.

    - **Install the Android SDK**

        Android Studio installs the latest Android SDK by default. Building a React Native app with native code, however, requires the Android 13 `Tiramisu` SDK in particular. Additional Android SDKs can be installed through the SDK Manager in Android Studio. To do that, open Android Studio, click on `More Actions` button and select `SDK Manager`. The SDK Manager can also be found within the Android Studio `Settings` dialog, under `Languages & Frameworks → Android SDK`.

        Select the `SDK Platforms` tab from within the `SDK Manager`, then check the box next to `Show Package Details` in the bottom right corner. Look for and expand the Android 13 `Tiramisu` entry, then make sure the following items are checked:

            1. Android SDK Platform 33
            2. Intel x86 Atom_64 System Image or Google APIs Intel x86 Atom System Image

        Next, select the `SDK Tools` tab and check the box next to `Show Package Details` here as well. Look for and expand the Android SDK Build-Tools entry, then make sure that `33.0.0` is selected.

        Finally, click `Apply` to download and install the Android SDK and related build tools.

    - **Configure the ANDROID_HOME environment variable**

        The React Native tools require some environment variables to be set up in order to build apps with native code.

            1. Open the Windows Control Panel.
            2. Click on User Accounts, then click User Accounts again
            3. Click on Change my environment variables
            4. Click on New... to create a new ANDROID_HOME user variable that points to the path to your Android SDK

        You can find the actual location of the SDK in the Android Studio `Settings` dialog, under `Languages & Frameworks → Android SDK`.

    - **Add platform-tools to Path**

            1. Open the Windows Control Panel.
            2. Click on User Accounts, then click User Accounts again
            3. Click on Change my environment variables
            4. Select the Path variable.
            5. Click Edit.
            6. Click New and add the path to platform-tools to the list.

    - **Preparing the Android device**

        You will need an Android device to run your React Native Android app. This can be either a physical Android device, or more commonly, you can use an Android Virtual Device which allows you to emulate an Android device on your computer. Either way, you will need to prepare the device to run Android apps for development.

        - **Using a virtual device** - If you have recently installed Android Studio, you will likely need to [create a new AVD]((https://developer.android.com/studio/run/managing-avds.html)). Select `Create Virtual Device...`, then pick any Phone from the list and click `Next`, then select the `Tiramisu API Level 33 image`. Click  `Next` then `Finish` to create your AVD. At this point you should be able to click on the green triangle button next to your AVD to launch it, then proceed to the next step.


## Android Build

```bash
$ npm android
or
$ yarn android

# If android build failed with Error on instalDebug task use following command
$ react-native run-android --variant=DevDebug
```
# Schedula
# Schedula
