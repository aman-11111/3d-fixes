# 3DMigoto Blender add-on
Expands on DarkStarSword's Blender add-on, 3DMigoto Frame analysis dump with Multi-VB export and Multi-games support

- Add a "VB Format" drop down list to 3DMigoto Frame Analysis dump (vb.txt + ib.txt) import dialog which support game specific VB format.
- VB Formats are defined in a dictionary in code: Supports conversion of mis-labelled dump element names and formats to the correct values. 
- 3 game VB formats are defined:
-       God of War 2018    -> lightly tested
-       State of Decay 2   -> has an unknown element "ATTRIBUTE13". exported multi-VBs mesh has deformed black shadow in game
-       FFVII Remake       -> untested  
-  Add a "Flip Face" check box to import dialog for game mesh that shows inside out in Blender. Export mesh will reverse this action.
-  Original Add-on can import Frame analysis dump that with multiple VBs  (one ib.txt  with multiple *-vb[n].txt and *-vb[n].buf). 
-  Add support for exporting Multi-VBs mesh as raw buffers, create multiple *-vb[n].vb files, each with its corresponding *-vb[n].fmt file. 
-  Exception: If all VBs in a multi-VBs mesh have the same layout and stride size. it will be exported as one single .vb with one .fmt file insteads.
-  3DMigoto raw buffer import (.vb + .ib ) search for mulitple -vb[n].fmt files and import the .ib with *-vb[n].vb files.   
