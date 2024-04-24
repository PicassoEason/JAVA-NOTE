在 Java 中，每個應用程式都以類別名稱開頭，並且該類別必須與檔案名稱相符。

讓我們建立第一個 Java 文件，名為 Main.java，它可以在任何文字編輯器（如記事本）中完成。

該文件應包含一條「Hello World」訊息，其程式碼如下：
>主程式.java

    public class Main {
      public static void main(String[] args) {
        System.out.println("Hello World");
      }
    }


在 Java 中運行的每一行程式碼都必須位於class. 在我們的範例中，我們將類別命名為Main。
### !!!類別應始終以大寫首字母開頭。

注意： Java 區分大小寫：「MyClass」和「myclass」有不同的意義。

java 檔案的名稱必須與類別名稱相符。儲存檔案時，使用類別名稱儲存，並在檔案名稱末尾新增“.java”。

每個 Java 程式都有一個class必須與檔案名稱相符的名稱，並且每個程式都必須包含該 main()方法。
>注意：大括號標記{}程式碼區塊的開始和結束。

>System是一個內建的 Java 類，包含有用的成員，例如out，它是「output」的縮寫。該println()方法是“print line”的縮寫，用於將值列印到螢幕（或檔案）。

>不要太擔心System,out和println()。只需知道您需要將它們結合在一起才能將內容列印到螢幕上。

>每個代碼語句必須以分號 ( ;) 結尾。

    public class Main {
      public static void main(String[] args) {
        System.out.print("Hello World!");
        System.out.println("Peter,");
        System.out.println("Welcome.");
      }
    }
輸出結果:
    Hello World!Peter,
    Welcome.
### print()方法，與println()
System.out.print 和 System.out.println 唯一的區別是它不會在輸出末尾插入新行

println()，括號內可以是{數字or數字的運算式，ex:300 or 3 * 5}
不加""

### Variables
    public class Main{
      public static void main(String[] args){
        String name="Peter";
        System.out.println(name);
      }
    }
Type: String、int、float、char、boolean
**語法: type variablename = value;**
#### Sample 1
    public class Main {
      public static void main(String[] args) {
        String name = "John";
        int num = 100;
        int sum;
        sum=50;
        int amm=66;
        amm=77;
        System.out.println(name);//return name.
        System.out.println(num);//return 100.
        System.out.println(sum);//return 50.
        System.out.println(amm);//return 77.
      }
    }
value可以在一定義時就設好，也可先訂自變數名稱後再給value.
如果賦予已存在的變數新的值，將會覆寫先前的值。

**All Java variables must be identified with unique names.
These unique names are called identifiers.**

如果不希望自己或他人覆寫掉現有的值，可以在定義時前面加上 'final'
>final int amm=66;
>amm=77;// will generate an error: cannot assign a value to a final variable
>
>Other type of value: 
>>int myNum = 5;
>>float myFloatNum = 5.99f;
>>char myLetter = 'D';
>>boolean myBool = true;
>>String myText = "Hello";

# Data type
EX:int、float、char、boolean、String
## Primitive Data Type
**byte**	1 byte	Stores whole numbers from -128 to 127
**short**	2 bytes	Stores whole numbers from -32,768 to 32,767
**int**	    4 bytes	Stores whole numbers from -2,147,483,648 to 2,147,483,647
**long**	8 bytes	Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
**float**	4 bytes	Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits
**double**	8 bytes	Stores fractional numbers. Sufficient for storing 15 decimal digits
**boolean**	1 bit	Stores true or false values
**char**	2 bytes	Stores a single character/letter or ASCII values
## Non-primitive data types:
包含:String、Array、Classes、Interface
Non-primitive data types也叫reference type，因為會參考物件
和Primitive Data Type最主要的差別在於:

>1.Primitive Type在java是已經被定義的，而Non-primitive types是由程式設計師建立，在java沒有被定義(String例外)
>
>2.Non-primitive types可以用來呼叫methods來呈現特定操作，而Primitive Type不行
>
>3.Primitive Type一定會有值，而Non-primitive types可以是null.
>
>4.而Non-primitive types第一個字要大寫，Primitive Type則是小寫。
### Number
**Integer type:**
[byte:store whole numbers from -128 to 127.]
>byte myNum = 100;

[short:store whole numbers from -32768 to 32767]
>short myNum = 5000;

[int:store whole numbers from -2147483648 to 2147483647.]
>int myNum = 100000;

[long:The long data type can store whole numbers from -9223372036854775808 to 9223372036854775807]
**Note that you should end the value with an "L"**
>long myNum = 15000000000L;

Floating point type:
The float and double data types can store fractional numbers. Note that you should **end the value with an "f" for floats and "d" for doubles:**
>float myNum = 5.75f;
>double myNum = 19.99d;

Char:單一字母orASCII value.

# Type Casting
>Type casting is when you assign a value of one primitive data type to another type.

Widening Casting (automatically) - converting a smaller type to a larger type size
byte -> short -> char -> int -> long -> float -> double

Narrowing Casting (manually) - converting a larger type to a smaller size type
double -> float -> long -> int -> char -> short -> byte
## Widening Casting:(全自動)
        public class Main {
          public static void main(String[] args) {
            int myInt = 9;
            double myDouble = myInt; // Automatic casting: int to double

            System.out.println(myInt);      // Outputs 9
            System.out.println(myDouble);   // Outputs 9.0
          }
        }

## Narrowing Casting:(純手動)
```=java
    public class Main {
        public static void main(String[] args) {
            double myDouble = 9.78d;
            int myInt = (int) myDouble; // Manual casting:double to int
            System.out.println(myDouble);   // Outputs 9.78
            System.out.println(myInt);      // Outputs 9
        }
    }
```
## String
### String Length >> length()
    String txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
    System.out.println("The length of the txt string is: " + txt.length());
Other String Methods:
toUpperCase()、toLowerCase()。
```
public class Main {
  public static void main(String[] args) {
    String txt = "Hello World";
    System.out.println(txt.toUpperCase());
    System.out.println(txt.toLowerCase());
  }
}
```
### Finding a character in a string >> indexOf()
    public class Main{
        public static void main(String[] args){
            String txt="Please locate where 'locate' occurs!";
            System.out.println(txt.indexOf("locate"));
        }
    }
indexOf()函數會回傳特定text在String裡，第一次Occurrence的index(位置)，包含空白鍵。
**Java計算位置從0開始，0是第1個，1是第2個，2是第3個**
### String concatenation 
    public class Main {
      public static void main(String[] args) {
        String firstName = "John ";
        String lastName = "Doe";
        System.out.println(firstName.concat(lastName));
        System.out.println(firstName + lastName);
        System.out.println(firstName + "" + lastName);
      }
    }
上述三個輸出的都是:[John Doe]
Method:
(1)使用'+'，合併兩個String。
(2)使用concat()函數，合併Strings.
### 數字和字串
    public class Main {
      public static void main(String[] args) {
        int x = 10;
        int y = 20;
        int z = x + y;
        System.out.println(z);

        String a="11";
        String b="22";
        String c=a+b;
        System.out.println(c);

        String www=x+a;
        //int mmm=y+b;
        System.out.println(www);
        //System.out.println(mmm);
      }
    }
//省略是因為會出錯，**注意，Java使用'+'於addtion and concatenation。不同在於:數字用add，字串用concatenate**
### 特殊Character
由於字串必須要寫在雙括號裡面，如果字串中出現第二個雙括號會出現error
方法:
    Escape character	Result	Description
    \'	                 '	    Single quote
    \"	                 "	    Double quote
    \\	                 \	    Backslash
    \n                    New line
    \r                    迴車鍵
    \t                    Tab
    \b                    Backspace
### 運算符號
    public class Main {
      public static void main(String[] args) {
        int x = 5;
        int y = 3;
        System.out.println(x > y); // returns true, because 5 is higher than 3
      }
    }
傳回值為true和false.
### Math >>　Math.max(x,y)函數
    public class Main {
      public static void main(String[] args) {
        System.out.println(Math.max(5, 11));  
      }
    }
Math.max(x,y)函數，用來找出x和y之間最高的數，包含自己。
### Math >>　Math.min(x,y)函數
    public class Main {
      public static void main(String[] args) {
        System.out.println(Math.min(5, 11));  
      }
    }
Math.min(x,y)函數，用來找出x和y之間最小的數，包含自己。
### Math >>　Math.sqrt(x)函數
    public class Main {
          public static void main(String[] args) {
            System.out.println(Math.sqrt(64));//return 8.0; 
          }
        }
Math.sqrt(x)回傳x的開根號
### Math >>　Math.abs(x)函數 回傳x的絕對值。
### Math >>　Math.random()函數 回傳0.0(包含)~1.0(不包含)的隨機數，如果要讓範圍加大的話，可以這樣做:
    public class Main {
      public static void main(String[] args) {
        System.out.println(Math.random());
        int randomNum = (int)(Math.random() * 101);  // 0 to 100
        System.out.println(randomNum);
      }
    }
# Boolean :Boolean Values
    public class Main {
      public static void main(String[] args) {
        boolean isJavaFun = true;
        boolean isFishTasty = false;    
        System.out.println(isJavaFun);
        System.out.println(isFishTasty);
      }
    }
能夠在System.out.println()中，加入x > y >>System.out.println(x > y);

#### System.out.println()中，可以加入[> or < or == or >= or <=]
    public class Main {
      public static void main(String[] args) {
        int myAge = 25;
        int votingAge = 18;

        if (myAge >= votingAge) {
          System.out.println("Old enough to vote!");
        } else {
          System.out.println("Not old enough to vote.");
        }  
      }
    }
