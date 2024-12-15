program 1 AIM: Design a class ‘Complex ‘with data members for real and imaginary part. Provide 
default and Parameterized constructors. Write a program to perform arithmetic 
operations of two complex numbers. 
import java.util.Scanner; 
public class Complex 
{ 
public static void main(String args[]) 
{ 
int num1, num2, answer,ch=0; 
Complex_Op cal = new Complex_Op () ; 
Scanner sc = new Scanner(System.in); 
System.out.print("Enter first Number :\n"); 
num1 = sc.nextInt(); //Real part 
num2 = sc.nextInt(); //Imaginary Part 
Complex_Op Object1 = new Complex_Op(num1,num2); 
System.out.print("Enter Second Number :\n"); 
num1 = sc.nextInt(); //Real Part 
num2 = sc.nextInt(); //Imaginary Part 
Complex_Op Object2 = new Complex_Op(num1,num2); 
System.out.println ("******Following Arithmetic Operations are perform                               
on Complex Numbers*****"); 
System.out.println("1. Addition"); 
System.out.println("2. Substraction"); 
System.out.println("3. Multiplication"); 
System.out.println("4. Division"); 
System.out.println("Enter Your Choice : "); 
ch=sc.nextInt(); 
switch(ch) 
{ 
case 1: cal.Addition(Object1,Object2); 
break; 
case 2: cal.Substraction(Object1,Object2); 
break; 
case 3: cal.Multiplication(Object1,Object2); 
break; 
case 4: cal.Division(Object1,Object2); 
break; 
  } 
                      } 
             } 
              class Complex_Op 
{ 
                                 float real,imag; 
Complex_Op() //Default Constructor 
                                    { 
 real=0; 
  imag=0; 
                                     } 
                           Complex_Op(float Comp1,float Comp2) //Parameterized Constructor 
{ 
    real=Comp1; 
     imag=Comp2; 
} 
void Addition(Complex_Op C1,Complex_Op C2) 
{ 
      float real,imag; 
      real = (C1.real + C2.real); 
                                             imag = (C1.imag + C2.imag); 
                                         System.out.println("Addition is:("+real+") + ("+imag+")i" ); 
} 
void Substraction(Complex_Op C1,Complex_Op C2) 
{ 
      float real,imag; 
                                              real = (C1.real -C2.real); 
                                              imag = (C1.imag - C2.imag); 
                                              System.out.println("Substraction is:("+real+") - ("+imag+")i"); 
} 
void Multiplication(Complex_Op C1,Complex_Op C2) 
{ 
                                               float real,imag; 
                                               real=(C1.real * C2.real - C1.imag * C2.imag); 
          imag=(C1.real * C2.imag+ C1.imag * C2.real); 
                                                 System.out.println("Multiplication is:("+real+") *("+imag+")i"); 
} 
void Division(Complex_Op C1,Complex_Op C2) 
{ 
        float real,imag; 
        float a = C1.real; 
                float b = C1.imag; 
             float c= C2.real; 
                     float d = C2.imag; 
                                                float denominator = c * c + d * d; 
                real = (a * c + b * d) / denominator; 
                      imag= (b * c - a * d) / denominator; 
                      System.out.println("Division is:("+real+") / ("+imag+")i" );  
             } 
    } 
Output 
Enter first Number 
2 3 
Enter Second Number 
3 4 
******Following Arithmetic Operations are perform on 
Complex Numbers***** 
1.Addition 
2.Substraction 
3.Multiplication 
4.Division 
Enter Your Choice :  
1 
Addition is:(5.0) + (7.0)i



program2
class Publication  
{ 
    String title; 
    double price; 
    int copies; 
 public Publication(String title, double price, int copies)  
    { 
        this.title = title; 
        this.price = price; 
        this.copies = copies; 
    } 
 
    public void saleCopy(int numberOfCopies)  
    { 
        this.copies = this.copies-numberOfCopies; 
    } 
 
    public double totalSale()  
    { 
        return price * copies; 
    } 
} 
 
class Book extends Publication  
{ 
    String author; 
 
    public Book(String title, double price, int copies, String author)  
    { 
        super(title, price, copies); 
        this.author = author; 
    } 
 
    public void orderCopies(int numberOfCopies) 
    { 
        this.copies =  this.copies +numberOfCopies; 
    } 
} 
 
class Magazine extends Publication 
{ 
    int currentIssue; 
 
