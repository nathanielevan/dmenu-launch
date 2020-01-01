# dmenu-launch

Simple and customizable dmenu launcher for quicly accessing gpg encrypted passwords with `pass`, application shortcuts, notes and documents in general.

## Requirements

Following utils are required:

- [dmenu](https://tools.suckless.org/dmenu/)
- [gpg](https://gnupg.org/)
- [pass](https://www.passwordstore.org/)
- [xclip](https://github.com/astrand/xclip)
- [exo-open](http://manpages.ubuntu.com/manpages/bionic/man1/exo-open.1.html)

## Usage

```properties
usage: dmenu-launch.py [-h] [--pass | --apps | --notes | --search]

Simple dmenu launcher for passwords, docs, notes and application shortcuts.

optional arguments:
  -h, --help  show this help message and exit
  --pass      Copy password from password store.
  --apps      Quick launches a desktop application with exo-open.
  --notes     Opens a text/markdown note from a given directory with exo-open.
  --search    Quick search and launch from a given directory with exo-open.
```

## (Optional) OpenBox Keybindings

OpenBox users just need to add the following to `~/.config/openbox/rc.xml` for the suggested keybindings:

```xml
   <keybind key="W-A">
    <action name="Execute">
      <command>/usr/bin/dmenu-launch --pass</command>
    </action>
   </keybind>
   <keybind key="W-Q">
    <action name="Execute">
      <command>/usr/bin/dmenu-launch --notes</command>
    </action>
   </keybind>
   <keybind key="W-O">
    <action name="Execute">
      <command>/usr/bin/dmenu-launch --apps</command>
    </action>
   </keybind>
   <keybind key="W-F">
    <action name="Execute">
      <command>/usr/bin/dmenu-launch --search</command>
    </action>
   </keybind>
```

## Contact

Create an [issue](https://github.com/fsilveir/dmenu-launch/issues) if you want to report a problem or ask for a new functionality any feedback is highly appreciated.
