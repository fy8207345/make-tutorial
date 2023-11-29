# 定义变量
files := file1 file2

# 使用变量
some_file: $(files)
	echo Look at this variable: $(files)
	touch some_file

file1:
	touch file1

file2:
	touch file2

clean:
	rm -f file1 file2 some_file


a := one two # a is set to the string "one two"
b := 'one two' # b is set to the string "'one two'"!!!!! Not recommend!!
all:
	printf '$a\n' # printf需要带上引号
	printf $b\n # 不带引号会导致换行无法输出

x := dude
var:
	echo $(x) # 两种方式均可取值
	echo ${x}


# 多目标: 目标可以没有命令要执行
multi: f1.o f2.o

f1.o f2.o:
	echo $@
# 用以下一样
# f1.o:
# 	echo f1.o
# f2.o:
# 	echo f2.o
