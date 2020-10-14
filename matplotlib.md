# matplotlib
matplotlib has two methods for graphing data


- One uses MATLAB's plotting syntax
    MATLAB's plotting syntax is concise and the most useful when 
    creating simple plots that require little coding. This method 
    is most effective when graphing data directly from a DataFrame

- object-oriented interface
    better suited to more complicated graphs that require more 
    coding, such as those with multiple lines or bars, or multiple 
    plots in one graph.

must be imported as `import matplotlib.pyplot`

## Variables for pyplot
    #Set the x-axis to a list of strings for each month.
    x_axis = ["Jan", "Feb", "Mar", "April", "May", "June", "July", "Aug", "Sept", "Oct", "Nov", "Dec"]

    #Set the y-axis to a list of floats as the total fare in US dollars accumulated for each month.
    y_axis = [10.02, 23.24, 39.20, 35.42, 32.34, 27.04, 43.82, 10.56, 11.85, 27.90, 20.71, 20.09]


## function to generate a simple x and y axis line plot

    import matplotlib.pyplot

    X_axis=list_1

    Y_axis=list_2

    matplotlib.pyplot.xlabel("Label for Axis X")

    matplotlib.pyplot.ylabel("Label for Axis Y")

    matplotlib.pyplot.plot(X_axis,Y_axis)

    matplotlib.pyplot.show()

## Generate a Line Chart with object oriented interface

    import matplotlib.pyplot

    #matplotlib.pyplot.subplots() returns a tuple that contains a figure and axes objects, unpacked into variables fig and ax
    fig, ax = matplotlib.pyplot.subplots() 
    
    ax.plot(X_axis,Y_axis)


## Generate a Line Chart with object oriented interface without the tuple
    import matplotlib.pyplot

    #Create the plot with ax
    fig = matplotlib.pyplot.figure()
    
    ax = fig.add_subplot()
    
    ax.plot(x_axis, y_axis)

To change the figure level attributes(axis labels, title , legend) or dave the figure of the image use code below:

    fig = matplotlib.pyplot.figure()

## Annotiating charts with matplotlib Method

    Matplotlib Functions	    Feature
    
    plt.figure(figsize=(w, h)):	Change the size of the figure in pixels. Added on the first line of the script.
    
    plt.plot(x, y, label='line'): Add a label that will be added to the legend.

    plt.xlim(min, max):	Set the min and max range of the x-axis.
    
    plt.ylim(min, max):	Set the min and max range of the y-axis.
    
    plt.xlabel('x label'):	Add a label to the x-axis.
    
    plt.ylabel('y label'):	Add a label to the y-axis.
    
    plt.title("Title"):	Add a title.
    
    plt.legend():	Add a legend.
    
    plt.grid():	Add a grid to the chart.
    
    plt.savefig("add a path and figure extension"):	Save the figure with the given extension. Added at the end of the script.

## Example of anotating code
    import matplotlib.pyplot as plt

    #Create the plot and add a label for the legend.
    plt.plot(x_axis, y_axis, label='Boston')
    
    #Create labels for the x and y axes.
    plt.xlabel("Date")
    plt.ylabel("Fare($)")
    
    #Set the y limit between 0 and 45.
    plt.ylim(0, 45)
    
    #Create a title.
    plt.title("PyBer Fare by Month")
    
    #Add the legend.
    plt.legend()
    ____________________________________________________

    #Create the plot.
    plt.plot(x_axis, y_axis, marker="*", color="blue", linewidth=2, label='Boston')
    
    #Create labels for the x and y axes.
    plt.xlabel("Date")
    plt.ylabel("Fare($)")
    
    #Set the y limit between 0 and 45.
    plt.ylim(0, 45)
    
    #Create a title.
    plt.title("PyBer Fare by Month")
    
    #Add a grid.
    plt.grid()
    
    #Add the legend.
    plt.legend()


## Annotating using object oriented interface
    Matplotlib Object-Oriented Functions	Feature

    fig, ax = plt.subplots(figsize=(w, h)):	Change the size of the figure in pixels. Add this in the subplots() function.

    ax.plot(x, y, label='line'):	Add a label that will be added to the legend.
    
    ax.set_ylim(min, max):	Sets the min and max range of the y-axis.
    
    ax.set_xlim(min, max):	Sets the min and max range of the x-axis.
    
    ax.set_xlabel('x label'):	Add a label to the x-axis.
    
    ax.set_ylabel('y label'):	Add a label to the y-axis.
    
    ax.set_title("Title"):	Add a title.
    
    ax.legend():	Add a legend.
    
    ax.grid():	Add a grid to the chart.
    
    ** plt.savefig("add a path and figure extension"):	Saves the figure with the given extension. Added at the end of your script.


## Creating a vertical bar graph

    import matplotlib.pyplot

    matplotlib.pyplot.bar(x_axis,y_axis)

## Anotating the bar graph

    # Create the plot.
    matplotlib.pyplot.bar(x_axis, y_axis, color="green", label='Boston')
    
    # Create labels for the x and y axes.
    matplotlib.pyplot.xlabel("Date")
    matplotlib.pyplot.ylabel("Fare($)")
    
    # Create a title.
    matplotlib.pyplot.title("PyBer Fare by Month")
    
    # Add the legend.
    matplotlib.pyplot.legend()


## Creating a horizontal bar graph

    matplotlib.pyplot.barh(x_axis,y_axis)


`.gca()` will return the current axes


## Scatter plots

### Maplotlib method
- adding 'o' will create a scatterplot
    
    plt.plot(x_axis,y_axos,'o')

- or we can plot this way

    plt.scatter(x_axis, y_axis)

- adding the 's' argument will effect the size of the given axes

    plt.scatter(x_axis,y_axis,s=y_axis)

- editing size of the 's' argument can be done by editing the given axes

    plt.scatter(x_axis,y_axis,s=[i*3 for i in y_axis])

### Object oriented scatter plot
    
    fig, ax = plt.subplots()
    ax.scatter(x_axis, y_axis)


## Create a Pie Chart Using MATPLOTLIB method
    colors = ["slateblue", "magenta", "lightblue", "green", "yellowgreen", "greenyellow", "yellow", "orange", "gold", "indianred", "tomato", "mistyrose"]
    explode_values = (0, 0, 0, 0, 0, 0, 0.2, 0, 0, 0, 0, 0)
    plt.subplots(figsize=(8, 8))
    plt.pie(y_axis, labels=x_axis)
    explode_values = (0, 0, 0, 0, 0, 0, 0.2, 0, 0, 0, 0, 0)
    plt.pie(y_axis, explode=explode_values, labels=x_axis, autopct='%.1f%%',colors=colors)

- To explode a pie wedge, we use array-like data points (like the tuple explode_values = (0, 0, 0, 0, 0, 0, 0.2, 0, 0, 0, 0, 0)) for each value in the pie chart.
    - The length of the tuple should be equal to the number of wedges in the pie chart.
    - The value specified to "explode" a wedge is the fraction of the radius from the center of the pie for each wedge.
- To pop out the seventh month, July, we use a decimal-point value of 0.2.
- To add the percentage of each wedge on the pie chart, we use the autopct parameter and provide the format of one decimal place using .1f%.
- The % before and after the .1f% formats the number as a percentage.

## Create a Pie Chart using the object-oriented interface

