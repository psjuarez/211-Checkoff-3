# 211-Checkoff-3
Topic: Garbage Collection: Mark-and-Sweep Garbage Collection (Java or JavaScript)
  I explored the main ways that Java handles garbage collection in order to optimize memory usage, and the methods it uses, mainly concrerning Mark-and-Sweep garbage collection and how that's implemented. The topics I talk about in my presentation that interested me the most, were:
  The tasks this process automates
  When/how often Java uses this process
  How this gains efficiency using Partial Memory Collection and avoiding Memory Fragmentation
Some of the main findings are that the process marks every "reachable" memory allocation through an algorithm that scans them all, then sweeps them away similarly to how free() works in C. Java does not execute this process under any strict conditions, however 
Something I thought was interesting regarding efficiency, were the many processes that work to kind of "compact" memory away from the fragmented state that we've been okay with in C. So far in Comp211 we've worked with understanding fragmented memory when blocks leave smaller blocks in between, however Java's mark and sweep algorithm works against this by either copying the reallocating memory to somewhere else without the gaps, or compacting the existing memory.

References:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Memory_management
https://docs.oracle.com/en/java/javase/26/gctuning/garbage-first-g1-garbage-collector1.html?utm_source=chatgpt.com
