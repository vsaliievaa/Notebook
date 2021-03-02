# Notebook
This code is an example to explain how Python classes work and was taken from "Python 3 Object Oriented Programming" (second edition) by Dusty Phillips.

## Installation
To run the program on your computer, download all the code files or clone a repository from GitHub, and run a user_menu.py file.
## Running
The app suggests a very simple and intuitive interface. First of all, the user will see a menu and available oprtions. To add a new note, the user should enter "3" and then the memo they want to add. A message about successful creation of a note will appear immediately after that.  
![Starting work](starting.png?raw="text")
To modify the existing note, the user has to enter "4" and, again, follow the prompts that appear.
![Starting work](modify_note.png?raw="text")
To search for a specific letter combination or show all the notes, the user should enter "2" and "1" respectively.
![Starting work](show_notes.png?raw="text")
Finally, to quit the notebook, the user has to press "5". 
![Starting work](final.png?raw="text")
## Dir(), type() and isinstance() functions
If we use dir() function for Notebook class or notebook.Notebook or notebook.Note objects, we'll see the lists of atrributes for each of these objects.
```python
>>> import notebook
>>> print(dir(notebook))
['Note', 'Notebook', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', 'datetime', 'last_id']
>>> print(dir(notebook.Note))
['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__',
'__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'match']
>>> print(dir(notebook.Notebook))
['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__',
'__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', '_find_note', 'modify_memo', 'modify_tags', 'new_note', 'search']
```
With the help of isinstance() function we can learn even more about classes. First, let's create a notepad and add a note to it. 
```python
>>> import notebook
>>> note = notebook.Note("First note")
>>> isinstance(note, object)
True
>>> notepad = notebook.Notebook()
>>> isinstance(notepad, object)
True
```
Let's now add a second note to it.
```python
>>> note_1 = notebook.Note("Second note")
>>> notepad.new_note(note, note_1)
```
If we use type() for each of the objects we created, we'll see the following:
```python
>>> type(note)
<class 'notebook.Note'>
>>> type(note_1)
<class 'notebook.Note'>
>>> type(notepad)
<class 'notebook.Notebook'>
```
