# System Calls

> [!NOTE]
>
> ## System Call
>
> Se puede ver como una simple llamada a función que además cambia a modo `kernel`
>
> **Objetivo de una `syscall`**: Proveer un conjunto abstracto y limpio del hardware y administrar los mismos
>
> El mecanismo para realizar una `syscall` depende de la arquitectura y debe expresarse en `assembler`
>
> Se provee una librería para poder realizarlas desde un lenguaje de alto nivel
>
> > Para poder ver que `syscall` usa un programa, se puede usar `strace` (Los virus se llaman `strace` a ellos mismos para que los antivirus no lo hagan)

```cpp
#define TRUE 1

while (TRUE) {
    type_prompt();                          // Display prompt on the screen
    read_command(command, parameters);      // Read input from terminal

    if (fork() != 0){                       // For off child process
        // Parent code          
        waitpid(-1, &status, 0);            // Wait for child to exit
    } 
    else {
        // Child code
        execve(command, parameters, 0)      // Execute command 
    }
}
```

```cpp
int main(void) {
    static char buf[100];

    // ...

    // Read and run input commands.
    while(getcmd(buf, sizeof(buf)) >= 0){
        if(buf[0] == 'c' && buf[1] == 'd' && buf[2] == ' '){
         // Chdir must be called by the parent, not the child.
            buf[strlen(buf)-1] = 0; // chop \n
            if(chdir(buf+3) < 0)
            printf(2, "cannot cd %s\n", buf+3);
            continue;
        }
        if(fork1() == 0)
            runcmd(parsecmd(buf));
        wait();
    }
    exit();
}
```