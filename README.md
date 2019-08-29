# python-data-modeling
pandas, numpy, scipy, matplotlib
## Top View
- [1.Python 解析word](#1Python-解析word)
- [2.Connect to DBMS and Select DB](#2Connect-to-DBMS-and-Select-DB)
- [3.Query](#3Query)
- [4.use result](#4use-result)
- [5.video upload to database and retrieve to server site](#5video-upload-to-database-and-retrieve-to-server-site)
- [6.Read video uploaded](#6Read-video-uploaded)
### 1.python 解析word

```python
#showing all the pacjages and versions you have installed
pip freeze

#docx, a package for decoding the word.
pip install python-docx
from docx import Document
from docx.shared import Inches
##locate the document
document = Document('xxxxxxxxxxxxx.docx')  #打开文件docx文档
##解析table
table=document.tables
table_t=table[0  ] #第一个table
##解析Paragraph
paragraph=document.[aragraphs
for i in range(len(table_t.rows)):
    result = table_t.cell(i,0).text + table_t.cell(i,1).text+
    table_t.cell(i,2).text + table_t.cell(i,3).text
    #cell(i,0)表示第(i+1)行第1列数据，以此类推
    print(result)
```
