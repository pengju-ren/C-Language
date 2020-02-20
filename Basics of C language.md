使用GPU进行并行计算

```C
#define _CRT_SECURE_NO_DEPRECATE
```



#### sscanf()函数

作用：从一个字符串中读进与指定格式相符的数据

原型：

```c
int sscanf (const char *str,const char * format,........);
```

sscanf()会将参数str的字符串根据参数format字符串来转换并格式化数据。     成功则返回参数数目，失败则返回0

例子: 

1: 取指定长度的字符串

```c
#include<stdio.h>
#include<string.h>
int main()
{
	char str[100];
	sscanf("12345","%4s",str);
	printf("%s\n",str);
	return 0;
}
```

输出：1234

2:读入字符串

```c

#include<stdio.h>
#include<string.h>
int main()
{
	char str[100];
	sscanf("12345","%s",str);
	printf("%s\n",str);
	return 0;
}

```

输出：12345

```C
#include<stdio.h>
#include<string.h>
int main()
{
 	char str1[100], str2[100], str3[100];
  	gets(str1);
  	sscanf(str1,"%s%s",str2,str3);
  	printf("%s %s\n",str2,str3);
	return 0;
}
```



strcmp()函数

strncmp()函数





**fread()函数**

功能: 用于读取二进文件

声明:

```C
size_t fread （void * ptr ，size_t size ，size_t nmemb ，FILE * stream ）
```

参数:

- **ptr** - 这是指向带有最小尺寸的 *大小\* nmemb* 字节的内存块的指针。
- **size** - 这是要读取的每个元素的大小，以字节为单位。
- **nmemb** - 这是元素的个数，每个元素的大小为尺寸字节。
- **stream** - 这是指向FILE对象的指针，该FILE对象指定了一个输入流。