# state
##### 初始化 state
一般情况下，state 要有专门的**初始化函数**  
应保证初始化之后是可用的、不需进一步加工，如果某一小步出现异常但有补救措施，应在这里执行  
或者发现 state 不可用，也应返回不需进一步处理的异常情况  

##### state 之间的依赖
如果 state 之间有依赖关系  
比如 A state 要等 B state 初始化完成才能初始化  
或者 A state 出现异常后，需要 B state 的结果来补救  

此时应把这些有依赖关系的 state 的**初始化函数**合并在一起