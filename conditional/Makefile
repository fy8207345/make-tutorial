foo = ok
all:
ifeq ($(foo), ok)
	echo "foo equals ok"
else
	echo "nope"
endif

bar = 
foo = $(bar)

check_define:
ifdef foo
	echo "foo is defined"
endif
ifndef bar
	echo "but bar is not defined"
endif

nullstring = 
foo = $(nullstring) # end of line; there is a space here

check_empty:
ifeq ($(strip $(foo)),)
	echo "foo is empty after being stripped"
endif
ifeq ($(nullstring),)
	echo "nullstring does't even have spaces"
endif

flags:
# Search for the "-i" flag. MAKEFLAGS is just a list of single characters, one per flag. So look for "i" in this case.
ifneq (,$(findstring i, $(MAKEFLAGS)))
	echo "i was passed to MAKEFLAGS"
endif
	echo 'flags'
