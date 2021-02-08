# Flashing firmware

In the `mdloader` directory:

```sh
$ sudo ./mdloader_mac --first --download <firmware.bin> --restart
```

When `Scanning for device for 60 seconds` appears, put the keyboard in 
DFU (Device Firmware Update) mode by pressing and holding for two seconds
either:

- the default key combo `Fn-b`, assuming it hasn't been overridden, or
- the hardware reset button located under the right edge of the keyboard
  (requires a pin or probe)

# Function keys

Apple bluetooth keyboard:

- Function keys except (blank) F5 & F6 send no keycode unless Fn is pressed,
  but are recognized as media keys etc.
- If Fn is pressed, keys send the appropriate keycodes



