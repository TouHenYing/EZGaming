# MarkDown tips

## 1. 如何实现表格合并单元
  - 在md文件中添加一个未合并的表格.
  - 导出md文件成html
  - 在html的源码中修改,添加`<rowspan>`,`<colspan>`
  - 修改好后将`table`的源码拷贝到md文件中

## 2. 如何实现在文档内跳转
  1. 先定义一个锚(id)
     - `<span id="jump">Hello World</span>`
  2. 然后使用markdown的语法:
     - `[XXXX](#jump)`
