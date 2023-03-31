# Linux学习

学习视频[【小白入门 通俗易懂】2021韩顺平 一周学会Linux_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Sv411r7vd?p=1&vd_source=eeae710419e6a12e4f563be8a991eec7)

## 【准备工作】

### 一、准备学习环境

1. 安装VMware

2. 在VMware上创建虚拟机（[【小白入门 通俗易懂】2021韩顺平 一周学会Linux_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Sv411r7vd?p=6&vd_source=eeae710419e6a12e4f563be8a991eec7)）

   虚拟机及母机之间的关系：

   ![image-20220703231923940](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220703231923940.png)

   安装虚拟机时网络连接的三种方式（视频007）：

   (1) 桥接模式，虚拟系统可以和外部系统通讯，但是容易造成IP冲突。（因为这意味着它需要占用外部网段的IP。假设一个教师网段192.168.0.这个网段中有二百个学生在使用电脑，若每个学生的电脑中都在使用虚拟系统，那么总共需要的IP就是400个，但是192.168.0.这个网段只能够提供255个IP，这样就造成了IP冲突。）

   (2) NAT模式，即网络地址转换模式。虚拟系统可以和外部系统通讯，不造成IP冲突。（内部会产生成一个虚拟的网卡提供IP）

   (3) 主机模式，独立的系统。

   ![image-20220703230953884](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220703230953884.png)

​		

3. 安装CentOS 7系统（视频006）

### 二、虚拟机拓展学习

#### 1. 虚拟机克隆

​	如果已经安装好了一个Linux虚拟机系统，还想要更多的，没有必要重新安装，只需要克隆就可以

##### 1）方法

* 方式1：直接拷贝一份安装好的虚拟机文件，拷贝好之后使用VMware打开：

![image-20220703235039282](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220703235039282.png)





* 方式2：使用VMware的克隆操作（注意克隆是要先关闭被克隆的Linux系统）

##### 2）操作步骤：

![image-20220704001558037](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704001558037.png)

![image-20220704001431624](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704001431624.png)

![image-20220704001508787](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704001508787.png)

![image-20220704001628972](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704001628972.png)

![image-20220704001709120](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704001709120.png)

![image-20220704001740011](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704001740011.png)



#### 2.虚拟机快照

##### 1）使用位置：

![image-20220704001837542](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704001837542.png)

##### 2）介绍：

![image-20220704001306215](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704001306215.png)



#### 3.虚拟机的迁移和删除

![image-20220704004704920](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704004704920.png)

![image-20220704004802034](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704004802034.png)

注意：移除不是真正的删除。

#### 4.VMtools

##### 1）介绍

1. vmtools 安装后，可以让我们在Windows下更好的管理vm虚拟机。
2. 可以设置Windows和CentOS的共享文件夹。

##### 2）vmtools安装步骤

[【小白入门 通俗易懂】2021韩顺平 一周学会Linux_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Sv411r7vd?p=11&vd_source=eeae710419e6a12e4f563be8a991eec7)

