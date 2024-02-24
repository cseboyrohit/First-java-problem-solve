// # First-java-problem-solve
//Java code for chapter 10 problem sove 
//Question number 2;
 class Rectangle {
     protected double length;
     protected Double width;

     Rectangle() {
         System.out.println(" I am rectangle Class no pass auguement");
     }

     Rectangle(double length, double width) {
         System.out.println("I am Rectangle class ");
         this.length = length;
         this.width = width;
     }

     public
     double getlength() {
         return length;
     }
     public void setlength(double length){
         this.length=length;
     }

     public double getwidth(){
         return width;
     }
     public  void setwidth(double width){
         this.width=width;
     }
     public double calculateArea(){
         return length*width;
     }
     public double calculatePerimeter(){
         return 2*(length*width);
     }
}
class Cuboid extends Rectangle{
     private double height;
     Cuboid(double length ,double width,double height){
         super(length,width);
         System.out.println(" i am a cuboid class ");
         this.height=height;
     }
     public double getheight(){
         return height;
     }
     public void setheigth(double height){
         this.height=height;
     }
     public double calVolum(){
         return length*width*height;
     }
    // now Overriding
    @Override
    public double calculateArea(){
         return 2*(length*width+width*height+height*length);
    }
    @Override
    public double calculatePerimeter(){
         return 4*(length+width+height);
    }

}
public class Main {
    public static void main(String[] args) {
        Rectangle rc = new Rectangle(12,23);
        System.out.print(rc.calculateArea());
        Cuboid obj= new Cuboid(5,2,3);
        System.out.println(obj.calVolum());
        System.out.println(obj.calculateArea());
        System.out.println(obj.calculatePerimeter());
 
    }
}
