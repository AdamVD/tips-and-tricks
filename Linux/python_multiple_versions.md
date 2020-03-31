# Managing Multiple Versions of Python

Problem: Programs like Python are installed with our OS, but changing or upgrading these pre-installed software packages can break the system.

See this solution for exact directions: https://hackersandslackers.com/multiple-versions-python-ubuntu/

Generally:
- Ensure you don't install in `/usr`, instead use `/usr/local` or `/opt/local`
  - _Theoretically_, every system function that relies on Python should directly call the ones in `/usr/bin/`, so you will not break your system
- Use `update-alternatives` as a tool to switch between the versions of Python referenced by the `python` command
  - This manages the `python` simlink in `/usr/bin`
  - Alternatively, don't keep a `/usr/bin/python` link, instead only directly use specific versions, e.g., `python3.8`
