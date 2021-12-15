CC ?= gcc
CFLAGS ?= -Wall

libfoo: foo.c
	$(CC) $(CFLAGS) -fPIC -shared -Wl,-soname,libfoo.so.0 -o libfoo.so.0 foo.c

install: libfoo
	mkdir -p $(DESTDIR)/usr/lib
	cp libfoo.so.0 $(DESTDIR)/usr/lib
	ln -sf libfoo.so.0 $(DESTDIR)/usr/lib/libfoo.so
	mkdir -p $(DESTDIR)/usr/include
	cp foo.h $(DESTDIR)/usr/include

clean:
	rm -f libfoo.so.0
