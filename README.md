# chromavr's Guide to make qsabers
In this guide i'll be showing you how to create your own qsabers. Be prepared for some typing errors, i am just a human, i make some mistakes too.

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

![Choosing the right Version of Unity](/GuideFiles/Images/qsaber/1 selecting unity version.jpg) 

When opened, check if the `Saber Exporter` in the `Window` tab is existent.

---Bild---

The scene should contain a Object called `Template Saber`, select the Object. If you opened the scene for the first time, you might be a bit far from the Template Saber. To select the saber you click the Object `Template Saber` in the Hierarchy (the window on the left side of Unity). Click the small arrow next to it or double click the Object to discover two Gamobjects named `LeftSaber` and `RightSaber`. Check if both GameObjects have the EventManager attached.

---Bild---

Now import your model/models by simply draging them into the `Assets` window.

---Bild---

Now that you imported it/them, you need to drag it/them into the scene. To do that simply select the saber and drag it into the Hierarchy window. When the saber is in the scene you now need to allign the saber with the Template sabers, that means, that it has the same size as the Template sabers. I had to rotate it for 270° on the X Axis, but didnt had to tweak with the Scale variables. In the Hierarchy window you take the saber that you just imported at drag it on top of the `RightSaber` GameObject, then copy your saber and drag it on the `LeftSaber` GameObject. So the Hierarchy should look like this:

---Bild---

When your saber is the same size as the template saber you simply can disable the Mesh Renderer of the `LeftSaberMesh` and `RightSaberMesh`, which are in the GameObjects called `RightSaber` and `LeftSaber`, so it wont disturb as we work more on it. In the Hierarchy window you take the saber that you just imported at drag it on top of the `RightSaber` GameObject, then copy your saber and drag it on the `LeftSaber` GameObject.

---Bild---

Now we are going to create Materials for the each part. Simply create a Material by `Right Click -> Create -> Material`. It has to have a Beat Saber compatible shader, so it wont appear white in the game. When you created a Material select it and look to the right side of Unity. Under the name of the 
