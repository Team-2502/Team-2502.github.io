---
layout: post
title: Day 1
categories: Java Guide
---

## Variables:
To store a value in Java one uses a variable. A variable assigns a value to a name. For example, to store the number of cats I owned I could declare a variable `catsOwned` to hold this value using the following syntax.

`data_type variable_name = value;`

To declare that I had 5 cats I would say

`int catsOwned = 5;`

Similarly, I could store my name in a variable using the same syntax but with a different data type `String`.

`String name = Ryan;`

I can also delcare a variable exists without giving in a value intitally.

`int dogsOwned;`

Also notice that all *decleration statements* (like the statements above) as well as expression statements (like the statements below) in Java must end with a semicolon.

Once a variable is declared using the above syntax it is then stored on the RAM of your computer to be accessed later. The value of a variable can be changed using an expression statement. For example suppose I acquire two dogs. I can access the variable `dogsOwned` which I declared before and change its value to 2.

`dogsOwned = 2;`

`name = Joe;`

Notice that since I already told Java the type(int) in the decleration statement, I don't need to mention the type again here and can just refer to the variable by its name.

#### A note on variable naming conventions

Variable names **cannot have a space**. Therefore the convention is to use either an underscore(`dogs_owned`) or camelCase(`dogsOwned`) to make it more readable. Variable names must also start with either a letter, _, or $ and **cannot start with a number**. 

Therefore both `2cats` and `two cats` are not valid variable names.

### Primitive Data Types
As you saw above, all variables in Java must be given a data type. The main data types you should know for now are booleans, ints, and doubles.

int: An int represents an integer and has a minimum value of -2^31 and a maximum value of 2^31-1. An int cannot reresent a decimal value. 

`int i = 1234;`

`int x = 12345;`

double: A double represents a floating point value, which means it can represent a decimal.

`double f = 12.34;`

`double e = 123.45;`

boolean: A boolean can have two values, either `true` or `false`.

`boolean b = true;`

`boolean c = false;`

### Reference Data Types
You may have noticed that `String` was not one of the primitve data types mentioned above. This is because `String` is a reference data type. This means that `String` is based on another Java class and not on a primitive type. Eventually you will be able to create your own reference data types, but for now `String`s are the main one you should know. Notice that because `String` is a reference data type it begins with a capital letter

String: A String is a sequence of unicode characters enclosed in double quotes.

`String s = "super";`

`String z = "2 zany zebras zapped with zeal";`

### Working with Variables
Expression statements can do much more than just assign a variable to a set value (`i = 6;`). If your variable has a type such as int or double, you can do mathematical operations such as addition or subtraction.

    int i = 9;
    i = i + 5;
    
In this case the new value of i will be 14 (5+9). As you can see we can access the current value of a variable by just typing the name of the variable(in this case i) once it is declared. Therefore the statement `i + 5` in this case really means `9 + 5` and evaluates to 14, which is then assigned to i. 

You can also subtract, multiply, and divide numbers as well using the -, *, and / characters respectively.

    int x = 4;
    x = x - 3;
    x = x * 10;
    x = x / 5;
    
## Printing Data
So you have created a bunch of variables and done operations with them. How do you actually see the results of your program? In this case "printing" does not mean printing to a sheet of paper, but instead printing to the terminal. To print data to the terminal use the line `System.out.println()` and then pass whatever you want to print as an argument inside the parentheses. 

    System.out.println("hello, world");
    System.out.println(7);
    
    int i = 5;
    System.out.println(i);
    
The previous block of code will print out

    hello, world
    7
    5
    
As you can see, you can print out the value of a variable by passing the name of the variable to the println function.

## Getting User Input
To dynamically change your programs, you can get input from the user. To do this, you will need to create a scanner object using the following line.
 
 `Scanner scan = new Scanner(System.in);`
 
 This creates a variable with the name scan that has the type Scanner. This is another reference type similar to the String type. To get input from the user you will have to call a method contained in the Scanner class using dot syntax.
 
 `int i = scan.nextInt();`
 
 This creates a variable i and sets the value of i to the result of scan.nextInt(). The . after scan tells Java you want to use one of scan's methods and the nextInt method allows the user to input an int. Remember that for the value to actually be saved by Java you have to assign the result of the nextInt() method to a variable. If you just did 
 
 `scan.nextInt();`
 
 you could get input from the user but you would have no way to access this value. Other useful methods you can call from the scan object are `scan.nextLine()` which gets a String from the user, and `scan.nextDouble()`, which gets a double from the user
 
 You only need to create one Scanner variable (in this case scan) and can call its methods multiple times. The following code example gets a number from the user and prints it out.
 
    int i = 0;
    Scanner scan = new Scanner(System.in);
    
    System.out.println("Input a number");
    i = scan.nextInt();
    System.out.println(i);
    
Also of note, to use the scanner you will have to import the class by including the following line at the very top of your class(line 1)

`import java.util.Scanner;`

This allows Java to find the Scanner class and allows you to use it in your program.
