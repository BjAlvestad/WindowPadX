Modified fork of WindowPadX
==========
This repo is a slightly modified fork of WindowPadX (by hoppfrosch), which in turn was a modified fork from WindowPad (by Lexikos)

It is a useful tool for managing windows when using several monitors.<br>
Window placement works fine also when using monitors with differen scaling (in Windows 10).

# Shortcuts
Capslock is the main modifier used, and must be pressed before the other key combinations.<br>
I.e. `Alt + CapsLock` is not the same as `CapsLock + Alt`. <br>
However `CapsLock + Ctrl + Shift` is the same as `CapsLock + Shift + Ctrl`.

## Misc.
- `CapsLock + Tab`:  Togle window *always on top*
- `CapsLock + Space`:  Toggle *transparent* window
- `CapsLock + Enter`:  Toggle *maximize* window
- `LeftMouse + RightMouse`:  Signal where mouse cursor is

### Mouse cursor
- `CapsLock + Alt + 1-6`:  Move *mouse cursor* to center of monitor 1-6
- ``CapsLock + ` ``:  Togle clip cursor to current monitor (NB: currently buggy)

## Moving windows
### Moving windows between monitors
- `CapsLock + 1-6`:  Move *active* window to monitor 1-6
- `CapsLock + Shift + 1-6`:  Move *previous* window to monitor 1-6
- `CapsLock + Ctrl + Shift + 1-6`:  Move *all* windows to monitor 1-6

### Moving window arround on current monitor
Windows are placed with letterkeys based on the following logic:
- Upper row places window at top with 50% height. Double tap for 70% height.
- Middle row places window with full height.
- Bottom row places window at bottom with 50% height. Double tap for 30% height.

#### Spanning from L/R monitor
- `CapsLock + q-u, a-j, z-m`:  Places window from monitor edge with widths L30, L50, L70, 100, R70, R50, R30.
- `CapsLock + i/k`:  Backup alternatives for `v` and `r` (full width top and full width bottom), but with a width of 99 instead of 100 (some windows may have issues moving with width 100 due to windows get made a bit wider due the invisible boarders. Ref. pull request "pacobyte:windows-10-border-fix" in original repo).
 
#### Spanning from offset (30) from monitor edge
- `CapsLock + Alt + e,r,t, d,f,g, c,v,b`:  Places window at 30% offset from edge with widths L20, 40, R20.

 Intended to be used in conjuction with normal window spanning 30 from edge (`CapsLock + q,a,z u,j,m`).

# How to edit shortcuts / functions
- Shortcuts gets defined in WindowPadX.ini file.
- If it is nessecary to modify a function, most of the methods reside in the WPXA.ahk file. <br>
Be warned however that the code is a bit messy and would benefit from refactoring if any major work is to be done.

<br>
<br>
<br>

# Original ReadMe for WindowPadX
This is a modified version of AutoHotkeyX, and the readme above is written for the modified version - for original ReadMe, see below.

-----------------------------------------------------------------------------------------------------------

Detailed Documentation can be found here: http://hoppfrosch.github.com/WindowPadX/files/WindowPadX-ahk.html

Introduction
------------

***WindowPadX*** is an enhancement of ***WindowPad***, originally released by Lexikos (see: http://http://www.autohotkey.com/forum/viewtopic.php?t=21703)

***WindowPadX*** is a tool which provides some useful functionality within multi monitor environments.

Features
--------
- Possible actions to be configured on hotkeys
    - Window actions
      - Multi-Monitor
          - WPXA_MoveWindowToMonitor: Move window between screens, preserving relative position and size.
          - WPXA_MinimizeWindowsOnMonitor: Minimize all windows on the given Screen
          - WPXA_GatherWindowsOnMonitor: "Gather" windows on a specific screen.
          - WPXA_FillVirtualScreen: Expand the window to fill the virtual screen (all monitors).
      - General
          - WPXA_MaximizeToggle: Maximize or restore the window.
          - WPXA_TopToggle: Toggles "AlwaysOnTop" for given window
          - WPXA_RollToggle: Toggles "Roll/Unroll" for given window
          - WPXA_Move: move and resize window based on a "pad" concept.
          - WPXA_TileLast2Windows: Tile active and last window
    - Mouse actions
      - Multi-Monitor
          - WPXA_MoveMouseToMonitor: Moves mouse to center of given monitor
          - WPXA_ClipCursorToCurrentMonitorToggle: Toogles clipping mouse to current monitor
          - WPXA_ClipCursorToMonitor: Clips (Restricts) mouse to given monitor
      - General
          - WPXA_MouseLocator: Easy find the mouse 

For more details see http://hoppfrosch.github.com/WindowPadX/files/WindowPadX-ahk.html