能搭配if...else
### if...else
    if (condition1) {
      // block of code to be executed if condition1 is true
    } else if (condition2) {
      // block of code to be executed if the condition1 is false and condition2 is true
    } else {
      // block of code to be executed if the condition1 is false and condition2 is false
    }
Use**if**to specify a block of code to be executed, if a specified condition is true
Use **else** to specify a block of code to be executed, if the same condition is false
Use **else** if to specify a new condition to test, if the first condition is false
Use **switch** to specify many alternative blocks of code to be executed

>Short Hand:variable = (condition) ? expressionTrue :  expressionFalse;

# Switch
    public class Main {
      public static void main(String[] args) {
          switch(expression) {
        case x:
          // code block
          break;
        case y:
          // code block
          break;
        default:
          // code block
            }
        }
    }
# Loop (while)
    public class Main{
        public static void main(String[] args){
            int i=0;
            while(i<5){
                System.out.println(i);
                i++;
            }
        }
    }
while(condition){//code}
# Loop (do...while)
    public class Main{
        public static void main(String[] args){
            int i=0;
            do{
                System.out.println(i);
                i++;
            }
            while(i<5);
        }
    }
# Loop (for)
    public class Main{
        public static void main(String[] args){
            for(int i=0;i<5;i++){
                System.out.println(i);
            }
        }
    }
for (statement 1; statement 2; statement 3) {// code}
# Nested loop
    public class Main{
        public static void main(String[] args){
            for(int i=1;i<=2;i++){
                System.out.println("Outer: " + i);
                for(int j=1;j<=3;j++){
                    System.out.println(" Inner: " + j);
                }
            }
        }
    }
# For-Each Loop
    public class Main{
        public static void main(String[] args){
            String[] cars={"Volvo","BMW","Ford","Mazda"};
            for(String i : cars){
                System.out.println(i);
            }
        }
    }
語法:for(type variablename : arrayname){code}
PS.break、continue

# Array
寫法:
>1.type[] arrayname; EX:String[] cars;
>2.EX:String[] cars={"Volvo", "BMW", "Ford", "Mazda"};
>3.numbers array: int[] mynum={10,20,30,40};
### Access the Elements of an Array by index number
    public class Main{
        public static void main(String[] args){
            String[] cars={"Volvo","BMW","Ford","Mazda"};
            System.out.println(cars[1]);
        }
    }
### Change the Elements of an Array by index number
    public class Main{
        public static void main(String[] args){
            String[] cars={"Volvo","BMW","Ford","Mazda"};
            System.out.println(cars[1]);
            cars[1]="Benz";
            System.out.println(cars[1]);
        }
    }
###  Array length
    public class Main{
        public static void main(String[] args){
            String[] cars={"Volvo","BMW","Ford","Mazda"};
            System.out.println(cars.length);
        }
    }
###  Array for loop
語法:
>for (type variable : arrayname) {
  ...
}
### 多維Array
Example:int[][]mynum={{1,2,3},{4,5,6}};
**能搭配for loop和Change the Elements of an Array by index number**

## 自定義函數:Methods
#### 1.create a method inside Main:
    public class Main{
        static void myMethod(){
        //code.
        }
    }
#### 呼叫函數 in main.可以呼叫多次
    public class Main {
      static void myMethod() {
        System.out.println("I just got executed!");
      }

      public static void main(String[] args) {
        myMethod();
      }
    }
###### 在myMethod()中帶入參數，String fname,int age
    public class Main {
      static void myMethod(String fname,int age) {
        System.out.println(fname + " Refsnes is "+age);
      }

      public static void main(String[] args) {
        myMethod("Liam",5);
        myMethod("Jenny",8);
        myMethod("Anja",31);
      }
    }
###### Method Overloading
    public class Main {
      static int plusMethod(int x, int y) {
        return x + y;
      }

      static double plusMethod(double x, double y) {
        return x + y;
      }

      public static void main(String[] args) {
        int myNum1 = plusMethod(8, 5);
        double myNum2 = plusMethod(4.3, 6.26);
        System.out.println("int: " + myNum1);
        System.out.println("double: " + myNum2);
      }
    }

Multiple methods can have the same name with different parameters。
多個擁有相同名稱的函數，但帶入不同的參數

### 範圍Scope
變數只能在它們建立的區域內存取。這稱為 範圍。
程式碼區塊指的是大括號之間的所有程式碼{}。
### 遞迴:停止條件Halting Condition
    public class Main {
      public static void main(String[] args) {
        int result = sum(5, 10);
        System.out.println(result);
      }
      public static int sum(int start, int end) {
        if (end > start) {
          return end + sum(start, end - 1);
        } else {
          return end;
        }
      }
    }
# Java 物件導向
類別是物件的模板，物件是類別的實例。
建立各個物件時，它們會繼承該類別的所有變數和方法。
### Step 1.建立class(類別)，keyword: class
    public class Main{
        int x=5;
    }
注意:class的命名的字首都必須是大寫
### Step 2.建立object(物件)，keyword: new
    public class Main{
            int x=5;
            public static void main(String[] args) {
                Main myobj=new Main();
                System.out.println(myobj.x);
            }
    }
### Step 3.多個object(物件)
    public class Main{
            int x=5;
            public static void main(String[] args) {
                Main myobj1=new Main();
                Main myobj2=new Main();
                System.out.println(myobj1.x);
                System.out.println(myobj2.x);
            }
    }
### Class Attributes
    public class Main {
      int x = 5;
      int y = 3;
    }
上述範例是create a class 'Main'，有兩個attribute x,y:
### Access attribute，by (.):
    public class Main {
      int y = 3;
      public static void main(String[] args) {
        Main myObj = new Main();
        System.out.println(myObj.y);
      }
    }
### 變更attribute
    public class Main {
      int x ;
      int y = 3;
      public static void main(String[] args) {
        Main myObj = new Main();
        myObj.x=10;//set x value 10.
        myObj.y=5;// override existing value
        System.out.println(myObj.x);
        System.out.println(myObj.y);
      }
    }
### 為了不覆蓋掉現有的value，keyword:final
    public class Main {
          final int y = 3;
          public static void main(String[] args) {
            Main myObj = new Main();
            myObj.x=10;//會出現error，不能賦予final變數value.
            System.out.println(myObj.y);
         }
    }
### 多個object
    public class Main {
      int x = 5;

      public static void main(String[] args) {
        Main myObj1 = new Main();  // Object 1
        Main myObj2 = new Main();  // Object 2
        myObj2.x = 25;
        System.out.println(myObj1.x);  // Outputs 5
        System.out.println(myObj2.x);  // Outputs 25
      }
    }
>Change the value of x to 25 in myObj2, and leave x in myObj1 unchanged
### 多個attribute
    public class Main {
      String fname = "John";
      String lname = "Doe";
      int age = 24;

      public static void main(String[] args) {
        Main myObj = new Main();
        System.out.println("Name: " + myObj.fname + " " + myObj.lname);
        System.out.println("Age: " + myObj.age);
      }
    }
# Class Methods
>簡單來說就是將上一步的屬性換成函數

    public class Main{
        stasic void mymethod(){
            System.out.println("Hello.");
        }
        public static void main(String[] args){
            mymethod();//Output "Hello."
        }
    }
在main呼叫mymethod().
### Static and Public
    public class Main {
      // Static method
      static void myStaticMethod() {
        System.out.println("Static methods can be called without creating objects");
      }

      // Public method
      public void myPublicMethod() {
        System.out.println("Public methods must be called by creating objects");
      }

      // Main method
      public static void main(String[] args) {
        myStaticMethod(); // Call the static method
        // myPublicMethod(); This would compile an error

      Main myObj = new Main(); // Create an object of Main
      myObj.myPublicMethod(); // Call the public method on the object
      }
    }
static:可以不用在class建立object就能呼叫
public:只能access by object才能呼叫
### Access methods with an object
    public class Main {

      // Create a fullThrottle() method
      public void fullThrottle() {
        System.out.println("The car is going as fast as it can!");
      }

      // Create a speed() method and add a parameter
      public void speed(int maxSpeed) {
        System.out.println("Max speed is: " + maxSpeed);
      }

      // Inside main, call the methods on the myCar object
      public static void main(String[] args) {
        Main myCar = new Main();   // Create a myCar object
        myCar.fullThrottle();      // Call the fullThrottle() method
        myCar.speed(200);          // Call the speed() method
      }
    }
建立名為myCar的Car object,在myCar object上呼叫fullThrottle() and speed()函數
注意:
>(.)用來訪問object的attribute和methods.要呼叫method in Java，要加()和;，
>如果你有一個名為 Main 的類，那麼你的源文件的文件名必須是 Main.java。
### 使用多個class
    Main.java
    public class Main {
      public void fullThrottle() {
        System.out.println("The car is going as fast as it can!");
      }

      public void speed(int maxSpeed) {
        System.out.println("Max speed is: " + maxSpeed);
      }
    }
    Second.java
    class Second {
      public static void main(String[] args) {
        Main myCar = new Main();     // Create a myCar object
        myCar.fullThrottle();      // Call the fullThrottle() method
        myCar.speed(200);          // Call the speed() method
      }
    }
In this example, we have created two files in the same directory:
>1.Main.java
>2.Second.java

# Java Class Attributes
    public class Main{
        int x=5;
        int y=3;
    }
Create a class called "Main" with two attributes: x and y
### 訪問attribute，用(.)
    public class Main{
        int x=10;
        public static void main(String[] args){
            Main myobj=new Main();
            System.out.println(myobj.x);
        }
    }
Create an object called "myObj" and print the value of x
如果沒有特別宣告 預設是private 要建立物件，才能存取值
只有static 才能不須建立物件然後直接取用
### 變更attribute，1.給予value，2.覆蓋掉原有值
    public class Main{
        int y=10;
        int x;//原本沒有值
        public static void main(String[] args){
            Main myobj=new Main();
            myobj.x=20;
            myobj.y=40;
            System.out.println(myobj.x);//接收值後
            System.out.println(myobj.y);//更改值後
        }
    }
如果不希望覆蓋掉原有的值，要使用keyword:**final**
>public class Main{
    final int x=5;
    //
}
The final keyword is useful when you want a variable to always store the same value, like PI (3.14159...).

The final keyword is called a "modifier".
### 多個 object in one class
    public class Main{
            int x=10;
            public static void main(String[] args){
                Main myobj1=new Main();
                Main myobj2=new Main();
                myobj2.x=40;
                System.out.println(myobj1.x);
                System.out.println(myobj2.x);
        }
    }
### 多個 attribute
    public class Main{
        String fname="Chou";
        String lname="Bruce";
        int age=22;
        public static void main(String[] args){
            Main myobj=new Main();
            System.out.println("Name:"+myobj.lname+" "+myobj.fname+"\nAge:"+myobj.age);
        }
    }
# Java Class Methods
```
public class Main{
    static void mymethod(){
        System.out.println("Yahoo");
    }
    public static void main(String[] args){
        mymethod();
    }
}
```
建立自訂義method，並呼叫。
### Static vs. Public
```
public class Main {
  static void myMethod1() {
    System.out.println("Hello World!");
  }

  public void myMethod2() {
    System.out.println("Yahoo.");
  }
  public static void main(String[] args) {
    myMethod1();

    Main myobj=new Main();
    myobj.myMethod2();
  }
}
```
Static:不需要建立object即可直接訪問
Public:只能藉由object訪問
兩個的正式名稱是modifier

### 藉由object訪問method
```
public class Main{
    public void speed(int maxspeed){
        System.out.println("Speed:"+maxspeed);
    }
    public void fullthrottle(){
        System.out.println("The car is going as fast !");
    }
    public static void main(String[] args){
        Main mycar=new Main();
        mycar.fullthrottle();
        mycar.speed(300);
    }
}
```
### 使用多個class
```
1.Main.java
public class Main {
  public void fullThrottle() {
    System.out.println("The car is going as fast as it can!");
     }

  public void speed(int maxSpeed) {
    System.out.println("Max speed is: " + maxSpeed);
  }
}
```

```
2.Second.java
class Second{
    public static void main(String[] args){
        Main mycar=new Main();
        mycar.fullThrottle();
        mycar.speed(200);
    }
}
```
# Java Constructors 建構函數: 
>The constructor is called when an object of a class is created. It can be used to set initial values for object attributes
```
// Create a Main class
public class Main {
  int y=10;
  int x;

  // Create a class constructor for the Main class
  public Main() {
    x=5;
    y=20;
  }

  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj.x);//output 5
    System.out.println(myObj.y);//output 20
  }
}
```
A special method that is used to initialize(初始化) objects.
請注意，建構函數名稱必須與類別名稱匹配，並且它不能有 返回類型（如void）。
另請注意，創建物件時會呼叫建構函數。
預設情況下，所有類別都有建構函數：如果您沒有自己建立類別建構函數，Java 會為您建立一個。但是，您將無法設定物件屬性的初始值。
### 構造函數也可以接受參數，用於初始化屬性。
```
public class Main{
    int x;
    public Main(int y){
        y=x;
    }
    public static void main(String[] args){
        Main myobj=new Main(5);
        System.out.println(myobj.x);
    }
}
//一個參數or多個參數
public class Main{
    int age;
    String name;
    public Main(int Age,String Name){
        age=Age;
        name=Name;
    }
    public static void main(String[] args){
        Main mydog=new Main(20,"John");
        System.out.println("Dog`s age and name:"+mydog.age+","+mydog.name);
    }
}
```
>建構值的檔案名稱一定要一樣。

# Java Modifiers
public class Main，其中 public 是 access modifier，用於設定類別、屬性、方法和建構函數的存取等級。
We divide modifiers into two groups:

Access Modifiers - 控制存取級別
Non-Access Modifiers - 不控制存取級別，但提供其他功能

### Access Modifiers for class:
    public class Main {
          public static void main(String[] args) {
            System.out.println("Hello World");
          }
        }
        //上:public，下:default
    class Main {
          public static void main(String[] args) {
            System.out.println("Hello World");
          }
        }
>public:class is accessible by any other class
>default:The class is only accessible by classes in the same package. This is used when you don't specify a modifier.
### Access Modifiers for attribute:
```
public class Main {
  public String fname = "John";
  public String lname = "Doe";
  public String email = "john@doe.com";
  public static void main(String[] args){
  Main myobj = new Main();
  	System.out.println(myobj.fname+ "," + myobj.lname +"," + myobj.email);
  }
    }//public，並在其他class呼叫
