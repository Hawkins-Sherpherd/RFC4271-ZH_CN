# 内容表

* [1. 介绍](Section01/1.md)
    * [1.1. 常用术语解释](Section01/1.1.md)
    * [1.2. 规范需求](Section01/1.2.md)
* [2. 致谢](Section02/2.md)
* [3. 运作总述](Section03/3.md)
    * [3.1. 路由：广播与存储](Section03/3.1.md)
    * [3.2. 路由信息数据库](Section03/3.2.md)
* [4. 报文格式](Section04/4.md)
    * [4.1. 报文头格式](Section04/4.1.md)
    * [4.2. OPEN 报文格式](Section04/4.2.md)
    * [4.3. UPDATE 报文格式](Section04/4.3.md)
    * [4.4. KEEPALIVE 报文格式](Section04/4.4.md)
    * [4.5. NOTIFICATION 报文格式](Section04/4.5.md)
* [5. 路径属性](Section05/5.md)
    * [5.1. 路径属性的使用](Section05/5.1/5.1.md)
        * [5.1.1. ORIGIN](Section05/5.1/5.1.1.md)
        * [5.1.2. AS_PATH](Section05/5.1/5.1.2.md)
        * [5.1.3. NEXT_HOP](Section05/5.1/5.1.3.md)
        * [5.1.4. MULTI_EXIT_DISC](Section05/5.1/5.1.4.md)
        * [5.1.5. LOCAL_PREF](Section05/5.1/5.1.5.md)
        * [5.1.6. ATOMIC_AGGREGATE](Section05/5.1/5.1.6.md)
        * [5.1.7. AGGREGATOR](Section05/5.1/5.1.7.md)
* [6. BGP 错误处理](Section06/6.md)
    * [6.1. 报文头错误处理](Section06/6.1.md)
    * [6.2. OPEN 报文错误处理](Section06/6.2.md)
    * [6.3. UPDATE 报文错误处理](Section06/6.3.md)
    * [6.4. NOTIFICATION 报文错误处理](Section06/6.4.md)
    * [6.5. 保持计时器超时错误处理](Section06/6.5.md)
    * [6.6. 有限状态机错误处理](Section06/6.6.md)
    * [6.7. 终止](Section06/6.7.md)
    * [6.8. BGP 连接冲突检测](Section06/6.8.md)
* [7. BGP 版本协商](Section07/7.md)
* [8. BGP 有限状态机 (FSM)](Section08/8.md)
    * [8.1. BGP 有限状态机事件](Section08/8.1/8.1.md)
        * [8.1.1. 与可选会话关联的可选事件属性](Section08/8.1/8.1.1.md)
        * [8.1.2. 管理性事件](Section08/8.1/8.1.2.md)
        * [8.1.3. 计时器事件](Section08/8.1/8.1.3.md)
        * [8.1.4. 基于 TCP 连接的事件](Section08/8.1/8.1.4.md)
        * [8.1.5. 基于 BGP 报文的事件](Section08/8.1/8.1.5.md)
    * [8.2. 有限状态机描述](Section08/8.2/8.2.md)
        * [8.2.1. 有限状态机定义](Section08/8.2/8.2.1/8.2.1.md)
            * [8.2.1.1. 术语“主动”和“被动”](Section08/8.2/8.2.1/8.2.1.1.md)
            * [8.2.1.2. 有限状态机与冲突检测](Section08/8.2/8.2.1/8.2.1.2.md)
            * [8.2.1.3. 有限状态机与可选会话属性](Section08/8.2/8.2.1/8.2.1.3.md)
            * [8.2.1.4. 有限状态机事件编号](Section08/8.2/8.2.1/8.2.1.4.md)
            * [8.2.1.5. 与具体实现相关的有限状态机行为](Section08/8.2/8.2.1/8.2.1.5.md)
        * [8.2.2. 有限状态机](Section08/8.2/8.2.2.md)
* [9. UPDATE 报文处理](Section09/9.md)
    * [9.1. 决策步骤](Section09/9.1/9.1.md)
        * [9.1.1. 阶段 1: 偏好程度计算](Section09/9.1/9.1.1.md)
        * [9.1.2. 阶段 2: 路由选择](Section09/9.1/9.1.2/9.1.2.md)
            * [9.1.2.1. 路由解析性条件](Section09/9.1/9.1.2/9.1.2.1.md)
            * [9.1.2.2. 解除关联 (阶段 2)](Section09/9.1/9.1.2/9.1.2.2.md)
        * [9.1.3. 阶段 3: 路由广播](Section09/9.1/9.1.3.md)
        * [9.1.4. 重复路由](Section09/9.1/9.1.4.md)
    * [9.2. Update-Send 过程](Section09/9.2/9.2.md)
        * [9.2.1. 控制路由流量开销](Section09/9.2/9.2.1/9.2.1.md)
            * [9.2.1.1. 路由广播的频率](Section09/9.2/9.2.2/9.2.2.1.md)
            * [9.2.1.2. 路由发布的频率](Section09/9.2/9.2.2/9.2.2.2.md)
        * [9.2.2. 路由信息的高效组织](Section09/9.2/9.2.2/9.2.2.md)
            * [9.2.2.1. 信息量削减](Section09/9.2/9.2.2/9.2.2.1.md)
            * [9.2.2.2. 聚合路由信息](Section09/9.2/9.2.2/9.2.2.2.md)
    * [9.3. 路由选择标准](Section09/9.3.md)
    * [9.4. 发布 BGP 路由](Section09/9.4.md)
* [10. BGP 计时器](Section10/10.md)
* [附录 A. 与 RFC 1771 的比较](AppendixA/A.md)
* [附录 B. 与 RFC 1267 的比较](AppendixB/B.md)
* [附录 C. 与 RFC 1163 的比较](AppendixC/C.md)
* [附录 D. 与 RFC 1105 的比较](AppendixD/D.md)
* [附录 E. 可能与 BGP 一同使用的 TCP 选项](AppendixE/E.md)
* [附录 F. 实现建议](AppendixF/F.md)
    * [附录 F.1. 每个报文传递多个网络信息](AppendixF/F.1.md)
    * [附录 F.2. 减少路由动荡](AppendixF/F.2.md)
    * [附录 F.3. 路径属性排序](AppendixF/F.3.md)
    * [附录 F.4. AS_SET 排序](AppendixF/F.4.md)
    * [附录 F.5. 控制版本协商](AppendixF/F.5.md)
    * [附录 F.6. 复杂 AS_PATH 聚合](AppendixF/F.6.md)
* [安全观点](Security_Considerations.md)
* [IANA 观点](IANA_Considerations.md)
* [标准参考](Normative_References.md)
* [参考信息](Informative_References.md)