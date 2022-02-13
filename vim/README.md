# Vim configuration workshop

> 💡 Content of this workshop is work in progress

## 📙 What you will learn

* It's a beginning
	* Installation
	* Tutorial time
	* Hello world!
	* Basic configuration
* Extend nvim
	* Themes! themes everywhere!
	* Lsp code completion
	* Snippets
	* File lookup

## It's a beginning

> 💡 You can also use vim but you will probably miss Lsp capability.
> There are plugins that do just that though!

### Installation

To install nvim, just use the package manager of your choice!
You will find more instructions [here](https://github.com/neovim/neovim/wiki/Installing-Neovim).

### Tutorial time

**Step 1 - Vim tutor**
> - Do the vim tutorial. You can access it by typing `:Tutor` in nvim or on [openvim](https://www.openvim.com/) if you want a nice gui.
> - You can also use [vim-adventures](https://vim-adventures.com/) but i do not recommand it cause I am so bad at this.
> - It takes about 30 minutes and will give you usefull (and sometimes less usefull) shortcuts to start with.

### Hello world!

**Step 2 - Write some code!**
> Use some C or another language you are familliar with and do the following function.
> - Given a string of characters as parameter
> - If it is an isogram return 0
> - Else return 1.

### Basic configuration

We will do basic configuration:

**Step 3 - Make it clean**
> - Map the `<esc>` key to a more reachable key if needed (i use `<²>`)
> - Make `(`, `[` and `{` autoclose without using plugins
> - Map the `<esc>` key to close escape terminal mode (try `:terminal` in normal mode)
> - Show line numbers, or better: show relative line numbers !
> - Move swap files to another default location (e.g `~/.config/nvim/tmp/`)
> - Make every tab 4 spaces
> - Setup fold methods

> 💡 `:help` is your best friend!

**Choose your path**
> 🔀 **To develop your muscle memory, you will need to write more code.**
> It takes more than a few hours to develop vi like editor muscle memory!

> You can now choose what you will do during the rest of the workshop. You can:
> - Keep going and extend nvim.
> - Make a pause and train your muscle memory. I recommand using [exercism](https://exercism.org) and doing exercises in a language you have already used.

## Extend nvim

### Themes! Themes everywhere!

**Step 4 - Add a plugin manager**
> You can use whatever you want here. I recommand [VimPlug](https://github.com/junegunn/vim-plug).

**Step 5 - Add a theme**
> - Themes are bloat. You just need color to see different parts of statements and expressions.
> - Well just install one. Or not. But install something else then.

> 🔀 **You can do the next steps in any order.** Choose whatever picks your interest!

### Lsp code completion

**Step 6 - LSP is the future and it's included**
> - Check `:help lsp` and add lsp support to your nvim.

**Step 7 - Add clang completion**
> - Add clang and at least one other language server.
> - You can checkout a list of curated language servers on the [nvim-lsp-config repo](https://github.com/neovim/nvim-lspconfig/blob/master/doc/server_configurations.md).
> I recommand `nvim-cmp`.

### Snippets

**Step 8 - Install a snippet plugin**
> - Install a snippet plugin.
> - Create at least 1 snippet that creates a main function when you type `int main` for c programs.
> I recommand `cmp-vsnip`.

### File lookup

**Step 9 - Install a file lookup plugin**
> Finding files so far might have been frustrating. You might have so far:
> - Exited vim to re-enter changing cli argument.
> - Used the command `:e [path]`.
> 
> There are better ways:
> - Fzf
> - NerdTree
