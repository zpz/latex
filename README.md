# latex

LaTeX style files and utilities from older times.

----


Update: most tex things I have written are now stored directly under $TEXMFHOME.

This directory contains LaTeX style files and class files I develop.
The installation may also contain third party packages that do not come
with the system by default.
However, only things that have been written or hacked by me are stored
in this directory.

Subdirectory 'fonts' has its own Makefile and should be run seperately,
because installing fonts are slower than simple copying,
and its content is not changed that often.

Two very basic documents are the 'teTeX manual' and the 'TeX Directory Structure'.

The personal texmf tree is pointed to by TEXMFHOME (used to be HOMETEXMF).
The full search path is TEXMF, in which TEXMFHOME comes very early in the list.

The distribution tree is usually /usr/share/texmf-tetex
Use it as a model for the directory structure of the personal tree.

Most useful commands:

Everytime after you make changes to you personal tree, 
update the file database by
$ texhash $TEXMFHOME

For the teTeX manual, run
$ texdoc TETEXDOC

To see the definition of teTeX environ variables, run
$ texconfig conf

After font-related changes, run
$ updmap
$ updmap --enable Map=<mapfile.map>
$ updmap --disable <mapfile.map>

