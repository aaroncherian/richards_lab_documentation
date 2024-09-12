
# Qualisys Setup

## Creating a New Project
1. Open QTM and select 'New Project'.
    - Always import from an existing project to avoid reconfiguring hardware.
    - Look for the `.qtmproj` file for settings (update location of the best file to use).

## Loading Calibration
1. In the toolbar, go to Settings (gear icon) > Input Devices > Camera Systems > Calibration.
2. Press 'Load Other' and find a `.qca` file to load a good calibration.

## 2D and 3D Views
1. Press `Ctrl + N` for a new 2D view of infrared.
2. Switch between infrared and RGB views using the Marker and Video view options on the right.
3. Enter 3D view by pressing `3` or selecting the 3D button in the toolbar.
    - The bounding box restricts tracking outside of this box.
    - Keep the bounding box due to external lights and webcams.

## Dealing with Reflections
1. Check the number of reflections in the bottom right of the 2D view. Aim for 0 reflections.
2. Investigate reflections and mask objects if necessary.
    - Use the mask tool in the marker view.

## Wooden Rig Setup
1. Place the wooden rig bar on the treadmill.
    - Ensure the wooden blocks contact the poles on the back of the treadmill.
    - The arrows should face forward.
2. Place the L-bracket on the left side of the treadmill.
    - Adjust with the axle if necessary to level out the bubbles.

## Calibration Process
1. Adjust exposure, flash time, and marker threshold to strengthen reflections.
    - Typical exposure: 130-200, marker threshold: 20-30.
2. Avoid adjusting settings from the main screen, as it affects all cameras.
3. Start calibration using `Ctrl + Shift + Alt + C`.
    - Move the wand slowly and cover a larger volume for better calibration.
4. Check calibration residuals.
    - Ideal: under 0.6, Excellent: under 0.4, Investigate: around 1.
    - Camera 3 tends to have slightly higher residuals.

## Starting a Capture
1. Press `Ctrl + M` or use the red button to start a capture.
2. Create a new folder within the Data directory and label it with the participant's tag.
3. In Project Options, go to Processing > 3D Tracking.
    - Set the minimum ray count per marker to 2 for treadmill use and 3 for overground.