```


```
public class Main {
  private String fname = "John";
  private String lname = "Doe";
  private String email = "john@doe.com";
  private int age = 24;

  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println("Name: " + myObj.fname + " " + myObj.lname);
    System.out.println("Email: " + myObj.email);
    System.out.println("Age: " + myObj.age);
  }
}//private
```


```
class Person {
  String fname = "John";
  String lname = "Doe";
  String email = "john@doe.com";
  int age = 24;

  public static void main(String[] args) {
    Person myObj = new Person();
    System.out.println("Name: " + myObj.fname + " " + myObj.lname);
    System.out.println("Email: " + myObj.email);
    System.out.println("Age: " + myObj.age);
  }
}//default
```


```
class Person {
  protected String fname = "John";
  protected String lname = "Doe";
  protected String email = "john@doe.com";
  protected int age = 24;
}

class Student extends Person {
  private int graduationYear = 2018;
  public static void main(String[] args) {
    Student myObj = new Student();
    System.out.println("Name: " + myObj.fname + " " + myObj.lname);
    System.out.println("Email: " + myObj.email);
    System.out.println("Age: " + myObj.age);
    System.out.println("Graduation Year: " + myObj.graduationYear);
  }
}//protected
```


>public:The code is accessible for all classes
>private:The code is only accessible within the declared class
>default:The code is only accessible in the same package. This is used when you don't specify a modifier. 
>protected:The code is accessible in the same package and subclasses.
### Non-Access Modifiers for attribute and methods:
Modifiers:
*     **final**:屬性和函數不能被更改或覆蓋
*     **static**:屬性和函數屬於class，而非object。
*     **abstract**:Can only be used in an abstract class, and can only be used on methods. The method does not have a body,the body is provided by the subclass (inherited from).抽象的類別不能用來生成物件。
*     **transient**:序列化包含屬性和方法的物件時會跳過他們
*     **synchronized**:方法只能被一個執行序訪問
*     **volatile**:屬性的值不會在本地緩存，而且始終從'主內存'中讀取
### Non-Access Modifiers for class:final,abstract
```
final class Vehicle{
    protected String brand="Ford";
    public void honk(){
        System.out.println("Bon");
    }
}//final:the class 不能被其他class繼承
    
Main.java:
// abstract class
abstract class Main {
     public abstract void study();  
}// abstract method

