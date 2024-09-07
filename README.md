
# vifm

The classic program that simulates being the Midnight Commander program but with the advantage of being like Vim.

[Screenshot](Screenshot.png)

Everything is better near the keyboard!. 

## Installation

1. You can clone this repository with the next command: 

     ```bash
     git clone https://github.com/SonidoCristalino/vifm
     ```

2. You must clone the repository in `$HOME/.config/`. 
3. If you have another `vifm` directory, please delete it. 

## Image preview

The Image preview in some terminals is a **big problem** and the solution is in the following guide. For this
guide we will assume the following:

1. Ubuntu 22.04.03 LTS
2. We will use [kitty](https://sw.kovidgoyal.net/kitty/) terminal 

Therefore you must be careful from here: 

1. First, you must download the program called [ueberzugpp](https://github.com/jstkdng/ueberzugpp)
2. Please follow the steps indicated on the page according to your operating system. From here to adopt Ubuntu
   as our operating system.
3. Once we generate the repositories within our source.list, we can easily do: `sudo apt-get install
   ueberzugpp`
4. Then, we must download two scripts from the [vifmimg](https://github.com/thimc/vifmimg) page
5. Within this page we must download two scripts: `vifmimg` and `vifmrun`. You must download them in a raw text. 
6. Then, you must copy them to a directory that is into `$PATH`, just like `/usr/local/bin`. 
7. After having copied to this `/usr/local/bin/` directory, we must give it execution access as follows:
   `chmod a+x vifmimg` and `chmod a+x vifmrun` 
8. As our terminal is kitty, so we must follow the following comment:
   https://github.com/jstkdng/ueberzugpp/issues/81#issuecomment-1623923211    As we can see, we need to create
   a file into `$HOME/.config/ueberzugpp/config.json` with the following text: 
   
     ```bash
     {
        "layer": {
            "output": "kitty"
        }
     }
     ```
9. Finally we can generate a trigger from Gnome as follows: 
* Name: vifm
* Command: `kitty sh -c "vifmrun"`
* Shortcut: `Super + r`
1. Enjoy it!
