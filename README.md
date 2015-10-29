# Vim 配置备份

#### By Wang Hsutung

欢迎 __喜欢 Vim 的同学__ 与我交流 Vim 使用中的一些小技巧, 亦或是一些非常 awesome 的插件 :-)  

## 安装方法
~1. 克隆本配置到本地:~
~2. 安装 [Vundle](https://github.com/VundleVim/Vundle.vim), 一个 Vim 插件管理器;~
~3. 安装 Debian 8 源里已经编译好的 Ycm 插件 (Ubuntu 14.04 以后的版本也有)~
~4. 用 Vim-addon-manager 把 Ycm 链接到 ~/.vim 目录下~
~5. 运行 `:PluginInstall` 安装所有插件 (Github 在中国网速慢, 请耐心等待)~
6. 把 ~/.vim/myconf/sourceCodeMode.vim 中的个人信息改成你自己的


## **SourceCodeMode.vim** 简略说明


* 按 `\\if` 可快速插入 `if() {}` 代码块, `\\fo` 插入 `for(;;) {}`. 其他请见 ~/.vim/myconf/sourceCodeMode.vim 源码;
* 简单的代码片段插入：
 * 按 `\\if` 可快速插入 `if () {}`
 * 按 `\\ie` 可快速插入 `if () {} else {}`
 * 按 `\\ei` 可快速插入 `else if () {}`
 * 按 `\\el` 可快速插入 `else {}`
 * 按 `\\fo` 可快速插入 `for (;;) {}`
 * 按 `\\wh` 可快速插入 `while () {}`
 * 按 `\\dw` 可快速插入 `do {} while ();`
 * 按 `\\cl` 可快速插入 `class X{};`
 * 按 `\\st` 可快速插入 `struct X{};`
* 编辑 C/C++、Java、Python 等文件时，按 `<F3>` 进行语义补全；
* 快速编译运行:
 1. 按 `<F5>` 编译当前文件. 如果当前目录下有 Makefile, 直接 make, 否则执行类似 `gcc -Wall -g main.cpp -o main` 的命令.
 可以调用 `:call SetMakeprg()` 设置编译程序的命令和参数
 2. 按 `<F7>` 执行对应可执行文件(比如, 在编辑 main.cpp, 则运行 ./main)
 3. 按 `<F9>` 一键编译运行
 可以调用 `:call SetRunprg()` 设置执行可执行的命令和参数

模板文件示例:

~/Templates/C源代码.c
```C
/*
 * Author:
 * Date:
 * Locale:
 * Email:
 */

#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[])
{
    printf("Hello, world!\n");
    exit(EXIT_SUCCESS);
}
```

~/Templates/C++源代码.cpp
```C++
/*
 * Author:
 * Date:
 * Locale:
 * Email:
 */

#include <iostream>
#include <string>
#include <vector>
#include <cstdlib>

using namespace std;

int main(int argc, char *argv[])
{
    cout << "Hello, world!" << endl;
    exit(EXIT_SUCCESS);
}
```


~/Templates/Java类样本.java
```Java
/**
 * Author:
 * Date:
 * Locale:
 * Email:
 */
import java.util.*;

public class ClassName {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("int >> ");
        int n = input.nextInt();
        System.out.println("Your input: " + n);
    }
}
```
