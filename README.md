### TP-Link_TL-SG3210_CLI

This project contains a collection of scripts to query a TP-Link TL-SG3210 Gigabit Switch
via its Telnet CLI interface. In addition SSH is now also supported.

The scripts make it easier for you to export the configuration settings of the switch and
save them in a human readable format.

#### Usage

Just run any of the 'expect'-scripts. Expect ships with almost any Linux distro as well as
with Mac OS X.

You could run this for example to gather some network stats:

    ./get-stats 192.168.1.2 admin password enablepassword > switch-stats_$(date +"%Y-%m-%d_%H-%M").log

The log files contain a lot of carriage returns (CR / 0x0D). If you want to remove those
and leave only the newline characters (LF / 0x0A) in the file, run this perl command:

    perl -pi -e 's/\r//;s/\r//' switch-stats_2013-03-02_18-26.log

### Enabling the Telnet / SSH Access

Login via the serial port first to set an administration password.
The default serial connecion parameters are:

* Baud: 38400,
* Data bits: 8
* Parity: none
* Stop bits: 1
* Flow control: none

Once you are connected, enter the following commands:

    enable
    config
    line vty 0 5
    login local
    exit
    enable password yourNewPassword

The line configurations you can set are `login` (a special password has to be set) or `login local` (the username/password) combination are being used.

For more information consult the
[CLI manual](http://www.tp-link.com/resources/document/TL-SG3210_V1_CLI_Guide.pdf).

The above steps have been automized in the scripts `./set-password-serial` and `./remove-password-serial`.
Right now they are only functional on Mac OS X!
Call them like this:

    ./set-password-serial /dev/tty.usbserial-FTGACCA2 yourNewPassword
    ./remove-password-serial /dev/tty.usbserial-FTGACCA2 yourOldPassword

### Author

Philipp Klaus  
[blog.philippklaus.de](http://blog.philippklaus.de)  
Email: philipp.l.klaus → AT → web.de
