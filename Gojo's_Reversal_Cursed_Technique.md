After downloading the file, I used ghidra to decompile the binary file.. It gave me a code of many lines.. I just started readin the code from the main function.. In the beginning, it asks us to give any random input.. And then that input undergoes many transformations and gets modified to a string.. The input is stored in a var acStack_419.. Then we can see that the strings s and s00 gets generated after getting transformed by the functions.. And while gng through the functions, there is an ambiguity.. So I once used IDA too.. Then checked both and my ambiguity got erased.. The string s gets generated after undergoing the functions scar(does XOR with 10 for each character),key_e(converts the string to it's ascii values and concatenates them),tomato(rot13),scar,key_e,tomato,scar,key_e,tomato,scar.. The tomato function doesn’t really change the string cuz the input we r giving to tomato function is numbers and rot 13 won’t work on numbers.. Hence the tomato fun actually doesn’t change anythingg.. After all these 10 functions, finally we get the s string.. Same thing happens with s00 too.. But the order of functions is key,scar and tomato 13 times.. After these 13 functions, we will get the s00 string.. After we get the s and s00, there is another logic for s2.. The characters of s and s00 adds up to the empty string s2 alternatively.. Finally a string s2 is generated.. We need to give a input of what our string turns into and enclose it with “#”.. If our string and s2 matches, the flag will be printed.. Else gojo will mock us by flexing his hiding skills.. I wrote a python script for the execution of functions and to concatenate the final string.. I got the flag and submitted it.