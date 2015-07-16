Tibetan spellchecker
===

This repository provides files for constituting a tibetan spell-checker with the
hunspell format.

This is work in progress, do not use yet!

You might be interested in the different [documents](doc/) though.


## Features

The syllables present in the files are those present in the TDC (see [bibliography](https://github.com/eroux/tibetan-spellchecker/blob/master/doc/bibliography.md)), conforming [standard tibetan rules](https://github.com/eroux/tibetan-spellchecker/blob/master/doc/standard-syllable-structure.md).


## Limitations and Bugs

Some very common words of sanskrit translitterations are not present but might
be in the future, words like པ་དྨ་ or ཀརྨ་.

Only single syllables are considered, not words with multiple syllables. This
could be added, and might be soon, but will only work if syllables of the same
word are separated by non-breaking tsheg (`Ux0F0C`) instead of tsheg (`Ux0F0B`), which
is something rarely used.

If you find a bug, please file a bugreport on [github](https://github.com/eroux/tibetan-spellchecker/issues).


## Thanks

This package is developped with the valuable help of:

- Hélios Hildt
- Xavier Faure             <suizokukan@orange.fr>
- Elie Roux                <elie.roux@telecom-bretagne.eu>

## Using

#### Note about Microsoft
  Microsoft officially integrates only dictionaries that have been validated
  by an official linguistic authority. In the case of Tibetan, this is no
  easy thing.

#### Under Windows

- for Firefox, go in the `firefox/` directory and run make, this will
     build a .xpi extension that you can add to you firefox. The most simple
     way of getting it (without compiling) is on [the project page](https://addons.mozilla.org/fr/firefox/addon/tibetan-spellchecker/)
- for LibreOffice (should work for OpenOffice too), go in the `lo/` directory
     and run make, it will build an `.oxt` extension you can install.
- for Adobe Indesign (>= CS5.5), see the instructions exposed on [this page](http://blog.napsys.com/2012/11/adding-hyphenation-and-spelling.html).
- for MS Word, see above notice. It is possible to make an extension with the
     CSAPI, but this is a tough job, especially since I don't have MS Word. If
     you are ready to help on the topic, please contact the team!

#### Under Linux
- if you are under debian or ubuntu, you can create a `.deb` file by running make in the `debian/`
     directory. Make sure you have `dpkg-dev`, `debhelper` and
     `dictionaries-common-dev` installed. This will make the spellchecker
     available for Firefox, LibreOffice and all applications.
- if you are not, then please file a bugreport against your distribution
     asking for it to package tibetan-spellchecker. The team is ready
     to help for this. In the meantime you can use the Firefox and LibreOffice
     extensions (see above, "Under Windows").

#### Under MacOSX (untested)

 Copy the .aff and .dic files in the `/Library/Spelling` directory.
 Reboot the computer, this way the Huspell files will be loaded when the
 system initializes. This should make the dictionary available for all
 applications (I hope).


##License

This work and the derived files are under the Creative Commons CC0 license,
which is as close to public domain as possible in the country of the authors.
See the [full text](http://creativecommons.org/publicdomain/zero/1.0/legalcode) or the [FAQ](http://wiki.creativecommons.org/CC0).
