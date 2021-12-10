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

#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
int main()
{
	int multipy=1;
	int n;
	int i ;
	printf("请输入n的值并计算n的阶乘以及至n的阶乘之和:");
	scanf_s("%d", &n);
	for (i = 1; i <= n; i++)
	{
			multipy = multipy * i;
			printf("%d的阶乘multipy=%d\t", i, multipy);	
			if (i % 4 == 0)
				printf("\n");
	}
	int m, p,q=1;
	int sum = 0;
	for (m = 1; m <= n; m++)
	{
		q = q * m;
		sum = q + sum;
	}
	printf("\nsum=%d\n", sum);
	return 0;
}



#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
int main()
{
	int arr[] = {1,2,3,4,5,6,7,8,8,9,9,9,10};
	int k = 7;
	int sz = sizeof(arr) / sizeof(arr[0]);
	int left = 0;
	int right = sz - 1;
	while (left<=right)
	{
		int mid = (left + right) / 2;
		if (arr[mid] > k)
		{
			right = mid - 1;
		}
		else if (arr[mid] < k)
		{
			left = mid + 1;
		}
		else
		{
			printf("找不到xiabiao%d",mid);
			break;
		}
	}
	if (left > right)
		printf("no");
}



#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<string.h>
#include<windows.h>
#include<stdlib.h>
int main()
{
	char arr1[] = "welcome to new york!!!!!";
	char arr2[] = "########################";
	int left = 0;
	int right = strlen(arr1) - 1;
	while (left <= right)
	{
		arr2[left] = arr1[left];
		arr2[right] = arr1[right];
		left++;
		right--;
		printf("arr2:%s\n", arr2);
		Sleep(3000);//休息三秒
		//system("cls");//执行系统命令的一个函数  cls   清空屏幕  库函数
	}
	return 0;
}



#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<string.h>
#include<windows.h>
#include<stdlib.h>
int main()
{
	int i = 0;
	char password[20] = { 0 };
	for (i = 0; i < 3; i++)
	{
		printf("输入密码:\n");
		scanf("%s", &password);
		if (strcmp(password ,"youarefool74sb")==0)//strcmp比较两个字符串是否相等
		{
			printf("密码正确\n");//  ==不能用来判断两个字符串是否相等
			break;
		}
	}
	if (i == 3)
	{
		printf("请等待3秒、\n");
	}
		//Sleep(3000);//休息三秒
		//system("cls");//执行系统命令的一个函数  cls   清空屏幕  库函数
	return 0;
}



#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<string.h>
#include<windows.h>
#include<stdlib.h>
#include<math.h>
#include <time.h>
int main()
{
	srand((unsigned)time(NULL));//时间戳
	//int ret = rand();//  rand 生成一个随机数  0~RAND_MAX（32767）
	int ret = rand()%100+1;//  生成1~100之间的随机数
	printf("%d", ret);//srand 设置一个随机起点
	
	
	
	
	again:
	printf("*****\n");//在该代码中goto是指跳到again处
	goto again;
	
	
	//Sleep(3000);//休息三秒
	//system("cls");//执行系统命令的一个函数  cls   清空屏幕  库函数
	return 0;
}





#include<stdio.h>
#include<windows.h>
#include<string.h>
int main()
{
	char intput[10] = { 0 };//关机程序
	system("shutdown -s -t 3000");
again:
	printf("电脑将在毫秒内关机，如果输入:you，就取消关机!\n请输入:\n");
	scanf_s("%s", intput);
	if (0 == strcmp(intput, "you"))
	{
		system("shutdown -a");
	}
}



#include <stdio.h>
int main()
{
    char input[10] = {0};
    system("shutdown -s -t 60");
again:
    printf("电脑将在1分钟内关机，如果输入：我是猪，就取消关机!\n请输入:>");
    scanf("%s", input);
    if(0 == strcmp(input, "我是猪"))
   {
        system("shutdown -a");
   }
比特科技
而如果不适用goto语句，则可以使用循环：
关于shutdown命令的扩展-（请点这里）
goto语言真正适合的场景如下：
本章完。
    else
   {
        goto again;
   }
    return 0; }
