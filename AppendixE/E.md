# 可能与 BGP 一起使用的 TCP 选项

如果一个本地系统的 TCP 用户接口支持 TCP PUSH 功能，那么每个 BGP 报文都**应该**在设置 PUSH 标识的情况下传输。设定 PUSH 标识将强制 BGP 报文要及时被接收者接收。

如果一个本地系统的 TCP 用户接口支持为 TCP 连接设定 DSCP 字段[[RFC2474]](https://www.rfc-editor.org/rfc/rfc2474.html)，那么 BGP 使用的 TCP 连接**应该**在开放时有着 DSCP 字段的0-2位的值为110（二进制）的设定。

一个 BGP 实现**必须**支持 TCP MD5 选项[[RFC2385]](https://www.rfc-editor.org/rfc/rfc2385.html)。