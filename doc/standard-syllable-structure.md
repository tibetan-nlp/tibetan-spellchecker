## Standard Tibetan Syllable Structure

This document describes the syllable structure of standard Tibetan. It is made from a computer engineering point of view, and tries to include all cases. This document aims at standardizing the vocabulary used to describe the different syllable parts, and to help parsing and validating standard Tibetan.

The syllable is composed of (in this order):
- zero or one prefix
- a main stack, composed of:
  - zero or one subscript letter
  - one main letter
  - zero or one subscript letter
  - zero or one second subscript letter
  - zero or one explicit vowel
- zero or one suffix
- zero or one second suffix
- zero or one grammatical suffixes

### Reference

The reference book on this is TSH, see [bibliography](https://github.com/eroux/tibetan-spellchecker/blob/master/doc/bibliography.md) for reference. The author of this page doesn't have a direct access to this book.

### Prefixes

A prefix can be:

- ག
- ད
- བ
- མ
- འ

### Main stack

#### main letter

The main letter can be any of the standard tibetan consonants (ཀ, ཁ, ག, ང, ཅ, ཆ, ཇ, ཉ, ཏ, ཐ, ད, ན, པ, ཕ, བ, མ, ཙ, ཚ, ཛ, ཝ, ཞ, ཟ, འ, ཡ, ར, ལ, ཤ, ས, ཧ, ཨ).

#### superscript letter

A subscript letter is written above the main letter. For example རྒ decomposes in subscript ར above main letter ག.

Subscript letters are (combination with main letter ཀ in parenthesis)

- ར (རྐ)
- ལ (ལྐ)
- ས (སྐ)

#### subscript letter

Subscript letters are written below the main letter. They are (combination with main letter ཀ in parenthesis):

- ཡ (ཀྱ)
- ར (ཀྲ)
- ལ (ཀླ)
- ཝ (ཀྭ)

#### second subscript letter

The second subscript letter appears under the first subscript, it cannot appear without a first subscript. It can only be ཝ.

#### Explicit vowels

Explicit vowels appear on top or bottom of the main stack. At most one explicit vowel appears per syllable. Explicit vowels are (combined with ཀ):

- ཀི
- ཀོ
- ཀེ
- ཀུ

## Suffix

A suffix can appear after the main stack, it can be:

- ག
- ང
- ད
- ན
- བ
- མ
- འ
- འུ
- འི (extremely rare as a full part of the syllable, example: ཀྭའི་)
- འོ (extremely rare as a full part of the syllable, example: བྲའོ་ or སླེའོ་)
- ར
- ལ
- ས

## Second suffix

The second suffixes ས and ད (archaic) can appear only after a suffix.

## Grammatical suffixes

The following grammatical suffixes can appear if the syllable have no suffix, or suffix འུ, འོ, འི or འ (first suffix འ disappears if a grammatical suffix is present):

- འི
- འོ
- འང
- འམ
- ར
- ས

Some archaic forms can also be found:

- འིས
- འའིས (only when འ is suffix)
- འར (only when འ is suffix)


## Constraints

For a Tibetan syllable to be valid, it must respect a few constraints:

### Constraints on superscript and subscript letters

The only valid combinations of superscript + main + subscript + second subscript letters are:

- the main letters without superscript nor subscript nor second subscript letters
- the following stacks:
  - རྐ རྒ རྔ རྗ རྙ རྟ རྡ རྣ རྦ རྨ རྩ རྫ
  - ལྐ ལྒ ལྔ ལྕ ལྗ ལྟ ལྡ ལྤ ལྦ ལྷ
  - སྐ སྒ སྔ སྙ སྟ སྡ སྣ སྤ སྦ སྨ སྩ
  - ཀྭ ཁྭ གྭ ཉྭ ཏྭ དྭ ཙྭ ཚྭ ཞྭ ཟྭ རྭ ལྭ ཤྭ སྭ ཧྭ
  - ཀྱ ཁྱ གྱ པྱ ཕྱ བྱ མྱ
  - ཀྲ ཁྲ གྲ ཏྲ ཐྲ དྲ པྲ ཕྲ བྲ མྲ ཤྲ སྲ ཧྲ
  - ཀླ གླ བླ ཟླ རླ སླ
  - རྐྱ རྒྱ རྨྱ
  - སྐྱ སྒྱ སྤྱ སྦྱ སྨྱ
  - སྐྲ སྒྲ སྣྲ སྤྲ སྦྲ སྨྲ
  - གྲྭ རྩྭ ཕྱྭ སྟྭ དྲྭ

The source is [the list by Chris Fynn](https://sites.google.com/site/chrisfynn2/home/tibetanscriptfonts/thetibetanwritingsystem/tibetanlettercombinations), merged with NT and TSH.

Note that TSH doesn't list ཏྭ, ཙྭ, སྭ (found in བསྭ་སྒྲ་), མྲ, ཤྲ, སྟྭ (found in སྟྭ་རེ་) nor དྲྭ (contraction of དྲ་བ་).

### Constraints on prefix and superscript letter

The only valid combinations of prefix + superscript letter + main letter + subscript + second subscript are (in alphabetical order): 

  - ཀ ཀྱ ཀྲ ཀླ དཀ དཀྱ དཀྲ དཀླ བཀ བཀྱ བཀྲ བཀླ རྐ རྐྱ ལྐ སྐ སྐྱ སྐྲ བརྐ བརྐྱ བསྐ བསྐྱ བསྐྲ
  - ཁ ཁྱ ཁྲ མཁ མཁྱ མཁྲ འཁ འཁྱ འཁྲ
  - ག གྱ གྲ གླ དག དགྱ དགྲ བག བགྱ བགྲ བགླ མག མགྱ མགྲ འག འགྱ འགྲ རྒ རྒྱ ལྒ སྒ སྒྱ སྒྲ བརྒ བརྒྱ བསྒ བསྒྱ བསྒྲ
  - ང དང མང རྔ ལྔ སྔ བརྔ བསྔ
  - ཅ གཅ བཅ ལྕ
  - ཆ མཆ འཆ
  - ཇ མཇ འཇ རྗ ལྗ བརྗ
  - ཉ གཉ མཉ རྙ སྙ བརྙ བསྙ
  - ཏ ཏྲ གཏ གཏྲ བཏ བཏྲ རྟ ལྟ སྟྭ སྟ བརྟ བལྟ བསྟ
  - ཐ ཐྲ མཐ འཐ
  - ད དྲ གད བད མད མདྲ འད འདྲ རྡ ལྡ སྡ བརྡ བལྡ བསྡ
  - ན གན མན རྣ སྣ སྣྲ བརྣ བསྣ
  - པ པྱ པྲ དཔ དཔྱ དཔྲ ལྤ སྤ སྤྱ སྤྲ
  - ཕ ཕྱ ཕྲ འཕ འཕྱ འཕྲ
  - བ བྱ བྲ བླ དབ དབྱ དབྲ འབ འབྱ འབྲ རྦ ལྦ སྦ སྦྱ སྦྲ
  - མ མྱ མྲ དམ དམྱ དམྲ རྨ རྨྱ སྨ སྨྱ སྨྲ
  - ཙ གཙ བཙ རྩ སྩ བརྩ བསྩ
  - ཚ མཚ འཚ
  - ཛ མཛ འཛ རྫ བརྫ
  - ཝ
  - ཞ གཞ བཞ
  - ཟ ཟླ གཟ བཟ བཟླ
  - འ
  - ཡ གཡ
  - ར རླ བརླ
  - ལ ལྭ
  - ཤ གཤ བཤ
  - ས སྲ སླ གས བས བསྲ བསླ
  - ཧ ཧྲ ལྷ
  - ཨ

TSH does not include བགླ nor མདྲ in his list, but lists them as exceptions for valid syllables བགླ་ and མདྲོན་.

The wasurs are not included in this list, as it seems easier to consider them as exceptions.

### Constraints on suffix and second suffix

The second suffix ས can only appear after the following suffixes:

- ག
- ང
- བ
- མ

The second suffix ད (archaic) can only appear after the following suffixes:

- ན
- ར
- ལ

### Constraints on འ suffix

The འ suffix only appears in syllables with:

- one prefix
- no superscript
- no subscript
- no vowel

This rule is not documented explicitely in grammar books, but is yet to be challenged seriously.

Some mispelled words (like བརྡའ་) do not follow this rule, and the only counter-example found so far is བརྟའ (in GT). This rule does not apply to འི, འུ or འོ suffixes.
