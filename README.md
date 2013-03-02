### TP-Link_TL-SG3210_CLI

This project contains a collection of scripts to query a TP-Link TL-SG3210 Gigabit Switch
via its Telnet CLI interface.

The scripts make it easier for you to export the configuration settings of the switch and
save them in a human readable format.

#### Usage

Just run any of the 'expect'-scripts. Expect ships with almost any Linux distro as well as
with Mac OS X.

You could run this for example to gather some network stats:

    ./get-stats 192.168.1.2 admin password > switch-stats_$(date +"%Y-%m-%d_%H-%M").log

The log files contain a lot of carriage returns (CR / 0x0D) If you want to replace those with
newline characters (LF / 0x0A), just run this perl command:

    perl -pi -e 's/\r//;s/\r//' switch-stats_2013-03-02_18-26.log

### Author

Philipp Klaus  
[blog.philippklaus.de](http://blog.philippklaus.de)  
Email: philipp.l.klaus → AT → web.de
