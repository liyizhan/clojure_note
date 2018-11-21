---
typora-root-url: ./
---

### 一、介绍

Leiningen是Clojure范畴内的项目管理和综合工具，可以类比为Java与maven/ant的关系。目前Clojure有两种工具，一种是Leiningen，另一种是Boot。

为了学习Clojure，有一个合适的工具可以快速帮助入门，一起来学习Leiningen吧~

### 二、下载与安装

1. 进入网址：<https://leiningen.org/>

2. 在Install栏目内根据操作系统下载对应的脚本文件（lein或者lein.bat）

3. 将脚本文件放置在操作系统$PATH环境变量路径下，以便Shell能够找得到它

4. 将脚本文件设置为可执行文件

5. 在Shell中输入“lein”（windows为“lein.bat”）运行脚本文件，它会自己下载自安装文件

![181121A-1](/181121A-1.png)

### 三、启动REPL交互环境

在Shell中输入命令“lein repl”启动一个REPL会话。

![181121A-2](/181121A-2.png)

若Shell当前路径位于lein创建的项目且该项目有指向主函数的，则REPL提示符指向该主函数位于的命名空间。

![181121A-3](/181121A-3.png)

### 四、利用Leiningen创建并运行项目

在Shell中输入命令“lein new app project-name”会在当前路径下创建一个名为project-name的项目，“cd project-name”切换到该项目，输入“lein run”运行该项目，此后将会执行该项目的主函数并打印出“Hello, World!”

![181121A-4](/181121A-4.png)

在“src/project-name”这个项目下，切换路径到“src/project-name”，就可以看到打印出“Hello, World!”的clojure源文件“core.clj”啦。

![181121A-5](/181121A-5.png)

### 五、利用IDEA创建Leiningen项目

由Shell这种方式去创建Leiningen项目还是太慢了，如果能够借助常用的IDE创建，那会省下不少的事。

#### IntelliJ IDEA创建项目的方式：

1. 安装Leiningen插件并重启（安装插件的方式请自行百度啦）

2. 创建IDEA项目（Create New Project）

3. 选择项目类型为Leiningen

4. 选择项目的JDK 版本为1.8并点击next

![181121A-6](/181121A-6.png)

5. 输入新项目名idea-lein-proj并点击finish

![181121A-7](/181121A-7.png)

#### 在IDEA运行项目的方式：

1. 修改idea-lein-proj/src/idea_lein_proj/core.clj中foo函数，将其函数名改为主函数名-main（若已存在-main函数则忽略这一步）

![181121A-8](/181121A-8.png)

2. 在IDEA右上角添加运行配置

![181121A-9](/181121A-9.png)

3. 添加Clojure应用程序运行配置

![181121A-10](/181121A-10.png)

4. 将配置设置为

![181121A-11](/181121A-11.png)

5. 点击apply按钮完成配置，随后在右上角点击运行即可

![181121A-12](/181121A-12.png)

### 六、在IDEA中添加Cursive插件

为了更好地学习Clojure这门语言，有一款强大的IDE提供语法高亮、代码跳转、代码提示等功能是最好不过了，只不过纯净的IDEA对此没有支持，需要自己下载Cursive插件。

同样地，在IDEA中搜索Cursive这个插件并安装，后续提示需要到Cursive官网去获取license以获得授权。Cursive的授权分为收费和非收费的，这里选择non-commercial版本的license，随后将license内容复制到IDEA的Cursive插件中去验证就完成了。

随后，即可享受Cursive带来的Clojure Coding优良体验啦~