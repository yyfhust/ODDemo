##功能说明
- 操作系统段式存储管理的简单实现
- 效果为利用段式存储的方式在屏幕上进行输出


##使用说明
- bochsrc为bochs配置文件
- pm.inc为所需要的头文件
- demo2.asm为源文件
- a.img是利用bximage生成的软盘镜像

###bochs使用
- 切换到当前目录，直接使用bochs命令即可启动bochs
- bochs会自动在当前目录下寻找bochsrc配置文件

1. 启动bochs

    ```
    # wangyuhao @ wangyuhaodeMBP in /Volumes/Transcend/code/OSDemo/demo1 on git:master x [23:21:30]
     ➜ bochs
    ========================================================================
                           Bochs x86 Emulator 2.6.8
                    Built from SVN snapshot on May 3, 2015
                      Compiled on Jan 25 2017 at 10:35:32
    ========================================================================
    00000000000i[      ] BXSHARE not set. using compile time default '/usr/local/share/bochs'
    00000000000i[      ] reading configuration from bochsrc
    ------------------------------
    Bochs Configuration: Main Menu
    ------------------------------
    
    This is the Bochs Configuration Interface, where you can describe the
    machine that you want to simulate.  Bochs has already searched for a
    configuration file (typically called bochsrc.txt) and loaded it if it
    could be found.  When you are satisfied with the configuration, go
    ahead and start the simulation.
    
    You can also start bochs with the -q option to skip these menus.
    
    1. Restore factory default configuration
    2. Read options from...
    3. Edit options
    4. Save options to...
    5. Restore the Bochs state from...
    6. Begin simulation
    7. Quit now
    
    Please choose one: [6] 6
    ```

2. 进行调试
    
    ```
    Please choose one: [6] 6
    00000000000i[      ] installing sdl module as the Bochs GUI
    00000000000i[SDL   ] maximum host resolution: x=2560 y=1600
    
    00000000000i[      ] using log file bochsout.txt
    Next at t=0
    (0) [0x0000fffffff0] f000:fff0 (unk. ctxt): jmpf 0xf000:e05b          ; ea5be000f0
    <bochs:1> c
    ```
    - c命令的含义是继续运行程序直到遇到断点


###运行截图

- 在屏幕右方打印出红色的p
![运行截图](https://lh3.googleusercontent.com/-E9ctV_eT-ms/WKcadvbnnsI/AAAAAAAAAC0/GExpvmaN9ws/I/%25255BUNSET%25255D.png)

