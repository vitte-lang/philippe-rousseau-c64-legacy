               README for the Windows version of SIDPLAY
              ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

                     October 30 version (1998)

This file isn't meant as a complete manual, simply as a brief
description of the features of SIDPLAY/Windows



                      What is SIDPLAY/Windows?


SIDPLAY is a music player and SID chip emulator written by
Michael Schwendt <sidplay@geocities.com>. For info
on SIDPLAY and SID files, go to the SIDPLAY home page at
http://www.geocities.com/SiliconValley/Lakes/5147/

SIDPLAY/Windows is a port of SIDPLAY to the MS Windows environment. The Windows
port and user interface is written by Adam Lorentzon <d93-alo@nada.kth.se>.



INSTALLATION

Simply copy the SIDPLAYW.EXE file to a directory of your choice, add an
icon to it and you're done. If you wish to run the 32-bit version under
Windows 3.1, you will need Win32s. It can be obtained from Microsoft at
http://www.microsoft.com/ . The 32-bit version is almost twice as fast
as the 16-bit version.
If you want SIDPLAY to start playing a file when it is double-clicked,
you need to associate the file extension (usually .dat) with SIDPLAY:
Windows 3.1: In the File Manager, choose File|Associate, enter the extension,
press Browse, browse to where you put SIDPLAYW.EXE and press OK.
Windows 95: In the Explorer, hold the shift key and right-click on a file
with the extension you want to associate. Choose Open With, press Browse,
browse to where you put SIDPLAYW.EXE and press OK.


USAGE - DESCRIPTION OF THE MENU

The file menu has five entries: Open, Save as, Conversion,
  Properties and Exit.

File|Open:                  (Shortcut  -  Alt + O or Ctrl + O)
  Opens a standard Windows file open dialog, from which you can choose
  a sid music file to open and start playing. If you open a SIDPLAY playlist,
  it will be loaded and the first entry will start playing.

File|Save as:               (Shortcut  -  Ctrl + S)
  Asks for a filename and the type of file to be saved. If no extensions is
  specified, the extension corresponding to the chosen file type will be
  added to the filename before saving.
  If the Windows PCM file format is chosen, a WAV file is saved using
  the settings in the Settings|Wav dialog box. During the creation of the
  WAV file, a progression dialog will show how much is done. It also has a
  cancel button, which if pressed will abort the save process and delete
  the partially saved WAV file. (Note that the old shortcut for saving WAV
  files, Alt + W, still works although the explicit menu option is removed.)

File|Conversion:            (Shortcut  -  Alt + C)
  Dialog for converting sid files to a specified format.
  For example, suppose you've got a dir full of sid files in DAT+SID format.
  Use the filter to show all *.dat files, set destination directory to the
  same as the source, convert all files with the overwrite option, making
  the PSID files (.sid) overwrite the old .sid files, and the delete source
  files option, removing the old .dat files and you've replaced all DAT+SID
  files with a corresponding SID file in PSID format. Be a little careful
  with the overwriting and deleting though, make sure you have a backup if
  something goes wrong.

File|Properties:
  Shows information about the sid file currently loaded.

File|Exit:                  (Shortcut  -  Alt + X)
  Terminates the program.

---
The view menu controls which windows apart from the main window that are
  shown. It has four entries: Mixer, Filter, Directory-based UI and Playlist.

View|Mixer:
  In the mixing dialog, you can control the volume level and the Left-Right
  panning of the individual SID voices here. Panning is not available in
  mono. If HQ mixing mode is selected you only have limited control over the
  panning, a sort of blending of the left and right stereo channels.
  With manual panning, you can set the panning position of each voice.
  With auto-panning, the panning position changes during the duration of the
  note, creating cool effects. Centered auto-panning works like auto-panning,
  except that the pan position starts in the middle, which gives a more
  balanced, not so jumpy, mix.
  Switching off the mixer uses a somewhat faster algorithm.

View|Filter:
  This window controls the three parameters to the adjustable SID-filter
  emulation. You can also switch off the filter to gain speed.

View|Directory-based UI:    (Shortcut  -  Alt + D)
  Toggles a file-selection window which looks like the main window in
  SIDPLAY/DOS. Use the mouse or the arrow keys to select a drive, directory
  or file and press enter or double-click to change to the selected drive/
  directory or start playing the selected file. Backspace takes you up one
  directory. Entering an alphanumeric key highlights the first entry that
  begins with that character. Repeated use of the same key will highlight
  the next entry beginning with that character. Pressing the Filter button
  lets you choose which files that will be shown in the directory window.
  If you press the delete-key when a file is selected, a confirmation box
  will appear, and if you select Yes the file will be deleted.  

