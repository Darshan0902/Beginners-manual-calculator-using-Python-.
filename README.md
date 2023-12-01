# Beginners-manual-calculator-using-Python-.


Before we begin breaking the code into a step by step format : 

## 1 -  SOURCE CODE : 

soruce_code.py

## 2- OUTPUTS : 


Screenshot 2023-12-01 130308.png

Screenshot 2023-12-01 131412.png

Screenshot 2023-12-01 134427.png


This code is a simple calculator GUI (Graphical User Interface) implemented using the Tkinter library in Python. 
Let's break down the code step by step:


## 3 - CODE BREAKDOWN : 

### 3.1 - Import Tkinter:

```
from tkinter import *

```
This line imports all classes and functions from the Tkinter library, which is used for creating GUI applications.

### 3.2 - Create the main window:

```
me = Tk()
me.geometry("354x460")
me.title("DARSHAN_CALCULATOR")

```
This initializes the main window (me) with a size of 354x460 pixels and sets the title to "DARSHAN_CALCULATOR."

### 3.3 - Configure the main window:

```
melabel = Label(me, text="CALCULATOR", bg='White', font=("Times", 30, 'bold'))
melabel.pack(side=TOP)
me.config(background='Dark gray')
```

This sets up a label at the top of the window with a white background and a bold Times font.
The main window background color is set to dark gray.


### 3.4 - Define variables and functions:

```
textin = StringVar()
operator = ""
```
textin is a StringVar variable used to store and update the display text in the calculator. operator is a string 
variable used to store the mathematical expression entered by the user.

### 3.5 - Define calculator functions:

```
def clickbut(number):
    global operator
    operator = operator + str(number)
    textin.set(operator)

def equlbut():
    global operator
    add = str(eval(operator))
    textin.set(add)
    operator = ''

def clrbut():
    textin.set('')
```

- clickbut: Appends the clicked number to the operator string and updates the display.
- equlbut: Evaluates the mathematical expression in operator using eval() and sets the result in the display.
- clrbut: Clears the display.

### 3.6 - Create the display entry widget:

```
metext = Entry(me, font=("Courier New", 12, 'bold'), textvar=textin, width=25, bd=5, bg='powder blue')
metext.pack()
```

This creates an entry widget for displaying and entering text. The widget is configured with a specific font, size, and color.


### 3.7 - Create number and operator buttons:

- Numeric buttons (0-9) and decimal point:

```
but1 = Button(me, padx=14, pady=14, bd=4, bg='white', command=lambda: clickbut(1), text="1", font=("Courier New", 16, 'bold'))
but1.place(x=10, y=100)

```

These buttons are created with specific properties such as size, border, background color, command to execute when clicked, and text to display.
The lambda function is used to pass arguments to the clickbut function.

- Operator buttons (+, -, *, /):

```
butpl = Button(me, padx=14, pady=14, bd=4, bg='white', text="+", command=lambda: clickbut("+"), font=("Courier New", 16, 'bold'))
butpl.place(x=205, y=100)

```

Similar to numeric buttons, these buttons have specific properties and call the clickbut function with the corresponding operator.


### 3.8 - Create other control buttons:

-  CLEAR BUTTON :
  
```
butclear = Button(me, padx=14, pady=119, bd=4, bg='white', text="CE", command=clrbut, font=("Courier New", 16, 'bold'))
butclear.place(x=270, y=100)
```

- EQUAL BUTTON : 

```
butequal = Button(me, padx=151, pady=14, bd=4, bg='white', command=equlbut, text="=", font=("Courier New", 16, 'bold'))
butequal.place(x=10, y=380)

```
These buttons have specific properties, trigger the corresponding functions when clicked, and display relevant text.

### 3.9 - Start the main loop:

```
me.mainloop()

```
This line starts the Tkinter main loop, allowing the GUI to run and respond to user interactions.


### 4 - NOTE : 
The code contains multiple equlbut functions with different calculations (addition, subtraction, multiplication, division). 
Only the last one will have an effect. If you want to support multiple operations, you should consider a different approach.



# Thank you and Regards;
## K. Darshan Prabhu;
### Aao Code Kare;
