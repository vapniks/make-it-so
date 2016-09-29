# This is a template for the Makefile.
# Parameters should go in the upper half as:
#     width = 200
# and be referenced in the command as $(width)

# ______________________________________________________________________________

DIRDOT = $(shell dir *.dot)

DIROUT.DOT = $(DIRDOT:.dot=.out.dot)

all: clean Makefile $(DIROUT.DOT)

%.out.dot: %.dot
	echo "add command here"
	echo $@ >> provide

clean:
	rm -f *.out.dot provide

# Insert the install command here.
# e.g. sudo apt-get install ffmpeg
install-tools:
	echo "No tools required"

# Use this target when one file requires another.
# See "../../cue/split/Makefile" for an example.
require:
	@echo

.PHONY: all install-tools require clean