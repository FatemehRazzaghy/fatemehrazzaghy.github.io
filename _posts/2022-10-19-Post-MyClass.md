---
layout: posts
title: My tree and jungle
---
_This is my tree_ 

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



_This is my jungle_

import turtle<br>
import time<br>
import random<br>
turtle.penup()<br>
turtle.setpos( 0 , -250 )<br>
turtle.pendown()<br>
turtle.right( 180 )<br>
turtle.pensize( 280 )<br>
turtle.pencolor( "peachpuff3" )<br>
turtle.forward( 1000 )<br>
turtle.backward( 2000 )<br>

turtle.right( 180 )<br>
list1=[ 'yellow3' , 'khaki1' , 'tan1' , 'lightsalmon' ]<br>
def leaf(n,d):<br>
    turtle.fillcolor( random.choice( list1 ) )<br>
    turtle.begin_fill()<br>
    turtle.right( 90 )<br>
    for _ in range( n ):<br>
        turtle.forward( d )<br>
        turtle.left( 360 / n )<br>
    turtle.left( 90 )<br>
    turtle.end_fill()<br>
def leaf1(n,d):<br>
    turtle.fillcolor( random.choice( list1 ) )<br>
    turtle.begin_fill()<br>
    turtle.left( 90 )<br>
    for _ in range( n ):<br>
        turtle.forward( d )<br>
        turtle.left( 360 / n )<br>
    turtle.left( 90 )<br>
    turtle.end_fill()<br>
def tree( d , a , r ) :<br>
    if d < random.randint( 13 , 14 ) or a < random.randint( 5 , 6 ) :<br>
        return<br>
    turtle.pencolor( 'lightsalmon4' )<br>
    turtle.pensize( r )<br>
    turtle.forward( d )<br>
    turtle.left( a )<br>
    tree( d * ( random.random() / 2 + 0.75 ) , a * ( random.random() / 2 + 0.5 ) , r * 0.8 )<br>
    if d < 20 :<br>
        turtle.pencolor( 'papayawhip' )<br>
        turtle.pensize( 0.0001 )<br>
        leaf( 5 , 8 )<br>
        leaf1( 5 , 8 )<br>
    turtle.pencolor( 'lightsalmon4' )<br>
    turtle.right( 2 * a )<br>
    tree( d * ( random.random() / 2 + 0.5 ) , a * ( random.random() / 2 + 0.5 ) , r * 0.8  )<br>
    if d < 20 :<br>
        turtle.pencolor( 'papayawhip' )<br> 
        turtle.pensize( 0.0001 )<br>
        leaf( 5 , 8 )<br>
        leaf1( 5 , 8 )<br>
    turtle.pencolor( 'lightsalmon4' )<br>
    turtle.left( a )<br>
    turtle.backward( d )<br>
turtle.left( 90 )<br>
turtle.tracer( 0 )<br>
for a in range( 10 , 25 , 5 ):<br>
    for r in range( 1 , 4 , 1 ):<br>
        turtle.hideturtle()<br>
        turtle.pensize( 7 )<br>
        turtle.penup()<br>
        turtle.setpos( random.randint( -500 , 300 ) , random.randint( -300 , -200 ) )<br>
        turtle.pendown() <br>
        tree( 60 , 25 , 10 )<br>
        turtle.penup()<br>
        turtle.setpos( 0 , -300 )<br>
        turtle.update()<br>
        time.sleep( 0.3 )<br>
        turtle.pendown()<br>
turtle.bgcolor( "lemonchiffon" )<br>
turtle.mainloop()<br>
