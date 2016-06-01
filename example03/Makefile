CC ?= gcc
PKGCONFIG = $(shell which pkg-config)
CFLAGS = $(shell $(PKGCONFIG) --cflags gtk+-3.0)
LIBS = $(shell $(PKGCONFIG) --libs gtk+-3.0)

SRC = example-3.c

OBJS = $(SRC:.c=.o)

all: example3

%.o: %.c
	$(CC) $(CFLAGS) -c -o $(@F)  $<

example3: $(OBJS)
	$(CC) $(LIBS) -o $(@F) $(OBJS)

clean:
	rm -f $(OBJS)
	rm -f example3
