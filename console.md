# Taffy Syntax Guide - console

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
Returns:

    $ taffy -r HelloWorld.tf
    Hello World!
    $
In this example, script "show" output "Hello World!" in a newline. Script "newline" allows "show" to output these words in a newline.

*Another example:*

    console.show.newline(extra.system.time|extra.system.timezone)
Return:

    $ taffy time.tf
    22:24 Beijing
    $
show also allows to output another messages.