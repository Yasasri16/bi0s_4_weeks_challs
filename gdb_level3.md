Executing the file :

![Screenshot 2024-11-29 162620](https://github.com/user-attachments/assets/a4d5f293-dc7c-46d2-8298-df08a6fd48dd)

![Screenshot 2024-11-29 160317](https://github.com/user-attachments/assets/d473a74f-9e29-4be4-91cc-d80f0a135570)

After executing the file, gdb took control over this program.

![Screenshot 2024-11-29 163703](https://github.com/user-attachments/assets/a18796c5-2741-4cad-95ed-8688dc9d5e87)

First we need to find where the random value is being set.

so we use "ni" over and over again to go through the program and find where the random value is set.

![Screenshot 2024-11-29 164608](https://github.com/user-attachments/assets/e8653ddd-bd4a-4f42-aa60-95da8cc1ffc3)

We must figure out the random value on the stack.

So we used "x/8gx" on rsp to see the values on the stack. x is short for "examine". 8 is the number of values you wanna see. g is short for "giant" and x is for "hex". 

After looking at the values, we use "c" to go on.

After the random value is set, we use examine command again. 

There will be change in one value because a random value is set.

![Screenshot 2024-11-29 164635](https://github.com/user-attachments/assets/44f76f13-41c7-4b93-879f-b0e4c5b9cc98)

Then we use "c" to go through the program. 

It asked us to give the random value.

After entering the value, we will get the flag.
