# JVM

## 垃圾回收器

### 串行

### 并行

### CMS
1. 新生代：parNew (标记-复制)， 老年代 （标记-清楚 + 空闲列表）
2. CMS 过程
 - 1: Initial Mark
 - 2: Concurrent Mark
 - 3: Concurrent PreClean
 - 4: Final Remark
 - 5: Concurrent Sweep
 - 6: Concurrent Reset

### G1

