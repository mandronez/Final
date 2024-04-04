These codes were apart of my finals to show my skill with using shell, pointers, and structures.
In the main code, a basic implementation of a shell program in C was being shown. Here's a breakdown of how it works:

Builtin Commands Handling: The shell supports a few built-in commands such as cd, help, and exit. These commands are defined in functions like lsh_cd, lsh_help, and lsh_exit.

Command Execution: If the entered command is not a built-in command, the shell tries to execute it as an external program using execvp in the lsh_launch function. It also handles forking processes to execute commands in the background.

Input Parsing: The shell reads input from the user using getchar() in lsh_read_line. It then tokenizes the input into separate arguments using strtok in lsh_split_line.

Main Loop: The main loop in lsh_loop repeatedly prompts the user for input, reads the input, parses it into arguments, and then executes the command or built-in function accordingly.

Here's a brief overview of the functions:

main: Entry point of the program. It initializes the shell and starts the command loop.
lsh_loop: The main loop of the shell where it reads input, parses it, and executes commands.
lsh_read_line: Reads a line of input from the user.
lsh_split_line: Tokenizes the input line into separate arguments.
lsh_execute: Executes either a built-in command or an external program.
lsh_launch: Launches an external program using execvp after forking.
lsh_num_builtins: Returns the number of built-in commands.

In the math code, the C code demonstrates the use of function pointers and structures to perform arithmetic operations based on user input. Here's how it works:

Function Pointers and Structure: The code defines function pointers pfnMessage and pfnCalculator for displaying messages and performing arithmetic operations, respectively. It also defines a structure sArithMaticOperation that contains an arithmetic result, a function pointer to display messages, and a function pointer to perform arithmetic operations.

Arithmetic Functions: Four arithmetic functions (Addition, Subtraction, Multiplication, Division) are defined to perform the respective operations.

Display Message Function: The Message function is used to display messages with the arithmetic results.

Main Function: In the main function, memory is allocated for an instance of the sArithMaticOperation structure. The user is prompted to choose an arithmetic operation (addition, subtraction, multiplication, division, or exit). Based on the choice, the corresponding arithmetic function is assigned to the function pointer in the structure.

Perform Calculation Function: The PerformCalculation function takes input data and the structure pointer. It then calls the appropriate arithmetic function through the function pointer and displays the result using the display message function.

Looping: The program runs in a loop until the user chooses to exit.

Memory Deallocation: Memory allocated for the structure is freed before the program exits.
