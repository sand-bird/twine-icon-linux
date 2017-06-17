# twine-icon-mint-y

A set of Linux desktop icons for [Twine](http://twinery.org) in the style of the [Mint-Y](https://github.com/linuxmint/mint-y-icons) and [Moka](https://github.com/snwh/moka-icon-theme) icon themes (they are pretty much the same thing).


### Installation

1. Clone this repository or download and extract it to a folder
2. Run the following from within the directory: 
```cp -r ./icons/* ~/.local/share/icons/hicolor```
3. That's it! The icon should now show up in the Browse Icons dialog.

Linux keeps icons in [a lot of different places](https://specifications.freedesktop.org/icon-theme-spec/icon-theme-spec-latest.html#directory_layout). I chose `~/.local/share/icons/hicolor` for a couple of reasons:

- acts as part of the hicolor (default) theme, which is specifically for third-party icons
- lives in the home folder, which is a cinch to restore if you ever change, reinstall, or clean-upgrade your OS

Of course, feel free to place them somewhere else if you prefer!


### Editing

The source SVG and Twine logo are included if you want to make any changes. I've also included a slightly modified version of Sam Hewitt's `render-bitmaps.py` from his excellent [Moka theme](https://github.com/snwh/moka-icon-theme). More documentation is available there, but in a nutshell:

1. The script requires **Inkscape** and **python3** to be installed, and will most likely not work if you edit the source SVG with anything other than Inkscape.
2. Make the script executable by running `chmod +x render-bitmaps.py` from within the `twine-icon-mint-y` directory.
3. Run with `./render-bitmaps.py` to render a new set of icons into the `icons` folder. If you have multiple templates in the root directory, it will try to render all of them; use `./render-bitmaps.py twine` (or whatever your file is called) to just do the one.
4. The script also has "filter" options, apparently, but I'm not super clear on what those are. Check Moka's readme for more info.
