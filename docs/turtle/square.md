# Simple square in turtle.
Like the title says we'll be making a simple square using the `turtle` module in python. For more info please refer to a turtle tutorial.

```py
import turtle

canvas = turtle.Turtle()
screen = canvas.getscreen()
screen.bgcolor("#336699")
canvas.pencolor("#fc0a24")
canvas.pensize(10)
canvas.right(90)
canvas.forward(100)
canvas.left(90)
canvas.backward(100)
canvas.left(90)
canvas.forward(100)
canvas.right(90)
canvas.forward(100)
turtle.done()
```

