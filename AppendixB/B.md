# 与 RFC 1267 的比较

包含所有在[附录 A ](../AppendixA/A.md)中记录的改动和下文所述的改动：

BGP-4 能够在可能将一组可达的目的地表示为单个 IP 前缀的环境中运作。网络中“类”的概念，子网划分，这些与 BGP-4 本身并不相关。为了容纳这些特性，BGP-4 修改了与 AS_PATH 属性相关的语义和编码标准。添加了新的文字来定义与 IP 前缀相关的语义。这些能力使得 BGP-4 能够支持这些提议的“超网”主题[[RFC1518](https://www.rfc-editor.org/rfc/rfc1518.html), [RFC1519](https://www.rfc-editor.org/rfc/rfc1519.html)]。

为了简化配置，这个版本引入了一个新的属性：LOCAL_PREF，有利于路由选择的程序流程。

INTER_AS_METRIC 属性被重命名为 MULTI_EXIT_DISC。

引入了一个名为 ATOMIC_AGGREGATE 的新属性，用于确保一些聚合不会被排除在聚合之外。还有另一个新的名为 AGGREGATOR 的属性，可用于在广播聚合路由时标识哪个自治系统和哪个该自治系统内的 BGP Speaker 对此进行的聚合。

为了保证保持计时器是对称的，保持计时器现在在每条连接之上进行协商。现在支持值为0的保持计时器。