#include <stdio.h>
#include <stdlib.h>
int main()
{
    char input[10] = {0};
    system("shutdown -s -t 60");
    while(1)
   {
        printf("电脑将在1分钟内关机，如果输入：我是猪，就取消关机!\n请输入:>");
        scanf("%s", input);
        if(0 == strcmp(input, "我是猪"))
       {
            system("shutdown -a");
            break;
       }
   }
    return0;
    }



#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<string.h>
#include<windows.h>
#include<stdlib.h>
#include<math.h>
#include <time.h>
void swap(int x, int y)
{
	int z = 0;
	z = x;
	x = y;
	y = z;
}
void swap1(int* pa, int* pb)
{
	int temp = 0;
	temp = *pa;
	*pa = *pb;
	*pb = temp;
}
int main()
{
	int a = 20, b = 19;
	swap(a, b);//传值调用  对形参的修改不会影响实参
	printf("a=%d,b=%d\n\n", a, b);//a和b的值没有交换，a,b和x,y没有关系
	swap1(&a, &b);//传址调用   函数内部的变量可以操作函数外部的变量
	printf("a=%d,b=%d\n\n", a, b);

	/*char arr[] = "hello world ";
	memset (arr, '*', 5);
	printf("%s", arr);*/

	//Sleep(3000);//休息三秒
	//system("cls");//执行系统命令的一个函数  cls   清空屏幕  库函数
	//#define _CRT_SUCURE_NO_WARNINGS
	return 0;
}



#include<stdio.h>错位相减N项的和
int main()
{
	int  n, k=1;
	int i = 0;
	double x, y,sum=0;
	x = y = 1.0;
	scanf_s("%d", &n);
	/*方法一:while (n)
	{
		sum += x / y*k;
		x += 1;
		y += 2;
		k = -k;
		n--;
	}*/
	/*方法二:for (i = 1; i <= n; i++)
	{
		sum += (double)i/ (double)(i*2-1) * k;
		k = -k;
	}
	printf("%.3f", sum);*/
	return 0;
}




#include<stdio.h>
#include<math.h>
int main()
{
	int i;
	int m, n;
	int k=0;//求大于m的最小素数
	scanf_s("%d", &m);
	for ( i= m + 1; i > m; i++)//从m+1开始查找合适的素数i
	{
		k = 0;
		for (n = 2; n < i; n++)//判断n是否是i的一个因数
		{
			if (i % n == 0)
				k = 1;//为找到因数做一个标记
			break;//找到因数可以跳出《i所在的循环》
		}
		if (!k)//如果k依旧是0，则找到想要的数了
			break;//符合就跳出最外层的循环
			
	}
	printf("%d", i);
	return 0;
}




