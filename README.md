# bluetooth
Add support to bluetooth on 0489:e0e4 Foxconn / Hon Hai Wireless_Device. 

master branch based on linux kernel 6.3
kernel6.2 - based on linux kernel 6.1.7

# Usage

Clone repo and run following commands:

```
make
sudo rmmod btusb
sudo insmod ./btusb
```

From time to time this sequence results in following error:

```
Bluetooth: hci0: Failed to get fw version (-108)
Bluetooth: hci0: HCI Enhanced Setup Synchronous Connection command is advertised, but not supported.
```

If it happens - try to repeat rmmod and insmod sequence. It sometimes takes about 10 runs to successfully bring up bluetooth.

Also possible thing - restart bluetooth device. Sometimes it helps.

Here is short code snippet for this:

`sudo usb_modeswitch -R -v 0489 -p e0e4`



