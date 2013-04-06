vim: sts=4:sw=4:ts=4:ft=markdown

## lesson1: Turtling.

With NetLogo open and the `Interface` tab selected, try out the following in the `Command Center`:

This is how you make a turtle:

    create-turtles 1

We are going to ask our turtles to draw underneath them as they move.

    ask turtles [ pendown ]
    
Now let's ask the turtle to move forward `5 steps` and then turn right `60` degrees. I hope you guys remember your shapes. It's especially useful if you remember how big the angles of the shape are.

    ask turtles [ forward 5 ]
    ask turtles [ right 60 ]

You should have the following:

![step1.png](images/step1.png)

We can combine the 2 instructions to one line as follows.

    ask turtles [ forward 5 right 60 ]

Alright, why don't we tell this turtle to repeat the last instruction 3 more times?

    ask turtles [repeat 3 [forward 5 right 60 ] ]

Why don't we look at what we have so far? 

![step2.png](images/step2.png)

It looks like we almost have a shape. What shape does this look like?  Why don't we complete the shape? What instructions do we need to give to complete the shape?

**Note**: if you make a mistake by giving the wrong instruction to the turtle, you can reset and start again by running:

    clear-all
    
We can even keep telling the turtles to repeat what they're repeating. Something like:

    clear-all
    create-turtles 1 
    ask turtles [ pendown ]
    ask turtles [ repeat 6 [repeat 6 [ forward 5 right 60] right 60 ] ]

You should get something like this.

![starinhexagon.png](images/starinhexagon.png)

Very pretty, isn't it?

We can also tell the turtle to move backwards and to the left.

    ask turtles [ left 60 ]
    ask turtles [ back 4 ]

Okay, now let's clean up that mess we drew. This time we will create 2 turtles.

    clear-all
    create-turtles 2

Do you notice where the 2 turtles are? They are right on top of each other. Why don't we ask them to move?

    ask turtles [ pendown ]
    ask turtles [ forward 5 ]
    ask turtles [ right 180 ]

But what if we don't want them on top of each other? Okay, let's try this again:

    clear-all
    create-turtles 2 [setxy random-xcor random-ycor ]

Where are the turtles? Try running that command again.

    clear-all
    create-turtles 2 [setxy random-xcor random-ycor ]

Okay, now we made our turtles, let's tell them to move exactly like before.

    ask turtles [ pendown ]
    ask turtles [ forward 5 ]
    ask turtles [ right 60 ]
    ask turtles repeat 5 [ forward 5 right 60 ]

So what's happening? We're giving all the turtles the same set of instructions. So in this case, both turtles are moving, even though they are in different places.
Why don't you try the above code for 3 turtles? Or 5 turtles? Or more?

    clear-all
    create-turtles 10 [setxy random-xcor random-ycor ]
    ask turtles [ pendown ]
    ask turtles [ forward 5 ]
    ask turtles [ right 60 ]
    ask turtles repeat 5 [ forward 5 right 60 ]

## Time for some Exercises

## Can you make the following shapes?

### a triangle whose side is length 4 

![triangle.png](images/triangle.png)

### a square whose side is length 4 

![square.png](images/square.png)

### a rhombus whose side is length 4 and with angles of `120 degrees` and `60 degrees`

![rhombus.png](images/rhombus.png)

### a rectangle whose sides are 4 and 8 

![rectangle](images/rectangle.png)

## Extras!

### CHALLENGE: a five tipped star.

![5tippedstar.png](images/5tippedstar.png)

### BONUS ROUND: a six tipped star.

![6tippedstar.png](images/6tippedstar.png)

### CAN'T DO THIS: 4 squares inside a square

![squaresinsquare.png](images/squaresinsquare.png)

### ONE STEP FURTHER: 16 squares inside a square

![16squaresinsquare.png](images/16squaresinsquare.png)

Do you think you can remake any of the following shapes?
--
- [album of images](http://imgur.com/a/rEf7R)
- [rotating squares](http://logo.twentygototen.org/4gxRYOCe)
- [pretty scatterplot](http://logo.twentygototen.org/U-vJcCz3)
- [hexaflake](http://logo.twentygototen.org/AJeuVkKc)
- [asymmetric fractal tree](http://logo.twentygototen.org/rvgjjMiS)
- [fractal tree](http://logo.twentygototen.org/aiexE8RU)
