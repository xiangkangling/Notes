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
##### git的基本命令
```npm
git init    // 初始化
git add README.md   // 添加某一个文件
git add .      // 添加所有文件
git commit -m "first commit"    // 提交文件,并给出提交内容的描述
git remote add origin https://git.oschina.net/name/package.git   // 设置仓库的别名为origin, 这里用自己仓库的url
git push origin master  // 提交到仓库
```
##### git给远程库添加多个地址
增加第一个地址 `git remote add origin <url1>`          
然后增加第二个地址 `git remote set-url --add origin <url2>`      
增加第三个地址 git `remote set-url --add origin <url3>`        

##### live-server的安装和使用命令
安装: `npm install -g live-server`    
打开: `live-server`   
指定端口打开(当默认端口8080被占用时使用): `live-server --port=8090`      
指定主机打开(默认主机是localhost): `live-server --host=127.0.0.1`  
      






