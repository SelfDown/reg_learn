"# reg_learn" 
正则表达式学习

1.从xml 中取某个标签的值

var content = "<xml><service>test</service><body>...</body></xml> "

result = context.match(/<service>(\S*)<\/service>/)
  
result[1] 即匹配的结果

(x) 匹配x保存x在名为$1...$9的变量中 
