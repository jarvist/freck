# Freck

Obsolete English word. 
Verb intr. *"To move swiftly or nimbly"* 
<sup>[1](#ref1)</sup>

A bare-bones Bash script to help archive and organise scientific computation,
as you go along, from the command line.

A work flow software, designed in the minimalist Unix philosophy.

## What does it do?

Very little. It demands an input name, then archives the files in the present working directory in a set of folders sequentially named '0001-InputName' '0002-InputName2' etc. It saves as much info as possible (username, hostname, date/time) into a 'breadcrumb' file within this directory. You then copy those files you need for the next calculation back into the present directory, then continue working.

The intent is to avoid impossible directory structures that look like: ` NewProject/Optimisation/WhoopsRestart/TighterConverged/ `.

## What will it do in the future?

* I'd really like it to save history of the shell. This makes things a lot more specific, and as it is a sub shell, might be easier by assuming / integrating `tmux`. 
* I might add an (optional) assumption that it should check the breadcrumb file into git, if it detects it is in a git work tree.

## What won't it do?

* Feed into an SQL database <shudder>.

<a name="ref1">1</a>: http://matadornetwork.com/abroad/20-obsolete-english-words-that-should-make-a-comeback/
