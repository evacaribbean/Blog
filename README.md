# Blog


> Light articles and thoughts on Java and frontend, with the latest post closest to below. 

<br>
<br>

- ...
- [Input Output](https://github.com/evacaribbean/Blog#input-output)
- [Color and Size in Geometrics](https://github.com/evacaribbean/Blog#color-and-size-in-geometrics) 
- [The Java Adventure](https://github.com/evacaribbean/Blog#the-java-adventure)
- [ipsum aquia vitae](https://github.com/evacaribbean/Blog#ipsum-aquia-vitae)

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

![geometrics overview](/images/geometricsoverview.jpg)

<br>

The solution above consists of six classes. Where the main method entry point is unfolded.

I find it nice to have as little as possible written in the entry point. So I often start here, and work may way back into the classes and its members. In this way the overview will present itself first. And the code design naturally finding its way from overwiew to "details".


To try the console program out, just change the values in the instantiated objects.  

<br>

![geometrics instantiated](/images/geometricsinstantiated.jpg)

<br>

(the [next article](https://github.com/evacaribbean/Blog#input-output) describes a console program where the user instead has the possibility to alter the values directly by console input)

<br>
<br>

### entry point

Starting with the overview, coding and "set up" the main method entry point. Now the code design easily forms and answers my questions on how the program should be written.

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

The only thing in this program that extends from the superclass "Geometry", are the variables. To be used in each and everyone’s geometry subclass to avoid variable duplicates.

"Geometry" also has two void methods (without being used as "extensions"). The "main class" calls (invokes) the info() method. The other one doesn't do anything.

Plain and simple.

<br>

``` javascript
class Circle extends Geometry { … }
``` 

By calling the geometry class from the circle class. Asking to extend from geometry. Circle inherits all available varaibles and methods from geometry. In this contect geometry is a superclass and circle a subclass. Sometimes also refered to as parent and child classes. 

<br>

Looking at inheritance in its context of *interface*, *superclass*, *subclass*, *abstract class*, *overload* and *override* from a more overall perspective, the concept will be quite straightforward. Below a picture on this concept. 

<br>

![a logical perspective](/images/overallperspective.jpg)

<br>

...

<br>
<br>

### constructors

text...

<br>
<br>

### java access specifiers

text...

<br> 

![geometrics console](/images/geometricsconsole.jpg)

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