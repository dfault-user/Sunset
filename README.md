# Sunset
A mod for @discord's mobile apps. Forked from Vendetta's recent sunset.

## Installing
Sunset's codebase is platform-agnostic, but you need a platform-specific loader.

### Android
* Root - [SunsetXposed](https://github.com/sunset-mod/VendettaXposed/releases/latest)
* Non-root - [SunsetManager](https://github.com/sunset-mod/VendettaManager/releases/latest)
    - Manager not working? No problem! Pre-built APKs are provided [here](https://discord.k6.tf/).
    - The minimum Android version required is 9. It will not work any lower.

### iOS
* Jailbroken - [SunsetTweak](https://github.com/sunset-mod/VendettaTweak)
    - You can get prebuilt `.deb` files from GitHub Actions - we support rootful and rootless jailbreaks!
* Jailed - You can get IPAs from [the thread](https://discord.com/channels/1015931589865246730/1087295482667208766) in our [Discord server](https://discord.gg/n9QQ4XhhJP) or from our [host](https://discord.k6.tf/ios/).
    - These IPAs do *not* work with AltStore! You should use [Sideloadly](https://sideloadly.io).

## Contributing
1. Install a Vendetta loader with loader config support (any mentioned in the [Installing](#installing) section).

2. Go to Settings > General and enable Developer Settings.

3. Clone the repo:
    ```
    git clone https://github.com/vendetta-mod/Vendetta
    ```

4. Install dependencies:
    ```
    pnpm i
    ```
    <sup>`npm` or `yarn` should also work.</sup>

5. Build Vendetta's code:
    ```
    pnpm build
    ```
    <sup>`npm` or `yarn` should also work.</sup>

6. In the newly created `dist` directory, run a HTTP server. I recommend [http-server](https://www.npmjs.com/package/http-server).

7. Go to Settings > Developer enabled earlier). Enable `Load from custom url` and input the IP address and port of the server (e.g.  e.g. `http://192.168.1.236:4040`) in the new input box labelled `VENDETTA URL`.

8. Restart Discord. Upon reload, you should notice that your device will download Vendetta's bundled code from your server, rather than GitHub.

9. Make your changes, rebuild, reload, go wild!
