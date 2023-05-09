# 与 RFC 1105 的比较

包含所有在[附录 A ](../AppendixA/A.md)，[附录 B](../AppendixB/B.md) ，[附录 C ](../AppendixC/C.md)中记录的改动和下文所述的改动：

基于[[RFC1105]](https://www.rfc-editor.org/rfc/rfc1105.html)的有限状态机部分的小修改对于容纳 BSD 4.3 提供的 TCP 用户接口是有必要的。

在 [RFC 1105](https://www.rfc-editor.org/rfc/rfc1105.html) 中描述的关于 Up/Down/Horizontal 的联系的观念已从该协议中移除。

与 RFC 1105 相比的报文格式变化如下所述：

1. 保持时间字段从 BGP 报头中移除并添加到 OPEN 报文中。

2. 版本字段从 BGP 报头中移除并添加到 OPEN 报文中。

3. 链路类型（Link Type）字段从 OPEN 报文中移除。

4. OPEN CONFIRM 报文被隐式的确认方式取代，由 KEEPALIVE 报文提供。

5. UPDATE 报文格式被明显地改动了。新的字段添加到 UPDATE 报文中以支持多种路径属性。

6. 标识字段被拓展并且其角色扩大到能支持验证功能。

请记住，在 [RFC 1105](https://www.rfc-editor.org/rfc/rfc1105.html) 中提到的 BGP 指的是 BGP-1；而在[[RFC1163]](https://www.rfc-editor.org/rfc/rfc1163.html)中提到的是 BGP-2；在 [RFC 1267](https://www.rfc-editor.org/rfc/rfc1267.html) 提到的是 BGP-3；而在本文档中提到的 BGP 指的则是 BGP-4。