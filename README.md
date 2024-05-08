# ICS3U
ICS3U Course 

## Plotting a Function
  
  #### My project is graphing an expression in the form of `a(bx-h)+k`. Samples of this can be `sin(x)`, `2sin(4 x -5)+8`, `sin(x-5)`, `sin(x)-5`, and etc. It can be sin, cos or tan. This code can graph expressions. 
  
  #### libraries used:
```   
libraries 
    •math
    •matplotlib
    •numpy
```
#### Reference

  - https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.tight_layout.html#matplotlib.pyplot.tight_layout 
  - https://www.geeksforgeeks.org/plotting-sine-and-cosine-graph-using-matloplib-in-python/ 
  - https://stackoverflow.com/questions/31556446/how-to-draw-axis-in-the-middle-of-the-figure 
  -  https://stackoverflow.com/questions/62160148/in-python-what-does-this-do-tan-y-1np-difftan-y-0


#### How to write my program?
Sample:  `2sin(2x+7)-4`
1. First it is asking for the user’s favorite color; this is for the color of the graph.

2. User is inputting its expression which is then split at the **open parenthesis**. Which will look like this `['2sin', '4 x -5)+8']`

3. **second = expression[1].split(")").** This code is splitting the expression further at the **closed parenthesis indexed at [1] in the list.** This is what it looks like **`['2sin', '4 x -5)+8'] ['4 x -5, '+8']`**

4. **`third = second[0].split("x").`** This code is splitting the expression further at **`x`** indexed at **`[0]` in the second list. This is what it will look like **`['2sin', '4 x -5)+8'] ['4 x -5', '+8'] ['4 ', ' -5']`**

5. The second two lines of code are removing elements from the lists that we did not need.

6. The function code is extracting the function from the user's input.

7. The next line of code is extracting the elements to graph the expression. Extracting **`a,b,k,h from the lists.`**

8. Also, setting their start value to 0 or 1 according to the formula.

9. **`x = np.arange(0, 6 * np.pi, 0.1).`** This line is generating the x values for the graph

10. **`y1 = a * np.sin(b * x - h) + k.`** This calculates the x values based on the function **sin, cos, or Tan.** This is also the formula for plotting the an expression which is **`a(bx-h)+k.`**

11. **`y1[:-1][np.diff(y1) < 0] = np.nan.`**  This is removing the lines of asymptotes. 

12. **`fig = plt.figure().`** This is making a figure for the graph

13. **`ax = fig.add_subplot(1, 1, 1)`** **Move left y-axis and bottom, x-axis to center, passing through (0,0), ax.spines['left'].set_position('center'), ax.spines['bottom'].set_position(`center`).** These line of code is centering the axis so they can be seen on the graph

14. **`plt.plot(x, y1,color=color).`** This is plotting the graph based on the x and y values. The color in this code is the color that the user chooses in the starting. 

15. **`print(f"The color {color} is not available. Defaulting to BLUE."), plt.plot(x, y1, color="blue").`** These two line of code is if the user’s color choice is not available or is invalid it will use the color blue on the graph

16. **`plt.ylim(k - a, k + a).`** sets the y-axis limits to be from k - a to k + a, where k and a are values from the expression. This will show the graph of the expression. This means that the plot will only show data points with y-values within this range.

17. **`plt.tight_layout()`** is a function that adjusts the layout of the plot so that the labels and titles fit nicely within the figure area. It adjusts the padding between the plot and the edges of the figure, and also adjusts the size of the plot to make sure everything fits.

18. **`plt.legend([function.capitalize()],loc='upper right'), plt.xlabel("x",loc="left"), plt.ylabel("y",loc="bottom"), plt.title(f"{function.capitalize()}(x)").`** This line of code is adding a legend of the function, x and y labels of the graph and the tile. **`loc`** is where the legend and the x and y labels should be on the graph. 

19. **`plt.grid(True).`** This is showing the grid on the graph

20. **`plt.show().`** This is the function to show the graph.


#### How to use my program? 
- Open your Python program and run the script
- Enter a unique expression in the format provided `('sin(2x) + 1')` when asked. Trigonometric functions such as `"sin," "cos," or "tan"` can be selected, and their variables (such as `"2x"`) can be specified 
- Aftering entering the expression, Based on the provided expression, the code will create and display a plot of the function that illustrates the behavior of the function throughout the range of `x-values` from `k - a to k + a`. The plot will be titled `"the function(x)"` and will include the function name 





## Scientific and Graphing Calculator
#### My project is a Scientific and Graphing Calculator that can calculate various problems. It can calculate basic calculations. Find the area of different shapes, graph polynomial and trigonometric expression. 

libraries used:
```
libraries 
  •math
  •Cmath
  •numpy
  •matplotlib
```

