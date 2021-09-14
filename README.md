# playjs-expo-template

An Expo development environment optimized specifically for usage in a local play.js sandbox.

A few caveats:

- Extra dev dependencies to make up for the lack of global Expo modules.
- Tunnel connection is not supported.
  - @expo/ngrok package simply prevents DevTools from error in when selecting the tunnel option.
- Expo Go app is not supported.
  - Test your app in the play.js browser by selecting `Run in web browser` in DevTools or by running the `web` script (a local URL will be produced).