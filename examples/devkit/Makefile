PREFIX=/usr/local
CC=gcc
CFLAGS=-O3 -Wall -I../../libs
LDLIBS=-L../../libs/exanic -lexanic

EXASOCK_CFLAGS=-I../../libs/exasock/include
EXASOCK_LDLIBS=-L../../libs/exasock/build -lexasock_ext

BIN=libexanic-responder-example exasock-tcp-responder-example custom-filter-example ping-example exanic-devkit-register-read exanic-devkit-register-write exanic-xvcserver
all: $(BIN)

libexanic-reponder-example: libexanic-responder-example.c
	$(CC) $(CFLAGS) $^ -o $@ $(LDLIBS)

exasock-tcp-responder-example: exasock-tcp-responder-example.c
	$(CC) $(CFLAGS) $(EXASOCK_CFLAGS) $^ -o $@ $(LDLIBS) $(EXASOCK_LDLIBS)

custom-filter-example: custom-filter-example.c
	$(CC) $(CFLAGS) $^ -o $@ $(LDLIBS)

ping-example: ping-example.c
	$(CC) $(CFLAGS) $^ -o $@ $(LDLIBS)

exanic-devkit-register-read: exanic-devkit-register-read.c
	$(CC) $(CFLAGS) $^ -o $@ $(LDLIBS)

exanic-devkit-register-write: exanic-devkit-register-write.c
	$(CC) $(CFLAGS) $^ -o $@ $(LDLIBS)

exanic-xvcserver: exanic-xvcserver.c
	$(CC) $(CFLAGS) $^ -o $@ $(LDLIBS)

clean:
	rm -f $(BIN)