Reference
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.tight_layout.html#matplotlib.pyplot.tight_layout
https://www.geeksforgeeks.org/plotting-sine-and-cosine-graph-using-matloplib-in-python/
https://stackoverflow.com/questions/31556446/how-to-draw-axis-in-the-middle-of-the-figure
https://stackoverflow.com/questions/62160148/in-python-what-does-this-do-tan-y-1np-difftan-y-0


#### How the Program Works
1. import math,cmath, numpy as np & matplotlib.pyplot as plt 
2. def basic(): This code is defining a function called basic 
3. def calculation():  This code is defining a function called calculation which is inside of the basic function. This functions is for calculating basic calculations such as addition, subtraction, multiplication, division, power
4. solve= input("Enter The Expression. This is an example sample is (10+20/5*4**2) "). This code is asking the user for what they what to calculate 
5. print(f"{solve} = {eval(solve)}"). This code is solving their given calculation using  {eval(solve)}. The print statement is printing the answer to the users calculation
6. print("Invalid Input Please Try Again"). This line tells the user if its input is invalid and the while True: try and except block helps the user enter the input again. 
7. def operation(): This function is for mathematical operations such as sin, cos, tan, log, exp, sqrt
8. def sin(x): return math.sin(x), def cos(x):return math.cos(x), def tan(x): return math.tan(x), def log(x): return math.log(x), def exp(x): return math.exp(x), def sqrt(x):return math.sqrt(x). This block of code is defining functions for the different mathematical operations. 

9. 
```python
while True:
      op= input("What operation do you want to do (Square Root= sqrt, Sin = S, Cos = C,Tan = T, Log = L, Exponential = E: ) ").lower()
      inputs=["sqrt", "s","c","t","l","e"]
      if op in inputs:

        # For Sin, Cos, Tan, Log, Exp, sqrt
        while True:
          try:

            user = float(input("Give me the number: "))
            if op == "s":
              print(f"The sin of {user} = {sin(user)}")
              break
            elif op =="c":
              print(f"The cos of {user} = {cos(user)}")
              break
            elif op =="t":
              print(f"The tan of {user} = {tan(user)}")
              break
            elif op=="l":
              print(f"The log of {user} = {log(user)}")
              break
            elif op=="sqrt":
              print(f"The Square Root of {user} = {sqrt(user)}")
              break
            elif op=="e":
              print(f"The exponential of {user} = {exp(user)}")
              break
            else:
              print("Invalid Input Please Try Again")
          except:
            print("Invalid Input Please Try Again")
      else:
        print("Invalid Input Please Try Again")
```

  **``user = float(input("Give me the number: "))``**. This line is asking the user for the number, they want to solve.  according to their chosen mathematical operation. This snippet of code is solving and retuning answer for that mathematical operation. For example if the user's choice was **``sin``** the user will enter **``s``**. It will verify if ``s`` is a valid input. Then the program will ask for the number you want to solve for. After, providing it the number it will go the the correct path for that function and execute it and return the value to the user. 


```python
while True:
    user= input("Do you want to do (basic calculation(1)) or (mathematical functions(2))  ")
    if user=="1":
      calculation()
      break
    elif user == "2":
      operation()
      break
    else:
      print("Invalid Input Please Try Again")
```
  This snippet of code is asking the user to enter what they want to do basic calculation or mathematical operation. After, the program will jump to the function coreesponding to their input. 

```python
# This function is for solving the area
def area():
  # This function is for asking the user for the dimensions of that shape. This is for the shapes that have one input
  def oneinput(s):
    return float(input(f"Enter the {s}"))
  # This function is for asking the user for the dimensions of that shape. This is for the shapes that have two inputs
  def twoinputs(s1,s2):
    return (oneinput(s1),oneinput(s2))

  # Area of rectangle
  def rectangle(l,w):
    return (l*w)
  # Area of square
  def square(l):
    return (l**2)

  # area of a triangle
  def triangle(b,h):
   return(b*h/2)

  # area of circle
  def circle(r):
    pi = math.pi
    return(pi*r**2)
```
This snippet of code is the function for area. **``def oneinput(s):``** This function is asking the user for the dimension of the shape. **`` def twoinputs(s1,s2):``** This function is also asking them for the demsinsion for the shape. There are two functions because some shapes require one or two dimensions to solve for the area. After the user has entered the dimension(s), then it will solve and return the area of that specific shape the user asked for. 

```python
 while True:
    choice=input("What do you want to find the area of (rectangle(1), square(2), triangle(3), circle(4)) ").lower()

    if choice== "2":
      l=oneinput("length")
      a= square(l)
      print(f"The area of the square with the length {l}= {a}")
      break
    elif choice=="1":
      sides=twoinputs("length","width")
      a= rectangle(sides[0],sides[1])
      print (f"The area of the rectangle with the length {sides[0]}and width {sides[1]} = {a}")
      break
    elif choice=="3":
      sides=twoinputs("base","heights")
      a=triangle(sides[0],sides[1])
      print (f"The area of the triangle with the base {sides[0]}and hight {sides[1]} = {a}")
      break
    elif choice== "4":
      r=oneinput("Radius")
      a=circle(r)
      print (f"The area of the circle with the radius {r}= {a}")
      break
    else:
      print("Invalid Input Please Try Again ")
```

