## Contributing

Thanks for your interest in contributing! Doing so is simple. Just [edit this page](/edit/master/README.md) and submit a pull request (PR) with your changes.
Someone will review it and merge it in as soon as possible.

When editing the Markdown, please keep these rules in mind:

1. Do not link to any APKs.
2. Double-check your spelling/grammar.

## Legend

This page currently uses Unicode characters from [Unicode Emoji (1.0)](https://unicode.org/Public/emoji/1.0/emoji-data.txt). If you are unable to see these characters, please open an issue.
 
- ✔️ Works
- 🆖 Works, but needs Google Mobile Services
- ⚠️ Works, but with some notable problems
- ❌ Broken

## Support table (OS features)

| Feature | Support level | Notes |
|---------|---------------|-------|
| Multi-touch | ✔️ | Demo: [Arcaea](https://www.bilibili.com/video/BV1Ph411n7M5) |
| Virtual Wifi (VirtWifi) | ✔️ |  |
| VPN | ❌ | VPN Connection request dialog does not appear |
| OpenGL ES 3.1 | ❌ | |
| Vulkan | ❌ | |

### Workarounds

#### VPN
There is no `com.android.vpndialogs` in WSA. However, it's possible to manually grant the VPN activation permission with AppOps via `adb shell`:
```shell
appops set [package name] ACTIVATE_VPN allow
```

#### Launching Android Apps with URL scheme
Microsoft provides a custom URI scheme for WSA, making it easier to launch apps:
```shell
wsl://[App Package Name]
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

| Application    | Latest tested version | Support level | Known Issues  | Notes |
|----------------|-----------------------|---------------|---------------|-------|
| 23andMe | 5.114.0 | ✔️ |||
| A+ Gallery | 2.2.55.4 | ✔️ | You might face graphical glitches when using dark theme, hence its recommended to use light theme instead. ||
| ADM | 12.5.4 | ✔️ |||
| ADM Pro | 6.4.0 | ✔️ |||
| Aegis | 2.0.2 | ✔️ |||
| AFK Arena | 1.72.01 | ⚠️ | Can't login using Google account || 
| AIMP | 3.10.1052 | ✔️ |||
| Alien: Blackout | 2.0 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS ||
| Alto's Adventure | 1.8.0 | ✔️ |||
| Alto's Odyssey | 1.0.10 | ✔️ |||
| AniLabX | 3.8.12 (Iridium) - Beta | ✔️ |||
| Among Us | 2021.6.30 | ✔️ || Xbox controller is working, however the keyboard isn't working |
| Amaze File Manager | 3.5.3 | ✔️ | | Avoid updating the app ||
| Angry Birds Epic | 3.0.27463.4821 | ⚠️ | Terrible in-game experience, bad performance and low FPS||
| APKMirror Installer (Beta) | 1.3.2 | ⚠️ | Cannot remove ads without subscription which requires Location to be turned on. Apart from this, there are random crashes ||
| Arknights | 5.0.01 | 🆖 | Can't login using Google account ||
| Aurora Store | 4.0.7 | ✔️ |||
| Audible | 3.15.0 | ✔️ |||
| APKPure | 3.17.26 | ✔️ | Sometimes, it might require multiple attempts to install an app ||
| Aptoide App Store | 9.20.2.1 | ✔️ | Sometimes, downloads might get stuck ||
| Apple Music | 3.7.1 | ✔️ |||
| App分享 (AppShare) | 2.1.1 (164) | ❌ | Can't login ||
| Authenticator by Microsoft | 6.2110.6737 |🆖| Requires GMS ||
| Arcaea |  | ✔️ |||
| Azur Lane | 6.0.1 | ✔️ |||
| Bromite | 94.0.4606.94 |  ✔️ |  | Use x64 build |
| Brawl Stars | 38.159 | ❌ | Game crashes ||
| Brave Browser | 1.30.87 | ✔️ ||
| Binance | 2.36.5 | ✔️ |||
| 哔哩哔哩 (Bilibili) |  | ✔️ |||
| Candy Crush Saga | 1.213.2.1 (12132011) | ✔️ |||
| Canvas Student | 6.14.1 | ✔️ |||
| CarX Highway Racing | 1.17.1 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS ||
| 超星学习通 | 5.0.3 |❌| Crashes on startup ||
| 超星学习通 | 4.6.1 |✔️|||
| Clash of Clans | 14.211.3 | ❌ | App crashes ||
| Clash Royale | 3.6.1 |❌ | App crashes ||
| Classroom by Google | 7.6.381.20.90.2 | 🆖 | Requires GMS ||
| Clouds & Sheep 2 | 1.4.6 | ✔️ | Optionally uses GMS ||
| Clubhouse | 1.0.11 | ⚠️ | Unable to login via phone number, it throws error after entering the OTP | |
| 酷安 (CoolApk) | 11.4.3 | ⚠️ | Unable to sign in using third party apps ||
| 创建快捷方式 (Create Shortcut) | 1.17 | ✔️ | | Can be used to access any app |
| Comixology | 3.10.18.310421 | ✔️ | | |
| CPU-Z | 1.41 | ✔️ |||
| Deus Ex GO | 2.1.111374 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS ||
| DevCheck | 3.39 | ❌ | Blank screen on startup ||
| Device Info HW | 5.4.1 | ✔️ |||
| Discord | 98.6 | ✔️ |||
| Дурак Онлайн (Durak Online) | 1.9.2 | 🆖 | Requires GMS ||
| DMM Games Store | 2.8.0 | 🆖 | Requires GMS ||
| Epic Seven | 1.0.406 | ⚠️ | Low FPS, unable to sign in with Google ||
| ES File Explorer | 4.2.1.8 | ✔️ | | Avoid updating the app |
| Excel | 16.0.14527.20162 | ✔️ |||
| F1 TV| 2.0.5 | ⚠️ | Terrible app experience including screen flashes and crashes while watching a video |
| Formula 1 | 11.0.1449 | ✔️ | |
| FAST Speed Test | 1.0.8 (88) | ✔️ |||
| Fancade | 1.7.6 | ❌ | App crashes ||
| F-Droid | 1.13.1 | ✔️ ||
| Fire Emblem Heroes | 5.10.0 | 🆖 | Requires GMS ||
| Firefox | 93.2.0 (2015839751) | ✔️ ||
| Firefox Nightly | 95.0a1 | ✔️ ||
| Facebook Messenger | 330.0.0.12.116 (x86_64) | ⚠️ | Chat Heads don't work |
| Fortnite Installer | 4.1.4 | ❌ | "Device not supported" error |
| Fortnite | 14.10.0 | ❌ | Crashes at login screen |
| Fruit Ninja | 3.3.4 | ✔️ | Version check error | Otherwise, other app functionality is fine |
| Game Pass | 2110.17.1005 | ✔️ | GMS warnings might appear but these can be safely ignored | Cloud games can be launched but controlling them with controller or touch has not been tested. |
| Genshin Impact | 2.2.0 | ⚠️ | Working but heavy graphical glitches - [video](https://www.bilibili.com/video/BV1zT4y1o73D?) |
| Genshin Impact (Cloud app) || ✔️ |||
| Geekbench |5.4.1| ✔️ |||
| Google Chrome | 94.0.4606.85 | ✔️ | Requires microG or GMS | |
| Guardian Tales | 2.23.2 | 🆖 | Requires GMS ||
| Grab | 5.172.200 from Huawei AppGallery | ✔️ ||
| Grand Theft Auto: San Andreas |  | ✔️ ||
| Hitman Sniper | 1.7.193827 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS ||
| Hobi | 2.1.7 | 🆖 | Requires GMS |
| 崩坏学园2 (Honkai Gakuen 2)| 8.5 | ✔️ | | Game has inbox keyboard controller for WASD |
| Honkai Impact 3rd| 5.1.0 | ⚠️ | Poor graphics quality |
| huaCtrl PRO | 1.0.27 | ✔️ ||
| Huawei AppGallery  | 11.4.2.300 | ✔️ | Frequent crashes were experienced, otherwise the app functionality is fine ||
| Hyper Square | 3.0.1 | ✔️ ||
| iOS app (any) | | ❌ | Thanks for testing, Brad. |
| Instagram | 210.0.0.28.71 | ✔️ ||
| Jetpack Joyride | 1.52.1 (58461800) | ⚠️ | Google Play Games sync doesn't work, otherwise the game functionality is fine ||
| Jet Car Stunts 2 | 1.0.13 | ❌ | Loads up but orientation and menus are broken ||
| JioSaavn | 8.2.1 | ✔️ |Doesn't support fullscreen and rare crashes but running fine|
| Joey (Reddit client) | 2.0.0.1 | ✔️ ||
| Joplin | 2.4.3 (2097651) | ✔️ ||
| Kik | 7.10.1.176 (82)  | ✔️ ||
| Kindle | 8.47.1.3370 | ✔️ | | |
| KINGDOM HEARTS Uχ Dark Road | 4.4.0 (Offline) | ✔️ | GMS warnings might appear but these can be safely ignored ||
| Konosuba:FD | 1.12.1 | 🆖 | Requires GMS ||
| Lawnchair | 11.0 Alpha 6.1 (8b01af8).release | ❌ | App crashes ||
| League of Legends: Wild Rift | | ✔️ ||
| LIMBO Demo | 1.20 | ✔️ |||
| Magic Tiles 3 | 8.086.201 | ✔️ ||
| Magisk | Internal build? | ✔️ || Magisk developer confirmed able to gain root access - [link to his tweet](https://twitter.com/topjohnwu/status/1451282578514735131) |
| MapleStory M | 1.7000.2835 | ❌ |Crashes at loading screen||
| Mario Kart Tour | 2.10.0 | ❌ | Fails to connect to servers after Nintendo login ||
| Material Files | 1.3.1 | ✔️ ||
| Microsoft Edge | 93.0.961.78 (96107815) | ❌ | Fails to load websites ||
| Microsoft Launcher | 6.210602.1.994630 | ✔️ ||
| Minecraft (Aurora Store) | 1.17.40.06 | ❌ | Unable to verify game owner ||
| Minecraft (Play Store) | 1.18.0.23 | ✔️ |||
| Minecraft (China Edition) |  | ✔️ |||
| MiX | 6.57.0-Beta_B21070510 | ✔️ |||
| Monument Valley | 2.7.17 | ✔️ |||
| Monument Valley 2 | 2.0.3 | ✔️ |||
| MT File Manager | 2.10.0 | ✔️ |||
| Muslim Pro | 1.2.3 | 🆖 | Requires GMS |
| 米游社 (mihoyo Chinese Community) | 2.14.1 | ⚠️ | The app might lag when inserting a photo into a new post |
| Nekogram X | 8.1.2-1-rc01 | ✔️ || Use NoGcm variant |
| Neko | 2.6.2 | ✔️ | | |
| Netflix (Aurora Store) | 8.4.0 | ❌ | "Device not supported" error ||
| NFL | 56.1.7 | ❌ | App crashes ||
| NieR Re[in]carnation | 1.7.1 | ❌ | Unable to get past the loading screen ||
| Nova Launcher | 7.0.49 (7049) | ⚠️ | UI is messy, but app drawer is fine |
| Office | 16.0.14527.20162 | ✔️ || Might require microG | 
| Office lens | 16.0.14527.20178 | ❌ || Might require GMS, cannot sign in |
| Opera Browser Beta | 65.1.3381.61349 (x86_64) | ✔️ || Change app layout to Tablet Mode for a better experience |
| Opera GX : Gaming Browser | 1.3.6 | ✔️ |||
| Opera Mini Beta | 61.0.2254.59921 | 🆖 | Dark mode doesn't work due to inability to draw over apps | Crashes without GSM (with no warning) |
| Opera Touch Browser | 2.9.6 | ⚠️ | My Flow feature requires GMS | GMS warnings might appear but these can be safely ignored |
| Oppo App Store (China) | 8.6.4 Beta 1 | ❌ | App freezes on blank screen ||
| Oppo Game Center (China) | 9.7.0_14b2c0c_210521 | ✔️ |||
| Oreo: Twist, Lick, Dunk | 1.5.6 | ✔️ | Minor graphical glitches ||
| OsmAnd~ | 3.9.10 | ✔️ |||
| Oto Music | 3.0.2 | ✔️ || Requires app restart to refresh list |
| Outlook | 4.2138.0 | ⚠️ | Cannot activate device administrator with Outlook, which prevents activation. ||
| Pixel People | 4.7 | ✔️ | Changing window size breaks the game. Runs at low FPS but is still playable. ||
| Princess Connect! Re: Dive (Traditional Chinese) | 2.9.0 | ⚠️ | Battle experience is terrible, cannot sync with Google Play Games |
| Pokémon Masters EX | 2.13.0 | 🆖 | Requires GMS ||
| Pokémon Unite | 1.2.1.2 | ⚠️ | Battle experience is terrible ||
| Pokémon GO | | ❌ | Unable to authenticate ||
| The Battle of Polytopia | 2.0.59.5719 | ❌ | Validation error ||
| Pou | 1.4.84 | ✔️ |||
| PowerPoint | 16.0.14527.20162 | ✔️ | Might require GMS / MicroG
| Phigros |  | ✔️ |||
| 战双帕弥什 (Punishing: Gray Raven) || ✔️ || Keyboard is supported |
| Q-Dance | 8.0.7 | ❌ | App crashes ||
| QooApp | 8.3.3 | ✔️ |||
| QQ | 8.2.11 | ✔️ |||
| Rayman Classic | 1.0.1 | ✔️ |||
| Reddit | | ✔️ |||
| Relay | 10.0.378 | ✔️ |||
| Remote Desktop (Microsoft) | 10.0.12.1148 | ✔️|||
| Roblox | 2.499.381 | ⚠️ | Graphical anomalies | GMS warnings might appear but these can be safely ignored |
| Rootless Launcher | 3.9.1 | ❌ | App crashes |
| SD Maid (pro) | 5.2.2 | ⚠️ | Unable to grant external storage privileges, can be skipped ||
| Shadow Fight 2 | 2.16.0 | ⚠️ | Optionally uses GMS, Doesn't support keyboard control makes fighting more harder | GMS warnings might appear but these can be safely ignored, Cloud save requires GMS |
| Shadow Fight 3 | 1.25.7 | ✔️ | Optionally uses GMS, Cloud save using Facebook not working | Keyboard control are supported uses (W A D X) to use analog, GMS warnings might appear but these can be safely ignored, Cloud save requires GMS |
| Shizuku | 12.3.0.r668.5687d0c | ✔️ | Works well with Wireless debugging |
| Simple Gallery | 5.3.9 | ❌ | App crashes when you try to view a photo ||
| Sky: Children of the Light | 0.15.1 | ❌ | OpenGL ES 3.1, Vulkan 1.0.3 and Vulkan level 0 missing ||
| Smart Life | 3.32.5 | ❌ | The app is producing constant flashes between light and dark mode, and the UI element of agreement pop-up is moving on screen so it can't be accepted ||
| Smart Launcher | 5.5 Build 052 | ✔️ ||
| Smash Hit | 1.4.3 | ✔️ ||
| Solid Explorer File Manager | 2.8.16 | ❌ | App crashes |
| Snapchat | | ⚠️ | Camera view is flipped | GMS warnings might appear but these can be safely ignored | 
| Speedtest by Ookla | 4.6.10 (145526) | ⚠️ | VPN does not work ||
| Spotify | 8.6.70.1102 | ⚠️ | The app crashes on first startup, but works second startup upwards |
| Spotify Lite | 1.9.0.2883 | ✔️ ||
| Standoff 2 | 0.16.6 | ⚠️ | Battle experience is terrible, includes micro-stutters |
| Stardew Valley | 1.4.5.151 | ✔️ ||
| State of Survival | 1.13.40 | ✔️ ||
| Steam | 2.3.13 | ✔️ ||
| Steam Chat | 1.0 | ✔️ ||
| Steam Link | 1.1.81 | ❌ | App crashes |
| Subway Surfers | 2.24.2 | ✔️ | Doesn't support keyboard control |
| Sword Art Online: Memory Defrag | 3.0.2 | ✔️ | Keyboard unsupported |
| Tachiyomi | 0.12.3 | ✔️ ||
| TeamViewer | 15.22.136 | ✔️ ||
| Termux | 0.117 | ⚠️ | `packages.termux.org` mirror is the only one that works ||
| TikTok (China) | 18.1.0 | ⚠️ | App crashes on first startup and you might face hiccups logging in |
| TikTok (Global) | 21.6.4 | ⚠️ | Error when trying to log in, you can create a new account |
| TikTok (TV Version) | 1.6.0 | ❌ | App crashes ||
| TikTok Lite | 21.7.1 | ❌ | App crashes ||
| Telegram | 8.1.2 | ✔️ |||
| True Skate | 1.5.39 | ✔️ | Minor graphical glitches ||
| Twitter | 9.16.1-release.00 | ✔️ | Optionally requires GMS ||
| The King Of Fighters Allstar | 1.9.3 | ✔️ | Blank screen / app crash on first boot, works on second boot upwards |
| This War of Mine | 1.0 | ❌ | Infinite loop at starup screen ||
| TP-Link Tapo | 2.4.25 | ✔️ ||
| UC Browser | 13.0.0.1288 (x86) | ✔️ || Avoid updating the app |
| Vanced Manager | 2.6.2 (Crimson) | ✔️ |||
| Vanced MicroG | 0.2.22.212658 | ⚠️ | microG Google sign-in method does not work, hence use Huawei sign-in method to sign in to Google account ||
| Via Browser | 4.3.1 | ✔️ ||
| VLC | 3.4.0 | ✔️ ||
| VK | 6.58 | ✔️ ||
| VooV (腾讯会议国际版) | 2.12.5.504 | ✔️ ||
| Warden | 1.0.3.release | ⚠️ | App screen flashes otherwise functionality-wise its normal |
| WhatsApp | 2.21.20.20 | ⚠️ | WhatsApp cloud chat backups will not work, app was tested with microG installed |
| Word | 16.0.14430.20246 | ✔️ || Might require microG |
| 微博 (Weibo) | 11.10.1 | ⚠️ | Cannot sign in using password, shows limit reached for verification codes |
| 微博国际版 (Weibo International) | 3.9.8 | ⚠️ | Cannot sign in |
| 微博极速版 (Weibo Fast) | 10.9.2 (4620) | ⚠️ | Cannot sign in |
| 文件管理器+ | 2.7.1 | ✔️ ||
| Yahoo! Fantasy Sports | 10.31.0 | ❌ | App crashes on launch |
| YouTube (Google)| 16.40.35 | 🆖 | Requires GMS |
| YouTube Music (Google) | 4.49.51 | 🆖 | Requires GMS |
| Youtube Vanced | 16.29.39 | ⚠️ | Picture-in-picture doesn't work & Can't join channel membership |
| YouTube Music Vanced | 43.9.50 | ✔️ ||
| Yandex.Maps | 10.6.0 | ⚠️ | Map doesn't work |
| Ymusic | 3.7.2 | ✔️ ||
| ZArchiver | 0.9.5.8 (9596) | ✔️ ||
| Zenly (Without Google Services) | 4.55.2 | ⚠️ | App crashes after login, but background location works | 