View|Playlist:
  This window shows the current playlist. Double-click an entry to play it.
  Press the Edit button to open the Playlist Edit dialog.

---
The settings menu is for configuring the program and has six entries:
  Play, Wav, Emulation, Directory UI, Extensions and Device.

Settings|Play:
  Controls the quality of the sound: frequency, resolution and channels:
    Frequency can be chosen between 4000 and 48000 Hz.
    8-bit or 16-bit output.
    Mono or stereo output.
  The number and size of buffers can be increased if the music is stuttering,
  and there are gaps in the music when you're running other programs. If you
  want faster response time, lower the size of the buffers.
  Higher frequency, stereo and 16-bit output all increase the CPU demand,
  so you might have to do with a little lower sound quality if you have a
  486 or a slow Pentium.

Settings|Wav:
  Here you set the type of WAV file that will be written when you choose
  File|Save as WAV. You also choose how long the WAV file will be in seconds.
  Be careful not to record too long files - the required filesize is shown
  at the bottom of the dialog.

Settings|Emulation:
  Memory model: This option controls how the bank-switching works. Full bank-switching
    is just like the real commodore. The other options are provided for compatibility.
  Clock speed: PAL and NTSC commodores plays some sids at different speeds.
    Without the force clock speed option checked, this setting doesn't matter
    (actually, for sids that use the CIA timer, the speed will differ with factor
    of 1.038). SIDPLAY will play the sids as the composer intended them to sound.
    If you want to hear the music at the same speed it played on your commodore,
    choose clock speed and check the force play speed option.
  Waveforms:
    The combined waveforms will use a table lookup with values recorded from
    a MOS-6581 R4 (old SID chip) or a MOS-8580 R5 (new SID chip),
    depending on this choise.
  Measured ADSR envelope master volume: Using measured values instead of theoretical.
  For more information about the emulation settings, please visit the SIDPLAY home page.

Settings|Directory UI:
  Configure the appearance of the files in the Directory UI. Select between
  short or long filenames, lower, upper or mixed(original)-case filenames.
  Select the order in which the files, directories and drives appear in the
  listbox.

Settings|Extensions:
  This dialog lets you specify which extensions SIDPLAY will use
  for the different file formats. These extensions will be used in the
  File|Open, File|Save As and File|Conversion dialogs.
  (AWB stands for Amiga Workbench icon + ASCII info strings)

Settings|HVSC:
  If you have the High Voltage SID Collection on your hard disk, use this
  dialog to tell SIDPLAY in which directory the collection resides.
  This is also where the settings for the STIL View are found. You can
  customize the type of STIL entries to be shown and whether the STIL View
  window should auto-size, and in that case, what maximum height it will
  auto-size to. More information about STIL in the chapter below about
  STIL View.

Settings|Device:
  If you have several audio devices installed on your system, you may want
  to select the one with the best audio capabilities. Here you can choose
  between the installed devices.

---

The help menu has only one entry: About.

Help|About:
  Shows information about the program, such as authors, whether it is
  the win16, win32s or win32 version, which version of the emulation engine
  is used and what date it was created.
  It also shows how long you have listened to SID music:
  First line shows how much you've listened the current session,
  last line shows how much you've listened since you installed the April 24 version.
  The value is stored in the SIDPLAYW.INI file, so if you want to keep the
  statistics, don't delete it when you upgrade.


USAGE - OTHER

A filename can be given on the command line, so associating SIDPLAY
with the .sid extension might be a good idea. If you have SIDPLAY
open you can drag a sidfile or playlist from the File Manager (Explorer in
Windows 95) and drop it on the main window and it will start playing.



PLAYLIST EDITOR:

To the left is the directory window. Use this to navigate to the sidtunes you
want to add to the playlist. To the right is the playlist.
    Adding sidtunes to the playlist:
To add sids to the list, mark them in the directory window and press the [Add]
button. Double-clicking a single sid will also add it. Press the [Add all] button
if you want to add all the sids in the directory to the list. If the "Add subsongs"
checkbox is marked, adding a sid with subtunes will add an entry to the list for
each subtune. If there is a number in the "Default playtime" edit box, the added
entries will have the same playtime as in the box.
    Removing sidtunes from the playlist:
Doubleclick an entry, or highlight it and press [Remove] to remove it from the list.
[Remove all] will empty the list.
    Ordering the tunes in the list:
Highlight a tune and press the [Up] or [Down] button to move it towards the beginning
or the end of the list.
    List properties:
If the "Repeat" check box is marked, the list will start playing from the beginning
of the list when it has reached the end. Otherwise it stops.
Normal play order means that the entries are played in the same order as they are in
the list. Random order means that each time there is time to choose a new entry, it
is randomly chosen from the list.
    List entry properties:
