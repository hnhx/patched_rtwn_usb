# patched_rtwn_usb

I applied [this](https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=254280) patch and compiled rtwn_usb so my USB N10 Nano rev. B1 wifi dongle can get recognized by the rtwn driver. This is mostly for myself but feel free to use the patched kernel module if you happen to use this wifi dongle.
<br><br>
Just simply download it from the releases and overwrite the old `if_rtwn_usb.ko` kernel module in `/boot/kernel` with it. <br>
Then just load it in via `sudo kldload if_rtwn_usb`, to load it at boot just append `if_rtwn_usb_load="YES"` to `/boot/loader.conf`.
