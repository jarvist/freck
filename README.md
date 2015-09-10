# Freck

Obsolete English word. 
Verb intr. *"To move swiftly or nimbly"* 
<sup>[1](#ref1)</sup>

A bare-bones Bash script to help archive and organise scientific computation,
as you go along, from the command line.

A work flow software, designed in the minimalist Unix philosophy.

## What does it do?

Very little. 
Every time you run it, it demands a name, and then archives the present working directory files in sequential folders that look like '0001-InputName' '0002-InputName2'. 
It records as much info as possible (username, hostname, date/time) into a 'breadcrumb' file within this directory.
If it appears to be within a git repo (i.e. ` git init `), it will check in this breadcrumb to the repo with an automatic commit message.

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

* I'd really like it to save history of the shell. This makes things a lot more specific, and as it is a sub shell, might be easier by assuming / integrating `tmux`. 

## What won't it do?

* Feed into an SQL database <shudder>.

<a name="ref1">1</a>: http://matadornetwork.com/abroad/20-obsolete-english-words-that-should-make-a-comeback/
