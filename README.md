# Setup_for_Archivematica
Generates staging directory for media artworks according to Denver Art Museum naming conventions


You may call the function directly from the terminal, though I have found it more user friendly to use PyInstaller to wrap all dependencies together.

The script prompts a user to drag and drop media files into the terminal, which are then copied to another directory. It uses out a central directory ("big_folder_path = "/YOURPATHHERE"" in line 78) in which individual staging directories for each artwork are added. 

The script creates a sub directory inside /YOURPATHHERE named after the accession number of the artwork, which is typed in by the user after adding the initial file (if no accession number is provided, it will be named after the initial file). Additional files may be added by dragging into the terminal window when prompted. These will be copied into the sub directory.

When each file is added, the script runs a sha256 checksum on the **original** file. This is then added to a text file in a metadata directory in the same sub directory as the files. This is named and formatted according to Archivematica specifications.

I would like to thank Eddy Colloton for teaching me how to ingest artworks into Archivematica, which inspired me to write this script.
