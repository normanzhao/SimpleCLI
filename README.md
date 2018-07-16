# SimpleCLI
Quick modules I wrote to make a standalone CLI app

To use:

The parser is located in the SimpleCLI module and will continually accept input. The default commands are:

help-shows every command, their descriptions, and their usage

exit-exits the bug tracker


Commands are in the form of [COMMAND] [OPTIONS] [ARGUMENT], commands can only be a single word. Options/flags can also only be one letter. For more details, but can allow groupings. The argument can be hacked to accept multiple arguments like I did for some commands for the [SimpleBugTracker](https://github.com/normanzhao/SimpleBugTracker).


All command inherit from the base class Command with certain attributes that can be overridden: name, aliases, options, usage and run.

Name is the name of the command and what every alias will associate with.

Aliases are other names that can be used. They are bound in a key->value pair where the key is the alias and the value is the associated name.

Options are flags that can be used in conjunction with the command. The SimpleCLI parser only allows for single letter flags, but does allow groupings.
-abc is only valid if a,b and c are all separate flags, it won't work if -a is a flag and -bc is another.

Usage is the litte blurb that tells you how to use a command.

Run is the function associated with that command.


The description for any given command is the docstring of the function assigned to the command.

See [SimpleBugTracker](https://github.com/normanzhao/SimpleBugTracker) for a quick and dirty demo on how to use this.
