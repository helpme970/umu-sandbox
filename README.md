# umu-sandbox
This allows you to run Windows Apps via umu inside a sandbox (via bwrap).

## Usage
1. Download umu-sandbox
2. Download bubblejail from [here](https://github.com/helpme970/bubblejail)
3. Download the umu zipapp from [here](https://github.com/Open-Wine-Components/umu-launcher/releases) and extract it
4. put both files and the umu folder in the same folder
5. launch umu-sandbox, e.g. `WINEPREFIX="example" bash umu-sandbox --net example.exe`

## command line arguments
umu-sandbox [options] executable.exe

```
--net                         grant access to internet
--no-audio | --disable-audio  self explaining
--xdg-runtime-dir             grant access to $XDG_RUNTIME_DIR (some games crash without this option)
--devices                     grant access to all devices
--usb                         grant access to all usb media drives
--ro-usb                      same as --usb but read-only
--no-fsync                    disable fsync in proton
--log                         enable logging
--video <socket>              share a specific socket to the program
--chdir <dir>                 execute the EXE in a specific directory
--input                       needed for controllers etc.
--noseccomp                   may improve cpu performance by opening an escape from the sandbox
--home <dir>                  directory where the sandbox is located
```
