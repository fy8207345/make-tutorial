one = export blah="I was set!"; echo $$blash

define two
export blah="I was set!"
echo $$blah
endef

all:
	@echo "this prints 'I was set'"
	@$(one)
	@echo "this does not print 'I was set' because each command runs in a seperate shell"
	@$(two)

# target-specific varibales
one: foo = bar
	

one:
	echo foo is defined: $(foo)

other:
	echo foo is nothing: $(foo)


# pattern-specific variables

%.c: foo = bar

blah.c:
	echo foo is defined: $(foo)

blah.o:
	echo foo is nothing: $(foo)
