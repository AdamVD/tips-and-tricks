# Managing Multiple Versions of Python

Problem: Programs like Python are installed with our OS, but changing or upgrading these pre-installed software packages can break the system.

~~See this solution for exact directions: https://hackersandslackers.com/multiple-versions-python-ubuntu/~~

**Don't bother trying to manage Python installs manually, instead use `pyenv` whenever possible.**

See `pyenv`[GitHub](https://github.com/pyenv/pyenv) and a helpful [installer](https://github.com/pyenv/pyenv-installer). If on Windows, try using the `pyenv-win` fork - [GitHub](https://github.com/pyenv-win/pyenv-win).

`pyenv` manages Python installations without touching your system directories (doesn't require sudo!). Instead, it installs all binaries and links in your home directory, which you then inlcude in your `PATH` when necessary.

```
$ which python
~/.pyenv/shims/python
$ pyenv versions
  system
* 3.8.2 (set by ~/.pyenv/version)
  3.7.6
  2.7.17
```