// Subclass (inherit from Person)
class Student extends Main {
     public int graduationYear = 2018;
     public void study() {
    System.out.println("Studying all day long");
     }
}
Second.java:
class Second {
     public static void main(String[] args) {
    // create an object of the Student class (which inherits attributes and methods from Main)
    Student myObj = new Student(); 
    System.out.println("Graduation Year: " + myObj.graduationYear);
    myObj.study(); // call abstract method
     }
}
//abstract:The class cannot be used to create objects (To access an abstract class, it must be inherited from another class. 
```
存取範圍大小：公開＞預設＞保護＞私有


### Example of final:
```
public class Main {
  final int x = 10;
  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj.x); 
  }
}
```
### Example of static:
```
public class Main {
  // Static method
  static void myStaticMethod() {
    System.out.println("Static methods can be called without creating objects");
  }
  // Main method
  public static void main(String[] args) {
    myStaticMethod(); // Call the static method
  }
}
```
### Example of abstract:
```
//Main.java
class Second {
  public static void main(String[] args) {
    // create an object of the Student class (which inherits attributes and methods from Main)
    Student myObj = new Student(); 
    myObj.study(); // call abstract method
  }
}
//Second.java
class Second {
  public static void main(String[] args) {
    // create an object of the Student class (which inherits attributes and methods from Main)
    Student myObj = new Student(); 
    myObj.study(); // call abstract method
  }
}
```
# Encapsulation  封裝:
### 確保隱藏"重要資料" keyword:private
>宣告class variable/attribute as private
>提供public取得(get)和設置(set)method來存取和更新private的值
### Get / Set
```
Person.java
public class Person{
    private String name;//無法從this class外access
    public String getName(){
        return name;
    }//Getter
    public void setName(String newname){
        this.name=newname;／／Setter
    }
}
Main.java
public class Main{
    public static void main(String[] args){
        Person myobj=new Person;
        myobj.setName("Ya");
        System.out.println(myObj.getName());
    }
}
```
解釋:
>this:此keyword指的是目前的object
>why:
>>更好控制class attributes and methods
>>Class attributes可設為:唯獨or唯寫
>>增加資料安全性
>>只需修改部分code而不影響其他部分
# Java Packages & API
Package: to group relate classes. like a folder in a file directory.
用處:避免name conflict,並能更好的對程式做維護。
Package分兩種:
>Built-in Packages (packages from the Java API) 內建
>User-defined Packages (create your own packages) 自訂義

### (1)Built-in Packages(packages from the Java API)
The Java API is a library of prewritten classes, that are free to use, included in the Java Development Environment.

其中:library分成 packages and classes.

也就是，你可以只import單個class，也可以import整個包含多個classes的package.

語法:
>import package.name Class;   //import a single class
>import package.name.*;      //import a whole package
### import a class, use **Scanner** class for example.
>ps.Scanner class:use for get user input.

EX: **import java.util.Scanner;**
上述例子，java.util is a package,Scanner是java.util這個package裡面的一個class.

### **Using the Scanner class to get user input:**
```=java
import java.util.Scanner;// import the Scanner class
class MyClass{
    public static void main(String[] args){
        Scanner myobj = new Scanner(System.in);
        String username;
        // Enter username and press Enter
        System.out.println("Enter Name:");
        username=myobj.nextLine();
        System.out.println("Username: "+username);
    }
}
```
### import a package,use (*)
>下列將舉例import all classes in java.util package 
EX: **import java.util.*;**

### User-defined Packages
Java uses a file system directory to store them. 
![image](https://hackmd.io/_uploads/S1piGNznT.png)
**create a package,keyword:package**
##### Mypackageclass.java
```=
package mypack;
class Mypackageclass{
    public static void main(String[] args){
        System.out.println("This is my package!");
    }
}
```
>Notice: The package name should be written in lower case to avoid conflict with class names.

# Inheritance 繼承 
## Subclass(子) and Superclass(父)，keyword:extends
```=
class Vehicle{
    protected String brand="Ford"; //vehicle attribute.
    //如果protected是private，Car class則無法access.
    public void honk(){            //vehicle method.
        System.out.println("Bon! Bon!");
    }
}
class Car extends Vehicle{
    private String carname=" Savilo";//Car attribute.
    public static void main(String[] args){
        Car mycar=new Car();//create a mycar object.
        System.out.println(mycar.brand+""+mycar.carname);
        // Display the value of the brand attribute (from the Vehicle class) and the value of the carname from the Car class.
        mycar.honk();
        //Call the honk() method (from the Vehicle class) on the mycar object.
    }
}
```
Subclass(子):the class that inherits from another class
Superclass(父):the class being inherited from
### keyword:final
If you don't want other classes to inherit from a class, use the final keyword.
If you try to access a final class, Java will generate an error
![image](https://hackmd.io/_uploads/BJOSpsVbR.png)

# Polymorphism
Many forms,related by inheritance.
Use methods to perform different tasks=perform a single action in differnet ways.
### Example
```
class animal{
    public void sound(){
        System.out.println("The animal makes a sound.");
    }
}
class pig extends animal{
    public void sound(){
        System.out.println("Wee.");
    }
}
class cat extends animal{
    public void sound(){
        System.out.println("Meow.");
    }
}
class Main{
    public static void main(String[] args){
        animal myanimal=new animal();
        animal mypig=new pig();
        animal mycat=new cat();
        myanimal.sound();
        mypig.sound();
        mycat.sound();
    }
}
```
# Java Inner Class
## class裡面有class{nested classes}
Group classes that belong together.
要連接inner class,create an object of the outer class,then create an object of the inner class.
### Regular Example
```
class Outer{
    int x=5;
    class Inner{
        int y = 44;
    }
}
public class Main{
    public static void main(String[] args){
        Outer myoutobj=new Outer();
        Outer.Inner myinobj=myoutobj.new Inner(); 
        System.out.println(myinobj.y+myoutobj.x);
    }
}
```
### Private Inner Class，可以是private/protected
```
class Outer{
    int x=5;
    private class Inner{
        int y = 44;
    }
}
public class Main{
    public static void main(String[] args){
        Outer myoutobj=new Outer();
        Outer.Inner myinobj=myoutobj.new Inner(); 
        System.out.println(myinobj.y+myoutobj.x);
    }
}
```
>return error,because inner class is private.
>想取得y，可以將private class Inner改成static class Inner即可
### Static Inner Class
```
class Outer{
    int x=5;
    static class Inner{
        int y = 44;
    }
}
public class Main{
    public static void main(String[] args){
        Outer.Inner myinobj=new Outer.Inner();
        System.out.println(myinobj.y);
    }
}
```
>static can access without creating object of outer class.
>a static inner class does not have access to members of the outer class.
### Access Outer class from Inner class
```
class Outer{
    String x="Hope.";
    class Inner{
        public String myinmethod(){
            return x;
        }
    }
}
public class Main{
    public static void main(String[] args){
        Outer myoutobj = new Outer();
        Outer.Inner myinobj= myoutobj.new Inner();
        System.out.println(myinobj.myinmethod());
    }
}
```
>inner classes的優勢就是，可以access attribute and methods of outer class.
# Abstraction
Data abstraction:隱藏重要details和只顯示必要的資訊給user。
Abstraction可以藉由abstraction classes和interfaces(接下來才會教)來達成。
## keyword:abstract,non-access modifier
```
abstract class Animal{
     public abstract void sound();
     public void sleep(){
      System.out.println("wee");
   }
}
```
>Abstract class:受限制的class，不能用於建立object(要存取必須從另一個class繼承)。可以同時有abstract and regular methods.
>Abstract method:只能用於Abstract class，沒有body(提供by subclass).
>To access the abstract class, it must be inherited from another class. 若想使用抽象類別，就要用繼承了抽象類別的子類別
>上述例子如果加上[Animal myobj=new Animal();]會出現error.
### Exapmle
```
//abstract class
abstract class Animal{
    public abstract void sound();abstract method(沒有body)
    public void sleep(){//regular method
        System.out.println("ZZZ");
    }
}
//subcalss inherit from Animal
class Pig extends Animal{
    public void sound(){
        System.out.println("gon");
        //the body of sound() provided here.
    }
}
class Main{
    public static void main(String[] args){
        Pig mypig=new Pig();
        //建立a pig object.
        mypig.sound();
        mypig.sleep();
    }
 }
```
# Interface
### keyword:interface、implements
能達成abstraction in Java，is interface.
An interface=abstract class，用於group related methods(只有名字卻沒有body)
### Example
```
//interface
interface Animal{
  public void animalsound();
  public void run();
  //both interface method don`t have body.
}
```
### Access interface method.

```
//interface
interface Animal{
  public void animalsound();
  public void run();
  //both interface method don`t have body.
}

class Pig implements Animal{
    //Pig "implements" the Animal interface
    //Need to rewrite all methods in interface.
  public void animalsound(){
    System.out.println("Wee Wee.");
    //body of animalsound() is provided here.
  }
  public void run(){
    System.out.println("40km per hour.");
    //body of run() is provided here.
  }
}
class Main{
    public static void main(String[] args){
      Pig mypig=new Pig();
      mypig.animalsound();
      mypig.run();
    }
}
```

>用implements,類似繼承的(extends)
>
>interface methods body由"implement"的class提供
>
>和abstract classes一樣，不能用來create object.
>
>interface methods沒有body,body由"implement"class提供.
>
>在實作interface時,必須要重新複寫所有methods.
>
>interface methods被默認為abstract和public.
>
>interface attribute被默認為public、static、final.
>
>interface不能包含construct.
>
### 使用interface的理由和時機
* security(隱藏特定細節只顯示物件的重要細節(interface))
* Java不支持"multiple inheritance"(a class can only inherit from one superclass)
* 但可以用Interface來實現，因為class可以implement多個interfaces.
### 執行Multiple interfaces,用(,)分隔
```
interface Firstinterface{
  public void mymethod1();
}
interface Secondinterface{
  public void mymethod2();
}
class Democlass implements Firstinterface,Secondinterface{
  public void mymethod1(){
    System.out.println("Some text...");
  }
  public void mymethod2(){
    System.out.println("Yahoo~");
  }
}
class Main{
  public static void main(String[] args){
    Democlass mydemo=new Democlass();
    mydemo.mymethod1();
    mydemo.mymethod2();
  }
}
```
# Java Enums
* keyword:enum, 代表一群constants(不可改變的變數，似final變數)
* 使用 enum 可以讓程式碼更加清晰和易於維護，因為它能夠將相關聯的常數聚合在一起。
* 通常情況下，我們會使用 enum 來定義一組固定的常量集合，例如表示星期幾、顏色、狀態等。
* 使用 enum 的優點之一是它能夠幫助我們避免使用數字或字串表示常量，這樣能夠提高程式碼的可讀性和可維護性。
* 此外，enum 還可以具有方法和屬性，使得我們可以將行為和數據封裝在一個 enum 常量中。
* 常量集合在 Java 中通常使用全大寫字母表示，這是一種習慣和慣例，有助於提高程式碼的可讀性和可理解性。
* 這樣做的好處是可以清楚地將常量與變數區分開來，讓程式碼更易於理解。
* **Why use enum?**
* **Use enums當你知道你的value不會變,like:day,color.**
### access enum constants 
with the dot syntax:  **Day today=Day.SUNDAY;**
```
//example 1
enum Day{
        MONDAY,TUESDAY,WEDNESDAY,THURSDAY,
        FRIDAY,SATURDAY,SUNDAY
    }
public class Main{
    public static void main(String[] args){
        Day today=Day.SUNDAY;
        System.out.println(today);
    }
    
}
```
### Enum in a class
```
//example 2
public class Main{
    enum Day{
        MONDAY,TUESDAY,WEDNESDAY,THURSDAY,
        FRIDAY,SATURDAY,SUNDAY
    }
    public static void main(String[] args){
        Day today=Day.SUNDAY;
        System.out.println("What day is today? " + today);
    }
    
}
```
### Enum in a Switch
```
public class Main{
    enum Day{
        MONDAY,TUESDAY,WEDNESDAY,THURSDAY,
        FRIDAY,SATURDAY,SUNDAY
    }
    public static void main(String[] args){
        Day today=Day.FRIDAY;
        switch(today){
        	case MONDAY:
            	System.out.println("Blue Day.");
                break;
            case FRIDAY:
            	System.out.println("Happy Day.");
                break;
        }
    }  
}
```
### Loop through an Enum,key method:value()
value():回傳一個陣列包含所有的enum constants.
```
public class Main{
    enum Day{
        MONDAY,TUESDAY,WEDNESDAY,THURSDAY,
        FRIDAY,SATURDAY,SUNDAY
    }
    public static void main(String[] args){
        //Day today=Day.SUNDAY;
        //System.out.println("What day is today? " + today);
        for(Day today : Day.values()){
        	System.out.println(today);
        }
    }
    
}
```
### Enum class example:
```
import java.util.InputMismatchException;
import java.util.Scanner;

