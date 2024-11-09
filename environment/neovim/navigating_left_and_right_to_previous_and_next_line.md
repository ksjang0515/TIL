# Navigating Left/Right on First/Last Character of the Line to Previous/Next Line

Moving left/right at the first/last character of the line to previous/next line's last/first character can be set by configuring `whichwrap`. Following example shows configuring `h` and `l` for such behavior. Note, configuring `h` and `l` is not recommended as it could alter vim's behavior. For more information refer to `:help whichwrap`

```lua
vim.opt.whichwrap:append("h,l")
```

#### Reference

- [How to move to next line by pressing l at the end of line in VIM? (Stack Overflow)](https://stackoverflow.com/questions/59478077/how-to-move-to-next-line-by-pressing-l-at-the-end-of-line-in-vim)
