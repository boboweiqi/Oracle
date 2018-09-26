# Oracle

概念：

统计信息主要是描述数据库中表，索引的大小，规模，数据分布状况等的一类信息。比如，表的行数，块数，平均每行的大小，索引的leaf blocks，索引字段的行数，
不同值的大小等，都属于统计信息。CBO正是根据这些统计信息数据，计算出不同访问路径下，不同join 方式下，各种计划的成本，最后选择出成本最小的计划。

在CBO(基于代价的优化器模式)条件下，SQL语句的执行计划由统计信息来决定，若没有统计信息则会采取动态采样的方式决定执行计划！可以说统计信息关乎sql的执行计划是否正确，属于sql执行的指导思想，oracle的初始化参数statistics_level控制收集统计信息的级别，有三个参数值:
BASIC :收集基本的统计信息
TYPICAL：收集大部分统计信息(数据库的默认设置)
ALL：收集全部统计信息
Oracle 10g之后，Query Optimizer就已经将CBO作为默认优化器，并且Oracle官方不再支持RBO服务。


weblogic.jar在启动weblogic服务的时候就被自动添加到CLASSPATH中
当用nohup命令执行启动weblogicde脚本，若没指定输出信息文件，会默认保持到启动脚本（startWeblogic.sh）的当前目录下的nohuo.out文件中
