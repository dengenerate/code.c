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



#include<stdio.h>
int main(void)
{
	int num;
	float price, value, commission1,commission2;
	printf("输入购股数量: ");
	scanf_s("%d", &num);
	printf("输入每股单价: ");
	scanf_s("%f", &price);
	value = num * price;
	if (value < 2500.0f) {
		commission1 = 30.0f + 0.017f * value;
	}
	else if (value < 6250.0f) {
		commission1 = 56.0f + 0.0066f * value;
	}
	else if (value < 20000.0f) {
		commission1 = 76.0f + 0.0034f * value;
	}
	else if (value < 50000.0f) {
		commission1 = 100.0f + 0.0022f * value;
	}
	else if (value < 500000.0f) {
		commission1 = 155.0f + 0.0011f * value;
	}
	else {
		commission1 = 255.0f + 0.0009f * value;
	}
	if (commission1 < 39) commission1 = 39;
	//竞争对手 
	if (num < 2000) {
		commission2 = 33.03f * num;
	}
	else {
		commission2 = 33.02f * num;
	}
	printf("你的佣金是: $%.2f ,竞争对手的佣金是: $%.2f", commission1, commission2);
	return 0;

}


#include<stdio.h>
int main(void)
	{
		float x;
		printf("收入为:");
		scanf_s("%f", &x);
		if (x <= 750)
		{
			printf("税金=%.2f\n", x * 0.01);
		}
		else if (x <= 2250)
		{
			printf("税金=%.2f\n", 7.5 + (x - 750) * 0.02);
		}
		else if (x <= 3750)
		{
			printf("税金=%.2f\n", 37.50 + (x - 2250) * 0.03);
		}
		else if (x <= 5250)
		{
			printf("税金=%.2f\n", 82.50 + (x - 3750) * 0.04);
		}
		else if (x <= 7000)
		{
			printf("税金=%.2f\n", 142.50 + (x - 5250) * 0.05);
		}
		else if (x > 7000)
		{
			printf("税金=%.2f\n", 230.00 + (x - 7000) * 0.06);
		}
		return 0;
	}
	
	
	
	#include<stdio.h>
int main(void)
{
	printf("Enter the first 11 dights of a UPC:");
	int x1, x2, x3, x4, x5, x6, x7, x8, x9, x10, x11, x12;
	scanf_s("%1d%1d%1d%1d%1d%1d%1d%1d%1d%1d%1d%1d", &x1, &x2, &x3, &x4, &x5, &x6, &x7, &x8, &x9, &x10, &x11, &x12);
	int y;
	y = 9 - ((x1 + x3 + x5 + x7 + x9 + x11) * 3 + (x2 + x4 + x6 + x8 + x10) - 1) % 10;
	if (y == x12)
		printf("VALID\n");
	else printf("NOT VALID\n");
	return 0;
}



#include<stdio.h>
int main(void)
{
	int q, w, e, r, max1, min1, max2, min2, max, min;
	printf("Enter four integers:");
	scanf_s("%d%d%d%d", &q, &w, &e, &r);
	if (q > w) {
		min1 = w;
		max1 = q;
	}
	else {
		min1 = q;
		max1 = w;
	}
	if (e > r) {
		min2 = r;
		max2 = e;
	}
	else {
		min2 = e;
		max2 = r;
	}
	if (min1 > min2)
	{
		min = min2;
	}
	else {
		min = min1;
	}
	if (max2 > max1) {
		max = max2;
	}
	else {
		max = max1;
	}
	printf("Largest:%d\n", max);
	printf("Smallest:%d\n", min);
	return 0;
}


