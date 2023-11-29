SHELL=/bin/bash
# default shell is /bin/sh, you can change this by changing the variable SHELL

# add an @ before a command to stop it from being printed
# you can also run make with -s to add an @ before line automaticlly

all:
	@echo "This make line will not be printed"
	echo "But this will:"

	cd ..
	# the cd command above dose not affect this line, because each command is effectively run in a new shell
	echo `pwd`

	# this cd command affects the next because they are on the same shell
	cd ..;echo `pwd`

	# Same as above
	cd ..; \
	echo `pwd`

error:
	# Add -k to make to continue running even in the face of errors.
	# this error will be printed but ignored, and make will continue to run
	# Add a - before a command to suppress the error
	# Add -i to make to have this happen for every command.
	-false
	touch error
