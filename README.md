# Freck

Obsolete English word. 
Verb intr. *"To move swiftly or nimbly"* 
<sup>[1](#ref1)</sup>

A bare-bones Bash script to help archive and organise scientific computation,
as you go along, from the command line.

A work flow software, designed in the minimalist Unix philosophy.

The intent is for it to help organise your project files and build a git repo as you go along for future reference and sharing. For a more sophisticant set of tools, you may be interested in http://www.aiida.net/ .

## What does it do?

Very little. 
Every time you run it, it demands a name, and then archives the present working directory files in sequential folders that look like '0001-InputName' '0002-InputName2'. 
It records as much info as possible (username, hostname, date/time) into a 'breadcrumb' file within this directory.
If it appears to be within a git repo (`git init` is all you need to create one), it will check in this breadcrumb to the repo with an automatic commit message.

You then copy those files you need for the next calculation back into the present directory, then continue working.

The intent is to avoid impossible directory structures that look like: ` NewProject/Optimisation/WhoopsRestard/TighterCoverged/ `

Instead you should see:
```
0001-InitialGeom
0002-DFT_opt
0003-Tight_DFT_opt
0004-PhononCalc
````

## What will it do in the future?

* I'd really like it to save history of the shell. This makes things a lot more specific to software versions / software. It seems difficult to get at this information in a general way, as 'freck' runs in a subshell. This might be easiest to do by assuming / requiring `tmux` or similar.
* Useful ideas here: https://news.ycombinator.com/item?id=10162189

## What won't it do?

* Feed into an SQL database (shudder)

<a name="ref1">1</a>: http://matadornetwork.com/abroad/20-obsolete-english-words-that-should-make-a-comeback/
