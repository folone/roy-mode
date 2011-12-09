# Roy-mode
Roy mode is a tiny major mode for emacs. It can be used for editing [roy scripts](http://roy.brianmckenna.org/ "roy scripts").

## Installation
Roy-mode is based on [generic-mode](http://www.emacswiki.org/emacs/GenericMode "generic-mode"), so it needs to be installed.
To install roy-mode, just add `(require 'roy-mode)` to your `.emacs` file.

## Usage

### REPL
You can start REPL by executing `M-x roy-repl`. If you're getting unwanted escape characters in your repl (something like `[1Groy> [0K[6G` instead of `roy>`), add `export NODE_NO_READLINE=1` to your `.bashrc` config.

![Roy mode](http://i.imgur.com/hf3aJ.png)

## TODO
* Add a way to compile to javascript or run file from editor
* Support indentation
