---
layout: posts
title: my tree
---

import turtle

def snow( n , d ) :
    turtle.fillcolor( "white" )
    turtle.begin_fill()
    turtle.right( 90 )
    for _ in range( n  ):
        turtle.forward( d )
        turtle.left( 360 / n )
    turtle.left( 90 )
    turtle.end_fill()


def tree( d , r , s ) :
    if d < 20 or r < 10 :
        return
    turtle.pencolor( "lightSalmon4" )
    turtle.pensize( s )
    turtle.forward( d )
    turtle.left(  r)
    tree( d * 0.8 , r , s * 0.8 )
    turtle.pencolor( "white" )
    if  d < 30 :
        snow( 15 , 3 )
    turtle.right( 2 * r )
    turtle.pencolor( "lightSalmon4" )
    tree( d * 0.8 , r , s * 0.8 )
    turtle.pencolor( "lightSalmon4" )
    turtle.left( r )
    turtle.backward( d )

turtle.hideturtle()      
turtle.speed( 0 )
turtle.penup()
turtle.left( 90 )
turtle.backward( 100 )
turtle.pendown()
turtle.bgcolor( "lightblue1" )
turtle.hideturtle()
tree( 100 , 30 , 15 )
turtle.right( 90 )
turtle.pensize( 30 )
turtle.pencolor( "snow2" )
turtle.forward( 1000 )
turtle.backward( 2000 )
turtle.mainloop()
