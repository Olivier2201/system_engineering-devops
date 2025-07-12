📘 Project Documentation: Loops, Conditionals, and Input Parsing in Bash
🔰 Project Overview
This project introduces learners to fundamental Bash scripting constructs used for automating tasks. It focuses on:

Loops (for, while, until)

Conditional statements (if, elif, else, case)

File system checks and input parsing

By completing each task, you will gain hands-on experience with logic that’s core to automating real-world shell operations, making your scripts more efficient, adaptable, and responsive.

🛠️ Learning Objectives
By the end of this project, you will be able to:

Use for, while, and until loops to automate repetitive logic

Make decisions in scripts using if, elif, else, and case

Perform file system checks (existence, type, content)

Parse data from file and directory listings

Write Bash scripts that are portable, readable, and functional

📦 Project Setup Instructions
📁 Repository Structure
Create a GitHub repository named:

Copy
Edit
system_engineering-devops
Inside it, create a directory:

Copy
Edit
0x04-loops_conditions_and_parsing
All scripts for this project must be saved inside this directory.

📄 Script Requirements
Each script file must:

Start with the shebang line:

bash
Copy
Edit
#!/usr/bin/env bash
Include a second line that’s a comment describing its purpose

Have execute permissions (chmod +x script_name)

Match exact file names as given in each task

🧪 Auto-Checker Requirements
Use only the allowed constructs per task

Output must match the example exactly

Naming and directory structure must be respected

✅ Tasks Documentation
🔁 0. For Best School Loop
File: 1-for_best_school

Loop Used: for

Goal: Print "Best School" 10 times using for loop.

🔁 1. While Best School Loop
File: 2-while_best_school

Loop Used: while

Goal: Print "Best School" 10 times using while loop.

🔁 2. Until Best School Loop
File: 3-until_best_school

Loop Used: until

Goal: Print "Best School" 10 times using until loop.

🧠 3. If 9, Say Hi!
File: 4-if_9_say_hi

Loop Used: while

Conditionals: if

Goal: Print "Best School" 10 times; on 9th iteration, add "Hi" in the next line.

🧠 4. 4 Bad Luck, 8 Is Your Chance
File: 5-4_bad_luck_8_is_your_chance

Loop Used: while

Conditionals: if, elif, else

Goal: Print:

"bad luck" on iteration 4

"good luck" on iteration 8

"Best School" on all others

🧠 5. Superstitious Numbers
File: 6-superstitious_numbers

Loop Used: while

Conditionals: case

Goal: Print numbers 1–20. For specific numbers:

4: "bad luck from China"

9: "bad luck from Japan"

17: "bad luck from Italy"

📂 6. For ls
File: 8-for_ls

Loop Used: for

Goal: List files in the current directory (not hidden), displaying only the portion after the first dash in the filename.

📄 7. To File, or Not to File
File: 9-to_file_or_not_to_file

Conditionals: if, else

Goal:

Check for existence of a file named school

If exists:

Check if it’s empty

Check if it’s a regular file

💡 Submission Instructions
Preferred (via GitHub Web UI):
Go to your GitHub repo.

Navigate to 0x04-loops_conditions_and_parsing

Click Add file > Upload files

Select each script file created for the tasks

Commit and push changes

Optional (via CLI):
bash
Copy
Edit
git clone https://github.com/your-username/system_engineering-devops.git
cd system_engineering-devops
mkdir 0x04-loops_conditions_and_parsing
# Copy scripts into the folder
git add .
git commit -m "Completed all loop and parsing tasks"
git push
🧪 Auto-Checker Guidelines
Every script must:

Be executable

Output exactly as shown

Use only the permitted constructs per task

Avoid:

Syntax errors

Extra whitespace or output

Unnecessary prompts

🧠 Final Thoughts
This project is the foundation of shell automation. Mastering it gives you the power to:

Replace tedious manual work with precise scripts

Parse, loop, and conditionally process anything in the Unix environment

Think like a sysadmin or DevOps engineer 🔧
