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

Disambiguating is difficult because ས can be suffix, second suffix or grammatical suffix. Here are some clues with the following notation: 

- the main stack is noted by appending "|" to it
- grammatical suffix ས is noted "+ས"
- a non-existing word is prefixed by "*"

Here are the different forms:

- *ད|བས, *དྭབས, དབ|ས (archaic), དབའ+ས -> དབ|ས can be considered definitive
- *མང|ས, མ|ངས, མངའ+ས -> མ|ངས can be considered reasonably probable
- *མག|ས, *མ|གས, *མགའ+ས -> impossible to determine, but མ|གས is more intuitive
- *བག|ས, *བགའ+ས, བ|གས -> བ|གས can be considered definitive
- *ད|གས, དྭགས, དག|ས, དགའ+ས -> དག|ས can be considered definitive
- *ད|ངས, *དང|ས, དྭངས, *དངའ+ས -> དང|ས due to the possibility of དྭངས
- *དྭངས, *ད|མས, དམ|ས, དམའ+ས -> དམ|ས can be considered definitive
- *འབ|ས, *འ|བས, འབ|འ+ས -> འབ|ས can be considered definitive
- *འ|གས, འག|ས, འག|འ+ས ->འག|ས can be considered definitive
