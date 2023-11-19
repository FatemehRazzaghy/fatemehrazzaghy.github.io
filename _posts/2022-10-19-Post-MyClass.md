---
layout: posts
title: my tree
---

import turtle

def snow( n , d ) :<br>
    turtle.fillcolor( "white" )<br>
    turtle.begin_fill()<br>
    turtle.right( 90 )<br>
    for _ in range( n  ):<br>
        turtle.forward( d )<br>
        turtle.left( 360 / n )<br>
    turtle.left( 90 )<br>
    turtle.end_fill()<br>


def tree( d , r , s ) :<br>
    if d < 20 or r < 10 :<br>
        return<br>
    turtle.pencolor( "lightSalmon4" )<br>
    turtle.pensize( s )<br>
    turtle.forward( d )<br>
    turtle.left(  r)<br>
    tree( d * 0.8 , r , s * 0.8 )<br>
    turtle.pencolor( "white" )<br>
    if  d < 30 :<br>
        snow( 15 , 3 )<br>
    turtle.right( 2 * r )<br>
    turtle.pencolor( "lightSalmon4" )<br>
    tree( d * 0.8 , r , s * 0.8 )<br>
    turtle.pencolor( "lightSalmon4" )<br>
    turtle.left( r )<br>
    turtle.backward( d )<br>

turtle.hideturtle()      <br>
turtle.speed( 0 )<br>
turtle.penup()<br>
turtle.left( 90 )<br>
turtle.backward( 100 )<br>
turtle.pendown()<br>
turtle.bgcolor( "lightblue1" )<br>
turtle.hideturtle()<br>
tree( 100 , 30 , 15 )<br>
turtle.right( 90 )<br>
turtle.pensize( 30 )<br>
turtle.pencolor( "snow2" )<br>
turtle.forward( 1000 )<br>
turtle.backward( 2000 )<br>
turtle.mainloop()<br>
