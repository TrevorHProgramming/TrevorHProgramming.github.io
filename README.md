<HTML>

<HEAD>

<TITLE>Leader-1 Host Site</TITLE>

</HEAD>

<BODY BGCOLOR="#9794b5">

<HR>

<H2>Home of Transformers (2004) (PS2) Hacking Tools</H2>

<P> Tools currently in development will be using this site for their automatic updates. 

<HR>

<H3>TF2004 File Converter</H3>

<P>This program converts game files from the existing proprietary formats more modern, more easily accessible file types. The end goal is to be able to turn those modern file types back into the proprietary formats to modify the game.<br>

Currently supported formats are listed below. Please keep in mind that research is still ongoing; many file types will not have complete information yet.
<ul>
  <li>VBIN, MESH.VBIN, GRAPH.VBIN - model files, can be exported as STL or DAE.</li>
  <li>ITF - texture files, can be exported to most image formats. Can be exported to the original ITF format.</li>
  <li>TMD/BMD, TDB/BDB - database files. Can be edited within the converter. Can be exported to the original formats.</li>
</ul>

Unsupported formats are listed below. Most of these formats require further research before even basic converstion can be started:
<ul>
  <li>VAC - Sound effects. Other programs can convert these with some trial and error.</li>
  <li>FBX - Visual effects. </li>
  <li>BT - Generic binary text files. Not missing research, just not implemented.</li>
  <li>COLLISIONSCENE - probably a collision scene manager. </li>
  <li>ACT - No idea.</li>
  <li>WPB - Related to visual effect placement.</li>
  <li>MS - Audio files.</li>
  <li>TLA/TLB - Audio files.</li> 
</ul>

Downloads:<br>
If you've never downloaded the program before, download this zip for all necessary dll files: <a href="https://TrevorHProgramming.github.io/TF04Converter/TF2004FileConverter-v0-7-0-0.7z">Download</a><br>
If you only need the newest exe, <a href="https://TrevorHProgramming.github.io/TF04Converter/VBINConverter.exe">download the most recent version here</a><br><br>
For more information about the Randomizer, <a href="https://TrevorHProgramming.github.io/Randomizer.html" check here</a><br>

<HR>

5/11/2024
<H3>TF2004 File Converter v0.7.0.0 is here</H3>
<H4>The Randomizer Update</H4>

New Features:
The Randomizer tab now exists. 
The Build tab now exists. This includes options for unpacking and repacking ZIP and ISO files related to the game.

Bugfixes:
Multiple fixes for the Database file system



<HR>

12/25/2023
<H4>TF2004 File Converter v0.6.6.0 is here</H4>

New features:
Model files now export with vertex colors
Database files can be exported to DAE to visualize object placement
Model file heirarchy now exports correctly


<HR>

12/11/2023
<H4>TF2004 File Converter v0.6.5.4 is here</H4>

Fixes:
Corrected binary output for "Link" and "LinkArray" values.


<HR>

12/11/2023
<H4>TF2004 File Converter v0.6.5.3 is here</H4>

New Features:
Dictionary (Definition and Database) files can now (mostly) be edited in the tree view. Enum values still have their own edit button.

Fixes:
Dictionary file exports should be more reliably accurate than before.

Known Issues:
Some of the "Array" types will not display correctly 

<HR>

09/21/2023
<H4>TF2004 File Converter v0.6.5.2 is here</H4>

New Features:
Textures now work on all Graph/Mesh.VBIN files.
Mesh sections for Graph/Mesh.VBIN files now export with names.

Known Issues:
The normals on all VBIN exports are almost correct, but not quite. These will need manual correction after export. 

<HR>

09/14/2023
<H4>TF2004 File Converter v0.6.5.1 is here</H4>

Bugfixes:
MESH.VBIN textures are correctly flipped like normal VBINS.
VBIN files no longer attempt to read animation data (this is still a work in progress).
Normals for VBIN model exports should now be correct. 

<HR>

