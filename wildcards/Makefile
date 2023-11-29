# Print out file information about every .c file
print: $(wildcard *.c)
	ls -al $?


# * 错误用法
thing_wrong := *.o # Don't do this! '*' will not get expanded
thing_right := $(wildcard *.o)

all: one two three four

# Fails, because $(thing_wrong) is the string "*.o"
one: $(thing_wrong)

# Stays as *.o if there are no files that match this pattern
two: *.o

# Works as you would expect! In this case, it does nothing
three: $(thing_right)

# Same as rule three
four: $(wildcard *.o)


hey: hey1 hey2
	# outputs "hey", since this is the target name
	echo $@

	# outputs all prerequisites newer than the target
	echo $?

	# output all prerequisites
	echo $^

	touch hey

hey1:
	touch hey1

hey2:
	touch hey2

clean:
	rm -f hey hey1 hey2
