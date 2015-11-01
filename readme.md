# Sublime Terminal

Shortcuts and menu entries for opening a terminal at the current file, or the current root project folder in [Sublime Text](http://sublimetext.com/).

## Features

 - Opens a terminal in the folder containing the currently edited file
 - Opens a terminal in the project folder containing the currently edited file

## Screenshots

![terminal_open](http://wbond.net/sublime_packages/img/terminal/terminal_open.png)

![settings_menu](http://wbond.net/sublime_packages/img/terminal/settings_menu.png)

## Installation

Download [Package Control](http://wbond.net/sublime_packages/package_control) and use the *Package Control: Install Package* command from the command palette. Using Package Control ensures Terminal will stay up to date automatically.

## Usage

 - **Open Terminal at File**
     Press *ctrl+shift+t* on Windows and Linux, or *cmd+shift+t* on OS X
 - **Open Terminal at Project Folder**
     Press *ctrl+alt+shift+t* on Windows and Linux, or *cmd+alt+shift+t* on OS X

In addition to the key bindings, terminals can also be opened via the editor context menu and the sidebar context menus.

## Package Settings

The default settings can be viewed by accessing the ***Preferences > Package Settings > Terminal > Settings – Default*** menu entry. To ensure settings are not lost when the package is upgraded, make sure all edits are saved to ***Settings – User***.

 - **terminal**
     - The terminal to execute, will default to the OS default if blank. OS X users may enter *iTerm.sh* to launch iTerm if installed.
     - *Default: **""***
 - **parameters**
     - The parameters to pass to the terminal. These parameters will be used if no [custom parameters](http://wbond.net/sublime_packages/terminal#Custom_Parameters) are passed via a key binding.
     - *Default: **[]***

## Custom Parameters

With the parameters argument to the *open_terminal* and *open_terminal_project_folder* commands, it is possible to construct custom terminal environments.

The following is an example of passing the parameters *-T 'Custom Window Title'* to a terminal. Please note that this example is just an example, and is tailored to the XFCE terminal application. Your terminal may use the `-T` option for some other features or setting. Custom key bindings such as this would be added to the file opened when accessing the *Preferences > Key Bindings – User* menu entry (the file name varies by operating system).

```json
{
  "keys": ["ctrl+alt+t"],
  "command": "open_terminal",
  "args": {
    "parameters": ["-T", "Custom Window Title"]
  }
}
```

A parameter may also contain the *%CWD%* placeholder, which will be substituted with the current working directory the terminal was opened to.

```json
{
  "keys": ["ctrl+alt+t"],
  "command": "open_terminal",
  "args": {
    "parameters": ["-T", "Working in directory %CWD%"]
  }
}
```

## Changelog

### v1.10.1

 - Replaced readme.creole with readme.md based off of website

### v1.10.0

 - Repaired handling of temporary views in Sublime Text 3

### v1.9.0

 - Added commands to open the terminal from the command palette

### v1.8.2

 - Fixed "--open-in-tab" behavior when no terminal is open

### v1.8.1

 - Repaired FiSH compatibility more elegantly

### v1.8.0

 - Added support for opening a new tab in iTerm

### v1.7.2

 - Repaired handling multiple project folders with same base path and starting name

### v1.7.1

 - Corrected hyphen/dash typo in settings

### v1.7.0

 - Added support for OS specific settings

### v1.6.0

 - Added compatibility for FiSH

### v1.5.0

 - Added support for LXTerminal, Mate Terminal, xfce4, and Linux Mint/Cinnamon

### v1.4.0

 - Added support for Sublime Text 3

### v1.3.1

 - Added support for non-ASCII directory paths
 - Fixed an error popup with some Linux distributions, when unable to determine the default terminal application

### v1.3.0

 - Added %CWD% placeholder for parameters to receive the current working directory the terminal was opened to
 - Tweaked menu entries

### v1.2.0

 - Fixed a bug with Open Terminal at Project Folder when no files are open
 - Added an iTerm.sh script for OS X users

### v1.1.1

 - Fixed a bug in spawning the terminal that would cause cmd.exe to hang

### v1.1.0

 - Added parameters setting
 - Added the parameters arg to the open_terminal and open_terminal_project_folder commands

### v1.0.2

 - Fixed the executable name for the XFCE terminal

### v1.0.1

 - Fixed Terminal.sh to not launch a second window on OS X Lion

### v1.0.0

 - Initial release

## License

All of Sublime Terminal is licensed under the MIT license.

  Copyright (c) 2011 Will Bond <will@wbond.net>

  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in
  all copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
  THE SOFTWARE.
