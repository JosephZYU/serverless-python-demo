
/c/Users/josep/bin:/mingw64/bin:/usr/local/bin:/usr/bin:/bin:/mingw64/bin:/usr/bin:
/c/Users/josep/bin:
/c/WINDOWS/system32:
/c/WINDOWS:
/c/WINDOWS/System32/Wbem:
/c/WINDOWS/System32/WindowsPowerShell/v1.0:
/c/WINDOWS/System32/OpenSSH:
/c/Program Files/GitHub CLI:/cmd:
/c/Program Files/Amazon/AWSSAMCLI/bin:
/c/Program Files/nodejs:
/c/ProgramData/chocolatey/bin:
/c/Users/josep/AppData/Local/Programs/Python/Python312/Scripts:
/c/Users/josep/AppData/Local/Programs/Python/Python312:
/c/Users/josep/AppData/Local/Microsoft/WindowsApps:
/c/Users/josep/AppData/Local/Programs/Microsoft VS Code/bin:
/c/Users/josep/AppData/Roaming/npm:/usr/bin/vendor_perl:/usr/bin/core_perl





Given the below Bash Terminal output:

```Bash
Admin@JosephYu-X:/c/JosephYu/serverless-python-demo$ echo $PATH
/c/Users/josep/bin:/mingw64/bin:/usr/local/bin:/usr/bin:/bin:/mingw64/bin:/usr/bin:/c/Users/josep/bin:/c/WINDOWS/system32:/c/WINDOWS:/c/WINDOWS/System32/Wbem:/c/WINDOWS/System32/WindowsPowerShell/v1.0:/c/WINDOWS/System32/OpenSSH:/c/Program Files/GitHub CLI:/cmd:/c/Program Files/Amazon/AWSSAMCLI/bin:/c/Program Files/nodejs:/c/ProgramData/chocolatey/bin:/c/Users/josep/AppData/Local/Programs/Python/Python312:/c/Users/josep/AppData/Local/Programs/Python/Python312/Scripts:/c/Users/josep/AppData/Local/Microsoft/WindowsApps:/c/Users/josep/AppData/Local/Programs/Microsoft VS Code/bin:/c/Users/josep/AppData/Roaming/npm:/usr/bin/vendor_perl:/usr/bin/core_perl
Admin@JosephYu-X:/c/JosephYu/serverless-python-demo$ which python
/c/Users/josep/AppData/Local/Microsoft/WindowsApps/python
Admin@JosephYu-X:/c/JosephYu/serverless-python-demo$ where python
C:\Users\josep\AppData\Local\Microsoft\WindowsApps\python.exe
```
How come that our [Python/Python312] take precedence over the [Microsoft/WindowsApps/python] as reflect on the 'echo $PATH' results, but when we run 'which python' and 'where python', it seems that [Microsoft/WindowsApps/python] still take higher priority over the default [Python/Python312]? Please give advice on how we can always make the [Python/Python312] as our 1st preference?




C:\Users\josep\AppData\Local\Programs\Python\Python312\
C:\Users\josep\AppData\Local\Programs\Python\Python312\Scripts\
%USERPROFILE%\AppData\Local\Microsoft\WindowsApps
C:\Users\josep\AppData\Local\Programs\Microsoft VS Code\bin
C:\Users\josep\AppData\Roaming\npm




/c/Users/josep/bin:/mingw64/bin:/usr/local/bin:/usr/bin:/bin:/mingw64/bin:/usr/bin:
/c/Users/josep/bin:
/c/WINDOWS/system32:
/c/WINDOWS:
/c/WINDOWS/System32/Wbem:
/c/WINDOWS/System32/WindowsPowerShell/v1.0:
/c/WINDOWS/System32/OpenSSH:
/c/Program Files/GitHub CLI:/cmd:
/c/Program Files/Amazon/AWSSAMCLI/bin:
/c/Program Files/nodejs:
/c/ProgramData/chocolatey/bin:
/c/Users/josep/AppData/Local/Programs/Python/Python312:
/c/Users/josep/AppData/Local/Programs/Python/Python312/Scripts:
/c/Users/josep/AppData/Local/Microsoft/WindowsApps:
/c/Users/josep/AppData/Local/Programs/Microsoft VS Code/bin:
/c/Users/josep/AppData/Roaming/npm:/usr/bin/vendor_perl:/usr/bin/core_perl