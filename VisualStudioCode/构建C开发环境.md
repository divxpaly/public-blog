## VisualStudioCode构建C开发环境

1. VisualStudioCode插件安装 `注:安装完成后重启vs`
	- cpptools
	- code runner *//动态运行选中的代码区块*
	- native debug *//gdb图形化调试C/C++*

2. 安装C/C++ 的 GCC 工具链，windows上可以安装[cygwin](cygwin安装/gcc编译环境安装)或者MinGW,设置GCC环境变量，将GCC工具链路“/cygwin/bin”径加入到windows系统环境变量中 

3. 调试C/C++程序
	1. 新建一个源文件:hello.c
	2. 添加头文件索引路径:在hello.c中,include头文件那一行下面有绿色的波浪线,代表vs code的cpptools插件找不到相应路径,提示出现黄色小灯泡符号,点击将生成并打开一c_cpp_properties.json 文件，编辑这个json文件，添加c/c++头文件的路径进去
	    > "includePath": [
                "xxxx","C:/xxx/cygwin64/usr/include/*"
            ],
	3. 编译运行