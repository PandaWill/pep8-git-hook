PEP8 Git Commit Hook
====================
This is a pre-commit hook for Git that checks the code to be committed
for Python PEP8 style compliance.  The hook will prevent the commit in
case style violations are detected. The script only checks for violations 
in the changes, not the file as a whole.

This code was forked from [https://github.com/cbrueffer/pep8-git-hook](https://github.com/cbrueffer/pep8-git-hook).


Installation
====================

1. Install the pep8 program: ```$ pip install "pep8>=1.3"```
2. Save pre-commit as your_project/.git/hooks/pre-commit
3. Mark pre-commit executable: ```$ chmod +x your_project/.git/hooks/pre-commit```


Usage
====================
* The hook can be overridden: ```$ git commit --no-verify```
* If you want to modify the list of codes to ignore, edit the ```ignore_codes``` list in the pre-commit file.
* If you want to select only specific codes to scan for, use the ```select_codes``` list.
* Additional arguments to the pep8 program (e.g., ```--max-line-length=120```) can be added to the ```overrides``` list.
