CC ?= gcc
PKGCONFIG = $(shell which pkg-config)
CFLAGS = $(shell $(PKGCONFIG) --cflags gtk+-3.0)
LIBS = $(shell $(PKGCONFIG) --libs gtk+-3.0)

SRC = example-0.c

OBJS = $(SRC:.c=.o)

all: example0

%.o: %.c
	$(CC) -c -o $(@F) $(CFLAGS) $<

example0: $(OBJS)
	$(CC) -o $(@F) $(LIBS) $(OBJS)

clean:
	rm -f $(OBJS)
	rm -f example0
