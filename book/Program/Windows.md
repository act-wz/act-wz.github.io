# Windows

## 实用命令


netstat -a   查看开启了哪些端口,常用netstat -an 

netstat -v   查看正在进行的工作 

netsh 查看或更改本地网络配置情况

winver 弹出一个窗口显示版本信息（内存大小、系统版本、补丁版本、计算机名）

ren 原文件名　新文件名 		重命名文件名

del /S /Q 目录 或用：rmdir /s /Q 目录 /S删除目录及目录下的所有子目录和文件。
同时使用参数/Q 可取消删除操作时的系统确认就直接删除。

move 盘符路径要移动的文件名　存放移动文件的路径移动后文件名 移动文件,用参数/y将取消确认移动目录存在相同文件的提示就直接覆盖 

copy 路径文件名1　路径文件名2 /y 复制文件1到指定的目录为文件2，用参数/y就同时取消确认你要改写一份现存目录文件 

xcopy 要复制的文件或目录树　目标地址目录名 复制文件和目录树，用参数/Y将不提示覆盖相同文件 

dir 查看文件，参数：/Q显示文件及目录属系统哪个用户，/T:C显示文件创建时间，/T:A显示文件上次被访问时间，/T:W上次被修改时间 

![命令](./img/bat_cmd.png)