# dmenu-frecency

A dmenu-based desktop application launcher that uses a combination of frequency
and recency to sort the application list. This is similar to the way Firefox
sorts its location bar suggestions.

If no application title matches the input, it it executed as a shell command
(and saved for later suggestions).

![Screenshot](http://i.imgur.com/UqwtAGL.png)

## Requirements

Python, pyxdg, docopt and dmenu.

## Configuration

On first launch a `config.json` is saved in `~/.config/dmenu-frecency` (or
wherever `XDG_CONFIG_PATH` is) where dmenu's command line and some other
options can be customized. The application cache is updated every
`cache-days` or if `--read-apps` is passed on the command line.
