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
| Landscape         |                               |
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
 - Avoid 'code' styling in headings - if it is really needed, it is preferred to at least begin the title by adding a normal styled word
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

## Interacting with UI elements

### Screenshots

Screenshots should be used sparingly.

A screenshot is not a replacement for clear descriptions in documentation. If an image is well described,
a screenshot shouldn’t be necessary in many situations, and including many screenshots can clutter the
documentation.

<!-- Rule#22
Images must have Alt text
-->
Screenshots also can’t be translated, so they aren’t as accessible to non-native English users or those using translated documentation. Additionally, those using screen-readers won’t be able to access the screenshots without alt-text.

### Using UI elements as the English words

<!-- Rule
#23 Don’t use UI elements as though they are English words
-->

Don’t use UI elements as though they are English words.

For example:

- **Use**: When you’re finished, click **Save** to save your settings.
- **Don’t use**: When you’re finished, **Save** your settings.

Using the UI text as English words is less clear and may not transfer well to certain translated versions.

### Click vs. Tap vs. Select

 - Use “Click” for buttons that you click on (or “Tap” if the product is primarily for mobile devices)
- Use “Select” for selecting from multiple options (e.g., a dropdown menu, multiple menu items, etc.)
- Use “Select” when there are multiple instructions separated by > (e.g., Select Preferences > Languages)

For example:

- **Use**: Click **Settings** to open your user settings.
- **Use**: Select the machines you want to register, then click **Save**.
- **Use**: Tap the application to open it.
- **Don’t use**: Select **Add bookmark** to save your bookmark.

“Click”/”Tap” is preferred over “Select” for UI elements that are definitive. This is because “Select” has an
open-ended connotation, while “Click”/”Tap” is direct and definitive. Although “Click”/”Tap” may
technically be wrong in certain situations (e.g., if a user is using the mobile version of a web page on
their desktop computer), it’s important to consider accessibility and the primary audience of the documentation
over these edge cases. Differentiating when users may have to *select* from
options or *select* more than one option can be useful for them, especially when following a longer
how-to guide (e.g., Click **X**, Click **Y**, Click **Z**, Select the settings you want to apply,
Click **Save**). This extra level of precision can also be helpful for non-native English users and
those using translated documentation.

### Bold vs. Italics

Use bold for UI elements the user clicks/selects, and quotes or quotes with italics when drawing attention to a
specific word or phrase, or using the name of a word as a word.

For example:

- **Use**: Click **Save**
- **Use**: In the Computers column, click **Register a new computer**.
- **Use**: Click the link in the text *“You can register new computers by following these instructions”*.
- **Use**: Use the word “and” instead of “or”*.*
- **Use**: Use the word *“and”* instead of *“or”*.
- **Don’t use**: Once you’ve made your selections, click *Save*.

Bolding UI elements can help make the documentation easier to scan for critical information. This is especially good for users who aren’t reading the documentation for the first time and just want key information without having to sift through extraneous documentation.

### Angled brackets

You can use a right angled bracket > for navigating menu items with multiple steps.

For example:

- **Use**: Select **Preferences > Languages > English**
- **Use**: You can navigate to **File** > **Documents** and select one of your saved documents.
- **Use**: Select **Blank Document** from the **File >** **New** menu.
- **Don’t use**: Navigate to the home page > Click **Packages** > Select each package you want to export > Click **Export**

Using the right angled bracket (**>**) is at the author’s discretion; however, you’re encouraged to use this format where possible to keep things concise.

### Checkboxes

Use “Select” and ”Clear” or “Check” and ”Uncheck” together at the author’s discretion, depending on what is most natural in context.

For example:

- **Use**: Select the **Enable firewall** checkbox.
- **Use**: Clear the **Add bookmark** checkbox.
- **Use**: “Check the computer(s) you want to register” with “Uncheck any computer(s) you don’t want registered”
- **Don’t use**: Check the computer(s) you want to register, or clear any computer(s) you don’t want registered

This helps establish consistency in how we refer to checkboxes in the UI.

### Keyboard shortcuts and keyboard keys

Use “Press” when instructing the user to use a specific keyboard shortcut or keyboard key, and “Use” when instructing them to use collective or ambiguous keys.

<!-- Rule
#24 Don’t use "Click the 'Enter' Key" or derivations
-->


For example:

- **Use**: Press `Ctrl + C`
- **Use**: “To save, press `Enter`.” or “To save, press the `Enter` key”.
- **Use**: Use the arrow keys to navigate the menu.
- **Don’t use**: Click the `Enter` key.

This ensures they don’t get confused with our use of “Click”/”Tap”/”Select”.

### “Icon” vs. “Button”

“Icon” is for a symbol/image that represents an object or function, and “button” is for UI elements that initiate action when clicked. Icons typically don’t include explanatory text, and are sometimes buttons or included on a button.

If using the image of an icon or button, write the name of the icon/button directly after it or add alt-text. Avoid using the terms “icon” or “button” unless they’re needed for clarity.

For example:

- A search icon (also may be a button): ![search icon](https://assets.ubuntu.com/v1/46244ff9-magnifying_glass.png)

- A save button: ![save button](https://assets.ubuntu.com/v1/46eccbaa-Screenshot%20from%202024-02-14%2012-25-36.png)

- A reply button with an icon: ![reply button](https://assets.ubuntu.com/v1/1370f4e1-reply_button.png)

- **Use**: Click ![menu](https://assets.ubuntu.com/v1/9526cf28-menu_icon.svg) for more options. (Alt-text: “the menu”)

- **Use**: Click the ![star](https://assets.ubuntu.com/v1/821178e7-icon-orange-resources.png) star to add the page to your favorites.

- **Don’t use:** Click the ![pencil](https://assets.ubuntu.com/v1/633aab2b-pencil.png) pencil icon to edit the post.

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
