CC ?= cc
CFLAGS ?= -O2 -Wall -Wextra -std=c11
LOCAL_CFLAGS = -I../../vendor/bonfyre-core/lib/libbonfyre/include
LDFLAGS  = -L../../vendor/bonfyre-core/lib/libbonfyre -lbonfyre
TARGET = bonfyre-pipeline
SRC = src/main.c

all: $(TARGET)

$(TARGET): $(SRC)
	$(CC) $(CFLAGS) $(LOCAL_CFLAGS) -o $(TARGET) $(SRC) -lsqlite3 $(LDFLAGS)

clean:
	rm -f $(TARGET)

.PHONY: all clean
