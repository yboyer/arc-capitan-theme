## Arc Capitan
> Fork of [**Arc Theme**](https://github.com/horst3180/arc-theme) by **horst3180**


### Installation
Clone the `theme` branch of the repo into your `~/.themes` directory and activate it with `gnome-tweak-tools` or `unity-tweak-tool`.
```bash
git clone -b theme --single-branch https://github.com/yboyer/arc-capitan '~/.themes/Arc Capitan' --depth 1
```

---

#### Manual Installation

To build the theme the follwing packages are required
* `autoconf`
* `automake`
* `pkg-config`
* `libgtk-3-dev`

**Note:** If your distribution doesn't ship separate development packages you just need GTK 3 instead of the `-dev` packages.

##### 1. Get the source
Clone the git repository with
```bash
git clone https://github.com/yboyer/arc-capitan --depth 1 && cd arc-capitan
```

##### 2. Build and install the theme
```bash
./autogen.sh --prefix=/usr
sudo make install
```

Other options to pass to `autogen.sh` are
```
--disable-transparency     disable transparency in the GTK3 theme
--disable-gtk2             disable GTK2 support
--disable-gtk3             disable GTK3 support
--disable-metacity         disable Metacity support
--disable-unity            disable Unity support

--with-gnome=<version>     build the theme for a specific Gnome version (3.14, 3.16, 3.18, 3.20)
                           Note: Normally the correct version is detected automatically and this
                           option should not be needed.
```

After the installation is complete you can activate the theme with `gnome-tweak-tool` or a similar program by selecting `Arc-Capitan` as Window/GTK+ theme .


## Uninstall
```bash
sudo make uninstall
```


## License
Arc is available under the terms of the GPL-3.0. See [`COPYING`](COPYING) for details.
