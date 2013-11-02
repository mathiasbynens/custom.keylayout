# My custom QWERTY `.keylayout` file for UK-style keyboards

This is an edited version of the default ‘US’ QWERTY keyboard layout available on OS X for UK-style hardware Apple keyboards. (See [the difference between UK and US QWERTY keyboards made by Apple](http://apple.stackexchange.com/a/106059/4408).)

The following special characters are now available through key combinations:

* `⌥` + `Y` = `→`
* `⌥` + `⇧` + `Y` = `←`
* `⌥` + `H` = `♥`
* `⌥` + `⇧` + `H` = `♡`
* `⌥` + `⇧` + `2` = `²`
* `⌥` + `⇧` + `3` = `³`
* `⌥` + `⇧` + `5` = `⁵`
* `⌥` + `3` = [U+1D306 tetragram for centre](http://codepoints.net/U+1D306)
* `⌥` + `4` = [U+1F4A9 pile of poo](http://codepoints.net/U+1F4A9)
* `⌥` + `§` = `※` (reference mark)
* `⌥` + `⇧` + `F` = `·` (`⌥` + `⇧` + `9` works too)
* `⌥` + `⇧` + `X` = `×`
* `⌥` + `⇧` + `C` = `⌘`
* `⌥` + `⇧` + `S` = `⇧`
* `⌥` + `⇧` + `O` = `⌥`
* `⌥` + `⇧` + `R` → `↪` instead of `‰`
* `⌥` + `⇧` + `M` = `−` (minus sign)
* `⌥` + `⇧` + `=` = `≈`
* `⌥` + `C` = `©` instead of `ç`
* `⌥` + `G` = `ç` instead of `©`
* `⌥` + `O` = `ಠ_ಠ` instead of `ø`
* `⇧` + `⌘` + `V` = `✓` instead of `◊`
* `⇧` + `⌥` + `1` = `‽` instead of `⁄`
* `⇧` + `⌥` + `Space` = zero width space

## How to install

1. Copy the `.keylayout` file to the `Keyboard Layouts` folder within `/Library`. In command form:

```bash
# Install the keyboard layout system-wide
cd /Library/Keyboard\ Layouts; sudo curl -O# https://raw.github.com/mathiasbynens/custom.keylayout/master/uk-qwerty/qwerty.keylayout
```

2. Reboot, or log out and log in again.

3. Enable the new keyboard layout via _System Preferences_ › _Language & Text_ › _Input Sources_ › _QWERTY_.

## How to remove the default OS X keyboard layout from the Input menu

You can remove any default OS X keyboard layout (that you won’t be using anymore) from the Input menu [as follows](http://osxnotes.net/keylayout-files-and-ukelele.html#disabling-other-input-sources):

1. Make sure the current input source is your custom keyboard layout.

2. Open `~/Library/Preferences/com.apple.HIToolbox.plist`. (If needed, you can convert the `plist` to XML by running `plutil -convert xml1`.)

3. Remove the input source or input sources you want to disable from the `AppleEnabledInputSources` dictionary. If there is an `AppleDefaultAsciiInputSource` key, remove it.

4. Reboot.

## Notes

OS X has supported `.keylayout` files since version 10.2 (Jaguar).

## Credits

Created using [Ukelele.app](http://scripts.sil.org/ukelele).

## Author

| [![twitter/mathias](http://gravatar.com/avatar/24e08a9ea84deb17ae121074d0f17125?s=70)](http://twitter.com/mathias "Follow @mathias on Twitter") |
|---|
| [Mathias Bynens](http://mathiasbynens.be/) |

## License

This keyboard layout is available under the [MIT](http://mths.be/mit) license.
