2. ¿Por qué el comando cd es builtin?
    Si un programa cambia su working directory, cambia su working directory y no lo cambia a la shell

3. Si no fuera builtin, ¿qué modificaciones considera necesarias para proveer la misma funcionalidad.
    Que un programa ejecute en nombre de la shell la syscall chdir()
