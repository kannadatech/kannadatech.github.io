---
layout: post
title: "Compiling Kannada documents using XeLaTeX"
date: 2020-06-17
category: typesetting
permalink: xelatex-kannada
---
*These steps are tested on Ubuntu, and they probably will work on Mac.
I will write a separate post for Windows after I get access to a 
Windows machine.*

1. **Install Kannada fonts**\\

   * Go to [Brahmi Downloads](http://brahmi.sourceforge.net/downloads2.html).
   * At the bottom of the page, there are two tables. In the first table, the
     second row has links to download the fonts in a zip file. Download it.
   * Extract the contents of the zip file.
   * Double click on the ttf files. In the new window that opens, look towards the
     top right corner and locate the 'Install' button.
   * Click the Install button. This installs the font.

2. **Install XeLaTex**
   * The easiest way to install XeLaTeX is to download it from the Ubuntu
     software repository by running the following command:

   ```shell
   sudo apt-get install texlive-xetex
   ```
   
   Ubuntu repository generally installs a slightly older version. This
   doesn't cause any problems, but sometimes, you may not be able to install certain
   packages. This happened to me recently, and that's why I decided to get the
   latest version.

   If you are comfortable with basic command line usage, I suggest you to get
   the latest version itself by following the steps given
   [here](https://puttym.github.io/update-texlive).   

  3. **Compile the document**
  * A minimum working example of a TeX file with Kannada text is available
  [here](https://github.com/puttym/berkeley-physics/blob/master/kannada_mwe.tex).
  Please download and save it at an appropriate location.
 * Open a terminal, navigate to the directory in which you have saved the
   above file, and run the following command.

   ```tex
  xelatex kannada_mwe.tex
   ```

  This produces a pdf file with your text neatly printed.

  Congratulations! You just produced your first Kannada document using XeLaTeX.
