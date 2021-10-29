# day 2

## 知识点
- ORG: 指定程序起始位置
- JMP: jump
- entry: 只是标签 label 类似goto
- MOV: 赋值语句 MOV AX,0 即AX = 0, MOV源数据和目的数据位数相同
- ADD: 加法指令
- CMP: 比较指令
- JE: 比较跳转指令, 比较结果相等则跳转 否则继续执行下一条指令 jump if equal
- INT: 中断指令 INT 0x10 bios显卡指令
- BIOS: basic input output system
- HLT: cpu睡眠

### 寄存器:
16位寄存器
- AX -> accumulator 累加
- CX -> counter 计数
- DX -> data 数据
- BX -> base 基址
- SP -> stack pointer 栈指针
- BP -> base pointer 基址指针
- SI -> source index  源变址
- DI -> destination index  目的变址

8位寄存器  
- AL,CL,DL,BL,AH,CH,DH,BH 分高低位

32位寄存器  
- EAX,ECX,EDX,EBX,ESP,EBP,ESI,EDI

段寄存器 16位
- ES -> extra segment 附加段
- CS -> code segment 代码段
- SS -> stack segment 栈段
- DS -> data segment 数据段
- FS,GS

### 其他
[]为指定内存 cpu与内存的存取
- MOV WORD [678], 123 内存678-679 设置为123
- MOV BYTE [BX],123 内存[BX寄存器的值] 设置为123 {BX BP SI DI}可用

对于ORG 0x7c00的解释:
- 0x00007c00 -> 0x00007dff为 启动区内容装载地址
- 内存有部分地址是BIOS的地址

### 疑问
- $符号在ORG下 含义有变化？