#include<stdio.h>
int main(void)
{
	int x1, x2, y1, y2, z1, z11, z2, z22;
	printf("Enter first date (mm/dd/yy):");
	scanf_s("%d/%d/%1d%1d", &x1, &y1, &z1, &z11);
	printf("Enter second date (mm/dd/yy):");
	scanf_s("%d/%d/%1d%1d", &x2, &y2, &z2, &z22);
	if (x1 > x2)
	{
		printf("%d/%d/%1d%1d is earlier than %d/%d/%1d%1d\n", x1, y1, z1, z11, x2, y2, z2, z22);
	}
	else if (x1 < x2) {
		printf("%d/%d/%1d%1d is earlier than %d/%d/%1d%1d\n", x2, y2, z2, z22, x1, y1, z1, z11);
	}
	else if (x1 == x2)
		if (y1 > y2) {
			printf("%d/%d/%1d%1d is earlier than %d/%d/%1d%1d\n", x1, y1, z1, z11, x2, y2, z2, z22);
		}
		else if (y1 < y2) {
			printf("%d/%d/%1d%1d is earlier than %d/%d/%1d%1d\n", x2, y2, z2, z22, x1, y1, z1, z11);
		}
		else if (y1 == y2)
			if ((10 * z1 + z11) > (10 * z2 + z22)) {
				printf("%d/%d/%1d%1d is earlier than %d/%d/%1d%1d\n", x1, y1, z1, z11, x2, y2, z2, z22);
			}
			else if ((10 * z1 + z11) < (10 * z2 + z22)) {
				printf("%d/%d/%1d%1d is earlier than %d/%d/%1d%1d\n", x2, y2, z2, z22, x1, y1, z1, z11);
			}
			else {
				printf("%d/%d/%1d%1d is earlier than %d/%d/%1d%1d\n", x1, y1, z1, z11, x2, y2, z2, z22);
			}
	return 0;
}


#include<stdio.h>
int main(void)
{
	int x;
	printf("Enter a two-dight number:");
	scanf("%d",&x);
	if(x<0)
	{
		printf("输入错误\n");
	}
	else if(x<=59){
		printf("Letter grade:F\n");
	}
	else if(x<=69){
		printf("Letter grade:D\n");
	}
	else if(x<=79){
		printf("Letter grade:C\n");
	}
	else if(x<=89){
		printf("Letter grade:B\n");
	}
	else if(x<=100){
		printf("Letter grade:A\n");
	}
	return 0;
}

#include <stdio.h>
void main()
{
	int h,m,hbak;
	printf("Enter a 24-hour time:");
	scanf("%d:%d",&h,&m);
	hbak=h;
	if(h>12)
		h=h%12;
	printf("Equivalent 12-hour time:%d:%d %s\n",h,m,hbak>12?"PM":"AM");
}

#include <stdio.h>
void main()
{
	float commission ,value;
	printf("Enter value of trade:");
	scanf("%f",&value);
	if(value<2500.00f)
		commission=30.00f+0.017f*value;
	else if(value<6250.00f)
		commission=56.00f+0.0066f*value;
	else if(value<20000.00f)
		commission=76.00f+0.0034f*value;
	else if(value<50000.00f)
		commission=100.00f+0.0022f*value;
	else if(value<500000.00f)
		commission=155.00f+0.0011f*value;
	else 
		commission=255.00f+0.0009f*value;
	if(commission<39.00f)
		commission=39.00f;
	printf("Commission :%.2f\n",commission);
}


#include <stdio.h>
void main()
{
	int h,m;
	double time;
	printf("Enter a 24-hour time:");
	scanf("%d:%d",&h,&m);
	time=h+m/100.0;
	if(time<=8.00)
		printf("Closet departure time is %d:%d a.m.,arriving at 10:16 a.m.\n",h,m);
	else if(time<=9.43)
		printf("Closet departure time is %d:%d a.m.,arriving at 11:52 a.m.\n",h,m);
	else if(time<=11.19)
		printf("Closet departure time is %d:%d a.m.,arriving at 1:31 p.m.\n",h,m);
	else if(time<=12.47)
		printf("Closet departure time is %d:%d p.m.,arriving at 3:00 p.m.\n",h,m);
	else if(time<=14.00)
		printf("Closet departure time is %d:%d p.m.,arriving at 4:08 p.m.\n",h,m);
	else if(time<=15.45)
		printf("Closet departure time is %d:%d p.m.,arriving at 5:55 p.m.\n",h,m);
	else if(time<=19.00)
		printf("Closet departure time is %d:%d p.m.,arriving at 9:20 p.m.\n",h,m);
	else if(time<=21.45)
		printf("Closet departure time is %d:%d p.m.,arriving at 11:88 p.m.\n",h,m);
	else
		printf("Closet departure time is %d:%d %s,arriving at 10:16 a.m.\n",h,m,(int)time%12>0?"p.m.":"a.m.");
}


