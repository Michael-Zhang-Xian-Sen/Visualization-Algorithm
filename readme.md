# Readme

该文件为整合后的代码结果。
每个页面中最后需添加如下引用：

* `<script src="https://cdn.bootcss.com/d3/4.10.0/d3.js"></script>`
* `<script type="text/javascript" src="js/move.min.js"></script>`
* `<script src="js/quick_sort.js"></script>`

亦或是

* `<script src="https://cdn.bootcss.com/d3/4.10.0/d3.js"></script>`
* `<script type="text/javascript" src="js/move.min.js"></script>`
* `<script src="js/direct_sort.js"></script>`

<strong>注意！</strong>

以下是页面中的一些特殊改动

* 由于页面中存在名称为move的函数。与引用库函数冲突，需将原页面函数更名为move1。
* title需要更改为相应的算法名称

<strong>算法信息</strong>

1. 直接插入排序
    * 时间复杂度：O(n^2)
    * 空间复杂度：O(1)
2. 快速排序
    * 时间复杂度：O(nlogn)
    * 空间复杂度：O(nlogn)
3. kruskal算法
    * 时间复杂度：
    * 空间复杂度：

响应式有问题.

kruskal算法, 添加了一个css文件,位于assets/css/kruskal.css.

### BUG列表：

1. 响应式。(fucking Responsive layout)
	* 快速排序。   已完成。
	* 直接插入排序需要改变块的大小或者改变svg大小。已完成。
    * kruskal完全不适配。   采用大片留白，已完成。具体要不要留白看小花。
2. explain区域的边距。  已完成
3. 调节速度的初始位置及可调节范围。  已完成。
4. kruskal算法在小屏幕的塌陷问题。  已完成。
5. 某些算法升序和降序的解释内容不正确。  已完成
    * 快速排序已完成。
    * 直接插入排序已完成。 
6. 顶栏在最后需要换一下。  留待解决
7. ~~开始只能使用一次，需更正为可多次使用。~~
8. “开始”按钮需要调整。 已完成。

#### 1.0bug

全部已在1.1版本中解决。

1. “开始”按钮在响应式中的显示不对。   解决
2. 部分解释内容没有清除。             解决
3. 点击random或自定义后应清除当前所有timeout.  解决

#### 1.1bug

1. 解释内容需要改进。

#### 1.3版本

修改了所有可使算法刷新的事件。

修改了kruskal算法的bug，当第二条边与第一条边没有相同点时算法结果会出现错误。

#### 1.4版本

修复了快速排序算法会出现的所有移动rect上移的问题，源于移动过程中的一个正则表达式因为逗号的出现而匹配错误数字。

#### 1.5版本

修正排序结束更换排序方式后无法继续执行的bug。
修正直接插入排序、快速排序执行过程中位置不正确的问题。
修正kruskal中的一个bug，第一步会将表格中“未执行”和“第一步”里的“剩余边及权值”全部进行排序。修改为只有“第一步”里会进行排序。