This snippet of code is asking the user what shape they want to find the area of. Then, it gets the dimensions of the shape from the user. After, it uses the functions given above to compute and return the area of the given shape.

```python
# This function is for the graphing calculator
def graphing():
  # This function is for graphing polynomials and also an optional linear line if the user has one
  def polynomial():
  # will make the user enter the expression again if it is invalid
    while True:
      try:
        #asking the user for the expression
        equation=input("Enter the expression in the form of (3*x**2 + 4*x + 6) (two * for power and one for multiply) ")

        # This is generating the x values
        x= np.linspace(-10,10,400)

        # evaluating the expression
        y= eval(equation)

        user= input("Do you have a linear expression ")

           # evaluating the linear expression
        if user=="yes":
          linear= input("Enter the linear expression. sample of this is (3*x+2) ")
          y2=eval(linear)
          plt.plot(x,y2)

        #plotting the function
        plt.title(equation)
        plt.xlabel("x")
        plt.ylabel("y")
        plt.grid(True)
        plt.plot(x,y)
        break
      except (ValueError,NameError,ZeroDivisionError, OverflowError, SyntaxError):
        print("Invalid Input Please Try Again")
        plt.clf()
```
This snippet of code is asking the user for the **polynomial expression** they want to graph. Then, it asks the user if they have a **linear expression** to graph as well. If **``yes``**, then it will ask the for the **linear expression** and graph both. Otherwise, it will graph the polynomial by it self. 

```python
def trignometry():
    # This is the color for the graph/ User input for favorite color
    color = input("What is your favorite color? ").replace(" ", "")

    while True:
        # User input for expression
        expression = input("What is the expression? Sample of this is (2sin(4 x -5)+8) ").split("(")

        try:
          # Extracting coefficient from the expression
            first = expression
            second = expression[1].split(")")
            third = second[0].split("x")
            first.remove(first[1])
            second.remove(second[0])
          # Trigonometry function
            function = first[0][-3:]

            # a
            a = first[0][:-3]
            if a == "":
                a = 1
            a = float(a)

            # k
            k = second[0]
            if k == "":
                k = 0
            k = float(k)

            # h
            h = third[1]
            if h == "":
                h = 0
            h = float(h)

            # b
            b = third[0]
            if b == "":
                b = 1
            b = float(b)
            break
        except:
            print("Cannot Graph Please Try Again")

    # Generate x values
    x = np.arange(0, 6 * np.pi, 0.1)

    # Calculate y values based on the selected function
    if function == "sin":
        y1 = a * np.sin(b * x - h) + k
    elif function == "cos":
        y1 = a * np.cos(b * x - h) + k
    elif function == "tan":
        y1 = a * np.tan(b * x - h) + k
        y1[:-1][np.diff(y1) < 0] = np.nan

    # Create the plot
    try:
        fig = plt.figure()
        ax = fig.add_subplot(1, 1, 1)
        # Move left y-axis and bottom x-axis to center, passing through (0,0)
        ax.spines['left'].set_position('center')
        ax.spines['bottom'].set_position('center')
        plt.plot(x, y1,color=color)

    except ValueError:

        print(f"The color {color} is not available. Defaulting to BLUE.")
        plt.plot(x, y1, color="blue")

    plt.ylim(k - a, k + a)
    plt.tight_layout()
    plt.legend([function.capitalize()],loc='upper right')
    plt.xlabel("x",loc="left")
    plt.ylabel("y",loc="bottom")
    plt.title(f"{function.capitalize()}(x)")
    plt.grid(True)
    plt.show()
```
This snippet of code is graphing **trigonometric expressions**. First, it asks the user for the **trigonometric expression**. Then, it extracts the coefficients from the user's given expression, which it then uses to graph the function according to the user's expression.

```python
 while True:
    user= input("What do want to do (1 for polynomial graph) (2 for trig graph)")
    if user=="1":
      polynomial()
      break
    elif user=="2":
      trignometry()
      break
    else:
      print("Invalid Input Please Try Again")
```
This snippet of code is asking the user what they want to graph; **polynomials** or  **trigonometric expressions**. Then, it jumps to the coressponding function.

###### 
```python
def main():

  while True:
    print("Enter (1) for Basic Calculations")
    print("Enter (2) for finding the area")
    print("Enter (3) for Graphing Calculator")

    calculator=input("What do you want to do? ")

    if calculator== "1":
      basic()
      break
    elif calculator=="2":
      area()
      break
    elif calculator=="3":
      graphing()
      break
    else:
      print("Invalid Input Please Try Agian")

main()
```
This snippet of code is the start of the program after running the program. This snippet of code is asking the user what they want to do; **Basic Calculator**, **area calculator**, or **Graphing Calculator**. Acordin to the user choice it will jump to that 
