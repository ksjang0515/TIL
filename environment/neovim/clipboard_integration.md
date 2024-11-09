# Clipboard Integration

Neovim uses two X11 Selections, Primary and Clipboard, denoted as "*" and "+" respectively [[1]](../arch/primary_vs_clipboard(x_windows_selection).md)

By default ("unnamed"), Neovim uses "*" clipboard (Primary) for operations such as yank, delete, change and put.
Changing the clipboard option to "unnamedplus" to use "+" register (Clipboard), we can start using Neovim operations on system clipboard. [[2]](https://neovim.io/doc/user/options.html#_3.-options-summary)

As I'm using LazyVim, added the following code to `options.lua`.

```lua
vim.opt.clipboard = "unnamedplus"
```

Without proper clipboard tool, Neovim won't be able to use system clipboard. Since I am running on Hyperland, I installed `wl-clipboard` [[3]](https://neovim.io/doc/user/provider.html#clipboard).
