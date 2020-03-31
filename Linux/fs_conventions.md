# Linux File System
_Trying to make sense of the Linux file system conventions._

## `/opt`
> "a directory for installing unbundled packages (i.e. packages not part of the Operating System distribution, but provided by an independent source) [[jilliagre](https://unix.stackexchange.com/a/11552)]"

Pre-built packages from a third-party.

Should follow the convention:
```
/opt/foo              # install root
/opt/foo/bin/bar      # one of the executable commands
/etc/opt/foo/bar.conf # configuration file
/var/opt/foo/logs/    # log files
```
#### Sources
https://unix.stackexchange.com/a/11552

## `/usr`

### `/usr/local`
> "`/usr/local` is a place to install files built by the administrator, typically by using the `make` command (e.g., `./configure; make; make install`). The idea is to avoid clashes with files that are part of the operating system, which would either be overwritten or overwrite the local ones otherwise (e.g., `/usr/bin/foo` is part of the OS while `/usr/local/bin/foo` is a local alternative)." [[jilliagre](https://unix.stackexchange.com/a/11552)]

> "This is a part where the FHS is slightly self-contradictory, as `/usr` is defined to be read-only, but `/usr/local/bin` needs to be read-write for local installation of software to succeed. The SVR4 file system standard, which was the FHS' main source of inspiration, is recommending to avoid `/usr/local` and use `/opt/local` instead to overcome this issue." [[jilliagre](https://unix.stackexchange.com/a/11552)]

## `/etc`
> "On modern unix systems, almost all system-wide configuration files are under /etc, but not all files in /etc are configuration files." [[Gilles 'SO- stop being evil'](https://unix.stackexchange.com/a/56172)]
