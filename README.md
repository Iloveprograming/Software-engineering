# hello-world

1.This is a simple java sample.

public class BeerSong
{
public static void main(String [] args)
{
BeerSong a=new BeerSong();
int n=99;
String word="bottles";
for(int i=n;i>=0;i--)
{
if(i==1)
{
word="bottle";
a.print(i,word);
}
else if(i==0)
System.out.println("No more bottles on the wall.");
else
{
a.print(i,word);
}
}
}
public void print(int i,String a)
{
System.out.println(i+" "+a+" of beer on the wall."+i+" "+a+" bottles of beer.");
System.out.println("Take one down.");
System.out.println("Pass it around.");
System.out.println((i-1)+" "+a+" of beer on the wall.");
System.out.println();
}
}

2.about array overflow

public class Test{
public static void main(String [] args){
int []a=new int[3];
a[-1]=10;
System.out.println(a[-1]);
a[3]=5;
System.out.println(a[3]);
}
}

OVERFLOW ERROR：
Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: -1
        at Test.main(Test.java:4)
Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: 3
        at Test.main(Test.java:4)
        
3.print address
public class Test{
public static void main(String [] args){
String a="man",b="women";
a=b;
b="human";
System.out.println(a);
System.out.println(a.hashCode());
System.out.println(b.hashCode());
}
}


输出：
women
113313790
99639597

结论：改变b的值，a不变，地址的输出如图.
