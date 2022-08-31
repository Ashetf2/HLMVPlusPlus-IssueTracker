# HLMVPlusPlus-IssueTracker
Report issues or provide feature suggestions for **HLMV++** here.

# Official Discord
We have a Discord server now where you can submit bugs or feature suggestions!

**[Click here to join](https://discord.gg/GeqVxrJfRs)**!

# Credits
- **TF2CutContentWiki** - Commissioned the creation of this project.
- **[ficool2](https://github.com/ficool2)** - Programming. The entire reason this even exists.
- **[Gabrielwoj](https://github.com/gabrielwoj)** - Bug testing, providing feedback and insight on changes/new features. Also made the Discord server image.
- **[Andrew360](https://wiki.teamfortress.com/wiki/User:Andrew360)** - Bug testing, providing feedback and insight on changes/new features.

# Important!
***This build is for Team Fortress 2***. I'm not certain if it will work nicely with other games, but it has been designed specifically for Team Fortress 2.

I have however inquired with ficool2 about making a version of this program for other games (L4D, L4D2, Portal, Portal 2, CSS, CS:GO, HL2, etc).

# Installation
Download the EXE and the DLL files and extract them into your `steamapps/common/Team Fortress 2/bin` folder (where `hlmv.exe` is stored). Then just launch `hlmvplusplus.exe` instead of `hlmv.exe` and you're done!

# Fixes & New Features
*There are some other features I haven't added to this list yet, like being able to apply unusual particle FX to a model. Those will be added in a few hours once I am in front of my PC.*
- **New Feature:** [View > Show/Hide Control Panel](https://drive.google.com/file/d/1zGoXqRgWLNYCyMDyXg15ZOw6gnSVF2An/view?usp=drivesdk).
  - Allows you to show/hide the lower-third controls panel, for larger renders.
- **New Feature/Fix:** Options > Make Screenshot.
  - I don't know if this option ever worked in HLMV, nor what type of image file it would/should have outputted, but it mow functions correctly, and functions way better. [It now generates a TGA formatted screenshot, complete with a proper automatically-created alpha channel](https://twitter.com/TF2CCWiki/status/1506697372360921091?t=6W5JvdDRSGEu30G94_DeHQ) for easier background-removal, even on [models with transparent/semi-transparent areas](https://twitter.com/TF2CCWiki/status/1505343182204190725?t=JvEA1EFZzbPdvkjvxJQ3cQ).
- **New Feature:** Options > Make Video.
  - Ever wanted a better way to make GIFs/APNGs of model animations in HLMV? This new "Make Video" option generates individual TGA screenshots for each frame of the animation you're viewing, complete with auto-generated alpha channels for easy background removal.
- **New Feature:** ["Picmip", "Antialias" and "Anistropic" dropdowns added to the "Render" tab on the lower-third controls panel](https://twitter.com/TF2CCWiki/status/1494112255151153154?t=Sm1IA5paAfwOYRvCZckx-Q).
  - Those dxsupport.cfg tweaks that you used to have to do to increase render quality should no longer be necessary.
- **New Feature:** [Live VMT material editing](https://twitter.com/TF2CCWiki/status/1492267684372828167?t=FQ9Brn1XsnCRMPTCRNdGbg).
  - This should make learning what VMT variables do what, and learning how to work with VMT files in general, a hell of a lot easier. 
- **Fixed:** VMT Material Proxies not being respected.
  - HLMV kind of ignored the entire Proxies section of VMT files for models. HLMV++ respects those proxies and thus, will display what the model would look like ingame.
  - **Upcoming Tweak:** An option to toggle whether or not to respect the Proxies section is planned.
- **New Feature/Fix:** [Facial flex panel overhaul](https://media.discordapp.net/attachments/993823597401489468/993824557574127697/unknown-60.png).
  - Kiss those dropdown boxes goodbye. The flex list is now auto-populating and paginated so there's no need for dropdown boxes to change a targeted flex.
  - This fixes the age-old bug where facial flexes you had changed would be reset to their default values when you changed which flex a dropdown box was targeting.
- **New Feature:** The ability to save and import facial flex layouts has been added. More info and an example layout can be seen in the next section.

# New Facial Flex Saving Explained
If you are familiar with using the Registry Editor (regedit.exe) to modify the "trans", "rot" and "lightrot" settings for models, there is now a new key that is added for models with facial flexes. The new key is called "flex" and can be used to export/import facial flex layouts.

Here is an example "flex" key layout for `models/player/heavy.mdl`:

`DS;0.000000;MB;0.000000;right_CloseLid;0.500000;left_CloseLid;0.500000;multi_CloseLid;0.500000;blink;0.000000;upset1;0.000000;upperAngry3;0.000000;P;0.000000;dead03;0.000000;actionfire01;0.000000;happy1;0.000000;painbig;0.000000;dead02;0.000000;upset2;0.000000;actionfire02;0.000000;happybig;0.000000;upperSad3;0.000000;upperSad1;0.000000;upperSuprise1;0.000000;happybig02;0.000000;happysmall02;0.000000;upperAngry2;0.000000;mad;1.000000;idleface;0.000000;upperHappy1;0.000000;upperHappy2;0.000000;upperUpset1;0.000000;dead01;0.000000;happyBig02Upper;0.000000;happybigUpper;0.000000;Neutral;0.000000;ER;0.000000;RR;0.000000;SH;0.000000;EEE;0.000000;WQU;0.000000;FFF;0.000000;AIY;0.000000;AH;0.000000;ST;0.000000;LTH;0.000000;UH;0.000000;OH;0.000000;eyes_updown;0.500000;eyes_rightleft;0.500000;`

# Other Notes
- The **Make Screenshot** function may not work correctly when HLMV++ is stretched across multiple monitors. Doing so may result in a very wide screenshot with two copies of the same model in it. This is, to my knowledge, not fixable.
