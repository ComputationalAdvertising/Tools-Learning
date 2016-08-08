## Sublime-使用总结

+ author: zhouyongsdzh
+ date: 20160807

### Sublime安装

1. 官网下载相应版本：https://www.sublimetext.com/3
2. 以Unbuntu为例，

```
1. 进入安装目录~/software/: cd ~/software/
2. 下载barball格式：wget https://download.sublimetext.com/sublime_text_3_build_3114_x64.tar.bz2
3. 解压：tar jxvf sublime_text_3_build_3114_x64.tar.bz2, 生成sublime_text_3目录
4. 在~/software/sublime_text_3下可直接运行：./sublime_text 打开。
5. 创建软链接（方便起见）：
6. 1). 复制：sudo cp ~/software/sublime_text_3/sublime_text.desktop /usr/share/applications
7. 2). 修改配置文件：/usr/share/applications/sublime_text.desktop。如下：

[Desktop Entry]Version=1.0Type=ApplicationName=Sublime TextGenericName=Text EditorComment=Sophisticated text editor for code, markup and proseExec=/home/zhouyong/software/sublime_text_3/sublime_text %FTerminal=falseMimeType=text/plain;Icon=/home/zhouyong/software/sublime_text_3/Icon/128x128/sublime-text.pngCategories=TextEditor;Development;StartupNotify=trueActions=Window;Document;[Desktop Action Window]Name=New WindowExec=/home/zhouyong/software/sublime_text_3/sublime_text -nOnlyShowIn=Unity;[Desktop Action Document]Name=New FileExec=/home/zhouyong/software/sublime_text_3/sublime_text --command new_fileOnlyShowIn=Unity;

8. 复制改文件至桌面 点击即可打开（可能存在权限问题，右键选择properties修改 或者 chmod +x *.desktop）
```
> 参考链接：http://www.sundabao.com/centos-%E5%AE%89%E8%A3%85sublime-text-3/

### Sublime插件安装

+ JSON插件

	```
	cd ~/.config/sublime-text-3/Packages/
 	git clone https://github.com/dzhibas/SublimePrettyJson.git
	```
	
	git地址：https://github.com/dzhibas/SublimePrettyJson
	
+ 安装Package Control插件管理工具

	进入view-> show console， 将下面代码输入进去，然后回车.
	
	```
	import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
	```
	重启sublime，使用ctrl/cmd + shift + p, 既可以看到control.
	
	参考地址：http://www.imjeff.cn/blog/62/
	
+ Terminal插件

	在ctrl+shift+p 选择“install package” 选择"terminal" 回车即可安装。
	
	使用```ctrl+shift+t```打开终端。
	
	