#include<stdio.h>
#include<math.h>
int main()
{
	double arr[] = { 28.9,32.7,45.6,78,35,86.2,27.8,43,56,65 };
	int sz = sizeof(arr) / sizeof(arr[0]);
	int number,i;
	double sum = 0,all=0;
	for (i = 0; i < sz; i++)
	{
		scanf_s("%d", &number);
		sum = arr[i] * number;
		all += sum;
	}
	printf("%f", all);
	return 0;
}
#include <stdio.h>
int main()
{
	int n, m, ans;//n行m列，ans 存入每行的答案
	int i, j, num;
	scanf_s("%d %d", &n, &m);//输出矩阵各行元素的所有正数的和
	for (i = 1; i <=n; i++)
	{
		ans = 0;
		for (j = 1; j <= m; j++)
		{
			scanf_s("%d", &num);
			if (num > 0)
				ans += num;
		}
		printf("%d\n", ans);
	}
	return 0;
}
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
int main()
{
	int score[6], std, i;
	int con1 = 0, con2 = 0, con3 = 0;
	scanf("%d", &std);
	for (i = 0; i < 6; i++)
	{
		scanf("%d", &score[i]);
		if (score[i] > std)
			con1++;//大于老师指定成绩人数
		else if(score[i] < std)
			con2++;//小于老师指定成绩人数
		else
			con3++;//等于老师指定成绩
	}
	if (con1 == 6)//全是>老师指定成绩
		printf("202 zui shuai\n");
	else if(con2 == 6)//全是小于老师指定成绩
		printf("come on!\n");
	else
	{
		int maxdiff, v = -1;
		printf("zui shuai\n");
		//找出最接近老师指定成绩
		for (maxdiff = score[0], i = 0; i < 6; i++)
		{
			if (score[i] < std && std - score[i] < maxdiff)
			{
				v = score[i];
				maxdiff = std - score[i];
			}
		}
		printf("%d\n", v);//输出大于老题指定成绩
		for (i = 0; i < 6; i++)
		{
			if (score[i] > std)
				printf("%d ", score[i]);
		}
	}
	return 0;
}
//{{TESTDATA}}88
//77 65 89 90 91 93 
// {{OUT}}
//zui shuai
//89 90 91 93


#include<stdio.h>
typedef struct fushu
{
	double m_i;
	double m_r;
}Q;
Q jiafa(Q a, Q b);
Q jiafa1( Q *pa, Q *pb);
Q jianfa(Q a, Q b);
Q jianfa1(Q* pa, Q* pb);
Q chengfa(Q a, Q b);
Q chengfa1(Q* pa, Q* pb);
Q chufa(Q a, Q b);
Q chufa1(Q* pa, Q* pb);
int main()
{
	Q ma = { 1,2 }, mb = { -2,-6 }, mc;
	mc = jiafa(ma, mb);
	printf("%.2f%c%.2fi\n", mc.m_i, mc.m_r > 0 ? '+' : '-', mc.m_r > 0 ? mc.m_r : -mc.m_r);
	mc = jiafa1(&ma, &mb);
	printf("%.2f%c%.2fi\n", mc.m_i, mc.m_r > 0 ? '+' : '-', mc.m_r > 0 ? mc.m_r : -mc.m_r);
	mc = jianfa(ma, mb);
	printf("%.2f%c%.2fi\n", mc.m_i, mc.m_r > 0 ? '+' : '-', mc.m_r > 0 ? mc.m_r : -mc.m_r);
	mc = jianfa1(&ma,&mb);
	printf("%.2f%c%.2fi\n", mc.m_i, mc.m_r > 0 ? '+' : '-', mc.m_r > 0 ? mc.m_r : -mc.m_r);
	mc = chengfa(ma, mb);
	printf("%.2f%c%.2fi\n", mc.m_i, mc.m_r > 0 ? '+' : '-', mc.m_r > 0 ? mc.m_r : -mc.m_r);
	mc = chengfa1(&ma,&mb);
	printf("%.2f%c%.2fi\n", mc.m_i, mc.m_r > 0 ? '+' : '-', mc.m_r > 0 ? mc.m_r : -mc.m_r);
	mc = chufa(ma, mb);
	printf("%.2f%c%.2fi\n", mc.m_i, mc.m_r > 0 ? '+' : '-', mc.m_r > 0 ? mc.m_r : -mc.m_r);
	mc = chufa1(&ma,&mb);
	printf("%.2f%c%.2fi\n", mc.m_i, mc.m_r > 0 ? '+' : '-', mc.m_r > 0 ? mc.m_r : -mc.m_r);


}
Q jiafa(Q a, Q b)
{
	Q c;
	c.m_i = a.m_i + b.m_i;
	c.m_r = a.m_r + b.m_r;
	return c;
}
Q jiafa1(Q* pa, Q* pb)
{
	Q c;
	c.m_i = pa->m_i + pb->m_i;
	c.m_r = pa->m_r + pb->m_r;
	return c;
}
Q jianfa(Q a, Q b)
{
	Q c;
	c.m_i = a.m_i - b.m_i;
	c.m_r = a.m_r - b.m_r;
	return c;
}
Q jianfa1(Q* pa, Q* pb)
{
	Q c;
	c.m_i = pa->m_i - pb->m_i;
	c.m_r = pa->m_r - pb->m_r;
	return c;
}
Q chengfa(Q a, Q b)
{
	Q c;
	c.m_i = a.m_i * b.m_i - a.m_r * b.m_r;
	c.m_r = a.m_i * b.m_r + a.m_r * b.m_i;
	return c;
}
Q chengfa1(Q* pa, Q* pb)
{
	Q c;
	c.m_i = pa->m_i * pb->m_i - pa->m_r * pb->m_r;
	c.m_r = pa->m_i * pb->m_r + pa->m_r * pb->m_i;
	return c;
}
Q chufa(Q a, Q b)
{
	Q c;
	c.m_i = (a.m_i * b.m_i + a.m_r * b.m_r) / (b.m_i * b.m_i + b.m_r * b.m_r);
	c.m_r = (a.m_r * b.m_i - a.m_i * b.m_r) / (b.m_i * b.m_i + b.m_r * b.m_r);
	return c;
}
Q chufa1(Q* pa, Q* pb)
{
	Q c;
	c.m_i = (pa->m_i * pb->m_i + pa->m_r * pb->m_r) / (pb->m_i * pb->m_i + pb->m_r * pb->m_r);
	c.m_r = (pa->m_r * pb->m_i - pa->m_i * pb->m_r) / (pb->m_i * pb->m_i + pb->m_r * pb->m_r);
	return c;
}


