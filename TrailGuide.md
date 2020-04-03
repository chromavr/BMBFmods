# chromavr's guide on how to create custom Trails

In this guide i'll be showing you how to create custom Trails. 
If you have any questions, please DM me on Discord (chromavr#2712)

# Required Files and Programs for making a Trail

- A image editor of your choice (I will be using [Krita](https://krita.org/en/download/krita-desktop/#) in this tutorial)
- [UABE](https://mega.nz/#!ScgiWYRJ!5b_9g2B4eOZaAA3JAV2htVRamNYuxQLrWyMbSXv-k1o) ([Source](https://forums.7daystodie.com/forum/-7-days-to-die-pc/game-modification/tools/23262-unity-assets-bundle-extractor?22675-Unity-Assets-Bundle-Extractor=))
- This [GuideFiles.zip]()

# Getting your Image for the Trail

You can use a image that you found on the internet or one you made. I wont be going over on how to create a image. 

# Editing the image

When you have your image you open up your image editing program and get your chosen image into it. Now you want to change the size of the image to 128x128, since that is the size of the Trail ingame. In Krita you resize it through `Image -> Scale Image to new Size` or by just pressing `CTRL + Alt + I`. 

![Resize Image]()

You have to disable `Constrain Proportions` so you can edit the image without it keeping the same ratio. 

![Resize Image]()

*This is optional: You may want to add a fade to it. Simply do that by selecting the `Gradient Tool` and drag it from right to left.* 

![Gradient Tool]()

![Gradient Tool]()

Now you can save it as a png. After that you can open UABE and open the GuideFiles file in the GuideFiles.zip file. To do so click `File` and then `Open` in UABE. When its opened you will see the asset `FullTrail`, click on it and then click `Plugins`. 

![UABE Window]()

A small window will appear with 3 options inside of it. You will click `Edit` and then `Ok`. Another Window will apear with the Edit settings. You just want to click `Load` and select your image. After that you click `Ok` again and both small windows will close. 

![The 3 options]()

![Edit Window]()

After that you wanna click `Ok` and you want to save the changes. Save it as whatever you want. Then open the file you just saved. When opened you wanna click `Export Raw` and select where you wanna save it. 

**You have to save it with the name `FullTrail`, otherwise it wont work!**

After that you can close UABE. Now that you have exported the Trail, you want to edit the `bmbfmod.json` file in the GuideFiles zip. To do so, open the file with a text editor of your choise (any other than Notepad works fine, i use [Sublime Text](https://www.sublimetext.com/3)). 

You just have to change something at the bottom of the json, so scroll down to it. What you see there is this:
```
"version": "1.0.0",
    "links": {},
    "description": [
        "Mod Description"
    ],
    "gameVersion": "1.8.0",
    "platform": "Quest",
    "id": "ModID",
    "name": "Mod name",
    "author": "Yourname",
    "category": "Other"
}
```

This is pretty self-explanitory but im explaining it anyways:
```
"version": "1.0.0", --- The version of your mod.
    "links": {}, --- You can put a link to your image source here, but not needed.
    "description": [
        "Mod Description" --- The description of the Mod.
    ],
    "gameVersion": "1.8.0", --- The version of Beat Saber the mod should work on.
    "platform": "Quest", --- The platform Beat Saber is installed on.
    "id": "ModID", --- The ModID
    "name": "Mod name", --- The Mod Name (what will be shown in BMBF)
    "author": "Yourname", --- Your Name 
    "category": "Other"
}
```

Now you change the fields. For my mod i put this in:
```
"version": "1.0.0",
    "links": {},
    "description": [
        "Changes your Trail to a glitch"
    ],
    "gameVersion": "1.8.0",
    "platform": "Quest",
    "id": "GlitchTrail",
    "name": "Glitch Trail",
    "author": "chromavr",
    "category": "Other"
}
```

After you changed it, save it and close the text editor. Now you just want to zip it up and test it.

**It has to be a .zip file, .rar files wont work**

# Testing your Mod

Now that you completed everything its time to test your mod. To do that, go to your browser and open BMBF (the URL will look like this: http://http://192.168.x.xxx:50000/. Ofcourse you have swap out the x's with the rest of your Quest IP.)

Now you just drag your Mod into the upload setion of BMBF and test it out.

![Trail Image](

Nice! Now that everything works you can take a screenshot. When you made a screenshot go back to your PC again and get it from the Quest. Open it with a image editor and save it as `Cover.png`. After that you zip the files again, this time with the Cover and, you're done!

If you have any questions about this guide or any other stuff, please DM me on Discord (chromavr#2712).