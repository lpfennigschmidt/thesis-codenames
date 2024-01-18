# Wordlists and Board Generation

Idea: boards are simple if words belonging to the same category are assigned to the same team, because the category name lends an obvious clue. And boards are difficult if the same words are assigned to different teams or the assassin, as the obvious clue cannot be used without penalty. So, I will extract categories, that are hopefully quite disjunct, extract hyponyms of these categories with wordnet or conceptnet and then later sample from these resulting lists. 

Requirements for words:
- All words should be nouns.
- All words should be single words, no compound words with spaces.
- Also, words should be known, so words with low frequency will be removed from the list.
- Word lists containing less than some threshold (25?) words should be removed.
- Words cannot contain the category word, otherwise the category word cannot be used as a hint. Also the category word should be one word, or have a synonym that is only one word.

TODO:

- [x] extracting useful categories from other papers/material (see folder `category lists/`)
- [x] extracting a wordlist for each category using wordnet, containing co-hyponyms for the hypernym `category`
- [x] comparing that for hyponyms extracted from ConceptNet
- [ ] comparing that to category norms dataset
- [ ] checking those words for word frequency (with SUBTLEX-US) 

## Category Lists
In here you can find lists of broad categories that could be used to generate a wordlist with exemplars of this category. The used lists are:

### Schröder et al.
[Schröder et al.](https://link.springer.com/article/10.3758/s13428-011-0164-y) ...

### Jaramillo et al.
[Jaramillo et al.](https://ojs.aaai.org/index.php/AIIDE/article/view/7435) constructed a Naive Bayes classifier that classifies words into one of the 118 collected categories (funnily, this bot was written to play the game Codenames, so it's not far from the domain). I found that some categories had duplicates within the list and a handful were closely related to the syntax of language which I found unfitting as semantic categories. I also excluded four more categories because I expect not to be able to generate good exemplars for them. This leaves me with 90 categories from the original 118. You can find the final 90 categories in `jaramillo et al cleaned.json` along with the excluded 28 categories, and the original 118 in `jaramillo et al.json`.

## Wordnet
- dataset use, citation

## ConceptNet
download, citation

## Category Norms
citation, download
