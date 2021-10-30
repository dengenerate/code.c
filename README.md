#include<stdio.h>
int main()
{
	int a = 0;
	while (a < 100)
	{
		printf("%d\n", a);
		a++;
	}
	return 0;
}


#include<stdio.h>
int main()
	int Max(int num1, int num2)
{
	if (num1 > num2) return num1;
	else return num2;
}


#include<stdio.h>
int main()
int main()
{
	int a, b,max=0;
	scanf_s("%d%d", &a, &b);
	max = Max(a, b);
	printf("max=%d\n",max);
	return 0;
}
 #include<stdio.h>
#define MAX(M,N) (M>N?M:N)//define 宏的定义
int main()
{
	int m, n, max = 0;
	scanf_s("%d%d", &m, &n);
	max = MAX(m, n);
	printf("max=%d\n", max);
}



int main()
{
	int a = 0;//	~	按（二进制）位取反 4个字节32个比特位	000000000000000000000000   32个零
	int b = ~a;//b有符号的整形												111111111111111111111111  最高位为符号位第一个1
	printf("%d", b);//原码	反码	补码	打印出的是原码  原码符号位不变其他按位取反得到反码，反码加1得到补码        
	return 0;//负数在内存中储存的时候，存的是二进制的补码
}
//11111111111111111111111111补码          正数和负数         有符号数  +1   -1  整形数 32个比特位  规定最高位为符号位
//11111111111111111111111110反码           [1][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][]  1代表它是负数
//10000000000000000000000001原码           [0][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][]   0代表它是正数
//只要是整数，内存中存储的都是二进制的补码    正数 原码补码反码相同   
// 负数：原码       反码                            补码 
//按照正负          原码符号位不变，其它按位取反     反码+1 
//写出的二进制序列
//
//int=signed int    unsigned int 表示没有符号位计算  即永远是正   struct——结构体关键字   union——联合体、
// 共用体
// typedef unsigned int  u_signed; //typedef  类型定义 类型重定义
//	while (i < 5)//unsigned int num1 = 20;//num1和num2类型相同，表示的数一样。
#include<stdio.h>;
int g_val = 2020;
int main()
{
    extern int  g_val;//extern声明外部符号表示可以运用其他文件的函数和数据等，而用static之后则不能用该文件外标记的任何东西。
    printf("g_val=%d\n", g_val);
}




#include <stdio.h>
void test()
{
	static int a = 1;//a变成了一个静态的局部变量 static修饰局部变量，其生命周期变长
	a++;
	printf("a=%d\n", a);
}
int main(void)
{
	int i = 0;
	while (i < 5)
	{
		test();
		i++;
	}
	return 0;
}//#include <stdio.h>                                       
void test()
{
	int a = 1;
	a++;
	printf("a=%d\n", a);
}
int main(void)
{
	int i = 0;
	while (i < 5)
	{
		test();//u_signed num2 = 20;
		i++;
	}
	return 0;
}
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>//	exp1?exp2:exp3   表达式exp1为真的话则整个程序的结果为exp2的，反之则为exp3的
int main()
{
	int a,b;
	int max = 0;
	scanf_s("%d %d", &a, &b);
	if (a > b)   //
		printf("max = %d\n",a); 
	else         //
		printf("max = %d\n",b); 
	return 0;
}
#include<stdio.h>
int main()
{
	int a, b;
	int max = 0;
	scanf_s("%d %d", &a, &b);
	max = (a > b) ? a : b;
	printf("max=%d\n", max = (a > b) ? a : b);
	return 0;
}


#include<stdio.h>计算1+2+3+……+100=？
int main()
{
	/*int w = 1, sum = 0;
	while (w <= 100)
	{
		sum = sum + w;
		printf("sum=%d,w=%d", sum, w);
		w += 1;
		if ((w - 1) % 6 == 0)
			printf(" \n");
		else
			printf("\t");
	}
	printf("\n\nsum=%d\n\n", sum);*/
	int w, sum = 0;
	for (w = 1; w <= 100;)
	{
		sum = sum + w;
		w++;
		printf("sum=%d,w=%d", sum, w);
		if ((w - 1) % 6 == 0)
			printf("\n");
		else
			printf("\t");
	}
	printf("\nsum=1+2+…+100=%d\n", sum);
}

#include<stdio.h>计算不同等级分数的个数以及平均值
int main(void)
{
	int n,i, a, b, c, d, e, grade;
	double sum = 0;
	scanf_s("%d", &n);
	i = a = b = c = d = e = 0;
	FOR:
	{
		scanf_s("%d", &grade);
		sum += grade;
		if (grade >= 120)
			a++;
		else if (grade >= 100)
			b++;
		else if (grade >= 90)
			c++;
		else if (grade >= 80)
			d++;
		else
			e++;
		    i++;
			if (i < n)
				goto FOR;
	}
	printf("A(120~150): %d\n", a);
	printf("B(100~120): %d\n", b);
	printf("C(90~100): %d\n", c);
	printf("D(80~90); %d\n", d);
	printf("E(0~80): %d|n", e);
	printf("average: %.2lf\n", sum/n);
}


#include <stdio.h>
int main()
{
	int m, n;
	for (m = 1; m < 10; m++)
	{
		for (n = 1; n <= m; n++)
			printf("%d*%d=%d\t", m, n, m * n);
		printf("\n");
	}
	return 0;
}



