# dmenu2
####dmenu2 with tab key mod/fix

This repo contains [Michał Lemke's dmenu2](https://bitbucket.org/melek/dmenu2) (which is a fork of [dmenu](http://tools.suckless.org/dmenu/)) with a slight modification:

I modded the **TAB** key's and the **Shift+TAB** key's behaviour to work like the down and the up arrow keys (select next and previous items in the list).
**UPDATED (2017/08/17):** 'copy selected item to the input field' is now bound to Up/Down arrow keys (it was originally bound to the TAB key).

#####Why is this mod/fix?

Originally when you reached the last element of the displayed list the highlighting stopped working and it didn't show the next set of elements (as a list, like when you are using the arrow keys, or Pg Up/Pg Dn).

In this repository you can find:

* the modded/fixed dmenu2 archive (**dmenu2-0.2.tar.gz**)
* the **PKGBUILD** for Arch Linux
* **dmenu.c.diff**, which you don't really need, but you can use it, if you want to patch the original package for yourself.

### Installation for Arch Linux

Clone this repository, change to the cloned directory, then run the `makepkg` command (or `makepkg -s` if you have missing dependencies).

Then run `sudo pacman -U /path/to/package` to install the package.

Or you can use the `makepkg -si` command to build & install automatically.
