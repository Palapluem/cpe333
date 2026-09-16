# CPE333 PS05 – Virtual Memory and VM Monitoring

Problem Session 5 covers virtual memory in Linux and Windows, Linux swap-space
management, Linux VM monitoring with `free` and `vmstat`, and Windows memory
monitoring with Resource Monitor.

## Layout

- `problem-session.md` – assignment requirements.
- `guide.md` – step-by-step experiment and report guide.
- `results/` – screenshots and command-output evidence.
- `notes/` – observations and exact outputs for the report owner.

This lab has no source program or Makefile. It consists of Linux commands,
system configuration observations, and a Windows GUI experiment.

The CPE333 checkout intentionally contains no report files. Keep the report,
PDF, and any report-specific copies of screenshots in the group's separate
submission workspace.

## Platform

Run the Linux sections on Debian, Ubuntu, WSL2, or another Linux system. A
Linux desktop VM is recommended because it makes screenshots easy. Run the
Windows section on Windows, either on a physical machine or in a Windows VM.

macOS is not a substitute for the required Linux commands or Windows Resource
Monitor. macOS has different tools such as `vm_stat`; use Linux and Windows for
the final evidence.

## Linux preparation

On Debian, Ubuntu, or WSL2 Ubuntu:

```bash
sudo apt update
sudo apt install -y procps
```

Check that the required commands are available:

```bash
command -v free
command -v vmstat
command -v swapon
free --version 2>/dev/null || true
vmstat --version 2>/dev/null || true
```

`free`, `vmstat`, and `swapon` may already be installed. Use the package
manager for the selected distribution if any command is missing.

## Windows preparation

Resource Monitor is included with Windows. Open it from PowerShell:

```powershell
resmon
```

Select the **Memory** tab and capture the physical-memory information shown by
the interface.

## Handoff

The person running the experiments should:

1. Record exact commands and outputs in `notes/README.md`.
2. Save screenshots in `results/` using the names in `guide.md`.
3. Give the notes and screenshots to the report owner.
4. Leave generated report files in the separate submission workspace.
