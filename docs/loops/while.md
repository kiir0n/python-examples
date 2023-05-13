# While Loops.
What is a while loop? Well a while loop is a loop in Python that will execute a block of code **as long as** the statement is true. Here is an example:


<code><pre>
name = input("Type in your name\n")
while not name:
    name = input("Type in your name\n")

print("Hey there "+name)</code></pre>


What did we just do?
Well we just made a simple while loop that prompts the user to enter their name, if **not name** ( which means if the name is empty ) we will reprompt the user
`name` is the variable with value `input()`
`while not name:` the statement 
