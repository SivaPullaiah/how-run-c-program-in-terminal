# how-run-c-program-in-terminal
How to write, compile and run your first C program
This is a tutorial which will teach you how to run your first C program. You will learn how to:

Edit C source code files with Notepad++
Access Cygwin Terminal on Windows 10
Compile source code with the GCC compiler to get an executable file
Let's get started!

STEP 1. Write and save the program
To write the source code of your first C program you need to open the Notepad++ text editor. The quickest way to do that in Windows 10 is to hit your Win key, type Notepad++ in the search window, and hit Enter.

Once you get the text editor running, copy the following piece of C source code:

/* hello.c
   A first program in C */
#include <stdio.h>

int main()
{
   printf("Hello Your name\n");
   printf("Welcome to EEE1008\n");

   return 0;
}
and paste it into the editor.

Yes, this is your first C program! Now you can save the file somewhere, choosing C source file in the Save as type drop-down menu, and naming it hello.c. You must carefully note the location of the saved file, it should be something like C:/Users/b1234567/EEE1008/hello.c, where b1234567 is your student number.

Once the first program has been written, we want to find out what it actually does. We need to make the computer to execute it.

To do that, we need to translate out program into the form computers understand and execute. In the next step we will use the GCC compiler to get an executable file.

STEP 2. Open Cygwin Terminal
We will be using the GCC compiler as a command line application, so we need to access the command line (also known as terminal).

You can do that in a similar way you did with Notepad++: hit you Win key and type Cygwin. The first option you get is likely to be the Cygwin64 Terminal --- this is what you need.

STEP 3. Navigate to your program with Cygwin Terminal
Now you need to find your program. Remember you had to take note of its location? Let's assume its location is C:/Users/b1234567/EEE1008/hello.c. To compile and execute your program you need to get to the directory C:/Users/b1234567/EEE1008/ by changing your current directory with the cd (stands for change directory) command.

cd C:/Users/b1234567/EEE1008/
You can check where you are with the pwd (print working directory) command:

pwd
If everything is all right, you'll get this:

/cygdrive/c/Users/b1234567/EEE1008/
You can browse the contents of the directory to make sure your source code file is here with the ls (list files) command:

ls
The result should be similar to this:

hello.c
STEP 4. Compile the program to get the executable file
To compile your program and get an executable, you need to run the GCC compiler supplying the source file name and the output executable file name. You can do so with the following command:

gcc hello.c -o hello.exe
The command should silently exit and create the executable file hello.exe containing the compiled program ready for execution.

STEP 5. Run the executable
To run the executable, simply type its name adding characters ./ in front of it, like this:

./hello.exe
This should result in the following lines appearing in the terminal:

Hello Your name
Welcome to EEE1008
Congratulations! You have just written, compiled and executed your first C program! It's alright for now if you have no idea what's going on, soon it will all become clear. Stay tuned! As a simple exercise, try to modify the program so that it actually prints your name instead of the text "Your name".
