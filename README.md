# HLMVPlusPlus-IssueTracker
Report issues or provide feature suggestions for HLMV++ here.

# Credits
- TF2CutContentWiki - Commissioned the creation of this project.
- [ficool2](https://github.com/ficool2) - Programming. The entire reason this even exists.
- [Gabrielwoj](https://github.com/gabrielwoj) - Bug testing, providing feedback and insight on changes/new features.

# Important!
This build is for Team Fortress 2. I'm not certain if it will work nicely with other games, but it has been designed specifically for Team Fortress 2.

I have however inquired with ficool2 about making a version of this program for other games (L4D, L4D2, Portal, Portal 2, CSS, CS:GO, HL2, etc).

# Installation
Download the EXE and the DLL files and extract them into your steamapps/common/Team Fortress 2/bin folder (where hlmv.exe is). Then just launch hlmvplusplus.exe instead of hlmv.exe and you're done!

# New Features
*This list is incomplete, as I am writing it up while at work, away from my PC.*

- [Hiding the controls panel that takes up the bottom third of the window can now be done](https://drive.google.com/file/d/1zGoXqRgWLNYCyMDyXg15ZOw6gnSVF2An/view?usp=drivesdk) via **View > Hide Control Panel**.
- **Options > Make Screenshot** now functions correctly, [generating a TGA formatted screenshot complete with a proper automatically created alpha channel](https://twitter.com/TF2CCWiki/status/1506697372360921091?t=6W5JvdDRSGEu30G94_DeHQ) for easy background removal for renders, even on [models with transparent/semi-transparent areas](https://twitter.com/TF2CCWiki/status/1505343182204190725?t=JvEA1EFZzbPdvkjvxJQ3cQ).
- dxsupport.cfg tweaks to increase render quality should no longer be necessary with [the new "Picmip", "Antialias" and "Anistropic" dropdowns added to the **Render** tab on the bottom controls panel](https://twitter.com/TF2CCWiki/status/1494112255151153154?t=Sm1IA5paAfwOYRvCZckx-Q).
- [VMT material variables can now be edited live in HLMV](https://twitter.com/TF2CCWiki/status/1492267684372828167?t=FQ9Brn1XsnCRMPTCRNdGbg)!
- The list of dropdowns for facial flexes [has been updated to use sliders instead of dropdowns, autopopulates the flexes so every flex is listed, and the list has been paginated as well](https://media.discordapp.net/attachments/993823597401489468/993824557574127697/unknown-60.png), so you don't run into that fun issue where changing which flex a dropdown controls causes all your flex settings to reset.
- The ability to save and import facial flex layouts has been added. More info and an example layout can be seen in the next section.

# New Facial Flex Saving
If you are familiar with using the Registry Editor (regedit.exe) to modify the "trans", "rot" and "lightrot" settings for models, there is now a new key that is added for models with facial flexes. The new key is called "flex" and can be used to export/import facial flex layouts.

Here is an example "flex" key layout for `models/player/heavy.mdl`:

`DS;0.000000;MB;0.000000;right_CloseLid;0.500000;left_CloseLid;0.500000;multi_CloseLid;0.500000;blink;0.000000;upset1;0.000000;upperAngry3;0.000000;P;0.000000;dead03;0.000000;actionfire01;0.000000;happy1;0.000000;painbig;0.000000;dead02;0.000000;upset2;0.000000;actionfire02;0.000000;happybig;0.000000;upperSad3;0.000000;upperSad1;0.000000;upperSuprise1;0.000000;happybig02;0.000000;happysmall02;0.000000;upperAngry2;0.000000;mad;1.000000;idleface;0.000000;upperHappy1;0.000000;upperHappy2;0.000000;upperUpset1;0.000000;dead01;0.000000;happyBig02Upper;0.000000;happybigUpper;0.000000;Neutral;0.000000;ER;0.000000;RR;0.000000;SH;0.000000;EEE;0.000000;WQU;0.000000;FFF;0.000000;AIY;0.000000;AH;0.000000;ST;0.000000;LTH;0.000000;UH;0.000000;OH;0.000000;eyes_updown;0.500000;eyes_rightleft;0.500000;`

# Other Notes
- The **Make Screenshot** function may not work correctly when HLMV is stretched across multiple monitors. Doing so may result in a very wide screenshot with two copies of the same model in it. This is, to my knowledge, not fixable.
