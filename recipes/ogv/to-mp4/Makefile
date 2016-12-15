# This is a template for the Makefile.
# Parameters should go in the upper half as:
#     width = 200
# and be referenced in the command as $(width)

# ______________________________________________________________________________

DIROGV = $(shell dir *.ogv)

DIRMP4 = $(DIROGV:.ogv=.mp4)

all: clean Makefile $(DIRMP4)

%.mp4: %.ogv
	avconv -i $^ $@
	echo $@ >> provide

clean:
	rm -f *.mp4 provide

# Insert the install command here.
# e.g. sudo apt-get install ffmpeg
install-tools:
	sudo apt-get install avconv

# Use this target when one file requires another.
# See "../../cue/split/Makefile" for an example.
require:
	@echo

.PHONY: all install-tools require clean
