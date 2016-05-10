## word文件里的表格数据内容，转换到excel里。
---
> Date：2016-3-15 author：quillerstone
  > 主要功能描述：
  1. 读取word表格里的文字内容；
  2. 提取关键内容内容；
  3. 将关键内容存储到excel里；
---
###使用下列python库: 
python-docx
xlrd、xlwt
---
> * ### 利用Python-docx模块读取表格里的内容
  from docx import Document
  *打开一个word文档* 
  docx_read = Document('example.docx')
  *获得文件中表格的一个实例（可能有多个）*
  docx= docx_read.tables[0]
  *获得单元格的内容*
  print docx_instance.cell(0, 1).text`
> * ### 利用xlrd存储内容

