# Libasm
The aim of this project is to become familiar with assembly language.

# Common Instructions
-  Your functions should not quit unexpectedly (segmentation fault, bus error, double
free, etc.) except in case of undefined behavior. If this happens, your project will
be considered non-functional, and you will receive a 0 during the evaluation.
-  Your Makefile must at least contain the rules `$(NAME)`, `all`, `clean`, `fclean` and `re`. It must recompile/relink only the necessary files.
- To include bonuses in your project, you must add a bonus rule to your Makefile,
which will incorporate all the various headers, libraries, or functions that are forbidden in the main part of the project. Bonuses must be in different files _bonus.{c/h}.
The evaluation of the mandatory and bonus parts is done separately.
- We encourage you to create test programs for your project, even though this work
won’t have to be submitted and won’t be graded. It will give you a chance
to easily test your work and your peers’ work. You will find those tests especially
useful during your defence. Indeed, during defence, you are free to use your tests
and/or the tests of the peer you are evaluating.
- Submit your work to your assigned Git repository. Only the work in the Git repository will be graded. If Deepthought is assigned to grade your work, it will be done
after your peer-evaluations. If an error occurs in any section of your work during
Deepthought’s grading, the evaluation will stop.
- You must write 64-bit assembly. Beware of the **"calling convention"**.
- You can’t do inline ASM, you must do **’.s’** files.
- You must compile your assembly code with **nasm**.
- You must use the **Intel** syntax, not the AT&T syntax.

It is forbidden to use the compilation flag: -no-pie.

# Mandatory part
- The library must be called libasm.a.
- You must submit a main function that will test your functions and compile with
your library to demonstrate that it is functional.
- You must rewrite the following functions in assembly:
  - `ft_strlen` (man 3 strlen)
  - `ft_strcpy` (man 3 strcpy)
  - `ft_strcmp` (man 3 strcmp)
  - `ft_write` (man 2 write)
  - `ft_read` (man 2 read)
  - `ft_strdup` (man 3 strdup, you can call to malloc)
- You must check for errors during syscalls and handle them properly when needed.
- Your code must set the variable errno properly.
- For that, you are allowed to call the extern ___error or errno_location.

# Bonus part
You can rewrite these functions in assembly. The linked list functions will use the following structure:

typedef struct s_list

{

  void *data;
  
  struct s_list *next;

} t_list;

- ft_atoi_base (like the one in the C-Piscine)
- ft_list_push_front (like the one in the C-Piscine)
- ft_list_size (like the one in the C-Piscine)
- ft_list_sort (like the one in the C-Piscine)
- ft_list_remove_if (like the one in the C-Piscine)

The bonus part will only be assessed if the mandatory part is PERFECT. Perfect means the mandatory part has been integrally done and works without malfunctioning. If you have not passed ALL the mandatory requirements, your bonus part will not be evaluated at all.

# Useful Links

![Structure of a NASM Program](https://cs.lmu.edu/~ray/images/nasmstructure.png)

[Intro to Assembly](https://github.com/0xAX/asm)

[Compiler Explorer](https://godbolt.org/)

[Assembly Files: Difference between .a .s .asm](https://stackoverflow.com/questions/34098596/assembly-files-difference-between-a-s-asm)

[r/asm](https://www.reddit.com/r/asm/wiki/links/)

[Linux System Call Table for x86 64](https://blog.rchapman.org/posts/Linux_System_Call_Table_for_x86_64/)


