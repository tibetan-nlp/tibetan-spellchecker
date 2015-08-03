# Tibetan syllable spellchecker for Hunspell 

This directory contains the necessary files to use spell checking for Tibetan at syllable level (not composed words) in [Hunspell](http://hunspell.sourceforge.net/) (used in [many applications](https://en.wikipedia.org/wiki/Hunspell#Uses)).

Note that checking compound words is not possible with hunspell.

## Using

#### Global installation

Under Linux or OSX, you can install the spellchecker globally and benefit from it in all you applications.

- under Linux, copy `bo.dic` and `bo.aff` to `/usr/share/hunspell`. We are trying to make the spellchecker available in Debian/Ubuntu as `hunspell-bo` package (not ready yet).
- Under OSX, copy `bo.dic` and `bo.aff` to `/usr/share/hunspell` to `/Library/Spelling` and restart your computer.

#### Application-specific installation

- for Firefox, [an extension](https://addons.mozilla.org/fr/firefox/addon/tibetan-spellchecker/) will be released (current one is obsolete)
- for LibreOffice/OpenOffice, an extension will be released too
- for Adobe products (>= CS5.5), see the instructions on [this page](http://blog.napsys.com/2012/11/adding-hyphenation-and-spelling.html)

The sources for these extensions are in the [firefox](firefox/) and [lo](lo/) directories.

## Building / Testing

To rebuild `bo.dic` from its sources in parent directory, run

    make bo.dic

For a small test, run

    make test

## Changelog

##### v0.1 - 06/2013

- initial release, contains syllables from the *Bod rgya tshik mdzod chen mo*.

##### v0.2 - 08/2015

- contains all possible standard tibetan syllables (coming from research in grammar books), not limitted to a dictionnary
- replacement proposals for archaic forms
- main proper name syllables (not including Sanskrit translitterations)

##License

This work and the derived files are under the Creative Commons CC0 license,
which is as close to public domain as possible in the country of the authors.
See the [full text](http://creativecommons.org/publicdomain/zero/1.0/legalcode) or the [FAQ](http://wiki.creativecommons.org/CC0).
