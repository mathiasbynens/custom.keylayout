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

1. Copy the `.keylayout` file to the `Keyboard Layouts` folder within `~/Library` or `/Library`. In command form:

```bash
# Install the keyboard layout only for the current user
cd ~/Library/Keyboard\ Layouts; curl -O# https://raw.github.com/mathiasbynens/custom.keylayout/master/azerty/azerty.keylayout
```

…or…

```bash
# Install the keyboard layout system-wide
cd /Library/Keyboard\ Layouts; sudo curl -O# https://raw.github.com/mathiasbynens/custom.keylayout/master/azerty/azerty.keylayout
```

2. Reboot, or log out and log in again.

3. Enable the new keyboard layout via _System Preferences_ › _Language & Text_ › _Input Sources_ › _AZERTY_.

## How to remove the default OS X keyboard layout from the Input menu

You can remove any default OS X keyboard layout (that you won’t be using anymore) from the Input menu [as follows](http://apple.stackexchange.com/a/60521/4408):

1. Go to _System Preferences_ → _Language & Text_ → _Input Sources_ and enable the _Afghan Dari_ keyboard layout (i.e. the first one in the list).

2. Run the following command:

    ```bash
plist=~/Library/Preferences/ByHost/com.apple.HIToolbox*.plist; curl -# https://raw.github.com/mathiasbynens/custom.keylayout/master/azerty/tmp.plist > $plist
```

3. Log out of your OS X account, then log back in.

4. Run the following command:

    ```bash
plist=~/Library/Preferences/ByHost/com.apple.HIToolbox*.plist; /usr/libexec/PlistBuddy -c "Delete :AppleEnabledInputSources:1 dict" $plist
```

5. Log out of your OS X account, then log back in.

## How to make a custom keyboard layout the system default

Optionally, you could [make the custom keyboard layout the system default](http://apple.stackexchange.com/a/44916/4408) by running the Setup Assistant with root privileges. This way, it will be used for the login screen, and any new user accounts you create will default to this layout as well. Note that this can only be done for keyboard layouts in `/Library/Keyboard Layouts`.

```bash
sudo rm /var/db/.AppleSetupDone; sudo "/System/Library/CoreServices/Setup Assistant.app/Contents/MacOS/Setup Assistant"
```

As of OS X 10.8, you will have to create a new user account in order to complete the Setup Assistant — but don’t worry, you can delete the new account afterwards.

## Notes

Note that I used ‘French Numerical’ instead of the ‘Belgian’ keyboard layout because the only difference between those two is that [the French Numerical layout allows you to type numbers without pressing `Shift` (by enabling `Caps Lock`)](http://superuser.com/q/138420/3218).

I’ve only overwritten key combinations that inserted characters that can be inserted by another, easier and more intuitive key combination. For example, to type `ê`, you can either press `^` followed by `E`, or `⌥` + `E`. I’d consider the last one to be obsolete.

OS X has supported `.keylayout` files since version 10.2 (Jaguar).

## Credits

Created using [Ukelele.app](http://scripts.sil.org/ukelele).

## Author

| [![twitter/mathias](http://gravatar.com/avatar/24e08a9ea84deb17ae121074d0f17125?s=70)](http://twitter.com/mathias "Follow @mathias on Twitter") |
|---|
| [Mathias Bynens](http://mathiasbynens.be/) |

## License

This keyboard layout is available under the [MIT](http://mths.be/mit) license.
