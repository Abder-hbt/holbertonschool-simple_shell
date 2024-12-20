<p align="center">
    <img src="https://raw.githubusercontent.com/Abder-hbt/holbertonschool-simple_shell/refs/heads/main/LOGO_SHELL_SF.png" alt="Logo SHELL" style="width: 500px;">
</p>

# Sommaire
- [Description](#description)
- [Appels système et bibliothèques](#appels-système-et-bibliothèques)
- [Structure des fichiers](#structure-des-fichiers)
- [Installation](#installation)
- [Example d'uilisation](#example-d'utilisation)
- [Contributions](#contributions)
- [Auteurs](#auteurs)

# Project SHELL
Ce projet consiste à recréer un shell Unix simplifié en langage C. Le shell permettra d'exécuter des commandes comme `ls` ou `pwd`, de gérer les arguments, de créer des processus avec `fork()`, et d'utiliser les variables d'environnement pour localiser les programmes. Il inclura une boucle interactive pour saisir et exécuter des commandes, tout en gérant les erreurs et en appliquant les concepts fondamentaux des systèmes Unix, comme les appels système et la gestion des processus.

---

## 1. Description
Le Simple Shell est un interprète de commandes UNIX simple, entièrement écrit en C. Le programme fonctionne à partir des commandes bash saisies via l'interface en ligne de commande (CLI) par l'utilisateur. Tout texte séparé par un nombre quelconque d'espaces, de tabulations ou une combinaison des deux est considéré comme un argument. La commande correspondante saisie par l'utilisateur est ensuite analysée et exécutée comme dans un shell UNIX classique.  

**Cycle de vie basique d'un shell :**  
1. Lancer le shell  
2. Attendre une entrée de l'utilisateur  
3. Analyser l'entrée de l'utilisateur  
4. Exécuter la commande et retourner le résultat  
5. Revenir à l'étape 2  

* Vous pouvez terminer le shell à tout moment en tapant la commande `exit` dans l'invite de commande ou en utilisant `Ctrl-D`, qui est interprété comme un End-of-File (EOF).  

---

## 2. Appels système et bibliothèques

This table lists all the System calls `2` and Library calls `3` used in this project, you could read more by clicking on their respective manual pages. 

| Name | Manual page | Brief description |
| --- | --- | --- |
| `access` | <pre>[man 2 access](https://man7.org/linux/man-pages/man2/access.2.html)</pre> | access() function checks whether the calling process can access the file pathname.  If pathname is a symbolic link, it is dereferenced. |
| `chdir` | <pre>[man 2 chdir](https://man7.org/linux/man-pages/man2/chdir.2.html)</pre> | chdir() function changes the current working directory of the calling process to the directory specified in one of its parameters. |
| `execve` | <pre>[man 2 execve](https://man7.org/linux/man-pages/man2/execve.2.html)</pre> | execve() function allows a process to execute another program. |
| `exit` | <pre>[man 3 exit](https://man7.org/linux/man-pages/man3/exit.3.html)</pre> | exit() function causes normal process termination. |
| `fork` | <pre>[man 2 fork](https://man7.org/linux/man-pages/man2/fork.2.html)</pre> | fork() function creates a new process by duplicating the calling process. The new process is referred to as the child process. The calling process is referred to as the parent process. |
| `free` | <pre>[man 3 free](https://man7.org/linux/man-pages/man3/malloc.3.html)</pre> | free() function frees the memory space from the heap, which must have been returned by a previous call to malloc(), calloc(), or realloc(). |
| `getcwd` | <pre>[man 3 getcwd](https://man7.org/linux/man-pages/man3/getcwd.3.html)</pre> | getcwd() function copies an absolute pathname of the current working directory. |
| `getenv` | <pre>[man 3 getenv](https://man7.org/linux/man-pages/man3/secure_getenv.3.html)</pre> | getenv() function searches the environment list to find the requested environment variable. |
| `getline` | <pre>[man 3 getline](https://man7.org/linux/man-pages/man3/getline.3.html)</pre> | getline() function reads an entire line from input, storing the address of the buffer containing the text into a pointer. |
| `isatty` | <pre>[man 3 isatty](https://www.man7.org/linux/man-pages/man3/isatty.3.html)</pre> | isatty() function tests whether a file descriptor refers to a terminal. |
| `malloc` | <pre>[man 3 malloc](https://man7.org/linux/man-pages/man3/malloc.3.html)</pre> | malloc() function dynamically allocates a single large block of memory with the specified size. |
| `perror` | <pre>[man 3 perror](https://man7.org/linux/man-pages/man3/sys_nerr.3.html)</pre> | perror() function produces a message on standard error describing the last error encountered during a call to a system or library function. |
| `signal` | <pre>[man 2 signal](https://man7.org/linux/man-pages/man2/signal.2.html)</pre> | signal() function sets a function to handle signal i.e. a signal handler with signal number, or the address of a programmer-defined function. |
| `strtok` | <pre>[man 3 strtok](https://man7.org/linux/man-pages/man3/strtok.3.html)</pre> | strtok() function breaks a string into a sequence of zero or more nonempty tokens. |
| `waitpid` | <pre>[man 2 waitpid](https://man7.org/linux/man-pages/man2/wait.2.html)</pre> | waitpid() function suspends execution of the calling thread until a child specified by pid argument has changed state. |
| `fprintf` | <pre>[man 3 fprintf](https://man7.org/linux/man-pages/man3/printf.3.html)</pre> | fprintf() function sends formatted output to a stream. |
| `setenv` | <pre>[man 3 setenv](https://man7.org/linux/man-pages/man3/setenv.3.html)</pre> | setenv() function adds a variable to the environment. |
| `unsetenv` | <pre>[man 3 unsetenv](https://man7.org/linux/man-pages/man3/setenv.3.html)</pre> | unsetenv() function deletes a variable from the environment. |
| `write` | <pre>[man 2 write](https://man7.org/linux/man-pages/man2/write.2.html)</pre> | write() function writes to a file descriptor. |
