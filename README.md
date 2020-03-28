# chromavr's Guide to make qsabers
In this guide i'll be showing you how to create your own qsabers. Be prepared for some typing errors, i am just a human, i make some mistakes too.

In this guide i'll be using the GHOST saber by Hooi.

# Required Programs and Files for making a qsaber

- First of all you need the [Unity Version 2019.3.2f1](https://unity3d.com/de/get-unity/download?thank-you=update&download_nid=63532&os=Win) (keep in mind that you need to install the Android SDK too)
- This [Unity project](https://bs.assistant.moe/Sabers/resources/CustomSaberUnityProject.zip), [Source](https://bs.assistant.moe/Sabers/)
- and lastly you need a model program of your choice (in this guide i'll be using Maya)

# Getting the model
## Using a Premade Model
When using a premade one, you need to split it first, because later in Unity you still want to apply materials to different parts. I wont be going over that here since i dont know what modeling program you use. To find out how to split it in your preferred program, i'd recommend googling it.

## Using a selfmade Model
When you use a selfmade model you dont need to split it, except its one mesh. I wont be going over on how to make your own model. Since this is a qsaber, you wont need to split it into three meshes.

# In Unity
When you got your models ready, you now need to open Unity with the CustomSaberUnityProject. Of course you need to select the right version of Unity and choose Android as the Build Platform. Then you open the project. It may warn you that you're on the wrong Unity version, but ignore that and click confirm, tt will work either way.

![Choosing the right Version of Unity](https://raw.githubusercontent.com/chromavr/BMBFmods/master/GuideFiles/Images/qsaber/1%20selecting%20unity%20version.JPG) 

![Choosing the right Build Platform](https://raw.githubusercontent.com/chromavr/BMBFmods/master/GuideFiles/Images/qsaber/2%20build%20platform.JPG)

When opened, check if the `Saber Exporter` in the `Window` tab is existent.

![Check if the Saber Exporter is existent](https://raw.githubusercontent.com/chromavr/BMBFmods/master/GuideFiles/Images/qsaber/3%20check%20if%20saber%20exporter%20is%20existent.jpg)

The scene should contain a Object called `Template Saber`, select the Object. If you opened the scene for the first time, you might be a bit far from the Template Saber. To select the saber you click the Object `Template Saber` in the Hierarchy (the window on the left side of Unity). Click the small arrow next to it or double click the Object to discover two GamObjects named `LeftSaber` and `RightSaber`. Check if both GameObjects have the EventManager attached.

![Importing the Saber](https://raw.githubusercontent.com/chromavr/BMBFmods/master/GuideFiles/Images/qsaber/4%20import%20saber%20into%20assets.jpg)

![Checking if both Template Meshes have the Event Manager attached]()

Now import your model/models by simply draging them into the `Assets` window.

![Import your Saber by draging it into the Assets Window](https://raw.githubusercontent.com/chromavr/BMBFmods/master/GuideFiles/Images/qsaber/4%20import%20saber%20into%20assets.jpg)

Now that you imported it/them, you need to drag it/them into the scene. To do that simply select the saber and drag it into the Hierarchy window.

![Drag them into the scene](https://raw.githubusercontent.com/chromavr/BMBFmods/master/GuideFiles/Images/qsaber/5%20drag%20into%20hierarchy.jpg)

When the saber is in the scene you now need to allign the saber with the Template sabers, that means, that it has the same size as the Template sabers. I had to rotate it for 270° on the X Axis, but didnt had to tweak with the Scale variables. To change the scale of your saber you need to click your saber in the Hierarchy and look to the right side of Unity. In the Hierarchy window you take the saber that you just imported at drag it on top of the `RightSaber` GameObject, then copy your saber and drag it on the `LeftSaber` GameObject. So the Hierarchy should look like this:

![Hierarchy Window](https://raw.githubusercontent.com/chromavr/BMBFmods/master/GuideFiles/Images/qsaber/6%20drag%20your%20saber%20on%20RightSaber%2C%20copy%20and%20drag%20on%20LeftSaber.JPG)


When your saber is the same size as the template saber you simply can disable the Mesh Renderer of the `LeftSaberMesh` and `RightSaberMesh`, which are in the GameObjects called `RightSaber` and `LeftSaber`, so it wont show up in the game. 

![Disabling the Mesh Renderer]()

Now we are going to create Materials for each part. Simply create a Material by `Right Click -> Create -> Material` and name it. It has to have a Beat Saber compatible shader, so it wont appear white in the game. When you created a Material select it and look to the right side of Unity. Under the name of the Material will be a drop-down field to select which shader the Material should use. Since we are using the Custom Saber Unity Project there now will be one extra option called Beat Saber. Click it and 4 possible shaders will appear.

![The 4 Shaders]()

Beat Saber has four compatible shaders. They are:

- Lit Glow
- Metallic
- Unlit Glow
- Unlit Glow Cutout Dithered.

Select one which you think will fit with the Mesh you want to apply it to. After you selected a Beat Saber shader you can now choose the color of the Material. For blue i chose blue, obviously. When you gave the Material a color you can now play around with the `Glow` slider. This slider basically allows the Material to glow in the game (keep in mind, anything over 0 will be affected by Custom Colors). For my material i put the glow to 1. 

![Shader settings]()

When everything is to your liking, you can now apply the Material to your mesh. Simply drag the Material on the part you want it to be affected by. I created 3 materials for the saber im using, Blue, Red and the material for the Blade and Handle. 

When you like how the saber looks you can now export your saber. To do that go to the `Window` tab and click `Saber Exporter`. A new Window will appear which will look like this:

![Saber Exporter Window]()

Where it says `Author Name`, put in your name, and where it says `Saber Name`, put in the name of the Saber. After that you click Export [Your Sabername]. Then you will have to go to where you saved your saber, and edit the File extension from `.saber` to `.qsaber`. It may say that after changing the file extension, the file might be broken, just click ok, it will work fine. And you're done!

![Changing file type]()

# Test your saber
To test your saber you want to install it on your Quest. If it works fine, take a picture and get the picture from the Quest. Name the file exactly like the saber.


# Uploading 
When you finished everything and it works you can either upload it to Modelsaber or make it into an BMBF compatible mod.

## Uploading to Modelsaber
To upload your qsaber to Modelsaber, go to their [website](https://modelsaber.com/). After that you log-in with your Discord account. Then you want to go to the upload tab. You now select you saber by clicking `Select File` on the bottom of the page. Then you click `Select Thumbnail` and select the picture you took earlier. After that you can upload the saber.

## Make the saber into a BMBF compatible mod
To make your saber BMBF compatible, you need to get the bmbfmod.json file from the GuideFiles. Open the json file with a text editor other than Notepad, Notepad++ should do the job. When you opened the file you will see this code:

```
{
  "coverImageFilename": "Cover.png",
  "icon": "Cover.png",
  "components": [
    {
      "Type": "FileCopyMod",
	  "SourceFileName": "SaberName.qsaber",
      "TargetRootedPathAndFileName": "/sdcard/Android/data/com.beatgames.beatsaber/files/sabers/testSaber.qsaber"
    }
  ],
  "version": "1.0.0",
  "links": {},
  "description": [
    "Mod Description"
  ],
  "gameVersion": "1.8.0",
  "platform": "Quest",
  "id": "ModID",
  "name": "Mod name",
  "author": "yourname",
  "category": "Saber"
}
```

Change the `SaberName.qsaber` at `SourceFileName` to whatever your saber is named. Then change the rest at the bottom, means `id`, `name` and `author`. After that save your changes and zip it up. Then you just need to drag it into BMBF and you're done!
