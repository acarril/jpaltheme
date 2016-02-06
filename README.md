![](https://www.povertyactionlab.org/sites/all/themes/JPal/img/J-PAL_logo_main.png?1)

# jpaltheme

**`jpaltheme` is a LaTeX program for making Beamer presentations that comply with J-PAL's new branding guidelines.** It is designed to be easily implemented and tweaked, while mantaining all the advantages of using LaTeX. Check out a screenshot of the title slide:

![](http://i.imgur.com/aZxX10A.png?1)

Pretty cool, huh?

## Features
- Adheres to J-PAL's new guidelines
- Waaay cooler than ~~Powerpoint~~
- Easy to [install](https://github.com/acarril/jpaltheme#installation)
- Easier to [use](https://github.com/acarril/jpaltheme#usage)
- Fun to [configure](https://github.com/acarril/jpaltheme#configuration)!

## Installation

### Option 1 (easiest)
Option 1 is the easiest, but it is not the most elegant one. It may be suitable if this is the first time you'll use the template or just want to try it once, to see what the fuzz is all about.

The **first step** is simply to [download this repository](https://github.com/acarril/jpaltheme/archive/master.zip) to your computer. There's also a download button if you scroll up this page, shown in this next screenshot in case you missed it:
![](http://i.imgur.com/nsrqc0V.png)

**Second step** is to uncompress the contents. That's it. Now you can just run the `*.tex` files contained in the `minimal` or `demo` folders. See the [usage](https://github.com/acarril/jpaltheme#usage) section for more information.

### Option 2 (best)
Option 2 is a tiny bit *less easy*, but much more elegant. You'll install only once, so no copying and pasting all those `*.sty` files that mess up your presentations' folders.

**First step** is to [download the contents of this repository](https://github.com/acarril/jpaltheme/archive/master.zip).

**Second step** is to check where your TeX home directory is. Open either the Command Prompt in Windows or the Terminal in Mac (if you're using Linux then I'm sure you know what to open :). Then copy, paste and execute this command:

```bash
kpsewhich -var-value=TEXMFHOME
```

That will return a directory address, like `/Users/alvaro/Library/texmf` in my case. It will almost certainly end with `/texmf`.  Go to that folder. If the `texmf` folder doesn't exist, you'll have to create it (it's normal).

**Third** (and final) **step** is to create a subfolder named `latex` and then inside it create another one named `beamer`. Unpack the `jpaltheme` folder from the `*.zip` file you downloaded in the first step (here's [another chance](https://github.com/acarril/jpaltheme/archive/master.zip)) into that `beamer` folder. At the end you should have this structure:

```bash
.../texmf/latex/beamer/jpaltheme
```

If you have any issues with steps 2 or 3, I recommend you check [this question](http://tex.stackexchange.com/questions/1137/where-do-i-place-my-own-sty-or-cls-files-to-make-them-available-to-all-my-te) in the [tex.SE site](http://tex.stackexchange.com/).

## Usage

There are various ways to try out your brand new installation of `jpaltheme`, but **always compile using XeLaTeX!**

### Basic usage

If you installed using **Option 1**, then all the files of the `jpaltheme` folder must be placed in the same folder as your main `*.tex` file. The files are:

- `beamercolorthememetropolis.sty`
- `beamerfontthememetropolis.sty`
- `beamerinnerthememetropolis.sty`
- `beamerouterthememetropolis.sty`
- `beamerthemejpal.sty`
- `swirl.png`

Now if you installed with **Option 2**, there's nothing extra to do! Just open a brand new `*.tex` file.

Without regard of the installation method, `jpaltheme` provides the `jpal` Beamer theme, so your document should start with

```latex
\documentclass{beamer}
\usetheme{jpal}
...
```

If you know what you're doing, then this should suffice you &mdash; beam away! Just remember to compile with XeLaTeX.

### Minimal

If you want to try out the J-PAL theme, I suggest you start with the `minimal` folder. In there, compile `jpaltheme_minimal.tex` (again, using XeLaTeX).

`minimal` showcases a barebones example of a document using `jpaltheme`, so that's why I called it "minimal". Creative naming right there. This should compile a boring but easy-to-understand document.

Trying to compile this is a good way to start using the theme, specially if you're (kind of) new to LaTeX.

### Demo

If you want to see all the nitty gritty details of what `jpaltheme` can do, then I suggest checking `jpaltheme_demo.tex`, located in the `demo` folder. As always, remember to compile using XeLaTeX.

The `jpaltheme_demo.tex` file showcases many typical elements of LaTeX documents and how they are displayed using this theme. There's also mention of some guideline elements, but it is not intended to be a complete guide. Please refer to the official document for a full rundown of all those guidelines.

## Configuration

[I'm working to get this part finished!]

## Unimportant stuff

### Author

I'm [Alvaro Carril](https://www.povertyactionlab.org/carril), research analyst at the J-PAL Latin America & The Caribbean office. I like econometrics, TeX, Stata and computer stuff.

If you have any suggestions, criticisms, doubts or fears, feel free to email me at [acarril@povertyactionlab.org](mailto:acarril@povertyactionlab.org).


### Disclaimer

Please note that this theme was independently developed by me, with very helpful comments and guidance from [Amanda Kohn](https://www.povertyactionlab.org/kohn), Senior Multimedia and Graphic Design Associate at J-PAL. However, I'm solely responsible for this product and all the errors I'm sure it contains.

**This is not an official J-PAL product** and you should always consult the powers that be prior to using it. This software is in beta stage and lots of things may not work as intended (or at all). Please [write an email](mailto:acarril@povertyactionlab.org) if you encounter problems.

This theme is based on the [Metropolis theme](https://www.ctan.org/pkg/beamertheme-metropolis) by Matthias Vogelgesang. Make sure to check out his template if you dig this one, but don't have anything to do with J-PAL... [or apply to work with us!](https://www.povertyactionlab.org/careers)
