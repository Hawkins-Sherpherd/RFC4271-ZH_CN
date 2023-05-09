# 与 RFC 1771 的比较

与 [[RFC1771]](https://www.rfc-editor.org/rfc/rfc1771.html) 相比，本文档有相当多的变化（实在太多了，在这里甚至都不能完整列出）。

下面列出了技术性的变更：

* 对诸如 TCP MD5 [[RFC2385]](https://www.rfc-editor.org/rfc/rfc2385.html)、BGP 路由反射器[[RFC2796]](https://www.rfc-editor.org/rfc/rfc2796.html)、BGP 联邦[[RFC3065]](https://www.rfc-editor.org/rfc/rfc3065.html)和 BGP 路由刷新[[RFC2918]](https://www.rfc-editor.org/rfc/rfc2918.html)等功能的使用的反映所作出的更改。

* 明确 BGP 标识在 AGGREGATOR 属性中的使用。

* BGP Speaker 添加从其对等体接收的前缀数量的上界值的程序流程。

* BGP Speaker 为进行跨自治系统的流量工程而允许在 AS_PATH 属性中包含多个自身 AS 号的能力。

* 明确多种类型的 NEXT_HOP。

* 明确 ATOMIC_AGGREGATE 属性的使用。

* 直接的下一跳和路径属性中指定的下一跳之间的联系。

* 明确解除关联的程序流程。

* 明确路由广播频率的概念。

* 可选参数类型1（Authentication Information）被废除。

* UPDATE 报文错误子代码7（AS Routing Loop）被废除。

* OPEN 报文错误子代码5（Authentication Failure）被废除。

* 标识字段的验证功能被废除。

* 实现**必须**支持 TCP MD5 [[RFC2385]](https://www.rfc-editor.org/rfc/rfc2385.html)用于验证。

* 对 BGP 有限状态机概念的明确。