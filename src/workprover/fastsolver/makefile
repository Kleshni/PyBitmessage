CFLAGS += -std=gnu99 -Wall -Wextra -pedantic -O3 -fPIC
LDFLAGS += -shared -Wl,-version-script=main.map

libfastsolver.so: main.map common.o pthread.o
	$(CC) $(LDFLAGS) -o $@ common.o pthread.o -lpthread -lcrypto

common.o: common.h common.c
pthread.o: common.h pthread.c

clean:
	rm -f common.o pthread.o libfastsolver.so
