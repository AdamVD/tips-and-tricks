# Linux Shell Commands

### checkinstall
**The issue:** Some applications/libraries that you `make` from source do not contain "uninstall" targets. You would need to manually remove the installed files from your system.

**Solution:** Use the tool `checkinstall`, which keeps track of installed files via `make` or another tool and builds a package out of it. The package may then be used for uninstall purposes. _These packages aren't meant for distribution purposes._

**Example: Installing Python**
```
sudo ./configure --enable-optimizations --with-lto  # configure Python as normal
sudo checkinstall -D --fstrans=no make altinstall   # prepend make commands with checkinstall

sudo dpkg -r python_3.8.2-1_amd64.deb               # remove python from /usr/local
sudo dpkg -i python_3.8.2-1_amd64.deb               # reinstall python to /usr/local
```
