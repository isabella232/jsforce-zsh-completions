# JSforce Zsh Completion functions

Completion functions in [Zsh](http://www.zsh.org) for [JSforce](https://jsforce.github.io) CLI and its [metadata tools](https://github.com/jsforce/jsforce-metadata-tools).

## Installation

* Clone the repository:

        git clone git://github.com/jsforce/jsforce-zsh-completions.git

* Include the directory in your `$fpath`, for example by adding in `~/.zshrc`:

        fpath=(path/to/jsforce-zsh-completions/functions $fpath)

* You may have to force rebuild `zcompdump`:

        rm -f ~/.zcompdump; compinit

## Feature

- Complete all options available in CLI
- For `--c, --connection` option argument, complete candidates from registered connections established in former OAuth2 authorization flow, reading JSforce config file (`.jsforce/config.json`).

```
$ jsforce --connection admin@a
 -- connections --
admin@aaa.example.com                          admin@abb.example.org
admin@abc.example.net                          admin@abcd.example.org
```
