**Linux Processes and Signals Project Documentation**

**Project Title**: Processes and Signals in Linux
**Contribution**: 12.5% of Overall Grade

---

### **Project Description**

This project introduces the fundamentals of Linux process and signal management. Learners will interact with the command line to identify, control, and monitor processes. The tasks are designed to strengthen understanding and practice of process lifecycles, PID tracking, and signal usage.

---

### **Repository Setup**

* **Repository Name**: `system_engineering-devops`
* **Directory**: `0x05-processes_and_signals`
* **Language**: Bash
* **Script Header**:

  ```bash
  #!/usr/bin/env bash
  # A Bash script that [describe task here]
  ```

---

### **Tasks Overview**

#### **Task 0: What Is My PID?**

* **File**: `0-what-is-my-pid`
* **Objective**: Print the PID of the script process itself.
* **Sample Code**:

  ```bash
  #!/usr/bin/env bash
  # A Bash script that displays its own PID

  echo $$
  ```

---

#### **Task 1: List Your Processes**

* **File**: `1-list_your_processes`
* **Objective**: Display all processes with a hierarchical view.
* **Sample Code**:

  ```bash
  #!/usr/bin/env bash
  # A Bash script that lists all currently running processes in a tree format

  ps -e -f --forest
  ```

---

#### **Task 2: Show Your Bash PID**

* **File**: `2-show_your_bash_pid`
* **Objective**: Display lines from `ps` that include the term "bash"
* **Sample Code**:

  ```bash
  #!/usr/bin/env bash
  # A Bash script that shows bash processes
  # shellcheck disable=SC2009

  ps -ef | grep bash
  ```

---

#### **Task 3: Show your Bash PID Made Easy**

* **File**: `3-show_your_bash_pid_made_easy`
* **Objective**: Print only the PID and process name for any bash processes (no `ps` allowed)
* **Sample Code**:

  ```bash
  #!/usr/bin/env bash
  # A Bash script that finds bash processes using /proc

  for pid in $(ls /proc | grep -E '^[0-9]+$'); do
    if [ -f "/proc/$pid/cmdline" ]; then
      cmdline=$(cat /proc/$pid/cmdline | tr -d '\0')
      if [[ $cmdline == *"bash"* ]]; then
        echo "$pid bash"
      fi
    fi
  done
  ```

---

#### **Task 4: To Infinity and Beyond**

* **File**: `4-to_infinity_and_beyond`
* **Objective**: Print message indefinitely every 2 seconds.
* **Sample Code**:

  ```bash
  #!/usr/bin/env bash
  # A Bash script that loops infinitely printing a message

  while true; do
    echo "To infinity and beyond"
    sleep 2
  done
  ```

---

#### **Task 5: Don't Stop Me Now!**

* **File**: `5-dont_stop_me_now`
* **Objective**: Kill the running `4-to_infinity_and_beyond` script.
* **Sample Code**:

  ```bash
  #!/usr/bin/env bash
  # A Bash script that stops the 4-to_infinity_and_beyond process

  pkill -f 4-to_infinity_and_beyond
  ```

---

#### **Task 6: Stop Me if You Can**

* **File**: `6-stop_me_if_you_can`
* **Objective**: Kill the `4-to_infinity_and_beyond` script without using `kill` or `killall`
* **Sample Code**:

  ```bash
  #!/usr/bin/env bash
  # A Bash script that stops 4-to_infinity_and_beyond without kill

  pid=$(pgrep -f 4-to_infinity_and_beyond)
  [ -n "$pid" ] && echo $pid > /proc/$pid/oom_score_adj && echo > /proc/$pid/oom_score_adj && echo "0" > /proc/$pid/oom_score_adj && echo > /proc/$pid/oom_score_adj && echo -15 > /proc/$pid/oom_score_adj && echo > /proc/$pid/oom_score_adj && echo "1" > /proc/$pid/oom_score_adj && echo > /proc/$pid/oom_score_adj && echo kill $pid > /proc/$pid/fd/1
  ```

---

#### **Task 7: Highlander**

* **File**: `7-highlander`
* **Objective**: React to SIGTERM with a custom message.
* **Sample Code**:

  ```bash
  #!/usr/bin/env bash
  # A Bash script that ignores SIGTERM and prints a message

  trap "echo 'I am invincible!!!'" SIGTERM
  while true; do
    echo "To infinity and beyond"
    sleep 2
  done
  ```

#### **Task 67: Stop Highlander**

* **File**: `67-stop_me_if_you_can`
* **Objective**: Stop `7-highlander` script
* **Sample Code**:

  ```bash
  #!/usr/bin/env bash
  # A Bash script that sends SIGTERM to 7-highlander

  pkill -f 7-highlander
  ```

---

#### **Task 8: Beheaded Process**

* **File**: `8-beheaded_process`
* **Objective**: Kill `7-highlander` using SIGKILL
* **Sample Code**:

  ```bash
  #!/usr/bin/env bash
  # A Bash script that kills 7-highlander with SIGKILL

  pkill -9 -f 7-highlander
  ```

---

### **Submission Checklist**

* ✅ GitHub repository named `system_engineering-devops`
* ✅ Folder named `0x05-processes_and_signals`
* ✅ Files named as per task instructions
* ✅ Each script begins with shebang `#!/usr/bin/env bash`
* ✅ Each script has a comment describing what it does
* ✅ Scripts execute correctly when tested via Bash

---

### **Conclusion**

This project builds hands-on skills in managing Linux processes, signals, and using command-line tools effectively. Mastering this helps in automation, system monitoring, and improving overall scripting expertise.

