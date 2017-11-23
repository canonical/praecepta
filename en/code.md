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


**DO** seperate commands and output where appropriate. For example, instead of:

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
