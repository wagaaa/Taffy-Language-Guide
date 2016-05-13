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
        
    console.show.newline("Hello World!")
*Return:*

    $ taffy -r HelloWorld.tf
    Hello World!
    $
In this example, "show" output "Hello World!" in a newline. Script "newline" allows "show" to output these words in a newline.

*Another example:*

    @ Show time and timezone @
    console.show.newline(extra.system.time|extra.system.timezone)
*Return:*

    $ taffy -r time.tf
    22:24 Beijing
    $

show also allows to output another messages.In Taffy, notices/annotations need to included in tow @.

## action
The order is used to run command in shell or active a action.
*A Example:*

    console.show.action-shell(ls)
    
Return:

    $ taffy -r action1.tf
    ls:
    main.tf 1.c
    $

