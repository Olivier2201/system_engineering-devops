📘 README: Shell Redirections & Filters (0x02-shell_redirections)

This directory contains scripts that demonstrate basic to intermediate usage of shell redirections, filters, and file handling using standard Linux/Unix shell tools.

✅ Tasks and Explanations

0. Hello World

File: 0-hello_world

Description: Prints Hello, World followed by a new line to standard output.

Command Used: echo "Hello, World"

1. Confused Smiley

File: 1-confused_smiley

Description: Displays the confused smiley "(Ôo)'.

Command Used: echo "\"(Ôo)'"

2. Let's Display a File

File: 2-hellofile

Description: Displays the content of /etc/passwd.

Command Used: cat /etc/passwd

3. What About 2?

File: 3-twofiles

Description: Displays content of /etc/passwd and /etc/hosts.

Command Used: cat /etc/passwd /etc/hosts

4. Last Lines of a File

File: 4-lastlines

Description: Displays the last 10 lines of /etc/passwd.

Command Used: tail /etc/passwd

5. I'd Prefer the First Ones, Actually

File: 5-firstlines

Description: Displays the first 10 lines of /etc/passwd.

Command Used: head /etc/passwd

6. Line #2

File: 6-third_line

Description: Displays the third line of a file named iacta.

Command Used: head -n 3 iacta | tail -n 1

Note: sed is not allowed.

7. It’s a Good File That Cuts Iron Without Making a Noise

File: 7-file

Description: Creates a file named *\'"Best School"\'*$?*****:) with content Best School\n.

Command Used: echo "Best School" > "*\'\"Best School\"\'*\$\?*****:)"

8. Save Current State of Directory

File: 8-cwd_state

Description: Saves output of ls -la to a file named ls_cwd_content.

Command Used: ls -la > ls_cwd_content

9. Duplicate the Last Line

File: 9-duplicate_last_line

Description: Duplicates the last line of the file iacta.

Command Used: tail -n 1 iacta >> iacta

10. No More Javascript

File: 10-no_more_js

Description: Deletes all .js regular files in current directory and subfolders.

Command Used: find . -type f -name "*.js" -delete

📁 Repository Info

GitHub Repository: system_engineering-devops

Directory: 0x02-shell_redirections

Each file corresponds to one task, and should be made executable using:
