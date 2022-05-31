# Operator-Overloading

## Aim:
 To write a C# program to find the volume of a box using operator overloading
 
 ## Algorithm:
 ### Step 1:
 Create a class for operator overloading

### Step 2:
Get inputs for length,breadth and height of the box from the user and then calculate the volume in overloading function

### Step 3:
After that return a new object for the calculated volume

### Step 4:
Then create a new object to store the return object

### Step 5:
After that print the calculated volume 
 
 ## Program:
 ```c#
 using System;

namespace ConsoleApp1
{
    class Program
    {
        public int length, breadth, height, volume;
        public static Program operator+(Program b1,Program b2)
        {
            Program b3=new Program();
            b1.volume = b1.length * b1.height * b1.breadth;
            b2.volume = b2.length * b2.height * b2.breadth;
            b3.volume = b1.volume + b2.volume;
            return b3;
        }
        static void Main(string[] args)
        {
            Program[] b = new Program[2];
            b[0] = new Program();
            b[1] = new Program();
            for(int i=0;i<2;i++)
            {
                Console.WriteLine("Enter Length of Box{0} is", i+1);
                b[i].length = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("Enter breadth of Box{0} is", i+1);
                b[i].breadth = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("Enter height of Box{0} is", i+1);
                b[i].height = Convert.ToInt32(Console.ReadLine());
            }
            Program b3 = new Program();
            b3 = b[0] + b[1];
            Console.WriteLine("Volume of Box1 = {0}\nVolume of Box2 = {1}\nVolume of Box3 = {2}",b[0].volume,b[1].volume,b3.volume);
        }
    }
}

 ```
 
 ## Output:
 ![Screenshot (2)](https://user-images.githubusercontent.com/75234807/170472241-57378bee-89c3-4dd8-b17e-8ed9466bf4e3.png)

 
 ## Result:
Thus the C# program to find the volume of a box using operator overloading is implemented successfully.
