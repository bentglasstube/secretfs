all: secretfs

clean:
	$(RM) secretfs *.o

CFLAGS := $(CFLAGS) -O0 -g -D_FILE_OFFSET_BITS=64
LDFLAGS := $(LDFLAGS) -lfuse -lgfshare

secretfs: secretfs.o sharefarm.o

install: secretfs
	install -Dm 0755 secretfs ${DESTDIR}/usr/bin/secretfs
