---
title: "Fixing 'Pytest Command Not Found' Error in Terminal"
date: 2024-02-29T23:21:32+09:00
draft: false
---

## Problem
When attempting to run pytest in your terminal, you encounter the `pytest command not found` error.

## How to Solve It

### Workaround
Use the following command as a workaround
```bash
python3 -m pytest
```

### Reason
The `pytest command not found` error occurs because pytest is not included in the system's PATH variable, making it inaccessible directly from the command line. Using `python3 -m pytest` bypasses this issue by running pytest as a module within the Python environment.

### Solution

1. Identify the pytest path

*Open a terminal and execute the following command to determine the path to pytest*
```bash
which pytest
```
*Note down the path displayed, such as "/Users/user/Library/Python/3.9/bin/pytest"*

2. Edit the Zsh Configuration File

*Use a text editor like nano to edit your Zsh configuration file*
```bash
nano ~/.zshrc
```

3. Add pytest Path to PATH Variable

*Within the ~/.zshrc file, add the pytest path to the PATH environment variable. Append the following line*
```bash
export PATH=$PATH:/Users/user/Library/Python/3.9/bin
```

4. Save and Exit

*Save the changes to ~/.zshrc by pressing Ctrl + X, followed by Y to confirm, and then press Enter.*

5. Apply Changes

*To apply the changes to the current terminal session, run*
```bash
source ~/.zshrc
```

6. Verify can access pytest

*Confirm that pytest is now accessible by checking its version*
```bash
pytest --version
```


### Conclusion
Following these steps should resolve the `pytest command not found` error and allow you to use pytest directly from the terminal without relying on the workaround. 


Happy testing! 😎





