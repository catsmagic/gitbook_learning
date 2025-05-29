## gitbook入门相关内容
在setting->pages可发布gitbook，即创建page使他人直接通过链接访问渲染后的电子书
更新电子书，应该先在本地生成电子书后，从生成的_book文件中复制到github仓库中。
当本地电子书部分内容不方便公开时，删除该章节，并需要更改根目录下的index.html文件，以及其余章节的.html文件：
```
<link rel="prev" href="../2_Viexergy/viexergy.html" />
以及
 <li class="chapter " data-level="1.2" data-path="../1_Ebsilon/ebsilon.html">
```
