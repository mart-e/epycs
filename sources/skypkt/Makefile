all: compile


OBJS = $(patsubst %.c,%.o,$(wildcard *.c)) miracl.a


compile: $(OBJS) $(miracl_objs)
	gcc $(OBJS) $(miracl_objs) -o skypkt -O0


%.o: %.c
	gcc -c $< -o $@ -I miracl_lib -I include -fasm-blocks
