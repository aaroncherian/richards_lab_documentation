So, when you walk into the lab:
1. Turn on the treadmill and unlock the clamps on the treadmill
- The clamps stop the treadmill from moving up or down incline wise
- We unlock them so we can home the treadmill (zeroing the incline)
- Loosen the clamps on either side slightly (till about 2 threads are showing)
- Hit the flashing enable button either at the treadmill or the computer to link the computer to the treadmill
a. Homing the treadmill
- Open the treadmill app from the toolbar (Treadmill Control Panel 1.8.7)
- If there are errors, hit okay (errors may appear if you hit the e-stop last)
- Close the app
- Open the app again
- Hit and hold it the blinking downward triangle to home it
- Once the slider looking thingy appears, decline it until it says 'Homed', instead of 'Jog Only' 
- Tighten the clamps again
2. Turn on the forceplates 
- Bottom black two boxes. The blue ones are for the overground, the top three are for the staircase 
3. Turn on cameras 
-  There's a light switch on the wall next to the computer 
- Cameras are warming up when there's no number on the display, they're ready when there is a number on the display 



## Qualisys 
1. Creating a new project
- Open QTM and hit new project
- Always import from another project or you'll have to reconfigure all the hardware 
-- Look for the .qtmproj file for settings (will update with location of best file to use)
- Go to Settings (the gear icon on the left side of the toolbar)
    - Go to input devices > camera systems > calibration > current calibration and press Load Other button and look for .qca file to load in a good calibration for whatever you are doing 
    - We use the good calibration as something to iterate on while we calibration 
- Cntrl + N for new - it will pop up the 2D view of the infrared 
    - Can click into each screen - use Marker and Video views on the right to switch between infrared/RGB. Double click again to exit
    - Can hit 3 or the 3D button in the toolbar on the left to go into 3d view
        - Here you may see the bounding box (the cube around the treadmill) - which cuts off tracking outside of that box. Good to keep the bounding box for us since we have external lights and webcams and such
- Back in the 2d view - on the bottom right is the number of reflections that it sees. The goal here is to have 0. Investigate what the reflection is if it exists. 
    - Move the object if possible, if not mask it
        - To mask, click into the marker view and use the mask tool from the sidebar
- So then put the wooden rig bar thing down on the treadmill - the wooden blocks should make contact with the poles on the back of the treadmill with the arrows facing forward
- Put the L-bracket on the left side of the treadmill. Adjust using the axle if necessary to level out the bubbles 
- Then click into it to test the quality of the reflections as well
    - Use the exposure and flash time/marker threshold to adjust and make sure the reflections are strong
        - Typical exposure would be 130-200, marker threshold of 20-30 (though it can depend on the cameras because some are finnicky)
    - Don't change the settings from the big screen, because it will change it for all the cameras
- Click the wand icon for calibration (cntrl shift alt c)
    - go slow, cover more volume 
    - if alone, use calibration delay 
    - 90 is standard, 90-120 is better
- Wave the wand around (paint, spin, scoop) - keep it movin'
    - It may fail :(
- To check calibration - hit the View Calibration button, and then hit Calibrated Volume button (brown box, Alt 7)
- Tmake new calibration to get out of calibration view,  hit cntrl N to make new one 
- After passing, look at residuals 
    - Good would be under 0.6, great would be under 0.4, concerned/investigate would be 1 or here
    - Camera 3 is typically a little higher 
    - The way to get better is mostly longer calibration times 
- To look further at why calibration failed, can switch into 2D view from the sidebar and play the video to view the calibration in 2d 
- Start a capture using cntrl M (or red button )
    - Make the capture period big 
    - Create a new folder (create a new folder within the Data with the particpiant tag )
    - Add counter if necessary 
    - Click into the trigger to set whether you want the trigger to start or stop things 
- In the project options go processing > 3d tracking, can handle the bounding box here. 
    - minimum ray count per marker is how many cameras need to see a marker for it to be tracked (try and leave it at 2 for treadmill), overground leave at around 3

    
