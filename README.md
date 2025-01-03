# duino
Collection of Arduino libraries and related utilites

| Repo | Description | Status |
| ---- | ----------- | ------ |
| [duino](https://github.com/dhylands/duino.git) | This repository | [<img src="https://github.com/dhylands/duino/actions/workflows/build.yml/badge.svg">](https://github.com/dhylands/duino/actions) |
| [duino_bus](https://github.com/dhylands/duino_bus.git) | Bus/Packet interface for communicating with Arduino devices | [<img src="https://github.com/dhylands/duino_bus/actions/workflows/build.yml/badge.svg">](https://github.com/dhylands/duino_bus/actions) |
| [duino_cli](https://github.com/dhylands/duino_cli.git) | Command Line Interface for Arduino Projects | [<img src="https://github.com/dhylands/duino_cli/actions/workflows/build.yml/badge.svg">](https://github.com/dhylands/duino_cli/actions) |
| [duino_led](https://github.com/dhylands/duino_led.git) | Some LED Abstractions | [<img src="https://github.com/dhylands/duino_led/actions/workflows/build.yml/badge.svg">](https://github.com/dhylands/duino_led/actions) |
| [duino_littlefs](https://github.com/dhylands/duino_littlefs.git) | A CLI Plugin for LittleFS filesystems | [<img src="https://github.com/dhylands/duino_littlefs/actions/workflows/build.yml/badge.svg">](https://github.com/dhylands/duino_littlefs/actions) |
| [duino_log](https://github.com/dhylands/duino_log.git) | A logging abstraction | [<img src="https://github.com/dhylands/duino_log/actions/workflows/build.yml/badge.svg">](https://github.com/dhylands/duino_log/actions) |
| [duino_makefile](https://github.com/dhylands/duino_makefile.git) | Common Makefile rules | [<img src="https://github.com/dhylands/duino_makefile/actions/workflows/build.yml/badge.svg">](https://github.com/dhylands/duino_makefile/actions) |
| [duino_util](https://github.com/dhylands/duino_util.git) | Common Utility functions | [<img src="https://github.com/dhylands/duino_util/actions/workflows/build.yml/badge.svg">](https://github.com/dhylands/duino_util/actions) |
| [duino_vscode_settings](https://github.com/dhylands/duino_vscode_settings.git) | Generate VSCode c_cpp_properties.json file |  |

This is my collection of Arduino libraries. Much of the code is portable and can work in other
environments. Some of the libraries also include python code to allow a host to interact with
an Arduino board.

This page has links to all of the other repositories and contains some scripts for installing
all of the libraries.

## Under Windows, add the Python Scripts directory into your PATH

To determine where the scripts directory is located, do the following:
```bash
python -m site
```
This will print something like the following:
```bash
PS C:\Users\dhyla> python -m site
sys.path = [
    'C:\\Users\\dhyla',
    'C:\\Program Files\\WindowsApps\\PythonSoftwareFoundation.Python.3.9_3.9.3568.0_x64__qbz5n2kfra8p0\\python39.zip',
    'C:\\Program Files\\WindowsApps\\PythonSoftwareFoundation.Python.3.9_3.9.3568.0_x64__qbz5n2kfra8p0\\DLLs',
    'C:\\Program Files\\WindowsApps\\PythonSoftwareFoundation.Python.3.9_3.9.3568.0_x64__qbz5n2kfra8p0\\lib',
    'C:\\Users\\dhyla\\AppData\\Local\\Microsoft\\WindowsApps\\PythonSoftwareFoundation.Python.3.9_qbz5n2kfra8p0',
    'C:\\Users\\dhyla\\AppData\\Local\\Packages\\PythonSoftwareFoundation.Python.3.9_qbz5n2kfra8p0\\LocalCache\\local-packages\\Python39\\site-packages',
    'C:\\Program Files\\WindowsApps\\PythonSoftwareFoundation.Python.3.9_3.9.3568.0_x64__qbz5n2kfra8p0',
    'C:\\Program Files\\WindowsApps\\PythonSoftwareFoundation.Python.3.9_3.9.3568.0_x64__qbz5n2kfra8p0\\lib\\site-packages',
]
USER_BASE: 'C:\\Users\\dhyla\\AppData\\Local\\Packages\\PythonSoftwareFoundation.Python.3.9_qbz5n2kfra8p0\\LocalCache\\local-packages' (exists)
USER_SITE: 'C:\\Users\\dhyla\\AppData\\Local\\Packages\\PythonSoftwareFoundation.Python.3.9_qbz5n2kfra8p0\\LocalCache\\local-packages\\Python39\\site-packages' (exists)
ENABLE_USER_SITE: True
```
Find the entry that's in `C:\Users` and ends in `site-packages`. Try replacing `site-packages` with `Scripts`.

If you see something like the following, then that should be the correct directory.

```bash
PS C:\Users\dhyla> dir C:\\Users\\dhyla\\AppData\\Local\\Packages\\PythonSoftwareFoundation.Python.3.9_qbz5n2kfra8p0\\LocalCache\\local-packages\\Python39\\Scripts


    Directory: C:\Users\dhyla\AppData\Local\Packages\PythonSoftwareFoundation.Python.3.9_qbz5n2kfra8p0\LocalCache\local-packages\Python39\Scripts


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        2024-11-23  11:06 PM         106422 pip.exe
-a----        2024-11-23  11:06 PM         106422 pip3.9.exe
-a----        2024-11-23  11:06 PM         106422 pip3.exe
```

Add the `Scripts` directory to your PATH (aka Path). See this [article](https://www.architectryan.com/2018/03/17/add-to-the-path-on-windows-10/) for a step-by-step guide on adding a directory to your PATH. You'll probably need to reboot to have the
updated PATH take effect.

## Installing duino from zip files

To install the duino libraries from zip files, start a shell and and cd into your Arduino directory (the directory that holds the sketches and has the libraries directory) and execute:
```bash
pip install duino
install-duino-from-zip
```
pip install puts the install-duino-from-zip program into your Scripts directory, so ensure that it's in
your PATH.

## Installing duino from git

To git clone all of the git repos, start a shell and cd into your Arduino directory (the directory that holds the sketches and has the libraries directory) and execute:
```bash
pip install duino
install-duino-from-git
```
pip install puts the install-duino-from-git program into your Scripts directory, so ensure that it's in
your PATH.
