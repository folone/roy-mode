# Roy-mode
Roy mode is a tiny major mode for emacs. It can be used for editing [roy scripts](http://roy.brianmckenna.org/ "roy scripts").

## Installation

### package.el installation via Marmalade or MELPA

This is the easiest solution, once installed you don't have anything
to add to your emacs config, just open a roy file and you are good to go.

It can be more convenient to use Emacs's package manager to handle
installation for you if you use many elisp libraries. If you have
package.el but haven't added Marmalade or MELPA, the community package source,
yet, add this to your `.emacs` :

Using Marmalade:

```lisp
(require 'package)
(add-to-list 'package-archives
             '("marmalade" . "http://marmalade-repo.org/packages/"))
(package-initialize)
```

Using MELPA:

```lisp
(require 'package)
(add-to-list 'package-archives
             '("melpa" . "https://melpa.org/packages/") t)
(package-initialize)
```

Then do this to load the package listing:

* <kbd>M-x eval-buffer</kbd>
* <kbd>M-x package-refresh-contents</kbd>

If you use a version of Emacs prior to 24 that doesn't include
package.el, you can get it from http://bit.ly/pkg-el23.

If you have an older ELPA package.el installed from tromey.com, you
should upgrade in order to support installation from multiple sources.
The ELPA archive is deprecated and no longer accepting new packages,
so the version there (1.7.1) is very outdated.

#### Install roy-mode

From there you can install roy-mode or any other modes by choosing
them from a list:

* <kbd>M-x package-list-packages</kbd>

Now, to install packages, move your cursor to them and press i. This
will mark the packages for installation. When you're done with
marking, press x, and ELPA will install the packages for you (under
~/.emacs.d/elpa/).

* or using <kbd>M-x package-install roy-mode

### Manual installation
Roy-mode is based on [generic-mode](http://www.emacswiki.org/emacs/GenericMode "generic-mode"), so it needs to be installed.
To install roy-mode, just add `(require 'roy-mode)` to your `.emacs` file.

## Usage

### REPL
You can start REPL by executing `M-x roy-repl`. If you're getting unwanted escape characters in your repl (something like `[1Groy> [0K[6G` instead of `roy>`), add `export NODE_NO_READLINE=1` to your `.bashrc` config.

![Roy mode](http://i.imgur.com/hf3aJ.png)

## TODO
* Add a way to compile to javascript or run file from editor
* Support indentation
