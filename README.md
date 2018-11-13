# Blog


> Light articles and thoughts on Java and frontend, with the latest post closest to below. 

<br>
<br>

- ...
- ...
- ...
- ...

<br>

*my first swim in the ocean*

<br>

- [A Do Re Mi Fa Sol La App](https://github.com/evacaribbean/Blog#a-do-re-mi-fa-sol-la-app)
- [A Module App Word Caser with Swing](https://github.com/evacaribbean/Blog#a-module-app-word-caser-with-swing)
- [CRUD 2](https://github.com/evacaribbean/Blog#)
- [CRUD 1](https://github.com/evacaribbean/Blog#)
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
 
## A Do Re Mi Fa Sol La App 

...

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

At last 🐬 🐋, it’s time 🐠 for apps! 🐳 This is a [NetBeans](https://netbeans.org) Platform Application. As time goes by I also go through [IntelliJ](https://www.jetbrains.com) and [Eclipse](https://www.eclipse.org). It’s swell to administering and code in all, and know that the IDEs feel equal familiar and seamless to work in. So far I’ve found it to be a choice, only depending on purpose and taste.      

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


## CRUD 2 

...

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

## A Database Connected  

...

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


## Input Output  

...

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


## The Java Adventure

Real real gone - such great time! I first thought: "No matter what, uphill both ways, snow and snow again, dog slow ... on and on and on, my my...". 

But nop! It is with such delight I´ve been reading books, enjoy Internet videos, teaching myself, and participate in Java courses. It is great! The subject seemed to be so fun. So interesting! Diving down, not sure if it'll be what I hoped for (even if it looked exciting). It soon turned out to be, just great time - Yeess! I was lucky. 

Then I knew, this is it. This is the subject. 

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