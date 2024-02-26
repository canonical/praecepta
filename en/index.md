# Canonical Documentation Style Guide

![Product logo](../media/logo.svg)

This is an as yet incomplete guide to the language and style conventions used
for Canonical documentation projects. Topics are listed in the navigation
to the left, and presented here as a single page to aid searching.


## Spelling

Canonical is a UK based company, and uses British English throughout. There
are many small differences between that and US English, but for the most 
part it comes down to spelling.

<!-- RULE
#01 Spelling suggestions for English words
-->
Some common differences are:

|    US English                     |            UK English               |
|-----------------------------------|-------------------------------------|
|license (verb) license (noun)      |  license (verb) licence (noun)      |
|defense (noun)                     |         defence (noun)              |
|sausages, beans, and mash          |      sausages, beans and mash       |
|program (TV, agenda) program (IT)  | programme (TV, agenda) program (IT) |
|percent                            |              per cent               |
|skeptical                          |   sceptical                         |
|catalog                            |   catalogue                         |
|   traveling                       |   travelling                        |
|   labeled                         |   labelled                          |
|   -able                           |  -eable                             |
|   -ize                            |  -ise                               |
|   -or                             |  -our                               |

In the most part this can be mitigated by simply enabling spell checking
on your editing software and choosing an **en-gb** dictionary. The minor 
differences in grammar will (hopefully) be picked up in review by the 
documentation team.

### Other common terms

<!-- RULE
#02 Spelling suggestions for common terms
-->

We would like to standardise on the following spellings for common 
technology terms: 

 - email
 - online
 - setup (noun), set up (verb)
 - backup (noun), back up (verb)
 - login (noun), log in (verb)
 - web
 - website
 - internet
 - systems management
 - virtualisation
 - space-separated, comma-delimited
 - load balancer (only upper case as part of proper name e.g. Elastic Load Balancer)

## Branding

Consistency in branding is important for a number of reasons, including the protection of trademarks where they apply. 
For our own products, and those of others we mention frequently, the following guidance applies.

### Ubuntu

When we refer to Ubuntu |oǒ'boǒntoō|, we are usually referring to the distribution, rather than the Ubuntu project itself. 

Our convention is to use the name, followed by the release number and, if applicable, 'LTS' to denote that the version
is in Long Term Support. Optionally, you may also further identify the release by its codename (the first or both parts
of the release name) if this is likely to be useful (e.g. some of our products also use the release names to identify
versions).

<!-- RULE
#03 Correct use of Ubuntu versions
-->
Some examples of correct usage:

- **Ubuntu 22.04 LTS**
- **Ubuntu 22.10**
- **Ubuntu 23.04 (Lunar Lobster)** _(note case!)_
- **Ubuntu 23.10 (Mantic)**

This also follows on to more specific products, e.g.

**Ubuntu Server 22.04 LTS**

In cases where the release may be mentioned many times in a single document, it is up to the author's judgement whether this
could be reworded or replaced by simply 'Ubuntu' on subsequent mentions. 

Note also that when referring to releases in the general sense, it is "_**an**_ Ubuntu release".

<!-- RULE
#04 Correct use of Canonical product names
-->

### Other Canonical products

| Product           |  Notes                        |
|-------------------|-------------------------------|
| Anbox Cloud       |                               |
| Charmed Kubeflow  |                               |
| COS               | Canonical Observability Stack |
| Juju              |                               |
| Launchpad         |                               |
| LXD               |                               |
| MAAS              | Metal As A Service            |
| MicroCeph         |                               |
| MicroCloud        |                               |
| MicroK8s          |                               |
| MicroOVN          |                               |
| MicroStack        |                               |
| Mir               |                               |
| Multipass         |                               |
| Snapcraft         |                               |
| snapd             |                               |
| Ubuntu Core       |                               |
| Ubuntu Pro        |                               |
| Ubuntu Server     |                               |

<!-- RULE
#05 Correct use of external product names
-->

### Other commonly referenced products/projects

| Product           | Notes                         |
|-------------------|-------------------------------|
| NVIDIA            |                               |
| OpenStack         |                               |
| PostgreSQL        |                               |
| Kubernetes        |                               |

## Contractions

