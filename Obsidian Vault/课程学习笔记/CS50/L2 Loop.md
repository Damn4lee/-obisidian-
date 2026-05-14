## 实现循环的逻辑词
1. while 
	1. 给定特定的“问题”，作为循环运行的前提。比如最开始，我们由掰手指来指挥眼前的Python进行计数
		1. 在此函数的问题一般是一个计数器，初定义一个“计数变量”然后进行加减，一般的我们采取从最开始加到目标循环次数这样子的顺序。
2. for
	1. 为了让我们能够在这个“问题”上有更多的自由，我们有一个for作为新的循环函数
		1. 在这里我们用到一个新的[[数据类型]]：list。剩下的还有整数，浮点，布尔。
		2. 由于我们会出现很多次的循环，这里有一个python的list类型函数，称作range()
	2. for简化了while的步骤，相比于需要定义，定规则的步骤，我们只需要一行代码就可以解决这些。
```python
 for i in[0,1,2]
```
## 一些逐步coding的例子 运用循环
### 检查输入的正负值
```python
n =int(input("What is n?"))
if n<0
   n=int(input("What is n?"))
   if n<0 
	   n=int(input("What is n?"))
```
这样子会无穷无尽，为了方便，我们采取一个思路：不妨让这个无限的循环设为一个默认的，通过遇到特殊情况再去打破，跳出新的循环：
```python
while True
	n=int(input("What is n?"))
	if n<0
		break
		
for _ in range(n)
	print("meow")
```
按照python人的性格来看，这个喵喵的东西，如果能够更加函数化的好，那最好不过了，基于此，让我们来让他更加pythonic
```python
def main():
	number=get_number
	meow(number)
	
def get_number():
	while True
	n=int(input("What is n?"))
	if n>0:
		return n   #p的特点，可以在特定代码块上面改变全局变量,没必要再次全局定义。
		
def meow():
	for _ in range(n)
	print("meow")

```
### list类数据也可以循环，都可以用for进行遍历
举个例子，我们要输出关于霍格沃兹学院的孩子们的名单
```python
students=["a","b","c"]

for student in students
	print(student)
```
for很智能，我们不需要like C去定一个顺序变量，他默认就直接按照顺序做了。
针对字符串表格，如果我们真的想要进行动态的变化，引入len的函数。
### [[dict]]
以霍格沃兹们住宿的地方举例子：
```python
students={
	"Hermione":"Gryffindor",
	"Harry":"Gryffindor",
	"Ron":"Gryffindor"
	"Draco":"Slytherin"
}

for student in students:
	print(student,students[student]) 
```
### 复杂的多重循环的嵌套
```python
def print_square(size)
	for i in range(size)
		for j in range(size)
			print("#",end="")
			
		print()

```


