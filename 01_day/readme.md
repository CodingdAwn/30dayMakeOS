## day 1

### 工具的使用
- asm.bat 执行汇编器 再生成一个img镜像  
- run.bat 直接使用qemu虚拟机打开镜像文件  

### 知识点
- 关键字使用大写或者小写都可以  
- DB: data byte 写入一个字节  
- DW: data word 2个字节  
- DD: data double-word 4个字节  
- ;用于注释  
- $是当前已输出的字节数  
- RESB: 填0  
- boot sector: 启动区 软盘第一个扇区为启动区  
  512字节为一个扇区 软盘大小为1440KB 故有2880个扇区  
  启动区最后两个字节固定为 55 AA  
- IPL: initial program loader  
