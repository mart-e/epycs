all: compile

miracl_objs := $(patsubst %.c,%.o,$(wildcard miracl_lib/*.c))

OBJS = $(patsubst %.c,%.o,$(wildcard *.c))


compile: $(OBJS) $(miracl_objs)
	gcc $(OBJS) $(miracl_objs) -o skypkt


%.o: %.c
	gcc -c $< -o $@ -I miracl_lib -I include -fasm-blocks 