#include <stdio.h>
void main()
{
	int d1,m1,y1,d2,m2,y2;
	double val1,val2;
	printf("Enter first date(mm/dd/yy):");
	scanf("%d/%d/%d",&m1,&d1,&y1);
	printf("Enter second date(mm/dd/yy):");
	scanf("%d/%d/%d",&m2,&d2,&y2);
	val1=y1+m1/10.0+d1/100.0;
	val2=y2+m2/10.0+d2/100.0;
	if(val1<val2)
		printf("%d/%d/%02d is earlier than %d/%d/%02d\n",m1,d1,y1,m2,d2,y2);
	else
		printf("%d/%d/%02d is earlier than %d/%d/%02d\n",m2,d2,y2,m1,d1,y1);
}


#include <stdio.h>
void main()
{
	int ind ,val;
	printf("Enter numerical grade:");
	scanf("%d",&ind);
	val=ind/10;
	if(val<6)
		val='F';
	else if(val<7)
		val='D';
	else if(val<8)
		val='C';
	else if(val<9)
		val='B';
	else val='A';
	printf("Letter grade: %c\n",val);
}



#include <stdio.h>
void main()
{
	int d1,d2;
	printf("Enter a two-digit number:");
	scanf("%1d%1d",&d1,&d2);
	if(d1*10+d2>=20)
		switch(d1)
		{
		case 2:
			if(d2>0) 
				printf("twenty-");
			else
				printf("twenty");
			break;
		case 3:
			if(d2>0)
				printf("thirty-");
			else
				printf("thirty");
			break;
		case 4:
			if(d2>0)
				printf("forty-");
			else
				printf("forty");
			break;
		case 5:
			if(d2>0)
				printf("fifty-");
			else
				printf("fifty");
			break;
		case 6:
			d2>0?printf("sixty-"):printf("sixty");
			break;
		case 7:
			d2>0?printf("seventy-"):printf("seventy");break;
		case 8:
			d2>0?printf("eighty-"):printf("eighty");break;
		case 9:
			d2>0?printf("ninety-"):printf("eighty");break;
		}
	else
		d2=d1*10+d2;
	switch(d2)
	{
	case 0:
		if(d1==0)
			printf("Zero");
		break;
	case 1:
		printf("one");break;
	case 2:
		printf("two");break;
	case 3:
		printf("three");break;
	case 4:
		printf("four");break;
	case 5:
		printf("five");break;
	case 6:
		printf("six");break;
	case 7:
		printf("seven");break;
	case 8:
		printf("eight");break;
	case 9:
		printf("nine");break;
	case 10:
		printf("ten");break;
	case 11:
		printf("eleven");break;
	case 12:
		printf("twelve");break;
	case 13:
		printf("thirteen");break;
	case 14:
		printf("fourteen");break;
	case 15:
		printf("fifteen");break;
	case 16:
		printf("sixteen");break;
	case 17:
		printf("seventeen");break;
	case 18:
		printf("eighteen");break;
	case 19:
		printf("nineteen");break;
	}
	printf("\n");
}


#include <stdio.h>
#define MAX_DIGITS 10
#define MAX_ROWS 3
//定全局数组segments并赋初值,初值依据是资料提供的数码管位段。
char segments[10][7] = { {1,1,1,1,1,1},
	{0,1,1},
	{1,1,0,1,1,0,1},
	{1,1,1,1,0,0,1},
	{0,1,1,0,0,1,1},
	{1,0,1,1,0,1,1},
	{1,0,1,1,1,1,1},
	{1,1,1,0,0,0,0},
	{1,1,1,1,1,1,1},
	{1,1,1,1,0,1,1} };
