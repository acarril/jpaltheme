![](https://www.povertyactionlab.org/sites/all/themes/JPal/img/J-PAL_logo_main.png?1)

# jpaltheme

`jpaltheme` is a LaTeX program for making Beamer presentations that comply with J-PAL's new branding guidelines. It is designed to be easily implemented and tweaked, while mantaining all the advantages of using LaTeX. Check out a screenshot of the title slide:

![](http://i.imgur.com/aZxX10A.png?1)

## Features

- Easy to [install](https://github.com/acarril/jpaltheme#installation)
- Easier to [use](https://github.com/acarril/jpaltheme#usage)
- Works on Mac, Linux and Windows
- Adheres to J-PAL's new guidelines
- Easy to tweak

## Installation

### Option 1 (easiest)
Option 1 is the easiest, but it is not the most elegant one. It may be suitable if this is the first time you'll use the template or just want to try it once, to see what the fuzz is all about.

To use, simply [download this repository](https://github.com/acarril/jpaltheme/archive/master.zip) to your computer. There's also a download button if you scroll up this page, shown in this screenshot in case you missed it:
![](http://i.imgur.com/nsrqc0V.png)

```bash
$ brew update
$ brew tap karan/karan
$ brew install gitignore
```

### Option 2 (best)
Option 2 is a tiny bit less easy, but much more elegant. You'll install only once, so no copying and pasting all those `sty` files that mess up your presentations' folders.

First step is to [download the contents of this repository](https://github.com/acarril/jpaltheme/archive/master.zip).

Second step is to check where your TeX home directory is. Open either the Command Prompt in Windows or the Terminal in Mac (if you're using Linux then I'm sure you know what to open :). Then copy, paste and execute this command:

```bash
kpsewhich -var-value=TEXMFHOME
```

That will return a directory address, like `/Users/alvaro/Library/texmf` in my case. It will almost certainly end with `/texmf`.  Go to that folder. If the `texmf` folder doesn't exist, you'll have to create it (it's normal).

Third (and final) step is to create a subfolder named `latex` and then inside that one put another named `beamer`. Unpack  the contents you downloaded in the first step into that `beamer` folder. So at the end you should have this directory:

```bash
.../texmf/latex/beamer/jpaltheme
```

If you have any issues with step 2 or 3, I recommend you check [this question](http://tex.stackexchange.com/questions/1137/where-do-i-place-my-own-sty-or-cls-files-to-make-them-available-to-all-my-te) in the tex.SE site.

## Usage

`jpaltheme` corresponds to a Beamer theme, so your document should start with

```bash
\documentclass[10pt]{beamer}
\usetheme{jpal}
```

### Basic usage


```bash
$ joe java    # outputs .gitignore file for java to stdout
```

### Overwrite existing `.gitignore` file

```bash
$ joe java > .gitignore    # saves a new .gitignore file for java
```

### Append to existing `.gitignore` file

```bash
$ joe java >> .gitignore    # appends to an existing .gitignore file
```

### Multiple languages

```bash
$ joe java node osx > .gitignore    # saves a new .gitignore file for multiple languages
```

### Create and append to a global .gitignore file

You can also use joe to append to a global .gitignore. These can be helpful when you want to ignore files generated by an IDE, OS, or otherwise.

```bash
$ git config --global core.excludesfile ~/.gitignore # Optional if you have not yet created a global .gitignore
$ joe OSX SublimeText >> ~/.gitignore
```

### List all available files

```bash
$ joe ls    # OR `joe list`
```

Output:

> actionscript, ada, agda, android, anjuta, appceleratortitanium, archives, archlinuxpackages, autotools, bricxcc, c, c++, cakephp, cfwheels, chefcookbook, clojure, cloud9, cmake, codeigniter, codekit, commonlisp, composer, concrete5, coq, craftcms, cvs, dart, darteditor, delphi, dm, dreamweaver, drupal, eagle, eclipse, eiffelstudio, elisp, elixir, emacs, ensime, episerver, erlang, espresso, expressionengine, extjs, fancy, finale, flexbuilder, forcedotcom, fortran, fuelphp, gcov, gitbook, go, gradle, grails, gwt, haskell, idris, igorpro, ipythonnotebook, java, jboss, jdeveloper, jekyll, jetbrains, joomla, jython, kate, kdevelop4, kohana, labview, laravel, lazarus, leiningen, lemonstand, libreoffice, lilypond, linux, lithium, lua, lyx, magento, matlab, maven, mercurial, mercury, metaprogrammingsystem, meteor, microsoftoffice, modelsim, momentics, monodevelop, nanoc, netbeans, nim, ninja, node, notepadpp, objective-c, ocaml, opa, opencart, oracleforms, osx, packer, perl, phalcon, playframework, plone, prestashop, processing, python, qooxdoo, qt, r, rails, redcar, redis, rhodesrhomobile, ros, ruby, rust, sass, sbt, scala, scons, scrivener, sdcc, seamgen, sketchup, slickedit, stella, sublimetext, sugarcrm, svn, swift, symfony, symphonycms, tags, tex, textmate, textpattern, tortoisegit, turbogears2, typo3, umbraco, unity, vagrant, vim, virtualenv, visualstudio, vvvv, waf, webmethods, windows, wordpress, xcode, xilinxise, xojo, yeoman, yii, zendframework, zephir

### BONUS ROUND: Alternate version control software

Joe isn't **just** a generator for `.gitignore` files. You can use it and its output wherever a SCM is used.

```bash
$ joe java > .hgignore
```

## Contributing

#### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/karan/joe/issues) to report any bugs or file feature requests.

#### Developing

PRs are welcome. To begin developing, do this:

```bash
# make virtual env
$ git clone --recursive git@github.com:karan/joe.git
$ cd joe/
$ python joe/joe.py java
```

#### `tool.sh`

This is a handly script that automates a lot of developing steps.


```bash
USAGE:
  $ tool.sh [-h|--help] COMMAND

EXAMPLES:
  $ tool.sh readme    Generate README.rst from README.md
  $ tool.sh test      Upload release to testpypi
  $ tool.sh prod      Upload release to prod pypi
```

Make sure you have a file `.pypirc` in `~/` in the following format:

    [distutils]
    index-servers =
        pypi
        pypitest

    [pypi]
    repository: https://pypi.python.org/pypi
    username: <<>>
    password: <<>>

    [pypitest]
    repository: https://testpypi.python.org/pypi
    username: <<>>
    password: <<>>




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