Contractions are very common in spoken English and in many types of writing.
Avoiding the use of them entirely makes it difficult to achieve a friendly,
conversational tone. However, we should keep to contractions that are commonly
understood and not part of some regional dialect, and only use them in
"conversational" parts of the documentation (i.e. explanatory text).

### Contractions you can use

| contraction | meaning           | notes                         |
|-------------|-------------------|-------------------------------|
|aren't       |are not            |                               |
|can't        |cannot             |                               |
|could've     |could have         |                               |
|couldn't     |could not          |                               |
|didn't       |did not            |                               |
|doesn't      |does not           |                               |
|don't        |do not             |                               |
|hadn't       |had not            |                               |
|hasn't       |has not            |                               |
|haven't      |have not           |                               |
|it's         |it has / it is     |                               |
|isn't        |is not             |                               |
|mustn't      |must not           |                               |
|o'clock      |of the clock       |                               |
|wasn't       | was not           |                               |
|we'll 	      |we will            |                               |
|we're 	      |we are             |                               |
|we've 	      |we have            |                               |
|won't 	      |will not           |                               |
|would've     |would have         |                               |
|wouldn't     |would not          |                               |
|you'd        |you had /you would |                               |  
|you'll       |you shall /you will|                               |
|you're       |you are            |                               |
|you've       |you have           |                               |

<!-- RULE
#06 Forbidden contractions
-->
### Don't use these!

| contraction | meaning       | notes
|-------------|---------------|-----------------------------------|
| ain't       | is not        | colloquial - use isn't            |
|how'd 	      |how did / how would|                               |
|how'll       |	how will      |                                   |
| I'd         | I would       | We don't use first person!        |
|'twas 	      | it was        | only relevant in Christmas fables |
|something's  | something is  | avoid - confusion with possessive |
|mayn't       |may not        |                                   |
|may've       |may have       |                                   |
|mightn't     |might not      |                                   |
|might've     |might have     |                                   |
|gonna 	      |going to       |                                   |
|gotta 	      |got to         |                                   |

## Headings

Headings are important for navigation, for setting tone and for search indexing. Please bear
in mind the following:

<!-- RULE
#07 Use sentence case in headings
-->
### Sentence case 

All headings and headlines should be sentence case. This means that you
should only capitalise the first word unless it falls into one of the categories
outlined below:

 - product names 
 - personal names
 - company names
 - brands
 - places
 - Ubuntu Server, not Ubuntu server

**Use:** Do more with Ubuntu
**Don't use:** Do More With Ubuntu

If it is not the actual product name, it should not be capitalised. Never capitalise keywords, technical terms and jargon.

