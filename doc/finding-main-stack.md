## Finding main stack in standard Tibetan syllables

Finding the main syllable in standard Tibetan is essential and contains a few ambiguous cases. We suppose here that the syllable is correct standard Tibetan. These rules can be applied by an algorithm in this order.

### simple cases

- when there is a subscript or superscript letter, it is on the main stack
- when there is an explicit vowel on a consonant other than འ, it is on the main stack

### explicit vowel above འ, no other explicit vowel, subscript nor superscript

- when a vowel is above འ and འ is the first letter, འ is the main stack
- when a vowel is above འ and འ is not the first letter, the rules following this one must be applied to the syllable truncated before all འ with vowels at the end (ex: མའིའོ་ -> མ་)

### no explicit vowel, subscript nor superscript

- when the syllable contains one consonnant, this consonnant is the main stack
- when the syllable contains two consonnants, the first is the main stack
- when the syllable contains three consonnants and the final consonnant is not ས, the main stack is the second consonnant
- when the syllable contains three consonnants and the final consonnant is ས, and the first consonnant cannot be a prefix (only ག, ད, བ, མ, འ can be prefix) the main stack is the first consonnant
- when the syllable contains three consonnants and the final consonnant is ས, and the first consonnant can be a prefix, and the second consonnant is not ག, ང, བ nor མ, the main stack is the first consonnant
- when the syllable contains four consonnants, the main stack is the second consonnant

### ambiguous cases

When the syllable no explicit vowel, no superscript, no subscript, has three consonnants with a final ས, the first consonnant can be a prefix and the second consonnant is ག, ང, བ or མ, the case is ambiguous. There are 9 such cases in standard Tibetan:

- མངས་
- མགས་
- དབས་
- དངས་
- དགས་
- དམས་
- བགས་
- འབས་
- འགས་

Disambiguating is difficult because ས can be suffix, second suffix or grammatical suffix. Here are some clues (the main stack is noted by appending | to it, grammatical suffix ས is noted "+ས"):

- དབ|ས is archaic, but ད|བ+ས is common, so ད|བ+ས can be considered highly probable
- མང|ས doesn't exist, nor མ|ངས, but མང+ས is common and can be considered definitive
- མག|ས doesn't exist, nor མ|གས, but མག+ས is common and can be considered definitive
- བག|ས doesn't exist but བ|གས does, so བ|ག+ས or བ|གས can be considered definitive
- ད|གས is usually written དྭགས, and དག|ས exists so it can be considered highly probable
- neither ད|ངས nor དང|ས exist, but དང does, so ད|ང+ས can be considered definitive
- ད|མ+ས and དམ|ས exist but ད|མ+ས is more usual, so it can be considered reasonably probabile
- འབ|ས and འ|བས don't exist, but འབ|འ+ས (=འབས) does, so it can be considered definitive
- འག|ས exists, འ|གས doesn't, and འག|འ+ས (=འགས) does, so འག|འ+ས or འག|ས can be considered definitive
