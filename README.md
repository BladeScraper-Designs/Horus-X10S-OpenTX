# Horus X10S OpenTX
This repository contains the SD Card contents from my Horus X10S with OpenTX.  It can be used as a reference or base for setting up your own models.  It also contains the .otx file for Companion with my models and settings.  SD Card folder "BRAIN2" contains the script necessary for Brain2 + OpenTX Integration.  Everything here in the readme assumes you already have OpenTX 2.3.9 (as of 7/15/2020) installed on your radio.  Older versions of OpenTX might not work with my models.

# Info About My Radio
-I have moved and replaced switches with different ones.  Throttle hold switch has been replaced with a 3-position switch instead of 2-position, similar to what the Vbar Control has.  This lets me use autorotation bailout with Brain2.  

-I've put the momentary switch in the back left of the radio, it's being used for rescue with Brain2.

-2 Position switch is on the back right of the radio.  For the N556 model, this is used for SwitchGlo.

As a result of these moved switches, the switch positions in the manual will not be accurate or representative of how my models are set up.  If you have not changed any switches around, you will have to mess with the switches used for various features, and some (mainly the throttle hold switch) will not work as intended on radios with a 2-position throttle hold switch.

-Volume is controlled by the left-most knob on the front of the radio.

# Spoken Flight Modes
Spoken flight modes are global for all models so I don't have to use special functions for each model.  They're located in global functions.  If you have a model (e.g. airplane) that you don't want spoken flight modes for, simply go to model setup first page and uncheck "Use Global Funcs".  If you want to have different spoken flight modes for that specific model you can create new ones in  the Special Functions page.

# Settings changed from stock OpenTX:

-Splash Screen Changed

-Radio Background Changed

-Theme Color Changed from Red to Black

-Removed most default images, since they were not useful to me, and especially not for helis :)


# Model Images for Helicopters can be found in /Images/Model Images.  
Simply put them into your Images folder on your radio's SD Card and you can use it as the image for your model.  You can rename the image, but be aware it must be only 6 characters long in order to be able to use it.  They are all transparent PNG images, which looks really nice when being used as a model image.  If you'd like to make a contribution with your own images, send me an email with the image and I might upload it here.  The correct resolution is 192x106.


# Viewing My Example Models (Click image for higher quality)
If you wish to view my models and setups in order to have an example of how to set up your own models, follow these steps.  This guide assumes you have already created a profile and flashed your Horus X10/S with the same version of OpenTX as I am running.  Potential incompatibilities exist between newer and older versions, so avoid mixing models made in a different version if possible.

1. Download SD Contents and .otx file from this repository.

2. Open the Companion software.

3. In Companion, create a new radio profile for my radio and my SD card contents.  Set SD Structure Path to wherever you put the SD Contents you downloaded from this repository. It's important that you do this because the SD card contains images, sound files, and Lua scripts all of which are used for my models.  Make sure the SD Structure Path is somewhere other than the one for your own radio.  Also make sure that when you open my .otx file to view models, the radio profile for my radio is slected so it knows where to get the SD contents when you run the simulator.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/Settings.png?raw=true)

4. Open my .otx file in Companion.  
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/open.png?raw=true)

5. At this point, you should see a window come up with my models in it.  If you click Simulate Radio, you should see a virtualized Horus X10/S with my models on it.  Controlling it with your keyboard can be a bit confusing to get used to, but you can use your mouse as well.  Use the simulator to browse my models and explore how they are set up.  
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/simulator.png?raw=true)



# Importing my models onto your radio (Click image for higher quality)
Follow the above steps to view my models, then:

1. Connect your Horus X10/S to your computer.

2. Switch to your radio's profile instead of mine (Settings>Radio Profiles>Your Radio Profile).  Again, this guide assumes you have already created a profile and flashed your Horus X10/S with OpenTX 2.2.4.  This must be done so that when you write the model to your radio it knows where to put them (into your SD Structure Path)

3. With your radio connected to the computer and in Mass Storage mode, click the "Read Models and Settings From Radio" in Companion.  This will create an otx tile of your radio called document1.otx.  If this radio has never been used before and has no new models, the file will be empty, but you still need it for this process.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/readmodels.png?raw=true)

4. Open my x10s.otx file in Companion. This will create a second window with my models visible.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/openmine.png?raw=true)

5. Find the model you want to copy from my radio.  Click and drag it onto your radio.  You can also copy and paste the model if click+drag isn't working.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/drag.png?raw=true)
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/copied.png?raw=true)

6. With your radio's model/settings highlighted, hit File>Save or Ctrl+S.  This will save the model to your radio's otx file.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/save.png?raw=true)

7. Press Write Models and Settings To Radio" in Companion.  
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/write.png?raw=true)

8. Once this is done, click Synchronize SD Card in the top menu, which will ensure your radio's SD card and the SD Structure Path have the same contents.




# Disclaimer
This repository is provided without any implied warranty, service, or guarantee.  It is simply a place for me to share my Horus' setup, models, and settings.  I am not responsible for loss, damage, or injury caused by the use of files in this repository.  
