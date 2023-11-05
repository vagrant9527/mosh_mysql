<a name="EkcFD"></a>
## 一、概览
<a name="xaq6z"></a>
### 1.一些数据库的基本概念
![](https://cdn.nlark.com/yuque/0/2023/jpeg/33626411/1685256043335-7f7f3ded-a8e0-4b2d-a887-f0eddd960914.jpeg)<br />SQL可以分为两类，关系型和非关系型。（本课程只介绍关系型，即多张表通过关系彼此关联）<br />其中常用的关系型sql有：MYSQL、SQL server、Oracle<br />每种DBMS的sql语言略有不同但是都遵循SQL规范

<a name="VfHpx"></a>
### 2、数据库的使用
mysql workbench是一个用来连接数据库的图形化界面。<br />127.0.0.1是本地计算机地址，3306是mysql服务器的默认端。<br />mysql workbench上端工具栏，创建sql新标签，或者打开sql文件<br />mysql workbench左侧导航栏：Adminstration、schemas<br />Adminstration：管理工作，比如开始或者结束服务器、导入导出数据等<br />schemas：查看当前服务器中的数据库（sys就是mysql自带的一个数据库）<br />mysql workbench中间：sql编辑器<br />mysql workbench右上角：面板隐藏按钮<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/33626411/1685257848549-87d92c5e-c172-426d-abd7-054727a4866c.png#averageHue=%23abd6c0&clientId=ue4877571-aa75-4&from=paste&height=699&id=u69e16a3b&originHeight=1049&originWidth=1917&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=252838&status=done&style=none&taskId=uede31299-9075-4ebd-ab85-1f6e742ba82&title=&width=1278)
<a name="WbXIx"></a>
### 3、创建数据库
1.每个数据库都有这些对象：<br />tables：表，存储数据的地方<br />views：虚拟表，把不同表的数据结合在一起放入虚拟表，对建立报告很有用<br />stored procedures:存储过程，查询数据<br />functions:函数，查询数据<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/33626411/1685265170720-78f74035-92f4-4e7c-9cd8-70c938e457e8.png#averageHue=%23d7c6aa&clientId=u0cfc6bdc-e2cd-4&from=paste&height=303&id=ua132e56d&originHeight=454&originWidth=415&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=58523&status=done&style=none&taskId=u0bb8c443-c3d6-4a70-8813-f0dc977923e&title=&width=276.6666666666667)<br />表：每张表由行和列组成，每一行就代表一条记录。<br />2、为什么要用这么多张表去构建关系型数据库<br />1）为了消除依赖：比如说我们将所有信息存储在一张表里，某个人的信息可能会出现在这张表多次，如果我们要修改他的部分信息（比如电话）就需要操作很多次，若是将信息分类放在不同的表中，那么只要去对应表中修改一次即可，只要保证能找到就好<br />2）减少内存占用<br />比如有存储学生、老师信息这样的一个场景，若是将它们全部放在一张表中，则每写一次学生信息都要写一遍老师信息，而老师是比学生少的，这样就会有冗余，因此要分别创建学生表与老师表
<a name="Fnu1v"></a>
### 4、课程概览
1-4：基本sql技能、包括获取（retrieve）、插入(insert)、更新(update)、删除(delete)<br />5-7：汇总数据，编写复杂查询，mysql基本内置函数<br />8-9：创建视图、存储过程和函数-->存储你的查询供后续使用<br />10-11：触发器（tiggers），事件(events)，事务(transactions)，并发(concurrency)<br />12：数据类型<br />13：设计数据库<br />14：索引-->使用它来为查询提速<br />15：保护数据库

