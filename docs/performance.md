# Performance notes

The point of this project is to find out how far I can push this Chromebook, not to pretend that its hardware has no limits. These notes are observations from my setup and may change as I test more things.

## Current observations

- The machine has 4 GB of RAM, with roughly 3.7 GiB visible to Linux.
- Firefox with multiple tabs has used a large share of the available memory in my testing.
- With several tabs open, Firefox has been around 1.3–1.6 GB of memory use at times. This is an observation, not a fixed amount.
- Running extra monitoring tools alongside the browser can add pressure.
- Disk usage was around 17% at one point, so memory has been the more obvious limit in those checks.
- Picom blur is left off to avoid spending resources on an effect that is not essential.
- An older kernel is being kept available as a fallback rather than removing it just to save a little space.

## What I am trying to get out of it

- Keep the desktop responsive for everyday use.
- Avoid unnecessary startup programs and background effects.
- Use lightweight tools where they make a real difference.
- Watch memory use before and after a change.
- Keep a working fallback when changing kernels or important configuration.
- Record problems as well as improvements.

## Basic checks

    free -h
    uptime

If btop is installed, it can help show which processes are using memory and CPU. Do not run lots of monitoring tools at once on a machine with limited RAM.

## How I want to test changes

When testing a tweak, I want to compare the same basic workload before and after the change. For example, use the same browser tabs, wait for startup activity to settle, then compare memory use and how responsive the desktop feels. One test is not enough to prove a change always helps, but it is better than guessing.

I will update this page as I collect more repeatable measurements. I do not want to claim a performance improvement until I have actually observed it.
