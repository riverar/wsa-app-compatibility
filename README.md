## Contributing

Thanks for your interest in contributing! Doing so is simple. Just [edit this page](../../edit/master/README.md) and submit a pull request (PR) with your changes.
Someone will review it and merge it in as soon as possible.

When editing the Markdown, please keep these rules in mind:

1. Do not link to any APKs.
2. Double-check your spelling/grammar.
3. In the Android column, ensure the latest version of Android is listed first. Separate subsequent versions with a comma `,` (e.g. `11`, `12, 11`, or `13, 12, 11`).

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
| IPv6 | ✅ | Loading `ipv6.google.com` in Fennec F-Droid on a PC with IPv6 access, works well
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

## Support tables

* [Apps](#apps)
* [Games](#games)

### Apps
| Application | Latest tested version | Android versions | Support level | Known Issues | Notes |
|-------------|-----------------------|------------------|---------------|--------------|-------|
| 23andMe | 5.114.0 | 11 | ✅ |
| 4PDA | 1.9.35 | 11 | ✅ |
| A+ Gallery | 2.2.55.4 | 11 | ✅ | You might face graphical glitches when using dark theme, hence its recommended to use light theme instead.
| Activity Launcher | 1.14.6 | 13,12 | ⚠️ | As of WSA version 2209.40000.28.0, you can't pin shortcuts to a home area of a launcher (like Lawnchair or Rootless Pixel Launcher) with the error `Current launcher does not support PinShortcut. Unable to create shortcut.` | You can still launch specific activities on any app 
| AdGuard | 3.6.10 | 12 | ⚠️ | "Local VPN" doesn't work even with the above workaround. "HTTPS Filtering" doesn't work due to problems with recognition of manually installed certificates. | Not to be confused with "AdGuard Content Blocker"
| ADM | 12.5.4 | 11 | ✅ |
| ADM Pro | 6.4.0 | 11 | ✅ |
| Aegis | 2.0.2 | 11 | ✅ |
| AIDE | 3.2.210316 | 11 | ✅ || Might optionally require GMS
| AIMP | 3.10.1052 | 11 | ✅
| Aliexpress | 8.58.0 | 12 | ❌ | Crashes on boot, sometimes shows "Oops, something went wrong, please clear app data or reinstall the app." but it never loads
| Amaze File Manager | 3.5.3 | 11 | ✅ || Avoid updating the app
| Amazon Alexa | 2.2.466191.0 | 12 | ✅ |
| Android System Info | 1.4.2 | 11 | ✅ ||
| Android System Webview | 113.0.5672.76 | 13, 12 | ✅ ||
| Android System Webview Dev | 103.0.5060.22 | 11 | ✅ || App installs correctly 
| AniLabX | 3.8.12 (Iridium) - Beta | 11 | ✅
| Animiru | 0.14.2.0 | 13 | ✅ | 
| Aniyomi | 0.12.3.10 | 13, 12 | ✅ |
| AntennaPod | 2.5.0 | 11 | ✅
| APKMirror Installer (Beta) | 1.3.2 | 11 | ⚠️ | Cannot remove ads without subscription which requires Location to be turned on. Apart from this, there are random crashes
| APKPure | 3.17.26 | 11 | ✅ | Sometimes, it might require multiple attempts to install an app
| Apple Music | 3.7.1 | 11 | ✅
| App分享 (AppShare) | 2.1.1 (164) | 11 | ❌ | Can't login
| Aptoide App Store | 9.20.2.1 | 11 | ✅ | Sometimes, downloads might get stuck
| AquaMail (Pro) | 1.34.0-118 | 11 | ✅
| ASUS Router | 1.0.0.7.35 | 12 | ✅ | The text on the bottom bar is more narrow than it should be, resulting in cutting off the last letters or taking up two lines. | 
| AtB | 1.23 | 12 | ❌ | Crashes during loading, as it relies on Google Services Framework and on having the latter be given `read_device_config` permissions, which doesn't seem to be possible to give.
| Audible | 3.15.0 | 11 | ✅
| Aurora Store | 4.1.1 | 12, 11 | ✅
| Authy | 24.8.5 (139) | 11 | ✅ || Produces warnings about GMS which are safe to ignore.
| BandLab | 10.45.0 | 13, 12 | 🆖 | Slight audio lag with Android 12, it was fixed in Microsoft's 2303.40000.3.0 update | Only tested from installing from Google Play Store with Google services, otherwise app has no issues whatsoever. It's responsive, and in Android 13 there's no audio lag. |
| BankID (Norway) | 2.1 | 12 | ❌ | Spams the desktop browser with new tabs about how the app thinks the phone is rooted. 
| BBC iPlayer | 4.137.0.25403 | 11 | ✅ | Sideloaded
| Berry Browser | 3.57.8 | 11, 12 | ✅
| Binance | 2.36.5 | 11 | ✅
| Bondee | 2.0.0.636 | 12 | ⚠️ | Has scaling issues. Specifically, after the introductory part, the app uses abnormally huge elements which makes it impossible to navigate.
| Boost for reddit | 1.12.5 | 12 | ✅
| Bouncer | 1.26.3 | 11 | ⚠️
| Brave Browser | 1.30.87 | 11 | ✅
| BritBox by BBC & ITV | 2.1.2 (20043) | 11 | ❌ | App crashes on start
| Bromite | 94.0.4606.94 | 11 | ✅ || Use x64 build
| CamScanner | 6.3.0.2110240000 | 11 | ❌ | WSA freezes after taking a snap
| Canvas Student | 6.14.1 | 11 | ✅
| ChMate | 0.8.10.153 | 11 | ✅
| Clubhouse | 1.0.11 | 11 | ⚠️ | Unable to login via phone number, it throws error after entering the OTP
| Comixology | 3.10.18.310421 | 11 | ✅
| Cignal Play | 2.2-play | 13 | ⚠️ | Stuck on loading animation when viewing live tv
| Coop Medlem | 3.4.30 | 12 | ⚠️ | Coopay activation fails because the app looks for whether a lockscreen is enabled or not | Core functionality works, although a bit slowly. 
| CPU-Z | 1.41 | 11 | ✅
| Cronometer | 3.13.1 | 11 | ✅
| Cryptography | 1.24.0 | 12 | ✅
| CX File Explorer | 2.0.0 | 13, 12 | ✅
| Dcoder | 4.0.76 | 11 | ✅
| Decibel X | 6.4.2 | 11 | ⚠️ | App crashes
| Decrypto | 1.4.7 | 12 | ✅
| Delivery Club | 4.64.0 | 11 | ❌ | App crashes after selecting a shipping address
| DevCheck | 3.39 | 11 | ❌ | Blank screen on startup
| Device Info HW | 5.4.1 | 11 | ✅
| Deezer | 7.0.14.1 beta | 12 | ✅ | The Deezer Labs crossfade function doesn't seem to work as of September 2022 | Music and menus seem to work pretty well, even with HiFi bitrates.
| Digital Wellness | 1.5.500315346 (471337) | 13 | ✅ | Its not available in the Settings App by default, requires Activity Launcher to launch it. | You can make it show in the launcher if you enable "Show icon on app list".
| DirecTV for Tablet | 5.29.001 | 11 | ⚠️ || Frequent crashing, other functionality proper.
| Discord | 98.6 | 11 | ✅
| DMM Games Store | 2.8.0 | 11 | 🆖 | Requires GMS
| Duolingo | 5.2.35 | 11 | ✅
| DuckDuckGo Privacy Browser+ | 5.142.2 | 12 | ✅
| Easybell | 2.1.30 | 11 | ✅
| EDS Lite | 2.0.0.237 | 12 | ✅ || Tested on an Intel x86-64 CPU (may work on AMD64 or ARM64). Recommended to add the exFAT module if you have a container that use this filesystem.
| Emby | 2.0.48g | 11 | ✅
| ES File Explorer | 4.2.1.8 | 11 | ✅ || Avoid updating the app
| Excel | 16.0.14527.20162 | 11 | ✅
| F-Droid | 1.15.6 | 13, 12, 11 | ✅
| F1 TV | 2.0.5 | 11 | ⚠️ | Terrible app experience including screen flashes and crashes while watching a video
| FaceApp: Face Editor || 11 | ❌
| Facebook | 377.0.0.22.107 | 12 | ✅ | 
| Facebook Lite | 339.0.0.10.100 | 12 | ✅ |
| Facebook Messenger | 330.0.0.12.116 (x86_64) | 11 | ⚠️ | Chat Heads don't work
| Facebook Messenger Lite | 334.0.0.10.101 | ✅ | 
| Fancade | 1.7.6 | 11 | ❌ | App crashes
| FAST Speed Test | 1.0.8 (88) | 11 | ✅
| Fate/Grand Order (US) FGO | 2.34.0 | 12, 11 | 🆖 || Require Google Play Services, skippable if you have Google Play Service (APK) installed
| FDM (Free Download Manager) (Play Store) | 6.18.1.4896 | 13 | ✅ | The app crashed after the splash screen (after granting its needed permissions) on some versions of the subsystem (due to libhoudini). Works fine again as of WSA 2301.40000.7.0 | Tested on an Intel x86_64 CPU
| Fennec F-Droid | 105.1.0 | 12 | ❌ | While the app is correctly installed, it crashes very often, and sites load very, very slowly compared to Firefox Nightly.
| Files by Google | Unknown | 11 | ✅ || Works fine
| Firefox | 113.1.0 (2015950743) | 13, 12, 11 | ✅ | On Android 11, it works albeit with broken rendered webpages. On Android 12, works (without white box after updating WSA to 2205.40000.21.0) | Tested on Intel HD integrated graphics.
| Firefox Nightly | 95.0a1 | 11 | ✅
| Firefox Focus | 106.1 | 12 | ✅
| foobar2000 | 1.2.30 | 11 | ✅
| Formula 1 | 11.0.1533 | 11 | ⚠️ | Live Timing is broken, keeps crashing on initialization
| Google Services Framework (APK) | 12, API 32 | 12 | ❌ | Although installation succeeds and apps become aware of it, it lacks a lot of permissions needed for most functions, e.g. `read_device_config`, which can't be given even with the Settings app.
| Google Translate | 6.45.0.474938783.2-release | 12 | ❌ | Crashes on startup due to reliance on Google Services Framework
| FTP Server (Free) (F-Droid) | 3.1 - 30100 | 13, 12, 11 | ✅ | A network connection is required for the FTP service to initialize.
| FX File Explorer | 9.0.1.2 (r9012) | 13, 12, 11 | ✅ | Tested only on the base version (without FX Plus)
| Game Pass | 2110.17.1005 | 11 | ✅ | GMS warnings might appear but these can be safely ignored | Cloud games can be launched but controlling them with controller or touch has not been tested.
| GBoard | Unknown | 12, 11 | ⚠️ | Will not work as expected in newest WSA (2204.x)
| GCash | 5.62.0 | 13, 12, 11 | 🆖 | Requires GMS. Will warn "limited functionality" if no GMS is present, if present, works normally. When it is launched for the first time, it will crash due to lack of permissions granted on previous version (5.61.0 and below). Starting with 5.62.0, an alert pops up `We have detected that you are running the GCash app on emulator. You will not be able to proceed.` 
| Geekbench |5.4.1| 11 | ✅
| GeoGebra | 5.0.674.0 | 11 | ✅
| Globe2Go | 4.7.4.20.0810/3890 | 11 | ✅
| GlobeOne | 1.8.37 | 12 | ✅ || May require GMS (otherwise use other login methods available in the app)
| Gmail | <sub>2022.05.01.440951655.Release</sub> | 11 | ✅ || May require GMS
| Gojek | 4.30.1 | 11 | 🆖 | Requires GMS
| Google Calendar | 2022.18.2-448173739-release | 11 | ✅ | Requires GMS | Works fine
| Google Camera | Unknown | 11 | ✅ || Works fine
| Google Chrome | 113.0.5672.131 | 13, 12, 11 | ✅ | Requires microG or GMS to sync with Google Account |
| Google Classroom | 8.0.181.20.90.3 | 11 | ✅ || Notifications are generic (do not show content), clicking on them may not open the app. Uploading of attachments locally is not possible.
| Google Contacts | 3.68.0.445910596 | Unknown | ✅ || App may be glitchy from time to time, if that happens, restart the app
| Google Drive | 2.22.197.0.all.alldpi | 11 | ✅ | Works fine, may require GMS
| Google Home | 2.58.1.7 | 12 | ❌ | An error message on startup says "Home cannot run without Google Play Services, which are not supported by your device."
| Google Meet | <sub>2021.10.03.404303734.Release</sub> | 11 | 🆖 | Requires GMS, Share screen doesn't work due to WSA's windowed nature
| Google Photos | 5.91.0.448844219 | 11 | ✅ | Requires GMS |
| Grab | 5.172.200 | 11 | ✅
| Gycso | 1.1.0 | 11, 12 | ✅ |
| HBO Max | 52.15.0.53 | 11 | ⚠️ | Failed to play video (internal player fails to display image and play sound).
| Hidden Settings | 1.7.5 | 12 | ✅
| Hirigana Pro | 1.4.4 | 12 | ✅ | Scaling issue when the app is in landscape mode.
| Hobi | 2.1.7 | 11 | 🆖 | Requires GMS
| Home Assistant | 2022.3.0-full | 11 | ✅ | Basic functionality works, additional / extended functionality has not been yet tested.
| Housesigma Canada Real Estate| 4.3.6 (121) | 11 | ✅
| HTV (hanime tv) | 3.6.7 | 11 | ⚠️ | Failed to play video | Internal player don't work, asks for external player and fails again
| huaCtrl PRO | 1.0.27 | 11 | ✅
| Huawei AppGallery | 11.4.2.300 | 11 | ✅ | Frequent crashes were experienced, otherwise the app functionality is fine
| Hyper Square | 3.0.1 | 11 | ✅
| IFTTT | 4.29.2 | 12 | 🆖 | Need GMS to receive notification. Ignore the Notification Reader Access error. | To avoid Play Protect blocking login to the Google Store, use GMS version open_gapps-x86_64-11.0-pico-20220215. (See also: WSAGAScript issue #213). 
| Instagram | 244.0.0.17.110 | 12, 11 | ⚠️ || Need to use an Android keyboard (eg. MS SwiftKey) to be able to reply stories (only works in 11. Keyboard app support in 12 is broken.
| Instagram Lite | 339.0.0.10.100 | 12 | ✅ 
| Intra | 1.3.8 | 12 | ✅ || VPN workaround is needed once after installation to allow the app to create VPN connections.
| iOS app (any) || 11 | ❌ | Thanks for testing, Brad.
| Ipsos MediaLink | 5.2.20 | 13 | ✅ || The VPN workaround is required, as are Accessibility permissions, and a CA certificate needs installing (wsa://com.android.settings) 
| iPusnas | 1.5.1 | 11 | ✅
| iRobot | 5.2.4-release | 12 | ❌ | Error message `java.lang.UnsatisfiedLinkError: dlopen failed: library "libcore_jni.so" not found`
| JAKI - Jakarta Kini | 1.2.34 | 11 | 🆖 | Some features require GMS
|JioSaavn | 8.2.1 | 11 | ✅ |Doesn't support fullscreen and rare crashes but running fine
|Jiocinema| 3.0.2.7 | 11 | ✅ | May crash initially but subsequent runs should work correctly. 
| Jlpt | 4.7 | 12 | ✅ ||
| Joey (Reddit client) | 2.0.0.1 | 11 | ✅
| Joplin | 2.4.3 (2097651) | 11 | ✅
| JuiceSSH | 3.2.2 | 11 | ⚠️ | Connecting to SSH server needs multiple tries
| Kahoot || 11 | ✅
| Katakana Pro | 1.4.4 | 12 |  ✅
| KawaiiNihongo | 3.10.9 | 12 |  ✅
| Khan Academy | 7.3.3 | 11 | ✅
| Kik | 7.10.1.176 (82) | 11 | ✅
| Kindle | 8.47.1.3370 | 11 | ✅
| Kiwi Browser | 107.0.5304.74 | 12,13 | ✅ |
| Kobo Books | 8.40.29843 | 11 | ⚠️ | Aspect ratio and resolution are fixed, appears blurry when resized
| KRL Access | 4.1.0 | 11 | ❌ | App crashes
| Kotatsu | 4.4.4 | 13 | ✅ | | Keyboard navigation is supported
| Lawnchair | 11.0 Alpha 6.1 (8b01af8).release | 11 | ❌ | App crashes
| Lawnchair | 12 Alpha 5 | 13, 12, 11 | ⚠️ | If your running the Android 13 of the subsystem (2211.40000.11.0), if you launch any app from either the home screen or the app drawer, it crashes with an error: `java.lang.NoSuchMethodError: No virtual method setSplashscreen(I)V in class Landroid/app/ActivityOptions; or is superclasses (declaration of 'android.app.ActivityOption'...` | Works fine on Android 11 or 12 versions of the subsystem.
| Lazada | 7.19.1 | 13 | ⚠️ | Google login requires GMS installed (use Email or Facebook login as alternatives). `Slide to verify` appear too often if logging in. Weird scaling options (interface elements are too large) | Keep it in portrait for the app to be usable.
| Libby | 4.3.1 | 11 | ✅
| LINE | 12.0.1 | 11 | ✅
| Line Rangers | 7.6.3 | 11 | ✅
| LinkedIn | 4.1.632 | 11 | ✅
| LNReader | 1.1.12 | 12 | ✅|| Partial keyboard navigation is available (example: arrows key up and down - scrolls) when reading light novel.
| LSPosed | 1.8.6 | 11, 13 | ✅
| Magisk | 25.2 | 11, 13 | ✅ || Magisk developer confirmed able to gain root access - [link to his tweet](https://twitter.com/topjohnwu/status/1451282578514735131)
| ManCityApp | 2.1.11 | 11 | 🆖 || Might require GMS
| Manzur's Study Circle (MSC) | 1.0.2 | 11 | ✅
| Material Files | 1.5.2 | 12, 11 | ✅
| Maya (Paymaya) | 2.85.1 | 13 | ❌ | App crashes immediately upon launching the app 
| Meta Quest (Oculus) | 181.1.0.81.114 | 12 | ⚠️ | Can't log in with a Meta account, but you can install the Facebook or Instagram app and enable "Logging in with accounts" in the Meta Accounts Center, and use the in-app login. Doesn't detects Quest 2 nearby, due to no Bluetooth support.
| microG Settings | N/A | 11 | ❌ | App crashes, doesn't load
| Microsoft Authenticator | 6.2112.8213 | 11 | ✅ || Some features might require GMS
| Microsoft Azure | 3.9.2.2021.09.30-19.35.50 | 11 | ✅
| Microsoft Bing - Search & earn | 23.5.401109307 | 12 | ✅
| Microsoft Edge | 95.0.1020.42 | 11 | ❌ | App frequently crashes
| Microsoft Edge Canary | 103.0.1264.1 | 11 | ❌ || Fails to load websites
| Microsoft Launcher | 6.210602.1.994630 | 11 | ✅
| Microsoft PowerApps | 3.21124.20 | 11 | ✅
| Microsoft Swiftkey Keyboard | 8.10.12.4 | 12, 11 | ✅ | Works on WSA 2203 (Android 11), but on-screen is completely broken in WSA 2204(Dev) (Android 12.1)
| Microsoft Teams | 1416/1.0.0 | 12 | ✅
| Mic Test | 5.2 | 12 | ✅ || lauresprojects.com.mictest
| MiX | 6.57.0-Beta_B21070510 | 11 | ✅
| Mobile JKN | 3.7.1 | 11 | ✅ || Some features might require GMS
| Mobile Legends | 1.6.66.7281 | 11 | ✅
| MOLA | 2.1.3 | 11 | ❌ | App crashes
| Monogolf | 3.4.10 | 13 | ✅ | 
| Monument Browser | 1.0.333 | 12 | ✅
| Moodle | 3.9.5 | 11 | ✅ 
| MPV | 2022-07-30-release | 12 | ✅ ||Keyboard navigation supported in the media player
| MT File Manager | 2.10.0 | 11 | ✅
| Musically (TikTok) | 7.8.0 | 11 | ✅
| Muslim Pro | 1.2.3 | 11 | 🆖 | Requires GMS
| MX Player | 1.40.9 | 11 | ✅
| MX Player Pro | 1.39.13 | 11 | ⚠️ | App crashes, but videos can be played from external sources
| MyPostNord (Norway) | 3.12 | 12 | ✅ 
| My Verizon | 16.4.2 | 11 | ✅ || The page might be displayed sideways for a short amount of time when the app is launched. The app automatically reverts to correct orientation in a second.
| Neko | 2.13.2 | 13, 12, 11 | ✅
| Nekogram X | 8.1.2-1-rc01 | 11 | ✅ || Use NoGcm variant
| Netflix (Aurora Store) | 8.4.0 | 11 | ❌ | "Device not supported" error
| Nettfart Mobile | 3.6.8 | 12 | ✅ | The app must be given network permissions in App Settings
| Network IP Scanner | 3.2 | 11 | ⚠️ | Only scans WSA's own VirtWifi network
| NewPipe | 0.22.1 | 11 | ✅
| NextDNS | 1.2 | 12 | ✅ || VPN workaround is needed once after installation, to allow the app to create VPN connections.
| NFL | 57.0.7 | 11 | ⚠️ | Videos/streams do not play or load. If embedded in an article, they only play without sound.
| Nintendo Switch Online | 2.2.0 | 12 | ✅ | Only displays in portrait 
| Nova Launcher | 7.0.49 (7049) | 11 | ⚠️ | UI is messy, but app drawer is fine
| Nova Launcher Beta | 8.0.2 | 12 | ⚠️ | UI is messy, but app drawer is fine
| Nu Carnival | 1.0.2-erolabs | 11 | ❌ | App stuck on a black screen
| Octopath Traveler: Champions of the Continent (CotC) | 1.5.0 (753410) | 12 | ❌ | OpenGL ES 3.1 (or higher) is unsupported | Security policy violation: 32  (Most likely due to OpenGL issue)
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
| Oss (Norway) | 2.9.2 | 12 | ❌ | Crashes on startup. The error log shows `java.lang.UnsatisfiedLinkError: couldn't find DSO to load: libhermes.so`
| Oto Music | 3.0.2 | 11 | ✅ || Requires app restart to refresh list
| OTT Navigator | 1.6.7.7 | ❌ | Crashes on video playback
| OurGroceries | 4.0.10 | 11 | ✅ | Premium keys require Google Play Store
| Outlook | 4.2138.0 | 11 | ⚠️ | Cannot activate device administrator with Outlook, which prevents activation.
| Package Manager | 6.7 | 12 | ✅ ||Recommeded with use of Shizuku for multi-app installation
| Phigros || 11 | ✅
| Philips Hue | 4.29.0 | 12 | ✅ 
| Pixel People | 4.7 | 11 | ✅ | Changing window size breaks the game. Runs at low FPS but is still playable.
| Playstation App | 21.11.2 | 11 | ⚠️ | Runs very slow and takes some time to connect to voice chat, beside that it works  
| Plex | 8.26.2.29389 | 11 | ✅
| Plex Dash | 1.1.1 | 11 | ❌ | App crashes after splash screen
| Plexamp | 3.8.2 | 11 | ⚠️ | Layout and app orientation issues
| Pocket | 7.56.0.0 | 11 | ⚠️ | Unable to log in with a Firefox account, instant (push) syncing is unavailable
| Polar Flow | 6.12.0 | 12 | ✅ | Not able to sync via Bluetooth since WSA doesn't support it. | Syncing via web and interaction is otherwise fine.
| PornHub || 11 | ✅
| Posten (Norway) | 5.16.4 | 12 | ❌ | If installed through the APKPure app, it crashes after the splash screen. If trying to install a locally downloaded XAPK over ADB that simply had its file extension changed to `.apk`, the error message `Failure [INSTALL_PARSE_FAILED_UNEXPECTED_EXCEPTION: Failed to parse /data/app/vmdl1025447652.tmp/base.apk: AndroidManifest.xml]` shows up.
| PostNord | 8.22.2 | 12 | ⚠️ | On the "Verify mobile number" page, keyboard key presses are not recognised, making it impossible to verify phone numbers.
| PowerPoint | 16.0.14527.20162 | 11 | ✅ | Might require GMS / MicroG
| Prep Ladder | 2.0.79-p | 11 | ⚠️ | Video pane opens but no audio or video and time keeps on going
| Pydroid | 5.00_x86_64 | 11 | ✅
| Q-Dance | 8.0.7 | 11 | ❌ | App crashes
| QooApp | 8.3.3 | 11 | ✅
| QPython 3L | 3.0.0 | 11 | ✅
| QQ | 8.9.28 | 13, 12 | ❌ | App crashes
| Reddit || 11 | ✅
| Relay | 10.0.378 | 11 | ✅
| Remini - AI Photo Enhancer || 11 | ⚠️ | Oops! Something went wrong Your image didn't save. Please try again.
| Remote Desktop (Microsoft) | 10.0.12.1148 | 11 | ✅
| Rider | 1.59 | 11 | ✅
| Robinhood - Food & Booking | 2.2.2 | 12 | ⚠️ | App having trouble loading content. Maps & Location picker don't work (Requires GMS). | You can log-in only on one device at the same time. Previous device will log-out upon signing-in on new device.
| Rootless Launcher | 3.9.1 | 11 | ❌ | App crashes
| Rootless Pixel Launcher | 3.9.1 | 13 | ✅ |
| Ruler (F-Droid) | 1.1 | 12 | ❌ | While the app is correctly installed, the ruler lengths are wildly off-course no matter how much in-app calibration is done. | The app also refuse to recognise values above circa 100mm for the 70mm calibration line.
| Saikou β (Beta) | 1.2.1.0 | 13, 12 | ✅ || Some keyboard functionality is somewhat limited but usable (both media playback and manga reading)
| SAI (Split APKs Installer) (Play Store) | 4.5 | 12 | ✅ || Used rootless method only, not yet tested for rooted WSA
| SAI (Split APKs Installer) (F-Droid) | 4.5 | 12 | ✅ || Used rootless method only, not yet tested for rooted WSA
| SATRIA | 1.0.0 | 11 | ❌ | Needs fingerprint reader support
| SD Maid (pro) | 5.2.2 | 11 | ⚠️ | Unable to grant external storage privileges, can be skipped
| Settings | 12, API 32 | 12 | ⚠️ | Setting screenlock to "Swipe", makes it impossible to use any apps without re-installing the entire Subsystem, since no method is provided on the lockscreen to swipe or otherwise unlock. Adding a Google account in the Account menu doesn't work. "Backup" and "SOS Alarm" sends the phone back to the main Settings menu. | Included by default in Subsystem. Accessed by creating a Windows shortcut with this path: `%LOCALAPPDATA%\Microsoft\WindowsApps\MicrosoftCorporationII.WindowsSubsystemForAndroid_8wekyb3d8bbwe\WsaClient.exe /launch wsa://com.android.settings`
| Shazam | 13.19.0-230223 | 13, 12 | ✅ | Shazam on pop-up doesn't work | Requires microphone for song identification
| ShemarooMe | 1.0.16 (106) | 11 | ✅
| Shizuku | 13.2.1.r958.5f9516b | 13, 12,11 | ⚠️ | Can't toggle wireless debugging in WSA 2207.40000.8.0 (android 12), use ADB on PC to use connect instead (even with dev options and USB debugging is on).
| Shopee PH | 2.98.30 | 13,11 | ✅ | Google login requires GMS installed (use Email or Facebook login as alternatives). Banner information are stretched horizontally 
| Shosetsu | 2.0.0-2417 | 13, 12 | ✅ | Keyboard navigation is unsupported when reading light novel.
| Showtime | 3.1.1 | 11 | ❌ | App crashes when you try to login. Button clicks dont work
| SIM Toolkit (Google) | 12, API 32 | 12 | ❌ | Does not launch even with a shortcut.
| Simple Gallery | 5.3.9 | 11 | ❌ | App crashes when you try to view a photo
| Sky Map | 1.10.0 - RC3 | 11 | 🆖 | Complains about missing accelerometer controls, requires GMS
| Skype | 8.91.0.406 | 12 | ✅
| SkySafari | 6.8.6.15 | 11 | 🆖 | Failed license check on startup, appears to require GMS
| Slack | 21.11.20.0-B | 11 | ✅
| Smart Launcher | 5.5 Build 052 | 11 | ✅
| Smart Life | 3.32.5 | 11 | ❌ | The app is producing constant flashes between light and dark mode, and the UI element of agreement pop-up is moving on screen so it can't be accepted
| Smash Hit | 1.4.3 | 13 | ✅ |
| Snapchat || 11 | ⚠️ | Camera view is flipped | GMS warnings might appear but these can be safely ignored
| Solid Explorer File Manager | 2.8.28b | 12 | ✅
| SoundHound | 10.1.2 | 12 | ✅ |  | Ensure in Windows' audio settings that the microphone has a high enough sound level 
| Speedtest by Ookla | 4.8.0 (177906) | 12 | ✅ | VPN workaround is needed once after installation, to allow the app to create VPN connections.
| Spotify | 8.7.30.1221 | 12, 11 | ✅ | 
| Spotify Lite | 1.9.0.2883 | 11 | ✅
| Squircle IDE | v2022.1.2 | 12, 11 | ✅
| Steam | 2.3.13 | 11 | ✅
| Steam Chat | 1.0 | 11 | ✅
| Steam Link | 1.1.81 | 11 | ❌ | App crashes
| Stocard | 10.12.1 | 12 | ✅ |  | To log in to an earlier Stocard account that is set to use Google login, it needs to be transitioned from a Google-based account to an E-mail-based account, which has to be done on a phone.
| SwiFTP Server| 1.24 | 11 | ✅
| Symbolab | 9.3.0 | 11 | ✅ || Keyboard not working, in-app keyboard is available though
| Sync for Reddit Pro | 20.0.3 | 11 | ✅
| Tachiyomi (Preview) | 0.14.6-5796 | 13, 12, 11 | ✅ | The notification about "Large updates harm sources..." cut off. Sometimes, "Updating Library" progress bar doesn't show, requires to clear the Tachiyomi notification.
| Tachiyomi (Release) | 0.14.6 | 13, 12, 11 | ✅ | The notification about "Large updates harm sources..." cut off. Sometimes, "Updating Library" progress bar doesn't show, requires to clear the Tachiyomi notification.
| TachiyomiAZ | 8.7.4-AZ | 13, 12, 11 | ✅
| TachiyomiJ2K/TachiJ2K | 1.6.6 | 13, 12, 11 | ✅ | Parsing links (from a browser) causes to open the Tachiyomi extension window or app picker dialog instead of opening TachiJ2K itself.
| TachiyomiSY | 1.9.3 | 13, 12, 11 | ✅
| Tap Tap | 3.1.1 | 12, 11 | ✅ | Sometimes freeze if you brute force the app, fixed by restarting the app
| Teamfight Tactics | 12.5.4259171 | 11 | ⚠️ | Crashes often before getting in game but after getting in, not many issues. Can get laggy at times but somewhat playable.
| TeamViewer | 15.22.136 | 11 | ✅
| Telegram | 8.1.2 | 11 | ✅
| Televizo | 1.9.0.1 | 11 | ❌ | Crashes on video playback
| Terminal Emulator for Android | 1.0.70-rebuild | 12 | ✅ | A warning shows up about the app being designed for older Android versions, but can be dismissed
| Termux (F-droid) | 0.118.0 | 12, 11 |✅
| Tesla | 4.6.1 | 11 | ⚠️ | Vehicle graphics and maps do not load, cannot enable phone key. | Internet-based vehicle controls, charge stats, services are functional.
| The Globe and Mail | 6.2.0 (100) | 11 | ✅
| TIDAL | 2.49.0 | 11 | ✅
| TikTok (China) | 18.1.0 | 11 | ⚠️ | App crashes on first startup and you might face hiccups logging in
| TikTok (Global) | 25.0.3 | 11, 12 | ✅
| TikTok (TV Version) | 1.6.0 | 11 | ❌ | App crashes
| TikTok Lite | 21.7.1 | 11 | ❌ | App crashes
| Tivimate | 4.4.0 | 11 | ✅ |   Compatibility Options -> Force App to be non-resizeable ; Disable smooth resize ; Keyboard Compatibility ;ForceFullScreen [F11] Note: Version 4.5. And above force crashes, the latest working version remains 4.4.0
| TP-Link Tapo | 2.4.25 | 11 | ✅
| Trello | 2021.14.1.16332-production | 11 | ⚠️ | Login needs web browser installed in WSA, using Windows' default browser will not work
| Trust: Crypto & Bitcoin Wallet | 6.57.1 | 12 | ✅ || for login, you have to go to Android settings => System => Date & Time and toggle the "Set Time Automatically" option. you can access it by this comman .\adb.exe shell "am start -n com.android.settings/.Settings"
| Tune In Pro | 28.7 (267721) | 11 | ✅
| Twitter | 9.16.1-release.00 | 11 | ✅ | Optionally requires GMS
| Twitter Lite | 3.1.1 | 12 | ✅ ||
| UC Browser | 13.0.0.1288 (x86) | 11 | ✅ || Avoid updating the app
| Uptodown App Store | 4.35 | 11 | ⚠️ | Keeps "analyzing device" on app details page, thus its unable to download APKs.
| Vanced Manager | 2.6.2 (Crimson) | 11 | ✅
| Vanced MicroG | 0.2.22.212658 | 11 | ⚠️ | microG Google sign-in method does not work, hence use Huawei sign-in method to sign in to Google account
| Via Browser | 4.3.1 | 11 | ✅
| Viaplay | 5.48 | 12 | ✅ |  | Episode playback of at least Nella the Princess Knight works correctly, as do the phone-app-exclusive download functionality.
| Vidio | 5.64.5-f0aa483a3d | 11 | 🆖 || Might require GMS for login
| Vipps | 2.142.0 | 12 | ❌ | Shows an error message about requiring "Google Services", even if both Google Play Services and Google Services Framework APKs are installed
| Vivaldi Browser | 4.3.2439.61 | 11 | ✅
| VK | 6.58 | 11 | ✅
| VLC | 3.5.3 | 12, 11 | ✅ || Keyboard supported in media player
| Voice Recorder | 55.1 | 12 | ✅ || com.media.bestrecorder.audiorecorder
| VSCO | 264 | 11 | ⚠️ | Cannot sign in
| Warden | 1.0.3.release | 11 | ⚠️ | App screen flashes otherwise functionality-wise its normal
| Wealthsimple Trade | 2.27.1 (2195) | 11 | ✅
| WeChat | 8.0.32 | 13, 12 | ✅
| WhatsApp | 2.21.20.20 | 11 | ⚠️ | WhatsApp cloud chat backups will not work, app was tested with microG installed
| Word | 16.0.14430.20246 | 11 | ✅ || Might require microG
| Wulkanowy (F-Droid) | 1.4.3 | 11 | ✅
| Wulkanowy (Play Store) | 1.4.3 | 11 | 🆖
| Wyze | 2.30.0 | 11 | ✅
| Xbox Game Pass (Beta) | 2212.51 | 12 | ✅|| Everything works in this app, tested Cloud Gaming on Windows 11 build 25236 and WSA 2209.400. connected my Xbox Series X controller to PC and the app worked perfectly with it.
| Xbox Game Pass | 2211.42 | 12 | ✅|| Everything works in this app, tested Cloud Gaming on Windows 11 build 25236 and WSA 2209.400. connected my Xbox Series X controller to PC and the app worked perfectly with it.
| Xbox Family Settings | 20221104 | 12 | ✅
| Xbox Beta | 2211.2.7 | 12 | ✅
| Xbox | 2211.1.4 | 12 | ✅
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
| Æ | 2.0.7 | 12 | ✅ | Adding debit cards requires Vipps, an app that is shown above in this list as not working. | 
| 哔哩哔哩 (Bilibili) || 11 | ✅
| 酷安 (CoolApk) | 11.4.3 | 11 | ⚠️ | Unable to sign in using third party apps
| 创建快捷方式 (Create Shortcut) | 1.17 | 11 | ✅ || Can be used to access any app
| মুনাজাতে মাকবূল ও মাসনূন দু'আ - Munajate Makbul | 1.0 | 11 | ✅
| 九黎 | 1.3.5.01 | 11 | ❌ | App crashes
| 米游社 (mihoyo Chinese Community) | 2.14.1 | 11 | ⚠️ | The app might lag when inserting a photo into a new post
| СберБанк (SberBank) | 12.9.0 | 11 | ✅
| Тинькофф (Tinkoff Bank) | 5.20.0 | 11 | ✅
| (腾讯会议国际版) VooV | 2.12.5.504 | 11 | ✅
| 微博 (Weibo) | 11.10.1 | 11 | ⚠️ | Cannot sign in using password, shows limit reached for verification codes
| 微博国际版 (Weibo International) | 3.9.8 | 11 | ⚠️ | Cannot sign in
| 微博极速版 (Weibo Fast) | 10.9.2 (4620) | 11 | ⚠️ | Cannot sign in
| 文件管理器+ | 2.7.1 | 11 | ✅
| 超星学习通 | 4.6.1 | 11 | ✅
| 超星学习通 | 5.0.3 | 11 | ❌ | Crashes on startup

### Games

| Game | Latest tested version | Android versions | Support level | Known Issues | Notes |
|-------------|-----------------------|------------------|---------------|--------------|-------|
| 2 3 4 Player Games | 3.8.8 | 12 | ✅ || Touchscreen is recommended for the Team vs. Team maches or some of the driving games
| 8 ball pool | 5.5.6 | 11 | ✅ |
| A Dance of Fire and Ice | 1.15.5 | 11 | ✅ || Keyboard supported
| AFK Arena | 1.72.01 | 11 | ⚠️ | Can't login using Google account
| Alan Walker-The Aviation Game | 3.0.6 | 11 | ✅ || Touchscreen and cursor works; keyboard doesn't work
| Alien: Blackout | 2.0 | 11 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS
| Alto's Adventure | 1.8.0 | 11 | ✅
| Alto's Odyssey | 1.0.10 | 11 | ✅
| Among Us | 2022.7.12 | 12, 11 | ✅ | Keyboard may be unresponsive. | Xbox controller works.
| Angry Birds Epic | 3.0.27463.4821 | 11 | ⚠️ | Terrible in-game experience, bad performance and low FPS
| Animal Crossing: Pocket Camp | 5.0.2 | 12 | ❌ | error 802-1-01a-069-008 ||
| Archero | 4.8.2 | 12 | ✅ | Requires GMS and Play Games to load your cloud progress
| Arknights | 10.0.01 | 12, 11 | 🆖 | Can't login using Google account. Unstable FPS throught the game, especially low FPS in combat for AMD system PC. Stable FPS throughout the game using NVIDIA GeForce GTX 1050 Ti Mobile
| Arknights (明日方舟; Simplified Chinese) | 1.6.01 | 11 | ✅
| Arknights (CN Server) | 1.9.21 | 12 | ✅
| Asphalt 8 | 6.3.1a | 12 | ✅ | Keyboard supported in latest version (2206)
| Asphalt 9 || 11 | ⚠️ | Keyboard unsupported
| Azur Lane | 6.1.2 | 12, 11 | ⚠️ | Sometimes stuck on downloading resources, can be fixed by restarting the app. Overall gameplay, got stable FPS using NVIDIA GeForce GTX 1050 Ti Mobile
| Bad Piggies HD | 2.4.3141 | 11 | ✅
| BanG Dream! Girls Band Party! | 4.5.0 | 11 | 🆖 | Requires GMS
| Arcaea | 3.8.8 | 11 | ⚠️ | Keyboard doesn't work on login/register form
| Battle Cats Quest | 1.0.4 | 11 | ✅
| C.A.T.S (Crash Arena Turbo Stars) | 2.40.2 | 11 | ✅ | GMS warnings might appear but these can be safely ignored
| CarX Highway Racing | 1.17.1 | 11 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS
| Command and Conquer: Rivals | 1.8.1 | 12, 11 | ✅ | | It will pop up "Won't run without GPlay services" when starts, but works fine except GPlay login. You may use link email instead.
| Endless Frontier - Idle RPG | 3.5.3 | 12 | ❌ | OpenGL ES 3.1 is unsupported
| Epic Seven | 1.0.406 | 11 | ⚠️ | Low FPS, unable to sign in with Google
| Blue Archive (GB) | 1.41.164236  | 12, 11 | ❌ | crashed when trying to log in/enter game
| Blue Archive (ブルーアーカイブ; JP) | 1.21.156614 | 12 | ❌ | Black screen on app launch
| Blue Archive (KR) | 1.39.146794 | 12, 11| ❌ | HEVC codec support required
| Blue Archive (KR, Onestore distributed) | 1.50.203922 | 13 | ✅ | Does not work with nvidia graphics
| Brawl Stars | 38.159 | 11 | ❌ | Game crashes
| Candy Crush Saga | 1.213.2.1 (12132011) | 11 | ✅
| Clash Mini | 1.1142.10 | 11 | ❌ | App crashes
| Clash of Clans | 15.292.12 | 13 | ❌ | App crashes
| Clash Royale | 3.6.1 | 11 | ❌ | App crashes
| Clouds & Sheep 2 | 1.4.6 | 11 | ✅ | Optionally uses GMS
| Crazy Taxi Classic | 4.7 | 12 | ❌ | An error message on startup says "Download failed because the resources could not be found." | OBB installation has not yet been tested.
| Deus Ex GO | 2.1.111374 | 11 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS
| Destiny Child | 2.8.6 | 11 | ⚠️ | Poor performance during battles
| Dwarf Balls | 3.5.2 | 11 | 🆖 | Requires GMS for Google Play login.
| Extreme Car Driving Simulator | 6.74.0 | 13, 12, 11 | ✅ | Keyboard & controller supported
| Fire Emblem Heroes | 6.7.0 | 12, 11 | 🆖 | Requires GMS. If GMS is installed, it cannot be played due to SafetyNet error.
| Fortnite | 14.10.0 | 11 | ❌ | Crashes at login screen
| Fortnite Installer | 4.1.4 | 11 | ❌ | "Device not supported" error
| Fruit Ninja | 3.3.4 | 11 | ✅ | Version check error | Otherwise, other app functionality is fine
| Game Dev Story | 2.47 | 11 | ❌ | App can start but with infinite "loading" screen
| Garage: Bad Dream Adventure | 1.0.191 | 11 | ⚠️ | Stuck after start of Chapter 1
| Geometry Dash | 2.11 | 11 | ✅ | If you use high refresh rate monitor, there is a small period where the game speeds up before the level plays for the first time and the audio will get desynced. You can simply pause and resume or die once to fix it since it won't happen on second attempt.
| Girls' Frontline (EN) | 2.0900_375 | 12, 11 | ⚠️ || Sometimes freeze while downloading resources, fixed by restarting the app
| Golf Rival | 2.54.241 (88) | 11 | 🆖 | Requires GMS | Produces warnings about GMS. Issues include not being able to pan.
| Grand Theft Auto: San Andreas || 11 | ✅
| Guardian Tales | 2.53.1 | 12, 11 | 🆖 | Requires GMS
| Hatsune Miku: Colorful Stage! | 1.3.2 | 11, 12 | ❌ | App either crashes when loading into game after login or app screen turns dark
| Hay Day | 1.55.93 (1706) | 1 | ❌ | App crashes on startup (Worked on 1.54.71 and earlier)
| Hill Climb Racing | 1.53.0 (501) | 11 | ✅
| Hitman Sniper | 1.7.193827 | 11 | ⚠️ | Terrible in-game experience, includes poor performance and low FPS
| Honkai Impact 3rd| 5.1.0 | 11 | ⚠️ | Poor graphics quality
| Hungry Shark Evolution || 11 | ✅
| iDOLM@STER Million Live! Theater Days | 4.0.401 | 11 | ⚠️ | Anything 3D with a moving background is broken, but everything 2D works perfectly | ARMv7 version is unusably slow, get ARM64
| Jet Car Stunts 2 | 1.0.13 | 11 | ❌ | Loads up but orientation and menus are broken
| Jetpack Joyride | 1.52.1 (58461800) | 11 | ⚠️ | Google Play Games sync doesn't work, otherwise the game functionality is fine
| KINGDOM HEARTS Uχ Dark Road | 4.4.0 (Offline) | 11 | ✅ | GMS warnings might appear but these can be safely ignored
| King of Thieves | 2.57.1 | ✅
| Konosuba:FD | 1.12.1 | 11 | 🆖 | Requires GMS
| Last Day On Earth: Survival || 11 | 🆖 | Might require GMS
| League of Legends: Wild Rift || 11 | ✅
| LIMBO Demo | 1.20 | 11 | ✅
| Love Live! All Stars | 3.6.0 | 12 | ⚠️ | Requires GMS, Hovers around 20-30 FPS with stuttering and slowdown on taps, requires root access and disabling SELinux. | Tested on a Ryzen 5 5600X and Nvidia RTX 3060 Ti
| Magic Tiles 3 | 8.086.201 | 11 | ✅
| MapleStory M | 1.7000.2835 | 11 | ❌ |Crashes at loading screen
| Mario Kart Tour | 2.10.0 | 11 | ❌ | Fails to connect to servers after Nintendo login
| Minecraft (Aurora Store) | 1.17.40.06 | 11 | ❌ | Unable to verify game owner
| Minecraft (China Edition) || 11 | ✅
| Minecraft (Play Store) | 1.18.0.23 | 11 | ✅
| Monument Valley | 2.7.17 | 11 | ✅
| Monument Valley 2 | 2.0.3 | 11 | ✅
| Mortal Kombat X (APKPure) | 5.9.0 | 11 | ❌ | Stuck on initialization screen, message shows up saying "Download failed to start"
| My Little Pony World | 2022.2.0 aarch64 | 12 | ⚠️ | An authentication error warning about not being signed in with Google shows up on boot, but can be clicked past. The game is heavily graphically demanding on an x64 PC, averaging 15fps with an Nvidia 1050Ti.
| My Talking Angela 2 (Play Store) | 2.2.4.2167 (ARM64_v8a) | 13 | ⚠️ | Does not resize into window, even when the "Resize" botton (on bottom right) is clicked on. Bug in Angela's tub (go to Bathroom -> Tub): When grabbing the soap to massage on Angela, the shower head briefly appears, then disappears in 1 second. | 
| NieR Re[in]carnation | 2.17.0 | 13, 12, 11 | 🆖 | Requires GMS to get past loading screen. If GMS is installed, terrible in-game experience, includes poor performance and low FPS. | Tested on a Ryzen 9 5900X and Nvidia RTX 3080
| New Star Soccer | 4.27 | 13, 12, 11 | ✅ | Keyboard not supported
| osu!lazer | 2023.403.1 | 5-13 | ⚠️ | Runs with terrible performance, high latency, generally unplayable
| Penguin Isle | 1.59.1 | 5-13 | ✅ | Great performance, but UI size breaks with weird resolutions.
| Plants vs Zombies 2 | 9.2.2 | 11 | ✅ | Cloud save using Google Play Games works if GMS is available
| Pojav Launcher | dahlia-209 | 12 | ✅ | Performance was great with an i7-10700K and a RTX 3060 Ti, but will probably be worse on lower hardware.
| Pokémon GO || 12, 11 | ❌ | This device, OS, or software is not compatible
| Pokémon Masters EX | 2.19.0 | 11 | ❌ | 10102 An error has occured.
| Pokémon Unite | 1.2.1.2 | 11 | ⚠️ | Battle experience is terrible
| Pou | 1.4.84 | 11 | ✅
| Princess Connect! Re: Dive (Korean) | 5.6.1 | 12 | ❌ | Only touch effect works after displaying the publisher logo
| Princess Connect! Re: Dive (Japanese) | 6.7.0 | 12 | ❌ | Only touch effect works after displaying the publisher logo
| Princess Connect! Re: Dive (Simplified Chinese) | 4.9.6 | 12 | ❌ | Only touch effect works after displaying "loading..."
| Princess Connect! Re: Dive (Traditional Chinese) | 2.9.0 | 11 | ⚠️ | Battle experience is terrible, cannot sync with Google Play Games
| Princess Connect! Re: Dive (Global) | 4.4.1 | 12 | ❌ | Only touch effect works after displaying the publisher logo
| Ragnarok M: Eternal Love EU | 1.0.70 | 11 | ✅
| Rayman Adventures | 3.9.95 ARMv7 | 12 | ✅ | Gameplay speed is tied to framerate, and even an Nvidia 1050Ti occasionally get slowdowns in the ARM version. | The game works well without major problems. The x86_64 version was discontinued after 3.9.0 and is no longer able to download game assets on first launch. Xbox Series controller works both with Bluetooth and USB, but only during levels.
| Rayman Classic | 1.0.1 | 11 | ✅
| Real Racing 3 | 10.1.0 | 12, 11 | ✅ | Only controller is supported. keyboard doesn't work
| RFS - Real Flight Simulator | 1.6.1 | 12.1 | ⚠️ | Does not work with keyboard | Works only by connecting a controller or on PCs with touch
| Roblox | 2.499.381 | 11 | ⚠️ | Graphical anomalies | GMS warnings might appear but these can be safely ignored
| Rocket League Sideswipe | 1.0 (356721) | 11 | ❌ | OpenGL ES 3.1 is unsupported
| Shadow Fight 2 | 2.16.0 | 11 | ⚠️ | Optionally uses GMS, Doesn't support keyboard control makes fighting more harder | GMS warnings might appear but these can be safely ignored, Cloud save requires GMS
| Shadow Fight 3 | 1.25.7 | 11 | ✅ | Optionally uses GMS, Cloud save using Facebook not working | Keyboard control are supported uses (W A D X) to use analog, GMS warnings might appear but these can be safely ignored, Cloud save requires GMS
| Sky: Children of the Light | 0.15.1 | 11 | ❌ | OpenGL ES 3.1, Vulkan 1.0.3 and Vulkan level 0 missing
| Smash Hit | 1.4.3 | 11 | ✅
| Standoff 2 | 0.16.6 | 11 | ⚠️ | Battle experience is terrible, includes micro-stutters
| Stardew Valley | 1.4.5.151 | 11 | ✅
| State of Survival | 1.13.40 | 11 | ✅
| Stickman Hook | 7.2.8 | 11 | ❌ | Game fails to initialize
| Strawberry Shortcake Dress Up Dreams | 1.4 | 12 | ❌ | An error message on startup says "Download Failed - An unexpected error occured. (Error Code: 15)" The error log indicate that it relies on Google Services Framework. | 
| Subway Surfers | 2.24.2 | 11 | ✅ | Doesn't support keyboard control
| Suzy Cube | 1.0.12 | 12 | ❌ | Shows a black screen after the developer logo screen. The error log shows `Unity: NullReferenceException: A null value was found where an object instance was required.`
| Sword Art Online: Integral Factor| 1.9.2 | 11 | ✅ | Keyboard unsupported
| Sword Art Online: Memory Defrag | 3.0.2 | 11 | ✅ | Keyboard unsupported
| Sword Art Online: Unleash Blading | 3.2.0 | 11 | ⚠️ | Can't detect device
| Terraria | 1.4.3.2.2 | 11 | ✅ || Keyboard supported
| The Battle Cats | 11.2.1 | 11 | ✅
| The Battle of Polytopia | 2.0.59.5719 | 11 | ❌ | Validation error
| The King Of Fighters Allstar | 1.9.3 | 11 | ✅ | Blank screen / app crash on first boot, works on second boot upwards
| This War of Mine | 1.0 | 11 | ❌ | Infinite loop at start-up screen
| Traffic Racer | 3.5 | 13,12,11 | ✅ | | Keyboard supported
| Toca Kitchen 2 | 2.2-play | 13 | ⚠️ | You can't access the game settings (or any swipe action) with a keyboard and mouse even with trackpad gestures | Recommended to use a touchscreen but it is also possible to play the game with just only the mouse.
| True Skate | 1.5.39 | 11 | ✅ | Minor graphical glitches
| Uma Musume: Pretty Derby (ウマ娘 プリティーダービー; JP) | 1.16.0 | 11 | ⚠️ | Doesn't work with GTX1660. Works with Microsoft Basic Render Driver with graphical issues. | Some features may require GMS.
| Uma Musume: Pretty Derby (ウマ娘 プリティーダービー; JP) | 1.20.0 | 12 | ❌ | Only touch effect works after displaying the developer logo
| Uma Musume: Pretty Derby (Korean) | 1.0.1 | 12 | ❌ | Only touch effect works after displaying the developer logo
| War Robots | 7.7.7 (134783) | 11 | ✅ | GMS warnings might appear but these can be safely ignored
| Warfare Incorporated | 1.63 | 11 | ✅ | The selection box does not work.
| Where is my Water? || 11 | ⚠️ | Many images are replaced with white rectangles
| Where is my Water? 2 || 11 | ⚠️ | Most images are replaced with white rectangles, Vignette overlay is full white and covered the whole playing area. The ground is not textured correctly.
| Where is my Water? Featuring XYY || 11 | ⚠️ | Bells are invisible
| Wordament | 3.9.10260 | 11 | ✅
| Дурак Онлайн (Durak Online) | 1.9.2 | 11 | 🆖 | Requires GMS
| 白夜極光 (Alchemy Stars) | 1.2.2 | 11 | ⚠️ | Poor in-game performance
| 公主连结R (Princess Connect! Re: Dive (Simplified Chinese) | 3.4.10 | 11 | ✅
| 神魔之塔 (Tower of Saviors) | 2022.600 | 12 | ✅ | Gameplay and graphics are excellent, but the game will crash at random when downloading game data. | The first time you open it, it will have difficulty downloading game data because it will crash randomly; simply be patient and keep restarting.
| 云·原神 (Genshin Impact (Cloud app) )|| 11 | ✅
| 原神（Genshin Impact） | 2.2.0 | 11 | ⚠️ | Working but heavy graphical glitches - [video](https://www.bilibili.com/video/BV1zT4y1o73D?)
| 崩坏学园2 (Honkai Gakuen 2)| 8.5 | 11 | ✅ || Game has inbox keyboard controller for WASD
| 東方LostWord (Touhou: Lost Word) | 1.16.0 | 11 | ❌
| 战双帕弥什 (Punishing: Gray Raven) || 11 | ✅ || Keyboard is supported
| プロジェクトセカイ カラフルステージ！ feat. 初音ミク (Project Sekai Colorful Stage JP) | 1.3.2 | 11, 12 | ❌ | App either crashes when loading into game after login or app screen turns dark
