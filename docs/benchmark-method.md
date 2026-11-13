# Chromebook performance testing method

My goal with this project is to compare changes on the same low-spec machine without guessing whether an optimization helped.

This page describes a repeatable test plan. **It does not contain benchmark results.**

## Before each test

- Keep the same power state, background apps, and number of browser tabs.
- Wait for startup activity to settle.
- Record the Linux version and desktop environment.
- Test one change at a time.
- Repeat each test several times and record the results.

## Basic commands

These commands show CPU, memory, uptime, and disk-space information:

```bash
free -h
uptime
df -h /
```

To see approximate system load over a short period:

```bash
vmstat 1 5
```

If `vmstat` is unavailable, it may require the `procps` package.

Check output carefully before sharing it; system reports sometimes contain identifying details.

## Suggested tests

| Test | What to compare |
| --- | --- |
| Idle desktop | Memory used after startup activity settles |
| Browser workload | Memory and responsiveness with the same tabs |
| Application launch | Time needed to open the same application |
| Window management | Responsiveness when switching windows |
| Background services | Difference after enabling or disabling one service |

## Results template

| Date | Test | Before | After | Repetitions | Notes |
| --- | --- | --- | --- | --- | --- |
| YYYY-MM-DD | Example: idle memory | Not measured | Not measured | 0 | Fill in after testing |

Keep original measurements and note unexpected results. Do not claim a percentage improvement until the tests have actually been run under comparable conditions.

## Safety

Avoid stress-testing a machine when cooling, power, or storage behavior is uncertain. Back up important data before changing system services or boot settings. Keep private network information, unique identifiers, and logs out of public commits.

Related notes: [performance.md](performance.md) and [SECURITY.md](../SECURITY.md).
