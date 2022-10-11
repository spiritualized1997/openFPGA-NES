# Spiritualized NES
NES core for openFPGA on Analogue Pocket
-

NSF playing, FDS games, Vs. Games, and everything else should be supported by this core.

If you wish to play FDS games, make sure the file "fds.bios" is present in your
/nes/common/ folder!  If not, you will get a "file not found" error. 

When loading an FDS file for the first time, it must be processed.  This can
take several seconds. Subsequent loading will be nearly instant.

Loading NSFs can take 2-3 seconds as well.

For Vs. games, press the left trigger (default) to insert coins.

The following interact menu items are present:

Region:

This lets you select one of three regions.  NTSC, PAL, or Dendy.  

The selected region can be overridden if the "auto region"
checkbox is checked.  This setting will allow NES 2.0 headered
games to override the region.

The following types of results can happen:

If the region is set to NTSC, and a PAL game is run, it will be
autoswitched to PAL for that game.  No user interaction is required.

Vice-versa is also true- If the region is set to PAL, and an NTSC
game is run, it will run in NTSC.

Note that the 2.0 header can specify "multiregion".  Codemasters
games are known for their ability to modify behavior based on which system
it is running on.  If a multiregion game is loaded, it will use the
region that you have selected, and will not override it.  

Custom Palette Loading:

Release includes Mono, Nostalgia and NTSC palettes.
Users can add their own .pal files to the palettes folder in Assets\NES\Common.

Overscan:

Checking this box will reduce the visible area of the screen, cutting
some of the top, bottom, and sides off, while resizing the screen so that
dead screen realestate is minimized.

Looped Noise Off:

Checking this box will simulate what a first run Famicom sounds like.
This is audible on games like the Metal Man stage on Megaman 2.  The
metallic instrument will turn into white noise instead.

Square Reset Off:

Checking this will disable the phase reset when the square wave
frequency is reloaded.  Some homebrew games/music don't sound quite as
good if they reload the frequency high byte each frame.  This is also
what gives the Super Mario Bros time countdown that "gritty" sound.
Toggle it on and off during the countdown to hear the difference.

16 Sprites/Line:

Selecting this will allow up to 16 sprites to be visible per line.
It can reduce sprite flicker on certain games.  Beware that some games
actually use the sprite limit to hide things. 

Multicart Mode:

Some multicarts have solder pads on them which can be jumpered to show
different game counts.  This lets you change that.

4 Player Mode:

Using a dock, up to 4 players can play games.  The type of 4 player adapter
can be selected here:  None, Four Score, or Famicom style 4 players.

The 4 player adapter is only enabled if 3 or more controllers are
hooked up to the dock.

FDS Mode:

Selects if automatic or manual disk change is used.

For automatic mode, the disk is automatically flipped and the user does
not have to do anything.

Manual mode requires the user to press the right trigger to change disks.

Most games are fine with automatic mode, but a few do not like it and 
will constantly think the disk is being ejected.  Select this mode if
you run into that.

Enjoy

This core is for the [Analogue Pocket](https://www.analogue.co/pocket) via [openFPGA](https://www.analogue.co/developer).

## Release Notes

* First public release

## Installation
To play NES on your Pocket follow these instructions. 
1. Download and install the latest Pocket firmware here https://www.analogue.co/support/pocket/firmware/1.1-beta-5
2. Unzip the contents onto the root of your Pocket SD Card in the appropriate folders. 
3. You will need to add a FDS bios to your sd card. Name the FDS bios file "fds.bios" and place it in the assets/nes/common folder.
4. Place rom files in the assets/nes/common folder.
5. Power on Pocket and select openFPGA to run the core.
