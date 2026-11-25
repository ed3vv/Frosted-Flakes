#           ❄︎ Frosted Flakes ❄︎

NOTE: This is a forked version of https://github.com/yike-shi/WINTER_IS_COMING

Let it snow on your Mac! ☃️

Snow falls on your desktop and piles up on your windows and Dock. Roll it into snowballs and build a little snowman. It's all one Swift file, and every flake is drawn in code.

<!-- ![demo](docs/demo.gif) -->

## What it can do ✨

- **Cozy snowfall**: three layers of flakes (near, middle and far) drifting in a gentle wind
- **Snow piles up** on top of your windows, along the Dock and at the bottom of the screen
- **Drag a window and *whoosh*!** The snow flies off. The faster you drag, the farther it goes
- **Roll snowballs** just by moving your mouse sideways over the snow (no clicking!). They grow as they roll
- **Snowballs push each other** along, and one that's pushed off the edge falls down
- **Hold a snowball** with the left mouse button and carry it anywhere
- **Stack three snowballs** and they turn into a snowman with a carrot nose and a red scarf
- **A falling snowball goes *poof*** into a soft heap of snow, ready to be rolled again
- **Fairy lights**: colorful twinkling lights that swing into place along the top of your windows. They're off by default, so turn them on from the ❄︎ menu (or press `L`)

## How to play 🎮

- **Roll a snowball**: slide your mouse sideways over snow on a window, the Dock or the ground
- **Push it**: roll one snowball into another and it gets shoved along
- **Carry it**: hold the left mouse button on a snowball and drag
- **Build a snowman**: stack three snowballs on top of each other ⛄
- **Make it fly**: drag a window and watch the snow whoosh off
- **Hang the lights**: ❄︎ menu → **Fairy Lights** ✨
- **Forgot something?** ❄︎ menu → **How to Play**

## Download 🎁

1. Grab `FrostedFlakes-mac-vX.zip` from [Releases](https://github.com/ed3vv/Frosted_Flakes/releases/latest) (not the "Source code" ones)
2. Unzip it and drag **FrostedFlakes** into your Applications folder
3. Double-click it. The first time, macOS will say it can't open the app. Click **Done**, then go to **System Settings → Privacy & Security**, scroll down and click **Open Anyway**. You only need to do this once ✨

> 🙏 **Why does macOS block it?** This is an early version, and it isn't signed with a paid Apple Developer account yet, so macOS doesn't recognize it. It's not a virus, promise! The app never connects to the internet, and all the code is right here for you to read. Thanks for your patience while I work on it 💙

## Build it yourself 🛠️

```sh
git clone https://github.com/ed3vv/Frosted_Flakes.git
cd Frosted_Flakes
zsh build.sh
```

Use the ❄︎ in the menu bar to pause, pick light, medium, heavy, or snowstorm, switch the fairy lights on, clear the snow, or quit.

- No `swiftc`? Run `xcode-select --install` first.
- Want snow on the Dock too? Turn on **FrostedFlakes** (or **Terminal**, if you run it with `build.sh`) in System Settings → Privacy & Security → Accessibility.
- Want your own `.app`? Run `zsh make_app.sh 1.0`.

## Windows version 🪟 (beta)

You asked for it, so here it is! Snow falls on your Windows desktop and piles up on your windows and the taskbar, and dragging a window still sends it flying. Snowballs and snowmen are coming soon ⛄

```sh
cd Frosted_Flakes/windows
dotnet run -c Release
```

Use the ❄ icon in the system tray to pause, pick the snow amount, clear the snow, or quit. You'll need the [.NET 8 SDK](https://dotnet.microsoft.com/download) (`winget install Microsoft.DotNet.SDK.8`).

## Make it yours 🎨

Every setting lives at the top of `FrostedFlakes.swift` (`enum Cfg`): how many flakes fall, how fast they fall, how tall the piles get, how big a snowball can grow… Change a number and run `zsh build.sh` again.

## License

[MIT](LICENSE) · Made with 💙 and a little help from Claude

## CHANGES FROM ORIGINAL REPO:

v1.1 (19 Nov)
- Hides snowflakes behind windows.
- Fixed UI glitch where snowflakes were spawning/immediately despawning in fullscreen
- Multi monitor support (does not yet support snow transferring monitors)
- Constant snowfall rate (Used to be dependent on window size)

v1.2 (20 Nov)
- Decreased snowfall accumulation rate 70%
- new snowstorm snow amount
- rebalanced snow falling rates (12, 24, 48, 96)
- fixed points <-> discrepancy on different resolutions
- removed snow landing on docks
- Rounded corners for windows

v1.3 (24 Nov)
- Added option for snow to fall in front of window.
- replaced preset snow amounts with a slider

## CHANGES LATER:
- Instead of deleting snow behind windows simply hide them
- Prevent snowflakes from appearing in front of window near edges
- make window interactions with snow more clean
- Fix rounded edges
- Add idle snow falling
- fix diff desktop