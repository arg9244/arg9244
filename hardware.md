# Hardware

## OS

| Field | Value |
|---|---|
| **Distribution** | CachyOS Linux (Arch-based, rolling) |
| **Kernel** | `7.1.8-1-cachyos` — PREEMPT_DYNAMIC |
| **Compiler** | clang 22.1.8 / LLD 22.1.8 |
| **Display Server** | Wayland |
| **Compositor** | niri |

---

## CPU

| Field | Value |
|---|---|
| **Model** | AMD Ryzen 5 3600 |
| **Architecture** | Zen 2 (Matisse, 2019) |
| **Cores / Threads** | 6C / 12T |
| **Base / Boost Clock** | 3.6 GHz / 4.2 GHz |
| **L1d / L1i** | 192 KiB each (6 instances) |
| **L2** | 3 MiB (6 instances) |
| **L3** | 32 MiB (2 instances) |
| **SMT** | Enabled |
| **Virtualization** | AMD-V (SVM) |
| **Microcode** | 0x8701035 |
| **Freq. driver / governor** | amd-pstate-epp (active) / powersave |

---

## Memory

| Field | Value |
|---|---|
| **Total RAM** | 32 GiB |
| **Type** | DDR4-2666 (2× 16 GiB, single-rank, Kingston KD4AGUA80-26N1900) |
| **Channels** | Dual (CH A + CH B populated); JEDEC 2666 — no XMP/EXPO profile, at rated speed |
| **Swap** | 32 GiB zram (zstd compression) |
| **Swappiness** | 150 |
| **VM overcommit** | 0 (heuristic), ratio 50% |
| **Dirty ratios** | 10 / 5 |

---

## GPU

| Field | Value |
|---|---|
| **GPU** | AMD Radeon RX 6800 (Navi 21, rev c3) |
| **VRAM** | 16 GB GDDR6 |
| **Kernel Driver** | amdgpu |
| **Vulkan Driver** | RADV (Mesa 3:26.1.6) |
| **Vulkan Version** | 1.4.354 |
| **GPU Power Level** | auto |
| **SCLK Range** | 500 MHz (idle) → 2475 MHz (boost) |
| **MCLK Range** | 96 MHz (idle) → 1000 MHz (boost) |
| **FCLK Range** | 417 MHz (idle) → 1200 MHz (boost) |

---

## Platform

| Field | Value |
|---|---|
| **Motherboard** | Gigabyte A320M-S2H |
| **Chipset** | AMD A320 (AM4, DDR4) — chipset I/O lanes Gen3 |
| **BIOS** | F59a (AMI) |
| **GPU slot** | PCIe Gen4 ×16 active (16.0 GT/s ×16, CPU-attached) |
| **ReBAR** | Enabled — BAR 0 resized to full 16 GiB (lspci: current 16 GB / max 16 GB) |

---

## Storage

| Device | Size | Type | Notes |
|---|---|---|---|
| `nvme0n1` | 931.5 GiB | Samsung SSD 980 NVMe | — |
| `sda` | 223.6 GiB | Kingston SA400 SATA | Root `/` on `sda2`, `/boot` on `sda1` |
| `zram0` | 31.3 GiB | zstd compressed swap | Active |

---

## Display

| Field | Value |
|---|---|
| **Monitor** | Samsung LS32CG51x (VA) |
| **Resolution** | 2560×1440 |
| **Refresh** | 165 Hz (current, preferred); VRR supported but disabled |
| **Connector** | DP-2 (EDID: serial H9JWA00258) |
