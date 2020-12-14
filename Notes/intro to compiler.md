# intro to compiler
## Introdution
开始学习compiler的介绍，课程里有一个比较好的图直接搬过来:  
![1.png](https://i.loli.net/2020/12/14/uI3y9LEzvMOB42i.jpg)  
- 解释器Interpreters，输入我们的程序program，数据data，程序直接会产生输出，它在程序执行之前不会对程序进行任何的处理，所以只需要写程序和数据，之后调用解释器这个程序就马上开始运行了，所以我们说解释器是online，意思就是它做的工作都是运行的一部分  
- 编译器compilers，输入我们的程序program，我们会通过编译器得到一个可执行文件exec，通过接受我们的data从而得到输出，所以说我们的编译器是离线的，意味着我们对程序进程预处理，编译器的本质就是一个预处理的工作，输出的文件，我们可以通过不同的输入进行不同的输出，在许多不同的数据集上不用重新编译以及做其他别的处理  

我们的编译器5个重要阶段
- Lexical Analysis  词法分析
- Parsing           解析
- Semantic Analysis 语义分析
- Optimization      优化
- Code Generation   代码生成
## Structure of a compiler
- Lexical Analysis
这里举一个例子：  
I can help you 这句话是由4个单词组成的一句话，我们能很容易的看明白，是因为我们通过了这个空格，以及一些标点分隔符来帮助我们快速的看，假设我们把这句话变成了 Ic anh elpy ou 我们会非常难的去看懂，所以计算机中的词法分析是划分我们程序文本中输入的单词，以及编译器中调用的语句，标记  
`if x == y then z = 1;else z = 2;` 这里有很多的tokens，比如关键字：if then else，变量：x y z，常量：1，2，运算符：== =，标点符号也属于tokens，分隔符空格，用空格去分割了很多的东西，就像变量名和其他的符号一样  
- Parsing 
所以这些词被理解了，我们下一步就是理解句子的结构，首先我们要解析，这个理解起来有点像主谓宾，副词呀等等的，解析出来  
![2.png](https://i.loli.net/2020/12/14/dnpKejNrYmazE71.jpg)  
- Semantic Analysis
语义分析，也相当于类似的类型检查
- Optimization 
主要是将我们的程序Run faster，Use less memory，举个例子:  
`X=Y*0` is the same as `X=0`，但是我们不可以直接这么替换，我必须要知道他们都是int，才可以，因为如果是float，其中有一个数值叫做not a number -> NaN，`NaN * 0 = NaN`，所以如果这种情况的时候进行优化程序会崩溃  
- Code Generation
code gen 可以生成汇编代码，这是很多编译器都会产生的东西，也就是相当于把一种语言翻译成另一种语言  
## The Economy of Programming Languages
大概讲了一下编程语言为什么要有，编译器为什么要有（有点类似于 告诉我们有编译器和编程语言的好处）这节课没讲什么！
