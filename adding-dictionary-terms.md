# Adding dictionary terms

The first thing to look at when thinking about adding a term to the dictionary, is to consider what that word is and where it should go.

* Product names should not be added to the dictionary, they should be added to the vocabulary list in this repository.
* Command references and project-specific terms that are not used widely outside of a given context, should be added to a project's local custom wordlist.
* Words that are currently flagged by the spelling check, but exist in a dictionary (or are accepted modern terminology) should be added to the dictionary in this repository.

Let's consider adding the term `rebasing` to the dictionary. Where do we start?

## Dictionary overview

Vale relies on Hunspell dictionaries for spelling functionality. Hunspell dictionaries consist of two files, a `.dic` file containing a list of words, and a `.aff` file which essentially contains structures of prefixes and suffixes.

A word defined in the `en_US.dic` file can be appended with a structure to indicate accepted variants as declared in the `en_US.aff` file.

Knowing that the system uses core words and affixes, the term `rebase` can be split into `re` and `base`.

## Affix file

The `en_US.aff` file contains some structures that define how a prefix or suffix functions for given words. If we look for the affix we need, `re`, we find that in this block:

```
PFX A Y 1
PFX A   0     re         .
```

We need to break down exactly what this block means. First, consider the
structure as a table:

| PFX | A | Y | 1 |    |     |
|-----|---|---|---|----|-----|
| PFX | A |   | 0 | re |  .  |

Each block has a header row, and then content rows following it. In this case there is a header row, and a single content row. The header row always contains four columns, and the first two columns are shared for the entry. The content row contains six columns, with an empty column in the third position.

The first column indicates if this indicates a prefix (`PFX`) or suffix (`SFX`). In this case, it is a prefix.

The second column indicates the letter used to represent this structure in the dictionary file. In this case, it is the letter `A`.

The third column, with content only in the header row, is the combinable flag which indicates if this structure can be used in conjunction with other structures, or if it is dealt with separately. In this case, this prefix can be used in conjunction with other structures - meaning that this prefix can be used with suffixes that also have a `Y` in this column.

The title row's fourth column indicates the number of entries in the table, in this case a single entry.

The content row's fourth column indicates if a letter is replaced by the affix and what that letter is. In this case, no letter is replaced.

The content row's fifth column indicates the letters used by the affix. In this case, the leters `re` are used.

The content row's sixth column provides a regex structure of letters used to understand if this row applies to a given word. In this case, as a single content row is used, it applies to all words.

So, in this example, the prefix `re` is defined and provided by the letter `A` when used in the dictionary file.

## Dictionary file

Each line in the dictionary provides a different word base, which may also define affixes that may be used with that word using a forward slash `/`.

So we want to add `base/A` to indicate base can be used with the prefix `re`.

However, `base` is already defined in the dictionary file:

```
base/CDRSLTG
```

We could just add `A`, to make `base/ACDRSLTG`, but that might make for some strange terms. Remember that `re` can be combined with other affixes, if it wasn't able to be combined we could just add the affix letter and leave it here.

## Understanding existing terms

Looking at how `base` is currently defined, we need to understand the terms currently provided by this structure, and what a modification would do.

```
base/CDRSLTG
```

Looking at the affix file, the letter C can be found by looking for `FX C` (as all affixes are provided in this pattern, prefix or suffix). So, looking at `C`:

```
PFX C Y 1
PFX C   0     de          .
```

This shows `C` provides the prefix `de` which, despite being having a positive combination flag, cannot be used in conjunction with another prefix. So, `C` does not cause issues with the `A` affix we want to add.

Looking at `D`:

```
SFX D Y 4
SFX D   0     d          e
SFX D   y     ied        [^aeiou]y
SFX D   0     ed         [^ey]
SFX D   0     ed         [aeiou]y
```

This shows that `D` provides the suffix `d`, `ied`, and `ed` in different contexts. The last column defines a regex structure that dictates which suffix applies to which words. In our case, with `base` the last letter is `e` which means the suffix that applies in this case is `d`.

It is worth noting that, if our word ended with `[^aeiou]y`, the `y` at the end of our word would be removed before `ied` was added. This is indicated by the fourth column containing `y`.

This suffix is combinable, so if we consider adding `A`, then the word `rebased` would be added to the dictionary. This is a term we also want to accept.

Looking at `R`:

```
SFX R Y 4
SFX R   0     r          e
SFX R   y     ier        [^aeiou]y
SFX R   0     er         [aeiou]y
SFX R   0     er         [^ey]
```

This shows that `R` provides the suffix `r`, `ier`, or `er` in different contexts. The last column defines a regex structure that dictates which suffix applies to which words. In our case, with `base` the last letter is `e` which means the suffix that applies in this case is `r`.

This suffix is combinable, so if we consider adding `A`, then the word `rebaser` would be added to the dictionary.

This word lies in a grey area, where it *could* be a word we want added to the dictionary, but it would be limited use, and a small edge case. We are adding an action, do we need to refer to the party that does the action in this way? Because of the grey area, this should be raised with the Technical Author team, but for now we will decide that this shouldn't be added to the dictionary.

This means we can't just add `A` to the existing affixes on `base`.

A short summary of the additional affixes:

* `S` provides `-s`, and is combinable, giving `rebases`. This would not be blocking.
* `L` provides `-ment`, and is combinable, giving `rebasement`. This would be blocking.
* `T` provides `-st`, and is not combinable. This would not be blocking.
* `G` provides `-ing`, replaces `e` at the end of a word, and is combinable, giving `rebasing`. This is not blocking.

## Adding a new term

If we cannot just add to the existing `base`, what's the best way to add this new word?

We could add `base/A`, or we could add `rebase`. Both options are acceptable. For our purposes, `rebase` is the core word, so it's better for us to add `rebase` with some relevant affixes.

So, considering the existing forms of `base`, what are the affixes we should use with `rebase`?

We can drop any prefixes, like `C`, otherwise we would get `derebasing`.

We can drop any blocking affixes from the above analysis, like `R` and `L`, which would give us `rebaser` and `rebasement`.

We can drop any non-blocking affixes that weren't combinable but don't make sense, like `T`, which would give us `rebasest`.

We are then left with `D`, `S`, `G`, so we will add `rebase/DSG` to the dictionary in the approrpriate line in alphabetical order.
