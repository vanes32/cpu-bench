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
| Device                  | OpenWrt Version |  CPU Threads | int128 (1 Thread) | matrixprod (1 Thread) | int128 (ALL Threads) | matrixprod (ALL Threads) |
|-------------------------|-----------------|--------------|----------------|---------------------|-------------------|------------------------|
| FriendlyElec NanoPi R2S | OpenWrt 24.10.1 | 4            | 298.83         | 10.49               | 1185.91           | 34.99                  |
