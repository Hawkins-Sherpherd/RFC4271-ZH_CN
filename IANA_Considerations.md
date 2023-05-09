# IANA 观点
   
所有的 BGP 报文包含一个8位的报文类型，为此 IANA 创建并维护一个名为“BGP Message Types”的注册表。这篇文档定义了如下的报文类型：

|名称             |值          |定义
|-----------------|------------|----------
|OPEN             |1           |参见 [Section 4.2](Section04/4.2.md)
|UPDATE           |2           |参见 [Section 4.3](Section04/4.3.md)
|NOTIFICATION     |3           |参见 [Section 4.5](Section04/4.5.md)
|KEEPALIVE        |4           |参见 [Section 4.4](Section04/4.4.md)

未来的分配将以 [[RFC2434]](https://www.rfc-editor.org/rfc/rfc2434.html) 中定义的“标准动作”流程，或以在 [[RFC4020]](https://www.rfc-editor.org/rfc/rfc4020.html) 中定义的 IANA 早期分配流程进行。分配由名称和值组成。

BGP UPDATE 报文可能承载一个或多个路径属性，每个路径属性包含一个8位的属性类型代码。IANA 已在维护这样的一个名为“BGP Path Attributes”的注册表。

这篇文档定义了如下的路径属性类型代码：

|名称               |值          |定义
|-------------------|-----------|----------
|ORIGIN             |1          |参见 [Section 5.1.1](Section05/5.1/5.1.1.md)
|AS_PATH            |2          |参见 [Section 5.1.2](Section05/5.1/5.1.2.md)
|NEXT_HOP           |3          |参见 [Section 5.1.3](Section05/5.1/5.1.3.md)
|MULTI_EXIT_DISC    |4          |参见 [Section 5.1.4](Section05/5.1/5.1.4.md)
|LOCAL_PREF         |5          |参见 [Section 5.1.5](Section05/5.1/5.1.5.md)
|ATOMIC_AGGREGATE   |6          |参见 [Section 5.1.6](Section05/5.1/5.1.6.md)
|AGGREGATOR         |7          |参见 [Section 5.1.7](Section05/5.1/5.1.7.md)

未来的分配将以 [[RFC2434]](https://www.rfc-editor.org/rfc/rfc2434.html) 中定义的“标准动作”流程，或以在 [[RFC4020]](https://www.rfc-editor.org/rfc/rfc4020.html) 中定义的 IANA 早期分配流程进行。分配由名称和值组成。

BGP NOTIFICATION 报文承载了一个8位的错误代码，为此 IANA 创建并维护一个名为“BGP Error Codes”的注册表。这篇文档定义了如下的错误代码：

|名称                       |值          |  定义
|---------------------------|-----------|----------
|Message Header Error       |1          |[Section 6.1](Section06/6.1.md)
|OPEN Message Error         |2          |[Section 6.2](Section06/6.2.md)
|UPDATE Message Error       |3          |[Section 6.3](Section06/6.3.md)
|Hold Timer Expired         |4          |[Section 6.5](Section06/6.5.md)
|Finite State Machine Error |5          |[Section 6.6](Section06/6.6.md)
|Cease                      |6          |[Section 6.7](Section06/6.7.md)

未来的分配将以 [[RFC2434]](https://www.rfc-editor.org/rfc/rfc2434.html) 中定义的“标准动作”流程，或以在 [[RFC4020]](https://www.rfc-editor.org/rfc/rfc4020.html) 中定义的 IANA 早期分配流程进行。分配由名称和值组成。

BGP NOTIFICATION 报文承载了一个8位的错误子代码，每个子代码在特定错误代码的上下文中之中被定义，因此它仅在此上下文中具有唯一性。

IANA 已经创建并维护一系列的“错误子代码”注册表，每个 BGP 错误代码都有独立的注册表。未来的分配将以 [[RFC2434]](https://www.rfc-editor.org/rfc/rfc2434.html) 中定义的“标准动作”流程，或以在 [[RFC4020]](https://www.rfc-editor.org/rfc/rfc4020.html) 中定义的 IANA 早期分配流程进行。分配由名称和值组成。

这篇文档定义了如下的报文头错误子代码：

|名称                          | 值          |定义
|------------------------------|------------|----------
|Connection Not Synchronized   |1           |参见 [Section 6.1](Section06/6.1.md)
|Bad Message Length            |2           |参见 [Section 6.1](Section06/6.1.md)
|Bad Message Type              |3           |参见 [Section 6.1](Section06/6.1.md)

这篇文档定义了如下的 OPEN 报文错误子代码：

|名称                           |值         |定义
|-------------------------------|-----------|----------
|Unsupported Version Number     |1          |参见 [Section 6.2](Section06/6.2.md)
|Bad Peer AS                    |2          |参见 [Section 6.2](Section06/6.2.md)
|Bad BGP Identifier             |3          |参见 [Section 6.2](Section06/6.2.md)
|Unsupported Optional Parameter |4          |参见 [Section 6.2](Section06/6.2.md)
|[Deprecated]                   |5          |参见 [Appendix A](AppendixA/A.md)
|Unacceptable Hold Time         |6          |参见 [Section 6.2](Section06/6.2.md)

这篇文档定义了如下的 UPDATE 报文错误子代码：

|名称                               |值     |定义
|-----------------------------------|-------|----------
|Malformed Attribute List           |1      |参见 [Section 6.3](Section06/6.3.md)
|Unrecognized Well-known Attribute  |2      |参见 [Section 6.3](Section06/6.3.md)
|Missing Well-known Attribute       |3      |参见 [Section 6.3](Section06/6.3.md)
|Attribute Flags Error              |4      |参见 [Section 6.3](Section06/6.3.md)
|Attribute Length Error             |5      |参见 [Section 6.3](Section06/6.3.md)
|Invalid ORIGIN Attribute           |6      |参见 [Section 6.3](Section06/6.3.md)
|[Deprecated]                       |7      |参见 [Appendix A](AppendixA/A.md)
|Invalid NEXT_HOP Attribute         |8      |参见 [Section 6.3](Section06/6.3.md)
|Optional Attribute Error           |9      |参见 [Section 6.3](Section06/6.3.md)
|Invalid Network Field              |10     |参见 [Section 6.3](Section06/6.3.md)
|Malformed AS_PATH                  |11     |参见 [Section 6.3](Section06/6.3.md)