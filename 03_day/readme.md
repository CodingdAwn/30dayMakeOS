# day 3

## 知识点
- JC: jump if carry, 如果进位标记carry flag是1的话就跳转
- INT 0x13: 磁盘读写
- FLACS.CF: 进位标志 读写磁盘后进位标志会被设置  
  FLACS.CF为1位的寄存器
- JNC: jump if not carry 进位标记为0跳转
- JAE: jump if above or equal 如果大于或等于跳转
- JBE: jump if below or equal 如果小于或等于跳转
- JB: jump if below 如果小于就跳转
- EQU: 相当于#define CYLS EQU 10  ; CYLS=10

## 读写磁盘操作
- AH: 0x02读盘 0x03写盘 0x04校验 0x0c寻道
- AL: 扇区数
- CH: 柱面号&0xff
- CL: 扇区号
- DH: 磁头号 软盘有正反面2个磁头
- DL: 驱动器号 如果有多个软盘的话
- ES:BX 缓冲地址 从软盘中读取的数据装载到内存的哪个位置  
  MOV AL,[ES:BX] 标识ES*16+BX的内存地址 如果ES为0x20那么正好每次移动512个字节 即一个扇区..
  如果指定内存的话 都必须同时指定 段寄存器 默认的话为DS: 可以省略
- 
  
