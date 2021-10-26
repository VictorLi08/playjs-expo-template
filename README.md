# playjs-expo-template

An Expo development environment optimized specifically for usage in a local play.js sandbox.

Check out play.js for iOS by [clicking here](https://apps.apple.com/us/app/play-js-javascript-ide/id1423330822).

Features:

- Formatting script due to the lack of watch capabilities in play.js sandboxes.
- Preset Expo CLI scripts for login and publish.
  - You will need to replace `<YOUR_USERNAME>` and `<YOUR_PASSWORD>` in the `package.json` login script with your Expo login credentials.
    - **:warning: DANGER: You will only need to log in to Expo once. Always discard your changes to the login script immediately after running it in order to ensure the safety of your credentials.**
  - You may need to customize the publish script to your workflow's needs.
  - View the [Expo CLI documentation](https://docs.expo.dev/workflow/expo-cli/) for more on CLI commands.

A few caveats:

- Some scripts don't stop on their own.
- Extra dev dependencies added to make up for the lack of global module support in play.js
- Tunneling is not supported.
  - `@expo/ngrok` package simply prevents DevTools from producing an error in when selecting the tunnel option.
- Expo Go app is not directly supported.
  - QR code generates but is not usable (scans but Expo Go can't open it properly).
  - The only way to run within Expo Go is to publish the project to Expo and then open it from the `Profile` menu.
- Simulators are not supported.
  - The only way of testing the app with hot reloading is to select `Run in web browser` in DevTools or by running the dev command with the `--web` flag (baked into the `dev` script in this template). Expo Web is typically hosted at http://localhost:19006.
