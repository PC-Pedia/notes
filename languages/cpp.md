# Cpp

[Inheritance](https://www.tutorialspoint.com/cplusplus/cpp_inheritance.htm)

## Debug

Using `gdb` http://users.ece.utexas.edu/~adnan/gdb-refcard.pdf

- `b` - Puts a breakpoint at the current line
- `d N` - Deletes breakpoint number N
- `info break` - list breakpoints
- `c` - Continues running the program until the next breakpoint or error
- `r` - Runs the program until a breakpoint or error
- `f` - Runs until the current function is finished
- `s` - Runs the next line of the program
- `n` - Like s, but it does not step into functions
- `p var` - Prints the current value of the variable "var"
- `bt` - Prints a stack trace
- `u` - Goes up a level in the stack
- `d` - Goes down a level in the stack
- `q` - Quits gdb

```sh
(gdb) set disassembly-flavor intel
(gdb) disas main
(gdb) b *0x080493ef //break point
(gdb) print/x $esp //(show contents of the ESP-register in hexadecimal)
$1 = 0xabcdef10
(gdb) x/24w $esp //(examine memory: 24 words starting from the address in ESP)
0xabcdef10: 0x00000000 0x00000000
(gdb) x/i $eip //(examine instruction at the address contained in EIP)
0x80403020: movl $0x0,%eax
(gdb) continue //(c/continue running)

(gdb) x/300wx \$esp

(gdb) x/16bx foo
0x400604 <foo>:0x55    0x48    0x89    0xe5    0x53    0x48    0x81   0xec
(gdb) set ((unsigned char *)foo)[6] = 0x85
(gdb) x/16bx foo
0x400604 <foo>:0x55    0x48    0x89    0xe5    0x53    0x48    0x85   0xec

(gdb) p $rax
$1 = 3671197290184
(gdb) set $rax = $rbx
(gdb) p $rax
$2 = 0
```

## Pointer

- `*(adr)` deref_func = return val inside adr
- `&(val)` ref_func = return adr pointer of the val
- `&(*(adr))` = get back adr

```cpp
int x = 1111;
int* adr = &x; // 0x010fffff
int& deadr = *adr; //1111


&&x //err
**x //err

&*adr // 0x010fffff
&*deadr //err

*&adr // 0x010fffff
*&deadr  //1111
```

## Naming Conv

- foo is public
- \_bar is protected
- \_\_baz is private