    public Magazine(String title, double price, int copies, int currentIssue)  
    { 
        super(title, price, copies); 
        this.currentIssue = currentIssue; 
    } 
 
    public void orderQty(int quantity)  
    { 
        this.copies += quantity; 
    } 
 
    public void receiveIssue(int newIssue)  
    { 
        this.currentIssue = newIssue; 
    } 
} 
 
 
 
public class PublicationDemo  
{ 
    public static void main(String[] args)  
    { 
        Book book = new Book("Java Programming", 50.0, 100, "Author A"); 
        Magazine magazine = new Magazine("Tech Today", 5.0, 200, 10); 
         
        book.orderCopies(20); 
        book.saleCopy(30); 
        
        magazine.saleCopy(50); 
        magazine.orderQty(100); 
        magazine.receiveIssue(11); 
 
        System.out.println("Title of book: " + book.title); 
        System.out.println("Price of book: " + book.price); 
        System.out.println("Total sale of book: $" + book.totalSale()); 
        System.out.println("Title of Magazine :" + magazine.title); 
        System.out.println("Price of Magazine: " + magazine.price); 
        System.out.println("Total sale of magazine: $" + magazine.totalSale()); 
    } 
} 
Output 
Title of book: Java Programming 
Price of book: 50.0 
Total sale of book: $4500.0 
 
Title of Magazine :Tech Today 
Price of Magazine: 5.0 
Total sale of magazine: $1250.0


