## Contributing

Thanks for your interest in contributing! Doing so is simple. Just [edit this page](../../edit/master/README.md) and submit a pull request (PR) with your changes.
Someone will review it and merge it in as soon as possible.

When editing the Markdown, please keep these rules in mind:

1. Do not link to any APKs.
2. Double-check your spelling/grammar.

## Legend

This page currently uses Unicode characters from [Unicode Emoji (1.0)](https://unicode.org/Public/emoji/1.0/emoji-data.txt). If you are unable to see these characters, please open an issue.

- ✅ Works
- 🆖 Works, but needs Google Mobile Services
- ⚠️ Works, but with some notable problems
- ❌ Broken

## Support table (OS features)

| Feature | Support level | Notes |
|---------|---------------|-------|
| Multi-touch | ✅ | Demo: [Arcaea](https://www.bilibili.com/video/BV1Ph411n7M5)
| Virtual Wifi (VirtWifi) | ✅
| Fingerprint Reader | ❌ | Test failed on ROG Flow X13, with SATRIA app
| VPN | ❌ | VPN Connection request dialog does not appear
| OpenGL ES 3.1 | ❌
| Vulkan | ❌

### Workarounds

#### VPN

There is no `com.android.vpndialogs` in WSA. However, it's possible to manually grant the VPN activation permission with AppOps via `adb shell`:

```shell
appops set [package name] ACTIVATE_VPN allow
```

#### Launching Android Apps with URI scheme

Microsoft provides a custom URI scheme for WSA, making it easier to launch apps:

```shell
wsa://[App Package Name]
```

For example, to launch Apple Music in WSA, use:

```shell
wsa://com.apple.android.music
```

Some URIs are not supported in WSA, such as:

```shell
wsa://com.android.settings
```

## Support table (applications)

| Application | Latest tested version | Support level | Known Issues | Notes |
|-------------|-----------------------|---------------|--------------|-------|
| 23andMe | 5.114.0 | ✅
| 4PDA | 1.9.35 | ✅
| 8 ball pool | 5.5.6 | ✅
| A Dance of Fire and Ice | 1.15.5 | ✅ || Keyboard supported
| A+ Gallery | 2.2.55.4 | ✅ | You might face graphical glitches when using dark theme, hence its recommended to use light theme instead.
| ADM | 12.5.4 | ✅
| ADM Pro | 6.4.0 | ✅
| Aegis | 2.0.2 | ✅
| AFK Arena | 1.72.01 | ⚠️ | Can't login using Google account
| AIDE | 3.2.210316 | ✅ || Might optionally require GMS
| AIMP | 3.10.1052 | ✅
| Alan Walker-The Aviation Game | 3.0.6 | ✅ || Touchscreen and cursor works; keyboard doesn't work
| Alien: Blackout | 2.0 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS
| Alto's Adventure | 1.8.0 | ✅
| Alto's Odyssey | 1.0.10 | ✅
| Amaze File Manager | 3.5.3 | ✅ || Avoid updating the app
| Among Us | 2022.3.29 | ✅ | Keyboard may be unresponsive. | Xbox controller works.
| Angry Birds Epic | 3.0.27463.4821 | ⚠️ | Terrible in-game experience, bad performance and low FPS
| AniLabX | 3.8.12 (Iridium) - Beta | ✅
| AntennaPod | 2.5.0 | ✅
| APKMirror Installer (Beta) | 1.3.2 | ⚠️ | Cannot remove ads without subscription which requires Location to be turned on. Apart from this, there are random crashes
| APKPure | 3.17.26 | ✅ | Sometimes, it might require multiple attempts to install an app
| Apple Music | 3.7.1 | ✅
| App分享 (AppShare) | 2.1.1 (164) | ❌ | Can't login
| Aptoide App Store | 9.20.2.1 | ✅ | Sometimes, downloads might get stuck
| AquaMail (Pro) | 1.34.0-118 | ✅
| Arcaea | 3.8.8 | ⚠️ | Keyboard doesn't work on login/register form
| Arknights | 5.0.01 | 🆖 | Can't login using Google account. Unstable FPS throught the game, especially low FPS in combat for AMD system PC
| Asphalt 9 || ⚠️ | Keyboard unsupported
| Audible | 3.15.0 | ✅
| Aurora Store | 4.0.7 | ✅
| Authy | 24.8.5 (139) | ✅ || Produces warnings about GMS which are safe to ignore.
| Azur Lane | 6.0.820 | ⚠️ | Some characters may appear missing and the game can get stuck while in combat, this can be fixed by restarting the app.
| Bad Piggies HD | 2.4.3141 | ✅
| BanG Dream! Girls Band Party! | 4.5.0 | 🆖 | Requires GMS
| Battle Cats Quest | 1.0.4 | ✅
| BBC iPlayer | 4.137.0.25403 | ✅ | Sideloaded
| Berry Browser | 3.55.18 | ✅
| Binance | 2.36.5 | ✅
| Blue Archive (GB) | 1.36.120365 | ❌ | Black screen on app launch
| Blue Archive (KR) | 1.35.115378 | ❌ | Blank screen on app launch
| Bouncer | 1.26.3 | ⚠️
| Brave Browser | 1.30.87 | ✅
| Brawl Stars | 38.159 | ❌ | Game crashes
| BritBox by BBC & ITV | 2.1.2 (20043) | ❌ | App crashes on start
| Bromite | 94.0.4606.94 | ✅ || Use x64 build
| C.A.T.S (Crash Arena Turbo Stars) | 2.40.2 | ✅ | GMS warnings might appear but these can be safely ignored
| CamScanner | 6.3.0.2110240000 | ❌ | WSA freezes after taking a snap
| Candy Crush Saga | 1.213.2.1 (12132011) | ✅
| Canvas Student | 6.14.1 | ✅
| CarX Highway Racing | 1.17.1 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS
| ChMate | 0.8.10.153 | ✅
| Clash Mini | 1.1142.10 | ❌ | App crashes
| Clash of Clans | 14.211.3 | ❌ | App crashes
| Clash Royale | 3.6.1 | ❌ | App crashes
| Clouds & Sheep 2 | 1.4.6 | ✅ | Optionally uses GMS
| Clubhouse | 1.0.11 | ⚠️ | Unable to login via phone number, it throws error after entering the OTP
| Comixology | 3.10.18.310421 | ✅
| CnC Rivals | 1.8.1 | ✅ | | It will pop up "Won't run without GPlay services" when starts, but works fine except GPlay login. You may use link email instead.
| CPU-Z | 1.41 | ✅
| Cronometer | 3.13.1 | ✅
| Dcoder | 4.0.76 | ✅
| Decibel X | 6.4.2 | ⚠️ | App crashes
| Delivery Club | 4.64.0 | ❌ | App crashes after selecting a shipping address
| Deus Ex GO | 2.1.111374 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS
| Destiny Child | 2.8.6 | ⚠️ | Poor performance during battles
| DevCheck | 3.39 | ❌ | Blank screen on startup
| Device Info HW | 5.4.1 | ✅
| DirecTV for Tablet | 5.29.001 | ⚠️ || Frequent crashing, other functionality proper.
| Discord | 98.6 | ✅
| DMM Games Store | 2.8.0 | 🆖 | Requires GMS
| Duolingo | 5.2.35 | ✅
| Dwarf Balls | 3.5.2 | 🆖 | Requires GMS for Google Play login.
| Easybell | 2.1.30 | ✅
| Emby | 2.0.48g | ✅
| Epic Seven | 1.0.406 | ⚠️ | Low FPS, unable to sign in with Google
| ES File Explorer | 4.2.1.8 | ✅ || Avoid updating the app
| Excel | 16.0.14527.20162 | ✅
| F-Droid | 1.13.1 | ✅
| F1 TV| 2.0.5 | ⚠️ | Terrible app experience including screen flashes and crashes while watching a video
| FaceApp: Face Editor || ❌
| Facebook Messenger | 330.0.0.12.116 (x86_64) | ⚠️ | Chat Heads don't work
| Fancade | 1.7.6 | ❌ | App crashes
| FAST Speed Test | 1.0.8 (88) | ✅
| Fate/Grand Order (US) FGO | 2.22.1 (135) | ✅ || A little unstable, but playable
| Fire Emblem Heroes | 6.0.0 | 🆖 | Requires GMS. If GMS is installed, it cannot be played due to SafetyNet error.
| Firefox | 93.2.0 (2015839751) | ✅
| Firefox Nightly | 95.0a1 | ✅
| foobar2000 | 1.2.30 | ✅
| Formula 1 | 11.0.1533 | ⚠️ | Live Timing is broken, keeps crashing on initialization
| Fortnite | 14.10.0 | ❌ | Crashes at login screen
| Fortnite Installer | 4.1.4 | ❌ | "Device not supported" error
| Fruit Ninja | 3.3.4 | ✅ | Version check error | Otherwise, other app functionality is fine
| FTP Server (Free) (F-Droid) | 3.1 - 30100 (11-30) | ✅
| FX File Explorer | 8.0.3.0 (r8008) | ✅ | Tested only on the base version (without FX Plus)
| Game Dev Story | 2.47 | ❌ | App can start but with infinite "loading" screen
| Game Pass | 2110.17.1005 | ✅ | GMS warnings might appear but these can be safely ignored | Cloud games can be launched but controlling them with controller or touch has not been tested.
| Garage: Bad Dream Adventure | 1.0.191 | ⚠️ | Stuck after start of Chapter 1
| GCash | 5.51.0 | 🆖 | Requires GMS. Will warn "limited functionality" if no GMS is present, if present, works normally. 
| Geekbench |5.4.1| ✅
| GeoGebra | 5.0.674.0 | ✅
| Geometry Dash | 2.11 | ✅ | If you use high refresh rate monitor, there is a small period where the game speeds up before the level plays for the first time and the audio will get desynced. You can simply pause and resume or die once to fix it since it won't happen on second attempt.
| Girls' Frontline (EN) | 2.0702_362 (362) | ⚠️ || Game freezes after splash screen, works after installing WSL2, using `wsl --install`
| Globe2Go | 4.7.4.20.0810/3890 | ✅
| Gmail | 2022.03.06.437126241.Release | ✅ || May require GMS
| Gojek | 4.30.1 | 🆖 | Requires GMS
| Golf Rival | 2.54.241 (88) | 🆖 | Requires GMS | Produces warnings about GMS. Issues include not being able to pan.
| Google Chrome | 94.0.4606.85 | ✅ | Requires microG or GMS
| Google Classroom | 8.0.061.20.90.3 | ✅ || Notifications are generic (do not show content), clicking on them may not open the app. Uploading of attachments locally is not possible.
| Google Drive | 2.22.117.3.all.alldpi | ✅ | Works fine, may require GMS
| Google Meet | 2021.10.03.404303734.Release | 🆖 | Requires GMS, Share screen doesn't work due to WSA's windowed nature
| Grab | 5.172.200 from Huawei AppGallery | ✅
| Grand Theft Auto: San Andreas || ✅
| Guardian Tales | 2.23.2 | 🆖 | Requires GMS
| Hay Day | 1.53.46(1700) | 🆖 | Account synchronization requires GMS, but it can be bypassed with Supercell ID
| HBO Max | 52.15.0.53 | ⚠️ | Failed to play video (internal player fails to display image and play sound).
| Hill Climb Racing | 1.53.0 (501) | ✅
| Hitman Sniper | 1.7.193827 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS
| Hobi | 2.1.7 | 🆖 | Requires GMS
| Home Assistant | 2022.3.0-full | ✅ | Basic functionality works, additional / extended functionality has not been yet tested.
| Honkai Impact 3rd| 5.1.0 | ⚠️ | Poor graphics quality
| Housesigma Canada Real Estate| 4.3.6 (121) | ✅
| HTV (hanime tv) | 3.6.7 | ⚠️ | Failed to play video | Internal player don't work, asks for external player and fails again
| huaCtrl PRO | 1.0.27 | ✅
| Huawei AppGallery | 11.4.2.300 | ✅ | Frequent crashes were experienced, otherwise the app functionality is fine
| Hungry Shark Evolution || ✅
| Hyper Square | 3.0.1 | ✅
| iDOLM@STER Million Live! Theater Days | 4.0.401 | ⚠️ | Anything 3D with a moving background is broken, but everything 2D works perfectly | ARMv7 version is unusably slow, get ARM64
| Instagram | 234.0.0.0.108 | ⚠️ || Need to use an Android keyboard (eg. MS SwiftKey) to be able to reply stories
| iOS app (any) || ❌ | Thanks for testing, Brad.
| iPusnas | 1.5.1 | ✅
| JAKI - Jakarta Kini | 1.2.34 | 🆖 | Some features require GMS
| Jet Car Stunts 2 | 1.0.13 | ❌ | Loads up but orientation and menus are broken
| Jetpack Joyride | 1.52.1 (58461800) | ⚠️ | Google Play Games sync doesn't work, otherwise the game functionality is fine
| JioSaavn | 8.2.1 | ✅ |Doesn't support fullscreen and rare crashes but running fine
| Joey (Reddit client) | 2.0.0.1 | ✅
| Joplin | 2.4.3 (2097651) | ✅
| JuiceSSH | 3.2.2 | ⚠️ | Connecting to SSH server needs multiple tries
| Kahoot || ✅
| Khan Academy | 7.3.3 | ✅
| Kik | 7.10.1.176 (82) | ✅
| Kindle | 8.47.1.3370 | ✅
| KINGDOM HEARTS Uχ Dark Road | 4.4.0 (Offline) | ✅ | GMS warnings might appear but these can be safely ignored
| Kobo Books | 8.40.29843 | ⚠️ | Aspect ratio and resolution are fixed, appears blurry when resized
| Konosuba:FD | 1.12.1 | 🆖 | Requires GMS
| KRL Access | 4.1.0 | ❌ | App crashes
| Last Day On Earth: Survival || 🆖 | Might require GMS
| Lawnchair | 11.0 Alpha 6.1 (8b01af8).release | ❌ | App crashes
| Lawnchair | 12 Alpha 5 | ✅
| League of Legends: Wild Rift || ✅
| Libby | 4.3.1 | ✅
| LIMBO Demo | 1.20 | ✅
| LINE | 12.0.1 | ✅
| Line Rangers | 7.6.3 | ✅
| LinkedIn | 4.1.632 | ✅
| LSPosed | 1.8.0 | ✅
| Magic Tiles 3 | 8.086.201 | ✅
| Magisk | Internal build? | ✅ || Magisk developer confirmed able to gain root access - [link to his tweet](https://twitter.com/topjohnwu/status/1451282578514735131)
| ManCityApp | 2.1.11 | 🆖 || Might require GMS
| Manzur's Study Circle (MSC) | 1.0.2 | ✅
| MapleStory M | 1.7000.2835 | ❌ |Crashes at loading screen
| Mario Kart Tour | 2.10.0 | ❌ | Fails to connect to servers after Nintendo login
| Material Files | 1.3.1 | ✅
| microG Settings | from NanoDroid and MinMicroG | ❌ | App crashes, doesn't load
| Microsoft Authenticator | 6.2112.8213 | ✅ || Some features might require GMS
| Microsoft Azure | 3.9.2.2021.09.30-19.35.50 | ✅
| Microsoft Edge | 95.0.1020.42 | ❌ | App frequently crashes
| Microsoft Launcher | 6.210602.1.994630 | ✅
| Microsoft PowerApps | 3.21124.20 | ✅
| Microsoft Swiftkey Keyboard | 8.10.12.4 | ✅
| Minecraft (Aurora Store) | 1.17.40.06 | ❌ | Unable to verify game owner
| Minecraft (China Edition) || ✅
| Minecraft (Play Store) | 1.18.0.23 | ✅
| MiX | 6.57.0-Beta_B21070510 | ✅
| Mobile JKN | 3.7.1 | ✅ || Some features might require GMS
| Mobile Legends | 1.6.66.7281 | ✅
| MOLA | 2.1.3 | ❌ | App crashes
| Monument Valley | 2.7.17 | ✅
| Monument Valley 2 | 2.0.3 | ✅
| Moodle | 3.9.5 | ✅
| Mortal Kombat X(APKPure) | 5.9.0 | ❌ | Stuck on initialization screen, message shows up saying "Download failed to start"
| MT File Manager | 2.10.0 | ✅
| Musically (TikTok) | 7.8.0 | ✅
| Muslim Pro | 1.2.3 | 🆖 | Requires GMS
| MX Player | 1.40.9 | ✅
| MX Player Pro | 1.39.13 | ⚠️ | App crashes, but videos can be played from external sources
| My Verizon | 16.4.2 | ✅ || The page might be displayed sideways for a short amount of time when the app is launched. The app automatically reverts to correct orientation in a second.
| Neko | 2.6.2 | ✅
| Nekogram X | 8.1.2-1-rc01 | ✅ || Use NoGcm variant
| Netflix (Aurora Store) | 8.4.0 | ❌ | "Device not supported" error
| Network IP Scanner | 3.2 | ⚠️ | Only scans WSA's own VirtWifi network
| NewPipe | 0.22.1 | ✅
| NFL | 56.1.7 | ❌ | App crashes
| NieR Re[in]carnation | 1.7.1 | ❌ | Unable to get past the loading screen
| Nova Launcher | 7.0.49 (7049) | ⚠️ | UI is messy, but app drawer is fine
| Nu Carnival | 1.0.2-erolabs | ❌ | App stuck on a black screen
| Office | 16.0.14527.20162 | ✅ || Might require microG
| Office Lens | 16.0.14527.20178 | ❌ | Might require GMS, cannot sign in
| Okay? | 4.08 | ✅
| One Store | 7.6.0 | ✅
| Opera Browser Beta | 65.1.3381.61349 (x86_64) | ✅ || Change app layout to Tablet Mode for a better experience
| Opera GX : Gaming Browser | 1.3.6 | ✅
| Opera Mini Beta | 61.0.2254.59921 | 🆖 | Requires GMS
| Opera Touch Browser | 2.9.6 | ⚠️ | My Flow feature requires GMS | GMS warnings might appear but these can be safely ignored
| Oppo App Store (China) | 8.6.4 Beta 1 | ❌ | App freezes on blank screen
| Oppo Game Center (China) | 9.7.0_14b2c0c_210521 | ✅
| Oreo: Twist, Lick, Dunk | 1.5.6 | ✅ | Minor graphical glitches
| OsmAnd~ | 3.9.10 | ✅
| Oto Music | 3.0.2 | ✅ || Requires app restart to refresh list
| OurGroceries | 4.0.10 | ✅ | Premium keys require Google Play Store
| Outlook | 4.2138.0 | ⚠️ | Cannot activate device administrator with Outlook, which prevents activation.
| Phigros || ✅
| Pixel People | 4.7 | ✅ | Changing window size breaks the game. Runs at low FPS but is still playable.
| Plants vs Zombies 2 | 9.2.2 | ✅ | Cloud save using Google Play Games works if GMS is available
| Playstation App | 21.11.2 | ⚠️ | Runs very slow and takes some time to connect to voice chat, beside that it works  
| Plex | 8.26.2.29389 | ✅
| Plex Dash | 1.1.1 | ❌ | App crashes after splash screen
| Plexamp | 3.8.2 | ⚠️ | Layout and app orientation issues
| Pocket | 7.56.0.0 | ⚠️ | Unable to log in with a Firefox account, instant (push) syncing is unavailable
| Pokémon GO || ❌ | Unable to authenticate
| Pokémon Masters EX | 2.19.0 | ❌ | 10102 An error has occured.
| Pokémon Unite | 1.2.1.2 | ⚠️ | Battle experience is terrible
| PornHub || ✅
| Pou | 1.4.84 | ✅
| PowerPoint | 16.0.14527.20162 | ✅ | Might require GMS / MicroG
| Prep Ladder | 2.0.79-p | ⚠️ | Video pane opens but no audio or video and time keeps on going
| Princess Connect! Re: Dive (Traditional Chinese) | 2.9.0 | ⚠️ | Battle experience is terrible, cannot sync with Google Play Games
| Pydroid | 5.00_x86_64 | ✅
| Q-Dance | 8.0.7 | ❌ | App crashes
| QooApp | 8.3.3 | ✅
| QPython 3L | 3.0.0 | ✅
| QQ | 8.2.11 | ✅
| Rayman Classic | 1.0.1 | ✅
| Real Racing 3 | 10.1.0 | ✅ | Only controller is supported. keyboard doesn't work
| Reddit || ✅
| Relay | 10.0.378 | ✅
| Remini - AI Photo Enhancer || ⚠️ | Oops! Something went wrong Your image didn't save. Please try again.
| Remote Desktop (Microsoft) | 10.0.12.1148 | ✅
| Rider | 1.59 | ✅
| Roblox | 2.499.381 | ⚠️ | Graphical anomalies | GMS warnings might appear but these can be safely ignored
| Rocket League Sideswipe | 1.0 (356721) | ❌ | OpenGL ES 3.1 is unsupported
| Rootless Launcher | 3.9.1 | ❌ | App crashes
| SATRIA | 1.0.0 | ❌ | Needs fingerprint reader support
| SD Maid (pro) | 5.2.2 | ⚠️ | Unable to grant external storage privileges, can be skipped
| Shadow Fight 2 | 2.16.0 | ⚠️ | Optionally uses GMS, Doesn't support keyboard control makes fighting more harder | GMS warnings might appear but these can be safely ignored, Cloud save requires GMS
| Shadow Fight 3 | 1.25.7 | ✅ | Optionally uses GMS, Cloud save using Facebook not working | Keyboard control are supported uses (W A D X) to use analog, GMS warnings might appear but these can be safely ignored, Cloud save requires GMS
| ShemarooMe | 1.0.16 (106) | ✅
| Shizuku | 12.3.0.r668.5687d0c | ✅ | Works well with Wireless debugging
| Shopee PH | 2.86.09 | ⚠️ | App works but cannot login
| Showtime | 3.1.1 | ❌ | App crashes when you try to login. Button clicks dont work
| Simple Gallery | 5.3.9 | ❌ | App crashes when you try to view a photo
| Sky Map | 1.10.0 - RC3 | 🆖 | Complains about missing accelerometer controls, requires GMS
| Sky: Children of the Light | 0.15.1 | ❌ | OpenGL ES 3.1, Vulkan 1.0.3 and Vulkan level 0 missing
| SkySafari | 6.8.6.15 | 🆖 | Failed license check on startup, appears to require GMS
| Slack | 21.11.20.0-B | ✅
| Smart Launcher | 5.5 Build 052 | ✅
| Smart Life | 3.32.5 | ❌ | The app is producing constant flashes between light and dark mode, and the UI element of agreement pop-up is moving on screen so it can't be accepted
| Smash Hit | 1.4.3 | ✅
| Snapchat || ⚠️ | Camera view is flipped | GMS warnings might appear but these can be safely ignored
| Solid Explorer File Manager | 2.8.16 | ❌ | App crashes
| Speedtest by Ookla | 4.6.10 (145526) | ⚠️ | VPN does not work
| Spotify | 8.7.20.1261 | ✅ | 
| Spotify Lite | 1.9.0.2883 | ✅
| Squircle IDE | v2022.1.0 | ✅
| Standoff 2 | 0.16.6 | ⚠️ | Battle experience is terrible, includes micro-stutters
| Stardew Valley | 1.4.5.151 | ✅
| State of Survival | 1.13.40 | ✅
| Steam | 2.3.13 | ✅
| Steam Chat | 1.0 | ✅
| Steam Link | 1.1.81 | ❌ | App crashes
| Stickman Hook | 7.2.8 | ❌ | Game fails to initialize
| Subway Surfers | 2.24.2 | ✅ | Doesn't support keyboard control
| SwiFTP Server| 1.24 | ✅
| Sword Art Online: Integral Factor| 1.9.2 | ✅ | Keyboard unsupported
| Sword Art Online: Memory Defrag | 3.0.2 | ✅ | Keyboard unsupported
| Sword Art Online: Unleash Blading | 3.2.0 | ⚠️ | Can't detect device
| Symbolab | 9.3.0 | ✅ || Keyboard not working, in-app keyboard is available though
| Sync for Reddit Pro | 20.0.3 | ✅
| Tachiyomi | 0.13.4 | ✅
| Teamfight Tactics | 12.5.4259171 | ⚠️ | Crashes often before getting in game but after getting in, not many issues. Can get laggy at times but somewhat playable.
| TeamViewer | 15.22.136 | ✅
| Telegram | 8.1.2 | ✅
| Termux | 0.117 | ⚠️ | `packages.termux.org` mirror is the only one that works
| Terraria | 1.4.3.2.2 | ✅ || Keyboard supported
| Tesla | 4.6.1 | ⚠️ | Vehicle graphics and maps do not load, cannot enable phone key. | Internet-based vehicle controls, charge stats, services are functional.
| The Battle Cats | 11.2.1 | ✅
| The Battle of Polytopia | 2.0.59.5719 | ❌ | Validation error
| The Globe and Mail | 6.2.0 (100) | ✅
| The King Of Fighters Allstar | 1.9.3 | ✅ | Blank screen / app crash on first boot, works on second boot upwards
| This War of Mine | 1.0 | ❌ | Infinite loop at start-up screen
| TIDAL | 2.49.0 | ✅
| TikTok (China) | 18.1.0 | ⚠️ | App crashes on first startup and you might face hiccups logging in
| TikTok (Global) | 24.0.3 | ✅
| TikTok (TV Version) | 1.6.0 | ❌ | App crashes
| TikTok Lite | 21.7.1 | ❌ | App crashes
| TP-Link Tapo | 2.4.25 | ✅
| Trello | 2021.14.1.16332-production | ⚠️ | Login needs web browser installed in WSA, using Windows' default browser will not work
| True Skate | 1.5.39 | ✅ | Minor graphical glitches
| Tune In Pro | 28.7 (267721) | ✅
| Twitter | 9.16.1-release.00 | ✅ | Optionally requires GMS
| UC Browser | 13.0.0.1288 (x86) | ✅ || Avoid updating the app
| Uptodown App Store | 4.35 | ⚠️ | Keeps "analyzing device" on app details page, thus its unable to download APKs.
| Vanced Manager | 2.6.2 (Crimson) | ✅
| Vanced MicroG | 0.2.22.212658 | ⚠️ | microG Google sign-in method does not work, hence use Huawei sign-in method to sign in to Google account
| Via Browser | 4.3.1 | ✅
| Vidio | 5.64.5-f0aa483a3d | 🆖 || Might require GMS for login
| Vivaldi Browser | 4.3.2439.61 | ✅
| VK | 6.58 | ✅
| VLC | 3.4.0 | ✅
| VSCO | 264 | ⚠️ | Cannot sign in
| War Robots | 7.7.7 (134783) | ✅ | GMS warnings might appear but these can be safely ignored
| Warden | 1.0.3.release | ⚠️ | App screen flashes otherwise functionality-wise its normal
| Warfare Incorporated | 1.63 | ✅ | The selection box does not work.
| Wealthsimple Trade | 2.27.1 (2195) | ✅
| WhatsApp | 2.21.20.20 | ⚠️ | WhatsApp cloud chat backups will not work, app was tested with microG installed
| Where is my Water? || ⚠️ | Many images are replaced with white rectangles
| Where is my Water? 2 || ⚠️ | Most images are replaced with white rectangles, Vignette overlay is full white and covered the whole playing area. The ground is not textured correctly.
| Where is my Water? Featuring XYY || ⚠️ | Bells are invisible
| Word | 16.0.14430.20246 | ✅ || Might require microG
| Wordament | 3.9.10260 | ✅
| Wulkanowy (F-Droid) | 1.4.3 | ✅
| Wulkanowy (Play Store) | 1.4.3 | 🆖
| Wyze | 2.30.0 | ✅
| XBrowser | 3.7.7 | ✅
| xManager | 3.3 | ✅
| X-plore File Manager | 4.27.10 | ✅
| Yahoo! Fantasy Sports | 10.31.0 | ❌ | App crashes on launch
| Yandex.Maps | 10.6.0 | ⚠️ | Map doesn't work
| Ymusic | 3.7.2 | ✅
| YouTube (Google)| 16.40.35 | 🆖 | Requires GMS
| YouTube Music (Google) | 4.49.51 | 🆖 | Requires GMS
| YouTube Music Vanced | 43.9.50 | ✅
| Youtube Vanced | 16.29.39 | ⚠️ | Picture-in-picture doesn't work & Can't join channel membership
| ZArchiver | 0.9.5.8 (9596) | ✅
| Zenly (w/o GMS) | 4.55.2 | ⚠️ | App crashes after login, but background location works
| Zoom | 5.8.3.2634 | ⚠️ | Camera severely glitched, share screen doesn't work due to WSA's windowed nature.
| 白夜極光 (Alchemy Stars) | 1.2.2 | ⚠️ | Poor in-game performance
| 明日方舟 (Arknights Simplified Chinese) | 1.6.01 | ✅
| 哔哩哔哩 (Bilibili) || ✅
| 酷安 (CoolApk) | 11.4.3 | ⚠️ | Unable to sign in using third party apps
| 创建快捷方式 (Create Shortcut) | 1.17 | ✅ || Can be used to access any app
| Дурак Онлайн (Durak Online) | 1.9.2 | 🆖 | Requires GMS
| মুনাজাতে মাকবূল ও মাসনূন দু'আ - Munajate Makbul | 1.0 | ✅
| ウマ娘 プリティーダービー | 1.16.0 | ⚠️ | Doesn't work with GTX1660. Works with Microsoft Basic Render Driver with graphical issues. | Some features may require GMS.
| 九黎 | 1.3.5.01 | ❌ | App crashes
| 公主连结R (Princess Connect! Re: Dive (Simplified Chinese) | 3.4.10 | ✅
| 云·原神 (Genshin Impact (Cloud app) )|| ✅
| 原神（Genshin Impact） | 2.2.0 | ⚠️ | Working but heavy graphical glitches - [video](https://www.bilibili.com/video/BV1zT4y1o73D?)
| 崩坏学园2 (Honkai Gakuen 2)| 8.5 | ✅ || Game has inbox keyboard controller for WASD
| 米游社 (mihoyo Chinese Community) | 2.14.1 | ⚠️ | The app might lag when inserting a photo into a new post
| 東方LostWord | 1.16.0 | ❌
| 战双帕弥什 (Punishing: Gray Raven) || ✅ || Keyboard is supported
| СберБанк (SberBank) | 12.9.0 | ✅
| Тинькофф (Tinkoff Bank) | 5.20.0 | ✅
| (腾讯会议国际版) VooV | 2.12.5.504 | ✅
| 微博 (Weibo) | 11.10.1 | ⚠️ | Cannot sign in using password, shows limit reached for verification codes
| 微博国际版 (Weibo International) | 3.9.8 | ⚠️ | Cannot sign in
| 微博极速版 (Weibo Fast) | 10.9.2 (4620) | ⚠️ | Cannot sign in
| 文件管理器+ | 2.7.1 | ✅
| 超星学习通 | 4.6.1 |✅
| 超星学习通 | 5.0.3 | ❌ | Crashes on startup

