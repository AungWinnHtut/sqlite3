# sqlite3
sqlite3 files for programming in gcc

To use sqlite database in gcc, follow these steps...

download sqlites files from here 
[https://github.com/AungWinnHtut/sqlite3/archive/master.zip]

unzip the downloaded file.

copy into your source code folder (.c file included)

sqlite3.dll and sqlite3.h files must be together with your .c files

sample source code can be found here!
[http://www.tutorialspoint.com/sqlite/sqlite_c_cpp.htm]

But from sample you must change #include<sqlite3.h> to #include"sqlite3.h" 

if your source file is test.c then compilation process is like that

gcc -c test.c
gcc -o test.exe test.o sqlite3.dll


Makefile

test.exe: test.o sqlite3.dll
        gcc -o test.exe test.o sqlite3.dll

test.o: test.c
        gcc -c test.c


Code::Blocks  Settings>Compiler settings>Linker settings>Add> then find sqlite3.dll and add. Copy sqlite3.h into your source code folder and you must change  #include"sqlite3.h".
