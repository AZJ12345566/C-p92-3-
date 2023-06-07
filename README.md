# C-p92-3-
C语言学习笔记 p92函数和递归(3)
#include<stdio.h>
int my_strlen(char* str)//这个str是元素首地址
{
    if(*str!='\0')
        return 1+my_strlen(atr+1);
    else
        retrun 0;
}
int main()
{
    char arr[]="bit";
    int len=my_strlen(arr);
    printf("%d\n,len);
    return 0;
}

//递归与迭代
//迭代也就是循环

//循环方式
int Facl(int n)
{
    int i=0;
    int ret=1;
    for(i=0;i<=n;i++)
    {
        ret *=i;
    }
    return ret;
}
//递归方式
int Facl(int n)
{
    if(n<=1)
        return 1;
    else
        return n*Facl2(n-1);
}
int main()
{
    //求n的阶乘
    int n=0;
    int ret=0;
    scanf("%d",&n);
    ret=Facl(n);//循环方式
    printf("%d\n",ret);
    return 0;
}

//斐波那契数列：1 1 2 3 5 8 13 21 34 55 ...
//第一种版本
int Fib(int n)
{
    if(n<=2)
        return 1;
    else
        return Fib(n-1)+Fib(n-2);
}
//第二种版本
int Fib(int n)
{
    int a=1;
    int b=1;
    int c=0;
    while(n>2)
    {
        c=a+b;
        a=b;
        b=c;
        n--;
    }
    return c;
}
int main()
{
    int n=0;
    int ret=0;
    scanf("%d",&n);
    //TDD-测试驱动开发：先想函数怎么用，再想函数怎么去实现
    ret=Fib(n);
    printf("ret=%d\n",ret);
    return 0;
}