//定义全局数组,用于存放数码显示数据
char digits[MAX_ROWS][MAX_DIGITS * 4];
//一个显示数字8参考输出。供编程参考
void expalent()
{
	printf(" _ \n");
	printf("|_|\n");
	printf("|_|\n\n");
}
void process_digit(int digit, int position);
void print_digits_array(void);
void clear_digits_array(void);
void main()
{
	clear_digits_array();
	process_digit(4, 0);
	process_digit(9, 1);
	process_digit(1, 2);
	process_digit(9, 3);
	process_digit(0, 4);
	process_digit(1, 5);
	process_digit(4, 6);
	process_digit(6, 7);
	print_digits_array();
}
//清除digits数组中所有元素，即给元素赋值为'\0'
void clear_digits_array(void)
{
	int i, j;
	for (i = 0; i < MAX_ROWS; i++)
	{
		for (j = 0; j < MAX_DIGITS * 4; j++)
			digits[i][j] = '\0';//赋值为字符串结束符
	}
}
void process_digit(int digit, int position)
{
	const int pos_len = 4;
	switch (digit)
	{
	case 0:
	case 8:
	case 9:
		digits[0][pos_len * position + 0] = ' ';
		digits[0][pos_len * position + 1] = '_';
		digits[0][pos_len * position + 2] = ' ';
		digits[0][pos_len * position + 3] = ' ';
		digits[1][pos_len * position + 0] = '|';
		digits[1][pos_len * position + 1] = digit == 0 ? ' ' : '_';
		digits[1][pos_len * position + 2] = '|';
		digits[1][pos_len * position + 3] = ' ';
		digits[2][pos_len * position + 0] = digit == 9 ? ' ' : '|';
		digits[2][pos_len * position + 1] = '_';
		digits[2][pos_len * position + 2] = '|';
		digits[2][pos_len * position + 3] = ' ';
		break;
	case 1:
	case 7:
		digits[0][pos_len * position + 0] = ' ';
		digits[0][pos_len * position + 1] = digit == 1 ? ' ' : '_';
		digits[0][pos_len * position + 2] = ' ';
		digits[0][pos_len * position + 3] = ' ';
		digits[1][pos_len * position + 0] = ' ';
		digits[1][pos_len * position + 1] = ' ';
		digits[1][pos_len * position + 2] = '|';
		digits[1][pos_len * position + 3] = ' ';
		digits[2][pos_len * position + 0] = ' ';
		digits[2][pos_len * position + 1] = ' ';
		digits[2][pos_len * position + 2] = '|';
		digits[2][pos_len * position + 3] = ' ';
		break;
	case 2:
		digits[0][pos_len * position + 0] = ' ';
		digits[0][pos_len * position + 1] = '_';
		digits[0][pos_len * position + 2] = ' ';
		digits[0][pos_len * position + 3] = ' ';
		digits[1][pos_len * position + 0] = ' ';
		digits[1][pos_len * position + 1] = '_';
		digits[1][pos_len * position + 2] = '|';
		digits[1][pos_len * position + 3] = ' ';
		digits[2][pos_len * position + 0] = '|';
		digits[2][pos_len * position + 1] = '_';
		digits[2][pos_len * position + 2] = ' ';
		digits[2][pos_len * position + 3] = ' ';
		break;
	case 3:
		digits[0][pos_len * position + 0] = ' ';
		digits[0][pos_len * position + 1] = '_';
		digits[0][pos_len * position + 2] = ' ';
		digits[0][pos_len * position + 3] = ' ';
		digits[1][pos_len * position + 0] = ' ';
		digits[1][pos_len * position + 1] = '_';
		digits[1][pos_len * position + 2] = '|';
		digits[1][pos_len * position + 3] = ' ';
		digits[2][pos_len * position + 0] = ' ';
		digits[2][pos_len * position + 1] = '_';
		digits[2][pos_len * position + 2] = '|';
		digits[2][pos_len * position + 3] = ' ';
		break;
	case 4:
		digits[0][pos_len * position + 0] = ' ';
		digits[0][pos_len * position + 1] = ' ';
		digits[0][pos_len * position + 2] = ' ';
		digits[0][pos_len * position + 3] = ' ';
		digits[1][pos_len * position + 0] = '|';
		digits[1][pos_len * position + 1] = '_';
		digits[1][pos_len * position + 2] = '|';
		digits[1][pos_len * position + 3] = ' ';
		digits[2][pos_len * position + 0] = ' ';
		digits[2][pos_len * position + 1] = ' ';
		digits[2][pos_len * position + 2] = '|';
		digits[2][pos_len * position + 3] = ' ';
		break;
	case 5:
	case 6:
		digits[0][pos_len * position + 0] = ' ';
		digits[0][pos_len * position + 1] = '_';
		digits[0][pos_len * position + 2] = ' ';
		digits[0][pos_len * position + 3] = ' ';
		digits[1][pos_len * position + 0] = '|';
		digits[1][pos_len * position + 1] = '_';
		digits[1][pos_len * position + 2] = ' ';
		digits[1][pos_len * position + 3] = ' ';
		digits[2][pos_len * position + 0] = digit == 5 ? ' ' : '|';
		digits[2][pos_len * position + 1] = '_';
		digits[2][pos_len * position + 2] = '|';
		digits[2][pos_len * position + 3] = ' ';
		break;
	}
}
void print_digits_array(void)
{
	printf("%s\n", digits[0]);
	printf("%s\n", digits[1]);
	printf("%s\n", digits[2]);
	printf("\n");
}