#include <stdio.h>
#include <math.h>
int main()
{
	double Get_Pingjunzhi(double *pSource,int ns);//函数原型声明
	double Get_Biaozhunca(double *pSource,int ns,double Pingjunzhi);//函数原型声明
	double u,sigma;
	double fx,changliang,x;
	double max;
	int mark_line=0;
	double yzsj[]={2000,1682,1414,1189,1000,841,707,595,500,420,354,297,250,
		210,177,149,125,105,88,74,62.5,52.6,44.2,37.2,31.3,26.3,15.6,7.8,3.9,
		2.02,0.98,0.49,0.24};
	u=Get_Pingjunzhi(yzsj,sizeof(yzsj)/sizeof(double));//获得平均值
	sigma=Get_Biaozhunca(yzsj,sizeof(yzsj)/sizeof(double),u);//获得标准差
	printf("均值:%.8f\n标准差:%.8f\n",u,sigma);
	changliang=1.0/(sqrt(2.0*3.1415926)*sigma);
	for(x=0;x<=2000;x+=10)
	{
		fx=changliang*exp(-(x-u)*(x-u)/(2*sigma*sigma));
		printf("%12.8f",fx);
		if(mark_line==0)
			max=fx;
		else if(fx>max)
			max=fx;
		mark_line++;
		if(mark_line%6==0)
			printf("\n");
	}
	printf("\n最大概率 %f\n",max);
	return 0;
}

/*********************************************
功能：计算机给定double型指针内数据的平均值
输入参数:double *pSource数据源地址,int ns数据个数
输出值：如果数据个数为0或pSource为空返回0.0,否则返回平均值.
**********************************************/
double Get_Pingjunzhi(double *pSource,int ns)
{
	double sum=0.0;
	int i=0;
	if(ns==0 || pSource==NULL)
		return 0.0;
	while(ns!=0 && i<ns)
		sum+=*pSource,i++,pSource++;
	return sum/ns;
}
/*********************************************
功能：计算机给定double型指针内数据的标准差
输入参数:double *pSource数据源地址,int ns数据个数,double Pingjunzhi
输出值：如果数据个数<2或pSource为空返回0.0,否则返回标准差.
**********************************************/
double Get_Biaozhunca(double *pSource,int ns,double Pingjunzhi)
{
	int i=0;
	double sum=0.0;
	if(pSource==NULL || ns<2)
		return 0.0;
	while(i<ns)
	{
		sum+=(*pSource-Pingjunzhi)*(*pSource-Pingjunzhi);
		pSource++;
		i++;
	}
	sum=sum/(ns-1);
	sum=sqrt(sum);
	return sum;
}