   program 3
   class Employee  
{ 
private String Emp_name; 
private String Emp_id; 
private String Address; 
private String Mail_id; 
private String Mobile_no; 
public Employee(String Emp_name, String Emp_id, String Address, String Mail_id, String 
Mobile_no)  
{ 
{ 
} 
this. Emp_name = Emp_name; 
this. Emp_id = Emp_id; 
this. Address = Address; 
this. Mail_id = Mail_id; 
this.Mobile_no = Mobile_no; 
} 
// Display Employee details 
public void displayEmployeeDetails() 
System.out.println("Employee ID: " + Emp_id); 
System.out.println("Name: " + Emp_name); 
System.out.println("Address: " + Address); 
System.out.println("Email: " + Mail_id); 
System.out.println("Mobile: " + Mobile_no); 
} 
class Programmer extends Employee 
{ 
private double basicPay; 
public Programmer(String Emp_name, String Emp_id, String Address, String Mail_id, String 
Mobile_no, double basicPay)  
{ 
} 
super(Emp_name, Emp_id, Address, Mail_id, Mobile_no); 
this.basicPay = basicPay; 
public void generatePaySlip() 
{ 
System.out.println("Basic Pay: " + basicPay);    
double da = 0.97 * basicPay; 
System.out.println("DA: " + da); 
double hra = 0.10 * basicPay; 
System.out.println("HRA: " + hra); 
double pf = 0.12 * basicPay; 
System.out.println("PF: " + pf); 
double staffClubFund = 0.001 * basicPay; 
System.out.println("Staff Club Fund: " + staffClubFund); 
double grossSalary = basicPay + da + hra; 
System.out.println("Gross Salary: " + grossSalary); 
double netSalary = grossSalary - pf - staffClubFund; 
System.out.println("Net Salary: " + netSalary); 
} 
} 
class TeamLead extends Employee 
{ 
private double basicPay; 
public TeamLead(String Emp_name, String Emp_id, String Address, String Mail_id, String 
Mobile_no, double basicPay)  
{ 
{ 
super(Emp_name, Emp_id, Address, Mail_id, Mobile_no); 
this.basicPay = basicPay; 
} 
public void generatePaySlip() 
System.out.println("Basic Pay: " + basicPay);    
double da = 0.97 * basicPay; 
System.out.println("DA: " + da); 
double hra = 0.10 * basicPay; 
System.out.println("HRA: " + hra); 
double pf = 0.12 * basicPay; 
System.out.println("PF: " + pf); 
double staffClubFund = 0.001 * basicPay; 
System.out.println("Staff Club Fund: " + staffClubFund); 
double grossSalary = basicPay + da + hra; 
System.out.println("Gross Salary: " + grossSalary); 
double netSalary = grossSalary - pf - staffClubFund; 
System.out.println("Net Salary: " + netSalary); 
} 
} 
class AssistantProjectManager extends Employee  
{ 
private double basicPay; 
public AssistantProjectManager(String Emp_name, String Emp_id, String Address, String 
Mail_id, String Mobile_no, double basicPay)  
{ 
super(Emp_name, Emp_id, Address, Mail_id, Mobile_no); 
this.basicPay = basicPay; 
} 
public void generatePaySlip() 
{ 
System.out.println("Basic Pay: " + basicPay);    
double da = 0.97 * basicPay; 
System.out.println("DA: " + da); 
double hra = 0.10 * basicPay; 
System.out.println("HRA: " + hra); 
double pf = 0.12 * basicPay; 
System.out.println("PF: " + pf); 
double staffClubFund = 0.001 * basicPay; 
System.out.println("Staff Club Fund: " + staffClubFund); 
double grossSalary = basicPay + da + hra; 
System.out.println("Gross Salary: " + grossSalary); 
double netSalary = grossSalary - pf - staffClubFund; 
System.out.println("Net Salary: " + netSalary); 
} 
} 
class ProjectManager extends Employee 
{ 
private double basicPay; 
public ProjectManager(String Emp_name, String Emp_id, String Address, String Mail_id, 
String Mobile_no, double basicPay) 
{ 
super(Emp_name, Emp_id, Address, Mail_id, Mobile_no); 
this.basicPay = basicPay; 
} 
public void generatePaySlip() 
{ 
} 
System.out.println("Basic Pay: " + basicPay);    
double da = 0.97 * basicPay; 
System.out.println("DA: " + da); 
double hra = 0.10 * basicPay; 
System.out.println("HRA: " + hra); 
double pf = 0.12 * basicPay; 
System.out.println("PF: " + pf); 
double staffClubFund = 0.001 * basicPay; 
System.out.println("Staff Club Fund: " + staffClubFund); 
double grossSalary = basicPay + da + hra; 
System.out.println("Gross Salary: " + grossSalary); 
double netSalary = grossSalary - pf - staffClubFund; 
System.out.println("Net Salary: " + netSalary); 
} 
public class Main { 
public static void main(String[] args) 
{ 
Programmer programmer = new Programmer("Amit", "1001", "Pune", 
"amit@mail.com",     "1234567890", 50000); 
TeamLead teamLead = new TeamLead("Puja", "1002", "Sangamner", "puja@mail.com", 
"0987654321", 70000); 
AssistantProjectManager apm = new AssistantProjectManager("Anay", "1003", 
"Mumbai", "anay@mail.com", "1112223333", 90000); 
ProjectManager pm = new ProjectManager("Bob", "1004", "Nashik", "bob@mail.com", 
"4445556666", 120000); 
System.out.println("****Information of Programmer****"); 
programmer.displayEmployeeDetails(); 
programmer.generatePaySlip(); 
System.out.println(); 
System.out.println("****Information of Team Lead****"); 
teamLead.displayEmployeeDetails(); 
teamLead.generatePaySlip(); 
System.out.println(); 
System.out.println("****Information of Assistant Project Manager****"); 
apm.displayEmployeeDetails(); 
apm.generatePaySlip(); 
System.out.println(); 
System.out.println("****Information of Project Manager****"); 
pm.displayEmployeeDetails(); 
pm.generatePaySlip(); 
} 
} 
Output 
****Information of Programmer**** 
Employee ID: 1001 
Name: Amit 
Address: Pune 
Email: amit@mail.com 
Mobile: 1234567890 
Basic Pay: 50000.0 
DA: 48500.0 
HRA: 5000.0 
PF: 6000.0 
Staff Club Fund: 50.0 
Gross Salary: 103500.0 
Net Salary: 97450.0 
****Information of Team Lead**** 
Employee ID: 1002 
Name: Puja 
Address: Sangamner 
Email: puja@mail.com 
Mobile: 0987654321 
Basic Pay: 70000.0 
DA: 67900.0 
HRA: 7000.0 
PF: 8400.0 
Staff Club Fund: 70.0 
Gross Salary: 144900.0 
Net Salary: 136430.0



program 4
import java.util.Scanner; 
// Base class 
abstract class Shape 
{ 
double dimention1; 
double dimention2; 
// Method to input data 
public void inputData(double d1, double d2) 
{ 
} 
this.dimention1 = d1; 
this.dimention2 = d2; 
// Abstract method to compute area 
public abstract double compute_area(); 
} 
// Derived class for Triangle 
class Triangle extends Shape 
{ 
} 
public double compute_area() 
{ 
} 
return 0.5 *dimention1 * dimention2; // Area = 0.5 * base * height 
// Derived class for Rectangle 
class Rectangle extends Shape 
{ 
public double compute_area() 
{ 
return dimention1 *dimention2; // Area = length * width 
} 
} 
public class Main 
{ 
public static void main(String[] args) 
{ 
Scanner sc= new Scanner(System.in); 
Rectangle rectangle = new Rectangle(); 
Triangle triangle=new Triangle(); 
System.out.println("*****We have following shapes to calculate Area****”); 
System.out.println("1. Triangle"); 
System.out.println("2. Rectangle"); 
System.out.println("Enter Your choice :"); 
int ch=sc.nextInt(); 
if (ch == 1) 
{ 
System.out.println("Enter base and height of the triangle:"); 
double d1 = sc.nextDouble(); 
double d2 = sc.nextDouble(); 
triangle.inputData(d1,d2); 
double area = triangle.compute_area(); 
System.out.println("Calculated area of Triangle is : " + area); 
} 
else if (ch == 2) 
{ 
System.out.println("Enter length and width of the rectangle:"); 
double d1 = sc.nextDouble(); 
double d2 = sc.nextDouble(); 
rectangle.inputData(d1,d2); 
double area = rectangle.compute_area(); 
System.out.println("Calculated area of Rectangle is: " + area); 
} 
} 
} 
else 
{ 
} 
Output 
System.out.println("Invalid choice!"); 
return; 
*****We have following shapes to calculate Area***** 
1. Triangle 
2. Rectangle 
Enter Your choice : 
1 
Enter base and height of the triangle: 
3 
5 
Calculated area of Triangle is : 7.5


program5
interface Vehicle  
{ 
   public void changeGear(int newGear); 
   public void speedUp(int increment); 
   public void applyBreaks(int decrement); 
} 
class Bicycle implements Vehicle 
 { 
    private int speed; 
    private int gear; 
    public Bicycle() 
     { 
        this.speed = 0; 
        this.gear = 1; 
     } 
      public void changeGear(int newGear)  
      { 
         if (newGear > 0 && newGear <= 6)  
           { 
                 this.gear = newGear; 
                  System.out.println("Bicycle gear changed to: " + gear); 
           } 
        else  
         { 
            System.out.println("Invalid gear"); 
           } 
     } 
     public void speedUp(int increment)  
     { 
        speed = speed+increment; 
        System.out.println("Bicycle speed increased to: " + speed + " km/h"); 
     } 
      public void applyBrakes(int decrement)  
     {  
           if (speed > 0)  
          {         
             speed = speed-decrement; 
             System.out.println("Bicycle speed After applying break decreased to: " 
+ speed + " km/h"); 
        } 
    } 
} 
 class Bike implements Vehicle  
{ 
    private int speed; 
    private int gear; 
     public Bike()  
      { 
           this.speed = 0; 
            this.gear = 1; 
      } 
    
 
     public void changeGear(int newGear)  
     { 
          if (newGear > 0 && newGear <= 6)  
         { 
            this.gear = newGear; 
            System.out.println("Bike gear changed to: " + gear); 
         }  
        else  
         { 
            System.out.println("Invalid gear"); 
          } 
      } 
     public void speedUp(int increment)  
    { 
        speed = speed+increment; 
        System.out.println("Bike speed increased to: " + speed + " km/h"); 
     } 
    public void applyBrakes(int decrement)  
     { 
          if (speed > 0)  
        { 
            speed = speed-decrement; 
           System.out.println("Bike speed after applying gear decreased to: " + 
speed + " km/h"); 
          } 
        } 
    } 
 
