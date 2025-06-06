# CCRL extensions

The extensions consist of 2 parts:

- A .js script that modifies CCRL live viewer files to query one or more kibitzers and showing/printing their evaluations.
- A .NET backend capable of running those kibitzers locally in the background.

Only one CCRL live viewer tab can be open at a time in the browser for these extensions to work.

This is what it looks like to watch a game with one engine (StockFish 17) as kibitzer with MultiPV set to 3:

![Screenshot of the extension in action, with StockFish 17 acting as kibitzer in a game with MultiPv set to 3](https://github.com/user-attachments/assets/cb9bab38-8852-49a6-903c-8c3d76081c34)

## How to setup

You can find the frontend script and a few pre-compiled binaries (Windows, Linux, macOS) in the [latest release](https://github.com/GediminasMasaitis/CcrlExtensions/releases/latest).

Alternatively, you can always build the backend yourself (.NET 8.0 required) and take the script from the repository ([`src/front/ccrlExtensions.js`](src/front/ccrlExtensions.js))

### Front end

1. Install a usercript runner. Only tested on Firefox and Violentmonkey plugin.
2. Copy [`ccrlExtensions.js`](src/front/ccrlExtensions.js) into a new userscript and save changes.

![Screenshot of Violentmonkey setup](https://github.com/GediminasMasaitis/CcrlExtensions/assets/11148519/13439011-eb74-4004-8ba9-1b5399e248b5)

### Back end

1. Adjust kibitzer path(s) in `appsettings.json` to your local engine(s) path(s).
2. Execute the binary (or build and run the project if you're not using a pre-built one).
