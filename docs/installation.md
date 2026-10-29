# Installation and setup notes

This page records the general direction of the setup. It is not a complete, verified, step-by-step Chromebook conversion guide yet. I will add exact steps as I confirm them against my own device.

## Current state

- Linux Mint is installed and running on the Acer Chromebook 315.
- The desktop uses i3 rather than a full traditional desktop environment.
- The system has been updated, and an older kernel is being kept as a fallback.
- The desktop has been customized with Polybar, Rofi, Kitty, Picom, wallpapers, and hot-pink accents.

## Before changing the system

1. Back up files you care about.
2. Make sure you understand how to recover or reinstall the operating system if a change fails.
3. Keep a known-working kernel or configuration available when possible.
4. Change one thing at a time and test it before making more changes.
5. Check the exact Chromebook model and firmware situation before following instructions written for a different model.

Chromebook boot and firmware procedures can differ by model and device state. Do not assume a guide for another Chromebook applies to this one.

## Desktop configuration locations

The main configuration files used in this setup are under the home directory:

- i3: ~/.config/i3/config
- Polybar: ~/.config/polybar/config.ini
- Picom: ~/.config/picom/picom.conf
- Kitty: ~/.config/kitty/kitty.conf
- Rofi: ~/.config/rofi/

Some helper scripts are stored in ~/.local/bin/. The exact configuration files and scripts have not all been published here yet. They should be reviewed for private information and tested before being added.

## Useful i3 checks

Check the i3 configuration for syntax errors:

    i3 -C -c ~/.config/i3/config

If the check succeeds, reload the current i3 configuration:

    i3-msg reload

Back up a configuration before editing it. Do not copy commands blindly if you are unsure what they do.
