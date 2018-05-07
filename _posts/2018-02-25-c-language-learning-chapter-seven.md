---
title: C语言第七章-scanf的用法
layout: post
tags: c
---

## 概述
函数原型：
```
# include <stdio.h>

init scanf(const char *format, ...);
```

两种格式：
1. scanf("输入控制符", 输入参数 );
```
# include <stdio.h>
int main(void)
{
	int i;
	scanf("%d", &i);
	printf("i = %d\n", i);
	return 0;
}
```

## 注意事项
1. 输入参数顺序和个数一定要一一对应。
2. 输入的数据类型一定要与所需要的数据类型一致。
3. 在使用scanf之前使用printf提示输入。