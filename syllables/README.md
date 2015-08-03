# Source files for particle checking

This directory contains the source files on which syllable spellchecking is based.

The files are based on the [documentation](../doc/standard-syllable-structure.md), with the following choices:

- all syllables with wasurs have been listed instead of allowing all wasurs possibilities
- all syllables with suffix འི, འོ, or འུ have been listed instead of allowing them all
- the syllables composed with ཧྤ are allowed, as they appear in many foreign names (country names for instance)
- archaic forms (ད་དྲག, -འིས, etc.) are not included
- Ux0F35 and Ux0F37 are ignored


### Dictionary files (.txt)

These files are in a format similar to hunspell .dic files, with the exception that the suffix type may not include the "empty string" suffix (which it always does in hunspell).

### Suffix files (.json)

This file is in a json format and simply lists the possible suffixes for all suffix types.

### Usage

The currently only way to use these files is through [hunspell](http://hunspell.sourceforge.net/), see the [hunspell/](hunspell) directory.

#### Note about Microsoft
  Microsoft officially integrates only dictionaries that have been validated
  by an official linguistic authority. In the case of Tibetan, this is no
  easy thing.

