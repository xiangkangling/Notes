#### 外部链接
[常用快捷键总结](https://segmentfault.com/a/1190000009396435)  
 

## vscode常用快捷键
1. 预览markdown: Ctrl + Shift + V
2. 自动保存: File -> AutoSave
3. 切换自动换行: Alt + Z
4. 格式化代码: 选中需要格式化的代码 Ctrl + k, Ctrl + f  (只对.html .js文件有效)
5. 在当前行上下复制当前行: Shift+Alt+Up/Down        
6. 折叠区域代码: Ctrl + Shift + [
7. 展开区域代码: Ctrl + Shift + ]   
8. 折叠区域内所有代码（包括子域和父域）: Ctrl + K Ctrl + [
9. 展开区域内所有代码（包括子域和父域）: Ctrl + K Ctrl + ]
10. 移动当前行上下: Alt + Up/Down
11. 在当前行之后插入一行: Ctrl + Enter
12. 在当前行之前插入一行: Ctrl + Shift+Enter
13. 搜索指定行: ctrl + G
14. 回到上次鼠标的位置: Alt + ← (左箭头)
15. 所有文件中搜索: Ctrl + Shift + f    
16. 重新打开一个关闭的页面: Ctrl + Shift + T            
17. 搜索打开文件: Ctrl + T 
18. 查看正在运行的插件: Ctrl + Shift + P 并输入 Show running extensions         
19. 删除上一个单词: Mac( option + Backspace ),window( Ctrl + Backspace )        
20. 逐个选择文本: Mac( option + Shift + 左右箭头 ),window( Ctrl + Shift + 左右箭头 )
21. 格式化代码: Alt+Shift+f

## Mac快捷键和常用命令：
> 快捷键   
1. Chrome打开开发者工具：command + option(alt) + I      
2. 撤销：Command-Z          
3. 重做：Command-Shift-Z    
4. 打开文件路径：shift+command+g然后copy地址        
5. 快速锁屏：control+command+q            
6. QuickTime Player退出录制: command + control + esc 

> 常用命令     
1. 停止阿里安全服务：./alisafe stop         
2. 开启阿里安全服务：./alisafe start            
3. 查看IP地址的命令：ifconfig           
4. 修改hosts:
```cmd
	先在终端输入命令：sudo vi /etc/hosts
	输入密码
	输入i
	在文件最后面修改hosts
	按esc，输入:wq ，回车
	修改成功
```
5. 查看鼠标速度参数的命令：
```cmd
	defaults read -g com.apple.mouse.scaling（移速调到最大时默认是3）
        修改鼠标速度参数的命令：
	defaults write -g com.apple.mouse.scaling（建议设为6-8，修改后需要重启电脑才能生效）
```




## chrome快捷键
1. 快速切换响应式模式: cmd + shift + M 




## vscode常用插件
1. Vetur    
    vue代码高亮显示代码补全等
2. Chinese
    vsc中文显示
3. vscode-icons
    文件图表
4. Color Picker
    代码的颜色选择器
5. JavaScript (ES6) code snippets
    支持JavaScript  ES6 语法
6. HTML Snippets
    支持HTML5标签提示
7. HTML CSS support
    css 自动补齐
8. jQuery Code Snippets
    jq代码段提示
9. open in browser
    在浏览器中打开，安装后在左侧目录中右键点击会出现 open in browser 选项