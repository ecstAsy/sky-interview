<h3 align='center'>语义化标签</h3>

* 语义化标签优点
  - 代码结构清晰，方便阅读，有利于团队合作开发。
  - 方便其他设备解析（如屏幕阅读器、盲人阅读器、移动设备）以语义的方式来渲染网页。
  - 有利于搜索引擎优化（SEO）。
  - 方便其他设备解析（如移动设备、盲人阅读器等）。
  - 有利于合作，遵守W3C标准。

* 常见语义化标签
  - __title__  页面主体内容。
  - __h(1-6) h1~h6__ 分级标题。
  - __ul/li__ ul => 无序列表。 li=>有序列表。
  - __header__  页眉通常包括网站标志、主导航、全站链接以及搜索框。
  - __nav__ 标记导航，仅对文档中重要的链接群使用。
  - __main__ 页面主要内容，一个页面只能使用一次。如果是web应用，则包围其主要功能。
  - __article__ 定义外部的内容，其中的内容独立于文档的其余部分。
  - __section__ 定义文档中的节（section、区段）。比如章节、页眉、页脚或文档中的其他部分。
  - __aside__ 定义其所处内容之外的内容。如侧栏、文章的一组链接、广告、友情链接、相关产品列表等。
  - __footer__ 页脚，只有当父级是body时，才是整个页面的页脚。
  - __small__ 呈现小号字体效果，指定细则，输入免责声明、注解、署名、版权。
  - __strong__ 和 em 标签一样，用于强调文本，但它强调的程度更强一些。
  - __em__ 将其中的文本表示为强调的内容，表现为斜体。
  - __mark__ 使用黄色突出显示部分文本。
  - __figure__ 规定独立的流内容（图像、图表、照片、代码等等）（默认有40px左右margin）。
  - __figcaption__ 定义 figure 元素的标题，应该被置于 figure 元素的第一个或最后一个子元素的位置。
  - __cite__ 表示所包含的文本对某个参考文献的引用，比如书籍或者杂志的标题。
  - __blockquoto__ 定义块引用，块引用拥有它们自己的空间。
  - __q__ 短的引述（跨浏览器问题，尽量避免使用）。
  - __time__ datetime属性遵循特定格式，如果忽略此属性，文本内容必须是合法的日期或者时间格式。
  - __abbr__ 简称或缩写。
  - __dfn__ 定义术语元素，与定义必须紧挨着，可以在描述列表dl元素中使用。
  - __address__ 作者、相关人士或组织的联系信息（电子邮件地址、指向联系信息页的链接）。
  - __del__ 移除的内容。
  - __ins__ 添加的内容。
  - __code__ 标记代码。
  - __meter__ 定义已知范围或分数值内的标量测量。（Internet Explorer 不支持 meter 标签）
  - __progress__ 定义运行中的进度（进程）。

* 图示

    ![语义化](../assets/semantization.png)

* 注意
  - 尽可能少的使用无语义的标签div和span
  - 在语义不明显时，既可以使用div或者p时，尽量用p，因为p在默认情况下有上下间距，对兼容特殊终端有利
  - 不要使用纯样式标签，如：b、font、u等，改用css设置
  - 需要强调的文本，可以包含在strong或者em标签中
  - 使用表格时，标题要用caption，表头用thead，主体部分用tbody包围，尾部用tfoot包围。表头和一般单元格要区分开，表头用th，单元格用td
  - 表单域要用fieldset标签包起来，并用legend标签说明表单的用途
  - 每个input标签对应的说明文本都需要使用label标签，并且通过为input设置id属性