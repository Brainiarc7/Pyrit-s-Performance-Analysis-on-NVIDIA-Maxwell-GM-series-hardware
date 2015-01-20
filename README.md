# Pyrit-s-Performance-Analysis-on-NVIDIA-Maxwell-GM-series-hardware

To see the results of the analysis, open this file with NVIDIA Visual Profiler.

Notes:

1. NVIDIA Visual profiler is a component of the NVIDIA CUDA SDK toolkit.
2. Observations dawn from the analysis are as follows:

(a).Low Memcpy/Compute Overlap is observed while running Pyrit: implies that the percentage of time when memcpy is being performed in parallel with compute is low.( 0 ns / 791.203 ms)
(b). Low kernel concurrency: The percentage of time when two kernels are being executed in parallel is low.( 0 ns / 512.441 s)
(c). Low memcpy throughput (Currently at ~1.306 GB/s for memcpys accounting for ~57.3% of all memcpy time).
(d). Compute Utilization: Normal, at about ~100% for both GPU and CPU. Minimal tearing is observed in X Graphical server in this Optimus-enabled notebook.

More profiled tests for other CUDA enabled software on 'nix is coming. 
