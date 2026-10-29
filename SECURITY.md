# Security and privacy notes

This repository documents a personal device and its configuration. Before publishing commands, logs, screenshots, or configuration files, check them for information that should not be public.

## Check before committing

Look for and remove anything that could expose:

- Passwords, API keys, tokens, private keys, or recovery codes
- Wi-Fi names or passwords
- Public or private IP addresses and network details
- MAC addresses, serial numbers, device IDs, or account IDs
- Personal email addresses or other private account information
- Usernames, home-directory paths, or filenames that reveal private information
- Browser data, private messages, or unrelated personal files

Review screenshots too. Sensitive details can appear in terminal output, browser tabs, notifications, file managers, or wallpaper images.

## Configuration safety

Read scripts and configuration changes before running them. Back up working files before replacing them. Do not run commands with elevated privileges unless you understand what they change.

If a secret is accidentally committed, deleting it from the latest version may not remove it from the repository's history. Revoke or rotate the exposed secret first, then clean up the repository history if needed.

This project is for documenting my own Linux setup and learning process. It is not a security audit or a guarantee that every configuration is suitable for every device.
