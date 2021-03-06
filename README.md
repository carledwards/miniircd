miniircd -- A (very) simple Internet Relay Chat (IRC) server
============================================================

Carl's Changes
--------------

Added support by allowing an IRC client to communicate to one or more serial boards
(e.g. Pinnocio http://pinocc.io) at the same time.

To use this, open up the serial port by specifying it as the channel name 
(e.g. #/dev/tty.usbmodem14111).  This will open up a local serial on the machine 
running the miniircd.  All chats are directed to the serial port and 
responses are automatically written back by a serial-port user.

The baked-in serial port parameters are 115200,8,N,1.

Description
-----------

miniircd is a small and limited IRC server written in Python. Despite its size,
it is a functional alternative to a full-blown ircd for private or internal
use. Installation is simple; no configuration is required.

Features
--------

* Knows about the basic IRC protocol and commands.
* Easy installation.
* Basic SSL support.
* No configuration.
* No ident lookup (so that people behind firewalls that filter the ident port
  without sending NACK can connect without long timeouts).

Limitations
-----------

* Can't connect to other IRC servers.
* Only knows the most basic IRC commands.
* No IRC operators.
* No channel operators.
* No user or channel modes except channel key.
* No reverse DNS lookup.
* No other mechanism to reject clients than requiring a password.

Requirements
------------

Python 2.5 or newer, Python 2.6 or newer when SSL is used.
Get it at http://www.python.org.

Installation
------------

None. Just run "./miniircd --help" (or "python miniircd --help") to get some
help.

License
-------

GNU General Public License version 2 or later.

Primary author
--------------

Joel Rosdahl <joel@rosdahl.net>

Contributors
------------

Alex Wright
Leandro Lucarella
Matt Behrens
