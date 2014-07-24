---
layout: default
title: Changelog
permalink: /changelog.html
---

# Changelog

## 2.0 alpha

24 July 2014

- added _dbgfunctions to plugin header
- fixed some context menu bugs in the RegistersView
- option to disassemble in uppercase
- color settings for symbol log
- use hexedit colors in ASCII and UNICODE fiels in HexEditDialog
- added various plugin functions
- automatically add plugin callbacks on certain exports (see help)
- updated help
- updated DeviceNameResolver
- added boundary checks on DbgMem* functions (resolved some crash)
- added patches, comments, labels, bookmarks, functions to the toolbar
- speed boost because the memory map is now cached
- allow sorting in every StdTable (References, Symbols etc)
- added simple update checker
- limit size of the log view
- click bullets to enable/disable/remove breakpoints
- fixed a display bug in the title when not inside a module
- fixed attaching (does not hang anymore)
- fixed issue with deleting disabled breakpoints
- fixed an issue with the last breakpoint never removed from the database
- fixed a crash in the string reference functions
- fixed a bug in valapifromstring (test.exe:imagebase now works)
- double click now works better
- double click on breakpoints will follow in CPU
- fixed a display bug in the InfoBox
- breakpoints/bookmarks in the reference view
- fixed focus problem in Goto dialog
- double click on the CIP register will follow it in the CPU
- added font customization options
- fixed a bug with displaying 'rep stosb'
- fixed a display bug when there are no bookmarks/comments etc
- fixed a bug in valtostring, editing CSP will now actually update the stack
- fixed a bug with negative values in 'complex' expressions
- WordEditDialog now allows signed and unsigned decimal editing too
- added callstack
- added 'Patches' to Disassembly context menu
- you can now 'Modify' a value in the stack from the context menu

## 1.9 alpha

07 July 2014

- fixed scroll bar ranges in tables
- support SetThreadName exception
- fixed a very annoying bug on some systems with the '^' character being inserted after the '6' without shift pressed
- re-enabled autocomments (strings etc)
- strings in register view
- search for inter-modular calls
- CALL <jmp.&user32.MessageBoxA> auto label
- shift+click selection
- latest XEDParse version (you can now assemble jumps etc)
- auto-select next instruction after assembling
- assemble -> fill with NOPs
- fixed a bug with the sidebar (jumps going out of the bar have no lines anymore)
- breakpoint menu in dump (hwbp)
- hexdump ASCII/UNICODE are now actually readable (no spaces between characters)
- save previous hexdump view mode to config
- fixed incorrect stack default option (remove your config to apply)
- memory breakpoints are highlighted in the memory map
- copy context menu in every StdTable (not yet in disasm/dump)
- breakpoint context menu in memory map
- follow in dump/disasm context menu in memory map
- removed invalid 'OrdinalX' from symbol view
- section name + module name + rva + label in InfoBox
- list comments/labels/bookmarks/functions in the reference view
- fixed a bug in memfindpattern (thanks to Computer_Angel)
- fixed a crash when deleting all breakpoints
- ctrl+g now works in CPUDump
- fixed a bug with printing the instruction immediat values
- added hex edit dialog
- added binary edit/copy/paste context menu in disasm/dump/stack
- binary fill (with wildcard support)
- added search for -> pattern context menu option
- required administrator in manifest (may resolve some random bugs)
- fully support patching (+ save to file) + advanced patch dialog
- patch import/export
- fixed jmp/call FAR tokenizing
- support 0x prefixed numbers
- added some exception names when an exception is reached
- binary -> fill NOPs in disassembly
- fixed a bug with disassembling on an invalid address
- add support to get the module base (see help)
- updated help, most commands are now documented

## 1.8 alpha

21 June 2014

