
    Welcome to PSP2600

The Stella team :

   Bradford Mott       Project management and emulation core developer
                       (original author of Stella)

   Stephen Anthony     Author of the SDL port of Stella and emulation core
   Joe D'Andrea        Maintainer of the Solaris build of Stella
   Doodle              Current maintainer of the OS/2 port of Stella
   Mark Grebe          Author/maintainer of the Mac OSX port of Stella
   Erik "Voch" Kovach  Maintainer of the 'stella.pro' game properties file
   Kostas Nakos        Author/maintainer of the WinCE port of Stella
   Darrell Spice Jr.   Original author of the OS/2 port of Stella
   Eckhard Stolberg    Emulation core development
   David Voswinkel     Author of the first PSP port of Stella
   Brian Watson        Emulation core development and debugger support
   Alex Zaballa        Author of the first GP2X port of Stella

   see http://stella.sourceforge.net/ for further informations
   

Author of another PSP port version 

  Ludovic.Jacomme also known as Zx-81 (see http://zx81.zx81.free.fr)


1. INTRODUCTION
   ------------

  Stella is the best emulator of Atari 2600 game console, 
  running on many different systems, such as Linux, Solaris, 
  Windows, MacOS/X WinCE, OS/2, GP2X.

  PSP2600 is a port on PSP of the version v2.2 of Stella. It's based
  on the work of David Voswinkel, who was the first to port Stella to PSP.

  Thanks to Horeus for his beautiful icons and gfx, to the Stella team 
  for this nice emulator, and to all PSPSDK developpers.

  Special thanks to Poem58 and all Atari2600's fans for their help and 
  support, this port wouldn't have been without them ...

  This package is under GPL Copyright, read COPYING file for
  more information about it.


2. INSTALLATION
   ------------

  Unzip the zip file, and copy the content of the directory fw5.x or fw1.5
  (depending of the version of your firmware) on the psp/game, psp/game150, or
  psp/game5xx if you use custom firmware 5.xx-M33.

  It has been developped on linux for Firmware 5.01-m33 and i hope it works also
  for all others M33 firmwares.

  For any comments or questions on this version, please visit
  http://zx81.zx81.free.fr or http://zx81.dcemu.co.uk

  Put your roms files on "roms" sub-directory. 


3. CONTROL
   ------------

3.1 - Virtual keyboard

    PSP        Atari 2600
  
    Cross      Fire
    Triangle   L Diff A 
    Circle     L Diff B
    Square     R Diff A

  LTrigger mapping :
    
    PSP        Atari 2600
      
    Square     Hotkey FPS
    Triangle   Hotkey Load state
    Cross      Hotkey Save state
    Circle     Hotkey swap joystick
    Up         Hotkey flicker
    Down       Hotkey flicker
    Left       Hotkey render
    Right      Hotkey render
    
  RTrigger mapping :
    
    PSP        Atari 2600 
      
    Square     Escape
    Triangle   Reset
    Cross      Hotkey auto-fire
    Circle     Select
    Up         Up
    Down       Down
    Left       Hotkey Dec Fire
    Right      Hotkey Inc Fire

    Analog     Joystick

    LTrigger   Reset
    RTrigger   Select
    
    Press Start  + L + R   to exit and return to eloader.
    Press Select           to enter in emulator main menu.
    Press Start            open/close the On-Screen keyboard

  In the main menu

    RTrigger   Reset the emulator

    Triangle   Go Up directory
    Cross      Valid
    Circle     Valid
    Square     Go Back to the emulator window

  The On-Screen Keyboard of "Danzel" and "Jeff Chen"

    Use Analog stick to choose one of the 9 squares, and
    use Triangle, Square, Cross and Circle to choose one
    of the 4 letters of the highlighted square.

3.2 - IR keyboard

  You can also use IR keyboard. Edit the pspirkeyb.ini file
  to specify your IR keyboard model, and modify eventually
  layout keyboard files in the keymap directory.

  The following mapping is done :

  IR-keyboard   PSP

  Cursor        Digital Pad

  Tab           Start
  Ctrl-W        Start

  Escape        Select
  Ctrl-Q        Select

  Ctrl-E        Triangle
  Ctrl-X        Cross
  Ctrl-S        Square
  Ctrl-F        Circle
  Ctrl-Z        L-trigger
  Ctrl-C        R-trigger

  In the emulator window you can use the IR keyboard to
  enter letters, special characters and digits.


4. LOADING ROM FILES (.A26 or .BIN)
   ------------

  If you want to load rom images in the virtual drive of your emulator,
  you have to put your rom file (with .zip, .bin or .a26 file extension) on your 
  PSP memory stick in the 'roms' directory. 

  Then, while inside Atari 2600 emulator, just press SELECT to enter in the emulator 
  main menu, choose "Load ROM" and then using the file selector choose one game 
  file to load in your emulator. Back to the emulator window, your game should 
  run automatically.


5. LOADING KEY MAPPING FILES
   ------------

  For given games, the default keyboard mapping between PSP Keys and Atari 2600
  keys, is not suitable, and the game can't be played on PSP2600.

  To overcome the issue, you can write your own mapping file. Using notepad for
  example you can edit a file with the .kbd extension and put it in the kbd 
  directory.

  For the exact syntax of those mapping files, have a look on sample files already
  presents in the kbd directory (default.kbd etc ...).

  After writting such keyboard mapping file, you can load them using 
  the main menu inside the emulator.

  If the keyboard filename is the same as the rom file (.a26) then 
  when you load this rom file, the corresponding keyboard file is 
  automatically loaded !

  You can now use the Keyboard menu and edit, load and save your
  keyboard mapping files inside the emulator. The Save option save the .kbd
  file in the kbd directory using the "Game Name" as filename. The game name
  is displayed on the right corner in the emulator menu.

6. FLICKERING 
   ------------

  On several games such as Asteroids or Missile Command, the screen flicks,
  or the color are dark. You can then change the Flicker mode parameters in 
  the Settings menu. For example, Asteroids is very nice using the "Simple"
  anti-flicker mode.


7. CHEAT CODE (.CHT)
   ----------

  You can use cheat codes with this emulator.  You can add your own cheat
  codes in the cheat.txt file and then import them in the cheat menu.  

  All cheat codes you have specified for a game can be save in a CHT file in
  'cht' folder.  Those cheat codes would then be automatically loaded when you
  start the game.

  The CHT file format is the following :
  #
  # Enable, Address, Value, Comment
  #
  1,36f,3,Cheat comment

  Using the Cheat menu you can search for modified bytes in RAM between current
  time and the last time you saved the RAM. It might be very usefull to find
  "poke" address by yourself, monitoring for example life numbers.

  To find a new "poke address" you can proceed as follow :

  Let's say you're playing Moon patrol and you want to find the memory address where
  "number lives" is stored.

  . Start a new game in Moon patrol
  . Enter in the cheat menu. 
  . Choose Save Ram to save initial state of the memory. 
  . Specify the number of lives you want to find in
    "Scan Old Value" field.
    (for Glouton the initial lives number is 3)
  . Go back to the game and loose a life.
  . Enter in the cheat menu. 
  . Specify the number of lives you want to find in
    "Scan New Value" field.
    (for Moon patrol the lives number is now 2)
  . In Add Cheat you have now one matching Address
  . Specify the Poke value you want (for example 3) 
    and add a new cheat with this address / value.

  The cheat is now activated in the cheat list and you can save it using the
  "Save cheat" menu.

  Let's enjoy Moon patrol with infinite life !!

8. COMMENTS
   ------------

  You can write your own comments for games using the "Comment" menu.  The first
  line of your comments would then be displayed in the file requester menu while
  selecting the given file name (roms, keyboard, settings).

9. SETTINGS
   ------------

You can modify several settings value in the settings
menu of this emulator.  The following parameters are
available :

  Sound enable : 
    enable or disable the sound

  Active Joystick : 
    Joystick player, it could be 1 or 2

  Paddle enable :
    enable or disable paddle

  Paddle speed :
    specify paddle speed factor (from 1 to 3)

  Speed limiter :
    limit the speed to a given fps value

  Skip frame : 
    to skip frame and increase emulator speed

  Display fps : 
    display real time fps value 

  Render mode : 
    many render modes are available with different
    geometry that should covered all games
    requirements

  Delta Y : 
    move the center of the screen vertically

  Vsync : 
    wait for vertical signal between each frame displayed

  Flicker mode : 
    set flicker mode (none, simple, phosphor or average)
    
  Swap Analog/Cursor : 
    swap key mapping between PSP analog pad and PSP
    digital pad

  Auto fire period : 
    auto fire period

  Auto fire mode : 
    auto fire mode active or not

  Display LR led : 
    draw a small blue rectangle in top of the screen
    when trigger keys are pressed

  Clock frequency : 
    PSP clock frequency, by default the value is set
    to 222Mhz, and should be enough for most of all
    games.

  
9. COMPILATION
   ------------

  It has been developped under Linux using gcc with PSPSDK. 
  To rebuild the homebrew run the Makefile in the src archive.

