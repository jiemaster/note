# JVM

## 垃圾回收器

### 串行

### 并行

### CMS
1. 新生代：parNew (标记-复制)， 老年代 （标记-清楚 + 空闲列表）
2. CMS 过程
 - Process1: Initial Mark
 - process2: Concurrent Mark
 - process3: Concurrent PreClean
 - process4: Final Remark
 - process5: Concurrent Sweep
 - process6: Concurrent Reset

### G1

