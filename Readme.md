# Sample App - React Native
A sample React Native app to demonstrate my skills.

## Key features:
- Sample folder structure
- Basic Authentication screens(Login, Signup, Forgot Password) and flow
- Reusable common components, utility functions and constants
- [Logger](./src/utilities/logger.js) to log data more clearly using coloured logs in Chrome Debugger
- Navigation using [react-navigation](https://reactnavigation.org/) (v6)
- State management using [redux](https://redux.js.org/)
- Redux middleware [redux-saga](https://redux-saga.js.org/)
- Git hooks using [husky](https://typicode.github.io/husky/#/)
- Staging and Production environment configurations using [react-native-config](https://github.com/luggit/react-native-config)
- TDD(Test-Driven Development) using [jest](https://jestjs.io/)
- (Unsecured) local data storage using [AsyncStorage](https://github.com/react-native-async-storage/async-storage#readme)
- Splash screen using [react-native-bootsplash](https://github.com/zoontek/react-native-bootsplash)
- API requests using [axios](https://axios-http.com/)
- Localization using [react-native-localization](https://github.com/stefalda/ReactNativeLocalization)
- Responsive UI using flexbox and [react-native-size-matters](https://github.com/nirsky/react-native-size-matters)

## Installation Steps

1. Clone the repo

```
git clone https://github.com/twointo2/sample-app-react-native.git
```

2. Install `node_modules`

if using `yarn`:

```
yarn install
```

if using `npm`:

```
npm install
```

3. Install `pods` (if running on MacOS)

An automation script [runPostInstallUninstallTasks](./scripts/runPostInstallUninstallTasks.js) is added into the project which will run after every npm dependency `install` or `uninstall`. Using this, the step 2 will automatically install the pods for iOS if you are using the MacOS. For some reason, if the step 2 will fail to install the pods, then you can mannually install the pods using:

```
cd ios && pod install
```

4. Create ENV files

Hit the following commands in the terminal to create the .env files for the respective environment. `.env.staging` and `.env.production` are added into the `.gitignore` file and will not be pushed to the version control system.

```
echo ENV_TYPE=staging > .env.staging
echo ENV_TYPE=production > .env.production
```

## Running the app

This app is configured for the custom staging and production environments. So, the standard `npm run android` or `npm run ios` commands will not work on this project.
- **To run Android Staging Debug:** `yarn androidStagingDebug` or `npm run androidStagingDebug`
- **To run iOS Staging Debug:** `yarn iosStagingDebug` or `npm run iosStagingDebug`
- **To run Android Production Debug:** `yarn androidStagingDebug` or `npm run androidProductionDebug`
- **To run iOS Production Debug:** `yarn androidStagingDebug` or `npm run iosProductionDebug`
