"# reg_learn" 
正则表达式学习

1.从xml 中取某个标签的值

result = "<xml><service>test</service><body>...</body></xml> ".match(/<service>(\S*)<\/service>/)
  
result[1] 即匹配的结果

(x) 匹配x保存x在名为$1...$9的变量中 


去掉前后空格 "<body><service>  \ntest  </service></body>".match(/<service>\s*(\S*)\s*<\/service>/)
  
 去掉前后空格。中间有空格
 "<body><service>  \nte s t  </service></body>".match(/<service>\s*(\S*[\w\s]*\S)\s*<\/service>/)
  
  
 ^ 匹配一个输入或一行的开头，/^a/匹配"an A"，而不匹配"An a" 
  
$ 匹配一个输入或一行的结尾，/a$/匹配"An a"，而不匹配"an A" 

\* 匹配前面元字符0次或多次，/ba*/将匹配b,ba,baa,baaa 

\+ 匹配前面元字符1次或多次，/ba*/将匹配ba,baa,baaa 

? 匹配前面元字符0次或1次，/ba*/将匹配b,ba 

(x) 匹配x保存x在名为$1...$9的变量中 

x|y 匹配x或y 

{n} 精确匹配n次 

{n,} 匹配n次以上 

{n,m} 匹配n-m次 

[xyz] 字符集(character set)，匹配这个集合中的任一一个字符(或元字符) 

[^xyz] 不匹配这个集合中的任何一个字符 

[\b] 匹配一个退格符 

\b 匹配一个单词的边界 

 \B 匹配一个单词的非边界 

\cX 这儿，X是一个控制符，/\cM/匹配Ctrl-M 

\d 匹配一个字数字符，/\d/ = /[0-9]/ 

\D 匹配一个非字数字符，/\D/ = /[^0-9]/ 

\n 匹配一个换行符 

\r 匹配一个回车符 

\s 匹配一个空白字符，包括\n,\r,\f,\t,\v等 

\S 匹配一个非空白字符，等于/[^\n\f\r\t\v]/ 

\t 匹配一个制表符 

\v 匹配一个重直制表符 

\w 匹配一个可以组成单词的字符(alphanumeric，这是我的意译，含数字)，包括下划线，如[\w]匹配"$5.98"中的5，等于[a-zA-Z0-9] 

\W 匹配一个不可以组成单词的字符，如[\W]匹配"$5.98"中的$，等于[^a-zA-Z0-9]。