- added IDA-like sidebar
- color customization
- instruction tokenizing
- allow highlighting of instruction tokens (CTRL+H)
- new register view that highlights changes
- fixed a bug with detaching
- updated BeaEngine
- new database format (JSON + lz4)
- massive performance improvements
- use SHIFT for selection
- small fixes
- project code cleaup
- more API functions

## 1.7 alpha

02 June 2014

- some help updates
- added version information to file
- detach using right click -> detach on the tab you want to detach
- fixed a bug when searching for strings twice (search didn't work)
- fixd a crash on loading an empty script
- fixed a potential overflow while escaping a debug string
- escape the section names from the memory map
- better pattern finder
- added command auto-completion (includes plugin commands)
- removed an annoying log message on clicking a plugin menu
- fixed bugs in GuiSelectionGet & GuiSelectionSet (thanks to ahmadmansoor)
- added commandline support (x64_dbg.exe "c:\program files\test.exe")
- fixed a bug in modbasefromname (thanks to Artic!)
- added status bar API
- added bpdll command
- fixed a bug in DeviceNameResolver
- fixed various bugs in TitanEngine
- fixed a bug with manual functions in the GUI
- added various bridge exports

## 1.6 alpha

13 May 2014

- search for menu in disassembly context menu
- 'ready' instead of 'terminated' on start
- selection API
- updated find, strref and reffind commands
- strings in the stack
- follow in dump/disasm/stack in stack context menu
- force default alignment in SDK
- section names in memory map
- bring debugger to front when paused
- fixed a bug with the '=' sign
- added a line edit window api
- updated TitanEngine (fixes some handle leaks and maybe hanging bugs)

## 1.5 alpha

28 April 2014

- added debug privilege option (TitanEngine)
- fixed a bug with GetFileNameFromHandle ('error starting process (invalid pe?)')
- fixed a bug with attaching to an x32 process from the x64 debugger
- added 'detach' command
- added twords,dqwords,ywords and zwords
- added a menu API for plugins
- movable tabs
- detachable tabs (for example to place a tab on a second screen)
- fixed a bug with [esp]=4 (valtostring)
- fixed a lot of bugs with scripts
- removed result display of the mov instruction
- press enter on a script jump to get to the destination
- basic script syntax highlighting
- added RVA view in disassembly (double click on the address)
- double click on the opcodes to toggle breakpoints
- double click on the disassembly to assemble
- double clikc on the comments to comment
- fixed an annoying bug with searching for referenced strings
- when you use '-1' in the ExceptionRangeDialog it will use 'FFFFFFFF' instead
- better documentation
- added a simple 'find' command for scripts
- added find references to an address (ctrl+r)

## 1.4 alpha

07 April 2014 

- fixed some bugs with references
- added the 'Previous (-)' and 'Next (+)' function (to get back to your previous address of interest). This has a maximum depth of 1024, but it's easy to change this to any other value, since I use dynamic arrays

## 1.3 alpha

04 April 2014

- added reference searching 'ref value[,page]'
- added string reference searching (little button in the upper-right or the command 'strref [page]'
- fixed a bug when you removed all ignored exception ranges.

## 1.2 alpha

30 March 2014

- many small crash fixes (stack overflows etc)
- many fixes regarding the Dump window
- different dump views
- bugs with valfromstring fixed (now much faster)
- latest development version of TitanEngine Community Edition (many, many, many fixes)
- simple thread view
- project design overview (x64_dbg_sceme.vsd), useful for plugin developers
- TLS callback support
- informative window title
- user preferences (eg on which events to break)
- bug with the recent file list fixed
- ignore exception ranges
- debug strings are now displayed (escaped)
- added 'xor' command
- many fixes in the script engine
- simple stack display

## 1.1 alpha

03 March 2014

- simple stack view (no interaction yet, sorry)
- small bugfixes

## 1.0 alpha

24 February 2014 

- better symbol searching
- draft of the reference window (currently only manually adding references using the commands 'refinit' and 'refadd addr,label'
- Sigma fixed the dump window! (dump using the 'dump addr' command)
- small bugfixes

## 0.9 alpha

19 February 2014

- added symbol viewer
- fixed many memory leaks and random crashes (hopefully the random crashes will stay away now)
- added recent file list (thanks to durazell!)
- everything compiled with MSVC2010, also fixed some crashes, don't know why, create a fresh installation
- simple tabbed layout (will be extended later)

## 0.8 alpha

16 February 2014

- DBG: fixed a bug when stopping the currently debugged file
- DBG: fixed a problem with the output symbols
- DBG: undecorated symbol names
- DBG: resolved issue #34 (no more random crashes)
- DBG: added step until return (thanks to RaMMicHaeL for the suggestion)
- GUI: updated breakpoint view to display label+comment
- DBG: fixed a small bug in DebugDisableBPX
- DBG: breakpoint list contains module names without extension
- BRIDGE: changed BridgeAlloc to use WINAPI
- DBG: changed emalloc to use WINAPI
- GUI: added GPUStack files
- GUI: Fixed a display bug in the disassembly

## 0.7 alpha

13 February 2014

- many fixes with the scripting support
- added many general purpose commands (see help)
- added some script commands (msg and msgyn)

## 0.6 alpha

11 February 2014

- scripting support (using the debug commands)

## 0.5 alpha

08 February 2014

- draft implementation of hex dump (by Sigma)
- bugfixes
- generates crash dumps on crash

## 0.4 alpha

28 December 2013

- fixed many, many bugs
- added function analysis (currently manual, select some data, press SHIFT+F)
- attach attach feature (little problems when you close x64_dbg, but works)
- pageup/pagedown in disassembly
- string detection (very basic, no support for UNICODE yet)
- ??? probably some more improvements, check BitBucket for a full changelog

## 0.3 alpha

25 November 2013

- fixed many bugs
- more context menu options (you can now select a HWBP to replace when DRX is full)
- bookmarks (ctrl+d)
- plugin support
- user database is stable, so your labels+comments+bookmarks+breakpoints are saved automatically

## 0.2 alpha

19 November 2013

- GUI hotkeys
- user databases for labels/comments/breakpoints (*.dd64 or *.dd32 files)
- easy context menu in disassembly (to set breakpoints etc)
- many bugfixes
- edit: symbol support (especially for cyberbob)

## 0.1 c

- variables (with regard to the upcoming script feature)
- basic calculations (var*@401000+.45^4A)
- hide debugger (very basic)
- software breakpoints (INT3, LONG INT3, UD2)
- memory breakpoints (read, write, execute)
- hardware breakpoints (access, write, execute)
- stepping (into, over, n instructions)
- rtr (return from function)
- memory allocation/deallocation in the debuggee
- quickly accessing API addresses (GetProcAddress->76E13620)
- highlighting (not yet customizable, but really helpful)
- memory map
- basic module labeling
- import reconstruction (plugin using Scylla)
- drag&drop files
- goto window
- register/flags view with editing support
- quite fast working in really big code pages (tested up to 5GB)
- GUI hotkeys
- dynamic jump arrow (just like OllyDbg)

## 0.1 b

- added Scylla 'plugin' (start scylla with the current process/dll you have loaded)
- fixed many GUI bugs (redraw bugs etc), by Sigma
- fixed this disassembly bug with truncated QWORDS

## 0.1

27 October 2013

- variables, currently command-based only
- basic calculations, can be used in the goto window and in the register edit window. Example: var*@401000+(.45^4A)
- software breakpoints (INT3, LONG INT3, UD2), currently command-only (just type 'bp addr')
- hardware breakpoints (access, write, execute), also command-only
- stepping (over, into, out, n instructions), can be done with buttons/shortcuts
- memory allocation/deallocation inside the debuggee
- quickly access API adresses (bp GetProcAddress)
- syntax highlighting, currently not customizable
- simple memory map (just addr+size+module+protection basically)