public class Main {
    public enum Inch {
        SMALL(150), MEDIUM(200), BIG(300);
        private final int price;
        Inch(int price) { this.price = price; }
        public int getprice() { return price; }
    }

    public static void main(String[] args) {
        Scanner num = new Scanner(System.in);
        int cakesize,price=0;
        System.out.print("Enter size: ");
        cakesize = num.nextInt();
        switch (cakesize) {
            case 6 : price = Inch.SMALL.getprice();break;
            case 8 : price = Inch.MEDIUM.getprice();break;
            case 12 : price = Inch.BIG.getprice();break;
            default : throw new IllegalArgumentException("Invalid size");
        };
        System.out.println(price);
    }
}
```
### class 和 enum 的差別
enum 其實和class很像，有attributes,methods.
>唯一的不同是enum constants are {public,static,final(不可變、不能被覆寫)}
>enum不能用來建立objects.也不能擴展其他類別（extends）
>擴展（extends）通常用於建立一個新的類別，這個新類別繼承了某個父類別的屬性和方法。
>然而，對於 enum 來說，它是一個特殊的類型，不能擴展其他類別。
>但是，enum 可以實現（implements）一個或多個介面（interface），這使得 enum 在某些情況下仍然可以與其他類別進行相互作用。
### Enum + Interface的 example:
```
//interface part, need to be put in another file
public interface Operation {
  int apply(int a, int b);
}

//enum part, need to be put in another file
public enum SimpleOperations implements Operation {
  PLUS {
    @Override
    public int apply(int a, int b) {
      return a + b;
    }
  },
  MINUS {
    @Override
    public int apply(int a, int b) {
      return a - b;
    }
  }
}


//Main2 part, need to be put in another file
public class Main2 {
  public static void main(String[] args) {
    int num1 = 10;
    int num2 = 5;

    // Use enum to choose the operation
    SimpleOperations operation1 = SimpleOperations.PLUS;
    SimpleOperations operation2 = SimpleOperations.MINUS;
    
    // Apply the operation using the interface method
    int result1 = operation1.apply(num1, num2);
    int result2 = operation2.apply(num1, num2);
    System.out.println("Result1: " + result1); // Output: Result: 15
    System.out.println("Result2: " + result2); // Output: Result: 5
  }
}
```

# Java User Input
keyword:Scanner{a class to get user input}
package:java.util
要使用Scanner這個class,要建立物件of the class,並用Scanner這個class document中任何可行的方式.ex:**nextLine()**,用來讀取String
```
import java.util.Scanner;  // Import the Scanner class
class Main {
  public static void main(String[] args) {
    Scanner myObj = new Scanner(System.in);  // Create a Scanner object
    System.out.println("Enter username");
    String userName = myObj.nextLine();  // Read user input
    System.out.println("Username is: " + userName);  // Output user input
  }
}
```
### Input types:
上面的例子:nextLine(),用來讀取String。接下來介紹如何讀取其他type

| Method        | Explaination                  |
| ------------- | ----------------------------- |
| nextBoolean() | read a boolean value from use |
| nextByte()    | read a byte from user         |
| nextFloat()   | read a float from user        |
| nextInt()     | read a int value from user    |
| nextLine()    | read a String value from user |
| nextLong()    | read a long value from user   |
| nextShort()   | read a short value from user  |
| nextDouble()  | read a double value from user |

```
import java.util.Scanner;
class Main{
	public static void main(String[] args){
		Scanner myobj=new Scanner(System.in);
		System.out.println("Enter name,age and salary: ");
		String name=myobj.nextLine();//String input
		int age=myobj.nextInt();// Numerical input
		double salary=myobj.nextDouble();
		System.out.println("Name: "+name);
		System.out.println("Age: "+age);
		System.out.println("Salary: "+salary);
	}
}
```
### Notice:當輸入錯誤的資料型態時，會出現error。
```
import java.util.Date;  // import the Date class
public class Main {
    public static void main(String[] args) {
        Date myObj = new Date(); // Create a date object
        String x = myObj.toString(); // Note the correct variable name myObj
        System.out.println(x); // Display the current date
    }
}
```
# Date and Time, package keyword:java.time
1.LocalDate:表示日期(year,month,day)>(yyyy-MM-dd)
2.LocalTime:表示時間(hour,minute,second and毫秒)(HH-mm-ss-ns)
3.LocalDateTime:表示日期和時間(yyyy-MM-dd-HH-mm-ss-ns)
4.DateTimeFormatter:格式化展示和解析物件的日期和時間
### 展示當前日期
```
import java.time.LocalDate;// import the LocalDate class
public class Main{
	public static void main(String[] args){
    	LocalDate myobj=LocalDate.now();// Create a date object
        System.out.println(myobj);// Display the current date
    }
}
```
### 展示當前日期 as String way
```
import java.time.LocalDate;  // import the LocalDate class

public class Main {  
  public static void main(String[] args) {  
    LocalDate myObj = LocalDate.now();  // Create a date object
    String x= (String)myobj;
    System.out.println(x);  // Display the current date
  }  
}  
```
### 展示當前時間
```
import java.time.LocalTime;// import the LocalTime class
public class Main{
	public static void main(String[] args){
    	LocalTime myobj=LocalTime.now();
        System.out.println(myobj);
    }
}
```
### 展示當前日期和時間
```
import java.time.LocalDateTime;  
public class Main {  
  public static void main(String[] args) {  
    LocalDateTime myObj = LocalDateTime.now();
    System.out.println(myObj);
  }  
}  
```
### 格式化時間和日期
```
import java.time.LocalDateTime;
import java.time.format.DateTimeFormatter;

public class Main {  
  public static void main(String[] args) {  
    LocalDateTime myobj = LocalDateTime.now();
    System.out.println("Before: "+ myobj);
    DateTimeFormatter myformatobj=DateTimeFormatter.ofPattern("dd-MM-yyyy HH:mm:ss");
    String formatDate=myobj.format(myformatobj);
    System.out.println("After: "+formatDate);
  }  
}  
```
### 其中，ofPattern()
接受各種value的排序
* yyyy-MM-dd    "1988-09-29"
* dd/MM/yyyy    "29/09/1988"
* dd-MMM-yyyy   "29-Sep-1988"
* E,MMM dd yyyy "Thu, Sep 29 1988"

# Java ArrayList
### keyword: import java.util.ArrayList;
內建的array大小無法作變更:如果要對元素做變更(+、-)，要建立新的array物件。
ArrayList:可以隨意對元素進行變更(+、-)
### 語法:
```
import java.util.ArrayList;
// import the ArrayList class

public class Main {
  public static void main(String[] args) {
    ArrayList<String>cars=new ArrayList<String>();
    // Create an ArrayList object,name is:cars.
    //<String> this is a wapper class.
    System.out.println(cars);//output:[]，nothing.
  }
}
```
### Add Item, keyword : add()
```
import java.util.ArrayList;

public class Main {
  public static void main(String[] args) {
    ArrayList<String>cars=new ArrayList<String>();
    cars.add("BMW");
    System.out.println(cars);
  }
}
```
### Access an Item,keyword : get()
```
import java.util.ArrayList;
public class Main {
  public static void main(String[] args) {
    ArrayList<String>cars=new ArrayList<String>();
	cars.add("Tesla");
    cars.add("BMW");
    cars.add("Saphilo");
    System.out.println(cars);
    System.out.println(cars.get(2));
  }
}
```
>Array indexes start with 0: [0] is the first element. [1] is the second element,etc.
### Change an Item,keyword : set()
```
import java.util.ArrayList;
public class Main {
  public static void main(String[] args) {
    ArrayList<String>cars=new ArrayList<String>();
    cars.add("Tesla");
    cars.add("BMW");
    cars.add("Saphilo");
    System.out.println(cars);
    cars.set(2,"Volov");
    System.out.println(cars);
  }
}
```
### Remove an Item,keyword : remove()、clear()
```
import java.util.ArrayList;
public class Main {
  public static void main(String[] args) {
    ArrayList<String>cars=new ArrayList<String>();
    cars.add("Tesla");
    cars.add("BMW");
    cars.add("Saphilo");
    cars.add("Volov");
    System.out.println(cars);
    cars.remove(0);            //remove by index number
    cars.remove("Volov");    //remove by specific String
    System.out.println(cars);
    cars.clear();    //remove all elements
    System.out.println(cars);
  }
}
```
### ArrayList size,keyword : size()
```
import java.util.ArrayList;
public class Main {
  public static void main(String[] args) {
    ArrayList<String>cars=new ArrayList<String>();
	cars.add("Tesla");
    cars.add("BMW");
    cars.add("Saphilo");
    cars.add("Volov");
    System.out.println(cars);
    System.out.println(cars.size());
  }
}
```
### Loop an ArrayList,keyword : for loop,size().
```
import java.util.ArrayList;
public class Main {
  public static void main(String[] args) {
    ArrayList<String>cars=new ArrayList<String>();
    cars.add("Tesla");
    cars.add("BMW");
    cars.add("Saphilo");
    cars.add("Volov");
    for(int i=0;i<cars.size();i++){
    	System.out.println(cars.get(i));
    }
  }
}
```
### Loop an ArrayList,keyword : for-each loop,size().
```
import java.util.ArrayList;
public class Main {
  public static void main(String[] args) {
    ArrayList<String>cars=new ArrayList<String>();
    cars.add("Tesla");
    cars.add("BMW");
    cars.add("Saphilo");
    cars.add("Volov");
    for(String i:cars){
    	System.out.println(i);
    }
  }
}
```
### Other type of ArrayList
>Integer、Boolean、Character、Double
```
import java.util.ArrayList;
public class Main {
  public static void main(String[] args) {
    ArrayList<Integer>cars=new ArrayList<Integer>();
    cars.add(50);
    cars.add(60);
    cars.add(70);
    for(Integer i:cars){
    	System.out.println(i);
    }
  }
}
```
### Sort ArrayList,keyword : sort(),lists alphabetically or numerically
>import java.util.Collections;
```
import java.util.ArrayList;
import java.util.Collections;
public class Main2{
    public static void main(String[] args){
        ArrayList<String> cars = new ArrayList<String>();
        cars.add("Porch");
        cars.add("Tesla");
        cars.add("BMW");
        cars.add("Saphilo");
        System.out.println(cars);
        System.out.println("After sorted.........");
        Collections.sort(cars);
        System.out.println(cars);
    }
}
```
The way it sort is depend on the data type in ArrayList.
### forEach():
ArrayList's **forEach()** method to print every item in the list
```
import java.util.ArrayList;
import java.util.Collections;

