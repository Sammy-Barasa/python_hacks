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
## Python notebooks

### Converting python notebooks to markdown
```
jupyter nbconvert qc.ipynb --to markdown
```




## WSL2 

### Logs in as root user by default on startup

Solution is change user id of the user you want as default at the registry editor

1. #### Find your UID for your username in your Linux distro

```sh
id -u <yourUserName>
```

2. #### Open registry edit and navigate to

```
HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Lxss\{MY-UUID}
```
Please be careful when editing registry keys!

3. #### Replace the ***DefaultUid*** value with the UID value of the user in your distro.

For more information visit [github_wsl_issue](https://github.com/microsoft/WSL/issues/4276)

## Common Django Packages
1. django
2. django-cors-headers
3. django-phone-field
4. djangorestframework
5. djangorestframework-simplejwt
6. drf-yasg
7. gunicorn
8. postgres
9. psycopg2-binary
10. PyJWT
11. whitenoise
