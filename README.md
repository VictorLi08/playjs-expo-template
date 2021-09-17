# playjs-expo-template

An Expo development environment optimized specifically for usage in a local play.js sandbox.

Check out play.js for iOS by [clicking here](https://apps.apple.com/us/app/play-js-javascript-ide/id1423330822).

Features:

- Formatting script due to the lack of watch capabilities in play.js sandboxes.
- Preset Expo CLI scripts for login and publish.
  - You will need to replace `<YOUR_USERNAME>` and `<YOUR_PASSWORD>` in the `package.json` login script with your Expo login credentials. 
    - __:warning: DANGER: You will only need to log in to Expo once. Always discard your changes to the login script immediately after running it in order to ensure the safety of your credentials.__
  - You may need to customize the publish script to your workflow's needs.
  - View the [Expo CLI documentation](https://docs.expo.dev/workflow/expo-cli/) for more on CLI commands.

A few caveats:

- Some scripts don't stop on their own.
- Extra dev dependencies added to make up for the lack of global module support in play.js
- Tunneling is not supported.
  - `@expo/ngrok` package simply prevents DevTools from producing an error in when selecting the tunnel option.
- Expo Go app is not supported.
  - QR code generates but is not usable (scans but Expo Go can't open it properly).
  - You can only test your app in the play.js browser by selecting `Run in web browser` in DevTools or by running the `web` script.