### History of Firmware Updates

Check [TP-Link's Product Site](http://www.tp-link.us/support/download/?model=TL-SG3210&version=V1#tbl_j) for new versions.

 Name                 | Publish Date | Version
----------------------|--------------|----------
TL-SG3210_V1_121114   | 2012-11-14   | 1.9.0 Build 20121114 Rel.55704
TL-SG3210_V1_20120510 | 2012-05-10   | ?
TL-SG3210_V1_20120206 | 2012-03-05   | 1.8.2 Build 20120206 Rel.77891

* **TL-SG3210_V1_121114**  
  2012-11-14  
  Modifications and Bug Fixes:
  * Added "lookback detection" feature.
  * Optimized CLI comand and added some new comands, such as "show running-config" etc. More detailed information, please read the new CLI guide.
  * Changed the saved config file format, the config-file of the new firmware can be edited by the text editing tools. It can be edited, and then restored.
  * Changed the multicast filter entry from 5 to 15.
  * Optimized the "DHCP snooping option 82" featrue.
  * Notes: As we have changed the saved config file format, then the config file of the old firmware cannot be restored to the new firmware. So once upgraded to the new firmware, you need to configure the switch manually.
* **TL-SG3210_V1_20120510**  
  2012-05-10
  Modifications and Bug Fixes:
  * Improved the multicast feature performance.
* **TL-SG3210_V1_20120206**  
  2012-03-05  
  Modifications and Bug Fixes:
  * Fixed the bug that the SFP port cannot forward multicast streams when LAG and multicast feature configured;
  * Fixed the bug that the linked SFP port cannot be added to the static LAG group;
  * Fixed the bug that the 256th static multicast IP cannot be added effectively;
  * Fixed the bug that the IGMP Group-Specific Query packet cannot be forwarded.

#### Comments and Warnings

In *TL-SG3210_V1_121114* (2012-11-14) the whole CLI interface has changed and is mostly not compatible to previous versions!