# Zanderman_News
# Zanderman-News
#logo
import time
import turtle
wn = turtle.Screen()
john = turtle.Turtle()
john.hideturtle()
wn.screensize(1000,1000)
# Making the Z
john.speed(0)
john.color("green")
john.begin_fill()
 
john.left(60)
john.forward(100)
john.left(120)
john.forward(100)
 
john.right(90)
john.forward(10)
john.right(90)
john.forward(120)
 
john.right(120)
john.forward(200)
john.left(120)
john.forward(100)
 
john.right(90)
john.forward(10)
john.right(90)
 
john.forward(120)
john.right(120)
john.forward(100)
 
john.end_fill()
 
# Making the circle
 
john.penup()
 
john.left(120)
john.forward(120)
john.left(90)
john.color("red")
john.pendown()
john.circle(140)
for i in range(10):
    john.left(10)
    john.circle(140)

#undoing logo
def undo(times, t):
  '''undos the previous code times times with turtle t'''
  
  for i in range(times):
    t.speed(0)
    t.undo()
    t.undo()
    
undo(42, john)

#drawing triangle
john.fillcolor("blue")
john.begin_fill()
john.left(120)
john.forward(100)
john.left(120)
john.forward(100)
john.left(120)
john.forward(100)
john.end_fill()
john.penup()
#getting to center of triangle (pythagorean theoream)
john.goto(0,1/2*((10000-2500)**0.5))
john.pendown()
#writing 1
style=('normal', 20, 'bold')
john.pencolor('white')
john.write('1', font=style, align='center')

john.right(90)
john.penup()
john.forward(100)
john.pencolor('black')
style=('normal', 30, 'bold')
john.pendown()
#top, writing to show channel 1
john.write('Channel', font=style, align='center')
john.hideturtle()
wn.bgcolor('lavender')
#timer (lily stalls time)
time.sleep(3)
#undo
undo(42, john)
john.write('Daily News', font=style, align='center')
john.hideturtle()
time.sleep(3)
undo(3, john)
john.penup()

style2=('normal', 20, 'bold')
story="Today's story is about TigerEye123."
john.left(90)
john.forward(100)
john.write(story, font=style2, align='center')
wn.bgcolor('lightblue')
john.hideturtle()
john.forward(-100)
style3=('normal', 10, 'bold')
report = 'Last week the great "jumper" TigerEye123 broke the long jumping world record, by jumping 10 feet."\n" TigerEye123 is now in the python hall of fame, and is known around the world.'

john.write(report, font = style3, align = 'center')
time.sleep(7)
undo(43, john)
john.fillcolor('navy')
john.goto(0,0)
john.begin_fill()
john.forward(-50)
for i in range(3):
  john.forward(100)
  john.left(120)
john.end_fill()
john.forward(50)
john.penup()
john.goto(0, 16)
john.pencolor('white') #We make the second story, channel 2
john.write('2', font=style, align='center')
john.left(90)
john.penup()
john.forward(100)
john.write('Channel', font=style, align='center')
john.hideturtle()
time.sleep(3)
undo(20, john)
john.hideturtle()
john.penup()
style=('normal', 15, 'bold')
john.home()
john.left(90)
john.forward(100)
john.right(180)
john.write("Weather Today:", font = style, align = 'center')
john.forward(50)
john.write("Hot and Humid, go for a walk!", font=style, align = 'center') #We tell the weather
john.forward(50)
john.write ("It's 6/22/20 and...", font=style, align = 'center') #Tell the date
john.forward(50)
john.write("That's it folks!", font=style, align = 'center')#We end with a that's it folks!
time.sleep(3)
undo(16,john)
john.penup()
style=('normal', 20, 'underline')
john.home()
john.write("Credits", font = style, align = 'center')#And here are the credits
john.left(90)
john.forward(100)
style=('normal', 20, 'bold')
john.write("ZANDERMAN NEWS",font = style, align = 'center')
john.right(180)
john.forward(150)
john.write("SparklyFlowers",font = style, align = 'center')#SparklyFlowers
john.forward(50)
john.write('TigerEye123', font = style, align = 'center')#TigerEye123
john.forward(50)
john.write("Zanderman", font = style, align = 'center')#And Zanderman
