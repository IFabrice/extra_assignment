# Creating the VM

Start creating a brand new VM by running `vagrant up` in this
directory (install Vagrant on your system if needed). This command
creates a _release_ VM that includes P4 software installed from
pre-compiled packages and allows to update those packages with `apt
upgrade`.



Below are steps that were performed _after_ the command above
was run on the host OS, before creating the VM images. 

+ Log in as user p4 (password p4)
+ Click "Upgrade" in the pop-up window asking if you want to upgrade
  the system, if asked.  This will download the latest Linux kernel
  version released for Ubuntu 20.04, and other updated packages.
+ Reboot the system.
+ `sudo apt clean`

+ Log in as user p4 (password p4)
+ Start menu -> Preferences -> LXQt settings -> Monitor settings
  + Change resolution from initial 800x600 to 1024x768.  Apply the changes.
  + Close monitor settings window
    
+ Start menu -> Preferences -> LXQt settings -> Desktop
  + In "Wallpaper mode" popup menu, choose "Center on the screen".
  + Click Apply button
  + Close "Desktop preferences" window
+ Several of the icons on the desktop have an exclamation mark on
  them.  If you try double-clicking those icons, it pops up a window
  saying "This file 'Wireshark' seems to be a desktop entry.  What do
  you want to do with it?" with buttons for "Open", "Execute", and
  "Cancel".  Clicking "Open" causes the file to be opened using the
  Atom editor.  Clicking "Execute" executes the associated command.
  If you do a mouse middle click on one of these desktop icons, a
  popup menu appears where the second-to-bottom choice is "Trust this
  executable".  Selecting that causes the exclamation mark to go away,
  and future double-clicks of the icon execute the program without
  first popping up a window to choose between Open/Execute/Cancel.  I
  did that for each of these desktop icons:
  + Terminal
  + Wireshark
+ Log off

+ Log in as user vagrant (password vagrant)
+ Change monitor settings and wallpaper mode as described above for
  user p4.
+ Open a terminal.
  + Run the command `./clean.sh`, which removes about 6 to 7 GBytes of
    files created while building the projects.
+ Log off


