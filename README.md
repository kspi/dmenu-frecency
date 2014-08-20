# dmenu-frecency

A dmenu-based desktop application launcher that uses a combination of frequency
and recency to sort the application list. This is similar to the way Firefox
sorts its location bar suggestions.

Applications that haven't been launched yet are sorted by modification date, so
the newest ones are at the top.

If no application title matches the input, it it executed as a shell command
(and saved for later suggestions).

It scans XDG desktop files and optionally executables from PATH (off by default).

![Screenshot](http://i.imgur.com/UqwtAGL.png)

## Requirements

Python, pyxdg, docopt and dmenu.

## Configuration

On first launch a `config.json` is saved in `~/.config/dmenu-frecency` (or
wherever `XDG_CONFIG_PATH` is) where dmenu's command line and some other
options can be customized. The command line arguments are specified as a JSON
array, for example `["-i", "-b"]`. The application cache is updated every
`cache-days` or if `--read-apps` is passed on the command line.

PATH scanning can by activated with the "scan-path" option.
