# CPU Benchmark for OpenWrt Devices
This script benchmarks CPU performance on OpenWrt devices using stress-ng.

It measures **Bogo Ops/s** for **int128** and **matrixprod** methods on both single-thread and multi-thread execution.

The results are printed as a Markdown-formatted table row, ready to be copied into the table below.  
Feel free to submit a pull request with benchmark results from your device.

## Run
> [!NOTE]
> Tested only OpenWrt

```
sh <(wget -O - https://raw.githubusercontent.com/itdoginfo/cpu-wrt-bench/refs/heads/main/cpu-wrt-bench.sh)
```

## Device Results
| Device                  | CPU             | OpenWrt Version |  CPU Threads | int128 (1 Thread) | matrixprod (1 Thread) | int128 (ALL Threads) | matrixprod (ALL Threads) |
|-------------------------|-----------------|-----------------|--------------|----------------|---------------------|-------------------|------------------------|
| Beeline SmartBox TURBO+ | MediaTek MT7621A | OpenWrt 24.10.1 | 4            | n/s            | 8.13                | n/s               | 17.81                  |
| Xiaomi Mi Router AX3000T | MediaTek MT7981BA | OpenWrt 24.10.1 | 2            | 282.87         | 10.71               | 562.66            | 19.05                  |
| FriendlyElec NanoPi R2S | Rockchip RK3328 | OpenWrt 24.10.1 | 4            | 298.83         | 10.49               | 1185.91           | 34.99                  |
| Xiaomi Redmi Router AX6000 | MediaTek MT7986A | OpenWrt 24.10.1 | 4            | 436.07         | 18.79               | 1743.46           | 54.70                  |

> [!NOTE]
> n/s - CPU not supported int128 method.
