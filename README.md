# Horus X10S OpenTX
This repository contains the SD Card contents from my Horus X10S with OpenTX.  It can be used as a reference or base for setting up your own models.  It also contains the .otx file for Companion 2.2.4 with my models and settings.  SD Card folder "BRAIN2" contains the script necessary for Brain2 + OpenTX Integration.  Everything here in the readme assumes you already have OpenTX 2.2.4 installed on your radio.

# Info About My Radio
-I have moved and replaced switches with different ones.  Throttle hold switch has been replaced with a 3-position switch instead of 2-position, similar to what the Vbar Control has.  This lets me use autorotation bailout with Brain2.  

-I've put the momentary switch in the back left of the radio, it's being used for rescue with Brain2.

-2 Position switch is on the back right of the radio.  For the N556 model, this is used for SwitchGlo.

As a result of these moved switches, the switch positions in the manual will not be accurate.  If you have not changed any switches around, you will have to mess with the switches used for various features, and some (mainly the throttle hold switch) will not work as intended on radios with a 2-position throttle hold switch.

-Volume is controlled by the left-most knob on the front of the radio.

# Model-Specific Info
**LOGO 480**

-Uses channel overrides for throttle outputs for use with governor.  If you're NOT running a governor, it will act like flat throttle curves.  I will eventually update this model to use curves like the N556 model does.



**Synergy N556**

-This model is properly set up with curves and flight modes.  This is the better way of doing helicopters on OpenTX, compared to using channel overrides like the LOGO 480 model does.  This helicopter model, like the LOGO 480 model, has three stunt modes, and no normal mode, however because it uses curves instead of overrides, it would be pretty easy to set up a normal mode if one wanted it.

-Hot Start Prevention safety feature in use on this model.  It works by using a logic switch to check the state of the throttle hold switch.  If throttle hold is NOT enabled (it's off or in the AR bailout mode, positions 2-3) it will use a Special Function to override the Aux channel to -150.  Since SwitchGlo is on the Aux channel of the Brain2, SwitchGlo will not be allowed to ignite.  This effectively means that a hot start is impossible because the glow igniter will not ignite unless the throttle servo is in idle position.

**Nano S2**

-This model is super simple.  Because the Nano S2 runs the motor at 100% throttle in 3D mode no matter what throttle output you have, I just use channel overrides instead of curves, because curves would be useless in this case.  

-The flight mode switch is set to the 3-position switch normally used for Normal/IU1/IU2.  SAFE mode (self-leveling and fixed pitch amount) does work.

**AccuRC**

-This model is for use with the XSR-SIM FrSky Simulator Dongle with AccuRC.  It's super simple, but because the spoken flight modes are in global functions, it still has those. 

# Spoken Flight Modes
Spoken flight modes are global for all models so I don't have to use special functions for each model.  They're located in global functions.  If you have a model (e.g. airplane) that you don't want spoken flight modes for, simply go to model setup first page and uncheck "Use Global Funcs".  If you want to have different spoken flight modes for that specific model you can create new ones in  the Special Functions page.

# Settings changed from stock OpenTX:

-Splash Screen Changed

-Radio Background Changed

-Theme Color Changed from Red to Black

-Removed most default images, since they were not useful to me, and especially not for helis :)


# Model Images for Helicopters can be found in /Images/Model Images.  
Simply put them into your Images folder on your radio's SD Card and you can use it as the image for your model.  You can rename the image, but be aware it must be only 6 characters long in order to be able to use it.  They are all transparent PNG images, which looks really nice when being used as a model image.  If you'd like to make a contribution with your own images, send me an email with the image and I might upload it here.  The correct resolution is 192x106.


# Viewing My Example Models
If you wish to view my models and setups in order to have an example of how to set up your own models, follow these steps.

1. Download SD Contents and .otx file from this repository.

2. Open the Companion software.

3. In Companion, make sure your radio profile is set up for the X10/S.  Set SD Structure Path to wherever you put the SD Contents you downloaded from this repository. It's important that you do this because the SD card contains images, sound files, and Lua scripts all of which are used for my models.  
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/Settings.png?raw=true)

4. Open my .otx file in Companion.  
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/open.png?raw=true)

5. At this point, you should see a window come up with my models in it.  If you click Simulate Radio, you should see a virtualized Horus X10/S with my models on it.  Controlling it with your keyboard can be a bit confusing to get used to, but you can use your mouse as well.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/simulator.png?raw=true)



# Importing my models onto your radio (Click image for higher quality)
Follow the above steps to view my models, then:

1. Connect your Horus X10/S to your computer.

2. Make sure the radio profile for your radio is selected.  Again, this guide assumes you have already created a profile and flashed your Horus X10/S with OpenTX 2.2.4.  

3.  

2. With your radio connected to the computer and in Mass Storage mode, click the "Read Models and Settings From Radio" in Companion.  This will create an otx tile of your radio called document1.otx.  If this radio has never been used before and has no new models, the file will be empty, but you still need it for this process.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/readmodels.png?raw=true)
3. Open my x10s.otx file in Companion. This will create a second window with my models visible.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/openmine.png?raw=true)
4. Find the model you want to copy from my radio.  Click and drag it onto your radio.  You can also copy and paste the model if click+drag isn't working.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/drag.png?raw=true)
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/copied.png?raw=true)
5. With your radio's model/settings highlighted, hit File>Save or Ctrl+S.  This will save the model to your radio's otx file.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/save.png?raw=true)
6. Press Write Models and Settings To Radio" in Companion.  
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/write.png?raw=true)
7. You're done!
