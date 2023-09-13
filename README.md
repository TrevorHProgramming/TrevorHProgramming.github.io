<HTML>

<HEAD>

<TITLE>Leader-1 Host Site</TITLE>

</HEAD>

<BODY BGCOLOR="9794b5">

<HR>

<H2>Home of Transformers (2004) (PS2) Hacking Tools</H2>

<P> Tools currently in development will be using this site for their automatic updates. Ideally, this site will also become a usable interface for the Leader-1 Discord bot. 

<HR>

Downloads:
If you've never downloaded the program before, download this zip for all necessary dll files: <a href="https://TrevorHProgramming.github.io/TF04Converter/TF2004FileConverter-v0-6-5-0">Download</a>
If you only need the newest exe, <a href="https://TrevorHProgramming.github.io/TF04Converter/VBINConverter.exe">download the most recent version here</a>

<HR>

09/13/2023
<H3>TF2004 File Converter v0.6.5.0 is here</H3>

New Feature(s):
The program can now read and export MESH.VBIN files. Huge thanks to Discord member bbatts for solving the index array issue.

Known Issues:
The program will attempt to assign textures based on the data in the corresponding GRAPH.VBIN file, but this system needs work. Most levels will have no textures assigned, while some will have incorrect textures.

<HR>

09/05/2023
<H3>TF2004 File Converter v0.6.4.2 is here</H3>

New Feature(s):
Some functions now have logging enabled on the right sidebar.
.DAE files now expect .PNG textures on export.

Bugfixe(s):
Program will no longer freeze when reading models with vlLodSwitchers (Cybertron towers, build 3944 level .vbins)
When loading a vbin with no LODs, the dropdown will automatically select "1".
Imported images with indexed color data/color palettes will now export at the correct bit depth. 

<HR>

08/22/2023
<H3>TF2004 File Converter v0.6.4.1 is here</H3>

New Feature(s):
Added a "clear files" option on the menu bar. This will clear out all currently loaded files.

Bugfixe(s):
Corrected version number. The version number is also shown in the title bar.
Mipmaps now properly swizzle.
The palette table now properly updates when converting an image from color to index.
Fixed a crash related to mipmap generation 

<HR>

08/20/2023
<H3>TF2004 File Converter v0.6.4 is here</H3>

Changed the ITF system to use Qt's QImage system. This allows importing and exporting for most common image formats. With this update, there is now a complete toolchain for ITF creation. 

<HR>

07/15/2023
<H3>TF2004 File Converter v0.6.3.1 is here</H3>

Bugfix: TDB and BDB files should now load an export correctly.  

<HR>

06/18/2023
<H3>TF2004 File Converter v0.6.3 is here</H3>

Added auto-updating. Future versions should be downloaded from this site automatically by the program. 

<HR>

05/05/2023
<H3>TF2004 File Converter v0.6.2 is here</H3>

Some bugfixes for the previous version.
Fixes:
VBIN models with sections that are not rendered at lower LODs would crash the program. Now these will instead render at the lowest available level. Also technically a known issue as this is inaccurate to how the model should be. 
256 color textures have their palette issues resolved. Still a known issue: there are some textures that are not swizzled, but the program assumes that all ITF files are. There is likely a bit somewhere to indicate whether to swizzle the image or not. 
Model sections with a . in the name will be culled to just the name section after the ".". This will allow the DAE format to properly assign textures to these sections. 

Known issues:
Files with long extensions (ex .MESH.VBIN) will only read the last extension. This should be a fairly easy fix I just forgot about it and don't have time today
Database files still don't work.

<HR>

05/03/2023
<H3>TF2004 File Converter v0.6.1 is here</H3>

Lots of bugfixes and a couple new features.

New features:
Exporting the file you have selected will have that file chosen by default on the export popup if it's the right file type.
Bulk importer and exporter for VBIN and ITF files. Select a file path and the program will do the rest.

Bug fixes:
Attempting to export a texture while a different texture is selected will no longer crash the program.
Cancelling a file export should actually cancel it, preventing further prompts.
Loading multiple files with the same file name will give them a numbered disambiguation in the file list and export options.
GeometrySets will export all position data instead of just the first set's.
BDB files should now load properly.
UVs should be properly flipped (let me know if this is actually fixed correctly)

