UpdateApp
=========

这是一个可以自动更新phonegap android app 的plugin，能显示下载进度条，下载完自动安装。

使用方法：
========
+项目中引入UpdateApp.java,updateAppPlugin.js
+Phongegap配置文件(res->xml->config.xml)添加<plugin name="Update" value="com.apusic.plugin.UpdatePlugin" />
+在你的服务器上放置version.js,插件会自动与该文件进行比对，以便自动更新
+在phonegap的OnDeviceReady事件中即可使用插件了

API:
=========
+window.plugin.updateApp.checkAndUpdate(checkPath) 检查并更新程序 checkPath为你的version.js的访问地址 
+window.plugin.updateApp.getCurrentVerInfo 返回APP当前的versionCode和versionName
+window.plugin.updateApp.getServerVerInfo 返回服务器上APP的versionCode和versionName

version.js
==========
[{'verCode':2,'verName':'1.2.1','apkPath':'http://****.com/your.apk'}]
+verCode  版本代码  int型  程序更新的依据
+verName  版本名称 一般用来填写程序的版本号如1.0 1.1 2.0等
+apkPath  版本对应的APK下载地址，可以放在自己的服务器上，也可以是市场的下载地址

