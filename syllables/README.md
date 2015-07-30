# Source files for particle checking

This directory contains the source files on which syllable spellchecking are based.

The files are based on the [documentation](../doc/standard-syllable-structure.md), with the following choices:

- all syllables with wasurs have been listed instead of allowing all wasurs possibilities
- all syllables with suffix འི, འོ, or འུ have been listed instead of allowing them all
- the syllables composed with ཧྤ are allowed, as they appear in many foreign names (country names for instance)

### Dictionary files (.txt)

These files are in a format similar to hunspell .dic files, with the exception that the suffix type may not include the "empty string" suffix (which it always does in hunspell).

### Suffix files (.json)

This file is in a json format and simply lists the possible suffixes for all suffix types.
