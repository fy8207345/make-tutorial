hello:
	echo "hello make"
	echo "This command is executed in every build if file 'hello' dose not exist!"

exec: exec.o
	cc exec.o -o exec # run third

exec.o: exec.c
	cc -c exec.c -o exec.o # run second

exec.c:
	echo "int main() { return 0; }" > exec.c #run first

clean:
	rm -f exec

blah: blah.c
	cc -c blah.c -o blah


# 每次都会运行的target
some_file: other_file
	echo "This target will always run , and runs secondly"
	touch some_file
other_file:
	echo "This target will always run, and runs firstly"
