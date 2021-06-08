# Description-  programming logic project 
## ADS - IFPE
## Colleges: Gabriel Carvalho and Rodrigo Rocha
## Professor: Msc. Dr. Eugênio Saraiva

### Category: sales 
### Objectives: make easly for stores and clients to sell and purchase

### Language: 
> Python 

#### To this project we used tkinter with the program 'pages', thats helps to build GUI. We follow the "way" that pages build the elements for all the code (except in the third window, because we made it "alone"), so, the code could be smallest.

### imports
> We start importing tkinter as tk (to facilite along the code), and import Tkinter and tkk to exceptions. Was also necessary import os, PIL(for images) and sys.

### Building the class
> we build the class TopLevel (just like the standards) and start with de funcuntion init with the method "self" (it replace the necessity to use pack in every element)

### Using self and take tkinter 
> to create the code, build the elements self.name and pass the tkinter element.

### Building a window
> To build a window we use self.top(name top is not obrigatory, is just a standard)
~~~python
self.top = tk.Tk() #it starts the window
self.top.mainloop() #it close turns the window loop on
~~~

#### Between this line we create our window 

### Geometry 
> We need define the window geometry (or tkinter will build it 300x300 px) but in out code we put in fullsceen as an atribute.
~~~python
self.top.geometry("1280x720") #per exemple
self.name.atribute = "-fullscreen", True)
~~~

### Frames
> frames are used like divs in html, defining a space.
~~~python
self.framename = tk.Frame()
~~~
### Labels
>Labels are used to insert text and images in the program.
~~~python
self.labelname = tk.Label()
~~~
#### We also can select the "field" per exemple: put a label inside a frame. It looks like html:
~~~html
<body>
    <div>
    </div>
</body>
~~~
#### But, in python
~~~python
self.labelname = tk.Label(self.frame) # The frame tha we created above
~~~

#### Entry
> the entries are text area that always return a string (it looks like input command but we can't choose the type),(we can convert the type after but no do like int(input))
~~~python
self.entryname = tk.Entry()
~~~

#### Buttons
>The buttons are the part that recives commands, we can say that it's the main part of a GUI.
~~~python
self.buttonname = tk.Button()
~~~

#### RadioButtons
> Buttons that recive values and show to user choose one of them.
~~~python
self.radioButtonname = tk.Radiobutton()
~~~

### Elements 

#### place
> place is where we select the place of something( in the program we used width and height to set the size and the relative position for X and Y.)

~~~python
self.elementname.place() #I will use label as an exemple bellow
self.label.place(relx=0, rely=0.5, width=300, heitgh=150)
~~~

#### configure
> The most important part from the elements because we can can change everythig following tkinter.

~~~python
self.label.configure()
~~~
### Elements from configure:
* background : change the background color.

* activebacground : change the background color when the user click on the element.

* foreground : change the text color.

* activebacground : change the text color when the user click on the element.

* relief : change the border type.

* borderwidth : change the border size.

* disableforeground : use to disable some color when the user is not using.

* disablebackground : use to disable some color when the user is not using.

* cursor: change the cursor type when the user put the cursor on the element.

* font : change the font elements (font, size, family and weigth).

* justify: use to justify the text.

* anchor : use to set the position for the element.

* obs: use hexadecimal colors .

#### commands for the Buttons
> to make a button do something we use the element command (still into configure). Obs: if the button need to recive two or more commands, you need to use lambda function like:

~~~python
self.btn.configure(command=lambda:[self.command1(), self.command2()])
~~~

#### Destroying the previous window
> to destroy the window we use the name and the command destroy:

~~~python
self.top.destroy()
~~~

#### Building functions
> We can build functions to create a new window or for commands, but we need use self as a parameter
~~~ python
def function(self):
    pass
~~~

#### We can put the element from the same type, together(as in CSS), like:

~~~ python
self.label.configure(
    background = "#000000", #black
    foreground = "#ffffff", #white
    justify = "center",
    anchor = "w",
    cursor = "hand2",
    text = "Hello World"
)
~~~