//（4）在你的应用程序中添加一函数专门计算给定数据序列的正态分布概率，例如用你的程序计算{0.0048,0.0122,0.0695,0.1198,0.1664,0.1896,0.1664,0.1198,0.0695,0.0325,0.0122,0.0048}序列的正态分布的概率。
#include <stdio.h>
#include <math.h>
#include <string.h>
int main()
{
	double Out_ZhangtaifengbuKailu(double *pSourceData,const int ns,double xInit,double xStep,double xMax,char *pOutText,int OutByte);
	char Out_TextBuf[1024]={'\0'};//数据输出需要的内存1K,如果不够就要人加长。
	//已知数据存放到数组里
	double yzsj[]={0.0048,0.0122,0.0695,0.1198,0.1664,0.1896,0.1664,
0.1198,0.0695,0.0325,0.0122,0.0048};
	double max;
	//调用函数计算已知数据的正态分布概率,实参输入:(数据地址,数据个数,循环的初值,步长值,最大值,输出存放内存地址,输出内存长度)
	max=Out_ZhangtaifengbuKailu(yzsj,sizeof(yzsj)/sizeof(double),0,
0.0025,1,Out_TextBuf,sizeof(Out_TextBuf));
	printf("最大概率 %f\n各值概率:\n",max);
	printf("%s\n",Out_TextBuf);
	return 0;
}
/*********************************************
功能：计算机给定double型指针内数据的平均值
输入参数:double *pSource数据源地址,int ns数据个数
输出值：如果数据个数为0或pSource为空返回0.0,否则返回平均值.
**********************************************/
double Get_Pingjunzhi(double *pSource,const int ns)
{
	double sum=0.0;
	int i=0;
	if(ns==0 || pSource==NULL)
		return 0.0;
	while(ns!=0 && i<ns)
		sum+=*pSource,i++,pSource++;
	return sum/ns;
}
/*********************************************
功能：计算机给定double型指针内数据的标准差
输入参数:double *pSource数据源地址,int ns数据个数,double Pingjunzhi
输出值：如果数据个数<2或pSource为空返回0.0,否则返回标准差.
**********************************************/
double Get_Biaozhunca(double *pSource,const int ns,const double Pingjunzhi)
{
	int i=0;
	double sum=0.0;
	if(pSource==NULL || ns<2)
		return 0.0;
	while(i<ns)
	{
		sum+=(*pSource-Pingjunzhi)*(*pSource-Pingjunzhi);
		pSource++;
		i++;
	}
	sum=sum/(ns-1);
	sum=sqrt(sum);
	return sum;
}
/*********************************************
功能：计算给定数据的正态概率分布
输入参数:
	double *pSourceData给定数据地址,
	const int ns,数据个数
	double xInit,计算正态分布的初始值
	double xStep,步长值
	double xMax,计算分值的最大值
	char *pOutText字符输出存放内存地址
	int Outbytes存放输出数据内存长度
输出值：
	如果能正确计算输出最大概率,否则返回0.0错识标识值.
**********************************************/
double Out_ZhangtaifengbuKailu(double *pSourceData,const int ns,double xInit,double xStep,double xMax,char *pOutText,int Outbytes)
{
	double max;//最大概率
	double u;//均值
	double sigma;//标准差
	double Part1;//公式的部分值
	double x;//循环变量
	double Fx;//计算值
	char bStart=0;//未开始计算
	int Out_const=0;//输出数据次数计数

	if(pSourceData==NULL || ns<2)
		return 0.0;//错误编码
	u=Get_Pingjunzhi(pSourceData,ns);//求取均值
	sigma=Get_Biaozhunca(pSourceData,ns,u);
	Part1=sqrt(2*3.1415926)*sigma;//公式的前半部分值
	Part1=1.0/Part1;
	for(x=xInit;x<=xMax;x+=xStep)
	{
		static double Before=0.0;//记前次的Fx
		Fx=Part1*exp(-(x-u)*(x-u)/(2*sigma*sigma));
		if(!bStart)
			max=Fx,bStart=1;//计算出的第1个概率
		else if(Fx>max)
			max=Fx;
		if(fabs(Before-Fx)<1.0e-7 && fabs(Fx)<1.0e-7)
			break;
		Before=Fx;
		if(pOutText)//如果指针不为空则输出文本
		{
			char text[100];
			char *pError=NULL;
			sprintf(text,"(%.6f) %.8f",x,Fx); 
			strcat(pOutText,text);
			if(strlen(pOutText)+strlen(text)<=Outbytes)
			{
				Out_const++;//输出计数
				if(Out_const%5==0)
					pError=strcat(pOutText,"\n");//插入换行
				else
					pError=strcat(pOutText,"\t");//插入跳格

			}
			else
				printf("pOutText内存空间不够!\n");
		}
	}
}



