Technical Artist - Tech Test (Luis Hostos)

**Git repository Main:**

https://github.com/BuhoNero/ta-tech-test

**Branch:**

polish/play-button

**Pull Request:**

https://github.com/BuhoNero/ta-tech-test/pull/1


**Project structure**

The original project folder structure corresponds to a Unity package downloaded from the Asset Store. 

In those folders there’s a Unity Scene. While the structure is well-defined, it presents a risk, as working directly in it could result on accidentally replacing work, either when reimporting or updating the original package from the Asset Store. 

For best practices, I created a new folder structure:


_Project
  Animations
  Audio
    SFX
  Materials
  Prefabs
  Scenes
  Textures

I also created a Unity scene called “Main”, for the test itself.

**Game Juice**

As shown in the demo scene I added animations to the several elements.

Also imported a third party extension to facilitate Particles in UI canvases: (https://github.com/mob-sakai/ParticleEffectForUGUI)

**UI**

For the test purposes, I removed buttons that weren’t visible
I created new prefabs and reorganized slighty to include the Animations and SFX needed.

**Performance optimization**

Not much to optimize at this point, the scene itself is very light. Around 29 draw calls, and high FPS at the moment (pc editor)

Sprite Atlases could be used if there are several individual sprites, that could be packed into a single texture and then compressed due to a power of two image size.

**Pipeline optimization**

Artist should have a basic training on how to export assets for Unity. Some examples:
Working on the exact resolution needed for a target device (Mobile Phone)
Prepare buttons, panels, backgrounds and other to be 9-sliced or other common slice settings
Prepare assets that need to be colored dynamically in grayscale
Prepare textures that might support power of two sizes, for compression.
In the case of UI, prepare assets to support for multiple aspect ratios 


Assuming the project is in 2D, sprite based, I would create a texture import settings preset and set is default, this way, every texture imported will automatically be setup as a 2D sprite. 