[(56条消息) centos7安装 VMTools（安装VMware Tools显示灰色正确解决办法）_OceanStar的学习笔记的博客-CSDN博客_centos7安装vmware tools灰色](https://blog.csdn.net/zhizhengguan/article/details/112061061#:~:text=CentOS7安装VMware Tools 的具体步骤如下： 一、准备工作 点击 VMware 菜单栏[虚拟机]，选择[ 安装VMware,在虚拟机中，以 root 身份登录客... 百度了一天，重新 安装 了vm，在csdn逛了又逛，结合无数篇大神文章，最后自己成功琢磨出了真正能点亮 灰色 按钮的方法。)

## 【基础篇】

### 一、Linux目录结构

#### 1）基本介绍

​        Linux的文件系统是采用级层式的梳妆目录结构，在此结构中的最上层时根目录“/“，然后在此目录下创建其他的目录。（Linux中一切皆文件）

#### 2）具体的目录结构

![image-20220704170723596](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704170723596.png)

![image-20220704170925939](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704170925939.png)

![image-20220704170951118](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704170951118.png)

![image-20220704171044445](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704171044445.png)注意：

* /lost+found一般在图形界面看不到，用终端转到根目录查看。 

* / selinux[security-enhanced linux]这个目录如果在安装系统的时候没有使用安全政策是没                                有的。

* 安装软件时最好把文件先放在/opt目录中，便于其他用户来查找。

### 二、远程登陆Linux

#### 1）为什么要远程登陆Linux

![image-20220704173545906](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704173545906.png)

#### 2）操作方法

使用Xshell软件（远程登陆）和Xftp软件（远程文件传输）。

[【小白入门 通俗易懂】2021韩顺平 一周学会Linux_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Sv411r7vd?p=15&spm_id_from=pageDriver&vd_source=eeae710419e6a12e4f563be8a991eec7)

### 三、vi和vim

#### 1）基本介绍

Linux系统会内置vi文本编辑器（有点类似于Windows的记事本）。

Vim具有程序编辑的能力，可以看作是vi的增强版有语法的高亮提示，方便程序设计。同时具有代码补全、编译以及错误跳转等方便编程的功能，功能十分丰富，在程序员中被广泛使用。

#### 2）Vi和Vim常用的三种模式

![image-20220704174716556](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704174716556.png)

理解：

* 正常模式不能够敲代码，只能进行一些上述的特殊操作来处理文件。
* 插入模式相当于编辑模式。
* 命令行模式可以进行读取、写入退出等操作。
* 一般的流程是vim + 文件名创建或者打开一个文件，进入默认模式，然后输入i或者I等任意字母之后进入插入模式。在编辑完成之后按：进入命令行模式，对文件完成指令。

#### 3）各种模式的相互切换

![image-20220704180956481](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704180956481.png)

#### 4）Vi和Vim快捷键

![image-20220704181156793](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704181156793.png)

注意：1，2，5是正常模式下的快捷键

* ctrl-e 移动页面

* ctrl-f 上翻一页

* ctrl-b 下翻一页

* ctrl-u 上翻半页

* ctrl-d 下翻半页

* dw 删除一个字(word)

一般来说只需要用到这些，其他在需要时可以上网查找[VIM常用快捷键 - markleaf - 博客园 (cnblogs.com)](https://www.cnblogs.com/markleaf/p/7808817.html)

![image-20220704183054078](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704183054078.png)

### 四、关机&重启

![image-20220704183324693](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704183324693.png)

### 五、用户登录和注销

![image-20220704184009081](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704184009081.png)

* su 与su - 的区别：su 是不改变当前变量。su - 是切换到用户的变量。su只能获得root的执行权限，不能获得环境变量，而su - 是切换到root并获得root的环境变量及执行权限.

### 六、用户管理

#### 1）基本介绍

![image-20220704184929304](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704184929304.png)

#### 2）添加用户（在root用户下执行）

![image-20220704185358872](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220704185358872.png)

添加用户时如果没有指定组那么会默认把该用户放到跟该用户相同名的组中。

#### 3） 指定/修改密码

* 基本语法： passwd + 用户名。

#### 4）删除用户（在root用户下执行）

（1）基本语法： userdel

（2）应用案例：

* 删除用户但是保留家目录。（userdel + 用户名）

* 删除用户及其家目录。（userdel -r + 用户名）

（3）一般情况下建议保留家目录。

#### 5）查询用户信息指令

基本语法：id + 用户名，当用户不存在时，返回无此用户

![image-20220705165149362](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220705165149362.png)

#### 6）切换用户

##### （1）介绍

在操作Linux中，如果当前用户的权限不够，可以通过su - 指令切换到高权限用户，帮你如root用户。

##### （2）基本语法

su -  +  用户名

##### （3）细节说明

* 从权限高的用户切换到权限低的用户不需要输入密码  

* 使用exit或者logout返回到上一个用户，返回之后若是再用exit或者logout则会退出系统。（在图形界面使用exit和logout退出系统是无效的，只会退出终端。需要在运行级别3下才有效）

#### 7）查看当前用户

基本语法：whoami和who am i（用法不同）

whoami 命令和 who am i 命令是不同的 2 个命令，前者用来打印当前执行操作的用户名，后者则用来打印登陆当前 Linux 系统的用户名。

#### 8）用户组

##### （1）介绍

用于对有同一共性（权限）的用户进行统一的管理。

##### （2）增加组

指令：groupadd  +   组名。

##### （3）删除组

指令：groupdel   +   组名。

##### （4）增加用户时直接加上组

指令：useradd -g  +   用户组名   +    用户名。

##### （5）修改用户的组

指令：usermod -g   +    用户组名   +   用户名。

#### 9）用户和组相关文件

![image-20220707163402044](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220707163402044.png)

（使用vim或vi访问）

### 七、指定运行级别

![image-20220707163910027](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220707163910027.png)

指定默认运行级别：在centos7以前，在/etc/inittab文件中进行修改。在centos7之后进行了简化。

具体操作：

* 查看当前默认运行级别：systemctl get-default
* 设置当前默认运行级别：systemctl set-default multi-user.target（设置为运行级别3）/graphical.target（设置为运行级别5）.

### 八、找回root密码

不同版本找回root密码的方法有点区别，此处讲解centos7及以后的版本。

#### 步骤：

![image-20220707180157932](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220707180157932.png)

![image-20220707180256676](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220707180256676.png)

![image-20220707180237075](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220707180237075.png)

![image-20220707180349702](z)

### 九、帮助指令

![image-20220709101348062](C:\Users\50687\AppData\Roaming\Typora\typora-user-images\image-20220709101348062.png)

### 十、文件目录类指令

##### 1）pwd指令

基本语法：pwd 

功能描述：显示当前工作目录的绝对路径。

##### 2）ls指令

基本语法：ls  [选项] [目录或者文件]

功能描述：列出该目录（或当前目录）下的所有的文件和目录。

常用选项：

* -a ： 显示当前目录的所有内容信息，包括隐藏的。（在Linux下隐藏文件是以.开头的。）

* -l ：以列表的方式显示信息。
* -la（-al）：以列表的方式显示所有的信息。（即选项可以叠加）

##### 3）cd指令

基本语法: cd [参数（路径）]

功能描述：切换到指定目录。其中，cd和cd ~表示回到自己的家目录。例如，你是root用户，则cd指令回到/root。cd..表示回到该目录的上一级目录

理解相对路径与绝对路径：

* 使用绝对路径到root目录：cd /root。
* 使用相对路径到root目录，假设此时是在/home/tom：cd ../../root。（../表示回到上一级目录）

##### 4）mkdir指令

基本语法：mkdir [选项]  +  要创建的目录。

功能描述：用于创建目录。

常用选项：-p  ：用于创建多级目录。

实例：

* 创建一个目录/home/dog。     mkdir /home/dog
* 创建多级目录/home/animals/dog.     mkdir /home/animals/dog

##### 5）rmdir指令

基本语法：rmdir [选项]  +  要删除的空目录。

功能描述：删除空目录。

使用细节：

* rmdir删除的是空目录，如果目录下有内容是时无法删除。
* 如果要删除非空目录，因该使用rm -rf  +  要删除的目录（表示递归、强制的删除）（小心谨慎）。

##### 6）touch指令

基本语法：touch  +  文件名称。

功能描述：创建一个空文件。（也可以使用vim，但是vim使用后会直接打开）

##### 7）cp指令

基本语法：cp [选项]  +  source  +   dest

功能描述：拷贝文件到指定目录。

常用选项：-r ：递归复制整个文件夹。

应用实例：

* 案例1：将/home/hello.txt拷贝到/home/bbb目录下(假设此时在home目录下，hello.txt和/bbb在home目录中)       

  cp hello.txt /bbb

* 案例2：递归复制整个文件夹（将home目录下的/bbb以及其下的文件全部复制到/opt目录下）

  cp -r /home/bbb/opt

使用细节：强制覆盖不提示的方法：使用/cp指令（）与cp指令与用法相同。

##### 8）rm指令

基本用法：rm [选项]  +  要删除的文件或目录（要删除目录选项必须有-r）。

功能描述：移除文件或目录。

常用选项：

* -r  ： 递归删除整个文件夹
* -f  ： 强制删除不提示
* -rf  ： 以上两者结合

注意：文件一旦通过rm命令删除则无法恢复，因此使用时应格外小心。

##### 9）mv指令

基本语法：

* mv  +  oldNameFile  +  newNameFile
* mv  +  被移动的文件  +  目标目录

功能描述：移动文件或目录或重命名。

##### 10）cat指令

基本语法：cat [选项]  +  要查看的文件

功能描述：查看文件（相比于vim，cat指令只能查看不能修改，因此更安全，在查看一些重要的文件时，建议使用cat指令）

常用选项：-n ：显示行号

使用细节：为了使用方便，一般在后面会带上管道命令（指在完成上一指令之后交给下一指令） ： |more，带上管道命令后，打开文件就可以进行如下的操作：

![image-20220709142058148](Linux%E5%AD%A6%E4%B9%A0.assets/image-20220709142058148.png)

##### 11）more指令

基本语法：more  +  要查看的文件

操作说明：![image-20220709142414246](Linux%E5%AD%A6%E4%B9%A0.assets/image-20220709142414246.png)

功能描述：more指令是一个基于VI编辑器的文本过滤器，它会以全屏幕的方式按页显示文本文件的内容。more指令中内置了若干快捷键（用于交互）。

使用细节：一般cat和more组合使用更为方便。

##### 12）less指令

基本语法：less  +  要查看的文件。

功能描述：less指令用来分屏查看文件内容，它的功能与more指令类似，但是比起more指令更加强大，支持各种显示终端。less指令在显示文件内容时，并不是一次将整个文件加载后才显示，而是根据显示需要加载内容，对于显示大型文件具有极高的效率

操作说明：![image-20220709143506220](Linux%E5%AD%A6%E4%B9%A0.assets/image-20220709143506220.png)

##### 13）echo指令

基本语法：echo [选项] [输出内容]

功能描述：输出内容到控制台。

应用实例：

* 使用echo指令输出环境变量，比如输出$HOSTNAME和$PATH
  ![image-20220710114829284](Linux%E5%AD%A6%E4%B9%A0.assets/image-20220710114829284.png)

* 使用echo指令输出“hello world”
  ![image-20220710114923136](Linux%E5%AD%A6%E4%B9%A0.assets/image-20220710114923136.png)

##### 14）head指令

基本语法：

* head  +  文件（查看文件的头十行内容）

* head -n 5  +  文件（查看文件头5行内容，5可以是任意行数）

功能描述：用于显示文件的开头部分内容，默认情况下head指令显示文件的前10行内容。

##### 15）tail指令

基本语法：

* tail  +  文件（查看文件尾十行内容）
* tail -n 5  +  文件（查看文件尾5行内容，5可以是任意行数）

* tail -f  +  文件（实时追踪该文档的所有更新）（ctrl +  c退出）

功能描述：用于输出文件中尾部的内容，默认情况下tail指令显示文件的前10行内容。

##### 16）>指令和>>指令

基本语法：

* ls -l >  +  文件（列表的文件写入文件中（覆盖写））

* ls -al >>  +  文件（列表的文件追加到文件的末尾）
* cat  +  文件1 >  +  文件2（将内容1的内容覆盖到内容2）
* echo “内容” >>  +  文件

功能描述：>输出重定向，>>追加。

使用细节：若追加或者重定向的文件不存在，则会自动创建。

##### 17）ln指令

基本语法：ln -s [源文件或目录] [软链接名]

功能描述：给源文件创建一个软链接，类似于Windows里面的快捷方式，主要存放了链接其他文件的路径。

使用细节：

* 当使用pwd指令查看目录时，看到的仍然是软连接所在的目录。

* cd + 软链接之后会到该软链接所指向的位置。

##### 18)history指令

基本语法：

* history（查看执行过的所有命令）

* history 10（查看最近十次执行的命令）
* !5（执行执行过的所有命令中编号为5的指令）

功能描述：查看已经执行过的历史命令，也可以执行历史命令

### 十一、时间日期类指令

##### 1）date指令

基本用法：

* date （显示当前时间）
* date +%Y（显示当前年份）
* date +%m（显示当前月份）
* date +%d（显示当前是哪一天）
* date "+%Y-%m-%d %H:%M:%S"（其中的-和：为分隔符）（里面的元素可以删减）
* date -s  +  字符串时间（设置时间）   例如![image-20220710141559151](Linux%E5%AD%A6%E4%B9%A0.assets/image-20220710141559151.png)

##### 2）cal指令

基本用法：

* cal （直接cal显示本月日历）

* cal  +  年份（显示该年的日历）

### 十二、搜索查找类

##### 1）find指令

基本语法：find [搜索范围] [选项]

选项说明：![image-20220710142039319](Linux%E5%AD%A6%E4%B9%A0.assets/image-20220710142039319.png)

功能描述：将从指定目录向下递归地遍历其各个子目录，将满足条件的文件或目录显示在终端。 

应用案例：
![image-20220710142814698](Linux%E5%AD%A6%E4%B9%A0.assets/image-20220710142814698.png)

##### 2）locate指令

![image-20220710143534132](Linux%E5%AD%A6%E4%B9%A0.assets/image-20220710143534132.png)

##### 3）which指令

基本用法：which  +  一个指令

功能描述：查看一个指令在那个目录下

##### 4）grep指令和管道符号|（用法类似于之前所学的more）

![image-20220720155825845](Linux%E5%AD%A6%E4%B9%A0.assets/image-20220720155825845.png)

### 十三、解压和压缩类指令

##### 1）gzip/gunzip指令

![image-20220720160031955](Linux%E5%AD%A6%E4%B9%A0.assets/image-20220720160031955.png)

##### 2）zip/unzip指令

![image-20220720161012021](Linux%E5%AD%A6%E4%B9%A0.assets/image-20220720161012021.png)

##### 3）tar指令

![image-20220720162206404](Linux%E5%AD%A6%E4%B9%A0.assets/image-20220720162206404.png)

注意：-z选项是解压或者压缩。 -C指令是转移到指定目录。