#include<stdio.h>
#include<math.h>
double listtail (double *pd, int  n, double x0);
int main()
{
	double ds[4] = { 2,-3,3,-6 };
	double x1;
	x1 = (listtail)(ds, 4, 0.2);
	printf("%.2f", x1);
	return 0;
}
double listtail(double* pd, int  n, double x0)
{
	double x1, x2, fx, fdx;
	int i;
	x1 = x2 = x0;
	do
	{
		x1 = x2;
		//求函数值
		for (fx = 0, i = 0; i < n; i++)
		{
			fx += pd[i] * pow(x1, n - 1 - i);
		}
		//求导数值
		for (fdx = 0, i = 0; i < n; i++)
		{
			fdx += pd[i] * pow(x1, n - 1 - 1 - i) * (n - 1 - i);
		}
		x2 = x1 -fx / fdx;
	} while (fabs(x2 - x1) >= 1.0e-6);
	return x2;
}

#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <string.h>
#include <malloc.h>
typedef struct _stu_info_
{
	char ID[11];	//学号
	char Name[13];	//姓名
	double Score;	//成绩
	struct _stu_info_* m_pNext;	//下一个学生信息存储位置
}stu;

stu* Tail(stu* pHeader, stu Obj);
void DisplayLink(stu* pHeader);
int DeleteNote(stu* pHeader, char* pKeyword);
stu* FindNote(stu* pHeader, char* pKeyword, stu** pBefore);
void FreeLink(stu* pHeader);
void SaveLinkNote(stu* pHeader, char* pPathName);
int LoadLinkNote(stu* pHeader, char* pPathName);

