WARNING
=======
THIS IS AN OUTDATED PROJECT, PLEASE TAKE A LOOK TO THE NEW [Midi23D](https://github.com/XDrake99/Midi23D)

<br><br><br><br><br>

OVERVIEW
========
This is a hacked version of Tim Gipson's awesome mid2cnc code to support 3D printers. You can choose over three different playing modes: 4axes, 3axes, Zaxis
mid2cnc requies a MIDI file; Miles Lightwood has found that this workflow is effective on OS X 10.5.8, YMMV:

1. Obtain the song you want as a PowerTab guitar tablature file. Search for .ptb or gp4 files using your favorite search engine
2. Use Tablatures or other application to convert tablature file to MIDI file
3. Use mid2cnc to convert MIDI file to gcode file.

INSTRUCTIONS
============
Usage with "4axes" printer_mode (default):
python ./mid2cnc.py midifile gcodefile machine_ppi_x machine_ppi_y machine_ppi_z machine_ppi_e tone_multiplier tempo_multiplier tune_motors_mode
Example:
python ./mid2cnc.py music.mid output.gcode 100 100 800 100 1.0 1.0 no

Usage with "Zaxis" printer_mode:
python ./mid2cnc.py midifile gcodefile machine_ppi tone_multiplier tempo_multiplier
Example:
python ./mid2cnc.py music.mid output.gcode 800 1.0 1.0

Usage with "3axes" printer_mode:
python ./mid2cnc.py midifile gcodefile machine_ppi_x machine_ppi_y machine_ppi_z tone_multiplier tempo_multiplier tune_motors_mode
Example:
python ./mid2cnc.py music.mid output.gcode 100 100 800 1.0 1.0 no

You may have to experiment with the ppi value to get the song right.
To tune these values you might change the last "no" argument to "yes": in this way you force the program to run the same sound to all the motors.

RESOURCES
=========
mid2cnc - http://tim.cexx.org/?p=633 (Also read the mid2cnc_readme.txt file)
PowerTab files - http://www.ultimate-guitar.com/tabs/
MakerBot Music group - http://groups.google.com/group/makerbotmusic
MakerBot Music - http://wiki.makerbot.com/makerbot-music

THANKS
======
Slowhand (http://www.instantpowertabs.de.vu) for the "Man On The Silver Mountain" source PowerTab file
Aladin for the "Tour de France" source guitar tab file
And last, but not least, T. R. Gipson (drmn4ea at google mail) for the awesome mid2cnc code on which to hack.