public class Main { 
  public static void main(String[] args) { 
    ArrayList<Integer> myNumbers = new ArrayList<Integer>();
    myNumbers.add(33);
    myNumbers.add(15);
    myNumbers.add(20);
    myNumbers.add(34);
    myNumbers.add(8);
    myNumbers.add(12);
    Collections.sort(myNumbers);
    myNumbers.forEach((n)->{System.out.println(n);});
  } 
}
```

# Java LinkedList
LinkedList 和 ArrayList很類似，因為LinkedList class 能執行和 ArrayList class因為它都實作了interface.
不同之處:
>如果需要頻繁地插入和刪除元素，則LinkedList可能更適合

>如果需要頻繁地按索引查找元素，則ArrayList可能更適合

ArrayList內部使用一個動態數組來存儲元素，當元素數量超過了動態數組的容量時，會自動擴展數組的大小。
LinkedList內部使用一個鏈表來存儲元素，每個節點包含了該元素的值以及指向下一個節點的指針。

插入和刪除操作：
在ArrayList中，插入和刪除操作涉及到元素的移動，需要保持連續的索引。
在LinkedList中，插入和刪除操作通常更快，只需要調整相鄰節點的指針。

查找操作：
在ArrayList中，通過索引查找元素是非常快速的，可以直接通過索引計算元素的位置。
在LinkedList中，由於是一個連續的鏈表，查找元素要從頭開始找，慢。

空間使用：
在ArrayList中，每個元素都需要一個固定大小的空間，並且可能會浪費一些空間，因為動態數組的大小可能會超過實際元素數量。
在LinkedList中，每個元素只需要存儲自己的值和指向下一個節點的指針，因此通常佔用的空間較少。

### 方法
* addFirst() : Adds an item to the beginning of the list.
* addLast() : Add an item to the end of the list	
* removeFirst() : Remove an item from the beginning of the list.	
* removeLast() : Remove an item from the end of the list	
* getFirst() : Get the item at the beginning of the list	
* getLast() : Get the item at the end of the list
```
import java.util.LinkedList;
public class Main {
  public static void main(String[] args) {
    LinkedList<Integer>cars=new LinkedList<Integer>();
    cars.addFirst(6870);
    cars.add(59);//add element
    cars.add(40);
    cars.addFirst(6990);//add eleent to the first
    cars.add(59);
    System.out.println(cars);
  }
}
```
```
import java.util.LinkedList;
public class Main {
  public static void main(String[] args) {
    LinkedList<Integer>cars=new LinkedList<Integer>();
    cars.addFirst(6870);
    cars.add(59);//add element
    cars.add(40);
    cars.addFirst(6990);//add eleent to the first
    cars.add(59);
    cars.removeLast();
    System.out.println(cars);
  }
}
```
```
import java.util.LinkedList;
public class Main {
  public static void main(String[] args) {
    LinkedList<Integer>cars=new LinkedList<Integer>();
    cars.addFirst(6870);
    cars.add(59);//add element
    cars.add(40);
    cars.addFirst(6990);//add eleent to the first
    int x=cars.getLast();
    System.out.println(cars);
    System.out.println(x);
    System.out.println(cars.getFirst());
  }
}
```
# Java HashMap
在ArrayList如果要存取items必須需要index number.
在HashMap,儲存items如:<key,value>配對，存取by index of another type.
在HashMap中，一個物件（通常是稱為鍵或索引）被用作另一個物件（通常是稱為值）的索引。
>當您想要根據特定的鍵查找對應的值時，您可以使用HashMap結構。HashMap允許您快速地根據鍵查找相應的值，而不需要經歷整個數據結構。

可以儲存(String keys和Integer vlaues)  or  都是相同類型(String keys and String values:)
### key part:
* import java.util.HashMap;
>import the HashMap class.

* HashMap<String,String>variablename=new HashMap<String,String>();
>create new HashMap item.
### Add item,keword:put()
```
import java.util.HashMap;
public class Main{
	public static void main(String[] args){
    	HashMap<String,String>product=new HashMap<String,String>();
        product.put("Taichung","chiliy sauce");
        //add key:value
        product.put("Taipei","Dihua street");
        product.put("Kaoshung","Ruro rice");
        System.out.println(product);
    }
}
```
### Access item,keyword:get()
```
import java.util.HashMap;
public class Main{
	public static void main(String[] args){
    	HashMap<String,String>product=new HashMap<String,String>();
        product.put("Taichung","chiliy sauce");
        //add key:value
        product.put("Taipei","Dihua street");
        product.put("Kaoshung","Ruro rice");
        System.out.println(product.get("Taichung"));
    }
}
```
### Remove item,keyword:remove(),clear()
```
import java.util.HashMap;
public class Main{
	public static void main(String[] args){
    	HashMap<String,String>product=new HashMap<String,String>();
        product.put("Taichung","chiliy sauce");
        //add key:value
        product.put("Taipei","Dihua street");
        product.put("Kaoshung","Ruro rice");
        product.remove("Kaoshung");
        System.out.println(product);
        product.clear();
        System.out.println(product);
    }
}
```
### HashMap Size,keyword:size()
```
import java.util.HashMap;
public class Main{
	public static void main(String[] args){
    	HashMap<String,String>product=new HashMap<String,String>();
        product.put("Taichung","chiliy sauce");
        //add key:value
        product.put("Taipei","Dihua street");
        product.put("Kaoshung","Ruro rice");
        System.out.println(product.size());
    }
}
```
### Loop through a HashMap,for-each loop
>Want keys:keySet()
>Want values:values()
```
import java.util.HashMap;
public class Main{
	public static void main(String[] args){
    	HashMap<String,String>product=new HashMap<String,String>();
        product.put("Taichung","chiliy sauce");
        //add key:value
        product.put("Taipei","Dihua street");
        product.put("Kaoshung","Ruro rice");
        for(String i:product.keySet()){
        	System.out.println(i);
        }//print all keys
        for(String i:product.values()){
        	System.out.println(i);
        }//print all values
        for(String i:product.keySet()){
        	System.out.println("key:"+i+" ,values:"+product.get(i));//print all keys and value
        }
    }
}
```
### Other types
主要改的部分:
>HashMap<String,*Integer*>product=new HashMap<String,*Integer*>();
```
import java.util.HashMap;
public class Main{
	public static void main(String[] args){
    	HashMap<String,Integer>product=new HashMap<String,Integer>();
        product.put("Apple",20);
        product.put("Banana",40);
        product.put("Cat",1500);
        for(String i:product.keySet()){
        	System.out.println("key:"+i+" ,price:"+product.get(i));
        }
    }
}
```
# Hashset
一堆獨特的item的集合，其中的元素排序是無序的，沒有特定的順序。
### keypoint:
```
1.import java.util.HashSet;
2.HashSet<String> cars=new HashSet<String>();
```
    
### Add item,keyword:add()
```
import java.util.HashSet;
public class Main{
	public static void main(String[] args){
    	HashSet<String>fruits=new HashSet<String>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");
        fruits.add("Tomato");
        fruits.add("Apple");//even add two times of apple,it only show one times
        fruits.add("apple");//different word,different meaning
        System.out.println(fruits);
    }
}
```
>Because every item in a set has to be unique.
### Check item in set or not,keyword:contains()
```
import java.util.HashSet;
public class Main{
	public static void main(String[] args){
    	HashSet<String>fruits=new HashSet<String>();
        fruits.add("Tomato");
        System.out.println(fruits.contains("Tomato"));
    }
}
```
### Remove single or clear all items:remove()、clear()
```
import java.util.HashSet;
public class Main{
	public static void main(String[] args){
    	HashSet<String>fruits=new HashSet<String>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");
        fruits.add("Tomato");
        System.out.println(fruits);
        System.out.println(fruits.contains("Tomato"));
        fruits.remove("Tomato");//remove tomato
        System.out.println(fruits);
        fruits.clear();//remove all items
        System.out.println(fruits);
        System.out.println(fruits.contains("Tomato"));//second try tomato
    }
}
```
### Size of set,keyword:size()
```
import java.util.HashSet;
public class Main{
	public static void main(String[] args){
    	HashSet<String>fruits=new HashSet<String>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");
        fruits.add("Tomato");
        System.out.println(fruits);
        System.out.println("Number of fruits: "+fruits.size());
    }
}
```
### Loop through a set:
```
import java.util.HashSet;
public class Main{
	public static void main(String[] args){
    	HashSet<String>fruits=new HashSet<String>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");
        fruits.add("Tomato");
        for(String i :fruits){
        	System.out.println(i);
        }
    }
}
```
### Loop through a set with another type:
```
import java.util.HashSet;
public class Main{
	public static void main(String[] args){
    	HashSet<Integer>fruits=new HashSet<Integer>();
        fruits.add(2);
        fruits.add(3);
        fruits.add(5);
        fruits.add(9);
        for(Integer i :fruits){
        	System.out.println(i);
        }
        //for loop also can be like this:
        //for(Integer i :fruits)
        for(int i=0;i<10;i++){
        	if(fruits.contains(i)){
            	System.out.println(i+" was found in set.");
            }else{
            	System.out.println(i+" was not found in set.");
            }
        }
    }
}
```
# Iterator
用來循環集合的物件，像是ArrayList和HashSet，迭代來自Loop
### Get an Iterator
```=java
import java.util.HashSet;
import java.util.Iterator;
import java.util.ArrayList;
// Import the ArrayList class、the Iterator class、the HashSet class
public class Main{
	public static void main(String[] args){
    	HashSet<Integer>numbers=new HashSet<Integer>();
        ArrayList<String>fruits=new ArrayList<String>();
        // Make a number collection
        numbers.add(4);
        numbers.add(3);
        numbers.add(5);
        numbers.add(9);
        // Make a fruit collection
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");
        
        // Get the iterator
        Iterator<String>fruitlist=fruits.iterator();
        Iterator<Integer>numberlist=numbers.iterator();
        
        System.out.println(numberlist.next()); // Print the first item
        System.out.println(fruitlist.next()); // Print the first item
    }
}
```
### Looping Through a Collection
```=java
import java.util.HashSet;
import java.util.Iterator;
import java.util.ArrayList;
// Import the ArrayList class、the Iterator class、the HashSet class
public class Main{
	public static void main(String[] args){
    	HashSet<Integer>numbers=new HashSet<Integer>();
        ArrayList<String>fruits=new ArrayList<String>();
        // Make a collection
        numbers.add(4);
        numbers.add(3);
        numbers.add(5);
        numbers.add(9);
        // Make a collection
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");
        Iterator<String>y=fruits.iterator();
        // Get the iterator
        Iterator<Integer>x=numbers.iterator();
        // Get the iterator
        while(x.hasNext()){
        	System.out.println(x.next()); // Print the first item
        }
        while(y.hasNext()){
        	System.out.println(y.next()); // Print the first item
        } 
    }
}
```
### Removing Items from a Collection
>keyword:remove()

>嘗試使用for 循環或 for-each 循環刪除項目將無法正常工作，因為在程式碼嘗試循環的同時集合正在更改大小
```=java
import java.util.HashSet;
import java.util.Iterator;
import java.util.ArrayList;
// Import the ArrayList class、the Iterator class、the HashSet class
public class Main{
	public static void main(String[] args){
    	HashSet<Integer>numbers=new HashSet<Integer>();
        ArrayList<String>fruits=new ArrayList<String>();
        // Make a collection
        numbers.add(22);
        numbers.add(33);
        numbers.add(55);
        numbers.add(44);
        // Make a collection
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");
        Iterator<String>y=fruits.iterator();
        // Get the iterator
        Iterator<Integer>x=numbers.iterator();
        // Get the iterator
        
        while(x.hasNext()){
        	Integer i=x.next();
        	if(i<30){
            	x.remove();
            }
            System.out.println(i); // Print the first item
        }
        
        while(y.hasNext()){
        	String m=y.next();
        	if(m.equals("Banana")){
            	y.remove();
            }else {
                System.out.println(m); // Print the item
            }
        }
    }
}
```
# Java Wapper Classes
Wrapper Class提供將primitive data type(原始資料型態)作為物件(object)
>A primitive data type specifies the size and type of variable values, and it has no additional methods.

原始資料型態:
byte、short、int、long、float、double、boolean、char
換成Wrapper Class:
Byte、Short、Integer、Long、Float、Double、Boolean、Character
### 必須使用wrapper classes:
>和物件的集合,ArrayList,原始資料型態不能使用，list只能儲存物件

```=java
Invalid:ArrayList<int>mynumber=new ArrayList<int>();

