# My custom AZERTY `.keylayout` file

This is an edited version of the default ‘French Numerical’ AZERTY keyboard layout available on OS X.

The following special characters are now available through key combinations:

* `⌥` + `i` = `←`
* `⌥` + `⇧` + `i` = `→`
* `⌥` + `H` = `♥`
* `⌥` + `⇧` + `H` = `♡`
* `⌥` + `2` = `²`
* `⌥` + `⇧` + `2` = `³`
* `⌥` + `L` = `λ`
* `⌥` + `⇧` + `@` = `☆`
* `⌥` + `⇧` + `;` = `‥`
* `⌥` + `⇧` + `X` = `×`
* `⌥` + `⇧` + `C` = `⌘`
* `⌥` + `⇧` + `S` = `⇧`
* `⌥` + `⇧` + `O` = `⌥`
* `⌥` + `⇧` + `M` = `−` (minus sign)
* `⌥` + `S` = `∑` (used to be `⌥` + `⇧` + `S`)

## How to install

1. Copy the `.keylayout` file to the `Keyboard Layouts` folder within `/Library`. In command form:

    ```bash
    # Install the keyboard layout system-wide
    cd /Library/Keyboard\ Layouts; sudo curl -O# https://raw.githubusercontent.com/mathiasbynens/custom.keylayout/master/azerty/azerty.keylayout
    ```

2. Reboot, or log out and log in again.

3. Enable the new keyboard layout via _System Preferences_ › _Language & Text_ › _Input Sources_ › _AZERTY_.

## How to make the custom keyboard layout the system default

To use the custom layout for the login screen, you need to [set it as the system default](http://apple.stackexchange.com/a/108836/4408).

1. Run the following command:

    ```bash
    sudo curl -#o /Library/Preferences/com.apple.HIToolbox.plist https://raw.githubusercontent.com/mathiasbynens/custom.keylayout/master/azerty/tmp.plist
    ```

2. Reboot.

## How to remove the default OS X keyboard layout from the Input menu

You can remove any default OS X keyboard layout (that you won’t be using anymore) from the Input menu [as follows](http://osxnotes.net/keylayout-files-and-ukelele.html#disabling-other-input-sources):

1. Make sure the current input source is your custom keyboard layout.

2. Open `~/Library/Preferences/com.apple.HIToolbox.plist`. (If needed, you can convert the `plist` to XML by running `plutil -convert xml1`.)

3. Remove the input source or input sources you want to disable from the `AppleEnabledInputSources` dictionary. If there is an `AppleDefaultAsciiInputSource` key, remove it.

4. Reboot.

## Notes

Note that I used ‘French Numerical’ instead of the ‘Belgian’ keyboard layout because the only difference between those two is that [the French Numerical layout allows you to type numbers without pressing `Shift` (by enabling `Caps Lock`)](http://superuser.com/q/138420/3218).

I’ve only overwritten key combinations that inserted characters that can be inserted by another, easier and more intuitive key combination. For example, to type `ê`, you can either press `^` followed by `E`, or `⌥` + `E`. I’d consider the last one to be obsolete.

OS X has supported `.keylayout` files since version 10.2 (Jaguar).

## Credits

Created using [Ukelele.app](http://scripts.sil.org/ukelele).

## Author

| [![twitter/mathias](https://gravatar.com/avatar/24e08a9ea84deb17ae121074d0f17125?s=70)](https://twitter.com/mathias "Follow @mathias on Twitter") |
|---|
| [Mathias Bynens](http://mathiasbynens.be/) |

## License

This keyboard layout is available under the [MIT](http://mths.be/mit) license.
