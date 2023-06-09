
# ReaListi

This project aims to be a strong foundation for react-native applications. It provides a clear and organized structure, core dependencies, and boilerplate to jumpstart development.


## Prerequisites

- [Node.js](https://nodejs.org/en) and npm (Recommended: Use [nvm](https://github.com/nvm-sh/nvm))
- [Watchman](https://facebook.github.io/watchman/)
- [Xcode](https://developer.apple.com/xcode/)
- [Cocoapods](https://cocoapods.org/)
- [JDK](https://www.oracle.com/java/technologies/downloads/)
- [Android Studio and Android SDK](https://developer.android.com/studio)
- [Expo](https://docs.expo.dev/get-started/installation/)
- [VS Code Editor](https://code.visualstudio.com/download)

## Base dependencies

- [react-native (0.71.1)](https://reactnative.dev/docs/getting-started) open-source JavaScript framework based on [React](https://reactjs.org/), designed for building apps on multiple platforms like iOS, Android and web applications, utilizing the very same code base
- [@openspacelabs/react-native-zoomable-view](https://github.com/openspacelabs/react-native-zoomable-view#readme) for a pinch to zoom, tap to move and double tap to zoom capability.
- [@react-native-community/netinfo](https://github.com/react-native-netinfo/react-native-netinfo) allows you to get information on - Connection type and Connection quality
- [@react-navigation/bottom-tabs](https://reactnavigation.org/docs/bottom-tab-navigator/) for a tab bar on the bottom of the screen
- [@react-navigation/drawer](https://reactnavigation.org/docs/drawer-based-navigation/) is to use drawer from left (sometimes right) side for navigating between screens
- [@react-navigation/native](https://reactnavigation.org/docs/getting-started/) is a standalone library that enables you to implement navigation functionality in a React Native application
- [@stripe/stripe-react-native](https://www.npmjs.com/package/@stripe/stripe-react-native) provides powerful and customizable UI screens and elements that can be used out-of-the-box to collect your users' payment details
- [apisauce](https://github.com/infinitered/apisauce) is a low-fat wrapper for the amazing axios http client library, all responses follow the same flow: success and failure alike
- [expo-apple-authentication](https://docs.expo.dev/versions/latest/sdk/apple-authentication/) provides Apple authentication for iOS 13+. It does not yet support lower iOS versions, Android, or the web
- [expo-firebase-recaptcha](https://docs.expo.dev/versions/v47.0.0/sdk/firebase-recaptcha/) provides a set of building blocks for creating a reCAPTCHA verifier and using that with your Firebase Phone authentication workflow 
- [expo-linear-gradient](https://docs.expo.dev/versions/latest/sdk/linear-gradient/) provides a native React view that transitions between multiple colors in a linear direction.
- [expo-linking](https://docs.expo.dev/guides/linking/) Native apps, like the ones built with React Native, can implement any URL scheme, and the JavaScript React layer can handle the URL used to launch the corresponding native app.
- [expo-location](https://docs.expo.dev/versions/latest/sdk/location/) allows reading geolocation information from the device.
- [expo-notifications](https://docs.expo.dev/versions/latest/sdk/notifications/) provides an API to fetch push notification tokens and to present, schedule, receive and respond to notifications.
- [expo-secure-store](https://docs.expo.dev/versions/latest/sdk/securestore/) provides a way to encrypt and securely store key–value pairs locally on the device.
- [formik](https://formik.org/docs/overview) Formik is the world's most popular open source form library for React and React Native.
- [html-entities](https://www.npmjs.com/package/html-entities) Fastest HTML entities library.
- [lottie-react-native](https://www.npmjs.com/package/lottie-react-native) Lottie is an ecosystem of libraries for parsing Adobe After Effects animations exported as JSON with bodymovin and rendering them natively.
- [react-native-draggable-flatlist](https://github.com/computerjazz/react-native-draggable-flatlist) A drag-and-drop-enabled FlatList component for React Native.
- [react-native-geocoding](https://www.npmjs.com/package/react-native-geocoding) A geocoding module for React Native to transform a description of a location (i.e. street address, town name, etc.) into geographic coordinates (i.e. latitude and longitude) and vice versa.
- [react-native-maps](https://github.com/react-native-maps/react-native-maps) for display map into application
- [react-native-razorpay](https://github.com/razorpay/react-native-razorpay) to accept payments from customers on your app built using React Native.
- [react-native-svg](https://github.com/software-mansion/react-native-svg) provides SVG support to React Native on iOS, Android, macOS, Windows, and a compatibility layer for the web.
- [react-native-webview](https://github.com/react-native-webview/react-native-webview) is a community maintained WebView component for React Native.
- [react-native-youtube-iframe](https://lonelycpp.github.io/react-native-youtube-iframe/) is a wrapper of the Youtube IFrame player API build for react native.
## Features

- Light/dark mode toggle
- Live previews
- Fullscreen mode
- Cross platform


## Installation

Install ReaListi with yarn

```bash
git clone https://github.com/1986webdeveloper/ReaListi.git
cd ReaListi
yarn install
cd ios && pod install
yarn start
```

## Folder Structure

This project follows a very simple structure :

```
├── ReaListi
│ ├── api (Contains apisauce function with different params)
│ ├── app (Contains function for the local storage)
│ ├── assets (Contains fonts, images, json files for the amination, svg images)
│ ├── components (Folder to store any common component that you use through your app)
│ ├── helper (Contains manipulation functions like decodeString, getCurrencySymbol, getPrice)
│ ├── language (Contains json file to store default text which is used in application with english and arabic language)
│ ├── navigation (Contains home navigator, tab navigator and drawer navigator)
│ ├── screens (Folder that contains all your application screens/features)
│ ├── variables (Contains json file for the colors)
│ ├── App.js (Main component that starts your whole app)
│ ├── index.js (Entry point of your application as per React-Native standards)
│ ├── reducer.js (Contains all the different reducers with the initial state)
```

## Generate production version
These are the steps to generate ```.apk```, ```.aab``` and ```.ipa``` files

### Android
- Generate an upload key
- Setting up gradle variables
- Go to the android folder
- Execute ```./gradlew assemble[Env][BuildType]```

**Note**: You have three options to execute the project assemble: Generates an apk that you can share with others. install: When you want to test a release build on a connected device. bundle: When you are uploading the app to the Play Store.

For more info please follow https://reactnative.dev/docs/signed-apk-android

### iOS
- Go to the Xcode
- Select the schema
- Select 'Any iOS device' as target
- Product -> Archive

For more info please follow https://reactnative.dev/docs/publishing-to-app-store


## Customization

These area can be customized as per requirement.

- **App Configuration:** Update the app's configuration files, such as `app.json`, `babel.config.js` and `metro.config.js`, to match desired settings.

- **Directory Structure:** Adjust the project's directory structure to better organize codebase.

- **Styling and Theming:** Modify the existing styles and themes or add own to create a unique visual identity for app.

- **Additional Scripts:** Extend the `scripts` directory with own scripts to automate repetitive tasks specific to project.