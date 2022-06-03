# Web Dev Setup


This repo hold the info setup proper _Web Dev Setup_ on :
  - Windows 10
  - Gnu/Linux

This repo also covers tips to config WSL, Docker & so.

## Tools
- Basic
- [Terminal tweaks](#terminal-tweaks)
- IDE / Editor
- SQL clients


### Basic
|# |Variable/File | Windows | GNU/Linux |Usage|
|--|--|--|--|--|
|1|`hosts`|`C:\Windows\System32\drivers\etc`|`/etc/hosts`| Manage the host entry which act as lookup for a browser (& all other apps) requests to locate the (internet/intranet) server |
|2|WSL Root|`\\wsl$\Ubuntu`|`/`|ROOT path of WSL within Windows|
|3|HOME dir|`%userprofile%`|`$HOME` or `~`|Path to user's HOME|
|4|SSH dir|`%userprofile%\.ssh`|`$HOME/.ssh`|`id.rsa`, `id_rs.pub` & `known_hosts`|
|5|temp files|`%temp%`|`/tmp/`|Temp dir used by OS / Servers|

### Terminal tweaks
- Terminus
- Git Bash
- WSL terminal

### IDEs / Editors
Choosing and Sticking with an IDE is hard. In fact choosing IDE vs Editor itself is a war. But getting the job done is ultimate goal. There's no perfect IDE/Editor. Every tool has it's own pros and cons.

In my view, an IDE / Editor should support:
- Extending functionality - by means adding more `plugins` & `extensions`
- Increasing productivity - by easing the debugging , automating repeated tasks
- Balancing the life -   by not killing the OS with memory hungry

|IDE/Editor |  Active| License| Plugins| Learning curve| Config effort|
|--|--|--|--|--|--|
|VIM| 	✓ | Opensource|	✓ | Hard| Geeky way
|ATOM|  less active|  Opensource|	✓| Easy| Medium  |
|VS Code| 	✓| Opensource|	✓| Easy| Medium  |
|PHPStorm| 	✓| Fee need to be paid|	✓| Easy| Out of the Box|


#### VIM
- Basic vim configs
- VIM as Web IDE

#### VS code
VS Code generally called as `vscode` is great editor from Microsoft and loved by most developers. Flavors:
  - Codium  - The vanilla flavor of original editor
  - VSCode -  Additional essence added and marketed by Microsoft


#### Atom



In case you encounter errors connecting GitHub, ensure `%userprofile%\.ssh` folder on  has the following all 3 files with right permission:
`id_rsa`, `id_rsa.pub` & `known_hosts`




In case if you prefer to run multi instances of ATOM editor with it's own profile & settings

On Windows modify the `   atom-nightly.cmd` file :

*atom-nightly.cmd* :

`
@echo off
set "ATOM_HOME=C:\Users\kmuthuvel\AppData\Roaming\AtomNightly"
"%~dp0\..\app-1.63.0-nightly1\resources\cli\atom.cmd" %*
C:\Users\kmuthuvel\AppData\Local\atom-nightly\bin>atom-nightly.cmd
`







#### PHPStorm
