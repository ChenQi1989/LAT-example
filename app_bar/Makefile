CC ?= gcc
CFLAGS ?= -Wall

bar: bar.c
	$(CC) $(CFLAGS) -o bar -lfoo bar.c

install: bar
	mkdir -p $(DESTDIR)/usr/bin
	cp bar $(DESTDIR)/usr/bin

clean:
	rm -f bar