Valid:ArrayList<Integer>mynumber=new ArrayList<Integer>();
```

### 建立wrapper object
使用Wrapper class代替原始資料。
```=java
public class Main{
	public static void main(String[] args){
    	Integer myint=10;
        Double mydouble=12.063;
        Character mychar='B';
        System.out.println(myint);
        System.out.println(mydouble);
        System.out.println(mychar);
    }
}
```
### 用特定方法取得特定資訊
原始資料型態+Value(),example:intValue();
Example:intValue()、byteValue()、shortValue()、longValue()、floatValue()、doubleValue()、charValue()、booleanValue()
```=java
public class Main{
	public static void main(String[] args){
    	Integer myint=10;
        Double mydouble=12.063;
        Character mychar='B';
        System.out.println(myint.intValue());
        System.out.println(mydouble.doubleValue());
        System.out.println(mychar.charValue());
    }
}
```
### 特殊方法:toString()
將Wrapper class轉換成字串
```=java
public class Main{
	public static void main(String[] args){
    	Integer myint=10000;
        String myprice=myint.toString();
        System.out.println(myprice);
        System.out.println(myprice.length());
    }
}
```
# Exception...Try-Catch
### 語法:
```=java
try{
 //code to try
}
catch(Exception e){
 // code to handle errors
}
```
### Try-catch example
```=java
public class Main{
	public static void main(String[] args){
    	try{
            int[] mynumbers={1,2,3,4,5};
            System.out.println(mynumbers[6]);
        }catch(Exception e){
        	System.out.println("Nothing in here.");
        }
    }
}
```
### Keyword: finally
>finally在try-catch之後才執行，且一定會執行
```=java
public class Main{
	public static void main(String[] args){
    	try{
        	int[] mynumbers={1,2,3,4,5};
            System.out.println(mynumbers[6]);
        }catch(Exception e){
        	System.out.println("Nothing in here.");
        }finally{
        	System.out.println("Finally part executed.");
        }
    }
}
```
### keyword : throw
**throw** : 允許你建立常見的eroor
通常會搭配一種exception type一起使用
>EX:
>ArithmeticException,FileNotFoundException,
>ArrayIndexOutOfBoundsException,SecurityException
```=java
public class Main{
	static void checkage(int age){
    	if(age<20){
        	throw new ArithmeticException("Access Denied.");
        }else{
        	System.out.println("Access granted.");
        }
    }
	public static void main(String[] args){
    	checkage(15);
    }
}
```
# Java Regular Expressions(考試不會考)
一種字元序列的搜尋方法。可以是單一字元 或 複雜的組合
可以使用此搜尋方法在一串字串中搜尋你想要的資料。
### keyword:
>import java.util.regex

### keyword後面再加class:
1. **Pattern** class : 定義pattern,用來做search
1. **Match** class : 用pattern來搜尋
1. **PatternSyntaxEcxeption** class : 指出在regular expression pattern的語法錯誤
### Example:
```java=
import java.util.regex.Matcher;
import java.util.regex.Pattern;
public class Main{
	public static void main(String[] args){
    	Pattern pattern = Pattern.compile("oo",Pattern.CASE_INSENSITIVE);
        Matcher matcher = pattern.matcher("Yahoo ha-re.");
        boolean resultFound=matcher.find();
        if(resultFound){
        	System.out.println("Match");
        }else{
        	System.out.println("Not match");
        }
    }
}
```
解釋:
1.用Pattern.compile()來建立pattern.第一個參數指示正在搜尋哪個模式，第二個參數有一個Flag來指示搜尋應不區分大小寫。第二個參數是可選的。

2.matcher()方法用於搜尋字串中的模式。它會傳回一個 Matcher 對象，其中包含有關所執行的搜尋的資訊。

3.find()如果在字串中找到該模式，則該方法傳回 true；如果未找到，則傳回 false。
### Regular Expression Patterns:Pattern.compile()的第個參數
表示方式:[abc] 在字串中找abc
表示方式:[^abc] 在字串外面找abc
表示方式:[0-9] 在0~9的範圍中找某個字元
### Flags:Pattern.compile()的第二個參數
>Pattern.CASE_INSENSITIVE- 執行搜尋時將忽略字母的大小寫。

>Pattern.LITERAL- 模式中的特殊字元不會有任何特殊意義，在執行搜尋時將被視為普通字元。

>Pattern.UNICODE_CASE- 將其與CASE_INSENSITIVE標誌一起使用也可以忽略英文字母表之外的字母的大小寫

# Threads
Thread 允許程式藉由在同一時間執行多件事情來達到更有效率
Thread 用來在後台表現複雜的問題而不打擾主程式區
>*線程安全問題 : ArrayList、LinkList、HashMap、HashSet 皆不安全
什麼意思? Thread允許同時進行，上述4個存取時可能都要存資料到最後一個，兩方同時進行導致存取到錯誤的資料
### 建立 Thread、運行Thread : **start()**
* 方法1，extend
* 它可以透過擴展Thread類別並重寫其run() 方法來創建
* If the class extends the Thread class, the thread can be run by creating an instance of the class and call its **start()** method
```java=
public class Main extends Thread{
	public static void main(String[] args){
    	Main thread = new Main();
        thread.start();//會執行下面的run()
        System.out.println("This code is outside of the thread"); 
    }
    //會先執行主程式還是分支的程式，不一定
    public void run(){
    	System.out.println("This code is running in  thread");
    }
}
```
* 方法2，implement，Runnable是interface
* 創建線程的另一種方法是實作該Runnable介面
* If the class implements the Runnable interface, the thread can be run by passing an instance of the class to a Thread object's constructor and then calling the thread's **start()** method
```java=
public class Main implements Runnable{
	public static void main(String[] args){
    	Main object = new Main();
        Thread abc = new Thread(object);
        abc.start();
        System.out.println("This code is outside of the thread"); 
    }
    public void run(){
    	System.out.println("This code is running in  thread");
    }
}
```
### “extending”和“implementing”Threads之間的差異

主要區別在於，當一個類別擴展 Thread 類別時，您不能擴展任何其他類，但透過實作 Runnable 接口，也可以從另一個類別擴展，例如： class MyClass extends OtherClass implements Runnable。
### Concurrency Problems : 線程安全
由於執行緒與程式的其他部分同時運行，因此無法知道程式碼將按什麼順序運行。
當執行緒和主程式讀寫相同的變數時，這些值是不可預測的。由此產生的問題稱為並發問題。
**最好不要分享attribute between threads as possible.**
isAlive() 使用執行緒可以更改的任何屬性之前，使用執行緒的方法檢查執行緒是否已完成運行。
### Example Code:
```java=
public class Main extends Thread {
  public static int amount = 0;

