https://wiki.winehq.org/Wine_User%27s_Guide#OSS_Audio_Driver_Settings

The link is for environment variables pertaining to audio drivers, environment variables and how to point wine to the right hardware in linux if needed.

# How do I get my setup windows apps to run in their own container?

Set the environment variable WINEPREFIX equal to the folder for your app container. Remember to have that set when you run wine.

# What do I have to do to get my app to use VirtualGL, Vulkan, Gallium, and Mesa?

winetricks will also need the WINEPREFIX that you set before installing Vulkan, Gallium, and nine-wine. You'll need to look under the DLLs options. Once you've checked the boxes needed, and click okay, your app components for wine should install.

I am using ubuntu & intel hardware. Do note that if you aren't using NVidia drivers, this will also help you, as well as those that are using NVidia.
Currently, I use "sudo apt-get install" and "sudo dpkg -i" to install the drivers and VirtualGL.

# How do I start my Windows app with wine & VirtualGL? Aren't Linux & Windows opposites?

It is as simple as typing "vglrun wine" and then add the app you want to run. I currently use VirtualGL with my linux Chrome browser install. While yes, Windows & Linux are different beasts, I have found that wine works well enough to run things like python, java, & google-chrome.
