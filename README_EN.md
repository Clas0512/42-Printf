# ft_printf

This project is a low-budget version of the popular printf() function in the C language. It can be considered low-budget because ft_printf has significant differences compared to printf. For example, this function does not include "Buffer Management" like printf. Another example is that this function supports only 8 out of the "diouxXfFeEgGaAcsb" formats supported by printf.

## Requirements
- C Compiler: The project is written in the C programming language, so you need a C compiler such as GCC (GNU Compiler Collection) or a similar compiler. GCC is usually the default compiler on Linux and other Unix-based systems. You can download it from here if you don't have it installed.
- Standard C Library: The functions and data types used in the project are dependent on the C language's standard library. This library comes as part of your C compiler and is typically already installed on your system.
- Make: The project includes a configuration file called Makefile to compile and build it. This file uses the Make tool to automate the compilation process. Therefore, you need to ensure that the Make tool is installed on your system.

Note: The required compiler and tools are usually included by default in most Unix-based operating systems. However, for Windows operating systems, you may need to install additional tools such as GCC and Make.

## Installation
1. Download the project files or create a directory to contain them.
2. Open a terminal and navigate to the project directory.
3. Use the "Make" command to compile the project.

        make
   This command will create a static library file named libftprintf.a.
4. Once the compilation is successful, include the ft_printf.h header file in your C file that will use the project.
5. Compile and run your project.

        gcc -o program_name.c ft_printf.a
    This command will combine the C file named program_name.c with the library file ft_printf.a to create an executable file named program_name. You can then run it using the command:

        ./program_name

## Usage
The ft_printf function is used with formatting specifiers and variable arguments. The function processes the special formatting tokens (%d, %s, %c, etc.) in the format string and outputs the result to the console.

Example Usage:


    #include "ft_printf.h"

    int main()
    {
        char *str;
        int  i;

        str = "World";
        i = 10;
        
        ft_printf("Hello, %s! Today %d. day.", str, i);
        return 0;
    }
The function takes the values corresponding to the placeholders in the format string and prints the result to the console.

### Make Commands
- make all: Compiles the default target for the project. This command is automatically executed when you run the make command.
- make clean: Cleans the object files generated during the compilation process. It deletes the compilation files (*.o).
- make fclean: Calls the make clean command and also cleans the library file. It deletes all the compilation files and the library (*.a).
- make re: Calls the make fclean command and then recompiles the project. It cleans all the files and recompiles the entire project.

### Supported Formatting Specifiers
- %d or %i: Prints integers.
- %u: Prints unsigned integers.
- %s: Prints strings.
- %c: Prints characters.
- %p: Prints pointers.
- %x: Prints hexadecimal integers in lowercase.
- %X: Prints hexadecimal integers in uppercase.

# What I Learned ?
Studied and compared the printf() function in detail, observing how Buffer Management works.

Had to use Variadic Functions and learned how to create flexible and general-purpose functions.

---

If you have any questions, suggestions, or feedback, feel free to reach me at mrb.bn@hotmail.com. I would be happy to assist you with your inquiries :)



