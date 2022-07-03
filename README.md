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

| Application | Latest tested version | Android versions | Support level | Known Issues | Notes |
|-------------|-----------------------|------------------|---------------|--------------|-------|
| 23andMe | 5.114.0 | 11 | ✅ |
| 4PDA | 1.9.35 | 11 | ✅ |
| 8 ball pool | 5.5.6 | 11 | ✅ |
| A Dance of Fire and Ice | 1.15.5 | 11 | ✅ || Keyboard supported
| A+ Gallery | 2.2.55.4 | 11 | ✅ | You might face graphical glitches when using dark theme, hence its recommended to use light theme instead.
| ADM | 12.5.4 | 11 | ✅ |
| ADM Pro | 6.4.0 | 11 | ✅ |
| Aegis | 2.0.2 | 11 | ✅ |
| AFK Arena | 1.72.01 | 11 | ⚠️ | Can't login using Google account
| AIDE | 3.2.210316 | 11 | ✅ || Might optionally require GMS
| AIMP | 3.10.1052 | 11 | ✅
| Alan Walker-The Aviation Game | 3.0.6 | 11 | ✅ || Touchscreen and cursor works; keyboard doesn't work
| Alien: Blackout | 2.0 | 11 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS
| Alto's Adventure | 1.8.0 | 11 | ✅
| Alto's Odyssey | 1.0.10 | 11 | ✅
| Amaze File Manager | 3.5.3 | 11 | ✅ || Avoid updating the app
| Among Us | 2022.3.29 | 11 | ✅ | Keyboard may be unresponsive. | Xbox controller works.
| Android System Info | 1.4.2 | 11 | ✅ ||
| Android System Webview Dev | 103.0.5060.22 | 11 | ✅ || App installs correctly 
| Angry Birds Epic | 3.0.27463.4821 | 11 | ⚠️ | Terrible in-game experience, bad performance and low FPS
| AniLabX | 3.8.12 (Iridium) - Beta | 11 | ✅
| AntennaPod | 2.5.0 | 11 | ✅
| APKMirror Installer (Beta) | 1.3.2 | 11 | ⚠️ | Cannot remove ads without subscription which requires Location to be turned on. Apart from this, there are random crashes
| APKPure | 3.17.26 | 11 | ✅ | Sometimes, it might require multiple attempts to install an app
| Apple Music | 3.7.1 | 11 | ✅
| App分享 (AppShare) | 2.1.1 (164) | 11 | ❌ | Can't login
| Aptoide App Store | 9.20.2.1 | 11 | ✅ | Sometimes, downloads might get stuck
| AquaMail (Pro) | 1.34.0-118 | 11 | ✅
| Arcaea | 3.8.8 | 11 | ⚠️ | Keyboard doesn't work on login/register form
| Arknights | 5.0.01 | 11 | 🆖 | Can't login using Google account. Unstable FPS throught the game, especially low FPS in combat for AMD system PC
| Asphalt 9 || 11 | ⚠️ | Keyboard unsupported
| Audible | 3.15.0 | 11 | ✅
| Aurora Store | 4.1.1 | 12 & 11 | ✅
| Authy | 24.8.5 (139) | 11 | ✅ || Produces warnings about GMS which are safe to ignore.
| Azur Lane | 6.0.820 | 11 | ⚠️ | Some characters may appear missing and the game can get stuck while in combat, this can be fixed by restarting the app.
| Bad Piggies HD | 2.4.3141 | 11 | ✅
| BanG Dream! Girls Band Party! | 4.5.0 | 11 | 🆖 | Requires GMS
| Battle Cats Quest | 1.0.4 | 11 | ✅
| BBC iPlayer | 4.137.0.25403 | 11 | ✅ | Sideloaded
| Berry Browser | 3.57.8 | 11, 12 | ✅
| Binance | 2.36.5 | 11 | ✅
| Blue Archive (GB) | 1.36.120365 | 11 | ❌ | Black screen on app launch
| Blue Archive (KR) | 1.39.146794 | 12 & 11 | ❌ | HEVC codec support required
| Bouncer | 1.26.3 | 11 | ⚠️
| Brave Browser | 1.30.87 | 11 | ✅
| Brawl Stars | 38.159 | 11 | ❌ | Game crashes
| BritBox by BBC & ITV | 2.1.2 (20043) | 11 | ❌ | App crashes on start
| Bromite | 94.0.4606.94 | 11 | ✅ || Use x64 build
| C.A.T.S (Crash Arena Turbo Stars) | 2.40.2 | 11 | ✅ | GMS warnings might appear but these can be safely ignored
| CamScanner | 6.3.0.2110240000 | 11 | ❌ | WSA freezes after taking a snap
| Candy Crush Saga | 1.213.2.1 (12132011) | 11 | ✅
| Canvas Student | 6.14.1 | 11 | ✅
| CarX Highway Racing | 1.17.1 | 11 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS
| ChMate | 0.8.10.153 | 11 | ✅
| Clash Mini | 1.1142.10 | 11 | ❌ | App crashes
| Clash of Clans | 14.211.3 | 11 | ❌ | App crashes
| Clash Royale | 3.6.1 | 11 | ❌ | App crashes
| Clouds & Sheep 2 | 1.4.6 | 11 | ✅ | Optionally uses GMS
| Clubhouse | 1.0.11 | 11 | ⚠️ | Unable to login via phone number, it throws error after entering the OTP
| Comixology | 3.10.18.310421 | 11 | ✅
| CnC Rivals | 1.8.1 | 11, 12 | ✅ | | It will pop up "Won't run without GPlay services" when starts, but works fine except GPlay login. You may use link email instead.
| CPU-Z | 1.41 | 11 | ✅
| Cronometer | 3.13.1 | 11 | ✅
| Dcoder | 4.0.76 | 11 | ✅
| Decibel X | 6.4.2 | 11 | ⚠️ | App crashes
| Delivery Club | 4.64.0 | 11 | ❌ | App crashes after selecting a shipping address
| Deus Ex GO | 2.1.111374 | 11 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS
| Destiny Child | 2.8.6 | 11 | ⚠️ | Poor performance during battles
| DevCheck | 3.39 | 11 | ❌ | Blank screen on startup
| Device Info HW | 5.4.1 | 11 | ✅
| DirecTV for Tablet | 5.29.001 | 11 | ⚠️ || Frequent crashing, other functionality proper.
| Discord | 98.6 | 11 | ✅
| DMM Games Store | 2.8.0 | 11 | 🆖 | Requires GMS
| Duolingo | 5.2.35 | 11 | ✅
| Dwarf Balls | 3.5.2 | 11 | 🆖 | Requires GMS for Google Play login.
| Easybell | 2.1.30 | 11 | ✅
| Emby | 2.0.48g | 11 | ✅
| Epic Seven | 1.0.406 | 11 | ⚠️ | Low FPS, unable to sign in with Google
| ES File Explorer | 4.2.1.8 | 11 | ✅ || Avoid updating the app
| Excel | 16.0.14527.20162 | 11 | ✅
| F-Droid | 1.13.1 | 11 | ✅
| F1 TV| 2.0.5 | 11 | ⚠️ | Terrible app experience including screen flashes and crashes while watching a video
| FaceApp: Face Editor || 11 | ❌
| Facebook Messenger | 330.0.0.12.116 (x86_64) | 11 | ⚠️ | Chat Heads don't work
| Fancade | 1.7.6 | 11 | ❌ | App crashes
| FAST Speed Test | 1.0.8 (88) | 11 | ✅
| Fate/Grand Order (US) FGO | 2.22.1 (135) | 11 | ✅ || A little unstable, but playable
| Files by Google | Unknown | Android 11 | ✅ || Works fine
| Fire Emblem Heroes | 6.0.0 | 11 | 🆖 | Requires GMS. If GMS is installed, it cannot be played due to SafetyNet error.
| Firefox | 101.2.0 (2015885319) | 12 & 11 | ⚠️ | On Android 11, it works albeit with improperly rendered webpages. On Android 12, webpages doesn't render anymore causing to consume more resources | Tested only on Intel HD integrated graphics.
| Firefox Nightly | 95.0a1 | 11 | ✅
| foobar2000 | 1.2.30 | 11 | ✅
| Formula 1 | 11.0.1533 | 11 | ⚠️ | Live Timing is broken, keeps crashing on initialization
| Fortnite | 14.10.0 | 11 | ❌ | Crashes at login screen
| Fortnite Installer | 4.1.4 | 11 | ❌ | "Device not supported" error
| Fruit Ninja | 3.3.4 | 11 | ✅ | Version check error | Otherwise, other app functionality is fine
| FTP Server (Free) (F-Droid) | 3.1 - 30100 (11-30) | 11 | ✅
| FX File Explorer | 8.0.3.0 (r8008) | 11 | ✅ | Tested only on the base version (without FX Plus)
| Game Dev Story | 2.47 | 11 | ❌ | App can start but with infinite "loading" screen
| Game Pass | 2110.17.1005 | 11 | ✅ | GMS warnings might appear but these can be safely ignored | Cloud games can be launched but controlling them with controller or touch has not been tested.
| Garage: Bad Dream Adventure | 1.0.191 | 11 | ⚠️ | Stuck after start of Chapter 1
| GBoard | UNKNOWN | 11, 12.1 | ⚠️ | Will not work as expected in newest WSA (2204.x)
| GCash | 5.51.0 | 11 | 🆖 | Requires GMS. Will warn "limited functionality" if no GMS is present, if present, works normally. 
| Geekbench |5.4.1| 11 | ✅
| GeoGebra | 5.0.674.0 | 11 | ✅
| Geometry Dash | 2.11 | 11 | ✅ | If you use high refresh rate monitor, there is a small period where the game speeds up before the level plays for the first time and the audio will get desynced. You can simply pause and resume or die once to fix it since it won't happen on second attempt.
| Girls' Frontline (EN) | 2.0702_362 (362) | 11 | ⚠️ || Game freezes after splash screen, works after installing WSL2, using `wsl --install`
| Globe2Go | 4.7.4.20.0810/3890 | 11 | ✅
| Gmail | <sub>2022.05.01.440951655.Release</sub> | 11 | ✅ || May require GMS
| Gojek | 4.30.1 | 11 | 🆖 | Requires GMS
| Golf Rival | 2.54.241 (88) | 11 | 🆖 | Requires GMS | Produces warnings about GMS. Issues include not being able to pan.
| Google Calendar | 2022.18.2-448173739-release | 11 | ✅ | Requires GMS | Works fine
| Google Camera | Unknown | Android 11 | ✅ || Works fine
| Google Chrome | 94.0.4606.85 | 11 | ✅ | Requires microG or GMS
| Google Classroom | 8.0.181.20.90.3 | 11 | ✅ || Notifications are generic (do not show content), clicking on them may not open the app. Uploading of attachments locally is not possible.
| Google Contacts | 3.68.0.445910596 | ✅ || App may be glitchy from time to time, if that happens, restart the app
| Google Drive | 2.22.197.0.all.alldpi | 11 | ✅ | Works fine, may require GMS
| Google Meet | <sub>2021.10.03.404303734.Release</sub> | 11 | 🆖 | Requires GMS, Share screen doesn't work due to WSA's windowed nature
| Google Photos | 5.91.0.448844219 | 11 | ✅ | Requires GMS |
| Grab | 5.172.200 | 11 | ✅
| Grand Theft Auto: San Andreas || 11 | ✅
| Guardian Tales | 2.23.2 | 11 | 🆖 | Requires GMS
| Hay Day | 1.53.46(1700) | 11 | 🆖 | Account synchronization requires GMS, but it can be bypassed with Supercell ID
| HBO Max | 52.15.0.53 | 11 | ⚠️ | Failed to play video (internal player fails to display image and play sound).
| Hill Climb Racing | 1.53.0 (501) | 11 | ✅
| Hitman Sniper | 1.7.193827 | 11 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS
| Hobi | 2.1.7 | 11 | 🆖 | Requires GMS
| Home Assistant | 2022.3.0-full | 11 | ✅ | Basic functionality works, additional / extended functionality has not been yet tested.
| Honkai Impact 3rd| 5.1.0 | 11 | ⚠️ | Poor graphics quality
| Housesigma Canada Real Estate| 4.3.6 (121) | 11 | ✅
| HTV (hanime tv) | 3.6.7 | 11 | ⚠️ | Failed to play video | Internal player don't work, asks for external player and fails again
| huaCtrl PRO | 1.0.27 | 11 | ✅
| Huawei AppGallery | 11.4.2.300 | 11 | ✅ | Frequent crashes were experienced, otherwise the app functionality is fine
| Hungry Shark Evolution || 11 | ✅
| Hyper Square | 3.0.1 | 11 | ✅
| iDOLM@STER Million Live! Theater Days | 4.0.401 | 11 | ⚠️ | Anything 3D with a moving background is broken, but everything 2D works perfectly | ARMv7 version is unusably slow, get ARM64
| Instagram | 236.0.0.18.109 | 11, 12.1 | ⚠️ || Need to use an Android keyboard (eg. MS SwiftKey) to be able to reply stories
| iOS app (any) || 11 | ❌ | Thanks for testing, Brad.
| iPusnas | 1.5.1 | 11 | ✅
| JAKI - Jakarta Kini | 1.2.34 | 11 | 🆖 | Some features require GMS
| Jet Car Stunts 2 | 1.0.13 | 11 | ❌ | Loads up but orientation and menus are broken
| Jetpack Joyride | 1.52.1 (58461800) | 11 | ⚠️ | Google Play Games sync doesn't work, otherwise the game functionality is fine
| JioSaavn | 8.2.1 | 11 | ✅ |Doesn't support fullscreen and rare crashes but running fine
| Joey (Reddit client) | 2.0.0.1 | 11 | ✅
| Joplin | 2.4.3 (2097651) | 11 | ✅
| JuiceSSH | 3.2.2 | 11 | ⚠️ | Connecting to SSH server needs multiple tries
| Kahoot || 11 | ✅
| Khan Academy | 7.3.3 | 11 | ✅
| Kik | 7.10.1.176 (82) | 11 | ✅
| Kindle | 8.47.1.3370 | 11 | ✅
| KINGDOM HEARTS Uχ Dark Road | 4.4.0 (Offline) | 11 | ✅ | GMS warnings might appear but these can be safely ignored
| Kobo Books | 8.40.29843 | 11 | ⚠️ | Aspect ratio and resolution are fixed, appears blurry when resized
| Konosuba:FD | 1.12.1 | 11 | 🆖 | Requires GMS
| KRL Access | 4.1.0 | 11 | ❌ | App crashes
| Last Day On Earth: Survival || 11 | 🆖 | Might require GMS
| Lawnchair | 11.0 Alpha 6.1 (8b01af8).release | 11 | ❌ | App crashes
| Lawnchair | 12 Alpha 5 | 11 | ✅
| League of Legends: Wild Rift || 11 | ✅
| Libby | 4.3.1 | 11 | ✅
| LIMBO Demo | 1.20 | 11 | ✅
| LINE | 12.0.1 | 11 | ✅
| Line Rangers | 7.6.3 | 11 | ✅
| LinkedIn | 4.1.632 | 11 | ✅
| LSPosed | 1.8.0 | 11 | ✅
| Magic Tiles 3 | 8.086.201 | 11 | ✅
| Magisk | Internal build? | 11 | ✅ || Magisk developer confirmed able to gain root access - [link to his tweet](https://twitter.com/topjohnwu/status/1451282578514735131)
| ManCityApp | 2.1.11 | 11 | 🆖 || Might require GMS
| Manzur's Study Circle (MSC) | 1.0.2 | 11 | ✅
| MapleStory M | 1.7000.2835 | 11 | ❌ |Crashes at loading screen
| Mario Kart Tour | 2.10.0 | 11 | ❌ | Fails to connect to servers after Nintendo login
| Material Files | 1.5.2 | 11, 12 | ✅
| microG Settings | N/A | 11 | ❌ | App crashes, doesn't load
| Microsoft Authenticator | 6.2112.8213 | 11 | ✅ || Some features might require GMS
| Microsoft Azure | 3.9.2.2021.09.30-19.35.50 | 11 | ✅
| Microsoft Edge | 95.0.1020.42 | 11 | ❌ | App frequently crashes
| Microsoft Edge Canary | 103.0.1264.1 | 11 | ❌ || Fails to load websites
| Microsoft Launcher | 6.210602.1.994630 | 11 | ✅
| Microsoft PowerApps | 3.21124.20 | 11 | ✅
| Microsoft Swiftkey Keyboard | 8.10.12.4 | 11, 12.1 | ✅ | Works on WSA 2203 (Android 11), but on-screen is completely broken in WSA 2204(Dev) (Android 12.1)
| Minecraft (Aurora Store) | 1.17.40.06 | 11 | ❌ | Unable to verify game owner
| Minecraft (China Edition) || 11 | ✅
| Minecraft (Play Store) | 1.18.0.23 | 11 | ✅
| MiX | 6.57.0-Beta_B21070510 | 11 | ✅
| Mobile JKN | 3.7.1 | 11 | ✅ || Some features might require GMS
| Mobile Legends | 1.6.66.7281 | 11 | ✅
| MOLA | 2.1.3 | 11 | ❌ | App crashes
| Monument Browser | 1.0.333 | 12 | ✅
| Monument Valley | 2.7.17 | 11 | ✅
| Monument Valley 2 | 2.0.3 | 11 | ✅
| Moodle | 3.9.5 | 11 | ✅
| Mortal Kombat X(APKPure) | 5.9.0 | 11 | ❌ | Stuck on initialization screen, message shows up saying "Download failed to start"
| MT File Manager | 2.10.0 | 11 | ✅
| Musically (TikTok) | 7.8.0 | 11 | ✅
| Muslim Pro | 1.2.3 | 11 | 🆖 | Requires GMS
| MX Player | 1.40.9 | 11 | ✅
| MX Player Pro | 1.39.13 | 11 | ⚠️ | App crashes, but videos can be played from external sources
| My Verizon | 16.4.2 | 11 | ✅ || The page might be displayed sideways for a short amount of time when the app is launched. The app automatically reverts to correct orientation in a second.
| Neko | 2.6.2 | 11 | ✅
| Nekogram X | 8.1.2-1-rc01 | 11 | ✅ || Use NoGcm variant
| Netflix (Aurora Store) | 8.4.0 | 11 | ❌ | "Device not supported" error
| Network IP Scanner | 3.2 | 11 | ⚠️ | Only scans WSA's own VirtWifi network
| NewPipe | 0.22.1 | 11 | ✅
| NFL | 56.1.7 | 11 | ❌ | App crashes
| NieR Re[in]carnation | 1.7.1 | 11 | ❌ | Unable to get past the loading screen
| Nova Launcher | 7.0.49 (7049) | 11 | ⚠️ | UI is messy, but app drawer is fine
| Nu Carnival | 1.0.2-erolabs | 11 | ❌ | App stuck on a black screen
| Office | 16.0.14527.20162 | 11 | ✅ || Might require microG
| Office Lens | 16.0.14527.20178 | 11 | ❌ | Might require GMS, cannot sign in
| Okay? | 4.08 | 11 | ✅
| One Store | 7.6.0 | 11 | ✅
| Opera Browser Beta | 65.1.3381.61349 (x86_64) | 11 | ✅ || Change app layout to Tablet Mode for a better experience
| Opera GX : Gaming Browser | 1.3.6 | 11 | ✅
| Opera Mini Beta | 61.0.2254.59921 | 11 | 🆖 | Requires GMS
| Opera Touch Browser | 2.9.6 | 11 | ⚠️ | My Flow feature requires GMS | GMS warnings might appear but these can be safely ignored
| Oppo App Store (China) | 8.6.4 Beta 1 | 11 | ❌ | App freezes on blank screen
| Oppo Game Center (China) | 9.7.0_14b2c0c_210521 | 11 | ✅
| Oreo: Twist, Lick, Dunk | 1.5.6 | 11 | ✅ | Minor graphical glitches
| OsmAnd~ | 3.9.10 | 11 | ✅
| Oto Music | 3.0.2 | 11 | ✅ || Requires app restart to refresh list
| OurGroceries | 4.0.10 | 11 | ✅ | Premium keys require Google Play Store
| Outlook | 4.2138.0 | 11 | ⚠️ | Cannot activate device administrator with Outlook, which prevents activation.
| Phigros || 11 | ✅
| Pixel People | 4.7 | 11 | ✅ | Changing window size breaks the game. Runs at low FPS but is still playable.
| Plants vs Zombies 2 | 9.2.2 | 11 | ✅ | Cloud save using Google Play Games works if GMS is available
| Playstation App | 21.11.2 | 11 | ⚠️ | Runs very slow and takes some time to connect to voice chat, beside that it works  
| Plex | 8.26.2.29389 | 11 | ✅
| Plex Dash | 1.1.1 | 11 | ❌ | App crashes after splash screen
| Plexamp | 3.8.2 | 11 | ⚠️ | Layout and app orientation issues
| Pocket | 7.56.0.0 | 11 | ⚠️ | Unable to log in with a Firefox account, instant (push) syncing is unavailable
| Pokémon GO || 11 | ❌ | Unable to authenticate
| Pokémon Masters EX | 2.19.0 | 11 | ❌ | 10102 An error has occured.
| Pokémon Unite | 1.2.1.2 | 11 | ⚠️ | Battle experience is terrible
| PornHub || 11 | ✅
| Pou | 1.4.84 | 11 | ✅
| PowerPoint | 16.0.14527.20162 | 11 | ✅ | Might require GMS / MicroG
| Prep Ladder | 2.0.79-p | 11 | ⚠️ | Video pane opens but no audio or video and time keeps on going
| Princess Connect! Re: Dive (Korean) | 5.6.1 | 12 | ❌ | Only touch effect works after displaying the publisher logo
| Princess Connect! Re: Dive (Traditional Chinese) | 2.9.0 | 11 | ⚠️ | Battle experience is terrible, cannot sync with Google Play Games
| Pydroid | 5.00_x86_64 | 11 | ✅
| Q-Dance | 8.0.7 | 11 | ❌ | App crashes
| QooApp | 8.3.3 | 11 | ✅
| QPython 3L | 3.0.0 | 11 | ✅
| QQ | 8.2.11 | 11 | ✅
| Ragnarok M: Eternal Love EU | 1.0.70 | 11 | ✅
| Rayman Classic | 1.0.1 | 11 | ✅
| Real Racing 3 | 10.1.0 | 11 | ✅ | Only controller is supported. keyboard doesn't work
| Reddit || 11 | ✅
| Relay | 10.0.378 | 11 | ✅
| Remini - AI Photo Enhancer || 11 | ⚠️ | Oops! Something went wrong Your image didn't save. Please try again.
| Remote Desktop (Microsoft) | 10.0.12.1148 | 11 | ✅
| Rider | 1.59 | 11 | ✅
| Robinhood - Food & Booking | 2.2.2 | 12.1 | ⚠️ | App having trouble loading content. Maps & Location picker don't work (Requires GMS). | You can log-in only on one device at the same time. Previous device will log-out upon signing-in on new device.
| Roblox | 2.499.381 | 11 | ⚠️ | Graphical anomalies | GMS warnings might appear but these can be safely ignored
| Rocket League Sideswipe | 1.0 (356721) | 11 | ❌ | OpenGL ES 3.1 is unsupported
| Rootless Launcher | 3.9.1 | 11 | ❌ | App crashes
| SATRIA | 1.0.0 | 11 | ❌ | Needs fingerprint reader support
| SD Maid (pro) | 5.2.2 | 11 | ⚠️ | Unable to grant external storage privileges, can be skipped
| Shadow Fight 2 | 2.16.0 | 11 | ⚠️ | Optionally uses GMS, Doesn't support keyboard control makes fighting more harder | GMS warnings might appear but these can be safely ignored, Cloud save requires GMS
| Shadow Fight 3 | 1.25.7 | 11 | ✅ | Optionally uses GMS, Cloud save using Facebook not working | Keyboard control are supported uses (W A D X) to use analog, GMS warnings might appear but these can be safely ignored, Cloud save requires GMS
| ShemarooMe | 1.0.16 (106) | 11 | ✅
| Shizuku | 12.3.0.r668.5687d0c | 11 | ✅ | Works well with Wireless debugging
| Shopee PH | 2.86.09 | 11 | ⚠️ | App works but cannot login
| Showtime | 3.1.1 | 11 | ❌ | App crashes when you try to login. Button clicks dont work
| Simple Gallery | 5.3.9 | 11 | ❌ | App crashes when you try to view a photo
| Sky Map | 1.10.0 - RC3 | 11 | 🆖 | Complains about missing accelerometer controls, requires GMS
| Sky: Children of the Light | 0.15.1 | 11 | ❌ | OpenGL ES 3.1, Vulkan 1.0.3 and Vulkan level 0 missing
| SkySafari | 6.8.6.15 | 11 | 🆖 | Failed license check on startup, appears to require GMS
| Slack | 21.11.20.0-B | 11 | ✅
| Smart Launcher | 5.5 Build 052 | 11 | ✅
| Smart Life | 3.32.5 | 11 | ❌ | The app is producing constant flashes between light and dark mode, and the UI element of agreement pop-up is moving on screen so it can't be accepted
| Smash Hit | 1.4.3 | 11 | ✅
| Snapchat || 11 | ⚠️ | Camera view is flipped | GMS warnings might appear but these can be safely ignored
| Solid Explorer File Manager | 2.8.16 | 11 | ❌ | App crashes
| Speedtest by Ookla | 4.6.10 (145526) | 11 | ⚠️ | VPN does not work
| Spotify | 8.7.30.1221 | 11, 12.1 | ✅ | 
| Spotify Lite | 1.9.0.2883 | 11 | ✅
| Squircle IDE | v2022.1.2 | 11, 12 | ✅
| Standoff 2 | 0.16.6 | 11 | ⚠️ | Battle experience is terrible, includes micro-stutters
| Stardew Valley | 1.4.5.151 | 11 | ✅
| State of Survival | 1.13.40 | 11 | ✅
| Steam | 2.3.13 | 11 | ✅
| Steam Chat | 1.0 | 11 | ✅
| Steam Link | 1.1.81 | 11 | ❌ | App crashes
| Stickman Hook | 7.2.8 | 11 | ❌ | Game fails to initialize
| Subway Surfers | 2.24.2 | 11 | ✅ | Doesn't support keyboard control
| SwiFTP Server| 1.24 | 11 | ✅
| Sword Art Online: Integral Factor| 1.9.2 | 11 | ✅ | Keyboard unsupported
| Sword Art Online: Memory Defrag | 3.0.2 | 11 | ✅ | Keyboard unsupported
| Sword Art Online: Unleash Blading | 3.2.0 | 11 | ⚠️ | Can't detect device
| Symbolab | 9.3.0 | 11 | ✅ || Keyboard not working, in-app keyboard is available though
| Sync for Reddit Pro | 20.0.3 | 11 | ✅
| Tachiyomi | 0.13.4 | 12 & 11 | ✅
| TachiyomiAZ | 8.7.0-AZ | 12 & 11 | ✅
| TachiyomiJ2K/TachiJ2K | 1.5.4 | 11/12 | ✅ | Parsing links (from a browser) causes to open the Tachiyomi extension window instead of opening TachiJ2K itself.
| Teamfight Tactics | 12.5.4259171 | 11 | ⚠️ | Crashes often before getting in game but after getting in, not many issues. Can get laggy at times but somewhat playable.
| TeamViewer | 15.22.136 | 11 | ✅
| Telegram | 8.1.2 | 11 | ✅
| Termux (F-droid) | 0.118.0 | 12 & 11 |✅
| Terraria | 1.4.3.2.2 | 11 | ✅ || Keyboard supported
| Tesla | 4.6.1 | 11 | ⚠️ | Vehicle graphics and maps do not load, cannot enable phone key. | Internet-based vehicle controls, charge stats, services are functional.
| The Battle Cats | 11.2.1 | 11 | ✅
| The Battle of Polytopia | 2.0.59.5719 | 11 | ❌ | Validation error
| The Globe and Mail | 6.2.0 (100) | 11 | ✅
| The King Of Fighters Allstar | 1.9.3 | 11 | ✅ | Blank screen / app crash on first boot, works on second boot upwards
| This War of Mine | 1.0 | 11 | ❌ | Infinite loop at start-up screen
| TIDAL | 2.49.0 | 11 | ✅
| TikTok (China) | 18.1.0 | 11 | ⚠️ | App crashes on first startup and you might face hiccups logging in
| TikTok (Global) | 24.0.3 | 11 | ✅
| TikTok (TV Version) | 1.6.0 | 11 | ❌ | App crashes
| TikTok Lite | 21.7.1 | 11 | ❌ | App crashes
| TP-Link Tapo | 2.4.25 | 11 | ✅
| Trello | 2021.14.1.16332-production | 11 | ⚠️ | Login needs web browser installed in WSA, using Windows' default browser will not work
| True Skate | 1.5.39 | 11 | ✅ | Minor graphical glitches
| Tune In Pro | 28.7 (267721) | 11 | ✅
| Twitter | 9.16.1-release.00 | 11 | ✅ | Optionally requires GMS
| UC Browser | 13.0.0.1288 (x86) | 11 | ✅ || Avoid updating the app
| Uptodown App Store | 4.35 | 11 | ⚠️ | Keeps "analyzing device" on app details page, thus its unable to download APKs.
| Umamusume: Pretty derby (Korean) | 1.0.1 | 12 | ❌ | Only touch effect works after displaying the developer logo
| Vanced Manager | 2.6.2 (Crimson) | 11 | ✅
| Vanced MicroG | 0.2.22.212658 | 11 | ⚠️ | microG Google sign-in method does not work, hence use Huawei sign-in method to sign in to Google account
| Via Browser | 4.3.1 | 11 | ✅
| Vidio | 5.64.5-f0aa483a3d | 11 | 🆖 || Might require GMS for login
| Vivaldi Browser | 4.3.2439.61 | 11 | ✅
| VK | 6.58 | 11 | ✅
| VLC | 3.4.0 | 11 | ✅
| VSCO | 264 | 11 | ⚠️ | Cannot sign in
| War Robots | 7.7.7 (134783) | 11 | ✅ | GMS warnings might appear but these can be safely ignored
| Warden | 1.0.3.release | 11 | ⚠️ | App screen flashes otherwise functionality-wise its normal
| Warfare Incorporated | 1.63 | 11 | ✅ | The selection box does not work.
| Wealthsimple Trade | 2.27.1 (2195) | 11 | ✅
| WhatsApp | 2.21.20.20 | 11 | ⚠️ | WhatsApp cloud chat backups will not work, app was tested with microG installed
| Where is my Water? || 11 | ⚠️ | Many images are replaced with white rectangles
| Where is my Water? 2 || 11 | ⚠️ | Most images are replaced with white rectangles, Vignette overlay is full white and covered the whole playing area. The ground is not textured correctly.
| Where is my Water? Featuring XYY || 11 | ⚠️ | Bells are invisible
| Word | 16.0.14430.20246 | 11 | ✅ || Might require microG
| Wordament | 3.9.10260 | 11 | ✅
| Wulkanowy (F-Droid) | 1.4.3 | 11 | ✅
| Wulkanowy (Play Store) | 1.4.3 | 11 | 🆖
| Wyze | 2.30.0 | 11 | ✅
| XBrowser | 3.7.7 | 11 | ✅
| xManager | 3.3 | 11 | ✅
| X-plore File Manager | 4.27.10 | 11 | ✅
| Yahoo! Fantasy Sports | 10.31.0 | 11 | ❌ | App crashes on launch
| Yandex.Maps | 10.6.0 | 11 | ⚠️ | Map doesn't work
| Ymusic | 3.7.2 | 11 | ✅
| YouTube (Google)| 16.40.35 | 11 | 🆖 | Requires GMS
| YouTube Music (Google) | 5.07.50 | 11 | 🆖 | Requires GMS
| YouTube Music Vanced | 43.9.50 | 11 | ✅
| Youtube Vanced | 16.29.39 | 11 | ⚠️ | Picture-in-picture doesn't work & Can't join channel membership
| ZArchiver | 0.9.5.8 (9596) | 11 | ✅
| Zenly (w/o GMS) | 4.55.2 | 11 | ⚠️ | App crashes after login, but background location works
| Zoom | 5.8.3.2634 | 11 | ⚠️ | Camera severely glitched, share screen doesn't work due to WSA's windowed nature.
| 白夜極光 (Alchemy Stars) | 1.2.2 | 11 | ⚠️ | Poor in-game performance
| 明日方舟 (Arknights Simplified Chinese) | 1.6.01 | 11 | ✅
| 哔哩哔哩 (Bilibili) || 11 | ✅
| 酷安 (CoolApk) | 11.4.3 | 11 | ⚠️ | Unable to sign in using third party apps
| 创建快捷方式 (Create Shortcut) | 1.17 | 11 | ✅ || Can be used to access any app
| Дурак Онлайн (Durak Online) | 1.9.2 | 11 | 🆖 | Requires GMS
| মুনাজাতে মাকবূল ও মাসনূন দু'আ - Munajate Makbul | 1.0 | 11 | ✅
| ウマ娘 プリティーダービー | 1.16.0 | 11 | ⚠️ | Doesn't work with GTX1660. Works with Microsoft Basic Render Driver with graphical issues. | Some features may require GMS.
| ウマ娘 プリティーダービー | 1.19.5 | 12 | ❌ | Only touch effect works after displaying the developer logo
| 九黎 | 1.3.5.01 | 11 | ❌ | App crashes
| 公主连结R (Princess Connect! Re: Dive (Simplified Chinese) | 3.4.10 | 11 | ✅
| 云·原神 (Genshin Impact (Cloud app) )|| 11 | ✅
| 原神（Genshin Impact） | 2.2.0 | 11 | ⚠️ | Working but heavy graphical glitches - [video](https://www.bilibili.com/video/BV1zT4y1o73D?)
| 崩坏学园2 (Honkai Gakuen 2)| 8.5 | 11 | ✅ || Game has inbox keyboard controller for WASD
| 米游社 (mihoyo Chinese Community) | 2.14.1 | 11 | ⚠️ | The app might lag when inserting a photo into a new post
| 東方LostWord | 1.16.0 | 11 | ❌
| 战双帕弥什 (Punishing: Gray Raven) || 11 | ✅ || Keyboard is supported
| СберБанк (SberBank) | 12.9.0 | 11 | ✅
| Тинькофф (Tinkoff Bank) | 5.20.0 | 11 | ✅
| (腾讯会议国际版) VooV | 2.12.5.504 | 11 | ✅
| 微博 (Weibo) | 11.10.1 | 11 | ⚠️ | Cannot sign in using password, shows limit reached for verification codes
| 微博国际版 (Weibo International) | 3.9.8 | 11 | ⚠️ | Cannot sign in
| 微博极速版 (Weibo Fast) | 10.9.2 (4620) | 11 | ⚠️ | Cannot sign in
| 文件管理器+ | 2.7.1 | 11 | ✅
| 超星学习通 | 4.6.1 | 11 | ✅
| 超星学习通 | 5.0.3 | 11 | ❌ | Crashes on startup
