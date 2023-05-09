# 复杂 AS_PATH 聚合

一个选择提供可保留大量路径信息的路径聚合算法的实现可能希望使用以下的程序流程：

为达成聚合两条路由的 AS_PATH 属性的目的，我们为每个自治系统建立了 <类型，值> 的二元组模型，“类型”表示自治系统所属的路径分段为何种类型（例如，AS_SEQUENCE，AS_SET），而“值”即是自治系统号码。两个自治系统在其二元组的内容相等时，它们便是相等的。

聚合两个 AS_PATH 属性的算法的工作方式如下文所示：

* a) 标识每个 AS_PATH 属性中在 AS_PATH 属性中均具有相同的相对顺序的相同的自治系统。两个自治系统，X 和 Y ，如果在这些情况下它们具有相同的顺序：
  * 在所有的 AS_PATH 属性中，X 在 Y 之前，或者
  * 在所有的 AS_PATH 属性中，Y 在 X 之前

* b) 聚合过的 AS_PATH 属性由 (a) 中标识的自治系统组成，它们以聚合前的 AS_PATH 属性里相同的顺序出现在这里。如果两个在 (a) 中标识的连续的自治系统在所有聚合前的 AS_PATH 属性里都不紧挨着，那么所有属性中的中间的自治系统（这些夹在两个连续的自治系统中间的自治系统是相同的）将融合到一个包含所有 AS_PATH 中的中间自治系统的 AS_SET 路径分段。这个分段将在聚合后的属性里放在两个连续的在 (a) 中被标识的自治系统中间。

* c) 每个在聚合后的 AS_PATH 里邻接的二元组，如果二者都有相同的类型，将它们融合就能使生成的分段的长度不超过255。

      If, as a result of the above procedure, a given AS number appears
      more than once within the aggregated AS_PATH attribute, all but
      the last instance (rightmost occurrence) of that AS number should
      be removed from the aggregated AS_PATH attribute.

如果，在经历上述流程后，一个给定的自治系统号码在聚合后的 AS_PATH 属性中出现多次，除了最后一个实例外（在最右侧的）的所有该自治号码的实例应当从聚合后的 AS_PATH 属性中移除。