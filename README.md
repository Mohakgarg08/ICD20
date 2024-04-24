# ICS3U
ICS3U Course 

## Plotting a Function
  
#### My project is graphing an expression in the form of a(bx-h)+k. Samples of this can be sin(x), 2sin(4 x -5)+8, sin(x-5), sin(x)-5, and etc. It can be sin, cos or tan. This code can graph expressions. 
  
  steps to to graph the expression
    1. After running the code
    2. It will ask for your favorite color that is just the color of the graph.
    3. then it will ask for the expression to graph
    4. After entering it it will showcase the graph of the function you inputted.
  
  #### credits and Appreciation:
    libraries used
      •math
      •matplotlib
      •matplotlib
      •numpy
    This is where I copied codes for specific parts in my code which were amended according to my requirements.
      • https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.tight_layout.html#matplotlib.pyplot.tight_layout 
      • https://www.geeksforgeeks.org/plotting-sine-and-cosine-graph-using-matloplib-in-python/ 
      • https://stackoverflow.com/questions/31556446/how-to-draw-axis-in-the-middle-of-the-figure 
      • https://stackoverflow.com/questions/62160148/in-python-what-does-this-do-tan-y-1np-difftan-y-0

Sample:  2sin(2x+7)-4 

How to write my program? 

  1. First it is asking for the user’s favorite color; this is for the color of the graph.
  2. User is inputting its expression which is then split at the open parenthesis. Which will look like this ['2sin', '4 x -5)+8']
  3. second = expression[1].split(")"). This code is splitting the expression further at the closed parenthesis indexed at [1] in the list.This is what it looks like ['2sin', '4 x 
-5)+8'] ['4 x -5', '+8']
  4. third = second[0].split("x"). This code is splitting the expression further at x indexed at [0] in the second list. This is what it will look like ['2sin', '4 x -5)+8'] ['4 x -5', '+8'] ['4 ', ' -5']
  5. The second two lines of code are removing elements from the lists that we did not need.
  6. The function code is extracting the function from the user's input.
  7. The next line of code is extracting the elements to graph the expression. Extracting a,b,k,h from the lists.
  8. Also, setting their start value to 0 or 1 according to the formula.
  9. x = np.arange(0, 6 * np.pi, 0.1). This line is generating the x values for the graph
  10. y1 = a * np.sin(b * x - h) + k. This calculates the x values based on the function sin, cos, or Tan. This is also the formula for plotting the an expression which is a(bx-h)+k
  11. y1[:-1][np.diff(y1) < 0] = np.nan.  This is removing the lines of asymptotes. 
  12. fig = plt.figure(). This is making a figure for the graph
  13. ax = fig.add_subplot(1, 1, 1) # Move left y-axis and bottom, x-axis to center, passing through (0,0), ax.spines['left'].set_position('center'), ax.spines['bottom'].set_position('center'). These line of code is centering the axis so they can be seen on the graph
  14. plt.plot(x, y1,color=color). This is plotting the graph based on the x and y values. The color in this code is the color that the user chooses in the starting. 
   15. print(f"The color {color} is not available. Defaulting to BLUE."), plt.plot(x, y1, color="blue"). These two line of code is if the user’s color choice is not available or is invalid it will use the color blue on the graph
  16. plt.ylim(k - a, k + a). sets the y-axis limits to be from k - a to k + a, where k and a are values from the expression. This will show the graph of the expression. This means that the plot will only show data points with y-values within this range.
  17. plt.tight_layout() is a function that adjusts the layout of the plot so that the labels and titles fit nicely within the figure area. It adjusts the padding between the plot and the edges of the figure, and also adjusts the size of the plot to make sure everything fits.
  18. plt.legend([function.capitalize()],loc='upper right'), plt.xlabel("x",loc="left"), plt.ylabel("y",loc="bottom"), plt.title(f"{function.capitalize()}(x)"). This line of code is adding a legend of the function, x and y labels of the graph and the tile. loc is where the legend and the x and y labels should be on the graph. 
  19. plt.grid(True). This is showing the grid on the graph
  20. plt.show(). This is the function to show the graph.

How to use my program? 

  1. Open your Python program and run the script
  2. Enter a unique expression in the format provided ('sin(2x) + 1') when asked. Trigonometric functions such as "sin," "cos," or "tan" can be selected, and their variables (such as "2x") can be specified 
  3. Aftering entering the expression,
  4. Based on the provided expression, the code will create and display a plot of the function that illustrates the behavior of the function throughout the range of x-values from from k - a to k + a. The plot will be titled "the function(x)" and will include the function name. To understand the behavior of the function, including its magnitude, frequency, phase shift, and vertical shift, analyze the plotted graph
  
  
