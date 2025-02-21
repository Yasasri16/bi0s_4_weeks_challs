How to compile C Program : 
gcc -o <output_file_name> <input_file_name>

The command gdb file_name is used to launch GDB (GNU Debugger) on a specific program, typically a compiled executable or binary file.

Debugging symbols are additional information included in a compiled program to assist developers in debugging. These symbols provide a mapping between the machine code (which the computer can execute) and the source code (which the developer writes).

They will provide more information about function names, variable names, line numbers, source files.

In programming, a.out (short for "assembler output") is the default name for the executable file produced by the GNU gcc or g++ compiler if no output file name is specified using the -o option. It is commonly used in Unix-like systems.

Registers are small, high-speed storage locations within a computer's CPU (Central Processing Unit).

RIP stands for Instruction Pointer Register in the x86-64 architecture. It plays a crucial role in the execution of programs by holding the memory address of the next instruction to be executed by the CPU.

RSP stands for Stack Pointer Register in the x86-64 architecture. It is used to manage the stack in a program's memory, a region used for temporary storage during program execution.

RSI stands for Source Index Register in the x86-64 architecture. It is one of the general-purpose registers and has specific uses in data movement, string operations, and function parameter passing.

print $<reg_name> : to print the value of a register.

p $<reg_name> : same

p/x $<reg_name> : same but prints in hex

To find the random value stored in the stack, you would need to inspect the stack at a particular point during the execution of the program.

examine command is used to inspect memory at a specified address.
x/(no_of_instructions)i

To see all of the assembly instructions in main, we use diassemble main or shortly "disas main"

To see the value on the stack or to look at the memoryon the stack, we use "x/4gx $rsp" 
~ "p/a *(long*) $rsp"

When you use print, gdb will assign it to $1,$2..,etc.. You can use them later by 'printf "%lx",$1'

“Si” is step instruction and “ni” is next instruction.. Both are almost similar with a lil difference.. if u use “si” if the next instruction is the calll of a function, you will step into the code of the function.. where as if u use “ni” , you willl be gng to the next instruction in the main..

Display will allows you to specify information to show up every time gdb breaks or step..

If you use print, you can access the variables or registers later.. We can’t do this with examine..

 inish will run the rest of the current function that we are in until it returns to the main function..

Info break : to see where the break points are set..

del <breakpoint_num> : removes the breakpoint..

Undisplay <number> : to stop displaying

Del display : disables all displays..

Setting break points using their memory address is not that much effective.. Instead, we specify the function it is in and the line it is in.. This is much more effective..

You can set the value of a variable or reg by using “set $<var_name> = <value>”

To change the stack value, 
    We can use “set *(long *) $rsp = <value>”

How to execute gdb scripts :
“Gdb -x <script_name> ./a.out”

If u wanna perform something every time the program hits a break point, you use “commands and write the code in between and end it with end”..

You can use “silent” when you just wanna print the address and nothing else.. 

You can make a file in home directory “~/.gdbinit” which contains these two commands.. “ set disassembly-flavor intel
					source/opt/gef/gef.py”  and these commands run 	every time you run gdb..

Gef adds color coding to all the instructions..

By including the first command in your .gdbinit, it ensures that all disassembled code shown in GDB uses the Intel-style syntax.

The second command you mentioned is used to load the GEF (GDB Enhanced Features) plugin into GDB.
