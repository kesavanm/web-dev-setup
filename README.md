# Web Dev Setup


This repo hold the info setup proper _Web Dev Setup_ on :
  - Windows 10
  - Gnu/Linux

This repo also covers tips to config WSL, Docker & so.

## Tools
- Basic
- [Terminal tweaks](#terminals)
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

### Terminals
- `PuTTY` - every developers first & must have SSH client to connect to remote server.
- `Git Bash` - If there's Git flow on your work, Git bash is life saver. Comes with basic Gnu utilites making you feel in right enviroment. Also used to execute Windows native commands as well as to connect to `dockers`
- `WSL terminal` - This gives access to the WSL where te project most likely lives.
- `Tabby` - Earlier called as `Terminus` , a modern console which can replace all the above. This tabbed terminal let you have as many terminals as need. It can connect to remote SSH, WSL, PowerShell, Command Prompt,Git Bash. All-in-all terminals tool and your swiss-knife! Since this is built on `Electron`, yes this is bit memory hungry.Ready to feed him some gigs

Detailed discussion on [Terminals](tools/terminals)

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
More on [VS code](tools/ide-editor/vscode/README.md)


#### Atom

ATOM is another great editor and favorite of most developers. This great `hackable` editor is from GitHub and the tool comes with lot of out-of-box configs for GitHub & Git integrations. This repo itself built using ATOM editor :)


More on [ATOM](tools/ide-editor/atom)



#### PHPStorm



### SQL clients
SQL clients help you to get connected with RDBMS service. Most common are MySQL/Oracle & MS-SQL. This section covers on how to connect/manage the service

More on [SQL clients](tools/sql-stuffs/README.md )