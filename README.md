HaSuite is a collection of tools for MapleStory.

To build HaSuite, you need at least Visual Studio 2013 (.NET 4.5.1 and Visual C++ Runtimes 2013). You must build it in AnyCPU mode, otherwise you will have to copy apng32.dll/apng64.dll from the AnyCPU build directory to the correct path.

To run HaSuite, you need .NET 4.5.1 and Visual C++ Redistributable 2013.

Helpful stuff:
[Tutorial/sample video of HaCreator2](https://youtu.be/0VrzpvPV8MI)
[The map shown in the video](http://www.mediafire.com/download/bxc3z0st7mpsi4m/BEST+MAP+NA.ham)

Important - Version support and Prerequisite
This version has been tested and is known to work on Windows 7, with MapleStory v83 running MoopleDev r120. It should also work with older MapleStory versions, up until v0.01/Beta (I have personally tested it on Data.wz-based clients, including Beta 0.40), and on newer versions up until Big Bang.
All versions after the Big Bang (~90) are not guaranteed to be supported; I know for fact that the current GMS version/whatever Extalia is using crash when loading. I am not interesting in adding support for them either (see roadmap for more details). If you have the time, you may implement the required fixes and open a pull request.

Why not support newer versions/why bother working on this if it doesn't support contemporary versions?
I personally think MapleStory has gone downhill rapidly starting with the big bang patch, which brought it to the point where it is no more the game I used to call MapleStory, but rather an entirely different game that I have no interest in. Also, in the race to support the newest versions, many complicated features must be added and little attention is paid to old features. v83 seems like a nice checkpoint to set as a reference version and try to implement to perfection.
The main reason I took the time and finished this project is not to do anything particularly useful with it, as I do not play MapleStory anymore and have no interest in it. However, I did feel like not completing the project has been a failure on my part, and I wanted to have a completed HaCreator for future reference.

Roadmap - where are we going from here
Since I do not have any actual use for this project, and I wish to invest as little time in it as possible from now on, and since I have implemented everything I had in mind, the code is from now on feature-frozen. This means that no new features, major code changes or improvements will be added - not by me, at the very least. With that said, I will stay around for a month or two to do basic maintenance, after which I will take my leave, hopefully for good this time.

In particular I want to bring HaCreator to a high UI quality - so if you encounter any bugs, crashes, weird UI mishaps (even simple things such as wrong tab ordering or hotkeys that do not do what you expect them to do), post here. As for HaRepacker, I will only fix major bugs/crashes; if you encounter any, post them here too.

List of features in HaCreator/Hotkey reference
-Opening and editing existing maps, including MapLogin
-Handling of all map elements as of v83 (tooltips, clocks, areas/swimareas), including all mapinfo nodes
-Copy/cut/paste (Ctrl+C, Ctrl+X, Ctrl+V)
-User objects (drop an image file onto the map and have it automatically added as an in-game object)
-Saving (apparently not a trivial feature to have in a map creator)
-Saving and loading to/from a custom file format, *.HAM (based on JSON serialization). Note - you should load HAM files on the same maple version they were saved on, or risk crashes.
-Editing of map items' internal attributes - double click/right click on an item to see.
-Snapping of almost anything, tiles, footholds, ropes, "connect" objects, chairs, etc.
-Not relying on any external libraries such as DotNetBar/XNA (apart from .NET 4.5.x and Visual C++ Redistributable 2013, which you should install as always)
-Automatic backup of original WZ files and odin-style XML exporting when repacking
-Should work without Administrator/UAC (but you must be running as admin if you want HaRepacker to configure itself as the default file association for *.wz)
