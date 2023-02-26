package rational;
import java.util.Scanner;
public class Rational
{
    int a,b,c,d;
    public Rational(){}
    public Rational(int n1,int n2, int n3, int n4){
    a=n1;
    b=n2;
    c=n3;
    d=n4;
    }
    Scanner ob=new Scanner(System.in);
    public void getnumbers()
    {
        System.out.print("Enter number a:");
        a=ob.nextInt();
        System.out.print("Enter number b:");
        b=ob.nextInt();
        System.out.print("Enter number c:");
        c=ob.nextInt();
        System.out.print("Enter number d:");
        d=ob.nextInt();
    }
    String toStrinng()
    {        
        return a+" "+b+" "+c+" "+d;
    }
    int den;
    int num;
    public void addition(){
       num=(a*d+b*c);
       den=(b*d); 
       if(b==0 || d==0)
        {
            System.out.println("Invalid Rational number");
        }
       else{
       System.out.println("Addition="+num+"/"+den);
       }
    }
    public void subtraction(){
        num=(a*d-b*c);
        den=(b*d); 
        if(b==0 || d==0)
        {
            System.out.println("Invalid Rational number");
        }
        else{
        System.out.println("Subtraction="+num+"/"+den);
        }
    }
    public void multiplication(){
        num=(a*c);
        den=(b*d);
        if(b==0 || d==0)
        {
            System.out.println("Invalid Rational number");
        }
        else{
        System.out.println("Multiplication="+num+"/"+den);
        }
    }    
    public void division(){
        num=(a*d);
        int den=(b*c);
         if(b==0 || d==0)
        {
            System.out.println("Invalid Rational number");
        }
         else{
        System.out.println("Division="+num+"/"+den); 
         }
        }
    }    

Package with Mainclass:
package RationalMain;
import rational.Rational;
public class RationalClass {
public static void main(String args[]){
    Rational r=new Rational();
    r.getnumbers();
    r.addition();
    r.subtraction();
    r.multiplication();
    r.division();
}       
}


