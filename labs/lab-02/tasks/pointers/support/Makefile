CC = gcc
CFLAGS = -Wall
LDFLAGS =

TARGET_EXEC = main

SRCS := $(shell find $(SRC_DIRS) -name "*.c")
OBJS := $(SRCS:.c=.o)

$(info OBJS is $(OBJS))
$(info SRCS is $(SRCS))

$(TARGET_EXEC): $(OBJS)
	$(CC) $(OBJS) -o $@ $(LDFLAGS)

.o: %.c
	$(CC) $(CFLAGS) $(LDFLAGS) -c $< -o $@

.PHONY: clean

clean:
	$(RM) -r *.o $(TARGET_EXEC)
