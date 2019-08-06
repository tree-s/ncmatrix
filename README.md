## NCMatrix
Section: User Commands (1)
Updated: 2019.08.06

* * *
[ ]()

### NAME
NCMatrix - A network monitoring screen saver (derived from CMatrix by Chris Allegretta) [ ]()

### SYNOPSIS
**ncmatrix** [-abBflohnsVx] [-u update] [-C color] [-H threshold] [-I netdev] [-R color] [-T color] [ ]()

### DESCRIPTION
Shows a console mode scrolling 'Matrix' like screen in Linux with optional network packet activity. [ ]()

#### OPTIONS
_-a_ Asynchronous scroll

_-b_ Bold characters on

_-B_ All bold characters (overrides -b)

_-f_ Force the linux $TERM type to be on

_-l_ Linux mode (sets "matrix.fnt" font in console)

_-o_ Use old-style scrolling

_-h, -?_ Print usage and exit

_-n_ No bold characters (overrides -b and -B)

_-s_ "Screensaver" mode, exits on first keystroke

_-x_ X window mode, use if your xterm is using mtx.pcf

_-V_ Print version information and exit

_-u delay_ Screen update delay 0 - 9, default 4

_-C color_ Use this color for matrix (default green). Valid colors are green, red, blue, white, yellow, cyan, magenta and black.

_-I netdev_ ncmatrix will display transmitted and received packets as different colored characters entering the matrix. You must use the -I option to tell ncmatrix what netork device to monitor. This device must exist in /proc/net/dev and you must have read access to it. examples would be:

   -I ppp0   
   -I eth0   
   -I eth1   

_-H threshold_ This threshold will tell ncmatrix to wait a number of times before computing the total number of packets that have been transmitted or recieved since the last time it checked netdev. On slow connections, this can cause ncmatrix to intersperse single characters into the matrix. We want a nice stream of chars to represent the network data. Setting the -H number higher *should* minimize the number of sparse characters entering the matrix. Depending on your processor speed and network speed, this can vary greatly. An H value of 1000 on my AMD 1.8Ghz was not noticeable. On a Pentium 266 with no H value (more intensive) the load was around 17%.

_-R color_ Use this color for coloring received packets (default blue). Valid colors are green, red, blue, white, yellow, cyan, magenta and black.

_-T color_ Use this color for transmitted packets (default red). Valid colors are green, red, blue, white, yellow, cyan, magenta and black.[ ]()

#### KEYSTROKES
The following keystrokes are available during execution (unavailable in -s mode)

_a_ Toggle asynchronous scroll

_b_ Random bold characters

_B_ All bold characters

_n_ Turn off bold characters

_0-9_ Adjust update speed

_! @ # $ % ^ & )_ Change the color of the matrix to the corresponding color: ! - red, @ - green, # - yellow, $ - blue, % - magenta, ^ - cyan, & - white, ) - black.

_q_ Quit the program