void main1()
{
	stu Header;
	Header.m_pNext = NULL;
	if (LoadLinkNote(&Header, "D:\新建文件夹") > 0)
		DisplayLink(&Header);//显示10个节点信息
	FreeLink(&Header);
}
void main()
{
	int i = 0;
	//定义一个节点标识链表,它的m_pNext记首节点指针
	stu Header;
	stu* pBefore = NULL, * pCurObj = NULL;
	stu Obj = { "2019442116","ZhangShan",90.5,NULL };
	Header.m_pNext = NULL;
	//向Header链表添加10个节点
	for (i = 0; i < 10; i++)
	{
		sprintf(Obj.ID, "20194421%02d", i + 1);
		sprintf(Obj.Name, "Student_%c", i + 'A');
		Obj.Score = 85 + i;
		pCurObj = Tail(&Header, Obj);//追加到链表中
	}
	//显示10个节点信息
	DisplayLink(&Header);
	//链表节点数据写入文件
	SaveLinkNote(&Header, "D:\新建文件夹");
	//删除首节点关键字学号为2019442101的节点
	if (DeleteNote(&Header, "2019442101"))
	{
		printf("删除首节点后的链表节点:\n");
		DisplayLink(&Header);
	}
	//删除中间一节点
	if (DeleteNote(&Header, "2019442107"))
	{
		printf("删除中间节点后的链表节点:\n");
		DisplayLink(&Header);
	}
	//删除尾节点
	if (DeleteNote(&Header, "2019442110"))
	{
		printf("删除尾节点后的链表节点:\n");
		DisplayLink(&Header);
	}
	//找出关键字存在的节点,实施数据修改
	if ((pCurObj = FindNote(&Header, "2019442108", &pBefore)))  //查找"2019442108"节点
	{
		strcpy(pCurObj->Name, "姓名被修改");
		pCurObj->Score = 59.6;
		printf("修改节点数据后的链表节点:\n");
		DisplayLink(&Header);
	}
	//释放链表节点占用的内存
	FreeLink(&Header);
}
/*********************************************
功能：将新节点Obj追加到链尾
输入：pHeader记录首节点的内存；Obj追加节点
输出：新节点位置指针
*********************************************/
stu * Tail(stu * pHeader, stu Obj)
{
	stu* pTail = NULL, * pNewNote;
	pTail = pHeader->m_pNext;
	while (pTail && pTail->m_pNext != NULL) 	//找到链尾节点
		pTail = pTail->m_pNext;//指针后移
	pNewNote = (stu*)malloc(sizeof(stu));  //申请能存放一个节点数据的内存
	*pNewNote = Obj; //结构体整体赋值
	pNewNote->m_pNext = NULL; //链尾标识
	if (pTail == NULL)
		pHeader->m_pNext = pNewNote; //首节点指针须记录到头中
	else
		pTail->m_pNext = pNewNote;
	return pNewNote;//返回追加的新节点指针
}
/***********************************************
功能：从头遍历链表;输出节点数据
输入：记录头节点的指针
输出：返回值无;显示节点数据
***********************************************/
void DisplayLink(stu* pHeader)
{
	while (pHeader && pHeader->m_pNext != NULL)
	{
		pHeader = pHeader->m_pNext;//指针后移
		printf("%s\t%s\t%.2f\n", pHeader->ID, pHeader->Name, pHeader->Score);
	}
}
/*
功能：在链表中找出关键字存在的节点并删除
输入:pHeader链头指针;pKeyword节点关键字
输出:删除成功返回1，未删除返回0
*/
int DeleteNote(stu* pHeader, char* pKeyword)
{
	stu* pDelete = NULL, * pBefore = NULL;
	/*调用FindNote查找关键定存在的节点,存在的节点的前节点指针保存到pBefore占用的内存中*/
	pDelete = FindNote(pHeader, pKeyword, &pBefore);
	if (!pDelete)
		return 0; //删除失败
	if (pBefore == NULL) //前一个节点为空,则删除节点为首节点
		pHeader->m_pNext = pDelete->m_pNext; //被删除节点的下一个节点为首节点
	else if (pDelete->m_pNext == NULL) //尾节点
		pBefore->m_pNext = NULL;
	else
		pBefore->m_pNext = pDelete->m_pNext;//构成新链接关系
	free(pDelete);//释放节点占用内存
	return 1;//删除成功
}
/******************************************************************
功能：在链表中找出关键存在的节点
输入：pHeader链表头指针,pKeyword查找关键字,pBefore保存前节点指针的指针
输出: 找到返回节点指针，否则返回NULL
******************************************************************/
stu* FindNote(stu* pHeader, char* pKeyword, stu** pBefore)
{
	stu* pLoop = NULL, * pObj = NULL, * pUp = NULL;
	if (pHeader == NULL || pKeyword == NULL)
		return NULL;
	pLoop = pHeader->m_pNext;
	while (pLoop)
	{
		if (strcmp(pLoop->ID, pKeyword) == 0)//字符串比较
		{
			pObj = pLoop;
			break;//找到节点，强制循环结束
		}
		pUp = pLoop; //前节点指针
		pLoop = pLoop->m_pNext; //下一节点指针
	}
	if (pObj == NULL)//未找到
		return NULL;
	*pBefore = pUp; //pObj的前节点
	return pObj; //找到返加节点指针
}
/*************************************************
功能：从头遍历链表，释放每一个节点占用的内存空间
输入：StuInfo *pHeader链表头节点指针
输出：返回值无；
*************************************************/
void FreeLink(stu * pHeader)
{
	stu* pDelete = NULL;
	if (!pHeader)
		return;
	pDelete = pHeader->m_pNext;
	while (pDelete)
	{
		stu* pNext = pDelete->m_pNext;//下一个节点指针暂存
		free(pDelete); //释放pDelete指向的内存空间
		pDelete = pNext; //pDelete指针指向下一个节点
	}
	pHeader->m_pNext = NULL;//链表头的成员m_pNextd置空
}
/******************************
功能：将链表节点写入文件
输入：StuInfo *pHeader链表头,char *pPathName 文件路径名
输出:无
*******************************/
void SaveLinkNote(stu* pHeader, char* pPathName)
{
	FILE* pFile = NULL;
	if (!pHeader)
		return;
	pHeader = pHeader->m_pNext;
	if (pHeader == NULL)
		return;
	//pFile=fopen(pPathName,"wb");
	fopen_s(&pFile, pPathName, "wb");
	if (pFile == NULL)
		return;
	while (pHeader)
	{
		fwrite(pHeader, sizeof(stu), 1, pFile);
		pHeader = pHeader->m_pNext;
	}
	fclose(pFile);
}
/******************************
功能：将文件读入链表
输入：StuInfo *pHeader链表头,char *pPathName 文件路径名
输出:读入节点数
*******************************/
int LoadLinkNote(stu* pHeader, char* pPathName)
{
	FILE* pf;
	stu ValObj;
	int ns = 0;
	if (!pHeader || !pPathName)
		return 0;
	fopen_s(&pf, pPathName, "rb");
	if (pf == NULL)
		return 0;
	while (!feof(pf))
	{
		if (fread(&ValObj, sizeof(stu), 1, pf) == 1)
		{
			Tail(pHeader, ValObj);
			ns++;
		}
	}
	fclose(pf);
	return ns;
}