Highlight a list entry to see its properties: the filename of the sid file, the name,
author and copyright of the sid, the subsong that will be played and the time it will
be played. The subsong and playtime can be edited.
    Loading and saving playlists:
Straightforward - press the [Load] button to load a new playlist or the [Save] button
to save the current list. NOTE: when a new list is loaded, or the program is terminated,
the changes made to the playlist will be lost unless they're saved first. No warning
will be issued!



STIL VIEW:
The High Voltage SID Collection (HVSC) has a file, STIL.txt, in the DOCUMENTS
directory. STIL is short for SidTune Information List. From the FAQ (STIL.faq):
  " The SID Tune Information List (STIL) contains information about the SID
tunes in the HVSC besides the standard TITLE, AUTHOR, and COPYRIGHT
information. STIL goes a little deeper listing SID tune information that only a
true SID freak would enjoy. Such information listed in STIL includes cover
information, interesting facts, useless trivia, comments on the tunes by the
composers themselves, etc. STIL is limited to factual data and does not try to
provide an encyclopedia about every original artist. "
  The STIL View shows the information in the STIL about the current sid loaded.
The various types of information to be shown can be turned on/off in the
Settings|HVSC dialog. If the STIL View is set to auto-size, the window will
adjust its size to show the entire STIL entry. Because some STIL entries are
quite long, there is a maximum height that the STIL View will auto-size to,
also adjustable from the settings dialog. Double-clicking in the STIL View
window closes it.
  The STIL View also shows entries from the BUGlist.txt document, with information
about tunes in the HVSC that are incomplete or flawed.
  If you want to add to, or correct the STIL, please read the STIL.faq document
in the DOCUMENTS directory of the HVSC.



TABLE OF SHORTCUT KEYS:

Alt+P     = Play/Pause
Alt+S     = Start/Stop playing
Ctrl+O    = Open file
Alt+O     = Open file
Ctrl+S    = Save as
Alt+W     = Save as Wav
Alt+C     = The conversion dialog
Alt+D     = Show/Hide the directory window
Alt+X     = Terminates the program
Alt+Left  = Previous entry in playlist
Alt+Right = Next entry in playlist
Alt+Up    = Next subsong
Alt+Down  = Previous subsong
Alt+1     = 1x play speed
Alt+2     = 2x play speed
Alt+4     = 4x play speed

GLOBAL HOTKEYS: (works even when SIDPLAY is in the background)

Ctrl+Alt+P     = Play/Pause
Ctrl+Alt+S     = Start/Stop playing
Ctrl+Alt+Left  = Previous entry in playlist
Ctrl+Alt+Right = Next entry in playlist
Ctrl+Alt+Up    = Next subsong
Ctrl+Alt+Down  = Previous subsong

Instead of Ctrl+Alt, you can use the [Alt Gr] key, so
[Alt Gr]+P		= Play/Pause, and so on.
---

DISTRIBUTION SITES

For the latest version of SIDPLAY/Windows, look at these places. The WWW
page will have the new version first, as well as the past and future of
SIDPLAY/Windows. It also contains PSID files for use with SIDPLAY, and
links to other SID resources on the net.

  WWW: http://www.student.nada.kth.se/~d93-alo/c64/spw
  BBS: Point of No Return  Node 1 (28k8) +49-6039-95934
                           Node 2 (ISDN) +49-6039-95935

For extensive SIDPLAY and sid music information, like the file formats
supported by SIDPLAY, information about how to rip SID music from games
or demos and much more, don't miss the original
                     -= SIDPLAY WWW Home Page =-    at
            http://www.geocities.com/SiliconValley/Lakes/5147/

For the greatest collection of SID tunes on this planet, get
The High Voltage SID Collection at
            http://www.dhp.com/~shark/c64music/


---

THANKS TO

  Michael Schwendt for everything
  LaLa for the STIL View
  All betatesters for finding bugs, making suggestions and general motivation
  Jonathan Hunt for drawing the nice icon
  Alpaslan Deveci (Kris/Clique) for additional icons
  All C64 composers for the groovy tunes
  Sid rippers and sid collection organizers for making them available
   (esp. the High Voltage SID Collection crew)


---

CONTACTING THE AUTHOR

If you have questions, comments, suggestions or bug reports, don't hesitate
to mail me at d93-alo@nada.kth.se .

The C64 WWW Games page at http://www.student.nada.kth.se/~d93-alo/c64/
has links to most C64 resources on the net. Try it!

Be well!

/ Adam Lorentzon   <d93-alo@nada.kth.se>
