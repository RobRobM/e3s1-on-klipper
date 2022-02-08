# e3s1-on-klipper
## Creality Ender 3 S1 running on Klipper, Moonraker and Fluidd (Mainsail is another great option)

# THIS IS A WORK IN PROGRESS

This is a continuous journey, getting the Ender 3 S1 running as consitantly as possible on Klipper.

All these settings are for my specific setup. For example my printer is facing me sideways  (see picture). But they can be altered to fit yours. I will not be responsible if the files don't meet your setup or if they break your machine. 

These are file I'm currently using with my Ender 3 S1.

I'll try list all guides and documents I used. And list links to all addons I downloaded or created for my setup.

A lot of the printer.cfg and macros and here comes from or was created with help from so many helpful people on Discord, Reddit. 

Right now I am genuinely enjoying this the speed and quality of prints it is producing. I hope you do too.

I hope these files help getting started with klipper on your Ender 3 S1. Even if it is just one person.

Thanks to all and happy printing!


## Documentation:
- https://www.klipper3d.org/
- https://docs.fluidd.xyz/installation/fluiddpi
- https://3dprintbeginner.com/how-to-install-klipper-on-ender-3-s1/

## Steps after installing klipper and Fluidd/Mainsail
Follow all steps for probe calibration first. https://www.klipper3d.org/Probe_Calibrate.html So you can set the offset of the crtouch and nozzle in the printer.cfg

Get the bed as level as possible:
In your printer.cfg in the [bed_mesh] section, set you mesh_min and max to your liking. 
I tried to do the leveling the same spots the nozzle can reach. 
Since there is an offset with the crouch the probe can reach more of the left side of the bed than the right. 
I tried to have the margins that the probe does not reach similar. 
(I hope this makes sense 😃) 

I set my probe count to 3, 3 for the fastest bed mesh calibration.

Then I prepared to level the bed as much as possible. I turned the knobs all the way counterclockwise. Warmed the bed to 60° C
Then at the tune page of Fluids I initiated calibrate. And tuned each corner a corner at a time to the exact same height 0.00something.
After this I changed the probe count to 10,10 so the mesh is as accurate as possible.

Run the mesh calibration an save_config My mesh has a wavy form 🤔

Then calibrate the z-offset. https://www.klipper3d.org/Probe_Calibrate.html

After this I started the bed level calibration from super slicer.

I have mashed together a start print gcode that runs the bed leveling calibration every 10 prints.

I also lowered the first layer speed to 15 and first layer infill to 25 in super slicer.

First layer problems have been solved since these steps.