  public static void main(String[] args) {
    Main thread = new Main();
    thread.start();
    // Wait for the thread to finish
    while(thread.isAlive()) {
      System.out.println("Waiting...");
    }
    // Update amount and print its value
    System.out.println("Main: " + amount);
    amount++;
    System.out.println("Main: " + amount);
  }
  public void run() {
    amount++;
  }
}
```
```java=
public class Main extends Thread {
  public static int amount = 0;

  public static void main(String[] args) {
    Main thread = new Main();
    thread.start();
    // Wait for the thread to finish
    while(thread.isAlive()) {
      System.out.println("Waiting...");
    }
    // Update amount and print its value
    System.out.println("Main: " + amount);
    amount++;
    System.out.println("Main: " + amount);
  }
  public void run() {
    amount++;
  }
}
```

# Lambda
接受某個參數然後return value
類似method，但沒有名稱，執行很快速
### 語法
```java=
parameter -> expression
or
(parameter1,parameter2)-> expression
or
(parameter1,parameter2)-> {code block}
```
### 使用Lambda Expressions
方法1. ArrayList : forEach() method to print every item in the list
```java=
import java.util.ArrayList;
public class Main{
	public static void main(String[] args){
    	ArrayList<Integer>numbers=new ArrayList<Integer>();
        numbers.add(5);
        numbers.add(3);
        numbers.add(6);
        numbers.add(9);
        numbers.forEach((n)->{System.out.println(n);});
    }
}
```
方法2.Consumer interface
Use **Java's Consumer interface** to store a lambda expression in a variable
lambda 表達式應具有與該方法相同數量的參數和相同的傳回類型。
**Keyword:import java.util.function.Consumer;**
```java=
import java.util.ArrayList;
import java.util.function.Consumer;
public class Main{
	public static void main(String[] args){
    	ArrayList<Integer>numbers=new ArrayList<Integer>();
        numbers.add(5);
        numbers.add(3);
        numbers.add(6);
        numbers.add(9);
        Consumer<Integer>method=(n)->{System.out.println(n);};
        numbers.forEach(method);
    }
}
```
```java=
import java.util.ArrayList;
import java.util.Collections;
import java.util.function.Consumer;

public class Main { 
  public static void main(String[] args) { 
    ArrayList<Integer> myNumbers = new ArrayList<Integer>();
    myNumbers.add(33);
    myNumbers.add(15);
    myNumbers.add(20);
    myNumbers.add(34);
    myNumbers.add(8);
    myNumbers.add(12);
    Collections.sort(myNumbers);
    Consumer<Integer>func=(n)->{System.out.println(n);};
    myNumbers.forEach(func);
  } 
}
```

方法3.要在方法中使用 lambda 表達式，該方法應具有以單一方法介面作為其類型的參數。呼叫介面的方法將運行 lambda 表達式
```java=
interface StringFunction {
  String run(String str);
}

public class Main {
  public static void main(String[] args) {
    StringFunction shock = (s) -> s + "!";
    StringFunction ask = (s) -> s + "?";
    printFormatted("Hello", shock);
    printFormatted("Hello", ask);
  }
  public static void printFormatted(String str, StringFunction format) {
    String result = format.run(str);
    System.out.println(result);
  }
}
```
# Java Files
File這個class來自java.io package.
要使用File class須用class建立物件，並給予檔名
### Example:
```java=
import java.io.File;
File myobj=new File("filename.txt");
```
### 其他的methods()
* canRead() Boolean : Tests whether the file is readable or not
* canWrite() Boolean:Tests whether the file is writable or not
* CreateNewFile() Boolean: Creates an empty file
* delete() Boolean:Deletes a file
* exists() Boolean:Tests whether the file exists
* getName() Boolean:Returns the name of the file
* getAbsolutePath() String:Returns the absolute pathname of the file
* length() Long:Returns the size of the file in bytes
* list() String[]:Returns an array of the files in the directory
* mkdir() Boolean:Creates a directory
# Java Create and Write To Files
### Create a File
```java=
import java.io.File;
import java.io.IOException;
public class CreateFile{
    public static void main(String[] args){
        try{
            File myobj=new File("filename.txt");
            //filename.txt前面可以再加上檔案的路徑
            if(myobj.createNewFile()){
                System.out.println("File Name:"+myobj.getName());
            }else{
                System.out.println("File existed");
            }
        }catch(IOException e){
            System.out.println("Error");
            e.printStackTrace();
        }
    }
}
```
### Write to File
```java=
import java.io.File;
import java.io.IOException;

public class WriteFile{
    public static void main(String[] args){
        try{
            FileWriter myobj=new FileWriter("filename.txt");
            //filename.txt前面可以再加上檔案的路徑
            myobj.write("Part in file");
            myobj.close();
            System.out.println("Wrote successful.");
        }catch(IOException e){
            System.out.println("Error");
            e.printStackTrace();
        }
    }
}
```
# Java Read Files
```java=
import java.io.File;
import java.io.FileNotFoundException;
//import this class to handle errors
import java.util.Scanner;

public class ReadFile{
    public static void main(String[] args){
        try{
            File myobj=new File("filename.txt");
            Scanner myReader =new Scanner(myobj);
            while(myReader.hasNextLine()){
                String data = myReader.nextLine();
                System.out.println(data);
            }
            myReader.close();
        }catch(FileNotFoundException e){
            System.out.println("Error");
            e.printStackTrace();
        }
    }
}
```
### Get File information
```
import java.util.File;
public class GetFileInfo{
    public static void main(String[] args){
        File myobj = new File("filename.txt");
        if(myobj.exists()){
            System.out.println("Filename:"+myobj.getName());
            System.out.println("Path:"+myobj.getAbsolutePath());
            System.out.println("Can Write:"+myobj.canWrite());
            System.out.println("Can Read:"+myobj.canRead());
            System.out.println("File size in byte:"+myobj.length());
        }else{
            System.out.println("File not exist.");
        }
    }
}
```
# Java Delete files
>keywords :  delete()

```
import java.io.File;
public class DeleteFile{
    public static void main(String[] args){
        File myobj = new File("filename.txt");
        //File()中加入絕對路徑=刪除Folder
        if(myobj.delete()){
            System.out.println("Delete File: "+myobj.getName());
        }else{
            System.out.println("Fialed to delete.");
        }
    }
}
```


# HashMap,ArrayList,HashSet 整理



| | ArrayList | HashMap | HashSet |
| -------- | -------- | -------- | -------- |
| add item     | add()     | put()     | add()|
| get item     | get()     | get()     | |
| set item     | set()     |    | |
| remove item     | remove()     | remove()     |remove()|
| all remove item     | clear()     | clear()     |clear() |
| item size     | size()     | size()     |size() |


* HashSet To check whether an item exists in a HashSet, use the contains() method:

```=java
// Import the HashSet class
import java.util.HashSet;

public class Main {
  public static void main(String[] args) {
    HashSet<String> cars = new HashSet<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("BMW");
    cars.add("Mazda");
    System.out.println(cars.contains("Mazda")); // true
  }
}

```
## data structure

![LINE_ALBUM_2024.4.17_240423_1](https://hackmd.io/_uploads/BkXd164bR.jpg)


# some information
![image](https://hackmd.io/_uploads/HJhAnNrZA.png)


# 各種歷遍方式

## Enum values()
```java=
for (Level myVar : Level.values()) {
  System.out.println(myVar);
}
```

## ArrayList(陣列歷遍)

```java=
public class Main {
  public static void main(String[] args) {
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    for (String i : cars) {
      System.out.println(i);
    }
  }
}
```

## HashMap keySet()

```java=
import java.util.HashMap;

public class Main {
  public static void main(String[] args) {
    HashMap<String, String> capitalCities = new HashMap<String, String>();
    capitalCities.put("England", "London");
    capitalCities.put("Germany", "Berlin");
    capitalCities.put("Norway", "Oslo");
    capitalCities.put("USA", "Washington DC");
    
    for (String i : capitalCities.keySet()) {
      System.out.println(i);
    }
  }
}

```

## HashSet(陣列歷遍)
```java=
// Import the HashSet class
import java.util.HashSet;

public class Main {
  public static void main(String[] args) {
    HashSet<String> cars = new HashSet<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("BMW");
    cars.add("Mazda");
    for (String i : cars) {
      System.out.println(i);
    }
  }
}

```

