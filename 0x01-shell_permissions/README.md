📄 0-iam_betty
✅ Description
This script switches the current user to the user betty.
It uses the su command to change the current session’s user.

📌 Requirements
The script must contain exactly 8 characters (su betty) plus a newline → total 9 characters when checked with wc -c.

You can assume that the user betty exists on the system.

The script must be executable.

🗂️ File Path
Copy
Edit
0x01-shell_permissions/0-iam_betty
⚙️ Usage
bash
Copy
Edit
./0x01-shell_permissions/0-iam_betty
This will prompt for betty's password and switch the shell to betty.

✔️ Check File Length
To verify the file length requirement:

bash
Copy
Edit
tail -1 0x01-shell_permissions/0-iam_betty | wc -c
# Should output: 9
🔑 Permissions
Make sure the script is executable:

bash
Copy
Edit
chmod +x 0x01-shell_permissions/0-iam_betty
📚 Example
bash
Copy
Edit
$ ./0x01-shell_permissions/0-iam_betty
Password:  # (enter betty's password)
betty@ubuntu:~$
✅ Git Commit
bash
Copy
Edit
git add 0x01-shell_permissions/0-iam_betty
git commit -m "Add script to switch user to betty"
git push
