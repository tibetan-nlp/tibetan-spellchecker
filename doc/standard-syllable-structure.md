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

### Prefixes

A prefix can be:

- ག
- ད
- བ
- མ
- འ

### Main stack

#### superscript letter

A subscript letter is written above the main letter. For example རྒ decomposes in subscript ར above main letter ག.

Subscript letters are (combination with main letter ཀ in parenthesis)

- ར (རྐ)
- ལ (ལྐ)
- ས (སྐ)

#### main letter

The main letter can be any of the standard tibetan consonants (ཀ, ཁ, ག, ང, ཅ, ཆ, ཇ, ཉ, ཏ, ཐ, ད, ན, པ, ཕ, བ, མ, ཙ, ཚ, ཛ, ཝ, ཞ, ཟ, འ, ཡ, ར, ལ, ཤ, ས, ཧ, ཨ).

### subscript letter

Subscript letters are written below the main letter. They are (combination with main letter ཀ in parenthesis):

- ཡ (ཀྱ)
- ར (ཀྲ)
- ལ (ཀླ)
- ཝ (ཀྭ)

### second subscript letter

The second subscript letter appears under the first subscript, it cannot appear without a first subscript. It can only be ཝ.

### Explicit vowels

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
- ར
- ལ
- ས

## Second suffix

The second suffix ས can appear only after a suffix.

## Grammatical suffixes

The following grammatical suffixes can appear if the syllable have no suffix or suffix འུ :

- འི
- འོ
- འིའོ
- ར
- ས
- འང
- འམ

When a syllable has suffix འ and no second suffix, it can take the following grammatical suffixes (here including suffix འ):

- འི
- འིའོ
- འོ
- འང
- འམ

## Constraints

For a Tibetan syllable to be valid, it must respect a few constraints:

### Constraints on superscript and subscript letters

The only valid combinations of superscript + main + subscript + second subscript letters are:

- the main letters without superscript nor subscript nor second subscript letters
- the following stacks:
  - རྐ རྒ རྔ རྗ རྙ རྟ རྡ རྣ རྦ རྨ རྩ རྫ
  - ལྐ ལྒ ལྔ ལྕ ལྗ ལྟ ལྡ ལྤ ལྦ ལྷ
  - སྐ སྒ སྔ སྙ སྟ སྡ སྣ སྤ སྦ སྨ སྩ
  - ཀྭ ཁྭ གྭ ཅྭ ཉྭ ཏྭ དྭ ཙྭ ཚྭ ཞྭ ཟྭ རྭ ལྭ ཤྭ སྭ ཧྭ
  - ཀྱ ཁྱ གྱ པྱ ཕྱ བྱ མྱ
  - ཀྲ ཁྲ གྲ ཏྲ ཐྲ དྲ པྲ ཕྲ བྲ མྲ ཤྲ སྲ ཧྲ
  - ཀླ གླ བླ ཟླ རླ སླ
  - རྐྱ རྒྱ རྨྱ
  - སྐྱ སྒྱ སྤྱ སྦྱ སྨྱ
  - སྐྲ སྒྲ སྣྲ སྤྲ སྦྲ སྨྲ
  - གྲྭ དྲྭ ཕྱྭ རྒྭ རྩྭ

These are the same as [the famous list](http://www.thlib.org/reference/transliteration/tibstacks.php), adding ལྭ (from Nicolas Tournadre, Manuel de Tibétain Standard).

### Constraints on prefix and superscript letter

The only valid combinations of prefix + superscript letter + main letter + subscript + second subscript are (in alphabetical order): 

  - ཀ ཀྭ ཀྱ ཀྲ ཀླ དཀ དཀྭ དཀྱ དཀྲ དཀླ བཀ བཀྭ བཀྱ བཀྲ བཀླ རྐ རྐྱ ལྐ སྐ སྐྱ སྐྲ བརྐ བརྐྱ བསྐ བསྐྱ བསྐྲ
  - ཁ ཁྭ ཁྱ ཁྲ མཁ མཁྭ མཁྱ མཁྲ འཁ འཁྭ འཁྱ འཁྲ
  - ག གྭ གྱ གྲ གྲྭ གླ དག དགྭ དགྱ དགྲ དགྲྭ བག བགྭ བགྱ བགྲ བགྲྭ བགླ མག མགྭ མགྱ མགྲ མགྲྭ འག འགྭ འགྱ འགྲ འགྲྭ རྒ རྒྱ ལྒ སྒ སྒྱ སྒྲ བརྒ བརྒྱ བསྒ བསྒྱ བསྒྲ
  - ང དང མང རྔ ལྔ སྔ བརྔ བསྔ
  - ཅ ཅྭ གཅ གཅྭ བཅ བཅྭ
  - ཆ མཆ འཆ
  - ཇ མཇ འཇ རྗ ལྗ བརྗ
  - ཉ ཉྭ གཉ གཉྭ མཉ མཉྭ རྙ སྙ བརྙ བསྙ
  - ཏ ཏྭ ཏྲ གཏ གཏྭ གཏྲ བཏ བཏྭ བཏྲ རྟ ལྟ སྟ བརྟ བལྟ བསྟ
  - ཐ ཐྲ མཐ འཐ
  - ད དྭ དྲ དྲྭ གད གདྭ བད བདྭ མད མདྭ འད འདྭ འདྲ འདྲྭ རྡ ལྡ སྡ བརྡ བལྡ བསྡ
  - ན གན མན རྣ སྣ སྣྲ བརྣ བསྣ
  - པ པྱ པྲ དཔ དཔྱ དཔྲ ལྤ སྤ སྤྱ སྤྲ
  - ཕ ཕྱ ཕྱྭ ཕྲ འཕ འཕྱ འཕྱྭ འཕྲ
  - བ བྱ བྲ བླ དབ དབྱ དབྲ འབ འབྱ འབྲ རྦ ལྦ སྦ སྦྱ སྦྲ
  - མ མྱ མྲ དམ དམྱ དམྲ རྨ རྨྱ སྨ སྨྱ སྨྲ
  - ཙ ཙྭ གཙ གཙྭ བཙ བཙྭ རྩ རྩྭ སྩ བརྩ བརྩྭ བསྩ
  - ཚ ཚྭ མཚ མཚྭ འཚ འཚྭ
  - ཛ མཛ འཛ རྫ བརྫ
  - ཝ
  - ཞ ཞྭ གཞ གཞྭ བཞ བཞྭ
  - ཟ ཟྭ ཟླ གཟ བཟ བཟྭ བཟླ
  - འ
  - གཡ
  - ར རྭ རླ བརླ
  - ལ
  - ཤ ཤྭ གཤ གཤྭ བཤ བཤྭ
  - ས སྭ སྲ སླ གས གསྭ བས བསྭ བསྲ བསླ
  - ཧ ཧྭ ཧྲ ལྷ
  - ཨ

### Constraints on suffix and second suffix

The second suffix ས can only appear after the following suffixes:

- ག
- ང
- བ
- མ

### Simplification of contraints on suffixes

Mixing suffix, second suffix and grammatical suffix, the following can appear after the main stack:

- ག
- ང
- ད
- ན
- བ
- མ
- འ
- འུ
- འེ
- ར
- ལ
- ས
- གས
- ངས
- བས
- མས
- འི
- འིའོ
- འོ
- འང
- འམ
- འུའི
- འུའིའོ
- འུའོ
- འུའང
- འུའམ