Known issues:
256 color textures have swizzling and palette issues. These are still being investigated.

<HR>

04/30/2023
<H3>TF2004 File Converter v0.6 is here</H3>

This update brings a GUI overhaul and the ability to load multiple files at once. For now, this doesn't do much (and actually broke the only type that could load multiple before, database/definition files) but it opens the door for important features later on. The database and definition files can still be opened, but not edited or saved. 

This rework also ripped out a lot of the early code from when I didn't know what I was doing. The correction for database/definition files will be the next area of improvement that isn't driven by new research. We're still working on MESH.VBIN files, their related files, and some details on texture swizzling.

Please let me know of any issues or suggestions. 

<HR>

04/05/2023
<H3>TF2004 File Converter v0.5.4.1 is here</H3>

Bugfixes: 
Meshes that have multiple textures should now export properly to DAE (This was done a while ago but I forgot to upload the updated build, oops)
BMP files should now be correctly oriented on export. This hasn't been as thoroughly tested as it could be so let me know if any textures don't work.

5.4's known issues are still present. I'm doing some work in the background to improve the UI design which will also resolve those issues.

<HR>

03/04/2023
<H3>TF2004 File Converter v0.5.4 is here</H3>

New features:
Can now export VBIN models to .DAE. These DAE files will reference the appropriate textures for that model and will be properly mapped when imported to a program like Blender. 
Can now correctly export ITF files to BMP. These will be properly unswizzled and should line up correctly on exported DAE models (if they don't, they should only need to be flipped vertically in an image editor)

Bugfixes:
Can now export most old models and textures.
Cancelling an export to all file types will no longer crash the program
Attempting to save without a loaded file will no longer crash the program.

Known issues:
Attempting to load an ITF file after a VBIN file will result in a crash. 
Loading a VBIN file after an ITF file will leave the palette table visible.

<HR>

02/13/2023
<H3>TF2004 File Converter v0.5.3 is here.</H3>

New features:
Added a distance calculator for Amazon warpgates. Enter the X, Y, and Z coordinates of a position on the map and it'll tell you what the closest warpgate is. 
Loading a VBIN file will show a list of animations for that model. These don't currently do anything.

Bugfixes: 
Cancelling an export to STL will no longer crash the program

Known issues:
Cancelling a save for most file types will cause a crash
VBIN files in the PICKUPS folder will not load 

<HR>

02/05/2023
<H3>TF2004 File Converter v0.5.2 is here.</H3>

Bugfixes: 
LOD-less models with multiple elements now export correctly
Models with animation data before their mesh data now read correctly
Scale offsets are now applied before rotation offsets for more accurate exports

<HR>

02/05/2023 
<H3>TF2004 File Converter v0.5.1 is here.</H3>

Patch notes: 
VBIN offsets are now correct. 

Bugfixes:
Multi-file outputs weren't working correctly
VBIN models without LOD levels wouldn't export
Models with SurfaceProperties version 1 or 3 would not read correctly
Models with a mesh as their root instead of a scene node wouldn't export

<HR>

02/04/2023 
<H3>TF2004 File Converter v0.5.0 is here.</H3>

Patch notes: 
Complete overhaul of the VBIN reading system. Read quality should be exactly the same as before, but there's a couple quality of life improvements for both coding and using:
1. You can now load multiple VBIN files at once. When exporting to STL, it will export the file selected on the dropdown. 
2. The program should crash less on read fails and instead error out and give an error message. Please let me know if you find files where this happens so I can find out what's up with them. At least one set of models is known to not read, the CybertronTower vbin models in the Cybertron geometry folder, but there are definitely more out there that don't work.

<HR>

10/16/2022 
<H3>TF2004 File Converter v0.4.4 is here.</H3>

Patch notes: 
Added a mode indicator and filename label. These display what the current operation mode is (Model, texture, database, etc) and the last opened file. 
Bugfixes for ITF export
Corrected column labels for ITF palette table
Added a color preview to the ITF palette table

<HR>

09/14/2022 
<H3>TF2004 File Converter v0.4.3 is here.</H3>

Patch notes: 
Can now remove classes in definition files and instances in database files. Addition of new items will be Later
Can now set an instances values to "Default", causing it to pull the default values from the definition file
a couple misc bugfixes I found along the way. nothing for vbins this update.

<HR>
