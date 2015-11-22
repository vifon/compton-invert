compton-invert
==============

A `compton` window compositor wrapper managing the list of windows
with inverted colors.

SYNOPSIS
--------

    # Add Chromium to the list of inverted windows and restart compton
    compton-invert -a Chromium-browser -s -r

    # Invert the colors of an interactively selected window
    compton-invert -Asr

    # Restore the colors of an interactively selected window
    compton-invert -Dsr

DESCRIPTION
-----------

The window list is maintained in `~/.compton-invert`, one window class
per line. The duplicate lines are removed.

**OPTIONS**

* `-a CLASS` -- add a new window class to the list
* `-d CLASS` -- remove a window class from the list
* `-A` -- add a window interactively
* `-D` -- remove a window interactively
* `-l` -- print the window list, including the current modifications
* `-s` -- save the modifications from this call back to the stored list
* `-r` -- restart compton (does not fork); no further options are read

**The `-a` and `-d` switches do not modify the saved list on their
own. Use `-s`.** The order of the arguments matters.

The `-A` and `-D` switches are designed to be bound to some hotkeys.

COPYRIGHT
---------

Copyright (C) 2015  Wojciech Siewierski

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
