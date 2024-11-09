# Clipboard doesn't work over SSH

## Background

- Following [this](./copy_paste_in_kitty.md), local environment was configured and `kitten clipboard` worked properly.
- While connected to the server, both kitty's copy and paste command doesn't work.

## Troubleshooting

1. Check clipboard tool is installed on the server.
    - `pacman -Q | grep clip` found no clipboard tool installed.
1. Install clipboard package on the server.
    - `pacman -S wl-clipboard`, `wl-clipboard` was chosen to match local clipboard tool.
