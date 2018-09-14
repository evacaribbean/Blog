# Blog


> Light articles and thoughts on Java and frontend, with the latest post closest to below. 

<br>
<br>

- ...
- [Color and Size in Geometrics](https://github.com/evacaribbean/Blog#color-and-size-in-geometrics) 
- [The Java Adventure](https://github.com/evacaribbean/Blog#the-java-adventure)
- [ipsum aquia vitae](https://github.com/evacaribbean/Blog#ipsum-aquia-vitae)

<br>
<br>
<br>


## Color and Size in Geometrics
 
This geometrics program is coded in one source file. Without zillions of classes though with many enought, it could have been good to divide them into a few more source files. But here I wanted to focus on constructors, public and not public classes, inheritance (extends) and overloading.

I make up a task, saying:

<em>"Create a console program that changes the colors and sizes of its geometrical figures. Depending on each shape's area or volume."</em>      

<br>

![geometrics overview](/images/geometricsoverview.jpg)

<br>

The solution above consists of six classes. Where the *main method entry point* is unfolded.

I find it nice to have as little as possible written in the entry point. So I often start here, and work may way back into the classes and its members. In this way the overview automatically has to present itself first. And with this, the design which will give the answers on how to code also naturally makes it easy on how to continue. From overwiew to "details".

To try the console program out, just change the values in the instantiated objects.  

<br>

![geometrics instantiated](/images/geometricsinstantiated.jpg)

<br>
<br>

### entry point

Starting with the overview, I've found it good to always begin coding and "set up" by the main method entry point. With this approach the code design easily forms and answers my questions on how the program should be written. 

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

### inheritance (extends)

text...

<br>

### constructors

text...

<br>

### java access specifiers

text...

<br>

![geometrics console](/images/geometricsconsole.jpg)

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


## ipsum aquia vitae

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae consequatur, vel illum qui dolorem eum fugiat quo voluptas nulla pariatur?

<br> 

![Koivo](/images/koivowatercolor.jpg)

<br>

( I just test now how font and images will look, I will come back later on. Maybe it'll take a while, but I'll be back 😊 ) 