This is a copy of what exactly the LifeDriveMgr does when working with files over USB. 

LiveConnect is a local DCOM application on Windows (you can find it and configure it under Component Services). 

This testing was done on Windows 11, LDMgr has a issue with deleting files under W11, wherein it'll crash due to a problem with MFC42.dll; so file deleting could not be tested.

First I began capturing the packets on USB 1.19 (Palm Handheld), then launched LifeDriveMgrTray (which then launches PalmOneLiveConnect with the "-Embedding" switch).
Then I navigated to the Documents directory through LDMgr (on the LD, not on the SD Card named "Recovery"). 

I copied "palmwiki.txt" (a text version of the Wikipedia article for Palm, Inc.) to the Documents directory. The request for that begins at 176 or so (or at least when the file name appears, the 
beginning of the request likely starts before that).

I then copied "palmpdf.txt" (a pdf converted version of the same article) to the Documents directory, the file name appears at 278.

I copied both files back to my PC, this time to the desktop, the PDF was copied first, file name appears at 380. The text file appears at 420.

Even though both files (should) be the same, there are 2 copies in this folder, one being transfered to the LD, the other being copied from the LD. 

Not sure if any of this is of practical use, but this theoretically could enable a custom cross-platform "LDMgr" that's far more stable than the original (and does not require the device to be
in drive mode).



