# Atom linter systemverilog
## Intro
This is a atom-linter provider that turns vcs into a linter.

## Requirements
A makefile with a silent target ```linter```  (add ```.SILENT: linter``` to the makefile) that:
  1. Prints the directory in which vcs is run. This is necessary as the makefile can ```cd``` into another directory and this directory should be known. This should be the first output of ```make linter```. (For this reason, the target should be silent)
  2. Runs vcs, with ``` 2>&1 || true``` appended to the command so that errors are not considered as a failed linter run.
  3. Is located in the directory of the source (rtl) files, or any parent directory.

## TODO
* clean up unused template code
* support more errors and warnings
* support line-breaks in error messages. This might be something to fix at a higher level (atom-linter / atom).
