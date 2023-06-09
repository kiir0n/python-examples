# For Loops.
What is a for loop? Well a for loop is a loop in Python that will execute a block of code **for a limited amount of times**, kinda like while loops y'know. Here is an example:

1. Example one, looping through arrays.
2. Looping through tuples.
3. Looping through dictionaries ( objects in js ).

With that said lets get started!
# Looping through an array
```py
array = ["I love code","Python is my fav coding language","I absolutely suck at python"]
for i in range(len(array)):
    print(array[i])
```
What's going on here? Well first of all we defined an array in the `array` variable, `for i in range(len(array))` we basicaly defined our iterator as `i`.
Them we used `range()` which tells python in what range it should iterate. `len(array)` tells us the length of our array. 

# Looping through tuples.
```py
tuple = ("I love code","Python is my fav coding language","I absolutely suck at python")
for i in range(len(tuple)):
    print(tuple[i])
 ```
 What did we do here? Well basically we did the same thing in an array only thing is we change the array to a tuple.
 
 # Looping through a dictionary
 I will show you two examples, first one is dealing with `sub keys`
 ```py
 dictionary = {
    "bio": {
        "name" : "Kiir0n",
        "nickname" : "kia and kii",
        "age" : 0
    },
    "contacts" : {
        "discord" : "Kiir0n#0728",
        "twitter" : "@kiir0n",
        "instagram" : "@kiir0n",
        "youtube" : "@kiir0n_"
    }
}
for tkey in dictionary:
    print(f"Top level key, {tkey}")
    print(f"Value, {dictionary[tkey]}")
    sub_dictionary = dictionary[tkey]

    for sub_key in sub_dictionary:
        print(f"Sub key: {sub_key}")
        print("Value: ", sub_dictionary[sub_key])
 ```
In this example we provided a dictionary in the var `dictionary` with sub keys. Then we looped through the first top level keys ( keep in mind we can't use `len()` on a dictionary.
After that we then nested another `for` loop in our main loop with iterator sub_key using a defined variable named `sub_dictionary`
Then we repeated the same thing.

Here's an example without sub keys
```py
dictionary = {
        "name" : "Kiir0n",
        "nickname" : "kia and kii",
        "age" : 0,
        "discord" : "Kiir0n#0728",
        "twitter" : "@kiir0n",
        "instagram" : "@kiir0n",
        "youtube" : "@kiir0n_"
}
for tkey in dictionary:
    print(f"Key, {tkey}")
    print(f"Value, {dictionary[tkey]}")
```

# Looping through a list of dictionaries
In javascript it took me quite some time figuring this out but here is how you loop through a list of dictionaries, ofc 2 examples, one with and one without sub keys
```py
my_list = [{"key": "value"}]

for my_dict in my_list:
    for key, value in my_dict.items():
        print(f"Key: {key}")
        print(f"Value: {value}")
```

what did we do here? Well first off this is a dictionary list without sub keys, we first defined it in `my_list` then iterate over it with `for my_dict in my_list` then we make another for loop in it like `for key, value in my_dict.items()`, `.items()` method is used with dictionaries to return a view object containing key-value pairs. This method allows you to iterate over the key-value pairs of a dictionary.
Here is an example with sub keys
```py
my_list = [{"key1": {"sub_key1": "sub_value1", "sub_key2": "sub_value2"}},           {"key2": {"sub_key3": "sub_value3", "sub_key4": "sub_value4"}}]

for my_dict in my_list:
    for key, sub_dict in my_dict.items():
        print(f"Key: {key}")
        for sub_key, sub_value in sub_dict.items():
            print(f"Sub Key: {sub_key}")
            print(f"Sub Value: {sub_value}")
```

We basically do everything above, only this time the code creates a list with one dictionary that has one key-value pair. It then goes through the list and uses the .items() method to get each key-value pair from the dictionary. It then prints the key and value of each pair.
