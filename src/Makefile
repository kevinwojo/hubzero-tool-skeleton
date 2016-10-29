
# simple makefile for a Rappture-based program

CC            = gcc
CFLAGS        = -g -Wall

RAPPTURE_DIR  = $(shell . /etc/environ.sh; use -e -r rappture; echo $$RAPPTURE_PATH)
INCLUDES      = -I$(RAPPTURE_DIR)/include
LIBS          = -L$(RAPPTURE_DIR)/lib -lrappture -lm


all: mainc

mainc: main.c
	$(CC) $(CFLAGS) $(INCLUDES) $< -o $@ $(LIBS)

	install:
		install --mode 0755 -D mainc ../bin

		clean:
			$(RM) mainc run*.xml
