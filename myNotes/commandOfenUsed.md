##### i5ting_toc安装命令	
npm install -g i5ting_toc		
##### i5ting_toc 将MD转换为HTML的命令		
i5ting_toc -f qksheetProjectReadingNotes.md -o	
##### web服务器live-server的安装及使用
全局安装: npm install -g live-server        
使用: 在指定文件位置打开命令行工具(如cmd, git bash), 输入liver-server   
指定接口打开(默认接口是8080): live-server --port=8081 
##### 在指定位置打开命令行
按住shift键 然后右键 点击`在此处打开命令窗口`
##### 清空命令行
cls
##### window下生成SSH key(公钥)
cd到c:/Users/Administrator/.ssh目录下,然后执行:
```js
ssh-keygen -t rsa
```
##### 查看公钥
```js
cat ~/.ssh/id_rsa.pub 
```  
或打开c:/Users/Administrator/.ssh/，在文件中，id_rsa是私钥文件，id_rsa.pub是公钥文件