<!-- RULE
#08 Headings must not end in '.'
-->
<!-- RULE
#09 Headings should not contain links 
-->
<!-- RULE
#10 Headings should not contain code
-->
<!-- RULE
#11 Headings should not be followed by a subheading
-->
### Other considerations

 - Avoid overusing punctuation in headings. Headings should not end with a period/full point/full stop
 - Avoid links in headings
 - Avoid 'code' styling in headings - if it is really needed, it is preferred to at least sbegin the title by adding normal styled word
 - Imperatives should be used for 'How to...' style docs instead of gerunds (i.e. "Create an instance" rather than "Creating an instance")
 - Do not skip levels of heading hierarchy (e.g. following an h1/# with an h3/###)
 - Headings require content and should not be followed directly by a subheading


<!-- RULE
#12 Dates should follow '1 January 1970' format
-->
## Dates

For consistency, we will use the following date format:

 - Single day: 1 January 2013
 - Date range within same month: 1-2 January 2013
 - Date range across two or more months: 1 January - 2 February 2013

<!-- RULE
#13 Numbers below 10 should be spelled out
-->
<!-- RULE
#14 Numbers above 9 should be written in the '1,970' format
-->
## Numbers

Numbers in single figures should be spelled out in most cases. From
10 onwards, numbers should be written in digits.

Exceptions to this rule include numbered lists and units of measurement.

When writing out numbers over the 100s, remember to include commas.

**Use:** 7,000

**Don't use:** 7000

<!-- RULE
#15 Do not use $/# prompts in code blocks
-->
<!-- RULE
#16 Avoid inlining comments in code blocks
-->
<!-- RULE
#17 Avoid cade blocks more than 40 lines long
-->
<!-- RULE
#18 Separate input and output code blocks
-->
# Code examples in documentation

**DO NOT** use prompt marks (e.g. `$` or `#`) in code samples. These cause problems
for users who sometimes mistakenly type them in, or who want to copy and paste
sections of code. They also encourage poor explanation of the code. 

**DO NOT** use comments in normal bash code. E.g.:

```bash
juju deploy wordpress 
juju deploy ntp-master --to 2   #colocates with wordpress
juju add-relation mysql wordpress
```

This may be a useful comment if you just have a bash script to communicate
information, but we have words! It is clearer, more obvious and more helpful
to simply explain, before after or during the code.

**DO NOT** use long blocks of code. Anything which doesn't comfortably fit
on a screen is too long. Consider *why* you are showing it. Can it be broken
up into parts? Long sections of code are rarely read in documentation. If the
code is an example intended to be used rather than read, offer it as a 
download instead.


**DO** separate commands and output where appropriate. For example, instead of:

```bash
juju status
environment: gce3
machines:
  "0":
    agent-state: started
    agent-version: 1.24.2
    dns-name: 104.197.44.114
...
...
```

It is more informative to break between the command and the output
with explanation. This doesn't even have to be long. It breaks up the
code blocks somewhat and makes the whole document more legible and less
likely to cause unintended naps. For example

``` bash
To check what is going on, run:


      juju status

... which should return some formatted information giving the current
state of each unit and service:

       environment: gce3
       machines:
        "0":
          agent-state: started
          agent-version: 1.24.2
...
...
```

## Images

An image should not be overly cropped - allow for context. 

<!-- RULE
#19 No images linked to Google drive
-->
**DO NOT LINK IMAGES FROM A GOOGLE DRIVE** 
This will work, until such a time as whoever owns the image closes their account (or leaves Canonical).

<!-- RULE
#20 Cliché words and phrases to avoid
-->
## Words and phrases to avoid

Try to avoid jargon, long-winded phrases and words with negative
connotations. Steer clear of the following:

 - *Allow* - This suggests that we are in a position of power,
permitting users or customers to conduct certain activities.
 - *The ability to* – Use 'We can' instead of 'We have the ability to'
 - *Is able to* – Use 'Ubuntu can' instead of 'Ubuntu is able to'
 - *Not only...but also...*
 - *Eliminate*
 - *Execute*
 - *Terminate*
 - *Kill*
 - *Disruptive*
 - *Explosive*
 - *Leverage*
 - *Ecosystem*
 - *Going forward*
 - *In order to*
 - *Form factor*
 - *Use case*
 - *End user* – Use 'user' instead
 - *Linux for human beings*

It can be tempting to use flowery, official-sounding words
rather than plain English. Try to keep it simple.
<!-- RULE
#21 No double space after a period/full stop
-->
## FAQs
There are some grammatical issues that can cause confusion. Here are some of the main offenders.

### What is the difference between fewer and less?

Fewer means “not as many,” less means “not as much.”

A commonly-quoted example used to highlight the distinction is: “There are fewer cars on the road, which means there is less traffic.”

Also compare: “The fewer people know about this the better” and “The less people know about this the better”.

Note: The rule does not work if the number is counted as a quantity or as a unit. For example: “She paid less than ten pounds for it” or “His last jump was less than fifteen feet”.

### What is the difference between that and which?
This can, and has, caused many arguments, so it's probably best not to get too worried about it. A useful guide is: that defines, which informs.

This is not a cast-iron rule but it can help: “This is the house that Jack built, but I think the one next door, which Jack also built, is more attractive.”

“Which” is often clausal, so is predominantly preceded by a comma - compare “The police stopped the second car that was driven by a woman.” and “The police stopped the second car, which was driven by a woman.”

### Is it OK to split an infinitive?
There is no grammatical rule that says you can't split an infinitive. Sometimes, it is definitely better to split:

_"Can dot.com companies ever hope to fully recover their share values?"_

This sounds much better than moving “fully” in front of “to recover” or behind it. The key is not to write anything that is ambiguous or inelegant.

