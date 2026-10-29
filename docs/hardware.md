# Hardware

These are the hardware details from the Acer Chromebook 315 I have been configuring. The goal is to understand what the machine can do and where its limits start to show.

## Main specifications

| Part | Details |
| --- | --- |
| Device | Acer Chromebook 315, CB315-4H/4HT family |
| Board name | MAGMA / magma-rev6 |
| Processor | Intel Celeron N4500, 2 cores, up to 2.8 GHz |
| Graphics | Intel UHD integrated graphics |
| RAM | About 3.68 GiB usable, sold/configured as 4 GB |
| Storage | eMMC; Linux root partition is on /dev/mmcblk1p2 |
| Linux storage | Approximately 114 GB for the root filesystem at the time of checking |
| Display | 1920 × 1080 |

Storage figures and available memory can vary depending on partitions, updates, and what is running.

## What these limits mean for the project

The biggest constraint so far is memory. A browser with several tabs can take a large share of the available RAM, and running extra monitoring tools or multiple browser windows can push the system harder. The Celeron processor and integrated graphics also mean this is not a machine for assuming heavy workloads will run smoothly.

That makes the Chromebook useful for experimenting with lightweight Linux tools, window managers, startup services, and careful configuration. It also means changes should be tested one at a time so it is easier to tell what helped or made things worse.

## Things to check after system changes

These commands check local system information and do not intentionally print network addresses.

    lscpu
    free -h
    lsblk -o NAME,SIZE,TYPE,FSTYPE,MOUNTPOINTS
    uname -r

Avoid posting full diagnostic output without checking it first. It can include device identifiers, usernames, mount paths, or other details you may not want public.