09/13/2023
<H4>TF2004 File Converter v0.6.5.0 is here</H4>

New Feature(s):
The program can now read and export MESH.VBIN files. Huge thanks to Discord member bbatts for solving the index array issue.

Known Issues:
The program will attempt to assign textures based on the data in the corresponding GRAPH.VBIN file, but this system needs work. Most levels will have no textures assigned, while some will have incorrect textures.

<HR>

09/05/2023
<H4>TF2004 File Converter v0.6.4.2 is here</H4>

New Feature(s):
Some functions now have logging enabled on the right sidebar.<br>
.DAE files now expect .PNG textures on export.

Bugfixe(s):
Program will no longer freeze when reading models with vlLodSwitchers (Cybertron towers, build 3944 level .vbins)<br>
When loading a vbin with no LODs, the dropdown will automatically select "1".<br>
Imported images with indexed color data/color palettes will now export at the correct bit depth. 

<HR>

08/22/2023
<H4>TF2004 File Converter v0.6.4.1 is here</H4>

New Feature(s):
Added a "clear files" option on the menu bar. This will clear out all currently loaded files.

Bugfixe(s):
Corrected version number. The version number is also shown in the title bar.<br>
Mipmaps now properly swizzle.<br>
The palette table now properly updates when converting an image from color to index.<br>
Fixed a crash related to mipmap generation 

<HR>

08/20/2023
<H4>TF2004 File Converter v0.6.4 is here</H4>

Changed the ITF system to use Qt's QImage system. This allows importing and exporting for most common image formats. With this update, there is now a complete toolchain for ITF creation. 

<HR>

07/15/2023
<H4>TF2004 File Converter v0.6.3.1 is here</H4>

Bugfix: TDB and BDB files should now load an export correctly.  

<HR>

06/18/2023
<H4>TF2004 File Converter v0.6.3 is here</H4>

Added auto-updating. Future versions should be downloaded from this site automatically by the program. 

<HR>

05/05/2023
<H4>TF2004 File Converter v0.6.2 is here</H4>

Some bugfixes for the previous version.
Fixes:
VBIN models with sections that are not rendered at lower LODs would crash the program. Now these will instead render at the lowest available level. Also technically a known issue as this is inaccurate to how the model should be. <br>
256 color textures have their palette issues resolved. Still a known issue: there are some textures that are not swizzled, but the program assumes that all ITF files are. There is likely a bit somewhere to indicate whether to swizzle the image or not. <br>
Model sections with a . in the name will be culled to just the name section after the ".". This will allow the DAE format to properly assign textures to these sections. <br>

Known issues:
Files with long extensions (ex .MESH.VBIN) will only read the last extension. This should be a fairly easy fix I just forgot about it and don't have time today<br>
Database files still don't work.

<HR>

05/03/2023
<H4>TF2004 File Converter v0.6.1 is here</H4>

Lots of bugfixes and a couple new features.

New features:
Exporting the file you have selected will have that file chosen by default on the export popup if it's the right file type.<br>
Bulk importer and exporter for VBIN and ITF files. Select a file path and the program will do the rest.

Bug fixes:
Attempting to export a texture while a different texture is selected will no longer crash the program.<br>
Cancelling a file export should actually cancel it, preventing further prompts.<br>
Loading multiple files with the same file name will give them a numbered disambiguation in the file list and export options.<br>
GeometrySets will export all position data instead of just the first set's.<br>
BDB files should now load properly.<br>
UVs should be properly flipped (let me know if this is actually fixed correctly)

Known issues:
256 color textures have swizzling and palette issues. These are still being investigated.

<HR>

04/30/2023
<H4>TF2004 File Converter v0.6 is here</H4>

This update brings a GUI overhaul and the ability to load multiple files at once. For now, this doesn't do much (and actually broke the only type that could load multiple before, database/definition files) but it opens the door for important features later on. The database and definition files can still be opened, but not edited or saved. 

