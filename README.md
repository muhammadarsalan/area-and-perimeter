# area-and-perimeter
package shape;

public class main {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		shape [] shapeList = new shape[2];
		shapeList[0] = new rectangle(5.0,3.0); 
		shapeList[1] = new circle(4.0);
		for (int i=0;i<2;i++)
		{
			System.out.print (shapeList[i].toString()+" ");
			System.out.print (shapeList[i].area()+" ");
			System.out.println (shapeList[i].perimeter());
			
		}
		
		
	}

}
package shape;

public abstract class shape {

		protected String shapeName;
		public shape(String name) {shapeName = name; }
		public abstract double area();
		public abstract double perimeter();
		public String toString() {
			return shapeName;
		}; 
		
		}		
		package shape;

public class rectangle extends shape
{
protected double lenght,width;
public rectangle (double len, double wid)
{
	super("rectangle");
	lenght = len; width = wid;
}

	public double area ()
	{return lenght * width;	}
		public double perimeter()
		{return 2.0 * (lenght + width); }
		

}
package shape;

public class circle extends shape
{
private double radius;
public circle (double rad)
{
super("circle");
radius = rad; 
}

public double area()
{return Math.PI * radius *radius; }
public double perimeter()
{return 2.0 * Math.PI * radius; }

}
