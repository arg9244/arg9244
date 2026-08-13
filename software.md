# Software

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
