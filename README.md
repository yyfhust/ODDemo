##两个操作系统小Demo
###bochs安装
[bochs下载地址](https://nchc.dl.sourceforge.net/project/bochs/bochs/2.6/bochs-2.6.tar.gz)

- 解压后进入目录

```
./configure --enable-debugger --enable-disasm -with-sdl(mac)
./configure --enable-debugger --enable-disasm (linux)
(后面的选项会打开调试功能)

sudo make $$ make install
```

###利用bximage生成软盘
- bochs自带bximage工具可用来生成软盘


```
========================================================================
                                bximage
  Disk Image Creation / Conversion / Resize and Commit Tool for Bochs
         $Id: bximage.cc 12690 2015-03-20 18:01:52Z vruppert $
========================================================================

1. Create new floppy or hard disk image
2. Convert hard disk image to other format (mode)
3. Resize hard disk image
4. Commit 'undoable' redolog to base image
5. Disk image info

0. Quit

Please choose one [0] 1
```

- 选择fd生成软盘


```
Create image

Do you want to create a floppy disk image or a hard disk image?
Please type hd or fd. [hd] fd
```

- 选择软盘大小(选择默认大小即可)

```
Choose the size of floppy disk image to create, in megabytes.
Please type 160k, 180k, 320k, 360k, 720k, 1.2M, 1.44M, 1.68M, 1.72M, or 2.88M.
 [1.44M]
```

- 软盘名称 默认为a.img

```
What should be the name of the image?
[a.img]
```

- 生成软盘后，可用dd命令将内容写人软盘

```
 dd if=test.bin of=a.img bs=512 count=1 conv=notrunc
 
 参数:
 if为input file :输入文件
 of为output file :输出文件
```

