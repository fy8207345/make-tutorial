new_contents = "hello:\n\ttouch inside_file"
all:
	mkdir -p subdir
	printf $(new_contents) | sed -e 's/^ //' > subdir/Makefile
	cd subdir && $(MAKE)
# Run this with "export shell_env_var='I am an environment variable'; make"
env:
	# Print out the Shell variable
	echo $$shell_env_var

	# Print out the Make varibale
	echo $(shell_env_var)

shell_var=Shell env var, created inside of Make
export shell_var
env2:
	echo $(shell_var)
	echo $$shell_var

# Recursive variable. This will print "later" below
one = one $(later_variable)
# Simply expanded variable. This will not print "later" below
two := two ${later_variable}

later_variable = later

recursive:
	echo $(one)
	echo $(two)

three = hello
# one gets defined as a simply expaned variable (:=) and thus can handle appending
three := $(three) four
three:
	echo $(three)


# ?= only set variables if they have not yet been set
four = hello
four ?= will not be set
five ?= will be set
five:
	echo $(four)
	echo $(five)

# 字符串的尾部空格会被清除，但头部的空格会保留
white_spaces = hello
after = $(white_spaces)there

nullstring =
space = $(nullstring) # Make a variable with a single space.
space:
	echo $(after)
	echo $(space)

# 未定义的变量，直接使用会是空字符串
undefined:
	echo $(undefined)


# += 用于拼接字符串
foo := start
foo += more
append:
	echo $(foo)

# 命令行参数与覆盖
# Overrides command line arguments
override option_one = did_override
# Does not override command line arguments
option_two = not_override
override_target:
	echo $(option_one)
	echo $(option_two)


clean:
	rm -rf subdir
