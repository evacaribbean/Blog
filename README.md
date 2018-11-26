# Blog


> Light articles and thoughts on Java and frontend, with the latest post closest to below. 

<br>
<br>

- ...
- ...
- ...
- [Agility, Design and My First Full Stack Project](https://github.com/evacaribbean/Blog#agility-design-and-my-first-full-stack-project)

<br>

*a first swim in the ocean - no structure yet, just diving in having fun and exploring the basics just as it comes*

<br>

- [A Do Re Mi Fa Sol La App](https://github.com/evacaribbean/Blog#a-do-re-mi-fa-sol-la-app)
- [A Module App Word Caser with Swing](https://github.com/evacaribbean/Blog#a-module-app-word-caser-with-swing)
- [CRUD 2](https://github.com/evacaribbean/Blog#)
- [CRUD 1](https://github.com/evacaribbean/Blog#)
- [Different Database Connections](https://github.com/evacaribbean/Blog#different-database-connections)
- [A Database Connected](https://github.com/evacaribbean/Blog#a-database-connected)

<br>

- [Input Directly Through the Console](https://github.com/evacaribbean/Blog#input-directly-though-the-console) 
- [Input Output](https://github.com/evacaribbean/Blog#input-output)
- [Color and Size in Geometrics](https://github.com/evacaribbean/Blog#color-and-size-in-geometrics) 
- [The Java Adventure](https://github.com/evacaribbean/Blog#the-java-adventure)
- [ipsum aquia vitae](https://github.com/evacaribbean/Blog#ipsum-aquia-vitae)

<br>
<br>
<br>
<br> 
 
## Agility, Design and My First Full Stack Project 

...

<br>

<!-- ![the index image](/images/blogindex.png) -->

<br>
<br>
<br>
<br>
<br>
<br>
<br>
 
## A Do Re Mi Fa Sol La App 

...

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## A Module App Word Caser with Swing   

Well, why not?

A word playing title… But then again, just words. Why not? The small “WordCaser” app’s only purpose is to switch letters from lower case to upper case, and vice versa. 
 
<br>

![the word-caser app](/images/wordcaser.jpg)

<br>

At last 🐬 🐋, it’s time 🐠 for apps! 🐳 This is a [NetBeans](https://netbeans.org) Platform Application. As time goes by I also go through [IntelliJ](https://www.jetbrains.com) and [Eclipse](https://www.eclipse.org). It’s swell to administering and code in all, and kind of know that the IDEs feel equal familiar and seamless to work in. So far I’ve found it to be a choice, only depending on purpose and taste.      

The application’s single coding part that has to be added is the two event handlers, “upButton” and “lowButton”.
    

<br>

``` javascript
    private void upButtonActionPerformed(java.awt.event.ActionEvent evt) {                                         
        String letters = textArea.getText();
        letters = letters.toUpperCase();
        textArea.setText(letters);

    }                                        

    private void lowButtonActionPerformed(java.awt.event.ActionEvent evt) {                                          
        String letters;
        letters = textArea.getText();
        letters = letters.toLowerCase();
        textArea.setText(letters);

    }
```

<br>

...

<br>
<br>
<br>
<br> 
<br>
<br>
<br>
<br>

## CRUD 2 

...

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## CRUD 1

...

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Different Database Connections 

In the [previous](https://github.com/evacaribbean/Blog#a-database-connected) blog post a Java DB (Derby) *Network* JDBC driver was used to connect to an Apache's Derby database. Below the *Embedded* Derby JDBC driver will be used to connect to the same database as in the previous blog post. And the second connection will show how to connect to a MySQL database, using a network JDBC driver.

The JDBC API (Java Database Connectiviy, Application Programming Interface) is a Java API that was designed to make the everyday db-administation easy. Three common programming tasks that JDBC API gives great support in are: 1) to connect to a database 2) to update, send, and retrieve data 3) to ask queries and analyse data. 

Especially data that's stored in a relational db.

<br>

Good notes - Since JDBC 4.0 (which is included in Java SE 6 and forward) there's no need to register the driver, as JDBC driver manager detects and loads the driver [automatically](https://docs.oracle.com/javase/8/docs/api/java/sql/package-summary.html).   

<br>
<br>

...  <!-- Connection with an embedded Derby JDBC driver -->

<br>
``` javascript 
        ...
        Connection conn = null;         
        //String driver = "org.apache.derby.jdbc.EmbeddedDriver";  
        String url = "jdbc:derby:aData"; 
     
        try {
            //Class.forName(driver); //.newInstance();  
            conn = DriverManager.getConnection(url);
            System.out.println("Wazzaiiupppp! Jaour'On !");
        } catch (Exception e) {
            e.printStackTrace();
        }
        ... 
```



<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## A Database Connected  

I eagerly wanted to come to the point where I could start to explore the sea more than focus on how to swim. So many questions, and each in its turn had its own life and worlds of wonder. So fun, interesting and in good ways challenging.

One morning, though not swimming like the seals but friends now, I saw a glimpse! Of beacons, islands, waves, its ocean floor, and sky with wind. 

Now it was time. In the evening I swam up to the surface for air again and to see, had I really understood? These glimpses, could it be? That at night, also the sky wore light? …and…they were there! The stars!

<br>
<br>

### JDBC

More clearly I saw and could now answer myself, on how to connect java applications to databases. And further. When you know, it’s simple easy. And well, when not knowing of course it’s the reverse.

Even in a computer’s world every language needs to be interpreted if different machines and systems should be able to understand each other. One could switch of course, talking the language that applies for the moment. But is it realistic?

So instead, databases communicate in their own way and programming languages in theirs. And the interpreter translates between the two. The interpreter’s name is “Java Database Connectivity”. It’s an application programming interface. And to make the two connect, it uses its JDBC drivers. 

<br>
<br>

### the code

First. Tree packages will be imported. 

Well, when coding within an IDE the platform will give the suggestions needed. By the `Connection` and `DriverManager` parts for example, a tool window will show libraries with supportive coding alternatives. 

<br>   

``` javascript
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;  
...  
```
<br>
<br>

Next. Without a main method, no program (in nearly all cases). This program's  main method resides in one file. `JavaToDatabaseConnect.java`. The first statement will be a println-message (it's always nice to check that the code compiles properly). 

<br> 

``` javascript
public class JavaToDatabaseConnect {

    public static void main(String[] args) {
    
        System.out.println("A network Derby driver example. The program compiles.");          
        ...    	
    }
}  
```

<br>
<br>

...and then the four statements that handle the connection variables and their assigned values.  

<br>  

``` javascript 
        ...      
        Connection connection = null; 
        String url = "jdbc:derby://localhost:1527/Ocean";    
        String user = "a-user";
        String password = "a-password";  
        ...   	 
```
<br>
<br>

It's time! 

Now the connection variables can be invoked (called upon). And a println-message sent, when the program runs.

Here the getConnection method gets the `url`, `user` and `password`, assisted by its DriverManager class. And the variable `connection` is assigned.

(in older Java versions it would have been necessary to also register the driver, by using `Class.forName()` or `DriverManager.registerDriver()`). 

<br>

``` javascript 
        ...
        try { 
            connection = DriverManager.getConnection(url, user, password);
            System.out.println("Wazzaiiupppp! Jaour'On !"); 
        ...                
```

<br>
<br>

Finally. When calling risky methods they have to be surrounded with try-catch blocks (the IDE will give suggestions on try-catch blocks and also throws clauses). As the Java code can be allright, even without an ok connection.

<br>

``` javascript 
        ...
        try { 
            conn = DriverManager.getConnection(url, user, password);
            System.out.println("Wazzaiiupppp! Jaour'On !");
        } catch(Exception e) {
            e.printStackTrace();
        }

        try {
            connection.close();
            System.out.println("The connection is closed.");
        } catch (SQLException eq) {
            System.err.println(eq);
        } 
        ...
```

<br>
<br>
 
Below the whole 🐬 🐋 Java file. 

Before running the program a few steps has to be taken in the IDE. In turn, create a New Project &nbsp;&nbsp;> &nbsp;&nbsp;(skip creating a main class, as the method already exists in the java file) &nbsp;&nbsp;> &nbsp;&nbsp;Name the project: `JavaToDatabaseConnect.java`. 

The new project opens in the IDE. ⇒

Create a new package (or subfolder, depending on IDE) within the `Source Packages` (or `src` folder), named `Connection` &nbsp;&nbsp;> &nbsp;&nbsp;right-click `Libraries` &nbsp;&nbsp;> &nbsp;&nbsp;`Add JAR/Folder...` &nbsp;&nbsp;> &nbsp;&nbsp;to import `derby.jar` (it resides default in the current JDK, that the IDE also uses). 

In IntelliJ the `derby.jar` is imported by choosing: &nbsp;&nbsp;File Menu | `Project Structure...` &nbsp;&nbsp;> &nbsp;&nbsp;`Modules` &nbsp;&nbsp;> &nbsp;&nbsp;`Dependencies` &nbsp;&nbsp;> &nbsp;&nbsp;`+` &nbsp;&nbsp;> &nbsp;&nbsp;`JARs or Directories...` &nbsp;&nbsp;> &nbsp;&nbsp;`derby.jar`.


<br>

And that's it. 🐠 The [next](https://github.com/evacaribbean/Blog#different-database-connections) blog post 🐳 will walk through on how to connect to a MySQL db and on how to use an embedded driver.

<br>

``` javascript 
package Connections;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

 
public class JavaToDatabaseConnect {
    
    public static void main(String[] args) {
        System.out.println("A network Derby example. The program compiles.");
        
        Connection connection = null; 
        String url = "jdbc:derby://localhost:1527/Ocean";        
        String user = "a-user";
        String password = "a-password"; 

        try {   
            connection = DriverManager.getConnection(url, user, password);
            System.out.println("Wazzaiiupppp! Jaour'On !");
        } catch(Exception e) {
            e.printStackTrace();
        }

        try {
            connection.close();
            System.out.println("The connection is closed.");
        } catch (SQLException eq) {
            System.err.println(eq);
        }
    }      
}
```

<br>

![a database connection message](/images/connectionmessage-network.jpg)

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Input Directly Through the Console  

...

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Input Output  

...

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Color and Size in Geometrics
 
This geometrics program is coded in one source file. Without zillions of classes though with many enought, it could have been good to divide them into a few more source files. But here I wanted to focus on constructors, public and not public classes, inheritance and overloading.

I create a task, saying:

<em>"Build a console program that changes the colors and sizes of its geometrical figures. Depending on each shape's area or volume."</em>      

<br>

![a geometrics console overview](/images/geometricsoverview.jpg)

<br>

The solution above consists of six classes. Where the main method entry point is unfolded.

I find it nice to have as little as possible written in the entry point. So I often start here, and work may way back into the classes and its members. In this way the overview will present itself first. And the code design naturally finding its way from overwiew to "details".


To try the console program out, just change the values in the instantiated objects.  

<br>

![the geometrics instantiated objects](/images/geometricsinstantiated.jpg)

<br>

([next article](https://github.com/evacaribbean/Blog#input-directly-through-the-console) describes a console program where the user instead has the possibility to alter the values directly by console input)

<br>
<br>

### entry point

Starting with the overview, coding and "set up" the main method entry point. The code design easily forms and answers my questions on how the program should be written.

<br>

- Should the class have printlns?
- Should there be any direct values in the class?
- Should the class present just one method and constructor, or many?
- Should I use as few members as possible in the class?
- Should the program have few or many classes?
<br>

``` javascript
public class G {
	public static void main(String[] args) {
		
		Circle cir = new Circle(1, 21);	 
		Cube cub = new Cube(5, 18, 64);		 		
		Square squ = new Square(12, 4);		 	
		Triangle tri = new Triangle(2, 1);	 

		cir.info();		
	 	cir.cirColorInfo(); cub.cubColorInfo(); 
	 	squ.squColorInfo(); tri.triColorInfo(); 		
	}
} 
``` 
 
<br>
<br>

### inheritance (extends)  

The only thing in this program that `extends` from the superclass "Geometry", are the variables. To be used in each geometry subclass to avoid variable duplicates.

"Geometry" also has two void methods (without being used as "extensions"). The "main class" calls (invokes) the info() method. The other one doesn't do anything.

Plain and simple.

<br>

``` javascript
class Circle extends Geometry { … }
``` 

By calling the geometry class from for example the circle class. Asking to extend from geometry. Circle inherits all available varaibles and methods from geometry. In this context, geometry is a superclass and circle a subclass. Sometimes also refered to as parent and child classes. 

<br> 

#### an overall perspective

Viewing inheritance in its context of *interface*, *superclass*, *subclass*, *abstract class*, *overload* and *override* from a more overall perspective, the concept will be quite straightforward. Below a picture on this concept. 

<br>

![a logical overall perspective picture](/images/overallperspective.jpg)

<br>

First. Any class can `implements` from an interface. But a subclass can also `extends` (inherit) from an abstract class or a superclass.

<br>

Looking at the picture’s subclass "**Bird**". It can inherit from the two abstract classes and the superclass. And if it wish to use the interface it does so by implementing it.

To narrow it down a bit. If the program is well written, there will be no logical reason why Bird should use the abstract class "Plants". And likewise, both the superclass and the abstract class will not repeat the members that already exist in the interface “Unspecific”. Instread, the interface will be implemented.

Checking the subclass "**Forest**" instead. It will in the same manner inherit from its abstract class "Plants" and its superclass "Biology". And finally. The interface's members should preferably be so common, that they can be used in every class. In this way these members don't have to be repeated in any other class in the program.  

<br>

#### the bryophyte, the human and the berry

Let's test the similarities between a bryophyte a human and a berry. Accordingly to the picture's interface.

They are all included in the superclass "**Biology**", as they are living creatures. And everyone will also inherit from the abstract class "**Plants**" or "**Animals**". Along with that they all have a depth, height, name, type, volume, weight, width and year (the interface) together. 

So **Berry** can use all the interface's members just as a human, or a bryophyte. The superclass here `implements` the interface "**Unspecific**". Next, after Berry has `extends` from the superclass "Biology", it'll `extends` from its abstract class "Plants". And finally, as it has some specific features (variables or methods) that its cousins "Tree" or "Flower" don't have. Berry will add these in its own class.

The same goes for Human and Bryophyte. And also for for example a ladybug, a forest or a bacteria. 

<br>

#### override and overload

This concept is basically also rather straightforward. If for example **Ladybug** desides to `extends` a methods from its abstract class **Animals**, then this is called *override*. But if **Ladybug** then changes something in that method's argument list after it is extended, it is called *overload*.

Override a method or a constructor, is what a class does when it **inherits**. While overloading doesn't have anything with inheritance to do. It is simply just what is done when a method or a constructor from another class is reused, and something thereafter is changed in this method's or constructor's **argument list**.      

<br>
<br>

### constructors

constructor: default, no argument, access modifiers, overloaded, parameterized 

<br>
<br>

### java access specifiers

text...

<br> 

![the geometrics console output](/images/geometricsconsole.jpg)

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## The Java Adventure

Real real gone - such great time! I first thought: "No matter what, uphill both ways, snow and snow again, dog slow ... on and on and on, my my...". 

But nop! It is with such delight I´ve been reading books, enjoy Internet videos, teaching myself, and participate in Java courses. It is great! The subject seemed to be so fun. So interesting! Diving down, not sure if it'll be what I hoped for (even if it looked exciting). It soon turned out to be, just great time - Yeess! I was lucky. 

Then I knew, this is it. This is the subject. 

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## ipsum aquia vitae

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae consequatur, vel illum qui dolorem eum fugiat quo voluptas nulla pariatur?

<br> 

![Koivo](/images/koivowatercolor.jpg)

<br>

( I just test now how font and images will look, I will come back later on. Maybe it'll take a while, but I'll be back 😊 ) 