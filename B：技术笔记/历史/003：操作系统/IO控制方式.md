zQ：什么是I/O控制方式？

A：控制I/O设备与主存（或设备机）之间的数据传送（即外围设备与内存之间的输入/输出控制方式）

---

| I/O控制方式  | 完成一次读/写的过程                                          | CPU干预率 | 每次I/O的数据传输单位 | 数据流向                        | 特点                                                 |
| ------------ | :----------------------------------------------------------- | --------- | --------------------- | ------------------------------- | ---------------------------------------------------- |
| 程序直接控制 | CPU发出 I/O命令之后需要不断轮询                              | 极高      | 字                    | 设备→CPU→内存<br/>内存→CPU→设备 | CPU与I/O设备只能串行工作，且CPU主动发起和轮询        |
| 中断驱动方式 | CPU发出I/O命令后可以做其他事，本次I/O完成后设备控制器发出中断信号 | 高        | 字                    | 设备→CPU→内存<br/>内存→CPU→设备 | 允许I/O设备主动打断CPU的运行并请求服务               |
| DMA方式      | CPU发出I/O命令后可以做其他事，本次I/O完成后DMA控制器发出控制信号 | 中        | 块                    | 设备→内存<br/>内存→设备         | 在I/O设备与内存之间开辟直接的数据交换通路（解放CPU） |
| 通道控制方式 | CPU发出I/O命令后可以做其他事，通道会执行通道程序以完成I/O，I/O完成后通道向CPU发出控制信号 | 低        | 一组块                | 设备→内存<br/>内存→设备         | 通道：弱鸡版CPU<br/>通道程序：任务清单               |

> 优缺点：
>
> 每一个阶段的优点都是解决上一个阶段的缺点。总体来说，整个发展过程就是尽量`减少CPU对I/O过程的干预`，把CPU从复杂的I/O控制事务中解脱出来，以便更多地去完成数据处理工作。

# 1.程序直接控制

