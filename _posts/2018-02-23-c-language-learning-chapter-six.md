---
title: C语言第六章-printf的用法
layout: post
tags: c
---

## printf 的格式
printf 函数的原型为：
```
#include <stdio.h>

int printf(const char *format, ...);
```
printf 的格式有4种：
1. printf("字符串 \n");
```
#include <stdio.h>
int main(void){
	int printf("Hello World!\n");
	
	return 0;
}
```
2. printf(" 输出控制符 "， 输出参数)；
```
#include <stdio.h>
int main(void){
	int i = 10;
	
	printf("%d\n", i);
	
	return 0;
}
```
3. printf("输出控制符1 输出控制符2...", 输出参数1, 输出参数2, ...);
```
#include <stdio.h>
int main(void){
	int i = 10;
	int j = 3;
	
	printf("%d %d\n", i, j);
	
	return 0;
}
```

## 输出控制符
1. %d: 十进制整型;
2. %ld: 长整型;
3. %md: m指定输出字段的宽度。如果数据位数小于m，则左端补空格，若大于m，则按十几位数输出；
4. %u: 输出无符号整型(unsigned)；
5. %c: 输出字符；
6. %f: 输出用来输出实数，包括单精度和双精度，以小数形式输出。小数最多6位，超过6位四舍五入；
7. %.mf: 输出实数小数点后保留m位；
8. %o: 以八进制整数形式输出；
9. %s: 输出字符串；
10. %x: 以十六进制形式输出整数；

## %x、%X、%#x、%#X 的区别
```
#include <stdio.h>

int main(void){
	int i = 47;

	printf("%x\n", i);
	printf("%X\n", i);
	printf("%#x\n", i);
	printf("%#X\n", i);
	
	return 0;
}
/*
* 2f
* 2F
* 0x2f
* 0X2F
*/
```