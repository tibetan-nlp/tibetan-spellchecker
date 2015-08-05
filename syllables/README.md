# Source files for particle checking

This directory contains the source files on which syllable spellchecking is based.

The files are based on the [documentation](../doc/standard-syllable-structure.md), with the following choices:

- all syllables with wasurs have been listed instead of allowing all wasurs possibilities
- all syllables with suffix འི, འོ, or འུ have been listed instead of allowing them all
- the syllables composed with ཧྤ are allowed, as they appear in many foreign names (country names for instance)
- archaic forms (ད་དྲག, -འིས, etc.) are not included
- Ux0F35 and Ux0F37 are ignored


### Dictionary files (.txt)

These files are in hunspell .dic format (easily parsable) their names should be explicit.

### Suffix files (.json)

This file is in a json format and simply lists the possible suffixes for all suffix types.

### Usage

The currently only way to use these files is through [hunspell](http://hunspell.sourceforge.net/), see [hunspell-bo](https://github.com/eroux/hunspell-bo) for an implementation.

Microsoft officially integrates only dictionaries that have been validated by an official linguistic authority, so this is not currently possible to use this work with Microsoft products.
