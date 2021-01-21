
## 执行 `` apt-get update `` 时状态字的意思 
    使用apt-get update它时验证是否需要下载相同的更新索引，如果不是，则不会再次下载相同的更新索引。
    Hit 表示apt检查包列表上的时间戳，这些匹配并没有变化。
    Ign 意味着pdiff索引文件没有变化，它不会再打扰它了。
    Get 意味着检查包列表上的时间戳，有更改并将被下载。



## 无法安装 yum 
    具体描述：使用 `` apt-get install yum ``  安装yum时，报错无法找到包
    
    尝试1：1.apt-get update 更新源
    
    尝试2：2.打开apt配置文件，vi /etc/apt/sources.list 添加国外源

            deb http://archive.ubuntu.com/ubuntu/ trusty main universe 
            restricted multiverse
            p.s deb 表示直接通过.deb文件进行安装和通过源文件的方式进行安装。
    
            3.缺乏 yum 安装所需的依赖，yum需要python及一些python依赖，按照提示进行安装即可。

### 忘记root密码
root 的密码在/etc/shadow 当中，因此可以使用各种可行的方法开机进入 Linux 再去修改。 例如重新启动进入单人维护模式(第十九章)后，系统会主动的给予 root 权限的 bash 接口， 此时再以 passwd 修改密码即可；或以Live CD 开机后挂载根目录去修改 /etc/shadow，将里面的 root 的密码字段清空， 再重新启动后 root 将不用密码即可登入！登入后再赶快以 passwd 指令去设定 root 密码即可。