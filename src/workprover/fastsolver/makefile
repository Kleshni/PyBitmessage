CFLAGS += -std=gnu99 -Wall -Wextra -pedantic -O3 -fPIC -fvisibility=hidden -v -I/usr/local/opt/openssl/include
LDFLAGS += -shared -v -L/usr/local/opt/openssl/lib
LDLIBS = -lpthread -lcrypto

libfastsolver.so: common.o pthread.o
	$(CC) $(LDFLAGS) -o $@ $^ $(LDLIBS)

common.o: common.h common.c
pthread.o: common.h pthread.c

clean:
	rm -f common.o pthread.o libfastsolver.so
