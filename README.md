# Define the README file content
README_CONTENT = "\
# My Shell Project\n\
\n\
This is a simple shell project. It includes the following commands:\n\
- ls: List files and directories\n\
- mkdir: Create directories\n\
- cat: Display file contents\n\
- rm: Remove files or directories\n\
- date: Display the current date and time\n\
\n\
## How to Compile\n\
To compile the shell and individual commands, use the following commands:\n\
\n\
```sh\n\
make compile\n\
``gcc simple_shell.c -lreadline -pthread -lreadline -o shell\n\
make compile\n\
./shell\n\
rm -f shell\n\
rm -f ls\n\
rm -f mkdir\n\
rm -f cat\n\
rm -f rm\n\
rm -f date\n\
```\n\

## Compilation of Individual Commands
To compile individual commands, you can use the following commands:
make compile
gcc ls.c -o ls
gcc mkdir.c -o mkdir
gcc cat.c -o cat
gcc rm.c -o rm
gcc date.c -o date

"

# Rule to create README file
README:
	echo "$(README_CONTENT)" > README.md

# Define the list of targets that don't create files
.PHONY: compile README