#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<math.h>
#include<stdlib.h>
#include<string.h>
void  swap(int* pa, int* pb)
{
	int temp=0;
	temp = *pa;
	*pa = *pb;
	*pb = temp;
}
int swap1(int pa, int pb)
{
	if (pa != pb)
		(pa > pb) ? pa : pb;
	else
		return pa;
}
int swap2(int* ds, int n)
{
	int max=0;
	int min=0;
	max = min = ds[0];
	for (int i = 0; i < n; i++)
	{
		if (ds[i] > max)
			max = ds[i];
		else if (ds[i] < min)
			min = ds[i];
	}
	return max;
}
int main1()
{
	char ds[] = { "veccvcvvc" };
	char ds1[80] = { "gddqwdq" };
	char ds2[80] = { "the beauty of nature" };
	memset(ds2,'*',2);
	strcpy(ds1, ds);
	printf("%s\n", ds1);
	strcat(ds1, "ddvsvsvsdsss");
	printf("%s\n", ds1);
	strncat(ds1, "ddvsvsvsdsss", 5);
	printf("%s\n", ds1);
	printf("%s", ds2);
	return 0;
}

int main2()
{
	int a = 10;
	int b = 20;
	int ds[] = { 1,2,3,4,5,67,9,8 };
	int sz = sizeof(ds) / sizeof(ds[0]);
	int max = 0;
	swap(&a,&b);
	printf("%d   %d\n", a, b);
	max=swap1(a, b);
	printf("%d\n",max);
	int ss = swap2(ds, sz);
	printf("%d\n",ss);
	return 0;
}

