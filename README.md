# Horus X10S OpenTX
This repository contains the SD Card contents from my Horus X10S with OpenTX.  It can be used as a reference or base for setting up your own models.  It also contains the .otx file for Companion 2.2.4 with my models and settings.


LOGO 480 XXtreme Model contains the Lua script necessary for Brain2 OpenTX Integration.

Synergy N556 uses curves instead of channel overrides for throttle.  This is the better way to do things.  Eventually I will do the same with the LOGO.

Synergy N556 has hot-start prevention for use with SwitchGlo.  It will only allow SwitchGlo to ignite if throttle hold is on.



**Settings changed from stock OpenTX:**

-Splash Screen Changed

-Radio Background Changed

-Theme Color Changed from Red to Black

-Removed most default images, since they were not useful to me, and especially not for helis :)


# Model Images for Helicopters can be found in /Images/Model Images.  
Simply put them into your Images folder on your radio's SD Card and you can use it as the image for your model.  You can rename the image, but be aware it must be only 6 characters long in order to be able to use it.  They are all transparent PNG images, which looks really nice when being used as a model image.  If you'd like to make a contribution with your own images, send me an email with the image and I might upload it here.  The correct resolution is 192x106.


# Follow these steps in order to copy one of my models onto your radio (click image for higher quality):

1. Download the x10s.otx file from here.  

2. Open the Companion 2.2 software.

3. Connect your OpenTX radio to your computer.

4. Click the "Read Models and Settings From Radio" in Companion.  This will create an otx tile of your radio called document1.otx.  If you already have one, you can open it.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/readmodels.png?raw=true)
5. Open my x10s.otx file in Companion. This will create a second window with my models visible.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/openmine.png?raw=true)
6. Find the model you want to copy from my radio.  Click and drag it onto your radio.  You can also copy and paste the model if click+drag isn't working.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/drag.png?raw=true)
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/copied.png?raw=true)
7. With your window highlighted, hit File>Save or Ctrl+S.  This will save the model to your radio's otx file.
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/save.png?raw=true)
8. Press Write Models and Settings To Radio" in Companion.  
![](https://github.com/BladeScraper-Designs/Horus-X10S-OpenTX/blob/master/Images/HowTo/write.png?raw=true)
9. You're done!
