---
layout: publication
title: "IDIO: Network-Driven, Inbound Network Data Orchestration on Server Processors"
image:
authors:
  - name: Mohammad Alian
    short: M. Alian
  - name: Siddharth Agarwal
    short: S. Agarwal
  - name: Jongmin Shin
  - name: Neel Patel
    short: N. Patel
  - name: Yifan Yuan
    short: Y. Yuan
  - name: Daehoon Kim
  - name: Ren Wang
    short: R. Wang
  - name: Nam Sung Kim
    short: N. S. Kim
co-first: false
type: Conference
international: true
paper:
  year: 2022
  publisher: "IEEE/ACM International Symposium on Microarchitecture"
  publisher-short: "MICRO"
  ref: pp. 480-493
sidebar:
  doi: 10.1109/MICRO56248.2022.00042
hidden: false
---

High-bandwidth network interface cards (NICs), each capable of transferring 100s of Gigabits per second, are making inroads into the servers of next-generation datacenters. Such unprecedented data delivery rates impose immense pressure, especially on the server’s memory subsystem, as NICs first transfer network data to DRAM before processing. To alleviate the pressure, the cache hierarchy has evolved, supporting a direct data I/O (DDIO) technology to directly place network data in the last-level cache (LLC). Subsequently, various policies have been explored to manage such LLC and have proven to effectively reduce service latency and memory bandwidth consumption of network applications. However, the more recent evolution of the cache hierarchy decreased the size of LLC per core but significantly increased that of midlevel cache (MLC) with a non-inclusive policy. This calls for a re-examination of the aforementioned DDIO technology and management policies. In this paper, first, we identify three shortcomings of the current static data placement policy placing network data to LLC first and the non-inclusive policy with a commercial server system: (1) ineffectively using large MLC, (2) suffering from high rates of writebacks from MLC to LLC, and (3) breaking the isolation between application and network data enforced by limiting cache ways for DDIO. Second, to tackle the three shortcomings, we propose an intelligent direct I/O (IDIO) technology that extends DDIO to MLC and provides three synergistic mechanisms: (1) self-invalidating I/O buffer, (2) network-driven MLC prefetching, and (3) selective direct DRAM access. Our detailed experiments using a full-system simulator — capable of running modern DPDK userspace network functions while sustaining 100Gbps + network bandwidth — show that IDIO significantly reduces data movement (up to 84% MLC and LLC writeback reduction), provides LLC isolation (up to 22% performance improvement), and improves tail latency (up to 38% reduction in 99th latency) for receive-intensive network applications.