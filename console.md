# Taffy Syntax Guide - console

---

Generally, Taffy allows you to run these scripts:

* show
* action
* keyin
* tool
* file
* set

And more.

## show

This script allows to output sth. on the screen.For example:

```
console.show.newline("Hello World!")
```

_Return:_

```
$ taffy -r HelloWorld.tf
Hello World!
$
```

In this example, "show" output "Hello World!" in a newline. Script "newline" allows "show" to output these words in a newline.

_Another example:_

```
@ Show time and timezone @
console.show.newline(extra.system.time|extra.system.timezone)
```

_Return:_

```
$ taffy -r time.tf
22:24 Beijing
$
```

show also allows to output another messages.In Taffy, notices\/annotations need to included in tow @.

> ## Steal a little lazy
> 
> If you don't want to type \_console, \_you can add this in the head of the source:
> 
> `# EXEC IN CONSOLE`
> 
> So the code looks like this:
> 
> `# EXEC IN CONSOLEshow.newline("No CONSOLE! ")`
> 
> If you want use a famwork in the program, you can still type it.
> 
> `# EXEC IN CONSOLEshow.newline("Taffy")gui.newd>(main.tfw)`

## action

The order is used to run command in shell or active a action.
_A Example:_

```
console.show.action-shell(ls)
```

Return:

```
$ taffy -r action1.tf
ls:
main.tf 1.c
$
```

If you want to hide "ls", try:

```
console.show.action-shell:h(ls)
```

Result:

```
$ taffy -r action-2-hide.tf
main.tf 1.c
$
```