This rework also ripped out a lot of the early code from when I didn't know what I was doing. The correction for database/definition files will be the next area of improvement that isn't driven by new research. We're still working on MESH.VBIN files, their related files, and some details on texture swizzling.

Please let me know of any issues or suggestions. 

<HR>

04/05/2023
<H4>TF2004 File Converter v0.5.4.1 is here</H4>

Bugfixes: 
Meshes that have multiple textures should now export properly to DAE (This was done a while ago but I forgot to upload the updated build, oops)<br>
BMP files should now be correctly oriented on export. This hasn't been as thoroughly tested as it could be so let me know if any textures don't work.

5.4's known issues are still present. I'm doing some work in the background to improve the UI design which will also resolve those issues.

<HR>

03/04/2023
<H4>TF2004 File Converter v0.5.4 is here</H4>

New features:
Can now export VBIN models to .DAE. These DAE files will reference the appropriate textures for that model and will be properly mapped when imported to a program like Blender. <br>
Can now correctly export ITF files to BMP. These will be properly unswizzled and should line up correctly on exported DAE models (if they don't, they should only need to be flipped vertically in an image editor)

Bugfixes:
Can now export most old models and textures.<br>
Cancelling an export to all file types will no longer crash the program<br>
Attempting to save without a loaded file will no longer crash the program.

Known issues:
Attempting to load an ITF file after a VBIN file will result in a crash. <br>
Loading a VBIN file after an ITF file will leave the palette table visible.

<HR>

02/13/2023
<H4>TF2004 File Converter v0.5.3 is here.</H4>

New features:
Added a distance calculator for Amazon warpgates. Enter the X, Y, and Z coordinates of a position on the map and it'll tell you what the closest warpgate is.<br> 
Loading a VBIN file will show a list of animations for that model. These don't currently do anything.

Bugfixes: 
Cancelling an export to STL will no longer crash the program

Known issues:
Cancelling a save for most file types will cause a crash<br>
VBIN files in the PICKUPS folder will not load 

<HR>

02/05/2023
<H4>TF2004 File Converter v0.5.2 is here.</H4>

Bugfixes: 
LOD-less models with multiple elements now export correctly<br>
Models with animation data before their mesh data now read correctly<br>
Scale offsets are now applied before rotation offsets for more accurate exports

<HR>

02/05/2023 
<H4>TF2004 File Converter v0.5.1 is here.</H4>

Patch notes: 
VBIN offsets are now correct. 

Bugfixes:
Multi-file outputs weren't working correctly<br>
VBIN models without LOD levels wouldn't export<br>
Models with SurfaceProperties version 1 or 3 would not read correctly<br>
Models with a mesh as their root instead of a scene node wouldn't export

<HR>

02/04/2023 
<H4>TF2004 File Converter v0.5.0 is here.</H4>

Patch notes: 
Complete overhaul of the VBIN reading system. Read quality should be exactly the same as before, but there's a couple quality of life improvements for both coding and using:<br>
1. You can now load multiple VBIN files at once. When exporting to STL, it will export the file selected on the dropdown. <br>
2. The program should crash less on read fails and instead error out and give an error message. Please let me know if you find files where this happens so I can find out what's up with them. At least one set of models is known to not read, the CybertronTower vbin models in the Cybertron geometry folder, but there are definitely more out there that don't work.

<HR>

10/16/2022 
<H4>TF2004 File Converter v0.4.4 is here.</H4>

Patch notes: 
Added a mode indicator and filename label. These display what the current operation mode is (Model, texture, database, etc) and the last opened file. <br>
Bugfixes for ITF export<br>
Corrected column labels for ITF palette table<br>
Added a color preview to the ITF palette table<br>

<HR>

09/14/2022 
<H4>TF2004 File Converter v0.4.3 is here.</H4>

Patch notes: 
Can now remove classes in definition files and instances in database files. Addition of new items will be Later<br>
Can now set an instances values to "Default", causing it to pull the default values from the definition file<br>
a couple misc bugfixes I found along the way. nothing for vbins this update.

<HR>
