# Spiky-Heart
This program draws a spiky green heart using the turtle graphics library in Python

Program Name: Spiky Green Heart
# Purpose:  The heart is created by plotting points based on mathematical functions that define the shape of the heart.
#           The turtle moves to each point and draws lines to create the spiky effect
#           The background is set to black, and the heart is colored bright green for a striking visual effect.
#           You can change the color of the heart by modifying the color code in the program I used "#39ff14" which is a bright green color.
# Coder: Neha Vishal
# Date: 2026-03-19



import math 
from turtle import *

def hearta(k):
    return 15*math.sin(k)**3

def heartb(k):
    return 12*math.cos(k)-5*math.cos(2*k)-2*math.cos(3*k)-math.cos(4*k)

speed(0)
bgcolor("black")
color("#39ff14")

penup()

for i in range(1, 1000, 3):
    x = hearta(i * 0.02) * 20
    y = heartb(i * 0.02) * 20
    
    penup()
    goto(0, 0)
    pendown()
    goto(x, y)

hideturtle()
done()
