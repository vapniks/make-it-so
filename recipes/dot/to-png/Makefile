# This is a template for the Makefile.
# Parameters should go in the upper half as:
#     width = 200
# and be referenced in the command as $(width)

# Press <f5> (mis-save-and-compile) to run this makefile (i.e. apply the transformation).
# Then in the corresponding dired buffer press one of:
# C-, (mis-finalize)  : finalize the transformation (delete makefile and other auxiliary files).
# C-M-. (mis-replace) : to clean up (delete auxiliary files and original file).
# C-M-, (mis-abort)   : revert back to state before `mis-action' was called.

# ______________________________________________________________________________

DIRDOT = $(shell dir *.dot)

DIRPNG = $(DIRDOT:.dot=.png)

all: clean Makefile $(DIRPNG)

%.png: %.dot
	dot -Tpng "$^" > "$@"
	echo $@ >> provide

clean:
	rm -f *.png provide

# Insert the install command here.
# e.g. sudo apt-get install ffmpeg
install-tools:
	sudo apt-get install graphviz

# Use this target when one file requires another.
# See "../../cue/split/Makefile" for an example.
require:
	@echo

.PHONY: all install-tools require clean
