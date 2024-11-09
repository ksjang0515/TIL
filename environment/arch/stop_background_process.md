# How to stop a process running in the background

1. Find process ID and kill
    1. Get process ID with `pgrep [name]`, `ps aux | grep [name]`, `ps -eaf | grep [name]`.
    1. Kill process with `kill [ID]`.
1. Bring background process to foreground with `fg`.
1. Use `pkill [name]` to kill all process with matching name.

##### Reference

- [How to terminate a background process?](https://unix.stackexchange.com/questions/104821/how-to-terminate-a-background-process)
