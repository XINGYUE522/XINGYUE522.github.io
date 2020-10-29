# 1.申请github账号
参考[这个](https://jingyan.baidu.com/article/86fae346e723303c49121abb.html)
# 2.安装vccode
## 安装
[官网](https://code.visualstudio.com/)下载并安装
## 汉化
安装汉化：按下快捷键ctrl+shift+p，输入搜索configuration display language，选择Install additional languages，安装简体中文汉化包，重启后完成。
# 3.安装git

在Git命令行模式下 输入如下命令，配置username和useremail

```
git config --global user.name "username"
git config --global user.email "example@example.com"
```

输入git config --list，显示user.name和user.email即为成功

输入git config --list，显示user.name和user.email即为成功

# 4.同步电脑段和云端
参考[这个帖子](https://www.cnblogs.com/wgong/p/6914717.html)
***
# 一些指令
拉取云端文件
在Git命令行下输入 git pull

修改本地文件并上传
在本地库文件夹新建一个文件1.txt
1、在Git命令行下输入git status，确认文件变动
2、在Git命令行下输入git add 1.txt(第一次新建文件需输入)
3、在Git命令行下输入git commit -m 1.txt（-m参数取消对文件的描述）
4、在Git命令行下输入git push，即上传至云端


