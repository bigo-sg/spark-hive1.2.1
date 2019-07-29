# spark-hive1.2.1

bigo spark dependency for hive  

1 fix load rpc for hive1.2.1  
  load过程  
  1 动态分区  
  2 静态分区  
  3 无分区，loadtable  
  
  只看带分区的load  
  下分是否overwrite  
  1 是，走replacefiles，如果存在oldpath，删除oldpath, rename整个目录  
  2 否，如果目标分区不存在，走replacefiles，rename整个目录，如果存在目标分区，则逐一mv文件到已有分区  
