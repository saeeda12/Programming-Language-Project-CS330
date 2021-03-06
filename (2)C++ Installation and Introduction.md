##C++ Installation and Programming Environment
**Amal Saeed**




In this second addition to learning C++, we will learn how to install C++ so we can write and execute programs in the language. C++ can be installed on any operating system - Windows, Mac, or Unix/Linux. 

First, we will need to install a compiler, as C++ is a compiled language. The most popular compiler is the GNU C/C++ (GCC) Compiler. 

**WINDOWS:** To install GCC on a Windows machine you need to install MinGW - a minimalist development environment for native Microsoft Windows applications. To install MinGW, go to the [MinGW homepage](www.mingw.org), and follow the link to the MinGW download page. Download the latest version of the MinGW installation program, which should be named MinGW-<version>.exe. While installing MinGW, at a minimum, you must install gcc-core, gcc-g++, binutils, and the MinGW runtime, but you may wish to install more. Add the bin subdirectory of your MinGW installation to your PATH environment variable so that you can specify these tools on the command line by their simple names. When the installation is complete, you will be able to run gcc, g++, ar, ranlib, dlltool, and several other GNU tools from the Windows command line.

**LINUX/ UNIX:** If you are running Linux or UNIX, check whether GCC is installed on your system by entering the following command from the command line: `$ g++ -v` . If you have installed GCC, then it should print a similar message:
``````
Using built-in specs.
Target: i386-redhat-linux1Configured with: ../configure --prefix=/usr .......
Thread model: posix1gcc1version 4.1.2 20080704 (Red Hat 4.1.2-46)
``````

If GCC is not installed, then you will have to install it yourself via the command line. You can enter: 
```
sudo apt-get install build-essential`
```
OR
````
$ sudo yum group install "Development Tools"
`````

If the last command failed, type in: 
````
# yum groupinstall "Development Tools"
`````


**MAC:** I have a Macbook, so all I needed to do was install Xcode (the latest non-beta version: 7.2.1) from the App Store, which includes the Xcode IDE and a compiler. But make sure you have enough space on your machine! Xcode is a little over 4 GB. There is also another free tool called [Code::Blocks](http://www.codeblocks.org/) which includes both an IDE and a compiler, and is available for Windows, Linux, *and* Mac. Click on the downloads tab, choose "Download the binary release" and then choose your OS and download the setup file.

Sources:
- http://www.tutorialspoint.com/cplusplus/cpp_environment_setup.htm
- https://gcc.gnu.org/wiki/FAQ?highlight=%28%28InstallingGCC%29%29
- http://www.mingw.org
- http://www.cyberciti.biz/faq/centos-rhel-7-redhat-linux-install-gcc-compiler-development-tools/
- http://crybit.com/how-to-install-gcc-gnu-c-c-compiler-unixlinux/

Next, choose a text editor to type your programs in as your IDE (integrated development environment) - for example, Notepad on Windows, TextEdit or TextWrangler for Mac, and vi or vim for Unix/Linux. You must save your C++ files with .cpp, .cp or .c extensions. By the way, C++ does *not* come with a recommended programming environment.

However, in Xcode, I can write all of my programs in the application, so there is no need to use a separate text editing application. Go to File -> New Project, then click on Application under OS X, then choose Command Line Tool and hit next. And then you can name the project, and choose which language you would like to program in (Swift, Objective-C, C++, or C). This creates a folder, with a main.cpp file already written in C++ that executes the basic "Hello World!" program; you can write your C++ code in the folder, as well as create new files. After writing the program, there is a play button in the upper right of Xcode that builds and then executes the program. If there are problems in the program, it will say Build Failed and highlight where there are errors in your program.

There is not a lot of boiler-plate code that you need to write in order to write a program, at least not as much as in Java. It needs a header, in the program pasted below, that header is <iostream> and the pound # sign at the beginning of the line targets the compiler's pre-processor; `#include` tells the processor to include the `<iostream>` header which allows the use of `cout`. The `using namespace std;` line tells the compiler to use the standard namespace, and `cout` displays the following string line to the screen. And program execution begins with the main function `int main()`. 

Here is a sample program:
`````
#include <iostream>
using namespace std;
int main() {
    cout << "Hello world!";
    return 0;
}
`````

In C++, comments are written the same way as in Java: `//this is a single-line comment` and `/*this is a multi-line comment.*/`
