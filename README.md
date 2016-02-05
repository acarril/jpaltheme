# J-PAL Beamer Theme

## README

J-PAL Theme
Author: Alvaro Carril
Contact: acarril@povertyactionlab.org
Revision: 02/02/2016


DISCLAIMER

Please note that this theme was independently developed by me, with very helpful comments and guidance from Amanda Kohn. Nevertheless, this is not an official J-PAL theme. This software is in alpha stage and lots of things may not work as intended (or at all). Please write an email if you encounter problems or have any comments.

This theme is based on the Metropolis theme by Matthias Vogelgesang.


USAGE

In order to use this theme, all the files in the "jpaltheme" folder must be placed in the same folder as your main tex file. The files are:

- beamercolorthememetropolis.sty
- beamerfontthememetropolis.sty
- beamerinnerthememetropolis.sty
- beamerouterthememetropolis.sty
- beamerthemejpal.sty
- swirl.png

The main tex file should then start with
	\documentclass{beamer}
	\usetheme{jpal}
	
Finally, it is highly recommended to compile the document using XeLaTeX.

MINIMAL

A minimal example of the theme is contained in the "minimal" folder. This is a barebones document intended to show how to get started. Trying to compile this is a good way to start using the theme (remember to use XeLaTeX!).


DEMO

A demo document is contained in the "demo" folder, which showcases many typical elements of LaTeX documents and how they are displayed using the theme. There's also mention of some guideline elements, but it is not intended to be a full guide. Please refer to the official document for a full rundown of all those guidelines.
