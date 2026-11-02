---
publish: true
created: 2026-11-01T17:12:07.876Z
modified: 2026-11-01T18:04:23.424Z
tags:
  - project
  - school
---

> [!garden] Summary
> Coursework for the Computer Systems A unit, focused on **parallel and distributed systems**.
>
> The goal was to implement Conway's Game of Life using Go and AWS, comparing the efficiency of different techniques, strategies and architectures. I received a **grade of 80** for the coursework.

> [!tldr]
>
> **Parallel Implementation**
>
> - local parallelism using goroutines and CPU threads
> - visualisation with SDL window, event reporting through channels and basic key command functions (pause, start, save and quit)
> - optimisation using modulus for toroidal wrap around, a worker pool and mutex locks for race condition prevention
> - used CPU profiling to determine computational bottlenecks and evaluate system
>
> ![[media/Game of Life-1793554975937.webp]]
>
> ![[media/Game of Life-1793555083426.webp]]
>
> **Distributed Implementation**
>
> - moved to a distributed implementation on AWS EC2 instances with a client-broker-servers model
> - implemented optimisation techniques, separation and halo exchange, utilising the distributed nature of the system to speed up computation
> - implemented fault tolerance with a simple rollback to resume from whenever the client shut down
>
> ![[media/Game of Life-1793555483512.webp|659x237]]
>
> ![[media/Game of Life-1793555607924.webp]]

#### References
