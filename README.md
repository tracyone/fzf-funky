fzf-funky
============
A super simple function navigator for [fzf](https://github.com/junegunn/fzf), porting from [ctrlp-funky](https://github.com/tacahiroy/ctrlp-funky).It is a very useful plugin when ctags is not exist or lsp is not support.

- Support neovim's floating window feature!
- Support vim's popup window feature!

SYNOPSIS
----------
This is a [fzf](https://github.com/junegunn/fzf) vim extension. It simply navigates and jumps to function definitions from the current file without ctags. It just searches for function definitions or equivalent lines using regular expressions, therefore some languages' abstractions aren't accurate because of them being hard to parse.

One of advantages of this plugin is that no configuration is required in most cases, so it starts working right after installation with no ctags required.
*If you want to have a more accurate list of function defs, you should use other ctags-based tools, etc.*

[![asciicast](https://asciinema.org/a/253055.svg)](https://asciinema.org/a/253055)

Support preview:

![Image](https://github.com/user-attachments/assets/f6e393ae-3416-46eb-a6ed-b9d78af755e7)

### Supported filetypes:

* c
* carbon
* cf (ColdFusion)
* clojure
* cmm (TRACE32)
* coffee-script
* coldfusion
* cpp (C++)
* cs (C#)
* css (css, scss)
* dart
* elixir
* elm
* fish (fish-shell)
* go (Golang)
* graphql
* groovy
* haskell
* html/xhtml
* java
* javascript
* Jenkinsfile (Jenkins pipeline script)
* jinja (template engine for Python)
* lua
* make (Makefile)
* markdown
* moon (MoonScript)
* nerdtree
* objc (Objective-C)
* perl
* php
* plsql (PL/SQL)
* proto (Protocol Buffers)
* python
* r
* rmd (rmarkdown)
* ruby (ruby, rake, rspec and chef recipe)
* rust
* scala
* sh (bash, dash, fish and zsh)
* sql
* tex (LaTeX)
* tf (terraform)
* thrift
* toml
* typescript
* vb (Visual Basic)
* vim
* vue (Vue.js)
* yaml
* zig


PREMISE
----------

First of all, I believe you're a user of a great Vim plugin called [fzf.vim](https://git::@github.com/junegunn/fzf.vim.git).
Otherwise, you need to install fzf.vim before you start using this plugin.


INSTALLATION
----------

### Plugin managers
It is recommended to install the plugin using plugin managers such as minpac, vim-plug, pathogen, Vundle, Dein.vim etc.
You can copy/paste a line below if you use vim-plug:

```vim
Plug 'junegunn/fzf', { 'dir': '~/.fzf', 'do': './install --all' }
Plug 'junegunn/fzf.vim'
Plug 'tracyone/fzf-funky',{'on': 'FzfFunky'}
```

### Manual installation
If you use neither of the plugin management systems, copy _autoload_ and _plugin_ directories to _.vim_ directory.
On Windows, basically, _vimfiles_ directory is used instead of _.vim_ directory.


CONFIGURATION
--------------
It should be useful to define key mappings like this:
```vim
nnoremap <Leader>fu :FzfFunky<Cr>
" narrow the list down with a word under cursor
nnoremap <Leader>fU :execute 'FzfFunky ' . expand('<cword>')<Cr>
```

LINK
-------

* [ctrlpvim/ctrlp.vim](https://github.com/ctrlpvim/ctrlp.vim)
* [vim.org/ctrlp-funky](http://www.vim.org/scripts/script.php?script_id=4592)
* [junegunn/fzf](https://github.com/junegunn/fzf)


LICENSE
-------

Copyright (C) 2012-2020 Takahiro Yoshihara. Distributed under the MIT License.

[1]: http://i.imgur.com/yO4PWAF.png
[2]: http://i.imgur.com/CnKui5H.png
[3]: http://i.imgur.com/B3hBycd.png
