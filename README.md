[![Workflow Status](https://img.shields.io/github/workflow/status/usecallmanagernz/commands/python%20lint/master?label=python%20lint)](https://github.com/usecallmanagernz/commands/actions/workflows/pylint.yml) [![Version](https://img.shields.io/github/v/tag/usecallmanagernz/commands?color=blue&label=version&sort=semver)](https://github.com/usecallmanagernz/commands/releases) [![Licence](https://img.shields.io/github/license/usecallmanagernz/commands?color=red)](LICENSE)

# Command Line Utilities

This respository contains a set of command line utilities that 
can be used to query or remotely control a Cisco IP Phone.

* `cgiexecute` - Execute a URI on the phone (eg: Dial:).
* `mediastream` - Play a .wav file on one or more phones at the same time.
* `screenshot` - Download a screenshot of the phones screen.
* `setbackground` - Set the background image on the phone.
* `setringtone` - Set the ring-tone on the phone.
* `xmlinfo` - Get call, line or settings information from phone as XML.

## Requirements

The following non-standard Python modules are required: `requests` and `lxml`.

You can use the packages provided by your OS distribution or run
`sudo pip3 install -r requirements.txt` to satisfy those dependancies.

To use `mediastream` you will need to also install GStreamer and the Glib
object bindings. Installation is OS dependant, the following example shows how
to install those packages on Debian/Ubuntu:

```sh
sudo apt install python3-gi python3-gst-1.0 \
  libgstreamer-plugins-good-1.0 libgstreamer-plugins-bad-1.0
```

## Installation

```
sudo cp cgiexecute mediastream setbackground setringtone \
  screenshot xmlinfo /usr/local/bin
```

Optionally, install the bash tab-completion helpers.

```
sudo cp bash_completion /etc/bash_completion.d/usecallmanagernz-commands
```