 class Car implements Vehicle  
{ 
    private int speed; 
    private int gear; 
     public Car()  
     { 
        this.speed = 0; 
        this.gear = 1; 
      } 
    public void changeGear(int newGear)  
     { 
          if (newGear > 0 && newGear <= 6) 
         { 
                this.gear = newGear; 
                 System.out.println("Car gear changed to: " + gear); 
         }  
            else  
              { 
                   System.out.println("Invalid gear"); 
               } 
        } 
    public void speedUp(int increment)  
       { 
          speed = speed+increment; 
          System.out.println("Car speed increased to: " + speed + " km/h"); 
        } 
    public void applyBrakes(int decrement)  
        { 
if (speed > 0)  
{ 
speed = speed-decrement; 
System.out.println("Car speed after applying gear decreased to: " 
+ speed + " km/h"); 
} 
} 
} 
public class VehicleTest  
{ 
public static void main(String[] args)  
{ 
Vehicle bicycle = new Bicycle(); 
System.out.println("*********Bicycle Information*********"); 
bicycle.changeGear(2); 
bicycle.speedUp(10); 
bicycle.applyBrakes(5); 
System.out.println("\n*********Bike Information*********"); 
Vehicle bike = new Bike(); 
bike.changeGear(3); 
bike.speedUp(20); 
bike.applyBrakes(10); 
System.out.println("\n*********Car Information*********"); 
Vehicle car = new Car(); 
car.changeGear(4); 
car.speedUp(50); 
car.applyBrakes(20); 
} 
} 
Output 
*********Bicycle Information********* 
Bicycle gear changed to: 2 
Bicycle speed increased to: 10 km/h 
Bicycle speed After applying break decreased to: 5 km/h 
*********Bike Information********* 
Bike gear changed to: 3 
Bike speed increased to: 20 km/h 
Bike speed after applying gear decreased to: 10 km/h 
*********Car Information********* 
Car gear changed to: 4 
Car speed increased to: 50 km/h 
Car speed after applying gear decreased to: 30 km/h


program 6
import java.util.Scanner; 
 
public class ExceptionHandlingExample  
{ 
    public static void main(String[] args) 
 { 
        Scanner sc = new Scanner(System.in); 
try { 
                // User input for two numbers 
                  System.out.println("Enter the first number (Num1): "); 
                  String input1 = sc.nextLine(); 
                  System.out.println("Enter the second number (Num2): "); 
                 String input2 = sc.nextLine(); 
         
                 // Convert input strings to integers 
                 int num1 = Integer.parseInt(input1); 
                 int num2 = Integer.parseInt(input2); 
                 
                  int[] array = {10, 20, 30, 40, 50}; 
             
            int result = num1 / num2;  
            System.out.println("Result of division: " + result); 
            System.out.println("Value at index " + num1 + ": " +array[num1]); 
            System.out.println("Value at index " + num2 + ": " + array[num2]); 
        } catch (ArrayIndexOutOfBoundsException e)  
 
{ 
System.out.println("ArrayIndexOutOfBoundsException: " + e.getMessage()); 
}catch (NumberFormatException e)  
{ 
System.out.println("NumberFormatException: Invalid number format."); 
} catch (ArithmeticException e)  
{ 
System.out.println("ArithmeticException: Cannot divide by zero."); 
} finally  
{ 
} 
} 
} 
System.out.println("Program execution completed……….."); 
Output: 
Enter the first number (Num1):  
1 
Enter the second number (Num2):  
3 
Result of division: 0 
Value at index 1: 20 
Value at index 3: 40 
Program execution completed………… 
Enter the first number (Num1):  
abc 
Enter the second number (Num2):  
45 
NumberFormatException: Invalid number format. 
Program execution completed………… 
Enter the first number (Num1):  
8 
Enter the second number (Num2):  
5 
Result of division: 1 
ArrayIndexOutOfBoundsException: Index 8 out of bounds for length 5 
Program execution completed………… 
Enter the first number (Num1):  
4 
Enter the second number (Num2):  
0 
ArithmeticException: Cannot divide by zero.


program7
import java.util.*; 
import java.lang.*; 
import java.io.*; 
public class GenericFunctionExample 
{ 
 static int count = 0;  
 //Function to check palindrome 
 static void check_palindrome(String x) 
    { 
       StringBuilder s1 = new StringBuilder(x); 
       if(x.equals(s1.reverse().toString())) 
        { 
              System.out.println(x+" is a Palindrome"); 
              count += 1; //count the number of palindromes 
         } 
      else 
       { 
           System.out.println(x+" is not a Palindrome"); 
       } 
     } 
 //Function to check even or odd number 
  static void even_odd(int x) 
{ 
       if(x % 2 == 0) 
      { 
                        System.out.println(x+" is Even Number"); 
                     count += 1; //count the number of even numbers 
               } 
             else 
              { 
                   System.out.println(x+" is Odd Number"); 
              } 
       } 
//Function to check Prime Number 
      static void prime(int x) 
     { 
          boolean flag = false; 
         for(int i = 2; i <= x/2; i++) 
      { 
           if(x % i == 0) 
          { 
             flag = true; 
             break; 
        } 
    } 
       if (!flag) // flag ==false 
     { 
         System.out.println(x + " is a prime number."); 
        count += 1; //count the number of prime numbers 
     } 
   else 
     { 
          System.out.println(x + " is not a prime number."); 
   }  
 } 
static void check(int ch,int x) 
     { 
         switch(ch) 
      { 
            case 1: 
                       even_odd(x); //call even_odd fucntion for number x 
                       break; 
           case 2: 
                    prime(x); //call prime function for number x 
                    break; 
        default: 
              System.out.println("ENTER CORRECT OPTION"); 
        } 
    }  
//Function for integer Array 
   static void number_op() 
      { 
          int element, n, choice; 
         Scanner sc = new Scanner(System.in); 
       //ArrayList from Collection Interface 
       //Integer type 
        ArrayList<Integer> nums = new ArrayList<Integer>();  
        System.out.println("Enter the total number of elements:"); 
         n = sc.nextInt(); 
         System.out.println("Enter the elements:"); 
  
            for(int i=0;i<n;i++) 
            { 
                 element = sc.nextInt(); 
                 nums.add(element); //Add elements to the ArrayList 
            } 
          System.out.println("***You have following choice on Integer                        
Numbers****"); 
         System.out.println("1. Check Number is ODD or EVEN "); 
         System.out.println("2. Check Number is PRIME OR NOT"); 
         System.out.print("Enter your choice :"); 
          choice = sc.nextInt(); 
         Iterator itr = nums.iterator(); //Iterator from the COLLECTION interface 
         count = 0; 
        while(itr.hasNext()) 
        { 
 //Loop till there are elements in the ArrayList 
         check(choice,(int)itr.next()); //call the check function for each element 
       } 
          //Give the Count 
          if(choice == 1) 
         { 
           System.out.println("The number of Even numbers is: "+ count); 
           System.out.println("The number of Odd numbers is: "+ (nums.size()-  
                        count)); 
        } 
         else 
 
       { 
           System.out.println(" Number of Prime numbers is: "+ count); 
           System.out.println(" Number of Non-Prime numbers is: " 
                 +(nums.size()-count)); 
       } 
   }  
 //Function for String Array 
      static void string_op() 
    { 
        int n; 
        String word; 
     //ArrayList from COLLECTION interface 
      //String type 
       ArrayList<String> words = new ArrayList<String>(); 
       Scanner sc = new Scanner(System.in); 
       System.out.println("Enter the total number of elements:"); 
        n = sc.nextInt(); 
        System.out.println("Enter elements:"); 
        for(int i=0;i<n;i++) 
        { 
             word = sc.next(); 
             words.add(word); //Add elements to the ArrayList 
        } 
        count = 0; 
        for(String w:words){ //Loop the ArrayList 
        check_palindrome(w); 
      } 
  
         System.out.println("The Number of Palindrome is: "+ count); 
    } 
        // Main Function 
      public static void main(String[] args) 
     { 
          Scanner sc = new Scanner(System.in); 
          System.out.println("*****We have following data type to perform       
operations*****"); 
          System.out.println("1. Integer"); 
          System.out.println("2. String"); 
         System.out.print(“Enter your choice: ”); 
          int ch = sc.nextInt(); 
          if(ch == 1) 
            { 
               number_op(); //Calls Interger arraylist 
            } 
        else if(ch==2) 
          { 
             string_op(); //Calls String arraylist 
          } 
        else 
         { 
            System.out.println("Enter valid choice"); 
         } 
     } 
} 
 
Output 
*******We have following data type to perform operations******* 
1. Integer 
2. String 
Enter your choice: 1 
Enter the total number of elements: 
5 
Enter the elements: 
2 
3 
1 
4 
5 
***You have following choice on Integer  Numbers**** 
1. Check Number is ODD or EVEN  
2. Check Number is PRIME OR NOT 
Enter your choice :1 
2 is Even Number 
3 is Odd Number 
1 is Odd Number 
4 is Even Number 
5 is Odd Number 
The number of Even numbers is: 2 
The number of Odd numbers is: 3
