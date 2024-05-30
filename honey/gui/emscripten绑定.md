 #ui  #ems  

[安装部署教程](https://www.codercto.com/a/59841.html)

基于ems在cpp中写绑定，再用emcc编译器将cpp编译成js文件，同步提供.d.ts文件，使ts侧可以调用接口

ems中绑定时，不要将const A* Var指针通过cosnt_cast<void*>(static_cast<const void*>(Var))转型为void*再传递给ems::val，否则web侧会出现Uncaught报红

在windows平台下，ems安装的环境变量要配置好，否则makefile中调用emcc会出错，makefile中的mkdir -p命令powershell不识别，可以用git bash