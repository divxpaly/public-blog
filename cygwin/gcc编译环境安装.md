## Cygwin安装gcc

1. Cygwin 下载安装网址[ https://cygwin.com/install.html]( https://cygwin.com/install.html "download") 分为32位,64位可按需下载

2. 执行安装,有三种安装模式:
	- **Install from Internet**  直接从Internet安装
	- **Download Without Installing**  只下载Cygwin的组件包,但不安装
	- **Install from Local Directory** 与上面第二种模式对应,当你的Cygwin组件包已经下载到本地,则可以使用此模式从本地安装Cygwin

3. 默认安装源速度慢经常有错误,建议修改下载源为163镜像
   - Add User URL:　[http://mirrors.163.com/cygwin/](http://mirrors.163.com/cygwin/ "mirrors.163.com")
   - 如需以后修改下载源可在Cygwin安装目录\etc\setup\setup.rc文件中修改

4. 下一步可选择需要下载安装的组件包,为了使Cygwin能够编译C\C++程序,需要安装gcc编译器,缺省情况下gcc不会被安装,我们需要选中它来安装,这里我推荐直接退出安装程序然后在命令行下继续执行安装程序:
   	> setup-x86_64.exe -q -P wget -P gcc-g++ -P make -P diffutils -P libmpfr-devel -P libgmp-devel -P libmpc-devel 

5. 验证gcc安装是否成功
	
	> Cygwin.bat > gcc -v