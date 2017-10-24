import java.util.Scanner;
abstract class Shape{
    abstract float GetArea();
    abstract float GetPerimeter();
}
class Rectangle{
    private double x,y;
    public Rectangle(int i, int j) {
		x=i;
		y=j;
	}
	public float GetArea(){
		return (float)(x*y);
	}
	public float GetPerimeter(){
        return (float)((x+y)*2);
    }
	
}
class Circle{
    private double x;
    public Circle(int r) {
    	x=r;
	}
	public float GetArea(){
		return (float)(x*x*3.14);
	}
	public float GetPerimeter(){
        return (float)(x*2*3.14);
    }
}
public class Main{
    public static void main(String[] args){
    	Scanner sca = new Scanner(System.in);
    	int a = sca.nextInt();
    	int b = sca.nextInt();
    	int r = sca.nextInt();
        Rectangle aa = new Rectangle(a,b);
        System.out.println(aa.GetArea());
        System.out.println(aa.GetPerimeter());
        Circle c = new Circle(r);
        System.out.println(c.GetArea());
        System.out.println(c.GetPerimeter());
    }
}
