# 控制版本协商

因为 BGP-4 可以携带 BGP-3 中不能正确处理的汇聚路由，一个同时支持 BGP-4 和其它版本的 BGP 实现应该提供只基于每对对等连接进行 BGP-4 会话的能力。