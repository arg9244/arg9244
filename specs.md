# System Specs

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

## Gaming Stack

| Component | Version |
|---|---|
| **Mesa** | 26.1.6 (RADV Vulkan + OpenGL) |
| **VKD3D-Pro** | 3.0.1.r260.g731c4aae-1 |
| **Gamescope** | 3.16.25 |
| **MangoHud** | 0.8.4 |
| **Proton-CachyOS** | 11.0.20260703 |
| **protontricks** | 1.14.1 |
| **lib32-mesa** | 26.1.6 |
| **lib32-vulkan-radeon** | 26.1.6 |
| **lib32-vkd3d** | 1.19 |
| **lib32-sdl2 / sdl3** | 2.32.70 / 3.4.14 |
| **lib32-openal** | 1.25.2 |
| **lib32-opencl-mesa** | 3:26.1.6 |
| **xf86-video-amdgpu** | 25.0.0 |

---

## Kernel Tuning

| Parameter | Value |
|---|---|
| `vm.swappiness` | 150 |
| `vm.overcommit_memory` | 0 (heuristic — kernel default) |
| `vm.overcommit_ratio` | 50 (default; only used in mode 2) |
| `vm.dirty_ratio` | 10 |
| `vm.dirty_background_ratio` | 5 |
| `vm.dirty_bytes` | 0 (cleared — ratio form takes precedence) |
| `vm.dirty_background_bytes` | 0 (cleared) |
| `vm.dirty_writeback_centisecs` | 1500 |
| `vm.dirty_expire_centisecs` | 3000 (default) |
| `vm.page-cluster` | 0 |
| `vm.vfs_cache_pressure` | 50 |
| `kernel.perf_event_paranoid` | 2 (default) |
| `kernel.nmi_watchdog` | 0 |
| `kernel.split_lock_mitigate` | 0 |
| `kernel.printk` | 3 3 3 3 |

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
