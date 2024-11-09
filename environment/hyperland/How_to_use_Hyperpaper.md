# How to use Hyperpaper

Hyperpaper is a wallpaper utility for Hyperland with simple image display functionality.
By default, configuration file is located at `~/.config/hypr/hyprpaper.conf`.
To run Hyperpaper on startup, edit `hyprland.conf` and add `exec-once = hyprpaper`.
Note, all `img_path` of following examples must be absolute path.

## Preload

- `preload = [img_path]` loads the selected image into memory.

## Unload

- `unload = [img_path]` unloads preloaded image from memory.
- `unload all` unloads all preloaded images.
- `unload unused` unload all undisplayed images.

## Display

For following examples, `[monitor]` can be omitted to apply for all monitors.
To view list of available monitors run `hyprctl monitors`.

- `wallpaper = [monitor], [img_path]` displays the preloaded image to the monitor.
- `wallpaper = [monitor], contain:[img_path]` adjust image to fit the monitor.
- `wallpaper = [monitor], tile:[img_path]` repeat image to cover all monitor.
- `wallpaper = desc:[monitor_description], [img_path]` indicate monitor without port.

## Reload

Same syntax as `wallpaper` keyword. Unload current wallpaper and preload/display the given image, `reload = [monitor], [img_path]`.

## IPC

`hyprctl hyprpaper [dispatcher] [args]`

### References

- [Hyperpaper Wiki](https://wiki.hyprland.org/Hypr-Ecosystem/hyprpaper/)
