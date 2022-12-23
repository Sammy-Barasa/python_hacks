# python_hacks
Python hacks I have learnt that are imporant

## TensorFlow
### Enable Long Paths in Windows 10, Version 1607, and Later
Starting in Windows 10, version 1607, MAX_PATH limitations have 
been removed from common Win32 file and directory functions.
To enable,you can use windows registry .reg or use powershell
command.

Powershell command
```sh
New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" `
-Name "LongPathsEnabled" -Value 1 -PropertyType DWORD -Force
```

More on the same following this link
[Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/fileio/maximum-file-path-limitation?tabs=powershell#enable-long-paths-in-windows-10-version-1607-and-later)

## Docker

### Docker desktop stopped running
Remove docker files from the following directory

`
Fix: Manually remove this file <HOME>\AppData\Roaming\Docker\locked-directories
`

## Git remote repo


1. ### Set a new remote

```sh
git remote add origin https://github.com/USER/REPO.git

```

2. ### Check origin
```sh
git remote -v

```
3. ### rename your local branch:

```sh
git branch -m master main
```

4. ### change the tracked branch

```sh
git fetch -p origin
git branch -u origin/main main
```

5. ### change the main local branch

```sh
git remote set-head origin -a
```

6. ### change git init from master to main

```sh
git config --global init.defaultBranch main
```
