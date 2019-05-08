# Canonical Documentation Style Guide

![Product logo](../media/logo.svg)

This is an as yet incomplete guide to the language and style conventions used
for Canonical documentation projects. Topics are listed in the navigation
to the left, and presented here as a single page to aid searching.


# Spelling

Canonical is a UK based company, and uses British English throughout. There
are many small differences between that and US English, but for the most 
part it comes down to spelling.

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

## Other common terms

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

# Contractions

Contractions are very common in spoken English and in many types of writing.
Avoiding the use of them entirely makes it difficult to achieve a friendly,
conversational tone. However, we should keep to contractions that are commonly
understood and not part of some regional dialect, and only use them in
"conversational" parts of the documentation (i.e. explanatory text).

## Contractions you can use

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


## Don't use these!

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

# Headings and capitalisation

All headings and headlines should be sentence case. This means that you
should only capitalise the first word.

**Use:** Ubuntu reaches new heights
**Don't use:** Ubuntu Reaches New Heights

You should only capitalise:

 - product names 
 - personal names
 - company names
 - brands
 - places
 - Ubuntu Server, not Ubuntu server

If it is not the actual product name, it should not be capitalised. Never capitalise keywords, technical terms and jargon.

# Dates

For consistency, we will use the following date format:

 - Single day: 1 January 2013
 - Date range within same month: 1-2 January 2013
 - Date range across two or more months: 1 January - 2 February 2013

# Numbers

Numbers in single figures should be spelled out in most cases. From
10 onwards, numbers should be written in digits.

Exceptions to this rule include numbered lists and units of measurement.

When writing out numbers over the 100s, remember to include commas.

**Use:** 7,000

**Don't use:** 7000

# Code examples in documentation

This details how to present code samples in documentation, and how to 
work around some of the limitations there are in static media when
trying to show an interactive behaviour.

In general *ALL* code samples should be marked as code via whatever
markup system is in use. In the case of most output, this will normally
result in the code:

 - being slightly indented
 - being highlighted in some way
 - appearing in a monospace font

There are some types of final output which cannot easily reproduce all these
elements, but in such cases the best approximation will be made. 

## Markdown styles

Most of our documentation is generated from Markdown sources. There are 
two relevant conventions to follow:

### Code blocks

A code block is enclosed by three backticks and includes the type of code:


      ```bash
      maas command do something
      maas command do something else
      ```

The most common types used are: `bash`, `yaml`, `json`, and `no-highlight`. 
The last is like a miscellaneous type. It is often used to display
command output.

### Inline code

Use a backtick to `inline filenames and other literals` like this:

      Use a backtick to `inline filenames and other literals` like this:


## General notes

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

# Hyperlinks

Links to internal files or external URLs use the following format:

```no-highlight
[visible text][label]
```

The `visible text` is what will appear on the web page. The `label` is used to
refer to the destination, which is placed at the bottom of the file:

```
<!-- LINKS -->

[label]: destination
```

For example:

```no-highlight
- For more on this topic see [DHCP][dhcp].
- To understand haproxy, see the [upstream configuration manual][upstream-haproxy-manual].

...

[dhcp]: installconfig-networking-dhcp.md
[upstream-haproxy-manual]: http://cbonte.github.io/haproxy-dconv/1.6/configuration.html
```

The visible text should use an active style as opposed to a passive style. For
instance, try to avoid:

```no-highlight
A [proxy][maas-proxy] can optionally be configured.
```

Notes:

- An internal page is referred to by its source filename (i.e. `.md` not
  `.html`).
- Try to use the same `label:destination` pair throughout the documentation.


# Images

An image should not be overly cropped - allow for context. 

In terms of linking, they are managed very similarly to hyperlinks. However,
they are placed on their own line; are preceded by an exclamation point; and
both the label and destination have a specific naming convention:

```no-highlight
![alt attribute][img_filename]
```

The bottom of the file will look like:

```no-highlight
[img_filename]: ./path/to/image.png
```


# Words and phrases to avoid

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