#include <stdio.h>
void main()
{
	int ItemNo, year, month, day;
	double price;
	printf("Enter item nummber:");
	scanf_s("%d", &ItemNo);
	printf("Enter unit price: ");
	scanf_s("%lf", &price);
	printf_s("Enter purchase date (mm/ dd/yyyy): ");
	scanf_s("%d/%d/%d", &month, &day, &year);
	printf("Item\tUnit\tPurchase\n");
	printf("\tPrice\tDate\n");
	Ò»¸öÖÆ±í¿í¶ÈÊÇ8¸ö×Ö·û
	printf("%d\t%7.2f\t%d/%d/%d\n", ItemNo, price, month, day, year);
}




指针
#include<stdio.h>
int main()
{
	int a = 10;//&a取地址  %p打印地址
	int*p = &a;//p是一种存放地址的变量——指针变量     
	printf("%p\n", &a);
	printf("%p\n", p);
	*p=20;//找到p所指向的对象a  *——解引用操作符
	printf("%d\n", a);
	return 0;
	char ch = 'a';
	char* cy = &ch;
	*cy = 'z';
	printf("%d",sizeof(cy));
}



#include<stdio.h>
#include<string.h>
struct Book//结构体  +  复杂对象=我们自己创建的类型   结构体类型
{
	char name[20];//C语言程序设计
	short price;//55
};//；用来结束类型定义
int main()
{
	struct Book b1 = { "C语言程序设计",55 };//书名是字符串
	struct Book* pb = &b1;
	printf("书名:%s\n", b1.name);
	printf("价格:%d\n", b1.price);
	b1.price = 44;
	printf("修改后的价格:%d\n", b1.price);
	printf("%p\n", pb);
	printf("书名:%s\n", (*pb).name);
	printf("价格:%d\n", (*pb).price);//   .操作符       结构体变量  .能够找到成员
	printf("书名:%s\n", pb->name);//       ->c操作符    结构体指针 ->能够找到成员
	printf("价格:%d\n", pb->price);
	strcpy_s(b1.name,"C++");//strcpy   string copy  字符串+拷贝 库函数
	printf("书名:%s\n",b1.name);

	return 0;
}

#include<stdio.h>
int main()
{
	int age;
	scanf_s("%d", &age);
	if (age < 18)
		printf("未成年：不能进入网吧\n");
	else if (age >= 18 && age < 24)
		printf("青年：可以进入网吧\n");
	else if (age >= 24 && age < 60)
		printf("成年：尽量少进入网吧\n");
	else
		printf("老年：不建议进入网吧\n");
	return 0;
}


#include<stdio.h>
int main()
{
	int day;
	scanf_s("%d", &day);
	switch (day)
	{
	        case 1:
			printf("Monday");
			break;
		case 2:
			printf("Thuesday");
			break;
		case 3:
			printf("Wednesday");
			break;
		case 4:
			printf("Thursday");
			break;
		case 5:
			printf("Friday");
			break;
		case 6:
			printf("Saturday");
			break;
		case 7:
			printf("Sunday");
			break;
	 	default://default  表示整形变量与整形常量不符合时，提示它输入错误
	                printf("输入错误");
			break; 				
	}
	return 0;
}

#include <stdio.h>

int main(void)

{

	float a, x, y;
	for (y = 1.5f; y > -1.5f; y -= 0.1f)

	{

		for (x = -1.5f; x < 1.5f; x += 0.05f)

		{

			a = x * x + y * y - 1;

			char ch = a * a * a - x * x * y * y * y <= 0.0f ? '*' : ' ';

			putchar(ch);

		}

		printf("\n");

	}

	return 0;

}

#include <stdio.h>

int main(void)

{

	float a, x, y;
	for (y = 1.5f; y > -1.5f; y -= 0.1f)

	{

		for (x = -1.5f; x < 1.5f; x += 0.05f)

		{

			a = x * x + y * y - 1;

			char ch = a * a * a - x * x * y * y * y <= 0.0f ? '*' : ' ';

			putchar(ch);

		}

		printf("\n");

	}

	return 0;

}


#include<stdio.h>
int main()
{
	int n = 1, m = 2;
	switch (n)
	{
	case 1:
		m++;
	case 2:
		n++;
	case 3:
		switch (n)//switch 可以嵌套使用
		{
			case 1:
				n++;
			case 2:
				m++;
				n++;
				break;
		}
	case 4:
		m++;
			break;
	default:
		printf("输入错误");
	}
	printf("m = % d, n = % d", m, n);
}


#include<stdio.h>
int main()
{
	int area_code;
	scanf_s("%d", &area_code);
	switch (area_code)
	{
	case 229:
		printf("Albany");
		break;
	case 404:
	case 470:
	case 678:
	case 770:
		printf("Atlanta");
		break;
	case 478:
		printf("Macon");
		break;
	case 706:
	case 762:
		printf("Cloumn");
		break;
	case 912:
		printf("Savannah");
		break;
	default:
		printf("Area code not recognized");
		break;
	}

}



#include<stdio.h>
int main(void)
{
	printf("Enterb a number:");
	int y;
	scanf_s("%d", &y);
	printf("The number %d has", y);
	if (y >= 0)
	{
		if (y < 10)
			printf(" 1 ");
		else if(y < 100)
			printf(" 2 ");
		else if(y < 1000)
			printf(" 3 ");
	}
	else
	{
		if (y >- 10)
			printf(" 1 ");
		else if(y >-100)
			printf(" 2 ");
		else if(y >-1000)
			printf(" 3 ");
	}
	printf("dights");
	return 0;
}



#include<stdio.h>
int main(void)
{
	int x, y, q;
	printf("Enter a 24-hour time:");
	scanf_s("%d %d", &x, &y);
	if (x > 12)
	{
		q = x - 12;
		printf("Equivalent 12-hour time:%d:%d PM\n", q, y);
	}
	else if (x <= 12)
	{
		q = x;
		printf("Equivalent 12-hour time:%d:%d AM\n", q, y);
	}
	return 0;
}
