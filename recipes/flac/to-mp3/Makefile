# ——— parameters ———————————————————————————————————————————————————————————————
bitrate = 320k
frequency = 48000
channels = 2

# ——— implementation ———————————————————————————————————————————————————————————
DIRFLAC = $(shell dir *.flac)
DIRMP3 = $(DIRFLAC:.flac=.mp3)

all: clean Makefile $(DIRMP3)

%.mp3: %.flac
	ffmpeg -i "$<" -ab $(bitrate) -ac $(channels) -ar $(frequency) "$@"
	echo "$@" >> provide

clean:
	rm -f *.mp3 provide

install-tools:
	sudo apt-get install ffmpeg

require:
	@echo

.PHONY: all install-tools require clean
