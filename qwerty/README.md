# My custom QWERTY `.keylayout` file

This is an edited version of the default ‘US’ QWERTY keyboard layout available on OS X.

The following special characters are now available through key combinations:

* `⌥` + `Y` = `→`
* `⌥` + `⇧` + `Y` = `←`
* `⌥` + `H` = `♥`
* `⌥` + `⇧` + `H` = `♡`
* `⌥` + `⇧` + `2` = `²`
* `⌥` + `⇧` + `3` = `³`
* `⌥` + `⇧` + `5` = `⁵`
* `⌥` + `3` = [U+1D306 tetragram for centre](http://graphemica.com/%F0%9D%8C%86)
* `⌥` + `§` = `※` (reference mark)
* `⌥` + `⇧` + `F` = `·` (`⌥` + `⇧` + `9` works too)
* `⌥` + `⇧` + `X` = `×`
* `⌥` + `⇧` + `C` = `⌘`
* `⌥` + `⇧` + `S` = `⇧`
* `⌥` + `⇧` + `O` = `⌥`
* `⌥` + `⇧` + `M` = `−` (minus sign)
* `⌥` + `⇧` + `=` = `≈`
* `⌥` + `C` = `©` instead of `ç`
* `⌥` + `G` = `ç` instead of `©`
* `⌥` + `O` = `ಠ_ಠ` instead of `ø`
* `⇧` + `⌘` + `V` = `✓` instead of `◊`
* `⇧` + `⌥` + `1` = `‽` instead of `⁄`
* `⇧` + `⌥` + `Space` = zero width space

## How to install

1. Copy the `.keylayout` file to the `Keyboard Layouts` folder within `~/Library` or `/Library`. In command form:

    ```bash
# Install the keyboard layout only for the current user
cd ~/Library/Keyboard\ Layouts; curl -O# https://raw.github.com/mathiasbynens/custom.keylayout/master/qwerty/qwerty.keylayout
```

    …or…

    ```bash
# Install the keyboard layout system-wide
cd /Library/Keyboard\ Layouts; sudo curl -O# https://raw.github.com/mathiasbynens/custom.keylayout/master/qwerty/qwerty.keylayout
```

2. Reboot, or log out and log in again.
3. Enable the new keyboard layout via _System Preferences_ › _Language & Text_ › _Input Sources_ › _QWERTY_.
4. Optionally, you could [make the custom keyboard layout the system default](http://apple.stackexchange.com/a/44916/4408) by running the Setup Assistant with root privileges. This way, it will be used for the login screen, and any new user accounts you create will default to this layout as well. Note that this can only be done for keyboard layouts in `/Library/Keyboard Layouts`.

    ```bash
sudo "/System/Library/CoreServices/Setup Assistant.app/Contents/MacOS/Setup Assistant"
```

## Notes

Mac OS X has supported `.keylayout` files since version 10.2 (Jaguar).

## Credits

Created using [Ukelele.app](http://scripts.sil.org/ukelele).

_– [Mathias](http://mathiasbynens.be/)_