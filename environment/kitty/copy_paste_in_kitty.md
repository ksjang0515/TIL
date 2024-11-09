# Copy and Paste in Kitty

Using clipboard in Kitty terminal is simple, refer to the following example [[1]](https://sw.kovidgoyal.net/kitty/kittens/clipboard/).

```bash
# copy
echo 123 | kitten clipboard

# paste
kitten clipboard --get-clipboard
kitten clipboard -g
```

To stop Kitty from asking for permission on paste, configure `clipboard_control` on Kitty config from `read-clipboard-ask` to `read-clipboard` [[2]](https://sw.kovidgoyal.net/kitty/conf/#opt-kitty.clipboard_control).

```conf
clipboard_control write-clipboard write-primary read-clipboard read-primary-ask
```
