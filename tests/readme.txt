vs������cl����:


cl LoadDll.cpp ../MemoryModule.c



rc SampleDLL.rc

cl SampleDLL.cpp  ../MemoryModule.c SampleDLL.res  /link /out:SampleDLL.dll /dll  /machine:x86 

cl SampleDLL.cpp  ../MemoryModule.c SampleDLL.res  /link /out:SampleDLL.dll /dll 







//����ʹ����Դ������(rc.exe) ����.res�ļ�.
rc SampleDLL.rc

//ʹ��cl.exe����������һ��dll��ڵ�(.obj)�����ļ�, /c������ʾ����������, RES.cpp�������������.
cl /c RES.CPP

// ���ʹ�����ӹ���link.exe������Դ(resource.res)��dll��ڶ���(res.obj) ��res.dllģ�������.
link res.obj resource.res /dll /machine:x86 /out:res.dll


