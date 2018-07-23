# TPC-DS-diff
> 包含两个部分:

    - DDL: 
        DDL文件夹中包含所有25张表的DDL语句, 其中:
            - spark-sql-DDL.sql是Spark-SQL修改过的DDL, 主要修改内容为将char(N)类型修改为String类型.
            - tpcds-_source.sql是原始的为Oracle生成的DDL语句
    - queries:
        - 包含针对Oracle平台的修改过99条query, 原始的query可以用tpc-ds-tools生成,但是原始的会有部分query跑不成功, 修改的部分主要是显式在date类型变量相关的表达式中使用to_date函数