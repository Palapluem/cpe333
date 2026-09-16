# PS05 experiment notes

Record actual output here while running the experiments. Keep screenshots in
`ps05/results/`. Do not invent values – copy the output from the selected Linux
and Windows systems exactly.

## Environment

### Linux

- Distribution and release:
- Kernel and architecture (`uname -a`):
- `free --version`:
- `vmstat --version`:
- Screenshot: `00_environment.png`

### Windows

- Windows edition and version:
- Architecture:
- Resource Monitor version or build, if shown:

## Part 1 – virtual memory comparison

### Linux

- Virtual-address-space model:
- Page tables and page faults:
- Demand paging:
- Swap areas/files:
- Other relevant mechanisms:

### Windows

- Virtual-address-space model:
- Page tables and page faults:
- Working sets and commit:
- Pagefile:
- Other relevant mechanisms:

### Comparison

- Similarities:
- Differences:
- Sources used:

## Part 1 – swap-space experiment

Use a dedicated temporary swap file, if possible. Record its path and size.
Do not disable an existing system swap area unless the instructor explicitly
requires it.

- Swap state before the experiment (`swapon --show`):
- Memory and swap before (`free -h`):
- Temporary swap file path:
- Temporary swap file size:
- `mkswap` output:
- Swap state after increase:
- Memory and swap after increase:
- Swap state after decrease:
- Memory and swap after cleanup:
- Screenshots: `01_swap_before.png`, `02_swap_create.png`,
  `03_swap_after_increase.png`, `04_swap_after_decrease.png`
- Did the reported total swap change as expected?
- Why is sufficient free memory needed before `swapoff`?

## Part 2 – `free`

Commands run:

```text
$ free
<paste exact output here>

$ free -h
<paste exact output here, if used>
```

- Units shown by the command:
- `Mem` total:
- `Mem` used:
- `Mem` free:
- `Mem` shared:
- `Mem` buff/cache:
- `Mem` available:
- `Swap` total:
- `Swap` used:
- `Swap` free:
- Explanation of every heading:
- Paragraph summarizing all numerical values:
- Screenshot: `05_free.png`

### `free` help and selected arguments

```text
$ free --help
<paste relevant help here>

$ <sample command 1>
<paste exact output here>

$ <sample command 2>
<paste exact output here>
```

- Argument 1 and what it does:
- Argument 2 and what it does:
- Explanation of both sample outputs:
- Screenshot: `06_free_arguments.png`

## Part 2 – `vmstat`

Commands run:

```text
$ vmstat
<paste exact output here>

$ vmstat 1 5
<paste exact output here, if used>
```

- Meaning of the `procs` columns:
- Meaning of the `memory` columns:
- Meaning of the `swap` columns:
- Meaning of the `io` columns:
- Meaning of the `system` columns:
- Meaning of the `cpu` columns:
- Which row is the since-boot average?
- What changed between interval samples?
- Paragraph summarizing all numerical values:
- Screenshot: `07_vmstat.png`

### `vmstat` help and selected arguments

```text
$ vmstat --help
<paste relevant help here>

$ <sample command 1>
<paste exact output here>

$ <sample command 2>
<paste exact output here>
```

- Argument 1 and what it does:
- Argument 2 and what it does:
- Explanation of both sample outputs:
- Screenshot: `08_vmstat_arguments.png`

## Part 3 – Windows Resource Monitor

- How Resource Monitor was opened:
- Screenshot: `09_windows_resource_monitor.png`
- Information shown in the Memory tab:
- Meaning of the physical-memory graph categories:
- Process columns and their meanings:
- All numerical values in the **Physical Memory** section:
- Paragraph summarizing those values:
- Linux and Windows monitoring comparison:

## Evidence checklist

- [ ] `00_environment.png`
- [ ] `01_swap_before.png`
- [ ] `02_swap_create.png`
- [ ] `03_swap_after_increase.png`
- [ ] `04_swap_after_decrease.png`
- [ ] `05_free.png`
- [ ] `06_free_arguments.png`
- [ ] `07_vmstat.png`
- [ ] `08_vmstat_arguments.png`
- [ ] `09_windows_resource_monitor.png`

Every screenshot should show the command or application title, the full
relevant output, and enough system context to identify the experiment.
