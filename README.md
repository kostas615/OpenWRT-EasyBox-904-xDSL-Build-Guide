# OpenWRT EasyBox 904 xDSL Guide

## Installing LEDE

### Required files:

1.  <a href="https://mega.nz/#!DBVCmZAB!8pLr-vmOcSTwJ8Szr-J32LRNLfZYJCH8tjaDGSnwIv8">fullimage.img</a>
  (md5sum: 7d8065859222511a9cdebb17b44038a8)<br>
2.  <a href="https://mega.nz/#!vIEiQThY!YwYEYCsxyr1f3EEMh9dlMO2__wzGv5x-YfrWvVZwz7E">sysupgrade.bin</a>
  (md5sum: abc4c14ea9ef35ff33be027b434a2a27)

### Steps:

1.  Prepare TFTP server (e.g. <a href="https://bitbucket.org/phjounin/tftpd64/downloads/tftpd64.460.zip">TFTPD32</a>) by putting <b>fullimage.img</b> in server directory.<br>
  a.  Image must have name "fullimage.img"
2.  Connect device to computer with one of four LAN ports, and set your computer's static ip to <b>192.168.2.100</b>.
3.  Turn on device with reset button pressed for at least 8 seconds.<br>
  a.  LCD will show information about recovery mode selected.<br>
  b.  If you have serial cable connected, you can depress button when countdown starts
4.  Box will download and flash image. After successfull flash, LCD will show message to shutdown and restart router.
5.  Turn device off and on again.
6.  After some time it will boot to LEDE sysupgrade interface at 192.168.1.1.<br>
  a.  Set your computer's static ip to <b>192.168.1.X</b> (e.g. 192.168.1.100)<br>
  b.  The device's LCD will be stuck in "Der Startvorgang läuft..." mode.
7.  Using this interface, upload <b>sysupgrade.bin</b>
8.  After succesfull flash, router will reboot into full LEDE image.<br>
  a.  You can use the same procedure again from step 1 to flash a new image.<br>
  b.  If you have access into LUCI, you can flash a new image directly from the "Backup/Flash Firmware" Section.
