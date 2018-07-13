# SimpleCLI
Quick modules I wrote to make a standalone CLI app

Inherit from Command class to make a command. 

The SimpleCLI parser onnly allows for single letter flags, but does allow groupings.
-abc is only valid if a,b and c are all separate flags, it won't work if -a is a flag and -bc is another.