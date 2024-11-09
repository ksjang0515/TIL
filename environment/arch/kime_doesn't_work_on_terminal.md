# kime doesn't work on terminal

## Background

- kime (Korean IME) is installed for korean inputs.
- Environment variables are set according to the kime manual.
- Korean input works for firefox.
- `wayland_enable_ime` is set to `true` on `kitty.config`

## Troubleshooting

1. Check `kime daemon` is running
    - `pgrep kime`, `ps aux | grep "kime daemon"` gave no results, thereby kime daemon wasn't running.
1. Start `kime daemon`
    - Run `kime daemon &` to start daemon
1. Start daemon on boot
    - Add `kime daemon &` to `.bash_profile`.

After walking through the above steps, I was able to type korean on the terminal like, 이처럼 터미널에 한국어를 작성할 수 있네요.
