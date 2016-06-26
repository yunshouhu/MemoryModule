vs命令行cl编译:


cl LoadDll.cpp ../MemoryModule.c



rc SampleDLL.rc

cl SampleDLL.cpp  ../MemoryModule.c SampleDLL.res  /link /out:SampleDLL.dll /dll  /machine:x86 

cl SampleDLL.cpp  ../MemoryModule.c SampleDLL.res  /link /out:SampleDLL.dll /dll 







//首先使用资源编译器(rc.exe) 生成.res文件.
rc SampleDLL.rc

//使用cl.exe编译器生成一个dll入口的(.obj)对象文件, /c参数表示不进行连接, RES.cpp在文章下面给出.
cl /c RES.CPP

// 最后使用链接工具link.exe链接资源(resource.res)与dll入口对象(res.obj) 到res.dll模块对象中.
link res.obj resource.res /dll /machine:x86 /out:res.dll


